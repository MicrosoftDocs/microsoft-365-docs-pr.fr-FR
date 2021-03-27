---
title: Table DeviceTvmSecureConfigurationAssessment dans le schéma de repérage avancé
description: Découvrez les événements d’évaluation de la sécurité dans la table DeviceTvmSecureConfigurationAssessment du schéma de recherche avancé. Ces événements de gestion & des vulnérabilités fournissent des informations sur l’appareil, ainsi que des détails sur la configuration de la sécurité, l’impact et les informations de conformité.
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, threat & vulnerability management, TVM, device management, security configuration, DeviceTvmSecureConfigurationAssessment
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: 3d991bc5e78fc7b33e20df1f86471a0969b7345f
ms.sourcegitcommit: ef98b8a18d275e5b5961e63d2b0743d046321737
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "51382594"
---
# <a name="devicetvmsecureconfigurationassessment"></a><span data-ttu-id="ef829-105">DeviceTvmSecureConfigurationAssessment</span><span class="sxs-lookup"><span data-stu-id="ef829-105">DeviceTvmSecureConfigurationAssessment</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="ef829-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ef829-106">**Applies to:**</span></span>
- <span data-ttu-id="ef829-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ef829-107">Microsoft 365 Defender</span></span>



<span data-ttu-id="ef829-108">Chaque ligne du tableau `DeviceTvmSecureConfigurationAssessment` contient un événement d’évaluation pour une configuration de sécurité spécifique de [Gestion des menaces et des vulnérabilités](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span><span class="sxs-lookup"><span data-stu-id="ef829-108">Each row in the `DeviceTvmSecureConfigurationAssessment` table contains an assessment event for a specific security configuration from [Threat & Vulnerability Management](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span></span> <span data-ttu-id="ef829-109">Utilisez cette référence pour vérifier les derniers résultats de l’évaluation et déterminer si les appareils sont conformes.</span><span class="sxs-lookup"><span data-stu-id="ef829-109">Use this reference to check the latest assessment results and determine whether devices are compliant.</span></span>

<span data-ttu-id="ef829-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ef829-110">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="ef829-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ef829-111">Column name</span></span> | <span data-ttu-id="ef829-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="ef829-112">Data type</span></span> | <span data-ttu-id="ef829-113">Description</span><span class="sxs-lookup"><span data-stu-id="ef829-113">Description</span></span> |
|-------------|-----------|-------------|
| `DeviceId` | <span data-ttu-id="ef829-114">string</span><span class="sxs-lookup"><span data-stu-id="ef829-114">string</span></span> | <span data-ttu-id="ef829-115">Identificateur unique de l’appareil dans le service</span><span class="sxs-lookup"><span data-stu-id="ef829-115">Unique identifier for the device in the service</span></span> |
| `DeviceName` | <span data-ttu-id="ef829-116">string</span><span class="sxs-lookup"><span data-stu-id="ef829-116">string</span></span> | <span data-ttu-id="ef829-117">Nom de domaine complet (FQDN) de l’appareil</span><span class="sxs-lookup"><span data-stu-id="ef829-117">Fully qualified domain name (FQDN) of the device</span></span> |
| `OSPlatform` | <span data-ttu-id="ef829-118">string</span><span class="sxs-lookup"><span data-stu-id="ef829-118">string</span></span> | <span data-ttu-id="ef829-119">Plateforme du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ef829-119">Platform of the operating system running on the device.</span></span> <span data-ttu-id="ef829-120">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ef829-120">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span>|
| `Timestamp` | <span data-ttu-id="ef829-121">DateHeure</span><span class="sxs-lookup"><span data-stu-id="ef829-121">datetime</span></span> | <span data-ttu-id="ef829-122">Date et heure de génération de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="ef829-122">Date and time when the record was generated</span></span> |
| `ConfigurationId` | <span data-ttu-id="ef829-123">string</span><span class="sxs-lookup"><span data-stu-id="ef829-123">string</span></span> | <span data-ttu-id="ef829-124">Identificateur unique pour une configuration spécifique</span><span class="sxs-lookup"><span data-stu-id="ef829-124">Unique identifier for a specific configuration</span></span> |
| `ConfigurationCategory` | <span data-ttu-id="ef829-125">string</span><span class="sxs-lookup"><span data-stu-id="ef829-125">string</span></span> | <span data-ttu-id="ef829-126">Catégorie ou regroupement auquel appartient la configuration : application, système d’exploitation, réseau, comptes, contrôles de sécurité</span><span class="sxs-lookup"><span data-stu-id="ef829-126">Category or grouping to which the configuration belongs: Application, OS, Network, Accounts, Security controls</span></span> |
| `ConfigurationSubcategory` | <span data-ttu-id="ef829-127">string</span><span class="sxs-lookup"><span data-stu-id="ef829-127">string</span></span> | <span data-ttu-id="ef829-128">Sous-catégorie ou sous-groupement auquel appartient la configuration.</span><span class="sxs-lookup"><span data-stu-id="ef829-128">Subcategory or subgrouping to which the configuration belongs.</span></span> <span data-ttu-id="ef829-129">Dans de nombreux cas, cela décrit des capacités ou des fonctionnalités spécifiques.</span><span class="sxs-lookup"><span data-stu-id="ef829-129">In many cases, this describes specific capabilities or features.</span></span> |
| `ConfigurationImpact` | <span data-ttu-id="ef829-130">string</span><span class="sxs-lookup"><span data-stu-id="ef829-130">string</span></span> | <span data-ttu-id="ef829-131">Impact nominal de la configuration sur la note de configuration globale (1-10)</span><span class="sxs-lookup"><span data-stu-id="ef829-131">Rated impact of the configuration to the overall configuration score (1-10)</span></span> |
| `IsCompliant` | <span data-ttu-id="ef829-132">booléen</span><span class="sxs-lookup"><span data-stu-id="ef829-132">boolean</span></span> | <span data-ttu-id="ef829-133">Indique si la configuration ou la stratégie est correctement configurée.</span><span class="sxs-lookup"><span data-stu-id="ef829-133">Indicates whether the configuration or policy is properly configured</span></span> |
| `IsApplicable` | <span data-ttu-id="ef829-134">booléen</span><span class="sxs-lookup"><span data-stu-id="ef829-134">boolean</span></span> | <span data-ttu-id="ef829-135">Indique si la configuration ou la stratégie s’applique à l’appareil</span><span class="sxs-lookup"><span data-stu-id="ef829-135">Indicates whether the configuration or policy applies to the device</span></span> |
| `Context` | <span data-ttu-id="ef829-136">string</span><span class="sxs-lookup"><span data-stu-id="ef829-136">string</span></span> | <span data-ttu-id="ef829-137">Informations contextuelles supplémentaires sur la configuration ou la stratégie</span><span class="sxs-lookup"><span data-stu-id="ef829-137">Additional contextual information about the configuration or policy</span></span> |
| `IsExpectedUserImpact` | <span data-ttu-id="ef829-138">booléen</span><span class="sxs-lookup"><span data-stu-id="ef829-138">boolean</span></span> | <span data-ttu-id="ef829-139">Indique s’il y aura un impact sur l’utilisateur si la configuration ou la stratégie est appliquée</span><span class="sxs-lookup"><span data-stu-id="ef829-139">Indicates whether there will be user impact if the configuration or policy is applied</span></span> |

## <a name="related-topics"></a><span data-ttu-id="ef829-140">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="ef829-140">Related topics</span></span>

- [<span data-ttu-id="ef829-141">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="ef829-141">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="ef829-142">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="ef829-142">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="ef829-143">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="ef829-143">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="ef829-144">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="ef829-144">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="ef829-145">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="ef829-145">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="ef829-146">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="ef829-146">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="ef829-147">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="ef829-147">Overview of Threat & Vulnerability Management</span></span>](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)