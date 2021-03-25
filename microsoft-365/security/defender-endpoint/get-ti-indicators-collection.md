---
title: API Des indicateurs de liste
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
ms.openlocfilehash: 868fd141cda3b3d92464a2d9247780e0e74d6de8
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51198552"
---
# <a name="list-indicators-api"></a><span data-ttu-id="80f5e-104">API d’indicateurs de liste</span><span class="sxs-lookup"><span data-stu-id="80f5e-104">List Indicators API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="80f5e-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="80f5e-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="80f5e-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="80f5e-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="80f5e-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="80f5e-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="80f5e-108">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="80f5e-108">API description</span></span>
<span data-ttu-id="80f5e-109">Extrait une collection de tous les indicateurs [actifs.](ti-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="80f5e-109">Retrieves a collection of all active [Indicators](ti-indicator.md).</span></span>
<br><span data-ttu-id="80f5e-110">Prend [en charge les requêtes OData V4.](https://www.odata.org/documentation/)</span><span class="sxs-lookup"><span data-stu-id="80f5e-110">Supports [OData V4 queries](https://www.odata.org/documentation/).</span></span>
<br><span data-ttu-id="80f5e-111">La requête OData est prise en charge sur ```$filter``` : , , , et les ```indicatorValue``` ```indicatorType``` ```creationTimeDateTimeUtc``` ```createdBy``` ```action``` ```severity``` propriétés.</span><span class="sxs-lookup"><span data-stu-id="80f5e-111">The OData's ```$filter``` query is supported on: ```indicatorValue```, ```indicatorType```, ```creationTimeDateTimeUtc```, ```createdBy```, ```action``` and ```severity``` properties.</span></span>
<br><span data-ttu-id="80f5e-112">Voir des exemples [dans les requêtes OData avec Microsoft Defender for Endpoint](exposed-apis-odata-samples.md)</span><span class="sxs-lookup"><span data-stu-id="80f5e-112">See examples at [OData queries with Microsoft Defender for Endpoint](exposed-apis-odata-samples.md)</span></span>


## <a name="limitations"></a><span data-ttu-id="80f5e-113">Limites</span><span class="sxs-lookup"><span data-stu-id="80f5e-113">Limitations</span></span>
1. <span data-ttu-id="80f5e-114">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="80f5e-114">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span> 


## <a name="permissions"></a><span data-ttu-id="80f5e-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="80f5e-115">Permissions</span></span>
<span data-ttu-id="80f5e-116">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="80f5e-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="80f5e-117">Pour en savoir plus, notamment sur le choix des autorisations, [consultez La](apis-intro.md) mise en place</span><span class="sxs-lookup"><span data-stu-id="80f5e-117">To learn more, including how to choose permissions, see [Get started](apis-intro.md)</span></span>

<span data-ttu-id="80f5e-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="80f5e-118">Permission type</span></span> |   <span data-ttu-id="80f5e-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="80f5e-119">Permission</span></span>  |   <span data-ttu-id="80f5e-120">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="80f5e-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="80f5e-121">Application</span><span class="sxs-lookup"><span data-stu-id="80f5e-121">Application</span></span> |   <span data-ttu-id="80f5e-122">Ti.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="80f5e-122">Ti.ReadWrite</span></span> |  <span data-ttu-id="80f5e-123">« Lire et écrire des indicateurs »</span><span class="sxs-lookup"><span data-stu-id="80f5e-123">'Read and write Indicators'</span></span>
<span data-ttu-id="80f5e-124">Application</span><span class="sxs-lookup"><span data-stu-id="80f5e-124">Application</span></span> |   <span data-ttu-id="80f5e-125">Ti.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="80f5e-125">Ti.ReadWrite.All</span></span> |  <span data-ttu-id="80f5e-126">« Lire et écrire tous les indicateurs »</span><span class="sxs-lookup"><span data-stu-id="80f5e-126">'Read and write All Indicators'</span></span>
<span data-ttu-id="80f5e-127">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="80f5e-127">Delegated (work or school account)</span></span> |    <span data-ttu-id="80f5e-128">Ti.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="80f5e-128">Ti.ReadWrite</span></span> |  <span data-ttu-id="80f5e-129">« Lire et écrire des indicateurs »</span><span class="sxs-lookup"><span data-stu-id="80f5e-129">'Read and write Indicators'</span></span>

## <a name="http-request"></a><span data-ttu-id="80f5e-130">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="80f5e-130">HTTP request</span></span>
```
GET https://api.securitycenter.microsoft.com/api/indicators
```

## <a name="request-headers"></a><span data-ttu-id="80f5e-131">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="80f5e-131">Request headers</span></span>

<span data-ttu-id="80f5e-132">Nom</span><span class="sxs-lookup"><span data-stu-id="80f5e-132">Name</span></span> | <span data-ttu-id="80f5e-133">Type</span><span class="sxs-lookup"><span data-stu-id="80f5e-133">Type</span></span> | <span data-ttu-id="80f5e-134">Description</span><span class="sxs-lookup"><span data-stu-id="80f5e-134">Description</span></span>
:---|:---|:---
<span data-ttu-id="80f5e-135">Autorisation</span><span class="sxs-lookup"><span data-stu-id="80f5e-135">Authorization</span></span> | <span data-ttu-id="80f5e-136">Chaîne</span><span class="sxs-lookup"><span data-stu-id="80f5e-136">String</span></span> | <span data-ttu-id="80f5e-137">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="80f5e-137">Bearer {token}.</span></span> <span data-ttu-id="80f5e-138">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="80f5e-138">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="80f5e-139">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="80f5e-139">Request body</span></span>
<span data-ttu-id="80f5e-140">Vide</span><span class="sxs-lookup"><span data-stu-id="80f5e-140">Empty</span></span>

## <a name="response"></a><span data-ttu-id="80f5e-141">Réponse</span><span class="sxs-lookup"><span data-stu-id="80f5e-141">Response</span></span>
<span data-ttu-id="80f5e-142">Si elle réussit, cette méthode renvoie le code de réponse 200, Ok avec une collection [d’entités Indicator.](ti-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="80f5e-142">If successful, this method returns 200, Ok response code with a collection of [Indicator](ti-indicator.md) entities.</span></span>

>[!Note]
> <span data-ttu-id="80f5e-143">Si l’application dispose de l’autorisation « Ti.ReadWrite.All » , elle est exposée à tous les indicateurs.</span><span class="sxs-lookup"><span data-stu-id="80f5e-143">If the Application has 'Ti.ReadWrite.All' permission, it will be exposed to all Indicators.</span></span> <span data-ttu-id="80f5e-144">Sinon, il sera exposé uniquement aux indicateurs qu’il a créés.</span><span class="sxs-lookup"><span data-stu-id="80f5e-144">Otherwise, it will be exposed only to the Indicators it created.</span></span>

## <a name="example-1"></a><span data-ttu-id="80f5e-145">Exemple 1 :</span><span class="sxs-lookup"><span data-stu-id="80f5e-145">Example 1:</span></span>

<span data-ttu-id="80f5e-146">**Demande**</span><span class="sxs-lookup"><span data-stu-id="80f5e-146">**Request**</span></span>

<span data-ttu-id="80f5e-147">Voici un exemple de demande qui obtient tous les indicateurs</span><span class="sxs-lookup"><span data-stu-id="80f5e-147">Here is an example of a request that gets all Indicators</span></span>

```
GET https://api.securitycenter.microsoft.com/api/indicators
```

<span data-ttu-id="80f5e-148">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="80f5e-148">**Response**</span></span>

<span data-ttu-id="80f5e-149">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="80f5e-149">Here is an example of the response.</span></span>

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

## <a name="example-2"></a><span data-ttu-id="80f5e-150">Exemple 2 :</span><span class="sxs-lookup"><span data-stu-id="80f5e-150">Example 2:</span></span>

<span data-ttu-id="80f5e-151">**Demande**</span><span class="sxs-lookup"><span data-stu-id="80f5e-151">**Request**</span></span>

<span data-ttu-id="80f5e-152">Voici un exemple de demande qui obtient tous les indicateurs avec l’action « AlertAndBlock »</span><span class="sxs-lookup"><span data-stu-id="80f5e-152">Here is an example of a request that gets all Indicators with 'AlertAndBlock' action</span></span> 

```
GET https://api.securitycenter.microsoft.com/api/indicators?$filter=action+eq+'AlertAndBlock'
```

<span data-ttu-id="80f5e-153">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="80f5e-153">**Response**</span></span>

<span data-ttu-id="80f5e-154">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="80f5e-154">Here is an example of the response.</span></span>

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
