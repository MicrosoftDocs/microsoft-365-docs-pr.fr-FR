---
title: API obtenir la collection d’états de sécurité des ordinateurs
description: Récupérez une collection d’états de sécurité d’appareil à l’aide de Microsoft Defender for Endpoint.
keywords: api, api de graphique, api pris en charge, obtenir, appareil, sécurité, état
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: w10
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
ms.openlocfilehash: 9dab4bdccc1fead5bc2cc5b9bdff8f2a45b6c8db
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51200364"
---
# <a name="get-machines-security-states-collection-api"></a><span data-ttu-id="8ed95-104">API obtenir la collection d’états de sécurité des ordinateurs</span><span class="sxs-lookup"><span data-stu-id="8ed95-104">Get Machines security states collection API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="8ed95-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="8ed95-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="8ed95-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="8ed95-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="8ed95-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="8ed95-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

<span data-ttu-id="8ed95-108">Récupère une collection d’états de sécurité des appareils.</span><span class="sxs-lookup"><span data-stu-id="8ed95-108">Retrieves a collection of devices security states.</span></span>

## <a name="permissions"></a><span data-ttu-id="8ed95-109">Autorisations</span><span class="sxs-lookup"><span data-stu-id="8ed95-109">Permissions</span></span>
<span data-ttu-id="8ed95-110">L’utilisateur a besoin d’autorisations de lecture.</span><span class="sxs-lookup"><span data-stu-id="8ed95-110">User needs read permissions.</span></span>

## <a name="http-request"></a><span data-ttu-id="8ed95-111">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="8ed95-111">HTTP request</span></span>
```
GET /testwdatppreview/machinesecuritystates
```

## <a name="request-headers"></a><span data-ttu-id="8ed95-112">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="8ed95-112">Request headers</span></span>

<span data-ttu-id="8ed95-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ed95-113">Header</span></span> | <span data-ttu-id="8ed95-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ed95-114">Value</span></span> 
:---|:---
<span data-ttu-id="8ed95-115">Autorisation</span><span class="sxs-lookup"><span data-stu-id="8ed95-115">Authorization</span></span> | <span data-ttu-id="8ed95-116">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="8ed95-116">Bearer {token}.</span></span> <span data-ttu-id="8ed95-117">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="8ed95-117">**Required**.</span></span>
<span data-ttu-id="8ed95-118">Type de contenu</span><span class="sxs-lookup"><span data-stu-id="8ed95-118">Content type</span></span> | <span data-ttu-id="8ed95-119">application/json</span><span class="sxs-lookup"><span data-stu-id="8ed95-119">application/json</span></span>

## <a name="request-body"></a><span data-ttu-id="8ed95-120">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="8ed95-120">Request body</span></span>
<span data-ttu-id="8ed95-121">Vide</span><span class="sxs-lookup"><span data-stu-id="8ed95-121">Empty</span></span>

## <a name="response"></a><span data-ttu-id="8ed95-122">Réponse</span><span class="sxs-lookup"><span data-stu-id="8ed95-122">Response</span></span>
<span data-ttu-id="8ed95-123">En cas de réussite : 200 - OK.</span><span class="sxs-lookup"><span data-stu-id="8ed95-123">If successful - 200 OK.</span></span>

## <a name="example"></a><span data-ttu-id="8ed95-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="8ed95-124">Example</span></span>

<span data-ttu-id="8ed95-125">**Demande**</span><span class="sxs-lookup"><span data-stu-id="8ed95-125">**Request**</span></span>

<span data-ttu-id="8ed95-126">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="8ed95-126">Here is an example of the request.</span></span>

```
GET https://graph.microsoft.com/testwdatppreview/machinesecuritystates
Content-type: application/json
```

<span data-ttu-id="8ed95-127">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="8ed95-127">**Response**</span></span>

<span data-ttu-id="8ed95-128">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="8ed95-128">Here is an example of the response.</span></span>
<span data-ttu-id="8ed95-129">*L’ID de* champ contient l’ID de l’appareil et est égal à l’ID *de* champ \* dans les informations sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="8ed95-129">Field *id* contains device id and equal to the field *id*\* in devices info.</span></span> 

```
HTTP/1.1 200 OK
Content-type: application/json
{
    "@odata.context":"https://graph.microsoft.com/testwdatppreview/$metadata#MachineSecurityStates",
    "@odata.count":444,
    "@odata.nextLink":"https://graph.microsoft.com/testwdatppreview/machinesecuritystates?$skiptoken=[continuation token]",
    "value":[
        {
            "id":"000050e1b4afeee3742489ede9ad7a3e16bbd9c4",
            "build":14393,
            "revision":2485,
            "architecture":"Amd64",
            "osVersion":"10.0.14393.2485.amd64fre.rs1_release.180827-1809",
            "propertiesRequireAttention":[
                "AntivirusNotReporting",
                "EdrImpairedCommunications"
            ]
        },
        …
    ]
}
```
