---
title: Créer des enregistrements DNS à 1&1 IONOS pour Microsoft
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
ms.assetid: 5762c3ca-1de2-4999-bfe5-4c5e25a8957e
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype Entreprise Online et d’autres services au niveau 1&1 IONOS pour Microsoft.
ms.openlocfilehash: 123abd6d1d93f80eb73f187b7ff75ccd90d02980
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50910557"
---
# <a name="create-dns-records-at-11-ionos-for-microsoft"></a><span data-ttu-id="61549-103">Créer des enregistrements DNS à 1&1 IONOS pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="61549-103">Create DNS records at 1&1 IONOS for Microsoft</span></span>

 <span data-ttu-id="61549-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="61549-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="61549-105">Notez que 1&1 IONOS n’autorise pas un domaine à avoir un enregistrement MX et un enregistrement CNAME de découverte automatique de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="61549-105">Note that 1&1 IONOS doesn't allow a domain to have both an MX record and a top-level Autodiscover CNAME record.</span></span> <span data-ttu-id="61549-106">Cela limite les méthodes de configuration d’Exchange Online pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="61549-106">This limits the ways in which you can configure Exchange Online for Microsoft.</span></span> <span data-ttu-id="61549-107">Il existe une solution de contournement,  mais nous vous recommandons de l’utiliser uniquement si vous avez déjà de l’expérience dans la création de sous-domaine à 1&1 IONOS.</span><span class="sxs-lookup"><span data-stu-id="61549-107">There is a workaround, but we recommend employing it **only** if you already have experience with creating subdomains at 1&1 IONOS.</span></span> <span data-ttu-id="61549-108">> Si, malgré cette limitation de [service,](../setup/domains-faq.yml) vous choisissez de gérer vos propres enregistrements DNS Microsoft à l’adresse 1&1 IONOS, suivez les étapes de cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="61549-108">> If despite this [service limitation](../setup/domains-faq.yml) you choose to manage your own Microsoft DNS records at 1&1 IONOS, follow the steps in this article to verify your domain and to set up DNS records for email, Skype for Business Online, and so on.</span></span> 
  
<span data-ttu-id="61549-109">Une fois ces enregistrements ajoutés à 1&1 IONOS, votre domaine est installé pour fonctionner avec les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="61549-109">After you add these records at 1&1 IONOS, your domain will be set up to work with Microsoft services.</span></span>
  
  
> [!NOTE]
> <span data-ttu-id="61549-110">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="61549-110">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="61549-111">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="61549-111">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="61549-112">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="61549-112">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="61549-113">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="61549-113">Add a TXT record for verification</span></span>

<span data-ttu-id="61549-p103">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="61549-p103">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="61549-p104">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="61549-p104">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
<span data-ttu-id="61549-118">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 0:42)]().</span><span class="sxs-lookup"><span data-stu-id="61549-118">Follow the steps below or [watch the video (start at 0:42)]().</span></span>
  
1. <span data-ttu-id="61549-119">To get started, go to your domains page at 1&1 IONOS by using [this link](https://my.1and1.com/).</span><span class="sxs-lookup"><span data-stu-id="61549-119">To get started, go to your domains page at 1&1 IONOS by using [this link](https://my.1and1.com/).</span></span> <span data-ttu-id="61549-120">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="61549-120">You'll be prompted to log in.</span></span>
    
2. <span data-ttu-id="61549-121">Sélectionnez **Gérer les domaines.**</span><span class="sxs-lookup"><span data-stu-id="61549-121">Select **Manage domains**.</span></span>
    
3. <span data-ttu-id="61549-122">Dans la page **Centre de domaines,** recherchez le domaine que vous souhaitez mettre à jour, puis sélectionnez le contrôle **Panel** ( **v**) pour ce domaine.</span><span class="sxs-lookup"><span data-stu-id="61549-122">On the **Domain Center** page, find the domain that you want to update, and then select the **Panel** ( **v**) control for that domain.</span></span>
    
4. <span data-ttu-id="61549-123">Dans la **zone Paramètres du domaine,** **sélectionnez Modifier les paramètres DNS.**</span><span class="sxs-lookup"><span data-stu-id="61549-123">In the **Domain Settings** area, select **Edit DNS Settings**.</span></span>
    
5. <span data-ttu-id="61549-124">Dans la section **TXT et enregistrements SRV,** sélectionnez **Ajouter un enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="61549-124">In the **TXT and SRV Records** section, select **Add Record**.</span></span>
    
6. <span data-ttu-id="61549-125">In the **Add Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="61549-125">In the **Add Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="61549-126">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="61549-126">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    ||||
    |:-----|:-----|:-----|
    |<span data-ttu-id="61549-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="61549-127">**Type**</span></span> <br/> |<span data-ttu-id="61549-128">**Prefix (Préfixe)**</span><span class="sxs-lookup"><span data-stu-id="61549-128">**Prefix**</span></span> <br/> |<span data-ttu-id="61549-129">**Name Value (Valeur de nom)**</span><span class="sxs-lookup"><span data-stu-id="61549-129">**Name Value**</span></span> <br/> |
    |<span data-ttu-id="61549-130">TXT</span><span class="sxs-lookup"><span data-stu-id="61549-130">TXT</span></span>  <br/> |<span data-ttu-id="61549-131">(Laissez ce champ vide)</span><span class="sxs-lookup"><span data-stu-id="61549-131">(Leave this field blank)</span></span>  <br/> |<span data-ttu-id="61549-132">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="61549-132">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="61549-133">REMARQUE : il s’agit d’un exemple.</span><span class="sxs-lookup"><span data-stu-id="61549-133">NOTE: This is an example.</span></span> <span data-ttu-id="61549-134">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="61549-134">Use your specific **Destination or Points to Address** value here, from the table.</span></span> [<span data-ttu-id="61549-135">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="61549-135">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
7. <span data-ttu-id="61549-136">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="61549-136">Select **Save**.</span></span>
    
8. <span data-ttu-id="61549-137">Sélectionnez **Enregistrer à** nouveau.</span><span class="sxs-lookup"><span data-stu-id="61549-137">Select **Save** again.</span></span> 
    
9. <span data-ttu-id="61549-138">Dans la **boîte de dialogue Modifier les paramètres DNS,** sélectionnez **Oui.**</span><span class="sxs-lookup"><span data-stu-id="61549-138">In the **Edit DNS Settings** dialog box, select **Yes**.</span></span>
    
10. <span data-ttu-id="61549-139">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="61549-139">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="61549-140">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Microsoft 365 et demandez à Microsoft 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="61549-140">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft 365 and request Microsoft 365 to look for the record.</span></span>
  
<span data-ttu-id="61549-141">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="61549-141">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="61549-142">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="61549-142">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="61549-143">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="61549-143">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="61549-144">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="61549-144">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="61549-145">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="61549-145">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="61549-146">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="61549-146">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="61549-147">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="61549-147">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="61549-148">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="61549-148">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="61549-149">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="61549-149">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="61549-150"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="61549-150"><a name="BKMK_add_MX"> </a></span></span>

<span data-ttu-id="61549-151">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 3:22)]().</span><span class="sxs-lookup"><span data-stu-id="61549-151">Follow the steps below or [watch the video (start at 3:22)]().</span></span>
  
> [!NOTE]
> <span data-ttu-id="61549-152">Si vous vous êtes inscrit auprès 1und1.de, [connectez-vous ici.](https://go.microsoft.com/fwlink/?linkid=859152)</span><span class="sxs-lookup"><span data-stu-id="61549-152">If you've registered with 1und1.de, [sign in here](https://go.microsoft.com/fwlink/?linkid=859152).</span></span> 
  
1. <span data-ttu-id="61549-153">To get started, go to your domains page at 1&1 IONOS by using [this link](https://my.1and1.com/).</span><span class="sxs-lookup"><span data-stu-id="61549-153">To get started, go to your domains page at 1&1 IONOS by using [this link](https://my.1and1.com/).</span></span> <span data-ttu-id="61549-154">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="61549-154">You'll be prompted to log in.</span></span>
    
2. <span data-ttu-id="61549-155">Sélectionnez **Gérer les domaines.**</span><span class="sxs-lookup"><span data-stu-id="61549-155">Select **Manage domains**.</span></span>
    
3. <span data-ttu-id="61549-156">Dans la page **Centre de domaines,** recherchez le domaine que vous souhaitez mettre à jour, puis sélectionnez le contrôle **Panel** ( **v**) pour ce domaine.</span><span class="sxs-lookup"><span data-stu-id="61549-156">On the **Domain Center** page, find the domain that you want to update, and then select the **Panel** ( **v**) control for that domain.</span></span>
    
4. <span data-ttu-id="61549-157">Dans la **zone Paramètres du domaine,** **sélectionnez Modifier les paramètres DNS.**</span><span class="sxs-lookup"><span data-stu-id="61549-157">In the **Domain Settings** area, select **Edit DNS Settings**.</span></span>
    
5. <span data-ttu-id="61549-158">Dans la section MX Records (Enregistrements **MX),** dans la zone **Mail Exchanger (MX Record),** **sélectionnez Other mail server (Autre serveur de messagerie).**</span><span class="sxs-lookup"><span data-stu-id="61549-158">In the **MX Records** section, in the **Mail Exchanger (MX Record)** area, select **Other mail server**.</span></span><br/><span data-ttu-id="61549-159">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="61549-159">(You may have to scroll down.)</span></span><br/><span data-ttu-id="61549-160">![1 &amp; 1-BP-Configure-2-1](../../media/b0db72ae-9431-460f-ba7a-3268590b892e.png)</span><span class="sxs-lookup"><span data-stu-id="61549-160">![1&amp;1-BP-Configure-2-1](../../media/b0db72ae-9431-460f-ba7a-3268590b892e.png)</span></span> <br/>
  
6. <span data-ttu-id="61549-161">Si d'autres enregistrements MX sont déjà répertoriés, supprimez-les en sélectionnant un enregistrement et en appuyant sur la touche **Suppr**.</span><span class="sxs-lookup"><span data-stu-id="61549-161">If there are any MX records already listed, delete each of them by selecting the record and then pressing the **Delete** key on your keyboard.</span></span><br/><span data-ttu-id="61549-162">(Si aucun enregistrement MX n'est déjà répertorié, passez à l'étape suivante.)</span><span class="sxs-lookup"><span data-stu-id="61549-162">(If there are no MX records already listed, continue to the next step.)</span></span><br/><span data-ttu-id="61549-163">![1 &amp; 1-BP-Configure-2-2](../../media/4a39bac7-7310-481d-bda4-1dd5c220c60f.png)</span><span class="sxs-lookup"><span data-stu-id="61549-163">![1&amp;1-BP-Configure-2-2](../../media/4a39bac7-7310-481d-bda4-1dd5c220c60f.png)</span></span><br/>
  
7. <span data-ttu-id="61549-164">Dans les zones de l'enregistrement **MX 1**, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="61549-164">In the boxes for the **MX 1** record, type or copy and paste the values from the following table.</span></span> 
    
    |<span data-ttu-id="61549-165">**MX 1**</span><span class="sxs-lookup"><span data-stu-id="61549-165">**MX 1**</span></span>|<span data-ttu-id="61549-166">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="61549-166">**Priority**</span></span>|
    |:-----|:-----|
    | <span data-ttu-id="61549-167">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="61549-167">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/>  <span data-ttu-id="61549-168">REMARQUE : obtenez le vôtre \<domain-key\> à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="61549-168">NOTE: Get your \<domain-key\> from your Microsoft account.</span></span> [<span data-ttu-id="61549-169">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="61549-169">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="61549-170">10 </span><span class="sxs-lookup"><span data-stu-id="61549-170">10</span></span>  <br/> <span data-ttu-id="61549-171">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](../setup/domains-faq.yml).</span><span class="sxs-lookup"><span data-stu-id="61549-171">For more information about priority, see [What is MX priority?](../setup/domains-faq.yml)</span></span> <br/> | 
    
    ![1 et 1 : configurer 2 et 3](../../media/3afb04d1-7bbf-4147-89ae-561e14ded26d.png)<br/>
  
8. <span data-ttu-id="61549-173">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="61549-173">Select **Save**.</span></span><br/><span data-ttu-id="61549-174">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="61549-174">(You may have to scroll down.)</span></span><br/><span data-ttu-id="61549-175">![1 &amp; 1-BP-Configure-2-4](../../media/355b3ba7-4d2b-45ed-aa17-ac4affb54fe3.png)</span><span class="sxs-lookup"><span data-stu-id="61549-175">![1&amp;1-BP-Configure-2-4](../../media/355b3ba7-4d2b-45ed-aa17-ac4affb54fe3.png)</span></span>
  
9. <span data-ttu-id="61549-176">Dans la **boîte de dialogue Modifier les paramètres DNS,** sélectionnez **Oui.**</span><span class="sxs-lookup"><span data-stu-id="61549-176">In the **Edit DNS Settings** dialog box, select **Yes**.</span></span><br/><span data-ttu-id="61549-177">![Sélection de Oui dans la boîte de dialogue Modifier les paramètres DNS](../../media/920cc95f-fedf-4da2-94a4-9cb41ed49bcf.png)</span><span class="sxs-lookup"><span data-stu-id="61549-177">![Selecting Yes in the Edit DNS Settings dialog box](../../media/920cc95f-fedf-4da2-94a4-9cb41ed49bcf.png)</span></span>
  
## <a name="add-the-six-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="61549-178">Ajouter les six enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="61549-178">Add the six CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="61549-179"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="61549-179"><a name="BKMK_add_CNAME"> </a></span></span>

<span data-ttu-id="61549-180">1&1 IONOS nécessite une solution de contournement afin que vous pouvez utiliser un enregistrement MX avec les enregistrements CNAME requis pour les services de messagerie Microsoft.</span><span class="sxs-lookup"><span data-stu-id="61549-180">1&1 IONOS requires a workaround so that you can use an MX record together with the CNAME records that are required for Microsoft email services.</span></span> <span data-ttu-id="61549-181">Cette solution de contournement nécessite de créer un ensemble de sous-domaine à 1&1 IONOS et de les affecter aux enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="61549-181">This workaround requires you to create a set of subdomains at 1&1 IONOS, and to assign them to CNAME records.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="61549-182">Vérifiez que vous avez au moins deux sous-domaines disponibles avant de commencer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="61549-182">Make sure that you have at least two available subdomains before starting this procedure.</span></span> <span data-ttu-id="61549-183">Nous vous recommandons cette solution uniquement si vous avez déjà de l’expérience dans la création de sous-domaine à 1&1 IONOS.</span><span class="sxs-lookup"><span data-stu-id="61549-183">We recommend this solution only if you already have experience with creating subdomains at 1&1 IONOS.</span></span> 
  
### <a name="basic-cname-records"></a><span data-ttu-id="61549-184">Enregistrements CNAME de base</span><span class="sxs-lookup"><span data-stu-id="61549-184">Basic CNAME records</span></span>

<span data-ttu-id="61549-185">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 3:57)]().</span><span class="sxs-lookup"><span data-stu-id="61549-185">Follow the steps below or [watch the video (start at 3:57)]().</span></span>
  
> [!NOTE]
> <span data-ttu-id="61549-186">Si vous vous êtes inscrit auprès 1und1.de, [connectez-vous ici.](https://go.microsoft.com/fwlink/?linkid=859152)</span><span class="sxs-lookup"><span data-stu-id="61549-186">If you've registered with 1und1.de, [sign in here](https://go.microsoft.com/fwlink/?linkid=859152).</span></span> 
  
1. <span data-ttu-id="61549-187">To get started, go to your domains page at 1&1 IONOS by using [this link](https://my.1and1.com/).</span><span class="sxs-lookup"><span data-stu-id="61549-187">To get started, go to your domains page at 1&1 IONOS by using [this link](https://my.1and1.com/).</span></span> <span data-ttu-id="61549-188">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="61549-188">You'll be prompted to log in.</span></span>
    
2. <span data-ttu-id="61549-189">Sélectionnez **Gérer les domaines.**</span><span class="sxs-lookup"><span data-stu-id="61549-189">Select **Manage domains**.</span></span>
    
3. <span data-ttu-id="61549-190">Dans la page **Centre de domaines,** recherchez le domaine à mettre à jour, puis sélectionnez **Gérer les sous-domaines.**</span><span class="sxs-lookup"><span data-stu-id="61549-190">On the **Domain Center** page, find the domain that you want to update, and then select **Manage Subdomains**.</span></span><br/><span data-ttu-id="61549-191">![1 &amp; 1-BP-Configure-3-0](../../media/d570d03f-5c38-463d-809e-5bb9e4fb2777.png)</span><span class="sxs-lookup"><span data-stu-id="61549-191">![1&amp;1-BP-Configure-3-0](../../media/d570d03f-5c38-463d-809e-5bb9e4fb2777.png)</span></span> <br/><span data-ttu-id="61549-192">Vous allez maintenant créer deux sous-domaines et définir une valeur **Alias (Alias)** pour chaque sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="61549-192">Now you'll create two subdomains and set an **Alias** value for each.</span></span><br/><span data-ttu-id="61549-193">(Ceci est obligatoire car 1&1 IONOS prend en charge un seul enregistrement CNAME de niveau supérieur, mais Microsoft requiert plusieurs enregistrements CNAME.)</span><span class="sxs-lookup"><span data-stu-id="61549-193">(This is required because 1&1 IONOS supports only one top-level CNAME record, but Microsoft requires several CNAME records.)</span></span><br/><span data-ttu-id="61549-194">Tout d'abord, vous devez créer le sous-domaine de découverte automatique.</span><span class="sxs-lookup"><span data-stu-id="61549-194">First, you'll create the Autodiscover subdomain.</span></span>
    
4. <span data-ttu-id="61549-195">Dans la section **Vue d’ensemble du** sous-domaine, **sélectionnez Créer un sous-domaine.**</span><span class="sxs-lookup"><span data-stu-id="61549-195">In the **Subdomain Overview** section, select **Create Subdomain**.</span></span>
    
    ![1&amp;1-BP-Configure-3-1](../../media/95c63639-eb80-443d-8951-98e8b6cdcc4f.png)
  
5. <span data-ttu-id="61549-p113">Dans la zone **Create Subdomain (Créer un sous-domaine)** correspondant au nouveau sous-domaine, tapez ou copiez-collez uniquement la valeur **Create Subdomain (Créer un sous-domaine)** du tableau suivant. (Vous ajouterez la valeur **Alias (Alias)** au cours d'une étape ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="61549-p113">In the **Create Subdomain** box for the new subdomain, type or copy and paste only the **Create Subdomain** value from the following table. (You'll add the **Alias** value in a later step.)</span></span>

    |<span data-ttu-id="61549-199">**Create Subdomain (Créer un sous-domaine)**</span><span class="sxs-lookup"><span data-stu-id="61549-199">**Create Subdomain**</span></span>|<span data-ttu-id="61549-200">**Alias**</span><span class="sxs-lookup"><span data-stu-id="61549-200">**Alias**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="61549-201">autodiscover</span><span class="sxs-lookup"><span data-stu-id="61549-201">autodiscover</span></span>  <br/> |<span data-ttu-id="61549-202">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="61549-202">autodiscover.outlook.com</span></span>   | 

    ![1 &amp; 1-BP-Configure-3-2](../../media/9be45113-ebaf-48e6-983c-a7e6ff9eea45.png)
  
6. <span data-ttu-id="61549-204">Sélectionnez **Créer un sous-domaine.**</span><span class="sxs-lookup"><span data-stu-id="61549-204">Select **Create Subdomain**.</span></span><br/><span data-ttu-id="61549-205">![1 &amp; 1-BP-Configure-3-3](../../media/1e7bc874-f174-4597-8c08-df611d16a74d.png)</span><span class="sxs-lookup"><span data-stu-id="61549-205">![1&amp;1-BP-Configure-3-3](../../media/1e7bc874-f174-4597-8c08-df611d16a74d.png)</span></span>
  
7. <span data-ttu-id="61549-206">Dans la section **Vue** d’ensemble du sous-domaine, recherchez le sous-domaine de découverte automatique que vous avez créé, puis sélectionnez le contrôle **Panel (v)** pour ce sous-domaine. </span><span class="sxs-lookup"><span data-stu-id="61549-206">In the **Subdomain Overview** section, locate the **autodiscover** subdomain that you just created, and then select the **Panel (v)** control for that subdomain.</span></span> <br/><span data-ttu-id="61549-207">![1 &amp; 1-BP-Configure-3-4](../../media/10e2e446-3e54-4fb2-8a29-8c442536cc31.png)</span><span class="sxs-lookup"><span data-stu-id="61549-207">![1&amp;1-BP-Configure-3-4](../../media/10e2e446-3e54-4fb2-8a29-8c442536cc31.png)</span></span>
  
8. <span data-ttu-id="61549-208">Dans la **zone Paramètres du** sous-domaine, **sélectionnez Modifier les paramètres DNS.**</span><span class="sxs-lookup"><span data-stu-id="61549-208">In the **Subdomain Settings** area, select **Edit DNS Settings**.</span></span> <br/><span data-ttu-id="61549-209">![1 &amp; 1-BP-Configure-3-5](../../media/5c602118-b89b-4897-9faf-0736be8a6a0d.png)</span><span class="sxs-lookup"><span data-stu-id="61549-209">![1&amp;1-BP-Configure-3-5](../../media/5c602118-b89b-4897-9faf-0736be8a6a0d.png)</span></span>
  
9. <span data-ttu-id="61549-210">Dans la section **Enregistrements A/AAAA (adresses IP),** dans la zone **Adresse IP (A Record),** sélectionnez **CNAME**.</span><span class="sxs-lookup"><span data-stu-id="61549-210">In the **A/AAAA Records (IP Addresses)** section, in the **IP address (A Record)** area, select **CNAME**.</span></span><br/><span data-ttu-id="61549-211">![1 &amp; 1-BP-Configure-3-6](../../media/7f57f468-fbee-4440-a53d-3e334d8e5b71.png)</span><span class="sxs-lookup"><span data-stu-id="61549-211">![1&amp;1-BP-Configure-3-6](../../media/7f57f468-fbee-4440-a53d-3e334d8e5b71.png)</span></span>
  
10. <span data-ttu-id="61549-212">Dans la zone **Alias: (Alias :)**, tapez ou copiez-collez uniquement la valeur **Alias (Alias)** du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="61549-212">In the **Alias:** box, type or copy and paste only the **Alias** value from the following table.</span></span><br/> 
    
    |<span data-ttu-id="61549-213">**Create Subdomain (Créer un sous-domaine)**</span><span class="sxs-lookup"><span data-stu-id="61549-213">**Create Subdomain**</span></span>|<span data-ttu-id="61549-214">**Alias**</span><span class="sxs-lookup"><span data-stu-id="61549-214">**Alias**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="61549-215">autodiscover</span><span class="sxs-lookup"><span data-stu-id="61549-215">autodiscover</span></span>  <br/> |<span data-ttu-id="61549-216">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="61549-216">autodiscover.outlook.com</span></span>   |

    ![1 &amp; 1-BP-Configure-3-7](../../media/afac3118-3337-4f99-98dd-a7ca930230ce.png)
  
11. <span data-ttu-id="61549-218">Cochez la case correspondant à la clause d'exclusion de responsabilité **I am aware** (J'accepte).</span><span class="sxs-lookup"><span data-stu-id="61549-218">Select the check box for the **I am aware** disclaimer.</span></span><br/><span data-ttu-id="61549-219">![1 &amp; 1-BP-Configure-3-8-1](../../media/6c4cac1a-23f2-4ff3-b2d1-3dca908638d2.png)</span><span class="sxs-lookup"><span data-stu-id="61549-219">![1&amp;1-BP-Configure-3-8-1](../../media/6c4cac1a-23f2-4ff3-b2d1-3dca908638d2.png)</span></span>
  
12. <span data-ttu-id="61549-220">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="61549-220">Select **Save**.</span></span><br/><span data-ttu-id="61549-221">![1 &amp; 1-BP-Configure-3-8-2](../../media/ea1dfc06-c175-4146-ab40-da4d162097e1.png)</span><span class="sxs-lookup"><span data-stu-id="61549-221">![1&amp;1-BP-Configure-3-8-2](../../media/ea1dfc06-c175-4146-ab40-da4d162097e1.png)</span></span>
  
  
### <a name="additional-cname-records"></a><span data-ttu-id="61549-222">Enregistrements CNAME supplémentaires</span><span class="sxs-lookup"><span data-stu-id="61549-222">Additional CNAME records</span></span>

<span data-ttu-id="61549-p114">Les enregistrements CNAME supplémentaires créés au cours de la procédure suivante activent les services Skype Entreprise Online. Vous allez suivre les mêmes étapes que vous avez suivies précédemment pour créer les deux enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="61549-p114">The additional CNAME records created in the following procedure enable Skype for Business Online services. You will employ the same steps that you used to create the two CNAME records you have already created.</span></span>
  
1. <span data-ttu-id="61549-225">Créez le troisième sous-domaine (Lyncdiscover).</span><span class="sxs-lookup"><span data-stu-id="61549-225">Create the third subdomain (Lyncdiscover).</span></span><br/><span data-ttu-id="61549-226">Dans la section **Vue d’ensemble du** sous-domaine, **sélectionnez Créer un sous-domaine.**</span><span class="sxs-lookup"><span data-stu-id="61549-226">On the **Subdomain Overview** section, select **Create Subdomain**.</span></span>
    
2. <span data-ttu-id="61549-p115">Dans la zone **Create Subdomain (Créer un sous-domaine)** correspondant au nouveau sous-domaine, tapez ou copiez-collez uniquement la valeur **Create Subdomain (Créer un sous-domaine)** du tableau suivant. (Vous ajouterez la valeur **Alias (Alias)** au cours d'une étape ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="61549-p115">In the **Create Subdomain** box for the new subdomain, type or copy and paste only the **Create Subdomain** value from the following table. (You'll add the **Alias** value in a later step.)</span></span><br/> 
    
    |<span data-ttu-id="61549-229">**Create Subdomain (Créer un sous-domaine)**</span><span class="sxs-lookup"><span data-stu-id="61549-229">**Create Subdomain**</span></span>|<span data-ttu-id="61549-230">**Alias**</span><span class="sxs-lookup"><span data-stu-id="61549-230">**Alias**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="61549-231">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="61549-231">lyncdiscover</span></span>   |<span data-ttu-id="61549-232">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="61549-232">webdir.online.lync.com</span></span>  |
   
3. <span data-ttu-id="61549-233">Sélectionnez **Créer un sous-domaine.**</span><span class="sxs-lookup"><span data-stu-id="61549-233">Select **Create Subdomain**.</span></span>
    
4. <span data-ttu-id="61549-234">Dans la page **Centre de domaines,** **sélectionnez Gérer les sous-domaines.**</span><span class="sxs-lookup"><span data-stu-id="61549-234">On the **Domain Center** page, select **Manage Subdomains**.</span></span>
    
5. <span data-ttu-id="61549-235">Dans la section **Vue** d’ensemble du sous-domaine, recherchez le sous-domaine **lyncdiscover** que vous avez créé, puis sélectionnez le contrôle **Panel (v)** pour ce sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="61549-235">In the **Subdomain Overview** section, find the **lyncdiscover** subdomain that you just created, and then select the **Panel (v)** control for that subdomain.</span></span> <br/><span data-ttu-id="61549-236">Dans la **zone Paramètres du** sous-domaine, **sélectionnez Modifier les paramètres DNS.**</span><span class="sxs-lookup"><span data-stu-id="61549-236">In the **Subdomain Settings** area, select **Edit DNS Settings**.</span></span>
    
6. <span data-ttu-id="61549-237">Dans la section **Enregistrements A/AAAA (adresses IP),** dans la zone **Adresse IP (A Record),** sélectionnez **CNAME**.</span><span class="sxs-lookup"><span data-stu-id="61549-237">In the **A/AAAA Records (IP Addresses)** section, in the **IP address (A Record)** area, select **CNAME**.</span></span>
    
7. <span data-ttu-id="61549-238">Dans la zone **Alias: (Alias :)**, tapez ou copiez-collez uniquement la valeur **Alias (Alias)** du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="61549-238">In the **Alias:** box, type or copy and paste only the **Alias** value from the following table.</span></span> <br/>
    
    |<span data-ttu-id="61549-239">**Create Subdomain (Créer un sous-domaine)**</span><span class="sxs-lookup"><span data-stu-id="61549-239">**Create Subdomain**</span></span>|<span data-ttu-id="61549-240">**Alias**</span><span class="sxs-lookup"><span data-stu-id="61549-240">**Alias**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="61549-241">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="61549-241">lyncdiscover</span></span>  <br/> |<span data-ttu-id="61549-242">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="61549-242">webdir.online.lync.com</span></span>  <br/> |
   
8. <span data-ttu-id="61549-243">Cochez la case de la clause **d’exclusion** de responsabilité, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="61549-243">Select the check box for the **I am aware** disclaimer, and then select **Save**.</span></span>
    
9. <span data-ttu-id="61549-244">Dans la **boîte de dialogue Modifier les paramètres DNS,** sélectionnez **Oui.**</span><span class="sxs-lookup"><span data-stu-id="61549-244">In the **Edit DNS Settings** dialog box, select **Yes**.</span></span>
    
10. <span data-ttu-id="61549-245">Créez le quatrième sous-domaine (SIP) :</span><span class="sxs-lookup"><span data-stu-id="61549-245">Create the fourth subdomain (SIP):</span></span> <br/><span data-ttu-id="61549-246">Dans la section **Vue d’ensemble du** sous-domaine, **sélectionnez Créer un sous-domaine.**</span><span class="sxs-lookup"><span data-stu-id="61549-246">In the **Subdomain Overview** section, select **Create Subdomain**.</span></span>
    
11. <span data-ttu-id="61549-p116">Dans la zone **Create Subdomain (Créer un sous-domaine)** correspondant au nouveau sous-domaine, tapez ou copiez-collez uniquement la valeur **Create Subdomain (Créer un sous-domaine)** du tableau suivant. (Vous ajouterez la valeur **Alias (Alias)** au cours d'une étape ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="61549-p116">In the **Create Subdomain** box for the new subdomain, type or copy and paste only the **Create Subdomain** value from the following table. (You'll add the **Alias** value in a later step.) </span></span><br/>
    
    |<span data-ttu-id="61549-249">**Create Subdomain (Créer un sous-domaine)**</span><span class="sxs-lookup"><span data-stu-id="61549-249">**Create Subdomain**</span></span>|<span data-ttu-id="61549-250">**Alias**</span><span class="sxs-lookup"><span data-stu-id="61549-250">**Alias**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="61549-251">sip</span><span class="sxs-lookup"><span data-stu-id="61549-251">sip</span></span>  <br/> |<span data-ttu-id="61549-252">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="61549-252">sipdir.online.lync.com</span></span>  <br/> |
   
12. <span data-ttu-id="61549-253">Sélectionnez **Créer un sous-domaine.**</span><span class="sxs-lookup"><span data-stu-id="61549-253">Select **Create Subdomain**.</span></span>
    
13. <span data-ttu-id="61549-254">Dans la page **Centre de domaines,** **sélectionnez Gérer les sous-domaines.**</span><span class="sxs-lookup"><span data-stu-id="61549-254">On the **Domain Center** page, select **Manage Subdomains**.</span></span>
    
14. <span data-ttu-id="61549-255">Dans la section **Vue d’ensemble** du sous-domaine, recherchez le sous-domaine **sip** que vous avez créé, puis sélectionnez le contrôle **Panel (v)** pour ce sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="61549-255">In the **Subdomain Overview** section, find the **sip** subdomain that you just created, and then select the **Panel (v)** control for that subdomain.</span></span> <br/><span data-ttu-id="61549-256">Dans la **zone Paramètres du** sous-domaine, **sélectionnez Modifier les paramètres DNS.**</span><span class="sxs-lookup"><span data-stu-id="61549-256">In the **Subdomain Settings** area, select **Edit DNS Settings**.</span></span>
    
15. <span data-ttu-id="61549-257">Dans la section **Enregistrements A/AAAA (adresses IP),** dans la zone **Adresse IP (A Record),** sélectionnez **CNAME**.</span><span class="sxs-lookup"><span data-stu-id="61549-257">In the **A/AAAA Records (IP Addresses)** section, in the **IP address (A Record)** area, select **CNAME**.</span></span>
    
16. <span data-ttu-id="61549-258">Dans la zone **Alias: (Alias :)**, tapez ou copiez-collez uniquement la valeur **Alias (Alias)** du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="61549-258">In the **Alias:** box, type or copy and paste only the **Alias** value from the following table.</span></span> 
    
    |<span data-ttu-id="61549-259">**Create Subdomain (Créer un sous-domaine)**</span><span class="sxs-lookup"><span data-stu-id="61549-259">**Create Subdomain**</span></span>|<span data-ttu-id="61549-260">**Alias**</span><span class="sxs-lookup"><span data-stu-id="61549-260">**Alias**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="61549-261">sip</span><span class="sxs-lookup"><span data-stu-id="61549-261">sip</span></span>  <br/> |<span data-ttu-id="61549-262">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="61549-262">sipdir.online.lync.com</span></span>  <br/> |
   
17. <span data-ttu-id="61549-263">Cochez la case de la clause **d’exclusion** de responsabilité, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="61549-263">Select the check box for the **I am aware** disclaimer, and then select **Save**.</span></span>
    
18. <span data-ttu-id="61549-264">Dans la **boîte de dialogue Modifier les paramètres DNS,** sélectionnez **Oui.**</span><span class="sxs-lookup"><span data-stu-id="61549-264">In the **Edit DNS Settings** dialog box, select **Yes**.</span></span>
    
### <a name="cname-records-needed-for-mdm"></a><span data-ttu-id="61549-265">Enregistrements CNAME requis pour la gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="61549-265">CNAME records needed for MDM</span></span>

> [!IMPORTANT]
> <span data-ttu-id="61549-266">Suivez la procédure que vous avez utilisée pour les quatre autres enregistrements CNAME, mais fournissez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="61549-266">Follow the procedure that you used for the other four CNAME records, but supply the values from the following table.</span></span> 
  
|<span data-ttu-id="61549-267">**Create Subdomain (Créer un sous-domaine)**</span><span class="sxs-lookup"><span data-stu-id="61549-267">**Create Subdomain**</span></span>|<span data-ttu-id="61549-268">**Alias**</span><span class="sxs-lookup"><span data-stu-id="61549-268">**Alias**</span></span>|
|:-----|:-----|
|<span data-ttu-id="61549-269">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="61549-269">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="61549-270">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="61549-270">enterpriseregistration.windows.net</span></span>  <br/> |
|<span data-ttu-id="61549-271">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="61549-271">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="61549-272">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="61549-272">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
   
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="61549-273">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="61549-273">Add a TXT record for SPF to help prevent email spam</span></span>

> [!IMPORTANT]
> <span data-ttu-id="61549-274">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="61549-274">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="61549-275">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="61549-275">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="61549-276">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="61549-276">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="61549-277">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel de manière à n’avoir *qu’un seul* enregistrement SPF incluant les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="61549-277">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> <span data-ttu-id="61549-278">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="61549-278">Need examples?</span></span> <span data-ttu-id="61549-279">Consultez ces [Enregistrements DNS externes pour Microsoft](../../enterprise/external-domain-name-system-records.md).</span><span class="sxs-lookup"><span data-stu-id="61549-279">Check out these [External Domain Name System records for Microsoft](../../enterprise/external-domain-name-system-records.md).</span></span> <span data-ttu-id="61549-280">Pour valider votre enregistrement SPF, vous pouvez utiliser l’un de ces outils[de validation SPF.](../setup/domains-faq.yml)</span><span class="sxs-lookup"><span data-stu-id="61549-280">To validate your SPF record, you can use one of these[SPF validation tools](../setup/domains-faq.yml).</span></span> 
  
<span data-ttu-id="61549-281">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 5:09)]().</span><span class="sxs-lookup"><span data-stu-id="61549-281">Follow the steps below or [watch the video (start at 5:09)]().</span></span>
  
> [!NOTE]
> <span data-ttu-id="61549-282">Si vous vous êtes inscrit auprès 1und1.de, [connectez-vous ici.](https://go.microsoft.com/fwlink/?linkid=859152)</span><span class="sxs-lookup"><span data-stu-id="61549-282">If you've registered with 1und1.de, [sign in here](https://go.microsoft.com/fwlink/?linkid=859152).</span></span> 
  
1. <span data-ttu-id="61549-283">To get started, go to your domains page at 1&1 IONOS by using [this link](https://my.1and1.com/).</span><span class="sxs-lookup"><span data-stu-id="61549-283">To get started, go to your domains page at 1&1 IONOS by using [this link](https://my.1and1.com/).</span></span> <span data-ttu-id="61549-284">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="61549-284">You'll be prompted to log in.</span></span>
    
2. <span data-ttu-id="61549-285">Sélectionnez **Gérer les domaines.**</span><span class="sxs-lookup"><span data-stu-id="61549-285">Select **Manage domains**.</span></span>
    
3. <span data-ttu-id="61549-286">Dans la page **Centre de domaines,** recherchez le domaine que vous souhaitez mettre à jour, puis sélectionnez le contrôle **Panel** (**v**) pour ce domaine.</span><span class="sxs-lookup"><span data-stu-id="61549-286">On the **Domain Center** page, find the domain that you want to update, and then select the **Panel** (**v**) control for that domain.</span></span>
    
4. <span data-ttu-id="61549-287">Dans la **zone Paramètres du domaine,** **sélectionnez Modifier les paramètres DNS.**</span><span class="sxs-lookup"><span data-stu-id="61549-287">In the **Domain Settings** area, select **Edit DNS Settings**.</span></span>
    
5. <span data-ttu-id="61549-288">Dans la section **TXT et enregistrements SRV,** sélectionnez **Ajouter un enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="61549-288">In the **TXT and SRV Records** section, select **Add Record**.</span></span> <br/><span data-ttu-id="61549-289">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="61549-289">(You may have to scroll down.)</span></span>
    
6. <span data-ttu-id="61549-290">In the **Add Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="61549-290">In the **Add Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> <br/><span data-ttu-id="61549-291">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="61549-291">(Choose the **Type** value from the drop-down list.)</span></span> <br/>
    
    |<span data-ttu-id="61549-292">**Type**</span><span class="sxs-lookup"><span data-stu-id="61549-292">**Type**</span></span>|<span data-ttu-id="61549-293">**Prefix (Préfixe)**</span><span class="sxs-lookup"><span data-stu-id="61549-293">**Prefix**</span></span>|<span data-ttu-id="61549-294">**Name Value (Valeur de nom)**</span><span class="sxs-lookup"><span data-stu-id="61549-294">**Name Value**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="61549-295">TXT</span><span class="sxs-lookup"><span data-stu-id="61549-295">TXT</span></span>  <br/> |<span data-ttu-id="61549-296">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="61549-296">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="61549-297">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="61549-297">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="61549-298">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="61549-298">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           | 
    
    ![Enregistrement TXT](../../media/0b3ba3b4-64b9-4d68-9ee1-04eb3a17d4c5.png)
  
7. <span data-ttu-id="61549-300">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="61549-300">Select **Save**.</span></span><br/><span data-ttu-id="61549-301">![Ajouter un enregistrement](../../media/0f222eb9-3bfd-4908-9a99-516cc6fb1d0e.png)</span><span class="sxs-lookup"><span data-stu-id="61549-301">![Add record](../../media/0f222eb9-3bfd-4908-9a99-516cc6fb1d0e.png)</span></span>
  
8. <span data-ttu-id="61549-302">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="61549-302">Select **Save**.</span></span><br/><span data-ttu-id="61549-303">![Enregistrer un enregistrement](../../media/86ed1b59-31b2-4094-9cd4-32b94eb09e35.png)</span><span class="sxs-lookup"><span data-stu-id="61549-303">![Save record](../../media/86ed1b59-31b2-4094-9cd4-32b94eb09e35.png)</span></span>
  
9. <span data-ttu-id="61549-304">Dans la **boîte de dialogue Modifier les paramètres DNS,** sélectionnez **Oui.**</span><span class="sxs-lookup"><span data-stu-id="61549-304">In the **Edit DNS Settings** dialog box, select **Yes**.</span></span><br/><span data-ttu-id="61549-305">![Sélection de Oui dans la boîte de dialogue Modifier les paramètres DNS](../../media/920cc95f-fedf-4da2-94a4-9cb41ed49bcf.png)</span><span class="sxs-lookup"><span data-stu-id="61549-305">![Selecting Yes in the Edit DNS Settings dialog box](../../media/920cc95f-fedf-4da2-94a4-9cb41ed49bcf.png)</span></span>
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="61549-306">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="61549-306">Add the two SRV records that are required for Microsoft</span></span>

<span data-ttu-id="61549-307">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 5:51)]().</span><span class="sxs-lookup"><span data-stu-id="61549-307">Follow the steps below or [watch the video (start at 5:51)]().</span></span>
  
> [!NOTE]
> <span data-ttu-id="61549-308">Si vous vous êtes inscrit auprès 1und1.de, [connectez-vous ici.](https://go.microsoft.com/fwlink/?linkid=859152)</span><span class="sxs-lookup"><span data-stu-id="61549-308">If you've registered with 1und1.de, [sign in here](https://go.microsoft.com/fwlink/?linkid=859152).</span></span> 
  
1. <span data-ttu-id="61549-309">To get started, go to your domains page at 1&1 IONOS by using [this link](https://my.1and1.com/).</span><span class="sxs-lookup"><span data-stu-id="61549-309">To get started, go to your domains page at 1&1 IONOS by using [this link](https://my.1and1.com/).</span></span> <span data-ttu-id="61549-310">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="61549-310">You'll be prompted to log in.</span></span>
    
2. <span data-ttu-id="61549-311">Sélectionnez **Gérer les domaines.**</span><span class="sxs-lookup"><span data-stu-id="61549-311">Select **Manage domains**.</span></span>
    
3. <span data-ttu-id="61549-312">Dans la page **Centre de domaines,** recherchez le domaine que vous souhaitez mettre à jour, puis sélectionnez le contrôle **Panel** ( **v**) pour ce domaine.</span><span class="sxs-lookup"><span data-stu-id="61549-312">On the **Domain Center** page, find the domain that you want to update, and then select the **Panel** ( **v**) control for that domain.</span></span>
    
4. <span data-ttu-id="61549-313">Dans la **zone Paramètres du domaine,** **sélectionnez Modifier les paramètres DNS.**</span><span class="sxs-lookup"><span data-stu-id="61549-313">In the **Domain Settings** area, select **Edit DNS Settings**.</span></span>
    
5. <span data-ttu-id="61549-314">Dans la section **TXT et enregistrements SRV,** sélectionnez **Ajouter un enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="61549-314">In the **TXT and SRV Records** section, select **Add Record**.</span></span>
    
6. <span data-ttu-id="61549-315">Ajoutez le premier des deux enregistrements SRV :</span><span class="sxs-lookup"><span data-stu-id="61549-315">Add the first of the two SRV records.</span></span><br/><span data-ttu-id="61549-316">Dans la zone **Add Record (Ajouter un enregistrement)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="61549-316">In the **Add Record** area, in the boxes for the new record, type or copy and paste the values from the first row in the following table.</span></span> <br/><span data-ttu-id="61549-317">(Choisissez les **valeurs Type** et **TTL** dans la liste liste.)</span><span class="sxs-lookup"><span data-stu-id="61549-317">(Choose the **Type** and **TTL** values from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="61549-318">**Type**</span><span class="sxs-lookup"><span data-stu-id="61549-318">**Type**</span></span>|<span data-ttu-id="61549-319">**Service**</span><span class="sxs-lookup"><span data-stu-id="61549-319">**Service**</span></span>|<span data-ttu-id="61549-320">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="61549-320">**Protocol**</span></span>|<span data-ttu-id="61549-321">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="61549-321">**Name**</span></span>|<span data-ttu-id="61549-322">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="61549-322">**Host**</span></span>|<span data-ttu-id="61549-323">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="61549-323">**Priority**</span></span>|<span data-ttu-id="61549-324">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="61549-324">**Weight**</span></span>|<span data-ttu-id="61549-325">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="61549-325">**Port**</span></span>|<span data-ttu-id="61549-326">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="61549-326">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="61549-327">SRV</span><span class="sxs-lookup"><span data-stu-id="61549-327">SRV</span></span>  <br/> |<span data-ttu-id="61549-328">sip</span><span class="sxs-lookup"><span data-stu-id="61549-328">sip</span></span>  <br/> |<span data-ttu-id="61549-329">tls</span><span class="sxs-lookup"><span data-stu-id="61549-329">tls</span></span>  <br/> |<span data-ttu-id="61549-330">(Laissez ce champ vide.)</span><span class="sxs-lookup"><span data-stu-id="61549-330">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="61549-331">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="61549-331">sipdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="61549-332">100</span><span class="sxs-lookup"><span data-stu-id="61549-332">100</span></span>  <br/> |<span data-ttu-id="61549-333">1</span><span class="sxs-lookup"><span data-stu-id="61549-333">1</span></span>  <br/> |<span data-ttu-id="61549-334">443</span><span class="sxs-lookup"><span data-stu-id="61549-334">443</span></span>  <br/> |<span data-ttu-id="61549-335">3600 (1 h)</span><span class="sxs-lookup"><span data-stu-id="61549-335">3600 (1 h)</span></span>  <br/> |
    |<span data-ttu-id="61549-336">SRV</span><span class="sxs-lookup"><span data-stu-id="61549-336">SRV</span></span>  <br/> |<span data-ttu-id="61549-337">sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="61549-337">sipfederationtls</span></span>  <br/> |<span data-ttu-id="61549-338">tcp</span><span class="sxs-lookup"><span data-stu-id="61549-338">tcp</span></span>  <br/> |<span data-ttu-id="61549-339">(Laissez ce champ vide.)</span><span class="sxs-lookup"><span data-stu-id="61549-339">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="61549-340">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="61549-340">sipfed.online.lync.com</span></span>  <br/> |<span data-ttu-id="61549-341">100</span><span class="sxs-lookup"><span data-stu-id="61549-341">100</span></span>  <br/> |<span data-ttu-id="61549-342">1</span><span class="sxs-lookup"><span data-stu-id="61549-342">1</span></span>  <br/> |<span data-ttu-id="61549-343">5061</span><span class="sxs-lookup"><span data-stu-id="61549-343">5061</span></span>  <br/> |<span data-ttu-id="61549-344">3600 (1 h)</span><span class="sxs-lookup"><span data-stu-id="61549-344">3600 (1 h)</span></span>  <br/> |  
    
    ![1 &amp; 1-BP-Configure-5-1](../../media/087e337d-926b-42ff-b11d-b449cfaed76c.png)
  
7. <span data-ttu-id="61549-346">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="61549-346">Select **Save**.</span></span> <br/><span data-ttu-id="61549-347">![1 &amp; 1-BP-Configure-5-2](../../media/aa5f803d-fb24-48e0-976a-6759c5fd252c.png)</span><span class="sxs-lookup"><span data-stu-id="61549-347">![1&amp;1-BP-Configure-5-2](../../media/aa5f803d-fb24-48e0-976a-6759c5fd252c.png)</span></span>
  
8. <span data-ttu-id="61549-348">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="61549-348">Select **Save**.</span></span> <br/><span data-ttu-id="61549-349">![1 &amp; 1-BP-Configure-5-3](../../media/097e7e95-4899-4878-b6e7-c3abd8193c52.png)</span><span class="sxs-lookup"><span data-stu-id="61549-349">![1&amp;1-BP-Configure-5-3](../../media/097e7e95-4899-4878-b6e7-c3abd8193c52.png)</span></span>
  
9. <span data-ttu-id="61549-350">Dans la **boîte de dialogue Modifier les paramètres DNS,** sélectionnez **Oui.**</span><span class="sxs-lookup"><span data-stu-id="61549-350">In the **Edit DNS Settings** dialog box, select **Yes**.</span></span> <br/><span data-ttu-id="61549-351">![Sélection de Oui dans la boîte de dialogue Modifier les paramètres DNS](../../media/920cc95f-fedf-4da2-94a4-9cb41ed49bcf.png)</span><span class="sxs-lookup"><span data-stu-id="61549-351">![Selecting Yes in the Edit DNS Settings dialog box](../../media/920cc95f-fedf-4da2-94a4-9cb41ed49bcf.png)</span></span>
  
10. <span data-ttu-id="61549-352">Ajoutez l’autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="61549-352">Add the other SRV record.</span></span> <br/><span data-ttu-id="61549-353">Dans la section **TXT et enregistrements SRV,** sélectionnez **Ajouter un enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="61549-353">In the **TXT and SRV Records** section, select **Add Record**.</span></span> <br/><span data-ttu-id="61549-354">Dans la zone **Ajouter** un enregistrement, créez un enregistrement à l’aide des valeurs de l’autre ligne du tableau, puis sélectionnez de nouveau **Ajouter,** Enregistrer et **Oui** pour terminer l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="61549-354">In the **Add Record** area, create a record using the values from the other row in the table, and then again select **Add**, **Save**, and **Yes** to complete the record.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="61549-355">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="61549-355">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="61549-356">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="61549-356">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="61549-357">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="61549-357">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
