---
title: Exécuter des commandes de réponse en direct sur un appareil
description: Découvrez comment exécuter une séquence de commandes de réponse en direct sur un appareil.
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
ms.openlocfilehash: 2a7daf18b1a1d791e7b92ded0a6b839bba1fd4c2
ms.sourcegitcommit: 337e8d8a2fee112d799edd8a0e04b3a2f124f900
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "52879669"
---
#  <a name="run-live-response-commands-on-a-device"></a><span data-ttu-id="3a3bc-104">Exécuter des commandes de réponse en direct sur un appareil</span><span class="sxs-lookup"><span data-stu-id="3a3bc-104">Run live response commands on a device</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="3a3bc-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3a3bc-105">**Applies to:**</span></span>
- [<span data-ttu-id="3a3bc-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3a3bc-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)


[!include[Prerelease information](../../includes/prerelease.md)]

><span data-ttu-id="3a3bc-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="3a3bc-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="3a3bc-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="3a3bc-109">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="3a3bc-109">API description</span></span>

<span data-ttu-id="3a3bc-110">Exécute une séquence de commandes de réponse en direct sur un appareil</span><span class="sxs-lookup"><span data-stu-id="3a3bc-110">Runs a sequence of live response commands on a device</span></span>

## <a name="limitations"></a><span data-ttu-id="3a3bc-111">Limites</span><span class="sxs-lookup"><span data-stu-id="3a3bc-111">Limitations</span></span>

1.  <span data-ttu-id="3a3bc-112">Les limites de taux pour cette API sont de 10 appels par minute (les demandes supplémentaires sont répondues par HTTP 429).</span><span class="sxs-lookup"><span data-stu-id="3a3bc-112">Rate limitations for this API are 10 calls per minute (additional requests are responded with HTTP 429).</span></span>

2.  <span data-ttu-id="3a3bc-113">25 sessions en cours d’exécution simultanée (les demandes dépassant la limite de limitation recevront une réponse « 429 - Trop de demandes »).</span><span class="sxs-lookup"><span data-stu-id="3a3bc-113">25 concurrently running sessions (requests exceeding the throttling limit will receive a "429 - Too many requests" response).</span></span>

3.  <span data-ttu-id="3a3bc-114">Si l’ordinateur n’est pas disponible, la session est en file d’attente pendant 3 jours.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-114">If the machine is not available, the session will be queued for up to 3 days.</span></span>

4.  <span data-ttu-id="3a3bc-115">Le délai d’un délai de commande RunScript est passé au bout de 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-115">RunScript command timeouts after 10 minutes.</span></span>

5.  <span data-ttu-id="3a3bc-116">En cas d’échec d’une commande de réponse en direct, toutes les actions suivies ne sont pas exécutées.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-116">When a live response command fails all followed actions will not be executed.</span></span>

## <a name="permissions"></a><span data-ttu-id="3a3bc-117">Autorisations</span><span class="sxs-lookup"><span data-stu-id="3a3bc-117">Permissions</span></span>

<span data-ttu-id="3a3bc-118">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-118">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="3a3bc-119">Pour en savoir plus, notamment sur le choix des autorisations, [consultez La mise en place.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="3a3bc-119">To learn more, including how to choose permissions, see [Get started](apis-intro.md).</span></span>

| <span data-ttu-id="3a3bc-120">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="3a3bc-120">Permission type</span></span>                    | <span data-ttu-id="3a3bc-121">Autorisation</span><span class="sxs-lookup"><span data-stu-id="3a3bc-121">Permission</span></span>           | <span data-ttu-id="3a3bc-122">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="3a3bc-122">Permission display name</span></span>                   |
|------------------------------------|----------------------|-------------------------------------------|
| <span data-ttu-id="3a3bc-123">Application</span><span class="sxs-lookup"><span data-stu-id="3a3bc-123">Application</span></span>                        | <span data-ttu-id="3a3bc-124">Machine.LiveResponse</span><span class="sxs-lookup"><span data-stu-id="3a3bc-124">Machine.LiveResponse</span></span> | <span data-ttu-id="3a3bc-125">Exécuter une réponse en direct sur un ordinateur spécifique</span><span class="sxs-lookup"><span data-stu-id="3a3bc-125">Run live response on a specific machine</span></span> |
| <span data-ttu-id="3a3bc-126">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="3a3bc-126">Delegated (work or school account)</span></span> | <span data-ttu-id="3a3bc-127">Machine.LiveResponse</span><span class="sxs-lookup"><span data-stu-id="3a3bc-127">Machine.LiveResponse</span></span> | <span data-ttu-id="3a3bc-128">Exécuter une réponse en direct sur un ordinateur spécifique</span><span class="sxs-lookup"><span data-stu-id="3a3bc-128">Run live response on a specific machine</span></span> |

## <a name="http-request"></a><span data-ttu-id="3a3bc-129">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="3a3bc-129">HTTP request</span></span>

```HTTP
POST
https://api.securitycenter.microsoft.com/API/machines/{machine_id}/runliveresponse
```

## <a name="request-headers"></a><span data-ttu-id="3a3bc-130">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="3a3bc-130">Request headers</span></span>

| <span data-ttu-id="3a3bc-131">Nom</span><span class="sxs-lookup"><span data-stu-id="3a3bc-131">Name</span></span>      | <span data-ttu-id="3a3bc-132">Type</span><span class="sxs-lookup"><span data-stu-id="3a3bc-132">Type</span></span> | <span data-ttu-id="3a3bc-133">Description</span><span class="sxs-lookup"><span data-stu-id="3a3bc-133">Description</span></span>                 |
|---------------|----------|---------------------------------|
| <span data-ttu-id="3a3bc-134">Autorisation</span><span class="sxs-lookup"><span data-stu-id="3a3bc-134">Authorization</span></span> | <span data-ttu-id="3a3bc-135">String</span><span class="sxs-lookup"><span data-stu-id="3a3bc-135">String</span></span>   | <span data-ttu-id="3a3bc-136">Porteur\<token>\.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-136">Bearer\<token>\.</span></span> <span data-ttu-id="3a3bc-137">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-137">Required.</span></span>   |
| <span data-ttu-id="3a3bc-138">Content-Type</span><span class="sxs-lookup"><span data-stu-id="3a3bc-138">Content-Type</span></span>  | <span data-ttu-id="3a3bc-139">string</span><span class="sxs-lookup"><span data-stu-id="3a3bc-139">string</span></span>   | <span data-ttu-id="3a3bc-p104">application/json. Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-p104">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3a3bc-142">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="3a3bc-142">Request body</span></span>

| <span data-ttu-id="3a3bc-143">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a3bc-143">Parameter</span></span> | <span data-ttu-id="3a3bc-144">Type</span><span class="sxs-lookup"><span data-stu-id="3a3bc-144">Type</span></span> | <span data-ttu-id="3a3bc-145">Description</span><span class="sxs-lookup"><span data-stu-id="3a3bc-145">Description</span></span>                                                        |
|---------------|----------|------------------------------------------------------------------------|
| <span data-ttu-id="3a3bc-146">Commentaire</span><span class="sxs-lookup"><span data-stu-id="3a3bc-146">Comment</span></span>       | <span data-ttu-id="3a3bc-147">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3a3bc-147">String</span></span>   | <span data-ttu-id="3a3bc-148">Commentaire à associer à l’action.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-148">Comment to associate with the action.</span></span>                                 |
| <span data-ttu-id="3a3bc-149">Commandes</span><span class="sxs-lookup"><span data-stu-id="3a3bc-149">Commands</span></span>      | <span data-ttu-id="3a3bc-150">Tableau</span><span class="sxs-lookup"><span data-stu-id="3a3bc-150">Array</span></span>    | <span data-ttu-id="3a3bc-151">Commandes à exécuter.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-151">Commands to run.</span></span> <span data-ttu-id="3a3bc-152">Les valeurs autorisées sont PutFile, RunScript, GetFile.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-152">Allowed values are PutFile, RunScript, GetFile.</span></span> |

<span data-ttu-id="3a3bc-153">Commandes :</span><span class="sxs-lookup"><span data-stu-id="3a3bc-153">Commands:</span></span>

| <span data-ttu-id="3a3bc-154">Type de commande</span><span class="sxs-lookup"><span data-stu-id="3a3bc-154">Command Type</span></span> | <span data-ttu-id="3a3bc-155">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a3bc-155">Parameters</span></span>                                                                          | <span data-ttu-id="3a3bc-156">Description</span><span class="sxs-lookup"><span data-stu-id="3a3bc-156">Description</span></span>                                                                                                                      |
|------------------|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a3bc-157">PutFile</span><span class="sxs-lookup"><span data-stu-id="3a3bc-157">PutFile</span></span>      | <span data-ttu-id="3a3bc-158">Clé : FileName</span><span class="sxs-lookup"><span data-stu-id="3a3bc-158">Key: FileName</span></span>  <br><br>  <span data-ttu-id="3a3bc-159">Valeur : \<file name\></span><span class="sxs-lookup"><span data-stu-id="3a3bc-159">Value: \<file name\></span></span>                                                                          | <span data-ttu-id="3a3bc-160">Place un fichier de la bibliothèque sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-160">Puts a file from the library to the device.</span></span> <span data-ttu-id="3a3bc-161">Les fichiers sont enregistrés dans un dossier de travail et supprimés lorsque l’appareil redémarre par défaut.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-161">Files are saved in a working folder and are deleted when the device restarts by default.</span></span>
| <span data-ttu-id="3a3bc-162">RunScript</span><span class="sxs-lookup"><span data-stu-id="3a3bc-162">RunScript</span></span>    | <span data-ttu-id="3a3bc-163">Clé : ScriptName</span><span class="sxs-lookup"><span data-stu-id="3a3bc-163">Key: ScriptName</span></span><br><span data-ttu-id="3a3bc-164">Valeur : \<Script from library\></span><span class="sxs-lookup"><span data-stu-id="3a3bc-164">Value: \<Script from library\></span></span> <br><br> <span data-ttu-id="3a3bc-165">Clé : Args</span><span class="sxs-lookup"><span data-stu-id="3a3bc-165">Key: Args</span></span>  <br> <span data-ttu-id="3a3bc-166">Valeur : \<Script arguments\></span><span class="sxs-lookup"><span data-stu-id="3a3bc-166">Value: \<Script arguments\></span></span>                          | <span data-ttu-id="3a3bc-167">Exécute un script à partir de la bibliothèque sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-167">Runs a script from the library on a device.</span></span>    <br><br>  <span data-ttu-id="3a3bc-168">Le paramètre Args est transmis à votre script.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-168">The Args parameter is passed to your script.</span></span> <br><br> <span data-ttu-id="3a3bc-169">Délai d’délai au bout de 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-169">Timeouts after 10 minutes.</span></span>     
| <span data-ttu-id="3a3bc-170">GetFile</span><span class="sxs-lookup"><span data-stu-id="3a3bc-170">GetFile</span></span>      | <span data-ttu-id="3a3bc-171">Clé : Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3a3bc-171">Key: Path</span></span> <br> <span data-ttu-id="3a3bc-172">Valeur : \<File path\></span><span class="sxs-lookup"><span data-stu-id="3a3bc-172">Value: \<File path\></span></span>                                                        | <span data-ttu-id="3a3bc-173">Collecter un fichier à partir d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-173">Collect file from a device.</span></span> <span data-ttu-id="3a3bc-174">REMARQUE : les barre obliques inverses dans le chemin d’accès doivent être échappés.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-174">NOTE: Backslashes in path must be escaped.</span></span>                                                                      |

## <a name="response"></a><span data-ttu-id="3a3bc-175">Réponse</span><span class="sxs-lookup"><span data-stu-id="3a3bc-175">Response</span></span>

-   <span data-ttu-id="3a3bc-176">Si elle réussit, cette méthode renvoie 200, OK.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-176">If successful, this method returns 200, Ok.</span></span>
    <span data-ttu-id="3a3bc-177">Entité Action.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-177">Action entity.</span></span> <span data-ttu-id="3a3bc-178">Si l’ordinateur avec l’ID spécifié est in trouvé - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-178">If machine with the specified ID was not found - 404 Not Found.</span></span>

## <a name="example"></a><span data-ttu-id="3a3bc-179">Exemple</span><span class="sxs-lookup"><span data-stu-id="3a3bc-179">Example</span></span>

<span data-ttu-id="3a3bc-180">**Demande**</span><span class="sxs-lookup"><span data-stu-id="3a3bc-180">**Request**</span></span>

<span data-ttu-id="3a3bc-181">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-181">Here is an example of the request.</span></span>

```HTTP

POST
https://api.securitycenter.microsoft.com/api/machines/1e5bc9d7e413ddd7902c2932e418702b84d0cc07/runliveresponse

```
<span data-ttu-id="3a3bc-182">**JSON**</span><span class="sxs-lookup"><span data-stu-id="3a3bc-182">**JSON**</span></span>

```JSON
{
   "Commands":[
      {
         "type":"RunScript",
         "params":[
            {
               "key":"ScriptName",
               "value":"minidump.ps1"
            },
            {
               "key":"Args",
               "value":"OfficeClickToRun"
            }

         ]
      },
      {
         "type":"GetFile",
         "params":[
            {
               "key":"Path",
               "value":"C:\\windows\\TEMP\\OfficeClickToRun.dmp.zip"
            }
         ]
      }
   ],
   "Comment":"Testing Live Response API"
}
```

<span data-ttu-id="3a3bc-183">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="3a3bc-183">**Response**</span></span>

<span data-ttu-id="3a3bc-184">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-184">Here is an example of the response.</span></span>

```HTTP
HTTP/1.1 200 Ok
```

<span data-ttu-id="3a3bc-185">Content-type: application/json</span><span class="sxs-lookup"><span data-stu-id="3a3bc-185">Content-type: application/json</span></span>

```JSON
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#MachineActions/$entity",
    "id": "{machine_action_id}",
    "type": "LiveResponse",
    "requestor": "analyst@microsoft.com",
    "requestorComment": "Testing Live Response API",
    "status": "Pending",
    "machineId": "{machine_id}",
    "computerDnsName": "hostname",
    "creationDateTimeUtc": "2021-02-04T15:36:52.7788848Z",
    "lastUpdateDateTimeUtc": "2021-02-04T15:36:52.7788848Z",
    "errorHResult": 0,
    "commands": [
        {
            "index": 0,
            "startTime": null,
            "endTime": null,
            "commandStatus": "Created",
            "errors": [],
            "command": {
                "type": "RunScript",
                "params": [
                    {
                        "key": "ScriptName",
                        "value": "minidump.ps1"
                    },{
                        "key": "Args",
                        "value": "OfficeClickToRun"
                    }
                ]
            }
        }, {
            "index": 1,
            "startTime": null,
            "endTime": null,
            "commandStatus": "Created",
            "errors": [],
            "command": {
                "type": "GetFile",
                "params": [{
                        "key": "Path", "value": "C:\\windows\\TEMP\\OfficeClickToRun.dmp.zip"
                    }
                ]
            }
        }
    ]
}


```

## <a name="related-topics"></a><span data-ttu-id="3a3bc-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a3bc-186">Related topics</span></span>
- [<span data-ttu-id="3a3bc-187">API Obtenir l’action de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="3a3bc-187">Get machine action API</span></span>](get-machineaction-object.md)
- [<span data-ttu-id="3a3bc-188">Obtenir un résultat de réponse en direct</span><span class="sxs-lookup"><span data-stu-id="3a3bc-188">Get live response result</span></span>](get-live-response-result.md)
- [<span data-ttu-id="3a3bc-189">Annuler l’action de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="3a3bc-189">Cancel machine action</span></span>](cancel-machine-action.md)
