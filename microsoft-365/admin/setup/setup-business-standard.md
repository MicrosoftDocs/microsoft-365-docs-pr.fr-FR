---
title: Configurer Microsoft 365 Business Standard
f1.keywords:
- NOCSH
ms.author: efrene
author: efrene
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
- Adm_O365_Setup
- TRN_SMB
ms.custom:
- TRN_M365B
- OKR_SMB_Videos
- AdminSurgePortfolio
search.appverid:
- MET150
- MOE150
- BEA160
description: Découvrez comment configurer votre abonnement Microsoft 365 Business Standard.
ms.openlocfilehash: ce45b4869000892b5640730e765dbfc9c21386ed
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52244454"
---
# <a name="set-up-microsoft-business-standard"></a><span data-ttu-id="adb20-103">Configurer Microsoft Business Standard</span><span class="sxs-lookup"><span data-stu-id="adb20-103">Set up Microsoft Business Standard</span></span>



## <a name="add-your-domain-to-personalize-sign-in"></a><span data-ttu-id="adb20-104">Ajouter votre domaine pour personnaliser la connexion</span><span class="sxs-lookup"><span data-stu-id="adb20-104">Add your domain to personalize sign-in</span></span>

<span data-ttu-id="adb20-105">Lorsque vous achetez Microsoft 365 Business Standard, vous avez la possibilité d’utiliser un domaine que vous possédez ou d’en acheter un pendant l’inscription.</span><span class="sxs-lookup"><span data-stu-id="adb20-105">When you purchase Microsoft 365 Business Standard, you have the option of using a domain you own, or buying one during the sign-up.</span></span>

- <span data-ttu-id="adb20-106">Si vous avez acheté un nouveau domaine lorsque vous vous êtes inscrit, votre domaine est configuré et vous pouvez accéder à [Ajouter des utilisateurs et attribuer des licences](#add-users-and-assign-licenses).</span><span class="sxs-lookup"><span data-stu-id="adb20-106">If you purchased a new domain when you signed up, your domain is all set up and you can move to [Add users and assign licenses](#add-users-and-assign-licenses).</span></span>

1. <span data-ttu-id="adb20-107">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide de vos informations d’identification d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="adb20-107">Sign in to [Microsoft 365 admin center](https://admin.microsoft.com) by using your global admin credentials.</span></span> 

2. <span data-ttu-id="adb20-108">Choisissez **Configurer** pour démarrer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="adb20-108">Choose **Go to setup** to start the wizard.</span></span>

3. <span data-ttu-id="adb20-109">Sur la page **Installer vos applications Office**, vous pouvez installer les applications sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="adb20-109">On the **Install your Office apps** page, you can optionally install the apps on your own computer.</span></span>
    
4. <span data-ttu-id="adb20-110">Dans l’étape **ajouter un domaine**, entrez le nom de domaine que vous voulez utiliser (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="adb20-110">In the **Add domain** step, enter the domain name you want to use (like contoso.com).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="adb20-111">Si vous avez acheté un domaine pendant l’inscription, vous ne verrez pas l’étape **Ajouter un domaine** ici.</span><span class="sxs-lookup"><span data-stu-id="adb20-111">If you purchased a domain during the sign-up, you will not see **Add a domain** step here.</span></span> <span data-ttu-id="adb20-112">Accédez à [Ajouter des utilisateurs](#add-users-and-assign-licenses) à la place.</span><span class="sxs-lookup"><span data-stu-id="adb20-112">Go to [Add users](#add-users-and-assign-licenses) instead.</span></span>

    
4. <span data-ttu-id="adb20-113">Suivez les étapes de l’Assistant pour [Créer des enregistrements DNS auprès d’un fournisseur d’hébergement DNS pour Office 365](/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) qui vérifie que vous êtes le propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="adb20-113">Follow the steps in the wizard to [Create DNS records at any DNS hosting provider for Office 365](/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) that verifies you own the domain.</span></span> <span data-ttu-id="adb20-114">Si vous savez qu’il s’agit de votre hôte de domaine, consultez également les [Instructions propres à l’hôte](/office365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions).</span><span class="sxs-lookup"><span data-stu-id="adb20-114">If you know your domain host, see also the [host specific instructions](/office365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions).</span></span>

    <span data-ttu-id="adb20-115">Si votre fournisseur d’hébergement est GoDaddy ou si un autre hôte est activé avec [connexion de domaine](/office365/admin/get-help-with-domains/domain-connect), le processus est simple et vous êtes automatiquement invité à vous connecter et à laisser Microsoft s’authentifier en votre nom.</span><span class="sxs-lookup"><span data-stu-id="adb20-115">If your hosting provider is GoDaddy or another host enabled with [domain connect](/office365/admin/get-help-with-domains/domain-connect), the process is easy and you'll be automatically asked to sign in and let Microsoft authenticate on your behalf.</span></span>

    ![Sur la page Confirmer l’accès GoDaddy, sélectionnez Autoriser.](../../media/godaddyauth.png)

## <a name="add-users-and-assign-licenses"></a><span data-ttu-id="adb20-117">Ajouter des utilisateurs et attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="adb20-117">Add users and assign licenses</span></span>

<span data-ttu-id="adb20-118">Vous pouvez ajouter des utilisateurs dans l’Assistant, mais vous pouvez également [Ajouter des utilisateurs plus tard](../add-users/add-users.md) dans le Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="adb20-118">You can add users in the wizard, but you can also [add users later](../add-users/add-users.md) in the admin center.</span></span> <span data-ttu-id="adb20-119">De plus, si vous avez un contrôleur de domaine local, vous pouvez ajouter des utilisateurs avec [Azure AD Connect](/azure/active-directory/hybrid/how-to-connect-install-express).</span><span class="sxs-lookup"><span data-stu-id="adb20-119">Additionally, if you have a local domain controller, you can add users with [Azure AD Connect](/azure/active-directory/hybrid/how-to-connect-install-express).</span></span>

## <a name="add-users-in-the-wizard"></a><span data-ttu-id="adb20-120">Ajouter des utilisateurs dans l’Assistant</span><span class="sxs-lookup"><span data-stu-id="adb20-120">Add users in the wizard</span></span>

<span data-ttu-id="adb20-121">Les utilisateurs que vous ajoutez à l’Assistant reçoivent automatiquement une licence Microsoft 365 Business Standard.</span><span class="sxs-lookup"><span data-stu-id="adb20-121">Any users you add in the wizard get automatically assigned a Microsoft 365 Business Standard license.</span></span>

1. <span data-ttu-id="adb20-p104">Si votre abonnement Microsoft 365 Business Standard est associé à des utilisateurs existants (par exemple, si vous utilisiez Azure AD Connect), vous avez la possibilité de leur attribuer des licences à ce stade. Poursuivez et ajoutez leur des licences aussi.</span><span class="sxs-lookup"><span data-stu-id="adb20-p104">If your Microsoft 365 Business Standard subscription has existing users (for example, if you used Azure AD Connect), you get an option to assign licenses to them now. Go ahead and add licenses to them as well.</span></span>

2. <span data-ttu-id="adb20-124">Une fois que vous avez ajouté les utilisateurs, vous avez également la possibilité de partager des informations d’identification avec les nouveaux utilisateurs que vous ajoutez.</span><span class="sxs-lookup"><span data-stu-id="adb20-124">After you've added the users, you'll also get an option to share credentials with the new users you added.</span></span> <span data-ttu-id="adb20-125">Vous pouvez choisir de les imprimer, de les envoyer par e-mail ou de les télécharger.</span><span class="sxs-lookup"><span data-stu-id="adb20-125">You can choose to print them out, email them, or download them.</span></span>

## <a name="connect-your-domain"></a><span data-ttu-id="adb20-126">Sélectionner votre domaine</span><span class="sxs-lookup"><span data-stu-id="adb20-126">Connect your domain</span></span>

> [!NOTE]
> <span data-ttu-id="adb20-127">Si vous avez choisi d’utiliser le domaine .onmicrosoft, ou si vous avez utilisé Azure AD Connect pour configurer des utilisateurs, vous ne verrez pas cette étape.</span><span class="sxs-lookup"><span data-stu-id="adb20-127">If you chose to use the .onmicrosoft domain, or used Azure AD Connect to set up users, you will not see this step.</span></span>
  
<span data-ttu-id="adb20-128">Pour configurer des services, vous devez mettre à jour des enregistrements au niveau de votre hôte DNS ou de votre bureau d’enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="adb20-128">To set up services, you have to update some records at your DNS host or domain registrar.</span></span>
  
1. <span data-ttu-id="adb20-129">L’Assistant Configuration détecte généralement votre bureau d’enregistrement et vous fournit un lien vers des instructions détaillées vous permettant de mettre à jour vos enregistrements NS sur le site web du bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="adb20-129">The setup wizard typically detects your registrar and gives you a link to step-by-step instructions for updating your NS records at the registrar website.</span></span> <span data-ttu-id="adb20-130">Si ce n’est pas le cas,[Modifier les serveurs de noms de manière à configurer Office 365 avec n'importe quel bureau d'enregistrement de domaines](../get-help-with-domains/change-nameservers-at-any-domain-registrar.md).</span><span class="sxs-lookup"><span data-stu-id="adb20-130">If it doesn't, [Change nameservers to set up Office 365 with any domain registrar](../get-help-with-domains/change-nameservers-at-any-domain-registrar.md).</span></span> 

    - <span data-ttu-id="adb20-131">Si vous avez des enregistrements DNS existants (par exemple, un site web existant), mais que votre hôte DNS est activé pour [connexion de domaine](/office365/admin/get-help-with-domains/domain-connect), sélectionnez **Ajouter des enregistrements pour moi**.</span><span class="sxs-lookup"><span data-stu-id="adb20-131">If you have existing DNS records, for example an existing web site, but your DNS host is enabled for [domain connect](/office365/admin/get-help-with-domains/domain-connect), choose **Add records for me**.</span></span> <span data-ttu-id="adb20-132">Sur la page **sélectionnez votre services en ligne**, acceptez toutes les valeurs par défaut, puis sélectionnez **Suivant**, puis sélectionnez **Autoriser** sur la page de votre hôte DNS.</span><span class="sxs-lookup"><span data-stu-id="adb20-132">On the **Choose your online services** page, accept all the defaults, and choose **Next**, and choose **Authorize** on your DNS host's page.</span></span>
    - <span data-ttu-id="adb20-133">Si vous avez des enregistrements DNS existants avec d’autres hôtes DNS (non activé pour la connexion de domaine), vous pouvez gérer vos propres enregistrements DNS pour vous assurer que les services existants restent connectés.</span><span class="sxs-lookup"><span data-stu-id="adb20-133">If you have existing DNS records with other DNS hosts (not enabled for domain connect), you'll want to manage your own DNS records to make sure the existing services stay connected.</span></span> <span data-ttu-id="adb20-134">Pour plus d’informations, consultez [notions de base du domaine](/office365/admin/get-help-with-domains/dns-basics).</span><span class="sxs-lookup"><span data-stu-id="adb20-134">See [domain basics](/office365/admin/get-help-with-domains/dns-basics) for more info.</span></span>

2. <span data-ttu-id="adb20-135">Suivez les étapes de l’Assistant, et la messagerie électronique et d’autres services sont configurés pour vous.</span><span class="sxs-lookup"><span data-stu-id="adb20-135">Follow the steps in the wizard and email and other services will be set up for you.</span></span>

    <span data-ttu-id="adb20-136">Une fois le processus d'inscription terminé, vous êtes dirigé vers le centre d'administration, où vous suivez un assistant qui vous aide à installer les applications Office, ajouter votre domaine, ajouter des utilisateurs et attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="adb20-136">When the signup process is complete, you'll be directed to the admin center, where you'll follow a wizard to install Office apps, add your domain, add users, and assign licenses.</span></span> <span data-ttu-id="adb20-137">Une fois la configuration initiale terminée, vous pouvez utiliser la page de **configuration** dans le centre d'administration pour continuer la mise en place et la configuration des services qui accompagnent vos abonnements.</span><span class="sxs-lookup"><span data-stu-id="adb20-137">After you complete the initial setup, you can use the **Setup** page in the admin center to continue setting up and configuring the services that come with your subscriptions.</span></span>

    <span data-ttu-id="adb20-138">Pour plus d'informations sur l'assistant de configuration et la page de **configuration** du centre d'administration, consultez la rubrique [Différence entre l'assistant de configuration et la page de configuration](o365-setup-wizard-and-setup-page.md).</span><span class="sxs-lookup"><span data-stu-id="adb20-138">For more information about the setup wizard and the admin center **Setup** page, see [Difference between the setup wizard and the Setup page](o365-setup-wizard-and-setup-page.md).</span></span>

## <a name="finish-setting-up"></a><span data-ttu-id="adb20-139">Terminez la configuration</span><span class="sxs-lookup"><span data-stu-id="adb20-139">Finish setting up</span></span>

### <a name="set-up-outlook-for-email"></a><span data-ttu-id="adb20-140">Configurer Outlook pour le courrier électronique</span><span class="sxs-lookup"><span data-stu-id="adb20-140">Set up Outlook for email</span></span>

1. <span data-ttu-id="adb20-141">Dans le menu Démarrer de Windows, recherchez Outlook, puis sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="adb20-141">On the Windows Start menu, search for Outlook, and select it.</span></span>

    <span data-ttu-id="adb20-142">(Si vous utilisez un Mac, ouvrez Outlook à partir de la barre d’outils ou recherchez-le à l’aide du Finder).</span><span class="sxs-lookup"><span data-stu-id="adb20-142">(If you're using a Mac, open Outlook from the toolbar or locate it using the Finder.)</span></span>

    <span data-ttu-id="adb20-143">Si vous venez d’installer Outlook, sur la page Accueil, sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="adb20-143">If you've just installed Outlook, on the Welcome page, select **Next**.</span></span>

2. <span data-ttu-id="adb20-144">Choisissez **Fichier** \> **Informations** \> **Ajouter un compte**.</span><span class="sxs-lookup"><span data-stu-id="adb20-144">Choose **File** \> **Info** \> **Add Account**.</span></span>

3. <span data-ttu-id="adb20-145">Entrez votre adresse e-mail Microsoft , puis sélectionnez **Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="adb20-145">Enter your Microsoft email address and select **Connect**.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/9fe86884-8a83-42cc-bca9-61a12e6dad31?autoplay=false]
  
<span data-ttu-id="adb20-146">Pour plus d’informations, voir [Configurer Outlook pour le courrier](https://support.microsoft.com/office/f5bf0cd1-e1f3-4b0d-a022-ecab17efe86f).</span><span class="sxs-lookup"><span data-stu-id="adb20-146">More at [Set up Outlook for email](https://support.microsoft.com/office/f5bf0cd1-e1f3-4b0d-a022-ecab17efe86f).</span></span>
  
### <a name="import-email"></a><span data-ttu-id="adb20-147">Importer le courrier électronique</span><span class="sxs-lookup"><span data-stu-id="adb20-147">Import email</span></span>

<span data-ttu-id="adb20-148">Si vous utilisiez Outlook avec un autre compte de courrier, vous pouvez importer vos e-mails, votre calendrier et vos contacts antérieurs dans votre nouveau compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="adb20-148">If you were using Outlook with another email account, you can import your previous email, calendar, and contacts into your new Microsoft account.</span></span>
  
1. <span data-ttu-id="adb20-149">**Exporter vos anciens e-mails**</span><span class="sxs-lookup"><span data-stu-id="adb20-149">**Export your old email**</span></span>

    <span data-ttu-id="adb20-150">Dans Outlook, choisissez **Fichier** \> **Ouvrir &amp; Exporter** \> **Importer/Exporter**.</span><span class="sxs-lookup"><span data-stu-id="adb20-150">In Outlook, choose **File** \> **Open &amp; Export** \> **Import/Export**.</span></span>

    <span data-ttu-id="adb20-151">Sélectionnez **Exporter vers un fichier**, puis suivez la procédure pour exporter votre fichier de données Outlook (.pst) et tous les sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="adb20-151">Select **Export to a File** and then follow the steps to export your Outlook Data File (.pst) and any subfolders.</span></span>

2. <span data-ttu-id="adb20-152">**Importer vos anciens e-mails**</span><span class="sxs-lookup"><span data-stu-id="adb20-152">**Import your old email**</span></span>

    <span data-ttu-id="adb20-153">Dans Outlook, choisissez de nouveau **Fichier** \> **Ouvrir &amp; Exporter** \> **Importer/Exporter**.</span><span class="sxs-lookup"><span data-stu-id="adb20-153">In Outlook, choose **File** \> **Open &amp; Export** \> **Import/Export** again.</span></span>

    <span data-ttu-id="adb20-154">Cette fois, sélectionnez **Importer à partir d’un autre programme ou fichier** et suivez la procédure pour importer le fichier de sauvegarde que vous avez créé lors de l’exportation de vos anciens e-mails.</span><span class="sxs-lookup"><span data-stu-id="adb20-154">This time, select **Import from another program or file** and follow the steps to import the backup file you created when you exported your old email.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/40f7df36-9e24-44e5-8791-e9ed0dd8fd21?autoplay=false]
  
<span data-ttu-id="adb20-155">Pour plus d’informations, voir [Importer le courrier avec Outlook](https://support.microsoft.com/office/6a3771d4-4c1d-4a25-92a6-0b8e476335de).</span><span class="sxs-lookup"><span data-stu-id="adb20-155">More at [Import email with Outlook](https://support.microsoft.com/office/6a3771d4-4c1d-4a25-92a6-0b8e476335de).</span></span>

<span data-ttu-id="adb20-156">Vous pouvez également utiliser le Centre d’administration Exchange pour importer le courrier électronique de tout le monde.</span><span class="sxs-lookup"><span data-stu-id="adb20-156">You can also use Exchange admin center to import everyone's email.</span></span> <span data-ttu-id="adb20-157">Pour obtenir plus d'informations, consultez l'article [Migrer plusieurs comptes de messagerie](/Exchange/mailbox-migration/mailbox-migration).</span><span class="sxs-lookup"><span data-stu-id="adb20-157">For more information, see [migrate multiple email accounts](/Exchange/mailbox-migration/mailbox-migration).</span></span>
  
### <a name="use-a-public-website"></a><span data-ttu-id="adb20-158">Utiliser un site web public</span><span class="sxs-lookup"><span data-stu-id="adb20-158">Use a public website</span></span>

<span data-ttu-id="adb20-159">Microsoft 365 n'inclut pas de site web public pour votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="adb20-159">Microsoft 365 doesn't include a public website for your business.</span></span> <span data-ttu-id="adb20-160">Si vous voulez en configurer un, vous pouvez utiliser un partenaire Microsoft, tel que GoDaddy ou WIX.</span><span class="sxs-lookup"><span data-stu-id="adb20-160">If you want to set one up, consider using a Microsoft partner, such as GoDaddy or WIX.</span></span>
  
1. <span data-ttu-id="adb20-161">Dans le centre d’administration, accédez à **Ressources**, puis sélectionnez **Site web public**.</span><span class="sxs-lookup"><span data-stu-id="adb20-161">From the admin center, go to **Resources**, and then select **Public website**.</span></span>

2. <span data-ttu-id="adb20-162">Sélectionnez **En savoir plus** sous l’une des options, puis inscrivez-vous à un site web partenaire et servez-vous de ses outils pour configurer et concevoir votre site.</span><span class="sxs-lookup"><span data-stu-id="adb20-162">Select **Learn more** under one of the options, and then sign up with a website partner and use their tools to set up and design your site.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/4839abc6-9323-4cbf-a79d-2907235f9ebb]

<span data-ttu-id="adb20-163">Pour plus d’informations, voir [Utiliser un site web public](../../business-video/create-web-site.md).</span><span class="sxs-lookup"><span data-stu-id="adb20-163">More at [Use a public website](../../business-video/create-web-site.md).</span></span>