---
title: Créer des enregistrements DNS sur Bluehost pour Microsoft
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
ms.assetid: 657934ff-d9d2-4563-9ccf-ef4832a03a99
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur Bluehost pour Microsoft.
ms.openlocfilehash: c0ba1b876c939632bc6c43a6e0004fbbe23a7723
ms.sourcegitcommit: 628f195cbe3c00910f7350d8b09997a675dde989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "48646234"
---
# <a name="create-dns-records-at-bluehost-for-microsoft"></a><span data-ttu-id="a3549-103">Créer des enregistrements DNS sur Bluehost pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="a3549-103">Create DNS records at Bluehost for Microsoft</span></span>

 <span data-ttu-id="a3549-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="a3549-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="a3549-105">Si Bluehost est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="a3549-105">If Bluehost is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="a3549-106">Une fois ces enregistrements ajoutés sur Bluehost, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a3549-106">After you add these records at Bluehost, your domain will be set up to work with Microsoft services.</span></span>

> [!NOTE]
> <span data-ttu-id="a3549-107">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="a3549-107">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="a3549-108">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="a3549-108">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="a3549-109">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="a3549-109">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="a3549-110">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="a3549-110">Add a TXT record for verification</span></span>
<span data-ttu-id="a3549-111"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="a3549-111"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="a3549-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="a3549-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a3549-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="a3549-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="a3549-116">Pour commencer, accédez à la page de vos domaines sur le site Bluehost en utilisant [ce lien](https://my.bluehost.com/cgi/dm).</span><span class="sxs-lookup"><span data-stu-id="a3549-116">To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm).</span></span> <span data-ttu-id="a3549-117">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="a3549-117">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="a3549-118">Dans la page **domains (domaines)**, dans la zone **domain (domaine)**, recherchez la ligne associée au domaine que vous modifiez, puis cochez la case correspondant à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="a3549-118">On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain.</span></span> 
    
    <span data-ttu-id="a3549-119">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="a3549-119">(You may have to scroll down.)</span></span>
    
3. <span data-ttu-id="a3549-120">Dans la **zone _domain_name_*_, sur la*ligne éditeur de zone DNS** , sélectionnez **gérer les enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="a3549-120">In the **_domain_name_*_ area, on the _\* DNS Zone Editor*\* row, select **Manage DNS records**.</span></span>
    
4. <span data-ttu-id="a3549-121">On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="a3549-121">On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="a3549-122">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="a3549-122">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |||||
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="a3549-123">**Host Record**</span><span class="sxs-lookup"><span data-stu-id="a3549-123">**Host Record**</span></span> <br/> |<span data-ttu-id="a3549-124">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="a3549-124">**TTL**</span></span> <br/> |<span data-ttu-id="a3549-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="a3549-125">**Type**</span></span> <br/> |<span data-ttu-id="a3549-126">**TXT Value**</span><span class="sxs-lookup"><span data-stu-id="a3549-126">**TXT Value**</span></span> <br/> |
    |@  <br/> |<span data-ttu-id="a3549-127">14400</span><span class="sxs-lookup"><span data-stu-id="a3549-127">14400</span></span>  <br/> |<span data-ttu-id="a3549-128">TXT</span><span class="sxs-lookup"><span data-stu-id="a3549-128">TXT</span></span>  <br/> |<span data-ttu-id="a3549-129">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="a3549-129">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="a3549-130">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="a3549-130">**Note:** This is an example.</span></span> <span data-ttu-id="a3549-131">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="a3549-131">Use your specific **Destination or Points to Address** value here, from the table.</span></span> [<span data-ttu-id="a3549-132">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="a3549-132">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
5. <span data-ttu-id="a3549-133">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="a3549-133">Select **add record**.</span></span>
    
6. <span data-ttu-id="a3549-134">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="a3549-134">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="a3549-135">À présent que vous avez ajouté l’enregistrement sur le site de votre bureau d’enregistrement de domaines, vous allez retourner à Microsoft et demander une recherche pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a3549-135">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request a search for the record.</span></span>
  
<span data-ttu-id="a3549-136">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="a3549-136">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="a3549-137">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="a3549-137">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="a3549-138">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="a3549-138">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="a3549-139">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="a3549-139">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="a3549-140">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="a3549-140">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="a3549-141">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="a3549-141">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="a3549-142">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="a3549-142">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="a3549-143">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="a3549-143">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="a3549-144">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="a3549-144">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="a3549-145"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="a3549-145"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="a3549-146">Pour commencer, accédez à la page de vos domaines sur le site Bluehost en utilisant [ce lien](https://my.bluehost.com/cgi/dm).</span><span class="sxs-lookup"><span data-stu-id="a3549-146">To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm).</span></span> <span data-ttu-id="a3549-147">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="a3549-147">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="a3549-148">Dans la page **domains (domaines)**, dans la zone **domain (domaine)**, recherchez la ligne associée au domaine que vous modifiez, puis cochez la case correspondant à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="a3549-148">On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain.</span></span> 
    
    <span data-ttu-id="a3549-149">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="a3549-149">(You may have to scroll down.)</span></span>
    
3. <span data-ttu-id="a3549-150">Dans la **zone _domain_name_*_, sur la*ligne éditeur de zone DNS** , sélectionnez **gérer les enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="a3549-150">In the **_domain_name_*_ area, on the _\* DNS Zone Editor*\* row, select **Manage DNS records**.</span></span>
    
4. <span data-ttu-id="a3549-151">On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="a3549-151">On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="a3549-152">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="a3549-152">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="a3549-153">**Host Record**</span><span class="sxs-lookup"><span data-stu-id="a3549-153">**Host Record**</span></span>|<span data-ttu-id="a3549-154">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="a3549-154">**TTL**</span></span>|<span data-ttu-id="a3549-155">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="a3549-155">**Type**</span></span>|<span data-ttu-id="a3549-156">**Points to (Destination)**</span><span class="sxs-lookup"><span data-stu-id="a3549-156">**Points To**</span></span>|<span data-ttu-id="a3549-157">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="a3549-157">**Priority**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="a3549-158">14400</span><span class="sxs-lookup"><span data-stu-id="a3549-158">14400</span></span>  <br/> |<span data-ttu-id="a3549-159">MX</span><span class="sxs-lookup"><span data-stu-id="a3549-159">MX</span></span>  <br/> | <span data-ttu-id="a3549-160">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="a3549-160">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/><span data-ttu-id="a3549-161">**Remarque :** Obtenez votre \<*domain-key*\> à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a3549-161">**Note:** Get your \<*domain-key*\> from your Microsoft account.</span></span> [<span data-ttu-id="a3549-162">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="a3549-162">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="a3549-163">0</span><span class="sxs-lookup"><span data-stu-id="a3549-163">0</span></span>  <br/> <span data-ttu-id="a3549-164">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span><span class="sxs-lookup"><span data-stu-id="a3549-164">For more information about priority, see [What is MX priority?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span></span> <br/> |
   
   ![Choisissez type dans la liste déroulante.](../../media/70791420-d83c-4a5d-a46c-5cc3bc67f565.png)
  
5. <span data-ttu-id="a3549-166">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="a3549-166">Select **add record**.</span></span>
    
    ![Sélectionnez Ajouter un enregistrement](../../media/c7ef9733-1665-4dbf-accc-caadf1574abc.png)
  
6. <span data-ttu-id="a3549-168">Si d'autres enregistrements MX sont répertoriés dans la section **MX (Mail Exchanger) (MX (Mail Exchanger))**, supprimez-les individuellement.</span><span class="sxs-lookup"><span data-stu-id="a3549-168">If there are any other MX records in the **MX (Mail Exchanger)** section, delete each of them.</span></span> 
    
    <span data-ttu-id="a3549-169">Pour l’un des autres enregistrements MX, sélectionnez **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="a3549-169">For one of the other MX records, select **Delete.**</span></span>
    
    ![Sélectionnez Delete pour chaque enregistrement MX supplémentaire](../../media/6be17f54-3f33-47af-a9db-4689141530c2.png)
  
7. <span data-ttu-id="a3549-171">Dans la boîte de dialogue de confirmation, sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3549-171">In the confirmation dialog box, select **OK**.</span></span>
    
    ![Sélectionnez OK.](../../media/a50df7a3-2906-4cc0-87d4-1231ab234230.png)
  
8. <span data-ttu-id="a3549-173">Utilisez la même procédure pour supprimer tous les enregistrements MX déjà répertoriés.</span><span class="sxs-lookup"><span data-stu-id="a3549-173">Use the same process to delete any other MX records that were already listed.</span></span>
    
## <a name="add-the-six-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="a3549-174">Ajouter les six enregistrements CNAMe requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="a3549-174">Add the six CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="a3549-175"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="a3549-175"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="a3549-176">Pour commencer, accédez à la page de vos domaines sur le site Bluehost en utilisant [ce lien](https://my.bluehost.com/cgi/dm).</span><span class="sxs-lookup"><span data-stu-id="a3549-176">To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm).</span></span> <span data-ttu-id="a3549-177">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="a3549-177">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="a3549-178">Dans la page **domains (domaines)**, dans la zone **domain (domaine)**, recherchez la ligne associée au domaine que vous modifiez, puis cochez la case correspondant à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="a3549-178">On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain.</span></span> 
    
    <span data-ttu-id="a3549-179">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="a3549-179">(You may have to scroll down.)</span></span>
    
3. <span data-ttu-id="a3549-180">Dans la **zone _domain_name_*_, sur la*ligne éditeur de zone DNS** , sélectionnez **gérer les enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="a3549-180">In the **_domain_name_*_ area, on the _\* DNS Zone Editor*\* row, select **Manage DNS records**.</span></span>
    
4. <span data-ttu-id="a3549-181">Dans la section **A (hôte)** , recherchez la ligne de l’enregistrement de **découverte automatique** , puis sélectionnez **supprimer** pour cette ligne.</span><span class="sxs-lookup"><span data-stu-id="a3549-181">In the **A (Host)** records section, find the row for the **autodiscover** record, and then select **delete** for that row.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="a3549-182">Vous devez supprimer l’enregistrement de **découverte automatique** existant  *avant*  d’ajouter l’enregistrement de **découverte automatique** requis par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a3549-182">You must delete the existing **autodiscover** record  *before*  adding the **autodiscover** record that is required by Microsoft.</span></span> <span data-ttu-id="a3549-183">Bluehost ne vous permet pas de conserver deux enregistrements **autodiscover** simultanément.</span><span class="sxs-lookup"><span data-stu-id="a3549-183">Bluehost does not allow you to maintain two **autodiscover** records simultaneously.</span></span> 
  
    ![Sélectionnez Supprimer](../../media/416a447e-3710-4ae7-8bf1-459381af4f6e.png)
  
5. <span data-ttu-id="a3549-185">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3549-185">Select **OK**.</span></span>
    
    ![Sélectionnez OK.](../../media/0c8f409d-c39f-4ed2-9c95-9af3e61c2411.png)
  
6. <span data-ttu-id="a3549-187">Créer le premier des six enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="a3549-187">Create the first of the six CNAME records.</span></span>
    
    <span data-ttu-id="a3549-188">Sur la page **DNS Zone Editor (Éditeur de zone DNS)**, dans la zone **Add DNS Record (Ajouter un enregistrement DNS)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs dans la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a3549-188">On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the first row in the following table.</span></span> 
    
    <span data-ttu-id="a3549-189">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="a3549-189">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="a3549-190">**Host Record**</span><span class="sxs-lookup"><span data-stu-id="a3549-190">**Host Record**</span></span>|<span data-ttu-id="a3549-191">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="a3549-191">**TTL**</span></span>|<span data-ttu-id="a3549-192">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="a3549-192">**Type**</span></span>|<span data-ttu-id="a3549-193">**Points to (Destination)**</span><span class="sxs-lookup"><span data-stu-id="a3549-193">**Points To**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="a3549-194">autodiscover</span><span class="sxs-lookup"><span data-stu-id="a3549-194">autodiscover</span></span>  <br/> |<span data-ttu-id="a3549-195">14400</span><span class="sxs-lookup"><span data-stu-id="a3549-195">14400</span></span>  <br/> |<span data-ttu-id="a3549-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="a3549-196">CNAME</span></span>  <br/> |<span data-ttu-id="a3549-197">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="a3549-197">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="a3549-198">sip</span><span class="sxs-lookup"><span data-stu-id="a3549-198">sip</span></span>  <br/> |<span data-ttu-id="a3549-199">14400</span><span class="sxs-lookup"><span data-stu-id="a3549-199">14400</span></span>  <br/> |<span data-ttu-id="a3549-200">CNAME</span><span class="sxs-lookup"><span data-stu-id="a3549-200">CNAME</span></span>  <br/> |<span data-ttu-id="a3549-201">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="a3549-201">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="a3549-202">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="a3549-202">lyncdiscover</span></span>  <br/> |<span data-ttu-id="a3549-203">14400</span><span class="sxs-lookup"><span data-stu-id="a3549-203">14400</span></span>  <br/> |<span data-ttu-id="a3549-204">CNAME</span><span class="sxs-lookup"><span data-stu-id="a3549-204">CNAME</span></span>  <br/> |<span data-ttu-id="a3549-205">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="a3549-205">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="a3549-206">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="a3549-206">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="a3549-207">14400</span><span class="sxs-lookup"><span data-stu-id="a3549-207">14400</span></span>  <br/> |<span data-ttu-id="a3549-208">CNAME</span><span class="sxs-lookup"><span data-stu-id="a3549-208">CNAME</span></span>  <br/> |<span data-ttu-id="a3549-209">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="a3549-209">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="a3549-210">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="a3549-210">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="a3549-211">14400</span><span class="sxs-lookup"><span data-stu-id="a3549-211">14400</span></span>  <br/> |<span data-ttu-id="a3549-212">CNAME</span><span class="sxs-lookup"><span data-stu-id="a3549-212">CNAME</span></span>  <br/> |<span data-ttu-id="a3549-213">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a3549-213">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
   
    ![Créer le premier enregistrement CNAMe](../../media/4f12e9b1-9dec-4bc2-aa15-8bffa71fe131.png)
  
7. <span data-ttu-id="a3549-215">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="a3549-215">Select **add record**.</span></span>
    
    ![Sélectionnez Ajouter un enregistrement](../../media/c2782250-a9a6-4aee-bb15-f57cb0008587.png)
  
8. <span data-ttu-id="a3549-217">Ajoutez successivement les 5 autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="a3549-217">Add each of the other five CNAME records.</span></span>
    
    <span data-ttu-id="a3549-218">Toujours dans la section **Add DNS record (ajouter un enregistrement DNS** ), créez un enregistrement en utilisant les valeurs de la ligne suivante du tableau, puis sélectionnez de nouveau **Add record (Ajouter** un enregistrement) pour valider cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a3549-218">Still in the **Add DNS Record** section, create a record by using the values from the next row in the table, and then again select **add record** to complete that record.</span></span> 
    
    <span data-ttu-id="a3549-219">Répétez cette procédure jusqu'à avoir créé les 6 enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="a3549-219">Repeat this process until you have created all six CNAME records.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="a3549-220">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="a3549-220">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="a3549-221"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="a3549-221"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="a3549-222">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="a3549-222">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="a3549-223">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a3549-223">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="a3549-224">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a3549-224">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="a3549-225">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="a3549-225">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> <span data-ttu-id="a3549-226">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="a3549-226">Need examples?</span></span> <span data-ttu-id="a3549-227">Consultez ces [Enregistrements DNS externes pour Microsoft](https://docs.microsoft.com/microsoft-365/enterprise/external-domain-name-system-records).</span><span class="sxs-lookup"><span data-stu-id="a3549-227">Check out these [External Domain Name System records for Microsoft](https://docs.microsoft.com/microsoft-365/enterprise/external-domain-name-system-records).</span></span> <span data-ttu-id="a3549-228">Pour valider votre enregistrement SPF, vous pouvez utiliser l’un de ces[outils de validation SPF](../setup/domains-faq.md).</span><span class="sxs-lookup"><span data-stu-id="a3549-228">To validate your SPF record, you can use one of these[SPF validation tools](../setup/domains-faq.md).</span></span> 
  
1. <span data-ttu-id="a3549-229">Pour commencer, accédez à la page de vos domaines sur le site Bluehost en utilisant [ce lien](https://my.bluehost.com/cgi/dm).</span><span class="sxs-lookup"><span data-stu-id="a3549-229">To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm).</span></span> <span data-ttu-id="a3549-230">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="a3549-230">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="a3549-231">Dans la page **domains (domaines)**, dans la zone **domain (domaine)**, recherchez la ligne associée au domaine que vous modifiez, puis cochez la case correspondant à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="a3549-231">On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain.</span></span> 
    
    <span data-ttu-id="a3549-232">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="a3549-232">(You may have to scroll down.)</span></span>
    
3. <span data-ttu-id="a3549-233">Dans la **zone _domain_name_*_, sur la*ligne éditeur de zone DNS** , sélectionnez **gérer les enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="a3549-233">In the **_domain_name_*_ area, on the _\* DNS Zone Editor*\* row, select **Manage DNS records**.</span></span>
    
4. <span data-ttu-id="a3549-234">On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="a3549-234">On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="a3549-235">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="a3549-235">(Choose the **Type** value from the drop-down list.)</span></span> 
        
    |<span data-ttu-id="a3549-236">**Host Record**</span><span class="sxs-lookup"><span data-stu-id="a3549-236">**Host Record**</span></span>|<span data-ttu-id="a3549-237">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="a3549-237">**TTL**</span></span>|<span data-ttu-id="a3549-238">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="a3549-238">**Type**</span></span>|<span data-ttu-id="a3549-239">**TXT Value**</span><span class="sxs-lookup"><span data-stu-id="a3549-239">**TXT Value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="a3549-240">14400</span><span class="sxs-lookup"><span data-stu-id="a3549-240">14400</span></span>  <br/> |<span data-ttu-id="a3549-241">TXT</span><span class="sxs-lookup"><span data-stu-id="a3549-241">TXT</span></span>  <br/> |<span data-ttu-id="a3549-242">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="a3549-242">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/><span data-ttu-id="a3549-243">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="a3549-243">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Copier la valeur TXT](../../media/b2dabd7a-ee3d-4209-aa1e-0233eb8cf3b9.png)
  
5. <span data-ttu-id="a3549-245">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="a3549-245">Select **add record**.</span></span>
    
    ![Sélectionnez Ajouter un enregistrement](../../media/c050e9a2-2274-4640-8f0f-6752d382df5d.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="a3549-247">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="a3549-247">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="a3549-248"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="a3549-248"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="a3549-249">Pour commencer, accédez à la page de vos domaines sur le site Bluehost en utilisant [ce lien](https://my.bluehost.com/cgi/dm).</span><span class="sxs-lookup"><span data-stu-id="a3549-249">To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm).</span></span> <span data-ttu-id="a3549-250">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="a3549-250">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="a3549-251">Dans la page **domains (domaines)**, dans la zone **domain (domaine)**, recherchez la ligne associée au domaine que vous modifiez, puis cochez la case correspondant à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="a3549-251">On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain.</span></span> 
    
    <span data-ttu-id="a3549-252">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="a3549-252">(You may have to scroll down.)</span></span>
    
3. <span data-ttu-id="a3549-253">Dans la **zone _domain_name_*_, sur la*ligne éditeur de zone DNS** , sélectionnez **gérer les enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="a3549-253">In the **_domain_name_*_ area, on the _\* DNS Zone Editor*\* row, select **Manage DNS records**.</span></span>
    
4. <span data-ttu-id="a3549-254">Créez le premier des deux enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="a3549-254">Create the first of the two SRV records.</span></span>
    
    <span data-ttu-id="a3549-255">Sur la page **DNS Zone Editor (Éditeur de zone DNS)**, dans la zone **Add DNS Record (Ajouter un enregistrement DNS)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs dans la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a3549-255">On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the first row in the following table.</span></span> 
    
    <span data-ttu-id="a3549-256">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="a3549-256">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="a3549-257">**Service**</span><span class="sxs-lookup"><span data-stu-id="a3549-257">**Service**</span></span>|<span data-ttu-id="a3549-258">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="a3549-258">**Protocol**</span></span>|<span data-ttu-id="a3549-259">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="a3549-259">**Host**</span></span>|<span data-ttu-id="a3549-260">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="a3549-260">**TTL**</span></span>|<span data-ttu-id="a3549-261">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="a3549-261">**Type**</span></span>|<span data-ttu-id="a3549-262">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="a3549-262">**Priority**</span></span>|<span data-ttu-id="a3549-263">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="a3549-263">**Weight**</span></span>|<span data-ttu-id="a3549-264">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="a3549-264">**Port**</span></span>|<span data-ttu-id="a3549-265">**Points to (Destination)**</span><span class="sxs-lookup"><span data-stu-id="a3549-265">**Points To**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="a3549-266">_sip</span><span class="sxs-lookup"><span data-stu-id="a3549-266">_sip</span></span>  <br/> |<span data-ttu-id="a3549-267">_tls</span><span class="sxs-lookup"><span data-stu-id="a3549-267">_tls</span></span>  <br/> |@  <br/> |<span data-ttu-id="a3549-268">14400</span><span class="sxs-lookup"><span data-stu-id="a3549-268">14400</span></span>  <br/> |<span data-ttu-id="a3549-269">SRV</span><span class="sxs-lookup"><span data-stu-id="a3549-269">SRV</span></span>  <br/> |<span data-ttu-id="a3549-270">100</span><span class="sxs-lookup"><span data-stu-id="a3549-270">100</span></span>  <br/> |<span data-ttu-id="a3549-271">0,1</span><span class="sxs-lookup"><span data-stu-id="a3549-271">1</span></span>  <br/> |<span data-ttu-id="a3549-272">443</span><span class="sxs-lookup"><span data-stu-id="a3549-272">443</span></span>  <br/> |<span data-ttu-id="a3549-273">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="a3549-273">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="a3549-274">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="a3549-274">_sipfederationtls</span></span>  <br/> |<span data-ttu-id="a3549-275">_tcp</span><span class="sxs-lookup"><span data-stu-id="a3549-275">_tcp</span></span>  <br/> |@  <br/> |<span data-ttu-id="a3549-276">14400</span><span class="sxs-lookup"><span data-stu-id="a3549-276">14400</span></span>  <br/> |<span data-ttu-id="a3549-277">SRV</span><span class="sxs-lookup"><span data-stu-id="a3549-277">SRV</span></span>  <br/> |<span data-ttu-id="a3549-278">100</span><span class="sxs-lookup"><span data-stu-id="a3549-278">100</span></span>  <br/> |<span data-ttu-id="a3549-279">0,1</span><span class="sxs-lookup"><span data-stu-id="a3549-279">1</span></span>  <br/> |<span data-ttu-id="a3549-280">5061</span><span class="sxs-lookup"><span data-stu-id="a3549-280">5061</span></span>  <br/> |<span data-ttu-id="a3549-281">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="a3549-281">sipfed.online.lync.com</span></span>  <br/> |
   
    ![Copier la valeur du nouvel enregistrement](../../media/e2911bca-c00b-4b8a-837f-f1d438c474c4.png)
  
5. <span data-ttu-id="a3549-283">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="a3549-283">Select **add record**.</span></span>
    
    ![Sélectionnez Ajouter un enregistrement](../../media/0fd6a587-03fd-4bce-8321-b14e6ad21f5c.png)
  
6. <span data-ttu-id="a3549-285">Ajoutez l’autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="a3549-285">Add the other SRV record.</span></span>
    
    <span data-ttu-id="a3549-286">Toujours dans la section **Add DNS record (ajouter un enregistrement DNS** ), créez un enregistrement en utilisant les valeurs de l’autre ligne du tableau, puis sélectionnez de nouveau **Add record (Ajouter** un enregistrement) pour valider cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a3549-286">Still in the **Add DNS Record** section, create a record by using the values from the other row in the table, and then again select **add record** to complete that record.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="a3549-287">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="a3549-287">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="a3549-288">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="a3549-288">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="a3549-289">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="a3549-289">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  

