---
title: Surveiller et signaler la protection antivirus Microsoft Defender
description: Utilisez Configuration Manager ou les outils de gestion des informations et des événements de sécurité (SIEM) pour utiliser des rapports et surveiller Microsoft Defender AV avec PowerShell et WMI.
keywords: siem, monitor, report, Microsoft Defender AV
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
ms.localizationpriority: medium
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 12/07/2020
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: f0065792f525827ccd1471087b8a707989ef61ef
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51690699"
---
# <a name="report-on-microsoft-defender-antivirus"></a><span data-ttu-id="db812-104">Rapport sur l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="db812-104">Report on Microsoft Defender Antivirus</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="db812-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="db812-105">**Applies to:**</span></span>

- [<span data-ttu-id="db812-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="db812-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="db812-107">L'Antivirus Microsoft Defender est intégré à Windows 10, Windows Server 2019 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="db812-107">Microsoft Defender Antivirus is built into Windows 10, Windows Server 2019, and Windows Server 2016.</span></span> <span data-ttu-id="db812-108">L'Antivirus Microsoft Defender est de votre nouvelle génération de protection dans Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="db812-108">Microsoft Defender Antivirus is of your next-generation protection in Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="db812-109">La protection nouvelle génération permet de protéger vos appareils contre les menaces logicielles telles que les virus, les programmes malveillants et les logiciels espions dans le courrier électronique, les applications, le cloud et le web.</span><span class="sxs-lookup"><span data-stu-id="db812-109">Next-generation protection helps protect your devices from software threats like viruses, malware, and spyware across email, apps, the cloud, and the web.</span></span>

<span data-ttu-id="db812-110">Avec l'Antivirus Microsoft Defender, vous avez plusieurs options pour passer en revue l'état et les alertes de la protection.</span><span class="sxs-lookup"><span data-stu-id="db812-110">With Microsoft Defender Antivirus, you have several options for reviewing protection status and alerts.</span></span> <span data-ttu-id="db812-111">Vous pouvez utiliser Microsoft Endpoint Manager pour surveiller [l'Antivirus Microsoft Defender](/configmgr/protect/deploy-use/monitor-endpoint-protection) ou [créer des alertes par courrier électronique.](/configmgr/protect/deploy-use/endpoint-configure-alerts)</span><span class="sxs-lookup"><span data-stu-id="db812-111">You can use Microsoft Endpoint Manager to [monitor Microsoft Defender Antivirus](/configmgr/protect/deploy-use/monitor-endpoint-protection) or [create email alerts](/configmgr/protect/deploy-use/endpoint-configure-alerts).</span></span> <span data-ttu-id="db812-112">Vous pouvez également surveiller la protection à [l'aide de Microsoft Intune.](/intune/introduction-intune)</span><span class="sxs-lookup"><span data-stu-id="db812-112">Or, you can monitor protection using [Microsoft Intune](/intune/introduction-intune).</span></span>  

<span data-ttu-id="db812-113">Microsoft Operations Management [](/windows/deployment/update/update-compliance-get-started) Suite dispose d'un module de conformité des mises à jour qui signale les principaux problèmes de l'Antivirus Microsoft Defender, notamment les mises à jour de protection et les paramètres de protection en temps réel.</span><span class="sxs-lookup"><span data-stu-id="db812-113">Microsoft Operations Management Suite has an [Update Compliance add-in](/windows/deployment/update/update-compliance-get-started) that reports on key Microsoft Defender Antivirus issues, including protection updates and real-time protection settings.</span></span>

<span data-ttu-id="db812-114">Si vous avez un serveur tiers d'informations sur la sécurité et de gestion des événements (SIEM), vous pouvez également utiliser Windows Defender [événements clients .](/windows/win32/events/windows-events)</span><span class="sxs-lookup"><span data-stu-id="db812-114">If you have a third-party security information and event management (SIEM) server, you can also consume [Windows Defender client events](/windows/win32/events/windows-events).</span></span> 

<span data-ttu-id="db812-115">Les événements Windows comprennent plusieurs sources d'événements de sécurité, y compris [](/windows/device-security/auditing/security-auditing-overview) les événements SAM (Security Account Manager) ( améliorés pour[Windows 10](/windows/whats-new/whats-new-windows-10-version-1507-and-1511), voir également la rubrique Audit de sécurité) et les [Windows Defender événements .](troubleshoot-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="db812-115">Windows events comprise several security event sources, including Security Account Manager (SAM) events ([enhanced for Windows 10](/windows/whats-new/whats-new-windows-10-version-1507-and-1511), also see the [Security auditing](/windows/device-security/auditing/security-auditing-overview) topic) and  [Windows Defender events](troubleshoot-microsoft-defender-antivirus.md).</span></span> 

<span data-ttu-id="db812-116">Ces événements peuvent être regroupés de manière centralisée à l'aide du [collecteur d'événements Windows.](/windows/win32/wec/windows-event-collector)</span><span class="sxs-lookup"><span data-stu-id="db812-116">These events can be centrally aggregated using the [Windows event collector](/windows/win32/wec/windows-event-collector).</span></span> <span data-ttu-id="db812-117">Souvent, les serveurs SIEM ont des connecteurs pour les événements Windows, ce qui vous permet de corréler tous les événements de sécurité dans votre serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="db812-117">Often, SIEM servers have connectors for Windows events, allowing you to correlate all security events in your SIEM server.</span></span> 

<span data-ttu-id="db812-118">Vous pouvez également surveiller les événements de programmes malveillants à [l'aide de la solution d'évaluation des programmes malveillants dans Log Analytics.](/azure/log-analytics/log-analytics-malware)</span><span class="sxs-lookup"><span data-stu-id="db812-118">You can also [monitor malware events using the Malware Assessment solution in Log Analytics](/azure/log-analytics/log-analytics-malware).</span></span>

<span data-ttu-id="db812-119">Pour surveiller ou déterminer l'état avec PowerShell, WMI ou Microsoft Azure, consultez [le tableau (Options](deploy-manage-report-microsoft-defender-antivirus.md#ref2)de déploiement, de gestion et de rapport).</span><span class="sxs-lookup"><span data-stu-id="db812-119">For monitoring or determining status with PowerShell, WMI, or Microsoft Azure, see the [(Deployment, management, and reporting options table)](deploy-manage-report-microsoft-defender-antivirus.md#ref2).</span></span>

## <a name="related-articles"></a><span data-ttu-id="db812-120">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="db812-120">Related articles</span></span>

- [<span data-ttu-id="db812-121">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="db812-121">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="db812-122">Antivirus Microsoft Defender sur Windows Server 2016 et 2019</span><span class="sxs-lookup"><span data-stu-id="db812-122">Microsoft Defender Antivirus on Windows Server 2016 and 2019</span></span>](microsoft-defender-antivirus-on-windows-server.md)
- [<span data-ttu-id="db812-123">Déployer l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="db812-123">Deploy Microsoft Defender Antivirus</span></span>](deploy-manage-report-microsoft-defender-antivirus.md)