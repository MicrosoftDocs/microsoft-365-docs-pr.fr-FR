---
title: Déployer des paramètres configurables dans le bureau géré Microsoft
description: Déployer et suivre les modifications de paramètres configurables dans le bureau géré Microsoft.
keywords: Microsoft maNaged Desktop, Microsoft 365, service, documentation, Deploy, Staging Deployment, configurable Settings
ms.service: m365-md
author: trudyha
ms.localizationpriority: normal
ms.date: 2/17/2019
ms.collection: M365-modern-desktop
ms.openlocfilehash: 62a17c95f5dc6b11f446a27684c507d7aaa95b7b
ms.sourcegitcommit: 8d2e6bcc257a665f53ee914c7f0e1dfb9d31a9e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30414166"
---
# <a name="deploy-and-track-configurable-settings---microsoft-managed-desktop"></a><span data-ttu-id="0298c-104">Déployer et suivre les paramètres configurables-bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="0298c-104">Deploy and track configurable settings - Microsoft Managed Desktop</span></span>

<span data-ttu-id="0298c-105">Après avoir apporté des modifications à vos catégories de paramètres et à déployer un déploiement, vous pouvez déployer et suivre la progression du déploiement sur l'état du déploiement.</span><span class="sxs-lookup"><span data-stu-id="0298c-105">After you make changes to your setting categories and stage a deployment, you can deploy and track progress for the deployment on Deployment status.</span></span> <span data-ttu-id="0298c-106">Cette page affiche un résumé de chaque paramètre configurable.</span><span class="sxs-lookup"><span data-stu-id="0298c-106">This page shows a summary of each configurable setting.</span></span> <span data-ttu-id="0298c-107">Ouvrez une catégorie de paramètres pour afficher chaque déploiement et ses détails, afin de déployer les modifications.</span><span class="sxs-lookup"><span data-stu-id="0298c-107">Open a setting category to see each deployment and their details, to deploy the changes.</span></span> 

## <a name="deployment-statuses"></a><span data-ttu-id="0298c-108">Statuts de déploiement</span><span class="sxs-lookup"><span data-stu-id="0298c-108">Deployment statuses</span></span> 

<span data-ttu-id="0298c-109">Voici les statues que vous verrez pour chaque déploiement.</span><span class="sxs-lookup"><span data-stu-id="0298c-109">These are the statues you’ll see for each deployment.</span></span>

<span data-ttu-id="0298c-110">Status</span><span class="sxs-lookup"><span data-stu-id="0298c-110">Status</span></span>  | <span data-ttu-id="0298c-111">Explication</span><span class="sxs-lookup"><span data-stu-id="0298c-111">Explanation</span></span> 
--- | --- 
<span data-ttu-id="0298c-112">Déployer</span><span class="sxs-lookup"><span data-stu-id="0298c-112">Deploy</span></span> | <span data-ttu-id="0298c-113">Votre modification attend d'être déployée sur cette sonnerie.</span><span class="sxs-lookup"><span data-stu-id="0298c-113">Your change is waiting to be deployed to this ring.</span></span>
<span data-ttu-id="0298c-114">En cours</span><span class="sxs-lookup"><span data-stu-id="0298c-114">In progress</span></span> | <span data-ttu-id="0298c-115">La modification est appliquée aux appareils actifs dans cette sonnerie.</span><span class="sxs-lookup"><span data-stu-id="0298c-115">The change is being applied to active devices in this ring.</span></span> 
<span data-ttu-id="0298c-116">Exécuter</span><span class="sxs-lookup"><span data-stu-id="0298c-116">Complete</span></span> | <span data-ttu-id="0298c-117">Modification effectuée sur tous les périphériques actifs de cette sonnerie.</span><span class="sxs-lookup"><span data-stu-id="0298c-117">The change completed on all active devices in this ring.</span></span> 
<span data-ttu-id="0298c-118">Failed</span><span class="sxs-lookup"><span data-stu-id="0298c-118">Failed</span></span> | <span data-ttu-id="0298c-119">La modification a échoué sur 10% des appareils actifs dans l'anneau, de sorte que le déploiement a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="0298c-119">The change failed on a 10 percent of active devices in the ring, so the deployment was stopped.</span></span><br><br> <span data-ttu-id="0298c-120">Une demande de support sera automatiquement ouverte avec les opérations de bureau géré Microsoft pour résoudre les problèmes de déploiement.</span><span class="sxs-lookup"><span data-stu-id="0298c-120">A support request will be automatically opened with Microsoft Managed Desktop operations to troubleshoot the deployment.</span></span> 
<span data-ttu-id="0298c-121">Retrouveront</span><span class="sxs-lookup"><span data-stu-id="0298c-121">Reverted</span></span> | <span data-ttu-id="0298c-122">La modification a été rétablie à la dernière modification qui a été correctement déployée sur toutes les sonneries de déploiement.</span><span class="sxs-lookup"><span data-stu-id="0298c-122">The change was reverted to the last change that was successfully deployed to all deployment rings.</span></span>

## <a name="deploy-changes"></a><span data-ttu-id="0298c-123">Déployer les modifications</span><span class="sxs-lookup"><span data-stu-id="0298c-123">Deploy changes</span></span>

<span data-ttu-id="0298c-124">Nous allons afficher l'image d'arrière-plan du bureau dans ces instructions.</span><span class="sxs-lookup"><span data-stu-id="0298c-124">We’ll show Desktop background picture in these instructions.</span></span> <span data-ttu-id="0298c-125">Une fois que vous avez déployé un déploiement, vous déployez les modifications à partir de l'état du déploiement.</span><span class="sxs-lookup"><span data-stu-id="0298c-125">After you’ve staged a deployment, you deploy changes from Deployment status.</span></span> 

<span data-ttu-id="0298c-126">**Pour déployer les modifications**</span><span class="sxs-lookup"><span data-stu-id="0298c-126">**To deploy changes**</span></span>

1. <span data-ttu-id="0298c-127">Se connecter au [portail d'administration de bureau géré Microsoft](http://aka.ms/mwaasportal)</span><span class="sxs-lookup"><span data-stu-id="0298c-127">Sign in to [Microsoft Managed Desktop Admin portal](http://aka.ms/mwaasportal)</span></span>
2. <span data-ttu-id="0298c-128">Sous **paramètres**, sélectionnez **configurable**.</span><span class="sxs-lookup"><span data-stu-id="0298c-128">Under **Settings**, select **Configurable**.</span></span>
3. <span data-ttu-id="0298c-129">Dans l'espace de travail **État de déploiement** , sélectionnez le paramètre que vous souhaitez déployer, puis sélectionnez le déploiement intermédiaire à déployer.</span><span class="sxs-lookup"><span data-stu-id="0298c-129">In **Deployment status** workspace, select the setting you want to deploy, and then select the staged deployment to deploy.</span></span>
4. <span data-ttu-id="0298c-130">Sélectionnez **déployer** pour déployer la modification vers l'une des sonneries de déploiement.</span><span class="sxs-lookup"><span data-stu-id="0298c-130">Select **Deploy** to deploy the change to one of the deployment rings.</span></span>

![Vue d'ensemble du statut de déploiement des paramètres configurables](images/deploy-cs-overview.png)

<span data-ttu-id="0298c-132">Microsoft maNaged Desktop recommande le déploiement aux sonneries de déploiement dans cet ordre: test, First, Fast, puis large.</span><span class="sxs-lookup"><span data-stu-id="0298c-132">Microsoft Managed Desktop recommends deploying to deployment rings in this order: Test, First, Fast, and then Broad.</span></span> 

<span data-ttu-id="0298c-133">Lorsque les modifications sont terminées dans chaque sonnerie, l'État devient **terminé**.</span><span class="sxs-lookup"><span data-stu-id="0298c-133">When changes complete in each ring, the status changes to **Complete**.</span></span>

![Déploiement des paramètres configurables terminé](images/config-setting-complete.png)

## <a name="revert-deployment"></a><span data-ttu-id="0298c-135">Rétablir le déploiement</span><span class="sxs-lookup"><span data-stu-id="0298c-135">Revert deployment</span></span>

<span data-ttu-id="0298c-136">Nous allons afficher l'image d'arrière-plan du bureau dans ces instructions.</span><span class="sxs-lookup"><span data-stu-id="0298c-136">We’ll show Desktop background picture in these instructions.</span></span> 

<span data-ttu-id="0298c-137">Une fois que vous avez déployé une modification, vous pouvez revenir à l' **État de déploiement**.</span><span class="sxs-lookup"><span data-stu-id="0298c-137">After you’ve deployed a change, you can revert from **Deployment status**.</span></span> <span data-ttu-id="0298c-138">Lorsque vous rétablissez une modification qui est **en cours** ou **terminée**, le déploiement actuel s'arrête.</span><span class="sxs-lookup"><span data-stu-id="0298c-138">When you revert a change that is **In progress** or **Complete**, the current deployment stops.</span></span> <span data-ttu-id="0298c-139">Le paramètre reprendra la dernière version qui a été déployée sur toutes les sonneries.</span><span class="sxs-lookup"><span data-stu-id="0298c-139">The setting will revert to the last version that was deployed to all rings.</span></span> 

<span data-ttu-id="0298c-140">**Pour annuler une modification**</span><span class="sxs-lookup"><span data-stu-id="0298c-140">**To revert a change**</span></span>
1. <span data-ttu-id="0298c-141">Se connecter au [portail d'administration de bureau géré Microsoft](http://aka.ms/mwaasportal)</span><span class="sxs-lookup"><span data-stu-id="0298c-141">Sign in to [Microsoft Managed Desktop Admin portal](http://aka.ms/mwaasportal)</span></span>
2. <span data-ttu-id="0298c-142">Sous **paramètres**, sélectionnez **configurable**.</span><span class="sxs-lookup"><span data-stu-id="0298c-142">Under **Settings**, select **Configurable**.</span></span>
3. <span data-ttu-id="0298c-143">Dans l'espace de travail **État de déploiement** , sélectionnez le paramètre que vous souhaitez rétablir, puis sélectionnez le déploiement intermédiaire à rétablir.</span><span class="sxs-lookup"><span data-stu-id="0298c-143">In **Deployment status** workspace, select the setting you want to revert, and then select the staged deployment to revert.</span></span>
4. <span data-ttu-id="0298c-144">Sous **nécessité de rétablir cette modification**, sélectionnez **rétablir le déploiement**.</span><span class="sxs-lookup"><span data-stu-id="0298c-144">Under **Need to revert this change**, select **Revert deployment**.</span></span>

![Rétablissement du déploiement des paramètres configurables](images/config-setting-revert.png) 

## <a name="additional-resources"></a><span data-ttu-id="0298c-146">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="0298c-146">Additional resources</span></span>
- [<span data-ttu-id="0298c-147">Vue d'ensemble des paramètres configurables</span><span class="sxs-lookup"><span data-stu-id="0298c-147">Configurable settings overview</span></span>](config-setting-overview.md)
- [<span data-ttu-id="0298c-148">Référence des paramètres configurables</span><span class="sxs-lookup"><span data-stu-id="0298c-148">Configurable settings reference</span></span>](config-setting-ref.md) 