---
title: Intégration au service Microsoft Defender for Endpoint
description: Découvrez comment intégrer des points de terminaison au service Microsoft Defender for Endpoint
keywords: microsoft defender pour le point de terminaison, intégrer, déployer
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
ms.openlocfilehash: f63b4f81f454fec60a26c7cb063d66bed4a2bead
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933540"
---
# <a name="onboard-to-the-microsoft-defender-for-endpoint-service"></a><span data-ttu-id="ff1bf-104">Intégration au service Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="ff1bf-104">Onboard to the Microsoft Defender for Endpoint service</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="ff1bf-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-105">**Applies to:**</span></span>
- [<span data-ttu-id="ff1bf-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ff1bf-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="ff1bf-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ff1bf-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="ff1bf-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="ff1bf-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="ff1bf-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="ff1bf-110">Découvrez les différentes phases du déploiement de Microsoft Defender pour Endpoint et comment configurer les fonctionnalités au sein de la solution.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-110">Learn about the various phases of deploying Microsoft Defender for Endpoint and how to configure the capabilities within the solution.</span></span> 

<span data-ttu-id="ff1bf-111">Le déploiement de Defender pour endpoint est un processus en trois phases :</span><span class="sxs-lookup"><span data-stu-id="ff1bf-111">Deploying Defender for Endpoint is a three-phase process:</span></span>

| <span data-ttu-id="ff1bf-112">[![phase de déploiement : préparer](images/phase-diagrams/prepare.png)](prepare-deployment.md)</span><span class="sxs-lookup"><span data-stu-id="ff1bf-112">[![deployment phase - prepare](images/phase-diagrams/prepare.png)](prepare-deployment.md)</span></span><br>[<span data-ttu-id="ff1bf-113">Phase 1 : préparation</span><span class="sxs-lookup"><span data-stu-id="ff1bf-113">Phase 1: Prepare</span></span>](prepare-deployment.md) | <span data-ttu-id="ff1bf-114">[![phase de déploiement : configuration](images/phase-diagrams/setup.png)](production-deployment.md)</span><span class="sxs-lookup"><span data-stu-id="ff1bf-114">[![deployment phase - setup](images/phase-diagrams/setup.png)](production-deployment.md)</span></span><br>[<span data-ttu-id="ff1bf-115">Phase 2 : configuration</span><span class="sxs-lookup"><span data-stu-id="ff1bf-115">Phase 2: Setup</span></span>](production-deployment.md) | ![phase de déploiement : intégration](images/phase-diagrams/onboard.png)<br><span data-ttu-id="ff1bf-117">Phase 3 : intégration</span><span class="sxs-lookup"><span data-stu-id="ff1bf-117">Phase 3: Onboard</span></span> |
| ----- | ----- | ----- |
| | |<span data-ttu-id="ff1bf-118">*Vous êtes là !*</span><span class="sxs-lookup"><span data-stu-id="ff1bf-118">*You are here!*</span></span>|

<span data-ttu-id="ff1bf-119">Vous êtes actuellement en phase d'intégration.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-119">You are currently in the onboarding phase.</span></span>

<span data-ttu-id="ff1bf-120">Voici les étapes à suivre pour déployer Defender pour Endpoint :</span><span class="sxs-lookup"><span data-stu-id="ff1bf-120">These are the steps you need to take to deploy Defender for Endpoint:</span></span>

- <span data-ttu-id="ff1bf-121">Étape 1 : Intégrer des points de terminaison au service</span><span class="sxs-lookup"><span data-stu-id="ff1bf-121">Step 1: Onboard endpoints to the service</span></span> 
- <span data-ttu-id="ff1bf-122">Étape 2 : Configurer les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="ff1bf-122">Step 2: Configure capabilities</span></span> 

## <a name="step-1-onboard-endpoints-using-any-of-the-supported-management-tools"></a><span data-ttu-id="ff1bf-123">Étape 1 : Intégrer des points de terminaison à l'aide de l'un des outils de gestion pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff1bf-123">Step 1: Onboard endpoints using any of the supported management tools</span></span>
<span data-ttu-id="ff1bf-124">La [rubrique Planifier le](deployment-strategy.md) déploiement décrit les étapes générales à suivre pour déployer Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-124">The [Plan deployment](deployment-strategy.md) topic outlines the general steps you need to take to deploy Defender for Endpoint.</span></span>  


<span data-ttu-id="ff1bf-125">Regardez cette vidéo pour obtenir une vue d'ensemble rapide du processus d'intégration et en savoir plus sur les outils et méthodes disponibles.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-125">Watch this video for a quick overview of the onboarding process and learn about the available tools and methods.</span></span>
<br />
<br />

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4bGqr]



<span data-ttu-id="ff1bf-126">Après avoir identifié votre architecture, vous devez choisir la méthode de déploiement à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-126">After identifying your architecture, you'll need to decide which deployment method to use.</span></span> <span data-ttu-id="ff1bf-127">L'outil de déploiement que vous choisissez influence la façon dont vous intégrerez les points de terminaison au service.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-127">The deployment tool you choose influences how you onboard endpoints to the service.</span></span> 

### <a name="onboarding-tool-options"></a><span data-ttu-id="ff1bf-128">Options de l'outil d'intégration</span><span class="sxs-lookup"><span data-stu-id="ff1bf-128">Onboarding tool options</span></span>

<span data-ttu-id="ff1bf-129">Le tableau suivant répertorie les outils disponibles en fonction du point de terminaison que vous devez intégrer.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-129">The following table lists the available tools based on the endpoint that you need to onboard.</span></span>

| <span data-ttu-id="ff1bf-130">Point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ff1bf-130">Endpoint</span></span>     | <span data-ttu-id="ff1bf-131">Options de l'outil</span><span class="sxs-lookup"><span data-stu-id="ff1bf-131">Tool options</span></span>                       |
|--------------|------------------------------------------|
| <span data-ttu-id="ff1bf-132">**Windows**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-132">**Windows**</span></span>  |  [<span data-ttu-id="ff1bf-133">Script local (jusqu'à 10 appareils)</span><span class="sxs-lookup"><span data-stu-id="ff1bf-133">Local script (up to 10 devices)</span></span>](configure-endpoints-script.md) <br>  [<span data-ttu-id="ff1bf-134">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff1bf-134">Group Policy</span></span>](configure-endpoints-gp.md) <br>  [<span data-ttu-id="ff1bf-135">Gestionnaire de point de terminaison Microsoft/ Gestionnaire d'appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="ff1bf-135">Microsoft Endpoint Manager/ Mobile Device Manager</span></span>](configure-endpoints-mdm.md) <br> [<span data-ttu-id="ff1bf-136">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ff1bf-136">Microsoft Endpoint Configuration Manager</span></span>](configure-endpoints-sccm.md) <br> [<span data-ttu-id="ff1bf-137">Scripts VDI</span><span class="sxs-lookup"><span data-stu-id="ff1bf-137">VDI scripts</span></span>](configure-endpoints-vdi.md) <br> [<span data-ttu-id="ff1bf-138">Intégration à Azure Defender</span><span class="sxs-lookup"><span data-stu-id="ff1bf-138">Integration with Azure Defender</span></span>](configure-server-endpoints.md#integration-with-azure-defender) |
| <span data-ttu-id="ff1bf-139">**MacOS**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-139">**macOS**</span></span>    | [<span data-ttu-id="ff1bf-140">Scripts locaux</span><span class="sxs-lookup"><span data-stu-id="ff1bf-140">Local scripts</span></span>](mac-install-manually.md) <br> [<span data-ttu-id="ff1bf-141">Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="ff1bf-141">Microsoft Endpoint Manager</span></span>](mac-install-with-intune.md) <br> [<span data-ttu-id="ff1bf-142">JAMF Pro</span><span class="sxs-lookup"><span data-stu-id="ff1bf-142">JAMF Pro</span></span>](mac-install-with-jamf.md) <br> [<span data-ttu-id="ff1bf-143">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="ff1bf-143">Mobile Device Management</span></span>](mac-install-with-other-mdm.md) |
| <span data-ttu-id="ff1bf-144">**Serveur Linux**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-144">**Linux Server**</span></span> | [<span data-ttu-id="ff1bf-145">Script local</span><span class="sxs-lookup"><span data-stu-id="ff1bf-145">Local script</span></span>](linux-install-manually.md) <br> [<span data-ttu-id="ff1bf-146">Sondent</span><span class="sxs-lookup"><span data-stu-id="ff1bf-146">Puppet</span></span>](linux-install-with-puppet.md) <br> [<span data-ttu-id="ff1bf-147">Ansible</span><span class="sxs-lookup"><span data-stu-id="ff1bf-147">Ansible</span></span>](linux-install-with-ansible.md)|
| <span data-ttu-id="ff1bf-148">**iOS**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-148">**iOS**</span></span>      | [<span data-ttu-id="ff1bf-149">Basée sur l'application</span><span class="sxs-lookup"><span data-stu-id="ff1bf-149">App-based</span></span>](ios-install.md)                                |
| <span data-ttu-id="ff1bf-150">**Android**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-150">**Android**</span></span>  | [<span data-ttu-id="ff1bf-151">Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="ff1bf-151">Microsoft Endpoint Manager</span></span>](android-intune.md)               | 


## <a name="step-2-configure-capabilities"></a><span data-ttu-id="ff1bf-152">Étape 2 : Configurer les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="ff1bf-152">Step 2: Configure capabilities</span></span>
<span data-ttu-id="ff1bf-153">Après avoir intégré les points de terminaison, vous allez configurer les différentes fonctionnalités telles que la détection et la réponse des points de terminaison, la protection nouvelle génération et la réduction de la surface d'attaque.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-153">After onboarding the endpoints, you'll then configure the various capabilities such as endpoint detection and response, next-generation protection, and attack surface reduction.</span></span> 


## <a name="example-deployments"></a><span data-ttu-id="ff1bf-154">Exemples de déploiements</span><span class="sxs-lookup"><span data-stu-id="ff1bf-154">Example deployments</span></span>
<span data-ttu-id="ff1bf-155">Dans ce guide de déploiement, nous allons vous guider tout au long de l'utilisation de deux outils de déploiement pour intégrer des points de terminaison et configurer des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-155">In this deployment guide, we'll guide you through using two deployment tools to onboard endpoints and how to configure capabilities.</span></span>

<span data-ttu-id="ff1bf-156">Les outils de l’exemple de déploiement sont les :</span><span class="sxs-lookup"><span data-stu-id="ff1bf-156">The tools in the example deployments are:</span></span>
- [<span data-ttu-id="ff1bf-157">Intégration à l'aide de Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ff1bf-157">Onboarding using Microsoft Endpoint Configuration Manager</span></span>](onboarding-endpoint-configuration-manager.md)
- [<span data-ttu-id="ff1bf-158">Intégration à l'aide de Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="ff1bf-158">Onboarding using Microsoft Endpoint Manager</span></span>](onboarding-endpoint-manager.md)

<span data-ttu-id="ff1bf-159">À l’aide des outils de déploiement mentionnés ci-dessus, vous serez guidé dans la configuration des fonctionnalités defender pour point de terminaison suivantes :</span><span class="sxs-lookup"><span data-stu-id="ff1bf-159">Using the mentioned deployment tools above, you'll then be guided in configuring the following Defender for Endpoint capabilities:</span></span>
- <span data-ttu-id="ff1bf-160">Détection de point de terminaison et configuration de la réponse</span><span class="sxs-lookup"><span data-stu-id="ff1bf-160">Endpoint detection and response configuration</span></span>
- <span data-ttu-id="ff1bf-161">Configuration de la protection nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="ff1bf-161">Next-generation protection configuration</span></span>
- <span data-ttu-id="ff1bf-162">Configuration de la réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="ff1bf-162">Attack surface reduction configuration</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff1bf-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff1bf-163">Related topics</span></span>
- [<span data-ttu-id="ff1bf-164">Intégration à l'aide de Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ff1bf-164">Onboarding using Microsoft Endpoint Configuration Manager</span></span>](onboarding-endpoint-configuration-manager.md)
- [<span data-ttu-id="ff1bf-165">Intégration à l'aide de Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="ff1bf-165">Onboarding using Microsoft Endpoint Manager</span></span>](onboarding-endpoint-manager.md)
- [<span data-ttu-id="ff1bf-166">Documents sécurisés dans Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="ff1bf-166">Safe Documents in Microsoft 365 E5</span></span>](../office-365-security/safe-docs.md)
