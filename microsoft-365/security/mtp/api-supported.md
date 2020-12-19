---
title: API Microsoft 365 Defender prises en charge
description: API Microsoft 365 Defender prises en charge
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
ms.openlocfilehash: dbb7613dae3755b0fb794a3d68b5b424d765cc62
ms.sourcegitcommit: d6b1da2e12d55f69e4353289e90f5ae2f60066d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "49719321"
---
# <a name="supported-microsoft-365-defender-apis"></a><span data-ttu-id="80b8d-104">API Microsoft 365 Defender prises en charge</span><span class="sxs-lookup"><span data-stu-id="80b8d-104">Supported Microsoft 365 Defender APIs</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="80b8d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="80b8d-105">**Applies to:**</span></span>
- <span data-ttu-id="80b8d-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="80b8d-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="80b8d-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="80b8d-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="80b8d-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="80b8d-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

## <a name="list-of-available-apis"></a><span data-ttu-id="80b8d-109">Liste des API disponibles</span><span class="sxs-lookup"><span data-stu-id="80b8d-109">List of available APIs</span></span>

<span data-ttu-id="80b8d-110">Article</span><span class="sxs-lookup"><span data-stu-id="80b8d-110">Article</span></span> | <span data-ttu-id="80b8d-111">Description</span><span class="sxs-lookup"><span data-stu-id="80b8d-111">Description</span></span>
-|-
[<span data-ttu-id="80b8d-112">API de recherche avancée de menaces</span><span class="sxs-lookup"><span data-stu-id="80b8d-112">Advanced Hunting API</span></span>](api-advanced-hunting.md) | <span data-ttu-id="80b8d-113">Exécuter des requêtes de chasse avancées.</span><span class="sxs-lookup"><span data-stu-id="80b8d-113">Run Advanced Hunting queries.</span></span>
[<span data-ttu-id="80b8d-114">API d’incident</span><span class="sxs-lookup"><span data-stu-id="80b8d-114">Incident APIs</span></span>](api-incident.md) | <span data-ttu-id="80b8d-115">Répertorier et mettre à jour les incidents, ainsi que d’autres tâches pratiques.</span><span class="sxs-lookup"><span data-stu-id="80b8d-115">List and update incidents, along with other practical tasks.</span></span>

### <a name="endpoint-uris"></a><span data-ttu-id="80b8d-116">URI de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="80b8d-116">Endpoint URIs</span></span>

<span data-ttu-id="80b8d-117">L’URI de base pour les deux API principales est : https://api.security.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="80b8d-117">The base URI for both of the main APIs is: https://api.security.microsoft.com.</span></span> <span data-ttu-id="80b8d-118">Pour de meilleures performances, utilisez un serveur plus près de votre géolocalisation :</span><span class="sxs-lookup"><span data-stu-id="80b8d-118">For better performance, use a server closer to your geolocation:</span></span>

- <span data-ttu-id="80b8d-119">États-Unis : api-us.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="80b8d-119">The United States: api-us.security.microsoft.com</span></span>
- <span data-ttu-id="80b8d-120">Europe : api-eu.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="80b8d-120">Europe: api-eu.security.microsoft.com</span></span>
- <span data-ttu-id="80b8d-121">Royaume-Uni : api-uk.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="80b8d-121">The United Kingdom: api-uk.security.microsoft.com</span></span>

<span data-ttu-id="80b8d-122">Les jetons peuvent être obtenus en accédant à https://api.security.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="80b8d-122">Tokens can be acquired by accessing https://api.security.microsoft.com.</span></span>

<span data-ttu-id="80b8d-123">Toutes les API sur le `/api` chemin d’accès utilisent le protocole [OData](https://docs.microsoft.com/odata/overview) , par exemple, https://api.security.microsoft.com/api/incidents .</span><span class="sxs-lookup"><span data-stu-id="80b8d-123">All APIs along the `/api` path use the [OData](https://docs.microsoft.com/odata/overview) Protocol; for example, https://api.security.microsoft.com/api/incidents.</span></span>

## <a name="related-articles"></a><span data-ttu-id="80b8d-124">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="80b8d-124">Related articles</span></span>

- [<span data-ttu-id="80b8d-125">Vue d’ensemble des API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="80b8d-125">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="80b8d-126">Accéder aux API de protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="80b8d-126">Access the Microsoft Threat Protection APIs</span></span>](api-access.md)
- [<span data-ttu-id="80b8d-127">En savoir plus sur les limites d’API et la gestion des licences</span><span class="sxs-lookup"><span data-stu-id="80b8d-127">Learn about API limits and licensing</span></span>](api-terms.md)
- [<span data-ttu-id="80b8d-128">Comprendre les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="80b8d-128">Understand error codes</span></span>](api-error-codes.md)
