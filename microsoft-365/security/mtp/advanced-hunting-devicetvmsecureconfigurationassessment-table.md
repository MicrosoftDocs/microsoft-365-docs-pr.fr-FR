---
title: Table DeviceTvmSecureConfigurationAssessment dans le schéma de repérage avancé
description: Découvrez les événements d’évaluation de la sécurité de Gestion des menaces et des vulnérabilités dans la table DeviceTvmSecureConfigurationAssessment du schéma de repérage avancé. Ces événements fournissent des informations sur la machine, ainsi que sur la configuration de la sécurité, l’impact et la conformité.
keywords: chasse de menace, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, table, colonne, type de données, description, menace & gestion des vulnérabilités, TVM, gestion des appareils, configuration de la sécurité, DeviceTvmSecureConfigurationAssessment
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365-initiative-m365-defender
ms.topic: article
ms.openlocfilehash: f25c0ad47a520ec23a94775b64a4f1ecc2eb9486
ms.sourcegitcommit: 5e1b8c959a081022826fb09358730096248507ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48414249"
---
# <a name="devicetvmsecureconfigurationassessment"></a><span data-ttu-id="78e92-105">DeviceTvmSecureConfigurationAssessment</span><span class="sxs-lookup"><span data-stu-id="78e92-105">DeviceTvmSecureConfigurationAssessment</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="78e92-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="78e92-106">**Applies to:**</span></span>
- <span data-ttu-id="78e92-107">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="78e92-107">Microsoft Threat Protection</span></span>



<span data-ttu-id="78e92-108">Chaque ligne du tableau `DeviceTvmSecureConfigurationAssessment` contient un événement d’évaluation pour une configuration de sécurité spécifique de [Gestion des menaces et des vulnérabilités](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span><span class="sxs-lookup"><span data-stu-id="78e92-108">Each row in the `DeviceTvmSecureConfigurationAssessment` table contains an assessment event for a specific security configuration from [Threat & Vulnerability Management](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span></span> <span data-ttu-id="78e92-109">Utilisez cette référence pour vérifier les derniers résultats de l’évaluation et déterminer si les appareils sont conformes.</span><span class="sxs-lookup"><span data-stu-id="78e92-109">Use this reference to check the latest assessment results and determine whether devices are compliant.</span></span>

<span data-ttu-id="78e92-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="78e92-110">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="78e92-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="78e92-111">Column name</span></span> | <span data-ttu-id="78e92-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="78e92-112">Data type</span></span> | <span data-ttu-id="78e92-113">Description</span><span class="sxs-lookup"><span data-stu-id="78e92-113">Description</span></span> |
|-------------|-----------|-------------|
| `DeviceId` | <span data-ttu-id="78e92-114">string</span><span class="sxs-lookup"><span data-stu-id="78e92-114">string</span></span> | <span data-ttu-id="78e92-115">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="78e92-115">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="78e92-116">string</span><span class="sxs-lookup"><span data-stu-id="78e92-116">string</span></span> | <span data-ttu-id="78e92-117">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="78e92-117">Fully qualified domain name (FQDN) of the machine</span></span> |
| `OSPlatform` | <span data-ttu-id="78e92-118">string</span><span class="sxs-lookup"><span data-stu-id="78e92-118">string</span></span> | <span data-ttu-id="78e92-119">Plateforme du système d’exploitation client s’exécutant sur la machine.</span><span class="sxs-lookup"><span data-stu-id="78e92-119">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="78e92-120">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="78e92-120">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span>|
| `Timestamp` | <span data-ttu-id="78e92-121">DateHeure</span><span class="sxs-lookup"><span data-stu-id="78e92-121">datetime</span></span> | <span data-ttu-id="78e92-122">Date et heure de génération de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="78e92-122">Date and time when the record was generated</span></span> |
| `ConfigurationId` | <span data-ttu-id="78e92-123">string</span><span class="sxs-lookup"><span data-stu-id="78e92-123">string</span></span> | <span data-ttu-id="78e92-124">Identificateur unique pour une configuration spécifique</span><span class="sxs-lookup"><span data-stu-id="78e92-124">Unique identifier for a specific configuration</span></span> |
| `ConfigurationCategory` | <span data-ttu-id="78e92-125">string</span><span class="sxs-lookup"><span data-stu-id="78e92-125">string</span></span> | <span data-ttu-id="78e92-126">Catégorie ou regroupement auquel appartient la configuration : application, système d’exploitation, réseau, comptes, contrôles de sécurité</span><span class="sxs-lookup"><span data-stu-id="78e92-126">Category or grouping to which the configuration belongs: Application, OS, Network, Accounts, Security controls</span></span> |
| `ConfigurationSubcategory` | <span data-ttu-id="78e92-127">string</span><span class="sxs-lookup"><span data-stu-id="78e92-127">string</span></span> | <span data-ttu-id="78e92-128">Sous-catégorie ou sous-groupement auquel appartient la configuration.</span><span class="sxs-lookup"><span data-stu-id="78e92-128">Subcategory or subgrouping to which the configuration belongs.</span></span> <span data-ttu-id="78e92-129">Dans de nombreux cas, cela décrit des capacités ou des fonctionnalités spécifiques.</span><span class="sxs-lookup"><span data-stu-id="78e92-129">In many cases, this describes specific capabilities or features.</span></span> |
| `ConfigurationImpact` | <span data-ttu-id="78e92-130">string</span><span class="sxs-lookup"><span data-stu-id="78e92-130">string</span></span> | <span data-ttu-id="78e92-131">Impact nominal de la configuration sur la note de configuration globale (1-10)</span><span class="sxs-lookup"><span data-stu-id="78e92-131">Rated impact of the configuration to the overall configuration score (1-10)</span></span> |
| `IsCompliant` | <span data-ttu-id="78e92-132">booléen</span><span class="sxs-lookup"><span data-stu-id="78e92-132">boolean</span></span> | <span data-ttu-id="78e92-133">Indique si la configuration ou la stratégie est correctement configurée.</span><span class="sxs-lookup"><span data-stu-id="78e92-133">Indicates whether the configuration or policy is properly configured</span></span> |

## <a name="related-topics"></a><span data-ttu-id="78e92-134">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="78e92-134">Related topics</span></span>

- [<span data-ttu-id="78e92-135">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="78e92-135">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="78e92-136">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="78e92-136">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="78e92-137">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="78e92-137">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="78e92-138">Rechercher sur les appareils, les emails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="78e92-138">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="78e92-139">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="78e92-139">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="78e92-140">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="78e92-140">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="78e92-141">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="78e92-141">Overview of Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)
