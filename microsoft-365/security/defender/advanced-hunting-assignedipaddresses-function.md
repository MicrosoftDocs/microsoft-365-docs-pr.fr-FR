---
title: Fonction AssignedIPAddresses() dans le recherche avancée pour Microsoft 365 Defender
description: Découvrez comment utiliser la fonction AssignedIPAddresses() pour obtenir les dernières adresses IP attribuées à un appareil
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, FileProfile, file profile, function, enrichment
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
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: 3760ff84e6abfbe05d9e4605d64087d0077300e3
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51063598"
---
# <a name="assignedipaddresses"></a><span data-ttu-id="c6b56-104">AssignedIPAddresses()</span><span class="sxs-lookup"><span data-stu-id="c6b56-104">AssignedIPAddresses()</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="c6b56-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c6b56-105">**Applies to:**</span></span>
- <span data-ttu-id="c6b56-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c6b56-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="c6b56-107">Utilisez la fonction dans vos requêtes de recherche avancées pour obtenir rapidement les dernières `AssignedIPAddresses()` adresses IP attribuées à [](advanced-hunting-overview.md) un appareil.</span><span class="sxs-lookup"><span data-stu-id="c6b56-107">Use the `AssignedIPAddresses()` function in your [advanced hunting](advanced-hunting-overview.md) queries to quickly obtain the latest IP addresses that have been assigned to a device.</span></span> <span data-ttu-id="c6b56-108">Si vous spécifiez un argument d’timestamp, cette fonction obtient les adresses IP les plus récentes à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c6b56-108">If you specify a timestamp argument, this function obtains the most recent IP addresses at the specified time.</span></span> 

<span data-ttu-id="c6b56-109">Cette fonction renvoie un tableau avec les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="c6b56-109">This function returns a table with the following columns:</span></span>

| <span data-ttu-id="c6b56-110">Column</span><span class="sxs-lookup"><span data-stu-id="c6b56-110">Column</span></span> | <span data-ttu-id="c6b56-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="c6b56-111">Data type</span></span> | <span data-ttu-id="c6b56-112">Description</span><span class="sxs-lookup"><span data-stu-id="c6b56-112">Description</span></span> |
|------------|-------------|-------------|
| `Timestamp` | <span data-ttu-id="c6b56-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="c6b56-113">datetime</span></span> | <span data-ttu-id="c6b56-114">Heure de la dernière observation de l’appareil à l’aide de l’adresse IP</span><span class="sxs-lookup"><span data-stu-id="c6b56-114">Latest time when the device was observed using the IP address</span></span> |
| `IPAddress` | <span data-ttu-id="c6b56-115">string</span><span class="sxs-lookup"><span data-stu-id="c6b56-115">string</span></span> | <span data-ttu-id="c6b56-116">Adresse IP utilisée par l’appareil</span><span class="sxs-lookup"><span data-stu-id="c6b56-116">IP address used by the device</span></span> |
| `IPType` | <span data-ttu-id="c6b56-117">string</span><span class="sxs-lookup"><span data-stu-id="c6b56-117">string</span></span> | <span data-ttu-id="c6b56-118">Indique si l’adresse IP est une adresse publique ou privée</span><span class="sxs-lookup"><span data-stu-id="c6b56-118">Indicates whether the IP address is a public or private address</span></span> |
| `NetworkAdapterType` | <span data-ttu-id="c6b56-119">entier</span><span class="sxs-lookup"><span data-stu-id="c6b56-119">int</span></span> | <span data-ttu-id="c6b56-120">Type de carte réseau utilisé par l’appareil à qui l’adresse IP a été attribuée.</span><span class="sxs-lookup"><span data-stu-id="c6b56-120">Network adapter type used by the device that has been assigned the IP address.</span></span> <span data-ttu-id="c6b56-121">Pour les valeurs possibles, reportez-vous [à cette éumération](/dotnet/api/system.net.networkinformation.networkinterfacetype)</span><span class="sxs-lookup"><span data-stu-id="c6b56-121">For the possible values, refer to [this enumeration](/dotnet/api/system.net.networkinformation.networkinterfacetype)</span></span> |
| `ConnectedNetworks` | <span data-ttu-id="c6b56-122">entier</span><span class="sxs-lookup"><span data-stu-id="c6b56-122">int</span></span> | <span data-ttu-id="c6b56-123">Réseaux à qui l’adaptateur avec l’adresse IP affectée est connectée.</span><span class="sxs-lookup"><span data-stu-id="c6b56-123">Networks that the adapter with the assigned IP address is connected to.</span></span> <span data-ttu-id="c6b56-124">Chaque tableau JSON contient le nom du réseau, la catégorie (public, privé ou domaine), une description et un indicateur indiquant s’il est connecté publiquement à Internet</span><span class="sxs-lookup"><span data-stu-id="c6b56-124">Each JSON array contains the network name, category (public, private, or domain), a description, and a flag indicating if it's connected publicly to the internet</span></span> |

## <a name="syntax"></a><span data-ttu-id="c6b56-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6b56-125">Syntax</span></span>

```kusto
AssignedIPAddresses(x, y)
```

## <a name="arguments"></a><span data-ttu-id="c6b56-126">Arguments</span><span class="sxs-lookup"><span data-stu-id="c6b56-126">Arguments</span></span>

- <span data-ttu-id="c6b56-127">**x** ou `DeviceId` valeur identifiant `DeviceName` l’appareil</span><span class="sxs-lookup"><span data-stu-id="c6b56-127">**x**—`DeviceId` or `DeviceName` value identifying the device</span></span>
- <span data-ttu-id="c6b56-128">**y**— valeur (datetime) qui indique à la fonction d’obtenir les adresses IP attribuées les plus `Timestamp` récentes à partir d’une heure spécifique.</span><span class="sxs-lookup"><span data-stu-id="c6b56-128">**y**—`Timestamp` (datetime) value instructing the function to obtain the most recent assigned IP addresses from a specific time.</span></span> <span data-ttu-id="c6b56-129">Si elle n’est pas spécifiée, la fonction renvoie les dernières adresses IP.</span><span class="sxs-lookup"><span data-stu-id="c6b56-129">If not specified, the function returns the latest IP addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="c6b56-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="c6b56-130">Examples</span></span>

### <a name="get-the-list-of-ip-addresses-used-by-a-device-24-hours-ago"></a><span data-ttu-id="c6b56-131">Obtenir la liste des adresses IP utilisées par un appareil il y a 24 heures</span><span class="sxs-lookup"><span data-stu-id="c6b56-131">Get the list of IP addresses used by a device 24 hours ago</span></span>

```kusto
AssignedIPAddresses('example-device-name', ago(1d))
```

### <a name="get-ip-addresses-used-by-a-device-and-find-devices-communicating-with-it"></a><span data-ttu-id="c6b56-132">Obtenir les adresses IP utilisées par un appareil et trouver les appareils qui communiquent avec lui</span><span class="sxs-lookup"><span data-stu-id="c6b56-132">Get IP addresses used by a device and find devices communicating with it</span></span>
<span data-ttu-id="c6b56-133">Cette requête utilise la fonction pour obtenir des adresses IP attribuées pour l’appareil ( ) à une date spécifique `AssignedIPAddresses()` `example-device-name` ou avant ( `example-date` ).</span><span class="sxs-lookup"><span data-stu-id="c6b56-133">This query uses the `AssignedIPAddresses()` function to get assigned IP addresses for the device (`example-device-name`) on or before a specific date (`example-date`).</span></span> <span data-ttu-id="c6b56-134">Il utilise ensuite les adresses IP pour rechercher les connexions à l’appareil initiées par d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="c6b56-134">It then uses the IP addresses to find connections to the device initiated by other devices.</span></span> 

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

## <a name="related-topics"></a><span data-ttu-id="c6b56-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6b56-135">Related topics</span></span>
- [<span data-ttu-id="c6b56-136">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="c6b56-136">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="c6b56-137">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="c6b56-137">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="c6b56-138">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="c6b56-138">Understand the schema</span></span>](advanced-hunting-schema-tables.md)