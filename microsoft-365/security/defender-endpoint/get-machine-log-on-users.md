---
title: API Obtenir les utilisateurs de connexion de l’ordinateur
description: Découvrez comment utiliser l’API Obtenir les utilisateurs de connexion de l’ordinateur pour récupérer une collection d’utilisateurs connectés sur un appareil dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, appareil, se connecter, utilisateurs
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 634a381ca862dc7580d82168a4b9540acc0cd394
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53229022"
---
# <a name="get-machine-logon-users-api"></a><span data-ttu-id="6fc20-104">API Obtenir les utilisateurs de connexion de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="6fc20-104">Get machine logon users API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="6fc20-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="6fc20-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

> <span data-ttu-id="6fc20-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="6fc20-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="6fc20-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6fc20-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="6fc20-108">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="6fc20-108">API description</span></span>
<span data-ttu-id="6fc20-109">Récupère une collection d’utilisateurs connectés sur un appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="6fc20-109">Retrieves a collection of logged on users on a specific device.</span></span>

## <a name="limitations"></a><span data-ttu-id="6fc20-110">Limites</span><span class="sxs-lookup"><span data-stu-id="6fc20-110">Limitations</span></span>
1. <span data-ttu-id="6fc20-111">Vous pouvez interroger la dernière mise à jour des alertes en fonction de votre période de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="6fc20-111">You can query on alerts last updated according to your configured retention period.</span></span>
2. <span data-ttu-id="6fc20-112">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="6fc20-112">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>

## <a name="permissions"></a><span data-ttu-id="6fc20-113">Autorisations</span><span class="sxs-lookup"><span data-stu-id="6fc20-113">Permissions</span></span>
<span data-ttu-id="6fc20-114">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="6fc20-114">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="6fc20-115">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="6fc20-115">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="6fc20-116">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="6fc20-116">Permission type</span></span> |<span data-ttu-id="6fc20-117">Autorisation</span><span class="sxs-lookup"><span data-stu-id="6fc20-117">Permission</span></span>|<span data-ttu-id="6fc20-118">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="6fc20-118">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="6fc20-119">Application</span><span class="sxs-lookup"><span data-stu-id="6fc20-119">Application</span></span> |<span data-ttu-id="6fc20-120">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="6fc20-120">User.Read.All</span></span> |<span data-ttu-id="6fc20-121">« Lire les profils utilisateur »</span><span class="sxs-lookup"><span data-stu-id="6fc20-121">'Read user profiles'</span></span>
<span data-ttu-id="6fc20-122">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="6fc20-122">Delegated (work or school account)</span></span> | <span data-ttu-id="6fc20-123">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="6fc20-123">User.Read.All</span></span> | <span data-ttu-id="6fc20-124">« Lire les profils utilisateur »</span><span class="sxs-lookup"><span data-stu-id="6fc20-124">'Read user profiles'</span></span>

> [!NOTE]
> <span data-ttu-id="6fc20-125">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="6fc20-125">When obtaining a token using user credentials:</span></span>
>
> - <span data-ttu-id="6fc20-126">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données ».</span><span class="sxs-lookup"><span data-stu-id="6fc20-126">The user needs to have at least the following role permission: 'View Data'.</span></span> <span data-ttu-id="6fc20-127">Pour plus d’informations, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="6fc20-127">For more information, see [Create and manage roles](user-roles.md)).</span></span>
> - <span data-ttu-id="6fc20-128">La réponse inclut les utilisateurs uniquement si l’appareil est visible par l’utilisateur, en fonction des paramètres de groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="6fc20-128">Response will include users only if the device is visible to the user, based on device group settings.</span></span> <span data-ttu-id="6fc20-129">Pour plus d’informations, voir [Créer et gérer des groupes d’appareils.](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="6fc20-129">For more information, see [Create and manage device groups](machine-groups.md).</span></span>

## <a name="http-request"></a><span data-ttu-id="6fc20-130">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="6fc20-130">HTTP request</span></span>

```http
GET /api/machines/{id}/logonusers
```

## <a name="request-headers"></a><span data-ttu-id="6fc20-131">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="6fc20-131">Request headers</span></span>

<span data-ttu-id="6fc20-132">Nom</span><span class="sxs-lookup"><span data-stu-id="6fc20-132">Name</span></span> | <span data-ttu-id="6fc20-133">Type</span><span class="sxs-lookup"><span data-stu-id="6fc20-133">Type</span></span> | <span data-ttu-id="6fc20-134">Description</span><span class="sxs-lookup"><span data-stu-id="6fc20-134">Description</span></span>
:---|:---|:---
<span data-ttu-id="6fc20-135">Autorisation</span><span class="sxs-lookup"><span data-stu-id="6fc20-135">Authorization</span></span> | <span data-ttu-id="6fc20-136">String</span><span class="sxs-lookup"><span data-stu-id="6fc20-136">String</span></span> | <span data-ttu-id="6fc20-137">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="6fc20-137">Bearer {token}.</span></span> <span data-ttu-id="6fc20-138">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="6fc20-138">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="6fc20-139">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="6fc20-139">Request body</span></span>

<span data-ttu-id="6fc20-140">Vide</span><span class="sxs-lookup"><span data-stu-id="6fc20-140">Empty</span></span>

## <a name="response"></a><span data-ttu-id="6fc20-141">Réponse</span><span class="sxs-lookup"><span data-stu-id="6fc20-141">Response</span></span>

<span data-ttu-id="6fc20-142">En cas de réussite et si l’appareil existe : 200 - OK avec la liste [des](user.md) entités utilisateur dans le corps.</span><span class="sxs-lookup"><span data-stu-id="6fc20-142">If successful and device exists - 200 OK with list of [user](user.md) entities in the body.</span></span> <span data-ttu-id="6fc20-143">If device was not found - 404 Not Found.</span><span class="sxs-lookup"><span data-stu-id="6fc20-143">If device was not found - 404 Not Found.</span></span>

## <a name="example"></a><span data-ttu-id="6fc20-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="6fc20-144">Example</span></span>

### <a name="request"></a><span data-ttu-id="6fc20-145">Demande</span><span class="sxs-lookup"><span data-stu-id="6fc20-145">Request</span></span>

<span data-ttu-id="6fc20-146">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="6fc20-146">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/machines/1e5bc9d7e413ddd7902c2932e418702b84d0cc07/logonusers
```

### <a name="response"></a><span data-ttu-id="6fc20-147">Réponse</span><span class="sxs-lookup"><span data-stu-id="6fc20-147">Response</span></span>

<span data-ttu-id="6fc20-148">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="6fc20-148">Here is an example of the response.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Users",
    "value": [
        {
            "id": "contoso\\user1",
            "accountName": "user1",
            "accountDomain": "contoso",
            "accountSid": "S-1-5-21-72051607-1745760036-109187956-93922",
            "firstSeen": "2019-12-18T08:02:54Z",
            "lastSeen": "2020-01-06T08:01:48Z",
            "logonTypes": "Interactive",
            "logOnMachinesCount": 8,
            "isDomainAdmin": true,
            "isOnlyNetworkUser": false
        },
        ...
    ]
}
```
