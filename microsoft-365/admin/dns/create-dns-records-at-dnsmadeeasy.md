---
title: Créer des enregistrements DNS chez DNSMadeEasy pour Microsoft
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
ms.assetid: e158b079-b054-4b7e-8e01-e55169ce18d7
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype Entreprise Online et d’autres services sur DNSMadeEasy pour Microsoft.
ms.openlocfilehash: 719b416564447b3a6f4108b747ae921b4f6f6bb8
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49657947"
---
# <a name="create-dns-records-at-dnsmadeeasy-for-microsoft"></a><span data-ttu-id="ea016-103">Créer des enregistrements DNS chez DNSMadeEasy pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="ea016-103">Create DNS records at DNSMadeEasy for Microsoft</span></span>

 <span data-ttu-id="ea016-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="ea016-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="ea016-105">Si DNSMadeEasy est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="ea016-105">If DNSMadeEasy is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="ea016-106">Une fois ces enregistrements ajoutés sur DNSMadeEasy, votre domaine est installé pour fonctionner avec les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ea016-106">After you add these records at DNSMadeEasy, your domain will be set up to work with Microsoft services.</span></span>
  

  
> [!NOTE]
> <span data-ttu-id="ea016-107">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="ea016-107">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="ea016-108">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="ea016-108">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="ea016-109">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ea016-109">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="ea016-110">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="ea016-110">Add a TXT record for verification</span></span>
<span data-ttu-id="ea016-111"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="ea016-111"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="ea016-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="ea016-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ea016-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="ea016-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="ea016-116">Pour les comptes DNSMadeEasy, le domaine que vous avez ajouté a été acheté auprès d'un bureau d'enregistrement de domaines distinct.</span><span class="sxs-lookup"><span data-stu-id="ea016-116">For DNSMadeEasy accounts, the domain you added was purchased from a separate domain registrar.</span></span> <span data-ttu-id="ea016-117">DNSMadeEasy ne propose pas de services d'enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="ea016-117">DNSMadeEasy does not offer domain registration services.</span></span> <span data-ttu-id="ea016-118">Votre connexion au site DNSMadeEasy et la création de l'enregistrement DNS constituent une preuve de propriété suffisante.</span><span class="sxs-lookup"><span data-stu-id="ea016-118">Your ability to log in at DNSMadeEasy and create the DNS record is sufficient proof of ownership.</span></span> 
  
1. <span data-ttu-id="ea016-119">Pour commencer, accédez à la page de vos domaines sur le site DNSMadeEasy en utilisant [ce lien](https://cp.dnsmadeeasy.com/).</span><span class="sxs-lookup"><span data-stu-id="ea016-119">To get started, go to your domains page at DNSMadeEasy by using [this link](https://cp.dnsmadeeasy.com/).</span></span> <span data-ttu-id="ea016-120">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ea016-120">You'll be prompted to login first.</span></span>
    
2. <span data-ttu-id="ea016-121">Dans la page Console  **de** gestion, dans la zone Domaines récemment mis à jour, sélectionnez le domaine à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="ea016-121">On the **Management Console** page, in the **Recently Updated Domains** area, select the domain that you want to update.</span></span> 
    
3. <span data-ttu-id="ea016-122">Dans la page **DNS géré,** dans la zone **Enregistrements TXT,** sélectionnez le contrôle **+** ( ) ( Ajouter **nouveau**).</span><span class="sxs-lookup"><span data-stu-id="ea016-122">On the **Managed DNS** page, in the **TXT Records** area, select the ( **+**) control ( **Add new**).</span></span>
    
    <span data-ttu-id="ea016-123">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="ea016-123">(You may have to scroll down.)</span></span>
    
4. <span data-ttu-id="ea016-124">In the **Add TXT Records** area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="ea016-124">In the **Add TXT Records** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    ||||
    |:-----|:-----|:-----|
    |<span data-ttu-id="ea016-125">**Name**</span><span class="sxs-lookup"><span data-stu-id="ea016-125">**Name**</span></span> <br/> |<span data-ttu-id="ea016-126">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="ea016-126">**Value**</span></span> <br/> |<span data-ttu-id="ea016-127">**TTL**</span><span class="sxs-lookup"><span data-stu-id="ea016-127">**TTL**</span></span> <br/> |
    |<span data-ttu-id="ea016-128">(Laissez ce champ vide.)</span><span class="sxs-lookup"><span data-stu-id="ea016-128">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="ea016-129">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="ea016-129">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="ea016-130">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="ea016-130">**Note:** This is an example.</span></span> <span data-ttu-id="ea016-131">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="ea016-131">Use your specific **Destination or Points to Address** value here, from the table.</span></span> [<span data-ttu-id="ea016-132">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="ea016-132">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="ea016-133">1800</span><span class="sxs-lookup"><span data-stu-id="ea016-133">1800</span></span>  <br/> |
   
5. <span data-ttu-id="ea016-134">Sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="ea016-134">Select **Submit**.</span></span>
    
6. <span data-ttu-id="ea016-135">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="ea016-135">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="ea016-136">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ea016-136">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="ea016-137">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="ea016-137">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="ea016-138">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="ea016-138">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="ea016-139">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="ea016-139">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="ea016-140">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="ea016-140">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="ea016-141">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="ea016-141">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="ea016-142">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="ea016-142">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="ea016-143">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="ea016-143">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="ea016-144">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ea016-144">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="ea016-145">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="ea016-145">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="ea016-146"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="ea016-146"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="ea016-p108">Pour commencer, accédez à la page de vos domaines sur le site DNSMadeEasy en utilisant [ce lien](https://cp.dnsmadeeasy.com/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ea016-p108">To get started, go to your domains page at DNSMadeEasy by using [this link](https://cp.dnsmadeeasy.com/). You'll be prompted to login first.</span></span>
    
2. <span data-ttu-id="ea016-149">Dans la page Console  **de** gestion, dans la zone Domaines récemment mis à jour, sélectionnez le domaine à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="ea016-149">On the **Management Console** page, in the **Recently Updated Domains** area, select the domain that you want to update.</span></span> 
    
    <span data-ttu-id="ea016-150">Dans la page Console  **de** gestion, dans la zone Domaines récemment mis à jour, sélectionnez le domaine à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="ea016-150">On the **Management Console** page, in the **Recently Updated Domains** area, select the domain that you want to update.</span></span> 
    
    ![DNSMadeEasy-BP-Configure-1-2](../../media/8d8f403e-d7cd-429e-913b-dacb1f4644a2.png)
  
3. <span data-ttu-id="ea016-152">Dans la page **DNS géré,** dans la zone **Enregistrements MX,** sélectionnez **le contrôle (+)** ( **Ajouter nouveau**).</span><span class="sxs-lookup"><span data-stu-id="ea016-152">On the **Managed DNS** page, in the **MX Records** area, select the **(+)** control ( **Add new**).</span></span>
    
    <span data-ttu-id="ea016-153">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="ea016-153">(You may have to scroll down.)</span></span>
    
    ![DNSMadeEasy-BP-Configure-2-1](../../media/404c73bf-1db4-4d68-82d8-68303f418ed4.png)
  
4. <span data-ttu-id="ea016-155">Dans la zone **Add MX Records (Ajouter des enregistrements MX)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ea016-155">In the **Add MX Records** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="ea016-156">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="ea016-156">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="ea016-157">**Name**</span><span class="sxs-lookup"><span data-stu-id="ea016-157">**Name**</span></span>|<span data-ttu-id="ea016-158">**Server**</span><span class="sxs-lookup"><span data-stu-id="ea016-158">**Server**</span></span>|<span data-ttu-id="ea016-159">**MX Level (Niveau MX)**</span><span class="sxs-lookup"><span data-stu-id="ea016-159">**MX Level**</span></span>|<span data-ttu-id="ea016-160">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="ea016-160">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="ea016-161">(Laissez ce champ vide.)</span><span class="sxs-lookup"><span data-stu-id="ea016-161">(Leave this field empty.)</span></span>  <br/> | <span data-ttu-id="ea016-162">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="ea016-162">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="ea016-163">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="ea016-163">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="ea016-164">**Remarque :** Obtenez votre \<*domain-key*\> depuis votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ea016-164">**Note:** Get your \<*domain-key*\> from your Microsoft account.</span></span> [<span data-ttu-id="ea016-165">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="ea016-165">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="ea016-166">10 </span><span class="sxs-lookup"><span data-stu-id="ea016-166">10</span></span>  <br/> <span data-ttu-id="ea016-167">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span><span class="sxs-lookup"><span data-stu-id="ea016-167">For more information about priority, see [What is MX priority?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span></span> <br/> |<span data-ttu-id="ea016-168">1800</span><span class="sxs-lookup"><span data-stu-id="ea016-168">1800</span></span>  <br/> |
   
    ![DNSMadeEasy-BP-Configure-2-2](../../media/69b53af9-1eec-435c-8434-1b6058c1ec82.png)
  
5. <span data-ttu-id="ea016-170">Sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="ea016-170">Select **Submit**.</span></span>
    
    ![DNSMadeEasy-BP-Configure-2-3](../../media/381054a6-bb85-4ebb-b576-42cbba78ed1b.png)
  
6. <span data-ttu-id="ea016-172">Si d'autres enregistrements MX sont répertoriés dans la section **MX Records (Enregistrements MX)**, supprimez-les tous en les sélectionnant individuellement.</span><span class="sxs-lookup"><span data-stu-id="ea016-172">If there are any other MX records listed in the **MX Records** section, delete all of them by selecting each one.</span></span> 
    
    ![DNSMadeEasy-BP-Configure-2-4-1](../../media/58a07769-0b30-4111-b555-bfc3b82a7d4c.png)
  
7. <span data-ttu-id="ea016-174">Lorsque tous les enregistrements sont sélectionnés, **sélectionnez Supprimer sélectionné.**</span><span class="sxs-lookup"><span data-stu-id="ea016-174">When all records are selected, select **Delete selected**.</span></span>
    
    ![DNSMadeEasy-BP-Configure-2-4-2](../../media/e9064c07-1ce7-4387-b47a-90d4193da374.png)
  
8. <span data-ttu-id="ea016-176">Dans la **boîte de dialogue Supprimer les enregistrements MX,** **sélectionnez Supprimer** pour confirmer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="ea016-176">In the **Delete MX Records** dialog box, select **Delete** to confirm your changes.</span></span> 
    
    ![DNSMadeEasy-BP-Configure-2-5](../../media/03c405e5-868f-468f-b6d2-046d27b201fb.png)
  
## <a name="add-the-five-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="ea016-178">Ajouter les cinq enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="ea016-178">Add the five CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="ea016-179"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="ea016-179"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="ea016-p110">Pour commencer, accédez à la page de vos domaines sur le site DNSMadeEasy en utilisant [ce lien](https://cp.dnsmadeeasy.com/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ea016-p110">To get started, go to your domains page at DNSMadeEasy by using [this link](https://cp.dnsmadeeasy.com/). You'll be prompted to login first.</span></span>
    
2. <span data-ttu-id="ea016-182">Dans la page Console  **de** gestion, dans la zone Domaines récemment mis à jour, sélectionnez le domaine à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="ea016-182">On the **Management Console** page, in the **Recently Updated Domains** area, select the domain that you want to update.</span></span> 
    
3. <span data-ttu-id="ea016-183">Dans la page **DNS géré,** dans la zone Enregistrements **CNAME,** sélectionnez **le contrôle (+)** ( **Ajouter nouveau**).</span><span class="sxs-lookup"><span data-stu-id="ea016-183">On the **Managed DNS** page, in the **CNAME Records** area, select the **(+)** control ( **Add new**).</span></span>
    
    <span data-ttu-id="ea016-184">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="ea016-184">(You may have to scroll down.)</span></span>
    
    ![DNSMadeEasy-BP-Configure-3-1](../../media/a5feb238-690d-4b64-a625-91a82b3f4068.png)
  
4. <span data-ttu-id="ea016-186">Ajoutez le premier des cinq enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="ea016-186">Add the first of the five CNAME records.</span></span>
    
    <span data-ttu-id="ea016-187">Dans la zone **Add CNAME Records (Ajouter des enregistrements CNAME)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ea016-187">In the **Add CNAME Records** area, in the boxes for the new record, type or copy and paste the values from the first row in the following table.</span></span> 
    
    |<span data-ttu-id="ea016-188">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="ea016-188">**Name**</span></span>|<span data-ttu-id="ea016-189">**Alias to (Alias vers)**</span><span class="sxs-lookup"><span data-stu-id="ea016-189">**Alias to**</span></span>|<span data-ttu-id="ea016-190">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="ea016-190">**TTL**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="ea016-191">autodiscover</span><span class="sxs-lookup"><span data-stu-id="ea016-191">autodiscover</span></span>  <br/> |<span data-ttu-id="ea016-192">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="ea016-192">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="ea016-193">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="ea016-193">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="ea016-194">1800</span><span class="sxs-lookup"><span data-stu-id="ea016-194">1800</span></span>  <br/> |
    |<span data-ttu-id="ea016-195">sip</span><span class="sxs-lookup"><span data-stu-id="ea016-195">sip</span></span>  <br/> |<span data-ttu-id="ea016-196">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="ea016-196">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="ea016-197">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="ea016-197">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="ea016-198">1800</span><span class="sxs-lookup"><span data-stu-id="ea016-198">1800</span></span>  <br/> |
    |<span data-ttu-id="ea016-199">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="ea016-199">lyncdiscover</span></span>  <br/> |<span data-ttu-id="ea016-200">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="ea016-200">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="ea016-201">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="ea016-201">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="ea016-202">1800</span><span class="sxs-lookup"><span data-stu-id="ea016-202">1800</span></span>  <br/> |
    |<span data-ttu-id="ea016-203">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="ea016-203">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="ea016-204">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="ea016-204">enterpriseregistration.windows.net.</span></span>  <br/> <span data-ttu-id="ea016-205">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="ea016-205">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="ea016-206">1800</span><span class="sxs-lookup"><span data-stu-id="ea016-206">1800</span></span>  <br/> |
    |<span data-ttu-id="ea016-207">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="ea016-207">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="ea016-208">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="ea016-208">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> <span data-ttu-id="ea016-209">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="ea016-209">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="ea016-210">1800</span><span class="sxs-lookup"><span data-stu-id="ea016-210">1800</span></span>  <br/> |
   
    ![DNSMadeEasy-BP-Configure-3-2](../../media/de6dddcd-bf0a-4993-ab4c-a6d10167bf34.png)
  
5. <span data-ttu-id="ea016-212">Sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="ea016-212">Select **Submit**.</span></span>
    
    ![DNSMadeEasy-BP-Configure-3-3](../../media/e44ef73e-99cb-41ce-a3f2-549cb2f29eef.png)
  
6. <span data-ttu-id="ea016-214">Ajoutez chacun des quatre autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="ea016-214">Add each of the other four CNAME records.</span></span>
    
    <span data-ttu-id="ea016-215">Dans la section Enregistrements  **CNAME,** sélectionnez le contrôle **(+)** ( Ajouter nouveau ), créez un enregistrement en utilisant les valeurs de la ligne suivante du tableau, puis sélectionnez de nouveau Envoyer pour terminer cet enregistrement. </span><span class="sxs-lookup"><span data-stu-id="ea016-215">In the **CNAME Records** section, select the **(+)** control ( **Add new**), create a record by using the values from the next row in the table, and then again select **Submit** to complete that record.</span></span> 
    
    <span data-ttu-id="ea016-216">Répétez ce processus jusqu’à ce que vous avez créé les cinq enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="ea016-216">Repeat this process until you have created all five CNAME records.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="ea016-217">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="ea016-217">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="ea016-218"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="ea016-218"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea016-219">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="ea016-219">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="ea016-220">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="ea016-220">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="ea016-221">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ea016-221">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="ea016-222">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de n’avoir qu’un seul  *enregistrement*  SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="ea016-222">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> <span data-ttu-id="ea016-223">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="ea016-223">Need examples?</span></span> <span data-ttu-id="ea016-224">Consultez ces [Enregistrements DNS externes pour Microsoft](https://docs.microsoft.com/microsoft-365/enterprise/external-domain-name-system-records).</span><span class="sxs-lookup"><span data-stu-id="ea016-224">Check out these [External Domain Name System records for Microsoft](https://docs.microsoft.com/microsoft-365/enterprise/external-domain-name-system-records).</span></span> <span data-ttu-id="ea016-225">Pour valider votre enregistrement SPF, vous pouvez utiliser l’un de ces outils[de validation SPF.](../setup/domains-faq.yml)</span><span class="sxs-lookup"><span data-stu-id="ea016-225">To validate your SPF record, you can use one of these[SPF validation tools](../setup/domains-faq.yml).</span></span> 
  
1. <span data-ttu-id="ea016-226">Pour commencer, accédez à la page de vos domaines sur le site DNSMadeEasy en utilisant [ce lien](https://cp.dnsmadeeasy.com/).</span><span class="sxs-lookup"><span data-stu-id="ea016-226">To get started, go to your domains page at DNSMadeEasy by using [this link](https://cp.dnsmadeeasy.com/).</span></span> <span data-ttu-id="ea016-227">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ea016-227">You'll be prompted to login first.</span></span>
    
2. <span data-ttu-id="ea016-228">Dans la page Console  **de** gestion, dans la zone Domaines récemment mis à jour, sélectionnez le domaine à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="ea016-228">On the **Management Console** page, in the **Recently Updated Domains** area, select the domain that you want to update.</span></span> 
    
3. <span data-ttu-id="ea016-229">Dans la page **DNS géré,** dans la zone **Enregistrements TXT,** sélectionnez **le contrôle (+)** ( **Ajouter nouveau**).</span><span class="sxs-lookup"><span data-stu-id="ea016-229">On the **Managed DNS** page, in the **TXT Records** area, select the **(+)** control ( **Add new**).</span></span>
    
    <span data-ttu-id="ea016-230">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="ea016-230">(You may have to scroll down.)</span></span>
    
    ![DNSMadeEasy-BP-Configure-4-1](../../media/657b87a5-dcb4-4ae7-8f27-bd857f0f4189.png)
  
4. <span data-ttu-id="ea016-232">In the **Add TXT Records** area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="ea016-232">In the **Add TXT Records** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    |<span data-ttu-id="ea016-233">**Name**</span><span class="sxs-lookup"><span data-stu-id="ea016-233">**Name**</span></span>|<span data-ttu-id="ea016-234">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="ea016-234">**Value**</span></span>|<span data-ttu-id="ea016-235">**TTL**</span><span class="sxs-lookup"><span data-stu-id="ea016-235">**TTL**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="ea016-236">(Laissez ce champ vide.)</span><span class="sxs-lookup"><span data-stu-id="ea016-236">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="ea016-237">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="ea016-237">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="ea016-238">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="ea016-238">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |<span data-ttu-id="ea016-239">1800</span><span class="sxs-lookup"><span data-stu-id="ea016-239">1800</span></span>  <br/> |
   
    ![DNSMadeEasy-BP-Configure-4-2](../../media/b317bcb9-18c6-4609-a8f4-963823032669.png)
  
5. <span data-ttu-id="ea016-241">Sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="ea016-241">Select **Submit**.</span></span>
    
    ![DNSMadeEasy-BP-Configure-4-3](../../media/8a1c53c3-1222-4127-a190-70f6f5059433.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="ea016-243">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="ea016-243">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="ea016-244"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="ea016-244"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="ea016-p113">Pour commencer, accédez à la page de vos domaines sur le site DNSMadeEasy en utilisant [ce lien](https://cp.dnsmadeeasy.com/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ea016-p113">To get started, go to your domains page at DNSMadeEasy by using [this link](https://cp.dnsmadeeasy.com/). You'll be prompted to login first.</span></span>
    
2. <span data-ttu-id="ea016-247">Dans la page Console  **de** gestion, dans la zone Domaines récemment mis à jour, sélectionnez le domaine à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="ea016-247">On the **Management Console** page, in the **Recently Updated Domains** area, select the domain that you want to update.</span></span> 
    
3. <span data-ttu-id="ea016-248">Dans la page **DNS géré,** dans la zone **Enregistrements SRV,** sélectionnez **le contrôle (+)** ( **Ajouter nouveau**).</span><span class="sxs-lookup"><span data-stu-id="ea016-248">On the **Managed DNS** page, in the **SRV Records** area, select the **(+)** control ( **Add new**).</span></span>
    
    <span data-ttu-id="ea016-249">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="ea016-249">(You may have to scroll down)</span></span>
    
    ![DNSMadeEasy-BP-Configure-5-1](../../media/5c9e8f50-adbd-4f23-8ce3-2844b2896f3f.png)
  
4. <span data-ttu-id="ea016-251">Ajoutez le premier des deux enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="ea016-251">Add the first of the two SRV records.</span></span>
    
    <span data-ttu-id="ea016-252">Dans la zone **Add SRV Records (Ajouter des enregistrements SRV)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ea016-252">In the **Add SRV Records** area, in the boxes for the new record, type or copy and paste the values from the first row in the following table.</span></span> 
    
    |<span data-ttu-id="ea016-253">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="ea016-253">**Name**</span></span>|<span data-ttu-id="ea016-254">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="ea016-254">**Priority**</span></span>|<span data-ttu-id="ea016-255">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="ea016-255">**Weight**</span></span>|<span data-ttu-id="ea016-256">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="ea016-256">**Port**</span></span>|<span data-ttu-id="ea016-257">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="ea016-257">**Host**</span></span>|<span data-ttu-id="ea016-258">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="ea016-258">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="ea016-259">_sip._tls</span><span class="sxs-lookup"><span data-stu-id="ea016-259">_sip._tls</span></span>  <br/> |<span data-ttu-id="ea016-260">100</span><span class="sxs-lookup"><span data-stu-id="ea016-260">100</span></span>  <br/> |<span data-ttu-id="ea016-261">1 </span><span class="sxs-lookup"><span data-stu-id="ea016-261">1</span></span>  <br/> |<span data-ttu-id="ea016-262">443</span><span class="sxs-lookup"><span data-stu-id="ea016-262">443</span></span>  <br/> |<span data-ttu-id="ea016-263">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="ea016-263">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="ea016-264">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="ea016-264">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="ea016-265">1800</span><span class="sxs-lookup"><span data-stu-id="ea016-265">1800</span></span>  <br/> |
    |<span data-ttu-id="ea016-266">_sipfederationtls._tcp</span><span class="sxs-lookup"><span data-stu-id="ea016-266">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="ea016-267">100</span><span class="sxs-lookup"><span data-stu-id="ea016-267">100</span></span>  <br/> |<span data-ttu-id="ea016-268">1 </span><span class="sxs-lookup"><span data-stu-id="ea016-268">1</span></span>  <br/> |<span data-ttu-id="ea016-269">5061</span><span class="sxs-lookup"><span data-stu-id="ea016-269">5061</span></span>  <br/> |<span data-ttu-id="ea016-270">sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="ea016-270">sipfed.online.lync.com.</span></span>  <br/> <span data-ttu-id="ea016-271">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="ea016-271">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="ea016-272">1800</span><span class="sxs-lookup"><span data-stu-id="ea016-272">1800</span></span>  <br/> |
   
    ![DNSMadeEasy-BP-Configure-5-2](../../media/e1155f94-575f-441a-9a61-d948391d42ca.png)
  
5. <span data-ttu-id="ea016-274">Sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="ea016-274">Select **Submit**.</span></span>
    
    ![DNSMadeEasy-BP-Configure-5-3](../../media/7eae54e1-08bd-4902-afdf-fd5cc251ab59.png)
  
6. <span data-ttu-id="ea016-276">Ajoutez l'autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="ea016-276">Add the other SRV record.</span></span>
    
    <span data-ttu-id="ea016-277">Dans la section Enregistrements  **SRV,** sélectionnez le contrôle **(+)** ( Ajouter nouveau ), créez un enregistrement en utilisant les valeurs de la ligne suivante du tableau, puis sélectionnez de nouveau Envoyer pour terminer cet enregistrement. </span><span class="sxs-lookup"><span data-stu-id="ea016-277">In the **SRV Records** section, select the **(+)** control ( **Add new**), create a record by using the values from the next row in the table, and then again select **Submit** to complete that record.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="ea016-278">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="ea016-278">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="ea016-279">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="ea016-279">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="ea016-280">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ea016-280">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  

