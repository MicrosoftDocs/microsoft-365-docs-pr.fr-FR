---
title: Fonction DeviceFromIP() dans le recherche avancée pour Microsoft 365 Defender
description: Découvrez comment utiliser la fonction DeviceFromIP() pour obtenir les appareils affectés à une adresse IP spécifique
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, device, devicefromIP, function, enrichment
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
ms.openlocfilehash: d2996021a84186adc6656927dbdc910db4d037de
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51063534"
---
# <a name="devicefromip"></a><span data-ttu-id="c363d-104">DeviceFromIP()</span><span class="sxs-lookup"><span data-stu-id="c363d-104">DeviceFromIP()</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="c363d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c363d-105">**Applies to:**</span></span>
- <span data-ttu-id="c363d-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c363d-106">Microsoft 365 Defender</span></span>


[!INCLUDE [Prerelease information](../includes/prerelease.md)]


<span data-ttu-id="c363d-107">Utilisez la fonction dans vos requêtes de recherche avancées pour obtenir rapidement la liste des appareils qui ont été affectés à une certaine adresse IP à `DeviceFromIP()` un moment donné dans le temps. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="c363d-107">Use the `DeviceFromIP()` function in your [advanced hunting](advanced-hunting-overview.md) queries to quickly obtain the list of devices that have been assigned to a certain IP address at a given point in time.</span></span> 

<span data-ttu-id="c363d-108">Cette fonction renvoie un tableau avec les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="c363d-108">This function returns a table with the following columns:</span></span>

| <span data-ttu-id="c363d-109">Column</span><span class="sxs-lookup"><span data-stu-id="c363d-109">Column</span></span> | <span data-ttu-id="c363d-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="c363d-110">Data type</span></span> | <span data-ttu-id="c363d-111">Description</span><span class="sxs-lookup"><span data-stu-id="c363d-111">Description</span></span> |
|------------|-------------|-------------|
| `IP` | <span data-ttu-id="c363d-112">string</span><span class="sxs-lookup"><span data-stu-id="c363d-112">string</span></span> | <span data-ttu-id="c363d-113">Adresse IP</span><span class="sxs-lookup"><span data-stu-id="c363d-113">IP address</span></span>  |
| `DeviceId` | <span data-ttu-id="c363d-114">string</span><span class="sxs-lookup"><span data-stu-id="c363d-114">string</span></span> | <span data-ttu-id="c363d-115">Identificateur unique de l’appareil dans le service</span><span class="sxs-lookup"><span data-stu-id="c363d-115">Unique identifier for the device in the service</span></span> |


## <a name="syntax"></a><span data-ttu-id="c363d-116">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c363d-116">Syntax</span></span>

```kusto
invoke DeviceFromIP()
```

## <a name="arguments"></a><span data-ttu-id="c363d-117">Arguments</span><span class="sxs-lookup"><span data-stu-id="c363d-117">Arguments</span></span>

<span data-ttu-id="c363d-118">Cette fonction est invoquée dans le cadre d’une requête.</span><span class="sxs-lookup"><span data-stu-id="c363d-118">This function is invoked as part of a query.</span></span>

- <span data-ttu-id="c363d-119">**x**— Le premier paramètre est généralement déjà une colonne dans la requête.</span><span class="sxs-lookup"><span data-stu-id="c363d-119">**x**—The first parameter is typically already a column in the query.</span></span> <span data-ttu-id="c363d-120">Dans ce cas, il s’agit de la colonne nommée , l’adresse IP pour laquelle vous souhaitez voir la liste des appareils qui lui ont `IP` été affectés.</span><span class="sxs-lookup"><span data-stu-id="c363d-120">In this case, it is the column named `IP`, the IP address for which you want to see a list of devices that have been assigned to it.</span></span> <span data-ttu-id="c363d-121">Il doit s’agit d’une adresse IP locale.</span><span class="sxs-lookup"><span data-stu-id="c363d-121">It should be a local IP address.</span></span> <span data-ttu-id="c363d-122">Les adresses IP externes ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c363d-122">External IP addresses are not supported.</span></span>
- <span data-ttu-id="c363d-123">**y**— Un deuxième paramètre facultatif est le , qui indique à la fonction d’obtenir les appareils affectés les plus `Timestamp` récents à partir d’un moment spécifique.</span><span class="sxs-lookup"><span data-stu-id="c363d-123">**y**—A second optional parameter is the `Timestamp`, which instructs the function to obtain the most recent assigned devices from a specific time.</span></span> <span data-ttu-id="c363d-124">Si elle n’est pas spécifiée, la fonction renvoie les derniers enregistrements disponibles.</span><span class="sxs-lookup"><span data-stu-id="c363d-124">If not specified, the function returns the latest available records.</span></span>

## <a name="example"></a><span data-ttu-id="c363d-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="c363d-125">Example</span></span>


### <a name="get-the-latest-devices-that-have-been-assigned-specific-ip-addresses"></a><span data-ttu-id="c363d-126">Obtenir les appareils les plus récents qui ont été affectés à des adresses IP spécifiques</span><span class="sxs-lookup"><span data-stu-id="c363d-126">Get the latest devices that have been assigned specific IP addresses</span></span>

```kusto
DeviceNetworkEvents 
| limit 100 
| project IP = LocalIP 
| invoke DeviceFromIP()
```

## <a name="related-topics"></a><span data-ttu-id="c363d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c363d-127">Related topics</span></span>
- [<span data-ttu-id="c363d-128">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="c363d-128">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="c363d-129">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="c363d-129">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="c363d-130">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="c363d-130">Understand the schema</span></span>](advanced-hunting-schema-tables.md)