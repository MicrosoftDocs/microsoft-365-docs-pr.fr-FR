---
title: Table DeviceTvmSoftwareVulnerabilitiesKB dans le schéma de repérage avancé
description: Découvrez les vulnérabilités logicielles suivies par la fonction Gestion des menaces et des vulnérabilités dans la table DeviceTvmSoftwareVulnerabilitiesKB du schéma de repérage avancé.
keywords: chasse avancée, recherche de menace, recherche dans les menaces informatiques, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, schéma, référence, Kusto, table, colonne, type de données, description, menace & gestion des vulnérabilités, TVM, gestion des périphériques, logiciel, inventaire, vulnérabilités, ID CVE, CVSS, DeviceTvmSoftwareVulnerabilitiesKB
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
- m365initiative-m365-defender
ms.topic: article
ms.openlocfilehash: b7ec1a314875327bee6c9f16900874ee109e0a25
ms.sourcegitcommit: de600339b08951d6dd3933288a8da2327a4b6ef3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/13/2020
ms.locfileid: "48429874"
---
# <a name="devicetvmsoftwarevulnerabilitieskb"></a><span data-ttu-id="57983-104">DeviceTvmSoftwareVulnerabilitiesKB</span><span class="sxs-lookup"><span data-stu-id="57983-104">DeviceTvmSoftwareVulnerabilitiesKB</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="57983-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="57983-105">**Applies to:**</span></span>
- <span data-ttu-id="57983-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="57983-106">Microsoft Threat Protection</span></span>



<span data-ttu-id="57983-107">La table `DeviceTvmSoftwareVulnerabilitiesKB` du schéma de repérage avancé contient la liste des vulnérabilités pour lesquelles la fonction [Gestion des menaces et des vulnérabilités](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt) évalue les appareils.</span><span class="sxs-lookup"><span data-stu-id="57983-107">The `DeviceTvmSoftwareVulnerabilitiesKB` table in the advanced hunting schema contains the list of vulnerabilities [Threat & Vulnerability Management](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt) assesses devices for.</span></span> <span data-ttu-id="57983-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="57983-108">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="57983-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="57983-109">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="57983-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="57983-110">Column name</span></span> | <span data-ttu-id="57983-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="57983-111">Data type</span></span> | <span data-ttu-id="57983-112">Description</span><span class="sxs-lookup"><span data-stu-id="57983-112">Description</span></span> |
|-------------|-----------|-------------|
| `CveId` | <span data-ttu-id="57983-113">string</span><span class="sxs-lookup"><span data-stu-id="57983-113">string</span></span> | <span data-ttu-id="57983-114">Identificateur unique affecté à la vulnérabilité de sécurité dans le système Common Vulnerabilities and Exposures (CVE)</span><span class="sxs-lookup"><span data-stu-id="57983-114">Unique identifier assigned to the security vulnerability under the Common Vulnerabilities and Exposures (CVE) system</span></span> |
| `CvssScore` | <span data-ttu-id="57983-115">string</span><span class="sxs-lookup"><span data-stu-id="57983-115">string</span></span> | <span data-ttu-id="57983-116">Score de gravité attribué à la vulnérabilité de sécurité dans le cadre du système Common Vulnerability Scoring System (CVSS)</span><span class="sxs-lookup"><span data-stu-id="57983-116">Severity score assigned to the security vulnerability under th Common Vulnerability Scoring System (CVSS)</span></span> |
| `IsExploitAvailable` | <span data-ttu-id="57983-117">booléen</span><span class="sxs-lookup"><span data-stu-id="57983-117">boolean</span></span> | <span data-ttu-id="57983-118">Indique si un code d’exploitation pour la vulnérabilité est disponible publiquement</span><span class="sxs-lookup"><span data-stu-id="57983-118">Indicates whether exploit code for the vulnerability is publicly available</span></span> |
| `VulnerabilitySeverityLevel` | <span data-ttu-id="57983-119">string</span><span class="sxs-lookup"><span data-stu-id="57983-119">string</span></span> | <span data-ttu-id="57983-120">Niveau de gravité affecté à la vulnérabilité de sécurité sur la base du score CVSS et des facteurs dynamiques influencés par le paysage des menaces</span><span class="sxs-lookup"><span data-stu-id="57983-120">Severity level assigned to the security vulnerability based on the CVSS score and dynamic factors influenced by the threat landscape</span></span> |
| `LastModifiedTime` | <span data-ttu-id="57983-121">DateHeure</span><span class="sxs-lookup"><span data-stu-id="57983-121">datetime</span></span> | <span data-ttu-id="57983-122">Date et heure de la dernière modification de l’élément ou des métadonnées associées</span><span class="sxs-lookup"><span data-stu-id="57983-122">Date and time the item or related metadata was last modified</span></span> |
| `PublishedDate` | <span data-ttu-id="57983-123">DateHeure</span><span class="sxs-lookup"><span data-stu-id="57983-123">datetime</span></span> | <span data-ttu-id="57983-124">La vulnérabilité de la date a été divulguée au public</span><span class="sxs-lookup"><span data-stu-id="57983-124">Date vulnerability was disclosed to public</span></span> |
| `VulnerabilityDescription` | <span data-ttu-id="57983-125">string</span><span class="sxs-lookup"><span data-stu-id="57983-125">string</span></span> | <span data-ttu-id="57983-126">Description de la vulnérabilité et risques associés</span><span class="sxs-lookup"><span data-stu-id="57983-126">Description of vulnerability and associated risks</span></span> |
| `AffectedSoftware` | <span data-ttu-id="57983-127">string</span><span class="sxs-lookup"><span data-stu-id="57983-127">string</span></span> | <span data-ttu-id="57983-128">Liste de tous les produits logiciels concernés par la vulnérabilité</span><span class="sxs-lookup"><span data-stu-id="57983-128">List of all software products affected by the vulnerability</span></span> |

## <a name="related-topics"></a><span data-ttu-id="57983-129">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="57983-129">Related topics</span></span>

- [<span data-ttu-id="57983-130">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="57983-130">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="57983-131">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="57983-131">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="57983-132">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="57983-132">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="57983-133">Rechercher sur les appareils, les emails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="57983-133">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="57983-134">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="57983-134">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="57983-135">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="57983-135">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="57983-136">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="57983-136">Overview of Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)
