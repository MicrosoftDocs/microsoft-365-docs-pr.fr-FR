---
title: Créer des enregistrements DNS auprès de MyDomain pour Office 365
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 9982191d-ed79-46a9-b2e7-317d1a3a9867
description: Apprenez à vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online et les autres services sur MyDomain pour Office 365.
ms.openlocfilehash: c85c04d369add95d3aaa815229257fe90a24fb28
ms.sourcegitcommit: 812aab5f58eed4bf359faf0e99f7f876af5b1023
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/02/2020
ms.locfileid: "42349863"
---
# <a name="create-dns-records-at-mydomain-for-office-365"></a><span data-ttu-id="494b0-103">Créer des enregistrements DNS auprès de MyDomain pour Office 365</span><span class="sxs-lookup"><span data-stu-id="494b0-103">Create DNS records at MyDomain for Office 365</span></span>


  
 <span data-ttu-id="494b0-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="494b0-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="494b0-p101">Le site web MyDomain ne prend pas en charge les enregistrements SRV, ce qui signifie que plusieurs fonctionnalités de Skype Entreprise Online et d'Outlook Web App ne fonctionnent pas. Quelle que soit l'offre Office 365 que vous utilisez, si vous gérez vos enregistrements DNS via MyDomain, il existe des [limitations de service importantes](https://support.office.com/article/7ae9a655-041d-4724-aa92-60392ee390c2.aspx). Le cas échéant, vous pouvez basculer vers un autre fournisseur d'hébergement DNS.</span><span class="sxs-lookup"><span data-stu-id="494b0-p101">The MyDomain website doesn't support SRV records, which means several Skype for Business Online and Outlook Web App features won't work. No matter which Office 365 plan you use, if you manage your DNS records at MyDomain, there are [significant service limitations](https://support.office.com/article/7ae9a655-041d-4724-aa92-60392ee390c2.aspx), and you might want to switch to a different DNS hosting provider.</span></span> 
  
<span data-ttu-id="494b0-107">Si vous décidez de gérer vos propres enregistrements DNS Office 365 via MyDomain malgré ces limitations de service, procédez de la manière décrite dans cet article pour configurer vos enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="494b0-107">If you choose to manage your own Office 365 DNS records at MyDomain despite the service limitations, follow the steps in this article to set up your DNS records for email, Skype for Business Online, and so on.</span></span>
    
<span data-ttu-id="494b0-108">Une fois ces enregistrements ajoutés sur MyDomain, votre domaine est configuré pour utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="494b0-108">After you add these records at MyDomain, your domain will be set up to work with Office 365 services.</span></span>
  
<span data-ttu-id="494b0-109">Pour en savoir plus sur l'hébergement web et le DNS pour les sites web avec Office 365, voir [Utiliser un site web public avec Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span><span class="sxs-lookup"><span data-stu-id="494b0-109">To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span></span>
  
> [!NOTE]
> <span data-ttu-id="494b0-110">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="494b0-110">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="494b0-111">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="494b0-111">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="494b0-112">Si vous rencontrez des difficultés avec le flux de courrier ou d'autres problèmes suite à l'ajout des enregistrements DNS, consultez [Rechercher et corriger les problèmes suite à l'ajout de votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="494b0-112">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="494b0-113">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="494b0-113">Add a TXT record for verification</span></span>
<span data-ttu-id="494b0-114"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="494b0-114"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="494b0-p103">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="494b0-p103">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="494b0-p104">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="494b0-p104">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="494b0-p105">Pour commencer, accédez à la page de vos domaines sur le site MyDomain en utilisant [ce lien](https://www.mydomain.com/controlpanel). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="494b0-p105">To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="494b0-121">Dans la rubrique **Mes favoris**, choisissez **Domaine central**.</span><span class="sxs-lookup"><span data-stu-id="494b0-121">In the **My Favorites** section, select **Domain Central**.</span></span>
    
3. <span data-ttu-id="494b0-122">Sous **Domaine**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="494b0-122">Under **Domain**, select the name of the domain that you want to edit.</span></span>
    
4. <span data-ttu-id="494b0-123">Sur la ligne de la **Vue d'ensemble**, choisissez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="494b0-123">In the **Overview** row, select **DNS**.</span></span>
    
5. <span data-ttu-id="494b0-124">Dans la liste déroulante **Modifier**, sélectionnez **Enregistrement TXT/SPF**.</span><span class="sxs-lookup"><span data-stu-id="494b0-124">From the **Modify** drop-down list, choose **TXT/SPF Record**.</span></span>
    
6. <span data-ttu-id="494b0-125">Sous **Content (Contenu)**, dans la zone du nouvel enregistrement, tapez ou copiez-collez la valeur du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="494b0-125">Under **Content**, in the box for the new record, type or copy and paste the value from the following table.</span></span>
    
    ||
    |:-----|
    |<span data-ttu-id="494b0-126">**Content**</span><span class="sxs-lookup"><span data-stu-id="494b0-126">**Content**</span></span> <br/> |
    |<span data-ttu-id="494b0-127">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="494b0-127">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="494b0-128">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="494b0-128">**Note:** This is an example.</span></span> <span data-ttu-id="494b0-129">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="494b0-129">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span> [<span data-ttu-id="494b0-130">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="494b0-130">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
7. <span data-ttu-id="494b0-131">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="494b0-131">Select **Add**.</span></span>
    
8. <span data-ttu-id="494b0-132">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="494b0-132">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="494b0-133">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Office 365 et demandez à Office 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="494b0-133">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="494b0-134">Lorsqu’Office 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="494b0-134">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="494b0-135">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="494b0-135">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="494b0-136">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="494b0-136">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="494b0-137">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="494b0-137">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="494b0-138">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="494b0-138">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="494b0-139">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="494b0-139">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="494b0-140">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="494b0-140">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="494b0-141">Si vous rencontrez des difficultés avec le flux de courrier ou d'autres problèmes suite à l'ajout des enregistrements DNS, consultez [Rechercher et corriger les problèmes suite à l'ajout de votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="494b0-141">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="494b0-142">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="494b0-142">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="494b0-143"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="494b0-143"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="494b0-p108">Pour commencer, accédez à la page de vos domaines sur le site MyDomain en utilisant [ce lien](https://www.mydomain.com/controlpanel). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="494b0-p108">To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="494b0-146">Dans la rubrique **Mes favoris**, choisissez **Domaine central**.</span><span class="sxs-lookup"><span data-stu-id="494b0-146">In the **My Favorites** section, select **Domain Central**.</span></span>
    
3. <span data-ttu-id="494b0-147">Sous **Domaine**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="494b0-147">Under **Domain**, select the name of the domain that you want to edit.</span></span>
    
4. <span data-ttu-id="494b0-148">Sur la ligne de la **Vue d'ensemble**, choisissez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="494b0-148">In the **Overview** row, select **DNS**.</span></span>
    
5. <span data-ttu-id="494b0-149">Dans la liste déroulante **Modify** (Modifier), sélectionnez **MX Record** (Enregistrement MX).</span><span class="sxs-lookup"><span data-stu-id="494b0-149">From the **Modify** drop-down list, choose **MX Record**.</span></span>
    
    ![MyDomain-BP-Configure-2-1](../../media/bbfba978-8c53-471b-8c9e-8ae62e559d15.png)
  
6. <span data-ttu-id="494b0-151">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="494b0-151">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="494b0-152">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="494b0-152">**Priority**</span></span>|<span data-ttu-id="494b0-153">**Host**</span><span class="sxs-lookup"><span data-stu-id="494b0-153">**Host**</span></span>|<span data-ttu-id="494b0-154">**Points to: (Pointe vers :)**</span><span class="sxs-lookup"><span data-stu-id="494b0-154">**Points To:**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="494b0-155">0</span><span class="sxs-lookup"><span data-stu-id="494b0-155">0</span></span>  <br/> <span data-ttu-id="494b0-156">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="494b0-156">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> |@  <br/> | <span data-ttu-id="494b0-157">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="494b0-157">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="494b0-158">**Remarque :** Obtenez votre \<*clé de domaine*\> à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="494b0-158">**Note:** Get your \<*domain-key*\> from your Office 365 account.</span></span><span data-ttu-id="494b0-159"> > [Comment puis-je trouver ceci ?](../get-help-with-domains/information-for-dns-records.md)</span><span class="sxs-lookup"><span data-stu-id="494b0-159"> > [How do I find this?](../get-help-with-domains/information-for-dns-records.md)</span></span>          |
   
    ![MyDomain-BP-Configure-2-2](../../media/3e19cec3-7f3b-493d-81f7-cda30ba007d5.png)
  
7. <span data-ttu-id="494b0-161">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="494b0-161">Select **Add**.</span></span>
    
    ![MyDomain-BP-Configure-2-3](../../media/1a1951a8-11d7-405d-bef5-285bbb053ce8.png)
  
8. <span data-ttu-id="494b0-163">S’il existe d’autres enregistrements MX, sélectionnez **Remove** (Supprimer) dans la colonne **Action** pour chacun d’eux afin de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="494b0-163">If there are any other existing MX records, select **Remove** in the **Action** column for each one to delete it.</span></span> 
    
    ![MyDomain-BP-Configure-2-4](../../media/42576149-e056-4a81-a5fd-2c5dfac44e2e.png)
  
9. <span data-ttu-id="494b0-165">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="494b0-165">Select **OK**.</span></span>
    
    ![MyDomain-BP-Configure-2-5](../../media/d6b70eb7-b79c-499e-82ff-ecef2e300368.png)
  
## <a name="add-the-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="494b0-167">Ajouter les enregistrements CNAME requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="494b0-167">Add the CNAME records that are required for Office 365</span></span>
<span data-ttu-id="494b0-168"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="494b0-168"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="494b0-p110">Pour commencer, accédez à la page de vos domaines sur le site MyDomain en utilisant [ce lien](https://www.mydomain.com/controlpanel). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="494b0-p110">To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="494b0-171">Dans la rubrique **Mes favoris**, choisissez **Domaine central**.</span><span class="sxs-lookup"><span data-stu-id="494b0-171">In the **My Favorites** section, select **Domain Central**.</span></span>
    
3. <span data-ttu-id="494b0-172">Sous **Domaine**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="494b0-172">Under **Domain**, select the name of the domain that you want to edit.</span></span>
    
4. <span data-ttu-id="494b0-173">Sur la ligne de la **Vue d'ensemble**, choisissez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="494b0-173">In the **Overview** row, select **DNS**.</span></span>
    
5. <span data-ttu-id="494b0-174">Dans la liste déroulante **Modify** (Modifier), sélectionnez **CNAME Alias** (Alias CNAME).</span><span class="sxs-lookup"><span data-stu-id="494b0-174">From the **Modify** drop-down list, choose **CNAME Alias**.</span></span>
    
    ![MyDomain-BP-Configure-3-1](../../media/628267fc-d37b-42ef-bb92-265284e339ac.png)
  
6. <span data-ttu-id="494b0-176">Ajoutez le premier enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="494b0-176">Add the first CNAME record.</span></span>
    
    <span data-ttu-id="494b0-177">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="494b0-177">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span>
    
    |<span data-ttu-id="494b0-178">**Host**</span><span class="sxs-lookup"><span data-stu-id="494b0-178">**Host**</span></span>|<span data-ttu-id="494b0-179">**Points to: (Pointe vers :)**</span><span class="sxs-lookup"><span data-stu-id="494b0-179">**Points To:**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="494b0-180">autodiscover</span><span class="sxs-lookup"><span data-stu-id="494b0-180">autodiscover</span></span>  <br/> |<span data-ttu-id="494b0-181">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="494b0-181">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="494b0-182">sip</span><span class="sxs-lookup"><span data-stu-id="494b0-182">sip</span></span>  <br/> |<span data-ttu-id="494b0-183">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="494b0-183">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="494b0-184">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="494b0-184">lyncdiscover</span></span>  <br/> |<span data-ttu-id="494b0-185">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="494b0-185">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="494b0-186">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="494b0-186">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="494b0-187">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="494b0-187">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="494b0-188">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="494b0-188">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="494b0-189">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="494b0-189">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
   
    ![MyDomain-BP-Configure-3-2](../../media/3c8660b3-40bb-453d-8b99-4d22032bc4b3.png)
  
7. <span data-ttu-id="494b0-191">Sélectionnez **Ajouter** pour ajouter le premier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="494b0-191">Select **Add** to add the first record.</span></span> 
    
    ![MyDomain-BP-Configure-3-3](../../media/103a1d99-70da-4fdf-9291-7dd058ec6c4a.png)
  
8. <span data-ttu-id="494b0-193">Ajoutez le deuxième enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="494b0-193">Add the second CNAME record.</span></span>
    
    <span data-ttu-id="494b0-194">Utilisez les valeurs de la deuxième ligne du tableau ci-dessus, puis choisissez **Ajouter** pour ajouter le deuxième enregistrement.</span><span class="sxs-lookup"><span data-stu-id="494b0-194">Use the values from the second row of the table above, and then select **Add** to add the second record.</span></span> 
    
    <span data-ttu-id="494b0-195">Ajoutez les enregistrements restants de la même manière, en utilisant les valeurs des troisième, quatrième, cinquième et sixième lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="494b0-195">Add the remaining records in the same way, using the values from the third, fourth, fifth, and sixth rows of the table.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="494b0-196">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="494b0-196">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="494b0-197"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="494b0-197"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="494b0-198">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="494b0-198">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="494b0-199">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="494b0-199">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="494b0-200">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="494b0-200">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="494b0-201">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un seul enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="494b0-201">Instead, add the required Office 365 values to the current record so that you have a single SPF record that includes both sets of values.</span></span> <span data-ttu-id="494b0-202">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="494b0-202">Need examples?</span></span> <span data-ttu-id="494b0-203">Consultez ces [Enregistrements DNS externes pour Office 365](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0#bkmk_spfrecords).</span><span class="sxs-lookup"><span data-stu-id="494b0-203">Check out these [External Domain Name System records for Office 365](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0#bkmk_spfrecords).</span></span> <span data-ttu-id="494b0-204">To validate your SPF record, you can use one of these [SPF validation tools](../setup/domains-faq.md).</span><span class="sxs-lookup"><span data-stu-id="494b0-204">To validate your SPF record, you can use one of these [SPF validation tools](../setup/domains-faq.md).</span></span> 
  
1. <span data-ttu-id="494b0-p112">Pour commencer, accédez à la page de vos domaines sur le site MyDomain en utilisant [ce lien](https://www.mydomain.com/controlpanel). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="494b0-p112">To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="494b0-207">Dans la rubrique **Mes favoris**, choisissez **Domaine central**.</span><span class="sxs-lookup"><span data-stu-id="494b0-207">In the **My Favorites** section, select **Domain Central**.</span></span>
    
3. <span data-ttu-id="494b0-208">Sous **Domaine**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="494b0-208">Under **Domain**, select the name of the domain that you want to edit.</span></span>
    
4. <span data-ttu-id="494b0-209">Sur la ligne de la **Vue d'ensemble**, choisissez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="494b0-209">In the **Overview** row, select **DNS**.</span></span>
    
5. <span data-ttu-id="494b0-210">Dans la liste déroulante **Modify (Modifier)**, sélectionnez **TXT/SPF Record (Enregistrement TXT/SPF)**.</span><span class="sxs-lookup"><span data-stu-id="494b0-210">From the **Modify** drop-down list, choose **TXT/SPF Record**.</span></span>
    
    ![MyDomain-BP-Configure-4-1](../../media/c461c762-52e6-4fde-b5bc-4dd5e5d62ed3.png)
  
6. <span data-ttu-id="494b0-212">Sous **Content (Contenu)**, dans la zone du nouvel enregistrement, tapez ou copiez-collez la valeur du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="494b0-212">Under **Content**, in the box for the new record, type or copy and paste the value from the following table.</span></span>
    
    |<span data-ttu-id="494b0-213">**Content**</span><span class="sxs-lookup"><span data-stu-id="494b0-213">**Content**</span></span>|
    |:-----|
    |<span data-ttu-id="494b0-214">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="494b0-214">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="494b0-215">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="494b0-215">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![MyDomain-BP-Configure-4-2](../../media/17d43106-88e6-47e5-aeba-0f18484acf3e.png)
  
7. <span data-ttu-id="494b0-217">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="494b0-217">Select **Add**.</span></span>
    
    ![MyDomain-BP-Configure-4-3](../../media/b3670563-b620-470c-a42b-2c77888981f8.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="494b0-219">Ajoutez les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="494b0-219">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="494b0-220"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="494b0-220"><a name="BKMK_add_SRV"> </a></span></span>

> [!CAUTION]
> <span data-ttu-id="494b0-p113">Le site web MyDomain ne prend pas en charge les enregistrements SRV, ce qui signifie que plusieurs fonctionnalités de Skype Entreprise Online et d'Outlook Web App ne fonctionnent pas. Quelle que soit l'offre Office 365 que vous utilisez, si vous gérez vos enregistrements DNS via MyDomain, il existe des [limitations de service importantes](https://support.office.com/article/7ae9a655-041d-4724-aa92-60392ee390c2.aspx). Le cas échéant, vous pouvez basculer vers un autre fournisseur d'hébergement DNS.</span><span class="sxs-lookup"><span data-stu-id="494b0-p113">The MyDomain website doesn't support SRV records, which means several Skype for Business Online and Outlook Web App features won't work. No matter which Office 365 plan you use, if you manage your DNS records at MyDomain, there are [significant service limitations](https://support.office.com/article/7ae9a655-041d-4724-aa92-60392ee390c2.aspx), and you might want to switch to a different DNS hosting provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="494b0-223">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="494b0-223">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="494b0-224">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="494b0-224">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="494b0-225">Si vous rencontrez des difficultés avec le flux de courrier ou d'autres problèmes suite à l'ajout des enregistrements DNS, consultez [Rechercher et corriger les problèmes suite à l'ajout de votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="494b0-225">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
