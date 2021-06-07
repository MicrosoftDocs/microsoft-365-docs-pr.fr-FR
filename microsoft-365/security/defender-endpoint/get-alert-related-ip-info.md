---
title: Obtenir les informations des IP liées à l’alerte
description: Récupérez toutes les IP associées à une alerte spécifique à l’aide de Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir des informations d’alerte, informations d’alerte, adresse IP associée
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
ms.openlocfilehash: b6ac9746ff82f81772505daac7d7f36249687d7d
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52772328"
---
# <a name="get-alert-related-ips-information-api"></a><span data-ttu-id="1e1a5-104">API Obtenir les informations sur les IPS associées aux alertes</span><span class="sxs-lookup"><span data-stu-id="1e1a5-104">Get alert related IPs information API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="1e1a5-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1e1a5-105">**Applies to:**</span></span>
- [<span data-ttu-id="1e1a5-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1e1a5-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="1e1a5-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1e1a5-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="1e1a5-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="1e1a5-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="1e1a5-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="1e1a5-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 


[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="1e1a5-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="1e1a5-110">API description</span></span>
<span data-ttu-id="1e1a5-111">Récupère toutes les IP associées à une alerte spécifique.</span><span class="sxs-lookup"><span data-stu-id="1e1a5-111">Retrieves all IPs related to a specific alert.</span></span>


## <a name="limitations"></a><span data-ttu-id="1e1a5-112">Limitations</span><span class="sxs-lookup"><span data-stu-id="1e1a5-112">Limitations</span></span>
1. <span data-ttu-id="1e1a5-113">Vous pouvez interroger la dernière mise à jour des alertes en fonction de votre période de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="1e1a5-113">You can query on alerts last updated according to your configured retention period.</span></span>
2. <span data-ttu-id="1e1a5-114">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="1e1a5-114">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="1e1a5-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="1e1a5-115">Permissions</span></span>
<span data-ttu-id="1e1a5-116">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="1e1a5-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="1e1a5-117">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="1e1a5-117">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="1e1a5-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="1e1a5-118">Permission type</span></span> |   <span data-ttu-id="1e1a5-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="1e1a5-119">Permission</span></span>  |   <span data-ttu-id="1e1a5-120">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="1e1a5-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="1e1a5-121">Application</span><span class="sxs-lookup"><span data-stu-id="1e1a5-121">Application</span></span> |   <span data-ttu-id="1e1a5-122">Ip.Read.All</span><span class="sxs-lookup"><span data-stu-id="1e1a5-122">Ip.Read.All</span></span> |   <span data-ttu-id="1e1a5-123">« Lire les profils d’adresse IP »</span><span class="sxs-lookup"><span data-stu-id="1e1a5-123">'Read IP address profiles'</span></span>
<span data-ttu-id="1e1a5-124">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="1e1a5-124">Delegated (work or school account)</span></span> | <span data-ttu-id="1e1a5-125">Ip.Read.All</span><span class="sxs-lookup"><span data-stu-id="1e1a5-125">Ip.Read.All</span></span> |  <span data-ttu-id="1e1a5-126">« Lire les profils d’adresse IP »</span><span class="sxs-lookup"><span data-stu-id="1e1a5-126">'Read IP address profiles'</span></span>

>[!Note]
> <span data-ttu-id="1e1a5-127">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="1e1a5-127">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="1e1a5-128">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="1e1a5-128">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="1e1a5-129">L’utilisateur doit avoir accès à l’appareil associé à l’alerte, en fonction des paramètres de groupe d’appareils (pour plus d’informations, voir Créer et gérer des groupes d’appareils) [](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="1e1a5-129">The user needs to have access to the device associated with the alert, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="1e1a5-130">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="1e1a5-130">HTTP request</span></span>
```
GET /api/alerts/{id}/ips
```

## <a name="request-headers"></a><span data-ttu-id="1e1a5-131">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="1e1a5-131">Request headers</span></span>

<span data-ttu-id="1e1a5-132">Nom</span><span class="sxs-lookup"><span data-stu-id="1e1a5-132">Name</span></span> | <span data-ttu-id="1e1a5-133">Type</span><span class="sxs-lookup"><span data-stu-id="1e1a5-133">Type</span></span> | <span data-ttu-id="1e1a5-134">Description</span><span class="sxs-lookup"><span data-stu-id="1e1a5-134">Description</span></span>
:---|:---|:---
<span data-ttu-id="1e1a5-135">Autorisation</span><span class="sxs-lookup"><span data-stu-id="1e1a5-135">Authorization</span></span> | <span data-ttu-id="1e1a5-136">String</span><span class="sxs-lookup"><span data-stu-id="1e1a5-136">String</span></span> | <span data-ttu-id="1e1a5-137">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="1e1a5-137">Bearer {token}.</span></span> <span data-ttu-id="1e1a5-138">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="1e1a5-138">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="1e1a5-139">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="1e1a5-139">Request body</span></span>
<span data-ttu-id="1e1a5-140">Vide</span><span class="sxs-lookup"><span data-stu-id="1e1a5-140">Empty</span></span>

## <a name="response"></a><span data-ttu-id="1e1a5-141">Réponse</span><span class="sxs-lookup"><span data-stu-id="1e1a5-141">Response</span></span>
<span data-ttu-id="1e1a5-142">En cas de réussite et si une alerte et une adresse IP existent : 200 - OK.</span><span class="sxs-lookup"><span data-stu-id="1e1a5-142">If successful and alert and an IP exist - 200 OK.</span></span> <span data-ttu-id="1e1a5-143">Si l’alerte est in trouvée - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="1e1a5-143">If alert not found - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="1e1a5-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="1e1a5-144">Example</span></span>

<span data-ttu-id="1e1a5-145">**Demande**</span><span class="sxs-lookup"><span data-stu-id="1e1a5-145">**Request**</span></span>

<span data-ttu-id="1e1a5-146">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="1e1a5-146">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/alerts/636688558380765161_2136280442/ips
```

<span data-ttu-id="1e1a5-147">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="1e1a5-147">**Response**</span></span>

<span data-ttu-id="1e1a5-148">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="1e1a5-148">Here is an example of the response.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/$metadata#Ips",    
    "value": [
                {
                    "id": "104.80.104.128"
                },
                {
                    "id": "23.203.232.228   
                }
                ...
    ]
}
 
```
