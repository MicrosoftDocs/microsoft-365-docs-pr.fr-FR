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
ms.openlocfilehash: 99f39a10de6231a72220c5c2a90ec915b1a4e44a
ms.sourcegitcommit: cbe8724bd71d1c002395d98f1451c5f578c824f9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2021
ms.locfileid: "49988115"
---
# <a name="microsoft-365-defender-advanced-hunting-api"></a><span data-ttu-id="a0e21-104">API de recherche avancée Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a0e21-104">Microsoft 365 Defender Advanced hunting API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="a0e21-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a0e21-105">**Applies to:**</span></span>

- <span data-ttu-id="a0e21-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="a0e21-106">Microsoft Threat Protection</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a0e21-107">Certaines informations concernent des produits pré-publiés qui peuvent être considérablement modifiés avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="a0e21-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a0e21-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="a0e21-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="a0e21-109">[Le recherche](advanced-hunting-overview.md) avancée est un [](advanced-hunting-query-language.md) outil de recherche de menaces qui utilise des requêtes spécialement conçues pour examiner les 30 derniers jours de données d’événement dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="a0e21-109">[Advanced hunting](advanced-hunting-overview.md) is a threat-hunting tool that uses [specially constructed queries](advanced-hunting-query-language.md) to examine the past 30 days of event data in Microsoft 365 Defender.</span></span> <span data-ttu-id="a0e21-110">Vous pouvez utiliser des requêtes de recherche avancées pour inspecter les activités inhabituelles, détecter les menaces possibles et même répondre aux attaques.</span><span class="sxs-lookup"><span data-stu-id="a0e21-110">You can use advanced hunting queries to inspect unusual activity, detect possible threats, and even respond to attacks.</span></span> <span data-ttu-id="a0e21-111">L’API de recherche avancée vous permet d’interroger par programmation des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="a0e21-111">The advanced hunting API allows you to programatically query event data.</span></span>

## <a name="quotas-and-resource-allocation"></a><span data-ttu-id="a0e21-112">Quotas et allocation de ressources</span><span class="sxs-lookup"><span data-stu-id="a0e21-112">Quotas and resource allocation</span></span>

<span data-ttu-id="a0e21-113">Les conditions suivantes concernent toutes les requêtes.</span><span class="sxs-lookup"><span data-stu-id="a0e21-113">The following conditions relate to all queries.</span></span>

1. <span data-ttu-id="a0e21-114">Les requêtes explorent et retournent des données des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="a0e21-114">Queries explore and return data from the past 30 days.</span></span>
2. <span data-ttu-id="a0e21-115">Les résultats peuvent renvoyer jusqu’à 100 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="a0e21-115">Results can return up to 100,000 rows.</span></span>
3. <span data-ttu-id="a0e21-116">Vous pouvez effectuer jusqu’à 15 appels par minute et par client.</span><span class="sxs-lookup"><span data-stu-id="a0e21-116">You can make up to 15 calls per minute per tenant.</span></span>
4. <span data-ttu-id="a0e21-117">Vous avez 10 minutes d’exécution par heure et par client.</span><span class="sxs-lookup"><span data-stu-id="a0e21-117">You have 10 minutes of running time per hour per tenant.</span></span>
5. <span data-ttu-id="a0e21-118">Vous avez quatre heures d’exécution par jour et par client.</span><span class="sxs-lookup"><span data-stu-id="a0e21-118">You have four total hours of running time per day per tenant.</span></span>
6. <span data-ttu-id="a0e21-119">Si une seule demande s’exécute pendant plus de 10 minutes, elle prend du temps et retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="a0e21-119">If a single request runs for more than 10 minutes, it will time out and return an error.</span></span>
7. <span data-ttu-id="a0e21-120">Un code de réponse HTTP indique que vous avez atteint un quota, soit par nombre de demandes envoyées, soit par temps `429` d’exécution alloué.</span><span class="sxs-lookup"><span data-stu-id="a0e21-120">A `429` HTTP response code indicates that you've reached a quota, either by number of requests sent, or by allotted running time.</span></span> <span data-ttu-id="a0e21-121">Lisez le corps de la réponse pour comprendre la limite que vous avez atteinte.</span><span class="sxs-lookup"><span data-stu-id="a0e21-121">Read the response body to understand the limit you have reached.</span></span> 

> [!NOTE]
> <span data-ttu-id="a0e21-122">Tous les quotas répertoriés ci-dessus (par exemple, 15 appels par minute) sont de taille par client.</span><span class="sxs-lookup"><span data-stu-id="a0e21-122">All quotas listed above (for example 15 calls per min) are per tenant size.</span></span> <span data-ttu-id="a0e21-123">Ces quotas sont au minimum.</span><span class="sxs-lookup"><span data-stu-id="a0e21-123">These quotas are the minimum.</span></span>

## <a name="permissions"></a><span data-ttu-id="a0e21-124">Autorisations</span><span class="sxs-lookup"><span data-stu-id="a0e21-124">Permissions</span></span>

<span data-ttu-id="a0e21-125">L’une des autorisations suivantes est nécessaire pour appeler l’API de recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="a0e21-125">One of the following permissions is required to call the advanced hunting API.</span></span> <span data-ttu-id="a0e21-126">Pour plus d’informations, notamment sur le choix des autorisations, voir Access sur les API [Microsoft 365 Defender Protection](api-access.md)</span><span class="sxs-lookup"><span data-stu-id="a0e21-126">To learn more, including how to choose permissions, see [Access the Microsoft 365 Defender Protection APIs](api-access.md)</span></span>

<span data-ttu-id="a0e21-127">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="a0e21-127">Permission type</span></span> | <span data-ttu-id="a0e21-128">Autorisation</span><span class="sxs-lookup"><span data-stu-id="a0e21-128">Permission</span></span> | <span data-ttu-id="a0e21-129">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="a0e21-129">Permission display name</span></span>
-|-|-
<span data-ttu-id="a0e21-130">Application</span><span class="sxs-lookup"><span data-stu-id="a0e21-130">Application</span></span> | <span data-ttu-id="a0e21-131">AdvancedHouting.Read.All</span><span class="sxs-lookup"><span data-stu-id="a0e21-131">AdvancedHunting.Read.All</span></span> | <span data-ttu-id="a0e21-132">Exécuter des requêtes avancées</span><span class="sxs-lookup"><span data-stu-id="a0e21-132">Run advanced queries</span></span>
<span data-ttu-id="a0e21-133">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="a0e21-133">Delegated (work or school account)</span></span> | <span data-ttu-id="a0e21-134">AdvancedHouting.Read</span><span class="sxs-lookup"><span data-stu-id="a0e21-134">AdvancedHunting.Read</span></span> | <span data-ttu-id="a0e21-135">Exécuter des requêtes avancées</span><span class="sxs-lookup"><span data-stu-id="a0e21-135">Run advanced queries</span></span>

>[!Note]
> <span data-ttu-id="a0e21-136">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="a0e21-136">When obtaining a token using user credentials:</span></span>
>
>- <span data-ttu-id="a0e21-137">L’utilisateur doit avoir le rôle AD « Afficher les données »</span><span class="sxs-lookup"><span data-stu-id="a0e21-137">The user needs to have the 'View Data' AD role</span></span>
>- <span data-ttu-id="a0e21-138">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres de groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="a0e21-138">The user needs to have access to the device, based on device group settings.</span></span>

## <a name="http-request"></a><span data-ttu-id="a0e21-139">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="a0e21-139">HTTP request</span></span>

```HTTP
POST https://api.security.microsoft.com/api/advancedhunting/run
```

## <a name="request-headers"></a><span data-ttu-id="a0e21-140">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="a0e21-140">Request headers</span></span>

<span data-ttu-id="a0e21-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0e21-141">Header</span></span> | <span data-ttu-id="a0e21-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0e21-142">Value</span></span>
-|-
<span data-ttu-id="a0e21-143">Autorisation</span><span class="sxs-lookup"><span data-stu-id="a0e21-143">Authorization</span></span> | <span data-ttu-id="a0e21-144">Remarque {token} du porteur **: obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a0e21-144">Bearer {token} **Note: required**</span></span>
<span data-ttu-id="a0e21-145">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a0e21-145">Content-Type</span></span> | <span data-ttu-id="a0e21-146">application/json</span><span class="sxs-lookup"><span data-stu-id="a0e21-146">application/json</span></span>

## <a name="request-body"></a><span data-ttu-id="a0e21-147">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="a0e21-147">Request body</span></span>

<span data-ttu-id="a0e21-148">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="a0e21-148">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="a0e21-149">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a0e21-149">Parameter</span></span> | <span data-ttu-id="a0e21-150">Type</span><span class="sxs-lookup"><span data-stu-id="a0e21-150">Type</span></span> | <span data-ttu-id="a0e21-151">Description</span><span class="sxs-lookup"><span data-stu-id="a0e21-151">Description</span></span>
-|-|-
<span data-ttu-id="a0e21-152">Requête</span><span class="sxs-lookup"><span data-stu-id="a0e21-152">Query</span></span> | <span data-ttu-id="a0e21-153">Texte</span><span class="sxs-lookup"><span data-stu-id="a0e21-153">Text</span></span> | <span data-ttu-id="a0e21-154">Requête à exécuter.</span><span class="sxs-lookup"><span data-stu-id="a0e21-154">The query to run.</span></span> <span data-ttu-id="a0e21-155">**Remarque : obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a0e21-155">**Note: required**</span></span>

## <a name="response"></a><span data-ttu-id="a0e21-156">Réponse</span><span class="sxs-lookup"><span data-stu-id="a0e21-156">Response</span></span>

<span data-ttu-id="a0e21-157">Si elle réussit, cette méthode retourne `200 OK` un objet _QueryResponse_ dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="a0e21-157">If successful, this method will return `200 OK`, and a _QueryResponse_ object in the response body.</span></span>

<span data-ttu-id="a0e21-158">L’objet de réponse contient trois propriétés de niveau supérieur :</span><span class="sxs-lookup"><span data-stu-id="a0e21-158">The response object contains three top-level properties:</span></span>

1. <span data-ttu-id="a0e21-159">Statistiques : dictionnaire des statistiques de performances des requêtes.</span><span class="sxs-lookup"><span data-stu-id="a0e21-159">Stats - A dictionary of query performance statistics.</span></span>
2. <span data-ttu-id="a0e21-160">Schéma : schéma de la réponse, liste des Name-Type pour chaque colonne.</span><span class="sxs-lookup"><span data-stu-id="a0e21-160">Schema - The schema of the response, a list of Name-Type pairs for each column.</span></span>
3. <span data-ttu-id="a0e21-161">Résultats : liste des événements de recherche avancés.</span><span class="sxs-lookup"><span data-stu-id="a0e21-161">Results - A list of advanced hunting events.</span></span>

## <a name="example"></a><span data-ttu-id="a0e21-162">Exemple</span><span class="sxs-lookup"><span data-stu-id="a0e21-162">Example</span></span>

<span data-ttu-id="a0e21-163">Dans l’exemple suivant, un utilisateur envoie la requête ci-dessous et reçoit un objet de réponse API contenant `Stats` `Schema` , et `Results` .</span><span class="sxs-lookup"><span data-stu-id="a0e21-163">In the following example, a user sends the query below and receives an API response object containing `Stats`, `Schema`, and `Results`.</span></span>

### <a name="query"></a><span data-ttu-id="a0e21-164">Requête</span><span class="sxs-lookup"><span data-stu-id="a0e21-164">Query</span></span>

```json
{
    "Query":"DeviceProcessEvents | where InitiatingProcessFileName =~ \"powershell.exe\" | project Timestamp, FileName, InitiatingProcessFileName | order by Timestamp desc | limit 2"
}

```

### <a name="response-object"></a><span data-ttu-id="a0e21-165">Objet Response</span><span class="sxs-lookup"><span data-stu-id="a0e21-165">Response object</span></span>

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

## <a name="related-articles"></a><span data-ttu-id="a0e21-166">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="a0e21-166">Related articles</span></span>

- [<span data-ttu-id="a0e21-167">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a0e21-167">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="a0e21-168">En savoir plus sur les limites d’API et les licences</span><span class="sxs-lookup"><span data-stu-id="a0e21-168">Learn about API limits and licensing</span></span>](api-terms.md)
- [<span data-ttu-id="a0e21-169">Comprendre les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a0e21-169">Understand error codes</span></span>](api-error-codes.md)
- [<span data-ttu-id="a0e21-170">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="a0e21-170">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
