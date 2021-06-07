---
title: API collecter un package d’examen
description: Utilisez cette API pour créer des appels liés à la collecte d’un package d’enquête à partir d’un appareil.
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
ms.openlocfilehash: 0083d806f3e52307e6dce30f74e255073a09c16a
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52770492"
---
# <a name="collect-investigation-package-api"></a><span data-ttu-id="fb52a-104">API collecter un package d’examen</span><span class="sxs-lookup"><span data-stu-id="fb52a-104">Collect investigation package API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="fb52a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="fb52a-105">**Applies to:**</span></span>
- [<span data-ttu-id="fb52a-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fb52a-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="fb52a-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="fb52a-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


- <span data-ttu-id="fb52a-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="fb52a-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="fb52a-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="fb52a-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="fb52a-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="fb52a-110">API description</span></span>
<span data-ttu-id="fb52a-111">Collecter un package d’examen à partir d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="fb52a-111">Collect investigation package from a device.</span></span>


## <a name="limitations"></a><span data-ttu-id="fb52a-112">Limitations</span><span class="sxs-lookup"><span data-stu-id="fb52a-112">Limitations</span></span>
1. <span data-ttu-id="fb52a-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="fb52a-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="fb52a-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="fb52a-114">Permissions</span></span>
<span data-ttu-id="fb52a-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="fb52a-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="fb52a-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="fb52a-116">To learn more, including how to choose permissions, see [Use Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="fb52a-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="fb52a-117">Permission type</span></span> |   <span data-ttu-id="fb52a-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="fb52a-118">Permission</span></span>  |   <span data-ttu-id="fb52a-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="fb52a-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="fb52a-120">Application</span><span class="sxs-lookup"><span data-stu-id="fb52a-120">Application</span></span> |   <span data-ttu-id="fb52a-121">Machine.CollectForensics</span><span class="sxs-lookup"><span data-stu-id="fb52a-121">Machine.CollectForensics</span></span> |  <span data-ttu-id="fb52a-122">« Collecter les enquêtes légales »</span><span class="sxs-lookup"><span data-stu-id="fb52a-122">'Collect forensics'</span></span>
<span data-ttu-id="fb52a-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="fb52a-123">Delegated (work or school account)</span></span> |    <span data-ttu-id="fb52a-124">Machine.CollectForensics</span><span class="sxs-lookup"><span data-stu-id="fb52a-124">Machine.CollectForensics</span></span> |  <span data-ttu-id="fb52a-125">« Collecter les enquêtes légales »</span><span class="sxs-lookup"><span data-stu-id="fb52a-125">'Collect forensics'</span></span>

>[!Note]
> <span data-ttu-id="fb52a-126">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="fb52a-126">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="fb52a-127">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Alerts Investigation » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="fb52a-127">The user needs to have at least the following role permission: 'Alerts Investigation' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="fb52a-128">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="fb52a-128">The user needs to have access to the device, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="fb52a-129">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="fb52a-129">HTTP request</span></span>
```
POST https://api.securitycenter.microsoft.com/api/machines/{id}/collectInvestigationPackage
```

## <a name="request-headers"></a><span data-ttu-id="fb52a-130">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="fb52a-130">Request headers</span></span>

<span data-ttu-id="fb52a-131">Nom</span><span class="sxs-lookup"><span data-stu-id="fb52a-131">Name</span></span> | <span data-ttu-id="fb52a-132">Type</span><span class="sxs-lookup"><span data-stu-id="fb52a-132">Type</span></span> | <span data-ttu-id="fb52a-133">Description</span><span class="sxs-lookup"><span data-stu-id="fb52a-133">Description</span></span>
:---|:---|:---
<span data-ttu-id="fb52a-134">Autorisation</span><span class="sxs-lookup"><span data-stu-id="fb52a-134">Authorization</span></span> | <span data-ttu-id="fb52a-135">String</span><span class="sxs-lookup"><span data-stu-id="fb52a-135">String</span></span> | <span data-ttu-id="fb52a-136">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="fb52a-136">Bearer {token}.</span></span> <span data-ttu-id="fb52a-137">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="fb52a-137">**Required**.</span></span>
<span data-ttu-id="fb52a-138">Content-Type</span><span class="sxs-lookup"><span data-stu-id="fb52a-138">Content-Type</span></span> | <span data-ttu-id="fb52a-139">string</span><span class="sxs-lookup"><span data-stu-id="fb52a-139">string</span></span> | <span data-ttu-id="fb52a-140">application/json.</span><span class="sxs-lookup"><span data-stu-id="fb52a-140">application/json.</span></span> <span data-ttu-id="fb52a-141">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="fb52a-141">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="fb52a-142">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="fb52a-142">Request body</span></span>
<span data-ttu-id="fb52a-143">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="fb52a-143">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="fb52a-144">Paramètre</span><span class="sxs-lookup"><span data-stu-id="fb52a-144">Parameter</span></span> | <span data-ttu-id="fb52a-145">Type</span><span class="sxs-lookup"><span data-stu-id="fb52a-145">Type</span></span>    | <span data-ttu-id="fb52a-146">Description</span><span class="sxs-lookup"><span data-stu-id="fb52a-146">Description</span></span>
:---|:---|:---
<span data-ttu-id="fb52a-147">Commentaire</span><span class="sxs-lookup"><span data-stu-id="fb52a-147">Comment</span></span> |   <span data-ttu-id="fb52a-148">Chaîne</span><span class="sxs-lookup"><span data-stu-id="fb52a-148">String</span></span> |    <span data-ttu-id="fb52a-149">Commentaire à associer à l’action.</span><span class="sxs-lookup"><span data-stu-id="fb52a-149">Comment to associate with the action.</span></span> <span data-ttu-id="fb52a-150">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="fb52a-150">**Required**.</span></span>

## <a name="response"></a><span data-ttu-id="fb52a-151">Réponse</span><span class="sxs-lookup"><span data-stu-id="fb52a-151">Response</span></span>
<span data-ttu-id="fb52a-152">Si elle réussit, cette méthode renvoie 201 - Code de réponse créé et Action de [l’ordinateur](machineaction.md) dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="fb52a-152">If successful, this method returns 201 - Created response code and [Machine Action](machineaction.md) in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="fb52a-153">Exemple</span><span class="sxs-lookup"><span data-stu-id="fb52a-153">Example</span></span>

<span data-ttu-id="fb52a-154">**Demande**</span><span class="sxs-lookup"><span data-stu-id="fb52a-154">**Request**</span></span>

<span data-ttu-id="fb52a-155">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="fb52a-155">Here is an example of the request.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/machines/fb9ab6be3965095a09c057be7c90f0a2/collectInvestigationPackage
```

```json
{
  "Comment": "Collect forensics due to alert 1234"
}
```
