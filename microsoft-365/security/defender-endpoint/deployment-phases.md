---
title: Phases de déploiement
description: Découvrez comment déployer Microsoft Defender pour endpoint en préparation, configuration et intégration de points de terminaison à ce service
keywords: déployer, préparer, configurer, intégrer, phase, déploiement, déploiement, adoption, configuration
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365solution-endpointprotect
- m365solution-overview
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 3f0527192a55d67df7e23507bed46df446f8b2b7
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51165164"
---
# <a name="deployment-phases"></a><span data-ttu-id="902a8-104">Phases de déploiement</span><span class="sxs-lookup"><span data-stu-id="902a8-104">Deployment phases</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="902a8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="902a8-105">**Applies to:**</span></span>
- [<span data-ttu-id="902a8-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="902a8-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="902a8-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="902a8-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="902a8-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="902a8-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="902a8-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="902a8-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="902a8-110">Découvrez comment déployer Microsoft Defender pour endpoint afin que votre entreprise puisse tirer parti de la protection préventive, de la détection post-violation, de l’examen automatisé et de la réponse.</span><span class="sxs-lookup"><span data-stu-id="902a8-110">Learn how to deploy Microsoft Defender for Endpoint so that your enterprise can take advantage of preventative protection, post-breach detection, automated investigation, and response.</span></span> 


<span data-ttu-id="902a8-111">Ce guide vous aide à travailler au sein des parties prenantes pour préparer votre environnement, puis intégrer les appareils d’une manière méthodique, en passant de l’évaluation à un projet pilote significatif vers un déploiement complet.</span><span class="sxs-lookup"><span data-stu-id="902a8-111">This guide helps you work across stakeholders to prepare your environment and then onboard devices in a methodical way, moving from evaluation, to a meaningful pilot, to full deployment.</span></span>

<span data-ttu-id="902a8-112">Chaque section correspond à un article distinct de cette solution.</span><span class="sxs-lookup"><span data-stu-id="902a8-112">Each section corresponds to a separate article in this solution.</span></span>

![Image des phases de déploiement avec les détails du tableau](images/deployment-guide-phases.png)


![Résumé des phases de déploiement : préparer, configurer, intégrer](images/phase-diagrams/deployment-phases.png)

|<span data-ttu-id="902a8-115">Phase</span><span class="sxs-lookup"><span data-stu-id="902a8-115">Phase</span></span> | <span data-ttu-id="902a8-116">Description</span><span class="sxs-lookup"><span data-stu-id="902a8-116">Description</span></span> | 
|:-------|:-----|
| [<span data-ttu-id="902a8-117">Phase 1 : préparation</span><span class="sxs-lookup"><span data-stu-id="902a8-117">Phase 1: Prepare</span></span>](prepare-deployment.md)| <span data-ttu-id="902a8-118">Découvrez ce que vous devez prendre en compte lors du déploiement de Defender for Endpoint, comme les approbations des parties prenantes, les considérations sur l’environnement, les autorisations d’accès et l’ordre d’adoption des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="902a8-118">Learn about what you need to consider when deploying Defender for Endpoint such as stakeholder approvals, environment considerations, access permissions, and adoption order of capabilities.</span></span> 
| [<span data-ttu-id="902a8-119">Phase 2 : configuration</span><span class="sxs-lookup"><span data-stu-id="902a8-119">Phase 2: Setup</span></span>](production-deployment.md)|  <span data-ttu-id="902a8-120">Obtenez des conseils sur les étapes initiales à suivre pour accéder au portail, telles que la validation des licences, l’exécution de l’Assistant Installation et la configuration réseau.</span><span class="sxs-lookup"><span data-stu-id="902a8-120">Get guidance on the initial steps you need to take so that you can access the portal such as validating licensing, completing the setup wizard, and network configuration.</span></span> 
| [<span data-ttu-id="902a8-121">Phase 3 : intégration</span><span class="sxs-lookup"><span data-stu-id="902a8-121">Phase 3: Onboard</span></span>](onboarding.md) | <span data-ttu-id="902a8-122">Découvrez comment utiliser les anneaux de déploiement, les outils d’intégration pris en charge en fonction du type de point de terminaison et la configuration des fonctionnalités disponibles.</span><span class="sxs-lookup"><span data-stu-id="902a8-122">Learn how to make use of deployment rings, supported onboarding tools based on the type of endpoint, and configuring available capabilities.</span></span> 


<span data-ttu-id="902a8-123">Une fois que vous aurez terminé ce guide, vous serez configuré avec les autorisations d’accès adéquates, vos points de terminaison seront intégrés et des données de capteur seront signalés au service, et des fonctionnalités telles que la protection nouvelle génération et la réduction de la surface d’attaque seront en place.</span><span class="sxs-lookup"><span data-stu-id="902a8-123">After you've completed this guide, you'll be setup with the right access permissions, your endpoints will be onboarded and reporting sensor data to the service, and capabilities such as next-generation protection and attack surface reduction will be in place.</span></span>



<span data-ttu-id="902a8-124">Quelle que soit l’architecture et la méthode [](deployment-strategy.md) de déploiement de l’environnement que vous choisissez décrites dans les instructions de déploiement de plan, ce guide va vous prendre en charge lors de l’intégration des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="902a8-124">Regardless of the environment architecture and method of deployment you choose outlined in the [Plan deployment](deployment-strategy.md) guidance, this guide is going to support you in onboarding endpoints.</span></span> 








## <a name="key-capabilities"></a><span data-ttu-id="902a8-125">Fonctionnalités clés</span><span class="sxs-lookup"><span data-stu-id="902a8-125">Key capabilities</span></span>

<span data-ttu-id="902a8-126">Bien que Microsoft Defender pour point de terminaison offre de nombreuses fonctionnalités, l’objectif principal de ce guide de déploiement est de vous aider à commencer par l’intégration d’appareils.</span><span class="sxs-lookup"><span data-stu-id="902a8-126">While Microsoft Defender for Endpoint provides many capabilities, the primary purpose of this deployment guide is to get you started by onboarding devices.</span></span> <span data-ttu-id="902a8-127">En plus de l’intégration, ces conseils vous guident avec les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="902a8-127">In addition to onboarding, this guidance gets you started with the following capabilities.</span></span>



<span data-ttu-id="902a8-128">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="902a8-128">Capability</span></span> | <span data-ttu-id="902a8-129">Description</span><span class="sxs-lookup"><span data-stu-id="902a8-129">Description</span></span> 
:---|:---
<span data-ttu-id="902a8-130">Détection et réponse du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="902a8-130">Endpoint detection and response</span></span> | <span data-ttu-id="902a8-131">Des fonctionnalités de détection et de réponse de point de terminaison sont mises en place pour détecter, examiner et répondre aux tentatives d’intrusion et aux violations actives.</span><span class="sxs-lookup"><span data-stu-id="902a8-131">Endpoint detection and response capabilities are put in place to detect, investigate, and respond to intrusion attempts and active breaches.</span></span>
<span data-ttu-id="902a8-132">Protection de nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="902a8-132">Next-generation protection</span></span> | <span data-ttu-id="902a8-133">Pour renforcer davantage le périmètre de sécurité de votre réseau, Microsoft Defender pour Endpoint utilise une protection nouvelle génération conçue pour capturer tous les types de menaces émergentes.</span><span class="sxs-lookup"><span data-stu-id="902a8-133">To further reinforce the security perimeter of your network, Microsoft Defender for Endpoint uses next-generation protection designed to catch all types of emerging threats.</span></span>
<span data-ttu-id="902a8-134">Réduction de la surface d'attaque</span><span class="sxs-lookup"><span data-stu-id="902a8-134">Attack surface reduction</span></span> |  <span data-ttu-id="902a8-135">Fournissez la première ligne de défense dans la pile.</span><span class="sxs-lookup"><span data-stu-id="902a8-135">Provide the first line of defense in the stack.</span></span> <span data-ttu-id="902a8-136">En veillant à ce que les paramètres de configuration soient correctement définies et que des techniques d’atténuation des attaques soient appliquées, ces fonctionnalités peuvent résister aux attaques et à l’exploitation.</span><span class="sxs-lookup"><span data-stu-id="902a8-136">By ensuring configuration settings are properly set and exploit mitigation techniques are applied, these set of capabilities resist attacks and exploitation.</span></span>

<span data-ttu-id="902a8-137">Toutes ces fonctionnalités sont disponibles pour les titulaires de licences Microsoft Defender pour les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="902a8-137">All these capabilities are available for Microsoft Defender for Endpoint license holders.</span></span> <span data-ttu-id="902a8-138">Pour plus d’informations, voir [Conditions requises pour les licences.](minimum-requirements.md#licensing-requirements)</span><span class="sxs-lookup"><span data-stu-id="902a8-138">For more information, see [Licensing requirements](minimum-requirements.md#licensing-requirements).</span></span>

## <a name="scope"></a><span data-ttu-id="902a8-139">Portée</span><span class="sxs-lookup"><span data-stu-id="902a8-139">Scope</span></span>

### <a name="in-scope"></a><span data-ttu-id="902a8-140">Dans l’étendue</span><span class="sxs-lookup"><span data-stu-id="902a8-140">In scope</span></span>

-   <span data-ttu-id="902a8-141">Utilisation de Microsoft Endpoint Manager et Microsoft Endpoint Manager pour intégrer des points de terminaison dans le service et configurer des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="902a8-141">Use of Microsoft Endpoint Manager and Microsoft Endpoint Manager to onboard endpoints into the service and configure capabilities</span></span>

-   <span data-ttu-id="902a8-142">Activation de Defender pour les fonctionnalités de protection évolutive des points de terminaison point de terminaison (PEPT)</span><span class="sxs-lookup"><span data-stu-id="902a8-142">Enabling Defender for Endpoint endpoint detection and response (EDR)  capabilities</span></span>

-   <span data-ttu-id="902a8-143">Activation des fonctionnalités DE LAS (Endpoint Endpoint Protection Platform) de Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="902a8-143">Enabling Defender for Endpoint endpoint protection platform (EPP) capabilities</span></span>

    -   <span data-ttu-id="902a8-144">Protection de nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="902a8-144">Next-generation protection</span></span>

    -   <span data-ttu-id="902a8-145">Réduction de la surface d'attaque</span><span class="sxs-lookup"><span data-stu-id="902a8-145">Attack surface reduction</span></span>


### <a name="out-of-scope"></a><span data-ttu-id="902a8-146">Non compris</span><span class="sxs-lookup"><span data-stu-id="902a8-146">Out of scope</span></span>

<span data-ttu-id="902a8-147">Ce guide de déploiement n’entre pas dans le cadre de ce guide de déploiement :</span><span class="sxs-lookup"><span data-stu-id="902a8-147">The following are out of scope of this deployment guide:</span></span>

-   <span data-ttu-id="902a8-148">Configuration de solutions tierces qui peuvent s’intégrer à Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="902a8-148">Configuration of third-party solutions that might integrate with Defender for Endpoint</span></span>

-   <span data-ttu-id="902a8-149">Test de pénétration dans un environnement de production</span><span class="sxs-lookup"><span data-stu-id="902a8-149">Penetration testing in production environment</span></span>




## <a name="see-also"></a><span data-ttu-id="902a8-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="902a8-150">See also</span></span>
- [<span data-ttu-id="902a8-151">Phase 1 : préparation</span><span class="sxs-lookup"><span data-stu-id="902a8-151">Phase 1: Prepare</span></span>](prepare-deployment.md)
- [<span data-ttu-id="902a8-152">Phase 2 : configuration</span><span class="sxs-lookup"><span data-stu-id="902a8-152">Phase 2: Set up</span></span>](production-deployment.md)
- [<span data-ttu-id="902a8-153">Phase 3 : intégration</span><span class="sxs-lookup"><span data-stu-id="902a8-153">Phase 3: Onboard</span></span>](onboarding.md)
- [<span data-ttu-id="902a8-154">Planifier le déploiement</span><span class="sxs-lookup"><span data-stu-id="902a8-154">Plan deployment</span></span>](deployment-strategy.md)