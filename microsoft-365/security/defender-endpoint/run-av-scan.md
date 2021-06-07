---
title: API d’analyse antivirus
description: Utilisez cette API pour créer des appels liés à l’exécution d’une analyse antivirus sur un appareil.
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 3df703fd84c87a2bd34bb2a81f8c83063e468b17
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52771447"
---
# <a name="run-antivirus-scan-api"></a><span data-ttu-id="2eebe-104">API d’analyse antivirus</span><span class="sxs-lookup"><span data-stu-id="2eebe-104">Run antivirus scan API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="2eebe-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="2eebe-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="2eebe-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="2eebe-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="2eebe-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="2eebe-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="2eebe-108">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="2eebe-108">API description</span></span>
<span data-ttu-id="2eebe-109">Lancez Antivirus Microsoft Defender analyse sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="2eebe-109">Initiate Microsoft Defender Antivirus scan on a device.</span></span>


## <a name="limitations"></a><span data-ttu-id="2eebe-110">Limitations</span><span class="sxs-lookup"><span data-stu-id="2eebe-110">Limitations</span></span>
1. <span data-ttu-id="2eebe-111">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="2eebe-111">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


[!include[Device actions note](../../includes/machineactionsnote.md)]

## <a name="permissions"></a><span data-ttu-id="2eebe-112">Autorisations</span><span class="sxs-lookup"><span data-stu-id="2eebe-112">Permissions</span></span>
<span data-ttu-id="2eebe-113">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="2eebe-113">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="2eebe-114">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="2eebe-114">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="2eebe-115">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="2eebe-115">Permission type</span></span> |   <span data-ttu-id="2eebe-116">Autorisation</span><span class="sxs-lookup"><span data-stu-id="2eebe-116">Permission</span></span>  |   <span data-ttu-id="2eebe-117">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="2eebe-117">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="2eebe-118">Application</span><span class="sxs-lookup"><span data-stu-id="2eebe-118">Application</span></span> |   <span data-ttu-id="2eebe-119">Machine.Scan</span><span class="sxs-lookup"><span data-stu-id="2eebe-119">Machine.Scan</span></span> |  <span data-ttu-id="2eebe-120">« Analyser l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="2eebe-120">'Scan machine'</span></span>
<span data-ttu-id="2eebe-121">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="2eebe-121">Delegated (work or school account)</span></span> |    <span data-ttu-id="2eebe-122">Machine.Scan</span><span class="sxs-lookup"><span data-stu-id="2eebe-122">Machine.Scan</span></span> |  <span data-ttu-id="2eebe-123">« Analyser l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="2eebe-123">'Scan machine'</span></span>

>[!Note]
> <span data-ttu-id="2eebe-124">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="2eebe-124">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="2eebe-125">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Actions de correction actives » (pour plus d’informations, voir Créer et gérer [des](user-roles.md) rôles)</span><span class="sxs-lookup"><span data-stu-id="2eebe-125">The user needs to have at least the following role permission: 'Active remediation actions' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="2eebe-126">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="2eebe-126">The user needs to have access to the device, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="2eebe-127">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="2eebe-127">HTTP request</span></span>
```
POST https://api.securitycenter.microsoft.com/api/machines/{id}/runAntiVirusScan
```

## <a name="request-headers"></a><span data-ttu-id="2eebe-128">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="2eebe-128">Request headers</span></span>

<span data-ttu-id="2eebe-129">Nom</span><span class="sxs-lookup"><span data-stu-id="2eebe-129">Name</span></span> | <span data-ttu-id="2eebe-130">Type</span><span class="sxs-lookup"><span data-stu-id="2eebe-130">Type</span></span> | <span data-ttu-id="2eebe-131">Description</span><span class="sxs-lookup"><span data-stu-id="2eebe-131">Description</span></span>
:---|:---|:---
<span data-ttu-id="2eebe-132">Autorisation</span><span class="sxs-lookup"><span data-stu-id="2eebe-132">Authorization</span></span> | <span data-ttu-id="2eebe-133">String</span><span class="sxs-lookup"><span data-stu-id="2eebe-133">String</span></span> | <span data-ttu-id="2eebe-134">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="2eebe-134">Bearer {token}.</span></span> <span data-ttu-id="2eebe-135">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="2eebe-135">**Required**.</span></span>
<span data-ttu-id="2eebe-136">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2eebe-136">Content-Type</span></span> | <span data-ttu-id="2eebe-137">string</span><span class="sxs-lookup"><span data-stu-id="2eebe-137">string</span></span> | <span data-ttu-id="2eebe-138">application/json</span><span class="sxs-lookup"><span data-stu-id="2eebe-138">application/json</span></span>

## <a name="request-body"></a><span data-ttu-id="2eebe-139">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="2eebe-139">Request body</span></span>
<span data-ttu-id="2eebe-140">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="2eebe-140">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="2eebe-141">Paramètre</span><span class="sxs-lookup"><span data-stu-id="2eebe-141">Parameter</span></span> | <span data-ttu-id="2eebe-142">Type</span><span class="sxs-lookup"><span data-stu-id="2eebe-142">Type</span></span>    | <span data-ttu-id="2eebe-143">Description</span><span class="sxs-lookup"><span data-stu-id="2eebe-143">Description</span></span>
:---|:---|:---
<span data-ttu-id="2eebe-144">Commentaire</span><span class="sxs-lookup"><span data-stu-id="2eebe-144">Comment</span></span> |   <span data-ttu-id="2eebe-145">Chaîne</span><span class="sxs-lookup"><span data-stu-id="2eebe-145">String</span></span> | <span data-ttu-id="2eebe-146">Commentaire à associer à l’action.</span><span class="sxs-lookup"><span data-stu-id="2eebe-146">Comment to associate with the action.</span></span> <span data-ttu-id="2eebe-147">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="2eebe-147">**Required**.</span></span>
<span data-ttu-id="2eebe-148">ScanType</span><span class="sxs-lookup"><span data-stu-id="2eebe-148">ScanType</span></span>|   <span data-ttu-id="2eebe-149">String</span><span class="sxs-lookup"><span data-stu-id="2eebe-149">String</span></span>  | <span data-ttu-id="2eebe-150">Définit le type de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="2eebe-150">Defines the type of the Scan.</span></span> <span data-ttu-id="2eebe-151">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="2eebe-151">**Required**.</span></span>

<span data-ttu-id="2eebe-152">**ScanType** contrôle le type d’analyse à effectuer et peut être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="2eebe-152">**ScanType** controls the type of scan to perform and can be one of the following:</span></span>

- <span data-ttu-id="2eebe-153">**Rapide** : effectuer une analyse rapide sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="2eebe-153">**Quick** – Perform quick scan on the device</span></span>
- <span data-ttu-id="2eebe-154">**Complète** : effectuer une analyse complète sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="2eebe-154">**Full** – Perform full scan on the device</span></span>



## <a name="response"></a><span data-ttu-id="2eebe-155">Réponse</span><span class="sxs-lookup"><span data-stu-id="2eebe-155">Response</span></span>
<span data-ttu-id="2eebe-156">Si elle réussit, cette méthode renvoie 201, code de réponse créé et _objet MachineAction_ dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="2eebe-156">If successful, this method returns 201, Created response code and _MachineAction_ object in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="2eebe-157">Exemple</span><span class="sxs-lookup"><span data-stu-id="2eebe-157">Example</span></span>

<span data-ttu-id="2eebe-158">**Demande**</span><span class="sxs-lookup"><span data-stu-id="2eebe-158">**Request**</span></span>

<span data-ttu-id="2eebe-159">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="2eebe-159">Here is an example of the request.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/machines/1e5bc9d7e413ddd7902c2932e418702b84d0cc07/runAntiVirusScan 
```

```json
{
  "Comment": "Check machine for viruses due to alert 3212",
  "ScanType": "Full"
}
```

