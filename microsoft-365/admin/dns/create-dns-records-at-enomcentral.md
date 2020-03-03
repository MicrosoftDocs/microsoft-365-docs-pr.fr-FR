---
title: Créer des enregistrements DNS auprès de eNomCentral pour Office 365
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
ms.assetid: a6626053-a9c8-445b-81ee-eeb6672fae77
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur auprès enomcentral pour Office 365.
ms.openlocfilehash: dec76e0dde2775851ff464e3b8765f82dfb57625
ms.sourcegitcommit: 812aab5f58eed4bf359faf0e99f7f876af5b1023
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/02/2020
ms.locfileid: "42350465"
---
# <a name="create-dns-records-at-enomcentral-for-office-365"></a><span data-ttu-id="ed6bc-103">Créer des enregistrements DNS auprès de eNomCentral pour Office 365</span><span class="sxs-lookup"><span data-stu-id="ed6bc-103">Create DNS records at eNomCentral for Office 365</span></span>

 <span data-ttu-id="ed6bc-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="ed6bc-105">Si eNomCentral est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-105">If eNomCentral is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="ed6bc-106">Une fois ces enregistrements ajoutés sur eNomCentral, votre domaine est configuré pour utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-106">After you add these records at eNomCentral, your domain will be set up to work with Office 365 services.</span></span>
  
<span data-ttu-id="ed6bc-107">Pour en savoir plus sur l'hébergement web et le DNS pour les sites web avec Office 365, voir [Utiliser un site web public avec Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span><span class="sxs-lookup"><span data-stu-id="ed6bc-107">To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="ed6bc-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ed6bc-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="ed6bc-111">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="ed6bc-111">Add a TXT record for verification</span></span>
<span data-ttu-id="ed6bc-112"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="ed6bc-112"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="ed6bc-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ed6bc-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
<span data-ttu-id="ed6bc-117">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 0:46)](https://support.office.com/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="ed6bc-117">Follow the steps below or [watch the video (start at 0:46)](https://support.office.com/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="ed6bc-p104">Pour commencer, accédez à la page de vos domaines sur le site eNom Central en utilisant [ce lien](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-p104">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). You'll be prompted to login.</span></span>
    
    ![eNom-BP-configure-1-1](../../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. <span data-ttu-id="ed6bc-121">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-121">Under **my domains**, select the name of the domain that you want to edit.</span></span>
    
    ![eNom-BP-configure-1-2](../../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. <span data-ttu-id="ed6bc-123">Dans la liste déroulante **Manage Domain (Gérer le domaine)**, sélectionnez **Host Records (Enregistrements d'hôtes)**.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-123">On the **Manage Domain** drop-down list, choose **Host Records**.</span></span>
    
    ![eNom-BP-Verify-1-1](../../media/6e4184a1-9525-47a6-8a8a-9600126c0db4.png)
  
4. <span data-ttu-id="ed6bc-125">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-125">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="ed6bc-126">(Choose the **Record Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="ed6bc-126">(Choose the **Record Type** value from the drop-down list.)</span></span> 
    
    ||||
    |:-----|:-----|:-----|
    |<span data-ttu-id="ed6bc-127">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-127">**Host Name**</span></span> <br/> |<span data-ttu-id="ed6bc-128">**Record Type**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-128">**Record Type**</span></span> <br/> |<span data-ttu-id="ed6bc-129">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-129">**Address**</span></span> <br/> |
    |@  <br/> |<span data-ttu-id="ed6bc-130">TXT</span><span class="sxs-lookup"><span data-stu-id="ed6bc-130">TXT</span></span>  <br/> |<span data-ttu-id="ed6bc-131">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="ed6bc-131">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="ed6bc-132">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-132">**Note:** This is an example.</span></span> <span data-ttu-id="ed6bc-133">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-133">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span>           [<span data-ttu-id="ed6bc-134">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="ed6bc-134">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
       
   ![eNom-BP-Verify-1-2](../../media/e1f95529-46a6-40f9-9709-9fe66f373bcf.png)
  
5. <span data-ttu-id="ed6bc-136">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-136">Select **save**.</span></span>
    
    ![eNom-BP-Verify-1-3](../../media/d6277ab0-5d03-44e0-968f-fd5de1905423.png)
  
6. <span data-ttu-id="ed6bc-138">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-138">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="ed6bc-139">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Office 365 et demandez à Office 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-139">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="ed6bc-140">Lorsqu’Office 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-140">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="ed6bc-141">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-141">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="ed6bc-142">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-142">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="ed6bc-143">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-143">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="ed6bc-144">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-144">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="ed6bc-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ed6bc-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="ed6bc-148">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="ed6bc-148">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="ed6bc-149"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="ed6bc-149"><a name="BKMK_add_MX"> </a></span></span>

<span data-ttu-id="ed6bc-150">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 3:40)](https://support.office.com/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="ed6bc-150">Follow the steps below or [watch the video (start at 3:40)](https://support.office.com/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="ed6bc-p107">Pour commencer, accédez à la page de vos domaines sur le site eNom Central en utilisant [ce lien](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-p107">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). You'll be prompted to login.</span></span>
    
    ![eNom-BP-configure-1-1](../../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. <span data-ttu-id="ed6bc-154">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-154">Under **my domains**, select the name of the domain that you want to edit.</span></span>
    
    ![eNom-BP-configure-1-2](../../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. <span data-ttu-id="ed6bc-156">Dans la liste déroulante **Manage Domain (Gérer le domaine)**, sélectionnez **Email Settings (Paramètres de courrier)**.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-156">On the **Manage Domain** drop-down list, choose **Email Settings**.</span></span>
    
    ![eNom-BP-configure-1-3](../../media/4b438629-afdf-4a47-ab11-56644cdb6158.png)
  
4. <span data-ttu-id="ed6bc-158">Dans le menu déroulant **Service Selection (Sélection du service)**, choisissez **User (MX) (Utilisateur (MX))**.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-158">On the **Service Selection** drop-down list, choose **User (MX)**.</span></span>
    
    ![eNom-BP-configure-1-4](../../media/7680ab48-b8d1-4573-b20f-4745a5d7c079.png)
  
5. <span data-ttu-id="ed6bc-160">In the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-160">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="ed6bc-161">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-161">**Host Name**</span></span>|<span data-ttu-id="ed6bc-162">**Address**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-162">**Address**</span></span>|<span data-ttu-id="ed6bc-163">**Pref (Préference)**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-163">**Pref**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> | <span data-ttu-id="ed6bc-164">*\<clé_de_domaine\>*  .mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-164">*\<domain-key\>*  .mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="ed6bc-165">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-165">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="ed6bc-166">**Remarque :** Obtenez votre \* \<clé\> de domaine\* à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-166">**Note:** Get your  *\<domain-key\>*  from your Office 365 account.</span></span>           [<span data-ttu-id="ed6bc-167">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="ed6bc-167">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="ed6bc-168">10 </span><span class="sxs-lookup"><span data-stu-id="ed6bc-168">10</span></span>  <br/> <span data-ttu-id="ed6bc-169">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="ed6bc-169">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> |
       
   ![eNom-BP-configure-2-1](../../media/c32e8954-8209-4f77-a3a8-4b7aeea325d5.png)
  
6. <span data-ttu-id="ed6bc-171">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-171">Select **save**.</span></span>
    
    ![eNom-BP-configure-2-2](../../media/cf3058ea-9d30-4747-8cf0-2bc13d5ec6be.png)
  
7. <span data-ttu-id="ed6bc-173">Si d'autres enregistrements MX sont répertoriés, activez les cases à cocher correspondantes pour les sélectionner.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-173">If there are any other existing MX records, select the check boxes for those records to select them.</span></span>
    
    ![eNom-BP-configure-2-3](../../media/5017ed03-ca76-4c5c-93a7-84ffe24125dc.png)
  
8. <span data-ttu-id="ed6bc-175">Sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-175">Select **delete checked**.</span></span>
    
    ![eNom-BP-configure-2-4](../../media/072dc039-bddb-4c1f-bb44-5660e77f14b0.png)
  
## <a name="add-the-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="ed6bc-177">Ajouter les enregistrements CNAME requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="ed6bc-177">Add the CNAME records that are required for Office 365</span></span>
<span data-ttu-id="ed6bc-178"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="ed6bc-178"><a name="BKMK_add_CNAME"> </a></span></span>

<span data-ttu-id="ed6bc-179">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 4:24)](https://support.office.com/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="ed6bc-179">Follow the steps below or [watch the video (start at 4:24)](https://support.office.com/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="ed6bc-p109">Pour commencer, accédez à la page de vos domaines sur le site eNom Central en utilisant [ce lien](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-p109">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). You'll be prompted to login.</span></span>
    
    ![eNom-BP-configure-1-1](../../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. <span data-ttu-id="ed6bc-183">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-183">Under **my domains**, select the name of the domain that you want to edit.</span></span>
    
    ![eNom-BP-configure-1-2](../../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. <span data-ttu-id="ed6bc-185">Dans la liste déroulante **Manage Domain (Gérer le domaine)**, sélectionnez **Host Records (Enregistrements d'hôtes)**.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-185">On the **Manage Domain** drop-down list, choose **Host Records**.</span></span>
    
    ![eNom-BP-configure-1-5](../../media/c92c514c-8166-4cba-97e3-ee1d9847d255.png)
  
4. <span data-ttu-id="ed6bc-187">Sélectionnez **nouvelle ligne**.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-187">Select **new row**.</span></span>
    
    ![eNom-BP-configure-3-1](../../media/a30f0a88-7b09-411e-9133-e7965bcf1de0.png)
  
5. <span data-ttu-id="ed6bc-189">Dans les zones des six nouveaux enregistrements, tapez ou copiez-collez les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-189">In the boxes for the six new records, type or copy and paste the following values.</span></span>
    
        (Choose the **Record Type** value from the drop-down list.) 
        
    |<span data-ttu-id="ed6bc-190">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-190">**Host Name**</span></span>|<span data-ttu-id="ed6bc-191">**Record Type**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-191">**Record Type**</span></span>|<span data-ttu-id="ed6bc-192">**Address (Adresse)**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-192">**Address**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="ed6bc-193">autodiscover</span><span class="sxs-lookup"><span data-stu-id="ed6bc-193">autodiscover</span></span>  <br/> |<span data-ttu-id="ed6bc-194">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="ed6bc-194">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="ed6bc-195">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-195">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="ed6bc-196">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-196">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="ed6bc-197">sip</span><span class="sxs-lookup"><span data-stu-id="ed6bc-197">sip</span></span>  <br/> |<span data-ttu-id="ed6bc-198">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="ed6bc-198">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="ed6bc-199">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-199">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="ed6bc-200">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-200">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="ed6bc-201">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="ed6bc-201">lyncdiscover</span></span>  <br/> |<span data-ttu-id="ed6bc-202">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="ed6bc-202">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="ed6bc-203">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-203">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="ed6bc-204">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-204">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="ed6bc-205">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="ed6bc-205">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="ed6bc-206">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="ed6bc-206">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="ed6bc-207">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-207">enterpriseregistration.windows.net.</span></span>  <br/> <span data-ttu-id="ed6bc-208">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-208">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="ed6bc-209">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="ed6bc-209">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="ed6bc-210">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="ed6bc-210">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="ed6bc-211">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-211">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> <span data-ttu-id="ed6bc-212">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-212">**This value MUST end with a period (.)**</span></span> <br/> |
   
    ![eNom-BP-configure-3-2](../../media/672371c0-51af-44ba-bb18-80286b7676c1.png)
  
6. <span data-ttu-id="ed6bc-214">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-214">Select **save**.</span></span>
    
    ![eNom-BP-configure-3-3](../../media/027b57ce-5699-408b-993b-e46a9ac31090.png)
  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="ed6bc-216">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="ed6bc-216">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="ed6bc-217"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="ed6bc-217"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed6bc-218">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-218">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="ed6bc-219">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-219">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="ed6bc-220">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-220">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="ed6bc-221">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-221">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>
  
<span data-ttu-id="ed6bc-222">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 5:12)](https://support.office.com/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="ed6bc-222">Follow the steps below or [watch the video (start at 5:12)](https://support.office.com/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="ed6bc-p111">Pour commencer, accédez à la page de vos domaines sur le site eNom Central en utilisant [ce lien](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-p111">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). You'll be prompted to login.</span></span>
    
    ![eNom-BP-configure-1-1](../../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. <span data-ttu-id="ed6bc-226">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-226">Under **my domains**, select the name of the domain that you want to edit.</span></span>
    
    ![eNom-BP-configure-1-2](../../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. <span data-ttu-id="ed6bc-228">Dans la liste déroulante **Manage Domain (Gérer le domaine)**, sélectionnez **Host Records (Enregistrements d'hôtes)**.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-228">On the **Manage Domain** drop-down list, choose **Host Records**.</span></span>
    
    ![eNom-BP-configure-1-5](../../media/c92c514c-8166-4cba-97e3-ee1d9847d255.png)
  
4. <span data-ttu-id="ed6bc-230">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-230">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="ed6bc-231">(Choose the **Record Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="ed6bc-231">(Choose the **Record Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="ed6bc-232">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-232">**Host Name**</span></span>|<span data-ttu-id="ed6bc-233">**Record Type**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-233">**Record Type**</span></span>|<span data-ttu-id="ed6bc-234">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-234">**Address**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="ed6bc-235">TXT</span><span class="sxs-lookup"><span data-stu-id="ed6bc-235">TXT</span></span>  <br/> |<span data-ttu-id="ed6bc-236">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="ed6bc-236">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/><span data-ttu-id="ed6bc-237">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-237">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
   ![eNom-BP-configure-4-1](../../media/64c68697-258d-4044-84b1-c28f4a402e3b.png)
  
5. <span data-ttu-id="ed6bc-239">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-239">Select **save**.</span></span>
    
    ![eNom-BP-configure-4-2](../../media/89f4effa-349e-4734-96a5-cd80b0cecd60.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="ed6bc-241">Ajoutez les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="ed6bc-241">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="ed6bc-242"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="ed6bc-242"><a name="BKMK_add_SRV"> </a></span></span>

<span data-ttu-id="ed6bc-243">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 5:50)](https://support.office.com/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="ed6bc-243">Follow the steps below or [watch the video (start at 5:50)](https://support.office.com/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="ed6bc-p112">Pour commencer, accédez à la page de vos domaines sur le site eNom Central en utilisant [ce lien](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-p112">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). You'll be prompted to login.</span></span>
    
    ![eNom-BP-configure-1-1](../../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. <span data-ttu-id="ed6bc-247">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-247">Under **my domains**, select the name of the domain that you want to edit.</span></span>
    
    ![eNom-BP-configure-1-2](../../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. <span data-ttu-id="ed6bc-249">Dans la liste déroulante **Manage Domain (Gérer le domaine)**, sélectionnez **Host Records (Enregistrements d'hôtes)**.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-249">On the **Manage Domain** drop-down list, choose **Host Records**.</span></span>
    
    ![eNom-BP-configure-1-5](../../media/c92c514c-8166-4cba-97e3-ee1d9847d255.png)
  
4. <span data-ttu-id="ed6bc-251">À droite de **nouvelle ligne**, sélectionnez **Ajouter un enregistrement SRV ou SPF**.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-251">To the right of **new row**, select **add SRV or SPF record**.</span></span>
    
    ![eNom-BP-configure-5-1](../../media/c73c154d-5aa0-41ef-be25-f43129eb178c.png)
  
5. <span data-ttu-id="ed6bc-253">Dans les zones des deux nouveaux enregistrements, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-253">In the boxes for the two new records, type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="ed6bc-254">**Service (Service)**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-254">**Service**</span></span>|<span data-ttu-id="ed6bc-255">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-255">**Protocol**</span></span>|<span data-ttu-id="ed6bc-256">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-256">**Priority**</span></span>|<span data-ttu-id="ed6bc-257">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-257">**Weight**</span></span>|<span data-ttu-id="ed6bc-258">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-258">**Port**</span></span>|<span data-ttu-id="ed6bc-259">**Target (Cible)          (Hostname) (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-259">**Target          (Hostname)**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="ed6bc-260">_sip</span><span class="sxs-lookup"><span data-stu-id="ed6bc-260">_sip</span></span>  <br/> |<span data-ttu-id="ed6bc-261">_tls</span><span class="sxs-lookup"><span data-stu-id="ed6bc-261">_tls</span></span>  <br/> |<span data-ttu-id="ed6bc-262">100</span><span class="sxs-lookup"><span data-stu-id="ed6bc-262">100</span></span>  <br/> |<span data-ttu-id="ed6bc-263">0,1</span><span class="sxs-lookup"><span data-stu-id="ed6bc-263">1</span></span>  <br/> |<span data-ttu-id="ed6bc-264">443</span><span class="sxs-lookup"><span data-stu-id="ed6bc-264">443</span></span>  <br/> |<span data-ttu-id="ed6bc-265">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-265">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="ed6bc-266">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-266">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="ed6bc-267">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="ed6bc-267">_sipfederationtls</span></span>  <br/> |<span data-ttu-id="ed6bc-268">_tcp</span><span class="sxs-lookup"><span data-stu-id="ed6bc-268">_tcp</span></span>  <br/> |<span data-ttu-id="ed6bc-269">100</span><span class="sxs-lookup"><span data-stu-id="ed6bc-269">100</span></span>  <br/> |<span data-ttu-id="ed6bc-270">0,1</span><span class="sxs-lookup"><span data-stu-id="ed6bc-270">1</span></span>  <br/> |<span data-ttu-id="ed6bc-271">5061</span><span class="sxs-lookup"><span data-stu-id="ed6bc-271">5061</span></span>  <br/> |<span data-ttu-id="ed6bc-272">sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-272">sipfed.online.lync.com.</span></span>  <br/> <span data-ttu-id="ed6bc-273">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="ed6bc-273">**This value MUST end with a period (.)**</span></span> <br/> |
   
    ![eNom-BP-configure-5-2](../../media/4d478f40-780f-43b9-940b-712b09da8c63.png)
  
6. <span data-ttu-id="ed6bc-275">Sélectionnez **Enregistrer** .</span><span class="sxs-lookup"><span data-stu-id="ed6bc-275">Select **save**</span></span>
    
    ![eNom-BP-configure-5-3](../../media/d03b6f75-49f2-471d-978d-d32c47cd6aa7.png)
  
> [!NOTE]
>  <span data-ttu-id="ed6bc-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ed6bc-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  

