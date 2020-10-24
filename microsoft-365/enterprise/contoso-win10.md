---
title: Déploiement de Windows 10 Entreprise pour Contoso
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
ms.author: josephd
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-modern-desktop
- Strat_O365_Enterprise
ms.custom: ''
description: Comprendre la façon dont Contoso a utilisé Microsoft Endpoint Configuration Manager pour déployer les mises à niveau sur place pour Windows 10 Entreprise.
ms.openlocfilehash: 0543f24665048d0679bc1b099fdd0a2d431c1e54
ms.sourcegitcommit: 66b8fc1d8ba4f17487cd2004ac19cf2fff472f3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2020
ms.locfileid: "48754246"
---
# <a name="windows-10-enterprise-deployment-for-contoso"></a><span data-ttu-id="72757-103">Déploiement de Windows 10 Entreprise pour Contoso</span><span class="sxs-lookup"><span data-stu-id="72757-103">Windows 10 Enterprise deployment for Contoso</span></span>

<span data-ttu-id="72757-p101">Avant le déploiement étendu de Microsoft 365 pour Enterprise, contoso disposait de PC et de périphériques compatibles avec Windows qui exécutent un mélange de Windows 7 (10%), de Windows 8,1 (65%) et de Windows 10 (25%). Contoso souhaitait mettre à niveau ses PC pour Windows 10 entreprise tirer parti de la sécurité avancée et avoir réduit les charges de travail informatiques des déploiements automatisés de mises à jour.</span><span class="sxs-lookup"><span data-stu-id="72757-p101">Prior to the wide rollout of Microsoft 365 for enterprise, Contoso had Windows-compatible PCs and devices running a mixture of Windows 7 (10%), Windows 8.1 (65%), and Windows 10 (25%). Contoso wanted to upgrade their PCs for Windows 10 Enterprise take advantage of advanced security and lowered IT overhead from automated deployments of updates.</span></span> 

<span data-ttu-id="72757-106">Après évaluation de ses besoins d’infrastructure et de ses besoins métier, Contoso a identifié les exigences principales suivantes en matière de déploiement :</span><span class="sxs-lookup"><span data-stu-id="72757-106">After assessing their infrastructure and business needs, Contoso identified these key requirements for the deployment:</span></span>

- <span data-ttu-id="72757-107">Le plus possible de PC et de périphériques doivent exécuter Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="72757-107">As many PCs and devices as possible should run Windows 10 Enterprise</span></span>
- <span data-ttu-id="72757-108">Déploiement des mises à niveau sur place exploitant l’infrastructure Configuration Manager existante</span><span class="sxs-lookup"><span data-stu-id="72757-108">Rollout of the in-place upgrades leverages existing Configuration Manager infrastructure</span></span>
- <span data-ttu-id="72757-109">Contrôler les versions de Windows 10 Entreprise à déployer, et les mises à jour sont effectuées via des anneaux</span><span class="sxs-lookup"><span data-stu-id="72757-109">Control over which versions of Windows 10 Enterprise to deploy and updates are done through rings</span></span>
- <span data-ttu-id="72757-110">Les PC et les périphériques doivent rester à jour moyennant des coûts d’administration informatique minimes et avec un faible impact pour les utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="72757-110">PCs and devices should stay up to date with minimal IT administrative costs and with minimal impact to end-users</span></span>

<span data-ttu-id="72757-111">Une version « à jour » est définie comme la version de Windows 10 Entreprise prise en charge qui répond aux besoins métier de Contoso, ce qui peut être différent d’avoir tous les PC compatibles avec Windows exécutant la dernière version de Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="72757-111">Up to date is defined as the supported version of Windows 10 Enterprise that meets Contoso’s business needs, which can be different from having all Windows-compatible PCs running the latest version of Windows 10 Enterprise.</span></span>

## <a name="deployment-tools"></a><span data-ttu-id="72757-112">Outils de déploiement</span><span class="sxs-lookup"><span data-stu-id="72757-112">Deployment tools</span></span>

<span data-ttu-id="72757-113">Avant et pendant les mises à niveau sur place de Windows 10 Entreprise, Contoso a utilisé les solutions de Windows Analytics suivantes :</span><span class="sxs-lookup"><span data-stu-id="72757-113">Prior to and during in-place upgrades of Windows 10 Enterprise, Contoso used the following solutions of Windows Analytics:</span></span>

- <span data-ttu-id="72757-114">Préparation des mises à niveau</span><span class="sxs-lookup"><span data-stu-id="72757-114">Upgrade Readiness</span></span>  

  <span data-ttu-id="72757-115">Collecte les données du pilote, des applications et du système en vue d’une analyse, puis identifie les problèmes de compatibilité susceptibles d’empêcher une mise à niveau et les correctifs aux problèmes suggérés et connus par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="72757-115">Collects system, application, and driver data for analysis, and then identifies compatibility issues that can block an upgrade and suggested fixes the issues are known to Microsoft.</span></span>

- <span data-ttu-id="72757-116">Conformité des mises à niveau</span><span class="sxs-lookup"><span data-stu-id="72757-116">Update Compliance</span></span>  

  <span data-ttu-id="72757-117">Indique l’état de vos appareils par rapport aux mises à jour Windows, afin que vous puissiez vous assurer que ceux-ci disposent des mises à jour les plus récentes, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="72757-117">Shows you the state of your devices with respect to the Windows updates so that you can ensure that they are on the most current updates as appropriate.</span></span>

- <span data-ttu-id="72757-118">Intégrité du périphérique</span><span class="sxs-lookup"><span data-stu-id="72757-118">Device Health</span></span>  

  <span data-ttu-id="72757-119">Identifie les appareils qui se bloquent fréquemment et qui, par conséquent, doivent être recréés ou remplacés et les pilotes de périphériques qui provoquent des blocages sur les appareils, avec des suggestions d’autres versions de ces pilotes susceptibles de réduire le nombre d’incidents.</span><span class="sxs-lookup"><span data-stu-id="72757-119">Identifies devices that crash frequently, and therefore might need to be rebuilt or replaced and device drivers that are causing device crashes, with suggestions of alternative versions of those drivers that might reduce the number of crashes.</span></span> <span data-ttu-id="72757-120">Fournit une notification de configurations incorrectes de la Protection des informations Windows qui envoient des invites à des utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="72757-120">Provides notification of Windows Information Protection misconfigurations that send prompts to end users.</span></span>
 
<span data-ttu-id="72757-p103">Contoso dispose d’une infrastructure Configuration Manager (branche actuelle) existante. Le gestionnaire de configuration s’adapte à des environnements volumineux et offre un contrôle extensif sur l’installation, les mises à jour et les paramètres. Il dispose également de fonctionnalités intégrées pour simplifier et accroître l’efficacité du déploiement et de la gestion de Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="72757-p103">Contoso has an existing Configuration Manager (Current Branch) infrastructure. Configuration Manager scales for large environments and provides extensive control over installation, updates, and settings. It also has built-in features to make it easier and more efficient to deploy and manage Windows 10 Enterprise.</span></span>

## <a name="planning-process"></a><span data-ttu-id="72757-124">Processus de planification</span><span class="sxs-lookup"><span data-stu-id="72757-124">Planning process</span></span>

<span data-ttu-id="72757-125">Contoso a utilisé la préparation à la mise à niveau dans Windows Analytics pour déterminer l’ensemble des applications installées et leur compatibilité avec Windows 10 entreprise.</span><span class="sxs-lookup"><span data-stu-id="72757-125">Contoso used the Upgrade Readiness in Windows Analytics to determine the set of installed apps and their compatibility with Windows 10 Enterprise.</span></span>

## <a name="deployment-process"></a><span data-ttu-id="72757-126">Processus de déploiement</span><span class="sxs-lookup"><span data-stu-id="72757-126">Deployment process</span></span>

<span data-ttu-id="72757-127">Pour effectuer le déploiement de mises à niveau sur place de Windows 10 Entreprise, Contoso a implémenté le processus suivant, qui inclut les recommandations concernant les meilleures pratiques de Microsoft suivantes :</span><span class="sxs-lookup"><span data-stu-id="72757-127">To complete the in-place upgrade deployment of Windows 10 Enterprise, Contoso implemented the following process, which includes best practice recommendations from Microsoft:</span></span>

1. <span data-ttu-id="72757-128">Activation d’un cache d’homologue pour le gestionnaire de configuration</span><span class="sxs-lookup"><span data-stu-id="72757-128">Enabled peer cache for Configuration Manager.</span></span>
2. <span data-ttu-id="72757-129">Création de packages Windows personnalisés basés sur des images du centre de service de gestion des licences en volume</span><span class="sxs-lookup"><span data-stu-id="72757-129">Created customized Windows packages based on images from the Volume Licensing Service Center.</span></span>
3. <span data-ttu-id="72757-130">Utilisez le gestionnaire de configuration pour déployer les packages Windows sur les points de distribution sur le réseau et les versions déployées vers les trois groupes de test de validation et de déploiement.</span><span class="sxs-lookup"><span data-stu-id="72757-130">Used Configuration Manager to deploy the Windows packages to distribution points across their network and deployed builds to the three validation and deployment staging groups.</span></span>
4. <span data-ttu-id="72757-131">Exécution de l’évaluation de réussite pour les PC et les périphériques dans les trois anneaux de gestion intermédiaire de la validation et du déploiement utilisant des solutions de conformité de mise à jour et d’intégrité des périphériques de Windows Analytics.</span><span class="sxs-lookup"><span data-stu-id="72757-131">Performed assessment of success for PCs and devices in the three validation and deployment staging rings using the Device Health and Update Compliance solutions of Windows Analytics.</span></span>
5. <span data-ttu-id="72757-132">En fonction des informations Windows Analytics, Contoso a déterminé la version de Windows 10 entreprise à déployer dans le groupe de déploiement large.</span><span class="sxs-lookup"><span data-stu-id="72757-132">Based on the Windows Analytics information, Contoso determined the version of Windows 10 Enterprise to deploy to the broad deployment group.</span></span>
6. <span data-ttu-id="72757-133">Exécutez les séquences de tâches de déploiement du gestionnaire de configuration pour déployer le package Windows sélectionné dans le groupe de déploiement large.</span><span class="sxs-lookup"><span data-stu-id="72757-133">Ran the Configuration Manager deployment task sequences to deploy the selected Windows package to the broad deployment group.</span></span>
7. <span data-ttu-id="72757-134">Surveillance des PC et des appareils dans le groupe de déploiement large à l’aide des solutions d’intégrité des appareils et de conformité des mises à jour pour résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="72757-134">Monitored PCs and devices in the broad deployment group using the Device Health and Update Compliance solutions to address issues.</span></span>

<span data-ttu-id="72757-135">Voici la mise à niveau sur place et l’architecture de déploiement de mises à jour en cours de Contoso.</span><span class="sxs-lookup"><span data-stu-id="72757-135">Here is Contoso’s in-place upgrade and ongoing updates deployment architecture.</span></span>

![Infrastructure de déploiement de Windows 10 Entreprise de Contoso](../media/contoso-win10/contoso-win10-fig1.png)

<span data-ttu-id="72757-137">Cette infrastructure se compose des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="72757-137">This infrastructure consists of:</span></span>

- <span data-ttu-id="72757-138">Configuration Manager, qui :</span><span class="sxs-lookup"><span data-stu-id="72757-138">Configuration Manager, which:</span></span>
  - <span data-ttu-id="72757-139">obtient des images pour les packages Windows 10 Entreprise à partir du centre de gestion des licences en volume Microsoft dans The Microsoft Network ;</span><span class="sxs-lookup"><span data-stu-id="72757-139">Obtains images for Windows 10 Enterprise packages from the Microsoft Volume Licensing Center in the Microsoft Network.</span></span>
  - <span data-ttu-id="72757-140">est le point d’administration central pour les packages de déploiement.</span><span class="sxs-lookup"><span data-stu-id="72757-140">Is the central administration point for deployment packages.</span></span>
- <span data-ttu-id="72757-141">Les points de distribution régionaux généralement situés dans les centres régionaux de Contoso.</span><span class="sxs-lookup"><span data-stu-id="72757-141">Regional distribution points that are typically located in Contoso’s regional hub offices.</span></span>
- <span data-ttu-id="72757-142">PC et appareils Windows dans divers emplacements qui reçoivent et installent les packages de déploiement pour la mise à niveau sur place ou les mises à jour en continu en fonction de l’appartenance au groupe.</span><span class="sxs-lookup"><span data-stu-id="72757-142">Windows PCs and devices in various locations that receive and install the deployment packages for the in-place upgrade or ongoing updates based on group membership.</span></span>

## <a name="next-step"></a><span data-ttu-id="72757-143">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="72757-143">Next step</span></span>

<span data-ttu-id="72757-144">Découvrez comment contoso exploite son infrastructure de gestionnaire de configuration pour [déployer et conserver les applications Microsoft 365 actuelles pour les entreprises](contoso-o365pp.md) au sein de son organisation.</span><span class="sxs-lookup"><span data-stu-id="72757-144">Learn how Contoso is leveraging its Configuration Manager infrastructure to [deploy and keep current Microsoft 365 Apps for enterprise](contoso-o365pp.md) across its organization.</span></span> 

## <a name="see-also"></a><span data-ttu-id="72757-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72757-145">See also</span></span>

[<span data-ttu-id="72757-146">Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="72757-146">Windows 10 Enterprise</span></span>](https://docs.microsoft.com/windows/deployment/)

[<span data-ttu-id="72757-147">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="72757-147">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="72757-148">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="72757-148">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)
