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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 7173c635-58b3-400f-95e0-97abe915565e
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services chez WiX pour Microsoft.
ms.openlocfilehash: 2cbc4887f276e63f09b433225e09315c227c961c
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43629238"
---
# <a name="create-dns-records-at-wix-for-microsoft"></a><span data-ttu-id="6594f-103">Créer des enregistrements DNS auprès de WiX pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="6594f-103">Create DNS records at Wix for Microsoft</span></span>

 <span data-ttu-id="6594f-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="6594f-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="6594f-105">Si WiX est votre fournisseur d’hébergement DNS, suivez la procédure décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier électronique, Skype entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="6594f-105">If Wix is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="6594f-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="6594f-106">These are the main records to add.</span></span> 
  
- <span data-ttu-id="6594f-107">[Ajoutez un enregistrement txt à des fins de vérification](#add-a-txt-record-for-verification).</span><span class="sxs-lookup"><span data-stu-id="6594f-107">[Add a TXT record for verification](#add-a-txt-record-for-verification).</span></span>
    
- <span data-ttu-id="6594f-108">[Ajoutez un enregistrement MX afin que les messages électroniques pour votre domaine soient envoyés à Microsoft](#add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft).</span><span class="sxs-lookup"><span data-stu-id="6594f-108">[Add an MX record so email for your domain will come to Microsoft](#add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft).</span></span>
    
- <span data-ttu-id="6594f-109">[Ajoutez les cinq enregistrements CNAME requis pour Microsoft](#add-the-five-cname-records-that-are-required-for-microsoft).</span><span class="sxs-lookup"><span data-stu-id="6594f-109">[Add the five CNAME records that are required for Microsoft](#add-the-five-cname-records-that-are-required-for-microsoft).</span></span>
    
- <span data-ttu-id="6594f-110">[Ajoutez un enregistrement txt pour SPF afin d’éviter le courrier indésirable](#add-a-txt-record-for-spf-to-help-prevent-email-spam).</span><span class="sxs-lookup"><span data-stu-id="6594f-110">[Add a TXT record for SPF to help prevent email spam](#add-a-txt-record-for-spf-to-help-prevent-email-spam).</span></span>
    
- <span data-ttu-id="6594f-111">[Ajoutez les deux enregistrements SRV requis pour Microsoft](#add-the-two-srv-records-that-are-required-for-microsoft).</span><span class="sxs-lookup"><span data-stu-id="6594f-111">[Add the two SRV records that are required for Microsoft](#add-the-two-srv-records-that-are-required-for-microsoft).</span></span>
    
<span data-ttu-id="6594f-112">Une fois que vous avez ajouté ces enregistrements à WiX, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6594f-112">After you add these records at Wix, your domain will be set up to work with Microsoft services.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="6594f-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="6594f-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="6594f-116">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="6594f-116">Add a TXT record for verification</span></span>
<span data-ttu-id="6594f-117"><a name="BKMK_txt"> </a></span><span class="sxs-lookup"><span data-stu-id="6594f-117"><a name="BKMK_txt"> </a></span></span>

<span data-ttu-id="6594f-118">Avant d’utiliser votre domaine avec Microsoft, vous devez vous assurer que vous en êtes propriétaire.</span><span class="sxs-lookup"><span data-stu-id="6594f-118">Before you use your domain with Microsoft, we have to make sure that you own it.</span></span> <span data-ttu-id="6594f-119">Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="6594f-119">Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6594f-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="6594f-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="6594f-122">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="6594f-122">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="6594f-123">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="6594f-123">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="6594f-124">Sur la page **Mes domaines** , dans la zone **avancé** , sélectionnez le bouton **modifier le DNS** .</span><span class="sxs-lookup"><span data-stu-id="6594f-124">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="6594f-125">Sélectionnez **+ Ajouter un autre** dans la ligne **txt (texte)** de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="6594f-125">Select **+ Add another** in the **TXT (Text)** row of the DNS editor.</span></span> 
    
4. <span data-ttu-id="6594f-126">In the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="6594f-126">In the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="6594f-127">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="6594f-127">**Host Name**</span></span> <br/> |<span data-ttu-id="6594f-128">**VALEUR TXT**</span><span class="sxs-lookup"><span data-stu-id="6594f-128">**TXT Value**</span></span> <br/> |<span data-ttu-id="6594f-129">**TTL**</span><span class="sxs-lookup"><span data-stu-id="6594f-129">**TTL**</span></span> <br/> |
|<span data-ttu-id="6594f-130">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="6594f-130">Automatically populated</span></span>  <br/> |<span data-ttu-id="6594f-131">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="6594f-131">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="6594f-132">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="6594f-132">**Note:** This is an example.</span></span> <span data-ttu-id="6594f-133">Utilisez votre **adresse de destination ou de pointage** spécifique ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="6594f-133">Use your specific **Destination or Points to Address** value here, from the table.</span></span>  [<span data-ttu-id="6594f-134">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="6594f-134">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)|<span data-ttu-id="6594f-135">1 Hour</span><span class="sxs-lookup"><span data-stu-id="6594f-135">1 Hour</span></span> <br/> |          |
   
5. <span data-ttu-id="6594f-136">Sélectionnez le bouton **enregistrer le DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="6594f-136">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="6594f-137">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="6594f-137">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="6594f-138">À présent que vous avez ajouté l’enregistrement sur le site de votre bureau d’enregistrement de domaines, vous allez revenir à Microsoft et demander l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6594f-138">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="6594f-139">Lorsque Microsoft trouve l’enregistrement TXT correct, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="6594f-139">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="6594f-140">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="6594f-140">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="6594f-141">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="6594f-141">On the **Domains** page, select the domain that you are verifying.</span></span> 
  
  
3. <span data-ttu-id="6594f-142">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="6594f-142">On the **Setup** page, select **Start setup**.</span></span>
   
  
4. <span data-ttu-id="6594f-143">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="6594f-143">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="6594f-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="6594f-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="6594f-147">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient envoyés à Microsoft</span><span class="sxs-lookup"><span data-stu-id="6594f-147">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="6594f-148"><a name="BKMK_mx"> </a></span><span class="sxs-lookup"><span data-stu-id="6594f-148"><a name="BKMK_mx"> </a></span></span>

1. <span data-ttu-id="6594f-149">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="6594f-149">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="6594f-150">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="6594f-150">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="6594f-151">Sur la page **Mes domaines** , dans la zone **boîtes aux lettres** , sélectionnez le lien **configurer votre enregistrement MX** .</span><span class="sxs-lookup"><span data-stu-id="6594f-151">On the **My Domains** page, in the **Mailboxes** area, select the **Configure your MX records** link.</span></span> 
    
3. <span data-ttu-id="6594f-152">Sélectionnez **autre** dans la liste déroulante **votre fournisseur de messagerie** .</span><span class="sxs-lookup"><span data-stu-id="6594f-152">Choose **Other** from the **Your Email Provider** drop-down list.</span></span> 
    
4. <span data-ttu-id="6594f-153">Sélectionnez **+ Ajouter un autre**.</span><span class="sxs-lookup"><span data-stu-id="6594f-153">Select **+ Add another**.</span></span>
    
5. <span data-ttu-id="6594f-154">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="6594f-154">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
|<span data-ttu-id="6594f-155">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="6594f-155">**Host Name**</span></span>|<span data-ttu-id="6594f-156">**Points to (Pointe vers)**</span><span class="sxs-lookup"><span data-stu-id="6594f-156">**Points to**</span></span>|<span data-ttu-id="6594f-157">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="6594f-157">**Priority**</span></span>|<span data-ttu-id="6594f-158">**TTL**</span><span class="sxs-lookup"><span data-stu-id="6594f-158">**TTL**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6594f-159">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="6594f-159">Automatically populated</span></span> <br/> | <span data-ttu-id="6594f-160">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="6594f-160">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="6594f-161">**Remarque :** Obtenir votre \* \<clé\> de domaine\* à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6594f-161">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>   [<span data-ttu-id="6594f-162">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="6594f-162">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md) |<span data-ttu-id="6594f-163">0</span><span class="sxs-lookup"><span data-stu-id="6594f-163">0</span></span>  <br/> <span data-ttu-id="6594f-164">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/What-is-MX-priority-2784cc4d-95be-443d-b5f7-bb5dd867ba83).</span><span class="sxs-lookup"><span data-stu-id="6594f-164">For more information about priority, see [What is MX priority?](https://support.office.com/article/What-is-MX-priority-2784cc4d-95be-443d-b5f7-bb5dd867ba83)</span></span> | <span data-ttu-id="6594f-165">1 Hour</span><span class="sxs-lookup"><span data-stu-id="6594f-165">1 Hour</span></span>|
   
6. <span data-ttu-id="6594f-166">Si d’autres enregistrements MX sont répertoriés, supprimez-les chacun.</span><span class="sxs-lookup"><span data-stu-id="6594f-166">If there are any other MX records listed, delete each of them.</span></span> 
    
7. <span data-ttu-id="6594f-167">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="6594f-167">Select **OK**.</span></span>
    
8. <span data-ttu-id="6594f-168">Dans la boîte de dialogue de confirmation, sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="6594f-168">In the confirmation dialog box, select **OK**.</span></span>
    
## <a name="add-the-five-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="6594f-169">Ajouter les cinq enregistrements CNAMe requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="6594f-169">Add the five CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="6594f-170"><a name="BKMK_cname"> </a></span><span class="sxs-lookup"><span data-stu-id="6594f-170"><a name="BKMK_cname"> </a></span></span>

1. <span data-ttu-id="6594f-171">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="6594f-171">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="6594f-172">You'll be prompted to login first.</span><span class="sxs-lookup"><span data-stu-id="6594f-172">You'll be prompted to login first.</span></span>
    
2. <span data-ttu-id="6594f-173">Sur la page **Mes domaines** , dans la zone **avancé** , sélectionnez le bouton **modifier le DNS** .</span><span class="sxs-lookup"><span data-stu-id="6594f-173">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="6594f-174">Sélectionnez **+ Ajouter un autre** dans la ligne **CNAME (alias)** de l’éditeur DNS pour chaque enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="6594f-174">Select **+ Add another** in the **CNAME (Aliases)** row of the DNS editor for each CNAME record.</span></span> 
    
4. <span data-ttu-id="6594f-175">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="6594f-175">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
|<span data-ttu-id="6594f-176">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="6594f-176">**Host Name**</span></span>|<span data-ttu-id="6594f-177">**Points to (Destination)**</span><span class="sxs-lookup"><span data-stu-id="6594f-177">**Points to**</span></span>|<span data-ttu-id="6594f-178">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="6594f-178">**TTL**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6594f-179">autodiscover</span><span class="sxs-lookup"><span data-stu-id="6594f-179">autodiscover</span></span>  <br/> |<span data-ttu-id="6594f-180">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="6594f-180">autodiscover.outlook.com</span></span>  <br/> |<span data-ttu-id="6594f-181">1 Hour</span><span class="sxs-lookup"><span data-stu-id="6594f-181">1 Hour</span></span>  <br/> |
|<span data-ttu-id="6594f-182">sip</span><span class="sxs-lookup"><span data-stu-id="6594f-182">sip</span></span>  <br/> |<span data-ttu-id="6594f-183">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="6594f-183">sipdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="6594f-184">1 Hour</span><span class="sxs-lookup"><span data-stu-id="6594f-184">1 Hour</span></span> <br/> |
|<span data-ttu-id="6594f-185">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="6594f-185">lyncdiscover</span></span>  <br/> |<span data-ttu-id="6594f-186">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="6594f-186">webdir.online.lync.com</span></span>   <br/> |<span data-ttu-id="6594f-187">1 Hour</span><span class="sxs-lookup"><span data-stu-id="6594f-187">1 Hour</span></span>  <br/> |
|<span data-ttu-id="6594f-188">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="6594f-188">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="6594f-189">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="6594f-189">enterpriseregistration.windows.net</span></span>  <br/> |<span data-ttu-id="6594f-190">1 heure</span><span class="sxs-lookup"><span data-stu-id="6594f-190">1 Hour</span></span> <br/> |
|<span data-ttu-id="6594f-191">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="6594f-191">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="6594f-192">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="6594f-192">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |<span data-ttu-id="6594f-193">1 Hour</span><span class="sxs-lookup"><span data-stu-id="6594f-193">1 Hour</span></span>  <br/> |
   
5. <span data-ttu-id="6594f-194">Sélectionnez le bouton **enregistrer le DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="6594f-194">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="6594f-195">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="6594f-195">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="6594f-196">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="6594f-196">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="6594f-197"><a name="BKMK_spf"> </a></span><span class="sxs-lookup"><span data-stu-id="6594f-197"><a name="BKMK_spf"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="6594f-198">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="6594f-198">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="6594f-199">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="6594f-199">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="6594f-200">Si vous disposez déjà d’un enregistrement SPF pour votre domaine, n’en créez pas pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6594f-200">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="6594f-201">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="6594f-201">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>  
  
1. <span data-ttu-id="6594f-202">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="6594f-202">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="6594f-203">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="6594f-203">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="6594f-204">Sur la page **Mes domaines** , dans la zone **avancé** , sélectionnez le bouton **modifier le DNS** .</span><span class="sxs-lookup"><span data-stu-id="6594f-204">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="6594f-205">Sélectionnez **+ Ajouter un autre** dans la ligne **txt (texte)** de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="6594f-205">Select **+ Add another** in the **TXT (Text)** row of the DNS editor.</span></span> 
    
4. <span data-ttu-id="6594f-206">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="6594f-206">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
|<span data-ttu-id="6594f-207">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="6594f-207">**Host Name**</span></span>|<span data-ttu-id="6594f-208">**VALEUR TXT**</span><span class="sxs-lookup"><span data-stu-id="6594f-208">**TXT Value**</span></span>|<span data-ttu-id="6594f-209">**TTL**</span><span class="sxs-lookup"><span data-stu-id="6594f-209">**TTL**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6594f-210">[Laissez ce champ vide]</span><span class="sxs-lookup"><span data-stu-id="6594f-210">[leave this blank]</span></span>  <br/> |<span data-ttu-id="6594f-211">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="6594f-211">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="6594f-212">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="6594f-212">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span><br/> |<span data-ttu-id="6594f-213">TXT</span><span class="sxs-lookup"><span data-stu-id="6594f-213">TXT</span></span>  <br/> | <span data-ttu-id="6594f-214">1 Hour</span><span class="sxs-lookup"><span data-stu-id="6594f-214">1 Hour</span></span> |
   
5. <span data-ttu-id="6594f-215">Sélectionnez le bouton **enregistrer le DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="6594f-215">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="6594f-216">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="6594f-216">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="6594f-217">Ajouter les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="6594f-217">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="6594f-218"><a name="BKMK_srv"> </a></span><span class="sxs-lookup"><span data-stu-id="6594f-218"><a name="BKMK_srv"> </a></span></span>

1. <span data-ttu-id="6594f-219">Pour commencer, accédez à la page de vos domaines sur WiX en utilisant [ce lien](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span><span class="sxs-lookup"><span data-stu-id="6594f-219">To get started, go to your domains page at Wix by using [this link](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account).</span></span> <span data-ttu-id="6594f-220">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="6594f-220">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="6594f-221">Sur la page **Mes domaines** , dans la zone **avancé** , sélectionnez le bouton **modifier le DNS** .</span><span class="sxs-lookup"><span data-stu-id="6594f-221">On the **My Domains** page, in the **Advanced** area, select the **Edit DNS** button.</span></span> 
    
3. <span data-ttu-id="6594f-222">Sélectionnez **+ Ajouter un autre** dans la ligne **SRV** de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="6594f-222">Select **+ Add another** in the **SRV** row of the DNS editor.</span></span> 
    
4. <span data-ttu-id="6594f-223">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="6594f-223">In the boxes for the new record, type or copy and paste the values from the following table:</span></span>
    
|<span data-ttu-id="6594f-224">**Service**</span><span class="sxs-lookup"><span data-stu-id="6594f-224">**Service**</span></span>|<span data-ttu-id="6594f-225">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="6594f-225">**Protocol**</span></span>|<span data-ttu-id="6594f-226">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="6594f-226">**Name**</span></span>|<span data-ttu-id="6594f-227">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="6594f-227">**Weight**</span></span>|<span data-ttu-id="6594f-228">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="6594f-228">**Port**</span></span>|<span data-ttu-id="6594f-229">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="6594f-229">**Target**</span></span>|<span data-ttu-id="6594f-230">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="6594f-230">**Priority**</span></span>|<span data-ttu-id="6594f-231">**TTL**</span><span class="sxs-lookup"><span data-stu-id="6594f-231">**TTL**</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6594f-232">sip</span><span class="sxs-lookup"><span data-stu-id="6594f-232">sip</span></span>  |<span data-ttu-id="6594f-233">tls</span><span class="sxs-lookup"><span data-stu-id="6594f-233">tls</span></span>  |<span data-ttu-id="6594f-234">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="6594f-234">Automatically populated</span></span> |<span data-ttu-id="6594f-235">0,1</span><span class="sxs-lookup"><span data-stu-id="6594f-235">1</span></span>  |<span data-ttu-id="6594f-236">443</span><span class="sxs-lookup"><span data-stu-id="6594f-236">443</span></span>   |<span data-ttu-id="6594f-237">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="6594f-237">sipdir.online.lync.com</span></span> |<span data-ttu-id="6594f-238">100</span><span class="sxs-lookup"><span data-stu-id="6594f-238">100</span></span> |<span data-ttu-id="6594f-239">1 Hour</span><span class="sxs-lookup"><span data-stu-id="6594f-239">1 Hour</span></span> |
|<span data-ttu-id="6594f-240">sipfed</span><span class="sxs-lookup"><span data-stu-id="6594f-240">sipfed</span></span>|<span data-ttu-id="6594f-241">tcp</span><span class="sxs-lookup"><span data-stu-id="6594f-241">tcp</span></span> |<span data-ttu-id="6594f-242">Rempli automatiquement</span><span class="sxs-lookup"><span data-stu-id="6594f-242">Automatically populated</span></span>|<span data-ttu-id="6594f-243">0,1</span><span class="sxs-lookup"><span data-stu-id="6594f-243">1</span></span> |<span data-ttu-id="6594f-244">5061</span><span class="sxs-lookup"><span data-stu-id="6594f-244">5061</span></span> |<span data-ttu-id="6594f-245">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="6594f-245">sipfed.online.lync.com</span></span>|<span data-ttu-id="6594f-246">100</span><span class="sxs-lookup"><span data-stu-id="6594f-246">100</span></span> | <span data-ttu-id="6594f-247">1 Hour</span><span class="sxs-lookup"><span data-stu-id="6594f-247">1 Hour</span></span> |
   
5. <span data-ttu-id="6594f-248">Sélectionnez le bouton **enregistrer le DNS** en haut de l’éditeur DNS.</span><span class="sxs-lookup"><span data-stu-id="6594f-248">Select the **Save DNS** button at the top of the DNS editor.</span></span> 
    
6. <span data-ttu-id="6594f-249">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="6594f-249">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="6594f-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="6594f-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  

