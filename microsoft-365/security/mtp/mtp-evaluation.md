---
title: Évaluation de Microsoft 365 Defender
description: Configurez votre laboratoire de test Microsoft 365 Defender ou votre environnement pilote pour tester et tester la solution de sécurité conçue pour protéger les périphériques, l’identité, les données et les applications de votre organisation.
keywords: Version d’évaluation de la protection de Microsoft contre les menaces, essayez Microsoft Threat Protection, évaluez Microsoft Threat Protection, l’atelier d’évaluation de Microsoft Threat Protection, Microsoft Threat Protection Pilot, Cyber Security, Advanced persistent, Enterprise Security, appareils, Device, Identity, Users, Data, applications, incidents, analyse automatisée et correction, recherche avancée
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
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
ms.openlocfilehash: 8504b036203e1f73dc9e0a0d79a228425fb88bfa
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49659632"
---
# <a name="create-a-microsoft-365-defender-trial-lab-or-pilot-environment"></a><span data-ttu-id="b827e-104">Création d’un laboratoire d’évaluation ou d’un environnement pilote Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b827e-104">Create a Microsoft 365 Defender trial lab or pilot environment</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="b827e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b827e-105">**Applies to:**</span></span>
- <span data-ttu-id="b827e-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b827e-106">Microsoft 365 Defender</span></span>


<span data-ttu-id="b827e-107">Ce guide vous aide à configurer un environnement de laboratoire avec des utilisateurs et des groupes, puis vous guide tout au long de la configuration des fonctionnalités dans Microsoft 365 Defender afin que vous puissiez imiter une attaque de menace et obtenir un résultat d’évaluation significatif.</span><span class="sxs-lookup"><span data-stu-id="b827e-107">This guide helps you work across setting up a lab environment with users and groups, then guides you through the configuration of the capabilities in Microsoft 365 Defender so that you can mimic a threat attack and obtain a meaningful trial result.</span></span> 

<span data-ttu-id="b827e-108">L’objectif de la création de ce laboratoire d’évaluation ou de cet environnement pilote est d’illustrer les fonctionnalités complètes et intégrées de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="b827e-108">The purpose of creating this trial lab or pilot environment is to illustrate the comprehensive and integrated Microsoft 365 Defender capabilities.</span></span> <span data-ttu-id="b827e-109">Découvrez comment cette solution de sécurité intelligente détecte, empêche, recherche automatiquement les menaces avancées de votre organisation et y répond.</span><span class="sxs-lookup"><span data-stu-id="b827e-109">Experience how this intelligent security solution detects, prevents, automatically investigates, and responds to advanced threats your organization.</span></span> 


<span data-ttu-id="b827e-110">Vous serez guidé lors de la procédure de démarrage de votre évaluation de Microsoft 365 Defender en fonction des chemins de déploiement recommandés.</span><span class="sxs-lookup"><span data-stu-id="b827e-110">You will be guided through the steps to start your Microsoft 365 Defender evaluation based on the recommended deployment paths.</span></span> <span data-ttu-id="b827e-111">L’objectif est de vous aider à configurer la solution de sécurité dans un environnement de laboratoire avec un compte d’évaluation ou dans un environnement pilote en production avec une licence complète.</span><span class="sxs-lookup"><span data-stu-id="b827e-111">The goal is to help you set up the security solution either in a lab environment with a trial account, or in a pilot environment in production with a full license.</span></span> <span data-ttu-id="b827e-112">La préparation de votre laboratoire d’évaluation ou de votre environnement pilote peut vous aider à présenter des cas d’utilisation des opérations de sécurité pour les décideurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b827e-112">Preparing your trial lab or pilot environment can help you present security operation use cases to decision makers in your organization.</span></span> <span data-ttu-id="b827e-113">Lorsque vous avez terminé d’exécuter vos simulations d’attaque et que vous êtes satisfait du résultat, vous pouvez le déployer et l’utiliser entièrement dans votre organisation à l’aide des professionnels techniques ou des experts de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b827e-113">When you’re done running your attack simulations and are satisfied with the results, you can fully deploy and operationalize it in your organization with the help of Microsoft Technical Sales Professionals or experts in your organization.</span></span> 

<span data-ttu-id="b827e-114">Ce guide vous aidera à :</span><span class="sxs-lookup"><span data-stu-id="b827e-114">This guide will help you:</span></span>
- <span data-ttu-id="b827e-115">Configurer le serveur et les ordinateurs de l’atelier</span><span class="sxs-lookup"><span data-stu-id="b827e-115">Set up your lab server and computers</span></span>
- <span data-ttu-id="b827e-116">Configurer Active Directory avec des utilisateurs et des groupes</span><span class="sxs-lookup"><span data-stu-id="b827e-116">Configure Active Directory with users and groups</span></span>
- <span data-ttu-id="b827e-117">Installer et configurer Microsoft Defender pour l’identité, Microsoft Defender pour Office 365, Microsoft Defender pour le point de terminaison et sécurité des applications Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="b827e-117">Set up and configure Microsoft Defender for Identity, Microsoft Defender for Office 365, Microsoft Defender for Endpoint, and Microsoft Cloud App Security</span></span>
- <span data-ttu-id="b827e-118">Configurer des stratégies locales pour votre serveur et vos ordinateurs</span><span class="sxs-lookup"><span data-stu-id="b827e-118">Set up local policies for your server and computers</span></span>
- <span data-ttu-id="b827e-119">Imiter une attaque de menace pour générer un incident ou une alerte de test dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b827e-119">Mimic a threat attack to generate a test incident or alert in Microsoft 365 Defender</span></span>

>[!IMPORTANT]
><span data-ttu-id="b827e-120">Pour obtenir des résultats optimaux, suivez autant que possible les instructions de configuration de l’atelier.</span><span class="sxs-lookup"><span data-stu-id="b827e-120">For optimum results, follow the lab setup instructions as closely as possible.</span></span>


## <a name="deployment-phases"></a><span data-ttu-id="b827e-121">Phases de déploiement</span><span class="sxs-lookup"><span data-stu-id="b827e-121">Deployment phases</span></span>

<span data-ttu-id="b827e-122">Il existe trois phases pour créer un environnement de laboratoire de test Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="b827e-122">There are three phases in creating a Microsoft 365 Defender trial lab environment.</span></span>

![Phases de déploiement : Prepare, Setup, Onboard](../../media/evaluation-guide-phases.png)

|<span data-ttu-id="b827e-124">Phase</span><span class="sxs-lookup"><span data-stu-id="b827e-124">Phase</span></span> | <span data-ttu-id="b827e-125">Description</span><span class="sxs-lookup"><span data-stu-id="b827e-125">Description</span></span> | 
|:-------|:-----|
|[<span data-ttu-id="b827e-126">Phase 1 : préparer</span><span class="sxs-lookup"><span data-stu-id="b827e-126">Phase 1: Prepare</span></span>](prepare-mtpeval.md)| <span data-ttu-id="b827e-127">Découvrez ce que vous devez prendre en compte lors du déploiement de Microsoft 365 Defender dans un laboratoire d’évaluation ou un environnement pilote :</span><span class="sxs-lookup"><span data-stu-id="b827e-127">Learn what you need to consider when deploying Microsoft 365 Defender in a trial lab or pilot environment:</span></span> <br><br><span data-ttu-id="b827e-128">-Parties prenantes et déconnexion</span><span class="sxs-lookup"><span data-stu-id="b827e-128">- Stakeholders and sign-off</span></span> <br> <span data-ttu-id="b827e-129">-Considérations sur l’environnement</span><span class="sxs-lookup"><span data-stu-id="b827e-129">- Environment considerations</span></span> <br><span data-ttu-id="b827e-130">-Accès</span><span class="sxs-lookup"><span data-stu-id="b827e-130">- Access</span></span> <br><span data-ttu-id="b827e-131">-Installation d’Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b827e-131">- Azure Active Directory setup</span></span> <br> <span data-ttu-id="b827e-132">-Ordre de configuration</span><span class="sxs-lookup"><span data-stu-id="b827e-132">- Configuration order</span></span>
|[<span data-ttu-id="b827e-133">Phase 2 : configuration</span><span class="sxs-lookup"><span data-stu-id="b827e-133">Phase 2: Setup</span></span>](setup-mtpeval.md)|  <span data-ttu-id="b827e-134">Suivez les étapes initiales pour accéder au centre de sécurité Microsoft 365 afin de configurer votre laboratoire d’évaluation ou votre environnement pilote Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="b827e-134">Take the initial steps to access Microsoft 365 Security Center to set up your Microsoft 365 Defender trial lab or pilot environment.</span></span> <span data-ttu-id="b827e-135">Vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="b827e-135">You'll be guided to:</span></span><br><br><span data-ttu-id="b827e-136">-Inscrivez-vous à la version d’évaluation de Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="b827e-136">- Sign up for Microsoft 365 E5 Trial</span></span> <br>  <span data-ttu-id="b827e-137">-Configurer le domaine</span><span class="sxs-lookup"><span data-stu-id="b827e-137">- Configure domain</span></span><br><span data-ttu-id="b827e-138">-Affecter les licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="b827e-138">- Assign Microsoft 365 E5 licenses</span></span><br><span data-ttu-id="b827e-139">-Exécutez l’Assistant Installation dans le portail.</span><span class="sxs-lookup"><span data-stu-id="b827e-139">- Complete the setup wizard in the portal</span></span>|
|[<span data-ttu-id="b827e-140">Phase 3 : configurer & Onboard</span><span class="sxs-lookup"><span data-stu-id="b827e-140">Phase 3: Configure & Onboard</span></span>](config-mtpeval.md) | <span data-ttu-id="b827e-141">Configurez chaque pilier Microsoft 365 Defender et les points de terminaison intégrés.</span><span class="sxs-lookup"><span data-stu-id="b827e-141">Configure each Microsoft 365 Defender pillar and onboard endpoints.</span></span> <span data-ttu-id="b827e-142">Vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="b827e-142">You'll be guided to:</span></span><br><br><span data-ttu-id="b827e-143">-Configurer Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="b827e-143">- Configure Microsoft Defender for Office 365</span></span><br><span data-ttu-id="b827e-144">-Configurer la sécurité des applications Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="b827e-144">- Configure Microsoft Cloud App Security</span></span><br><span data-ttu-id="b827e-145">-Configurer Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="b827e-145">- Configure Microsoft Defender for Identity</span></span><br><span data-ttu-id="b827e-146">-Configurer Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b827e-146">- Configure Microsoft Defender for Endpoint</span></span>


<span data-ttu-id="b827e-147">Une fois que vous avez terminé ce guide, vous auriez identifié les parties prenantes impliquées et les approbations requises, disposez des autorisations d’accès appropriées, inscrites pour les domaines configurés et chacun des piliers de Microsoft 365 Defender, et vos points de terminaison seront intégrés au service.</span><span class="sxs-lookup"><span data-stu-id="b827e-147">After you've completed this guide, you would have identified the stakeholders involved and the required approvals,  have the right access permissions, signed up for trial, configured domains and each of the Microsoft 365 Defender pillars, and your endpoints will be onboarded to the service.</span></span>

## <a name="key-capabilities"></a><span data-ttu-id="b827e-148">Fonctionnalités clés</span><span class="sxs-lookup"><span data-stu-id="b827e-148">Key capabilities</span></span>

<span data-ttu-id="b827e-149">Bien que Microsoft 365 Defender offre de nombreuses fonctionnalités, l’objectif principal de ce guide de déploiement est de vous aider à commencer par les appareils d’intégration.</span><span class="sxs-lookup"><span data-stu-id="b827e-149">While Microsoft 365 Defender provides many capabilities, the primary purpose of this deployment guide is to get you started by onboarding devices.</span></span> <span data-ttu-id="b827e-150">En plus de l’intégration, ces instructions vous permettent de commencer à utiliser les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="b827e-150">In addition to onboarding, this guidance gets you started with the following capabilities.</span></span>


<span data-ttu-id="b827e-151">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="b827e-151">Capability</span></span> | <span data-ttu-id="b827e-152">Description</span><span class="sxs-lookup"><span data-stu-id="b827e-152">Description</span></span> 
:---|:---
<span data-ttu-id="b827e-153">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="b827e-153">Microsoft Defender for Office 365</span></span> | <span data-ttu-id="b827e-154">Permet de protéger l’ensemble de votre environnement Office 365 des menaces actuelles</span><span class="sxs-lookup"><span data-stu-id="b827e-154">Helps protect your entire Office 365 envrionment from today's threats</span></span>
<span data-ttu-id="b827e-155">Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="b827e-155">Microsoft Defender for Identity</span></span> | <span data-ttu-id="b827e-156">Identifie et détecte les menaces liées aux identités compromises et aux actions malveillantes.</span><span class="sxs-lookup"><span data-stu-id="b827e-156">Identifies and detects  threats on compromised identities and malicious insider actions.</span></span>
<span data-ttu-id="b827e-157">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b827e-157">Microsoft Cloud App Security</span></span> | <span data-ttu-id="b827e-158">Offre une visibilité enrichie, un contrôle des déplacements de données et la détection des cyber dans les services Cloud.</span><span class="sxs-lookup"><span data-stu-id="b827e-158">Provides rich visibility, control data travel, and detect cyberthreats across cloud services.</span></span>
<span data-ttu-id="b827e-159">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b827e-159">Microsoft Defender for Endpoint</span></span> | <span data-ttu-id="b827e-160">Empêche, détecte et offre des fonctionnalités de réponse aux menaces avancées avec une sécurité de point de terminaison complète.</span><span class="sxs-lookup"><span data-stu-id="b827e-160">Prevents, detects, and provides response capabilities to advanced threats with comprehensive endpoint security.</span></span>


## <a name="in-scope"></a><span data-ttu-id="b827e-161">Dans l’étendue</span><span class="sxs-lookup"><span data-stu-id="b827e-161">In scope</span></span>

<span data-ttu-id="b827e-162">Les tâches suivantes sont dans l’étendue de ce guide :</span><span class="sxs-lookup"><span data-stu-id="b827e-162">The following tasks are in scope for this guide:</span></span>
-   <span data-ttu-id="b827e-163">Configurer Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b827e-163">Set up Azure Active Directory</span></span>
-   <span data-ttu-id="b827e-164">Configurer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b827e-164">Set up Microsoft 365 Defender</span></span>
    -   <span data-ttu-id="b827e-165">Inscrivez-vous à la version d’évaluation de Microsoft 365 E5 ou utilisez votre licence complète si vous exécutez un projet pilote.</span><span class="sxs-lookup"><span data-stu-id="b827e-165">Sign up for Microsoft 365 E5 Trial or use your full license if you're running a pilot</span></span>
    -   <span data-ttu-id="b827e-166">Configurer le domaine</span><span class="sxs-lookup"><span data-stu-id="b827e-166">Configure domain</span></span>
    -   <span data-ttu-id="b827e-167">Affecter des licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="b827e-167">Assign Microsoft 365 E5 licenses</span></span>
    -   <span data-ttu-id="b827e-168">Fin de l’Assistant Installation dans le portail</span><span class="sxs-lookup"><span data-stu-id="b827e-168">Completing the setup wizard within the portal</span></span>
-   <span data-ttu-id="b827e-169">Configurer tous les piliers de Microsoft 365 Defender en fonction des meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="b827e-169">Configure all Microsoft 365 Defender pillars based on best practices</span></span>
    -   <span data-ttu-id="b827e-170">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="b827e-170">Microsoft Defender for Office 365</span></span>
    -   <span data-ttu-id="b827e-171">Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="b827e-171">Microsoft Defender for Identity</span></span>
    -   <span data-ttu-id="b827e-172">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b827e-172">Microsoft Cloud App Security</span></span>
    -   <span data-ttu-id="b827e-173">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b827e-173">Microsoft Defender for Endpoint</span></span>

## <a name="out-of-scope"></a><span data-ttu-id="b827e-174">Non compris</span><span class="sxs-lookup"><span data-stu-id="b827e-174">Out of scope</span></span>

<span data-ttu-id="b827e-175">Ce guide de déploiement ne comporte pas les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b827e-175">The following are out of scope of this deployment guide:</span></span>

-   <span data-ttu-id="b827e-176">Configuration de solutions tierces qui peuvent s’intégrer à Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b827e-176">Configuration of third-party solutions that might integrate with Microsoft 365 Defender</span></span>
-   <span data-ttu-id="b827e-177">Test de pénétration dans l’environnement de production</span><span class="sxs-lookup"><span data-stu-id="b827e-177">Penetration testing in production environment</span></span>

## <a name="next-step"></a><span data-ttu-id="b827e-178">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="b827e-178">Next step</span></span>
<span data-ttu-id="b827e-179">[Phase 1 : préparer](prepare-mtpeval.md) 
</span><span class="sxs-lookup"><span data-stu-id="b827e-179">[Phase 1: Prepare](prepare-mtpeval.md) 
</span></span><br> <span data-ttu-id="b827e-180">Préparation de votre laboratoire d’évaluation ou de votre environnement pilote Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b827e-180">Prepare your Microsoft 365 Defender trial lab or pilot environment</span></span>
