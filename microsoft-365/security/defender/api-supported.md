---
title: API Microsoft 365 Defender prises en charge
description: API Microsoft 365 Defender prises en charge
keywords: Microsoft 365 Defender, API, api
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: c10b2863503a5bda829cbf67379a606b687ac2e3
ms.sourcegitcommit: e8f5d88f0fe54620308d3bec05263568f9da2931
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52730941"
---
# <a name="supported-microsoft-365-defender-apis"></a><span data-ttu-id="26eb0-104">API Microsoft 365 Defender prises en charge</span><span class="sxs-lookup"><span data-stu-id="26eb0-104">Supported Microsoft 365 Defender APIs</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="26eb0-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="26eb0-105">**Applies to:**</span></span>
- <span data-ttu-id="26eb0-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="26eb0-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="26eb0-107">Certaines informations ont trait à un produit préalablement publié, qui peut être modifié de manière significative avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="26eb0-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="26eb0-108">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="26eb0-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

## <a name="list-of-available-apis"></a><span data-ttu-id="26eb0-109">Liste des API disponibles</span><span class="sxs-lookup"><span data-stu-id="26eb0-109">List of available APIs</span></span>

<span data-ttu-id="26eb0-110">Article</span><span class="sxs-lookup"><span data-stu-id="26eb0-110">Article</span></span> | <span data-ttu-id="26eb0-111">Description</span><span class="sxs-lookup"><span data-stu-id="26eb0-111">Description</span></span>
-|-
[<span data-ttu-id="26eb0-112">API de recherche avancée de menaces</span><span class="sxs-lookup"><span data-stu-id="26eb0-112">Advanced Hunting API</span></span>](api-advanced-hunting.md) | <span data-ttu-id="26eb0-113">Exécutez des requêtes de recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="26eb0-113">Run Advanced Hunting queries.</span></span>
[<span data-ttu-id="26eb0-114">API d’incident</span><span class="sxs-lookup"><span data-stu-id="26eb0-114">Incident APIs</span></span>](api-incident.md) | <span data-ttu-id="26eb0-115">Liste et mise à jour des incidents, ainsi que d’autres tâches pratiques.</span><span class="sxs-lookup"><span data-stu-id="26eb0-115">List and update incidents, along with other practical tasks.</span></span>
<span data-ttu-id="26eb0-116">[API de diffusion en](../defender-endpoint/raw-data-export.md) continu (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="26eb0-116">[Streaming API](../defender-endpoint/raw-data-export.md) (Preview)</span></span> | <span data-ttu-id="26eb0-117">Expédiez des alertes et des événements en temps réel à mesure qu’ils se produisent dans un flux de données unique.</span><span class="sxs-lookup"><span data-stu-id="26eb0-117">Ship real-time events and alerts as they occur in a single data stream.</span></span>

### <a name="endpoint-uris"></a><span data-ttu-id="26eb0-118">URL de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="26eb0-118">Endpoint URIs</span></span>

<span data-ttu-id="26eb0-119">L’URI de base pour les deux API principales est : https://api.security.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="26eb0-119">The base URI for both of the main APIs is: https://api.security.microsoft.com.</span></span> <span data-ttu-id="26eb0-120">Pour de meilleures performances, utilisez un serveur plus proche de votre géolocalisation :</span><span class="sxs-lookup"><span data-stu-id="26eb0-120">For better performance, use a server closer to your geolocation:</span></span>

- <span data-ttu-id="26eb0-121">États-Unis : api-us.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="26eb0-121">The United States: api-us.security.microsoft.com</span></span>
- <span data-ttu-id="26eb0-122">Europe : api-eu.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="26eb0-122">Europe: api-eu.security.microsoft.com</span></span>
- <span data-ttu-id="26eb0-123">Royaume-Uni : api-uk.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="26eb0-123">The United Kingdom: api-uk.security.microsoft.com</span></span>

<span data-ttu-id="26eb0-124">Les jetons peuvent être acquis en accédant à https://api.security.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="26eb0-124">Tokens can be acquired by accessing https://api.security.microsoft.com.</span></span>

<span data-ttu-id="26eb0-125">Toutes les API le long du `/api` chemin d’accès utilisent le [protocole OData](/odata/overview) ; par exemple, https://api.security.microsoft.com/api/incidents .</span><span class="sxs-lookup"><span data-stu-id="26eb0-125">All APIs along the `/api` path use the [OData](/odata/overview) Protocol; for example, https://api.security.microsoft.com/api/incidents.</span></span>

## <a name="related-articles"></a><span data-ttu-id="26eb0-126">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="26eb0-126">Related articles</span></span>

- [<span data-ttu-id="26eb0-127">Microsoft 365 Vue d’ensemble des API Defender</span><span class="sxs-lookup"><span data-stu-id="26eb0-127">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="26eb0-128">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="26eb0-128">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="26eb0-129">API de diffusion en continu</span><span class="sxs-lookup"><span data-stu-id="26eb0-129">Streaming API</span></span>](../defender-endpoint/raw-data-export.md)
- [<span data-ttu-id="26eb0-130">En savoir plus sur les limites d’API et les licences</span><span class="sxs-lookup"><span data-stu-id="26eb0-130">Learn about API limits and licensing</span></span>](api-terms.md)
- [<span data-ttu-id="26eb0-131">Comprendre les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="26eb0-131">Understand error codes</span></span>](api-error-codes.md)
