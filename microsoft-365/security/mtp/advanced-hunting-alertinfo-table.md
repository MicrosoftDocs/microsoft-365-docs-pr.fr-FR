---
title: Table AlertInfo dans le schéma de recherche avancé
description: En savoir plus sur les événements de génération d’alertes dans la table AlertInfo du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, AlertInfo, alert, severity, category, MITRE, ATT&CK, Microsoft Defender ATP, MDATP, Office 365 ATP, Microsoft Cloud App Security, MCAS et Azure ATP
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
ms.openlocfilehash: ac1e28987a944a8f7786af4f10a85362f2f92a80
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49929969"
---
# <a name="alertinfo"></a><span data-ttu-id="60ff7-104">AlertInfo</span><span class="sxs-lookup"><span data-stu-id="60ff7-104">AlertInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="60ff7-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="60ff7-105">**Applies to:**</span></span>
- <span data-ttu-id="60ff7-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="60ff7-106">Microsoft 365 Defender</span></span>



<span data-ttu-id="60ff7-107">Le tableau du schéma de recherche avancée contient des informations sur les alertes de Microsoft Defender pour `AlertInfo` Endpoint, Microsoft Defender pour Office 365, Microsoft Cloud App Security et Microsoft Defender pour l’identité. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="60ff7-107">The `AlertInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about alerts from Microsoft  Defender for Endpoint, Microsoft Defender for Office 365, Microsoft Cloud App Security, and Microsoft Defender for Identity.</span></span> <span data-ttu-id="60ff7-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="60ff7-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="60ff7-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="60ff7-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="60ff7-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="60ff7-110">Column name</span></span> | <span data-ttu-id="60ff7-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="60ff7-111">Data type</span></span> | <span data-ttu-id="60ff7-112">Description</span><span class="sxs-lookup"><span data-stu-id="60ff7-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="60ff7-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="60ff7-113">datetime</span></span> | <span data-ttu-id="60ff7-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="60ff7-114">Date and time when the event was recorded</span></span> |
| `AlertId` | <span data-ttu-id="60ff7-115">string</span><span class="sxs-lookup"><span data-stu-id="60ff7-115">string</span></span> | <span data-ttu-id="60ff7-116">Identificateur unique de l’alerte</span><span class="sxs-lookup"><span data-stu-id="60ff7-116">Unique identifier for the alert</span></span> |
| `Title` | <span data-ttu-id="60ff7-117">string</span><span class="sxs-lookup"><span data-stu-id="60ff7-117">string</span></span> | <span data-ttu-id="60ff7-118">Titre de l'alerte</span><span class="sxs-lookup"><span data-stu-id="60ff7-118">Title of the alert</span></span> |
| `Category` | <span data-ttu-id="60ff7-119">string</span><span class="sxs-lookup"><span data-stu-id="60ff7-119">string</span></span> | <span data-ttu-id="60ff7-120">Type d’indicateur de menace ou d’activité de violation identifié par l’alerte</span><span class="sxs-lookup"><span data-stu-id="60ff7-120">Type of threat indicator or breach activity identified by the alert</span></span> |
| `Severity` | <span data-ttu-id="60ff7-121">string</span><span class="sxs-lookup"><span data-stu-id="60ff7-121">string</span></span> | <span data-ttu-id="60ff7-122">Indique l’impact potentiel (élevé, moyen ou faible) de l’indicateur de menace ou de la violation identifié(e) par l’alerte</span><span class="sxs-lookup"><span data-stu-id="60ff7-122">Indicates the potential impact (high, medium, or low) of the threat indicator or breach activity identified by the alert</span></span> |
| `ServiceSource` | <span data-ttu-id="60ff7-123">string</span><span class="sxs-lookup"><span data-stu-id="60ff7-123">string</span></span> | <span data-ttu-id="60ff7-124">Produit ou service qui a fourni les informations d’alerte</span><span class="sxs-lookup"><span data-stu-id="60ff7-124">Product or service that provided the alert information</span></span> |
| `DetectionSource` | <span data-ttu-id="60ff7-125">string</span><span class="sxs-lookup"><span data-stu-id="60ff7-125">string</span></span> | <span data-ttu-id="60ff7-126">Technologie ou capteur de détection qui a identifié le composant ou l’activité notable</span><span class="sxs-lookup"><span data-stu-id="60ff7-126">Detection technology or sensor that identified the notable component or activity</span></span> |
| `AttackTechniques` | <span data-ttu-id="60ff7-127">string</span><span class="sxs-lookup"><span data-stu-id="60ff7-127">string</span></span> | <span data-ttu-id="60ff7-128">MITRE ATT&techniques CK associées à l’activité ayant déclenché l’alerte</span><span class="sxs-lookup"><span data-stu-id="60ff7-128">MITRE ATT&CK techniques associated with the activity that triggered the alert</span></span> |

## <a name="related-topics"></a><span data-ttu-id="60ff7-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="60ff7-129">Related topics</span></span>
- [<span data-ttu-id="60ff7-130">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="60ff7-130">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="60ff7-131">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="60ff7-131">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="60ff7-132">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="60ff7-132">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="60ff7-133">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="60ff7-133">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="60ff7-134">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="60ff7-134">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="60ff7-135">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="60ff7-135">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
