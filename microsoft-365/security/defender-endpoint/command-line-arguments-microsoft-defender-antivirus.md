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
ms.date: 05/17/2021
ms.technology: mde
ms.topic: how-to
ms.openlocfilehash: eb7fa7fdf5b88bd9361176003817116bcbb1a087
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52538902"
---
# <a name="configure-and-manage-microsoft-defender-antivirus-with-the-mpcmdrunexe-command-line-tool"></a><span data-ttu-id="a9e92-104">Configurer et gérer les Antivirus Microsoft Defender l’outil mpcmdrun.exe ligne de commande</span><span class="sxs-lookup"><span data-stu-id="a9e92-104">Configure and manage Microsoft Defender Antivirus with the mpcmdrun.exe command-line tool</span></span>

<span data-ttu-id="a9e92-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a9e92-105">**Applies to:**</span></span>

- [<span data-ttu-id="a9e92-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a9e92-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="a9e92-107">Vous pouvez effectuer diverses Antivirus Microsoft Defender fonctions avec l’outil de ligne de commande **dédiémpcmdrun.exe**.</span><span class="sxs-lookup"><span data-stu-id="a9e92-107">You can perform various Microsoft Defender Antivirus functions with the dedicated command-line tool **mpcmdrun.exe**.</span></span> <span data-ttu-id="a9e92-108">Cet utilitaire est utile lorsque vous souhaitez automatiser Antivirus Microsoft Defender’utilisation.</span><span class="sxs-lookup"><span data-stu-id="a9e92-108">This utility is useful when you want to automate Microsoft Defender Antivirus use.</span></span> <span data-ttu-id="a9e92-109">Vous pouvez trouver l’utilitaire dans `%ProgramFiles%\Windows Defender\MpCmdRun.exe` .</span><span class="sxs-lookup"><span data-stu-id="a9e92-109">You can find the utility in `%ProgramFiles%\Windows Defender\MpCmdRun.exe`.</span></span> <span data-ttu-id="a9e92-110">Vous devez l’exécuter à partir d’une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="a9e92-110">You must run it from a command prompt.</span></span>

> [!NOTE]
> <span data-ttu-id="a9e92-111">Vous devrez peut-être ouvrir une version de niveau administrateur de l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="a9e92-111">You might need to open an administrator-level version of the command prompt.</span></span> <span data-ttu-id="a9e92-112">Lorsque vous recherchez **l’invite de commandes** dans le menu Démarrer, choisissez **Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="a9e92-112">When you search for **Command Prompt** on the Start menu, choose **Run as administrator**.</span></span>
> <span data-ttu-id="a9e92-113">Si vous exécutez une version mise à jour de la plateforme Microsoft Defender, exécutez-la à `**MpCmdRun**` partir de l’emplacement suivant : `C:\ProgramData\Microsoft\Windows Defender\Platform\<antimalware platform version>`</span><span class="sxs-lookup"><span data-stu-id="a9e92-113">If you're running an updated Microsoft Defender Platform version, run `**MpCmdRun**` from the following location: `C:\ProgramData\Microsoft\Windows Defender\Platform\<antimalware platform version>`.</span></span>
> <span data-ttu-id="a9e92-114">Pour plus d’informations sur la plateforme anti-programme malveillant, voir Antivirus Microsoft Defender mises à jour [et les lignes de base.](manage-updates-baselines-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="a9e92-114">For more information about the antimalware platform, see [Microsoft Defender Antivirus updates and baselines](manage-updates-baselines-microsoft-defender-antivirus.md).</span></span>

<span data-ttu-id="a9e92-115">L’utilitaire MpCmdRun utilise la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a9e92-115">The MpCmdRun utility uses the following syntax:</span></span>

```console
MpCmdRun.exe [command] [-options]
```

<span data-ttu-id="a9e92-116">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="a9e92-116">Here's an example:</span></span>

```console
MpCmdRun.exe -Scan -ScanType 2
``` 

| <span data-ttu-id="a9e92-117">Command</span><span class="sxs-lookup"><span data-stu-id="a9e92-117">Command</span></span>  | <span data-ttu-id="a9e92-118">Description</span><span class="sxs-lookup"><span data-stu-id="a9e92-118">Description</span></span>   |
|:----|:----|
| <span data-ttu-id="a9e92-119">`-?` **ou** `-h`</span><span class="sxs-lookup"><span data-stu-id="a9e92-119">`-?` **or** `-h`</span></span>   | <span data-ttu-id="a9e92-120">Affiche toutes les options disponibles pour cet outil</span><span class="sxs-lookup"><span data-stu-id="a9e92-120">Displays all available options for this tool</span></span> |
| `-Scan [-ScanType [0\|1\|2\|3]] [-File <path> [-DisableRemediation] [-BootSectorScan] [-CpuThrottling]] [-Timeout <days>] [-Cancel]` | <span data-ttu-id="a9e92-121">Recherche les logiciels malveillants.</span><span class="sxs-lookup"><span data-stu-id="a9e92-121">Scans for malicious software.</span></span> <span data-ttu-id="a9e92-122">Les valeurs **de ScanType** sont :</span><span class="sxs-lookup"><span data-stu-id="a9e92-122">Values for **ScanType** are:</span></span><p><span data-ttu-id="a9e92-123">**0 Par** défaut, en fonction de votre configuration</span><span class="sxs-lookup"><span data-stu-id="a9e92-123">**0** Default, according to your configuration</span></span><p><span data-ttu-id="a9e92-124">**-1** Analyse rapide</span><span class="sxs-lookup"><span data-stu-id="a9e92-124">**-1** Quick scan</span></span><p><span data-ttu-id="a9e92-125">**-2** Analyse complète</span><span class="sxs-lookup"><span data-stu-id="a9e92-125">**-2** Full scan</span></span><p><span data-ttu-id="a9e92-126">**-3** Analyse personnalisée de fichier et d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="a9e92-126">**-3** File and directory custom scan.</span></span><p><span data-ttu-id="a9e92-127">CpuThrottling respectera la limitation de l’UC configurée à partir de la stratégie</span><span class="sxs-lookup"><span data-stu-id="a9e92-127">CpuThrottling will honor the configured CPU throttling from policy</span></span> |
| `-Trace [-Grouping #] [-Level #]` | <span data-ttu-id="a9e92-128">Démarre le suivi des diagnostics</span><span class="sxs-lookup"><span data-stu-id="a9e92-128">Starts diagnostic tracing</span></span> |
| `-GetFiles [-SupportLogLocation <path>]` | <span data-ttu-id="a9e92-129">Collecte des informations de support.</span><span class="sxs-lookup"><span data-stu-id="a9e92-129">Collects support information.</span></span> <span data-ttu-id="a9e92-130">Voir «[Collecte des données de diagnostic](collect-diagnostic-data.md)»</span><span class="sxs-lookup"><span data-stu-id="a9e92-130">See '[collecting diagnostic data](collect-diagnostic-data.md)'</span></span>  |
| `-GetFilesDiagTrack`  | <span data-ttu-id="a9e92-131">Identique à `-GetFiles` , mais sorties dans le dossier DiagTrack temporaire</span><span class="sxs-lookup"><span data-stu-id="a9e92-131">Same as `-GetFiles`, but outputs to temporary DiagTrack folder</span></span> |
| `-RemoveDefinitions [-All]` | <span data-ttu-id="a9e92-132">Restaure l’intelligence de sécurité installée sur une copie de sauvegarde précédente ou sur l’ensemble par défaut d’origine</span><span class="sxs-lookup"><span data-stu-id="a9e92-132">Restores the installed Security intelligence to a previous backup copy or to the original default set</span></span> |
| `-RemoveDefinitions [-DynamicSignatures]` | <span data-ttu-id="a9e92-133">Supprime uniquement l’intelligence de sécurité téléchargée dynamiquement</span><span class="sxs-lookup"><span data-stu-id="a9e92-133">Removes only the dynamically downloaded Security intelligence</span></span> |
| `-RemoveDefinitions [-Engine]` | <span data-ttu-id="a9e92-134">Restaure le moteur installé précédent</span><span class="sxs-lookup"><span data-stu-id="a9e92-134">Restores the previous installed engine</span></span> |
| `-SignatureUpdate [-UNC \| -MMPC]` | <span data-ttu-id="a9e92-135">Recherche les nouvelles mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="a9e92-135">Checks for new Security intelligence updates</span></span> |
| `-Restore  [-ListAll \| [[-Name <name>] [-All] \| [-FilePath <filePath>]] [-Path <path>]]` | <span data-ttu-id="a9e92-136">Restaure ou répertorie les éléments mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a9e92-136">Restores or lists quarantined item(s)</span></span> |
| `-AddDynamicSignature [-Path]` | <span data-ttu-id="a9e92-137">Charge l’intelligence de sécurité dynamique</span><span class="sxs-lookup"><span data-stu-id="a9e92-137">Loads dynamic Security intelligence</span></span> |
| `-ListAllDynamicSignatures` | <span data-ttu-id="a9e92-138">Répertorie l’intelligence de sécurité dynamique chargée</span><span class="sxs-lookup"><span data-stu-id="a9e92-138">Lists the loaded dynamic Security intelligence</span></span> |
| `-RemoveDynamicSignature [-SignatureSetID]` | <span data-ttu-id="a9e92-139">Supprime l’intelligence de sécurité dynamique</span><span class="sxs-lookup"><span data-stu-id="a9e92-139">Removes dynamic Security intelligence</span></span> |
| `-CheckExclusion -path <path>` | <span data-ttu-id="a9e92-140">Vérifie si un chemin d’accès est exclu</span><span class="sxs-lookup"><span data-stu-id="a9e92-140">Checks whether a path is excluded</span></span> |
| `-ValidateMapsConnection` | <span data-ttu-id="a9e92-141">Vérifie que votre réseau peut communiquer avec le service Antivirus Microsoft Defender cloud.</span><span class="sxs-lookup"><span data-stu-id="a9e92-141">Verifies that your network can communicate with the Microsoft Defender Antivirus cloud service.</span></span> <span data-ttu-id="a9e92-142">Cette commande ne fonctionne que sur Windows 10 version 1703 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="a9e92-142">This command will only work on Windows 10, version 1703 or higher.</span></span>|


## <a name="common-errors-in-running-commands-via-mpcmdrunexe"></a><span data-ttu-id="a9e92-143">Erreurs courantes lors de l’exécution de commandes via mpcmdrun.exe</span><span class="sxs-lookup"><span data-stu-id="a9e92-143">Common errors in running commands via mpcmdrun.exe</span></span> 

|<span data-ttu-id="a9e92-144">Message d’erreur</span><span class="sxs-lookup"><span data-stu-id="a9e92-144">Error message</span></span> | <span data-ttu-id="a9e92-145">Raison possible</span><span class="sxs-lookup"><span data-stu-id="a9e92-145">Possible reason</span></span>
|:----|:----|
| `ValidateMapsConnection failed (800106BA) or 0x800106BA` | <span data-ttu-id="a9e92-146">Le service Antivirus Microsoft Defender est désactivé.</span><span class="sxs-lookup"><span data-stu-id="a9e92-146">The Microsoft Defender Antivirus service is disabled.</span></span> <span data-ttu-id="a9e92-147">Activez le service et essayez à nouveau.</span><span class="sxs-lookup"><span data-stu-id="a9e92-147">Enable the service and try again.</span></span> <br>   <span data-ttu-id="a9e92-148">**Remarque :**  Dans Windows 10 1909 ou plus, et Windows Server 2019 ou plus ancien, le service était appelé service Antivirus Windows Defender *service.*</span><span class="sxs-lookup"><span data-stu-id="a9e92-148">**Note:**  In Windows 10 1909 or older, and Windows Server 2019 or older, the service used to be called the *Windows Defender Antivirus* service.</span></span>|
| `0x80070667` | <span data-ttu-id="a9e92-149">Vous exécutez la commande à partir d’un ordinateur qui Windows 10 version 1607 ou antérieure, ou qui `-ValidateMapsConnection` Windows Server 2016 ou une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="a9e92-149">You're running the `-ValidateMapsConnection` command from a computer that is Windows 10 version 1607 or older, or Windows Server 2016 or older.</span></span> <span data-ttu-id="a9e92-150">Exécutez la commande à partir d’un ordinateur Windows 10 version 1703 ou plus récente, ou Windows Server 2019 ou version plus récente.</span><span class="sxs-lookup"><span data-stu-id="a9e92-150">Run the command from a machine that is Windows 10 version 1703 or newer, or Windows Server 2019 or newer.</span></span>|
| `'MpCmdRun' is not recognized as an internal or external command, operable program or batch file.` | <span data-ttu-id="a9e92-151">L’outil doit être exécuté à partir de : ou (où peut différer étant donné que les mises à jour de plateforme `%ProgramFiles%\Windows Defender` `C:\ProgramData\Microsoft\Windows Defender\Platform\4.18.2012.4-0` sont `2012.4-0` mensuelles à l’exception de mars)</span><span class="sxs-lookup"><span data-stu-id="a9e92-151">The tool needs to be run from either: `%ProgramFiles%\Windows Defender` or `C:\ProgramData\Microsoft\Windows Defender\Platform\4.18.2012.4-0` (where `2012.4-0` might differ since platform updates are monthly except for March)</span></span>|
| `ValidateMapsConnection failed to establish a connection to MAPS (hr=80070005 httpcode=450)` | <span data-ttu-id="a9e92-152">Privilèges insuffisants.</span><span class="sxs-lookup"><span data-stu-id="a9e92-152">Not enough privileges.</span></span> <span data-ttu-id="a9e92-153">Utilisez l’invite de commandes (cmd.exe) en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="a9e92-153">Use the command prompt (cmd.exe) as an administrator.</span></span>|
| `ValidateMapsConnection failed to establish a connection to MAPS (hr=80070006 httpcode=451)` | <span data-ttu-id="a9e92-154">Le pare-feu bloque la connexion ou effectue une inspection SSL.</span><span class="sxs-lookup"><span data-stu-id="a9e92-154">The firewall is blocking the connection or conducting SSL inspection.</span></span> |
| `ValidateMapsConnection failed to establish a connection to MAPS (hr=80004005 httpcode=450)` | <span data-ttu-id="a9e92-155">Problèmes éventuels liés au réseau, tels que les problèmes de résolution de noms</span><span class="sxs-lookup"><span data-stu-id="a9e92-155">Possible network-related issues, like name resolution problems</span></span>|
| `ValidateMapsConnection failed to establish a connection to MAPS (hr=0x80508015` | <span data-ttu-id="a9e92-156">Le pare-feu bloque la connexion ou effectue une inspection SSL.</span><span class="sxs-lookup"><span data-stu-id="a9e92-156">The firewall is blocking the connection or conducting SSL inspection.</span></span> |
| `ValidateMapsConnection failed to establish a connection to MAPS (hr=800722F0D` | <span data-ttu-id="a9e92-157">Le pare-feu bloque la connexion ou effectue une inspection SSL.</span><span class="sxs-lookup"><span data-stu-id="a9e92-157">The firewall is blocking the connection or conducting SSL inspection.</span></span> |
| `ValidateMapsConnection failed to establish a connection to MAPS (hr=80072EE7 httpcode=451)` | <span data-ttu-id="a9e92-158">Le pare-feu bloque la connexion ou effectue une inspection SSL.</span><span class="sxs-lookup"><span data-stu-id="a9e92-158">The firewall is blocking the connection or conducting SSL inspection.</span></span> |

## <a name="see-also"></a><span data-ttu-id="a9e92-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9e92-159">See also</span></span>

- [<span data-ttu-id="a9e92-160">Configurer les fonctionnalités antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="a9e92-160">Configure Microsoft Defender Antivirus features</span></span>](configure-microsoft-defender-antivirus-features.md)
- [<span data-ttu-id="a9e92-161">Gérer Antivirus Microsoft Defender dans votre entreprise</span><span class="sxs-lookup"><span data-stu-id="a9e92-161">Manage Microsoft Defender Antivirus in your business</span></span>](configuration-management-reference-microsoft-defender-antivirus.md)
- [<span data-ttu-id="a9e92-162">Rubriques de référence pour les outils de gestion et de configuration</span><span class="sxs-lookup"><span data-stu-id="a9e92-162">Reference topics for management and configuration tools</span></span>](configuration-management-reference-microsoft-defender-antivirus.md)
- [<span data-ttu-id="a9e92-163">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="a9e92-163">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)