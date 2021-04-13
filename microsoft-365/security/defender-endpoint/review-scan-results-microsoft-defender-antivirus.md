---
title: Passer en revue les résultats des analyses de l'Antivirus Microsoft Defender
description: Passer en revue les résultats des analyses à l'aide de Microsoft Endpoint Configuration Manager, Microsoft Intune ou l'application sécurité Windows
keywords: résultats de l'analyse, correction, analyse complète, analyse rapide
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
ms.localizationpriority: medium
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 09/28/2020
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 8fe2810ce18589d3131aa17f25ccfb01ec26b892
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51690570"
---
# <a name="review-microsoft-defender-antivirus-scan-results"></a><span data-ttu-id="f07a1-104">Passer en revue les résultats de l'analyse de l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="f07a1-104">Review Microsoft Defender Antivirus scan results</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="f07a1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f07a1-105">**Applies to:**</span></span>

- [<span data-ttu-id="f07a1-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f07a1-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="f07a1-107">Une fois l'analyse de l'Antivirus [](run-scan-microsoft-defender-antivirus.md) Microsoft Defender terminée, qu'il s'agit d'une analyse à la demande ou d'une analyse [programmée,](scheduled-catch-up-scans-microsoft-defender-antivirus.md)les résultats sont enregistrés et vous pouvez afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="f07a1-107">After a Microsoft Defender Antivirus scan completes, whether it is an [on-demand](run-scan-microsoft-defender-antivirus.md) or [scheduled scan](scheduled-catch-up-scans-microsoft-defender-antivirus.md), the results are recorded and you can view the results.</span></span> 


## <a name="use-configuration-manager-to-review-scan-results"></a><span data-ttu-id="f07a1-108">Utiliser Configuration Manager pour passer en revue les résultats de l'analyse</span><span class="sxs-lookup"><span data-stu-id="f07a1-108">Use Configuration Manager to review scan results</span></span>

<span data-ttu-id="f07a1-109">Découvrez [comment surveiller l'état de Endpoint Protection.](/configmgr/protect/deploy-use/monitor-endpoint-protection)</span><span class="sxs-lookup"><span data-stu-id="f07a1-109">See [How to monitor Endpoint Protection status](/configmgr/protect/deploy-use/monitor-endpoint-protection).</span></span>

## <a name="use-powershell-cmdlets-to-review-scan-results"></a><span data-ttu-id="f07a1-110">Utiliser les cmdlets PowerShell pour passer en revue les résultats de l'analyse</span><span class="sxs-lookup"><span data-stu-id="f07a1-110">Use PowerShell cmdlets to review scan results</span></span>

<span data-ttu-id="f07a1-111">L'cmdlet suivante retourne chaque détection sur le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f07a1-111">The following cmdlet will return each detection on the endpoint.</span></span> <span data-ttu-id="f07a1-112">S'il existe plusieurs détections de la même menace, chaque détection est répertoriée séparément, en fonction de l'heure de chaque détection :</span><span class="sxs-lookup"><span data-stu-id="f07a1-112">If there are multiple detections of the same threat, each detection will be listed separately, based on the time of each detection:</span></span>

```PowerShell
Get-MpThreatDetection
```

![Capture d'écran des cmdlets et sorties PowerShell](images/defender/wdav-get-mpthreatdetection.png)

<span data-ttu-id="f07a1-114">Vous pouvez `-ThreatID` spécifier de limiter la sortie pour afficher uniquement les détections d'une menace spécifique.</span><span class="sxs-lookup"><span data-stu-id="f07a1-114">You can specify `-ThreatID` to limit the output to only show the detections for a specific threat.</span></span>

<span data-ttu-id="f07a1-115">Si vous souhaitez lister les détections de menaces, mais combiner les détections de la même menace en un seul élément, vous pouvez utiliser la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="f07a1-115">If you want to list threat detections, but combine detections of the same threat into a single item, you can use the following cmdlet:</span></span>

```PowerShell
Get-MpThreat
```

![Capture d'écran de PowerShell](images/defender/wdav-get-mpthreat.png)

<span data-ttu-id="f07a1-117">Pour [plus d'informations](use-powershell-cmdlets-microsoft-defender-antivirus.md) sur l'utilisation de PowerShell avec l'Antivirus Microsoft Defender, voir les cmdlets Utiliser PowerShell pour configurer et exécuter les [cmdlets](/powershell/module/defender/) Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="f07a1-117">See [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

## <a name="use-windows-management-instruction-wmi-to-review-scan-results"></a><span data-ttu-id="f07a1-118">Utiliser Windows Management Instruction (WMI) pour passer en revue les résultats de l'analyse</span><span class="sxs-lookup"><span data-stu-id="f07a1-118">Use Windows Management Instruction (WMI) to review scan results</span></span>

<span data-ttu-id="f07a1-119">Utilisez la [ **méthode Get** des **classes MSFT_MpThreat** et **MSFT_MpThreatDetection**](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal) classes.</span><span class="sxs-lookup"><span data-stu-id="f07a1-119">Use the [**Get** method of the **MSFT_MpThreat** and **MSFT_MpThreatDetection**](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal) classes.</span></span>


## <a name="related-articles"></a><span data-ttu-id="f07a1-120">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="f07a1-120">Related articles</span></span>

- [<span data-ttu-id="f07a1-121">Personnaliser, lancer et passer en revue les résultats des analyses et des corrections de l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="f07a1-121">Customize, initiate, and review the results of Microsoft Defender Antivirus scans and remediation</span></span>](customize-run-review-remediate-scans-microsoft-defender-antivirus.md)
- [<span data-ttu-id="f07a1-122">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="f07a1-122">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)