---
title: Rechercher des appareils par API IP interne
description: Rechercher les appareils visibles avec l’adresse IP interne demandée dans l’plage de temps de 15 minutes avant et après un timestamp donné
keywords: api, api de graphique, api pris en charge, obtenir, appareil, IP, rechercher, trouver un appareil, par ip, ip
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
ms.openlocfilehash: 46afa945ce86c35e3af1c542eb1a9770041b3430
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52769436"
---
# <a name="find-devices-by-internal-ip-api"></a><span data-ttu-id="dd3fe-104">Rechercher des appareils par API IP interne</span><span class="sxs-lookup"><span data-stu-id="dd3fe-104">Find devices by internal IP API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="dd3fe-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="dd3fe-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

> <span data-ttu-id="dd3fe-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="dd3fe-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="dd3fe-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="dd3fe-108">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="dd3fe-108">API description</span></span>
<span data-ttu-id="dd3fe-109">Recherchez [les](machine.md) ordinateurs visibles avec l’adresse IP interne demandée dans l’plage de temps de 15 minutes avant et après un timestamp donné.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-109">Find [Machines](machine.md) seen with the requested internal IP in the time range of 15 minutes prior and after a given timestamp.</span></span>


## <a name="limitations"></a><span data-ttu-id="dd3fe-110">Limites</span><span class="sxs-lookup"><span data-stu-id="dd3fe-110">Limitations</span></span>
1. <span data-ttu-id="dd3fe-111">L’timestamp donné doit se trouver dans les 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-111">The given timestamp must be in the past 30 days.</span></span>
2. <span data-ttu-id="dd3fe-112">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-112">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="dd3fe-113">Autorisations</span><span class="sxs-lookup"><span data-stu-id="dd3fe-113">Permissions</span></span>
<span data-ttu-id="dd3fe-114">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-114">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="dd3fe-115">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="dd3fe-115">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="dd3fe-116">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="dd3fe-116">Permission type</span></span> |   <span data-ttu-id="dd3fe-117">Autorisation</span><span class="sxs-lookup"><span data-stu-id="dd3fe-117">Permission</span></span>  |   <span data-ttu-id="dd3fe-118">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="dd3fe-118">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="dd3fe-119">Application</span><span class="sxs-lookup"><span data-stu-id="dd3fe-119">Application</span></span> |   <span data-ttu-id="dd3fe-120">Machine.Read.All</span><span class="sxs-lookup"><span data-stu-id="dd3fe-120">Machine.Read.All</span></span> |  <span data-ttu-id="dd3fe-121">« Lire tous les profils d’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="dd3fe-121">'Read all machine profiles'</span></span>
<span data-ttu-id="dd3fe-122">Application</span><span class="sxs-lookup"><span data-stu-id="dd3fe-122">Application</span></span> |   <span data-ttu-id="dd3fe-123">Machine.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dd3fe-123">Machine.ReadWrite.All</span></span> | <span data-ttu-id="dd3fe-124">« Lire et écrire toutes les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="dd3fe-124">'Read and write all machine information'</span></span>
<span data-ttu-id="dd3fe-125">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="dd3fe-125">Delegated (work or school account)</span></span> | <span data-ttu-id="dd3fe-126">Machine.Read</span><span class="sxs-lookup"><span data-stu-id="dd3fe-126">Machine.Read</span></span> | <span data-ttu-id="dd3fe-127">« Lire les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="dd3fe-127">'Read machine information'</span></span>
<span data-ttu-id="dd3fe-128">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="dd3fe-128">Delegated (work or school account)</span></span> | <span data-ttu-id="dd3fe-129">Machine.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="dd3fe-129">Machine.ReadWrite</span></span> | <span data-ttu-id="dd3fe-130">« Lire et écrire des informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="dd3fe-130">'Read and write machine information'</span></span>

>[!Note]
> <span data-ttu-id="dd3fe-131">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="dd3fe-131">When obtaining a token using user credentials:</span></span>
> - <span data-ttu-id="dd3fe-132">La réponse inclut uniquement les appareils accessibles par l’utilisateur en fonction des paramètres de groupe d’appareils (pour plus d’informations, voir Créer et gérer des groupes d’appareils). [](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="dd3fe-132">Response will include only devices that the user have access to based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>
> - <span data-ttu-id="dd3fe-133">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="dd3fe-133">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
> - <span data-ttu-id="dd3fe-134">La réponse inclut uniquement les appareils accessibles par l’utilisateur en fonction des paramètres de groupe d’appareils (pour plus d’informations, voir Créer et gérer des groupes d’appareils). [](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="dd3fe-134">Response will include only devices that the user have access to based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="dd3fe-135">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="dd3fe-135">HTTP request</span></span>
```
GET /api/machines/findbyip(ip='{IP}',timestamp={TimeStamp})
```

## <a name="request-headers"></a><span data-ttu-id="dd3fe-136">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="dd3fe-136">Request headers</span></span>

<span data-ttu-id="dd3fe-137">Nom</span><span class="sxs-lookup"><span data-stu-id="dd3fe-137">Name</span></span> | <span data-ttu-id="dd3fe-138">Type</span><span class="sxs-lookup"><span data-stu-id="dd3fe-138">Type</span></span> | <span data-ttu-id="dd3fe-139">Description</span><span class="sxs-lookup"><span data-stu-id="dd3fe-139">Description</span></span>
:---|:---|:---
<span data-ttu-id="dd3fe-140">Autorisation</span><span class="sxs-lookup"><span data-stu-id="dd3fe-140">Authorization</span></span> | <span data-ttu-id="dd3fe-141">String</span><span class="sxs-lookup"><span data-stu-id="dd3fe-141">String</span></span> | <span data-ttu-id="dd3fe-142">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-142">Bearer {token}.</span></span> <span data-ttu-id="dd3fe-143">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-143">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="dd3fe-144">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="dd3fe-144">Request body</span></span>
<span data-ttu-id="dd3fe-145">Vide</span><span class="sxs-lookup"><span data-stu-id="dd3fe-145">Empty</span></span>

## <a name="response"></a><span data-ttu-id="dd3fe-146">Réponse</span><span class="sxs-lookup"><span data-stu-id="dd3fe-146">Response</span></span>
<span data-ttu-id="dd3fe-147">En cas de réussite : 200 - OK avec la liste des ordinateurs dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-147">If successful - 200 OK with list of the machines in the response body.</span></span>
<span data-ttu-id="dd3fe-148">Si l’timestamp n’est pas dans les 30 derniers jours - 400 demande mauvaise.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-148">If the timestamp is not in the past 30 days - 400 Bad Request.</span></span>

## <a name="example"></a><span data-ttu-id="dd3fe-149">Exemple</span><span class="sxs-lookup"><span data-stu-id="dd3fe-149">Example</span></span>

<span data-ttu-id="dd3fe-150">**Demande**</span><span class="sxs-lookup"><span data-stu-id="dd3fe-150">**Request**</span></span>

<span data-ttu-id="dd3fe-151">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-151">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/machines/findbyip(ip='10.248.240.38',timestamp=2019-09-22T08:44:05Z)
```
