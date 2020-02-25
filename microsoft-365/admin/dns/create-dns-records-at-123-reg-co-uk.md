---
title: Créer des enregistrements DNS auprès de 123-reg.co.uk pour Office 365
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
ms.assetid: 1f2d08c9-2a88-4d2f-ae1f-e39f9e358b17
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur 123-reg.co.uk pour Office 365.
ms.openlocfilehash: acbc0f1c8a7eb7dcbe5f274d0f2c8b2c403e7de0
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42243027"
---
# <a name="create-dns-records-at-123-regcouk-for-office-365"></a><span data-ttu-id="ae4be-103">Créer des enregistrements DNS auprès de 123-reg.co.uk pour Office 365</span><span class="sxs-lookup"><span data-stu-id="ae4be-103">Create DNS records at 123-reg.co.uk for Office 365</span></span>

 <span data-ttu-id="ae4be-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="ae4be-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="ae4be-105">Si 123-reg.co.uk est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="ae4be-105">If 123-reg.co.uk is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="ae4be-106">Une fois ces enregistrements ajoutés sur 123-reg.co.uk, votre domaine est configuré pour utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="ae4be-106">After you add these records at 123-reg.co.uk, your domain will be set up to work with Office 365 services.</span></span>
  
<span data-ttu-id="ae4be-107">Pour en savoir plus sur l'hébergement web et le DNS pour les sites web avec Office 365, voir [Utiliser un site web public avec Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span><span class="sxs-lookup"><span data-stu-id="ae4be-107">To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span></span>
  
> [!NOTE]
> <span data-ttu-id="ae4be-108">Typically it takes about 15 minutes for DNS changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="ae4be-108">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="ae4be-109">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="ae4be-109">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="ae4be-110">Si vous rencontrez des problèmes avec le flux de messagerie ou d’autres problèmes après avoir ajouté des enregistrements DNS, consultez [la rubrique Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ae4be-110">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="ae4be-111">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="ae4be-111">Add a TXT record for verification</span></span>
<span data-ttu-id="ae4be-112"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="ae4be-112"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="ae4be-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="ae4be-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ae4be-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="ae4be-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="ae4be-p104">Pour commencer, accédez à la page de vos domaines sur le site 123-reg.co.uk en utilisant [ce lien](https://www.123-reg.co.uk/secure/cpanel/domain/overview). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ae4be-p104">To get started, go to your domains page at 123-reg.co.uk by using [this link](https://www.123-reg.co.uk/secure/cpanel/domain/overview). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="ae4be-119">On the **Domain name overview** page, select the name of the domain that you want to edit.</span><span class="sxs-lookup"><span data-stu-id="ae4be-119">On the **Domain name overview** page, select the name of the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="ae4be-120">Choose **DNS** from the **Select action** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="ae4be-120">Choose **DNS** from the **Select action** drop-down list.</span></span> 
    
4. <span data-ttu-id="ae4be-121">Sur la page **gérer votre DNS** , sélectionnez l’onglet **DNS avancé** .</span><span class="sxs-lookup"><span data-stu-id="ae4be-121">On the **Manage your DNS** page, select the **Advanced DNS** tab.</span></span> 
    
5. <span data-ttu-id="ae4be-122">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="ae4be-122">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="ae4be-123">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="ae4be-123">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    ||||
    |:-----|:-----|:-----|
    |<span data-ttu-id="ae4be-124">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-124">**Hostname**</span></span> <br/> |<span data-ttu-id="ae4be-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-125">**Type**</span></span> <br/> |<span data-ttu-id="ae4be-126">**Destination TXT/SPF**</span><span class="sxs-lookup"><span data-stu-id="ae4be-126">**Destination TXT/SPF**</span></span> <br/> |
    |@  <br/> |<span data-ttu-id="ae4be-127">TXT/SPF</span><span class="sxs-lookup"><span data-stu-id="ae4be-127">TXT/SPF</span></span>  <br/> |<span data-ttu-id="ae4be-128">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="ae4be-128">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="ae4be-129">**Remarque :** Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="ae4be-129">**Note:** This is an example.</span></span> <span data-ttu-id="ae4be-130">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="ae4be-130">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span> [<span data-ttu-id="ae4be-131">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="ae4be-131">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
6. <span data-ttu-id="ae4be-132">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ae4be-132">Select **Add**.</span></span>
    
7. <span data-ttu-id="ae4be-133">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="ae4be-133">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="ae4be-134">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span><span class="sxs-lookup"><span data-stu-id="ae4be-134">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="ae4be-135">When Office 365 finds the correct TXT record, your domain is verified.</span><span class="sxs-lookup"><span data-stu-id="ae4be-135">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="ae4be-136">Dans le centre d’administration, accédez à la page **paramètres** \> des <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="ae4be-136">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="ae4be-137">Dans la page **domaines** , sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="ae4be-137">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="ae4be-138">Sur la page **installation** , sélectionnez **Démarrer l’installation**.</span><span class="sxs-lookup"><span data-stu-id="ae4be-138">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="ae4be-139">Sur la page **vérifier le domaine** , sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="ae4be-139">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="ae4be-140">Typically it takes about 15 minutes for DNS changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="ae4be-140">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="ae4be-141">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="ae4be-141">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="ae4be-142">Si vous rencontrez des problèmes avec le flux de messagerie ou d’autres problèmes après avoir ajouté des enregistrements DNS, consultez [la rubrique Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ae4be-142">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="ae4be-143">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="ae4be-143">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="ae4be-144"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="ae4be-144"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="ae4be-145">Pour commencer, accédez à la page de vos domaines sur le site 123-reg.co.uk en utilisant [ce lien](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span><span class="sxs-lookup"><span data-stu-id="ae4be-145">To get started, go to your domains page at 123-reg.co.uk by using [this link](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span></span> <span data-ttu-id="ae4be-146">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ae4be-146">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="ae4be-147">On the **Domain name overview** page, select the name of the domain that you want to edit.</span><span class="sxs-lookup"><span data-stu-id="ae4be-147">On the **Domain name overview** page, select the name of the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="ae4be-148">Choose **DNS** from the **Select action** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="ae4be-148">Choose **DNS** from the **Select action** drop-down list.</span></span> 
    
4. <span data-ttu-id="ae4be-149">Sur la page **gérer votre DNS** , sélectionnez l’onglet **DNS avancé** .</span><span class="sxs-lookup"><span data-stu-id="ae4be-149">On the **Manage your DNS** page, select the **Advanced DNS** tab.</span></span> 
    
5. <span data-ttu-id="ae4be-150">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="ae4be-150">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="ae4be-151">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="ae4be-151">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="ae4be-152">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-152">**Hostname**</span></span>|<span data-ttu-id="ae4be-153">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-153">**Type**</span></span>|<span data-ttu-id="ae4be-154">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-154">**Priority**</span></span>|<span data-ttu-id="ae4be-155">**Destination MX (Enregistrement MX de la destination)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-155">**Destination MX**</span></span>|
    |:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="ae4be-156">MX</span><span class="sxs-lookup"><span data-stu-id="ae4be-156">MX</span></span>  <br/> |<span data-ttu-id="ae4be-157">0,1</span><span class="sxs-lookup"><span data-stu-id="ae4be-157">1</span></span>  <br/> <span data-ttu-id="ae4be-158">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="ae4be-158">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> | <span data-ttu-id="ae4be-159">*\<clé_de_domaine\>*  .mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="ae4be-159">*\<domain-key\>*  .mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="ae4be-160">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-160">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="ae4be-161">**Remarque :** Obtenez votre \<clé\> de domaine à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="ae4be-161">**Note:** Get your \<domain-key\> from your Office 365 account.</span></span> [<span data-ttu-id="ae4be-162">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="ae4be-162">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Copier et coller des valeurs à partir du tableau](../media/65366165-85a6-4a39-b9a7-6c5f47fbe790.png)
  
6. <span data-ttu-id="ae4be-164">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ae4be-164">Select **Add**.</span></span>
    
    ![Sélectionnez Ajouter](../media/a8ae6c0c-4365-4137-af8a-6e003996e3d0.png)
  
7. <span data-ttu-id="ae4be-166">Si d'autres enregistrements MX sont répertoriés, supprimez-les individuellement en sélectionnant l'icône **Delete (Supprimer)** représentant une corbeille des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="ae4be-166">If there are any other MX records, remove each one by choosing the **Delete (trash can)** icon for that record.</span></span> 
    
    ![Sélectionnez Supprimer (l’icône Corbeille)](../media/3be635e6-b591-49af-8430-a158272834b4.png)
  
## <a name="add-the-six-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="ae4be-168">Ajouter les 6 enregistrements CNAME requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="ae4be-168">Add the six CNAME records that are required for Office 365</span></span>
<span data-ttu-id="ae4be-169"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="ae4be-169"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="ae4be-170">Pour commencer, accédez à la page de vos domaines sur le site 123-reg.co.uk en utilisant [ce lien](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span><span class="sxs-lookup"><span data-stu-id="ae4be-170">To get started, go to your domains page at 123-reg.co.uk by using [this link](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span></span> <span data-ttu-id="ae4be-171">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ae4be-171">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="ae4be-172">On the **Domain name overview** page, select the name of the domain that you want to edit.</span><span class="sxs-lookup"><span data-stu-id="ae4be-172">On the **Domain name overview** page, select the name of the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="ae4be-173">Choose **DNS** from the **Select action** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="ae4be-173">Choose **DNS** from the **Select action** drop-down list.</span></span> 
    
4. <span data-ttu-id="ae4be-174">Sur la page **gérer votre DNS** , sélectionnez l’onglet **DNS avancé** .</span><span class="sxs-lookup"><span data-stu-id="ae4be-174">On the **Manage your DNS** page, select the **Advanced DNS** tab.</span></span> 
    
5. <span data-ttu-id="ae4be-175">Ajoutez le premier des six enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="ae4be-175">Add the first of the six CNAME records.</span></span>
    
    <span data-ttu-id="ae4be-176">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="ae4be-176">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="ae4be-177">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="ae4be-177">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="ae4be-178">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-178">**Hostname**</span></span>|<span data-ttu-id="ae4be-179">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-179">**Type**</span></span>|<span data-ttu-id="ae4be-180">**Destination CNAME (Enregistrement CNAME de la destination)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-180">**Destination CNAME**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="ae4be-181">autodiscover</span><span class="sxs-lookup"><span data-stu-id="ae4be-181">autodiscover</span></span>  <br/> |<span data-ttu-id="ae4be-182">CNAME</span><span class="sxs-lookup"><span data-stu-id="ae4be-182">CNAME</span></span>  <br/> |<span data-ttu-id="ae4be-183">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="ae4be-183">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="ae4be-184">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-184">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="ae4be-185">sip</span><span class="sxs-lookup"><span data-stu-id="ae4be-185">sip</span></span>  <br/> |<span data-ttu-id="ae4be-186">CNAME</span><span class="sxs-lookup"><span data-stu-id="ae4be-186">CNAME</span></span>  <br/> |<span data-ttu-id="ae4be-187">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="ae4be-187">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="ae4be-188">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-188">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="ae4be-189">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="ae4be-189">lyncdiscover</span></span>  <br/> |<span data-ttu-id="ae4be-190">CNAME</span><span class="sxs-lookup"><span data-stu-id="ae4be-190">CNAME</span></span>  <br/> |<span data-ttu-id="ae4be-191">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="ae4be-191">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="ae4be-192">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-192">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="ae4be-193">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="ae4be-193">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="ae4be-194">CNAME</span><span class="sxs-lookup"><span data-stu-id="ae4be-194">CNAME</span></span>  <br/> |<span data-ttu-id="ae4be-195">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="ae4be-195">enterpriseregistration.windows.net.</span></span>  <br/> <span data-ttu-id="ae4be-196">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-196">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="ae4be-197">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="ae4be-197">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="ae4be-198">CNAME</span><span class="sxs-lookup"><span data-stu-id="ae4be-198">CNAME</span></span>  <br/> |<span data-ttu-id="ae4be-199">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="ae4be-199">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> <span data-ttu-id="ae4be-200">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-200">**This value MUST end with a period (.)**</span></span> <br/> |
   
    ![Copiez et collez les valeurs de la table.](../media/24bf388c-5f7f-4fc0-b4ec-4b17226b6246.png)
  
6. <span data-ttu-id="ae4be-202">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ae4be-202">Select **Add**.</span></span>
    
    ![Sélectionnez Ajouter](../media/825a9854-559d-4a22-90ac-5e7a0a54269a.png)
  
7. <span data-ttu-id="ae4be-204">Ajoutez les cinq autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="ae4be-204">Add the other five CNAME records.</span></span>
    
    <span data-ttu-id="ae4be-205">Dans la section **DNS avancé** , créez un enregistrement en utilisant les valeurs de la ligne suivante du tableau, puis sélectionnez de nouveau **Ajouter** pour valider cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ae4be-205">In the **Advanced DNS** section, create a record using the values from the next row in the table, and then again select **Add** to complete that record.</span></span> 
    
    <span data-ttu-id="ae4be-206">Répétez cette procédure jusqu'à avoir créé les 6 enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="ae4be-206">Repeat this process until you have created all six CNAME records.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="ae4be-207">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="ae4be-207">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="ae4be-208"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="ae4be-208"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae4be-209">You cannot have more than one TXT record for SPF for a domain.</span><span class="sxs-lookup"><span data-stu-id="ae4be-209">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="ae4be-210">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span><span class="sxs-lookup"><span data-stu-id="ae4be-210">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="ae4be-211">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="ae4be-211">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="ae4be-212">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="ae4be-212">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> <span data-ttu-id="ae4be-213">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="ae4be-213">Need examples?</span></span> <span data-ttu-id="ae4be-214">Consultez ces [enregistrements DNS externes pour Office 365](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0#bkmk_spfrecords).</span><span class="sxs-lookup"><span data-stu-id="ae4be-214">Check out these [External Domain Name System records for Office 365](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0#bkmk_spfrecords).</span></span> <span data-ttu-id="ae4be-215">Pour valider votre enregistrement SPF, vous pouvez utiliser l'un des outils de [validation SPF suivants](../setup/domains-faq.md).</span><span class="sxs-lookup"><span data-stu-id="ae4be-215">To validate your SPF record, you can use one of these [SPF validation tools](../setup/domains-faq.md).</span></span> 
  
1. <span data-ttu-id="ae4be-216">Pour commencer, accédez à la page de vos domaines sur le site 123-reg.co.uk en utilisant [ce lien](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span><span class="sxs-lookup"><span data-stu-id="ae4be-216">To get started, go to your domains page at 123-reg.co.uk by using [this link](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span></span> <span data-ttu-id="ae4be-217">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ae4be-217">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="ae4be-218">On the **Domain name overview** page, select the name of the domain that you want to edit.</span><span class="sxs-lookup"><span data-stu-id="ae4be-218">On the **Domain name overview** page, select the name of the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="ae4be-219">Choose **DNS** from the **Select action** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="ae4be-219">Choose **DNS** from the **Select action** drop-down list.</span></span> 
    
4. <span data-ttu-id="ae4be-220">Sur la page **gérer votre DNS** , sélectionnez l’onglet **DNS avancé** .</span><span class="sxs-lookup"><span data-stu-id="ae4be-220">On the **Manage your DNS** page, select the **Advanced DNS** tab.</span></span> 
    
5. <span data-ttu-id="ae4be-221">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="ae4be-221">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="ae4be-222">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="ae4be-222">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="ae4be-223">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-223">**Hostname**</span></span>|<span data-ttu-id="ae4be-224">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-224">**Type**</span></span>|<span data-ttu-id="ae4be-225">**Destination TXT/SPF**</span><span class="sxs-lookup"><span data-stu-id="ae4be-225">**Destination TXT/SPF**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="ae4be-226">TXT/SPF</span><span class="sxs-lookup"><span data-stu-id="ae4be-226">TXT/SPF</span></span>  <br/> |<span data-ttu-id="ae4be-227">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="ae4be-227">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="ae4be-228">**Remarque :** Nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="ae4be-228">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![123Reg-BP-configure-4-1](../media/4697701c-eba0-4b03-8d75-4f7fc3bef94a.png)
  
6. <span data-ttu-id="ae4be-230">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ae4be-230">Select **Add**.</span></span>
    
    ![Sélectionnez Ajouter](../media/7906dd91-fd23-44c3-bb37-ef185655c6eb.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="ae4be-232">Ajouter les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="ae4be-232">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="ae4be-233"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="ae4be-233"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="ae4be-234">Pour commencer, accédez à la page de vos domaines sur le site 123-reg.co.uk en utilisant [ce lien](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span><span class="sxs-lookup"><span data-stu-id="ae4be-234">To get started, go to your domains page at 123-reg.co.uk by using [this link](https://www.123-reg.co.uk/secure/cpanel/domain/overview).</span></span> <span data-ttu-id="ae4be-235">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ae4be-235">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="ae4be-236">On the **Domain name overview** page, select the name of the domain that you want to edit.</span><span class="sxs-lookup"><span data-stu-id="ae4be-236">On the **Domain name overview** page, select the name of the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="ae4be-237">Choose **DNS** from the **Select action** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="ae4be-237">Choose **DNS** from the **Select action** drop-down list.</span></span> 
    
4. <span data-ttu-id="ae4be-238">Sur la page **gérer votre DNS** , sélectionnez l’onglet **DNS avancé** .</span><span class="sxs-lookup"><span data-stu-id="ae4be-238">On the **Manage your DNS** page, select the **Advanced DNS** tab.</span></span> 
    
5. <span data-ttu-id="ae4be-239">Ajoutez le premier des deux enregistrements SRV :</span><span class="sxs-lookup"><span data-stu-id="ae4be-239">Add the first of the two SRV records:</span></span>
    
    <span data-ttu-id="ae4be-240">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="ae4be-240">In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="ae4be-241">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="ae4be-241">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    ||||||
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="ae4be-242">Hostname (Nom d'hôte)</span><span class="sxs-lookup"><span data-stu-id="ae4be-242">Hostname</span></span>|<span data-ttu-id="ae4be-243">Type (Type)</span><span class="sxs-lookup"><span data-stu-id="ae4be-243">Type</span></span>|<span data-ttu-id="ae4be-244">Priority (Priorité)</span><span class="sxs-lookup"><span data-stu-id="ae4be-244">Priority</span></span>|<span data-ttu-id="ae4be-245">TTL (Durée de vie)</span><span class="sxs-lookup"><span data-stu-id="ae4be-245">TTL</span></span>|<span data-ttu-id="ae4be-246">Destination SRV (Enregistrement SRV de la destination)</span><span class="sxs-lookup"><span data-stu-id="ae4be-246">Destination SRV</span></span>|
    |<span data-ttu-id="ae4be-247">_sip. _tls</span><span class="sxs-lookup"><span data-stu-id="ae4be-247">_sip._tls</span></span>|<span data-ttu-id="ae4be-248">SRV</span><span class="sxs-lookup"><span data-stu-id="ae4be-248">SRV</span></span>|<span data-ttu-id="ae4be-249">100</span><span class="sxs-lookup"><span data-stu-id="ae4be-249">100</span></span>|<span data-ttu-id="ae4be-250">3600</span><span class="sxs-lookup"><span data-stu-id="ae4be-250">3600</span></span>|<span data-ttu-id="ae4be-251">1 443 sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="ae4be-251">1 443 sipdir.online.lync.com.</span></span> <span data-ttu-id="ae4be-252">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-252">**This value MUST end with a period (.)**</span></span><br> <span data-ttu-id="ae4be-253">**Remarque :** Nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="ae4be-253">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
    |<span data-ttu-id="ae4be-254">_sipfederationtls. _tcp</span><span class="sxs-lookup"><span data-stu-id="ae4be-254">_sipfederationtls._tcp</span></span>|<span data-ttu-id="ae4be-255">SRV</span><span class="sxs-lookup"><span data-stu-id="ae4be-255">SRV</span></span>|<span data-ttu-id="ae4be-256">100</span><span class="sxs-lookup"><span data-stu-id="ae4be-256">100</span></span>|<span data-ttu-id="ae4be-257">3600</span><span class="sxs-lookup"><span data-stu-id="ae4be-257">3600</span></span>|<span data-ttu-id="ae4be-258">1 5061 sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="ae4be-258">1 5061 sipfed.online.lync.com.</span></span> <span data-ttu-id="ae4be-259">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="ae4be-259">**This value MUST end with a period (.)**</span></span> <br> <span data-ttu-id="ae4be-260">**Remarque :** Nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="ae4be-260">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Copiez et collez les valeurs de la table.](../media/c1786b86-52ef-4dca-8b99-b479554fa531.png)
  
6. <span data-ttu-id="ae4be-262">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ae4be-262">Select **Add**.</span></span>
    
    ![Sélectionnez Ajouter](../media/5fd9d3a2-a8bb-466b-829f-b3a6e54b5104.png)
  
7. <span data-ttu-id="ae4be-264">Pour ajouter l'autre enregistrement SRV :</span><span class="sxs-lookup"><span data-stu-id="ae4be-264">To add the other SRV record:</span></span>
    
    <span data-ttu-id="ae4be-265">Dans la section **DNS avancé** , créez un enregistrement en utilisant les valeurs de la deuxième ligne du tableau, puis sélectionnez de nouveau **Ajouter** pour valider cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ae4be-265">In the **Advanced DNS** section, create a record by using the values from the second row in the table, and then again select **Add** to complete that record.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="ae4be-266">Typically it takes about 15 minutes for DNS changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="ae4be-266">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="ae4be-267">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="ae4be-267">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="ae4be-268">Si vous rencontrez des problèmes avec le flux de messagerie ou d’autres problèmes après avoir ajouté des enregistrements DNS, consultez [la rubrique Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ae4be-268">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
