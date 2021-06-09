---
title: API d’alertes de liste
description: Découvrez comment utiliser l’API d’alertes de liste pour récupérer une collection d’alertes dans Microsoft Defender for Endpoint.
keywords: api, api de graphique, api pris en charge, obtenir, alertes, récent
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
ms.openlocfilehash: 4da646a52392871cde99271a17ed6eb9111f51ab
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52769242"
---
# <a name="list-alerts-api"></a><span data-ttu-id="990d6-104">API d’alertes de liste</span><span class="sxs-lookup"><span data-stu-id="990d6-104">List alerts API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="990d6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="990d6-105">**Applies to:**</span></span>
- [<span data-ttu-id="990d6-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="990d6-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="990d6-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="990d6-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="990d6-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="990d6-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="990d6-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="990d6-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 


[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="990d6-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="990d6-110">API description</span></span>
<span data-ttu-id="990d6-111">Récupère une collection d’alertes.</span><span class="sxs-lookup"><span data-stu-id="990d6-111">Retrieves a collection of Alerts.</span></span>
<br><span data-ttu-id="990d6-112">Prend [en charge les requêtes OData V4.](https://www.odata.org/documentation/)</span><span class="sxs-lookup"><span data-stu-id="990d6-112">Supports [OData V4 queries](https://www.odata.org/documentation/).</span></span>
<br><span data-ttu-id="990d6-113">Opérateurs pris en charge par OData :</span><span class="sxs-lookup"><span data-stu-id="990d6-113">OData supported operators:</span></span>
<br><span data-ttu-id="990d6-114">```$filter``` on: ```alertCreationTime``` , , , , , and ```lastUpdateTime``` ```incidentId``` ```InvestigationId``` ```status``` ```severity``` ```category``` properties.</span><span class="sxs-lookup"><span data-stu-id="990d6-114">```$filter``` on: ```alertCreationTime```, ```lastUpdateTime```, ```incidentId```,```InvestigationId```, ```status```, ```severity``` and ```category``` properties.</span></span>
<br><span data-ttu-id="990d6-115">```$top``` avec une valeur maximale de 10 000</span><span class="sxs-lookup"><span data-stu-id="990d6-115">```$top``` with max value of 10,000</span></span>
<br>```$skip```
<br><span data-ttu-id="990d6-116">```$expand``` of ```evidence```</span><span class="sxs-lookup"><span data-stu-id="990d6-116">```$expand``` of ```evidence```</span></span>
<br><span data-ttu-id="990d6-117">Voir des exemples [dans les requêtes OData avec Microsoft Defender for Endpoint](exposed-apis-odata-samples.md)</span><span class="sxs-lookup"><span data-stu-id="990d6-117">See examples at [OData queries with Microsoft Defender for Endpoint](exposed-apis-odata-samples.md)</span></span>


## <a name="limitations"></a><span data-ttu-id="990d6-118">Limites</span><span class="sxs-lookup"><span data-stu-id="990d6-118">Limitations</span></span>
1. <span data-ttu-id="990d6-119">Vous pouvez obtenir la dernière mise à jour des alertes en fonction de votre période de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="990d6-119">You can get alerts last updated according to your configured retention period.</span></span>
2. <span data-ttu-id="990d6-120">La taille maximale de page est de 10 000.</span><span class="sxs-lookup"><span data-stu-id="990d6-120">Maximum page size is 10,000.</span></span>
3. <span data-ttu-id="990d6-121">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="990d6-121">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span> 


## <a name="permissions"></a><span data-ttu-id="990d6-122">Autorisations</span><span class="sxs-lookup"><span data-stu-id="990d6-122">Permissions</span></span>
<span data-ttu-id="990d6-123">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="990d6-123">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="990d6-124">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="990d6-124">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="990d6-125">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="990d6-125">Permission type</span></span> |   <span data-ttu-id="990d6-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="990d6-126">Permission</span></span>  |   <span data-ttu-id="990d6-127">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="990d6-127">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="990d6-128">Application</span><span class="sxs-lookup"><span data-stu-id="990d6-128">Application</span></span> |   <span data-ttu-id="990d6-129">Alert.Read.All</span><span class="sxs-lookup"><span data-stu-id="990d6-129">Alert.Read.All</span></span> |    <span data-ttu-id="990d6-130">« Lire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="990d6-130">'Read all alerts'</span></span>
<span data-ttu-id="990d6-131">Application</span><span class="sxs-lookup"><span data-stu-id="990d6-131">Application</span></span> |   <span data-ttu-id="990d6-132">Alert.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="990d6-132">Alert.ReadWrite.All</span></span> |   <span data-ttu-id="990d6-133">« Lire et écrire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="990d6-133">'Read and write all alerts'</span></span>
<span data-ttu-id="990d6-134">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="990d6-134">Delegated (work or school account)</span></span> | <span data-ttu-id="990d6-135">Alert.Read</span><span class="sxs-lookup"><span data-stu-id="990d6-135">Alert.Read</span></span> | <span data-ttu-id="990d6-136">« Lire les alertes »</span><span class="sxs-lookup"><span data-stu-id="990d6-136">'Read alerts'</span></span>
<span data-ttu-id="990d6-137">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="990d6-137">Delegated (work or school account)</span></span> | <span data-ttu-id="990d6-138">Alert.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="990d6-138">Alert.ReadWrite</span></span> | <span data-ttu-id="990d6-139">« Lire et écrire des alertes »</span><span class="sxs-lookup"><span data-stu-id="990d6-139">'Read and write alerts'</span></span>

>[!Note]
> <span data-ttu-id="990d6-140">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="990d6-140">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="990d6-141">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="990d6-141">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="990d6-142">La réponse inclut uniquement les alertes associées aux appareils accessibles par [](machine-groups.md) l’utilisateur, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="990d6-142">The response will include only alerts that are associated with devices that the user can access, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="990d6-143">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="990d6-143">HTTP request</span></span>
```
GET /api/alerts
```

## <a name="request-headers"></a><span data-ttu-id="990d6-144">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="990d6-144">Request headers</span></span>

<span data-ttu-id="990d6-145">Nom</span><span class="sxs-lookup"><span data-stu-id="990d6-145">Name</span></span> | <span data-ttu-id="990d6-146">Type</span><span class="sxs-lookup"><span data-stu-id="990d6-146">Type</span></span> | <span data-ttu-id="990d6-147">Description</span><span class="sxs-lookup"><span data-stu-id="990d6-147">Description</span></span>
:---|:---|:---
<span data-ttu-id="990d6-148">Autorisation</span><span class="sxs-lookup"><span data-stu-id="990d6-148">Authorization</span></span> | <span data-ttu-id="990d6-149">String</span><span class="sxs-lookup"><span data-stu-id="990d6-149">String</span></span> | <span data-ttu-id="990d6-150">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="990d6-150">Bearer {token}.</span></span> <span data-ttu-id="990d6-151">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="990d6-151">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="990d6-152">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="990d6-152">Request body</span></span>
<span data-ttu-id="990d6-153">Vide</span><span class="sxs-lookup"><span data-stu-id="990d6-153">Empty</span></span>

## <a name="response"></a><span data-ttu-id="990d6-154">Réponse</span><span class="sxs-lookup"><span data-stu-id="990d6-154">Response</span></span>
<span data-ttu-id="990d6-155">Si elle réussit, cette méthode renvoie 200 OK et une liste d’objets d’alerte dans le corps de la réponse. [](alerts.md)</span><span class="sxs-lookup"><span data-stu-id="990d6-155">If successful, this method returns 200 OK, and a list of [alert](alerts.md) objects in the response body.</span></span>


## <a name="example-1---default"></a><span data-ttu-id="990d6-156">Exemple 1 - Par défaut</span><span class="sxs-lookup"><span data-stu-id="990d6-156">Example 1 - Default</span></span>

<span data-ttu-id="990d6-157">**Demande**</span><span class="sxs-lookup"><span data-stu-id="990d6-157">**Request**</span></span>

<span data-ttu-id="990d6-158">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="990d6-158">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/alerts
```

<span data-ttu-id="990d6-159">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="990d6-159">**Response**</span></span>

<span data-ttu-id="990d6-160">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="990d6-160">Here is an example of the response.</span></span>

>[!NOTE]
><span data-ttu-id="990d6-161">La liste de réponses présentée ici peut être tronquée à des raisons de concision.</span><span class="sxs-lookup"><span data-stu-id="990d6-161">The response list shown here may be truncated for brevity.</span></span> <span data-ttu-id="990d6-162">Toutes les alertes sont renvoyées à partir d’un appel réel.</span><span class="sxs-lookup"><span data-stu-id="990d6-162">All alerts will be returned from an actual call.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Alerts",
    "value": [
        {
            "id": "da637308392288907382_-880718168",
            "incidentId": 7587,
            "investigationId": 723156,
            "assignedTo": "secop123@contoso.com",
            "severity": "Low",
            "status": "New",
            "classification": "TruePositive",
            "determination": null,
            "investigationState": "Queued",
            "detectionSource": "WindowsDefenderAv",
            "category": "SuspiciousActivity",
            "threatFamilyName": "Meterpreter",
            "title": "Suspicious 'Meterpreter' behavior was detected",
            "description": "Malware and unwanted software are undesirable applications that perform annoying, disruptive, or harmful actions on affected machines. Some of these undesirable applications can replicate and spread from one machine to another. Others are able to receive commands from remote attackers and perform activities associated with cyber attacks.\n\nA malware is considered active if it is found running on the machine or it already has persistence mechanisms in place. Active malware detections are assigned higher severity ratings.\n\nBecause this malware was active, take precautionary measures and check for residual signs of infection.",
            "alertCreationTime": "2020-07-20T10:53:48.7657932Z",
            "firstEventTime": "2020-07-20T10:52:17.6654369Z",
            "lastEventTime": "2020-07-20T10:52:18.1362905Z",
            "lastUpdateTime": "2020-07-20T10:53:50.19Z",
            "resolvedTime": null,
            "machineId": "12ee6dd8c833c8a052ea231ec1b19adaf497b625",
            "computerDnsName": "temp123.middleeast.corp.microsoft.com",
            "rbacGroupName": "MiddleEast",
            "aadTenantId": "a839b112-1253-6432-9bf6-94542403f21c",
            "threatName": null,
            "mitreTechniques": [
                "T1064",
                "T1085",
                "T1220"
            ],
            "relatedUser": {
                "userName": "temp123",
                "domainName": "MIDDLEEAST"
            },
            "comments": [
                {
                    "comment": "test comment for docs",
                    "createdBy": "secop123@contoso.com",
                    "createdTime": "2020-07-21T01:00:37.8404534Z"
                }
            ],
            "evidence": []
        }
        ...
    ]
}
```

## <a name="example-2---get-10-latest-alerts-with-related-evidence"></a><span data-ttu-id="990d6-163">Exemple 2 : obtenir 10 alertes les plus récentes avec des preuves associées</span><span class="sxs-lookup"><span data-stu-id="990d6-163">Example 2 - Get 10 latest Alerts with related Evidence</span></span>

<span data-ttu-id="990d6-164">**Demande**</span><span class="sxs-lookup"><span data-stu-id="990d6-164">**Request**</span></span>

<span data-ttu-id="990d6-165">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="990d6-165">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/alerts?$top=10&$expand=evidence
```


<span data-ttu-id="990d6-166">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="990d6-166">**Response**</span></span>

<span data-ttu-id="990d6-167">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="990d6-167">Here is an example of the response.</span></span>

>[!NOTE]
><span data-ttu-id="990d6-168">La liste de réponses présentée ici peut être tronquée à des raisons de concision.</span><span class="sxs-lookup"><span data-stu-id="990d6-168">The response list shown here may be truncated for brevity.</span></span> <span data-ttu-id="990d6-169">Toutes les alertes sont renvoyées à partir d’un appel réel.</span><span class="sxs-lookup"><span data-stu-id="990d6-169">All alerts will be returned from an actual call.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Alerts",
    "value": [
        {
            "id": "da637472900382838869_1364969609",
            "incidentId": 1126093,
            "investigationId": null,
            "assignedTo": null,
            "severity": "Low",
            "status": "New",
            "classification": null,
            "determination": null,
            "investigationState": "Queued",
            "detectionSource": "WindowsDefenderAtp",
            "detectorId": "17e10bbc-3a68-474a-8aad-faef14d43952",
            "category": "Execution",
            "threatFamilyName": null,
            "title": "Low-reputation arbitrary code executed by signed executable",
            "description": "Binaries signed by Microsoft can be used to run low-reputation arbitrary code. This technique hides the execution of malicious code within a trusted process. As a result, the trusted process might exhibit suspicious behaviors, such as opening a listening port or connecting to a command-and-control (C&C) server.",
            "alertCreationTime": "2021-01-26T20:33:57.7220239Z",
            "firstEventTime": "2021-01-26T20:31:32.9562661Z",
            "lastEventTime": "2021-01-26T20:31:33.0577322Z",
            "lastUpdateTime": "2021-01-26T20:33:59.2Z",
            "resolvedTime": null,
            "machineId": "111e6dd8c833c8a052ea231ec1b19adaf497b625",
            "computerDnsName": "temp123.middleeast.corp.microsoft.com",
            "rbacGroupName": "A",
            "aadTenantId": "a839b112-1253-6432-9bf6-94542403f21c",
            "threatName": null,
            "mitreTechniques": [
                "T1064",
                "T1085",
                "T1220"
            ],
            "relatedUser": {
                "userName": "temp123",
                "domainName": "MIDDLEEAST"
            },
            "comments": [
                {
                    "comment": "test comment for docs",
                    "createdBy": "secop123@contoso.com",
                    "createdTime": "2021-01-26T01:00:37.8404534Z"
                }
            ],
            "evidence": [
                {
                    "entityType": "User",
                    "evidenceCreationTime": "2021-01-26T20:33:58.42Z",
                    "sha1": null,
                    "sha256": null,
                    "fileName": null,
                    "filePath": null,
                    "processId": null,
                    "processCommandLine": null,
                    "processCreationTime": null,
                    "parentProcessId": null,
                    "parentProcessCreationTime": null,
                    "parentProcessFileName": null,
                    "parentProcessFilePath": null,
                    "ipAddress": null,
                    "url": null,
                    "registryKey": null,
                    "registryHive": null,
                    "registryValueType": null,
                    "registryValue": null,
                    "accountName": "eranb",
                    "domainName": "MIDDLEEAST",
                    "userSid": "S-1-5-21-11111607-1111760036-109187956-75141",
                    "aadUserId": "11118379-2a59-1111-ac3c-a51eb4a3c627",
                    "userPrincipalName": "temp123@microsoft.com",
                    "detectionStatus": null
                },
                {
                    "entityType": "Process",
                    "evidenceCreationTime": "2021-01-26T20:33:58.6133333Z",
                    "sha1": "ff836cfb1af40252bd2a2ea843032e99a5b262ed",
                    "sha256": "a4752c71d81afd3d5865d24ddb11a6b0c615062fcc448d24050c2172d2cbccd6",
                    "fileName": "rundll32.exe",
                    "filePath": "C:\\Windows\\SysWOW64",
                    "processId": 3276,
                    "processCommandLine": "rundll32.exe  c:\\temp\\suspicious.dll,RepeatAfterMe",
                    "processCreationTime": "2021-01-26T20:31:32.9581596Z",
                    "parentProcessId": 8420,
                    "parentProcessCreationTime": "2021-01-26T20:31:32.9004163Z",
                    "parentProcessFileName": "rundll32.exe",
                    "parentProcessFilePath": "C:\\Windows\\System32",
                    "ipAddress": null,
                    "url": null,
                    "registryKey": null,
                    "registryHive": null,
                    "registryValueType": null,
                    "registryValue": null,
                    "accountName": null,
                    "domainName": null,
                    "userSid": null,
                    "aadUserId": null,
                    "userPrincipalName": null,
                    "detectionStatus": "Detected"
                },
                {
                    "entityType": "File",
                    "evidenceCreationTime": "2021-01-26T20:33:58.42Z",
                    "sha1": "8563f95b2f8a284fc99da44500cd51a77c1ff36c",
                    "sha256": "dc0ade0c95d6db98882bc8fa6707e64353cd6f7767ff48d6a81a6c2aef21c608",
                    "fileName": "suspicious.dll",
                    "filePath": "c:\\temp",
                    "processId": null,
                    "processCommandLine": null,
                    "processCreationTime": null,
                    "parentProcessId": null,
                    "parentProcessCreationTime": null,
                    "parentProcessFileName": null,
                    "parentProcessFilePath": null,
                    "ipAddress": null,
                    "url": null,
                    "registryKey": null,
                    "registryHive": null,
                    "registryValueType": null,
                    "registryValue": null,
                    "accountName": null,
                    "domainName": null,
                    "userSid": null,
                    "aadUserId": null,
                    "userPrincipalName": null,
                    "detectionStatus": "Detected"
                }
            ]
        },
        ...
    ]
}
```


## <a name="see-also"></a><span data-ttu-id="990d6-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="990d6-170">See also</span></span>
- [<span data-ttu-id="990d6-171">Requêtes OData avec Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="990d6-171">OData queries with Microsoft Defender for Endpoint</span></span>](exposed-apis-odata-samples.md)
