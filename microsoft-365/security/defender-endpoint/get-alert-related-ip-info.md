---
title: Obtenir les informations d’IPS associées aux alertes
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
ms.technology: mde
ms.openlocfilehash: 970f82038bd7feb4f0c568ed13b285f75bf1ab19
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166666"
---
# <a name="get-alert-related-ips-information-api"></a><span data-ttu-id="b736b-104">API Obtenir les informations sur les IPS associées aux alertes</span><span class="sxs-lookup"><span data-stu-id="b736b-104">Get alert related IPs information API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="b736b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b736b-105">**Applies to:**</span></span>
- [<span data-ttu-id="b736b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b736b-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="b736b-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b736b-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="b736b-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="b736b-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="b736b-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="b736b-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 


[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="b736b-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="b736b-110">API description</span></span>
<span data-ttu-id="b736b-111">Récupère toutes les IP associées à une alerte spécifique.</span><span class="sxs-lookup"><span data-stu-id="b736b-111">Retrieves all IPs related to a specific alert.</span></span>


## <a name="limitations"></a><span data-ttu-id="b736b-112">Limites</span><span class="sxs-lookup"><span data-stu-id="b736b-112">Limitations</span></span>
1. <span data-ttu-id="b736b-113">Vous pouvez interroger la dernière mise à jour des alertes en fonction de votre période de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="b736b-113">You can query on alerts last updated according to your configured retention period.</span></span>
2. <span data-ttu-id="b736b-114">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="b736b-114">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="b736b-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="b736b-115">Permissions</span></span>
<span data-ttu-id="b736b-116">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="b736b-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="b736b-117">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="b736b-117">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="b736b-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="b736b-118">Permission type</span></span> |   <span data-ttu-id="b736b-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="b736b-119">Permission</span></span>  |   <span data-ttu-id="b736b-120">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="b736b-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="b736b-121">Application</span><span class="sxs-lookup"><span data-stu-id="b736b-121">Application</span></span> |   <span data-ttu-id="b736b-122">Ip.Read.All</span><span class="sxs-lookup"><span data-stu-id="b736b-122">Ip.Read.All</span></span> |   <span data-ttu-id="b736b-123">« Lire les profils d’adresse IP »</span><span class="sxs-lookup"><span data-stu-id="b736b-123">'Read IP address profiles'</span></span>
<span data-ttu-id="b736b-124">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="b736b-124">Delegated (work or school account)</span></span> | <span data-ttu-id="b736b-125">Ip.Read.All</span><span class="sxs-lookup"><span data-stu-id="b736b-125">Ip.Read.All</span></span> |  <span data-ttu-id="b736b-126">« Lire les profils d’adresse IP »</span><span class="sxs-lookup"><span data-stu-id="b736b-126">'Read IP address profiles'</span></span>

>[!Note]
> <span data-ttu-id="b736b-127">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="b736b-127">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="b736b-128">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="b736b-128">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="b736b-129">L’utilisateur doit avoir accès à l’appareil associé à l’alerte, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="b736b-129">The user needs to have access to the device associated with the alert, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="b736b-130">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="b736b-130">HTTP request</span></span>
```
GET /api/alerts/{id}/ips
```

## <a name="request-headers"></a><span data-ttu-id="b736b-131">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="b736b-131">Request headers</span></span>

<span data-ttu-id="b736b-132">Nom</span><span class="sxs-lookup"><span data-stu-id="b736b-132">Name</span></span> | <span data-ttu-id="b736b-133">Type</span><span class="sxs-lookup"><span data-stu-id="b736b-133">Type</span></span> | <span data-ttu-id="b736b-134">Description</span><span class="sxs-lookup"><span data-stu-id="b736b-134">Description</span></span>
:---|:---|:---
<span data-ttu-id="b736b-135">Autorisation</span><span class="sxs-lookup"><span data-stu-id="b736b-135">Authorization</span></span> | <span data-ttu-id="b736b-136">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b736b-136">String</span></span> | <span data-ttu-id="b736b-137">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="b736b-137">Bearer {token}.</span></span> <span data-ttu-id="b736b-138">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="b736b-138">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="b736b-139">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="b736b-139">Request body</span></span>
<span data-ttu-id="b736b-140">Vide</span><span class="sxs-lookup"><span data-stu-id="b736b-140">Empty</span></span>

## <a name="response"></a><span data-ttu-id="b736b-141">Réponse</span><span class="sxs-lookup"><span data-stu-id="b736b-141">Response</span></span>
<span data-ttu-id="b736b-142">En cas de réussite et si une alerte et une adresse IP existent : 200 - OK.</span><span class="sxs-lookup"><span data-stu-id="b736b-142">If successful and alert and an IP exist - 200 OK.</span></span> <span data-ttu-id="b736b-143">Si l’alerte est in trouvée - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="b736b-143">If alert not found - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="b736b-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="b736b-144">Example</span></span>

<span data-ttu-id="b736b-145">**Demande**</span><span class="sxs-lookup"><span data-stu-id="b736b-145">**Request**</span></span>

<span data-ttu-id="b736b-146">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="b736b-146">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/alerts/636688558380765161_2136280442/ips
```

<span data-ttu-id="b736b-147">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="b736b-147">**Response**</span></span>

<span data-ttu-id="b736b-148">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="b736b-148">Here is an example of the response.</span></span>


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
