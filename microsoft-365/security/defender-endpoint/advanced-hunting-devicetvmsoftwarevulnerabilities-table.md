---
title: Table DeviceTvmSoftwareVulnerabilities dans le schéma de recherche avancé
description: Découvrez les vulnérabilités logicielles trouvées sur les appareils et la liste des mises à jour de sécurité disponibles qui adressent chaque vulnérabilité dans la table DeviceTvmSoftwareVulnerabilities du schéma de recherche avancée.
keywords: advanced hunting, threat hunting, cyber threat hunting, mdatp, microsoft defender atp, wdatp search, query, telemetry, schema reference, kusto, table, column, data type, description, threat & vulnerability management, TVM, device management, software, inventory, vulnerabilities, CVE ID, OS DeviceTvmSoftwareInventoryVulnerabilities
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: maccruz
author: schmurky
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 6b38297cd0fa2e931619ff9c0557d2ae868c7aa4
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51067998"
---
# <a name="devicetvmsoftwarevulnerabilities"></a><span data-ttu-id="a4126-104">DeviceTvmSoftwareVulnerabilities</span><span class="sxs-lookup"><span data-stu-id="a4126-104">DeviceTvmSoftwareVulnerabilities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="a4126-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a4126-105">**Applies to:**</span></span>
- [<span data-ttu-id="a4126-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a4126-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)


><span data-ttu-id="a4126-107">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="a4126-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="a4126-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="a4126-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/WindowsForBusiness/windows-atp?ocid=docs-wdatp-advancedhuntingref-abovefoldlink)

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="a4126-109">Le tableau du schéma de recherche avancée contient la liste des vulnérabilités de gestion des menaces & vulnérabilités dans les `DeviceTvmSoftwareVulnerabilities` produits logiciels [](next-gen-threat-and-vuln-mgt.md) installés.</span><span class="sxs-lookup"><span data-stu-id="a4126-109">The `DeviceTvmSoftwareVulnerabilities` table in the advanced hunting schema contains the [Threat & Vulnerability Management](next-gen-threat-and-vuln-mgt.md) list of vulnerabilities in installed software products.</span></span> <span data-ttu-id="a4126-110">Cette table inclut également des informations sur le système d’exploitation, les ID CVE et sur la gravité des vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="a4126-110">This table also includes operating system information, CVE IDs, and vulnerability severity information.</span></span> <span data-ttu-id="a4126-111">Vous pouvez utiliser ce tableau, par exemple, pour chercher les événements impliquant des appareils qui ont des vulnérabilités graves dans leur logiciel.</span><span class="sxs-lookup"><span data-stu-id="a4126-111">You can use this table, for example, to hunt for events involving devices that have severe vulnerabilities in their software.</span></span> <span data-ttu-id="a4126-112">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="a4126-112">Use this reference to construct queries that return information from the table.</span></span>

>[!NOTE]
><span data-ttu-id="a4126-113">Les `DeviceTvmSoftwareInventory` `DeviceTvmSoftwareVulnerabilities` tableaux et les tables ont remplacé `DeviceTvmSoftwareInventoryVulnerabilities` le tableau.</span><span class="sxs-lookup"><span data-stu-id="a4126-113">The `DeviceTvmSoftwareInventory` and `DeviceTvmSoftwareVulnerabilities` tables have replaced the `DeviceTvmSoftwareInventoryVulnerabilities` table.</span></span> <span data-ttu-id="a4126-114">Ensemble, les deux premiers tableaux incluent d’autres colonnes que vous pouvez utiliser pour vous aider à informer vos activités de gestion des vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="a4126-114">Together, the first two tables include more columns you can use to help inform your vulnerability management activities.</span></span>

<span data-ttu-id="a4126-115">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference).</span><span class="sxs-lookup"><span data-stu-id="a4126-115">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference).</span></span>

| <span data-ttu-id="a4126-116">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="a4126-116">Column name</span></span> | <span data-ttu-id="a4126-117">Type de données</span><span class="sxs-lookup"><span data-stu-id="a4126-117">Data type</span></span> | <span data-ttu-id="a4126-118">Description</span><span class="sxs-lookup"><span data-stu-id="a4126-118">Description</span></span> |
|-------------|-----------|-------------|
| `DeviceId` | <span data-ttu-id="a4126-119">string</span><span class="sxs-lookup"><span data-stu-id="a4126-119">string</span></span> | <span data-ttu-id="a4126-120">Identificateur unique de l’appareil dans le service</span><span class="sxs-lookup"><span data-stu-id="a4126-120">Unique identifier for the device in the service</span></span> |
| `DeviceName` | <span data-ttu-id="a4126-121">string</span><span class="sxs-lookup"><span data-stu-id="a4126-121">string</span></span> | <span data-ttu-id="a4126-122">Nom de domaine complet (FQDN) de l’appareil</span><span class="sxs-lookup"><span data-stu-id="a4126-122">Fully qualified domain name (FQDN) of the device</span></span> |
| `OSPlatform` | <span data-ttu-id="a4126-123">string</span><span class="sxs-lookup"><span data-stu-id="a4126-123">string</span></span> | <span data-ttu-id="a4126-124">Plateforme du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a4126-124">Platform of the operating system running on the device.</span></span> <span data-ttu-id="a4126-125">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a4126-125">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> |
| `OSVersion` | <span data-ttu-id="a4126-126">string</span><span class="sxs-lookup"><span data-stu-id="a4126-126">string</span></span> | <span data-ttu-id="a4126-127">Version du système d’exploitation en cours d’exécution sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="a4126-127">Version of the operating system running on the device</span></span> |
| `OSArchitecture` | <span data-ttu-id="a4126-128">string</span><span class="sxs-lookup"><span data-stu-id="a4126-128">string</span></span> | <span data-ttu-id="a4126-129">Architecture du système d’exploitation en cours d’exécution sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="a4126-129">Architecture of the operating system running on the device</span></span> |
| `SoftwareVendor` | <span data-ttu-id="a4126-130">string</span><span class="sxs-lookup"><span data-stu-id="a4126-130">string</span></span> | <span data-ttu-id="a4126-131">Nom du fournisseur de logiciels</span><span class="sxs-lookup"><span data-stu-id="a4126-131">Name of the software vendor</span></span> |
| `SoftwareName` | <span data-ttu-id="a4126-132">string</span><span class="sxs-lookup"><span data-stu-id="a4126-132">string</span></span> | <span data-ttu-id="a4126-133">Nom du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="a4126-133">Name of the software product</span></span> |
| `SoftwareVersion` | <span data-ttu-id="a4126-134">string</span><span class="sxs-lookup"><span data-stu-id="a4126-134">string</span></span> | <span data-ttu-id="a4126-135">Numéro de version du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="a4126-135">Version number of the software product</span></span> |
| `CveId` | <span data-ttu-id="a4126-136">string</span><span class="sxs-lookup"><span data-stu-id="a4126-136">string</span></span> | <span data-ttu-id="a4126-137">Identificateur unique affecté à la vulnérabilité de sécurité dans le système Common Vulnerabilities and Exposures (CVE)</span><span class="sxs-lookup"><span data-stu-id="a4126-137">Unique identifier assigned to the security vulnerability under the Common Vulnerabilities and Exposures (CVE) system</span></span> |
| `VulnerabilitySeverityLevel` | <span data-ttu-id="a4126-138">string</span><span class="sxs-lookup"><span data-stu-id="a4126-138">string</span></span> | <span data-ttu-id="a4126-139">Niveau de gravité affecté à la vulnérabilité de sécurité sur la base du score CVSS et des facteurs dynamiques influencés par le paysage des menaces</span><span class="sxs-lookup"><span data-stu-id="a4126-139">Severity level assigned to the security vulnerability based on the CVSS score and dynamic factors influenced by the threat landscape</span></span> |
| `RecommendedSecurityUpdate` | <span data-ttu-id="a4126-140">string</span><span class="sxs-lookup"><span data-stu-id="a4126-140">string</span></span> | <span data-ttu-id="a4126-141">Nom ou description de la mise à jour de sécurité fournie par le fournisseur de logiciels pour résoudre la vulnérabilité</span><span class="sxs-lookup"><span data-stu-id="a4126-141">Name or description of the security update provided by the software vendor to address the vulnerability</span></span> |
| `RecommendedSecurityUpdateId` | <span data-ttu-id="a4126-142">string</span><span class="sxs-lookup"><span data-stu-id="a4126-142">string</span></span> | <span data-ttu-id="a4126-143">Identificateur des mises à jour de sécurité applicables ou identificateur pour les articles de base de connaissances ou d’aide correspondants</span><span class="sxs-lookup"><span data-stu-id="a4126-143">Identifier of the applicable security updates or identifier for the corresponding guidance or knowledge base (KB) articles</span></span> |



## <a name="related-topics"></a><span data-ttu-id="a4126-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4126-144">Related topics</span></span>

- [<span data-ttu-id="a4126-145">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="a4126-145">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="a4126-146">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="a4126-146">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="a4126-147">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="a4126-147">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
- [<span data-ttu-id="a4126-148">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="a4126-148">Overview of Threat & Vulnerability Management</span></span>](next-gen-threat-and-vuln-mgt.md)
