---
title: API de recherche avancée de menaces
ms.reviewer: ''
description: Découvrez comment utiliser l’API de recherche avancée pour exécuter des requêtes avancées sur Microsoft Defender for Endpoint. Découvrez les limitations et consultez un exemple.
keywords: api, api pris en charge, recherche avancée, requête
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
ms.technology: mde
ms.openlocfilehash: 40487143ff18cedb76c9f3f33c52cab24687c282
ms.sourcegitcommit: dc1ac43a57fac6f57438859dd668f927d94fdf34
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2021
ms.locfileid: "51604368"
---
# <a name="advanced-hunting-api"></a><span data-ttu-id="10b54-105">API de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="10b54-105">Advanced hunting API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="10b54-106">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="10b54-106">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="10b54-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="10b54-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="10b54-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="10b54-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="limitations"></a><span data-ttu-id="10b54-109">Limites</span><span class="sxs-lookup"><span data-stu-id="10b54-109">Limitations</span></span>

1. <span data-ttu-id="10b54-110">Vous pouvez uniquement exécuter une requête sur les données des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="10b54-110">You can only run a query on data from the last 30 days.</span></span>

2. <span data-ttu-id="10b54-111">Les résultats incluent un maximum de 100 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="10b54-111">The results will include a maximum of 100,000 rows.</span></span>

3. <span data-ttu-id="10b54-112">Le nombre d’exécutions est limité par client :</span><span class="sxs-lookup"><span data-stu-id="10b54-112">The number of executions is limited per tenant:</span></span>
   - <span data-ttu-id="10b54-113">Appels d’API : jusqu’à 45 appels par minute, jusqu’à 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="10b54-113">API calls: Up to 45 calls per minute, up to 1500 calls per hour.</span></span>
   - <span data-ttu-id="10b54-114">Durée d’exécution : 10 minutes d’exécution toutes les heures et 3 heures d’exécution par jour.</span><span class="sxs-lookup"><span data-stu-id="10b54-114">Execution time: 10 minutes of running time every hour and 3 hours of running time a day.</span></span>

4. <span data-ttu-id="10b54-115">La durée d’exécution maximale d’une seule demande est de 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="10b54-115">The maximal execution time of a single request is 10 minutes.</span></span>

5. <span data-ttu-id="10b54-116">La réponse 429 représente l’atteinte de la limite de quota par nombre de demandes ou par processeur.</span><span class="sxs-lookup"><span data-stu-id="10b54-116">429 response will represent reaching quota limit either by number of requests or by CPU.</span></span> <span data-ttu-id="10b54-117">Lire le corps de la réponse pour comprendre quelle limite a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="10b54-117">Read response body to understand what limit has been reached.</span></span> 

## <a name="permissions"></a><span data-ttu-id="10b54-118">Autorisations</span><span class="sxs-lookup"><span data-stu-id="10b54-118">Permissions</span></span>

<span data-ttu-id="10b54-119">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="10b54-119">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="10b54-120">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="10b54-120">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="10b54-121">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="10b54-121">Permission type</span></span> |   <span data-ttu-id="10b54-122">Autorisation</span><span class="sxs-lookup"><span data-stu-id="10b54-122">Permission</span></span>  |   <span data-ttu-id="10b54-123">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="10b54-123">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="10b54-124">Application</span><span class="sxs-lookup"><span data-stu-id="10b54-124">Application</span></span> |   <span data-ttu-id="10b54-125">AdvancedQuery.Read.All</span><span class="sxs-lookup"><span data-stu-id="10b54-125">AdvancedQuery.Read.All</span></span> |    <span data-ttu-id="10b54-126">« Exécuter des requêtes avancées »</span><span class="sxs-lookup"><span data-stu-id="10b54-126">'Run advanced queries'</span></span>
<span data-ttu-id="10b54-127">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="10b54-127">Delegated (work or school account)</span></span> | <span data-ttu-id="10b54-128">AdvancedQuery.Read</span><span class="sxs-lookup"><span data-stu-id="10b54-128">AdvancedQuery.Read</span></span> | <span data-ttu-id="10b54-129">« Exécuter des requêtes avancées »</span><span class="sxs-lookup"><span data-stu-id="10b54-129">'Run advanced queries'</span></span>

>[!Note]
> <span data-ttu-id="10b54-130">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="10b54-130">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="10b54-131">L’utilisateur doit avoir le rôle AD « Afficher les données »</span><span class="sxs-lookup"><span data-stu-id="10b54-131">The user needs to have 'View Data' AD role</span></span>
>- <span data-ttu-id="10b54-132">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="10b54-132">The user needs to have access to the device, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="10b54-133">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="10b54-133">HTTP request</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/advancedqueries/run
```

## <a name="request-headers"></a><span data-ttu-id="10b54-134">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="10b54-134">Request headers</span></span>

<span data-ttu-id="10b54-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="10b54-135">Header</span></span> | <span data-ttu-id="10b54-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="10b54-136">Value</span></span> 
:---|:---
<span data-ttu-id="10b54-137">Autorisation</span><span class="sxs-lookup"><span data-stu-id="10b54-137">Authorization</span></span> | <span data-ttu-id="10b54-138">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="10b54-138">Bearer {token}.</span></span> <span data-ttu-id="10b54-139">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="10b54-139">**Required**.</span></span>
<span data-ttu-id="10b54-140">Content-Type</span><span class="sxs-lookup"><span data-stu-id="10b54-140">Content-Type</span></span>    | <span data-ttu-id="10b54-141">application/json</span><span class="sxs-lookup"><span data-stu-id="10b54-141">application/json</span></span>

## <a name="request-body"></a><span data-ttu-id="10b54-142">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="10b54-142">Request body</span></span>

<span data-ttu-id="10b54-143">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="10b54-143">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="10b54-144">Paramètre</span><span class="sxs-lookup"><span data-stu-id="10b54-144">Parameter</span></span> | <span data-ttu-id="10b54-145">Type</span><span class="sxs-lookup"><span data-stu-id="10b54-145">Type</span></span>    | <span data-ttu-id="10b54-146">Description</span><span class="sxs-lookup"><span data-stu-id="10b54-146">Description</span></span>
:---|:---|:---
<span data-ttu-id="10b54-147">Requête</span><span class="sxs-lookup"><span data-stu-id="10b54-147">Query</span></span> | <span data-ttu-id="10b54-148">Texte</span><span class="sxs-lookup"><span data-stu-id="10b54-148">Text</span></span> |  <span data-ttu-id="10b54-149">Requête à exécuter.</span><span class="sxs-lookup"><span data-stu-id="10b54-149">The query to run.</span></span> <span data-ttu-id="10b54-150">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="10b54-150">**Required**.</span></span>

## <a name="response"></a><span data-ttu-id="10b54-151">Réponse</span><span class="sxs-lookup"><span data-stu-id="10b54-151">Response</span></span>

<span data-ttu-id="10b54-152">Si elle réussit, cette méthode renvoie 200 OK et l’objet _QueryResponse_ dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="10b54-152">If successful, this method returns 200 OK, and _QueryResponse_ object in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="10b54-153">Exemple</span><span class="sxs-lookup"><span data-stu-id="10b54-153">Example</span></span>

##### <a name="request"></a><span data-ttu-id="10b54-154">Demande</span><span class="sxs-lookup"><span data-stu-id="10b54-154">Request</span></span>

<span data-ttu-id="10b54-155">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="10b54-155">Here is an example of the request.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/advancedqueries/run
```

```json
{
    "Query":"DeviceProcessEvents  
    | where InitiatingProcessFileName =~ 'powershell.exe'
    | where ProcessCommandLine contains 'appdata'
    | project Timestamp, FileName, InitiatingProcessFileName, DeviceId
    | limit 2"
}
```

##### <a name="response"></a><span data-ttu-id="10b54-156">Réponse</span><span class="sxs-lookup"><span data-stu-id="10b54-156">Response</span></span>

<span data-ttu-id="10b54-157">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="10b54-157">Here is an example of the response.</span></span>

>[!NOTE]
><span data-ttu-id="10b54-158">L’objet de réponse illustré ici peut être tronqué pour des raisons de concision.</span><span class="sxs-lookup"><span data-stu-id="10b54-158">The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="10b54-159">Toutes les propriétés sont renvoyées à partir d’un appel réel.</span><span class="sxs-lookup"><span data-stu-id="10b54-159">All of the properties will be returned from an actual call.</span></span>

```json
{
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
        },
        {
            "Name": "DeviceId",
            "Type": "String"
        }
    ],
    "Results": [
        {
            "Timestamp": "2020-02-05T01:10:26.2648757Z",
            "FileName": "csc.exe",
            "InitiatingProcessFileName": "powershell.exe",
            "DeviceId": "10cbf9182d4e95660362f65cfa67c7731f62fdb3"
        },
        {
            "Timestamp": "2020-02-05T01:10:26.5614772Z",
            "FileName": "csc.exe",
            "InitiatingProcessFileName": "powershell.exe",
            "DeviceId": "10cbf9182d4e95660362f65cfa67c7731f62fdb3"
        }
    ]
}
```

## <a name="related-topics"></a><span data-ttu-id="10b54-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10b54-160">Related topics</span></span>

- [<span data-ttu-id="10b54-161">Présentation des API Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="10b54-161">Microsoft Defender for Endpoint APIs introduction</span></span>](apis-intro.md)
- [<span data-ttu-id="10b54-162">Recherche avancée à partir du portail</span><span class="sxs-lookup"><span data-stu-id="10b54-162">Advanced Hunting from Portal</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="10b54-163">Repérage avancé à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="10b54-163">Advanced Hunting using PowerShell</span></span>](run-advanced-query-sample-powershell.md)
