---
title: API Obtenir des statistiques IP
description: Obtenez les dernières statistiques de votre adresse IP à l’aide de Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, ip, statistiques, prévalence
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
ms.openlocfilehash: 55bf10d01093c17ba2d186ce0a1d1313db2c3a75
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52770084"
---
# <a name="get-ip-statistics-api"></a><span data-ttu-id="555e4-104">API Obtenir des statistiques IP</span><span class="sxs-lookup"><span data-stu-id="555e4-104">Get IP statistics API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="555e4-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="555e4-105">**Applies to:**</span></span>
- [<span data-ttu-id="555e4-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="555e4-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="555e4-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="555e4-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="555e4-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="555e4-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="555e4-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="555e4-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="555e4-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="555e4-110">API description</span></span>
<span data-ttu-id="555e4-111">Récupère les statistiques de l’adresse IP donnée.</span><span class="sxs-lookup"><span data-stu-id="555e4-111">Retrieves the statistics for the given IP.</span></span>

## <a name="limitations"></a><span data-ttu-id="555e4-112">Limites</span><span class="sxs-lookup"><span data-stu-id="555e4-112">Limitations</span></span>
1. <span data-ttu-id="555e4-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="555e4-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>

## <a name="permissions"></a><span data-ttu-id="555e4-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="555e4-114">Permissions</span></span>
<span data-ttu-id="555e4-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="555e4-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="555e4-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="555e4-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="555e4-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="555e4-117">Permission type</span></span> |   <span data-ttu-id="555e4-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="555e4-118">Permission</span></span>  |   <span data-ttu-id="555e4-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="555e4-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="555e4-120">Application</span><span class="sxs-lookup"><span data-stu-id="555e4-120">Application</span></span> |   <span data-ttu-id="555e4-121">Ip.Read.All</span><span class="sxs-lookup"><span data-stu-id="555e4-121">Ip.Read.All</span></span> |   <span data-ttu-id="555e4-122">« Lire les profils d’adresse IP »</span><span class="sxs-lookup"><span data-stu-id="555e4-122">'Read IP address profiles'</span></span>
<span data-ttu-id="555e4-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="555e4-123">Delegated (work or school account)</span></span> | <span data-ttu-id="555e4-124">Ip.Read.All</span><span class="sxs-lookup"><span data-stu-id="555e4-124">Ip.Read.All</span></span> |  <span data-ttu-id="555e4-125">« Lire les profils d’adresse IP »</span><span class="sxs-lookup"><span data-stu-id="555e4-125">'Read IP address profiles'</span></span>

>[!NOTE]
> <span data-ttu-id="555e4-126">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="555e4-126">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="555e4-127">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="555e4-127">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="555e4-128">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="555e4-128">HTTP request</span></span>

```http
GET /api/ips/{ip}/stats
```

## <a name="request-headers"></a><span data-ttu-id="555e4-129">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="555e4-129">Request headers</span></span>

<span data-ttu-id="555e4-130">Nom</span><span class="sxs-lookup"><span data-stu-id="555e4-130">Name</span></span> | <span data-ttu-id="555e4-131">Type</span><span class="sxs-lookup"><span data-stu-id="555e4-131">Type</span></span> | <span data-ttu-id="555e4-132">Description</span><span class="sxs-lookup"><span data-stu-id="555e4-132">Description</span></span>
:---|:---|:---
<span data-ttu-id="555e4-133">Autorisation</span><span class="sxs-lookup"><span data-stu-id="555e4-133">Authorization</span></span> | <span data-ttu-id="555e4-134">String</span><span class="sxs-lookup"><span data-stu-id="555e4-134">String</span></span> | <span data-ttu-id="555e4-135">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="555e4-135">Bearer {token}.</span></span> <span data-ttu-id="555e4-136">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="555e4-136">**Required**.</span></span>

## <a name="request-uri-parameters"></a><span data-ttu-id="555e4-137">Paramètres d’URI de demande</span><span class="sxs-lookup"><span data-stu-id="555e4-137">Request URI parameters</span></span>

<span data-ttu-id="555e4-138">Nom</span><span class="sxs-lookup"><span data-stu-id="555e4-138">Name</span></span> | <span data-ttu-id="555e4-139">Type</span><span class="sxs-lookup"><span data-stu-id="555e4-139">Type</span></span> | <span data-ttu-id="555e4-140">Description</span><span class="sxs-lookup"><span data-stu-id="555e4-140">Description</span></span>
:---|:---|:---
<span data-ttu-id="555e4-141">lookBackHours</span><span class="sxs-lookup"><span data-stu-id="555e4-141">lookBackHours</span></span> | <span data-ttu-id="555e4-142">Int32</span><span class="sxs-lookup"><span data-stu-id="555e4-142">Int32</span></span> | <span data-ttu-id="555e4-143">Définit les heures pendant les recherches pour obtenir les statistiques.</span><span class="sxs-lookup"><span data-stu-id="555e4-143">Defines the hours we search back to get the statistics.</span></span> <span data-ttu-id="555e4-144">La valeur par défaut est 30 jours.</span><span class="sxs-lookup"><span data-stu-id="555e4-144">Defaults to 30 days.</span></span> <span data-ttu-id="555e4-145">**Facultatif**.</span><span class="sxs-lookup"><span data-stu-id="555e4-145">**Optional**.</span></span>

## <a name="request-body"></a><span data-ttu-id="555e4-146">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="555e4-146">Request body</span></span>
<span data-ttu-id="555e4-147">Vide</span><span class="sxs-lookup"><span data-stu-id="555e4-147">Empty</span></span>

## <a name="response"></a><span data-ttu-id="555e4-148">Réponse</span><span class="sxs-lookup"><span data-stu-id="555e4-148">Response</span></span>
<span data-ttu-id="555e4-149">En cas de réussite et si ip existe - 200 OK avec des données statistiques dans le corps.</span><span class="sxs-lookup"><span data-stu-id="555e4-149">If successful and ip exists - 200 OK with statistical data in the body.</span></span> <span data-ttu-id="555e4-150">L’adresse IP n’existe pas : 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="555e4-150">IP do not exist - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="555e4-151">Exemple</span><span class="sxs-lookup"><span data-stu-id="555e4-151">Example</span></span>

<span data-ttu-id="555e4-152">**Demande**</span><span class="sxs-lookup"><span data-stu-id="555e4-152">**Request**</span></span>

<span data-ttu-id="555e4-153">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="555e4-153">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/ips/10.209.67.177/stats?lookBackHours=48
```

<span data-ttu-id="555e4-154">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="555e4-154">**Response**</span></span>

<span data-ttu-id="555e4-155">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="555e4-155">Here is an example of the response.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#microsoft.windowsDefenderATP.api.InOrgIPStats",
    "ipAddress": "10.209.67.177",
    "orgPrevalence": "63515",
    "orgFirstSeen": "2017-07-30T13:36:06Z",
    "orgLastSeen": "2017-08-29T13:32:59Z"
}
```


| <span data-ttu-id="555e4-156">Nom</span><span class="sxs-lookup"><span data-stu-id="555e4-156">Name</span></span> | <span data-ttu-id="555e4-157">Description</span><span class="sxs-lookup"><span data-stu-id="555e4-157">Description</span></span> |
| :--- | :---------- |
| <span data-ttu-id="555e4-158">Prévalence de l’organisation</span><span class="sxs-lookup"><span data-stu-id="555e4-158">Org prevalence</span></span> | <span data-ttu-id="555e4-159">nombre distinct d’appareils qui ont ouvert une connexion réseau à cette adresse IP;</span><span class="sxs-lookup"><span data-stu-id="555e4-159">the distinct count of devices that opened network connection to this IP.</span></span> |
| <span data-ttu-id="555e4-160">Organisation vue pour la première fois</span><span class="sxs-lookup"><span data-stu-id="555e4-160">Org first seen</span></span> | <span data-ttu-id="555e4-161">première connexion pour cette adresse IP dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="555e4-161">the first connection for this IP in the organization.</span></span> |
| <span data-ttu-id="555e4-162">Organisation vue pour la dernière fois</span><span class="sxs-lookup"><span data-stu-id="555e4-162">Org last seen</span></span>  | <span data-ttu-id="555e4-163">dernière connexion pour cette adresse IP dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="555e4-163">the last connection for this IP in the organization.</span></span> |

> [!NOTE]
> <span data-ttu-id="555e4-164">Ces informations de statistique sont basées sur les données des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="555e4-164">This statistic information is based on data from the past 30 days.</span></span> 
