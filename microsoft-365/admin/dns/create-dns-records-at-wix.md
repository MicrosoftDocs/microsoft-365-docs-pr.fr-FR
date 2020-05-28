---
title: Créer des enregistrements DNS auprès de WiX pour Microsoft
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
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 7173c635-58b3-400f-95e0-97abe915565e
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services chez WiX pour Microsoft.
ms.openlocfilehash: b5fe216e65954bbcbdd9a1da223258a8362743ca
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44400291"
---
# <a name="create-dns-records-at-wix-for-microsoft"></a><span data-ttu-id="ee0f0-103">Créer des enregistrements DNS auprès de WiX pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="ee0f0-103">Create DNS records at Wix for Microsoft</span></span>

 <span data-ttu-id="ee0f0-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="ee0f0-105">Si WiX est votre fournisseur d’hébergement DNS, suivez la procédure décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier électronique, Skype entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-105">If Wix is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="ee0f0-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-106">These are the main records to add.</span></span> 
  
- <span data-ttu-id="ee0f0-107">[Ajoutez un enregistrement txt à des fins de vérification](#add-a-txt-record-for-verification).</span><span class="sxs-lookup"><span data-stu-id="ee0f0-107">[Add a TXT record for verification](#add-a-txt-record-for-verification).</span></span>
    
- <span data-ttu-id="ee0f0-108">[Ajoutez un enregistrement MX afin que les messages électroniques pour votre domaine soient envoyés à Microsoft](#add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft).</span><span class="sxs-lookup"><span data-stu-id="ee0f0-108">[Add an MX record so email for your domain will come to Microsoft](#add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft).</span></span>
    
- <span data-ttu-id="ee0f0-109">[Ajoutez les cinq enregistrements CNAME requis pour Microsoft](#add-the-five-cname-records-that-are-required-for-microsoft).</span><span class="sxs-lookup"><span data-stu-id="ee0f0-109">[Add the five CNAME records that are required for Microsoft](#add-the-five-cname-records-that-are-required-for-microsoft).</span></span>
    
- <span data-ttu-id="ee0f0-110">[Ajoutez un enregistrement txt pour SPF afin d’éviter le courrier indésirable](#add-a-txt-record-for-spf-to-help-prevent-email-spam).</span><span class="sxs-lookup"><span data-stu-id="ee0f0-110">[Add a TXT record for SPF to help prevent email spam](#add-a-txt-record-for-spf-to-help-prevent-email-spam).</span></span>
    
- <span data-ttu-id="ee0f0-111">[Ajoutez les deux enregistrements SRV requis pour Microsoft](#add-the-two-srv-records-that-are-required-for-microsoft).</span><span class="sxs-lookup"><span data-stu-id="ee0f0-111">[Add the two SRV records that are required for Microsoft](#add-the-two-srv-records-that-are-required-for-microsoft).</span></span>
    
<span data-ttu-id="ee0f0-112">Une fois que vous avez ajouté ces enregistrements à WiX, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-112">After you add these records at Wix, your domain will be set up to work with Microsoft services.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="ee0f0-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ee0f0-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="ee0f0-116">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="ee0f0-116">Add a TXT record for verification</span></span>
<span data-ttu-id="ee0f0-117"><a name="BKMK_txt"> </a></span><span class="sxs-lookup"><span data-stu-id="ee0f0-117"><a name="BKMK_txt"> </a></span></span>

<span data-ttu-id="ee0f0-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ee0f0-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="ee0f0-122">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="ee0f0-122">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="ee0f0-123">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-123">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="ee0f0-124">Sur la page **Mes domaines** , dans la zone **avancé** , sélectionnez le bouton **modifier le DNS** .</span><span class="sxs-lookup"><span data-stu-id="ee0f0-124">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="ee0f0-125">Sélectionnez **+ Ajouter un autre** dans la ligne **txt (texte)** de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-125">Select **+ Add another** in the **TXT (Text)** row of the DNS editor.</span></span> 
    
4. <span data-ttu-id="ee0f0-126">In the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-126">In the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="ee0f0-127">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-127">**Host Name**</span></span> <br/> |<span data-ttu-id="ee0f0-128">**VALEUR TXT**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-128">**TXT Value**</span></span> <br/> |<span data-ttu-id="ee0f0-129">**TTL**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-129">**TTL**</span></span> <br/> |
|<span data-ttu-id="ee0f0-130">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="ee0f0-130">Automatically populated</span></span>  <br/> |<span data-ttu-id="ee0f0-131">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="ee0f0-131">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="ee0f0-132">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-132">**Note:** This is an example.</span></span> <span data-ttu-id="ee0f0-133">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-133">Use your specific **Destination or Points to Address** value here, from the table.</span></span>  [<span data-ttu-id="ee0f0-134">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="ee0f0-134">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)|<span data-ttu-id="ee0f0-135">1 Hour</span><span class="sxs-lookup"><span data-stu-id="ee0f0-135">1 Hour</span></span> <br/> |          |
   
5. <span data-ttu-id="ee0f0-136">Sélectionnez le bouton **enregistrer le DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-136">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="ee0f0-137">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-137">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="ee0f0-138">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-138">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="ee0f0-139">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-139">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="ee0f0-140">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-140">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="ee0f0-141">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-141">On the **Domains** page, select the domain that you are verifying.</span></span> 
  
  
3. <span data-ttu-id="ee0f0-142">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-142">On the **Setup** page, select **Start setup**.</span></span>
   
  
4. <span data-ttu-id="ee0f0-143">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-143">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="ee0f0-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ee0f0-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="ee0f0-147">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="ee0f0-147">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="ee0f0-148"><a name="BKMK_mx"> </a></span><span class="sxs-lookup"><span data-stu-id="ee0f0-148"><a name="BKMK_mx"> </a></span></span>

1. <span data-ttu-id="ee0f0-149">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="ee0f0-149">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="ee0f0-150">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-150">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="ee0f0-151">Sur la page **Mes domaines** , dans la zone **boîtes aux lettres** , sélectionnez le lien **configurer votre enregistrement MX** .</span><span class="sxs-lookup"><span data-stu-id="ee0f0-151">On the **My Domains** page, in the **Mailboxes** area, select the **Configure your MX records** link.</span></span> 
    
3. <span data-ttu-id="ee0f0-152">Sélectionnez **autre** dans la liste déroulante **votre fournisseur de messagerie** .</span><span class="sxs-lookup"><span data-stu-id="ee0f0-152">Choose **Other** from the **Your Email Provider** drop-down list.</span></span> 
    
4. <span data-ttu-id="ee0f0-153">Sélectionnez **+ Ajouter un autre**.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-153">Select **+ Add another**.</span></span>
    
5. <span data-ttu-id="ee0f0-154">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="ee0f0-154">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
|<span data-ttu-id="ee0f0-155">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-155">**Host Name**</span></span>|<span data-ttu-id="ee0f0-156">**Points to (Pointe vers)**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-156">**Points to**</span></span>|<span data-ttu-id="ee0f0-157">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-157">**Priority**</span></span>|<span data-ttu-id="ee0f0-158">**TTL**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-158">**TTL**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ee0f0-159">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="ee0f0-159">Automatically populated</span></span> <br/> | <span data-ttu-id="ee0f0-160">*\<domain-key\>*. mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="ee0f0-160">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="ee0f0-161">**Remarque :** Obtenir votre *\<domain-key\>* à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-161">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>   [<span data-ttu-id="ee0f0-162">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="ee0f0-162">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md) |<span data-ttu-id="ee0f0-163">0</span><span class="sxs-lookup"><span data-stu-id="ee0f0-163">0</span></span>  <br/> <span data-ttu-id="ee0f0-164">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span><span class="sxs-lookup"><span data-stu-id="ee0f0-164">For more information about priority, see [What is MX priority?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span></span> | <span data-ttu-id="ee0f0-165">1 Hour</span><span class="sxs-lookup"><span data-stu-id="ee0f0-165">1 Hour</span></span>|
   
6. <span data-ttu-id="ee0f0-166">Si d’autres enregistrements MX sont répertoriés, supprimez-les chacun.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-166">If there are any other MX records listed, delete each of them.</span></span> 
    
7. <span data-ttu-id="ee0f0-167">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-167">Select **OK**.</span></span>
    
8. <span data-ttu-id="ee0f0-168">Dans la boîte de dialogue de confirmation, sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-168">In the confirmation dialog box, select **OK**.</span></span>
    
## <a name="add-the-five-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="ee0f0-169">Ajouter les cinq enregistrements CNAMe requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="ee0f0-169">Add the five CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="ee0f0-170"><a name="BKMK_cname"> </a></span><span class="sxs-lookup"><span data-stu-id="ee0f0-170"><a name="BKMK_cname"> </a></span></span>

1. <span data-ttu-id="ee0f0-171">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="ee0f0-171">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="ee0f0-172">You'll be prompted to login first.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-172">You'll be prompted to login first.</span></span>
    
2. <span data-ttu-id="ee0f0-173">Sur la page **Mes domaines** , dans la zone **avancé** , sélectionnez le bouton **modifier le DNS** .</span><span class="sxs-lookup"><span data-stu-id="ee0f0-173">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="ee0f0-174">Sélectionnez **+ Ajouter un autre** dans la ligne **CNAME (alias)** de l’éditeur DNS pour chaque enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-174">Select **+ Add another** in the **CNAME (Aliases)** row of the DNS editor for each CNAME record.</span></span> 
    
4. <span data-ttu-id="ee0f0-175">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="ee0f0-175">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
|<span data-ttu-id="ee0f0-176">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-176">**Host Name**</span></span>|<span data-ttu-id="ee0f0-177">**Points to (Destination)**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-177">**Points to**</span></span>|<span data-ttu-id="ee0f0-178">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-178">**TTL**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ee0f0-179">autodiscover</span><span class="sxs-lookup"><span data-stu-id="ee0f0-179">autodiscover</span></span>  <br/> |<span data-ttu-id="ee0f0-180">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="ee0f0-180">autodiscover.outlook.com</span></span>  <br/> |<span data-ttu-id="ee0f0-181">1 Hour</span><span class="sxs-lookup"><span data-stu-id="ee0f0-181">1 Hour</span></span>  <br/> |
|<span data-ttu-id="ee0f0-182">sip</span><span class="sxs-lookup"><span data-stu-id="ee0f0-182">sip</span></span>  <br/> |<span data-ttu-id="ee0f0-183">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="ee0f0-183">sipdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="ee0f0-184">1 Hour</span><span class="sxs-lookup"><span data-stu-id="ee0f0-184">1 Hour</span></span> <br/> |
|<span data-ttu-id="ee0f0-185">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="ee0f0-185">lyncdiscover</span></span>  <br/> |<span data-ttu-id="ee0f0-186">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="ee0f0-186">webdir.online.lync.com</span></span>   <br/> |<span data-ttu-id="ee0f0-187">1 Hour</span><span class="sxs-lookup"><span data-stu-id="ee0f0-187">1 Hour</span></span>  <br/> |
|<span data-ttu-id="ee0f0-188">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="ee0f0-188">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="ee0f0-189">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="ee0f0-189">enterpriseregistration.windows.net</span></span>  <br/> |<span data-ttu-id="ee0f0-190">1 heure</span><span class="sxs-lookup"><span data-stu-id="ee0f0-190">1 Hour</span></span> <br/> |
|<span data-ttu-id="ee0f0-191">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="ee0f0-191">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="ee0f0-192">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="ee0f0-192">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |<span data-ttu-id="ee0f0-193">1 Hour</span><span class="sxs-lookup"><span data-stu-id="ee0f0-193">1 Hour</span></span>  <br/> |
   
5. <span data-ttu-id="ee0f0-194">Sélectionnez le bouton **enregistrer le DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-194">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="ee0f0-195">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-195">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="ee0f0-196">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="ee0f0-196">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="ee0f0-197"><a name="BKMK_spf"> </a></span><span class="sxs-lookup"><span data-stu-id="ee0f0-197"><a name="BKMK_spf"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee0f0-198">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-198">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="ee0f0-199">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-199">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="ee0f0-200">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-200">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="ee0f0-201">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-201">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>  
  
1. <span data-ttu-id="ee0f0-202">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="ee0f0-202">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="ee0f0-203">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-203">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="ee0f0-204">Sur la page **Mes domaines** , dans la zone **avancé** , sélectionnez le bouton **modifier le DNS** .</span><span class="sxs-lookup"><span data-stu-id="ee0f0-204">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="ee0f0-205">Sélectionnez **+ Ajouter un autre** dans la ligne **txt (texte)** de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-205">Select **+ Add another** in the **TXT (Text)** row of the DNS editor.</span></span> 
    
4. <span data-ttu-id="ee0f0-206">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="ee0f0-206">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
|<span data-ttu-id="ee0f0-207">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-207">**Host Name**</span></span>|<span data-ttu-id="ee0f0-208">**VALEUR TXT**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-208">**TXT Value**</span></span>|<span data-ttu-id="ee0f0-209">**TTL**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-209">**TTL**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ee0f0-210">[Laissez ce champ vide]</span><span class="sxs-lookup"><span data-stu-id="ee0f0-210">[leave this blank]</span></span>  <br/> |<span data-ttu-id="ee0f0-211">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="ee0f0-211">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="ee0f0-212">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-212">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span><br/> |<span data-ttu-id="ee0f0-213">TXT</span><span class="sxs-lookup"><span data-stu-id="ee0f0-213">TXT</span></span>  <br/> | <span data-ttu-id="ee0f0-214">1 Hour</span><span class="sxs-lookup"><span data-stu-id="ee0f0-214">1 Hour</span></span> |
   
5. <span data-ttu-id="ee0f0-215">Sélectionnez le bouton **enregistrer le DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-215">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="ee0f0-216">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-216">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="ee0f0-217">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="ee0f0-217">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="ee0f0-218"><a name="BKMK_srv"> </a></span><span class="sxs-lookup"><span data-stu-id="ee0f0-218"><a name="BKMK_srv"> </a></span></span>

1. <span data-ttu-id="ee0f0-219">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="ee0f0-219">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="ee0f0-220">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-220">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="ee0f0-221">Sur la page **Mes domaines** , dans la zone **avancé** , sélectionnez le bouton **modifier le DNS** .</span><span class="sxs-lookup"><span data-stu-id="ee0f0-221">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="ee0f0-222">Sélectionnez **+ Ajouter un autre** dans la ligne **SRV** de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-222">Select **+ Add another** in the **SRV** row of the DNS editor.</span></span> 
    
4. <span data-ttu-id="ee0f0-223">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="ee0f0-223">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
|<span data-ttu-id="ee0f0-224">**Service**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-224">**Service**</span></span>|<span data-ttu-id="ee0f0-225">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-225">**Protocol**</span></span>|<span data-ttu-id="ee0f0-226">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-226">**Name**</span></span>|<span data-ttu-id="ee0f0-227">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-227">**Weight**</span></span>|<span data-ttu-id="ee0f0-228">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-228">**Port**</span></span>|<span data-ttu-id="ee0f0-229">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-229">**Target**</span></span>|<span data-ttu-id="ee0f0-230">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-230">**Priority**</span></span>|<span data-ttu-id="ee0f0-231">**TTL**</span><span class="sxs-lookup"><span data-stu-id="ee0f0-231">**TTL**</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ee0f0-232">sip</span><span class="sxs-lookup"><span data-stu-id="ee0f0-232">sip</span></span>  |<span data-ttu-id="ee0f0-233">tls</span><span class="sxs-lookup"><span data-stu-id="ee0f0-233">tls</span></span>  |<span data-ttu-id="ee0f0-234">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="ee0f0-234">Automatically populated</span></span> |<span data-ttu-id="ee0f0-235">1 </span><span class="sxs-lookup"><span data-stu-id="ee0f0-235">1</span></span>  |<span data-ttu-id="ee0f0-236">443</span><span class="sxs-lookup"><span data-stu-id="ee0f0-236">443</span></span>   |<span data-ttu-id="ee0f0-237">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="ee0f0-237">sipdir.online.lync.com</span></span> |<span data-ttu-id="ee0f0-238">100</span><span class="sxs-lookup"><span data-stu-id="ee0f0-238">100</span></span> |<span data-ttu-id="ee0f0-239">1 Hour</span><span class="sxs-lookup"><span data-stu-id="ee0f0-239">1 Hour</span></span> |
|<span data-ttu-id="ee0f0-240">sipfed</span><span class="sxs-lookup"><span data-stu-id="ee0f0-240">sipfed</span></span>|<span data-ttu-id="ee0f0-241">tcp</span><span class="sxs-lookup"><span data-stu-id="ee0f0-241">tcp</span></span> |<span data-ttu-id="ee0f0-242">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="ee0f0-242">Automatically populated</span></span>|<span data-ttu-id="ee0f0-243">1 </span><span class="sxs-lookup"><span data-stu-id="ee0f0-243">1</span></span> |<span data-ttu-id="ee0f0-244">5061</span><span class="sxs-lookup"><span data-stu-id="ee0f0-244">5061</span></span> |<span data-ttu-id="ee0f0-245">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="ee0f0-245">sipfed.online.lync.com</span></span>|<span data-ttu-id="ee0f0-246">100</span><span class="sxs-lookup"><span data-stu-id="ee0f0-246">100</span></span> | <span data-ttu-id="ee0f0-247">1 Hour</span><span class="sxs-lookup"><span data-stu-id="ee0f0-247">1 Hour</span></span> |
   
5. <span data-ttu-id="ee0f0-248">Sélectionnez le bouton **enregistrer le DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-248">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="ee0f0-249">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="ee0f0-249">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="ee0f0-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ee0f0-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  

