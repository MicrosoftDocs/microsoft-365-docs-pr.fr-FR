---
title: Obtenir des informations pertinentes sur une entité avec la recherche de Go
description: Découvrez comment utiliser l’outil « aller-retour » pour demander rapidement des informations pertinentes sur une entité ou un événement à l’aide de la chasse avancée.
keywords: recherche avancée, incident, tableau croisé dynamique, entité, recherche de contenu, événements pertinents, recherche de menace, recherche sur les menaces informatiques, recherche, requête, télémétrie, Microsoft 365, protection contre les menaces Microsoft
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
ms.openlocfilehash: 496deff5d2fda47b7ffac4bc87e98bf28e90ea50
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48196964"
---
# <a name="quickly-hunt-for-entity-or-event-information-with-go-hunt"></a><span data-ttu-id="c6cfb-104">Recherche rapide d’informations sur les entités ou les événements avec la recherche de Go</span><span class="sxs-lookup"><span data-stu-id="c6cfb-104">Quickly hunt for entity or event information with go hunt</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="c6cfb-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c6cfb-105">**Applies to:**</span></span>
- <span data-ttu-id="c6cfb-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="c6cfb-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="c6cfb-107">L’action de *recherche aller-retour* vous permet d’examiner rapidement les événements et différents types d’entité à l’aide de puissantes fonctionnalités de recherche [avancée](advanced-hunting-overview.md) basées sur les requêtes.</span><span class="sxs-lookup"><span data-stu-id="c6cfb-107">With the *go hunt* action, you can quickly investigate events and various entity types using powerful query-based [advanced hunting](advanced-hunting-overview.md) capabilities.</span></span> <span data-ttu-id="c6cfb-108">Cette action exécute automatiquement une requête de chasse avancée pour trouver des informations pertinentes sur l’événement ou l’entité sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c6cfb-108">This action automatically runs an advanced hunting query to find relevant information about the selected event or entity.</span></span>

<span data-ttu-id="c6cfb-109">L’action aller à la *recherche* est disponible dans les différentes sections du centre de sécurité chaque fois que des détails d’événements ou d’entités sont affichés.</span><span class="sxs-lookup"><span data-stu-id="c6cfb-109">The *go hunt* action is available in various sections of the security center whenever event or entity details are displayed.</span></span> <span data-ttu-id="c6cfb-110">Par exemple, vous pouvez utiliser la *recherche aller* à partir des sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="c6cfb-110">For example, you can use *go hunt* from the following sections:</span></span>

- <span data-ttu-id="c6cfb-111">Dans la [page incident](investigate-incidents.md#incident-overview), vous pouvez consulter les détails relatifs aux utilisateurs, aux appareils et à de nombreuses autres entités associées à un incident.</span><span class="sxs-lookup"><span data-stu-id="c6cfb-111">In the [incident page](investigate-incidents.md#incident-overview), you can review details about users, devices, and many other entities associated with an incident.</span></span> <span data-ttu-id="c6cfb-112">Lorsque vous sélectionnez une entité, vous obtenez des informations supplémentaires, ainsi que diverses actions que vous pouvez effectuer sur cette entitity.</span><span class="sxs-lookup"><span data-stu-id="c6cfb-112">As you select an entity, you get additional information as well as various actions you could take on that entitity.</span></span> <span data-ttu-id="c6cfb-113">Dans l’exemple ci-dessous, une boîte aux lettres est sélectionnée, affichant des détails sur la boîte aux lettres, ainsi que la recherche d’informations supplémentaires sur la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="c6cfb-113">In the example below, a mailbox is selected, showing details about the mailbox as well the option to hunt for more information about the mailbox.</span></span>

    ![Image illustrant les détails de la boîte aux lettres avec l’option aller à la recherche](../../media/mtp-ah/go-hunt-email.png)

- <span data-ttu-id="c6cfb-115">Dans la page incident, vous pouvez également accéder à une liste d’entités sous l’onglet preuve. La sélection de l’une de ces entités offre une option permettant de rechercher rapidement des informations sur cette entité.</span><span class="sxs-lookup"><span data-stu-id="c6cfb-115">In the incident page, you can also access a list of entities under the evidence tab. Selecting one of those entities provides an option to quickly hunt for information about that entity.</span></span>

    ![Image illustrant le fichier sélectionné avec l’option aller à la recherche dans l’onglet preuve](../../media/mtp-ah/go-hunt-evidence-file.png)


- <span data-ttu-id="c6cfb-117">Lors de l’affichage de la chronologie d’un appareil, vous pouvez sélectionner un événement dans la chronologie pour afficher des informations supplémentaires sur cet événement.</span><span class="sxs-lookup"><span data-stu-id="c6cfb-117">When viewing the timeline for a device, you can select an event in the timeline to view additional information about that event.</span></span> <span data-ttu-id="c6cfb-118">Une fois qu’un événement est sélectionné, vous avez la possibilité de rechercher d’autres événements pertinents dans la recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="c6cfb-118">Once an event is selected, you get the option to hunt for other relevant events in advanced hunting.</span></span>

    ![Image montrant les détails de l’événement avec l’option aller à la recherche](../../media/mtp-ah/go-hunt-event.png)

<span data-ttu-id="c6cfb-120">La sélection de l’option **aller-retour** ou **Hunt pour les événements associés** transmet des requêtes différentes, selon que vous avez sélectionné une entité ou un événement.</span><span class="sxs-lookup"><span data-stu-id="c6cfb-120">Selecting **Go hunt** or **Hunt for related events** passes different queries, depending on whether you've selected an entity or an event.</span></span>

## <a name="query-for-entity-information"></a><span data-ttu-id="c6cfb-121">Requête d’informations d’entité</span><span class="sxs-lookup"><span data-stu-id="c6cfb-121">Query for entity information</span></span>
<span data-ttu-id="c6cfb-122">Lors de l’utilisation de la *recherche aller-retour* pour obtenir des informations sur un utilisateur, un appareil ou tout autre type d’entité, la requête vérifie toutes les tables de schéma pertinentes pour les événements impliquant cette entité.</span><span class="sxs-lookup"><span data-stu-id="c6cfb-122">When using *go hunt* to query for information about a user, device, or any other type of entity, the query checks all relevant schema tables for any events involving that entity.</span></span> <span data-ttu-id="c6cfb-123">Pour que les résultats soient gérables, la requête est étendue à environ la même période que l’activité la plus ancienne au cours des 30 derniers jours qui implique l’entité et qui est associée à l’incident.</span><span class="sxs-lookup"><span data-stu-id="c6cfb-123">To keep the results manageable, the query is scoped to around the same time period as the earliest activity in the past 30 days that involves the entity and is associated with the incident.</span></span>

<span data-ttu-id="c6cfb-124">Voici un exemple de la requête Go Hunt pour un appareil :</span><span class="sxs-lookup"><span data-stu-id="c6cfb-124">Here is an example of the go hunt query for a device:</span></span>

```kusto
let selectedTimestamp = datetime(2020-06-02T02:06:47.1167157Z);
let deviceName = "fv-az770.example.com";
let deviceId = "device-guid";
search in (DeviceLogonEvents, DeviceProcessEvents, DeviceNetworkEvents, DeviceFileEvents, DeviceRegistryEvents, DeviceImageLoadEvents, DeviceEvents, DeviceImageLoadEvents, IdentityLogonEvents, IdentityQueryEvents)
Timestamp between ((selectedTimestamp - 1h) .. (selectedTimestamp + 1h))
and DeviceName == deviceName
// or RemoteDeviceName == deviceName
// or DeviceId == deviceId
| take 100
```
### <a name="supported-entity-types"></a><span data-ttu-id="c6cfb-125">Types d’entités pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6cfb-125">Supported entity types</span></span>
<span data-ttu-id="c6cfb-126">Vous pouvez utiliser la *recherche aller-retour* après avoir sélectionné l’un de ces types d’entité :</span><span class="sxs-lookup"><span data-stu-id="c6cfb-126">You can use *go hunt* after selecting any of these entity types:</span></span>

- <span data-ttu-id="c6cfb-127">Fichiers</span><span class="sxs-lookup"><span data-stu-id="c6cfb-127">Files</span></span>
- <span data-ttu-id="c6cfb-128">Messages électroniques</span><span class="sxs-lookup"><span data-stu-id="c6cfb-128">Emails</span></span>
- <span data-ttu-id="c6cfb-129">Clusters de messagerie</span><span class="sxs-lookup"><span data-stu-id="c6cfb-129">Email clusters</span></span>
- <span data-ttu-id="c6cfb-130">Boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="c6cfb-130">Mailboxes</span></span>
- <span data-ttu-id="c6cfb-131">Users</span><span class="sxs-lookup"><span data-stu-id="c6cfb-131">Users</span></span>
- <span data-ttu-id="c6cfb-132">Appareils</span><span class="sxs-lookup"><span data-stu-id="c6cfb-132">Devices</span></span>
- <span data-ttu-id="c6cfb-133">Adresses IP</span><span class="sxs-lookup"><span data-stu-id="c6cfb-133">IP addresses</span></span>
- <span data-ttu-id="c6cfb-134">URL</span><span class="sxs-lookup"><span data-stu-id="c6cfb-134">URLs</span></span>

## <a name="query-for-event-information"></a><span data-ttu-id="c6cfb-135">Requête d’informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="c6cfb-135">Query for event information</span></span>
<span data-ttu-id="c6cfb-136">Lors de l’utilisation de la *recherche aller-retour* pour obtenir des informations sur un événement de chronologie, la requête vérifie toutes les tables de schéma pertinentes pour les autres événements autour de l’heure de l’événement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c6cfb-136">When using *go hunt* to query for information about a timeline event, the query checks all relevant schema tables for other events around the time of the selected event.</span></span> <span data-ttu-id="c6cfb-137">Par exemple, la requête suivante répertorie les événements de différentes tables de schéma qui se sont produites sur la même période sur le même appareil :</span><span class="sxs-lookup"><span data-stu-id="c6cfb-137">For example, the following query lists events in various schema tables that occured around the same time period on the same device:</span></span>

```kusto
// List relevant events 30 minutes before and after selected LogonAttempted event
let selectedEventTimestamp = datetime(2020-06-04T01:29:09.2496688Z);
search in (DeviceFileEvents, DeviceProcessEvents, DeviceEvents, DeviceRegistryEvents, DeviceNetworkEvents, DeviceImageLoadEvents, DeviceLogonEvents)
    Timestamp between ((selectedEventTimestamp - 30m) .. (selectedEventTimestamp + 30m))
    and DeviceId == "079ecf9c5798d249128817619606c1c47369eb3e"
| sort by Timestamp desc
| extend Relevance = iff(Timestamp == selectedEventTimestamp, "Selected event", iff(Timestamp < selectedEventTimestamp, "Earlier event", "Later event"))
| project-reorder Relevance
```

## <a name="adjust-the-query"></a><span data-ttu-id="c6cfb-138">Ajuster la requête</span><span class="sxs-lookup"><span data-stu-id="c6cfb-138">Adjust the query</span></span>
<span data-ttu-id="c6cfb-139">Avec certaines connaissances du [langage de requête](advanced-hunting-query-language.md), vous pouvez ajuster la requête à vos préférences.</span><span class="sxs-lookup"><span data-stu-id="c6cfb-139">With some knowledge of the [query language](advanced-hunting-query-language.md), you can adjust the query to your preference.</span></span> <span data-ttu-id="c6cfb-140">Par exemple, vous pouvez ajuster cette ligne, ce qui détermine la taille de la fenêtre de temps :</span><span class="sxs-lookup"><span data-stu-id="c6cfb-140">For example, you can adjust this line, which determines the size of the time window:</span></span>

```kusto
Timestamp between ((selectedTimestamp - 1h) .. (selectedTimestamp + 1h))
```

<span data-ttu-id="c6cfb-141">En plus de modifier la requête pour obtenir des résultats plus pertinents, vous pouvez également effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c6cfb-141">In addition to modifying the query to get more relevant results, you can also:</span></span>
- [<span data-ttu-id="c6cfb-142">Afficher les résultats sous forme de graphiques</span><span class="sxs-lookup"><span data-stu-id="c6cfb-142">View the results as charts</span></span>](advanced-hunting-query-results.md#view-query-results-as-a-table-or-chart)
- [<span data-ttu-id="c6cfb-143">Créer une règle de détection personnalisée</span><span class="sxs-lookup"><span data-stu-id="c6cfb-143">Create a custom detection rule</span></span>](custom-detection-rules.md)

## <a name="related-topics"></a><span data-ttu-id="c6cfb-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6cfb-144">Related topics</span></span>
- [<span data-ttu-id="c6cfb-145">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="c6cfb-145">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="c6cfb-146">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="c6cfb-146">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="c6cfb-147">Travailler avec les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="c6cfb-147">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="c6cfb-148">Règles de détection personnalisées</span><span class="sxs-lookup"><span data-stu-id="c6cfb-148">Custom detection rules</span></span>](custom-detection-rules.md)
