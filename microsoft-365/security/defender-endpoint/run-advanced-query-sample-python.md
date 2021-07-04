---
title: Guide de l’API de recherche avancée avec Python
ms.reviewer: ''
description: Découvrez comment interroger à l’aide de l’API Microsoft Defender for Endpoint, à l’aide de Python, avec des exemples.
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 7ee431c88430916fcba60266a3a3a5180d830c0d
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53289258"
---
# <a name="advanced-hunting-using-python"></a><span data-ttu-id="d8517-104">Repérage avancé à l’aide de Python</span><span class="sxs-lookup"><span data-stu-id="d8517-104">Advanced Hunting using Python</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="d8517-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="d8517-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="d8517-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="d8517-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="d8517-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d8517-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

<span data-ttu-id="d8517-108">Exécutez des requêtes avancées à l’aide de Python, voir [API de recherche avancée.](run-advanced-query-api.md)</span><span class="sxs-lookup"><span data-stu-id="d8517-108">Run advanced queries using Python, see [Advanced Hunting API](run-advanced-query-api.md).</span></span>

<span data-ttu-id="d8517-109">Dans cette section, nous partageons des exemples Python pour récupérer un jeton et l’utiliser pour exécuter une requête.</span><span class="sxs-lookup"><span data-stu-id="d8517-109">In this section, we share Python samples to retrieve a token and use it to run a query.</span></span>

> <span data-ttu-id="d8517-110">**Conditions préalables**: vous devez d’abord [créer une application.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="d8517-110">**Prerequisite**: You first need to [create an app](apis-intro.md).</span></span>

## <a name="get-token"></a><span data-ttu-id="d8517-111">Obtenir un jeton</span><span class="sxs-lookup"><span data-stu-id="d8517-111">Get token</span></span>

- <span data-ttu-id="d8517-112">Exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8517-112">Run the following commands:</span></span>

```python
import json
import urllib.request
import urllib.parse

tenantId = '00000000-0000-0000-0000-000000000000' # Paste your own tenant ID here
appId = '11111111-1111-1111-1111-111111111111' # Paste your own app ID here
appSecret = '22222222-2222-2222-2222-222222222222' # Paste your own app secret here

url = "https://login.microsoftonline.com/%s/oauth2/token" % (tenantId)

resourceAppIdUri = 'https://api.securitycenter.microsoft.com'

body = {
    'resource' : resourceAppIdUri,
    'client_id' : appId,
    'client_secret' : appSecret,
    'grant_type' : 'client_credentials'
}

data = urllib.parse.urlencode(body).encode("utf-8")

req = urllib.request.Request(url, data)
response = urllib.request.urlopen(req)
jsonResponse = json.loads(response.read())
aadToken = jsonResponse["access_token"]
```

<span data-ttu-id="d8517-113">where</span><span class="sxs-lookup"><span data-stu-id="d8517-113">where</span></span>

- <span data-ttu-id="d8517-114">tenantId : ID du client pour le compte duquel vous souhaitez exécuter la requête (autrement dit, la requête sera exécuté sur les données de ce client)</span><span class="sxs-lookup"><span data-stu-id="d8517-114">tenantId: ID of the tenant on behalf of which you want to run the query (that is, the query will be run on the data of this tenant)</span></span>
- <span data-ttu-id="d8517-115">appId : ID de votre application Azure AD (l’application doit avoir l’autorisation « Exécuter des requêtes avancées » sur Microsoft Defender pour le point de terminaison)</span><span class="sxs-lookup"><span data-stu-id="d8517-115">appId: ID of your Azure AD app (the app must have 'Run advanced queries' permission to Microsoft Defender for Endpoint)</span></span>
- <span data-ttu-id="d8517-116">appSecret : secret de votre application Azure AD</span><span class="sxs-lookup"><span data-stu-id="d8517-116">appSecret: Secret of your Azure AD app</span></span>

## <a name="run-query"></a><span data-ttu-id="d8517-117">Exécuter la requête</span><span class="sxs-lookup"><span data-stu-id="d8517-117">Run query</span></span>

 <span data-ttu-id="d8517-118">Exécutez la requête suivante :</span><span class="sxs-lookup"><span data-stu-id="d8517-118">Run the following query:</span></span>

```python
query = 'RegistryEvents | limit 10' # Paste your own query here

url = "https://api.securitycenter.microsoft.com/api/advancedqueries/run"
headers = { 
    'Content-Type' : 'application/json',
    'Accept' : 'application/json',
    'Authorization' : "Bearer " + aadToken
}

data = json.dumps({ 'Query' : query }).encode("utf-8")

req = urllib.request.Request(url, data, headers)
response = urllib.request.urlopen(req)
jsonResponse = json.loads(response.read())
schema = jsonResponse["Schema"]
results = jsonResponse["Results"]
```

- <span data-ttu-id="d8517-119">contient le schéma des résultats de votre requête</span><span class="sxs-lookup"><span data-stu-id="d8517-119">schema contains the schema of the results of your query</span></span>
- <span data-ttu-id="d8517-120">les résultats contiennent les résultats de votre requête</span><span class="sxs-lookup"><span data-stu-id="d8517-120">results contain the results of your query</span></span>

### <a name="complex-queries"></a><span data-ttu-id="d8517-121">Requêtes complexes</span><span class="sxs-lookup"><span data-stu-id="d8517-121">Complex queries</span></span>

<span data-ttu-id="d8517-122">Si vous souhaitez exécuter des requêtes complexes (ou des requêtes multilignes), enregistrez votre requête dans un fichier et, au lieu de la première ligne de l’exemple ci-dessus, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d8517-122">If you want to run complex queries (or multiline queries), save your query in a file and, instead of the first line in the above sample, run the below command:</span></span>

```python
queryFile = open("D:\\Temp\\myQuery.txt", 'r') # Replace with the path to your file
query = queryFile.read()
queryFile.close()
```

## <a name="work-with-query-results"></a><span data-ttu-id="d8517-123">Travailler avec les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="d8517-123">Work with query results</span></span>

<span data-ttu-id="d8517-124">Vous pouvez désormais utiliser les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="d8517-124">You can now use the query results.</span></span>

<span data-ttu-id="d8517-125">Pour itérer sur les résultats, faites les choses suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8517-125">To iterate over the results do the below:</span></span>

```python
for result in results:
    print(result) # Prints the whole result
    print(result["EventTime"]) # Prints only the property 'EventTime' from the result
```

<span data-ttu-id="d8517-126">Pour obtenir les résultats de la requête au format CSV dans un fichier, file1.csv ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="d8517-126">To output the results of the query in CSV format in file file1.csv do the below:</span></span>

```python
import csv

outputFile = open("D:\\Temp\\file1.csv", 'w')
output = csv.writer(outputFile)
output.writerow(results[0].keys())
for result in results:
    output.writerow(result.values())

outputFile.close()
```

<span data-ttu-id="d8517-127">Pour obtenir les résultats de la requête au format JSON au file1.jssur :</span><span class="sxs-lookup"><span data-stu-id="d8517-127">To output the results of the query in JSON format in file file1.json do the below:</span></span>

```python
outputFile = open("D:\\Temp\\file1.json", 'w')
json.dump(results, outputFile)
outputFile.close()
```

## <a name="related-topic"></a><span data-ttu-id="d8517-128">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="d8517-128">Related topic</span></span>

- [<span data-ttu-id="d8517-129">API Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d8517-129">Microsoft Defender for Endpoint APIs</span></span>](apis-intro.md)
- [<span data-ttu-id="d8517-130">API de recherche avancée de menaces</span><span class="sxs-lookup"><span data-stu-id="d8517-130">Advanced Hunting API</span></span>](run-advanced-query-api.md)
- [<span data-ttu-id="d8517-131">Repérage avancé à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="d8517-131">Advanced Hunting using PowerShell</span></span>](run-advanced-query-sample-powershell.md)
