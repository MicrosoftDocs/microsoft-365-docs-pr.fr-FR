---
title: Utiliser la ligne de commande pour gérer les Antivirus Microsoft Defender
description: Exécutez Antivirus Microsoft Defender analyse et configurez la protection nouvelle génération avec un utilitaire de ligne de commande dédié.
keywords: exécuter l’analyse windows defender, exécuter l’analyse antivirus à partir de la ligne de commande, exécuter l’analyse windows defender à partir de la ligne de commande, mpcmdrun, defender
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.reviewer: ksarens
manager: dansimp
ms.date: 03/19/2021
ms.technology: mde
ms.topic: how-to
ms.openlocfilehash: 85fb60d8d4504ba3a4aa8744c1183d094da01a9b
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52274747"
---
# <a name="configure-and-manage-microsoft-defender-antivirus-with-the-mpcmdrunexe-command-line-tool"></a><span data-ttu-id="8ed2f-104">Configurer et gérer les Antivirus Microsoft Defender l’outil mpcmdrun.exe ligne de commande</span><span class="sxs-lookup"><span data-stu-id="8ed2f-104">Configure and manage Microsoft Defender Antivirus with the mpcmdrun.exe command-line tool</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="8ed2f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8ed2f-105">**Applies to:**</span></span>

- [<span data-ttu-id="8ed2f-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8ed2f-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="8ed2f-107">Vous pouvez effectuer différentes Antivirus Microsoft Defender fonctions avec l’outil en ligne de commande **dédiémpcmdrun.exe**.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-107">You can perform various Microsoft Defender Antivirus functions with the dedicated command-line tool **mpcmdrun.exe**.</span></span> <span data-ttu-id="8ed2f-108">Cet utilitaire est utile lorsque vous souhaitez automatiser l’Antivirus Microsoft Defender’utilisation.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-108">This utility is useful when you want to automate Microsoft Defender Antivirus use.</span></span> <span data-ttu-id="8ed2f-109">Vous trouverez l’utilitaire dans `%ProgramFiles%\Windows Defender\MpCmdRun.exe` .</span><span class="sxs-lookup"><span data-stu-id="8ed2f-109">You can find the utility in `%ProgramFiles%\Windows Defender\MpCmdRun.exe`.</span></span> <span data-ttu-id="8ed2f-110">Vous devez l’exécuter à partir d’une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-110">You must run it from a command prompt.</span></span>

> [!NOTE]
> <span data-ttu-id="8ed2f-111">Vous devrez peut-être ouvrir une version de niveau administrateur de l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-111">You might need to open an administrator-level version of the command prompt.</span></span> <span data-ttu-id="8ed2f-112">Lorsque vous recherchez **l’invite de commandes** dans le menu Démarrer, choisissez **Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="8ed2f-112">When you search for **Command Prompt** on the Start menu, choose **Run as administrator**.</span></span>
> <span data-ttu-id="8ed2f-113">Si vous exécutez une version mise à jour de la plateforme Microsoft Defender, exécutez-la à `**MpCmdRun**` partir de l’emplacement suivant : `C:\ProgramData\Microsoft\Windows Defender\Platform\<version>`</span><span class="sxs-lookup"><span data-stu-id="8ed2f-113">If you're running an updated Microsoft Defender Platform version, run `**MpCmdRun**` from the following location: `C:\ProgramData\Microsoft\Windows Defender\Platform\<version>`.</span></span>

<span data-ttu-id="8ed2f-114">L’utilitaire dispose des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ed2f-114">The utility has the following commands:</span></span>

```console
MpCmdRun.exe [command] [-options]
```
<span data-ttu-id="8ed2f-115">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="8ed2f-115">Here's an example:</span></span>

```console
MpCmdRun.exe -Scan -ScanType 2
``` 

| <span data-ttu-id="8ed2f-116">Command</span><span class="sxs-lookup"><span data-stu-id="8ed2f-116">Command</span></span>  | <span data-ttu-id="8ed2f-117">Description</span><span class="sxs-lookup"><span data-stu-id="8ed2f-117">Description</span></span>   |
|:----|:----|
| <span data-ttu-id="8ed2f-118">`-?`**ou**`-h`</span><span class="sxs-lookup"><span data-stu-id="8ed2f-118">`-?` **or** `-h`</span></span>   | <span data-ttu-id="8ed2f-119">Affiche toutes les options disponibles pour cet outil</span><span class="sxs-lookup"><span data-stu-id="8ed2f-119">Displays all available options for this tool</span></span> |
| `-Scan [-ScanType [0\|1\|2\|3]] [-File <path> [-DisableRemediation] [-BootSectorScan] [-CpuThrottling]] [-Timeout <days>] [-Cancel]` | <span data-ttu-id="8ed2f-120">Recherche les logiciels malveillants.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-120">Scans for malicious software.</span></span> <span data-ttu-id="8ed2f-121">Les valeurs de **ScanType** sont les suivants : **0** Par défaut, en fonction de votre configuration, **-1** Analyse rapide, **-2** Analyse complète, **-3** Analyse personnalisée de fichier et d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-121">Values for **ScanType** are: **0** Default, according to your configuration, **-1** Quick scan, **-2** Full scan, **-3** File and directory custom scan.</span></span>  <span data-ttu-id="8ed2f-122">CpuThrottling respectera la limitation de l’UC configurée à partir de la stratégie</span><span class="sxs-lookup"><span data-stu-id="8ed2f-122">CpuThrottling will honor the configured CPU throttling from policy</span></span> |
| `-Trace [-Grouping #] [-Level #]` | <span data-ttu-id="8ed2f-123">Démarre le suivi des diagnostics</span><span class="sxs-lookup"><span data-stu-id="8ed2f-123">Starts diagnostic tracing</span></span> |
| `-GetFiles [-SupportLogLocation <path>]` | <span data-ttu-id="8ed2f-124">Collecte des informations de support.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-124">Collects support information.</span></span> <span data-ttu-id="8ed2f-125">Voir «[Collecte des données de diagnostic](collect-diagnostic-data.md)»</span><span class="sxs-lookup"><span data-stu-id="8ed2f-125">See '[collecting diagnostic data](collect-diagnostic-data.md)'</span></span>  |
| `-GetFilesDiagTrack`  | <span data-ttu-id="8ed2f-126">Identique à `-GetFiles` , mais sorties dans le dossier DiagTrack temporaire</span><span class="sxs-lookup"><span data-stu-id="8ed2f-126">Same as `-GetFiles`, but outputs to temporary DiagTrack folder</span></span> |
| `-RemoveDefinitions [-All]` | <span data-ttu-id="8ed2f-127">Restaure l’intelligence de sécurité installée sur une copie de sauvegarde précédente ou sur l’ensemble par défaut d’origine</span><span class="sxs-lookup"><span data-stu-id="8ed2f-127">Restores the installed Security intelligence to a previous backup copy or to the original default set</span></span> |
| `-RemoveDefinitions [-DynamicSignatures]` | <span data-ttu-id="8ed2f-128">Supprime uniquement l’intelligence de sécurité téléchargée dynamiquement</span><span class="sxs-lookup"><span data-stu-id="8ed2f-128">Removes only the dynamically downloaded Security intelligence</span></span> |
| `-RemoveDefinitions [-Engine]` | <span data-ttu-id="8ed2f-129">Restaure le moteur installé précédent</span><span class="sxs-lookup"><span data-stu-id="8ed2f-129">Restores the previous installed engine</span></span> |
| `-SignatureUpdate [-UNC \| -MMPC]` | <span data-ttu-id="8ed2f-130">Recherche les nouvelles mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="8ed2f-130">Checks for new Security intelligence updates</span></span> |
| `-Restore  [-ListAll \| [[-Name <name>] [-All] \| [-FilePath <filePath>]] [-Path <path>]]` | <span data-ttu-id="8ed2f-131">Restaure ou répertorie les éléments mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="8ed2f-131">Restores or lists quarantined item(s)</span></span> |
| `-AddDynamicSignature [-Path]` | <span data-ttu-id="8ed2f-132">Charge l’intelligence de sécurité dynamique</span><span class="sxs-lookup"><span data-stu-id="8ed2f-132">Loads dynamic Security intelligence</span></span> |
| `-ListAllDynamicSignatures` | <span data-ttu-id="8ed2f-133">Répertorie l’intelligence de sécurité dynamique chargée</span><span class="sxs-lookup"><span data-stu-id="8ed2f-133">Lists the loaded dynamic Security intelligence</span></span> |
| `-RemoveDynamicSignature [-SignatureSetID]` | <span data-ttu-id="8ed2f-134">Supprime l’intelligence de sécurité dynamique</span><span class="sxs-lookup"><span data-stu-id="8ed2f-134">Removes dynamic Security intelligence</span></span> |
| `-CheckExclusion -path <path>` | <span data-ttu-id="8ed2f-135">Vérifie si un chemin d’accès est exclu</span><span class="sxs-lookup"><span data-stu-id="8ed2f-135">Checks whether a path is excluded</span></span> |
| `-ValidateMapsConnection` | <span data-ttu-id="8ed2f-136">Vérifie que votre réseau peut communiquer avec le service Antivirus Microsoft Defender cloud.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-136">Verifies that your network can communicate with the Microsoft Defender Antivirus cloud service.</span></span> <span data-ttu-id="8ed2f-137">Cette commande ne fonctionne que sur Windows 10 version 1703 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-137">This command will only work on Windows 10, version 1703 or higher.</span></span>|


## <a name="common-errors-in-running-commands-via-mpcmdrunexe"></a><span data-ttu-id="8ed2f-138">Erreurs courantes lors de l’exécution de commandes via mpcmdrun.exe</span><span class="sxs-lookup"><span data-stu-id="8ed2f-138">Common errors in running commands via mpcmdrun.exe</span></span> 

|<span data-ttu-id="8ed2f-139">Message d’erreur</span><span class="sxs-lookup"><span data-stu-id="8ed2f-139">Error message</span></span> | <span data-ttu-id="8ed2f-140">Raison possible</span><span class="sxs-lookup"><span data-stu-id="8ed2f-140">Possible reason</span></span>
|:----|:----|
| `ValidateMapsConnection failed (800106BA) or 0x800106BA` | <span data-ttu-id="8ed2f-141">Le service Antivirus Microsoft Defender est désactivé.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-141">The Microsoft Defender Antivirus service is disabled.</span></span> <span data-ttu-id="8ed2f-142">Activez le service et essayez à nouveau.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-142">Enable the service and try again.</span></span> <br>   <span data-ttu-id="8ed2f-143">**Remarque :**  Dans Windows 10 1909 ou plus, et Windows Server 2019 ou une ancienne, le service était appelé service « Antivirus Windows Defender ».</span><span class="sxs-lookup"><span data-stu-id="8ed2f-143">**Note:**  In Windows 10 1909 or older, and Windows Server 2019 or older, the service used to be called "Windows Defender Antivirus" service.</span></span>|
| `0x80070667` | <span data-ttu-id="8ed2f-144">Vous exécutez la commande à partir d’un ordinateur qui Windows 10 version 1607 ou antérieure, ou qui `-ValidateMapsConnection` Windows Server 2016 ou une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-144">You're running the `-ValidateMapsConnection` command from a computer that is Windows 10 version 1607 or older, or Windows Server 2016 or older.</span></span> <span data-ttu-id="8ed2f-145">Exécutez la commande à partir d’un ordinateur Windows 10 version 1703 ou plus récente, ou Windows Server 2019 ou version plus récente.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-145">Run the command from a machine that is Windows 10 version 1703 or newer, or Windows Server 2019 or newer.</span></span>|
| `'MpCmdRun' is not recognized as an internal or external command, operable program or batch file.` | <span data-ttu-id="8ed2f-146">L’outil doit être exécuté à partir de : ou (où peut différer puisque les mises à jour de plateforme `%ProgramFiles%\Windows Defender` `C:\ProgramData\Microsoft\Windows Defender\Platform\4.18.2012.4-0` sont mensuelles à l’exception `2012.4-0` de mars)</span><span class="sxs-lookup"><span data-stu-id="8ed2f-146">The tool needs to be run from either: `%ProgramFiles%\Windows Defender` or `C:\ProgramData\Microsoft\Windows Defender\Platform\4.18.2012.4-0` (where `2012.4-0` might differ since platform updates are monthly except for March)</span></span>|
| `ValidateMapsConnection failed to establish a connection to MAPS (hr=80070005 httpcode=450)` | <span data-ttu-id="8ed2f-147">Privilèges insuffisants.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-147">Not enough privileges.</span></span> <span data-ttu-id="8ed2f-148">Utilisez l’invite de commandes (cmd.exe) en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-148">Use the command prompt (cmd.exe) as an administrator.</span></span>|
| `ValidateMapsConnection failed to establish a connection to MAPS (hr=80070006 httpcode=451)` | <span data-ttu-id="8ed2f-149">Le pare-feu bloque la connexion ou effectue une inspection SSL.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-149">The firewall is blocking the connection or conducting SSL inspection.</span></span> |
| `ValidateMapsConnection failed to establish a connection to MAPS (hr=80004005 httpcode=450)` | <span data-ttu-id="8ed2f-150">Problèmes éventuels liés au réseau, tels que les problèmes de résolution de noms</span><span class="sxs-lookup"><span data-stu-id="8ed2f-150">Possible network-related issues, like name resolution problems</span></span>|
| `ValidateMapsConnection failed to establish a connection to MAPS (hr=0x80508015` | <span data-ttu-id="8ed2f-151">Le pare-feu bloque la connexion ou effectue une inspection SSL.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-151">The firewall is blocking the connection or conducting SSL inspection.</span></span> |
| `ValidateMapsConnection failed to establish a connection to MAPS (hr=800722F0D` | <span data-ttu-id="8ed2f-152">Le pare-feu bloque la connexion ou effectue une inspection SSL.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-152">The firewall is blocking the connection or conducting SSL inspection.</span></span> |
| `ValidateMapsConnection failed to establish a connection to MAPS (hr=80072EE7 httpcode=451)` | <span data-ttu-id="8ed2f-153">Le pare-feu bloque la connexion ou effectue une inspection SSL.</span><span class="sxs-lookup"><span data-stu-id="8ed2f-153">The firewall is blocking the connection or conducting SSL inspection.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8ed2f-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ed2f-154">See also</span></span>

- [<span data-ttu-id="8ed2f-155">Configurer les fonctionnalités antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="8ed2f-155">Configure Microsoft Defender Antivirus features</span></span>](configure-microsoft-defender-antivirus-features.md)
- [<span data-ttu-id="8ed2f-156">Gérer Antivirus Microsoft Defender dans votre entreprise</span><span class="sxs-lookup"><span data-stu-id="8ed2f-156">Manage Microsoft Defender Antivirus in your business</span></span>](configuration-management-reference-microsoft-defender-antivirus.md)
- [<span data-ttu-id="8ed2f-157">Rubriques de référence pour les outils de gestion et de configuration</span><span class="sxs-lookup"><span data-stu-id="8ed2f-157">Reference topics for management and configuration tools</span></span>](configuration-management-reference-microsoft-defender-antivirus.md)
- [<span data-ttu-id="8ed2f-158">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="8ed2f-158">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)