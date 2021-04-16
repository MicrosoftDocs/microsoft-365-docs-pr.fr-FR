---
title: Comment planifier des analyses avec MDATP pour macOS
description: Découvrez comment planifier un temps d'analyse automatique pour Microsoft Defender for Endpoint dans macOS afin de mieux protéger les ressources de votre organisation.
keywords: microsoft, defender, atp, mac, analyses, antivirus
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
ms.openlocfilehash: 71576c777f58aa193f2a73db7edea832d29a97c6
ms.sourcegitcommit: 22505ce322f68a2d0ce70d71caf3b0a657fa838a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2021
ms.locfileid: "51860930"
---
# <a name="schedule-scans-with-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="9c074-104">Planifier des analyses avec Microsoft Defender pour endpoint sur macOS</span><span class="sxs-lookup"><span data-stu-id="9c074-104">Schedule scans with Microsoft Defender for Endpoint on macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="9c074-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9c074-105">**Applies to:**</span></span>
- [<span data-ttu-id="9c074-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9c074-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="9c074-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9c074-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="9c074-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="9c074-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="9c074-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="9c074-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="9c074-110">Bien que vous pouvez démarrer une analyse des menaces à tout moment avec Microsoft Defender pour le point de terminaison, votre entreprise peut bénéficier d'analyses programmées ou programmées.</span><span class="sxs-lookup"><span data-stu-id="9c074-110">While you can start a threat scan at any time with Microsoft Defender for Endpoint, your enterprise might benefit from scheduled or timed scans.</span></span> <span data-ttu-id="9c074-111">Par exemple, vous pouvez planifier une analyse à exécuter au début de chaque jour ou semaine de travail.</span><span class="sxs-lookup"><span data-stu-id="9c074-111">For example, you can schedule a scan to run at the beginning of every workday or week.</span></span> 

## <a name="schedule-a-scan-with-launchd"></a><span data-ttu-id="9c074-112">Planifier une analyse avec *lancement*</span><span class="sxs-lookup"><span data-stu-id="9c074-112">Schedule a scan with *launchd*</span></span>

<span data-ttu-id="9c074-113">Vous pouvez créer une planification d'analyse à l'aide du *daemon* lancé sur un appareil macOS.</span><span class="sxs-lookup"><span data-stu-id="9c074-113">You can create a scanning schedule using the *launchd* daemon on a macOS device.</span></span>

1. <span data-ttu-id="9c074-114">Le code suivant montre le schéma que vous devez utiliser pour planifier une analyse.</span><span class="sxs-lookup"><span data-stu-id="9c074-114">The following code shows the schema you need to use to schedule a scan.</span></span> <span data-ttu-id="9c074-115">Ouvrez un éditeur de texte et utilisez cet exemple comme guide pour votre propre fichier d'analyse programmé.</span><span class="sxs-lookup"><span data-stu-id="9c074-115">Open a text editor and use this example as a guide for your own scheduled scan file.</span></span>

    <span data-ttu-id="9c074-116">Pour plus d'informations sur le format [](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) de fichier *.plist* utilisé ici, voir à propos des fichiers de liste de propriétés d'informations sur le site web officiel du développeur Apple.</span><span class="sxs-lookup"><span data-stu-id="9c074-116">For more information on the *.plist* file format used here, see [About Information Property List Files](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) at the official Apple developer website.</span></span>

    ```XML
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN"
      "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
    <plist version="1.0">
    <dict>
        <key>Label</key>
        <string>com.microsoft.wdav.schedquickscan</string>
        <key>ProgramArguments</key>
        <array>
            <string>sh</string>
            <string>-c</string>
            <string>/usr/local/bin/mdatp scan quick</string>
        </array>
        <key>RunAtLoad</key>
        <true/>
        <key>StartCalendarInterval</key>
        <dict>
            <key>Day</key>
            <integer>3</integer>
            <key>Hour</key>
            <integer>2</integer>
            <key>Minute</key>
            <integer>0</integer>
            <key>Weekday</key>
            <integer>5</integer>
        </dict>
        <key>WorkingDirectory</key>
        <string>/usr/local/bin/</string>
    </dict>
    </plist>
     ```

2. <span data-ttu-id="9c074-117">Enregistrez le fichier *sous com.microsoft.wdav.schedquickscan.plist*.</span><span class="sxs-lookup"><span data-stu-id="9c074-117">Save the file as *com.microsoft.wdav.schedquickscan.plist*.</span></span>

    > [!TIP]
    > <span data-ttu-id="9c074-118">Pour exécuter une analyse complète au lieu d'une analyse rapide, modifiez la ligne 12, pour utiliser l'option au lieu (c'est-à-dire) et enregistrez le fichier sous le nom `<string>/usr/local/bin/mdatp scan quick</string>` `full` `quick` `<string>/usr/local/bin/mdatp scan full</string>` *com.microsoft.wdav.sched **full** scan.plist* au lieu de *com.microsoft.wdav.sched **quick** scan.plist*.</span><span class="sxs-lookup"><span data-stu-id="9c074-118">To run a full scan instead of a quick scan, change line 12, `<string>/usr/local/bin/mdatp scan quick</string>`, to use the `full` option instead of `quick` (i.e. `<string>/usr/local/bin/mdatp scan full</string>`) and save the file as *com.microsoft.wdav.sched **full** scan.plist* instead of *com.microsoft.wdav.sched **quick** scan.plist*.</span></span>

3. <span data-ttu-id="9c074-119">Ouvrez **Terminal**.</span><span class="sxs-lookup"><span data-stu-id="9c074-119">Open **Terminal**.</span></span>
4. <span data-ttu-id="9c074-120">Entrez les commandes suivantes pour charger votre fichier :</span><span class="sxs-lookup"><span data-stu-id="9c074-120">Enter the following commands to load your file:</span></span>

    ```bash
    launchctl load /Library/LaunchDaemons/<your file name.plist>
    launchctl start <your file name>
    ```

5. <span data-ttu-id="9c074-121">Votre analyse programmée s'exécutera à la date, à l'heure et à la fréquence que vous avez définies dans votre liste P.</span><span class="sxs-lookup"><span data-stu-id="9c074-121">Your scheduled scan will run at the date, time, and frequency you defined in your p-list.</span></span> <span data-ttu-id="9c074-122">Dans l'exemple, l'analyse s'exécute à 02:00 tous les vendredis.</span><span class="sxs-lookup"><span data-stu-id="9c074-122">In the example, the scan runs at 2:00 AM every Friday.</span></span> 

    <span data-ttu-id="9c074-123">La `Weekday` valeur `StartCalendarInterval` d'utilise un nombre integer pour indiquer le cinquième jour de la semaine ou le vendredi.</span><span class="sxs-lookup"><span data-stu-id="9c074-123">The `Weekday` value of `StartCalendarInterval` uses an integer to indicate the fifth day of the week, or Friday.</span></span>

 > [!IMPORTANT]
 > <span data-ttu-id="9c074-124">Les agents exécutés *avec lancement* ne s'exécutent pas à l'heure prévue pendant que l'appareil est en veille.</span><span class="sxs-lookup"><span data-stu-id="9c074-124">Agents executed with *launchd* will not run at the scheduled time while the device is asleep.</span></span> <span data-ttu-id="9c074-125">Ils s'exécutent à la place une fois que l'appareil reprend en mode veille.</span><span class="sxs-lookup"><span data-stu-id="9c074-125">They will instead run once the device resumes from sleep mode.</span></span>
 >
 > <span data-ttu-id="9c074-126">Si l'appareil est désactivé, l'analyse s'exécutera à la prochaine heure d'analyse programmée.</span><span class="sxs-lookup"><span data-stu-id="9c074-126">If the device is turned off, the scan will run at the next scheduled scan time.</span></span>

## <a name="schedule-a-scan-with-intune"></a><span data-ttu-id="9c074-127">Planifier une analyse avec Intune</span><span class="sxs-lookup"><span data-stu-id="9c074-127">Schedule a scan with Intune</span></span>

<span data-ttu-id="9c074-128">Vous pouvez également planifier des analyses avec Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="9c074-128">You can also schedule scans with Microsoft Intune.</span></span> <span data-ttu-id="9c074-129">Le [script runMDATPQuickScan.sh](https://github.com/microsoft/shell-intune-samples/tree/master/Misc/MDATP#runmdatpquickscansh) shell disponible dans [scripts pour Microsoft Defender pour le](https://github.com/microsoft/shell-intune-samples/tree/master/Misc/MDATP) point de terminaison est persistant lorsque l'appareil reprend du mode veille.</span><span class="sxs-lookup"><span data-stu-id="9c074-129">The [runMDATPQuickScan.sh](https://github.com/microsoft/shell-intune-samples/tree/master/Misc/MDATP#runmdatpquickscansh) shell script available at [Scripts for Microsoft Defender for Endpoint](https://github.com/microsoft/shell-intune-samples/tree/master/Misc/MDATP) will persist when the device resumes from sleep mode.</span></span> 

<span data-ttu-id="9c074-130">Voir Utiliser des scripts shell sur les appareils macOS dans [Intune](https://docs.microsoft.com/mem/intune/apps/macos-shell-scripts) pour obtenir des instructions plus détaillées sur l'utilisation de ce script dans votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="9c074-130">See [Use shell scripts on macOS devices in Intune](https://docs.microsoft.com/mem/intune/apps/macos-shell-scripts) for more detailed instructions on how to use this script in your enterprise.</span></span>
