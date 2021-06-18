---
title: Passer en revue les résultats des analyses de l’Antivirus Microsoft Defender
description: Passer en revue les résultats des analyses à l’aide Microsoft Endpoint Configuration Manager, Microsoft Intune ou l’Sécurité Windows de données
keywords: résultats de l’analyse, correction, analyse complète, analyse rapide
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 06/17/2021
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.topic: article
ms.openlocfilehash: bc7c84e089b08c440512f8a8bf7583f41394f2ca
ms.sourcegitcommit: bbad1938b6661d4a6bca99f235c44e521b1fb662
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2021
ms.locfileid: "53007629"
---
# <a name="review-microsoft-defender-antivirus-scan-results"></a><span data-ttu-id="ca7a8-104">Passer en Antivirus Microsoft Defender résultats d’analyse</span><span class="sxs-lookup"><span data-stu-id="ca7a8-104">Review Microsoft Defender Antivirus scan results</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="ca7a8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ca7a8-105">**Applies to:**</span></span>

- [<span data-ttu-id="ca7a8-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ca7a8-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="ca7a8-107">Une fois Antivirus Microsoft Defender analyse complète, qu’il s’agit d’une analyse à la demande ou d’une analyse [programmée,](scheduled-catch-up-scans-microsoft-defender-antivirus.md)les résultats sont enregistrés et vous pouvez afficher les résultats. [](run-scan-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="ca7a8-107">After a Microsoft Defender Antivirus scan completes, whether it is an [on-demand](run-scan-microsoft-defender-antivirus.md) or [scheduled scan](scheduled-catch-up-scans-microsoft-defender-antivirus.md), the results are recorded and you can view the results.</span></span> 


## <a name="use-configuration-manager-to-review-scan-results"></a><span data-ttu-id="ca7a8-108">Utiliser Configuration Manager pour passer en revue les résultats de l’analyse</span><span class="sxs-lookup"><span data-stu-id="ca7a8-108">Use Configuration Manager to review scan results</span></span>

<span data-ttu-id="ca7a8-109">Découvrez [comment surveiller l’état Endpoint Protection de l’ordinateur.](/configmgr/protect/deploy-use/monitor-endpoint-protection)</span><span class="sxs-lookup"><span data-stu-id="ca7a8-109">See [How to monitor Endpoint Protection status](/configmgr/protect/deploy-use/monitor-endpoint-protection).</span></span>

## <a name="use-powershell-cmdlets-to-review-scan-results"></a><span data-ttu-id="ca7a8-110">Utiliser les cmdlets PowerShell pour passer en revue les résultats de l’analyse</span><span class="sxs-lookup"><span data-stu-id="ca7a8-110">Use PowerShell cmdlets to review scan results</span></span>

<span data-ttu-id="ca7a8-111">L’cmdlet suivante retourne chaque détection sur le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ca7a8-111">The following cmdlet will return each detection on the endpoint.</span></span> <span data-ttu-id="ca7a8-112">S’il existe plusieurs détections de la même menace, chaque détection est répertoriée séparément, en fonction de l’heure de chaque détection :</span><span class="sxs-lookup"><span data-stu-id="ca7a8-112">If there are multiple detections of the same threat, each detection will be listed separately, based on the time of each detection:</span></span>

```PowerShell
Get-MpThreatDetection
```

:::image type="content" source="../../media/wdav-get-mpthreatdetection.png" alt-text="Capture d’écran des cmdlets et sorties PowerShell":::

<span data-ttu-id="ca7a8-114">Vous pouvez `-ThreatID` spécifier de limiter la sortie pour afficher uniquement les détections d’une menace spécifique.</span><span class="sxs-lookup"><span data-stu-id="ca7a8-114">You can specify `-ThreatID` to limit the output to only show the detections for a specific threat.</span></span>

<span data-ttu-id="ca7a8-115">Si vous souhaitez lister les détections de menaces, mais combiner les détections de la même menace en un seul élément, vous pouvez utiliser la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="ca7a8-115">If you want to list threat detections, but combine detections of the same threat into a single item, you can use the following cmdlet:</span></span>

```PowerShell
Get-MpThreat
```

:::image type="content" source="../../media/wdav-get-mpthreat.png" alt-text="Code PowerShell":::

<span data-ttu-id="ca7a8-117">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender/) Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="ca7a8-117">See [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

## <a name="use-windows-management-instruction-wmi-to-review-scan-results"></a><span data-ttu-id="ca7a8-118">Utiliser Windows Management Instruction (WMI) pour passer en revue les résultats de l’analyse</span><span class="sxs-lookup"><span data-stu-id="ca7a8-118">Use Windows Management Instruction (WMI) to review scan results</span></span>

<span data-ttu-id="ca7a8-119">Utilisez la [ **méthode Get** des **classes MSFT_MpThreat** et **MSFT_MpThreatDetection**](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal) classes.</span><span class="sxs-lookup"><span data-stu-id="ca7a8-119">Use the [**Get** method of the **MSFT_MpThreat** and **MSFT_MpThreatDetection**](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal) classes.</span></span>


## <a name="related-articles"></a><span data-ttu-id="ca7a8-120">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="ca7a8-120">Related articles</span></span>

- [<span data-ttu-id="ca7a8-121">Personnaliser, lancer et passer en revue les résultats des analyses et Antivirus Microsoft Defender correction</span><span class="sxs-lookup"><span data-stu-id="ca7a8-121">Customize, initiate, and review the results of Microsoft Defender Antivirus scans and remediation</span></span>](customize-run-review-remediate-scans-microsoft-defender-antivirus.md)
- [<span data-ttu-id="ca7a8-122">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="ca7a8-122">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)