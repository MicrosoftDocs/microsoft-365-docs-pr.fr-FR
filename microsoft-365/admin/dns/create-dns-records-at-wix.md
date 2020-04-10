---
title: Créer des enregistrements DNS auprès de WiX pour Office 365
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: article
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
ms.openlocfilehash: 8487c49e989bf2db345ae9e6d0e2970c5eb40cb6
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "43211061"
---
# <a name="create-dns-records-at-wix-for-office-365"></a><span data-ttu-id="65f6b-103">Créer des enregistrements DNS auprès de WiX pour Office 365</span><span class="sxs-lookup"><span data-stu-id="65f6b-103">Create DNS records at Wix for Office 365</span></span>

 <span data-ttu-id="65f6b-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="65f6b-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="65f6b-105">Si WiX est votre fournisseur d’hébergement DNS, suivez la procédure décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier électronique, Skype entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="65f6b-105">If Wix is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="65f6b-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="65f6b-106">These are the main records to add.</span></span> 
  
- <span data-ttu-id="65f6b-107">[Ajoutez un enregistrement txt à des fins de vérification](#add-a-txt-record-for-verification).</span><span class="sxs-lookup"><span data-stu-id="65f6b-107">[Add a TXT record for verification](#add-a-txt-record-for-verification).</span></span>
    
- <span data-ttu-id="65f6b-108">[Ajoutez un enregistrement MX de sorte que le courrier électronique pour votre domaine arrivera dans Office 365](#add-an-mx-record-so-email-for-your-domain-will-come-to-office-365).</span><span class="sxs-lookup"><span data-stu-id="65f6b-108">[Add an MX record so email for your domain will come to Office 365](#add-an-mx-record-so-email-for-your-domain-will-come-to-office-365).</span></span>
    
- <span data-ttu-id="65f6b-109">[Ajoutez les cinq enregistrements CNAME requis pour Office 365](#add-the-five-cname-records-that-are-required-for-office-365).</span><span class="sxs-lookup"><span data-stu-id="65f6b-109">[Add the five CNAME records that are required for Office 365](#add-the-five-cname-records-that-are-required-for-office-365).</span></span>
    
- <span data-ttu-id="65f6b-110">[Ajoutez un enregistrement txt pour SPF afin d’éviter le courrier indésirable](#add-a-txt-record-for-spf-to-help-prevent-email-spam).</span><span class="sxs-lookup"><span data-stu-id="65f6b-110">[Add a TXT record for SPF to help prevent email spam](#add-a-txt-record-for-spf-to-help-prevent-email-spam).</span></span>
    
- <span data-ttu-id="65f6b-111">[Ajoutez les deux enregistrements SRV requis pour Office 365](#add-the-two-srv-records-that-are-required-for-office-365).</span><span class="sxs-lookup"><span data-stu-id="65f6b-111">[Add the two SRV records that are required for Office 365](#add-the-two-srv-records-that-are-required-for-office-365).</span></span>
    
<span data-ttu-id="65f6b-112">Une fois que vous avez ajouté ces enregistrements à WiX, votre domaine est configuré pour utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="65f6b-112">After you add these records at Wix, your domain will be set up to work with Office 365 services.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="65f6b-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="65f6b-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="65f6b-116">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="65f6b-116">Add a TXT record for verification</span></span>
<span data-ttu-id="65f6b-117"><a name="BKMK_txt"> </a></span><span class="sxs-lookup"><span data-stu-id="65f6b-117"><a name="BKMK_txt"> </a></span></span>

<span data-ttu-id="65f6b-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="65f6b-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="65f6b-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="65f6b-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="65f6b-122">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="65f6b-122">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="65f6b-123">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="65f6b-123">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="65f6b-124">Sur la page **Mes domaines** , dans la zone **avancé** , sélectionnez le bouton **modifier le DNS** .</span><span class="sxs-lookup"><span data-stu-id="65f6b-124">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="65f6b-125">Sélectionnez **+ Ajouter un autre** dans la ligne **txt (texte)** de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="65f6b-125">Select **+ Add another** in the **TXT (Text)** row of the DNS editor.</span></span> 
    
4. <span data-ttu-id="65f6b-126">In the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="65f6b-126">In the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="65f6b-127">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="65f6b-127">**Host Name**</span></span> <br/> |<span data-ttu-id="65f6b-128">**VALEUR TXT**</span><span class="sxs-lookup"><span data-stu-id="65f6b-128">**TXT Value**</span></span> <br/> |<span data-ttu-id="65f6b-129">**TTL**</span><span class="sxs-lookup"><span data-stu-id="65f6b-129">**TTL**</span></span> <br/> |
|<span data-ttu-id="65f6b-130">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="65f6b-130">Automatically populated</span></span>  <br/> |<span data-ttu-id="65f6b-131">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="65f6b-131">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="65f6b-132">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="65f6b-132">**Note:** This is an example.</span></span> <span data-ttu-id="65f6b-133">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="65f6b-133">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span>  [<span data-ttu-id="65f6b-134">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="65f6b-134">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)|<span data-ttu-id="65f6b-135">1 Hour</span><span class="sxs-lookup"><span data-stu-id="65f6b-135">1 Hour</span></span> <br/> |          |
   
5. <span data-ttu-id="65f6b-136">Sélectionnez le bouton **enregistrer le DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="65f6b-136">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="65f6b-137">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="65f6b-137">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="65f6b-138">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Office 365 et demandez à Office 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="65f6b-138">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="65f6b-139">Lorsqu’Office 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="65f6b-139">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="65f6b-140">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="65f6b-140">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="65f6b-141">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="65f6b-141">On the **Domains** page, select the domain that you are verifying.</span></span> 
  
  
3. <span data-ttu-id="65f6b-142">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="65f6b-142">On the **Setup** page, select **Start setup**.</span></span>
   
  
4. <span data-ttu-id="65f6b-143">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="65f6b-143">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="65f6b-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="65f6b-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="65f6b-147">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="65f6b-147">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="65f6b-148"><a name="BKMK_mx"> </a></span><span class="sxs-lookup"><span data-stu-id="65f6b-148"><a name="BKMK_mx"> </a></span></span>

1. <span data-ttu-id="65f6b-149">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="65f6b-149">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="65f6b-150">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="65f6b-150">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="65f6b-151">Sur la page **Mes domaines** , dans la zone **boîtes aux lettres** , sélectionnez le lien **configurer votre enregistrement MX** .</span><span class="sxs-lookup"><span data-stu-id="65f6b-151">On the **My Domains** page, in the **Mailboxes** area, select the **Configure your MX records** link.</span></span> 
    
3. <span data-ttu-id="65f6b-152">Sélectionnez **autre** dans la liste déroulante **votre fournisseur de messagerie** .</span><span class="sxs-lookup"><span data-stu-id="65f6b-152">Choose **Other** from the **Your Email Provider** drop-down list.</span></span> 
    
4. <span data-ttu-id="65f6b-153">Sélectionnez **+ Ajouter un autre**.</span><span class="sxs-lookup"><span data-stu-id="65f6b-153">Select **+ Add another**.</span></span>
    
5. <span data-ttu-id="65f6b-154">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="65f6b-154">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
|<span data-ttu-id="65f6b-155">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="65f6b-155">**Host Name**</span></span>|<span data-ttu-id="65f6b-156">**Points to (Pointe vers)**</span><span class="sxs-lookup"><span data-stu-id="65f6b-156">**Points to**</span></span>|<span data-ttu-id="65f6b-157">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="65f6b-157">**Priority**</span></span>|<span data-ttu-id="65f6b-158">**TTL**</span><span class="sxs-lookup"><span data-stu-id="65f6b-158">**TTL**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="65f6b-159">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="65f6b-159">Automatically populated</span></span> <br/> | <span data-ttu-id="65f6b-160">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="65f6b-160">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="65f6b-161">**Remarque :** Obtenez votre \* \<clé\> de domaine\* à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="65f6b-161">**Note:** Get your  *\<domain-key\>*  from your Office 365 account.</span></span>   [<span data-ttu-id="65f6b-162">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="65f6b-162">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md) |<span data-ttu-id="65f6b-163">0</span><span class="sxs-lookup"><span data-stu-id="65f6b-163">0</span></span>  <br/> <span data-ttu-id="65f6b-164">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/What-is-MX-priority-2784cc4d-95be-443d-b5f7-bb5dd867ba83).</span><span class="sxs-lookup"><span data-stu-id="65f6b-164">For more information about priority, see [What is MX priority?](https://support.office.com/article/What-is-MX-priority-2784cc4d-95be-443d-b5f7-bb5dd867ba83)</span></span> | <span data-ttu-id="65f6b-165">1 Hour</span><span class="sxs-lookup"><span data-stu-id="65f6b-165">1 Hour</span></span>|
   
6. <span data-ttu-id="65f6b-166">Si d’autres enregistrements MX sont répertoriés, supprimez-les chacun.</span><span class="sxs-lookup"><span data-stu-id="65f6b-166">If there are any other MX records listed, delete each of them.</span></span> 
    
7. <span data-ttu-id="65f6b-167">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="65f6b-167">Select **OK**.</span></span>
    
8. <span data-ttu-id="65f6b-168">Dans la boîte de dialogue de confirmation, sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="65f6b-168">In the confirmation dialog box, select **OK**.</span></span>
    
## <a name="add-the-five-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="65f6b-169">Ajouter les cinq enregistrements CNAMe requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="65f6b-169">Add the five CNAME records that are required for Office 365</span></span>
<span data-ttu-id="65f6b-170"><a name="BKMK_cname"> </a></span><span class="sxs-lookup"><span data-stu-id="65f6b-170"><a name="BKMK_cname"> </a></span></span>

1. <span data-ttu-id="65f6b-171">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="65f6b-171">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="65f6b-172">You'll be prompted to login first.</span><span class="sxs-lookup"><span data-stu-id="65f6b-172">You'll be prompted to login first.</span></span>
    
2. <span data-ttu-id="65f6b-173">Sur la page **Mes domaines** , dans la zone **avancé** , sélectionnez le bouton **modifier le DNS** .</span><span class="sxs-lookup"><span data-stu-id="65f6b-173">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="65f6b-174">Sélectionnez **+ Ajouter un autre** dans la ligne **CNAME (alias)** de l’éditeur DNS pour chaque enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="65f6b-174">Select **+ Add another** in the **CNAME (Aliases)** row of the DNS editor for each CNAME record.</span></span> 
    
4. <span data-ttu-id="65f6b-175">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="65f6b-175">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
|<span data-ttu-id="65f6b-176">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="65f6b-176">**Host Name**</span></span>|<span data-ttu-id="65f6b-177">**Points to (Destination)**</span><span class="sxs-lookup"><span data-stu-id="65f6b-177">**Points to**</span></span>|<span data-ttu-id="65f6b-178">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="65f6b-178">**TTL**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="65f6b-179">autodiscover</span><span class="sxs-lookup"><span data-stu-id="65f6b-179">autodiscover</span></span>  <br/> |<span data-ttu-id="65f6b-180">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="65f6b-180">autodiscover.outlook.com</span></span>  <br/> |<span data-ttu-id="65f6b-181">1 Hour</span><span class="sxs-lookup"><span data-stu-id="65f6b-181">1 Hour</span></span>  <br/> |
|<span data-ttu-id="65f6b-182">sip</span><span class="sxs-lookup"><span data-stu-id="65f6b-182">sip</span></span>  <br/> |<span data-ttu-id="65f6b-183">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="65f6b-183">sipdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="65f6b-184">1 Hour</span><span class="sxs-lookup"><span data-stu-id="65f6b-184">1 Hour</span></span> <br/> |
|<span data-ttu-id="65f6b-185">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="65f6b-185">lyncdiscover</span></span>  <br/> |<span data-ttu-id="65f6b-186">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="65f6b-186">webdir.online.lync.com</span></span>   <br/> |<span data-ttu-id="65f6b-187">1 Hour</span><span class="sxs-lookup"><span data-stu-id="65f6b-187">1 Hour</span></span>  <br/> |
|<span data-ttu-id="65f6b-188">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="65f6b-188">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="65f6b-189">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="65f6b-189">enterpriseregistration.windows.net</span></span>  <br/> |<span data-ttu-id="65f6b-190">1 heure</span><span class="sxs-lookup"><span data-stu-id="65f6b-190">1 Hour</span></span> <br/> |
|<span data-ttu-id="65f6b-191">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="65f6b-191">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="65f6b-192">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="65f6b-192">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |<span data-ttu-id="65f6b-193">1 Hour</span><span class="sxs-lookup"><span data-stu-id="65f6b-193">1 Hour</span></span>  <br/> |
   
5. <span data-ttu-id="65f6b-194">Sélectionnez le bouton **enregistrer le DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="65f6b-194">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="65f6b-195">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="65f6b-195">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="65f6b-196">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="65f6b-196">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="65f6b-197"><a name="BKMK_spf"> </a></span><span class="sxs-lookup"><span data-stu-id="65f6b-197"><a name="BKMK_spf"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="65f6b-198">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="65f6b-198">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="65f6b-199">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="65f6b-199">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="65f6b-200">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="65f6b-200">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="65f6b-201">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="65f6b-201">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>  
  
1. <span data-ttu-id="65f6b-202">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="65f6b-202">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="65f6b-203">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="65f6b-203">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="65f6b-204">Sur la page **Mes domaines** , dans la zone **avancé** , sélectionnez le bouton **modifier le DNS** .</span><span class="sxs-lookup"><span data-stu-id="65f6b-204">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="65f6b-205">Sélectionnez **+ Ajouter un autre** dans la ligne **txt (texte)** de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="65f6b-205">Select **+ Add another** in the **TXT (Text)** row of the DNS editor.</span></span> 
    
4. <span data-ttu-id="65f6b-206">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="65f6b-206">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
|<span data-ttu-id="65f6b-207">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="65f6b-207">**Host Name**</span></span>|<span data-ttu-id="65f6b-208">**VALEUR TXT**</span><span class="sxs-lookup"><span data-stu-id="65f6b-208">**TXT Value**</span></span>|<span data-ttu-id="65f6b-209">**TTL**</span><span class="sxs-lookup"><span data-stu-id="65f6b-209">**TTL**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="65f6b-210">[Laissez ce champ vide]</span><span class="sxs-lookup"><span data-stu-id="65f6b-210">[leave this blank]</span></span>  <br/> |<span data-ttu-id="65f6b-211">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="65f6b-211">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="65f6b-212">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="65f6b-212">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span><br/> |<span data-ttu-id="65f6b-213">TXT</span><span class="sxs-lookup"><span data-stu-id="65f6b-213">TXT</span></span>  <br/> | <span data-ttu-id="65f6b-214">1 Hour</span><span class="sxs-lookup"><span data-stu-id="65f6b-214">1 Hour</span></span> |
   
5. <span data-ttu-id="65f6b-215">Sélectionnez le bouton **enregistrer le DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="65f6b-215">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="65f6b-216">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="65f6b-216">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="65f6b-217">Ajoutez les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="65f6b-217">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="65f6b-218"><a name="BKMK_srv"> </a></span><span class="sxs-lookup"><span data-stu-id="65f6b-218"><a name="BKMK_srv"> </a></span></span>

1. <span data-ttu-id="65f6b-219">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="65f6b-219">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="65f6b-220">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="65f6b-220">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="65f6b-221">Sur la page **Mes domaines** , dans la zone **avancé** , sélectionnez le bouton **modifier le DNS** .</span><span class="sxs-lookup"><span data-stu-id="65f6b-221">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="65f6b-222">Sélectionnez **+ Ajouter un autre** dans la ligne **SRV** de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="65f6b-222">Select **+ Add another** in the **SRV** row of the DNS editor.</span></span> 
    
4. <span data-ttu-id="65f6b-223">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="65f6b-223">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
|<span data-ttu-id="65f6b-224">**Service**</span><span class="sxs-lookup"><span data-stu-id="65f6b-224">**Service**</span></span>|<span data-ttu-id="65f6b-225">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="65f6b-225">**Protocol**</span></span>|<span data-ttu-id="65f6b-226">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="65f6b-226">**Name**</span></span>|<span data-ttu-id="65f6b-227">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="65f6b-227">**Weight**</span></span>|<span data-ttu-id="65f6b-228">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="65f6b-228">**Port**</span></span>|<span data-ttu-id="65f6b-229">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="65f6b-229">**Target**</span></span>|<span data-ttu-id="65f6b-230">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="65f6b-230">**Priority**</span></span>|<span data-ttu-id="65f6b-231">**TTL**</span><span class="sxs-lookup"><span data-stu-id="65f6b-231">**TTL**</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="65f6b-232">sip</span><span class="sxs-lookup"><span data-stu-id="65f6b-232">sip</span></span>  |<span data-ttu-id="65f6b-233">tls</span><span class="sxs-lookup"><span data-stu-id="65f6b-233">tls</span></span>  |<span data-ttu-id="65f6b-234">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="65f6b-234">Automatically populated</span></span> |<span data-ttu-id="65f6b-235">0,1</span><span class="sxs-lookup"><span data-stu-id="65f6b-235">1</span></span>  |<span data-ttu-id="65f6b-236">443</span><span class="sxs-lookup"><span data-stu-id="65f6b-236">443</span></span>   |<span data-ttu-id="65f6b-237">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="65f6b-237">sipdir.online.lync.com</span></span> |<span data-ttu-id="65f6b-238">100</span><span class="sxs-lookup"><span data-stu-id="65f6b-238">100</span></span> |<span data-ttu-id="65f6b-239">1 Hour</span><span class="sxs-lookup"><span data-stu-id="65f6b-239">1 Hour</span></span> |
|<span data-ttu-id="65f6b-240">sipfed</span><span class="sxs-lookup"><span data-stu-id="65f6b-240">sipfed</span></span>|<span data-ttu-id="65f6b-241">tcp</span><span class="sxs-lookup"><span data-stu-id="65f6b-241">tcp</span></span> |<span data-ttu-id="65f6b-242">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="65f6b-242">Automatically populated</span></span>|<span data-ttu-id="65f6b-243">0,1</span><span class="sxs-lookup"><span data-stu-id="65f6b-243">1</span></span> |<span data-ttu-id="65f6b-244">5061</span><span class="sxs-lookup"><span data-stu-id="65f6b-244">5061</span></span> |<span data-ttu-id="65f6b-245">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="65f6b-245">sipfed.online.lync.com</span></span>|<span data-ttu-id="65f6b-246">100</span><span class="sxs-lookup"><span data-stu-id="65f6b-246">100</span></span> | <span data-ttu-id="65f6b-247">1 Hour</span><span class="sxs-lookup"><span data-stu-id="65f6b-247">1 Hour</span></span> |
   
5. <span data-ttu-id="65f6b-248">Sélectionnez le bouton **enregistrer le DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="65f6b-248">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="65f6b-249">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="65f6b-249">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="65f6b-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="65f6b-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  

