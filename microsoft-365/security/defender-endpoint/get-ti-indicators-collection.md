---
title: API d’indicateurs de liste
description: Découvrez comment utiliser l’API Indicateurs de liste pour récupérer une collection de tous les indicateurs actifs dans Microsoft Defender pour point de terminaison.
keywords: api, api publique, api pris en charge, collection d’indicateurs
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
ms.openlocfilehash: d9ec8610957af0bc7741848e7c7bd4fe850f5e32
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52770422"
---
# <a name="list-indicators-api"></a><span data-ttu-id="dd9ac-104">API d’indicateurs de liste</span><span class="sxs-lookup"><span data-stu-id="dd9ac-104">List Indicators API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="dd9ac-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="dd9ac-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="dd9ac-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="dd9ac-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="dd9ac-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="dd9ac-108">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="dd9ac-108">API description</span></span>
<span data-ttu-id="dd9ac-109">Extrait une collection de tous les indicateurs [actifs.](ti-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="dd9ac-109">Retrieves a collection of all active [Indicators](ti-indicator.md).</span></span>
<br><span data-ttu-id="dd9ac-110">Prend [en charge les requêtes OData V4.](https://www.odata.org/documentation/)</span><span class="sxs-lookup"><span data-stu-id="dd9ac-110">Supports [OData V4 queries](https://www.odata.org/documentation/).</span></span>
<br><span data-ttu-id="dd9ac-111">La requête OData est prise en charge sur ```$filter``` : , , , et les ```indicatorValue``` ```indicatorType``` ```creationTimeDateTimeUtc``` ```createdBy``` ```action``` ```severity``` propriétés.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-111">The OData's ```$filter``` query is supported on: ```indicatorValue```, ```indicatorType```, ```creationTimeDateTimeUtc```, ```createdBy```, ```action``` and ```severity``` properties.</span></span>
<br><span data-ttu-id="dd9ac-112">Voir des exemples [dans les requêtes OData avec Microsoft Defender for Endpoint](exposed-apis-odata-samples.md)</span><span class="sxs-lookup"><span data-stu-id="dd9ac-112">See examples at [OData queries with Microsoft Defender for Endpoint](exposed-apis-odata-samples.md)</span></span>


## <a name="limitations"></a><span data-ttu-id="dd9ac-113">Limites</span><span class="sxs-lookup"><span data-stu-id="dd9ac-113">Limitations</span></span>
1. <span data-ttu-id="dd9ac-114">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-114">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span> 


## <a name="permissions"></a><span data-ttu-id="dd9ac-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="dd9ac-115">Permissions</span></span>
<span data-ttu-id="dd9ac-116">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="dd9ac-117">Pour en savoir plus, notamment sur le choix des autorisations, [consultez La](apis-intro.md) mise en place</span><span class="sxs-lookup"><span data-stu-id="dd9ac-117">To learn more, including how to choose permissions, see [Get started](apis-intro.md)</span></span>

<span data-ttu-id="dd9ac-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="dd9ac-118">Permission type</span></span> |   <span data-ttu-id="dd9ac-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="dd9ac-119">Permission</span></span>  |   <span data-ttu-id="dd9ac-120">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="dd9ac-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="dd9ac-121">Application</span><span class="sxs-lookup"><span data-stu-id="dd9ac-121">Application</span></span> |   <span data-ttu-id="dd9ac-122">Ti.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="dd9ac-122">Ti.ReadWrite</span></span> |  <span data-ttu-id="dd9ac-123">« Lire et écrire des indicateurs »</span><span class="sxs-lookup"><span data-stu-id="dd9ac-123">'Read and write Indicators'</span></span>
<span data-ttu-id="dd9ac-124">Application</span><span class="sxs-lookup"><span data-stu-id="dd9ac-124">Application</span></span> |   <span data-ttu-id="dd9ac-125">Ti.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dd9ac-125">Ti.ReadWrite.All</span></span> |  <span data-ttu-id="dd9ac-126">« Lire et écrire tous les indicateurs »</span><span class="sxs-lookup"><span data-stu-id="dd9ac-126">'Read and write All Indicators'</span></span>
<span data-ttu-id="dd9ac-127">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="dd9ac-127">Delegated (work or school account)</span></span> |    <span data-ttu-id="dd9ac-128">Ti.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="dd9ac-128">Ti.ReadWrite</span></span> |  <span data-ttu-id="dd9ac-129">« Lire et écrire des indicateurs »</span><span class="sxs-lookup"><span data-stu-id="dd9ac-129">'Read and write Indicators'</span></span>

## <a name="http-request"></a><span data-ttu-id="dd9ac-130">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="dd9ac-130">HTTP request</span></span>
```
GET https://api.securitycenter.microsoft.com/api/indicators
```

## <a name="request-headers"></a><span data-ttu-id="dd9ac-131">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="dd9ac-131">Request headers</span></span>

<span data-ttu-id="dd9ac-132">Nom</span><span class="sxs-lookup"><span data-stu-id="dd9ac-132">Name</span></span> | <span data-ttu-id="dd9ac-133">Type</span><span class="sxs-lookup"><span data-stu-id="dd9ac-133">Type</span></span> | <span data-ttu-id="dd9ac-134">Description</span><span class="sxs-lookup"><span data-stu-id="dd9ac-134">Description</span></span>
:---|:---|:---
<span data-ttu-id="dd9ac-135">Autorisation</span><span class="sxs-lookup"><span data-stu-id="dd9ac-135">Authorization</span></span> | <span data-ttu-id="dd9ac-136">String</span><span class="sxs-lookup"><span data-stu-id="dd9ac-136">String</span></span> | <span data-ttu-id="dd9ac-137">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-137">Bearer {token}.</span></span> <span data-ttu-id="dd9ac-138">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-138">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="dd9ac-139">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="dd9ac-139">Request body</span></span>
<span data-ttu-id="dd9ac-140">Vide</span><span class="sxs-lookup"><span data-stu-id="dd9ac-140">Empty</span></span>

## <a name="response"></a><span data-ttu-id="dd9ac-141">Réponse</span><span class="sxs-lookup"><span data-stu-id="dd9ac-141">Response</span></span>
<span data-ttu-id="dd9ac-142">Si elle réussit, cette méthode renvoie le code de réponse 200, Ok avec une collection [d’entités Indicator.](ti-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="dd9ac-142">If successful, this method returns 200, Ok response code with a collection of [Indicator](ti-indicator.md) entities.</span></span>

>[!Note]
> <span data-ttu-id="dd9ac-143">Si l’application dispose de l’autorisation « Ti.ReadWrite.All » , elle est exposée à tous les indicateurs.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-143">If the Application has 'Ti.ReadWrite.All' permission, it will be exposed to all Indicators.</span></span> <span data-ttu-id="dd9ac-144">Sinon, il sera exposé uniquement aux indicateurs qu’il a créés.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-144">Otherwise, it will be exposed only to the Indicators it created.</span></span>

## <a name="example-1"></a><span data-ttu-id="dd9ac-145">Exemple 1 :</span><span class="sxs-lookup"><span data-stu-id="dd9ac-145">Example 1:</span></span>

<span data-ttu-id="dd9ac-146">**Demande**</span><span class="sxs-lookup"><span data-stu-id="dd9ac-146">**Request**</span></span>

<span data-ttu-id="dd9ac-147">Voici un exemple de demande qui obtient tous les indicateurs</span><span class="sxs-lookup"><span data-stu-id="dd9ac-147">Here is an example of a request that gets all Indicators</span></span>

```
GET https://api.securitycenter.microsoft.com/api/indicators
```

<span data-ttu-id="dd9ac-148">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="dd9ac-148">**Response**</span></span>

<span data-ttu-id="dd9ac-149">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-149">Here is an example of the response.</span></span>

```
HTTP/1.1 200 Ok
Content-type: application/json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Indicators",
    "value": [
        {
            "id": "995",
            "indicatorValue": "12.13.14.15",
            "indicatorType": "IpAddress",
            "action": "Alert",
            "application": "demo-test",
            "source": "TestPrdApp",
            "sourceType": "AadApp",
            "title": "test",
            "creationTimeDateTimeUtc": "2018-10-24T11:15:35.3688259Z",
            "createdBy": "45097602-1234-5678-1234-9f453233e62c",
            "expirationTime": "2020-12-12T00:00:00Z",
            "lastUpdateTime": "2019-10-24T10:54:23.2009016Z",
            "lastUpdatedBy": TestPrdApp,
            "severity": "Informational",
            "description": "test",
            "recommendedActions": "test",
            "rbacGroupNames": []
        },
        {
            "id": "996",
            "indicatorValue": "220e7d15b0b3d7fac48f2bd61114db1022197f7f",
            "indicatorType": "FileSha1",
            "action": "AlertAndBlock",
            "application": null,
            "source": "TestPrdApp",
            "sourceType": "AadApp",
            "title": "test",
            "creationTimeDateTimeUtc": "2018-10-24T10:54:23.2009016Z",
            "createdBy": "45097602-1234-5678-1234-9f453233e62c",
            "expirationTime": "2020-12-12T00:00:00Z",
            "lastUpdateTime": "2019-10-24T10:54:23.2009016Z",
            "lastUpdatedBy": TestPrdApp,
            "severity": "Informational",
            "description": "test",
            "recommendedActions": "TEST",
            "rbacGroupNames": [ "Group1", "Group2" ]
        }
        ...
    ]
}
```

## <a name="example-2"></a><span data-ttu-id="dd9ac-150">Exemple 2 :</span><span class="sxs-lookup"><span data-stu-id="dd9ac-150">Example 2:</span></span>

<span data-ttu-id="dd9ac-151">**Demande**</span><span class="sxs-lookup"><span data-stu-id="dd9ac-151">**Request**</span></span>

<span data-ttu-id="dd9ac-152">Voici un exemple de demande qui obtient tous les indicateurs avec l’action « AlertAndBlock »</span><span class="sxs-lookup"><span data-stu-id="dd9ac-152">Here is an example of a request that gets all Indicators with 'AlertAndBlock' action</span></span> 

```
GET https://api.securitycenter.microsoft.com/api/indicators?$filter=action+eq+'AlertAndBlock'
```

<span data-ttu-id="dd9ac-153">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="dd9ac-153">**Response**</span></span>

<span data-ttu-id="dd9ac-154">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-154">Here is an example of the response.</span></span>

```
HTTP/1.1 200 Ok
Content-type: application/json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Indicators",
    "value": [
        {
            "id": "997",
            "indicatorValue": "111e7d15b0b3d7fac48f2bd61114db1022197f7f",
            "indicatorType": "FileSha1",
            "action": "AlertAndBlock",
            "application": null,
            "source": "TestPrdApp",
            "sourceType": "AadApp",
            "title": "test",
            "creationTimeDateTimeUtc": "2018-10-24T10:54:23.2009016Z",
            "createdBy": "45097602-1234-5678-1234-9f453233e62c",
            "expirationTime": "2020-12-12T00:00:00Z",
            "lastUpdateTime": "2019-10-24T10:54:23.2009016Z",
            "lastUpdatedBy": TestPrdApp,
            "severity": "Informational",
            "description": "test",
            "recommendedActions": "TEST",
            "rbacGroupNames": [ "Group1", "Group2" ]
        }
        ...
    ]
}
```
