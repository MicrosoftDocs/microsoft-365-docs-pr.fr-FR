---
title: Planifier des analyses antivirus à l’aide de PowerShell
description: Planifier des analyses antivirus à l’aide de PowerShell
keywords: analyse rapide, analyse complète, antivirus, planification, PowerShell
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 06/09/2021
ms.reviewer: pauhijbr, ksarens
manager: dansimp
ms.technology: mde
ms.topic: how-to
ms.openlocfilehash: 73ba654dd312c63651f0cf43244796e94e8ad55b
ms.sourcegitcommit: 337e8d8a2fee112d799edd8a0e04b3a2f124f900
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "52879675"
---
# <a name="schedule-antivirus-scans-using-powershell"></a><span data-ttu-id="8738b-104">Planifier des analyses antivirus à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="8738b-104">Schedule antivirus scans using PowerShell</span></span>

<span data-ttu-id="8738b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8738b-105">**Applies to:**</span></span>

- [<span data-ttu-id="8738b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8738b-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="8738b-107">Cet article explique comment configurer des analyses programmées à l’aide des cmdlets PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8738b-107">This article describes how to configure scheduled scans using PowerShell cmdlets.</span></span> <span data-ttu-id="8738b-108">Pour en savoir plus sur la planification des analyses et sur les types d’analyse, voir Configurer des analyses rapides ou [complètes Antivirus Microsoft Defender planification.](schedule-antivirus-scans.md)</span><span class="sxs-lookup"><span data-stu-id="8738b-108">To learn more about scheduling scans and about scan types, see [Configure scheduled quick or full Microsoft Defender Antivirus scans](schedule-antivirus-scans.md).</span></span> 

## <a name="use-powershell-cmdlets-to-schedule-scans"></a><span data-ttu-id="8738b-109">Utiliser les cmdlets PowerShell pour planifier des analyses</span><span class="sxs-lookup"><span data-stu-id="8738b-109">Use PowerShell cmdlets to schedule scans</span></span>

<span data-ttu-id="8738b-110">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="8738b-110">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -ScanParameters
Set-MpPreference -ScanScheduleDay
Set-MpPreference -ScanScheduleTime
Set-MpPreference -RandomizeScheduleTaskTimes

```

<span data-ttu-id="8738b-111">Pour plus d’informations, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender/) Antivirus Microsoft Defender et Defender pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="8738b-111">For more information, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

## <a name="powershell-cmdlets-for-scheduling-scans-when-an-endpoint-is-not-in-use"></a><span data-ttu-id="8738b-112">Cmdlets PowerShell pour la planification des analyses lorsqu’un point de terminaison n’est pas utilisé</span><span class="sxs-lookup"><span data-stu-id="8738b-112">PowerShell cmdlets for scheduling scans when an endpoint is not in use</span></span>

<span data-ttu-id="8738b-113">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="8738b-113">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -ScanOnlyIfIdleEnabled
```

<span data-ttu-id="8738b-114">Pour plus d’informations, voir [Utiliser les cmdlets PowerShell pour configurer et gérer l'Antivirus Microsoft Defender](use-powershell-cmdlets-microsoft-defender-antivirus.md) et [Cmdlets Defender](/powershell/module/defender/).</span><span class="sxs-lookup"><span data-stu-id="8738b-114">For more information, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/).</span></span>

> [!NOTE]
> <span data-ttu-id="8738b-115">Lorsque vous programmez des analyses à des moments où les points de terminaison ne sont pas utilisés, les analyses ne respectent pas la configuration de limitation du processeur et tirez pleinement parti des ressources disponibles pour effectuer l’analyse aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="8738b-115">When you schedule scans for times when endpoints are not in use, scans do not honor the CPU throttling configuration and will take full advantage of the resources available to complete the scan as fast as possible.</span></span>

## <a name="powershell-cmdlets-for-scheduling-scans-to-complete-remediation"></a><span data-ttu-id="8738b-116">Cmdlets PowerShell pour la planification des analyses afin de terminer la correction</span><span class="sxs-lookup"><span data-stu-id="8738b-116">PowerShell cmdlets for scheduling scans to complete remediation</span></span>

<span data-ttu-id="8738b-117">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="8738b-117">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -RemediationScheduleDay
Set-MpPreference -RemediationScheduleTime
```

<span data-ttu-id="8738b-118">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender/) Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="8738b-118">See [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

## <a name="powershell-cmdlets-for-scheduling-daily-scans"></a><span data-ttu-id="8738b-119">Cmdlets PowerShell pour la planification des analyses quotidiennes</span><span class="sxs-lookup"><span data-stu-id="8738b-119">PowerShell cmdlets for scheduling daily scans</span></span>

<span data-ttu-id="8738b-120">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="8738b-120">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -ScanScheduleQuickScanTime
```

<span data-ttu-id="8738b-121">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender/)Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="8738b-121">For more information about how to use PowerShell with Microsoft Defender Antivirus, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/).</span></span>


