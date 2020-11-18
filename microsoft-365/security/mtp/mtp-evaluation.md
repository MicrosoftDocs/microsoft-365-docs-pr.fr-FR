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
ms.openlocfilehash: fe0a06dd104f0f0532363ee046f4bad1c03c5400
ms.sourcegitcommit: ce46d1bd67091d4ed0e2b776dfed55e2d88cdbf4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49130893"
---
# <a name="create-a-microsoft-365-defender-trial-lab-or-pilot-environment"></a><span data-ttu-id="0eb9a-104">Création d’un laboratoire d’évaluation ou d’un environnement pilote Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0eb9a-104">Create a Microsoft 365 Defender trial lab or pilot environment</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="0eb9a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0eb9a-105">**Applies to:**</span></span>
- <span data-ttu-id="0eb9a-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0eb9a-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="0eb9a-107">L’objectif de la création de ce laboratoire d’évaluation ou de cet environnement pilote est d’illustrer les fonctionnalités complètes et intégrées de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="0eb9a-107">The purpose of creating this trial lab or pilot environment is to illustrate the comprehensive and integrated Microsoft 365 Defender capabilities.</span></span> <span data-ttu-id="0eb9a-108">Découvrez comment cette solution de sécurité intelligente détecte, empêche, recherche automatiquement les menaces avancées de votre organisation et y répond.</span><span class="sxs-lookup"><span data-stu-id="0eb9a-108">Experience how this intelligent security solution detects, prevents, automatically investigates, and responds to advanced threats your organization.</span></span> 

<span data-ttu-id="0eb9a-109">Ce guide décrit les étapes à suivre pour démarrer votre évaluation de Microsoft 365 Defender en fonction des chemins de déploiement recommandés.</span><span class="sxs-lookup"><span data-stu-id="0eb9a-109">This guide takes you through the steps to start your Microsoft 365 Defender evaluation based on the recommended deployment paths.</span></span> <span data-ttu-id="0eb9a-110">L’objectif est de vous aider à configurer la solution de sécurité dans un environnement de laboratoire avec un compte d’évaluation ou dans un environnement pilote en production avec une licence complète.</span><span class="sxs-lookup"><span data-stu-id="0eb9a-110">The goal is to help you set up the security solution either in a lab environment with a trial account, or in a pilot environment in production with a full license.</span></span> <span data-ttu-id="0eb9a-111">La préparation de votre laboratoire d’évaluation ou de votre environnement pilote peut vous aider à présenter des cas d’utilisation des opérations de sécurité pour les décideurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0eb9a-111">Preparing your trial lab or pilot environment can help you present security operation use cases to decision makers in your organization.</span></span> <span data-ttu-id="0eb9a-112">Lorsque vous avez terminé d’exécuter vos simulations d’attaque et que vous êtes satisfait du résultat, vous pouvez le déployer et l’utiliser entièrement dans votre organisation à l’aide des professionnels techniques ou des experts de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0eb9a-112">When you’re done running your attack simulations and are satisfied with the results, you can fully deploy and operationalize it in your organization with the help of Microsoft Technical Sales Professionals or experts in your organization.</span></span> 

<span data-ttu-id="0eb9a-113">Ce guide vous aidera à :</span><span class="sxs-lookup"><span data-stu-id="0eb9a-113">This guide will help you:</span></span>
- <span data-ttu-id="0eb9a-114">Configurer le serveur et les ordinateurs de l’atelier</span><span class="sxs-lookup"><span data-stu-id="0eb9a-114">Set up your lab server and computers</span></span>
- <span data-ttu-id="0eb9a-115">Configurer Active Directory avec des utilisateurs et des groupes</span><span class="sxs-lookup"><span data-stu-id="0eb9a-115">Configure Active Directory with users and groups</span></span>
- <span data-ttu-id="0eb9a-116">Installer et configurer Microsoft Defender pour l’identité, Microsoft Defender pour Office 365, Microsoft Defender pour le point de terminaison et sécurité des applications Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="0eb9a-116">Set up and configure Microsoft Defender for Identity, Microsoft Defender for Office 365, Microsoft Defender for Endpoint, and Microsoft Cloud App Security</span></span>
- <span data-ttu-id="0eb9a-117">Configurer des stratégies locales pour votre serveur et vos ordinateurs</span><span class="sxs-lookup"><span data-stu-id="0eb9a-117">Set up local policies for your server and computers</span></span>
- <span data-ttu-id="0eb9a-118">Imiter une attaque de menace pour générer un incident ou une alerte de test dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0eb9a-118">Mimic a threat attack to generate a test incident or alert in Microsoft 365 Defender</span></span>

>[!IMPORTANT]
><span data-ttu-id="0eb9a-119">Pour obtenir des résultats optimaux, suivez autant que possible les instructions de configuration de l’atelier.</span><span class="sxs-lookup"><span data-stu-id="0eb9a-119">For optimum results, follow the lab setup instructions as closely as possible.</span></span>


## <a name="deployment-phases"></a><span data-ttu-id="0eb9a-120">Phases de déploiement</span><span class="sxs-lookup"><span data-stu-id="0eb9a-120">Deployment phases</span></span>

<span data-ttu-id="0eb9a-121">Il existe trois phases pour créer un environnement de laboratoire de test Microsoft 365 Defender et le déployer :</span><span class="sxs-lookup"><span data-stu-id="0eb9a-121">There are three phases in creating a Microsoft 365 Defender trial lab environment and deploying it:</span></span>

![Phases de déploiement : Prepare, Setup, Onboard](../../media/phase-diagrams/deployment-phases.png)

|<span data-ttu-id="0eb9a-123">Phase</span><span class="sxs-lookup"><span data-stu-id="0eb9a-123">Phase</span></span> | <span data-ttu-id="0eb9a-124">Description</span><span class="sxs-lookup"><span data-stu-id="0eb9a-124">Description</span></span> | 
|:-------|:-----|
|[<span data-ttu-id="0eb9a-125">Phase 1 : préparer</span><span class="sxs-lookup"><span data-stu-id="0eb9a-125">Phase 1: Prepare</span></span>](prepare-mtpeval.md)| <span data-ttu-id="0eb9a-126">Découvrez ce que vous devez prendre en compte lors du déploiement de Microsoft 365 Defender dans un laboratoire d’évaluation ou un environnement pilote :</span><span class="sxs-lookup"><span data-stu-id="0eb9a-126">Learn what you need to consider when deploying Microsoft 365 Defender in a trial lab or pilot environment:</span></span> <br><br><span data-ttu-id="0eb9a-127">-Parties prenantes et déconnexion</span><span class="sxs-lookup"><span data-stu-id="0eb9a-127">- Stakeholders and sign-off</span></span> <br> <span data-ttu-id="0eb9a-128">-Considérations sur l’environnement</span><span class="sxs-lookup"><span data-stu-id="0eb9a-128">- Environment considerations</span></span> <br><span data-ttu-id="0eb9a-129">-Accès</span><span class="sxs-lookup"><span data-stu-id="0eb9a-129">- Access</span></span> <br><span data-ttu-id="0eb9a-130">-Installation d’Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="0eb9a-130">- Azure Active Directory setup</span></span> <br> <span data-ttu-id="0eb9a-131">-Ordre de configuration</span><span class="sxs-lookup"><span data-stu-id="0eb9a-131">- Configuration order</span></span>
|[<span data-ttu-id="0eb9a-132">Phase 2 : configuration</span><span class="sxs-lookup"><span data-stu-id="0eb9a-132">Phase 2: Setup</span></span>](setup-mtpeval.md)|  <span data-ttu-id="0eb9a-133">Suivez les étapes initiales pour accéder au centre de sécurité Microsoft 365 afin de configurer votre laboratoire d’évaluation ou votre environnement pilote Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="0eb9a-133">Take the initial steps to access Microsoft 365 Security Center to set up your Microsoft 365 Defender trial lab or pilot environment.</span></span> <span data-ttu-id="0eb9a-134">Vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="0eb9a-134">You'll be guided to:</span></span><br><br><span data-ttu-id="0eb9a-135">-Inscrivez-vous à la version d’évaluation de Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="0eb9a-135">- Sign up for Microsoft 365 E5 Trial</span></span> <br>  <span data-ttu-id="0eb9a-136">-Configurer le domaine</span><span class="sxs-lookup"><span data-stu-id="0eb9a-136">- Configure domain</span></span><br><span data-ttu-id="0eb9a-137">-Affecter les licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="0eb9a-137">- Assign Microsoft 365 E5 licenses</span></span><br><span data-ttu-id="0eb9a-138">-Exécutez l’Assistant Installation dans le portail.</span><span class="sxs-lookup"><span data-stu-id="0eb9a-138">- Complete the setup wizard in the portal</span></span>|
|[<span data-ttu-id="0eb9a-139">Phase 3 : configurer & Onboard</span><span class="sxs-lookup"><span data-stu-id="0eb9a-139">Phase 3: Configure & Onboard</span></span>](config-mtpeval.md) | <span data-ttu-id="0eb9a-140">Configurez chaque pilier Microsoft 365 Defender et les points de terminaison intégrés.</span><span class="sxs-lookup"><span data-stu-id="0eb9a-140">Configure each Microsoft 365 Defender pillar and onboard endpoints.</span></span> <span data-ttu-id="0eb9a-141">Vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="0eb9a-141">You'll be guided to:</span></span><br><br><span data-ttu-id="0eb9a-142">-Configurer Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="0eb9a-142">- Configure Microsoft Defender for Office 365</span></span><br><span data-ttu-id="0eb9a-143">-Configurer la sécurité des applications Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="0eb9a-143">- Configure Microsoft Cloud App Security</span></span><br><span data-ttu-id="0eb9a-144">-Configurer Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="0eb9a-144">- Configure Microsoft Defender for Identity</span></span><br><span data-ttu-id="0eb9a-145">-Configurer Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0eb9a-145">- Configure Microsoft Defender for Endpoint</span></span>


## <a name="in-scope"></a><span data-ttu-id="0eb9a-146">Dans l’étendue</span><span class="sxs-lookup"><span data-stu-id="0eb9a-146">In scope</span></span>

<span data-ttu-id="0eb9a-147">Les tâches suivantes sont dans l’étendue de ce guide :</span><span class="sxs-lookup"><span data-stu-id="0eb9a-147">The following tasks are in scope for this guide:</span></span>
-   <span data-ttu-id="0eb9a-148">Configurer Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="0eb9a-148">Set up Azure Active Directory</span></span>
-   <span data-ttu-id="0eb9a-149">Configurer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0eb9a-149">Set up Microsoft 365 Defender</span></span>
    -   <span data-ttu-id="0eb9a-150">Inscrivez-vous à la version d’évaluation de Microsoft 365 E5 ou utilisez votre licence complète si vous exécutez un projet pilote.</span><span class="sxs-lookup"><span data-stu-id="0eb9a-150">Sign up for Microsoft 365 E5 Trial or use your full license if you're running a pilot</span></span>
    -   <span data-ttu-id="0eb9a-151">Configurer le domaine</span><span class="sxs-lookup"><span data-stu-id="0eb9a-151">Configure domain</span></span>
    -   <span data-ttu-id="0eb9a-152">Affecter des licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="0eb9a-152">Assign Microsoft 365 E5 licenses</span></span>
    -   <span data-ttu-id="0eb9a-153">Fin de l’Assistant Installation dans le portail</span><span class="sxs-lookup"><span data-stu-id="0eb9a-153">Completing the setup wizard within the portal</span></span>
-   <span data-ttu-id="0eb9a-154">Configurer tous les piliers de Microsoft 365 Defender en fonction des meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="0eb9a-154">Configure all Microsoft 365 Defender pillars based on best practices</span></span>
    -   <span data-ttu-id="0eb9a-155">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="0eb9a-155">Microsoft Defender for Office 365</span></span>
    -   <span data-ttu-id="0eb9a-156">Microsoft Defender pour identité</span><span class="sxs-lookup"><span data-stu-id="0eb9a-156">Microsoft Defender for Identity</span></span>
    -   <span data-ttu-id="0eb9a-157">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="0eb9a-157">Microsoft Cloud App Security</span></span>
    -   <span data-ttu-id="0eb9a-158">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0eb9a-158">Microsoft Defender for Endpoint</span></span>

## <a name="out-of-scope"></a><span data-ttu-id="0eb9a-159">Non compris</span><span class="sxs-lookup"><span data-stu-id="0eb9a-159">Out of scope</span></span>

<span data-ttu-id="0eb9a-160">Ce guide de déploiement ne comporte pas les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="0eb9a-160">The following are out of scope of this deployment guide:</span></span>

-   <span data-ttu-id="0eb9a-161">Configuration de solutions tierces qui peuvent s’intégrer à Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0eb9a-161">Configuration of third-party solutions that might integrate with Microsoft 365 Defender</span></span>
-   <span data-ttu-id="0eb9a-162">Test de pénétration dans l’environnement de production</span><span class="sxs-lookup"><span data-stu-id="0eb9a-162">Penetration testing in production environment</span></span>

## <a name="next-step"></a><span data-ttu-id="0eb9a-163">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="0eb9a-163">Next step</span></span>
<span data-ttu-id="0eb9a-164">[Phase 1 : préparer](prepare-mtpeval.md) 
</span><span class="sxs-lookup"><span data-stu-id="0eb9a-164">[Phase 1: Prepare](prepare-mtpeval.md) 
</span></span><br> <span data-ttu-id="0eb9a-165">Préparation de votre laboratoire d’évaluation ou de votre environnement pilote Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0eb9a-165">Prepare your Microsoft 365 Defender trial lab or pilot environment</span></span>
