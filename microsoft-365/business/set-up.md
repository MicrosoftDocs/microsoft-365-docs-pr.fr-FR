---
title: Configurer Microsoft 365 Business Premium
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
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
description: Découvrez les étapes de configuration Microsoft 365 Business Premium, notamment l’ajout d’un domaine et d’utilisateurs, la configuration de stratégies de sécurité, etc.
ms.openlocfilehash: 3e15f16db2a233d2e11d444600398102b075932d
ms.sourcegitcommit: 686f192e1a650ec805fe8e908b46ca51771ed41f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52624386"
---
# <a name="set-up-microsoft-365-business-premium-in-the-setup-wizard"></a><span data-ttu-id="afac7-103">Configurer des Microsoft 365 Business Premium dans l’Assistant Installation</span><span class="sxs-lookup"><span data-stu-id="afac7-103">Set up Microsoft 365 Business Premium in the setup wizard</span></span>

## <a name="watch-overview-of-microsoft-365-setup"></a><span data-ttu-id="afac7-104">Regardez : Vue d’ensemble de Microsoft 365 configuration</span><span class="sxs-lookup"><span data-stu-id="afac7-104">Watch: Overview of Microsoft 365 setup</span></span>

<span data-ttu-id="afac7-105">Regardez cette vidéo pour obtenir une vue d’ensemble Microsoft 365 Business Premium configuration.</span><span class="sxs-lookup"><span data-stu-id="afac7-105">Watch this video for an overview of Microsoft 365 Business Premium setup.</span></span><br><br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4jZwg] 

## <a name="add-your-domain-users-and-set-up-policies"></a><span data-ttu-id="afac7-106">Ajouter votre domaine, vos utilisateurs et configurer des stratégies</span><span class="sxs-lookup"><span data-stu-id="afac7-106">Add your domain, users, and set up policies</span></span>

<span data-ttu-id="afac7-107">Lorsque vous achetez Microsoft 365 Business Premium, vous avez la possibilité d’utiliser un domaine que vous possédez ou d’en acheter un lors de [l’inscription.](sign-up.md)</span><span class="sxs-lookup"><span data-stu-id="afac7-107">When you purchase Microsoft 365 Business Premium, you have the option of using a domain you own, or buying one during the [sign-up](sign-up.md).</span></span>

- <span data-ttu-id="afac7-108">Si vous avez acheté un nouveau domaine lorsque vous vous êtes inscrit, votre domaine est configuré et vous pouvez accéder à [Ajouter des utilisateurs et attribuer des licences](#add-users-and-assign-licenses).</span><span class="sxs-lookup"><span data-stu-id="afac7-108">If you purchased a new domain when you signed up, your domain is all set up and you can move to [Add users and assign licenses](#add-users-and-assign-licenses).</span></span>

### <a name="add-your-domain-to-personalize-sign-in"></a><span data-ttu-id="afac7-109">Ajouter votre domaine pour personnaliser la connexion</span><span class="sxs-lookup"><span data-stu-id="afac7-109">Add your domain to personalize sign-in</span></span>

1. <span data-ttu-id="afac7-110">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide de vos informations d’identification d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="afac7-110">Sign in to [Microsoft 365 admin center](https://admin.microsoft.com) by using your global admin credentials.</span></span> 

2. <span data-ttu-id="afac7-111">Choisissez **Configurer** pour démarrer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="afac7-111">Choose **Go to setup** to start the wizard.</span></span>

    ![Sélectionnez Aller à l’installation.](../media/gotosetupinadmincenter.png)

3. <span data-ttu-id="afac7-113">Sur la page **Installer vos applications Office**, vous pouvez installer les applications sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="afac7-113">On the **Install your Office apps** page, you can optionally install the apps on your own computer.</span></span>
    
4. <span data-ttu-id="afac7-114">Dans l’étape **ajouter un domaine**, entrez le nom de domaine que vous voulez utiliser (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="afac7-114">In the **Add domain** step, enter the domain name you want to use (like contoso.com).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="afac7-p101">Si vous avez acheté un domaine pendant l'inscription, vous ne verrez pas l'étape **Ajouter un domaine** ici. Allez à [Ajouter](#add-users-and-assign-licenses) des utilisateurs à la place.</span><span class="sxs-lookup"><span data-stu-id="afac7-p101">If you purchased a domain during the sign-up, you will not see **Add a domain** step here. Go to [Add users](#add-users-and-assign-licenses) instead.</span></span>

    ![Capture d’écran de la page Personnaliser votre connectez-vous.](../media/adddomain.png)

    
4. <span data-ttu-id="afac7-118">Suivez les étapes de l’Assistant pour créer des enregistrements DNS chez un fournisseur d’hébergement [DNS](/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) Microsoft 365 qui vérifie que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="afac7-118">Follow the steps in the wizard to [Create DNS records at any DNS hosting provider for Microsoft 365](/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) that verifies you own the domain.</span></span> <span data-ttu-id="afac7-119">Si vous savez qu’il s’agit de votre hôte de domaine, consultez également les [Instructions propres à l’hôte](/office365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions).</span><span class="sxs-lookup"><span data-stu-id="afac7-119">If you know your domain host, see also the [host specific instructions](/office365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions).</span></span>

    <span data-ttu-id="afac7-120">Si votre fournisseur d’hébergement est GoDaddy ou si un autre hôte est activé avec [connexion de domaine](/office365/admin/get-help-with-domains/domain-connect), le processus est simple et vous êtes automatiquement invité à vous connecter et à laisser Microsoft s’authentifier en votre nom.</span><span class="sxs-lookup"><span data-stu-id="afac7-120">If your hosting provider is GoDaddy or another host enabled with [domain connect](/office365/admin/get-help-with-domains/domain-connect), the process is easy and you'll be automatically asked to sign in and let Microsoft authenticate on your behalf.</span></span>

    ![Sur la page Confirmer l’accès GoDaddy, sélectionnez Autoriser.](../media/godaddyauth.png)

### <a name="add-users-and-assign-licenses"></a><span data-ttu-id="afac7-122">Ajouter des utilisateurs et attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="afac7-122">Add users and assign licenses</span></span>

<span data-ttu-id="afac7-123">Vous pouvez ajouter des utilisateurs dans l’Assistant, mais vous pouvez également [Ajouter des utilisateurs plus tard](../admin/add-users/add-users.md) dans le Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="afac7-123">You can add users in the wizard, but you can also [add users later](../admin/add-users/add-users.md) in the admin center.</span></span> <span data-ttu-id="afac7-124">De plus, si vous avez un contrôleur de domaine local, vous pouvez ajouter des utilisateurs avec [Azure AD Connect](/azure/active-directory/hybrid/how-to-connect-install-express).</span><span class="sxs-lookup"><span data-stu-id="afac7-124">Additionally, if you have a local domain controller, you can add users with [Azure AD Connect](/azure/active-directory/hybrid/how-to-connect-install-express).</span></span>

#### <a name="add-users-in-the-wizard"></a><span data-ttu-id="afac7-125">Ajouter des utilisateurs dans l’Assistant</span><span class="sxs-lookup"><span data-stu-id="afac7-125">Add users in the wizard</span></span>

<span data-ttu-id="afac7-126">Tous les utilisateurs que vous ajoutez dans l’Assistant obtiennent automatiquement une licence Microsoft 365 Business Premium licence.</span><span class="sxs-lookup"><span data-stu-id="afac7-126">Any users you add in the wizard get automatically assigned a Microsoft 365 Business Premium license.</span></span>

![Capture d’écran de la page Ajouter de nouveaux utilisateurs dans l’Assistant](../media/addnewuserspage.png)

1. <span data-ttu-id="afac7-128">Si votre abonnement Microsoft 365 Business Premium a des utilisateurs existants (par exemple, si vous avez utilisé Azure AD Connecter), vous avez la possibilité de leur attribuer des licences maintenant.</span><span class="sxs-lookup"><span data-stu-id="afac7-128">If your Microsoft 365 Business Premium subscription has existing users (for example, if you used Azure AD Connect), you get an option to assign licenses to them now.</span></span> <span data-ttu-id="afac7-129">Poursuivez et ajoutez des licences pour eux aussi.</span><span class="sxs-lookup"><span data-stu-id="afac7-129">Go ahead and add licenses to them as well.</span></span>

2. <span data-ttu-id="afac7-p105">Après avoir ajouté des utilisateurs, vous avez également la possibilité de partager des informations d'identification avec les nouveaux utilisateurs que vous avez ajouté. Vous pouvez choisir de les imprimer, de les envoyer par e-mail ou les télécharger.</span><span class="sxs-lookup"><span data-stu-id="afac7-p105">After you've added the users, you'll also get an option to share credentials with the new users you added. You can choose to print them out, email them, or download them.</span></span>

### <a name="connect-your-domain"></a><span data-ttu-id="afac7-132">Sélectionner votre domaine</span><span class="sxs-lookup"><span data-stu-id="afac7-132">Connect your domain</span></span>

> [!NOTE]
> <span data-ttu-id="afac7-133">Si vous avez choisi d’utiliser le domaine .onmicrosoft, ou si vous avez utilisé Azure AD Connect pour configurer des utilisateurs, vous ne verrez pas cette étape.</span><span class="sxs-lookup"><span data-stu-id="afac7-133">If you chose to use the .onmicrosoft domain, or used Azure AD Connect to set up users, you will not see this step.</span></span>
  
<span data-ttu-id="afac7-134">Pour configurer des services, vous devez mettre à jour des enregistrements au niveau de votre hôte DNS ou de votre bureau d’enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="afac7-134">To set up services, you have to update some records at your DNS host or domain registrar.</span></span>
  
1. <span data-ttu-id="afac7-135">L’Assistant Configuration détecte généralement votre bureau d’enregistrement et vous fournit un lien vers des instructions détaillées vous permettant de mettre à jour vos enregistrements NS sur le site web du bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="afac7-135">The setup wizard typically detects your registrar and gives you a link to step-by-step instructions for updating your NS records at the registrar website.</span></span> <span data-ttu-id="afac7-136">Si ce n’est pas le cas, modifiez les serveurs de noms pour configurer [Microsoft 365 auprès d’un bureau d’enregistrement de domaines.](../admin/get-help-with-domains/change-nameservers-at-any-domain-registrar.md)</span><span class="sxs-lookup"><span data-stu-id="afac7-136">If it doesn't, [Change nameservers to set up Microsoft 365 with any domain registrar](../admin/get-help-with-domains/change-nameservers-at-any-domain-registrar.md).</span></span> 

    - <span data-ttu-id="afac7-137">Si vous avez des enregistrements DNS existants (par exemple, un site web existant), mais que votre hôte DNS est activé pour [connexion de domaine](/office365/admin/get-help-with-domains/domain-connect), sélectionnez **Ajouter des enregistrements pour moi**.</span><span class="sxs-lookup"><span data-stu-id="afac7-137">If you have existing DNS records, for example an existing web site, but your DNS host is enabled for [domain connect](/office365/admin/get-help-with-domains/domain-connect), choose **Add records for me**.</span></span> <span data-ttu-id="afac7-138">Sur la page **sélectionnez votre services en ligne**, acceptez toutes les valeurs par défaut, puis sélectionnez **Suivant**, puis sélectionnez **Autoriser** sur la page de votre hôte DNS.</span><span class="sxs-lookup"><span data-stu-id="afac7-138">On the **Choose your online services** page, accept all the defaults, and choose **Next**, and choose **Authorize** on your DNS host's page.</span></span>
    - <span data-ttu-id="afac7-p108">Si vous avez des enregistrements DNS existants avec d'autres hôtes DNS (non activés pour la connexion de domaine), vous devrez gérer vos propres enregistrements DNS pour vous assurer que les services existants restent connectés. [Voir les bases du domaine pour plus d'informations](/office365/admin/get-help-with-domains/dns-basics).</span><span class="sxs-lookup"><span data-stu-id="afac7-p108">If you have existing DNS records with other DNS hosts (not enabled for domain connect), you'll want to manage your own DNS records to make sure the existing services stay connected. See [domain basics](/office365/admin/get-help-with-domains/dns-basics) for more info.</span></span>

        ![Page Activer les enregistrements.](../media/activaterecords.png)

2. <span data-ttu-id="afac7-142">Suivez les étapes de l’Assistant, et la messagerie électronique et d’autres services sont configurés pour vous.</span><span class="sxs-lookup"><span data-stu-id="afac7-142">Follow the steps in the wizard and email and other services will be set up for you.</span></span>

### <a name="protect-your-organization"></a><span data-ttu-id="afac7-143">Protéger votre organisation</span><span class="sxs-lookup"><span data-stu-id="afac7-143">Protect your organization</span></span> 

<span data-ttu-id="afac7-144">Les stratégies que vous avez définies dans l’Assistant sont appliquées automatiquement à un groupe [de sécurité](/office365/admin/create-groups/compare-groups#security-groups) appelé Tous *les utilisateurs.*</span><span class="sxs-lookup"><span data-stu-id="afac7-144">The policies you set up in the wizard are applied automatically to a [Security group](/office365/admin/create-groups/compare-groups#security-groups) called *All Users*.</span></span> <span data-ttu-id="afac7-145">Vous pouvez également créer des groupes supplémentaires pour attribuer des stratégies dans le Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="afac7-145">You can also create additional groups to assign policies to in the admin center.</span></span>

1. <span data-ttu-id="afac7-146">Dans l’option Augmenter la protection contre les **cybermenaces** avancées, il est recommandé d’accepter les valeurs par défaut pour laisser Office 365 Les fichiers et les liens de la [Protection](../security/office-365-security/defender-for-office-365.md) avancée contre les menaces peuvent être Office applications.</span><span class="sxs-lookup"><span data-stu-id="afac7-146">On the **Increase protection from advanced cyber threats**, it is recommended that you accept the defaults to let [Office 365 Advance Threat Protection](../security/office-365-security/defender-for-office-365.md) scan files and links in Office apps.</span></span>

    ![Capture d’écran de la page Augmenter la protection.](../media/increasetreatprotection.png)


2. <span data-ttu-id="afac7-148">Dans la page Empêcher les fuites de données **sensibles,** acceptez les valeurs par défaut pour activer la protection contre la perte de données Office 365 (DLP) pour suivre les données sensibles dans les applications Office et empêcher le partage accidentel de ces données à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="afac7-148">On the **Prevent leaks of sensitive data** page, accept the defaults to turn on Office 365 Data Loss Prevention (DLP) to track sensitive data in Office apps and prevent the accidental sharing of these outside your organization.</span></span>

3. <span data-ttu-id="afac7-149">Dans la page Protéger les données **dans Office** pour appareils mobiles, laissez la gestion des applications mobiles en place, développez les paramètres et examinez-les, puis sélectionnez Créer une stratégie de gestion des applications **mobiles.**</span><span class="sxs-lookup"><span data-stu-id="afac7-149">On the **Protect data in Office for mobile** page, leave mobile app management on, expand the settings and review them, and then select **Create mobile app management policy**.</span></span>

    ![Capture d’écran de La protection des Office pour la page mobile.](../media/protectdatainmobile.png)


## <a name="secure-windows-10-pcs"></a><span data-ttu-id="afac7-151">Sécuriser les PC Windows 10</span><span class="sxs-lookup"><span data-stu-id="afac7-151">Secure Windows 10 PCs</span></span>

<span data-ttu-id="afac7-152">Dans le navigation de gauche, sélectionnez **Installation,** puis, sous Se connectez **et sécurité,** sélectionnez Sécuriser **Windows 10 ordinateurs.**</span><span class="sxs-lookup"><span data-stu-id="afac7-152">On the left nav, select **Setup** and then, under **Sign-in and security**, choose **Secure your Windows 10 computers**.</span></span> <span data-ttu-id="afac7-153">Choose **View** to get started.</span><span class="sxs-lookup"><span data-stu-id="afac7-153">Choose **View** to get started.</span></span> <span data-ttu-id="afac7-154">Pour obtenir des instructions [complètes, Windows 10 vos ordinateurs](secure-win-10-pcs.md) de sécurité.</span><span class="sxs-lookup"><span data-stu-id="afac7-154">See [secure your Windows 10 computers](secure-win-10-pcs.md) for complete instructions.</span></span>

## <a name="deploy-office-365-client-apps"></a><span data-ttu-id="afac7-155">Déployer Office 365 applications clientes</span><span class="sxs-lookup"><span data-stu-id="afac7-155">Deploy Office 365 client apps</span></span>

<span data-ttu-id="afac7-156">Si vous avez choisi d’installer automatiquement des applications Office lors de l’installation, elles s’installeront sur les appareils Windows 10 une fois que les utilisateurs se sont connectés à Azure AD à partir de leurs appareils Windows, à l’aide de leurs informations d’identification professionnelles.</span><span class="sxs-lookup"><span data-stu-id="afac7-156">If you chose to automatically install Office apps during setup, the apps will install on the Windows 10 devices once the users have signed in to Azure AD from their Windows devices, using their work credentials.</span></span>

<span data-ttu-id="afac7-157">Pour installer Office sur des appareils mobiles iOS ou Android, voir Configurer des appareils [mobiles pour Microsoft 365 Business Premium utilisateurs.](set-up-mobile-devices.md)</span><span class="sxs-lookup"><span data-stu-id="afac7-157">To install Office on mobile iOS or Android devices, see [Set up mobile devices for Microsoft 365 Business Premium users](set-up-mobile-devices.md).</span></span>

<span data-ttu-id="afac7-158">Vous pouvez également installer Office individuellement.</span><span class="sxs-lookup"><span data-stu-id="afac7-158">You can also install Office individually.</span></span> <span data-ttu-id="afac7-159">Pour [plus d’Office, voir](https://support.microsoft.com/office/4414eaaf-0478-48be-9c42-23adc4716658) l’installation sur un PC ou Mac.</span><span class="sxs-lookup"><span data-stu-id="afac7-159">See [install Office on a PC or Mac](https://support.microsoft.com/office/4414eaaf-0478-48be-9c42-23adc4716658) for instructions.</span></span>

## <a name="related-content"></a><span data-ttu-id="afac7-160">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="afac7-160">Related content</span></span>

<span data-ttu-id="afac7-161">[Microsoft 365 vidéos de formation pour les entreprises](../business-video/index.yml) (page de liens)</span><span class="sxs-lookup"><span data-stu-id="afac7-161">[Microsoft 365 for business training videos](../business-video/index.yml) (link page)</span></span>
