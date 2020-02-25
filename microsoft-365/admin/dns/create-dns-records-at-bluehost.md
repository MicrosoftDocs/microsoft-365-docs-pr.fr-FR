---
title: Créer des enregistrements DNS sur Bluehost pour Office 365
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
ms.assetid: 657934ff-d9d2-4563-9ccf-ef4832a03a99
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur Bluehost pour Office 365.
ms.openlocfilehash: 9a5cad6778cb66958539a324befee43ddb2dd8b9
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42243456"
---
# <a name="create-dns-records-at-bluehost-for-office-365"></a><span data-ttu-id="8daef-103">Créer des enregistrements DNS sur Bluehost pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8daef-103">Create DNS records at Bluehost for Office 365</span></span>

 <span data-ttu-id="8daef-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="8daef-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="8daef-105">Si Bluehost est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="8daef-105">If Bluehost is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="8daef-106">Une fois ces enregistrements ajoutés sur Bluehost, votre domaine est configuré pour utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="8daef-106">After you add these records at Bluehost, your domain will be set up to work with Office 365 services.</span></span>
  
<span data-ttu-id="8daef-107">Pour en savoir plus sur l'hébergement web et le DNS pour les sites web avec Office 365, voir [Utiliser un site web public avec Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span><span class="sxs-lookup"><span data-stu-id="8daef-107">To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span></span>
  
> [!NOTE]
> <span data-ttu-id="8daef-108">Typically it takes about 15 minutes for DNS changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="8daef-108">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="8daef-109">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="8daef-109">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="8daef-110">Si vous rencontrez des problèmes avec le flux de messagerie ou d’autres problèmes après avoir ajouté des enregistrements DNS, consultez [la rubrique Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="8daef-110">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="8daef-111">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="8daef-111">Add a TXT record for verification</span></span>
<span data-ttu-id="8daef-112"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="8daef-112"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="8daef-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="8daef-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8daef-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="8daef-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="8daef-117">Pour commencer, accédez à la page de vos domaines sur le site Bluehost en utilisant [ce lien](https://my.bluehost.com/cgi/dm).</span><span class="sxs-lookup"><span data-stu-id="8daef-117">To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm).</span></span> <span data-ttu-id="8daef-118">You'll be prompted to log in first.</span><span class="sxs-lookup"><span data-stu-id="8daef-118">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="8daef-119">Dans la page **domains (domaines)**, dans la zone **domain (domaine)**, recherchez la ligne associée au domaine que vous modifiez, puis cochez la case correspondant à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="8daef-119">On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain.</span></span> 
    
    <span data-ttu-id="8daef-120">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8daef-120">(You may have to scroll down.)</span></span>
    
3. <span data-ttu-id="8daef-121">Dans la zone ***domain_name*** , sur la ligne **éditeur de zone DNS** , sélectionnez **gérer les enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="8daef-121">In the ***domain_name*** area, on the **DNS Zone Editor** row, select **Manage DNS records**.</span></span>
    
4. <span data-ttu-id="8daef-122">Dans la page \* \* éditeur de zone DNS \* \*, dans la zone **Ajouter un enregistrement DNS** , dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8daef-122">On the \*\* DNS Zone Editor \*\* page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="8daef-123">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="8daef-123">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |||||
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="8daef-124">**Host Record**</span><span class="sxs-lookup"><span data-stu-id="8daef-124">**Host Record**</span></span> <br/> |<span data-ttu-id="8daef-125">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="8daef-125">**TTL**</span></span> <br/> |<span data-ttu-id="8daef-126">**Type**</span><span class="sxs-lookup"><span data-stu-id="8daef-126">**Type**</span></span> <br/> |<span data-ttu-id="8daef-127">**TXT Value**</span><span class="sxs-lookup"><span data-stu-id="8daef-127">**TXT Value**</span></span> <br/> |
    |@  <br/> |<span data-ttu-id="8daef-128">14400</span><span class="sxs-lookup"><span data-stu-id="8daef-128">14400</span></span>  <br/> |<span data-ttu-id="8daef-129">TXT</span><span class="sxs-lookup"><span data-stu-id="8daef-129">TXT</span></span>  <br/> |<span data-ttu-id="8daef-130">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="8daef-130">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="8daef-131">**Remarque :** Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="8daef-131">**Note:** This is an example.</span></span> <span data-ttu-id="8daef-132">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="8daef-132">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span> [<span data-ttu-id="8daef-133">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="8daef-133">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
5. <span data-ttu-id="8daef-134">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="8daef-134">Select **add record**.</span></span>
    
6. <span data-ttu-id="8daef-135">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="8daef-135">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="8daef-136">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span><span class="sxs-lookup"><span data-stu-id="8daef-136">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="8daef-137">When Office 365 finds the correct TXT record, your domain is verified.</span><span class="sxs-lookup"><span data-stu-id="8daef-137">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="8daef-138">Dans le centre d’administration, accédez à la page **paramètres** \> des <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="8daef-138">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="8daef-139">Dans la page **domaines** , sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="8daef-139">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="8daef-140">Sur la page **installation** , sélectionnez **Démarrer l’installation**.</span><span class="sxs-lookup"><span data-stu-id="8daef-140">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="8daef-141">Sur la page **vérifier le domaine** , sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="8daef-141">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="8daef-142">Typically it takes about 15 minutes for DNS changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="8daef-142">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="8daef-143">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="8daef-143">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="8daef-144">Si vous rencontrez des problèmes avec le flux de messagerie ou d’autres problèmes après avoir ajouté des enregistrements DNS, consultez [la rubrique Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="8daef-144">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="8daef-145">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="8daef-145">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="8daef-146"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="8daef-146"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="8daef-147">Pour commencer, accédez à la page de vos domaines sur le site Bluehost en utilisant [ce lien](https://my.bluehost.com/cgi/dm).</span><span class="sxs-lookup"><span data-stu-id="8daef-147">To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm).</span></span> <span data-ttu-id="8daef-148">You'll be prompted to log in first.</span><span class="sxs-lookup"><span data-stu-id="8daef-148">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="8daef-149">Dans la page **domains (domaines)**, dans la zone **domain (domaine)**, recherchez la ligne associée au domaine que vous modifiez, puis cochez la case correspondant à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="8daef-149">On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain.</span></span> 
    
    <span data-ttu-id="8daef-150">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8daef-150">(You may have to scroll down.)</span></span>
    
3. <span data-ttu-id="8daef-151">Dans la zone ***domain_name*** , sur la ligne **éditeur de zone DNS** , sélectionnez **gérer les enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="8daef-151">In the ***domain_name*** area, on the **DNS Zone Editor** row, select **Manage DNS records**.</span></span>
    
4. <span data-ttu-id="8daef-152">On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="8daef-152">On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="8daef-153">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="8daef-153">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="8daef-154">**Host Record**</span><span class="sxs-lookup"><span data-stu-id="8daef-154">**Host Record**</span></span>|<span data-ttu-id="8daef-155">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="8daef-155">**TTL**</span></span>|<span data-ttu-id="8daef-156">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="8daef-156">**Type**</span></span>|<span data-ttu-id="8daef-157">**Points to (Destination)**</span><span class="sxs-lookup"><span data-stu-id="8daef-157">**Points To**</span></span>|<span data-ttu-id="8daef-158">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="8daef-158">**Priority**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="8daef-159">14400</span><span class="sxs-lookup"><span data-stu-id="8daef-159">14400</span></span>  <br/> |<span data-ttu-id="8daef-160">MX</span><span class="sxs-lookup"><span data-stu-id="8daef-160">MX</span></span>  <br/> | <span data-ttu-id="8daef-161">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="8daef-161">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/><span data-ttu-id="8daef-162">**Remarque :** Obtenez votre \< *clé* \> de domaine à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="8daef-162">**Note:** Get your \<*domain-key*\> from your Office 365 account.</span></span> [<span data-ttu-id="8daef-163">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="8daef-163">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="8daef-164">0</span><span class="sxs-lookup"><span data-stu-id="8daef-164">0</span></span>  <br/> <span data-ttu-id="8daef-165">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="8daef-165">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> |
   
   ![Choisissez type dans la liste déroulante.](../media/70791420-d83c-4a5d-a46c-5cc3bc67f565.png)
  
5. <span data-ttu-id="8daef-167">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="8daef-167">Select **add record**.</span></span>
    
    ![Sélectionnez Ajouter un enregistrement](../media/c7ef9733-1665-4dbf-accc-caadf1574abc.png)
  
6. <span data-ttu-id="8daef-169">Si d'autres enregistrements MX sont répertoriés dans la section **MX (Mail Exchanger) (MX (Mail Exchanger))**, supprimez-les individuellement.</span><span class="sxs-lookup"><span data-stu-id="8daef-169">If there are any other MX records in the **MX (Mail Exchanger)** section, delete each of them.</span></span> 
    
    <span data-ttu-id="8daef-170">Pour l’un des autres enregistrements MX, sélectionnez **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="8daef-170">For one of the other MX records, select **Delete.**</span></span>
    
    ![Sélectionnez Delete pour chaque enregistrement MX supplémentaire](../media/6be17f54-3f33-47af-a9db-4689141530c2.png)
  
7. <span data-ttu-id="8daef-172">Dans la boîte de dialogue de confirmation, sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="8daef-172">In the confirmation dialog box, select **OK**.</span></span>
    
    ![Sélectionnez OK.](../media/a50df7a3-2906-4cc0-87d4-1231ab234230.png)
  
8. <span data-ttu-id="8daef-174">Utilisez la même procédure pour supprimer tous les enregistrements MX déjà répertoriés.</span><span class="sxs-lookup"><span data-stu-id="8daef-174">Use the same process to delete any other MX records that were already listed.</span></span>
    
## <a name="add-the-six-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="8daef-175">Ajouter les 6 enregistrements CNAME requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8daef-175">Add the six CNAME records that are required for Office 365</span></span>
<span data-ttu-id="8daef-176"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="8daef-176"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="8daef-177">Pour commencer, accédez à la page de vos domaines sur le site Bluehost en utilisant [ce lien](https://my.bluehost.com/cgi/dm).</span><span class="sxs-lookup"><span data-stu-id="8daef-177">To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm).</span></span> <span data-ttu-id="8daef-178">You'll be prompted to log in first.</span><span class="sxs-lookup"><span data-stu-id="8daef-178">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="8daef-179">Dans la page **domains (domaines)**, dans la zone **domain (domaine)**, recherchez la ligne associée au domaine que vous modifiez, puis cochez la case correspondant à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="8daef-179">On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain.</span></span> 
    
    <span data-ttu-id="8daef-180">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8daef-180">(You may have to scroll down.)</span></span>
    
3. <span data-ttu-id="8daef-181">Dans la zone ***domain_name*** , sur la ligne **éditeur de zone DNS** , sélectionnez **gérer les enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="8daef-181">In the ***domain_name*** area, on the **DNS Zone Editor** row, select **Manage DNS records**.</span></span>
    
4. <span data-ttu-id="8daef-182">Dans la section **A (hôte)** , recherchez la ligne de l’enregistrement de **découverte automatique** , puis sélectionnez **supprimer** pour cette ligne.</span><span class="sxs-lookup"><span data-stu-id="8daef-182">In the **A (Host)** records section, find the row for the **autodiscover** record, and then select **delete** for that row.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="8daef-p110">Vous devez supprimer l'enregistrement **autodiscover** existant  *avant*  d'ajouter l'enregistrement **autodiscover** requis par Office 365. Bluehost ne vous permet pas de conserver deux enregistrements **autodiscover** simultanément.</span><span class="sxs-lookup"><span data-stu-id="8daef-p110">You must delete the existing **autodiscover** record  *before*  adding the **autodiscover** record that is required by Office 365. Bluehost does not allow you to maintain two **autodiscover** records simultaneously.</span></span> 
  
    ![Sélectionnez supprimer](../media/416a447e-3710-4ae7-8bf1-459381af4f6e.png)
  
5. <span data-ttu-id="8daef-186">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="8daef-186">Select **OK**.</span></span>
    
    ![Sélectionnez OK.](../media/0c8f409d-c39f-4ed2-9c95-9af3e61c2411.png)
  
6. <span data-ttu-id="8daef-188">Créer le premier des six enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="8daef-188">Create the first of the six CNAME records.</span></span>
    
    <span data-ttu-id="8daef-189">Sur la page **DNS Zone Editor (Éditeur de zone DNS)**, dans la zone **Add DNS Record (Ajouter un enregistrement DNS)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs dans la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8daef-189">On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the first row in the following table.</span></span> 
    
    <span data-ttu-id="8daef-190">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="8daef-190">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="8daef-191">**Host Record**</span><span class="sxs-lookup"><span data-stu-id="8daef-191">**Host Record**</span></span>|<span data-ttu-id="8daef-192">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="8daef-192">**TTL**</span></span>|<span data-ttu-id="8daef-193">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="8daef-193">**Type**</span></span>|<span data-ttu-id="8daef-194">**Points to (Destination)**</span><span class="sxs-lookup"><span data-stu-id="8daef-194">**Points To**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="8daef-195">autodiscover</span><span class="sxs-lookup"><span data-stu-id="8daef-195">autodiscover</span></span>  <br/> |<span data-ttu-id="8daef-196">14400</span><span class="sxs-lookup"><span data-stu-id="8daef-196">14400</span></span>  <br/> |<span data-ttu-id="8daef-197">CNAME</span><span class="sxs-lookup"><span data-stu-id="8daef-197">CNAME</span></span>  <br/> |<span data-ttu-id="8daef-198">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="8daef-198">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="8daef-199">sip</span><span class="sxs-lookup"><span data-stu-id="8daef-199">sip</span></span>  <br/> |<span data-ttu-id="8daef-200">14400</span><span class="sxs-lookup"><span data-stu-id="8daef-200">14400</span></span>  <br/> |<span data-ttu-id="8daef-201">CNAME</span><span class="sxs-lookup"><span data-stu-id="8daef-201">CNAME</span></span>  <br/> |<span data-ttu-id="8daef-202">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="8daef-202">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="8daef-203">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="8daef-203">lyncdiscover</span></span>  <br/> |<span data-ttu-id="8daef-204">14400</span><span class="sxs-lookup"><span data-stu-id="8daef-204">14400</span></span>  <br/> |<span data-ttu-id="8daef-205">CNAME</span><span class="sxs-lookup"><span data-stu-id="8daef-205">CNAME</span></span>  <br/> |<span data-ttu-id="8daef-206">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="8daef-206">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="8daef-207">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="8daef-207">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="8daef-208">14400</span><span class="sxs-lookup"><span data-stu-id="8daef-208">14400</span></span>  <br/> |<span data-ttu-id="8daef-209">CNAME</span><span class="sxs-lookup"><span data-stu-id="8daef-209">CNAME</span></span>  <br/> |<span data-ttu-id="8daef-210">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="8daef-210">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="8daef-211">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="8daef-211">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="8daef-212">14400</span><span class="sxs-lookup"><span data-stu-id="8daef-212">14400</span></span>  <br/> |<span data-ttu-id="8daef-213">CNAME</span><span class="sxs-lookup"><span data-stu-id="8daef-213">CNAME</span></span>  <br/> |<span data-ttu-id="8daef-214">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="8daef-214">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
   
    ![Créer le premier enregistrement CNAMe](../media/4f12e9b1-9dec-4bc2-aa15-8bffa71fe131.png)
  
7. <span data-ttu-id="8daef-216">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="8daef-216">Select **add record**.</span></span>
    
    ![Sélectionnez Ajouter un enregistrement](../media/c2782250-a9a6-4aee-bb15-f57cb0008587.png)
  
8. <span data-ttu-id="8daef-218">Ajoutez successivement les 5 autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="8daef-218">Add each of the other five CNAME records.</span></span>
    
    <span data-ttu-id="8daef-219">Toujours dans la section **Add DNS record (ajouter un enregistrement DNS** ), créez un enregistrement en utilisant les valeurs de la ligne suivante du tableau, puis sélectionnez de nouveau **Add record (Ajouter** un enregistrement) pour valider cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8daef-219">Still in the **Add DNS Record** section, create a record by using the values from the next row in the table, and then again select **add record** to complete that record.</span></span> 
    
    <span data-ttu-id="8daef-220">Répétez cette procédure jusqu'à avoir créé les 6 enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="8daef-220">Repeat this process until you have created all six CNAME records.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="8daef-221">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="8daef-221">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="8daef-222"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="8daef-222"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="8daef-223">You cannot have more than one TXT record for SPF for a domain.</span><span class="sxs-lookup"><span data-stu-id="8daef-223">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="8daef-224">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span><span class="sxs-lookup"><span data-stu-id="8daef-224">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="8daef-225">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="8daef-225">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="8daef-226">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="8daef-226">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> <span data-ttu-id="8daef-227">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="8daef-227">Need examples?</span></span> <span data-ttu-id="8daef-228">Consultez ces [enregistrements DNS externes pour Office 365](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0).</span><span class="sxs-lookup"><span data-stu-id="8daef-228">Check out these [External Domain Name System records for Office 365](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0).</span></span> <span data-ttu-id="8daef-229">Pour valider votre enregistrement SPF, vous pouvez utiliser l’un de ces[outils de validation SPF](../setup/domains-faq.md).</span><span class="sxs-lookup"><span data-stu-id="8daef-229">To validate your SPF record, you can use one of these[SPF validation tools](../setup/domains-faq.md).</span></span> 
  
1. <span data-ttu-id="8daef-230">Pour commencer, accédez à la page de vos domaines sur le site Bluehost en utilisant [ce lien](https://my.bluehost.com/cgi/dm).</span><span class="sxs-lookup"><span data-stu-id="8daef-230">To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm).</span></span> <span data-ttu-id="8daef-231">You'll be prompted to log in first.</span><span class="sxs-lookup"><span data-stu-id="8daef-231">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="8daef-232">Dans la page **domains (domaines)**, dans la zone **domain (domaine)**, recherchez la ligne associée au domaine que vous modifiez, puis cochez la case correspondant à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="8daef-232">On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain.</span></span> 
    
    <span data-ttu-id="8daef-233">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8daef-233">(You may have to scroll down.)</span></span>
    
3. <span data-ttu-id="8daef-234">Dans la zone ***domain_name*** , sur la ligne **éditeur de zone DNS** , sélectionnez **gérer les enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="8daef-234">In the ***domain_name*** area, on the **DNS Zone Editor** row, select **Manage DNS records**.</span></span>
    
4. <span data-ttu-id="8daef-235">On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="8daef-235">On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="8daef-236">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="8daef-236">(Choose the **Type** value from the drop-down list.)</span></span> 
        
    |<span data-ttu-id="8daef-237">**Host Record**</span><span class="sxs-lookup"><span data-stu-id="8daef-237">**Host Record**</span></span>|<span data-ttu-id="8daef-238">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="8daef-238">**TTL**</span></span>|<span data-ttu-id="8daef-239">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="8daef-239">**Type**</span></span>|<span data-ttu-id="8daef-240">**TXT Value**</span><span class="sxs-lookup"><span data-stu-id="8daef-240">**TXT Value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="8daef-241">14400</span><span class="sxs-lookup"><span data-stu-id="8daef-241">14400</span></span>  <br/> |<span data-ttu-id="8daef-242">TXT</span><span class="sxs-lookup"><span data-stu-id="8daef-242">TXT</span></span>  <br/> |<span data-ttu-id="8daef-243">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="8daef-243">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/><span data-ttu-id="8daef-244">**Remarque :** Nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="8daef-244">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Copier la valeur TXT](../media/b2dabd7a-ee3d-4209-aa1e-0233eb8cf3b9.png)
  
5. <span data-ttu-id="8daef-246">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="8daef-246">Select **add record**.</span></span>
    
    ![Sélectionnez Ajouter un enregistrement](../media/c050e9a2-2274-4640-8f0f-6752d382df5d.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="8daef-248">Ajouter les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8daef-248">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="8daef-249"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="8daef-249"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="8daef-250">Pour commencer, accédez à la page de vos domaines sur le site Bluehost en utilisant [ce lien](https://my.bluehost.com/cgi/dm).</span><span class="sxs-lookup"><span data-stu-id="8daef-250">To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm).</span></span> <span data-ttu-id="8daef-251">You'll be prompted to log in first.</span><span class="sxs-lookup"><span data-stu-id="8daef-251">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="8daef-252">Dans la page **domains (domaines)**, dans la zone **domain (domaine)**, recherchez la ligne associée au domaine que vous modifiez, puis cochez la case correspondant à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="8daef-252">On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain.</span></span> 
    
    <span data-ttu-id="8daef-253">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8daef-253">(You may have to scroll down.)</span></span>
    
3. <span data-ttu-id="8daef-254">Dans la zone ***domain_name*** , sur la ligne **éditeur de zone DNS** , sélectionnez **gérer les enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="8daef-254">In the ***domain_name*** area, on the **DNS Zone Editor** row, select **Manage DNS records**.</span></span>
    
4. <span data-ttu-id="8daef-255">Créez le premier des deux enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="8daef-255">Create the first of the two SRV records.</span></span>
    
    <span data-ttu-id="8daef-256">Sur la page **DNS Zone Editor (Éditeur de zone DNS)**, dans la zone **Add DNS Record (Ajouter un enregistrement DNS)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs dans la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8daef-256">On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the first row in the following table.</span></span> 
    
    <span data-ttu-id="8daef-257">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="8daef-257">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="8daef-258">**Service**</span><span class="sxs-lookup"><span data-stu-id="8daef-258">**Service**</span></span>|<span data-ttu-id="8daef-259">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="8daef-259">**Protocol**</span></span>|<span data-ttu-id="8daef-260">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="8daef-260">**Host**</span></span>|<span data-ttu-id="8daef-261">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="8daef-261">**TTL**</span></span>|<span data-ttu-id="8daef-262">**Type**</span><span class="sxs-lookup"><span data-stu-id="8daef-262">**Type**</span></span>|<span data-ttu-id="8daef-263">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="8daef-263">**Priority**</span></span>|<span data-ttu-id="8daef-264">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="8daef-264">**Weight**</span></span>|<span data-ttu-id="8daef-265">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="8daef-265">**Port**</span></span>|<span data-ttu-id="8daef-266">**Points to (Destination)**</span><span class="sxs-lookup"><span data-stu-id="8daef-266">**Points To**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="8daef-267">_sip</span><span class="sxs-lookup"><span data-stu-id="8daef-267">_sip</span></span>  <br/> |<span data-ttu-id="8daef-268">_tls</span><span class="sxs-lookup"><span data-stu-id="8daef-268">_tls</span></span>  <br/> |@  <br/> |<span data-ttu-id="8daef-269">14400</span><span class="sxs-lookup"><span data-stu-id="8daef-269">14400</span></span>  <br/> |<span data-ttu-id="8daef-270">SRV</span><span class="sxs-lookup"><span data-stu-id="8daef-270">SRV</span></span>  <br/> |<span data-ttu-id="8daef-271">100</span><span class="sxs-lookup"><span data-stu-id="8daef-271">100</span></span>  <br/> |<span data-ttu-id="8daef-272">0,1</span><span class="sxs-lookup"><span data-stu-id="8daef-272">1</span></span>  <br/> |<span data-ttu-id="8daef-273">443</span><span class="sxs-lookup"><span data-stu-id="8daef-273">443</span></span>  <br/> |<span data-ttu-id="8daef-274">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="8daef-274">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="8daef-275">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="8daef-275">_sipfederationtls</span></span>  <br/> |<span data-ttu-id="8daef-276">_tcp</span><span class="sxs-lookup"><span data-stu-id="8daef-276">_tcp</span></span>  <br/> |@  <br/> |<span data-ttu-id="8daef-277">14400</span><span class="sxs-lookup"><span data-stu-id="8daef-277">14400</span></span>  <br/> |<span data-ttu-id="8daef-278">SRV</span><span class="sxs-lookup"><span data-stu-id="8daef-278">SRV</span></span>  <br/> |<span data-ttu-id="8daef-279">100</span><span class="sxs-lookup"><span data-stu-id="8daef-279">100</span></span>  <br/> |<span data-ttu-id="8daef-280">0,1</span><span class="sxs-lookup"><span data-stu-id="8daef-280">1</span></span>  <br/> |<span data-ttu-id="8daef-281">5061</span><span class="sxs-lookup"><span data-stu-id="8daef-281">5061</span></span>  <br/> |<span data-ttu-id="8daef-282">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="8daef-282">sipfed.online.lync.com</span></span>  <br/> |
   
    ![Copier la valeur du nouvel enregistrement](../media/e2911bca-c00b-4b8a-837f-f1d438c474c4.png)
  
5. <span data-ttu-id="8daef-284">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="8daef-284">Select **add record**.</span></span>
    
    ![Sélectionnez Ajouter un enregistrement](../media/0fd6a587-03fd-4bce-8321-b14e6ad21f5c.png)
  
6. <span data-ttu-id="8daef-286">Ajoutez l'autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="8daef-286">Add the other SRV record.</span></span>
    
    <span data-ttu-id="8daef-287">Toujours dans la section **Add DNS record (ajouter un enregistrement DNS** ), créez un enregistrement en utilisant les valeurs de l’autre ligne du tableau, puis sélectionnez de nouveau **Add record (Ajouter** un enregistrement) pour valider cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8daef-287">Still in the **Add DNS Record** section, create a record by using the values from the other row in the table, and then again select **add record** to complete that record.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="8daef-288">Typically it takes about 15 minutes for DNS changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="8daef-288">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="8daef-289">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="8daef-289">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="8daef-290">Si vous rencontrez des problèmes avec le flux de messagerie ou d’autres problèmes après avoir ajouté des enregistrements DNS, consultez [la rubrique Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="8daef-290">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  

