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
ms.collection:
- M365-security-compliance
- m365-initiative-m365-defender
ms.topic: article
ms.openlocfilehash: 7f0b479051c46fe35ec9aea84b23ca0c4937fbfe
ms.sourcegitcommit: 5e1b8c959a081022826fb09358730096248507ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48412321"
---
# <a name="assignedipaddresses"></a><span data-ttu-id="98032-104">AssignedIPAddresses()</span><span class="sxs-lookup"><span data-stu-id="98032-104">AssignedIPAddresses()</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="98032-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="98032-105">**Applies to:**</span></span>
- <span data-ttu-id="98032-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="98032-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="98032-107">Utilisez la `AssignedIPAddresses()` fonction dans vos requêtes de [chasse avancée](advanced-hunting-overview.md) pour obtenir rapidement les dernières adresses IP qui ont été affectées à un appareil.</span><span class="sxs-lookup"><span data-stu-id="98032-107">Use the `AssignedIPAddresses()` function in your [advanced hunting](advanced-hunting-overview.md) queries to quickly obtain the latest IP addresses that have been assigned to a device.</span></span> <span data-ttu-id="98032-108">Si vous spécifiez un argument timestamp, cette fonction obtient les adresses IP les plus récentes à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="98032-108">If you specify a timestamp argument, this function obtains the most recent IP addresses at the specified time.</span></span> 

<span data-ttu-id="98032-109">Cette fonction renvoie une table avec les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="98032-109">This function returns a table with the following columns:</span></span>

| <span data-ttu-id="98032-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="98032-110">Column</span></span> | <span data-ttu-id="98032-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="98032-111">Data type</span></span> | <span data-ttu-id="98032-112">Description</span><span class="sxs-lookup"><span data-stu-id="98032-112">Description</span></span> |
|------------|-------------|-------------|
| `Timestamp` | <span data-ttu-id="98032-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="98032-113">datetime</span></span> | <span data-ttu-id="98032-114">Dernière heure à laquelle l’appareil a été observé à l’aide de l’adresse IP</span><span class="sxs-lookup"><span data-stu-id="98032-114">Latest time when the device was observed using the IP address</span></span> |
| `IPAddress` | <span data-ttu-id="98032-115">string</span><span class="sxs-lookup"><span data-stu-id="98032-115">string</span></span> | <span data-ttu-id="98032-116">Adresse IP utilisée par l’appareil</span><span class="sxs-lookup"><span data-stu-id="98032-116">IP address used by the device</span></span> |
| `IPType` | <span data-ttu-id="98032-117">string</span><span class="sxs-lookup"><span data-stu-id="98032-117">string</span></span> | <span data-ttu-id="98032-118">Indique si l’adresse IP est une adresse publique ou privée</span><span class="sxs-lookup"><span data-stu-id="98032-118">Indicates whether the IP address is a public or private address</span></span> |
| `NetworkAdapterType` | <span data-ttu-id="98032-119">int</span><span class="sxs-lookup"><span data-stu-id="98032-119">int</span></span> | <span data-ttu-id="98032-120">Type de carte réseau utilisé par l’appareil auquel l’adresse IP a été attribuée.</span><span class="sxs-lookup"><span data-stu-id="98032-120">Network adapter type used by the device that has been assigned the IP address.</span></span> <span data-ttu-id="98032-121">Pour les valeurs possibles, reportez-vous à [cette énumération](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.networkinterfacetype)</span><span class="sxs-lookup"><span data-stu-id="98032-121">For the possible values, refer to [this enumeration](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.networkinterfacetype)</span></span> |
| `ConnectedNetworks` | <span data-ttu-id="98032-122">int</span><span class="sxs-lookup"><span data-stu-id="98032-122">int</span></span> | <span data-ttu-id="98032-123">Réseaux auxquels est connectée la carte à laquelle l’adresse IP est attribuée.</span><span class="sxs-lookup"><span data-stu-id="98032-123">Networks that the adapter with the assigned IP address is connected to.</span></span> <span data-ttu-id="98032-124">Chaque tableau JSON contient le nom de réseau, la catégorie (public, privé ou domaine), une description et un indicateur qui indique s’il est connecté publiquement à Internet.</span><span class="sxs-lookup"><span data-stu-id="98032-124">Each JSON array contains the network name, category (public, private, or domain), a description, and a flag indicating if it's connected publicly to the internet</span></span> |

## <a name="syntax"></a><span data-ttu-id="98032-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98032-125">Syntax</span></span>

```kusto
AssignedIPAddresses(x, y)
```

## <a name="arguments"></a><span data-ttu-id="98032-126">Arguments</span><span class="sxs-lookup"><span data-stu-id="98032-126">Arguments</span></span>

- <span data-ttu-id="98032-127">**x**— `DeviceId` ou `DeviceName` valeur identifiant l’appareil</span><span class="sxs-lookup"><span data-stu-id="98032-127">**x**—`DeviceId` or `DeviceName` value identifying the device</span></span>
- <span data-ttu-id="98032-128">**y**— `Timestamp` valeur (DateTime) indiquant à la fonction d’obtenir les adresses IP affectées les plus récentes à partir d’un certain temps.</span><span class="sxs-lookup"><span data-stu-id="98032-128">**y**—`Timestamp` (datetime) value instructing the function to obtain the most recent assigned IP addresses from a specific time.</span></span> <span data-ttu-id="98032-129">Si ce n’est pas spécifié, la fonction renvoie les dernières adresses IP.</span><span class="sxs-lookup"><span data-stu-id="98032-129">If not specified, the function returns the latest IP addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="98032-130">範例</span><span class="sxs-lookup"><span data-stu-id="98032-130">Examples</span></span>

### <a name="get-the-list-of-ip-addresses-used-by-a-device-24-hours-ago"></a><span data-ttu-id="98032-131">Obtenir la liste des adresses IP utilisées par un périphérique il y a 24 heures</span><span class="sxs-lookup"><span data-stu-id="98032-131">Get the list of IP addresses used by a device 24 hours ago</span></span>

```kusto
AssignedIPAddresses('example-device-name', ago(1d))
```

### <a name="get-ip-addresses-used-by-a-device-and-find-devices-communicating-with-it"></a><span data-ttu-id="98032-132">Obtenir des adresses IP utilisées par un appareil et trouver des périphériques communiquant avec celui-ci</span><span class="sxs-lookup"><span data-stu-id="98032-132">Get IP addresses used by a device and find devices communicating with it</span></span>
<span data-ttu-id="98032-133">Cette requête utilise la `AssignedIPAddresses()` fonction pour obtenir des adresses IP attribuées pour l’appareil ( `example-device-name` ) au plus tard à une date spécifique ( `example-date` ).</span><span class="sxs-lookup"><span data-stu-id="98032-133">This query uses the `AssignedIPAddresses()` function to get assigned IP addresses for the device (`example-device-name`) on or before a specific date (`example-date`).</span></span> <span data-ttu-id="98032-134">Il utilise ensuite les adresses IP pour rechercher les connexions à l’appareil initié par d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="98032-134">It then uses the IP addresses to find connections to the device initiated by other devices.</span></span> 

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

## <a name="related-topics"></a><span data-ttu-id="98032-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98032-135">Related topics</span></span>
- [<span data-ttu-id="98032-136">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="98032-136">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="98032-137">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="98032-137">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="98032-138">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="98032-138">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
