---
title: Déployer les applications sur les appareils
description: Informations pour ajouter et déployer des applications sur des appareils de bureau gérés Microsoft.
keywords: Microsoft Managed Desktop, Microsoft 365, service, documentation, applications, applications métiers, applications métier
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: 2eb8b984550f301af9d99e738f6db4623aa2cc86
ms.sourcegitcommit: 6647055154002c7d3b8f7ce25ad53c9636bc8066
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2020
ms.locfileid: "48769105"
---
# <a name="deploy-apps-to-devices"></a><span data-ttu-id="a6e03-104">Déployer les applications sur les appareils</span><span class="sxs-lookup"><span data-stu-id="a6e03-104">Deploy apps to devices</span></span>
<span data-ttu-id="a6e03-105">L’intégration à Microsoft Managed Desktop inclut l’ajout et le déploiement d’applications sur les appareils de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a6e03-105">Part of onboarding to Microsoft Managed Desktop includes adding and deploying apps to your user's devices.</span></span> <span data-ttu-id="a6e03-106">Une fois que vous utilisez le portail de bureau géré Microsoft, vous pouvez ajouter et déployer vos applications.</span><span class="sxs-lookup"><span data-stu-id="a6e03-106">Once you're using the Microsoft Managed Desktop portal, you can add and deploy your apps.</span></span> 

<span data-ttu-id="a6e03-107">Le processus global se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="a6e03-107">The overall process looks like this:</span></span>
1. <span data-ttu-id="a6e03-108">[Ajouter des applications au portail de bureau géré Microsoft](#1) -il peut s’agir d’applications métier existantes ou d’applications de Microsoft Store pour les entreprises que vous avez synchronisées avec Intune.</span><span class="sxs-lookup"><span data-stu-id="a6e03-108">[Add apps to Microsoft Managed Desktop portal](#1) - This can be existing line-of-business (LOB) apps, or apps from Microsoft Store for Business that you've synced with Intune.</span></span> 
2. <span data-ttu-id="a6e03-109">[Créer des groupes Azure Active Directory (AD) pour l’affectation d’application](#2) : vous utiliserez ces groupes pour gérer l’affectation d’application.</span><span class="sxs-lookup"><span data-stu-id="a6e03-109">[Create Azure Active Directory (AD) groups for app assignment](#2) - You'll use these groups to manage app assignment.</span></span>
3. [<span data-ttu-id="a6e03-110">Affecter des applications à vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a6e03-110">Assign apps to your users</span></span>](#3)

<span id="1" />

## <a name="step-1-add-apps-to-microsoft-managed-desktop-portal"></a><span data-ttu-id="a6e03-111">Étape 1 : ajouter des applications au portail de bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="a6e03-111">Step 1: Add apps to Microsoft Managed Desktop portal</span></span>
<span data-ttu-id="a6e03-112">Vous pouvez ajouter des [applications Win32 ou Windows MSI](#lob-apps), ou [des applications Microsoft Store pour les entreprises](#msfb-apps) à Microsoft Managed Desktop, puis les déployer sur des appareils de bureau gérés Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a6e03-112">You can add [Win32, or Windows MSI-based apps](#lob-apps), or [Microsoft Store for Business apps](#msfb-apps) to Microsoft Managed Desktop, and then deploy them to Microsoft Managed Desktop devices.</span></span>

<span id="lob-apps">

###  <a name="win32-or-windows-msi-based-apps-to-microsoft-managed-desktop"></a><span data-ttu-id="a6e03-113">Applications Win32 ou Windows MSI à Microsoft Managed Desktop</span><span class="sxs-lookup"><span data-stu-id="a6e03-113">Win32 or Windows MSI-based apps to Microsoft Managed Desktop</span></span>

<span data-ttu-id="a6e03-114">Vous pouvez ajouter vos applications métier à Microsoft Managed Desktop Portal.</span><span class="sxs-lookup"><span data-stu-id="a6e03-114">You can add your line-of-business (LOB) apps to Microsoft Managed Desktop portal.</span></span> <span data-ttu-id="a6e03-115">Pour plus d’informations sur les conditions requises pour les applications installées sur les appareils de bureau géré Microsoft, consultez la rubrique [conditions requises pour les applications de bureau géré Microsoft](https://docs.microsoft.com/microsoft-365/managed-desktop/service-description/mmd-app-requirements).</span><span class="sxs-lookup"><span data-stu-id="a6e03-115">For information on requirements for apps installed on Microsoft Managed Desktop devices, see [Microsoft Managed Desktop app requirements](https://docs.microsoft.com/microsoft-365/managed-desktop/service-description/mmd-app-requirements).</span></span>

<span data-ttu-id="a6e03-116">Dans cette procédure, vous allez sélectionner le type d’application que vous souhaitez ajouter, puis configurer et télécharger la source de l’application.</span><span class="sxs-lookup"><span data-stu-id="a6e03-116">In this procedure, you'll select which kind of app you want to add, and then configure and upload the app source.</span></span> 

<span data-ttu-id="a6e03-117">**Pour ajouter votre application LOB ou votre application Windows au portail de bureau géré Microsoft**</span><span class="sxs-lookup"><span data-stu-id="a6e03-117">**To add your LOB app or Windows app to Microsoft Managed Desktop portal**</span></span>

<span data-ttu-id="a6e03-118">Vous pouvez vous connecter à Microsoft Managed Desktop Portal ou vous connecter à Intune, puis rechercher le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a6e03-118">You can sign in to Microsoft Managed Desktop portal, or sign in to Intune and then search for Microsoft Managed Desktop.</span></span> <span data-ttu-id="a6e03-119">Nous allons afficher la connexion à Microsoft Managed Desktop Portal.</span><span class="sxs-lookup"><span data-stu-id="a6e03-119">We'll show signing in to Microsoft Managed Desktop portal.</span></span> 

1.    <span data-ttu-id="a6e03-120">Connectez-vous au [portail d’administration de bureau géré Microsoft](https://aka.ms/mmdportal).</span><span class="sxs-lookup"><span data-stu-id="a6e03-120">Sign in to [Microsoft Managed Desktop Admin portal](https://aka.ms/mmdportal).</span></span> 
2.    <span data-ttu-id="a6e03-121">Sous **inventaire** , sélectionnez **applications** .</span><span class="sxs-lookup"><span data-stu-id="a6e03-121">Under **Inventory** , select **Apps** .</span></span>
3.    <span data-ttu-id="a6e03-122">Dans la charge de travail applications, sélectionnez **Ajouter** .</span><span class="sxs-lookup"><span data-stu-id="a6e03-122">In the Apps workload, select **Add** .</span></span>
4.    <span data-ttu-id="a6e03-123">Dans **Ajouter une application** , sélectionnez **application métier** ou **application Windows (Win32)** .</span><span class="sxs-lookup"><span data-stu-id="a6e03-123">In **Add app** , select **Line-of-business app** or **Windows app (Win32)** .</span></span>
    - <span data-ttu-id="a6e03-124">Si vous avez sélectionné **application métier** , voir [Add a Windows Line of Business app to Microsoft Intune](https://docs.microsoft.com/intune/lob-apps-windows) pour obtenir des instructions sur l’ajout et la configuration d’applications métiers.</span><span class="sxs-lookup"><span data-stu-id="a6e03-124">If you selected **Line-of-business app** , see [Add a Windows line-of-business app to Microsoft Intune](https://docs.microsoft.com/intune/lob-apps-windows) for instruction on adding and configuring line-of-business apps.</span></span>
    - <span data-ttu-id="a6e03-125">Si vous avez sélectionné **Windows App (Win32)** , voir [Win32 App Management](https://docs.microsoft.com/intune/apps-win32-app-management) pour obtenir des instructions sur l’ajout et la configuration d’applications Windows.</span><span class="sxs-lookup"><span data-stu-id="a6e03-125">If you selected **Windows app (Win32)** , see [Win32 app management](https://docs.microsoft.com/intune/apps-win32-app-management) for instruction on adding and configuring Windows apps.</span></span>

<span id="msfb-apps">

### <a name="microsoft-store-for-business-apps"></a><span data-ttu-id="a6e03-126">Applications Microsoft Store pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="a6e03-126">Microsoft Store for Business apps</span></span>
<span data-ttu-id="a6e03-127">Si vous ne vous êtes pas inscrit auprès de Microsoft Store pour les entreprises, vous pouvez vous inscrire lorsque vous achetez des applications.</span><span class="sxs-lookup"><span data-stu-id="a6e03-127">If you haven't signed up with Microsoft Store for Business, you can sign up when you shop for apps.</span></span> <span data-ttu-id="a6e03-128">Une fois que vous avez vos applications, vous pouvez les synchroniser avec le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a6e03-128">After you have your apps, you can sync them with Microsoft Managed Desktop.</span></span> 

<span data-ttu-id="a6e03-129">**Pour acheter des applications à partir de Microsoft Store pour les entreprises**</span><span class="sxs-lookup"><span data-stu-id="a6e03-129">**To buy apps from the Microsoft Store for Business**</span></span>

1. <span data-ttu-id="a6e03-130">Connectez-vous à [Microsoft Store pour entreprises](https://businessstore.microsoft.com) avec votre compte d’administrateur Microsoft Store pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="a6e03-130">Sign in to [Microsoft Store for Business](https://businessstore.microsoft.com) with your Microsoft Store for Business Admin account.</span></span>
2. <span data-ttu-id="a6e03-131">Sélectionnez **acheter pour mon groupe** .</span><span class="sxs-lookup"><span data-stu-id="a6e03-131">Select **Shop for my group** .</span></span>
3. <span data-ttu-id="a6e03-132">Utilisez la recherche pour trouver l’application de votre choix, puis sélectionnez l’application.</span><span class="sxs-lookup"><span data-stu-id="a6e03-132">Use Search to find that the app that you want, and select the app.</span></span>
4. <span data-ttu-id="a6e03-133">Dans les détails du produit, sélectionnez **obtenir l’application** .</span><span class="sxs-lookup"><span data-stu-id="a6e03-133">On the product details, select **Get the App** .</span></span> <span data-ttu-id="a6e03-134">Microsoft Store ajoute l’application à **vos produits** pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a6e03-134">Microsoft Store adds the app to **Your products** for your organization.</span></span>

<span data-ttu-id="a6e03-135">**Pour forcer une synchronisation entre Intune et Microsoft Store pour les entreprises**</span><span class="sxs-lookup"><span data-stu-id="a6e03-135">**To force a sync between Intune and Microsoft Store for Business**</span></span>
1. <span data-ttu-id="a6e03-136">Connectez-vous au [Centre d’administration du gestionnaire de points de terminaison Microsoft](https://go.microsoft.com/fwlink/?linkid=2109431).</span><span class="sxs-lookup"><span data-stu-id="a6e03-136">Sign in to the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431).</span></span>
2. <span data-ttu-id="a6e03-137">Sélectionnez **Tenant administration** les  >  **connecteurs et les jetons**  >  **d’administration du client Microsoft Store pour les entreprises** .</span><span class="sxs-lookup"><span data-stu-id="a6e03-137">Select **Tenant administration** > **Connectors and tokens** > **Microsoft Store for Business** .</span></span>
3. <span data-ttu-id="a6e03-138">Sélectionnez **synchroniser** pour obtenir les applications que vous avez achetées à partir du Microsoft Store dans Intune.</span><span class="sxs-lookup"><span data-stu-id="a6e03-138">Select **Sync** to get the apps you've purchased from the Microsoft Store into Intune.</span></span>

<span data-ttu-id="a6e03-139">**Pour vérifier qu’une synchronisation entre Intune et Microsoft Store pour les entreprises est active**</span><span class="sxs-lookup"><span data-stu-id="a6e03-139">**To verify that a sync between Intune and Microsoft Store for Business is active**</span></span>
1. <span data-ttu-id="a6e03-140">Connectez-vous à [Microsoft Store pour entreprises](https://businessstore.microsoft.com) avec votre compte d’administrateur Microsoft Store pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="a6e03-140">Sign in to [Microsoft Store for Business](https://businessstore.microsoft.com) with your Microsoft Store for Business Admin account.</span></span>
2. <span data-ttu-id="a6e03-141">Sélectionnez **gérer** .</span><span class="sxs-lookup"><span data-stu-id="a6e03-141">Select **Manage** .</span></span>
3. <span data-ttu-id="a6e03-142">Sélectionnez **paramètres** , puis **distribuer** .</span><span class="sxs-lookup"><span data-stu-id="a6e03-142">Select **Settings** and then select **Distribute** .</span></span>
4. <span data-ttu-id="a6e03-143">Sous **outils de gestion** , vérifiez que Intune est affiché et que l’État est **actif** .</span><span class="sxs-lookup"><span data-stu-id="a6e03-143">Under **Management tools** , verify that Intune is listed and that the status is **Active** .</span></span>  

<span id="2" />

## <a name="step-2-create-azure-ad-groups"></a><span data-ttu-id="a6e03-144">Étape 2 : créer des groupes Azure AD</span><span class="sxs-lookup"><span data-stu-id="a6e03-144">Step 2: Create Azure AD groups</span></span>

<span data-ttu-id="a6e03-145">Créez trois groupes Azure AD pour chaque application.</span><span class="sxs-lookup"><span data-stu-id="a6e03-145">Create three Azure AD groups for each app.</span></span> <span data-ttu-id="a6e03-146">Ce tableau décrit les groupes dont vous aurez besoin (disponible, requis et désinstallation).</span><span class="sxs-lookup"><span data-stu-id="a6e03-146">This table outlines the groups you'll need (Available, Required, and Uninstall).</span></span> 

<span data-ttu-id="a6e03-147">Type d’affectation d’application</span><span class="sxs-lookup"><span data-stu-id="a6e03-147">App assignment type</span></span> |    <span data-ttu-id="a6e03-148">Utilisation de groupe</span><span class="sxs-lookup"><span data-stu-id="a6e03-148">Group use</span></span>    | <span data-ttu-id="a6e03-149">Exemple de nom Azure AD</span><span class="sxs-lookup"><span data-stu-id="a6e03-149">Example Azure AD name</span></span>
--- | --- | ---
<span data-ttu-id="a6e03-150">Available</span><span class="sxs-lookup"><span data-stu-id="a6e03-150">Available</span></span> |  <span data-ttu-id="a6e03-151">L’application sera disponible à partir de l’application ou du site Web du portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="a6e03-151">The app will be available from Company Portal app or website.</span></span> | <span data-ttu-id="a6e03-152">MMD – *nom* de l’application – disponible</span><span class="sxs-lookup"><span data-stu-id="a6e03-152">MMD – *app name* – Available</span></span>
<span data-ttu-id="a6e03-153">Requis</span><span class="sxs-lookup"><span data-stu-id="a6e03-153">Required</span></span> |  <span data-ttu-id="a6e03-154">L’application est installée sur les appareils dans les groupes sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="a6e03-154">The app is installed on devices in the selected groups.</span></span> | <span data-ttu-id="a6e03-155">MMD – *nom* de l’application – obligatoire</span><span class="sxs-lookup"><span data-stu-id="a6e03-155">MMD – *app name* – Required</span></span>
<span data-ttu-id="a6e03-156">Uninstall</span><span class="sxs-lookup"><span data-stu-id="a6e03-156">Uninstall</span></span> |  <span data-ttu-id="a6e03-157">L’application est désinstallée des appareils dans les groupes sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="a6e03-157">The app is uninstalled from devices in the selected groups.</span></span> | <span data-ttu-id="a6e03-158">MMD – *nom* de l’application – Uninstall</span><span class="sxs-lookup"><span data-stu-id="a6e03-158">MMD – *app name* – Uninstall</span></span>

<span data-ttu-id="a6e03-159">Ajoutez vos utilisateurs à ces groupes pour que l’application soit disponible, installez l’application ou supprimez l’application de son appareil de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a6e03-159">Add your users to these groups to either make the app available, install the app, or remove the app from their Microsoft Managed Desktop device.</span></span> 

<span id="3" />

## <a name="step-3-assign-apps-to-your-users"></a><span data-ttu-id="a6e03-160">Étape 3 : attribuer des applications à vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a6e03-160">Step 3: Assign apps to your users</span></span>

<span data-ttu-id="a6e03-161">**Pour affecter l’application à vos utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="a6e03-161">**To assign the app to your users**</span></span>

1. <span data-ttu-id="a6e03-162">Connectez-vous au [portail d’administration de bureau géré Microsoft](https://aka.ms/mmdportal).</span><span class="sxs-lookup"><span data-stu-id="a6e03-162">Sign in to [Microsoft Managed Desktop Admin portal](https://aka.ms/mmdportal).</span></span>
2. <span data-ttu-id="a6e03-163">Dans le volet bureau géré, sélectionnez **applications** .</span><span class="sxs-lookup"><span data-stu-id="a6e03-163">In Managed Desktop pane, select **Apps** .</span></span>
3. <span data-ttu-id="a6e03-164">Dans la charge de travail applications, sélectionnez l’application à laquelle vous souhaitez attribuer des utilisateurs et sélectionnez **affecter des groupes d’utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="a6e03-164">In the Apps workload, select the app you want to assign users to and select **Assign users groups** .</span></span>
4. <span data-ttu-id="a6e03-165">Pour l’application spécifique, sélectionnez un type d’affectation (disponible, obligatoire, désinstaller) et affectez le groupe approprié.</span><span class="sxs-lookup"><span data-stu-id="a6e03-165">For the specific app, select an assignment type (Available, Required, Uninstall) and assign the appropriate group.</span></span>
5. <span data-ttu-id="a6e03-166">Dans le volet attribuer des applications, sélectionnez **OK** .</span><span class="sxs-lookup"><span data-stu-id="a6e03-166">In the Assign Apps pane, select **OK** .</span></span>


## <a name="steps-to-get-started-with-microsoft-managed-desktop"></a><span data-ttu-id="a6e03-167">Étapes de prise en main de Microsoft Managed Desktop</span><span class="sxs-lookup"><span data-stu-id="a6e03-167">Steps to get started with Microsoft Managed Desktop</span></span>

1. [<span data-ttu-id="a6e03-168">Ajouter et vérifier des contacts d’administrateur dans le portail d’administration</span><span class="sxs-lookup"><span data-stu-id="a6e03-168">Add and verify admin contacts in the Admin portal</span></span>](add-admin-contacts.md)
2. [<span data-ttu-id="a6e03-169">Ajuster l’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="a6e03-169">Adjust conditional access</span></span>](conditional-access.md)
3. [<span data-ttu-id="a6e03-170">Affecter des licences</span><span class="sxs-lookup"><span data-stu-id="a6e03-170">Assign licenses</span></span>](assign-licenses.md)
4. [<span data-ttu-id="a6e03-171">Déployer le portail d’entreprise Intune</span><span class="sxs-lookup"><span data-stu-id="a6e03-171">Deploy Intune Company Portal</span></span>](company-portal.md)
5. [<span data-ttu-id="a6e03-172">Activer Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="a6e03-172">Enable Enterprise State Roaming</span></span>](enterprise-state-roaming.md)
6. [<span data-ttu-id="a6e03-173">Configurer les appareils</span><span class="sxs-lookup"><span data-stu-id="a6e03-173">Set up devices</span></span>](set-up-devices.md)
7. [<span data-ttu-id="a6e03-174">Préparer vos utilisateurs à l’utilisation les appareils</span><span class="sxs-lookup"><span data-stu-id="a6e03-174">Get your users ready to use devices</span></span>](get-started-devices.md)
8. <span data-ttu-id="a6e03-175">Déployer des applications (cette rubrique)</span><span class="sxs-lookup"><span data-stu-id="a6e03-175">Deploy apps (this topic)</span></span>


<!--# Preparing apps for Microsoft Managed Desktop

This topic is the target for 2 "Learn more" links in the Admin Portal (aka.ms/app-overview;app-package); also target for link from Online resources (aka.ms/app-overviewmmd-app-prep) do not delete.

-->
