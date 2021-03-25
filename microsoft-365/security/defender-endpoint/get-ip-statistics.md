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
ms.technology: mde
ms.openlocfilehash: c47a5e58b1888447a4428fad78e71b85cfe79b69
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166731"
---
# <a name="get-ip-statistics-api"></a><span data-ttu-id="bdd32-104">API Obtenir des statistiques IP</span><span class="sxs-lookup"><span data-stu-id="bdd32-104">Get IP statistics API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="bdd32-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="bdd32-105">**Applies to:**</span></span>
- [<span data-ttu-id="bdd32-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="bdd32-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="bdd32-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bdd32-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="bdd32-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="bdd32-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="bdd32-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="bdd32-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="bdd32-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="bdd32-110">API description</span></span>
<span data-ttu-id="bdd32-111">Récupère les statistiques de l’adresse IP donnée.</span><span class="sxs-lookup"><span data-stu-id="bdd32-111">Retrieves the statistics for the given IP.</span></span>

## <a name="limitations"></a><span data-ttu-id="bdd32-112">Limites</span><span class="sxs-lookup"><span data-stu-id="bdd32-112">Limitations</span></span>
1. <span data-ttu-id="bdd32-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="bdd32-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>

## <a name="permissions"></a><span data-ttu-id="bdd32-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="bdd32-114">Permissions</span></span>
<span data-ttu-id="bdd32-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="bdd32-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="bdd32-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="bdd32-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="bdd32-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="bdd32-117">Permission type</span></span> |   <span data-ttu-id="bdd32-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="bdd32-118">Permission</span></span>  |   <span data-ttu-id="bdd32-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="bdd32-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="bdd32-120">Application</span><span class="sxs-lookup"><span data-stu-id="bdd32-120">Application</span></span> |   <span data-ttu-id="bdd32-121">Ip.Read.All</span><span class="sxs-lookup"><span data-stu-id="bdd32-121">Ip.Read.All</span></span> |   <span data-ttu-id="bdd32-122">« Lire les profils d’adresse IP »</span><span class="sxs-lookup"><span data-stu-id="bdd32-122">'Read IP address profiles'</span></span>
<span data-ttu-id="bdd32-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="bdd32-123">Delegated (work or school account)</span></span> | <span data-ttu-id="bdd32-124">Ip.Read.All</span><span class="sxs-lookup"><span data-stu-id="bdd32-124">Ip.Read.All</span></span> |  <span data-ttu-id="bdd32-125">« Lire les profils d’adresse IP »</span><span class="sxs-lookup"><span data-stu-id="bdd32-125">'Read IP address profiles'</span></span>

>[!NOTE]
> <span data-ttu-id="bdd32-126">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="bdd32-126">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="bdd32-127">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="bdd32-127">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="bdd32-128">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="bdd32-128">HTTP request</span></span>

```http
GET /api/ips/{ip}/stats
```

## <a name="request-headers"></a><span data-ttu-id="bdd32-129">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="bdd32-129">Request headers</span></span>

<span data-ttu-id="bdd32-130">Nom</span><span class="sxs-lookup"><span data-stu-id="bdd32-130">Name</span></span> | <span data-ttu-id="bdd32-131">Type</span><span class="sxs-lookup"><span data-stu-id="bdd32-131">Type</span></span> | <span data-ttu-id="bdd32-132">Description</span><span class="sxs-lookup"><span data-stu-id="bdd32-132">Description</span></span>
:---|:---|:---
<span data-ttu-id="bdd32-133">Autorisation</span><span class="sxs-lookup"><span data-stu-id="bdd32-133">Authorization</span></span> | <span data-ttu-id="bdd32-134">Chaîne</span><span class="sxs-lookup"><span data-stu-id="bdd32-134">String</span></span> | <span data-ttu-id="bdd32-135">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="bdd32-135">Bearer {token}.</span></span> <span data-ttu-id="bdd32-136">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="bdd32-136">**Required**.</span></span>

## <a name="request-uri-parameters"></a><span data-ttu-id="bdd32-137">Paramètres d’URI de demande</span><span class="sxs-lookup"><span data-stu-id="bdd32-137">Request URI parameters</span></span>

<span data-ttu-id="bdd32-138">Nom</span><span class="sxs-lookup"><span data-stu-id="bdd32-138">Name</span></span> | <span data-ttu-id="bdd32-139">Type</span><span class="sxs-lookup"><span data-stu-id="bdd32-139">Type</span></span> | <span data-ttu-id="bdd32-140">Description</span><span class="sxs-lookup"><span data-stu-id="bdd32-140">Description</span></span>
:---|:---|:---
<span data-ttu-id="bdd32-141">lookBackHours</span><span class="sxs-lookup"><span data-stu-id="bdd32-141">lookBackHours</span></span> | <span data-ttu-id="bdd32-142">Int32</span><span class="sxs-lookup"><span data-stu-id="bdd32-142">Int32</span></span> | <span data-ttu-id="bdd32-143">Définit les heures que nous allons rechercher pour obtenir les statistiques.</span><span class="sxs-lookup"><span data-stu-id="bdd32-143">Defines the hours we search back to get the statistics.</span></span> <span data-ttu-id="bdd32-144">La valeur par défaut est 30 jours.</span><span class="sxs-lookup"><span data-stu-id="bdd32-144">Defaults to 30 days.</span></span> <span data-ttu-id="bdd32-145">**Facultatif**.</span><span class="sxs-lookup"><span data-stu-id="bdd32-145">**Optional**.</span></span>

## <a name="request-body"></a><span data-ttu-id="bdd32-146">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="bdd32-146">Request body</span></span>
<span data-ttu-id="bdd32-147">Vide</span><span class="sxs-lookup"><span data-stu-id="bdd32-147">Empty</span></span>

## <a name="response"></a><span data-ttu-id="bdd32-148">Réponse</span><span class="sxs-lookup"><span data-stu-id="bdd32-148">Response</span></span>
<span data-ttu-id="bdd32-149">En cas de réussite et si ip existe : 200 - OK avec des données statistiques dans le corps.</span><span class="sxs-lookup"><span data-stu-id="bdd32-149">If successful and ip exists - 200 OK with statistical data in the body.</span></span> <span data-ttu-id="bdd32-150">L’adresse IP n’existe pas : 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="bdd32-150">IP do not exist - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="bdd32-151">Exemple</span><span class="sxs-lookup"><span data-stu-id="bdd32-151">Example</span></span>

<span data-ttu-id="bdd32-152">**Demande**</span><span class="sxs-lookup"><span data-stu-id="bdd32-152">**Request**</span></span>

<span data-ttu-id="bdd32-153">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="bdd32-153">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/ips/10.209.67.177/stats?lookBackHours=48
```

<span data-ttu-id="bdd32-154">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="bdd32-154">**Response**</span></span>

<span data-ttu-id="bdd32-155">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="bdd32-155">Here is an example of the response.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#microsoft.windowsDefenderATP.api.InOrgIPStats",
    "ipAddress": "10.209.67.177",
    "orgPrevalence": "63515",
    "orgFirstSeen": "2017-07-30T13:36:06Z",
    "orgLastSeen": "2017-08-29T13:32:59Z"
}
```


| <span data-ttu-id="bdd32-156">Nom</span><span class="sxs-lookup"><span data-stu-id="bdd32-156">Name</span></span> | <span data-ttu-id="bdd32-157">Description</span><span class="sxs-lookup"><span data-stu-id="bdd32-157">Description</span></span> |
| :--- | :---------- |
| <span data-ttu-id="bdd32-158">Prévalence de l’organisation</span><span class="sxs-lookup"><span data-stu-id="bdd32-158">Org prevalence</span></span> | <span data-ttu-id="bdd32-159">nombre distinct d’appareils qui ont ouvert une connexion réseau à cette adresse IP;</span><span class="sxs-lookup"><span data-stu-id="bdd32-159">the distinct count of devices that opened network connection to this IP.</span></span> |
| <span data-ttu-id="bdd32-160">Organisation vue pour la première fois</span><span class="sxs-lookup"><span data-stu-id="bdd32-160">Org first seen</span></span> | <span data-ttu-id="bdd32-161">première connexion pour cette adresse IP dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="bdd32-161">the first connection for this IP in the organization.</span></span> |
| <span data-ttu-id="bdd32-162">Organisation vue pour la dernière fois</span><span class="sxs-lookup"><span data-stu-id="bdd32-162">Org last seen</span></span>  | <span data-ttu-id="bdd32-163">dernière connexion pour cette adresse IP dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="bdd32-163">the last connection for this IP in the organization.</span></span> |

> [!NOTE]
> <span data-ttu-id="bdd32-164">Ces informations de statistique sont basées sur les données des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="bdd32-164">This statistic information is based on data from the past 30 days.</span></span> 
