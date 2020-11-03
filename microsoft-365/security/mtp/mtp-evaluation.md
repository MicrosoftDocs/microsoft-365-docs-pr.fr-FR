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
ms.openlocfilehash: d6c96f7720344721bb2786dc130c490a5a8ea657
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48846483"
---
# <a name="create-a-microsoft-365-defender-trial-lab-or-pilot-environment"></a><span data-ttu-id="3783a-104">Création d’un laboratoire d’évaluation ou d’un environnement pilote Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3783a-104">Create a Microsoft 365 Defender trial lab or pilot environment</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="3783a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3783a-105">**Applies to:**</span></span>
- <span data-ttu-id="3783a-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3783a-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="3783a-107">L’objectif de la création de ce laboratoire d’évaluation ou de cet environnement pilote est d’illustrer les fonctionnalités complètes et intégrées de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="3783a-107">The purpose of creating this trial lab or pilot environment is to illustrate the comprehensive and integrated Microsoft 365 Defender capabilities.</span></span> <span data-ttu-id="3783a-108">Découvrez comment cette solution de sécurité intelligente détecte, empêche, recherche automatiquement les menaces avancées de votre organisation et y répond.</span><span class="sxs-lookup"><span data-stu-id="3783a-108">Experience how this intelligent security solution detects, prevents, automatically investigates, and responds to advanced threats your organization.</span></span> 

<span data-ttu-id="3783a-109">Ce guide décrit les étapes à suivre pour démarrer votre évaluation de Microsoft 365 Defender en fonction des chemins de déploiement recommandés.</span><span class="sxs-lookup"><span data-stu-id="3783a-109">This guide takes you through the steps to start your Microsoft 365 Defender evaluation based on the recommended deployment paths.</span></span> <span data-ttu-id="3783a-110">L’objectif est de vous aider à configurer la solution de sécurité dans un environnement de laboratoire avec un compte d’évaluation ou dans un environnement pilote en production avec une licence complète.</span><span class="sxs-lookup"><span data-stu-id="3783a-110">The goal is to help you set up the security solution either in a lab environment with a trial account, or in a pilot environment in production with a full license.</span></span> <span data-ttu-id="3783a-111">La préparation de votre laboratoire d’évaluation ou de votre environnement pilote peut vous aider à présenter des cas d’utilisation des opérations de sécurité pour les décideurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3783a-111">Preparing your trial lab or pilot environment can help you present security operation use cases to decision makers in your organization.</span></span> <span data-ttu-id="3783a-112">Lorsque vous avez terminé d’exécuter vos simulations d’attaque et que vous êtes satisfait du résultat, vous pouvez le déployer et l’utiliser entièrement dans votre organisation à l’aide des professionnels techniques ou des experts de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3783a-112">When you’re done running your attack simulations and are satisfied with the results, you can fully deploy and operationalize it in your organization with the help of Microsoft Technical Sales Professionals or experts in your organization.</span></span> 

<span data-ttu-id="3783a-113">Ce guide vous aidera à :</span><span class="sxs-lookup"><span data-stu-id="3783a-113">This guide will help you:</span></span>
- <span data-ttu-id="3783a-114">Configurer le serveur et les ordinateurs de l’atelier</span><span class="sxs-lookup"><span data-stu-id="3783a-114">Set up your lab server and computers</span></span>
- <span data-ttu-id="3783a-115">Configurer Active Directory avec des utilisateurs et des groupes</span><span class="sxs-lookup"><span data-stu-id="3783a-115">Configure Active Directory with users and groups</span></span>
- <span data-ttu-id="3783a-116">Installer et configurer Microsoft Defender pour l’identité, Microsoft Defender pour Office 365, Microsoft Defender pour le point de terminaison et sécurité des applications Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="3783a-116">Set up and configure Microsoft Defender for Identity, Microsoft Defender for Office 365, Microsoft Defender for Endpoint, and Microsoft Cloud App Security</span></span>
- <span data-ttu-id="3783a-117">Configurer des stratégies locales pour votre serveur et vos ordinateurs</span><span class="sxs-lookup"><span data-stu-id="3783a-117">Set up local policies for your server and computers</span></span>
- <span data-ttu-id="3783a-118">Imiter une attaque de menace pour générer un incident ou une alerte de test dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3783a-118">Mimic a threat attack to generate a test incident or alert in Microsoft 365 Defender</span></span>

>[!IMPORTANT]
><span data-ttu-id="3783a-119">Pour obtenir des résultats optimaux, suivez autant que possible les instructions de configuration de l’atelier.</span><span class="sxs-lookup"><span data-stu-id="3783a-119">For optimum results, follow the lab setup instructions as closely as possible.</span></span>


## <a name="deployment-phases"></a><span data-ttu-id="3783a-120">Phases de déploiement</span><span class="sxs-lookup"><span data-stu-id="3783a-120">Deployment phases</span></span>

<span data-ttu-id="3783a-121">Il existe trois phases pour créer un environnement de laboratoire de test Microsoft 365 Defender et le déployer :</span><span class="sxs-lookup"><span data-stu-id="3783a-121">There are three phases in creating a Microsoft 365 Defender trial lab environment and deploying it:</span></span>

|<span data-ttu-id="3783a-122">Phase</span><span class="sxs-lookup"><span data-stu-id="3783a-122">Phase</span></span> | <span data-ttu-id="3783a-123">Description</span><span class="sxs-lookup"><span data-stu-id="3783a-123">Description</span></span> | 
|:-------|:-----|
| <span data-ttu-id="3783a-124">![Phase 1 : préparer](../../media/prepare.png)</span><span class="sxs-lookup"><span data-stu-id="3783a-124">![Phase 1: Prepare](../../media/prepare.png)</span></span><br>[<span data-ttu-id="3783a-125">Phase 1 : préparer</span><span class="sxs-lookup"><span data-stu-id="3783a-125">Phase 1: Prepare</span></span>](prepare-mtpeval.md)| <span data-ttu-id="3783a-126">Découvrez ce que vous devez prendre en compte lors du déploiement de Microsoft 365 Defender dans un laboratoire d’évaluation ou un environnement pilote :</span><span class="sxs-lookup"><span data-stu-id="3783a-126">Learn what you need to consider when deploying Microsoft 365 Defender in a trial lab or pilot environment:</span></span> <br><br><span data-ttu-id="3783a-127">-Parties prenantes et déconnexion</span><span class="sxs-lookup"><span data-stu-id="3783a-127">- Stakeholders and sign-off</span></span> <br> <span data-ttu-id="3783a-128">-Considérations sur l’environnement</span><span class="sxs-lookup"><span data-stu-id="3783a-128">- Environment considerations</span></span> <br><span data-ttu-id="3783a-129">-Accès</span><span class="sxs-lookup"><span data-stu-id="3783a-129">- Access</span></span> <br><span data-ttu-id="3783a-130">-Installation d’Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3783a-130">- Azure Active Directory setup</span></span> <br> <span data-ttu-id="3783a-131">-Ordre de configuration</span><span class="sxs-lookup"><span data-stu-id="3783a-131">- Configuration order</span></span>
|  <span data-ttu-id="3783a-132">![Phase 2 : configuration](../../media/setup.png)</span><span class="sxs-lookup"><span data-stu-id="3783a-132">![Phase 2: Setup](../../media/setup.png)</span></span> <br>[<span data-ttu-id="3783a-133">Phase 2 : configuration</span><span class="sxs-lookup"><span data-stu-id="3783a-133">Phase 2: Setup</span></span>](setup-mtpeval.md)|  <span data-ttu-id="3783a-134">Suivez les étapes initiales pour accéder au centre de sécurité Microsoft 365 afin de configurer votre laboratoire d’évaluation ou votre environnement pilote Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="3783a-134">Take the initial steps to access Microsoft 365 Security Center to set up your Microsoft 365 Defender trial lab or pilot environment.</span></span> <span data-ttu-id="3783a-135">Vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="3783a-135">You'll be guided to:</span></span><br><br><span data-ttu-id="3783a-136">-Inscrivez-vous à la version d’évaluation de Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="3783a-136">- Sign up for Microsoft 365 E5 Trial</span></span> <br>  <span data-ttu-id="3783a-137">-Configurer le domaine</span><span class="sxs-lookup"><span data-stu-id="3783a-137">- Configure domain</span></span><br><span data-ttu-id="3783a-138">-Affecter les licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="3783a-138">- Assign Microsoft 365 E5 licenses</span></span><br><span data-ttu-id="3783a-139">-Exécutez l’Assistant Installation dans le portail.</span><span class="sxs-lookup"><span data-stu-id="3783a-139">- Complete the setup wizard in the portal</span></span>|
|  <span data-ttu-id="3783a-140">![Phase 3 : configurer & Onboard](../../media/config-onboard.png)</span><span class="sxs-lookup"><span data-stu-id="3783a-140">![Phase 3: Configure & Onboard](../../media/config-onboard.png)</span></span> <br>[<span data-ttu-id="3783a-141">Phase 3 : configurer & Onboard</span><span class="sxs-lookup"><span data-stu-id="3783a-141">Phase 3: Configure & Onboard</span></span>](config-mtpeval.md) | <span data-ttu-id="3783a-142">Configurez chaque pilier Microsoft 365 Defender et les points de terminaison intégrés.</span><span class="sxs-lookup"><span data-stu-id="3783a-142">Configure each Microsoft 365 Defender pillar and onboard endpoints.</span></span> <span data-ttu-id="3783a-143">Vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="3783a-143">You'll be guided to:</span></span><br><br><span data-ttu-id="3783a-144">-Configurer Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="3783a-144">- Configure Microsoft Defender for Office 365</span></span><br><span data-ttu-id="3783a-145">-Configurer la sécurité des applications Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="3783a-145">- Configure Microsoft Cloud App Security</span></span><br><span data-ttu-id="3783a-146">-Configurer Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="3783a-146">- Configure Microsoft Defender for Identity</span></span><br><span data-ttu-id="3783a-147">-Configurer Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3783a-147">- Configure Microsoft Defender for Endpoint</span></span>


## <a name="in-scope"></a><span data-ttu-id="3783a-148">Dans l’étendue</span><span class="sxs-lookup"><span data-stu-id="3783a-148">In scope</span></span>

<span data-ttu-id="3783a-149">Les tâches suivantes sont dans l’étendue de ce guide :</span><span class="sxs-lookup"><span data-stu-id="3783a-149">The following tasks are in scope for this guide:</span></span>
-   <span data-ttu-id="3783a-150">Configurer Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3783a-150">Set up Azure Active Directory</span></span>
-   <span data-ttu-id="3783a-151">Configurer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3783a-151">Set up Microsoft 365 Defender</span></span>
    -   <span data-ttu-id="3783a-152">Inscrivez-vous à la version d’évaluation de Microsoft 365 E5 ou utilisez votre licence complète si vous exécutez un projet pilote.</span><span class="sxs-lookup"><span data-stu-id="3783a-152">Sign up for Microsoft 365 E5 Trial or use your full license if you're running a pilot</span></span>
    -   <span data-ttu-id="3783a-153">Configurer le domaine</span><span class="sxs-lookup"><span data-stu-id="3783a-153">Configure domain</span></span>
    -   <span data-ttu-id="3783a-154">Affecter des licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="3783a-154">Assign Microsoft 365 E5 licenses</span></span>
    -   <span data-ttu-id="3783a-155">Fin de l’Assistant Installation dans le portail</span><span class="sxs-lookup"><span data-stu-id="3783a-155">Completing the setup wizard within the portal</span></span>
-   <span data-ttu-id="3783a-156">Configurer tous les piliers de Microsoft 365 Defender en fonction des meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="3783a-156">Configure all Microsoft 365 Defender pillars based on best practices</span></span>
    -   <span data-ttu-id="3783a-157">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="3783a-157">Microsoft Defender for Office 365</span></span>
    -   <span data-ttu-id="3783a-158">Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="3783a-158">Microsoft Defender for Identity</span></span>
    -   <span data-ttu-id="3783a-159">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="3783a-159">Microsoft Cloud App Security</span></span>
    -   <span data-ttu-id="3783a-160">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3783a-160">Microsoft Defender for Endpoint</span></span>

## <a name="out-of-scope"></a><span data-ttu-id="3783a-161">Non compris</span><span class="sxs-lookup"><span data-stu-id="3783a-161">Out of scope</span></span>

<span data-ttu-id="3783a-162">Ce guide de déploiement ne comporte pas les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3783a-162">The following are out of scope of this deployment guide:</span></span>

-   <span data-ttu-id="3783a-163">Configuration de solutions tierces qui peuvent s’intégrer à Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3783a-163">Configuration of third-party solutions that might integrate with Microsoft 365 Defender</span></span>
-   <span data-ttu-id="3783a-164">Test de pénétration dans l’environnement de production</span><span class="sxs-lookup"><span data-stu-id="3783a-164">Penetration testing in production environment</span></span>

## <a name="next-step"></a><span data-ttu-id="3783a-165">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="3783a-165">Next step</span></span>
<span data-ttu-id="3783a-166">![Phase 1 : préparer](../../media/prepare.png)</span><span class="sxs-lookup"><span data-stu-id="3783a-166">![Phase 1: Prepare](../../media/prepare.png)</span></span> <br><span data-ttu-id="3783a-167">[Phase 1 : préparer](prepare-mtpeval.md) 
</span><span class="sxs-lookup"><span data-stu-id="3783a-167">[Phase 1: Prepare](prepare-mtpeval.md) 
</span></span><br> <span data-ttu-id="3783a-168">Préparation de votre laboratoire d’évaluation ou de votre environnement pilote Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3783a-168">Prepare your Microsoft 365 Defender trial lab or pilot environment</span></span>
