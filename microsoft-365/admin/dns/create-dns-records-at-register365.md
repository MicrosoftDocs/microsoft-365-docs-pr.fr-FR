---
title: Créer des enregistrements DNS auprès de Register365 pour Office 365
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
ms.assetid: 004030b4-10ad-4026-96e7-011b6afc7e73
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur Register365 pour Office 365.
ms.openlocfilehash: 7f9398e14ea5280948829b263d4cd66d61fab682
ms.sourcegitcommit: 812aab5f58eed4bf359faf0e99f7f876af5b1023
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/02/2020
ms.locfileid: "42362849"
---
# <a name="create-dns-records-at-register365-for-office-365"></a><span data-ttu-id="2dcc8-103">Créer des enregistrements DNS auprès de Register365 pour Office 365</span><span class="sxs-lookup"><span data-stu-id="2dcc8-103">Create DNS records at Register365 for Office 365</span></span>

 <span data-ttu-id="2dcc8-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="2dcc8-105">Si Register365 est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-105">If Register365 is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span> 
  
<span data-ttu-id="2dcc8-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-106">These are the main records to add.</span></span>  
  
- [<span data-ttu-id="2dcc8-107">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="2dcc8-107">Add a TXT record for verification</span></span>](#add-a-txt-record-for-verification)
    
- [<span data-ttu-id="2dcc8-108">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="2dcc8-108">Add an MX record so email for your domain will come to Office 365</span></span>](#add-an-mx-record-so-email-for-your-domain-will-come-to-office-365)
    
- [<span data-ttu-id="2dcc8-109">Ajouter les 6 enregistrements CNAME requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="2dcc8-109">Add the six CNAME records that are required for Office 365</span></span>](#add-the-six-cname-records-that-are-required-for-office-365)
    
- [<span data-ttu-id="2dcc8-110">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="2dcc8-110">Add a TXT record for SPF to help prevent email spam</span></span>](#add-a-txt-record-for-spf-to-help-prevent-email-spam)
    
- [<span data-ttu-id="2dcc8-111">Ajouter les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="2dcc8-111">Add the two SRV records that are required for Office 365</span></span>](#add-the-two-srv-records-that-are-required-for-office-365)
    
<span data-ttu-id="2dcc8-112">Après avoir ajouté ces enregistrements sur Office 365, votre domaine sera configuré de manière à utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-112">After you add these records at Office 365, your domain will be set up to work with Office 365 services.</span></span>
  
<span data-ttu-id="2dcc8-113">Pour en savoir plus sur l'hébergement web et le DNS pour les sites web avec Office 365, voir [Utiliser un site web public avec Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span><span class="sxs-lookup"><span data-stu-id="2dcc8-113">To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="2dcc8-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="2dcc8-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="2dcc8-117">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="2dcc8-117">Add a TXT record for verification</span></span>
<span data-ttu-id="2dcc8-118"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="2dcc8-118"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="2dcc8-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2dcc8-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="2dcc8-p104">Pour commencer, accédez à la page de vos domaines sur le site Register365 en utilisant [ce lien](https://admin.register365.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-p104">To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.</span></span>
    
    ![Page de connexion au Panneau de configuration](../../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. <span data-ttu-id="2dcc8-126">Sur la page **Dashboard (Tableau de bord)**, recherchez le nom du domaine à mettre à jour, puis sélectionnez **DNS Settings (Paramètres DNS)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-126">On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="2dcc8-127">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-127">(You may have to scroll down.)</span></span>
    
    ![Sélection des paramètres DNS dans la liste](../../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. <span data-ttu-id="2dcc8-129">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-129">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="2dcc8-130">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-130">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    <span data-ttu-id="2dcc8-131">(Si vous avez besoin d’ajouter une ligne, sélectionnez **Ajouter des enregistrements a/CNAME (+)**.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-131">(If you need to add a row, select **ADD A/CNAME RECORDS (+)**.)</span></span>
    
    <span data-ttu-id="2dcc8-132">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-132">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="2dcc8-133">**Host name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="2dcc8-133">**Host name**</span></span>|<span data-ttu-id="2dcc8-134">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="2dcc8-134">**Type**</span></span>|<span data-ttu-id="2dcc8-135">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="2dcc8-135">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="2dcc8-136">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-136">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="2dcc8-137">TXT</span><span class="sxs-lookup"><span data-stu-id="2dcc8-137">TXT</span></span>  <br/> |<span data-ttu-id="2dcc8-138">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="2dcc8-138">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="2dcc8-139">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-139">**Note:** This is an example.</span></span> <span data-ttu-id="2dcc8-140">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-140">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span>           [<span data-ttu-id="2dcc8-141">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="2dcc8-141">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Entrée de valeurs dans la page Add/Modify DNS zone (ajouter/modifier la zone DNS)](../../media/22326005-de95-464d-8e33-08ea31a89b2d.png)
  
4. <span data-ttu-id="2dcc8-143">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-143">Select **Save**.</span></span>
    
    <span data-ttu-id="2dcc8-144">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-144">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/157cfb98-d5d0-48a3-8dd1-c4e759c2f8a8.png)
  
5. <span data-ttu-id="2dcc8-146">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-146">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="2dcc8-147">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Office 365 et demandez à Office 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-147">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="2dcc8-148">Lorsqu’Office 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-148">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="2dcc8-149">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-149">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="2dcc8-150">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-150">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="2dcc8-151">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-151">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="2dcc8-152">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-152">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="2dcc8-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="2dcc8-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="2dcc8-156">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="2dcc8-156">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="2dcc8-157"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="2dcc8-157"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="2dcc8-p107">Pour commencer, accédez à la page de vos domaines sur le site Register365 en utilisant [ce lien](https://admin.register365.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-p107">To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.</span></span>
    
    ![Page de connexion au Panneau de configuration](../../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. <span data-ttu-id="2dcc8-161">Sur la page **Dashboard (Tableau de bord)**, recherchez le nom du domaine à mettre à jour, puis sélectionnez **DNS Settings (Paramètres DNS)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-161">On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="2dcc8-162">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-162">(You may have to scroll down.)</span></span>
    
    ![Sélection des paramètres DNS dans la liste](../../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. <span data-ttu-id="2dcc8-164">Dans la page **Add/Modify DNS Zone (Ajouter/modifier la zone DNS)**, dans la section **Mail exchange records (Enregistrements MX)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-164">On the **Add/Modify DNS Zone** page, in the **Mail exchange records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="2dcc8-165">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-165">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="2dcc8-166">**Host name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="2dcc8-166">**Host name**</span></span>|<span data-ttu-id="2dcc8-167">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="2dcc8-167">**Priority**</span></span>|<span data-ttu-id="2dcc8-168">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="2dcc8-168">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="2dcc8-169">(Laissez ce champ vide.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-169">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="2dcc8-170">0,1</span><span class="sxs-lookup"><span data-stu-id="2dcc8-170">1</span></span>  <br/> <span data-ttu-id="2dcc8-171">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="2dcc8-171">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> | <span data-ttu-id="2dcc8-172">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="2dcc8-172">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="2dcc8-173">**Remarque :** Obtenez votre \* \<clé\> de domaine\* à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-173">**Note:** Get your  *\<domain-key\>*  from your Office 365 account.</span></span>  [<span data-ttu-id="2dcc8-174">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="2dcc8-174">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)     |
   
    ![Entrée de valeurs dans la page Add/Modify DNS zone (ajouter/modifier la zone DNS)](../../media/2d3645a8-9cb8-435e-b895-5535b6b1fffd.png)
  
4. <span data-ttu-id="2dcc8-176">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-176">Select **Save**.</span></span>
    
    <span data-ttu-id="2dcc8-177">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-177">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/0e565fb0-a126-4a48-8ff7-2c2d79d4af32.png)
  
5. <span data-ttu-id="2dcc8-179">Si d'autres enregistrements MX sont répertoriés dans la section **Mail exchange records (Enregistrements MX)**, supprimez-les en les sélectionnant et en appuyant sur la touche **Suppr** de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-179">If there are any other MX records in the **Mail exchange records** section, delete each one by selecting it and then pressing the **Delete** key on your keyboard.</span></span> 
    
    ![Deleting records in the Mail exchange records section](../../media/8cc37e4f-2e85-4242-af0e-78149434167f.png)
  
6. <span data-ttu-id="2dcc8-181">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-181">Select **Save**.</span></span>
    
    <span data-ttu-id="2dcc8-182">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-182">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/1fb69bb5-b5df-4060-adf1-eb26cfaa6c4f.png)
  
## <a name="add-the-six-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="2dcc8-184">Ajouter les 6 enregistrements CNAME requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="2dcc8-184">Add the six CNAME records that are required for Office 365</span></span>
<span data-ttu-id="2dcc8-185"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="2dcc8-185"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="2dcc8-p109">Pour commencer, accédez à la page de vos domaines sur le site Register365 en utilisant [ce lien](https://admin.register365.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-p109">To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.</span></span>
    
    ![Page de connexion au Panneau de configuration](../../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. <span data-ttu-id="2dcc8-189">Sur la page **Dashboard (Tableau de bord)**, recherchez le nom du domaine à mettre à jour, puis sélectionnez **DNS Settings (Paramètres DNS)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-189">On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="2dcc8-190">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-190">(You may have to scroll down.)</span></span>
    
    ![Sélection des paramètres DNS dans la liste](../../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. <span data-ttu-id="2dcc8-192">Dans la page **Add/Modify DNS Zone (Ajouter/modifier la zone DNS)**, dans la section **A, CNAME, AAAA, TXT and NS records (Enregistrements A, CNAME, AAAA, TXT et NS)**, dans les zones des nouveaux enregistrements, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-192">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new records, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="2dcc8-193">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-193">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    <span data-ttu-id="2dcc8-194">(Si vous avez besoin d’ajouter une ligne, sélectionnez **Ajouter des enregistrements a/CNAME (+)**.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-194">(If you need to add a row, select **ADD A/CNAME RECORDS (+)**.)</span></span>
    
    <span data-ttu-id="2dcc8-195">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-195">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="2dcc8-196">\*\*\*\*Host name (Nom d'hôte)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2dcc8-196">\*\*\*\*Host name\*\*\*\*</span></span>|<span data-ttu-id="2dcc8-197">\*\*\*\*Type (Type)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2dcc8-197">\*\*\*\*Type\*\*\*\*</span></span>|<span data-ttu-id="2dcc8-198">\*\*\*\*Result (Résultat)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2dcc8-198">\*\*\*\*Result\*\*\*\*</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="2dcc8-199">autodiscover</span><span class="sxs-lookup"><span data-stu-id="2dcc8-199">autodiscover</span></span>  <br/> |<span data-ttu-id="2dcc8-200">CNAME</span><span class="sxs-lookup"><span data-stu-id="2dcc8-200">CNAME</span></span>  <br/> |<span data-ttu-id="2dcc8-201">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="2dcc8-201">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="2dcc8-202">sip</span><span class="sxs-lookup"><span data-stu-id="2dcc8-202">sip</span></span>  <br/> |<span data-ttu-id="2dcc8-203">CNAME</span><span class="sxs-lookup"><span data-stu-id="2dcc8-203">CNAME</span></span>  <br/> |<span data-ttu-id="2dcc8-204">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="2dcc8-204">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="2dcc8-205">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="2dcc8-205">lyncdiscover</span></span>  <br/> |<span data-ttu-id="2dcc8-206">CNAME</span><span class="sxs-lookup"><span data-stu-id="2dcc8-206">CNAME</span></span>  <br/> |<span data-ttu-id="2dcc8-207">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="2dcc8-207">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="2dcc8-208">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="2dcc8-208">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="2dcc8-209">CNAME</span><span class="sxs-lookup"><span data-stu-id="2dcc8-209">CNAME</span></span>  <br/> |<span data-ttu-id="2dcc8-210">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="2dcc8-210">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="2dcc8-211">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="2dcc8-211">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="2dcc8-212">CNAME</span><span class="sxs-lookup"><span data-stu-id="2dcc8-212">CNAME</span></span>  <br/> |<span data-ttu-id="2dcc8-213">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="2dcc8-213">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
   
    ![Entrée de valeurs dans la page Add/Modify DNS zone (ajouter/modifier la zone DNS)](../../media/3b79f0de-9cab-4c98-8fa8-c92b35241e8b.png)
  
4. <span data-ttu-id="2dcc8-215">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-215">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/8ded6428-af97-4fd8-9104-477fa22a5586.png)
  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="2dcc8-217">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="2dcc8-217">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="2dcc8-218"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="2dcc8-218"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="2dcc8-219">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-219">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="2dcc8-220">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-220">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="2dcc8-221">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-221">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="2dcc8-222">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-222">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
1. <span data-ttu-id="2dcc8-p111">Pour commencer, accédez à la page de vos domaines sur le site Register365 en utilisant [ce lien](https://admin.register365.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-p111">To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.</span></span>
    
    ![Page de connexion au Panneau de configuration](../../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. <span data-ttu-id="2dcc8-226">Sur la page **Dashboard (Tableau de bord)**, recherchez le nom du domaine à mettre à jour, puis sélectionnez **DNS Settings (Paramètres DNS)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-226">On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="2dcc8-227">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-227">(You may have to scroll down.)</span></span>
    
    ![Sélection des paramètres DNS dans la liste](../../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. <span data-ttu-id="2dcc8-229">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-229">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="2dcc8-230">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-230">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    <span data-ttu-id="2dcc8-231">(Si vous avez besoin d’ajouter une ligne, sélectionnez **Ajouter des enregistrements a/CNAME (+)**.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-231">(If you need to add a row, select **ADD A/CNAME RECORDS (+)**.)</span></span>
    
    <span data-ttu-id="2dcc8-232">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-232">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="2dcc8-233">**Host name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="2dcc8-233">**Host name**</span></span>|<span data-ttu-id="2dcc8-234">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="2dcc8-234">**Type**</span></span>|<span data-ttu-id="2dcc8-235">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="2dcc8-235">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="2dcc8-236">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-236">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="2dcc8-237">TXT</span><span class="sxs-lookup"><span data-stu-id="2dcc8-237">TXT</span></span>  <br/> |<span data-ttu-id="2dcc8-238">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="2dcc8-238">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/><span data-ttu-id="2dcc8-239">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-239">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Entrée de valeurs dans la page Add/Modify DNS zone (ajouter/modifier la zone DNS)](../../media/33976398-da8a-439b-8e3d-534503b20ee0.png)
  
4. <span data-ttu-id="2dcc8-241">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-241">Select **Save**.</span></span>
    
    <span data-ttu-id="2dcc8-242">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-242">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/1d8da122-4861-4ca3-bc9b-d01f18557d4c.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="2dcc8-244">Ajoutez les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="2dcc8-244">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="2dcc8-245"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="2dcc8-245"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="2dcc8-p112">Pour commencer, accédez à la page de vos domaines sur le site Register365 en utilisant [ce lien](https://admin.register365.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-p112">To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.</span></span>
    
    ![Page de connexion au Panneau de configuration](../../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. <span data-ttu-id="2dcc8-249">Sur la page **Dashboard (Tableau de bord)**, recherchez le nom du domaine à mettre à jour, puis sélectionnez **DNS Settings (Paramètres DNS)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-249">On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="2dcc8-250">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-250">(You may have to scroll down.)</span></span>
    
    ![Sélection des paramètres DNS dans la liste](../../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. <span data-ttu-id="2dcc8-252">Dans la page **Add/Modify DNS Zone (Ajouter/modifier la zone DNS)**, dans la section **Service records (Enregistrements du service)**, dans les zones des nouveaux enregistrements, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-252">On the **Add/Modify DNS Zone** page, in the **Service records** section, in the boxes for the new records, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="2dcc8-253">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-253">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="2dcc8-254">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="2dcc8-254">**Name**</span></span>|<span data-ttu-id="2dcc8-255">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="2dcc8-255">**Priority**</span></span>|<span data-ttu-id="2dcc8-256">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="2dcc8-256">**Weight**</span></span>|<span data-ttu-id="2dcc8-257">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="2dcc8-257">**Port**</span></span>|<span data-ttu-id="2dcc8-258">**Result (Résultat)**</span><span class="sxs-lookup"><span data-stu-id="2dcc8-258">**Result**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="2dcc8-259">_sip. _tls</span><span class="sxs-lookup"><span data-stu-id="2dcc8-259">_sip._tls</span></span>  <br/> |<span data-ttu-id="2dcc8-260">100</span><span class="sxs-lookup"><span data-stu-id="2dcc8-260">100</span></span>  <br/> |<span data-ttu-id="2dcc8-261">0,1</span><span class="sxs-lookup"><span data-stu-id="2dcc8-261">1</span></span>  <br/> |<span data-ttu-id="2dcc8-262">443</span><span class="sxs-lookup"><span data-stu-id="2dcc8-262">443</span></span>  <br/> |<span data-ttu-id="2dcc8-263">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="2dcc8-263">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="2dcc8-264">_sipfederationtls. _tcp</span><span class="sxs-lookup"><span data-stu-id="2dcc8-264">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="2dcc8-265">100</span><span class="sxs-lookup"><span data-stu-id="2dcc8-265">100</span></span>  <br/> |<span data-ttu-id="2dcc8-266">0,1</span><span class="sxs-lookup"><span data-stu-id="2dcc8-266">1</span></span>  <br/> |<span data-ttu-id="2dcc8-267">5061</span><span class="sxs-lookup"><span data-stu-id="2dcc8-267">5061</span></span>  <br/> |<span data-ttu-id="2dcc8-268">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="2dcc8-268">sipfed.online.lync.com</span></span>  <br/> |
   
    ![Entrée de valeurs dans la section des enregistrements de service](../../media/56bb1813-90e2-40c8-98bf-750e2dc3f8b6.png)
  
4. <span data-ttu-id="2dcc8-270">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2dcc8-270">Select **Save**.</span></span>
    
    <span data-ttu-id="2dcc8-271">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="2dcc8-271">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/3b80757c-01e1-492d-b2ce-f721d71f7235.png)
  
> [!NOTE]
>  <span data-ttu-id="2dcc8-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="2dcc8-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
