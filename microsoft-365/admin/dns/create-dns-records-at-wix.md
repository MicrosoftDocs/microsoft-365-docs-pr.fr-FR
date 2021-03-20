---
title: Créer des enregistrements DNS sur Wix pour Microsoft
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
ms.assetid: 7173c635-58b3-400f-95e0-97abe915565e
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype Entreprise Online et d’autres services via Wix pour Microsoft.
ms.openlocfilehash: 3ec2ea0dc24e1872ba22e591fae96b39a9a0deee
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50916105"
---
# <a name="create-dns-records-at-wix-for-microsoft"></a><span data-ttu-id="ecca3-103">Créer des enregistrements DNS sur Wix pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="ecca3-103">Create DNS records at Wix for Microsoft</span></span>

<span data-ttu-id="ecca3-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="ecca3-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="ecca3-105">Si Wix est votre fournisseur d’hébergement DNS, suivez les étapes de cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="ecca3-105">If Wix is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>

<span data-ttu-id="ecca3-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="ecca3-106">These are the main records to add.</span></span> 
  
- <span data-ttu-id="ecca3-107">[Ajoutez un enregistrement TXT à des fins de vérification.](#add-a-txt-record-for-verification)</span><span class="sxs-lookup"><span data-stu-id="ecca3-107">[Add a TXT record for verification](#add-a-txt-record-for-verification).</span></span>
    
- <span data-ttu-id="ecca3-108">[Ajoutez un enregistrement MX afin que le courrier électronique de votre domaine soit envoyé à Microsoft.](#add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft)</span><span class="sxs-lookup"><span data-stu-id="ecca3-108">[Add an MX record so email for your domain will come to Microsoft](#add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft).</span></span>
    
- <span data-ttu-id="ecca3-109">[Ajoutez les cinq enregistrements CNAME requis pour Microsoft.](#add-the-five-cname-records-that-are-required-for-microsoft)</span><span class="sxs-lookup"><span data-stu-id="ecca3-109">[Add the five CNAME records that are required for Microsoft](#add-the-five-cname-records-that-are-required-for-microsoft).</span></span>
    
- <span data-ttu-id="ecca3-110">[Ajoutez un enregistrement TXT pour SPF pour éviter le courrier indésirable.](#add-a-txt-record-for-spf-to-help-prevent-email-spam)</span><span class="sxs-lookup"><span data-stu-id="ecca3-110">[Add a TXT record for SPF to help prevent email spam](#add-a-txt-record-for-spf-to-help-prevent-email-spam).</span></span>
    
- <span data-ttu-id="ecca3-111">[Ajoutez les deux enregistrements SRV requis pour Microsoft.](#add-the-two-srv-records-that-are-required-for-microsoft)</span><span class="sxs-lookup"><span data-stu-id="ecca3-111">[Add the two SRV records that are required for Microsoft](#add-the-two-srv-records-that-are-required-for-microsoft).</span></span>
    
<span data-ttu-id="ecca3-112">Une fois ces enregistrements ajoutés sur Wix, votre domaine est installé pour fonctionner avec les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ecca3-112">After you add these records at Wix, your domain will be set up to work with Microsoft services.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="ecca3-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ecca3-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 

  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="ecca3-116">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="ecca3-116">Add a TXT record for verification</span></span>
<span data-ttu-id="ecca3-117"><a name="BKMK_txt"> </a></span><span class="sxs-lookup"><span data-stu-id="ecca3-117"><a name="BKMK_txt"> </a></span></span>

<span data-ttu-id="ecca3-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="ecca3-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ecca3-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="ecca3-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 

> [!NOTE]
> <span data-ttu-id="ecca3-122">WIX ne prend pas en charge les entrées DNS pour les sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="ecca3-122">WIX does not support DNS entries for subdomains.</span></span>
  
1. <span data-ttu-id="ecca3-123">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="ecca3-123">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="ecca3-124">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ecca3-124">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="ecca3-125">Dans la page **Mes domaines,** dans la **zone** Avancé, sélectionnez le bouton **Modifier le DNS.**</span><span class="sxs-lookup"><span data-stu-id="ecca3-125">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="ecca3-126">Sélectionnez **+ Ajoutez-en** une autre dans la ligne **TXT (texte)** de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="ecca3-126">Select **+ Add another** in the **TXT (Text)** row of the DNS editor.</span></span> 
    
4. <span data-ttu-id="ecca3-127">In the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="ecca3-127">In the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
   ||||
   |:-----|:-----|:-----|
   | <span data-ttu-id="ecca3-128">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="ecca3-128">Host Name</span></span> <br/> | <span data-ttu-id="ecca3-129">TXT Value</span><span class="sxs-lookup"><span data-stu-id="ecca3-129">TXT Value</span></span> <br/> | <span data-ttu-id="ecca3-130">TTL (Durée de vie)</span><span class="sxs-lookup"><span data-stu-id="ecca3-130">TTL</span></span> <br/> |
   |<span data-ttu-id="ecca3-131">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="ecca3-131">Automatically populated</span></span>  <br/> |<span data-ttu-id="ecca3-132">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="ecca3-132">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="ecca3-133">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="ecca3-133">**Note:** This is an example.</span></span> <span data-ttu-id="ecca3-134">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="ecca3-134">Use your specific **Destination or Points to Address** value here, from the table.</span></span>  [<span data-ttu-id="ecca3-135">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="ecca3-135">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)|<span data-ttu-id="ecca3-136">1 heure</span><span class="sxs-lookup"><span data-stu-id="ecca3-136">1 Hour</span></span> <br/> |          |
   
5. <span data-ttu-id="ecca3-137">Sélectionnez **le bouton Enregistrer DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="ecca3-137">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="ecca3-138">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="ecca3-138">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="ecca3-139">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ecca3-139">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="ecca3-140">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="ecca3-140">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="ecca3-141">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="ecca3-141">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="ecca3-142">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="ecca3-142">On the **Domains** page, select the domain that you are verifying.</span></span> 
  
3. <span data-ttu-id="ecca3-143">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="ecca3-143">On the **Setup** page, select **Start setup**.</span></span>
   
4. <span data-ttu-id="ecca3-144">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="ecca3-144">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="ecca3-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ecca3-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 

  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="ecca3-148">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="ecca3-148">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="ecca3-149"><a name="BKMK_mx"> </a></span><span class="sxs-lookup"><span data-stu-id="ecca3-149"><a name="BKMK_mx"> </a></span></span>

1. <span data-ttu-id="ecca3-150">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="ecca3-150">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="ecca3-151">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ecca3-151">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="ecca3-152">Dans la page **Mes domaines,** dans la zone **Boîtes** aux lettres, sélectionnez le lien Configurer vos enregistrements **MX.**</span><span class="sxs-lookup"><span data-stu-id="ecca3-152">On the **My Domains** page, in the **Mailboxes** area, select the **Configure your MX records** link.</span></span> 
    
3. <span data-ttu-id="ecca3-153">Choisissez **Autre dans** la **liste** de listes de votre fournisseur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="ecca3-153">Choose **Other** from the **Your Email Provider** drop-down list.</span></span> 
    
4. <span data-ttu-id="ecca3-154">Sélectionnez **+ Ajoutez-en un autre.**</span><span class="sxs-lookup"><span data-stu-id="ecca3-154">Select **+ Add another**.</span></span>
    
5. <span data-ttu-id="ecca3-155">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="ecca3-155">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
   | <span data-ttu-id="ecca3-156">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="ecca3-156">Host Name</span></span> | <span data-ttu-id="ecca3-157">Points to </span><span class="sxs-lookup"><span data-stu-id="ecca3-157">Points to</span></span> | <span data-ttu-id="ecca3-158">Priority (Priorité)</span><span class="sxs-lookup"><span data-stu-id="ecca3-158">Priority</span></span> | <span data-ttu-id="ecca3-159">TTL (Durée de vie)</span><span class="sxs-lookup"><span data-stu-id="ecca3-159">TTL</span></span> |
   |:-----|:-----|:-----|:-----|
   |<span data-ttu-id="ecca3-160">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="ecca3-160">Automatically populated</span></span> <br/> | <span data-ttu-id="ecca3-161">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="ecca3-161">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="ecca3-162">**Remarque :** Obtenez votre *\<domain-key\>* depuis votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ecca3-162">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>   [<span data-ttu-id="ecca3-163">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="ecca3-163">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md) |<span data-ttu-id="ecca3-164">0</span><span class="sxs-lookup"><span data-stu-id="ecca3-164">0</span></span>  <br/> <span data-ttu-id="ecca3-165">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](../setup/domains-faq.yml).</span><span class="sxs-lookup"><span data-stu-id="ecca3-165">For more information about priority, see [What is MX priority?](../setup/domains-faq.yml)</span></span> | <span data-ttu-id="ecca3-166">1 heure</span><span class="sxs-lookup"><span data-stu-id="ecca3-166">1 Hour</span></span>|
   
6. <span data-ttu-id="ecca3-167">Si d’autres enregistrements MX sont répertoriés, supprimez chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="ecca3-167">If there are any other MX records listed, delete each of them.</span></span> 
    
7. <span data-ttu-id="ecca3-168">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="ecca3-168">Select **OK**.</span></span>
    
8. <span data-ttu-id="ecca3-169">Dans la boîte de dialogue de confirmation, sélectionnez **OK.**</span><span class="sxs-lookup"><span data-stu-id="ecca3-169">In the confirmation dialog box, select **OK**.</span></span>
    
    
## <a name="add-the-five-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="ecca3-170">Ajouter les cinq enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="ecca3-170">Add the five CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="ecca3-171"><a name="BKMK_cname"> </a></span><span class="sxs-lookup"><span data-stu-id="ecca3-171"><a name="BKMK_cname"> </a></span></span>

1. <span data-ttu-id="ecca3-172">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="ecca3-172">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="ecca3-173">You'll be prompted to login first.</span><span class="sxs-lookup"><span data-stu-id="ecca3-173">You'll be prompted to login first.</span></span>
    
2. <span data-ttu-id="ecca3-174">Dans la page **Mes domaines,** dans la **zone** Avancé, sélectionnez le bouton **Modifier le DNS.**</span><span class="sxs-lookup"><span data-stu-id="ecca3-174">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="ecca3-175">Sélectionnez **+ Ajoutez-en** une autre dans la ligne **CNAME (Alias)** de l’éditeur DNS pour chaque enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="ecca3-175">Select **+ Add another** in the **CNAME (Aliases)** row of the DNS editor for each CNAME record.</span></span> 
    
4. <span data-ttu-id="ecca3-176">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="ecca3-176">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
   | <span data-ttu-id="ecca3-177">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="ecca3-177">Host Name</span></span> | <span data-ttu-id="ecca3-178">Points to </span><span class="sxs-lookup"><span data-stu-id="ecca3-178">Points to</span></span> | <span data-ttu-id="ecca3-179">Durée de vie</span><span class="sxs-lookup"><span data-stu-id="ecca3-179">TTL</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="ecca3-180">autodiscover</span><span class="sxs-lookup"><span data-stu-id="ecca3-180">autodiscover</span></span>  <br/> |<span data-ttu-id="ecca3-181">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="ecca3-181">autodiscover.outlook.com</span></span>  <br/> |<span data-ttu-id="ecca3-182">1 heure</span><span class="sxs-lookup"><span data-stu-id="ecca3-182">1 Hour</span></span>  <br/> |
   |<span data-ttu-id="ecca3-183">sip</span><span class="sxs-lookup"><span data-stu-id="ecca3-183">sip</span></span>  <br/> |<span data-ttu-id="ecca3-184">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="ecca3-184">sipdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="ecca3-185">1 heure</span><span class="sxs-lookup"><span data-stu-id="ecca3-185">1 Hour</span></span> <br/> |
   |<span data-ttu-id="ecca3-186">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="ecca3-186">lyncdiscover</span></span>  <br/> |<span data-ttu-id="ecca3-187">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="ecca3-187">webdir.online.lync.com</span></span>   <br/> |<span data-ttu-id="ecca3-188">1 heure</span><span class="sxs-lookup"><span data-stu-id="ecca3-188">1 Hour</span></span>  <br/> |
   |<span data-ttu-id="ecca3-189">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="ecca3-189">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="ecca3-190">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="ecca3-190">enterpriseregistration.windows.net</span></span>  <br/> |<span data-ttu-id="ecca3-191">1 heure</span><span class="sxs-lookup"><span data-stu-id="ecca3-191">1 Hour</span></span> <br/> |
   |<span data-ttu-id="ecca3-192">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="ecca3-192">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="ecca3-193">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="ecca3-193">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |<span data-ttu-id="ecca3-194">1 Hour</span><span class="sxs-lookup"><span data-stu-id="ecca3-194">1 Hour</span></span>  <br/> |
   
5. <span data-ttu-id="ecca3-195">Sélectionnez **le bouton Enregistrer DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="ecca3-195">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="ecca3-196">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="ecca3-196">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="ecca3-197">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="ecca3-197">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="ecca3-198"><a name="BKMK_spf"> </a></span><span class="sxs-lookup"><span data-stu-id="ecca3-198"><a name="BKMK_spf"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="ecca3-199">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="ecca3-199">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="ecca3-200">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="ecca3-200">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="ecca3-201">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ecca3-201">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="ecca3-202">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel de manière à n’avoir *qu’un seul* enregistrement SPF incluant les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="ecca3-202">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>  
  
1. <span data-ttu-id="ecca3-203">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="ecca3-203">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="ecca3-204">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ecca3-204">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="ecca3-205">Dans la page **Mes domaines,** dans la **zone** Avancé, sélectionnez le bouton **Modifier le DNS.**</span><span class="sxs-lookup"><span data-stu-id="ecca3-205">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="ecca3-206">Sélectionnez **+ Ajoutez-en** une autre dans la ligne **TXT (texte)** de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="ecca3-206">Select **+ Add another** in the **TXT (Text)** row of the DNS editor.</span></span> 
    
4. <span data-ttu-id="ecca3-207">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="ecca3-207">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
   | <span data-ttu-id="ecca3-208">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="ecca3-208">Host Name</span></span> | <span data-ttu-id="ecca3-209">TXT Value</span><span class="sxs-lookup"><span data-stu-id="ecca3-209">TXT Value</span></span> | <span data-ttu-id="ecca3-210">TTL (Durée de vie)</span><span class="sxs-lookup"><span data-stu-id="ecca3-210">TTL</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="ecca3-211">[laissez ce vide]</span><span class="sxs-lookup"><span data-stu-id="ecca3-211">[leave this blank]</span></span>  <br/> |<span data-ttu-id="ecca3-212">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="ecca3-212">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="ecca3-213">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="ecca3-213">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span><br/> |<span data-ttu-id="ecca3-214">TXT</span><span class="sxs-lookup"><span data-stu-id="ecca3-214">TXT</span></span>  <br/> | <span data-ttu-id="ecca3-215">1 Hour</span><span class="sxs-lookup"><span data-stu-id="ecca3-215">1 Hour</span></span> |
   
5. <span data-ttu-id="ecca3-216">Sélectionnez **le bouton Enregistrer DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="ecca3-216">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="ecca3-217">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="ecca3-217">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
    
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="ecca3-218">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="ecca3-218">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="ecca3-219"><a name="BKMK_srv"> </a></span><span class="sxs-lookup"><span data-stu-id="ecca3-219"><a name="BKMK_srv"> </a></span></span>

1. <span data-ttu-id="ecca3-220">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="ecca3-220">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="ecca3-221">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ecca3-221">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="ecca3-222">Dans la page **Mes domaines,** dans la **zone** Avancé, sélectionnez le bouton **Modifier le DNS.**</span><span class="sxs-lookup"><span data-stu-id="ecca3-222">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="ecca3-223">Sélectionnez **+ Ajoutez-en** une autre dans la **ligne SRV** de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="ecca3-223">Select **+ Add another** in the **SRV** row of the DNS editor.</span></span> 
    
4. <span data-ttu-id="ecca3-224">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="ecca3-224">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
   | <span data-ttu-id="ecca3-225">Service</span><span class="sxs-lookup"><span data-stu-id="ecca3-225">Service</span></span> | <span data-ttu-id="ecca3-226">Protocole</span><span class="sxs-lookup"><span data-stu-id="ecca3-226">Protocol</span></span> | <span data-ttu-id="ecca3-227">Nom</span><span class="sxs-lookup"><span data-stu-id="ecca3-227">Name</span></span> | <span data-ttu-id="ecca3-228">Pondération</span><span class="sxs-lookup"><span data-stu-id="ecca3-228">Weight</span></span> | <span data-ttu-id="ecca3-229">Port</span><span class="sxs-lookup"><span data-stu-id="ecca3-229">Port</span></span> | <span data-ttu-id="ecca3-230">Target</span><span class="sxs-lookup"><span data-stu-id="ecca3-230">Target</span></span> | <span data-ttu-id="ecca3-231">Priority (Priorité)</span><span class="sxs-lookup"><span data-stu-id="ecca3-231">Priority</span></span> | <span data-ttu-id="ecca3-232">TTL (Durée de vie)</span><span class="sxs-lookup"><span data-stu-id="ecca3-232">TTL</span></span> |
   |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
   |<span data-ttu-id="ecca3-233">sip</span><span class="sxs-lookup"><span data-stu-id="ecca3-233">sip</span></span>  |<span data-ttu-id="ecca3-234">tls</span><span class="sxs-lookup"><span data-stu-id="ecca3-234">tls</span></span>  |<span data-ttu-id="ecca3-235">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="ecca3-235">Automatically populated</span></span> |<span data-ttu-id="ecca3-236">1</span><span class="sxs-lookup"><span data-stu-id="ecca3-236">1</span></span>  |<span data-ttu-id="ecca3-237">443</span><span class="sxs-lookup"><span data-stu-id="ecca3-237">443</span></span>   |<span data-ttu-id="ecca3-238">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="ecca3-238">sipdir.online.lync.com</span></span> |<span data-ttu-id="ecca3-239">100</span><span class="sxs-lookup"><span data-stu-id="ecca3-239">100</span></span> |<span data-ttu-id="ecca3-240">1 Hour</span><span class="sxs-lookup"><span data-stu-id="ecca3-240">1 Hour</span></span> |
   |<span data-ttu-id="ecca3-241">sipfed</span><span class="sxs-lookup"><span data-stu-id="ecca3-241">sipfed</span></span>|<span data-ttu-id="ecca3-242">tcp</span><span class="sxs-lookup"><span data-stu-id="ecca3-242">tcp</span></span> |<span data-ttu-id="ecca3-243">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="ecca3-243">Automatically populated</span></span>|<span data-ttu-id="ecca3-244">1</span><span class="sxs-lookup"><span data-stu-id="ecca3-244">1</span></span> |<span data-ttu-id="ecca3-245">5061</span><span class="sxs-lookup"><span data-stu-id="ecca3-245">5061</span></span> |<span data-ttu-id="ecca3-246">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="ecca3-246">sipfed.online.lync.com</span></span>|<span data-ttu-id="ecca3-247">100</span><span class="sxs-lookup"><span data-stu-id="ecca3-247">100</span></span> | <span data-ttu-id="ecca3-248">1 Hour</span><span class="sxs-lookup"><span data-stu-id="ecca3-248">1 Hour</span></span> |
   
5. <span data-ttu-id="ecca3-249">Sélectionnez **le bouton Enregistrer DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="ecca3-249">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="ecca3-250">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="ecca3-250">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
> [!NOTE]
> <span data-ttu-id="ecca3-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ecca3-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
