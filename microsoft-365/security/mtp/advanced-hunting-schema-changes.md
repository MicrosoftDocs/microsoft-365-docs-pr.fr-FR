---
title: Changements d’appellation dans le schéma de recherche avancée Microsoft 365 Defender
description: Suivre et passer en revue les tables et colonnes de modifications d’attribution de noms dans le schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, data, naming changes, rename, Microsoft Threat Protection
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
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: 3f03543b03dca5fe426700ffff4f5c6edb8fa3c7
ms.sourcegitcommit: c550c1b5b9e67398fd95bfb0256c4f5c7930b2be
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/01/2021
ms.locfileid: "50066868"
---
# <a name="advanced-hunting-schema---naming-changes"></a><span data-ttu-id="9cf88-104">Schéma de recherche avancé : modifications d’attribution de noms</span><span class="sxs-lookup"><span data-stu-id="9cf88-104">Advanced hunting schema - Naming changes</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="9cf88-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9cf88-105">**Applies to:**</span></span>
- <span data-ttu-id="9cf88-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9cf88-106">Microsoft 365 Defender</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="9cf88-107">Le [schéma de recherche avancée est mis à jour](advanced-hunting-schema-tables.md) régulièrement pour ajouter de nouvelles tables et colonnes.</span><span class="sxs-lookup"><span data-stu-id="9cf88-107">The [advanced hunting schema](advanced-hunting-schema-tables.md) is updated regularly to add new tables and columns.</span></span> <span data-ttu-id="9cf88-108">Dans certains cas, les noms des colonnes existantes sont renommés ou remplacés pour améliorer l’expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9cf88-108">In some cases, existing columns names are renamed or replaced to improve the user experience.</span></span> <span data-ttu-id="9cf88-109">Reportez-vous à cet article pour passer en revue les modifications d’attribution de noms qui peuvent avoir un impact sur vos requêtes.</span><span class="sxs-lookup"><span data-stu-id="9cf88-109">Refer to this article to review naming changes that could impact your queries.</span></span>

<span data-ttu-id="9cf88-110">Les modifications d’attribution de noms sont automatiquement appliquées aux requêtes enregistrées dans le centre de sécurité, y compris les requêtes utilisées par les règles de détection personnalisées.</span><span class="sxs-lookup"><span data-stu-id="9cf88-110">Naming changes are automatically applied to queries that are saved in the security center, including queries used by custom detection rules.</span></span> <span data-ttu-id="9cf88-111">Vous n’avez pas besoin de mettre à jour ces requêtes manuellement.</span><span class="sxs-lookup"><span data-stu-id="9cf88-111">You don't need to update these queries manually.</span></span> <span data-ttu-id="9cf88-112">Toutefois, vous devrez mettre à jour les requêtes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9cf88-112">However, you will need to update the following queries:</span></span>
- <span data-ttu-id="9cf88-113">Requêtes qui sont exécutés à l’aide de l’API</span><span class="sxs-lookup"><span data-stu-id="9cf88-113">Queries that are run using the API</span></span>
- <span data-ttu-id="9cf88-114">Requêtes enregistrées ailleurs en dehors du centre de sécurité</span><span class="sxs-lookup"><span data-stu-id="9cf88-114">Queries that are saved elsewhere outside the security center</span></span>

## <a name="december-2020"></a><span data-ttu-id="9cf88-115">Décembre 2020</span><span class="sxs-lookup"><span data-stu-id="9cf88-115">December 2020</span></span>

| <span data-ttu-id="9cf88-116">Nom du tableau</span><span class="sxs-lookup"><span data-stu-id="9cf88-116">Table name</span></span> | <span data-ttu-id="9cf88-117">Nom de colonne d’origine</span><span class="sxs-lookup"><span data-stu-id="9cf88-117">Original column name</span></span> | <span data-ttu-id="9cf88-118">Nouveau nom de colonne</span><span class="sxs-lookup"><span data-stu-id="9cf88-118">New column name</span></span> | <span data-ttu-id="9cf88-119">Raison du changement</span><span class="sxs-lookup"><span data-stu-id="9cf88-119">Reason for change</span></span>
|--|--|--|--|
| [<span data-ttu-id="9cf88-120">EmailEvents</span><span class="sxs-lookup"><span data-stu-id="9cf88-120">EmailEvents</span></span>](advanced-hunting-emailevents-table.md) | `FinalEmailAction` | `EmailAction` | <span data-ttu-id="9cf88-121">Commentaires des clients.</span><span class="sxs-lookup"><span data-stu-id="9cf88-121">Customer feedback</span></span> |
| [<span data-ttu-id="9cf88-122">EmailEvents</span><span class="sxs-lookup"><span data-stu-id="9cf88-122">EmailEvents</span></span>](advanced-hunting-emailevents-table.md) | `FinalEmailActionPolicy` | `EmailActionPolicy` | <span data-ttu-id="9cf88-123">Commentaires des clients.</span><span class="sxs-lookup"><span data-stu-id="9cf88-123">Customer feedback</span></span> |
| [<span data-ttu-id="9cf88-124">EmailEvents</span><span class="sxs-lookup"><span data-stu-id="9cf88-124">EmailEvents</span></span>](advanced-hunting-emailevents-table.md) | `FinalEmailActionPolicyGuid` | `EmailActionPolicyGuid` | <span data-ttu-id="9cf88-125">Commentaires des clients.</span><span class="sxs-lookup"><span data-stu-id="9cf88-125">Customer feedback</span></span> |

## <a name="january-2021"></a><span data-ttu-id="9cf88-126">Janvier 2021</span><span class="sxs-lookup"><span data-stu-id="9cf88-126">January 2021</span></span>

| <span data-ttu-id="9cf88-127">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="9cf88-127">Column name</span></span> | <span data-ttu-id="9cf88-128">Nom de la valeur d’origine</span><span class="sxs-lookup"><span data-stu-id="9cf88-128">Original value name</span></span> | <span data-ttu-id="9cf88-129">Nouveau nom de valeur</span><span class="sxs-lookup"><span data-stu-id="9cf88-129">New value name</span></span> | <span data-ttu-id="9cf88-130">Raison du changement</span><span class="sxs-lookup"><span data-stu-id="9cf88-130">Reason for change</span></span>
|--|--|--|--|
| `DetectionSource` | <span data-ttu-id="9cf88-131">MCAS</span><span class="sxs-lookup"><span data-stu-id="9cf88-131">MCAS</span></span> |    <span data-ttu-id="9cf88-132">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="9cf88-132">Microsoft Cloud App Security</span></span> | <span data-ttu-id="9cf88-133">Changement de nom</span><span class="sxs-lookup"><span data-stu-id="9cf88-133">Rebranding</span></span> |
| `DetectionSource` | <span data-ttu-id="9cf88-134">WindowsDefenderAtp</span><span class="sxs-lookup"><span data-stu-id="9cf88-134">WindowsDefenderAtp</span></span>|   <span data-ttu-id="9cf88-135">EDR</span><span class="sxs-lookup"><span data-stu-id="9cf88-135">EDR</span></span>| <span data-ttu-id="9cf88-136">Changement de nom</span><span class="sxs-lookup"><span data-stu-id="9cf88-136">Rebranding</span></span> |
| `DetectionSource` | <span data-ttu-id="9cf88-137">WindowsDefenderAv</span><span class="sxs-lookup"><span data-stu-id="9cf88-137">WindowsDefenderAv</span></span> | <span data-ttu-id="9cf88-138">Antivirus</span><span class="sxs-lookup"><span data-stu-id="9cf88-138">Antivirus</span></span> | <span data-ttu-id="9cf88-139">Changement de nom</span><span class="sxs-lookup"><span data-stu-id="9cf88-139">Rebranding</span></span> |
| `DetectionSource` | <span data-ttu-id="9cf88-140">WindowsDefenderSmartScreen</span><span class="sxs-lookup"><span data-stu-id="9cf88-140">WindowsDefenderSmartScreen</span></span> |  <span data-ttu-id="9cf88-141">SmartScreen</span><span class="sxs-lookup"><span data-stu-id="9cf88-141">SmartScreen</span></span> | <span data-ttu-id="9cf88-142">Changement de nom</span><span class="sxs-lookup"><span data-stu-id="9cf88-142">Rebranding</span></span> |
| `DetectionSource` | <span data-ttu-id="9cf88-143">CustomerTI</span><span class="sxs-lookup"><span data-stu-id="9cf88-143">CustomerTI</span></span> |  <span data-ttu-id="9cf88-144">Ti personnalisée</span><span class="sxs-lookup"><span data-stu-id="9cf88-144">Custom TI</span></span> | <span data-ttu-id="9cf88-145">Changement de nom</span><span class="sxs-lookup"><span data-stu-id="9cf88-145">Rebranding</span></span> |
| `DetectionSource` | <span data-ttu-id="9cf88-146">OfficeATP</span><span class="sxs-lookup"><span data-stu-id="9cf88-146">OfficeATP</span></span> | <span data-ttu-id="9cf88-147">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="9cf88-147">Microsoft Defender for Office 365</span></span> | <span data-ttu-id="9cf88-148">Changement de nom</span><span class="sxs-lookup"><span data-stu-id="9cf88-148">Rebranding</span></span> |
| `DetectionSource` | <span data-ttu-id="9cf88-149">MTP</span><span class="sxs-lookup"><span data-stu-id="9cf88-149">MTP</span></span>   | <span data-ttu-id="9cf88-150">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9cf88-150">Microsoft 365 Defender</span></span> | <span data-ttu-id="9cf88-151">Changement de nom</span><span class="sxs-lookup"><span data-stu-id="9cf88-151">Rebranding</span></span> |
| `DetectionSource` | <span data-ttu-id="9cf88-152">AzureATP</span><span class="sxs-lookup"><span data-stu-id="9cf88-152">AzureATP</span></span> |    <span data-ttu-id="9cf88-153">Microsoft Defender pour Identity</span><span class="sxs-lookup"><span data-stu-id="9cf88-153">Microsoft Defender for Identity</span></span> | <span data-ttu-id="9cf88-154">Changement de nom</span><span class="sxs-lookup"><span data-stu-id="9cf88-154">Rebranding</span></span> |
| `DetectionSource` | <span data-ttu-id="9cf88-155">CustomDetection</span><span class="sxs-lookup"><span data-stu-id="9cf88-155">CustomDetection</span></span>   | <span data-ttu-id="9cf88-156">Détection personnalisée</span><span class="sxs-lookup"><span data-stu-id="9cf88-156">Custom detection</span></span> | <span data-ttu-id="9cf88-157">Changement de nom</span><span class="sxs-lookup"><span data-stu-id="9cf88-157">Rebranding</span></span> |
| `DetectionSource` | <span data-ttu-id="9cf88-158">AutomatedIgoigation</span><span class="sxs-lookup"><span data-stu-id="9cf88-158">AutomatedInvestigation</span></span> |<span data-ttu-id="9cf88-159">Examen automatisé</span><span class="sxs-lookup"><span data-stu-id="9cf88-159">Automated investigation</span></span> | <span data-ttu-id="9cf88-160">Changement de nom</span><span class="sxs-lookup"><span data-stu-id="9cf88-160">Rebranding</span></span> |
| `DetectionSource` | <span data-ttu-id="9cf88-161">ThreatExperts</span><span class="sxs-lookup"><span data-stu-id="9cf88-161">ThreatExperts</span></span> | <span data-ttu-id="9cf88-162">Spécialistes des menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="9cf88-162">Microsoft Threat Experts</span></span> | <span data-ttu-id="9cf88-163">Changement de nom</span><span class="sxs-lookup"><span data-stu-id="9cf88-163">Rebranding</span></span> |
| `DetectionSource` | <span data-ttu-id="9cf88-164">Ti tiers</span><span class="sxs-lookup"><span data-stu-id="9cf88-164">3rd party TI</span></span> | <span data-ttu-id="9cf88-165">Capteurs tiers</span><span class="sxs-lookup"><span data-stu-id="9cf88-165">3rd Party sensors</span></span> | <span data-ttu-id="9cf88-166">Changement de nom</span><span class="sxs-lookup"><span data-stu-id="9cf88-166">Rebranding</span></span> |
| `ServiceSource` | <span data-ttu-id="9cf88-167">Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="9cf88-167">Microsoft Defender ATP</span></span>| <span data-ttu-id="9cf88-168">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9cf88-168">Microsoft Defender for Endpoint</span></span> | <span data-ttu-id="9cf88-169">Changement de nom</span><span class="sxs-lookup"><span data-stu-id="9cf88-169">Rebranding</span></span> |
|`ServiceSource` |<span data-ttu-id="9cf88-170">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="9cf88-170">Microsoft Threat Protection</span></span>   | <span data-ttu-id="9cf88-171">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9cf88-171">Microsoft 365 Defender</span></span> | <span data-ttu-id="9cf88-172">Changement de nom</span><span class="sxs-lookup"><span data-stu-id="9cf88-172">Rebranding</span></span> |
| `ServiceSource` | <span data-ttu-id="9cf88-173">Office 365 – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="9cf88-173">Office 365 ATP</span></span>  |<span data-ttu-id="9cf88-174">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="9cf88-174">Microsoft Defender for Office 365</span></span> | <span data-ttu-id="9cf88-175">Changement de nom</span><span class="sxs-lookup"><span data-stu-id="9cf88-175">Rebranding</span></span> |
| `ServiceSource` |<span data-ttu-id="9cf88-176">Azure ATP</span><span class="sxs-lookup"><span data-stu-id="9cf88-176">Azure ATP</span></span>    |<span data-ttu-id="9cf88-177">Microsoft Defender pour Identity</span><span class="sxs-lookup"><span data-stu-id="9cf88-177">Microsoft Defender for Identity</span></span> | <span data-ttu-id="9cf88-178">Changement de nom</span><span class="sxs-lookup"><span data-stu-id="9cf88-178">Rebranding</span></span> |

<span data-ttu-id="9cf88-179">`DetectionSource`est disponible dans la table [AlertInfo.](advanced-hunting-alertinfo-table.md)</span><span class="sxs-lookup"><span data-stu-id="9cf88-179">`DetectionSource` is available in the [AlertInfo](advanced-hunting-alertinfo-table.md) table.</span></span> <span data-ttu-id="9cf88-180">`ServiceSource`est disponible dans les tables [AlertEvidence](advanced-hunting-alertevidence-table.md) et [AlertInfo.](advanced-hunting-alertinfo-table.md)</span><span class="sxs-lookup"><span data-stu-id="9cf88-180">`ServiceSource` is available in the [AlertEvidence](advanced-hunting-alertevidence-table.md) and [AlertInfo](advanced-hunting-alertinfo-table.md) tables.</span></span> 
## <a name="related-topics"></a><span data-ttu-id="9cf88-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cf88-181">Related topics</span></span>
- [<span data-ttu-id="9cf88-182">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="9cf88-182">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="9cf88-183">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="9cf88-183">Understand the schema</span></span>](advanced-hunting-schema-tables.md)