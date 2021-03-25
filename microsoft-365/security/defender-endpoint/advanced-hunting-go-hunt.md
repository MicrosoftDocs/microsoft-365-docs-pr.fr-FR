---
title: Obtenir des informations pertinentes sur une entité avec go hunt
description: Découvrez comment utiliser l’outil de recherche pour rapidement interroger des informations pertinentes sur une entité ou un événement à l’aide d’une recherche avancée.
keywords: recherche avancée, incident, tableau croisé dynamique, entité, rechercher, événements pertinents, recherche de menaces, recherche, requête, télémétrie, Protection Microsoft contre les menaces
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: v-maave
author: martyav
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 4fe3c204fe49f008cf5d9dd18b5066fa91dc6196
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51067953"
---
# <a name="quickly-hunt-for-entity-or-event-information-with-go-hunt"></a><span data-ttu-id="dbaa9-104">Recherche rapide des informations sur l’entité ou les événements avec la recherche de go</span><span class="sxs-lookup"><span data-stu-id="dbaa9-104">Quickly hunt for entity or event information with go hunt</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="dbaa9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="dbaa9-105">**Applies to:**</span></span>
- [<span data-ttu-id="dbaa9-106">Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="dbaa9-106">Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

><span data-ttu-id="dbaa9-107">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="dbaa9-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="dbaa9-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-advancedhuntingref-abovefoldlink)


<span data-ttu-id="dbaa9-109">Avec *l’action de recherche* go, vous pouvez rapidement examiner les événements et différents types d’entités à l’aide de puissantes fonctionnalités de recherche avancée [basées](advanced-hunting-overview.md) sur des requêtes.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-109">With the *go hunt* action, you can quickly investigate events and various entity types using powerful query-based [advanced hunting](advanced-hunting-overview.md) capabilities.</span></span> <span data-ttu-id="dbaa9-110">Cette action exécute automatiquement une requête de recherche avancée pour rechercher des informations pertinentes sur l’événement ou l’entité sélectionné.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-110">This action automatically runs an advanced hunting query to find relevant information about the selected event or entity.</span></span>

<span data-ttu-id="dbaa9-111">*L’action de recherche* est disponible dans différentes sections du centre de sécurité chaque fois que les détails de l’événement ou de l’entité sont affichés.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-111">The *go hunt* action is available in various sections of the security center whenever event or entity details are displayed.</span></span> <span data-ttu-id="dbaa9-112">Par exemple, vous pouvez utiliser *la recherche dans* les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbaa9-112">For example, you can use *go hunt* from the following sections:</span></span>

- <span data-ttu-id="dbaa9-113">Dans la [page Incident,](investigate-incidents.md)vous pouvez consulter les détails sur les utilisateurs, les appareils et de nombreuses autres entités associées à un incident.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-113">In the [incident page](investigate-incidents.md), you can review details about users, devices, and many other entities associated with an incident.</span></span> <span data-ttu-id="dbaa9-114">Lorsque vous sélectionnez une entité, vous obtenez des informations supplémentaires ainsi que diverses actions que vous pouvez prendre sur cette entité.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-114">When you select an entity, you get additional information as well as various actions you could take on that entity.</span></span> <span data-ttu-id="dbaa9-115">Dans l’exemple ci-dessous, un appareil est sélectionné, affichant des détails sur l’appareil, ainsi que l’option de recherche d’informations supplémentaires sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-115">In the example below, a device is selected, showing details about the device as well the option to hunt for more information about the device.</span></span>

    ![Image montrant les détails de l’appareil avec l’option aller à la recherche](./images/go-hunt-device.png)

- <span data-ttu-id="dbaa9-117">Dans la page incident, vous pouvez également accéder à une liste d’entités sous l’onglet Preuve. La sélection de l’une de ces entités permet de trouver rapidement des informations sur cette entité.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-117">In the incident page, you can also access a list of entities under the evidence tab. Selecting one of those entities provides an option to quickly hunt for information about that entity.</span></span>

    ![Image montrant l’URL sélectionnée avec l’option Aller à la recherche dans l’onglet Preuves](./images/go-hunt-evidence-url.png)

- <span data-ttu-id="dbaa9-119">Lorsque vous affichez la chronologie d’un appareil, vous pouvez sélectionner un événement dans la chronologie pour afficher des informations supplémentaires sur cet événement.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-119">When viewing the timeline for a device, you can select an event in the timeline to view additional information about that event.</span></span> <span data-ttu-id="dbaa9-120">Une fois qu’un événement est sélectionné, vous avez la possibilité de chercher d’autres événements pertinents dans le hunting avancé.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-120">Once an event is selected, you get the option to hunt for other relevant events in advanced hunting.</span></span>

    ![Image montrant les détails de l’événement avec l’option aller à la recherche](./images/go-hunt-event.png)

<span data-ttu-id="dbaa9-122">La sélection **de la** fonction De recherche ou de recherche pour les événements connexes transmet différentes requêtes, selon que vous avez sélectionné une entité ou un événement. </span><span class="sxs-lookup"><span data-stu-id="dbaa9-122">Selecting **Go hunt** or **Hunt for related events** passes different queries, depending on whether you've selected an entity or an event.</span></span>

## <a name="query-for-entity-information"></a><span data-ttu-id="dbaa9-123">Requête d’informations sur l’entité</span><span class="sxs-lookup"><span data-stu-id="dbaa9-123">Query for entity information</span></span>

<span data-ttu-id="dbaa9-124">Lorsque vous utilisez *go hunt* to query for information about a user, device, or any other type of entity, the query checks all relevant schema tables for any events involving that entity.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-124">When using *go hunt* to query for information about a user, device, or any other type of entity, the query checks all relevant schema tables for any events involving that entity.</span></span> <span data-ttu-id="dbaa9-125">Pour que les résultats restent gérables, la requête est limitée à la même période que l’activité la plus tôt au cours des 30 derniers jours qui implique l’entité et est associée à l’incident.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-125">To keep the results manageable, the query is scoped to around the same time period as the earliest activity in the past 30 days that involves the entity and is associated with the incident.</span></span>

<span data-ttu-id="dbaa9-126">Voici un exemple de requête go hunt pour un appareil :</span><span class="sxs-lookup"><span data-stu-id="dbaa9-126">Here is an example of the go hunt query for a device:</span></span>

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

### <a name="supported-entity-types"></a><span data-ttu-id="dbaa9-127">Types d’entités pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbaa9-127">Supported entity types</span></span>

<span data-ttu-id="dbaa9-128">Vous pouvez utiliser *la recherche après* avoir sélectionné l’un des types d’entités ci-après :</span><span class="sxs-lookup"><span data-stu-id="dbaa9-128">You can use *go hunt* after selecting any of these entity types:</span></span>

- <span data-ttu-id="dbaa9-129">Fichiers</span><span class="sxs-lookup"><span data-stu-id="dbaa9-129">Files</span></span>
- <span data-ttu-id="dbaa9-130">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="dbaa9-130">Users</span></span>
- <span data-ttu-id="dbaa9-131">Appareils</span><span class="sxs-lookup"><span data-stu-id="dbaa9-131">Devices</span></span>
- <span data-ttu-id="dbaa9-132">Adresses IP</span><span class="sxs-lookup"><span data-stu-id="dbaa9-132">IP addresses</span></span>
- <span data-ttu-id="dbaa9-133">URL</span><span class="sxs-lookup"><span data-stu-id="dbaa9-133">URLs</span></span>

## <a name="query-for-event-information"></a><span data-ttu-id="dbaa9-134">Requête d’informations sur les événements</span><span class="sxs-lookup"><span data-stu-id="dbaa9-134">Query for event information</span></span>

<span data-ttu-id="dbaa9-135">Lorsque vous *utilisez go hunt* to query pour obtenir des informations sur un événement de chronologie, la requête vérifie toutes les tables de schéma pertinentes pour les autres événements à l’heure de l’événement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-135">When using *go hunt* to query for information about a timeline event, the query checks all relevant schema tables for other events around the time of the selected event.</span></span> <span data-ttu-id="dbaa9-136">Par exemple, la requête suivante répertorie les événements dans différentes tables de schéma qui se sont produits autour de la même période sur le même appareil :</span><span class="sxs-lookup"><span data-stu-id="dbaa9-136">For example, the following query lists events in various schema tables that occurred around the same time period on the same device:</span></span>

```kusto
// List relevant events 30 minutes before and after selected RegistryValueSet event
let selectedEventTimestamp = datetime(2020-10-06T21:40:25.3466868Z);
search in (DeviceFileEvents, DeviceProcessEvents, DeviceEvents, DeviceRegistryEvents, DeviceNetworkEvents, DeviceImageLoadEvents, DeviceLogonEvents)
    Timestamp between ((selectedEventTimestamp - 30m) .. (selectedEventTimestamp + 30m))
    and DeviceId == "a305b52049c4658ec63ae8b55becfe5954c654a4"
| sort by Timestamp desc
| extend Relevance = iff(Timestamp == selectedEventTimestamp, "Selected event", iff(Timestamp < selectedEventTimestamp, "Earlier event", "Later event"))
| project-reorder Relevance
```

## <a name="adjust-the-query"></a><span data-ttu-id="dbaa9-137">Ajuster la requête</span><span class="sxs-lookup"><span data-stu-id="dbaa9-137">Adjust the query</span></span>

<span data-ttu-id="dbaa9-138">Avec une certaine connaissance du langage [de requête,](advanced-hunting-query-language.md)vous pouvez ajuster la requête à votre préférence.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-138">With some knowledge of the [query language](advanced-hunting-query-language.md), you can adjust the query to your preference.</span></span> <span data-ttu-id="dbaa9-139">Par exemple, vous pouvez ajuster cette ligne, qui détermine la taille de la fenêtre de temps :</span><span class="sxs-lookup"><span data-stu-id="dbaa9-139">For example, you can adjust this line, which determines the size of the time window:</span></span>

```kusto
Timestamp between ((selectedTimestamp - 1h) .. (selectedTimestamp + 1h))
```

<span data-ttu-id="dbaa9-140">En plus de modifier la requête pour obtenir des résultats plus pertinents, vous pouvez également :</span><span class="sxs-lookup"><span data-stu-id="dbaa9-140">In addition to modifying the query to get more relevant results, you can also:</span></span>

- [<span data-ttu-id="dbaa9-141">Afficher les résultats en tant que graphiques</span><span class="sxs-lookup"><span data-stu-id="dbaa9-141">View the results as charts</span></span>](advanced-hunting-query-results.md#view-query-results-as-a-table-or-chart)
- [<span data-ttu-id="dbaa9-142">Créer une règle de détection personnalisée</span><span class="sxs-lookup"><span data-stu-id="dbaa9-142">Create a custom detection rule</span></span>](custom-detection-rules.md)

## <a name="related-topics"></a><span data-ttu-id="dbaa9-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbaa9-143">Related topics</span></span>

- [<span data-ttu-id="dbaa9-144">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="dbaa9-144">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="dbaa9-145">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="dbaa9-145">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="dbaa9-146">Travailler avec les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="dbaa9-146">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="dbaa9-147">Règles de détection personnalisée</span><span class="sxs-lookup"><span data-stu-id="dbaa9-147">Custom detection rules</span></span>](custom-detection-rules.md)
