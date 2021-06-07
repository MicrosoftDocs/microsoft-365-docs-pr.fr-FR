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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: d2edc5d429d124412134b466753b65506d2dd7a9
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52772184"
---
# <a name="get-domain-statistics-api"></a><span data-ttu-id="f93b5-104">API Obtenir les statistiques de domaine</span><span class="sxs-lookup"><span data-stu-id="f93b5-104">Get domain statistics API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f93b5-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f93b5-105">**Applies to:**</span></span>
- [<span data-ttu-id="f93b5-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f93b5-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="f93b5-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f93b5-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="f93b5-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="f93b5-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="f93b5-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f93b5-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="f93b5-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="f93b5-110">API description</span></span>
<span data-ttu-id="f93b5-111">Récupère les statistiques sur le domaine donné.</span><span class="sxs-lookup"><span data-stu-id="f93b5-111">Retrieves the statistics on the given domain.</span></span>


## <a name="limitations"></a><span data-ttu-id="f93b5-112">Limitations</span><span class="sxs-lookup"><span data-stu-id="f93b5-112">Limitations</span></span>
1. <span data-ttu-id="f93b5-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="f93b5-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="f93b5-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="f93b5-114">Permissions</span></span>
<span data-ttu-id="f93b5-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="f93b5-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="f93b5-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="f93b5-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="f93b5-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="f93b5-117">Permission type</span></span> |   <span data-ttu-id="f93b5-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="f93b5-118">Permission</span></span>  |   <span data-ttu-id="f93b5-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="f93b5-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="f93b5-120">Application</span><span class="sxs-lookup"><span data-stu-id="f93b5-120">Application</span></span> |   <span data-ttu-id="f93b5-121">URL. Read.All</span><span class="sxs-lookup"><span data-stu-id="f93b5-121">URL.Read.All</span></span> |  <span data-ttu-id="f93b5-122">« Lire les URL »</span><span class="sxs-lookup"><span data-stu-id="f93b5-122">'Read URLs'</span></span>
<span data-ttu-id="f93b5-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="f93b5-123">Delegated (work or school account)</span></span> | <span data-ttu-id="f93b5-124">URL. Read.All</span><span class="sxs-lookup"><span data-stu-id="f93b5-124">URL.Read.All</span></span> | <span data-ttu-id="f93b5-125">« Lire les URL »</span><span class="sxs-lookup"><span data-stu-id="f93b5-125">'Read URLs'</span></span>

>[!Note]
> <span data-ttu-id="f93b5-126">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="f93b5-126">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="f93b5-127">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="f93b5-127">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="f93b5-128">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="f93b5-128">HTTP request</span></span>
```
GET /api/domains/{domain}/stats
```

## <a name="request-headers"></a><span data-ttu-id="f93b5-129">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="f93b5-129">Request headers</span></span>

<span data-ttu-id="f93b5-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="f93b5-130">Header</span></span> | <span data-ttu-id="f93b5-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f93b5-131">Value</span></span> 
:---|:---
<span data-ttu-id="f93b5-132">Autorisation</span><span class="sxs-lookup"><span data-stu-id="f93b5-132">Authorization</span></span> | <span data-ttu-id="f93b5-133">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="f93b5-133">Bearer {token}.</span></span> <span data-ttu-id="f93b5-134">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="f93b5-134">**Required**.</span></span>

## <a name="request-uri-parameters"></a><span data-ttu-id="f93b5-135">Paramètres d’URI de demande</span><span class="sxs-lookup"><span data-stu-id="f93b5-135">Request URI parameters</span></span>

<span data-ttu-id="f93b5-136">Nom</span><span class="sxs-lookup"><span data-stu-id="f93b5-136">Name</span></span> | <span data-ttu-id="f93b5-137">Type</span><span class="sxs-lookup"><span data-stu-id="f93b5-137">Type</span></span> | <span data-ttu-id="f93b5-138">Description</span><span class="sxs-lookup"><span data-stu-id="f93b5-138">Description</span></span>
:---|:---|:---
<span data-ttu-id="f93b5-139">lookBackHours</span><span class="sxs-lookup"><span data-stu-id="f93b5-139">lookBackHours</span></span> | <span data-ttu-id="f93b5-140">Int32</span><span class="sxs-lookup"><span data-stu-id="f93b5-140">Int32</span></span> | <span data-ttu-id="f93b5-141">Définit les heures pendant les recherches pour obtenir les statistiques.</span><span class="sxs-lookup"><span data-stu-id="f93b5-141">Defines the hours we search back to get the statistics.</span></span> <span data-ttu-id="f93b5-142">La valeur par défaut est 30 jours.</span><span class="sxs-lookup"><span data-stu-id="f93b5-142">Defaults to 30 days.</span></span> <span data-ttu-id="f93b5-143">**Facultatif**.</span><span class="sxs-lookup"><span data-stu-id="f93b5-143">**Optional**.</span></span>

## <a name="request-body"></a><span data-ttu-id="f93b5-144">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="f93b5-144">Request body</span></span>
<span data-ttu-id="f93b5-145">Vide</span><span class="sxs-lookup"><span data-stu-id="f93b5-145">Empty</span></span>

## <a name="response"></a><span data-ttu-id="f93b5-146">Réponse</span><span class="sxs-lookup"><span data-stu-id="f93b5-146">Response</span></span>
<span data-ttu-id="f93b5-147">En cas de réussite et si le domaine existe : 200 - OK, avec un objet statistiques dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="f93b5-147">If successful and domain exists - 200 OK, with statistics object in the response body.</span></span> <span data-ttu-id="f93b5-148">Si le domaine n’existe pas - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="f93b5-148">If domain does not exist - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="f93b5-149">Exemple</span><span class="sxs-lookup"><span data-stu-id="f93b5-149">Example</span></span>

<span data-ttu-id="f93b5-150">**Demande**</span><span class="sxs-lookup"><span data-stu-id="f93b5-150">**Request**</span></span>

<span data-ttu-id="f93b5-151">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="f93b5-151">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/domains/example.com/stats?lookBackHours=48
```

<span data-ttu-id="f93b5-152">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="f93b5-152">**Response**</span></span>

<span data-ttu-id="f93b5-153">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="f93b5-153">Here is an example of the response.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#microsoft.windowsDefenderATP.api.InOrgDomainStats",
    "host": "example.com",
    "orgPrevalence": "4070",
    "orgFirstSeen": "2017-07-30T13:23:48Z",
    "orgLastSeen": "2017-08-29T13:09:05Z"
}
```
