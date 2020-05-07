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
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: 1136115a-75af-4497-b693-640c4ce70bc6
description: 'Créez des liens rapides vers vos courriers électroniques, vos documents, vos applications, vos sites SharePoint, vos sites externes et d’autres ressources en ajoutant des vignettes personnalisées au lanceur d’applications. '
ms.openlocfilehash: 44a8af104f6f39bd6b095a08f8ad9b2750d86d11
ms.sourcegitcommit: 83f980927728bc080f97a3e6dc70dc305f3df841
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2020
ms.locfileid: "44053775"
---
# <a name="add-custom-tiles-to-the-app-launcher"></a><span data-ttu-id="1152f-103">Ajouter des vignettes personnalisées au lanceur d'applications</span><span class="sxs-lookup"><span data-stu-id="1152f-103">Add custom tiles to the app launcher</span></span>

<span data-ttu-id="1152f-104">Dans Microsoft 365, vous pouvez rapidement et facilement accéder à vos courriers électroniques, calendriers, documents et applications à l’aide du lanceur d’applications ([en savoir plus](https://support.microsoft.com/en-us/office/meet-the-microsoft-365-app-launcher-79f12104-6fed-442f-96a0-eb089a3f476a)).</span><span class="sxs-lookup"><span data-stu-id="1152f-104">In Microsoft 365, you can quickly and easily get to your email, calendars, documents, and apps using the App launcher ([learn more](https://support.microsoft.com/en-us/office/meet-the-microsoft-365-app-launcher-79f12104-6fed-442f-96a0-eb089a3f476a)).</span></span> <span data-ttu-id="1152f-105">Il s’agit des applications que vous obtenez avec Microsoft 365, ainsi que des applications personnalisées que vous ajoutez à partir de [SharePoint Store](https://support.office.com/article/dd98e50e-d3db-4ecb-9bb7-82b189822d43.aspx) ou [Azure ad](https://msdn.microsoft.com/office/office365/howto/connect-your-app-to-o365-app-launcher).</span><span class="sxs-lookup"><span data-stu-id="1152f-105">These are apps you get with Microsoft 365 as well as custom apps that you add from the [SharePoint Store](https://support.office.com/article/dd98e50e-d3db-4ecb-9bb7-82b189822d43.aspx) or [Azure AD](https://msdn.microsoft.com/office/office365/howto/connect-your-app-to-o365-app-launcher).</span></span>
  
<span data-ttu-id="1152f-p102">Vous pouvez ajouter vos propres vignettes au lanceur d'applications pointant vers des sites SharePoint, des sites externes, des applications existantes, etc. La vignette personnalisée apparaît dans l'onglet **Toutes** les applications du lanceur d'applications. Vous pouvez également l'épingler aux applications de l'onglet **Accueil** et inviter vos utilisateurs à faire de même. Il sera ainsi plus facile de repérer les sites, les applications et les ressources dont vous avez besoin pour effectuer votre travail. Dans l'exemple ci-dessous, une vignette personnalisée nommée « Portail Contoso » permet d'accéder au site intranet SharePoint d'une organisation.</span><span class="sxs-lookup"><span data-stu-id="1152f-p102">You can add your own custom tiles to the app launcher that point to SharePoint sites, external sites, legacy apps, and more. The custom tile appears under the app launcher's **All** apps, but you can pin it to the **Home** apps and instruct your users to do the same. This makes it easy to find the relevant sites, apps, and resources to do your job. In the below example, a custom tile called "Contoso Portal" is used to access an organization's SharePoint intranet site.</span></span> 
  
![Lanceur d’applications](../../media/7acc06cc-ac7a-4c6e-8ea7-81570a5bdbab.png)
  
## <a name="add-a-custom-tile-to-the-app-launcher"></a><span data-ttu-id="1152f-111">Ajouter une vignette personnalisée au lanceur d'applications</span><span class="sxs-lookup"><span data-stu-id="1152f-111">Add a custom tile to the app launcher</span></span>

1. <span data-ttu-id="1152f-112">Dans le centre d’administration, accédez à **Settings** > **paramètres** des paramètres et sélectionnez l’onglet Profil de l' **organisation** .</span><span class="sxs-lookup"><span data-stu-id="1152f-112">In the admin center, go to the **Settings** > **Settings** and choose **Organization profile** tab.</span></span>
    
2. <span data-ttu-id="1152f-113">Sous l’onglet Profil de l' **organisation** , choisissez les **vignettes du lanceur d’applications personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="1152f-113">On the **Organization profile** tab, choose **Custom app launcher tiles**.</span></span>
  
3. <span data-ttu-id="1152f-114">Sélectionnez **Ajouter une vignette personnalisée**.</span><span class="sxs-lookup"><span data-stu-id="1152f-114">Select **Add a custom tile**.</span></span> 
  
4. <span data-ttu-id="1152f-115">Attribuez un **nom** à la nouvelle vignette.</span><span class="sxs-lookup"><span data-stu-id="1152f-115">Enter a **Tile name** for the new tile.</span></span> <span data-ttu-id="1152f-116">Le nom s'affiche alors dans la vignette.</span><span class="sxs-lookup"><span data-stu-id="1152f-116">The name will appear in the tile.</span></span> 
    
5. <span data-ttu-id="1152f-117">Entrez une **URL de site Web** pour la vignette.</span><span class="sxs-lookup"><span data-stu-id="1152f-117">Enter a **URL of website** for the tile.</span></span> <span data-ttu-id="1152f-118">Il s’agit de l’emplacement où les utilisateurs doivent accéder lorsqu’ils sélectionnent la vignette sur le lanceur d’applications.</span><span class="sxs-lookup"><span data-stu-id="1152f-118">This is the location where you want your users to go when they select the tile on the app launcher.</span></span> <span data-ttu-id="1152f-119">Utilisez le protocole HTTPs dans l’URL.</span><span class="sxs-lookup"><span data-stu-id="1152f-119">Use HTTPS in the URL.</span></span><br/><span data-ttu-id="1152f-120">Conseil : Si vous créez une vignette pour un site SharePoint, accédez à ce site, copiez l’URL et collez-la ici.</span><span class="sxs-lookup"><span data-stu-id="1152f-120">TIP: If you're creating a tile for a SharePoint site, navigate to that site, copy the URL, and paste it here.</span></span> <span data-ttu-id="1152f-121">L’URL de votre site d’équipe par défaut se présente comme suit :`https://<company_name>.sharepoint.com`</span><span class="sxs-lookup"><span data-stu-id="1152f-121">The URL of your default team site looks like this: `https://<company_name>.sharepoint.com`</span></span> 
  
6. <span data-ttu-id="1152f-122">Entrez l' **URL de l’image** de la vignette.</span><span class="sxs-lookup"><span data-stu-id="1152f-122">Enter an **URL of the image** for the tile.</span></span> <span data-ttu-id="1152f-123">Cette image apparaît sur la page Mes applications et le lanceur d'applications.</span><span class="sxs-lookup"><span data-stu-id="1152f-123">The image appears on the My apps page and app launcher.</span></span><br/><span data-ttu-id="1152f-124">Conseil : l’image doit être 60x60 pixels et être disponible pour tous les membres de votre organisation sans nécessiter une authentification.</span><span class="sxs-lookup"><span data-stu-id="1152f-124">TIP: The image should be 60x60 pixels and be available to everyone in your organization without requiring authentication.</span></span>

7. <span data-ttu-id="1152f-125">Entrez la **description** de la vignette.</span><span class="sxs-lookup"><span data-stu-id="1152f-125">Enter a **Description** for the tile.</span></span> <span data-ttu-id="1152f-126">Cette option apparaît lorsque vous sélectionnez la vignette sur la page mes applications et que vous sélectionnez Détails de l' **application**.</span><span class="sxs-lookup"><span data-stu-id="1152f-126">You see this when you select the tile on the My apps page and select **App details**.</span></span> 
  
8. <span data-ttu-id="1152f-127">Sélectionnez **enregistrer les modifications** pour créer la vignette personnalisée.</span><span class="sxs-lookup"><span data-stu-id="1152f-127">Select **Save changes** to create the custom tile.</span></span> 
    
<span data-ttu-id="1152f-128">Celle-ci apparaît désormais dans l'onglet **Toutes** du lanceur d'applications pour vous et vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1152f-128">Your custom tile now appears in the app launcher on the **All** tab for you and your users.</span></span> 
  
## <a name="promote-the-tile-to-app-launcher"></a><span data-ttu-id="1152f-129">Promouvoir la vignette sur le lanceur d’applications</span><span class="sxs-lookup"><span data-stu-id="1152f-129">Promote the tile to App Launcher</span></span>

1. <span data-ttu-id="1152f-130">Sélectionnez l’icône du lanceur d’applications et sélectionnez **toutes les applications**.</span><span class="sxs-lookup"><span data-stu-id="1152f-130">Select the app launcher icon and select the **All apps**.</span></span> 
    
2. <span data-ttu-id="1152f-131">Localisez la nouvelle vignette de votre application, sélectionnez les points de suspension, puis choisissez **code confidentiel pour le lanceur**.</span><span class="sxs-lookup"><span data-stu-id="1152f-131">Locate the new tile for your app, select the ellipsis, and choose **Pin to launcher**.</span></span>
  
    > [!NOTE]
    > <span data-ttu-id="1152f-132">Si la vignette personnalisée créée aux étapes précédente n'apparaît pas, vérifiez qu'une boîte aux lettres Exchange Online vous est affectée et que vous vous y êtes connecté au moins une fois.</span><span class="sxs-lookup"><span data-stu-id="1152f-132">If you don't see the custom tile created in the previous steps, make sure you have an Exchange Online mailbox assigned to you and you've signed into your mailbox at least once.</span></span> <span data-ttu-id="1152f-133">Ces étapes sont requises pour les vignettes personnalisées dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1152f-133">These steps are required for custom tiles in Microsoft 365.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="1152f-134">Vous et vos utilisateurs devez suivre les étapes ci-dessous pour promouvoir les vignettes personnalisées de la page Mes applications dans le lanceur d'applications.</span><span class="sxs-lookup"><span data-stu-id="1152f-134">Both you and your users need to perform these steps to promote custom tiles from the My apps page to the app launcher.</span></span> 
  
## <a name="edit-or-delete-a-custom-tile"></a><span data-ttu-id="1152f-135">Edit or delete a custom tile</span><span class="sxs-lookup"><span data-stu-id="1152f-135">Edit or delete a custom tile</span></span>

1. <span data-ttu-id="1152f-136">Dans le centre d’administration, accédez à l’onglet<a href="https://go.microsoft.com/fwlink/p/?linkid=2067339" target="_blank">profil d’organisation</a> des**paramètres** > de **paramètres** > .</span><span class="sxs-lookup"><span data-stu-id="1152f-136">In the admin center, go to the **Settings** > **Settings** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2067339" target="_blank">Organization profile</a> tab.</span></span>
    
2. <span data-ttu-id="1152f-137">Sur la page profil de l' **organisation** , en regard de **Ajouter des vignettes personnalisées pour votre organisation**, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="1152f-137">On the **Organization profile** page, next to   **Add custom tiles for your organization**, select **Edit**.</span></span>

3. <span data-ttu-id="1152f-138">Mettez à jour les champs **Nom de la vignette**, **URL**, **Description** ou **URL de l'image** de la vignette personnalisée (voir la [Ajouter une vignette personnalisée au lanceur d'applications](#add-a-custom-tile-to-the-app-launcher)).</span><span class="sxs-lookup"><span data-stu-id="1152f-138">Update the **Tile name**, **URL**, **Description**, or **Image URL** for the custom tile (see [Add a custom tile to the app launcher](#add-a-custom-tile-to-the-app-launcher)).</span></span>
    
4. <span data-ttu-id="1152f-139">Sélectionnez **Fermer**la **mise à jour** \> .</span><span class="sxs-lookup"><span data-stu-id="1152f-139">Select **Update** \> **Close**.</span></span> 
    
<span data-ttu-id="1152f-140">Pour supprimer une vignette personnalisée, dans la fenêtre **mosaïques personnalisées** , sélectionnez la vignette, sélectionnez Supprimer la**suppression**de **mosaïque** > .</span><span class="sxs-lookup"><span data-stu-id="1152f-140">To delete a custom tile, from the **Custom tiles** window, select the tile, select **Remove tile** > **Delete**.</span></span> 
  
## <a name="whats-next"></a><span data-ttu-id="1152f-141">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="1152f-141">What's next?</span></span>

<span data-ttu-id="1152f-142">En plus d’ajouter des vignettes au lanceur d’applications, vous pouvez ajouter des vignettes du lanceur d’applications dans la barre de navigation ([en savoir plus](https://support.office.com/article/personalize-your-office-365-experience-eb34a21b-52fa-4fbf-a8d5-146132242985)).</span><span class="sxs-lookup"><span data-stu-id="1152f-142">In addition to adding tiles to the app launcher, you can add app launcher tiles to the navigation bar ([learn more](https://support.office.com/article/personalize-your-office-365-experience-eb34a21b-52fa-4fbf-a8d5-146132242985)).</span></span> <span data-ttu-id="1152f-143">Pour personnaliser l’apparence de Microsoft 365 en fonction de la marque de votre organisation, consultez [la rubrique Customize the microsoft 365 Theme](../setup/customize-your-organization-theme.md).</span><span class="sxs-lookup"><span data-stu-id="1152f-143">To customize the look and feel of Microsoft 365 to match your organization's brand, see [Customize the Microsoft 365 theme](../setup/customize-your-organization-theme.md).</span></span>
  

