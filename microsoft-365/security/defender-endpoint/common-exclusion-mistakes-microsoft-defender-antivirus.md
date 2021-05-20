---
title: Erreurs courantes à éviter lors de la définition d’exclusions
description: Évitez les erreurs courantes lors de la définition d’exclusions Antivirus Microsoft Defender analyses.
keywords: exclusions, fichiers, extension, type de fichier, nom de dossier, nom de fichier, analyses
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.topic: article
ms.date: 05/17/2021
ms.openlocfilehash: d10343538c995534878196cc57092c37fd2dcf7b
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52538062"
---
# <a name="common-mistakes-to-avoid-when-defining-exclusions"></a><span data-ttu-id="9f201-104">Erreurs courantes à éviter lors de la définition d’exclusions</span><span class="sxs-lookup"><span data-stu-id="9f201-104">Common mistakes to avoid when defining exclusions</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="9f201-105">Vous pouvez définir une liste d’exclusions pour les éléments que vous ne souhaitez Antivirus Microsoft Defender analyser.</span><span class="sxs-lookup"><span data-stu-id="9f201-105">You can define an exclusion list for items that you don't want Microsoft Defender Antivirus to scan.</span></span> <span data-ttu-id="9f201-106">Ces éléments exclus peuvent contenir des menaces qui rendent votre appareil vulnérable.</span><span class="sxs-lookup"><span data-stu-id="9f201-106">Such excluded items could contain threats that make your device vulnerable.</span></span> 

<span data-ttu-id="9f201-107">Cet article décrit une erreur courante que vous devez éviter lors de la définition d’exclusions.</span><span class="sxs-lookup"><span data-stu-id="9f201-107">This article describes some common mistake that you should avoid when defining exclusions.</span></span> 

<span data-ttu-id="9f201-108">Avant de définir vos listes d’exclusions, [voir Recommandations pour définir des exclusions.](configure-exclusions-microsoft-defender-antivirus.md#recommendations-for-defining-exclusions)</span><span class="sxs-lookup"><span data-stu-id="9f201-108">Before defining your exclusion lists, see [Recommendations for defining exclusions](configure-exclusions-microsoft-defender-antivirus.md#recommendations-for-defining-exclusions).</span></span>

## <a name="excluding-certain-trusted-items"></a><span data-ttu-id="9f201-109">Exclusion de certains éléments fiables</span><span class="sxs-lookup"><span data-stu-id="9f201-109">Excluding certain trusted items</span></span>

<span data-ttu-id="9f201-110">Certains fichiers, types de fichiers, dossiers ou processus ne doivent pas être exclus de l’analyse, même si vous les faites confiance pour ne pas être malveillants.</span><span class="sxs-lookup"><span data-stu-id="9f201-110">Certain files, file types, folders, or processes should not be excluded from scanning even though you trust them to be not malicious.</span></span> 

<span data-ttu-id="9f201-111">Ne définissez pas d’exclusions pour les emplacements de dossiers, les extensions de fichiers et les processus répertoriés dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="9f201-111">Do not define exclusions for the folder locations, file extensions, and processes that are listed in the following sections:</span></span>
- <span data-ttu-id="9f201-112">Emplacements des dossiers</span><span class="sxs-lookup"><span data-stu-id="9f201-112">Folder locations</span></span>
- <span data-ttu-id="9f201-113">Extensions de fichier</span><span class="sxs-lookup"><span data-stu-id="9f201-113">File extensions</span></span>
- <span data-ttu-id="9f201-114">Processus</span><span class="sxs-lookup"><span data-stu-id="9f201-114">Processes</span></span>

### <a name="folder-locations"></a><span data-ttu-id="9f201-115">Emplacements des dossiers</span><span class="sxs-lookup"><span data-stu-id="9f201-115">Folder locations</span></span>

<span data-ttu-id="9f201-116">En règle générale, ne définissez pas d’exclusions pour les emplacements de dossier suivants :</span><span class="sxs-lookup"><span data-stu-id="9f201-116">In general, do not define exclusions for the following folder locations:</span></span>

`%systemdrive%` 

`C:`

`C:\`

`C:\*`

`%ProgramFiles%\Java`

`C:\Program Files\Java` 

`%ProgramFiles%\Contoso\` 

`C:\Program Files\Contoso\` 

`%ProgramFiles(x86)%\Contoso\` 

`C:\Program Files (x86)\Contoso\`

`C:\Temp`

`C:\Temp\`

`C:\Temp\*`

`C:\Users\`

`C:\Users\*`

<span data-ttu-id="9f201-117">`C:\Users\<UserProfileName>\AppData\Local\Temp\`**Notez l’exception suivante SharePoint**: exclure lorsque vous utilisez la protection antivirus au niveau du `C:\Users\ServiceAccount\AppData\Local\Temp` fichier dans [SharePoint](https://support.microsoft.com/office/certain-folders-may-have-to-be-excluded-from-antivirus-scanning-when-you-use-file-level-antivirus-software-in-sharepoint-01cbc532-a24e-4bba-8d67-0b1ed733a3d9).</span><span class="sxs-lookup"><span data-stu-id="9f201-117">`C:\Users\<UserProfileName>\AppData\Local\Temp\` **Note the following exception for SharePoint**: Do exclude `C:\Users\ServiceAccount\AppData\Local\Temp` when you use [file-level antivirus protection in SharePoint](https://support.microsoft.com/office/certain-folders-may-have-to-be-excluded-from-antivirus-scanning-when-you-use-file-level-antivirus-software-in-sharepoint-01cbc532-a24e-4bba-8d67-0b1ed733a3d9).</span></span>

<span data-ttu-id="9f201-118">`C:\Users\<UserProfileName>\AppData\LocalLow\Temp\`**Notez l’exception suivante SharePoint**: exclure lorsque vous utilisez la protection antivirus au niveau du `C:\Users\Default\AppData\Local\Temp` fichier dans [SharePoint](https://support.microsoft.com/office/certain-folders-may-have-to-be-excluded-from-antivirus-scanning-when-you-use-file-level-antivirus-software-in-sharepoint-01cbc532-a24e-4bba-8d67-0b1ed733a3d9).</span><span class="sxs-lookup"><span data-stu-id="9f201-118">`C:\Users\<UserProfileName>\AppData\LocalLow\Temp\` **Note the following exception for SharePoint**: Do exclude `C:\Users\Default\AppData\Local\Temp` when you use [file-level antivirus protection in SharePoint](https://support.microsoft.com/office/certain-folders-may-have-to-be-excluded-from-antivirus-scanning-when-you-use-file-level-antivirus-software-in-sharepoint-01cbc532-a24e-4bba-8d67-0b1ed733a3d9).</span></span>

`%Windir%\Prefetch`

`C:\Windows\Prefetch`

`C:\Windows\Prefetch\`

`C:\Windows\Prefetch\*`

`%Windir%\System32\Spool`

`C:\Windows\System32\Spool`

`C:\Windows\System32\CatRoot2`
`%Windir%\Temp`

`C:\Windows\Temp`

`C:\Windows\Temp\`

`C:\Windows\Temp\*`

### <a name="file-extensions"></a><span data-ttu-id="9f201-119">Extensions de fichier</span><span class="sxs-lookup"><span data-stu-id="9f201-119">File extensions</span></span>

<span data-ttu-id="9f201-120">En règle générale, ne définissez pas d’exclusions pour les extensions de fichier suivantes :</span><span class="sxs-lookup"><span data-stu-id="9f201-120">In general, do not define exclusions for the following file extensions:</span></span>

`.7z`

`.bat`

`.bin`

`.cab`

`.cmd`

`.com` 

`.cpl`

`.dll`

`.exe`

`.fla`

`.gif`

`.gz`

`.hta`

`.inf`

`.java`

`.jar`

`.job`

`.jpeg`

`.jpg`

`.js`

`.ko`

`.ko.gz`

`.msi`

`.ocx`

`.png`

`.ps1`

`.py`

`.rar`

`.reg`

`.scr`

`.sys`

`.tar`

`.tmp`

`.url`

`.vbe`

`.vbs`

`.wsf`

`.zip`

### <a name="processes"></a><span data-ttu-id="9f201-121">Processus</span><span class="sxs-lookup"><span data-stu-id="9f201-121">Processes</span></span> 

<span data-ttu-id="9f201-122">En règle générale, ne définissez pas d’exclusions pour les processus suivants :</span><span class="sxs-lookup"><span data-stu-id="9f201-122">In general, do not define exclusions for the following processes:</span></span>

`AcroRd32.exe`  

`bitsadmin.exe`  

`excel.exe`  

`iexplore.exe`  

`java.exe`  

`outlook.exe`  

`psexec.exe`  

`powerpnt.exe`  

`powershell.exe`  

`schtasks.exe`

`svchost.exe` 

`wmic.exe`  

`winword.exe`  

`wuauclt.exe`  

`addinprocess.exe`  

`addinprocess32.exe`  

`addinutil.exe`  

`bash.exe`  

`bginfo.exe` 

`cdb.exe`  

`csi.exe`  

`dbghost.exe`  

`dbgsvc.exe`  

`dnx.exe`  

`fsi.exe`  

`fsiAnyCpu.exe`  

`kd.exe`  

`ntkd.exe`  

`lxssmanager.dll`  

`msbuild.exe` 

`mshta.exe`  

`ntsd.exe`  

`rcsi.exe`  

`system.management.automation.dll`  

`windbg.exe`

> [!NOTE]
> <span data-ttu-id="9f201-123">Vous pouvez choisir d’exclure des types de fichiers, tels que , ou si votre environnement dispose d’un logiciel moderne à jour avec une stratégie de mise à jour stricte pour gérer les `.gif` `.jpg` `.jpeg` `.png` vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="9f201-123">You can choose to exclude file types, such as `.gif`, `.jpg`, `.jpeg`, or `.png` if your environment has a modern, up-to-date software with a strict update policy to handle any vulnerabilities.</span></span>

## <a name="using-just-the-file-name-in-the-exclusion-list"></a><span data-ttu-id="9f201-124">Utilisation du nom de fichier dans la liste d’exclusions</span><span class="sxs-lookup"><span data-stu-id="9f201-124">Using just the file name in the exclusion list</span></span>

<span data-ttu-id="9f201-125">Un programme malveillant peut avoir le même nom que celui du fichier que vous faites confiance et que vous souhaitez exclure de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="9f201-125">A malware may have the same name as that of the file that you trust and want to exclude from scanning.</span></span> <span data-ttu-id="9f201-126">Par conséquent, pour éviter d’exclure un programme malveillant potentiel de l’analyse, utilisez un chemin d’accès complet au fichier que vous souhaitez exclure au lieu d’utiliser uniquement le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="9f201-126">Therefore, to avoid excluding a potential malware from scanning, use a fully qualified path to the file that you want to exclude instead of using just the file name.</span></span> <span data-ttu-id="9f201-127">Par exemple, si vous souhaitez exclure de l’analyse, utilisez le chemin d’accès complet `Filename.exe` au fichier, tel que `C:\program files\contoso\Filename.exe` .</span><span class="sxs-lookup"><span data-stu-id="9f201-127">For example, if you want to exclude `Filename.exe` from scanning, use the complete path to the file, such as `C:\program files\contoso\Filename.exe`.</span></span>

## <a name="using-a-single-exclusion-list-for-multiple-server-workloads"></a><span data-ttu-id="9f201-128">Utilisation d’une seule liste d’exclusions pour plusieurs charges de travail serveur</span><span class="sxs-lookup"><span data-stu-id="9f201-128">Using a single exclusion list for multiple server workloads</span></span>

<span data-ttu-id="9f201-129">N’utilisez pas une seule liste d’exclusions pour définir des exclusions pour plusieurs charges de travail de serveur.</span><span class="sxs-lookup"><span data-stu-id="9f201-129">Do not use a single exclusion list to define exclusions for multiple server workloads.</span></span> <span data-ttu-id="9f201-130">Fractionner les exclusions pour différentes charges de travail d’application ou de service en plusieurs listes d’exclusions.</span><span class="sxs-lookup"><span data-stu-id="9f201-130">Split the exclusions for different application or service workloads into multiple exclusion lists.</span></span> <span data-ttu-id="9f201-131">Par exemple, la liste d’exclusions de votre charge de travail de serveur IIS doit être différente de la liste d’exclusions pour SQL Server charge de travail.</span><span class="sxs-lookup"><span data-stu-id="9f201-131">For example, the exclusion list for your IIS Server workload must be different from the exclusion list for your SQL Server workload.</span></span>

## <a name="using-incorrect-environment-variables-as-wildcards-in-the-file-name-and-folder-path-or-extension-exclusion-lists"></a><span data-ttu-id="9f201-132">Utilisation de variables d’environnement incorrectes comme caractères génériques dans les listes d’exclusions de nom de fichier et de chemin d’accès au dossier ou d’extension</span><span class="sxs-lookup"><span data-stu-id="9f201-132">Using incorrect environment variables as wildcards in the file name and folder path or extension exclusion lists</span></span>

<span data-ttu-id="9f201-133">Antivirus Microsoft Defender Le service s’exécute dans le contexte système à l’aide du compte LocalSystem, ce qui signifie qu’il obtient des informations à partir de la variable d’environnement système, et non de la variable d’environnement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9f201-133">Microsoft Defender Antivirus Service runs in system context using the LocalSystem account, which means it gets information from the system environment variable, and not from the user environment variable.</span></span> <span data-ttu-id="9f201-134">L’utilisation de variables d’environnement comme caractère générique dans les listes d’exclusions est limitée aux variables système et à celles applicables aux processus en cours d’exécution en tant que compte NT AUTHORITY\SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="9f201-134">Use of environment variables as a wildcard in exclusion lists is limited to system variables and those applicable to processes running as an NT AUTHORITY\SYSTEM account.</span></span> <span data-ttu-id="9f201-135">Par conséquent, n’utilisez pas de variables d’environnement utilisateur comme caractères génériques lors de l Antivirus Microsoft Defender exclusions de dossiers et de processus.</span><span class="sxs-lookup"><span data-stu-id="9f201-135">Therefore, do not use user environment variables as wildcards when adding Microsoft Defender Antivirus folder and process exclusions.</span></span> <span data-ttu-id="9f201-136">Consultez le tableau sous [Variables d’environnement système](configure-extension-file-exclusions-microsoft-defender-antivirus.md#system-environment-variables) pour obtenir la liste complète des variables d’environnement système.</span><span class="sxs-lookup"><span data-stu-id="9f201-136">See the table under [System environment variables](configure-extension-file-exclusions-microsoft-defender-antivirus.md#system-environment-variables) for a complete list of system environment variables.</span></span>

<span data-ttu-id="9f201-137">Pour plus d’informations sur l’utilisation des caractères génériques dans les listes d’exclusions, voir Utiliser des [caractères génériques](configure-extension-file-exclusions-microsoft-defender-antivirus.md#use-wildcards-in-the-file-name-and-folder-path-or-extension-exclusion-lists) dans les listes d’exclusions et le chemin d’accès au dossier ou les listes d’exclusions.</span><span class="sxs-lookup"><span data-stu-id="9f201-137">See [Use wildcards in the file name and folder path or extension exclusion lists](configure-extension-file-exclusions-microsoft-defender-antivirus.md#use-wildcards-in-the-file-name-and-folder-path-or-extension-exclusion-lists) for information on how to use wildcards in exclusion lists.</span></span>

## <a name="related-articles"></a><span data-ttu-id="9f201-138">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="9f201-138">Related articles</span></span>

- [<span data-ttu-id="9f201-139">Configurer et valider des exclusions dans Antivirus Microsoft Defender analyses</span><span class="sxs-lookup"><span data-stu-id="9f201-139">Configure and validate exclusions in Microsoft Defender Antivirus scans</span></span>](configure-exclusions-microsoft-defender-antivirus.md)
- [<span data-ttu-id="9f201-140">Configurer et valider des exclusions en fonction de l’extension de fichier et de l’emplacement du dossier</span><span class="sxs-lookup"><span data-stu-id="9f201-140">Configure and validate exclusions based on file extension and folder location</span></span>](configure-extension-file-exclusions-microsoft-defender-antivirus.md)
- [<span data-ttu-id="9f201-141">Configurer et valider des exclusions pour les fichiers ouverts par des processus</span><span class="sxs-lookup"><span data-stu-id="9f201-141">Configure and validate exclusions for files opened by processes</span></span>](configure-process-opened-file-exclusions-microsoft-defender-antivirus.md)
- [<span data-ttu-id="9f201-142">Configurer des exclusions Antivirus Microsoft Defender sur Windows Server</span><span class="sxs-lookup"><span data-stu-id="9f201-142">Configure Microsoft Defender Antivirus exclusions on Windows Server</span></span>](configure-server-exclusions-microsoft-defender-antivirus.md)
