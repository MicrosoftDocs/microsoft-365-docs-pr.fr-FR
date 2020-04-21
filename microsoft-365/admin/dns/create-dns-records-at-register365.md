---
title: Créer des enregistrements DNS sur Register365 pour Microsoft
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
ms.assetid: 004030b4-10ad-4026-96e7-011b6afc7e73
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur Register365 pour Microsoft.
ms.openlocfilehash: 08db53df7510de76c6c5c33d2047cba4203324d8
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43629262"
---
# <a name="create-dns-records-at-register365-for-microsoft"></a><span data-ttu-id="49272-103">Créer des enregistrements DNS sur Register365 pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="49272-103">Create DNS records at Register365 for Microsoft</span></span>

 <span data-ttu-id="49272-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="49272-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="49272-105">Si Register365 est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="49272-105">If Register365 is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span> 
  
<span data-ttu-id="49272-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="49272-106">These are the main records to add.</span></span>  
  
- [<span data-ttu-id="49272-107">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="49272-107">Add a TXT record for verification</span></span>](#add-a-txt-record-for-verification)
    
- [<span data-ttu-id="49272-108">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient envoyés à Microsoft</span><span class="sxs-lookup"><span data-stu-id="49272-108">Add an MX record so email for your domain will come to Microsoft</span></span>](#add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft)
    
- [<span data-ttu-id="49272-109">Ajouter les six enregistrements CNAMe requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="49272-109">Add the six CNAME records that are required for Microsoft</span></span>](#add-the-six-cname-records-that-are-required-for-microsoft)
    
- [<span data-ttu-id="49272-110">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="49272-110">Add a TXT record for SPF to help prevent email spam</span></span>](#add-a-txt-record-for-spf-to-help-prevent-email-spam)
    
- [<span data-ttu-id="49272-111">Ajouter les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="49272-111">Add the two SRV records that are required for Microsoft</span></span>](#add-the-two-srv-records-that-are-required-for-microsoft)
    
<span data-ttu-id="49272-112">Une fois que vous avez ajouté ces enregistrements auprès de Microsoft, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="49272-112">After you add these records at Microsoft, your domain will be set up to work with Microsoft services.</span></span>
  
<span data-ttu-id="49272-113">Pour en savoir plus sur l’hébergement Web et le DNS pour les sites Web avec Microsoft, consultez [la rubrique utiliser un site Web public avec Microsoft](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span><span class="sxs-lookup"><span data-stu-id="49272-113">To learn about webhosting and DNS for websites with Microsoft, see [Use a public website with Microsoft](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="49272-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="49272-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="49272-117">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="49272-117">Add a TXT record for verification</span></span>
<span data-ttu-id="49272-118"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="49272-118"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="49272-119">Avant d’utiliser votre domaine avec Microsoft, vous devez vous assurer que vous en êtes propriétaire.</span><span class="sxs-lookup"><span data-stu-id="49272-119">Before you use your domain with Microsoft, we have to make sure that you own it.</span></span> <span data-ttu-id="49272-120">Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="49272-120">Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="49272-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="49272-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="49272-p104">Pour commencer, accédez à la page de vos domaines sur le site Register365 en utilisant [ce lien](https://admin.register365.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="49272-p104">To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.</span></span>
    
    ![Page de connexion au Panneau de configuration](../../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. <span data-ttu-id="49272-126">Sur la page **Dashboard (Tableau de bord)**, recherchez le nom du domaine à mettre à jour, puis sélectionnez **DNS Settings (Paramètres DNS)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="49272-126">On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="49272-127">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="49272-127">(You may have to scroll down.)</span></span>
    
    ![Sélection des paramètres DNS dans la liste](../../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. <span data-ttu-id="49272-129">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="49272-129">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="49272-130">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="49272-130">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    <span data-ttu-id="49272-131">(Si vous avez besoin d’ajouter une ligne, sélectionnez **Ajouter des enregistrements a/CNAME (+)**.)</span><span class="sxs-lookup"><span data-stu-id="49272-131">(If you need to add a row, select **ADD A/CNAME RECORDS (+)**.)</span></span>
    
    <span data-ttu-id="49272-132">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="49272-132">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="49272-133">**Host name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="49272-133">**Host name**</span></span>|<span data-ttu-id="49272-134">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="49272-134">**Type**</span></span>|<span data-ttu-id="49272-135">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="49272-135">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="49272-136">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="49272-136">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="49272-137">TXT</span><span class="sxs-lookup"><span data-stu-id="49272-137">TXT</span></span>  <br/> |<span data-ttu-id="49272-138">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="49272-138">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="49272-139">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="49272-139">**Note:** This is an example.</span></span> <span data-ttu-id="49272-140">Utilisez votre **adresse de destination ou de pointage** spécifique ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="49272-140">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="49272-141">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="49272-141">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Entrée de valeurs dans la page Add/Modify DNS zone (ajouter/modifier la zone DNS)](../../media/22326005-de95-464d-8e33-08ea31a89b2d.png)
  
4. <span data-ttu-id="49272-143">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="49272-143">Select **Save**.</span></span>
    
    <span data-ttu-id="49272-144">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="49272-144">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/157cfb98-d5d0-48a3-8dd1-c4e759c2f8a8.png)
  
5. <span data-ttu-id="49272-146">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="49272-146">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="49272-147">À présent que vous avez ajouté l’enregistrement sur le site de votre bureau d’enregistrement de domaines, vous allez revenir à Microsoft et demander l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="49272-147">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="49272-148">Lorsque Microsoft trouve l’enregistrement TXT correct, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="49272-148">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="49272-149">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="49272-149">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="49272-150">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="49272-150">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="49272-151">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="49272-151">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="49272-152">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="49272-152">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="49272-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="49272-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="49272-156">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient envoyés à Microsoft</span><span class="sxs-lookup"><span data-stu-id="49272-156">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="49272-157"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="49272-157"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="49272-p107">Pour commencer, accédez à la page de vos domaines sur le site Register365 en utilisant [ce lien](https://admin.register365.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="49272-p107">To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.</span></span>
    
    ![Page de connexion au Panneau de configuration](../../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. <span data-ttu-id="49272-161">Sur la page **Dashboard (Tableau de bord)**, recherchez le nom du domaine à mettre à jour, puis sélectionnez **DNS Settings (Paramètres DNS)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="49272-161">On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="49272-162">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="49272-162">(You may have to scroll down.)</span></span>
    
    ![Sélection des paramètres DNS dans la liste](../../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. <span data-ttu-id="49272-164">Dans la page **Add/Modify DNS Zone (Ajouter/modifier la zone DNS)**, dans la section **Mail exchange records (Enregistrements MX)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="49272-164">On the **Add/Modify DNS Zone** page, in the **Mail exchange records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="49272-165">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="49272-165">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="49272-166">**Host name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="49272-166">**Host name**</span></span>|<span data-ttu-id="49272-167">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="49272-167">**Priority**</span></span>|<span data-ttu-id="49272-168">**Result (Résultat)**</span><span class="sxs-lookup"><span data-stu-id="49272-168">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="49272-169">(Laissez ce champ vide.)</span><span class="sxs-lookup"><span data-stu-id="49272-169">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="49272-170">0,1</span><span class="sxs-lookup"><span data-stu-id="49272-170">1</span></span>  <br/> <span data-ttu-id="49272-171">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="49272-171">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> | <span data-ttu-id="49272-172">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="49272-172">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="49272-173">**Remarque :** Obtenir votre \* \<clé\> de domaine\* à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="49272-173">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>  [<span data-ttu-id="49272-174">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="49272-174">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)     |
   
    ![Entrée de valeurs dans la page Add/Modify DNS zone (ajouter/modifier la zone DNS)](../../media/2d3645a8-9cb8-435e-b895-5535b6b1fffd.png)
  
4. <span data-ttu-id="49272-176">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="49272-176">Select **Save**.</span></span>
    
    <span data-ttu-id="49272-177">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="49272-177">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/0e565fb0-a126-4a48-8ff7-2c2d79d4af32.png)
  
5. <span data-ttu-id="49272-179">Si d'autres enregistrements MX sont répertoriés dans la section **Mail exchange records (Enregistrements MX)**, supprimez-les en les sélectionnant et en appuyant sur la touche **Suppr** de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="49272-179">If there are any other MX records in the **Mail exchange records** section, delete each one by selecting it and then pressing the **Delete** key on your keyboard.</span></span> 
    
    ![Deleting records in the Mail exchange records section](../../media/8cc37e4f-2e85-4242-af0e-78149434167f.png)
  
6. <span data-ttu-id="49272-181">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="49272-181">Select **Save**.</span></span>
    
    <span data-ttu-id="49272-182">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="49272-182">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/1fb69bb5-b5df-4060-adf1-eb26cfaa6c4f.png)
  
## <a name="add-the-six-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="49272-184">Ajouter les six enregistrements CNAMe requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="49272-184">Add the six CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="49272-185"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="49272-185"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="49272-p109">Pour commencer, accédez à la page de vos domaines sur le site Register365 en utilisant [ce lien](https://admin.register365.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="49272-p109">To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.</span></span>
    
    ![Page de connexion au Panneau de configuration](../../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. <span data-ttu-id="49272-189">Sur la page **Dashboard (Tableau de bord)**, recherchez le nom du domaine à mettre à jour, puis sélectionnez **DNS Settings (Paramètres DNS)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="49272-189">On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="49272-190">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="49272-190">(You may have to scroll down.)</span></span>
    
    ![Sélection des paramètres DNS dans la liste](../../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. <span data-ttu-id="49272-192">Dans la page **Add/Modify DNS Zone (Ajouter/modifier la zone DNS)**, dans la section **A, CNAME, AAAA, TXT and NS records (Enregistrements A, CNAME, AAAA, TXT et NS)**, dans les zones des nouveaux enregistrements, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="49272-192">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new records, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="49272-193">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="49272-193">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    <span data-ttu-id="49272-194">(Si vous avez besoin d’ajouter une ligne, sélectionnez **Ajouter des enregistrements a/CNAME (+)**.)</span><span class="sxs-lookup"><span data-stu-id="49272-194">(If you need to add a row, select **ADD A/CNAME RECORDS (+)**.)</span></span>
    
    <span data-ttu-id="49272-195">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="49272-195">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="49272-196">\*\*\*\*Host name (Nom d'hôte)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="49272-196">\*\*\*\*Host name\*\*\*\*</span></span>|<span data-ttu-id="49272-197">\*\*\*\*Type (Type)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="49272-197">\*\*\*\*Type\*\*\*\*</span></span>|<span data-ttu-id="49272-198">\*\*\*\*Result (Résultat)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="49272-198">\*\*\*\*Result\*\*\*\*</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="49272-199">autodiscover</span><span class="sxs-lookup"><span data-stu-id="49272-199">autodiscover</span></span>  <br/> |<span data-ttu-id="49272-200">CNAME</span><span class="sxs-lookup"><span data-stu-id="49272-200">CNAME</span></span>  <br/> |<span data-ttu-id="49272-201">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="49272-201">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="49272-202">sip</span><span class="sxs-lookup"><span data-stu-id="49272-202">sip</span></span>  <br/> |<span data-ttu-id="49272-203">CNAME</span><span class="sxs-lookup"><span data-stu-id="49272-203">CNAME</span></span>  <br/> |<span data-ttu-id="49272-204">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="49272-204">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="49272-205">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="49272-205">lyncdiscover</span></span>  <br/> |<span data-ttu-id="49272-206">CNAME</span><span class="sxs-lookup"><span data-stu-id="49272-206">CNAME</span></span>  <br/> |<span data-ttu-id="49272-207">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="49272-207">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="49272-208">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="49272-208">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="49272-209">CNAME</span><span class="sxs-lookup"><span data-stu-id="49272-209">CNAME</span></span>  <br/> |<span data-ttu-id="49272-210">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="49272-210">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="49272-211">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="49272-211">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="49272-212">CNAME</span><span class="sxs-lookup"><span data-stu-id="49272-212">CNAME</span></span>  <br/> |<span data-ttu-id="49272-213">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="49272-213">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
   
    ![Entrée de valeurs dans la page Add/Modify DNS zone (ajouter/modifier la zone DNS)](../../media/3b79f0de-9cab-4c98-8fa8-c92b35241e8b.png)
  
4. <span data-ttu-id="49272-215">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="49272-215">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/8ded6428-af97-4fd8-9104-477fa22a5586.png)
  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="49272-217">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="49272-217">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="49272-218"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="49272-218"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="49272-219">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="49272-219">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="49272-220">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="49272-220">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="49272-221">Si vous disposez déjà d’un enregistrement SPF pour votre domaine, n’en créez pas pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="49272-221">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="49272-222">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="49272-222">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
1. <span data-ttu-id="49272-p111">Pour commencer, accédez à la page de vos domaines sur le site Register365 en utilisant [ce lien](https://admin.register365.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="49272-p111">To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.</span></span>
    
    ![Page de connexion au Panneau de configuration](../../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. <span data-ttu-id="49272-226">Sur la page **Dashboard (Tableau de bord)**, recherchez le nom du domaine à mettre à jour, puis sélectionnez **DNS Settings (Paramètres DNS)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="49272-226">On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="49272-227">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="49272-227">(You may have to scroll down.)</span></span>
    
    ![Sélection des paramètres DNS dans la liste](../../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. <span data-ttu-id="49272-229">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="49272-229">On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="49272-230">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="49272-230">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    <span data-ttu-id="49272-231">(Si vous avez besoin d’ajouter une ligne, sélectionnez **Ajouter des enregistrements a/CNAME (+)**.)</span><span class="sxs-lookup"><span data-stu-id="49272-231">(If you need to add a row, select **ADD A/CNAME RECORDS (+)**.)</span></span>
    
    <span data-ttu-id="49272-232">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="49272-232">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="49272-233">**Host name (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="49272-233">**Host name**</span></span>|<span data-ttu-id="49272-234">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="49272-234">**Type**</span></span>|<span data-ttu-id="49272-235">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="49272-235">**Result**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="49272-236">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="49272-236">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="49272-237">TXT</span><span class="sxs-lookup"><span data-stu-id="49272-237">TXT</span></span>  <br/> |<span data-ttu-id="49272-238">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="49272-238">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/><span data-ttu-id="49272-239">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="49272-239">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Entrée de valeurs dans la page Add/Modify DNS zone (ajouter/modifier la zone DNS)](../../media/33976398-da8a-439b-8e3d-534503b20ee0.png)
  
4. <span data-ttu-id="49272-241">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="49272-241">Select **Save**.</span></span>
    
    <span data-ttu-id="49272-242">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="49272-242">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/1d8da122-4861-4ca3-bc9b-d01f18557d4c.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="49272-244">Ajouter les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="49272-244">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="49272-245"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="49272-245"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="49272-p112">Pour commencer, accédez à la page de vos domaines sur le site Register365 en utilisant [ce lien](https://admin.register365.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="49272-p112">To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.</span></span>
    
    ![Page de connexion au Panneau de configuration](../../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. <span data-ttu-id="49272-249">Sur la page **Dashboard (Tableau de bord)**, recherchez le nom du domaine à mettre à jour, puis sélectionnez **DNS Settings (Paramètres DNS)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="49272-249">On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list.</span></span> 
    
    <span data-ttu-id="49272-250">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="49272-250">(You may have to scroll down.)</span></span>
    
    ![Sélection des paramètres DNS dans la liste](../../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. <span data-ttu-id="49272-252">Dans la page **Add/Modify DNS Zone (Ajouter/modifier la zone DNS)**, dans la section **Service records (Enregistrements du service)**, dans les zones des nouveaux enregistrements, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="49272-252">On the **Add/Modify DNS Zone** page, in the **Service records** section, in the boxes for the new records, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="49272-253">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="49272-253">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="49272-254">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="49272-254">**Name**</span></span>|<span data-ttu-id="49272-255">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="49272-255">**Priority**</span></span>|<span data-ttu-id="49272-256">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="49272-256">**Weight**</span></span>|<span data-ttu-id="49272-257">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="49272-257">**Port**</span></span>|<span data-ttu-id="49272-258">**Result (Résultat)**</span><span class="sxs-lookup"><span data-stu-id="49272-258">**Result**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="49272-259">_sip. _tls</span><span class="sxs-lookup"><span data-stu-id="49272-259">_sip._tls</span></span>  <br/> |<span data-ttu-id="49272-260">100</span><span class="sxs-lookup"><span data-stu-id="49272-260">100</span></span>  <br/> |<span data-ttu-id="49272-261">0,1</span><span class="sxs-lookup"><span data-stu-id="49272-261">1</span></span>  <br/> |<span data-ttu-id="49272-262">443</span><span class="sxs-lookup"><span data-stu-id="49272-262">443</span></span>  <br/> |<span data-ttu-id="49272-263">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="49272-263">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="49272-264">_sipfederationtls. _tcp</span><span class="sxs-lookup"><span data-stu-id="49272-264">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="49272-265">100</span><span class="sxs-lookup"><span data-stu-id="49272-265">100</span></span>  <br/> |<span data-ttu-id="49272-266">0,1</span><span class="sxs-lookup"><span data-stu-id="49272-266">1</span></span>  <br/> |<span data-ttu-id="49272-267">5061</span><span class="sxs-lookup"><span data-stu-id="49272-267">5061</span></span>  <br/> |<span data-ttu-id="49272-268">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="49272-268">sipfed.online.lync.com</span></span>  <br/> |
   
    ![Entrée de valeurs dans la section des enregistrements de service](../../media/56bb1813-90e2-40c8-98bf-750e2dc3f8b6.png)
  
4. <span data-ttu-id="49272-270">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="49272-270">Select **Save**.</span></span>
    
    <span data-ttu-id="49272-271">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="49272-271">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/3b80757c-01e1-492d-b2ce-f721d71f7235.png)
  
> [!NOTE]
>  <span data-ttu-id="49272-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="49272-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
