---
title: Configurer Microsoft 365 Business
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
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MSB365
search.appverid:
- BCS160
- MET150
ms.assetid: 6e7a2dfd-8ec4-4eb7-8390-3ee103e5fece
description: Découvrez comment configurer Microsoft 365 Business.
ms.openlocfilehash: dbd2e740c85f52d3f43e6cd3d6ce45c478a9b1a9
ms.sourcegitcommit: 7690c8bfdea6e6d245cfa7c5b09b913b092cde0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/23/2019
ms.locfileid: "37121315"
---
# <a name="set-up-microsoft-365-business-in-the-setup-wizard"></a><span data-ttu-id="412b8-103">Configurer Microsoft 365 entreprise dans l’Assistant Installation</span><span class="sxs-lookup"><span data-stu-id="412b8-103">Set up Microsoft 365 Business in the setup wizard</span></span>

## <a name="add-your-domain-users-and-set-up-policies"></a><span data-ttu-id="412b8-104">Ajouter votre domaine, vos utilisateurs et configurer des stratégies</span><span class="sxs-lookup"><span data-stu-id="412b8-104">Add your domain, users, and set up policies</span></span>

<span data-ttu-id="412b8-105">[![Étiquette pour vous informer le centre d’administration change et vous trouverez plus de détails sur aka.ms/aboutM365preview.](media/m365admincenterchanging.png)](https://docs.microsoft.com/office365/admin/microsoft-365-admin-center-preview)</span><span class="sxs-lookup"><span data-stu-id="412b8-105">[![Label to let you know the admin center is changing and you can find more details at aka.ms/aboutM365preview.](media/m365admincenterchanging.png)](https://docs.microsoft.com/office365/admin/microsoft-365-admin-center-preview)</span></span>

<span data-ttu-id="412b8-106">Lorsque vous achetez Microsoft 365 Business, vous avez la possibilité d’utiliser un domaine que vous possédez ou d’en acheter un lors de l' [inscription](sign-up.md).</span><span class="sxs-lookup"><span data-stu-id="412b8-106">When you purchase Microsoft 365 Business, you have the option of using a domain you own, or buying one during the [sign-up](sign-up.md).</span></span>

- <span data-ttu-id="412b8-107">Si vous avez acheté un nouveau domaine lorsque vous vous êtes inscrit, votre domaine est configuré et vous pouvez le déplacer pour [Ajouter des utilisateurs et attribuer des licences](#add-users-and-assign-licenses).</span><span class="sxs-lookup"><span data-stu-id="412b8-107">If you purchased a new domain when you signed up, your domain is all set up and you can move to [Add users and assign licenses](#add-users-and-assign-licenses).</span></span>

### <a name="add-your-domain-to-personalize-sign-in"></a><span data-ttu-id="412b8-108">Ajouter votre domaine pour personnaliser la connexion</span><span class="sxs-lookup"><span data-stu-id="412b8-108">Add your domain to personalize sign-in</span></span>

1. <span data-ttu-id="412b8-109">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide de vos informations d’identification d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="412b8-109">Sign in to [Microsoft 365 admin center](https://admin.microsoft.com) by using your global admin credentials.</span></span> 

2. <span data-ttu-id="412b8-110">Sélectionnez **Ajouter un domaine** ou **Ajouter des utilisateurs** pour démarrer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="412b8-110">Choose **Add a domain** or **Add users** to start the wizard.</span></span>
    > [!IMPORTANT]
    > <span data-ttu-id="412b8-111">Si vous avez acheté un domaine lors de l’inscription, vous ne verrez pas **Ajouter une étape de domaine** ici.</span><span class="sxs-lookup"><span data-stu-id="412b8-111">If you purchased a domain during the sign-up, you will not see **Add a domain** step here.</span></span> <span data-ttu-id="412b8-112">Accédez à [Ajouter des utilisateurs](#add-users-and-assign-licenses) à la place.</span><span class="sxs-lookup"><span data-stu-id="412b8-112">Go to [Add users ](#add-users-and-assign-licenses) instead.</span></span>

    ![Sélectionnez Ajouter un domaine.](media/addadomainadmincenter.png)
    
3. <span data-ttu-id="412b8-114">Dans l’Assistant, entrez le nom de domaine que vous souhaitez utiliser (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="412b8-114">In the wizard, enter the domain name you want to use (like contoso.com).</span></span>


    ![Capture d’écran de la page Personnalisez votre connexion.](media/personalizesignin.png)

    
4. <span data-ttu-id="412b8-116">Suivez les étapes de l’Assistant pour [créer des enregistrements DNS auprès d’un fournisseur d’hébergement DNS pour Office 365](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) qui vérifie que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="412b8-116">Follow the steps in the wizard to [Create DNS records at any DNS hosting provider for Office 365](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) that verifies you own the domain.</span></span> <span data-ttu-id="412b8-117">Si vous êtes conscient de votre hôte de domaine, reportez-vous aux [instructions spécifiques](https://docs.microsoft.com/office365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions)de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="412b8-117">If you know your domain host, see also the [host specific instructions](https://docs.microsoft.com/office365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions).</span></span>

    <span data-ttu-id="412b8-118">Si votre fournisseur d’hébergement est GoDaddy ou si un autre hôte est activé avec la [connexion au domaine](https://docs.microsoft.com/office365/admin/get-help-with-domains/domain-connect), le processus est facile et vous êtes automatiquement invité à vous connecter et à laisser Microsoft s’authentifier à votre place :</span><span class="sxs-lookup"><span data-stu-id="412b8-118">If your hosting provider is GoDaddy, or another host enabled with [domain connect](https://docs.microsoft.com/office365/admin/get-help-with-domains/domain-connect),the process is easy and you will be automatically asked to sign in and let Microsoft authenticate on your behalf:</span></span>

    ![Sur GoDaddy, sélectionnez Autoriser.](media/godaddyauth.png)

### <a name="add-users-and-assign-licenses"></a><span data-ttu-id="412b8-120">Ajouter des utilisateurs et attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="412b8-120">Add users and assign licenses</span></span>

<span data-ttu-id="412b8-121">Vous pouvez ajouter des utilisateurs dans l’Assistant, mais vous pouvez également [Ajouter des utilisateurs ultérieurement](add-users-m365b.md) dans le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="412b8-121">You can add users in the wizard, but you can also [add users later](add-users-m365b.md) in the admin center.</span></span> <span data-ttu-id="412b8-122">En outre, si vous disposez d’un contrôleur de domaine local, vous pouvez ajouter des utilisateurs avec [Azure ad Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express).</span><span class="sxs-lookup"><span data-stu-id="412b8-122">Additionally, if you have a local domain controller, you can add users with [Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express).</span></span>

#### <a name="add-users-in-the-wizard"></a><span data-ttu-id="412b8-123">Ajouter des utilisateurs dans l’Assistant</span><span class="sxs-lookup"><span data-stu-id="412b8-123">Add users in the wizard</span></span>

<span data-ttu-id="412b8-124">Tous les utilisateurs que vous ajoutez dans l’Assistant reçoivent automatiquement une licence d’entreprise Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="412b8-124">Any users you add in the wizard get automatically assigned a Microsoft 365 Business license.</span></span>

![Capture d’écran de la page Ajouter de nouveaux utilisateurs dans l’Assistant](media/addnewuserspage.png)

1. <span data-ttu-id="412b8-126">Si votre abonnement professionnel Microsoft 365 comporte des utilisateurs existants (par exemple, si vous avez utilisé Azure AD Connect), vous avez la possibilité de leur attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="412b8-126">If your Microsoft 365 Business subscription has existing users (for example, if you used Azure AD Connect) , you get an option to assign licenses to them now.</span></span> <span data-ttu-id="412b8-127">Poursuivez et ajoutez des licences pour eux aussi.</span><span class="sxs-lookup"><span data-stu-id="412b8-127">Go ahead and add licenses to them as well.</span></span>

3. <span data-ttu-id="412b8-128">Une fois que vous avez ajouté les utilisateurs, vous pouvez également partager les informations d’identification avec les nouveaux utilisateurs que vous avez ajoutés.</span><span class="sxs-lookup"><span data-stu-id="412b8-128">After you have added the users, you will also get an option to share credentials with the new users you added.</span></span> <span data-ttu-id="412b8-129">Vous pouvez choisir de les imprimer, de les envoyer par e-mail ou de les télécharger.</span><span class="sxs-lookup"><span data-stu-id="412b8-129">You can choose to print them out, email them, or download them.</span></span>

4. <span data-ttu-id="412b8-130">Ignorez la migration des messages e-mail et sélectionnez **Suivant** dans la page **Migrer les messages e-mail**.</span><span class="sxs-lookup"><span data-stu-id="412b8-130">Skip migrating email messages and choose **Next** on **Migrate email messages** page.</span></span> 

    <span data-ttu-id="412b8-131">Si vous effectuez une migration à partir d’un autre fournisseur de courrier et que vous souhaitez copier vos données ultérieurement, vous pouvez [migrer le courrier électronique et les contacts vers Office 365](https://support.office.com/article/a3e3bddb-582e-4133-8670-e61b9f58627e).</span><span class="sxs-lookup"><span data-stu-id="412b8-131">If you are moving from another email provider and want to copy your data later, you can [Migrate email and contacts to Office 365](https://support.office.com/article/a3e3bddb-582e-4133-8670-e61b9f58627e).</span></span>


### <a name="connect-your-domain"></a><span data-ttu-id="412b8-132">Sélectionner votre domaine</span><span class="sxs-lookup"><span data-stu-id="412b8-132">Connect your domain</span></span>

> [!NOTE]
> <span data-ttu-id="412b8-133">Si vous avez choisi d’utiliser le domaine. onmicrosoft ou si vous avez utilisé Azure AD Connect pour configurer des utilisateurs, vous ne verrez pas cette étape.</span><span class="sxs-lookup"><span data-stu-id="412b8-133">If you chose to use the .onmicrosoft domain, or used Azure AD Connect to set up users, you will not see this step.</span></span>
  
<span data-ttu-id="412b8-134">Pour configurer des services, vous devez mettre à jour des enregistrements au niveau de votre hôte DNS ou de votre bureau d'enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="412b8-134">To set up services, you have to update some records at your DNS host or domain registrar.</span></span>
  
1. <span data-ttu-id="412b8-135">L'Assistant Configuration détecte généralement votre bureau d'enregistrement et vous fournit un lien vers des instructions détaillées vous permettant de mettre à jour vos enregistrements NS sur le site web du bureau d'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="412b8-135">The setup wizard typically detects your registrar and gives you a link to step-by-step instructions for updating your NS records at the registrar website.</span></span> <span data-ttu-id="412b8-136">Si ce n’est pas le cas, [Modifiez les serveurs de noms pour configurer Office 365 avec n’importe quel](https://support.office.com/article/a8b487a9-2a45-4581-9dc4-5d28a47010a2)Bureau d’enregistrement de domaine.</span><span class="sxs-lookup"><span data-stu-id="412b8-136">If it doesn't, [Change nameservers to set up Office 365 with any domain registrar](https://support.office.com/article/a8b487a9-2a45-4581-9dc4-5d28a47010a2).</span></span> 

    - <span data-ttu-id="412b8-137">Si vous avez des enregistrements DNS existants, par exemple un site Web existant, mais que votre hôte DNS est activé pour la [connexion au domaine](https://docs.microsoft.com/office365/admin/get-help-with-domains/domain-connect), choisissez **Ajouter des enregistrements pour moi**.</span><span class="sxs-lookup"><span data-stu-id="412b8-137">If you have existing DNS records, for example an existing web site, but your DNS host is enabled for [domain connect](https://docs.microsoft.com/office365/admin/get-help-with-domains/domain-connect), choose **Add records for me**.</span></span> 
    - <span data-ttu-id="412b8-138">Si vous avez des enregistrements DNS existants avec d’autres hôtes DNS (non activé pour la connexion au domaine), vous devez gérer vos propres enregistrements DNS pour vous assurer que les services existants restent connectés.</span><span class="sxs-lookup"><span data-stu-id="412b8-138">If you have existing DNS records with other DNS hosts (not enabled for domain connect), you will want to manage your own DNS records to make sure the existing services stay connected.</span></span> <span data-ttu-id="412b8-139">Pour plus d’informations, voir [notions de base](https://docs.microsoft.com/office365/admin/get-help-with-domains/dns-basics) sur le domaine.</span><span class="sxs-lookup"><span data-stu-id="412b8-139">See [domain basics](https://docs.microsoft.com/office365/admin/get-help-with-domains/dns-basics) for more info.</span></span>

        ![Connecter votre page de domaine avec je vais gérer mes propres enregistrements DNS.](media/connectyourdomainpage.png)

2. <span data-ttu-id="412b8-141">Suivez les étapes de l’Assistant et de la messagerie et d’autres services sont configurés pour vous.</span><span class="sxs-lookup"><span data-stu-id="412b8-141">Follow the steps in the wizard and email and other services will be set up for you.</span></span>

### <a name="set-up-security-policies-and-device-configurations"></a><span data-ttu-id="412b8-142">Configurer les stratégies de sécurité et les configurations des appareils</span><span class="sxs-lookup"><span data-stu-id="412b8-142">Set up security policies and device configurations</span></span> 

<span data-ttu-id="412b8-143">Les stratégies que vous configurez dans l’Assistant sont appliquées automatiquement à un [groupe de sécurité](https://docs.microsoft.com/office365/admin/create-groups/compare-groups#security-groups) appelé *tous les utilisateurs*.</span><span class="sxs-lookup"><span data-stu-id="412b8-143">The policies you set up in the wizard are applied automatically to a [Security group](https://docs.microsoft.com/office365/admin/create-groups/compare-groups#security-groups) called *All Users*.</span></span> <span data-ttu-id="412b8-144">Vous pouvez également créer des groupes supplémentaires auxquels affecter des stratégies dans le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="412b8-144">You can also create additional groups to assign policies to in the admin center.</span></span>

1. <span data-ttu-id="412b8-145">Dans la case à cocher **protéger vos fichiers professionnels sur les appareils mobiles** , l’option **protéger les fichiers de travail lorsque les appareils sont perdus ou volés** est sélectionnée par défaut.</span><span class="sxs-lookup"><span data-stu-id="412b8-145">On the **Protect your work files on mobile devices** the option **Protect work files when devices are lost or stolen** is selected by default.</span></span> <span data-ttu-id="412b8-146">Vous avez la possibilité d’activer **la gestion de la manière dont les utilisateurs accèdent aux fichiers Office sur les appareils mobiles**, ce qui est recommandé.</span><span class="sxs-lookup"><span data-stu-id="412b8-146">You have an option to turn on **Manage how users access Office files on mobile devices**, and this is recommended.</span></span>

    ![Capture d’écran de la page protéger les fichiers de travail sur les appareils mobiles.](media/protectworkfilesondevices.png)

     - <span data-ttu-id="412b8-148">Développez **protéger les fichiers de travail en cas de perte ou de vol des appareils** pour afficher les [valeurs par défaut](protect-work-files-on-lost-or-stolen-device.md):</span><span class="sxs-lookup"><span data-stu-id="412b8-148">Expand **Protect work files when devices are lost or stolen** to display the [default values](protect-work-files-on-lost-or-stolen-device.md):</span></span>

        ![Capture d’écran des valeurs par défaut pour la protection des fichiers sur les appareils perdus.](media/protectworkfilesondevicesdefault.png)

    - <span data-ttu-id="412b8-150">Sélectionnez **gérer la manière dont les utilisateurs accèdent aux fichiers Office sur les appareils mobiles** et développez-le pour afficher les [valeurs par défaut](manage-user-access-on-mobile-devices.md).</span><span class="sxs-lookup"><span data-stu-id="412b8-150">Select **Manage how users access Office files on mobile devices** and expand it to display the [default values](manage-user-access-on-mobile-devices.md).</span></span> <span data-ttu-id="412b8-151">Nous vous recommandons d’accepter les valeurs par défaut lors de l’installation pour créer des stratégies d’application pour Android, iOS et Windows 10 qui s’appliquent à tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="412b8-151">We recommend that you accept the default values during setup to create application policies for Android, iOS, and Windows 10 that apply to all users.</span></span> <span data-ttu-id="412b8-152">Vous pouvez créer des stratégies supplémentaires une fois l'installation terminée.</span><span class="sxs-lookup"><span data-stu-id="412b8-152">You can create more policies after setup completes.</span></span>

        ![Capture d’écran des paramètres de protection pour les fichiers Office sur mobile.](media/useraccessonmobile.png)

2. <span data-ttu-id="412b8-154">La dernière étape sur la protection des données et des périphériques vous permet de configurer des stratégies pour sécuriser les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="412b8-154">The last step on protect data and devices allows you to set up policies to secure Windows 10 devices.</span></span> <span data-ttu-id="412b8-155">Ces paramètres sont appliqués automatiquement lorsque le Windows 10 d’un utilisateur se connecte à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="412b8-155">These settings are applied automatically when a user's Windows 10 connects to your organization.</span></span> <span data-ttu-id="412b8-156">Vous pouvez développer des **appareils Windows 10 sécurisés** pour afficher et modifier les [valeurs par défaut](secure-windows-10-devices.md).</span><span class="sxs-lookup"><span data-stu-id="412b8-156">You can expand **Secure Windows 10 devices** to see and modify the [default values](secure-windows-10-devices.md).</span></span>
3. <span data-ttu-id="412b8-157">Vous pouvez également choisir d' [installer automatiquement Office](install-office-on-windows-10-during-setup.md) sur les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="412b8-157">You can also choose to [automatically install Office](install-office-on-windows-10-during-setup.md) on Windows 10 devices.</span></span>

    ![Capture d’écran de la page définir la configuration de l’appareil Windows 10.](media/setwin10config.png)



## <a name="deploy-office-365-client-apps"></a><span data-ttu-id="412b8-159">Déployer des applications clientes Office 365</span><span class="sxs-lookup"><span data-stu-id="412b8-159">Deploy Office 365 client apps</span></span>

<span data-ttu-id="412b8-160">Si vous avez choisi d’installer automatiquement les applications Office dans lors de la configuration, les applications s’installeront sur les appareils Windows 10 une fois que les utilisateurs se sont connectés à Azure AD à partir de leurs appareils Windows avec leurs informations d’identification professionnelles.</span><span class="sxs-lookup"><span data-stu-id="412b8-160">If you chose to automatically install Office apps in during the set up, the apps will install on the Windows 10 devices once the users have signed in to Azure AD from their Windows devices with their work credentials.</span></span>
<span data-ttu-id="412b8-161">Pour installer Office sur des appareils mobiles iOS ou Android, consultez la rubrique [configurer des appareils mobiles pour les utilisateurs professionnels de Microsoft 365](set-up-mobile-devices.md).</span><span class="sxs-lookup"><span data-stu-id="412b8-161">To install Office on mobile iOS or Android devices, see [Set up mobile devices for Microsoft 365 Business users](set-up-mobile-devices.md).</span></span>

<span data-ttu-id="412b8-162">Vous pouvez également installer Office individuellement.</span><span class="sxs-lookup"><span data-stu-id="412b8-162">You can also install Office individually.</span></span> <span data-ttu-id="412b8-163">Pour obtenir des instructions, voir [installer Office sur un PC ou un Mac](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc4716658) .</span><span class="sxs-lookup"><span data-stu-id="412b8-163">See [install Office on a PC or Mac](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc4716658) for instructions.</span></span>
