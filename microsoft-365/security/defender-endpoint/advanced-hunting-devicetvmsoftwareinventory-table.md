---
title: Table DeviceTvmSoftwareInventory dans le schéma de recherche avancé
description: Découvrez l’inventaire des logiciels sur vos appareils dans la table DeviceTvmSoftwareInventory du schéma de recherche avancée.
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
ms.openlocfilehash: fc9e5fb29518207c5360d5fbe29b8b4848d350e2
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51067505"
---
# <a name="devicetvmsoftwareinventory"></a><span data-ttu-id="efa01-104">DeviceTvmSoftwareInventory</span><span class="sxs-lookup"><span data-stu-id="efa01-104">DeviceTvmSoftwareInventory</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="efa01-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="efa01-105">**Applies to:**</span></span>
- [<span data-ttu-id="efa01-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="efa01-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)

><span data-ttu-id="efa01-107">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="efa01-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="efa01-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="efa01-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/WindowsForBusiness/windows-atp?ocid=docs-wdatp-advancedhuntingref-abovefoldlink)

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="efa01-109">Le tableau du schéma de recherche avancée contient l’inventaire de gestion des menaces & vulnérabilités des logiciels actuellement installés sur les appareils de votre réseau, y compris les informations de fin `DeviceTvmSoftwareInventory` de support. [](next-gen-threat-and-vuln-mgt.md)</span><span class="sxs-lookup"><span data-stu-id="efa01-109">The `DeviceTvmSoftwareInventory` table in the advanced hunting schema contains the [Threat & Vulnerability Management](next-gen-threat-and-vuln-mgt.md) inventory of software currently installed on devices in your network, including end of support information.</span></span> <span data-ttu-id="efa01-110">Vous pouvez, par exemple, chercher des événements impliquant des appareils installés avec une version logicielle actuellement vulnérable.</span><span class="sxs-lookup"><span data-stu-id="efa01-110">You can, for instance, hunt for events involving devices that are installed with a currently vulnerable software version.</span></span> <span data-ttu-id="efa01-111">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="efa01-111">Use this reference to construct queries that return information from the table.</span></span>

>[!NOTE]
><span data-ttu-id="efa01-112">Les `DeviceTvmSoftwareInventory` `DeviceTvmSoftwareVulnerabilities` tableaux et les tables ont remplacé `DeviceTvmSoftwareInventoryVulnerabilities` le tableau.</span><span class="sxs-lookup"><span data-stu-id="efa01-112">The `DeviceTvmSoftwareInventory` and `DeviceTvmSoftwareVulnerabilities` tables have replaced the `DeviceTvmSoftwareInventoryVulnerabilities` table.</span></span> <span data-ttu-id="efa01-113">Ensemble, les deux premiers tableaux incluent d’autres colonnes que vous pouvez utiliser pour vous aider à informer vos activités de gestion des vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="efa01-113">Together, the first two tables include more columns you can use to help inform your vulnerability management activities.</span></span>

<span data-ttu-id="efa01-114">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference).</span><span class="sxs-lookup"><span data-stu-id="efa01-114">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference).</span></span>

| <span data-ttu-id="efa01-115">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="efa01-115">Column name</span></span> | <span data-ttu-id="efa01-116">Type de données</span><span class="sxs-lookup"><span data-stu-id="efa01-116">Data type</span></span> | <span data-ttu-id="efa01-117">Description</span><span class="sxs-lookup"><span data-stu-id="efa01-117">Description</span></span> |
|-------------|-----------|-------------|
| `DeviceId` | <span data-ttu-id="efa01-118">string</span><span class="sxs-lookup"><span data-stu-id="efa01-118">string</span></span> | <span data-ttu-id="efa01-119">Identificateur unique de l’appareil dans le service</span><span class="sxs-lookup"><span data-stu-id="efa01-119">Unique identifier for the device in the service</span></span> |
| `DeviceName` | <span data-ttu-id="efa01-120">string</span><span class="sxs-lookup"><span data-stu-id="efa01-120">string</span></span> | <span data-ttu-id="efa01-121">Nom de domaine complet (FQDN) de l’appareil</span><span class="sxs-lookup"><span data-stu-id="efa01-121">Fully qualified domain name (FQDN) of the device</span></span> |
| `OSPlatform` | <span data-ttu-id="efa01-122">string</span><span class="sxs-lookup"><span data-stu-id="efa01-122">string</span></span> | <span data-ttu-id="efa01-123">Plateforme du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="efa01-123">Platform of the operating system running on the device.</span></span> <span data-ttu-id="efa01-124">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="efa01-124">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> |
| `OSVersion` | <span data-ttu-id="efa01-125">string</span><span class="sxs-lookup"><span data-stu-id="efa01-125">string</span></span> | <span data-ttu-id="efa01-126">Version du système d’exploitation en cours d’exécution sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="efa01-126">Version of the operating system running on the device</span></span> |
| `OSArchitecture` | <span data-ttu-id="efa01-127">string</span><span class="sxs-lookup"><span data-stu-id="efa01-127">string</span></span> | <span data-ttu-id="efa01-128">Architecture du système d’exploitation en cours d’exécution sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="efa01-128">Architecture of the operating system running on the device</span></span> |
| `SoftwareVendor` | <span data-ttu-id="efa01-129">string</span><span class="sxs-lookup"><span data-stu-id="efa01-129">string</span></span> | <span data-ttu-id="efa01-130">Nom du fournisseur de logiciels</span><span class="sxs-lookup"><span data-stu-id="efa01-130">Name of the software vendor</span></span> |
| `SoftwareName` | <span data-ttu-id="efa01-131">string</span><span class="sxs-lookup"><span data-stu-id="efa01-131">string</span></span> | <span data-ttu-id="efa01-132">Nom du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="efa01-132">Name of the software product</span></span> |
| `SoftwareVersion` | <span data-ttu-id="efa01-133">string</span><span class="sxs-lookup"><span data-stu-id="efa01-133">string</span></span> | <span data-ttu-id="efa01-134">Numéro de version du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="efa01-134">Version number of the software product</span></span> |
| `EndOfSupportStatus` | <span data-ttu-id="efa01-135">string</span><span class="sxs-lookup"><span data-stu-id="efa01-135">string</span></span> | <span data-ttu-id="efa01-136">Indique l’étape de cycle de vie du produit logiciel par rapport à sa date de fin de support (EOS) ou de fin de vie (EOL) spécifiée</span><span class="sxs-lookup"><span data-stu-id="efa01-136">Indicates the lifecycle stage of the software product relative to its specified end-of-support (EOS) or end-of-life (EOL) date</span></span> |
| `EndOfSupportDate` | <span data-ttu-id="efa01-137">string</span><span class="sxs-lookup"><span data-stu-id="efa01-137">string</span></span> | <span data-ttu-id="efa01-138">Date de fin de support (EOS) ou de fin de vie (EOL) du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="efa01-138">End-of-support (EOS) or end-of-life (EOL) date of the software product</span></span> |



## <a name="related-topics"></a><span data-ttu-id="efa01-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efa01-139">Related topics</span></span>

- [<span data-ttu-id="efa01-140">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="efa01-140">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="efa01-141">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="efa01-141">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="efa01-142">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="efa01-142">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
- [<span data-ttu-id="efa01-143">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="efa01-143">Overview of Threat & Vulnerability Management</span></span>](next-gen-threat-and-vuln-mgt.md)

