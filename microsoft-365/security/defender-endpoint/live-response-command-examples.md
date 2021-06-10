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
ms.openlocfilehash: f08f20753a1f0926abbbce01fe97f20ef1c07f2c
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51689088"
---
# <a name="live-response-command-examples"></a><span data-ttu-id="74594-104">Exemples de commande Live response</span><span class="sxs-lookup"><span data-stu-id="74594-104">Live response command examples</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="74594-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="74594-105">**Applies to:**</span></span>
- [<span data-ttu-id="74594-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="74594-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="74594-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="74594-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="74594-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="74594-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="74594-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="74594-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="74594-110">Découvrez les commandes courantes utilisées dans la réponse en direct et consultez des exemples sur la façon dont elles sont généralement utilisées.</span><span class="sxs-lookup"><span data-stu-id="74594-110">Learn about common commands used in live response and see examples on how they are typically used.</span></span>

<span data-ttu-id="74594-111">Selon le rôle qui vous a été accordé, vous pouvez exécuter des commandes de réponse en direct de base ou avancées.</span><span class="sxs-lookup"><span data-stu-id="74594-111">Depending on the role that's been granted to you, you can run basic or advanced live response commands.</span></span> <span data-ttu-id="74594-112">Pour plus d’informations sur les commandes de base et avancées, voir [Examiner les entités sur les appareils à l’aide de la réponse en direct.](live-response.md)</span><span class="sxs-lookup"><span data-stu-id="74594-112">For more information on basic and advanced commands, see [Investigate entities on devices using live response](live-response.md).</span></span>


## <a name="analyze"></a><span data-ttu-id="74594-113">analyser</span><span class="sxs-lookup"><span data-stu-id="74594-113">analyze</span></span> 

```
# Analyze the file malware.txt
analyze file c:\Users\user\Desktop\malware.txt
```

```
# Analyze the process by PID
analyze process 1234
```

## <a name="connections"></a><span data-ttu-id="74594-114">connexions</span><span class="sxs-lookup"><span data-stu-id="74594-114">connections</span></span>

```
# List active connections in json format using parameter name
connections -output json
```

```
# List active connections in json format without parameter name
connections json
```

## <a name="dir"></a><span data-ttu-id="74594-115">dir</span><span class="sxs-lookup"><span data-stu-id="74594-115">dir</span></span>

```
# List files and sub-folders in the current folder
dir
```

```
# List files and sub-folders in a specific folder
dir C:\Users\user\Desktop\
```

```
# List files and subfolders in the current folder in json format
dir -output json
```

## <a name="fileinfo"></a><span data-ttu-id="74594-116">fileinfo</span><span class="sxs-lookup"><span data-stu-id="74594-116">fileinfo</span></span>

```
# Display information about a file
fileinfo C:\Windows\notepad.exe
```

## <a name="findfile"></a><span data-ttu-id="74594-117">findfile</span><span class="sxs-lookup"><span data-stu-id="74594-117">findfile</span></span>

```
# Find file by name
findfile test.txt
```

## <a name="getfile"></a><span data-ttu-id="74594-118">getfile</span><span class="sxs-lookup"><span data-stu-id="74594-118">getfile</span></span>

```
# Download a file from a machine
getfile c:\Users\user\Desktop\work.txt
```

```
# Download a file from a machine, automatically run prerequisite commands
getfile c:\Users\user\Desktop\work.txt -auto
```

>[!NOTE]
>
> <span data-ttu-id="74594-119">Les types de fichiers **suivants ne peuvent** pas être téléchargés à l’aide de cette commande à partir de Live Response :</span><span class="sxs-lookup"><span data-stu-id="74594-119">The following file types **cannot** be downloaded using this command from within Live Response:</span></span>
>
> * [<span data-ttu-id="74594-120">Reparse point files</span><span class="sxs-lookup"><span data-stu-id="74594-120">Reparse point files</span></span>](/windows/desktop/fileio/reparse-points/)
> * [<span data-ttu-id="74594-121">Fichiers dispersés</span><span class="sxs-lookup"><span data-stu-id="74594-121">Sparse files</span></span>](/windows/desktop/fileio/sparse-files/)
> * <span data-ttu-id="74594-122">Fichiers vides</span><span class="sxs-lookup"><span data-stu-id="74594-122">Empty files</span></span>
> * <span data-ttu-id="74594-123">Fichiers virtuels ou fichiers qui ne sont pas entièrement présents localement</span><span class="sxs-lookup"><span data-stu-id="74594-123">Virtual files, or files that are not fully present locally</span></span>
>
> <span data-ttu-id="74594-124">Ces types de **fichiers sont pris** en charge par [PowerShell.](/powershell/scripting/overview?view=powershell-6/?&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="74594-124">These file types **are** supported by [PowerShell](/powershell/scripting/overview?view=powershell-6/?&preserve-view=true).</span></span>
>
> <span data-ttu-id="74594-125">Utilisez PowerShell comme alternative si vous avez des problèmes à l’aide de cette commande à partir de Live Response.</span><span class="sxs-lookup"><span data-stu-id="74594-125">Use PowerShell as an alternative, if you have problems using this command from within Live Response.</span></span>

## <a name="processes"></a><span data-ttu-id="74594-126">Processus</span><span class="sxs-lookup"><span data-stu-id="74594-126">processes</span></span>
```
# Show all processes
processes
```

```
# Get process by pid
processes 123
```

```
# Get process by pid with argument name
processes -pid 123
```

```
# Get process by name
processes -name notepad.exe
```

## <a name="putfile"></a><span data-ttu-id="74594-127">putfile</span><span class="sxs-lookup"><span data-stu-id="74594-127">putfile</span></span>

```
# Upload file from library
putfile get-process-by-name.ps1
```

```
# Upload file from library, overwrite file if it exists
putfile get-process-by-name.ps1 -overwrite
```

```
# Upload file from library, keep it on the machine after a restart
putfile get-process-by-name.ps1 -keep
```

## <a name="registry"></a><span data-ttu-id="74594-128">registre</span><span class="sxs-lookup"><span data-stu-id="74594-128">registry</span></span>

```
# Show information about the values in a registry key
registry HKEY_CURRENT_USER\Console
```

```
# Show information about a specific registry value
registry HKEY_CURRENT_USER\Console\\ScreenBufferSize
```


## <a name="remediate"></a><span data-ttu-id="74594-129">corriger</span><span class="sxs-lookup"><span data-stu-id="74594-129">remediate</span></span>

```
# Remediate file in specific path
remediate file c:\Users\user\Desktop\malware.exe
```

```
# Remediate process with specific PID
remediate process 7960
```

```
# See list of all remediated entities
remediate list
```

## <a name="run"></a><span data-ttu-id="74594-130">run</span><span class="sxs-lookup"><span data-stu-id="74594-130">run</span></span>

```
# Run PowerShell script from the library without arguments
run script.ps1
```

```
# Run PowerShell script from the library with arguments
run get-process-by-name.ps1 -parameters "-processName Registry"
```
>[!NOTE]
>
> <span data-ttu-id="74594-131">Pour les commandes de longue durée telles que «**exécuter**» ou «**getfile**» , vous pouvez utiliser le symbole ' ' à la fin de la commande pour effectuer cette action en arrière-plan. **&**</span><span class="sxs-lookup"><span data-stu-id="74594-131">For long running commands such as '**run**' or '**getfile**', you may want to use the '**&**' symbol at the end of the command to perform that action in the background.</span></span>
> <span data-ttu-id="74594-132">Cela vous permettra de continuer à examiner l’ordinateur et de revenir à la commande en arrière-plan lorsque vous avez terminé à l’aide de la commande de base «**fg** [».](live-response.md#basic-commands)</span><span class="sxs-lookup"><span data-stu-id="74594-132">This will allow you to continue investigating the machine and return to the background command when done using '**fg**' [basic command](live-response.md#basic-commands).</span></span>
>
## <a name="scheduledtask"></a><span data-ttu-id="74594-133">scheduledtask</span><span class="sxs-lookup"><span data-stu-id="74594-133">scheduledtask</span></span>

```
# Get all scheduled tasks
scheduledtasks
```

```
# Get specific scheduled task by location and name
scheduledtasks Microsoft\Windows\Subscription\LicenseAcquisition
```

```
# Get specific scheduled task by location and name with spacing
scheduledtasks "Microsoft\Configuration Manager\Configuration Manager Health Evaluation"
```


## <a name="undo"></a><span data-ttu-id="74594-134">undo</span><span class="sxs-lookup"><span data-stu-id="74594-134">undo</span></span>

```
# Restore remediated registry
undo registry HKEY_CURRENT_USER\Console\ScreenBufferSize
```

```
# Restore remediated scheduledtask
undo scheduledtask Microsoft\Windows\Subscription\LicenseAcquisition
```

```
# Restore remediated file
undo file c:\Users\user\Desktop\malware.exe
```

