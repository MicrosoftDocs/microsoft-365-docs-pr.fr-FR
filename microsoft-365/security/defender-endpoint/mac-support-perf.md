---
title: Résoudre les problèmes de performances pour Microsoft Defender pour Endpoint pour Mac
description: Résolution des problèmes de performances dans Microsoft Defender pour Point de terminaison pour Mac.
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
ms.openlocfilehash: 6ff93b44627cf876384522f0c4f25d22347c8661
ms.sourcegitcommit: 7b8104015a76e02bc215e1cf08069979c70650ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/31/2021
ms.locfileid: "51476254"
---
# <a name="troubleshoot-performance-issues-for-microsoft-defender-for-endpoint-for-mac"></a><span data-ttu-id="0d06a-104">Résoudre les problèmes de performances pour Microsoft Defender pour Endpoint pour Mac</span><span class="sxs-lookup"><span data-stu-id="0d06a-104">Troubleshoot performance issues for Microsoft Defender for Endpoint for Mac</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="0d06a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0d06a-105">**Applies to:**</span></span>

- [<span data-ttu-id="0d06a-106">Microsoft Defender pour point de terminaison Mac</span><span class="sxs-lookup"><span data-stu-id="0d06a-106">Microsoft Defender for Endpoint for Mac</span></span>](microsoft-defender-endpoint-mac.md)
- [<span data-ttu-id="0d06a-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0d06a-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="0d06a-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0d06a-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="0d06a-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="0d06a-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="0d06a-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="0d06a-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="0d06a-111">Cette rubrique fournit quelques étapes générales qui peuvent être utilisées pour affiner les problèmes de performances liés à Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="0d06a-111">This topic provides some general steps that can be used to narrow down performance issues related to Microsoft Defender for Endpoint for Mac.</span></span>

<span data-ttu-id="0d06a-112">La protection en temps réel (RTP) est une fonctionnalité de Microsoft Defender pour Endpoint pour Mac qui surveille et protège en permanence votre appareil contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="0d06a-112">Real-time protection (RTP) is a feature of Microsoft Defender for Endpoint for Mac that continuously monitors and protects your device against threats.</span></span> <span data-ttu-id="0d06a-113">Il se compose de la surveillance des fichiers et des processus, ainsi que d’autres heuristiques.</span><span class="sxs-lookup"><span data-stu-id="0d06a-113">It consists of file and process monitoring and other heuristics.</span></span>

<span data-ttu-id="0d06a-114">Selon les applications que vous exécutez et les caractéristiques de votre appareil, vous pouvez obtenir des performances sous-optimales lors de l’exécution de Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="0d06a-114">Depending on the applications that you're running and your device characteristics, you may experience suboptimal performance when running Microsoft Defender for Endpoint for Mac.</span></span> <span data-ttu-id="0d06a-115">En particulier, les applications ou les processus système qui accèdent à de nombreuses ressources sur un court laps de temps peuvent entraîner des problèmes de performances dans Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="0d06a-115">In particular, applications or system processes that access many resources over a short timespan can lead to performance issues in Microsoft Defender for Endpoint for Mac.</span></span>

<span data-ttu-id="0d06a-116">Les étapes suivantes peuvent être utilisées pour résoudre et atténuer ces problèmes :</span><span class="sxs-lookup"><span data-stu-id="0d06a-116">The following steps can be used to troubleshoot and mitigate these issues:</span></span>

1. <span data-ttu-id="0d06a-117">Désactivez la protection en temps réel à l’aide de l’une des méthodes suivantes et observez si les performances s’améliorent.</span><span class="sxs-lookup"><span data-stu-id="0d06a-117">Disable real-time protection using one of the following methods and observe whether the performance improves.</span></span> <span data-ttu-id="0d06a-118">Cette approche permet de déterminer si Microsoft Defender pour Endpoint pour Mac contribue aux problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="0d06a-118">This approach helps narrow down whether Microsoft Defender for Endpoint for Mac is contributing to the performance issues.</span></span>

      <span data-ttu-id="0d06a-119">Si votre appareil n’est pas géré par votre organisation, la protection en temps réel peut être désactivée à l’aide de l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="0d06a-119">If your device is not managed by your organization, real-time protection can be disabled using one of the following options:</span></span>

    - <span data-ttu-id="0d06a-120">À partir de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0d06a-120">From the user interface.</span></span> <span data-ttu-id="0d06a-121">Ouvrez Microsoft Defender pour le point de terminaison pour Mac et accédez **à Gérer les paramètres.**</span><span class="sxs-lookup"><span data-stu-id="0d06a-121">Open Microsoft Defender for Endpoint for Mac and navigate to **Manage settings**.</span></span>

      ![Capture d’écran gérer la protection en temps réel](images/mdatp-36-rtp.png)

    - <span data-ttu-id="0d06a-123">À partir du terminal.</span><span class="sxs-lookup"><span data-stu-id="0d06a-123">From the Terminal.</span></span> <span data-ttu-id="0d06a-124">Pour des raisons de sécurité, cette opération nécessite une élévation.</span><span class="sxs-lookup"><span data-stu-id="0d06a-124">For security purposes, this operation requires elevation.</span></span>

      ```bash
      mdatp config real-time-protection --value disabled
      ```

      <span data-ttu-id="0d06a-125">Si votre appareil est géré par votre organisation, la protection en temps réel peut être désactivée par votre administrateur à l’aide des instructions dans Définir les préférences pour [Microsoft Defender pour Endpoint pour Mac.](mac-preferences.md)</span><span class="sxs-lookup"><span data-stu-id="0d06a-125">If your device is managed by your organization, real-time protection can be disabled by your administrator using the instructions in [Set preferences for Microsoft Defender for Endpoint for Mac](mac-preferences.md).</span></span>
      
      <span data-ttu-id="0d06a-126">Si le problème de performances persiste alors que la protection en temps réel est éteinte, l’origine du problème peut être le composant de détection et de réponse du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0d06a-126">If the performance problem persists while real-time protection is off, the origin of the problem could be the endpoint detection and response component.</span></span> <span data-ttu-id="0d06a-127">Dans ce cas, contactez le support technique pour obtenir des instructions supplémentaires et des mesures d’atténuation.</span><span class="sxs-lookup"><span data-stu-id="0d06a-127">In this case, please contact customer support for further instructions and mitigation.</span></span>

2. <span data-ttu-id="0d06a-128">Ouvrez Finder et accédez aux  >  **utilitaires d’applications.**</span><span class="sxs-lookup"><span data-stu-id="0d06a-128">Open Finder and navigate to **Applications** > **Utilities**.</span></span> <span data-ttu-id="0d06a-129">Ouvrez **l’Analyseur** d’activité et analysez les applications qui utilisent les ressources de votre système.</span><span class="sxs-lookup"><span data-stu-id="0d06a-129">Open **Activity Monitor** and analyze which applications are using the resources on your system.</span></span> <span data-ttu-id="0d06a-130">Les compilateurs et les outils de mise à jour logicielles sont des exemples classiques.</span><span class="sxs-lookup"><span data-stu-id="0d06a-130">Typical examples include software updaters and compilers.</span></span>

1. <span data-ttu-id="0d06a-131">Pour rechercher les applications qui déclenchent le plus d’analyses, vous pouvez utiliser les statistiques en temps réel recueillies par Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="0d06a-131">To find the applications that are triggering the most scans, you can use real-time statistics gathered by Defender for Endpoint for Mac.</span></span>

      > [!NOTE]
      > <span data-ttu-id="0d06a-132">Cette fonctionnalité est disponible dans la version 100.90.70 ou une version plus récente.</span><span class="sxs-lookup"><span data-stu-id="0d06a-132">This feature is available in version 100.90.70 or newer.</span></span>
      <span data-ttu-id="0d06a-133">Cette fonctionnalité est activée par défaut sur les canaux **Dog food** et **InsiderFast.**</span><span class="sxs-lookup"><span data-stu-id="0d06a-133">This feature is enabled by default on the **Dogfood** and **InsiderFast** channels.</span></span> <span data-ttu-id="0d06a-134">Si vous utilisez un autre canal de mise à jour, cette fonctionnalité peut être activée à partir de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="0d06a-134">If you're using a different update channel, this feature can be enabled from the command line:</span></span>
      ```bash
      mdatp config real-time-protection-statistics  --value enabled
      ```

      <span data-ttu-id="0d06a-135">Cette fonctionnalité nécessite une protection en temps réel pour être activée.</span><span class="sxs-lookup"><span data-stu-id="0d06a-135">This feature requires real-time protection to be enabled.</span></span> <span data-ttu-id="0d06a-136">Pour vérifier l’état de la protection en temps réel, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0d06a-136">To check the status of real-time protection, run the following command:</span></span>

      ```bash
      mdatp health --field real_time_protection_enabled
      ```

    <span data-ttu-id="0d06a-137">Vérifiez que **l’entrée real_time_protection_enabled** est vraie.</span><span class="sxs-lookup"><span data-stu-id="0d06a-137">Verify that the **real_time_protection_enabled** entry is true.</span></span> <span data-ttu-id="0d06a-138">Sinon, exécutez la commande suivante pour l’activer :</span><span class="sxs-lookup"><span data-stu-id="0d06a-138">Otherwise, run the following command to enable it:</span></span>

      ```bash
      mdatp config real-time-protection --value enabled
      ```

      ```output
      Configuration property updated
      ```

      <span data-ttu-id="0d06a-139">Pour collecter les statistiques actuelles, exécutez :</span><span class="sxs-lookup"><span data-stu-id="0d06a-139">To collect current statistics, run:</span></span>

      ```bash
      mdatp config real-time-protection --value enabled
      ```

      > [!NOTE]
      > <span data-ttu-id="0d06a-140">L’utilisation du json de sortie **(notez** le tiret double) garantit que le format de sortie est prêt pour l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="0d06a-140">Using **--output json** (note the double dash) ensures that the output format is ready for parsing.</span></span>
      <span data-ttu-id="0d06a-141">Le résultat de cette commande affiche tous les processus et l’activité d’analyse associée.</span><span class="sxs-lookup"><span data-stu-id="0d06a-141">The output of this command will show all processes and their associated scan activity.</span></span>

1. <span data-ttu-id="0d06a-142">Sur votre système Mac, téléchargez l’exemple d’analyseur Python high_cpu_parser.py à l’aide de la commande :</span><span class="sxs-lookup"><span data-stu-id="0d06a-142">On your Mac system, download the sample Python parser high_cpu_parser.py using the command:</span></span>

    ```bash
    wget -c https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/linux/diagnostic/high_cpu_parser.py
    ```

    <span data-ttu-id="0d06a-143">La sortie de cette commande doit être similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="0d06a-143">The output of this command should be similar to the following:</span></span>

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

1. <span data-ttu-id="0d06a-144">Ensuite, tapez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0d06a-144">Next, type the following commands:</span></span>

      ```bash
        chmod +x high_cpu_parser.py
      ```

      ```bash
        cat real_time_protection.json | python high_cpu_parser.py  > real_time_protection.log
      ```

      <span data-ttu-id="0d06a-145">La sortie de ce qui précède est une liste des principaux contributeurs aux problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="0d06a-145">The output of the above is a list of the top contributors to performance issues.</span></span> <span data-ttu-id="0d06a-146">La première colonne est l’identificateur de processus (PID), la deuxième colonne est le nom du processus te et la dernière colonne le nombre de fichiers analysés, triés par impact.</span><span class="sxs-lookup"><span data-stu-id="0d06a-146">The first column is the process identifier (PID), the second column is te process name, and the last column is the number of scanned files, sorted by impact.</span></span>

      <span data-ttu-id="0d06a-147">Par exemple, la sortie de la commande ressemblera à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="0d06a-147">For example, the output of the command will be something like the below:</span></span>

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

      <span data-ttu-id="0d06a-148">Pour améliorer les performances de Defender pour Point de terminaison pour Mac, recherchez celui qui a le plus grand nombre sous la ligne Nombre total de fichiers analysés et ajoutez une exclusion pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="0d06a-148">To improve the performance of Defender for Endpoint for Mac, locate the one with the highest number under the Total files scanned row and add an exclusion for it.</span></span> <span data-ttu-id="0d06a-149">Pour plus d’informations, voir [Configurer et valider des exclusions pour Defender pour Endpoint pour Linux.](linux-exclusions.md)</span><span class="sxs-lookup"><span data-stu-id="0d06a-149">For more information, see [Configure and validate exclusions for Defender for Endpoint for Linux](linux-exclusions.md).</span></span>

      > [!NOTE]
      > <span data-ttu-id="0d06a-150">L’application stocke les statistiques en mémoire et suit uniquement l’activité des fichiers depuis son début et que la protection en temps réel a été activée.</span><span class="sxs-lookup"><span data-stu-id="0d06a-150">The application stores statistics in memory and only keeps track of file activity since it was started and real-time protection was enabled.</span></span> <span data-ttu-id="0d06a-151">Les processus qui ont été lancés avant ou pendant les périodes où la protection en temps réel était hors programme ne sont pas comptabilisés.</span><span class="sxs-lookup"><span data-stu-id="0d06a-151">Processes that were launched before or during periods when real time protection was off are not counted.</span></span> <span data-ttu-id="0d06a-152">En outre, seuls les événements qui ont déclenché des analyses sont comptés.</span><span class="sxs-lookup"><span data-stu-id="0d06a-152">Additionally, only events which triggered scans are counted.</span></span>
      > 
1. <span data-ttu-id="0d06a-153">Configurez Microsoft Defender pour Endpoint pour Mac avec des exclusions pour les processus ou les emplacements de disque qui contribuent aux problèmes de performances et activez à nouveau la protection en temps réel.</span><span class="sxs-lookup"><span data-stu-id="0d06a-153">Configure Microsoft Defender for Endpoint for Mac with exclusions for the processes or disk locations that contribute to the performance issues and re-enable real-time protection.</span></span>

     <span data-ttu-id="0d06a-154">Pour [plus d’informations,](mac-exclusions.md) voir Configurer et valider des exclusions pour Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="0d06a-154">See [Configure and validate exclusions for Microsoft Defender for Endpoint for Mac](mac-exclusions.md) for details.</span></span>
