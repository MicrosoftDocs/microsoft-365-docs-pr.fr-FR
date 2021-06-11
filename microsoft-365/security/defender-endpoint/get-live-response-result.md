---
title: Obtenir des résultats de réponse en direct
description: Découvrez comment récupérer un résultat de commande de réponse en direct spécifique par son index.
keywords: api, api de graphique, api pris en charge, téléchargement vers la bibliothèque
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
ms.openlocfilehash: d58fc87d16bb58199c95933d85752008a08a0e81
ms.sourcegitcommit: 337e8d8a2fee112d799edd8a0e04b3a2f124f900
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "52879732"
---
#  <a name="get-live-response-results"></a><span data-ttu-id="3a9bb-104">Obtenir des résultats de réponse en direct</span><span class="sxs-lookup"><span data-stu-id="3a9bb-104">Get live response results</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="3a9bb-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3a9bb-105">**Applies to:**</span></span>
- [<span data-ttu-id="3a9bb-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3a9bb-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)

[!include[Prerelease information](../../includes/prerelease.md)]

><span data-ttu-id="3a9bb-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="3a9bb-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="3a9bb-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="3a9bb-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="3a9bb-109">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="3a9bb-109">API description</span></span>

<span data-ttu-id="3a9bb-110">Récupère un résultat de commande de réponse en direct spécifique par son index.</span><span class="sxs-lookup"><span data-stu-id="3a9bb-110">Retrieves a specific live response command result by its index.</span></span>

## <a name="limitations"></a><span data-ttu-id="3a9bb-111">Limites</span><span class="sxs-lookup"><span data-stu-id="3a9bb-111">Limitations</span></span>

1.  <span data-ttu-id="3a9bb-112">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="3a9bb-112">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>

## <a name="permissions"></a><span data-ttu-id="3a9bb-113">Autorisations</span><span class="sxs-lookup"><span data-stu-id="3a9bb-113">Permissions</span></span>

<span data-ttu-id="3a9bb-114">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="3a9bb-114">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="3a9bb-115">Pour en savoir plus, notamment sur le choix des autorisations, [consultez La mise en place.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="3a9bb-115">To learn more, including how to choose permissions, see [Get started](apis-intro.md).</span></span>

| <span data-ttu-id="3a9bb-116">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="3a9bb-116">Permission type</span></span>                    | <span data-ttu-id="3a9bb-117">Autorisation</span><span class="sxs-lookup"><span data-stu-id="3a9bb-117">Permission</span></span>           | <span data-ttu-id="3a9bb-118">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="3a9bb-118">Permission display name</span></span>                   |
|------------------------------------|----------------------|-------------------------------------------|
| <span data-ttu-id="3a9bb-119">Application</span><span class="sxs-lookup"><span data-stu-id="3a9bb-119">Application</span></span>                        | <span data-ttu-id="3a9bb-120">Machine.LiveResponse</span><span class="sxs-lookup"><span data-stu-id="3a9bb-120">Machine.LiveResponse</span></span> | <span data-ttu-id="3a9bb-121">Exécuter une réponse en direct sur un ordinateur spécifique</span><span class="sxs-lookup"><span data-stu-id="3a9bb-121">Run live response on a specific machine</span></span> |
| <span data-ttu-id="3a9bb-122">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="3a9bb-122">Delegated (work or school account)</span></span> | <span data-ttu-id="3a9bb-123">Machine.LiveResponse</span><span class="sxs-lookup"><span data-stu-id="3a9bb-123">Machine.LiveResponse</span></span> | <span data-ttu-id="3a9bb-124">Exécuter une réponse en direct sur un ordinateur spécifique</span><span class="sxs-lookup"><span data-stu-id="3a9bb-124">Run live response on a specific machine</span></span> |

## <a name="http-request"></a><span data-ttu-id="3a9bb-125">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="3a9bb-125">HTTP request</span></span>

```HTTP
GET https://api.securitycenter.microsoft.com/api/machineactions/{machine action
id}/GetLiveResponseResultDownloadLink(index={command-index})
```

## <a name="request-headers"></a><span data-ttu-id="3a9bb-126">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="3a9bb-126">Request headers</span></span>

| <span data-ttu-id="3a9bb-127">Nom</span><span class="sxs-lookup"><span data-stu-id="3a9bb-127">Name</span></span>      | <span data-ttu-id="3a9bb-128">Type</span><span class="sxs-lookup"><span data-stu-id="3a9bb-128">Type</span></span> | <span data-ttu-id="3a9bb-129">Description</span><span class="sxs-lookup"><span data-stu-id="3a9bb-129">Description</span></span>               |
|---------------|----------|-------------------------------|
| <span data-ttu-id="3a9bb-130">Autorisation</span><span class="sxs-lookup"><span data-stu-id="3a9bb-130">Authorization</span></span> | <span data-ttu-id="3a9bb-131">String</span><span class="sxs-lookup"><span data-stu-id="3a9bb-131">String</span></span>   | <span data-ttu-id="3a9bb-p103">Porteur {token}. Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3a9bb-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3a9bb-134">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="3a9bb-134">Request body</span></span>

<span data-ttu-id="3a9bb-135">Vide</span><span class="sxs-lookup"><span data-stu-id="3a9bb-135">Empty</span></span>

## <a name="response"></a><span data-ttu-id="3a9bb-136">Réponse</span><span class="sxs-lookup"><span data-stu-id="3a9bb-136">Response</span></span>

<span data-ttu-id="3a9bb-137">Si elle réussit, cette méthode renvoie un code de réponse 200, Ok avec un objet qui contient le lien vers le résultat de commande dans la *propriété value.*</span><span class="sxs-lookup"><span data-stu-id="3a9bb-137">If successful, this method returns 200, Ok response code with object that holds the link to the command result in the *value* property.</span></span> <span data-ttu-id="3a9bb-138">Ce lien est valide pendant 30 minutes et doit être utilisé immédiatement pour télécharger le package dans un stockage local.</span><span class="sxs-lookup"><span data-stu-id="3a9bb-138">This link is valid for 30 minutes and should be used immediately for downloading the package to a local storage.</span></span> <span data-ttu-id="3a9bb-139">Un lien expiré peut être re-créé par un autre appel et il n’est pas nécessaire d’exécuter à nouveau une réponse en direct.</span><span class="sxs-lookup"><span data-stu-id="3a9bb-139">An expired link can be re-created by another call, and there is no need to run live response again.</span></span>

<span data-ttu-id="3a9bb-140">*Propriétés de transcription Runscript :*</span><span class="sxs-lookup"><span data-stu-id="3a9bb-140">*Runscript transcript properties:*</span></span>

| <span data-ttu-id="3a9bb-141">Propriété</span><span class="sxs-lookup"><span data-stu-id="3a9bb-141">Property</span></span>  | <span data-ttu-id="3a9bb-142">Description</span><span class="sxs-lookup"><span data-stu-id="3a9bb-142">Description</span></span>                       |
|---------------|---------------------------------------|
| <span data-ttu-id="3a9bb-143">name</span><span class="sxs-lookup"><span data-stu-id="3a9bb-143">name</span></span>          | <span data-ttu-id="3a9bb-144">Nom du script exécuté</span><span class="sxs-lookup"><span data-stu-id="3a9bb-144">Executed script name</span></span>                  |
| <span data-ttu-id="3a9bb-145">exit_code</span><span class="sxs-lookup"><span data-stu-id="3a9bb-145">exit_code</span></span>     | <span data-ttu-id="3a9bb-146">Code de sortie de script exécuté</span><span class="sxs-lookup"><span data-stu-id="3a9bb-146">Executed script exit code</span></span>             |
| <span data-ttu-id="3a9bb-147">script_output</span><span class="sxs-lookup"><span data-stu-id="3a9bb-147">script_output</span></span> | <span data-ttu-id="3a9bb-148">Sortie standard du script exécuté</span><span class="sxs-lookup"><span data-stu-id="3a9bb-148">Executed script standard output</span></span>       |
| <span data-ttu-id="3a9bb-149">script_error</span><span class="sxs-lookup"><span data-stu-id="3a9bb-149">script_error</span></span>  | <span data-ttu-id="3a9bb-150">Sortie d’erreur standard du script exécuté</span><span class="sxs-lookup"><span data-stu-id="3a9bb-150">Executed script standard error output</span></span> |

## <a name="example"></a><span data-ttu-id="3a9bb-151">Exemple</span><span class="sxs-lookup"><span data-stu-id="3a9bb-151">Example</span></span>

<span data-ttu-id="3a9bb-152">**Demande**</span><span class="sxs-lookup"><span data-stu-id="3a9bb-152">**Request**</span></span>

<span data-ttu-id="3a9bb-153">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="3a9bb-153">Here is an example of the request.</span></span>

```HTTP
GET
https://api.securitycenter.microsoft.com/api/machineactions/988cc94e-7a8f-4b28-ab65-54970c5d5018/GetLiveResponseResultDownloadLink(index=0)
```

<span data-ttu-id="3a9bb-154">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="3a9bb-154">**Response**</span></span>

<span data-ttu-id="3a9bb-155">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="3a9bb-155">Here is an example of the response.</span></span>

<span data-ttu-id="3a9bb-156">HTTP/1.1 200 Ok</span><span class="sxs-lookup"><span data-stu-id="3a9bb-156">HTTP/1.1 200 Ok</span></span>

<span data-ttu-id="3a9bb-157">Content-type: application/json</span><span class="sxs-lookup"><span data-stu-id="3a9bb-157">Content-type: application/json</span></span>

```JSON
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Edm.String",
    "value": "https://core.windows.net/investigation-actions-data/ID/CustomPlaybookCommandOutput/4ed5e7807ad1fe59b00b664fe06a0f07?se=2021-02-04T16%3A13%3A50Z&sp=r&sv=2019-07-07&sr=b&sig=1dYGe9rPvUlXBPvYSmr6/OLXPY98m8qWqfIQCBbyZTY%3D"
}
```

<span data-ttu-id="3a9bb-158">*Contenu du fichier :*</span><span class="sxs-lookup"><span data-stu-id="3a9bb-158">*File content:*</span></span> 

```JSON
{
    "script_name": "minidump.ps1",
    "exit_code": 0,
    "script_output": "Transcript started, output file is C:\\ProgramData\\Microsoft\\Windows Defender Advanced Threat Protection\\Temp\\PSScriptOutputs\\PSScript_Transcript_{TRANSCRIPT_ID}.txt
C:\\windows\\TEMP\\OfficeClickToRun.dmp.zip\n51 MB\n\u0000\u0000\u0000",
    "script_error":""
}
```

## <a name="related-topics"></a><span data-ttu-id="3a9bb-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a9bb-159">Related topics</span></span>

- [<span data-ttu-id="3a9bb-160">API Obtenir l’action de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="3a9bb-160">Get machine action API</span></span>](get-machineaction-object.md)
- [<span data-ttu-id="3a9bb-161">Annuler l’action de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="3a9bb-161">Cancel machine action</span></span>](cancel-machine-action.md)
- [<span data-ttu-id="3a9bb-162">Exécuter une réponse en direct</span><span class="sxs-lookup"><span data-stu-id="3a9bb-162">Run live response</span></span>](run-live-response.md) 
