---
title: Table DeviceTvmSoftwareVulnerabilitiesKB dans le schéma de repérage avancé
description: Découvrez les vulnérabilités logicielles suivies par la fonction Gestion des menaces et des vulnérabilités dans la table DeviceTvmSoftwareVulnerabilitiesKB du schéma de repérage avancé.
keywords: advanced hunting, threat hunting, cyber threat hunting, mdatp, microsoft defender atp, wdatp search, query, telemetry, schema reference, kusto, table, column, data type, description, threat & vulnerability management, TVM, device management, software, inventory, vulnerabilities, CVE ID, CVSS, DeviceTvmSoftwareVulnerabilitiesKBB
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
ms.openlocfilehash: 772a287097f0b204eb329d066cdd81c4eef7a755
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51062886"
---
# <a name="devicetvmsoftwarevulnerabilitieskb"></a><span data-ttu-id="6a7ef-104">DeviceTvmSoftwareVulnerabilitiesKB</span><span class="sxs-lookup"><span data-stu-id="6a7ef-104">DeviceTvmSoftwareVulnerabilitiesKB</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="6a7ef-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-105">**Applies to:**</span></span>
- [<span data-ttu-id="6a7ef-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6a7ef-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)

><span data-ttu-id="6a7ef-107">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="6a7ef-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="6a7ef-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/WindowsForBusiness/windows-atp?ocid=docs-wdatp-advancedhuntingref-abovefoldlink)

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="6a7ef-109">La table `DeviceTvmSoftwareVulnerabilitiesKB` du schéma de repérage avancé contient la liste des vulnérabilités pour lesquelles la fonction [Gestion des menaces et des vulnérabilités](next-gen-threat-and-vuln-mgt.md) évalue les appareils.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-109">The `DeviceTvmSoftwareVulnerabilitiesKB` table in the advanced hunting schema contains the list of vulnerabilities [Threat & Vulnerability Management](next-gen-threat-and-vuln-mgt.md) assesses devices for.</span></span> <span data-ttu-id="6a7ef-110">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-110">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="6a7ef-111">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](advanced-hunting-schema-reference.md).</span><span class="sxs-lookup"><span data-stu-id="6a7ef-111">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-reference.md).</span></span>

| <span data-ttu-id="6a7ef-112">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="6a7ef-112">Column name</span></span> | <span data-ttu-id="6a7ef-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="6a7ef-113">Data type</span></span> | <span data-ttu-id="6a7ef-114">Description</span><span class="sxs-lookup"><span data-stu-id="6a7ef-114">Description</span></span> |
|-------------|-----------|-------------|
| `CveId` | <span data-ttu-id="6a7ef-115">string</span><span class="sxs-lookup"><span data-stu-id="6a7ef-115">string</span></span> | <span data-ttu-id="6a7ef-116">Identificateur unique affecté à la vulnérabilité de sécurité dans le système Common Vulnerabilities and Exposures (CVE)</span><span class="sxs-lookup"><span data-stu-id="6a7ef-116">Unique identifier assigned to the security vulnerability under the Common Vulnerabilities and Exposures (CVE) system</span></span> |
| `CvssScore` | <span data-ttu-id="6a7ef-117">string</span><span class="sxs-lookup"><span data-stu-id="6a7ef-117">string</span></span> | <span data-ttu-id="6a7ef-118">Score de gravité attribué à la vulnérabilité de sécurité dans le cadre du système Common Vulnerability Scoring System (CVSS)</span><span class="sxs-lookup"><span data-stu-id="6a7ef-118">Severity score assigned to the security vulnerability under th Common Vulnerability Scoring System (CVSS)</span></span> |
| `IsExploitAvailable` | <span data-ttu-id="6a7ef-119">booléen</span><span class="sxs-lookup"><span data-stu-id="6a7ef-119">boolean</span></span> | <span data-ttu-id="6a7ef-120">Indique si un code d’exploitation pour la vulnérabilité est disponible publiquement</span><span class="sxs-lookup"><span data-stu-id="6a7ef-120">Indicates whether exploit code for the vulnerability is publicly available</span></span> |
| `VulnerabilitySeverityLevel` | <span data-ttu-id="6a7ef-121">string</span><span class="sxs-lookup"><span data-stu-id="6a7ef-121">string</span></span> | <span data-ttu-id="6a7ef-122">Niveau de gravité affecté à la vulnérabilité de sécurité sur la base du score CVSS et des facteurs dynamiques influencés par le paysage des menaces</span><span class="sxs-lookup"><span data-stu-id="6a7ef-122">Severity level assigned to the security vulnerability based on the CVSS score and dynamic factors influenced by the threat landscape</span></span> |
| `LastModifiedTime` | <span data-ttu-id="6a7ef-123">DateHeure</span><span class="sxs-lookup"><span data-stu-id="6a7ef-123">datetime</span></span> | <span data-ttu-id="6a7ef-124">Date et heure de la dernière modification de l’élément ou des métadonnées associées</span><span class="sxs-lookup"><span data-stu-id="6a7ef-124">Date and time the item or related metadata was last modified</span></span> |
| `PublishedDate` | <span data-ttu-id="6a7ef-125">DateHeure</span><span class="sxs-lookup"><span data-stu-id="6a7ef-125">datetime</span></span> | <span data-ttu-id="6a7ef-126">La vulnérabilité de la date a été divulguée au public</span><span class="sxs-lookup"><span data-stu-id="6a7ef-126">Date vulnerability was disclosed to public</span></span> |
| `VulnerabilityDescription` | <span data-ttu-id="6a7ef-127">string</span><span class="sxs-lookup"><span data-stu-id="6a7ef-127">string</span></span> | <span data-ttu-id="6a7ef-128">Description de la vulnérabilité et risques associés</span><span class="sxs-lookup"><span data-stu-id="6a7ef-128">Description of vulnerability and associated risks</span></span> |
| `AffectedSoftware` | <span data-ttu-id="6a7ef-129">string</span><span class="sxs-lookup"><span data-stu-id="6a7ef-129">string</span></span> | <span data-ttu-id="6a7ef-130">Liste de tous les produits logiciels concernés par la vulnérabilité</span><span class="sxs-lookup"><span data-stu-id="6a7ef-130">List of all software products affected by the vulnerability</span></span> |

## <a name="related-topics"></a><span data-ttu-id="6a7ef-131">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="6a7ef-131">Related topics</span></span>

- [<span data-ttu-id="6a7ef-132">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="6a7ef-132">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="6a7ef-133">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="6a7ef-133">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="6a7ef-134">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="6a7ef-134">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
- [<span data-ttu-id="6a7ef-135">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="6a7ef-135">Overview of Threat & Vulnerability Management</span></span>](next-gen-threat-and-vuln-mgt.md)
