---
title: Table DeviceTvmSoftwareInventoryVulnerabilities dans le schéma de repérage avancé
description: Découvrez l’inventaire des logiciels dans vos appareils et leurs vulnérabilités dans la table DeviceTvmSoftwareInventoryVulnerabilities du schéma de repérage avancé.
keywords: advanced hunting, threat hunting, cyber threat hunting, mdatp, microsoft defender atp, wdatp search, query, telemetry, schema reference, kusto, table, column, data type, description, threat & vulnerability management, TVM, device management, software, inventory, vulnerabilities, CVE ID, OS DeviceTvmSoftwareInventoryVulnerabilities
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: w10
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
ms.openlocfilehash: bbb535aa3f106c8569edb3c64ba95bba9bf36186
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51163458"
---
# <a name="devicetvmsoftwareinventoryvulnerabilities"></a><span data-ttu-id="9f495-104">DeviceTvmSoftwareInventoryVulnerabilities</span><span class="sxs-lookup"><span data-stu-id="9f495-104">DeviceTvmSoftwareInventoryVulnerabilities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="9f495-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9f495-105">**Applies to:**</span></span>

- [<span data-ttu-id="9f495-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9f495-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)

><span data-ttu-id="9f495-107">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="9f495-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="9f495-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="9f495-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/WindowsForBusiness/windows-atp?ocid=docs-wdatp-advancedhuntingref-abovefoldlink)


[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="9f495-109">La table `DeviceTvmSoftwareInventoryVulnerabilities` dans le schéma de repérage avancé contient l’inventaire [Gestion des menaces et des vulnérabilités](next-gen-threat-and-vuln-mgt.md) des logiciels sur vos appareils, ainsi que les vulnérabilités connues dans ces produits logiciels.</span><span class="sxs-lookup"><span data-stu-id="9f495-109">The `DeviceTvmSoftwareInventoryVulnerabilities` table in the advanced hunting schema contains the [Threat & Vulnerability Management](next-gen-threat-and-vuln-mgt.md) inventory of software on your devices as well as any known vulnerabilities in these software products.</span></span> <span data-ttu-id="9f495-110">Cette table inclut également des informations sur le système d’exploitation, les ID CVE et sur la gravité des vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="9f495-110">This table also includes operating system information, CVE IDs, and vulnerability severity information.</span></span> <span data-ttu-id="9f495-111">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="9f495-111">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="9f495-112">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference).</span><span class="sxs-lookup"><span data-stu-id="9f495-112">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference).</span></span>

| <span data-ttu-id="9f495-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="9f495-113">Column name</span></span> | <span data-ttu-id="9f495-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="9f495-114">Data type</span></span> | <span data-ttu-id="9f495-115">Description</span><span class="sxs-lookup"><span data-stu-id="9f495-115">Description</span></span> |
|-------------|-----------|-------------|
| `DeviceId` | <span data-ttu-id="9f495-116">string</span><span class="sxs-lookup"><span data-stu-id="9f495-116">string</span></span> | <span data-ttu-id="9f495-117">Identificateur unique de l’appareil dans le service</span><span class="sxs-lookup"><span data-stu-id="9f495-117">Unique identifier for the device in the service</span></span> |
| `DeviceName` | <span data-ttu-id="9f495-118">string</span><span class="sxs-lookup"><span data-stu-id="9f495-118">string</span></span> | <span data-ttu-id="9f495-119">Nom de domaine complet (FQDN) de l’appareil</span><span class="sxs-lookup"><span data-stu-id="9f495-119">Fully qualified domain name (FQDN) of the device</span></span> |
| `OSPlatform` | <span data-ttu-id="9f495-120">string</span><span class="sxs-lookup"><span data-stu-id="9f495-120">string</span></span> | <span data-ttu-id="9f495-121">Plateforme du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9f495-121">Platform of the operating system running on the device.</span></span> <span data-ttu-id="9f495-122">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9f495-122">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> |
| `OSVersion` | <span data-ttu-id="9f495-123">string</span><span class="sxs-lookup"><span data-stu-id="9f495-123">string</span></span> | <span data-ttu-id="9f495-124">Version du système d’exploitation en cours d’exécution sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="9f495-124">Version of the operating system running on the device</span></span> |
| `OSArchitecture` | <span data-ttu-id="9f495-125">string</span><span class="sxs-lookup"><span data-stu-id="9f495-125">string</span></span> | <span data-ttu-id="9f495-126">Architecture du système d’exploitation en cours d’exécution sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="9f495-126">Architecture of the operating system running on the device</span></span> |
| `SoftwareVendor` | <span data-ttu-id="9f495-127">string</span><span class="sxs-lookup"><span data-stu-id="9f495-127">string</span></span> | <span data-ttu-id="9f495-128">Nom du fournisseur de logiciels</span><span class="sxs-lookup"><span data-stu-id="9f495-128">Name of the software vendor</span></span> |
| `SoftwareName` | <span data-ttu-id="9f495-129">string</span><span class="sxs-lookup"><span data-stu-id="9f495-129">string</span></span> | <span data-ttu-id="9f495-130">Nom du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="9f495-130">Name of the software product</span></span> |
| `SoftwareVersion` | <span data-ttu-id="9f495-131">string</span><span class="sxs-lookup"><span data-stu-id="9f495-131">string</span></span> | <span data-ttu-id="9f495-132">Numéro de version du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="9f495-132">Version number of the software product</span></span> |
| `CveId` | <span data-ttu-id="9f495-133">string</span><span class="sxs-lookup"><span data-stu-id="9f495-133">string</span></span> | <span data-ttu-id="9f495-134">Identificateur unique affecté à la vulnérabilité de sécurité dans le système Common Vulnerabilities and Exposures (CVE)</span><span class="sxs-lookup"><span data-stu-id="9f495-134">Unique identifier assigned to the security vulnerability under the Common Vulnerabilities and Exposures (CVE) system</span></span> |
| `VulnerabilitySeverityLevel` | <span data-ttu-id="9f495-135">string</span><span class="sxs-lookup"><span data-stu-id="9f495-135">string</span></span> | <span data-ttu-id="9f495-136">Niveau de gravité affecté à la vulnérabilité de sécurité sur la base du score CVSS et des facteurs dynamiques influencés par le paysage des menaces</span><span class="sxs-lookup"><span data-stu-id="9f495-136">Severity level assigned to the security vulnerability based on the CVSS score and dynamic factors influenced by the threat landscape</span></span> |



## <a name="related-topics"></a><span data-ttu-id="9f495-137">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="9f495-137">Related topics</span></span>

- [<span data-ttu-id="9f495-138">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="9f495-138">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="9f495-139">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="9f495-139">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="9f495-140">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="9f495-140">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
- [<span data-ttu-id="9f495-141">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="9f495-141">Overview of Threat & Vulnerability Management</span></span>](next-gen-threat-and-vuln-mgt.md)
