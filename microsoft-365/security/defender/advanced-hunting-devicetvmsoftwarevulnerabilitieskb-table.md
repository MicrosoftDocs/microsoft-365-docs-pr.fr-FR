---
title: Table DeviceTvmSoftwareVulnerabilitiesKB dans le schéma de repérage avancé
description: Découvrez les vulnérabilités logicielles suivies par la fonction Gestion des menaces et des vulnérabilités dans la table DeviceTvmSoftwareVulnerabilitiesKB du schéma de repérage avancé.
keywords: advanced hunting, threat hunting, cyber threat hunting, Microsoft 365 Defender, microsoft 365, m365, search, query, telemetry, schema, reference, kusto, table, column, data type, description, threat & vulnerability management, TVM, device management, software, inventory, vulnerabilities, CVE ID, CVSS, DeviceTvmSoftwareVulnerabilitiesKBB
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
ms.openlocfilehash: afcd6bcd81e1a8635be9ced766c533ea4195334f
ms.sourcegitcommit: 72795ec56a7c4db863dcaaff5e9f7c41c653fda8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "52023796"
---
# <a name="devicetvmsoftwarevulnerabilitieskb"></a><span data-ttu-id="cd680-104">DeviceTvmSoftwareVulnerabilitiesKB</span><span class="sxs-lookup"><span data-stu-id="cd680-104">DeviceTvmSoftwareVulnerabilitiesKB</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="cd680-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="cd680-105">**Applies to:**</span></span>
- <span data-ttu-id="cd680-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="cd680-106">Microsoft 365 Defender</span></span>
- <span data-ttu-id="cd680-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="cd680-107">Microsoft Defender for Endpoint</span></span>



<span data-ttu-id="cd680-108">La table `DeviceTvmSoftwareVulnerabilitiesKB` du schéma de repérage avancé contient la liste des vulnérabilités pour lesquelles la fonction [Gestion des menaces et des vulnérabilités](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt) évalue les appareils.</span><span class="sxs-lookup"><span data-stu-id="cd680-108">The `DeviceTvmSoftwareVulnerabilitiesKB` table in the advanced hunting schema contains the list of vulnerabilities [Threat & Vulnerability Management](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt) assesses devices for.</span></span> <span data-ttu-id="cd680-109">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="cd680-109">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="cd680-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="cd680-110">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="cd680-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="cd680-111">Column name</span></span> | <span data-ttu-id="cd680-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="cd680-112">Data type</span></span> | <span data-ttu-id="cd680-113">Description</span><span class="sxs-lookup"><span data-stu-id="cd680-113">Description</span></span> |
|-------------|-----------|-------------|
| `CveId` | <span data-ttu-id="cd680-114">string</span><span class="sxs-lookup"><span data-stu-id="cd680-114">string</span></span> | <span data-ttu-id="cd680-115">Identificateur unique affecté à la vulnérabilité de sécurité dans le système Common Vulnerabilities and Exposures (CVE)</span><span class="sxs-lookup"><span data-stu-id="cd680-115">Unique identifier assigned to the security vulnerability under the Common Vulnerabilities and Exposures (CVE) system</span></span> |
| `CvssScore` | <span data-ttu-id="cd680-116">string</span><span class="sxs-lookup"><span data-stu-id="cd680-116">string</span></span> | <span data-ttu-id="cd680-117">Score de gravité attribué à la vulnérabilité de sécurité dans le cadre du système Common Vulnerability Scoring System (CVSS)</span><span class="sxs-lookup"><span data-stu-id="cd680-117">Severity score assigned to the security vulnerability under th Common Vulnerability Scoring System (CVSS)</span></span> |
| `IsExploitAvailable` | <span data-ttu-id="cd680-118">booléen</span><span class="sxs-lookup"><span data-stu-id="cd680-118">boolean</span></span> | <span data-ttu-id="cd680-119">Indique si un code d’exploitation pour la vulnérabilité est disponible publiquement</span><span class="sxs-lookup"><span data-stu-id="cd680-119">Indicates whether exploit code for the vulnerability is publicly available</span></span> |
| `VulnerabilitySeverityLevel` | <span data-ttu-id="cd680-120">string</span><span class="sxs-lookup"><span data-stu-id="cd680-120">string</span></span> | <span data-ttu-id="cd680-121">Niveau de gravité affecté à la vulnérabilité de sécurité sur la base du score CVSS et des facteurs dynamiques influencés par le paysage des menaces</span><span class="sxs-lookup"><span data-stu-id="cd680-121">Severity level assigned to the security vulnerability based on the CVSS score and dynamic factors influenced by the threat landscape</span></span> |
| `LastModifiedTime` | <span data-ttu-id="cd680-122">DateHeure</span><span class="sxs-lookup"><span data-stu-id="cd680-122">datetime</span></span> | <span data-ttu-id="cd680-123">Date et heure de la dernière modification de l’élément ou des métadonnées associées</span><span class="sxs-lookup"><span data-stu-id="cd680-123">Date and time the item or related metadata was last modified</span></span> |
| `PublishedDate` | <span data-ttu-id="cd680-124">DateHeure</span><span class="sxs-lookup"><span data-stu-id="cd680-124">datetime</span></span> | <span data-ttu-id="cd680-125">La vulnérabilité de la date a été divulguée au public</span><span class="sxs-lookup"><span data-stu-id="cd680-125">Date vulnerability was disclosed to public</span></span> |
| `VulnerabilityDescription` | <span data-ttu-id="cd680-126">string</span><span class="sxs-lookup"><span data-stu-id="cd680-126">string</span></span> | <span data-ttu-id="cd680-127">Description de la vulnérabilité et risques associés</span><span class="sxs-lookup"><span data-stu-id="cd680-127">Description of vulnerability and associated risks</span></span> |
| `AffectedSoftware` | <span data-ttu-id="cd680-128">string</span><span class="sxs-lookup"><span data-stu-id="cd680-128">string</span></span> | <span data-ttu-id="cd680-129">Liste de tous les produits logiciels concernés par la vulnérabilité</span><span class="sxs-lookup"><span data-stu-id="cd680-129">List of all software products affected by the vulnerability</span></span> |

## <a name="related-topics"></a><span data-ttu-id="cd680-130">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="cd680-130">Related topics</span></span>

- [<span data-ttu-id="cd680-131">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="cd680-131">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="cd680-132">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="cd680-132">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="cd680-133">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="cd680-133">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="cd680-134">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="cd680-134">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="cd680-135">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="cd680-135">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="cd680-136">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="cd680-136">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="cd680-137">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="cd680-137">Overview of Threat & Vulnerability Management</span></span>](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)