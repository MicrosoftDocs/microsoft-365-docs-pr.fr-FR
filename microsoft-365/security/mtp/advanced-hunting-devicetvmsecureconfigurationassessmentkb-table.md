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
ms.collection:
- M365-security-compliance
- m365-initiative-m365-defender
ms.topic: article
ms.openlocfilehash: f2642a46f952d3324cec4936aeb813d4ee5507d1
ms.sourcegitcommit: 5e1b8c959a081022826fb09358730096248507ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48412993"
---
# <a name="devicetvmsecureconfigurationassessmentkb"></a><span data-ttu-id="b6ae5-104">DeviceTvmSecureConfigurationAssessmentKB</span><span class="sxs-lookup"><span data-stu-id="b6ae5-104">DeviceTvmSecureConfigurationAssessmentKB</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="b6ae5-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b6ae5-105">**Applies to:**</span></span>
- <span data-ttu-id="b6ae5-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="b6ae5-106">Microsoft Threat Protection</span></span>



<span data-ttu-id="b6ae5-107">La table `DeviceTvmSecureConfigurationAssessmentKB` dans le schéma de repérage avancé contient des informations sur les différentes configurations sécurisées (par exemple, si un appareil dispose de mises à jour automatiques), vérifié par la fonction [Gestion des menaces et des vulnérabilités](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span><span class="sxs-lookup"><span data-stu-id="b6ae5-107">The `DeviceTvmSecureConfigurationAssessmentKB` table in the advanced hunting schema contains information about the various secure configurations — such as whether a device has automatic updates on — checked by [Threat & Vulnerability Management](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span></span> <span data-ttu-id="b6ae5-108">Elle inclut également des informations sur les risques, des références du secteur associées et des techniques et tactiques MITRE ATT & CK applicables.</span><span class="sxs-lookup"><span data-stu-id="b6ae5-108">It also includes risk information, related industry benchmarks, and applicable MITRE ATT&CK techniques and tactics.</span></span> <span data-ttu-id="b6ae5-109">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="b6ae5-109">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="b6ae5-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b6ae5-110">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="b6ae5-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b6ae5-111">Column name</span></span> | <span data-ttu-id="b6ae5-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="b6ae5-112">Data type</span></span> | <span data-ttu-id="b6ae5-113">Description</span><span class="sxs-lookup"><span data-stu-id="b6ae5-113">Description</span></span> |
|-------------|-----------|-------------|
| `ConfigurationId` | <span data-ttu-id="b6ae5-114">string</span><span class="sxs-lookup"><span data-stu-id="b6ae5-114">string</span></span> | <span data-ttu-id="b6ae5-115">Identificateur unique pour une configuration spécifique</span><span class="sxs-lookup"><span data-stu-id="b6ae5-115">Unique identifier for a specific configuration</span></span> |
| `ConfigurationImpact` | <span data-ttu-id="b6ae5-116">string</span><span class="sxs-lookup"><span data-stu-id="b6ae5-116">string</span></span> | <span data-ttu-id="b6ae5-117">Impact nominal de la configuration sur la note de configuration globale (1-10)</span><span class="sxs-lookup"><span data-stu-id="b6ae5-117">Rated impact of the configuration to the overall configuration score (1-10)</span></span> |
| `ConfigurationName` | <span data-ttu-id="b6ae5-118">string</span><span class="sxs-lookup"><span data-stu-id="b6ae5-118">string</span></span> | <span data-ttu-id="b6ae5-119">Nom d’affichage de la configuration</span><span class="sxs-lookup"><span data-stu-id="b6ae5-119">Display name of the configuration</span></span> |
| `ConfigurationDescription` | <span data-ttu-id="b6ae5-120">string</span><span class="sxs-lookup"><span data-stu-id="b6ae5-120">string</span></span> | <span data-ttu-id="b6ae5-121">Description de la configuration</span><span class="sxs-lookup"><span data-stu-id="b6ae5-121">Description of the configuration</span></span> |
| `RiskDescription` | <span data-ttu-id="b6ae5-122">string</span><span class="sxs-lookup"><span data-stu-id="b6ae5-122">string</span></span> | <span data-ttu-id="b6ae5-123">Description du risque associé</span><span class="sxs-lookup"><span data-stu-id="b6ae5-123">Description of the associated risk</span></span> |
| `ConfigurationCategory` | <span data-ttu-id="b6ae5-124">string</span><span class="sxs-lookup"><span data-stu-id="b6ae5-124">string</span></span> | <span data-ttu-id="b6ae5-125">Catégorie ou regroupement auquel appartient la configuration : application, système d’exploitation, réseau, comptes, contrôles de sécurité</span><span class="sxs-lookup"><span data-stu-id="b6ae5-125">Category or grouping to which the configuration belongs: Application, OS, Network, Accounts, Security controls</span></span>|
| `ConfigurationSubcategory` | <span data-ttu-id="b6ae5-126">string</span><span class="sxs-lookup"><span data-stu-id="b6ae5-126">string</span></span> |<span data-ttu-id="b6ae5-127">Sous-catégorie ou sous-groupement auquel appartient la configuration.</span><span class="sxs-lookup"><span data-stu-id="b6ae5-127">Subcategory or subgrouping to which the configuration belongs.</span></span> <span data-ttu-id="b6ae5-128">Dans de nombreux cas, cela décrit des capacités ou des fonctionnalités spécifiques.</span><span class="sxs-lookup"><span data-stu-id="b6ae5-128">In many cases, this describes specific capabilities or features.</span></span> |
| `ConfigurationBenchmarks` | <span data-ttu-id="b6ae5-129">string</span><span class="sxs-lookup"><span data-stu-id="b6ae5-129">string</span></span> | <span data-ttu-id="b6ae5-130">Liste des références du secteur recommandant une configuration identique ou similaire</span><span class="sxs-lookup"><span data-stu-id="b6ae5-130">List of industry benchmarks recommending the same or similar configuration</span></span> |
| `RelatedMitreTechniques` | <span data-ttu-id="b6ae5-131">string</span><span class="sxs-lookup"><span data-stu-id="b6ae5-131">string</span></span> | <span data-ttu-id="b6ae5-132">Liste des techniques d’infrastructure Mitre ATT&CK relatives à la configuration</span><span class="sxs-lookup"><span data-stu-id="b6ae5-132">List of Mitre ATT&CK framework techniques related to the configuration</span></span> |
| `RelatedMitreTactics ` | <span data-ttu-id="b6ae5-133">string</span><span class="sxs-lookup"><span data-stu-id="b6ae5-133">string</span></span> | <span data-ttu-id="b6ae5-134">Liste des tactiques d’infrastructure Mitre ATT&CK relatives à la configuration</span><span class="sxs-lookup"><span data-stu-id="b6ae5-134">List of Mitre ATT&CK framework tactics related to the configuration</span></span> |

## <a name="related-topics"></a><span data-ttu-id="b6ae5-135">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="b6ae5-135">Related topics</span></span>

- [<span data-ttu-id="b6ae5-136">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="b6ae5-136">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="b6ae5-137">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="b6ae5-137">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="b6ae5-138">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="b6ae5-138">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="b6ae5-139">Rechercher sur les appareils, les emails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="b6ae5-139">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="b6ae5-140">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="b6ae5-140">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="b6ae5-141">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="b6ae5-141">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="b6ae5-142">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="b6ae5-142">Overview of Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)
