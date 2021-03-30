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
ms.openlocfilehash: 18e43d8e38c24a8aa28c6455dc1a769b8da0df2b
ms.sourcegitcommit: c75aac39ee8d93218a79585113ef6b36f47c9ddf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2021
ms.locfileid: "51408622"
---
# <a name="devicetvmsoftwareinventory"></a><span data-ttu-id="f5df3-104">DeviceTvmSoftwareInventory</span><span class="sxs-lookup"><span data-stu-id="f5df3-104">DeviceTvmSoftwareInventory</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f5df3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f5df3-105">**Applies to:**</span></span>
- [<span data-ttu-id="f5df3-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f5df3-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)

><span data-ttu-id="f5df3-107">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="f5df3-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="f5df3-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f5df3-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/WindowsForBusiness/windows-atp?ocid=docs-wdatp-advancedhuntingref-abovefoldlink)

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="f5df3-109">Le tableau du schéma de recherche avancée contient l’inventaire de gestion des menaces et des vulnérabilités des logiciels actuellement installés sur les appareils de votre réseau, y compris les informations de fin `DeviceTvmSoftwareInventory` de support. [](next-gen-threat-and-vuln-mgt.md)</span><span class="sxs-lookup"><span data-stu-id="f5df3-109">The `DeviceTvmSoftwareInventory` table in the advanced hunting schema contains the [threat and vulnerability management](next-gen-threat-and-vuln-mgt.md) inventory of software currently installed on devices in your network, including end of support information.</span></span> <span data-ttu-id="f5df3-110">Vous pouvez, par exemple, chercher des événements impliquant des appareils qui sont installés avec une version logicielle actuellement vulnérable.</span><span class="sxs-lookup"><span data-stu-id="f5df3-110">You can, for instance, hunt for events involving devices that are installed with a currently vulnerable software version.</span></span> <span data-ttu-id="f5df3-111">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="f5df3-111">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="f5df3-112">DeviceTVMSoftwareInventory contient tous les logiciels dont la gestion des menaces et des vulnérabilités a pu correspondre à une CPE (Common Platform Enumeration), qu’elle soit vulnérable ou non.</span><span class="sxs-lookup"><span data-stu-id="f5df3-112">DeviceTVMSoftwareInventory contains all the software which threat and vulnerability management was able to match to a Common Platform Enumeration (CPE) – whether it is vulnerable or not.</span></span>

>[!NOTE]
><span data-ttu-id="f5df3-113">Les `DeviceTvmSoftwareInventory` `DeviceTvmSoftwareVulnerabilities` tableaux et les tables ont remplacé `DeviceTvmSoftwareInventoryVulnerabilities` le tableau.</span><span class="sxs-lookup"><span data-stu-id="f5df3-113">The `DeviceTvmSoftwareInventory` and `DeviceTvmSoftwareVulnerabilities` tables have replaced the `DeviceTvmSoftwareInventoryVulnerabilities` table.</span></span> <span data-ttu-id="f5df3-114">Ensemble, les deux premiers tableaux incluent d’autres colonnes que vous pouvez utiliser pour vous aider à informer vos activités de gestion des vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="f5df3-114">Together, the first two tables include more columns you can use to help inform your vulnerability management activities.</span></span>

<span data-ttu-id="f5df3-115">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference).</span><span class="sxs-lookup"><span data-stu-id="f5df3-115">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference).</span></span>

| <span data-ttu-id="f5df3-116">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="f5df3-116">Column name</span></span> | <span data-ttu-id="f5df3-117">Type de données</span><span class="sxs-lookup"><span data-stu-id="f5df3-117">Data type</span></span> | <span data-ttu-id="f5df3-118">Description</span><span class="sxs-lookup"><span data-stu-id="f5df3-118">Description</span></span> |
|-------------|-----------|-------------|
| `DeviceId` | <span data-ttu-id="f5df3-119">string</span><span class="sxs-lookup"><span data-stu-id="f5df3-119">string</span></span> | <span data-ttu-id="f5df3-120">Identificateur unique de l’appareil dans le service.</span><span class="sxs-lookup"><span data-stu-id="f5df3-120">Unique identifier for the device in the service.</span></span> |
| `DeviceName` | <span data-ttu-id="f5df3-121">string</span><span class="sxs-lookup"><span data-stu-id="f5df3-121">string</span></span> | <span data-ttu-id="f5df3-122">Nom de domaine complet (FQDN) de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f5df3-122">Fully qualified domain name (FQDN) of the device.</span></span> |
| `OSPlatform` | <span data-ttu-id="f5df3-123">string</span><span class="sxs-lookup"><span data-stu-id="f5df3-123">string</span></span> | <span data-ttu-id="f5df3-124">Plateforme du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f5df3-124">Platform of the operating system running on the device.</span></span> <span data-ttu-id="f5df3-125">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f5df3-125">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> |
| `OSVersion` | <span data-ttu-id="f5df3-126">string</span><span class="sxs-lookup"><span data-stu-id="f5df3-126">string</span></span> | <span data-ttu-id="f5df3-127">Version du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f5df3-127">Version of the operating system running on the device.</span></span> |
| `OSArchitecture` | <span data-ttu-id="f5df3-128">string</span><span class="sxs-lookup"><span data-stu-id="f5df3-128">string</span></span> | <span data-ttu-id="f5df3-129">Architecture du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f5df3-129">Architecture of the operating system running on the device.</span></span> |
| `SoftwareVendor` | <span data-ttu-id="f5df3-130">string</span><span class="sxs-lookup"><span data-stu-id="f5df3-130">string</span></span> | <span data-ttu-id="f5df3-131">Nom du fournisseur de logiciels.</span><span class="sxs-lookup"><span data-stu-id="f5df3-131">Name of the software vendor.</span></span> |
| `SoftwareName` | <span data-ttu-id="f5df3-132">string</span><span class="sxs-lookup"><span data-stu-id="f5df3-132">string</span></span> | <span data-ttu-id="f5df3-133">Nom du produit logiciel.</span><span class="sxs-lookup"><span data-stu-id="f5df3-133">Name of the software product.</span></span> |
| `SoftwareVersion` | <span data-ttu-id="f5df3-134">string</span><span class="sxs-lookup"><span data-stu-id="f5df3-134">string</span></span> | <span data-ttu-id="f5df3-135">Numéro de version du produit logiciel.</span><span class="sxs-lookup"><span data-stu-id="f5df3-135">Version number of the software product.</span></span> |
| `EndOfSupportStatus` | <span data-ttu-id="f5df3-136">string</span><span class="sxs-lookup"><span data-stu-id="f5df3-136">string</span></span> | <span data-ttu-id="f5df3-137">Indique l’étape de cycle de vie du produit logiciel par rapport à sa date de fin de prise en charge (EOS) ou de fin de vie (EOL) spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f5df3-137">Indicates the lifecycle stage of the software product relative to its specified end-of-support (EOS) or end-of-life (EOL) date.</span></span> |
| `EndOfSupportDate` | <span data-ttu-id="f5df3-138">string</span><span class="sxs-lookup"><span data-stu-id="f5df3-138">string</span></span> | <span data-ttu-id="f5df3-139">Date de fin de support (EOS) ou de fin de vie (EOL) du produit logiciel.</span><span class="sxs-lookup"><span data-stu-id="f5df3-139">End-of-support (EOS) or end-of-life (EOL) date of the software product.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="f5df3-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5df3-140">Related topics</span></span>

- [<span data-ttu-id="f5df3-141">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="f5df3-141">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="f5df3-142">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="f5df3-142">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="f5df3-143">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="f5df3-143">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
- [<span data-ttu-id="f5df3-144">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="f5df3-144">Overview of Threat & Vulnerability Management</span></span>](next-gen-threat-and-vuln-mgt.md)
