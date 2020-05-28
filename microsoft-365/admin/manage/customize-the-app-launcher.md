---
title: Ajouter des vignettes personnalisées au lanceur d'applications
f1.keywords:
- CSH
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
- Adm_TOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: 1136115a-75af-4497-b693-640c4ce70bc6
description: 'Créez des liens rapides vers vos courriers électroniques, vos documents, vos applications, vos sites SharePoint, vos sites externes et d’autres ressources en ajoutant des vignettes personnalisées au lanceur d’applications. '
ms.openlocfilehash: cad78207c5d4025d385a7452fbe86df79a694067
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44399775"
---
# <a name="add-custom-tiles-to-the-app-launcher"></a><span data-ttu-id="aaa05-103">Ajouter des vignettes personnalisées au lanceur d'applications</span><span class="sxs-lookup"><span data-stu-id="aaa05-103">Add custom tiles to the app launcher</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="aaa05-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="aaa05-104">The admin center is changing.</span></span> <span data-ttu-id="aaa05-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="aaa05-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="aaa05-106">Dans Microsoft 365, vous pouvez rapidement et facilement accéder à vos courriers électroniques, calendriers, documents et applications à l’aide du lanceur d’applications ([en savoir plus](https://support.office.com/article/79f12104-6fed-442f-96a0-eb089a3f476a.aspx)).</span><span class="sxs-lookup"><span data-stu-id="aaa05-106">In Microsoft 365, you can quickly and easily get to your email, calendars, documents, and apps using the App launcher ([learn more](https://support.office.com/article/79f12104-6fed-442f-96a0-eb089a3f476a.aspx)).</span></span> <span data-ttu-id="aaa05-107">Il s’agit des applications que vous obtenez avec Microsoft 365, ainsi que des applications personnalisées que vous ajoutez à partir de [SharePoint Store](https://support.office.com/article/dd98e50e-d3db-4ecb-9bb7-82b189822d43.aspx) ou [Azure ad](https://msdn.microsoft.com/office/office365/howto/connect-your-app-to-o365-app-launcher).</span><span class="sxs-lookup"><span data-stu-id="aaa05-107">These are apps you get with Microsoft 365 as well as custom apps that you add from the [SharePoint Store](https://support.office.com/article/dd98e50e-d3db-4ecb-9bb7-82b189822d43.aspx) or [Azure AD](https://msdn.microsoft.com/office/office365/howto/connect-your-app-to-o365-app-launcher).</span></span>
  
<span data-ttu-id="aaa05-p103">Vous pouvez ajouter vos propres vignettes au lanceur d'applications pointant vers des sites SharePoint, des sites externes, des applications existantes, etc. La vignette personnalisée apparaît dans l'onglet **Toutes** les applications du lanceur d'applications. Vous pouvez également l'épingler aux applications de l'onglet **Accueil** et inviter vos utilisateurs à faire de même. Il sera ainsi plus facile de repérer les sites, les applications et les ressources dont vous avez besoin pour effectuer votre travail. Dans l'exemple ci-dessous, une vignette personnalisée nommée « Portail Contoso » permet d'accéder au site intranet SharePoint d'une organisation.</span><span class="sxs-lookup"><span data-stu-id="aaa05-p103">You can add your own custom tiles to the app launcher that point to SharePoint sites, external sites, legacy apps, and more. The custom tile appears under the app launcher's **All** apps, but you can pin it to the **Home** apps and instruct your users to do the same. This makes it easy to find the relevant sites, apps, and resources to do your job. In the below example, a custom tile called "Contoso Portal" is used to access an organization's SharePoint intranet site.</span></span> 
  
![Lanceur d’applications](../../media/7acc06cc-ac7a-4c6e-8ea7-81570a5bdbab.png)
  
## <a name="add-a-custom-tile-to-the-app-launcher"></a><span data-ttu-id="aaa05-113">Ajouter une vignette personnalisée au lanceur d'applications</span><span class="sxs-lookup"><span data-stu-id="aaa05-113">Add a custom tile to the app launcher</span></span>

1. <span data-ttu-id="aaa05-114">Dans le centre d’administration, accédez aux **Settings**paramètres  >  **org** paramètres et sélectionnez l’onglet **Profil** de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="aaa05-114">In the admin center, go to the **Settings** > **Org Settings** and choose **Organization profile** tab.</span></span>
    
2. <span data-ttu-id="aaa05-115">Sous l’onglet Profil de l' **organisation** , choisissez les **vignettes du lanceur d’applications personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="aaa05-115">On the **Organization profile** tab, choose **Custom app launcher tiles**.</span></span>
  
3. <span data-ttu-id="aaa05-116">Sélectionnez **Ajouter une vignette personnalisée**.</span><span class="sxs-lookup"><span data-stu-id="aaa05-116">Select **Add a custom tile**.</span></span> 
  
4. <span data-ttu-id="aaa05-117">Attribuez un **nom** à la nouvelle vignette.</span><span class="sxs-lookup"><span data-stu-id="aaa05-117">Enter a **Tile name** for the new tile.</span></span> <span data-ttu-id="aaa05-118">Le nom s'affiche alors dans la vignette.</span><span class="sxs-lookup"><span data-stu-id="aaa05-118">The name will appear in the tile.</span></span> 
    
5. <span data-ttu-id="aaa05-119">Entrez une **URL de site Web** pour la vignette.</span><span class="sxs-lookup"><span data-stu-id="aaa05-119">Enter a **URL of website** for the tile.</span></span> <span data-ttu-id="aaa05-120">Il s’agit de l’emplacement où les utilisateurs doivent accéder lorsqu’ils sélectionnent la vignette sur le lanceur d’applications.</span><span class="sxs-lookup"><span data-stu-id="aaa05-120">This is the location where you want your users to go when they select the tile on the app launcher.</span></span> <span data-ttu-id="aaa05-121">Utilisez le protocole HTTPs dans l’URL.</span><span class="sxs-lookup"><span data-stu-id="aaa05-121">Use HTTPS in the URL.</span></span><br/><span data-ttu-id="aaa05-122">Conseil : Si vous créez une vignette pour un site SharePoint, accédez à ce site, copiez l’URL et collez-la ici.</span><span class="sxs-lookup"><span data-stu-id="aaa05-122">TIP: If you're creating a tile for a SharePoint site, navigate to that site, copy the URL, and paste it here.</span></span> <span data-ttu-id="aaa05-123">L’URL de votre site d’équipe par défaut se présente comme suit :`https://<company_name>.sharepoint.com`</span><span class="sxs-lookup"><span data-stu-id="aaa05-123">The URL of your default team site looks like this: `https://<company_name>.sharepoint.com`</span></span> 
  
6. <span data-ttu-id="aaa05-124">Entrez l' **URL de l’image** de la vignette.</span><span class="sxs-lookup"><span data-stu-id="aaa05-124">Enter an **URL of the image** for the tile.</span></span> <span data-ttu-id="aaa05-125">Cette image apparaît sur la page Mes applications et le lanceur d'applications.</span><span class="sxs-lookup"><span data-stu-id="aaa05-125">The image appears on the My apps page and app launcher.</span></span><br/><span data-ttu-id="aaa05-126">Conseil : l’image doit être 60x60 pixels et être disponible pour tous les membres de votre organisation sans nécessiter une authentification.</span><span class="sxs-lookup"><span data-stu-id="aaa05-126">TIP: The image should be 60x60 pixels and be available to everyone in your organization without requiring authentication.</span></span>

7. <span data-ttu-id="aaa05-127">Entrez la **description** de la vignette.</span><span class="sxs-lookup"><span data-stu-id="aaa05-127">Enter a **Description** for the tile.</span></span> <span data-ttu-id="aaa05-128">Cette option apparaît lorsque vous sélectionnez la vignette sur la page mes applications et que vous sélectionnez Détails de l' **application**.</span><span class="sxs-lookup"><span data-stu-id="aaa05-128">You see this when you select the tile on the My apps page and select **App details**.</span></span> 
  
8. <span data-ttu-id="aaa05-129">Sélectionnez **enregistrer les modifications** pour créer la vignette personnalisée.</span><span class="sxs-lookup"><span data-stu-id="aaa05-129">Select **Save changes** to create the custom tile.</span></span> 
    
<span data-ttu-id="aaa05-130">Celle-ci apparaît désormais dans l'onglet **Toutes** du lanceur d'applications pour vous et vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="aaa05-130">Your custom tile now appears in the app launcher on the **All** tab for you and your users.</span></span> 
  
## <a name="promote-the-tile-to-app-launcher"></a><span data-ttu-id="aaa05-131">Promouvoir la vignette sur le lanceur d’applications</span><span class="sxs-lookup"><span data-stu-id="aaa05-131">Promote the tile to App Launcher</span></span>

1. <span data-ttu-id="aaa05-132">Sélectionnez l’icône du lanceur d’applications et sélectionnez **toutes les applications**.</span><span class="sxs-lookup"><span data-stu-id="aaa05-132">Select the app launcher icon and select the **All apps**.</span></span> 
    
2. <span data-ttu-id="aaa05-133">Localisez la nouvelle vignette de votre application, sélectionnez les points de suspension, puis choisissez **code confidentiel pour le lanceur**.</span><span class="sxs-lookup"><span data-stu-id="aaa05-133">Locate the new tile for your app, select the ellipsis, and choose **Pin to launcher**.</span></span>
  
    > [!NOTE]
    > <span data-ttu-id="aaa05-134">Si la vignette personnalisée créée aux étapes précédente n'apparaît pas, vérifiez qu'une boîte aux lettres Exchange Online vous est affectée et que vous vous y êtes connecté au moins une fois.</span><span class="sxs-lookup"><span data-stu-id="aaa05-134">If you don't see the custom tile created in the previous steps, make sure you have an Exchange Online mailbox assigned to you and you've signed into your mailbox at least once.</span></span> <span data-ttu-id="aaa05-135">Ces étapes sont requises pour les vignettes personnalisées dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="aaa05-135">These steps are required for custom tiles in Microsoft 365.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="aaa05-136">Vous et vos utilisateurs devez suivre les étapes ci-dessous pour promouvoir les vignettes personnalisées de la page Mes applications dans le lanceur d'applications.</span><span class="sxs-lookup"><span data-stu-id="aaa05-136">Both you and your users need to perform these steps to promote custom tiles from the My apps page to the app launcher.</span></span> 
  
## <a name="edit-or-delete-a-custom-tile"></a><span data-ttu-id="aaa05-137">Edit or delete a custom tile</span><span class="sxs-lookup"><span data-stu-id="aaa05-137">Edit or delete a custom tile</span></span>

1. <span data-ttu-id="aaa05-138">Dans le centre d’administration, accédez à **Settings**l'  >  **Org Settings**  >  onglet Profil d’organisation des paramètres d'**organisation** des paramètres </a> .</span><span class="sxs-lookup"><span data-stu-id="aaa05-138">In the admin center, go to the **Settings** > **Org Settings** > **Organization profile**</a> tab.</span></span>
    
2. <span data-ttu-id="aaa05-139">Sur la page profil de l' **organisation** , en regard de **Ajouter des vignettes personnalisées pour votre organisation**, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="aaa05-139">On the **Organization profile** page, next to   **Add custom tiles for your organization**, select **Edit**.</span></span>

3. <span data-ttu-id="aaa05-140">Mettez à jour les champs **Nom de la vignette**, **URL**, **Description** ou **URL de l'image** de la vignette personnalisée (voir la [Ajouter une vignette personnalisée au lanceur d'applications](#add-a-custom-tile-to-the-app-launcher)).</span><span class="sxs-lookup"><span data-stu-id="aaa05-140">Update the **Tile name**, **URL**, **Description**, or **Image URL** for the custom tile (see [Add a custom tile to the app launcher](#add-a-custom-tile-to-the-app-launcher)).</span></span>
    
4. <span data-ttu-id="aaa05-141">Sélectionnez Fermer la **mise à jour** \> **Close**.</span><span class="sxs-lookup"><span data-stu-id="aaa05-141">Select **Update** \> **Close**.</span></span> 
    
<span data-ttu-id="aaa05-142">Pour supprimer une vignette personnalisée, dans la fenêtre **mosaïques personnalisées** , sélectionnez la vignette, sélectionnez Supprimer la suppression de **mosaïque**  >  **Delete**.</span><span class="sxs-lookup"><span data-stu-id="aaa05-142">To delete a custom tile, from the **Custom tiles** window, select the tile, select **Remove tile** > **Delete**.</span></span> 
  
## <a name="whats-next"></a><span data-ttu-id="aaa05-143">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="aaa05-143">What's next?</span></span>

<span data-ttu-id="aaa05-144">En plus d’ajouter des vignettes au lanceur d’applications, vous pouvez ajouter des vignettes du lanceur d’applications dans la barre de navigation ([en savoir plus](https://support.office.com/article/personalize-your-office-365-experience-eb34a21b-52fa-4fbf-a8d5-146132242985)).</span><span class="sxs-lookup"><span data-stu-id="aaa05-144">In addition to adding tiles to the app launcher, you can add app launcher tiles to the navigation bar ([learn more](https://support.office.com/article/personalize-your-office-365-experience-eb34a21b-52fa-4fbf-a8d5-146132242985)).</span></span> <span data-ttu-id="aaa05-145">Pour personnaliser l’apparence de Microsoft 365 en fonction de la marque de votre organisation, consultez [la rubrique Customize the microsoft 365 Theme](../setup/customize-your-organization-theme.md).</span><span class="sxs-lookup"><span data-stu-id="aaa05-145">To customize the look and feel of Microsoft 365 to match your organization's brand, see [Customize the Microsoft 365 theme](../setup/customize-your-organization-theme.md).</span></span>
  

