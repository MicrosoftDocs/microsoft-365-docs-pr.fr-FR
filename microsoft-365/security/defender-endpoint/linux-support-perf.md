---
title: Résoudre les problèmes de performances pour Microsoft Defender pour point de terminaison sur Linux
description: Résolution des problèmes de performances dans Microsoft Defender pour point de terminaison sur Linux.
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, linux, performances
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
mms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 998d8c500613ffa9fc6d790535e555ff9503f590
ms.sourcegitcommit: 8e4c107e4da3a00be0511b05bc655a98fe871a54
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52281016"
---
# <a name="troubleshoot-performance-issues-for-microsoft-defender-for-endpoint-on-linux"></a><span data-ttu-id="3858c-104">Résoudre les problèmes de performances pour Microsoft Defender pour point de terminaison sur Linux</span><span class="sxs-lookup"><span data-stu-id="3858c-104">Troubleshoot performance issues for Microsoft Defender for Endpoint on Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="3858c-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3858c-105">**Applies to:**</span></span>
- [<span data-ttu-id="3858c-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3858c-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="3858c-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3858c-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)
> <span data-ttu-id="3858c-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="3858c-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="3858c-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="3858c-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="3858c-110">Cet article fournit quelques étapes générales qui peuvent être utilisées pour affiner les problèmes de performances liés à Defender pour Endpoint sur Linux.</span><span class="sxs-lookup"><span data-stu-id="3858c-110">This article provides some general steps that can be used to narrow down performance issues related to Defender for Endpoint on Linux.</span></span>

<span data-ttu-id="3858c-111">La protection en temps réel (RTP) est une fonctionnalité de Defender for Endpoint sur Linux qui surveille et protège en permanence votre appareil contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="3858c-111">Real-time protection (RTP) is a feature of Defender for Endpoint on Linux that continuously monitors and protects your device against threats.</span></span> <span data-ttu-id="3858c-112">Il se compose de la surveillance des fichiers et des processus et d’autres heuristiques.</span><span class="sxs-lookup"><span data-stu-id="3858c-112">It consists of file and process monitoring and other heuristics.</span></span>

<span data-ttu-id="3858c-113">Selon les applications que vous exécutez et les caractéristiques de votre appareil, vous pouvez obtenir des performances sous-optimales lors de l’exécution de Defender pour Endpoint sur Linux.</span><span class="sxs-lookup"><span data-stu-id="3858c-113">Depending on the applications that you are running and your device characteristics, you may experience suboptimal performance when running Defender for Endpoint on Linux.</span></span> <span data-ttu-id="3858c-114">En particulier, les applications ou les processus système qui accèdent à de nombreuses ressources sur un court laps de temps peuvent entraîner des problèmes de performances dans Defender pour Endpoint sur Linux.</span><span class="sxs-lookup"><span data-stu-id="3858c-114">In particular, applications or system processes that access many resources over a short timespan can lead to performance issues in Defender for Endpoint on Linux.</span></span>

<span data-ttu-id="3858c-115">Avant de commencer, assurez-vous que les autres produits de sécurité ne sont pas en cours **d’exécution sur l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="3858c-115">Before starting, **please make sure that other security products are not currently running on the device**.</span></span> <span data-ttu-id="3858c-116">Plusieurs produits de sécurité peuvent être en conflit et avoir un impact sur les performances de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="3858c-116">Multiple security products may conflict and impact the host performance.</span></span>

<span data-ttu-id="3858c-117">Les étapes suivantes peuvent être utilisées pour résoudre et atténuer ces problèmes :</span><span class="sxs-lookup"><span data-stu-id="3858c-117">The following steps can be used to troubleshoot and mitigate these issues:</span></span>

1. <span data-ttu-id="3858c-118">Désactivez la protection en temps réel à l’aide de l’une des méthodes suivantes et observez si les performances sont améliorées.</span><span class="sxs-lookup"><span data-stu-id="3858c-118">Disable real-time protection using one of the following methods and observe whether the performance improves.</span></span> <span data-ttu-id="3858c-119">Cette approche permet de déterminer si Defender for Endpoint sur Linux contribue aux problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="3858c-119">This approach helps narrow down whether Defender for Endpoint on Linux is contributing to the performance issues.</span></span>

    <span data-ttu-id="3858c-120">Si votre appareil n’est pas géré par votre organisation, la protection en temps réel peut être désactivée à partir de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="3858c-120">If your device is not managed by your organization, real-time protection can be disabled from the command line:</span></span>

    ```bash
    mdatp config real-time-protection --value disabled
    ```
    ```Output
    Configuration property updated
    ```

    <span data-ttu-id="3858c-121">Si votre appareil est géré par votre organisation, la protection en temps réel peut être désactivée par votre administrateur à l’aide des instructions dans Définir les préférences pour [Defender pour Endpoint sur Linux.](linux-preferences.md)</span><span class="sxs-lookup"><span data-stu-id="3858c-121">If your device is managed by your organization, real-time protection can be disabled by your administrator using the instructions in [Set preferences for Defender for Endpoint on Linux](linux-preferences.md).</span></span>

    <span data-ttu-id="3858c-122">Si le problème de performances persiste alors que la protection en temps réel est éteinte, l’origine du problème peut être protection évolutive des points de terminaison composant.</span><span class="sxs-lookup"><span data-stu-id="3858c-122">If the performance problem persists while real-time protection is off, the origin of the problem could be the endpoint detection and response component.</span></span> <span data-ttu-id="3858c-123">Dans ce cas, contactez le support technique pour obtenir des instructions supplémentaires et des mesures de prévention.</span><span class="sxs-lookup"><span data-stu-id="3858c-123">In this case please contact customer support for further instructions and mitigation.</span></span>

2. <span data-ttu-id="3858c-124">Pour rechercher les applications qui déclenchent le plus d’analyses, vous pouvez utiliser des statistiques en temps réel recueillies par Defender pour Endpoint sur Linux.</span><span class="sxs-lookup"><span data-stu-id="3858c-124">To find the applications that are triggering the most scans, you can use real-time statistics gathered by Defender for Endpoint on Linux.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3858c-125">Cette fonctionnalité est disponible dans la version 100.90.70 ou une version plus récente.</span><span class="sxs-lookup"><span data-stu-id="3858c-125">This feature is available in version 100.90.70 or newer.</span></span>

    <span data-ttu-id="3858c-126">Cette fonctionnalité est activée par défaut sur les `Dogfood` canaux et les `InsiderFast` canaux.</span><span class="sxs-lookup"><span data-stu-id="3858c-126">This feature is enabled by default on the `Dogfood` and `InsiderFast` channels.</span></span> <span data-ttu-id="3858c-127">Si vous utilisez un autre canal de mise à jour, cette fonctionnalité peut être activée à partir de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="3858c-127">If you're using a different update channel, this feature can be enabled from the command line:</span></span>
    ```bash
    mdatp config real-time-protection-statistics --value enabled
    ```

    <span data-ttu-id="3858c-128">Cette fonctionnalité nécessite une protection en temps réel pour être activée.</span><span class="sxs-lookup"><span data-stu-id="3858c-128">This feature requires real-time protection to be enabled.</span></span> <span data-ttu-id="3858c-129">Pour vérifier l’état de la protection en temps réel, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3858c-129">To check the status of real-time protection, run the following command:</span></span>

    ```bash
    mdatp health --field real_time_protection_enabled
    ```

    <span data-ttu-id="3858c-130">Vérifiez que `real_time_protection_enabled` l’entrée est `true` .</span><span class="sxs-lookup"><span data-stu-id="3858c-130">Verify that the `real_time_protection_enabled` entry is `true`.</span></span> <span data-ttu-id="3858c-131">Sinon, exécutez la commande suivante pour l’activer :</span><span class="sxs-lookup"><span data-stu-id="3858c-131">Otherwise, run the following command to enable it:</span></span>

    ```bash
    mdatp config real-time-protection --value enabled
    ```
    ```Output
    Configuration property updated
    ```

    <span data-ttu-id="3858c-132">Pour collecter les statistiques actuelles, exécutez :</span><span class="sxs-lookup"><span data-stu-id="3858c-132">To collect current statistics, run:</span></span>

    ```bash
    mdatp diagnostic real-time-protection-statistics --output json > real_time_protection.json
    ```

    > [!NOTE]
    > <span data-ttu-id="3858c-133">L’utilisation (notez le tiret double) permet de s’assurer que le format de sortie ```--output json``` est prêt pour l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="3858c-133">Using ```--output json``` (note the double dash) ensures that the output format is ready for parsing.</span></span>

    <span data-ttu-id="3858c-134">Le résultat de cette commande affiche tous les processus et l’activité d’analyse associée.</span><span class="sxs-lookup"><span data-stu-id="3858c-134">The output of this command will show all processes and their associated scan activity.</span></span>

3. <span data-ttu-id="3858c-135">Sur votre système Linux, téléchargez l’exemple d’analyseur Python **high_cpu_parser.py** à l’aide de la commande :</span><span class="sxs-lookup"><span data-stu-id="3858c-135">On your Linux system, download the sample Python parser **high_cpu_parser.py** using the command:</span></span>

    ```bash
    wget -c https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/linux/diagnostic/high_cpu_parser.py
    ```
    <span data-ttu-id="3858c-136">La sortie de cette commande doit être similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="3858c-136">The output of this command should be similar to the following:</span></span>

    ```Output
    --2020-11-14 11:27:27-- https://raw.githubusercontent.com/microsoft.mdatp-xplat/master/linus/diagnostic/high_cpu_parser.py
    Resolving raw.githubusercontent.com (raw.githubusercontent.com)... 151.101.xxx.xxx
    Connecting to raw.githubusercontent.com (raw.githubusercontent.com)| 151.101.xxx.xxx| :443... connected.
    HTTP request sent, awaiting response... 200 OK
    Length: 1020 [text/plain]
    Saving to: 'high_cpu_parser.py'

    100%[===========================================>] 1,020    --.-K/s   in 0s
    ```

4. <span data-ttu-id="3858c-137">Ensuite, tapez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="3858c-137">Next, type the following commands:</span></span>

    ```bash
    chmod +x high_cpu_parser.py
    ```

    ```bash
    cat real_time_protection.json | python high_cpu_parser.py  > real_time_protection.log
    ```

      <span data-ttu-id="3858c-138">La sortie de ce qui précède est une liste des principaux contributeurs aux problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="3858c-138">The output of the above is a list of the top contributors to performance issues.</span></span> <span data-ttu-id="3858c-139">La première colonne est l’identificateur de processus (PID), la deuxième colonne est le nom du processus te et la dernière colonne le nombre de fichiers analysés, triés par impact.</span><span class="sxs-lookup"><span data-stu-id="3858c-139">The first column is the process identifier (PID), the second column is te process name, and the last column is the number of scanned files, sorted by impact.</span></span>
    <span data-ttu-id="3858c-140">Par exemple, la sortie de la commande ressemblera à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="3858c-140">For example, the output of the command will be something like the below:</span></span> 

    ```Output
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

    <span data-ttu-id="3858c-141">Pour améliorer les performances de Defender pour Endpoint sur Linux, recherchez celui qui a le plus grand nombre sous la ligne et ajoutez une `Total files scanned` exclusion pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="3858c-141">To improve the performance of Defender for Endpoint on Linux, locate the one with the highest number under the `Total files scanned` row and add an exclusion for it.</span></span> <span data-ttu-id="3858c-142">Pour plus d’informations, voir Configurer et valider des [exclusions pour Defender pour Endpoint sur Linux.](linux-exclusions.md)</span><span class="sxs-lookup"><span data-stu-id="3858c-142">For more information, see [Configure and validate exclusions for Defender for Endpoint on Linux](linux-exclusions.md).</span></span>

    >[!NOTE]
    > <span data-ttu-id="3858c-143">L’application stocke les statistiques en mémoire et suit uniquement l’activité des fichiers depuis son début et que la protection en temps réel a été activée.</span><span class="sxs-lookup"><span data-stu-id="3858c-143">The application stores statistics in memory and only keeps track of file activity since it was started and real-time protection was enabled.</span></span> <span data-ttu-id="3858c-144">Les processus qui ont été lancés avant ou pendant les périodes où la protection en temps réel était hors programme ne sont pas comptabilisés.</span><span class="sxs-lookup"><span data-stu-id="3858c-144">Processes that were launched before or during periods when real time protection was off are not counted.</span></span> <span data-ttu-id="3858c-145">En outre, seuls les événements qui ont déclenché des analyses sont comptés.</span><span class="sxs-lookup"><span data-stu-id="3858c-145">Additionally, only events which triggered scans are counted.</span></span>

5. <span data-ttu-id="3858c-146">Configurez Microsoft Defender pour endpoint sur Linux avec des exclusions pour les processus ou les emplacements de disque qui contribuent aux problèmes de performances et activez à nouveau la protection en temps réel.</span><span class="sxs-lookup"><span data-stu-id="3858c-146">Configure Microsoft Defender for Endpoint on Linux with exclusions for the processes or disk locations that contribute to the performance issues and re-enable real-time protection.</span></span>

    <span data-ttu-id="3858c-147">Pour plus d’informations, voir Configurer et valider des [exclusions pour Microsoft Defender pour Endpoint sur Linux.](linux-exclusions.md)</span><span class="sxs-lookup"><span data-stu-id="3858c-147">For more information, see [Configure and validate exclusions for Microsoft Defender for Endpoint on Linux](linux-exclusions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3858c-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3858c-148">See also</span></span>
- [<span data-ttu-id="3858c-149">Examiner les problèmes d’état de l’agent</span><span class="sxs-lookup"><span data-stu-id="3858c-149">Investigate agent health issues</span></span>](health-status.md)