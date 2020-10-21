---
title: Créer des enregistrements DNS sur Names.co.uk pour Microsoft
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: scotv
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
ms.assetid: b6c15128-b456-49b4-8b5e-5b823c700f26
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur Names.co.uk pour Microsoft.
ms.openlocfilehash: d3a3e68558efc3857d343b3298c3c01f0e8d8802
ms.sourcegitcommit: 628f195cbe3c00910f7350d8b09997a675dde989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "48645862"
---
# <a name="create-dns-records-at-namescouk-for-microsoft"></a><span data-ttu-id="33399-103">Créer des enregistrements DNS sur Names.co.uk pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="33399-103">Create DNS records at Names.co.uk for Microsoft</span></span>

 <span data-ttu-id="33399-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="33399-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="33399-105">Si Names.co.uk est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="33399-105">If Names.co.uk is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
    
<span data-ttu-id="33399-106">Une fois ces enregistrements ajoutés sur Names.co.uk, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="33399-106">After you add these records at Names.co.uk, your domain will be set up to work with Microsoft services.</span></span>
  

  
> [!NOTE]
>  <span data-ttu-id="33399-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="33399-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="33399-110">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="33399-110">Add a TXT record for verification</span></span>
<span data-ttu-id="33399-111"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="33399-111"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="33399-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="33399-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="33399-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="33399-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="33399-p104">Pour commencer, accédez à la page de vos domaines sur le site Names.co.uk en utilisant [ce lien](https://account.names.co.uk/dashboard#/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="33399-p104">To get started, go to your domains page at Names.co.uk by using [this link](https://account.names.co.uk/dashboard#/). You'll be prompted to log in first.</span></span>
    
    ![NamesUK-BP-configure-1-1](../../media/e5cd0e0c-57f9-4b3d-b1c2-0d6b260f5524.png)
  
2. <span data-ttu-id="33399-119">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span><span class="sxs-lookup"><span data-stu-id="33399-119">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="33399-120">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="33399-120">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-1-2](../../media/b618f8e5-404e-466a-9e71-acd7479f3994.png)
  
3. <span data-ttu-id="33399-122">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="33399-122">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="33399-123">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="33399-123">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    <span data-ttu-id="33399-124">(Si vous avez besoin d’ajouter une ligne, sélectionnez **Ajouter des enregistrements a/CNAME (+)**.)</span><span class="sxs-lookup"><span data-stu-id="33399-124">(If you need to add a row, select **ADD A/CNAME RECORDS (+)**.)</span></span>
    
    <span data-ttu-id="33399-125">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="33399-125">(You may have to scroll down.)</span></span>
        
    |<span data-ttu-id="33399-126">**Host name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="33399-126">**Host name**</span></span>|<span data-ttu-id="33399-127">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="33399-127">**Type**</span></span>|<span data-ttu-id="33399-128">**Result (Résultat)**</span><span class="sxs-lookup"><span data-stu-id="33399-128">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="33399-129">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="33399-129">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="33399-130">TXT</span><span class="sxs-lookup"><span data-stu-id="33399-130">TXT</span></span>  <br/> |<span data-ttu-id="33399-131">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="33399-131">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="33399-132">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="33399-132">**Note:** This is an example.</span></span> <span data-ttu-id="33399-133">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="33399-133">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="33399-134">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="33399-134">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)    |
       
    ![NamesUK-BP-Verify-1-1](../../media/91ed1f22-a796-418d-bbb0-345e2cd99bde.png)
  
4. <span data-ttu-id="33399-136">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="33399-136">Select **Save**.</span></span>
    
    <span data-ttu-id="33399-137">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="33399-137">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-Verify-1-2](../../media/40e991f9-2209-4210-8762-981cca670d70.png)
  
5. <span data-ttu-id="33399-139">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="33399-139">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="33399-140">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="33399-140">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="33399-141">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="33399-141">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="33399-142">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="33399-142">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="33399-143">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="33399-143">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="33399-144">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="33399-144">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="33399-145">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="33399-145">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="33399-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="33399-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="33399-149">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="33399-149">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="33399-150"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="33399-150"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="33399-p107">Pour commencer, accédez à la page de vos domaines sur le site Names.co.uk en utilisant [ce lien](https://account.names.co.uk/dashboard#/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="33399-p107">To get started, go to your domains page at Names.co.uk by using [this link](https://account.names.co.uk/dashboard#/). You'll be prompted to log in first.</span></span>
    
    ![NamesUK-BP-configure-1-1](../../media/e5cd0e0c-57f9-4b3d-b1c2-0d6b260f5524.png)
  
2. <span data-ttu-id="33399-154">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span><span class="sxs-lookup"><span data-stu-id="33399-154">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="33399-155">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="33399-155">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-1-2](../../media/b618f8e5-404e-466a-9e71-acd7479f3994.png)
  
3. <span data-ttu-id="33399-157">Sur la page **Add/Modify DNS Zone (Ajouter/modifier la zone DNS)**, dans la section **Mail exchange records (Enregistrements MX)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="33399-157">On the **Add/Modify DNS Zone** page, in the **Mail exchange records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="33399-158">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="33399-158">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="33399-159">**Host name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="33399-159">**Host name**</span></span>|<span data-ttu-id="33399-160">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="33399-160">**Priority**</span></span>|<span data-ttu-id="33399-161">**Result (Résultat)**</span><span class="sxs-lookup"><span data-stu-id="33399-161">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="33399-162">(Laissez ce champ vide.)</span><span class="sxs-lookup"><span data-stu-id="33399-162">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="33399-163">0,1</span><span class="sxs-lookup"><span data-stu-id="33399-163">1</span></span>  <br/> <span data-ttu-id="33399-164">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span><span class="sxs-lookup"><span data-stu-id="33399-164">For more information about priority, see [What is MX priority?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span></span> <br/> | <span data-ttu-id="33399-165">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="33399-165">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="33399-166">> [!NOTE]> obtenir votre  *\<domain-key\>*  compte à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="33399-166">> [!NOTE]> Get your  *\<domain-key\>*  from your Microsoft account.</span></span>           [<span data-ttu-id="33399-167">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="33399-167">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
       
    ![NamesUK-BP-configure-2-1](../../media/e211d73d-864f-4114-864b-8e636c69f595.png)
  
4. <span data-ttu-id="33399-169">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="33399-169">Select **Save**.</span></span>
    
    <span data-ttu-id="33399-170">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="33399-170">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-2-2](../../media/01e6c801-daa2-40ca-84f9-dcac6422257c.png)
  
5. <span data-ttu-id="33399-172">Si d'autres enregistrements MX apparaissent dans la section **Mail exchange records (Enregistrements MX)**, supprimez-les en les sélectionnant et en appuyant sur la touche **Suppr** du clavier.</span><span class="sxs-lookup"><span data-stu-id="33399-172">If there are any other MX records listed in the **Mail exchange records** section, delete each one by selecting it and then pressing the **Delete** key on your keyboard.</span></span> 
    
    ![NamesUK-BP-configure-2-3](../../media/f8e43926-b724-4690-94e7-ec4b8d7a8da5.png)
  
6. <span data-ttu-id="33399-174">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="33399-174">Select **Save**.</span></span>
    
    <span data-ttu-id="33399-175">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="33399-175">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-2-4](../../media/cd705919-d0bd-408f-82be-b54e732cb05c.png)
  
## <a name="add-the-six-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="33399-177">Ajouter les six enregistrements CNAMe requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="33399-177">Add the six CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="33399-178"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="33399-178"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="33399-p109">Pour commencer, accédez à la page de vos domaines sur le site Names.co.uk en utilisant [ce lien](https://account.names.co.uk/dashboard#/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="33399-p109">To get started, go to your domains page at Names.co.uk by using [this link](https://account.names.co.uk/dashboard#/). You'll be prompted to log in first.</span></span>
    
    ![NamesUK-BP-configure-1-1](../../media/e5cd0e0c-57f9-4b3d-b1c2-0d6b260f5524.png)
  
2. <span data-ttu-id="33399-182">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span><span class="sxs-lookup"><span data-stu-id="33399-182">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="33399-183">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="33399-183">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-1-2](../../media/b618f8e5-404e-466a-9e71-acd7479f3994.png)
  
3. <span data-ttu-id="33399-185">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="33399-185">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="33399-186">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="33399-186">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    <span data-ttu-id="33399-187">(Si vous avez besoin d’ajouter une ligne, sélectionnez **Ajouter des enregistrements a/CNAME (+)**.)</span><span class="sxs-lookup"><span data-stu-id="33399-187">(If you need to add a row, select **ADD A/CNAME RECORDS (+)**.)</span></span>
    
    <span data-ttu-id="33399-188">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="33399-188">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="33399-189">**Host Name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="33399-189">**Host Name**</span></span>|<span data-ttu-id="33399-190">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="33399-190">**Type**</span></span>|<span data-ttu-id="33399-191">**Result (Résultat)**</span><span class="sxs-lookup"><span data-stu-id="33399-191">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="33399-192">autodiscover</span><span class="sxs-lookup"><span data-stu-id="33399-192">autodiscover</span></span>  <br/> |<span data-ttu-id="33399-193">CNAME</span><span class="sxs-lookup"><span data-stu-id="33399-193">CNAME</span></span>  <br/> |<span data-ttu-id="33399-194">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="33399-194">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="33399-195">sip</span><span class="sxs-lookup"><span data-stu-id="33399-195">sip</span></span>  <br/> |<span data-ttu-id="33399-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="33399-196">CNAME</span></span>  <br/> |<span data-ttu-id="33399-197">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="33399-197">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="33399-198">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="33399-198">lyncdiscover</span></span>  <br/> |<span data-ttu-id="33399-199">CNAME</span><span class="sxs-lookup"><span data-stu-id="33399-199">CNAME</span></span>  <br/> |<span data-ttu-id="33399-200">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="33399-200">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="33399-201">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="33399-201">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="33399-202">CNAME</span><span class="sxs-lookup"><span data-stu-id="33399-202">CNAME</span></span>  <br/> |<span data-ttu-id="33399-203">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="33399-203">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="33399-204">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="33399-204">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="33399-205">CNAME</span><span class="sxs-lookup"><span data-stu-id="33399-205">CNAME</span></span>  <br/> |<span data-ttu-id="33399-206">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="33399-206">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
       
    ![NamesUK-BP-configure-3-1](../../media/392772bf-2ed3-4959-9a9a-bb1611905e86.png)
  
4. <span data-ttu-id="33399-208">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="33399-208">Select **Save**.</span></span>
    
    ![NamesUK-BP-configure-3-2](../../media/c009795e-7eef-4804-bf23-556f498306cc.png)
  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="33399-210">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="33399-210">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="33399-211"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="33399-211"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="33399-212">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="33399-212">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="33399-213">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="33399-213">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="33399-214">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="33399-214">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="33399-215">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="33399-215">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>
  
1. <span data-ttu-id="33399-p111">Pour commencer, accédez à la page de vos domaines sur le site Names.co.uk en utilisant [ce lien](https://account.names.co.uk/dashboard#/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="33399-p111">To get started, go to your domains page at Names.co.uk by using [this link](https://account.names.co.uk/dashboard#/). You'll be prompted to log in first.</span></span>
    
    ![NamesUK-BP-configure-1-1](../../media/e5cd0e0c-57f9-4b3d-b1c2-0d6b260f5524.png)
  
2. <span data-ttu-id="33399-219">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span><span class="sxs-lookup"><span data-stu-id="33399-219">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="33399-220">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="33399-220">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-1-2](../../media/b618f8e5-404e-466a-9e71-acd7479f3994.png)
  
3. <span data-ttu-id="33399-222">Sur la page **zones DNS sur le compte** , dans la colonne **nom de domaine** , sélectionnez le nom du domaine que vous mettez à jour.</span><span class="sxs-lookup"><span data-stu-id="33399-222">On the **DNS Zones on Account** page, in the **Domain name** column, select the name of the domain that you are updating.</span></span> 
    
    ![NamesUK-BP-configure-1-2-1](../../media/20254eec-6952-47ba-b12b-da32860ee7ef.png)
  
4. <span data-ttu-id="33399-224">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="33399-224">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="33399-225">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="33399-225">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    <span data-ttu-id="33399-226">(Si vous avez besoin d’ajouter une ligne, sélectionnez **Ajouter des enregistrements a/CNAME (+)**.)</span><span class="sxs-lookup"><span data-stu-id="33399-226">(If you need to add a row, select **ADD A/CNAME RECORDS (+)**.)</span></span>
    
    <span data-ttu-id="33399-227">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="33399-227">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="33399-228">**Host name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="33399-228">**Host name**</span></span>|<span data-ttu-id="33399-229">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="33399-229">**Type**</span></span>|<span data-ttu-id="33399-230">**Result (Résultat)**</span><span class="sxs-lookup"><span data-stu-id="33399-230">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="33399-231">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="33399-231">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="33399-232">TXT</span><span class="sxs-lookup"><span data-stu-id="33399-232">TXT</span></span>  <br/> |<span data-ttu-id="33399-233">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="33399-233">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="33399-234">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="33399-234">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
       
    ![NamesUK-BP-configure-4-1](../../media/cfc61387-630e-4aa0-8762-ef36eaeda44a.png)
  
5. <span data-ttu-id="33399-236">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="33399-236">Select **Save**.</span></span>
    
    <span data-ttu-id="33399-237">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="33399-237">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-4-2](../../media/b4d445a1-09c0-46c3-8141-672cc2831a9b.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="33399-239">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="33399-239">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="33399-240"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="33399-240"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="33399-p112">Pour commencer, accédez à la page de vos domaines sur le site Names.co.uk en utilisant [ce lien](https://account.names.co.uk/dashboard#/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="33399-p112">To get started, go to your domains page at Names.co.uk by using [this link](https://account.names.co.uk/dashboard#/). You'll be prompted to log in first.</span></span>
    
    ![NamesUK-BP-configure-1-1](../../media/e5cd0e0c-57f9-4b3d-b1c2-0d6b260f5524.png)
  
2. <span data-ttu-id="33399-244">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span><span class="sxs-lookup"><span data-stu-id="33399-244">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="33399-245">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="33399-245">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-1-2](../../media/b618f8e5-404e-466a-9e71-acd7479f3994.png)
  
3. <span data-ttu-id="33399-247">Sur la page **Add/Modify DNS Zone (Ajouter/modifier la zone DNS)**, dans la section **Service records (Enregistrements de service)**, dans les zones des nouveaux enregistrements, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="33399-247">On the **Add/Modify DNS Zone** page, in the **Service records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="33399-248">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="33399-248">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="33399-249">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="33399-249">**Name**</span></span>|<span data-ttu-id="33399-250">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="33399-250">**Priority**</span></span>|<span data-ttu-id="33399-251">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="33399-251">**Weight**</span></span>|<span data-ttu-id="33399-252">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="33399-252">**Port**</span></span>|<span data-ttu-id="33399-253">**Result (Résultat)**</span><span class="sxs-lookup"><span data-stu-id="33399-253">**Result**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="33399-254">_sip._tls</span><span class="sxs-lookup"><span data-stu-id="33399-254">_sip._tls</span></span>  <br/> |<span data-ttu-id="33399-255">100</span><span class="sxs-lookup"><span data-stu-id="33399-255">100</span></span>  <br/> |<span data-ttu-id="33399-256">0,1</span><span class="sxs-lookup"><span data-stu-id="33399-256">1</span></span>  <br/> |<span data-ttu-id="33399-257">443</span><span class="sxs-lookup"><span data-stu-id="33399-257">443</span></span>  <br/> |<span data-ttu-id="33399-258">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="33399-258">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="33399-259">_sipfederationtls._tcp</span><span class="sxs-lookup"><span data-stu-id="33399-259">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="33399-260">100</span><span class="sxs-lookup"><span data-stu-id="33399-260">100</span></span>  <br/> |<span data-ttu-id="33399-261">0,1</span><span class="sxs-lookup"><span data-stu-id="33399-261">1</span></span>  <br/> |<span data-ttu-id="33399-262">5061</span><span class="sxs-lookup"><span data-stu-id="33399-262">5061</span></span>  <br/> |<span data-ttu-id="33399-263">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="33399-263">sipfed.online.lync.com</span></span>  <br/> |
       
    ![NamesUK-BP-configure-5-1](../../media/97a96523-005a-4058-9e12-19f6c3bf9b3b.png)
  
4. <span data-ttu-id="33399-265">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="33399-265">Select **Save**.</span></span>
    
    <span data-ttu-id="33399-266">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="33399-266">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-5-2](../../media/bb617a5f-14f9-44b7-9256-bdef34d22d6b.png)
  
> [!NOTE]
>  <span data-ttu-id="33399-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="33399-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
