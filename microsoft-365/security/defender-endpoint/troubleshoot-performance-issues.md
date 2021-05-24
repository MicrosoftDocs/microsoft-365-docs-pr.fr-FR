---
title: Résoudre des problèmes de performance
description: Résoudre les problèmes d’utilisation élevée du processeur lié au service de protection en temps réel dans Microsoft Defender pour Endpoint.
keywords: résolution des problèmes, performances, utilisation élevée du processeur, utilisation élevée du processeur, erreur, correctif, conformité des mises à jour, oms, surveiller, rapport, Microsoft Defender AV
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
ms.author: maccruz
author: schmurky
localization_priority: normal
manager: dansimp
ms.date: 04/14/2021
audience: ITPro
ms.topic: troubleshooting
ms.technology: mde
ms.openlocfilehash: 1a969b6430914eb2dd667a906dc071d3cd49be8b
ms.sourcegitcommit: 686f192e1a650ec805fe8e908b46ca51771ed41f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52625328"
---
# <a name="troubleshoot-performance-issues-related-to-real-time-protection"></a><span data-ttu-id="6baae-104">Résoudre les problèmes de performances liés à la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="6baae-104">Troubleshoot performance issues related to real-time protection</span></span>


[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="6baae-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6baae-105">**Applies to:**</span></span>

- [<span data-ttu-id="6baae-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6baae-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
 
<span data-ttu-id="6baae-107">Si votre système présente des problèmes élevés d’utilisation du processeur ou de performances liés au service de protection en temps réel dans Microsoft Defender pour le point de terminaison, vous pouvez soumettre un ticket au support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6baae-107">If your system is having high CPU usage or performance issues related to the real-time protection service in Microsoft Defender for Endpoint, you can submit a ticket to Microsoft support.</span></span> <span data-ttu-id="6baae-108">Suivez les étapes de [collecte Antivirus Microsoft Defender données de diagnostic.](collect-diagnostic-data.md)</span><span class="sxs-lookup"><span data-stu-id="6baae-108">Follow the steps in [Collect Microsoft Defender Antivirus diagnostic data](collect-diagnostic-data.md).</span></span>

<span data-ttu-id="6baae-109">En tant qu’administrateur, vous pouvez également résoudre ces problèmes vous-même.</span><span class="sxs-lookup"><span data-stu-id="6baae-109">As an admin, you can also troubleshoot these issues on your own.</span></span> 

<span data-ttu-id="6baae-110">Tout d’abord, vous pouvez vérifier si le problème est dû à un autre logiciel.</span><span class="sxs-lookup"><span data-stu-id="6baae-110">First, you might want to check if the issue is being caused by another software.</span></span> <span data-ttu-id="6baae-111">Consultez [La vérification auprès du fournisseur pour les exclusions antivirus.](#check-with-vendor-for-antivirus-exclusions)</span><span class="sxs-lookup"><span data-stu-id="6baae-111">Read [Check with vendor for antivirus exclusions](#check-with-vendor-for-antivirus-exclusions).</span></span>

<span data-ttu-id="6baae-112">Dans le cas contraire, vous pouvez identifier les logiciels associés au problème de performances identifié en suivant les étapes de la procédure d’analyse du [journal de protection Microsoft.](#analyze-the-microsoft-protection-log)</span><span class="sxs-lookup"><span data-stu-id="6baae-112">Otherwise, you can identify which software is related to the identified performance issue by following the steps in [Analyze the Microsoft Protection Log](#analyze-the-microsoft-protection-log).</span></span> 

<span data-ttu-id="6baae-113">Vous pouvez également fournir des journaux supplémentaires à votre soumission au support Microsoft en suivant les étapes ci-après :</span><span class="sxs-lookup"><span data-stu-id="6baae-113">You can also provide additional logs to your submission to Microsoft support by following the steps in:</span></span>
- [<span data-ttu-id="6baae-114">Capturer les journaux de processus à l’aide du moniteur de processus</span><span class="sxs-lookup"><span data-stu-id="6baae-114">Capture process logs using Process Monitor</span></span>](#capture-process-logs-using-process-monitor)
- [<span data-ttu-id="6baae-115">Capturer les journaux de performances à l’aide Windows Enregistreur de performances</span><span class="sxs-lookup"><span data-stu-id="6baae-115">Capture performance logs using Windows Performance Recorder</span></span>](#capture-performance-logs-using-windows-performance-recorder) 

## <a name="check-with-vendor-for-antivirus-exclusions"></a><span data-ttu-id="6baae-116">Consulter le fournisseur pour les exclusions antivirus</span><span class="sxs-lookup"><span data-stu-id="6baae-116">Check with vendor for antivirus exclusions</span></span>

<span data-ttu-id="6baae-117">Si vous pouvez facilement identifier les logiciels qui affectent les performances du système, allez à la base de connaissances ou au centre de support du fournisseur de logiciels.</span><span class="sxs-lookup"><span data-stu-id="6baae-117">If you can readily identify the software affecting system performance, go to the software vendor's knowledge base or support center.</span></span> <span data-ttu-id="6baae-118">Recherchez s’ils ont des recommandations sur les exclusions antivirus.</span><span class="sxs-lookup"><span data-stu-id="6baae-118">Search if they have recommendations about antivirus exclusions.</span></span> <span data-ttu-id="6baae-119">Si le site web du fournisseur ne les a pas, vous pouvez ouvrir un ticket de support avec lui et lui demander d’en publier un.</span><span class="sxs-lookup"><span data-stu-id="6baae-119">If the vendor's website does not have them, you can open a support ticket with them and ask them to publish one.</span></span> 

<span data-ttu-id="6baae-120">Nous recommandons aux éditeurs de logiciels de suivre les différentes directives de Partenariat avec le secteur [afin de minimiser les faux positifs.](https://www.microsoft.com/security/blog/2018/08/16/partnering-with-the-industry-to-minimize-false-positives/)</span><span class="sxs-lookup"><span data-stu-id="6baae-120">We recommend that software vendors follow the various guidelines in [Partnering with the industry to minimize false positives](https://www.microsoft.com/security/blog/2018/08/16/partnering-with-the-industry-to-minimize-false-positives/).</span></span> <span data-ttu-id="6baae-121">Le fournisseur peut soumettre ses logiciels via le portail [Microsoft Defender Security Intelligence (MDSI).](https://www.microsoft.com/wdsi/filesubmission?persona=SoftwareDeveloper)</span><span class="sxs-lookup"><span data-stu-id="6baae-121">The vendor can submit their software through the [Microsoft Defender Security Intelligence portal (MDSI)](https://www.microsoft.com/wdsi/filesubmission?persona=SoftwareDeveloper).</span></span>


## <a name="analyze-the-microsoft-protection-log"></a><span data-ttu-id="6baae-122">Analyser le journal de protection Microsoft</span><span class="sxs-lookup"><span data-stu-id="6baae-122">Analyze the Microsoft Protection Log</span></span>

<span data-ttu-id="6baae-123">Dans **MPLog-xxxxxxxx-xxxxxx.log,** vous pouvez trouver les informations d’impact sur les performances estimées de l’exécution de logiciels en tant *qu’EstimatedImpact*:</span><span class="sxs-lookup"><span data-stu-id="6baae-123">In **MPLog-xxxxxxxx-xxxxxx.log**, you can find the estimated performance impact information of running software as *EstimatedImpact*:</span></span>
    
`Per-process counts:ProcessImageName: smsswd.exe, TotalTime: 6597, Count: 1406, MaxTime: 609, MaxTimeFile: \Device\HarddiskVolume3\_SMSTaskSequence\Packages\WQ1008E9\Files\FramePkg.exe, EstimatedImpact: 65%`

| <span data-ttu-id="6baae-124">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="6baae-124">Field name</span></span> | <span data-ttu-id="6baae-125">Description</span><span class="sxs-lookup"><span data-stu-id="6baae-125">Description</span></span> |
|---|---|
|<span data-ttu-id="6baae-126">ProcessImageName</span><span class="sxs-lookup"><span data-stu-id="6baae-126">ProcessImageName</span></span> | <span data-ttu-id="6baae-127">Nom de l’image de processus</span><span class="sxs-lookup"><span data-stu-id="6baae-127">Process image name</span></span> |
| <span data-ttu-id="6baae-128">TotalTime</span><span class="sxs-lookup"><span data-stu-id="6baae-128">TotalTime</span></span> | <span data-ttu-id="6baae-129">Durée cumulée en millisecondes passées dans les analyses des fichiers accessibles par ce processus</span><span class="sxs-lookup"><span data-stu-id="6baae-129">The cumulative duration in milliseconds spent in scans of files accessed by this process</span></span> |
|<span data-ttu-id="6baae-130">Count</span><span class="sxs-lookup"><span data-stu-id="6baae-130">Count</span></span> | <span data-ttu-id="6baae-131">Nombre de fichiers analysés accédés par ce processus</span><span class="sxs-lookup"><span data-stu-id="6baae-131">The number of scanned files accessed by this process</span></span> |
|<span data-ttu-id="6baae-132">MaxTime</span><span class="sxs-lookup"><span data-stu-id="6baae-132">MaxTime</span></span> |  <span data-ttu-id="6baae-133">Durée en millisecondes de l’analyse unique la plus longue d’un fichier accessible par ce processus</span><span class="sxs-lookup"><span data-stu-id="6baae-133">The duration in milliseconds in the longest single scan of a file accessed by this process</span></span> |
| <span data-ttu-id="6baae-134">MaxTimeFile</span><span class="sxs-lookup"><span data-stu-id="6baae-134">MaxTimeFile</span></span> | <span data-ttu-id="6baae-135">Chemin d’accès au fichier accessible par ce processus pour lequel l’analyse la plus longue `MaxTime` de la durée a été enregistrée</span><span class="sxs-lookup"><span data-stu-id="6baae-135">The path of the file accessed by this process for which the longest scan of `MaxTime` duration was recorded</span></span> |
| <span data-ttu-id="6baae-136">EstimatedImpact</span><span class="sxs-lookup"><span data-stu-id="6baae-136">EstimatedImpact</span></span> | <span data-ttu-id="6baae-137">Le pourcentage de temps passé dans les analyses pour les fichiers accédés par ce processus en dehors de la période pendant laquelle ce processus a connu une activité d’analyse</span><span class="sxs-lookup"><span data-stu-id="6baae-137">The percentage of time spent in scans for files accessed by this process out of the period in which this process experienced scan activity</span></span> |

<span data-ttu-id="6baae-138">Si l’impact sur les performances est élevé, essayez d’ajouter le processus aux exclusions chemin/processus en suivant les étapes de configuration et de validation des exclusions pour [Antivirus Microsoft Defender analyses.](collect-diagnostic-data.md)</span><span class="sxs-lookup"><span data-stu-id="6baae-138">If the performance impact is high, try adding the process to the Path/Process exclusions by following the steps in [Configure and validate exclusions for Microsoft Defender Antivirus scans](collect-diagnostic-data.md).</span></span>

<span data-ttu-id="6baae-139">Si l’étape précédente ne résout pas le problème, [](#capture-process-logs-using-process-monitor) vous pouvez collecter plus d’informations via le Moniteur de processus ou l’enregistreur de performances [Windows](#capture-performance-logs-using-windows-performance-recorder) dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="6baae-139">If the previous step doesn't solve the problem, you can collect more information through the [Process Monitor](#capture-process-logs-using-process-monitor) or the [Windows Performance Recorder](#capture-performance-logs-using-windows-performance-recorder) in the following sections.</span></span>
     
## <a name="capture-process-logs-using-process-monitor"></a><span data-ttu-id="6baae-140">Capturer les journaux de processus à l’aide du moniteur de processus</span><span class="sxs-lookup"><span data-stu-id="6baae-140">Capture process logs using Process Monitor</span></span>

<span data-ttu-id="6baae-141">Process Monitor (ProcMon) est un outil de surveillance avancé qui peut afficher les processus en temps réel.</span><span class="sxs-lookup"><span data-stu-id="6baae-141">Process Monitor (ProcMon) is an advanced monitoring tool that can show real-time processes.</span></span> <span data-ttu-id="6baae-142">Vous pouvez l’utiliser pour capturer le problème de performances tel qu’il se produit.</span><span class="sxs-lookup"><span data-stu-id="6baae-142">You can use this to capture the performance issue as it is occurring.</span></span>

1. <span data-ttu-id="6baae-143">Téléchargez [process monitor v3.60 dans](/sysinternals/downloads/procmon) un dossier tel que `C:\temp` .</span><span class="sxs-lookup"><span data-stu-id="6baae-143">Download [Process Monitor v3.60](/sysinternals/downloads/procmon) to a folder like `C:\temp`.</span></span>

2. <span data-ttu-id="6baae-144">Pour supprimer la marque du fichier du web :</span><span class="sxs-lookup"><span data-stu-id="6baae-144">To remove the file's mark of the web:</span></span>
    1. <span data-ttu-id="6baae-145">Cliquez avec le **bouton droitProcessMonitor.zip** puis sélectionnez **Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="6baae-145">Right-click **ProcessMonitor.zip** and select **Properties**.</span></span>
    1. <span data-ttu-id="6baae-146">Sous *l’onglet Général,* recherchez *Sécurité.*</span><span class="sxs-lookup"><span data-stu-id="6baae-146">Under the *General* tab, look for *Security*.</span></span>
    1. <span data-ttu-id="6baae-147">Cochez la case en **regard de Débloquer.**</span><span class="sxs-lookup"><span data-stu-id="6baae-147">Check the box beside **Unblock**.</span></span>
    1. <span data-ttu-id="6baae-148">Sélectionnez **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="6baae-148">Select **Apply**.</span></span>
    
    ![Supprimer MOTW](images/procmon-motw.png) 

3. <span data-ttu-id="6baae-150">Dézipez le fichier de `C:\temp` sorte que le chemin d’accès du dossier soit `C:\temp\ProcessMonitor` .</span><span class="sxs-lookup"><span data-stu-id="6baae-150">Unzip the file in `C:\temp` so that the folder path will be `C:\temp\ProcessMonitor`.</span></span> 

4. <span data-ttu-id="6baae-151">Copiez **ProcMon.exe** vers Windows client ou Windows serveur que vous dépannagez.</span><span class="sxs-lookup"><span data-stu-id="6baae-151">Copy **ProcMon.exe**  to the Windows client or Windows server you're troubleshooting.</span></span>  

5. <span data-ttu-id="6baae-152">Avant d’utiliser ProcMon, assurez-vous que toutes les autres applications non liées au problème d’utilisation élevée du processeur sont fermées.</span><span class="sxs-lookup"><span data-stu-id="6baae-152">Before running ProcMon, make sure all other applications not related to the high CPU usage issue are closed.</span></span> <span data-ttu-id="6baae-153">Cela permet de réduire le nombre de processus à vérifier.</span><span class="sxs-lookup"><span data-stu-id="6baae-153">Doing this will minimize the number of processes to check.</span></span>

6. <span data-ttu-id="6baae-154">Vous pouvez lancer ProcMon de deux manières.</span><span class="sxs-lookup"><span data-stu-id="6baae-154">You can launch ProcMon in two ways.</span></span>
    1. <span data-ttu-id="6baae-155">Cliquez avec le **bouton droitProcMon.exe** **sélectionnez Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="6baae-155">Right-click **ProcMon.exe** and select **Run as administrator**.</span></span> 
    

        <span data-ttu-id="6baae-156">Étant donné que la journalisation démarre automatiquement, sélectionnez l’icône de loupe pour arrêter la capture actuelle ou utilisez le raccourci clavier **Ctrl+E**.</span><span class="sxs-lookup"><span data-stu-id="6baae-156">Since logging starts automatically, select the magnifying glass icon  to stop the current capture or use the keyboard shortcut **Ctrl+E**.</span></span>
 
        ![icône de loupe](images/procmon-magglass.png)

        <span data-ttu-id="6baae-158">Pour vérifier que vous avez arrêté la capture, vérifiez si l’icône en forme de loupe apparaît maintenant avec un X rouge.</span><span class="sxs-lookup"><span data-stu-id="6baae-158">To verify that you have stopped the capture, check if the magnifying glass icon now appears with a red X.</span></span>

        ![barre oblique rouge](images/procmon-magglass-stop.png)         

        <span data-ttu-id="6baae-160">Ensuite, pour effacer la capture précédente, sélectionnez l’icône de gomme.</span><span class="sxs-lookup"><span data-stu-id="6baae-160">Next, to clear the earlier capture, select the eraser icon.</span></span>

        ![icône effacer](images/procmon-eraser-clear.png)

        <span data-ttu-id="6baae-162">Vous pouvez également utiliser le raccourci clavier **Ctrl+X**.</span><span class="sxs-lookup"><span data-stu-id="6baae-162">Or use the keyboard shortcut **Ctrl+X**.</span></span>

    2. <span data-ttu-id="6baae-163">La deuxième consiste à exécuter la ligne de **commande en** tant qu’administrateur, puis à partir du chemin d’accès du moniteur de processus, exécutez :</span><span class="sxs-lookup"><span data-stu-id="6baae-163">The second way is to run the **command line** as admin, then from the Process Monitor path, run:</span></span>

        ![procmon cmd](images/cmd-procmon.png)
 
        ```console
        Procmon.exe /AcceptEula /Noconnect /Profiling
        ```
        
        >[!TIP] 
        ><span data-ttu-id="6baae-165">Faites en sorte que la fenêtre ProcMon soit aussi petite que possible lors de la capture des données afin que vous pouvez facilement démarrer et arrêter le suivi.</span><span class="sxs-lookup"><span data-stu-id="6baae-165">Make the ProcMon window as small as possible when capturing data so you can easily start and stop the trace.</span></span>
        > 
        >![Réduire procmon](images/procmon-minimize.png)
    
7. <span data-ttu-id="6baae-167">Après avoir suivi l’une des procédures de l’étape 6, vous verrez ensuite une option pour définir des filtres.</span><span class="sxs-lookup"><span data-stu-id="6baae-167">After following one of the procedures in step 6, you'll next see an option to set filters.</span></span> <span data-ttu-id="6baae-168">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="6baae-168">Select **OK**.</span></span> <span data-ttu-id="6baae-169">Vous pouvez toujours filtrer les résultats une fois la capture terminée.</span><span class="sxs-lookup"><span data-stu-id="6baae-169">You can always filter the results after the capture is completed.</span></span>
 
    ![Filtrer le nom du processus est Exclusion du système](images/procmon-filter-options.png) 

8. <span data-ttu-id="6baae-171">Pour démarrer la capture, sélectionnez de nouveau l’icône en forme de loupe.</span><span class="sxs-lookup"><span data-stu-id="6baae-171">To start the capture, select the magnifying glass icon again.</span></span>
     
9. <span data-ttu-id="6baae-172">Reproduisez le problème.</span><span class="sxs-lookup"><span data-stu-id="6baae-172">Reproduce the problem.</span></span>
 
    >[!TIP] 
    ><span data-ttu-id="6baae-173">Attendez que le problème soit entièrement reproduit, puis notez l’timestamp au début du suivi.</span><span class="sxs-lookup"><span data-stu-id="6baae-173">Wait for the problem to be fully reproduced, then take note of the timestamp when the trace started.</span></span>

10. <span data-ttu-id="6baae-174">Une fois que vous avez deux à quatre minutes d’activité de processus pendant la condition d’utilisation élevée du processeur, arrêtez la capture en sélectionnant l’icône de loupe.</span><span class="sxs-lookup"><span data-stu-id="6baae-174">Once you have two to four minutes of process activity during the high CPU usage condition, stop the capture by selecting the magnifying glass icon.</span></span>

11. <span data-ttu-id="6baae-175">Pour enregistrer la capture avec un nom unique et au format .pml, sélectionnez **Fichier,** puis **Enregistrer...**. Veillez à sélectionner les boutons d’radio **Tous les événements** et **le format PML (Native Process Monitor Format).**</span><span class="sxs-lookup"><span data-stu-id="6baae-175">To save the capture with a unique name and with the .pml format, select **File** then select **Save...**. Make sure to select the radio buttons **All events** and **Native Process Monitor Format (PML)**.</span></span>

    ![enregistrer les paramètres](images/procmon-savesettings1.png)

12. <span data-ttu-id="6baae-177">Pour un meilleur suivi, modifiez le chemin d’accès par `C:\temp\ProcessMonitor\LogFile.PML` défaut de l’endroit `C:\temp\ProcessMonitor\%ComputerName%_LogFile_MMDDYEAR_Repro_of_issue.PML` où :</span><span class="sxs-lookup"><span data-stu-id="6baae-177">For better tracking, change the default path from `C:\temp\ProcessMonitor\LogFile.PML` to `C:\temp\ProcessMonitor\%ComputerName%_LogFile_MMDDYEAR_Repro_of_issue.PML` where:</span></span>
    - <span data-ttu-id="6baae-178">`%ComputerName%` est le nom de l’appareil</span><span class="sxs-lookup"><span data-stu-id="6baae-178">`%ComputerName%` is the device name</span></span>
    - <span data-ttu-id="6baae-179">`MMDDYEAR` est le mois, le jour et l’année</span><span class="sxs-lookup"><span data-stu-id="6baae-179">`MMDDYEAR` is the month, day, and year</span></span>
    -  <span data-ttu-id="6baae-180">`Repro_of_issue` est le nom du problème que vous essayez de reproduire</span><span class="sxs-lookup"><span data-stu-id="6baae-180">`Repro_of_issue` is the name of the issue you're trying to reproduce</span></span>

    >[!TIP] 
    > <span data-ttu-id="6baae-181">Si vous avez un système de travail, vous souhaitez peut-être obtenir un exemple de journal à comparer.</span><span class="sxs-lookup"><span data-stu-id="6baae-181">If you have a working system, you might want to get a sample log to compare.</span></span>

13. <span data-ttu-id="6baae-182">Zip the .pml file and submit it to Microsoft support.</span><span class="sxs-lookup"><span data-stu-id="6baae-182">Zip the .pml file and submit it to Microsoft support.</span></span>


## <a name="capture-performance-logs-using-windows-performance-recorder"></a><span data-ttu-id="6baae-183">Capturer les journaux de performances à l’aide Windows Enregistreur de performances</span><span class="sxs-lookup"><span data-stu-id="6baae-183">Capture performance logs using Windows Performance Recorder</span></span>

<span data-ttu-id="6baae-184">Vous pouvez utiliser Windows enregistreur de performances (WPR) pour inclure des informations supplémentaires dans votre soumission au support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6baae-184">You can use Windows Performance Recorder (WPR) to include additional information in your submission to Microsoft support.</span></span> <span data-ttu-id="6baae-185">WPR est un outil d’enregistrement puissant qui crée le suivi des événements pour Windows enregistrements.</span><span class="sxs-lookup"><span data-stu-id="6baae-185">WPR is a powerful recording tool that creates Event Tracing for Windows recordings.</span></span> 

<span data-ttu-id="6baae-186">WPR fait partie du Kit de déploiement et d’évaluation Windows (Windows ADK) et peut être téléchargé à partir du téléchargement et de l’installation du [kit Windows ADK.](/windows-hardware/get-started/adk-install)</span><span class="sxs-lookup"><span data-stu-id="6baae-186">WPR is part of the Windows Assessment and Deployment Kit (Windows ADK) and can be downloaded from [Download and install the Windows ADK](/windows-hardware/get-started/adk-install).</span></span> <span data-ttu-id="6baae-187">Vous pouvez également le télécharger dans le cadre du Kit de développement logiciel Windows 10 sur [Windows 10 SDK.](https://developer.microsoft.com/windows/downloads/windows-10-sdk/)</span><span class="sxs-lookup"><span data-stu-id="6baae-187">You can also download it as part of the Windows 10 Software Development Kit at [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk/).</span></span>

<span data-ttu-id="6baae-188">Vous pouvez utiliser l’interface utilisateur WPR en suivant les étapes de capture des journaux de performances à l’aide de [l’interface utilisateur WPR.](#capture-performance-logs-using-the-wpr-ui)</span><span class="sxs-lookup"><span data-stu-id="6baae-188">You can use the WPR user interface by following the steps in [Capture performance logs using the WPR UI](#capture-performance-logs-using-the-wpr-ui).</span></span> 

<span data-ttu-id="6baae-189">Vous pouvez également utiliser l’outil en ligne de commande *wpr.exe*, qui est disponible dans Windows 8 et versions ultérieures en suivant les étapes de capture des journaux de performances à l’aide de [l’CLI WPR.](#capture-performance-logs-using-the-wpr-cli)</span><span class="sxs-lookup"><span data-stu-id="6baae-189">Alternatively, you can also use the command-line tool *wpr.exe*, which is available in Windows 8 and later versions  by following the steps in [Capture performance logs using the WPR CLI](#capture-performance-logs-using-the-wpr-cli).</span></span>


### <a name="capture-performance-logs-using-the-wpr-ui"></a><span data-ttu-id="6baae-190">Capturer les journaux de performances à l’aide de l’interface utilisateur WPR</span><span class="sxs-lookup"><span data-stu-id="6baae-190">Capture performance logs using the WPR UI</span></span>

>[!TIP]
><span data-ttu-id="6baae-191">Si vous avez plusieurs appareils sur lesquels le problème se produit, utilisez celui qui a la plus grande quantité de RAM.</span><span class="sxs-lookup"><span data-stu-id="6baae-191">If you have multiple devices where the issue is occurring, use the one which has the most amount of RAM.</span></span>

1. <span data-ttu-id="6baae-192">Téléchargez et installez WPR.</span><span class="sxs-lookup"><span data-stu-id="6baae-192">Download and install WPR.</span></span>

2. <span data-ttu-id="6baae-193">Sous *kits Windows,* cliquez avec le bouton droit sur **Windows Enregistreur de performances.**</span><span class="sxs-lookup"><span data-stu-id="6baae-193">Under *Windows Kits*, right-click **Windows Performance Recorder**.</span></span> 

    ![Menu Démarrer](images/wpr-01.png)

    <span data-ttu-id="6baae-195">Sélectionnez **plus**.</span><span class="sxs-lookup"><span data-stu-id="6baae-195">Select **More**.</span></span> <span data-ttu-id="6baae-196">Sélectionnez **Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="6baae-196">Select **Run as administrator**.</span></span>

3. <span data-ttu-id="6baae-197">Lorsque la boîte de dialogue Contrôle de compte d’utilisateur s’affiche, sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="6baae-197">When the User Account Control dialog box appears, select **Yes**.</span></span>

    ![UAC](images/wpt-yes.png)

4. <span data-ttu-id="6baae-199">Ensuite, téléchargez le [profil d’analyse microsoft Defender pour point](https://github.com/YongRhee-MDE/Scripts/blob/master/MDAV.wprp) de terminaison et enregistrez-le dans un dossier tel que `MDAV.wprp` `C:\temp` .</span><span class="sxs-lookup"><span data-stu-id="6baae-199">Next, download the [Microsoft Defender for Endpoint analysis](https://github.com/YongRhee-MDE/Scripts/blob/master/MDAV.wprp) profile and save as `MDAV.wprp` to a folder like `C:\temp`.</span></span> 
     
5. <span data-ttu-id="6baae-200">Dans la boîte de dialogue WPR, sélectionnez **Plus d’options.**</span><span class="sxs-lookup"><span data-stu-id="6baae-200">On the WPR dialog box, select **More options**.</span></span>

    ![Sélectionner d’autres options](images/wpr-03.png)

6. <span data-ttu-id="6baae-202">Sélectionnez **Ajouter des profils...** et accédez au chemin d’accès du `MDAV.wprp` fichier.</span><span class="sxs-lookup"><span data-stu-id="6baae-202">Select **Add Profiles...** and browse to the path of the `MDAV.wprp` file.</span></span>

7. <span data-ttu-id="6baae-203">Après cela, vous devriez voir un nouveau profil sous Mesures *personnalisées nommées* Analyse du point de terminaison *Microsoft Defender* en dessous.</span><span class="sxs-lookup"><span data-stu-id="6baae-203">After that, you should see a new profile set under *Custom measurements* named *Microsoft Defender for Endpoint analysis* underneath it.</span></span>

    ![dans le fichier](images/wpr-infile.png)

    >[!WARNING]
    ><span data-ttu-id="6baae-205">Si votre serveur Windows a 64 Go de RAM ou plus, utilisez la mesure personnalisée `Microsoft Defender for Endpoint analysis for large servers` au lieu de `Microsoft Defender for Endpoint analysis` .</span><span class="sxs-lookup"><span data-stu-id="6baae-205">If your Windows Server has 64 GB of RAM or more, use the custom measurement `Microsoft Defender for Endpoint analysis for large servers` instead of `Microsoft Defender for Endpoint analysis`.</span></span> <span data-ttu-id="6baae-206">Dans le cas contraire, votre système pourrait consommer une quantité élevée de mémoires ou de mémoires tampons de pool non pagyés, ce qui peut entraîner une instabilité du système.</span><span class="sxs-lookup"><span data-stu-id="6baae-206">Otherwise, your system could consume a high amount of non-paged pool memory or buffers which can lead to system instability.</span></span> <span data-ttu-id="6baae-207">Vous pouvez choisir les profils à ajouter en **développez l’analyse des ressources.**</span><span class="sxs-lookup"><span data-stu-id="6baae-207">You can choose which profiles to add by expanding **Resource Analysis**.</span></span> <span data-ttu-id="6baae-208">Ce profil personnalisé fournit le contexte nécessaire pour une analyse approfondie des performances.</span><span class="sxs-lookup"><span data-stu-id="6baae-208">This custom profile provides the necessary context for in-depth performance analysis.</span></span>
 
8. <span data-ttu-id="6baae-209">Pour utiliser le profil d’analyse détaillée de la mesure personnalisée Microsoft Defender pour point de terminaison dans l’interface utilisateur WPR :</span><span class="sxs-lookup"><span data-stu-id="6baae-209">To use the custom measurement Microsoft Defender for Endpoint verbose analysis profile in the WPR UI:</span></span>

    1. <span data-ttu-id="6baae-210">Assurez-vous qu’aucun profil n’est sélectionné dans les groupes *Tri de premier* niveau, Analyse *des* ressources et *Analyse de* scénario.</span><span class="sxs-lookup"><span data-stu-id="6baae-210">Ensure no profiles are selected under the *First-level triage*, *Resource Analysis* and *Scenario Analysis* groups.</span></span>
    2. <span data-ttu-id="6baae-211">Sélectionnez **mesures personnalisées.**</span><span class="sxs-lookup"><span data-stu-id="6baae-211">Select **Custom measurements**.</span></span>
    3. <span data-ttu-id="6baae-212">Sélectionnez **Microsoft Defender pour l’analyse des points de terminaison.**</span><span class="sxs-lookup"><span data-stu-id="6baae-212">Select **Microsoft Defender for Endpoint analysis**.</span></span>
    4. <span data-ttu-id="6baae-213">Sélectionnez **Détaillé sous** *niveau* Détails.</span><span class="sxs-lookup"><span data-stu-id="6baae-213">Select **Verbose** under *Detail* level.</span></span>
    1. <span data-ttu-id="6baae-214">Sélectionnez **Fichier ou** **Mémoire en** mode Journalisation.</span><span class="sxs-lookup"><span data-stu-id="6baae-214">Select **File** or **Memory** under Logging mode.</span></span> 

    >[!important]
    ><span data-ttu-id="6baae-215">Vous devez sélectionner *Fichier* pour utiliser le mode de journalisation des fichiers si le problème de performances peut être reproduit directement par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6baae-215">You should select *File* to use the file logging mode if the performance issue can be reproduced directly by the user.</span></span> <span data-ttu-id="6baae-216">La plupart des problèmes relèvent de cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="6baae-216">Most issues fall under this category.</span></span> <span data-ttu-id="6baae-217">Toutefois, si l’utilisateur ne peut pas reproduire directement le problème mais  qu’il peut facilement le remarquer une fois le problème se produit, l’utilisateur doit sélectionner Mémoire pour utiliser le mode de journalisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="6baae-217">However, if the user cannot directly reproduce the issue but can easily notice it once the issue occurs, the user should select *Memory* to use the memory logging mode.</span></span> <span data-ttu-id="6baae-218">Cela permet de s’assurer que le journal de suivi n’est pas excessivement insérable en raison du temps de longue durée.</span><span class="sxs-lookup"><span data-stu-id="6baae-218">This ensures that the trace log will not inflate excessively due to the long run time.</span></span>

9. <span data-ttu-id="6baae-219">Vous êtes maintenant prêt à collecter des données.</span><span class="sxs-lookup"><span data-stu-id="6baae-219">Now you're ready to collect data.</span></span> <span data-ttu-id="6baae-220">Quittez toutes les applications qui ne sont pas pertinentes pour reproduire le problème de performances.</span><span class="sxs-lookup"><span data-stu-id="6baae-220">Exit all the applications that are not relevant to reproducing the performance issue.</span></span> <span data-ttu-id="6baae-221">Vous pouvez sélectionner **les options Masquer pour** que l’espace occupé par la fenêtre WPR reste petit.</span><span class="sxs-lookup"><span data-stu-id="6baae-221">You can select **Hide options** to keep the space occupied by the WPR window small.</span></span>

    ![Options hipe](images/wpr-08.png)

    >[!TIP]
    ><span data-ttu-id="6baae-223">Essayez de démarrer le suivi à un nombre entier de secondes.</span><span class="sxs-lookup"><span data-stu-id="6baae-223">Try starting the trace at whole number seconds.</span></span> <span data-ttu-id="6baae-224">Par exemple, 01:30:00.</span><span class="sxs-lookup"><span data-stu-id="6baae-224">For instance, 01:30:00.</span></span> <span data-ttu-id="6baae-225">Cela facilite l’analyse des données.</span><span class="sxs-lookup"><span data-stu-id="6baae-225">This will make it easier to analyze the data.</span></span> <span data-ttu-id="6baae-226">Essayez également d’assurer le suivi de l’timestamp du moment exact où le problème est reproduit.</span><span class="sxs-lookup"><span data-stu-id="6baae-226">Also try to keep track of the timestamp of exactly when the issue is reproduced.</span></span>

10. <span data-ttu-id="6baae-227">Sélectionnez **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="6baae-227">Select **Start**.</span></span>

    ![Sélectionner le début du suivi](images/wpr-09.png)

11. <span data-ttu-id="6baae-229">Reproduisez le problème.</span><span class="sxs-lookup"><span data-stu-id="6baae-229">Reproduce the issue.</span></span>

    >[!TIP]
    ><span data-ttu-id="6baae-230">Conservez la collecte de données au plus cinq minutes.</span><span class="sxs-lookup"><span data-stu-id="6baae-230">Keep the data collection to no more than five minutes.</span></span> <span data-ttu-id="6baae-231">Deux à trois minutes sont une bonne plage, car un grand nombre de données sont collectées.</span><span class="sxs-lookup"><span data-stu-id="6baae-231">Two to three minutes is a good range since a lot of data is being collected.</span></span>

12. <span data-ttu-id="6baae-232">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6baae-232">Select **Save**.</span></span>

    ![Sélectionnez Enregistrer](images/wpr-10.png)

13. <span data-ttu-id="6baae-234">Remplissez **Type dans une description détaillée** du problème : avec des informations sur le problème et la façon dont vous avez reproduit le problème.</span><span class="sxs-lookup"><span data-stu-id="6baae-234">Fill up **Type in a detailed description of the problem:** with information about the problem and how you reproduced the issue.</span></span>

    ![Remplir les détails](images/wpr-12.png)

    1. <span data-ttu-id="6baae-236">Sélectionnez **Nom de fichier :** pour déterminer l’endroit où votre fichier de suivi sera enregistré.</span><span class="sxs-lookup"><span data-stu-id="6baae-236">Select **File Name:** to determine where your trace file will be saved.</span></span> <span data-ttu-id="6baae-237">Par défaut, il 1.is enregistré dans `%user%\Documents\WPR Files\` .</span><span class="sxs-lookup"><span data-stu-id="6baae-237">By default, it 1.is saved to `%user%\Documents\WPR Files\`.</span></span>
    1. <span data-ttu-id="6baae-238">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6baae-238">Select **Save**.</span></span>

14. <span data-ttu-id="6baae-239">Patientez pendant la fusion du suivi.</span><span class="sxs-lookup"><span data-stu-id="6baae-239">Wait while the trace is being merged.</span></span>

    ![WPR collecte du suivi général](images/wpr-13.png)

15. <span data-ttu-id="6baae-241">Une fois le suivi enregistré, sélectionnez **Ouvrir le dossier.**</span><span class="sxs-lookup"><span data-stu-id="6baae-241">Once the trace is saved, select **Open folder**.</span></span>

    ![Suivi WPR enregistré](images/wpr-14.png)

    <span data-ttu-id="6baae-243">Incluez à la fois le fichier et le dossier dans votre soumission au support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6baae-243">Include both the file and the folder in your submission to Microsoft support.</span></span>

    ![Fichier et dossier](images/wpr-15.png)

### <a name="capture-performance-logs-using-the-wpr-cli"></a><span data-ttu-id="6baae-245">Capturer les journaux de performances à l’aide de l’CLI WPR</span><span class="sxs-lookup"><span data-stu-id="6baae-245">Capture performance logs using the WPR CLI</span></span>

<span data-ttu-id="6baae-246">L’outil en ligne *dewpr.exe* fait partie du système d’exploitation en commençant par Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6baae-246">The command-line tool *wpr.exe* is part of the operating system starting with Windows 8.</span></span> <span data-ttu-id="6baae-247">Pour collecter un suivi WPR à l’aide de l’outil en ligne de wpr.exe :</span><span class="sxs-lookup"><span data-stu-id="6baae-247">To collect a WPR trace using the command-line tool wpr.exe:</span></span>

1. <span data-ttu-id="6baae-248">Téléchargez **[le profil d’analyse](https://github.com/YongRhee-MDE/Scripts/blob/master/MDAV.wprp)** De Microsoft Defender pour point de terminaison pour le suivi des performances vers un fichier nommé dans un `MDAV.wprp` répertoire local tel que `C:\traces` .</span><span class="sxs-lookup"><span data-stu-id="6baae-248">Download **[Microsoft Defender for Endpoint analysis](https://github.com/YongRhee-MDE/Scripts/blob/master/MDAV.wprp)** profile for performance traces to a file named `MDAV.wprp` in a local directory such as `C:\traces`.</span></span>

3. <span data-ttu-id="6baae-249">Cliquez avec  le bouton droit sur l’icône Menu Démarrer et sélectionnez **Windows PowerShell (administrateur)** ou l’invite de commandes **(Administrateur)** pour ouvrir une fenêtre d’invite de commandes d’administration.</span><span class="sxs-lookup"><span data-stu-id="6baae-249">Right-click the **Start Menu** icon and select **Windows PowerShell (Admin)** or **Command Prompt (Admin)** to open an Admin command prompt window.</span></span>

4. <span data-ttu-id="6baae-250">Lorsque la boîte de dialogue Contrôle de compte d’utilisateur s’affiche, sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="6baae-250">When the User Account Control dialog box appears, select **Yes**.</span></span>

5. <span data-ttu-id="6baae-251">À l’invite avec élévation de droits, exécutez la commande suivante pour démarrer un suivi des performances de Microsoft Defender for Endpoint :</span><span class="sxs-lookup"><span data-stu-id="6baae-251">At the elevated prompt, run the following command to start a Microsoft Defender for Endpoint performance trace:</span></span>

    ```console
    wpr.exe -start C:\traces\MDAV.wprp!WD.Verbose -filemode
    ```
    
    >[!WARNING]
    ><span data-ttu-id="6baae-252">Si votre serveur Windows dispose de 64 Go ou de RAM ou plus, utilisez des profils et non des profils `WDForLargeServers.Light` `WDForLargeServers.Verbose` `WD.Light` `WD.Verbose` et, respectivement.</span><span class="sxs-lookup"><span data-stu-id="6baae-252">If your Windows Server has 64 GB or RAM or more, use profiles `WDForLargeServers.Light` and `WDForLargeServers.Verbose` instead of profiles `WD.Light` and `WD.Verbose`, respectively.</span></span> <span data-ttu-id="6baae-253">Dans le cas contraire, votre système pourrait consommer une quantité élevée de mémoires ou de mémoires tampons de pool non pagyés, ce qui peut entraîner une instabilité du système.</span><span class="sxs-lookup"><span data-stu-id="6baae-253">Otherwise, your system could consume a high amount of non-paged pool memory or buffers which can lead to system instability.</span></span>

6. <span data-ttu-id="6baae-254">Reproduisez le problème.</span><span class="sxs-lookup"><span data-stu-id="6baae-254">Reproduce the issue.</span></span>

    >[!TIP]
    ><span data-ttu-id="6baae-255">Conservez la collecte de données au plus cinq minutes.</span><span class="sxs-lookup"><span data-stu-id="6baae-255">Keep the data collection no to more than five minutes.</span></span>  <span data-ttu-id="6baae-256">Selon le scénario, deux à trois minutes sont une bonne plage, car un grand nombre de données sont collectées.</span><span class="sxs-lookup"><span data-stu-id="6baae-256">Depending on the scenario, two to three minutes is a good range since a lot of data is being collected.</span></span>

7. <span data-ttu-id="6baae-257">À l’invite avec élévation de niveau élevé, exécutez la commande suivante pour arrêter le suivi des performances, en vous assurez de fournir des informations sur le problème et la façon dont vous avez reproduit le problème :</span><span class="sxs-lookup"><span data-stu-id="6baae-257">At the elevated prompt, run the following command to stop the performance trace, making sure to provide information about the problem and how you reproduced the issue:</span></span>

    ```console
    wpr.exe -stop merged.etl "Timestamp when the issue was reproduced, in HH:MM:SS format" "Description of the issue" "Any error that popped up"
    ```

8. <span data-ttu-id="6baae-258">Patientez jusqu’à ce que le suivi soit fusionné.</span><span class="sxs-lookup"><span data-stu-id="6baae-258">Wait until the trace is merged.</span></span> 

9. <span data-ttu-id="6baae-259">Incluez à la fois le fichier et le dossier dans votre soumission au support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6baae-259">Include both the file and the folder in your submission to Microsoft support.</span></span>

## <a name="see-also"></a><span data-ttu-id="6baae-260">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6baae-260">See also</span></span>

- [<span data-ttu-id="6baae-261">Collecter des Antivirus Microsoft Defender de diagnostic</span><span class="sxs-lookup"><span data-stu-id="6baae-261">Collect Microsoft Defender Antivirus diagnostic data</span></span>](collect-diagnostic-data.md)
- [<span data-ttu-id="6baae-262">Configurer et valider des exclusions pour Antivirus Microsoft Defender analyses</span><span class="sxs-lookup"><span data-stu-id="6baae-262">Configure and validate exclusions for Microsoft Defender Antivirus scans</span></span>](configure-exclusions-microsoft-defender-antivirus.md)
