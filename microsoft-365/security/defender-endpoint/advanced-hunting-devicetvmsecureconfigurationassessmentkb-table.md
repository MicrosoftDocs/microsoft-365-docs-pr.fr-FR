---
title: Table DeviceTvmSecureConfigurationAssessmentKB dans le schéma de repérage avancé
description: Découvrez les différentes configurations sécurisées évaluées par threat & Vulnerability Management dans la table DeviceTvmSecureConfigurationAssessmentKB du schéma de recherche avancée.
keywords: advanced hunting, threat hunting, cyber threat hunting, mdatp, microsoft defender atp, wdatp search, query, telemetry, schema reference, kusto, table, column, data type, description, threat & vulnerability management, TVM, device management, security configuration, MITRE ATT&CK framework, knowledge base, KB, DeviceTvmSecureConfigurationAssessmentKB
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dolmont
author: DulceMontemayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 3ba0d90fae872eff209b41b7ba62baeccfe62808
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51067006"
---
# <a name="devicetvmsecureconfigurationassessmentkb"></a><span data-ttu-id="93527-104">DeviceTvmSecureConfigurationAssessmentKB</span><span class="sxs-lookup"><span data-stu-id="93527-104">DeviceTvmSecureConfigurationAssessmentKB</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="93527-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="93527-105">**Applies to:**</span></span>
- [<span data-ttu-id="93527-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="93527-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)


><span data-ttu-id="93527-107">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="93527-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="93527-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="93527-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/WindowsForBusiness/windows-atp?ocid=docs-wdatp-advancedhuntingref-abovefoldlink)

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="93527-109">La table `DeviceTvmSecureConfigurationAssessmentKB` dans le schéma de repérage avancé contient des informations sur les différentes configurations sécurisées (par exemple, si un appareil dispose de mises à jour automatiques), vérifié par la fonction [Gestion des menaces et des vulnérabilités](next-gen-threat-and-vuln-mgt.md).</span><span class="sxs-lookup"><span data-stu-id="93527-109">The `DeviceTvmSecureConfigurationAssessmentKB` table in the advanced hunting schema contains information about the various secure configurations — such as whether a device has automatic updates on — checked by [Threat & Vulnerability Management](next-gen-threat-and-vuln-mgt.md).</span></span> <span data-ttu-id="93527-110">Elle inclut également des informations sur les risques, des références du secteur associées et des techniques et tactiques MITRE ATT & CK applicables.</span><span class="sxs-lookup"><span data-stu-id="93527-110">It also includes risk information, related industry benchmarks, and applicable MITRE ATT&CK techniques and tactics.</span></span> <span data-ttu-id="93527-111">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="93527-111">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="93527-112">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference).</span><span class="sxs-lookup"><span data-stu-id="93527-112">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference).</span></span>

| <span data-ttu-id="93527-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93527-113">Column name</span></span> | <span data-ttu-id="93527-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="93527-114">Data type</span></span> | <span data-ttu-id="93527-115">Description</span><span class="sxs-lookup"><span data-stu-id="93527-115">Description</span></span> |
|-------------|-----------|-------------|
| `ConfigurationId` | <span data-ttu-id="93527-116">string</span><span class="sxs-lookup"><span data-stu-id="93527-116">string</span></span> | <span data-ttu-id="93527-117">Identificateur unique pour une configuration spécifique</span><span class="sxs-lookup"><span data-stu-id="93527-117">Unique identifier for a specific configuration</span></span> |
| `ConfigurationImpact` | <span data-ttu-id="93527-118">string</span><span class="sxs-lookup"><span data-stu-id="93527-118">string</span></span> | <span data-ttu-id="93527-119">Impact nominal de la configuration sur la note de configuration globale (1-10)</span><span class="sxs-lookup"><span data-stu-id="93527-119">Rated impact of the configuration to the overall configuration score (1-10)</span></span> |
| `ConfigurationName` | <span data-ttu-id="93527-120">string</span><span class="sxs-lookup"><span data-stu-id="93527-120">string</span></span> | <span data-ttu-id="93527-121">Nom d’affichage de la configuration</span><span class="sxs-lookup"><span data-stu-id="93527-121">Display name of the configuration</span></span> |
| `ConfigurationDescription` | <span data-ttu-id="93527-122">string</span><span class="sxs-lookup"><span data-stu-id="93527-122">string</span></span> | <span data-ttu-id="93527-123">Description de la configuration</span><span class="sxs-lookup"><span data-stu-id="93527-123">Description of the configuration</span></span> |
| `RiskDescription` | <span data-ttu-id="93527-124">string</span><span class="sxs-lookup"><span data-stu-id="93527-124">string</span></span> | <span data-ttu-id="93527-125">Description du risque associé</span><span class="sxs-lookup"><span data-stu-id="93527-125">Description of the associated risk</span></span> |
| `ConfigurationCategory` | <span data-ttu-id="93527-126">string</span><span class="sxs-lookup"><span data-stu-id="93527-126">string</span></span> | <span data-ttu-id="93527-127">Catégorie ou regroupement auquel appartient la configuration : application, système d’exploitation, réseau, comptes, contrôles de sécurité</span><span class="sxs-lookup"><span data-stu-id="93527-127">Category or grouping to which the configuration belongs: Application, OS, Network, Accounts, Security controls</span></span>|
| `ConfigurationSubcategory` | <span data-ttu-id="93527-128">string</span><span class="sxs-lookup"><span data-stu-id="93527-128">string</span></span> |<span data-ttu-id="93527-129">Sous-catégorie ou sous-groupement auquel appartient la configuration.</span><span class="sxs-lookup"><span data-stu-id="93527-129">Subcategory or subgrouping to which the configuration belongs.</span></span> <span data-ttu-id="93527-130">Dans de nombreux cas, cela décrit des capacités ou des fonctionnalités spécifiques.</span><span class="sxs-lookup"><span data-stu-id="93527-130">In many cases, this describes specific capabilities or features.</span></span> |
| `ConfigurationBenchmarks` | <span data-ttu-id="93527-131">string</span><span class="sxs-lookup"><span data-stu-id="93527-131">string</span></span> | <span data-ttu-id="93527-132">Liste des références du secteur recommandant une configuration identique ou similaire</span><span class="sxs-lookup"><span data-stu-id="93527-132">List of industry benchmarks recommending the same or similar configuration</span></span> |
| `RelatedMitreTechniques` | <span data-ttu-id="93527-133">string</span><span class="sxs-lookup"><span data-stu-id="93527-133">string</span></span> | <span data-ttu-id="93527-134">Liste des techniques d’infrastructure Mitre ATT&CK relatives à la configuration</span><span class="sxs-lookup"><span data-stu-id="93527-134">List of Mitre ATT&CK framework techniques related to the configuration</span></span> |
| `RelatedMitreTactics ` | <span data-ttu-id="93527-135">string</span><span class="sxs-lookup"><span data-stu-id="93527-135">string</span></span> | <span data-ttu-id="93527-136">Liste des tactiques d’infrastructure Mitre ATT&CK relatives à la configuration</span><span class="sxs-lookup"><span data-stu-id="93527-136">List of Mitre ATT&CK framework tactics related to the configuration</span></span> |

## <a name="related-topics"></a><span data-ttu-id="93527-137">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="93527-137">Related topics</span></span>

- [<span data-ttu-id="93527-138">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="93527-138">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="93527-139">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="93527-139">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="93527-140">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="93527-140">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
- [<span data-ttu-id="93527-141">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="93527-141">Overview of Threat & Vulnerability Management</span></span>](next-gen-threat-and-vuln-mgt.md)
