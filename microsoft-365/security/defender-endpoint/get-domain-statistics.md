---
title: API Obtenir les statistiques de domaine
description: Découvrez comment utiliser l’API Obtenir des statistiques de domaine pour récupérer les statistiques sur le domaine donné dans Microsoft Defender for Endpoint.
keywords: api, api de graphique, api pris en charge, obtenir, domaine, appareils associés à un domaine
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
ms.openlocfilehash: eef06657d7f691a89e5985640431c2cc706557b4
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166707"
---
# <a name="get-domain-statistics-api"></a><span data-ttu-id="38a51-104">API Obtenir les statistiques de domaine</span><span class="sxs-lookup"><span data-stu-id="38a51-104">Get domain statistics API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="38a51-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="38a51-105">**Applies to:**</span></span>
- [<span data-ttu-id="38a51-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="38a51-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="38a51-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="38a51-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="38a51-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="38a51-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="38a51-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="38a51-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="38a51-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="38a51-110">API description</span></span>
<span data-ttu-id="38a51-111">Récupère les statistiques sur le domaine donné.</span><span class="sxs-lookup"><span data-stu-id="38a51-111">Retrieves the statistics on the given domain.</span></span>


## <a name="limitations"></a><span data-ttu-id="38a51-112">Limites</span><span class="sxs-lookup"><span data-stu-id="38a51-112">Limitations</span></span>
1. <span data-ttu-id="38a51-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="38a51-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="38a51-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="38a51-114">Permissions</span></span>
<span data-ttu-id="38a51-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="38a51-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="38a51-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="38a51-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="38a51-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="38a51-117">Permission type</span></span> |   <span data-ttu-id="38a51-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="38a51-118">Permission</span></span>  |   <span data-ttu-id="38a51-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="38a51-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="38a51-120">Application</span><span class="sxs-lookup"><span data-stu-id="38a51-120">Application</span></span> |   <span data-ttu-id="38a51-121">URL. Read.All</span><span class="sxs-lookup"><span data-stu-id="38a51-121">URL.Read.All</span></span> |  <span data-ttu-id="38a51-122">« Lire les URL »</span><span class="sxs-lookup"><span data-stu-id="38a51-122">'Read URLs'</span></span>
<span data-ttu-id="38a51-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="38a51-123">Delegated (work or school account)</span></span> | <span data-ttu-id="38a51-124">URL. Read.All</span><span class="sxs-lookup"><span data-stu-id="38a51-124">URL.Read.All</span></span> | <span data-ttu-id="38a51-125">« Lire les URL »</span><span class="sxs-lookup"><span data-stu-id="38a51-125">'Read URLs'</span></span>

>[!Note]
> <span data-ttu-id="38a51-126">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="38a51-126">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="38a51-127">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="38a51-127">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="38a51-128">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="38a51-128">HTTP request</span></span>
```
GET /api/domains/{domain}/stats
```

## <a name="request-headers"></a><span data-ttu-id="38a51-129">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="38a51-129">Request headers</span></span>

<span data-ttu-id="38a51-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="38a51-130">Header</span></span> | <span data-ttu-id="38a51-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="38a51-131">Value</span></span> 
:---|:---
<span data-ttu-id="38a51-132">Autorisation</span><span class="sxs-lookup"><span data-stu-id="38a51-132">Authorization</span></span> | <span data-ttu-id="38a51-133">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="38a51-133">Bearer {token}.</span></span> <span data-ttu-id="38a51-134">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="38a51-134">**Required**.</span></span>

## <a name="request-uri-parameters"></a><span data-ttu-id="38a51-135">Paramètres d’URI de demande</span><span class="sxs-lookup"><span data-stu-id="38a51-135">Request URI parameters</span></span>

<span data-ttu-id="38a51-136">Nom</span><span class="sxs-lookup"><span data-stu-id="38a51-136">Name</span></span> | <span data-ttu-id="38a51-137">Type</span><span class="sxs-lookup"><span data-stu-id="38a51-137">Type</span></span> | <span data-ttu-id="38a51-138">Description</span><span class="sxs-lookup"><span data-stu-id="38a51-138">Description</span></span>
:---|:---|:---
<span data-ttu-id="38a51-139">lookBackHours</span><span class="sxs-lookup"><span data-stu-id="38a51-139">lookBackHours</span></span> | <span data-ttu-id="38a51-140">Int32</span><span class="sxs-lookup"><span data-stu-id="38a51-140">Int32</span></span> | <span data-ttu-id="38a51-141">Définit les heures que nous allons rechercher pour obtenir les statistiques.</span><span class="sxs-lookup"><span data-stu-id="38a51-141">Defines the hours we search back to get the statistics.</span></span> <span data-ttu-id="38a51-142">La valeur par défaut est 30 jours.</span><span class="sxs-lookup"><span data-stu-id="38a51-142">Defaults to 30 days.</span></span> <span data-ttu-id="38a51-143">**Facultatif**.</span><span class="sxs-lookup"><span data-stu-id="38a51-143">**Optional**.</span></span>

## <a name="request-body"></a><span data-ttu-id="38a51-144">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="38a51-144">Request body</span></span>
<span data-ttu-id="38a51-145">Vide</span><span class="sxs-lookup"><span data-stu-id="38a51-145">Empty</span></span>

## <a name="response"></a><span data-ttu-id="38a51-146">Réponse</span><span class="sxs-lookup"><span data-stu-id="38a51-146">Response</span></span>
<span data-ttu-id="38a51-147">En cas de réussite et si le domaine existe : 200 - OK, avec un objet statistiques dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="38a51-147">If successful and domain exists - 200 OK, with statistics object in the response body.</span></span> <span data-ttu-id="38a51-148">Si le domaine n’existe pas - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="38a51-148">If domain does not exist - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="38a51-149">Exemple</span><span class="sxs-lookup"><span data-stu-id="38a51-149">Example</span></span>

<span data-ttu-id="38a51-150">**Demande**</span><span class="sxs-lookup"><span data-stu-id="38a51-150">**Request**</span></span>

<span data-ttu-id="38a51-151">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="38a51-151">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/domains/example.com/stats?lookBackHours=48
```

<span data-ttu-id="38a51-152">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="38a51-152">**Response**</span></span>

<span data-ttu-id="38a51-153">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="38a51-153">Here is an example of the response.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#microsoft.windowsDefenderATP.api.InOrgDomainStats",
    "host": "example.com",
    "orgPrevalence": "4070",
    "orgFirstSeen": "2017-07-30T13:23:48Z",
    "orgLastSeen": "2017-08-29T13:09:05Z"
}
```
