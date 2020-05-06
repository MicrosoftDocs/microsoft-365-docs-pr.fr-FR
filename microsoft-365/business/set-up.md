---
title: Configurer Microsoft 365 Business Premium
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
f1_keywords:
- O365E_M365SetupBanner
- BCS365_M365SetupBanner
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
- TRN_SMB
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MSB365
- OKR_SMB_M365
- TRN_M365B
- OKR_SMB_Videos
- seo-marvel-mar
search.appverid:
- BCS160
- MET150
ms.assetid: 6e7a2dfd-8ec4-4eb7-8390-3ee103e5fece
description: Découvrez les étapes de configuration de Microsoft 365 Business Premium, y compris l’ajout d’un domaine et d’utilisateurs, la configuration des stratégies de sécurité, et bien plus encore.
ms.openlocfilehash: cfc8523fe88ebca6b8c03db0ad0f6caeba662923
ms.sourcegitcommit: 5476c2578400894640ae74bfe8e93c3319f685bd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2020
ms.locfileid: "44048036"
---
# <a name="set-up-microsoft-365-business-premium-in-the-setup-wizard"></a><span data-ttu-id="65154-103">Configurer Microsoft 365 Business Premium dans l’Assistant Installation</span><span class="sxs-lookup"><span data-stu-id="65154-103">Set up Microsoft 365 Business Premium in the setup wizard</span></span>

<span data-ttu-id="65154-104">Regardez cette vidéo pour obtenir une vue d’ensemble de l’installation de Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="65154-104">Watch this video for an overview of Microsoft 365 Business Premium setup.</span></span><br><br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE1FYSM] 

<span data-ttu-id="65154-105">Si vous avez trouvé cette vidéo utile, consultez les [séries de formations complètes pour les petites entreprises et les nouveaux utilisateurs de Microsoft 365](https://support.office.com/article/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816).</span><span class="sxs-lookup"><span data-stu-id="65154-105">If you found this video helpful, check out the [complete training series for small businesses and those new to Microsoft 365](https://support.office.com/article/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816).</span></span>

## <a name="add-your-domain-users-and-set-up-policies"></a><span data-ttu-id="65154-106">Ajouter votre domaine, vos utilisateurs et configurer des stratégies</span><span class="sxs-lookup"><span data-stu-id="65154-106">Add your domain, users, and set up policies</span></span>

<span data-ttu-id="65154-107">[![Étiquette vous informant le centre d’administration est en train de changer et vous pouvez trouver plus de détails à ce sujet à l’adresse aka.ms/aboutM365preview.](../media/m365admincenterchanging.png)](https://docs.microsoft.com/office365/admin/microsoft-365-admin-center-preview)</span><span class="sxs-lookup"><span data-stu-id="65154-107">[![Label to let you know the admin center is changing and you can find more details at aka.ms/aboutM365preview.](../media/m365admincenterchanging.png)](https://docs.microsoft.com/office365/admin/microsoft-365-admin-center-preview)</span></span>

<span data-ttu-id="65154-108">Lorsque vous achetez Microsoft 365 Business Premium, vous avez la possibilité d’utiliser un domaine que vous possédez ou d’en acheter un lors de l' [inscription](sign-up.md).</span><span class="sxs-lookup"><span data-stu-id="65154-108">When you purchase Microsoft 365 Business Premium, you have the option of using a domain you own, or buying one during the [sign-up](sign-up.md).</span></span>

- <span data-ttu-id="65154-109">Si vous avez acheté un nouveau domaine lorsque vous vous êtes inscrit, votre domaine est configuré et vous pouvez le déplacer pour [Ajouter des utilisateurs et attribuer des licences](#add-users-and-assign-licenses).</span><span class="sxs-lookup"><span data-stu-id="65154-109">If you purchased a new domain when you signed up, your domain is all set up and you can move to [Add users and assign licenses](#add-users-and-assign-licenses).</span></span>

### <a name="add-your-domain-to-personalize-sign-in"></a><span data-ttu-id="65154-110">Ajouter votre domaine pour personnaliser la connexion</span><span class="sxs-lookup"><span data-stu-id="65154-110">Add your domain to personalize sign-in</span></span>

1. <span data-ttu-id="65154-111">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide de vos informations d’identification d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="65154-111">Sign in to [Microsoft 365 admin center](https://admin.microsoft.com) by using your global admin credentials.</span></span> 

2. <span data-ttu-id="65154-112">Sélectionnez **accéder au programme d’installation** pour démarrer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="65154-112">Choose **Go to setup** to start the wizard.</span></span>

    ![Sélectionnez atteindre le programme d’installation.](../media/gotosetupinadmincenter.png)

3. <span data-ttu-id="65154-114">Sur la page **installer vos applications Office** , vous pouvez installer les applications sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="65154-114">On the **Install your Office apps** page, you can optionally install the apps on your own computer.</span></span>
    
4. <span data-ttu-id="65154-115">Dans l’étape **Ajouter un domaine** , entrez le nom de domaine que vous souhaitez utiliser (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="65154-115">In the **Add domain** step, enter the domain name you want to use (like contoso.com).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="65154-116">Si vous avez acheté un domaine lors de l’inscription, vous ne verrez pas **Ajouter une étape de domaine** ici.</span><span class="sxs-lookup"><span data-stu-id="65154-116">If you purchased a domain during the sign-up, you will not see **Add a domain** step here.</span></span> <span data-ttu-id="65154-117">Accédez à [Ajouter des utilisateurs](#add-users-and-assign-licenses) à la place.</span><span class="sxs-lookup"><span data-stu-id="65154-117">Go to [Add users](#add-users-and-assign-licenses) instead.</span></span>

    ![Capture d’écran de la page Personnalisez votre connexion.](../media/adddomain.png)

    
4. <span data-ttu-id="65154-119">Suivez les étapes de l’Assistant pour [créer des enregistrements DNS auprès d’un fournisseur d’hébergement DNS pour Office 365](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) qui vérifie que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="65154-119">Follow the steps in the wizard to [Create DNS records at any DNS hosting provider for Office 365](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) that verifies you own the domain.</span></span> <span data-ttu-id="65154-120">Si vous êtes conscient de votre hôte de domaine, reportez-vous aux [instructions spécifiques](https://docs.microsoft.com/office365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions)de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="65154-120">If you know your domain host, see also the [host specific instructions](https://docs.microsoft.com/office365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions).</span></span>

    <span data-ttu-id="65154-121">Si votre fournisseur d’hébergement est GoDaddy ou si un autre hôte est activé avec la [connexion au domaine](https://docs.microsoft.com/office365/admin/get-help-with-domains/domain-connect), le processus est facile et vous êtes automatiquement invité à vous connecter et à laisser Microsoft s’authentifier à votre place.</span><span class="sxs-lookup"><span data-stu-id="65154-121">If your hosting provider is GoDaddy or another host enabled with [domain connect](https://docs.microsoft.com/office365/admin/get-help-with-domains/domain-connect), the process is easy and you'll be automatically asked to sign in and let Microsoft authenticate on your behalf.</span></span>

    ![Sur GoDaddy, sélectionnez Autoriser.](../media/godaddyauth.png)

### <a name="add-users-and-assign-licenses"></a><span data-ttu-id="65154-123">Ajouter des utilisateurs et attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="65154-123">Add users and assign licenses</span></span>

<span data-ttu-id="65154-124">Vous pouvez ajouter des utilisateurs dans l’Assistant, mais vous pouvez également [Ajouter des utilisateurs ultérieurement](add-users-m365b.md) dans le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="65154-124">You can add users in the wizard, but you can also [add users later](add-users-m365b.md) in the admin center.</span></span> <span data-ttu-id="65154-125">En outre, si vous disposez d’un contrôleur de domaine local, vous pouvez ajouter des utilisateurs avec [Azure ad Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express).</span><span class="sxs-lookup"><span data-stu-id="65154-125">Additionally, if you have a local domain controller, you can add users with [Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express).</span></span>

#### <a name="add-users-in-the-wizard"></a><span data-ttu-id="65154-126">Ajouter des utilisateurs dans l’Assistant</span><span class="sxs-lookup"><span data-stu-id="65154-126">Add users in the wizard</span></span>

<span data-ttu-id="65154-127">Tous les utilisateurs que vous ajoutez dans l’Assistant reçoivent automatiquement une licence Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="65154-127">Any users you add in the wizard get automatically assigned a Microsoft 365 Business Premium license.</span></span>

![Capture d’écran de la page Ajouter de nouveaux utilisateurs dans l’Assistant](../media/addnewuserspage.png)

1. <span data-ttu-id="65154-129">Si votre abonnement Microsoft 365 Business Premium comporte des utilisateurs existants (par exemple, si vous avez utilisé Azure AD Connect), vous avez la possibilité de leur attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="65154-129">If your Microsoft 365 Business Premium subscription has existing users (for example, if you used Azure AD Connect), you get an option to assign licenses to them now.</span></span> <span data-ttu-id="65154-130">Poursuivez et ajoutez des licences pour eux aussi.</span><span class="sxs-lookup"><span data-stu-id="65154-130">Go ahead and add licenses to them as well.</span></span>

2. <span data-ttu-id="65154-131">Une fois que vous avez ajouté les utilisateurs, vous avez également la possibilité de partager des informations d’identification avec les nouveaux utilisateurs que vous avez ajoutés.</span><span class="sxs-lookup"><span data-stu-id="65154-131">After you've added the users, you'll also get an option to share credentials with the new users you added.</span></span> <span data-ttu-id="65154-132">Vous pouvez choisir de les imprimer, de les envoyer par e-mail ou de les télécharger.</span><span class="sxs-lookup"><span data-stu-id="65154-132">You can choose to print them out, email them, or download them.</span></span>

### <a name="connect-your-domain"></a><span data-ttu-id="65154-133">Sélectionner votre domaine</span><span class="sxs-lookup"><span data-stu-id="65154-133">Connect your domain</span></span>

> [!NOTE]
> <span data-ttu-id="65154-134">Si vous avez choisi d’utiliser le domaine. onmicrosoft ou si vous avez utilisé Azure AD Connect pour configurer des utilisateurs, vous ne verrez pas cette étape.</span><span class="sxs-lookup"><span data-stu-id="65154-134">If you chose to use the .onmicrosoft domain, or used Azure AD Connect to set up users, you will not see this step.</span></span>
  
<span data-ttu-id="65154-135">Pour configurer des services, vous devez mettre à jour des enregistrements au niveau de votre hôte DNS ou de votre bureau d'enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="65154-135">To set up services, you have to update some records at your DNS host or domain registrar.</span></span>
  
1. <span data-ttu-id="65154-136">L'Assistant Configuration détecte généralement votre bureau d'enregistrement et vous fournit un lien vers des instructions détaillées vous permettant de mettre à jour vos enregistrements NS sur le site web du bureau d'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="65154-136">The setup wizard typically detects your registrar and gives you a link to step-by-step instructions for updating your NS records at the registrar website.</span></span> <span data-ttu-id="65154-137">Si ce n’est pas le cas, [Modifiez les serveurs de noms pour configurer Office 365 avec n’importe quel](https://support.office.com/article/a8b487a9-2a45-4581-9dc4-5d28a47010a2)Bureau d’enregistrement de domaine.</span><span class="sxs-lookup"><span data-stu-id="65154-137">If it doesn't, [Change nameservers to set up Office 365 with any domain registrar](https://support.office.com/article/a8b487a9-2a45-4581-9dc4-5d28a47010a2).</span></span> 

    - <span data-ttu-id="65154-138">Si vous avez des enregistrements DNS existants, par exemple un site Web existant, mais que votre hôte DNS est activé pour la [connexion au domaine](https://docs.microsoft.com/office365/admin/get-help-with-domains/domain-connect), choisissez **Ajouter des enregistrements pour moi**.</span><span class="sxs-lookup"><span data-stu-id="65154-138">If you have existing DNS records, for example an existing web site, but your DNS host is enabled for [domain connect](https://docs.microsoft.com/office365/admin/get-help-with-domains/domain-connect), choose **Add records for me**.</span></span> <span data-ttu-id="65154-139">Sur la page **choisir vos services en ligne** , acceptez toutes les valeurs par défaut, cliquez sur **suivant**, puis choisissez **autoriser** sur la page de votre hôte DNS.</span><span class="sxs-lookup"><span data-stu-id="65154-139">On the **Choose your online services** page, accept all the defaults, and choose **Next**, and choose **Authorize** on your DNS host's page.</span></span>
    - <span data-ttu-id="65154-140">Si vous avez des enregistrements DNS existants avec d’autres hôtes DNS (non activé pour la connexion au domaine), vous pouvez gérer vos propres enregistrements DNS afin de vous assurer que les services existants restent connectés.</span><span class="sxs-lookup"><span data-stu-id="65154-140">If you have existing DNS records with other DNS hosts (not enabled for domain connect), you'll want to manage your own DNS records to make sure the existing services stay connected.</span></span> <span data-ttu-id="65154-141">Pour plus d’informations, voir [notions de base](https://docs.microsoft.com/office365/admin/get-help-with-domains/dns-basics) sur le domaine.</span><span class="sxs-lookup"><span data-stu-id="65154-141">See [domain basics](https://docs.microsoft.com/office365/admin/get-help-with-domains/dns-basics) for more info.</span></span>

        ![Page activer les enregistrements.](../media/activaterecords.png)

2. <span data-ttu-id="65154-143">Suivez les étapes de l’Assistant et de la messagerie et d’autres services sont configurés pour vous.</span><span class="sxs-lookup"><span data-stu-id="65154-143">Follow the steps in the wizard and email and other services will be set up for you.</span></span>

### <a name="protect-your-organization"></a><span data-ttu-id="65154-144">Protéger votre organisation</span><span class="sxs-lookup"><span data-stu-id="65154-144">Protect your organization</span></span> 

<span data-ttu-id="65154-145">Les stratégies que vous configurez dans l’Assistant sont appliquées automatiquement à un [groupe de sécurité](https://docs.microsoft.com/office365/admin/create-groups/compare-groups#security-groups) appelé *tous les utilisateurs*.</span><span class="sxs-lookup"><span data-stu-id="65154-145">The policies you set up in the wizard are applied automatically to a [Security group](https://docs.microsoft.com/office365/admin/create-groups/compare-groups#security-groups) called *All Users*.</span></span> <span data-ttu-id="65154-146">Vous pouvez également créer des groupes supplémentaires auxquels affecter des stratégies dans le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="65154-146">You can also create additional groups to assign policies to in the admin center.</span></span>

1. <span data-ttu-id="65154-147">Sur la **protection renforcée contre les menaces informatiques avancées**, il est recommandé d’accepter les valeurs par défaut pour permettre à [Office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp) d’analyser les fichiers et les liens dans les applications Office.</span><span class="sxs-lookup"><span data-stu-id="65154-147">On the **Increase protection from advanced cyber threats**, it is recommended that you accept the defaults to let [Office 365 Advance Threat Protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp) scan files and links in Office apps.</span></span>

    ![Capture d’écran de la page d’augmentation de la protection.](../media/increasetreatprotection.png)


2. <span data-ttu-id="65154-149">Sur la page **empêcher les fuites de données sensibles** , acceptez les valeurs par défaut pour activer la protection contre la perte de données (DLP) d’Office 365 pour effectuer le suivi des données sensibles dans les applications Office et empêcher le partage accidentel de ces derniers à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="65154-149">On the **Prevent leaks of sensitive data** page, accept the defaults to turn on Office 365 Data Loss Prevention (DLP) to track sensitive data in Office apps and prevent the accidental sharing of these outside your organization.</span></span>

3. <span data-ttu-id="65154-150">Sur la page **protéger les données dans Office pour les appareils mobiles** , conservez la gestion des applications mobiles activée, développez les paramètres et examinez-les, puis sélectionnez **créer une stratégie de gestion des applications mobiles**.</span><span class="sxs-lookup"><span data-stu-id="65154-150">On the **Protect data in Office for mobile** page, leave mobile app management on, expand the settings and review them, and then select **Create mobile app management policy**.</span></span>

    ![Capture d’écran de la page protéger les données dans Office pour les appareils mobiles.](../media/protectdatainmobile.png)


## <a name="secure-windows-10-pcs"></a><span data-ttu-id="65154-152">Sécurisation des PC Windows 10</span><span class="sxs-lookup"><span data-stu-id="65154-152">Secure Windows 10 PCs</span></span>

<span data-ttu-id="65154-153">Dans le volet de navigation de gauche, sélectionnez **configuration** , puis sous **connexion et sécurité**, choisissez **sécuriser vos ordinateurs Windows 10**.</span><span class="sxs-lookup"><span data-stu-id="65154-153">On the left nav, select **Setup** and then, under **Sign-in and security**, choose **Secure your Windows 10 computers**.</span></span> <span data-ttu-id="65154-154">Choisissez **affichage** pour commencer.</span><span class="sxs-lookup"><span data-stu-id="65154-154">Choose **View** to get started.</span></span> <span data-ttu-id="65154-155">Pour plus d’informations, consultez [la rubrique sécuriser vos ordinateurs Windows 10](secure-win-10-pcs.md) .</span><span class="sxs-lookup"><span data-stu-id="65154-155">See [secure your Windows 10 computers](secure-win-10-pcs.md) for complete instructions.</span></span>

## <a name="deploy-office-365-client-apps"></a><span data-ttu-id="65154-156">Déployer des applications clientes Office 365</span><span class="sxs-lookup"><span data-stu-id="65154-156">Deploy Office 365 client apps</span></span>

<span data-ttu-id="65154-157">Si vous avez choisi d’installer automatiquement les applications Office lors de l’installation, les applications sont installées sur les appareils Windows 10 une fois que les utilisateurs se sont connectés à Azure AD à partir de leurs appareils Windows, à l’aide de leurs informations d’identification professionnelles.</span><span class="sxs-lookup"><span data-stu-id="65154-157">If you chose to automatically install Office apps during setup, the apps will install on the Windows 10 devices once the users have signed in to Azure AD from their Windows devices, using their work credentials.</span></span>

<span data-ttu-id="65154-158">Pour installer Office sur des appareils mobiles iOS ou Android, consultez la rubrique [configurer des appareils mobiles pour les utilisateurs de Microsoft 365 Business Premium](set-up-mobile-devices.md).</span><span class="sxs-lookup"><span data-stu-id="65154-158">To install Office on mobile iOS or Android devices, see [Set up mobile devices for Microsoft 365 Business Premium users](set-up-mobile-devices.md).</span></span>

<span data-ttu-id="65154-159">Vous pouvez également installer Office individuellement.</span><span class="sxs-lookup"><span data-stu-id="65154-159">You can also install Office individually.</span></span> <span data-ttu-id="65154-160">Pour obtenir des instructions, voir [installer Office sur un PC ou un Mac](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc4716658) .</span><span class="sxs-lookup"><span data-stu-id="65154-160">See [install Office on a PC or Mac](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc4716658) for instructions.</span></span>

## <a name="see-also"></a><span data-ttu-id="65154-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65154-161">See also</span></span>

[<span data-ttu-id="65154-162">Vidéos de formation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="65154-162">Microsoft 365 for business training videos</span></span>](https://support.office.com/article/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816)
