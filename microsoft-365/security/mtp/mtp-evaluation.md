---
title: Évaluer la Protection Microsoft contre les menaces
description: Configurez votre laboratoire d’évaluation de la protection contre les menaces Microsoft ou votre environnement pilote afin de tester la solution de sécurité conçue pour protéger les périphériques, l’identité, les données et les applications de votre organisation.
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
ms.openlocfilehash: d3f63c8ac4ba82a80c365dce564bbd8d3dd4da4b
ms.sourcegitcommit: 9a764c2aed7338c37f6e92f5fb487f02b3c4dfa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/13/2020
ms.locfileid: "48447118"
---
# <a name="create-a-microsoft-threat-protection-trial-lab-or-pilot-environment"></a><span data-ttu-id="94ff3-104">Créer un laboratoire d’évaluation de la protection contre les menaces Microsoft ou un environnement pilote</span><span class="sxs-lookup"><span data-stu-id="94ff3-104">Create a Microsoft Threat Protection trial lab or pilot environment</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="94ff3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="94ff3-105">**Applies to:**</span></span>
- <span data-ttu-id="94ff3-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="94ff3-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="94ff3-107">L’objectif de la création de ce laboratoire d’évaluation ou de cet environnement pilote est d’illustrer les fonctionnalités complètes et intégrées de protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="94ff3-107">The purpose of creating this trial lab or pilot environment is to illustrate the comprehensive and integrated Microsoft Threat Protection capabilities.</span></span> <span data-ttu-id="94ff3-108">Découvrez comment cette solution de sécurité intelligente détecte, empêche, recherche automatiquement les menaces avancées de votre organisation et y répond.</span><span class="sxs-lookup"><span data-stu-id="94ff3-108">Experience how this intelligent security solution detects, prevents, automatically investigates, and responds to advanced threats your organization.</span></span> 

<span data-ttu-id="94ff3-109">Ce guide décrit les étapes à suivre pour commencer votre évaluation de la protection contre les menaces Microsoft en fonction des chemins de déploiement recommandés.</span><span class="sxs-lookup"><span data-stu-id="94ff3-109">This guide takes you through the steps to start your Microsoft Threat Protection evaluation based on the recommended deployment paths.</span></span> <span data-ttu-id="94ff3-110">L’objectif est de vous aider à configurer la solution de sécurité dans un environnement de laboratoire avec un compte d’évaluation ou dans un environnement pilote en production avec une licence complète.</span><span class="sxs-lookup"><span data-stu-id="94ff3-110">The goal is to help you set up the security solution either in a lab environment with a trial account, or in a pilot environment in production with a full license.</span></span> <span data-ttu-id="94ff3-111">La préparation de votre laboratoire d’évaluation ou de votre environnement pilote peut vous aider à présenter des cas d’utilisation des opérations de sécurité pour les décideurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="94ff3-111">Preparing your trial lab or pilot environment can help you present security operation use cases to decision makers in your organization.</span></span> <span data-ttu-id="94ff3-112">Lorsque vous avez terminé d’exécuter vos simulations d’attaque et que vous êtes satisfait du résultat, vous pouvez le déployer et l’utiliser entièrement dans votre organisation à l’aide des professionnels techniques ou des experts de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="94ff3-112">When you’re done running your attack simulations and are satisfied with the results, you can fully deploy and operationalize it in your organization with the help of Microsoft Technical Sales Professionals or experts in your organization.</span></span> 

<span data-ttu-id="94ff3-113">Ce guide vous aidera à :</span><span class="sxs-lookup"><span data-stu-id="94ff3-113">This guide will help you:</span></span>
- <span data-ttu-id="94ff3-114">Configurer le serveur et les ordinateurs de l’atelier</span><span class="sxs-lookup"><span data-stu-id="94ff3-114">Set up your lab server and computers</span></span>
- <span data-ttu-id="94ff3-115">Configurer Active Directory avec des utilisateurs et des groupes</span><span class="sxs-lookup"><span data-stu-id="94ff3-115">Configure Active Directory with users and groups</span></span>
- <span data-ttu-id="94ff3-116">Installer et configurer Azure ATP, Office ATP, Microsoft Defender ATP et Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="94ff3-116">Set up and configure Azure ATP, Office ATP, Microsoft Defender ATP, and Microsoft Cloud App Security</span></span>
- <span data-ttu-id="94ff3-117">Configurer des stratégies locales pour votre serveur et vos ordinateurs</span><span class="sxs-lookup"><span data-stu-id="94ff3-117">Set up local policies for your server and computers</span></span>
- <span data-ttu-id="94ff3-118">Imiter une attaque de menace pour générer un incident ou une alerte de test dans la protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="94ff3-118">Mimic a threat attack to generate a test incident or alert in Microsoft Threat Protection</span></span>

>[!IMPORTANT]
><span data-ttu-id="94ff3-119">Pour obtenir des résultats optimaux, suivez autant que possible les instructions de configuration de l’atelier.</span><span class="sxs-lookup"><span data-stu-id="94ff3-119">For optimum results, follow the lab setup instructions as closely as possible.</span></span>


## <a name="deployment-phases"></a><span data-ttu-id="94ff3-120">Phases de déploiement</span><span class="sxs-lookup"><span data-stu-id="94ff3-120">Deployment phases</span></span>

<span data-ttu-id="94ff3-121">Il existe trois phases pour créer un environnement de laboratoire de test de la protection contre les menaces Microsoft et le déployer :</span><span class="sxs-lookup"><span data-stu-id="94ff3-121">There are three phases in creating a Microsoft Threat Protection trial lab environment and deploying it:</span></span>

|<span data-ttu-id="94ff3-122">Phase</span><span class="sxs-lookup"><span data-stu-id="94ff3-122">Phase</span></span> | <span data-ttu-id="94ff3-123">Description</span><span class="sxs-lookup"><span data-stu-id="94ff3-123">Description</span></span> | 
|:-------|:-----|
| <span data-ttu-id="94ff3-124">![Phase 1 : préparer](../../media/prepare.png)</span><span class="sxs-lookup"><span data-stu-id="94ff3-124">![Phase 1: Prepare](../../media/prepare.png)</span></span><br>[<span data-ttu-id="94ff3-125">Phase 1 : préparer</span><span class="sxs-lookup"><span data-stu-id="94ff3-125">Phase 1: Prepare</span></span>](prepare-mtpeval.md)| <span data-ttu-id="94ff3-126">Découvrez ce que vous devez prendre en compte lors du déploiement de la protection contre les menaces Microsoft dans un laboratoire d’évaluation ou un environnement pilote :</span><span class="sxs-lookup"><span data-stu-id="94ff3-126">Learn what you need to consider when deploying Microsoft Threat Protection in a trial lab or pilot environment:</span></span> <br><br><span data-ttu-id="94ff3-127">-Parties prenantes et déconnexion</span><span class="sxs-lookup"><span data-stu-id="94ff3-127">- Stakeholders and sign-off</span></span> <br> <span data-ttu-id="94ff3-128">-Considérations sur l’environnement</span><span class="sxs-lookup"><span data-stu-id="94ff3-128">- Environment considerations</span></span> <br><span data-ttu-id="94ff3-129">-Accès</span><span class="sxs-lookup"><span data-stu-id="94ff3-129">- Access</span></span> <br><span data-ttu-id="94ff3-130">-Installation d’Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="94ff3-130">- Azure Active Directory setup</span></span> <br> <span data-ttu-id="94ff3-131">-Ordre de configuration</span><span class="sxs-lookup"><span data-stu-id="94ff3-131">- Configuration order</span></span>
|  <span data-ttu-id="94ff3-132">![Phase 2 : configuration](../../media/setup.png)</span><span class="sxs-lookup"><span data-stu-id="94ff3-132">![Phase 2: Setup](../../media/setup.png)</span></span> <br>[<span data-ttu-id="94ff3-133">Phase 2 : configuration</span><span class="sxs-lookup"><span data-stu-id="94ff3-133">Phase 2: Setup</span></span>](setup-mtpeval.md)|  <span data-ttu-id="94ff3-134">Suivez les étapes initiales pour accéder au centre de sécurité Microsoft 365 afin de configurer votre laboratoire d’évaluation ou votre environnement pilote Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="94ff3-134">Take the initial steps to access Microsoft 365 Security Center to set up your Microsoft Threat Protection trial lab or pilot environment.</span></span> <span data-ttu-id="94ff3-135">Vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="94ff3-135">You'll be guided to:</span></span><br><br><span data-ttu-id="94ff3-136">-Inscrivez-vous à la version d’évaluation de Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="94ff3-136">- Sign up for Microsoft 365 E5 Trial</span></span> <br>  <span data-ttu-id="94ff3-137">-Configurer le domaine</span><span class="sxs-lookup"><span data-stu-id="94ff3-137">- Configure domain</span></span><br><span data-ttu-id="94ff3-138">-Affecter les licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="94ff3-138">- Assign Microsoft 365 E5 licenses</span></span><br><span data-ttu-id="94ff3-139">-Exécutez l’Assistant Installation dans le portail.</span><span class="sxs-lookup"><span data-stu-id="94ff3-139">- Complete the setup wizard in the portal</span></span>|
|  <span data-ttu-id="94ff3-140">![Phase 3 : configurer & Onboard](../../media/config-onboard.png)</span><span class="sxs-lookup"><span data-stu-id="94ff3-140">![Phase 3: Configure & Onboard](../../media/config-onboard.png)</span></span> <br>[<span data-ttu-id="94ff3-141">Phase 3 : configurer & Onboard</span><span class="sxs-lookup"><span data-stu-id="94ff3-141">Phase 3: Configure & Onboard</span></span>](config-mtpeval.md) | <span data-ttu-id="94ff3-142">Configurez chaque pilier de protection contre les menaces Microsoft et les points de terminaison intégrés.</span><span class="sxs-lookup"><span data-stu-id="94ff3-142">Configure each Microsoft Threat Protection pillar and onboard endpoints.</span></span> <span data-ttu-id="94ff3-143">Vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="94ff3-143">You'll be guided to:</span></span><br><br><span data-ttu-id="94ff3-144">-Configurer la protection avancée contre les menaces d’Office 365</span><span class="sxs-lookup"><span data-stu-id="94ff3-144">- Configure Office 365 Advanced Threat Protection</span></span><br><span data-ttu-id="94ff3-145">-Configurer la sécurité des applications Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="94ff3-145">- Configure Microsoft Cloud App Security</span></span><br><span data-ttu-id="94ff3-146">-Configurer Azure protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="94ff3-146">- Configure Azure Advanced Threat Protection</span></span><br><span data-ttu-id="94ff3-147">-Configurer Microsoft Defender-protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="94ff3-147">- Configure Microsoft Defender Advanced Threat Protection</span></span> 


## <a name="in-scope"></a><span data-ttu-id="94ff3-148">Dans l’étendue</span><span class="sxs-lookup"><span data-stu-id="94ff3-148">In scope</span></span>

<span data-ttu-id="94ff3-149">Les tâches suivantes sont dans l’étendue de ce guide :</span><span class="sxs-lookup"><span data-stu-id="94ff3-149">The following tasks are in scope for this guide:</span></span>
-   <span data-ttu-id="94ff3-150">Configurer Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="94ff3-150">Set up Azure Active Directory</span></span>
-   <span data-ttu-id="94ff3-151">Configuration de la protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="94ff3-151">Set up Microsoft Threat Protection</span></span>
    -   <span data-ttu-id="94ff3-152">Inscrivez-vous à la version d’évaluation de Microsoft 365 E5 ou utilisez votre licence complète si vous exécutez un projet pilote.</span><span class="sxs-lookup"><span data-stu-id="94ff3-152">Sign up for Microsoft 365 E5 Trial or use your full license if you're running a pilot</span></span>
    -   <span data-ttu-id="94ff3-153">Configurer le domaine</span><span class="sxs-lookup"><span data-stu-id="94ff3-153">Configure domain</span></span>
    -   <span data-ttu-id="94ff3-154">Affecter des licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="94ff3-154">Assign Microsoft 365 E5 licenses</span></span>
    -   <span data-ttu-id="94ff3-155">Fin de l’Assistant Installation dans le portail</span><span class="sxs-lookup"><span data-stu-id="94ff3-155">Completing the setup wizard within the portal</span></span>
-   <span data-ttu-id="94ff3-156">Configurer tous les piliers de protection contre les menaces Microsoft en fonction des meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="94ff3-156">Configure all Microsoft Threat Protection pillars based on best practices</span></span>
    -   <span data-ttu-id="94ff3-157">Office 365 – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="94ff3-157">Office 365 Advanced Threat Protection</span></span>
    -   <span data-ttu-id="94ff3-158">Azure Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="94ff3-158">Azure Advanced Threat Protection</span></span>
    -   <span data-ttu-id="94ff3-159">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="94ff3-159">Microsoft Cloud App Security</span></span>
    -   <span data-ttu-id="94ff3-160">Microsoft Defender – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="94ff3-160">Microsoft Defender Advanced Threat Protection</span></span>

## <a name="out-of-scope"></a><span data-ttu-id="94ff3-161">Non compris</span><span class="sxs-lookup"><span data-stu-id="94ff3-161">Out of scope</span></span>

<span data-ttu-id="94ff3-162">Ce guide de déploiement ne comporte pas les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="94ff3-162">The following are out of scope of this deployment guide:</span></span>

-   <span data-ttu-id="94ff3-163">Configuration de solutions tierces qui peuvent s’intégrer à la protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="94ff3-163">Configuration of third-party solutions that might integrate with Microsoft Threat Protection</span></span>
-   <span data-ttu-id="94ff3-164">Test de pénétration dans l’environnement de production</span><span class="sxs-lookup"><span data-stu-id="94ff3-164">Penetration testing in production environment</span></span>

## <a name="next-step"></a><span data-ttu-id="94ff3-165">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="94ff3-165">Next step</span></span>
<span data-ttu-id="94ff3-166">![Phase 1 : préparer](../../media/prepare.png)</span><span class="sxs-lookup"><span data-stu-id="94ff3-166">![Phase 1: Prepare](../../media/prepare.png)</span></span> <br><span data-ttu-id="94ff3-167">[Phase 1 : préparer](prepare-mtpeval.md) 
</span><span class="sxs-lookup"><span data-stu-id="94ff3-167">[Phase 1: Prepare](prepare-mtpeval.md) 
</span></span><br> <span data-ttu-id="94ff3-168">Préparation de votre laboratoire d’évaluation ou de votre environnement pilote Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="94ff3-168">Prepare your Microsoft Threat Protection trial lab or pilot environment</span></span>
