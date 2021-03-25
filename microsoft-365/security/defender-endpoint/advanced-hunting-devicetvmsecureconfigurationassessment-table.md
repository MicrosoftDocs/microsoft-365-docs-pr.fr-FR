---
title: Table DeviceTvmSecureConfigurationAssessment dans le schéma de repérage avancé
description: Découvrez les événements d’évaluation de la sécurité & gestion des menaces dans la table DeviceTvmSecureConfigurationAssessment du schéma de recherche avancée. Ces événements fournissent des informations sur l’appareil, ainsi que des informations sur la configuration de la sécurité, l’impact et la conformité.
keywords: advanced hunting, threat hunting, cyber threat hunting, mdatp, microsoft defender atp, wdatp search, query, telemetry, schema reference, kusto, table, column, data type, description, threat & vulnerability management, TVM, device management, security configuration, DeviceTvmSecureConfigurationAssessment
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
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
ms.technology: mde
ms.openlocfilehash: 1be5d911d1a2d21abdadce5745151a2778361672
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51067009"
---
# <a name="devicetvmsecureconfigurationassessment"></a><span data-ttu-id="ced7b-105">DeviceTvmSecureConfigurationAssessment</span><span class="sxs-lookup"><span data-stu-id="ced7b-105">DeviceTvmSecureConfigurationAssessment</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="ced7b-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ced7b-106">**Applies to:**</span></span>
- [<span data-ttu-id="ced7b-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ced7b-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)



><span data-ttu-id="ced7b-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="ced7b-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="ced7b-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ced7b-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/WindowsForBusiness/windows-atp?ocid=docs-wdatp-advancedhuntingref-abovefoldlink)

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="ced7b-110">Chaque ligne du tableau `DeviceTvmSecureConfigurationAssessment` contient un événement d’évaluation pour une configuration de sécurité spécifique de [Gestion des menaces et des vulnérabilités](next-gen-threat-and-vuln-mgt.md).</span><span class="sxs-lookup"><span data-stu-id="ced7b-110">Each row in the `DeviceTvmSecureConfigurationAssessment` table contains an assessment event for a specific security configuration from [Threat & Vulnerability Management](next-gen-threat-and-vuln-mgt.md).</span></span> <span data-ttu-id="ced7b-111">Utilisez cette référence pour vérifier les derniers résultats de l’évaluation et déterminer si les appareils sont conformes.</span><span class="sxs-lookup"><span data-stu-id="ced7b-111">Use this reference to check the latest assessment results and determine whether devices are compliant.</span></span>

<span data-ttu-id="ced7b-112">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference).</span><span class="sxs-lookup"><span data-stu-id="ced7b-112">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference).</span></span>

| <span data-ttu-id="ced7b-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ced7b-113">Column name</span></span> | <span data-ttu-id="ced7b-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="ced7b-114">Data type</span></span> | <span data-ttu-id="ced7b-115">Description</span><span class="sxs-lookup"><span data-stu-id="ced7b-115">Description</span></span> |
|-------------|-----------|-------------|
| `DeviceId` | <span data-ttu-id="ced7b-116">string</span><span class="sxs-lookup"><span data-stu-id="ced7b-116">string</span></span> | <span data-ttu-id="ced7b-117">Identificateur unique de l’appareil dans le service</span><span class="sxs-lookup"><span data-stu-id="ced7b-117">Unique identifier for the device in the service</span></span> |
| `DeviceName` | <span data-ttu-id="ced7b-118">string</span><span class="sxs-lookup"><span data-stu-id="ced7b-118">string</span></span> | <span data-ttu-id="ced7b-119">Nom de domaine complet (FQDN) de l’appareil</span><span class="sxs-lookup"><span data-stu-id="ced7b-119">Fully qualified domain name (FQDN) of the device</span></span> |
| `OSPlatform` | <span data-ttu-id="ced7b-120">string</span><span class="sxs-lookup"><span data-stu-id="ced7b-120">string</span></span> | <span data-ttu-id="ced7b-121">Plateforme du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ced7b-121">Platform of the operating system running on the device.</span></span> <span data-ttu-id="ced7b-122">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ced7b-122">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span>|
| `Timestamp` | <span data-ttu-id="ced7b-123">DateHeure</span><span class="sxs-lookup"><span data-stu-id="ced7b-123">datetime</span></span> |<span data-ttu-id="ced7b-124">Date et heure de génération de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="ced7b-124">Date and time when the record was generated</span></span> |
| `ConfigurationId` | <span data-ttu-id="ced7b-125">string</span><span class="sxs-lookup"><span data-stu-id="ced7b-125">string</span></span> | <span data-ttu-id="ced7b-126">Identificateur unique pour une configuration spécifique</span><span class="sxs-lookup"><span data-stu-id="ced7b-126">Unique identifier for a specific configuration</span></span> |
| `ConfigurationCategory` | <span data-ttu-id="ced7b-127">string</span><span class="sxs-lookup"><span data-stu-id="ced7b-127">string</span></span> | <span data-ttu-id="ced7b-128">Catégorie ou regroupement auquel appartient la configuration : application, système d’exploitation, réseau, comptes, contrôles de sécurité</span><span class="sxs-lookup"><span data-stu-id="ced7b-128">Category or grouping to which the configuration belongs: Application, OS, Network, Accounts, Security controls</span></span> |
| `ConfigurationSubcategory` | <span data-ttu-id="ced7b-129">string</span><span class="sxs-lookup"><span data-stu-id="ced7b-129">string</span></span> |<span data-ttu-id="ced7b-130">Sous-catégorie ou sous-groupement auquel appartient la configuration.</span><span class="sxs-lookup"><span data-stu-id="ced7b-130">Subcategory or subgrouping to which the configuration belongs.</span></span> <span data-ttu-id="ced7b-131">Dans de nombreux cas, cela décrit des capacités ou des fonctionnalités spécifiques.</span><span class="sxs-lookup"><span data-stu-id="ced7b-131">In many cases, this describes specific capabilities or features.</span></span> |
| `ConfigurationImpact` | <span data-ttu-id="ced7b-132">string</span><span class="sxs-lookup"><span data-stu-id="ced7b-132">string</span></span> | <span data-ttu-id="ced7b-133">Impact nominal de la configuration sur la note de configuration globale (1-10)</span><span class="sxs-lookup"><span data-stu-id="ced7b-133">Rated impact of the configuration to the overall configuration score (1-10)</span></span> |
| `IsCompliant` | <span data-ttu-id="ced7b-134">booléen</span><span class="sxs-lookup"><span data-stu-id="ced7b-134">boolean</span></span> | <span data-ttu-id="ced7b-135">Indique si la configuration ou la stratégie est correctement configurée.</span><span class="sxs-lookup"><span data-stu-id="ced7b-135">Indicates whether the configuration or policy is properly configured</span></span> |
| `IsApplicable` | <span data-ttu-id="ced7b-136">booléen</span><span class="sxs-lookup"><span data-stu-id="ced7b-136">boolean</span></span> | <span data-ttu-id="ced7b-137">Indique si la configuration ou la stratégie s’applique à l’appareil</span><span class="sxs-lookup"><span data-stu-id="ced7b-137">Indicates whether the configuration or policy applies to the device</span></span> |
| `Context` | <span data-ttu-id="ced7b-138">string</span><span class="sxs-lookup"><span data-stu-id="ced7b-138">string</span></span> | <span data-ttu-id="ced7b-139">Informations contextuelles supplémentaires sur la configuration ou la stratégie</span><span class="sxs-lookup"><span data-stu-id="ced7b-139">Additional contextual information about the configuration or policy</span></span> |
| `IsExpectedUserImpactCompliant` | <span data-ttu-id="ced7b-140">booléen</span><span class="sxs-lookup"><span data-stu-id="ced7b-140">boolean</span></span> | <span data-ttu-id="ced7b-141">Indique s’il y aura un impact sur l’utilisateur si la configuration ou la stratégie est appliquée</span><span class="sxs-lookup"><span data-stu-id="ced7b-141">Indicates whether there will be user impact if the configuration or policy is applied</span></span> |

## <a name="related-topics"></a><span data-ttu-id="ced7b-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ced7b-142">Related topics</span></span>

- [<span data-ttu-id="ced7b-143">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="ced7b-143">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="ced7b-144">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="ced7b-144">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="ced7b-145">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="ced7b-145">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
- [<span data-ttu-id="ced7b-146">Présentation de la fonction Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="ced7b-146">Overview of Threat & Vulnerability Management</span></span>](next-gen-threat-and-vuln-mgt.md)