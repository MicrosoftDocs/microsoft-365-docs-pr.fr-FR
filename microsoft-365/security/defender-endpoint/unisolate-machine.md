---
title: LIBÉRER l’appareil à partir de l’API d’isolation
description: Utilisez cette API pour créer des appels liés à la libération d’un appareil de l’isolation.
keywords: api, api de graphique, api pris en charge, supprimer l’appareil de l’isolation
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
ms.openlocfilehash: 036eb6f589c13fb9232557c45619829149179148
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51199332"
---
# <a name="release-device-from-isolation-api"></a><span data-ttu-id="f7d49-104">LIBÉRER l’appareil à partir de l’API d’isolation</span><span class="sxs-lookup"><span data-stu-id="f7d49-104">Release device from isolation API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f7d49-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f7d49-105">**Applies to:**</span></span> 
- [<span data-ttu-id="f7d49-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f7d49-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="f7d49-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f7d49-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

- <span data-ttu-id="f7d49-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="f7d49-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="f7d49-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f7d49-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="f7d49-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="f7d49-110">API description</span></span>
<span data-ttu-id="f7d49-111">Annuler l’isolation d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="f7d49-111">Undo isolation of a device.</span></span>


## <a name="limitations"></a><span data-ttu-id="f7d49-112">Limites</span><span class="sxs-lookup"><span data-stu-id="f7d49-112">Limitations</span></span>
1. <span data-ttu-id="f7d49-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="f7d49-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


[!include[Device actions note](../../includes/machineactionsnote.md)]

## <a name="permissions"></a><span data-ttu-id="f7d49-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="f7d49-114">Permissions</span></span>
<span data-ttu-id="f7d49-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="f7d49-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="f7d49-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="f7d49-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="f7d49-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="f7d49-117">Permission type</span></span> |   <span data-ttu-id="f7d49-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="f7d49-118">Permission</span></span>  |   <span data-ttu-id="f7d49-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="f7d49-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="f7d49-120">Application</span><span class="sxs-lookup"><span data-stu-id="f7d49-120">Application</span></span> |   <span data-ttu-id="f7d49-121">Machine.Isolate</span><span class="sxs-lookup"><span data-stu-id="f7d49-121">Machine.Isolate</span></span> |   <span data-ttu-id="f7d49-122">« Isoler l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="f7d49-122">'Isolate machine'</span></span>
<span data-ttu-id="f7d49-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="f7d49-123">Delegated (work or school account)</span></span> |    <span data-ttu-id="f7d49-124">Machine.Isolate</span><span class="sxs-lookup"><span data-stu-id="f7d49-124">Machine.Isolate</span></span> |   <span data-ttu-id="f7d49-125">« Isoler l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="f7d49-125">'Isolate machine'</span></span>

>[!Note]
> <span data-ttu-id="f7d49-126">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="f7d49-126">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="f7d49-127">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Actions de correction actives » (pour plus d’informations, voir Créer et gérer [des](user-roles.md) rôles)</span><span class="sxs-lookup"><span data-stu-id="f7d49-127">The user needs to have at least the following role permission: 'Active remediation actions' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="f7d49-128">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="f7d49-128">The user needs to have access to the device, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="f7d49-129">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="f7d49-129">HTTP request</span></span>
```
POST https://api.securitycenter.microsoft.com/api/machines/{id}/unisolate
```

## <a name="request-headers"></a><span data-ttu-id="f7d49-130">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="f7d49-130">Request headers</span></span>

<span data-ttu-id="f7d49-131">Nom</span><span class="sxs-lookup"><span data-stu-id="f7d49-131">Name</span></span> | <span data-ttu-id="f7d49-132">Type</span><span class="sxs-lookup"><span data-stu-id="f7d49-132">Type</span></span> | <span data-ttu-id="f7d49-133">Description</span><span class="sxs-lookup"><span data-stu-id="f7d49-133">Description</span></span>
:---|:---|:---
<span data-ttu-id="f7d49-134">Autorisation</span><span class="sxs-lookup"><span data-stu-id="f7d49-134">Authorization</span></span> | <span data-ttu-id="f7d49-135">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f7d49-135">String</span></span> | <span data-ttu-id="f7d49-136">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="f7d49-136">Bearer {token}.</span></span> <span data-ttu-id="f7d49-137">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="f7d49-137">**Required**.</span></span>
<span data-ttu-id="f7d49-138">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f7d49-138">Content-Type</span></span> | <span data-ttu-id="f7d49-139">string</span><span class="sxs-lookup"><span data-stu-id="f7d49-139">string</span></span> | <span data-ttu-id="f7d49-140">application/json.</span><span class="sxs-lookup"><span data-stu-id="f7d49-140">application/json.</span></span> <span data-ttu-id="f7d49-141">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="f7d49-141">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="f7d49-142">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="f7d49-142">Request body</span></span>
<span data-ttu-id="f7d49-143">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f7d49-143">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="f7d49-144">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f7d49-144">Parameter</span></span> | <span data-ttu-id="f7d49-145">Type</span><span class="sxs-lookup"><span data-stu-id="f7d49-145">Type</span></span>    | <span data-ttu-id="f7d49-146">Description</span><span class="sxs-lookup"><span data-stu-id="f7d49-146">Description</span></span>
:---|:---|:---
<span data-ttu-id="f7d49-147">Commentaire</span><span class="sxs-lookup"><span data-stu-id="f7d49-147">Comment</span></span> |   <span data-ttu-id="f7d49-148">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f7d49-148">String</span></span> |    <span data-ttu-id="f7d49-149">Commentaire à associer à l’action.</span><span class="sxs-lookup"><span data-stu-id="f7d49-149">Comment to associate with the action.</span></span> <span data-ttu-id="f7d49-150">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="f7d49-150">**Required**.</span></span>

## <a name="response"></a><span data-ttu-id="f7d49-151">Réponse</span><span class="sxs-lookup"><span data-stu-id="f7d49-151">Response</span></span>
<span data-ttu-id="f7d49-152">Si elle réussit, cette méthode renvoie 201 - Code de réponse créé et Action de [l’ordinateur](machineaction.md) dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="f7d49-152">If successful, this method returns 201 - Created response code and [Machine Action](machineaction.md) in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="f7d49-153">Exemple</span><span class="sxs-lookup"><span data-stu-id="f7d49-153">Example</span></span>

<span data-ttu-id="f7d49-154">**Demande**</span><span class="sxs-lookup"><span data-stu-id="f7d49-154">**Request**</span></span>

<span data-ttu-id="f7d49-155">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="f7d49-155">Here is an example of the request.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/machines/1e5bc9d7e413ddd7902c2932e418702b84d0cc07/unisolate 
```

```json
{
  "Comment": "Unisolate machine since it was clean and validated"
}

```


- <span data-ttu-id="f7d49-156">Pour isoler un appareil, voir [Isoler l’appareil.](isolate-machine.md)</span><span class="sxs-lookup"><span data-stu-id="f7d49-156">To isolate a device, see [Isolate device](isolate-machine.md).</span></span>

