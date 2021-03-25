---
title: Planifier votre déploiement de Microsoft Defender pour les points de terminaison
description: Sélectionnez la meilleure stratégie de déploiement de Microsoft Defender pour les points de terminaison pour votre environnement
keywords: déployer, planifier, stratégie de déploiement, cloud natif, gestion, sur site, évaluation, intégration, local, stratégie de groupe, gp, gestionnaire de point de terminaison, mem
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
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 8cd670e72bbb4ec0abacd4ed053a9ea9af12608b
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51163574"
---
# <a name="plan-your-microsoft-defender-for-endpoint-deployment"></a><span data-ttu-id="bb10f-104">Planifier votre déploiement de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="bb10f-104">Plan your Microsoft Defender for Endpoint deployment</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="bb10f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="bb10f-105">**Applies to:**</span></span>
- [<span data-ttu-id="bb10f-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="bb10f-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="bb10f-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bb10f-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="bb10f-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="bb10f-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="bb10f-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="bb10f-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-secopsdashboard-abovefoldlink) 


<span data-ttu-id="bb10f-110">Planifiez votre déploiement de Microsoft Defender for Endpoint afin d’optimiser les fonctionnalités de sécurité de la suite et de mieux protéger votre entreprise contre les cybermenaces.</span><span class="sxs-lookup"><span data-stu-id="bb10f-110">Plan your Microsoft Defender for Endpoint deployment so that you can maximize the security capabilities within the suite and better protect your enterprise from cyber threats.</span></span>


<span data-ttu-id="bb10f-111">Cette solution fournit des conseils sur l’identification de l’architecture de votre environnement, la sélection du type d’outil de déploiement qui répond le mieux à vos besoins et des instructions sur la configuration des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="bb10f-111">This solution provides guidance on how to identify your environment architecture, select the type of deployment tool that best fits your needs, and guidance on how to configure capabilities.</span></span>


![Image du flux de déploiement](images/deployment-guide-plan.png)


## <a name="step-1-identify-architecture"></a><span data-ttu-id="bb10f-113">Étape 1 : identifier l’architecture</span><span class="sxs-lookup"><span data-stu-id="bb10f-113">Step 1: Identify architecture</span></span>
<span data-ttu-id="bb10f-114">Comme nous savons que chaque environnement d’entreprise est unique, nous avons fourni plusieurs options pour vous offrir la flexibilité nécessaire pour choisir le déploiement du service.</span><span class="sxs-lookup"><span data-stu-id="bb10f-114">We understand that every enterprise environment is unique, so we've provided several options to give you the flexibility in choosing how to deploy the service.</span></span>

<span data-ttu-id="bb10f-115">Selon votre environnement, certains outils conviennent mieux à certaines architectures.</span><span class="sxs-lookup"><span data-stu-id="bb10f-115">Depending on your environment, some tools are better suited for certain architectures.</span></span> 

<span data-ttu-id="bb10f-116">Utilisez les documents suivants pour sélectionner l’architecture defender pour point de terminaison appropriée qui convient le mieux à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bb10f-116">Use the following material to select the appropriate Defender for Endpoint architecture that best suites your organization.</span></span>

| <span data-ttu-id="bb10f-117">Item</span><span class="sxs-lookup"><span data-stu-id="bb10f-117">Item</span></span> | <span data-ttu-id="bb10f-118">Description</span><span class="sxs-lookup"><span data-stu-id="bb10f-118">Description</span></span> |
|:-----|:-----|
|<span data-ttu-id="bb10f-119">[![Image miniature de la stratégie de déploiement de Defender for Endpoint](images/mdatp-deployment-strategy.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf)</span><span class="sxs-lookup"><span data-stu-id="bb10f-119">[![Thumb image for Defender for Endpoint deployment strategy](images/mdatp-deployment-strategy.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf)</span></span><br/> <span data-ttu-id="bb10f-120">[PDF](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf)  \| [Visio](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.vsdx)</span><span class="sxs-lookup"><span data-stu-id="bb10f-120">[PDF](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf)  \| [Visio](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.vsdx)</span></span> | <span data-ttu-id="bb10f-121">Le matériel architectural vous aide à planifier votre déploiement pour les architectures suivantes :</span><span class="sxs-lookup"><span data-stu-id="bb10f-121">The architectural material helps you plan your deployment for the following architectures:</span></span> <ul><li> <span data-ttu-id="bb10f-122">Cloud-natif</span><span class="sxs-lookup"><span data-stu-id="bb10f-122">Cloud-native</span></span> </li><li> <span data-ttu-id="bb10f-123">Cogestion</span><span class="sxs-lookup"><span data-stu-id="bb10f-123">Co-management</span></span> </li><li> <span data-ttu-id="bb10f-124">Sur site</span><span class="sxs-lookup"><span data-stu-id="bb10f-124">On-premise</span></span></li><li><span data-ttu-id="bb10f-125">Évaluation et intégration locale</span><span class="sxs-lookup"><span data-stu-id="bb10f-125">Evaluation and local onboarding</span></span></li>



## <a name="step-2-select-deployment-method"></a><span data-ttu-id="bb10f-126">Étape 2 : sélectionner la méthode de déploiement</span><span class="sxs-lookup"><span data-stu-id="bb10f-126">Step 2: Select deployment method</span></span>
<span data-ttu-id="bb10f-127">Defender pour le point de terminaison prend en charge divers points de terminaison que vous pouvez intégrer au service.</span><span class="sxs-lookup"><span data-stu-id="bb10f-127">Defender for Endpoint supports a variety of endpoints that you can onboard to the service.</span></span> 

<span data-ttu-id="bb10f-128">Le tableau suivant répertorie les points de terminaison pris en charge et l’outil de déploiement correspondant que vous pouvez utiliser pour planifier le déploiement de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="bb10f-128">The following table lists the supported endpoints and the corresponding deployment tool that you can use so that you can plan the deployment appropriately.</span></span>

| <span data-ttu-id="bb10f-129">Point de terminaison</span><span class="sxs-lookup"><span data-stu-id="bb10f-129">Endpoint</span></span>     | <span data-ttu-id="bb10f-130">Outil de déploiement</span><span class="sxs-lookup"><span data-stu-id="bb10f-130">Deployment tool</span></span>                       |
|--------------|------------------------------------------|
| <span data-ttu-id="bb10f-131">**Windows**</span><span class="sxs-lookup"><span data-stu-id="bb10f-131">**Windows**</span></span>  |  [<span data-ttu-id="bb10f-132">Script local (jusqu’à 10 appareils)</span><span class="sxs-lookup"><span data-stu-id="bb10f-132">Local script (up to 10 devices)</span></span>](configure-endpoints-script.md) <br>  [<span data-ttu-id="bb10f-133">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="bb10f-133">Group Policy</span></span>](configure-endpoints-gp.md) <br>  [<span data-ttu-id="bb10f-134">Gestionnaire de point de terminaison Microsoft/ Gestionnaire d’appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="bb10f-134">Microsoft Endpoint Manager/ Mobile Device Manager</span></span>](configure-endpoints-mdm.md) <br>   [<span data-ttu-id="bb10f-135">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bb10f-135">Microsoft Endpoint Configuration Manager</span></span>](configure-endpoints-sccm.md) <br> [<span data-ttu-id="bb10f-136">Scripts VDI</span><span class="sxs-lookup"><span data-stu-id="bb10f-136">VDI scripts</span></span>](configure-endpoints-vdi.md)   |
| <span data-ttu-id="bb10f-137">**MacOS**</span><span class="sxs-lookup"><span data-stu-id="bb10f-137">**macOS**</span></span>    | [<span data-ttu-id="bb10f-138">Script local</span><span class="sxs-lookup"><span data-stu-id="bb10f-138">Local script</span></span>](mac-install-manually.md) <br> [<span data-ttu-id="bb10f-139">Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="bb10f-139">Microsoft Endpoint Manager</span></span>](mac-install-with-intune.md) <br> [<span data-ttu-id="bb10f-140">JAMF Pro</span><span class="sxs-lookup"><span data-stu-id="bb10f-140">JAMF Pro</span></span>](mac-install-with-jamf.md) <br> [<span data-ttu-id="bb10f-141">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="bb10f-141">Mobile Device Management</span></span>](mac-install-with-other-mdm.md) |
| <span data-ttu-id="bb10f-142">**Serveur Linux**</span><span class="sxs-lookup"><span data-stu-id="bb10f-142">**Linux Server**</span></span> | [<span data-ttu-id="bb10f-143">Script local</span><span class="sxs-lookup"><span data-stu-id="bb10f-143">Local script</span></span>](linux-install-manually.md) <br> [<span data-ttu-id="bb10f-144">Sondent</span><span class="sxs-lookup"><span data-stu-id="bb10f-144">Puppet</span></span>](linux-install-with-puppet.md) <br> [<span data-ttu-id="bb10f-145">Ansible</span><span class="sxs-lookup"><span data-stu-id="bb10f-145">Ansible</span></span>](linux-install-with-ansible.md)|
| <span data-ttu-id="bb10f-146">**iOS**</span><span class="sxs-lookup"><span data-stu-id="bb10f-146">**iOS**</span></span>      | [<span data-ttu-id="bb10f-147">Basée sur l’application</span><span class="sxs-lookup"><span data-stu-id="bb10f-147">App-based</span></span>](ios-install.md)                                |
| <span data-ttu-id="bb10f-148">**Android**</span><span class="sxs-lookup"><span data-stu-id="bb10f-148">**Android**</span></span>  | [<span data-ttu-id="bb10f-149">Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="bb10f-149">Microsoft Endpoint Manager</span></span>](android-intune.md)               | 



## <a name="step-3-configure-capabilities"></a><span data-ttu-id="bb10f-150">Étape 3 : Configurer les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="bb10f-150">Step 3: Configure capabilities</span></span>
<span data-ttu-id="bb10f-151">Après l’intégration des points de terminaison, configurez les fonctionnalités de sécurité dans Defender pour le point de terminaison afin que vous pouvez optimiser la protection de sécurité robuste disponible dans la suite.</span><span class="sxs-lookup"><span data-stu-id="bb10f-151">After onboarding endpoints, configure the security capabilities in Defender for Endpoint so that you can maximize the robust security protection available in the suite.</span></span> <span data-ttu-id="bb10f-152">Les fonctionnalités sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="bb10f-152">Capabilities include:</span></span>

- <span data-ttu-id="bb10f-153">Détection et réponse au point de terminaison</span><span class="sxs-lookup"><span data-stu-id="bb10f-153">Endpoint detection and response</span></span>
- <span data-ttu-id="bb10f-154">Protection nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="bb10f-154">Next-generation protection</span></span>
- <span data-ttu-id="bb10f-155">Réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="bb10f-155">Attack surface reduction</span></span>


  
## <a name="related-topics"></a><span data-ttu-id="bb10f-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb10f-156">Related topics</span></span>
- [<span data-ttu-id="bb10f-157">Phases de déploiement</span><span class="sxs-lookup"><span data-stu-id="bb10f-157">Deployment phases</span></span>](deployment-phases.md)
