---
title: Gérer les applications dans le bureau géré Microsoft
description: Informations sur la mise à jour des applications métiers déployées sur des appareils de bureau gérés par Microsoft
keywords: Microsoft maNaged Desktop, Microsoft 365, service, documentation
ms.service: m365-md
author: trudyha
ms.localizationpriority: normal
ms.date: 01/18/2019
ms.collection: M365-modern-desktop
ms.openlocfilehash: ce2765ef2ab176dc5d9a1d41db7e26549b007d79
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285944"
---
# <a name="manage-line-of-business-apps-in-microsoft-managed-desktop"></a><span data-ttu-id="4196d-104">Gérer les applications métiers dans le bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="4196d-104">Manage line-of-business apps in Microsoft Managed Desktop</span></span>

<!--Application management -->

<span data-ttu-id="4196d-105">Il existe deux façons de gérer les mises à jour de l'application pour les applications que vous avez intégrées à Microsoft maNaged Desktop et déployées sur vos appareils de bureau gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4196d-105">There are a couple of ways to manage app updates for apps that you've onboarded to Microsoft Managed Desktop and deployed to your Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="4196d-106">Vous pouvez créer des mises à jour d'application dans le portail de bureau géré Microsoft ou dans Intune.</span><span class="sxs-lookup"><span data-stu-id="4196d-106">You can make app updates in Microsoft Managed Desktop portal, or Intune.</span></span> 

<span id="update-app-mmd" />

## <a name="update-line-of-business-apps-in-microsoft-managed-desktop"></a><span data-ttu-id="4196d-107">Mettre à jour les applications métiers dans le bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="4196d-107">Update line-of-business apps in Microsoft Managed Desktop</span></span>

<span data-ttu-id="4196d-108">**Pour mettre à jour vos applications métiers dans le portail de bureau géré Microsoft**</span><span class="sxs-lookup"><span data-stu-id="4196d-108">**To update your line-of-business apps in Microsoft Managed Desktop portal**</span></span>
1. <span data-ttu-id="4196d-109">Connectez-vous au [portail d'administration de bureau géré Microsoft](http://aka.ms/mmdportal).</span><span class="sxs-lookup"><span data-stu-id="4196d-109">Sign in to [Microsoft Managed Desktop Admin portal](http://aka.ms/mmdportal).</span></span>
2. <span data-ttu-id="4196d-110">Sous **inventaire**, sélectionnez **applications**.</span><span class="sxs-lookup"><span data-stu-id="4196d-110">Under **Inventory**, select **Apps**.</span></span>  
3. <span data-ttu-id="4196d-111">Sélectionnez l'application que vous souhaitez mettre à jour, puis sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="4196d-111">Select the app you want to updates, and then select **Edit**.</span></span>
4. <span data-ttu-id="4196d-112">Sous **gérer**, sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="4196d-112">Under **Manage**, select **Properties**.</span></span> 
5. <span data-ttu-id="4196d-113">Cliquez sur **fichier de package d'application**, puis accédez à télécharger un nouveau fichier de package d'application.</span><span class="sxs-lookup"><span data-stu-id="4196d-113">Click **App package file**, and then browse to upload a new app package file.</span></span>
6. <span data-ttu-id="4196d-114">Sélectionnez **fichier de package d'application**.</span><span class="sxs-lookup"><span data-stu-id="4196d-114">Select **App package file**.</span></span>
7. <span data-ttu-id="4196d-115">Sélectionnez l'icône de dossier et accédez à l'emplacement de votre fichier d'application mis à jour.</span><span class="sxs-lookup"><span data-stu-id="4196d-115">Select the folder icon and browse to the location of your updated app file.</span></span> <span data-ttu-id="4196d-116">Sélectionnez **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="4196d-116">Select **Open**.</span></span> <span data-ttu-id="4196d-117">Les informations de l'application sont mises à jour avec les informations du package.</span><span class="sxs-lookup"><span data-stu-id="4196d-117">The app information is updated with the package information.</span></span>
8. <span data-ttu-id="4196d-118">Vérifiez que la version de l' **application** reflète le package d'application mis à jour.</span><span class="sxs-lookup"><span data-stu-id="4196d-118">Verify that **App version** reflects the updated app package.</span></span> 

<span data-ttu-id="4196d-119">L'application mise à jour sera déployée sur les appareils de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4196d-119">The updated app will be deployed to your user's devices.</span></span>

<span id="update-app-intune" />

## <a name="update-line-of-business-apps-in-intune"></a><span data-ttu-id="4196d-120">Mettre à jour les applications métiers dans Intune</span><span class="sxs-lookup"><span data-stu-id="4196d-120">Update line-of-business apps in Intune</span></span>

<span data-ttu-id="4196d-121">**Pour mettre à jour vos applications métiers dans Intune**</span><span class="sxs-lookup"><span data-stu-id="4196d-121">**To update your line-of-business apps in Intune**</span></span>
1. <span data-ttu-id="4196d-122">Connectez-vous au [portail Azure](https://azure.portal.com).</span><span class="sxs-lookup"><span data-stu-id="4196d-122">Sign in to [Azure portal](https://azure.portal.com).</span></span>
2. <span data-ttu-id="4196d-123">Sélectionnez **tous les services** > **Intune**.</span><span class="sxs-lookup"><span data-stu-id="4196d-123">Select **All Services** > **Intune**.</span></span> <span data-ttu-id="4196d-124">Intune se trouve dans la section **surveillance + Management** .</span><span class="sxs-lookup"><span data-stu-id="4196d-124">Intune is in the **Monitoring + Management** section.</span></span>
3. <span data-ttu-id="4196d-125">Sélectionnez applications **clientEs _GT_ applications**.</span><span class="sxs-lookup"><span data-stu-id="4196d-125">Select **Client Apps > Apps**.</span></span>
4. <span data-ttu-id="4196d-126">Recherchez et sélectionnez votre application dans la liste des applications.</span><span class="sxs-lookup"><span data-stu-id="4196d-126">Find and select your app in the list of apps.</span></span>
5. <span data-ttu-id="4196d-127">Dans le panneau de **vue d'ensemble** , sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="4196d-127">In the **Overview** blade, select **Properties**.</span></span>
6. <span data-ttu-id="4196d-128">Sélectionnez **fichier de package d'application**.</span><span class="sxs-lookup"><span data-stu-id="4196d-128">Select **App package file**.</span></span>
7. <span data-ttu-id="4196d-129">Sélectionnez l'icône de dossier et accédez à l'emplacement de votre fichier d'application mis à jour.</span><span class="sxs-lookup"><span data-stu-id="4196d-129">Select the folder icon and browse to the location of your updated app file.</span></span> <span data-ttu-id="4196d-130">Sélectionnez **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="4196d-130">Select **Open**.</span></span> <span data-ttu-id="4196d-131">Les informations de l'application sont mises à jour avec les informations du package.</span><span class="sxs-lookup"><span data-stu-id="4196d-131">The app information is updated with the package information.</span></span>
8. <span data-ttu-id="4196d-132">Vérifiez que la version de l' **application** reflète le package d'application mis à jour.</span><span class="sxs-lookup"><span data-stu-id="4196d-132">Verify that **App version** reflects the updated app package.</span></span>

<span id="roll-back-app-mmd" />

## <a name="roll-back-an-app-to-a-previous-version"></a><span data-ttu-id="4196d-133">Restaurer une version antérieure d'une application</span><span class="sxs-lookup"><span data-stu-id="4196d-133">Roll back an app to a previous version</span></span>

<span data-ttu-id="4196d-134">Si une erreur est détectée lors du déploiement d'une nouvelle version d'une application, vous pouvez revenir à une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="4196d-134">If there's an error found when a new version of an app is deployed, you can roll back to a previous version.</span></span> <span data-ttu-id="4196d-135">Le processus décrit ici est destiné aux applications où le type est répertorié en tant qu' **application métier Windows MSI** ou **application windows (Win 32)-Aperçu**</span><span class="sxs-lookup"><span data-stu-id="4196d-135">The process outlined here is for apps where type is listed as **Windows MSI line-of-business app** or **Windows app (Win 32) - preview**</span></span>

<span data-ttu-id="4196d-136">**Pour restaurer une application métier vers une version antérieure**</span><span class="sxs-lookup"><span data-stu-id="4196d-136">**To roll back a line-of-business app to a previous version**</span></span>

1. <span data-ttu-id="4196d-137">Connectez-vous au [portail d'administration de bureau géré Microsoft](http://aka.ms/mmdportal).</span><span class="sxs-lookup"><span data-stu-id="4196d-137">Sign in to [Microsoft Managed Desktop Admin portal](http://aka.ms/mmdportal).</span></span>
2. <span data-ttu-id="4196d-138">Sous **inventaire**, sélectionnez **applications**.</span><span class="sxs-lookup"><span data-stu-id="4196d-138">Under **Inventory**, select **Apps**.</span></span>  
3. <span data-ttu-id="4196d-139">Sélectionnez l'application que vous devez restaurer, puis sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="4196d-139">Select the app you need to roll back, and then select **Edit**.</span></span>
4. <span data-ttu-id="4196d-140">Sous **gérer**, sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="4196d-140">Under **Manage**, select **Properties**.</span></span> 
    - <span data-ttu-id="4196d-141">Pour les applications d' **application sectorielle Windows MSI** , sélectionnez **informations sur l'application**, puis sous **ignorer la version**de l'application, sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="4196d-141">For **Windows MSI line-of-business app** apps, select **App information**, and then under **Ignore app version**, select **Yes**.</span></span>
    - <span data-ttu-id="4196d-142">Pour **Windows App (Win 32)-Preview** Apps, SELECT **app information**, SELECT **detectIon Rules**, puis **Add**.</span><span class="sxs-lookup"><span data-stu-id="4196d-142">For **Windows app (Win 32) - preview** apps, select **App information**, select **Detection rules**, and then select **Add**.</span></span> 
    <span data-ttu-id="4196d-143">S'il existe une règle MSI, vérifiez que la **case à cocher vérification de la version du produit MSI** est définie sur **non**.</span><span class="sxs-lookup"><span data-stu-id="4196d-143">If there is an MSI rule, verify that **MSI product version check** is set to **No**.</span></span>
5. <span data-ttu-id="4196d-144">[Téléchargez une version précédente du fichier source de l'application vers le](../get-started/deploy-apps.md) portail d'administration de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4196d-144">[Upload a previous version of the app source file](../get-started/deploy-apps.md) to Microsoft Managed Desktop Admin portal.</span></span>  

