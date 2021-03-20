---
title: Table DeviceTvmSoftwareVulnerabilities dans le schéma de recherche avancé
description: Découvrez les vulnérabilités logicielles trouvées sur les appareils et la liste des mises à jour de sécurité disponibles qui s’adressent à chaque vulnérabilité dans la table DeviceTvmSoftwareVulnerabilities du schéma de recherche avancée.
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, threat & vulnerability management, TVM, device management, software, inventory, vulnerabilities, CVE ID, OS DeviceTvmSoftwareInventoryVulnerabilities
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
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: dfa0c74757a5403573a9300002b92e4b2b109ebb
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50907251"
---
# <a name="devicetvmsoftwarevulnerabilities"></a><span data-ttu-id="65a0f-104">DeviceTvmSoftwareVulnerabilities</span><span class="sxs-lookup"><span data-stu-id="65a0f-104">DeviceTvmSoftwareVulnerabilities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="65a0f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="65a0f-105">**Applies to:**</span></span>
- <span data-ttu-id="65a0f-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="65a0f-106">Microsoft 365 Defender</span></span>

>[!IMPORTANT]
> <span data-ttu-id="65a0f-107">Certaines informations concernent des produits pré-publiés qui peuvent être considérablement modifiés avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="65a0f-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="65a0f-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="65a0f-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="65a0f-109">Le tableau du schéma de recherche avancée contient la liste des vulnérabilités de gestion des menaces & vulnérabilités dans les `DeviceTvmSoftwareVulnerabilities` produits logiciels [](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt) installés.</span><span class="sxs-lookup"><span data-stu-id="65a0f-109">The `DeviceTvmSoftwareVulnerabilities` table in the advanced hunting schema contains the [Threat & Vulnerability Management](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt) list of vulnerabilities in installed software products.</span></span> <span data-ttu-id="65a0f-110">Cette table inclut également des informations sur le système d’exploitation, les ID CVE et sur la gravité des vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="65a0f-110">This table also includes operating system information, CVE IDs, and vulnerability severity information.</span></span> <span data-ttu-id="65a0f-111">Vous pouvez utiliser ce tableau, par exemple, pour chercher les événements impliquant des appareils qui ont des vulnérabilités graves dans leur logiciel.</span><span class="sxs-lookup"><span data-stu-id="65a0f-111">You can use this table, for example, to hunt for events involving devices that have severe vulnerabilities in their software.</span></span> <span data-ttu-id="65a0f-112">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="65a0f-112">Use this reference to construct queries that return information from the table.</span></span>

>[!NOTE]
> <span data-ttu-id="65a0f-113">Les `DeviceTvmSoftwareInventory` tableaux `DeviceTvmSoftwareVulnerabilities` et les tables ont remplacé le `DeviceTvmSoftwareInventoryVulnerabilities` tableau.</span><span class="sxs-lookup"><span data-stu-id="65a0f-113">The `DeviceTvmSoftwareInventory` and `DeviceTvmSoftwareVulnerabilities` tables have replaced the `DeviceTvmSoftwareInventoryVulnerabilities` table.</span></span> <span data-ttu-id="65a0f-114">Ensemble, les deux premiers tableaux incluent d’autres colonnes que vous pouvez utiliser pour vous aider à informer vos activités de gestion de la vulnerablity ou à la recherche d’appareils vulnérables.</span><span class="sxs-lookup"><span data-stu-id="65a0f-114">Together, the first two tables include more columns you can use to help inform your vulnerablity management activities or hunt for vulnerable devices.</span></span>

<span data-ttu-id="65a0f-115">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="65a0f-115">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="65a0f-116">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="65a0f-116">Column name</span></span> | <span data-ttu-id="65a0f-117">Type de données</span><span class="sxs-lookup"><span data-stu-id="65a0f-117">Data type</span></span> | <span data-ttu-id="65a0f-118">Description</span><span class="sxs-lookup"><span data-stu-id="65a0f-118">Description</span></span> |
|-------------|-----------|-------------|
| `DeviceId` | <span data-ttu-id="65a0f-119">string</span><span class="sxs-lookup"><span data-stu-id="65a0f-119">string</span></span> | <span data-ttu-id="65a0f-120">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="65a0f-120">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="65a0f-121">string</span><span class="sxs-lookup"><span data-stu-id="65a0f-121">string</span></span> | <span data-ttu-id="65a0f-122">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="65a0f-122">Fully qualified domain name (FQDN) of the machine</span></span> |
| `OSPlatform` | <span data-ttu-id="65a0f-123">string</span><span class="sxs-lookup"><span data-stu-id="65a0f-123">string</span></span> | <span data-ttu-id="65a0f-124">Plateforme du système d’exploitation client s’exécutant sur la machine.</span><span class="sxs-lookup"><span data-stu-id="65a0f-124">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="65a0f-125">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="65a0f-125">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> |
| `OSVersion` | <span data-ttu-id="65a0f-126">string</span><span class="sxs-lookup"><span data-stu-id="65a0f-126">string</span></span> | <span data-ttu-id="65a0f-127">Version du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="65a0f-127">Version of the operating system running on the machine</span></span> |
| `OSArchitecture` | <span data-ttu-id="65a0f-128">string</span><span class="sxs-lookup"><span data-stu-id="65a0f-128">string</span></span> | <span data-ttu-id="65a0f-129">Architecture du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="65a0f-129">Architecture of the operating system running on the machine</span></span> |
| `SoftwareVendor` | <span data-ttu-id="65a0f-130">string</span><span class="sxs-lookup"><span data-stu-id="65a0f-130">string</span></span> | <span data-ttu-id="65a0f-131">Nom du fournisseur de logiciels</span><span class="sxs-lookup"><span data-stu-id="65a0f-131">Name of the software vendor</span></span> |
| `SoftwareName` | <span data-ttu-id="65a0f-132">string</span><span class="sxs-lookup"><span data-stu-id="65a0f-132">string</span></span> | <span data-ttu-id="65a0f-133">Nom du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="65a0f-133">Name of the software product</span></span> |
| `SoftwareVersion` | <span data-ttu-id="65a0f-134">string</span><span class="sxs-lookup"><span data-stu-id="65a0f-134">string</span></span> | <span data-ttu-id="65a0f-135">Numéro de version du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="65a0f-135">Version number of the software product</span></span> |
| `CveId` | <span data-ttu-id="65a0f-136">string</span><span class="sxs-lookup"><span data-stu-id="65a0f-136">string</span></span> | <span data-ttu-id="65a0f-137">Identificateur unique affecté à la vulnérabilité de sécurité dans le système Common Vulnerabilities and Exposures (CVE)</span><span class="sxs-lookup"><span data-stu-id="65a0f-137">Unique identifier assigned to the security vulnerability under the Common Vulnerabilities and Exposures (CVE) system</span></span> |
| `VulnerabilitySeverityLevel` | <span data-ttu-id="65a0f-138">string</span><span class="sxs-lookup"><span data-stu-id="65a0f-138">string</span></span> | <span data-ttu-id="65a0f-139">Niveau de gravité affecté à la vulnérabilité de sécurité sur la base du score CVSS et des facteurs dynamiques influencés par le paysage des menaces</span><span class="sxs-lookup"><span data-stu-id="65a0f-139">Severity level assigned to the security vulnerability based on the CVSS score and dynamic factors influenced by the threat landscape</span></span> |
| `RecommendedSecurityUpdate` | <span data-ttu-id="65a0f-140">string</span><span class="sxs-lookup"><span data-stu-id="65a0f-140">string</span></span> | <span data-ttu-id="65a0f-141">Nom ou description de la mise à jour de sécurité fournie par le fournisseur de logiciels pour résoudre la vulnérabilité</span><span class="sxs-lookup"><span data-stu-id="65a0f-141">Name or description of the security update provided by the software vendor to address the vulnerability</span></span> |
| `RecommendedSecurityUpdateId` | <span data-ttu-id="65a0f-142">string</span><span class="sxs-lookup"><span data-stu-id="65a0f-142">string</span></span> | <span data-ttu-id="65a0f-143">Identificateur des mises à jour de sécurité applicables ou identificateur pour les articles de base de connaissances ou d’aide correspondants</span><span class="sxs-lookup"><span data-stu-id="65a0f-143">Identifier of the applicable security updates or identifier for the corresponding guidance or knowledge base (KB) articles</span></span> |



## <a name="related-topics"></a><span data-ttu-id="65a0f-144">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="65a0f-144">Related topics</span></span>

- [<span data-ttu-id="65a0f-145">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="65a0f-145">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="65a0f-146">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="65a0f-146">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="65a0f-147">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="65a0f-147">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="65a0f-148">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="65a0f-148">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="65a0f-149">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="65a0f-149">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="65a0f-150">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="65a0f-150">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="65a0f-151">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="65a0f-151">Overview of Threat & Vulnerability Management</span></span>](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)