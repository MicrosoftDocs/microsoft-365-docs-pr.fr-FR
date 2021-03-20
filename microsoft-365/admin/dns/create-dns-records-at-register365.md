---
title: Créer des enregistrements DNS auprès de Register365 pour Microsoft
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
ms.assetid: 004030b4-10ad-4026-96e7-011b6afc7e73
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype Entreprise Online et d’autres services auprès de Register365 pour Microsoft.
ms.openlocfilehash: a0bf077a6e034add48e9745711fb37d59e2c8203
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50910005"
---
# <a name="create-dns-records-at-register365-for-microsoft"></a><span data-ttu-id="8d0b9-103">Créer des enregistrements DNS auprès de Register365 pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="8d0b9-103">Create DNS records at Register365 for Microsoft</span></span>

 <span data-ttu-id="8d0b9-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="8d0b9-105">Si Register365 est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-105">If Register365 is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span> 
  
<span data-ttu-id="8d0b9-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-106">These are the main records to add.</span></span>  
  
- [<span data-ttu-id="8d0b9-107">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="8d0b9-107">Add a TXT record for verification</span></span>](#add-a-txt-record-for-verification)
    
- [<span data-ttu-id="8d0b9-108">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="8d0b9-108">Add an MX record so email for your domain will come to Microsoft</span></span>](#add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft)
    
- [<span data-ttu-id="8d0b9-109">Ajouter les six enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="8d0b9-109">Add the six CNAME records that are required for Microsoft</span></span>](#add-the-six-cname-records-that-are-required-for-microsoft)
    
- [<span data-ttu-id="8d0b9-110">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="8d0b9-110">Add a TXT record for SPF to help prevent email spam</span></span>](#add-a-txt-record-for-spf-to-help-prevent-email-spam)
    
- [<span data-ttu-id="8d0b9-111">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="8d0b9-111">Add the two SRV records that are required for Microsoft</span></span>](#add-the-two-srv-records-that-are-required-for-microsoft)
    
<span data-ttu-id="8d0b9-112">Une fois ces enregistrements ajoutés chez Microsoft, votre domaine est installé pour fonctionner avec les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-112">After you add these records at Microsoft, your domain will be set up to work with Microsoft services.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="8d0b9-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="8d0b9-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="8d0b9-116">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="8d0b9-116">Add a TXT record for verification</span></span>
<span data-ttu-id="8d0b9-117"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="8d0b9-117"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="8d0b9-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8d0b9-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="8d0b9-p104">Pour commencer, accédez à la page de vos domaines sur le site Register365 en utilisant [ce lien](https://admin.register365.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-p104">To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.</span></span>
    
    ![Page de connexion au Panneau de configuration](../../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. <span data-ttu-id="8d0b9-125">Sur la page **Dashboard (Tableau de bord)**, recherchez le nom du domaine à mettre à jour, puis sélectionnez **DNS Settings (Paramètres DNS)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-125">On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="8d0b9-126">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-126">(You may have to scroll down.)</span></span>
    
    ![Sélection des paramètres DNS dans la liste](../../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. <span data-ttu-id="8d0b9-128">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-128">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="8d0b9-129">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-129">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    <span data-ttu-id="8d0b9-130">(Si vous devez ajouter une ligne, sélectionnez **AJOUTER DES ENREGISTREMENTS A/CNAME (+)**.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-130">(If you need to add a row, select **ADD A/CNAME RECORDS (+)**.)</span></span>
    
    <span data-ttu-id="8d0b9-131">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-131">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="8d0b9-132">**Host name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="8d0b9-132">**Host name**</span></span>|<span data-ttu-id="8d0b9-133">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="8d0b9-133">**Type**</span></span>|<span data-ttu-id="8d0b9-134">**Result (Résultat)**</span><span class="sxs-lookup"><span data-stu-id="8d0b9-134">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="8d0b9-135">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-135">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="8d0b9-136">TXT</span><span class="sxs-lookup"><span data-stu-id="8d0b9-136">TXT</span></span>  <br/> |<span data-ttu-id="8d0b9-137">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="8d0b9-137">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="8d0b9-138">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-138">**Note:** This is an example.</span></span> <span data-ttu-id="8d0b9-139">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-139">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="8d0b9-140">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="8d0b9-140">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Saisie de valeurs dans la page Ajouter/Modifier une zone DNS](../../media/22326005-de95-464d-8e33-08ea31a89b2d.png)
  
4. <span data-ttu-id="8d0b9-142">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-142">Select **Save**.</span></span>
    
    <span data-ttu-id="8d0b9-143">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-143">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Enregistrer](../../media/157cfb98-d5d0-48a3-8dd1-c4e759c2f8a8.png)
  
5. <span data-ttu-id="8d0b9-145">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-145">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="8d0b9-146">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-146">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="8d0b9-147">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-147">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="8d0b9-148">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-148">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="8d0b9-149">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-149">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="8d0b9-150">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-150">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="8d0b9-151">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-151">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="8d0b9-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="8d0b9-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="8d0b9-155">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="8d0b9-155">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="8d0b9-156"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="8d0b9-156"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="8d0b9-p107">Pour commencer, accédez à la page de vos domaines sur le site Register365 en utilisant [ce lien](https://admin.register365.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-p107">To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.</span></span>
    
    ![Page de connexion au Panneau de configuration](../../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. <span data-ttu-id="8d0b9-160">Sur la page **Dashboard (Tableau de bord)**, recherchez le nom du domaine à mettre à jour, puis sélectionnez **DNS Settings (Paramètres DNS)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-160">On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="8d0b9-161">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-161">(You may have to scroll down.)</span></span>
    
    ![Sélection des paramètres DNS dans la liste](../../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. <span data-ttu-id="8d0b9-163">Dans la page **Add/Modify DNS Zone (Ajouter/modifier la zone DNS)**, dans la section **Mail exchange records (Enregistrements MX)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-163">On the **Add/Modify DNS Zone** page, in the **Mail exchange records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="8d0b9-164">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-164">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="8d0b9-165">**Host name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="8d0b9-165">**Host name**</span></span>|<span data-ttu-id="8d0b9-166">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="8d0b9-166">**Priority**</span></span>|<span data-ttu-id="8d0b9-167">**Result (Résultat)**</span><span class="sxs-lookup"><span data-stu-id="8d0b9-167">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="8d0b9-168">(Laissez ce champ vide.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-168">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="8d0b9-169">1</span><span class="sxs-lookup"><span data-stu-id="8d0b9-169">1</span></span>  <br/> <span data-ttu-id="8d0b9-170">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](../setup/domains-faq.yml).</span><span class="sxs-lookup"><span data-stu-id="8d0b9-170">For more information about priority, see [What is MX priority?](../setup/domains-faq.yml)</span></span> <br/> | <span data-ttu-id="8d0b9-171">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="8d0b9-171">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="8d0b9-172">**Remarque :** Obtenez votre *\<domain-key\>* depuis votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-172">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>  [<span data-ttu-id="8d0b9-173">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="8d0b9-173">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)     |
   
    ![Saisie de valeurs dans la page Ajouter/Modifier une zone DNS](../../media/2d3645a8-9cb8-435e-b895-5535b6b1fffd.png)
  
4. <span data-ttu-id="8d0b9-175">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-175">Select **Save**.</span></span>
    
    <span data-ttu-id="8d0b9-176">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-176">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Enregistrer](../../media/0e565fb0-a126-4a48-8ff7-2c2d79d4af32.png)
  
5. <span data-ttu-id="8d0b9-178">Si d'autres enregistrements MX sont répertoriés dans la section **Mail exchange records (Enregistrements MX)**, supprimez-les en les sélectionnant et en appuyant sur la touche **Suppr** de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-178">If there are any other MX records in the **Mail exchange records** section, delete each one by selecting it and then pressing the **Delete** key on your keyboard.</span></span> 
    
    ![Deleting records in the Mail exchange records section](../../media/8cc37e4f-2e85-4242-af0e-78149434167f.png)
  
6. <span data-ttu-id="8d0b9-180">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-180">Select **Save**.</span></span>
    
    <span data-ttu-id="8d0b9-181">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-181">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Enregistrer](../../media/1fb69bb5-b5df-4060-adf1-eb26cfaa6c4f.png)
  
## <a name="add-the-six-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="8d0b9-183">Ajouter les six enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="8d0b9-183">Add the six CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="8d0b9-184"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="8d0b9-184"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="8d0b9-p109">Pour commencer, accédez à la page de vos domaines sur le site Register365 en utilisant [ce lien](https://admin.register365.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-p109">To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.</span></span>
    
    ![Page de connexion au Panneau de configuration](../../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. <span data-ttu-id="8d0b9-188">Sur la page **Dashboard (Tableau de bord)**, recherchez le nom du domaine à mettre à jour, puis sélectionnez **DNS Settings (Paramètres DNS)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-188">On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="8d0b9-189">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-189">(You may have to scroll down.)</span></span>
    
    ![Sélection des paramètres DNS dans la liste](../../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. <span data-ttu-id="8d0b9-191">Dans la page **Add/Modify DNS Zone (Ajouter/modifier la zone DNS)**, dans la section **A, CNAME, AAAA, TXT and NS records (Enregistrements A, CNAME, AAAA, TXT et NS)**, dans les zones des nouveaux enregistrements, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-191">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new records, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="8d0b9-192">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-192">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    <span data-ttu-id="8d0b9-193">(Si vous devez ajouter une ligne, sélectionnez **AJOUTER DES ENREGISTREMENTS A/CNAME (+)**.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-193">(If you need to add a row, select **ADD A/CNAME RECORDS (+)**.)</span></span>
    
    <span data-ttu-id="8d0b9-194">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-194">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="8d0b9-195">\*\*\*\*Host name (Nom d'hôte)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8d0b9-195">\*\*\*\*Host name\*\*\*\*</span></span>|<span data-ttu-id="8d0b9-196">\*\*\*\*Type (Type)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8d0b9-196">\*\*\*\*Type\*\*\*\*</span></span>|<span data-ttu-id="8d0b9-197">\*\*\*\*Result (Résultat)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8d0b9-197">\*\*\*\*Result\*\*\*\*</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="8d0b9-198">autodiscover</span><span class="sxs-lookup"><span data-stu-id="8d0b9-198">autodiscover</span></span>  <br/> |<span data-ttu-id="8d0b9-199">CNAME</span><span class="sxs-lookup"><span data-stu-id="8d0b9-199">CNAME</span></span>  <br/> |<span data-ttu-id="8d0b9-200">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="8d0b9-200">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="8d0b9-201">sip</span><span class="sxs-lookup"><span data-stu-id="8d0b9-201">sip</span></span>  <br/> |<span data-ttu-id="8d0b9-202">CNAME</span><span class="sxs-lookup"><span data-stu-id="8d0b9-202">CNAME</span></span>  <br/> |<span data-ttu-id="8d0b9-203">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="8d0b9-203">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="8d0b9-204">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="8d0b9-204">lyncdiscover</span></span>  <br/> |<span data-ttu-id="8d0b9-205">CNAME</span><span class="sxs-lookup"><span data-stu-id="8d0b9-205">CNAME</span></span>  <br/> |<span data-ttu-id="8d0b9-206">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="8d0b9-206">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="8d0b9-207">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="8d0b9-207">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="8d0b9-208">CNAME</span><span class="sxs-lookup"><span data-stu-id="8d0b9-208">CNAME</span></span>  <br/> |<span data-ttu-id="8d0b9-209">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="8d0b9-209">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="8d0b9-210">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="8d0b9-210">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="8d0b9-211">CNAME</span><span class="sxs-lookup"><span data-stu-id="8d0b9-211">CNAME</span></span>  <br/> |<span data-ttu-id="8d0b9-212">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="8d0b9-212">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
   
    ![Saisie de valeurs dans la page Ajouter/Modifier une zone DNS](../../media/3b79f0de-9cab-4c98-8fa8-c92b35241e8b.png)
  
4. <span data-ttu-id="8d0b9-214">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-214">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer](../../media/8ded6428-af97-4fd8-9104-477fa22a5586.png)
  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="8d0b9-216">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="8d0b9-216">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="8d0b9-217"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="8d0b9-217"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d0b9-218">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-218">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="8d0b9-219">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-219">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="8d0b9-220">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-220">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="8d0b9-221">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel de manière à n’avoir *qu’un seul* enregistrement SPF incluant les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-221">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
1. <span data-ttu-id="8d0b9-p111">Pour commencer, accédez à la page de vos domaines sur le site Register365 en utilisant [ce lien](https://admin.register365.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-p111">To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.</span></span>
    
    ![Page de connexion au Panneau de configuration](../../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. <span data-ttu-id="8d0b9-225">Sur la page **Dashboard (Tableau de bord)**, recherchez le nom du domaine à mettre à jour, puis sélectionnez **DNS Settings (Paramètres DNS)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-225">On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="8d0b9-226">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-226">(You may have to scroll down.)</span></span>
    
    ![Sélection des paramètres DNS dans la liste](../../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. <span data-ttu-id="8d0b9-228">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-228">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="8d0b9-229">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-229">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    <span data-ttu-id="8d0b9-230">(Si vous devez ajouter une ligne, sélectionnez **AJOUTER DES ENREGISTREMENTS A/CNAME (+)**.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-230">(If you need to add a row, select **ADD A/CNAME RECORDS (+)**.)</span></span>
    
    <span data-ttu-id="8d0b9-231">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-231">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="8d0b9-232">**Host name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="8d0b9-232">**Host name**</span></span>|<span data-ttu-id="8d0b9-233">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="8d0b9-233">**Type**</span></span>|<span data-ttu-id="8d0b9-234">**Result (Résultat)**</span><span class="sxs-lookup"><span data-stu-id="8d0b9-234">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="8d0b9-235">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-235">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="8d0b9-236">TXT</span><span class="sxs-lookup"><span data-stu-id="8d0b9-236">TXT</span></span>  <br/> |<span data-ttu-id="8d0b9-237">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="8d0b9-237">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/><span data-ttu-id="8d0b9-238">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-238">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Saisie de valeurs dans la page Ajouter/Modifier une zone DNS](../../media/33976398-da8a-439b-8e3d-534503b20ee0.png)
  
4. <span data-ttu-id="8d0b9-240">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-240">Select **Save**.</span></span>
    
    <span data-ttu-id="8d0b9-241">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-241">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Enregistrer](../../media/1d8da122-4861-4ca3-bc9b-d01f18557d4c.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="8d0b9-243">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="8d0b9-243">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="8d0b9-244"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="8d0b9-244"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="8d0b9-p112">Pour commencer, accédez à la page de vos domaines sur le site Register365 en utilisant [ce lien](https://admin.register365.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-p112">To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.</span></span>
    
    ![Page de connexion au Panneau de configuration](../../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. <span data-ttu-id="8d0b9-248">Sur la page **Dashboard (Tableau de bord)**, recherchez le nom du domaine à mettre à jour, puis sélectionnez **DNS Settings (Paramètres DNS)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-248">On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="8d0b9-249">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-249">(You may have to scroll down.)</span></span>
    
    ![Sélection des paramètres DNS dans la liste](../../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. <span data-ttu-id="8d0b9-251">Dans la page **Add/Modify DNS Zone (Ajouter/modifier la zone DNS)**, dans la section **Service records (Enregistrements du service)**, dans les zones des nouveaux enregistrements, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-251">On the **Add/Modify DNS Zone** page, in the **Service records** section, in the boxes for the new records, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="8d0b9-252">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-252">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="8d0b9-253">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="8d0b9-253">**Name**</span></span>|<span data-ttu-id="8d0b9-254">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="8d0b9-254">**Priority**</span></span>|<span data-ttu-id="8d0b9-255">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="8d0b9-255">**Weight**</span></span>|<span data-ttu-id="8d0b9-256">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="8d0b9-256">**Port**</span></span>|<span data-ttu-id="8d0b9-257">**Result (Résultat)**</span><span class="sxs-lookup"><span data-stu-id="8d0b9-257">**Result**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="8d0b9-258">_sip._tls</span><span class="sxs-lookup"><span data-stu-id="8d0b9-258">_sip._tls</span></span>  <br/> |<span data-ttu-id="8d0b9-259">100</span><span class="sxs-lookup"><span data-stu-id="8d0b9-259">100</span></span>  <br/> |<span data-ttu-id="8d0b9-260">1</span><span class="sxs-lookup"><span data-stu-id="8d0b9-260">1</span></span>  <br/> |<span data-ttu-id="8d0b9-261">443</span><span class="sxs-lookup"><span data-stu-id="8d0b9-261">443</span></span>  <br/> |<span data-ttu-id="8d0b9-262">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="8d0b9-262">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="8d0b9-263">_sipfederationtls._tcp</span><span class="sxs-lookup"><span data-stu-id="8d0b9-263">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="8d0b9-264">100</span><span class="sxs-lookup"><span data-stu-id="8d0b9-264">100</span></span>  <br/> |<span data-ttu-id="8d0b9-265">1</span><span class="sxs-lookup"><span data-stu-id="8d0b9-265">1</span></span>  <br/> |<span data-ttu-id="8d0b9-266">5061</span><span class="sxs-lookup"><span data-stu-id="8d0b9-266">5061</span></span>  <br/> |<span data-ttu-id="8d0b9-267">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="8d0b9-267">sipfed.online.lync.com</span></span>  <br/> |
   
    ![Saisie de valeurs dans la section Enregistrements de service](../../media/56bb1813-90e2-40c8-98bf-750e2dc3f8b6.png)
  
4. <span data-ttu-id="8d0b9-269">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8d0b9-269">Select **Save**.</span></span>
    
    <span data-ttu-id="8d0b9-270">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="8d0b9-270">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Enregistrer](../../media/3b80757c-01e1-492d-b2ce-f721d71f7235.png)
  
> [!NOTE]
>  <span data-ttu-id="8d0b9-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="8d0b9-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
