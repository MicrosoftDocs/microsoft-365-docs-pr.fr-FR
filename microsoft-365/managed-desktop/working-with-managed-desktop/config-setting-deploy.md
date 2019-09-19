---
title: Déployer des paramètres configurables dans le bureau géré Microsoft
description: Déployer et suivre les modifications de paramètres configurables dans le bureau géré Microsoft.
keywords: Microsoft Managed Desktop, Microsoft 365, service, documentation, Deploy, Staging Deployment, configurable Settings
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 5b6a2756514e94cb4f96141d6e7c9f6f2a6dd7ff
ms.sourcegitcommit: a4657a499967751d4c2dfc6cd1904258ab8be193
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/19/2019
ms.locfileid: "37040795"
---
# <a name="deploy-and-track-configurable-settings---microsoft-managed-desktop"></a><span data-ttu-id="64840-104">Déployer et suivre les paramètres configurables-bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="64840-104">Deploy and track configurable settings - Microsoft Managed Desktop</span></span>

<span data-ttu-id="64840-105">Une fois que vous avez apporté des modifications à vos catégories de paramètres et que vous déployez un déploiement, la page État du déploiement vous permet de commencer à déployer vos paramètres dans des groupes.</span><span class="sxs-lookup"><span data-stu-id="64840-105">After you make changes to your setting categories and stage a deployment, the Deployment status page allows you to begin deploying your settings to groups.</span></span> <span data-ttu-id="64840-106">Cette page affiche un résumé de chaque paramètre configurable.</span><span class="sxs-lookup"><span data-stu-id="64840-106">This page shows a summary of each configurable setting.</span></span> <span data-ttu-id="64840-107">En ouvrant une catégorie de paramètres, vous pouvez déployer des paramètres dans des groupes et suivre la progression de ces déploiements.</span><span class="sxs-lookup"><span data-stu-id="64840-107">By opening a setting category you can deploy settings to groups and track the progress of these deployments.</span></span>

## <a name="deployment-statuses"></a><span data-ttu-id="64840-108">Statuts de déploiement</span><span class="sxs-lookup"><span data-stu-id="64840-108">Deployment statuses</span></span> 

<span data-ttu-id="64840-109">Voici les statuts que vous verrez pour chaque déploiement.</span><span class="sxs-lookup"><span data-stu-id="64840-109">These are the statuses you’ll see for each deployment.</span></span>

<span data-ttu-id="64840-110">Statut</span><span class="sxs-lookup"><span data-stu-id="64840-110">Status</span></span>  | <span data-ttu-id="64840-111">Explication</span><span class="sxs-lookup"><span data-stu-id="64840-111">Explanation</span></span> 
--- | --- 
<span data-ttu-id="64840-112">Déployer</span><span class="sxs-lookup"><span data-stu-id="64840-112">Deploy</span></span> | <span data-ttu-id="64840-113">Votre modification attend d’être déployée sur ce groupe.</span><span class="sxs-lookup"><span data-stu-id="64840-113">Your change is waiting to be deployed to this group.</span></span>
<span data-ttu-id="64840-114">En cours</span><span class="sxs-lookup"><span data-stu-id="64840-114">In progress</span></span> | <span data-ttu-id="64840-115">La modification est appliquée aux appareils actifs de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="64840-115">The change is being applied to active devices in this group.</span></span> 
<span data-ttu-id="64840-116">Exécuter</span><span class="sxs-lookup"><span data-stu-id="64840-116">Complete</span></span> | <span data-ttu-id="64840-117">Modification effectuée sur tous les appareils actifs de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="64840-117">The change completed on all active devices in this group.</span></span> 
<span data-ttu-id="64840-118">Failed</span><span class="sxs-lookup"><span data-stu-id="64840-118">Failed</span></span> | <span data-ttu-id="64840-119">La modification a échoué sur 10% des appareils actifs dans le groupe, de sorte que le déploiement a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="64840-119">The change failed on a 10 percent of active devices in the group, so the deployment was stopped.</span></span><br><br> <span data-ttu-id="64840-120">Une demande de support sera automatiquement ouverte avec les opérations de bureau géré Microsoft pour résoudre les problèmes de déploiement.</span><span class="sxs-lookup"><span data-stu-id="64840-120">A support request will be automatically opened with Microsoft Managed Desktop operations to troubleshoot the deployment.</span></span> 
<span data-ttu-id="64840-121">Retrouveront</span><span class="sxs-lookup"><span data-stu-id="64840-121">Reverted</span></span> | <span data-ttu-id="64840-122">Le changement a été rétabli sur la dernière modification qui a été déployée avec succès sur tous les groupes de déploiement.</span><span class="sxs-lookup"><span data-stu-id="64840-122">The change was reverted to the last change that was successfully deployed to all deployment groups.</span></span>

## <a name="deploy-changes"></a><span data-ttu-id="64840-123">Déployer les modifications</span><span class="sxs-lookup"><span data-stu-id="64840-123">Deploy changes</span></span>

<span data-ttu-id="64840-124">Nous allons afficher l’image d’arrière-plan du bureau dans ces instructions.</span><span class="sxs-lookup"><span data-stu-id="64840-124">We’ll show Desktop background picture in these instructions.</span></span> <span data-ttu-id="64840-125">Une fois que vous avez déployé un déploiement, vous déployez les modifications à partir de la page État du déploiement.</span><span class="sxs-lookup"><span data-stu-id="64840-125">After you’ve staged a deployment, you deploy changes from the Deployment status page.</span></span> 

<span data-ttu-id="64840-126">**Pour déployer les modifications**</span><span class="sxs-lookup"><span data-stu-id="64840-126">**To deploy changes**</span></span>

1. <span data-ttu-id="64840-127">Se connecter au [portail d’administration de bureau géré Microsoft](http://aka.ms/mwaasportal)</span><span class="sxs-lookup"><span data-stu-id="64840-127">Sign in to [Microsoft Managed Desktop Admin portal](http://aka.ms/mwaasportal)</span></span>
2. <span data-ttu-id="64840-128">Sous **paramètres**, sélectionnez **configurable**.</span><span class="sxs-lookup"><span data-stu-id="64840-128">Under **Settings**, select **Configurable**.</span></span>
3. <span data-ttu-id="64840-129">Dans l’espace de travail **État de déploiement** , sélectionnez le paramètre que vous souhaitez déployer, puis sélectionnez le déploiement intermédiaire à déployer.</span><span class="sxs-lookup"><span data-stu-id="64840-129">In **Deployment status** workspace, select the setting you want to deploy, and then select the staged deployment to deploy.</span></span>
4. <span data-ttu-id="64840-130">Sélectionnez **déployer** pour déployer la modification dans l’un des groupes de déploiement.</span><span class="sxs-lookup"><span data-stu-id="64840-130">Select **Deploy** to deploy the change to one of the deployment groups.</span></span>

<span data-ttu-id="64840-131">![Vue d’ensemble](images/1deployedit.png) de l’état de déploiement des paramètres configurables Microsoft Managed Desktop recommande le déploiement aux groupes de déploiement dans cet ordre : test, First, Fast, puis large.</span><span class="sxs-lookup"><span data-stu-id="64840-131">![Configurable settings deployment status overview](images/1deployedit.png) Microsoft Managed Desktop recommends deploying to deployment groups in this order: Test, First, Fast, and then Broad.</span></span> 

<span data-ttu-id="64840-132">Lorsque les modifications sont terminées dans chaque groupe, l’État devient **terminé**.</span><span class="sxs-lookup"><span data-stu-id="64840-132">When changes complete in each group, the status changes to **Complete**.</span></span>

![Déploiement des paramètres configurables terminé](images/2completeedit.png)

## <a name="revert-deployment"></a><span data-ttu-id="64840-134">Rétablir le déploiement</span><span class="sxs-lookup"><span data-stu-id="64840-134">Revert deployment</span></span>

<span data-ttu-id="64840-135">Une fois que vous avez déployé une modification, vous pouvez revenir à l' **État de déploiement**.</span><span class="sxs-lookup"><span data-stu-id="64840-135">After you’ve deployed a change, you can revert from **Deployment status**.</span></span> <span data-ttu-id="64840-136">Lorsque vous rétablissez une modification qui est **en cours** ou **terminée**, le déploiement actuel s’arrête.</span><span class="sxs-lookup"><span data-stu-id="64840-136">When you revert a change that is **In progress** or **Complete**, the current deployment stops.</span></span> <span data-ttu-id="64840-137">Le paramètre reprendra la dernière version qui a été déployée sur tous les groupes.</span><span class="sxs-lookup"><span data-stu-id="64840-137">The setting will revert to the last version that was deployed to all groups.</span></span> 

<span data-ttu-id="64840-138">Nous allons vous montrer les étapes permettant de rétablir une modification à l’aide de l’image d’arrière-plan du Bureau à titre d’exemple.</span><span class="sxs-lookup"><span data-stu-id="64840-138">We’ll show the steps to revert a change using the Desktop background picture as an example.</span></span> 

<span data-ttu-id="64840-139">**Pour annuler une modification**</span><span class="sxs-lookup"><span data-stu-id="64840-139">**To revert a change**</span></span>
1. <span data-ttu-id="64840-140">Se connecter au [portail d’administration de bureau géré Microsoft](http://aka.ms/mwaasportal)</span><span class="sxs-lookup"><span data-stu-id="64840-140">Sign in to [Microsoft Managed Desktop Admin portal](http://aka.ms/mwaasportal)</span></span>
2. <span data-ttu-id="64840-141">Sous **paramètres**, sélectionnez **configurable**.</span><span class="sxs-lookup"><span data-stu-id="64840-141">Under **Settings**, select **Configurable**.</span></span>
3. <span data-ttu-id="64840-142">Dans l’espace de travail **État de déploiement** , sélectionnez le paramètre que vous souhaitez rétablir, puis sélectionnez le déploiement intermédiaire à rétablir.</span><span class="sxs-lookup"><span data-stu-id="64840-142">In **Deployment status** workspace, select the setting you want to revert, and then select the staged deployment to revert.</span></span>
4. <span data-ttu-id="64840-143">Sous **nécessité de rétablir cette modification**, sélectionnez **rétablir le déploiement**.</span><span class="sxs-lookup"><span data-stu-id="64840-143">Under **Need to revert this change**, select **Revert deployment**.</span></span>

![Rétablissement du déploiement des paramètres configurables](images/3revert.png) 

## <a name="additional-resources"></a><span data-ttu-id="64840-145">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="64840-145">Additional resources</span></span>
- [<span data-ttu-id="64840-146">Vue d’ensemble des paramètres configurables</span><span class="sxs-lookup"><span data-stu-id="64840-146">Configurable settings overview</span></span>](config-setting-overview.md)
- [<span data-ttu-id="64840-147">Référence des paramètres configurables</span><span class="sxs-lookup"><span data-stu-id="64840-147">Configurable settings reference</span></span>](config-setting-ref.md) 
