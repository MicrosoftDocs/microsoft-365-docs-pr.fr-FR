---
title: Créer des enregistrements DNS auprès de Names.co.uk pour Office 365
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
ms.assetid: b6c15128-b456-49b4-8b5e-5b823c700f26
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur Names.co.uk pour Office 365.
ms.openlocfilehash: d27cd22b0047cf58def01533a486c7641f50148e
ms.sourcegitcommit: 812aab5f58eed4bf359faf0e99f7f876af5b1023
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/02/2020
ms.locfileid: "42348135"
---
# <a name="create-dns-records-at-namescouk-for-office-365"></a><span data-ttu-id="f0652-103">Créer des enregistrements DNS auprès de Names.co.uk pour Office 365</span><span class="sxs-lookup"><span data-stu-id="f0652-103">Create DNS records at Names.co.uk for Office 365</span></span>

 <span data-ttu-id="f0652-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="f0652-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="f0652-105">Si Names.co.uk est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="f0652-105">If Names.co.uk is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
    
<span data-ttu-id="f0652-106">Une fois ces enregistrements ajoutés sur Names.co.uk, votre domaine est configuré pour utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="f0652-106">After you add these records at Names.co.uk, your domain will be set up to work with Office 365 services.</span></span>
  
<span data-ttu-id="f0652-107">Pour en savoir plus sur l'hébergement web et le DNS pour les sites web avec Office 365, voir [Utiliser un site web public avec Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span><span class="sxs-lookup"><span data-stu-id="f0652-107">To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="f0652-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f0652-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="f0652-111">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="f0652-111">Add a TXT record for verification</span></span>
<span data-ttu-id="f0652-112"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="f0652-112"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="f0652-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="f0652-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f0652-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="f0652-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="f0652-p104">Pour commencer, accédez à la page de vos domaines sur le site Names.co.uk en utilisant [ce lien](https://account.names.co.uk/dashboard#/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f0652-p104">To get started, go to your domains page at Names.co.uk by using [this link](https://account.names.co.uk/dashboard#/). You'll be prompted to log in first.</span></span>
    
    ![NamesUK-BP-configure-1-1](../../media/e5cd0e0c-57f9-4b3d-b1c2-0d6b260f5524.png)
  
2. <span data-ttu-id="f0652-120">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span><span class="sxs-lookup"><span data-stu-id="f0652-120">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="f0652-121">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f0652-121">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-1-2](../../media/b618f8e5-404e-466a-9e71-acd7479f3994.png)
  
3. <span data-ttu-id="f0652-123">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="f0652-123">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="f0652-124">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="f0652-124">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    <span data-ttu-id="f0652-125">(Si vous avez besoin d’ajouter une ligne, sélectionnez **Ajouter des enregistrements a/CNAME (+)**.)</span><span class="sxs-lookup"><span data-stu-id="f0652-125">(If you need to add a row, select **ADD A/CNAME RECORDS (+)**.)</span></span>
    
    <span data-ttu-id="f0652-126">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f0652-126">(You may have to scroll down.)</span></span>
        
    |<span data-ttu-id="f0652-127">**Host name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="f0652-127">**Host name**</span></span>|<span data-ttu-id="f0652-128">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="f0652-128">**Type**</span></span>|<span data-ttu-id="f0652-129">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="f0652-129">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="f0652-130">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="f0652-130">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="f0652-131">TXT</span><span class="sxs-lookup"><span data-stu-id="f0652-131">TXT</span></span>  <br/> |<span data-ttu-id="f0652-132">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="f0652-132">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="f0652-133">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="f0652-133">**Note:** This is an example.</span></span> <span data-ttu-id="f0652-134">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="f0652-134">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span>           [<span data-ttu-id="f0652-135">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="f0652-135">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)    |
       
    ![NamesUK-BP-Verify-1-1](../../media/91ed1f22-a796-418d-bbb0-345e2cd99bde.png)
  
4. <span data-ttu-id="f0652-137">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f0652-137">Select **Save**.</span></span>
    
    <span data-ttu-id="f0652-138">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f0652-138">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-Verify-1-2](../../media/40e991f9-2209-4210-8762-981cca670d70.png)
  
5. <span data-ttu-id="f0652-140">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="f0652-140">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="f0652-141">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Office 365 et demandez à Office 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f0652-141">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="f0652-142">Lorsqu’Office 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="f0652-142">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="f0652-143">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="f0652-143">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="f0652-144">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="f0652-144">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="f0652-145">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="f0652-145">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="f0652-146">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="f0652-146">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="f0652-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f0652-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="f0652-150">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="f0652-150">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="f0652-151"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="f0652-151"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="f0652-p107">Pour commencer, accédez à la page de vos domaines sur le site Names.co.uk en utilisant [ce lien](https://account.names.co.uk/dashboard#/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f0652-p107">To get started, go to your domains page at Names.co.uk by using [this link](https://account.names.co.uk/dashboard#/). You'll be prompted to log in first.</span></span>
    
    ![NamesUK-BP-configure-1-1](../../media/e5cd0e0c-57f9-4b3d-b1c2-0d6b260f5524.png)
  
2. <span data-ttu-id="f0652-155">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span><span class="sxs-lookup"><span data-stu-id="f0652-155">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="f0652-156">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f0652-156">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-1-2](../../media/b618f8e5-404e-466a-9e71-acd7479f3994.png)
  
3. <span data-ttu-id="f0652-158">Sur la page **Add/Modify DNS Zone (Ajouter/modifier la zone DNS)**, dans la section **Mail exchange records (Enregistrements MX)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f0652-158">On the **Add/Modify DNS Zone** page, in the **Mail exchange records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="f0652-159">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f0652-159">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="f0652-160">**Host name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="f0652-160">**Host name**</span></span>|<span data-ttu-id="f0652-161">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="f0652-161">**Priority**</span></span>|<span data-ttu-id="f0652-162">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="f0652-162">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="f0652-163">(Laissez ce champ vide.)</span><span class="sxs-lookup"><span data-stu-id="f0652-163">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="f0652-164">0,1</span><span class="sxs-lookup"><span data-stu-id="f0652-164">1</span></span>  <br/> <span data-ttu-id="f0652-165">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="f0652-165">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> | <span data-ttu-id="f0652-166">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="f0652-166">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="f0652-167">> [!NOTE]> obtenir votre \* \<clé\> de domaine\* à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="f0652-167">> [!NOTE]> Get your  *\<domain-key\>*  from your Office 365 account.</span></span>           [<span data-ttu-id="f0652-168">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="f0652-168">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
       
    ![NamesUK-BP-configure-2-1](../../media/e211d73d-864f-4114-864b-8e636c69f595.png)
  
4. <span data-ttu-id="f0652-170">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f0652-170">Select **Save**.</span></span>
    
    <span data-ttu-id="f0652-171">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f0652-171">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-2-2](../../media/01e6c801-daa2-40ca-84f9-dcac6422257c.png)
  
5. <span data-ttu-id="f0652-173">Si d'autres enregistrements MX apparaissent dans la section **Mail exchange records (Enregistrements MX)**, supprimez-les en les sélectionnant et en appuyant sur la touche **Suppr** du clavier.</span><span class="sxs-lookup"><span data-stu-id="f0652-173">If there are any other MX records listed in the **Mail exchange records** section, delete each one by selecting it and then pressing the **Delete** key on your keyboard.</span></span> 
    
    ![NamesUK-BP-configure-2-3](../../media/f8e43926-b724-4690-94e7-ec4b8d7a8da5.png)
  
6. <span data-ttu-id="f0652-175">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f0652-175">Select **Save**.</span></span>
    
    <span data-ttu-id="f0652-176">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f0652-176">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-2-4](../../media/cd705919-d0bd-408f-82be-b54e732cb05c.png)
  
## <a name="add-the-six-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="f0652-178">Ajouter les 6 enregistrements CNAME requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="f0652-178">Add the six CNAME records that are required for Office 365</span></span>
<span data-ttu-id="f0652-179"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="f0652-179"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="f0652-p109">Pour commencer, accédez à la page de vos domaines sur le site Names.co.uk en utilisant [ce lien](https://account.names.co.uk/dashboard#/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f0652-p109">To get started, go to your domains page at Names.co.uk by using [this link](https://account.names.co.uk/dashboard#/). You'll be prompted to log in first.</span></span>
    
    ![NamesUK-BP-configure-1-1](../../media/e5cd0e0c-57f9-4b3d-b1c2-0d6b260f5524.png)
  
2. <span data-ttu-id="f0652-183">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span><span class="sxs-lookup"><span data-stu-id="f0652-183">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="f0652-184">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f0652-184">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-1-2](../../media/b618f8e5-404e-466a-9e71-acd7479f3994.png)
  
3. <span data-ttu-id="f0652-186">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="f0652-186">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="f0652-187">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="f0652-187">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    <span data-ttu-id="f0652-188">(Si vous avez besoin d’ajouter une ligne, sélectionnez **Ajouter des enregistrements a/CNAME (+)**.)</span><span class="sxs-lookup"><span data-stu-id="f0652-188">(If you need to add a row, select **ADD A/CNAME RECORDS (+)**.)</span></span>
    
    <span data-ttu-id="f0652-189">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f0652-189">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="f0652-190">**Host Name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="f0652-190">**Host Name**</span></span>|<span data-ttu-id="f0652-191">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="f0652-191">**Type**</span></span>|<span data-ttu-id="f0652-192">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="f0652-192">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="f0652-193">autodiscover</span><span class="sxs-lookup"><span data-stu-id="f0652-193">autodiscover</span></span>  <br/> |<span data-ttu-id="f0652-194">CNAME</span><span class="sxs-lookup"><span data-stu-id="f0652-194">CNAME</span></span>  <br/> |<span data-ttu-id="f0652-195">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="f0652-195">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="f0652-196">sip</span><span class="sxs-lookup"><span data-stu-id="f0652-196">sip</span></span>  <br/> |<span data-ttu-id="f0652-197">CNAME</span><span class="sxs-lookup"><span data-stu-id="f0652-197">CNAME</span></span>  <br/> |<span data-ttu-id="f0652-198">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="f0652-198">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="f0652-199">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="f0652-199">lyncdiscover</span></span>  <br/> |<span data-ttu-id="f0652-200">CNAME</span><span class="sxs-lookup"><span data-stu-id="f0652-200">CNAME</span></span>  <br/> |<span data-ttu-id="f0652-201">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="f0652-201">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="f0652-202">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="f0652-202">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="f0652-203">CNAME</span><span class="sxs-lookup"><span data-stu-id="f0652-203">CNAME</span></span>  <br/> |<span data-ttu-id="f0652-204">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="f0652-204">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="f0652-205">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="f0652-205">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="f0652-206">CNAME</span><span class="sxs-lookup"><span data-stu-id="f0652-206">CNAME</span></span>  <br/> |<span data-ttu-id="f0652-207">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="f0652-207">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
       
    ![NamesUK-BP-configure-3-1](../../media/392772bf-2ed3-4959-9a9a-bb1611905e86.png)
  
4. <span data-ttu-id="f0652-209">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f0652-209">Select **Save**.</span></span>
    
    ![NamesUK-BP-configure-3-2](../../media/c009795e-7eef-4804-bf23-556f498306cc.png)
  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="f0652-211">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="f0652-211">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="f0652-212"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="f0652-212"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="f0652-213">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="f0652-213">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="f0652-214">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="f0652-214">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="f0652-215">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="f0652-215">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="f0652-216">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="f0652-216">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>
  
1. <span data-ttu-id="f0652-p111">Pour commencer, accédez à la page de vos domaines sur le site Names.co.uk en utilisant [ce lien](https://account.names.co.uk/dashboard#/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f0652-p111">To get started, go to your domains page at Names.co.uk by using [this link](https://account.names.co.uk/dashboard#/). You'll be prompted to log in first.</span></span>
    
    ![NamesUK-BP-configure-1-1](../../media/e5cd0e0c-57f9-4b3d-b1c2-0d6b260f5524.png)
  
2. <span data-ttu-id="f0652-220">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span><span class="sxs-lookup"><span data-stu-id="f0652-220">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="f0652-221">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f0652-221">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-1-2](../../media/b618f8e5-404e-466a-9e71-acd7479f3994.png)
  
3. <span data-ttu-id="f0652-223">Sur la page **zones DNS sur le compte** , dans la colonne **nom de domaine** , sélectionnez le nom du domaine que vous mettez à jour.</span><span class="sxs-lookup"><span data-stu-id="f0652-223">On the **DNS Zones on Account** page, in the **Domain name** column, select the name of the domain that you are updating.</span></span> 
    
    ![NamesUK-BP-configure-1-2-1](../../media/20254eec-6952-47ba-b12b-da32860ee7ef.png)
  
4. <span data-ttu-id="f0652-225">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="f0652-225">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="f0652-226">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="f0652-226">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    <span data-ttu-id="f0652-227">(Si vous avez besoin d’ajouter une ligne, sélectionnez **Ajouter des enregistrements a/CNAME (+)**.)</span><span class="sxs-lookup"><span data-stu-id="f0652-227">(If you need to add a row, select **ADD A/CNAME RECORDS (+)**.)</span></span>
    
    <span data-ttu-id="f0652-228">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f0652-228">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="f0652-229">**Host name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="f0652-229">**Host name**</span></span>|<span data-ttu-id="f0652-230">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="f0652-230">**Type**</span></span>|<span data-ttu-id="f0652-231">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="f0652-231">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="f0652-232">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="f0652-232">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="f0652-233">TXT</span><span class="sxs-lookup"><span data-stu-id="f0652-233">TXT</span></span>  <br/> |<span data-ttu-id="f0652-234">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="f0652-234">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="f0652-235">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="f0652-235">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
       
    ![NamesUK-BP-configure-4-1](../../media/cfc61387-630e-4aa0-8762-ef36eaeda44a.png)
  
5. <span data-ttu-id="f0652-237">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f0652-237">Select **Save**.</span></span>
    
    <span data-ttu-id="f0652-238">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f0652-238">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-4-2](../../media/b4d445a1-09c0-46c3-8141-672cc2831a9b.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="f0652-240">Ajoutez les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="f0652-240">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="f0652-241"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="f0652-241"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="f0652-p112">Pour commencer, accédez à la page de vos domaines sur le site Names.co.uk en utilisant [ce lien](https://account.names.co.uk/dashboard#/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f0652-p112">To get started, go to your domains page at Names.co.uk by using [this link](https://account.names.co.uk/dashboard#/). You'll be prompted to log in first.</span></span>
    
    ![NamesUK-BP-configure-1-1](../../media/e5cd0e0c-57f9-4b3d-b1c2-0d6b260f5524.png)
  
2. <span data-ttu-id="f0652-245">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span><span class="sxs-lookup"><span data-stu-id="f0652-245">On the **Dashboard** page, find the name of the domain that you are updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="f0652-246">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f0652-246">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-1-2](../../media/b618f8e5-404e-466a-9e71-acd7479f3994.png)
  
3. <span data-ttu-id="f0652-248">Sur la page **Add/Modify DNS Zone (Ajouter/modifier la zone DNS)**, dans la section **Service records (Enregistrements de service)**, dans les zones des nouveaux enregistrements, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f0652-248">On the **Add/Modify DNS Zone** page, in the **Service records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="f0652-249">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="f0652-249">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="f0652-250">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="f0652-250">**Name**</span></span>|<span data-ttu-id="f0652-251">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="f0652-251">**Priority**</span></span>|<span data-ttu-id="f0652-252">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="f0652-252">**Weight**</span></span>|<span data-ttu-id="f0652-253">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="f0652-253">**Port**</span></span>|<span data-ttu-id="f0652-254">**Result (Résultat)**</span><span class="sxs-lookup"><span data-stu-id="f0652-254">**Result**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f0652-255">_sip. _tls</span><span class="sxs-lookup"><span data-stu-id="f0652-255">_sip._tls</span></span>  <br/> |<span data-ttu-id="f0652-256">100</span><span class="sxs-lookup"><span data-stu-id="f0652-256">100</span></span>  <br/> |<span data-ttu-id="f0652-257">0,1</span><span class="sxs-lookup"><span data-stu-id="f0652-257">1</span></span>  <br/> |<span data-ttu-id="f0652-258">443</span><span class="sxs-lookup"><span data-stu-id="f0652-258">443</span></span>  <br/> |<span data-ttu-id="f0652-259">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="f0652-259">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="f0652-260">_sipfederationtls. _tcp</span><span class="sxs-lookup"><span data-stu-id="f0652-260">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="f0652-261">100</span><span class="sxs-lookup"><span data-stu-id="f0652-261">100</span></span>  <br/> |<span data-ttu-id="f0652-262">0,1</span><span class="sxs-lookup"><span data-stu-id="f0652-262">1</span></span>  <br/> |<span data-ttu-id="f0652-263">5061</span><span class="sxs-lookup"><span data-stu-id="f0652-263">5061</span></span>  <br/> |<span data-ttu-id="f0652-264">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="f0652-264">sipfed.online.lync.com</span></span>  <br/> |
       
    ![NamesUK-BP-configure-5-1](../../media/97a96523-005a-4058-9e12-19f6c3bf9b3b.png)
  
4. <span data-ttu-id="f0652-266">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f0652-266">Select **Save**.</span></span>
    
    <span data-ttu-id="f0652-267">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="f0652-267">(You may have to scroll down.)</span></span>
    
    ![NamesUK-BP-configure-5-2](../../media/bb617a5f-14f9-44b7-9256-bdef34d22d6b.png)
  
> [!NOTE]
>  <span data-ttu-id="f0652-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f0652-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
