---
title: Créer des enregistrements DNS sur auprès enomcentral pour Microsoft
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
ms.assetid: a6626053-a9c8-445b-81ee-eeb6672fae77
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur auprès enomcentral pour Microsoft.
ms.openlocfilehash: 94b0648e03d756f429094a6d35f03d5596a272f4
ms.sourcegitcommit: 50526f81ce3f57d58f0a7c0df4fe21685c5a0236
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/28/2020
ms.locfileid: "45434190"
---
# <a name="create-dns-records-at-enomcentral-for-microsoft"></a><span data-ttu-id="efcc5-103">Créer des enregistrements DNS sur auprès enomcentral pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="efcc5-103">Create DNS records at eNomCentral for Microsoft</span></span>

 <span data-ttu-id="efcc5-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="efcc5-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span>

<span data-ttu-id="efcc5-105">Si eNomCentral est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="efcc5-105">If eNomCentral is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>

<span data-ttu-id="efcc5-106">Une fois ces enregistrements ajoutés sur auprès enomcentral, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="efcc5-106">After you add these records at eNomCentral, your domain will be set up to work with Microsoft services.</span></span>

> [!NOTE]
> <span data-ttu-id="efcc5-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="efcc5-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span>

## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="efcc5-110">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="efcc5-110">Add a TXT record for verification</span></span>
<span data-ttu-id="efcc5-111"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="efcc5-111"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="efcc5-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="efcc5-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>

> [!NOTE]
> <span data-ttu-id="efcc5-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="efcc5-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span>

<span data-ttu-id="efcc5-116">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 0:46)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span><span class="sxs-lookup"><span data-stu-id="efcc5-116">Follow the steps below or [watch the video (start at 0:46)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span></span>

1. <span data-ttu-id="efcc5-p104">Pour commencer, accédez à la page de vos domaines sur le site eNom Central en utilisant [ce lien](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="efcc5-p104">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). You'll be prompted to login.</span></span>

   ![eNom-BP-configure-1-1](../../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)

2. <span data-ttu-id="efcc5-120">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="efcc5-120">Under **my domains**, select the name of the domain that you want to edit.</span></span>

   ![eNom-BP-configure-1-2](../../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)

3. <span data-ttu-id="efcc5-122">Dans la liste déroulante **Manage Domain (Gérer le domaine)**, sélectionnez **Host Records (Enregistrements d'hôtes)**.</span><span class="sxs-lookup"><span data-stu-id="efcc5-122">On the **Manage Domain** drop-down list, choose **Host Records**.</span></span>

   ![eNom-BP-Verify-1-1](../../media/6e4184a1-9525-47a6-8a8a-9600126c0db4.png)

4. <span data-ttu-id="efcc5-124">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="efcc5-124">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>

   <span data-ttu-id="efcc5-125">Choisissez la valeur **type d’enregistrement** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="efcc5-125">Choose the **Record Type** value from the drop-down list.</span></span>

   |<span data-ttu-id="efcc5-126">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="efcc5-126">Host Name</span></span>|<span data-ttu-id="efcc5-127">Record Type</span><span class="sxs-lookup"><span data-stu-id="efcc5-127">Record Type</span></span>|<span data-ttu-id="efcc5-128">Adresse</span><span class="sxs-lookup"><span data-stu-id="efcc5-128">Address</span></span>|
   |---|---|---|
   |@|<span data-ttu-id="efcc5-129">TXT</span><span class="sxs-lookup"><span data-stu-id="efcc5-129">TXT</span></span>|<span data-ttu-id="efcc5-130">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="efcc5-130">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="efcc5-131">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="efcc5-131">**Note:** This is an example.</span></span> <span data-ttu-id="efcc5-132">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="efcc5-132">Use your specific **Destination or Points to Address** value here, from the table.</span></span> [<span data-ttu-id="efcc5-133">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="efcc5-133">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)|

   ![eNom-BP-Verify-1-2](../../media/e1f95529-46a6-40f9-9709-9fe66f373bcf.png)

5. <span data-ttu-id="efcc5-135">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="efcc5-135">Select **save**.</span></span>

   ![eNom-BP-Verify-1-3](../../media/d6277ab0-5d03-44e0-968f-fd5de1905423.png)

6. <span data-ttu-id="efcc5-137">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="efcc5-137">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>

<span data-ttu-id="efcc5-138">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Microsoft 365 et demandez à Microsoft 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="efcc5-138">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft 365 and request Microsoft 365 to look for the record.</span></span>

<span data-ttu-id="efcc5-139">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="efcc5-139">When Microsoft finds the correct TXT record, your domain is verified.</span></span>

1. <span data-ttu-id="efcc5-140">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="efcc5-140">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

2. <span data-ttu-id="efcc5-141">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="efcc5-141">On the **Domains** page, select the domain that you are verifying.</span></span>

3. <span data-ttu-id="efcc5-142">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="efcc5-142">On the **Setup** page, select **Start setup**.</span></span>

4. <span data-ttu-id="efcc5-143">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="efcc5-143">On the **Verify domain** page, select **Verify**.</span></span>

> [!NOTE]
> <span data-ttu-id="efcc5-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="efcc5-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span>

## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="efcc5-147">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="efcc5-147">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="efcc5-148"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="efcc5-148"><a name="BKMK_add_MX"> </a></span></span>

<span data-ttu-id="efcc5-149">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 3:40)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span><span class="sxs-lookup"><span data-stu-id="efcc5-149">Follow the steps below or [watch the video (start at 3:40)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span></span>

1. <span data-ttu-id="efcc5-p107">Pour commencer, accédez à la page de vos domaines sur le site eNom Central en utilisant [ce lien](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="efcc5-p107">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). You'll be prompted to login.</span></span>

   ![eNom-BP-configure-1-1](../../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)

2. <span data-ttu-id="efcc5-153">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="efcc5-153">Under **my domains**, select the name of the domain that you want to edit.</span></span>

   ![eNom-BP-configure-1-2](../../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)

3. <span data-ttu-id="efcc5-155">Dans la liste déroulante **Manage Domain (Gérer le domaine)**, sélectionnez **Email Settings (Paramètres de courrier)**.</span><span class="sxs-lookup"><span data-stu-id="efcc5-155">On the **Manage Domain** drop-down list, choose **Email Settings**.</span></span>

   ![eNom-BP-configure-1-3](../../media/4b438629-afdf-4a47-ab11-56644cdb6158.png)

4. <span data-ttu-id="efcc5-157">Dans le menu déroulant **Service Selection (Sélection du service)**, choisissez **User (MX) (Utilisateur (MX))**.</span><span class="sxs-lookup"><span data-stu-id="efcc5-157">On the **Service Selection** drop-down list, choose **User (MX)**.</span></span>

   ![eNom-BP-configure-1-4](../../media/7680ab48-b8d1-4573-b20f-4745a5d7c079.png)

5. <span data-ttu-id="efcc5-159">In the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="efcc5-159">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>

   |<span data-ttu-id="efcc5-160">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="efcc5-160">Host Name</span></span>|<span data-ttu-id="efcc5-161">Adresse</span><span class="sxs-lookup"><span data-stu-id="efcc5-161">Address</span></span>|<span data-ttu-id="efcc5-162">Pref (Préference)</span><span class="sxs-lookup"><span data-stu-id="efcc5-162">Pref</span></span>|
   |---|---|---|
   |@| <span data-ttu-id="efcc5-163">*\<domain-key\>*. mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="efcc5-163">*\<domain-key\>*  .mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="efcc5-164">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="efcc5-164">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="efcc5-165">**Remarque :** Obtenir votre *\<domain-key\>* à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="efcc5-165">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span> [<span data-ttu-id="efcc5-166">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="efcc5-166">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)|<span data-ttu-id="efcc5-167">10 </span><span class="sxs-lookup"><span data-stu-id="efcc5-167">10</span></span>  <br/> <span data-ttu-id="efcc5-168">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span><span class="sxs-lookup"><span data-stu-id="efcc5-168">For more information about priority, see [What is MX priority?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span></span>|

   ![eNom-BP-configure-2-1](../../media/c32e8954-8209-4f77-a3a8-4b7aeea325d5.png)

6. <span data-ttu-id="efcc5-170">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="efcc5-170">Select **save**.</span></span>

   ![eNom-BP-configure-2-2](../../media/cf3058ea-9d30-4747-8cf0-2bc13d5ec6be.png)

7. <span data-ttu-id="efcc5-172">Si d'autres enregistrements MX sont répertoriés, activez les cases à cocher correspondantes pour les sélectionner.</span><span class="sxs-lookup"><span data-stu-id="efcc5-172">If there are any other existing MX records, select the check boxes for those records to select them.</span></span>

   ![eNom-BP-configure-2-3](../../media/5017ed03-ca76-4c5c-93a7-84ffe24125dc.png)

8. <span data-ttu-id="efcc5-174">Sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="efcc5-174">Select **delete checked**.</span></span>

   ![eNom-BP-configure-2-4](../../media/072dc039-bddb-4c1f-bb44-5660e77f14b0.png)

## <a name="add-the-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="efcc5-176">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="efcc5-176">Add the CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="efcc5-177"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="efcc5-177"><a name="BKMK_add_CNAME"> </a></span></span>

<span data-ttu-id="efcc5-178">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 4:24)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span><span class="sxs-lookup"><span data-stu-id="efcc5-178">Follow the steps below or [watch the video (start at 4:24)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span></span>

1. <span data-ttu-id="efcc5-p109">Pour commencer, accédez à la page de vos domaines sur le site eNom Central en utilisant [ce lien](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="efcc5-p109">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). You'll be prompted to login.</span></span>

   ![eNom-BP-configure-1-1](../../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)

2. <span data-ttu-id="efcc5-182">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="efcc5-182">Under **my domains**, select the name of the domain that you want to edit.</span></span>

   ![eNom-BP-configure-1-2](../../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)

3. <span data-ttu-id="efcc5-184">Dans la liste déroulante **Manage Domain (Gérer le domaine)**, sélectionnez **Host Records (Enregistrements d'hôtes)**.</span><span class="sxs-lookup"><span data-stu-id="efcc5-184">On the **Manage Domain** drop-down list, choose **Host Records**.</span></span>

   ![eNom-BP-configure-1-5](../../media/c92c514c-8166-4cba-97e3-ee1d9847d255.png)

4. <span data-ttu-id="efcc5-186">Sélectionnez **nouvelle ligne**.</span><span class="sxs-lookup"><span data-stu-id="efcc5-186">Select **new row**.</span></span>

   ![eNom-BP-configure-3-1](../../media/a30f0a88-7b09-411e-9133-e7965bcf1de0.png)

5. <span data-ttu-id="efcc5-188">Dans les zones des six nouveaux enregistrements, tapez ou copiez-collez les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="efcc5-188">In the boxes for the six new records, type or copy and paste the following values.</span></span>

   <span data-ttu-id="efcc5-189">Choisissez la valeur **type d’enregistrement** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="efcc5-189">Choose the **Record Type** value from the drop-down list.</span></span>

   |<span data-ttu-id="efcc5-190">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="efcc5-190">Host Name</span></span>|<span data-ttu-id="efcc5-191">Record Type</span><span class="sxs-lookup"><span data-stu-id="efcc5-191">Record Type</span></span>|<span data-ttu-id="efcc5-192">Adresse</span><span class="sxs-lookup"><span data-stu-id="efcc5-192">Address</span></span>|
   |---|---|---|
   |<span data-ttu-id="efcc5-193">autodiscover</span><span class="sxs-lookup"><span data-stu-id="efcc5-193">autodiscover</span></span>|<span data-ttu-id="efcc5-194">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="efcc5-194">CNAME (Alias)</span></span>|<span data-ttu-id="efcc5-195">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="efcc5-195">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="efcc5-196">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="efcc5-196">**This value MUST end with a period (.)**</span></span>|
   |<span data-ttu-id="efcc5-197">sip</span><span class="sxs-lookup"><span data-stu-id="efcc5-197">sip</span></span>|<span data-ttu-id="efcc5-198">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="efcc5-198">CNAME (Alias)</span></span>|<span data-ttu-id="efcc5-199">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="efcc5-199">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="efcc5-200">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="efcc5-200">**This value MUST end with a period (.)**</span></span>|
   |<span data-ttu-id="efcc5-201">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="efcc5-201">lyncdiscover</span></span>|<span data-ttu-id="efcc5-202">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="efcc5-202">CNAME (Alias)</span></span>|<span data-ttu-id="efcc5-203">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="efcc5-203">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="efcc5-204">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="efcc5-204">**This value MUST end with a period (.)**</span></span>|
   |<span data-ttu-id="efcc5-205">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="efcc5-205">enterpriseregistration</span></span>|<span data-ttu-id="efcc5-206">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="efcc5-206">CNAME (Alias)</span></span>|<span data-ttu-id="efcc5-207">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="efcc5-207">enterpriseregistration.windows.net.</span></span>  <br/> <span data-ttu-id="efcc5-208">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="efcc5-208">**This value MUST end with a period (.)**</span></span>|
   |<span data-ttu-id="efcc5-209">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="efcc5-209">enterpriseenrollment</span></span>|<span data-ttu-id="efcc5-210">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="efcc5-210">CNAME (Alias)</span></span>|<span data-ttu-id="efcc5-211">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="efcc5-211">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> <span data-ttu-id="efcc5-212">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="efcc5-212">**This value MUST end with a period (.)**</span></span>|

   ![eNom-BP-configure-3-2](../../media/672371c0-51af-44ba-bb18-80286b7676c1.png)

6. <span data-ttu-id="efcc5-214">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="efcc5-214">Select **save**.</span></span>

   ![eNom-BP-configure-3-3](../../media/027b57ce-5699-408b-993b-e46a9ac31090.png)

## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="efcc5-216">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="efcc5-216">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="efcc5-217"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="efcc5-217"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="efcc5-218">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="efcc5-218">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="efcc5-219">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="efcc5-219">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="efcc5-220">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="efcc5-220">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="efcc5-221">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="efcc5-221">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>

<span data-ttu-id="efcc5-222">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 5:12)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span><span class="sxs-lookup"><span data-stu-id="efcc5-222">Follow the steps below or [watch the video (start at 5:12)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span></span>

1. <span data-ttu-id="efcc5-p111">Pour commencer, accédez à la page de vos domaines sur le site eNom Central en utilisant [ce lien](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="efcc5-p111">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). You'll be prompted to login.</span></span>

   ![eNom-BP-configure-1-1](../../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)

2. <span data-ttu-id="efcc5-226">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="efcc5-226">Under **my domains**, select the name of the domain that you want to edit.</span></span>

   ![eNom-BP-configure-1-2](../../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)

3. <span data-ttu-id="efcc5-228">Dans la liste déroulante **Manage Domain (Gérer le domaine)**, sélectionnez **Host Records (Enregistrements d'hôtes)**.</span><span class="sxs-lookup"><span data-stu-id="efcc5-228">On the **Manage Domain** drop-down list, choose **Host Records**.</span></span>

   ![eNom-BP-configure-1-5](../../media/c92c514c-8166-4cba-97e3-ee1d9847d255.png)

4. <span data-ttu-id="efcc5-230">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="efcc5-230">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>

   <span data-ttu-id="efcc5-231">Choisissez la valeur **type d’enregistrement** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="efcc5-231">Choose the **Record Type** value from the drop-down list.</span></span>

   |<span data-ttu-id="efcc5-232">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="efcc5-232">Host Name</span></span>|<span data-ttu-id="efcc5-233">Record Type</span><span class="sxs-lookup"><span data-stu-id="efcc5-233">Record Type</span></span>|<span data-ttu-id="efcc5-234">Adresse</span><span class="sxs-lookup"><span data-stu-id="efcc5-234">Address</span></span>|
   |---|---|---|
   |@|<span data-ttu-id="efcc5-235">TXT</span><span class="sxs-lookup"><span data-stu-id="efcc5-235">TXT</span></span>|<span data-ttu-id="efcc5-236">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="efcc5-236">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/><span data-ttu-id="efcc5-237">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="efcc5-237">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>|

   ![eNom-BP-configure-4-1](../../media/64c68697-258d-4044-84b1-c28f4a402e3b.png)

5. <span data-ttu-id="efcc5-239">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="efcc5-239">Select **save**.</span></span>

   ![eNom-BP-configure-4-2](../../media/89f4effa-349e-4734-96a5-cd80b0cecd60.png)

## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="efcc5-241">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="efcc5-241">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="efcc5-242"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="efcc5-242"><a name="BKMK_add_SRV"> </a></span></span>

<span data-ttu-id="efcc5-243">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 5:50)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span><span class="sxs-lookup"><span data-stu-id="efcc5-243">Follow the steps below or [watch the video (start at 5:50)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span></span>

1. <span data-ttu-id="efcc5-p112">Pour commencer, accédez à la page de vos domaines sur le site eNom Central en utilisant [ce lien](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="efcc5-p112">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). You'll be prompted to login.</span></span>

   ![eNom-BP-configure-1-1](../../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)

2. <span data-ttu-id="efcc5-247">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="efcc5-247">Under **my domains**, select the name of the domain that you want to edit.</span></span>

   ![eNom-BP-configure-1-2](../../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)

3. <span data-ttu-id="efcc5-249">Dans la liste déroulante **Manage Domain (Gérer le domaine)**, sélectionnez **Host Records (Enregistrements d'hôtes)**.</span><span class="sxs-lookup"><span data-stu-id="efcc5-249">On the **Manage Domain** drop-down list, choose **Host Records**.</span></span>

   ![eNom-BP-configure-1-5](../../media/c92c514c-8166-4cba-97e3-ee1d9847d255.png)

4. <span data-ttu-id="efcc5-251">À droite de **nouvelle ligne**, sélectionnez **Ajouter un enregistrement SRV ou SPF**.</span><span class="sxs-lookup"><span data-stu-id="efcc5-251">To the right of **new row**, select **add SRV or SPF record**.</span></span>

   ![eNom-BP-configure-5-1](../../media/c73c154d-5aa0-41ef-be25-f43129eb178c.png)

5. <span data-ttu-id="efcc5-253">Dans les zones des deux nouveaux enregistrements, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="efcc5-253">In the boxes for the two new records, type or copy and paste the values from the following table.</span></span>

   |<span data-ttu-id="efcc5-254">Service</span><span class="sxs-lookup"><span data-stu-id="efcc5-254">Service</span></span>|<span data-ttu-id="efcc5-255">Protocole</span><span class="sxs-lookup"><span data-stu-id="efcc5-255">Protocol</span></span>|<span data-ttu-id="efcc5-256">Priorité</span><span class="sxs-lookup"><span data-stu-id="efcc5-256">Priority</span></span>|<span data-ttu-id="efcc5-257">Pondération</span><span class="sxs-lookup"><span data-stu-id="efcc5-257">Weight</span></span>|<span data-ttu-id="efcc5-258">Port</span><span class="sxs-lookup"><span data-stu-id="efcc5-258">Port</span></span>|<span data-ttu-id="efcc5-259">Cible (nom d’hôte)</span><span class="sxs-lookup"><span data-stu-id="efcc5-259">Target (Hostname)</span></span>|
   |---|---|---|---|---|---|
   |<span data-ttu-id="efcc5-260">_sip</span><span class="sxs-lookup"><span data-stu-id="efcc5-260">_sip</span></span>|<span data-ttu-id="efcc5-261">_tls</span><span class="sxs-lookup"><span data-stu-id="efcc5-261">_tls</span></span>|<span data-ttu-id="efcc5-262">100</span><span class="sxs-lookup"><span data-stu-id="efcc5-262">100</span></span>|<span data-ttu-id="efcc5-263">0,1</span><span class="sxs-lookup"><span data-stu-id="efcc5-263">1</span></span>|<span data-ttu-id="efcc5-264">443</span><span class="sxs-lookup"><span data-stu-id="efcc5-264">443</span></span>|<span data-ttu-id="efcc5-265">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="efcc5-265">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="efcc5-266">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="efcc5-266">**This value MUST end with a period (.)**</span></span>|
   |<span data-ttu-id="efcc5-267">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="efcc5-267">_sipfederationtls</span></span>|<span data-ttu-id="efcc5-268">_tcp</span><span class="sxs-lookup"><span data-stu-id="efcc5-268">_tcp</span></span>|<span data-ttu-id="efcc5-269">100</span><span class="sxs-lookup"><span data-stu-id="efcc5-269">100</span></span>|<span data-ttu-id="efcc5-270">0,1</span><span class="sxs-lookup"><span data-stu-id="efcc5-270">1</span></span>|<span data-ttu-id="efcc5-271">5061</span><span class="sxs-lookup"><span data-stu-id="efcc5-271">5061</span></span>|<span data-ttu-id="efcc5-272">sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="efcc5-272">sipfed.online.lync.com.</span></span>  <br/> <span data-ttu-id="efcc5-273">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="efcc5-273">**This value MUST end with a period (.)**</span></span>|

   ![eNom-BP-configure-5-2](../../media/4d478f40-780f-43b9-940b-712b09da8c63.png)

6. <span data-ttu-id="efcc5-275">Sélectionnez **Enregistrer** .</span><span class="sxs-lookup"><span data-stu-id="efcc5-275">Select **save**</span></span>

   ![eNom-BP-configure-5-3](../../media/d03b6f75-49f2-471d-978d-d32c47cd6aa7.png)

> [!NOTE]
> <span data-ttu-id="efcc5-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="efcc5-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span>
