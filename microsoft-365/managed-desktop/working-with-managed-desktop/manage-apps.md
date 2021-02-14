---
title: Gérer les applications dans Le Bureau géré Microsoft
description: Informations sur la mise à jour des applications métier déployées sur les appareils de bureau géré Microsoft
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
f1.keywords:
- NOCSH
ms.author: jaimeo
ms.localizationpriority: normal
ms.date: 01/18/2019
ms.collection: M365-modern-desktop
ms.openlocfilehash: 1a6b91ab5b4523f4b980dab0c25af41a9d614189
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41600681"
---
# <a name="manage-line-of-business-apps-in-microsoft-managed-desktop"></a><span data-ttu-id="d56f8-104">Gérer les applications métier dans le bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="d56f8-104">Manage line-of-business apps in Microsoft Managed Desktop</span></span>

<!--Application management -->

<span data-ttu-id="d56f8-105">Il existe deux façons de gérer les mises à jour des applications pour les applications que vous avez intégrés au Bureau géré Microsoft et déployées sur vos appareils de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d56f8-105">There are a couple of ways to manage app updates for apps that you've onboarded to Microsoft Managed Desktop and deployed to your Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="d56f8-106">Vous pouvez effectuer des mises à jour d’application dans le portail Bureau géré Microsoft ou Intune.</span><span class="sxs-lookup"><span data-stu-id="d56f8-106">You can make app updates in Microsoft Managed Desktop portal, or Intune.</span></span> 

<span id="update-app-mmd" />

## <a name="update-line-of-business-apps-in-microsoft-managed-desktop"></a><span data-ttu-id="d56f8-107">Mettre à jour des applications métier dans le Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="d56f8-107">Update line-of-business apps in Microsoft Managed Desktop</span></span>

<span data-ttu-id="d56f8-108">**Pour mettre à jour vos applications métier dans le portail Bureau géré Microsoft**</span><span class="sxs-lookup"><span data-stu-id="d56f8-108">**To update your line-of-business apps in Microsoft Managed Desktop portal**</span></span>
1. <span data-ttu-id="d56f8-109">Connectez-vous au [portail d’administration du bureau géré Microsoft.](https://aka.ms/mmdportal)</span><span class="sxs-lookup"><span data-stu-id="d56f8-109">Sign in to [Microsoft Managed Desktop Admin portal](https://aka.ms/mmdportal).</span></span>
2. <span data-ttu-id="d56f8-110">Sous **Inventaire,** sélectionnez **Applications.**</span><span class="sxs-lookup"><span data-stu-id="d56f8-110">Under **Inventory**, select **Apps**.</span></span>  
3. <span data-ttu-id="d56f8-111">Sélectionnez l’application à mettre à jour, puis sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="d56f8-111">Select the app you want to updates, and then select **Edit**.</span></span>
4. <span data-ttu-id="d56f8-112">Sous **Gérer,** sélectionnez **Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="d56f8-112">Under **Manage**, select **Properties**.</span></span> 
5. <span data-ttu-id="d56f8-113">Cliquez **sur Fichier de package d’application,** puis recherchez un nouveau fichier de package d’application.</span><span class="sxs-lookup"><span data-stu-id="d56f8-113">Click **App package file**, and then browse to upload a new app package file.</span></span>
6. <span data-ttu-id="d56f8-114">Sélectionnez **le fichier de package d’application.**</span><span class="sxs-lookup"><span data-stu-id="d56f8-114">Select **App package file**.</span></span>
7. <span data-ttu-id="d56f8-115">Sélectionnez l’icône du dossier et accédez à l’emplacement de votre fichier d’application mis à jour.</span><span class="sxs-lookup"><span data-stu-id="d56f8-115">Select the folder icon and browse to the location of your updated app file.</span></span> <span data-ttu-id="d56f8-116">Sélectionnez **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="d56f8-116">Select **Open**.</span></span> <span data-ttu-id="d56f8-117">Les informations de l’application sont mises à jour avec les informations de package.</span><span class="sxs-lookup"><span data-stu-id="d56f8-117">The app information is updated with the package information.</span></span>
8. <span data-ttu-id="d56f8-118">Vérifiez que la **version de l’application** reflète le package d’application mis à jour.</span><span class="sxs-lookup"><span data-stu-id="d56f8-118">Verify that **App version** reflects the updated app package.</span></span> 

<span data-ttu-id="d56f8-119">L’application mise à jour sera déployée sur les appareils de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d56f8-119">The updated app will be deployed to your user's devices.</span></span>

<span id="update-app-intune" />

## <a name="update-line-of-business-apps-in-intune"></a><span data-ttu-id="d56f8-120">Mettre à jour des applications métier dans Intune</span><span class="sxs-lookup"><span data-stu-id="d56f8-120">Update line-of-business apps in Intune</span></span>

<span data-ttu-id="d56f8-121">**Pour mettre à jour vos applications métier dans Intune**</span><span class="sxs-lookup"><span data-stu-id="d56f8-121">**To update your line-of-business apps in Intune**</span></span>
1. <span data-ttu-id="d56f8-122">Connectez-vous au [portail Azure.](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="d56f8-122">Sign in to [Azure portal](https://portal.azure.com).</span></span>
2. <span data-ttu-id="d56f8-123">Sélectionnez **Tous les services**  >  **Intune**.</span><span class="sxs-lookup"><span data-stu-id="d56f8-123">Select **All Services** > **Intune**.</span></span> <span data-ttu-id="d56f8-124">Intune se trouve dans la section **Analyse + Gestion.**</span><span class="sxs-lookup"><span data-stu-id="d56f8-124">Intune is in the **Monitoring + Management** section.</span></span>
3. <span data-ttu-id="d56f8-125">Sélectionnez **applications clientes > applications.**</span><span class="sxs-lookup"><span data-stu-id="d56f8-125">Select **Client Apps > Apps**.</span></span>
4. <span data-ttu-id="d56f8-126">Recherchez et sélectionnez votre application dans la liste des applications.</span><span class="sxs-lookup"><span data-stu-id="d56f8-126">Find and select your app in the list of apps.</span></span>
5. <span data-ttu-id="d56f8-127">Dans le tableau **de** présentation, sélectionnez **Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="d56f8-127">In the **Overview** blade, select **Properties**.</span></span>
6. <span data-ttu-id="d56f8-128">Sélectionnez **le fichier de package d’application.**</span><span class="sxs-lookup"><span data-stu-id="d56f8-128">Select **App package file**.</span></span>
7. <span data-ttu-id="d56f8-129">Sélectionnez l’icône du dossier et accédez à l’emplacement de votre fichier d’application mis à jour.</span><span class="sxs-lookup"><span data-stu-id="d56f8-129">Select the folder icon and browse to the location of your updated app file.</span></span> <span data-ttu-id="d56f8-130">Sélectionnez **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="d56f8-130">Select **Open**.</span></span> <span data-ttu-id="d56f8-131">Les informations de l’application sont mises à jour avec les informations de package.</span><span class="sxs-lookup"><span data-stu-id="d56f8-131">The app information is updated with the package information.</span></span>
8. <span data-ttu-id="d56f8-132">Vérifiez que la **version de l’application** reflète le package d’application mis à jour.</span><span class="sxs-lookup"><span data-stu-id="d56f8-132">Verify that **App version** reflects the updated app package.</span></span>

<span id="roll-back-app-mmd" />

## <a name="roll-back-an-app-to-a-previous-version"></a><span data-ttu-id="d56f8-133">Revenir à une version antérieure d’une application</span><span class="sxs-lookup"><span data-stu-id="d56f8-133">Roll back an app to a previous version</span></span>

<span data-ttu-id="d56f8-134">Si une erreur est trouvée lors du déploiement d’une nouvelle version d’une application, vous pouvez revenir à une version précédente.</span><span class="sxs-lookup"><span data-stu-id="d56f8-134">If there's an error found when a new version of an app is deployed, you can roll back to a previous version.</span></span> <span data-ttu-id="d56f8-135">Le processus décrit ici est pour les applications où le type est répertorié en tant qu’application métier **Windows MSI** ou application **Windows (Win 32) - aperçu**</span><span class="sxs-lookup"><span data-stu-id="d56f8-135">The process outlined here is for apps where type is listed as **Windows MSI line-of-business app** or **Windows app (Win 32) - preview**</span></span>

<span data-ttu-id="d56f8-136">**Pour revenir à une version antérieure d’une application métier**</span><span class="sxs-lookup"><span data-stu-id="d56f8-136">**To roll back a line-of-business app to a previous version**</span></span>

1. <span data-ttu-id="d56f8-137">Connectez-vous au [portail d’administration du bureau géré Microsoft.](https://aka.ms/mmdportal)</span><span class="sxs-lookup"><span data-stu-id="d56f8-137">Sign in to [Microsoft Managed Desktop Admin portal](https://aka.ms/mmdportal).</span></span>
2. <span data-ttu-id="d56f8-138">Sous **Inventaire,** sélectionnez **Applications.**</span><span class="sxs-lookup"><span data-stu-id="d56f8-138">Under **Inventory**, select **Apps**.</span></span>  
3. <span data-ttu-id="d56f8-139">Sélectionnez l’application que vous devez revenir en arrière, puis sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="d56f8-139">Select the app you need to roll back, and then select **Edit**.</span></span>
4. <span data-ttu-id="d56f8-140">Sous **Gérer,** sélectionnez **Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="d56f8-140">Under **Manage**, select **Properties**.</span></span> 
    - <span data-ttu-id="d56f8-141">Pour les applications métier **Windows MSI,** sélectionnez Informations sur l’application, puis sous Ignorer la **version** de l’application, sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="d56f8-141">For **Windows MSI line-of-business app** apps, select **App information**, and then under **Ignore app version**, select **Yes**.</span></span>
    - <span data-ttu-id="d56f8-142">Pour **l’application Windows (Win 32) : prévisualiser** les applications, sélectionner les informations sur **l’application,** sélectionner les règles de **détection,** puis sélectionner Ajouter .</span><span class="sxs-lookup"><span data-stu-id="d56f8-142">For **Windows app (Win 32) - preview** apps, select **App information**, select **Detection rules**, and then select **Add**.</span></span> 
    <span data-ttu-id="d56f8-143">S’il existe une règle MSI, vérifiez que la vérification de la version du produit **MSI** est définie sur **Non**.</span><span class="sxs-lookup"><span data-stu-id="d56f8-143">If there is an MSI rule, verify that **MSI product version check** is set to **No**.</span></span>
5. <span data-ttu-id="d56f8-144">[Téléchargez une version précédente du fichier source](../get-started/deploy-apps.md) de l’application sur le portail d’administration du bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d56f8-144">[Upload a previous version of the app source file](../get-started/deploy-apps.md) to Microsoft Managed Desktop Admin portal.</span></span>  

