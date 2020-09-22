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
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: b186574cfc1307dfd8a01f7a77ef60bf91f4b162
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48196989"
---
# <a name="devicetvmsecureconfigurationassessment"></a><span data-ttu-id="19711-105">DeviceTvmSecureConfigurationAssessment</span><span class="sxs-lookup"><span data-stu-id="19711-105">DeviceTvmSecureConfigurationAssessment</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="19711-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="19711-106">**Applies to:**</span></span>
- <span data-ttu-id="19711-107">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="19711-107">Microsoft Threat Protection</span></span>



<span data-ttu-id="19711-108">Chaque ligne du tableau `DeviceTvmSecureConfigurationAssessment` contient un événement d’évaluation pour une configuration de sécurité spécifique de [Gestion des menaces et des vulnérabilités](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span><span class="sxs-lookup"><span data-stu-id="19711-108">Each row in the `DeviceTvmSecureConfigurationAssessment` table contains an assessment event for a specific security configuration from [Threat & Vulnerability Management](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span></span> <span data-ttu-id="19711-109">Utilisez cette référence pour vérifier les derniers résultats de l’évaluation et déterminer si les appareils sont conformes.</span><span class="sxs-lookup"><span data-stu-id="19711-109">Use this reference to check the latest assessment results and determine whether devices are compliant.</span></span>

<span data-ttu-id="19711-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="19711-110">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="19711-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="19711-111">Column name</span></span> | <span data-ttu-id="19711-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="19711-112">Data type</span></span> | <span data-ttu-id="19711-113">Description</span><span class="sxs-lookup"><span data-stu-id="19711-113">Description</span></span> |
|-------------|-----------|-------------|
| `DeviceId` | <span data-ttu-id="19711-114">string</span><span class="sxs-lookup"><span data-stu-id="19711-114">string</span></span> | <span data-ttu-id="19711-115">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="19711-115">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="19711-116">string</span><span class="sxs-lookup"><span data-stu-id="19711-116">string</span></span> | <span data-ttu-id="19711-117">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="19711-117">Fully qualified domain name (FQDN) of the machine</span></span> |
| `OSPlatform` | <span data-ttu-id="19711-118">string</span><span class="sxs-lookup"><span data-stu-id="19711-118">string</span></span> | <span data-ttu-id="19711-119">Plateforme du système d’exploitation client s’exécutant sur la machine.</span><span class="sxs-lookup"><span data-stu-id="19711-119">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="19711-120">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="19711-120">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span>|
| `Timestamp` | <span data-ttu-id="19711-121">DateHeure</span><span class="sxs-lookup"><span data-stu-id="19711-121">datetime</span></span> | <span data-ttu-id="19711-122">Date et heure de génération de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="19711-122">Date and time when the record was generated</span></span> |
| `ConfigurationId` | <span data-ttu-id="19711-123">string</span><span class="sxs-lookup"><span data-stu-id="19711-123">string</span></span> | <span data-ttu-id="19711-124">Identificateur unique pour une configuration spécifique</span><span class="sxs-lookup"><span data-stu-id="19711-124">Unique identifier for a specific configuration</span></span> |
| `ConfigurationCategory` | <span data-ttu-id="19711-125">string</span><span class="sxs-lookup"><span data-stu-id="19711-125">string</span></span> | <span data-ttu-id="19711-126">Catégorie ou regroupement auquel appartient la configuration : application, système d’exploitation, réseau, comptes, contrôles de sécurité</span><span class="sxs-lookup"><span data-stu-id="19711-126">Category or grouping to which the configuration belongs: Application, OS, Network, Accounts, Security controls</span></span> |
| `ConfigurationSubcategory` | <span data-ttu-id="19711-127">string</span><span class="sxs-lookup"><span data-stu-id="19711-127">string</span></span> | <span data-ttu-id="19711-128">Sous-catégorie ou sous-groupement auquel appartient la configuration.</span><span class="sxs-lookup"><span data-stu-id="19711-128">Subcategory or subgrouping to which the configuration belongs.</span></span> <span data-ttu-id="19711-129">Dans de nombreux cas, cela décrit des capacités ou des fonctionnalités spécifiques.</span><span class="sxs-lookup"><span data-stu-id="19711-129">In many cases, this describes specific capabilities or features.</span></span> |
| `ConfigurationImpact` | <span data-ttu-id="19711-130">string</span><span class="sxs-lookup"><span data-stu-id="19711-130">string</span></span> | <span data-ttu-id="19711-131">Impact nominal de la configuration sur la note de configuration globale (1-10)</span><span class="sxs-lookup"><span data-stu-id="19711-131">Rated impact of the configuration to the overall configuration score (1-10)</span></span> |
| `IsCompliant` | <span data-ttu-id="19711-132">booléen</span><span class="sxs-lookup"><span data-stu-id="19711-132">boolean</span></span> | <span data-ttu-id="19711-133">Indique si la configuration ou la stratégie est correctement configurée.</span><span class="sxs-lookup"><span data-stu-id="19711-133">Indicates whether the configuration or policy is properly configured</span></span> |

## <a name="related-topics"></a><span data-ttu-id="19711-134">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="19711-134">Related topics</span></span>

- [<span data-ttu-id="19711-135">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="19711-135">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="19711-136">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="19711-136">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="19711-137">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="19711-137">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="19711-138">Rechercher sur les appareils, les emails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="19711-138">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="19711-139">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="19711-139">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="19711-140">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="19711-140">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="19711-141">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="19711-141">Overview of Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)
