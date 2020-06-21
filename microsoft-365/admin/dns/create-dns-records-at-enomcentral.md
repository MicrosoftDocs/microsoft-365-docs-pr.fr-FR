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
ms.openlocfilehash: c964729c052f5c0b61441f14ce15a167caa06b72
ms.sourcegitcommit: 659adf65d88ee44f643c471e6202396f1ffb6576
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "44780396"
---
# <a name="create-dns-records-at-enomcentral-for-microsoft"></a><span data-ttu-id="e5b3a-103">Créer des enregistrements DNS sur auprès enomcentral pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="e5b3a-103">Create DNS records at eNomCentral for Microsoft</span></span>

 <span data-ttu-id="e5b3a-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="e5b3a-105">Si eNomCentral est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-105">If eNomCentral is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="e5b3a-106">Une fois ces enregistrements ajoutés sur auprès enomcentral, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-106">After you add these records at eNomCentral, your domain will be set up to work with Microsoft services.</span></span>

  
> [!NOTE]
>  <span data-ttu-id="e5b3a-107">Typically it takes about 15 minutes for DNS changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-107">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="e5b3a-108">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-108">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="e5b3a-109">If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="e5b3a-109">If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="e5b3a-110">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="e5b3a-110">Add a TXT record for verification</span></span>
<span data-ttu-id="e5b3a-111"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="e5b3a-111"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="e5b3a-112">Before you use your domain with Microsoft, we have to make sure that you own it.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-112">Before you use your domain with Microsoft, we have to make sure that you own it.</span></span> <span data-ttu-id="e5b3a-113">Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-113">Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e5b3a-114">This record is used only to verify that you own your domain; it doesn't affect anything else.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-114">This record is used only to verify that you own your domain; it doesn't affect anything else.</span></span> <span data-ttu-id="e5b3a-115">You can delete it later, if you like.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-115">You can delete it later, if you like.</span></span> 
  
<span data-ttu-id="e5b3a-116">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 0:46)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span><span class="sxs-lookup"><span data-stu-id="e5b3a-116">Follow the steps below or [watch the video (start at 0:46)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span></span>
  
1. <span data-ttu-id="e5b3a-117">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered).</span><span class="sxs-lookup"><span data-stu-id="e5b3a-117">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered).</span></span> <span data-ttu-id="e5b3a-118">You'll be prompted to login.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-118">You'll be prompted to login.</span></span>
    
    ![eNom-BP-configure-1-1](../../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. <span data-ttu-id="e5b3a-120">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-120">Under **my domains**, select the name of the domain that you want to edit.</span></span>
    
    ![eNom-BP-configure-1-2](../../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. <span data-ttu-id="e5b3a-122">Dans la liste déroulante **Manage Domain (Gérer le domaine)**, sélectionnez **Host Records (Enregistrements d'hôtes)**.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-122">On the **Manage Domain** drop-down list, choose **Host Records**.</span></span>
    
    ![eNom-BP-Verify-1-1](../../media/6e4184a1-9525-47a6-8a8a-9600126c0db4.png)
  
4. <span data-ttu-id="e5b3a-124">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-124">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="e5b3a-125">Choisissez la valeur **type d’enregistrement** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-125">Choose the **Record Type** value from the drop-down list.</span></span>
    
    ||||
    |:-----|:-----|:-----|
    |<span data-ttu-id="e5b3a-126">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-126">**Host Name**</span></span> <br/> |<span data-ttu-id="e5b3a-127">**Record Type**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-127">**Record Type**</span></span> <br/> |<span data-ttu-id="e5b3a-128">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-128">**Address**</span></span> <br/> |
    |@  <br/> |<span data-ttu-id="e5b3a-129">TXT</span><span class="sxs-lookup"><span data-stu-id="e5b3a-129">TXT</span></span>  <br/> |<span data-ttu-id="e5b3a-130">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="e5b3a-130">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="e5b3a-131">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-131">**Note:** This is an example.</span></span> <span data-ttu-id="e5b3a-132">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-132">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="e5b3a-133">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="e5b3a-133">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
       
   ![eNom-BP-Verify-1-2](../../media/e1f95529-46a6-40f9-9709-9fe66f373bcf.png)
  
5. <span data-ttu-id="e5b3a-135">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-135">Select **save**.</span></span>
    
    ![eNom-BP-Verify-1-3](../../media/d6277ab0-5d03-44e0-968f-fd5de1905423.png)
  
6. <span data-ttu-id="e5b3a-137">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-137">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="e5b3a-138">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Microsoft 365 et demandez à Microsoft 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-138">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft 365 and request Microsoft 365 to look for the record.</span></span>
  
<span data-ttu-id="e5b3a-139">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-139">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="e5b3a-140">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-140">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="e5b3a-141">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-141">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="e5b3a-142">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-142">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="e5b3a-143">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-143">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="e5b3a-144">Typically it takes about 15 minutes for DNS changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-144">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="e5b3a-145">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-145">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="e5b3a-146">If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="e5b3a-146">If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="e5b3a-147">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="e5b3a-147">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="e5b3a-148"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="e5b3a-148"><a name="BKMK_add_MX"> </a></span></span>

<span data-ttu-id="e5b3a-149">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 3:40)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span><span class="sxs-lookup"><span data-stu-id="e5b3a-149">Follow the steps below or [watch the video (start at 3:40)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span></span>
  
1. <span data-ttu-id="e5b3a-150">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered).</span><span class="sxs-lookup"><span data-stu-id="e5b3a-150">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered).</span></span> <span data-ttu-id="e5b3a-151">You'll be prompted to login.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-151">You'll be prompted to login.</span></span>
    
    ![eNom-BP-configure-1-1](../../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. <span data-ttu-id="e5b3a-153">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-153">Under **my domains**, select the name of the domain that you want to edit.</span></span>
    
    ![eNom-BP-configure-1-2](../../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. <span data-ttu-id="e5b3a-155">Dans la liste déroulante **Manage Domain (Gérer le domaine)**, sélectionnez **Email Settings (Paramètres de courrier)**.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-155">On the **Manage Domain** drop-down list, choose **Email Settings**.</span></span>
    
    ![eNom-BP-configure-1-3](../../media/4b438629-afdf-4a47-ab11-56644cdb6158.png)
  
4. <span data-ttu-id="e5b3a-157">Dans le menu déroulant **Service Selection (Sélection du service)**, choisissez **User (MX) (Utilisateur (MX))**.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-157">On the **Service Selection** drop-down list, choose **User (MX)**.</span></span>
    
    ![eNom-BP-configure-1-4](../../media/7680ab48-b8d1-4573-b20f-4745a5d7c079.png)
  
5. <span data-ttu-id="e5b3a-159">In the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-159">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="e5b3a-160">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-160">**Host Name**</span></span>|<span data-ttu-id="e5b3a-161">**Address**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-161">**Address**</span></span>|<span data-ttu-id="e5b3a-162">**Pref (Préference)**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-162">**Pref**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> | <span data-ttu-id="e5b3a-163">*\<domain-key\>*. mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-163">*\<domain-key\>*  .mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="e5b3a-164">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-164">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="e5b3a-165">**Remarque :** Obtenir votre *\<domain-key\>* à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-165">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>           [<span data-ttu-id="e5b3a-166">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="e5b3a-166">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="e5b3a-167">10 </span><span class="sxs-lookup"><span data-stu-id="e5b3a-167">10</span></span>  <br/> <span data-ttu-id="e5b3a-168">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span><span class="sxs-lookup"><span data-stu-id="e5b3a-168">For more information about priority, see [What is MX priority?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span></span> <br/> |
       
   ![eNom-BP-configure-2-1](../../media/c32e8954-8209-4f77-a3a8-4b7aeea325d5.png)
  
6. <span data-ttu-id="e5b3a-170">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-170">Select **save**.</span></span>
    
    ![eNom-BP-configure-2-2](../../media/cf3058ea-9d30-4747-8cf0-2bc13d5ec6be.png)
  
7. <span data-ttu-id="e5b3a-172">Si d'autres enregistrements MX sont répertoriés, activez les cases à cocher correspondantes pour les sélectionner.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-172">If there are any other existing MX records, select the check boxes for those records to select them.</span></span>
    
    ![eNom-BP-configure-2-3](../../media/5017ed03-ca76-4c5c-93a7-84ffe24125dc.png)
  
8. <span data-ttu-id="e5b3a-174">Sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-174">Select **delete checked**.</span></span>
    
    ![eNom-BP-configure-2-4](../../media/072dc039-bddb-4c1f-bb44-5660e77f14b0.png)
  
## <a name="add-the-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="e5b3a-176">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="e5b3a-176">Add the CNAME records that are required for Microsoft</span></span> 
<span data-ttu-id="e5b3a-177"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="e5b3a-177"><a name="BKMK_add_CNAME"> </a></span></span>

<span data-ttu-id="e5b3a-178">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 4:24)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span><span class="sxs-lookup"><span data-stu-id="e5b3a-178">Follow the steps below or [watch the video (start at 4:24)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span></span>
  
1. <span data-ttu-id="e5b3a-179">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered).</span><span class="sxs-lookup"><span data-stu-id="e5b3a-179">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered).</span></span> <span data-ttu-id="e5b3a-180">You'll be prompted to login.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-180">You'll be prompted to login.</span></span>
    
    ![eNom-BP-configure-1-1](../../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. <span data-ttu-id="e5b3a-182">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-182">Under **my domains**, select the name of the domain that you want to edit.</span></span>
    
    ![eNom-BP-configure-1-2](../../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. <span data-ttu-id="e5b3a-184">Dans la liste déroulante **Manage Domain (Gérer le domaine)**, sélectionnez **Host Records (Enregistrements d'hôtes)**.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-184">On the **Manage Domain** drop-down list, choose **Host Records**.</span></span>
    
    ![eNom-BP-configure-1-5](../../media/c92c514c-8166-4cba-97e3-ee1d9847d255.png)
  
4. <span data-ttu-id="e5b3a-186">Sélectionnez **nouvelle ligne**.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-186">Select **new row**.</span></span>
    
    ![eNom-BP-configure-3-1](../../media/a30f0a88-7b09-411e-9133-e7965bcf1de0.png)
  
5. <span data-ttu-id="e5b3a-188">Dans les zones des six nouveaux enregistrements, tapez ou copiez-collez les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-188">In the boxes for the six new records, type or copy and paste the following values.</span></span>
    
<span data-ttu-id="e5b3a-189">Choisissez la valeur **type d’enregistrement** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-189">Choose the **Record Type** value from the drop-down list.</span></span>
        
    |<span data-ttu-id="e5b3a-190">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-190">**Host Name**</span></span>|<span data-ttu-id="e5b3a-191">**Record Type**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-191">**Record Type**</span></span>|<span data-ttu-id="e5b3a-192">**Address (Adresse)**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-192">**Address**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="e5b3a-193">autodiscover</span><span class="sxs-lookup"><span data-stu-id="e5b3a-193">autodiscover</span></span>  <br/> |<span data-ttu-id="e5b3a-194">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="e5b3a-194">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="e5b3a-195">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-195">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="e5b3a-196">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-196">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="e5b3a-197">sip</span><span class="sxs-lookup"><span data-stu-id="e5b3a-197">sip</span></span>  <br/> |<span data-ttu-id="e5b3a-198">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="e5b3a-198">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="e5b3a-199">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-199">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="e5b3a-200">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-200">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="e5b3a-201">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="e5b3a-201">lyncdiscover</span></span>  <br/> |<span data-ttu-id="e5b3a-202">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="e5b3a-202">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="e5b3a-203">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-203">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="e5b3a-204">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-204">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="e5b3a-205">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="e5b3a-205">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="e5b3a-206">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="e5b3a-206">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="e5b3a-207">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-207">enterpriseregistration.windows.net.</span></span>  <br/> <span data-ttu-id="e5b3a-208">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-208">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="e5b3a-209">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="e5b3a-209">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="e5b3a-210">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="e5b3a-210">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="e5b3a-211">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-211">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> <span data-ttu-id="e5b3a-212">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-212">**This value MUST end with a period (.)**</span></span> <br/> |
   
    ![eNom-BP-Configure-3-2](../../media/672371c0-51af-44ba-bb18-80286b7676c1.png)
  
6. <span data-ttu-id="e5b3a-213">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-213">Select **save**.</span></span>
    
    ![eNom-BP-configure-3-3](../../media/027b57ce-5699-408b-993b-e46a9ac31090.png)
  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="e5b3a-215">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="e5b3a-215">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="e5b3a-216"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="e5b3a-216"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5b3a-217">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-217">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="e5b3a-218">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-218">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="e5b3a-219">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-219">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="e5b3a-220">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-220">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>
  
<span data-ttu-id="e5b3a-221">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 5:12)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span><span class="sxs-lookup"><span data-stu-id="e5b3a-221">Follow the steps below or [watch the video (start at 5:12)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span></span>
  
1. <span data-ttu-id="e5b3a-222">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered).</span><span class="sxs-lookup"><span data-stu-id="e5b3a-222">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered).</span></span> <span data-ttu-id="e5b3a-223">You'll be prompted to login.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-223">You'll be prompted to login.</span></span>
    
    ![eNom-BP-configure-1-1](../../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. <span data-ttu-id="e5b3a-225">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-225">Under **my domains**, select the name of the domain that you want to edit.</span></span>
    
    ![eNom-BP-configure-1-2](../../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. <span data-ttu-id="e5b3a-227">Dans la liste déroulante **Manage Domain (Gérer le domaine)**, sélectionnez **Host Records (Enregistrements d'hôtes)**.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-227">On the **Manage Domain** drop-down list, choose **Host Records**.</span></span>
    
    ![eNom-BP-configure-1-5](../../media/c92c514c-8166-4cba-97e3-ee1d9847d255.png)
  
4. <span data-ttu-id="e5b3a-229">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-229">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
<span data-ttu-id="e5b3a-230">Choisissez la valeur **type d’enregistrement** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-230">Choose the **Record Type** value from the drop-down list.</span></span>
    
    |<span data-ttu-id="e5b3a-231">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-231">**Host Name**</span></span>|<span data-ttu-id="e5b3a-232">**Record Type**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-232">**Record Type**</span></span>|<span data-ttu-id="e5b3a-233">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-233">**Address**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="e5b3a-234">TXT</span><span class="sxs-lookup"><span data-stu-id="e5b3a-234">TXT</span></span>  <br/> |<span data-ttu-id="e5b3a-235">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="e5b3a-235">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/><span data-ttu-id="e5b3a-236">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-236">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
   ![eNom-BP-configure-4-1](../../media/64c68697-258d-4044-84b1-c28f4a402e3b.png)
  
5. <span data-ttu-id="e5b3a-238">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-238">Select **save**.</span></span>
    
    ![eNom-BP-configure-4-2](../../media/89f4effa-349e-4734-96a5-cd80b0cecd60.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="e5b3a-240">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="e5b3a-240">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="e5b3a-241"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="e5b3a-241"><a name="BKMK_add_SRV"> </a></span></span>

<span data-ttu-id="e5b3a-242">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 5:50)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span><span class="sxs-lookup"><span data-stu-id="e5b3a-242">Follow the steps below or [watch the video (start at 5:50)](https://support.microsoft.com/office/3766a9e8-77dd-4a42-908d-89b076143e7d).</span></span>
  
1. <span data-ttu-id="e5b3a-243">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered).</span><span class="sxs-lookup"><span data-stu-id="e5b3a-243">To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered).</span></span> <span data-ttu-id="e5b3a-244">You'll be prompted to login.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-244">You'll be prompted to login.</span></span>
    
    ![eNom-BP-configure-1-1](../../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. <span data-ttu-id="e5b3a-246">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-246">Under **my domains**, select the name of the domain that you want to edit.</span></span>
    
    ![eNom-BP-configure-1-2](../../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. <span data-ttu-id="e5b3a-248">Dans la liste déroulante **Manage Domain (Gérer le domaine)**, sélectionnez **Host Records (Enregistrements d'hôtes)**.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-248">On the **Manage Domain** drop-down list, choose **Host Records**.</span></span>
    
    ![eNom-BP-configure-1-5](../../media/c92c514c-8166-4cba-97e3-ee1d9847d255.png)
  
4. <span data-ttu-id="e5b3a-250">À droite de **nouvelle ligne**, sélectionnez **Ajouter un enregistrement SRV ou SPF**.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-250">To the right of **new row**, select **add SRV or SPF record**.</span></span>
    
    ![eNom-BP-configure-5-1](../../media/c73c154d-5aa0-41ef-be25-f43129eb178c.png)
  
5. <span data-ttu-id="e5b3a-252">Dans les zones des deux nouveaux enregistrements, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-252">In the boxes for the two new records, type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="e5b3a-253">**Service (Service)**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-253">**Service**</span></span>|<span data-ttu-id="e5b3a-254">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-254">**Protocol**</span></span>|<span data-ttu-id="e5b3a-255">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-255">**Priority**</span></span>|<span data-ttu-id="e5b3a-256">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-256">**Weight**</span></span>|<span data-ttu-id="e5b3a-257">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-257">**Port**</span></span>|<span data-ttu-id="e5b3a-258">**Target (Cible)          (Hostname) (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-258">**Target          (Hostname)**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="e5b3a-259">_sip</span><span class="sxs-lookup"><span data-stu-id="e5b3a-259">_sip</span></span>  <br/> |<span data-ttu-id="e5b3a-260">_tls</span><span class="sxs-lookup"><span data-stu-id="e5b3a-260">_tls</span></span>  <br/> |<span data-ttu-id="e5b3a-261">100</span><span class="sxs-lookup"><span data-stu-id="e5b3a-261">100</span></span>  <br/> |<span data-ttu-id="e5b3a-262">1 </span><span class="sxs-lookup"><span data-stu-id="e5b3a-262">1</span></span>  <br/> |<span data-ttu-id="e5b3a-263">443</span><span class="sxs-lookup"><span data-stu-id="e5b3a-263">443</span></span>  <br/> |<span data-ttu-id="e5b3a-264">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-264">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="e5b3a-265">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-265">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="e5b3a-266">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="e5b3a-266">_sipfederationtls</span></span>  <br/> |<span data-ttu-id="e5b3a-267">_tcp</span><span class="sxs-lookup"><span data-stu-id="e5b3a-267">_tcp</span></span>  <br/> |<span data-ttu-id="e5b3a-268">100</span><span class="sxs-lookup"><span data-stu-id="e5b3a-268">100</span></span>  <br/> |<span data-ttu-id="e5b3a-269">1 </span><span class="sxs-lookup"><span data-stu-id="e5b3a-269">1</span></span>  <br/> |<span data-ttu-id="e5b3a-270">5061</span><span class="sxs-lookup"><span data-stu-id="e5b3a-270">5061</span></span>  <br/> |<span data-ttu-id="e5b3a-271">sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-271">sipfed.online.lync.com.</span></span>  <br/> <span data-ttu-id="e5b3a-272">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="e5b3a-272">**This value MUST end with a period (.)**</span></span> <br/> |
   
    ![eNom-BP-configure-5-2](../../media/4d478f40-780f-43b9-940b-712b09da8c63.png)
  
6. <span data-ttu-id="e5b3a-274">Sélectionnez **Enregistrer** .</span><span class="sxs-lookup"><span data-stu-id="e5b3a-274">Select **save**</span></span>
    
    ![eNom-BP-configure-5-3](../../media/d03b6f75-49f2-471d-978d-d32c47cd6aa7.png)
  
> [!NOTE]
>  <span data-ttu-id="e5b3a-276">Typically it takes about 15 minutes for DNS changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-276">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="e5b3a-277">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="e5b3a-277">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="e5b3a-278">If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="e5b3a-278">If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  

