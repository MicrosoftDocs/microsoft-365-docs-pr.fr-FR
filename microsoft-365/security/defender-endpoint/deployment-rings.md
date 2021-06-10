---
title: Déployer Microsoft Defender pour le point de terminaison dans des anneaux
description: Découvrez comment déployer Microsoft Defender pour le point de terminaison dans les anneaux
keywords: déployer, anneaux, évaluer, pilote, insider fast, insider slow, setup, onboard, phase, deployment, deploying, adoption, configuring
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
- m365solution-overview
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 5aeaa51e5ab8974c8ca26453534396dac14b5853
ms.sourcegitcommit: de5fce90de22ba588e75e1a1d2e87e03b9e25ec7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "52297204"
---
# <a name="deploy-microsoft-defender-for-endpoint-in-rings"></a><span data-ttu-id="051d6-104">Déployer Microsoft Defender pour le point de terminaison dans des anneaux</span><span class="sxs-lookup"><span data-stu-id="051d6-104">Deploy Microsoft Defender for Endpoint in rings</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="051d6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="051d6-105">**Applies to:**</span></span>
- [<span data-ttu-id="051d6-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="051d6-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="051d6-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="051d6-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="051d6-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="051d6-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="051d6-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="051d6-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="051d6-110">Le déploiement de Microsoft Defender pour Endpoint peut être effectué à l’aide d’une approche de déploiement basée sur l’anneau.</span><span class="sxs-lookup"><span data-stu-id="051d6-110">Deploying Microsoft Defender for Endpoint can be done using a ring-based deployment approach.</span></span> 

<span data-ttu-id="051d6-111">Les anneaux de déploiement peuvent être appliqués dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="051d6-111">The deployment rings can be applied in the following scenarios:</span></span>
- [<span data-ttu-id="051d6-112">Nouveaux déploiements</span><span class="sxs-lookup"><span data-stu-id="051d6-112">New deployments</span></span>](#new-deployments)
- [<span data-ttu-id="051d6-113">Déploiements existants</span><span class="sxs-lookup"><span data-stu-id="051d6-113">Existing deployments</span></span>](#existing-deployments)

## <a name="new-deployments"></a><span data-ttu-id="051d6-114">Nouveaux déploiements</span><span class="sxs-lookup"><span data-stu-id="051d6-114">New deployments</span></span>

![Image des anneaux de déploiement](images/deployment-rings.png)


<span data-ttu-id="051d6-116">Une approche basée sur l’anneau est une méthode d’identification d’un ensemble de points de terminaison à intégrer et de vérifier que certains critères sont satisfaits avant de poursuivre le déploiement du service sur un plus grand ensemble d’appareils.</span><span class="sxs-lookup"><span data-stu-id="051d6-116">A ring-based approach is a method of identifying a set of endpoints to onboard and verifying that certain criteria is met before proceeding to deploy the service to a larger set of devices.</span></span> <span data-ttu-id="051d6-117">Vous pouvez définir les critères de sortie de chaque anneau et vous assurer qu’ils sont satisfaits avant de passer à l’anneau suivant.</span><span class="sxs-lookup"><span data-stu-id="051d6-117">You can define the exit criteria for each ring and ensure that they are satisfied before moving on to the next ring.</span></span>

<span data-ttu-id="051d6-118">L’adoption d’un déploiement basé sur l’anneau permet de réduire les problèmes potentiels qui peuvent survenir lors du déploiement du service.</span><span class="sxs-lookup"><span data-stu-id="051d6-118">Adopting a ring-based deployment helps reduce potential issues that could arise while rolling out the service.</span></span> <span data-ttu-id="051d6-119">En pilotant d’abord un certain nombre d’appareils, vous pouvez identifier les problèmes potentiels et atténuer les risques potentiels qui peuvent survenir.</span><span class="sxs-lookup"><span data-stu-id="051d6-119">By piloting a certain number of devices first, you can identify potential issues and mitigate potential risks that might arise.</span></span> 


<span data-ttu-id="051d6-120">Le tableau 1 fournit un exemple des anneaux de déploiement que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="051d6-120">Table 1 provides an example of the deployment rings you might use.</span></span> 

<span data-ttu-id="051d6-121">**Tableau 1**</span><span class="sxs-lookup"><span data-stu-id="051d6-121">**Table 1**</span></span>

|<span data-ttu-id="051d6-122">**Anneau de déploiement**</span><span class="sxs-lookup"><span data-stu-id="051d6-122">**Deployment ring**</span></span>|<span data-ttu-id="051d6-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="051d6-123">**Description**</span></span>|
|:-----|:-----|
<span data-ttu-id="051d6-124">Évaluation</span><span class="sxs-lookup"><span data-stu-id="051d6-124">Evaluate</span></span> | <span data-ttu-id="051d6-125">Anneau 1 : Identifier 50 systèmes pour les tests pilotes</span><span class="sxs-lookup"><span data-stu-id="051d6-125">Ring 1: Identify 50 systems for pilot testing</span></span> 
<span data-ttu-id="051d6-126">Pilote</span><span class="sxs-lookup"><span data-stu-id="051d6-126">Pilot</span></span> | <span data-ttu-id="051d6-127">Anneau 2 : identifier les 50 à 100 points de terminaison suivants dans l’environnement de production</span><span class="sxs-lookup"><span data-stu-id="051d6-127">Ring 2: Identify the next 50-100  endpoints in production environment</span></span> <br>  
<span data-ttu-id="051d6-128">Déploiement complet</span><span class="sxs-lookup"><span data-stu-id="051d6-128">Full deployment</span></span> | <span data-ttu-id="051d6-129">Anneau 3 : déployer le service dans le reste de l’environnement par incréments plus importants</span><span class="sxs-lookup"><span data-stu-id="051d6-129">Ring 3: Roll out service to the rest of environment in larger increments</span></span>



### <a name="exit-criteria"></a><span data-ttu-id="051d6-130">Critères de sortie</span><span class="sxs-lookup"><span data-stu-id="051d6-130">Exit criteria</span></span>
<span data-ttu-id="051d6-131">Voici un exemple de critères de sortie pour ces anneaux :</span><span class="sxs-lookup"><span data-stu-id="051d6-131">An example set of exit criteria for these rings can include:</span></span>
- <span data-ttu-id="051d6-132">Les appareils s’affichent dans la liste d’inventaire des appareils</span><span class="sxs-lookup"><span data-stu-id="051d6-132">Devices show up in the device inventory list</span></span>
- <span data-ttu-id="051d6-133">Les alertes apparaissent dans le tableau de bord</span><span class="sxs-lookup"><span data-stu-id="051d6-133">Alerts appear in dashboard</span></span>
- [<span data-ttu-id="051d6-134">Exécuter un test de détection</span><span class="sxs-lookup"><span data-stu-id="051d6-134">Run a detection test</span></span>](run-detection-test.md)
- [<span data-ttu-id="051d6-135">Exécuter une attaque simulée sur un appareil</span><span class="sxs-lookup"><span data-stu-id="051d6-135">Run a simulated attack on a device</span></span>](attack-simulations.md)

### <a name="evaluate"></a><span data-ttu-id="051d6-136">Évaluation</span><span class="sxs-lookup"><span data-stu-id="051d6-136">Evaluate</span></span>
<span data-ttu-id="051d6-137">Identifiez un petit nombre d’ordinateurs de test dans votre environnement pour intégrer le service.</span><span class="sxs-lookup"><span data-stu-id="051d6-137">Identify a small number of test machines in your environment to onboard to the service.</span></span> <span data-ttu-id="051d6-138">Dans l’idéal, ces ordinateurs doivent être inférieurs à 50 points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="051d6-138">Ideally, these machines would be fewer than 50 endpoints.</span></span> 


### <a name="pilot"></a><span data-ttu-id="051d6-139">Pilote</span><span class="sxs-lookup"><span data-stu-id="051d6-139">Pilot</span></span>
<span data-ttu-id="051d6-140">Microsoft Defender pour le point de terminaison prend en charge divers points de terminaison que vous pouvez intégrer au service.</span><span class="sxs-lookup"><span data-stu-id="051d6-140">Microsoft Defender for Endpoint supports a variety of endpoints that you can onboard to the service.</span></span> <span data-ttu-id="051d6-141">Dans cet anneau, identifiez plusieurs appareils à intégrer et, en fonction des critères de sortie que vous définissez, décidez de passer à l’anneau de déploiement suivant.</span><span class="sxs-lookup"><span data-stu-id="051d6-141">In this ring, identify several devices to onboard and based on the exit criteria you define, decide to proceed to the next deployment ring.</span></span>

<span data-ttu-id="051d6-142">Le tableau suivant présente les points de terminaison pris en charge et l’outil correspondant que vous pouvez utiliser pour intégrer des appareils au service.</span><span class="sxs-lookup"><span data-stu-id="051d6-142">The following table shows the supported endpoints and the corresponding tool you can use to onboard devices to the service.</span></span> 

| <span data-ttu-id="051d6-143">Point de terminaison</span><span class="sxs-lookup"><span data-stu-id="051d6-143">Endpoint</span></span>     | <span data-ttu-id="051d6-144">Outil de déploiement</span><span class="sxs-lookup"><span data-stu-id="051d6-144">Deployment tool</span></span>                       |
|--------------|------------------------------------------|
| <span data-ttu-id="051d6-145">**Windows**</span><span class="sxs-lookup"><span data-stu-id="051d6-145">**Windows**</span></span>  |  [<span data-ttu-id="051d6-146">Script local (jusqu’à 10 appareils)</span><span class="sxs-lookup"><span data-stu-id="051d6-146">Local script (up to 10 devices)</span></span>](configure-endpoints-script.md) <br> <span data-ttu-id="051d6-147">REMARQUE : si vous souhaitez déployer plus de 10 appareils dans un environnement de production, utilisez plutôt la méthode de stratégie de groupe ou les autres outils pris en charge répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="051d6-147">NOTE: If you want to deploy more than 10 devices in a production environment, use the Group Policy method instead or the other supported tools listed below.</span></span><br>  [<span data-ttu-id="051d6-148">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="051d6-148">Group Policy</span></span>](configure-endpoints-gp.md) <br>  [<span data-ttu-id="051d6-149">Microsoft Endpoint Manager/ Gestionnaire de périphériques mobiles</span><span class="sxs-lookup"><span data-stu-id="051d6-149">Microsoft Endpoint Manager/ Mobile Device Manager</span></span>](configure-endpoints-mdm.md) <br>   [<span data-ttu-id="051d6-150">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="051d6-150">Microsoft Endpoint Configuration Manager</span></span>](configure-endpoints-sccm.md) <br> [<span data-ttu-id="051d6-151">Scripts VDI</span><span class="sxs-lookup"><span data-stu-id="051d6-151">VDI scripts</span></span>](configure-endpoints-vdi.md)   |
| <span data-ttu-id="051d6-152">**MacOS**</span><span class="sxs-lookup"><span data-stu-id="051d6-152">**macOS**</span></span>    | [<span data-ttu-id="051d6-153">Script local</span><span class="sxs-lookup"><span data-stu-id="051d6-153">Local script</span></span>](mac-install-manually.md) <br> [<span data-ttu-id="051d6-154">Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="051d6-154">Microsoft Endpoint Manager</span></span>](mac-install-with-intune.md) <br> [<span data-ttu-id="051d6-155">JamF Pro</span><span class="sxs-lookup"><span data-stu-id="051d6-155">JAMF Pro</span></span>](mac-install-with-jamf.md) <br> [<span data-ttu-id="051d6-156">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="051d6-156">Mobile Device Management</span></span>](mac-install-with-other-mdm.md) |
| <span data-ttu-id="051d6-157">**Serveur Linux**</span><span class="sxs-lookup"><span data-stu-id="051d6-157">**Linux Server**</span></span> | [<span data-ttu-id="051d6-158">Script local</span><span class="sxs-lookup"><span data-stu-id="051d6-158">Local script</span></span>](linux-install-manually.md) <br> [<span data-ttu-id="051d6-159">Sondent</span><span class="sxs-lookup"><span data-stu-id="051d6-159">Puppet</span></span>](linux-install-with-puppet.md) <br> [<span data-ttu-id="051d6-160">Ansible</span><span class="sxs-lookup"><span data-stu-id="051d6-160">Ansible</span></span>](linux-install-with-ansible.md)|
| <span data-ttu-id="051d6-161">**iOS**</span><span class="sxs-lookup"><span data-stu-id="051d6-161">**iOS**</span></span>      | [<span data-ttu-id="051d6-162">Basée sur l’application</span><span class="sxs-lookup"><span data-stu-id="051d6-162">App-based</span></span>](ios-install.md)                                |
| <span data-ttu-id="051d6-163">**Android**</span><span class="sxs-lookup"><span data-stu-id="051d6-163">**Android**</span></span>  | [<span data-ttu-id="051d6-164">Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="051d6-164">Microsoft Endpoint Manager</span></span>](android-intune.md)               | 




### <a name="full-deployment"></a><span data-ttu-id="051d6-165">Déploiement complet</span><span class="sxs-lookup"><span data-stu-id="051d6-165">Full deployment</span></span>
<span data-ttu-id="051d6-166">À ce stade, vous pouvez utiliser le matériel de [déploiement de plan](deployment-strategy.md) pour vous aider à planifier votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="051d6-166">At this stage, you can use the [Plan deployment](deployment-strategy.md) material to help you plan your deployment.</span></span> 


<span data-ttu-id="051d6-167">Utilisez les documents suivants pour sélectionner l’architecture microsoft Defender pour point de terminaison appropriée qui convient le mieux à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="051d6-167">Use the following material to select the appropriate Microsoft Defender for Endpoint architecture that best suites your organization.</span></span>

|<span data-ttu-id="051d6-168">**Élément**</span><span class="sxs-lookup"><span data-stu-id="051d6-168">**Item**</span></span>|<span data-ttu-id="051d6-169">**Description**</span><span class="sxs-lookup"><span data-stu-id="051d6-169">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="051d6-170">[![Image miniature de la stratégie de déploiement de microsoft Defender pour les points de terminaison](images/mdatp-deployment-strategy.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf)</span><span class="sxs-lookup"><span data-stu-id="051d6-170">[![Thumb image for Microsoft Defender for Endpoint deployment strategy](images/mdatp-deployment-strategy.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf)</span></span><br/> <span data-ttu-id="051d6-171">[PDF](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf)  \| [Visio](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.vsdx)</span><span class="sxs-lookup"><span data-stu-id="051d6-171">[PDF](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf)  \| [Visio](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.vsdx)</span></span> | <span data-ttu-id="051d6-172">Le matériel architectural vous aide à planifier votre déploiement pour les architectures suivantes :</span><span class="sxs-lookup"><span data-stu-id="051d6-172">The architectural material helps you plan your deployment for the following architectures:</span></span> <ul><li> <span data-ttu-id="051d6-173">Cloud-natif</span><span class="sxs-lookup"><span data-stu-id="051d6-173">Cloud-native</span></span> </li><li> <span data-ttu-id="051d6-174">Cogestion</span><span class="sxs-lookup"><span data-stu-id="051d6-174">Co-management</span></span> </li><li> <span data-ttu-id="051d6-175">Sur site</span><span class="sxs-lookup"><span data-stu-id="051d6-175">On-premise</span></span></li><li><span data-ttu-id="051d6-176">Évaluation et intégration locale</span><span class="sxs-lookup"><span data-stu-id="051d6-176">Evaluation and local onboarding</span></span></li>




## <a name="existing-deployments"></a><span data-ttu-id="051d6-177">Déploiements existants</span><span class="sxs-lookup"><span data-stu-id="051d6-177">Existing deployments</span></span>

### <a name="windows-endpoints"></a><span data-ttu-id="051d6-178">Windows de terminaison</span><span class="sxs-lookup"><span data-stu-id="051d6-178">Windows endpoints</span></span>
<span data-ttu-id="051d6-179">Pour Windows serveurs et/ou Windows, vous sélectionnez plusieurs ordinateurs à tester à l’avance (avant le correctif de mardi) à l’aide du programme DE VALIDATION de mise à jour de sécurité **(PROGRAMME).**</span><span class="sxs-lookup"><span data-stu-id="051d6-179">For Windows and/or Windows Servers, you select several machines to test ahead of time (before patch Tuesday) by using the **Security Update Validation program (SUVP)**.</span></span>

<span data-ttu-id="051d6-180">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="051d6-180">For more information, see:</span></span>
- [<span data-ttu-id="051d6-181">Qu’est-ce que le programme de validation des mises à jour de sécurité ?</span><span class="sxs-lookup"><span data-stu-id="051d6-181">What is the Security Update Validation Program</span></span>](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/what-is-the-security-update-validation-program/ba-p/275767)
- [<span data-ttu-id="051d6-182">Programme de validation de mise à jour logicielle et établissement Centre de protection Microsoft contre les programmes malveillants - Chronologie interactive TwC partie 4</span><span class="sxs-lookup"><span data-stu-id="051d6-182">Software Update Validation Program and Microsoft Malware Protection Center Establishment - TwC Interactive Timeline Part 4</span></span>](https://www.microsoft.com/security/blog/2012/03/28/software-update-validation-program-and-microsoft-malware-protection-center-establishment-twc-interactive-timeline-part-4/)


### <a name="non-windows-endpoints"></a><span data-ttu-id="051d6-183">Points de terminaison Windows non-Windows</span><span class="sxs-lookup"><span data-stu-id="051d6-183">Non-Windows endpoints</span></span>
<span data-ttu-id="051d6-184">Avec macOS et Linux, vous pouvez prendre quelques systèmes et les exécuter dans le canal bêta.</span><span class="sxs-lookup"><span data-stu-id="051d6-184">With macOS and Linux, you could take a couple of systems and run in the Beta channel.</span></span>

>[!NOTE]
><span data-ttu-id="051d6-185">Dans l’idéal, au moins un administrateur de sécurité et un développeur sont en mesure de trouver des problèmes de compatibilité, de performances et de fiabilité avant que la build n’entre dans le canal actuel.</span><span class="sxs-lookup"><span data-stu-id="051d6-185">Ideally at least one security admin and one developer so that you are able to find compatibility, performance and reliability issues before the build makes it into the Current channel.</span></span>

<span data-ttu-id="051d6-186">Le choix du canal détermine le type et la fréquence des mises à jour proposées à votre appareil.</span><span class="sxs-lookup"><span data-stu-id="051d6-186">The choice of the channel determines the type and frequency of updates that are offered to your device.</span></span> <span data-ttu-id="051d6-187">Les appareils en version bêta sont les premiers à recevoir des mises à jour et de nouvelles fonctionnalités, suivis plus tard de la prévisualisation et enfin de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="051d6-187">Devices in Beta are the first ones to receive updates and new features, followed later by Preview and lastly by Current.</span></span>

![Image des anneaux internes](images/insider-rings.png)

<span data-ttu-id="051d6-189">Pour prévisualiser les nouvelles fonctionnalités et fournir des commentaires préliminaires, il est recommandé de configurer certains appareils de votre entreprise pour qu’ils utilisent la version bêta ou la prévisualisation.</span><span class="sxs-lookup"><span data-stu-id="051d6-189">In order to preview new features and provide early feedback, it is recommended that you configure some devices in your enterprise to use either Beta or Preview.</span></span>

>[!WARNING]
><span data-ttu-id="051d6-190">Le basculement du canal après l’installation initiale nécessite la réinstallation du produit.</span><span class="sxs-lookup"><span data-stu-id="051d6-190">Switching the channel after the initial installation requires the product to be reinstalled.</span></span> <span data-ttu-id="051d6-191">Pour basculer le canal de produit : désinstallez le package existant, configurez de nouveau votre appareil pour utiliser le nouveau canal et suivez les étapes de ce document pour installer le package à partir du nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="051d6-191">To switch the product channel: uninstall the existing package, re-configure your device to use the new channel, and follow the steps in this document to install the package from the new location.</span></span>
