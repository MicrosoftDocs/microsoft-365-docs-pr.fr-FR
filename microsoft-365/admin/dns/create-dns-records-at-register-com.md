---
title: Créer des enregistrements DNS sur Register.com pour Microsoft
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
ms.assetid: 55bd8c38-3316-48ae-a368-4959b2c1684e
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur Register.com pour Microsoft.
ms.openlocfilehash: 125baf224cc9f3f21746a2f802b17f2572b65316
ms.sourcegitcommit: 5476c2578400894640ae74bfe8e93c3319f685bd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2020
ms.locfileid: "44048902"
---
# <a name="create-dns-records-at-registercom-for-microsoft"></a><span data-ttu-id="93bcc-103">Créer des enregistrements DNS sur Register.com pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="93bcc-103">Create DNS records at Register.com for Microsoft</span></span>

 <span data-ttu-id="93bcc-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="93bcc-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="93bcc-105">Si Register.com est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="93bcc-105">If Register.com is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="93bcc-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="93bcc-106">These are the main records to add.</span></span> <span data-ttu-id="93bcc-107">Suivez les étapes ci-dessous ou [regardez la vidéo](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US)</span><span class="sxs-lookup"><span data-stu-id="93bcc-107">Follow the steps below or [watch the video](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
- [<span data-ttu-id="93bcc-108">Ajouter un enregistrement TXT auprès de Register.com pour vérifier que vous êtes propriétaire du domaine</span><span class="sxs-lookup"><span data-stu-id="93bcc-108">Add a TXT record at Register.com to verify that you own the domain</span></span>](#add-a-txt-record-at-registercom-to-verify-that-you-own-the-domain)
    
- [<span data-ttu-id="93bcc-109">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="93bcc-109">Add an MX record so email for your domain will come to Microsoft</span></span>](#add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft)
    
- [<span data-ttu-id="93bcc-110">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="93bcc-110">Add the CNAME records that are required for Microsoft</span></span>](#add-the-cname-records-that-are-required-for-microsoft)
    
- [<span data-ttu-id="93bcc-111">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="93bcc-111">Add a TXT record for SPF to help prevent email spam</span></span>](#add-a-txt-record-for-spf-to-help-prevent-email-spam)

- [<span data-ttu-id="93bcc-112">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="93bcc-112">Add the two SRV records that are required for Microsoft</span></span>](#add-the-two-srv-records-that-are-required-for-microsoft)
    
<span data-ttu-id="93bcc-113">Une fois ces enregistrements ajoutés sur Register.com, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="93bcc-113">After you add these records at Register.com, your domain will be set up to work with Microsoft services.</span></span>
  

  
> [!NOTE]
> <span data-ttu-id="93bcc-114">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="93bcc-114">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="93bcc-115">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="93bcc-115">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="93bcc-116">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="93bcc-116">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-at-registercom-to-verify-that-you-own-the-domain"></a><span data-ttu-id="93bcc-117">Ajouter un enregistrement TXT auprès de Register.com pour vérifier que vous êtes propriétaire du domaine</span><span class="sxs-lookup"><span data-stu-id="93bcc-117">Add a TXT record at Register.com to verify that you own the domain</span></span>
<span data-ttu-id="93bcc-118"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="93bcc-118"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="93bcc-p103">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="93bcc-p103">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="93bcc-p104">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="93bcc-p104">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
<span data-ttu-id="93bcc-123">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 0:44)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="93bcc-123">Follow the steps below or [watch the video (start at 0:44)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="93bcc-124">Pour commencer, accédez à la page de vos domaines sur le site Register.com en utilisant [ce lien](https://www.register.com/myaccount/).</span><span class="sxs-lookup"><span data-stu-id="93bcc-124">To get started, go to your domains page at Register.com by using [this link](https://www.register.com/myaccount/).</span></span> <span data-ttu-id="93bcc-125">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="93bcc-125">You'll be prompted to sign in.</span></span>
    
2. <span data-ttu-id="93bcc-126">Sélectionnez **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-126">Select **Domains**.</span></span>
    
3. <span data-ttu-id="93bcc-127">Sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-127">Select **Manage**.</span></span>
    
4. <span data-ttu-id="93bcc-128">Recherchez la ligne qui contient le nom du domaine que vous souhaitez modifier ; puis, dans cette ligne, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-128">Find the row that contains the name of the domain that you want to modify; and then, in that row, select **Manage**.</span></span>
    
5. <span data-ttu-id="93bcc-129">Faites défiler jusqu’à la section **paramètres techniques avancés** , puis sélectionnez **modifier les enregistrements TXT (SPF)**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-129">Scroll down to the **Advanced Technical Settings** section, and then select **Edit TXT Records (SPF)**.</span></span>
    
6. <span data-ttu-id="93bcc-130">In the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="93bcc-130">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    |||
    |:-----|:-----|
    |<span data-ttu-id="93bcc-131">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="93bcc-131">**Host Name**</span></span> <br/> |<span data-ttu-id="93bcc-132">**TXT Record**</span><span class="sxs-lookup"><span data-stu-id="93bcc-132">**TXT Record**</span></span> <br/> |
    |@  <br/> |<span data-ttu-id="93bcc-133">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="93bcc-133">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="93bcc-134">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="93bcc-134">**Note:** This is an example.</span></span> <span data-ttu-id="93bcc-135">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="93bcc-135">Use your specific **Destination or Points to Address** value here, from the table.</span></span> [<span data-ttu-id="93bcc-136">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="93bcc-136">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
7. <span data-ttu-id="93bcc-137">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-137">Select **Continue**.</span></span>
    
8. <span data-ttu-id="93bcc-138">Sur la page suivante, sélectionnez de nouveau **continue (continuer** ) pour confirmer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="93bcc-138">On the next page, select **Continue** again to confirm your changes.</span></span> 
    
9. <span data-ttu-id="93bcc-139">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="93bcc-139">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="93bcc-140">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="93bcc-140">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="93bcc-141">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="93bcc-141">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="93bcc-142">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="93bcc-142">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="93bcc-143">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="93bcc-143">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="93bcc-144">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-144">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="93bcc-145">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-145">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="93bcc-146">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="93bcc-146">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="93bcc-147">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="93bcc-147">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="93bcc-148">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="93bcc-148">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="93bcc-149">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="93bcc-149">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="93bcc-150"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="93bcc-150"><a name="BKMK_add_MX"> </a></span></span>

<span data-ttu-id="93bcc-151">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 3:32)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="93bcc-151">Follow the steps below or [watch the video (start at 3:32)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="93bcc-152">Pour commencer, accédez à la page de vos domaines sur le site Register.com en utilisant [ce lien](https://www.register.com/myaccount/).</span><span class="sxs-lookup"><span data-stu-id="93bcc-152">To get started, go to your domains page at Register.com by using [this link](https://www.register.com/myaccount/).</span></span> <span data-ttu-id="93bcc-153">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="93bcc-153">You'll be prompted to sign in.</span></span>
    
2. <span data-ttu-id="93bcc-154">Sélectionnez **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-154">Select **Domains**.</span></span>
    
3. <span data-ttu-id="93bcc-155">Sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-155">Select **Manage**.</span></span>
    
4. <span data-ttu-id="93bcc-156">Recherchez la ligne qui contient le nom du domaine que vous souhaitez modifier ; puis, dans cette ligne, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-156">Find the row that contains the name of the domain that you want to modify; and then, in that row, select **Manage**.</span></span>
    
5. <span data-ttu-id="93bcc-157">Faites défiler jusqu’à la section **paramètres techniques avancés** , puis sélectionnez **modifier les enregistrements de serveur de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-157">Scroll to the **Advanced Technical Settings** section, and then select **Edit Mail Exchanger Records**.</span></span>
    
    ![Sélectionnez modifier les enregistrements de serveur de messagerie](../../media/366b96a1-9147-4bbb-9f8f-50856466cc61.png)
  
6. <span data-ttu-id="93bcc-159">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="93bcc-159">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="93bcc-160">(Choisissez la valeur **Priority** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="93bcc-160">(Choose the **Priority** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="93bcc-161">\*\*\*\*Host Name (Nom d'hôte)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93bcc-161">\*\*\*\*Host Name\*\*\*\*</span></span>|<span data-ttu-id="93bcc-162">\*\*\*\*Priority (Priorité)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93bcc-162">\*\*\*\*Priority\*\*\*\*</span></span>|<span data-ttu-id="93bcc-163">\*\*\*\*Mail Server (Serveur de courrier)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93bcc-163">\*\*\*\*Mail Server\*\*\*\*</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="93bcc-164">Élevé</span><span class="sxs-lookup"><span data-stu-id="93bcc-164">High</span></span>  <br/> <span data-ttu-id="93bcc-165">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span><span class="sxs-lookup"><span data-stu-id="93bcc-165">For more information about priority, see [What is MX priority?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span></span> <br/> | <span data-ttu-id="93bcc-166">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="93bcc-166">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/>  <br/><span data-ttu-id="93bcc-167">**Remarque :** Obtenez votre \<*clé de domaine*\> à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="93bcc-167">**Note:** Get your \<*domain-key*\> from your Microsoft account.</span></span> <br> [<span data-ttu-id="93bcc-168">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="93bcc-168">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Copiez et collez la valeur à partir du tableau](../../media/a1a15a14-c3dc-45dc-adcd-90fdb3f7455d.png)
  
7. <span data-ttu-id="93bcc-170">Si d'autres enregistrements MX sont répertoriés dans la liste, sélectionnez-les individuellement pour les supprimer.</span><span class="sxs-lookup"><span data-stu-id="93bcc-170">If there were any other MX records already listed, select each of those records to be deleted.</span></span>
    
    ![Select each record to delete](../../media/0708d03e-346f-4ae7-8cc4-01589efc00ce.png)
  
8. <span data-ttu-id="93bcc-172">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-172">Select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/6ef6ce01-ce21-4e3c-8209-4aa9a3dd4b76.png)
  
9. <span data-ttu-id="93bcc-174">Sur la page suivante, sélectionnez de nouveau **continue (continuer** ) pour confirmer et enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="93bcc-174">On the next page, select **Continue** again to confirm and save your changes.</span></span> 
    
    ![Sélectionnez continuer](../../media/adba4a60-bf61-44fc-9ad9-360e66f8a2ee.png)
  
## <a name="add-the-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="93bcc-176">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="93bcc-176">Add the CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="93bcc-177"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="93bcc-177"><a name="BKMK_add_CNAME"> </a></span></span>

<span data-ttu-id="93bcc-178">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 4:23)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="93bcc-178">Follow the steps below or [watch the video (start at 4:23)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="93bcc-179">Pour commencer, accédez à la page de vos domaines sur le site Register.com en utilisant [ce lien](https://www.register.com/myaccount/).</span><span class="sxs-lookup"><span data-stu-id="93bcc-179">To get started, go to your domains page at Register.com by using [this link](https://www.register.com/myaccount/).</span></span> <span data-ttu-id="93bcc-180">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="93bcc-180">You'll be prompted to sign in.</span></span>
    
2. <span data-ttu-id="93bcc-181">Sélectionnez **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-181">Select **Domains**.</span></span>
    
3. <span data-ttu-id="93bcc-182">Sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-182">Select **Manage**.</span></span>
    
4. <span data-ttu-id="93bcc-183">Recherchez la ligne qui contient le nom du domaine que vous souhaitez modifier ; puis, dans cette ligne, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-183">Find the row that contains the name of the domain that you want to modify; and then, in that row, select **Manage**.</span></span>
    
5. <span data-ttu-id="93bcc-184">Faites défiler jusqu’à la section **paramètres techniques avancés** , puis sélectionnez **modifier les alias de domaine**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-184">Scroll to the **Advanced Technical Settings** section, and then select **Edit Domain Aliases Records**.</span></span>
    
    ![Sélectionnez modifier les alias des alias de domaine.](../../media/9fbc31ed-d67c-4828-8bd4-b51068f1e0ca.png)
  
6. <span data-ttu-id="93bcc-186">Sélectionnez **ajouter d’autres alias de domaine**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-186">Select **Add more domain aliases**.</span></span>
    
    ![Sélectionnez Ajouter d’autres alias de domaines.](../../media/b787505f-5566-4879-8552-13f9e89cbf6b.png)
  
7. <span data-ttu-id="93bcc-188">Ajoutez les enregistrements CNAME nécessaires.</span><span class="sxs-lookup"><span data-stu-id="93bcc-188">Add the required CNAME records.</span></span>
    
    <span data-ttu-id="93bcc-189">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="93bcc-189">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span>
    
    |<span data-ttu-id="93bcc-190">\*\*\*\*First field (unlabeled) (Premier champ (sans étiquette))\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93bcc-190">\*\*\*\*First field (unlabeled)\*\*\*\*</span></span>|<span data-ttu-id="93bcc-191">\*\*\*\*Points to (Destination)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93bcc-191">\*\*\*\*Points to\*\*\*\*</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="93bcc-192">autodiscover</span><span class="sxs-lookup"><span data-stu-id="93bcc-192">autodiscover</span></span>  <br/> |<span data-ttu-id="93bcc-193">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="93bcc-193">autodiscover.outlook.com</span></span>  <br/>  <br/> |
    |<span data-ttu-id="93bcc-194">sip</span><span class="sxs-lookup"><span data-stu-id="93bcc-194">sip</span></span>  <br/> |<span data-ttu-id="93bcc-195">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="93bcc-195">sipdir.online.lync.com</span></span>  <br/>  <br/> |
    |<span data-ttu-id="93bcc-196">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="93bcc-196">lyncdiscover</span></span>  <br/> |<span data-ttu-id="93bcc-197">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="93bcc-197">webdir.online.lync.com</span></span> <br/>  <br/> |
    |<span data-ttu-id="93bcc-198">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="93bcc-198">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="93bcc-199">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="93bcc-199">enterpriseregistration.windows.net</span></span>  <br/>  <br/> |
    |<span data-ttu-id="93bcc-200">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="93bcc-200">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="93bcc-201">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="93bcc-201">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/>  <br/> |
   
     ![Copiez et collez les valeurs DNS de la table.](../../media/0e2b36b2-8a0b-4019-addf-301763f9a626.png)
  
8. <span data-ttu-id="93bcc-203">Une fois que vous avez ajouté tous les enregistrements CNAMe dont vous avez besoin, sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-203">When you have added all of the CNAME records that you need, select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/1942612b-338a-48fa-a45d-2d5434516723.png)
  
9. <span data-ttu-id="93bcc-205">Sur la page suivante, sélectionnez de nouveau **continue (continuer** ) pour confirmer et enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="93bcc-205">On the next page, select **Continue** again to confirm and save your changes.</span></span> 
    
    ![Sélectionnez continuer](../../media/3342b570-0633-49c5-9175-5cc8e4a67b53.png)
  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="93bcc-207">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="93bcc-207">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="93bcc-208"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="93bcc-208"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="93bcc-209">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="93bcc-209">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="93bcc-210">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="93bcc-210">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="93bcc-211">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="93bcc-211">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="93bcc-212">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel de manière à n’avoir qu’un seul enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="93bcc-212">Instead, add the required Microsoft values to the current record so that you have a single SPF record that includes both sets of values.</span></span>  
  
<span data-ttu-id="93bcc-213">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 5:12)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="93bcc-213">Follow the steps below or [watch the video (start at 5:12)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="93bcc-214">Pour commencer, accédez à la page de vos domaines sur le site Register.com en utilisant [ce lien](https://www.register.com/myaccount/).</span><span class="sxs-lookup"><span data-stu-id="93bcc-214">To get started, go to your domains page at Register.com by using [this link](https://www.register.com/myaccount/).</span></span> <span data-ttu-id="93bcc-215">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="93bcc-215">You'll be prompted to sign in.</span></span>
    
2. <span data-ttu-id="93bcc-216">Sélectionnez **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-216">Select **Domains**.</span></span>
    
3. <span data-ttu-id="93bcc-217">Sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-217">Select **Manage**.</span></span>
    
4. <span data-ttu-id="93bcc-218">Recherchez la ligne qui contient le nom du domaine que vous souhaitez modifier ; puis, dans cette ligne, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-218">Find the row that contains the name of the domain that you want to modify; and then, in that row, select **Manage**.</span></span>
    
5. <span data-ttu-id="93bcc-219">Faites défiler jusqu’à la section **paramètres techniques avancés** , puis sélectionnez **modifier les enregistrements TXT (SPF)**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-219">Scroll to the **Advanced Technical Settings** section, and then select **Edit TXT Records (SPF)**.</span></span>
    
    ![Sélectionnez modifier les enregistrements TXT (SPF)](../../media/c917577a-8b3a-4210-ab6e-776e84f926d0.png)
  
6. <span data-ttu-id="93bcc-221">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="93bcc-221">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="93bcc-222">\*\*\*\*Host Name (Nom d'hôte)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93bcc-222">\*\*\*\*Host Name\*\*\*\*</span></span>|<span data-ttu-id="93bcc-223">\*\*\*\*TXT Record (Enregistrement TXT)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93bcc-223">\*\*\*\*TXT Record\*\*\*\*</span></span>|
    |:-----|:-----|
    |@  <br/> |<span data-ttu-id="93bcc-224">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="93bcc-224">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="93bcc-225">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="93bcc-225">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>  |
   
     ![Copiez et collez les valeurs de la table.](../../media/b1dc5036-c13c-4306-b1e3-5a38a74643b7.png)
  
7. <span data-ttu-id="93bcc-227">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-227">Select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/08250c98-1a86-48a8-ad94-f96cf338126b.png)
  
8. <span data-ttu-id="93bcc-229">Sur la page suivante, sélectionnez de nouveau **continue (continuer** ) pour confirmer et enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="93bcc-229">On the next page, select **Continue** again to confirm and save your changes.</span></span> 
    
    ![Sélectionnez continuer](../../media/56be3b0a-dc71-471c-9be3-6ab927296f67.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="93bcc-231">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="93bcc-231">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="93bcc-232"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="93bcc-232"><a name="BKMK_add_SRV"> </a></span></span>

<span data-ttu-id="93bcc-233">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 5:55)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="93bcc-233">Follow the steps below or [watch the video (start at 5:55)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="93bcc-p112">Pour commencer, accédez à la page de vos domaines sur le site Register.com en utilisant [ce lien](https://www.register.com/myaccount/). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="93bcc-p112">To get started, go to your domains page at Register.com by using [this link](https://www.register.com/myaccount/). You'll be prompted to sign in.</span></span>
    
2. <span data-ttu-id="93bcc-236">Sélectionnez **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-236">Select **Domains**.</span></span>
    
3. <span data-ttu-id="93bcc-237">Sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-237">Select **Manage**.</span></span>
    
4. <span data-ttu-id="93bcc-238">Recherchez la ligne qui contient le nom du domaine que vous souhaitez modifier ; puis, dans cette ligne, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-238">Find the row that contains the name of the domain that you want to modify; and then, in that row, select **Manage**.</span></span>
    
5. <span data-ttu-id="93bcc-239">Faites défiler jusqu’à la section **paramètres techniques avancés** , puis sélectionnez **modifier les enregistrements SRV**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-239">Scroll to the **Advanced Technical Settings** section, and then select **Edit SRV Records**.</span></span>
    
    ![Sélectionnez modifier les enregistrements SRV](../../media/73c149ae-f0d6-460e-880a-7e04a995acc3.png)
  
6. <span data-ttu-id="93bcc-241">Ajoutez le premier des deux enregistrements SRV :</span><span class="sxs-lookup"><span data-stu-id="93bcc-241">Add the first of the two SRV records:</span></span>
    
    <span data-ttu-id="93bcc-242">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="93bcc-242">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span>
    
    <span data-ttu-id="93bcc-243">(Choisissez la valeur **Priority** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="93bcc-243">(Choose the **Priority** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="93bcc-244">\*\*\*\*Service (Service)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93bcc-244">\*\*\*\*Service\*\*\*\*</span></span>|<span data-ttu-id="93bcc-245">\*\*\*\*Proto (Protocole)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93bcc-245">\*\*\*\*Proto\*\*\*\*</span></span>|<span data-ttu-id="93bcc-246">\*\*\*\*Name (Nom)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93bcc-246">\*\*\*\*Name\*\*\*\*</span></span>|<span data-ttu-id="93bcc-247">\*\*\*\*Priority (Priorité)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93bcc-247">\*\*\*\*Priority\*\*\*\*</span></span>|<span data-ttu-id="93bcc-248">\*\*\*\*Weight (Poids)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93bcc-248">\*\*\*\*Weight\*\*\*\*</span></span>|<span data-ttu-id="93bcc-249">\*\*\*\*Port (Port)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93bcc-249">\*\*\*\*Port\*\*\*\*</span></span>|<span data-ttu-id="93bcc-250">\*\*\*\*Target (Cible)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93bcc-250">\*\*\*\*Target\*\*\*\*</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="93bcc-251">_sip</span><span class="sxs-lookup"><span data-stu-id="93bcc-251">_sip</span></span>  <br/> |<span data-ttu-id="93bcc-252">_tls</span><span class="sxs-lookup"><span data-stu-id="93bcc-252">_tls</span></span>  <br/> |@  <br/> |<span data-ttu-id="93bcc-253">High</span><span class="sxs-lookup"><span data-stu-id="93bcc-253">High</span></span>  <br/> |<span data-ttu-id="93bcc-254">0,1</span><span class="sxs-lookup"><span data-stu-id="93bcc-254">1</span></span>  <br/> |<span data-ttu-id="93bcc-255">443</span><span class="sxs-lookup"><span data-stu-id="93bcc-255">443</span></span>  <br/> |<span data-ttu-id="93bcc-256">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="93bcc-256">sipdir.online.lync.com</span></span>  <br/>  <br/> |
    |<span data-ttu-id="93bcc-257">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="93bcc-257">_sipfederationtls</span></span>  <br/> |<span data-ttu-id="93bcc-258">_tcp</span><span class="sxs-lookup"><span data-stu-id="93bcc-258">_tcp</span></span>  <br/> |@  <br/> |<span data-ttu-id="93bcc-259">High</span><span class="sxs-lookup"><span data-stu-id="93bcc-259">High</span></span>  <br/> |<span data-ttu-id="93bcc-260">0,1</span><span class="sxs-lookup"><span data-stu-id="93bcc-260">1</span></span>  <br/> |<span data-ttu-id="93bcc-261">5061</span><span class="sxs-lookup"><span data-stu-id="93bcc-261">5061</span></span>  <br/> |<span data-ttu-id="93bcc-262">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="93bcc-262">sipfed.online.lync.com</span></span>  <br/>  <br/> |
   
    ![Copiez et collez les valeurs de la table.](../../media/71304c81-5845-4a8f-b969-d9efc8721184.png)
  
7. <span data-ttu-id="93bcc-264">Sélectionnez **ajouter d’autres enregistrements SRV**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-264">Select **Add more SRV records**.</span></span>
    
    ![Sélectionnez Ajouter d’autres enregistrements SRV](../../media/823c6bd2-4af7-4079-bf8c-8d35a5c6730f.png)
  
8. <span data-ttu-id="93bcc-266">Ajoutez le deuxième enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="93bcc-266">Add the second SRV record:</span></span>
    
    <span data-ttu-id="93bcc-267">Tapez ou copiez-collez les valeurs de la deuxième ligne du tableau ci-dessus dans les zones du deuxième enregistrement.</span><span class="sxs-lookup"><span data-stu-id="93bcc-267">Type or copy and paste the values from the second row of the table above into the boxes for the second record.</span></span>
    
9. <span data-ttu-id="93bcc-268">Une fois que vous avez ajouté les deux enregistrements SRV, sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="93bcc-268">When you have added both of the SRV records, select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/008b255a-42d3-442d-83ea-3ffcb7c8fc5d.png)
  
10. <span data-ttu-id="93bcc-270">Sur la page suivante, sélectionnez de nouveau **continue (continuer** ) pour confirmer et enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="93bcc-270">On the next page, select **Continue** again to confirm and save your changes.</span></span> 
    
    ![Sélectionnez continuer](../../media/b4166e3d-7e4b-41ef-b616-747e95aefc37.png)
  
> [!NOTE]
> <span data-ttu-id="93bcc-272">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="93bcc-272">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="93bcc-273">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="93bcc-273">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="93bcc-274">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="93bcc-274">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
