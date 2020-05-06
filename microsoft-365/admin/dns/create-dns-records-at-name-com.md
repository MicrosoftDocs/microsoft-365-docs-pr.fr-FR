---
title: Créer des enregistrements DNS sur name.com pour Microsoft
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
ms.assetid: 9ddcc2fc-9433-4335-8192-6ffb1f541087
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur name.com pour Microsoft.
ms.openlocfilehash: e9133b3701c2b454cad11b9579dc7463f1a74460
ms.sourcegitcommit: 5476c2578400894640ae74bfe8e93c3319f685bd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2020
ms.locfileid: "44048962"
---
# <a name="create-dns-records-at-namecom-for-microsoft"></a><span data-ttu-id="f08d7-103">Créer des enregistrements DNS sur name.com pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="f08d7-103">Create DNS records at name.com for Microsoft</span></span>

 <span data-ttu-id="f08d7-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="f08d7-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="f08d7-105">Si name.com est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="f08d7-105">If name.com is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="f08d7-106">Une fois ces enregistrements ajoutés sur name.com, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f08d7-106">After you add these records at name.com, your domain will be set up to work with Microsoft services.</span></span>

  
> [!NOTE]
> <span data-ttu-id="f08d7-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f08d7-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="f08d7-110">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="f08d7-110">Add a TXT record for verification</span></span>
<span data-ttu-id="f08d7-111"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="f08d7-111"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="f08d7-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="f08d7-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f08d7-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="f08d7-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="f08d7-p104">Pour commencer, accédez à la page de vos domaines sur le site name.com en utilisant [ce lien](https://www.name.com/account/domain). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f08d7-p104">To get started, go to your domains page at name.com by using [this link](https://www.name.com/account/domain). You'll be prompted to log in first.</span></span>
    
    ![Name-BP-Configure-1-1](../../media/1869b416-1d3f-4fb1-99c6-62b74ca7a4c7.png)
  
2. <span data-ttu-id="f08d7-119">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f08d7-119">Under **My Domains**, select the name of the domain that you want to modify.</span></span>
    
    ![Name-BP-Configure-1-2](../../media/c8b96e1e-aa35-4fb1-8209-450f587fec4d.png)
  
3. <span data-ttu-id="f08d7-121">Dans la colonne **Détails** , sélectionnez **enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="f08d7-121">In the **Details** column, select **DNS Records**.</span></span> 
    
    ![Name-BP-Configure-1-3](../../media/c5da31e2-2f77-4d0c-b31d-189e6fb7b205.png)
  
4. <span data-ttu-id="f08d7-123">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f08d7-123">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="f08d7-124">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="f08d7-124">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |||||
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f08d7-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-125">**Type**</span></span> <br/> |<span data-ttu-id="f08d7-126">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-126">**Host**</span></span> <br/> |<span data-ttu-id="f08d7-127">**Answer (Réponse)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-127">**Answer**</span></span> <br/> |<span data-ttu-id="f08d7-128">**TTL**</span><span class="sxs-lookup"><span data-stu-id="f08d7-128">**TTL**</span></span> <br/> |
    |<span data-ttu-id="f08d7-129">TXT</span><span class="sxs-lookup"><span data-stu-id="f08d7-129">TXT</span></span>  <br/> |<span data-ttu-id="f08d7-130">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="f08d7-130">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="f08d7-131">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="f08d7-131">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="f08d7-132">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="f08d7-132">**Note:** This is an example.</span></span> <span data-ttu-id="f08d7-133">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="f08d7-133">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="f08d7-134">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="f08d7-134">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="f08d7-135">Use the default value (300).</span><span class="sxs-lookup"><span data-stu-id="f08d7-135">Use the default value (300).</span></span>  <br/> |
   
    ![Nom-BP-Verify-1-1](../../media/0c352fd3-cf84-439f-a481-0705e225cc54.png)
  
5. <span data-ttu-id="f08d7-137">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="f08d7-137">Select **Add Record**.</span></span>
    
    ![Name-BP-Verify-1-2](../../media/816fc60b-17ab-4982-8849-6c3fcf3ca3d6.png)
  
6. <span data-ttu-id="f08d7-139">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="f08d7-139">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="f08d7-140">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f08d7-140">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="f08d7-141">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="f08d7-141">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="f08d7-142">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="f08d7-142">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="f08d7-143">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="f08d7-143">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="f08d7-144">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="f08d7-144">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="f08d7-145">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="f08d7-145">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
> <span data-ttu-id="f08d7-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f08d7-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="f08d7-149">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="f08d7-149">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="f08d7-150"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="f08d7-150"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="f08d7-p107">Pour commencer, accédez à la page de vos domaines sur le site name.com en utilisant [ce lien](https://www.name.com/account/domain). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f08d7-p107">To get started, go to your domains page at name.com by using [this link](https://www.name.com/account/domain). You'll be prompted to log in first.</span></span>
    
    ![Name-BP-Configure-1-1](../../media/1869b416-1d3f-4fb1-99c6-62b74ca7a4c7.png)
  
2. <span data-ttu-id="f08d7-154">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f08d7-154">Under **My Domains**, select the name of the domain that you want to modify.</span></span>
    
    ![Name-BP-Configure-1-2](../../media/c8b96e1e-aa35-4fb1-8209-450f587fec4d.png)
  
3. <span data-ttu-id="f08d7-156">Dans la colonne **Détails** , sélectionnez **enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="f08d7-156">In the **Details** column, select **DNS Records**.</span></span> 
    
    ![Name-BP-Configure-1-3](../../media/c5da31e2-2f77-4d0c-b31d-189e6fb7b205.png)
  
4. <span data-ttu-id="f08d7-158">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f08d7-158">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="f08d7-159">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="f08d7-159">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="f08d7-160">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-160">**Type**</span></span>|<span data-ttu-id="f08d7-161">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-161">**Host**</span></span>|<span data-ttu-id="f08d7-162">**Answer (Réponse)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-162">**Answer**</span></span>|<span data-ttu-id="f08d7-163">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-163">**TTL**</span></span>|<span data-ttu-id="f08d7-164">**Prio (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-164">**Prio**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f08d7-165">MX</span><span class="sxs-lookup"><span data-stu-id="f08d7-165">MX</span></span>  <br/> |<span data-ttu-id="f08d7-166">(Laissez ce champ vide.)</span><span class="sxs-lookup"><span data-stu-id="f08d7-166">(Leave this field empty.)</span></span>  <br/> | <span data-ttu-id="f08d7-167">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="f08d7-167">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="f08d7-168">**Remarque :** Obtenir votre \* \<clé\> de domaine\* à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f08d7-168">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>           [<span data-ttu-id="f08d7-169">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="f08d7-169">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="f08d7-170">Use the default value (300).</span><span class="sxs-lookup"><span data-stu-id="f08d7-170">Use the default value (300).</span></span>  <br/> |<span data-ttu-id="f08d7-171">0</span><span class="sxs-lookup"><span data-stu-id="f08d7-171">0</span></span>  <br/> <span data-ttu-id="f08d7-172">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span><span class="sxs-lookup"><span data-stu-id="f08d7-172">For more information about priority, see [What is MX priority?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span></span> <br/> |
   
   ![Nom-BP-configure-2-1](../../media/11ba2160-fc8e-4196-bb15-2b7c6d49c8fc.png)
  
5. <span data-ttu-id="f08d7-174">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="f08d7-174">Select **Add Record**.</span></span>
    
    ![Name-BP-Configuration-2-2](../../media/fd09f161-7cc4-4723-aec2-5fa801bd19e9.png)
  
6. <span data-ttu-id="f08d7-176">S'il existe d'autres enregistrements MX, supprimez chacun d'eux à l'aide de la procédure en deux étapes suivante :</span><span class="sxs-lookup"><span data-stu-id="f08d7-176">If there are any other MX records, delete each of them by using the following two-step procedure:</span></span>
    
    <span data-ttu-id="f08d7-177">Pour chaque autre enregistrement MX, sélectionnez **supprimer** dans la colonne **actions** .</span><span class="sxs-lookup"><span data-stu-id="f08d7-177">For each other MX record, select **Delete** in the **Actions** column.</span></span> 
    
    ![Name-BP-Configuration-2-3](../../media/16734a98-31c4-4023-a2a5-10b7c95bc58e.png)
  
    <span data-ttu-id="f08d7-179">Pour confirmer chaque suppression, sélectionnez **supprimer** dans la colonne **actions** .</span><span class="sxs-lookup"><span data-stu-id="f08d7-179">To confirm each deletion, select **Delete** in the **Actions** column again.</span></span> 
    
    ![Name-BP-Configure-2-4](../../media/409c21c5-51f4-4244-bb84-5d32084224b2.png)
  
    <span data-ttu-id="f08d7-181">Répétez cette procédure en deux étapes jusqu'à avoir supprimé tous les autres enregistrements MX.</span><span class="sxs-lookup"><span data-stu-id="f08d7-181">Repeat this two-step procedure until you have deleted each of the other MX records.</span></span>
    
## <a name="add-the-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="f08d7-182">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="f08d7-182">Add the CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="f08d7-183"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="f08d7-183"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="f08d7-p109">Pour commencer, accédez à la page de vos domaines sur le site name.com en utilisant [ce lien](https://www.name.com/account/domain). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f08d7-p109">To get started, go to your domains page at name.com by using [this link](https://www.name.com/account/domain). You'll be prompted to log in first.</span></span>
    
    ![Name-BP-Configure-1-1](../../media/1869b416-1d3f-4fb1-99c6-62b74ca7a4c7.png)
  
2. <span data-ttu-id="f08d7-187">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f08d7-187">Under **My Domains**, select the name of the domain that you want to modify.</span></span>
    
    ![Name-BP-Configure-1-2](../../media/c8b96e1e-aa35-4fb1-8209-450f587fec4d.png)
  
3. <span data-ttu-id="f08d7-189">Dans la colonne **Détails** , sélectionnez **enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="f08d7-189">In the **Details** column, select **DNS Records**.</span></span> 
    
    ![Name-BP-Configure-1-3](../../media/c5da31e2-2f77-4d0c-b31d-189e6fb7b205.png)
  
4. <span data-ttu-id="f08d7-191">Ajoutez le premier enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="f08d7-191">Add the first CNAME record.</span></span>
    
    <span data-ttu-id="f08d7-192">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f08d7-192">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span>
    
    <span data-ttu-id="f08d7-193">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="f08d7-193">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="f08d7-194">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-194">**Type**</span></span>|<span data-ttu-id="f08d7-195">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-195">**Host**</span></span>|<span data-ttu-id="f08d7-196">**Answer (Réponse)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-196">**Answer**</span></span>|<span data-ttu-id="f08d7-197">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-197">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f08d7-198">CNAME</span><span class="sxs-lookup"><span data-stu-id="f08d7-198">CNAME</span></span>  <br/> |<span data-ttu-id="f08d7-199">autodiscover</span><span class="sxs-lookup"><span data-stu-id="f08d7-199">autodiscover</span></span>  <br/> |<span data-ttu-id="f08d7-200">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="f08d7-200">autodiscover.outlook.com</span></span>  <br/> |<span data-ttu-id="f08d7-201">Utilisez la valeur par défaut (300).</span><span class="sxs-lookup"><span data-stu-id="f08d7-201">Use the default value (300).</span></span>  <br/> |
    |<span data-ttu-id="f08d7-202">CNAME</span><span class="sxs-lookup"><span data-stu-id="f08d7-202">CNAME</span></span>  <br/> |<span data-ttu-id="f08d7-203">sip</span><span class="sxs-lookup"><span data-stu-id="f08d7-203">sip</span></span>  <br/> |<span data-ttu-id="f08d7-204">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="f08d7-204">sipdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="f08d7-205">Utilisez la valeur par défaut (300).</span><span class="sxs-lookup"><span data-stu-id="f08d7-205">Use the default value (300).</span></span>  <br/> |
    |<span data-ttu-id="f08d7-206">CNAME</span><span class="sxs-lookup"><span data-stu-id="f08d7-206">CNAME</span></span>  <br/> |<span data-ttu-id="f08d7-207">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="f08d7-207">lyncdiscover</span></span>  <br/> |<span data-ttu-id="f08d7-208">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="f08d7-208">webdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="f08d7-209">Utilisez la valeur par défaut (300).</span><span class="sxs-lookup"><span data-stu-id="f08d7-209">Use the default value (300).</span></span>  <br/> |
    |<span data-ttu-id="f08d7-210">CNAME</span><span class="sxs-lookup"><span data-stu-id="f08d7-210">CNAME</span></span>  <br/> |<span data-ttu-id="f08d7-211">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="f08d7-211">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="f08d7-212">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="f08d7-212">enterpriseregistration.windows.net</span></span>  <br/> |<span data-ttu-id="f08d7-213">Utilisez la valeur par défaut (300).</span><span class="sxs-lookup"><span data-stu-id="f08d7-213">Use the default value (300).</span></span>  <br/> |
    |<span data-ttu-id="f08d7-214">CNAME</span><span class="sxs-lookup"><span data-stu-id="f08d7-214">CNAME</span></span>  <br/> |<span data-ttu-id="f08d7-215">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="f08d7-215">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="f08d7-216">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="f08d7-216">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |<span data-ttu-id="f08d7-217">Utilisez la valeur par défaut (300).</span><span class="sxs-lookup"><span data-stu-id="f08d7-217">Use the default value (300).</span></span>  <br/> |
   
   ![Nom-BP-configure-3-1](../../media/4e34caaf-b418-40ec-abfa-fe62175a87c2.png)
  
5. <span data-ttu-id="f08d7-219">Sélectionnez **Add record (ajouter un enregistrement** ) pour ajouter le premier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f08d7-219">Select **Add Record** to add the first record.</span></span> 
    
    ![Name-BP-Configure-3-2](../../media/1053c2a7-07c3-4c1b-b54a-1c02881fb0ec.png)
  
6. <span data-ttu-id="f08d7-221">Ajoutez le deuxième enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="f08d7-221">Add the second CNAME record.</span></span>
    
    <span data-ttu-id="f08d7-222">Utilisez les valeurs de la deuxième ligne du tableau ci-dessus, puis sélectionnez **Add record (ajouter un enregistrement** ) pour ajouter le deuxième enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f08d7-222">Use the values from the second row of the table above, and then select **Add Record** to add the second record.</span></span> 
    
    <span data-ttu-id="f08d7-223">Ajoutez les enregistrements restants de la même manière, en utilisant les valeurs des troisième, quatrième, cinquième et sixième lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="f08d7-223">Add the remaining records in the same way, using the values from the third, fourth, fifth, and sixth rows of the table.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="f08d7-224">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="f08d7-224">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="f08d7-225"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="f08d7-225"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="f08d7-226">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="f08d7-226">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="f08d7-227">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="f08d7-227">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="f08d7-228">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f08d7-228">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="f08d7-229">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="f08d7-229">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
1. <span data-ttu-id="f08d7-p111">Pour commencer, accédez à la page de vos domaines sur le site name.com en utilisant [ce lien](https://www.name.com/account/domain). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f08d7-p111">To get started, go to your domains page at name.com by using [this link](https://www.name.com/account/domain). You'll be prompted to log in first.</span></span>
    
    ![Name-BP-Configure-1-1](../../media/1869b416-1d3f-4fb1-99c6-62b74ca7a4c7.png)
  
2. <span data-ttu-id="f08d7-233">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f08d7-233">Under **My Domains**, select the name of the domain that you want to modify.</span></span>

    ![Name-BP-Configure-1-2](../../media/c8b96e1e-aa35-4fb1-8209-450f587fec4d.png)
  
3. <span data-ttu-id="f08d7-235">Dans la colonne **Détails** , sélectionnez **enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="f08d7-235">In the **Details** column, select **DNS Records**.</span></span> 
    
    ![Name-BP-Configure-1-3](../../media/c5da31e2-2f77-4d0c-b31d-189e6fb7b205.png)
  
4. <span data-ttu-id="f08d7-237">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f08d7-237">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="f08d7-238">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="f08d7-238">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="f08d7-239">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-239">**Type**</span></span>|<span data-ttu-id="f08d7-240">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-240">**Host**</span></span>|<span data-ttu-id="f08d7-241">**Answer (Réponse)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-241">**Answer**</span></span>|<span data-ttu-id="f08d7-242">**TTL**</span><span class="sxs-lookup"><span data-stu-id="f08d7-242">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f08d7-243">TXT</span><span class="sxs-lookup"><span data-stu-id="f08d7-243">TXT</span></span>  <br/> |<span data-ttu-id="f08d7-244">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="f08d7-244">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="f08d7-245">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="f08d7-245">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="f08d7-246">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="f08d7-246">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |<span data-ttu-id="f08d7-247">Use the default value (300).</span><span class="sxs-lookup"><span data-stu-id="f08d7-247">Use the default value (300).</span></span>  <br/> |
   
   ![Nom-BP-configure-4-1](../../media/cbbfc071-840a-4ffa-a59e-0dfce03063cc.png)
  
5. <span data-ttu-id="f08d7-249">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="f08d7-249">Select **Add Record**.</span></span>
    
    ![Name-BP-Configure-4-2](../../media/db1e0e09-2b95-4fc1-88bd-e86da536921f.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="f08d7-251">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="f08d7-251">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="f08d7-252"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="f08d7-252"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="f08d7-p112">Pour commencer, accédez à la page de vos domaines sur le site name.com en utilisant [ce lien](https://www.name.com/account/domain). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f08d7-p112">To get started, go to your domains page at name.com by using [this link](https://www.name.com/account/domain). You'll be prompted to log in first.</span></span>
    
    ![Name-BP-Configure-1-1](../../media/1869b416-1d3f-4fb1-99c6-62b74ca7a4c7.png)
  
2. <span data-ttu-id="f08d7-256">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f08d7-256">Under **My Domains**, select the name of the domain that you want to modify.</span></span>
    
    ![Name-BP-Configure-1-2](../../media/c8b96e1e-aa35-4fb1-8209-450f587fec4d.png)
  
3. <span data-ttu-id="f08d7-258">Dans la colonne **Détails** , sélectionnez **enregistrements DNS +**.</span><span class="sxs-lookup"><span data-stu-id="f08d7-258">In the **Details** column, select **DNS Records+**.</span></span> 
    
    ![Name-BP-Configure-1-3](../../media/c5da31e2-2f77-4d0c-b31d-189e6fb7b205.png)
  
4. <span data-ttu-id="f08d7-260">Ajoutez le premier enregistrement SRV :</span><span class="sxs-lookup"><span data-stu-id="f08d7-260">Add the first SRV record:</span></span>
    
    <span data-ttu-id="f08d7-261">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f08d7-261">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span>
    
    <span data-ttu-id="f08d7-262">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="f08d7-262">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="f08d7-263">**Type**</span><span class="sxs-lookup"><span data-stu-id="f08d7-263">**Type**</span></span>|<span data-ttu-id="f08d7-264">**Service**</span><span class="sxs-lookup"><span data-stu-id="f08d7-264">**Service**</span></span>|<span data-ttu-id="f08d7-265">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-265">**Weight**</span></span>|<span data-ttu-id="f08d7-266">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-266">**TTL**</span></span>|<span data-ttu-id="f08d7-267">**Prio (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-267">**Prio**</span></span>|<span data-ttu-id="f08d7-268">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-268">**Protocol**</span></span>|<span data-ttu-id="f08d7-269">**Port**</span><span class="sxs-lookup"><span data-stu-id="f08d7-269">**Port**</span></span>|<span data-ttu-id="f08d7-270">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="f08d7-270">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f08d7-271">SRV</span><span class="sxs-lookup"><span data-stu-id="f08d7-271">SRV</span></span>|<span data-ttu-id="f08d7-272">sip</span><span class="sxs-lookup"><span data-stu-id="f08d7-272">sip</span></span>|<span data-ttu-id="f08d7-273">0,1</span><span class="sxs-lookup"><span data-stu-id="f08d7-273">1</span></span>|<span data-ttu-id="f08d7-274">Utilisez la valeur par défaut (300).</span><span class="sxs-lookup"><span data-stu-id="f08d7-274">Use the default value (300).</span></span>|<span data-ttu-id="f08d7-275">100</span><span class="sxs-lookup"><span data-stu-id="f08d7-275">100</span></span>|<span data-ttu-id="f08d7-276">tls</span><span class="sxs-lookup"><span data-stu-id="f08d7-276">tls</span></span>|<span data-ttu-id="f08d7-277">443</span><span class="sxs-lookup"><span data-stu-id="f08d7-277">443</span></span>|<span data-ttu-id="f08d7-278">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="f08d7-278">sipdir.online.lync.com</span></span> <br> <span data-ttu-id="f08d7-279">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="f08d7-279">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
    |<span data-ttu-id="f08d7-280">SRV</span><span class="sxs-lookup"><span data-stu-id="f08d7-280">SRV</span></span>|<span data-ttu-id="f08d7-281">sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="f08d7-281">sipfederationtls</span></span>|<span data-ttu-id="f08d7-282">0,1</span><span class="sxs-lookup"><span data-stu-id="f08d7-282">1</span></span>|<span data-ttu-id="f08d7-283">Utilisez la valeur par défaut (300).</span><span class="sxs-lookup"><span data-stu-id="f08d7-283">Use the default value (300).</span></span>|<span data-ttu-id="f08d7-284">100</span><span class="sxs-lookup"><span data-stu-id="f08d7-284">100</span></span>|<span data-ttu-id="f08d7-285">tcp</span><span class="sxs-lookup"><span data-stu-id="f08d7-285">tcp</span></span>|<span data-ttu-id="f08d7-286">5061</span><span class="sxs-lookup"><span data-stu-id="f08d7-286">5061</span></span>|<span data-ttu-id="f08d7-287">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="f08d7-287">sipfed.online.lync.com</span></span> <br><span data-ttu-id="f08d7-288">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="f08d7-288">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
   ![Nom-BP-configure-5-1](../../media/d9a885fd-7300-45b6-ad4c-0b4bf1067560.png)
  
5. <span data-ttu-id="f08d7-290">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="f08d7-290">Select **Add Record**.</span></span>

    ![Name-BP-Configure-5-2](../../media/a804d51d-8f57-4b0b-8bd6-a52eb1c87a97.png)
  
6. <span data-ttu-id="f08d7-292">Ajoutez le deuxième enregistrement SRV :</span><span class="sxs-lookup"><span data-stu-id="f08d7-292">Add the second SRV record:</span></span>

<span data-ttu-id="f08d7-293">Utilisez les valeurs de la ligne suivante du tableau ci-dessus, puis sélectionnez **Add record (ajouter un enregistrement** ) pour ajouter le deuxième enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f08d7-293">Use the values from the next row of the table above, and then select **Add Record** to add the second record.</span></span>

>[!NOTE]
><span data-ttu-id="f08d7-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f08d7-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span>
