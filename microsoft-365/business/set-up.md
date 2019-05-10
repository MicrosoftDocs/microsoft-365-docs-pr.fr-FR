---
title: Configurer Microsoft 365 Business
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: article
f1_keywords:
- O365E_M365SetupBanner
- BCS365_M365SetupBanner
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MSB365
search.appverid:
- BCS160
- MET150
ms.assetid: 6e7a2dfd-8ec4-4eb7-8390-3ee103e5fece
description: Découvrez comment configurer Microsoft 365 Business.
ms.openlocfilehash: e635b828609fc47cd8b92bb179a25bcc43cb0a1a
ms.sourcegitcommit: db1dfb2df2c2f7beced3b57bc772d106c189e88a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "33660776"
---
# <a name="set-up-microsoft-365-business"></a><span data-ttu-id="b46a5-103">Configurer Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="b46a5-103">Set up Microsoft 365 Business</span></span>

<span data-ttu-id="b46a5-104">Avant de commencer, reportez-vous à la rubrique obtenir les détails de l’inscription de [Microsoft 365 Business](get-microsoft-365-business.md) .</span><span class="sxs-lookup"><span data-stu-id="b46a5-104">Before you get started, see [Get Microsoft 365 Business](get-microsoft-365-business.md) for sign-up details.</span></span>

<span data-ttu-id="b46a5-105">Visionnez une [courte vidéo sur la configuration de Microsoft 365 Business](https://support.office.com/article/38003e30-9d10-44cf-b596-f1b5f662bfa1) à l’aide de l’Assistant de configuration et lorsque vous n’avez pas d’Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="b46a5-105">Watch a [short video on how to set up Microsoft 365 Business](https://support.office.com/article/38003e30-9d10-44cf-b596-f1b5f662bfa1) by using the set up wizard, and when you don't have an on-premises Active Directory</span></span>
  

## <a name="overview"></a><span data-ttu-id="b46a5-106">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="b46a5-106">Overview</span></span>

<span data-ttu-id="b46a5-107">La plupart des étapes de configuration peuvent être effectuées dans l’Assistant Installation, mais les autres options sont également répertoriées.</span><span class="sxs-lookup"><span data-stu-id="b46a5-107">Most of the set up steps can be done in the setup wizard, but the other options are also listed.</span></span>

1. <span data-ttu-id="b46a5-108">[Ajouter votre domaine](#add-your-domain-to-personalize-sign-in) (si vous avez acheté votre domaine lors de l' [inscription](sign-up.md), cette étape est déjà terminée).</span><span class="sxs-lookup"><span data-stu-id="b46a5-108">[Add your domain](#add-your-domain-to-personalize-sign-in) (if you bought your domain during [sign up](sign-up.md), this step is already done.)</span></span>
2. <span data-ttu-id="b46a5-109">Ajouter des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b46a5-109">Add users.</span></span> <span data-ttu-id="b46a5-110">Pour ce faire, vous pouvez procéder de l’une des manières suivantes:</span><span class="sxs-lookup"><span data-stu-id="b46a5-110">You can do this in any of the three ways:</span></span>
    - <span data-ttu-id="b46a5-111">Dans l' [Assistant Installation](#add-users-in-the-wizard).</span><span class="sxs-lookup"><span data-stu-id="b46a5-111">In the [setup wizard](#add-users-in-the-wizard).</span></span>
    - <span data-ttu-id="b46a5-112">Utilisez la synchronisation d’annuaires pour [Ajouter des utilisateurs à l’aide d’Azure ad Connect](#add-users-by-using-azure-ad-connect) si vous disposez d’un annuaire Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="b46a5-112">Use directory synchronization to [add users by using Azure AD Connect](#add-users-by-using-azure-ad-connect) if you have an on-premises Active directory.</span></span>
    - <span data-ttu-id="b46a5-113">Vous pouvez également [Ajouter des utilisateurs ultérieurement](add-users-m365b.md) dans le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="b46a5-113">You can also [add users later](add-users-m365b.md) in the admin center.</span></span>
3. <span data-ttu-id="b46a5-114">Configurez les stratégies de sécurité et configurez les appareils.</span><span class="sxs-lookup"><span data-stu-id="b46a5-114">Set up security policies and configure devices.</span></span> <span data-ttu-id="b46a5-115">Pour ce faire, vous pouvez procéder de l’une des manières suivantes:</span><span class="sxs-lookup"><span data-stu-id="b46a5-115">You can do this in any of the three ways:</span></span>
    - <span data-ttu-id="b46a5-116">Dans l' [Assistant Installation](#set-up-policies-in-the-wizard).</span><span class="sxs-lookup"><span data-stu-id="b46a5-116">In the [setup wizard](#set-up-policies-in-the-wizard).</span></span>  
    - <span data-ttu-id="b46a5-117">Dans le [Centre d’administration](#modify-or-add-policies-in-the-admin-center).</span><span class="sxs-lookup"><span data-stu-id="b46a5-117">In the [admin center](#modify-or-add-policies-in-the-admin-center).</span></span>
    - <span data-ttu-id="b46a5-118">Dans le [Centre d’administration Intune](https://docs.microsoft.com/intune/what-is-device-management).</span><span class="sxs-lookup"><span data-stu-id="b46a5-118">In the [Intune admin center](https://docs.microsoft.com/intune/what-is-device-management).</span></span>
4. <span data-ttu-id="b46a5-119">Configurez et gérez les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b46a5-119">Set up and manage Windows 10 devices.</span></span>

    <span data-ttu-id="b46a5-120">Lorsque vous joignez un appareil WIndows 10 à Azure AD, toutes les stratégies sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="b46a5-120">When you join a WIndows 10 device to Azure AD, all the policies get applied to it.</span></span>
    - <span data-ttu-id="b46a5-121">Configurez les configurations des appareils Windows 10 dans l' [Assistant Installation](#set-up-policies-in-the-wizard).</span><span class="sxs-lookup"><span data-stu-id="b46a5-121">Set up Windows 10 device configurations in the [setup wizard](#set-up-policies-in-the-wizard).</span></span>
    - <span data-ttu-id="b46a5-122">Rejoignez un [nouveau périphérique Windows 10](set-up-windows-devices.md#for-a-brand-new-or-newly-upgraded-windows-10-pro-device) à Azure ad.</span><span class="sxs-lookup"><span data-stu-id="b46a5-122">Join a [new Windows 10 device](set-up-windows-devices.md#for-a-brand-new-or-newly-upgraded-windows-10-pro-device) to Azure AD.</span></span>
    - <span data-ttu-id="b46a5-123">Associez un [appareil Windows 10](set-up-windows-devices.md#for-a-device-already-set-up-and-running-windows-10-pro) à Azure ad.</span><span class="sxs-lookup"><span data-stu-id="b46a5-123">Join an [existing Windows 10 device](set-up-windows-devices.md#for-a-device-already-set-up-and-running-windows-10-pro) to Azure AD.</span></span>
1. <span data-ttu-id="b46a5-124">Installez Office 365 Business.</span><span class="sxs-lookup"><span data-stu-id="b46a5-124">Install Office 365 Business.</span></span>
    - <span data-ttu-id="b46a5-125">Vous pouvez installer automatiquement Office sur les appareils Windows à l’aide de l' [Assistant Installation](#set-up-policies-in-the-wizard).</span><span class="sxs-lookup"><span data-stu-id="b46a5-125">You can automatically install Office in the Windows devices by using the [setup wizard](#set-up-policies-in-the-wizard).</span></span>
    - <span data-ttu-id="b46a5-126">[Installer automatiquement Office](auto-install-or-uninstall-office.md) à partir du centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="b46a5-126">Automatically [install Office](auto-install-or-uninstall-office.md) from the admin center.</span></span>
    - <span data-ttu-id="b46a5-127">Autorisez les utilisateurs à [installer les applications Office](https://docs.microsoft.com/office365/admin/setup/install-applications) pour Windows et les appareils.</span><span class="sxs-lookup"><span data-stu-id="b46a5-127">Let users [install Office apps](https://docs.microsoft.com/office365/admin/setup/install-applications) for Windows and devices.</span></span>
     
1. <span data-ttu-id="b46a5-128">Configurez une sécurité supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="b46a5-128">Set up additional security.</span></span>
    - <span data-ttu-id="b46a5-129">L’Assistant installation ajoute des stratégies pour sécuriser vos appareils, mais vous pouvez également tirer parti de fonctionnalités de [sécurité supplémentaires](#additional-security-settings) pour sécuriser vos données, vos comptes et vos e-mails.</span><span class="sxs-lookup"><span data-stu-id="b46a5-129">The setup wizard adds policies to secure your devices, but you can also take advantage of [additional security](#additional-security-settings) capabilities to helps secure your data, accounts, and emails.</span></span> 

## <a name="add-your-domain-users-and-set-up-policies"></a><span data-ttu-id="b46a5-130">Ajouter votre domaine, vos utilisateurs et configurer des stratégies</span><span class="sxs-lookup"><span data-stu-id="b46a5-130">Add your domain, users and set up policies</span></span>

![Bannière pointant vers https://aka.ms/aboutM365preview.](media/m365admincenterchanging.png)

<span data-ttu-id="b46a5-132">Lorsque vous achetez Microsoft 365 Business, vous avez la possibilité d’utiliser un domaine que vous possédez ou d’en acheter un lors de l' [inscription](sign-up.md).</span><span class="sxs-lookup"><span data-stu-id="b46a5-132">When you purchase Microsoft 365 Business, you have the option of using a domain you own, or buying one during the [sign-up](sign-up.md).</span></span>

- <span data-ttu-id="b46a5-133">Si vous avez acheté un nouveau domaine lorsque vous vous êtes inscrit, votre domaine est configuré et vous pouvez le déplacer pour [Ajouter des utilisateurs et attribuer des licences](#add-users-and-assign-licenses).</span><span class="sxs-lookup"><span data-stu-id="b46a5-133">If you purchased a new domain when you signed up, your domain is all set up and you can move to [Add users and assign licenses](#add-users-and-assign-licenses).</span></span>

### <a name="add-your-domain-to-personalize-sign-in"></a><span data-ttu-id="b46a5-134">Ajouter votre domaine pour personnaliser la connexion</span><span class="sxs-lookup"><span data-stu-id="b46a5-134">Add your domain to personalize sign-in</span></span>

1. <span data-ttu-id="b46a5-135">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide de vos informations d’identification d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="b46a5-135">Sign in to [Microsoft 365 admin center](https://admin.microsoft.com) by using your global admin credentials.</span></span> 

2. <span data-ttu-id="b46a5-136">Sélectionnez **Ajouter un domaine** pour démarrer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="b46a5-136">Choose **Add a domain** to start the wizard.</span></span>

    ![Sélectionnez Ajouter un domaine.](media/addadomainadmincenter.png)
    
3. <span data-ttu-id="b46a5-138">Dans l’Assistant, entrez le nom de domaine que vous souhaitez utiliser (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="b46a5-138">In the wizard, enter the domain name you want to use (like contoso.com).</span></span>


    ![Capture d’écran de la page Personnalisez votre connexion.](media/personalizesignin.png)

    
4. <span data-ttu-id="b46a5-140">Suivez les étapes de l’Assistant pour [créer des enregistrements DNS auprès d’un fournisseur d’hébergement DNS pour Office 365](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) qui vérifie que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="b46a5-140">Follow the steps in the wizard to [Create DNS records at any DNS hosting provider for Office 365](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) that verifies you own the domain.</span></span> <span data-ttu-id="b46a5-141">Si vous êtes conscient de votre hôte de domaine, reportez-vous aux [instructions spécifiques](https://docs.microsoft.com/office365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions)de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="b46a5-141">If you know your domain host, see also the [host specific instructions](https://docs.microsoft.com/office365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions).</span></span>

    <span data-ttu-id="b46a5-142">Si votre fournisseur d’hébergement est GoDaddy, le processus est facile et vous êtes automatiquement invité à vous connecter et à permettre à Microsoft de s’authentifier à votre place:</span><span class="sxs-lookup"><span data-stu-id="b46a5-142">If your hosting provider is GoDaddy, the process is easy and you will be automatically asked to sign in and let Microsoft authenticate on your behalf:</span></span>

    ![Sur GoDaddy, sélectionnez Autoriser.](media/godaddyauth.png)

### <a name="add-users-and-assign-licenses"></a><span data-ttu-id="b46a5-144">Ajouter des utilisateurs et attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="b46a5-144">Add users and assign licenses</span></span>

<span data-ttu-id="b46a5-145">Vous pouvez ajouter des utilisateurs dans l’Assistant, mais vous pouvez également [Ajouter des utilisateurs ultérieurement](add-users-m365b.md) dans le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="b46a5-145">You can add users in the wizard, but you can also [add users later](add-users-m365b.md) in the admin center.</span></span> <span data-ttu-id="b46a5-146">En outre, si vous disposez d’un contrôleur de domaine local, vous pouvez ajouter des utilisateurs avec [Azure ad Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express).</span><span class="sxs-lookup"><span data-stu-id="b46a5-146">Additionally, if you have a local domain controller, you can add users with [Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express).</span></span>

#### <a name="add-users-in-the-wizard"></a><span data-ttu-id="b46a5-147">Ajouter des utilisateurs dans l’Assistant</span><span class="sxs-lookup"><span data-stu-id="b46a5-147">Add users in the wizard</span></span>

<span data-ttu-id="b46a5-148">Tous les utilisateurs que vous ajoutez dans l’Assistant reçoivent automatiquement une licence d’entreprise Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b46a5-148">Any users you add in the wizard get automatically assigned a Microsoft 365 Business license.</span></span>
<span data-ttu-id="b46a5-149">Si vous disposez d’un contrôleur de domaine local et que vous utilisez Active Directory, voir [How to DDD Users by using Azure ad Connect](#add-users-by-using-azure-ad-connect).</span><span class="sxs-lookup"><span data-stu-id="b46a5-149">If you have a local domain controller, and are using Active Directory, see [how to ddd users by using Azure AD Connect](#add-users-by-using-azure-ad-connect).</span></span>

![Capture d’écran de la page Ajouter de nouveaux utilisateurs dans l’Assistant](media/addnewuserspage.png)

1. <span data-ttu-id="b46a5-p106">Si votre abonnement Microsoft 365 Entreprise est associé à des utilisateurs existants (par exemple, si vous utilisiez Azure AD Connect), vous avez la possibilité de leur attribuer des licences à ce stade. Poursuivez et ajoutez des licences pour eux aussi.</span><span class="sxs-lookup"><span data-stu-id="b46a5-p106">If your Microsoft 365 Business subscription has existing users (for example, if you used Azure AD Connect) , you will get an option to assign licenses to them now. Go ahead and add licenses to them as well.</span></span>

3. <span data-ttu-id="b46a5-153">Une fois que vous avez ajouté les utilisateurs, vous pouvez également partager les informations d’identification avec les nouveaux utilisateurs que vous avez ajoutés.</span><span class="sxs-lookup"><span data-stu-id="b46a5-153">After you have added the users, you will also get an option to share credentials with the new users you added.</span></span> <span data-ttu-id="b46a5-154">Vous pouvez choisir de les imprimer, de les envoyer par e-mail ou de les télécharger.</span><span class="sxs-lookup"><span data-stu-id="b46a5-154">You can choose to print them out, email them, or download them.</span></span>

4. <span data-ttu-id="b46a5-155">Ignorez la migration des messages e-mail et sélectionnez **Suivant** dans la page **Migrer les messages e-mail**.</span><span class="sxs-lookup"><span data-stu-id="b46a5-155">Skip migrating email messages and choose **Next** on **Migrate email messages** page.</span></span> 

    <span data-ttu-id="b46a5-156">Si vous effectuez une migration à partir d’un autre fournisseur de courrier et que vous souhaitez copier vos données ultérieurement, vous pouvez migrer le [courrier électronique et les contacts vers Office 365](https://support.office.com/article/a3e3bddb-582e-4133-8670-e61b9f58627e).</span><span class="sxs-lookup"><span data-stu-id="b46a5-156">If you are moving from another email provider and want to copy your data later, you can [Migrate email and contacts to Office 365](https://support.office.com/article/a3e3bddb-582e-4133-8670-e61b9f58627e).</span></span>

#### <a name="add-users-by-using-azure-ad-connect"></a><span data-ttu-id="b46a5-157">Ajouter des utilisateurs à l’aide d’Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="b46a5-157">Add users by using Azure AD Connect</span></span>

 <span data-ttu-id="b46a5-158">Si vous disposez d’un contrôleur de domaine local avec Active Directory, vous synchronisez vos utilisateurs avec Microsoft 365 Business à l’aide d' [Azure ad Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express).</span><span class="sxs-lookup"><span data-stu-id="b46a5-158">If you have a local domain controller with Active Directory, you synchronize your users with Microsoft 365 Business by using [Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express).</span></span> <span data-ttu-id="b46a5-159">Effectuez cette opération avant de démarrer l’Assistant installation.</span><span class="sxs-lookup"><span data-stu-id="b46a5-159">Complete this before you start the setup wizard.</span></span> <span data-ttu-id="b46a5-160">Vous pouvez le télécharger dans le centre d’administration:</span><span class="sxs-lookup"><span data-stu-id="b46a5-160">You can download it in the admin center:</span></span>

- <span data-ttu-id="b46a5-161">Accédez à \*\*\*\* \> utilisateurs **actifs utilisateurs**, sélectionnez les ellipses en haut de la page, puis sélectionnez **synchronisation d’annuaires** pour télécharger Azure ad Connect.</span><span class="sxs-lookup"><span data-stu-id="b46a5-161">Go to **Users** \> **Active users**, select the ellipses on the top of the page and then select **Directory synchronization** to download Azure AD Connect.</span></span>

    ![Sur la page utilisateurs actifs, sélectionnez ellipses > Directory snchronization.](media/setupdirsync.png)

    > [!IMPORTANT]
    > <span data-ttu-id="b46a5-163">Si vous créez des utilisateurs de cette manière, vous devrez toujours leur attribuer des licences dans le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="b46a5-163">If you create users this way, you will still have to assign licenses to them in the admin center.</span></span>

##### <a name="continue-to-access-domain-joined-apps-and-devices"></a><span data-ttu-id="b46a5-164">Continuer à accéder aux applications et aux appareils joints au domaine</span><span class="sxs-lookup"><span data-stu-id="b46a5-164">Continue to access domain-joined apps and devices</span></span>

<span data-ttu-id="b46a5-165">Si vous souhaitez continuer à accéder aux applications et aux appareils joints par le domaine, lisez les articles suivants pour les deux façons d’activer ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="b46a5-165">If you want to continue to access domain-joined apps and devices, read the following articles for two different way of enabling that:</span></span>
  
- [<span data-ttu-id="b46a5-166">Activer la gestion des appareils Windows 10 associés à un domaine par Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="b46a5-166">Enable domain-joined Windows 10 devices to be managed by Microsoft 365 Business</span></span>](manage-windows-devices.md)
    - <span data-ttu-id="b46a5-167">Il s’agit de la méthode recommandée.</span><span class="sxs-lookup"><span data-stu-id="b46a5-167">This is the recommended way.</span></span>

- [<span data-ttu-id="b46a5-168">Accéder aux ressources locales à partir d’un appareil joint à Azure AD dans Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="b46a5-168">Access on-premises resources from an Azure AD-joined device in Microsoft 365 Business</span></span>](access-resources.md)

### <a name="connect-your-domain"></a><span data-ttu-id="b46a5-169">Sélectionner votre domaine</span><span class="sxs-lookup"><span data-stu-id="b46a5-169">Connect your domain</span></span>

> [!NOTE]
> <span data-ttu-id="b46a5-170">Si vous avez choisi d’utiliser le domaine. onmicrosoft ou si vous avez utilisé Azure AD Connect pour configurer des utilisateurs, vous ne verrez pas cette étape.</span><span class="sxs-lookup"><span data-stu-id="b46a5-170">If you chose to use the .onmicrosoft domain, or used Azure AD Connect to set up users, you will not see this step.</span></span>
  
<span data-ttu-id="b46a5-171">Pour configurer des services, vous devez mettre à jour des enregistrements au niveau de votre hôte DNS ou de votre bureau d'enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="b46a5-171">To set up services, you have to update some records at your DNS host or domain registrar.</span></span>
  
1. <span data-ttu-id="b46a5-172">L'Assistant Configuration détecte généralement votre bureau d'enregistrement et vous fournit un lien vers des instructions détaillées vous permettant de mettre à jour vos enregistrements NS sur le site web du bureau d'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b46a5-172">The setup wizard typically detects your registrar and gives you a link to step-by-step instructions for updating your NS records at the registrar website.</span></span> <span data-ttu-id="b46a5-173">Si ce n’est pas le cas, [Modifiez les serveurs de noms pour configurer Office 365 avec n’importe quel](https://support.office.com/article/a8b487a9-2a45-4581-9dc4-5d28a47010a2)Bureau d’enregistrement de domaine.</span><span class="sxs-lookup"><span data-stu-id="b46a5-173">If it doesn't, [Change nameservers to set up Office 365 with any domain registrar](https://support.office.com/article/a8b487a9-2a45-4581-9dc4-5d28a47010a2).</span></span> 

    - <span data-ttu-id="b46a5-174">Si vous avez des enregistrements DNS existants, par exemple un site Web existant, vous devez gérer vos propres enregistrements DNS pour vous assurer que les services existants restent connectés.</span><span class="sxs-lookup"><span data-stu-id="b46a5-174">If you have existing DNS records, for example an existing web site, you will want to manage your own DNS records to make sure the existing services stay connected.</span></span> <span data-ttu-id="b46a5-175">Pour plus d’informations, voir [notions de base](https://docs.microsoft.com/office365/admin/get-help-with-domains/dns-basics) sur le domaine.</span><span class="sxs-lookup"><span data-stu-id="b46a5-175">See [domain basics](https://docs.microsoft.com/office365/admin/get-help-with-domains/dns-basics) for more info.</span></span>

        ![Connecter votre page de domaine avec je vais gérer mes propres enregistrements DNS.](media/connectyourdomainpage.png)

2. <span data-ttu-id="b46a5-177">Suivez les étapes de l’Assistant et de la messagerie et d’autres services sont configurés pour vous.</span><span class="sxs-lookup"><span data-stu-id="b46a5-177">Follow the steps in the wizard and email and other services will be set up for you.</span></span>

### <a name="set-up-security-policies-and-device-configurations"></a><span data-ttu-id="b46a5-178">Configurer les stratégies de sécurité et les configurations des appareils</span><span class="sxs-lookup"><span data-stu-id="b46a5-178">Set up security policies and device configurations</span></span> 

<span data-ttu-id="b46a5-179">Ces stratégies s’appliquent à tous les utilisateurs auxquels vous octroyez une licence, ou à un groupe d’utilisateurs si vous décidez d’affecter des stratégies différentes à un ensemble d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b46a5-179">These policies apply to every user you give a license to, or to a group of users if you decide to assign different policies to a set of users.</span></span>

#### <a name="set-up-policies-in-the-wizard"></a><span data-ttu-id="b46a5-180">Configurer des stratégies dans l’Assistant</span><span class="sxs-lookup"><span data-stu-id="b46a5-180">Set up policies in the wizard</span></span>

<span data-ttu-id="b46a5-181">Les stratégies que vous configurez dans l’Assistant sont appliquées automatiquement à un [groupe de sécurité](https://docs.microsoft.com/office365/admin/create-groups/compare-groups#security-groups) appelé *tous les utilisateurs*.</span><span class="sxs-lookup"><span data-stu-id="b46a5-181">The policies you set up in the wizard are applied automatically to a [Security group](https://docs.microsoft.com/office365/admin/create-groups/compare-groups#security-groups) called *All Users*.</span></span>

1. <span data-ttu-id="b46a5-182">Dans la case à cocher **protéger vos fichiers professionnels sur les appareils mobiles** , l’option **protéger les fichiers de travail lorsque les appareils sont perdus ou volés** est sélectionnée par défaut.</span><span class="sxs-lookup"><span data-stu-id="b46a5-182">On the **Protect your work files on mobile devices** the option **Protect work files when devices are lost or stolen** is selected by default.</span></span> <span data-ttu-id="b46a5-183">Vous avez la possibilité d’activer **la gestion de la manière dont les utilisateurs accèdent aux fichiers Office sur les appareils mobiles**, ce qui est recommandé.</span><span class="sxs-lookup"><span data-stu-id="b46a5-183">You have an option to turn on **Manage how users access Office files on mobile devices**, and this is recommended.</span></span>

    ![Capture d’écran de la page protéger les fichiers de travail sur les appareils mobiles.](media/protectworkfilesondevices.png)

     - <span data-ttu-id="b46a5-185">Si vous développez **protéger les fichiers de travail en cas de perte ou de vol des appareils**, les [valeurs par défaut](protect-work-files-on-lost-or-stolen-device.md) sont présélectionnées:</span><span class="sxs-lookup"><span data-stu-id="b46a5-185">If you expand **Protect work files when devices are lost or stolen**, the [default values](protect-work-files-on-lost-or-stolen-device.md) are pre-selected:</span></span>

        ![Capture d’écran des valeurs par défaut pour la protection des fichiers sur les appareils perdus.](media/protectworkfilesondevicesdefault.png)

    - <span data-ttu-id="b46a5-187">Si vous sélectionnez **gérer la manière dont les utilisateurs accèdent aux fichiers Office sur les appareils mobiles** et les développer, les [valeurs par défaut](manage-user-access-on-mobile-devices.md) sont affichées.</span><span class="sxs-lookup"><span data-stu-id="b46a5-187">If you select **Manage how users access Office files on mobile devices** and expand it, the [default values](manage-user-access-on-mobile-devices.md) are shown.</span></span> <span data-ttu-id="b46a5-188">Nous vous recommandons d'accepter les valeurs par défaut lors de l'installation pour créer des stratégies d'application pour Windows 10, iOS et Android qui s'appliquent à tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b46a5-188">We recommend you accept the default values during setup to create application policies for Android, iOS, and Windows 10 that apply to all users.</span></span> <span data-ttu-id="b46a5-189">Vous pouvez créer des stratégies supplémentaires une fois l'installation terminée.</span><span class="sxs-lookup"><span data-stu-id="b46a5-189">You can create more policies after setup completes.</span></span>

        ![Capture d’écran des paramètres de protection pour les fichiers Office sur mobile.](media/useraccessonmobile.png)

2. <span data-ttu-id="b46a5-191">La dernière étape sur la protection des données et des périphériques vous permet de configurer des stratégies pour sécuriser les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b46a5-191">The last step on protect data and devices allows you to set up policies to secure Windows 10 devices.</span></span> <span data-ttu-id="b46a5-192">Ces paramètres sont appliqués automatiquement lorsque le Windows 10 d’un utilisateur se connecte à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b46a5-192">These settings are applied automatically when a user's Windows 10 connects to your organization.</span></span> <span data-ttu-id="b46a5-193">Vous pouvez développer des **appareils Windows 10 sécurisés** pour afficher et modifier les [valeurs par défaut](secure-windows-10-devices.md).</span><span class="sxs-lookup"><span data-stu-id="b46a5-193">You can expand **Secure Windows 10 devices** to see and modify the [default values](secure-windows-10-devices.md).</span></span>
3. <span data-ttu-id="b46a5-194">Vous pouvez également choisir d' [installer automatiquement Office](install-office-on-windows-10-during-setup.md) sur les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b46a5-194">You can also choose to [automatically install Office](install-office-on-windows-10-during-setup.md) on Windows 10 devices.</span></span>

    ![Capture d’écran de la page définir la configuration de l’appareil Windows 10.](media/setwin10config.png)

#### <a name="modify-or-add-policies-in-the-admin-center"></a><span data-ttu-id="b46a5-196">Modifier ou ajouter des stratégies dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="b46a5-196">Modify or add policies in the admin center</span></span>

<span data-ttu-id="b46a5-197">Consultez la rubrique [Manage Microsoft 365 Business](manage.md) pour obtenir des liens vers des rubriques expliquant comment afficher et modifier des stratégies de protection des applications et des périphériques, et comment supprimer ou réinitialiser des appareils utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b46a5-197">See [manage Microsoft 365 Business](manage.md) for links to topics on how to view and modify device and app protection polices, and how to remove data from, or reset user devices.</span></span>

## <a name="deploy-and-manage-windows-10"></a><span data-ttu-id="b46a5-198">Déployer et gérer Windows 10</span><span class="sxs-lookup"><span data-stu-id="b46a5-198">Deploy and manage Windows 10</span></span>
<span data-ttu-id="b46a5-199">Consultez la rubrique [configurer les appareils Windows pour les utilisateurs professionnels de Microsoft 365](set-up-windows-devices.md) pour se connecter manuellement à Azure ad, soit lors de la configuration des nouveaux ordinateurs, soit en modifiant le profil de connexion pour les ordinateurs existants.</span><span class="sxs-lookup"><span data-stu-id="b46a5-199">See [Set up Windows devices for Microsoft 365 Business users](set-up-windows-devices.md) to manually connect to Azure AD, either during setup for new computers, or by changing sign-in profile for existing computers.</span></span> 

### <a name="use-autopilot-to-set-up-new-devices"></a><span data-ttu-id="b46a5-200">Utiliser AutoPilot pour configurer de nouveaux appareils</span><span class="sxs-lookup"><span data-stu-id="b46a5-200">Use Autopilot to set up new devices</span></span>

<span data-ttu-id="b46a5-201">Vous pouvez utiliser [Windows AutoPilot](add-autopilot-devices-and-profile.md) pour préconfigurer automatiquement les **nouveaux** appareils Windows 10 pour un utilisateur, mais il peut être plus facile d’obtenir un [partenaire](https://www.microsoft.com/solution-providers/search) qui peut le faire pour vous.</span><span class="sxs-lookup"><span data-stu-id="b46a5-201">You can use [Windows Autopilot](add-autopilot-devices-and-profile.md) to automatically pre-configure **new** Windows 10 devices for a user, but it might be easier to get a [partner](https://www.microsoft.com/solution-providers/search) who can do this for you.</span></span> <span data-ttu-id="b46a5-202">Vous pouvez également accéder à [Microsoft Store](https://go.microsoft.com/fwlink/?linkid=874598) et demander à un spécialiste de la technologie Cloud de configurer de nouveaux appareils que vous achetez pour vous.</span><span class="sxs-lookup"><span data-stu-id="b46a5-202">You can also go to [Microsoft Store](https://go.microsoft.com/fwlink/?linkid=874598) and ask a cloud technology expert set up new devices you purchase for you.</span></span>

### <a name="access-on-premises-resources"></a><span data-ttu-id="b46a5-203">Accéder aux ressources locales</span><span class="sxs-lookup"><span data-stu-id="b46a5-203">Access on-premises resources</span></span>

<span data-ttu-id="b46a5-204">Si votre organisation utilise Windows Server Active Directory en local, vous pouvez configurer Microsoft 365 entreprise pour protéger vos appareils Windows 10, tout en conservant l’accès aux ressources locales qui nécessitent une authentification locale.</span><span class="sxs-lookup"><span data-stu-id="b46a5-204">If your organization uses Windows Server Active Directory on-premises, you can set up Microsoft 365 Business to protect your Windows 10 devices, while still maintaining access to on-premises resources that require local authentication.</span></span> <span data-ttu-id="b46a5-205">Suivez les étapes de la procédure [activer les appareils Windows 10 appartenant à un domaine pour qu’ils soient gérés par Microsoft 365 Business](manage-windows-devices.md) pour le configurer.</span><span class="sxs-lookup"><span data-stu-id="b46a5-205">Follow the steps in [Enable domain-joined Windows 10 devices to be managed by Microsoft 365 Business](manage-windows-devices.md) to set this up.</span></span> <span data-ttu-id="b46a5-206">Il s’agit de la méthode préférée et les appareils dans cet État sont appelés appareils hybrides Azure AD.</span><span class="sxs-lookup"><span data-stu-id="b46a5-206">This is the preferred method and devices in this state are called Hybrid Azure AD joined devices.</span></span>

<span data-ttu-id="b46a5-207">Si votre entreprise dispose d’un annuaire local Active Directory qui contient certaines ressources locales (telles que des partages de fichiers et des imprimantes), vous pouvez donner à vos appareils joints à Azure AD l’accès à ces ressources en suivant les étapes ci-dessous: accéder à des [ressources locales à partir d’un Appareil rejoint Azure AD dans Microsoft 365 Business](access-resources.md).</span><span class="sxs-lookup"><span data-stu-id="b46a5-207">If your business has a local Active Directory that contains some on-premises resources (such as file shares and printers) , you can give your Azure AD-joined devices access to these resources by following the steps here: [Access on-premises resources from an Azure AD-joined device in Microsoft 365 Business](access-resources.md).</span></span>

## <a name="deploy-office-365-client-apps"></a><span data-ttu-id="b46a5-208">Déployer des applications clientes Office 365</span><span class="sxs-lookup"><span data-stu-id="b46a5-208">Deploy Office 365 client apps</span></span>

<span data-ttu-id="b46a5-209">Si vous avez choisi d’installer automatiquement les applications Office dans lors de la configuration, les applications s’installeront sur les appareils Windows 10 une fois que les utilisateurs se sont connectés à Azure AD à partir de leurs appareils Windows avec leurs informations d’identification professionnelles.</span><span class="sxs-lookup"><span data-stu-id="b46a5-209">If you chose to automatically install Office apps in during the set up, the apps will install on the Windows 10 devices once the users have signed in to Azure AD from their Windows devices with their work credentials.</span></span>
<span data-ttu-id="b46a5-210">Pour installer Office sur des appareils mobiles iOS ou Android, consultez la rubrique [configurer des appareils mobiles pour les utilisateurs professionnels de Microsoft 365](set-up-mobile-devices.md).</span><span class="sxs-lookup"><span data-stu-id="b46a5-210">To install Office on mobile iOS or Android devices, see [Set up mobile devices for Microsoft 365 Business users](set-up-mobile-devices.md).</span></span>

<span data-ttu-id="b46a5-211">Vous pouvez également installer Office individuellement.</span><span class="sxs-lookup"><span data-stu-id="b46a5-211">You can also install Office individually.</span></span> <span data-ttu-id="b46a5-212">Pour obtenir des instructions, voir [installer Office sur un PC ou un Mac](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc471665) .</span><span class="sxs-lookup"><span data-stu-id="b46a5-212">See [install Office on a PC or Mac](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc471665) for instructions.</span></span>

## <a name="additional-security-settings"></a><span data-ttu-id="b46a5-213">Paramètres de sécurité supplémentaires</span><span class="sxs-lookup"><span data-stu-id="b46a5-213">Additional security settings</span></span>

<span data-ttu-id="b46a5-214">Outre le paramètre de sécurité et de conformité dans l’Assistant Installation, vous pouvez également configurer les paramètres supplémentaires suivants:</span><span class="sxs-lookup"><span data-stu-id="b46a5-214">In addition to the security and compliance setting in the setup wizard, you can also set up the following additional settings:</span></span>
  
- <span data-ttu-id="b46a5-215">**Protection contre les programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="b46a5-215">**Email malware protection**</span></span>
- <span data-ttu-id="b46a5-216">**Pièces jointes sûres de protection avancée contre les menaces**</span><span class="sxs-lookup"><span data-stu-id="b46a5-216">**Advanced Threat Protection (ATP) Safe Attachments**</span></span>
- <span data-ttu-id="b46a5-217">**Liens fiables ATP**</span><span class="sxs-lookup"><span data-stu-id="b46a5-217">**ATP Safe Links**</span></span>
- <span data-ttu-id="b46a5-218">**Protection contre le hameçonnage APT**</span><span class="sxs-lookup"><span data-stu-id="b46a5-218">**APT anti-phishing**</span></span>
- <span data-ttu-id="b46a5-219">**Archivage Exchange Online**</span><span class="sxs-lookup"><span data-stu-id="b46a5-219">**Exchange Online Archiving**</span></span>
- <span data-ttu-id="b46a5-220">**Protection contre la perte de données (DLP)**</span><span class="sxs-lookup"><span data-stu-id="b46a5-220">**Data loss prevention (DLP)**</span></span>
- <span data-ttu-id="b46a5-221">**Azure information protection** (Plan 1)</span><span class="sxs-lookup"><span data-stu-id="b46a5-221">**Azure Information Protection** (Plan 1)</span></span>
- <span data-ttu-id="b46a5-222">**Disponibilité du portail Intune**</span><span class="sxs-lookup"><span data-stu-id="b46a5-222">**Intune portal availability**</span></span>

<span data-ttu-id="b46a5-223">Pour commencer, consultez la rubrique [configurer des stratégies de sécurité avancées](set-up-advanced-security.md).</span><span class="sxs-lookup"><span data-stu-id="b46a5-223">To get started see, [set up advanced security policies](set-up-advanced-security.md).</span></span>

<span data-ttu-id="b46a5-224">Consultez également les [10 meilleures façons de sécuriser votre entreprise Microsoft 365](https://docs.microsoft.com/office365/admin/security-and-compliance/secure-your-business-data) pour obtenir une feuille de route des meilleures pratiques en matière de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b46a5-224">See also [top 10 ways to secure your Microsoft 365 Business](https://docs.microsoft.com/office365/admin/security-and-compliance/secure-your-business-data) for a roadmap of best security practices.</span></span>