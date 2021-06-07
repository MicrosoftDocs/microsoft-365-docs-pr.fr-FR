---
title: API Restreindre l’exécution de l’application
description: Utilisez cette API pour créer des appels liés à la restriction de l’exécution d’une application.
keywords: api, api de graphique, api pris en charge, collecter un package d’enquête
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
ms.openlocfilehash: 7195e91a3a9b7aef6977c925f2c8689d3e461815
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52771572"
---
# <a name="restrict-app-execution-api"></a><span data-ttu-id="2c2b8-104">API Restreindre l’exécution de l’application</span><span class="sxs-lookup"><span data-stu-id="2c2b8-104">Restrict app execution API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="2c2b8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2c2b8-105">**Applies to:**</span></span>
- [<span data-ttu-id="2c2b8-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2c2b8-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="2c2b8-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2c2b8-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="2c2b8-108">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="2c2b8-108">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="2c2b8-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="2c2b8-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="2c2b8-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="2c2b8-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="2c2b8-111">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="2c2b8-111">API description</span></span>
<span data-ttu-id="2c2b8-112">Limiter l’exécution de toutes les applications sur l’appareil à l’exception d’un ensemble prédéféré.</span><span class="sxs-lookup"><span data-stu-id="2c2b8-112">Restrict execution of all applications on the device except a predefined set.</span></span>


## <a name="limitations"></a><span data-ttu-id="2c2b8-113">Limitations</span><span class="sxs-lookup"><span data-stu-id="2c2b8-113">Limitations</span></span>
1. <span data-ttu-id="2c2b8-114">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="2c2b8-114">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


[!include[Device actions note](../../includes/machineactionsnote.md)]

## <a name="permissions"></a><span data-ttu-id="2c2b8-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="2c2b8-115">Permissions</span></span>
<span data-ttu-id="2c2b8-116">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="2c2b8-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="2c2b8-117">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="2c2b8-117">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="2c2b8-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="2c2b8-118">Permission type</span></span> |   <span data-ttu-id="2c2b8-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="2c2b8-119">Permission</span></span>  |   <span data-ttu-id="2c2b8-120">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="2c2b8-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="2c2b8-121">Application</span><span class="sxs-lookup"><span data-stu-id="2c2b8-121">Application</span></span> |   <span data-ttu-id="2c2b8-122">Machine.RestrictExecution</span><span class="sxs-lookup"><span data-stu-id="2c2b8-122">Machine.RestrictExecution</span></span> | <span data-ttu-id="2c2b8-123">« Restreindre l’exécution du code »</span><span class="sxs-lookup"><span data-stu-id="2c2b8-123">'Restrict code execution'</span></span>
<span data-ttu-id="2c2b8-124">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="2c2b8-124">Delegated (work or school account)</span></span> | <span data-ttu-id="2c2b8-125">Machine.RestrictExecution</span><span class="sxs-lookup"><span data-stu-id="2c2b8-125">Machine.RestrictExecution</span></span> | <span data-ttu-id="2c2b8-126">« Restreindre l’exécution du code »</span><span class="sxs-lookup"><span data-stu-id="2c2b8-126">'Restrict code execution'</span></span>

>[!Note]
> <span data-ttu-id="2c2b8-127">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="2c2b8-127">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="2c2b8-128">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Actions de correction actives » (pour plus d’informations, voir Créer et gérer [des](user-roles.md) rôles)</span><span class="sxs-lookup"><span data-stu-id="2c2b8-128">The user needs to have at least the following role permission: 'Active remediation actions' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="2c2b8-129">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="2c2b8-129">The user needs to have access to the device, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="2c2b8-130">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="2c2b8-130">HTTP request</span></span>
```
POST https://api.securitycenter.microsoft.com/api/machines/{id}/restrictCodeExecution
```

## <a name="request-headers"></a><span data-ttu-id="2c2b8-131">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="2c2b8-131">Request headers</span></span>

<span data-ttu-id="2c2b8-132">Nom</span><span class="sxs-lookup"><span data-stu-id="2c2b8-132">Name</span></span> | <span data-ttu-id="2c2b8-133">Type</span><span class="sxs-lookup"><span data-stu-id="2c2b8-133">Type</span></span> | <span data-ttu-id="2c2b8-134">Description</span><span class="sxs-lookup"><span data-stu-id="2c2b8-134">Description</span></span>
:---|:---|:---
<span data-ttu-id="2c2b8-135">Autorisation</span><span class="sxs-lookup"><span data-stu-id="2c2b8-135">Authorization</span></span> | <span data-ttu-id="2c2b8-136">String</span><span class="sxs-lookup"><span data-stu-id="2c2b8-136">String</span></span> | <span data-ttu-id="2c2b8-137">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="2c2b8-137">Bearer {token}.</span></span> <span data-ttu-id="2c2b8-138">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="2c2b8-138">**Required**.</span></span>
<span data-ttu-id="2c2b8-139">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2c2b8-139">Content-Type</span></span> | <span data-ttu-id="2c2b8-140">string</span><span class="sxs-lookup"><span data-stu-id="2c2b8-140">string</span></span> | <span data-ttu-id="2c2b8-141">application/json.</span><span class="sxs-lookup"><span data-stu-id="2c2b8-141">application/json.</span></span> <span data-ttu-id="2c2b8-142">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="2c2b8-142">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="2c2b8-143">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="2c2b8-143">Request body</span></span>
<span data-ttu-id="2c2b8-144">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="2c2b8-144">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="2c2b8-145">Paramètre</span><span class="sxs-lookup"><span data-stu-id="2c2b8-145">Parameter</span></span> | <span data-ttu-id="2c2b8-146">Type</span><span class="sxs-lookup"><span data-stu-id="2c2b8-146">Type</span></span>    | <span data-ttu-id="2c2b8-147">Description</span><span class="sxs-lookup"><span data-stu-id="2c2b8-147">Description</span></span>
:---|:---|:---
<span data-ttu-id="2c2b8-148">Commentaire</span><span class="sxs-lookup"><span data-stu-id="2c2b8-148">Comment</span></span> |   <span data-ttu-id="2c2b8-149">Chaîne</span><span class="sxs-lookup"><span data-stu-id="2c2b8-149">String</span></span> |    <span data-ttu-id="2c2b8-150">Commentaire à associer à l’action.</span><span class="sxs-lookup"><span data-stu-id="2c2b8-150">Comment to associate with the action.</span></span> <span data-ttu-id="2c2b8-151">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="2c2b8-151">**Required**.</span></span>

## <a name="response"></a><span data-ttu-id="2c2b8-152">Réponse</span><span class="sxs-lookup"><span data-stu-id="2c2b8-152">Response</span></span>
<span data-ttu-id="2c2b8-153">Si elle réussit, cette méthode renvoie 201 : code de réponse créé et action de [l’ordinateur](machineaction.md) dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="2c2b8-153">If successful, this method returns 201 - Created response code and [Machine Action](machineaction.md) in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="2c2b8-154">Exemple</span><span class="sxs-lookup"><span data-stu-id="2c2b8-154">Example</span></span>

<span data-ttu-id="2c2b8-155">**Demande**</span><span class="sxs-lookup"><span data-stu-id="2c2b8-155">**Request**</span></span>

<span data-ttu-id="2c2b8-156">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="2c2b8-156">Here is an example of the request.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/machines/1e5bc9d7e413ddd7902c2932e418702b84d0cc07/restrictCodeExecution 
```

```json
{
  "Comment": "Restrict code execution due to alert 1234"
}

```

- <span data-ttu-id="2c2b8-157">Pour supprimer la restriction d’exécution du code d’un appareil, voir [Supprimer la restriction d’application.](unrestrict-code-execution.md)</span><span class="sxs-lookup"><span data-stu-id="2c2b8-157">To remove code execution restriction from a device, see [Remove app restriction](unrestrict-code-execution.md).</span></span>
