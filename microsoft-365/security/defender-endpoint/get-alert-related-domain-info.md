---
title: Obtenir les informations des domaines liés à l’alerte
description: Récupérez tous les domaines liés à une alerte spécifique à l’aide de Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir des informations d’alerte, informations d’alerte, domaine associé
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
ms.openlocfilehash: a5f3db65b42d8dc98c11f2ef2c3c5d509340e386
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52771260"
---
# <a name="get-alert-related-domain-information-api"></a><span data-ttu-id="59d54-104">API Obtenir les informations de domaine associées à une alerte</span><span class="sxs-lookup"><span data-stu-id="59d54-104">Get alert related domain information API</span></span>

<span data-ttu-id="59d54-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="59d54-105">**Applies to:**</span></span> 
- [<span data-ttu-id="59d54-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="59d54-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

- <span data-ttu-id="59d54-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="59d54-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="59d54-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="59d54-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="59d54-109">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="59d54-109">API description</span></span>
<span data-ttu-id="59d54-110">Récupère tous les domaines liés à une alerte spécifique.</span><span class="sxs-lookup"><span data-stu-id="59d54-110">Retrieves all domains related to a specific alert.</span></span>


## <a name="limitations"></a><span data-ttu-id="59d54-111">Limitations</span><span class="sxs-lookup"><span data-stu-id="59d54-111">Limitations</span></span>
1. <span data-ttu-id="59d54-112">Vous pouvez interroger la dernière mise à jour des alertes en fonction de votre période de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="59d54-112">You can query on alerts last updated according to your configured retention period.</span></span>
2. <span data-ttu-id="59d54-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="59d54-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="59d54-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="59d54-114">Permissions</span></span>
<span data-ttu-id="59d54-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="59d54-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="59d54-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="59d54-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="59d54-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="59d54-117">Permission type</span></span> | <span data-ttu-id="59d54-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="59d54-118">Permission</span></span> | <span data-ttu-id="59d54-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="59d54-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="59d54-120">Application</span><span class="sxs-lookup"><span data-stu-id="59d54-120">Application</span></span> | <span data-ttu-id="59d54-121">URL. Read.All</span><span class="sxs-lookup"><span data-stu-id="59d54-121">URL.Read.All</span></span> | <span data-ttu-id="59d54-122">« Lire les URL »</span><span class="sxs-lookup"><span data-stu-id="59d54-122">'Read URLs'</span></span>
<span data-ttu-id="59d54-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="59d54-123">Delegated (work or school account)</span></span> | <span data-ttu-id="59d54-124">URL. Read.All</span><span class="sxs-lookup"><span data-stu-id="59d54-124">URL.Read.All</span></span> | <span data-ttu-id="59d54-125">« Lire les URL »</span><span class="sxs-lookup"><span data-stu-id="59d54-125">'Read URLs'</span></span>

>[!Note]
> <span data-ttu-id="59d54-126">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="59d54-126">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="59d54-127">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="59d54-127">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="59d54-128">L’utilisateur doit avoir accès à l’appareil associé à l’alerte, en fonction des paramètres de groupe d’appareils (pour plus d’informations, voir Créer et gérer des groupes d’appareils) [](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="59d54-128">The user needs to have access to the device associated with the alert, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="59d54-129">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="59d54-129">HTTP request</span></span>
```
GET /api/alerts/{id}/domains
```

## <a name="request-headers"></a><span data-ttu-id="59d54-130">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="59d54-130">Request headers</span></span>

<span data-ttu-id="59d54-131">Nom</span><span class="sxs-lookup"><span data-stu-id="59d54-131">Name</span></span> | <span data-ttu-id="59d54-132">Type</span><span class="sxs-lookup"><span data-stu-id="59d54-132">Type</span></span> | <span data-ttu-id="59d54-133">Description</span><span class="sxs-lookup"><span data-stu-id="59d54-133">Description</span></span>
:---|:---|:---
<span data-ttu-id="59d54-134">Autorisation</span><span class="sxs-lookup"><span data-stu-id="59d54-134">Authorization</span></span> | <span data-ttu-id="59d54-135">String</span><span class="sxs-lookup"><span data-stu-id="59d54-135">String</span></span> | <span data-ttu-id="59d54-136">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="59d54-136">Bearer {token}.</span></span> <span data-ttu-id="59d54-137">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="59d54-137">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="59d54-138">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="59d54-138">Request body</span></span>
<span data-ttu-id="59d54-139">Vide</span><span class="sxs-lookup"><span data-stu-id="59d54-139">Empty</span></span>

## <a name="response"></a><span data-ttu-id="59d54-140">Réponse</span><span class="sxs-lookup"><span data-stu-id="59d54-140">Response</span></span>
<span data-ttu-id="59d54-141">En cas de réussite et si l’alerte et le domaine existent : 200 - OK.</span><span class="sxs-lookup"><span data-stu-id="59d54-141">If successful and alert and domain exist - 200 OK.</span></span> <span data-ttu-id="59d54-142">Si l’alerte est in trouvée - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="59d54-142">If alert not found - 404 Not Found.</span></span>

## <a name="example"></a><span data-ttu-id="59d54-143">Exemple</span><span class="sxs-lookup"><span data-stu-id="59d54-143">Example</span></span>

<span data-ttu-id="59d54-144">**Demande**</span><span class="sxs-lookup"><span data-stu-id="59d54-144">**Request**</span></span>

<span data-ttu-id="59d54-145">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="59d54-145">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/alerts/636688558380765161_2136280442/domains
```

<span data-ttu-id="59d54-146">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="59d54-146">**Response**</span></span>

<span data-ttu-id="59d54-147">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="59d54-147">Here is an example of the response.</span></span>

```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/$metadata#Domains",
    "value": [
        {
            "host": "www.example.com"
        },
        {
            "host": "www.example2.com"
        }
        ...
    ]
}

```
