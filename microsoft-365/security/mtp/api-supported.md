---
title: API de protection Microsoft contre les menaces prises en charge
description: API de protection Microsoft contre les menaces prises en charge
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
ms.openlocfilehash: 49fa182a6142748ca7769411fe74389f365ba75f
ms.sourcegitcommit: 9a275a13af3e063e80ce1bd3cd8142a095db92d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2020
ms.locfileid: "47650270"
---
# <a name="supported-microsoft-threat-protection-apis"></a><span data-ttu-id="e2f0d-104">API de protection Microsoft contre les menaces prises en charge</span><span class="sxs-lookup"><span data-stu-id="e2f0d-104">Supported Microsoft Threat Protection APIs</span></span> 
<span data-ttu-id="e2f0d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e2f0d-105">**Applies to:**</span></span>
- <span data-ttu-id="e2f0d-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="e2f0d-106">Microsoft Threat Protection</span></span>

>[!IMPORTANT] 
><span data-ttu-id="e2f0d-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e2f0d-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>


### <a name="end-point-uris"></a><span data-ttu-id="e2f0d-109">URI de point de terminaison :</span><span class="sxs-lookup"><span data-stu-id="e2f0d-109">End Point URIs:</span></span>

- <span data-ttu-id="e2f0d-110">L’URI de la base de service est : https://api.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="e2f0d-110">The service base URI is: https://api.security.microsoft.com</span></span> <br>

>[!NOTE]
><span data-ttu-id="e2f0d-111">Pour de meilleures performances, vous pouvez utiliser le serveur plus près de votre emplacement géographique :</span><span class="sxs-lookup"><span data-stu-id="e2f0d-111">For better performance, you can use server closer to your Geo location:</span></span>
> - <span data-ttu-id="e2f0d-112">api-us.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="e2f0d-112">api-us.security.microsoft.com</span></span>
> - <span data-ttu-id="e2f0d-113">api-eu.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="e2f0d-113">api-eu.security.microsoft.com</span></span>
> - <span data-ttu-id="e2f0d-114">api-uk.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="e2f0d-114">api-uk.security.microsoft.com</span></span>

 - <span data-ttu-id="e2f0d-115">La ressource pour l’acquisition de jetons doit être : https://api.security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="e2f0d-115">The resource for token acquisition should be: https://api.security.microsoft.com</span></span>

 - <span data-ttu-id="e2f0d-116">Toutes les API sous ```/api``` chemin d’accès sont des API OData.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-116">All the APIs under ```/api``` path are OData APIs.</span></span> <span data-ttu-id="e2f0d-117">p ```https://api.security.microsoft.com/api/incidents```</span><span class="sxs-lookup"><span data-stu-id="e2f0d-117">e.g. ```https://api.security.microsoft.com/api/incidents```</span></span>

## <a name="list-of-available-apis"></a><span data-ttu-id="e2f0d-118">Liste des API disponibles :</span><span class="sxs-lookup"><span data-stu-id="e2f0d-118">List of available APIs:</span></span>

<span data-ttu-id="e2f0d-119">Rubrique</span><span class="sxs-lookup"><span data-stu-id="e2f0d-119">Topic</span></span> | <span data-ttu-id="e2f0d-120">Description</span><span class="sxs-lookup"><span data-stu-id="e2f0d-120">Description</span></span>
:---|:---
[<span data-ttu-id="e2f0d-121">API de chasse avancée</span><span class="sxs-lookup"><span data-stu-id="e2f0d-121">Advanced Hunting API</span></span>](api-advanced-hunting.md) | <span data-ttu-id="e2f0d-122">Exécuter des requêtes de chasse avancées à partir de l’API.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-122">Run Advanced Hunting queries from API.</span></span>
[<span data-ttu-id="e2f0d-123">API d’incident</span><span class="sxs-lookup"><span data-stu-id="e2f0d-123">Incident APIs</span></span>](api-incident.md) | <span data-ttu-id="e2f0d-124">Exécutez des appels d’API liés aux incidents, tels que : répertorier les incidents, mettre à jour l’incident et plus encore.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-124">Run incident related API calls such as: list incidents, update incident and more.</span></span>
