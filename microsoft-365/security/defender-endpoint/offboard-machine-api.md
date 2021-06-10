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
# <a name="offboard-machine-api"></a><span data-ttu-id="dcdcf-104">API d’ordinateur de tableau de bord</span><span class="sxs-lookup"><span data-stu-id="dcdcf-104">Offboard machine API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="dcdcf-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="dcdcf-105">**Applies to:**</span></span>
- [<span data-ttu-id="dcdcf-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="dcdcf-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="dcdcf-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="dcdcf-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="dcdcf-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="dcdcf-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="dcdcf-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 



[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="dcdcf-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="dcdcf-110">API description</span></span>
<span data-ttu-id="dcdcf-111">Appareil de tableau de bord à partir de Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-111">Offboard device from Defender for Endpoint.</span></span>


## <a name="limitations"></a><span data-ttu-id="dcdcf-112">Limites</span><span class="sxs-lookup"><span data-stu-id="dcdcf-112">Limitations</span></span>
 - <span data-ttu-id="dcdcf-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


[!include[Machine actions note](../../includes/machineactionsnote.md)]

>[!Note]
> <span data-ttu-id="dcdcf-114">Cette API est prise en charge Windows 10, les versions 1703 et ultérieures, ou Windows Server 2019 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-114">This API is supported on Windows 10, version 1703 and later, or Windows Server 2019 and later.</span></span> <span data-ttu-id="dcdcf-115">Cette API n’est pas prise en charge sur les appareils MacOS ou Linux.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-115">This API is not supported on MacOS or Linux devices.</span></span>

## <a name="permissions"></a><span data-ttu-id="dcdcf-116">Autorisations</span><span class="sxs-lookup"><span data-stu-id="dcdcf-116">Permissions</span></span>
<span data-ttu-id="dcdcf-117">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-117">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="dcdcf-118">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="dcdcf-118">To learn more, including how to choose permissions, see [Use Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="dcdcf-119">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="dcdcf-119">Permission type</span></span> |   <span data-ttu-id="dcdcf-120">Autorisation</span><span class="sxs-lookup"><span data-stu-id="dcdcf-120">Permission</span></span>  |   <span data-ttu-id="dcdcf-121">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="dcdcf-121">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="dcdcf-122">Application</span><span class="sxs-lookup"><span data-stu-id="dcdcf-122">Application</span></span> |   <span data-ttu-id="dcdcf-123">Machine.Offboard</span><span class="sxs-lookup"><span data-stu-id="dcdcf-123">Machine.Offboard</span></span> |  <span data-ttu-id="dcdcf-124">« Offboard machine »</span><span class="sxs-lookup"><span data-stu-id="dcdcf-124">'Offboard machine'</span></span>
<span data-ttu-id="dcdcf-125">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="dcdcf-125">Delegated (work or school account)</span></span> |    <span data-ttu-id="dcdcf-126">Machine.Offboard</span><span class="sxs-lookup"><span data-stu-id="dcdcf-126">Machine.Offboard</span></span> |  <span data-ttu-id="dcdcf-127">« Offboard machine »</span><span class="sxs-lookup"><span data-stu-id="dcdcf-127">'Offboard machine'</span></span>

>[!Note]
> <span data-ttu-id="dcdcf-128">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="dcdcf-128">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="dcdcf-129">L’utilisateur doit avoir le rôle aD « Administrateur global »</span><span class="sxs-lookup"><span data-stu-id="dcdcf-129">The user needs to 'Global Admin' AD role</span></span>
>- <span data-ttu-id="dcdcf-130">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="dcdcf-130">The user needs to have access to the device, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="dcdcf-131">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="dcdcf-131">HTTP request</span></span>
```
POST https://api.securitycenter.microsoft.com/api/machines/{id}/offboard
```

## <a name="request-headers"></a><span data-ttu-id="dcdcf-132">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="dcdcf-132">Request headers</span></span>

<span data-ttu-id="dcdcf-133">Nom</span><span class="sxs-lookup"><span data-stu-id="dcdcf-133">Name</span></span> | <span data-ttu-id="dcdcf-134">Type</span><span class="sxs-lookup"><span data-stu-id="dcdcf-134">Type</span></span> | <span data-ttu-id="dcdcf-135">Description</span><span class="sxs-lookup"><span data-stu-id="dcdcf-135">Description</span></span>
:---|:---|:---
<span data-ttu-id="dcdcf-136">Autorisation</span><span class="sxs-lookup"><span data-stu-id="dcdcf-136">Authorization</span></span> | <span data-ttu-id="dcdcf-137">String</span><span class="sxs-lookup"><span data-stu-id="dcdcf-137">String</span></span> | <span data-ttu-id="dcdcf-138">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-138">Bearer {token}.</span></span> <span data-ttu-id="dcdcf-139">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-139">**Required**.</span></span>
<span data-ttu-id="dcdcf-140">Content-Type</span><span class="sxs-lookup"><span data-stu-id="dcdcf-140">Content-Type</span></span> | <span data-ttu-id="dcdcf-141">string</span><span class="sxs-lookup"><span data-stu-id="dcdcf-141">string</span></span> | <span data-ttu-id="dcdcf-142">application/json.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-142">application/json.</span></span> <span data-ttu-id="dcdcf-143">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-143">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="dcdcf-144">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="dcdcf-144">Request body</span></span>
<span data-ttu-id="dcdcf-145">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="dcdcf-145">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="dcdcf-146">Paramètre</span><span class="sxs-lookup"><span data-stu-id="dcdcf-146">Parameter</span></span> | <span data-ttu-id="dcdcf-147">Type</span><span class="sxs-lookup"><span data-stu-id="dcdcf-147">Type</span></span>    | <span data-ttu-id="dcdcf-148">Description</span><span class="sxs-lookup"><span data-stu-id="dcdcf-148">Description</span></span>
:---|:---|:---
<span data-ttu-id="dcdcf-149">Commentaire</span><span class="sxs-lookup"><span data-stu-id="dcdcf-149">Comment</span></span> |   <span data-ttu-id="dcdcf-150">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dcdcf-150">String</span></span> |    <span data-ttu-id="dcdcf-151">Commentaire à associer à l’action.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-151">Comment to associate with the action.</span></span> <span data-ttu-id="dcdcf-152">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-152">**Required**.</span></span>

## <a name="response"></a><span data-ttu-id="dcdcf-153">Réponse</span><span class="sxs-lookup"><span data-stu-id="dcdcf-153">Response</span></span>
<span data-ttu-id="dcdcf-154">Si elle réussit, cette méthode renvoie 201 : code de réponse créé et action de [l’ordinateur](machineaction.md) dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-154">If successful, this method returns 201 - Created response code and [Machine Action](machineaction.md) in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="dcdcf-155">Exemple</span><span class="sxs-lookup"><span data-stu-id="dcdcf-155">Example</span></span>

<span data-ttu-id="dcdcf-156">**Demande**</span><span class="sxs-lookup"><span data-stu-id="dcdcf-156">**Request**</span></span>

<span data-ttu-id="dcdcf-157">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-157">Here is an example of the request.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/machines/1e5bc9d7e413ddd7902c2932e418702b84d0cc07/offboard
```

```json
{
  "Comment": "Offboard machine by automation"
}
```
