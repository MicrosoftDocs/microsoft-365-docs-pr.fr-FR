---
title: Table AlertInfo dans le schéma de chasse avancé
description: En savoir plus sur les événements de génération d’alerte dans la table AlertInfo du schéma de chasse avancé
keywords: chasse aux menaces, recherche de menace, recherche de menace, protection contre les menaces Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, table, colonne, type de données, description, AlertInfo, alerte, gravité, catégorie, MITRE, ATT&CK, Microsoft Defender ATP, MDATP, Office 365 ATP, Microsoft Cloud App Security, MCAS et Azure ATP
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
- m365initiative-m365-defender
ms.topic: article
ms.openlocfilehash: 7672d974666a381a48da15e0917a46c97df88895
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48847667"
---
# <a name="alertinfo"></a><span data-ttu-id="a64e2-104">AlertInfo</span><span class="sxs-lookup"><span data-stu-id="a64e2-104">AlertInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="a64e2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a64e2-105">**Applies to:**</span></span>
- <span data-ttu-id="a64e2-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a64e2-106">Microsoft 365 Defender</span></span>



<span data-ttu-id="a64e2-107">Le `AlertInfo` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les alertes de Microsoft Defender pour le point de terminaison, Microsoft defender pour Office 365, Microsoft Cloud App Security et Microsoft Defender for Identity.</span><span class="sxs-lookup"><span data-stu-id="a64e2-107">The `AlertInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about alerts from Microsoft  Defender for Endpoint, Microsoft Defender for Office 365, Microsoft Cloud App Security, and Microsoft Defender for Identity.</span></span> <span data-ttu-id="a64e2-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="a64e2-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="a64e2-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a64e2-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="a64e2-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="a64e2-110">Column name</span></span> | <span data-ttu-id="a64e2-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="a64e2-111">Data type</span></span> | <span data-ttu-id="a64e2-112">Description</span><span class="sxs-lookup"><span data-stu-id="a64e2-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="a64e2-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="a64e2-113">datetime</span></span> | <span data-ttu-id="a64e2-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="a64e2-114">Date and time when the event was recorded</span></span> |
| `AlertId` | <span data-ttu-id="a64e2-115">string</span><span class="sxs-lookup"><span data-stu-id="a64e2-115">string</span></span> | <span data-ttu-id="a64e2-116">Identificateur unique de l’alerte</span><span class="sxs-lookup"><span data-stu-id="a64e2-116">Unique identifier for the alert</span></span> |
| `Title` | <span data-ttu-id="a64e2-117">string</span><span class="sxs-lookup"><span data-stu-id="a64e2-117">string</span></span> | <span data-ttu-id="a64e2-118">Titre de l'alerte</span><span class="sxs-lookup"><span data-stu-id="a64e2-118">Title of the alert</span></span> |
| `Category` | <span data-ttu-id="a64e2-119">string</span><span class="sxs-lookup"><span data-stu-id="a64e2-119">string</span></span> | <span data-ttu-id="a64e2-120">Type d’indicateur de menace ou d’activité de violation identifié par l’alerte</span><span class="sxs-lookup"><span data-stu-id="a64e2-120">Type of threat indicator or breach activity identified by the alert</span></span> |
| `Severity` | <span data-ttu-id="a64e2-121">string</span><span class="sxs-lookup"><span data-stu-id="a64e2-121">string</span></span> | <span data-ttu-id="a64e2-122">Indique l’impact potentiel (élevé, moyen ou faible) de l’indicateur de menace ou de la violation identifié(e) par l’alerte</span><span class="sxs-lookup"><span data-stu-id="a64e2-122">Indicates the potential impact (high, medium, or low) of the threat indicator or breach activity identified by the alert</span></span> |
| `ServiceSource` | <span data-ttu-id="a64e2-123">string</span><span class="sxs-lookup"><span data-stu-id="a64e2-123">string</span></span> | <span data-ttu-id="a64e2-124">Produit ou service qui a fourni les informations d’alerte</span><span class="sxs-lookup"><span data-stu-id="a64e2-124">Product or service that provided the alert information</span></span> |
| `DetectionSource` | <span data-ttu-id="a64e2-125">string</span><span class="sxs-lookup"><span data-stu-id="a64e2-125">string</span></span> | <span data-ttu-id="a64e2-126">Technologie ou capteur de détection qui a identifié le composant ou l’activité notable</span><span class="sxs-lookup"><span data-stu-id="a64e2-126">Detection technology or sensor that identified the notable component or activity</span></span> |
| `AttackTechniques` | <span data-ttu-id="a64e2-127">string</span><span class="sxs-lookup"><span data-stu-id="a64e2-127">string</span></span> | <span data-ttu-id="a64e2-128">MITRE ATT&CK techniques associées à l’activité qui a déclenché l’alerte</span><span class="sxs-lookup"><span data-stu-id="a64e2-128">MITRE ATT&CK techniques associated with the activity that triggered the alert</span></span> |

## <a name="related-topics"></a><span data-ttu-id="a64e2-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a64e2-129">Related topics</span></span>
- [<span data-ttu-id="a64e2-130">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="a64e2-130">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="a64e2-131">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="a64e2-131">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="a64e2-132">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="a64e2-132">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="a64e2-133">Rechercher sur les appareils, les emails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="a64e2-133">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="a64e2-134">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="a64e2-134">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="a64e2-135">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="a64e2-135">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
