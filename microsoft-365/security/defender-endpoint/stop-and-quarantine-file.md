---
title: API de fichier d’arrêt et de mise en quarantaine
description: Découvrez comment arrêter l’exécution d’un fichier sur un appareil et supprimer le fichier dans Microsoft Defender pour endpoint. Consultez un exemple.
keywords: api, api de graphique, api pris en charge, arrêter et mettre en quarantaine le fichier
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
ms.openlocfilehash: ac14f1ecda2b6256dc19223869b8878e6e725b96
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52771401"
---
# <a name="stop-and-quarantine-file-api"></a><span data-ttu-id="c2a58-105">API de fichier d’arrêt et de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="c2a58-105">Stop and quarantine file API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="c2a58-106">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="c2a58-106">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="c2a58-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="c2a58-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="c2a58-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="c2a58-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="c2a58-109">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="c2a58-109">API description</span></span>
<span data-ttu-id="c2a58-110">Arrêtez l’exécution d’un fichier sur un appareil et supprimez-le.</span><span class="sxs-lookup"><span data-stu-id="c2a58-110">Stop execution of a file on a device and delete it.</span></span>


## <a name="limitations"></a><span data-ttu-id="c2a58-111">Limitations</span><span class="sxs-lookup"><span data-stu-id="c2a58-111">Limitations</span></span>
1. <span data-ttu-id="c2a58-112">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="c2a58-112">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


[!include[Device actions note](../../includes/machineactionsnote.md)]

## <a name="permissions"></a><span data-ttu-id="c2a58-113">Autorisations</span><span class="sxs-lookup"><span data-stu-id="c2a58-113">Permissions</span></span>
<span data-ttu-id="c2a58-114">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="c2a58-114">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="c2a58-115">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="c2a58-115">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="c2a58-116">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="c2a58-116">Permission type</span></span> |   <span data-ttu-id="c2a58-117">Autorisation</span><span class="sxs-lookup"><span data-stu-id="c2a58-117">Permission</span></span>  |   <span data-ttu-id="c2a58-118">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="c2a58-118">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="c2a58-119">Application</span><span class="sxs-lookup"><span data-stu-id="c2a58-119">Application</span></span> |   <span data-ttu-id="c2a58-120">Machine.StopAndQuarantine</span><span class="sxs-lookup"><span data-stu-id="c2a58-120">Machine.StopAndQuarantine</span></span> | <span data-ttu-id="c2a58-121">« Arrêter et mettre en quarantaine »</span><span class="sxs-lookup"><span data-stu-id="c2a58-121">'Stop And Quarantine'</span></span>
<span data-ttu-id="c2a58-122">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="c2a58-122">Delegated (work or school account)</span></span> | <span data-ttu-id="c2a58-123">Machine.StopAndQuarantine</span><span class="sxs-lookup"><span data-stu-id="c2a58-123">Machine.StopAndQuarantine</span></span> | <span data-ttu-id="c2a58-124">« Arrêter et mettre en quarantaine »</span><span class="sxs-lookup"><span data-stu-id="c2a58-124">'Stop And Quarantine'</span></span>

>[!Note]
> <span data-ttu-id="c2a58-125">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="c2a58-125">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="c2a58-126">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Actions de correction actives » (pour plus d’informations, voir Créer et gérer [des](user-roles.md) rôles)</span><span class="sxs-lookup"><span data-stu-id="c2a58-126">The user needs to have at least the following role permission: 'Active remediation actions' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="c2a58-127">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="c2a58-127">The user needs to have access to the device, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="c2a58-128">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="c2a58-128">HTTP request</span></span>
```
POST https://api.securitycenter.microsoft.com/api/machines/{id}/StopAndQuarantineFile
```

## <a name="request-headers"></a><span data-ttu-id="c2a58-129">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="c2a58-129">Request headers</span></span>

<span data-ttu-id="c2a58-130">Nom</span><span class="sxs-lookup"><span data-stu-id="c2a58-130">Name</span></span> | <span data-ttu-id="c2a58-131">Type</span><span class="sxs-lookup"><span data-stu-id="c2a58-131">Type</span></span> | <span data-ttu-id="c2a58-132">Description</span><span class="sxs-lookup"><span data-stu-id="c2a58-132">Description</span></span>
:---|:---|:---
<span data-ttu-id="c2a58-133">Autorisation</span><span class="sxs-lookup"><span data-stu-id="c2a58-133">Authorization</span></span> | <span data-ttu-id="c2a58-134">String</span><span class="sxs-lookup"><span data-stu-id="c2a58-134">String</span></span> | <span data-ttu-id="c2a58-135">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="c2a58-135">Bearer {token}.</span></span> <span data-ttu-id="c2a58-136">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="c2a58-136">**Required**.</span></span>
<span data-ttu-id="c2a58-137">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c2a58-137">Content-Type</span></span> | <span data-ttu-id="c2a58-138">string</span><span class="sxs-lookup"><span data-stu-id="c2a58-138">string</span></span> | <span data-ttu-id="c2a58-139">application/json.</span><span class="sxs-lookup"><span data-stu-id="c2a58-139">application/json.</span></span> <span data-ttu-id="c2a58-140">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="c2a58-140">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="c2a58-141">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="c2a58-141">Request body</span></span>
<span data-ttu-id="c2a58-142">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="c2a58-142">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="c2a58-143">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c2a58-143">Parameter</span></span> | <span data-ttu-id="c2a58-144">Type</span><span class="sxs-lookup"><span data-stu-id="c2a58-144">Type</span></span>    | <span data-ttu-id="c2a58-145">Description</span><span class="sxs-lookup"><span data-stu-id="c2a58-145">Description</span></span>
:---|:---|:---
<span data-ttu-id="c2a58-146">Commentaire</span><span class="sxs-lookup"><span data-stu-id="c2a58-146">Comment</span></span> |   <span data-ttu-id="c2a58-147">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c2a58-147">String</span></span> |    <span data-ttu-id="c2a58-148">Commentaire à associer à l’action.</span><span class="sxs-lookup"><span data-stu-id="c2a58-148">Comment to associate with the action.</span></span> <span data-ttu-id="c2a58-149">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="c2a58-149">**Required**.</span></span>
<span data-ttu-id="c2a58-150">Sha1</span><span class="sxs-lookup"><span data-stu-id="c2a58-150">Sha1</span></span> |  <span data-ttu-id="c2a58-151">String</span><span class="sxs-lookup"><span data-stu-id="c2a58-151">String</span></span>   | <span data-ttu-id="c2a58-152">Sha1 du fichier à arrêter et mettre en quarantaine sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c2a58-152">Sha1 of the file to stop and quarantine on the device.</span></span> <span data-ttu-id="c2a58-153">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="c2a58-153">**Required**.</span></span>

## <a name="response"></a><span data-ttu-id="c2a58-154">Réponse</span><span class="sxs-lookup"><span data-stu-id="c2a58-154">Response</span></span>
<span data-ttu-id="c2a58-155">Si elle réussit, cette méthode renvoie 201 - Code de réponse créé et Action de [l’ordinateur](machineaction.md) dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="c2a58-155">If successful, this method returns 201 - Created response code and [Machine Action](machineaction.md) in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="c2a58-156">Exemple</span><span class="sxs-lookup"><span data-stu-id="c2a58-156">Example</span></span>

<span data-ttu-id="c2a58-157">**Demande**</span><span class="sxs-lookup"><span data-stu-id="c2a58-157">**Request**</span></span>

<span data-ttu-id="c2a58-158">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="c2a58-158">Here is an example of the request.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/machines/1e5bc9d7e413ddd7902c2932e418702b84d0cc07/StopAndQuarantineFile 
```

```json
{
  "Comment": "Stop and quarantine file on machine due to alert 441688558380765161_2136280442",
  "Sha1": "87662bc3d60e4200ceaf7aae249d1c343f4b83c9"
}

```
