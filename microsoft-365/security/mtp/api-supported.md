---
title: API Microsoft 365 Defender prises en charge
description: API Microsoft 365 Defender prises en charge
keywords: MTP, API, api
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
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
ms.technology: m365d
ms.openlocfilehash: ee03e5a255a88c084403842e7bf0319c06c0517b
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49926197"
---
# <a name="supported-microsoft-365-defender-apis"></a><span data-ttu-id="b81b2-104">API Microsoft 365 Defender prises en charge</span><span class="sxs-lookup"><span data-stu-id="b81b2-104">Supported Microsoft 365 Defender APIs</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="b81b2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b81b2-105">**Applies to:**</span></span>
- <span data-ttu-id="b81b2-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b81b2-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b81b2-107">Certaines informations concernent des produits pré-publiés qui peuvent être considérablement modifiés avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="b81b2-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b81b2-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="b81b2-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

## <a name="list-of-available-apis"></a><span data-ttu-id="b81b2-109">Liste des API disponibles</span><span class="sxs-lookup"><span data-stu-id="b81b2-109">List of available APIs</span></span>

<span data-ttu-id="b81b2-110">Article</span><span class="sxs-lookup"><span data-stu-id="b81b2-110">Article</span></span> | <span data-ttu-id="b81b2-111">Description</span><span class="sxs-lookup"><span data-stu-id="b81b2-111">Description</span></span>
-|-
[<span data-ttu-id="b81b2-112">API de recherche avancée de menaces</span><span class="sxs-lookup"><span data-stu-id="b81b2-112">Advanced Hunting API</span></span>](api-advanced-hunting.md) | <span data-ttu-id="b81b2-113">Exécutez des requêtes de recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="b81b2-113">Run Advanced Hunting queries.</span></span>
[<span data-ttu-id="b81b2-114">API d’incident</span><span class="sxs-lookup"><span data-stu-id="b81b2-114">Incident APIs</span></span>](api-incident.md) | <span data-ttu-id="b81b2-115">Liste et mise à jour des incidents, ainsi que d’autres tâches pratiques.</span><span class="sxs-lookup"><span data-stu-id="b81b2-115">List and update incidents, along with other practical tasks.</span></span>

### <a name="endpoint-uris"></a><span data-ttu-id="b81b2-116">URL de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b81b2-116">Endpoint URIs</span></span>

<span data-ttu-id="b81b2-117">L’URI de base pour les deux API principales est : https://api.security.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="b81b2-117">The base URI for both of the main APIs is: https://api.security.microsoft.com.</span></span> <span data-ttu-id="b81b2-118">Pour de meilleures performances, utilisez un serveur plus proche de votre géolocalisation :</span><span class="sxs-lookup"><span data-stu-id="b81b2-118">For better performance, use a server closer to your geolocation:</span></span>

- <span data-ttu-id="b81b2-119">États-Unis : api-us.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b81b2-119">The United States: api-us.security.microsoft.com</span></span>
- <span data-ttu-id="b81b2-120">Europe : api-eu.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b81b2-120">Europe: api-eu.security.microsoft.com</span></span>
- <span data-ttu-id="b81b2-121">Royaume-Uni : api-uk.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b81b2-121">The United Kingdom: api-uk.security.microsoft.com</span></span>

<span data-ttu-id="b81b2-122">Les jetons peuvent être acquis en accédant à https://api.security.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="b81b2-122">Tokens can be acquired by accessing https://api.security.microsoft.com.</span></span>

<span data-ttu-id="b81b2-123">Toutes les API le long du `/api` chemin d’accès utilisent [le protocole OData](https://docs.microsoft.com/odata/overview) ; par exemple, https://api.security.microsoft.com/api/incidents .</span><span class="sxs-lookup"><span data-stu-id="b81b2-123">All APIs along the `/api` path use the [OData](https://docs.microsoft.com/odata/overview) Protocol; for example, https://api.security.microsoft.com/api/incidents.</span></span>

## <a name="related-articles"></a><span data-ttu-id="b81b2-124">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="b81b2-124">Related articles</span></span>

- [<span data-ttu-id="b81b2-125">Présentation des API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b81b2-125">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="b81b2-126">Accéder aux API de protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="b81b2-126">Access the Microsoft Threat Protection APIs</span></span>](api-access.md)
- [<span data-ttu-id="b81b2-127">En savoir plus sur les limites d’API et les licences</span><span class="sxs-lookup"><span data-stu-id="b81b2-127">Learn about API limits and licensing</span></span>](api-terms.md)
- [<span data-ttu-id="b81b2-128">Comprendre les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b81b2-128">Understand error codes</span></span>](api-error-codes.md)
