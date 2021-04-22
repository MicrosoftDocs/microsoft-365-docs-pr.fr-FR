---
title: API obtenir la collection de groupes d'ordinateurs RBAC
description: Découvrez comment utiliser l'API get KB collection pour récupérer une collection de groupes d'appareils RBAC dans Microsoft Defender pour Endpoint.
keywords: api, api de graphique, api pris en charge, obtenir, RBAC, groupe
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
ms.date: 10/07/2018
ms.openlocfilehash: 18566025d79f02281c1d2c1509dd98f1e57879c2
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51932774"
---
# <a name="get-kb-collection-api"></a><span data-ttu-id="63791-104">API Obtenir une collection de ko</span><span class="sxs-lookup"><span data-stu-id="63791-104">Get KB collection API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="63791-105">**S'applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/p/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="63791-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/p/?linkid=2154037)</span></span>

- <span data-ttu-id="63791-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="63791-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="63791-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="63791-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


<span data-ttu-id="63791-108">Récupère une collection de groupes d'appareils RBAC.</span><span class="sxs-lookup"><span data-stu-id="63791-108">Retrieves a collection of RBAC device groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="63791-109">Autorisations</span><span class="sxs-lookup"><span data-stu-id="63791-109">Permissions</span></span>
<span data-ttu-id="63791-110">L'utilisateur a besoin d'autorisations de lecture.</span><span class="sxs-lookup"><span data-stu-id="63791-110">User needs read permissions.</span></span>

## <a name="http-request"></a><span data-ttu-id="63791-111">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="63791-111">HTTP request</span></span>
```
GET /testwdatppreview/machinegroups
```

## <a name="request-headers"></a><span data-ttu-id="63791-112">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="63791-112">Request headers</span></span>

<span data-ttu-id="63791-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="63791-113">Header</span></span> | <span data-ttu-id="63791-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="63791-114">Value</span></span> 
:---|:---
<span data-ttu-id="63791-115">Autorisation</span><span class="sxs-lookup"><span data-stu-id="63791-115">Authorization</span></span> | <span data-ttu-id="63791-116">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="63791-116">Bearer {token}.</span></span> <span data-ttu-id="63791-117">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="63791-117">**Required**.</span></span>
<span data-ttu-id="63791-118">Type de contenu</span><span class="sxs-lookup"><span data-stu-id="63791-118">Content type</span></span> | <span data-ttu-id="63791-119">application/json</span><span class="sxs-lookup"><span data-stu-id="63791-119">application/json</span></span>

## <a name="request-body"></a><span data-ttu-id="63791-120">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="63791-120">Request body</span></span>
<span data-ttu-id="63791-121">Vide</span><span class="sxs-lookup"><span data-stu-id="63791-121">Empty</span></span>

## <a name="response"></a><span data-ttu-id="63791-122">Réponse</span><span class="sxs-lookup"><span data-stu-id="63791-122">Response</span></span>
<span data-ttu-id="63791-123">En cas de réussite : 200 - OK.</span><span class="sxs-lookup"><span data-stu-id="63791-123">If successful - 200 OK.</span></span>

## <a name="example"></a><span data-ttu-id="63791-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="63791-124">Example</span></span>

<span data-ttu-id="63791-125">**Demande**</span><span class="sxs-lookup"><span data-stu-id="63791-125">**Request**</span></span>

<span data-ttu-id="63791-126">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="63791-126">Here is an example of the request.</span></span>

```
GET https://graph.microsoft.com/testwdatppreview/machinegroups
Content-type: application/json
```

<span data-ttu-id="63791-127">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="63791-127">**Response**</span></span>

<span data-ttu-id="63791-128">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="63791-128">Here is an example of the response.</span></span>
<span data-ttu-id="63791-129">L'ID de champ contient **l'ID** du groupe d'appareils et est égal au champ **rbacGroupId** dans les informations des appareils.</span><span class="sxs-lookup"><span data-stu-id="63791-129">Field id contains device group **id** and equal to field **rbacGroupId** in devices info.</span></span> <span data-ttu-id="63791-130">Le **champ non regroupé** n'est vrai que pour un seul groupe pour tous les appareils qui n'ont été affectés à aucun groupe.</span><span class="sxs-lookup"><span data-stu-id="63791-130">Field **ungrouped** is true only for one group for all devices that have not been assigned to any group.</span></span> <span data-ttu-id="63791-131">Comme d'habitude, ce groupe a le nom « UnassignedGroup ».</span><span class="sxs-lookup"><span data-stu-id="63791-131">This group as usual has name "UnassignedGroup".</span></span>

```
HTTP/1.1 200 OK
Content-type: application/json
{
    "@odata.context":"https://graph.microsoft.com/testwdatppreview/$metadata#MachineGroups",
    "@odata.count":7,
    "value":[
        {
            "id":86,
            "name":"UnassignedGroup",
            "description":"",
            "ungrouped":true},
        …
}
```
