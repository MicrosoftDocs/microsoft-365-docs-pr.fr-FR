---
title: API Obtenir un incident
description: Découvrez comment utiliser l’API Obtenir des incidents pour obtenir un incident unique dans Microsoft 365 Defender.
keywords: api, api de graphique, api pris en charge, obtenir, fichier, hachage
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
ms.openlocfilehash: 2e051803a4cd228e3b455ec08b30e5c2197ca9a3
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53289606"
---
# <a name="get-incident-information-api"></a><span data-ttu-id="9e6ab-104">API Obtenir des informations sur l’incident</span><span class="sxs-lookup"><span data-stu-id="9e6ab-104">Get incident information API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="9e6ab-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9e6ab-105">**Applies to:**</span></span>
- [<span data-ttu-id="9e6ab-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9e6ab-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="9e6ab-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="9e6ab-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="9e6ab-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="9e6ab-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="9e6ab-109">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="9e6ab-109">API description</span></span>

<span data-ttu-id="9e6ab-110">Récupère un incident spécifique par son ID</span><span class="sxs-lookup"><span data-stu-id="9e6ab-110">Retrieves a specific incident by its ID</span></span>

## <a name="limitations"></a><span data-ttu-id="9e6ab-111">Limites</span><span class="sxs-lookup"><span data-stu-id="9e6ab-111">Limitations</span></span>

1. <span data-ttu-id="9e6ab-112">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="9e6ab-112">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="9e6ab-113">Autorisations</span><span class="sxs-lookup"><span data-stu-id="9e6ab-113">Permissions</span></span>

<span data-ttu-id="9e6ab-114">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="9e6ab-114">One of the following permissions is required to call this API.</span></span> 

<span data-ttu-id="9e6ab-115">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="9e6ab-115">Permission type</span></span> | <span data-ttu-id="9e6ab-116">Autorisation</span><span class="sxs-lookup"><span data-stu-id="9e6ab-116">Permission</span></span> | <span data-ttu-id="9e6ab-117">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="9e6ab-117">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="9e6ab-118">Application</span><span class="sxs-lookup"><span data-stu-id="9e6ab-118">Application</span></span> | <span data-ttu-id="9e6ab-119">Incident.Read.All</span><span class="sxs-lookup"><span data-stu-id="9e6ab-119">Incident.Read.All</span></span> | <span data-ttu-id="9e6ab-120">« Lire tous les incidents »</span><span class="sxs-lookup"><span data-stu-id="9e6ab-120">'Read all Incidents'</span></span>
<span data-ttu-id="9e6ab-121">Application</span><span class="sxs-lookup"><span data-stu-id="9e6ab-121">Application</span></span> | <span data-ttu-id="9e6ab-122">Incident.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9e6ab-122">Incident.ReadWrite.All</span></span> | <span data-ttu-id="9e6ab-123">« Lire et écrire tous les incidents »</span><span class="sxs-lookup"><span data-stu-id="9e6ab-123">'Read and write all Incidents'</span></span>
<span data-ttu-id="9e6ab-124">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="9e6ab-124">Delegated (work or school account)</span></span> | <span data-ttu-id="9e6ab-125">Incident.Read</span><span class="sxs-lookup"><span data-stu-id="9e6ab-125">Incident.Read</span></span> | <span data-ttu-id="9e6ab-126">' Read Incidents'</span><span class="sxs-lookup"><span data-stu-id="9e6ab-126">'Read Incidents'</span></span>
<span data-ttu-id="9e6ab-127">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="9e6ab-127">Delegated (work or school account)</span></span> | <span data-ttu-id="9e6ab-128">Incident.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9e6ab-128">Incident.ReadWrite</span></span> | <span data-ttu-id="9e6ab-129">« Lire et écrire des incidents »</span><span class="sxs-lookup"><span data-stu-id="9e6ab-129">'Read and write Incidents'</span></span>

> [!NOTE]
>
> <span data-ttu-id="9e6ab-130">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="9e6ab-130">When obtaining a token using user credentials:</span></span>
>
> - <span data-ttu-id="9e6ab-131">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données »</span><span class="sxs-lookup"><span data-stu-id="9e6ab-131">The user needs to have at least the following role permission: 'View Data'</span></span>
> - <span data-ttu-id="9e6ab-132">La réponse inclut uniquement les incidents que l’utilisateur est exposé à</span><span class="sxs-lookup"><span data-stu-id="9e6ab-132">The response will only include incidents that the user is exposed to</span></span>

## <a name="http-request"></a><span data-ttu-id="9e6ab-133">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="9e6ab-133">HTTP request</span></span>

```console
GET .../api/incidents/{id} 
```

## <a name="request-headers"></a><span data-ttu-id="9e6ab-134">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="9e6ab-134">Request headers</span></span>

<span data-ttu-id="9e6ab-135">Nom</span><span class="sxs-lookup"><span data-stu-id="9e6ab-135">Name</span></span> | <span data-ttu-id="9e6ab-136">Type</span><span class="sxs-lookup"><span data-stu-id="9e6ab-136">Type</span></span> | <span data-ttu-id="9e6ab-137">Description</span><span class="sxs-lookup"><span data-stu-id="9e6ab-137">Description</span></span>
:---|:---|:---
<span data-ttu-id="9e6ab-138">Autorisation</span><span class="sxs-lookup"><span data-stu-id="9e6ab-138">Authorization</span></span> | <span data-ttu-id="9e6ab-139">String</span><span class="sxs-lookup"><span data-stu-id="9e6ab-139">String</span></span> | <span data-ttu-id="9e6ab-140">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="9e6ab-140">Bearer {token}.</span></span> <span data-ttu-id="9e6ab-141">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="9e6ab-141">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="9e6ab-142">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="9e6ab-142">Request body</span></span>

<span data-ttu-id="9e6ab-143">Vide</span><span class="sxs-lookup"><span data-stu-id="9e6ab-143">Empty</span></span>

## <a name="response"></a><span data-ttu-id="9e6ab-144">Réponse</span><span class="sxs-lookup"><span data-stu-id="9e6ab-144">Response</span></span>

<span data-ttu-id="9e6ab-145">Si elle réussit, cette méthode renvoie 200 OK et l’entité d’incident dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="9e6ab-145">If successful, this method returns 200 OK, and the incident entity in the response body.</span></span> <span data-ttu-id="9e6ab-146">Si l’incident avec l’ID spécifié n’a pas été trouvé - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="9e6ab-146">If incident with the specified id was not found - 404 Not Found.</span></span>

## <a name="example"></a><span data-ttu-id="9e6ab-147">Exemple</span><span class="sxs-lookup"><span data-stu-id="9e6ab-147">Example</span></span>

<span data-ttu-id="9e6ab-148">**Demande**</span><span class="sxs-lookup"><span data-stu-id="9e6ab-148">**Request**</span></span>

<span data-ttu-id="9e6ab-149">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="9e6ab-149">Here is an example of the request.</span></span>

```http
GET https://api.security.microsoft.com/api/incidents/{id}
```
