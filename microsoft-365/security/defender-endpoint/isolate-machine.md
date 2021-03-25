---
title: API Isoler l’ordinateur
description: Découvrez comment utiliser l’API Isoler l’ordinateur pour isoler un appareil de l’accès au réseau externe dans Microsoft Defender pour point de terminaison.
keywords: api, api de graphique, api pris en charge, isoler l’appareil
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
ms.openlocfilehash: b9c8d4da528ba065dc1b4a68ddaa816a1ad78c4a
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51187831"
---
# <a name="isolate-machine-api"></a><span data-ttu-id="f6c99-104">API Isoler l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="f6c99-104">Isolate machine API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="f6c99-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f6c99-105">**Applies to:**</span></span>
- [<span data-ttu-id="f6c99-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f6c99-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="f6c99-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f6c99-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="f6c99-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="f6c99-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="f6c99-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f6c99-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="f6c99-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="f6c99-110">API description</span></span>
<span data-ttu-id="f6c99-111">Isole un appareil de l’accès au réseau externe.</span><span class="sxs-lookup"><span data-stu-id="f6c99-111">Isolates a device from accessing external network.</span></span>


## <a name="limitations"></a><span data-ttu-id="f6c99-112">Limites</span><span class="sxs-lookup"><span data-stu-id="f6c99-112">Limitations</span></span>
1. <span data-ttu-id="f6c99-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="f6c99-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


[!include[Device actions note](../../includes/machineactionsnote.md)]

## <a name="permissions"></a><span data-ttu-id="f6c99-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="f6c99-114">Permissions</span></span>
<span data-ttu-id="f6c99-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="f6c99-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="f6c99-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="f6c99-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="f6c99-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="f6c99-117">Permission type</span></span> |   <span data-ttu-id="f6c99-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="f6c99-118">Permission</span></span>  |   <span data-ttu-id="f6c99-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="f6c99-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="f6c99-120">Application</span><span class="sxs-lookup"><span data-stu-id="f6c99-120">Application</span></span> |   <span data-ttu-id="f6c99-121">Machine.Isolate</span><span class="sxs-lookup"><span data-stu-id="f6c99-121">Machine.Isolate</span></span> |   <span data-ttu-id="f6c99-122">« Isoler l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="f6c99-122">'Isolate machine'</span></span>
<span data-ttu-id="f6c99-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="f6c99-123">Delegated (work or school account)</span></span> | <span data-ttu-id="f6c99-124">Machine.Isolate</span><span class="sxs-lookup"><span data-stu-id="f6c99-124">Machine.Isolate</span></span> |  <span data-ttu-id="f6c99-125">« Isoler l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="f6c99-125">'Isolate machine'</span></span>

>[!Note]
> <span data-ttu-id="f6c99-126">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="f6c99-126">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="f6c99-127">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Actions de correction actives » (pour plus d’informations, voir Créer et gérer [des](user-roles.md) rôles)</span><span class="sxs-lookup"><span data-stu-id="f6c99-127">The user needs to have at least the following role permission: 'Active remediation actions' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="f6c99-128">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="f6c99-128">The user needs to have access to the device, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>


## <a name="http-request"></a><span data-ttu-id="f6c99-129">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="f6c99-129">HTTP request</span></span>
```
POST https://api.securitycenter.microsoft.com/api/machines/{id}/isolate
```

## <a name="request-headers"></a><span data-ttu-id="f6c99-130">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="f6c99-130">Request headers</span></span>

<span data-ttu-id="f6c99-131">Nom</span><span class="sxs-lookup"><span data-stu-id="f6c99-131">Name</span></span> | <span data-ttu-id="f6c99-132">Type</span><span class="sxs-lookup"><span data-stu-id="f6c99-132">Type</span></span> | <span data-ttu-id="f6c99-133">Description</span><span class="sxs-lookup"><span data-stu-id="f6c99-133">Description</span></span>
:---|:---|:---
<span data-ttu-id="f6c99-134">Autorisation</span><span class="sxs-lookup"><span data-stu-id="f6c99-134">Authorization</span></span> | <span data-ttu-id="f6c99-135">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f6c99-135">String</span></span> | <span data-ttu-id="f6c99-136">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="f6c99-136">Bearer {token}.</span></span> <span data-ttu-id="f6c99-137">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="f6c99-137">**Required**.</span></span>
<span data-ttu-id="f6c99-138">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f6c99-138">Content-Type</span></span> | <span data-ttu-id="f6c99-139">string</span><span class="sxs-lookup"><span data-stu-id="f6c99-139">string</span></span> | <span data-ttu-id="f6c99-140">application/json.</span><span class="sxs-lookup"><span data-stu-id="f6c99-140">application/json.</span></span> <span data-ttu-id="f6c99-141">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="f6c99-141">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="f6c99-142">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="f6c99-142">Request body</span></span>
<span data-ttu-id="f6c99-143">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f6c99-143">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="f6c99-144">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f6c99-144">Parameter</span></span> | <span data-ttu-id="f6c99-145">Type</span><span class="sxs-lookup"><span data-stu-id="f6c99-145">Type</span></span>    | <span data-ttu-id="f6c99-146">Description</span><span class="sxs-lookup"><span data-stu-id="f6c99-146">Description</span></span>
:---|:---|:---
<span data-ttu-id="f6c99-147">Commentaire</span><span class="sxs-lookup"><span data-stu-id="f6c99-147">Comment</span></span> |   <span data-ttu-id="f6c99-148">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f6c99-148">String</span></span> |    <span data-ttu-id="f6c99-149">Commentaire à associer à l’action.</span><span class="sxs-lookup"><span data-stu-id="f6c99-149">Comment to associate with the action.</span></span> <span data-ttu-id="f6c99-150">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="f6c99-150">**Required**.</span></span>
<span data-ttu-id="f6c99-151">IsolationType</span><span class="sxs-lookup"><span data-stu-id="f6c99-151">IsolationType</span></span>   | <span data-ttu-id="f6c99-152">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f6c99-152">String</span></span> |  <span data-ttu-id="f6c99-153">Type de l’isolation.</span><span class="sxs-lookup"><span data-stu-id="f6c99-153">Type of the isolation.</span></span> <span data-ttu-id="f6c99-154">Les valeurs autorisées sont : « Full » ou « Selective ».</span><span class="sxs-lookup"><span data-stu-id="f6c99-154">Allowed values are: 'Full' or 'Selective'.</span></span>

<span data-ttu-id="f6c99-155">**IsolationType** contrôle le type d’isolation à effectuer et peut être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="f6c99-155">**IsolationType** controls the type of isolation to perform and can be one of the following:</span></span>
- <span data-ttu-id="f6c99-156">Complète – Isolation complète</span><span class="sxs-lookup"><span data-stu-id="f6c99-156">Full – Full isolation</span></span>
- <span data-ttu-id="f6c99-157">Sélectif : empêcher uniquement un ensemble limité d’applications d’accéder au réseau (voir [Isoler](respond-machine-alerts.md#isolate-devices-from-the-network) les appareils du réseau pour plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="f6c99-157">Selective – Restrict only limited set of applications from accessing the network (see [Isolate devices from the network](respond-machine-alerts.md#isolate-devices-from-the-network) for more details)</span></span>


## <a name="response"></a><span data-ttu-id="f6c99-158">Réponse</span><span class="sxs-lookup"><span data-stu-id="f6c99-158">Response</span></span>
<span data-ttu-id="f6c99-159">Si elle réussit, cette méthode renvoie 201 : code de réponse créé et action de [l’ordinateur](machineaction.md) dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="f6c99-159">If successful, this method returns 201 - Created response code and [Machine Action](machineaction.md) in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="f6c99-160">Exemple</span><span class="sxs-lookup"><span data-stu-id="f6c99-160">Example</span></span>

<span data-ttu-id="f6c99-161">**Demande**</span><span class="sxs-lookup"><span data-stu-id="f6c99-161">**Request**</span></span>

<span data-ttu-id="f6c99-162">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="f6c99-162">Here is an example of the request.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/machines/1e5bc9d7e413ddd7902c2932e418702b84d0cc07/isolate
```

```json
{
  "Comment": "Isolate machine due to alert 1234",
  "IsolationType": "Full" 
}
```

- <span data-ttu-id="f6c99-163">Pour libérer un appareil de l’isolation, voir [Libérer l’appareil de l’isolation.](unisolate-machine.md)</span><span class="sxs-lookup"><span data-stu-id="f6c99-163">To release a device from isolation, see [Release device from isolation](unisolate-machine.md).</span></span>
