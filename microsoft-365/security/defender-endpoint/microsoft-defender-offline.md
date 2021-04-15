---
title: Microsoft Defender hors ligne dans Windows 10
description: Vous pouvez utiliser Microsoft Defender hors ligne directement à partir de l Windows Defender antivirus. Vous pouvez également gérer la façon dont elle est déployée dans votre réseau.
keywords: analyse, defender, hors connexion
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 3b1e7e70c6ca217d3ad8859c1493598d71054f84
ms.sourcegitcommit: 7a339c9f7039825d131b39481ddf54c57b021b11
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51765334"
---
# <a name="run-and-review-the-results-of-a-microsoft-defender-offline-scan"></a><span data-ttu-id="97c39-105">Exécuter et passer en revue les résultats d'une analyse Microsoft Defender hors ligne</span><span class="sxs-lookup"><span data-stu-id="97c39-105">Run and review the results of a Microsoft Defender Offline scan</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="97c39-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="97c39-106">**Applies to:**</span></span>

- [<span data-ttu-id="97c39-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="97c39-107">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="97c39-108">Microsoft Defender hors ligne est un outil d'analyse anti-programme malveillant qui vous permet de démarrer et d'exécuter une analyse à partir d'un environnement approuvé.</span><span class="sxs-lookup"><span data-stu-id="97c39-108">Microsoft Defender Offline is an antimalware scanning tool that lets you boot and run a scan from a trusted environment.</span></span> <span data-ttu-id="97c39-109">L'analyse s'exécute en dehors du noyau Windows normal afin qu'elle puisse cibler les programmes malveillants qui tentent de contourner l'shell Windows, tels que les virus et rootkits qui infectent ou éviennent l'enregistrement de démarrage maître (MBR).</span><span class="sxs-lookup"><span data-stu-id="97c39-109">The scan runs from outside the normal Windows kernel so it can target malware that attempts to bypass the Windows shell, such as viruses and rootkits that infect or overwrite the master boot record (MBR).</span></span>

<span data-ttu-id="97c39-110">Vous pouvez utiliser Microsoft Defender hors ligne si vous suspectez une infection par un programme malveillant ou si vous souhaitez confirmer un nettoyage complet du point de terminaison après une attaque par programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="97c39-110">You can use Microsoft Defender Offline if you suspect a malware infection, or you want to confirm a thorough clean of the endpoint after a malware outbreak.</span></span>

<span data-ttu-id="97c39-111">Dans Windows 10, Microsoft Defender hors ligne peut être exécuté en un clic directement à partir de [l'application Sécurité Windows.](microsoft-defender-security-center-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="97c39-111">In Windows 10, Microsoft Defender Offline can be run with one click directly from the [Windows Security app](microsoft-defender-security-center-antivirus.md).</span></span> <span data-ttu-id="97c39-112">Dans les versions précédentes de Windows, un utilisateur devait installer Microsoft Defender hors ligne sur un support démarrable, redémarrer le point de terminaison et charger le support démarrable.</span><span class="sxs-lookup"><span data-stu-id="97c39-112">In previous versions of Windows, a user had to install Microsoft Defender Offline to bootable media, restart the endpoint, and load the bootable media.</span></span>

## <a name="prerequisites-and-requirements"></a><span data-ttu-id="97c39-113">conditions préalables et conditions requises</span><span class="sxs-lookup"><span data-stu-id="97c39-113">prerequisites and requirements</span></span>

<span data-ttu-id="97c39-114">Microsoft Defender hors ligne dans Windows 10 présente la même configuration matérielle requise que Windows 10.</span><span class="sxs-lookup"><span data-stu-id="97c39-114">Microsoft Defender Offline in Windows 10 has the same hardware requirements as Windows 10.</span></span> 

<span data-ttu-id="97c39-115">Pour plus d'informations sur les conditions requises pour Windows 10, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="97c39-115">For more information about Windows 10 requirements, see the following topics:</span></span>

- [<span data-ttu-id="97c39-116">Configuration matérielle minimale requise</span><span class="sxs-lookup"><span data-stu-id="97c39-116">Minimum hardware requirements</span></span>](/windows-hardware/design/minimum/minimum-hardware-requirements-overview)

- [<span data-ttu-id="97c39-117">Recommandations en matière de composants matériels</span><span class="sxs-lookup"><span data-stu-id="97c39-117">Hardware component guidelines</span></span>](/windows-hardware/design/component-guidelines/components)

> [!NOTE]
> <span data-ttu-id="97c39-118">Microsoft Defender hors ligne n'est pas pris en charge sur les ordinateurs ARM processeurs ou sur les unités de conservation de stock Windows Server.</span><span class="sxs-lookup"><span data-stu-id="97c39-118">Microsoft Defender Offline is not supported on machines with ARM processors, or on Windows Server Stock Keeping Units.</span></span>

<span data-ttu-id="97c39-119">Pour exécuter Microsoft Defender hors ligne à partir du point de terminaison, l'utilisateur doit être connecté avec des privilèges d'administrateur.</span><span class="sxs-lookup"><span data-stu-id="97c39-119">To run Microsoft Defender Offline from the endpoint, the user must be logged in with administrator privileges.</span></span>
 
## <a name="microsoft-defender-offline-updates"></a><span data-ttu-id="97c39-120">Mises à jour De Microsoft Defender hors ligne</span><span class="sxs-lookup"><span data-stu-id="97c39-120">Microsoft Defender Offline updates</span></span>

<span data-ttu-id="97c39-121">Microsoft Defender hors ligne utilise les dernières mises à jour de protection disponibles sur le point de terminaison . Il est mis à jour chaque fois Windows Defender antivirus est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="97c39-121">Microsoft Defender Offline uses the most recent protection updates available on the endpoint; it's updated whenever Windows Defender Antivirus is updated.</span></span> 

> [!NOTE]
> <span data-ttu-id="97c39-122">Avant d'exécution d'une analyse hors connexion, vous devez essayer de mettre à jour la protection de l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="97c39-122">Before running an offline scan, you should attempt to update Microsoft Defender AV protection.</span></span> <span data-ttu-id="97c39-123">Vous pouvez forcer une mise à jour à l'aide d'une stratégie de groupe ou toutefois déployer normalement des mises à jour sur les points de terminaison, ou vous pouvez télécharger et installer manuellement les dernières mises à jour de la protection à partir du [Centre de protection Microsoft contre les programmes malveillants](https://www.microsoft.com/security/portal/definitions/adl.aspx).</span><span class="sxs-lookup"><span data-stu-id="97c39-123">You can either force an update with Group Policy or however you normally deploy updates to endpoints, or you can manually download and install the latest protection updates from the [Microsoft Malware Protection Center](https://www.microsoft.com/security/portal/definitions/adl.aspx).</span></span>

<span data-ttu-id="97c39-124">Pour plus d'informations, consultez la rubrique Gérer les mises à jour de [l'Antivirus Security de Microsoft Defender.](manage-protection-updates-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="97c39-124">See the [Manage Microsoft Defender Antivirus Security intelligence  updates](manage-protection-updates-microsoft-defender-antivirus.md) topic for more information.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="97c39-125">Scénarios d'utilisation</span><span class="sxs-lookup"><span data-stu-id="97c39-125">Usage scenarios</span></span>

<span data-ttu-id="97c39-126">Dans Windows 10, version 1607, vous pouvez forcer manuellement une analyse hors connexion.</span><span class="sxs-lookup"><span data-stu-id="97c39-126">In Windows 10, version 1607, you can manually force an offline scan.</span></span> <span data-ttu-id="97c39-127">Sinon, si Windows Defender que Microsoft Defender hors ligne doit s'exécuter, il invite l'utilisateur sur le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="97c39-127">Alternatively, if Windows Defender determines that Microsoft Defender Offline needs to run, it will prompt the user on the endpoint.</span></span> 

<span data-ttu-id="97c39-128">La nécessité d'effectuer une analyse hors connexion sera également révélée dans Microsoft Endpoint Manager si vous l'utilisez pour gérer vos points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="97c39-128">The need to perform an offline scan will also be revealed in Microsoft Endpoint Manager if you're using it to manage your endpoints.</span></span>

<span data-ttu-id="97c39-129">L'invite peut se produire via une notification, semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="97c39-129">The prompt can occur via a notification, similar to the following:</span></span>

![Notification Windows indiquant la nécessité d'exécuter Microsoft Defender hors ligne](images/defender/notification.png)

<span data-ttu-id="97c39-131">L'utilisateur est également informé dans le client Windows Defender client.</span><span class="sxs-lookup"><span data-stu-id="97c39-131">The user will also be notified within the Windows Defender client.</span></span>

<span data-ttu-id="97c39-132">Dans Configuration Manager, vous pouvez identifier l'état des points de terminaison en naviguant vers Surveillance > Vue d'ensemble > Sécurité **> Endpoint Protection Status > System Center Endpoint Protection Status**.</span><span class="sxs-lookup"><span data-stu-id="97c39-132">In Configuration Manager, you can identify the status of endpoints by navigating to **Monitoring > Overview > Security > Endpoint Protection Status > System Center Endpoint Protection Status**.</span></span> 

<span data-ttu-id="97c39-133">Les analyses Microsoft Defender hors  ligne sont indiquées sous l'état de correction des programmes malveillants comme **analyse hors connexion requise.**</span><span class="sxs-lookup"><span data-stu-id="97c39-133">Microsoft Defender Offline scans are indicated under **Malware remediation status** as **Offline scan required**.</span></span>

![Microsoft Endpoint Manager indiquant qu'une analyse Microsoft Defender hors ligne est requise](images/defender/sccm-wdo.png)

## <a name="configure-notifications"></a><span data-ttu-id="97c39-135">Configurer les notifications</span><span class="sxs-lookup"><span data-stu-id="97c39-135">Configure notifications</span></span>

<span data-ttu-id="97c39-136">Les notifications Microsoft Defender hors ligne sont configurées dans le même paramètre de stratégie que les autres notifications De l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="97c39-136">Microsoft Defender Offline notifications are configured in the same policy setting as other Microsoft Defender AV notifications.</span></span>

<span data-ttu-id="97c39-137">Pour plus d'informations sur les notifications Windows Defender, consultez la rubrique Configurer les [notifications](configure-notifications-microsoft-defender-antivirus.md) qui apparaissent sur les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="97c39-137">For more information about notifications in Windows Defender, see the [Configure the notifications that appear on endpoints](configure-notifications-microsoft-defender-antivirus.md) topic.</span></span>

## <a name="run-a-scan"></a><span data-ttu-id="97c39-138">Effectuer une analyse</span><span class="sxs-lookup"><span data-stu-id="97c39-138">Run a scan</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="97c39-139">Avant d'utiliser Microsoft Defender hors ligne, veillez à enregistrer les fichiers et à arrêter les programmes en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="97c39-139">Before you use Microsoft Defender Offline, make sure you save any files and shut down running programs.</span></span> <span data-ttu-id="97c39-140">L'analyse Microsoft Defender hors ligne prend environ 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="97c39-140">The Microsoft Defender Offline scan takes about 15 minutes to run.</span></span> <span data-ttu-id="97c39-141">Il redémarre le point de terminaison une fois l'analyse terminée.</span><span class="sxs-lookup"><span data-stu-id="97c39-141">It will restart the endpoint when the scan is complete.</span></span> <span data-ttu-id="97c39-142">L'analyse est effectuée en dehors de l'environnement d'exploitation Windows habituel.</span><span class="sxs-lookup"><span data-stu-id="97c39-142">The scan is performed outside of the usual Windows operating environment.</span></span> <span data-ttu-id="97c39-143">L'interface utilisateur s'affiche différemment d'une analyse normale effectuée par Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="97c39-143">The user interface will appear different to a normal scan performed by Windows Defender.</span></span> <span data-ttu-id="97c39-144">Une fois l'analyse terminée, le point de terminaison est redémarré et Windows se charge normalement.</span><span class="sxs-lookup"><span data-stu-id="97c39-144">After the scan is completed, the endpoint will be restarted and Windows will load normally.</span></span>

<span data-ttu-id="97c39-145">Vous pouvez exécuter une analyse Microsoft Defender hors ligne avec les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="97c39-145">You can run a Microsoft Defender Offline scan with the following:</span></span>

- <span data-ttu-id="97c39-146">PowerShell</span><span class="sxs-lookup"><span data-stu-id="97c39-146">PowerShell</span></span>
- <span data-ttu-id="97c39-147">WMI (Windows Management Instrumentation)</span><span class="sxs-lookup"><span data-stu-id="97c39-147">Windows Management Instrumentation (WMI)</span></span>
- <span data-ttu-id="97c39-148">Application Sécurité Windows</span><span class="sxs-lookup"><span data-stu-id="97c39-148">The Windows Security app</span></span>



### <a name="use-powershell-cmdlets-to-run-an-offline-scan"></a><span data-ttu-id="97c39-149">Utiliser les cmdlets PowerShell pour exécuter une analyse hors connexion</span><span class="sxs-lookup"><span data-stu-id="97c39-149">Use PowerShell cmdlets to run an offline scan</span></span>

<span data-ttu-id="97c39-150">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="97c39-150">Use the following cmdlets:</span></span>

```PowerShell
Start-MpWDOScan
```

<span data-ttu-id="97c39-151">Pour [plus d'informations](use-powershell-cmdlets-microsoft-defender-antivirus.md) sur l'utilisation de PowerShell avec l'Antivirus Microsoft Defender, voir les [cmdlets](/powershell/module/defender/) Utiliser PowerShell pour configurer et exécuter l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="97c39-151">See [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

### <a name="use-windows-management-instruction-wmi-to-run-an-offline-scan"></a><span data-ttu-id="97c39-152">Utiliser Windows Management Instruction (WMI) pour exécuter une analyse hors connexion</span><span class="sxs-lookup"><span data-stu-id="97c39-152">Use Windows Management Instruction (WMI) to run an offline scan</span></span>

<span data-ttu-id="97c39-153">Utilisez la [**MSFT_MpWDOScan**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour exécuter une analyse hors connexion.</span><span class="sxs-lookup"><span data-stu-id="97c39-153">Use the [**MSFT_MpWDOScan**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class to run an offline scan.</span></span>

<span data-ttu-id="97c39-154">L'extrait de script WMI suivant exécute immédiatement une analyse Microsoft Defender hors ligne, ce qui entraîne le redémarrage du point de terminaison, l'analyse hors connexion, puis le redémarrage et le démarrage dans Windows.</span><span class="sxs-lookup"><span data-stu-id="97c39-154">The following WMI script snippet will immediately run a Microsoft Defender Offline scan, which will cause the endpoint to restart, run the offline scan, and then restart and boot into Windows.</span></span>

```console
wmic /namespace:\\root\Microsoft\Windows\Defender path MSFT_MpWDOScan call Start 
```

<span data-ttu-id="97c39-155">Pour plus d'informations, voir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="97c39-155">See the following for more information:</span></span>
- [<span data-ttu-id="97c39-156">Windows Defender API WMIv2</span><span class="sxs-lookup"><span data-stu-id="97c39-156">Windows Defender WMIv2 APIs</span></span>](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)


### <a name="use-the-windows-defender-security-app-to-run-an-offline-scan"></a><span data-ttu-id="97c39-157">Utiliser l'application Windows Defender security pour exécuter une analyse hors connexion</span><span class="sxs-lookup"><span data-stu-id="97c39-157">Use the Windows Defender Security app to run an offline scan</span></span>

1. <span data-ttu-id="97c39-158">Ouvrez l'application Sécurité Windows en cliquant sur l'icône de bouclier dans la barre des tâches ou en recherchant Defender dans le menu **Démarrer.**</span><span class="sxs-lookup"><span data-stu-id="97c39-158">Open the Windows Security app by clicking the shield icon in the task bar or searching the start menu for **Defender**.</span></span>

2. <span data-ttu-id="97c39-159">Cliquez sur la **vignette & protection** antivirus contre les menaces (ou sur l'icône de bouclier dans la barre de menus de gauche), puis sur l'étiquette **d'analyse** avancée :</span><span class="sxs-lookup"><span data-stu-id="97c39-159">Click the **Virus & threat protection** tile (or the shield icon on the left menu bar) and then the **Advanced scan** label:</span></span>
    
3. <span data-ttu-id="97c39-160">Sélectionnez **Analyse Microsoft Defender hors ligne,** puis cliquez sur Analyser **maintenant.**</span><span class="sxs-lookup"><span data-stu-id="97c39-160">Select **Microsoft Defender Offline scan** and click **Scan now**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="97c39-161">Dans Windows 10, version 1607, l'analyse hors connexion peut être exécuté à partir de la Windows Defender de sécurité de la mise à jour des paramètre **& s Windows** ou à partir du  >    >   client Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="97c39-161">In Windows 10, version 1607, the offline scan could be run from under **Windows Settings** > **Update & security** > **Windows Defender** or from the Windows Defender client.</span></span>


## <a name="review-scan-results"></a><span data-ttu-id="97c39-162">Passer en revue les résultats de l'analyse</span><span class="sxs-lookup"><span data-stu-id="97c39-162">Review scan results</span></span>

<span data-ttu-id="97c39-163">Les résultats de l'analyse Microsoft Defender hors ligne sont répertoriés dans la section Historique d'analyse [de l'application Sécurité Windows.](microsoft-defender-security-center-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="97c39-163">Microsoft Defender Offline scan results will be listed in the [Scan history section of the Windows Security app](microsoft-defender-security-center-antivirus.md).</span></span> 


## <a name="related-articles"></a><span data-ttu-id="97c39-164">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="97c39-164">Related articles</span></span>

- [<span data-ttu-id="97c39-165">Personnaliser, lancer et examiner les résultats des analyses et des corrections</span><span class="sxs-lookup"><span data-stu-id="97c39-165">Customize, initiate, and review the results of scans and remediation</span></span>](customize-run-review-remediate-scans-microsoft-defender-antivirus.md)
- [<span data-ttu-id="97c39-166">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="97c39-166">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)