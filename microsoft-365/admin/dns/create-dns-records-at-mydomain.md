---
title: Créer des enregistrements DNS auprès de MyDomain pour Microsoft
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
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
ms.assetid: 9982191d-ed79-46a9-b2e7-317d1a3a9867
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online et les autres services sur MyDomain pour Microsoft.
ms.openlocfilehash: c084c0343b98e8231baae65ff0ec01ecb5bc135c
ms.sourcegitcommit: 555d756c69ac9031d1fb928f2e1f9750beede066
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2020
ms.locfileid: "47306994"
---
# <a name="create-dns-records-at-mydomain-for-microsoft"></a><span data-ttu-id="918df-103">Créer des enregistrements DNS auprès de MyDomain pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="918df-103">Create DNS records at MyDomain for Microsoft</span></span>


  
 <span data-ttu-id="918df-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="918df-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="918df-p101">Le site web MyDomain ne prend pas en charge les enregistrements SRV, ce qui signifie que plusieurs fonctionnalités de Skype Entreprise Online et d’Outlook Web App ne fonctionnent pas. Quelle que soit l’offre Microsoft que vous utilisez, si vous gérez vos enregistrements DNS via MyDomain, il existe des [limitations de service importantes](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq). Le cas échéant, vous pouvez basculer vers un autre fournisseur d’hébergement DNS.</span><span class="sxs-lookup"><span data-stu-id="918df-p101">The MyDomain website doesn't support SRV records, which means several Skype for Business Online and Outlook Web App features won't work. No matter which Microsoft plan you use, if you manage your DNS records at MyDomain, there are [significant service limitations](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq), and you might want to switch to a different DNS hosting provider.</span></span> 
  
<span data-ttu-id="918df-107">Si vous décidez de gérer vos propres enregistrements DNS Microsoft via MyDomain malgré ces limitations de service, procédez de la manière décrite dans cet article pour configurer vos enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="918df-107">If you choose to manage your own Microsoft DNS records at MyDomain despite the service limitations, follow the steps in this article to set up your DNS records for email, Skype for Business Online, and so on.</span></span>
    
<span data-ttu-id="918df-108">Une fois ces enregistrements ajoutés sur MyDomain, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="918df-108">After you add these records at MyDomain, your domain will be set up to work with Microsoft services.</span></span>
  

  
> [!NOTE]
> <span data-ttu-id="918df-109">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="918df-109">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="918df-110">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="918df-110">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="918df-111">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="918df-111">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="918df-112">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="918df-112">Add a TXT record for verification</span></span>
<span data-ttu-id="918df-113"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="918df-113"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="918df-p103">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="918df-p103">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="918df-p104">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="918df-p104">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="918df-p105">Pour commencer, accédez à la page de vos domaines sur le site MyDomain en utilisant [ce lien](https://www.mydomain.com/controlpanel). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="918df-p105">To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="918df-120">Dans la rubrique **Mes favoris**, choisissez **Domaine central**.</span><span class="sxs-lookup"><span data-stu-id="918df-120">In the **My Favorites** section, select **Domain Central**.</span></span>
    
3. <span data-ttu-id="918df-121">Sous **Domaine**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="918df-121">Under **Domain**, select the name of the domain that you want to edit.</span></span>
    
4. <span data-ttu-id="918df-122">Sur la ligne de la **Vue d'ensemble**, choisissez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="918df-122">In the **Overview** row, select **DNS**.</span></span>
    
5. <span data-ttu-id="918df-123">Dans la liste déroulante **Modifier**, sélectionnez **Enregistrement TXT/SPF**.</span><span class="sxs-lookup"><span data-stu-id="918df-123">From the **Modify** drop-down list, choose **TXT/SPF Record**.</span></span>
    
6. <span data-ttu-id="918df-124">Sous **Content (Contenu)**, dans la zone du nouvel enregistrement, tapez ou copiez-collez la valeur du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="918df-124">Under **Content**, in the box for the new record, type or copy and paste the value from the following table.</span></span>
    
    ||
    |:-----|
    |<span data-ttu-id="918df-125">**Content**</span><span class="sxs-lookup"><span data-stu-id="918df-125">**Content**</span></span> <br/> |
    |<span data-ttu-id="918df-126">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="918df-126">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="918df-127">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="918df-127">**Note:** This is an example.</span></span> <span data-ttu-id="918df-128">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="918df-128">Use your specific **Destination or Points to Address** value here, from the table.</span></span> [<span data-ttu-id="918df-129">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="918df-129">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
7. <span data-ttu-id="918df-130">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="918df-130">Select **Add**.</span></span>
    
8. <span data-ttu-id="918df-131">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="918df-131">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="918df-132">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="918df-132">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="918df-133">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="918df-133">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="918df-134">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="918df-134">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="918df-135">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="918df-135">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="918df-136">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="918df-136">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="918df-137">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="918df-137">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="918df-138">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="918df-138">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="918df-139">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="918df-139">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="918df-140">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="918df-140">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="918df-141">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="918df-141">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="918df-142"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="918df-142"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="918df-p108">Pour commencer, accédez à la page de vos domaines sur le site MyDomain en utilisant [ce lien](https://www.mydomain.com/controlpanel). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="918df-p108">To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="918df-145">Dans la rubrique **Mes favoris**, choisissez **Domaine central**.</span><span class="sxs-lookup"><span data-stu-id="918df-145">In the **My Favorites** section, select **Domain Central**.</span></span>
    
3. <span data-ttu-id="918df-146">Sous **Domaine**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="918df-146">Under **Domain**, select the name of the domain that you want to edit.</span></span>
    
4. <span data-ttu-id="918df-147">Sur la ligne de la **Vue d'ensemble**, choisissez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="918df-147">In the **Overview** row, select **DNS**.</span></span>
    
5. <span data-ttu-id="918df-148">Dans la liste déroulante **Modify** (Modifier), sélectionnez **MX Record** (Enregistrement MX).</span><span class="sxs-lookup"><span data-stu-id="918df-148">From the **Modify** drop-down list, choose **MX Record**.</span></span>
    
    ![MyDomain-BP-Configure-2-1](../../media/bbfba978-8c53-471b-8c9e-8ae62e559d15.png)
  
6. <span data-ttu-id="918df-150">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="918df-150">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="918df-151">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="918df-151">**Priority**</span></span>|<span data-ttu-id="918df-152">**Host**</span><span class="sxs-lookup"><span data-stu-id="918df-152">**Host**</span></span>|<span data-ttu-id="918df-153">**Points to: (Pointe vers :)**</span><span class="sxs-lookup"><span data-stu-id="918df-153">**Points To:**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="918df-154">0</span><span class="sxs-lookup"><span data-stu-id="918df-154">0</span></span>  <br/> <span data-ttu-id="918df-155">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span><span class="sxs-lookup"><span data-stu-id="918df-155">For more information about priority, see [What is MX priority?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span></span> <br/> |@  <br/> | <span data-ttu-id="918df-156">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="918df-156">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="918df-157">**Remarque :** Obtenez votre \<*domain-key*\> à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="918df-157">**Note:** Get your \<*domain-key*\> from your Microsoft account.</span></span><span data-ttu-id="918df-158"> > [Comment puis-je trouver ceci ?](../get-help-with-domains/information-for-dns-records.md)</span><span class="sxs-lookup"><span data-stu-id="918df-158"> > [How do I find this?](../get-help-with-domains/information-for-dns-records.md)</span></span>          |
   
    ![MyDomain-BP-Configure-2-2](../../media/3e19cec3-7f3b-493d-81f7-cda30ba007d5.png)
  
7. <span data-ttu-id="918df-160">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="918df-160">Select **Add**.</span></span>
    
    ![MyDomain-BP-Configure-2-3](../../media/1a1951a8-11d7-405d-bef5-285bbb053ce8.png)
  
8. <span data-ttu-id="918df-162">S’il existe d’autres enregistrements MX, sélectionnez **Remove** (Supprimer) dans la colonne **Action** pour chacun d’eux afin de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="918df-162">If there are any other existing MX records, select **Remove** in the **Action** column for each one to delete it.</span></span> 
    
    ![MyDomain-BP-Configure-2-4](../../media/42576149-e056-4a81-a5fd-2c5dfac44e2e.png)
  
9. <span data-ttu-id="918df-164">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="918df-164">Select **OK**.</span></span>
    
    ![MyDomain-BP-Configure-2-5](../../media/d6b70eb7-b79c-499e-82ff-ecef2e300368.png)
  
## <a name="add-the-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="918df-166">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="918df-166">Add the CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="918df-167"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="918df-167"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="918df-p110">Pour commencer, accédez à la page de vos domaines sur le site MyDomain en utilisant [ce lien](https://www.mydomain.com/controlpanel). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="918df-p110">To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="918df-170">Dans la rubrique **Mes favoris**, choisissez **Domaine central**.</span><span class="sxs-lookup"><span data-stu-id="918df-170">In the **My Favorites** section, select **Domain Central**.</span></span>
    
3. <span data-ttu-id="918df-171">Sous **Domaine**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="918df-171">Under **Domain**, select the name of the domain that you want to edit.</span></span>
    
4. <span data-ttu-id="918df-172">Sur la ligne de la **Vue d'ensemble**, choisissez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="918df-172">In the **Overview** row, select **DNS**.</span></span>
    
5. <span data-ttu-id="918df-173">Dans la liste déroulante **Modify** (Modifier), sélectionnez **CNAME Alias** (Alias CNAME).</span><span class="sxs-lookup"><span data-stu-id="918df-173">From the **Modify** drop-down list, choose **CNAME Alias**.</span></span>
    
    ![MyDomain-BP-Configure-3-1](../../media/628267fc-d37b-42ef-bb92-265284e339ac.png)
  
6. <span data-ttu-id="918df-175">Ajoutez le premier enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="918df-175">Add the first CNAME record.</span></span>
    
    <span data-ttu-id="918df-176">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="918df-176">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span>
    
    |<span data-ttu-id="918df-177">**Host**</span><span class="sxs-lookup"><span data-stu-id="918df-177">**Host**</span></span>|<span data-ttu-id="918df-178">**Points to: (Pointe vers :)**</span><span class="sxs-lookup"><span data-stu-id="918df-178">**Points To:**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="918df-179">autodiscover</span><span class="sxs-lookup"><span data-stu-id="918df-179">autodiscover</span></span>  <br/> |<span data-ttu-id="918df-180">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="918df-180">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="918df-181">sip</span><span class="sxs-lookup"><span data-stu-id="918df-181">sip</span></span>  <br/> |<span data-ttu-id="918df-182">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="918df-182">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="918df-183">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="918df-183">lyncdiscover</span></span>  <br/> |<span data-ttu-id="918df-184">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="918df-184">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="918df-185">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="918df-185">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="918df-186">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="918df-186">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="918df-187">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="918df-187">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="918df-188">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="918df-188">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
   
    ![MyDomain-BP-Configure-3-2](../../media/3c8660b3-40bb-453d-8b99-4d22032bc4b3.png)
  
7. <span data-ttu-id="918df-190">Sélectionnez **Ajouter** pour ajouter le premier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="918df-190">Select **Add** to add the first record.</span></span> 
    
    ![MyDomain-BP-Configure-3-3](../../media/103a1d99-70da-4fdf-9291-7dd058ec6c4a.png)
  
8. <span data-ttu-id="918df-192">Ajoutez le deuxième enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="918df-192">Add the second CNAME record.</span></span>
    
    <span data-ttu-id="918df-193">Utilisez les valeurs de la deuxième ligne du tableau ci-dessus, puis choisissez **Ajouter** pour ajouter le deuxième enregistrement.</span><span class="sxs-lookup"><span data-stu-id="918df-193">Use the values from the second row of the table above, and then select **Add** to add the second record.</span></span> 
    
    <span data-ttu-id="918df-194">Ajoutez les enregistrements restants de la même manière, en utilisant les valeurs des troisième, quatrième, cinquième et sixième lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="918df-194">Add the remaining records in the same way, using the values from the third, fourth, fifth, and sixth rows of the table.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="918df-195">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="918df-195">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="918df-196"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="918df-196"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="918df-197">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="918df-197">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="918df-198">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="918df-198">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="918df-199">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="918df-199">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="918df-200">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel de manière à n’avoir qu’un seul enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="918df-200">Instead, add the required Microsoft values to the current record so that you have a single SPF record that includes both sets of values.</span></span> <span data-ttu-id="918df-201">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="918df-201">Need examples?</span></span> <span data-ttu-id="918df-202">Consultez ces [Enregistrements DNS externes pour Microsoft](https://docs.microsoft.com/microsoft-365/enterprise/external-domain-name-system-records#bkmk_spfrecords).</span><span class="sxs-lookup"><span data-stu-id="918df-202">Check out these [External Domain Name System records for Microsoft](https://docs.microsoft.com/microsoft-365/enterprise/external-domain-name-system-records#bkmk_spfrecords).</span></span> <span data-ttu-id="918df-203">To validate your SPF record, you can use one of these [SPF validation tools](../setup/domains-faq.md).</span><span class="sxs-lookup"><span data-stu-id="918df-203">To validate your SPF record, you can use one of these [SPF validation tools](../setup/domains-faq.md).</span></span> 
  
1. <span data-ttu-id="918df-p112">Pour commencer, accédez à la page de vos domaines sur le site MyDomain en utilisant [ce lien](https://www.mydomain.com/controlpanel). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="918df-p112">To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="918df-206">Dans la rubrique **Mes favoris**, choisissez **Domaine central**.</span><span class="sxs-lookup"><span data-stu-id="918df-206">In the **My Favorites** section, select **Domain Central**.</span></span>
    
3. <span data-ttu-id="918df-207">Sous **Domaine**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="918df-207">Under **Domain**, select the name of the domain that you want to edit.</span></span>
    
4. <span data-ttu-id="918df-208">Sur la ligne de la **Vue d'ensemble**, choisissez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="918df-208">In the **Overview** row, select **DNS**.</span></span>
    
5. <span data-ttu-id="918df-209">Dans la liste déroulante **Modify (Modifier)**, sélectionnez **TXT/SPF Record (Enregistrement TXT/SPF)**.</span><span class="sxs-lookup"><span data-stu-id="918df-209">From the **Modify** drop-down list, choose **TXT/SPF Record**.</span></span>
    
    ![MyDomain-BP-Configure-4-1](../../media/c461c762-52e6-4fde-b5bc-4dd5e5d62ed3.png)
  
6. <span data-ttu-id="918df-211">Sous **Content (Contenu)**, dans la zone du nouvel enregistrement, tapez ou copiez-collez la valeur du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="918df-211">Under **Content**, in the box for the new record, type or copy and paste the value from the following table.</span></span>
    
    |<span data-ttu-id="918df-212">**Content**</span><span class="sxs-lookup"><span data-stu-id="918df-212">**Content**</span></span>|
    |:-----|
    |<span data-ttu-id="918df-213">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="918df-213">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="918df-214">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="918df-214">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![MyDomain-BP-Configure-4-2](../../media/17d43106-88e6-47e5-aeba-0f18484acf3e.png)
  
7. <span data-ttu-id="918df-216">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="918df-216">Select **Add**.</span></span>
    
    ![MyDomain-BP-Configure-4-3](../../media/b3670563-b620-470c-a42b-2c77888981f8.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="918df-218">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="918df-218">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="918df-219"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="918df-219"><a name="BKMK_add_SRV"> </a></span></span>

> [!CAUTION]
> <span data-ttu-id="918df-p113">Le site web MyDomain ne prend pas en charge les enregistrements SRV, ce qui signifie que plusieurs fonctionnalités de Skype Entreprise Online et d’Outlook Web App ne fonctionnent pas. Quelle que soit l’offre Microsoft que vous utilisez, si vous gérez vos enregistrements DNS via MyDomain, il existe des [limitations de service importantes](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq). Le cas échéant, vous pouvez basculer vers un autre fournisseur d’hébergement DNS.</span><span class="sxs-lookup"><span data-stu-id="918df-p113">The MyDomain website doesn't support SRV records, which means several Skype for Business Online and Outlook Web App features won't work. No matter which Microsoft plan you use, if you manage your DNS records at MyDomain, there are [significant service limitations](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq), and you might want to switch to a different DNS hosting provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="918df-222">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="918df-222">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="918df-223">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="918df-223">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="918df-224">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="918df-224">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
