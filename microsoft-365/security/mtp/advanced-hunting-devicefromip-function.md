---
title: Fonction DeviceFromIP () dans la chasse avancée pour Microsoft 365 Defender
description: Découvrez comment utiliser la fonction DeviceFromIP () pour obtenir les périphériques auxquels une adresse IP spécifique a été attribuée.
keywords: chasse de menace, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, appareil, devicefromIP, fonction, enrichissement
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: maccruz
author: schmurky
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.openlocfilehash: 65409dd93f3703f1af115178c4cd9fa470fb7497
ms.sourcegitcommit: 25ac2736a66bb72c0d574c3fbde7472ac98d5321
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/31/2020
ms.locfileid: "49741107"
---
# <a name="devicefromip"></a><span data-ttu-id="d56ce-104">DeviceFromIP()</span><span class="sxs-lookup"><span data-stu-id="d56ce-104">DeviceFromIP()</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="d56ce-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d56ce-105">**Applies to:**</span></span>
- <span data-ttu-id="d56ce-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d56ce-106">Microsoft 365 Defender</span></span>


[!INCLUDE [Prerelease information](../includes/prerelease.md)]


<span data-ttu-id="d56ce-107">Utilisez la `DeviceFromIP()` fonction dans vos requêtes de [chasse avancée](advanced-hunting-overview.md) pour obtenir rapidement la liste des périphériques affectés à une adresse IP spécifique à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d56ce-107">Use the `DeviceFromIP()` function in your [advanced hunting](advanced-hunting-overview.md) queries to quickly obtain the list of devices that have been assigned to a certain IP address at a given point in time.</span></span> 

<span data-ttu-id="d56ce-108">Cette fonction renvoie une table avec les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d56ce-108">This function returns a table with the following columns:</span></span>

| <span data-ttu-id="d56ce-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="d56ce-109">Column</span></span> | <span data-ttu-id="d56ce-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="d56ce-110">Data type</span></span> | <span data-ttu-id="d56ce-111">Description</span><span class="sxs-lookup"><span data-stu-id="d56ce-111">Description</span></span> |
|------------|-------------|-------------|
| `IP` | <span data-ttu-id="d56ce-112">string</span><span class="sxs-lookup"><span data-stu-id="d56ce-112">string</span></span> | <span data-ttu-id="d56ce-113">Adresse IP</span><span class="sxs-lookup"><span data-stu-id="d56ce-113">IP address</span></span>  |
| `DeviceId` | <span data-ttu-id="d56ce-114">chaîne</span><span class="sxs-lookup"><span data-stu-id="d56ce-114">string</span></span> | <span data-ttu-id="d56ce-115">Identificateur unique de l’appareil dans le service</span><span class="sxs-lookup"><span data-stu-id="d56ce-115">Unique identifier for the device in the service</span></span> |


## <a name="syntax"></a><span data-ttu-id="d56ce-116">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d56ce-116">Syntax</span></span>

```kusto
invoke DeviceFromIP()
```

## <a name="arguments"></a><span data-ttu-id="d56ce-117">Arguments</span><span class="sxs-lookup"><span data-stu-id="d56ce-117">Arguments</span></span>

<span data-ttu-id="d56ce-118">Cette fonction est appelée dans le cadre d’une requête.</span><span class="sxs-lookup"><span data-stu-id="d56ce-118">This function is invoked as part of a query.</span></span>

- <span data-ttu-id="d56ce-119">**x**— le premier paramètre est généralement déjà une colonne dans la requête.</span><span class="sxs-lookup"><span data-stu-id="d56ce-119">**x**—The first parameter is typically already a column in the query.</span></span> <span data-ttu-id="d56ce-120">Dans ce cas, il s’agit de la colonne nommée `IP` , de l’adresse IP pour laquelle vous souhaitez afficher la liste des périphériques qui lui ont été attribués.</span><span class="sxs-lookup"><span data-stu-id="d56ce-120">In this case, it is the column named `IP`, the IP address for which you want to see a list of devices that have been assigned to it.</span></span> <span data-ttu-id="d56ce-121">Il doit s’agir d’une adresse IP locale.</span><span class="sxs-lookup"><span data-stu-id="d56ce-121">It should be a local IP address.</span></span> <span data-ttu-id="d56ce-122">Les adresses IP externes ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d56ce-122">External IP addresses are not supported.</span></span>
- <span data-ttu-id="d56ce-123">**y**— un deuxième paramètre facultatif est l' `Timestamp` , qui demande à la fonction d’obtenir les appareils affectés les plus récents à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d56ce-123">**y**—A second optional parameter is the `Timestamp`, which instructs the function to obtain the most recent assigned devices from a specific time.</span></span> <span data-ttu-id="d56ce-124">Si ce n’est pas spécifié, la fonction renvoie les derniers enregistrements disponibles.</span><span class="sxs-lookup"><span data-stu-id="d56ce-124">If not specified, the function returns the latest available records.</span></span>

## <a name="example"></a><span data-ttu-id="d56ce-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="d56ce-125">Example</span></span>


### <a name="get-the-latest-devices-that-have-been-assigned-specific-ip-addresses"></a><span data-ttu-id="d56ce-126">Obtenir les derniers appareils auxquels des adresses IP spécifiques ont été affectées</span><span class="sxs-lookup"><span data-stu-id="d56ce-126">Get the latest devices that have been assigned specific IP addresses</span></span>

```kusto
DeviceNetworkEvents 
| limit 100 
| project IP = LocalIP 
| invoke DeviceFromIP()
```

## <a name="related-topics"></a><span data-ttu-id="d56ce-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d56ce-127">Related topics</span></span>
- [<span data-ttu-id="d56ce-128">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="d56ce-128">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="d56ce-129">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="d56ce-129">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="d56ce-130">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="d56ce-130">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
