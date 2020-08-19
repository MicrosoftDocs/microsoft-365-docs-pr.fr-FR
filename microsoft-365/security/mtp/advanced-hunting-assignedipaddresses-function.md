---
title: Fonction AssignedIPAddresses () pour la protection avancée contre les menaces Microsoft
description: Découvrez comment utiliser la fonction AssignedIPAddresses () pour obtenir les dernières adresses IP affectées à un appareil
keywords: chasse aux menaces, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, FileProfile, profil de fichier, fonction, enrichissement
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
ms.openlocfilehash: 72d02bafa168e48c2d588771f5289da09e6d6000
ms.sourcegitcommit: 234726a1795d984c4659da68f852d30a4dda5711
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/18/2020
ms.locfileid: "46794230"
---
# <a name="assignedipaddresses"></a><span data-ttu-id="26612-104">AssignedIPAddresses()</span><span class="sxs-lookup"><span data-stu-id="26612-104">AssignedIPAddresses()</span></span>

<span data-ttu-id="26612-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="26612-105">**Applies to:**</span></span>
- <span data-ttu-id="26612-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="26612-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="26612-107">Utilisez la `AssignedIPAddresses()` fonction pour obtenir rapidement les dernières adresses IP qui ont été affectées à un appareil ou les adresses IP les plus récentes à partir d’un moment donné.</span><span class="sxs-lookup"><span data-stu-id="26612-107">Use the `AssignedIPAddresses()` function to quickly obtain the latest IP addresses that have been assigned to a device or the most recent IP addresses from a specified point in time.</span></span> <span data-ttu-id="26612-108">Cette fonction renvoie une table avec les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="26612-108">This function returns a table with the following columns:</span></span>

| <span data-ttu-id="26612-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="26612-109">Column</span></span> | <span data-ttu-id="26612-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="26612-110">Data type</span></span> | <span data-ttu-id="26612-111">Description</span><span class="sxs-lookup"><span data-stu-id="26612-111">Description</span></span> |
|------------|-------------|-------------|
| <span data-ttu-id="26612-112">Timestamp</span><span class="sxs-lookup"><span data-stu-id="26612-112">Timestamp</span></span> | <span data-ttu-id="26612-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="26612-113">datetime</span></span> | <span data-ttu-id="26612-114">Dernière heure à laquelle l’appareil a été observé à l’aide de l’adresse IP</span><span class="sxs-lookup"><span data-stu-id="26612-114">Latest time when the device was observed using the IP address</span></span> |
| <span data-ttu-id="26612-115">IPAddress</span><span class="sxs-lookup"><span data-stu-id="26612-115">IPAddress</span></span> | <span data-ttu-id="26612-116">string</span><span class="sxs-lookup"><span data-stu-id="26612-116">string</span></span> | <span data-ttu-id="26612-117">Adresse IP utilisée par l’appareil</span><span class="sxs-lookup"><span data-stu-id="26612-117">IP address used by the device</span></span> |
| <span data-ttu-id="26612-118">IPType</span><span class="sxs-lookup"><span data-stu-id="26612-118">IPType</span></span> | <span data-ttu-id="26612-119">string</span><span class="sxs-lookup"><span data-stu-id="26612-119">string</span></span> | <span data-ttu-id="26612-120">Indique si l’adresse IP est une adresse publique ou privée</span><span class="sxs-lookup"><span data-stu-id="26612-120">Indicates whether the IP address is a public or private address</span></span> |
| <span data-ttu-id="26612-121">NetworkAdapterType</span><span class="sxs-lookup"><span data-stu-id="26612-121">NetworkAdapterType</span></span> | <span data-ttu-id="26612-122">int</span><span class="sxs-lookup"><span data-stu-id="26612-122">int</span></span> | <span data-ttu-id="26612-123">Type de carte réseau utilisé par l’appareil auquel l’adresse IP a été attribuée.</span><span class="sxs-lookup"><span data-stu-id="26612-123">Network adapter type used by the device that has been assigned the IP address.</span></span> <span data-ttu-id="26612-124">Pour les valeurs possibles, reportez-vous à [cette énumération](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.networkinterfacetype?view=netframework-4.7.2)</span><span class="sxs-lookup"><span data-stu-id="26612-124">For the possible values, refer to [this enumeration](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.networkinterfacetype?view=netframework-4.7.2)</span></span>  |
| <span data-ttu-id="26612-125">ConnectedNetworks</span><span class="sxs-lookup"><span data-stu-id="26612-125">ConnectedNetworks</span></span> | <span data-ttu-id="26612-126">int</span><span class="sxs-lookup"><span data-stu-id="26612-126">int</span></span> | <span data-ttu-id="26612-127">Réseaux auxquels est connectée la carte à laquelle l’adresse IP est attribuée.</span><span class="sxs-lookup"><span data-stu-id="26612-127">Networks that the adapter with the assigned IP address is connected to.</span></span> <span data-ttu-id="26612-128">Chaque tableau JSON contient le nom de réseau, la catégorie (public, Private ou Domain), une description et un indicateur qui indique s’il est connecté publiquement à Internet.</span><span class="sxs-lookup"><span data-stu-id="26612-128">Each JSON array contains the network name, category (public, private or domain), a description, and a flag indicating if it's connected publicly to the internet</span></span> |


## <a name="syntax"></a><span data-ttu-id="26612-129">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26612-129">Syntax</span></span>

```kusto
AssignedIPAddresses(x, y)
```

## <a name="arguments"></a><span data-ttu-id="26612-130">Arguments</span><span class="sxs-lookup"><span data-stu-id="26612-130">Arguments</span></span>

- <span data-ttu-id="26612-131">**x** — `DeviceId` ou `DeviceName` valeur identifiant l’appareil</span><span class="sxs-lookup"><span data-stu-id="26612-131">**x** — `DeviceId` or `DeviceName` value identifying the device</span></span>
- <span data-ttu-id="26612-132">**y** — `Timestamp` valeur (DateTime) indiquant le moment spécifique où obtenir les adresses IP les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="26612-132">**y** — `Timestamp` (datetime) value indicating the specific point in time where to get the most recent IP addresses.</span></span> <span data-ttu-id="26612-133">Si ce n’est pas spécifié, la fonction renvoie les dernières adresses IP.</span><span class="sxs-lookup"><span data-stu-id="26612-133">If not specified, the function returns the latest IP addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="26612-134">Exemples</span><span class="sxs-lookup"><span data-stu-id="26612-134">Examples</span></span>

### <a name="get-the-list-of-ip-addresses-used-by-a-device-as-of-24-hours-ago"></a><span data-ttu-id="26612-135">Obtenir la liste des adresses IP utilisées par un périphérique au plus tôt 24 heures</span><span class="sxs-lookup"><span data-stu-id="26612-135">Get the list of IP addresses used by a device as of 24 hours ago</span></span>

```kusto
AssignedIPAddresses('example-device-name', ago(1d))
```

### <a name="get-ip-addresses-used-by-a-device-and-find-devices-communicating-with-it"></a><span data-ttu-id="26612-136">Obtenir des adresses IP utilisées par un appareil et trouver des périphériques communiquant avec celui-ci</span><span class="sxs-lookup"><span data-stu-id="26612-136">Get IP addresses used by a device and find devices communicating with it</span></span>
<span data-ttu-id="26612-137">Cette requête utilise la `AssignedIPAddresses()` fonction pour obtenir des adresses IP attribuées pour l’appareil ( `example-device-name` ) au plus tard à une date spécifique ( `example-date` ).</span><span class="sxs-lookup"><span data-stu-id="26612-137">This query uses the `AssignedIPAddresses()` function to get assigned IP addresses for the device (`example-device-name`) on or before a specific date (`example-date`).</span></span> <span data-ttu-id="26612-138">Il utilise ensuite les adresses IP pour rechercher les connexions à l’appareil initié par d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="26612-138">It then uses the IP addresses to find connections to the device initiated by other devices.</span></span> 

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

## <a name="related-topics"></a><span data-ttu-id="26612-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="26612-139">Related topics</span></span>
- [<span data-ttu-id="26612-140">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="26612-140">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="26612-141">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="26612-141">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="26612-142">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="26612-142">Understand the schema</span></span>](advanced-hunting-schema-tables.md)