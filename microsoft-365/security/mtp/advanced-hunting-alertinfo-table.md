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
ms.openlocfilehash: 739ee33b162c1e701603a17e59f0d0c2611c064c
ms.sourcegitcommit: de600339b08951d6dd3933288a8da2327a4b6ef3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/13/2020
ms.locfileid: "48430174"
---
# <a name="alertinfo"></a><span data-ttu-id="33976-104">AlertInfo</span><span class="sxs-lookup"><span data-stu-id="33976-104">AlertInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="33976-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="33976-105">**Applies to:**</span></span>
- <span data-ttu-id="33976-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="33976-106">Microsoft Threat Protection</span></span>



<span data-ttu-id="33976-107">Le `AlertInfo` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les alertes à partir de Microsoft Defender atp, Office 365 ATP, Microsoft Cloud App Security et Azure ATP.</span><span class="sxs-lookup"><span data-stu-id="33976-107">The `AlertInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about alerts from Microsoft Defender ATP, Office 365 ATP, Microsoft Cloud App Security, and Azure ATP.</span></span> <span data-ttu-id="33976-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="33976-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="33976-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="33976-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="33976-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="33976-110">Column name</span></span> | <span data-ttu-id="33976-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="33976-111">Data type</span></span> | <span data-ttu-id="33976-112">Description</span><span class="sxs-lookup"><span data-stu-id="33976-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="33976-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="33976-113">datetime</span></span> | <span data-ttu-id="33976-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="33976-114">Date and time when the event was recorded</span></span> |
| `AlertId` | <span data-ttu-id="33976-115">string</span><span class="sxs-lookup"><span data-stu-id="33976-115">string</span></span> | <span data-ttu-id="33976-116">Identificateur unique de l’alerte</span><span class="sxs-lookup"><span data-stu-id="33976-116">Unique identifier for the alert</span></span> |
| `Title` | <span data-ttu-id="33976-117">string</span><span class="sxs-lookup"><span data-stu-id="33976-117">string</span></span> | <span data-ttu-id="33976-118">Titre de l'alerte</span><span class="sxs-lookup"><span data-stu-id="33976-118">Title of the alert</span></span> |
| `Category` | <span data-ttu-id="33976-119">string</span><span class="sxs-lookup"><span data-stu-id="33976-119">string</span></span> | <span data-ttu-id="33976-120">Type d’indicateur de menace ou d’activité de violation identifié par l’alerte</span><span class="sxs-lookup"><span data-stu-id="33976-120">Type of threat indicator or breach activity identified by the alert</span></span> |
| `Severity` | <span data-ttu-id="33976-121">string</span><span class="sxs-lookup"><span data-stu-id="33976-121">string</span></span> | <span data-ttu-id="33976-122">Indique l’impact potentiel (élevé, moyen ou faible) de l’indicateur de menace ou de la violation identifié(e) par l’alerte</span><span class="sxs-lookup"><span data-stu-id="33976-122">Indicates the potential impact (high, medium, or low) of the threat indicator or breach activity identified by the alert</span></span> |
| `ServiceSource` | <span data-ttu-id="33976-123">string</span><span class="sxs-lookup"><span data-stu-id="33976-123">string</span></span> | <span data-ttu-id="33976-124">Produit ou service qui a fourni les informations d’alerte</span><span class="sxs-lookup"><span data-stu-id="33976-124">Product or service that provided the alert information</span></span> |
| `DetectionSource` | <span data-ttu-id="33976-125">string</span><span class="sxs-lookup"><span data-stu-id="33976-125">string</span></span> | <span data-ttu-id="33976-126">Technologie ou capteur de détection qui a identifié le composant ou l’activité notable</span><span class="sxs-lookup"><span data-stu-id="33976-126">Detection technology or sensor that identified the notable component or activity</span></span> |
| `AttackTechniques` | <span data-ttu-id="33976-127">string</span><span class="sxs-lookup"><span data-stu-id="33976-127">string</span></span> | <span data-ttu-id="33976-128">MITRE ATT&CK techniques associées à l’activité qui a déclenché l’alerte</span><span class="sxs-lookup"><span data-stu-id="33976-128">MITRE ATT&CK techniques associated with the activity that triggered the alert</span></span> |

## <a name="related-topics"></a><span data-ttu-id="33976-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33976-129">Related topics</span></span>
- [<span data-ttu-id="33976-130">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="33976-130">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="33976-131">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="33976-131">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="33976-132">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="33976-132">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="33976-133">Rechercher sur les appareils, les emails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="33976-133">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="33976-134">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="33976-134">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="33976-135">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="33976-135">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
