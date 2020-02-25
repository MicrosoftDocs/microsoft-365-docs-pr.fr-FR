---
title: Table DeviceTvmSecureConfigurationAssessmentKB dans le schéma de repérage avancé
description: Découvrez les différentes configurations sécurisées évaluées par la fonction Gestion des menaces et des vulnérabilités dans la table DeviceTvmSecureConfigurationAssessmentKB du schéma de repérage avancé.
keywords: chasse aux menaces, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, table, colonne, type de données, description, menace & gestion des vulnérabilités, TVM, gestion des appareils, configuration de la sécurité, MITRE ATT&CK infrastructure, base de connaissances,
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: a265bb84b0ad59ee56cb0f0670951bab1bcd344a
ms.sourcegitcommit: 74bf600424d0cb7b9d16b4f391aeda7875058be1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42235143"
---
# <a name="devicetvmsecureconfigurationassessmentkb"></a><span data-ttu-id="1399f-104">DeviceTvmSecureConfigurationAssessmentKB</span><span class="sxs-lookup"><span data-stu-id="1399f-104">DeviceTvmSecureConfigurationAssessmentKB</span></span>

<span data-ttu-id="1399f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1399f-105">**Applies to:**</span></span>
- <span data-ttu-id="1399f-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="1399f-106">Microsoft Threat Protection</span></span>



<span data-ttu-id="1399f-107">La table `DeviceTvmSecureConfigurationAssessmentKB` dans le schéma de repérage avancé contient des informations sur les différentes configurations sécurisées (par exemple, si un appareil dispose de mises à jour automatiques), vérifié par la fonction [Gestion des menaces et des vulnérabilités](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span><span class="sxs-lookup"><span data-stu-id="1399f-107">The `DeviceTvmSecureConfigurationAssessmentKB` table in the advanced hunting schema contains information about the various secure configurations — such as whether a device has automatic updates on — checked by [Threat & Vulnerability Management](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span></span> <span data-ttu-id="1399f-108">Elle inclut également des informations sur les risques, des références du secteur associées et des techniques et tactiques MITRE ATT & CK applicables.</span><span class="sxs-lookup"><span data-stu-id="1399f-108">It also includes risk information, related industry benchmarks, and applicable MITRE ATT&CK techniques and tactics.</span></span> <span data-ttu-id="1399f-109">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="1399f-109">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="1399f-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1399f-110">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="1399f-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="1399f-111">Column name</span></span> | <span data-ttu-id="1399f-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="1399f-112">Data type</span></span> | <span data-ttu-id="1399f-113">Description</span><span class="sxs-lookup"><span data-stu-id="1399f-113">Description</span></span> |
|-------------|-----------|-------------|
| `ConfigurationId` | <span data-ttu-id="1399f-114">string</span><span class="sxs-lookup"><span data-stu-id="1399f-114">string</span></span> | <span data-ttu-id="1399f-115">Identificateur unique pour une configuration spécifique</span><span class="sxs-lookup"><span data-stu-id="1399f-115">Unique identifier for a specific configuration</span></span> |
| `ConfigurationImpact` | <span data-ttu-id="1399f-116">string</span><span class="sxs-lookup"><span data-stu-id="1399f-116">string</span></span> | <span data-ttu-id="1399f-117">Impact nominal de la configuration sur la note de configuration globale (1-10)</span><span class="sxs-lookup"><span data-stu-id="1399f-117">Rated impact of the configuration to the overall configuration score (1-10)</span></span> |
| `ConfigurationName` | <span data-ttu-id="1399f-118">string</span><span class="sxs-lookup"><span data-stu-id="1399f-118">string</span></span> | <span data-ttu-id="1399f-119">Nom d’affichage de la configuration</span><span class="sxs-lookup"><span data-stu-id="1399f-119">Display name of the configuration</span></span> |
| `ConfigurationDescription` | <span data-ttu-id="1399f-120">string</span><span class="sxs-lookup"><span data-stu-id="1399f-120">string</span></span> | <span data-ttu-id="1399f-121">Description de la configuration</span><span class="sxs-lookup"><span data-stu-id="1399f-121">Description of the configuration</span></span> |
| `RiskDescription` | <span data-ttu-id="1399f-122">string</span><span class="sxs-lookup"><span data-stu-id="1399f-122">string</span></span> | <span data-ttu-id="1399f-123">Description du risque associé</span><span class="sxs-lookup"><span data-stu-id="1399f-123">Description of the associated risk</span></span> |
| `ConfigurationCategory` | <span data-ttu-id="1399f-124">string</span><span class="sxs-lookup"><span data-stu-id="1399f-124">string</span></span> | <span data-ttu-id="1399f-125">Catégorie ou regroupement auquel appartient la configuration : application, système d’exploitation, réseau, comptes, contrôles de sécurité</span><span class="sxs-lookup"><span data-stu-id="1399f-125">Category or grouping to which the configuration belongs: Application, OS, Network, Accounts, Security controls</span></span>|
| `ConfigurationSubcategory` | <span data-ttu-id="1399f-126">string</span><span class="sxs-lookup"><span data-stu-id="1399f-126">string</span></span> |<span data-ttu-id="1399f-127">Sous-catégorie ou sous-groupement auquel appartient la configuration.</span><span class="sxs-lookup"><span data-stu-id="1399f-127">Subcategory or subgrouping to which the configuration belongs.</span></span> <span data-ttu-id="1399f-128">Dans de nombreux cas, cela décrit des capacités ou des fonctionnalités spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1399f-128">In many cases, this describes specific capabilities or features.</span></span> |
| `ConfigurationBenchmarks` | <span data-ttu-id="1399f-129">string</span><span class="sxs-lookup"><span data-stu-id="1399f-129">string</span></span> | <span data-ttu-id="1399f-130">Liste des références du secteur recommandant une configuration identique ou similaire</span><span class="sxs-lookup"><span data-stu-id="1399f-130">List of industry benchmarks recommending the same or similar configuration</span></span> |
| `RelatedMitreTechniques` | <span data-ttu-id="1399f-131">string</span><span class="sxs-lookup"><span data-stu-id="1399f-131">string</span></span> | <span data-ttu-id="1399f-132">Liste des techniques d’infrastructure Mitre ATT&CK relatives à la configuration</span><span class="sxs-lookup"><span data-stu-id="1399f-132">List of Mitre ATT&CK framework techniques related to the configuration</span></span> |
| `RelatedMitreTactics ` | <span data-ttu-id="1399f-133">string</span><span class="sxs-lookup"><span data-stu-id="1399f-133">string</span></span> | <span data-ttu-id="1399f-134">Liste des tactiques d’infrastructure Mitre ATT&CK relatives à la configuration</span><span class="sxs-lookup"><span data-stu-id="1399f-134">List of Mitre ATT&CK framework tactics related to the configuration</span></span> |

## <a name="related-topics"></a><span data-ttu-id="1399f-135">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="1399f-135">Related topics</span></span>

- [<span data-ttu-id="1399f-136">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="1399f-136">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="1399f-137">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="1399f-137">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="1399f-138">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="1399f-138">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="1399f-139">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="1399f-139">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="1399f-140">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="1399f-140">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="1399f-141">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="1399f-141">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="1399f-142">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="1399f-142">Overview of Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)
