---
title: Créer des enregistrements DNS auprès de Network Solutions pour Office 365
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
ms.assetid: 1dc55f9f-5309-450f-acc3-b2b4119c8be3
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur les solutions réseau pour Office 365.
ms.openlocfilehash: f94ad49f443e609aa28d634d05604601c7d5e576
ms.sourcegitcommit: 812aab5f58eed4bf359faf0e99f7f876af5b1023
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/02/2020
ms.locfileid: "42348535"
---
# <a name="create-dns-records-at-network-solutions-for-office-365"></a><span data-ttu-id="52c57-103">Créer des enregistrements DNS auprès de Network Solutions pour Office 365</span><span class="sxs-lookup"><span data-stu-id="52c57-103">Create DNS records at Network Solutions for Office 365</span></span>

 <span data-ttu-id="52c57-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="52c57-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="52c57-105">Si Network Solutions est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="52c57-105">If Network Solutions is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="52c57-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="52c57-106">These are the main records to add.</span></span> <span data-ttu-id="52c57-107">Suivez les étapes ci-dessous ou [regardez la vidéo](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US)</span><span class="sxs-lookup"><span data-stu-id="52c57-107">Follow the steps below or [watch the video](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span> 
  
- [<span data-ttu-id="52c57-108">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="52c57-108">Add a TXT record for verification</span></span>](#add-a-txt-record-for-verification)
    
- [<span data-ttu-id="52c57-109">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="52c57-109">Add an MX record so email for your domain will come to Office 365</span></span>](#add-an-mx-record-so-email-for-your-domain-will-come-to-office-365)
    
- [<span data-ttu-id="52c57-110">Ajouter les enregistrements CNAME requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="52c57-110">Add the CNAME records that are required for Office 365</span></span>](#add-the-cname-records-that-are-required-for-office-365)
    
- [<span data-ttu-id="52c57-111">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="52c57-111">Add a TXT record for SPF to help prevent email spam</span></span>](#add-a-txt-record-for-spf-to-help-prevent-email-spam)
    
- [<span data-ttu-id="52c57-112">Ajouter les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="52c57-112">Add the two SRV records that are required for Office 365</span></span>](#add-the-two-srv-records-that-are-required-for-office-365)
    
<span data-ttu-id="52c57-113">Une fois ces enregistrements ajoutés sur Network Solutions, votre domaine est configuré pour utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="52c57-113">After you add these records at Network Solutions, your domain will be set up to work with Office 365 services.</span></span>
  
<span data-ttu-id="52c57-114">Pour en savoir plus sur l'hébergement web et le DNS pour les sites web avec Office 365, voir [Utiliser un site web public avec Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span><span class="sxs-lookup"><span data-stu-id="52c57-114">To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="52c57-p102">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="52c57-p102">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="52c57-118">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="52c57-118">Add a TXT record for verification</span></span>
<span data-ttu-id="52c57-119"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="52c57-119"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="52c57-p103">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="52c57-p103">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="52c57-p104">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="52c57-p104">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
<span data-ttu-id="52c57-124">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 0:47)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="52c57-124">Follow the steps below or [watch the video (start at 0:47)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="52c57-125">Pour commencer, accédez à la page de vos domaines sur Network Solutions à l'aide de [ce lien](https://www.networksolutions.com/manage-it).</span><span class="sxs-lookup"><span data-stu-id="52c57-125">To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it).</span></span> <span data-ttu-id="52c57-126">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="52c57-126">You'll be prompted to log in.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="52c57-127">Avant de cliquer sur le bouton de **connexion** , choisissez **gérer mes noms de domaine** dans la liste déroulante **se connecter à :** .</span><span class="sxs-lookup"><span data-stu-id="52c57-127">Before you select the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list.</span></span> 
  
    ![Sélectionnez Manage My Domain Names (Gérer mes noms de domaine) et connectez-vous à Network Solutions](../../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. <span data-ttu-id="52c57-129">Cochez la case située en regard du nom du domaine que vous modifiez.</span><span class="sxs-lookup"><span data-stu-id="52c57-129">Select the check box next to the name of the domain that you are modifying.</span></span>
    
    ![Activez la case à cocher correspondant à votre domaine](../../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. <span data-ttu-id="52c57-131">Sélectionnez **modifier DNS**.</span><span class="sxs-lookup"><span data-stu-id="52c57-131">Select **Edit DNS**.</span></span>
    
    ![Sélectionnez Modifier DNS](../../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. <span data-ttu-id="52c57-133">Sélectionnez **gérer les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="52c57-133">Select **Manage Advanced DNS Records**.</span></span>
    
    <span data-ttu-id="52c57-134">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="52c57-134">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez gérer les enregistrements DNS avancés](../../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. <span data-ttu-id="52c57-136">Faites défiler jusqu’à la section **texte (enregistrements TXT)** , puis sélectionnez **modifier les enregistrements TXT**.</span><span class="sxs-lookup"><span data-stu-id="52c57-136">Scroll down to the **Text (TXT Records)** section, and then select **Edit TXT Records**.</span></span>
    
    ![Sélectionnez modifier les enregistrements TXT](../../media/240a01d6-750a-4da6-8554-641b571e4b71.png)
  
6. <span data-ttu-id="52c57-138">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="52c57-138">In the boxes for the new record, type or copy and paste the values in the following table.</span></span>
    
    |<span data-ttu-id="52c57-139">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="52c57-139">**Host**</span></span>|<span data-ttu-id="52c57-140">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="52c57-140">**TTL**</span></span>|<span data-ttu-id="52c57-141">**Text (Texte)**</span><span class="sxs-lookup"><span data-stu-id="52c57-141">**Text**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> <span data-ttu-id="52c57-142">(The system will change this value to **@ (None)** when you save the record.)</span><span class="sxs-lookup"><span data-stu-id="52c57-142">(The system will change this value to **@ (None)** when you save the record.)</span></span>  <br/> |<span data-ttu-id="52c57-143">3600</span><span class="sxs-lookup"><span data-stu-id="52c57-143">3600</span></span>  <br/> |<span data-ttu-id="52c57-144">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="52c57-144">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="52c57-145">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="52c57-145">**Note:** This is an example.</span></span> <span data-ttu-id="52c57-146">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="52c57-146">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span>  [<span data-ttu-id="52c57-147">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="52c57-147">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)   |
       
    ![Tapez ou collez des valeurs dans les zones du nouvel enregistrement.](../../media/8a76daab-b6ff-4c82-ba68-192b24fbb934.png)
  
7. <span data-ttu-id="52c57-149">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="52c57-149">Select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/89e7fb38-b4d9-4949-a1bb-d0dd10b361e0.png)
  
8. <span data-ttu-id="52c57-151">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="52c57-151">Select **Save Changes**.</span></span>
    
    ![Sélectionnez Enregistrer les modifications.](../../media/bd4d7cd0-c8a3-497a-b080-cfd5a5c60dc5.png)
  
9. <span data-ttu-id="52c57-153">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="52c57-153">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="52c57-154">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Office 365 et demandez à Office 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="52c57-154">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="52c57-155">Lorsqu’Office 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="52c57-155">When Office 365 finds the correct TXT record, your domain is verified.</span></span>

1. <span data-ttu-id="52c57-156">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="52c57-156">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="52c57-157">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="52c57-157">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="52c57-158">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="52c57-158">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="52c57-159">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="52c57-159">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="52c57-p107">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="52c57-p107">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="52c57-163">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="52c57-163">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="52c57-164"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="52c57-164"><a name="BKMK_add_MX"> </a></span></span>

<span data-ttu-id="52c57-165">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 3:51)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="52c57-165">Follow the steps below or [watch the video (start at 3:51)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="52c57-166">Pour commencer, accédez à la page de vos domaines sur Network Solutions à l'aide de [ce lien](https://www.networksolutions.com/manage-it).</span><span class="sxs-lookup"><span data-stu-id="52c57-166">To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it).</span></span> <span data-ttu-id="52c57-167">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="52c57-167">You'll be prompted to log in.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="52c57-168">Avant de cliquer sur le bouton de **connexion** , choisissez **gérer mes noms de domaine** dans la liste déroulante **se connecter à :** .</span><span class="sxs-lookup"><span data-stu-id="52c57-168">Before you select the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list.</span></span> 
  
    ![Sélectionnez Manage My Domain Names (Gérer mes noms de domaine) et connectez-vous à Network Solutions](../../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. <span data-ttu-id="52c57-170">Cochez la case située en regard du nom du domaine que vous modifiez.</span><span class="sxs-lookup"><span data-stu-id="52c57-170">Select the check box next to the name of the domain that you are modifying.</span></span>
    
    ![Activez la case à cocher correspondant à votre domaine](../../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. <span data-ttu-id="52c57-172">Sélectionnez **modifier DNS**.</span><span class="sxs-lookup"><span data-stu-id="52c57-172">Select **Edit DNS**.</span></span>
    
    ![Sélectionnez Modifier DNS](../../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. <span data-ttu-id="52c57-174">Sélectionnez **gérer les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="52c57-174">Select **Manage Advanced DNS Records**.</span></span>
    
    <span data-ttu-id="52c57-175">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="52c57-175">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez gérer les enregistrements DNS avancés](../../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. <span data-ttu-id="52c57-177">Faites défiler vers le bas jusqu’à la section **serveurs de messagerie (enregistrements MX)** , puis sélectionnez **modifier les enregistrements MX**.</span><span class="sxs-lookup"><span data-stu-id="52c57-177">Scroll down to the **Mail Servers (MX Records)** section, and then select **Edit MX Records**.</span></span>
    
    ![Sélectionnez modifier les enregistrements MX](../../media/74b4e412-9073-4d2d-8710-fe340b223798.png)
  
6. <span data-ttu-id="52c57-179">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="52c57-179">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="52c57-180">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="52c57-180">**Priority**</span></span>|<span data-ttu-id="52c57-181">**TTL**</span><span class="sxs-lookup"><span data-stu-id="52c57-181">**TTL**</span></span>|<span data-ttu-id="52c57-182">**Mail Server (Serveur de courrier)**</span><span class="sxs-lookup"><span data-stu-id="52c57-182">**Mail Server**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="52c57-183">10 </span><span class="sxs-lookup"><span data-stu-id="52c57-183">10</span></span>  <br/> <span data-ttu-id="52c57-184">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="52c57-184">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> |<span data-ttu-id="52c57-185">3600</span><span class="sxs-lookup"><span data-stu-id="52c57-185">3600</span></span>  <br/> | <span data-ttu-id="52c57-186">*\<clé_de_domaine\>*  .mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="52c57-186">*\<domain-key\>*  .mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="52c57-187">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="52c57-187">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="52c57-188">**Remarque :** Obtenez votre \* \<clé\> de domaine\* à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="52c57-188">**Note:** Get your  *\<domain-key\>*  from your Office 365 account.</span></span> [<span data-ttu-id="52c57-189">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="52c57-189">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
       
    ![Tapez ou collez des valeurs dans les zones du nouvel enregistrement.](../../media/0bb96872-cc6e-4dfa-a649-fb7efbbf0012.png)
  
7. <span data-ttu-id="52c57-191">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="52c57-191">Select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/963f758b-e79d-4452-8340-7eba8a3972c9.png)
  
8. <span data-ttu-id="52c57-193">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="52c57-193">Select **Save Changes**.</span></span>
    
    ![Sélectionnez Enregistrer les modifications.](../../media/7c2f784a-6dee-4364-866c-ad7202ef1fc2.png)
  
9. <span data-ttu-id="52c57-195">Si d'autres enregistrements MX sont répertoriés, supprimez-les individuellement en sélectionnant l'icône **Delete (Supprimer)** associée à chaque enregistrement.</span><span class="sxs-lookup"><span data-stu-id="52c57-195">If there are any other MX records, delete all of them by selecting **Delete** for each record.</span></span> 
    
    ![Select the Delete check box for other MX records](../../media/709d6133-9f5d-490a-a91e-95e21ca94695.png)
  
10. <span data-ttu-id="52c57-197">Lorsqu’elles sont toutes sélectionnées, sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="52c57-197">When they are all selected, select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/4710f988-0bbc-4ba7-bf31-ca2392b2900e.png)
  
11. <span data-ttu-id="52c57-199">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="52c57-199">Select **Save Changes**.</span></span>
    
    ![Sélectionnez Enregistrer les modifications.](../../media/24432ec6-666b-4612-9488-37c06437959b.png)
  
## <a name="add-the-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="52c57-201">Ajouter les enregistrements CNAME requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="52c57-201">Add the CNAME records that are required for Office 365</span></span>
<span data-ttu-id="52c57-202"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="52c57-202"><a name="BKMK_add_CNAME"> </a></span></span>

<span data-ttu-id="52c57-203">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 4:43)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="52c57-203">Follow the steps below or [watch the video (start at 4:43)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="52c57-204">Pour commencer, accédez à la page de vos domaines sur Network Solutions à l'aide de [ce lien](https://www.networksolutions.com/manage-it).</span><span class="sxs-lookup"><span data-stu-id="52c57-204">To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it).</span></span> <span data-ttu-id="52c57-205">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="52c57-205">You'll be prompted to log in.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="52c57-206">Avant de cliquer sur le bouton de **connexion** , choisissez **gérer mes noms de domaine** dans la liste déroulante **se connecter à :** .</span><span class="sxs-lookup"><span data-stu-id="52c57-206">Before you select the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list.</span></span> 
  
    ![Sélectionnez Manage My Domain Names (Gérer mes noms de domaine) et connectez-vous à Network Solutions](../../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. <span data-ttu-id="52c57-208">Cochez la case située en regard du nom du domaine que vous modifiez.</span><span class="sxs-lookup"><span data-stu-id="52c57-208">Select the check box next to the name of the domain that you are modifying.</span></span>
    
    ![Activez la case à cocher correspondant à votre domaine](../../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. <span data-ttu-id="52c57-210">Sélectionnez **modifier DNS**.</span><span class="sxs-lookup"><span data-stu-id="52c57-210">Select **Edit DNS**.</span></span>
    
    ![Sélectionnez Modifier DNS](../../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. <span data-ttu-id="52c57-212">Sélectionnez **gérer les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="52c57-212">Select **Manage Advanced DNS Records**.</span></span>
    
    <span data-ttu-id="52c57-213">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="52c57-213">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez gérer les enregistrements DNS avancés](../../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. <span data-ttu-id="52c57-215">Faites défiler jusqu’à la section **alias d’hôte (enregistrements CNAME)** , puis sélectionnez **modifier les enregistrements CNAME**.</span><span class="sxs-lookup"><span data-stu-id="52c57-215">Scroll down to the **Host Aliases (CNAME Records)** section, and then select **Edit CNAME Records**.</span></span>
    
    ![Sélectionnez modifier les enregistrements CNAMe sous alias d’hôte](../../media/2d0a4666-8d40-48f4-886c-64a5157baaf5.png)
  
6. <span data-ttu-id="52c57-217">Dans les zones des quatre nouveaux enregistrements, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="52c57-217">In the boxes for the four new records, type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="52c57-218">**Alias (Alias)**</span><span class="sxs-lookup"><span data-stu-id="52c57-218">**Alias**</span></span>|<span data-ttu-id="52c57-219">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="52c57-219">**TTL**</span></span>|<span data-ttu-id="52c57-220">**Refers to Host Name (Fait référence au nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="52c57-220">**Refers to Host Name**</span></span>|<span data-ttu-id="52c57-221">**Other Host (Autre hôte)          (sélectionnez la case d'option **Other Host (Autre hôte)**)**</span><span class="sxs-lookup"><span data-stu-id="52c57-221">**Other Host          (select the **Other Host** option button)**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="52c57-222">autodiscover</span><span class="sxs-lookup"><span data-stu-id="52c57-222">autodiscover</span></span>  <br/> |<span data-ttu-id="52c57-223">3600</span><span class="sxs-lookup"><span data-stu-id="52c57-223">3600</span></span>  <br/> |<span data-ttu-id="52c57-224">(Aucun paramètre)</span><span class="sxs-lookup"><span data-stu-id="52c57-224">(No setting)</span></span>  <br/> |<span data-ttu-id="52c57-225">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="52c57-225">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="52c57-226">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="52c57-226">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="52c57-227">sip</span><span class="sxs-lookup"><span data-stu-id="52c57-227">sip</span></span>  <br/> |<span data-ttu-id="52c57-228">3600</span><span class="sxs-lookup"><span data-stu-id="52c57-228">3600</span></span>  <br/> |<span data-ttu-id="52c57-229">(Aucun paramètre)</span><span class="sxs-lookup"><span data-stu-id="52c57-229">(No setting)</span></span>  <br/> |<span data-ttu-id="52c57-230">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="52c57-230">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="52c57-231">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="52c57-231">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="52c57-232">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="52c57-232">lyncdiscover</span></span>  <br/> |<span data-ttu-id="52c57-233">3600</span><span class="sxs-lookup"><span data-stu-id="52c57-233">3600</span></span>  <br/> |<span data-ttu-id="52c57-234">(Aucun paramètre)</span><span class="sxs-lookup"><span data-stu-id="52c57-234">(No setting)</span></span>  <br/> |<span data-ttu-id="52c57-235">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="52c57-235">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="52c57-236">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="52c57-236">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="52c57-237">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="52c57-237">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="52c57-238">3600</span><span class="sxs-lookup"><span data-stu-id="52c57-238">3600</span></span>  <br/> |<span data-ttu-id="52c57-239">(Aucun paramètre)</span><span class="sxs-lookup"><span data-stu-id="52c57-239">(No setting)</span></span>  <br/> |<span data-ttu-id="52c57-240">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="52c57-240">enterpriseregistration.windows.net</span></span>  <br/> <span data-ttu-id="52c57-241">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="52c57-241">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="52c57-242">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="52c57-242">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="52c57-243">3600</span><span class="sxs-lookup"><span data-stu-id="52c57-243">3600</span></span>  <br/> |<span data-ttu-id="52c57-244">(Aucun paramètre)</span><span class="sxs-lookup"><span data-stu-id="52c57-244">(No setting)</span></span>  <br/> |<span data-ttu-id="52c57-245">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="52c57-245">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> <span data-ttu-id="52c57-246">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="52c57-246">**This value MUST end with a period (.)**</span></span> <br/> |
    
    ![Taper ou coller des valeurs pour les nouveaux enregistrements](../../media/5ce0b30c-b46c-4778-aa5a-fb5e2f0961c1.png)
  
7. <span data-ttu-id="52c57-248">Une fois que vous avez ajouté tous les enregistrements CNAMe dont vous avez besoin, sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="52c57-248">When you have added all of the CNAME records that you need, select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/4978bd8b-f6a6-458d-9522-ad612b301c4a.png)
  
8. <span data-ttu-id="52c57-250">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="52c57-250">Select **Save Changes**.</span></span>
    
    ![Sélectionnez Enregistrer les modifications.](../../media/f005c38a-0d8d-4c61-bec6-15e60c89aa5a.png)
  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="52c57-252">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="52c57-252">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="52c57-253"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="52c57-253"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="52c57-254">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="52c57-254">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="52c57-255">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="52c57-255">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="52c57-256">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="52c57-256">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="52c57-257">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="52c57-257">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
<span data-ttu-id="52c57-258">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 5:35)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="52c57-258">Follow the steps below or [watch the video (start at 5:35)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="52c57-259">Pour commencer, accédez à la page de vos domaines sur Network Solutions à l'aide de [ce lien](https://www.networksolutions.com/manage-it).</span><span class="sxs-lookup"><span data-stu-id="52c57-259">To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it).</span></span> <span data-ttu-id="52c57-260">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="52c57-260">You'll be prompted to log in.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="52c57-261">Avant de cliquer sur le bouton de **connexion** , choisissez **gérer mes noms de domaine** dans la liste déroulante **se connecter à :** .</span><span class="sxs-lookup"><span data-stu-id="52c57-261">Before you select the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list.</span></span> 
  
    ![Sélectionnez Manage My Domain Names (Gérer mes noms de domaine) et connectez-vous à Network Solutions](../../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. <span data-ttu-id="52c57-263">Cochez la case située en regard du nom du domaine que vous modifiez.</span><span class="sxs-lookup"><span data-stu-id="52c57-263">Select the check box next to the name of the domain that you are modifying.</span></span>
    
    ![Activez la case à cocher correspondant à votre domaine](../../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. <span data-ttu-id="52c57-265">Sélectionnez **modifier DNS**.</span><span class="sxs-lookup"><span data-stu-id="52c57-265">Select **Edit DNS**.</span></span>
    
    ![Sélectionnez Modifier DNS](../../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. <span data-ttu-id="52c57-267">Sélectionnez **gérer les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="52c57-267">Select **Manage Advanced DNS Records**.</span></span>
    
    <span data-ttu-id="52c57-268">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="52c57-268">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez gérer les enregistrements DNS avancés](../../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. <span data-ttu-id="52c57-270">Faites défiler jusqu’à la section **texte (enregistrements TXT)** , puis sélectionnez **modifier les enregistrements TXT**.</span><span class="sxs-lookup"><span data-stu-id="52c57-270">Scroll down to the **Text (TXT Records)** section, and then select **Edit TXT Records**.</span></span>
    
    ![Sélectionnez modifier les enregistrements TXT sous texte](../../media/a69a2631-6da2-4e81-99ab-9a9ab9b30b07.png)
  
6. <span data-ttu-id="52c57-272">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="52c57-272">In the boxes for the new record, type or copy and paste the following values.</span></span>
    
    |<span data-ttu-id="52c57-273">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="52c57-273">**Host**</span></span>|<span data-ttu-id="52c57-274">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="52c57-274">**TTL**</span></span>|<span data-ttu-id="52c57-275">**Text (Texte)**</span><span class="sxs-lookup"><span data-stu-id="52c57-275">**Text**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> <span data-ttu-id="52c57-276">(The system will change this value to **@ (None)** when you save the record.)</span><span class="sxs-lookup"><span data-stu-id="52c57-276">(The system will change this value to **@ (None)** when you save the record.)</span></span>  <br/> |<span data-ttu-id="52c57-277">3600</span><span class="sxs-lookup"><span data-stu-id="52c57-277">3600</span></span>  <br/> |<span data-ttu-id="52c57-278">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="52c57-278">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="52c57-279">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="52c57-279">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span> |
       
    ![Taper ou coller des valeurs pour le nouvel enregistrement](../../media/11564eca-e2ee-4f17-af2b-a00eb7c157db.png)
  
7. <span data-ttu-id="52c57-281">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="52c57-281">Select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/482a8dae-0c79-47c4-8bd8-87965683de24.png)
  
8. <span data-ttu-id="52c57-283">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="52c57-283">Select **Save Changes**.</span></span>
    
    ![Sélectionnez Enregistrer les modifications.](../../media/600b8c6d-184f-4213-a50e-8f119ebf3ff0.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="52c57-285">Ajoutez les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="52c57-285">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="52c57-286"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="52c57-286"><a name="BKMK_add_SRV"> </a></span></span>

<span data-ttu-id="52c57-287">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 6:18)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="52c57-287">Follow the steps below or [watch the video (start at 6:18)](https://support.office.com/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="52c57-p113">Pour commencer, accédez à la page de vos domaines sur Network Solutions à l'aide de [ce lien](https://www.networksolutions.com/manage-it). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="52c57-p113">To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it). You'll be prompted to log in.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="52c57-290">Avant de cliquer sur le bouton de **connexion** , choisissez **gérer mes noms de domaine** dans la liste déroulante **se connecter à :** .</span><span class="sxs-lookup"><span data-stu-id="52c57-290">Before you select the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list.</span></span> 
  
    ![Sélectionnez Manage My Domain Names (Gérer mes noms de domaine) et connectez-vous à Network Solutions](../../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. <span data-ttu-id="52c57-292">Cochez la case située en regard du nom du domaine que vous modifiez.</span><span class="sxs-lookup"><span data-stu-id="52c57-292">Select the check box next to the name of the domain that you are modifying.</span></span>
    
    ![Activez la case à cocher correspondant à votre domaine](../../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. <span data-ttu-id="52c57-294">Sélectionnez **modifier DNS**.</span><span class="sxs-lookup"><span data-stu-id="52c57-294">Select **Edit DNS**.</span></span>
    
    ![Sélectionnez Modifier DNS](../../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. <span data-ttu-id="52c57-296">Sélectionnez **gérer les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="52c57-296">Select **Manage Advanced DNS Records**.</span></span>
    
    <span data-ttu-id="52c57-297">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="52c57-297">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez gérer les enregistrements DNS avancés](../../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. <span data-ttu-id="52c57-299">Faites défiler jusqu’à la section **service (enregistrements SRV)** , puis sélectionnez **modifier les enregistrements SRV**.</span><span class="sxs-lookup"><span data-stu-id="52c57-299">Scroll down to the **Service (SRV Records)** section, and then select **Edit SRV Records**.</span></span>
    
    ![Sélectionnez modifier les enregistrements SRV sous service.](../../media/9a9248ea-5de5-4e16-9364-f7600fa371f5.png)
  
6. <span data-ttu-id="52c57-301">Dans les zones des deux nouveaux enregistrements, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="52c57-301">In the boxes for the two new records, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="52c57-302">(Sélectionnez les valeurs **Service (Service)** et **Protocol (Protocole)** dans les listes déroulantes.)</span><span class="sxs-lookup"><span data-stu-id="52c57-302">(Choose the **Service** and **Protocol** values from the drop-down lists.)</span></span> 
    
    |<span data-ttu-id="52c57-303">**Service (Service)**</span><span class="sxs-lookup"><span data-stu-id="52c57-303">**Service**</span></span>|<span data-ttu-id="52c57-304">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="52c57-304">**Protocol**</span></span>|<span data-ttu-id="52c57-305">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="52c57-305">**TTL**</span></span>|<span data-ttu-id="52c57-306">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="52c57-306">**Priority**</span></span>|<span data-ttu-id="52c57-307">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="52c57-307">**Weight**</span></span>|<span data-ttu-id="52c57-308">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="52c57-308">**Port**</span></span>|<span data-ttu-id="52c57-309">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="52c57-309">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="52c57-310">_sip</span><span class="sxs-lookup"><span data-stu-id="52c57-310">_sip</span></span>  <br/> |<span data-ttu-id="52c57-311">_tls</span><span class="sxs-lookup"><span data-stu-id="52c57-311">_tls</span></span>  <br/> |<span data-ttu-id="52c57-312">3600</span><span class="sxs-lookup"><span data-stu-id="52c57-312">3600</span></span>  <br/> |<span data-ttu-id="52c57-313">100</span><span class="sxs-lookup"><span data-stu-id="52c57-313">100</span></span>  <br/> |<span data-ttu-id="52c57-314">0,1</span><span class="sxs-lookup"><span data-stu-id="52c57-314">1</span></span>  <br/> |<span data-ttu-id="52c57-315">443</span><span class="sxs-lookup"><span data-stu-id="52c57-315">443</span></span>  <br/> |<span data-ttu-id="52c57-316">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="52c57-316">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="52c57-317">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="52c57-317">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="52c57-318">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="52c57-318">_sipfederationtls</span></span>  <br/> |<span data-ttu-id="52c57-319">_tcp</span><span class="sxs-lookup"><span data-stu-id="52c57-319">_tcp</span></span>  <br/> |<span data-ttu-id="52c57-320">3600</span><span class="sxs-lookup"><span data-stu-id="52c57-320">3600</span></span>  <br/> |<span data-ttu-id="52c57-321">100</span><span class="sxs-lookup"><span data-stu-id="52c57-321">100</span></span>  <br/> |<span data-ttu-id="52c57-322">0,1</span><span class="sxs-lookup"><span data-stu-id="52c57-322">1</span></span>  <br/> |<span data-ttu-id="52c57-323">5061</span><span class="sxs-lookup"><span data-stu-id="52c57-323">5061</span></span>  <br/> |<span data-ttu-id="52c57-324">sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="52c57-324">sipfed.online.lync.com.</span></span>  <br/> <span data-ttu-id="52c57-325">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="52c57-325">**This value MUST end with a period (.)**</span></span> <br/> |
       
    ![Taper ou coller des valeurs pour les nouveaux enregistrements](../../media/86968d1c-8e43-4e61-aeaa-37fc7d7ef7a7.png)
  
7. <span data-ttu-id="52c57-327">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="52c57-327">Select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/bfe2c778-5d2b-4bb6-a79d-c3ff9caf9e1e.png)
  
8. <span data-ttu-id="52c57-329">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="52c57-329">Select **Save Changes**.</span></span>
    
    ![Sélectionnez Enregistrer les modifications.](../../media/6d323126-0ebe-45ab-8567-c234711d84c7.png)
  
> [!NOTE]
>  <span data-ttu-id="52c57-p114">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="52c57-p114">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
