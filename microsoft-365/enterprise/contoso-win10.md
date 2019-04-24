---
title: Déploiement de Windows 10 Entreprise pour Contoso
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 09/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-modern-desktop
- Strat_O365_Enterprise
ms.custom: ''
description: Comprendre la façon dont Contoso a utilisé System Center Configuration Manager pour déployer les mises à niveau sur place pour Windows 10 Entreprise.
ms.openlocfilehash: f5f8335b8769daf28b55769fc64fed6607b69eb3
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289167"
---
# <a name="windows-10-enterprise-deployment-for-contoso"></a><span data-ttu-id="395f4-103">Déploiement de Windows 10 Entreprise pour Contoso</span><span class="sxs-lookup"><span data-stu-id="395f4-103">Windows 10 Enterprise deployment for Contoso</span></span>

<span data-ttu-id="395f4-104">**Résumé :** Comprendre la façon dont Contoso a utilisé System Center Configuration Manager pour déployer les mises à niveau sur place pour Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="395f4-104">**Summary:** Understand how Contoso used System Center Configuration Manager to deploy in-place upgrades for Windows 10 Enterprise.</span></span>

<span data-ttu-id="395f4-p101">Avant le déploiement large de Microsoft 365 Entreprise, Contoso disposait de périphériques et de PC compatibles avec Windows qui exécutaient un mélange de Windows 7 (10 %), Windows 8.1 (65 %) et Windows 10 (25 %). Contoso souhaitait mettre à niveau ses PC vers Windows 10 Entreprise afin de profiter de la sécurité améliorée et des frais informatiques généraux réduits grâce aux déploiements automatisés des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="395f4-p101">Prior to the wide rollout of Microsoft 365 Enterprise, Contoso had Windows-compatible PCs and devices running a mixture of Windows 7 (10%), Windows 8.1 (65%), and Windows 10 (25%). Contoso wanted to upgrade their PCs for Windows 10 Enterprise take advantage of improved security and lowered IT overhead from automated deployments of updates.</span></span> 

<span data-ttu-id="395f4-107">Après évaluation de ses besoins d’infrastructure et de ses besoins métier, Contoso a identifié les exigences principales suivantes en matière de déploiement :</span><span class="sxs-lookup"><span data-stu-id="395f4-107">After assessing their infrastructure and business needs, Contoso identified these key requirements for the deployment:</span></span>

- <span data-ttu-id="395f4-108">Le plus possible de PC et de périphériques doivent exécuter Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="395f4-108">As many PCs and devices as possible should run Windows 10 Enterprise</span></span>
- <span data-ttu-id="395f4-109">Déploiement des mises à niveau sur place exploitant l’infrastructure System Center Configuration Manager existante</span><span class="sxs-lookup"><span data-stu-id="395f4-109">Rollout of the in-place upgrades leverages existing System Center Configuration Manager infrastructure</span></span>
- <span data-ttu-id="395f4-110">Contrôler les versions de Windows 10 Entreprise à déployer, et les mises à jour sont effectuées via des anneaux</span><span class="sxs-lookup"><span data-stu-id="395f4-110">Control over which versions of Windows 10 Enterprise to deploy and updates are done through rings</span></span>
- <span data-ttu-id="395f4-111">Les PC et les périphériques doivent rester à jour moyennant des coûts d’administration informatique minimes et avec un faible impact pour les utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="395f4-111">PCs and devices should stay up to date with minimal IT administrative costs and with minimal impact to end-users</span></span>

<span data-ttu-id="395f4-112">Une version « à jour » est définie comme la version de Windows 10 Entreprise prise en charge qui répond aux besoins métier de Contoso, ce qui peut être différent d’avoir tous les PC compatibles avec Windows exécutant la dernière version de Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="395f4-112">Up to date is defined as the supported version of Windows 10 Enterprise that meets Contoso’s business needs, which can be different from having all Windows-compatible PCs running the latest version of Windows 10 Enterprise.</span></span>

## <a name="deployment-tools"></a><span data-ttu-id="395f4-113">Outils de déploiement</span><span class="sxs-lookup"><span data-stu-id="395f4-113">Deployment tools</span></span>

<span data-ttu-id="395f4-114">Avant et pendant les mises à niveau sur place de Windows 10 Entreprise, Contoso a utilisé les solutions de Windows Analytics suivantes :</span><span class="sxs-lookup"><span data-stu-id="395f4-114">Prior to and during in-place upgrades of Windows 10 Enterprise, Contoso used the following solutions of Windows Analytics:</span></span>

- <span data-ttu-id="395f4-115">Préparation des mises à niveau</span><span class="sxs-lookup"><span data-stu-id="395f4-115">Upgrade Readiness</span></span>  

  <span data-ttu-id="395f4-116">Collecte les données du pilote, des applications et du système en vue d’une analyse, puis identifie les problèmes de compatibilité susceptibles d’empêcher une mise à niveau et les correctifs aux problèmes suggérés et connus par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="395f4-116">Collects system, application, and driver data for analysis, and then identifies compatibility issues that can block an upgrade and suggested fixes the issues are known to Microsoft.</span></span>

- <span data-ttu-id="395f4-117">Conformité des mises à niveau</span><span class="sxs-lookup"><span data-stu-id="395f4-117">Update Compliance</span></span>  

  <span data-ttu-id="395f4-118">Collecte les données de diagnostic et du système, notamment la progression de l’installation mise à jour, les données de configuration de Windows Update pour Entreprise (WUfB), les données Antivirus Windows Defender et autres informations spécifiques de la mise à jour, puis stocke ces données dans l’utilisation et l’analyse cloud.</span><span class="sxs-lookup"><span data-stu-id="395f4-118">Collects system and diagnostics data including update installation progress, Windows Update for Business (WUfB) configuration data, Windows Defender Antivirus data, and other update-specific information, and then stores this data in the cloud analysis and usage.</span></span>

- <span data-ttu-id="395f4-119">Intégrité du périphérique</span><span class="sxs-lookup"><span data-stu-id="395f4-119">Device Health</span></span>  

  <span data-ttu-id="395f4-120">Collecte les données de diagnostic et du système Windows 10, notamment la progression de l’installation mise à jour, les données de configuration de Windows Update pour Entreprise (WUfB), les données Antivirus Windows Defender et autres informations spécifiques de la mise à jour, puis stocke ces données dans l’utilisation et l’analyse cloud.</span><span class="sxs-lookup"><span data-stu-id="395f4-120">Collects Windows 10 system and diagnostic data including update installation progress, Windows Update for Business (WUfB) configuration data, Windows Defender Antivirus data, and other update-specific information, and then stores this data in the cloud analysis and usage.</span></span>
 
<span data-ttu-id="395f4-p102">Contoso dispose d’une infrastructure System Center Configuration Manager (branche actuelle) existante. Le gestionnaire de configuration s’adapte à des environnements volumineux et offre un contrôle extensif sur l’installation, les mises à jour et les paramètres. Il dispose également de fonctionnalités intégrées pour simplifier et accroître l’efficacité du déploiement et de la gestion de Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="395f4-p102">Contoso has an existing System Center Configuration Manager (Current Branch) infrastructure. Configuration Manager scales for large environments and provides extensive control over installation, updates, and settings. It also has built-in features to make it easier and more efficient to deploy and manage Windows 10 Enterprise.</span></span>

## <a name="planning-process"></a><span data-ttu-id="395f4-124">Processus de planification</span><span class="sxs-lookup"><span data-stu-id="395f4-124">Planning process</span></span>

<span data-ttu-id="395f4-125">Avant le déploiement, Contoso a défini les anneaux suivants :</span><span class="sxs-lookup"><span data-stu-id="395f4-125">Prior to deployment, Contoso defined the following rings:</span></span>

- <span data-ttu-id="395f4-126">Trois anneaux pour la gestion intermédiaire de la validation et du déploiement</span><span class="sxs-lookup"><span data-stu-id="395f4-126">Three rings for validation and deployment staging</span></span> 
  - <span data-ttu-id="395f4-127">Un anneau pour les versions précédentes</span><span class="sxs-lookup"><span data-stu-id="395f4-127">One for preview builds</span></span> 
  - <span data-ttu-id="395f4-128">Un anneau pour les nouvelles versions publiées</span><span class="sxs-lookup"><span data-stu-id="395f4-128">One for new release builds</span></span>
  - <span data-ttu-id="395f4-129">Un anneau pour une version précédente</span><span class="sxs-lookup"><span data-stu-id="395f4-129">One for a previous build</span></span> 
- <span data-ttu-id="395f4-130">Un anneau pour le déploiement large de Windows 10 Entreprise en fonction des données provenant des anneaux de validation</span><span class="sxs-lookup"><span data-stu-id="395f4-130">One ring for broad deployment of Windows 10 Enterprise based on data from the validation rings</span></span>

<span data-ttu-id="395f4-131">Contoso a également utilisé la solution de préparation des mises à niveau de Windows Analytics pour déterminer l’ensemble des applications installées et leur compatibilité avec Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="395f4-131">Contoso also used the Upgrade Readiness solution of Windows Analytics to determine the set of installed apps and their compatibility with Windows 10 Enterprise.</span></span>

## <a name="deployment-process"></a><span data-ttu-id="395f4-132">Processus de déploiement</span><span class="sxs-lookup"><span data-stu-id="395f4-132">Deployment process</span></span>

<span data-ttu-id="395f4-133">Pour effectuer le déploiement de mises à niveau sur place de Windows 10 Entreprise, Contoso a implémenté le processus suivant, qui inclut les recommandations concernant les meilleures pratiques de Microsoft suivantes :</span><span class="sxs-lookup"><span data-stu-id="395f4-133">To complete the in-place upgrade deployment of Windows 10 Enterprise, Contoso implemented the following process, which includes best practice recommendations from Microsoft:</span></span>

1. <span data-ttu-id="395f4-134">Activation d’un cache d’homologue pour le gestionnaire de configuration</span><span class="sxs-lookup"><span data-stu-id="395f4-134">Enabled peer cache for Configuration Manager.</span></span>
2. <span data-ttu-id="395f4-135">Création de packages Windows personnalisés basés sur des images du centre de service de gestion des licences en volume</span><span class="sxs-lookup"><span data-stu-id="395f4-135">Created customized Windows packages based on images from the Volume Licensing Service Center.</span></span>
3. <span data-ttu-id="395f4-136">Utilisation du gestionnaire de configuration pour déployer les packages Windows aux points de distribution au sein de son réseau et des versions déployées pour les trois anneaux de gestion intermédiaire de la validation et du déploiement.</span><span class="sxs-lookup"><span data-stu-id="395f4-136">Used Configuration Manager to deploy the Windows packages to distribution points across their network and deployed builds to the three validation and deployment staging rings.</span></span>
4. <span data-ttu-id="395f4-137">Exécution de l’évaluation de réussite pour les PC et les périphériques dans les trois anneaux de gestion intermédiaire de la validation et du déploiement utilisant des solutions de conformité de mise à jour et d’intégrité des périphériques de Windows Analytics.</span><span class="sxs-lookup"><span data-stu-id="395f4-137">Performed assessment of success for PCs and devices in the three validation and deployment staging rings using the Device Health and Update Compliance solutions of Windows Analytics.</span></span>
5. <span data-ttu-id="395f4-138">En fonction des informations de Windows Analytics, Contoso a déterminé la version de Windows 10 Entreprise à déployer vers l’anneau de déploiement large.</span><span class="sxs-lookup"><span data-stu-id="395f4-138">Based on the Windows Analytics information, Contoso determined the version of Windows 10 Enterprise to deploy to the broad deployment ring.</span></span>
6. <span data-ttu-id="395f4-139">Exécution des séquences de tâches du déploiement du gestionnaire de configuration pour déployer le package Windows sélectionné vers l’anneau de déploiement large.</span><span class="sxs-lookup"><span data-stu-id="395f4-139">Ran the Configuration Manager deployment task sequences to deploy the selected Windows package to the broad deployment ring.</span></span>
7. <span data-ttu-id="395f4-140">Surveillance des PC et des périphériques dans l’anneau de déploiement large en utilisant des solutions de conformité de mise à jour et d’intégrité des périphériques de Windows Analytics pour résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="395f4-140">Monitored PCs and devices in the broad deployment ring using the Device Health and Update Compliance solutions provided by Windows Analytics to address issues.</span></span>

<span data-ttu-id="395f4-141">La figure 1 décrit la mise à niveau sur place et l’architecture de déploiement de mises à jour en cours.</span><span class="sxs-lookup"><span data-stu-id="395f4-141">Figure 1 shows the in-place upgrade and ongoing updates deployment architecture.</span></span>

![](./media/contoso-win10/contoso-win10-fig1.png)
 
<span data-ttu-id="395f4-142">**Figure 1 : Infrastructure de déploiement de Windows 10 Entreprise de Contoso**</span><span class="sxs-lookup"><span data-stu-id="395f4-142">**Figure 1: Contoso’s Windows 10 Enterprise deployment infrastructure**</span></span>

<span data-ttu-id="395f4-143">Cette infrastructure se compose des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="395f4-143">This infrastructure consists of:</span></span>

- <span data-ttu-id="395f4-144">System Center Configuration Manager qui :</span><span class="sxs-lookup"><span data-stu-id="395f4-144">System Center Configuration Manager, which:</span></span>
  - <span data-ttu-id="395f4-145">obtient des images pour les packages Windows 10 Entreprise à partir du centre de gestion des licences en volume Microsoft dans The Microsoft Network ;</span><span class="sxs-lookup"><span data-stu-id="395f4-145">Obtains images for Windows 10 Enterprise packages from the Microsoft Volume Licensing Center in the Microsoft Network.</span></span>
  - <span data-ttu-id="395f4-146">est le point d’administration central pour les packages de déploiement.</span><span class="sxs-lookup"><span data-stu-id="395f4-146">Is the central administration point for deployment packages.</span></span>
- <span data-ttu-id="395f4-147">Les points de distribution régionaux généralement situés dans les succursales de Contoso.</span><span class="sxs-lookup"><span data-stu-id="395f4-147">Regional distribution points that are typically located in Contoso’s satellite offices.</span></span>
- <span data-ttu-id="395f4-148">Les périphériques et les PC Windows dans divers emplacements qui reçoivent et installent les packages de déploiement pour la mise à niveau sur place ou les mises à jour en continu basées sur l’appartenance à un anneau.</span><span class="sxs-lookup"><span data-stu-id="395f4-148">Windows PCs and devices in various locations that receive and install the deployment packages for the in-place upgrade or ongoing updates based on ring membership.</span></span>

## <a name="next-step"></a><span data-ttu-id="395f4-149">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="395f4-149">Next step</span></span>

<span data-ttu-id="395f4-150">[En savoir plus](contoso-o365pp.md) sur la façon dont Contoso exploite son infrastructure System Center Configuration Manager pour déployer et conserver la version actuelle d’Office 365 ProPlus au sein de son organisation.</span><span class="sxs-lookup"><span data-stu-id="395f4-150">[Learn](contoso-o365pp.md) how Contoso is leveraging its System Center Configuration Manager infrastructure to deploy and keep current Office 365 ProPlus across its organization.</span></span> 

## <a name="see-also"></a><span data-ttu-id="395f4-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="395f4-151">See also</span></span>

[<span data-ttu-id="395f4-152">Windows 10 Entreprise pour Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="395f4-152">Windows 10 Enterprise for Microsoft 365 Enterprise</span></span>](windows10-infrastructure.md)

[<span data-ttu-id="395f4-153">Guide de déploiement</span><span class="sxs-lookup"><span data-stu-id="395f4-153">Deployment guide</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="395f4-154">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="395f4-154">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)
