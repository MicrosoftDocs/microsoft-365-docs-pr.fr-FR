---
title: API Obtenir les informations utilisateur
description: Découvrez comment utiliser l’API Obtenir des informations utilisateur pour récupérer une entité Utilisateur par clé ou nom d’utilisateur dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, utilisateur, informations utilisateur
search.product: eADQiWindows 10XVcnh
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: 1c5b8fa6e0f1fd887c857bd4e6451a5e59b708af
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51198540"
---
# <a name="get-user-information-api"></a><span data-ttu-id="fc877-104">API Obtenir les informations utilisateur</span><span class="sxs-lookup"><span data-stu-id="fc877-104">Get user information API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="fc877-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="fc877-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="fc877-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="fc877-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="fc877-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="fc877-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

> <span data-ttu-id="fc877-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="fc877-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="fc877-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="fc877-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)
<span data-ttu-id="fc877-110">Récupérer une entité User par clé (nom d’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="fc877-110">Retrieve a User entity by key (user name).</span></span>

## <a name="permissions"></a><span data-ttu-id="fc877-111">Autorisations</span><span class="sxs-lookup"><span data-stu-id="fc877-111">Permissions</span></span>
<span data-ttu-id="fc877-112">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="fc877-112">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="fc877-113">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="fc877-113">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="fc877-114">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="fc877-114">Permission type</span></span> |   <span data-ttu-id="fc877-115">Autorisation</span><span class="sxs-lookup"><span data-stu-id="fc877-115">Permission</span></span>  |   <span data-ttu-id="fc877-116">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="fc877-116">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="fc877-117">Application</span><span class="sxs-lookup"><span data-stu-id="fc877-117">Application</span></span> |   <span data-ttu-id="fc877-118">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="fc877-118">User.Read.All</span></span> | <span data-ttu-id="fc877-119">« Lire tous les profils utilisateur »</span><span class="sxs-lookup"><span data-stu-id="fc877-119">'Read all user profiles'</span></span>

## <a name="http-request"></a><span data-ttu-id="fc877-120">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="fc877-120">HTTP request</span></span>
```
GET /api/users/{id}/
```

## <a name="request-headers"></a><span data-ttu-id="fc877-121">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="fc877-121">Request headers</span></span>

<span data-ttu-id="fc877-122">Nom</span><span class="sxs-lookup"><span data-stu-id="fc877-122">Name</span></span> | <span data-ttu-id="fc877-123">Type</span><span class="sxs-lookup"><span data-stu-id="fc877-123">Type</span></span> | <span data-ttu-id="fc877-124">Description</span><span class="sxs-lookup"><span data-stu-id="fc877-124">Description</span></span>
:---|:---|:---
<span data-ttu-id="fc877-125">Autorisation</span><span class="sxs-lookup"><span data-stu-id="fc877-125">Authorization</span></span> | <span data-ttu-id="fc877-126">String</span><span class="sxs-lookup"><span data-stu-id="fc877-126">String</span></span> | <span data-ttu-id="fc877-127">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="fc877-127">Bearer {token}.</span></span> <span data-ttu-id="fc877-128">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="fc877-128">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="fc877-129">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="fc877-129">Request body</span></span>
<span data-ttu-id="fc877-130">Vide</span><span class="sxs-lookup"><span data-stu-id="fc877-130">Empty</span></span>

## <a name="response"></a><span data-ttu-id="fc877-131">Réponse</span><span class="sxs-lookup"><span data-stu-id="fc877-131">Response</span></span>
<span data-ttu-id="fc877-132">En cas de réussite et si l’utilisateur existe : 200 - OK avec [l’entité](user.md) utilisateur dans le corps.</span><span class="sxs-lookup"><span data-stu-id="fc877-132">If successful and user exists - 200 OK with [user](user.md) entity in the body.</span></span> <span data-ttu-id="fc877-133">Si l’utilisateur n’existe pas - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="fc877-133">If user does not exist - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="fc877-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="fc877-134">Example</span></span>

<span data-ttu-id="fc877-135">**Demande**</span><span class="sxs-lookup"><span data-stu-id="fc877-135">**Request**</span></span>

<span data-ttu-id="fc877-136">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="fc877-136">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/users/user1
Content-type: application/json
```

<span data-ttu-id="fc877-137">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="fc877-137">**Response**</span></span>

<span data-ttu-id="fc877-138">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="fc877-138">Here is an example of the response.</span></span>


```
HTTP/1.1 200 OK
Content-type: application/json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Users/$entity",
    "id": "user1",
    "firstSeen": "2018-08-02T00:00:00Z",
    "lastSeen": "2018-08-04T00:00:00Z",
    "mostPrevalentMachineId": null,
    "leastPrevalentMachineId": null,
    "logonTypes": "Network",
    "logOnMachinesCount": 3,
    "isDomainAdmin": false,
    "isOnlyNetworkUser": null
}
```
