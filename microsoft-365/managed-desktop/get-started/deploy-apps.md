---
title: Déployer des applications sur des appareils
description: Informations pour ajouter et déployer des applications sur des appareils de bureau gérés Microsoft.
keywords: Microsoft Managed Desktop, Microsoft 365, service, documentation, applications, applications métiers, applications métier
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: a064a41fc7ab69e31d49553f600dfd6bb91ef7b0
ms.sourcegitcommit: 9083036e787cf997fbceb19c66af594d0fa81d0f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/13/2019
ms.locfileid: "38302911"
---
# <a name="deploy-apps-to-devices"></a><span data-ttu-id="7ccc0-104">Déployer des applications sur des appareils</span><span class="sxs-lookup"><span data-stu-id="7ccc0-104">Deploy apps to devices</span></span>
<span data-ttu-id="7ccc0-105">L’intégration à Microsoft Managed Desktop inclut l’ajout et le déploiement d’applications sur les appareils de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-105">Part of onboarding to Microsoft Managed Desktop includes adding and deploying apps to your user’s devices.</span></span> <span data-ttu-id="7ccc0-106">Une fois que vous utilisez le portail de bureau géré Microsoft, vous pouvez ajouter et déployer vos applications.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-106">Once you're using the Microsoft Managed Desktop portal, you can add and deploy your apps.</span></span> 

<span data-ttu-id="7ccc0-107">Le processus global se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="7ccc0-107">The overall process looks like this:</span></span>
1. <span data-ttu-id="7ccc0-108">[Ajouter des applications au portail de bureau géré Microsoft](#1) -il peut s’agir d’applications métier existantes ou d’applications de Microsoft Store pour les entreprises que vous avez synchronisées avec Intune.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-108">[Add apps to Microsoft Managed Desktop portal](#1) - This can be existing line-of-business (LOB) apps, or apps from Microsoft Store for Business that you've synced with Intune.</span></span> 
2. <span data-ttu-id="7ccc0-109">[Créer des groupes Azure Active Directory (AD) pour l’affectation d’application](#2) : vous utiliserez ces groupes pour gérer l’affectation d’application.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-109">[Create Azure Active Directory (AD) groups for app assignment](#2) - You'll use these groups to manage app assignment.</span></span>
3. [<span data-ttu-id="7ccc0-110">Affecter des applications à vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7ccc0-110">Assign apps to your users</span></span>](#3)

<span id="1" />

## <a name="step-1-add-apps-to-microsoft-managed-desktop-portal"></a><span data-ttu-id="7ccc0-111">Étape 1 : ajouter des applications au portail de bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="7ccc0-111">Step 1: Add apps to Microsoft Managed Desktop portal</span></span>
<span data-ttu-id="7ccc0-112">Vous pouvez ajouter des [applications Win32 ou Windows MSI](#lob-apps), ou [des applications Microsoft Store pour les entreprises](#msfb-apps) à Microsoft Managed Desktop, puis les déployer sur des appareils de bureau gérés Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-112">You can add [Win32, or Windows MSI-based apps](#lob-apps), or [Microsoft Store for Business apps](#msfb-apps) to Microsoft Managed Desktop, and then deploy them to Microsoft Managed Desktop devices.</span></span>

<span id="lob-apps">

###  <a name="win32-or-windows-msi-based-apps-to-microsoft-managed-desktop"></a><span data-ttu-id="7ccc0-113">Applications Win32 ou Windows MSI à Microsoft Managed Desktop</span><span class="sxs-lookup"><span data-stu-id="7ccc0-113">Win32 or Windows MSI-based apps to Microsoft Managed Desktop</span></span>

<span data-ttu-id="7ccc0-114">Vous pouvez ajouter vos applications métier à Microsoft Managed Desktop Portal.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-114">You can add your line-of-business (LOB) apps to Microsoft Managed Desktop portal.</span></span> <span data-ttu-id="7ccc0-115">Pour plus d’informations sur les conditions requises pour les applications installées sur les appareils de bureau géré Microsoft, consultez la rubrique [conditions requises pour les applications de bureau géré Microsoft](https://docs.microsoft.com/microsoft-365/managed-desktop/service-description/mmd-app-requirements).</span><span class="sxs-lookup"><span data-stu-id="7ccc0-115">For information on requirements for apps installed on Microsoft Managed Desktop devices, see [Microsoft Managed Desktop app requirements](https://docs.microsoft.com/microsoft-365/managed-desktop/service-description/mmd-app-requirements).</span></span>

<span data-ttu-id="7ccc0-116">Dans cette procédure, vous allez sélectionner le type d’application que vous souhaitez ajouter, puis configurer et télécharger la source de l’application.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-116">In this procedure, you'll select which kind of app you want to add, and then configure and upload the app source.</span></span> 

<span data-ttu-id="7ccc0-117">**Pour ajouter votre application LOB ou votre application Windows au portail de bureau géré Microsoft**</span><span class="sxs-lookup"><span data-stu-id="7ccc0-117">**To add your LOB app or Windows app to Microsoft Managed Desktop portal**</span></span>

<span data-ttu-id="7ccc0-118">Vous pouvez vous connecter à Microsoft Managed Desktop Portal ou vous connecter à Intune, puis rechercher le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-118">You can sign in to Microsoft Managed Desktop portal, or sign in to Intune and then search for Microsoft Managed Desktop.</span></span> <span data-ttu-id="7ccc0-119">Nous allons afficher la connexion à Microsoft Managed Desktop Portal.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-119">We'll show signing in to Microsoft Managed Desktop portal.</span></span> 

1.  <span data-ttu-id="7ccc0-120">Connectez-vous au [portail d’administration de bureau géré Microsoft](https://aka.ms/mmdportal).</span><span class="sxs-lookup"><span data-stu-id="7ccc0-120">Sign in to [Microsoft Managed Desktop Admin portal](https://aka.ms/mmdportal).</span></span> 
2.  <span data-ttu-id="7ccc0-121">Sous **inventaire**, sélectionnez **applications**.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-121">Under **Inventory**, select **Apps**.</span></span>
3.  <span data-ttu-id="7ccc0-122">Dans la charge de travail applications, sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-122">In the Apps workload, select **Add**.</span></span>
4.  <span data-ttu-id="7ccc0-123">Dans **Ajouter une application**, sélectionnez **application métier** ou **application Windows (Win32)**.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-123">In **Add app**, select **Line-of-business app** or **Windows app (Win32)**.</span></span>
    - <span data-ttu-id="7ccc0-124">Si vous avez sélectionné **application métier**, voir [Add a Windows Line of Business app to Microsoft Intune](https://docs.microsoft.com/intune/lob-apps-windows) pour obtenir des instructions sur l’ajout et la configuration d’applications métiers.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-124">If you selected **Line-of-business app**, see [Add a Windows line-of-business app to Microsoft Intune](https://docs.microsoft.com/intune/lob-apps-windows) for instruction on adding and configuring line-of-business apps.</span></span>
    - <span data-ttu-id="7ccc0-125">Si vous avez sélectionné **Windows App (Win32)**, voir [Win32 App Management](https://docs.microsoft.com/intune/apps-win32-app-management) pour obtenir des instructions sur l’ajout et la configuration d’applications Windows.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-125">If you selected **Windows app (Win32)**, see [Win32 app management](https://docs.microsoft.com/intune/apps-win32-app-management) for instruction on adding and configuring Windows apps.</span></span>

<span id="msfb-apps">

### <a name="microsoft-store-for-business-apps"></a><span data-ttu-id="7ccc0-126">Applications Microsoft Store pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="7ccc0-126">Microsoft Store for Business apps</span></span>
<span data-ttu-id="7ccc0-127">Si vous ne vous êtes pas inscrit auprès de Microsoft Store pour les entreprises, vous pouvez vous inscrire lorsque vous achetez des applications.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-127">If you haven't signed up with Microsoft Store for Business, you can sign up when you shop for apps.</span></span> <span data-ttu-id="7ccc0-128">Une fois que vous avez vos applications, vous pouvez les synchroniser avec le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-128">After you have your apps, you can sync them with Microsoft Managed Desktop.</span></span> 

<span data-ttu-id="7ccc0-129">**Pour acheter des applications à partir de Microsoft Store pour les entreprises**</span><span class="sxs-lookup"><span data-stu-id="7ccc0-129">**To buy apps from the Microsoft Store for Business**</span></span>

1. <span data-ttu-id="7ccc0-130">Connectez-vous à [Microsoft Store pour entreprises](https://businessstore.microsoft.com) avec votre compte d’administrateur Microsoft Store pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-130">Sign in to [Microsoft Store for Business](https://businessstore.microsoft.com) with your Microsoft Store for Business Admin account.</span></span>
2. <span data-ttu-id="7ccc0-131">Sélectionnez **acheter pour mon groupe**.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-131">Select **Shop for my group**.</span></span>
3. <span data-ttu-id="7ccc0-132">Utilisez la recherche pour trouver l’application de votre choix, puis sélectionnez l’application.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-132">Use Search to find that the app that you want, and select the app.</span></span>
4. <span data-ttu-id="7ccc0-133">Dans les détails du produit, sélectionnez **obtenir l’application**.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-133">On the product details, select **Get the App**.</span></span> <span data-ttu-id="7ccc0-134">Le Microsoft Store ajoute l’application aux **produits & services** de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-134">Microsoft Store adds the app to **Products & services** for your organization.</span></span>

<span data-ttu-id="7ccc0-135">**Pour forcer une synchronisation entre Intune et Microsoft Store pour les entreprises**</span><span class="sxs-lookup"><span data-stu-id="7ccc0-135">**To force a sync between Intune and Microsoft Store for Business**</span></span>
1. <span data-ttu-id="7ccc0-136">Se connecter au [portail Azure](https://portal.azure.com/) en tant qu’administrateur Intune ou administrateur global pour votre client</span><span class="sxs-lookup"><span data-stu-id="7ccc0-136">Sign in to [Azure Portal](https://portal.azure.com/) as Intune Admin or Global Admin for your tenant</span></span>
2. <span data-ttu-id="7ccc0-137">Sélectionnez **tous les services > Intune**.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-137">Select **All services > Intune**.</span></span> <span data-ttu-id="7ccc0-138">Intune se trouve dans la section surveillance + Management.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-138">Intune is in the Monitoring + Management section.</span></span>
3. <span data-ttu-id="7ccc0-139">Dans le volet Intune, sélectionnez **applications clientes**, puis sélectionnez **Microsoft Store pour les entreprises**.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-139">In the Intune pane, select **Client Apps**, and then select **Microsoft Store for Business**.</span></span>
4. <span data-ttu-id="7ccc0-140">Sélectionnez **activer** pour synchroniser vos applications Microsoft Store pour les entreprises avec Intune.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-140">Select **Enable** to sync your Microsoft Store for Business apps with Intune.</span></span>
    - <span data-ttu-id="7ccc0-141">Si vous ne l’avez pas encore fait, inscrivez-vous et associez votre compte Microsoft Store pour les entreprises avec Intune</span><span class="sxs-lookup"><span data-stu-id="7ccc0-141">If you haven't already, sign up and associate your Microsoft Store for Business account with Intune</span></span>
    - <span data-ttu-id="7ccc0-142">Sélectionnez la langue dans laquelle les applications de Microsoft Store pour les entreprises seront affichées dans votre console Intune.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-142">Select the language in which apps from the Microsoft Store for Business will be displayed in your Intune console</span></span>
    - <span data-ttu-id="7ccc0-143">Sélectionnez **synchroniser** pour synchroniser vos applications Microsoft Store pour les entreprises avec Intune.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-143">Select **Sync** to sync your Microsoft Store for Business apps with Intune.</span></span>
    - <span data-ttu-id="7ccc0-144">Vérifiez que la synchronisation entre Microsoft Store pour les entreprises et Intune est active (étape suivante).</span><span class="sxs-lookup"><span data-stu-id="7ccc0-144">Verify that the sync between Microsoft Store for Business and Intune is active (next step).</span></span> 

<span data-ttu-id="7ccc0-145">**Pour vérifier qu’une synchronisation entre Intune et Microsoft Store pour les entreprises est active**</span><span class="sxs-lookup"><span data-stu-id="7ccc0-145">**To verify that a sync between Intune and Microsoft Store for Business is active**</span></span>
1. <span data-ttu-id="7ccc0-146">Connectez-vous à [Microsoft Store pour entreprises](https://businessstore.microsoft.com) avec votre compte d’administrateur Microsoft Store pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-146">Sign in to [Microsoft Store for Business](https://businessstore.microsoft.com) with your Microsoft Store for Business Admin account.</span></span>
2. <span data-ttu-id="7ccc0-147">Sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-147">Select **Manage**.</span></span>
3. <span data-ttu-id="7ccc0-148">Sélectionnez **paramètres** , puis **distribuer**.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-148">Select **Settings** and then select **Distribute**.</span></span>
4. <span data-ttu-id="7ccc0-149">Sous **outils de gestion**, vérifiez que Intune est affiché et que l’État est **actif**.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-149">Under **Management tools**, verify that Intune is listed and that the status is **Active**.</span></span>  

<span id="2" />

## <a name="step-2-create-azure-ad-groups"></a><span data-ttu-id="7ccc0-150">Étape 2 : créer des groupes Azure AD</span><span class="sxs-lookup"><span data-stu-id="7ccc0-150">Step 2: Create Azure AD groups</span></span>

<span data-ttu-id="7ccc0-151">Créez trois groupes Azure AD pour chaque application.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-151">Create three Azure AD groups for each app.</span></span> <span data-ttu-id="7ccc0-152">Ce tableau décrit les groupes dont vous aurez besoin (disponible, requis et désinstallation).</span><span class="sxs-lookup"><span data-stu-id="7ccc0-152">This table outlines the groups you'll need (Available, Required, and Uninstall).</span></span> 

<span data-ttu-id="7ccc0-153">Type d’affectation d’application</span><span class="sxs-lookup"><span data-stu-id="7ccc0-153">App assignment type</span></span> |   <span data-ttu-id="7ccc0-154">Utilisation de groupe</span><span class="sxs-lookup"><span data-stu-id="7ccc0-154">Group use</span></span>   | <span data-ttu-id="7ccc0-155">Exemple de nom Azure AD</span><span class="sxs-lookup"><span data-stu-id="7ccc0-155">Example Azure AD name</span></span>
--- | --- | ---
<span data-ttu-id="7ccc0-156">Available</span><span class="sxs-lookup"><span data-stu-id="7ccc0-156">Available</span></span> |  <span data-ttu-id="7ccc0-157">L’application sera disponible à partir de l’application ou du site Web du portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-157">The app will be available from Company Portal app or website.</span></span> | <span data-ttu-id="7ccc0-158">MMD – *nom* de l’application – disponible</span><span class="sxs-lookup"><span data-stu-id="7ccc0-158">MMD – *app name* – Available</span></span>
<span data-ttu-id="7ccc0-159">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7ccc0-159">Required</span></span> |  <span data-ttu-id="7ccc0-160">L’application est installée sur les appareils dans les groupes sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-160">The app is installed on devices in the selected groups.</span></span> | <span data-ttu-id="7ccc0-161">MMD – *nom* de l’application – obligatoire</span><span class="sxs-lookup"><span data-stu-id="7ccc0-161">MMD – *app name* – Required</span></span>
<span data-ttu-id="7ccc0-162">Uninstall</span><span class="sxs-lookup"><span data-stu-id="7ccc0-162">Uninstall</span></span> |  <span data-ttu-id="7ccc0-163">L’application est désinstallée des appareils dans les groupes sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-163">The app is uninstalled from devices in the selected groups.</span></span> | <span data-ttu-id="7ccc0-164">MMD – *nom* de l’application – Uninstall</span><span class="sxs-lookup"><span data-stu-id="7ccc0-164">MMD – *app name* – Uninstall</span></span>

<span data-ttu-id="7ccc0-165">Ajoutez vos utilisateurs à ces groupes pour que l’application soit disponible, installez l’application ou supprimez l’application de son appareil de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-165">Add your users to these groups to either make the app availabe, install the app, or remove the app from their Microsoft Managed Desktop device.</span></span> 

<span id="3" />

## <a name="step-3-assign-apps-to-your-users"></a><span data-ttu-id="7ccc0-166">Étape 3 : attribuer des applications à vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7ccc0-166">Step 3: Assign apps to your users</span></span>

<span data-ttu-id="7ccc0-167">**Pour affecter l’application à vos utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="7ccc0-167">**To assign the app to your users**</span></span>

1. <span data-ttu-id="7ccc0-168">Connectez-vous au [portail d’administration de bureau géré Microsoft](https://aka.ms/mmdportal).</span><span class="sxs-lookup"><span data-stu-id="7ccc0-168">Sign in to [Microsoft Managed Desktop Admin portal](https://aka.ms/mmdportal).</span></span>
2. <span data-ttu-id="7ccc0-169">Dans le volet bureau géré, sélectionnez **applications**.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-169">In Managed Desktop pane, select **Apps**.</span></span>
3. <span data-ttu-id="7ccc0-170">Dans la charge de travail applications, sélectionnez l’application à laquelle vous souhaitez attribuer des utilisateurs et sélectionnez **affecter des groupes d’utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-170">In the Apps workload, select the app you want to assign users to and select **Assign users groups**.</span></span>
4. <span data-ttu-id="7ccc0-171">Pour l’application spécifique, sélectionnez un type d’affectation (disponible, obligatoire, désinstaller) et affectez le groupe approprié.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-171">For the specific app, select an assignment type (Available, Required, Uninstall) and assign the appropriate group.</span></span>
5. <span data-ttu-id="7ccc0-172">Dans le volet attribuer des applications, sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ccc0-172">In the Assign Apps pane, select **OK**.</span></span>


## <a name="steps-to-get-started-with-microsoft-managed-desktop"></a><span data-ttu-id="7ccc0-173">Étapes de prise en main de Microsoft Managed Desktop</span><span class="sxs-lookup"><span data-stu-id="7ccc0-173">Steps to get started with Microsoft Managed Desktop</span></span>

1. [<span data-ttu-id="7ccc0-174">Ajouter et vérifier des contacts d’administration dans le portail d’administration</span><span class="sxs-lookup"><span data-stu-id="7ccc0-174">Add and verify admin contacts in the Admin portal</span></span>](add-admin-contacts.md)
2. [<span data-ttu-id="7ccc0-175">Ajustement de l’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="7ccc0-175">Adjust conditional access</span></span>](conditional-access.md)
3. [<span data-ttu-id="7ccc0-176">Attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="7ccc0-176">Assign licenses</span></span>](assign-licenses.md)
4. [<span data-ttu-id="7ccc0-177">Déployer le portail d’entreprise Intune</span><span class="sxs-lookup"><span data-stu-id="7ccc0-177">Deploy Intune Company Portal</span></span>](company-portal.md)
5. [<span data-ttu-id="7ccc0-178">Activer l’itinérance de l’état d’entreprise</span><span class="sxs-lookup"><span data-stu-id="7ccc0-178">Enable Enterprise State Roaming</span></span>](enterprise-state-roaming.md)
6. [<span data-ttu-id="7ccc0-179">Configurer les appareils</span><span class="sxs-lookup"><span data-stu-id="7ccc0-179">Set up devices</span></span>](set-up-devices.md)
7. [<span data-ttu-id="7ccc0-180">Préparer vos utilisateurs à l’utilisation des appareils</span><span class="sxs-lookup"><span data-stu-id="7ccc0-180">Get your users ready to use devices</span></span>](get-started-devices.md)
8. <span data-ttu-id="7ccc0-181">Déployer des applications (cette rubrique)</span><span class="sxs-lookup"><span data-stu-id="7ccc0-181">Deploy apps (this topic)</span></span>


<!--# Preparing apps for Microsoft Managed Desktop

This topic is the target for 2 "Learn more" links in the Admin Portal (aka.ms/app-overview;app-package); also target for link from Online resources (aka.ms/app-overviewmmd-app-prep) do not delete.

-->
