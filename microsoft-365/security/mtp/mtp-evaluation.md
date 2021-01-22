---
title: Évaluer Microsoft 365 Defender
description: Configurer votre laboratoire d’essai ou votre environnement pilote Microsoft 365 Defender pour tester et tester la solution de sécurité conçue pour protéger les appareils, l’identité, les données et les applications de votre organisation.
keywords: Essai de la Protection Microsoft contre les menaces, essayer la Protection Microsoft contre les menaces, évaluer la Protection Microsoft contre les menaces, laboratoire d’évaluation de la Protection Microsoft contre les menaces, pilote de la Protection Microsoft contre les menaces, cyber-sécurité, menace avancée persistante, sécurité d’entreprise, appareils, identité, utilisateurs, données, applications, incidents, examen et correction automatisés, recherche avancée
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
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365solution-overview
- m365solution-evalutatemtp
ms.topic: conceptual
ms.technology: m365d
ms.openlocfilehash: 6735817a71f9fb50843acad3a13596ec247aa407
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49930209"
---
# <a name="create-a-microsoft-365-defender-trial-lab-or-pilot-environment"></a><span data-ttu-id="10f56-104">Créer un laboratoire d’essai ou un environnement pilote Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="10f56-104">Create a Microsoft 365 Defender trial lab or pilot environment</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="10f56-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="10f56-105">**Applies to:**</span></span>
- <span data-ttu-id="10f56-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="10f56-106">Microsoft 365 Defender</span></span>


<span data-ttu-id="10f56-107">Ce guide vous aide à travailler sur la configuration d’un environnement de laboratoire avec des utilisateurs et des groupes, puis vous guide tout au long de la configuration des fonctionnalités de Microsoft 365 Defender afin que vous pouvez simuler une attaque contre les menaces et obtenir un résultat d’essai significatif.</span><span class="sxs-lookup"><span data-stu-id="10f56-107">This guide helps you work across setting up a lab environment with users and groups, then guides you through the configuration of the capabilities in Microsoft 365 Defender so that you can mimic a threat attack and obtain a meaningful trial result.</span></span> 

<span data-ttu-id="10f56-108">L’objectif de la création de ce laboratoire d’évaluation ou de cet environnement pilote est d’illustrer les fonctionnalités complètes et intégrées de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="10f56-108">The purpose of creating this trial lab or pilot environment is to illustrate the comprehensive and integrated Microsoft 365 Defender capabilities.</span></span> <span data-ttu-id="10f56-109">Découvrez comment cette solution de sécurité intelligente détecte, empêche, examine automatiquement et répond aux menaces avancées de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="10f56-109">Experience how this intelligent security solution detects, prevents, automatically investigates, and responds to advanced threats your organization.</span></span> 


<span data-ttu-id="10f56-110">Vous serez guidé dans les étapes de démarrage de votre évaluation de Microsoft 365 Defender en fonction des chemins de déploiement recommandés.</span><span class="sxs-lookup"><span data-stu-id="10f56-110">You will be guided through the steps to start your Microsoft 365 Defender evaluation based on the recommended deployment paths.</span></span> <span data-ttu-id="10f56-111">L’objectif est de vous aider à configurer la solution de sécurité dans un environnement de laboratoire avec un compte d’essai ou dans un environnement pilote en production avec une licence complète.</span><span class="sxs-lookup"><span data-stu-id="10f56-111">The goal is to help you set up the security solution either in a lab environment with a trial account, or in a pilot environment in production with a full license.</span></span> <span data-ttu-id="10f56-112">La préparation de votre laboratoire d’essai ou de votre environnement pilote peut vous aider à présenter les cas d’utilisation des opérations de sécurité aux décideurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="10f56-112">Preparing your trial lab or pilot environment can help you present security operation use cases to decision makers in your organization.</span></span> <span data-ttu-id="10f56-113">Lorsque vous avez terminé l’exécution de vos simulations d’attaques et que vous êtes satisfait des résultats, vous pouvez entièrement le déployer et le déployer dans votre organisation à l’aide de professionnels des ventes techniques microsoft ou d’experts de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="10f56-113">When you’re done running your attack simulations and are satisfied with the results, you can fully deploy and operationalize it in your organization with the help of Microsoft Technical Sales Professionals or experts in your organization.</span></span> 

<span data-ttu-id="10f56-114">Ce guide vous aidera :</span><span class="sxs-lookup"><span data-stu-id="10f56-114">This guide will help you:</span></span>
- <span data-ttu-id="10f56-115">Configurer le serveur et les ordinateurs de votre atelier</span><span class="sxs-lookup"><span data-stu-id="10f56-115">Set up your lab server and computers</span></span>
- <span data-ttu-id="10f56-116">Configurer Active Directory avec des utilisateurs et des groupes</span><span class="sxs-lookup"><span data-stu-id="10f56-116">Configure Active Directory with users and groups</span></span>
- <span data-ttu-id="10f56-117">Configurer Microsoft Defender pour l’identité, Microsoft Defender pour Office 365, Microsoft Defender pour le point de terminaison et Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="10f56-117">Set up and configure Microsoft Defender for Identity, Microsoft Defender for Office 365, Microsoft Defender for Endpoint, and Microsoft Cloud App Security</span></span>
- <span data-ttu-id="10f56-118">Configurer des stratégies locales pour votre serveur et vos ordinateurs</span><span class="sxs-lookup"><span data-stu-id="10f56-118">Set up local policies for your server and computers</span></span>
- <span data-ttu-id="10f56-119">Simuler une attaque contre une menace pour générer un incident de test ou une alerte dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="10f56-119">Mimic a threat attack to generate a test incident or alert in Microsoft 365 Defender</span></span>

>[!IMPORTANT]
><span data-ttu-id="10f56-120">Pour obtenir des résultats optimaux, suivez les instructions de configuration de l’atelier aussi étroitement que possible.</span><span class="sxs-lookup"><span data-stu-id="10f56-120">For optimum results, follow the lab setup instructions as closely as possible.</span></span>


## <a name="deployment-phases"></a><span data-ttu-id="10f56-121">Phases de déploiement</span><span class="sxs-lookup"><span data-stu-id="10f56-121">Deployment phases</span></span>

<span data-ttu-id="10f56-122">La création d’un environnement de laboratoire d’essai Microsoft 365 Defender se fait en trois phases.</span><span class="sxs-lookup"><span data-stu-id="10f56-122">There are three phases in creating a Microsoft 365 Defender trial lab environment.</span></span>

![Phases de déploiement : préparer, configurer, intégrer](../../media/evaluation-guide-phases.png)

|<span data-ttu-id="10f56-124">Phase</span><span class="sxs-lookup"><span data-stu-id="10f56-124">Phase</span></span> | <span data-ttu-id="10f56-125">Description</span><span class="sxs-lookup"><span data-stu-id="10f56-125">Description</span></span> | 
|:-------|:-----|
|[<span data-ttu-id="10f56-126">Phase 1 : Préparer</span><span class="sxs-lookup"><span data-stu-id="10f56-126">Phase 1: Prepare</span></span>](prepare-mtpeval.md)| <span data-ttu-id="10f56-127">Découvrez ce que vous devez prendre en compte lors du déploiement de Microsoft 365 Defender dans un laboratoire d’essai ou un environnement pilote :</span><span class="sxs-lookup"><span data-stu-id="10f56-127">Learn what you need to consider when deploying Microsoft 365 Defender in a trial lab or pilot environment:</span></span> <br><br><span data-ttu-id="10f56-128">- Parties prenantes et sign-off</span><span class="sxs-lookup"><span data-stu-id="10f56-128">- Stakeholders and sign-off</span></span> <br> <span data-ttu-id="10f56-129">- Considérations sur l’environnement</span><span class="sxs-lookup"><span data-stu-id="10f56-129">- Environment considerations</span></span> <br><span data-ttu-id="10f56-130">- Access</span><span class="sxs-lookup"><span data-stu-id="10f56-130">- Access</span></span> <br><span data-ttu-id="10f56-131">- Configuration d’Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="10f56-131">- Azure Active Directory setup</span></span> <br> <span data-ttu-id="10f56-132">- Ordre de configuration</span><span class="sxs-lookup"><span data-stu-id="10f56-132">- Configuration order</span></span>
|[<span data-ttu-id="10f56-133">Phase 2 : Installation</span><span class="sxs-lookup"><span data-stu-id="10f56-133">Phase 2: Setup</span></span>](setup-mtpeval.md)|  <span data-ttu-id="10f56-134">Prenez les étapes initiales pour accéder au Centre de sécurité Microsoft 365 afin de configurer votre laboratoire d’évaluation ou votre environnement pilote Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="10f56-134">Take the initial steps to access Microsoft 365 Security Center to set up your Microsoft 365 Defender trial lab or pilot environment.</span></span> <span data-ttu-id="10f56-135">Vous serez guidé vers :</span><span class="sxs-lookup"><span data-stu-id="10f56-135">You'll be guided to:</span></span><br><br><span data-ttu-id="10f56-136">- S’inscrire à la version d’essai de Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="10f56-136">- Sign up for Microsoft 365 E5 Trial</span></span> <br>  <span data-ttu-id="10f56-137">- Configurer un domaine</span><span class="sxs-lookup"><span data-stu-id="10f56-137">- Configure domain</span></span><br><span data-ttu-id="10f56-138">- Attribuer des licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="10f56-138">- Assign Microsoft 365 E5 licenses</span></span><br><span data-ttu-id="10f56-139">- Terminer l’Assistant Installation dans le portail</span><span class="sxs-lookup"><span data-stu-id="10f56-139">- Complete the setup wizard in the portal</span></span>|
|[<span data-ttu-id="10f56-140">Phase 3 : Configurer & intégré</span><span class="sxs-lookup"><span data-stu-id="10f56-140">Phase 3: Configure & Onboard</span></span>](config-mtpeval.md) | <span data-ttu-id="10f56-141">Configurez chaque pilier microsoft 365 Defender et les points de terminaison intégrés.</span><span class="sxs-lookup"><span data-stu-id="10f56-141">Configure each Microsoft 365 Defender pillar and onboard endpoints.</span></span> <span data-ttu-id="10f56-142">Vous serez guidé vers :</span><span class="sxs-lookup"><span data-stu-id="10f56-142">You'll be guided to:</span></span><br><br><span data-ttu-id="10f56-143">- Configurer Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="10f56-143">- Configure Microsoft Defender for Office 365</span></span><br><span data-ttu-id="10f56-144">- Configurer Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="10f56-144">- Configure Microsoft Cloud App Security</span></span><br><span data-ttu-id="10f56-145">- Configurer Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="10f56-145">- Configure Microsoft Defender for Identity</span></span><br><span data-ttu-id="10f56-146">- Configurer Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="10f56-146">- Configure Microsoft Defender for Endpoint</span></span>


<span data-ttu-id="10f56-147">Une fois ce guide terminé, vous avez identifié les parties prenantes impliquées et les approbations requises, vous avez les autorisations d’accès requises, vous êtes inscrit pour la version d’évaluation, les domaines configurés et chacun des piliers de Microsoft 365 Defender, et vos points de terminaison sont intégrés au service.</span><span class="sxs-lookup"><span data-stu-id="10f56-147">After you've completed this guide, you would have identified the stakeholders involved and the required approvals,  have the right access permissions, signed up for trial, configured domains and each of the Microsoft 365 Defender pillars, and your endpoints will be onboarded to the service.</span></span>

## <a name="key-capabilities"></a><span data-ttu-id="10f56-148">Fonctionnalités clés</span><span class="sxs-lookup"><span data-stu-id="10f56-148">Key capabilities</span></span>

<span data-ttu-id="10f56-149">Bien que Microsoft 365 Defender offre de nombreuses fonctionnalités, l’objectif principal de ce guide de déploiement est de vous aider à commencer par l’intégration d’appareils.</span><span class="sxs-lookup"><span data-stu-id="10f56-149">While Microsoft 365 Defender provides many capabilities, the primary purpose of this deployment guide is to get you started by onboarding devices.</span></span> <span data-ttu-id="10f56-150">En plus de l’intégration, ces conseils vous guident avec les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="10f56-150">In addition to onboarding, this guidance gets you started with the following capabilities.</span></span>


<span data-ttu-id="10f56-151">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="10f56-151">Capability</span></span> | <span data-ttu-id="10f56-152">Description</span><span class="sxs-lookup"><span data-stu-id="10f56-152">Description</span></span> 
:---|:---
<span data-ttu-id="10f56-153">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="10f56-153">Microsoft Defender for Office 365</span></span> | <span data-ttu-id="10f56-154">Permet de protéger l’ensemble de votre système Office 365 contre les menaces actuelles</span><span class="sxs-lookup"><span data-stu-id="10f56-154">Helps protect your entire Office 365 envrionment from today's threats</span></span>
<span data-ttu-id="10f56-155">Microsoft Defender pour Identity</span><span class="sxs-lookup"><span data-stu-id="10f56-155">Microsoft Defender for Identity</span></span> | <span data-ttu-id="10f56-156">Identifie et détecte les menaces sur les identités compromises et les actions internes malveillantes.</span><span class="sxs-lookup"><span data-stu-id="10f56-156">Identifies and detects  threats on compromised identities and malicious insider actions.</span></span>
<span data-ttu-id="10f56-157">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="10f56-157">Microsoft Cloud App Security</span></span> | <span data-ttu-id="10f56-158">Fournit une visibilité enrichie, contrôle les déplacements de données et détecte les cybermenaces dans les services cloud.</span><span class="sxs-lookup"><span data-stu-id="10f56-158">Provides rich visibility, control data travel, and detect cyberthreats across cloud services.</span></span>
<span data-ttu-id="10f56-159">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="10f56-159">Microsoft Defender for Endpoint</span></span> | <span data-ttu-id="10f56-160">Empêche, détecte et fournit des fonctionnalités de réponse aux menaces avancées avec une sécurité complète des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="10f56-160">Prevents, detects, and provides response capabilities to advanced threats with comprehensive endpoint security.</span></span>


## <a name="in-scope"></a><span data-ttu-id="10f56-161">Dans l’étendue</span><span class="sxs-lookup"><span data-stu-id="10f56-161">In scope</span></span>

<span data-ttu-id="10f56-162">Les tâches suivantes sont dans l’étendue de ce guide :</span><span class="sxs-lookup"><span data-stu-id="10f56-162">The following tasks are in scope for this guide:</span></span>
-   <span data-ttu-id="10f56-163">Configurer Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="10f56-163">Set up Azure Active Directory</span></span>
-   <span data-ttu-id="10f56-164">Configurer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="10f56-164">Set up Microsoft 365 Defender</span></span>
    -   <span data-ttu-id="10f56-165">S’inscrire à la version d’essai de Microsoft 365 E5 ou utiliser votre licence complète si vous exécutez un pilote</span><span class="sxs-lookup"><span data-stu-id="10f56-165">Sign up for Microsoft 365 E5 Trial or use your full license if you're running a pilot</span></span>
    -   <span data-ttu-id="10f56-166">Configurer un domaine</span><span class="sxs-lookup"><span data-stu-id="10f56-166">Configure domain</span></span>
    -   <span data-ttu-id="10f56-167">Attribuer des licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="10f56-167">Assign Microsoft 365 E5 licenses</span></span>
    -   <span data-ttu-id="10f56-168">Fin de l’Assistant Installation dans le portail</span><span class="sxs-lookup"><span data-stu-id="10f56-168">Completing the setup wizard within the portal</span></span>
-   <span data-ttu-id="10f56-169">Configurer tous les piliers de Microsoft 365 Defender en fonction des meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="10f56-169">Configure all Microsoft 365 Defender pillars based on best practices</span></span>
    -   <span data-ttu-id="10f56-170">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="10f56-170">Microsoft Defender for Office 365</span></span>
    -   <span data-ttu-id="10f56-171">Microsoft Defender pour Identity</span><span class="sxs-lookup"><span data-stu-id="10f56-171">Microsoft Defender for Identity</span></span>
    -   <span data-ttu-id="10f56-172">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="10f56-172">Microsoft Cloud App Security</span></span>
    -   <span data-ttu-id="10f56-173">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="10f56-173">Microsoft Defender for Endpoint</span></span>

## <a name="out-of-scope"></a><span data-ttu-id="10f56-174">Non compris</span><span class="sxs-lookup"><span data-stu-id="10f56-174">Out of scope</span></span>

<span data-ttu-id="10f56-175">Ce guide de déploiement n’entre pas dans le cadre de ce guide de déploiement :</span><span class="sxs-lookup"><span data-stu-id="10f56-175">The following are out of scope of this deployment guide:</span></span>

-   <span data-ttu-id="10f56-176">Configuration de solutions tierces qui peuvent s’intégrer à Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="10f56-176">Configuration of third-party solutions that might integrate with Microsoft 365 Defender</span></span>
-   <span data-ttu-id="10f56-177">Test de pénétration dans un environnement de production</span><span class="sxs-lookup"><span data-stu-id="10f56-177">Penetration testing in production environment</span></span>

## <a name="next-step"></a><span data-ttu-id="10f56-178">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="10f56-178">Next step</span></span>
<span data-ttu-id="10f56-179">[Phase 1 : Préparer](prepare-mtpeval.md) 
</span><span class="sxs-lookup"><span data-stu-id="10f56-179">[Phase 1: Prepare](prepare-mtpeval.md) 
</span></span><br> <span data-ttu-id="10f56-180">Préparer votre laboratoire d’essai ou votre environnement pilote Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="10f56-180">Prepare your Microsoft 365 Defender trial lab or pilot environment</span></span>
