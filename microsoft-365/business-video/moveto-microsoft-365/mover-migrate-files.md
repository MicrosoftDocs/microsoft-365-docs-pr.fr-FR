---
title: 'Migrer des fichiers Google vers Microsoft 365 pour les entreprises '
f1.keywords:
- NOCSH
ms.author: twerner
author: twernermsft
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
ms.custom:
- AdminSurgePortfolio
- adminvideo
monikerRange: o365-worldwide
search.appverid:
- BCS160
- MET150
- MOE150
description: Découvrez comment migrer des fichiers Google vers Microsoft 365 pour les entreprises à l’aide de Mover.
ms.openlocfilehash: 72ea81ad86a20e01b4650915fef96a713b207c3b
ms.sourcegitcommit: a1846b1ee2e4fa397e39c1271c997fc4cf6d5619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "50166158"
---
# <a name="migrate-google-files-to-microsoft-365-for-business"></a><span data-ttu-id="71e4e-103">Migrer des fichiers Google vers Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="71e4e-103">Migrate Google files to Microsoft 365 for business</span></span> 

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4MhaD?autoplay=false]

<span data-ttu-id="71e4e-104">Lorsque vous migrez vers Microsoft 365 pour les entreprises, vous souhaiterez migrer vos fichiers à partir de Google Drive.</span><span class="sxs-lookup"><span data-stu-id="71e4e-104">When you move to Microsoft 365 for business, you'll want to migrate your files from Google Drive.</span></span> <span data-ttu-id="71e4e-105">Vous pouvez utiliser l’application Mover pour déplacer des fichiers à partir de lecteurs personnels et partagés.</span><span class="sxs-lookup"><span data-stu-id="71e4e-105">You can use the Mover app to move files from personal and shared Drives.</span></span> <span data-ttu-id="71e4e-106">Pour plus d’informations, [voir Migration cloud de Mover.](https://docs.microsoft.com/sharepointmigration/mover-plan-migration)</span><span class="sxs-lookup"><span data-stu-id="71e4e-106">For more information, see [Mover Cloud Migration](https://docs.microsoft.com/sharepointmigration/mover-plan-migration).</span></span>

> [!NOTE]
> <span data-ttu-id="71e4e-107">Mover effectuera une copie des fichiers et les déplacera vers Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="71e4e-107">Mover will make a copy of the files and move the copies to Microsoft 365 for business.</span></span> <span data-ttu-id="71e4e-108">Les fichiers d’origine resteront également dans Google Drives.</span><span class="sxs-lookup"><span data-stu-id="71e4e-108">The original files will stay in Google Drives also.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="71e4e-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="71e4e-109">Before you start</span></span>

<span data-ttu-id="71e4e-110">Tous les utilisateurs doivent s’être inscrits à Microsoft 365 pour les entreprises et configurer leur OneDrive Entreprise.</span><span class="sxs-lookup"><span data-stu-id="71e4e-110">All the users should have signed in to Microsoft 365 for business and set up their OneDrive for Business.</span></span> <span data-ttu-id="71e4e-111">Pour ce faire, [office.com,](https://office.com)connectez-vous avec vos informations d’identification Microsoft 365 entreprise, puis choisissez OneDrive.</span><span class="sxs-lookup"><span data-stu-id="71e4e-111">To do this, go to [office.com](https://office.com), sign in with your Microsoft 365 for business credentials, and then choose OneDrive.</span></span>

## <a name="try-it"></a><span data-ttu-id="71e4e-112">Essayez !</span><span class="sxs-lookup"><span data-stu-id="71e4e-112">Try it!</span></span>

### <a name="install-mover"></a><span data-ttu-id="71e4e-113">Installer Mover</span><span class="sxs-lookup"><span data-stu-id="71e4e-113">Install Mover</span></span>

1. <span data-ttu-id="71e4e-114">Connectez-vous à votre console d’administration Google Workspace [admin.google.com](https://admin.google.com).</span><span class="sxs-lookup"><span data-stu-id="71e4e-114">Sign in to your Google Workspace admin console at [admin.google.com](https://admin.google.com).</span></span>

1. <span data-ttu-id="71e4e-115">Choose **Apps**  >  **Google Workspace Marketplace apps** Add app to Domain Install  >  **list**.</span><span class="sxs-lookup"><span data-stu-id="71e4e-115">Choose **Apps** > **Google Workspace Marketplace apps** > **Add app to Domain Install list**.</span></span>

1. <span data-ttu-id="71e4e-116">Recherchez Mover et sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="71e4e-116">Search for Mover and select it.</span></span>

1. <span data-ttu-id="71e4e-117">Choose **Domain Install,** then **Continue**.</span><span class="sxs-lookup"><span data-stu-id="71e4e-117">Choose **Domain Install**, then **Continue**.</span></span>

1. <span data-ttu-id="71e4e-118">Examinez les autorisations, cochez la case pour accepter les termes, puis sélectionnez **Autoriser,** choisir **Suivant,** puis **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="71e4e-118">Review the permissions, select the checkbox to agree to the terms,then select **Allow**, choose **Next**, then **Done**.</span></span>

### <a name="create-connectors-and-run-the-migration"></a><span data-ttu-id="71e4e-119">Créer des connecteurs et exécuter la migration</span><span class="sxs-lookup"><span data-stu-id="71e4e-119">Create Connectors and run the migration</span></span>

1. <span data-ttu-id="71e4e-120">Revenir aux **applications Google Workspace Marketplace.**</span><span class="sxs-lookup"><span data-stu-id="71e4e-120">Return to **Google Workspace Marketplace apps**.</span></span>
1. <span data-ttu-id="71e4e-121">Actualisez votre navigateur et sélectionnez **l’application Mover.**</span><span class="sxs-lookup"><span data-stu-id="71e4e-121">Refresh your browser, and select the **Mover** app.</span></span>
1. <span data-ttu-id="71e4e-122">Faites défiler vers le bas et choisissez le lien de navigation universelle.</span><span class="sxs-lookup"><span data-stu-id="71e4e-122">Scroll down and choose the universal navigation link.</span></span>
1. <span data-ttu-id="71e4e-123">Sélectionnez **Autoriser un nouveau connecteur,** **recherchez G Suite (administrateur)** et choisissez **Autoriser.**</span><span class="sxs-lookup"><span data-stu-id="71e4e-123">Select **Authorize New Connector**, locate **G Suite (Admin)**, and choose **Authorize**.</span></span>
1. <span data-ttu-id="71e4e-124">Modifiez **le nom complet,** si vous le souhaitez, puis **sélectionnez Autoriser.**</span><span class="sxs-lookup"><span data-stu-id="71e4e-124">Change the **Display Name**, if you want, then select **Authorize**.</span></span>
1. <span data-ttu-id="71e4e-125">Choisissez un compte d’administrateur Google, examinez les autorisations, puis sélectionnez **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="71e4e-125">Choose a Google admin account, review the permissions,then select **Allow**.</span></span>

    <span data-ttu-id="71e4e-126">Mover affiche le nombre de lecteurs d’équipe et d’utilisateurs détectés.</span><span class="sxs-lookup"><span data-stu-id="71e4e-126">Mover displays the number of team drives and user drives it discovered.</span></span> 

1. <span data-ttu-id="71e4e-127">Under **Select destination**, choose **Authorize New Connector**, locate Office **365**, and select **Authorize**.</span><span class="sxs-lookup"><span data-stu-id="71e4e-127">Under **Select destination**, choose **Authorize New Connector**, locate **Office 365**, and select **Authorize**.</span></span>
1. <span data-ttu-id="71e4e-128">Pour accorder des autorisations à l’application Mover dans azure Active Directory, accédez [à aka.ms/Office365MoverAuth](https://aka.ms/Office365MoverAuth).</span><span class="sxs-lookup"><span data-stu-id="71e4e-128">To grant permissions to the Mover app in your Azure Active Directory, navigate to [aka.ms/Office365MoverAuth](https://aka.ms/Office365MoverAuth).</span></span>
1. <span data-ttu-id="71e4e-129">Sélectionnez **Office 365 Mover**, **Autorisations**, **Accorder le consentement administrateur pour votre entreprise**.</span><span class="sxs-lookup"><span data-stu-id="71e4e-129">Select **Office 365 Mover**, **Permissions**, **Grant admin consent for your company**.</span></span>
1. <span data-ttu-id="71e4e-130">Choisissez votre compte, examinez les autorisations, puis sélectionnez **Accepter.**</span><span class="sxs-lookup"><span data-stu-id="71e4e-130">Choose your account, review the permissions, and select **Accept**.</span></span>
1. <span data-ttu-id="71e4e-131">Choose **Properties** and verify that **User assignment required?** is turned on.</span><span class="sxs-lookup"><span data-stu-id="71e4e-131">Choose **Properties** and verify that **User assignment required?** is turned on.</span></span>
1. <span data-ttu-id="71e4e-132">Revenir à l’application Mover, modifier le nom **complet,** si vous le souhaitez, choisissez **Autoriser,** puis sélectionnez un compte d’administrateur Microsoft.</span><span class="sxs-lookup"><span data-stu-id="71e4e-132">Return to the Mover app, change the **Display Name**, if you want, choose **Authorize**,then select a Microsoft admin account.</span></span>

    <span data-ttu-id="71e4e-133">Mover vous informera du nombre de sites SharePoint Online (ou SPO) et d’utilisateurs qu’il a découverts.</span><span class="sxs-lookup"><span data-stu-id="71e4e-133">Mover will inform you about the number of SharePoint Online (or SPO) sites and users it discovered.</span></span>
1. <span data-ttu-id="71e4e-134">Choisissez **Continuer le programme d’installation de** la migration, **sélectionnez Ajouter des** utilisateurs, puis découvrir et ajouter automatiquement des **utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="71e4e-134">Choose **Continue Migration Setup**, select **Add Users**, then **Automatically Discover and Add Users**.</span></span>

    <span data-ttu-id="71e4e-135">L’application Mover tentera de maser les lecteurs du chemin d’accès source dans Google au chemin d’accès de destination dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="71e4e-135">The Mover app will attempt to map drives from the Source Path in Google, to the Destination Path in Microsoft 365.</span></span> 

    <span data-ttu-id="71e4e-136">Si un lecteur ne maque pas automatiquement, ajoutez son chemin de destination à un fichier CSV, que nous utiliserons ultérieurement pour migrer le lecteur partagé vers une bibliothèque de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="71e4e-136">If a drive doesn't map automatically, add its destination path to a CSV file, which we'll use later to migrate the shared drive to a SharePoint document library.</span></span> 

1. <span data-ttu-id="71e4e-137">Dans ce cas, nous avons ajouté un site SharePoint appelé Fichiers migrés et pris note de l’URL de la page de documents.</span><span class="sxs-lookup"><span data-stu-id="71e4e-137">In this case, we have added a SharePoint site called Migrated files, and taken note of the URL for the documents page.</span></span> 
1. <span data-ttu-id="71e4e-138">Nous avons ensuite créé un fichier CSV au format Chemin d’accès source, Chemin de destination et Balises.</span><span class="sxs-lookup"><span data-stu-id="71e4e-138">We then created a CSV file using the format of Source Path, Destination Path, and Tags.</span></span> 

    <span data-ttu-id="71e4e-139">Pour plus [d’informations, voir aka.ms/movercsv](https://docs.microsoft.com/sharepointmigration/mover-create-migration-csv).</span><span class="sxs-lookup"><span data-stu-id="71e4e-139">For details see [aka.ms/movercsv](https://docs.microsoft.com/sharepointmigration/mover-create-migration-csv).</span></span>

    <span data-ttu-id="71e4e-140">Lorsque vous ajoutez l’URL du chemin d’accès de destination, supprimez tout le texte après documents partagés.</span><span class="sxs-lookup"><span data-stu-id="71e4e-140">When adding the Destination Path URL, remove everything after Shared Documents.</span></span> <span data-ttu-id="71e4e-141">Par exemple, cette URL complète ne fonctionnera pas : `https://TENANT01.sharepoint.com/sites/SiteName/Shared Documents/Forms/AllItems.aspx`</span><span class="sxs-lookup"><span data-stu-id="71e4e-141">For example, this full URL won't work: `https://TENANT01.sharepoint.com/sites/SiteName/Shared Documents/Forms/AllItems.aspx`</span></span>

    <span data-ttu-id="71e4e-142">Remplacez-la par : `https://TENANT01.sharepoint.com/sites/SiteName/Shared Documents`</span><span class="sxs-lookup"><span data-stu-id="71e4e-142">Change it to: `https://TENANT01.sharepoint.com/sites/SiteName/Shared Documents`</span></span>

1. <span data-ttu-id="71e4e-143">Une fois votre fichier CSV prêt, sélectionnez Actions de **migration,** Ajouter à **la migration,** **Choisir un fichier à télécharger.**</span><span class="sxs-lookup"><span data-stu-id="71e4e-143">Once your CSV file is ready, select **Migration Actions**, **Add to Migration**, **Choose a file to upload**.</span></span>
1. <span data-ttu-id="71e4e-144">Accédez à votre fichier CSV, sélectionnez-le, puis choisissez **Ouvrir.**</span><span class="sxs-lookup"><span data-stu-id="71e4e-144">Navigate to your CSV file, select it,then choose **Open**.</span></span>
1. <span data-ttu-id="71e4e-145">Sélectionnez les lecteurs utilisateur dont vous souhaitez migrer les fichiers, puis **sélectionnez Démarrer la migration des utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="71e4e-145">Select the user drives whose files you want to migrate, then choose **Start Migrating Users**.</span></span>
1. <span data-ttu-id="71e4e-146">Examinez les informations de migration, choisissez quand commencer la migration, acceptez les conditions générales, puis sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="71e4e-146">Review the migration information, choose when to start the migration, agree to the **Terms and Conditions**, then select **Continue**.</span></span>

<span data-ttu-id="71e4e-147">L’application Mover vous informe lorsque le processus de migration est terminé.</span><span class="sxs-lookup"><span data-stu-id="71e4e-147">The Mover app will inform you when the migration process is complete.</span></span>
