---
title: Table DeviceTvmSecureConfigurationAssessment dans le schéma de repérage avancé
description: Découvrez les événements d’évaluation de la sécurité dans la table DeviceTvmSecureConfigurationAssessment du schéma de recherche avancé. Ces événements de gestion & des vulnérabilités fournissent des informations sur l’appareil, ainsi que des informations sur la configuration de la sécurité, l’impact et la conformité.
keywords: advanced hunting, threat hunting, cyber threat hunting, Microsoft 365 Defender, microsoft 365, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, threat & vulnerability management, TVM, device management, security configuration, DeviceTvmSecureConfigurationAssessment
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
ms.openlocfilehash: 2e3e649911cb2ce63c2a49be0ebc93e35e8055d6
ms.sourcegitcommit: 72795ec56a7c4db863dcaaff5e9f7c41c653fda8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "52024216"
---
# <a name="devicetvmsecureconfigurationassessment"></a><span data-ttu-id="07a56-105">DeviceTvmSecureConfigurationAssessment</span><span class="sxs-lookup"><span data-stu-id="07a56-105">DeviceTvmSecureConfigurationAssessment</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="07a56-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="07a56-106">**Applies to:**</span></span>
- <span data-ttu-id="07a56-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="07a56-107">Microsoft 365 Defender</span></span>
- <span data-ttu-id="07a56-108">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="07a56-108">Microsoft Defender for Endpoint</span></span>



<span data-ttu-id="07a56-109">Chaque ligne du tableau `DeviceTvmSecureConfigurationAssessment` contient un événement d’évaluation pour une configuration de sécurité spécifique de [Gestion des menaces et des vulnérabilités](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span><span class="sxs-lookup"><span data-stu-id="07a56-109">Each row in the `DeviceTvmSecureConfigurationAssessment` table contains an assessment event for a specific security configuration from [Threat & Vulnerability Management](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span></span> <span data-ttu-id="07a56-110">Utilisez cette référence pour vérifier les derniers résultats de l’évaluation et déterminer si les appareils sont conformes.</span><span class="sxs-lookup"><span data-stu-id="07a56-110">Use this reference to check the latest assessment results and determine whether devices are compliant.</span></span>

<span data-ttu-id="07a56-111">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="07a56-111">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="07a56-112">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="07a56-112">Column name</span></span> | <span data-ttu-id="07a56-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="07a56-113">Data type</span></span> | <span data-ttu-id="07a56-114">Description</span><span class="sxs-lookup"><span data-stu-id="07a56-114">Description</span></span> |
|-------------|-----------|-------------|
| `DeviceId` | <span data-ttu-id="07a56-115">string</span><span class="sxs-lookup"><span data-stu-id="07a56-115">string</span></span> | <span data-ttu-id="07a56-116">Identificateur unique de l’appareil dans le service</span><span class="sxs-lookup"><span data-stu-id="07a56-116">Unique identifier for the device in the service</span></span> |
| `DeviceName` | <span data-ttu-id="07a56-117">string</span><span class="sxs-lookup"><span data-stu-id="07a56-117">string</span></span> | <span data-ttu-id="07a56-118">Nom de domaine complet (FQDN) de l’appareil</span><span class="sxs-lookup"><span data-stu-id="07a56-118">Fully qualified domain name (FQDN) of the device</span></span> |
| `OSPlatform` | <span data-ttu-id="07a56-119">string</span><span class="sxs-lookup"><span data-stu-id="07a56-119">string</span></span> | <span data-ttu-id="07a56-120">Plateforme du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="07a56-120">Platform of the operating system running on the device.</span></span> <span data-ttu-id="07a56-121">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="07a56-121">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span>|
| `Timestamp` | <span data-ttu-id="07a56-122">DateHeure</span><span class="sxs-lookup"><span data-stu-id="07a56-122">datetime</span></span> | <span data-ttu-id="07a56-123">Date et heure de génération de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="07a56-123">Date and time when the record was generated</span></span> |
| `ConfigurationId` | <span data-ttu-id="07a56-124">string</span><span class="sxs-lookup"><span data-stu-id="07a56-124">string</span></span> | <span data-ttu-id="07a56-125">Identificateur unique pour une configuration spécifique</span><span class="sxs-lookup"><span data-stu-id="07a56-125">Unique identifier for a specific configuration</span></span> |
| `ConfigurationCategory` | <span data-ttu-id="07a56-126">string</span><span class="sxs-lookup"><span data-stu-id="07a56-126">string</span></span> | <span data-ttu-id="07a56-127">Catégorie ou regroupement auquel appartient la configuration : application, système d’exploitation, réseau, comptes, contrôles de sécurité</span><span class="sxs-lookup"><span data-stu-id="07a56-127">Category or grouping to which the configuration belongs: Application, OS, Network, Accounts, Security controls</span></span> |
| `ConfigurationSubcategory` | <span data-ttu-id="07a56-128">string</span><span class="sxs-lookup"><span data-stu-id="07a56-128">string</span></span> | <span data-ttu-id="07a56-129">Sous-catégorie ou sous-groupement auquel appartient la configuration.</span><span class="sxs-lookup"><span data-stu-id="07a56-129">Subcategory or subgrouping to which the configuration belongs.</span></span> <span data-ttu-id="07a56-130">Dans de nombreux cas, cela décrit des capacités ou des fonctionnalités spécifiques.</span><span class="sxs-lookup"><span data-stu-id="07a56-130">In many cases, this describes specific capabilities or features.</span></span> |
| `ConfigurationImpact` | <span data-ttu-id="07a56-131">string</span><span class="sxs-lookup"><span data-stu-id="07a56-131">string</span></span> | <span data-ttu-id="07a56-132">Impact nominal de la configuration sur la note de configuration globale (1-10)</span><span class="sxs-lookup"><span data-stu-id="07a56-132">Rated impact of the configuration to the overall configuration score (1-10)</span></span> |
| `IsCompliant` | <span data-ttu-id="07a56-133">booléen</span><span class="sxs-lookup"><span data-stu-id="07a56-133">boolean</span></span> | <span data-ttu-id="07a56-134">Indique si la configuration ou la stratégie est correctement configurée.</span><span class="sxs-lookup"><span data-stu-id="07a56-134">Indicates whether the configuration or policy is properly configured</span></span> |
| `IsApplicable` | <span data-ttu-id="07a56-135">valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="07a56-135">boolean</span></span> | <span data-ttu-id="07a56-136">Indique si la configuration ou la stratégie s’applique à l’appareil</span><span class="sxs-lookup"><span data-stu-id="07a56-136">Indicates whether the configuration or policy applies to the device</span></span> |
| `Context` | <span data-ttu-id="07a56-137">string</span><span class="sxs-lookup"><span data-stu-id="07a56-137">string</span></span> | <span data-ttu-id="07a56-138">Informations contextuelles supplémentaires sur la configuration ou la stratégie</span><span class="sxs-lookup"><span data-stu-id="07a56-138">Additional contextual information about the configuration or policy</span></span> |
| `IsExpectedUserImpact` | <span data-ttu-id="07a56-139">valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="07a56-139">boolean</span></span> | <span data-ttu-id="07a56-140">Indique s’il y aura un impact sur l’utilisateur si la configuration ou la stratégie est appliquée</span><span class="sxs-lookup"><span data-stu-id="07a56-140">Indicates whether there will be user impact if the configuration or policy is applied</span></span> |

## <a name="related-topics"></a><span data-ttu-id="07a56-141">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="07a56-141">Related topics</span></span>

- [<span data-ttu-id="07a56-142">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="07a56-142">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="07a56-143">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="07a56-143">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="07a56-144">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="07a56-144">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="07a56-145">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="07a56-145">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="07a56-146">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="07a56-146">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="07a56-147">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="07a56-147">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="07a56-148">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="07a56-148">Overview of Threat & Vulnerability Management</span></span>](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)