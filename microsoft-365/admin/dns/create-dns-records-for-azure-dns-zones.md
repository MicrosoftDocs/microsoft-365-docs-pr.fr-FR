---
title: Créer des enregistrements DNS pour les zones DNS Azure
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
- Adm_O365_Setup
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: fbcef2d7-ebaf-40d0-ba1f-cdaeff9f50ef
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype Entreprise Online et d’autres services dans les zones DNS Azure pour Microsoft.
ms.openlocfilehash: be4baa80d0f96e92dc9dd9004054f29f12f6415b
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50916141"
---
# <a name="create-dns-records-for-azure-dns-zones"></a><span data-ttu-id="c4a4c-103">Créer des enregistrements DNS pour les zones DNS Azure</span><span class="sxs-lookup"><span data-stu-id="c4a4c-103">Create DNS records for Azure DNS zones</span></span>

 <span data-ttu-id="c4a4c-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="c4a4c-105">Si Azure est votre fournisseur d’hébergement DNS, suivez les étapes de cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-105">If Azure is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="c4a4c-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-106">These are the main records to add.</span></span> 
  
- [<span data-ttu-id="c4a4c-107">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="c4a4c-107">Change your domain's nameserver (NS) records</span></span>](#change-your-domains-nameserver-ns-records)
    
- [<span data-ttu-id="c4a4c-108">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="c4a4c-108">Add a TXT record for verification</span></span>](#add-a-txt-record-for-verification)

- [<span data-ttu-id="c4a4c-109">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="c4a4c-109">Add an MX record so email for your domain will come to Microsoft</span></span>](#add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft)
    
- [<span data-ttu-id="c4a4c-110">Ajouter les quatre enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="c4a4c-110">Add the four CNAME records that are required for Microsoft</span></span>](#add-the-four-cname-records-that-are-required-for-microsoft)
    
- [<span data-ttu-id="c4a4c-111">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="c4a4c-111">Add a TXT record for SPF to help prevent email spam</span></span>](#add-a-txt-record-for-spf-to-help-prevent-email-spam)
    
- [<span data-ttu-id="c4a4c-112">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="c4a4c-112">Add the two SRV records that are required for Microsoft</span></span>](#add-the-two-srv-records-that-are-required-for-microsoft)
    
<span data-ttu-id="c4a4c-113">Une fois ces enregistrements ajoutés sur Azure, votre domaine est installé pour fonctionner avec les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-113">After you add these records at Azure, your domain will be set up to work with Microsoft services.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c4a4c-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="c4a4c-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="c4a4c-117">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="c4a4c-117">Change your domain's nameserver (NS) records</span></span>
<span data-ttu-id="c4a4c-118"><a name="BKMK_NS"> </a></span><span class="sxs-lookup"><span data-stu-id="c4a4c-118"><a name="BKMK_NS"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4a4c-119">Vous devez effectuer cette procédure au niveau du bureau d'enregistrement de domaines auprès duquel vous avez acheté et inscrit votre domaine.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-119">You must perform this procedure at the domain registrar where you purchased and registered your domain.</span></span> 
  
<span data-ttu-id="c4a4c-120">Lorsque vous vous êtes inscrit à Azure, vous avez créé un groupe de ressources dans une zone DNS, puis affecté votre nom de domaine à ce groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-120">When you signed up for Azure, you created a resource group within a DNS zone, and then assigned your domain name to that resource group.</span></span> <span data-ttu-id="c4a4c-121">Ce nom de domaine est inscrit auprès d’un bureau d’enregistrement de domaines externe . Azure ne propose pas de services d’inscription de domaine.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-121">That domain name is registered to an external domain registrar; Azure does not offer domain registration services.</span></span>
  
<span data-ttu-id="c4a4c-122">Pour vérifier et créer des enregistrements DNS pour votre domaine dans Microsoft, vous devez d’abord modifier les serveurs de noms de votre bureau d’enregistrement de domaines afin qu’ils utilisent les serveurs de noms Azure affectés à votre groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-122">To verify and create DNS records for your domain in Microsoft, you first need to change the nameservers at your domain registrar so that they use the Azure nameservers assigned to your resource group.</span></span>
  
<span data-ttu-id="c4a4c-123">Pour modifier vous-même les serveurs de noms de votre domaine sur le site web de votre bureau d'enregistrement de domaines, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-123">To change your domain's name servers at your domain registrar's website yourself, follow these steps.</span></span>
  
1. <span data-ttu-id="c4a4c-124">Identifiez la zone sur le site web du bureau d'enregistrement de domaines dans laquelle vous pouvez modifier les serveurs de noms pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-124">Find the area on the domain registrar's website where you can edit the nameservers for your domain.</span></span>
    
2. <span data-ttu-id="c4a4c-125">Créez deux enregistrements de nameserver à l’aide des valeurs du tableau suivant, ou modifiez les enregistrements de nameserver existants afin qu’ils correspondent à ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-125">Either create two nameserver records by using the values in the following table, or edit the existing nameserver records so that they match these values.</span></span> <span data-ttu-id="c4a4c-126">Vous trouverez ci-dessous un exemple de serveurs de noms affectés à Azure.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-126">An example of Azure assigned nameservers is shown below.</span></span>
    


<span data-ttu-id="c4a4c-127">**Premier nameserver :** Utilisez la valeur de serveur de noms attribuée par Azure.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-127">**First nameserver:** Use the name server value assigned by Azure.</span></span>  
<span data-ttu-id="c4a4c-128">**Second nameserver:** Utilisez la valeur de serveur de noms attribuée par Azure.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-128">**Second nameserver:** Use the name server value assigned by Azure.</span></span>  

![Azure-BP-Redelegate-1-1](../../media/3e4805ea-608a-4df9-8f68-1fbf70d13d08.png)
  
> [!TIP]
> <span data-ttu-id="c4a4c-130">You should use at least two name server records.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-130">You should use at least two name server records.</span></span> <span data-ttu-id="c4a4c-131">Si d’autres serveurs de noms sont répertoriés sur le site web de votre bureau d’enregistrement de domaines, vous devez les supprimer.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-131">If there are any other name servers listed at your domain registrar's website, you should delete them.</span></span> 
  
3. <span data-ttu-id="c4a4c-132">Enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-132">Save your changes.</span></span>
    
> [!NOTE]
> <span data-ttu-id="c4a4c-133">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-133">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span></span> <span data-ttu-id="c4a4c-134">Ensuite, votre messagerie Microsoft et d’autres services seront tous définies pour fonctionner avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-134">Then your Microsoft email and other services will be all set to work with your domain.</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="c4a4c-135">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="c4a4c-135">Add a TXT record for verification</span></span>
<span data-ttu-id="c4a4c-136"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="c4a4c-136"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="c4a4c-p106">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-p106">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c4a4c-p107">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-p107">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="c4a4c-141">To get started, go to your domains page at Azure by using [this link](https://portal.azure.com ).</span><span class="sxs-lookup"><span data-stu-id="c4a4c-141">To get started, go to your domains page at Azure by using [this link](https://portal.azure.com ).</span></span> <span data-ttu-id="c4a4c-142">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-142">You'll be prompted to log in first.</span></span>
    
    ![Azure-BP-Configure-1-1](../../media/ed377cad-0c47-4f9f-b322-c3e06b309b1f.png)
  
2. <span data-ttu-id="c4a4c-144">À **l’aide de la barre de recherche** sur la page Tableau **de** bord, tapez dans les **zones DNS**.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-144">Using the **search bar** on the **Dashboard** page, type in **DNS zones**.</span></span> <span data-ttu-id="c4a4c-145">Dans l’affichage des résultats, sélectionnez les **zones DNS** sous la **partie Services.**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-145">In the results display, select **DNS zones** under the **Services** portion.</span></span> <span data-ttu-id="c4a4c-146">Une fois que vous avez été redirigé, sélectionnez le domaine à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-146">Once you've been redirected, select the domain that you want to update.</span></span>
    
    ![Azure-BP-Configure-1-2](../../media/eb4baad2-92d7-49c9-95e5-1dd8510d5ec9.png)
  
3. <span data-ttu-id="c4a4c-148">Dans la page **Paramètres** de votre domaine, dans la zone **de zone DNS,** **sélectionnez + Jeu d’enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-148">On the **Settings** page for your domain, in the **DNS zone** area, select **+ Record set**.</span></span>
    
    ![Azure-BP-Configure-1-3](../../media/b04db89a-3dbc-4cd2-aaca-af17fda53a60.png)
  
4. <span data-ttu-id="c4a4c-150">Dans la **zone Ajouter un jeu d’enregistrement,** dans les zones du nouveau jeu d’enregistrement, sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-150">In the **Add record set** area, in the boxes for the new record set, select the values from the following table.</span></span> 
    
    <span data-ttu-id="c4a4c-151">(Choisissez les **valeurs des** unités Type et **TTL** dans les listes de listes.)</span><span class="sxs-lookup"><span data-stu-id="c4a4c-151">(Choose the **Type** and **TTL unit** values from the drop-down lists.)</span></span> 
    
    |<span data-ttu-id="c4a4c-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-152">**Name**</span></span>|<span data-ttu-id="c4a4c-153">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-153">**Type**</span></span>|<span data-ttu-id="c4a4c-154">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-154">**TTL**</span></span>|<span data-ttu-id="c4a4c-155">**Unité TTL**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-155">**TTL unit**</span></span>|<span data-ttu-id="c4a4c-156">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-156">**Value**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="c4a4c-157">TXT</span><span class="sxs-lookup"><span data-stu-id="c4a4c-157">TXT</span></span>  <br/> |<span data-ttu-id="c4a4c-158">1</span><span class="sxs-lookup"><span data-stu-id="c4a4c-158">1</span></span>  <br/> |<span data-ttu-id="c4a4c-159">Heures</span><span class="sxs-lookup"><span data-stu-id="c4a4c-159">Hours</span></span>  <br/> |<span data-ttu-id="c4a4c-160">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="c4a4c-160">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="c4a4c-161">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-161">**Note:** This is an example.</span></span> <span data-ttu-id="c4a4c-162">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-162">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="c4a4c-163">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="c4a4c-163">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Azure-BP-Verify-1-1](../../media/7d5a253c-e88f-4565-a00a-79bba52f9970.png)
  
5. <span data-ttu-id="c4a4c-165">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-165">Select **OK**.</span></span>
  
6. <span data-ttu-id="c4a4c-166">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-166">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="c4a4c-167">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-167">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="c4a4c-168">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-168">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="c4a4c-169">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-169">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="c4a4c-170">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-170">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="c4a4c-171">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-171">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="c4a4c-172">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-172">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="c4a4c-p111">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="c4a4c-p111">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="c4a4c-176">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="c4a4c-176">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="c4a4c-177"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="c4a4c-177"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="c4a4c-178">To get started, go to your domains page at Azure by using [this link](https://portal.azure.com ).</span><span class="sxs-lookup"><span data-stu-id="c4a4c-178">To get started, go to your domains page at Azure by using [this link](https://portal.azure.com ).</span></span> <span data-ttu-id="c4a4c-179">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-179">You'll be prompted to log in first.</span></span>
    
    ![Azure-BP-Configure-1-1](../../media/ed377cad-0c47-4f9f-b322-c3e06b309b1f.png)
  
2. <span data-ttu-id="c4a4c-181">Dans la page **Tableau de** bord, dans la zone **Toutes** les ressources, sélectionnez le domaine à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-181">On the **Dashboard** page, in the **All resources** area, select the domain that you want to update.</span></span> 
    
    ![Azure-BP-Configure-1-2](../../media/eb4baad2-92d7-49c9-95e5-1dd8510d5ec9.png)
  
3. <span data-ttu-id="c4a4c-183">Dans la page **Paramètres** de votre domaine, dans la zone **de zone DNS,** **sélectionnez + Jeu d’enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-183">On the **Settings** page for your domain, in the **DNS zone** area, select **+ Record set**.</span></span>
    
    ![Azure-BP-Configure-1-3](../../media/b04db89a-3dbc-4cd2-aaca-af17fda53a60.png)
  
4. <span data-ttu-id="c4a4c-185">Dans la **zone Ajouter un jeu d’enregistrement,** dans les zones du nouveau jeu d’enregistrement, sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-185">In the **Add record set** area, in the boxes for the new record set, select the values from the following table.</span></span> 
    
    <span data-ttu-id="c4a4c-186">(Choisissez les **valeurs des** unités Type et **TTL** dans les listes de listes.)</span><span class="sxs-lookup"><span data-stu-id="c4a4c-186">(Choose the **Type** and **TTL unit** values from the drop-down lists.)</span></span> 
    
    |<span data-ttu-id="c4a4c-187">**Name**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-187">**Name**</span></span>|<span data-ttu-id="c4a4c-188">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-188">**Type**</span></span>|<span data-ttu-id="c4a4c-189">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-189">**TTL**</span></span>|<span data-ttu-id="c4a4c-190">**Unité TTL**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-190">**TTL unit**</span></span>|<span data-ttu-id="c4a4c-191">**Preference (Préférence)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-191">**Preference**</span></span>|<span data-ttu-id="c4a4c-192">**Mail Exchange**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-192">**Mail Exchange**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="c4a4c-193">MX</span><span class="sxs-lookup"><span data-stu-id="c4a4c-193">MX</span></span>  <br/> |<span data-ttu-id="c4a4c-194">1</span><span class="sxs-lookup"><span data-stu-id="c4a4c-194">1</span></span>  <br/> |<span data-ttu-id="c4a4c-195">Heures</span><span class="sxs-lookup"><span data-stu-id="c4a4c-195">Hours</span></span>  <br/> |<span data-ttu-id="c4a4c-196">10 </span><span class="sxs-lookup"><span data-stu-id="c4a4c-196">10</span></span>  <br/> <span data-ttu-id="c4a4c-197">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](../setup/domains-faq.yml).</span><span class="sxs-lookup"><span data-stu-id="c4a4c-197">For more information about priority, see [What is MX priority?](../setup/domains-faq.yml)</span></span> <br/> | <span data-ttu-id="c4a4c-198">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="c4a4c-198">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="c4a4c-199">**Remarque :** Obtenez votre *\<domain-key\>* depuis votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-199">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>   [<span data-ttu-id="c4a4c-200">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="c4a4c-200">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)  
   
    ![Azure-BP-Configure-2-1](../../media/712c23ae-9d38-4af2-94e0-0704e70744fe.png)
  
5. <span data-ttu-id="c4a4c-202">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-202">Select **OK**.</span></span>
    
    ![Azure-BP-Configure-2-2](../../media/2f24225f-69ac-41dc-91c5-93d327360f74.png)
  
6. <span data-ttu-id="c4a4c-204">Si d’autres enregistrements MX sont répertoriés dans la section **Enregistrements MX,** vous devez les supprimer.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-204">If there are any other MX records listed in the **MX Records** section, you must delete them.</span></span> 
    
    <span data-ttu-id="c4a4c-205">Tout d’abord, dans la **zone DNS,** sélectionnez le jeu d’enregistrement **MX**.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-205">First, in the **DNS zone** area, select the **MX Record set**.</span></span>
    
    ![Azure-BP-Configure-2-3](../../media/9890da61-6fcd-4c61-888e-ccbb84f80cd0.png)
  
    <span data-ttu-id="c4a4c-207">Ensuite, sélectionnez l’enregistrement MX à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-207">Next, select the MX record you want to delete.</span></span>
    
    ![Azure-BP-Configure-2-4](../../media/afe54f12-66d2-4ff3-80e9-427448e4c32c.png)
  
7. <span data-ttu-id="c4a4c-209">Sélectionnez **le menu Context (...)**, puis choisissez **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-209">Select the **Context menu (…)**, and then choose **Remove**.</span></span>
    
    ![Azure-BP-Configure-2-5](../../media/25219e25-bc14-4bc7-84ed-ee65eb28a8ed.png)
  
8. <span data-ttu-id="c4a4c-211">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-211">Select **Save**.</span></span>
    
    ![Azure-BP-Configure-2-6](../../media/c6133096-5e43-4637-9c01-b63ee4b03517.png)
  
## <a name="add-the-four-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="c4a4c-213">Ajouter les quatre enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="c4a4c-213">Add the four CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="c4a4c-214"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="c4a4c-214"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="c4a4c-215">To get started, go to your domains page at Azure by using [this link](https://portal.azure.com ).</span><span class="sxs-lookup"><span data-stu-id="c4a4c-215">To get started, go to your domains page at Azure by using [this link](https://portal.azure.com ).</span></span> <span data-ttu-id="c4a4c-216">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-216">You'll be prompted to log in first.</span></span>
    
    ![Azure-BP-Configure-1-1](../../media/ed377cad-0c47-4f9f-b322-c3e06b309b1f.png)
  
2. <span data-ttu-id="c4a4c-218">Dans la page **Tableau de** bord, dans la zone **Toutes** les ressources, sélectionnez le domaine à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-218">On the **Dashboard** page, in the **All resources** area, select the domain that you want to update.</span></span> 
    
    ![Azure-BP-Configure-1-2](../../media/eb4baad2-92d7-49c9-95e5-1dd8510d5ec9.png)
  
3. <span data-ttu-id="c4a4c-220">Dans la page **Paramètres** de votre domaine, dans la zone **de zone DNS,** **sélectionnez + Jeu d’enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-220">On the **Settings** page for your domain, in the **DNS zone** area, select **+ Record set**.</span></span>
    
    ![Azure-BP-Configure-1-3](../../media/b04db89a-3dbc-4cd2-aaca-af17fda53a60.png)
  
4. <span data-ttu-id="c4a4c-222">Ajoutez le premier des quatre enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-222">Add the first of the four CNAME records.</span></span>
    
    <span data-ttu-id="c4a4c-223">Dans la **zone Ajouter** un jeu d’enregistrement, dans les zones du nouveau jeu d’enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-223">In the **Add record set** area, in the boxes for the new record set, type or copy and paste the values from the first row in the following table.</span></span> 
    
    <span data-ttu-id="c4a4c-224">(Choisissez les **valeurs des** unités Type et **TTL** dans les listes de listes.)</span><span class="sxs-lookup"><span data-stu-id="c4a4c-224">(Choose the **Type** and **TTL unit** values from the drop-down lists.)</span></span> 
    
    |<span data-ttu-id="c4a4c-225">**Name**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-225">**Name**</span></span>|<span data-ttu-id="c4a4c-226">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-226">**Type**</span></span>|<span data-ttu-id="c4a4c-227">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-227">**TTL**</span></span>|<span data-ttu-id="c4a4c-228">**Unité TTL**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-228">**TTL unit**</span></span>|<span data-ttu-id="c4a4c-229">**Alias**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-229">**Alias**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="c4a4c-230">autodiscover</span><span class="sxs-lookup"><span data-stu-id="c4a4c-230">autodiscover</span></span>  <br/> |<span data-ttu-id="c4a4c-231">CNAME</span><span class="sxs-lookup"><span data-stu-id="c4a4c-231">CNAME</span></span>  <br/> |<span data-ttu-id="c4a4c-232">1</span><span class="sxs-lookup"><span data-stu-id="c4a4c-232">1</span></span>  <br/> |<span data-ttu-id="c4a4c-233">Heures</span><span class="sxs-lookup"><span data-stu-id="c4a4c-233">Hours</span></span>  <br/> |<span data-ttu-id="c4a4c-234">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="c4a4c-234">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="c4a4c-235">sip</span><span class="sxs-lookup"><span data-stu-id="c4a4c-235">sip</span></span>  <br/> |<span data-ttu-id="c4a4c-236">CNAME</span><span class="sxs-lookup"><span data-stu-id="c4a4c-236">CNAME</span></span>  <br/> |<span data-ttu-id="c4a4c-237">1</span><span class="sxs-lookup"><span data-stu-id="c4a4c-237">1</span></span>  <br/> |<span data-ttu-id="c4a4c-238">Heures</span><span class="sxs-lookup"><span data-stu-id="c4a4c-238">Hours</span></span>  <br/> |<span data-ttu-id="c4a4c-239">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="c4a4c-239">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="c4a4c-240">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="c4a4c-240">lyncdiscover</span></span>  <br/> |<span data-ttu-id="c4a4c-241">CNAME</span><span class="sxs-lookup"><span data-stu-id="c4a4c-241">CNAME</span></span>  <br/> |<span data-ttu-id="c4a4c-242">1</span><span class="sxs-lookup"><span data-stu-id="c4a4c-242">1</span></span>  <br/> |<span data-ttu-id="c4a4c-243">Heures</span><span class="sxs-lookup"><span data-stu-id="c4a4c-243">Hours</span></span>  <br/> |<span data-ttu-id="c4a4c-244">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="c4a4c-244">webdir.online.lync.com</span></span>  <br/> |
    
   
    ![Azure-BP-Configure-3-1](../../media/a1c4d869-da97-43b3-952c-d513a20231dc.png)
  
5. <span data-ttu-id="c4a4c-246">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-246">Select **OK**.</span></span>
    
    ![Azure-BP-Configure-3-2](../../media/b89b51da-1c07-43cf-9fab-75d2e5eb3544.png)
  
6. <span data-ttu-id="c4a4c-248">Ajoutez chacun des trois autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-248">Add each of the other three CNAME records.</span></span>
    
    <span data-ttu-id="c4a4c-249">Dans la **zone de zone DNS,** sélectionnez **+ Jeu d’enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-249">In the **DNS zone** area, select **+ Record set**.</span></span> <span data-ttu-id="c4a4c-250">Ensuite, dans le jeu d’enregistrement vide, créez un enregistrement en utilisant les valeurs de la ligne suivante du tableau, puis sélectionnez de nouveau **OK** pour terminer cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-250">Then, in the empty record set, create a record by using the values from the next row in the table, and again select **OK** to complete that record.</span></span> 
    
    <span data-ttu-id="c4a4c-251">Répétez ce processus jusqu’à ce que vous avez créé les quatre enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-251">Repeat this process until you have created all four CNAME records.</span></span>
    
7.  <span data-ttu-id="c4a4c-252">(Facultatif) Ajoutez 2 enregistrements CNAME pour la gestion des enregistrements de gestion des données.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-252">(Optional) Add 2 CNAME records for MDM.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4a4c-253">Si vous avez la gestion des périphériques mobiles (MDM) pour Microsoft, vous devez créer deux enregistrements CNAME supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-253">If you have Mobile Device Management (MDM) for Microsoft, then you must create two additional CNAME records.</span></span> <span data-ttu-id="c4a4c-254">Suivez la procédure que vous avez utilisée pour les quatre autres enregistrements CNAME, mais fournissez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-254">Follow the procedure that you used for the other four CNAME records, but supply the values from the following table.</span></span> <span data-ttu-id="c4a4c-255">(Si vous n’avez pas de gestion des mdm, vous pouvez ignorer cette étape.)</span><span class="sxs-lookup"><span data-stu-id="c4a4c-255">(If you do not have MDM, you can skip this step.)</span></span> 
  
|<span data-ttu-id="c4a4c-256">**Name**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-256">**Name**</span></span>|<span data-ttu-id="c4a4c-257">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-257">**Type**</span></span>|<span data-ttu-id="c4a4c-258">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-258">**TTL**</span></span>|<span data-ttu-id="c4a4c-259">**Unité TTL**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-259">**TTL unit**</span></span>|<span data-ttu-id="c4a4c-260">**Alias**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-260">**Alias**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c4a4c-261">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="c4a4c-261">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="c4a4c-262">CNAME</span><span class="sxs-lookup"><span data-stu-id="c4a4c-262">CNAME</span></span>  <br/> |<span data-ttu-id="c4a4c-263">1</span><span class="sxs-lookup"><span data-stu-id="c4a4c-263">1</span></span>  <br/> |<span data-ttu-id="c4a4c-264">Heures</span><span class="sxs-lookup"><span data-stu-id="c4a4c-264">Hours</span></span>  <br/> |<span data-ttu-id="c4a4c-265">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="c4a4c-265">enterpriseregistration.windows.net</span></span>  <br/> |
|<span data-ttu-id="c4a4c-266">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="c4a4c-266">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="c4a4c-267">CNAME</span><span class="sxs-lookup"><span data-stu-id="c4a4c-267">CNAME</span></span>  <br/> |<span data-ttu-id="c4a4c-268">1</span><span class="sxs-lookup"><span data-stu-id="c4a4c-268">1</span></span>  <br/> |<span data-ttu-id="c4a4c-269">Heures</span><span class="sxs-lookup"><span data-stu-id="c4a4c-269">Hours</span></span>  <br/> |<span data-ttu-id="c4a4c-270">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="c4a4c-270">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
   
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="c4a4c-271">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="c4a4c-271">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="c4a4c-272"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="c4a4c-272"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4a4c-273">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-273">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="c4a4c-274">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-274">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="c4a4c-275">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-275">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="c4a4c-276">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel de manière à n’avoir *qu’un seul* enregistrement SPF incluant les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-276">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
1. <span data-ttu-id="c4a4c-277">To get started, go to your domains page at Azure by using [this link](https://portal.azure.com ).</span><span class="sxs-lookup"><span data-stu-id="c4a4c-277">To get started, go to your domains page at Azure by using [this link](https://portal.azure.com ).</span></span> <span data-ttu-id="c4a4c-278">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-278">You'll be prompted to log in first.</span></span>
    
    ![Azure-BP-Configure-1-1](../../media/ed377cad-0c47-4f9f-b322-c3e06b309b1f.png)
  
2. <span data-ttu-id="c4a4c-280">Dans la page **Tableau de** bord, dans la zone **Toutes** les ressources, sélectionnez le domaine à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-280">On the **Dashboard** page, in the **All resources** area, select the domain that you want to update.</span></span> 
    
    ![Azure-BP-Configure-1-2](../../media/eb4baad2-92d7-49c9-95e5-1dd8510d5ec9.png)
  
3. <span data-ttu-id="c4a4c-282">Dans la **zone de zone DNS,** sélectionnez le jeu d’enregistrement **TXT.**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-282">In the **DNS zone** area, select the **TXT record set**.</span></span>
    
    ![Azure-BP-Configure-4-1](../../media/03095196-5010-4072-8503-79b812084dbf.png)
  
4. <span data-ttu-id="c4a4c-284">Dans la **zone Propriétés du jeu** d’enregistrement, dans les zones du nouveau jeu d’enregistrement, sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-284">In the **Record set properties** area, in the boxes for the new record set, select the values from the following table.</span></span> 
    
    <span data-ttu-id="c4a4c-285">(Choisissez les **valeurs des** unités Type et **TTL** dans les listes de listes.)</span><span class="sxs-lookup"><span data-stu-id="c4a4c-285">(Choose the **Type** and **TTL unit** values from the drop-down lists.)</span></span> 
    
    |<span data-ttu-id="c4a4c-286">**Name**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-286">**Name**</span></span>|<span data-ttu-id="c4a4c-287">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-287">**Type**</span></span>|<span data-ttu-id="c4a4c-288">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-288">**TTL**</span></span>|<span data-ttu-id="c4a4c-289">**Unité TTL**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-289">**TTL unit**</span></span>|<span data-ttu-id="c4a4c-290">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-290">**Value**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="c4a4c-291">TXT</span><span class="sxs-lookup"><span data-stu-id="c4a4c-291">TXT</span></span>  <br/> |<span data-ttu-id="c4a4c-292">1</span><span class="sxs-lookup"><span data-stu-id="c4a4c-292">1</span></span>  <br/> |<span data-ttu-id="c4a4c-293">Heures</span><span class="sxs-lookup"><span data-stu-id="c4a4c-293">Hours</span></span>  <br/> |<span data-ttu-id="c4a4c-294">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="c4a4c-294">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="c4a4c-295">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-295">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           

    ![Azure-BP-Configure-4-2](../../media/78e84c43-e0ce-433f-8e74-9157fb093cca.png)
  
5. <span data-ttu-id="c4a4c-297">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-297">Select **Save**.</span></span>
    
    ![Azure-BP-Configure-4-3](../../media/d7421c7f-ea63-4e11-8595-a482b8c165e0.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="c4a4c-299">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="c4a4c-299">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="c4a4c-300"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="c4a4c-300"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="c4a4c-301">To get started, go to your domains page at Azure by using [this link](https://portal.azure.com ).</span><span class="sxs-lookup"><span data-stu-id="c4a4c-301">To get started, go to your domains page at Azure by using [this link](https://portal.azure.com ).</span></span> <span data-ttu-id="c4a4c-302">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-302">You'll be prompted to log in first.</span></span>
    
    ![Azure-BP-Configure-1-1](../../media/ed377cad-0c47-4f9f-b322-c3e06b309b1f.png)
  
2. <span data-ttu-id="c4a4c-304">Dans la page **Tableau de** bord, dans la zone **Toutes** les ressources, sélectionnez le domaine à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-304">On the **Dashboard** page, in the **All resources** area, select the domain that you want to update.</span></span> 
    
    ![Azure-BP-Configure-1-2](../../media/eb4baad2-92d7-49c9-95e5-1dd8510d5ec9.png)
  
3. <span data-ttu-id="c4a4c-306">Dans la page **Paramètres** de votre domaine, dans la zone **de zone DNS,** **sélectionnez + Jeu d’enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-306">On the **Settings** page for your domain, in the **DNS zone** area, select **+ Record set**.</span></span>
    
    ![Azure-BP-Configure-1-3](../../media/b04db89a-3dbc-4cd2-aaca-af17fda53a60.png)
  
4. <span data-ttu-id="c4a4c-308">Ajoutez le premier des deux enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-308">Add the first of the two SRV records.</span></span>
    
    <span data-ttu-id="c4a4c-309">Dans la **zone Ajouter un jeu d’enregistrement,** dans les zones du nouveau jeu d’enregistrement, sélectionnez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-309">In the **Add record set** area, in the boxes for the new record set, select the values from the first row in the following table.</span></span> 
    
    <span data-ttu-id="c4a4c-310">(Choisissez les **valeurs des** unités Type et **TTL** dans les listes de listes.)</span><span class="sxs-lookup"><span data-stu-id="c4a4c-310">(Choose the **Type** and **TTL unit** values from the drop-down lists.)</span></span> 
    
    |<span data-ttu-id="c4a4c-311">**Name**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-311">**Name**</span></span>|<span data-ttu-id="c4a4c-312">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-312">**Type**</span></span>|<span data-ttu-id="c4a4c-313">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-313">**TTL**</span></span>|<span data-ttu-id="c4a4c-314">**Unité TTL**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-314">**TTL unit**</span></span>|<span data-ttu-id="c4a4c-315">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-315">**Priority**</span></span>|<span data-ttu-id="c4a4c-316">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-316">**Weight**</span></span>|<span data-ttu-id="c4a4c-317">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-317">**Port**</span></span>|<span data-ttu-id="c4a4c-318">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="c4a4c-318">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="c4a4c-319">_sip._tls</span><span class="sxs-lookup"><span data-stu-id="c4a4c-319">_sip._tls</span></span>  <br/> |<span data-ttu-id="c4a4c-320">SRV</span><span class="sxs-lookup"><span data-stu-id="c4a4c-320">SRV</span></span>  <br/> |<span data-ttu-id="c4a4c-321">1</span><span class="sxs-lookup"><span data-stu-id="c4a4c-321">1</span></span>  <br/> |<span data-ttu-id="c4a4c-322">Heures</span><span class="sxs-lookup"><span data-stu-id="c4a4c-322">Hours</span></span>  <br/> |<span data-ttu-id="c4a4c-323">100</span><span class="sxs-lookup"><span data-stu-id="c4a4c-323">100</span></span>  <br/> |<span data-ttu-id="c4a4c-324">1</span><span class="sxs-lookup"><span data-stu-id="c4a4c-324">1</span></span>  <br/> |<span data-ttu-id="c4a4c-325">443</span><span class="sxs-lookup"><span data-stu-id="c4a4c-325">443</span></span>  <br/> |<span data-ttu-id="c4a4c-326">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="c4a4c-326">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="c4a4c-327">_sipfederationtls._tcp</span><span class="sxs-lookup"><span data-stu-id="c4a4c-327">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="c4a4c-328">SRV</span><span class="sxs-lookup"><span data-stu-id="c4a4c-328">SRV</span></span>  <br/> |<span data-ttu-id="c4a4c-329">1</span><span class="sxs-lookup"><span data-stu-id="c4a4c-329">1</span></span>  <br/> |<span data-ttu-id="c4a4c-330">Heures</span><span class="sxs-lookup"><span data-stu-id="c4a4c-330">Hours</span></span>  <br/> |<span data-ttu-id="c4a4c-331">100</span><span class="sxs-lookup"><span data-stu-id="c4a4c-331">100</span></span>  <br/> |<span data-ttu-id="c4a4c-332">1</span><span class="sxs-lookup"><span data-stu-id="c4a4c-332">1</span></span>  <br/> |<span data-ttu-id="c4a4c-333">5061</span><span class="sxs-lookup"><span data-stu-id="c4a4c-333">5061</span></span>  <br/> |<span data-ttu-id="c4a4c-334">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="c4a4c-334">sipfed.online.lync.com</span></span>  <br/> 

    ![Azure-BP-Configure-5-1](../../media/a436e0b4-8bb8-4a66-9c22-4e3b2dcf54ff.png)
  
5. <span data-ttu-id="c4a4c-336">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-336">Select **OK**.</span></span>
    
    ![Azure-BP-Configure-5-2](../../media/a35b6c8a-d001-4b3c-8a67-96b4890e564c.png)
  
6. <span data-ttu-id="c4a4c-338">Ajoutez l’autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-338">Add the other SRV record.</span></span>
    
    <span data-ttu-id="c4a4c-339">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la deuxième ligne du tableau.</span><span class="sxs-lookup"><span data-stu-id="c4a4c-339">In the boxes for the new record, type or copy and paste the values from the second row of the table.</span></span>
    
> [!NOTE]
> <span data-ttu-id="c4a4c-p120">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="c4a4c-p120">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
