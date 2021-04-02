---
title: Fonction AssignedIPAddresses() dans le recherche avancée de Microsoft Defender pour point de terminaison
description: Découvrez comment utiliser la fonction AssignedIPAddresses() pour obtenir les dernières adresses IP attribuées à un appareil
keywords: advanced hunting, threat hunting, cyber threat hunting, mdatp, Microsoft Defender ATP, Microsoft Defender for Endpoint, Windows Defender, Windows Defender ATP, Windows Defender Advanced Threat Protection, search, query, telemetry, schema reference, kusto, FileProfile, file profile, function, enrichment
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: maccruz
author: schmurky
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.date: 09/20/2020
ms.technology: mde
ms.openlocfilehash: 5dcc41302d797b4084c36d020908ba59131c90d4
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51499284"
---
# <a name="assignedipaddresses"></a><span data-ttu-id="57b27-104">AssignedIPAddresses()</span><span class="sxs-lookup"><span data-stu-id="57b27-104">AssignedIPAddresses()</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

><span data-ttu-id="57b27-105">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="57b27-105">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="57b27-106">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="57b27-106">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-advancedfeats-abovefoldlink)

<span data-ttu-id="57b27-107">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="57b27-107">**Applies to:**</span></span>
- [<span data-ttu-id="57b27-108">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="57b27-108">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)


<span data-ttu-id="57b27-109">Utilisez la fonction dans vos requêtes de recherche avancées pour obtenir rapidement les dernières adresses IP qui ont été `AssignedIPAddresses()` attribuées à un appareil.</span><span class="sxs-lookup"><span data-stu-id="57b27-109">Use the `AssignedIPAddresses()` function in your advanced hunting queries to quickly obtain the latest IP addresses that have been assigned to a device.</span></span> <span data-ttu-id="57b27-110">Si vous spécifiez un argument d’timestamp, cette fonction obtient les adresses IP les plus récentes à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="57b27-110">If you specify a timestamp argument, this function obtains the most recent IP addresses at the specified time.</span></span>

<span data-ttu-id="57b27-111">Cette fonction renvoie un tableau avec les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="57b27-111">This function returns a table with the following columns:</span></span>

<span data-ttu-id="57b27-112">Column</span><span class="sxs-lookup"><span data-stu-id="57b27-112">Column</span></span> | <span data-ttu-id="57b27-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="57b27-113">Data type</span></span> | <span data-ttu-id="57b27-114">Description</span><span class="sxs-lookup"><span data-stu-id="57b27-114">Description</span></span>
-|-|-
`Timestamp` | <span data-ttu-id="57b27-115">DateHeure</span><span class="sxs-lookup"><span data-stu-id="57b27-115">datetime</span></span> | <span data-ttu-id="57b27-116">Heure de la dernière observation de l’appareil à l’aide de l’adresse IP</span><span class="sxs-lookup"><span data-stu-id="57b27-116">Latest time when the device was observed using the IP address</span></span>
`IPAddress` | <span data-ttu-id="57b27-117">string</span><span class="sxs-lookup"><span data-stu-id="57b27-117">string</span></span> | <span data-ttu-id="57b27-118">Adresse IP utilisée par l’appareil</span><span class="sxs-lookup"><span data-stu-id="57b27-118">IP address used by the device</span></span>
`IPType` | <span data-ttu-id="57b27-119">string</span><span class="sxs-lookup"><span data-stu-id="57b27-119">string</span></span> | <span data-ttu-id="57b27-120">Indique si l’adresse IP est une adresse publique ou privée</span><span class="sxs-lookup"><span data-stu-id="57b27-120">Indicates whether the IP address is a public or private address</span></span>
`NetworkAdapterType` | <span data-ttu-id="57b27-121">entier</span><span class="sxs-lookup"><span data-stu-id="57b27-121">int</span></span> | <span data-ttu-id="57b27-122">Type de carte réseau utilisé par l’appareil à qui l’adresse IP a été attribuée.</span><span class="sxs-lookup"><span data-stu-id="57b27-122">Network adapter type used by the device that has been assigned the IP address.</span></span> <span data-ttu-id="57b27-123">Pour les valeurs possibles, reportez-vous [à cette éumération](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.networkinterfacetype)</span><span class="sxs-lookup"><span data-stu-id="57b27-123">For the possible values, refer to [this enumeration](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.networkinterfacetype)</span></span>
`ConnectedNetworks` | <span data-ttu-id="57b27-124">entier</span><span class="sxs-lookup"><span data-stu-id="57b27-124">int</span></span> | <span data-ttu-id="57b27-125">Réseaux à qui la carte avec l’adresse IP affectée est connectée.</span><span class="sxs-lookup"><span data-stu-id="57b27-125">Networks that the adapter with the assigned IP address is connected to.</span></span> <span data-ttu-id="57b27-126">Chaque tableau JSON contient le nom du réseau, la catégorie (public, privé ou domaine), une description et un indicateur indiquant s’il est connecté publiquement à Internet</span><span class="sxs-lookup"><span data-stu-id="57b27-126">Each JSON array contains the network name, category (public, private, or domain), a description, and a flag indicating if it's connected publicly to the internet</span></span>

## <a name="syntax"></a><span data-ttu-id="57b27-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57b27-127">Syntax</span></span>

```kusto
AssignedIPAddresses(x, y)
```

## <a name="arguments"></a><span data-ttu-id="57b27-128">Arguments</span><span class="sxs-lookup"><span data-stu-id="57b27-128">Arguments</span></span>

- <span data-ttu-id="57b27-129">**x** ou `DeviceId` valeur identifiant `DeviceName` l’appareil</span><span class="sxs-lookup"><span data-stu-id="57b27-129">**x**—`DeviceId` or `DeviceName` value identifying the device</span></span>
- <span data-ttu-id="57b27-130">**y**— valeur (date/heure) qui indique à la fonction d’obtenir les adresses IP attribuées les plus `Timestamp` récentes à partir d’une heure spécifique.</span><span class="sxs-lookup"><span data-stu-id="57b27-130">**y**—`Timestamp` (datetime) value instructing the function to obtain the most recent assigned IP addresses from a specific time.</span></span> <span data-ttu-id="57b27-131">Si elle n’est pas spécifiée, la fonction renvoie les dernières adresses IP.</span><span class="sxs-lookup"><span data-stu-id="57b27-131">If not specified, the function returns the latest IP addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="57b27-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="57b27-132">Examples</span></span>

### <a name="get-the-list-of-ip-addresses-used-by-a-device-24-hours-ago"></a><span data-ttu-id="57b27-133">Obtenir la liste des adresses IP utilisées par un appareil il y a 24 heures</span><span class="sxs-lookup"><span data-stu-id="57b27-133">Get the list of IP addresses used by a device 24 hours ago</span></span>

```kusto
AssignedIPAddresses('example-device-name', ago(1d))
```

### <a name="get-ip-addresses-used-by-a-device-and-find-devices-communicating-with-it"></a><span data-ttu-id="57b27-134">Obtenir les adresses IP utilisées par un appareil et trouver les appareils qui communiquent avec lui</span><span class="sxs-lookup"><span data-stu-id="57b27-134">Get IP addresses used by a device and find devices communicating with it</span></span>

<span data-ttu-id="57b27-135">Cette requête utilise la fonction pour obtenir des adresses IP attribuées pour l’appareil ( ) à une date spécifique `AssignedIPAddresses()` `example-device-name` ou avant ( `example-date` ).</span><span class="sxs-lookup"><span data-stu-id="57b27-135">This query uses the `AssignedIPAddresses()` function to get assigned IP addresses for the device (`example-device-name`) on or before a specific date (`example-date`).</span></span> <span data-ttu-id="57b27-136">Il utilise ensuite les adresses IP pour rechercher les connexions à l’appareil initiées par d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="57b27-136">It then uses the IP addresses to find connections to the device initiated by other devices.</span></span> 

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

## <a name="related-topics"></a><span data-ttu-id="57b27-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57b27-137">Related topics</span></span>

- [<span data-ttu-id="57b27-138">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="57b27-138">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="57b27-139">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="57b27-139">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="57b27-140">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="57b27-140">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
