---
title: Guide de l’API de recherche avancée avec PowerShell
ms.reviewer: ''
description: Utilisez ces exemples de code, interrogeant plusieurs API de point de terminaison Microsoft Defender.
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
ms.date: 09/24/2018
ms.technology: mde
ms.openlocfilehash: ef6d05bb27018bb72f731da2e8b7837c9d9f0127
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52842061"
---
# <a name="microsoft-defender-for-endpoint-apis-using-powershell"></a><span data-ttu-id="50339-104">API Microsoft Defender pour point de terminaison à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="50339-104">Microsoft Defender for Endpoint APIs using PowerShell</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="50339-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="50339-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

> <span data-ttu-id="50339-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="50339-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="50339-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="50339-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

><span data-ttu-id="50339-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="50339-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="50339-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="50339-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-enablesiem-abovefoldlink)

<span data-ttu-id="50339-110">Scénario complet utilisant plusieurs API de Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="50339-110">Full scenario using multiple APIs from Microsoft Defender for Endpoint.</span></span>

<span data-ttu-id="50339-111">Dans cette section, nous partageons des exemples PowerShell pour</span><span class="sxs-lookup"><span data-stu-id="50339-111">In this section, we share PowerShell samples to</span></span> 
- <span data-ttu-id="50339-112">Récupérer un jeton</span><span class="sxs-lookup"><span data-stu-id="50339-112">Retrieve a token</span></span> 
- <span data-ttu-id="50339-113">Utiliser un jeton pour récupérer les dernières alertes dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="50339-113">Use token to retrieve the latest alerts in Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="50339-114">Pour chaque alerte, si l’alerte a une priorité moyenne ou élevée et est toujours en cours, vérifiez combien de fois l’appareil s’est connecté à une URL suspecte.</span><span class="sxs-lookup"><span data-stu-id="50339-114">For each alert, if the alert has medium or high priority and is still in progress, check how many times the device has connected to suspicious URL.</span></span>

<span data-ttu-id="50339-115">**Conditions préalables**: vous devez d’abord [créer une application.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="50339-115">**Prerequisite**: You first need to [create an app](apis-intro.md).</span></span>

## <a name="preparation-instructions"></a><span data-ttu-id="50339-116">Instructions de préparation</span><span class="sxs-lookup"><span data-stu-id="50339-116">Preparation instructions</span></span>

- <span data-ttu-id="50339-117">Ouvrez une fenêtre PowerShell.</span><span class="sxs-lookup"><span data-stu-id="50339-117">Open a PowerShell window.</span></span>
- <span data-ttu-id="50339-118">Si votre stratégie ne vous permet pas d’exécuter les commandes PowerShell, vous pouvez exécuter la commande ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="50339-118">If your policy does not allow you to run the PowerShell commands, you can run the below command:</span></span>
  ```
  Set-ExecutionPolicy -ExecutionPolicy Bypass
  ```

<span data-ttu-id="50339-119">Pour plus d’informations, [voir la documentation PowerShell](/powershell/module/microsoft.powershell.security/set-executionpolicy)</span><span class="sxs-lookup"><span data-stu-id="50339-119">For more information, see [PowerShell documentation](/powershell/module/microsoft.powershell.security/set-executionpolicy)</span></span>

## <a name="get-token"></a><span data-ttu-id="50339-120">Obtenir un jeton</span><span class="sxs-lookup"><span data-stu-id="50339-120">Get token</span></span>

<span data-ttu-id="50339-121">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="50339-121">Run the below:</span></span>

- <span data-ttu-id="50339-122">$tenantId : ID du client pour le compte duquel vous souhaitez exécuter la requête (c’est-à-dire, la requête sera exécuté sur les données de ce client)</span><span class="sxs-lookup"><span data-stu-id="50339-122">$tenantId: ID of the tenant on behalf of which you want to run the query (i.e., the query will be run on the data of this tenant)</span></span>
- <span data-ttu-id="50339-123">$appId : ID de votre application AAD (l’application doit avoir l’autorisation « Exécuter des requêtes avancées » sur Defender pour le point de terminaison)</span><span class="sxs-lookup"><span data-stu-id="50339-123">$appId: ID of your AAD app (the app must have 'Run advanced queries' permission to Defender for Endpoint)</span></span>
- <span data-ttu-id="50339-124">$appSecret : secret de votre application Azure AD</span><span class="sxs-lookup"><span data-stu-id="50339-124">$appSecret: Secret of your Azure AD app</span></span>

- <span data-ttu-id="50339-125">$suspiciousUrl : URL</span><span class="sxs-lookup"><span data-stu-id="50339-125">$suspiciousUrl: The URL</span></span>


```
$tenantId = '00000000-0000-0000-0000-000000000000' # Paste your own tenant ID here
$appId = '11111111-1111-1111-1111-111111111111' # Paste your own app ID here
$appSecret = '22222222-2222-2222-2222-222222222222' # Paste your own app secret here
$suspiciousUrl = 'www.suspiciousUrl.com' # Paste your own URL here

$resourceAppIdUri = 'https://securitycenter.onmicrosoft.com/windowsatpservice'
$oAuthUri = "https://login.microsoftonline.com/$TenantId/oauth2/token"
$authBody = [Ordered] @{
    resource = "$resourceAppIdUri"
    client_id = "$appId"
    client_secret = "$appSecret"
    grant_type = 'client_credentials'
}
$authResponse = Invoke-RestMethod -Method Post -Uri $oAuthUri -Body $authBody -ErrorAction Stop
$aadToken = $authResponse.access_token


#Get latest alert
$alertUrl = "https://api.securitycenter.microsoft.com/api/alerts?`$top=10"
$headers = @{ 
    'Content-Type' = 'application/json'
    Accept = 'application/json'
    Authorization = "Bearer $aadToken" 
}
$alertResponse = Invoke-WebRequest -Method Get -Uri $alertUrl -Headers $headers -ErrorAction Stop
$alerts =  ($alertResponse | ConvertFrom-Json).value

$machinesToInvestigate = New-Object System.Collections.ArrayList

Foreach($alert in $alerts)
{
    #echo $alert.id $alert.machineId    $alert.severity $alert.status

    $isSevereAlert = $alert.severity -in 'Medium', 'High'
    $isOpenAlert = $alert.status -in 'InProgress', 'New'
    if($isOpenAlert -and $isSevereAlert)
    {
        if (-not $machinesToInvestigate.Contains($alert.machineId))
        {
            $machinesToInvestigate.Add($alert.machineId) > $null
        }
    }
}

$commaSeparatedMachines = '"{0}"' -f ($machinesToInvestigate -join '","')

$query = "NetworkCommunicationEvents
| where MachineId in ($commaSeparatedMachines)
| where RemoteUrl  == `"$suspiciousUrl`"
| summarize ConnectionsCount = count() by MachineId"

$queryUrl = "https://api.securitycenter.microsoft.com/api/advancedqueries/run"

$queryBody = ConvertTo-Json -InputObject @{ 'Query' = $query }
$queryResponse = Invoke-WebRequest -Method Post -Uri $queryUrl -Headers $headers -Body $queryBody -ErrorAction Stop
$response =  ($queryResponse | ConvertFrom-Json).Results
$response
```


## <a name="see-also"></a><span data-ttu-id="50339-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50339-126">See also</span></span>
- [<span data-ttu-id="50339-127">API Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="50339-127">Microsoft Defender for Endpoint APIs</span></span>](apis-intro.md)
- [<span data-ttu-id="50339-128">API de recherche avancée de menaces</span><span class="sxs-lookup"><span data-stu-id="50339-128">Advanced Hunting API</span></span>](run-advanced-query-api.md)
- [<span data-ttu-id="50339-129">Repérage avancé à l’aide de Python</span><span class="sxs-lookup"><span data-stu-id="50339-129">Advanced Hunting using Python</span></span>](run-advanced-query-sample-python.md)
