---
title: Advanced Hunting with PowerShell API Basics
ms.reviewer: ''
description: Découvrez les principes de base de l’interrogation de l’API Microsoft Defender for Endpoint à l’aide de PowerShell.
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
ms.openlocfilehash: 0d44f59f69c590ecd8d61207de8784af3e32197d
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52844885"
---
# <a name="advanced-hunting-using-powershell"></a><span data-ttu-id="a1f6e-104">Repérage avancé à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="a1f6e-104">Advanced Hunting using PowerShell</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="a1f6e-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="a1f6e-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

> <span data-ttu-id="a1f6e-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="a1f6e-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="a1f6e-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

<span data-ttu-id="a1f6e-108">Exécutez des requêtes avancées à l’aide de PowerShell, voir [API de recherche avancée.](run-advanced-query-api.md)</span><span class="sxs-lookup"><span data-stu-id="a1f6e-108">Run advanced queries using PowerShell, see [Advanced Hunting API](run-advanced-query-api.md).</span></span>

<span data-ttu-id="a1f6e-109">Dans cette section, nous partageons des exemples PowerShell pour récupérer un jeton et l’utiliser pour exécuter une requête.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-109">In this section, we share PowerShell samples to retrieve a token and use it to run a query.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="a1f6e-110">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a1f6e-110">Before you begin</span></span>
<span data-ttu-id="a1f6e-111">Vous devez d’abord [créer une application.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="a1f6e-111">You first need to [create an app](apis-intro.md).</span></span>

## <a name="preparation-instructions"></a><span data-ttu-id="a1f6e-112">Instructions de préparation</span><span class="sxs-lookup"><span data-stu-id="a1f6e-112">Preparation instructions</span></span>

- <span data-ttu-id="a1f6e-113">Ouvrez une fenêtre PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-113">Open a PowerShell window.</span></span>
- <span data-ttu-id="a1f6e-114">Si votre stratégie ne vous permet pas d’exécuter les commandes PowerShell, vous pouvez exécuter la commande ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="a1f6e-114">If your policy does not allow you to run the PowerShell commands, you can run the below command:</span></span>
  ```
  Set-ExecutionPolicy -ExecutionPolicy Bypass
  ```

><span data-ttu-id="a1f6e-115">Pour plus d’informations, [voir la documentation PowerShell](/powershell/module/microsoft.powershell.security/set-executionpolicy)</span><span class="sxs-lookup"><span data-stu-id="a1f6e-115">For more information, see [PowerShell documentation](/powershell/module/microsoft.powershell.security/set-executionpolicy)</span></span>

## <a name="get-token"></a><span data-ttu-id="a1f6e-116">Obtenir un jeton</span><span class="sxs-lookup"><span data-stu-id="a1f6e-116">Get token</span></span>

- <span data-ttu-id="a1f6e-117">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a1f6e-117">Run the following:</span></span>

```
$tenantId = '00000000-0000-0000-0000-000000000000' # Paste your own tenant ID here
$appId = '11111111-1111-1111-1111-111111111111' # Paste your own app ID here
$appSecret = '22222222-2222-2222-2222-222222222222' # Paste your own app secret here

$resourceAppIdUri = 'https://api.securitycenter.microsoft.com'
$oAuthUri = "https://login.microsoftonline.com/$TenantId/oauth2/token"
$body = [Ordered] @{
    resource = "$resourceAppIdUri"
    client_id = "$appId"
    client_secret = "$appSecret"
    grant_type = 'client_credentials'
}
$response = Invoke-RestMethod -Method Post -Uri $oAuthUri -Body $body -ErrorAction Stop
$aadToken = $response.access_token
```

<span data-ttu-id="a1f6e-118">where</span><span class="sxs-lookup"><span data-stu-id="a1f6e-118">where</span></span>
- <span data-ttu-id="a1f6e-119">$tenantId : ID du client pour le compte duquel vous souhaitez exécuter la requête (autrement dit, la requête sera exécuté sur les données de ce client)</span><span class="sxs-lookup"><span data-stu-id="a1f6e-119">$tenantId: ID of the tenant on behalf of which you want to run the query (that is, the query will be run on the data of this tenant)</span></span>
- <span data-ttu-id="a1f6e-120">$appId : ID de votre application Azure AD (l’application doit avoir l’autorisation « Exécuter des requêtes avancées » sur Defender for Endpoint)</span><span class="sxs-lookup"><span data-stu-id="a1f6e-120">$appId: ID of your Azure AD app (the app must have 'Run advanced queries' permission to Defender for Endpoint)</span></span>
- <span data-ttu-id="a1f6e-121">$appSecret : secret de votre application Azure AD</span><span class="sxs-lookup"><span data-stu-id="a1f6e-121">$appSecret: Secret of your Azure AD app</span></span>

## <a name="run-query"></a><span data-ttu-id="a1f6e-122">Exécuter la requête</span><span class="sxs-lookup"><span data-stu-id="a1f6e-122">Run query</span></span>

<span data-ttu-id="a1f6e-123">Exécutez la requête suivante :</span><span class="sxs-lookup"><span data-stu-id="a1f6e-123">Run the following query:</span></span>

```
$query = 'RegistryEvents | limit 10' # Paste your own query here

$url = "https://api.securitycenter.microsoft.com/api/advancedqueries/run"
$headers = @{ 
    'Content-Type' = 'application/json'
    Accept = 'application/json'
    Authorization = "Bearer $aadToken" 
}
$body = ConvertTo-Json -InputObject @{ 'Query' = $query }
$webResponse = Invoke-WebRequest -Method Post -Uri $url -Headers $headers -Body $body -ErrorAction Stop
$response =  $webResponse | ConvertFrom-Json
$results = $response.Results
$schema = $response.Schema
```

- <span data-ttu-id="a1f6e-124">$results contiennent les résultats de votre requête</span><span class="sxs-lookup"><span data-stu-id="a1f6e-124">$results contain the results of your query</span></span>
- <span data-ttu-id="a1f6e-125">$schema contient le schéma des résultats de votre requête</span><span class="sxs-lookup"><span data-stu-id="a1f6e-125">$schema contains the schema of the results of your query</span></span>

### <a name="complex-queries"></a><span data-ttu-id="a1f6e-126">Requêtes complexes</span><span class="sxs-lookup"><span data-stu-id="a1f6e-126">Complex queries</span></span>

<span data-ttu-id="a1f6e-127">Si vous souhaitez exécuter des requêtes complexes (ou des requêtes multilignes), enregistrez votre requête dans un fichier et, au lieu de la première ligne de l’exemple ci-dessus, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a1f6e-127">If you want to run complex queries (or multilines queries), save your query in a file and, instead of the first line in the above sample, run the below command:</span></span>

```
$query = [IO.File]::ReadAllText("C:\myQuery.txt"); # Replace with the path to your file
```

## <a name="work-with-query-results"></a><span data-ttu-id="a1f6e-128">Travailler avec les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="a1f6e-128">Work with query results</span></span>

<span data-ttu-id="a1f6e-129">Vous pouvez désormais utiliser les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-129">You can now use the query results.</span></span>

<span data-ttu-id="a1f6e-130">Pour obtenir les résultats de la requête au format CSV dans un fichier, file1.csv ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="a1f6e-130">To output the results of the query in CSV format in file file1.csv do the below:</span></span>

```
$results | ConvertTo-Csv -NoTypeInformation | Set-Content file1.csv
```

<span data-ttu-id="a1f6e-131">Pour obtenir les résultats de la requête au format JSON au file1.jssur :</span><span class="sxs-lookup"><span data-stu-id="a1f6e-131">To output the results of the query in JSON format in file file1.json do the below:</span></span>

```
$results | ConvertTo-Json | Set-Content file1.json
```


## <a name="related-topic"></a><span data-ttu-id="a1f6e-132">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="a1f6e-132">Related topic</span></span>
- [<span data-ttu-id="a1f6e-133">API Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a1f6e-133">Microsoft Defender for Endpoint APIs</span></span>](apis-intro.md)
- [<span data-ttu-id="a1f6e-134">API de recherche avancée de menaces</span><span class="sxs-lookup"><span data-stu-id="a1f6e-134">Advanced Hunting API</span></span>](run-advanced-query-api.md)
- [<span data-ttu-id="a1f6e-135">Repérage avancé à l’aide de Python</span><span class="sxs-lookup"><span data-stu-id="a1f6e-135">Advanced Hunting using Python</span></span>](run-advanced-query-sample-python.md)
