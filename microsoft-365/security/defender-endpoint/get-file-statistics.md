---
title: API Obtenir les statistiques sur les fichiers
description: Découvrez comment utiliser l’API Obtenir des statistiques de fichier pour récupérer les statistiques du fichier donné dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, fichier, statistiques
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
ms.openlocfilehash: ff43f6c46d89bc92cd1dc2a4fb0f329757b8f69e
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166701"
---
# <a name="get-file-statistics-api"></a><span data-ttu-id="1cce1-104">API Obtenir les statistiques sur les fichiers</span><span class="sxs-lookup"><span data-stu-id="1cce1-104">Get file statistics API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="1cce1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1cce1-105">**Applies to:**</span></span>
- [<span data-ttu-id="1cce1-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1cce1-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="1cce1-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1cce1-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="1cce1-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="1cce1-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="1cce1-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="1cce1-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="1cce1-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="1cce1-110">API description</span></span>
<span data-ttu-id="1cce1-111">Extrait les statistiques du fichier donné.</span><span class="sxs-lookup"><span data-stu-id="1cce1-111">Retrieves the statistics for the given file.</span></span>


## <a name="limitations"></a><span data-ttu-id="1cce1-112">Limites</span><span class="sxs-lookup"><span data-stu-id="1cce1-112">Limitations</span></span>
1. <span data-ttu-id="1cce1-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="1cce1-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="1cce1-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="1cce1-114">Permissions</span></span>
<span data-ttu-id="1cce1-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="1cce1-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="1cce1-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="1cce1-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="1cce1-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="1cce1-117">Permission type</span></span> |   <span data-ttu-id="1cce1-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="1cce1-118">Permission</span></span>  |   <span data-ttu-id="1cce1-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="1cce1-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="1cce1-120">Application</span><span class="sxs-lookup"><span data-stu-id="1cce1-120">Application</span></span> |   <span data-ttu-id="1cce1-121">File.Read.All</span><span class="sxs-lookup"><span data-stu-id="1cce1-121">File.Read.All</span></span> | <span data-ttu-id="1cce1-122">« Lire les profils de fichiers »</span><span class="sxs-lookup"><span data-stu-id="1cce1-122">'Read file profiles'</span></span>
<span data-ttu-id="1cce1-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="1cce1-123">Delegated (work or school account)</span></span> | <span data-ttu-id="1cce1-124">File.Read.All</span><span class="sxs-lookup"><span data-stu-id="1cce1-124">File.Read.All</span></span> | <span data-ttu-id="1cce1-125">« Lire les profils de fichiers »</span><span class="sxs-lookup"><span data-stu-id="1cce1-125">'Read file profiles'</span></span>

>[!Note]
> <span data-ttu-id="1cce1-126">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="1cce1-126">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="1cce1-127">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="1cce1-127">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="1cce1-128">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="1cce1-128">HTTP request</span></span>
```
GET /api/files/{id}/stats
```

## <a name="request-headers"></a><span data-ttu-id="1cce1-129">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="1cce1-129">Request headers</span></span>

<span data-ttu-id="1cce1-130">Nom</span><span class="sxs-lookup"><span data-stu-id="1cce1-130">Name</span></span> | <span data-ttu-id="1cce1-131">Type</span><span class="sxs-lookup"><span data-stu-id="1cce1-131">Type</span></span> | <span data-ttu-id="1cce1-132">Description</span><span class="sxs-lookup"><span data-stu-id="1cce1-132">Description</span></span>
:---|:---|:---
<span data-ttu-id="1cce1-133">Autorisation</span><span class="sxs-lookup"><span data-stu-id="1cce1-133">Authorization</span></span> | <span data-ttu-id="1cce1-134">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1cce1-134">String</span></span> | <span data-ttu-id="1cce1-135">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="1cce1-135">Bearer {token}.</span></span> <span data-ttu-id="1cce1-136">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="1cce1-136">**Required**.</span></span>

## <a name="request-uri-parameters"></a><span data-ttu-id="1cce1-137">Paramètres d’URI de demande</span><span class="sxs-lookup"><span data-stu-id="1cce1-137">Request URI parameters</span></span>

<span data-ttu-id="1cce1-138">Nom</span><span class="sxs-lookup"><span data-stu-id="1cce1-138">Name</span></span> | <span data-ttu-id="1cce1-139">Type</span><span class="sxs-lookup"><span data-stu-id="1cce1-139">Type</span></span> | <span data-ttu-id="1cce1-140">Description</span><span class="sxs-lookup"><span data-stu-id="1cce1-140">Description</span></span>
:---|:---|:---
<span data-ttu-id="1cce1-141">lookBackHours</span><span class="sxs-lookup"><span data-stu-id="1cce1-141">lookBackHours</span></span> | <span data-ttu-id="1cce1-142">Int32</span><span class="sxs-lookup"><span data-stu-id="1cce1-142">Int32</span></span> | <span data-ttu-id="1cce1-143">Définit les heures que nous allons rechercher pour obtenir les statistiques.</span><span class="sxs-lookup"><span data-stu-id="1cce1-143">Defines the hours we search back to get the statistics.</span></span> <span data-ttu-id="1cce1-144">La valeur par défaut est 30 jours.</span><span class="sxs-lookup"><span data-stu-id="1cce1-144">Defaults to 30 days.</span></span> <span data-ttu-id="1cce1-145">**Facultatif**.</span><span class="sxs-lookup"><span data-stu-id="1cce1-145">**Optional**.</span></span>

## <a name="request-body"></a><span data-ttu-id="1cce1-146">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="1cce1-146">Request body</span></span>
<span data-ttu-id="1cce1-147">Vide</span><span class="sxs-lookup"><span data-stu-id="1cce1-147">Empty</span></span>

## <a name="response"></a><span data-ttu-id="1cce1-148">Réponse</span><span class="sxs-lookup"><span data-stu-id="1cce1-148">Response</span></span>
<span data-ttu-id="1cce1-149">En cas de réussite et si le fichier existe : 200 - OK avec des données statistiques dans le corps.</span><span class="sxs-lookup"><span data-stu-id="1cce1-149">If successful and file exists - 200 OK with statistical data in the body.</span></span> <span data-ttu-id="1cce1-150">Si le fichier n’existe pas - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="1cce1-150">If file do not exist - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="1cce1-151">Exemple</span><span class="sxs-lookup"><span data-stu-id="1cce1-151">Example</span></span>

<span data-ttu-id="1cce1-152">**Demande**</span><span class="sxs-lookup"><span data-stu-id="1cce1-152">**Request**</span></span>

<span data-ttu-id="1cce1-153">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="1cce1-153">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/files/0991a395da64e1c5fbe8732ed11e6be064081d9f/stats?lookBackHours=48
```

<span data-ttu-id="1cce1-154">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="1cce1-154">**Response**</span></span>

<span data-ttu-id="1cce1-155">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="1cce1-155">Here is an example of the response.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#microsoft.windowsDefenderATP.api.InOrgFileStats",
    "sha1": "0991a395da64e1c5fbe8732ed11e6be064081d9f",
    "orgPrevalence": "14850",
    "orgFirstSeen": "2019-12-07T13:44:16Z",
    "orgLastSeen": "2020-01-06T13:39:36Z",
    "globalPrevalence": "705012",
    "globalFirstObserved": "2015-03-19T12:20:07.3432441Z",
    "globalLastObserved": "2020-01-06T13:39:36Z",
    "topFileNames": [
        "MREC.exe"
    ]
}

```
