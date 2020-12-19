---
title: API de chasse avancée Microsoft 365 Defender
description: Découvrez comment exécuter des requêtes de chasse avancées à l’aide de l’API de chasse avancée de Microsoft 365 Defender
keywords: Chasse avancée, API, API, MTP, M365 Defender, Microsoft 365 Defender
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
ms.openlocfilehash: e7cd9192ec25e01ed06b77cb2b39357cb9df79bd
ms.sourcegitcommit: d6b1da2e12d55f69e4353289e90f5ae2f60066d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "49719379"
---
# <a name="microsoft-365-defender-advanced-hunting-api"></a><span data-ttu-id="8075b-104">API de chasse avancée Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8075b-104">Microsoft 365 Defender Advanced hunting API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="8075b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8075b-105">**Applies to:**</span></span>

- <span data-ttu-id="8075b-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="8075b-106">Microsoft Threat Protection</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8075b-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="8075b-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8075b-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="8075b-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="8075b-109">La [chasse avancée](advanced-hunting-overview.md) est un outil de recherche de menace qui utilise des [requêtes spécialement construites](advanced-hunting-query-language.md) pour examiner les 30 derniers jours de données d’événement dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="8075b-109">[Advanced hunting](advanced-hunting-overview.md) is a threat-hunting tool that uses [specially constructed queries](advanced-hunting-query-language.md) to examine the past 30 days of event data in Microsoft 365 Defender.</span></span> <span data-ttu-id="8075b-110">Vous pouvez utiliser des requêtes de chasse avancées pour inspecter l’activité inhabituelle, détecter les menaces potentielles et même répondre aux attaques.</span><span class="sxs-lookup"><span data-stu-id="8075b-110">You can use advanced hunting queries to inspect unusual activity, detect possible threats, and even respond to attacks.</span></span> <span data-ttu-id="8075b-111">L’API de chasse avancée vous permet d’interroger des données d’événement par programmation.</span><span class="sxs-lookup"><span data-stu-id="8075b-111">The advanced hunting API allows you to programatically query event data.</span></span>

## <a name="quotas-and-resource-allocation"></a><span data-ttu-id="8075b-112">Quotas et allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="8075b-112">Quotas and resource allocation</span></span>

<span data-ttu-id="8075b-113">Les conditions suivantes sont liées à toutes les requêtes.</span><span class="sxs-lookup"><span data-stu-id="8075b-113">The following conditions relate to all queries.</span></span>

1. <span data-ttu-id="8075b-114">Les requêtes explorent et retournent les données des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="8075b-114">Queries explore and return data from the past 30 days.</span></span>
2. <span data-ttu-id="8075b-115">Les résultats peuvent renvoyer jusqu’à 100 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="8075b-115">Results can return up to 100,000 rows.</span></span>
3. <span data-ttu-id="8075b-116">Vous pouvez effectuer jusqu’à 10 appels par minute par client.</span><span class="sxs-lookup"><span data-stu-id="8075b-116">You can make up to 10 calls per minute per tenant.</span></span>
4. <span data-ttu-id="8075b-117">Vous disposez de 10 minutes d’exécution par heure et par client.</span><span class="sxs-lookup"><span data-stu-id="8075b-117">You have 10 minutes of running time per hour per tenant.</span></span>
5. <span data-ttu-id="8075b-118">Vous avez quatre heures au total du temps d’exécution par client.</span><span class="sxs-lookup"><span data-stu-id="8075b-118">You have four total hours of running time day per tenant.</span></span>
6. <span data-ttu-id="8075b-119">Si une demande unique s’exécute pendant plus de 10 minutes, elle expire et renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="8075b-119">If a single request runs for more than 10 minutes, it will time out and return an error.</span></span>
7. <span data-ttu-id="8075b-120">Un `429` Code de réponse http indique que vous avez atteint un quota, soit le nombre de demandes envoyées, soit le temps d’exécution alloué.</span><span class="sxs-lookup"><span data-stu-id="8075b-120">A `429` HTTP response code indicates that you've reached a quota, either by number of requests sent, or by allotted running time.</span></span> <span data-ttu-id="8075b-121">Le corps de la réponse inclura le temps jusqu’à ce que le quota que vous avez atteint soit réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="8075b-121">The response body will include the time until the quota you reached will be reset.</span></span>

## <a name="permissions"></a><span data-ttu-id="8075b-122">Autorisations</span><span class="sxs-lookup"><span data-stu-id="8075b-122">Permissions</span></span>

<span data-ttu-id="8075b-123">L’une des autorisations suivantes est nécessaire pour appeler l’API de chasse avancée.</span><span class="sxs-lookup"><span data-stu-id="8075b-123">One of the following permissions is required to call the advanced hunting API.</span></span> <span data-ttu-id="8075b-124">Pour plus d’informations, notamment sur la façon de choisir des autorisations, consultez [la rubrique Access the Microsoft 365 Defender protection APIs](api-access.md)</span><span class="sxs-lookup"><span data-stu-id="8075b-124">To learn more, including how to choose permissions, see [Access the Microsoft 365 Defender Protection APIs](api-access.md)</span></span>

<span data-ttu-id="8075b-125">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="8075b-125">Permission type</span></span> | <span data-ttu-id="8075b-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="8075b-126">Permission</span></span> | <span data-ttu-id="8075b-127">Nom d’affichage des autorisations</span><span class="sxs-lookup"><span data-stu-id="8075b-127">Permission display name</span></span>
-|-|-
<span data-ttu-id="8075b-128">Application</span><span class="sxs-lookup"><span data-stu-id="8075b-128">Application</span></span> | <span data-ttu-id="8075b-129">AdvancedHunting. Read. All</span><span class="sxs-lookup"><span data-stu-id="8075b-129">AdvancedHunting.Read.All</span></span> | <span data-ttu-id="8075b-130">Exécuter des requêtes avancées</span><span class="sxs-lookup"><span data-stu-id="8075b-130">Run advanced queries</span></span>
<span data-ttu-id="8075b-131">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="8075b-131">Delegated (work or school account)</span></span> | <span data-ttu-id="8075b-132">AdvancedHunting. Read</span><span class="sxs-lookup"><span data-stu-id="8075b-132">AdvancedHunting.Read</span></span> | <span data-ttu-id="8075b-133">Exécuter des requêtes avancées</span><span class="sxs-lookup"><span data-stu-id="8075b-133">Run advanced queries</span></span>

>[!Note]
> <span data-ttu-id="8075b-134">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="8075b-134">When obtaining a token using user credentials:</span></span>
>
>- <span data-ttu-id="8075b-135">L’utilisateur doit disposer du rôle « afficher les données » dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8075b-135">The user needs to have the 'View Data' AD role</span></span>
>- <span data-ttu-id="8075b-136">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres du groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="8075b-136">The user needs to have access to the device, based on device group settings.</span></span>

## <a name="http-request"></a><span data-ttu-id="8075b-137">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="8075b-137">HTTP request</span></span>

```HTTP
POST https://api.security.microsoft.com/api/advancedhunting/run
```

## <a name="request-headers"></a><span data-ttu-id="8075b-138">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="8075b-138">Request headers</span></span>

<span data-ttu-id="8075b-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="8075b-139">Header</span></span> | <span data-ttu-id="8075b-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="8075b-140">Value</span></span>
-|-
<span data-ttu-id="8075b-141">Autorisation</span><span class="sxs-lookup"><span data-stu-id="8075b-141">Authorization</span></span> | <span data-ttu-id="8075b-142">Support {Token} **Remarque : obligatoire**</span><span class="sxs-lookup"><span data-stu-id="8075b-142">Bearer {token} **Note: required**</span></span>
<span data-ttu-id="8075b-143">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8075b-143">Content-Type</span></span> | <span data-ttu-id="8075b-144">application/json</span><span class="sxs-lookup"><span data-stu-id="8075b-144">application/json</span></span>

## <a name="request-body"></a><span data-ttu-id="8075b-145">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="8075b-145">Request body</span></span>

<span data-ttu-id="8075b-146">Dans le corps de la demande, fournissez un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8075b-146">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="8075b-147">Paramètre</span><span class="sxs-lookup"><span data-stu-id="8075b-147">Parameter</span></span> | <span data-ttu-id="8075b-148">Type</span><span class="sxs-lookup"><span data-stu-id="8075b-148">Type</span></span> | <span data-ttu-id="8075b-149">Description</span><span class="sxs-lookup"><span data-stu-id="8075b-149">Description</span></span>
-|-|-
<span data-ttu-id="8075b-150">Requête</span><span class="sxs-lookup"><span data-stu-id="8075b-150">Query</span></span> | <span data-ttu-id="8075b-151">Texte</span><span class="sxs-lookup"><span data-stu-id="8075b-151">Text</span></span> | <span data-ttu-id="8075b-152">Requête à exécuter.</span><span class="sxs-lookup"><span data-stu-id="8075b-152">The query to run.</span></span> <span data-ttu-id="8075b-153">**Remarque : obligatoire**</span><span class="sxs-lookup"><span data-stu-id="8075b-153">**Note: required**</span></span>

## <a name="response"></a><span data-ttu-id="8075b-154">Réponse</span><span class="sxs-lookup"><span data-stu-id="8075b-154">Response</span></span>

<span data-ttu-id="8075b-155">Si elle réussit, cette méthode renvoie `200 OK` et un objet _QueryResponse_ dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="8075b-155">If successful, this method will return `200 OK`, and a _QueryResponse_ object in the response body.</span></span>

<span data-ttu-id="8075b-156">L’objet Response contient trois propriétés de niveau supérieur :</span><span class="sxs-lookup"><span data-stu-id="8075b-156">The response object contains three top-level properties:</span></span>

1. <span data-ttu-id="8075b-157">Stats-dictionnaire des statistiques de performances des requêtes.</span><span class="sxs-lookup"><span data-stu-id="8075b-157">Stats - A dictionary of query performance statistics.</span></span>
2. <span data-ttu-id="8075b-158">Schema : le schéma de la réponse, une liste de paires Name-Type pour chaque colonne.</span><span class="sxs-lookup"><span data-stu-id="8075b-158">Schema - The schema of the response, a list of Name-Type pairs for each column.</span></span>
3. <span data-ttu-id="8075b-159">Results-liste d’événements de chasse avancés.</span><span class="sxs-lookup"><span data-stu-id="8075b-159">Results - A list of advanced hunting events.</span></span>

## <a name="example"></a><span data-ttu-id="8075b-160">Exemple</span><span class="sxs-lookup"><span data-stu-id="8075b-160">Example</span></span>

<span data-ttu-id="8075b-161">Dans l’exemple suivant, un utilisateur envoie la requête ci-dessous et reçoit un objet de réponse d’API contenant `Stats` , `Schema` et `Results` .</span><span class="sxs-lookup"><span data-stu-id="8075b-161">In the following example, a user sends the query below and receives an API response object containing `Stats`, `Schema`, and `Results`.</span></span>

### <a name="query"></a><span data-ttu-id="8075b-162">Requête</span><span class="sxs-lookup"><span data-stu-id="8075b-162">Query</span></span>

```json
{
    "Query":"DeviceProcessEvents | where InitiatingProcessFileName =~ \"powershell.exe\" | project Timestamp, FileName, InitiatingProcessFileName | order by Timestamp desc | limit 2"
}

```

### <a name="response-object"></a><span data-ttu-id="8075b-163">Response, objet</span><span class="sxs-lookup"><span data-stu-id="8075b-163">Response object</span></span>

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

## <a name="related-articles"></a><span data-ttu-id="8075b-164">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="8075b-164">Related articles</span></span>

- [<span data-ttu-id="8075b-165">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8075b-165">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="8075b-166">En savoir plus sur les limites d’API et la gestion des licences</span><span class="sxs-lookup"><span data-stu-id="8075b-166">Learn about API limits and licensing</span></span>](api-terms.md)
- [<span data-ttu-id="8075b-167">Comprendre les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="8075b-167">Understand error codes</span></span>](api-error-codes.md)
- [<span data-ttu-id="8075b-168">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="8075b-168">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
