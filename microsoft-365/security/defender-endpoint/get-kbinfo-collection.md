---
title: API Obtenir une collection de ko
description: Récupérez une collection de bases de connaissances (Ko) et de détails de la Base de connaissances avec Microsoft Defender pour point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, kb
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: leonidzh
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ROBOTS: NOINDEX
ms.technology: mde
ms.openlocfilehash: 7becfc4a7246dc32aa244dc96ea423f5d31877f9
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166726"
---
# <a name="get-kb-collection-api"></a><span data-ttu-id="f5b95-104">API Obtenir une collection de ko</span><span class="sxs-lookup"><span data-stu-id="f5b95-104">Get KB collection API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f5b95-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f5b95-105">**Applies to:**</span></span>
- [<span data-ttu-id="f5b95-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f5b95-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="f5b95-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f5b95-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="f5b95-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="f5b95-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="f5b95-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f5b95-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

<span data-ttu-id="f5b95-110">Extrait une collection de détails de la Ko et de la Ko.</span><span class="sxs-lookup"><span data-stu-id="f5b95-110">Retrieves a collection of KB's and KB details.</span></span>

## <a name="permissions"></a><span data-ttu-id="f5b95-111">Autorisations</span><span class="sxs-lookup"><span data-stu-id="f5b95-111">Permissions</span></span>
<span data-ttu-id="f5b95-112">L’utilisateur a besoin d’autorisations de lecture.</span><span class="sxs-lookup"><span data-stu-id="f5b95-112">User needs read permissions.</span></span>

## <a name="http-request"></a><span data-ttu-id="f5b95-113">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="f5b95-113">HTTP request</span></span>
```
GET /testwdatppreview/kbinfo
```

## <a name="request-headers"></a><span data-ttu-id="f5b95-114">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="f5b95-114">Request headers</span></span>

<span data-ttu-id="f5b95-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5b95-115">Header</span></span> | <span data-ttu-id="f5b95-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5b95-116">Value</span></span> 
:---|:---
<span data-ttu-id="f5b95-117">Autorisation</span><span class="sxs-lookup"><span data-stu-id="f5b95-117">Authorization</span></span> | <span data-ttu-id="f5b95-118">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="f5b95-118">Bearer {token}.</span></span> <span data-ttu-id="f5b95-119">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="f5b95-119">**Required**.</span></span>
<span data-ttu-id="f5b95-120">Type de contenu</span><span class="sxs-lookup"><span data-stu-id="f5b95-120">Content type</span></span> | <span data-ttu-id="f5b95-121">application/json</span><span class="sxs-lookup"><span data-stu-id="f5b95-121">application/json</span></span>

## <a name="request-body"></a><span data-ttu-id="f5b95-122">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="f5b95-122">Request body</span></span>
<span data-ttu-id="f5b95-123">Vide</span><span class="sxs-lookup"><span data-stu-id="f5b95-123">Empty</span></span>

## <a name="response"></a><span data-ttu-id="f5b95-124">Réponse</span><span class="sxs-lookup"><span data-stu-id="f5b95-124">Response</span></span>
<span data-ttu-id="f5b95-125">En cas de réussite : 200 - OK.</span><span class="sxs-lookup"><span data-stu-id="f5b95-125">If successful - 200 OK.</span></span>

## <a name="example"></a><span data-ttu-id="f5b95-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="f5b95-126">Example</span></span>

<span data-ttu-id="f5b95-127">**Demande**</span><span class="sxs-lookup"><span data-stu-id="f5b95-127">**Request**</span></span>

<span data-ttu-id="f5b95-128">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="f5b95-128">Here is an example of the request.</span></span>

```http
GET https://graph.microsoft.com/testwdatppreview/KbInfo
```

<span data-ttu-id="f5b95-129">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="f5b95-129">**Response**</span></span>

<span data-ttu-id="f5b95-130">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="f5b95-130">Here is an example of the response.</span></span>

```json
{
    "@odata.context": "https://graph.microsoft.com/testwdatppreview/$metadata#KbInfo",
    "@odata.count": 271,
    "value":[
        {
            "id": "KB3097617 (10240.16549) Amd64",
            "release": "KB3097617 (10240.16549)",
            "publishingDate": "2015-10-16T21:00:00Z",
            "version": "10.0.10240.16549",
            "architecture": "Amd64"
        },
        …
}
```
