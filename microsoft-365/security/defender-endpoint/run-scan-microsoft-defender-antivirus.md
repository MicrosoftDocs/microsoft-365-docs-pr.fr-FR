---
title: Exécuter et personnaliser des analyses à la demande dans Antivirus Microsoft Defender
description: Exécuter et configurer des analyses à la demande à l’aide de PowerShell, Windows Management Instrumentation ou individuellement sur les points de terminaison avec l Sécurité Windows appl.
keywords: analyse, à la demande, dos, intune, analyse instantanée
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 05/05/2021
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.topic: how-to
ms.openlocfilehash: 124ebde48c008743a486a4454e7772fd93f9eca7
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52275359"
---
# <a name="configure-and-run-on-demand-microsoft-defender-antivirus-scans"></a><span data-ttu-id="9d3f7-104">Configurer et exécuter des analyses à la demande avec l’antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-104">Configure and run on-demand Microsoft Defender Antivirus scans</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="9d3f7-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9d3f7-105">**Applies to:**</span></span>

- [<span data-ttu-id="9d3f7-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9d3f7-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="9d3f7-107">Vous pouvez exécuter une analyse à la demande sur des points de terminaison individuels.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-107">You can run an on-demand scan on individual endpoints.</span></span> <span data-ttu-id="9d3f7-108">Ces analyses démarrent immédiatement et vous pouvez définir des paramètres pour l’analyse, tels que l’emplacement ou le type.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-108">These scans will start immediately, and you can define parameters for the scan, such as the location or type.</span></span>

## <a name="quick-scan-versus-full-scan"></a><span data-ttu-id="9d3f7-109">Analyse rapide et analyse complète</span><span class="sxs-lookup"><span data-stu-id="9d3f7-109">Quick scan versus full scan</span></span>

<span data-ttu-id="9d3f7-110">L’analyse rapide examine tous les emplacements où des programmes malveillants peuvent être enregistrés pour démarrer avec le système, tels que les clés de Registre et les dossiers de démarrage Windows connus.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-110">Quick scan looks at all the locations where there could be malware registered to start with the system, such as registry keys and known Windows startup folders.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9d3f7-111">Antivirus Microsoft Defender s’exécute dans le contexte du [compte LocalSystem](/windows/win32/services/localsystem-account) lors de l’analyse locale.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-111">Microsoft Defender Antivirus runs in the context of the [LocalSystem](/windows/win32/services/localsystem-account) account when performing a local scan.</span></span> <span data-ttu-id="9d3f7-112">Pour les analyses réseau, il utilise le contexte du compte d’appareil.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-112">For network scans, it uses the context of the device account.</span></span> <span data-ttu-id="9d3f7-113">Si le compte d’appareil de domaine ne peut pas accéder au partage, l’analyse ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-113">If the domain device account doesn't have appropriate permissions to access the share, the scan won't work.</span></span> <span data-ttu-id="9d3f7-114">Assurez-vous que l’appareil dispose d’autorisations sur le partage réseau d’accès.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-114">Ensure that the device has permissions to the access network share.</span></span>

<span data-ttu-id="9d3f7-115">Combinée avec la fonctionnalité de [protection](configure-real-time-protection-microsoft-defender-antivirus.md)en temps réel toujours en cours (qui examine les fichiers lorsqu’ils sont ouverts et fermés, et chaque fois qu’un utilisateur navigue vers un dossier), une analyse rapide permet d’assurer une couverture solide à la fois pour les programmes malveillants qui commencent par le système et les programmes malveillants au niveau du noyau.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-115">Combined with [always-on real-time protection capability](configure-real-time-protection-microsoft-defender-antivirus.md)--which reviews files when they're opened and closed, and whenever a user navigates to a folder--a quick scan helps provide strong coverage both for malware that starts with the system and kernel-level malware.</span></span>  

<span data-ttu-id="9d3f7-116">Dans la plupart des cas, une analyse rapide permet de trouver des programmes malveillants qui n’ont pas été détectés par la protection en temps réel.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-116">In most instances, a quick scan is adequate to find malware that wasn't picked up by real-time protection.</span></span>

<span data-ttu-id="9d3f7-117">Une analyse complète peut être utile sur les points de terminaison qui ont signalé une menace de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-117">A full scan can be useful on endpoints that have reported a malware threat.</span></span> <span data-ttu-id="9d3f7-118">L’analyse peut identifier s’il existe des composants inactifs qui nécessitent un nettoyage plus approfondi.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-118">The scan can identify if there are any inactive components that require a more thorough clean-up.</span></span> <span data-ttu-id="9d3f7-119">Cela est idéal si votre organisation exécute des analyses à la demande.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-119">This is  ideal if your organization is running on-demand scans.</span></span>

> [!NOTE]
> <span data-ttu-id="9d3f7-120">Par défaut, les analyses rapides s’exécutent sur des appareils amovibles montés, tels que des lecteurs USB.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-120">By default, quick scans run on mounted removable devices, such as USB drives.</span></span>

## <a name="use-microsoft-endpoint-manager-to-run-a-scan"></a><span data-ttu-id="9d3f7-121">Utiliser Microsoft Endpoint Manager pour exécuter une analyse</span><span class="sxs-lookup"><span data-stu-id="9d3f7-121">Use Microsoft Endpoint Manager to run a scan</span></span>

1. <span data-ttu-id="9d3f7-122">Go to the Microsoft Endpoint Manager admin center ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ) and log in.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-122">Go to the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and log in.</span></span>
2. <span data-ttu-id="9d3f7-123">Choisissez **l’Antivirus de sécurité des points de**  >  **terminaison.**</span><span class="sxs-lookup"><span data-stu-id="9d3f7-123">Choose **Endpoint security** > **Antivirus**.</span></span>
3. <span data-ttu-id="9d3f7-124">Dans la liste des onglets, sélectionnez Windows 10 points de **terminaison défectueux.**</span><span class="sxs-lookup"><span data-stu-id="9d3f7-124">In the list of tabs, select **Windows 10 unhealthy endpoints**.</span></span>
4. <span data-ttu-id="9d3f7-125">Dans la liste des actions fournies, sélectionnez **Analyse rapide** ou **Analyse complète.**</span><span class="sxs-lookup"><span data-stu-id="9d3f7-125">From the list of actions provided, select **Quick Scan** or **Full Scan**.</span></span>

<span data-ttu-id="9d3f7-126">[![IMAGE ](images/mem-antivirus-scan-on-demand.png)](images/mem-antivirus-scan-on-demand.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="9d3f7-126">[ ![IMAGE](images/mem-antivirus-scan-on-demand.png) ](images/mem-antivirus-scan-on-demand.png#lightbox)</span></span>

> [!TIP]
> <span data-ttu-id="9d3f7-127">Pour plus d’informations sur l’utilisation Microsoft Endpoint Manager pour exécuter une analyse, voir [Tâches anti-programme](/configmgr/protect/deploy-use/endpoint-antimalware-firewall#how-to-perform-an-on-demand-scan-of-computers)malveillant et pare-feu : Comment effectuer une analyse à la demande .</span><span class="sxs-lookup"><span data-stu-id="9d3f7-127">For more information about using Microsoft Endpoint Manager to run a scan, see [Antimalware and firewall tasks: How to perform an on-demand scan](/configmgr/protect/deploy-use/endpoint-antimalware-firewall#how-to-perform-an-on-demand-scan-of-computers).</span></span>

## <a name="use-the-mpcmdrunexe-command-line-utility-to-run-a-scan"></a><span data-ttu-id="9d3f7-128">Utiliser lmpcmdrun.exe de ligne de commande pour exécuter une analyse</span><span class="sxs-lookup"><span data-stu-id="9d3f7-128">Use the mpcmdrun.exe command-line utility to run a scan</span></span>

<span data-ttu-id="9d3f7-129">Utilisez le paramètre `-scan` suivant :</span><span class="sxs-lookup"><span data-stu-id="9d3f7-129">Use the following `-scan` parameter:</span></span>

```console
mpcmdrun.exe -scan -scantype 1
```

<span data-ttu-id="9d3f7-130">Pour plus d’informations sur l’utilisation de l’outil et des paramètres supplémentaires, notamment le démarrage d’une analyse complète ou la définition des chemins d’accès, voir Utiliser l’outil de ligne de commande mpcmdrun.exe pour configurer et gérer [Antivirus Microsoft Defender](command-line-arguments-microsoft-defender-antivirus.md).</span><span class="sxs-lookup"><span data-stu-id="9d3f7-130">For more information about how to use the tool and additional parameters, including starting a full scan, or defining paths, see [Use the mpcmdrun.exe commandline tool to configure and manage Microsoft Defender Antivirus](command-line-arguments-microsoft-defender-antivirus.md).</span></span>

## <a name="use-microsoft-intune-to-run-a-scan"></a><span data-ttu-id="9d3f7-131">Utiliser Microsoft Intune pour exécuter une analyse</span><span class="sxs-lookup"><span data-stu-id="9d3f7-131">Use Microsoft Intune to run a scan</span></span>

1. <span data-ttu-id="9d3f7-132">Go to the Microsoft Endpoint Manager admin center ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ) and log in.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-132">Go to the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and log in.</span></span>
2. <span data-ttu-id="9d3f7-133">Dans la barre latérale, sélectionnez **Appareils > tous** les appareils et choisissez l’appareil que vous souhaitez analyser.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-133">From the sidebar, select **Devices > All Devices** and choose the device you want to scan.</span></span>
3. <span data-ttu-id="9d3f7-134">Sélectionnez **... Plus**.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-134">Select **...More**.</span></span> <span data-ttu-id="9d3f7-135">Dans les options, sélectionnez **Analyse rapide** **ou Analyse complète.**</span><span class="sxs-lookup"><span data-stu-id="9d3f7-135">From the options, select **Quick Scan** or **Full Scan**.</span></span>

## <a name="use-the-windows-security-app-to-run-a-scan"></a><span data-ttu-id="9d3f7-136">Utiliser l’application Sécurité Windows pour exécuter une analyse</span><span class="sxs-lookup"><span data-stu-id="9d3f7-136">Use the Windows Security app to run a scan</span></span>

<span data-ttu-id="9d3f7-137">Voir [Exécuter une analyse dans l’application Sécurité Windows pour](microsoft-defender-security-center-antivirus.md) obtenir des instructions sur l’exécution d’une analyse sur des points de terminaison individuels.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-137">See [Run a scan in the Windows Security app](microsoft-defender-security-center-antivirus.md) for instructions on running a scan on individual endpoints.</span></span>

## <a name="use-powershell-cmdlets-to-run-a-scan"></a><span data-ttu-id="9d3f7-138">Utiliser les cmdlets PowerShell pour exécuter une analyse</span><span class="sxs-lookup"><span data-stu-id="9d3f7-138">Use PowerShell cmdlets to run a scan</span></span>

<span data-ttu-id="9d3f7-139">Utilisez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="9d3f7-139">Use the following cmdlet:</span></span>

```PowerShell
Start-MpScan
```

<span data-ttu-id="9d3f7-140">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender/)Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-140">For more information on how to use PowerShell with Microsoft Defender Antivirus, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/).</span></span>

## <a name="use-windows-management-instruction-wmi-to-run-a-scan"></a><span data-ttu-id="9d3f7-141">Utiliser Windows Management Instruction (WMI) pour exécuter une analyse</span><span class="sxs-lookup"><span data-stu-id="9d3f7-141">Use Windows Management Instruction (WMI) to run a scan</span></span>

<span data-ttu-id="9d3f7-142">Utilisez la [ **méthode Start** de](/previous-versions/windows/desktop/defender/start-msft-mpscan) la **MSFT_MpScan** classe.</span><span class="sxs-lookup"><span data-stu-id="9d3f7-142">Use the [**Start** method](/previous-versions/windows/desktop/defender/start-msft-mpscan) of the **MSFT_MpScan** class.</span></span>

<span data-ttu-id="9d3f7-143">Pour plus d’informations sur les paramètres autorisés, voir [Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="9d3f7-143">For more information about which parameters are allowed, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span></span>

## <a name="related-articles"></a><span data-ttu-id="9d3f7-144">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="9d3f7-144">Related articles</span></span>

- [<span data-ttu-id="9d3f7-145">Configurer les options d’analyse de l’antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="9d3f7-145">Configure Microsoft Defender Antivirus scanning options</span></span>](configure-advanced-scan-types-microsoft-defender-antivirus.md)
- [<span data-ttu-id="9d3f7-146">Configurer des analyses de Antivirus Microsoft Defender programmées</span><span class="sxs-lookup"><span data-stu-id="9d3f7-146">Configure scheduled Microsoft Defender Antivirus scans</span></span>](scheduled-catch-up-scans-microsoft-defender-antivirus.md)
- [<span data-ttu-id="9d3f7-147">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="9d3f7-147">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)