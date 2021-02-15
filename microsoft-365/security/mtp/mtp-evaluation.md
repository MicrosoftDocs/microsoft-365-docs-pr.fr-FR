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
# <a name="create-a-microsoft-365-defender-trial-lab-or-pilot-environment"></a><span data-ttu-id="924ff-104">Créer un laboratoire d’essai ou un environnement pilote Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="924ff-104">Create a Microsoft 365 Defender trial lab or pilot environment</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="924ff-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="924ff-105">**Applies to:**</span></span>
- <span data-ttu-id="924ff-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="924ff-106">Microsoft 365 Defender</span></span>


<span data-ttu-id="924ff-107">Ce guide vous aide à travailler sur la configuration d’un environnement de laboratoire avec des utilisateurs et des groupes, puis vous guide tout au long de la configuration des fonctionnalités de Microsoft 365 Defender afin que vous pouvez simuler une attaque contre les menaces et obtenir un résultat d’essai significatif.</span><span class="sxs-lookup"><span data-stu-id="924ff-107">This guide helps you work across setting up a lab environment with users and groups, then guides you through the configuration of the capabilities in Microsoft 365 Defender so that you can mimic a threat attack and obtain a meaningful trial result.</span></span> 

<span data-ttu-id="924ff-108">L’objectif de la création de ce laboratoire d’évaluation ou de cet environnement pilote est d’illustrer les fonctionnalités complètes et intégrées de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="924ff-108">The purpose of creating this trial lab or pilot environment is to illustrate the comprehensive and integrated Microsoft 365 Defender capabilities.</span></span> <span data-ttu-id="924ff-109">Découvrez comment cette solution de sécurité intelligente détecte, empêche, examine automatiquement et répond aux menaces avancées de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="924ff-109">Experience how this intelligent security solution detects, prevents, automatically investigates, and responds to advanced threats your organization.</span></span> 


<span data-ttu-id="924ff-110">Vous serez guidé dans les étapes de démarrage de votre évaluation de Microsoft 365 Defender en fonction des chemins de déploiement recommandés.</span><span class="sxs-lookup"><span data-stu-id="924ff-110">You will be guided through the steps to start your Microsoft 365 Defender evaluation based on the recommended deployment paths.</span></span> <span data-ttu-id="924ff-111">L’objectif est de vous aider à configurer la solution de sécurité dans un environnement de laboratoire avec un compte d’essai ou dans un environnement pilote en production avec une licence complète.</span><span class="sxs-lookup"><span data-stu-id="924ff-111">The goal is to help you set up the security solution either in a lab environment with a trial account, or in a pilot environment in production with a full license.</span></span> <span data-ttu-id="924ff-112">La préparation de votre laboratoire d’essai ou de votre environnement pilote peut vous aider à présenter les cas d’utilisation des opérations de sécurité aux décideurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="924ff-112">Preparing your trial lab or pilot environment can help you present security operation use cases to decision makers in your organization.</span></span> <span data-ttu-id="924ff-113">Lorsque vous avez terminé l’exécution de vos simulations d’attaques et que vous êtes satisfait des résultats, vous pouvez entièrement le déployer et le déployer dans votre organisation à l’aide de professionnels des ventes techniques microsoft ou d’experts de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="924ff-113">When you’re done running your attack simulations and are satisfied with the results, you can fully deploy and operationalize it in your organization with the help of Microsoft Technical Sales Professionals or experts in your organization.</span></span> 

<span data-ttu-id="924ff-114">Ce guide vous aidera :</span><span class="sxs-lookup"><span data-stu-id="924ff-114">This guide will help you:</span></span>
- <span data-ttu-id="924ff-115">Configurer le serveur et les ordinateurs de votre atelier</span><span class="sxs-lookup"><span data-stu-id="924ff-115">Set up your lab server and computers</span></span>
- <span data-ttu-id="924ff-116">Configurer Active Directory avec des utilisateurs et des groupes</span><span class="sxs-lookup"><span data-stu-id="924ff-116">Configure Active Directory with users and groups</span></span>
- <span data-ttu-id="924ff-117">Configurer Microsoft Defender pour l’identité, Microsoft Defender pour Office 365, Microsoft Defender pour le point de terminaison et Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="924ff-117">Set up and configure Microsoft Defender for Identity, Microsoft Defender for Office 365, Microsoft Defender for Endpoint, and Microsoft Cloud App Security</span></span>
- <span data-ttu-id="924ff-118">Configurer des stratégies locales pour votre serveur et vos ordinateurs</span><span class="sxs-lookup"><span data-stu-id="924ff-118">Set up local policies for your server and computers</span></span>
- <span data-ttu-id="924ff-119">Simuler une attaque contre une menace pour générer un incident de test ou une alerte dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="924ff-119">Mimic a threat attack to generate a test incident or alert in Microsoft 365 Defender</span></span>

>[!IMPORTANT]
><span data-ttu-id="924ff-120">Pour obtenir des résultats optimaux, suivez les instructions de configuration de l’atelier aussi étroitement que possible.</span><span class="sxs-lookup"><span data-stu-id="924ff-120">For optimum results, follow the lab setup instructions as closely as possible.</span></span>


## <a name="deployment-phases"></a><span data-ttu-id="924ff-121">Phases de déploiement</span><span class="sxs-lookup"><span data-stu-id="924ff-121">Deployment phases</span></span>

<span data-ttu-id="924ff-122">La création d’un environnement de laboratoire d’essai Microsoft 365 Defender se fait en trois phases.</span><span class="sxs-lookup"><span data-stu-id="924ff-122">There are three phases in creating a Microsoft 365 Defender trial lab environment.</span></span>

![Phases de déploiement : préparer, configurer, intégrer](../../media/evaluation-guide-phases.png)

|<span data-ttu-id="924ff-124">Phase</span><span class="sxs-lookup"><span data-stu-id="924ff-124">Phase</span></span> | <span data-ttu-id="924ff-125">Description</span><span class="sxs-lookup"><span data-stu-id="924ff-125">Description</span></span> | 
|:-------|:-----|
|[<span data-ttu-id="924ff-126">Phase 1 : Préparer</span><span class="sxs-lookup"><span data-stu-id="924ff-126">Phase 1: Prepare</span></span>](prepare-mtpeval.md)| <span data-ttu-id="924ff-127">Découvrez ce que vous devez prendre en compte lors du déploiement de Microsoft 365 Defender dans un laboratoire d’essai ou un environnement pilote :</span><span class="sxs-lookup"><span data-stu-id="924ff-127">Learn what you need to consider when deploying Microsoft 365 Defender in a trial lab or pilot environment:</span></span> <br><br><span data-ttu-id="924ff-128">- Parties prenantes et sign-off</span><span class="sxs-lookup"><span data-stu-id="924ff-128">- Stakeholders and sign-off</span></span> <br> <span data-ttu-id="924ff-129">- Considérations sur l’environnement</span><span class="sxs-lookup"><span data-stu-id="924ff-129">- Environment considerations</span></span> <br><span data-ttu-id="924ff-130">- Access</span><span class="sxs-lookup"><span data-stu-id="924ff-130">- Access</span></span> <br><span data-ttu-id="924ff-131">- Configuration d’Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="924ff-131">- Azure Active Directory setup</span></span> <br> <span data-ttu-id="924ff-132">- Ordre de configuration</span><span class="sxs-lookup"><span data-stu-id="924ff-132">- Configuration order</span></span>
|[<span data-ttu-id="924ff-133">Phase 2 : Installation</span><span class="sxs-lookup"><span data-stu-id="924ff-133">Phase 2: Setup</span></span>](setup-mtpeval.md)|  <span data-ttu-id="924ff-134">Prenez les étapes initiales pour accéder au Centre de sécurité Microsoft 365 afin de configurer votre laboratoire d’évaluation ou votre environnement pilote Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="924ff-134">Take the initial steps to access Microsoft 365 Security Center to set up your Microsoft 365 Defender trial lab or pilot environment.</span></span> <span data-ttu-id="924ff-135">Vous serez guidé vers :</span><span class="sxs-lookup"><span data-stu-id="924ff-135">You'll be guided to:</span></span><br><br><span data-ttu-id="924ff-136">- S’inscrire à la version d’essai de Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="924ff-136">- Sign up for Microsoft 365 E5 Trial</span></span> <br>  <span data-ttu-id="924ff-137">- Configurer un domaine</span><span class="sxs-lookup"><span data-stu-id="924ff-137">- Configure domain</span></span><br><span data-ttu-id="924ff-138">- Attribuer des licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="924ff-138">- Assign Microsoft 365 E5 licenses</span></span><br><span data-ttu-id="924ff-139">- Terminer l’Assistant Installation dans le portail</span><span class="sxs-lookup"><span data-stu-id="924ff-139">- Complete the setup wizard in the portal</span></span>|
|[<span data-ttu-id="924ff-140">Phase 3 : Configurer & intégré</span><span class="sxs-lookup"><span data-stu-id="924ff-140">Phase 3: Configure & Onboard</span></span>](config-mtpeval.md) | <span data-ttu-id="924ff-141">Configurez chaque pilier microsoft 365 Defender et les points de terminaison intégrés.</span><span class="sxs-lookup"><span data-stu-id="924ff-141">Configure each Microsoft 365 Defender pillar and onboard endpoints.</span></span> <span data-ttu-id="924ff-142">Vous serez guidé vers :</span><span class="sxs-lookup"><span data-stu-id="924ff-142">You'll be guided to:</span></span><br><br><span data-ttu-id="924ff-143">- Configurer Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="924ff-143">- Configure Microsoft Defender for Office 365</span></span><br><span data-ttu-id="924ff-144">- Configurer Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="924ff-144">- Configure Microsoft Cloud App Security</span></span><br><span data-ttu-id="924ff-145">- Configurer Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="924ff-145">- Configure Microsoft Defender for Identity</span></span><br><span data-ttu-id="924ff-146">- Configurer Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="924ff-146">- Configure Microsoft Defender for Endpoint</span></span>


<span data-ttu-id="924ff-147">Une fois ce guide terminé, vous avez identifié les parties prenantes impliquées et les approbations requises, vous avez les autorisations d’accès nécessaires, vous êtes inscrit à la version d’évaluation, vous avez configuré les domaines et chacun des piliers de Microsoft 365 Defender, et vos points de terminaison sont intégrés au service.</span><span class="sxs-lookup"><span data-stu-id="924ff-147">After you've completed this guide, you would have identified the stakeholders involved and the required approvals,  have the right access permissions, signed up for trial, configured domains and each of the Microsoft 365 Defender pillars, and your endpoints will be onboarded to the service.</span></span>

## <a name="key-capabilities"></a><span data-ttu-id="924ff-148">Fonctionnalités clés</span><span class="sxs-lookup"><span data-stu-id="924ff-148">Key capabilities</span></span>

<span data-ttu-id="924ff-149">Bien que Microsoft 365 Defender offre de nombreuses fonctionnalités, l’objectif principal de ce guide de déploiement est de vous aider à commencer par l’intégration d’appareils.</span><span class="sxs-lookup"><span data-stu-id="924ff-149">While Microsoft 365 Defender provides many capabilities, the primary purpose of this deployment guide is to get you started by onboarding devices.</span></span> <span data-ttu-id="924ff-150">En plus de l’intégration, ces conseils vous guident avec les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="924ff-150">In addition to onboarding, this guidance gets you started with the following capabilities.</span></span>


<span data-ttu-id="924ff-151">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="924ff-151">Capability</span></span> | <span data-ttu-id="924ff-152">Description</span><span class="sxs-lookup"><span data-stu-id="924ff-152">Description</span></span> 
:---|:---
<span data-ttu-id="924ff-153">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="924ff-153">Microsoft Defender for Office 365</span></span> | <span data-ttu-id="924ff-154">Permet de protéger l’ensemble de votre système Office 365 contre les menaces actuelles</span><span class="sxs-lookup"><span data-stu-id="924ff-154">Helps protect your entire Office 365 envrionment from today's threats</span></span>
<span data-ttu-id="924ff-155">Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="924ff-155">Microsoft Defender for Identity</span></span> | <span data-ttu-id="924ff-156">Identifie et détecte les menaces sur les identités compromises et les actions internes malveillantes.</span><span class="sxs-lookup"><span data-stu-id="924ff-156">Identifies and detects  threats on compromised identities and malicious insider actions.</span></span>
<span data-ttu-id="924ff-157">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="924ff-157">Microsoft Cloud App Security</span></span> | <span data-ttu-id="924ff-158">Fournit une visibilité enrichie, contrôle les déplacements de données et détecte les cybermenaces dans les services cloud.</span><span class="sxs-lookup"><span data-stu-id="924ff-158">Provides rich visibility, control data travel, and detect cyberthreats across cloud services.</span></span>
<span data-ttu-id="924ff-159">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="924ff-159">Microsoft Defender for Endpoint</span></span> | <span data-ttu-id="924ff-160">Empêche, détecte et fournit des fonctionnalités de réponse aux menaces avancées avec une sécurité complète des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="924ff-160">Prevents, detects, and provides response capabilities to advanced threats with comprehensive endpoint security.</span></span>


## <a name="in-scope"></a><span data-ttu-id="924ff-161">Dans l’étendue</span><span class="sxs-lookup"><span data-stu-id="924ff-161">In scope</span></span>

<span data-ttu-id="924ff-162">Les tâches suivantes sont dans l’étendue de ce guide :</span><span class="sxs-lookup"><span data-stu-id="924ff-162">The following tasks are in scope for this guide:</span></span>
-   <span data-ttu-id="924ff-163">Configurer Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="924ff-163">Set up Azure Active Directory</span></span>
-   <span data-ttu-id="924ff-164">Configurer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="924ff-164">Set up Microsoft 365 Defender</span></span>
    -   <span data-ttu-id="924ff-165">S’inscrire à la version d’essai de Microsoft 365 E5 ou utiliser votre licence complète si vous exécutez un pilote</span><span class="sxs-lookup"><span data-stu-id="924ff-165">Sign up for Microsoft 365 E5 Trial or use your full license if you're running a pilot</span></span>
    -   <span data-ttu-id="924ff-166">Configurer un domaine</span><span class="sxs-lookup"><span data-stu-id="924ff-166">Configure domain</span></span>
    -   <span data-ttu-id="924ff-167">Attribuer des licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="924ff-167">Assign Microsoft 365 E5 licenses</span></span>
    -   <span data-ttu-id="924ff-168">Fin de l’Assistant Installation dans le portail</span><span class="sxs-lookup"><span data-stu-id="924ff-168">Completing the setup wizard within the portal</span></span>
-   <span data-ttu-id="924ff-169">Configurer tous les piliers de Microsoft 365 Defender en fonction des meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="924ff-169">Configure all Microsoft 365 Defender pillars based on best practices</span></span>
    -   <span data-ttu-id="924ff-170">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="924ff-170">Microsoft Defender for Office 365</span></span>
    -   <span data-ttu-id="924ff-171">Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="924ff-171">Microsoft Defender for Identity</span></span>
    -   <span data-ttu-id="924ff-172">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="924ff-172">Microsoft Cloud App Security</span></span>
    -   <span data-ttu-id="924ff-173">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="924ff-173">Microsoft Defender for Endpoint</span></span>

## <a name="out-of-scope"></a><span data-ttu-id="924ff-174">Non compris</span><span class="sxs-lookup"><span data-stu-id="924ff-174">Out of scope</span></span>

<span data-ttu-id="924ff-175">Ce guide de déploiement n’entre pas dans le cadre de ce guide de déploiement :</span><span class="sxs-lookup"><span data-stu-id="924ff-175">The following are out of scope of this deployment guide:</span></span>

-   <span data-ttu-id="924ff-176">Configuration de solutions tierces qui peuvent s’intégrer à Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="924ff-176">Configuration of third-party solutions that might integrate with Microsoft 365 Defender</span></span>
-   <span data-ttu-id="924ff-177">Test de pénétration dans un environnement de production</span><span class="sxs-lookup"><span data-stu-id="924ff-177">Penetration testing in production environment</span></span>

## <a name="next-step"></a><span data-ttu-id="924ff-178">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="924ff-178">Next step</span></span>
<span data-ttu-id="924ff-179">[Phase 1 : Préparer](prepare-mtpeval.md) 
</span><span class="sxs-lookup"><span data-stu-id="924ff-179">[Phase 1: Prepare](prepare-mtpeval.md) 
</span></span><br> <span data-ttu-id="924ff-180">Préparer votre laboratoire d’essai ou votre environnement pilote Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="924ff-180">Prepare your Microsoft 365 Defender trial lab or pilot environment</span></span>
