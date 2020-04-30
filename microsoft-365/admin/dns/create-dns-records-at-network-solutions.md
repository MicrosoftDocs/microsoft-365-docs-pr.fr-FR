---
title: Créer des enregistrements DNS sur les solutions réseau pour Microsoft
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
ms.assetid: 1dc55f9f-5309-450f-acc3-b2b4119c8be3
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur les solutions réseau pour Microsoft.
ms.openlocfilehash: f990e4311ef88022d7fec2e1b7c90b3d8d035448
ms.sourcegitcommit: c7f11d851073ef14a69669f6c8b7e0c11e4bb7a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "43939142"
---
# <a name="create-dns-records-at-network-solutions-for-microsoft"></a><span data-ttu-id="84a4d-103">Créer des enregistrements DNS sur les solutions réseau pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="84a4d-103">Create DNS records at Network Solutions for Microsoft</span></span>

 <span data-ttu-id="84a4d-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="84a4d-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="84a4d-105">Si Network Solutions est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="84a4d-105">If Network Solutions is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="84a4d-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="84a4d-106">These are the main records to add.</span></span> <span data-ttu-id="84a4d-107">Suivez les étapes ci-dessous ou [regardez la vidéo](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US)</span><span class="sxs-lookup"><span data-stu-id="84a4d-107">Follow the steps below or [watch the video](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span> 
  
- [<span data-ttu-id="84a4d-108">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="84a4d-108">Add a TXT record for verification</span></span>](#add-a-txt-record-for-verification)
    
- [<span data-ttu-id="84a4d-109">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="84a4d-109">Add an MX record so email for your domain will come to Microsoft</span></span>](#add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft)
    
- [<span data-ttu-id="84a4d-110">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="84a4d-110">Add the CNAME records that are required for Microsoft</span></span>](#add-the-cname-records-that-are-required-for-microsoft)
    
- [<span data-ttu-id="84a4d-111">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="84a4d-111">Add a TXT record for SPF to help prevent email spam</span></span>](#add-a-txt-record-for-spf-to-help-prevent-email-spam)
    
- [<span data-ttu-id="84a4d-112">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="84a4d-112">Add the two SRV records that are required for Microsoft</span></span>](#add-the-two-srv-records-that-are-required-for-microsoft)
    
<span data-ttu-id="84a4d-113">Une fois ces enregistrements ajoutés sur les solutions réseau, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="84a4d-113">After you add these records at Network Solutions, your domain will be set up to work with Microsoft services.</span></span>
  

  
> [!NOTE]
>  <span data-ttu-id="84a4d-p102">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="84a4d-p102">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="84a4d-117">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="84a4d-117">Add a TXT record for verification</span></span>
<span data-ttu-id="84a4d-118"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="84a4d-118"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="84a4d-p103">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="84a4d-p103">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="84a4d-p104">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="84a4d-p104">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
<span data-ttu-id="84a4d-123">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 0:47)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="84a4d-123">Follow the steps below or [watch the video (start at 0:47)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="84a4d-124">Pour commencer, accédez à la page de vos domaines sur Network Solutions à l'aide de [ce lien](https://www.networksolutions.com/manage-it).</span><span class="sxs-lookup"><span data-stu-id="84a4d-124">To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it).</span></span> <span data-ttu-id="84a4d-125">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="84a4d-125">You'll be prompted to log in.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="84a4d-126">Avant de cliquer sur le bouton de **connexion** , choisissez **gérer mes noms de domaine** dans la liste déroulante **se connecter à :** .</span><span class="sxs-lookup"><span data-stu-id="84a4d-126">Before you select the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list.</span></span> 
  
    ![Sélectionnez Manage My Domain Names (Gérer mes noms de domaine) et connectez-vous à Network Solutions](../../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. <span data-ttu-id="84a4d-128">Cochez la case située en regard du nom du domaine que vous modifiez.</span><span class="sxs-lookup"><span data-stu-id="84a4d-128">Select the check box next to the name of the domain that you are modifying.</span></span>
    
    ![Activez la case à cocher correspondant à votre domaine](../../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. <span data-ttu-id="84a4d-130">Sélectionnez **modifier DNS**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-130">Select **Edit DNS**.</span></span>
    
    ![Sélectionnez Modifier DNS](../../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. <span data-ttu-id="84a4d-132">Sélectionnez **gérer les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-132">Select **Manage Advanced DNS Records**.</span></span>
    
    <span data-ttu-id="84a4d-133">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="84a4d-133">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez gérer les enregistrements DNS avancés](../../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. <span data-ttu-id="84a4d-135">Faites défiler jusqu’à la section **texte (enregistrements TXT)** , puis sélectionnez **modifier les enregistrements TXT**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-135">Scroll down to the **Text (TXT Records)** section, and then select **Edit TXT Records**.</span></span>
    
    ![Sélectionnez modifier les enregistrements TXT](../../media/240a01d6-750a-4da6-8554-641b571e4b71.png)
  
6. <span data-ttu-id="84a4d-137">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="84a4d-137">In the boxes for the new record, type or copy and paste the values in the following table.</span></span>
    
    |<span data-ttu-id="84a4d-138">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-138">**Host**</span></span>|<span data-ttu-id="84a4d-139">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-139">**TTL**</span></span>|<span data-ttu-id="84a4d-140">**Text (Texte)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-140">**Text**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> <span data-ttu-id="84a4d-141">(The system will change this value to **@ (None)** when you save the record.)</span><span class="sxs-lookup"><span data-stu-id="84a4d-141">(The system will change this value to **@ (None)** when you save the record.)</span></span>  <br/> |<span data-ttu-id="84a4d-142">3600</span><span class="sxs-lookup"><span data-stu-id="84a4d-142">3600</span></span>  <br/> |<span data-ttu-id="84a4d-143">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="84a4d-143">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="84a4d-144">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="84a4d-144">**Note:** This is an example.</span></span> <span data-ttu-id="84a4d-145">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="84a4d-145">Use your specific **Destination or Points to Address** value here, from the table.</span></span>  [<span data-ttu-id="84a4d-146">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="84a4d-146">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)   |
       
    ![Tapez ou collez des valeurs dans les zones du nouvel enregistrement.](../../media/8a76daab-b6ff-4c82-ba68-192b24fbb934.png)
  
7. <span data-ttu-id="84a4d-148">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-148">Select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/89e7fb38-b4d9-4949-a1bb-d0dd10b361e0.png)
  
8. <span data-ttu-id="84a4d-150">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-150">Select **Save Changes**.</span></span>
    
    ![Sélectionnez Enregistrer les modifications.](../../media/bd4d7cd0-c8a3-497a-b080-cfd5a5c60dc5.png)
  
9. <span data-ttu-id="84a4d-152">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="84a4d-152">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="84a4d-153">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="84a4d-153">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="84a4d-154">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="84a4d-154">When Microsoft finds the correct TXT record, your domain is verified.</span></span>

1. <span data-ttu-id="84a4d-155">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="84a4d-155">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="84a4d-156">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="84a4d-156">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="84a4d-157">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-157">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="84a4d-158">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-158">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="84a4d-p107">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="84a4d-p107">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="84a4d-162">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="84a4d-162">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="84a4d-163"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="84a4d-163"><a name="BKMK_add_MX"> </a></span></span>

<span data-ttu-id="84a4d-164">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 3:51)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="84a4d-164">Follow the steps below or [watch the video (start at 3:51)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="84a4d-165">Pour commencer, accédez à la page de vos domaines sur Network Solutions à l'aide de [ce lien](https://www.networksolutions.com/manage-it).</span><span class="sxs-lookup"><span data-stu-id="84a4d-165">To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it).</span></span> <span data-ttu-id="84a4d-166">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="84a4d-166">You'll be prompted to log in.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="84a4d-167">Avant de cliquer sur le bouton de **connexion** , choisissez **gérer mes noms de domaine** dans la liste déroulante **se connecter à :** .</span><span class="sxs-lookup"><span data-stu-id="84a4d-167">Before you select the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list.</span></span> 
  
    ![Sélectionnez Manage My Domain Names (Gérer mes noms de domaine) et connectez-vous à Network Solutions](../../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. <span data-ttu-id="84a4d-169">Cochez la case située en regard du nom du domaine que vous modifiez.</span><span class="sxs-lookup"><span data-stu-id="84a4d-169">Select the check box next to the name of the domain that you are modifying.</span></span>
    
    ![Activez la case à cocher correspondant à votre domaine](../../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. <span data-ttu-id="84a4d-171">Sélectionnez **modifier DNS**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-171">Select **Edit DNS**.</span></span>
    
    ![Sélectionnez Modifier DNS](../../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. <span data-ttu-id="84a4d-173">Sélectionnez **gérer les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-173">Select **Manage Advanced DNS Records**.</span></span>
    
    <span data-ttu-id="84a4d-174">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="84a4d-174">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez gérer les enregistrements DNS avancés](../../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. <span data-ttu-id="84a4d-176">Faites défiler vers le bas jusqu’à la section **serveurs de messagerie (enregistrements MX)** , puis sélectionnez **modifier les enregistrements MX**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-176">Scroll down to the **Mail Servers (MX Records)** section, and then select **Edit MX Records**.</span></span>
    
    ![Sélectionnez modifier les enregistrements MX](../../media/74b4e412-9073-4d2d-8710-fe340b223798.png)
  
6. <span data-ttu-id="84a4d-178">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="84a4d-178">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="84a4d-179">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="84a4d-179">**Priority**</span></span>|<span data-ttu-id="84a4d-180">**TTL**</span><span class="sxs-lookup"><span data-stu-id="84a4d-180">**TTL**</span></span>|<span data-ttu-id="84a4d-181">**Mail Server (Serveur de courrier)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-181">**Mail Server**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="84a4d-182">10 </span><span class="sxs-lookup"><span data-stu-id="84a4d-182">10</span></span>  <br/> <span data-ttu-id="84a4d-183">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="84a4d-183">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> |<span data-ttu-id="84a4d-184">3600</span><span class="sxs-lookup"><span data-stu-id="84a4d-184">3600</span></span>  <br/> | <span data-ttu-id="84a4d-185">*\<clé_de_domaine\>*  .mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="84a4d-185">*\<domain-key\>*  .mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="84a4d-186">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-186">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="84a4d-187">**Remarque :** Obtenir votre \* \<clé\> de domaine\* à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="84a4d-187">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span> [<span data-ttu-id="84a4d-188">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="84a4d-188">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
       
    ![Tapez ou collez des valeurs dans les zones du nouvel enregistrement.](../../media/0bb96872-cc6e-4dfa-a649-fb7efbbf0012.png)
  
7. <span data-ttu-id="84a4d-190">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-190">Select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/963f758b-e79d-4452-8340-7eba8a3972c9.png)
  
8. <span data-ttu-id="84a4d-192">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-192">Select **Save Changes**.</span></span>
    
    ![Sélectionnez Enregistrer les modifications.](../../media/7c2f784a-6dee-4364-866c-ad7202ef1fc2.png)
  
9. <span data-ttu-id="84a4d-194">Si d'autres enregistrements MX sont répertoriés, supprimez-les individuellement en sélectionnant l'icône **Delete (Supprimer)** associée à chaque enregistrement.</span><span class="sxs-lookup"><span data-stu-id="84a4d-194">If there are any other MX records, delete all of them by selecting **Delete** for each record.</span></span> 
    
    ![Select the Delete check box for other MX records](../../media/709d6133-9f5d-490a-a91e-95e21ca94695.png)
  
10. <span data-ttu-id="84a4d-196">Lorsqu’elles sont toutes sélectionnées, sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-196">When they are all selected, select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/4710f988-0bbc-4ba7-bf31-ca2392b2900e.png)
  
11. <span data-ttu-id="84a4d-198">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-198">Select **Save Changes**.</span></span>
    
    ![Sélectionnez Enregistrer les modifications.](../../media/24432ec6-666b-4612-9488-37c06437959b.png)
  
## <a name="add-the-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="84a4d-200">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="84a4d-200">Add the CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="84a4d-201"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="84a4d-201"><a name="BKMK_add_CNAME"> </a></span></span>

<span data-ttu-id="84a4d-202">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 4:43)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="84a4d-202">Follow the steps below or [watch the video (start at 4:43)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="84a4d-203">Pour commencer, accédez à la page de vos domaines sur Network Solutions à l'aide de [ce lien](https://www.networksolutions.com/manage-it).</span><span class="sxs-lookup"><span data-stu-id="84a4d-203">To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it).</span></span> <span data-ttu-id="84a4d-204">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="84a4d-204">You'll be prompted to log in.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="84a4d-205">Avant de cliquer sur le bouton de **connexion** , choisissez **gérer mes noms de domaine** dans la liste déroulante **se connecter à :** .</span><span class="sxs-lookup"><span data-stu-id="84a4d-205">Before you select the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list.</span></span> 
  
    ![Sélectionnez Manage My Domain Names (Gérer mes noms de domaine) et connectez-vous à Network Solutions](../../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. <span data-ttu-id="84a4d-207">Cochez la case située en regard du nom du domaine que vous modifiez.</span><span class="sxs-lookup"><span data-stu-id="84a4d-207">Select the check box next to the name of the domain that you are modifying.</span></span>
    
    ![Activez la case à cocher correspondant à votre domaine](../../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. <span data-ttu-id="84a4d-209">Sélectionnez **modifier DNS**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-209">Select **Edit DNS**.</span></span>
    
    ![Sélectionnez Modifier DNS](../../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. <span data-ttu-id="84a4d-211">Sélectionnez **gérer les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-211">Select **Manage Advanced DNS Records**.</span></span>
    
    <span data-ttu-id="84a4d-212">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="84a4d-212">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez gérer les enregistrements DNS avancés](../../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. <span data-ttu-id="84a4d-214">Faites défiler jusqu’à la section **alias d’hôte (enregistrements CNAME)** , puis sélectionnez **modifier les enregistrements CNAME**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-214">Scroll down to the **Host Aliases (CNAME Records)** section, and then select **Edit CNAME Records**.</span></span>
    
    ![Sélectionnez modifier les enregistrements CNAMe sous alias d’hôte](../../media/2d0a4666-8d40-48f4-886c-64a5157baaf5.png)
  
6. <span data-ttu-id="84a4d-216">Dans les zones des quatre nouveaux enregistrements, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="84a4d-216">In the boxes for the four new records, type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="84a4d-217">**Alias (Alias)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-217">**Alias**</span></span>|<span data-ttu-id="84a4d-218">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-218">**TTL**</span></span>|<span data-ttu-id="84a4d-219">**Refers to Host Name (Fait référence au nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-219">**Refers to Host Name**</span></span>|<span data-ttu-id="84a4d-220">**Other Host (Autre hôte)          (sélectionnez la case d'option **Other Host (Autre hôte)**)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-220">**Other Host          (select the **Other Host** option button)**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="84a4d-221">autodiscover</span><span class="sxs-lookup"><span data-stu-id="84a4d-221">autodiscover</span></span>  <br/> |<span data-ttu-id="84a4d-222">3600</span><span class="sxs-lookup"><span data-stu-id="84a4d-222">3600</span></span>  <br/> |<span data-ttu-id="84a4d-223">(Aucun paramètre)</span><span class="sxs-lookup"><span data-stu-id="84a4d-223">(No setting)</span></span>  <br/> |<span data-ttu-id="84a4d-224">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="84a4d-224">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="84a4d-225">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-225">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="84a4d-226">sip</span><span class="sxs-lookup"><span data-stu-id="84a4d-226">sip</span></span>  <br/> |<span data-ttu-id="84a4d-227">3600</span><span class="sxs-lookup"><span data-stu-id="84a4d-227">3600</span></span>  <br/> |<span data-ttu-id="84a4d-228">(Aucun paramètre)</span><span class="sxs-lookup"><span data-stu-id="84a4d-228">(No setting)</span></span>  <br/> |<span data-ttu-id="84a4d-229">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="84a4d-229">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="84a4d-230">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-230">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="84a4d-231">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="84a4d-231">lyncdiscover</span></span>  <br/> |<span data-ttu-id="84a4d-232">3600</span><span class="sxs-lookup"><span data-stu-id="84a4d-232">3600</span></span>  <br/> |<span data-ttu-id="84a4d-233">(Aucun paramètre)</span><span class="sxs-lookup"><span data-stu-id="84a4d-233">(No setting)</span></span>  <br/> |<span data-ttu-id="84a4d-234">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="84a4d-234">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="84a4d-235">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-235">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="84a4d-236">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="84a4d-236">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="84a4d-237">3600</span><span class="sxs-lookup"><span data-stu-id="84a4d-237">3600</span></span>  <br/> |<span data-ttu-id="84a4d-238">(Aucun paramètre)</span><span class="sxs-lookup"><span data-stu-id="84a4d-238">(No setting)</span></span>  <br/> |<span data-ttu-id="84a4d-239">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="84a4d-239">enterpriseregistration.windows.net</span></span>  <br/> <span data-ttu-id="84a4d-240">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-240">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="84a4d-241">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="84a4d-241">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="84a4d-242">3600</span><span class="sxs-lookup"><span data-stu-id="84a4d-242">3600</span></span>  <br/> |<span data-ttu-id="84a4d-243">(Aucun paramètre)</span><span class="sxs-lookup"><span data-stu-id="84a4d-243">(No setting)</span></span>  <br/> |<span data-ttu-id="84a4d-244">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="84a4d-244">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> <span data-ttu-id="84a4d-245">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-245">**This value MUST end with a period (.)**</span></span> <br/> |
    
    ![Taper ou coller des valeurs pour les nouveaux enregistrements](../../media/5ce0b30c-b46c-4778-aa5a-fb5e2f0961c1.png)
  
7. <span data-ttu-id="84a4d-247">Une fois que vous avez ajouté tous les enregistrements CNAMe dont vous avez besoin, sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-247">When you have added all of the CNAME records that you need, select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/4978bd8b-f6a6-458d-9522-ad612b301c4a.png)
  
8. <span data-ttu-id="84a4d-249">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-249">Select **Save Changes**.</span></span>
    
    ![Sélectionnez Enregistrer les modifications.](../../media/f005c38a-0d8d-4c61-bec6-15e60c89aa5a.png)
  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="84a4d-251">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="84a4d-251">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="84a4d-252"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="84a4d-252"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="84a4d-253">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="84a4d-253">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="84a4d-254">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="84a4d-254">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="84a4d-255">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="84a4d-255">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="84a4d-256">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="84a4d-256">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
<span data-ttu-id="84a4d-257">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 5:35)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="84a4d-257">Follow the steps below or [watch the video (start at 5:35)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="84a4d-258">Pour commencer, accédez à la page de vos domaines sur Network Solutions à l'aide de [ce lien](https://www.networksolutions.com/manage-it).</span><span class="sxs-lookup"><span data-stu-id="84a4d-258">To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it).</span></span> <span data-ttu-id="84a4d-259">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="84a4d-259">You'll be prompted to log in.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="84a4d-260">Avant de cliquer sur le bouton de **connexion** , choisissez **gérer mes noms de domaine** dans la liste déroulante **se connecter à :** .</span><span class="sxs-lookup"><span data-stu-id="84a4d-260">Before you select the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list.</span></span> 
  
    ![Sélectionnez Manage My Domain Names (Gérer mes noms de domaine) et connectez-vous à Network Solutions](../../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. <span data-ttu-id="84a4d-262">Cochez la case située en regard du nom du domaine que vous modifiez.</span><span class="sxs-lookup"><span data-stu-id="84a4d-262">Select the check box next to the name of the domain that you are modifying.</span></span>
    
    ![Activez la case à cocher correspondant à votre domaine](../../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. <span data-ttu-id="84a4d-264">Sélectionnez **modifier DNS**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-264">Select **Edit DNS**.</span></span>
    
    ![Sélectionnez Modifier DNS](../../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. <span data-ttu-id="84a4d-266">Sélectionnez **gérer les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-266">Select **Manage Advanced DNS Records**.</span></span>
    
    <span data-ttu-id="84a4d-267">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="84a4d-267">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez gérer les enregistrements DNS avancés](../../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. <span data-ttu-id="84a4d-269">Faites défiler jusqu’à la section **texte (enregistrements TXT)** , puis sélectionnez **modifier les enregistrements TXT**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-269">Scroll down to the **Text (TXT Records)** section, and then select **Edit TXT Records**.</span></span>
    
    ![Sélectionnez modifier les enregistrements TXT sous texte](../../media/a69a2631-6da2-4e81-99ab-9a9ab9b30b07.png)
  
6. <span data-ttu-id="84a4d-271">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="84a4d-271">In the boxes for the new record, type or copy and paste the following values.</span></span>
    
    |<span data-ttu-id="84a4d-272">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-272">**Host**</span></span>|<span data-ttu-id="84a4d-273">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-273">**TTL**</span></span>|<span data-ttu-id="84a4d-274">**Text (Texte)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-274">**Text**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> <span data-ttu-id="84a4d-275">(The system will change this value to **@ (None)** when you save the record.)</span><span class="sxs-lookup"><span data-stu-id="84a4d-275">(The system will change this value to **@ (None)** when you save the record.)</span></span>  <br/> |<span data-ttu-id="84a4d-276">3600</span><span class="sxs-lookup"><span data-stu-id="84a4d-276">3600</span></span>  <br/> |<span data-ttu-id="84a4d-277">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="84a4d-277">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="84a4d-278">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="84a4d-278">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span> |
       
    ![Taper ou coller des valeurs pour le nouvel enregistrement](../../media/11564eca-e2ee-4f17-af2b-a00eb7c157db.png)
  
7. <span data-ttu-id="84a4d-280">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-280">Select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/482a8dae-0c79-47c4-8bd8-87965683de24.png)
  
8. <span data-ttu-id="84a4d-282">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-282">Select **Save Changes**.</span></span>
    
    ![Sélectionnez Enregistrer les modifications.](../../media/600b8c6d-184f-4213-a50e-8f119ebf3ff0.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="84a4d-284">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="84a4d-284">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="84a4d-285"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="84a4d-285"><a name="BKMK_add_SRV"> </a></span></span>

<span data-ttu-id="84a4d-286">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 6:18)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="84a4d-286">Follow the steps below or [watch the video (start at 6:18)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="84a4d-p113">Pour commencer, accédez à la page de vos domaines sur Network Solutions à l'aide de [ce lien](https://www.networksolutions.com/manage-it). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="84a4d-p113">To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it). You'll be prompted to log in.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="84a4d-289">Avant de cliquer sur le bouton de **connexion** , choisissez **gérer mes noms de domaine** dans la liste déroulante **se connecter à :** .</span><span class="sxs-lookup"><span data-stu-id="84a4d-289">Before you select the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list.</span></span> 
  
    ![Sélectionnez Manage My Domain Names (Gérer mes noms de domaine) et connectez-vous à Network Solutions](../../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. <span data-ttu-id="84a4d-291">Cochez la case située en regard du nom du domaine que vous modifiez.</span><span class="sxs-lookup"><span data-stu-id="84a4d-291">Select the check box next to the name of the domain that you are modifying.</span></span>
    
    ![Activez la case à cocher correspondant à votre domaine](../../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. <span data-ttu-id="84a4d-293">Sélectionnez **modifier DNS**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-293">Select **Edit DNS**.</span></span>
    
    ![Sélectionnez Modifier DNS](../../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. <span data-ttu-id="84a4d-295">Sélectionnez **gérer les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-295">Select **Manage Advanced DNS Records**.</span></span>
    
    <span data-ttu-id="84a4d-296">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="84a4d-296">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez gérer les enregistrements DNS avancés](../../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. <span data-ttu-id="84a4d-298">Faites défiler jusqu’à la section **service (enregistrements SRV)** , puis sélectionnez **modifier les enregistrements SRV**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-298">Scroll down to the **Service (SRV Records)** section, and then select **Edit SRV Records**.</span></span>
    
    ![Sélectionnez modifier les enregistrements SRV sous service.](../../media/9a9248ea-5de5-4e16-9364-f7600fa371f5.png)
  
6. <span data-ttu-id="84a4d-300">Dans les zones des deux nouveaux enregistrements, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="84a4d-300">In the boxes for the two new records, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="84a4d-301">(Sélectionnez les valeurs **Service (Service)** et **Protocol (Protocole)** dans les listes déroulantes.)</span><span class="sxs-lookup"><span data-stu-id="84a4d-301">(Choose the **Service** and **Protocol** values from the drop-down lists.)</span></span> 
    
    |<span data-ttu-id="84a4d-302">**Service (Service)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-302">**Service**</span></span>|<span data-ttu-id="84a4d-303">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-303">**Protocol**</span></span>|<span data-ttu-id="84a4d-304">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-304">**TTL**</span></span>|<span data-ttu-id="84a4d-305">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-305">**Priority**</span></span>|<span data-ttu-id="84a4d-306">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-306">**Weight**</span></span>|<span data-ttu-id="84a4d-307">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-307">**Port**</span></span>|<span data-ttu-id="84a4d-308">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-308">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="84a4d-309">_sip</span><span class="sxs-lookup"><span data-stu-id="84a4d-309">_sip</span></span>  <br/> |<span data-ttu-id="84a4d-310">_tls</span><span class="sxs-lookup"><span data-stu-id="84a4d-310">_tls</span></span>  <br/> |<span data-ttu-id="84a4d-311">3600</span><span class="sxs-lookup"><span data-stu-id="84a4d-311">3600</span></span>  <br/> |<span data-ttu-id="84a4d-312">100</span><span class="sxs-lookup"><span data-stu-id="84a4d-312">100</span></span>  <br/> |<span data-ttu-id="84a4d-313">0,1</span><span class="sxs-lookup"><span data-stu-id="84a4d-313">1</span></span>  <br/> |<span data-ttu-id="84a4d-314">443</span><span class="sxs-lookup"><span data-stu-id="84a4d-314">443</span></span>  <br/> |<span data-ttu-id="84a4d-315">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="84a4d-315">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="84a4d-316">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-316">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="84a4d-317">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="84a4d-317">_sipfederationtls</span></span>  <br/> |<span data-ttu-id="84a4d-318">_tcp</span><span class="sxs-lookup"><span data-stu-id="84a4d-318">_tcp</span></span>  <br/> |<span data-ttu-id="84a4d-319">3600</span><span class="sxs-lookup"><span data-stu-id="84a4d-319">3600</span></span>  <br/> |<span data-ttu-id="84a4d-320">100</span><span class="sxs-lookup"><span data-stu-id="84a4d-320">100</span></span>  <br/> |<span data-ttu-id="84a4d-321">0,1</span><span class="sxs-lookup"><span data-stu-id="84a4d-321">1</span></span>  <br/> |<span data-ttu-id="84a4d-322">5061</span><span class="sxs-lookup"><span data-stu-id="84a4d-322">5061</span></span>  <br/> |<span data-ttu-id="84a4d-323">sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="84a4d-323">sipfed.online.lync.com.</span></span>  <br/> <span data-ttu-id="84a4d-324">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="84a4d-324">**This value MUST end with a period (.)**</span></span> <br/> |
       
    ![Taper ou coller des valeurs pour les nouveaux enregistrements](../../media/86968d1c-8e43-4e61-aeaa-37fc7d7ef7a7.png)
  
7. <span data-ttu-id="84a4d-326">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-326">Select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/bfe2c778-5d2b-4bb6-a79d-c3ff9caf9e1e.png)
  
8. <span data-ttu-id="84a4d-328">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="84a4d-328">Select **Save Changes**.</span></span>
    
    ![Sélectionnez Enregistrer les modifications.](../../media/6d323126-0ebe-45ab-8567-c234711d84c7.png)
  
> [!NOTE]
>  <span data-ttu-id="84a4d-p114">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="84a4d-p114">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
