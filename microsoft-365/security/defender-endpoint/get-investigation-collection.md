---
title: API Enquêtes de liste
description: Utilisez cette API pour créer des appels liés à l’utilisation de la collection Investigations
keywords: api, api de graphique, api pris en charge, collection Investigations
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
ms.openlocfilehash: 9ad1216a05846b48bff4186c7e6f39e9da3623b0
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166696"
---
# <a name="list-investigations-api"></a><span data-ttu-id="5cd60-104">API Enquêtes de liste</span><span class="sxs-lookup"><span data-stu-id="5cd60-104">List Investigations API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="5cd60-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5cd60-105">**Applies to:**</span></span>
- [<span data-ttu-id="5cd60-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5cd60-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="5cd60-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5cd60-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="5cd60-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="5cd60-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="5cd60-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="5cd60-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="5cd60-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="5cd60-110">API description</span></span>
<span data-ttu-id="5cd60-111">Récupère une collection [d’enquêtes.](investigation.md)</span><span class="sxs-lookup"><span data-stu-id="5cd60-111">Retrieves a collection of [Investigations](investigation.md).</span></span>
<br><span data-ttu-id="5cd60-112">Prend [en charge les requêtes OData V4.](https://www.odata.org/documentation/)</span><span class="sxs-lookup"><span data-stu-id="5cd60-112">Supports [OData V4 queries](https://www.odata.org/documentation/).</span></span>
<br><span data-ttu-id="5cd60-113">La requête OData est prise en charge sur ```$filter``` : , et les ```startTime``` ```state``` ```machineId``` ```triggeringAlertId``` propriétés.</span><span class="sxs-lookup"><span data-stu-id="5cd60-113">The OData's ```$filter``` query is supported on: ```startTime```, ```state```, ```machineId``` and ```triggeringAlertId``` properties.</span></span>
<br><span data-ttu-id="5cd60-114">Voir des exemples [dans les requêtes OData avec Microsoft Defender for Endpoint](exposed-apis-odata-samples.md)</span><span class="sxs-lookup"><span data-stu-id="5cd60-114">See examples at [OData queries with Microsoft Defender for Endpoint](exposed-apis-odata-samples.md)</span></span>


## <a name="limitations"></a><span data-ttu-id="5cd60-115">Limites</span><span class="sxs-lookup"><span data-stu-id="5cd60-115">Limitations</span></span>
1. <span data-ttu-id="5cd60-116">La taille maximale de page est de 10 000.</span><span class="sxs-lookup"><span data-stu-id="5cd60-116">Maximum page size is 10,000.</span></span>
2. <span data-ttu-id="5cd60-117">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="5cd60-117">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span> 


## <a name="permissions"></a><span data-ttu-id="5cd60-118">Autorisations</span><span class="sxs-lookup"><span data-stu-id="5cd60-118">Permissions</span></span>
<span data-ttu-id="5cd60-119">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="5cd60-119">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="5cd60-120">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="5cd60-120">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="5cd60-121">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="5cd60-121">Permission type</span></span> |   <span data-ttu-id="5cd60-122">Autorisation</span><span class="sxs-lookup"><span data-stu-id="5cd60-122">Permission</span></span>  |   <span data-ttu-id="5cd60-123">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="5cd60-123">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="5cd60-124">Application</span><span class="sxs-lookup"><span data-stu-id="5cd60-124">Application</span></span> |   <span data-ttu-id="5cd60-125">Alert.Read.All</span><span class="sxs-lookup"><span data-stu-id="5cd60-125">Alert.Read.All</span></span> |    <span data-ttu-id="5cd60-126">« Lire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="5cd60-126">'Read all alerts'</span></span>
<span data-ttu-id="5cd60-127">Application</span><span class="sxs-lookup"><span data-stu-id="5cd60-127">Application</span></span> |   <span data-ttu-id="5cd60-128">Alert.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5cd60-128">Alert.ReadWrite.All</span></span> |   <span data-ttu-id="5cd60-129">« Lire et écrire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="5cd60-129">'Read and write all alerts'</span></span>
<span data-ttu-id="5cd60-130">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="5cd60-130">Delegated (work or school account)</span></span> | <span data-ttu-id="5cd60-131">Alert.Read</span><span class="sxs-lookup"><span data-stu-id="5cd60-131">Alert.Read</span></span> | <span data-ttu-id="5cd60-132">« Lire les alertes »</span><span class="sxs-lookup"><span data-stu-id="5cd60-132">'Read alerts'</span></span>
<span data-ttu-id="5cd60-133">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="5cd60-133">Delegated (work or school account)</span></span> | <span data-ttu-id="5cd60-134">Alert.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5cd60-134">Alert.ReadWrite</span></span> | <span data-ttu-id="5cd60-135">« Lire et écrire des alertes »</span><span class="sxs-lookup"><span data-stu-id="5cd60-135">'Read and write alerts'</span></span>

>[!Note]
> <span data-ttu-id="5cd60-136">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="5cd60-136">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="5cd60-137">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="5cd60-137">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="5cd60-138">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="5cd60-138">HTTP request</span></span>
```
GET https://api.securitycenter.microsoft.com/api/investigations
```

## <a name="request-headers"></a><span data-ttu-id="5cd60-139">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="5cd60-139">Request headers</span></span>

<span data-ttu-id="5cd60-140">Nom</span><span class="sxs-lookup"><span data-stu-id="5cd60-140">Name</span></span> | <span data-ttu-id="5cd60-141">Type</span><span class="sxs-lookup"><span data-stu-id="5cd60-141">Type</span></span> | <span data-ttu-id="5cd60-142">Description</span><span class="sxs-lookup"><span data-stu-id="5cd60-142">Description</span></span>
:---|:---|:---
<span data-ttu-id="5cd60-143">Autorisation</span><span class="sxs-lookup"><span data-stu-id="5cd60-143">Authorization</span></span> | <span data-ttu-id="5cd60-144">Chaîne</span><span class="sxs-lookup"><span data-stu-id="5cd60-144">String</span></span> | <span data-ttu-id="5cd60-145">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="5cd60-145">Bearer {token}.</span></span> <span data-ttu-id="5cd60-146">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="5cd60-146">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="5cd60-147">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="5cd60-147">Request body</span></span>
<span data-ttu-id="5cd60-148">Vide</span><span class="sxs-lookup"><span data-stu-id="5cd60-148">Empty</span></span>

## <a name="response"></a><span data-ttu-id="5cd60-149">Réponse</span><span class="sxs-lookup"><span data-stu-id="5cd60-149">Response</span></span>
<span data-ttu-id="5cd60-150">Si elle réussit, cette méthode renvoie le code de réponse 200, Ok avec une collection d’entités [Investigations.](investigation.md)</span><span class="sxs-lookup"><span data-stu-id="5cd60-150">If successful, this method returns 200, Ok response code with a collection of [Investigations](investigation.md) entities.</span></span>


## <a name="example"></a><span data-ttu-id="5cd60-151">Exemple</span><span class="sxs-lookup"><span data-stu-id="5cd60-151">Example</span></span>

<span data-ttu-id="5cd60-152">**Demande**</span><span class="sxs-lookup"><span data-stu-id="5cd60-152">**Request**</span></span>

<span data-ttu-id="5cd60-153">Voici un exemple de demande d’obtenir toutes les enquêtes :</span><span class="sxs-lookup"><span data-stu-id="5cd60-153">Here is an example of a request to get all investigations:</span></span> 

```
GET https://api.securitycenter.microsoft.com/api/investigations
```

<span data-ttu-id="5cd60-154">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="5cd60-154">**Response**</span></span>

<span data-ttu-id="5cd60-155">Voici un exemple de réponse :</span><span class="sxs-lookup"><span data-stu-id="5cd60-155">Here is an example of the response:</span></span>

```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Investigations",
    "value": [
        {
            "id": "63017",
            "startTime": "2020-01-06T14:11:34Z",
            "endTime": null,
            "state": "Running",
            "cancelledBy": null,
            "statusDetails": null,
            "machineId": "a69a22debe5f274d8765ea3c368d00762e057b30",
            "computerDnsName": "desktop-gtrcon0",
            "triggeringAlertId": "da637139166940871892_-598649278"
        }
        ...
    ]
}
```
