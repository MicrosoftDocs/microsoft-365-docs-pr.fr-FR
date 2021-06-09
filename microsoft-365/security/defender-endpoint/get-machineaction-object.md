---
title: API Obtenir un objet MachineAction
description: Découvrez comment utiliser l’API Obtenir MachineAction pour récupérer une action ordinateur spécifique par son ID dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, objet machineaction
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
ms.openlocfilehash: dcb00d0d2afc7f873ea9c4afa3174ac46babf879
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52770780"
---
# <a name="get-machineaction-api"></a><span data-ttu-id="681ce-104">API Obtenir machineAction</span><span class="sxs-lookup"><span data-stu-id="681ce-104">Get machineAction API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="681ce-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="681ce-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="681ce-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="681ce-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="681ce-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="681ce-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="681ce-108">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="681ce-108">API description</span></span>
<span data-ttu-id="681ce-109">Récupère [l’action de l’ordinateur spécifique](machineaction.md) par son ID.</span><span class="sxs-lookup"><span data-stu-id="681ce-109">Retrieves specific [Machine Action](machineaction.md) by its ID.</span></span>


## <a name="limitations"></a><span data-ttu-id="681ce-110">Limites</span><span class="sxs-lookup"><span data-stu-id="681ce-110">Limitations</span></span>
1. <span data-ttu-id="681ce-111">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="681ce-111">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="681ce-112">Autorisations</span><span class="sxs-lookup"><span data-stu-id="681ce-112">Permissions</span></span>
<span data-ttu-id="681ce-113">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="681ce-113">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="681ce-114">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="681ce-114">To learn more, including how to choose permissions, see [Use Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="681ce-115">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="681ce-115">Permission type</span></span> |   <span data-ttu-id="681ce-116">Autorisation</span><span class="sxs-lookup"><span data-stu-id="681ce-116">Permission</span></span>  |   <span data-ttu-id="681ce-117">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="681ce-117">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="681ce-118">Application</span><span class="sxs-lookup"><span data-stu-id="681ce-118">Application</span></span> |   <span data-ttu-id="681ce-119">Machine.Read.All</span><span class="sxs-lookup"><span data-stu-id="681ce-119">Machine.Read.All</span></span> |  <span data-ttu-id="681ce-120">« Lire tous les profils d’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="681ce-120">'Read all machine profiles'</span></span>
<span data-ttu-id="681ce-121">Application</span><span class="sxs-lookup"><span data-stu-id="681ce-121">Application</span></span> |   <span data-ttu-id="681ce-122">Machine.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="681ce-122">Machine.ReadWrite.All</span></span> | <span data-ttu-id="681ce-123">« Lire et écrire toutes les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="681ce-123">'Read and write all machine information'</span></span>
<span data-ttu-id="681ce-124">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="681ce-124">Delegated (work or school account)</span></span> | <span data-ttu-id="681ce-125">Machine.Read</span><span class="sxs-lookup"><span data-stu-id="681ce-125">Machine.Read</span></span> | <span data-ttu-id="681ce-126">« Lire les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="681ce-126">'Read machine information'</span></span>
<span data-ttu-id="681ce-127">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="681ce-127">Delegated (work or school account)</span></span> | <span data-ttu-id="681ce-128">Machine.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="681ce-128">Machine.ReadWrite</span></span> | <span data-ttu-id="681ce-129">« Lire et écrire des informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="681ce-129">'Read and write machine information'</span></span>

>[!Note]
> <span data-ttu-id="681ce-130">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="681ce-130">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="681ce-131">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="681ce-131">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="681ce-132">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="681ce-132">HTTP request</span></span>
```
GET https://api.securitycenter.microsoft.com/api/machineactions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="681ce-133">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="681ce-133">Request headers</span></span>

<span data-ttu-id="681ce-134">Nom</span><span class="sxs-lookup"><span data-stu-id="681ce-134">Name</span></span> | <span data-ttu-id="681ce-135">Type</span><span class="sxs-lookup"><span data-stu-id="681ce-135">Type</span></span> | <span data-ttu-id="681ce-136">Description</span><span class="sxs-lookup"><span data-stu-id="681ce-136">Description</span></span>
:---|:---|:---
<span data-ttu-id="681ce-137">Autorisation</span><span class="sxs-lookup"><span data-stu-id="681ce-137">Authorization</span></span> | <span data-ttu-id="681ce-138">String</span><span class="sxs-lookup"><span data-stu-id="681ce-138">String</span></span> | <span data-ttu-id="681ce-139">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="681ce-139">Bearer {token}.</span></span> <span data-ttu-id="681ce-140">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="681ce-140">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="681ce-141">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="681ce-141">Request body</span></span>
<span data-ttu-id="681ce-142">Vide</span><span class="sxs-lookup"><span data-stu-id="681ce-142">Empty</span></span>

## <a name="response"></a><span data-ttu-id="681ce-143">Réponse</span><span class="sxs-lookup"><span data-stu-id="681ce-143">Response</span></span>
<span data-ttu-id="681ce-144">Si elle réussit, cette méthode renvoie le code de réponse 200, Ok avec une [entité Action](machineaction.md) de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="681ce-144">If successful, this method returns 200, Ok response code with a [Machine Action](machineaction.md) entity.</span></span> <span data-ttu-id="681ce-145">Si l’entité d’action de l’ordinateur avec l’ID spécifié est in trouvée - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="681ce-145">If machine action entity with the specified id was not found - 404 Not Found.</span></span>

## <a name="example"></a><span data-ttu-id="681ce-146">Exemple</span><span class="sxs-lookup"><span data-stu-id="681ce-146">Example</span></span>

<span data-ttu-id="681ce-147">**Demande**</span><span class="sxs-lookup"><span data-stu-id="681ce-147">**Request**</span></span>

<span data-ttu-id="681ce-148">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="681ce-148">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/machineactions/2e9da30d-27f6-4208-81f2-9cd3d67893ba
```

<span data-ttu-id="681ce-149">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="681ce-149">**Response**</span></span>

<span data-ttu-id="681ce-150">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="681ce-150">Here is an example of the response.</span></span>


```
HTTP/1.1 200 Ok
Content-type: application/json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#MachineActions/$entity",
    "id": "5382f7ea-7557-4ab7-9782-d50480024a4e",
    "type": "Isolate",
    "scope": "Selective",
    "requestor": "Analyst@TestPrd.onmicrosoft.com",
    "requestorComment": "test for docs",
    "status": "Succeeded",
    "machineId": "7b1f4967d9728e5aa3c06a9e617a22a4a5a17378",
    "computerDnsName": "desktop-test",
    "creationDateTimeUtc": "2019-01-02T14:39:38.2262283Z",
    "lastUpdateDateTimeUtc": "2019-01-02T14:40:44.6596267Z",
    "relatedFileInfo": null
}


```
