---
title: Créer des enregistrements DNS à des domaines bizarres pour Microsoft
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
ms.assetid: 6386d63e-b78f-4736-90e7-b99a2c116a9f
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour le courrier électronique, Skype entreprise Online et d’autres services sur des domaines folles pour Microsoft.
ms.openlocfilehash: af154db43f486f71443497180fe64cff89e11b5f
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44400532"
---
# <a name="create-dns-records-at-crazy-domains-for-microsoft"></a><span data-ttu-id="6c802-103">Créer des enregistrements DNS à des domaines bizarres pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="6c802-103">Create DNS records at Crazy Domains for Microsoft</span></span>

 <span data-ttu-id="6c802-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="6c802-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="6c802-105">Si Crazy Domains est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="6c802-105">If Crazy Domains is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="6c802-106">Une fois que vous avez ajouté ces enregistrements à des domaines bizarres, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6c802-106">After you add these records at Crazy Domains, your domain will be set up to work with Microsoft services.</span></span>
  

  
> [!NOTE]
> <span data-ttu-id="6c802-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="6c802-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="6c802-110">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="6c802-110">Add a TXT record for verification</span></span>
<span data-ttu-id="6c802-111"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="6c802-111"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="6c802-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="6c802-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6c802-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="6c802-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="6c802-p104">Pour commencer, accédez à la page de vos domaines sur le site Crazy Domains en utilisant [ce lien](https://manage.crazydomains.com/members/domains/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="6c802-p104">To get started, go to your domains page at Crazy Domains by using [this link](https://manage.crazydomains.com/members/domains/). You'll be prompted to log in first.</span></span>
    
    ![CrazyDomains-BP-configure-1-1](../../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. <span data-ttu-id="6c802-119">Dans la section **mon compte** , sélectionnez **domaines**.</span><span class="sxs-lookup"><span data-stu-id="6c802-119">In the **My Account** section, select **Domains**.</span></span>
    
    ![CrazyDomains-BP-configure-1-2](../../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. <span data-ttu-id="6c802-121">Dans la page **noms de domaine** , dans la section **domaine** , sélectionnez le nom du domaine que vous mettez à jour.</span><span class="sxs-lookup"><span data-stu-id="6c802-121">On the **Domain Names** page, in the **Domain** section, select the name of the domain that you are updating.</span></span> 
    
    ![CrazyDomains-BP-configure-1-3](../../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. <span data-ttu-id="6c802-123">Dans la section **paramètres DNS** , sélectionnez l’icône de la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6c802-123">In the **DNS Settings** section, select the drop-down list icon.</span></span> 
    
    ![CrazyDomains-BP-configure-1-4-1](../../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. <span data-ttu-id="6c802-125">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="6c802-125">Select **Add Record**.</span></span>
    
    ![CrazyDomains-BP-configure-1-4-2](../../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. <span data-ttu-id="6c802-127">Choisissez **Enregistrement TXT** dans la liste déroulante **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="6c802-127">Choose **TXT Record** from the **Add Record** drop-down list.</span></span> 
    
    ![CrazyDomains-BP-Verify-1-1](../../media/f0ffdefb-d7a5-47df-bb5e-bf8a3bcc9b01.png)
  
7. <span data-ttu-id="6c802-129">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6c802-129">Select **Add**.</span></span>
    
    ![CrazyDomains-BP-Verify-1-2](../../media/b0cd623a-67f7-4bae-a5b5-507f5a106123.png)
  
8. <span data-ttu-id="6c802-131">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6c802-131">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="6c802-132">**Sub Domain (Sous-domaine)**</span><span class="sxs-lookup"><span data-stu-id="6c802-132">**Sub Domain**</span></span>|<span data-ttu-id="6c802-133">**Text Record (Enregistrement texte)**</span><span class="sxs-lookup"><span data-stu-id="6c802-133">**Text Record**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="6c802-134">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="6c802-134">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="6c802-135">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="6c802-135">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="6c802-136">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="6c802-136">**Note:** This is an example.</span></span> <span data-ttu-id="6c802-137">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="6c802-137">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="6c802-138">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="6c802-138">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![CrazyDomains-BP-Verify-1-3](../../media/3867de97-6a98-4475-9bda-470bac75d483.png)
  
9. <span data-ttu-id="6c802-140">Sélectionnez **Mettre à jour**.</span><span class="sxs-lookup"><span data-stu-id="6c802-140">Select **Update**.</span></span>
    
    ![CrazyDomains-BP-Verify-1-4](../../media/0e416df6-b7a2-4dd7-971c-f1cc31df30da.png)
  
10. <span data-ttu-id="6c802-142">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="6c802-142">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="6c802-143">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6c802-143">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="6c802-144">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="6c802-144">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="6c802-145">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="6c802-145">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="6c802-146">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="6c802-146">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="6c802-147">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="6c802-147">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="6c802-148">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="6c802-148">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="6c802-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="6c802-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="6c802-152">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="6c802-152">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="6c802-153"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="6c802-153"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="6c802-p107">Pour commencer, accédez à la page de vos domaines sur le site Crazy Domains en utilisant [ce lien](https://manage.crazydomains.com/members/domains/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="6c802-p107">To get started, go to your domains page at Crazy Domains by using [this link](https://manage.crazydomains.com/members/domains/). You'll be prompted to log in first.</span></span>
    
    ![CrazyDomains-BP-configure-1-1](../../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. <span data-ttu-id="6c802-157">Dans la section **mon compte** , sélectionnez **domaines**.</span><span class="sxs-lookup"><span data-stu-id="6c802-157">In the **My Account** section, select **Domains**.</span></span>
    
    ![CrazyDomains-BP-configure-1-2](../../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. <span data-ttu-id="6c802-159">Dans la page **noms de domaine** , dans la section **domaine** , sélectionnez le nom du domaine que vous mettez à jour.</span><span class="sxs-lookup"><span data-stu-id="6c802-159">On the **Domain Names** page, in the **Domain** section, select the name of the domain that you are updating.</span></span> 
    
    ![CrazyDomains-BP-configure-1-3](../../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. <span data-ttu-id="6c802-161">Dans la section **paramètres DNS** , sélectionnez l’icône de la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6c802-161">In the **DNS Settings** section, select the drop-down list icon.</span></span> 
    
    ![CrazyDomains-BP-configure-1-4-1](../../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. <span data-ttu-id="6c802-163">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="6c802-163">Select **Add Record**.</span></span>
    
    ![CrazyDomains-BP-configure-1-4-2](../../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. <span data-ttu-id="6c802-165">Choisissez **MX Record** (Enregistrement MX) dans la liste déroulante **Add Record** (Ajouter un enregistrement).</span><span class="sxs-lookup"><span data-stu-id="6c802-165">Choose **MX Record** from the **Add Record:** drop-down list.</span></span> 
    
    ![CrazyDomains-BP-configure-2-1](../../media/63f7ab77-e686-4e7b-a3a2-1ac28a02d5f3.png)
  
7. <span data-ttu-id="6c802-167">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6c802-167">Select **Add**.</span></span>
    
    ![CrazyDomains-BP-configure-2-2](../../media/a60680a1-2513-498c-b42f-8ffa575ee48e.png)
  
8. <span data-ttu-id="6c802-169">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6c802-169">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="6c802-170">(Choisissez la valeur **Priority** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="6c802-170">(Choose the **Priority** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="6c802-171">**Mail For Zone (Courrier pour la zone)**</span><span class="sxs-lookup"><span data-stu-id="6c802-171">**Mail For Zone**</span></span>|<span data-ttu-id="6c802-172">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="6c802-172">**Priority**</span></span>|<span data-ttu-id="6c802-173">**Assigned To Server (Affecté au serveur)**</span><span class="sxs-lookup"><span data-stu-id="6c802-173">**Assigned To Server**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="6c802-174">(Laissez ce champ vide.)</span><span class="sxs-lookup"><span data-stu-id="6c802-174">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="6c802-175">1 </span><span class="sxs-lookup"><span data-stu-id="6c802-175">1</span></span>  <br/> <span data-ttu-id="6c802-176">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span><span class="sxs-lookup"><span data-stu-id="6c802-176">For more information about priority, see [What is MX priority?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span></span> <br/> | <span data-ttu-id="6c802-177">*\<domain-key\>*. mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="6c802-177">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="6c802-178">**Remarque :** Obtenir votre *\<domain-key\>* à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6c802-178">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>           [<span data-ttu-id="6c802-179">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="6c802-179">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
       
   ![CrazyDomains-BP-configure-2-3](../../media/e27df6a6-19a6-4e58-9716-a74be1c3f8da.png)
  
9. <span data-ttu-id="6c802-181">Sélectionnez **Mettre à jour**.</span><span class="sxs-lookup"><span data-stu-id="6c802-181">Select **Update**.</span></span>
    
    ![CrazyDomains-BP-configure-2-4](../../media/ba25cdef-a436-48bf-b0e9-5dffd03234a4.png)
  
10. <span data-ttu-id="6c802-183">Si d’autres enregistrements MX sont répertoriés dans la section **MX record (enregistrement MX** ), sélectionnez **Modify (modifier** ) pour l’un de ces enregistrements.</span><span class="sxs-lookup"><span data-stu-id="6c802-183">If there are any other MX records listed in the **MX Record** section, select **Modify** for one of those records.</span></span> 
    
    ![CrazyDomains-BP-configure-2-5](../../media/9acdda39-33ec-4b24-ad83-91c26f9c599b.png)
  
11. <span data-ttu-id="6c802-185">Sélectionnez **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="6c802-185">Select **Delete**.</span></span>
    
    ![CrazyDomains-BP-configure-2-6](../../media/50b0e263-6f21-41b3-8fa0-7dd55dbe6c2e.png)
  
12. <span data-ttu-id="6c802-187">Sélectionnez **Update (mettre à jour** ) pour confirmer la suppression.</span><span class="sxs-lookup"><span data-stu-id="6c802-187">Select **Update** to confirm the deletion.</span></span> 
    
    ![CrazyDomains-BP-configure-2-7](../../media/db751bfe-31c2-4632-a491-6893eda38a51.png)
  
13. <span data-ttu-id="6c802-189">Procédez de la même manière pour supprimer tous les autres enregistrements MX de la liste, jusqu'à ce qu'il ne reste plus que celui que vous avez ajouté précédemment dans cette procédure.</span><span class="sxs-lookup"><span data-stu-id="6c802-189">Use the same process to remove any other MX records in the list, until only the one that you added earlier in this procedure remains.</span></span>
    
## <a name="add-the-six-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="6c802-190">Ajouter les six enregistrements CNAMe requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="6c802-190">Add the six CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="6c802-191"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="6c802-191"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="6c802-p109">Pour commencer, accédez à la page de vos domaines sur le site Crazy Domains en utilisant [ce lien](https://manage.crazydomains.com/members/domains/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="6c802-p109">To get started, go to your domains page at Crazy Domains by using [this link](https://manage.crazydomains.com/members/domains/). You'll be prompted to log in first.</span></span>
    
    ![CrazyDomains-BP-configure-1-1](../../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. <span data-ttu-id="6c802-195">Dans la section **mon compte** , sélectionnez **domaines**.</span><span class="sxs-lookup"><span data-stu-id="6c802-195">In the **My Account** section, select **Domains**.</span></span>
    
    ![CrazyDomains-BP-configure-1-2](../../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. <span data-ttu-id="6c802-197">Dans la page **noms de domaine** , dans la section **domaine** , sélectionnez le nom du domaine que vous mettez à jour.</span><span class="sxs-lookup"><span data-stu-id="6c802-197">On the **Domain Names** page, in the **Domain** section, select the name of the domain that you are updating.</span></span> 
    
    ![CrazyDomains-BP-configure-1-3](../../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. <span data-ttu-id="6c802-199">Dans la section **paramètres DNS** , sélectionnez l’icône de la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6c802-199">In the **DNS Settings** section, select the drop-down list icon.</span></span> 
    
    ![CrazyDomains-BP-configure-1-4-1](../../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. <span data-ttu-id="6c802-201">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="6c802-201">Select **Add Record**.</span></span>
    
    ![CrazyDomains-BP-configure-1-4-2](../../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. <span data-ttu-id="6c802-203">Choisissez **CNAME Record** (Enregistrement CNAME) dans la liste déroulante **Add Record** (Ajouter un enregistrement).</span><span class="sxs-lookup"><span data-stu-id="6c802-203">Choose **CNAME Record** from the **Add Record:** drop-down list.</span></span> 
    
    ![CrazyDomains-BP-configure-3-1](../../media/2f02538b-fc79-46d2-a2b7-1022eaf0fb08.png)
  
7. <span data-ttu-id="6c802-205">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6c802-205">Select **Add**.</span></span>
    
    ![CrazyDomains-BP-configure-3-2](../../media/4c5929cf-1c21-4af9-899b-e36091f0f14d.png)
  
8. <span data-ttu-id="6c802-207">Ajoutez le premier des six enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="6c802-207">Add the first of the six CNAME records.</span></span>
    
    <span data-ttu-id="6c802-208">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6c802-208">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span>
    
    |<span data-ttu-id="6c802-209">**Sub Domain (Sous-domaine)**</span><span class="sxs-lookup"><span data-stu-id="6c802-209">**Sub Domain**</span></span>|<span data-ttu-id="6c802-210">**Alias for (Alias pour)**</span><span class="sxs-lookup"><span data-stu-id="6c802-210">**Alias for**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="6c802-211">autodiscover</span><span class="sxs-lookup"><span data-stu-id="6c802-211">autodiscover</span></span>  <br/> |<span data-ttu-id="6c802-212">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="6c802-212">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="6c802-213">sip</span><span class="sxs-lookup"><span data-stu-id="6c802-213">sip</span></span>  <br/> |<span data-ttu-id="6c802-214">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="6c802-214">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="6c802-215">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="6c802-215">lyncdiscover</span></span>  <br/> |<span data-ttu-id="6c802-216">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="6c802-216">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="6c802-217">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="6c802-217">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="6c802-218">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="6c802-218">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="6c802-219">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="6c802-219">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="6c802-220">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="6c802-220">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
   
    ![CrazyDomains-BP-configure-3-3](../../media/81a7b837-3f4d-4565-89a9-380e4d318acf.png)
  
9. <span data-ttu-id="6c802-222">Sélectionnez **Ajouter un enregistrement CNAME**.</span><span class="sxs-lookup"><span data-stu-id="6c802-222">Select **Add CNAME Record**.</span></span>
    
    ![CrazyDomains-BP-configure-3-4](../../media/9bcba729-7085-4ebc-8183-ecde82f5c364.png)
  
10. <span data-ttu-id="6c802-224">Ajoutez le deuxième enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="6c802-224">Add the second CNAME record.</span></span>
    
    <span data-ttu-id="6c802-225">Dans les zones du nouvel enregistrement, utilisez les valeurs de la ligne suivante du tableau, puis sélectionnez de nouveau ajouter un **enregistrement CNAME**.</span><span class="sxs-lookup"><span data-stu-id="6c802-225">In the boxes for the new record, use the values from the next row in the table, and then again select **Add CNAME Record**.</span></span>
    
    <span data-ttu-id="6c802-226">Répétez cette procédure jusqu'à avoir créé les 6 enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="6c802-226">Repeat this process until you have created all six CNAME records.</span></span>
    
11. <span data-ttu-id="6c802-227">Sélectionnez **mettre à jour** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="6c802-227">Select **Update** to save your changes.</span></span> 
    
    ![CrazyDomains-BP-configure-3-5](../../media/dbe578f6-359c-428c-b296-ca624cecfc3c.png)
  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="6c802-229">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="6c802-229">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="6c802-230"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="6c802-230"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c802-231">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="6c802-231">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="6c802-232">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="6c802-232">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="6c802-233">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6c802-233">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="6c802-234">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="6c802-234">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
1. <span data-ttu-id="6c802-p111">Pour commencer, accédez à la page de vos domaines sur le site Crazy Domains en utilisant [ce lien](https://manage.crazydomains.com/members/domains/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="6c802-p111">To get started, go to your domains page at Crazy Domains by using [this link](https://manage.crazydomains.com/members/domains/). You'll be prompted to log in first.</span></span>
    
    ![CrazyDomains-BP-configure-1-1](../../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. <span data-ttu-id="6c802-238">Dans la section **mon compte** , sélectionnez **domaines**.</span><span class="sxs-lookup"><span data-stu-id="6c802-238">In the **My Account** section, select **Domains**.</span></span>
    
    ![CrazyDomains-BP-configure-1-2](../../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. <span data-ttu-id="6c802-240">Dans la page **noms de domaine** , dans la section **domaine** , sélectionnez le nom du domaine que vous mettez à jour.</span><span class="sxs-lookup"><span data-stu-id="6c802-240">On the **Domain Names** page, in the **Domain** section, select the name of the domain that you are updating.</span></span> 
    
    ![CrazyDomains-BP-configure-1-3](../../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. <span data-ttu-id="6c802-242">Dans la section **paramètres DNS** , sélectionnez l’icône de la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6c802-242">In the **DNS Settings** section, select the drop-down list icon.</span></span> 
    
    ![CrazyDomains-BP-configure-1-4-1](../../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. <span data-ttu-id="6c802-244">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="6c802-244">Select **Add Record**.</span></span>
    
    ![CrazyDomains-BP-configure-1-4-2](../../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. <span data-ttu-id="6c802-246">Choisissez **TXT Record** (Enregistrement TXT) dans la liste déroulante **Add Record** (Ajouter un enregistrement).</span><span class="sxs-lookup"><span data-stu-id="6c802-246">Choose **TXT Record** from the **Add Record:** drop-down list.</span></span> 
    
    ![CrazyDomains-BP-configure-4-1](../../media/7f2461e2-0468-49bd-9eb0-981e9b2f72d6.png)
  
7. <span data-ttu-id="6c802-248">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6c802-248">Select **Add**.</span></span>
    
    ![CrazyDomains-BP-configure-4-2](../../media/64ef9e1f-676d-46e2-9253-a83d9bcd1c4e.png)
  
8. <span data-ttu-id="6c802-250">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6c802-250">In the boxes for the new record, type or paste the values from the following table.</span></span>
    
    |<span data-ttu-id="6c802-251">**Sub Domain (Sous-domaine)**</span><span class="sxs-lookup"><span data-stu-id="6c802-251">**Sub Domain**</span></span>|<span data-ttu-id="6c802-252">**Text Record (Enregistrement texte)**</span><span class="sxs-lookup"><span data-stu-id="6c802-252">**Text Record**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="6c802-253">(Laissez ce champ vide.)</span><span class="sxs-lookup"><span data-stu-id="6c802-253">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="6c802-254">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="6c802-254">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="6c802-255">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="6c802-255">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![CrazyDomains-BP-configure-4-3](../../media/e7fd524a-c94b-4cdd-b264-67abb532a71b.png)
  
9. <span data-ttu-id="6c802-257">Sélectionnez **Mettre à jour**.</span><span class="sxs-lookup"><span data-stu-id="6c802-257">Select **Update**.</span></span>
    
    ![CrazyDomains-BP-configure-4-4](../../media/d4f378ee-0f14-46ae-ba32-1596660ecf91.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="6c802-259">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="6c802-259">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="6c802-260"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="6c802-260"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="6c802-p112">Pour commencer, accédez à la page de vos domaines sur le site Crazy Domains en utilisant [ce lien](https://manage.crazydomains.com/members/domains/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="6c802-p112">To get started, go to your domains page at Crazy Domains by using [this link](https://manage.crazydomains.com/members/domains/). You'll be prompted to log in first.</span></span>
    
    ![CrazyDomains-BP-configure-1-1](../../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. <span data-ttu-id="6c802-264">Dans la section **mon compte** , sélectionnez **domaines**.</span><span class="sxs-lookup"><span data-stu-id="6c802-264">In the **My Account** section, select **Domains**.</span></span>
    
    ![CrazyDomains-BP-configure-1-2](../../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. <span data-ttu-id="6c802-266">Dans la page **noms de domaine** , dans la section **domaine** , sélectionnez le nom du domaine que vous mettez à jour.</span><span class="sxs-lookup"><span data-stu-id="6c802-266">On the **Domain Names** page, in the **Domain** section, select the name of the domain that you are updating.</span></span> 
    
    ![CrazyDomains-BP-configure-1-3](../../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. <span data-ttu-id="6c802-268">Dans la section **paramètres DNS** , sélectionnez l’icône de la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6c802-268">In the **DNS Settings** section, select the drop-down list icon.</span></span> 
    
    ![CrazyDomains-BP-configure-1-4-1](../../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. <span data-ttu-id="6c802-270">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="6c802-270">Select **Add Record**.</span></span>
    
    ![CrazyDomains-BP-configure-1-4-2](../../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. <span data-ttu-id="6c802-272">Choisissez **SRV Record** (Enregistrement SRV) dans la liste déroulante **Add Record** (Ajouter un enregistrement).</span><span class="sxs-lookup"><span data-stu-id="6c802-272">Choose **SRV Record** from the **Add Record:** drop-down list.</span></span> 
    
    ![CrazyDomains-BP-configure-5-1](../../media/156acebc-7f6d-4b5e-8493-6bc62ca0ee27.png)
  
7. <span data-ttu-id="6c802-274">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6c802-274">Select **Add**.</span></span>
    
    ![CrazyDomains-BP-configure-5-2](../../media/6a711df7-4215-49b2-b58f-1cf1a242b383.png)
  
8. <span data-ttu-id="6c802-276">Ajoutez le premier des deux enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="6c802-276">Add the first of the two SRV records.</span></span>
    
    <span data-ttu-id="6c802-277">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6c802-277">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span>
    
    |<span data-ttu-id="6c802-278">**Record Type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="6c802-278">**Record Type**</span></span>|<span data-ttu-id="6c802-279">**Sub Domain (Sous-domaine)**</span><span class="sxs-lookup"><span data-stu-id="6c802-279">**Sub Domain**</span></span>|<span data-ttu-id="6c802-280">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="6c802-280">**Priority**</span></span>|<span data-ttu-id="6c802-281">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="6c802-281">**Weight**</span></span>|<span data-ttu-id="6c802-282">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="6c802-282">**Port**</span></span>|<span data-ttu-id="6c802-283">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="6c802-283">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="6c802-284">SRV Record (Enregistrement SRV)</span><span class="sxs-lookup"><span data-stu-id="6c802-284">SRV Record</span></span>  <br/> |<span data-ttu-id="6c802-285">_sip. _tls</span><span class="sxs-lookup"><span data-stu-id="6c802-285">_sip._tls</span></span>  <br/> |<span data-ttu-id="6c802-286">100</span><span class="sxs-lookup"><span data-stu-id="6c802-286">100</span></span>  <br/> |<span data-ttu-id="6c802-287">1 </span><span class="sxs-lookup"><span data-stu-id="6c802-287">1</span></span>  <br/> |<span data-ttu-id="6c802-288">443</span><span class="sxs-lookup"><span data-stu-id="6c802-288">443</span></span>  <br/> |<span data-ttu-id="6c802-289">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="6c802-289">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="6c802-290">SRV Record (Enregistrement SRV)</span><span class="sxs-lookup"><span data-stu-id="6c802-290">SRV Record</span></span>  <br/> |<span data-ttu-id="6c802-291">_sipfederationtls. _tcp</span><span class="sxs-lookup"><span data-stu-id="6c802-291">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="6c802-292">100</span><span class="sxs-lookup"><span data-stu-id="6c802-292">100</span></span>  <br/> |<span data-ttu-id="6c802-293">1 </span><span class="sxs-lookup"><span data-stu-id="6c802-293">1</span></span>  <br/> |<span data-ttu-id="6c802-294">5061</span><span class="sxs-lookup"><span data-stu-id="6c802-294">5061</span></span>  <br/> |<span data-ttu-id="6c802-295">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="6c802-295">sipfed.online.lync.com</span></span>  <br/> |
   
    ![CrazyDomains-BP-configure-5-3](../../media/cc0ea6eb-7358-434e-bd1a-2737725c6d41.png)
  
9. <span data-ttu-id="6c802-297">Sélectionnez **Ajouter un enregistrement SRV**.</span><span class="sxs-lookup"><span data-stu-id="6c802-297">Select **Add SRV Record**.</span></span>
    
    ![CrazyDomains-BP-configure-5-4](../../media/de4ec312-6833-469a-b23a-f376140a35ca.png)
  
10. <span data-ttu-id="6c802-299">Ajoutez l'autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="6c802-299">Add the other SRV record.</span></span>
    
    <span data-ttu-id="6c802-300">Dans les zones du nouvel enregistrement, utilisez les valeurs de la deuxième ligne du tableau.</span><span class="sxs-lookup"><span data-stu-id="6c802-300">In the boxes for the new record, use the values from the second row in the table.</span></span>
    
11. <span data-ttu-id="6c802-301">Sélectionnez **mettre à jour** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="6c802-301">Select **Update** to save your changes.</span></span> 
    
    ![CrazyDomains-BP-configure-5-5](../../media/f0bb1dd6-3772-4293-bf74-710f635e0658.png)
  
> [!NOTE]
> <span data-ttu-id="6c802-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="6c802-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
