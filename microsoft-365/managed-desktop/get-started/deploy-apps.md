---
title: Déployer des applications pour les appareils de bureau gérés Microsoft
description: Informations pour ajouter et déployer des applications sur des appareils de bureau gérés Microsoft.
keywords: Microsoft Managed Desktop, Microsoft 365, service, documentation, applications, applications métiers, applications métier
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 5eac2e8c3023015bd034c51ad7e16a669a484772
ms.sourcegitcommit: 427c6459614d58f6ef7c74354ae1816423e22323
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/28/2019
ms.locfileid: "35390421"
---
# <a name="deploy-apps-to-microsoft-managed-desktop-devices"></a><span data-ttu-id="62c4b-104">Déployer des applications sur des appareils de bureau gérés Microsoft</span><span class="sxs-lookup"><span data-stu-id="62c4b-104">Deploy apps to Microsoft Managed Desktop devices</span></span>
<span data-ttu-id="62c4b-105">L’intégration à Microsoft Managed Desktop inclut l’ajout et le déploiement d’applications sur les appareils de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="62c4b-105">Part of onboarding to Microsoft Managed Desktop includes adding and deploying apps to your user’s devices.</span></span> <span data-ttu-id="62c4b-106">Une fois que vous utilisez le portail de bureau géré Microsoft, vous pouvez ajouter et déployer vos applications.</span><span class="sxs-lookup"><span data-stu-id="62c4b-106">Once you're using the Microsoft Managed Desktop portal, you can add and deploy your apps.</span></span> 

<span data-ttu-id="62c4b-107">Le processus global se présente comme suit:</span><span class="sxs-lookup"><span data-stu-id="62c4b-107">The overall process looks like this:</span></span>
1. <span data-ttu-id="62c4b-108">[Ajouter des applications au portail de bureau géré Microsoft](#1) -il peut s’agir d’applications métier existantes ou d’applications de Microsoft Store pour les entreprises que vous avez synchronisées avec Intune.</span><span class="sxs-lookup"><span data-stu-id="62c4b-108">[Add apps to Microsoft Managed Desktop portal](#1) - This can be existing line-of-business (LOB) apps, or apps from Microsoft Store for Business that you've synced with Intune.</span></span> 
2. <span data-ttu-id="62c4b-109">[Créer des groupes Azure Active Directory (AD) pour l’affectation d’application](#2) : vous utiliserez ces groupes pour gérer l’affectation d’application.</span><span class="sxs-lookup"><span data-stu-id="62c4b-109">[Create Azure Active Directory (AD) groups for app assignment](#2) - You'll use these groups to manage app assignment.</span></span>
3. [<span data-ttu-id="62c4b-110">Affecter des applications à vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="62c4b-110">Assign apps to your users</span></span>](#3)

<span id="1" />

## <a name="step-1-add-apps-to-microsoft-managed-desktop-portal"></a><span data-ttu-id="62c4b-111">Étape 1: ajouter des applications au portail de bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="62c4b-111">Step 1: Add apps to Microsoft Managed Desktop portal</span></span>
<span data-ttu-id="62c4b-112">Vous pouvez ajouter des [applications Win32 ou Windows MSI](#lob-apps), ou [des applications Microsoft Store pour les entreprises](#msfb-apps) à Microsoft Managed Desktop, puis les déployer sur des appareils de bureau gérés Microsoft.</span><span class="sxs-lookup"><span data-stu-id="62c4b-112">You can add [Win32, or Windows MSI-based apps](#lob-apps), or [Microsoft Store for Business apps](#msfb-apps) to Microsoft Managed Desktop, and then deploy them to Microsoft Managed Desktop devices.</span></span>

<span id="lob-apps">

###  <a name="win32-or-windows-msi-based-apps-to-microsoft-managed-desktop"></a><span data-ttu-id="62c4b-113">Applications Win32 ou Windows MSI à Microsoft Managed Desktop</span><span class="sxs-lookup"><span data-stu-id="62c4b-113">Win32 or Windows MSI-based apps to Microsoft Managed Desktop</span></span>

<span data-ttu-id="62c4b-114">Vous pouvez ajouter vos applications métier à Microsoft Managed Desktop Portal.</span><span class="sxs-lookup"><span data-stu-id="62c4b-114">You can add your line-of-business (LOB) apps to Microsoft Managed Desktop portal.</span></span> <span data-ttu-id="62c4b-115">Pour plus d’informations sur les conditions requises pour les applications installées sur les appareils de bureau géré Microsoft, consultez la rubrique [conditions requises pour les applications de bureau géré Microsoft](https://docs.microsoft.com/microsoft-365/managed-desktop/service-description/mmd-app-requirements).</span><span class="sxs-lookup"><span data-stu-id="62c4b-115">For information on requirements for apps installed on Microsoft Managed Desktop devices, see [Microsoft Managed Desktop app requirements](https://docs.microsoft.com/microsoft-365/managed-desktop/service-description/mmd-app-requirements).</span></span>

<span data-ttu-id="62c4b-116">Dans cette procédure, vous allez sélectionner le type d’application que vous souhaitez ajouter, puis configurer et télécharger la source de l’application.</span><span class="sxs-lookup"><span data-stu-id="62c4b-116">In this procedure, you'll select which kind of app you want to add, and then configure and upload the app source.</span></span> 

<span data-ttu-id="62c4b-117">**Pour ajouter votre application LOB ou votre application Windows au portail de bureau géré Microsoft**</span><span class="sxs-lookup"><span data-stu-id="62c4b-117">**To add your LOB app or Windows app to Microsoft Managed Desktop portal**</span></span>

<span data-ttu-id="62c4b-118">Vous pouvez vous connecter à Microsoft Managed Desktop Portal ou vous connecter à Intune, puis rechercher le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="62c4b-118">You can sign in to Microsoft Managed Desktop portal, or sign in to Intune and then search for Microsoft Managed Desktop.</span></span> <span data-ttu-id="62c4b-119">Nous allons afficher la connexion à Microsoft Managed Desktop Portal.</span><span class="sxs-lookup"><span data-stu-id="62c4b-119">We'll show signing in to Microsoft Managed Desktop portal.</span></span> 

1.  <span data-ttu-id="62c4b-120">Connectez-vous au [portail d’administration de bureau géré Microsoft](http://aka.ms/mmdportal).</span><span class="sxs-lookup"><span data-stu-id="62c4b-120">Sign in to [Microsoft Managed Desktop Admin portal](http://aka.ms/mmdportal).</span></span> 
2.  <span data-ttu-id="62c4b-121">Sous **inventaire**, sélectionnez **applications**.</span><span class="sxs-lookup"><span data-stu-id="62c4b-121">Under **Inventory**, select **Apps**.</span></span>
3.  <span data-ttu-id="62c4b-122">Dans la charge de travail applications, sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="62c4b-122">In the Apps workload, select **Add**.</span></span>
4.  <span data-ttu-id="62c4b-123">Dans **Ajouter une application**, sélectionnez **application métier** ou **application Windows (Win32)-Aperçu**.</span><span class="sxs-lookup"><span data-stu-id="62c4b-123">In **Add app**, select **Line-of-business app** or **Windows app (Win32) - preview**.</span></span>
    - <span data-ttu-id="62c4b-124">Si vous avez sélectionné **application métier**, voir [Add a Windows Line of Business app to Microsoft Intune](https://docs.microsoft.com/intune/lob-apps-windows) pour obtenir des instructions sur l’ajout et la configuration d’applications métiers.</span><span class="sxs-lookup"><span data-stu-id="62c4b-124">If you selected **Line-of-business app**, see [Add a Windows line-of-business app to Microsoft Intune](https://docs.microsoft.com/intune/lob-apps-windows) for instruction on adding and configuring line-of-business apps.</span></span>
    - <span data-ttu-id="62c4b-125">Si vous avez sélectionné **Windows App (Win32)-Preview**, voir [Win32 App Management](https://docs.microsoft.com/intune/apps-win32-app-management) pour obtenir des instructions sur l’ajout et la configuration d’applications Windows.</span><span class="sxs-lookup"><span data-stu-id="62c4b-125">If you selected **Windows app (Win32) - preview**, see [Win32 app management](https://docs.microsoft.com/intune/apps-win32-app-management) for instruction on adding and configuring Windows apps.</span></span>

<span id="msfb-apps">

### <a name="microsoft-store-for-business-apps"></a><span data-ttu-id="62c4b-126">Applications Microsoft Store pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="62c4b-126">Microsoft Store for Business apps</span></span>
<span data-ttu-id="62c4b-127">Si vous ne vous êtes pas inscrit auprès de Microsoft Store pour les entreprises, vous pouvez vous inscrire lorsque vous achetez des applications.</span><span class="sxs-lookup"><span data-stu-id="62c4b-127">If you haven't signed up with Microsoft Store for Business, you can sign up when you shop for apps.</span></span> <span data-ttu-id="62c4b-128">Une fois que vous avez vos applications, vous pouvez les synchroniser avec le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="62c4b-128">After you have your apps, you can sync them with Microsoft Managed Desktop.</span></span> 

<span data-ttu-id="62c4b-129">**Pour acheter des applications à partir de Microsoft Store pour les entreprises**</span><span class="sxs-lookup"><span data-stu-id="62c4b-129">**To buy apps from the Microsoft Store for Business**</span></span>

1. <span data-ttu-id="62c4b-130">Connectez-vous à [Microsoft Store pour entreprises](https://businessstore.microsoft.com) avec votre compte d’administrateur Microsoft Store pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="62c4b-130">Sign in to [Microsoft Store for Business](https://businessstore.microsoft.com) with your Microsoft Store for Business Admin account.</span></span>
2. <span data-ttu-id="62c4b-131">Sélectionnez **acheter pour mon groupe**.</span><span class="sxs-lookup"><span data-stu-id="62c4b-131">Select **Shop for my group**.</span></span>
3. <span data-ttu-id="62c4b-132">Utilisez la recherche pour trouver l’application de votre choix, puis sélectionnez l’application.</span><span class="sxs-lookup"><span data-stu-id="62c4b-132">Use Search to find that the app that you want, and select the app.</span></span>
4. <span data-ttu-id="62c4b-133">Dans les détails du produit, sélectionnez **obtenir l’application**.</span><span class="sxs-lookup"><span data-stu-id="62c4b-133">On the product details, select **Get the App**.</span></span> <span data-ttu-id="62c4b-134">Le Microsoft Store ajoute l’application aux **produits & services** de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="62c4b-134">Microsoft Store adds the app to **Products & services** for your organization.</span></span>

<span data-ttu-id="62c4b-135">**Pour forcer une synchronisation entre Intune et Microsoft Store pour les entreprises**</span><span class="sxs-lookup"><span data-stu-id="62c4b-135">**To force a sync between Intune and Microsoft Store for Business**</span></span>
1. <span data-ttu-id="62c4b-136">Se connecter au [portail Azure](https://portal.azure.com/) en tant qu’administrateur Intune ou administrateur global pour votre client</span><span class="sxs-lookup"><span data-stu-id="62c4b-136">Sign in to [Azure Portal](https://portal.azure.com/) as Intune Admin or Global Admin for your tenant</span></span>
2. <span data-ttu-id="62c4b-137">Sélectionnez **tous les services > Intune**.</span><span class="sxs-lookup"><span data-stu-id="62c4b-137">Select **All services > Intune**.</span></span> <span data-ttu-id="62c4b-138">Intune se trouve dans la section surveillance + Management.</span><span class="sxs-lookup"><span data-stu-id="62c4b-138">Intune is in the Monitoring + Management section.</span></span>
3. <span data-ttu-id="62c4b-139">Dans le volet Intune, sélectionnez **applications clientes**, puis sélectionnez **Microsoft Store pour les entreprises**.</span><span class="sxs-lookup"><span data-stu-id="62c4b-139">In the Intune pane, select **Client Apps**, and then select **Microsoft Store for Business**.</span></span>
4. <span data-ttu-id="62c4b-140">Sélectionnez **activer** pour synchroniser vos applications Microsoft Store pour les entreprises avec Intune.</span><span class="sxs-lookup"><span data-stu-id="62c4b-140">Select **Enable** to sync your Microsoft Store for Business apps with Intune.</span></span>
    - <span data-ttu-id="62c4b-141">Si vous ne l’avez pas encore fait, inscrivez-vous et associez votre compte Microsoft Store pour les entreprises avec Intune</span><span class="sxs-lookup"><span data-stu-id="62c4b-141">If you haven't already, sign up and associate your Microsoft Store for Business account with Intune</span></span>
    - <span data-ttu-id="62c4b-142">Sélectionnez la langue dans laquelle les applications de Microsoft Store pour les entreprises seront affichées dans votre console Intune.</span><span class="sxs-lookup"><span data-stu-id="62c4b-142">Select the language in which apps from the Microsoft Store for Business will be displayed in your Intune console</span></span>
    - <span data-ttu-id="62c4b-143">Sélectionnez **synchroniser** pour synchroniser vos applications Microsoft Store pour les entreprises avec Intune.</span><span class="sxs-lookup"><span data-stu-id="62c4b-143">Select **Sync** to sync your Microsoft Store for Business apps with Intune.</span></span>
    - <span data-ttu-id="62c4b-144">Vérifiez que la synchronisation entre Microsoft Store pour les entreprises et Intune est active (étape suivante).</span><span class="sxs-lookup"><span data-stu-id="62c4b-144">Verify that the sync between Microsoft Store for Business and Intune is active (next step).</span></span> 

<span data-ttu-id="62c4b-145">**Pour vérifier qu’une synchronisation entre Intune et Microsoft Store pour les entreprises est active**</span><span class="sxs-lookup"><span data-stu-id="62c4b-145">**To verify that a sync between Intune and Microsoft Store for Business is active**</span></span>
1. <span data-ttu-id="62c4b-146">Connectez-vous à [Microsoft Store pour entreprises](https://businessstore.microsoft.com) avec votre compte d’administrateur Microsoft Store pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="62c4b-146">Sign in to [Microsoft Store for Business](https://businessstore.microsoft.com) with your Microsoft Store for Business Admin account.</span></span>
2. <span data-ttu-id="62c4b-147">Sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="62c4b-147">Select **Manage**.</span></span>
3. <span data-ttu-id="62c4b-148">Sélectionnez **paramètres** , puis **distribuer**.</span><span class="sxs-lookup"><span data-stu-id="62c4b-148">Select **Settings** and then select **Distribute**.</span></span>
4. <span data-ttu-id="62c4b-149">Sous **outils de gestion**, vérifiez que Intune est affiché et que l’État est **actif**.</span><span class="sxs-lookup"><span data-stu-id="62c4b-149">Under **Management tools**, verify that Intune is listed and that the status is **Active**.</span></span>  

<span id="2" />

## <a name="step-2-create-azure-ad-groups"></a><span data-ttu-id="62c4b-150">Étape 2: créer des groupes Azure AD</span><span class="sxs-lookup"><span data-stu-id="62c4b-150">Step 2: Create Azure AD groups</span></span>

<span data-ttu-id="62c4b-151">Créez trois groupes Azure AD pour chaque application.</span><span class="sxs-lookup"><span data-stu-id="62c4b-151">Create three Azure AD groups for each app.</span></span> <span data-ttu-id="62c4b-152">Ce tableau décrit les groupes dont vous aurez besoin (disponible, requis et désinstallation).</span><span class="sxs-lookup"><span data-stu-id="62c4b-152">This table outlines the groups you'll need (Available, Required, and Uninstall).</span></span> 

<span data-ttu-id="62c4b-153">Type d’affectation d’application</span><span class="sxs-lookup"><span data-stu-id="62c4b-153">App assignment type</span></span> |   <span data-ttu-id="62c4b-154">Utilisation de groupe</span><span class="sxs-lookup"><span data-stu-id="62c4b-154">Group use</span></span>   | <span data-ttu-id="62c4b-155">Exemple de nom Azure AD</span><span class="sxs-lookup"><span data-stu-id="62c4b-155">Example Azure AD name</span></span>
--- | --- | ---
<span data-ttu-id="62c4b-156">Available</span><span class="sxs-lookup"><span data-stu-id="62c4b-156">Available</span></span> |  <span data-ttu-id="62c4b-157">L’application sera disponible à partir de l’application ou du site Web du portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="62c4b-157">The app will be available from Company Portal app or website.</span></span> | <span data-ttu-id="62c4b-158">MMD – *nom* de l’application – disponible</span><span class="sxs-lookup"><span data-stu-id="62c4b-158">MMD – *app name* – Available</span></span>
<span data-ttu-id="62c4b-159">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="62c4b-159">Required</span></span> |  <span data-ttu-id="62c4b-160">L’application est installée sur les appareils dans les groupes sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="62c4b-160">The app is installed on devices in the selected groups.</span></span> | <span data-ttu-id="62c4b-161">MMD – *nom* de l’application – obligatoire</span><span class="sxs-lookup"><span data-stu-id="62c4b-161">MMD – *app name* – Required</span></span>
<span data-ttu-id="62c4b-162">Uninstall</span><span class="sxs-lookup"><span data-stu-id="62c4b-162">Uninstall</span></span> |  <span data-ttu-id="62c4b-163">L’application est désinstallée des appareils dans les groupes sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="62c4b-163">TThe app is uninstalled from devices in the selected groups.</span></span> | <span data-ttu-id="62c4b-164">MMD – *nom* de l’application – Uninstall</span><span class="sxs-lookup"><span data-stu-id="62c4b-164">MMD – *app name* – Uninstall</span></span>

<span data-ttu-id="62c4b-165">Ajoutez vos utilisateurs à ces groupes pour que l’application soit disponible, installez l’application ou supprimez l’application de son appareil de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="62c4b-165">Add your users to these groups to either make the app availabe, install the app, or remove the app from their Microsoft Managed Desktop device.</span></span> 

<span id="3" />

## <a name="step-3-assign-apps-to-your-users"></a><span data-ttu-id="62c4b-166">Étape 3: attribuer des applications à vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="62c4b-166">Step 3: Assign apps to your users</span></span>

<span data-ttu-id="62c4b-167">**Pour affecter l’application à vos utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="62c4b-167">**To assign the app to your users**</span></span>

1. <span data-ttu-id="62c4b-168">Connectez-vous au [portail d’administration de bureau géré Microsoft](http://aka.ms/mmdportal).</span><span class="sxs-lookup"><span data-stu-id="62c4b-168">Sign in to [Microsoft Managed Desktop Admin portal](http://aka.ms/mmdportal).</span></span>
2. <span data-ttu-id="62c4b-169">Dans le volet bureau géré, sélectionnez **applications**.</span><span class="sxs-lookup"><span data-stu-id="62c4b-169">In Managed Desktop pane, select **Apps**.</span></span>
3. <span data-ttu-id="62c4b-170">Dans la charge de travail applications, sélectionnez l’application à laquelle vous souhaitez attribuer des utilisateurs et sélectionnez **affecter des groupes d’utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="62c4b-170">In the Apps workload, select the app you want to assign users to and select **Assign users groups**.</span></span>
4. <span data-ttu-id="62c4b-171">Pour l’application spécifique, sélectionnez un type d’affectation (disponible, obligatoire, désinstaller) et affectez le groupe approprié.</span><span class="sxs-lookup"><span data-stu-id="62c4b-171">For the specific app, select an assignment type (Available, Required, Uninstall) and assign the appropriate group.</span></span>
5. <span data-ttu-id="62c4b-172">Dans le volet attribuer des applications, sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="62c4b-172">In the Assign Apps pane, select **OK**.</span></span>

<!--# Preparing apps for Microsoft Managed Desktop

This topic is the target for 2 "Learn more" links in the Admin Portal (aka.ms/app-overview;app-package); also target for link from Online resources (aka.ms/app-overviewmmd-app-prep) do not delete.

Applications: supported/onboard/deployment
 
Microsoft and Microsoft Managed Desktop customers have equally critical, yet different responsibilities around applications used with Microsoft Managed Desktop.

## Microsoft responsibilities
**Office 365 apps**
Microsoft will provide full service for the deployment, update, and support of specific Office 365 apps. All users will receive the base set of Office 365 click to run, 64 bit version of applications included in the device’s image so that a user can quickly become productive. The Project and Visio applications in of the Office 365 suite are licensed separately.  Microsoft Managed Desktop will provide deployment groups allowing the IT Administrator to manage licenses and deploy these applications appropriately for their organization. Microsoft will support end users of these applications through the Microsoft Managed Desktop Support channels.

**Line-of-business apps**
Microsoft provides tooling for IT Administrators to manage and deploy their line-of-business (LOB) applications to end users as a part of the Intune product. Microsoft will support application deployment issues as detailed in [Line-of-business applications](#line-of-business-applications) 

**Deploy with Intune**
Intune will be linked to the **Microsoft Store for Business** during Microsoft Managed Desktop onboarding allowing procured apps to be deployed through Intune. Microsoft will also deploy the web-based version of the Company Portal to end users so that IT Administrators can provide a self-service experience for end users.

**App management**
Microsoft may identify restricted applications which are not suitable for the modern workplace because of their system impact. When such an application is identified Microsoft will notify the customer and that application will need to be removed from the tenant. 

For more information on restricted app behaviors and app requirements, see [Microsoft Managed Desktop app requirements](../service-description/mmd-app-requirements.md)

## Customer responsibilities
The Office 365 Suite is core to Microsoft’s productivity offerings and is included in the Microsoft 365 License for all Microsoft Managed Desktop users. While Microsoft deploys, updates, and supports Office Applications to Microsoft Managed Desktop Devices there are still some areas for which the customer is responsible.
- **Assign licenses** - Customers are responsible for assigning the appropriate licenses to end users for Office 365. 
- **Add users to security groups** - For customers with users who need Project or Visio, the IT administrator must add those users to the appropriate deployment groups. IT administrators are also responsible for managing end of life for those users. 
- **Deploy Office 365 Add Ons** - Customers are responsible for deploying any plugins to the Office 365 suite which are deemed necessary. 

Since line-of-business (LOB) apps are unique for each customer, customers are responsible for managing all applications within their organization not deployed by Microsoft. This includes:
- Deciding which apps are needed and who needs them
- Assigning apps to those users
- Create and maintain Azure Active Directory (AD) groups for managing app assignments 

The customer must upload LOB apps to Intune. They are then responsible for deploying, updating, and decommissioning those applications over their respective lifecycles, as well as managing support for these apps for their users.

## Office applications
As part of the Microsoft 365 E5 license, Office 365 Standard Suite (64 Bit) is deployed by Microsoft. 

For details, see [Microsoft Managed Desktop technologies](../intro/technologies.md) <!--- and the other applications licensed under Office 365 E5 may be deployed by the customer using Intune’s deployment tools.

## Line-of-business applications
This table summarizes responsibilities across the different phases for line-of-business (LOB) applications. 

Application work items |    Customer    | Microsoft
--- | --- | ---
**Onboarding apps** |  |
Identify applications needed for targeted user groups   | ![yes](images/checkmark.png)  |
Create and manage Azure AD groups for app deployment | ![yes](images/checkmark.png) |   
**App Packaging** |  |
Package apps to meet Intune deployment standards |  ![yes](images/checkmark.png) |  
Upload apps to Intune | ![yes](images/checkmark.png)     |
Test apps in Microsoft Managed Desktop environment |    ![yes](images/checkmark.png) |  
Test apps with end users    | ![yes](images/checkmark.png) |    
**Deployment** | |
Manage and assign users to applications  | ![yes](images/checkmark.png)  |
Intune deployment tools delivers application to remote clients| |   ![yes](images/checkmark.png)
Identify and deploy application updates through Intune | ![yes](images/checkmark.png)    |
Unistall and remove applications when they have been retired    | ![yes](images/checkmark.png) |    
**Management** | |
Procure and assign licenses |   ![yes](images/checkmark.png)     |
Provide end-user support for line-of-business apps  | ![yes](images/checkmark.png) |
Manage app settings remotely    | ![yes](images/checkmark.png) |

For information on LOB application requirements, see [Microsoft Managed Desktop application requirements](../service-description/mmd-app-requirements.md)


## Intune application deployment
Application management can be handled through the Microsoft Managed Desktop Admin portal, or through the Intune portal. Intune’s app management portal shows applications deployed for Windows, Android, and iOS. Microsoft Managed Desktop Admin portal limits the view to Windows 10 applications. Both are available through the Azure Portal. 
* [Intune app management basics](https://docs.microsoft.com/intune/app-management)
* [Add apps to Intune](https://docs.microsoft.com/intune/app-management)
   * [Add a line-of-business App](https://docs.microsoft.com/intune/lob-apps-windows)
   * [Add Win32 apps to Intune](https://docs.microsoft.com/intune/apps-win32-app-management)
   * [Add web applications](https://docs.microsoft.com/intune/web-app)
* [Deploy apps](https://docs.microsoft.com/intune/apps-deploy)
   * [Deploy apps to Windows 10](https://docs.microsoft.com/intune/apps-windows-10-app-deploy)
* Company Portal
   * [Deploy the Company Portal](https://docs.microsoft.com/intune/store-apps-company-portal-app)
   * [Configure the Company Portal app](https://docs.microsoft.com/intune/company-portal-app)-->
