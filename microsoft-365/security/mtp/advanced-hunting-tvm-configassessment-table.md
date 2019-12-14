---
title: Table DeviceTvmSecureConfigurationAssessment dans le schéma de repérage avancé
description: Découvrez les événements d’évaluation de la sécurité de Gestion des menaces et des vulnérabilités dans la table DeviceTvmSecureConfigurationAssessment du schéma de repérage avancé. Ces événements fournissent des informations sur la machine, ainsi que sur la configuration de la sécurité, l’impact et la conformité.
keywords: repérage avancé, repérage de menace, repérage de cybermenace, recherche, requête, télémétrie, schéma, référence, kusto, table, colonne, type de données, description, gestion des menaces et vulnérabilités, TVM, gestion des appareils, configuration de la sécurité, DeviceTvmSecureConfigurationAssessment
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: 2fee44c0d9c9ff30ca23ccef863e056cadee7de8
ms.sourcegitcommit: 0c9c28a87201c7470716216d99175356fb3d1a47
ms.translationtype: MT + HT Review
ms.contentlocale: fr-FR
ms.lasthandoff: 12/09/2019
ms.locfileid: "39910993"
---
# <a name="devicetvmsecureconfigurationassessment"></a><span data-ttu-id="e1412-105">DeviceTvmSecureConfigurationAssessment</span><span class="sxs-lookup"><span data-stu-id="e1412-105">DeviceTvmSecureConfigurationAssessment</span></span>

<span data-ttu-id="e1412-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e1412-106">**Applies to:**</span></span>
- <span data-ttu-id="e1412-107">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="e1412-107">Microsoft Threat Protection</span></span>

[!include[Prerelease information](prerelease.md)]

<span data-ttu-id="e1412-108">Chaque ligne du tableau `DeviceTvmSecureConfigurationAssessment` contient un événement d’évaluation pour une configuration de sécurité spécifique de [Gestion des menaces et des vulnérabilités](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span><span class="sxs-lookup"><span data-stu-id="e1412-108">Each row in the `DeviceTvmSecureConfigurationAssessment` table contains an assessment event for a specific security configuration from [Threat & Vulnerability Management](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span></span> <span data-ttu-id="e1412-109">Utilisez cette référence pour vérifier les derniers résultats de l’évaluation et déterminer si les appareils sont conformes.</span><span class="sxs-lookup"><span data-stu-id="e1412-109">Use this reference to check the latest assessment results and determine whether devices are compliant.</span></span>

<span data-ttu-id="e1412-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e1412-110">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="e1412-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="e1412-111">Column name</span></span> | <span data-ttu-id="e1412-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="e1412-112">Data type</span></span> | <span data-ttu-id="e1412-113">Description</span><span class="sxs-lookup"><span data-stu-id="e1412-113">Description</span></span> |
|-------------|-----------|-------------|
| `MachineId` | <span data-ttu-id="e1412-114">string</span><span class="sxs-lookup"><span data-stu-id="e1412-114">string</span></span> | <span data-ttu-id="e1412-115">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="e1412-115">Unique identifier for the machine in the service</span></span> |
| `ComputerName` | <span data-ttu-id="e1412-116">string</span><span class="sxs-lookup"><span data-stu-id="e1412-116">string</span></span> | <span data-ttu-id="e1412-117">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="e1412-117">Fully qualified domain name (FQDN) of the pool</span></span> |
| `OSPlatform` | <span data-ttu-id="e1412-118">string</span><span class="sxs-lookup"><span data-stu-id="e1412-118">string</span></span> | <span data-ttu-id="e1412-119">Plateforme du système d’exploitation client s’exécutant sur la machine.</span><span class="sxs-lookup"><span data-stu-id="e1412-119">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="e1412-120">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e1412-120">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span>|
| `Timestamp` | <span data-ttu-id="e1412-121">DateHeure</span><span class="sxs-lookup"><span data-stu-id="e1412-121">dateTime</span></span> | <span data-ttu-id="e1412-122">Date et heure de génération de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="e1412-122">Date and time when the record was generated</span></span> |
| `ConfigurationId` | <span data-ttu-id="e1412-123">string</span><span class="sxs-lookup"><span data-stu-id="e1412-123">string</span></span> | <span data-ttu-id="e1412-124">Identificateur unique pour une configuration spécifique</span><span class="sxs-lookup"><span data-stu-id="e1412-124">Unique identifier for a specific configuration</span></span> |
| `ConfigurationCategory` | <span data-ttu-id="e1412-125">string</span><span class="sxs-lookup"><span data-stu-id="e1412-125">string</span></span> | <span data-ttu-id="e1412-126">Catégorie ou regroupement auquel appartient la configuration : application, système d’exploitation, réseau, comptes, contrôles de sécurité</span><span class="sxs-lookup"><span data-stu-id="e1412-126">Category or grouping to which the configuration belongs: Application, OS, Network, Accounts, Security controls</span></span> |
| `ConfigurationSubcategory` | <span data-ttu-id="e1412-127">string</span><span class="sxs-lookup"><span data-stu-id="e1412-127">string</span></span> | <span data-ttu-id="e1412-128">Sous-catégorie ou sous-groupement auquel appartient la configuration.</span><span class="sxs-lookup"><span data-stu-id="e1412-128">Subcategory or subgrouping to which the configuration belongs.</span></span> <span data-ttu-id="e1412-129">Dans de nombreux cas, cela décrit des capacités ou des fonctionnalités spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e1412-129">In many cases, this describes specific capabilities or features.</span></span> |
| `ConfigurationImpact` | <span data-ttu-id="e1412-130">string</span><span class="sxs-lookup"><span data-stu-id="e1412-130">string</span></span> | <span data-ttu-id="e1412-131">Impact nominal de la configuration sur la note de configuration globale (1-10)</span><span class="sxs-lookup"><span data-stu-id="e1412-131">Rated impact of the configuration to the overall configuration score (1-10)</span></span> |
| `IsCompliant` | <span data-ttu-id="e1412-132">booléen</span><span class="sxs-lookup"><span data-stu-id="e1412-132">boolean</span></span> | <span data-ttu-id="e1412-133">Indique si la configuration ou la stratégie est correctement configurée.</span><span class="sxs-lookup"><span data-stu-id="e1412-133">Indicates whether the configuration or policy is properly configured</span></span> |

## <a name="related-topics"></a><span data-ttu-id="e1412-134">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="e1412-134">Related topics</span></span>

- [<span data-ttu-id="e1412-135">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="e1412-135">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="e1412-136">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="e1412-136">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="e1412-137">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="e1412-137">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="e1412-138">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="e1412-138">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="e1412-139">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="e1412-139">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="e1412-140">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="e1412-140">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="e1412-141">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="e1412-141">Overview of Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)
