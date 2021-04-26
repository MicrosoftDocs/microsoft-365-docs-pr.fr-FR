---
title: Table DeviceTvmSecureConfigurationAssessmentKB dans le schéma de repérage avancé
description: Découvrez les différentes configurations sécurisées évaluées par la fonction Gestion des menaces et des vulnérabilités dans la table DeviceTvmSecureConfigurationAssessmentKB du schéma de repérage avancé.
keywords: advanced hunting, threat hunting, cyber threat hunting, Microsoft 365 Defender, microsoft 365, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, threat & vulnerability management, TVM, device management, security configuration, MITRE ATT&CK framework, knowledge base, KB, DeviceTvmSecureConfigurationAssesmentKB
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: maccruz
author: schmurky
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: 1dfa710b86afdcfd8a5643555564a0f34c7b4702
ms.sourcegitcommit: 72795ec56a7c4db863dcaaff5e9f7c41c653fda8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "52024240"
---
# <a name="devicetvmsecureconfigurationassessmentkb"></a><span data-ttu-id="c9243-104">DeviceTvmSecureConfigurationAssessmentKB</span><span class="sxs-lookup"><span data-stu-id="c9243-104">DeviceTvmSecureConfigurationAssessmentKB</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="c9243-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c9243-105">**Applies to:**</span></span>
- <span data-ttu-id="c9243-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c9243-106">Microsoft 365 Defender</span></span>
- <span data-ttu-id="c9243-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c9243-107">Microsoft Defender for Endpoint</span></span>



<span data-ttu-id="c9243-108">La table `DeviceTvmSecureConfigurationAssessmentKB` dans le schéma de repérage avancé contient des informations sur les différentes configurations sécurisées (par exemple, si un appareil dispose de mises à jour automatiques), vérifié par la fonction [Gestion des menaces et des vulnérabilités](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span><span class="sxs-lookup"><span data-stu-id="c9243-108">The `DeviceTvmSecureConfigurationAssessmentKB` table in the advanced hunting schema contains information about the various secure configurations — such as whether a device has automatic updates on — checked by [Threat & Vulnerability Management](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span></span> <span data-ttu-id="c9243-109">Elle inclut également des informations sur les risques, des références du secteur associées et des techniques et tactiques MITRE ATT & CK applicables.</span><span class="sxs-lookup"><span data-stu-id="c9243-109">It also includes risk information, related industry benchmarks, and applicable MITRE ATT&CK techniques and tactics.</span></span> <span data-ttu-id="c9243-110">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="c9243-110">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="c9243-111">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c9243-111">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="c9243-112">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c9243-112">Column name</span></span> | <span data-ttu-id="c9243-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="c9243-113">Data type</span></span> | <span data-ttu-id="c9243-114">Description</span><span class="sxs-lookup"><span data-stu-id="c9243-114">Description</span></span> |
|-------------|-----------|-------------|
| `ConfigurationId` | <span data-ttu-id="c9243-115">string</span><span class="sxs-lookup"><span data-stu-id="c9243-115">string</span></span> | <span data-ttu-id="c9243-116">Identificateur unique pour une configuration spécifique</span><span class="sxs-lookup"><span data-stu-id="c9243-116">Unique identifier for a specific configuration</span></span> |
| `ConfigurationImpact` | <span data-ttu-id="c9243-117">string</span><span class="sxs-lookup"><span data-stu-id="c9243-117">string</span></span> | <span data-ttu-id="c9243-118">Impact nominal de la configuration sur la note de configuration globale (1-10)</span><span class="sxs-lookup"><span data-stu-id="c9243-118">Rated impact of the configuration to the overall configuration score (1-10)</span></span> |
| `ConfigurationName` | <span data-ttu-id="c9243-119">string</span><span class="sxs-lookup"><span data-stu-id="c9243-119">string</span></span> | <span data-ttu-id="c9243-120">Nom d’affichage de la configuration</span><span class="sxs-lookup"><span data-stu-id="c9243-120">Display name of the configuration</span></span> |
| `ConfigurationDescription` | <span data-ttu-id="c9243-121">string</span><span class="sxs-lookup"><span data-stu-id="c9243-121">string</span></span> | <span data-ttu-id="c9243-122">Description de la configuration</span><span class="sxs-lookup"><span data-stu-id="c9243-122">Description of the configuration</span></span> |
| `RiskDescription` | <span data-ttu-id="c9243-123">string</span><span class="sxs-lookup"><span data-stu-id="c9243-123">string</span></span> | <span data-ttu-id="c9243-124">Description du risque associé</span><span class="sxs-lookup"><span data-stu-id="c9243-124">Description of the associated risk</span></span> |
| `ConfigurationCategory` | <span data-ttu-id="c9243-125">string</span><span class="sxs-lookup"><span data-stu-id="c9243-125">string</span></span> | <span data-ttu-id="c9243-126">Catégorie ou regroupement auquel appartient la configuration : application, système d’exploitation, réseau, comptes, contrôles de sécurité</span><span class="sxs-lookup"><span data-stu-id="c9243-126">Category or grouping to which the configuration belongs: Application, OS, Network, Accounts, Security controls</span></span>|
| `ConfigurationSubcategory` | <span data-ttu-id="c9243-127">string</span><span class="sxs-lookup"><span data-stu-id="c9243-127">string</span></span> |<span data-ttu-id="c9243-128">Sous-catégorie ou sous-groupement auquel appartient la configuration.</span><span class="sxs-lookup"><span data-stu-id="c9243-128">Subcategory or subgrouping to which the configuration belongs.</span></span> <span data-ttu-id="c9243-129">Dans de nombreux cas, cela décrit des capacités ou des fonctionnalités spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c9243-129">In many cases, this describes specific capabilities or features.</span></span> |
| `ConfigurationBenchmarks` | <span data-ttu-id="c9243-130">string</span><span class="sxs-lookup"><span data-stu-id="c9243-130">string</span></span> | <span data-ttu-id="c9243-131">Liste des références du secteur recommandant une configuration identique ou similaire</span><span class="sxs-lookup"><span data-stu-id="c9243-131">List of industry benchmarks recommending the same or similar configuration</span></span> |
| `Tags` | <span data-ttu-id="c9243-132">string</span><span class="sxs-lookup"><span data-stu-id="c9243-132">string</span></span> | <span data-ttu-id="c9243-133">Étiquettes représentant différents attributs utilisés pour identifier ou classer une configuration de sécurité</span><span class="sxs-lookup"><span data-stu-id="c9243-133">Labels representing various attributes used to identify or categorize a security configuration</span></span> |
| `RemediationOptions` | <span data-ttu-id="c9243-134">string</span><span class="sxs-lookup"><span data-stu-id="c9243-134">string</span></span> | <span data-ttu-id="c9243-135">Actions recommandées pour réduire ou résoudre les risques associés</span><span class="sxs-lookup"><span data-stu-id="c9243-135">Recommended actions to reduce or address any associated risks</span></span> |

## <a name="related-topics"></a><span data-ttu-id="c9243-136">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="c9243-136">Related topics</span></span>

- [<span data-ttu-id="c9243-137">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="c9243-137">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="c9243-138">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="c9243-138">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="c9243-139">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="c9243-139">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="c9243-140">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="c9243-140">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="c9243-141">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="c9243-141">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="c9243-142">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="c9243-142">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="c9243-143">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="c9243-143">Overview of Threat & Vulnerability Management</span></span>](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)