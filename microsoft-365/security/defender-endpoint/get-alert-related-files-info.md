---
title: Obtenir des informations sur les fichiers associés à une alerte
description: Récupérez tous les fichiers liés à une alerte spécifique à l’aide de Microsoft Defender for Endpoint.
keywords: api, api de graphique, api pris en charge, obtenir des informations d’alerte, informations d’alerte, fichiers associés
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 369dd35c65094d5a5985b471bec506cb5d266e59
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52772348"
---
# <a name="get-alert-related-files-information-api"></a><span data-ttu-id="3a550-104">API Obtenir les informations sur les fichiers associés à une alerte</span><span class="sxs-lookup"><span data-stu-id="3a550-104">Get alert related files information API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="3a550-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3a550-105">**Applies to:**</span></span>
- [<span data-ttu-id="3a550-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3a550-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="3a550-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3a550-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)
 
> <span data-ttu-id="3a550-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="3a550-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="3a550-109">Inscrivez-vous pour une version d’essai gratuite.</span><span class="sxs-lookup"><span data-stu-id="3a550-109">Sign up for free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 


[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="3a550-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="3a550-110">API description</span></span>
<span data-ttu-id="3a550-111">Récupère tous les fichiers liés à une alerte spécifique.</span><span class="sxs-lookup"><span data-stu-id="3a550-111">Retrieves all files related to a specific alert.</span></span>


## <a name="limitations"></a><span data-ttu-id="3a550-112">Limitations</span><span class="sxs-lookup"><span data-stu-id="3a550-112">Limitations</span></span>
1. <span data-ttu-id="3a550-113">Vous pouvez interroger la dernière mise à jour des alertes en fonction de votre période de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="3a550-113">You can query on alerts last updated according to your configured retention period.</span></span>
2. <span data-ttu-id="3a550-114">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="3a550-114">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="3a550-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="3a550-115">Permissions</span></span>
<span data-ttu-id="3a550-116">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="3a550-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="3a550-117">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="3a550-117">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="3a550-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="3a550-118">Permission type</span></span> | <span data-ttu-id="3a550-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="3a550-119">Permission</span></span> | <span data-ttu-id="3a550-120">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="3a550-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="3a550-121">Application</span><span class="sxs-lookup"><span data-stu-id="3a550-121">Application</span></span> | <span data-ttu-id="3a550-122">File.Read.All</span><span class="sxs-lookup"><span data-stu-id="3a550-122">File.Read.All</span></span> | <span data-ttu-id="3a550-123">« Lire les profils de fichiers »</span><span class="sxs-lookup"><span data-stu-id="3a550-123">'Read file profiles'</span></span>
<span data-ttu-id="3a550-124">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="3a550-124">Delegated (work or school account)</span></span> | <span data-ttu-id="3a550-125">File.Read.All</span><span class="sxs-lookup"><span data-stu-id="3a550-125">File.Read.All</span></span> | <span data-ttu-id="3a550-126">« Lire les profils de fichiers »</span><span class="sxs-lookup"><span data-stu-id="3a550-126">'Read file profiles'</span></span>

>[!Note]
> <span data-ttu-id="3a550-127">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="3a550-127">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="3a550-128">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="3a550-128">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="3a550-129">L’utilisateur doit avoir accès à l’appareil associé à l’alerte, en fonction des paramètres de groupe d’appareils (pour plus d’informations, voir Créer et gérer des groupes d’appareils) [](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="3a550-129">The user needs to have access to the device associated with the alert, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="3a550-130">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="3a550-130">HTTP request</span></span>
```
GET /api/alerts/{id}/files
```

## <a name="request-headers"></a><span data-ttu-id="3a550-131">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="3a550-131">Request headers</span></span>

<span data-ttu-id="3a550-132">Nom</span><span class="sxs-lookup"><span data-stu-id="3a550-132">Name</span></span> | <span data-ttu-id="3a550-133">Type</span><span class="sxs-lookup"><span data-stu-id="3a550-133">Type</span></span> | <span data-ttu-id="3a550-134">Description</span><span class="sxs-lookup"><span data-stu-id="3a550-134">Description</span></span>
:---|:---|:---
<span data-ttu-id="3a550-135">Autorisation</span><span class="sxs-lookup"><span data-stu-id="3a550-135">Authorization</span></span> | <span data-ttu-id="3a550-136">String</span><span class="sxs-lookup"><span data-stu-id="3a550-136">String</span></span> | <span data-ttu-id="3a550-137">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="3a550-137">Bearer {token}.</span></span> <span data-ttu-id="3a550-138">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="3a550-138">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="3a550-139">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="3a550-139">Request body</span></span>
<span data-ttu-id="3a550-140">Vide</span><span class="sxs-lookup"><span data-stu-id="3a550-140">Empty</span></span>

## <a name="response"></a><span data-ttu-id="3a550-141">Réponse</span><span class="sxs-lookup"><span data-stu-id="3a550-141">Response</span></span>
<span data-ttu-id="3a550-142">En cas de réussite et si l’alerte et les fichiers existent : 200 - OK.</span><span class="sxs-lookup"><span data-stu-id="3a550-142">If successful and alert and files exist - 200 OK.</span></span> <span data-ttu-id="3a550-143">Si l’alerte est in trouvée - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="3a550-143">If alert not found - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="3a550-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="3a550-144">Example</span></span>

<span data-ttu-id="3a550-145">**Demande**</span><span class="sxs-lookup"><span data-stu-id="3a550-145">**Request**</span></span>

<span data-ttu-id="3a550-146">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="3a550-146">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/alerts/636688558380765161_2136280442/files
```

<span data-ttu-id="3a550-147">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="3a550-147">**Response**</span></span>

<span data-ttu-id="3a550-148">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="3a550-148">Here is an example of the response.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Files",
    "value": [
        {
            "sha1": "f2a00fd2f2de1be0214b8529f1e9f67096c1aa70",
            "sha256": "dcd71ef5fff4362a9f64cf3f96f14f2b11d6f428f3badbedcb9ff3361e7079aa",
            "md5": "8d5b7cc9a832e21d22503057e1fec8e9",
            "globalPrevalence": 29,
            "globalFirstObserved": "2019-03-23T23:54:06.0135204Z",
            "globalLastObserved": "2019-04-23T00:43:20.0489831Z",
            "size": 113984,
            "fileType": null,
            "isPeFile": true,
            "filePublisher": "Microsoft Corporation",
            "fileProductName": "Microsoft� Windows� Operating System",
            "signer": "Microsoft Corporation",
            "issuer": "Microsoft Code Signing PCA",
            "signerHash": "9dc17888b5cfad98b3cb35c1994e96227f061675",
            "isValidCertificate": true,
            "determinationType": "Unknown",
            "determinationValue": null
        }
        ...
    ]
}
```
