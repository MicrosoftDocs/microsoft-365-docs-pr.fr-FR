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
ms.openlocfilehash: 4ee07abe7ce1432921a843d713d0f9b914631174
ms.sourcegitcommit: dffb9b72acd2e0bd286ff7e79c251e7ec6e8ecae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "47949311"
---
# <a name="assignedipaddresses"></a><span data-ttu-id="41c2e-104">AssignedIPAddresses()</span><span class="sxs-lookup"><span data-stu-id="41c2e-104">AssignedIPAddresses()</span></span>

<span data-ttu-id="41c2e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="41c2e-105">**Applies to:**</span></span>
- <span data-ttu-id="41c2e-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="41c2e-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="41c2e-107">Utilisez la `AssignedIPAddresses()` fonction pour obtenir rapidement les dernières adresses IP qui ont été affectées à un appareil.</span><span class="sxs-lookup"><span data-stu-id="41c2e-107">Use the `AssignedIPAddresses()` function to quickly obtain the latest IP addresses that have been assigned to a device.</span></span> <span data-ttu-id="41c2e-108">Si vous spécifiez un argument timestamp, cette fonction obtient les adresses IP les plus récentes à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="41c2e-108">If you specify a timestamp argument, this function obtains the most recent IP addresses at the specified time.</span></span> 

<span data-ttu-id="41c2e-109">Cette fonction renvoie une table avec les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="41c2e-109">This function returns a table with the following columns:</span></span>

| <span data-ttu-id="41c2e-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="41c2e-110">Column</span></span> | <span data-ttu-id="41c2e-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="41c2e-111">Data type</span></span> | <span data-ttu-id="41c2e-112">Description</span><span class="sxs-lookup"><span data-stu-id="41c2e-112">Description</span></span> |
|------------|-------------|-------------|
| `Timestamp` | <span data-ttu-id="41c2e-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="41c2e-113">datetime</span></span> | <span data-ttu-id="41c2e-114">Dernière heure à laquelle l’appareil a été observé à l’aide de l’adresse IP</span><span class="sxs-lookup"><span data-stu-id="41c2e-114">Latest time when the device was observed using the IP address</span></span> |
| `IPAddress` | <span data-ttu-id="41c2e-115">string</span><span class="sxs-lookup"><span data-stu-id="41c2e-115">string</span></span> | <span data-ttu-id="41c2e-116">Adresse IP utilisée par l’appareil</span><span class="sxs-lookup"><span data-stu-id="41c2e-116">IP address used by the device</span></span> |
| `IPType` | <span data-ttu-id="41c2e-117">string</span><span class="sxs-lookup"><span data-stu-id="41c2e-117">string</span></span> | <span data-ttu-id="41c2e-118">Indique si l’adresse IP est une adresse publique ou privée</span><span class="sxs-lookup"><span data-stu-id="41c2e-118">Indicates whether the IP address is a public or private address</span></span> |
| `NetworkAdapterType` | <span data-ttu-id="41c2e-119">int</span><span class="sxs-lookup"><span data-stu-id="41c2e-119">int</span></span> | <span data-ttu-id="41c2e-120">Type de carte réseau utilisé par l’appareil auquel l’adresse IP a été attribuée.</span><span class="sxs-lookup"><span data-stu-id="41c2e-120">Network adapter type used by the device that has been assigned the IP address.</span></span> <span data-ttu-id="41c2e-121">Pour les valeurs possibles, reportez-vous à [cette énumération](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.networkinterfacetype)</span><span class="sxs-lookup"><span data-stu-id="41c2e-121">For the possible values, refer to [this enumeration](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.networkinterfacetype)</span></span> |
| `ConnectedNetworks` | <span data-ttu-id="41c2e-122">int</span><span class="sxs-lookup"><span data-stu-id="41c2e-122">int</span></span> | <span data-ttu-id="41c2e-123">Réseaux auxquels est connectée la carte à laquelle l’adresse IP est attribuée.</span><span class="sxs-lookup"><span data-stu-id="41c2e-123">Networks that the adapter with the assigned IP address is connected to.</span></span> <span data-ttu-id="41c2e-124">Chaque tableau JSON contient le nom de réseau, la catégorie (public, privé ou domaine), une description et un indicateur qui indique s’il est connecté publiquement à Internet.</span><span class="sxs-lookup"><span data-stu-id="41c2e-124">Each JSON array contains the network name, category (public, private, or domain), a description, and a flag indicating if it's connected publicly to the internet</span></span> |

## <a name="syntax"></a><span data-ttu-id="41c2e-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41c2e-125">Syntax</span></span>

```kusto
AssignedIPAddresses(x, y)
```

## <a name="arguments"></a><span data-ttu-id="41c2e-126">Arguments</span><span class="sxs-lookup"><span data-stu-id="41c2e-126">Arguments</span></span>

- <span data-ttu-id="41c2e-127">**x**— `DeviceId` ou `DeviceName` valeur identifiant l’appareil</span><span class="sxs-lookup"><span data-stu-id="41c2e-127">**x**—`DeviceId` or `DeviceName` value identifying the device</span></span>
- <span data-ttu-id="41c2e-128">**y**— `Timestamp` valeur (DateTime) indiquant à la fonction d’obtenir les adresses IP affectées les plus récentes à partir d’un certain temps.</span><span class="sxs-lookup"><span data-stu-id="41c2e-128">**y**—`Timestamp` (datetime) value instructing the function to obtain the most recent assigned IP addresses from a specific time.</span></span> <span data-ttu-id="41c2e-129">Si ce n’est pas spécifié, la fonction renvoie les dernières adresses IP.</span><span class="sxs-lookup"><span data-stu-id="41c2e-129">If not specified, the function returns the latest IP addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="41c2e-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="41c2e-130">Examples</span></span>

### <a name="get-the-list-of-ip-addresses-used-by-a-device-24-hours-ago"></a><span data-ttu-id="41c2e-131">Obtenir la liste des adresses IP utilisées par un périphérique il y a 24 heures</span><span class="sxs-lookup"><span data-stu-id="41c2e-131">Get the list of IP addresses used by a device 24 hours ago</span></span>

```kusto
AssignedIPAddresses('example-device-name', ago(1d))
```

### <a name="get-ip-addresses-used-by-a-device-and-find-devices-communicating-with-it"></a><span data-ttu-id="41c2e-132">Obtenir des adresses IP utilisées par un appareil et trouver des périphériques communiquant avec celui-ci</span><span class="sxs-lookup"><span data-stu-id="41c2e-132">Get IP addresses used by a device and find devices communicating with it</span></span>
<span data-ttu-id="41c2e-133">Cette requête utilise la `AssignedIPAddresses()` fonction pour obtenir des adresses IP attribuées pour l’appareil ( `example-device-name` ) au plus tard à une date spécifique ( `example-date` ).</span><span class="sxs-lookup"><span data-stu-id="41c2e-133">This query uses the `AssignedIPAddresses()` function to get assigned IP addresses for the device (`example-device-name`) on or before a specific date (`example-date`).</span></span> <span data-ttu-id="41c2e-134">Il utilise ensuite les adresses IP pour rechercher les connexions à l’appareil initié par d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="41c2e-134">It then uses the IP addresses to find connections to the device initiated by other devices.</span></span> 

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

## <a name="related-topics"></a><span data-ttu-id="41c2e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41c2e-135">Related topics</span></span>
- [<span data-ttu-id="41c2e-136">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="41c2e-136">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="41c2e-137">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="41c2e-137">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="41c2e-138">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="41c2e-138">Understand the schema</span></span>](advanced-hunting-schema-tables.md)