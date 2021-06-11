---
title: API Annuler l’action de l’ordinateur
description: Découvrez comment annuler une action d’ordinateur déjà lancée
keywords: api, api de graphique,
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
localization_priority: normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 490ee91d5f2d2c02174be94c52fc83fd0ec0fc5e
ms.sourcegitcommit: 337e8d8a2fee112d799edd8a0e04b3a2f124f900
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "52879755"
---
#   <a name="cancel-machine-action-api"></a><span data-ttu-id="62007-104">API Annuler l’action de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="62007-104">Cancel machine action API</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="62007-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="62007-105">**Applies to:**</span></span>
- [<span data-ttu-id="62007-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="62007-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)

[!include[Prerelease information](../../includes/prerelease.md)]

><span data-ttu-id="62007-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="62007-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="62007-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="62007-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="62007-109">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="62007-109">API description</span></span>

<span data-ttu-id="62007-110">Annuler une action de l’ordinateur déjà lancée qui n’est pas encore dans l’état final (terminé, annulé, échoué).</span><span class="sxs-lookup"><span data-stu-id="62007-110">Cancel an already launched machine action that are not yet in final state (completed, cancelled, failed).</span></span>

## <a name="limitations"></a><span data-ttu-id="62007-111">Limites</span><span class="sxs-lookup"><span data-stu-id="62007-111">Limitations</span></span>

1.  <span data-ttu-id="62007-112">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="62007-112">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>

## <a name="permissions"></a><span data-ttu-id="62007-113">Autorisations</span><span class="sxs-lookup"><span data-stu-id="62007-113">Permissions</span></span>

<span data-ttu-id="62007-114">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="62007-114">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="62007-115">Pour en savoir plus, notamment sur le choix des autorisations, [consultez La mise en place.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="62007-115">To learn more, including how to choose permissions, see [Get started](apis-intro.md).</span></span>

|     <span data-ttu-id="62007-116">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="62007-116">Permission    type</span></span>     |     <span data-ttu-id="62007-117">Autorisation</span><span class="sxs-lookup"><span data-stu-id="62007-117">Permission</span></span>     |    <span data-ttu-id="62007-118">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="62007-118">Permission    display name</span></span>     |
|-|-|-|
|    <br><span data-ttu-id="62007-119">Application</span><span class="sxs-lookup"><span data-stu-id="62007-119">Application</span></span>    |    <br><span data-ttu-id="62007-120">Machine.CollectForensic</span><span class="sxs-lookup"><span data-stu-id="62007-120">Machine.CollectForensic</span></span><br>   <span data-ttu-id="62007-121">Machine.Isolate</span><span class="sxs-lookup"><span data-stu-id="62007-121">Machine.Isolate</span></span>   <br><span data-ttu-id="62007-122">Machine.RestrictExecution</span><span class="sxs-lookup"><span data-stu-id="62007-122">Machine.RestrictExecution</span></span><br>   <span data-ttu-id="62007-123">Machine.Scan</span><span class="sxs-lookup"><span data-stu-id="62007-123">Machine.Scan</span></span><br>   <span data-ttu-id="62007-124">Machine.Offboard</span><span class="sxs-lookup"><span data-stu-id="62007-124">Machine.Offboard</span></span><br>   <span data-ttu-id="62007-125">Machine.StopAndQuarantine</span><span class="sxs-lookup"><span data-stu-id="62007-125">Machine.StopAndQuarantine</span></span><br>   <span data-ttu-id="62007-126">Machine.LiveResponse</span><span class="sxs-lookup"><span data-stu-id="62007-126">Machine.LiveResponse</span></span>    |    <span data-ttu-id="62007-127">Collecter des données d’investigation</span><span class="sxs-lookup"><span data-stu-id="62007-127">Collect   forensics</span></span>   <br><span data-ttu-id="62007-128">Isoler l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="62007-128">Isolate   machine</span></span><br><span data-ttu-id="62007-129">Restreindre l’exécution du code</span><span class="sxs-lookup"><span data-stu-id="62007-129">Restrict   code execution</span></span><br>  <span data-ttu-id="62007-130">Ordinateur d’analyse</span><span class="sxs-lookup"><span data-stu-id="62007-130">Scan   machine</span></span><br>  <span data-ttu-id="62007-131">Appareil hors-carte</span><span class="sxs-lookup"><span data-stu-id="62007-131">Offboard   machine</span></span><br>   <span data-ttu-id="62007-132">Arrêter et mettre en quarantaine</span><span class="sxs-lookup"><span data-stu-id="62007-132">Stop And   Quarantine</span></span><br>   <span data-ttu-id="62007-133">Exécuter une réponse en direct sur un ordinateur spécifique</span><span class="sxs-lookup"><span data-stu-id="62007-133">Run live   response on a specific machine</span></span>    |
|    <br><span data-ttu-id="62007-134">Délégué (compte scolaire ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="62007-134">Delegated   (work or school account)</span></span>    |    <span data-ttu-id="62007-135">Machine.CollectForensic</span><span class="sxs-lookup"><span data-stu-id="62007-135">Machine.CollectForensic</span></span><br>   <span data-ttu-id="62007-136">Machine.Isolate</span><span class="sxs-lookup"><span data-stu-id="62007-136">Machine.Isolate</span></span>    <br><span data-ttu-id="62007-137">Machine.RestrictExecution</span><span class="sxs-lookup"><span data-stu-id="62007-137">Machine.RestrictExecution</span></span><br>   <span data-ttu-id="62007-138">Machine.Scan</span><span class="sxs-lookup"><span data-stu-id="62007-138">Machine.Scan</span></span><br>   <span data-ttu-id="62007-139">Machine.Offboard</span><span class="sxs-lookup"><span data-stu-id="62007-139">Machine.Offboard</span></span><br>   <span data-ttu-id="62007-140">Machine.StopAndQuarantineMachine.LiveResponse</span><span class="sxs-lookup"><span data-stu-id="62007-140">Machine.StopAndQuarantineMachine.LiveResponse</span></span>    |    <span data-ttu-id="62007-141">Collecter des données d’investigation</span><span class="sxs-lookup"><span data-stu-id="62007-141">Collect   forensics</span></span><br>   <span data-ttu-id="62007-142">Isoler l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="62007-142">Isolate   machine</span></span><br>  <span data-ttu-id="62007-143">Restreindre l’exécution du code</span><span class="sxs-lookup"><span data-stu-id="62007-143">Restrict   code execution</span></span><br> <span data-ttu-id="62007-144">Ordinateur d’analyse</span><span class="sxs-lookup"><span data-stu-id="62007-144">Scan   machine</span></span><br><span data-ttu-id="62007-145">Appareil hors-carte</span><span class="sxs-lookup"><span data-stu-id="62007-145">Offboard   machine</span></span><br> <span data-ttu-id="62007-146">Arrêter et mettre en quarantaine</span><span class="sxs-lookup"><span data-stu-id="62007-146">Stop And   Quarantine</span></span><br> <span data-ttu-id="62007-147">Exécuter une réponse en direct sur un ordinateur spécifique</span><span class="sxs-lookup"><span data-stu-id="62007-147">Run live   response on a specific machine</span></span>    |


## <a name="http-request"></a><span data-ttu-id="62007-148">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="62007-148">HTTP request</span></span>

```
POST https://api.securitycenter.microsoft.com/api/machineactions/<machineactionid>/cancel  
```


## <a name="request-headers"></a><span data-ttu-id="62007-149">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="62007-149">Request headers</span></span>

| <span data-ttu-id="62007-150">Nom</span><span class="sxs-lookup"><span data-stu-id="62007-150">Name</span></span>      | <span data-ttu-id="62007-151">Type</span><span class="sxs-lookup"><span data-stu-id="62007-151">Type</span></span> | <span data-ttu-id="62007-152">Description</span><span class="sxs-lookup"><span data-stu-id="62007-152">Description</span></span>                 |
|---------------|----------|---------------------------------|
| <span data-ttu-id="62007-153">Autorisation</span><span class="sxs-lookup"><span data-stu-id="62007-153">Authorization</span></span> | <span data-ttu-id="62007-154">String</span><span class="sxs-lookup"><span data-stu-id="62007-154">String</span></span>   | <span data-ttu-id="62007-p103">Porteur {token}. Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="62007-p103">Bearer {token}. Required.</span></span>   |
| <span data-ttu-id="62007-157">Content-Type</span><span class="sxs-lookup"><span data-stu-id="62007-157">Content-Type</span></span>  | <span data-ttu-id="62007-158">string</span><span class="sxs-lookup"><span data-stu-id="62007-158">string</span></span>   | <span data-ttu-id="62007-p104">application/json. Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="62007-p104">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="62007-161">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="62007-161">Request body</span></span>

| <span data-ttu-id="62007-162">Parameter</span><span class="sxs-lookup"><span data-stu-id="62007-162">Parameter</span></span> | <span data-ttu-id="62007-163">Type</span><span class="sxs-lookup"><span data-stu-id="62007-163">Type</span></span> | <span data-ttu-id="62007-164">Description</span><span class="sxs-lookup"><span data-stu-id="62007-164">Description</span></span>                        |
|---------------|----------|----------------------------------------|
| <span data-ttu-id="62007-165">Commentaire</span><span class="sxs-lookup"><span data-stu-id="62007-165">Comment</span></span>       | <span data-ttu-id="62007-166">Chaîne</span><span class="sxs-lookup"><span data-stu-id="62007-166">String</span></span>   | <span data-ttu-id="62007-167">Commentaire à associer à l’action d’annulation.</span><span class="sxs-lookup"><span data-stu-id="62007-167">Comment to associate with the cancellation action.</span></span>  |

## <a name="response"></a><span data-ttu-id="62007-168">Réponse</span><span class="sxs-lookup"><span data-stu-id="62007-168">Response</span></span>

<span data-ttu-id="62007-169">Si elle réussit, cette méthode renvoie le code de réponse 200, Ok avec une entité Action de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="62007-169">If successful, this method returns 200, Ok response code with a Machine Action entity.</span></span> <span data-ttu-id="62007-170">Si l’entité d’action de l’ordinateur avec l’ID spécifié est in trouvée - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="62007-170">If machine action entity with the specified id was not found - 404 Not Found.</span></span>

## <a name="example"></a><span data-ttu-id="62007-171">Exemple</span><span class="sxs-lookup"><span data-stu-id="62007-171">Example</span></span>

<span data-ttu-id="62007-172">**Demande**</span><span class="sxs-lookup"><span data-stu-id="62007-172">**Request**</span></span>

<span data-ttu-id="62007-173">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="62007-173">Here is an example of the request.</span></span>

```HTTP
POST
https://api.securitycenter.microsoft.com/api/machineactions/988cc94e-7a8f-4b28-ab65-54970c5d5018/cancel
```


```JSON
{
    "Comment": "Machine action was canceled by automation"
}
```

## <a name="related-topic"></a><span data-ttu-id="62007-174">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="62007-174">Related topic</span></span>

- [<span data-ttu-id="62007-175">API Obtenir l’action de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="62007-175">Get machine action API</span></span>](get-machineaction-object.md)