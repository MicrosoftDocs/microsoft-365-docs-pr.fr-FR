---
title: Évaluer la Protection Microsoft contre les menaces
description: Configurez votre environnement de laboratoire de test Microsoft Threat Protection pour tester la solution de protection coordonnée contre les menaces conçue pour protéger les appareils, l’identité, les données et les applications peuvent aider votre organisation
keywords: Version d’évaluation de la protection de Microsoft contre les menaces, essayez Microsoft Threat Protection, évaluez Microsoft Threat Protection, l’atelier d’évaluation de la protection contre les menaces Microsoft, la cyber sécurité, la protection avancée contre les menaces, la sécurité des entreprises, les appareils, l’appareil, l’identité, les utilisateurs, les données, les applications, les incidents, l’analyse et la correction
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
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.openlocfilehash: a9d7b514aac8d1a769c0dabf6dcdb54f4bcb447b
ms.sourcegitcommit: 9a275a13af3e063e80ce1bd3cd8142a095db92d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2020
ms.locfileid: "47649960"
---
# <a name="create-a-microsoft-threat-protection-trial-lab-environment"></a><span data-ttu-id="fc145-104">Créer un environnement de laboratoire d’évaluation de la protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="fc145-104">Create a Microsoft Threat Protection trial lab environment</span></span> 

<span data-ttu-id="fc145-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="fc145-105">**Applies to:**</span></span>
- <span data-ttu-id="fc145-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="fc145-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="fc145-107">L’objectif de la création de cet environnement de laboratoire d’évaluation est d’illustrer les fonctionnalités complètes, intégrées et intelligentes de Microsoft Threat Protection dans le cadre de la détection, de la prévention, de l’enquête et de la réponse que vous pouvez utiliser dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="fc145-107">The purpose of creating this trial lab environment is to illustrate the comprehensive, integrated, and intelligent capabilities of Microsoft Threat Protection in detection, prevention, investigation, and response that you can use in your organization.</span></span> 

<span data-ttu-id="fc145-108">Ce guide décrit les étapes à suivre pour commencer votre évaluation de la protection contre les menaces Microsoft en fonction des chemins de déploiement recommandés.</span><span class="sxs-lookup"><span data-stu-id="fc145-108">This guide takes you through the steps to start your Microsoft Threat Protection evaluation based on the recommended deployment paths.</span></span> <span data-ttu-id="fc145-109">L’objectif est de vous aider à configurer les services intégrés de protection contre les menaces Microsoft dans un environnement de laboratoire ou en tant que preuve de concept (POC) lors de la présentation des décideurs de la solution de sécurité dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="fc145-109">The goal is to help you set up the integrated Microsoft Threat Protection services in a lab environment or as a proof of concept (POC) when presenting to security solution decision makers in your organization.</span></span> <span data-ttu-id="fc145-110">Lorsque vous avez terminé d’exécuter vos simulations d’attaque, l’analyse et la réponse automatiques, et que vous êtes satisfait des résultats, vous pouvez le déployer dans votre environnement de production à l’aide des professionnels techniques de Microsoft ou des experts de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="fc145-110">When you’re done running your attack simulations, automated investigation and response, and are satisfied with the results, you can deploy it in your production environment with the help of Microsoft Technical Sales Professionals or experts in your organization.</span></span> 

<span data-ttu-id="fc145-111">Ce guide vous aidera à :</span><span class="sxs-lookup"><span data-stu-id="fc145-111">This guide will help you:</span></span>
- <span data-ttu-id="fc145-112">Configurer le serveur et les ordinateurs de l’atelier</span><span class="sxs-lookup"><span data-stu-id="fc145-112">Set up your lab server and computers</span></span>
- <span data-ttu-id="fc145-113">Configurer Active Directory avec des utilisateurs et des groupes</span><span class="sxs-lookup"><span data-stu-id="fc145-113">Configure Active Directory with users and groups</span></span>
- <span data-ttu-id="fc145-114">Installer et configurer Azure ATP, Office ATP, Microsoft Defender ATP et Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="fc145-114">Set up and configure Azure ATP, Office ATP, Microsoft Defender ATP, and Microsoft Cloud App Security</span></span>
- <span data-ttu-id="fc145-115">Configurer des stratégies locales pour votre serveur et vos ordinateurs</span><span class="sxs-lookup"><span data-stu-id="fc145-115">Setup local policies for your server and computers</span></span>
- <span data-ttu-id="fc145-116">Imiter une attaque de menace pour générer un incident ou une alerte de test dans la protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="fc145-116">Mimic a threat attack to generate a test incident or alert in Microsoft Threat Protection</span></span>

>[!IMPORTANT]
><span data-ttu-id="fc145-117">Pour obtenir des résultats optimaux, suivez autant que possible les instructions de configuration de l’atelier.</span><span class="sxs-lookup"><span data-stu-id="fc145-117">For optimum results, follow the lab setup instructions as closely as possible.</span></span>


## <a name="deployment-phases"></a><span data-ttu-id="fc145-118">Phases de déploiement</span><span class="sxs-lookup"><span data-stu-id="fc145-118">Deployment phases</span></span>

<span data-ttu-id="fc145-119">Il existe trois phases pour créer un environnement de laboratoire de test de la protection contre les menaces Microsoft et le déployer :</span><span class="sxs-lookup"><span data-stu-id="fc145-119">There are three phases in creating a Microsoft Threat Protection trial lab environment and deploying it:</span></span>

|<span data-ttu-id="fc145-120">Phase</span><span class="sxs-lookup"><span data-stu-id="fc145-120">Phase</span></span> | <span data-ttu-id="fc145-121">Description</span><span class="sxs-lookup"><span data-stu-id="fc145-121">Description</span></span> | 
|:-------|:-----|
| <span data-ttu-id="fc145-122">![Phase 1 : préparer](../../media/prepare.png)</span><span class="sxs-lookup"><span data-stu-id="fc145-122">![Phase 1: Prepare](../../media/prepare.png)</span></span><br>[<span data-ttu-id="fc145-123">Phase 1 : préparer</span><span class="sxs-lookup"><span data-stu-id="fc145-123">Phase 1: Prepare</span></span>](prepare-mtpeval.md)| <span data-ttu-id="fc145-124">Découvrez ce que vous devez prendre en compte lors du déploiement de la protection contre les menaces Microsoft dans un environnement de laboratoire d’évaluation :</span><span class="sxs-lookup"><span data-stu-id="fc145-124">Learn what you need to consider when deploying Microsoft Threat Protection in a trial lab environment:</span></span> <br><br><span data-ttu-id="fc145-125">-Parties prenantes et déconnexion</span><span class="sxs-lookup"><span data-stu-id="fc145-125">- Stakeholders and sign-off</span></span> <br> <span data-ttu-id="fc145-126">-Considérations sur l’environnement</span><span class="sxs-lookup"><span data-stu-id="fc145-126">- Environment considerations</span></span> <br><span data-ttu-id="fc145-127">-Accès</span><span class="sxs-lookup"><span data-stu-id="fc145-127">- Access</span></span> <br><span data-ttu-id="fc145-128">-Installation d’Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fc145-128">- Azure Active Directory setup</span></span> <br> <span data-ttu-id="fc145-129">-Ordre de configuration</span><span class="sxs-lookup"><span data-stu-id="fc145-129">- Configuration order</span></span>
|  <span data-ttu-id="fc145-130">![Phase 2 : configuration](../../media/setup.png)</span><span class="sxs-lookup"><span data-stu-id="fc145-130">![Phase 2: Setup](../../media/setup.png)</span></span> <br>[<span data-ttu-id="fc145-131">Phase 2 : configuration</span><span class="sxs-lookup"><span data-stu-id="fc145-131">Phase 2: Setup</span></span>](setup-mtpeval.md)|  <span data-ttu-id="fc145-132">Suivez les étapes initiales pour accéder au centre de sécurité Microsoft 365 afin de configurer votre environnement de laboratoire de test Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="fc145-132">Take the initial steps to access Microsoft 365 Security Center to setup your Microsoft Threat Protection trial lab environment.</span></span> <span data-ttu-id="fc145-133">Vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="fc145-133">You will be guided to:</span></span><br><br><span data-ttu-id="fc145-134">-Inscrivez-vous à la version d’évaluation de Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="fc145-134">- Sign up for Microsoft 365 E5 Trial</span></span> <br>  <span data-ttu-id="fc145-135">-Configurer le domaine</span><span class="sxs-lookup"><span data-stu-id="fc145-135">- Configure domain</span></span><br><span data-ttu-id="fc145-136">-Affecter les licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="fc145-136">- Assign Microsoft 365 E5 licenses</span></span><br><span data-ttu-id="fc145-137">-Exécutez l’Assistant Installation dans le portail.</span><span class="sxs-lookup"><span data-stu-id="fc145-137">- Complete the setup wizard in the portal</span></span>|
|  <span data-ttu-id="fc145-138">![Phase 3 : configurer & Onboard](../../media/config-onboard.png)</span><span class="sxs-lookup"><span data-stu-id="fc145-138">![Phase 3: Configure & Onboard](../../media/config-onboard.png)</span></span> <br>[<span data-ttu-id="fc145-139">Phase 3 : configurer & Onboard</span><span class="sxs-lookup"><span data-stu-id="fc145-139">Phase 3: Configure & Onboard</span></span>](config-mtpeval.md) | <span data-ttu-id="fc145-140">Configurez chaque pilier de protection contre les menaces Microsoft et les points de terminaison intégrés.</span><span class="sxs-lookup"><span data-stu-id="fc145-140">Configure each Microsoft Threat Protection pillar and onboard endpoints.</span></span> <span data-ttu-id="fc145-141">Vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="fc145-141">You will be guided to:</span></span><br><br><span data-ttu-id="fc145-142">-Configurer la protection avancée contre les menaces d’Office 365</span><span class="sxs-lookup"><span data-stu-id="fc145-142">- Configure Office 365 Advanced Threat Protection</span></span><br><span data-ttu-id="fc145-143">-Configurer la sécurité des applications Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="fc145-143">- Configure Microsoft Cloud App Security</span></span><br><span data-ttu-id="fc145-144">-Configurer Azure protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="fc145-144">- Configure Azure Advanced Threat Protection</span></span><br><span data-ttu-id="fc145-145">-Configurer Microsoft Defender-protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="fc145-145">- Configure Microsoft Defender Advanced Threat Protection</span></span> 


## <a name="in-scope"></a><span data-ttu-id="fc145-146">Dans l’étendue</span><span class="sxs-lookup"><span data-stu-id="fc145-146">In scope</span></span>

<span data-ttu-id="fc145-147">Les éléments suivants sont inclus dans le cadre de ce guide de laboratoire d’évaluation :</span><span class="sxs-lookup"><span data-stu-id="fc145-147">The following is in scope for this trial lab environment guide:</span></span>
-   <span data-ttu-id="fc145-148">Configurer Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fc145-148">Set up Azure Active Directory</span></span>
-   <span data-ttu-id="fc145-149">Configuration de la protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="fc145-149">Set up Microsoft Threat Protection</span></span>
    -   <span data-ttu-id="fc145-150">Inscrivez-vous à la version d’évaluation de Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="fc145-150">Sign up for Microsoft 365 E5 Trial</span></span>
    -   <span data-ttu-id="fc145-151">Configurer le domaine</span><span class="sxs-lookup"><span data-stu-id="fc145-151">Configure domain</span></span>
    -   <span data-ttu-id="fc145-152">Affecter des licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="fc145-152">Assign Microsoft 365 E5 licenses</span></span>
    -   <span data-ttu-id="fc145-153">Fin de l’Assistant Installation dans le portail</span><span class="sxs-lookup"><span data-stu-id="fc145-153">Completing the setup wizard within the portal</span></span>
-   <span data-ttu-id="fc145-154">Configurer tous les piliers de protection contre les menaces Microsoft en fonction des meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="fc145-154">Configure all Microsoft Threat Protection pillars based on best practices</span></span>
    -   <span data-ttu-id="fc145-155">Office 365 – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="fc145-155">Office 365 Advanced Threat Protection</span></span>
    -   <span data-ttu-id="fc145-156">Azure Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="fc145-156">Azure Advanced Threat Protection</span></span>
    -   <span data-ttu-id="fc145-157">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="fc145-157">Microsoft Cloud App Security</span></span>
    -   <span data-ttu-id="fc145-158">Microsoft Defender – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="fc145-158">Microsoft Defender Advanced Threat Protection</span></span>

## <a name="out-of-scope"></a><span data-ttu-id="fc145-159">Non compris</span><span class="sxs-lookup"><span data-stu-id="fc145-159">Out of scope</span></span>

<span data-ttu-id="fc145-160">Ce guide de déploiement ne comporte pas les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="fc145-160">The following are out of scope of this deployment guide:</span></span>

-   <span data-ttu-id="fc145-161">Configuration de solutions tierces qui peuvent s’intégrer à Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="fc145-161">Configuration of third-party solutions that might integrate with Microsoft Defender ATP</span></span>
-   <span data-ttu-id="fc145-162">Test de pénétration dans l’environnement de production</span><span class="sxs-lookup"><span data-stu-id="fc145-162">Penetration testing in production environment</span></span>

## <a name="next-step"></a><span data-ttu-id="fc145-163">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="fc145-163">Next step</span></span>
<span data-ttu-id="fc145-164">![Phase 1 : préparer](../../media/prepare.png)</span><span class="sxs-lookup"><span data-stu-id="fc145-164">![Phase 1: Prepare](../../media/prepare.png)</span></span> <br><span data-ttu-id="fc145-165">[Phase 1 : préparer](prepare-mtpeval.md) 
</span><span class="sxs-lookup"><span data-stu-id="fc145-165">[Phase 1: Prepare](prepare-mtpeval.md) 
</span></span><br> <span data-ttu-id="fc145-166">Préparer votre environnement d’atelier d’évaluation de la protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="fc145-166">Prepare your Microsoft Threat Protection evaluation lab environment</span></span>
