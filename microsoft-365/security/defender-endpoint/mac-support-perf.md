---
title: Résoudre les problèmes de performances pour Microsoft Defender pour endpoint sur macOS
description: Résolution des problèmes de performances dans Microsoft Defender pour point de terminaison sur macOS.
keywords: microsoft, defender, atp, mac, performances
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 8dfaf1dbf2c3742cc97060c7f9e811c83d0cb023
ms.sourcegitcommit: 72ae1b49e7a3d3199272fcb4c39f5daec0d66f1a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51698219"
---
# <a name="troubleshoot-performance-issues-for-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="b04c9-104">Résoudre les problèmes de performances pour Microsoft Defender pour le point de terminaison sur macOS</span><span class="sxs-lookup"><span data-stu-id="b04c9-104">Troubleshoot performance issues for Microsoft Defender for Endpoint on macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="b04c9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b04c9-105">**Applies to:**</span></span>

- [<span data-ttu-id="b04c9-106">Microsoft Defender pour point de terminaison sur macOS</span><span class="sxs-lookup"><span data-stu-id="b04c9-106">Microsoft Defender for Endpoint on macOS</span></span>](microsoft-defender-endpoint-mac.md)
- [<span data-ttu-id="b04c9-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b04c9-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="b04c9-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b04c9-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="b04c9-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="b04c9-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="b04c9-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="b04c9-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="b04c9-111">Cette rubrique fournit quelques étapes générales qui peuvent être utilisées pour affiner les problèmes de performances liés à Microsoft Defender pour Endpoint sur macOS.</span><span class="sxs-lookup"><span data-stu-id="b04c9-111">This topic provides some general steps that can be used to narrow down performance issues related to Microsoft Defender for Endpoint on macOS.</span></span>

<span data-ttu-id="b04c9-112">La protection en temps réel (RTP) est une fonctionnalité de Microsoft Defender for Endpoint sur macOS qui surveille et protège en permanence votre appareil contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="b04c9-112">Real-time protection (RTP) is a feature of Microsoft Defender for Endpoint on macOS that continuously monitors and protects your device against threats.</span></span> <span data-ttu-id="b04c9-113">Il se compose de la surveillance des fichiers et des processus et d'autres heuristiques.</span><span class="sxs-lookup"><span data-stu-id="b04c9-113">It consists of file and process monitoring and other heuristics.</span></span>

<span data-ttu-id="b04c9-114">Selon les applications que vous exécutez et les caractéristiques de votre appareil, vous pouvez obtenir des performances sous-optimales lors de l'exécution de Microsoft Defender pour Endpoint sur macOS.</span><span class="sxs-lookup"><span data-stu-id="b04c9-114">Depending on the applications that you're running and your device characteristics, you may experience suboptimal performance when running Microsoft Defender for Endpoint on macOS.</span></span> <span data-ttu-id="b04c9-115">En particulier, les applications ou les processus système qui accèdent à de nombreuses ressources sur un court laps de temps peuvent entraîner des problèmes de performances dans Microsoft Defender pour Endpoint sur macOS.</span><span class="sxs-lookup"><span data-stu-id="b04c9-115">In particular, applications or system processes that access many resources over a short timespan can lead to performance issues in Microsoft Defender for Endpoint on macOS.</span></span>

<span data-ttu-id="b04c9-116">Les étapes suivantes peuvent être utilisées pour résoudre et atténuer ces problèmes :</span><span class="sxs-lookup"><span data-stu-id="b04c9-116">The following steps can be used to troubleshoot and mitigate these issues:</span></span>

1. <span data-ttu-id="b04c9-117">Désactivez la protection en temps réel à l'aide de l'une des méthodes suivantes et observez si les performances sont améliorées.</span><span class="sxs-lookup"><span data-stu-id="b04c9-117">Disable real-time protection using one of the following methods and observe whether the performance improves.</span></span> <span data-ttu-id="b04c9-118">Cette approche permet de déterminer si Microsoft Defender pour Point de terminaison sur macOS contribue aux problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="b04c9-118">This approach helps narrow down whether Microsoft Defender for Endpoint on macOS is contributing to the performance issues.</span></span>

      <span data-ttu-id="b04c9-119">Si votre appareil n'est pas géré par votre organisation, la protection en temps réel peut être désactivée à l'aide de l'une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="b04c9-119">If your device is not managed by your organization, real-time protection can be disabled using one of the following options:</span></span>

    - <span data-ttu-id="b04c9-120">À partir de l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b04c9-120">From the user interface.</span></span> <span data-ttu-id="b04c9-121">Ouvrez Microsoft Defender pour le point de terminaison sur macOS et accédez à **Gérer les paramètres.**</span><span class="sxs-lookup"><span data-stu-id="b04c9-121">Open Microsoft Defender for Endpoint on macOS and navigate to **Manage settings**.</span></span>

      ![Capture d'écran gérer la protection en temps réel](images/mdatp-36-rtp.png)

    - <span data-ttu-id="b04c9-123">À partir du terminal.</span><span class="sxs-lookup"><span data-stu-id="b04c9-123">From the Terminal.</span></span> <span data-ttu-id="b04c9-124">Pour des raisons de sécurité, cette opération nécessite une élévation.</span><span class="sxs-lookup"><span data-stu-id="b04c9-124">For security purposes, this operation requires elevation.</span></span>

      ```bash
      mdatp config real-time-protection --value disabled
      ```

      <span data-ttu-id="b04c9-125">Si votre appareil est géré par votre organisation, la protection en temps réel peut être désactivée par votre administrateur à l'aide des instructions dans Définir les préférences de Microsoft Defender pour Endpoint sur [macOS.](mac-preferences.md)</span><span class="sxs-lookup"><span data-stu-id="b04c9-125">If your device is managed by your organization, real-time protection can be disabled by your administrator using the instructions in [Set preferences for Microsoft Defender for Endpoint on macOS](mac-preferences.md).</span></span>
      
      <span data-ttu-id="b04c9-126">Si le problème de performances persiste alors que la protection en temps réel est éteinte, l'origine du problème peut être le composant de détection et de réponse du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b04c9-126">If the performance problem persists while real-time protection is off, the origin of the problem could be the endpoint detection and response component.</span></span> <span data-ttu-id="b04c9-127">Dans ce cas, contactez le support technique pour obtenir des instructions supplémentaires et des mesures d'atténuation.</span><span class="sxs-lookup"><span data-stu-id="b04c9-127">In this case, please contact customer support for further instructions and mitigation.</span></span>

2. <span data-ttu-id="b04c9-128">Ouvrez Finder et accédez aux  >  **utilitaires d'applications.**</span><span class="sxs-lookup"><span data-stu-id="b04c9-128">Open Finder and navigate to **Applications** > **Utilities**.</span></span> <span data-ttu-id="b04c9-129">Ouvrez **l'Analyseur** d'activité et analysez les applications qui utilisent les ressources de votre système.</span><span class="sxs-lookup"><span data-stu-id="b04c9-129">Open **Activity Monitor** and analyze which applications are using the resources on your system.</span></span> <span data-ttu-id="b04c9-130">Les compilateurs et les outils de mise à jour logicielles sont des exemples classiques.</span><span class="sxs-lookup"><span data-stu-id="b04c9-130">Typical examples include software updaters and compilers.</span></span>

1. <span data-ttu-id="b04c9-131">Pour rechercher les applications qui déclenchent le plus d'analyses, vous pouvez utiliser les statistiques en temps réel recueillies par Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="b04c9-131">To find the applications that are triggering the most scans, you can use real-time statistics gathered by Defender for Endpoint for Mac.</span></span>

      > [!NOTE]
      > <span data-ttu-id="b04c9-132">Cette fonctionnalité est disponible dans la version 100.90.70 ou une version plus récente.</span><span class="sxs-lookup"><span data-stu-id="b04c9-132">This feature is available in version 100.90.70 or newer.</span></span>
      <span data-ttu-id="b04c9-133">Cette fonctionnalité est activée par défaut sur les canaux **Dog food** et **InsiderFast.**</span><span class="sxs-lookup"><span data-stu-id="b04c9-133">This feature is enabled by default on the **Dogfood** and **InsiderFast** channels.</span></span> <span data-ttu-id="b04c9-134">Si vous utilisez un autre canal de mise à jour, cette fonctionnalité peut être activée à partir de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="b04c9-134">If you're using a different update channel, this feature can be enabled from the command line:</span></span>
      ```bash
      mdatp config real-time-protection-statistics  --value enabled
      ```

      <span data-ttu-id="b04c9-135">Cette fonctionnalité nécessite une protection en temps réel pour être activée.</span><span class="sxs-lookup"><span data-stu-id="b04c9-135">This feature requires real-time protection to be enabled.</span></span> <span data-ttu-id="b04c9-136">Pour vérifier l'état de la protection en temps réel, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b04c9-136">To check the status of real-time protection, run the following command:</span></span>

      ```bash
      mdatp health --field real_time_protection_enabled
      ```

    <span data-ttu-id="b04c9-137">Vérifiez que **l'entrée real_time_protection_enabled** est vraie.</span><span class="sxs-lookup"><span data-stu-id="b04c9-137">Verify that the **real_time_protection_enabled** entry is true.</span></span> <span data-ttu-id="b04c9-138">Sinon, exécutez la commande suivante pour l'activer :</span><span class="sxs-lookup"><span data-stu-id="b04c9-138">Otherwise, run the following command to enable it:</span></span>

      ```bash
      mdatp config real-time-protection --value enabled
      ```

      ```output
      Configuration property updated
      ```

      <span data-ttu-id="b04c9-139">Pour collecter les statistiques actuelles, exécutez :</span><span class="sxs-lookup"><span data-stu-id="b04c9-139">To collect current statistics, run:</span></span>

      ```bash
      mdatp config real-time-protection --value enabled
      ```

      > [!NOTE]
      > <span data-ttu-id="b04c9-140">L'utilisation du json de sortie **(notez** le tiret double) garantit que le format de sortie est prêt pour l'utilisation.</span><span class="sxs-lookup"><span data-stu-id="b04c9-140">Using **--output json** (note the double dash) ensures that the output format is ready for parsing.</span></span>
      <span data-ttu-id="b04c9-141">Le résultat de cette commande affiche tous les processus et l'activité d'analyse associée.</span><span class="sxs-lookup"><span data-stu-id="b04c9-141">The output of this command will show all processes and their associated scan activity.</span></span>

1. <span data-ttu-id="b04c9-142">Sur votre système Mac, téléchargez l'exemple d'analyseur Python high_cpu_parser.py à l'aide de la commande :</span><span class="sxs-lookup"><span data-stu-id="b04c9-142">On your Mac system, download the sample Python parser high_cpu_parser.py using the command:</span></span>

    ```bash
    wget -c https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/linux/diagnostic/high_cpu_parser.py
    ```

    <span data-ttu-id="b04c9-143">La sortie de cette commande doit être similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="b04c9-143">The output of this command should be similar to the following:</span></span>

    ```Output
    --2020-11-14 11:27:27-- https://raw.githubusercontent.com/microsoft.
    mdatp-xplat/master/linus/diagnostic/high_cpu_parser.py
    Resolving raw.githubusercontent.com (raw.githubusercontent.com)... 151.101.xxx.xxx
    Connecting to raw.githubusercontent.com (raw.githubusercontent.com)| 151.101.xxx.xxx| :443... connected.
    HTTP request sent, awaiting response... 200 OK
    Length: 1020 [text/plain]
    Saving to: 'high_cpu_parser.py'
    100%[===========================================>] 1,020    --.-K/s   in 
    0s
    ```

1. <span data-ttu-id="b04c9-144">Ensuite, tapez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b04c9-144">Next, type the following commands:</span></span>

      ```bash
        chmod +x high_cpu_parser.py
      ```

      ```bash
        cat real_time_protection.json | python high_cpu_parser.py  > real_time_protection.log
      ```

      <span data-ttu-id="b04c9-145">La sortie de ce qui précède est une liste des principaux contributeurs aux problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="b04c9-145">The output of the above is a list of the top contributors to performance issues.</span></span> <span data-ttu-id="b04c9-146">La première colonne est l'identificateur de processus (PID), la deuxième colonne est le nom du processus te et la dernière colonne le nombre de fichiers analysés, triés par impact.</span><span class="sxs-lookup"><span data-stu-id="b04c9-146">The first column is the process identifier (PID), the second column is te process name, and the last column is the number of scanned files, sorted by impact.</span></span>

      <span data-ttu-id="b04c9-147">Par exemple, la sortie de la commande ressemblera à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b04c9-147">For example, the output of the command will be something like the below:</span></span>

      ```output
        ... > python ~/repo/mdatp-xplat/linux/diagnostic/high_cpu_parser.py <~Downloads/output.json | head -n 10
        27432 None 76703
        73467 actool     1249
        73914 xcodebuild 1081
        73873 bash 1050
        27475 None 836
        1    launchd    407
        73468 ibtool     344
        549  telemetryd_v1   325
        4764 None 228
        125  CrashPlanService 164
      ```

      <span data-ttu-id="b04c9-148">Pour améliorer les performances de Defender pour Point de terminaison sur Mac, recherchez celui qui a le plus grand nombre sous la ligne Nombre total de fichiers analysés et ajoutez une exclusion pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="b04c9-148">To improve the performance of Defender for Endpoint on Mac, locate the one with the highest number under the Total files scanned row and add an exclusion for it.</span></span> <span data-ttu-id="b04c9-149">Pour plus d'informations, voir Configurer et valider des [exclusions pour Defender pour Endpoint sur Linux.](linux-exclusions.md)</span><span class="sxs-lookup"><span data-stu-id="b04c9-149">For more information, see [Configure and validate exclusions for Defender for Endpoint on Linux](linux-exclusions.md).</span></span>

      > [!NOTE]
      > <span data-ttu-id="b04c9-150">L'application stocke les statistiques en mémoire et suit uniquement l'activité des fichiers depuis son début et que la protection en temps réel a été activée.</span><span class="sxs-lookup"><span data-stu-id="b04c9-150">The application stores statistics in memory and only keeps track of file activity since it was started and real-time protection was enabled.</span></span> <span data-ttu-id="b04c9-151">Les processus qui ont été lancés avant ou pendant les périodes où la protection en temps réel était hors programme ne sont pas comptabilisés.</span><span class="sxs-lookup"><span data-stu-id="b04c9-151">Processes that were launched before or during periods when real time protection was off are not counted.</span></span> <span data-ttu-id="b04c9-152">En outre, seuls les événements qui ont déclenché des analyses sont comptés.</span><span class="sxs-lookup"><span data-stu-id="b04c9-152">Additionally, only events which triggered scans are counted.</span></span>
      > 
1. <span data-ttu-id="b04c9-153">Configurez Microsoft Defender pour endpoint sur macOS avec des exclusions pour les processus ou les emplacements de disque qui contribuent aux problèmes de performances et activez à nouveau la protection en temps réel.</span><span class="sxs-lookup"><span data-stu-id="b04c9-153">Configure Microsoft Defender for Endpoint on macOS with exclusions for the processes or disk locations that contribute to the performance issues and re-enable real-time protection.</span></span>

     <span data-ttu-id="b04c9-154">Pour plus d'informations, voir Configurer et valider des [exclusions pour Microsoft Defender for Endpoint sur macOS.](mac-exclusions.md)</span><span class="sxs-lookup"><span data-stu-id="b04c9-154">See [Configure and validate exclusions for Microsoft Defender for Endpoint on macOS](mac-exclusions.md) for details.</span></span>
