---
title: Créer des enregistrements DNS sur 123-reg.co.uk pour Microsoft
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
ms.assetid: 1f2d08c9-2a88-4d2f-ae1f-e39f9e358b17
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur 123-reg.co.uk pour Microsoft.
ms.openlocfilehash: af03f4994868c34ebd76537c21af9e4f3755dd6a
ms.sourcegitcommit: c7f11d851073ef14a69669f6c8b7e0c11e4bb7a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "43939366"
---
# <a name="create-dns-records-at-123-regcouk-for-microsoft"></a><span data-ttu-id="d401e-103">Créer des enregistrements DNS sur 123-reg.co.uk pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="d401e-103">Create DNS records at 123-reg.co.uk for Microsoft</span></span>

 <span data-ttu-id="d401e-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="d401e-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="d401e-105">Si 123-reg.co.uk est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="d401e-105">If 123-reg.co.uk is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="d401e-106">Une fois ces enregistrements ajoutés sur 123-reg.co.uk, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d401e-106">After you add these records at 123-reg.co.uk, your domain will be set up to work with Microsoft services.</span></span>
  
  
> [!NOTE]
> <span data-ttu-id="d401e-107">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="d401e-107">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="d401e-108">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="d401e-108">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="d401e-109">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="d401e-109">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="d401e-110">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="d401e-110">Add a TXT record for verification</span></span>
<span data-ttu-id="d401e-111"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="d401e-111"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="d401e-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="d401e-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d401e-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d401e-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="d401e-p104">Pour commencer, accédez à la page de vos domaines sur le site 123-reg.co.uk en utilisant [ce lien](https://www.123-reg.co.uk/secure/cpanel/domain/overview). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="d401e-p104">To get started, go to your domains page at 123-reg.co.uk by using [this link](https://www.123-reg.co.uk/secure/cpanel/domain/overview). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="d401e-118">On the **Domain name overview** page, select the name of the domain that you want to edit.</span><span class="sxs-lookup"><span data-stu-id="d401e-118">On the **Domain name overview** page, select the name of the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="d401e-119">Choose **DNS** from the **Select action** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="d401e-119">Choose **DNS** from the **Select action** drop-down list.</span></span> 
    
4. <span data-ttu-id="d401e-120">Sur la page **gérer votre DNS** , sélectionnez l’onglet **DNS avancé** .</span><span class="sxs-lookup"><span data-stu-id="d401e-120">On the **Manage your DNS** page, select the **Advanced DNS** tab.</span></span> 
    
5. <span data-ttu-id="d401e-121">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="d401e-121">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="d401e-122">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="d401e-122">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    ||||
    |:-----|:-----|:-----|
    |<span data-ttu-id="d401e-123">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="d401e-123">**Hostname**</span></span> <br/> |<span data-ttu-id="d401e-124">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="d401e-124">**Type**</span></span> <br/> |<span data-ttu-id="d401e-125">**Destination TXT/SPF**</span><span class="sxs-lookup"><span data-stu-id="d401e-125">**Destination TXT/SPF**</span></span> <br/> |
    |@  <br/> |<span data-ttu-id="d401e-126">TXT/SPF</span><span class="sxs-lookup"><span data-stu-id="d401e-126">TXT/SPF</span></span>  <br/> |<span data-ttu-id="d401e-127">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="d401e-127">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="d401e-128">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="d401e-128">**Note:** This is an example.</span></span> <span data-ttu-id="d401e-129">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="d401e-129">Use your specific **Destination or Points to Address** value here, from the table.</span></span> [<span data-ttu-id="d401e-130">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="d401e-130">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
6. <span data-ttu-id="d401e-131">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d401e-131">Select **Add**.</span></span>
    
7. <span data-ttu-id="d401e-132">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="d401e-132">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="d401e-133">À présent que vous avez ajouté l’enregistrement sur le site de votre bureau d’enregistrement de domaines, vous allez retourner à Microsoft et demander une recherche pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d401e-133">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request a search for the record.</span></span>
  
<span data-ttu-id="d401e-134">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="d401e-134">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="d401e-135">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="d401e-135">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="d401e-136">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="d401e-136">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="d401e-137">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="d401e-137">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="d401e-138">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="d401e-138">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="d401e-139">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="d401e-139">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="d401e-140">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="d401e-140">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="d401e-141">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="d401e-141">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="d401e-142">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="d401e-142">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="d401e-143"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="d401e-143"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="d401e-144">Pour commencer, accédez à la page de vos domaines sur le site 123-reg.co.uk en utilisant [ce lien](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span><span class="sxs-lookup"><span data-stu-id="d401e-144">To get started, go to your domains page at 123-reg.co.uk by using [this link](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span></span> <span data-ttu-id="d401e-145">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="d401e-145">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="d401e-146">On the **Domain name overview** page, select the name of the domain that you want to edit.</span><span class="sxs-lookup"><span data-stu-id="d401e-146">On the **Domain name overview** page, select the name of the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="d401e-147">Choose **DNS** from the **Select action** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="d401e-147">Choose **DNS** from the **Select action** drop-down list.</span></span> 
    
4. <span data-ttu-id="d401e-148">Sur la page **gérer votre DNS** , sélectionnez l’onglet **DNS avancé** .</span><span class="sxs-lookup"><span data-stu-id="d401e-148">On the **Manage your DNS** page, select the **Advanced DNS** tab.</span></span> 
    
5. <span data-ttu-id="d401e-149">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="d401e-149">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="d401e-150">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="d401e-150">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="d401e-151">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="d401e-151">**Hostname**</span></span>|<span data-ttu-id="d401e-152">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="d401e-152">**Type**</span></span>|<span data-ttu-id="d401e-153">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="d401e-153">**Priority**</span></span>|<span data-ttu-id="d401e-154">**Destination MX (Enregistrement MX de la destination)**</span><span class="sxs-lookup"><span data-stu-id="d401e-154">**Destination MX**</span></span>|
    |:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="d401e-155">MX</span><span class="sxs-lookup"><span data-stu-id="d401e-155">MX</span></span>  <br/> |<span data-ttu-id="d401e-156">0,1</span><span class="sxs-lookup"><span data-stu-id="d401e-156">1</span></span>  <br/> <span data-ttu-id="d401e-157">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="d401e-157">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> | <span data-ttu-id="d401e-158">*\<clé_de_domaine\>*  .mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="d401e-158">*\<domain-key\>*  .mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="d401e-159">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="d401e-159">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="d401e-160">**Remarque :** Obtenez votre \<clé de domaine\> à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d401e-160">**Note:** Get your \<domain-key\> from your Microsoft account.</span></span> [<span data-ttu-id="d401e-161">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="d401e-161">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Copier et coller des valeurs à partir du tableau](../../media/65366165-85a6-4a39-b9a7-6c5f47fbe790.png)
  
6. <span data-ttu-id="d401e-163">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d401e-163">Select **Add**.</span></span>
    
    ![Sélectionnez Ajouter](../../media/a8ae6c0c-4365-4137-af8a-6e003996e3d0.png)
  
7. <span data-ttu-id="d401e-165">Si d'autres enregistrements MX sont répertoriés, supprimez-les individuellement en sélectionnant l'icône **Delete (Supprimer)** représentant une corbeille des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="d401e-165">If there are any other MX records, remove each one by choosing the **Delete (trash can)** icon for that record.</span></span> 
    
    ![Sélectionnez Supprimer (l’icône Corbeille)](../../media/3be635e6-b591-49af-8430-a158272834b4.png)
  
## <a name="add-the-six-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="d401e-167">Ajouter les six enregistrements CNAMe requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="d401e-167">Add the six CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="d401e-168"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="d401e-168"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="d401e-169">Pour commencer, accédez à la page de vos domaines sur le site 123-reg.co.uk en utilisant [ce lien](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span><span class="sxs-lookup"><span data-stu-id="d401e-169">To get started, go to your domains page at 123-reg.co.uk by using [this link](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span></span> <span data-ttu-id="d401e-170">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="d401e-170">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="d401e-171">On the **Domain name overview** page, select the name of the domain that you want to edit.</span><span class="sxs-lookup"><span data-stu-id="d401e-171">On the **Domain name overview** page, select the name of the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="d401e-172">Choose **DNS** from the **Select action** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="d401e-172">Choose **DNS** from the **Select action** drop-down list.</span></span> 
    
4. <span data-ttu-id="d401e-173">Sur la page **gérer votre DNS** , sélectionnez l’onglet **DNS avancé** .</span><span class="sxs-lookup"><span data-stu-id="d401e-173">On the **Manage your DNS** page, select the **Advanced DNS** tab.</span></span> 
    
5. <span data-ttu-id="d401e-174">Ajoutez le premier des six enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="d401e-174">Add the first of the six CNAME records.</span></span>
    
    <span data-ttu-id="d401e-175">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="d401e-175">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="d401e-176">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="d401e-176">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="d401e-177">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="d401e-177">**Hostname**</span></span>|<span data-ttu-id="d401e-178">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="d401e-178">**Type**</span></span>|<span data-ttu-id="d401e-179">**Destination CNAME (Enregistrement CNAME de la destination)**</span><span class="sxs-lookup"><span data-stu-id="d401e-179">**Destination CNAME**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="d401e-180">autodiscover</span><span class="sxs-lookup"><span data-stu-id="d401e-180">autodiscover</span></span>  <br/> |<span data-ttu-id="d401e-181">CNAME</span><span class="sxs-lookup"><span data-stu-id="d401e-181">CNAME</span></span>  <br/> |<span data-ttu-id="d401e-182">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="d401e-182">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="d401e-183">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="d401e-183">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="d401e-184">sip</span><span class="sxs-lookup"><span data-stu-id="d401e-184">sip</span></span>  <br/> |<span data-ttu-id="d401e-185">CNAME</span><span class="sxs-lookup"><span data-stu-id="d401e-185">CNAME</span></span>  <br/> |<span data-ttu-id="d401e-186">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="d401e-186">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="d401e-187">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="d401e-187">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="d401e-188">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="d401e-188">lyncdiscover</span></span>  <br/> |<span data-ttu-id="d401e-189">CNAME</span><span class="sxs-lookup"><span data-stu-id="d401e-189">CNAME</span></span>  <br/> |<span data-ttu-id="d401e-190">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="d401e-190">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="d401e-191">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="d401e-191">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="d401e-192">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="d401e-192">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="d401e-193">CNAME</span><span class="sxs-lookup"><span data-stu-id="d401e-193">CNAME</span></span>  <br/> |<span data-ttu-id="d401e-194">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="d401e-194">enterpriseregistration.windows.net.</span></span>  <br/> <span data-ttu-id="d401e-195">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="d401e-195">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="d401e-196">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="d401e-196">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="d401e-197">CNAME</span><span class="sxs-lookup"><span data-stu-id="d401e-197">CNAME</span></span>  <br/> |<span data-ttu-id="d401e-198">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="d401e-198">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> <span data-ttu-id="d401e-199">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="d401e-199">**This value MUST end with a period (.)**</span></span> <br/> |
   
    ![Copiez et collez les valeurs de la table.](../../media/24bf388c-5f7f-4fc0-b4ec-4b17226b6246.png)
  
6. <span data-ttu-id="d401e-201">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d401e-201">Select **Add**.</span></span>
    
    ![Sélectionnez Ajouter](../../media/825a9854-559d-4a22-90ac-5e7a0a54269a.png)
  
7. <span data-ttu-id="d401e-203">Ajoutez les cinq autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="d401e-203">Add the other five CNAME records.</span></span>
    
    <span data-ttu-id="d401e-204">Dans la section **DNS avancé** , créez un enregistrement en utilisant les valeurs de la ligne suivante du tableau, puis sélectionnez de nouveau **Ajouter** pour valider cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d401e-204">In the **Advanced DNS** section, create a record using the values from the next row in the table, and then again select **Add** to complete that record.</span></span> 
    
    <span data-ttu-id="d401e-205">Répétez cette procédure jusqu'à avoir créé les 6 enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="d401e-205">Repeat this process until you have created all six CNAME records.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="d401e-206">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="d401e-206">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="d401e-207"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="d401e-207"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="d401e-208">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="d401e-208">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="d401e-209">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="d401e-209">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="d401e-210">Si vous disposez déjà d’un enregistrement SPF pour votre domaine, ne créez pas de nouvel enregistrement pour Microsfot.</span><span class="sxs-lookup"><span data-stu-id="d401e-210">If you already have an SPF record for your domain, don't create a new one for Microsfot.</span></span> <span data-ttu-id="d401e-211">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="d401e-211">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> <span data-ttu-id="d401e-212">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="d401e-212">Need examples?</span></span> <span data-ttu-id="d401e-213">Consultez ces [Enregistrements DNS externes pour Microsoft](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0#bkmk_spfrecords).</span><span class="sxs-lookup"><span data-stu-id="d401e-213">Check out these [External Domain Name System records for Microsoft](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0#bkmk_spfrecords).</span></span> <span data-ttu-id="d401e-214">To validate your SPF record, you can use one of these [SPF validation tools](../setup/domains-faq.md).</span><span class="sxs-lookup"><span data-stu-id="d401e-214">To validate your SPF record, you can use one of these [SPF validation tools](../setup/domains-faq.md).</span></span> 
  
1. <span data-ttu-id="d401e-215">Pour commencer, accédez à la page de vos domaines sur le site 123-reg.co.uk en utilisant [ce lien](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span><span class="sxs-lookup"><span data-stu-id="d401e-215">To get started, go to your domains page at 123-reg.co.uk by using [this link](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span></span> <span data-ttu-id="d401e-216">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="d401e-216">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="d401e-217">On the **Domain name overview** page, select the name of the domain that you want to edit.</span><span class="sxs-lookup"><span data-stu-id="d401e-217">On the **Domain name overview** page, select the name of the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="d401e-218">Choose **DNS** from the **Select action** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="d401e-218">Choose **DNS** from the **Select action** drop-down list.</span></span> 
    
4. <span data-ttu-id="d401e-219">Sur la page **gérer votre DNS** , sélectionnez l’onglet **DNS avancé** .</span><span class="sxs-lookup"><span data-stu-id="d401e-219">On the **Manage your DNS** page, select the **Advanced DNS** tab.</span></span> 
    
5. <span data-ttu-id="d401e-220">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="d401e-220">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="d401e-221">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="d401e-221">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="d401e-222">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="d401e-222">**Hostname**</span></span>|<span data-ttu-id="d401e-223">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="d401e-223">**Type**</span></span>|<span data-ttu-id="d401e-224">**Destination TXT/SPF**</span><span class="sxs-lookup"><span data-stu-id="d401e-224">**Destination TXT/SPF**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="d401e-225">TXT/SPF</span><span class="sxs-lookup"><span data-stu-id="d401e-225">TXT/SPF</span></span>  <br/> |<span data-ttu-id="d401e-226">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="d401e-226">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="d401e-227">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="d401e-227">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![123Reg-BP-configure-4-1](../../media/4697701c-eba0-4b03-8d75-4f7fc3bef94a.png)
  
6. <span data-ttu-id="d401e-229">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d401e-229">Select **Add**.</span></span>
    
    ![Sélectionnez Ajouter](../../media/7906dd91-fd23-44c3-bb37-ef185655c6eb.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="d401e-231">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="d401e-231">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="d401e-232"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="d401e-232"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="d401e-233">Pour commencer, accédez à la page de vos domaines sur le site 123-reg.co.uk en utilisant [ce lien](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span><span class="sxs-lookup"><span data-stu-id="d401e-233">To get started, go to your domains page at 123-reg.co.uk by using [this link](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span></span> <span data-ttu-id="d401e-234">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="d401e-234">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="d401e-235">On the **Domain name overview** page, select the name of the domain that you want to edit.</span><span class="sxs-lookup"><span data-stu-id="d401e-235">On the **Domain name overview** page, select the name of the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="d401e-236">Choose **DNS** from the **Select action** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="d401e-236">Choose **DNS** from the **Select action** drop-down list.</span></span> 
    
4. <span data-ttu-id="d401e-237">Sur la page **gérer votre DNS** , sélectionnez l’onglet **DNS avancé** .</span><span class="sxs-lookup"><span data-stu-id="d401e-237">On the **Manage your DNS** page, select the **Advanced DNS** tab.</span></span> 
    
5. <span data-ttu-id="d401e-238">Ajoutez le premier des deux enregistrements SRV :</span><span class="sxs-lookup"><span data-stu-id="d401e-238">Add the first of the two SRV records:</span></span>
    
    <span data-ttu-id="d401e-239">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="d401e-239">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="d401e-240">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="d401e-240">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    ||||||
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="d401e-241">Hostname (Nom d'hôte)</span><span class="sxs-lookup"><span data-stu-id="d401e-241">Hostname</span></span>|<span data-ttu-id="d401e-242">Type (Type)</span><span class="sxs-lookup"><span data-stu-id="d401e-242">Type</span></span>|<span data-ttu-id="d401e-243">Priority (Priorité)</span><span class="sxs-lookup"><span data-stu-id="d401e-243">Priority</span></span>|<span data-ttu-id="d401e-244">TTL (Durée de vie)</span><span class="sxs-lookup"><span data-stu-id="d401e-244">TTL</span></span>|<span data-ttu-id="d401e-245">Destination SRV (Enregistrement SRV de la destination)</span><span class="sxs-lookup"><span data-stu-id="d401e-245">Destination SRV</span></span>|
    |<span data-ttu-id="d401e-246">_sip. _tls</span><span class="sxs-lookup"><span data-stu-id="d401e-246">_sip._tls</span></span>|<span data-ttu-id="d401e-247">SRV</span><span class="sxs-lookup"><span data-stu-id="d401e-247">SRV</span></span>|<span data-ttu-id="d401e-248">100</span><span class="sxs-lookup"><span data-stu-id="d401e-248">100</span></span>|<span data-ttu-id="d401e-249">3600</span><span class="sxs-lookup"><span data-stu-id="d401e-249">3600</span></span>|<span data-ttu-id="d401e-250">1 443 sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="d401e-250">1 443 sipdir.online.lync.com.</span></span> <span data-ttu-id="d401e-251">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="d401e-251">**This value MUST end with a period (.)**</span></span><br> <span data-ttu-id="d401e-252">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="d401e-252">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
    |<span data-ttu-id="d401e-253">_sipfederationtls. _tcp</span><span class="sxs-lookup"><span data-stu-id="d401e-253">_sipfederationtls._tcp</span></span>|<span data-ttu-id="d401e-254">SRV</span><span class="sxs-lookup"><span data-stu-id="d401e-254">SRV</span></span>|<span data-ttu-id="d401e-255">100</span><span class="sxs-lookup"><span data-stu-id="d401e-255">100</span></span>|<span data-ttu-id="d401e-256">3600</span><span class="sxs-lookup"><span data-stu-id="d401e-256">3600</span></span>|<span data-ttu-id="d401e-257">1 5061 sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="d401e-257">1 5061 sipfed.online.lync.com.</span></span> <span data-ttu-id="d401e-258">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="d401e-258">**This value MUST end with a period (.)**</span></span> <br> <span data-ttu-id="d401e-259">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="d401e-259">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Copiez et collez les valeurs de la table.](../../media/c1786b86-52ef-4dca-8b99-b479554fa531.png)
  
6. <span data-ttu-id="d401e-261">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d401e-261">Select **Add**.</span></span>
    
    ![Sélectionnez Ajouter](../../media/5fd9d3a2-a8bb-466b-829f-b3a6e54b5104.png)
  
7. <span data-ttu-id="d401e-263">Pour ajouter l'autre enregistrement SRV :</span><span class="sxs-lookup"><span data-stu-id="d401e-263">To add the other SRV record:</span></span>
    
    <span data-ttu-id="d401e-264">Dans la section **DNS avancé** , créez un enregistrement en utilisant les valeurs de la deuxième ligne du tableau, puis sélectionnez de nouveau **Ajouter** pour valider cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d401e-264">In the **Advanced DNS** section, create a record by using the values from the second row in the table, and then again select **Add** to complete that record.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="d401e-265">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="d401e-265">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="d401e-266">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="d401e-266">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="d401e-267">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="d401e-267">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
