---
title: Table DeviceTvmSecureConfigurationAssessmentKB dans le schéma de repérage avancé
description: Découvrez les différentes configurations sécurisées évaluées par la fonction Gestion des menaces et des vulnérabilités dans la table DeviceTvmSecureConfigurationAssessmentKB du schéma de repérage avancé.
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, threat & vulnerability management, TVM, device management, security configuration, MITRE ATT&CK framework, knowledge base, KB, DeviceTvmSecureConfigurationAssessmentKB
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: e664f0da29e0403b415792c839fd740006791cf0
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51063457"
---
# <a name="devicetvmsecureconfigurationassessmentkb"></a><span data-ttu-id="477eb-104">DeviceTvmSecureConfigurationAssessmentKB</span><span class="sxs-lookup"><span data-stu-id="477eb-104">DeviceTvmSecureConfigurationAssessmentKB</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="477eb-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="477eb-105">**Applies to:**</span></span>
- <span data-ttu-id="477eb-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="477eb-106">Microsoft 365 Defender</span></span>



<span data-ttu-id="477eb-107">La table `DeviceTvmSecureConfigurationAssessmentKB` dans le schéma de repérage avancé contient des informations sur les différentes configurations sécurisées (par exemple, si un appareil dispose de mises à jour automatiques), vérifié par la fonction [Gestion des menaces et des vulnérabilités](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span><span class="sxs-lookup"><span data-stu-id="477eb-107">The `DeviceTvmSecureConfigurationAssessmentKB` table in the advanced hunting schema contains information about the various secure configurations — such as whether a device has automatic updates on — checked by [Threat & Vulnerability Management](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span></span> <span data-ttu-id="477eb-108">Elle inclut également des informations sur les risques, des références du secteur associées et des techniques et tactiques MITRE ATT & CK applicables.</span><span class="sxs-lookup"><span data-stu-id="477eb-108">It also includes risk information, related industry benchmarks, and applicable MITRE ATT&CK techniques and tactics.</span></span> <span data-ttu-id="477eb-109">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="477eb-109">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="477eb-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="477eb-110">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="477eb-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="477eb-111">Column name</span></span> | <span data-ttu-id="477eb-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="477eb-112">Data type</span></span> | <span data-ttu-id="477eb-113">Description</span><span class="sxs-lookup"><span data-stu-id="477eb-113">Description</span></span> |
|-------------|-----------|-------------|
| `ConfigurationId` | <span data-ttu-id="477eb-114">string</span><span class="sxs-lookup"><span data-stu-id="477eb-114">string</span></span> | <span data-ttu-id="477eb-115">Identificateur unique pour une configuration spécifique</span><span class="sxs-lookup"><span data-stu-id="477eb-115">Unique identifier for a specific configuration</span></span> |
| `ConfigurationImpact` | <span data-ttu-id="477eb-116">string</span><span class="sxs-lookup"><span data-stu-id="477eb-116">string</span></span> | <span data-ttu-id="477eb-117">Impact nominal de la configuration sur la note de configuration globale (1-10)</span><span class="sxs-lookup"><span data-stu-id="477eb-117">Rated impact of the configuration to the overall configuration score (1-10)</span></span> |
| `ConfigurationName` | <span data-ttu-id="477eb-118">string</span><span class="sxs-lookup"><span data-stu-id="477eb-118">string</span></span> | <span data-ttu-id="477eb-119">Nom d’affichage de la configuration</span><span class="sxs-lookup"><span data-stu-id="477eb-119">Display name of the configuration</span></span> |
| `ConfigurationDescription` | <span data-ttu-id="477eb-120">string</span><span class="sxs-lookup"><span data-stu-id="477eb-120">string</span></span> | <span data-ttu-id="477eb-121">Description de la configuration</span><span class="sxs-lookup"><span data-stu-id="477eb-121">Description of the configuration</span></span> |
| `RiskDescription` | <span data-ttu-id="477eb-122">string</span><span class="sxs-lookup"><span data-stu-id="477eb-122">string</span></span> | <span data-ttu-id="477eb-123">Description du risque associé</span><span class="sxs-lookup"><span data-stu-id="477eb-123">Description of the associated risk</span></span> |
| `ConfigurationCategory` | <span data-ttu-id="477eb-124">string</span><span class="sxs-lookup"><span data-stu-id="477eb-124">string</span></span> | <span data-ttu-id="477eb-125">Catégorie ou regroupement auquel appartient la configuration : application, système d’exploitation, réseau, comptes, contrôles de sécurité</span><span class="sxs-lookup"><span data-stu-id="477eb-125">Category or grouping to which the configuration belongs: Application, OS, Network, Accounts, Security controls</span></span>|
| `ConfigurationSubcategory` | <span data-ttu-id="477eb-126">string</span><span class="sxs-lookup"><span data-stu-id="477eb-126">string</span></span> |<span data-ttu-id="477eb-127">Sous-catégorie ou sous-groupement auquel appartient la configuration.</span><span class="sxs-lookup"><span data-stu-id="477eb-127">Subcategory or subgrouping to which the configuration belongs.</span></span> <span data-ttu-id="477eb-128">Dans de nombreux cas, cela décrit des capacités ou des fonctionnalités spécifiques.</span><span class="sxs-lookup"><span data-stu-id="477eb-128">In many cases, this describes specific capabilities or features.</span></span> |
| `ConfigurationBenchmarks` | <span data-ttu-id="477eb-129">string</span><span class="sxs-lookup"><span data-stu-id="477eb-129">string</span></span> | <span data-ttu-id="477eb-130">Liste des références du secteur recommandant une configuration identique ou similaire</span><span class="sxs-lookup"><span data-stu-id="477eb-130">List of industry benchmarks recommending the same or similar configuration</span></span> |
| `Tags` | <span data-ttu-id="477eb-131">string</span><span class="sxs-lookup"><span data-stu-id="477eb-131">string</span></span> | <span data-ttu-id="477eb-132">Étiquettes représentant différents attributs utilisés pour identifier ou classer une configuration de sécurité</span><span class="sxs-lookup"><span data-stu-id="477eb-132">Labels representing various attributes used to identify or categorize a security configuration</span></span> |
| `RemediationOptions` | <span data-ttu-id="477eb-133">string</span><span class="sxs-lookup"><span data-stu-id="477eb-133">string</span></span> | <span data-ttu-id="477eb-134">Actions recommandées pour réduire ou résoudre les risques associés</span><span class="sxs-lookup"><span data-stu-id="477eb-134">Recommended actions to reduce or address any associated risks</span></span> |

## <a name="related-topics"></a><span data-ttu-id="477eb-135">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="477eb-135">Related topics</span></span>

- [<span data-ttu-id="477eb-136">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="477eb-136">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="477eb-137">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="477eb-137">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="477eb-138">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="477eb-138">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="477eb-139">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="477eb-139">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="477eb-140">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="477eb-140">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="477eb-141">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="477eb-141">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="477eb-142">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="477eb-142">Overview of Threat & Vulnerability Management</span></span>](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)