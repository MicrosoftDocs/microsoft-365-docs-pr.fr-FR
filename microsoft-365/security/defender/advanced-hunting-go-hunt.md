---
title: Obtenir des informations pertinentes sur une entité avec go hunt
description: Découvrez comment utiliser l’outil de recherche pour rapidement interroger des informations pertinentes sur une entité ou un événement à l’aide d’un recherche avancée.
keywords: advanced hunting, incident, pivot, entity, go hunt, relevant events, threat hunting, cyber threat hunting, search, query, telemetry, Microsoft 365, Microsoft 365 Defender
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
ms.openlocfilehash: a78f37d8c1fed1063095e25f19136f0362f17db7
ms.sourcegitcommit: 7cc2be0244fcc30049351e35c25369cacaaf4ca9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "51952655"
---
# <a name="quickly-hunt-for-entity-or-event-information-with-go-hunt"></a><span data-ttu-id="51b8e-104">Recherche rapide des informations sur l’entité ou les événements avec la recherche de go</span><span class="sxs-lookup"><span data-stu-id="51b8e-104">Quickly hunt for entity or event information with go hunt</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="51b8e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="51b8e-105">**Applies to:**</span></span>
- <span data-ttu-id="51b8e-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="51b8e-106">Microsoft 365 Defender</span></span>
- <span data-ttu-id="51b8e-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="51b8e-107">Microsoft Defender for Endpoint</span></span>

<span data-ttu-id="51b8e-108">Avec *l’action de recherche* go, vous pouvez rapidement examiner les événements et différents types d’entités à l’aide de puissantes fonctionnalités de recherche avancée [basées](advanced-hunting-overview.md) sur des requêtes.</span><span class="sxs-lookup"><span data-stu-id="51b8e-108">With the *go hunt* action, you can quickly investigate events and various entity types using powerful query-based [advanced hunting](advanced-hunting-overview.md) capabilities.</span></span> <span data-ttu-id="51b8e-109">Cette action exécute automatiquement une requête de recherche avancée pour rechercher des informations pertinentes sur l’événement ou l’entité sélectionné.</span><span class="sxs-lookup"><span data-stu-id="51b8e-109">This action automatically runs an advanced hunting query to find relevant information about the selected event or entity.</span></span>

<span data-ttu-id="51b8e-110">*L’action de recherche* est disponible dans différentes sections du centre de sécurité chaque fois que les détails de l’événement ou de l’entité sont affichés.</span><span class="sxs-lookup"><span data-stu-id="51b8e-110">The *go hunt* action is available in various sections of the security center whenever event or entity details are displayed.</span></span> <span data-ttu-id="51b8e-111">Par exemple, vous pouvez utiliser *la recherche dans* les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="51b8e-111">For example, you can use *go hunt* from the following sections:</span></span>

- <span data-ttu-id="51b8e-112">Dans la [page Incident,](investigate-incidents.md#summary)vous pouvez consulter les détails sur les utilisateurs, les appareils et de nombreuses autres entités associées à un incident.</span><span class="sxs-lookup"><span data-stu-id="51b8e-112">In the [incident page](investigate-incidents.md#summary), you can review details about users, devices, and many other entities associated with an incident.</span></span> <span data-ttu-id="51b8e-113">Lorsque vous sélectionnez une entité, vous obtenez des informations supplémentaires ainsi que diverses actions que vous pouvez prendre sur cette entité.</span><span class="sxs-lookup"><span data-stu-id="51b8e-113">As you select an entity, you get additional information as well as various actions you could take on that entity.</span></span> <span data-ttu-id="51b8e-114">Dans l’exemple ci-dessous, une boîte aux lettres est sélectionnée, affichant des détails sur la boîte aux lettres, ainsi que l’option de recherche pour plus d’informations sur la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="51b8e-114">In the example below, a mailbox is selected, showing details about the mailbox as well the option to hunt for more information about the mailbox.</span></span>

    ![Image montrant les détails de la boîte aux lettres avec l’option aller à la recherche](../../media/mtp-ah/go-hunt-email.png)

- <span data-ttu-id="51b8e-116">Dans la page Incident, vous pouvez également accéder à une liste d’entités sous l’onglet Preuve. La sélection de l’une de ces entités permet de trouver rapidement des informations sur cette entité.</span><span class="sxs-lookup"><span data-stu-id="51b8e-116">In the incident page, you can also access a list of entities under the evidence tab. Selecting one of those entities provides an option to quickly hunt for information about that entity.</span></span>

    ![Image montrant le fichier sélectionné avec l’option Aller à la recherche dans l’onglet Preuves](../../media/mtp-ah/go-hunt-evidence-file.png)


- <span data-ttu-id="51b8e-118">Lorsque vous affichez la chronologie d’un appareil, vous pouvez sélectionner un événement dans la chronologie pour afficher des informations supplémentaires sur cet événement.</span><span class="sxs-lookup"><span data-stu-id="51b8e-118">When viewing the timeline for a device, you can select an event in the timeline to view additional information about that event.</span></span> <span data-ttu-id="51b8e-119">Une fois qu’un événement est sélectionné, vous avez la possibilité de chercher d’autres événements pertinents dans le hunting avancé.</span><span class="sxs-lookup"><span data-stu-id="51b8e-119">Once an event is selected, you get the option to hunt for other relevant events in advanced hunting.</span></span>

    ![Image montrant les détails de l’événement avec l’option aller à la recherche](../../media/mtp-ah/go-hunt-event.png)

<span data-ttu-id="51b8e-121">La sélection **de la** fonction De recherche ou de recherche pour les événements connexes transmet différentes requêtes, selon que vous avez sélectionné une entité ou un événement. </span><span class="sxs-lookup"><span data-stu-id="51b8e-121">Selecting **Go hunt** or **Hunt for related events** passes different queries, depending on whether you've selected an entity or an event.</span></span>

## <a name="query-for-entity-information"></a><span data-ttu-id="51b8e-122">Requête d’informations sur l’entité</span><span class="sxs-lookup"><span data-stu-id="51b8e-122">Query for entity information</span></span>
<span data-ttu-id="51b8e-123">Lorsque vous utilisez *go hunt* to query for information about a user, device, or any other type of entity, the query checks all relevant schema tables for any events involving that entity.</span><span class="sxs-lookup"><span data-stu-id="51b8e-123">When using *go hunt* to query for information about a user, device, or any other type of entity, the query checks all relevant schema tables for any events involving that entity.</span></span> <span data-ttu-id="51b8e-124">Pour que les résultats restent gérables, la requête est limitée à la même période que l’activité la plus tôt au cours des 30 derniers jours qui implique l’entité et est associée à l’incident.</span><span class="sxs-lookup"><span data-stu-id="51b8e-124">To keep the results manageable, the query is scoped to around the same time period as the earliest activity in the past 30 days that involves the entity and is associated with the incident.</span></span>

<span data-ttu-id="51b8e-125">Voici un exemple de requête go hunt pour un appareil :</span><span class="sxs-lookup"><span data-stu-id="51b8e-125">Here is an example of the go hunt query for a device:</span></span>

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
### <a name="supported-entity-types"></a><span data-ttu-id="51b8e-126">Types d’entités pris en charge</span><span class="sxs-lookup"><span data-stu-id="51b8e-126">Supported entity types</span></span>
<span data-ttu-id="51b8e-127">Vous pouvez utiliser *la recherche après* avoir sélectionné l’un des types d’entités ci-après :</span><span class="sxs-lookup"><span data-stu-id="51b8e-127">You can use *go hunt* after selecting any of these entity types:</span></span>

- <span data-ttu-id="51b8e-128">Fichiers</span><span class="sxs-lookup"><span data-stu-id="51b8e-128">Files</span></span>
- <span data-ttu-id="51b8e-129">Messages électroniques</span><span class="sxs-lookup"><span data-stu-id="51b8e-129">Emails</span></span>
- <span data-ttu-id="51b8e-130">Clusters de messagerie</span><span class="sxs-lookup"><span data-stu-id="51b8e-130">Email clusters</span></span>
- <span data-ttu-id="51b8e-131">Boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="51b8e-131">Mailboxes</span></span>
- <span data-ttu-id="51b8e-132">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="51b8e-132">Users</span></span>
- <span data-ttu-id="51b8e-133">Appareils</span><span class="sxs-lookup"><span data-stu-id="51b8e-133">Devices</span></span>
- <span data-ttu-id="51b8e-134">Adresses IP</span><span class="sxs-lookup"><span data-stu-id="51b8e-134">IP addresses</span></span>
- <span data-ttu-id="51b8e-135">URL</span><span class="sxs-lookup"><span data-stu-id="51b8e-135">URLs</span></span>

## <a name="query-for-event-information"></a><span data-ttu-id="51b8e-136">Requête d’informations sur les événements</span><span class="sxs-lookup"><span data-stu-id="51b8e-136">Query for event information</span></span>
<span data-ttu-id="51b8e-137">Lorsque vous *utilisez go hunt* to query pour obtenir des informations sur un événement de chronologie, la requête vérifie toutes les tables de schéma pertinentes pour les autres événements à l’heure de l’événement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="51b8e-137">When using *go hunt* to query for information about a timeline event, the query checks all relevant schema tables for other events around the time of the selected event.</span></span> <span data-ttu-id="51b8e-138">Par exemple, la requête suivante répertorie les événements dans différentes tables de schéma qui se sont produits autour de la même période sur le même appareil :</span><span class="sxs-lookup"><span data-stu-id="51b8e-138">For example, the following query lists events in various schema tables that occurred around the same time period on the same device:</span></span>

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

## <a name="adjust-the-query"></a><span data-ttu-id="51b8e-139">Ajuster la requête</span><span class="sxs-lookup"><span data-stu-id="51b8e-139">Adjust the query</span></span>
<span data-ttu-id="51b8e-140">Avec une certaine connaissance du langage [de requête,](advanced-hunting-query-language.md)vous pouvez ajuster la requête à vos préférences.</span><span class="sxs-lookup"><span data-stu-id="51b8e-140">With some knowledge of the [query language](advanced-hunting-query-language.md), you can adjust the query to your preference.</span></span> <span data-ttu-id="51b8e-141">Par exemple, vous pouvez ajuster cette ligne, qui détermine la taille de la fenêtre de temps :</span><span class="sxs-lookup"><span data-stu-id="51b8e-141">For example, you can adjust this line, which determines the size of the time window:</span></span>

```kusto
Timestamp between ((selectedTimestamp - 1h) .. (selectedTimestamp + 1h))
```

<span data-ttu-id="51b8e-142">En plus de modifier la requête pour obtenir des résultats plus pertinents, vous pouvez également :</span><span class="sxs-lookup"><span data-stu-id="51b8e-142">In addition to modifying the query to get more relevant results, you can also:</span></span>
- [<span data-ttu-id="51b8e-143">Afficher les résultats en tant que graphiques</span><span class="sxs-lookup"><span data-stu-id="51b8e-143">View the results as charts</span></span>](advanced-hunting-query-results.md#view-query-results-as-a-table-or-chart)
- [<span data-ttu-id="51b8e-144">Créer une règle de détection personnalisée</span><span class="sxs-lookup"><span data-stu-id="51b8e-144">Create a custom detection rule</span></span>](custom-detection-rules.md)

>[!NOTE]
><span data-ttu-id="51b8e-145">Certains tableaux de cet article peuvent ne pas être disponibles dans Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="51b8e-145">Some tables in this article might not be available in Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="51b8e-146">[Activer Microsoft 365 Defender pour qu’il](m365d-enable.md) recherche les menaces à l’aide de sources de données plus nombreuses.</span><span class="sxs-lookup"><span data-stu-id="51b8e-146">[Turn on Microsoft 365 Defender](m365d-enable.md) to hunt for threats using more data sources.</span></span> <span data-ttu-id="51b8e-147">Vous pouvez déplacer vos flux de travail de recherche avancée de Microsoft Defender pour point de terminaison vers Microsoft 365 Defender en suivant les étapes de la procédure de migration des requêtes de recherche avancée à partir de Microsoft Defender pour le point de [terminaison.](advanced-hunting-migrate-from-mde.md)</span><span class="sxs-lookup"><span data-stu-id="51b8e-147">You can move your advanced hunting workflows from Microsoft Defender for Endpoint to Microsoft 365 Defender by following the steps in [Migrate advanced hunting queries from Microsoft Defender for Endpoint](advanced-hunting-migrate-from-mde.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="51b8e-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51b8e-148">Related topics</span></span>
- [<span data-ttu-id="51b8e-149">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="51b8e-149">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="51b8e-150">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="51b8e-150">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="51b8e-151">Utiliser les résultats d’une requête</span><span class="sxs-lookup"><span data-stu-id="51b8e-151">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="51b8e-152">Règles de détection personnalisée</span><span class="sxs-lookup"><span data-stu-id="51b8e-152">Custom detection rules</span></span>](custom-detection-rules.md)
