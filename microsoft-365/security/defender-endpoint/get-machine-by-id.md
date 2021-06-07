---
title: API Obtenir l’ordinateur par ID
description: Découvrez comment utiliser l’API Obtenir un ordinateur par ID pour récupérer un ordinateur par son ID d’appareil ou son nom d’ordinateur dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, appareils, entité, ID
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
ms.openlocfilehash: e4ed5a68b0f4c5e9472702d3cc2798a810e4f84e
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52769472"
---
# <a name="get-machine-by-id-api"></a><span data-ttu-id="9d20d-104">API Obtenir l’ordinateur par ID</span><span class="sxs-lookup"><span data-stu-id="9d20d-104">Get machine by ID API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="9d20d-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="9d20d-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>


> <span data-ttu-id="9d20d-106">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="9d20d-106">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="9d20d-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="9d20d-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="9d20d-108">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="9d20d-108">API description</span></span>
<span data-ttu-id="9d20d-109">Récupère un ordinateur [spécifique par](machine.md) son ID d’appareil ou son nom d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9d20d-109">Retrieves specific [Machine](machine.md) by its device ID or computer name.</span></span>


## <a name="limitations"></a><span data-ttu-id="9d20d-110">Limitations</span><span class="sxs-lookup"><span data-stu-id="9d20d-110">Limitations</span></span>
1. <span data-ttu-id="9d20d-111">Vous pouvez obtenir la dernière vue des appareils en fonction de votre stratégie de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="9d20d-111">You can get devices last seen according to your configured retention policy.</span></span>
2. <span data-ttu-id="9d20d-112">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="9d20d-112">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="9d20d-113">Autorisations</span><span class="sxs-lookup"><span data-stu-id="9d20d-113">Permissions</span></span>
<span data-ttu-id="9d20d-114">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="9d20d-114">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="9d20d-115">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="9d20d-115">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="9d20d-116">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="9d20d-116">Permission type</span></span> |   <span data-ttu-id="9d20d-117">Autorisation</span><span class="sxs-lookup"><span data-stu-id="9d20d-117">Permission</span></span>  |   <span data-ttu-id="9d20d-118">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="9d20d-118">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="9d20d-119">Application</span><span class="sxs-lookup"><span data-stu-id="9d20d-119">Application</span></span> |   <span data-ttu-id="9d20d-120">Machine.Read.All</span><span class="sxs-lookup"><span data-stu-id="9d20d-120">Machine.Read.All</span></span> |  <span data-ttu-id="9d20d-121">« Lire tous les profils d’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="9d20d-121">'Read all machine profiles'</span></span>
<span data-ttu-id="9d20d-122">Application</span><span class="sxs-lookup"><span data-stu-id="9d20d-122">Application</span></span> |   <span data-ttu-id="9d20d-123">Machine.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9d20d-123">Machine.ReadWrite.All</span></span> | <span data-ttu-id="9d20d-124">« Lire et écrire toutes les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="9d20d-124">'Read and write all machine information'</span></span>
<span data-ttu-id="9d20d-125">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="9d20d-125">Delegated (work or school account)</span></span> | <span data-ttu-id="9d20d-126">Machine.Read</span><span class="sxs-lookup"><span data-stu-id="9d20d-126">Machine.Read</span></span> | <span data-ttu-id="9d20d-127">« Lire les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="9d20d-127">'Read machine information'</span></span>
<span data-ttu-id="9d20d-128">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="9d20d-128">Delegated (work or school account)</span></span> | <span data-ttu-id="9d20d-129">Machine.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9d20d-129">Machine.ReadWrite</span></span> | <span data-ttu-id="9d20d-130">« Lire et écrire des informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="9d20d-130">'Read and write machine information'</span></span>

>[!Note]
> <span data-ttu-id="9d20d-131">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="9d20d-131">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="9d20d-132">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="9d20d-132">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="9d20d-133">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="9d20d-133">User needs to have access to the device, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>


## <a name="http-request"></a><span data-ttu-id="9d20d-134">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="9d20d-134">HTTP request</span></span>
```http
GET /api/machines/{id}
```

## <a name="request-headers"></a><span data-ttu-id="9d20d-135">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="9d20d-135">Request headers</span></span>

<span data-ttu-id="9d20d-136">Nom</span><span class="sxs-lookup"><span data-stu-id="9d20d-136">Name</span></span> | <span data-ttu-id="9d20d-137">Type</span><span class="sxs-lookup"><span data-stu-id="9d20d-137">Type</span></span> | <span data-ttu-id="9d20d-138">Description</span><span class="sxs-lookup"><span data-stu-id="9d20d-138">Description</span></span>
:---|:---|:---
<span data-ttu-id="9d20d-139">Autorisation</span><span class="sxs-lookup"><span data-stu-id="9d20d-139">Authorization</span></span> | <span data-ttu-id="9d20d-140">String</span><span class="sxs-lookup"><span data-stu-id="9d20d-140">String</span></span> | <span data-ttu-id="9d20d-141">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="9d20d-141">Bearer {token}.</span></span> <span data-ttu-id="9d20d-142">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="9d20d-142">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="9d20d-143">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="9d20d-143">Request body</span></span>
<span data-ttu-id="9d20d-144">Vide</span><span class="sxs-lookup"><span data-stu-id="9d20d-144">Empty</span></span>

## <a name="response"></a><span data-ttu-id="9d20d-145">Réponse</span><span class="sxs-lookup"><span data-stu-id="9d20d-145">Response</span></span>
<span data-ttu-id="9d20d-146">En cas de réussite et si l’appareil existe : 200 - OK avec l’entité [de l’ordinateur](machine.md) dans le corps.</span><span class="sxs-lookup"><span data-stu-id="9d20d-146">If successful and device exists - 200 OK with the [machine](machine.md) entity in the body.</span></span>
<span data-ttu-id="9d20d-147">Si l’ordinateur avec l’ID spécifié est in trouvé - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="9d20d-147">If machine with the specified ID was not found - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="9d20d-148">Exemple</span><span class="sxs-lookup"><span data-stu-id="9d20d-148">Example</span></span>

<span data-ttu-id="9d20d-149">**Demande**</span><span class="sxs-lookup"><span data-stu-id="9d20d-149">**Request**</span></span>

<span data-ttu-id="9d20d-150">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="9d20d-150">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/machines/1e5bc9d7e413ddd7902c2932e418702b84d0cc07
```

<span data-ttu-id="9d20d-151">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="9d20d-151">**Response**</span></span>

<span data-ttu-id="9d20d-152">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="9d20d-152">Here is an example of the response.</span></span>


```http
HTTP/1.1 200 OK
Content-type: application/json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Machine",
    "id": "1e5bc9d7e413ddd7902c2932e418702b84d0cc07",
    "computerDnsName": "mymachine1.contoso.com",
    "firstSeen": "2018-08-02T14:55:03.7791856Z",
    "lastSeen": "2018-08-02T14:55:03.7791856Z",
    "osPlatform": "Windows10",
    "version": "1709",
    "osProcessor": "x64",
    "lastIpAddress": "172.17.230.209",
    "lastExternalIpAddress": "167.220.196.71",
    "osBuild": 18209,
    "healthStatus": "Active",
    "rbacGroupId": 140,
    "rbacGroupName": "The-A-Team",
    "riskScore": "Low",
    "exposureLevel": "Medium",
    "isAadJoined": true,
    "aadDeviceId": "80fe8ff8-2624-418e-9591-41f0491218f9",
    "machineTags": [ "test tag 1", "test tag 2" ]
}

```
