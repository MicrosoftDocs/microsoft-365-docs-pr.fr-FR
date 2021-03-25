---
title: Configurer Microsoft 365 Business Premium
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
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
ms.assetid: 6e7a2dfd-8ec4-4eb7-8390-3ee103e5fece
description: Découvrez les étapes de configuration de Microsoft 365 Business Premium, notamment l’ajout d’un domaine et d’utilisateurs, la configuration de stratégies de sécurité, etc.
ms.openlocfilehash: a06fb48ef5e1386a5c7b4df08500125f37943df6
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51198429"
---
# <a name="set-up-microsoft-365-business-premium-in-the-setup-wizard"></a><span data-ttu-id="7246d-103">Configurer Microsoft 365 Business Premium dans l’Assistant Installation</span><span class="sxs-lookup"><span data-stu-id="7246d-103">Set up Microsoft 365 Business Premium in the setup wizard</span></span>

<span data-ttu-id="7246d-104">Regardez cette vidéo pour obtenir une vue d’ensemble de la configuration de Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="7246d-104">Watch this video for an overview of Microsoft 365 Business Premium setup.</span></span><br><br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4jZwg] 

## <a name="add-your-domain-users-and-set-up-policies"></a><span data-ttu-id="7246d-105">Ajouter votre domaine, vos utilisateurs et configurer des stratégies</span><span class="sxs-lookup"><span data-stu-id="7246d-105">Add your domain, users, and set up policies</span></span>

<span data-ttu-id="7246d-106">Lorsque vous achetez Microsoft 365 Business Premium, vous avez la possibilité d’utiliser un domaine que vous possédez ou d’en acheter un lors de [l’inscription.](sign-up.md)</span><span class="sxs-lookup"><span data-stu-id="7246d-106">When you purchase Microsoft 365 Business Premium, you have the option of using a domain you own, or buying one during the [sign-up](sign-up.md).</span></span>

- <span data-ttu-id="7246d-107">Si vous avez acheté un nouveau domaine lorsque vous vous êtes inscrit, votre domaine est configuré et vous pouvez accéder à [Ajouter des utilisateurs et attribuer des licences](#add-users-and-assign-licenses).</span><span class="sxs-lookup"><span data-stu-id="7246d-107">If you purchased a new domain when you signed up, your domain is all set up and you can move to [Add users and assign licenses](#add-users-and-assign-licenses).</span></span>

### <a name="add-your-domain-to-personalize-sign-in"></a><span data-ttu-id="7246d-108">Ajouter votre domaine pour personnaliser la connexion</span><span class="sxs-lookup"><span data-stu-id="7246d-108">Add your domain to personalize sign-in</span></span>

1. <span data-ttu-id="7246d-109">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide de vos informations d’identification d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="7246d-109">Sign in to [Microsoft 365 admin center](https://admin.microsoft.com) by using your global admin credentials.</span></span> 

2. <span data-ttu-id="7246d-110">Choisissez **Configurer** pour démarrer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="7246d-110">Choose **Go to setup** to start the wizard.</span></span>

    ![Sélectionnez Aller à l’installation.](../media/gotosetupinadmincenter.png)

3. <span data-ttu-id="7246d-112">Sur la page **Installer vos applications Office**, vous pouvez installer les applications sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7246d-112">On the **Install your Office apps** page, you can optionally install the apps on your own computer.</span></span>
    
4. <span data-ttu-id="7246d-113">Dans l’étape **ajouter un domaine**, entrez le nom de domaine que vous voulez utiliser (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="7246d-113">In the **Add domain** step, enter the domain name you want to use (like contoso.com).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="7246d-114">Si vous avez acheté un domaine pendant l’inscription, vous ne verrez pas l’étape **Ajouter un domaine** ici.</span><span class="sxs-lookup"><span data-stu-id="7246d-114">If you purchased a domain during the sign-up, you will not see **Add a domain** step here.</span></span> <span data-ttu-id="7246d-115">Accédez à [Ajouter des utilisateurs](#add-users-and-assign-licenses) à la place.</span><span class="sxs-lookup"><span data-stu-id="7246d-115">Go to [Add users](#add-users-and-assign-licenses) instead.</span></span>

    ![Capture d’écran de la page Personnaliser votre connectez-vous.](../media/adddomain.png)

    
4. <span data-ttu-id="7246d-117">Suivez les étapes de l’Assistant pour créer des enregistrements DNS chez un fournisseur d’hébergement [DNS pour Microsoft 365](/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) qui vérifie que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="7246d-117">Follow the steps in the wizard to [Create DNS records at any DNS hosting provider for Microsoft 365](/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) that verifies you own the domain.</span></span> <span data-ttu-id="7246d-118">Si vous savez qu’il s’agit de votre hôte de domaine, consultez également les [Instructions propres à l’hôte](/office365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions).</span><span class="sxs-lookup"><span data-stu-id="7246d-118">If you know your domain host, see also the [host specific instructions](/office365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions).</span></span>

    <span data-ttu-id="7246d-119">Si votre fournisseur d’hébergement est GoDaddy ou si un autre hôte est activé avec [connexion de domaine](/office365/admin/get-help-with-domains/domain-connect), le processus est simple et vous êtes automatiquement invité à vous connecter et à laisser Microsoft s’authentifier en votre nom.</span><span class="sxs-lookup"><span data-stu-id="7246d-119">If your hosting provider is GoDaddy or another host enabled with [domain connect](/office365/admin/get-help-with-domains/domain-connect), the process is easy and you'll be automatically asked to sign in and let Microsoft authenticate on your behalf.</span></span>

    ![Sur la page Confirmer l’accès GoDaddy, sélectionnez Autoriser.](../media/godaddyauth.png)

### <a name="add-users-and-assign-licenses"></a><span data-ttu-id="7246d-121">Ajouter des utilisateurs et attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="7246d-121">Add users and assign licenses</span></span>

<span data-ttu-id="7246d-122">Vous pouvez ajouter des utilisateurs dans l’Assistant, mais vous pouvez également [Ajouter des utilisateurs plus tard](../admin/add-users/add-users.md) dans le Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="7246d-122">You can add users in the wizard, but you can also [add users later](../admin/add-users/add-users.md) in the admin center.</span></span> <span data-ttu-id="7246d-123">De plus, si vous avez un contrôleur de domaine local, vous pouvez ajouter des utilisateurs avec [Azure AD Connect](/azure/active-directory/hybrid/how-to-connect-install-express).</span><span class="sxs-lookup"><span data-stu-id="7246d-123">Additionally, if you have a local domain controller, you can add users with [Azure AD Connect](/azure/active-directory/hybrid/how-to-connect-install-express).</span></span>

#### <a name="add-users-in-the-wizard"></a><span data-ttu-id="7246d-124">Ajouter des utilisateurs dans l’Assistant</span><span class="sxs-lookup"><span data-stu-id="7246d-124">Add users in the wizard</span></span>

<span data-ttu-id="7246d-125">Les utilisateurs que vous ajoutez dans l’Assistant obtiennent automatiquement une licence Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="7246d-125">Any users you add in the wizard get automatically assigned a Microsoft 365 Business Premium license.</span></span>

![Capture d’écran de la page Ajouter de nouveaux utilisateurs dans l’Assistant](../media/addnewuserspage.png)

1. <span data-ttu-id="7246d-127">Si votre abonnement Microsoft 365 Business Premium dispose d’utilisateurs existants (par exemple, si vous avez utilisé Azure AD Connect), vous avez la possibilité de leur attribuer des licences maintenant.</span><span class="sxs-lookup"><span data-stu-id="7246d-127">If your Microsoft 365 Business Premium subscription has existing users (for example, if you used Azure AD Connect), you get an option to assign licenses to them now.</span></span> <span data-ttu-id="7246d-128">Poursuivez et ajoutez des licences pour eux aussi.</span><span class="sxs-lookup"><span data-stu-id="7246d-128">Go ahead and add licenses to them as well.</span></span>

2. <span data-ttu-id="7246d-129">Une fois que vous avez ajouté les utilisateurs, vous avez également la possibilité de partager des informations d’identification avec les nouveaux utilisateurs que vous ajoutez.</span><span class="sxs-lookup"><span data-stu-id="7246d-129">After you've added the users, you'll also get an option to share credentials with the new users you added.</span></span> <span data-ttu-id="7246d-130">Vous pouvez choisir de les imprimer, de les envoyer par e-mail ou de les télécharger.</span><span class="sxs-lookup"><span data-stu-id="7246d-130">You can choose to print them out, email them, or download them.</span></span>

### <a name="connect-your-domain"></a><span data-ttu-id="7246d-131">Sélectionner votre domaine</span><span class="sxs-lookup"><span data-stu-id="7246d-131">Connect your domain</span></span>

> [!NOTE]
> <span data-ttu-id="7246d-132">Si vous avez choisi d’utiliser le domaine .onmicrosoft, ou si vous avez utilisé Azure AD Connect pour configurer des utilisateurs, vous ne verrez pas cette étape.</span><span class="sxs-lookup"><span data-stu-id="7246d-132">If you chose to use the .onmicrosoft domain, or used Azure AD Connect to set up users, you will not see this step.</span></span>
  
<span data-ttu-id="7246d-133">Pour configurer des services, vous devez mettre à jour des enregistrements au niveau de votre hôte DNS ou de votre bureau d’enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="7246d-133">To set up services, you have to update some records at your DNS host or domain registrar.</span></span>
  
1. <span data-ttu-id="7246d-134">L’Assistant Configuration détecte généralement votre bureau d’enregistrement et vous fournit un lien vers des instructions détaillées vous permettant de mettre à jour vos enregistrements NS sur le site web du bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="7246d-134">The setup wizard typically detects your registrar and gives you a link to step-by-step instructions for updating your NS records at the registrar website.</span></span> <span data-ttu-id="7246d-135">Si ce n’est pas le cas, modifiez les serveurs de noms pour configurer [Microsoft 365 auprès d’un bureau d’enregistrement de domaines.](../admin/get-help-with-domains/change-nameservers-at-any-domain-registrar.md)</span><span class="sxs-lookup"><span data-stu-id="7246d-135">If it doesn't, [Change nameservers to set up Microsoft 365 with any domain registrar](../admin/get-help-with-domains/change-nameservers-at-any-domain-registrar.md).</span></span> 

    - <span data-ttu-id="7246d-136">Si vous avez des enregistrements DNS existants (par exemple, un site web existant), mais que votre hôte DNS est activé pour [connexion de domaine](/office365/admin/get-help-with-domains/domain-connect), sélectionnez **Ajouter des enregistrements pour moi**.</span><span class="sxs-lookup"><span data-stu-id="7246d-136">If you have existing DNS records, for example an existing web site, but your DNS host is enabled for [domain connect](/office365/admin/get-help-with-domains/domain-connect), choose **Add records for me**.</span></span> <span data-ttu-id="7246d-137">Sur la page **sélectionnez votre services en ligne**, acceptez toutes les valeurs par défaut, puis sélectionnez **Suivant**, puis sélectionnez **Autoriser** sur la page de votre hôte DNS.</span><span class="sxs-lookup"><span data-stu-id="7246d-137">On the **Choose your online services** page, accept all the defaults, and choose **Next**, and choose **Authorize** on your DNS host's page.</span></span>
    - <span data-ttu-id="7246d-138">Si vous avez des enregistrements DNS existants avec d’autres hôtes DNS (non activé pour la connexion de domaine), vous pouvez gérer vos propres enregistrements DNS pour vous assurer que les services existants restent connectés.</span><span class="sxs-lookup"><span data-stu-id="7246d-138">If you have existing DNS records with other DNS hosts (not enabled for domain connect), you'll want to manage your own DNS records to make sure the existing services stay connected.</span></span> <span data-ttu-id="7246d-139">Pour plus d’informations, consultez [notions de base du domaine](/office365/admin/get-help-with-domains/dns-basics).</span><span class="sxs-lookup"><span data-stu-id="7246d-139">See [domain basics](/office365/admin/get-help-with-domains/dns-basics) for more info.</span></span>

        ![Page Activer les enregistrements.](../media/activaterecords.png)

2. <span data-ttu-id="7246d-141">Suivez les étapes de l’Assistant, et la messagerie électronique et d’autres services sont configurés pour vous.</span><span class="sxs-lookup"><span data-stu-id="7246d-141">Follow the steps in the wizard and email and other services will be set up for you.</span></span>

### <a name="protect-your-organization"></a><span data-ttu-id="7246d-142">Protéger votre organisation</span><span class="sxs-lookup"><span data-stu-id="7246d-142">Protect your organization</span></span> 

<span data-ttu-id="7246d-143">Les stratégies que vous avez définies dans l’Assistant sont appliquées automatiquement à un groupe [de sécurité](/office365/admin/create-groups/compare-groups#security-groups) appelé Tous *les utilisateurs.*</span><span class="sxs-lookup"><span data-stu-id="7246d-143">The policies you set up in the wizard are applied automatically to a [Security group](/office365/admin/create-groups/compare-groups#security-groups) called *All Users*.</span></span> <span data-ttu-id="7246d-144">Vous pouvez également créer des groupes supplémentaires pour attribuer des stratégies dans le Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="7246d-144">You can also create additional groups to assign policies to in the admin center.</span></span>

1. <span data-ttu-id="7246d-145">Dans l’option Augmenter la **protection** contre les cybermenaces avancées, il est recommandé d’accepter les valeurs par défaut pour laisser [Office 365 Advance Threat Protection](../security/office-365-security/defender-for-office-365.md) analyser les fichiers et les liens dans les applications Office.</span><span class="sxs-lookup"><span data-stu-id="7246d-145">On the **Increase protection from advanced cyber threats**, it is recommended that you accept the defaults to let [Office 365 Advance Threat Protection](../security/office-365-security/defender-for-office-365.md) scan files and links in Office apps.</span></span>

    ![Capture d’écran de la page Augmenter la protection.](../media/increasetreatprotection.png)


2. <span data-ttu-id="7246d-147">Dans la page Empêcher les fuites de données **sensibles,** acceptez les valeurs par défaut pour activer la protection contre la perte de données Office 365 (DLP) pour suivre les données sensibles dans les applications Office et empêcher le partage accidentel de ces données à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7246d-147">On the **Prevent leaks of sensitive data** page, accept the defaults to turn on Office 365 Data Loss Prevention (DLP) to track sensitive data in Office apps and prevent the accidental sharing of these outside your organization.</span></span>

3. <span data-ttu-id="7246d-148">Dans la page Protéger les données dans Office pour **appareils mobiles,** laissez la gestion des applications mobiles en place, développez les paramètres et examinez-les, puis sélectionnez Créer une stratégie de gestion des applications **mobiles.**</span><span class="sxs-lookup"><span data-stu-id="7246d-148">On the **Protect data in Office for mobile** page, leave mobile app management on, expand the settings and review them, and then select **Create mobile app management policy**.</span></span>

    ![Capture d’écran de la page Protéger les données dans Office pour appareils mobiles.](../media/protectdatainmobile.png)


## <a name="secure-windows-10-pcs"></a><span data-ttu-id="7246d-150">Sécuriser les PC Windows 10</span><span class="sxs-lookup"><span data-stu-id="7246d-150">Secure Windows 10 PCs</span></span>

<span data-ttu-id="7246d-151">Dans le navigation de gauche, sélectionnez **Programme** d’installation, puis, sous Se connectez **et sécurité,** sélectionnez Sécuriser **vos ordinateurs Windows 10.**</span><span class="sxs-lookup"><span data-stu-id="7246d-151">On the left nav, select **Setup** and then, under **Sign-in and security**, choose **Secure your Windows 10 computers**.</span></span> <span data-ttu-id="7246d-152">Choose **View** to get started.</span><span class="sxs-lookup"><span data-stu-id="7246d-152">Choose **View** to get started.</span></span> <span data-ttu-id="7246d-153">Pour obtenir des instructions complètes, consultez sécuriser vos ordinateurs [Windows 10.](secure-win-10-pcs.md)</span><span class="sxs-lookup"><span data-stu-id="7246d-153">See [secure your Windows 10 computers](secure-win-10-pcs.md) for complete instructions.</span></span>

## <a name="deploy-office-365-client-apps"></a><span data-ttu-id="7246d-154">Déployer des applications clientes Office 365</span><span class="sxs-lookup"><span data-stu-id="7246d-154">Deploy Office 365 client apps</span></span>

<span data-ttu-id="7246d-155">Si vous avez choisi d’installer automatiquement les applications Office lors de l’installation, les applications s’installent sur les appareils Windows 10 une fois que les utilisateurs se sont connectés à Azure AD à partir de leurs appareils Windows, à l’aide de leurs informations d’identification professionnelles.</span><span class="sxs-lookup"><span data-stu-id="7246d-155">If you chose to automatically install Office apps during setup, the apps will install on the Windows 10 devices once the users have signed in to Azure AD from their Windows devices, using their work credentials.</span></span>

<span data-ttu-id="7246d-156">Pour installer Office sur des appareils iOS ou Android mobiles, voir Configurer des appareils mobiles pour les utilisateurs [de Microsoft 365 Business Premium.](set-up-mobile-devices.md)</span><span class="sxs-lookup"><span data-stu-id="7246d-156">To install Office on mobile iOS or Android devices, see [Set up mobile devices for Microsoft 365 Business Premium users](set-up-mobile-devices.md).</span></span>

<span data-ttu-id="7246d-157">Vous pouvez également installer Office individuellement.</span><span class="sxs-lookup"><span data-stu-id="7246d-157">You can also install Office individually.</span></span> <span data-ttu-id="7246d-158">Voir [installer Office sur un PC ou Mac pour](https://support.microsoft.com/office/4414eaaf-0478-48be-9c42-23adc4716658) obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="7246d-158">See [install Office on a PC or Mac](https://support.microsoft.com/office/4414eaaf-0478-48be-9c42-23adc4716658) for instructions.</span></span>

## <a name="see-also"></a><span data-ttu-id="7246d-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7246d-159">See also</span></span>

[<span data-ttu-id="7246d-160">Vidéos de formation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="7246d-160">Microsoft 365 for business training videos</span></span>](https://support.microsoft.com/office/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816)
