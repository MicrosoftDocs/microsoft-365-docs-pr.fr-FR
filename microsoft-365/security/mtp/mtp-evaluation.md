---
title: Évaluer la Protection Microsoft contre les menaces
description: Configurez votre laboratoire de test Microsoft Threat Protection ou votre environnement pilote pour tester la solution de protection coordonnée contre les menaces conçue pour protéger les périphériques, l’identité, les données et les applications qui peuvent aider votre organisation
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
- m365solution-evalutatemtp
ms.topic: conceptual
ms.openlocfilehash: 3768937fc882fee8d6a744e4fb504095882c7e81
ms.sourcegitcommit: 9d8d071659e662c266b101377e24549963e43fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2020
ms.locfileid: "48368058"
---
# <a name="create-a-microsoft-threat-protection-trial-lab-or-pilot-environment"></a><span data-ttu-id="b4ea4-104">Créer un laboratoire d’évaluation de la protection contre les menaces Microsoft ou un environnement pilote</span><span class="sxs-lookup"><span data-stu-id="b4ea4-104">Create a Microsoft Threat Protection trial lab or pilot environment</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="b4ea4-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b4ea4-105">**Applies to:**</span></span>
- <span data-ttu-id="b4ea4-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="b4ea4-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="b4ea4-107">L’objectif de la création de ce laboratoire d’évaluation ou de cet environnement pilote est d’illustrer les fonctionnalités complètes, intégrées et intelligentes de Microsoft Threat Protection dans le cadre de la détection, de la prévention, de l’enquête et de la réponse que vous pouvez utiliser dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b4ea4-107">The purpose of creating this trial lab or pilot environment is to illustrate the comprehensive, integrated, and intelligent capabilities of Microsoft Threat Protection in detection, prevention, investigation, and response that you can use in your organization.</span></span> 

<span data-ttu-id="b4ea4-108">Ce guide décrit les étapes à suivre pour commencer votre évaluation de la protection contre les menaces Microsoft en fonction des chemins de déploiement recommandés.</span><span class="sxs-lookup"><span data-stu-id="b4ea4-108">This guide takes you through the steps to start your Microsoft Threat Protection evaluation based on the recommended deployment paths.</span></span> <span data-ttu-id="b4ea4-109">L’objectif est de vous aider à configurer les services intégrés de protection contre les menaces Microsoft dans un environnement de laboratoire lors de l’utilisation d’un compte d’évaluation ou dans un environnement pilote en production lors de l’utilisation d’une licence complète.</span><span class="sxs-lookup"><span data-stu-id="b4ea4-109">The goal is to help you set up the integrated Microsoft Threat Protection services in a lab environment when using a trial account, or in a pilot environment in production when using a full license.</span></span> <span data-ttu-id="b4ea4-110">Les résultats qui seront utiles pour la présentation des cas d’utilisation des opérations de sécurité pour les décideurs de la solution de sécurité dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b4ea4-110">The results of which will be useful in presenting security operation use cases to security solution decision makers in your organization.</span></span> <span data-ttu-id="b4ea4-111">Lorsque vous avez terminé d’exécuter vos simulations d’attaque et que vous êtes satisfait du résultat, vous pouvez le déployer entièrement et l’utiliser dans votre organisation avec l’aide des professionnels techniques de Microsoft ou des experts de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b4ea4-111">When you’re done running your attack simulations, and are satisfied with the results, you can fully deploy and operationalize it in your organization with the help of Microsoft Technical Sales Professionals or experts in your organization.</span></span> 

<span data-ttu-id="b4ea4-112">Ce guide vous aidera à :</span><span class="sxs-lookup"><span data-stu-id="b4ea4-112">This guide will help you:</span></span>
- <span data-ttu-id="b4ea4-113">Configurer le serveur et les ordinateurs de l’atelier</span><span class="sxs-lookup"><span data-stu-id="b4ea4-113">Set up your lab server and computers</span></span>
- <span data-ttu-id="b4ea4-114">Configurer Active Directory avec des utilisateurs et des groupes</span><span class="sxs-lookup"><span data-stu-id="b4ea4-114">Configure Active Directory with users and groups</span></span>
- <span data-ttu-id="b4ea4-115">Installer et configurer Azure ATP, Office ATP, Microsoft Defender ATP et Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b4ea4-115">Set up and configure Azure ATP, Office ATP, Microsoft Defender ATP, and Microsoft Cloud App Security</span></span>
- <span data-ttu-id="b4ea4-116">Configurer des stratégies locales pour votre serveur et vos ordinateurs</span><span class="sxs-lookup"><span data-stu-id="b4ea4-116">Set up local policies for your server and computers</span></span>
- <span data-ttu-id="b4ea4-117">Imiter une attaque de menace pour générer un incident ou une alerte de test dans la protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="b4ea4-117">Mimic a threat attack to generate a test incident or alert in Microsoft Threat Protection</span></span>

>[!IMPORTANT]
><span data-ttu-id="b4ea4-118">Pour obtenir des résultats optimaux, suivez autant que possible les instructions de configuration de l’atelier.</span><span class="sxs-lookup"><span data-stu-id="b4ea4-118">For optimum results, follow the lab setup instructions as closely as possible.</span></span>


## <a name="deployment-phases"></a><span data-ttu-id="b4ea4-119">Phases de déploiement</span><span class="sxs-lookup"><span data-stu-id="b4ea4-119">Deployment phases</span></span>

<span data-ttu-id="b4ea4-120">Il existe trois phases pour créer un environnement de laboratoire de test de la protection contre les menaces Microsoft et le déployer :</span><span class="sxs-lookup"><span data-stu-id="b4ea4-120">There are three phases in creating a Microsoft Threat Protection trial lab environment and deploying it:</span></span>

|<span data-ttu-id="b4ea4-121">Phase</span><span class="sxs-lookup"><span data-stu-id="b4ea4-121">Phase</span></span> | <span data-ttu-id="b4ea4-122">Description</span><span class="sxs-lookup"><span data-stu-id="b4ea4-122">Description</span></span> | 
|:-------|:-----|
| <span data-ttu-id="b4ea4-123">![Phase 1 : préparer](../../media/prepare.png)</span><span class="sxs-lookup"><span data-stu-id="b4ea4-123">![Phase 1: Prepare](../../media/prepare.png)</span></span><br>[<span data-ttu-id="b4ea4-124">Phase 1 : préparer</span><span class="sxs-lookup"><span data-stu-id="b4ea4-124">Phase 1: Prepare</span></span>](prepare-mtpeval.md)| <span data-ttu-id="b4ea4-125">Découvrez ce que vous devez prendre en compte lors du déploiement de la protection contre les menaces Microsoft dans un laboratoire d’évaluation ou un environnement pilote :</span><span class="sxs-lookup"><span data-stu-id="b4ea4-125">Learn what you need to consider when deploying Microsoft Threat Protection in a trial lab or pilot environment:</span></span> <br><br><span data-ttu-id="b4ea4-126">-Parties prenantes et déconnexion</span><span class="sxs-lookup"><span data-stu-id="b4ea4-126">- Stakeholders and sign-off</span></span> <br> <span data-ttu-id="b4ea4-127">-Considérations sur l’environnement</span><span class="sxs-lookup"><span data-stu-id="b4ea4-127">- Environment considerations</span></span> <br><span data-ttu-id="b4ea4-128">-Accès</span><span class="sxs-lookup"><span data-stu-id="b4ea4-128">- Access</span></span> <br><span data-ttu-id="b4ea4-129">-Installation d’Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b4ea4-129">- Azure Active Directory setup</span></span> <br> <span data-ttu-id="b4ea4-130">-Ordre de configuration</span><span class="sxs-lookup"><span data-stu-id="b4ea4-130">- Configuration order</span></span>
|  <span data-ttu-id="b4ea4-131">![Phase 2 : configuration](../../media/setup.png)</span><span class="sxs-lookup"><span data-stu-id="b4ea4-131">![Phase 2: Setup](../../media/setup.png)</span></span> <br>[<span data-ttu-id="b4ea4-132">Phase 2 : configuration</span><span class="sxs-lookup"><span data-stu-id="b4ea4-132">Phase 2: Setup</span></span>](setup-mtpeval.md)|  <span data-ttu-id="b4ea4-133">Suivez les étapes initiales pour accéder au centre de sécurité Microsoft 365 afin de configurer votre laboratoire d’évaluation ou votre environnement pilote Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="b4ea4-133">Take the initial steps to access Microsoft 365 Security Center to set up your Microsoft Threat Protection trial lab or pilot environment.</span></span> <span data-ttu-id="b4ea4-134">Vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="b4ea4-134">You'll be guided to:</span></span><br><br><span data-ttu-id="b4ea4-135">-Inscrivez-vous à la version d’évaluation de Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="b4ea4-135">- Sign up for Microsoft 365 E5 Trial</span></span> <br>  <span data-ttu-id="b4ea4-136">-Configurer le domaine</span><span class="sxs-lookup"><span data-stu-id="b4ea4-136">- Configure domain</span></span><br><span data-ttu-id="b4ea4-137">-Affecter les licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="b4ea4-137">- Assign Microsoft 365 E5 licenses</span></span><br><span data-ttu-id="b4ea4-138">-Exécutez l’Assistant Installation dans le portail.</span><span class="sxs-lookup"><span data-stu-id="b4ea4-138">- Complete the setup wizard in the portal</span></span>|
|  <span data-ttu-id="b4ea4-139">![Phase 3 : configurer & Onboard](../../media/config-onboard.png)</span><span class="sxs-lookup"><span data-stu-id="b4ea4-139">![Phase 3: Configure & Onboard](../../media/config-onboard.png)</span></span> <br>[<span data-ttu-id="b4ea4-140">Phase 3 : configurer & Onboard</span><span class="sxs-lookup"><span data-stu-id="b4ea4-140">Phase 3: Configure & Onboard</span></span>](config-mtpeval.md) | <span data-ttu-id="b4ea4-141">Configurez chaque pilier de protection contre les menaces Microsoft et les points de terminaison intégrés.</span><span class="sxs-lookup"><span data-stu-id="b4ea4-141">Configure each Microsoft Threat Protection pillar and onboard endpoints.</span></span> <span data-ttu-id="b4ea4-142">Vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="b4ea4-142">You'll be guided to:</span></span><br><br><span data-ttu-id="b4ea4-143">-Configurer la protection avancée contre les menaces d’Office 365</span><span class="sxs-lookup"><span data-stu-id="b4ea4-143">- Configure Office 365 Advanced Threat Protection</span></span><br><span data-ttu-id="b4ea4-144">-Configurer la sécurité des applications Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="b4ea4-144">- Configure Microsoft Cloud App Security</span></span><br><span data-ttu-id="b4ea4-145">-Configurer Azure protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="b4ea4-145">- Configure Azure Advanced Threat Protection</span></span><br><span data-ttu-id="b4ea4-146">-Configurer Microsoft Defender-protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="b4ea4-146">- Configure Microsoft Defender Advanced Threat Protection</span></span> 


## <a name="in-scope"></a><span data-ttu-id="b4ea4-147">Dans l’étendue</span><span class="sxs-lookup"><span data-stu-id="b4ea4-147">In scope</span></span>

<span data-ttu-id="b4ea4-148">Les tâches suivantes sont dans l’étendue de ce guide :</span><span class="sxs-lookup"><span data-stu-id="b4ea4-148">The following tasks are in scope for this guide:</span></span>
-   <span data-ttu-id="b4ea4-149">Configurer Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b4ea4-149">Set up Azure Active Directory</span></span>
-   <span data-ttu-id="b4ea4-150">Configuration de la protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="b4ea4-150">Set up Microsoft Threat Protection</span></span>
    -   <span data-ttu-id="b4ea4-151">Inscrivez-vous à la version d’évaluation de Microsoft 365 E5 ou utilisez votre licence complète si vous exécutez un projet pilote.</span><span class="sxs-lookup"><span data-stu-id="b4ea4-151">Sign up for Microsoft 365 E5 Trial or use your full license if you're running a pilot</span></span>
    -   <span data-ttu-id="b4ea4-152">Configurer le domaine</span><span class="sxs-lookup"><span data-stu-id="b4ea4-152">Configure domain</span></span>
    -   <span data-ttu-id="b4ea4-153">Affecter des licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="b4ea4-153">Assign Microsoft 365 E5 licenses</span></span>
    -   <span data-ttu-id="b4ea4-154">Fin de l’Assistant Installation dans le portail</span><span class="sxs-lookup"><span data-stu-id="b4ea4-154">Completing the setup wizard within the portal</span></span>
-   <span data-ttu-id="b4ea4-155">Configurer tous les piliers de protection contre les menaces Microsoft en fonction des meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="b4ea4-155">Configure all Microsoft Threat Protection pillars based on best practices</span></span>
    -   <span data-ttu-id="b4ea4-156">Office 365 – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="b4ea4-156">Office 365 Advanced Threat Protection</span></span>
    -   <span data-ttu-id="b4ea4-157">Azure Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b4ea4-157">Azure Advanced Threat Protection</span></span>
    -   <span data-ttu-id="b4ea4-158">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b4ea4-158">Microsoft Cloud App Security</span></span>
    -   <span data-ttu-id="b4ea4-159">Microsoft Defender – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="b4ea4-159">Microsoft Defender Advanced Threat Protection</span></span>

## <a name="out-of-scope"></a><span data-ttu-id="b4ea4-160">Non compris</span><span class="sxs-lookup"><span data-stu-id="b4ea4-160">Out of scope</span></span>

<span data-ttu-id="b4ea4-161">Ce guide de déploiement ne comporte pas les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b4ea4-161">The following are out of scope of this deployment guide:</span></span>

-   <span data-ttu-id="b4ea4-162">Configuration de solutions tierces qui peuvent s’intégrer à la protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="b4ea4-162">Configuration of third-party solutions that might integrate with Microsoft Threat Protection</span></span>
-   <span data-ttu-id="b4ea4-163">Test de pénétration dans l’environnement de production</span><span class="sxs-lookup"><span data-stu-id="b4ea4-163">Penetration testing in production environment</span></span>

## <a name="next-step"></a><span data-ttu-id="b4ea4-164">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="b4ea4-164">Next step</span></span>
<span data-ttu-id="b4ea4-165">![Phase 1 : préparer](../../media/prepare.png)</span><span class="sxs-lookup"><span data-stu-id="b4ea4-165">![Phase 1: Prepare](../../media/prepare.png)</span></span> <br><span data-ttu-id="b4ea4-166">[Phase 1 : préparer](prepare-mtpeval.md) 
</span><span class="sxs-lookup"><span data-stu-id="b4ea4-166">[Phase 1: Prepare](prepare-mtpeval.md) 
</span></span><br> <span data-ttu-id="b4ea4-167">Préparation de votre laboratoire d’évaluation ou de votre environnement pilote Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b4ea4-167">Prepare your Microsoft Threat Protection trial lab or pilot environment</span></span>
