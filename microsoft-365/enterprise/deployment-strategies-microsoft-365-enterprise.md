---
title: Stratégies de déploiement de l’infrastructure de base de Microsoft 365 pour entreprise
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
ms.author: josephd
manager: laurawi
ms.date: 09/24/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Découvrez le déploiement des phases de l’infrastructure de base de Microsoft 365 pour entreprise.
ms.openlocfilehash: 765bba743485c13c65cd6377abe01f80f2df4c23
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42067796"
---
# <a name="microsoft-365-for-enterprise-foundation-infrastructure-deployment-strategies"></a><span data-ttu-id="4ee95-103">Stratégies de déploiement de l’infrastructure de base de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="4ee95-103">Microsoft 365 for enterprise foundation infrastructure deployment strategies</span></span>

<span data-ttu-id="4ee95-p101">Il existe plusieurs façons de déployer les phases de l’[infrastructure de base](deploy-foundation-infrastructure.md) de Microsoft 365 pour entreprise et de proposer ses fonctionnalités, logiciels et services à vos utilisateurs. Pour vous aider dans cette tâche, qui peut être vaste et complexe selon la taille de votre organisation et de son infrastructure existante, tenez compte des stratégies de déploiement suivantes :</span><span class="sxs-lookup"><span data-stu-id="4ee95-p101">There are many ways you can deploy the phases of the [foundation infrastructure](deploy-foundation-infrastructure.md) of Microsoft 365 for enterprise and roll out its capabilities, software, and services to your users. To get you started on the project management of this undertaking, which can be large and complex depending on the size of your organization and its existing infrastructure, consider the following deployment strategies:</span></span>

- <span data-ttu-id="4ee95-106">Déploiement en série</span><span class="sxs-lookup"><span data-stu-id="4ee95-106">Serial deployment</span></span>
- <span data-ttu-id="4ee95-107">Déploiement parallèle avec un lancement utilisateur décalé</span><span class="sxs-lookup"><span data-stu-id="4ee95-107">Parallel deployment with non-overlapping user rollout</span></span>
- <span data-ttu-id="4ee95-108">Déploiement parallèle avec un lancement utilisateur concomitant</span><span class="sxs-lookup"><span data-stu-id="4ee95-108">Parallel deployment with overlapping user rollout</span></span>
- <span data-ttu-id="4ee95-109">Infrastructure initiale et lancement de la configuration de bout en bout</span><span class="sxs-lookup"><span data-stu-id="4ee95-109">Up-front infrastructure and rollout of the end-to-end configuration</span></span>

<span data-ttu-id="4ee95-110">Utilisez ces stratégies pour obtenir des idées sur la gestion du projet global et découvrir plus rapidement les avantages de Microsoft 365 pour entreprise.</span><span class="sxs-lookup"><span data-stu-id="4ee95-110">Use these strategies for ideas on how to manage the overall project and more quickly realize the business benefits of Microsoft 365 for enterprise.</span></span>

>[!Note]
><span data-ttu-id="4ee95-p102">Cet article contient des suppositions et des simplifications dans le but de décrire de façon cohérente les stratégies de déploiement. Ces stratégies de déploiement sont considérées dans leur ensemble et n’impliquent en aucun cas l’existence de délais spécifiques. Elles ne sont pas non plus destinées à être appliquées à toutes les organisations et situations.</span><span class="sxs-lookup"><span data-stu-id="4ee95-p102">This article contains assumptions and simplifications for a consistent way to describe the deployment strategies. These deployment strategies are generalized and are not meant to imply any specific timeframes, nor are they meant to apply to all organizations and situations.</span></span>
>

## <a name="elements-of-it-project-management-for-typical-enterprise-organizations"></a><span data-ttu-id="4ee95-113">Éléments de gestion de projets informatiques pour les entreprises standard</span><span class="sxs-lookup"><span data-stu-id="4ee95-113">Elements of IT project management for typical enterprise organizations</span></span>

<span data-ttu-id="4ee95-p103">L’infrastructure informatique inclut des services principaux et le lancement de fonctionnalités inédites ou améliorées ou de logiciels installés à destination des utilisateurs finaux. Les départements informatiques déploient généralement les éléments d’une infrastructure informatique de façon méthodique. Pour réussir le déploiement d’un élément de l’infrastructure informatique, il vous faut :</span><span class="sxs-lookup"><span data-stu-id="4ee95-p103">IT infrastructure includes both backend services and the rollout of new or improved capabilities or installed software to end users. IT departments typically deploy elements of an IT infrastructure in a methodical way. One approach to the successful deployment of an element of IT infrastructure consists of:</span></span>

- <span data-ttu-id="4ee95-117">Un lancement pilote</span><span class="sxs-lookup"><span data-stu-id="4ee95-117">A pilot rollout</span></span> 

  <span data-ttu-id="4ee95-118">Comprend la configuration de l’infrastructure initiale et le lancement à destination d’un groupe pilote d’utilisateurs, les tests et les modifications ultérieures de la configuration de l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="4ee95-118">This includes initial infrastructure configuration and rollout to a pilot set of users, testing, and subsequent modifications to the infrastructure configuration.</span></span>

- <span data-ttu-id="4ee95-119">Un lancement utilisateur</span><span class="sxs-lookup"><span data-stu-id="4ee95-119">A user rollout</span></span>

  <span data-ttu-id="4ee95-120">Comprend le lancement destiné au reste de votre organisation par région, département, groupe ou tout autre méthode systématique de propagation de la configuration ou des logiciels.</span><span class="sxs-lookup"><span data-stu-id="4ee95-120">This includes the rollout to the rest of your organization based on regions, departments, groups, or other types of systematic propagation of configuration or software.</span></span>

<span data-ttu-id="4ee95-121">Le lancement pilote et le lancement utilisateur ne s’adressent pas aux mêmes utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4ee95-121">The set of users in the pilot rollout are not the same as those in the user rollout.</span></span>

<span data-ttu-id="4ee95-122">Voici comment ces deux lancements sont représentés dans cet article :</span><span class="sxs-lookup"><span data-stu-id="4ee95-122">This article uses the following graphics to depict these definitions:</span></span> 

![graphiques décrivant les définitions des déploiements pilote et utilisateur](../media/deployment-strategies-microsoft-365-enterprise/definitions.png) 

<span data-ttu-id="4ee95-124">Le dégradé utilisé pour illustrer le lancement utilisateur représente le pourcentage de 0 % à 100 % au sein de votre organisation, qui est réalisé de façon méthodique ou structurée par groupe, département ou région.</span><span class="sxs-lookup"><span data-stu-id="4ee95-124">The shading for the user rollout graphic indicates the percentage across your organization from 0% to 100% using a structured or methodical approach such as groups, departments, or regions.</span></span>

## <a name="deployment-strategies"></a><span data-ttu-id="4ee95-125">Stratégies de déploiement</span><span class="sxs-lookup"><span data-stu-id="4ee95-125">Deployment strategies</span></span>

<span data-ttu-id="4ee95-126">Voici les stratégies de déploiement que vous pouvez utiliser :</span><span class="sxs-lookup"><span data-stu-id="4ee95-126">Consider the following deployment strategies:</span></span>

- <span data-ttu-id="4ee95-127">Déploiement en série</span><span class="sxs-lookup"><span data-stu-id="4ee95-127">Serial deployment</span></span>
- <span data-ttu-id="4ee95-128">Déploiement parallèle avec un lancement utilisateur décalé</span><span class="sxs-lookup"><span data-stu-id="4ee95-128">Parallel deployment with non-overlapping user rollout</span></span>
- <span data-ttu-id="4ee95-129">Déploiement parallèle avec un lancement utilisateur concomitant</span><span class="sxs-lookup"><span data-stu-id="4ee95-129">Parallel deployment with overlapping user rollout</span></span>
- <span data-ttu-id="4ee95-130">Infrastructure initiale et lancement de la configuration de bout en bout</span><span class="sxs-lookup"><span data-stu-id="4ee95-130">Up-front infrastructure and rollout of the end-to-end configuration</span></span>

### <a name="serial-deployment"></a><span data-ttu-id="4ee95-131">Déploiement en série</span><span class="sxs-lookup"><span data-stu-id="4ee95-131">Serial deployment</span></span>

<span data-ttu-id="4ee95-p104">Un déploiement en série vous permet de lancer une phase dans son intégralité auprès de l’ensemble de vos utilisateurs, avant de passer à la suivante. Vous pouvez recourir à cette stratégie de déploiement pour différentes raisons, notamment dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="4ee95-p104">With a serial deployment, you completely roll out a phase, allowing the phase to reach 100% completion of deployment to all of your users, before moving on to the next one. Here are some of the reasons why you might deploy this way:</span></span>

- <span data-ttu-id="4ee95-134">Atténuation des risques</span><span class="sxs-lookup"><span data-stu-id="4ee95-134">Risk mitigation</span></span>
- <span data-ttu-id="4ee95-135">Ressources insuffisantes</span><span class="sxs-lookup"><span data-stu-id="4ee95-135">Resourcing constraints</span></span>
- <span data-ttu-id="4ee95-136">Cycles de financement du département informatique</span><span class="sxs-lookup"><span data-stu-id="4ee95-136">IT department funding cycles</span></span>
- <span data-ttu-id="4ee95-137">Dépendances de la technologie informatique</span><span class="sxs-lookup"><span data-stu-id="4ee95-137">IT technology dependencies</span></span>
- <span data-ttu-id="4ee95-138">Gestion des changements opérationnels et résistance des utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="4ee95-138">Business change management and end-user resistance</span></span>

<span data-ttu-id="4ee95-139">Ce diagramme de Gantt illustre un déploiement en série simplifié des phases 2 à 6 de l’infrastructure de base de Microsoft 365 pour entreprise.</span><span class="sxs-lookup"><span data-stu-id="4ee95-139">This Gantt chart shows a simplified serial deployment of phases 2-6 of the foundation infrastructure for Microsoft 365 for enterprise.</span></span>

![Déploiement en série des phases 2 à 6 de l’infrastructure de base](../media/deployment-strategies-microsoft-365-enterprise/serial.png) 
 
<span data-ttu-id="4ee95-141">Pour simplifier notre exposé, nous partons du principe que les phases et les segments de déploiement au sein de chaque phase ont la même durée.</span><span class="sxs-lookup"><span data-stu-id="4ee95-141">To simplify the discussion and example, each phase and deployment segment within each phase are assumed to take the same amount of time.</span></span>

>[!Note]
><span data-ttu-id="4ee95-p105">La Phase 1 : Mise en réseau de l’infrastructure de base de Microsoft 365 pour entreprise concerne uniquement le département informatique. Les utilisateurs profitent des avantages d’une meilleure connexion aux ressources cloud de Microsoft, mais ils ne sont pas obligés de la réaliser.</span><span class="sxs-lookup"><span data-stu-id="4ee95-p105">Phase 1: Networking of the Microsoft 365 for enterprise Foundation Infrastructure is an IT department-only phase. Users reap the benefits of optimized connectivity to Microsoft’s cloud resources but are not imposed upon to achieve it.</span></span>
>

<span data-ttu-id="4ee95-144">Voici une expérience utilisateur pilote simplifiée à titre d’exemple :</span><span class="sxs-lookup"><span data-stu-id="4ee95-144">Here’s a simplified pilot user experience as an example:</span></span>

- <span data-ttu-id="4ee95-p106">En décembre, je dois utiliser mon smartphone pour l’authentification multifacteur. (Identity)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p106">In December, I need to use my smart phone for MFA. (Identity)</span></span>
- <span data-ttu-id="4ee95-p107">En mars, Windows 10 Entreprise est installé sur mon ordinateur de bureau Windows 8.1. (Windows 10 Entreprise)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p107">In March, I get Windows 10 Enterprise installed on my Windows 8.1 desktop. (Windows 10 Enterprise)</span></span>
- <span data-ttu-id="4ee95-p108">En juin, Office 365 ProPlus est installé à la place d’Office 2013. (Office 365 ProPlus)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p108">In June, I get Office 365 ProPlus installed, replacing Office 2013. (Office 365 ProPlus)</span></span>
- <span data-ttu-id="4ee95-151">En septembre, j’obtiens l’inscription des appareils. D’autre part, les stratégies des applications et des appareils entrent en vigueur.</span><span class="sxs-lookup"><span data-stu-id="4ee95-151">In September, I get device enrollment and app and device policies applied.</span></span> <span data-ttu-id="4ee95-152">(Gestion des appareils mobiles)</span><span class="sxs-lookup"><span data-stu-id="4ee95-152">(Mobile device management)</span></span>
- <span data-ttu-id="4ee95-p110">En décembre, le client Azure Information Protection est installé et je reçois une formation pour savoir comment appliquer des étiquettes aux documents. (Information Protection)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p110">In December, I get the Azure Information Protection client installed and get trained on how to apply labels to documents. (Information protection)</span></span>

<span data-ttu-id="4ee95-155">Conclusion : vos lancements pilotes successifs sont espacés de 90 jours.</span><span class="sxs-lookup"><span data-stu-id="4ee95-155">The result is a 90-day cadence between successive pilot rollouts.</span></span>

<span data-ttu-id="4ee95-156">Voici une expérience d’utilisateur final simplifiée à titre d’exemple :</span><span class="sxs-lookup"><span data-stu-id="4ee95-156">Here’s a simplified end-user experience as an example:</span></span>

- <span data-ttu-id="4ee95-p111">En janvier, je dois utiliser mon smartphone pour l’authentification multifacteur. (Identity)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p111">In January, I need to use my smart phone for MFA. (Identity)</span></span>
- <span data-ttu-id="4ee95-p112">En avril, Windows 10 Entreprise est installé sur mon ordinateur de bureau Windows 8.1. (Windows 10 Entreprise)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p112">In April, I get Windows 10 Enterprise installed on my Windows 8.1 desktop. (Windows 10 Enterprise)</span></span>
- <span data-ttu-id="4ee95-p113">En juillet, Office 365 ProPlus est installé à la place d’Office 2013. (Office 365 ProPlus)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p113">In July, I get Office 365 ProPlus installed, replacing Office 2013. (Office 365 ProPlus)</span></span>
- <span data-ttu-id="4ee95-163">En octobre, j’obtiens l’inscription des appareils. D’autre part, les stratégies des applications et des appareils entrent en vigueur.</span><span class="sxs-lookup"><span data-stu-id="4ee95-163">In October, I get device enrollment and app and device policies applied.</span></span> <span data-ttu-id="4ee95-164">(Gestion des appareils mobiles)</span><span class="sxs-lookup"><span data-stu-id="4ee95-164">(Mobile device management)</span></span>
- <span data-ttu-id="4ee95-p115">En janvier de l’année suivante, le client Azure Information Protection est installé et je reçois une formation pour savoir comment appliquer des étiquettes aux documents. (Information Protection)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p115">In January of the following year, I get the Azure Information Protection client installed and get trained on how to apply labels to documents. (Information protection)</span></span>

<span data-ttu-id="4ee95-167">Conclusion : vos lancements utilisateurs successifs sont espacés de 90 jours.</span><span class="sxs-lookup"><span data-stu-id="4ee95-167">The result is a 90-day cadence between successive user rollouts.</span></span>

<span data-ttu-id="4ee95-168">L’inconvénient de cette stratégie de déploiement est que le déploiement de l’infrastructure de base de Microsoft 365 pour entreprise peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="4ee95-168">The disadvantage to this deployment strategy is that it can take a long time to fully deploy the Microsoft 365 for enterprise foundation infrastructure.</span></span>

### <a name="parallel-deployment-with-non-overlapping-user-rollout-parallel-1"></a><span data-ttu-id="4ee95-169">Déploiement parallèle avec un lancement utilisateur décalé (Parallèle 1)</span><span class="sxs-lookup"><span data-stu-id="4ee95-169">Parallel deployment with non-overlapping user rollout (Parallel 1)</span></span>

<span data-ttu-id="4ee95-p116">Avec cette stratégie de déploiement, le lancement pilote de la phase d’après a lieu quand le lancement utilisateur de la phase en cours se termine. Vous trouverez dans le graphique ci-dessous le déroulé des phases 2 à 6.</span><span class="sxs-lookup"><span data-stu-id="4ee95-p116">For this deployment strategy, you start the pilot rollout of the next phase during the last part of the user rollout of the current phase. Here is the deployment of phases 2-6 when the pilot rollout occurs as the user rollout of the previous phase is wrapping up.</span></span>

![Déploiement parallèle des phases 2 à 6 avec un lancement utilisateur décalé](../media/deployment-strategies-microsoft-365-enterprise/parallel1.png) 
 
<span data-ttu-id="4ee95-p117">Résultat : le lancement utilisateur pour la phase en cours se termine dans l’ensemble de votre organisation avant que la phase suivante commence. Les utilisateurs qui ne sont pas concernés par les lancements pilotes n’ont pas affaire aux lancement de plusieurs phases en même temps, mais vos lancements pilotes se terminent en parallèle des lancements utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4ee95-p117">The end result is that user rollout for the current phase completes across your organization before the next one starts. Users that are not in pilot rollouts are not dealing with the rollouts of multiple phases at the same time, but pilot rollouts are done in parallel with user rollouts.</span></span>

<span data-ttu-id="4ee95-175">Voici une expérience utilisateur pilote simplifiée à titre d’exemple :</span><span class="sxs-lookup"><span data-stu-id="4ee95-175">Here’s a simplified pilot user experience as an example:</span></span>

- <span data-ttu-id="4ee95-p118">En décembre, je dois utiliser mon smartphone pour l’authentification multifacteur. (Identity)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p118">In December, I need to use my smart phone for MFA. (Identity)</span></span>
- <span data-ttu-id="4ee95-p119">En février, Windows 10 Entreprise est installé sur mon ordinateur de bureau Windows 8.1. (Windows 10 Entreprise)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p119">In February, I get Windows 10 Enterprise installed on my Windows 8.1 desktop. (Windows 10 Enterprise)</span></span>
- <span data-ttu-id="4ee95-p120">En avril, Office 365 ProPlus est installé à la place d’Office 2013. (Office 365 ProPlus)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p120">In April, I get Office 365 ProPlus installed, replacing Office 2013. (Office 365 ProPlus)</span></span>
- <span data-ttu-id="4ee95-182">En juin, j’obtiens l’inscription des appareils. D’autre part, les stratégies des applications et des appareils entrent en vigueur.</span><span class="sxs-lookup"><span data-stu-id="4ee95-182">In June, I get device enrollment and app and device policies applied.</span></span> <span data-ttu-id="4ee95-183">(Gestion des appareils mobiles)</span><span class="sxs-lookup"><span data-stu-id="4ee95-183">(Mobile device management)</span></span>
- <span data-ttu-id="4ee95-p122">En août, le client Azure Information Protection est installé et je reçois une formation pour savoir comment appliquer des étiquettes aux documents. (Information Protection)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p122">In August, I get the Azure Information Protection client installed and get trained on how to apply labels to documents. (Information protection)</span></span>

<span data-ttu-id="4ee95-186">Conclusion : vos lancements pilotes successifs sont espacés de 60 jours.</span><span class="sxs-lookup"><span data-stu-id="4ee95-186">The result is a 60-day cadence between successive pilot rollouts.</span></span>

<span data-ttu-id="4ee95-187">Voici une expérience d’utilisateur final simplifiée à titre d’exemple :</span><span class="sxs-lookup"><span data-stu-id="4ee95-187">Here’s a simplified end-user experience as an example:</span></span>

- <span data-ttu-id="4ee95-p123">En janvier, je dois utiliser mon smartphone pour l’authentification multifacteur. (Identity)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p123">In January, I need to use my smart phone for MFA. (Identity)</span></span>
- <span data-ttu-id="4ee95-p124">En mars, Windows 10 Entreprise est installé sur mon ordinateur de bureau Windows 8.1. (Windows 10 Entreprise)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p124">In March, I get Windows 10 Enterprise installed on my Windows 8.1 desktop. (Windows 10 Enterprise)</span></span>
- <span data-ttu-id="4ee95-p125">En mai, Office 365 ProPlus est installé à la place d’Office 2013. (Office 365 ProPlus)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p125">In May, I get Office 365 ProPlus installed, replacing Office 2013. (Office 365 ProPlus)</span></span>
- <span data-ttu-id="4ee95-194">En juillet, j’obtiens l’inscription des appareils. D’autre part, les stratégies des applications et des appareils entrent en vigueur.</span><span class="sxs-lookup"><span data-stu-id="4ee95-194">In July, I get device enrollment and app and device policies applied.</span></span> <span data-ttu-id="4ee95-195">(Gestion des appareils mobiles)</span><span class="sxs-lookup"><span data-stu-id="4ee95-195">(Mobile device management)</span></span>
- <span data-ttu-id="4ee95-p127">En septembre, le client Azure Information Protection est installé et je reçois une formation pour savoir comment appliquer des étiquettes aux documents. (Information Protection)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p127">In September, I get the Azure Information Protection client installed and get trained on how to apply labels to documents. (Information protection)</span></span>

<span data-ttu-id="4ee95-198">Conclusion : vos lancements utilisateurs successifs sont espacés de 60 jours.</span><span class="sxs-lookup"><span data-stu-id="4ee95-198">The result is a 60-day cadence between successive user rollouts.</span></span>

<span data-ttu-id="4ee95-199">L’avantage de cette stratégie est que le déploiement intégral de l’infrastructure de base de Microsoft 365 pour entreprise prend moins de temps. De plus, votre département informatique et les utilisateurs n’ont pas affaire à plusieurs lancements en même temps.</span><span class="sxs-lookup"><span data-stu-id="4ee95-199">The advantage to this deployment strategy is that it can take less time to fully deploy the Microsoft 365 for enterprise foundation infrastructure, without having your IT department and users deal with multiple rollouts the same time.</span></span>

### <a name="parallel-deployment-with-overlapping-user-rollout-parallel-2"></a><span data-ttu-id="4ee95-200">Déploiement parallèle avec un lancement utilisateur concomitant (Parallèle 2)</span><span class="sxs-lookup"><span data-stu-id="4ee95-200">Parallel deployment with overlapping user rollout (Parallel 2)</span></span>

<span data-ttu-id="4ee95-201">Avec cette stratégie de déploiement :</span><span class="sxs-lookup"><span data-stu-id="4ee95-201">For this deployment strategy, you start the:</span></span>

- <span data-ttu-id="4ee95-202">le lancement pilote de la phase suivante commence quand le lancement utilisateur de la phase en cours se termine ;</span><span class="sxs-lookup"><span data-stu-id="4ee95-202">Pilot rollout of the next phase during the last part of the user rollout of the current phase.</span></span>
- <span data-ttu-id="4ee95-203">Déploiement des utilisateurs de la phase suivante pendant le déploiement des utilisateurs de la phase actuelle de sorte qu’aucun utilisateur ne fait face aux déploiements de plusieurs phases en même temps.</span><span class="sxs-lookup"><span data-stu-id="4ee95-203">User rollout of the next phase during the user rollout of the current phase in such a way that no user is dealing with the rollouts of multiple phases at the same time.</span></span> <span data-ttu-id="4ee95-204">Cela part du principe que vous déployez chaque phase de l’infrastructure de base de la même manière, à l’aide de régions, services ou autres groupements.</span><span class="sxs-lookup"><span data-stu-id="4ee95-204">This assumes that you are rolling out each phase of the foundation infrastructure in the same way, using regions, departments, or other groupings.</span></span>

<span data-ttu-id="4ee95-205">Voici une comparaison simplifiée des stratégies de déploiement.</span><span class="sxs-lookup"><span data-stu-id="4ee95-205">Here is a simplified comparison between the different deployment strategies.</span></span>

![Déploiement parallèle des phases 2 à 6 avec un lancement utilisateur concomitant](../media/deployment-strategies-microsoft-365-enterprise/parallel2.png) 

<span data-ttu-id="4ee95-207">Résultat :</span><span class="sxs-lookup"><span data-stu-id="4ee95-207">The end result is that:</span></span>

- <span data-ttu-id="4ee95-208">Les lancements pilotes passent d’une phase à l’autre sans interruption.</span><span class="sxs-lookup"><span data-stu-id="4ee95-208">Pilot rollouts go from one phase to the next without a pause.</span></span>
- <span data-ttu-id="4ee95-209">Le lancement utilisateur d’une phase commence avant la fin du lancement utilisateur de la phase précédente, mais aucun utilisateur ne déploie plusieurs phases à la fois.</span><span class="sxs-lookup"><span data-stu-id="4ee95-209">The user rollout for a phase begins before the completion of the user rollout of the previous phase, but no individual user is rolling out more than one phase at a time.</span></span>

<span data-ttu-id="4ee95-210">Voici une expérience utilisateur pilote simplifiée à titre d’exemple :</span><span class="sxs-lookup"><span data-stu-id="4ee95-210">Here’s a simplified pilot user experience as an example:</span></span>

- <span data-ttu-id="4ee95-p129">En décembre, je dois utiliser mon smartphone pour l’authentification multifacteur. (Identity)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p129">In December, I need to use my smart phone for MFA. (Identity)</span></span>
- <span data-ttu-id="4ee95-p130">En janvier, Windows 10 Entreprise est installé sur mon ordinateur de bureau Windows 8.1. (Windows 10 Entreprise)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p130">In January, I get Windows 10 Enterprise installed on my Windows 8.1 desktop. (Windows 10 Enterprise)</span></span>
- <span data-ttu-id="4ee95-p131">En février, Office 365 ProPlus est installé à la place d’Office 2013. (Office 365 ProPlus)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p131">In February, I get Office 365 ProPlus installed, replacing Office 2013. (Office 365 ProPlus)</span></span>
- <span data-ttu-id="4ee95-217">En mars, j’obtiens l’inscription des appareils. D’autre part, les stratégies des applications et des appareils entrent en vigueur.</span><span class="sxs-lookup"><span data-stu-id="4ee95-217">In March, I get device enrollment and app and device policies applied.</span></span> <span data-ttu-id="4ee95-218">(Gestion des appareils mobiles)</span><span class="sxs-lookup"><span data-stu-id="4ee95-218">(Mobile device management)</span></span>
- <span data-ttu-id="4ee95-p133">En avril, le client Azure Information Protection est installé et je reçois une formation pour savoir comment appliquer des étiquettes aux documents. (Information Protection)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p133">In April, I get the Azure Information Protection client installed and get trained on how to apply labels to documents. (Information protection)</span></span>

<span data-ttu-id="4ee95-221">Conclusion : vos lancements pilotes successifs sont espacés de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="4ee95-221">The result is a 30-day cadence between successive pilot rollouts.</span></span>

<span data-ttu-id="4ee95-222">Voici une expérience d’utilisateur final simplifiée à titre d’exemple :</span><span class="sxs-lookup"><span data-stu-id="4ee95-222">Here’s a simplified end-user experience as an example:</span></span>

- <span data-ttu-id="4ee95-p134">En janvier, je dois utiliser mon smartphone pour l’authentification multifacteur. (Identity)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p134">In January, I need to use my smart phone for MFA. (Identity)</span></span>
- <span data-ttu-id="4ee95-p135">En février, Windows 10 Entreprise est installé sur mon ordinateur de bureau Windows 8.1. (Windows 10 Entreprise)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p135">In February, I get Windows 10 Enterprise installed on my Windows 8.1 desktop. (Windows 10 Enterprise)</span></span>
- <span data-ttu-id="4ee95-p136">En mars, Office 365 ProPlus est installé à la place d’Office 2013. (Office 365 ProPlus)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p136">In March, I get Office 365 ProPlus installed, replacing Office 2013. (Office 365 ProPlus)</span></span>
- <span data-ttu-id="4ee95-229">En avril, j’obtiens l’inscription des appareils. D’autre part, les stratégies des applications et des appareils entrent en vigueur.</span><span class="sxs-lookup"><span data-stu-id="4ee95-229">In April, I get device enrollment and app and device policies applied.</span></span> <span data-ttu-id="4ee95-230">(Gestion des appareils mobiles)</span><span class="sxs-lookup"><span data-stu-id="4ee95-230">(Mobile device management)</span></span>
- <span data-ttu-id="4ee95-p138">En mai, le client Azure Information Protection est installé et je reçois une formation pour savoir comment appliquer des étiquettes aux documents. (Information Protection)</span><span class="sxs-lookup"><span data-stu-id="4ee95-p138">In May, I get the Azure Information Protection client installed and get trained on how to apply labels to documents. (Information protection)</span></span>

<span data-ttu-id="4ee95-233">Conclusion : vos lancements utilisateurs successifs sont espacés de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="4ee95-233">The result is a 30-day cadence between successive user rollouts.</span></span>

<span data-ttu-id="4ee95-234">L’avantage de cette stratégie est que le déploiement intégral de l’infrastructure de base de Microsoft 365 pour entreprise prend encore moins de temps. De plus, les utilisateurs finaux n’ont pas affaire à plusieurs déploiements simultanés.</span><span class="sxs-lookup"><span data-stu-id="4ee95-234">The advantage to this deployment strategy is that it can take even less time to fully deploy the Microsoft 365 for enterprise foundation infrastructure, still without having end-users deal with multiple rollouts the same time.</span></span> <span data-ttu-id="4ee95-235">Toutefois, les utilisateurs ne prennent pas de pause entre les phases successives.</span><span class="sxs-lookup"><span data-stu-id="4ee95-235">However, users don’t get a break between successive phases.</span></span>

### <a name="up-front-infrastructure-and-rollout-of-the-end-to-end-configuration"></a><span data-ttu-id="4ee95-236">Infrastructure initiale et lancement de la configuration de bout en bout</span><span class="sxs-lookup"><span data-stu-id="4ee95-236">Up-front infrastructure and rollout of the end-to-end configuration</span></span>

<span data-ttu-id="4ee95-237">Pour les petites organisations ayant la possibilité de condenser les phases 2à 6 dans un seul segment de déploiement, le déploiement qui en résulte se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="4ee95-237">For smaller organizations with the ability to compress phases 2-6 into a single deployment segment, the resulting deployment looks like this:</span></span>
 
![Infrastructure initiale et lancement de la configuration de bout en bout](../media/deployment-strategies-microsoft-365-enterprise/up-front.png) 

<span data-ttu-id="4ee95-p140">Le département informatique configure l’infrastructure pour les phases 2 à 6, puis la déploie auprès des utilisateurs pilotes pour vérifier les fonctionnalités de la configuration de bout à bout. Par exemple, les utilisateurs pilotes reçoivent toutes ces fonctionnalités en même temps :</span><span class="sxs-lookup"><span data-stu-id="4ee95-p140">The IT department configures the infrastructure for phases 2-6, then rolls out to the pilot users to check for the end-to-end functionality. For example, pilot users get all of this functionality at the same time:</span></span>

- <span data-ttu-id="4ee95-241">Authentification multifacteur et autres fonctionnalités d’identité (Identity)</span><span class="sxs-lookup"><span data-stu-id="4ee95-241">MFA and other identity features (Identity)</span></span>
- <span data-ttu-id="4ee95-242">Windows 10 Entreprise sur les appareils Windows (Windows 10 Entreprise)</span><span class="sxs-lookup"><span data-stu-id="4ee95-242">Windows 10 Enterprise on Windows devices (Windows 10 Enterprise)</span></span>
- <span data-ttu-id="4ee95-243">Office 365 ProPlus pour la suite Office (Office 365 ProPlus)</span><span class="sxs-lookup"><span data-stu-id="4ee95-243">Office 365 ProPlus for the Office suite (Office 365 ProPlus)</span></span>
- <span data-ttu-id="4ee95-244">Stratégies des applications et des appareils (Gestion des appareils mobiles)</span><span class="sxs-lookup"><span data-stu-id="4ee95-244">App and device policies (Mobile device management)</span></span>
- <span data-ttu-id="4ee95-245">Client Azure Information Protection installé et formation pour savoir appliquer des étiquettes aux documents (Information Protection)</span><span class="sxs-lookup"><span data-stu-id="4ee95-245">Azure Information Protection client installed and training on how to apply labels to documents (Information protection)</span></span>

<span data-ttu-id="4ee95-246">Une fois le lancement pilote terminé, le lancement utilisateur commence et fournit à chaque utilisateur toutes les fonctionnalités simultanément.</span><span class="sxs-lookup"><span data-stu-id="4ee95-246">Once the pilot rollout is concluded, the user rollout begins in which each user gets all the functionality the same time.</span></span>

## <a name="next-step"></a><span data-ttu-id="4ee95-247">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="4ee95-247">Next step</span></span>

<span data-ttu-id="4ee95-248">Lancez le déploiement de Microsoft 365 pour entreprise avec l’[infrastructure de base](deploy-foundation-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="4ee95-248">Start your deployment of Microsoft 365 for enterprise with the [foundation infrastructure](deploy-foundation-infrastructure.md).</span></span>
