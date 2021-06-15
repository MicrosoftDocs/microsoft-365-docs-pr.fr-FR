---
title: Exécuter et personnaliser des analyses à la demande dans Antivirus Microsoft Defender
description: Exécuter et configurer des analyses à la demande à l’aide de PowerShell, Windows Management Instrumentation ou individuellement sur les points de terminaison avec l Sécurité Windows app.
keywords: analyse, à la demande, dos, intune, analyse instantanée
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: normal
ms.topic: article
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 06/10/2021
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: b2910f9fe1c49178b8696d1a421248156b0fc4c2
ms.sourcegitcommit: be929f79751c0c52dfa6bd98a854432a0c63faf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52925730"
---
# <a name="configure-and-run-on-demand-microsoft-defender-antivirus-scans"></a><span data-ttu-id="0b3a1-104">Configurer et exécuter des analyses à la demande avec l’antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-104">Configure and run on-demand Microsoft Defender Antivirus scans</span></span>

<span data-ttu-id="0b3a1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0b3a1-105">**Applies to:**</span></span>

- [<span data-ttu-id="0b3a1-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0b3a1-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="0b3a1-107">Vous pouvez exécuter une analyse à la demande sur des points de terminaison individuels.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-107">You can run an on-demand scan on individual endpoints.</span></span> <span data-ttu-id="0b3a1-108">Ces analyses démarrent immédiatement et vous pouvez définir des paramètres pour l’analyse, tels que l’emplacement ou le type.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-108">These scans will start immediately, and you can define parameters for the scan, such as the location or type.</span></span> <span data-ttu-id="0b3a1-109">Lorsque vous exécutez une analyse, vous pouvez choisir parmi trois types : analyse rapide, analyse complète et analyse personnalisée.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-109">When you run a scan, you can choose from among three types: Quick scan, full scan, and custom scan.</span></span> <span data-ttu-id="0b3a1-110">Dans la plupart des cas, utilisez une analyse rapide.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-110">In most cases, use a quick scan.</span></span> <span data-ttu-id="0b3a1-111">Une analyse rapide examine tous les emplacements où des programmes malveillants peuvent être enregistrés pour démarrer avec le système, tels que les clés de Registre et les dossiers de démarrage Windows connus.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-111">A quick scan looks at all the locations where there could be malware registered to start with the system, such as registry keys and known Windows startup folders.</span></span> 

<span data-ttu-id="0b3a1-112">Combinée à une protection toujours en temps réel, qui examine les fichiers lorsqu’ils sont ouverts et fermés, et chaque fois qu’un utilisateur navigue vers un dossier, une analyse rapide permet de fournir une protection forte contre les programmes malveillants qui commencent par le système et les programmes malveillants au niveau du noyau.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-112">Combined with always-on, real-time protection, which reviews files when they are opened and closed, and whenever a user navigates to a folder, a quick scan helps provide strong protection against malware that starts with the system and kernel-level malware.</span></span> <span data-ttu-id="0b3a1-113">Dans la plupart des cas, une analyse rapide est suffisante et constitue l’option recommandée pour les analyses programmées ou à la demande.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-113">In most cases, a quick scan is sufficient and is the recommended option for scheduled or on-demand scans.</span></span>  <span data-ttu-id="0b3a1-114">[En savoir plus sur les types d’analyse.](schedule-antivirus-scans.md#quick-scan-full-scan-and-custom-scan)</span><span class="sxs-lookup"><span data-stu-id="0b3a1-114">[Learn more about scan types](schedule-antivirus-scans.md#quick-scan-full-scan-and-custom-scan).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b3a1-115">Antivirus Microsoft Defender s’exécute dans le contexte du [compte LocalSystem](/windows/win32/services/localsystem-account) lors de l’analyse locale.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-115">Microsoft Defender Antivirus runs in the context of the [LocalSystem](/windows/win32/services/localsystem-account) account when performing a local scan.</span></span> <span data-ttu-id="0b3a1-116">Pour les analyses réseau, il utilise le contexte du compte d’appareil.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-116">For network scans, it uses the context of the device account.</span></span> <span data-ttu-id="0b3a1-117">Si le compte d’appareil de domaine ne peut pas accéder au partage, l’analyse ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-117">If the domain device account doesn't have appropriate permissions to access the share, the scan won't work.</span></span> <span data-ttu-id="0b3a1-118">Assurez-vous que l’appareil dispose d’autorisations sur le partage réseau d’accès.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-118">Ensure that the device has permissions to the access network share.</span></span>

## <a name="use-microsoft-endpoint-manager-to-run-a-scan"></a><span data-ttu-id="0b3a1-119">Utiliser Microsoft Endpoint Manager pour exécuter une analyse</span><span class="sxs-lookup"><span data-stu-id="0b3a1-119">Use Microsoft Endpoint Manager to run a scan</span></span>

1. <span data-ttu-id="0b3a1-120">Go to the Microsoft Endpoint Manager admin center ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ) and log in.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-120">Go to the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and log in.</span></span>

2. <span data-ttu-id="0b3a1-121">Choisissez **l’Antivirus de sécurité des points de**  >  **terminaison.**</span><span class="sxs-lookup"><span data-stu-id="0b3a1-121">Choose **Endpoint security** > **Antivirus**.</span></span>

3. <span data-ttu-id="0b3a1-122">Dans la liste des onglets, sélectionnez Windows 10 points de **terminaison défectueux.**</span><span class="sxs-lookup"><span data-stu-id="0b3a1-122">In the list of tabs, select **Windows 10 unhealthy endpoints**.</span></span>

4. <span data-ttu-id="0b3a1-123">Dans la liste des actions fournies, sélectionnez **Analyse rapide** (recommandée) ou **Analyse complète.**</span><span class="sxs-lookup"><span data-stu-id="0b3a1-123">From the list of actions provided, select **Quick Scan** (recommended) or **Full Scan**.</span></span>

<span data-ttu-id="0b3a1-124">[![IMAGE ](images/mem-antivirus-scan-on-demand.png)](images/mem-antivirus-scan-on-demand.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="0b3a1-124">[ ![IMAGE](images/mem-antivirus-scan-on-demand.png) ](images/mem-antivirus-scan-on-demand.png#lightbox)</span></span>

> [!TIP]
> <span data-ttu-id="0b3a1-125">Pour plus d’informations sur l’utilisation Microsoft Endpoint Manager pour exécuter une analyse, voir [Tâches anti-programme](/configmgr/protect/deploy-use/endpoint-antimalware-firewall#how-to-perform-an-on-demand-scan-of-computers)malveillant et pare-feu : Comment effectuer une analyse à la demande .</span><span class="sxs-lookup"><span data-stu-id="0b3a1-125">For more information about using Microsoft Endpoint Manager to run a scan, see [Antimalware and firewall tasks: How to perform an on-demand scan](/configmgr/protect/deploy-use/endpoint-antimalware-firewall#how-to-perform-an-on-demand-scan-of-computers).</span></span>

## <a name="use-the-mpcmdrunexe-command-line-utility-to-run-a-scan"></a><span data-ttu-id="0b3a1-126">Utiliser lmpcmdrun.exe de ligne de commande pour exécuter une analyse</span><span class="sxs-lookup"><span data-stu-id="0b3a1-126">Use the mpcmdrun.exe command-line utility to run a scan</span></span>

<span data-ttu-id="0b3a1-127">Utilisez le paramètre `-scan` suivant :</span><span class="sxs-lookup"><span data-stu-id="0b3a1-127">Use the following `-scan` parameter:</span></span>

```console
mpcmdrun.exe -scan -scantype 1
```

<span data-ttu-id="0b3a1-128">Pour plus d’informations sur l’utilisation de l’outil et des paramètres supplémentaires, notamment le démarrage d’une analyse complète ou la définition des chemins d’accès, voir Utiliser l’outil de ligne de commande mpcmdrun.exe pour configurer et gérer [Antivirus Microsoft Defender](command-line-arguments-microsoft-defender-antivirus.md).</span><span class="sxs-lookup"><span data-stu-id="0b3a1-128">For more information about how to use the tool and additional parameters, including starting a full scan, or defining paths, see [Use the mpcmdrun.exe commandline tool to configure and manage Microsoft Defender Antivirus](command-line-arguments-microsoft-defender-antivirus.md).</span></span>

## <a name="use-microsoft-intune-to-run-a-scan"></a><span data-ttu-id="0b3a1-129">Utiliser Microsoft Intune pour exécuter une analyse</span><span class="sxs-lookup"><span data-stu-id="0b3a1-129">Use Microsoft Intune to run a scan</span></span>

1. <span data-ttu-id="0b3a1-130">Go to the Microsoft Endpoint Manager admin center ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ) and log in.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-130">Go to the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and log in.</span></span>

2. <span data-ttu-id="0b3a1-131">Dans la barre latérale, sélectionnez **Appareils**  >  **tous les appareils** et choisissez l’appareil que vous souhaitez analyser.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-131">From the sidebar, select **Devices** > **All Devices** and choose the device you want to scan.</span></span>

3. <span data-ttu-id="0b3a1-132">Sélectionnez **... Plus**.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-132">Select **...More**.</span></span> <span data-ttu-id="0b3a1-133">Dans les options, sélectionnez **Analyse rapide** (recommandé) ou **Analyse complète.**</span><span class="sxs-lookup"><span data-stu-id="0b3a1-133">From the options, select **Quick Scan** (recommended) or **Full Scan**.</span></span>

## <a name="use-the-windows-security-app-to-run-a-scan"></a><span data-ttu-id="0b3a1-134">Utiliser l’application Sécurité Windows pour exécuter une analyse</span><span class="sxs-lookup"><span data-stu-id="0b3a1-134">Use the Windows Security app to run a scan</span></span>

<span data-ttu-id="0b3a1-135">Voir [Exécuter une analyse dans l’application Sécurité Windows pour](microsoft-defender-security-center-antivirus.md) obtenir des instructions sur l’exécution d’une analyse sur des points de terminaison individuels.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-135">See [Run a scan in the Windows Security app](microsoft-defender-security-center-antivirus.md) for instructions on running a scan on individual endpoints.</span></span>

## <a name="use-powershell-cmdlets-to-run-a-scan"></a><span data-ttu-id="0b3a1-136">Utiliser les cmdlets PowerShell pour exécuter une analyse</span><span class="sxs-lookup"><span data-stu-id="0b3a1-136">Use PowerShell cmdlets to run a scan</span></span>

<span data-ttu-id="0b3a1-137">Utilisez la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="0b3a1-137">Use the following cmdlet:</span></span>

```PowerShell
Start-MpScan
```

<span data-ttu-id="0b3a1-138">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender/)Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-138">For more information on how to use PowerShell with Microsoft Defender Antivirus, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/).</span></span>

## <a name="use-windows-management-instruction-wmi-to-run-a-scan"></a><span data-ttu-id="0b3a1-139">Utiliser Windows Management Instruction (WMI) pour exécuter une analyse</span><span class="sxs-lookup"><span data-stu-id="0b3a1-139">Use Windows Management Instruction (WMI) to run a scan</span></span>

<span data-ttu-id="0b3a1-140">Utilisez la [ **méthode Start** de](/previous-versions/windows/desktop/defender/start-msft-mpscan) la **MSFT_MpScan** classe.</span><span class="sxs-lookup"><span data-stu-id="0b3a1-140">Use the [**Start** method](/previous-versions/windows/desktop/defender/start-msft-mpscan) of the **MSFT_MpScan** class.</span></span>

<span data-ttu-id="0b3a1-141">Pour plus d’informations sur les paramètres autorisés, voir [Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="0b3a1-141">For more information about which parameters are allowed, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span></span>

