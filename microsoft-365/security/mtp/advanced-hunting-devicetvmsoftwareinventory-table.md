---
title: Table DeviceTvmSoftwareInventory dans le schéma de recherche avancé
description: Découvrez l’inventaire des logiciels sur vos appareils dans la table DeviceTvmSoftwareInventory du schéma de recherche avancée.
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
ms.openlocfilehash: 0bdd3b8564a01b36d1c21d0f49a29ce1afd98348
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50907327"
---
# <a name="devicetvmsoftwareinventory"></a><span data-ttu-id="8d199-104">DeviceTvmSoftwareInventory</span><span class="sxs-lookup"><span data-stu-id="8d199-104">DeviceTvmSoftwareInventory</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="8d199-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8d199-105">**Applies to:**</span></span>
- <span data-ttu-id="8d199-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8d199-106">Microsoft 365 Defender</span></span>

>[!IMPORTANT]
> <span data-ttu-id="8d199-107">Certaines informations concernent des produits pré-publiés qui peuvent être considérablement modifiés avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="8d199-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8d199-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="8d199-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>


<span data-ttu-id="8d199-109">Le tableau du schéma de recherche avancée contient l’inventaire de gestion des menaces & vulnérabilités des logiciels actuellement installés sur les appareils de votre réseau, y compris les informations de fin `DeviceTvmSoftwareInventory` de support. [](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)</span><span class="sxs-lookup"><span data-stu-id="8d199-109">The `DeviceTvmSoftwareInventory` table in the advanced hunting schema contains the [Threat & Vulnerability Management](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt) inventory of software currently installed on devices in your network, including end of support information.</span></span> <span data-ttu-id="8d199-110">Vous pouvez, par exemple, chercher des événements impliquant des appareils qui sont installés avec une version logicielle actuellement vulnérable.</span><span class="sxs-lookup"><span data-stu-id="8d199-110">You can, for instance, hunt for events involving devices that are installed with a currently vulnerable software version.</span></span> <span data-ttu-id="8d199-111">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="8d199-111">Use this reference to construct queries that return information from the table.</span></span>

>[!NOTE]
> <span data-ttu-id="8d199-112">Les `DeviceTvmSoftwareInventory` tableaux `DeviceTvmSoftwareVulnerabilities` et les tables ont remplacé le `DeviceTvmSoftwareInventoryVulnerabilities` tableau.</span><span class="sxs-lookup"><span data-stu-id="8d199-112">The `DeviceTvmSoftwareInventory` and `DeviceTvmSoftwareVulnerabilities` tables have replaced the `DeviceTvmSoftwareInventoryVulnerabilities` table.</span></span> <span data-ttu-id="8d199-113">Ensemble, les deux premiers tableaux incluent d’autres colonnes que vous pouvez utiliser pour vous aider à informer vos activités de gestion de la vulnerablity ou à la recherche d’appareils vulnérables.</span><span class="sxs-lookup"><span data-stu-id="8d199-113">Together, the first two tables include more columns you can use to help inform your vulnerablity management activities or hunt for vulnerable devices.</span></span>

<span data-ttu-id="8d199-114">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8d199-114">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="8d199-115">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="8d199-115">Column name</span></span> | <span data-ttu-id="8d199-116">Type de données</span><span class="sxs-lookup"><span data-stu-id="8d199-116">Data type</span></span> | <span data-ttu-id="8d199-117">Description</span><span class="sxs-lookup"><span data-stu-id="8d199-117">Description</span></span> |
|-------------|-----------|-------------|
| `DeviceId` | <span data-ttu-id="8d199-118">string</span><span class="sxs-lookup"><span data-stu-id="8d199-118">string</span></span> | <span data-ttu-id="8d199-119">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="8d199-119">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="8d199-120">string</span><span class="sxs-lookup"><span data-stu-id="8d199-120">string</span></span> | <span data-ttu-id="8d199-121">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="8d199-121">Fully qualified domain name (FQDN) of the machine</span></span> |
| `OSPlatform` | <span data-ttu-id="8d199-122">string</span><span class="sxs-lookup"><span data-stu-id="8d199-122">string</span></span> | <span data-ttu-id="8d199-123">Plateforme du système d’exploitation client s’exécutant sur la machine.</span><span class="sxs-lookup"><span data-stu-id="8d199-123">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="8d199-124">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8d199-124">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> |
| `OSVersion` | <span data-ttu-id="8d199-125">string</span><span class="sxs-lookup"><span data-stu-id="8d199-125">string</span></span> | <span data-ttu-id="8d199-126">Version du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="8d199-126">Version of the operating system running on the machine</span></span> |
| `OSArchitecture` | <span data-ttu-id="8d199-127">string</span><span class="sxs-lookup"><span data-stu-id="8d199-127">string</span></span> | <span data-ttu-id="8d199-128">Architecture du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="8d199-128">Architecture of the operating system running on the machine</span></span> |
| `SoftwareVendor` | <span data-ttu-id="8d199-129">string</span><span class="sxs-lookup"><span data-stu-id="8d199-129">string</span></span> | <span data-ttu-id="8d199-130">Nom du fournisseur de logiciels</span><span class="sxs-lookup"><span data-stu-id="8d199-130">Name of the software vendor</span></span> |
| `SoftwareName` | <span data-ttu-id="8d199-131">string</span><span class="sxs-lookup"><span data-stu-id="8d199-131">string</span></span> | <span data-ttu-id="8d199-132">Nom du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="8d199-132">Name of the software product</span></span> |
| `SoftwareVersion` | <span data-ttu-id="8d199-133">string</span><span class="sxs-lookup"><span data-stu-id="8d199-133">string</span></span> | <span data-ttu-id="8d199-134">Numéro de version du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="8d199-134">Version number of the software product</span></span> |
| `EndOfSupportStatus` | <span data-ttu-id="8d199-135">string</span><span class="sxs-lookup"><span data-stu-id="8d199-135">string</span></span> | <span data-ttu-id="8d199-136">Indique l’étape de cycle de vie du produit logiciel par rapport à sa date de fin de support (EOS) ou de fin de vie (EOL) spécifiée</span><span class="sxs-lookup"><span data-stu-id="8d199-136">Indicates the lifecycle stage of the software product relative to its specified end-of-support (EOS) or end-of-life (EOL) date</span></span> |
| `EndOfSupportDate` | <span data-ttu-id="8d199-137">string</span><span class="sxs-lookup"><span data-stu-id="8d199-137">string</span></span> | <span data-ttu-id="8d199-138">Date de fin de support (EOS) ou de fin de vie (EOL) du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="8d199-138">End-of-support (EOS) or end-of-life (EOL) date of the software product</span></span> |



## <a name="related-topics"></a><span data-ttu-id="8d199-139">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="8d199-139">Related topics</span></span>

- [<span data-ttu-id="8d199-140">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="8d199-140">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="8d199-141">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="8d199-141">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="8d199-142">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="8d199-142">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="8d199-143">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="8d199-143">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="8d199-144">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="8d199-144">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="8d199-145">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="8d199-145">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="8d199-146">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="8d199-146">Overview of Threat & Vulnerability Management</span></span>](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)