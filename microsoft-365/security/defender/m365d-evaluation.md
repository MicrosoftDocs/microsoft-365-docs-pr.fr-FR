---
title: Évaluer Microsoft 365 Defender
description: Configurer votre laboratoire d’essai ou votre environnement pilote Microsoft 365 Defender pour tester et tester la solution de sécurité conçue pour protéger les appareils, l’identité, les données et les applications de votre organisation.
keywords: Microsoft 365 Version d’évaluation de Defender, essayez Microsoft 365 Defender, évaluez Microsoft 365 Defender, laboratoire d’évaluation de Microsoft 365 Defender, pilote Microsoft 365 Defender, cybersécurité, menace avancée persistante, sécurité d’entreprise, appareils, appareil, identité, utilisateurs, données, applications, incidents, investigation et correction automatisées, recherche avancée
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: dolmont
author: DulceMontemayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365solution-overview
- m365solution-evalutatemtp
ms.topic: conceptual
ms.technology: m365d
ms.openlocfilehash: 1c260588b80d8325567b74148a7a62586cfbc707
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933168"
---
# <a name="create-a-microsoft-365-defender-trial-lab-or-pilot-environment"></a><span data-ttu-id="36151-104">Créer un laboratoire d’essai Microsoft 365 Defender ou un environnement pilote</span><span class="sxs-lookup"><span data-stu-id="36151-104">Create a Microsoft 365 Defender trial lab or pilot environment</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="36151-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="36151-105">**Applies to:**</span></span>
- <span data-ttu-id="36151-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="36151-106">Microsoft 365 Defender</span></span>


<span data-ttu-id="36151-107">Ce guide vous aide à travailler sur la configuration d’un environnement de laboratoire avec des utilisateurs et des groupes, puis vous guide tout au long de la configuration des fonctionnalités dans Microsoft 365 Defender afin que vous pouvez simuler une attaque contre les menaces et obtenir un résultat d’essai significatif.</span><span class="sxs-lookup"><span data-stu-id="36151-107">This guide helps you work across setting up a lab environment with users and groups, then guides you through the configuration of the capabilities in Microsoft 365 Defender so that you can mimic a threat attack and obtain a meaningful trial result.</span></span> 

<span data-ttu-id="36151-108">L’objectif de la création de ce laboratoire d’évaluation ou de cet environnement pilote est d’illustrer les fonctionnalités complètes et intégrées Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="36151-108">The purpose of creating this trial lab or pilot environment is to illustrate the comprehensive and integrated Microsoft 365 Defender capabilities.</span></span> <span data-ttu-id="36151-109">Découvrez comment cette solution de sécurité intelligente détecte, empêche, examine automatiquement et répond aux menaces avancées de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="36151-109">Experience how this intelligent security solution detects, prevents, automatically investigates, and responds to advanced threats your organization.</span></span> 


<span data-ttu-id="36151-110">Vous serez guidé dans les étapes de démarrage de votre évaluation Microsoft 365 Defender en fonction des chemins de déploiement recommandés.</span><span class="sxs-lookup"><span data-stu-id="36151-110">You will be guided through the steps to start your Microsoft 365 Defender evaluation based on the recommended deployment paths.</span></span> <span data-ttu-id="36151-111">L’objectif est de vous aider à configurer la solution de sécurité dans un environnement de laboratoire avec un compte d’essai ou dans un environnement pilote en production avec une licence complète.</span><span class="sxs-lookup"><span data-stu-id="36151-111">The goal is to help you set up the security solution either in a lab environment with a trial account, or in a pilot environment in production with a full license.</span></span> <span data-ttu-id="36151-112">La préparation de votre laboratoire d’essai ou de votre environnement pilote peut vous aider à présenter les cas d’utilisation des opérations de sécurité aux décideurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="36151-112">Preparing your trial lab or pilot environment can help you present security operation use cases to decision makers in your organization.</span></span> <span data-ttu-id="36151-113">Lorsque vous avez terminé l’exécution de vos simulations d’attaques et que vous êtes satisfait des résultats, vous pouvez entièrement les déployer et les opérationnels dans votre organisation à l’aide de professionnels de la vente techniques Microsoft ou d’experts de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="36151-113">When you’re done running your attack simulations and are satisfied with the results, you can fully deploy and operationalize it in your organization with the help of Microsoft Technical Sales Professionals or experts in your organization.</span></span> 

<span data-ttu-id="36151-114">Ce guide vous aidera :</span><span class="sxs-lookup"><span data-stu-id="36151-114">This guide will help you:</span></span>
- <span data-ttu-id="36151-115">Configurer le serveur et les ordinateurs de votre atelier</span><span class="sxs-lookup"><span data-stu-id="36151-115">Set up your lab server and computers</span></span>
- <span data-ttu-id="36151-116">Configurer Active Directory avec des utilisateurs et des groupes</span><span class="sxs-lookup"><span data-stu-id="36151-116">Configure Active Directory with users and groups</span></span>
- <span data-ttu-id="36151-117">Configurer Microsoft Defender pour l’identité, Microsoft Defender pour Office 365, Microsoft Defender pour le point de terminaison et Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="36151-117">Set up and configure Microsoft Defender for Identity, Microsoft Defender for Office 365, Microsoft Defender for Endpoint, and Microsoft Cloud App Security</span></span>
- <span data-ttu-id="36151-118">Configurer des stratégies locales pour votre serveur et vos ordinateurs</span><span class="sxs-lookup"><span data-stu-id="36151-118">Set up local policies for your server and computers</span></span>
- <span data-ttu-id="36151-119">Simuler une attaque contre une menace pour générer un incident de test ou une alerte dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="36151-119">Mimic a threat attack to generate a test incident or alert in Microsoft 365 Defender</span></span>

>[!IMPORTANT]
><span data-ttu-id="36151-120">Pour obtenir des résultats optimaux, suivez les instructions de configuration de l’atelier aussi étroitement que possible.</span><span class="sxs-lookup"><span data-stu-id="36151-120">For optimum results, follow the lab setup instructions as closely as possible.</span></span>


## <a name="deployment-phases"></a><span data-ttu-id="36151-121">Phases de déploiement</span><span class="sxs-lookup"><span data-stu-id="36151-121">Deployment phases</span></span>

<span data-ttu-id="36151-122">La création d’un environnement de laboratoire d’Microsoft 365 Defender se fait en trois phases.</span><span class="sxs-lookup"><span data-stu-id="36151-122">There are three phases in creating a Microsoft 365 Defender trial lab environment.</span></span>

![Phases de déploiement : préparer, configurer, intégrer](../../media/evaluation-guide-phases.png)

|<span data-ttu-id="36151-124">Phase</span><span class="sxs-lookup"><span data-stu-id="36151-124">Phase</span></span> | <span data-ttu-id="36151-125">Description</span><span class="sxs-lookup"><span data-stu-id="36151-125">Description</span></span> | 
|:-------|:-----|
|[<span data-ttu-id="36151-126">Phase 1 : préparation</span><span class="sxs-lookup"><span data-stu-id="36151-126">Phase 1: Prepare</span></span>](prepare-m365d-eval.md)| <span data-ttu-id="36151-127">Découvrez ce que vous devez prendre en compte lors du déploiement de Microsoft 365 Defender dans un laboratoire d’essai ou un environnement pilote :</span><span class="sxs-lookup"><span data-stu-id="36151-127">Learn what you need to consider when deploying Microsoft 365 Defender in a trial lab or pilot environment:</span></span> <br><br><span data-ttu-id="36151-128">- Parties prenantes et sign-off</span><span class="sxs-lookup"><span data-stu-id="36151-128">- Stakeholders and sign-off</span></span> <br> <span data-ttu-id="36151-129">- Considérations sur l’environnement</span><span class="sxs-lookup"><span data-stu-id="36151-129">- Environment considerations</span></span> <br><span data-ttu-id="36151-130">- Access</span><span class="sxs-lookup"><span data-stu-id="36151-130">- Access</span></span> <br><span data-ttu-id="36151-131">- configuration Azure Active Directory’installation</span><span class="sxs-lookup"><span data-stu-id="36151-131">- Azure Active Directory setup</span></span> <br> <span data-ttu-id="36151-132">- Ordre de configuration</span><span class="sxs-lookup"><span data-stu-id="36151-132">- Configuration order</span></span>
|[<span data-ttu-id="36151-133">Phase 2 : configuration</span><span class="sxs-lookup"><span data-stu-id="36151-133">Phase 2: Setup</span></span>](setup-m365deval.md)|  <span data-ttu-id="36151-134">Prenez les étapes initiales pour accéder Microsoft 365 centre de sécurité pour configurer votre laboratoire d’évaluation Microsoft 365 Defender ou votre environnement pilote.</span><span class="sxs-lookup"><span data-stu-id="36151-134">Take the initial steps to access Microsoft 365 Security Center to set up your Microsoft 365 Defender trial lab or pilot environment.</span></span> <span data-ttu-id="36151-135">Vous serez guidé vers :</span><span class="sxs-lookup"><span data-stu-id="36151-135">You'll be guided to:</span></span><br><br><span data-ttu-id="36151-136">- S’inscrire à Microsoft 365 E5 d’essai</span><span class="sxs-lookup"><span data-stu-id="36151-136">- Sign up for Microsoft 365 E5 Trial</span></span> <br>  <span data-ttu-id="36151-137">- Configurer un domaine</span><span class="sxs-lookup"><span data-stu-id="36151-137">- Configure domain</span></span><br><span data-ttu-id="36151-138">- Attribuer Microsoft 365 E5 licences</span><span class="sxs-lookup"><span data-stu-id="36151-138">- Assign Microsoft 365 E5 licenses</span></span><br><span data-ttu-id="36151-139">- Terminer l’Assistant Installation dans le portail</span><span class="sxs-lookup"><span data-stu-id="36151-139">- Complete the setup wizard in the portal</span></span>|
|[<span data-ttu-id="36151-140">Phase 3 : Configurer & intégré</span><span class="sxs-lookup"><span data-stu-id="36151-140">Phase 3: Configure & Onboard</span></span>](config-m365d-eval.md) | <span data-ttu-id="36151-141">Configurez chaque colonne Microsoft 365 Defender et les points de terminaison intégrés.</span><span class="sxs-lookup"><span data-stu-id="36151-141">Configure each Microsoft 365 Defender pillar and onboard endpoints.</span></span> <span data-ttu-id="36151-142">Vous serez guidé vers :</span><span class="sxs-lookup"><span data-stu-id="36151-142">You'll be guided to:</span></span><br><br><span data-ttu-id="36151-143">- Configurer Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="36151-143">- Configure Microsoft Defender for Office 365</span></span><br><span data-ttu-id="36151-144">- Configurer Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="36151-144">- Configure Microsoft Cloud App Security</span></span><br><span data-ttu-id="36151-145">- Configurer Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="36151-145">- Configure Microsoft Defender for Identity</span></span><br><span data-ttu-id="36151-146">- Configurer Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="36151-146">- Configure Microsoft Defender for Endpoint</span></span>


<span data-ttu-id="36151-147">Une fois ce guide terminé, vous avez identifié les parties prenantes impliquées et les approbations requises, vous avez les autorisations d’accès nécessaires, vous êtes inscrit à la version d’évaluation, vous avez configuré les domaines et chacun des piliers de Microsoft 365 Defender, et vos points de terminaison sont intégrés au service.</span><span class="sxs-lookup"><span data-stu-id="36151-147">After you've completed this guide, you would have identified the stakeholders involved and the required approvals,  have the right access permissions, signed up for trial, configured domains and each of the Microsoft 365 Defender pillars, and your endpoints will be onboarded to the service.</span></span>

## <a name="key-capabilities"></a><span data-ttu-id="36151-148">Fonctionnalités clés</span><span class="sxs-lookup"><span data-stu-id="36151-148">Key capabilities</span></span>

<span data-ttu-id="36151-149">Bien Microsoft 365 Defender offre de nombreuses fonctionnalités, l’objectif principal de ce guide de déploiement est de vous aider à commencer par l’intégration d’appareils.</span><span class="sxs-lookup"><span data-stu-id="36151-149">While Microsoft 365 Defender provides many capabilities, the primary purpose of this deployment guide is to get you started by onboarding devices.</span></span> <span data-ttu-id="36151-150">En plus de l’intégration, ces conseils vous guident avec les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="36151-150">In addition to onboarding, this guidance gets you started with the following capabilities.</span></span>


<span data-ttu-id="36151-151">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="36151-151">Capability</span></span> | <span data-ttu-id="36151-152">Description</span><span class="sxs-lookup"><span data-stu-id="36151-152">Description</span></span> 
:---|:---
<span data-ttu-id="36151-153">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="36151-153">Microsoft Defender for Office 365</span></span> | <span data-ttu-id="36151-154">Permet de protéger l’ensemble Office 365 envrionment contre les menaces actuelles</span><span class="sxs-lookup"><span data-stu-id="36151-154">Helps protect your entire Office 365 envrionment from today's threats</span></span>
<span data-ttu-id="36151-155">Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="36151-155">Microsoft Defender for Identity</span></span> | <span data-ttu-id="36151-156">Identifie et détecte les menaces sur les identités compromises et les actions internes malveillantes.</span><span class="sxs-lookup"><span data-stu-id="36151-156">Identifies and detects  threats on compromised identities and malicious insider actions.</span></span>
<span data-ttu-id="36151-157">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="36151-157">Microsoft Cloud App Security</span></span> | <span data-ttu-id="36151-158">Fournit une visibilité enrichie, contrôle les déplacements de données et détecte les cybermenaces dans les services cloud.</span><span class="sxs-lookup"><span data-stu-id="36151-158">Provides rich visibility, control data travel, and detect cyberthreats across cloud services.</span></span>
<span data-ttu-id="36151-159">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="36151-159">Microsoft Defender for Endpoint</span></span> | <span data-ttu-id="36151-160">Empêche, détecte et fournit des fonctionnalités de réponse aux menaces avancées avec une sécurité complète des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="36151-160">Prevents, detects, and provides response capabilities to advanced threats with comprehensive endpoint security.</span></span>


## <a name="in-scope"></a><span data-ttu-id="36151-161">Dans l’étendue</span><span class="sxs-lookup"><span data-stu-id="36151-161">In scope</span></span>

<span data-ttu-id="36151-162">Les tâches suivantes sont dans l’étendue de ce guide :</span><span class="sxs-lookup"><span data-stu-id="36151-162">The following tasks are in scope for this guide:</span></span>
-   <span data-ttu-id="36151-163">Configurer Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="36151-163">Set up Azure Active Directory</span></span>
-   <span data-ttu-id="36151-164">Configurer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="36151-164">Set up Microsoft 365 Defender</span></span>
    -   <span data-ttu-id="36151-165">Inscrivez-vous à Microsoft 365 E5 version d’essai ou utilisez votre licence complète si vous exécutez un pilote</span><span class="sxs-lookup"><span data-stu-id="36151-165">Sign up for Microsoft 365 E5 Trial or use your full license if you're running a pilot</span></span>
    -   <span data-ttu-id="36151-166">Configurer un domaine</span><span class="sxs-lookup"><span data-stu-id="36151-166">Configure domain</span></span>
    -   <span data-ttu-id="36151-167">Attribuer Microsoft 365 E5 licences</span><span class="sxs-lookup"><span data-stu-id="36151-167">Assign Microsoft 365 E5 licenses</span></span>
    -   <span data-ttu-id="36151-168">Fin de l’Assistant Installation dans le portail</span><span class="sxs-lookup"><span data-stu-id="36151-168">Completing the setup wizard within the portal</span></span>
-   <span data-ttu-id="36151-169">Configurer tous les piliers Microsoft 365 Defender en fonction des meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="36151-169">Configure all Microsoft 365 Defender pillars based on best practices</span></span>
    -   <span data-ttu-id="36151-170">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="36151-170">Microsoft Defender for Office 365</span></span>
    -   <span data-ttu-id="36151-171">Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="36151-171">Microsoft Defender for Identity</span></span>
    -   <span data-ttu-id="36151-172">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="36151-172">Microsoft Cloud App Security</span></span>
    -   <span data-ttu-id="36151-173">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="36151-173">Microsoft Defender for Endpoint</span></span>

## <a name="out-of-scope"></a><span data-ttu-id="36151-174">Non compris</span><span class="sxs-lookup"><span data-stu-id="36151-174">Out of scope</span></span>

<span data-ttu-id="36151-175">Ce guide de déploiement n’entre pas dans le cadre de ce guide de déploiement :</span><span class="sxs-lookup"><span data-stu-id="36151-175">The following are out of scope of this deployment guide:</span></span>

-   <span data-ttu-id="36151-176">Configuration de solutions tierces qui peuvent s’intégrer à Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="36151-176">Configuration of third-party solutions that might integrate with Microsoft 365 Defender</span></span>
-   <span data-ttu-id="36151-177">Test de pénétration dans un environnement de production</span><span class="sxs-lookup"><span data-stu-id="36151-177">Penetration testing in production environment</span></span>

## <a name="next-step"></a><span data-ttu-id="36151-178">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="36151-178">Next step</span></span>
<span data-ttu-id="36151-179">[Phase 1 : Préparer](prepare-m365d-eval.md) 
</span><span class="sxs-lookup"><span data-stu-id="36151-179">[Phase 1: Prepare](prepare-m365d-eval.md) 
</span></span><br> <span data-ttu-id="36151-180">Préparer votre laboratoire d Microsoft 365 d’essai ou votre environnement pilote de Defender</span><span class="sxs-lookup"><span data-stu-id="36151-180">Prepare your Microsoft 365 Defender trial lab or pilot environment</span></span>
