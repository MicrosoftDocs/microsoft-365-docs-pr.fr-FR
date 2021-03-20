---
title: Créer des enregistrements DNS sur 123-reg.co.uk microsoft
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
ms.assetid: 1f2d08c9-2a88-4d2f-ae1f-e39f9e358b17
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype Entreprise Online et d’autres services sur 123-reg.co.uk pour Microsoft.
ms.openlocfilehash: d1e4d3d01a5e6b4f72c98fe09cf57374dd2417a0
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50910425"
---
# <a name="create-dns-records-at-123-regcouk-for-microsoft"></a><span data-ttu-id="f1cba-103">Créer des enregistrements DNS sur 123-reg.co.uk microsoft</span><span class="sxs-lookup"><span data-stu-id="f1cba-103">Create DNS records at 123-reg.co.uk for Microsoft</span></span>

 <span data-ttu-id="f1cba-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="f1cba-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="f1cba-105">Si 123-reg.co.uk est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="f1cba-105">If 123-reg.co.uk is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="f1cba-106">Une fois ces enregistrements ajoutés 123-reg.co.uk, votre domaine est installé pour fonctionner avec les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f1cba-106">After you add these records at 123-reg.co.uk, your domain will be set up to work with Microsoft services.</span></span>
  
  
> [!NOTE]
> <span data-ttu-id="f1cba-107">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="f1cba-107">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="f1cba-108">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="f1cba-108">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="f1cba-109">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f1cba-109">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="f1cba-110">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="f1cba-110">Add a TXT record for verification</span></span>
<span data-ttu-id="f1cba-111"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="f1cba-111"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="f1cba-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="f1cba-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f1cba-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="f1cba-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="f1cba-p104">Pour commencer, accédez à la page de vos domaines sur le site 123-reg.co.uk en utilisant [ce lien](https://www.123-reg.co.uk/secure/cpanel/domain/overview). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f1cba-p104">To get started, go to your domains page at 123-reg.co.uk by using [this link](https://www.123-reg.co.uk/secure/cpanel/domain/overview). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="f1cba-118">On the **Domain name overview** page, select the name of the domain that you want to edit.</span><span class="sxs-lookup"><span data-stu-id="f1cba-118">On the **Domain name overview** page, select the name of the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="f1cba-119">Choose **DNS** from the **Select action** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="f1cba-119">Choose **DNS** from the **Select action** drop-down list.</span></span> 
    
4. <span data-ttu-id="f1cba-120">Dans la page **Gérer votre DNS,** sélectionnez l’onglet **DNS** avancé.</span><span class="sxs-lookup"><span data-stu-id="f1cba-120">On the **Manage your DNS** page, select the **Advanced DNS** tab.</span></span> 
    
5. <span data-ttu-id="f1cba-121">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="f1cba-121">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="f1cba-122">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="f1cba-122">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    ||||
    |:-----|:-----|:-----|
    |<span data-ttu-id="f1cba-123">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-123">**Hostname**</span></span> <br/> |<span data-ttu-id="f1cba-124">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-124">**Type**</span></span> <br/> |<span data-ttu-id="f1cba-125">**Destination TXT/SPF**</span><span class="sxs-lookup"><span data-stu-id="f1cba-125">**Destination TXT/SPF**</span></span> <br/> |
    |@  <br/> |<span data-ttu-id="f1cba-126">TXT/SPF</span><span class="sxs-lookup"><span data-stu-id="f1cba-126">TXT/SPF</span></span>  <br/> |<span data-ttu-id="f1cba-127">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="f1cba-127">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="f1cba-128">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="f1cba-128">**Note:** This is an example.</span></span> <span data-ttu-id="f1cba-129">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="f1cba-129">Use your specific **Destination or Points to Address** value here, from the table.</span></span> [<span data-ttu-id="f1cba-130">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="f1cba-130">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
6. <span data-ttu-id="f1cba-131">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f1cba-131">Select **Add**.</span></span>
    
7. <span data-ttu-id="f1cba-132">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="f1cba-132">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="f1cba-133">Maintenant que vous avez ajouté l’enregistrement sur le site de votre bureau d’enregistrement de domaines, revenir à Microsoft et demander une recherche pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f1cba-133">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request a search for the record.</span></span>
  
<span data-ttu-id="f1cba-134">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="f1cba-134">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="f1cba-135">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="f1cba-135">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="f1cba-136">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="f1cba-136">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="f1cba-137">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="f1cba-137">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="f1cba-138">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="f1cba-138">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="f1cba-139">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="f1cba-139">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="f1cba-140">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="f1cba-140">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="f1cba-141">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f1cba-141">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="f1cba-142">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="f1cba-142">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="f1cba-143"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="f1cba-143"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="f1cba-p107">Pour commencer, accédez à la page de vos domaines sur le site 123-reg.co.uk en utilisant [ce lien](https://www.123-reg.co.uk/secure/cpanel/domain/overview). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f1cba-p107">To get started, go to your domains page at 123-reg.co.uk by using [this link](https://www.123-reg.co.uk/secure/cpanel/domain/overview). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="f1cba-146">On the **Domain name overview** page, select the name of the domain that you want to edit.</span><span class="sxs-lookup"><span data-stu-id="f1cba-146">On the **Domain name overview** page, select the name of the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="f1cba-147">Choose **DNS** from the **Select action** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="f1cba-147">Choose **DNS** from the **Select action** drop-down list.</span></span> 
    
4. <span data-ttu-id="f1cba-148">Dans la page **Gérer votre DNS,** sélectionnez l’onglet **DNS** avancé.</span><span class="sxs-lookup"><span data-stu-id="f1cba-148">On the **Manage your DNS** page, select the **Advanced DNS** tab.</span></span> 
    
5. <span data-ttu-id="f1cba-149">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="f1cba-149">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="f1cba-150">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="f1cba-150">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="f1cba-151">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-151">**Hostname**</span></span>|<span data-ttu-id="f1cba-152">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-152">**Type**</span></span>|<span data-ttu-id="f1cba-153">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-153">**Priority**</span></span>|<span data-ttu-id="f1cba-154">**Destination MX (Enregistrement MX de la destination)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-154">**Destination MX**</span></span>|
    |:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="f1cba-155">MX</span><span class="sxs-lookup"><span data-stu-id="f1cba-155">MX</span></span>  <br/> |<span data-ttu-id="f1cba-156">1</span><span class="sxs-lookup"><span data-stu-id="f1cba-156">1</span></span>  <br/> <span data-ttu-id="f1cba-157">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](../setup/domains-faq.yml).</span><span class="sxs-lookup"><span data-stu-id="f1cba-157">For more information about priority, see [What is MX priority?](../setup/domains-faq.yml)</span></span> <br/> | <span data-ttu-id="f1cba-158">*\<domain-key\>*  .mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="f1cba-158">*\<domain-key\>*  .mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="f1cba-159">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-159">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="f1cba-160">**Remarque :** Obtenez votre \<domain-key\> depuis votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f1cba-160">**Note:** Get your \<domain-key\> from your Microsoft account.</span></span> [<span data-ttu-id="f1cba-161">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="f1cba-161">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Copier et coller des valeurs à partir du tableau](../../media/65366165-85a6-4a39-b9a7-6c5f47fbe790.png)
  
6. <span data-ttu-id="f1cba-163">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f1cba-163">Select **Add**.</span></span>
    
    ![Capture d’écran de la boîte de dialogue avec le bouton Ajouter sélectionné](../../media/a8ae6c0c-4365-4137-af8a-6e003996e3d0.png)
  
7. <span data-ttu-id="f1cba-165">Si d'autres enregistrements MX sont répertoriés, supprimez-les individuellement en sélectionnant l'icône **Delete (Supprimer)** représentant une corbeille des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="f1cba-165">If there are any other MX records, remove each one by choosing the **Delete (trash can)** icon for that record.</span></span> 
    
    ![Sélectionner Supprimer (icône de la corbeille)](../../media/3be635e6-b591-49af-8430-a158272834b4.png)
  
## <a name="add-the-five-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="f1cba-167">Ajouter les cinq enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="f1cba-167">Add the five CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="f1cba-168"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="f1cba-168"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="f1cba-p109">Pour commencer, accédez à la page de vos domaines sur le site 123-reg.co.uk en utilisant [ce lien](https://www.123-reg.co.uk/secure/cpanel/domain/overview). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f1cba-p109">To get started, go to your domains page at 123-reg.co.uk by using [this link](https://www.123-reg.co.uk/secure/cpanel/domain/overview). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="f1cba-171">On the **Domain name overview** page, select the name of the domain that you want to edit.</span><span class="sxs-lookup"><span data-stu-id="f1cba-171">On the **Domain name overview** page, select the name of the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="f1cba-172">Choose **DNS** from the **Select action** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="f1cba-172">Choose **DNS** from the **Select action** drop-down list.</span></span> 
    
4. <span data-ttu-id="f1cba-173">Dans la page **Gérer votre DNS,** sélectionnez l’onglet **DNS** avancé.</span><span class="sxs-lookup"><span data-stu-id="f1cba-173">On the **Manage your DNS** page, select the **Advanced DNS** tab.</span></span> 
    
5. <span data-ttu-id="f1cba-174">Ajoutez le premier des cinq enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="f1cba-174">Add the first of the five CNAME records.</span></span>
    
    <span data-ttu-id="f1cba-175">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="f1cba-175">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="f1cba-176">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="f1cba-176">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="f1cba-177">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-177">**Hostname**</span></span>|<span data-ttu-id="f1cba-178">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-178">**Type**</span></span>|<span data-ttu-id="f1cba-179">**Destination CNAME (Enregistrement CNAME de la destination)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-179">**Destination CNAME**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="f1cba-180">autodiscover</span><span class="sxs-lookup"><span data-stu-id="f1cba-180">autodiscover</span></span>  <br/> |<span data-ttu-id="f1cba-181">CNAME</span><span class="sxs-lookup"><span data-stu-id="f1cba-181">CNAME</span></span>  <br/> |<span data-ttu-id="f1cba-182">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="f1cba-182">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="f1cba-183">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-183">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="f1cba-184">sip</span><span class="sxs-lookup"><span data-stu-id="f1cba-184">sip</span></span>  <br/> |<span data-ttu-id="f1cba-185">CNAME</span><span class="sxs-lookup"><span data-stu-id="f1cba-185">CNAME</span></span>  <br/> |<span data-ttu-id="f1cba-186">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="f1cba-186">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="f1cba-187">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-187">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="f1cba-188">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="f1cba-188">lyncdiscover</span></span>  <br/> |<span data-ttu-id="f1cba-189">CNAME</span><span class="sxs-lookup"><span data-stu-id="f1cba-189">CNAME</span></span>  <br/> |<span data-ttu-id="f1cba-190">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="f1cba-190">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="f1cba-191">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-191">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="f1cba-192">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="f1cba-192">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="f1cba-193">CNAME</span><span class="sxs-lookup"><span data-stu-id="f1cba-193">CNAME</span></span>  <br/> |<span data-ttu-id="f1cba-194">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="f1cba-194">enterpriseregistration.windows.net.</span></span>  <br/> <span data-ttu-id="f1cba-195">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-195">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="f1cba-196">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="f1cba-196">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="f1cba-197">CNAME</span><span class="sxs-lookup"><span data-stu-id="f1cba-197">CNAME</span></span>  <br/> |<span data-ttu-id="f1cba-198">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="f1cba-198">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> <span data-ttu-id="f1cba-199">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-199">**This value MUST end with a period (.)**</span></span> <br/> |
   
    ![Capture d’écran avec CNAME de destination à copier et coller](../../media/24bf388c-5f7f-4fc0-b4ec-4b17226b6246.png)
  
6. <span data-ttu-id="f1cba-201">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f1cba-201">Select **Add**.</span></span>
    
    ![Capture d’écran pour ajouter la destination CNAME](../../media/825a9854-559d-4a22-90ac-5e7a0a54269a.png)
  
7. <span data-ttu-id="f1cba-203">Ajoutez les quatre autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="f1cba-203">Add the other four CNAME records.</span></span>
    
    <span data-ttu-id="f1cba-204">Dans la section **DNS** avancée, créez un enregistrement à l’aide  des valeurs de la ligne suivante du tableau, puis sélectionnez de nouveau Ajouter pour compléter cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f1cba-204">In the **Advanced DNS** section, create a record using the values from the next row in the table, and then again select **Add** to complete that record.</span></span> 
    
    <span data-ttu-id="f1cba-205">Répétez ce processus jusqu’à ce que vous avez créé les cinq enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="f1cba-205">Repeat this process until you have created all five CNAME records.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="f1cba-206">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="f1cba-206">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="f1cba-207"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="f1cba-207"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1cba-208">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="f1cba-208">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="f1cba-209">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="f1cba-209">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="f1cba-210">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f1cba-210">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="f1cba-211">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel de manière à n’avoir *qu’un seul* enregistrement SPF incluant les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="f1cba-211">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> <span data-ttu-id="f1cba-212">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="f1cba-212">Need examples?</span></span> <span data-ttu-id="f1cba-213">Consultez ces [Enregistrements DNS externes pour Microsoft](../../enterprise/external-domain-name-system-records.md#external-dns-records-required-for-spf).</span><span class="sxs-lookup"><span data-stu-id="f1cba-213">Check out these [External Domain Name System records for Microsoft](../../enterprise/external-domain-name-system-records.md#external-dns-records-required-for-spf).</span></span> <span data-ttu-id="f1cba-214">To validate your SPF record, you can use one of these [SPF validation tools](../setup/domains-faq.yml).</span><span class="sxs-lookup"><span data-stu-id="f1cba-214">To validate your SPF record, you can use one of these [SPF validation tools](../setup/domains-faq.yml).</span></span> 
  
1. <span data-ttu-id="f1cba-215">Pour commencer, accédez à la page de vos domaines sur le site 123-reg.co.uk en utilisant [ce lien](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span><span class="sxs-lookup"><span data-stu-id="f1cba-215">To get started, go to your domains page at 123-reg.co.uk by using [this link](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span></span> <span data-ttu-id="f1cba-216">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f1cba-216">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="f1cba-217">On the **Domain name overview** page, select the name of the domain that you want to edit.</span><span class="sxs-lookup"><span data-stu-id="f1cba-217">On the **Domain name overview** page, select the name of the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="f1cba-218">Choose **DNS** from the **Select action** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="f1cba-218">Choose **DNS** from the **Select action** drop-down list.</span></span> 
    
4. <span data-ttu-id="f1cba-219">Dans la page **Gérer votre DNS,** sélectionnez l’onglet **DNS** avancé.</span><span class="sxs-lookup"><span data-stu-id="f1cba-219">On the **Manage your DNS** page, select the **Advanced DNS** tab.</span></span> 
    
5. <span data-ttu-id="f1cba-220">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="f1cba-220">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="f1cba-221">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="f1cba-221">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="f1cba-222">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-222">**Hostname**</span></span>|<span data-ttu-id="f1cba-223">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-223">**Type**</span></span>|<span data-ttu-id="f1cba-224">**Destination TXT/SPF**</span><span class="sxs-lookup"><span data-stu-id="f1cba-224">**Destination TXT/SPF**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="f1cba-225">TXT/SPF</span><span class="sxs-lookup"><span data-stu-id="f1cba-225">TXT/SPF</span></span>  <br/> |<span data-ttu-id="f1cba-226">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="f1cba-226">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="f1cba-227">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="f1cba-227">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![123Reg-BP-Configure-4-1](../../media/4697701c-eba0-4b03-8d75-4f7fc3bef94a.png)
  
6. <span data-ttu-id="f1cba-229">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f1cba-229">Select **Add**.</span></span>
    
    ![Capture d’écran avec destination TXT/SPF](../../media/7906dd91-fd23-44c3-bb37-ef185655c6eb.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="f1cba-231">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="f1cba-231">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="f1cba-232"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="f1cba-232"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="f1cba-p112">Pour commencer, accédez à la page de vos domaines sur le site 123-reg.co.uk en utilisant [ce lien](https://www.123-reg.co.uk/secure/cpanel/domain/overview). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f1cba-p112">To get started, go to your domains page at 123-reg.co.uk by using [this link](https://www.123-reg.co.uk/secure/cpanel/domain/overview). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="f1cba-235">On the **Domain name overview** page, select the name of the domain that you want to edit.</span><span class="sxs-lookup"><span data-stu-id="f1cba-235">On the **Domain name overview** page, select the name of the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="f1cba-236">Choose **DNS** from the **Select action** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="f1cba-236">Choose **DNS** from the **Select action** drop-down list.</span></span> 
    
4. <span data-ttu-id="f1cba-237">Dans la page **Gérer votre DNS,** sélectionnez l’onglet **DNS** avancé.</span><span class="sxs-lookup"><span data-stu-id="f1cba-237">On the **Manage your DNS** page, select the **Advanced DNS** tab.</span></span> 
    
5. <span data-ttu-id="f1cba-238">Ajoutez le premier des deux enregistrements SRV :</span><span class="sxs-lookup"><span data-stu-id="f1cba-238">Add the first of the two SRV records:</span></span>
    
    <span data-ttu-id="f1cba-239">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="f1cba-239">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="f1cba-240">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="f1cba-240">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    ||||||
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f1cba-241">Hostname (Nom d'hôte)</span><span class="sxs-lookup"><span data-stu-id="f1cba-241">Hostname</span></span>|<span data-ttu-id="f1cba-242">Type (Type)</span><span class="sxs-lookup"><span data-stu-id="f1cba-242">Type</span></span>|<span data-ttu-id="f1cba-243">Priority (Priorité)</span><span class="sxs-lookup"><span data-stu-id="f1cba-243">Priority</span></span>|<span data-ttu-id="f1cba-244">TTL (Durée de vie)</span><span class="sxs-lookup"><span data-stu-id="f1cba-244">TTL</span></span>|<span data-ttu-id="f1cba-245">Destination SRV (Enregistrement SRV de la destination)</span><span class="sxs-lookup"><span data-stu-id="f1cba-245">Destination SRV</span></span>|
    |<span data-ttu-id="f1cba-246">_sip._tls</span><span class="sxs-lookup"><span data-stu-id="f1cba-246">_sip._tls</span></span>|<span data-ttu-id="f1cba-247">SRV</span><span class="sxs-lookup"><span data-stu-id="f1cba-247">SRV</span></span>|<span data-ttu-id="f1cba-248">100</span><span class="sxs-lookup"><span data-stu-id="f1cba-248">100</span></span>|<span data-ttu-id="f1cba-249">3600</span><span class="sxs-lookup"><span data-stu-id="f1cba-249">3600</span></span>|<span data-ttu-id="f1cba-250">1 443 sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="f1cba-250">1 443 sipdir.online.lync.com.</span></span> <span data-ttu-id="f1cba-251">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-251">**This value MUST end with a period (.)**</span></span><br> <span data-ttu-id="f1cba-252">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="f1cba-252">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
    |<span data-ttu-id="f1cba-253">_sipfederationtls._tcp</span><span class="sxs-lookup"><span data-stu-id="f1cba-253">_sipfederationtls._tcp</span></span>|<span data-ttu-id="f1cba-254">SRV</span><span class="sxs-lookup"><span data-stu-id="f1cba-254">SRV</span></span>|<span data-ttu-id="f1cba-255">100</span><span class="sxs-lookup"><span data-stu-id="f1cba-255">100</span></span>|<span data-ttu-id="f1cba-256">3600</span><span class="sxs-lookup"><span data-stu-id="f1cba-256">3600</span></span>|<span data-ttu-id="f1cba-257">1 5061 sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="f1cba-257">1 5061 sipfed.online.lync.com.</span></span> <span data-ttu-id="f1cba-258">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="f1cba-258">**This value MUST end with a period (.)**</span></span> <br> <span data-ttu-id="f1cba-259">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="f1cba-259">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Capture d’écran avec les valeurs DNS du tableau](../../media/c1786b86-52ef-4dca-8b99-b479554fa531.png)
  
6. <span data-ttu-id="f1cba-261">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f1cba-261">Select **Add**.</span></span>
    
    ![Capture d’écran pour ajouter destination SRV](../../media/5fd9d3a2-a8bb-466b-829f-b3a6e54b5104.png)
  
7. <span data-ttu-id="f1cba-263">Pour ajouter l'autre enregistrement SRV :</span><span class="sxs-lookup"><span data-stu-id="f1cba-263">To add the other SRV record:</span></span>
    
    <span data-ttu-id="f1cba-264">Dans la section **DNS** avancée, créez un enregistrement en utilisant les valeurs de la deuxième ligne du tableau, puis sélectionnez de nouveau Ajouter pour compléter cet enregistrement. </span><span class="sxs-lookup"><span data-stu-id="f1cba-264">In the **Advanced DNS** section, create a record by using the values from the second row in the table, and then again select **Add** to complete that record.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="f1cba-265">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="f1cba-265">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="f1cba-266">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="f1cba-266">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="f1cba-267">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f1cba-267">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
