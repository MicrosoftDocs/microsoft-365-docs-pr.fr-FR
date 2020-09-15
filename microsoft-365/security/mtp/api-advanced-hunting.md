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
ms.openlocfilehash: 92d5d2840963ae00ae0f03e3359f287371f770ee
ms.sourcegitcommit: 9a275a13af3e063e80ce1bd3cd8142a095db92d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2020
ms.locfileid: "47650300"
---
# <a name="advanced-hunting-apis"></a><span data-ttu-id="56707-104">API de chasse avancée</span><span class="sxs-lookup"><span data-stu-id="56707-104">Advanced hunting APIs</span></span>

<span data-ttu-id="56707-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="56707-105">**Applies to:**</span></span>
- <span data-ttu-id="56707-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="56707-106">Microsoft Threat Protection</span></span>

>[!IMPORTANT] 
><span data-ttu-id="56707-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="56707-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="56707-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="56707-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

## <a name="limitations"></a><span data-ttu-id="56707-109">Limites</span><span class="sxs-lookup"><span data-stu-id="56707-109">Limitations</span></span>
1. <span data-ttu-id="56707-110">Vous pouvez uniquement exécuter une requête sur les données des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="56707-110">You can only run a query on data from the last 30 days.</span></span>
2. <span data-ttu-id="56707-111">Les résultats incluent un maximum de 100 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="56707-111">The results will include a maximum of 100,000 rows.</span></span>
3. <span data-ttu-id="56707-112">Le nombre d’exécutions est limité par client : jusqu’à 15 appels par minute, 15 minutes d’exécution toutes les heures et 4 heures de temps d’exécution par jour.</span><span class="sxs-lookup"><span data-stu-id="56707-112">The number of executions is limited per tenant: up to 15 calls per minute, 15 minutes of running time every hour and 4 hours of running time a day.</span></span>
4. <span data-ttu-id="56707-113">Le temps d’exécution maximal d’une demande unique est de 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="56707-113">The maximal execution time of a single request is 10 minutes.</span></span>

## <a name="permissions"></a><span data-ttu-id="56707-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="56707-114">Permissions</span></span>
<span data-ttu-id="56707-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="56707-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="56707-116">Pour plus d’informations, notamment sur la façon de choisir des autorisations, consultez [la rubrique Access the Microsoft Threat Protection APIs](api-access.md)</span><span class="sxs-lookup"><span data-stu-id="56707-116">To learn more, including how to choose permissions, see [Access the Microsoft Threat Protection APIs](api-access.md)</span></span>

<span data-ttu-id="56707-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="56707-117">Permission type</span></span> |   <span data-ttu-id="56707-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="56707-118">Permission</span></span>  |   <span data-ttu-id="56707-119">Nom d’affichage des autorisations</span><span class="sxs-lookup"><span data-stu-id="56707-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="56707-120">Application</span><span class="sxs-lookup"><span data-stu-id="56707-120">Application</span></span> |   <span data-ttu-id="56707-121">AdvancedHunting. Read. All</span><span class="sxs-lookup"><span data-stu-id="56707-121">AdvancedHunting.Read.All</span></span> |  <span data-ttu-id="56707-122">« Exécuter des requêtes avancées »</span><span class="sxs-lookup"><span data-stu-id="56707-122">'Run advanced queries'</span></span>
<span data-ttu-id="56707-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="56707-123">Delegated (work or school account)</span></span> | <span data-ttu-id="56707-124">AdvancedHunting. Read</span><span class="sxs-lookup"><span data-stu-id="56707-124">AdvancedHunting.Read</span></span> | <span data-ttu-id="56707-125">« Exécuter des requêtes avancées »</span><span class="sxs-lookup"><span data-stu-id="56707-125">'Run advanced queries'</span></span>

>[!Note]
> <span data-ttu-id="56707-126">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="56707-126">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="56707-127">L’utilisateur doit disposer du rôle AD « afficher les données »</span><span class="sxs-lookup"><span data-stu-id="56707-127">The user needs to have 'View Data' AD role</span></span>
>- <span data-ttu-id="56707-128">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres du groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="56707-128">The user needs to have access to the device, based on device group settings.</span></span>

## <a name="http-request"></a><span data-ttu-id="56707-129">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="56707-129">HTTP request</span></span>
```
POST https://api.security.microsoft.com/api/advancedhunting/run
```

## <a name="request-headers"></a><span data-ttu-id="56707-130">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="56707-130">Request headers</span></span>

<span data-ttu-id="56707-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="56707-131">Header</span></span> | <span data-ttu-id="56707-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="56707-132">Value</span></span> 
:---|:---
<span data-ttu-id="56707-133">Autorisation</span><span class="sxs-lookup"><span data-stu-id="56707-133">Authorization</span></span> | <span data-ttu-id="56707-134">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="56707-134">Bearer {token}.</span></span> <span data-ttu-id="56707-135">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="56707-135">**Required**.</span></span>
<span data-ttu-id="56707-136">Content-Type</span><span class="sxs-lookup"><span data-stu-id="56707-136">Content-Type</span></span>    | <span data-ttu-id="56707-137">application/json</span><span class="sxs-lookup"><span data-stu-id="56707-137">application/json</span></span>

## <a name="request-body"></a><span data-ttu-id="56707-138">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="56707-138">Request body</span></span>
<span data-ttu-id="56707-139">Dans le corps de la demande, fournissez un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="56707-139">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="56707-140">Paramètre</span><span class="sxs-lookup"><span data-stu-id="56707-140">Parameter</span></span> | <span data-ttu-id="56707-141">Type</span><span class="sxs-lookup"><span data-stu-id="56707-141">Type</span></span>    | <span data-ttu-id="56707-142">Description</span><span class="sxs-lookup"><span data-stu-id="56707-142">Description</span></span>
:---|:---|:---
<span data-ttu-id="56707-143">Requête</span><span class="sxs-lookup"><span data-stu-id="56707-143">Query</span></span> | <span data-ttu-id="56707-144">Texte</span><span class="sxs-lookup"><span data-stu-id="56707-144">Text</span></span> |  <span data-ttu-id="56707-145">Requête à exécuter.</span><span class="sxs-lookup"><span data-stu-id="56707-145">The query to run.</span></span> <span data-ttu-id="56707-146">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="56707-146">**Required**.</span></span>

## <a name="response"></a><span data-ttu-id="56707-147">Réponse</span><span class="sxs-lookup"><span data-stu-id="56707-147">Response</span></span>
<span data-ttu-id="56707-148">Si elle réussit, cette méthode renvoie 200 OK et l’objet _QueryResponse_ dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="56707-148">If successful, this method returns 200 OK, and _QueryResponse_ object in the response body.</span></span> <br><br>

<span data-ttu-id="56707-149">L’objet Response est divisé en trois parties (propriétés) :</span><span class="sxs-lookup"><span data-stu-id="56707-149">The response object is divided to 3 parts (properties):</span></span><br>
1) <span data-ttu-id="56707-150">```Stats``` -Statistiques de performances des requêtes.</span><span class="sxs-lookup"><span data-stu-id="56707-150">```Stats``` - Query performance statistics.</span></span><br>
2) <span data-ttu-id="56707-151">```Schema``` -Le schéma de la réponse, une liste de paires nom-type pour chaque colonne.</span><span class="sxs-lookup"><span data-stu-id="56707-151">```Schema``` - The schema of the response, a list of Name-Type pairs for each column.</span></span> <br>
3) <span data-ttu-id="56707-152">```Results``` -Une liste d’événements de chasse avancés.</span><span class="sxs-lookup"><span data-stu-id="56707-152">```Results``` - A list of Advanced Hunting events.</span></span>

## <a name="example"></a><span data-ttu-id="56707-153">Exemple</span><span class="sxs-lookup"><span data-stu-id="56707-153">Example</span></span>

<span data-ttu-id="56707-154">Demande</span><span class="sxs-lookup"><span data-stu-id="56707-154">Request</span></span>

<span data-ttu-id="56707-155">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="56707-155">Here is an example of the request.</span></span>


```json
{
    "Query":"DeviceProcessEvents | where InitiatingProcessFileName =~ \"powershell.exe\" | project Timestamp, FileName, InitiatingProcessFileName | order by Timestamp desc | limit 2"
}

```

<span data-ttu-id="56707-156">Réponse</span><span class="sxs-lookup"><span data-stu-id="56707-156">Response</span></span>

<span data-ttu-id="56707-157">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="56707-157">Here is an example of the response.</span></span>


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

## <a name="related-topic"></a><span data-ttu-id="56707-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56707-158">Related topic</span></span>
- [<span data-ttu-id="56707-159">Accéder aux API de protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="56707-159">Access the Microsoft Threat Protection APIs</span></span>](api-access.md)
