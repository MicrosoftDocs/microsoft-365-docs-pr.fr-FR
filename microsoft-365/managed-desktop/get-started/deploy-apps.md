---
title: Déployer les applications sur les appareils
description: Informations pour l’ajout et le déploiement d’applications sur des appareils de bureau géré Microsoft.
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation, applications, applications métier, applications métier
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: 8bfc53d46bdcb91c16e9f4a1ddbc8ab3f6dfb47e
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50922025"
---
# <a name="deploy-apps-to-devices"></a><span data-ttu-id="96392-104">Déployer les applications sur les appareils</span><span class="sxs-lookup"><span data-stu-id="96392-104">Deploy apps to devices</span></span>
<span data-ttu-id="96392-105">Une partie de l’intégration au Bureau géré Microsoft inclut l’ajout et le déploiement d’applications sur les appareils de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="96392-105">Part of onboarding to Microsoft Managed Desktop includes adding and deploying apps to your user's devices.</span></span> <span data-ttu-id="96392-106">Une fois que vous utilisez le portail Bureau géré Microsoft, vous pouvez ajouter et déployer vos applications.</span><span class="sxs-lookup"><span data-stu-id="96392-106">Once you're using the Microsoft Managed Desktop portal, you can add and deploy your apps.</span></span> 

<span data-ttu-id="96392-107">Le processus global ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="96392-107">The overall process looks like this:</span></span>
1. <span data-ttu-id="96392-108">[Ajoutez](#1) des applications au portail Bureau géré Microsoft : il peut s’y trouver des applications métier existantes ou des applications du Microsoft Store pour Entreprises que vous avez synchronisées avec Intune.</span><span class="sxs-lookup"><span data-stu-id="96392-108">[Add apps to Microsoft Managed Desktop portal](#1) - This can be existing line-of-business (LOB) apps, or apps from Microsoft Store for Business that you've synced with Intune.</span></span> 
2. <span data-ttu-id="96392-109">[Créez des groupes Azure Active Directory (AD)](#2) pour l’affectation d’applications : vous utiliserez ces groupes pour gérer l’attribution d’application.</span><span class="sxs-lookup"><span data-stu-id="96392-109">[Create Azure Active Directory (AD) groups for app assignment](#2) - You'll use these groups to manage app assignment.</span></span>
3. [<span data-ttu-id="96392-110">Affecter des applications à vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="96392-110">Assign apps to your users</span></span>](#3)

<span id="1" />

## <a name="step-1-add-apps-to-microsoft-managed-desktop-portal"></a><span data-ttu-id="96392-111">Étape 1 : Ajouter des applications au portail Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="96392-111">Step 1: Add apps to Microsoft Managed Desktop portal</span></span>
<span data-ttu-id="96392-112">Vous pouvez ajouter des applications [Win32,](#lob-apps)basées sur Windows MSI ou [Microsoft Store](#msfb-apps) pour Entreprises à Bureau géré Microsoft, puis les déployer sur des appareils de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="96392-112">You can add [Win32, or Windows MSI-based apps](#lob-apps), or [Microsoft Store for Business apps](#msfb-apps) to Microsoft Managed Desktop, and then deploy them to Microsoft Managed Desktop devices.</span></span>

<span id="lob-apps">

###  <a name="win32-or-windows-msi-based-apps-to-microsoft-managed-desktop"></a><span data-ttu-id="96392-113">Applications Win32 ou Windows MSI pour bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="96392-113">Win32 or Windows MSI-based apps to Microsoft Managed Desktop</span></span>

<span data-ttu-id="96392-114">Vous pouvez ajouter vos applications métier au portail Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="96392-114">You can add your line-of-business (LOB) apps to Microsoft Managed Desktop portal.</span></span> <span data-ttu-id="96392-115">Pour plus d’informations sur les conditions requises pour les applications installées sur les appareils de bureau géré Microsoft, consultez les conditions requises pour les applications de bureau [géré Microsoft.](../service-description/mmd-app-requirements.md)</span><span class="sxs-lookup"><span data-stu-id="96392-115">For information on requirements for apps installed on Microsoft Managed Desktop devices, see [Microsoft Managed Desktop app requirements](../service-description/mmd-app-requirements.md).</span></span>

<span data-ttu-id="96392-116">Dans cette procédure, vous allez sélectionner le type d’application que vous souhaitez ajouter, puis configurer et charger la source de l’application.</span><span class="sxs-lookup"><span data-stu-id="96392-116">In this procedure, you'll select which kind of app you want to add, and then configure and upload the app source.</span></span> 

<span data-ttu-id="96392-117">**Pour ajouter votre application LOB ou Windows au portail Bureau géré Microsoft**</span><span class="sxs-lookup"><span data-stu-id="96392-117">**To add your LOB app or Windows app to Microsoft Managed Desktop portal**</span></span>

<span data-ttu-id="96392-118">Vous pouvez vous connectez au portail Bureau géré Microsoft ou vous connectez à Intune, puis recherchez Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="96392-118">You can sign in to Microsoft Managed Desktop portal, or sign in to Intune and then search for Microsoft Managed Desktop.</span></span> <span data-ttu-id="96392-119">Nous allons afficher la signature au portail Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="96392-119">We'll show signing in to Microsoft Managed Desktop portal.</span></span> 

1.    <span data-ttu-id="96392-120">Connectez-vous au [portail d’administration du bureau géré Microsoft.](https://aka.ms/mmdportal)</span><span class="sxs-lookup"><span data-stu-id="96392-120">Sign in to [Microsoft Managed Desktop Admin portal](https://aka.ms/mmdportal).</span></span> 
2.    <span data-ttu-id="96392-121">Sous **Inventaire,** sélectionnez **Applications.**</span><span class="sxs-lookup"><span data-stu-id="96392-121">Under **Inventory**, select **Apps**.</span></span>
3.    <span data-ttu-id="96392-122">Dans la charge de travail applications, sélectionnez **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="96392-122">In the Apps workload, select **Add**.</span></span>
4.    <span data-ttu-id="96392-123">Dans **Ajouter une application,** sélectionnez **application** métier ou application **Windows (Win32).**</span><span class="sxs-lookup"><span data-stu-id="96392-123">In **Add app**, select **Line-of-business app** or **Windows app (Win32)**.</span></span>
    - <span data-ttu-id="96392-124">Si vous avez sélectionné une application **métier,** voir Ajouter une application métier Windows à [Microsoft Intune](/intune/lob-apps-windows) pour obtenir des instructions sur l’ajout et la configuration d’applications métier.</span><span class="sxs-lookup"><span data-stu-id="96392-124">If you selected **Line-of-business app**, see [Add a Windows line-of-business app to Microsoft Intune](/intune/lob-apps-windows) for instruction on adding and configuring line-of-business apps.</span></span>
    - <span data-ttu-id="96392-125">Si vous avez sélectionné **l’application Windows (Win32),** voir Gestion des applications [Win32](/intune/apps-win32-app-management) pour obtenir des instructions sur l’ajout et la configuration d’applications Windows.</span><span class="sxs-lookup"><span data-stu-id="96392-125">If you selected **Windows app (Win32)**, see [Win32 app management](/intune/apps-win32-app-management) for instruction on adding and configuring Windows apps.</span></span>

<span id="msfb-apps">

### <a name="microsoft-store-for-business-apps"></a><span data-ttu-id="96392-126">Applications du Microsoft Store pour Entreprises</span><span class="sxs-lookup"><span data-stu-id="96392-126">Microsoft Store for Business apps</span></span>
<span data-ttu-id="96392-127">Si vous ne vous êtes pas inscrit au Microsoft Store pour Entreprises, vous pouvez vous inscrire lorsque vous achetez des applications.</span><span class="sxs-lookup"><span data-stu-id="96392-127">If you haven't signed up with Microsoft Store for Business, you can sign up when you shop for apps.</span></span> <span data-ttu-id="96392-128">Une fois que vous avez vos applications, vous pouvez les synchroniser avec Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="96392-128">After you have your apps, you can sync them with Microsoft Managed Desktop.</span></span> 

<span data-ttu-id="96392-129">**Pour acheter des applications à partir du Microsoft Store pour Entreprises**</span><span class="sxs-lookup"><span data-stu-id="96392-129">**To buy apps from the Microsoft Store for Business**</span></span>

1. <span data-ttu-id="96392-130">Connectez-vous [au Microsoft Store pour Entreprises](https://businessstore.microsoft.com) à l’aide de votre compte d’administrateur du Microsoft Store pour Entreprises.</span><span class="sxs-lookup"><span data-stu-id="96392-130">Sign in to [Microsoft Store for Business](https://businessstore.microsoft.com) with your Microsoft Store for Business Admin account.</span></span>
2. <span data-ttu-id="96392-131">Sélectionnez **Acheter pour mon groupe.**</span><span class="sxs-lookup"><span data-stu-id="96392-131">Select **Shop for my group**.</span></span>
3. <span data-ttu-id="96392-132">Utilisez la recherche pour rechercher l’application de votre choix, puis sélectionnez l’application.</span><span class="sxs-lookup"><span data-stu-id="96392-132">Use Search to find that the app that you want, and select the app.</span></span>
4. <span data-ttu-id="96392-133">Dans les détails du produit, **sélectionnez Obtenir l’application.**</span><span class="sxs-lookup"><span data-stu-id="96392-133">On the product details, select **Get the App**.</span></span> <span data-ttu-id="96392-134">Le Microsoft Store ajoute l’application **à vos produits** pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="96392-134">Microsoft Store adds the app to **Your products** for your organization.</span></span>

<span data-ttu-id="96392-135">**Pour forcer une synchronisation entre Intune et Microsoft Store pour Entreprises**</span><span class="sxs-lookup"><span data-stu-id="96392-135">**To force a sync between Intune and Microsoft Store for Business**</span></span>
1. <span data-ttu-id="96392-136">Connectez-vous au [Centre d’administration Microsoft Endpoint Manager.](https://go.microsoft.com/fwlink/?linkid=2109431)</span><span class="sxs-lookup"><span data-stu-id="96392-136">Sign in to the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431).</span></span>
2. <span data-ttu-id="96392-137">Sélectionnez **les**  >  **connecteurs d’administration des** clients et les jetons  >  **du Microsoft Store pour Entreprises.**</span><span class="sxs-lookup"><span data-stu-id="96392-137">Select **Tenant administration** > **Connectors and tokens** > **Microsoft Store for Business**.</span></span>
3. <span data-ttu-id="96392-138">Sélectionnez **Synchroniser** pour obtenir les applications que vous avez achetées à partir du Microsoft Store dans Intune.</span><span class="sxs-lookup"><span data-stu-id="96392-138">Select **Sync** to get the apps you've purchased from the Microsoft Store into Intune.</span></span>

<span data-ttu-id="96392-139">**Pour vérifier qu’une synchronisation entre Intune et Microsoft Store pour Entreprises est active**</span><span class="sxs-lookup"><span data-stu-id="96392-139">**To verify that a sync between Intune and Microsoft Store for Business is active**</span></span>
1. <span data-ttu-id="96392-140">Connectez-vous [au Microsoft Store pour Entreprises](https://businessstore.microsoft.com) à l’aide de votre compte d’administrateur du Microsoft Store pour Entreprises.</span><span class="sxs-lookup"><span data-stu-id="96392-140">Sign in to [Microsoft Store for Business](https://businessstore.microsoft.com) with your Microsoft Store for Business Admin account.</span></span>
2. <span data-ttu-id="96392-141">Sélectionnez **Gérer**.</span><span class="sxs-lookup"><span data-stu-id="96392-141">Select **Manage**.</span></span>
3. <span data-ttu-id="96392-142">Sélectionnez **Paramètres,** puis **Distribuer.**</span><span class="sxs-lookup"><span data-stu-id="96392-142">Select **Settings** and then select **Distribute**.</span></span>
4. <span data-ttu-id="96392-143">Sous **Outils de** gestion, vérifiez qu’Intune est répertorié et que l’état est **Actif.**</span><span class="sxs-lookup"><span data-stu-id="96392-143">Under **Management tools**, verify that Intune is listed and that the status is **Active**.</span></span>  

<span id="2" />

## <a name="step-2-create-azure-ad-groups"></a><span data-ttu-id="96392-144">Étape 2 : Créer des groupes Azure AD</span><span class="sxs-lookup"><span data-stu-id="96392-144">Step 2: Create Azure AD groups</span></span>

<span data-ttu-id="96392-145">Créez trois groupes Azure AD pour chaque application.</span><span class="sxs-lookup"><span data-stu-id="96392-145">Create three Azure AD groups for each app.</span></span> <span data-ttu-id="96392-146">Ce tableau présente les groupes dont vous aurez besoin (disponible, obligatoire et désinstallé).</span><span class="sxs-lookup"><span data-stu-id="96392-146">This table outlines the groups you'll need (Available, Required, and Uninstall).</span></span> 

<span data-ttu-id="96392-147">Type d’affectation d’application</span><span class="sxs-lookup"><span data-stu-id="96392-147">App assignment type</span></span> |    <span data-ttu-id="96392-148">Utilisation de groupe</span><span class="sxs-lookup"><span data-stu-id="96392-148">Group use</span></span>    | <span data-ttu-id="96392-149">Exemple de nom Azure AD</span><span class="sxs-lookup"><span data-stu-id="96392-149">Example Azure AD name</span></span>
--- | --- | ---
<span data-ttu-id="96392-150">Available</span><span class="sxs-lookup"><span data-stu-id="96392-150">Available</span></span> |  <span data-ttu-id="96392-151">L’application sera disponible à partir de l’application ou du site web Portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="96392-151">The app will be available from Company Portal app or website.</span></span> | <span data-ttu-id="96392-152">MMD – *nom de l’application* – Disponible</span><span class="sxs-lookup"><span data-stu-id="96392-152">MMD – *app name* – Available</span></span>
<span data-ttu-id="96392-153">Requis</span><span class="sxs-lookup"><span data-stu-id="96392-153">Required</span></span> |  <span data-ttu-id="96392-154">L’application est installée sur les appareils des groupes sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="96392-154">The app is installed on devices in the selected groups.</span></span> | <span data-ttu-id="96392-155">MMD – *nom de l’application* – Obligatoire</span><span class="sxs-lookup"><span data-stu-id="96392-155">MMD – *app name* – Required</span></span>
<span data-ttu-id="96392-156">Uninstall</span><span class="sxs-lookup"><span data-stu-id="96392-156">Uninstall</span></span> |  <span data-ttu-id="96392-157">L’application est désinstallée des appareils des groupes sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="96392-157">The app is uninstalled from devices in the selected groups.</span></span> | <span data-ttu-id="96392-158">MMD – *nom de l’application* – Désinstaller</span><span class="sxs-lookup"><span data-stu-id="96392-158">MMD – *app name* – Uninstall</span></span>

<span data-ttu-id="96392-159">Ajoutez vos utilisateurs à ces groupes pour rendre l’application disponible, installer l’application ou supprimer l’application de son appareil Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="96392-159">Add your users to these groups to either make the app available, install the app, or remove the app from their Microsoft Managed Desktop device.</span></span> 

<span id="3" />

## <a name="step-3-assign-apps-to-your-users"></a><span data-ttu-id="96392-160">Étape 3 : Attribuer des applications à vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="96392-160">Step 3: Assign apps to your users</span></span>

<span data-ttu-id="96392-161">**Pour affecter l’application à vos utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="96392-161">**To assign the app to your users**</span></span>

1. <span data-ttu-id="96392-162">Connectez-vous au [portail d’administration du bureau géré Microsoft.](https://aka.ms/mmdportal)</span><span class="sxs-lookup"><span data-stu-id="96392-162">Sign in to [Microsoft Managed Desktop Admin portal](https://aka.ms/mmdportal).</span></span>
2. <span data-ttu-id="96392-163">Dans le volet Bureau géré, sélectionnez **Applications.**</span><span class="sxs-lookup"><span data-stu-id="96392-163">In Managed Desktop pane, select **Apps**.</span></span>
3. <span data-ttu-id="96392-164">Dans la charge de travail applications, sélectionnez l’application à qui vous souhaitez affecter des utilisateurs et **sélectionnez Affecter des groupes d’utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="96392-164">In the Apps workload, select the app you want to assign users to and select **Assign users groups**.</span></span>
4. <span data-ttu-id="96392-165">Pour l’application spécifique, sélectionnez un type d’affectation (Disponible, Obligatoire, Désinstaller) et affectez le groupe approprié.</span><span class="sxs-lookup"><span data-stu-id="96392-165">For the specific app, select an assignment type (Available, Required, Uninstall) and assign the appropriate group.</span></span>
5. <span data-ttu-id="96392-166">Dans le volet Attribuer des applications, sélectionnez **OK.**</span><span class="sxs-lookup"><span data-stu-id="96392-166">In the Assign Apps pane, select **OK**.</span></span>


## <a name="steps-to-get-started-with-microsoft-managed-desktop"></a><span data-ttu-id="96392-167">Étapes de mise en place du Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="96392-167">Steps to get started with Microsoft Managed Desktop</span></span>

1. [<span data-ttu-id="96392-168">Ajouter et vérifier des contacts d’administrateur dans le portail d’administration</span><span class="sxs-lookup"><span data-stu-id="96392-168">Add and verify admin contacts in the Admin portal</span></span>](add-admin-contacts.md)
2. [<span data-ttu-id="96392-169">Ajuster l’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="96392-169">Adjust conditional access</span></span>](conditional-access.md)
3. [<span data-ttu-id="96392-170">Affecter des licences</span><span class="sxs-lookup"><span data-stu-id="96392-170">Assign licenses</span></span>](assign-licenses.md)
4. [<span data-ttu-id="96392-171">Déployer le portail d’entreprise Intune</span><span class="sxs-lookup"><span data-stu-id="96392-171">Deploy Intune Company Portal</span></span>](company-portal.md)
5. [<span data-ttu-id="96392-172">Activer Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="96392-172">Enable Enterprise State Roaming</span></span>](enterprise-state-roaming.md)
6. [<span data-ttu-id="96392-173">Configurer les appareils</span><span class="sxs-lookup"><span data-stu-id="96392-173">Set up devices</span></span>](set-up-devices.md)
7. [<span data-ttu-id="96392-174">Préparer vos utilisateurs à l’utilisation les appareils</span><span class="sxs-lookup"><span data-stu-id="96392-174">Get your users ready to use devices</span></span>](get-started-devices.md)
8. <span data-ttu-id="96392-175">Déployer des applications (cette rubrique)</span><span class="sxs-lookup"><span data-stu-id="96392-175">Deploy apps (this topic)</span></span>


<!--# Preparing apps for Microsoft Managed Desktop

This topic is the target for 2 "Learn more" links in the Admin Portal (aka.ms/app-overview;app-package); also target for link from Online resources (aka.ms/app-overviewmmd-app-prep) do not delete.

-->