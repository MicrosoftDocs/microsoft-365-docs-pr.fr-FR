---
title: Déployer des applications pour les périphériques de bureau Microsoft
description: Informations pour l’ajout et le déploiement d’applications sur les périphériques de bureau Microsoft.
keywords: Ordinateur de bureau Microsoft, Microsoft 365, service, documentation, applications, line-of-business applications, applications métier
ms.service: m365-md
author: trudyha
ms.localizationpriority: normal
ms.date: 01/17/2019
ms.openlocfilehash: 65d45be5ddb21d8f2cac876a1c8f93b2bbddf7b8
ms.sourcegitcommit: 0fc00286d7dc8cafddf9d17a98a375503b9551e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "29341603"
---
# <a name="deploy-apps-to-microsoft-managed-desktop-devices"></a><span data-ttu-id="cd070-104">Déployer des applications sur les périphériques de bureau Microsoft</span><span class="sxs-lookup"><span data-stu-id="cd070-104">Deploy apps to Microsoft Managed Desktop devices</span></span>
<span data-ttu-id="cd070-p101">Composant d’intégration à Microsoft de bureau comprend l’ajout et déployer des applications sur les périphériques de l’utilisateur. Une fois que vous utilisez le portail Microsoft de bureau, vous pouvez ajouter et déployer vos applications.</span><span class="sxs-lookup"><span data-stu-id="cd070-p101">Part of onboarding to Microsoft Managed Desktop includes adding and deploying apps to your user’s devices. Once you're using the Microsoft Managed Desktop portal, you can add and deploy your apps.</span></span> 

<span data-ttu-id="cd070-107">Le processus global ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="cd070-107">The overall process looks like this:</span></span>
1. <span data-ttu-id="cd070-108">[Ajouter les applications pour ordinateur de bureau Microsoft portal](#1) - cela peut être existant de métier (LOB) applications ou les applications de Microsoft Store for Business que vous avez synchronisé avec Intune.</span><span class="sxs-lookup"><span data-stu-id="cd070-108">[Add apps to Microsoft Managed Desktop portal](#1) - This can be existing line-of-business (LOB) apps, or apps from Microsoft Store for Business that you've synced with Intune.</span></span> 
2. <span data-ttu-id="cd070-109">[Groupes créer Azure Active Directory (AD) pour l’affectation de l’application](#2) - vous allez utiliser ces groupes pour gérer l’affectation de l’application.</span><span class="sxs-lookup"><span data-stu-id="cd070-109">[Create Azure Active Directory (AD) groups for app assignment](#2) - You'll use these groups to manage app assignment.</span></span>
3. [<span data-ttu-id="cd070-110">Attribuer des applications à vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="cd070-110">Assign apps to your users</span></span>](#3)

<span id="1" />

## <a name="step-1-add-apps-to-microsoft-managed-desktop-portal"></a><span data-ttu-id="cd070-111">Étape 1 : Ajouter des applications au portail Microsoft de bureau</span><span class="sxs-lookup"><span data-stu-id="cd070-111">Step 1: Add apps to Microsoft Managed Desktop portal</span></span>
<span data-ttu-id="cd070-112">Vous pouvez ajouter [Win32, applications basées sur Windows MSI](#lob-apps)ou [Magasin de Microsoft pour les applications métiers](#msfb-apps) à l’ordinateur de bureau Microsoft et puis déployez-les sur les périphériques de bureau Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cd070-112">You can add [Win32, or Windows MSI-based apps](#lob-apps), or [Microsoft Store for Business apps](#msfb-apps) to Microsoft Managed Desktop, and then deploy them to Microsoft Managed Desktop devices.</span></span>

<span id="lob-apps">

###  <a name="win32-or-windows-msi-based-apps-to-microsoft-managed-desktop"></a><span data-ttu-id="cd070-113">Applications basées sur MSI Win32 ou Windows à Microsoft géré du bureau</span><span class="sxs-lookup"><span data-stu-id="cd070-113">Win32 or Windows MSI-based apps to Microsoft Managed Desktop</span></span>

<span data-ttu-id="cd070-p102">Vous pouvez ajouter vos applications de métier (LOB) au portail Microsoft de bureau. Pour plus d’informations sur la configuration requise pour les applications installées sur les périphériques de bureau Microsoft, voir [Configuration requise de bureau Microsoft](https://docs.microsoft.com/microsoft-365/managed-desktop/service-description/mmd-app-requirements).</span><span class="sxs-lookup"><span data-stu-id="cd070-p102">You can add your line-of-business (LOB) apps to Microsoft Managed Desktop portal. For information on requirements for apps installed on Microsoft Managed Desktop devices, see [Microsoft Managed Desktop app requirements](https://docs.microsoft.com/microsoft-365/managed-desktop/service-description/mmd-app-requirements).</span></span>

<span data-ttu-id="cd070-116">Dans cette procédure, vous devez sélectionner le type d’application que vous souhaitez ajouter, puis configurer et télécharger la source de l’application.</span><span class="sxs-lookup"><span data-stu-id="cd070-116">In this procedure, you'll select which kind of app you want to add, and then configure and upload the app source.</span></span> 

<span data-ttu-id="cd070-117">**Pour ajouter votre application métier ou une application Windows au portail Microsoft de bureau**</span><span class="sxs-lookup"><span data-stu-id="cd070-117">**To add your LOB app or Windows app to Microsoft Managed Desktop portal**</span></span>

<span data-ttu-id="cd070-p103">Vous pouvez connectez-vous au portail de l’ordinateur de bureau Microsoft, ou vous connecter à Intune et recherchez de bureau Microsoft. Nous allons connexion au portail Microsoft de bureau.</span><span class="sxs-lookup"><span data-stu-id="cd070-p103">You can sign in to Microsoft Managed Desktop portal, or sign in to Intune and then search for Microsoft Managed Desktop. We'll show signing in to Microsoft Managed Desktop portal.</span></span> 

1.  <span data-ttu-id="cd070-120">Connectez-vous au [portail d’administration de bureau géré Microsoft](http://aka.ms/mmdportal).</span><span class="sxs-lookup"><span data-stu-id="cd070-120">Sign in to [Microsoft Managed Desktop Admin portal](http://aka.ms/mmdportal).</span></span> 
2.  <span data-ttu-id="cd070-121">Dans le menu **inventaire**, sélectionnez **applications**.</span><span class="sxs-lookup"><span data-stu-id="cd070-121">Under **Inventory**, select **Apps**.</span></span>
3.  <span data-ttu-id="cd070-122">Dans la charge de travail des applications, sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="cd070-122">In the Apps workload, select **Add**.</span></span>
4.  <span data-ttu-id="cd070-123">Dans **Ajouter application**, sélectionnez **application métier** d’ou **Afficher un aperçu de l’application Windows (Win32)**.</span><span class="sxs-lookup"><span data-stu-id="cd070-123">In **Add app**, select **Line-of-business app** or **Windows app (Win32) - preview**.</span></span>
    - <span data-ttu-id="cd070-124">Si vous avez sélectionné **métier d’application**, voir [Ajouter une application métier de Windows Intune Microsoft](https://docs.microsoft.com/intune/lob-apps-windows) pour obtenir des instructions sur l’ajout et la configuration des applications line-of-business.</span><span class="sxs-lookup"><span data-stu-id="cd070-124">If you selected **Line-of-business app**, see [Add a Windows line-of-business app to Microsoft Intune](https://docs.microsoft.com/intune/lob-apps-windows) for instruction on adding and configuring line-of-business apps.</span></span>
    - <span data-ttu-id="cd070-125">Si vous avez sélectionné **Afficher un aperçu de l’application Windows (Win32) -**, voir [Gestion des applications Win32](https://docs.microsoft.com/intune/apps-win32-app-management) pour obtenir des instructions sur l’ajout et la configuration des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="cd070-125">If you selected **Windows app (Win32) - preview**, see [Win32 app management](https://docs.microsoft.com/intune/apps-win32-app-management) for instruction on adding and configuring Windows apps.</span></span>

<span id="msfb-apps">

### <a name="microsoft-store-for-business-apps"></a><span data-ttu-id="cd070-126">Magasin de Microsoft pour les applications métiers</span><span class="sxs-lookup"><span data-stu-id="cd070-126">Microsoft Store for Business apps</span></span>
<span data-ttu-id="cd070-p104">Si vous n’avez pas encore inscrit auprès de Microsoft Store pour les entreprises, vous pouvez vous inscrire lorsque vous achetez des applications. Une fois que vous avez vos applications, vous pouvez les synchroniser avec l’ordinateur de bureau Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cd070-p104">If you haven't signed up with Microsoft Store for Business, you can sign up when you shop for apps. After you have your apps, you can sync them with Microsoft Managed Desktop.</span></span> 

<span data-ttu-id="cd070-129">**Pour acheter des applications de le Store Microsoft pour les entreprises**</span><span class="sxs-lookup"><span data-stu-id="cd070-129">**To buy apps from the Microsoft Store for Business**</span></span>

1. <span data-ttu-id="cd070-130">Connectez-vous à [Microsoft Store for Business](https://businessstore.microsoft.com) avec votre Store Microsoft pour le compte d’administrateur d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="cd070-130">Sign in to [Microsoft Store for Business](https://businessstore.microsoft.com) with your Microsoft Store for Business Admin account.</span></span>
2. <span data-ttu-id="cd070-131">Sélectionnez **Mon groupe d’environnement de stockage centralisé**.</span><span class="sxs-lookup"><span data-stu-id="cd070-131">Select **Shop for my group**.</span></span>
3. <span data-ttu-id="cd070-132">Utiliser la recherche pour trouver que l’application que vous souhaitez, puis sélectionnez l’application.</span><span class="sxs-lookup"><span data-stu-id="cd070-132">Use Search to find that the app that you want, and select the app.</span></span>
4. <span data-ttu-id="cd070-p105">Dans les détails du produit, sélectionnez **obtenir l’application**. Microsoft Store ajoute l’application pour les **produits et services &** pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cd070-p105">On the product details, select **Get the App**. Microsoft Store adds the app to **Products & services** for your organization.</span></span>

<span data-ttu-id="cd070-135">**Pour forcer une synchronisation entre Intune et Microsoft Store pour les entreprises**</span><span class="sxs-lookup"><span data-stu-id="cd070-135">**To force a sync between Intune and Microsoft Store for Business**</span></span>
1. <span data-ttu-id="cd070-136">Connectez-vous au [Portail Azure](https://portal.azure.com/) Intune Admin ou administrateur Global pour votre client</span><span class="sxs-lookup"><span data-stu-id="cd070-136">Sign in to [Azure Portal](https://portal.azure.com/) as Intune Admin or Global Admin for your tenant</span></span>
2. <span data-ttu-id="cd070-p106">Sélectionnez **tous les services > Intune**. Intune convient bien la surveillance + gestion section.</span><span class="sxs-lookup"><span data-stu-id="cd070-p106">Select **All services > Intune**. Intune is in the Monitoring + Management section.</span></span>
3. <span data-ttu-id="cd070-139">Dans le volet Intune, sélectionnez les **Applications clientes**, puis sélectionnez **Banque de Microsoft pour les entreprises**.</span><span class="sxs-lookup"><span data-stu-id="cd070-139">In the Intune pane, select **Client Apps**, and then select **Microsoft Store for Business**.</span></span>
4. <span data-ttu-id="cd070-140">Sélectionnez **Activer** pour synchroniser votre Store Microsoft pour les applications métiers avec Intune.</span><span class="sxs-lookup"><span data-stu-id="cd070-140">Select **Enable** to sync your Microsoft Store for Business apps with Intune.</span></span>
    - <span data-ttu-id="cd070-141">Si vous n’avez pas déjà, sign up et associer votre Microsoft stocker pour un compte professionnel avec Intune</span><span class="sxs-lookup"><span data-stu-id="cd070-141">If you haven't already, sign up and associate your Microsoft Store for Business account with Intune</span></span>
    - <span data-ttu-id="cd070-142">Sélectionnez la langue dans laquelle les applications de le Store Microsoft pour les entreprises seront affichera dans votre console Intune</span><span class="sxs-lookup"><span data-stu-id="cd070-142">Select the language in which apps from the Microsoft Store for Business will be displayed in your Intune console</span></span>
    - <span data-ttu-id="cd070-143">Sélectionnez la **synchronisation** pour synchroniser votre Store Microsoft pour les applications métiers avec Intune.</span><span class="sxs-lookup"><span data-stu-id="cd070-143">Select **Sync** to sync your Microsoft Store for Business apps with Intune.</span></span>
    - <span data-ttu-id="cd070-144">Vérifiez que la synchronisation entre Microsoft Store for Business et Intune est active (étape suivante).</span><span class="sxs-lookup"><span data-stu-id="cd070-144">Verify that the sync between Microsoft Store for Business and Intune is active (next step).</span></span> 

<span data-ttu-id="cd070-145">**Pour vérifier qu’une synchronisation entre Intune et Microsoft Store for Business est active**</span><span class="sxs-lookup"><span data-stu-id="cd070-145">**To verify that a sync between Intune and Microsoft Store for Business is active**</span></span>
1. <span data-ttu-id="cd070-146">Connectez-vous à [Microsoft Store for Business](https://businessstore.microsoft.com) avec votre Store Microsoft pour le compte d’administrateur d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="cd070-146">Sign in to [Microsoft Store for Business](https://businessstore.microsoft.com) with your Microsoft Store for Business Admin account.</span></span>
2. <span data-ttu-id="cd070-147">Sélectionnez **Gérer**.</span><span class="sxs-lookup"><span data-stu-id="cd070-147">Select **Manage**.</span></span>
3. <span data-ttu-id="cd070-148">Sélectionnez **paramètres** , puis **distribuer**.</span><span class="sxs-lookup"><span data-stu-id="cd070-148">Select **Settings** and then select **Distribute**.</span></span>
4. <span data-ttu-id="cd070-149">Sous **Outils de gestion**, vérifiez que Intune est répertorié et que l’état est **actif**.</span><span class="sxs-lookup"><span data-stu-id="cd070-149">Under **Management tools**, verify that Intune is listed and that the status is **Active**.</span></span>  

<span id="2" />

## <a name="step-2-create-azure-ad-groups"></a><span data-ttu-id="cd070-150">Étape 2 : Créer des groupes d’Azure AD</span><span class="sxs-lookup"><span data-stu-id="cd070-150">Step 2: Create Azure AD groups</span></span>

<span data-ttu-id="cd070-p107">Créez trois groupes Azure AD pour chaque application. Ce tableau présente les groupes dont vous aurez besoin (disponible, nécessaire et désinstaller).</span><span class="sxs-lookup"><span data-stu-id="cd070-p107">Create three Azure AD groups for each app. This table outlines the groups you'll need (Available, Required, and Uninstall).</span></span> 

<span data-ttu-id="cd070-153">Type d’application affectation</span><span class="sxs-lookup"><span data-stu-id="cd070-153">App assignment type</span></span> |   <span data-ttu-id="cd070-154">Utilisation de groupe</span><span class="sxs-lookup"><span data-stu-id="cd070-154">Group use</span></span>   | <span data-ttu-id="cd070-155">Nom de l’exemple Azure AD</span><span class="sxs-lookup"><span data-stu-id="cd070-155">Example Azure AD name</span></span>
--- | --- | ---
<span data-ttu-id="cd070-156">Disponible</span><span class="sxs-lookup"><span data-stu-id="cd070-156">Available</span></span> |  <span data-ttu-id="cd070-157">L’application sera disponible à partir d’application de portail d’entreprise ou un site Web.</span><span class="sxs-lookup"><span data-stu-id="cd070-157">The app will be available from Company Portal app or website.</span></span> | <span data-ttu-id="cd070-158">MMD – *nom de l’application* – disponible</span><span class="sxs-lookup"><span data-stu-id="cd070-158">MMD – *app name* – Available</span></span>
<span data-ttu-id="cd070-159">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="cd070-159">Required</span></span> |  <span data-ttu-id="cd070-160">L’application est installée sur des appareils dans les groupes sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="cd070-160">The app is installed on devices in the selected groups.</span></span> | <span data-ttu-id="cd070-161">MMD – *nom de l’application* – requis</span><span class="sxs-lookup"><span data-stu-id="cd070-161">MMD – *app name* – Required</span></span>
<span data-ttu-id="cd070-162">Désinstaller</span><span class="sxs-lookup"><span data-stu-id="cd070-162">Uninstall</span></span> |  <span data-ttu-id="cd070-163">Application estimée est désinstallée à partir des périphériques dans les groupes sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="cd070-163">TThe app is uninstalled from devices in the selected groups.</span></span> | <span data-ttu-id="cd070-164">MMD – *nom de l’application* – désinstaller</span><span class="sxs-lookup"><span data-stu-id="cd070-164">MMD – *app name* – Uninstall</span></span>

<span data-ttu-id="cd070-165">Ajouter des utilisateurs à ces groupes pour rendre l’application disponible, installer l’application ou supprimer l’application à partir de leur appareil de bureau Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cd070-165">Add your users to these groups to either make the app availabe, install the app, or remove the app from their Microsoft Managed Desktop device.</span></span> 

<span id="3" />

## <a name="step-3-assign-apps-to-your-users"></a><span data-ttu-id="cd070-166">Étape 3 : Attribuer des applications à vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="cd070-166">Step 3: Assign apps to your users</span></span>

<span data-ttu-id="cd070-167">**Pour affecter l’application à vos utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="cd070-167">**To assign the app to your users**</span></span>

1. <span data-ttu-id="cd070-168">Connectez-vous au [portail d’administration de bureau géré Microsoft](http://aka.ms/mmdportal).</span><span class="sxs-lookup"><span data-stu-id="cd070-168">Sign in to [Microsoft Managed Desktop Admin portal](http://aka.ms/mmdportal).</span></span>
2. <span data-ttu-id="cd070-169">Dans le volet de l’ordinateur de bureau, sélectionnez **applications**.</span><span class="sxs-lookup"><span data-stu-id="cd070-169">In Managed Desktop pane, select **Apps**.</span></span>
3. <span data-ttu-id="cd070-170">Dans la charge de travail des applications, sélectionnez l’application que vous souhaitez affecter des utilisateurs à et sélectionnez **affecter des groupes d’utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="cd070-170">In the Apps workload, select the app you want to assign users to and select **Assign users groups**.</span></span>
4. <span data-ttu-id="cd070-171">Pour l’application spécifique, sélectionnez un type d’affectation (disponible, requis, Uninstall) et affecter le groupe approprié.</span><span class="sxs-lookup"><span data-stu-id="cd070-171">For the specific app, select an assignment type (Available, Required, Uninstall) and assign the appropriate group.</span></span>
5. <span data-ttu-id="cd070-172">Dans le volet affecter des applications, sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd070-172">In the Assign Apps pane, select **OK**.</span></span>

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