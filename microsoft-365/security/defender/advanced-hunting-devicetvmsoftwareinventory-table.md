---
title: Table DeviceTvmSoftwareInventory dans le schéma de recherche avancé
description: Découvrez l'inventaire des logiciels sur vos appareils dans la table DeviceTvmSoftwareInventory du schéma de recherche avancée.
keywords: advanced hunting, threat hunting, cyber threat hunting, Microsoft 365 Defender, microsoft 365, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, threat & vulnerability management, TVM, device management, software, inventory, vulnerabilities, CVE ID, OS DeviceTvmSoftwareInventoryVulnerabilities
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
ms.openlocfilehash: 5f82684ebb10b72ff83a6789c010f5ec9fa099e7
ms.sourcegitcommit: 72795ec56a7c4db863dcaaff5e9f7c41c653fda8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "52024228"
---
# <a name="devicetvmsoftwareinventory"></a><span data-ttu-id="28a05-104">DeviceTvmSoftwareInventory</span><span class="sxs-lookup"><span data-stu-id="28a05-104">DeviceTvmSoftwareInventory</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="28a05-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="28a05-105">**Applies to:**</span></span>
- <span data-ttu-id="28a05-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="28a05-106">Microsoft 365 Defender</span></span>
- <span data-ttu-id="28a05-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="28a05-107">Microsoft Defender for Endpoint</span></span>

>[!IMPORTANT]
> <span data-ttu-id="28a05-108">Certaines informations ont trait à un produit préalablement publié, qui peut être modifié de manière significative avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="28a05-108">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="28a05-109">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="28a05-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>


<span data-ttu-id="28a05-110">Le tableau du schéma de recherche avancée contient l'inventaire de gestion des menaces & vulnérabilités des logiciels actuellement installés sur les appareils de votre réseau, y compris les informations de fin `DeviceTvmSoftwareInventory` de support. [](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)</span><span class="sxs-lookup"><span data-stu-id="28a05-110">The `DeviceTvmSoftwareInventory` table in the advanced hunting schema contains the [Threat & Vulnerability Management](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt) inventory of software currently installed on devices in your network, including end of support information.</span></span> <span data-ttu-id="28a05-111">Vous pouvez, par exemple, chercher des événements impliquant des appareils qui sont installés avec une version logicielle actuellement vulnérable.</span><span class="sxs-lookup"><span data-stu-id="28a05-111">You can, for instance, hunt for events involving devices that are installed with a currently vulnerable software version.</span></span> <span data-ttu-id="28a05-112">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="28a05-112">Use this reference to construct queries that return information from the table.</span></span>

>[!NOTE]
> <span data-ttu-id="28a05-113">Les `DeviceTvmSoftwareInventory` `DeviceTvmSoftwareVulnerabilities` tableaux et les tables ont remplacé `DeviceTvmSoftwareInventoryVulnerabilities` le tableau.</span><span class="sxs-lookup"><span data-stu-id="28a05-113">The `DeviceTvmSoftwareInventory` and `DeviceTvmSoftwareVulnerabilities` tables have replaced the `DeviceTvmSoftwareInventoryVulnerabilities` table.</span></span> <span data-ttu-id="28a05-114">Ensemble, les deux premiers tableaux incluent d'autres colonnes que vous pouvez utiliser pour vous aider à informer vos activités de gestion de la vulnerablity ou à la recherche d'appareils vulnérables.</span><span class="sxs-lookup"><span data-stu-id="28a05-114">Together, the first two tables include more columns you can use to help inform your vulnerablity management activities or hunt for vulnerable devices.</span></span>

<span data-ttu-id="28a05-115">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="28a05-115">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="28a05-116">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="28a05-116">Column name</span></span> | <span data-ttu-id="28a05-117">Type de données</span><span class="sxs-lookup"><span data-stu-id="28a05-117">Data type</span></span> | <span data-ttu-id="28a05-118">Description</span><span class="sxs-lookup"><span data-stu-id="28a05-118">Description</span></span> |
|-------------|-----------|-------------|
| `DeviceId` | <span data-ttu-id="28a05-119">string</span><span class="sxs-lookup"><span data-stu-id="28a05-119">string</span></span> | <span data-ttu-id="28a05-120">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="28a05-120">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="28a05-121">string</span><span class="sxs-lookup"><span data-stu-id="28a05-121">string</span></span> | <span data-ttu-id="28a05-122">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="28a05-122">Fully qualified domain name (FQDN) of the machine</span></span> |
| `OSPlatform` | <span data-ttu-id="28a05-123">string</span><span class="sxs-lookup"><span data-stu-id="28a05-123">string</span></span> | <span data-ttu-id="28a05-124">Plateforme du système d’exploitation client s’exécutant sur la machine.</span><span class="sxs-lookup"><span data-stu-id="28a05-124">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="28a05-125">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="28a05-125">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> |
| `OSVersion` | <span data-ttu-id="28a05-126">string</span><span class="sxs-lookup"><span data-stu-id="28a05-126">string</span></span> | <span data-ttu-id="28a05-127">Version du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="28a05-127">Version of the operating system running on the machine</span></span> |
| `OSArchitecture` | <span data-ttu-id="28a05-128">string</span><span class="sxs-lookup"><span data-stu-id="28a05-128">string</span></span> | <span data-ttu-id="28a05-129">Architecture du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="28a05-129">Architecture of the operating system running on the machine</span></span> |
| `SoftwareVendor` | <span data-ttu-id="28a05-130">string</span><span class="sxs-lookup"><span data-stu-id="28a05-130">string</span></span> | <span data-ttu-id="28a05-131">Nom du fournisseur de logiciels</span><span class="sxs-lookup"><span data-stu-id="28a05-131">Name of the software vendor</span></span> |
| `SoftwareName` | <span data-ttu-id="28a05-132">string</span><span class="sxs-lookup"><span data-stu-id="28a05-132">string</span></span> | <span data-ttu-id="28a05-133">Nom du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="28a05-133">Name of the software product</span></span> |
| `SoftwareVersion` | <span data-ttu-id="28a05-134">string</span><span class="sxs-lookup"><span data-stu-id="28a05-134">string</span></span> | <span data-ttu-id="28a05-135">Numéro de version du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="28a05-135">Version number of the software product</span></span> |
| `EndOfSupportStatus` | <span data-ttu-id="28a05-136">string</span><span class="sxs-lookup"><span data-stu-id="28a05-136">string</span></span> | <span data-ttu-id="28a05-137">Indique l'étape de cycle de vie du produit logiciel par rapport à sa date de fin de support (EOS) ou de fin de vie (EOL) spécifiée</span><span class="sxs-lookup"><span data-stu-id="28a05-137">Indicates the lifecycle stage of the software product relative to its specified end-of-support (EOS) or end-of-life (EOL) date</span></span> |
| `EndOfSupportDate` | <span data-ttu-id="28a05-138">string</span><span class="sxs-lookup"><span data-stu-id="28a05-138">string</span></span> | <span data-ttu-id="28a05-139">Date de fin de support (EOS) ou de fin de vie (EOL) du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="28a05-139">End-of-support (EOS) or end-of-life (EOL) date of the software product</span></span> |



## <a name="related-topics"></a><span data-ttu-id="28a05-140">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="28a05-140">Related topics</span></span>

- [<span data-ttu-id="28a05-141">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="28a05-141">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="28a05-142">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="28a05-142">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="28a05-143">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="28a05-143">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="28a05-144">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="28a05-144">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="28a05-145">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="28a05-145">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="28a05-146">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="28a05-146">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="28a05-147">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="28a05-147">Overview of Threat & Vulnerability Management</span></span>](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)