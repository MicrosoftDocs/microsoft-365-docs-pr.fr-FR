---
title: Planifier des analyses antivirus à l’aide Windows Management Instrumentation
description: Planifier des analyses antivirus à l’aide de WMI
keywords: analyse rapide, analyse complète, WMI, planification, antivirus
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
ms.openlocfilehash: 1aa174f4601fb57eebbc4fb7c78e1809b9f072c8
ms.sourcegitcommit: 337e8d8a2fee112d799edd8a0e04b3a2f124f900
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "52879674"
---
# <a name="schedule-antivirus-scans-using-windows-management-instrumentation-wmi"></a><span data-ttu-id="fd30f-104">Planifier des analyses antivirus à l’aide Windows Management Instrumentation (WMI)</span><span class="sxs-lookup"><span data-stu-id="fd30f-104">Schedule antivirus scans using Windows Management Instrumentation (WMI)</span></span>

<span data-ttu-id="fd30f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="fd30f-105">**Applies to:**</span></span>

- [<span data-ttu-id="fd30f-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fd30f-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="fd30f-107">Cet article explique comment configurer des analyses programmées à l’aide de WMI.</span><span class="sxs-lookup"><span data-stu-id="fd30f-107">This article describes how to configure scheduled scans using WMI.</span></span> <span data-ttu-id="fd30f-108">Pour en savoir plus sur la planification des analyses et sur les types d’analyse, voir Configurer des analyses rapides ou [complètes Antivirus Microsoft Defender planification.](schedule-antivirus-scans.md)</span><span class="sxs-lookup"><span data-stu-id="fd30f-108">To learn more about scheduling scans and about scan types, see [Configure scheduled quick or full Microsoft Defender Antivirus scans](schedule-antivirus-scans.md).</span></span> 

## <a name="use-windows-management-instruction-wmi-to-schedule-scans"></a><span data-ttu-id="fd30f-109">Utiliser Windows Management Instruction (WMI) pour planifier des analyses</span><span class="sxs-lookup"><span data-stu-id="fd30f-109">Use Windows Management Instruction (WMI) to schedule scans</span></span>

<span data-ttu-id="fd30f-110">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd30f-110">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
ScanParameters
ScanScheduleDay
ScanScheduleTime
RandomizeScheduleTaskTimes
```

<span data-ttu-id="fd30f-111">Pour plus d’informations et les paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="fd30f-111">For more information and allowed parameters, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span></span>

## <a name="wmi-for-scheduling-scans-when-an-endpoint-is-not-in-use"></a><span data-ttu-id="fd30f-112">WMI pour la planification des analyses lorsqu’un point de terminaison n’est pas utilisé</span><span class="sxs-lookup"><span data-stu-id="fd30f-112">WMI for scheduling scans when an endpoint is not in use</span></span>

<span data-ttu-id="fd30f-113">Utilisez la [méthode Set de la classe MSFT_MpPreference pour](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd30f-113">Use the [Set method of the MSFT_MpPreference class](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) for the following properties:</span></span>

```WMI
ScanOnlyIfIdleEnabled
```

<span data-ttu-id="fd30f-114">Pour plus d’informations sur les API et les paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span><span class="sxs-lookup"><span data-stu-id="fd30f-114">For more information about APIs and allowed parameters, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span></span>

> [!NOTE]
> <span data-ttu-id="fd30f-115">Lorsque vous programmez des analyses à des moments où les points de terminaison ne sont pas utilisés, les analyses ne respectent pas la configuration de limitation du processeur et tirez pleinement parti des ressources disponibles pour effectuer l’analyse aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="fd30f-115">When you schedule scans for times when endpoints are not in use, scans do not honor the CPU throttling configuration and will take full advantage of the resources available to complete the scan as fast as possible.</span></span>


## <a name="wmi-for-scheduling-scans-to-complete-remediation"></a><span data-ttu-id="fd30f-116">WMI pour la planification des analyses afin de terminer la correction</span><span class="sxs-lookup"><span data-stu-id="fd30f-116">WMI for scheduling scans to complete remediation</span></span>

<span data-ttu-id="fd30f-117">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd30f-117">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
RemediationScheduleDay
RemediationScheduleTime
```

<span data-ttu-id="fd30f-118">Pour plus d’informations et les paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span><span class="sxs-lookup"><span data-stu-id="fd30f-118">For more information and allowed parameters, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span></span>

## <a name="wmi-for-scheduling-daily-scans"></a><span data-ttu-id="fd30f-119">WMI pour la planification des analyses quotidiennes</span><span class="sxs-lookup"><span data-stu-id="fd30f-119">WMI for scheduling daily scans</span></span>

<span data-ttu-id="fd30f-120">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd30f-120">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
ScanScheduleQuickScanTime
```

<span data-ttu-id="fd30f-121">Pour plus d’informations et les paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span><span class="sxs-lookup"><span data-stu-id="fd30f-121">For more information and allowed parameters, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span></span>

