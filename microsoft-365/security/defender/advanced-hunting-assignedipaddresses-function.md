---
title: Fonction AssignedIPAddresses() dans le recherche avancée de Microsoft 365 Defender
description: Découvrez comment utiliser la fonction AssignedIPAddresses() pour obtenir les dernières adresses IP attribuées à un appareil
keywords: advanced hunting, threat hunting, cyber threat hunting, Microsoft 365 Defender, microsoft 365, m365, search, query, telemetry, schema reference, kusto, FileProfile, file profile, function, enrichment
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
ms.openlocfilehash: d3ebd301d6c79bf5286d9293e04e4073b99d1e35
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51934908"
---
# <a name="assignedipaddresses"></a><span data-ttu-id="d1ef2-104">AssignedIPAddresses()</span><span class="sxs-lookup"><span data-stu-id="d1ef2-104">AssignedIPAddresses()</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="d1ef2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d1ef2-105">**Applies to:**</span></span>
- <span data-ttu-id="d1ef2-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d1ef2-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="d1ef2-107">Utilisez la fonction dans vos requêtes de recherche avancées pour obtenir rapidement les dernières `AssignedIPAddresses()` adresses IP attribuées à [](advanced-hunting-overview.md) un appareil.</span><span class="sxs-lookup"><span data-stu-id="d1ef2-107">Use the `AssignedIPAddresses()` function in your [advanced hunting](advanced-hunting-overview.md) queries to quickly obtain the latest IP addresses that have been assigned to a device.</span></span> <span data-ttu-id="d1ef2-108">Si vous spécifiez un argument d’timestamp, cette fonction obtient les adresses IP les plus récentes à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d1ef2-108">If you specify a timestamp argument, this function obtains the most recent IP addresses at the specified time.</span></span> 

<span data-ttu-id="d1ef2-109">Cette fonction renvoie un tableau avec les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d1ef2-109">This function returns a table with the following columns:</span></span>

| <span data-ttu-id="d1ef2-110">Column</span><span class="sxs-lookup"><span data-stu-id="d1ef2-110">Column</span></span> | <span data-ttu-id="d1ef2-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="d1ef2-111">Data type</span></span> | <span data-ttu-id="d1ef2-112">Description</span><span class="sxs-lookup"><span data-stu-id="d1ef2-112">Description</span></span> |
|------------|-------------|-------------|
| `Timestamp` | <span data-ttu-id="d1ef2-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="d1ef2-113">datetime</span></span> | <span data-ttu-id="d1ef2-114">Heure de la dernière observation de l’appareil à l’aide de l’adresse IP</span><span class="sxs-lookup"><span data-stu-id="d1ef2-114">Latest time when the device was observed using the IP address</span></span> |
| `IPAddress` | <span data-ttu-id="d1ef2-115">string</span><span class="sxs-lookup"><span data-stu-id="d1ef2-115">string</span></span> | <span data-ttu-id="d1ef2-116">Adresse IP utilisée par l’appareil</span><span class="sxs-lookup"><span data-stu-id="d1ef2-116">IP address used by the device</span></span> |
| `IPType` | <span data-ttu-id="d1ef2-117">string</span><span class="sxs-lookup"><span data-stu-id="d1ef2-117">string</span></span> | <span data-ttu-id="d1ef2-118">Indique si l’adresse IP est une adresse publique ou privée</span><span class="sxs-lookup"><span data-stu-id="d1ef2-118">Indicates whether the IP address is a public or private address</span></span> |
| `NetworkAdapterType` | <span data-ttu-id="d1ef2-119">entier</span><span class="sxs-lookup"><span data-stu-id="d1ef2-119">int</span></span> | <span data-ttu-id="d1ef2-120">Type de carte réseau utilisé par l’appareil à qui l’adresse IP a été attribuée.</span><span class="sxs-lookup"><span data-stu-id="d1ef2-120">Network adapter type used by the device that has been assigned the IP address.</span></span> <span data-ttu-id="d1ef2-121">Pour les valeurs possibles, reportez-vous [à cette éumération](/dotnet/api/system.net.networkinformation.networkinterfacetype)</span><span class="sxs-lookup"><span data-stu-id="d1ef2-121">For the possible values, refer to [this enumeration](/dotnet/api/system.net.networkinformation.networkinterfacetype)</span></span> |
| `ConnectedNetworks` | <span data-ttu-id="d1ef2-122">entier</span><span class="sxs-lookup"><span data-stu-id="d1ef2-122">int</span></span> | <span data-ttu-id="d1ef2-123">Réseaux à qui l’adaptateur avec l’adresse IP affectée est connectée.</span><span class="sxs-lookup"><span data-stu-id="d1ef2-123">Networks that the adapter with the assigned IP address is connected to.</span></span> <span data-ttu-id="d1ef2-124">Chaque tableau JSON contient le nom du réseau, la catégorie (public, privé ou domaine), une description et un indicateur indiquant s’il est connecté publiquement à Internet</span><span class="sxs-lookup"><span data-stu-id="d1ef2-124">Each JSON array contains the network name, category (public, private, or domain), a description, and a flag indicating if it's connected publicly to the internet</span></span> |

## <a name="syntax"></a><span data-ttu-id="d1ef2-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1ef2-125">Syntax</span></span>

```kusto
AssignedIPAddresses(x, y)
```

## <a name="arguments"></a><span data-ttu-id="d1ef2-126">Arguments</span><span class="sxs-lookup"><span data-stu-id="d1ef2-126">Arguments</span></span>

- <span data-ttu-id="d1ef2-127">**x** ou `DeviceId` valeur identifiant `DeviceName` l’appareil</span><span class="sxs-lookup"><span data-stu-id="d1ef2-127">**x**—`DeviceId` or `DeviceName` value identifying the device</span></span>
- <span data-ttu-id="d1ef2-128">**y**— valeur (date/heure) qui indique à la fonction d’obtenir les adresses IP attribuées les plus `Timestamp` récentes à partir d’une heure spécifique.</span><span class="sxs-lookup"><span data-stu-id="d1ef2-128">**y**—`Timestamp` (datetime) value instructing the function to obtain the most recent assigned IP addresses from a specific time.</span></span> <span data-ttu-id="d1ef2-129">Si elle n’est pas spécifiée, la fonction renvoie les dernières adresses IP.</span><span class="sxs-lookup"><span data-stu-id="d1ef2-129">If not specified, the function returns the latest IP addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="d1ef2-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="d1ef2-130">Examples</span></span>

### <a name="get-the-list-of-ip-addresses-used-by-a-device-24-hours-ago"></a><span data-ttu-id="d1ef2-131">Obtenir la liste des adresses IP utilisées par un appareil il y a 24 heures</span><span class="sxs-lookup"><span data-stu-id="d1ef2-131">Get the list of IP addresses used by a device 24 hours ago</span></span>

```kusto
AssignedIPAddresses('example-device-name', ago(1d))
```

### <a name="get-ip-addresses-used-by-a-device-and-find-devices-communicating-with-it"></a><span data-ttu-id="d1ef2-132">Obtenir les adresses IP utilisées par un appareil et trouver les appareils qui communiquent avec lui</span><span class="sxs-lookup"><span data-stu-id="d1ef2-132">Get IP addresses used by a device and find devices communicating with it</span></span>
<span data-ttu-id="d1ef2-133">Cette requête utilise la fonction pour obtenir des adresses IP attribuées pour l’appareil ( ) à une date spécifique `AssignedIPAddresses()` `example-device-name` ou avant ( `example-date` ).</span><span class="sxs-lookup"><span data-stu-id="d1ef2-133">This query uses the `AssignedIPAddresses()` function to get assigned IP addresses for the device (`example-device-name`) on or before a specific date (`example-date`).</span></span> <span data-ttu-id="d1ef2-134">Il utilise ensuite les adresses IP pour rechercher les connexions à l’appareil initiées par d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="d1ef2-134">It then uses the IP addresses to find connections to the device initiated by other devices.</span></span> 

```kusto
let Date = datetime(example-date);
let DeviceName = "example-device-name";
// List IP addresses used on or before the specified date
AssignedIPAddresses(DeviceName, Date)
| project DeviceName, IPAddress, AssignedTime = Timestamp 
// Get all network events on devices with the assigned IP addresses as the destination addresses
| join kind=inner DeviceNetworkEvents on $left.IPAddress == $right.RemoteIP
// Get only network events around the time the IP address was assigned
| where Timestamp between ((AssignedTime - 1h) .. (AssignedTime + 1h))
```

## <a name="related-topics"></a><span data-ttu-id="d1ef2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1ef2-135">Related topics</span></span>
- [<span data-ttu-id="d1ef2-136">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="d1ef2-136">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="d1ef2-137">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="d1ef2-137">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="d1ef2-138">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="d1ef2-138">Understand the schema</span></span>](advanced-hunting-schema-tables.md)