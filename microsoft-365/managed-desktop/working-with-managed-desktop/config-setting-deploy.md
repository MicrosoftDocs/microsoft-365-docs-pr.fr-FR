---
title: Déployer des paramètres configurables dans bureau géré Microsoft
description: Déployez et suivez les modifications des paramètres configurables dans Bureau géré Microsoft.
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation, déployer, déploiement par étapes, paramètres configurables
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: a24d0dc64e2262a8b208119c45a4a6bade701c10
ms.sourcegitcommit: adaedd1418a3bd6e4875b77fd9e008b47e0b2a51
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48104533"
---
# <a name="deploy-and-track-configurable-settings---microsoft-managed-desktop"></a><span data-ttu-id="89432-104">Déployer et suivre les paramètres configurables - Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="89432-104">Deploy and track configurable settings - Microsoft Managed Desktop</span></span>

<span data-ttu-id="89432-105">Après avoir apporté des modifications à vos catégories de paramètres et organisé un déploiement, la page État du déploiement vous permet de commencer à déployer vos paramètres dans des groupes.</span><span class="sxs-lookup"><span data-stu-id="89432-105">After you make changes to your setting categories and stage a deployment, the Deployment status page allows you to begin deploying your settings to groups.</span></span> <span data-ttu-id="89432-106">Cette page affiche un résumé de chaque paramètre configurable.</span><span class="sxs-lookup"><span data-stu-id="89432-106">This page shows a summary of each configurable setting.</span></span> <span data-ttu-id="89432-107">En ouvrant une catégorie de paramètres, vous pouvez déployer des paramètres sur des groupes et suivre la progression de ces déploiements.</span><span class="sxs-lookup"><span data-stu-id="89432-107">By opening a setting category you can deploy settings to groups and track the progress of these deployments.</span></span>

## <a name="deployment-statuses"></a><span data-ttu-id="89432-108">Statuts de déploiement</span><span class="sxs-lookup"><span data-stu-id="89432-108">Deployment statuses</span></span> 

<span data-ttu-id="89432-109">Voici les états que vous verrez pour chaque déploiement.</span><span class="sxs-lookup"><span data-stu-id="89432-109">These are the statuses you’ll see for each deployment.</span></span>

<span data-ttu-id="89432-110">Statut</span><span class="sxs-lookup"><span data-stu-id="89432-110">Status</span></span>  | <span data-ttu-id="89432-111">Explication</span><span class="sxs-lookup"><span data-stu-id="89432-111">Explanation</span></span> 
--- | --- 
<span data-ttu-id="89432-112">Déployer</span><span class="sxs-lookup"><span data-stu-id="89432-112">Deploy</span></span> | <span data-ttu-id="89432-113">Votre modification attend d’être déployée sur ce groupe.</span><span class="sxs-lookup"><span data-stu-id="89432-113">Your change is waiting to be deployed to this group.</span></span>
<span data-ttu-id="89432-114">En cours</span><span class="sxs-lookup"><span data-stu-id="89432-114">In progress</span></span> | <span data-ttu-id="89432-115">La modification est appliquée aux appareils actifs de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="89432-115">The change is being applied to active devices in this group.</span></span> 
<span data-ttu-id="89432-116">Exécuter</span><span class="sxs-lookup"><span data-stu-id="89432-116">Complete</span></span> | <span data-ttu-id="89432-117">Modification effectuée sur tous les appareils actifs de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="89432-117">The change completed on all active devices in this group.</span></span> 
<span data-ttu-id="89432-118">Échec</span><span class="sxs-lookup"><span data-stu-id="89432-118">Failed</span></span> | <span data-ttu-id="89432-119">La modification a échoué sur 10 % des appareils actifs du groupe, de sorte que le déploiement a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="89432-119">The change failed on a 10 percent of active devices in the group, so the deployment was stopped.</span></span><br><br> <span data-ttu-id="89432-120">Une demande de support est automatiquement ouverte avec les opérations bureau géré Microsoft pour résoudre les problèmes de déploiement.</span><span class="sxs-lookup"><span data-stu-id="89432-120">A support request will be automatically opened with Microsoft Managed Desktop operations to troubleshoot the deployment.</span></span> 
<span data-ttu-id="89432-121">Révérence</span><span class="sxs-lookup"><span data-stu-id="89432-121">Reverted</span></span> | <span data-ttu-id="89432-122">La modification a été revenir à la dernière modification qui a été correctement déployée sur tous les groupes de déploiement.</span><span class="sxs-lookup"><span data-stu-id="89432-122">The change was reverted to the last change that was successfully deployed to all deployment groups.</span></span>

## <a name="deploy-changes"></a><span data-ttu-id="89432-123">Déployer les modifications</span><span class="sxs-lookup"><span data-stu-id="89432-123">Deploy changes</span></span>

<span data-ttu-id="89432-124">Nous allons afficher l’image d’arrière-plan du bureau dans ces instructions.</span><span class="sxs-lookup"><span data-stu-id="89432-124">We’ll show Desktop background picture in these instructions.</span></span> <span data-ttu-id="89432-125">Une fois que vous avez mis en place un déploiement, vous déployez les modifications à partir de la page État du déploiement.</span><span class="sxs-lookup"><span data-stu-id="89432-125">After you’ve staged a deployment, you deploy changes from the Deployment status page.</span></span> 

<span data-ttu-id="89432-126">**Pour déployer les modifications**</span><span class="sxs-lookup"><span data-stu-id="89432-126">**To deploy changes**</span></span>

1. <span data-ttu-id="89432-127">Connectez-vous au Gestionnaire de point de [terminaison Microsoft](https://endpoint.microsoft.com/) et accédez au menu **Appareils**</span><span class="sxs-lookup"><span data-stu-id="89432-127">Sign in to [Microsoft Endpoint Manager](https://endpoint.microsoft.com/) and navigate to the **Devices** menu</span></span>
2. <span data-ttu-id="89432-128">Recherchez la section Bureau géré Microsoft, sélectionnez **Paramètres.**</span><span class="sxs-lookup"><span data-stu-id="89432-128">Look for the Microsoft Managed Desktop section, select **Settings**.</span></span>
3. <span data-ttu-id="89432-129">Dans **l’espace** de travail État du déploiement, sélectionnez le paramètre à déployer, puis le déploiement par étapes à déployer.</span><span class="sxs-lookup"><span data-stu-id="89432-129">In **Deployment status** workspace, select the setting you want to deploy, and then select the staged deployment to deploy.</span></span>
4. <span data-ttu-id="89432-130">Sélectionnez **Déployer** pour déployer la modification dans l’un des groupes de déploiement.</span><span class="sxs-lookup"><span data-stu-id="89432-130">Select **Deploy** to deploy the change to one of the deployment groups.</span></span>

> [!NOTE] 
> <span data-ttu-id="89432-131">L’icône d’avertissement orange indique qu’un groupe précédent est disponible pour le déploiement, car il est recommandé de le déployer dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="89432-131">The orange caution icon indicates there is a previous group available for deployment as it’s recommended to roll out in order.</span></span> 

<!-- Needs picture updated to show MEM ![Deployment status workspace. Trusted sites pane on the right. In the Deployment groups section are three columns: deployment groups, devices, and status. In the status column, "deploy" is highlighted.](../../media/1deployedit.png) -->

<span data-ttu-id="89432-132">Nous vous recommandons de déployer les groupes de déploiement dans cet ordre : Test, Premier, Rapide, puis Large.</span><span class="sxs-lookup"><span data-stu-id="89432-132">We recommend deploying to deployment groups in this order: Test, First, Fast, and then Broad.</span></span> 

<span data-ttu-id="89432-133">Lorsque les modifications sont terminées dans chaque groupe, l’état est **terminé.**</span><span class="sxs-lookup"><span data-stu-id="89432-133">When changes complete in each group, the status changes to **Complete**.</span></span>

<!-- Needs picture updated to show MEM ![Deployment status workspace with columns for date updated, version, test, first, fast, and broad. The Proxy row is expanded, showing a dated setting flagged as "complete" in each of the four deployment groups.](../../media/2completeedit.png) -->

## <a name="revert-deployment"></a><span data-ttu-id="89432-134">Revert deployment</span><span class="sxs-lookup"><span data-stu-id="89432-134">Revert deployment</span></span>

<span data-ttu-id="89432-135">Une fois que vous avez déployé une modification, vous pouvez revenir à **l’état de déploiement.**</span><span class="sxs-lookup"><span data-stu-id="89432-135">After you’ve deployed a change, you can revert from **Deployment status**.</span></span> <span data-ttu-id="89432-136">Lorsque vous inversez une modification en cours **ou** **terminée,** le déploiement actuel s’arrête.</span><span class="sxs-lookup"><span data-stu-id="89432-136">When you revert a change that is **In progress** or **Complete**, the current deployment stops.</span></span> <span data-ttu-id="89432-137">Le paramètre revient à la dernière version qui a été déployée pour tous les groupes.</span><span class="sxs-lookup"><span data-stu-id="89432-137">The setting will revert to the last version that was deployed to all groups.</span></span> 

<span data-ttu-id="89432-138">Nous allons vous montrer les étapes à suivre pour inverser une modification à l’aide de l’image d’arrière-plan du Bureau à titre d’exemple.</span><span class="sxs-lookup"><span data-stu-id="89432-138">We’ll show the steps to revert a change using the Desktop background picture as an example.</span></span> 

<span data-ttu-id="89432-139">**Pour inverser une modification**</span><span class="sxs-lookup"><span data-stu-id="89432-139">**To revert a change**</span></span>
1. <span data-ttu-id="89432-140">Connectez-vous au Gestionnaire de points de [terminaison Microsoft](https://endpoint.microsoft.com/) et accédez au menu **Appareils**</span><span class="sxs-lookup"><span data-stu-id="89432-140">Sign in to [Microsoft Endpoint Manager](https://endpoint.microsoft.com/) and navigate to the **Devices** menu</span></span>
2. <span data-ttu-id="89432-141">Recherchez la section Bureau géré Microsoft, sélectionnez **Paramètres.**</span><span class="sxs-lookup"><span data-stu-id="89432-141">Look for the Microsoft Managed Desktop section, select **Settings**.</span></span>
3. <span data-ttu-id="89432-142">Dans **l’espace** de travail État du déploiement, sélectionnez le paramètre à revenir, puis sélectionnez le déploiement par étapes à inverser.</span><span class="sxs-lookup"><span data-stu-id="89432-142">In **Deployment status** workspace, select the setting you want to revert, and then select the staged deployment to revert.</span></span>
4. <span data-ttu-id="89432-143">Under **Need to revert this change?**, select **Revert deployment**.</span><span class="sxs-lookup"><span data-stu-id="89432-143">Under **Need to revert this change?**, select **Revert deployment**.</span></span>

<!-- Needs picture updated to show MEM ![Deployment status workspace. Browser start pages is selected, opening a pane on the right side with data about the submitted change and its status. At the bottom is the "need to revert this change" area where you can select "Revert deployment."](../../media/3revert.png) -->

## <a name="additional-resources"></a><span data-ttu-id="89432-144">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="89432-144">Additional resources</span></span>
- [<span data-ttu-id="89432-145">Vue d’ensemble des paramètres configurables</span><span class="sxs-lookup"><span data-stu-id="89432-145">Configurable settings overview</span></span>](config-setting-overview.md)
- [<span data-ttu-id="89432-146">Référence des paramètres configurables</span><span class="sxs-lookup"><span data-stu-id="89432-146">Configurable settings reference</span></span>](config-setting-ref.md) 
