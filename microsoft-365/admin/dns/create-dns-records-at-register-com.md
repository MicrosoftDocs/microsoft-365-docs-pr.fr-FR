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
ms.openlocfilehash: 8badcff89b2a8d8cc9901ef4f10c0a6b31de13d7
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43629274"
---
# <a name="create-dns-records-at-registercom-for-microsoft"></a><span data-ttu-id="533ca-103">Créer des enregistrements DNS sur Register.com pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="533ca-103">Create DNS records at Register.com for Microsoft</span></span>

 <span data-ttu-id="533ca-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="533ca-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="533ca-105">Si Register.com est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="533ca-105">If Register.com is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="533ca-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="533ca-106">These are the main records to add.</span></span> <span data-ttu-id="533ca-107">Suivez les étapes ci-dessous ou [regardez la vidéo](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US)</span><span class="sxs-lookup"><span data-stu-id="533ca-107">Follow the steps below or [watch the video](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
- [<span data-ttu-id="533ca-108">Ajouter un enregistrement TXT auprès de Register.com pour vérifier que vous êtes propriétaire du domaine</span><span class="sxs-lookup"><span data-stu-id="533ca-108">Add a TXT record at Register.com to verify that you own the domain</span></span>](#add-a-txt-record-at-registercom-to-verify-that-you-own-the-domain)
    
- [<span data-ttu-id="533ca-109">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient envoyés à Microsoft</span><span class="sxs-lookup"><span data-stu-id="533ca-109">Add an MX record so email for your domain will come to Microsoft</span></span>](#add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft)
    
- [<span data-ttu-id="533ca-110">Ajouter les enregistrements CNAMe requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="533ca-110">Add the CNAME records that are required for Microsoft</span></span>](#add-the-cname-records-that-are-required-for-microsoft)
    
- [<span data-ttu-id="533ca-111">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="533ca-111">Add a TXT record for SPF to help prevent email spam</span></span>](#add-a-txt-record-for-spf-to-help-prevent-email-spam)

- [<span data-ttu-id="533ca-112">Ajouter les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="533ca-112">Add the two SRV records that are required for Microsoft</span></span>](#add-the-two-srv-records-that-are-required-for-microsoft)
    
<span data-ttu-id="533ca-113">Une fois ces enregistrements ajoutés sur Register.com, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="533ca-113">After you add these records at Register.com, your domain will be set up to work with Microsoft services.</span></span>
  
<span data-ttu-id="533ca-114">Pour en savoir plus sur l’hébergement Web et le DNS pour les sites Web avec Microsoft, consultez [la rubrique utiliser un site Web public avec Microsoft](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span><span class="sxs-lookup"><span data-stu-id="533ca-114">To learn about webhosting and DNS for websites with Microsoft, see [Use a public website with Microsoft](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span></span>
  
> [!NOTE]
> <span data-ttu-id="533ca-115">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="533ca-115">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="533ca-116">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="533ca-116">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="533ca-117">Si vous rencontrez des problèmes avec le flux de messagerie ou d’autres problèmes après avoir ajouté des enregistrements DNS, consultez [la rubrique Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="533ca-117">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-at-registercom-to-verify-that-you-own-the-domain"></a><span data-ttu-id="533ca-118">Ajouter un enregistrement TXT auprès de Register.com pour vérifier que vous êtes propriétaire du domaine</span><span class="sxs-lookup"><span data-stu-id="533ca-118">Add a TXT record at Register.com to verify that you own the domain</span></span>
<span data-ttu-id="533ca-119"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="533ca-119"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="533ca-120">Avant d’utiliser votre domaine avec Microsoft, vous devez vous assurer que vous en êtes propriétaire.</span><span class="sxs-lookup"><span data-stu-id="533ca-120">Before you use your domain with Microsoft, we have to make sure that you own it.</span></span> <span data-ttu-id="533ca-121">Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="533ca-121">Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="533ca-p104">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="533ca-p104">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
<span data-ttu-id="533ca-124">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 0:44)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="533ca-124">Follow the steps below or [watch the video (start at 0:44)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="533ca-125">Pour commencer, accédez à la page de vos domaines sur le site Register.com en utilisant [ce lien](https://www.register.com/myaccount/).</span><span class="sxs-lookup"><span data-stu-id="533ca-125">To get started, go to your domains page at Register.com by using [this link](https://www.register.com/myaccount/).</span></span> <span data-ttu-id="533ca-126">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="533ca-126">You'll be prompted to sign in.</span></span>
    
2. <span data-ttu-id="533ca-127">Sélectionnez **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="533ca-127">Select **Domains**.</span></span>
    
3. <span data-ttu-id="533ca-128">Sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="533ca-128">Select **Manage**.</span></span>
    
4. <span data-ttu-id="533ca-129">Recherchez la ligne qui contient le nom du domaine que vous souhaitez modifier ; puis, dans cette ligne, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="533ca-129">Find the row that contains the name of the domain that you want to modify; and then, in that row, select **Manage**.</span></span>
    
5. <span data-ttu-id="533ca-130">Faites défiler jusqu’à la section **paramètres techniques avancés** , puis sélectionnez **modifier les enregistrements TXT (SPF)**.</span><span class="sxs-lookup"><span data-stu-id="533ca-130">Scroll down to the **Advanced Technical Settings** section, and then select **Edit TXT Records (SPF)**.</span></span>
    
6. <span data-ttu-id="533ca-131">In the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="533ca-131">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    |||
    |:-----|:-----|
    |<span data-ttu-id="533ca-132">**Host Name**</span><span class="sxs-lookup"><span data-stu-id="533ca-132">**Host Name**</span></span> <br/> |<span data-ttu-id="533ca-133">**TXT Record**</span><span class="sxs-lookup"><span data-stu-id="533ca-133">**TXT Record**</span></span> <br/> |
    |@  <br/> |<span data-ttu-id="533ca-134">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="533ca-134">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="533ca-135">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="533ca-135">**Note:** This is an example.</span></span> <span data-ttu-id="533ca-136">Utilisez votre **adresse de destination ou de pointage** spécifique ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="533ca-136">Use your specific **Destination or Points to Address** value here, from the table.</span></span> [<span data-ttu-id="533ca-137">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="533ca-137">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
7. <span data-ttu-id="533ca-138">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="533ca-138">Select **Continue**.</span></span>
    
8. <span data-ttu-id="533ca-139">Sur la page suivante, sélectionnez de nouveau **continue (continuer** ) pour confirmer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="533ca-139">On the next page, select **Continue** again to confirm your changes.</span></span> 
    
9. <span data-ttu-id="533ca-140">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="533ca-140">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="533ca-141">À présent que vous avez ajouté l’enregistrement sur le site de votre bureau d’enregistrement de domaines, vous allez revenir à Microsoft et demander l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="533ca-141">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="533ca-142">Lorsque Microsoft trouve l’enregistrement TXT correct, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="533ca-142">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="533ca-143">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="533ca-143">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="533ca-144">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="533ca-144">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="533ca-145">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="533ca-145">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="533ca-146">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="533ca-146">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="533ca-147">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="533ca-147">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="533ca-148">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="533ca-148">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="533ca-149">Si vous rencontrez des problèmes avec le flux de messagerie ou d’autres problèmes après avoir ajouté des enregistrements DNS, consultez [la rubrique Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="533ca-149">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="533ca-150">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient envoyés à Microsoft</span><span class="sxs-lookup"><span data-stu-id="533ca-150">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="533ca-151"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="533ca-151"><a name="BKMK_add_MX"> </a></span></span>

<span data-ttu-id="533ca-152">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 3:32)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="533ca-152">Follow the steps below or [watch the video (start at 3:32)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="533ca-153">Pour commencer, accédez à la page de vos domaines sur le site Register.com en utilisant [ce lien](https://www.register.com/myaccount/).</span><span class="sxs-lookup"><span data-stu-id="533ca-153">To get started, go to your domains page at Register.com by using [this link](https://www.register.com/myaccount/).</span></span> <span data-ttu-id="533ca-154">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="533ca-154">You'll be prompted to sign in.</span></span>
    
2. <span data-ttu-id="533ca-155">Sélectionnez **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="533ca-155">Select **Domains**.</span></span>
    
3. <span data-ttu-id="533ca-156">Sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="533ca-156">Select **Manage**.</span></span>
    
4. <span data-ttu-id="533ca-157">Recherchez la ligne qui contient le nom du domaine que vous souhaitez modifier ; puis, dans cette ligne, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="533ca-157">Find the row that contains the name of the domain that you want to modify; and then, in that row, select **Manage**.</span></span>
    
5. <span data-ttu-id="533ca-158">Faites défiler jusqu’à la section **paramètres techniques avancés** , puis sélectionnez **modifier les enregistrements de serveur de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="533ca-158">Scroll to the **Advanced Technical Settings** section, and then select **Edit Mail Exchanger Records**.</span></span>
    
    ![Sélectionnez modifier les enregistrements de serveur de messagerie](../../media/366b96a1-9147-4bbb-9f8f-50856466cc61.png)
  
6. <span data-ttu-id="533ca-160">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="533ca-160">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="533ca-161">(Choisissez la valeur **Priority** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="533ca-161">(Choose the **Priority** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="533ca-162">\*\*\*\*Host Name (Nom d'hôte)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="533ca-162">\*\*\*\*Host Name\*\*\*\*</span></span>|<span data-ttu-id="533ca-163">\*\*\*\*Priority (Priorité)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="533ca-163">\*\*\*\*Priority\*\*\*\*</span></span>|<span data-ttu-id="533ca-164">\*\*\*\*Mail Server (Serveur de courrier)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="533ca-164">\*\*\*\*Mail Server\*\*\*\*</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="533ca-165">High</span><span class="sxs-lookup"><span data-stu-id="533ca-165">High</span></span>  <br/> <span data-ttu-id="533ca-166">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="533ca-166">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> | <span data-ttu-id="533ca-167">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="533ca-167">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/>  <br/><span data-ttu-id="533ca-168">**Remarque :** Obtenir votre \< *clé* \> de domaine à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="533ca-168">**Note:** Get your \<*domain-key*\> from your Microsoft account.</span></span> <br> [<span data-ttu-id="533ca-169">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="533ca-169">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Copiez et collez la valeur à partir du tableau](../../media/a1a15a14-c3dc-45dc-adcd-90fdb3f7455d.png)
  
7. <span data-ttu-id="533ca-171">Si d'autres enregistrements MX sont répertoriés dans la liste, sélectionnez-les individuellement pour les supprimer.</span><span class="sxs-lookup"><span data-stu-id="533ca-171">If there were any other MX records already listed, select each of those records to be deleted.</span></span>
    
    ![Select each record to delete](../../media/0708d03e-346f-4ae7-8cc4-01589efc00ce.png)
  
8. <span data-ttu-id="533ca-173">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="533ca-173">Select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/6ef6ce01-ce21-4e3c-8209-4aa9a3dd4b76.png)
  
9. <span data-ttu-id="533ca-175">Sur la page suivante, sélectionnez de nouveau **continue (continuer** ) pour confirmer et enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="533ca-175">On the next page, select **Continue** again to confirm and save your changes.</span></span> 
    
    ![Sélectionnez continuer](../../media/adba4a60-bf61-44fc-9ad9-360e66f8a2ee.png)
  
## <a name="add-the-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="533ca-177">Ajouter les enregistrements CNAMe requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="533ca-177">Add the CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="533ca-178"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="533ca-178"><a name="BKMK_add_CNAME"> </a></span></span>

<span data-ttu-id="533ca-179">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 4:23)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="533ca-179">Follow the steps below or [watch the video (start at 4:23)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="533ca-180">Pour commencer, accédez à la page de vos domaines sur le site Register.com en utilisant [ce lien](https://www.register.com/myaccount/).</span><span class="sxs-lookup"><span data-stu-id="533ca-180">To get started, go to your domains page at Register.com by using [this link](https://www.register.com/myaccount/).</span></span> <span data-ttu-id="533ca-181">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="533ca-181">You'll be prompted to sign in.</span></span>
    
2. <span data-ttu-id="533ca-182">Sélectionnez **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="533ca-182">Select **Domains**.</span></span>
    
3. <span data-ttu-id="533ca-183">Sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="533ca-183">Select **Manage**.</span></span>
    
4. <span data-ttu-id="533ca-184">Recherchez la ligne qui contient le nom du domaine que vous souhaitez modifier ; puis, dans cette ligne, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="533ca-184">Find the row that contains the name of the domain that you want to modify; and then, in that row, select **Manage**.</span></span>
    
5. <span data-ttu-id="533ca-185">Faites défiler jusqu’à la section **paramètres techniques avancés** , puis sélectionnez **modifier les alias de domaine**.</span><span class="sxs-lookup"><span data-stu-id="533ca-185">Scroll to the **Advanced Technical Settings** section, and then select **Edit Domain Aliases Records**.</span></span>
    
    ![Sélectionnez modifier les alias des alias de domaine.](../../media/9fbc31ed-d67c-4828-8bd4-b51068f1e0ca.png)
  
6. <span data-ttu-id="533ca-187">Sélectionnez **ajouter d’autres alias de domaine**.</span><span class="sxs-lookup"><span data-stu-id="533ca-187">Select **Add more domain aliases**.</span></span>
    
    ![Sélectionnez Ajouter d’autres alias de domaines.](../../media/b787505f-5566-4879-8552-13f9e89cbf6b.png)
  
7. <span data-ttu-id="533ca-189">Ajoutez les enregistrements CNAME nécessaires.</span><span class="sxs-lookup"><span data-stu-id="533ca-189">Add the required CNAME records.</span></span>
    
    <span data-ttu-id="533ca-190">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="533ca-190">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span>
    
    |<span data-ttu-id="533ca-191">\*\*\*\*First field (unlabeled) (Premier champ (sans étiquette))\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="533ca-191">\*\*\*\*First field (unlabeled)\*\*\*\*</span></span>|<span data-ttu-id="533ca-192">\*\*\*\*Points to (Destination)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="533ca-192">\*\*\*\*Points to\*\*\*\*</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="533ca-193">autodiscover</span><span class="sxs-lookup"><span data-stu-id="533ca-193">autodiscover</span></span>  <br/> |<span data-ttu-id="533ca-194">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="533ca-194">autodiscover.outlook.com</span></span>  <br/>  <br/> |
    |<span data-ttu-id="533ca-195">sip</span><span class="sxs-lookup"><span data-stu-id="533ca-195">sip</span></span>  <br/> |<span data-ttu-id="533ca-196">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="533ca-196">sipdir.online.lync.com</span></span>  <br/>  <br/> |
    |<span data-ttu-id="533ca-197">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="533ca-197">lyncdiscover</span></span>  <br/> |<span data-ttu-id="533ca-198">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="533ca-198">webdir.online.lync.com</span></span> <br/>  <br/> |
    |<span data-ttu-id="533ca-199">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="533ca-199">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="533ca-200">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="533ca-200">enterpriseregistration.windows.net</span></span>  <br/>  <br/> |
    |<span data-ttu-id="533ca-201">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="533ca-201">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="533ca-202">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="533ca-202">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/>  <br/> |
   
     ![Copiez et collez les valeurs DNS de la table.](../../media/0e2b36b2-8a0b-4019-addf-301763f9a626.png)
  
8. <span data-ttu-id="533ca-204">Une fois que vous avez ajouté tous les enregistrements CNAMe dont vous avez besoin, sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="533ca-204">When you have added all of the CNAME records that you need, select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/1942612b-338a-48fa-a45d-2d5434516723.png)
  
9. <span data-ttu-id="533ca-206">Sur la page suivante, sélectionnez de nouveau **continue (continuer** ) pour confirmer et enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="533ca-206">On the next page, select **Continue** again to confirm and save your changes.</span></span> 
    
    ![Sélectionnez continuer](../../media/3342b570-0633-49c5-9175-5cc8e4a67b53.png)
  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="533ca-208">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="533ca-208">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="533ca-209"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="533ca-209"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="533ca-210">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="533ca-210">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="533ca-211">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="533ca-211">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="533ca-212">Si vous disposez déjà d’un enregistrement SPF pour votre domaine, n’en créez pas pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="533ca-212">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="533ca-213">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un seul enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="533ca-213">Instead, add the required Microsoft values to the current record so that you have a single SPF record that includes both sets of values.</span></span>  
  
<span data-ttu-id="533ca-214">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 5:12)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="533ca-214">Follow the steps below or [watch the video (start at 5:12)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="533ca-215">Pour commencer, accédez à la page de vos domaines sur le site Register.com en utilisant [ce lien](https://www.register.com/myaccount/).</span><span class="sxs-lookup"><span data-stu-id="533ca-215">To get started, go to your domains page at Register.com by using [this link](https://www.register.com/myaccount/).</span></span> <span data-ttu-id="533ca-216">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="533ca-216">You'll be prompted to sign in.</span></span>
    
2. <span data-ttu-id="533ca-217">Sélectionnez **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="533ca-217">Select **Domains**.</span></span>
    
3. <span data-ttu-id="533ca-218">Sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="533ca-218">Select **Manage**.</span></span>
    
4. <span data-ttu-id="533ca-219">Recherchez la ligne qui contient le nom du domaine que vous souhaitez modifier ; puis, dans cette ligne, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="533ca-219">Find the row that contains the name of the domain that you want to modify; and then, in that row, select **Manage**.</span></span>
    
5. <span data-ttu-id="533ca-220">Faites défiler jusqu’à la section **paramètres techniques avancés** , puis sélectionnez **modifier les enregistrements TXT (SPF)**.</span><span class="sxs-lookup"><span data-stu-id="533ca-220">Scroll to the **Advanced Technical Settings** section, and then select **Edit TXT Records (SPF)**.</span></span>
    
    ![Sélectionnez modifier les enregistrements TXT (SPF)](../../media/c917577a-8b3a-4210-ab6e-776e84f926d0.png)
  
6. <span data-ttu-id="533ca-222">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="533ca-222">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="533ca-223">\*\*\*\*Host Name (Nom d'hôte)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="533ca-223">\*\*\*\*Host Name\*\*\*\*</span></span>|<span data-ttu-id="533ca-224">\*\*\*\*TXT Record (Enregistrement TXT)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="533ca-224">\*\*\*\*TXT Record\*\*\*\*</span></span>|
    |:-----|:-----|
    |@  <br/> |<span data-ttu-id="533ca-225">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="533ca-225">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="533ca-226">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="533ca-226">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>  |
   
     ![Copiez et collez les valeurs de la table.](../../media/b1dc5036-c13c-4306-b1e3-5a38a74643b7.png)
  
7. <span data-ttu-id="533ca-228">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="533ca-228">Select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/08250c98-1a86-48a8-ad94-f96cf338126b.png)
  
8. <span data-ttu-id="533ca-230">Sur la page suivante, sélectionnez de nouveau **continue (continuer** ) pour confirmer et enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="533ca-230">On the next page, select **Continue** again to confirm and save your changes.</span></span> 
    
    ![Sélectionnez continuer](../../media/56be3b0a-dc71-471c-9be3-6ab927296f67.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="533ca-232">Ajouter les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="533ca-232">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="533ca-233"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="533ca-233"><a name="BKMK_add_SRV"> </a></span></span>

<span data-ttu-id="533ca-234">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 5:55)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="533ca-234">Follow the steps below or [watch the video (start at 5:55)](https://support.office.com/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="533ca-p112">Pour commencer, accédez à la page de vos domaines sur le site Register.com en utilisant [ce lien](https://www.register.com/myaccount/). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="533ca-p112">To get started, go to your domains page at Register.com by using [this link](https://www.register.com/myaccount/). You'll be prompted to sign in.</span></span>
    
2. <span data-ttu-id="533ca-237">Sélectionnez **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="533ca-237">Select **Domains**.</span></span>
    
3. <span data-ttu-id="533ca-238">Sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="533ca-238">Select **Manage**.</span></span>
    
4. <span data-ttu-id="533ca-239">Recherchez la ligne qui contient le nom du domaine que vous souhaitez modifier ; puis, dans cette ligne, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="533ca-239">Find the row that contains the name of the domain that you want to modify; and then, in that row, select **Manage**.</span></span>
    
5. <span data-ttu-id="533ca-240">Faites défiler jusqu’à la section **paramètres techniques avancés** , puis sélectionnez **modifier les enregistrements SRV**.</span><span class="sxs-lookup"><span data-stu-id="533ca-240">Scroll to the **Advanced Technical Settings** section, and then select **Edit SRV Records**.</span></span>
    
    ![Sélectionnez modifier les enregistrements SRV](../../media/73c149ae-f0d6-460e-880a-7e04a995acc3.png)
  
6. <span data-ttu-id="533ca-242">Ajoutez le premier des deux enregistrements SRV :</span><span class="sxs-lookup"><span data-stu-id="533ca-242">Add the first of the two SRV records:</span></span>
    
    <span data-ttu-id="533ca-243">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="533ca-243">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span>
    
    <span data-ttu-id="533ca-244">(Choisissez la valeur **Priority** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="533ca-244">(Choose the **Priority** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="533ca-245">\*\*\*\*Service (Service)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="533ca-245">\*\*\*\*Service\*\*\*\*</span></span>|<span data-ttu-id="533ca-246">\*\*\*\*Proto (Protocole)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="533ca-246">\*\*\*\*Proto\*\*\*\*</span></span>|<span data-ttu-id="533ca-247">\*\*\*\*Name (Nom)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="533ca-247">\*\*\*\*Name\*\*\*\*</span></span>|<span data-ttu-id="533ca-248">\*\*\*\*Priority (Priorité)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="533ca-248">\*\*\*\*Priority\*\*\*\*</span></span>|<span data-ttu-id="533ca-249">\*\*\*\*Weight (Poids)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="533ca-249">\*\*\*\*Weight\*\*\*\*</span></span>|<span data-ttu-id="533ca-250">\*\*\*\*Port (Port)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="533ca-250">\*\*\*\*Port\*\*\*\*</span></span>|<span data-ttu-id="533ca-251">\*\*\*\*Target (Cible)\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="533ca-251">\*\*\*\*Target\*\*\*\*</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="533ca-252">_sip</span><span class="sxs-lookup"><span data-stu-id="533ca-252">_sip</span></span>  <br/> |<span data-ttu-id="533ca-253">_tls</span><span class="sxs-lookup"><span data-stu-id="533ca-253">_tls</span></span>  <br/> |@  <br/> |<span data-ttu-id="533ca-254">High</span><span class="sxs-lookup"><span data-stu-id="533ca-254">High</span></span>  <br/> |<span data-ttu-id="533ca-255">0,1</span><span class="sxs-lookup"><span data-stu-id="533ca-255">1</span></span>  <br/> |<span data-ttu-id="533ca-256">443</span><span class="sxs-lookup"><span data-stu-id="533ca-256">443</span></span>  <br/> |<span data-ttu-id="533ca-257">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="533ca-257">sipdir.online.lync.com</span></span>  <br/>  <br/> |
    |<span data-ttu-id="533ca-258">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="533ca-258">_sipfederationtls</span></span>  <br/> |<span data-ttu-id="533ca-259">_tcp</span><span class="sxs-lookup"><span data-stu-id="533ca-259">_tcp</span></span>  <br/> |@  <br/> |<span data-ttu-id="533ca-260">High</span><span class="sxs-lookup"><span data-stu-id="533ca-260">High</span></span>  <br/> |<span data-ttu-id="533ca-261">0,1</span><span class="sxs-lookup"><span data-stu-id="533ca-261">1</span></span>  <br/> |<span data-ttu-id="533ca-262">5061</span><span class="sxs-lookup"><span data-stu-id="533ca-262">5061</span></span>  <br/> |<span data-ttu-id="533ca-263">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="533ca-263">sipfed.online.lync.com</span></span>  <br/>  <br/> |
   
    ![Copiez et collez les valeurs de la table.](../../media/71304c81-5845-4a8f-b969-d9efc8721184.png)
  
7. <span data-ttu-id="533ca-265">Sélectionnez **ajouter d’autres enregistrements SRV**.</span><span class="sxs-lookup"><span data-stu-id="533ca-265">Select **Add more SRV records**.</span></span>
    
    ![Sélectionnez Ajouter d’autres enregistrements SRV](../../media/823c6bd2-4af7-4079-bf8c-8d35a5c6730f.png)
  
8. <span data-ttu-id="533ca-267">Ajoutez le deuxième enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="533ca-267">Add the second SRV record:</span></span>
    
    <span data-ttu-id="533ca-268">Tapez ou copiez-collez les valeurs de la deuxième ligne du tableau ci-dessus dans les zones du deuxième enregistrement.</span><span class="sxs-lookup"><span data-stu-id="533ca-268">Type or copy and paste the values from the second row of the table above into the boxes for the second record.</span></span>
    
9. <span data-ttu-id="533ca-269">Une fois que vous avez ajouté les deux enregistrements SRV, sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="533ca-269">When you have added both of the SRV records, select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../../media/008b255a-42d3-442d-83ea-3ffcb7c8fc5d.png)
  
10. <span data-ttu-id="533ca-271">Sur la page suivante, sélectionnez de nouveau **continue (continuer** ) pour confirmer et enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="533ca-271">On the next page, select **Continue** again to confirm and save your changes.</span></span> 
    
    ![Sélectionnez continuer](../../media/b4166e3d-7e4b-41ef-b616-747e95aefc37.png)
  
> [!NOTE]
> <span data-ttu-id="533ca-273">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="533ca-273">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="533ca-274">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="533ca-274">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="533ca-275">Si vous rencontrez des problèmes avec le flux de messagerie ou d’autres problèmes après avoir ajouté des enregistrements DNS, consultez [la rubrique Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="533ca-275">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
