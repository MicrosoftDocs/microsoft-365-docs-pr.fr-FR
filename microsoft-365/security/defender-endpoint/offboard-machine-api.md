---
title: API d’ordinateur de tableau de bord
description: Découvrez comment utiliser une API pour hors connexion d’un appareil à partir de Microsoft Defender pour endpoint.
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
ms.openlocfilehash: e2b1114cd091c9cd42aa8e4525416f9d73358a65
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52771992"
---
# <a name="offboard-machine-api"></a><span data-ttu-id="7129d-104">API d’ordinateur de tableau de bord</span><span class="sxs-lookup"><span data-stu-id="7129d-104">Offboard machine API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="7129d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="7129d-105">**Applies to:**</span></span>
- [<span data-ttu-id="7129d-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7129d-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="7129d-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="7129d-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="7129d-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="7129d-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="7129d-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="7129d-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 



[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="7129d-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="7129d-110">API description</span></span>
<span data-ttu-id="7129d-111">Appareil de tableau de bord à partir de Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="7129d-111">Offboard device from Defender for Endpoint.</span></span>


## <a name="limitations"></a><span data-ttu-id="7129d-112">Limitations</span><span class="sxs-lookup"><span data-stu-id="7129d-112">Limitations</span></span>
 - <span data-ttu-id="7129d-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="7129d-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


[!include[Machine actions note](../../includes/machineactionsnote.md)]

>[!Note]
> <span data-ttu-id="7129d-114">Cette API est prise en charge Windows 10, les versions 1703 et ultérieures, ou Windows Server 2019 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7129d-114">This API is supported on Windows 10, version 1703 and later, or Windows Server 2019 and later.</span></span> <span data-ttu-id="7129d-115">Cette API n’est pas prise en charge sur les appareils MacOS ou Linux.</span><span class="sxs-lookup"><span data-stu-id="7129d-115">This API is not supported on MacOS or Linux devices.</span></span>

## <a name="permissions"></a><span data-ttu-id="7129d-116">Autorisations</span><span class="sxs-lookup"><span data-stu-id="7129d-116">Permissions</span></span>
<span data-ttu-id="7129d-117">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="7129d-117">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="7129d-118">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="7129d-118">To learn more, including how to choose permissions, see [Use Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="7129d-119">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="7129d-119">Permission type</span></span> |   <span data-ttu-id="7129d-120">Autorisation</span><span class="sxs-lookup"><span data-stu-id="7129d-120">Permission</span></span>  |   <span data-ttu-id="7129d-121">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="7129d-121">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="7129d-122">Application</span><span class="sxs-lookup"><span data-stu-id="7129d-122">Application</span></span> |   <span data-ttu-id="7129d-123">Machine.Offboard</span><span class="sxs-lookup"><span data-stu-id="7129d-123">Machine.Offboard</span></span> |  <span data-ttu-id="7129d-124">« Offboard machine »</span><span class="sxs-lookup"><span data-stu-id="7129d-124">'Offboard machine'</span></span>
<span data-ttu-id="7129d-125">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="7129d-125">Delegated (work or school account)</span></span> |    <span data-ttu-id="7129d-126">Machine.Offboard</span><span class="sxs-lookup"><span data-stu-id="7129d-126">Machine.Offboard</span></span> |  <span data-ttu-id="7129d-127">« Offboard machine »</span><span class="sxs-lookup"><span data-stu-id="7129d-127">'Offboard machine'</span></span>

>[!Note]
> <span data-ttu-id="7129d-128">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="7129d-128">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="7129d-129">L’utilisateur doit avoir le rôle aD « Administrateur global »</span><span class="sxs-lookup"><span data-stu-id="7129d-129">The user needs to 'Global Admin' AD role</span></span>
>- <span data-ttu-id="7129d-130">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="7129d-130">The user needs to have access to the device, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="7129d-131">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="7129d-131">HTTP request</span></span>
```
POST https://api.securitycenter.microsoft.com/api/machines/{id}/offboard
```

## <a name="request-headers"></a><span data-ttu-id="7129d-132">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="7129d-132">Request headers</span></span>

<span data-ttu-id="7129d-133">Nom</span><span class="sxs-lookup"><span data-stu-id="7129d-133">Name</span></span> | <span data-ttu-id="7129d-134">Type</span><span class="sxs-lookup"><span data-stu-id="7129d-134">Type</span></span> | <span data-ttu-id="7129d-135">Description</span><span class="sxs-lookup"><span data-stu-id="7129d-135">Description</span></span>
:---|:---|:---
<span data-ttu-id="7129d-136">Autorisation</span><span class="sxs-lookup"><span data-stu-id="7129d-136">Authorization</span></span> | <span data-ttu-id="7129d-137">String</span><span class="sxs-lookup"><span data-stu-id="7129d-137">String</span></span> | <span data-ttu-id="7129d-138">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="7129d-138">Bearer {token}.</span></span> <span data-ttu-id="7129d-139">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="7129d-139">**Required**.</span></span>
<span data-ttu-id="7129d-140">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7129d-140">Content-Type</span></span> | <span data-ttu-id="7129d-141">string</span><span class="sxs-lookup"><span data-stu-id="7129d-141">string</span></span> | <span data-ttu-id="7129d-142">application/json.</span><span class="sxs-lookup"><span data-stu-id="7129d-142">application/json.</span></span> <span data-ttu-id="7129d-143">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="7129d-143">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="7129d-144">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="7129d-144">Request body</span></span>
<span data-ttu-id="7129d-145">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7129d-145">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="7129d-146">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7129d-146">Parameter</span></span> | <span data-ttu-id="7129d-147">Type</span><span class="sxs-lookup"><span data-stu-id="7129d-147">Type</span></span>    | <span data-ttu-id="7129d-148">Description</span><span class="sxs-lookup"><span data-stu-id="7129d-148">Description</span></span>
:---|:---|:---
<span data-ttu-id="7129d-149">Commentaire</span><span class="sxs-lookup"><span data-stu-id="7129d-149">Comment</span></span> |   <span data-ttu-id="7129d-150">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7129d-150">String</span></span> |    <span data-ttu-id="7129d-151">Commentaire à associer à l’action.</span><span class="sxs-lookup"><span data-stu-id="7129d-151">Comment to associate with the action.</span></span> <span data-ttu-id="7129d-152">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="7129d-152">**Required**.</span></span>

## <a name="response"></a><span data-ttu-id="7129d-153">Réponse</span><span class="sxs-lookup"><span data-stu-id="7129d-153">Response</span></span>
<span data-ttu-id="7129d-154">Si elle réussit, cette méthode renvoie 201 - Code de réponse créé et Action de [l’ordinateur](machineaction.md) dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="7129d-154">If successful, this method returns 201 - Created response code and [Machine Action](machineaction.md) in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="7129d-155">Exemple</span><span class="sxs-lookup"><span data-stu-id="7129d-155">Example</span></span>

<span data-ttu-id="7129d-156">**Demande**</span><span class="sxs-lookup"><span data-stu-id="7129d-156">**Request**</span></span>

<span data-ttu-id="7129d-157">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="7129d-157">Here is an example of the request.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/machines/1e5bc9d7e413ddd7902c2932e418702b84d0cc07/offboard
```

```json
{
  "Comment": "Offboard machine by automation"
}
```
