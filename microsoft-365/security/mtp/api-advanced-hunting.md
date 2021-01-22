---
title: API de recherche avancée Microsoft 365 Defender
description: Découvrez comment exécuter des requêtes de recherche avancée à l’aide de l’API de recherche avancée de Microsoft 365 Defender
keywords: Recherche avancée, API, api, MTP, M365 Defender, Microsoft 365 Defender
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
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
ms.technology: m365d
ms.openlocfilehash: 4213773c3305c28f0913013d8f7634c083811f52
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49932081"
---
# <a name="microsoft-365-defender-advanced-hunting-api"></a><span data-ttu-id="b8d4d-104">API de recherche avancée Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b8d4d-104">Microsoft 365 Defender Advanced hunting API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="b8d4d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b8d4d-105">**Applies to:**</span></span>

- <span data-ttu-id="b8d4d-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="b8d4d-106">Microsoft Threat Protection</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8d4d-107">Certaines informations concernent des produits pré-publiés qui peuvent être considérablement modifiés avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b8d4d-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="b8d4d-109">[Le recherche](advanced-hunting-overview.md) avancée est un [](advanced-hunting-query-language.md) outil de recherche de menaces qui utilise des requêtes spécialement conçues pour examiner les 30 derniers jours de données d’événement dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-109">[Advanced hunting](advanced-hunting-overview.md) is a threat-hunting tool that uses [specially constructed queries](advanced-hunting-query-language.md) to examine the past 30 days of event data in Microsoft 365 Defender.</span></span> <span data-ttu-id="b8d4d-110">Vous pouvez utiliser des requêtes de recherche avancées pour inspecter les activités inhabituelles, détecter les menaces possibles et même répondre aux attaques.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-110">You can use advanced hunting queries to inspect unusual activity, detect possible threats, and even respond to attacks.</span></span> <span data-ttu-id="b8d4d-111">L’API de recherche avancée vous permet d’interroger par programmation des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-111">The advanced hunting API allows you to programatically query event data.</span></span>

## <a name="quotas-and-resource-allocation"></a><span data-ttu-id="b8d4d-112">Quotas et allocation de ressources</span><span class="sxs-lookup"><span data-stu-id="b8d4d-112">Quotas and resource allocation</span></span>

<span data-ttu-id="b8d4d-113">Les conditions suivantes concernent toutes les requêtes.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-113">The following conditions relate to all queries.</span></span>

1. <span data-ttu-id="b8d4d-114">Les requêtes explorent et retournent des données des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-114">Queries explore and return data from the past 30 days.</span></span>
2. <span data-ttu-id="b8d4d-115">Les résultats peuvent renvoyer jusqu’à 100 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-115">Results can return up to 100,000 rows.</span></span>
3. <span data-ttu-id="b8d4d-116">Vous pouvez effectuer jusqu’à 10 appels par minute et par client.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-116">You can make up to 10 calls per minute per tenant.</span></span>
4. <span data-ttu-id="b8d4d-117">Vous avez 10 minutes d’exécution par heure et par client.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-117">You have 10 minutes of running time per hour per tenant.</span></span>
5. <span data-ttu-id="b8d4d-118">Vous avez quatre heures d’exécution par client.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-118">You have four total hours of running time day per tenant.</span></span>
6. <span data-ttu-id="b8d4d-119">Si une seule demande s’exécute pendant plus de 10 minutes, elle prend du temps et retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-119">If a single request runs for more than 10 minutes, it will time out and return an error.</span></span>
7. <span data-ttu-id="b8d4d-120">Un code de réponse HTTP indique que vous avez atteint un quota, soit par nombre de demandes envoyées, soit par temps `429` d’exécution alloué.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-120">A `429` HTTP response code indicates that you've reached a quota, either by number of requests sent, or by allotted running time.</span></span> <span data-ttu-id="b8d4d-121">Le corps de la réponse inclut la durée jusqu’à ce que le quota que vous avez atteint soit réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-121">The response body will include the time until the quota you reached will be reset.</span></span>

## <a name="permissions"></a><span data-ttu-id="b8d4d-122">Autorisations</span><span class="sxs-lookup"><span data-stu-id="b8d4d-122">Permissions</span></span>

<span data-ttu-id="b8d4d-123">L’une des autorisations suivantes est nécessaire pour appeler l’API de recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-123">One of the following permissions is required to call the advanced hunting API.</span></span> <span data-ttu-id="b8d4d-124">Pour en savoir plus, notamment sur le choix des autorisations, consultez [l’api Access de Microsoft 365 Defender Protection.](api-access.md)</span><span class="sxs-lookup"><span data-stu-id="b8d4d-124">To learn more, including how to choose permissions, see [Access the Microsoft 365 Defender Protection APIs](api-access.md)</span></span>

<span data-ttu-id="b8d4d-125">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="b8d4d-125">Permission type</span></span> | <span data-ttu-id="b8d4d-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="b8d4d-126">Permission</span></span> | <span data-ttu-id="b8d4d-127">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="b8d4d-127">Permission display name</span></span>
-|-|-
<span data-ttu-id="b8d4d-128">Application</span><span class="sxs-lookup"><span data-stu-id="b8d4d-128">Application</span></span> | <span data-ttu-id="b8d4d-129">AdvancedHouting.Read.All</span><span class="sxs-lookup"><span data-stu-id="b8d4d-129">AdvancedHunting.Read.All</span></span> | <span data-ttu-id="b8d4d-130">Exécuter des requêtes avancées</span><span class="sxs-lookup"><span data-stu-id="b8d4d-130">Run advanced queries</span></span>
<span data-ttu-id="b8d4d-131">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="b8d4d-131">Delegated (work or school account)</span></span> | <span data-ttu-id="b8d4d-132">AdvancedHouting.Read</span><span class="sxs-lookup"><span data-stu-id="b8d4d-132">AdvancedHunting.Read</span></span> | <span data-ttu-id="b8d4d-133">Exécuter des requêtes avancées</span><span class="sxs-lookup"><span data-stu-id="b8d4d-133">Run advanced queries</span></span>

>[!Note]
> <span data-ttu-id="b8d4d-134">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="b8d4d-134">When obtaining a token using user credentials:</span></span>
>
>- <span data-ttu-id="b8d4d-135">L’utilisateur doit avoir le rôle AD « Afficher les données »</span><span class="sxs-lookup"><span data-stu-id="b8d4d-135">The user needs to have the 'View Data' AD role</span></span>
>- <span data-ttu-id="b8d4d-136">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres de groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-136">The user needs to have access to the device, based on device group settings.</span></span>

## <a name="http-request"></a><span data-ttu-id="b8d4d-137">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="b8d4d-137">HTTP request</span></span>

```HTTP
POST https://api.security.microsoft.com/api/advancedhunting/run
```

## <a name="request-headers"></a><span data-ttu-id="b8d4d-138">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="b8d4d-138">Request headers</span></span>

<span data-ttu-id="b8d4d-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8d4d-139">Header</span></span> | <span data-ttu-id="b8d4d-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8d4d-140">Value</span></span>
-|-
<span data-ttu-id="b8d4d-141">Authorization</span><span class="sxs-lookup"><span data-stu-id="b8d4d-141">Authorization</span></span> | <span data-ttu-id="b8d4d-142">Remarque {token} du porteur **: obligatoire**</span><span class="sxs-lookup"><span data-stu-id="b8d4d-142">Bearer {token} **Note: required**</span></span>
<span data-ttu-id="b8d4d-143">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b8d4d-143">Content-Type</span></span> | <span data-ttu-id="b8d4d-144">application/json</span><span class="sxs-lookup"><span data-stu-id="b8d4d-144">application/json</span></span>

## <a name="request-body"></a><span data-ttu-id="b8d4d-145">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="b8d4d-145">Request body</span></span>

<span data-ttu-id="b8d4d-146">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="b8d4d-146">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="b8d4d-147">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b8d4d-147">Parameter</span></span> | <span data-ttu-id="b8d4d-148">Type</span><span class="sxs-lookup"><span data-stu-id="b8d4d-148">Type</span></span> | <span data-ttu-id="b8d4d-149">Description</span><span class="sxs-lookup"><span data-stu-id="b8d4d-149">Description</span></span>
-|-|-
<span data-ttu-id="b8d4d-150">Requête</span><span class="sxs-lookup"><span data-stu-id="b8d4d-150">Query</span></span> | <span data-ttu-id="b8d4d-151">Texte</span><span class="sxs-lookup"><span data-stu-id="b8d4d-151">Text</span></span> | <span data-ttu-id="b8d4d-152">Requête à exécuter.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-152">The query to run.</span></span> <span data-ttu-id="b8d4d-153">**Remarque : obligatoire**</span><span class="sxs-lookup"><span data-stu-id="b8d4d-153">**Note: required**</span></span>

## <a name="response"></a><span data-ttu-id="b8d4d-154">Réponse</span><span class="sxs-lookup"><span data-stu-id="b8d4d-154">Response</span></span>

<span data-ttu-id="b8d4d-155">Si elle réussit, cette méthode retourne `200 OK` un objet _QueryResponse_ dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-155">If successful, this method will return `200 OK`, and a _QueryResponse_ object in the response body.</span></span>

<span data-ttu-id="b8d4d-156">L’objet de réponse contient trois propriétés de niveau supérieur :</span><span class="sxs-lookup"><span data-stu-id="b8d4d-156">The response object contains three top-level properties:</span></span>

1. <span data-ttu-id="b8d4d-157">Statistiques : dictionnaire des statistiques de performances des requêtes.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-157">Stats - A dictionary of query performance statistics.</span></span>
2. <span data-ttu-id="b8d4d-158">Schéma : schéma de la réponse, liste des Name-Type pour chaque colonne.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-158">Schema - The schema of the response, a list of Name-Type pairs for each column.</span></span>
3. <span data-ttu-id="b8d4d-159">Résultats : liste des événements de recherche avancés.</span><span class="sxs-lookup"><span data-stu-id="b8d4d-159">Results - A list of advanced hunting events.</span></span>

## <a name="example"></a><span data-ttu-id="b8d4d-160">Exemple</span><span class="sxs-lookup"><span data-stu-id="b8d4d-160">Example</span></span>

<span data-ttu-id="b8d4d-161">Dans l’exemple suivant, un utilisateur envoie la requête ci-dessous et reçoit un objet de réponse API contenant `Stats` `Schema` , et `Results` .</span><span class="sxs-lookup"><span data-stu-id="b8d4d-161">In the following example, a user sends the query below and receives an API response object containing `Stats`, `Schema`, and `Results`.</span></span>

### <a name="query"></a><span data-ttu-id="b8d4d-162">Requête</span><span class="sxs-lookup"><span data-stu-id="b8d4d-162">Query</span></span>

```json
{
    "Query":"DeviceProcessEvents | where InitiatingProcessFileName =~ \"powershell.exe\" | project Timestamp, FileName, InitiatingProcessFileName | order by Timestamp desc | limit 2"
}

```

### <a name="response-object"></a><span data-ttu-id="b8d4d-163">Objet Response</span><span class="sxs-lookup"><span data-stu-id="b8d4d-163">Response object</span></span>

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

## <a name="related-articles"></a><span data-ttu-id="b8d4d-164">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="b8d4d-164">Related articles</span></span>

- [<span data-ttu-id="b8d4d-165">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b8d4d-165">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="b8d4d-166">En savoir plus sur les limites d’API et les licences</span><span class="sxs-lookup"><span data-stu-id="b8d4d-166">Learn about API limits and licensing</span></span>](api-terms.md)
- [<span data-ttu-id="b8d4d-167">Comprendre les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b8d4d-167">Understand error codes</span></span>](api-error-codes.md)
- [<span data-ttu-id="b8d4d-168">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="b8d4d-168">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
