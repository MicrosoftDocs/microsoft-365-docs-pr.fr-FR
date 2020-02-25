---
title: Créer des enregistrements DNS auprès de WiX pour Office 365
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
ms.assetid: 7173c635-58b3-400f-95e0-97abe915565e
description: Découvrez comment vérifier votre domaine et configurer des enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur WiX pour Office 365.
ms.openlocfilehash: 43d2f2417153dd0c848c33736733237b1681c02c
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42243048"
---
# <a name="create-dns-records-at-wix-for-office-365"></a><span data-ttu-id="1ab57-103">Créer des enregistrements DNS auprès de WiX pour Office 365</span><span class="sxs-lookup"><span data-stu-id="1ab57-103">Create DNS records at Wix for Office 365</span></span>

 <span data-ttu-id="1ab57-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="1ab57-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="1ab57-105">Si WiX est votre fournisseur d’hébergement DNS, suivez la procédure décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier électronique, Skype entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="1ab57-105">If Wix is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="1ab57-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="1ab57-106">These are the main records to add.</span></span> 
  
- <span data-ttu-id="1ab57-107">[Ajoutez un enregistrement txt à des fins de vérification](#add-a-txt-record-for-verification).</span><span class="sxs-lookup"><span data-stu-id="1ab57-107">[Add a TXT record for verification](#add-a-txt-record-for-verification).</span></span>
    
- <span data-ttu-id="1ab57-108">[Ajoutez un enregistrement MX de sorte que le courrier électronique pour votre domaine arrivera dans Office 365](#add-an-mx-record-so-email-for-your-domain-will-come-to-office-365).</span><span class="sxs-lookup"><span data-stu-id="1ab57-108">[Add an MX record so email for your domain will come to Office 365](#add-an-mx-record-so-email-for-your-domain-will-come-to-office-365).</span></span>
    
- <span data-ttu-id="1ab57-109">[Ajoutez les cinq enregistrements CNAME requis pour Office 365](#add-the-five-cname-records-that-are-required-for-office-365).</span><span class="sxs-lookup"><span data-stu-id="1ab57-109">[Add the five CNAME records that are required for Office 365](#add-the-five-cname-records-that-are-required-for-office-365).</span></span>
    
- <span data-ttu-id="1ab57-110">[Ajoutez un enregistrement txt pour SPF afin d’éviter le courrier indésirable](#add-a-txt-record-for-spf-to-help-prevent-email-spam).</span><span class="sxs-lookup"><span data-stu-id="1ab57-110">[Add a TXT record for SPF to help prevent email spam](#add-a-txt-record-for-spf-to-help-prevent-email-spam).</span></span>
    
- <span data-ttu-id="1ab57-111">[Ajoutez les deux enregistrements SRV requis pour Office 365](#add-the-two-srv-records-that-are-required-for-office-365).</span><span class="sxs-lookup"><span data-stu-id="1ab57-111">[Add the two SRV records that are required for Office 365](#add-the-two-srv-records-that-are-required-for-office-365).</span></span>
    
<span data-ttu-id="1ab57-112">Une fois que vous avez ajouté ces enregistrements à WiX, votre domaine est configuré pour utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="1ab57-112">After you add these records at Wix, your domain will be set up to work with Office 365 services.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="1ab57-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="1ab57-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="1ab57-116">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="1ab57-116">Add a TXT record for verification</span></span>
<span data-ttu-id="1ab57-117"><a name="BKMK_txt"> </a></span><span class="sxs-lookup"><span data-stu-id="1ab57-117"><a name="BKMK_txt"> </a></span></span>

<span data-ttu-id="1ab57-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="1ab57-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1ab57-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="1ab57-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="1ab57-122">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="1ab57-122">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="1ab57-123">You'll be prompted to log in first.</span><span class="sxs-lookup"><span data-stu-id="1ab57-123">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="1ab57-124">Sur la page **Mes domaines** , dans la zone **avancé** , sélectionnez le bouton **modifier le DNS** .</span><span class="sxs-lookup"><span data-stu-id="1ab57-124">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="1ab57-125">Sélectionnez **+ Ajouter un autre** dans la ligne **txt (texte)** de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="1ab57-125">Select **+ Add another** in the **TXT (Text)** row of the DNS editor.</span></span> 
    
4. <span data-ttu-id="1ab57-126">In the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="1ab57-126">In the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="1ab57-127">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="1ab57-127">**Host Name**</span></span> <br/> |<span data-ttu-id="1ab57-128">**TXT Value (Valeur TXT)**</span><span class="sxs-lookup"><span data-stu-id="1ab57-128">**TXT Value**</span></span> <br/> |<span data-ttu-id="1ab57-129">**TTL**</span><span class="sxs-lookup"><span data-stu-id="1ab57-129">**TTL**</span></span> <br/> |
|<span data-ttu-id="1ab57-130">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="1ab57-130">Automatically populated</span></span>  <br/> |<span data-ttu-id="1ab57-131">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="1ab57-131">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="1ab57-132">**Remarque :** Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="1ab57-132">**Note:** This is an example.</span></span> <span data-ttu-id="1ab57-133">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="1ab57-133">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span>  [<span data-ttu-id="1ab57-134">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="1ab57-134">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)|<span data-ttu-id="1ab57-135">1 Hour</span><span class="sxs-lookup"><span data-stu-id="1ab57-135">1 Hour</span></span> <br/> |          |
   
5. <span data-ttu-id="1ab57-136">Sélectionnez le bouton **enregistrer le DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="1ab57-136">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="1ab57-137">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="1ab57-137">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="1ab57-138">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span><span class="sxs-lookup"><span data-stu-id="1ab57-138">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="1ab57-139">When Office 365 finds the correct TXT record, your domain is verified.</span><span class="sxs-lookup"><span data-stu-id="1ab57-139">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="1ab57-140">Dans le centre d’administration, accédez à la page **paramètres** \> des <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="1ab57-140">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="1ab57-141">Dans la page **domaines** , sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="1ab57-141">On the **Domains** page, select the domain that you are verifying.</span></span> 
  
  
3. <span data-ttu-id="1ab57-142">Sur la page **installation** , sélectionnez **Démarrer l’installation**.</span><span class="sxs-lookup"><span data-stu-id="1ab57-142">On the **Setup** page, select **Start setup**.</span></span>
   
  
4. <span data-ttu-id="1ab57-143">Sur la page **vérifier le domaine** , sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="1ab57-143">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="1ab57-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="1ab57-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="1ab57-147">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="1ab57-147">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="1ab57-148"><a name="BKMK_mx"> </a></span><span class="sxs-lookup"><span data-stu-id="1ab57-148"><a name="BKMK_mx"> </a></span></span>

1. <span data-ttu-id="1ab57-149">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="1ab57-149">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="1ab57-150">You'll be prompted to log in first.</span><span class="sxs-lookup"><span data-stu-id="1ab57-150">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="1ab57-151">Sur la page **Mes domaines** , dans la zone **boîtes aux lettres** , sélectionnez le lien **configurer votre enregistrement MX** .</span><span class="sxs-lookup"><span data-stu-id="1ab57-151">On the **My Domains** page, in the **Mailboxes** area, select the **Configure your MX records** link.</span></span> 
    
3. <span data-ttu-id="1ab57-152">Sélectionnez **autre** dans la liste déroulante **votre fournisseur de messagerie** .</span><span class="sxs-lookup"><span data-stu-id="1ab57-152">Choose **Other** from the **Your Email Provider** drop-down list.</span></span> 
    
4. <span data-ttu-id="1ab57-153">Sélectionnez **+ Ajouter un autre**.</span><span class="sxs-lookup"><span data-stu-id="1ab57-153">Select **+ Add another**.</span></span>
    
5. <span data-ttu-id="1ab57-154">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="1ab57-154">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
|<span data-ttu-id="1ab57-155">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="1ab57-155">**Host Name**</span></span>|<span data-ttu-id="1ab57-156">**Points to (Pointe vers)**</span><span class="sxs-lookup"><span data-stu-id="1ab57-156">**Points to**</span></span>|<span data-ttu-id="1ab57-157">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="1ab57-157">**Priority**</span></span>|<span data-ttu-id="1ab57-158">**TTL**</span><span class="sxs-lookup"><span data-stu-id="1ab57-158">**TTL**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1ab57-159">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="1ab57-159">Automatically populated</span></span> <br/> | <span data-ttu-id="1ab57-160">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="1ab57-160">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="1ab57-161">**Remarque :** Obtenez votre \* \<clé\> de domaine\* à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="1ab57-161">**Note:** Get your  *\<domain-key\>*  from your Office 365 account.</span></span>   [<span data-ttu-id="1ab57-162">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="1ab57-162">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md) |<span data-ttu-id="1ab57-163">0</span><span class="sxs-lookup"><span data-stu-id="1ab57-163">0</span></span>  <br/> <span data-ttu-id="1ab57-164">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/What-is-MX-priority-2784cc4d-95be-443d-b5f7-bb5dd867ba83).</span><span class="sxs-lookup"><span data-stu-id="1ab57-164">For more information about priority, see [What is MX priority?](https://support.office.com/article/What-is-MX-priority-2784cc4d-95be-443d-b5f7-bb5dd867ba83)</span></span> | <span data-ttu-id="1ab57-165">1 Hour</span><span class="sxs-lookup"><span data-stu-id="1ab57-165">1 Hour</span></span>|
   
6. <span data-ttu-id="1ab57-166">Si d’autres enregistrements MX sont répertoriés, supprimez-les chacun.</span><span class="sxs-lookup"><span data-stu-id="1ab57-166">If there are any other MX records listed, delete each of them.</span></span> 
    
7. <span data-ttu-id="1ab57-167">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ab57-167">Select **OK**.</span></span>
    
8. <span data-ttu-id="1ab57-168">Dans la boîte de dialogue de confirmation, sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ab57-168">In the confirmation dialog box, select **OK**.</span></span>
    
## <a name="add-the-five-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="1ab57-169">Ajouter les cinq enregistrements CNAMe requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="1ab57-169">Add the five CNAME records that are required for Office 365</span></span>
<span data-ttu-id="1ab57-170"><a name="BKMK_cname"> </a></span><span class="sxs-lookup"><span data-stu-id="1ab57-170"><a name="BKMK_cname"> </a></span></span>

1. <span data-ttu-id="1ab57-171">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="1ab57-171">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="1ab57-172">You'll be prompted to login first.</span><span class="sxs-lookup"><span data-stu-id="1ab57-172">You'll be prompted to login first.</span></span>
    
2. <span data-ttu-id="1ab57-173">Sur la page **Mes domaines** , dans la zone **avancé** , sélectionnez le bouton **modifier le DNS** .</span><span class="sxs-lookup"><span data-stu-id="1ab57-173">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="1ab57-174">Sélectionnez **+ Ajouter un autre** dans la ligne **CNAME (alias)** de l’éditeur DNS pour chaque enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="1ab57-174">Select **+ Add another** in the **CNAME (Aliases)** row of the DNS editor for each CNAME record.</span></span> 
    
4. <span data-ttu-id="1ab57-175">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="1ab57-175">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
|<span data-ttu-id="1ab57-176">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="1ab57-176">**Host Name**</span></span>|<span data-ttu-id="1ab57-177">**Points to (Pointe vers)**</span><span class="sxs-lookup"><span data-stu-id="1ab57-177">**Points to**</span></span>|<span data-ttu-id="1ab57-178">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="1ab57-178">**TTL**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ab57-179">autodiscover</span><span class="sxs-lookup"><span data-stu-id="1ab57-179">autodiscover</span></span>  <br/> |<span data-ttu-id="1ab57-180">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="1ab57-180">autodiscover.outlook.com</span></span>  <br/> |<span data-ttu-id="1ab57-181">1 Hour</span><span class="sxs-lookup"><span data-stu-id="1ab57-181">1 Hour</span></span>  <br/> |
|<span data-ttu-id="1ab57-182">sip</span><span class="sxs-lookup"><span data-stu-id="1ab57-182">sip</span></span>  <br/> |<span data-ttu-id="1ab57-183">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="1ab57-183">sipdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="1ab57-184">1 Hour</span><span class="sxs-lookup"><span data-stu-id="1ab57-184">1 Hour</span></span> <br/> |
|<span data-ttu-id="1ab57-185">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="1ab57-185">lyncdiscover</span></span>  <br/> |<span data-ttu-id="1ab57-186">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="1ab57-186">webdir.online.lync.com</span></span>   <br/> |<span data-ttu-id="1ab57-187">1 Hour</span><span class="sxs-lookup"><span data-stu-id="1ab57-187">1 Hour</span></span>  <br/> |
|<span data-ttu-id="1ab57-188">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="1ab57-188">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="1ab57-189">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="1ab57-189">enterpriseregistration.windows.net</span></span>  <br/> |<span data-ttu-id="1ab57-190">1 heure</span><span class="sxs-lookup"><span data-stu-id="1ab57-190">1 Hour</span></span> <br/> |
|<span data-ttu-id="1ab57-191">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="1ab57-191">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="1ab57-192">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="1ab57-192">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |<span data-ttu-id="1ab57-193">1 Hour</span><span class="sxs-lookup"><span data-stu-id="1ab57-193">1 Hour</span></span>  <br/> |
   
5. <span data-ttu-id="1ab57-194">Sélectionnez le bouton **enregistrer le DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="1ab57-194">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="1ab57-195">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span><span class="sxs-lookup"><span data-stu-id="1ab57-195">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="1ab57-196">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="1ab57-196">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="1ab57-197"><a name="BKMK_spf"> </a></span><span class="sxs-lookup"><span data-stu-id="1ab57-197"><a name="BKMK_spf"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="1ab57-198">You cannot have more than one TXT record for SPF for a domain.</span><span class="sxs-lookup"><span data-stu-id="1ab57-198">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="1ab57-199">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span><span class="sxs-lookup"><span data-stu-id="1ab57-199">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="1ab57-200">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="1ab57-200">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="1ab57-201">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="1ab57-201">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>  
  
1. <span data-ttu-id="1ab57-202">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="1ab57-202">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="1ab57-203">You'll be prompted to log in first.</span><span class="sxs-lookup"><span data-stu-id="1ab57-203">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="1ab57-204">Sur la page **Mes domaines** , dans la zone **avancé** , sélectionnez le bouton **modifier le DNS** .</span><span class="sxs-lookup"><span data-stu-id="1ab57-204">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="1ab57-205">Sélectionnez **+ Ajouter un autre** dans la ligne **txt (texte)** de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="1ab57-205">Select **+ Add another** in the **TXT (Text)** row of the DNS editor.</span></span> 
    
4. <span data-ttu-id="1ab57-206">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="1ab57-206">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
|<span data-ttu-id="1ab57-207">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="1ab57-207">**Host Name**</span></span>|<span data-ttu-id="1ab57-208">**TXT Value (Valeur TXT)**</span><span class="sxs-lookup"><span data-stu-id="1ab57-208">**TXT Value**</span></span>|<span data-ttu-id="1ab57-209">**TTL**</span><span class="sxs-lookup"><span data-stu-id="1ab57-209">**TTL**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ab57-210">[Laissez ce champ vide]</span><span class="sxs-lookup"><span data-stu-id="1ab57-210">[leave this blank]</span></span>  <br/> |<span data-ttu-id="1ab57-211">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="1ab57-211">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="1ab57-212">**Remarque :** Nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="1ab57-212">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span><br/> |<span data-ttu-id="1ab57-213">TXT</span><span class="sxs-lookup"><span data-stu-id="1ab57-213">TXT</span></span>  <br/> | <span data-ttu-id="1ab57-214">1 Hour</span><span class="sxs-lookup"><span data-stu-id="1ab57-214">1 Hour</span></span> |
   
5. <span data-ttu-id="1ab57-215">Sélectionnez le bouton **enregistrer le DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="1ab57-215">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="1ab57-216">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span><span class="sxs-lookup"><span data-stu-id="1ab57-216">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="1ab57-217">Ajouter les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="1ab57-217">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="1ab57-218"><a name="BKMK_srv"> </a></span><span class="sxs-lookup"><span data-stu-id="1ab57-218"><a name="BKMK_srv"> </a></span></span>

1. <span data-ttu-id="1ab57-219">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="1ab57-219">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="1ab57-220">You'll be prompted to log in first.</span><span class="sxs-lookup"><span data-stu-id="1ab57-220">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="1ab57-221">Sur la page **Mes domaines** , dans la zone **avancé** , sélectionnez le bouton **modifier le DNS** .</span><span class="sxs-lookup"><span data-stu-id="1ab57-221">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="1ab57-222">Sélectionnez **+ Ajouter un autre** dans la ligne **SRV** de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="1ab57-222">Select **+ Add another** in the **SRV** row of the DNS editor.</span></span> 
    
4. <span data-ttu-id="1ab57-223">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="1ab57-223">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
|<span data-ttu-id="1ab57-224">**Service**</span><span class="sxs-lookup"><span data-stu-id="1ab57-224">**Service**</span></span>|<span data-ttu-id="1ab57-225">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="1ab57-225">**Protocol**</span></span>|<span data-ttu-id="1ab57-226">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="1ab57-226">**Name**</span></span>|<span data-ttu-id="1ab57-227">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="1ab57-227">**Weight**</span></span>|<span data-ttu-id="1ab57-228">**Port**</span><span class="sxs-lookup"><span data-stu-id="1ab57-228">**Port**</span></span>|<span data-ttu-id="1ab57-229">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="1ab57-229">**Target**</span></span>|<span data-ttu-id="1ab57-230">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="1ab57-230">**Priority**</span></span>|<span data-ttu-id="1ab57-231">**TTL**</span><span class="sxs-lookup"><span data-stu-id="1ab57-231">**TTL**</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1ab57-232">sip</span><span class="sxs-lookup"><span data-stu-id="1ab57-232">sip</span></span>  |<span data-ttu-id="1ab57-233">tls</span><span class="sxs-lookup"><span data-stu-id="1ab57-233">tls</span></span>  |<span data-ttu-id="1ab57-234">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="1ab57-234">Automatically populated</span></span> |<span data-ttu-id="1ab57-235">0,1</span><span class="sxs-lookup"><span data-stu-id="1ab57-235">1</span></span>  |<span data-ttu-id="1ab57-236">443</span><span class="sxs-lookup"><span data-stu-id="1ab57-236">443</span></span>   |<span data-ttu-id="1ab57-237">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="1ab57-237">sipdir.online.lync.com</span></span> |<span data-ttu-id="1ab57-238">100</span><span class="sxs-lookup"><span data-stu-id="1ab57-238">100</span></span> |<span data-ttu-id="1ab57-239">1 Hour</span><span class="sxs-lookup"><span data-stu-id="1ab57-239">1 Hour</span></span> |
|<span data-ttu-id="1ab57-240">sipfed</span><span class="sxs-lookup"><span data-stu-id="1ab57-240">sipfed</span></span>|<span data-ttu-id="1ab57-241">tcp</span><span class="sxs-lookup"><span data-stu-id="1ab57-241">tcp</span></span> |<span data-ttu-id="1ab57-242">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="1ab57-242">Automatically populated</span></span>|<span data-ttu-id="1ab57-243">0,1</span><span class="sxs-lookup"><span data-stu-id="1ab57-243">1</span></span> |<span data-ttu-id="1ab57-244">5061</span><span class="sxs-lookup"><span data-stu-id="1ab57-244">5061</span></span> |<span data-ttu-id="1ab57-245">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="1ab57-245">sipfed.online.lync.com</span></span>|<span data-ttu-id="1ab57-246">100</span><span class="sxs-lookup"><span data-stu-id="1ab57-246">100</span></span> | <span data-ttu-id="1ab57-247">1 Hour</span><span class="sxs-lookup"><span data-stu-id="1ab57-247">1 Hour</span></span> |
   
5. <span data-ttu-id="1ab57-248">Sélectionnez le bouton **enregistrer le DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="1ab57-248">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="1ab57-249">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span><span class="sxs-lookup"><span data-stu-id="1ab57-249">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="1ab57-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="1ab57-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  

