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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 6063d29562be40aed3060e241b52b1a2936aa36d
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52770204"
---
# <a name="get-file-statistics-api"></a><span data-ttu-id="bab91-104">API Obtenir les statistiques sur les fichiers</span><span class="sxs-lookup"><span data-stu-id="bab91-104">Get file statistics API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="bab91-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="bab91-105">**Applies to:**</span></span>
- [<span data-ttu-id="bab91-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="bab91-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="bab91-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bab91-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="bab91-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="bab91-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="bab91-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="bab91-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="bab91-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="bab91-110">API description</span></span>
<span data-ttu-id="bab91-111">Extrait les statistiques du fichier donné.</span><span class="sxs-lookup"><span data-stu-id="bab91-111">Retrieves the statistics for the given file.</span></span>


## <a name="limitations"></a><span data-ttu-id="bab91-112">Limitations</span><span class="sxs-lookup"><span data-stu-id="bab91-112">Limitations</span></span>
1. <span data-ttu-id="bab91-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="bab91-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="bab91-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="bab91-114">Permissions</span></span>
<span data-ttu-id="bab91-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="bab91-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="bab91-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="bab91-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="bab91-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="bab91-117">Permission type</span></span> |   <span data-ttu-id="bab91-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="bab91-118">Permission</span></span>  |   <span data-ttu-id="bab91-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="bab91-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="bab91-120">Application</span><span class="sxs-lookup"><span data-stu-id="bab91-120">Application</span></span> |   <span data-ttu-id="bab91-121">File.Read.All</span><span class="sxs-lookup"><span data-stu-id="bab91-121">File.Read.All</span></span> | <span data-ttu-id="bab91-122">« Lire les profils de fichiers »</span><span class="sxs-lookup"><span data-stu-id="bab91-122">'Read file profiles'</span></span>
<span data-ttu-id="bab91-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="bab91-123">Delegated (work or school account)</span></span> | <span data-ttu-id="bab91-124">File.Read.All</span><span class="sxs-lookup"><span data-stu-id="bab91-124">File.Read.All</span></span> | <span data-ttu-id="bab91-125">« Lire les profils de fichiers »</span><span class="sxs-lookup"><span data-stu-id="bab91-125">'Read file profiles'</span></span>

>[!Note]
> <span data-ttu-id="bab91-126">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="bab91-126">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="bab91-127">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="bab91-127">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="bab91-128">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="bab91-128">HTTP request</span></span>
```
GET /api/files/{id}/stats
```

## <a name="request-headers"></a><span data-ttu-id="bab91-129">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="bab91-129">Request headers</span></span>

<span data-ttu-id="bab91-130">Nom</span><span class="sxs-lookup"><span data-stu-id="bab91-130">Name</span></span> | <span data-ttu-id="bab91-131">Type</span><span class="sxs-lookup"><span data-stu-id="bab91-131">Type</span></span> | <span data-ttu-id="bab91-132">Description</span><span class="sxs-lookup"><span data-stu-id="bab91-132">Description</span></span>
:---|:---|:---
<span data-ttu-id="bab91-133">Autorisation</span><span class="sxs-lookup"><span data-stu-id="bab91-133">Authorization</span></span> | <span data-ttu-id="bab91-134">String</span><span class="sxs-lookup"><span data-stu-id="bab91-134">String</span></span> | <span data-ttu-id="bab91-135">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="bab91-135">Bearer {token}.</span></span> <span data-ttu-id="bab91-136">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="bab91-136">**Required**.</span></span>

## <a name="request-uri-parameters"></a><span data-ttu-id="bab91-137">Paramètres d’URI de demande</span><span class="sxs-lookup"><span data-stu-id="bab91-137">Request URI parameters</span></span>

<span data-ttu-id="bab91-138">Nom</span><span class="sxs-lookup"><span data-stu-id="bab91-138">Name</span></span> | <span data-ttu-id="bab91-139">Type</span><span class="sxs-lookup"><span data-stu-id="bab91-139">Type</span></span> | <span data-ttu-id="bab91-140">Description</span><span class="sxs-lookup"><span data-stu-id="bab91-140">Description</span></span>
:---|:---|:---
<span data-ttu-id="bab91-141">lookBackHours</span><span class="sxs-lookup"><span data-stu-id="bab91-141">lookBackHours</span></span> | <span data-ttu-id="bab91-142">Int32</span><span class="sxs-lookup"><span data-stu-id="bab91-142">Int32</span></span> | <span data-ttu-id="bab91-143">Définit les heures pendant les recherches pour obtenir les statistiques.</span><span class="sxs-lookup"><span data-stu-id="bab91-143">Defines the hours we search back to get the statistics.</span></span> <span data-ttu-id="bab91-144">La valeur par défaut est 30 jours.</span><span class="sxs-lookup"><span data-stu-id="bab91-144">Defaults to 30 days.</span></span> <span data-ttu-id="bab91-145">**Facultatif**.</span><span class="sxs-lookup"><span data-stu-id="bab91-145">**Optional**.</span></span>

## <a name="request-body"></a><span data-ttu-id="bab91-146">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="bab91-146">Request body</span></span>
<span data-ttu-id="bab91-147">Vide</span><span class="sxs-lookup"><span data-stu-id="bab91-147">Empty</span></span>

## <a name="response"></a><span data-ttu-id="bab91-148">Réponse</span><span class="sxs-lookup"><span data-stu-id="bab91-148">Response</span></span>
<span data-ttu-id="bab91-149">En cas de réussite et si le fichier existe - 200 OK avec des données statistiques dans le corps.</span><span class="sxs-lookup"><span data-stu-id="bab91-149">If successful and file exists - 200 OK with statistical data in the body.</span></span> <span data-ttu-id="bab91-150">Si le fichier n’existe pas - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="bab91-150">If file do not exist - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="bab91-151">Exemple</span><span class="sxs-lookup"><span data-stu-id="bab91-151">Example</span></span>

<span data-ttu-id="bab91-152">**Demande**</span><span class="sxs-lookup"><span data-stu-id="bab91-152">**Request**</span></span>

<span data-ttu-id="bab91-153">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="bab91-153">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/files/0991a395da64e1c5fbe8732ed11e6be064081d9f/stats?lookBackHours=48
```

<span data-ttu-id="bab91-154">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="bab91-154">**Response**</span></span>

<span data-ttu-id="bab91-155">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="bab91-155">Here is an example of the response.</span></span>


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
