---
title: Obtenir des informations sur l’utilisateur associé à une alerte
description: Découvrez comment utiliser l’API Obtenir les informations utilisateur associées à l’alerte pour récupérer l’utilisateur associé à une alerte spécifique dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, alerte, informations, associé, utilisateur
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
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
ms.technology: mde
ms.openlocfilehash: aee3c6fb381341c6823fbcb6766c0b761cb3413d
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166629"
---
# <a name="get-alert-related-user-information-api"></a><span data-ttu-id="3b513-104">API Obtenir les informations utilisateur associées à une alerte</span><span class="sxs-lookup"><span data-stu-id="3b513-104">Get alert related user information API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="3b513-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3b513-105">**Applies to:**</span></span>
- [<span data-ttu-id="3b513-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3b513-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="3b513-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3b513-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="3b513-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="3b513-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="3b513-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="3b513-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="3b513-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="3b513-110">API description</span></span>
<span data-ttu-id="3b513-111">Récupère l’utilisateur associé à une alerte spécifique.</span><span class="sxs-lookup"><span data-stu-id="3b513-111">Retrieves the User related to a specific alert.</span></span>


## <a name="limitations"></a><span data-ttu-id="3b513-112">Limites</span><span class="sxs-lookup"><span data-stu-id="3b513-112">Limitations</span></span>
1. <span data-ttu-id="3b513-113">Vous pouvez interroger la dernière mise à jour des alertes en fonction de votre période de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="3b513-113">You can query on alerts last updated according to your configured retention period.</span></span>
2. <span data-ttu-id="3b513-114">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="3b513-114">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="3b513-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="3b513-115">Permissions</span></span>
<span data-ttu-id="3b513-116">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="3b513-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="3b513-117">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="3b513-117">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="3b513-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="3b513-118">Permission type</span></span> |   <span data-ttu-id="3b513-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="3b513-119">Permission</span></span>  |   <span data-ttu-id="3b513-120">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="3b513-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="3b513-121">Application</span><span class="sxs-lookup"><span data-stu-id="3b513-121">Application</span></span> |   <span data-ttu-id="3b513-122">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="3b513-122">User.Read.All</span></span> | <span data-ttu-id="3b513-123">« Lire les profils utilisateur »</span><span class="sxs-lookup"><span data-stu-id="3b513-123">'Read user profiles'</span></span>
<span data-ttu-id="3b513-124">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="3b513-124">Delegated (work or school account)</span></span> | <span data-ttu-id="3b513-125">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="3b513-125">User.Read.All</span></span> | <span data-ttu-id="3b513-126">« Lire les profils utilisateur »</span><span class="sxs-lookup"><span data-stu-id="3b513-126">'Read user profiles'</span></span>

>[!Note]
> <span data-ttu-id="3b513-127">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="3b513-127">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="3b513-128">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="3b513-128">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="3b513-129">L’utilisateur doit avoir accès à l’appareil associé à l’alerte, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="3b513-129">The user needs to have access to the device associated with the alert, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="3b513-130">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="3b513-130">HTTP request</span></span>
```
GET /api/alerts/{id}/user
```

## <a name="request-headers"></a><span data-ttu-id="3b513-131">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="3b513-131">Request headers</span></span>

<span data-ttu-id="3b513-132">Nom</span><span class="sxs-lookup"><span data-stu-id="3b513-132">Name</span></span> | <span data-ttu-id="3b513-133">Type</span><span class="sxs-lookup"><span data-stu-id="3b513-133">Type</span></span> | <span data-ttu-id="3b513-134">Description</span><span class="sxs-lookup"><span data-stu-id="3b513-134">Description</span></span>
:---|:---|:---
<span data-ttu-id="3b513-135">Autorisation</span><span class="sxs-lookup"><span data-stu-id="3b513-135">Authorization</span></span> | <span data-ttu-id="3b513-136">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3b513-136">String</span></span> | <span data-ttu-id="3b513-137">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="3b513-137">Bearer {token}.</span></span> <span data-ttu-id="3b513-138">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="3b513-138">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="3b513-139">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="3b513-139">Request body</span></span>
<span data-ttu-id="3b513-140">Vide</span><span class="sxs-lookup"><span data-stu-id="3b513-140">Empty</span></span>

## <a name="response"></a><span data-ttu-id="3b513-141">Réponse</span><span class="sxs-lookup"><span data-stu-id="3b513-141">Response</span></span>
<span data-ttu-id="3b513-142">En cas de réussite et d’alerte et si un utilisateur existe : 200 - OK avec l’utilisateur dans le corps.</span><span class="sxs-lookup"><span data-stu-id="3b513-142">If successful and alert and a user exists - 200 OK with user in the body.</span></span> <span data-ttu-id="3b513-143">Si l’alerte ou l’utilisateur est in found - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="3b513-143">If alert or user not found - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="3b513-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="3b513-144">Example</span></span>

<span data-ttu-id="3b513-145">**Demande**</span><span class="sxs-lookup"><span data-stu-id="3b513-145">**Request**</span></span>

<span data-ttu-id="3b513-146">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="3b513-146">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/alerts/636688558380765161_2136280442/user
```

<span data-ttu-id="3b513-147">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="3b513-147">**Response**</span></span>

<span data-ttu-id="3b513-148">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="3b513-148">Here is an example of the response.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Users/$entity",
    "id": "contoso\\user1",
    "accountName": "user1",
    "accountDomain": "contoso",
    "accountSid": "S-1-5-21-72051607-1745760036-109187956-93922",
    "firstSeen": "2019-12-08T06:33:39Z",
    "lastSeen": "2020-01-05T06:58:34Z",
    "mostPrevalentMachineId": "0111b647235c26159bec3e5eb6c8c3a0cc3ab766",
    "leastPrevalentMachineId": "0111b647235c26159bec3e5eb6c8c3a0cc3ab766",
    "logonTypes": "Network",
    "logOnMachinesCount": 1,
    "isDomainAdmin": false,
    "isOnlyNetworkUser": false
}
```
