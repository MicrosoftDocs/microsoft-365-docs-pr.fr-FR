---
title: Intégrer au service Microsoft Defender ATP
description: Découvrez comment intégrer des points de terminaison au service Microsoft Defender ATP
keywords: ''
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365solution-endpointprotect
- m365solution-scenario
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 2b3ce535ba5abddbf1175e568638f7ee186e093d
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51068486"
---
# <a name="onboard-to-the-microsoft-defender-for-endpoint-service"></a><span data-ttu-id="2cc59-103">Intégration au service Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="2cc59-103">Onboard to the Microsoft Defender for Endpoint service</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="2cc59-104">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2cc59-104">**Applies to:**</span></span>
- [<span data-ttu-id="2cc59-105">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2cc59-105">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="2cc59-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2cc59-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="2cc59-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="2cc59-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="2cc59-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="2cc59-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="2cc59-109">Découvrez les différentes phases du déploiement de Microsoft Defender pour Endpoint et comment configurer les fonctionnalités au sein de la solution.</span><span class="sxs-lookup"><span data-stu-id="2cc59-109">Learn about the various phases of deploying Microsoft Defender for Endpoint and how to configure the capabilities within the solution.</span></span> 

<span data-ttu-id="2cc59-110">Le déploiement de Defender pour endpoint est un processus en trois phases :</span><span class="sxs-lookup"><span data-stu-id="2cc59-110">Deploying Defender for Endpoint is a three-phase process:</span></span>

| <span data-ttu-id="2cc59-111">[![phase de déploiement : préparer](images/phase-diagrams/prepare.png)](prepare-deployment.md)</span><span class="sxs-lookup"><span data-stu-id="2cc59-111">[![deployment phase - prepare](images/phase-diagrams/prepare.png)](prepare-deployment.md)</span></span><br>[<span data-ttu-id="2cc59-112">Phase 1 : Préparer</span><span class="sxs-lookup"><span data-stu-id="2cc59-112">Phase 1: Prepare</span></span>](prepare-deployment.md) | <span data-ttu-id="2cc59-113">[![phase de déploiement : configuration](images/phase-diagrams/setup.png)](production-deployment.md)</span><span class="sxs-lookup"><span data-stu-id="2cc59-113">[![deployment phase - setup](images/phase-diagrams/setup.png)](production-deployment.md)</span></span><br>[<span data-ttu-id="2cc59-114">Phase 2 : Installation</span><span class="sxs-lookup"><span data-stu-id="2cc59-114">Phase 2: Setup</span></span>](production-deployment.md) | ![phase de déploiement : intégration](images/phase-diagrams/onboard.png)<br><span data-ttu-id="2cc59-116">Phase 3 : Intégration</span><span class="sxs-lookup"><span data-stu-id="2cc59-116">Phase 3: Onboard</span></span> |
| ----- | ----- | ----- |
| | |<span data-ttu-id="2cc59-117">*Vous êtes là !*</span><span class="sxs-lookup"><span data-stu-id="2cc59-117">*You are here!*</span></span>|

<span data-ttu-id="2cc59-118">Vous êtes actuellement en phase d’intégration.</span><span class="sxs-lookup"><span data-stu-id="2cc59-118">You are currently in the onboarding phase.</span></span>

<span data-ttu-id="2cc59-119">Voici les étapes à suivre pour déployer Defender pour Endpoint :</span><span class="sxs-lookup"><span data-stu-id="2cc59-119">These are the steps you need to take to deploy Defender for Endpoint:</span></span>

- <span data-ttu-id="2cc59-120">Étape 1 : Intégrer des points de terminaison au service</span><span class="sxs-lookup"><span data-stu-id="2cc59-120">Step 1: Onboard endpoints to the service</span></span> 
- <span data-ttu-id="2cc59-121">Étape 2 : Configurer les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="2cc59-121">Step 2: Configure capabilities</span></span> 

## <a name="step-1-onboard-endpoints-using-any-of-the-supported-management-tools"></a><span data-ttu-id="2cc59-122">Étape 1 : Intégrer des points de terminaison à l’aide de l’un des outils de gestion pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cc59-122">Step 1: Onboard endpoints using any of the supported management tools</span></span>
<span data-ttu-id="2cc59-123">La [rubrique Planifier le](deployment-strategy.md) déploiement décrit les étapes générales à suivre pour déployer Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="2cc59-123">The [Plan deployment](deployment-strategy.md) topic outlines the general steps you need to take to deploy Defender for Endpoint.</span></span>  


<span data-ttu-id="2cc59-124">Regardez cette vidéo pour obtenir une vue d’ensemble rapide du processus d’intégration et en savoir plus sur les outils et méthodes disponibles.</span><span class="sxs-lookup"><span data-stu-id="2cc59-124">Watch this video for a quick overview of the onboarding process and learn about the available tools and methods.</span></span>
<br />
<br />

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4bGqr]



<span data-ttu-id="2cc59-125">Après avoir identifié votre architecture, vous devez choisir la méthode de déploiement à utiliser.</span><span class="sxs-lookup"><span data-stu-id="2cc59-125">After identifying your architecture, you'll need to decide which deployment method to use.</span></span> <span data-ttu-id="2cc59-126">L’outil de déploiement que vous choisissez influence la façon dont vous intégrerez les points de terminaison au service.</span><span class="sxs-lookup"><span data-stu-id="2cc59-126">The deployment tool you choose influences how you onboard endpoints to the service.</span></span> 

### <a name="onboarding-tool-options"></a><span data-ttu-id="2cc59-127">Options de l’outil d’intégration</span><span class="sxs-lookup"><span data-stu-id="2cc59-127">Onboarding tool options</span></span>

<span data-ttu-id="2cc59-128">Le tableau suivant répertorie les outils disponibles en fonction du point de terminaison que vous devez intégrer.</span><span class="sxs-lookup"><span data-stu-id="2cc59-128">The following table lists the available tools based on the endpoint that you need to onboard.</span></span>

| <span data-ttu-id="2cc59-129">Point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2cc59-129">Endpoint</span></span>     | <span data-ttu-id="2cc59-130">Options de l’outil</span><span class="sxs-lookup"><span data-stu-id="2cc59-130">Tool options</span></span>                       |
|--------------|------------------------------------------|
| <span data-ttu-id="2cc59-131">**Windows**</span><span class="sxs-lookup"><span data-stu-id="2cc59-131">**Windows**</span></span>  |  [<span data-ttu-id="2cc59-132">Script local (jusqu’à 10 appareils)</span><span class="sxs-lookup"><span data-stu-id="2cc59-132">Local script (up to 10 devices)</span></span>](configure-endpoints-script.md) <br>  [<span data-ttu-id="2cc59-133">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2cc59-133">Group Policy</span></span>](configure-endpoints-gp.md) <br>  [<span data-ttu-id="2cc59-134">Gestionnaire de point de terminaison Microsoft/ Gestionnaire d’appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="2cc59-134">Microsoft Endpoint Manager/ Mobile Device Manager</span></span>](configure-endpoints-mdm.md) <br>   [<span data-ttu-id="2cc59-135">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="2cc59-135">Microsoft Endpoint Configuration Manager</span></span>](configure-endpoints-sccm.md) <br> [<span data-ttu-id="2cc59-136">Scripts VDI</span><span class="sxs-lookup"><span data-stu-id="2cc59-136">VDI scripts</span></span>](configure-endpoints-vdi.md)   |
| <span data-ttu-id="2cc59-137">**MacOS**</span><span class="sxs-lookup"><span data-stu-id="2cc59-137">**macOS**</span></span>    | [<span data-ttu-id="2cc59-138">Scripts locaux</span><span class="sxs-lookup"><span data-stu-id="2cc59-138">Local scripts</span></span>](mac-install-manually.md) <br> [<span data-ttu-id="2cc59-139">Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="2cc59-139">Microsoft Endpoint Manager</span></span>](mac-install-with-intune.md) <br> [<span data-ttu-id="2cc59-140">JAMF Pro</span><span class="sxs-lookup"><span data-stu-id="2cc59-140">JAMF Pro</span></span>](mac-install-with-jamf.md) <br> [<span data-ttu-id="2cc59-141">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="2cc59-141">Mobile Device Management</span></span>](mac-install-with-other-mdm.md) |
| <span data-ttu-id="2cc59-142">**Serveur Linux**</span><span class="sxs-lookup"><span data-stu-id="2cc59-142">**Linux Server**</span></span> | [<span data-ttu-id="2cc59-143">Script local</span><span class="sxs-lookup"><span data-stu-id="2cc59-143">Local script</span></span>](linux-install-manually.md) <br> [<span data-ttu-id="2cc59-144">Sondent</span><span class="sxs-lookup"><span data-stu-id="2cc59-144">Puppet</span></span>](linux-install-with-puppet.md) <br> [<span data-ttu-id="2cc59-145">Ansible</span><span class="sxs-lookup"><span data-stu-id="2cc59-145">Ansible</span></span>](linux-install-with-ansible.md)|
| <span data-ttu-id="2cc59-146">**iOS**</span><span class="sxs-lookup"><span data-stu-id="2cc59-146">**iOS**</span></span>      | [<span data-ttu-id="2cc59-147">Basée sur l’application</span><span class="sxs-lookup"><span data-stu-id="2cc59-147">App-based</span></span>](ios-install.md)                                |
| <span data-ttu-id="2cc59-148">**Android**</span><span class="sxs-lookup"><span data-stu-id="2cc59-148">**Android**</span></span>  | [<span data-ttu-id="2cc59-149">Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="2cc59-149">Microsoft Endpoint Manager</span></span>](android-intune.md)               | 


## <a name="step-2-configure-capabilities"></a><span data-ttu-id="2cc59-150">Étape 2 : Configurer les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="2cc59-150">Step 2: Configure capabilities</span></span>
<span data-ttu-id="2cc59-151">Après avoir intégré les points de terminaison, vous allez configurer les différentes fonctionnalités telles que la détection et la réponse des points de terminaison, la protection nouvelle génération et la réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="2cc59-151">After onboarding the endpoints, you'll then configure the various capabilities such as endpoint detection and response, next-generation protection, and attack surface reduction.</span></span> 


## <a name="example-deployments"></a><span data-ttu-id="2cc59-152">Exemples de déploiements</span><span class="sxs-lookup"><span data-stu-id="2cc59-152">Example deployments</span></span>
<span data-ttu-id="2cc59-153">Dans ce guide de déploiement, nous allons vous guider tout au long de l’utilisation de deux outils de déploiement pour intégrer des points de terminaison et configurer des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="2cc59-153">In this deployment guide, we'll guide you through using two deployment tools to onboard endpoints and how to configure capabilities.</span></span>

<span data-ttu-id="2cc59-154">Les outils de l’exemple de déploiement sont :</span><span class="sxs-lookup"><span data-stu-id="2cc59-154">The tools in the example deployments are:</span></span>
- [<span data-ttu-id="2cc59-155">Intégration à l’aide de Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="2cc59-155">Onboarding using Microsoft Endpoint Configuration Manager</span></span>](onboarding-endpoint-configuration-manager.md)
- [<span data-ttu-id="2cc59-156">Intégration à l’aide de Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="2cc59-156">Onboarding using Microsoft Endpoint Manager</span></span>](onboarding-endpoint-manager.md)

<span data-ttu-id="2cc59-157">À l’aide des outils de déploiement mentionnés ci-dessus, vous serez guidé dans la configuration des fonctionnalités defender pour point de terminaison suivantes :</span><span class="sxs-lookup"><span data-stu-id="2cc59-157">Using the mentioned deployment tools above, you'll then be guided in configuring the following Defender for Endpoint capabilities:</span></span>
- <span data-ttu-id="2cc59-158">Détection de point de terminaison et configuration de la réponse</span><span class="sxs-lookup"><span data-stu-id="2cc59-158">Endpoint detection and response configuration</span></span>
- <span data-ttu-id="2cc59-159">Configuration de la protection nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="2cc59-159">Next-generation protection configuration</span></span>
- <span data-ttu-id="2cc59-160">Configuration de la réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="2cc59-160">Attack surface reduction configuration</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cc59-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cc59-161">Related topics</span></span>
- [<span data-ttu-id="2cc59-162">Intégration à l’aide de Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="2cc59-162">Onboarding using Microsoft Endpoint Configuration Manager</span></span>](onboarding-endpoint-configuration-manager.md)
- [<span data-ttu-id="2cc59-163">Intégration à l’aide de Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="2cc59-163">Onboarding using Microsoft Endpoint Manager</span></span>](onboarding-endpoint-manager.md)
