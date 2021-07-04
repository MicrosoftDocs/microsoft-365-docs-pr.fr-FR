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
ms.openlocfilehash: 4cf60ea73ea907be9c10b2dd9562a0ea60127f2d
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53289894"
---
# <a name="collect-investigation-package-api"></a><span data-ttu-id="8cabe-104">API collecter un package d’examen</span><span class="sxs-lookup"><span data-stu-id="8cabe-104">Collect investigation package API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="8cabe-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8cabe-105">**Applies to:**</span></span>
- [<span data-ttu-id="8cabe-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8cabe-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="8cabe-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8cabe-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


- <span data-ttu-id="8cabe-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="8cabe-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="8cabe-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="8cabe-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="8cabe-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="8cabe-110">API description</span></span>

<span data-ttu-id="8cabe-111">Collecter un package d’examen à partir d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="8cabe-111">Collect investigation package from a device.</span></span>

## <a name="limitations"></a><span data-ttu-id="8cabe-112">Limites</span><span class="sxs-lookup"><span data-stu-id="8cabe-112">Limitations</span></span>

1. <span data-ttu-id="8cabe-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="8cabe-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>

## <a name="permissions"></a><span data-ttu-id="8cabe-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="8cabe-114">Permissions</span></span>

<span data-ttu-id="8cabe-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="8cabe-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="8cabe-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="8cabe-116">To learn more, including how to choose permissions, see [Use Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="8cabe-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="8cabe-117">Permission type</span></span> | <span data-ttu-id="8cabe-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="8cabe-118">Permission</span></span> | <span data-ttu-id="8cabe-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="8cabe-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="8cabe-120">Application</span><span class="sxs-lookup"><span data-stu-id="8cabe-120">Application</span></span> | <span data-ttu-id="8cabe-121">Machine.CollectForensics</span><span class="sxs-lookup"><span data-stu-id="8cabe-121">Machine.CollectForensics</span></span> | <span data-ttu-id="8cabe-122">« Collecter les enquêtes légales »</span><span class="sxs-lookup"><span data-stu-id="8cabe-122">'Collect forensics'</span></span>
<span data-ttu-id="8cabe-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="8cabe-123">Delegated (work or school account)</span></span> | <span data-ttu-id="8cabe-124">Machine.CollectForensics</span><span class="sxs-lookup"><span data-stu-id="8cabe-124">Machine.CollectForensics</span></span> | <span data-ttu-id="8cabe-125">« Collecter les enquêtes légales »</span><span class="sxs-lookup"><span data-stu-id="8cabe-125">'Collect forensics'</span></span>

> [!NOTE]
> <span data-ttu-id="8cabe-126">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="8cabe-126">When obtaining a token using user credentials:</span></span>
>
> - <span data-ttu-id="8cabe-127">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Alerts Investigation » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="8cabe-127">The user needs to have at least the following role permission: 'Alerts Investigation' (See [Create and manage roles](user-roles.md) for more information)</span></span>
> - <span data-ttu-id="8cabe-128">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="8cabe-128">The user needs to have access to the device, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="8cabe-129">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="8cabe-129">HTTP request</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/machines/{id}/collectInvestigationPackage
```

## <a name="request-headers"></a><span data-ttu-id="8cabe-130">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="8cabe-130">Request headers</span></span>

<span data-ttu-id="8cabe-131">Nom</span><span class="sxs-lookup"><span data-stu-id="8cabe-131">Name</span></span> | <span data-ttu-id="8cabe-132">Type</span><span class="sxs-lookup"><span data-stu-id="8cabe-132">Type</span></span> | <span data-ttu-id="8cabe-133">Description</span><span class="sxs-lookup"><span data-stu-id="8cabe-133">Description</span></span>
:---|:---|:---
<span data-ttu-id="8cabe-134">Autorisation</span><span class="sxs-lookup"><span data-stu-id="8cabe-134">Authorization</span></span> | <span data-ttu-id="8cabe-135">String</span><span class="sxs-lookup"><span data-stu-id="8cabe-135">String</span></span> | <span data-ttu-id="8cabe-136">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="8cabe-136">Bearer {token}.</span></span> <span data-ttu-id="8cabe-137">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="8cabe-137">**Required**.</span></span>
<span data-ttu-id="8cabe-138">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8cabe-138">Content-Type</span></span> | <span data-ttu-id="8cabe-139">string</span><span class="sxs-lookup"><span data-stu-id="8cabe-139">string</span></span> | <span data-ttu-id="8cabe-140">application/json.</span><span class="sxs-lookup"><span data-stu-id="8cabe-140">application/json.</span></span> <span data-ttu-id="8cabe-141">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="8cabe-141">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="8cabe-142">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="8cabe-142">Request body</span></span>

<span data-ttu-id="8cabe-143">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8cabe-143">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="8cabe-144">Paramètre</span><span class="sxs-lookup"><span data-stu-id="8cabe-144">Parameter</span></span> | <span data-ttu-id="8cabe-145">Type</span><span class="sxs-lookup"><span data-stu-id="8cabe-145">Type</span></span> | <span data-ttu-id="8cabe-146">Description</span><span class="sxs-lookup"><span data-stu-id="8cabe-146">Description</span></span>
:---|:---|:---
<span data-ttu-id="8cabe-147">Commentaire</span><span class="sxs-lookup"><span data-stu-id="8cabe-147">Comment</span></span> | <span data-ttu-id="8cabe-148">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8cabe-148">String</span></span> | <span data-ttu-id="8cabe-149">Commentaire à associer à l’action.</span><span class="sxs-lookup"><span data-stu-id="8cabe-149">Comment to associate with the action.</span></span> <span data-ttu-id="8cabe-150">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="8cabe-150">**Required**.</span></span>

## <a name="response"></a><span data-ttu-id="8cabe-151">Réponse</span><span class="sxs-lookup"><span data-stu-id="8cabe-151">Response</span></span>

<span data-ttu-id="8cabe-152">Si elle réussit, cette méthode renvoie 201 : code de réponse créé et action de [l’ordinateur](machineaction.md) dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="8cabe-152">If successful, this method returns 201 - Created response code and [Machine Action](machineaction.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8cabe-153">Exemple</span><span class="sxs-lookup"><span data-stu-id="8cabe-153">Example</span></span>

### <a name="request"></a><span data-ttu-id="8cabe-154">Demande</span><span class="sxs-lookup"><span data-stu-id="8cabe-154">Request</span></span>

<span data-ttu-id="8cabe-155">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="8cabe-155">Here is an example of the request.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/machines/fb9ab6be3965095a09c057be7c90f0a2/collectInvestigationPackage
```

```json
{
  "Comment": "Collect forensics due to alert 1234"
}
```
