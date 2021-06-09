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
ms.openlocfilehash: 7907bf64acce3af8b21459202cb6f5cbc1e9f990
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50907685"
---
# <a name="windows-10-enterprise-deployment-for-contoso"></a><span data-ttu-id="1a90b-103">Déploiement de Windows 10 Entreprise pour Contoso</span><span class="sxs-lookup"><span data-stu-id="1a90b-103">Windows 10 Enterprise deployment for Contoso</span></span>

<span data-ttu-id="1a90b-104">Avant le déploiement large de Microsoft 365 pour entreprise, Contoso avait des PC et périphériques compatibles Windows exécutant une combinaison de Windows 7 (10 %) Windows 8.1 (65 %) et Windows 10 (25 %).</span><span class="sxs-lookup"><span data-stu-id="1a90b-104">Prior to the wide rollout of Microsoft 365 for enterprise, Contoso had Windows-compatible PCs and devices running a mixture of Windows 7 (10%), Windows 8.1 (65%), and Windows 10 (25%).</span></span> <span data-ttu-id="1a90b-105">Contoso souhaitait mettre à niveau ses PC pour Windows 10 Entreprise tirer parti de la sécurité avancée et réduire la surcharge informatique des déploiements automatisés de mises à jour.</span><span class="sxs-lookup"><span data-stu-id="1a90b-105">Contoso wanted to upgrade their PCs for Windows 10 Enterprise take advantage of advanced security and lowered IT overhead from automated deployments of updates.</span></span> 

<span data-ttu-id="1a90b-106">Après évaluation de ses besoins d’infrastructure et de ses besoins métier, Contoso a identifié les exigences principales suivantes en matière de déploiement :</span><span class="sxs-lookup"><span data-stu-id="1a90b-106">After assessing their infrastructure and business needs, Contoso identified these key requirements for the deployment:</span></span>

- <span data-ttu-id="1a90b-107">Le plus possible de PC et de périphériques doivent exécuter Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="1a90b-107">As many PCs and devices as possible should run Windows 10 Enterprise</span></span>
- <span data-ttu-id="1a90b-108">Déploiement des mises à niveau sur place exploitant l’infrastructure Configuration Manager existante</span><span class="sxs-lookup"><span data-stu-id="1a90b-108">Rollout of the in-place upgrades leverages existing Configuration Manager infrastructure</span></span>
- <span data-ttu-id="1a90b-109">Contrôler les versions de Windows 10 Entreprise à déployer, et les mises à jour sont effectuées via des anneaux</span><span class="sxs-lookup"><span data-stu-id="1a90b-109">Control over which versions of Windows 10 Enterprise to deploy and updates are done through rings</span></span>
- <span data-ttu-id="1a90b-110">Les PC et les périphériques doivent rester à jour moyennant des coûts d’administration informatique minimes et avec un faible impact pour les utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="1a90b-110">PCs and devices should stay up to date with minimal IT administrative costs and with minimal impact to end-users</span></span>

<span data-ttu-id="1a90b-111">Une version « à jour » est définie comme la version de Windows 10 Entreprise prise en charge qui répond aux besoins métier de Contoso, ce qui peut être différent d’avoir tous les PC compatibles avec Windows exécutant la dernière version de Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="1a90b-111">Up to date is defined as the supported version of Windows 10 Enterprise that meets Contoso’s business needs, which can be different from having all Windows-compatible PCs running the latest version of Windows 10 Enterprise.</span></span>

## <a name="deployment-tools"></a><span data-ttu-id="1a90b-112">Outils de déploiement</span><span class="sxs-lookup"><span data-stu-id="1a90b-112">Deployment tools</span></span>

<span data-ttu-id="1a90b-113">Avant et pendant les mises à niveau sur place de Windows 10 Entreprise, Contoso a utilisé les solutions de Windows Analytics suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a90b-113">Prior to and during in-place upgrades of Windows 10 Enterprise, Contoso used the following solutions of Windows Analytics:</span></span>

- <span data-ttu-id="1a90b-114">Préparation des mises à niveau</span><span class="sxs-lookup"><span data-stu-id="1a90b-114">Upgrade Readiness</span></span>  

  <span data-ttu-id="1a90b-115">Collecte les données du pilote, des applications et du système en vue d’une analyse, puis identifie les problèmes de compatibilité susceptibles d’empêcher une mise à niveau et les correctifs aux problèmes suggérés et connus par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1a90b-115">Collects system, application, and driver data for analysis, and then identifies compatibility issues that can block an upgrade and suggested fixes the issues are known to Microsoft.</span></span>

- <span data-ttu-id="1a90b-116">Conformité des mises à niveau</span><span class="sxs-lookup"><span data-stu-id="1a90b-116">Update Compliance</span></span>  

  <span data-ttu-id="1a90b-117">Indique l’état de vos appareils par rapport aux mises à jour Windows, afin que vous puissiez vous assurer que ceux-ci disposent des mises à jour les plus récentes, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1a90b-117">Shows you the state of your devices with respect to the Windows updates so that you can ensure that they are on the most current updates as appropriate.</span></span>

- <span data-ttu-id="1a90b-118">Intégrité du périphérique</span><span class="sxs-lookup"><span data-stu-id="1a90b-118">Device Health</span></span>  

  <span data-ttu-id="1a90b-119">Identifie les appareils qui se bloquent fréquemment et qui, par conséquent, doivent être recréés ou remplacés et les pilotes de périphériques qui provoquent des blocages sur les appareils, avec des suggestions d’autres versions de ces pilotes susceptibles de réduire le nombre d’incidents.</span><span class="sxs-lookup"><span data-stu-id="1a90b-119">Identifies devices that crash frequently, and therefore might need to be rebuilt or replaced and device drivers that are causing device crashes, with suggestions of alternative versions of those drivers that might reduce the number of crashes.</span></span> <span data-ttu-id="1a90b-120">Fournit une notification de configurations incorrectes de la Protection des informations Windows qui envoient des invites à des utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="1a90b-120">Provides notification of Windows Information Protection misconfigurations that send prompts to end users.</span></span>
 
<span data-ttu-id="1a90b-p103">Contoso dispose d’une infrastructure Configuration Manager (branche actuelle) existante. Le gestionnaire de configuration s’adapte à des environnements volumineux et offre un contrôle extensif sur l’installation, les mises à jour et les paramètres. Il dispose également de fonctionnalités intégrées pour simplifier et accroître l’efficacité du déploiement et de la gestion de Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="1a90b-p103">Contoso has an existing Configuration Manager (Current Branch) infrastructure. Configuration Manager scales for large environments and provides extensive control over installation, updates, and settings. It also has built-in features to make it easier and more efficient to deploy and manage Windows 10 Enterprise.</span></span>

## <a name="planning-process"></a><span data-ttu-id="1a90b-124">Processus de planification</span><span class="sxs-lookup"><span data-stu-id="1a90b-124">Planning process</span></span>

<span data-ttu-id="1a90b-125">Contoso a utilisé upgrade readiness dans Windows Analytics pour déterminer l’ensemble des applications installées et leur compatibilité avec Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="1a90b-125">Contoso used the Upgrade Readiness in Windows Analytics to determine the set of installed apps and their compatibility with Windows 10 Enterprise.</span></span>

## <a name="deployment-process"></a><span data-ttu-id="1a90b-126">Processus de déploiement</span><span class="sxs-lookup"><span data-stu-id="1a90b-126">Deployment process</span></span>

<span data-ttu-id="1a90b-127">Pour effectuer le déploiement de mises à niveau sur place de Windows 10 Entreprise, Contoso a implémenté le processus suivant, qui inclut les recommandations concernant les meilleures pratiques de Microsoft suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a90b-127">To complete the in-place upgrade deployment of Windows 10 Enterprise, Contoso implemented the following process, which includes best practice recommendations from Microsoft:</span></span>

1. <span data-ttu-id="1a90b-128">Activation d’un cache d’homologue pour le gestionnaire de configuration</span><span class="sxs-lookup"><span data-stu-id="1a90b-128">Enabled peer cache for Configuration Manager.</span></span>
2. <span data-ttu-id="1a90b-129">Création de packages Windows personnalisés basés sur des images du centre de service de gestion des licences en volume</span><span class="sxs-lookup"><span data-stu-id="1a90b-129">Created customized Windows packages based on images from the Volume Licensing Service Center.</span></span>
3. <span data-ttu-id="1a90b-130">Utilisé Configuration Manager pour déployer les packages Windows vers les points de distribution sur leur réseau et les builds déployées sur les trois groupes de transit de validation et de déploiement.</span><span class="sxs-lookup"><span data-stu-id="1a90b-130">Used Configuration Manager to deploy the Windows packages to distribution points across their network and deployed builds to the three validation and deployment staging groups.</span></span>
4. <span data-ttu-id="1a90b-131">Exécution de l’évaluation de réussite pour les PC et les périphériques dans les trois anneaux de gestion intermédiaire de la validation et du déploiement utilisant des solutions de conformité de mise à jour et d’intégrité des périphériques de Windows Analytics.</span><span class="sxs-lookup"><span data-stu-id="1a90b-131">Performed assessment of success for PCs and devices in the three validation and deployment staging rings using the Device Health and Update Compliance solutions of Windows Analytics.</span></span>
5. <span data-ttu-id="1a90b-132">Sur la base des Windows analytics, Contoso a déterminé la version de Windows 10 Entreprise à déployer vers le groupe de déploiement à grande échelle.</span><span class="sxs-lookup"><span data-stu-id="1a90b-132">Based on the Windows Analytics information, Contoso determined the version of Windows 10 Enterprise to deploy to the broad deployment group.</span></span>
6. <span data-ttu-id="1a90b-133">A lancé les séquences de tâches de déploiement configuration Manager pour déployer le package Windows sélectionné dans le groupe de déploiement étendu.</span><span class="sxs-lookup"><span data-stu-id="1a90b-133">Ran the Configuration Manager deployment task sequences to deploy the selected Windows package to the broad deployment group.</span></span>
7. <span data-ttu-id="1a90b-134">Pc et appareils surveillés dans le groupe de déploiement à grande échelle à l’aide des solutions de conformité d’état et de mise à jour des périphériques pour résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="1a90b-134">Monitored PCs and devices in the broad deployment group using the Device Health and Update Compliance solutions to address issues.</span></span>

<span data-ttu-id="1a90b-135">Voici la mise à niveau sur place et l’architecture de déploiement de mises à jour en cours de Contoso.</span><span class="sxs-lookup"><span data-stu-id="1a90b-135">Here is Contoso’s in-place upgrade and ongoing updates deployment architecture.</span></span>

![Infrastructure de déploiement de Windows 10 Entreprise de Contoso](../media/contoso-win10/contoso-win10-fig1.png)

<span data-ttu-id="1a90b-137">Cette infrastructure se compose des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="1a90b-137">This infrastructure consists of:</span></span>

- <span data-ttu-id="1a90b-138">Configuration Manager, qui :</span><span class="sxs-lookup"><span data-stu-id="1a90b-138">Configuration Manager, which:</span></span>
  - <span data-ttu-id="1a90b-139">obtient des images pour les packages Windows 10 Entreprise à partir du centre de gestion des licences en volume Microsoft dans The Microsoft Network ;</span><span class="sxs-lookup"><span data-stu-id="1a90b-139">Obtains images for Windows 10 Enterprise packages from the Microsoft Volume Licensing Center in the Microsoft Network.</span></span>
  - <span data-ttu-id="1a90b-140">est le point d’administration central pour les packages de déploiement.</span><span class="sxs-lookup"><span data-stu-id="1a90b-140">Is the central administration point for deployment packages.</span></span>
- <span data-ttu-id="1a90b-141">Les points de distribution régionaux généralement situés dans les centres régionaux de Contoso.</span><span class="sxs-lookup"><span data-stu-id="1a90b-141">Regional distribution points that are typically located in Contoso’s regional hub offices.</span></span>
- <span data-ttu-id="1a90b-142">Windows Pc et périphériques à différents emplacements qui reçoivent et installent les packages de déploiement pour la mise à niveau sur place ou les mises à jour en cours en fonction de l’appartenance au groupe.</span><span class="sxs-lookup"><span data-stu-id="1a90b-142">Windows PCs and devices in various locations that receive and install the deployment packages for the in-place upgrade or ongoing updates based on group membership.</span></span>

## <a name="next-step"></a><span data-ttu-id="1a90b-143">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="1a90b-143">Next step</span></span>

<span data-ttu-id="1a90b-144">Découvrez comment Contoso tire parti de son infrastructure Configuration Manager pour déployer et maintenir la Applications Microsoft 365 pour les grandes entreprises [au](contoso-o365pp.md) sein de son organisation.</span><span class="sxs-lookup"><span data-stu-id="1a90b-144">Learn how Contoso is leveraging its Configuration Manager infrastructure to [deploy and keep current Microsoft 365 Apps for enterprise](contoso-o365pp.md) across its organization.</span></span> 

## <a name="see-also"></a><span data-ttu-id="1a90b-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a90b-145">See also</span></span>

[<span data-ttu-id="1a90b-146">Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="1a90b-146">Windows 10 Enterprise</span></span>](/windows/deployment/)

[<span data-ttu-id="1a90b-147">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="1a90b-147">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="1a90b-148">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="1a90b-148">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)