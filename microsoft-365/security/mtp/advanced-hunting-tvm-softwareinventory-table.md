---
title: Table DeviceTvmSoftwareInventoryVulnerabilities dans le schéma de repérage avancé
description: Découvrez l’inventaire des logiciels dans vos appareils et leurs vulnérabilités dans la table DeviceTvmSoftwareInventoryVulnerabilities du schéma de repérage avancé.
keywords: repérage avancé, repérage de menace, repérage de cybermenace, recherche, requête, télémétrie, schéma, référence, Kusto, table, colonne, type de données, description, gestion des menaces et vulnérabilités, TVM, gestion des appareils, logiciel, inventaire, vulnérabilités, ID CVE , OS DeviceTvmSoftwareInventoryVulnerabilities
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
ms.openlocfilehash: 6aca41e46af8ba94f87e7ee91059c3d11a4fbe9e
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40808629"
---
# <a name="devicetvmsoftwareinventoryvulnerabilities"></a><span data-ttu-id="b3d32-104">DeviceTvmSoftwareInventoryVulnerabilities</span><span class="sxs-lookup"><span data-stu-id="b3d32-104">DeviceTvmSoftwareInventoryVulnerabilities</span></span>

<span data-ttu-id="b3d32-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b3d32-105">**Applies to:**</span></span>
- <span data-ttu-id="b3d32-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="b3d32-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="b3d32-107">La table `DeviceTvmSoftwareInventoryVulnerabilities` dans le schéma de repérage avancé contient l’inventaire [Gestion des menaces et des vulnérabilités](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt) des logiciels sur vos appareils, ainsi que les vulnérabilités connues dans ces produits logiciels.</span><span class="sxs-lookup"><span data-stu-id="b3d32-107">The `DeviceTvmSoftwareInventoryVulnerabilities` table in the advanced hunting schema contains the [Threat & Vulnerability Management](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt) inventory of software on your devices as well as any known vulnerabilities in these software products.</span></span> <span data-ttu-id="b3d32-108">Cette table inclut également des informations sur le système d’exploitation, les ID CVE et sur la gravité des vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="b3d32-108">This table also includes operating system information, CVE IDs, and vulnerability severity information.</span></span> <span data-ttu-id="b3d32-109">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="b3d32-109">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="b3d32-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b3d32-110">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="b3d32-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b3d32-111">Column name</span></span> | <span data-ttu-id="b3d32-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3d32-112">Data type</span></span> | <span data-ttu-id="b3d32-113">Description</span><span class="sxs-lookup"><span data-stu-id="b3d32-113">Description</span></span> |
|-------------|-----------|-------------|
| `DeviceId` | <span data-ttu-id="b3d32-114">string</span><span class="sxs-lookup"><span data-stu-id="b3d32-114">string</span></span> | <span data-ttu-id="b3d32-115">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="b3d32-115">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="b3d32-116">string</span><span class="sxs-lookup"><span data-stu-id="b3d32-116">string</span></span> | <span data-ttu-id="b3d32-117">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="b3d32-117">Fully qualified domain name (FQDN) of the machine</span></span> |
| `OSPlatform` | <span data-ttu-id="b3d32-118">string</span><span class="sxs-lookup"><span data-stu-id="b3d32-118">string</span></span> | <span data-ttu-id="b3d32-119">Plateforme du système d’exploitation client s’exécutant sur la machine.</span><span class="sxs-lookup"><span data-stu-id="b3d32-119">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="b3d32-120">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b3d32-120">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> |
| `OSVersion` | <span data-ttu-id="b3d32-121">string</span><span class="sxs-lookup"><span data-stu-id="b3d32-121">string</span></span> | <span data-ttu-id="b3d32-122">Version du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="b3d32-122">Version of the operating system running on the machine</span></span> |
| `OSArchitecture` | <span data-ttu-id="b3d32-123">string</span><span class="sxs-lookup"><span data-stu-id="b3d32-123">string</span></span> | <span data-ttu-id="b3d32-124">Architecture du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="b3d32-124">Architecture of the operating system running on the machine</span></span> |
| `SoftwareVendor` | <span data-ttu-id="b3d32-125">string</span><span class="sxs-lookup"><span data-stu-id="b3d32-125">string</span></span> | <span data-ttu-id="b3d32-126">Niveau de gravité affecté à la vulnérabilité de sécurité sur la base du score CVSS et des facteurs dynamiques influencés par le paysage des menaces</span><span class="sxs-lookup"><span data-stu-id="b3d32-126">Severity level assigned to the security vulnerability based on the CVSS score and dynamic factors influenced by the threat landscape</span></span> |
| `SoftwareName` | <span data-ttu-id="b3d32-127">string</span><span class="sxs-lookup"><span data-stu-id="b3d32-127">string</span></span> | <span data-ttu-id="b3d32-128">Nom du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="b3d32-128">Name of the software product</span></span> |
| `SoftwareVersion` | <span data-ttu-id="b3d32-129">string</span><span class="sxs-lookup"><span data-stu-id="b3d32-129">string</span></span> | <span data-ttu-id="b3d32-130">Numéro de version du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="b3d32-130">Version number of the software product</span></span> |
| `CveId` | <span data-ttu-id="b3d32-131">string</span><span class="sxs-lookup"><span data-stu-id="b3d32-131">string</span></span> | <span data-ttu-id="b3d32-132">Identificateur unique affecté à la vulnérabilité de sécurité dans le système Common Vulnerabilities and Exposures (CVE)</span><span class="sxs-lookup"><span data-stu-id="b3d32-132">Unique identifier assigned to the security vulnerability under the Common Vulnerabilities and Exposures (CVE) system</span></span> |
| `VulnerabilitySeverityLevel` | <span data-ttu-id="b3d32-133">string</span><span class="sxs-lookup"><span data-stu-id="b3d32-133">string</span></span> | <span data-ttu-id="b3d32-134">Niveau de gravité affecté à la vulnérabilité de sécurité sur la base du score CVSS et des facteurs dynamiques influencés par le paysage des menaces</span><span class="sxs-lookup"><span data-stu-id="b3d32-134">Severity level assigned to the security vulnerability based on the CVSS score and dynamic factors influenced by the threat landscape</span></span> |



## <a name="related-topics"></a><span data-ttu-id="b3d32-135">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="b3d32-135">Related topics</span></span>

- [<span data-ttu-id="b3d32-136">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="b3d32-136">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="b3d32-137">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="b3d32-137">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="b3d32-138">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="b3d32-138">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="b3d32-139">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="b3d32-139">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="b3d32-140">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="b3d32-140">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="b3d32-141">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="b3d32-141">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="b3d32-142">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="b3d32-142">Overview of Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)
