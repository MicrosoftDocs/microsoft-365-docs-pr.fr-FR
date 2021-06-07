---
title: API De liste des ordinateurs
description: Découvrez comment utiliser l’API Des ordinateurs de liste pour récupérer une collection d’ordinateurs ayant communiqué avec Microsoft Defender pour le cloud endpoint.
keywords: api, api de graphique, api pris en charge, obtenir, appareils
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: f06973bc45ecac05c15d48afe5f0e2e9e7788f78
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52770744"
---
# <a name="list-machines-api"></a><span data-ttu-id="e1750-104">API De liste des ordinateurs</span><span class="sxs-lookup"><span data-stu-id="e1750-104">List machines API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="e1750-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="e1750-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="e1750-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="e1750-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="e1750-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="e1750-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="e1750-108">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="e1750-108">API description</span></span>
<span data-ttu-id="e1750-109">Récupère une collection [d’ordinateurs](machine.md) qui ont communiqué avec Microsoft Defender pour le cloud endpoint.</span><span class="sxs-lookup"><span data-stu-id="e1750-109">Retrieves a collection of [Machines](machine.md) that have communicated with  Microsoft Defender for Endpoint cloud.</span></span>
<br><span data-ttu-id="e1750-110">Prend [en charge les requêtes OData V4.](https://www.odata.org/documentation/)</span><span class="sxs-lookup"><span data-stu-id="e1750-110">Supports [OData V4 queries](https://www.odata.org/documentation/).</span></span>
<br><span data-ttu-id="e1750-111">La requête OData est prise en charge sur `$filter` : , , et `computerDnsName` `lastSeen` `healthStatus` `osPlatform` `riskScore` `rbacGroupId` .</span><span class="sxs-lookup"><span data-stu-id="e1750-111">The OData's `$filter` query is supported on: `computerDnsName`, `lastSeen`, `healthStatus`, `osPlatform`, `riskScore` and `rbacGroupId`.</span></span>
<br><span data-ttu-id="e1750-112">Voir des exemples [dans les requêtes OData avec Defender for Endpoint](exposed-apis-odata-samples.md)</span><span class="sxs-lookup"><span data-stu-id="e1750-112">See examples at [OData queries with Defender for Endpoint](exposed-apis-odata-samples.md)</span></span>


## <a name="limitations"></a><span data-ttu-id="e1750-113">Limitations</span><span class="sxs-lookup"><span data-stu-id="e1750-113">Limitations</span></span>
1. <span data-ttu-id="e1750-114">Vous pouvez obtenir la dernière vue des appareils en fonction de votre période de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="e1750-114">You can get devices last seen according to your configured retention period.</span></span>
2. <span data-ttu-id="e1750-115">La taille maximale de page est de 10 000.</span><span class="sxs-lookup"><span data-stu-id="e1750-115">Maximum page size is 10,000.</span></span>
3. <span data-ttu-id="e1750-116">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="e1750-116">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span> 


## <a name="permissions"></a><span data-ttu-id="e1750-117">Autorisations</span><span class="sxs-lookup"><span data-stu-id="e1750-117">Permissions</span></span>

<span data-ttu-id="e1750-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="e1750-118">Permission type</span></span> |   <span data-ttu-id="e1750-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="e1750-119">Permission</span></span>  |   <span data-ttu-id="e1750-120">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="e1750-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="e1750-121">Application</span><span class="sxs-lookup"><span data-stu-id="e1750-121">Application</span></span> |   <span data-ttu-id="e1750-122">Machine.Read.All</span><span class="sxs-lookup"><span data-stu-id="e1750-122">Machine.Read.All</span></span> |  <span data-ttu-id="e1750-123">« Lire tous les profils d’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="e1750-123">'Read all machine profiles'</span></span>
<span data-ttu-id="e1750-124">Application</span><span class="sxs-lookup"><span data-stu-id="e1750-124">Application</span></span> |   <span data-ttu-id="e1750-125">Machine.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e1750-125">Machine.ReadWrite.All</span></span> | <span data-ttu-id="e1750-126">« Lire et écrire toutes les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="e1750-126">'Read and write all machine information'</span></span>
<span data-ttu-id="e1750-127">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="e1750-127">Delegated (work or school account)</span></span> | <span data-ttu-id="e1750-128">Machine.Read</span><span class="sxs-lookup"><span data-stu-id="e1750-128">Machine.Read</span></span> | <span data-ttu-id="e1750-129">« Lire les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="e1750-129">'Read machine information'</span></span>
<span data-ttu-id="e1750-130">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="e1750-130">Delegated (work or school account)</span></span> | <span data-ttu-id="e1750-131">Machine.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e1750-131">Machine.ReadWrite</span></span> | <span data-ttu-id="e1750-132">« Lire et écrire des informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="e1750-132">'Read and write machine information'</span></span>

>[!Note]
> <span data-ttu-id="e1750-133">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="e1750-133">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="e1750-134">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="e1750-134">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="e1750-135">La réponse inclut uniquement les appareils, accessibles par l’utilisateur, en fonction des paramètres de groupe d’appareils (pour plus d’informations, voir Créer et gérer des groupes d’appareils) [](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="e1750-135">Response will include only devices, that the user have access to, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="e1750-136">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="e1750-136">HTTP request</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/machines
```

## <a name="request-headers"></a><span data-ttu-id="e1750-137">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="e1750-137">Request headers</span></span>

<span data-ttu-id="e1750-138">Nom</span><span class="sxs-lookup"><span data-stu-id="e1750-138">Name</span></span> | <span data-ttu-id="e1750-139">Type</span><span class="sxs-lookup"><span data-stu-id="e1750-139">Type</span></span> | <span data-ttu-id="e1750-140">Description</span><span class="sxs-lookup"><span data-stu-id="e1750-140">Description</span></span>
:---|:---|:---
<span data-ttu-id="e1750-141">Autorisation</span><span class="sxs-lookup"><span data-stu-id="e1750-141">Authorization</span></span> | <span data-ttu-id="e1750-142">String</span><span class="sxs-lookup"><span data-stu-id="e1750-142">String</span></span> | <span data-ttu-id="e1750-143">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="e1750-143">Bearer {token}.</span></span> <span data-ttu-id="e1750-144">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="e1750-144">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="e1750-145">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="e1750-145">Request body</span></span>
<span data-ttu-id="e1750-146">Vide</span><span class="sxs-lookup"><span data-stu-id="e1750-146">Empty</span></span>

## <a name="response"></a><span data-ttu-id="e1750-147">Réponse</span><span class="sxs-lookup"><span data-stu-id="e1750-147">Response</span></span>
<span data-ttu-id="e1750-148">En cas de réussite et si les ordinateurs existent : 200 - OK avec la liste des entités de [l’ordinateur](machine.md) dans le corps.</span><span class="sxs-lookup"><span data-stu-id="e1750-148">If successful and machines exists - 200 OK with list of [machine](machine.md) entities in the body.</span></span> <span data-ttu-id="e1750-149">Si aucun ordinateur récent - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="e1750-149">If no recent machines - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="e1750-150">Exemple</span><span class="sxs-lookup"><span data-stu-id="e1750-150">Example</span></span>

<span data-ttu-id="e1750-151">**Demande**</span><span class="sxs-lookup"><span data-stu-id="e1750-151">**Request**</span></span>

<span data-ttu-id="e1750-152">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="e1750-152">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/machines
```

<span data-ttu-id="e1750-153">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="e1750-153">**Response**</span></span>

<span data-ttu-id="e1750-154">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="e1750-154">Here is an example of the response.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Machines",
    "value": [
        {
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
        ...
    ]
}
```

## <a name="related-topics"></a><span data-ttu-id="e1750-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1750-155">Related topics</span></span>
- [<span data-ttu-id="e1750-156">Requêtes OData avec Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e1750-156">OData queries with Microsoft Defender for Endpoint</span></span>](exposed-apis-odata-samples.md)
