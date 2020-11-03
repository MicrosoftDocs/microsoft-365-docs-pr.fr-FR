---
title: API Microsoft 365 Defender prises en charge
description: API Microsoft 365 Defender prises en charge
keywords: MTP, API, API
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: b7c0accf2d649d4ad6177260294922ee17783f2c
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48844959"
---
# <a name="supported-microsoft-365-defender-apis"></a><span data-ttu-id="a14d3-104">API Microsoft 365 Defender prises en charge</span><span class="sxs-lookup"><span data-stu-id="a14d3-104">Supported Microsoft 365 Defender APIs</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="a14d3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a14d3-105">**Applies to:**</span></span>
- <span data-ttu-id="a14d3-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a14d3-106">Microsoft 365 Defender</span></span>

>[!IMPORTANT] 
><span data-ttu-id="a14d3-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="a14d3-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a14d3-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="a14d3-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>


### <a name="end-point-uris"></a><span data-ttu-id="a14d3-109">URI de point de terminaison :</span><span class="sxs-lookup"><span data-stu-id="a14d3-109">End Point URIs:</span></span>

- <span data-ttu-id="a14d3-110">L’URI de la base de service est : https://api.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a14d3-110">The service base URI is: https://api.security.microsoft.com</span></span> <br>

>[!NOTE]
><span data-ttu-id="a14d3-111">Pour de meilleures performances, vous pouvez utiliser le serveur plus près de votre emplacement géographique :</span><span class="sxs-lookup"><span data-stu-id="a14d3-111">For better performance, you can use server closer to your Geo location:</span></span>
> - <span data-ttu-id="a14d3-112">api-us.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a14d3-112">api-us.security.microsoft.com</span></span>
> - <span data-ttu-id="a14d3-113">api-eu.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a14d3-113">api-eu.security.microsoft.com</span></span>
> - <span data-ttu-id="a14d3-114">api-uk.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a14d3-114">api-uk.security.microsoft.com</span></span>

 - <span data-ttu-id="a14d3-115">La ressource pour l’acquisition de jetons doit être : https://api.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a14d3-115">The resource for token acquisition should be: https://api.security.microsoft.com</span></span>

 - <span data-ttu-id="a14d3-116">Toutes les API sous ```/api``` chemin d’accès sont des API OData.</span><span class="sxs-lookup"><span data-stu-id="a14d3-116">All the APIs under ```/api``` path are OData APIs.</span></span> <span data-ttu-id="a14d3-117">p ```https://api.security.microsoft.com/api/incidents```</span><span class="sxs-lookup"><span data-stu-id="a14d3-117">e.g. ```https://api.security.microsoft.com/api/incidents```</span></span>

## <a name="list-of-available-apis"></a><span data-ttu-id="a14d3-118">Liste des API disponibles :</span><span class="sxs-lookup"><span data-stu-id="a14d3-118">List of available APIs:</span></span>

<span data-ttu-id="a14d3-119">Rubrique</span><span class="sxs-lookup"><span data-stu-id="a14d3-119">Topic</span></span> | <span data-ttu-id="a14d3-120">Description</span><span class="sxs-lookup"><span data-stu-id="a14d3-120">Description</span></span>
:---|:---
[<span data-ttu-id="a14d3-121">API de recherche avancée de menaces</span><span class="sxs-lookup"><span data-stu-id="a14d3-121">Advanced Hunting API</span></span>](api-advanced-hunting.md) | <span data-ttu-id="a14d3-122">Exécuter des requêtes de chasse avancées à partir de l’API.</span><span class="sxs-lookup"><span data-stu-id="a14d3-122">Run Advanced Hunting queries from API.</span></span>
[<span data-ttu-id="a14d3-123">API d’incident</span><span class="sxs-lookup"><span data-stu-id="a14d3-123">Incident APIs</span></span>](api-incident.md) | <span data-ttu-id="a14d3-124">Exécutez des appels d’API liés aux incidents, tels que : répertorier les incidents, mettre à jour l’incident et plus encore.</span><span class="sxs-lookup"><span data-stu-id="a14d3-124">Run incident related API calls such as: list incidents, update incident and more.</span></span>
