---
title: SUPPRIMER l’API de restriction d’application
description: Utilisez cette API pour créer des appels liés à la suppression d’une restriction d’exécution d’applications.
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
ms.openlocfilehash: abff4e02bfdfe6f5598ca96121815930dce3c85e
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51199320"
---
# <a name="remove-app-restriction-api"></a><span data-ttu-id="1e7d5-104">SUPPRIMER l’API de restriction d’application</span><span class="sxs-lookup"><span data-stu-id="1e7d5-104">Remove app restriction API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="1e7d5-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1e7d5-105">**Applies to:**</span></span>
- [<span data-ttu-id="1e7d5-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1e7d5-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="1e7d5-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1e7d5-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="1e7d5-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="1e7d5-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="1e7d5-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="1e7d5-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 


[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="1e7d5-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="1e7d5-110">API description</span></span>
<span data-ttu-id="1e7d5-111">Activez l’exécution de n’importe quelle application sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1e7d5-111">Enable execution of any application on the device.</span></span>


## <a name="limitations"></a><span data-ttu-id="1e7d5-112">Limites</span><span class="sxs-lookup"><span data-stu-id="1e7d5-112">Limitations</span></span>
1. <span data-ttu-id="1e7d5-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="1e7d5-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


[!include[Device actions note](../../includes/machineactionsnote.md)]

## <a name="permissions"></a><span data-ttu-id="1e7d5-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="1e7d5-114">Permissions</span></span>
<span data-ttu-id="1e7d5-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="1e7d5-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="1e7d5-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="1e7d5-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="1e7d5-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="1e7d5-117">Permission type</span></span> |   <span data-ttu-id="1e7d5-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="1e7d5-118">Permission</span></span>  |   <span data-ttu-id="1e7d5-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="1e7d5-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="1e7d5-120">Application</span><span class="sxs-lookup"><span data-stu-id="1e7d5-120">Application</span></span> |   <span data-ttu-id="1e7d5-121">Machine.RestrictExecution</span><span class="sxs-lookup"><span data-stu-id="1e7d5-121">Machine.RestrictExecution</span></span> | <span data-ttu-id="1e7d5-122">« Restreindre l’exécution du code »</span><span class="sxs-lookup"><span data-stu-id="1e7d5-122">'Restrict code execution'</span></span>
<span data-ttu-id="1e7d5-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="1e7d5-123">Delegated (work or school account)</span></span> | <span data-ttu-id="1e7d5-124">Machine.RestrictExecution</span><span class="sxs-lookup"><span data-stu-id="1e7d5-124">Machine.RestrictExecution</span></span> | <span data-ttu-id="1e7d5-125">« Restreindre l’exécution du code »</span><span class="sxs-lookup"><span data-stu-id="1e7d5-125">'Restrict code execution'</span></span>

>[!Note]
> <span data-ttu-id="1e7d5-126">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="1e7d5-126">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="1e7d5-127">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Actions de correction actives » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="1e7d5-127">The user needs to have at least the following role permission: 'Active remediation actions' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="1e7d5-128">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="1e7d5-128">The user needs to have access to the device, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="1e7d5-129">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="1e7d5-129">HTTP request</span></span>
```
POST https://api.securitycenter.microsoft.com/api/machines/{id}/unrestrictCodeExecution
```

## <a name="request-headers"></a><span data-ttu-id="1e7d5-130">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="1e7d5-130">Request headers</span></span>
<span data-ttu-id="1e7d5-131">Nom</span><span class="sxs-lookup"><span data-stu-id="1e7d5-131">Name</span></span> | <span data-ttu-id="1e7d5-132">Type</span><span class="sxs-lookup"><span data-stu-id="1e7d5-132">Type</span></span> | <span data-ttu-id="1e7d5-133">Description</span><span class="sxs-lookup"><span data-stu-id="1e7d5-133">Description</span></span>
:---|:---|:---
<span data-ttu-id="1e7d5-134">Autorisation</span><span class="sxs-lookup"><span data-stu-id="1e7d5-134">Authorization</span></span> | <span data-ttu-id="1e7d5-135">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1e7d5-135">String</span></span> | <span data-ttu-id="1e7d5-136">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="1e7d5-136">Bearer {token}.</span></span> <span data-ttu-id="1e7d5-137">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="1e7d5-137">**Required**.</span></span>
<span data-ttu-id="1e7d5-138">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1e7d5-138">Content-Type</span></span> | <span data-ttu-id="1e7d5-139">string</span><span class="sxs-lookup"><span data-stu-id="1e7d5-139">string</span></span> | <span data-ttu-id="1e7d5-140">application/json.</span><span class="sxs-lookup"><span data-stu-id="1e7d5-140">application/json.</span></span> <span data-ttu-id="1e7d5-141">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="1e7d5-141">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="1e7d5-142">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="1e7d5-142">Request body</span></span>
<span data-ttu-id="1e7d5-143">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="1e7d5-143">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="1e7d5-144">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1e7d5-144">Parameter</span></span> | <span data-ttu-id="1e7d5-145">Type</span><span class="sxs-lookup"><span data-stu-id="1e7d5-145">Type</span></span>    | <span data-ttu-id="1e7d5-146">Description</span><span class="sxs-lookup"><span data-stu-id="1e7d5-146">Description</span></span>
:---|:---|:---
<span data-ttu-id="1e7d5-147">Commentaire</span><span class="sxs-lookup"><span data-stu-id="1e7d5-147">Comment</span></span> |   <span data-ttu-id="1e7d5-148">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1e7d5-148">String</span></span> | <span data-ttu-id="1e7d5-149">Commentaire à associer à l’action.</span><span class="sxs-lookup"><span data-stu-id="1e7d5-149">Comment to associate with the action.</span></span> <span data-ttu-id="1e7d5-150">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="1e7d5-150">**Required**.</span></span>

## <a name="response"></a><span data-ttu-id="1e7d5-151">Réponse</span><span class="sxs-lookup"><span data-stu-id="1e7d5-151">Response</span></span>
<span data-ttu-id="1e7d5-152">Si elle réussit, cette méthode renvoie 201 : code de réponse créé et action de [l’ordinateur](machineaction.md) dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="1e7d5-152">If successful, this method returns 201 - Created response code and [Machine Action](machineaction.md) in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="1e7d5-153">Exemple</span><span class="sxs-lookup"><span data-stu-id="1e7d5-153">Example</span></span>

<span data-ttu-id="1e7d5-154">**Demande**</span><span class="sxs-lookup"><span data-stu-id="1e7d5-154">**Request**</span></span>

<span data-ttu-id="1e7d5-155">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="1e7d5-155">Here is an example of the request.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/machines/1e5bc9d7e413ddd7902c2932e418702b84d0cc07/unrestrictCodeExecution 
```

```json
{
  "Comment": "Unrestrict code execution since machine was cleaned and validated"
}

```


<span data-ttu-id="1e7d5-156">Pour restreindre l’exécution du code sur un appareil, voir [Restreindre l’exécution de l’application.](restrict-code-execution.md)</span><span class="sxs-lookup"><span data-stu-id="1e7d5-156">To restrict code execution on a device, see [Restrict app execution](restrict-code-execution.md).</span></span>
