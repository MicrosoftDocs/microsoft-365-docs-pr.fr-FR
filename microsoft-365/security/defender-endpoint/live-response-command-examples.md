---
title: Exemples de commande Live response
description: Apprenez à exécuter des commandes de réponse en direct de base ou avancées pour Microsoft Defender pour endpoint et consultez des exemples sur son utilisation.
keywords: exemple, commande, cli, distant, shell, connexion, live, response, real-time, command, script, remediate, hunt, export, log, drop, download, file
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 389d9ad4a3e5fc876e7bded89389202e95bfda45
ms.sourcegitcommit: 337e8d8a2fee112d799edd8a0e04b3a2f124f900
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "52879119"
---
# <a name="live-response-command-examples"></a><span data-ttu-id="58b93-104">Exemples de commande Live response</span><span class="sxs-lookup"><span data-stu-id="58b93-104">Live response command examples</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="58b93-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="58b93-105">**Applies to:**</span></span>
- [<span data-ttu-id="58b93-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="58b93-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="58b93-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="58b93-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="58b93-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="58b93-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="58b93-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="58b93-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="58b93-110">Découvrez les commandes courantes utilisées dans la réponse en direct et consultez des exemples sur la façon dont elles sont généralement utilisées.</span><span class="sxs-lookup"><span data-stu-id="58b93-110">Learn about common commands used in live response and see examples on how they are typically used.</span></span>

<span data-ttu-id="58b93-111">Selon le rôle qui vous a été accordé, vous pouvez exécuter des commandes de réponse en direct de base ou avancées.</span><span class="sxs-lookup"><span data-stu-id="58b93-111">Depending on the role that's been granted to you, you can run basic or advanced live response commands.</span></span> <span data-ttu-id="58b93-112">Pour plus d’informations sur les commandes de base et avancées, voir [Examiner les entités sur les appareils à l’aide de la réponse en direct.](live-response.md)</span><span class="sxs-lookup"><span data-stu-id="58b93-112">For more information on basic and advanced commands, see [Investigate entities on devices using live response](live-response.md).</span></span>


## <a name="analyze"></a><span data-ttu-id="58b93-113">analyser</span><span class="sxs-lookup"><span data-stu-id="58b93-113">analyze</span></span> 

```console
# Analyze the file malware.txt
analyze file c:\Users\user\Desktop\malware.txt
```

```console
# Analyze the process by PID
analyze process 1234
```

## <a name="connections"></a><span data-ttu-id="58b93-114">connexions</span><span class="sxs-lookup"><span data-stu-id="58b93-114">connections</span></span>

```console
# List active connections in json format using parameter name
connections -output json
```

```console
# List active connections in json format without parameter name
connections json
```

## <a name="dir"></a><span data-ttu-id="58b93-115">dir</span><span class="sxs-lookup"><span data-stu-id="58b93-115">dir</span></span>

```console
# List files and sub-folders in the current folder
dir
```

```console
# List files and sub-folders in a specific folder
dir C:\Users\user\Desktop\
```

```console
# List files and subfolders in the current folder in json format
dir -output json
```

## <a name="fileinfo"></a><span data-ttu-id="58b93-116">fileinfo</span><span class="sxs-lookup"><span data-stu-id="58b93-116">fileinfo</span></span>

```console
# Display information about a file
fileinfo C:\Windows\notepad.exe
```

## <a name="findfile"></a><span data-ttu-id="58b93-117">findfile</span><span class="sxs-lookup"><span data-stu-id="58b93-117">findfile</span></span>

```console
# Find file by name
findfile test.txt
```

## <a name="getfile"></a><span data-ttu-id="58b93-118">getfile</span><span class="sxs-lookup"><span data-stu-id="58b93-118">getfile</span></span>

```console
# Download a file from a machine
getfile c:\Users\user\Desktop\work.txt
```

```console
# Download a file from a machine, automatically run prerequisite commands
getfile c:\Users\user\Desktop\work.txt -auto
```

>[!NOTE]
>
> <span data-ttu-id="58b93-119">Les types de fichiers **suivants ne peuvent** pas être téléchargés à l’aide de cette commande à partir de Live Response :</span><span class="sxs-lookup"><span data-stu-id="58b93-119">The following file types **cannot** be downloaded using this command from within Live Response:</span></span>
>
> * [<span data-ttu-id="58b93-120">Reparse point files</span><span class="sxs-lookup"><span data-stu-id="58b93-120">Reparse point files</span></span>](/windows/desktop/fileio/reparse-points/)
> * [<span data-ttu-id="58b93-121">Fichiers dispersés</span><span class="sxs-lookup"><span data-stu-id="58b93-121">Sparse files</span></span>](/windows/desktop/fileio/sparse-files/)
> * <span data-ttu-id="58b93-122">Fichiers vides</span><span class="sxs-lookup"><span data-stu-id="58b93-122">Empty files</span></span>
> * <span data-ttu-id="58b93-123">Fichiers virtuels ou fichiers qui ne sont pas entièrement présents localement</span><span class="sxs-lookup"><span data-stu-id="58b93-123">Virtual files, or files that are not fully present locally</span></span>
>
> <span data-ttu-id="58b93-124">Ces types de **fichiers sont pris** en charge par [PowerShell.](/powershell/scripting/overview?view=powershell-6/?&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="58b93-124">These file types **are** supported by [PowerShell](/powershell/scripting/overview?view=powershell-6/?&preserve-view=true).</span></span>
>
> <span data-ttu-id="58b93-125">Utilisez PowerShell comme alternative si vous avez des problèmes à l’aide de cette commande à partir de Live Response.</span><span class="sxs-lookup"><span data-stu-id="58b93-125">Use PowerShell as an alternative, if you have problems using this command from within Live Response.</span></span>

## <a name="processes"></a><span data-ttu-id="58b93-126">Processus</span><span class="sxs-lookup"><span data-stu-id="58b93-126">processes</span></span>
```console
# Show all processes
processes
```

```console
# Get process by pid
processes 123
```

```console
# Get process by pid with argument name
processes -pid 123
```

```console
# Get process by name
processes -name notepad.exe
```

## <a name="putfile"></a><span data-ttu-id="58b93-127">putfile</span><span class="sxs-lookup"><span data-stu-id="58b93-127">putfile</span></span>

```console
# Upload file from library
putfile get-process-by-name.ps1
```

```console
# Upload file from library, overwrite file if it exists
putfile get-process-by-name.ps1 -overwrite
```

```console
# Upload file from library, keep it on the machine after a restart
putfile get-process-by-name.ps1 -keep
```

## <a name="registry"></a><span data-ttu-id="58b93-128">registre</span><span class="sxs-lookup"><span data-stu-id="58b93-128">registry</span></span>

```console
# Show information about the values in a registry key
registry HKEY_CURRENT_USER\Console
```

```console
# Show information about a specific registry value
registry HKEY_CURRENT_USER\Console\\ScreenBufferSize
```


## <a name="remediate"></a><span data-ttu-id="58b93-129">corriger</span><span class="sxs-lookup"><span data-stu-id="58b93-129">remediate</span></span>

```console
# Remediate file in specific path
remediate file c:\Users\user\Desktop\malware.exe
```

```console
# Remediate process with specific PID
remediate process 7960
```

```console
# See list of all remediated entities
remediate list
```

## <a name="run"></a><span data-ttu-id="58b93-130">run</span><span class="sxs-lookup"><span data-stu-id="58b93-130">run</span></span>

```console
# Run PowerShell script from the library without arguments
run script.ps1
```

```console
# Run PowerShell script from the library with arguments
run get-process-by-name.ps1 -parameters "-processName Registry"
```
>[!NOTE]
>
> <span data-ttu-id="58b93-131">Pour les commandes de longue durée telles que «**exécuter**» ou «**getfile**» , vous pouvez utiliser le symbole ' ' à la fin de la commande pour effectuer cette action en arrière-plan. **&**</span><span class="sxs-lookup"><span data-stu-id="58b93-131">For long running commands such as '**run**' or '**getfile**', you may want to use the '**&**' symbol at the end of the command to perform that action in the background.</span></span>
> <span data-ttu-id="58b93-132">Cela vous permettra de continuer à examiner l’ordinateur et de revenir à la commande en arrière-plan lorsque vous avez terminé à l’aide de la commande de base «**fg** [».](live-response.md#basic-commands)</span><span class="sxs-lookup"><span data-stu-id="58b93-132">This will allow you to continue investigating the machine and return to the background command when done using '**fg**' [basic command](live-response.md#basic-commands).</span></span>
>
## <a name="scheduledtask"></a><span data-ttu-id="58b93-133">scheduledtask</span><span class="sxs-lookup"><span data-stu-id="58b93-133">scheduledtask</span></span>

```console
# Get all scheduled tasks
scheduledtasks
```

```console
# Get specific scheduled task by location and name
scheduledtasks Microsoft\Windows\Subscription\LicenseAcquisition
```

```console
# Get specific scheduled task by location and name with spacing
scheduledtasks "Microsoft\Configuration Manager\Configuration Manager Health Evaluation"
```


## <a name="undo"></a><span data-ttu-id="58b93-134">undo</span><span class="sxs-lookup"><span data-stu-id="58b93-134">undo</span></span>

```console
# Restore remediated registry
undo registry HKEY_CURRENT_USER\Console\ScreenBufferSize
```

```console
# Restore remediated scheduledtask
undo scheduledtask Microsoft\Windows\Subscription\LicenseAcquisition
```

```console
# Restore remediated file
undo file c:\Users\user\Desktop\malware.exe
```


## <a name="library"></a><span data-ttu-id="58b93-135">library</span><span class="sxs-lookup"><span data-stu-id="58b93-135">library</span></span>

```console
# List files in the library
library
```

```console
# Delete a file from the library
library delete script.ps1
```
