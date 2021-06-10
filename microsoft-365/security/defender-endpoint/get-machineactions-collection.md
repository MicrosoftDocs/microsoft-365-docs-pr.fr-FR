---
title: List machineActions API
description: Découvrez comment utiliser l’API List MachineActions pour récupérer une collection d’actions de l’ordinateur dans Microsoft Defender pour endpoint.
keywords: api, api de graphique, api pris en charge, collection machineaction
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
ms.openlocfilehash: 2ee9a4e29dded3e299ffbb2c2997fd02f32d1abf
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52771116"
---
# <a name="list-machineactions-api"></a><span data-ttu-id="8c5cf-104">List MachineActions API</span><span class="sxs-lookup"><span data-stu-id="8c5cf-104">List MachineActions API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="8c5cf-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="8c5cf-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="8c5cf-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="8c5cf-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="8c5cf-108">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="8c5cf-108">API description</span></span>
<span data-ttu-id="8c5cf-109">Récupère une collection d’actions [de l’ordinateur.](machineaction.md)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-109">Retrieves a collection of [Machine Actions](machineaction.md).</span></span>
<br><span data-ttu-id="8c5cf-110">Prend [en charge les requêtes OData V4.](https://www.odata.org/documentation/)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-110">Supports [OData V4 queries](https://www.odata.org/documentation/).</span></span>
<br><span data-ttu-id="8c5cf-111">La requête OData est prise en charge sur ```$filter``` : , et les ```status``` ```machineId``` ```type``` ```requestor``` ```creationDateTimeUtc``` propriétés.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-111">The OData's ```$filter``` query is supported on: ```status```, ```machineId```, ```type```, ```requestor``` and ```creationDateTimeUtc``` properties.</span></span>
<br><span data-ttu-id="8c5cf-112">Voir des exemples [dans les requêtes OData avec Microsoft Defender for Endpoint](exposed-apis-odata-samples.md)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-112">See examples at [OData queries with Microsoft Defender for Endpoint](exposed-apis-odata-samples.md)</span></span>


## <a name="limitations"></a><span data-ttu-id="8c5cf-113">Limites</span><span class="sxs-lookup"><span data-stu-id="8c5cf-113">Limitations</span></span>
1. <span data-ttu-id="8c5cf-114">La taille maximale de page est de 10 000.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-114">Maximum page size is 10,000.</span></span>
2. <span data-ttu-id="8c5cf-115">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-115">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span> 


## <a name="permissions"></a><span data-ttu-id="8c5cf-116">Autorisations</span><span class="sxs-lookup"><span data-stu-id="8c5cf-116">Permissions</span></span>
<span data-ttu-id="8c5cf-117">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-117">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="8c5cf-118">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-118">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="8c5cf-119">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="8c5cf-119">Permission type</span></span> |   <span data-ttu-id="8c5cf-120">Autorisation</span><span class="sxs-lookup"><span data-stu-id="8c5cf-120">Permission</span></span>  |   <span data-ttu-id="8c5cf-121">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="8c5cf-121">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="8c5cf-122">Application</span><span class="sxs-lookup"><span data-stu-id="8c5cf-122">Application</span></span> |   <span data-ttu-id="8c5cf-123">Machine.Read.All</span><span class="sxs-lookup"><span data-stu-id="8c5cf-123">Machine.Read.All</span></span> |  <span data-ttu-id="8c5cf-124">« Lire tous les profils d’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="8c5cf-124">'Read all machine profiles'</span></span>
<span data-ttu-id="8c5cf-125">Application</span><span class="sxs-lookup"><span data-stu-id="8c5cf-125">Application</span></span> |   <span data-ttu-id="8c5cf-126">Machine.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8c5cf-126">Machine.ReadWrite.All</span></span> | <span data-ttu-id="8c5cf-127">« Lire et écrire toutes les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="8c5cf-127">'Read and write all machine information'</span></span>
<span data-ttu-id="8c5cf-128">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-128">Delegated (work or school account)</span></span> | <span data-ttu-id="8c5cf-129">Machine.Read</span><span class="sxs-lookup"><span data-stu-id="8c5cf-129">Machine.Read</span></span> | <span data-ttu-id="8c5cf-130">« Lire les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="8c5cf-130">'Read machine information'</span></span>
<span data-ttu-id="8c5cf-131">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-131">Delegated (work or school account)</span></span> | <span data-ttu-id="8c5cf-132">Machine.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8c5cf-132">Machine.ReadWrite</span></span> | <span data-ttu-id="8c5cf-133">« Lire et écrire des informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="8c5cf-133">'Read and write machine information'</span></span>

>[!Note]
> <span data-ttu-id="8c5cf-134">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="8c5cf-134">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="8c5cf-135">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-135">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="8c5cf-136">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="8c5cf-136">HTTP request</span></span>
```
GET https://api.securitycenter.microsoft.com/api/machineactions
```

## <a name="request-headers"></a><span data-ttu-id="8c5cf-137">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="8c5cf-137">Request headers</span></span>

<span data-ttu-id="8c5cf-138">Nom</span><span class="sxs-lookup"><span data-stu-id="8c5cf-138">Name</span></span> | <span data-ttu-id="8c5cf-139">Type</span><span class="sxs-lookup"><span data-stu-id="8c5cf-139">Type</span></span> | <span data-ttu-id="8c5cf-140">Description</span><span class="sxs-lookup"><span data-stu-id="8c5cf-140">Description</span></span>
:---|:---|:---
<span data-ttu-id="8c5cf-141">Autorisation</span><span class="sxs-lookup"><span data-stu-id="8c5cf-141">Authorization</span></span> | <span data-ttu-id="8c5cf-142">String</span><span class="sxs-lookup"><span data-stu-id="8c5cf-142">String</span></span> | <span data-ttu-id="8c5cf-143">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-143">Bearer {token}.</span></span> <span data-ttu-id="8c5cf-144">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-144">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="8c5cf-145">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="8c5cf-145">Request body</span></span>
<span data-ttu-id="8c5cf-146">Vide</span><span class="sxs-lookup"><span data-stu-id="8c5cf-146">Empty</span></span>

## <a name="response"></a><span data-ttu-id="8c5cf-147">Réponse</span><span class="sxs-lookup"><span data-stu-id="8c5cf-147">Response</span></span>
<span data-ttu-id="8c5cf-148">Si elle réussit, cette méthode renvoie le code de réponse 200, Ok avec une collection [d’entités machineAction.](machineaction.md)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-148">If successful, this method returns 200, Ok response code with a collection of [machineAction](machineaction.md) entities.</span></span>


## <a name="example-1"></a><span data-ttu-id="8c5cf-149">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="8c5cf-149">Example 1</span></span>

<span data-ttu-id="8c5cf-150">**Demande**</span><span class="sxs-lookup"><span data-stu-id="8c5cf-150">**Request**</span></span>

<span data-ttu-id="8c5cf-151">Voici un exemple de demande sur une organisation qui possède trois MachineActions.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-151">Here is an example of the request on an organization that has three MachineActions.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/machineactions
```

<span data-ttu-id="8c5cf-152">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="8c5cf-152">**Response**</span></span>

<span data-ttu-id="8c5cf-153">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-153">Here is an example of the response.</span></span>


```
HTTP/1.1 200 Ok
Content-type: application/json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#MachineActions",
    "value": [
        {
            "id": "69dc3630-1ccc-4342-acf3-35286eec741d",
            "type": "CollectInvestigationPackage",
            "scope": null,
            "requestor": "Analyst@contoso.com",
            "requestorComment": "test",
            "status": "Succeeded",
            "machineId": "f46b9bb259ed4a7fb9981b73510e3cc7aa81ec1f",
            "computerDnsName": "desktop-39g9tgl",
            "creationDateTimeUtc": "2018-12-04T12:43:57.2011911Z",
            "lastUpdateTimeUtc": "2018-12-04T12:45:25.4049122Z",
            "relatedFileInfo": null
        },
        {
            "id": "2e9da30d-27f6-4208-81f2-9cd3d67893ba",
            "type": "RunAntiVirusScan",
            "scope": "Full",
            "requestor": "Analyst@contoso.com",
            "requestorComment": "Check machine for viruses due to alert 3212",
            "status": "Succeeded",
            "machineId": "f46b9bb259ed4a7fb9981b73510e3cc7aa81ec1f",
            "computerDnsName": "desktop-39g9tgl",
            "creationDateTimeUtc": "2018-12-04T12:18:27.1293487Z",
            "lastUpdateTimeUtc": "2018-12-04T12:18:57.5511934Z",
            "relatedFileInfo": null
        },
        {
            "id": "44cffc15-0e3d-4cbf-96aa-bf76f9b27f5e",
            "type": "StopAndQuarantineFile",
            "scope": null,
            "requestor": "Analyst@contoso.com",
            "requestorComment": "test",
            "status": "Succeeded",
            "machineId": "f46b9bb259ed4a7fb9981b73510e3cc7aa81ec1f",
            "computerDnsName": "desktop-39g9tgl",
            "creationDateTimeUtc": "2018-12-04T12:15:40.6052029Z",
            "lastUpdateTimeUtc": "2018-12-04T12:16:14.2899973Z",
            "relatedFileInfo": {
                "fileIdentifier": "a0c659857ccbe457fdaf5fe21d54efdcbf6f6508",
                "fileIdentifierType": "Sha1"
            }
        }
    ]
}
```

## <a name="example-2"></a><span data-ttu-id="8c5cf-154">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="8c5cf-154">Example 2</span></span>

<span data-ttu-id="8c5cf-155">**Demande**</span><span class="sxs-lookup"><span data-stu-id="8c5cf-155">**Request**</span></span>

<span data-ttu-id="8c5cf-156">Voici un exemple de demande qui filtre les MachineActions par ID d’ordinateur et affiche les deux derniers MachineActions.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-156">Here is an example of a request that filters the MachineActions by machine ID and shows the latest two MachineActions.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/machineactions?$filter=machineId eq 'f46b9bb259ed4a7fb9981b73510e3cc7aa81ec1f'&$top=2
```

<span data-ttu-id="8c5cf-157">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="8c5cf-157">**Response**</span></span>

<span data-ttu-id="8c5cf-158">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-158">Here is an example of the response.</span></span>

```
HTTP/1.1 200 Ok
Content-type: application/json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#MachineActions",
    "value": [
        {
            "id": "69dc3630-1ccc-4342-acf3-35286eec741d",
            "type": "CollectInvestigationPackage",
            "scope": null,
            "requestor": "Analyst@contoso.com",
            "requestorComment": "test",
            "status": "Succeeded",
            "machineId": "f46b9bb259ed4a7fb9981b73510e3cc7aa81ec1f",
            "computerDnsName": "desktop-39g9tgl",
            "creationDateTimeUtc": "2018-12-04T12:43:57.2011911Z",
            "lastUpdateTimeUtc": "2018-12-04T12:45:25.4049122Z",
            "relatedFileInfo": null
        },
        {
            "id": "2e9da30d-27f6-4208-81f2-9cd3d67893ba",
            "type": "RunAntiVirusScan",
            "scope": "Full",
            "requestor": "Analyst@contoso.com",
            "requestorComment": "Check machine for viruses due to alert 3212",
            "status": "Succeeded",
            "machineId": "f46b9bb259ed4a7fb9981b73510e3cc7aa81ec1f",
            "computerDnsName": "desktop-39g9tgl",
            "creationDateTimeUtc": "2018-12-04T12:18:27.1293487Z",
            "lastUpdateTimeUtc": "2018-12-04T12:18:57.5511934Z",
            "relatedFileInfo": null
        }
    ]
}
```

## <a name="related-topics"></a><span data-ttu-id="8c5cf-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c5cf-159">Related topics</span></span>
- [<span data-ttu-id="8c5cf-160">Requêtes OData avec Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8c5cf-160">OData queries with Microsoft Defender for Endpoint</span></span>](exposed-apis-odata-samples.md)
