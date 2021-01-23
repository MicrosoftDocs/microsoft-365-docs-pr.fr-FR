---
title: Créer des enregistrements DNS chez Cloudflare pour Microsoft
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
ms.assetid: 84acd4fc-6eec-4d00-8bed-568f036ae2af
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online et d’autres services dans Cloudflare pour Microsoft.
ms.openlocfilehash: 8d5dd7779f07fd42dd230ee33c40849da3519d26
ms.sourcegitcommit: ba830e85899f247e5a1e117d63e09e4d5b8a8020
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49939271"
---
# <a name="create-dns-records-at-cloudflare-for-microsoft"></a><span data-ttu-id="7692d-103">Créer des enregistrements DNS chez Cloudflare pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="7692d-103">Create DNS records at Cloudflare for Microsoft</span></span>

 <span data-ttu-id="7692d-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="7692d-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="7692d-105">Si Cloudflare est votre fournisseur d’hébergement DNS, suivez les étapes de cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="7692d-105">If Cloudflare is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="7692d-106">Une fois ces enregistrements ajoutés sur Cloudflare, votre domaine est installé pour fonctionner avec les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7692d-106">After you add these records at Cloudflare, your domain will be set up to work with Microsoft 365 services.</span></span>
  
  
> [!NOTE]
>  <span data-ttu-id="7692d-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="7692d-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="7692d-110">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="7692d-110">Change your domain's nameserver (NS) records</span></span>
<span data-ttu-id="7692d-111"><a name="BKMK_Nameservers"> </a></span><span class="sxs-lookup"><span data-stu-id="7692d-111"><a name="BKMK_Nameservers"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="7692d-112">Vous devez effectuer cette procédure au niveau du bureau d'enregistrement de domaines auprès duquel vous avez acheté et inscrit votre domaine.</span><span class="sxs-lookup"><span data-stu-id="7692d-112">You must perform this procedure at the domain registrar where you purchased and registered your domain.</span></span> 
  
<span data-ttu-id="7692d-113">Lorsque vous vous êtes inscrit à Cloudflare, vous avez ajouté un domaine à l’aide du processus **d’installation de** Cloudflare.</span><span class="sxs-lookup"><span data-stu-id="7692d-113">When you signed up for Cloudflare, you added a domain by using the Cloudflare **Setup** process.</span></span> 
  
<span data-ttu-id="7692d-114">Le domaine que vous avez ajouté a été acheté auprès de Cloudflare ou d’un bureau d’enregistrement de domaines distinct.</span><span class="sxs-lookup"><span data-stu-id="7692d-114">The domain that you added was purchased from Cloudflare or a separate domain registrar.</span></span> <span data-ttu-id="7692d-115">Pour vérifier et créer des enregistrements DNS pour votre domaine dans Microsoft 365, vous devez d’abord modifier les serveurs de noms de votre bureau d’enregistrement de domaines afin qu’ils utilisent les serveurs de noms Cloudflare.</span><span class="sxs-lookup"><span data-stu-id="7692d-115">To verify and create DNS records for your domain in Microsoft 365, you first need to change the nameservers at your domain registrar so that they use Cloudflare's nameservers.</span></span>
  
<span data-ttu-id="7692d-116">Pour modifier vous-même les serveurs de noms de votre domaine sur le site web de votre bureau d'enregistrement de domaines, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="7692d-116">To change your domain's name servers at your domain registrar's website yourself, follow these steps.</span></span>
  
1. <span data-ttu-id="7692d-117">Identifiez la zone sur le site web du bureau d'enregistrement de domaines dans laquelle vous pouvez modifier les serveurs de noms pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="7692d-117">Find the area on the domain registrar's website where you can edit the nameservers for your domain.</span></span>
    
2. <span data-ttu-id="7692d-118">Créez deux enregistrements de nameserver à l’aide des valeurs du tableau suivant, ou modifiez les enregistrements de nameserver existants afin qu’ils correspondent à ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="7692d-118">Either create two nameserver records by using the values in the following table, or edit the existing nameserver records so that they match these values.</span></span>
    
    |||
    |:-----|:-----|
    |<span data-ttu-id="7692d-119">Premier serveur de noms</span><span class="sxs-lookup"><span data-stu-id="7692d-119">First nameserver</span></span>  <br/> |<span data-ttu-id="7692d-120">Utilisez la valeur de nameserver fournie par Cloudflare.</span><span class="sxs-lookup"><span data-stu-id="7692d-120">Use the nameserver value provided by Cloudflare.</span></span>  <br/> |
    |<span data-ttu-id="7692d-121">Deuxième serveur de noms</span><span class="sxs-lookup"><span data-stu-id="7692d-121">Second nameserver</span></span>  <br/> |<span data-ttu-id="7692d-122">Utilisez la valeur de nameserver fournie par Cloudflare.</span><span class="sxs-lookup"><span data-stu-id="7692d-122">Use the nameserver value provided by Cloudflare.</span></span>  <br/> |
   
    > [!TIP]
    > <span data-ttu-id="7692d-123">You should use at least two name server records.</span><span class="sxs-lookup"><span data-stu-id="7692d-123">You should use at least two name server records.</span></span> <span data-ttu-id="7692d-124">Si d’autres serveurs de noms sont répertoriés, vous devez les supprimer.</span><span class="sxs-lookup"><span data-stu-id="7692d-124">If there are any other name servers listed, you should delete them.</span></span> 
  
3. <span data-ttu-id="7692d-125">Enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="7692d-125">Save your changes.</span></span>
    
> [!NOTE]
> <span data-ttu-id="7692d-126">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="7692d-126">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span></span> <span data-ttu-id="7692d-127">Ensuite, votre messagerie Microsoft et d’autres services seront tous définies pour fonctionner avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="7692d-127">Then your Microsoft email and other services will be all set to work with your domain.</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="7692d-128">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="7692d-128">Add a TXT record for verification</span></span>
<span data-ttu-id="7692d-129"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="7692d-129"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="7692d-p105">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="7692d-p105">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7692d-p106">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="7692d-p106">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="7692d-134">To get started, go to your domains page at Cloudflare by using [this link](https://www.cloudflare.com/a/login).</span><span class="sxs-lookup"><span data-stu-id="7692d-134">To get started, go to your domains page at Cloudflare by using [this link](https://www.cloudflare.com/a/login).</span></span> <span data-ttu-id="7692d-135">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="7692d-135">You'll be prompted to log in first.</span></span>
  
2. <span data-ttu-id="7692d-136">Dans  la page d’accueil, sélectionnez le domaine à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="7692d-136">On the **Home** page, select the domain that you want to update.</span></span> 
  
3. <span data-ttu-id="7692d-137">Dans la page **Vue d’ensemble** de votre domaine, sélectionnez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="7692d-137">On the **Overview** page for your domain, select **DNS**.</span></span>

  
4. <span data-ttu-id="7692d-138">Dans la page de **gestion DNS,** cliquez sur Ajouter un **enregistrement,** puis sélectionnez les valeurs dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7692d-138">On the **DNS management** page, click **Add record**, and then select the values from the following table.</span></span> 
    
    | <span data-ttu-id="7692d-139">Type</span><span class="sxs-lookup"><span data-stu-id="7692d-139">Type</span></span> | <span data-ttu-id="7692d-140">Nom</span><span class="sxs-lookup"><span data-stu-id="7692d-140">Name</span></span> | <span data-ttu-id="7692d-141">TTL automatique</span><span class="sxs-lookup"><span data-stu-id="7692d-141">Automatic TTL</span></span> | <span data-ttu-id="7692d-142">Contenu</span><span class="sxs-lookup"><span data-stu-id="7692d-142">Content</span></span> |
    |:-----|:-----|:-----|:----|
    |<span data-ttu-id="7692d-143">TXT</span><span class="sxs-lookup"><span data-stu-id="7692d-143">TXT</span></span>  <br/> |@  <br/> |<span data-ttu-id="7692d-144">30 minutes</span><span class="sxs-lookup"><span data-stu-id="7692d-144">30 minutes</span></span>  <br/> |<span data-ttu-id="7692d-145">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="7692d-145">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="7692d-146">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="7692d-146">**Note:** This is an example.</span></span> <span data-ttu-id="7692d-147">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="7692d-147">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="7692d-148">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="7692d-148">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)    |
  
    
5. <span data-ttu-id="7692d-149">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7692d-149">Select **Save**.</span></span>
  
  
9. <span data-ttu-id="7692d-150">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="7692d-150">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="7692d-151">Maintenant que vous avez ajouté l’enregistrement sur le site de votre bureau d’enregistrement de domaines, vous revenirz à Microsoft et recherchez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="7692d-151">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and search for the record.</span></span>
  
<span data-ttu-id="7692d-152">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="7692d-152">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="7692d-153">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="7692d-153">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="7692d-154">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="7692d-154">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="7692d-155">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="7692d-155">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="7692d-156">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="7692d-156">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="7692d-p109">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="7692d-p109">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="7692d-160">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="7692d-160">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="7692d-161"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="7692d-161"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="7692d-162">To get started, go to your domains page at Cloudflare by using [this link](https://www.cloudflare.com/a/login).</span><span class="sxs-lookup"><span data-stu-id="7692d-162">To get started, go to your domains page at Cloudflare by using [this link](https://www.cloudflare.com/a/login).</span></span> <span data-ttu-id="7692d-163">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="7692d-163">You'll be prompted to log in first.</span></span>
  
2. <span data-ttu-id="7692d-164">Dans  la page d’accueil, sélectionnez le domaine à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="7692d-164">On the **Home** page, select the domain that you want to update.</span></span> 
  
3. <span data-ttu-id="7692d-165">Dans la page **Vue d’ensemble** de votre domaine, sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="7692d-165">On the **Overview** page for your domain, select **DNS**.</span></span>

  
4. <span data-ttu-id="7692d-166">Dans la page de **gestion DNS,** cliquez sur Ajouter un **enregistrement,** puis sélectionnez les valeurs dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7692d-166">On the **DNS management** page, click **Add record**, and then select the values from the following table.</span></span> 
    
    | <span data-ttu-id="7692d-167">Type</span><span class="sxs-lookup"><span data-stu-id="7692d-167">Type</span></span> | <span data-ttu-id="7692d-168">Nom</span><span class="sxs-lookup"><span data-stu-id="7692d-168">Name</span></span> | <span data-ttu-id="7692d-169">Serveur de messagerie</span><span class="sxs-lookup"><span data-stu-id="7692d-169">Mail server</span></span> | <span data-ttu-id="7692d-170">Priority (Priorité)</span><span class="sxs-lookup"><span data-stu-id="7692d-170">Priority</span></span> | <span data-ttu-id="7692d-171">TTL (Durée de vie)</span><span class="sxs-lookup"><span data-stu-id="7692d-171">TTL</span></span> |
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="7692d-172">MX</span><span class="sxs-lookup"><span data-stu-id="7692d-172">MX</span></span>  <br/> |@  <br/> |<span data-ttu-id="7692d-173">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="7692d-173">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="7692d-174">**Remarque :** Obtenez votre  *\<domain-key\>*  compte Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7692d-174">**Note:** Get your  *\<domain-key\>*  from your Microsoft 365 account.</span></span>   [<span data-ttu-id="7692d-175">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="7692d-175">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md) |<span data-ttu-id="7692d-176">1 </span><span class="sxs-lookup"><span data-stu-id="7692d-176">1</span></span>  <br/> <span data-ttu-id="7692d-177">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span><span class="sxs-lookup"><span data-stu-id="7692d-177">For more information about priority, see [What is MX priority?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span></span> <br/>|<span data-ttu-id="7692d-178">30 minutes</span><span class="sxs-lookup"><span data-stu-id="7692d-178">30 minutes</span></span>  <br/> |
   

  
5. <span data-ttu-id="7692d-179">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7692d-179">Select **Save**.</span></span>
  
9. <span data-ttu-id="7692d-180">Si d’autres enregistrements MX sont répertoriés dans la section **Enregistrements MX,** supprimez-les en sélectionnant l’icône **Supprimer (X).**</span><span class="sxs-lookup"><span data-stu-id="7692d-180">If there are any other MX records listed in the **MX Records** section, delete them by selecting the **Delete (X)** icon.</span></span> 
  
10. <span data-ttu-id="7692d-181">Dans la boîte de dialogue de confirmation, **sélectionnez Supprimer** pour confirmer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="7692d-181">In the confirmation dialog box, select **Delete** to confirm your changes.</span></span> 

  
## <a name="add-the-six-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="7692d-182">Ajouter les six enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="7692d-182">Add the Six CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="7692d-183"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="7692d-183"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="7692d-184">To get started, go to your domains page at Cloudflare by using [this link](https://www.cloudflare.com/a/login).</span><span class="sxs-lookup"><span data-stu-id="7692d-184">To get started, go to your domains page at Cloudflare by using [this link](https://www.cloudflare.com/a/login).</span></span> <span data-ttu-id="7692d-185">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="7692d-185">You'll be prompted to log in first.</span></span>
    
  
2. <span data-ttu-id="7692d-186">Dans  la page d’accueil, sélectionnez le domaine à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="7692d-186">On the **Home** page, select the domain that you want to update.</span></span> 
  
3. <span data-ttu-id="7692d-187">Dans la page **Vue d’ensemble** de votre domaine, sélectionnez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="7692d-187">On the **Overview** page for your domain, select **DNS**.</span></span>

  
4. <span data-ttu-id="7692d-188">Ajoutez le premier des cinq enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="7692d-188">Add the first of the five CNAME records.</span></span>
    
    <span data-ttu-id="7692d-189">Dans la page de **gestion DNS,** cliquez sur Ajouter un **enregistrement,** puis sélectionnez les valeurs dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7692d-189">On the **DNS management** page, click **Add record**, and then select the values from the following table.</span></span>
    
    
    | <span data-ttu-id="7692d-190">Type</span><span class="sxs-lookup"><span data-stu-id="7692d-190">Type</span></span> | <span data-ttu-id="7692d-191">Nom</span><span class="sxs-lookup"><span data-stu-id="7692d-191">Name</span></span> | <span data-ttu-id="7692d-192">Target</span><span class="sxs-lookup"><span data-stu-id="7692d-192">Target</span></span> | <span data-ttu-id="7692d-193">Durée de vie</span><span class="sxs-lookup"><span data-stu-id="7692d-193">TTL</span></span> |
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="7692d-194">CNAME</span><span class="sxs-lookup"><span data-stu-id="7692d-194">CNAME</span></span>  <br/> |<span data-ttu-id="7692d-195">autodiscover</span><span class="sxs-lookup"><span data-stu-id="7692d-195">autodiscover</span></span>  <br/> |<span data-ttu-id="7692d-196">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="7692d-196">autodiscover.outlook.com</span></span>  <br/> |<span data-ttu-id="7692d-197">30 minutes</span><span class="sxs-lookup"><span data-stu-id="7692d-197">30 minutes</span></span>  <br/> |
    |<span data-ttu-id="7692d-198">CNAME</span><span class="sxs-lookup"><span data-stu-id="7692d-198">CNAME</span></span>  <br/> |<span data-ttu-id="7692d-199">sip</span><span class="sxs-lookup"><span data-stu-id="7692d-199">sip</span></span>  <br/> |<span data-ttu-id="7692d-200">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="7692d-200">sipdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="7692d-201">30 minutes</span><span class="sxs-lookup"><span data-stu-id="7692d-201">30 minutes</span></span>  <br/> |
    |<span data-ttu-id="7692d-202">CNAME</span><span class="sxs-lookup"><span data-stu-id="7692d-202">CNAME</span></span>  <br/> |<span data-ttu-id="7692d-203">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="7692d-203">lyncdiscover</span></span>  <br/> |<span data-ttu-id="7692d-204">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="7692d-204">webdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="7692d-205">30 minutes</span><span class="sxs-lookup"><span data-stu-id="7692d-205">30 minutes</span></span>  <br/> |
    |<span data-ttu-id="7692d-206">CNAME</span><span class="sxs-lookup"><span data-stu-id="7692d-206">CNAME</span></span>  <br/> |<span data-ttu-id="7692d-207">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="7692d-207">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="7692d-208">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="7692d-208">enterpriseregistration.windows.net</span></span>  <br/> |<span data-ttu-id="7692d-209">30 minutes</span><span class="sxs-lookup"><span data-stu-id="7692d-209">30 minutes</span></span>  <br/> |
    |<span data-ttu-id="7692d-210">CNAME</span><span class="sxs-lookup"><span data-stu-id="7692d-210">CNAME</span></span>  <br/> |<span data-ttu-id="7692d-211">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="7692d-211">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="7692d-212">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="7692d-212">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |<span data-ttu-id="7692d-213">30 minutes</span><span class="sxs-lookup"><span data-stu-id="7692d-213">30 minutes</span></span>  <br/> |
    |<span data-ttu-id="7692d-214">CNAME</span><span class="sxs-lookup"><span data-stu-id="7692d-214">CNAME</span></span>  <br/> |<span data-ttu-id="7692d-215">msoid</span><span class="sxs-lookup"><span data-stu-id="7692d-215">msoid</span></span>  <br/> |<span data-ttu-id="7692d-216">clientconfig.microsoftonline-p.net</span><span class="sxs-lookup"><span data-stu-id="7692d-216">clientconfig.microsoftonline-p.net</span></span>  <br/> |<span data-ttu-id="7692d-217">30 minutes</span><span class="sxs-lookup"><span data-stu-id="7692d-217">30 minutes</span></span>  <br/> |
    
  
5. <span data-ttu-id="7692d-218">Sélectionnez **l’icône Trafic DNS** (changer le cloud orange en gris) pour contourner les serveurs Cloudflare.</span><span class="sxs-lookup"><span data-stu-id="7692d-218">Select the **DNS Traffic** icon (change orange cloud to grey) to bypass the Cloudflare servers.</span></span>
  
6. <span data-ttu-id="7692d-219">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7692d-219">Select **Save**.</span></span>
  
7. <span data-ttu-id="7692d-220">Ajoutez successivement les 5 autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="7692d-220">Add each of the other five CNAME records.</span></span>

    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="7692d-221">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="7692d-221">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="7692d-222"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="7692d-222"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="7692d-223">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="7692d-223">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="7692d-224">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="7692d-224">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="7692d-225">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7692d-225">If you already have an SPF record for your domain, don't create a new one for Microsoft 365.</span></span> <span data-ttu-id="7692d-226">Ajoutez plutôt les valeurs Microsoft 365 requises à l’enregistrement actuel de manière à n’avoir qu’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="7692d-226">Instead, add the required Microsoft 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
1. <span data-ttu-id="7692d-227">To get started, go to your domains page at Cloudflare by using [this link](https://www.cloudflare.com/a/login).</span><span class="sxs-lookup"><span data-stu-id="7692d-227">To get started, go to your domains page at Cloudflare by using [this link](https://www.cloudflare.com/a/login).</span></span> <span data-ttu-id="7692d-228">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="7692d-228">You'll be prompted to log in first.</span></span>
    
  
2. <span data-ttu-id="7692d-229">Dans  la page d’accueil, sélectionnez le domaine à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="7692d-229">On the **Home** page, select the domain that you want to update.</span></span> 
  
3. <span data-ttu-id="7692d-230">Dans la page **Vue d’ensemble** de votre domaine, sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="7692d-230">On the **Overview** page for your domain, select **DNS**.</span></span>

  
4. <span data-ttu-id="7692d-231">Dans la page de **gestion DNS,** cliquez sur Ajouter un **enregistrement,** puis sélectionnez les valeurs dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7692d-231">On the **DNS management** page, click **Add record**, and then select the values from the following table.</span></span>  
    
    | <span data-ttu-id="7692d-232">Type</span><span class="sxs-lookup"><span data-stu-id="7692d-232">Type</span></span> | <span data-ttu-id="7692d-233">Nom</span><span class="sxs-lookup"><span data-stu-id="7692d-233">Name</span></span> | <span data-ttu-id="7692d-234">Durée de vie</span><span class="sxs-lookup"><span data-stu-id="7692d-234">TTL</span></span> | <span data-ttu-id="7692d-235">Contenu</span><span class="sxs-lookup"><span data-stu-id="7692d-235">Content</span></span> |
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="7692d-236">TXT</span><span class="sxs-lookup"><span data-stu-id="7692d-236">TXT</span></span>  <br/> |@  <br/> |<span data-ttu-id="7692d-237">30 minutes</span><span class="sxs-lookup"><span data-stu-id="7692d-237">30 minutes</span></span>  <br/> |<span data-ttu-id="7692d-238">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="7692d-238">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="7692d-239">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="7692d-239">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>   |

 
5. <span data-ttu-id="7692d-240">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7692d-240">Select **Save**.</span></span>
    

  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="7692d-241">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="7692d-241">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="7692d-242"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="7692d-242"><a name="BKMK_add_SRV"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="7692d-243">N’oubliez pas que Cloudflare est responsable de la rendre disponible.</span><span class="sxs-lookup"><span data-stu-id="7692d-243">Please keep in mind that Cloudflare is responsible for making this functionality available.</span></span> <span data-ttu-id="7692d-244">Si vous voyez des différences entre les étapes ci-dessous et l’interface graphique graphique (INTERFACE utilisateur graphique) Cloudflare actuelle, tirez parti de [la communauté Cloudflare.](https://community.cloudflare.com/)</span><span class="sxs-lookup"><span data-stu-id="7692d-244">In case you see discrepancies between the steps below and the current Cloudflare GUI (Graphical User Interface), please leverage the [Cloudflare Community](https://community.cloudflare.com/).</span></span> 

1. <span data-ttu-id="7692d-245">To get started, go to your domains page at Cloudflare by using [this link](https://www.cloudflare.com/a/login).</span><span class="sxs-lookup"><span data-stu-id="7692d-245">To get started, go to your domains page at Cloudflare by using [this link](https://www.cloudflare.com/a/login).</span></span> <span data-ttu-id="7692d-246">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="7692d-246">You'll be prompted to log in first.</span></span>
      
2. <span data-ttu-id="7692d-247">Dans  la page d’accueil, sélectionnez le domaine à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="7692d-247">On the **Home** page, select the domain that you want to update.</span></span> 
  
3. <span data-ttu-id="7692d-248">Dans la page **Vue d’ensemble** de votre domaine, sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="7692d-248">On the **Overview** page for your domain, select **DNS**.</span></span>
  
4. <span data-ttu-id="7692d-249">Ajoutez le premier des deux enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="7692d-249">Add the first of the two SRV records.</span></span>

    <span data-ttu-id="7692d-250">Dans la page de **gestion DNS,** cliquez sur Ajouter un **enregistrement,** puis sélectionnez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7692d-250">On the **DNS management** page, click **Add record**, and then select the values from the first row of the following table.</span></span>
        
    | <span data-ttu-id="7692d-251">Type</span><span class="sxs-lookup"><span data-stu-id="7692d-251">Type</span></span> | <span data-ttu-id="7692d-252">Service</span><span class="sxs-lookup"><span data-stu-id="7692d-252">Service</span></span> | <span data-ttu-id="7692d-253">Protocole</span><span class="sxs-lookup"><span data-stu-id="7692d-253">Protocol</span></span> | <span data-ttu-id="7692d-254">Nom</span><span class="sxs-lookup"><span data-stu-id="7692d-254">Name</span></span> | <span data-ttu-id="7692d-255">Durée de vie</span><span class="sxs-lookup"><span data-stu-id="7692d-255">TTL</span></span> | <span data-ttu-id="7692d-256">Priorité</span><span class="sxs-lookup"><span data-stu-id="7692d-256">Priority</span></span> | <span data-ttu-id="7692d-257">Pondération</span><span class="sxs-lookup"><span data-stu-id="7692d-257">Weight</span></span> | <span data-ttu-id="7692d-258">Port</span><span class="sxs-lookup"><span data-stu-id="7692d-258">Port</span></span> | <span data-ttu-id="7692d-259">Target</span><span class="sxs-lookup"><span data-stu-id="7692d-259">Target</span></span> |
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="7692d-260">SRV</span><span class="sxs-lookup"><span data-stu-id="7692d-260">SRV</span></span>|<span data-ttu-id="7692d-261">_sip</span><span class="sxs-lookup"><span data-stu-id="7692d-261">_sip</span></span> |<span data-ttu-id="7692d-262">TLS</span><span class="sxs-lookup"><span data-stu-id="7692d-262">TLS</span></span> |<span data-ttu-id="7692d-263">Utilisez votre *domain_name*; par exemple, contoso.com</span><span class="sxs-lookup"><span data-stu-id="7692d-263">Use your *domain_name*; for example, contoso.com</span></span>  |<span data-ttu-id="7692d-264">30 minutes</span><span class="sxs-lookup"><span data-stu-id="7692d-264">30 minutes</span></span> | <span data-ttu-id="7692d-265">100</span><span class="sxs-lookup"><span data-stu-id="7692d-265">100</span></span>|<span data-ttu-id="7692d-266">1 </span><span class="sxs-lookup"><span data-stu-id="7692d-266">1</span></span> |<span data-ttu-id="7692d-267">443</span><span class="sxs-lookup"><span data-stu-id="7692d-267">443</span></span> |<span data-ttu-id="7692d-268">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="7692d-268">sipfed.online.lync.com</span></span>  |
    |<span data-ttu-id="7692d-269">SRV</span><span class="sxs-lookup"><span data-stu-id="7692d-269">SRV</span></span>|<span data-ttu-id="7692d-270">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="7692d-270">_sipfederationtls</span></span> | <span data-ttu-id="7692d-271">TCP</span><span class="sxs-lookup"><span data-stu-id="7692d-271">TCP</span></span>|<span data-ttu-id="7692d-272">Utilisez votre *domain_name*; par exemple, contoso.com</span><span class="sxs-lookup"><span data-stu-id="7692d-272">Use your *domain_name*; for example, contoso.com</span></span>   |<span data-ttu-id="7692d-273">30 minutes</span><span class="sxs-lookup"><span data-stu-id="7692d-273">30 minutes</span></span> |<span data-ttu-id="7692d-274">100</span><span class="sxs-lookup"><span data-stu-id="7692d-274">100</span></span> |<span data-ttu-id="7692d-275">1 </span><span class="sxs-lookup"><span data-stu-id="7692d-275">1</span></span> |<span data-ttu-id="7692d-276">5061</span><span class="sxs-lookup"><span data-stu-id="7692d-276">5061</span></span> | <span data-ttu-id="7692d-277">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="7692d-277">sipfed.online.lync.com</span></span> |

  
5. <span data-ttu-id="7692d-278">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7692d-278">Select **Save**.</span></span>

  
6. <span data-ttu-id="7692d-279">Ajoutez l’autre enregistrement SRV en choisissant les valeurs de la deuxième ligne du tableau.</span><span class="sxs-lookup"><span data-stu-id="7692d-279">Add the other SRV record by choosing the values from the second row of the table.</span></span> 

    
> [!NOTE]
>  <span data-ttu-id="7692d-p117">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="7692d-p117">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
