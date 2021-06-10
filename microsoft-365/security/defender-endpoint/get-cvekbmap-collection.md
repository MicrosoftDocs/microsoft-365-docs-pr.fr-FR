---
title: API de carte Get CVE-KB
description: Découvrez comment utiliser l’API obtenir le plan CVE-KB pour récupérer une carte de CVE vers les détails de la base de données et CVE dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, cve, kb
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
ms.openlocfilehash: 85c4d82f07354193fb1e997abb98dbdaa02dc8ef
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166582"
---
# <a name="get-cve-kb-map-api"></a><span data-ttu-id="50c96-104">API de carte Get CVE-KB</span><span class="sxs-lookup"><span data-stu-id="50c96-104">Get CVE-KB map API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="50c96-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="50c96-105">**Applies to:**</span></span>
- [<span data-ttu-id="50c96-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="50c96-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="50c96-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="50c96-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="50c96-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="50c96-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="50c96-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="50c96-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

<span data-ttu-id="50c96-110">Extrait une carte de CVE vers les détails de la ko et de la CVE.</span><span class="sxs-lookup"><span data-stu-id="50c96-110">Retrieves a map of CVE's to KB's and CVE details.</span></span>

## <a name="permissions"></a><span data-ttu-id="50c96-111">Autorisations</span><span class="sxs-lookup"><span data-stu-id="50c96-111">Permissions</span></span>
<span data-ttu-id="50c96-112">L’utilisateur a besoin d’autorisations de lecture.</span><span class="sxs-lookup"><span data-stu-id="50c96-112">User needs read permissions.</span></span>

## <a name="http-request"></a><span data-ttu-id="50c96-113">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="50c96-113">HTTP request</span></span>
```
GET /testwdatppreview/cvekbmap
```

## <a name="request-headers"></a><span data-ttu-id="50c96-114">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="50c96-114">Request headers</span></span>

<span data-ttu-id="50c96-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="50c96-115">Header</span></span> | <span data-ttu-id="50c96-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="50c96-116">Value</span></span> 
:---|:---
<span data-ttu-id="50c96-117">Autorisation</span><span class="sxs-lookup"><span data-stu-id="50c96-117">Authorization</span></span> | <span data-ttu-id="50c96-118">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="50c96-118">Bearer {token}.</span></span> <span data-ttu-id="50c96-119">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="50c96-119">**Required**.</span></span>
<span data-ttu-id="50c96-120">Type de contenu</span><span class="sxs-lookup"><span data-stu-id="50c96-120">Content type</span></span> | <span data-ttu-id="50c96-121">application/json</span><span class="sxs-lookup"><span data-stu-id="50c96-121">application/json</span></span>

## <a name="request-body"></a><span data-ttu-id="50c96-122">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="50c96-122">Request body</span></span>
<span data-ttu-id="50c96-123">Vide</span><span class="sxs-lookup"><span data-stu-id="50c96-123">Empty</span></span>

## <a name="response"></a><span data-ttu-id="50c96-124">Réponse</span><span class="sxs-lookup"><span data-stu-id="50c96-124">Response</span></span>
<span data-ttu-id="50c96-125">En cas de réussite et si la carte existe : 200 - OK.</span><span class="sxs-lookup"><span data-stu-id="50c96-125">If successful and map exists - 200 OK.</span></span>

## <a name="example"></a><span data-ttu-id="50c96-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="50c96-126">Example</span></span>

<span data-ttu-id="50c96-127">**Demande**</span><span class="sxs-lookup"><span data-stu-id="50c96-127">**Request**</span></span>

<span data-ttu-id="50c96-128">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="50c96-128">Here is an example of the request.</span></span>

```http
GET https://graph.microsoft.com/testwdatppreview/CveKbMap
```

<span data-ttu-id="50c96-129">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="50c96-129">**Response**</span></span>

<span data-ttu-id="50c96-130">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="50c96-130">Here is an example of the response.</span></span>

```json
{
    "@odata.context":"https://graph.microsoft.com/testwdatppreview/$metadata#CveKbMap",
    "@odata.count": 4168,
    "value": [
        {
            "cveKbId": "CVE-2015-2482-3097617",
            "cveId": "CVE-2015-2482",
            "kbId":"3097617",
            "title": "Cumulative Security Update for Internet Explorer",
            "severity": "Critical"
        },
    …
}

```
