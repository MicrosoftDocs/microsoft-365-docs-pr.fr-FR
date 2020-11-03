---
title: API de chasse avancée
description: Découvrez comment exécuter des requêtes de chasse avancées à l’aide de l’API Microsoft 365 Defender
keywords: Chasse avancée, API, API, MTP
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: c43d263009578af6280ffdc780ab0f9a174a3b97
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48844031"
---
# <a name="advanced-hunting-apis"></a><span data-ttu-id="6f3d6-104">API de chasse avancée</span><span class="sxs-lookup"><span data-stu-id="6f3d6-104">Advanced hunting APIs</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="6f3d6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6f3d6-105">**Applies to:**</span></span>
- <span data-ttu-id="6f3d6-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6f3d6-106">Microsoft 365 Defender</span></span>

>[!IMPORTANT] 
><span data-ttu-id="6f3d6-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6f3d6-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

## <a name="limitations"></a><span data-ttu-id="6f3d6-109">Limites</span><span class="sxs-lookup"><span data-stu-id="6f3d6-109">Limitations</span></span>
1. <span data-ttu-id="6f3d6-110">Vous pouvez uniquement exécuter une requête sur les données des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-110">You can only run a query on data from the last 30 days.</span></span>
2. <span data-ttu-id="6f3d6-111">Les résultats incluent un maximum de 100 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-111">The results will include a maximum of 100,000 rows.</span></span>
3. <span data-ttu-id="6f3d6-112">Le nombre d’exécutions est limité par client : jusqu’à 10 appels par minute, 10 minutes d’exécution toutes les heures et 4 heures de l’exécution quotidienne.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-112">The number of executions is limited per tenant: up to 10 calls per minute, 10 minutes of running time every hour and 4 hours of running time a day.</span></span>
4. <span data-ttu-id="6f3d6-113">Le temps d’exécution maximal d’une demande unique est de 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-113">The maximal execution time of a single request is 10 minutes.</span></span>
5. <span data-ttu-id="6f3d6-114">429 réponse représente la limite de quota atteinte en nombre de demandes ou par UC.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-114">429 response will represent reaching quota limit either by number of requests or by CPU.</span></span> <span data-ttu-id="6f3d6-115">Le corps de la réponse 429 indique également le moment où le quota est renouvelé.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-115">The 429 response body will also indicate the time until the quota is renewed.</span></span> 


## <a name="permissions"></a><span data-ttu-id="6f3d6-116">Autorisations</span><span class="sxs-lookup"><span data-stu-id="6f3d6-116">Permissions</span></span>
<span data-ttu-id="6f3d6-117">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-117">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="6f3d6-118">Pour plus d’informations, notamment sur la façon de choisir des autorisations, consultez [la rubrique Access the Microsoft 365 Defender API](api-access.md)</span><span class="sxs-lookup"><span data-stu-id="6f3d6-118">To learn more, including how to choose permissions, see [Access the Microsoft 365 Defender APIs](api-access.md)</span></span>

<span data-ttu-id="6f3d6-119">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="6f3d6-119">Permission type</span></span> |   <span data-ttu-id="6f3d6-120">Autorisation</span><span class="sxs-lookup"><span data-stu-id="6f3d6-120">Permission</span></span>  |   <span data-ttu-id="6f3d6-121">Nom d’affichage des autorisations</span><span class="sxs-lookup"><span data-stu-id="6f3d6-121">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="6f3d6-122">Application</span><span class="sxs-lookup"><span data-stu-id="6f3d6-122">Application</span></span> |   <span data-ttu-id="6f3d6-123">AdvancedHunting. Read. All</span><span class="sxs-lookup"><span data-stu-id="6f3d6-123">AdvancedHunting.Read.All</span></span> |  <span data-ttu-id="6f3d6-124">« Exécuter des requêtes avancées »</span><span class="sxs-lookup"><span data-stu-id="6f3d6-124">'Run advanced queries'</span></span>
<span data-ttu-id="6f3d6-125">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="6f3d6-125">Delegated (work or school account)</span></span> | <span data-ttu-id="6f3d6-126">AdvancedHunting. Read</span><span class="sxs-lookup"><span data-stu-id="6f3d6-126">AdvancedHunting.Read</span></span> | <span data-ttu-id="6f3d6-127">« Exécuter des requêtes avancées »</span><span class="sxs-lookup"><span data-stu-id="6f3d6-127">'Run advanced queries'</span></span>

>[!Note]
> <span data-ttu-id="6f3d6-128">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="6f3d6-128">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="6f3d6-129">L’utilisateur doit disposer du rôle AD « afficher les données »</span><span class="sxs-lookup"><span data-stu-id="6f3d6-129">The user needs to have 'View Data' AD role</span></span>
>- <span data-ttu-id="6f3d6-130">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres du groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-130">The user needs to have access to the device, based on device group settings.</span></span>

## <a name="http-request"></a><span data-ttu-id="6f3d6-131">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="6f3d6-131">HTTP request</span></span>
```
POST https://api.security.microsoft.com/api/advancedhunting/run
```

## <a name="request-headers"></a><span data-ttu-id="6f3d6-132">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="6f3d6-132">Request headers</span></span>

<span data-ttu-id="6f3d6-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f3d6-133">Header</span></span> | <span data-ttu-id="6f3d6-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f3d6-134">Value</span></span> 
:---|:---
<span data-ttu-id="6f3d6-135">Autorisation</span><span class="sxs-lookup"><span data-stu-id="6f3d6-135">Authorization</span></span> | <span data-ttu-id="6f3d6-136">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-136">Bearer {token}.</span></span> <span data-ttu-id="6f3d6-137">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-137">**Required**.</span></span>
<span data-ttu-id="6f3d6-138">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6f3d6-138">Content-Type</span></span>    | <span data-ttu-id="6f3d6-139">application/json</span><span class="sxs-lookup"><span data-stu-id="6f3d6-139">application/json</span></span>

## <a name="request-body"></a><span data-ttu-id="6f3d6-140">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="6f3d6-140">Request body</span></span>
<span data-ttu-id="6f3d6-141">Dans le corps de la demande, fournissez un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="6f3d6-141">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="6f3d6-142">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f3d6-142">Parameter</span></span> | <span data-ttu-id="6f3d6-143">Type</span><span class="sxs-lookup"><span data-stu-id="6f3d6-143">Type</span></span>    | <span data-ttu-id="6f3d6-144">Description</span><span class="sxs-lookup"><span data-stu-id="6f3d6-144">Description</span></span>
:---|:---|:---
<span data-ttu-id="6f3d6-145">Requête</span><span class="sxs-lookup"><span data-stu-id="6f3d6-145">Query</span></span> | <span data-ttu-id="6f3d6-146">Texte</span><span class="sxs-lookup"><span data-stu-id="6f3d6-146">Text</span></span> |  <span data-ttu-id="6f3d6-147">Requête à exécuter.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-147">The query to run.</span></span> <span data-ttu-id="6f3d6-148">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-148">**Required**.</span></span>

## <a name="response"></a><span data-ttu-id="6f3d6-149">Réponse</span><span class="sxs-lookup"><span data-stu-id="6f3d6-149">Response</span></span>
<span data-ttu-id="6f3d6-150">Si elle réussit, cette méthode renvoie 200 OK et l’objet _QueryResponse_ dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-150">If successful, this method returns 200 OK, and _QueryResponse_ object in the response body.</span></span> <br><br>

<span data-ttu-id="6f3d6-151">L’objet Response est divisé en trois parties (propriétés) :</span><span class="sxs-lookup"><span data-stu-id="6f3d6-151">The response object is divided to 3 parts (properties):</span></span><br>
1) <span data-ttu-id="6f3d6-152">```Stats``` -Statistiques de performances des requêtes.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-152">```Stats``` - Query performance statistics.</span></span><br>
2) <span data-ttu-id="6f3d6-153">```Schema``` -Le schéma de la réponse, une liste de paires de Name-Type pour chaque colonne.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-153">```Schema``` - The schema of the response, a list of Name-Type pairs for each column.</span></span> <br>
3) <span data-ttu-id="6f3d6-154">```Results``` -Une liste d’événements de chasse avancés.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-154">```Results``` - A list of Advanced Hunting events.</span></span>

## <a name="example"></a><span data-ttu-id="6f3d6-155">Exemple</span><span class="sxs-lookup"><span data-stu-id="6f3d6-155">Example</span></span>

<span data-ttu-id="6f3d6-156">Demande</span><span class="sxs-lookup"><span data-stu-id="6f3d6-156">Request</span></span>

<span data-ttu-id="6f3d6-157">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-157">Here is an example of the request.</span></span>


```json
{
    "Query":"DeviceProcessEvents | where InitiatingProcessFileName =~ \"powershell.exe\" | project Timestamp, FileName, InitiatingProcessFileName | order by Timestamp desc | limit 2"
}

```

<span data-ttu-id="6f3d6-158">Réponse</span><span class="sxs-lookup"><span data-stu-id="6f3d6-158">Response</span></span>

<span data-ttu-id="6f3d6-159">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-159">Here is an example of the response.</span></span>


```json
{
    "Stats": {
        "ExecutionTime": 4.621215,
        "resource_usage": {
            "cache": {
                "memory": {
                    "hits": 773461,
                    "misses": 4481,
                    "total": 777942
                },
                "disk": {
                    "hits": 994,
                    "misses": 197,
                    "total": 1191
                }
            },
            "cpu": {
                "user": "00:00:19.0468750",
                "kernel": "00:00:00.0156250",
                "total cpu": "00:00:19.0625000"
            },
            "memory": {
                "peak_per_node": 236822432
            }
        },
        "dataset_statistics": [
            {
                "table_row_count": 2,
                "table_size": 102
            }
        ]
    },
    "Schema": [
        {
            "Name": "Timestamp",
            "Type": "DateTime"
        },
        {
            "Name": "FileName",
            "Type": "String"
        },
        {
            "Name": "InitiatingProcessFileName",
            "Type": "String"
        }
    ],
    "Results": [
        {
            "Timestamp": "2020-08-30T06:38:35.7664356Z",
            "FileName": "conhost.exe",
            "InitiatingProcessFileName": "powershell.exe"
        },
        {
            "Timestamp": "2020-08-30T06:38:30.5163363Z",
            "FileName": "conhost.exe",
            "InitiatingProcessFileName": "powershell.exe"
        }
    ]
}

```

## <a name="related-topic"></a><span data-ttu-id="6f3d6-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f3d6-160">Related topic</span></span>
- [<span data-ttu-id="6f3d6-161">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6f3d6-161">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
