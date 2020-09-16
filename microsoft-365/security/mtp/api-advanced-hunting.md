---
title: API de chasse avancée
description: Découvrez comment exécuter des requêtes de chasse avancées à l’aide de l’API Microsoft Threat Protection
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
ms.openlocfilehash: 9e92a0328d2e7fb9cfe7461241dd866081926876
ms.sourcegitcommit: 62a8c226422eac9c085cc886b4836b037f95ef6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2020
ms.locfileid: "47825373"
---
# <a name="advanced-hunting-apis"></a><span data-ttu-id="df54b-104">API de chasse avancée</span><span class="sxs-lookup"><span data-stu-id="df54b-104">Advanced hunting APIs</span></span>

<span data-ttu-id="df54b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="df54b-105">**Applies to:**</span></span>
- <span data-ttu-id="df54b-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="df54b-106">Microsoft Threat Protection</span></span>

>[!IMPORTANT] 
><span data-ttu-id="df54b-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="df54b-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="df54b-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="df54b-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

## <a name="limitations"></a><span data-ttu-id="df54b-109">Limites</span><span class="sxs-lookup"><span data-stu-id="df54b-109">Limitations</span></span>
1. <span data-ttu-id="df54b-110">Vous pouvez uniquement exécuter une requête sur les données des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="df54b-110">You can only run a query on data from the last 30 days.</span></span>
2. <span data-ttu-id="df54b-111">Les résultats incluent un maximum de 100 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="df54b-111">The results will include a maximum of 100,000 rows.</span></span>
3. <span data-ttu-id="df54b-112">Le nombre d’exécutions est limité par client : jusqu’à 10 appels par minute, 10 minutes d’exécution toutes les heures et 4 heures de l’exécution quotidienne.</span><span class="sxs-lookup"><span data-stu-id="df54b-112">The number of executions is limited per tenant: up to 10 calls per minute, 10 minutes of running time every hour and 4 hours of running time a day.</span></span>
4. <span data-ttu-id="df54b-113">Le temps d’exécution maximal d’une demande unique est de 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="df54b-113">The maximal execution time of a single request is 10 minutes.</span></span>
5. <span data-ttu-id="df54b-114">429 réponse représente la limite de quota atteinte en nombre de demandes ou par UC.</span><span class="sxs-lookup"><span data-stu-id="df54b-114">429 response will represent reaching quota limit either by number of requests or by CPU.</span></span> <span data-ttu-id="df54b-115">Le corps de la réponse 429 indique également le moment où le quota est renouvelé.</span><span class="sxs-lookup"><span data-stu-id="df54b-115">The 429 response body will also indicate the time until the quota is renewed.</span></span> 


## <a name="permissions"></a><span data-ttu-id="df54b-116">Autorisations</span><span class="sxs-lookup"><span data-stu-id="df54b-116">Permissions</span></span>
<span data-ttu-id="df54b-117">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="df54b-117">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="df54b-118">Pour plus d’informations, notamment sur la façon de choisir des autorisations, consultez [la rubrique Access the Microsoft Threat Protection APIs](api-access.md)</span><span class="sxs-lookup"><span data-stu-id="df54b-118">To learn more, including how to choose permissions, see [Access the Microsoft Threat Protection APIs](api-access.md)</span></span>

<span data-ttu-id="df54b-119">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="df54b-119">Permission type</span></span> |   <span data-ttu-id="df54b-120">Autorisation</span><span class="sxs-lookup"><span data-stu-id="df54b-120">Permission</span></span>  |   <span data-ttu-id="df54b-121">Nom d’affichage des autorisations</span><span class="sxs-lookup"><span data-stu-id="df54b-121">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="df54b-122">Application</span><span class="sxs-lookup"><span data-stu-id="df54b-122">Application</span></span> |   <span data-ttu-id="df54b-123">AdvancedHunting. Read. All</span><span class="sxs-lookup"><span data-stu-id="df54b-123">AdvancedHunting.Read.All</span></span> |  <span data-ttu-id="df54b-124">« Exécuter des requêtes avancées »</span><span class="sxs-lookup"><span data-stu-id="df54b-124">'Run advanced queries'</span></span>
<span data-ttu-id="df54b-125">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="df54b-125">Delegated (work or school account)</span></span> | <span data-ttu-id="df54b-126">AdvancedHunting. Read</span><span class="sxs-lookup"><span data-stu-id="df54b-126">AdvancedHunting.Read</span></span> | <span data-ttu-id="df54b-127">« Exécuter des requêtes avancées »</span><span class="sxs-lookup"><span data-stu-id="df54b-127">'Run advanced queries'</span></span>

>[!Note]
> <span data-ttu-id="df54b-128">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="df54b-128">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="df54b-129">L’utilisateur doit disposer du rôle AD « afficher les données »</span><span class="sxs-lookup"><span data-stu-id="df54b-129">The user needs to have 'View Data' AD role</span></span>
>- <span data-ttu-id="df54b-130">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres du groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="df54b-130">The user needs to have access to the device, based on device group settings.</span></span>

## <a name="http-request"></a><span data-ttu-id="df54b-131">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="df54b-131">HTTP request</span></span>
```
POST https://api.security.microsoft.com/api/advancedhunting/run
```

## <a name="request-headers"></a><span data-ttu-id="df54b-132">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="df54b-132">Request headers</span></span>

<span data-ttu-id="df54b-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="df54b-133">Header</span></span> | <span data-ttu-id="df54b-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="df54b-134">Value</span></span> 
:---|:---
<span data-ttu-id="df54b-135">Autorisation</span><span class="sxs-lookup"><span data-stu-id="df54b-135">Authorization</span></span> | <span data-ttu-id="df54b-136">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="df54b-136">Bearer {token}.</span></span> <span data-ttu-id="df54b-137">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="df54b-137">**Required**.</span></span>
<span data-ttu-id="df54b-138">Content-Type</span><span class="sxs-lookup"><span data-stu-id="df54b-138">Content-Type</span></span>    | <span data-ttu-id="df54b-139">application/json</span><span class="sxs-lookup"><span data-stu-id="df54b-139">application/json</span></span>

## <a name="request-body"></a><span data-ttu-id="df54b-140">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="df54b-140">Request body</span></span>
<span data-ttu-id="df54b-141">Dans le corps de la demande, fournissez un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="df54b-141">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="df54b-142">Paramètre</span><span class="sxs-lookup"><span data-stu-id="df54b-142">Parameter</span></span> | <span data-ttu-id="df54b-143">Type</span><span class="sxs-lookup"><span data-stu-id="df54b-143">Type</span></span>    | <span data-ttu-id="df54b-144">Description</span><span class="sxs-lookup"><span data-stu-id="df54b-144">Description</span></span>
:---|:---|:---
<span data-ttu-id="df54b-145">Requête</span><span class="sxs-lookup"><span data-stu-id="df54b-145">Query</span></span> | <span data-ttu-id="df54b-146">Texte</span><span class="sxs-lookup"><span data-stu-id="df54b-146">Text</span></span> |  <span data-ttu-id="df54b-147">Requête à exécuter.</span><span class="sxs-lookup"><span data-stu-id="df54b-147">The query to run.</span></span> <span data-ttu-id="df54b-148">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="df54b-148">**Required**.</span></span>

## <a name="response"></a><span data-ttu-id="df54b-149">Réponse</span><span class="sxs-lookup"><span data-stu-id="df54b-149">Response</span></span>
<span data-ttu-id="df54b-150">Si elle réussit, cette méthode renvoie 200 OK et l’objet _QueryResponse_ dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="df54b-150">If successful, this method returns 200 OK, and _QueryResponse_ object in the response body.</span></span> <br><br>

<span data-ttu-id="df54b-151">L’objet Response est divisé en trois parties (propriétés) :</span><span class="sxs-lookup"><span data-stu-id="df54b-151">The response object is divided to 3 parts (properties):</span></span><br>
1) <span data-ttu-id="df54b-152">```Stats``` -Statistiques de performances des requêtes.</span><span class="sxs-lookup"><span data-stu-id="df54b-152">```Stats``` - Query performance statistics.</span></span><br>
2) <span data-ttu-id="df54b-153">```Schema``` -Le schéma de la réponse, une liste de paires nom-type pour chaque colonne.</span><span class="sxs-lookup"><span data-stu-id="df54b-153">```Schema``` - The schema of the response, a list of Name-Type pairs for each column.</span></span> <br>
3) <span data-ttu-id="df54b-154">```Results``` -Une liste d’événements de chasse avancés.</span><span class="sxs-lookup"><span data-stu-id="df54b-154">```Results``` - A list of Advanced Hunting events.</span></span>

## <a name="example"></a><span data-ttu-id="df54b-155">Exemple</span><span class="sxs-lookup"><span data-stu-id="df54b-155">Example</span></span>

<span data-ttu-id="df54b-156">Demande</span><span class="sxs-lookup"><span data-stu-id="df54b-156">Request</span></span>

<span data-ttu-id="df54b-157">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="df54b-157">Here is an example of the request.</span></span>


```json
{
    "Query":"DeviceProcessEvents | where InitiatingProcessFileName =~ \"powershell.exe\" | project Timestamp, FileName, InitiatingProcessFileName | order by Timestamp desc | limit 2"
}

```

<span data-ttu-id="df54b-158">Réponse</span><span class="sxs-lookup"><span data-stu-id="df54b-158">Response</span></span>

<span data-ttu-id="df54b-159">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="df54b-159">Here is an example of the response.</span></span>


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

## <a name="related-topic"></a><span data-ttu-id="df54b-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df54b-160">Related topic</span></span>
- [<span data-ttu-id="df54b-161">Accéder aux API de protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="df54b-161">Access the Microsoft Threat Protection APIs</span></span>](api-access.md)
