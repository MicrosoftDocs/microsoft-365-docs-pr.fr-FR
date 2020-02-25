---
title: Créer des enregistrements DNS pour les zones DNS Azure
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: fbcef2d7-ebaf-40d0-ba1f-cdaeff9f50ef
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur les zones DNS Azure pour Office 365.
ms.openlocfilehash: 3758b525bd98c724165f2671023ba416c338786d
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42239025"
---
# <a name="create-dns-records-for-azure-dns-zones"></a><span data-ttu-id="f0073-103">Créer des enregistrements DNS pour les zones DNS Azure</span><span class="sxs-lookup"><span data-stu-id="f0073-103">Create DNS records for Azure DNS zones</span></span>

 <span data-ttu-id="f0073-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="f0073-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="f0073-105">Si Azure est votre fournisseur d’hébergement DNS, suivez la procédure décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier électronique, Skype entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="f0073-105">If Azure is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="f0073-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="f0073-106">These are the main records to add.</span></span> 
  
- [<span data-ttu-id="f0073-107">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="f0073-107">Change your domain's nameserver (NS) records</span></span>](#change-your-domains-nameserver-ns-records)
    
- [<span data-ttu-id="f0073-108">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="f0073-108">Add a TXT record for verification</span></span>](#add-a-txt-record-for-verification)

- [<span data-ttu-id="f0073-109">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="f0073-109">Add an MX record so email for your domain will come to Office 365</span></span>](#add-an-mx-record-so-email-for-your-domain-will-come-to-office-365)
    
- [<span data-ttu-id="f0073-110">Ajouter les quatre enregistrements CNAMe requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="f0073-110">Add the four CNAME records that are required for Office 365</span></span>](#add-the-four-cname-records-that-are-required-for-office-365)
    
- [<span data-ttu-id="f0073-111">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="f0073-111">Add a TXT record for SPF to help prevent email spam</span></span>](#add-a-txt-record-for-spf-to-help-prevent-email-spam)
    
- [<span data-ttu-id="f0073-112">Ajouter les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="f0073-112">Add the two SRV records that are required for Office 365</span></span>](#add-the-two-srv-records-that-are-required-for-office-365)
    
<span data-ttu-id="f0073-113">Une fois ces enregistrements ajoutés sur Azure, votre domaine est configuré pour utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="f0073-113">After you add these records at Azure, your domain will be set up to work with Office 365 services.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f0073-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f0073-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="f0073-117">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="f0073-117">Change your domain's nameserver (NS) records</span></span>
<span data-ttu-id="f0073-118"><a name="BKMK_NS"> </a></span><span class="sxs-lookup"><span data-stu-id="f0073-118"><a name="BKMK_NS"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="f0073-119">Vous devez effectuer cette procédure au niveau du bureau d'enregistrement de domaines auprès duquel vous avez acheté et inscrit votre domaine.</span><span class="sxs-lookup"><span data-stu-id="f0073-119">You must perform this procedure at the domain registrar where you purchased and registered your domain.</span></span> 
  
<span data-ttu-id="f0073-120">Lorsque vous vous êtes inscrit à Azure, vous avez créé un groupe de ressources au sein d’une zone DNS, puis attribué votre nom de domaine à ce groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="f0073-120">When you signed up for Azure, you created a resource group within a DNS zone, and then assigned your domain name to that resource group.</span></span> <span data-ttu-id="f0073-121">Ce nom de domaine est enregistré auprès d’un bureau d’enregistrement de domaines externes ; Azure ne propose pas de services d’inscription de domaine.</span><span class="sxs-lookup"><span data-stu-id="f0073-121">That domain name is registered to an external domain registrar; Azure does not offer domain registration services.</span></span>
  
<span data-ttu-id="f0073-122">Pour vérifier et créer des enregistrements DNS pour votre domaine dans Office 365, vous devez d’abord modifier les serveurs de noms dans votre bureau d’enregistrement de domaines afin qu’ils utilisent les serveurs de noms Azure attribués à votre groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="f0073-122">To verify and create DNS records for your domain in Office 365, you first need to change the nameservers at your domain registrar so that they use the Azure nameservers assigned to your resource group.</span></span>
  
<span data-ttu-id="f0073-123">Pour modifier vous-même les serveurs de noms de votre domaine sur le site web de votre bureau d'enregistrement de domaines, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="f0073-123">To change your domain's name servers at your domain registrar's website yourself, follow these steps.</span></span>
  
1. <span data-ttu-id="f0073-124">Identifiez la zone sur le site web du bureau d'enregistrement de domaines dans laquelle vous pouvez modifier les serveurs de noms pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="f0073-124">Find the area on the domain registrar's website where you can edit the nameservers for your domain.</span></span>
    
2. <span data-ttu-id="f0073-125">Créez deux enregistrements de serveur de noms à l’aide des valeurs indiquées dans le tableau suivant, ou modifiez les enregistrements de serveur de noms existants afin qu’ils correspondent à ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="f0073-125">Either create two nameserver records by using the values in the following table, or edit the existing nameserver records so that they match these values.</span></span> <span data-ttu-id="f0073-126">Vous trouverez ci-dessous un exemple de serveurs de noms attribués Azure.</span><span class="sxs-lookup"><span data-stu-id="f0073-126">An example of Azure assigned nameservers is shown below.</span></span>
    


<span data-ttu-id="f0073-127">**Premier serveur de noms :** Utilisez la valeur de serveur de noms attribuée par Azure.</span><span class="sxs-lookup"><span data-stu-id="f0073-127">**First nameserver:** Use the name server value assigned by Azure.</span></span>  
<span data-ttu-id="f0073-128">**Deuxième serveur de noms :** Utilisez la valeur de serveur de noms attribuée par Azure.</span><span class="sxs-lookup"><span data-stu-id="f0073-128">**Second nameserver:** Use the name server value assigned by Azure.</span></span>  

![Azure-BP-redelegate-1-1](../media/3e4805ea-608a-4df9-8f68-1fbf70d13d08.png)
  
> [!TIP]
> <span data-ttu-id="f0073-130">You should use at least two name server records.</span><span class="sxs-lookup"><span data-stu-id="f0073-130">You should use at least two name server records.</span></span> <span data-ttu-id="f0073-131">Si d’autres serveurs de noms sont répertoriés sur le site Web de votre bureau d’enregistrement de domaines, vous devez les supprimer.</span><span class="sxs-lookup"><span data-stu-id="f0073-131">If there are any other name servers listed at your domain registrar's website, you should delete them.</span></span> 
  
3. <span data-ttu-id="f0073-132">Enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="f0073-132">Save your changes.</span></span>
    
> [!NOTE]
> <span data-ttu-id="f0073-p105">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures. Vous pourrez ensuite utiliser votre messagerie et les autres services Office 365 avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="f0073-p105">Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain.</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="f0073-135">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="f0073-135">Add a TXT record for verification</span></span>
<span data-ttu-id="f0073-136"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="f0073-136"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="f0073-p106">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="f0073-p106">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f0073-p107">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="f0073-p107">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="f0073-141">Pour commencer, accédez à la page de vos domaines sur Azure à l’aide de [ce lien](https://portal.azure.com ).</span><span class="sxs-lookup"><span data-stu-id="f0073-141">To get started, go to your domains page at Azure by using [this link](https://portal.azure.com ).</span></span> <span data-ttu-id="f0073-142">You'll be prompted to log in first.</span><span class="sxs-lookup"><span data-stu-id="f0073-142">You'll be prompted to log in first.</span></span>
    
    ![Azure-BP-configure-1-1](../media/ed377cad-0c47-4f9f-b322-c3e06b309b1f.png)
  
2. <span data-ttu-id="f0073-144">À l’aide de la **barre de recherche** de la page **tableau de bord** , tapez dans **zones DNS**.</span><span class="sxs-lookup"><span data-stu-id="f0073-144">Using the **search bar** on the **Dashboard** page, type in **DNS zones**.</span></span> <span data-ttu-id="f0073-145">Dans l’affichage des résultats, sélectionnez **zones DNS** sous la partie **services** .</span><span class="sxs-lookup"><span data-stu-id="f0073-145">In the results display, select **DNS zones** under the **Services** portion.</span></span> <span data-ttu-id="f0073-146">Une fois que vous avez été redirigé, sélectionnez le domaine que vous souhaitez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="f0073-146">Once you've been redirected, select the domain that you want to update.</span></span>
    
    ![Azure-BP-configure-1-2](../media/eb4baad2-92d7-49c9-95e5-1dd8510d5ec9.png)
  
3. <span data-ttu-id="f0073-148">Sur la page **paramètres** de votre domaine, dans la zone **zone DNS** , sélectionnez **+ jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="f0073-148">On the **Settings** page for your domain, in the **DNS zone** area, select **+ Record set**.</span></span>
    
    ![Azure-BP-configure-1-3](../media/b04db89a-3dbc-4cd2-aaca-af17fda53a60.png)
  
4. <span data-ttu-id="f0073-150">Dans la zone **Ajouter un jeu d’enregistrements** , dans les zones du nouveau jeu d’enregistrements, sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f0073-150">In the **Add record set** area, in the boxes for the new record set, select the values from the following table.</span></span> 
    
    <span data-ttu-id="f0073-151">(Choisissez les valeurs **type** et **unité de durée de vie** dans les listes déroulantes.)</span><span class="sxs-lookup"><span data-stu-id="f0073-151">(Choose the **Type** and **TTL unit** values from the drop-down lists.)</span></span> 
    
    |<span data-ttu-id="f0073-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="f0073-152">**Name**</span></span>|<span data-ttu-id="f0073-153">**Type**</span><span class="sxs-lookup"><span data-stu-id="f0073-153">**Type**</span></span>|<span data-ttu-id="f0073-154">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="f0073-154">**TTL**</span></span>|<span data-ttu-id="f0073-155">**Unité de durée de vie**</span><span class="sxs-lookup"><span data-stu-id="f0073-155">**TTL unit**</span></span>|<span data-ttu-id="f0073-156">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="f0073-156">**Value**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="f0073-157">TXT</span><span class="sxs-lookup"><span data-stu-id="f0073-157">TXT</span></span>  <br/> |<span data-ttu-id="f0073-158">0,1</span><span class="sxs-lookup"><span data-stu-id="f0073-158">1</span></span>  <br/> |<span data-ttu-id="f0073-159">Heures</span><span class="sxs-lookup"><span data-stu-id="f0073-159">Hours</span></span>  <br/> |<span data-ttu-id="f0073-160">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="f0073-160">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="f0073-161">**Remarque :** Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="f0073-161">**Note:** This is an example.</span></span> <span data-ttu-id="f0073-162">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="f0073-162">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span>           [<span data-ttu-id="f0073-163">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="f0073-163">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Azure-BP-Verify-1-1](../media/7d5a253c-e88f-4565-a00a-79bba52f9970.png)
  
5. <span data-ttu-id="f0073-165">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0073-165">Select **OK**.</span></span>
  
6. <span data-ttu-id="f0073-166">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="f0073-166">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="f0073-167">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span><span class="sxs-lookup"><span data-stu-id="f0073-167">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="f0073-168">When Office 365 finds the correct TXT record, your domain is verified.</span><span class="sxs-lookup"><span data-stu-id="f0073-168">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="f0073-169">Dans le centre d’administration, accédez à la page **paramètres** \> des <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="f0073-169">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="f0073-170">Dans la page **domaines** , sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="f0073-170">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="f0073-171">Sur la page **installation** , sélectionnez **Démarrer l’installation**.</span><span class="sxs-lookup"><span data-stu-id="f0073-171">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="f0073-172">Sur la page **vérifier le domaine** , sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="f0073-172">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="f0073-p111">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f0073-p111">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="f0073-176">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="f0073-176">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="f0073-177"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="f0073-177"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="f0073-178">Pour commencer, accédez à la page de vos domaines sur Azure à l’aide de [ce lien](https://portal.azure.com ).</span><span class="sxs-lookup"><span data-stu-id="f0073-178">To get started, go to your domains page at Azure by using [this link](https://portal.azure.com ).</span></span> <span data-ttu-id="f0073-179">You'll be prompted to log in first.</span><span class="sxs-lookup"><span data-stu-id="f0073-179">You'll be prompted to log in first.</span></span>
    
    ![Azure-BP-configure-1-1](../media/ed377cad-0c47-4f9f-b322-c3e06b309b1f.png)
  
2. <span data-ttu-id="f0073-181">Sur la page **tableau de bord** , dans la zone **toutes les ressources** , sélectionnez le domaine que vous souhaitez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="f0073-181">On the **Dashboard** page, in the **All resources** area, select the domain that you want to update.</span></span> 
    
    ![Azure-BP-configure-1-2](../media/eb4baad2-92d7-49c9-95e5-1dd8510d5ec9.png)
  
3. <span data-ttu-id="f0073-183">Sur la page **paramètres** de votre domaine, dans la zone **zone DNS** , sélectionnez **+ jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="f0073-183">On the **Settings** page for your domain, in the **DNS zone** area, select **+ Record set**.</span></span>
    
    ![Azure-BP-configure-1-3](../media/b04db89a-3dbc-4cd2-aaca-af17fda53a60.png)
  
4. <span data-ttu-id="f0073-185">Dans la zone **Ajouter un jeu d’enregistrements** , dans les zones du nouveau jeu d’enregistrements, sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f0073-185">In the **Add record set** area, in the boxes for the new record set, select the values from the following table.</span></span> 
    
    <span data-ttu-id="f0073-186">(Choisissez les valeurs **type** et **unité de durée de vie** dans les listes déroulantes.)</span><span class="sxs-lookup"><span data-stu-id="f0073-186">(Choose the **Type** and **TTL unit** values from the drop-down lists.)</span></span> 
    
    |<span data-ttu-id="f0073-187">**Name**</span><span class="sxs-lookup"><span data-stu-id="f0073-187">**Name**</span></span>|<span data-ttu-id="f0073-188">**Type**</span><span class="sxs-lookup"><span data-stu-id="f0073-188">**Type**</span></span>|<span data-ttu-id="f0073-189">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="f0073-189">**TTL**</span></span>|<span data-ttu-id="f0073-190">**Unité de durée de vie**</span><span class="sxs-lookup"><span data-stu-id="f0073-190">**TTL unit**</span></span>|<span data-ttu-id="f0073-191">**Preference (Préférence)**</span><span class="sxs-lookup"><span data-stu-id="f0073-191">**Preference**</span></span>|<span data-ttu-id="f0073-192">**Exchange mail**</span><span class="sxs-lookup"><span data-stu-id="f0073-192">**Mail Exchange**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="f0073-193">MX</span><span class="sxs-lookup"><span data-stu-id="f0073-193">MX</span></span>  <br/> |<span data-ttu-id="f0073-194">0,1</span><span class="sxs-lookup"><span data-stu-id="f0073-194">1</span></span>  <br/> |<span data-ttu-id="f0073-195">Heures</span><span class="sxs-lookup"><span data-stu-id="f0073-195">Hours</span></span>  <br/> |<span data-ttu-id="f0073-196">10 </span><span class="sxs-lookup"><span data-stu-id="f0073-196">10</span></span>  <br/> <span data-ttu-id="f0073-197">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="f0073-197">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> | <span data-ttu-id="f0073-198">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="f0073-198">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="f0073-199">**Remarque :** Obtenez votre \* \<clé\> de domaine\* à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="f0073-199">**Note:** Get your  *\<domain-key\>*  from your Office 365 account.</span></span>   [<span data-ttu-id="f0073-200">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="f0073-200">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)  
   
    ![Azure-BP-configure-2-1](../media/712c23ae-9d38-4af2-94e0-0704e70744fe.png)
  
5. <span data-ttu-id="f0073-202">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0073-202">Select **OK**.</span></span>
    
    ![Azure-BP-configure-2-2](../media/2f24225f-69ac-41dc-91c5-93d327360f74.png)
  
6. <span data-ttu-id="f0073-204">Si d’autres enregistrements MX sont répertoriés dans la section **MX Records (enregistrements MX** ), vous devez les supprimer.</span><span class="sxs-lookup"><span data-stu-id="f0073-204">If there are any other MX records listed in the **MX Records** section, you must delete them.</span></span> 
    
    <span data-ttu-id="f0073-205">Tout d’abord, dans la zone **zone DNS** , sélectionnez le **jeu d’enregistrements MX**.</span><span class="sxs-lookup"><span data-stu-id="f0073-205">First, in the **DNS zone** area, select the **MX Record set**.</span></span>
    
    ![Azure-BP-configure-2-3](../media/9890da61-6fcd-4c61-888e-ccbb84f80cd0.png)
  
    <span data-ttu-id="f0073-207">Ensuite, sélectionnez l’enregistrement MX que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="f0073-207">Next, select the MX record you want to delete.</span></span>
    
    ![Azure-BP-configure-2-4](../media/afe54f12-66d2-4ff3-80e9-427448e4c32c.png)
  
7. <span data-ttu-id="f0073-209">Sélectionnez le **menu contextuel (...)**, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="f0073-209">Select the **Context menu (…)**, and then choose **Remove**.</span></span>
    
    ![Azure-BP-configure-2-5](../media/25219e25-bc14-4bc7-84ed-ee65eb28a8ed.png)
  
8. <span data-ttu-id="f0073-211">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f0073-211">Select **Save**.</span></span>
    
    ![Azure-BP-configure-2-6](../media/c6133096-5e43-4637-9c01-b63ee4b03517.png)
  
## <a name="add-the-four-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="f0073-213">Ajouter les quatre enregistrements CNAMe requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="f0073-213">Add the four CNAME records that are required for Office 365</span></span>
<span data-ttu-id="f0073-214"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="f0073-214"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="f0073-215">Pour commencer, accédez à la page de vos domaines sur Azure à l’aide de [ce lien](https://portal.azure.com ).</span><span class="sxs-lookup"><span data-stu-id="f0073-215">To get started, go to your domains page at Azure by using [this link](https://portal.azure.com ).</span></span> <span data-ttu-id="f0073-216">You'll be prompted to log in first.</span><span class="sxs-lookup"><span data-stu-id="f0073-216">You'll be prompted to log in first.</span></span>
    
    ![Azure-BP-configure-1-1](../media/ed377cad-0c47-4f9f-b322-c3e06b309b1f.png)
  
2. <span data-ttu-id="f0073-218">Sur la page **tableau de bord** , dans la zone **toutes les ressources** , sélectionnez le domaine que vous souhaitez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="f0073-218">On the **Dashboard** page, in the **All resources** area, select the domain that you want to update.</span></span> 
    
    ![Azure-BP-configure-1-2](../media/eb4baad2-92d7-49c9-95e5-1dd8510d5ec9.png)
  
3. <span data-ttu-id="f0073-220">Sur la page **paramètres** de votre domaine, dans la zone **zone DNS** , sélectionnez **+ jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="f0073-220">On the **Settings** page for your domain, in the **DNS zone** area, select **+ Record set**.</span></span>
    
    ![Azure-BP-configure-1-3](../media/b04db89a-3dbc-4cd2-aaca-af17fda53a60.png)
  
4. <span data-ttu-id="f0073-222">Ajoutez le premier des quatre enregistrements CNAMe.</span><span class="sxs-lookup"><span data-stu-id="f0073-222">Add the first of the four CNAME records.</span></span>
    
    <span data-ttu-id="f0073-223">Dans la zone **Ajouter un jeu d’enregistrements** , dans les zones du nouveau jeu d’enregistrements, tapez ou copiez-collez les valeurs de la première ligne dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f0073-223">In the **Add record set** area, in the boxes for the new record set, type or copy and paste the values from the first row in the following table.</span></span> 
    
    <span data-ttu-id="f0073-224">(Choisissez les valeurs **type** et **unité de durée de vie** dans les listes déroulantes.)</span><span class="sxs-lookup"><span data-stu-id="f0073-224">(Choose the **Type** and **TTL unit** values from the drop-down lists.)</span></span> 
    
    |<span data-ttu-id="f0073-225">**Name**</span><span class="sxs-lookup"><span data-stu-id="f0073-225">**Name**</span></span>|<span data-ttu-id="f0073-226">**Type**</span><span class="sxs-lookup"><span data-stu-id="f0073-226">**Type**</span></span>|<span data-ttu-id="f0073-227">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="f0073-227">**TTL**</span></span>|<span data-ttu-id="f0073-228">**Unité de durée de vie**</span><span class="sxs-lookup"><span data-stu-id="f0073-228">**TTL unit**</span></span>|<span data-ttu-id="f0073-229">**Alias**</span><span class="sxs-lookup"><span data-stu-id="f0073-229">**Alias**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f0073-230">autodiscover</span><span class="sxs-lookup"><span data-stu-id="f0073-230">autodiscover</span></span>  <br/> |<span data-ttu-id="f0073-231">CNAME</span><span class="sxs-lookup"><span data-stu-id="f0073-231">CNAME</span></span>  <br/> |<span data-ttu-id="f0073-232">0,1</span><span class="sxs-lookup"><span data-stu-id="f0073-232">1</span></span>  <br/> |<span data-ttu-id="f0073-233">Heures</span><span class="sxs-lookup"><span data-stu-id="f0073-233">Hours</span></span>  <br/> |<span data-ttu-id="f0073-234">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="f0073-234">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="f0073-235">sip</span><span class="sxs-lookup"><span data-stu-id="f0073-235">sip</span></span>  <br/> |<span data-ttu-id="f0073-236">CNAME</span><span class="sxs-lookup"><span data-stu-id="f0073-236">CNAME</span></span>  <br/> |<span data-ttu-id="f0073-237">0,1</span><span class="sxs-lookup"><span data-stu-id="f0073-237">1</span></span>  <br/> |<span data-ttu-id="f0073-238">Heures</span><span class="sxs-lookup"><span data-stu-id="f0073-238">Hours</span></span>  <br/> |<span data-ttu-id="f0073-239">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="f0073-239">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="f0073-240">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="f0073-240">lyncdiscover</span></span>  <br/> |<span data-ttu-id="f0073-241">CNAME</span><span class="sxs-lookup"><span data-stu-id="f0073-241">CNAME</span></span>  <br/> |<span data-ttu-id="f0073-242">0,1</span><span class="sxs-lookup"><span data-stu-id="f0073-242">1</span></span>  <br/> |<span data-ttu-id="f0073-243">Heures</span><span class="sxs-lookup"><span data-stu-id="f0073-243">Hours</span></span>  <br/> |<span data-ttu-id="f0073-244">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="f0073-244">webdir.online.lync.com</span></span>  <br/> |
    
   
    ![Azure-BP-configure-3-1](../media/a1c4d869-da97-43b3-952c-d513a20231dc.png)
  
5. <span data-ttu-id="f0073-246">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0073-246">Select **OK**.</span></span>
    
    ![Azure-BP-configure-3-2](../media/b89b51da-1c07-43cf-9fab-75d2e5eb3544.png)
  
6. <span data-ttu-id="f0073-248">Ajoutez chacun des trois autres enregistrements CNAMe.</span><span class="sxs-lookup"><span data-stu-id="f0073-248">Add each of the other three CNAME records.</span></span>
    
    <span data-ttu-id="f0073-249">Dans la zone **zone DNS** , sélectionnez **+ jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="f0073-249">In the **DNS zone** area, select **+ Record set**.</span></span> <span data-ttu-id="f0073-250">Ensuite, dans le jeu d’enregistrements vide, créez un enregistrement en utilisant les valeurs de la ligne suivante du tableau, puis sélectionnez de nouveau **OK** pour valider cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f0073-250">Then, in the empty record set, create a record by using the values from the next row in the table, and again select **OK** to complete that record.</span></span> 
    
    <span data-ttu-id="f0073-251">Répétez cette procédure jusqu’à ce que vous ayez créé les quatre enregistrements CNAMe.</span><span class="sxs-lookup"><span data-stu-id="f0073-251">Repeat this process until you have created all four CNAME records.</span></span>
    
7.  <span data-ttu-id="f0073-252">Module Ajoutez 2 enregistrements CNAMe pour MDM.</span><span class="sxs-lookup"><span data-stu-id="f0073-252">(Optional) Add 2 CNAME records for MDM.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f0073-253">Si vous disposez de la gestion des appareils mobiles pour Office 365, vous devez créer deux enregistrements CNAMe supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f0073-253">If you have Mobile Device Management (MDM) for Office 365, then you must create two additional CNAME records.</span></span> <span data-ttu-id="f0073-254">Follow the procedure that you used for the other four CNAME records, but supply the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="f0073-254">Follow the procedure that you used for the other four CNAME records, but supply the values from the following table.</span></span> <span data-ttu-id="f0073-255">(Si vous ne disposez pas de MDM, vous pouvez ignorer cette étape.)</span><span class="sxs-lookup"><span data-stu-id="f0073-255">(If you do not have MDM, you can skip this step.)</span></span> 
  
|<span data-ttu-id="f0073-256">**Name**</span><span class="sxs-lookup"><span data-stu-id="f0073-256">**Name**</span></span>|<span data-ttu-id="f0073-257">**Type**</span><span class="sxs-lookup"><span data-stu-id="f0073-257">**Type**</span></span>|<span data-ttu-id="f0073-258">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="f0073-258">**TTL**</span></span>|<span data-ttu-id="f0073-259">**Unité de durée de vie**</span><span class="sxs-lookup"><span data-stu-id="f0073-259">**TTL unit**</span></span>|<span data-ttu-id="f0073-260">**Alias**</span><span class="sxs-lookup"><span data-stu-id="f0073-260">**Alias**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f0073-261">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="f0073-261">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="f0073-262">CNAME</span><span class="sxs-lookup"><span data-stu-id="f0073-262">CNAME</span></span>  <br/> |<span data-ttu-id="f0073-263">0,1</span><span class="sxs-lookup"><span data-stu-id="f0073-263">1</span></span>  <br/> |<span data-ttu-id="f0073-264">Heures</span><span class="sxs-lookup"><span data-stu-id="f0073-264">Hours</span></span>  <br/> |<span data-ttu-id="f0073-265">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="f0073-265">enterpriseregistration.windows.net</span></span>  <br/> |
|<span data-ttu-id="f0073-266">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="f0073-266">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="f0073-267">CNAME</span><span class="sxs-lookup"><span data-stu-id="f0073-267">CNAME</span></span>  <br/> |<span data-ttu-id="f0073-268">0,1</span><span class="sxs-lookup"><span data-stu-id="f0073-268">1</span></span>  <br/> |<span data-ttu-id="f0073-269">Heures</span><span class="sxs-lookup"><span data-stu-id="f0073-269">Hours</span></span>  <br/> |<span data-ttu-id="f0073-270">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="f0073-270">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
   
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="f0073-271">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="f0073-271">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="f0073-272"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="f0073-272"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="f0073-273">You cannot have more than one TXT record for SPF for a domain.</span><span class="sxs-lookup"><span data-stu-id="f0073-273">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="f0073-274">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span><span class="sxs-lookup"><span data-stu-id="f0073-274">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="f0073-275">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="f0073-275">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="f0073-276">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="f0073-276">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
1. <span data-ttu-id="f0073-277">Pour commencer, accédez à la page de vos domaines sur Azure à l’aide de [ce lien](https://portal.azure.com ).</span><span class="sxs-lookup"><span data-stu-id="f0073-277">To get started, go to your domains page at Azure by using [this link](https://portal.azure.com ).</span></span> <span data-ttu-id="f0073-278">You'll be prompted to log in first.</span><span class="sxs-lookup"><span data-stu-id="f0073-278">You'll be prompted to log in first.</span></span>
    
    ![Azure-BP-configure-1-1](../media/ed377cad-0c47-4f9f-b322-c3e06b309b1f.png)
  
2. <span data-ttu-id="f0073-280">Sur la page **tableau de bord** , dans la zone **toutes les ressources** , sélectionnez le domaine que vous souhaitez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="f0073-280">On the **Dashboard** page, in the **All resources** area, select the domain that you want to update.</span></span> 
    
    ![Azure-BP-configure-1-2](../media/eb4baad2-92d7-49c9-95e5-1dd8510d5ec9.png)
  
3. <span data-ttu-id="f0073-282">Dans la zone **zone DNS** , sélectionnez le **jeu d’enregistrements TXT**.</span><span class="sxs-lookup"><span data-stu-id="f0073-282">In the **DNS zone** area, select the **TXT record set**.</span></span>
    
    ![Azure-BP-configure-4-1](../media/03095196-5010-4072-8503-79b812084dbf.png)
  
4. <span data-ttu-id="f0073-284">Dans la zone Propriétés de l' **ensemble d’enregistrements** , dans les zones du nouveau jeu d’enregistrements, sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f0073-284">In the **Record set properties** area, in the boxes for the new record set, select the values from the following table.</span></span> 
    
    <span data-ttu-id="f0073-285">(Choisissez les valeurs **type** et **unité de durée de vie** dans les listes déroulantes.)</span><span class="sxs-lookup"><span data-stu-id="f0073-285">(Choose the **Type** and **TTL unit** values from the drop-down lists.)</span></span> 
    
    |<span data-ttu-id="f0073-286">**Name**</span><span class="sxs-lookup"><span data-stu-id="f0073-286">**Name**</span></span>|<span data-ttu-id="f0073-287">**Type**</span><span class="sxs-lookup"><span data-stu-id="f0073-287">**Type**</span></span>|<span data-ttu-id="f0073-288">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="f0073-288">**TTL**</span></span>|<span data-ttu-id="f0073-289">**Unité de durée de vie**</span><span class="sxs-lookup"><span data-stu-id="f0073-289">**TTL unit**</span></span>|<span data-ttu-id="f0073-290">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="f0073-290">**Value**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="f0073-291">TXT</span><span class="sxs-lookup"><span data-stu-id="f0073-291">TXT</span></span>  <br/> |<span data-ttu-id="f0073-292">0,1</span><span class="sxs-lookup"><span data-stu-id="f0073-292">1</span></span>  <br/> |<span data-ttu-id="f0073-293">Heures</span><span class="sxs-lookup"><span data-stu-id="f0073-293">Hours</span></span>  <br/> |<span data-ttu-id="f0073-294">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="f0073-294">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="f0073-295">**Remarque :** Nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="f0073-295">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           

    ![Azure-BP-configure-4-2](../media/78e84c43-e0ce-433f-8e74-9157fb093cca.png)
  
5. <span data-ttu-id="f0073-297">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f0073-297">Select **Save**.</span></span>
    
    ![Azure-BP-configure-4-3](../media/d7421c7f-ea63-4e11-8595-a482b8c165e0.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="f0073-299">Ajouter les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="f0073-299">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="f0073-300"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="f0073-300"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="f0073-301">Pour commencer, accédez à la page de vos domaines sur Azure à l’aide de [ce lien](https://portal.azure.com ).</span><span class="sxs-lookup"><span data-stu-id="f0073-301">To get started, go to your domains page at Azure by using [this link](https://portal.azure.com ).</span></span> <span data-ttu-id="f0073-302">You'll be prompted to log in first.</span><span class="sxs-lookup"><span data-stu-id="f0073-302">You'll be prompted to log in first.</span></span>
    
    ![Azure-BP-configure-1-1](../media/ed377cad-0c47-4f9f-b322-c3e06b309b1f.png)
  
2. <span data-ttu-id="f0073-304">Sur la page **tableau de bord** , dans la zone **toutes les ressources** , sélectionnez le domaine que vous souhaitez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="f0073-304">On the **Dashboard** page, in the **All resources** area, select the domain that you want to update.</span></span> 
    
    ![Azure-BP-configure-1-2](../media/eb4baad2-92d7-49c9-95e5-1dd8510d5ec9.png)
  
3. <span data-ttu-id="f0073-306">Sur la page **paramètres** de votre domaine, dans la zone **zone DNS** , sélectionnez **+ jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="f0073-306">On the **Settings** page for your domain, in the **DNS zone** area, select **+ Record set**.</span></span>
    
    ![Azure-BP-configure-1-3](../media/b04db89a-3dbc-4cd2-aaca-af17fda53a60.png)
  
4. <span data-ttu-id="f0073-308">Ajoutez le premier des deux enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="f0073-308">Add the first of the two SRV records.</span></span>
    
    <span data-ttu-id="f0073-309">Dans la zone **Ajouter un jeu d’enregistrements** , dans les zones du nouveau jeu d’enregistrements, sélectionnez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f0073-309">In the **Add record set** area, in the boxes for the new record set, select the values from the first row in the following table.</span></span> 
    
    <span data-ttu-id="f0073-310">(Choisissez les valeurs **type** et **unité de durée de vie** dans les listes déroulantes.)</span><span class="sxs-lookup"><span data-stu-id="f0073-310">(Choose the **Type** and **TTL unit** values from the drop-down lists.)</span></span> 
    
    |<span data-ttu-id="f0073-311">**Name**</span><span class="sxs-lookup"><span data-stu-id="f0073-311">**Name**</span></span>|<span data-ttu-id="f0073-312">**Type**</span><span class="sxs-lookup"><span data-stu-id="f0073-312">**Type**</span></span>|<span data-ttu-id="f0073-313">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="f0073-313">**TTL**</span></span>|<span data-ttu-id="f0073-314">**Unité de durée de vie**</span><span class="sxs-lookup"><span data-stu-id="f0073-314">**TTL unit**</span></span>|<span data-ttu-id="f0073-315">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="f0073-315">**Priority**</span></span>|<span data-ttu-id="f0073-316">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="f0073-316">**Weight**</span></span>|<span data-ttu-id="f0073-317">**Port**</span><span class="sxs-lookup"><span data-stu-id="f0073-317">**Port**</span></span>|<span data-ttu-id="f0073-318">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="f0073-318">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f0073-319">_sip. _tls</span><span class="sxs-lookup"><span data-stu-id="f0073-319">_sip._tls</span></span>  <br/> |<span data-ttu-id="f0073-320">SRV</span><span class="sxs-lookup"><span data-stu-id="f0073-320">SRV</span></span>  <br/> |<span data-ttu-id="f0073-321">0,1</span><span class="sxs-lookup"><span data-stu-id="f0073-321">1</span></span>  <br/> |<span data-ttu-id="f0073-322">Heures</span><span class="sxs-lookup"><span data-stu-id="f0073-322">Hours</span></span>  <br/> |<span data-ttu-id="f0073-323">100</span><span class="sxs-lookup"><span data-stu-id="f0073-323">100</span></span>  <br/> |<span data-ttu-id="f0073-324">0,1</span><span class="sxs-lookup"><span data-stu-id="f0073-324">1</span></span>  <br/> |<span data-ttu-id="f0073-325">443</span><span class="sxs-lookup"><span data-stu-id="f0073-325">443</span></span>  <br/> |<span data-ttu-id="f0073-326">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="f0073-326">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="f0073-327">_sipfederationtls. _tcp</span><span class="sxs-lookup"><span data-stu-id="f0073-327">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="f0073-328">SRV</span><span class="sxs-lookup"><span data-stu-id="f0073-328">SRV</span></span>  <br/> |<span data-ttu-id="f0073-329">0,1</span><span class="sxs-lookup"><span data-stu-id="f0073-329">1</span></span>  <br/> |<span data-ttu-id="f0073-330">Heures</span><span class="sxs-lookup"><span data-stu-id="f0073-330">Hours</span></span>  <br/> |<span data-ttu-id="f0073-331">100</span><span class="sxs-lookup"><span data-stu-id="f0073-331">100</span></span>  <br/> |<span data-ttu-id="f0073-332">0,1</span><span class="sxs-lookup"><span data-stu-id="f0073-332">1</span></span>  <br/> |<span data-ttu-id="f0073-333">5061</span><span class="sxs-lookup"><span data-stu-id="f0073-333">5061</span></span>  <br/> |<span data-ttu-id="f0073-334">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="f0073-334">sipfed.online.lync.com</span></span>  <br/> 

    ![Azure-BP-configure-5-1](../media/a436e0b4-8bb8-4a66-9c22-4e3b2dcf54ff.png)
  
5. <span data-ttu-id="f0073-336">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0073-336">Select **OK**.</span></span>
    
    ![Azure-BP-configure-5-2](../media/a35b6c8a-d001-4b3c-8a67-96b4890e564c.png)
  
6. <span data-ttu-id="f0073-338">Ajoutez l'autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="f0073-338">Add the other SRV record.</span></span>
    
    <span data-ttu-id="f0073-339">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la deuxième ligne du tableau.</span><span class="sxs-lookup"><span data-stu-id="f0073-339">In the boxes for the new record, type or copy and paste the values from the second row of the table.</span></span>
    
> [!NOTE]
> <span data-ttu-id="f0073-p120">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f0073-p120">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
