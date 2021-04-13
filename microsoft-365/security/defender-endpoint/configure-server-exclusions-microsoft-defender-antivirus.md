---
title: Configurer les exclusions de l'Antivirus Microsoft Defender sur Windows Server
ms.reviewer: ''
manager: dansimp
description: Windows Server inclut des exclusions automatiques, basées sur le rôle serveur. Vous pouvez également ajouter des exclusions personnalisées.
keywords: exclusions, serveur, exclusions automatiques, automatique, personnalisé, analyses, Antivirus Microsoft Defender
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
ms.localizationpriority: medium
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.technology: mde
ms.date: 02/10/2021
ms.openlocfilehash: 555daac32b202b0b9f46c4f19fa6e4b04bcadda3
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51690316"
---
# <a name="configure-microsoft-defender-antivirus-exclusions-on-windows-server"></a><span data-ttu-id="90c5b-105">Configurer les exclusions de l'Antivirus Microsoft Defender sur Windows Server</span><span class="sxs-lookup"><span data-stu-id="90c5b-105">Configure Microsoft Defender Antivirus exclusions on Windows Server</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="90c5b-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="90c5b-106">**Applies to:**</span></span>

- [<span data-ttu-id="90c5b-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="90c5b-107">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="90c5b-108">L'Antivirus Microsoft Defender sur Windows Server 2016 et Windows Server 2019 vous inscrit automatiquement dans certaines exclusions, telles que définies par votre rôle serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="90c5b-108">Microsoft Defender Antivirus on Windows Server 2016 and Windows Server 2019 automatically enrolls you in certain exclusions, as defined by your specified server role.</span></span> <span data-ttu-id="90c5b-109">Ces exclusions n'apparaissent pas dans les listes d'exclusions standard affichées dans [l'application Sécurité Windows.](microsoft-defender-security-center-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="90c5b-109">These exclusions do not appear in the standard exclusion lists that are shown in the [Windows Security app](microsoft-defender-security-center-antivirus.md).</span></span>

> [!NOTE]
> <span data-ttu-id="90c5b-110">Les exclusions automatiques s'appliquent uniquement à l'analyse de la protection en temps réel (RTP).</span><span class="sxs-lookup"><span data-stu-id="90c5b-110">Automatic exclusions only apply to Real-time protection (RTP) scanning.</span></span> <span data-ttu-id="90c5b-111">Les exclusions automatiques ne sont pas honorées lors d'une analyse complète/rapide ou à la demande.</span><span class="sxs-lookup"><span data-stu-id="90c5b-111">Automatic exclusions are not honored during a Full/Quick or On-demand scan.</span></span>

<span data-ttu-id="90c5b-112">Outre les exclusions automatiques définies par le rôle serveur, vous pouvez ajouter ou supprimer des exclusions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="90c5b-112">In addition to server role-defined automatic exclusions, you can add or remove custom exclusions.</span></span> <span data-ttu-id="90c5b-113">Pour ce faire, reportez-vous aux articles suivants :</span><span class="sxs-lookup"><span data-stu-id="90c5b-113">To do that, refer to these articles:</span></span>
- [<span data-ttu-id="90c5b-114">Configurer et valider des exclusions en fonction du nom de fichier, de l'extension et de l'emplacement du dossier</span><span class="sxs-lookup"><span data-stu-id="90c5b-114">Configure and validate exclusions based on file name, extension, and folder location</span></span>](configure-extension-file-exclusions-microsoft-defender-antivirus.md)
- [<span data-ttu-id="90c5b-115">Configurer et valider des exclusions pour les fichiers ouverts par des processus</span><span class="sxs-lookup"><span data-stu-id="90c5b-115">Configure and validate exclusions for files opened by processes</span></span>](configure-process-opened-file-exclusions-microsoft-defender-antivirus.md)

## <a name="a-few-points-to-keep-in-mind"></a><span data-ttu-id="90c5b-116">Quelques points à garder à l'esprit</span><span class="sxs-lookup"><span data-stu-id="90c5b-116">A few points to keep in mind</span></span>

<span data-ttu-id="90c5b-117">Gardez les points importants suivants à l'esprit :</span><span class="sxs-lookup"><span data-stu-id="90c5b-117">Keep the following important points in mind:</span></span>

- <span data-ttu-id="90c5b-118">Les exclusions personnalisées prévalent sur les exclusions automatiques.</span><span class="sxs-lookup"><span data-stu-id="90c5b-118">Custom exclusions take precedence over automatic exclusions.</span></span>
- <span data-ttu-id="90c5b-119">Les exclusions automatiques s'appliquent uniquement à l'analyse de la protection en temps réel (RTP).</span><span class="sxs-lookup"><span data-stu-id="90c5b-119">Automatic exclusions only apply to Real-time protection (RTP) scanning.</span></span> <span data-ttu-id="90c5b-120">Les exclusions automatiques ne sont pas honorées lors d'une analyse complète/rapide ou à la demande.</span><span class="sxs-lookup"><span data-stu-id="90c5b-120">Automatic exclusions are not honored during a Full/Quick or On-demand scan.</span></span>
- <span data-ttu-id="90c5b-121">Les exclusions personnalisées et dupliquées ne sont pas en conflit avec les exclusions automatiques.</span><span class="sxs-lookup"><span data-stu-id="90c5b-121">Custom and duplicate exclusions do not conflict with automatic exclusions.</span></span>
- <span data-ttu-id="90c5b-122">L'Antivirus Microsoft Defender utilise les outils gestion et maintenance des images de déploiement (DISM) pour déterminer les rôles installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="90c5b-122">Microsoft Defender Antivirus uses the Deployment Image Servicing and Management (DISM) tools to determine which roles are installed on your computer.</span></span>

## <a name="opt-out-of-automatic-exclusions"></a><span data-ttu-id="90c5b-123">Refuser les exclusions automatiques</span><span class="sxs-lookup"><span data-stu-id="90c5b-123">Opt out of automatic exclusions</span></span>

<span data-ttu-id="90c5b-124">Dans Windows Server 2016 et Windows Server 2019, les exclusions prédéfines délivrées par les mises à jour de l'intelligence de sécurité excluent uniquement les chemins d'accès par défaut pour un rôle ou une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="90c5b-124">In Windows Server 2016 and Windows Server 2019, the predefined exclusions delivered by Security intelligence updates only exclude the default paths for a role or feature.</span></span> <span data-ttu-id="90c5b-125">Si vous avez installé un rôle ou une fonctionnalité dans un chemin d'accès personnalisé, ou si vous souhaitez contrôler manuellement l'ensemble des exclusions, veillez à refuser les exclusions automatiques délivrées dans les mises à jour de l'intelligence de sécurité.</span><span class="sxs-lookup"><span data-stu-id="90c5b-125">If you installed a role or feature in a custom path, or you want to manually control the set of exclusions, make sure to opt out of the automatic exclusions delivered in Security intelligence updates.</span></span> <span data-ttu-id="90c5b-126">Mais n'oubliez pas que les exclusions qui sont automatiquement livrées sont optimisées pour les rôles Windows Server 2016 et 2019.</span><span class="sxs-lookup"><span data-stu-id="90c5b-126">But keep in mind that the exclusions that are delivered automatically are optimized for Windows Server 2016 and 2019 roles.</span></span> <span data-ttu-id="90c5b-127">Voir [Recommandations pour définir des exclusions avant](configure-exclusions-microsoft-defender-antivirus.md#recommendations-for-defining-exclusions) de définir vos listes d'exclusions.</span><span class="sxs-lookup"><span data-stu-id="90c5b-127">See [Recommendations for defining exclusions](configure-exclusions-microsoft-defender-antivirus.md#recommendations-for-defining-exclusions) before defining your exclusion lists.</span></span>

> [!WARNING]
> <span data-ttu-id="90c5b-128">Le fait de refuser les exclusions automatiques peut avoir un impact négatif sur les performances ou entraîner une altération des données.</span><span class="sxs-lookup"><span data-stu-id="90c5b-128">Opting out of automatic exclusions may adversely impact performance, or result in data corruption.</span></span> <span data-ttu-id="90c5b-129">Les exclusions qui sont livrées automatiquement sont optimisées pour les rôles Windows Server 2016 et Windows Server 2019.</span><span class="sxs-lookup"><span data-stu-id="90c5b-129">The exclusions that are delivered automatically are optimized for Windows Server 2016 and Windows Server 2019 roles.</span></span>

<span data-ttu-id="90c5b-130">Étant donné que les exclusions prédéfinie excluent uniquement les chemins d'accès par **défaut,** si vous déplacez NTDS et SYSVOL vers un autre lecteur ou chemin d'accès différent du chemin d'accès d'origine, vous devez ajouter des exclusions manuellement à l'aide des informations [ici.](configure-extension-file-exclusions-microsoft-defender-antivirus.md#configure-the-list-of-exclusions-based-on-folder-name-or-file-extension)</span><span class="sxs-lookup"><span data-stu-id="90c5b-130">Because predefined exclusions only exclude **default paths**, if you move NTDS and SYSVOL to another drive or path that is *different from the original path*, you must add exclusions manually using the information [here](configure-extension-file-exclusions-microsoft-defender-antivirus.md#configure-the-list-of-exclusions-based-on-folder-name-or-file-extension) .</span></span>

<span data-ttu-id="90c5b-131">Vous pouvez désactiver les listes d'exclusion automatique avec la stratégie de groupe, les cmdlets PowerShell et WMI.</span><span class="sxs-lookup"><span data-stu-id="90c5b-131">You can disable the automatic exclusion lists with Group Policy, PowerShell cmdlets, and WMI.</span></span>

### <a name="use-group-policy-to-disable-the-auto-exclusions-list-on-windows-server-2016-and-windows-server-2019"></a><span data-ttu-id="90c5b-132">Utiliser une stratégie de groupe pour désactiver la liste d'exclusions automatiques sur Windows Server 2016 et Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="90c5b-132">Use Group Policy to disable the auto-exclusions list on Windows Server 2016 and Windows Server 2019</span></span>

1. <span data-ttu-id="90c5b-133">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console de gestion des stratégies de groupe.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc725752(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="90c5b-133">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc725752(v=ws.11)).</span></span> <span data-ttu-id="90c5b-134">Cliquez avec le bouton droit sur l'objet de stratégie de groupe que vous souhaitez configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="90c5b-134">Right-click the Group Policy Object you want to configure, and then click **Edit**.</span></span>
2. <span data-ttu-id="90c5b-135">Dans **l'Éditeur de gestion des stratégies** de groupe, allez à **Configuration** ordinateur, puis cliquez sur **Modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="90c5b-135">In the **Group Policy Management Editor** go to **Computer configuration**, and then click **Administrative templates**.</span></span>
3. <span data-ttu-id="90c5b-136">Développez l'arborescence **des composants Windows**  >  **Exclusions de l'Antivirus Microsoft Defender.**  >  </span><span class="sxs-lookup"><span data-stu-id="90c5b-136">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Exclusions**.</span></span>
4. <span data-ttu-id="90c5b-137">Double-cliquez **sur Désactiver les exclusions automatiques** et définissez l'option sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="90c5b-137">Double-click **Turn off Auto Exclusions**, and set the option to **Enabled**.</span></span> <span data-ttu-id="90c5b-138">Cliquez ensuite sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="90c5b-138">Then click **OK**.</span></span> 

### <a name="use-powershell-cmdlets-to-disable-the-auto-exclusions-list-on-windows-server-2016-and-2019"></a><span data-ttu-id="90c5b-139">Utiliser les cmdlets PowerShell pour désactiver la liste d'exclusions automatiques sur Windows Server 2016 et 2019</span><span class="sxs-lookup"><span data-stu-id="90c5b-139">Use PowerShell cmdlets to disable the auto-exclusions list on Windows Server 2016 and 2019</span></span>

<span data-ttu-id="90c5b-140">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="90c5b-140">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -DisableAutoExclusions $true
```

<span data-ttu-id="90c5b-141">Pour en savoir plus, consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="90c5b-141">To learn more, see the following resources:</span></span>

- <span data-ttu-id="90c5b-142">[Utilisez les cmdlets PowerShell pour configurer et exécuter l'Antivirus Microsoft Defender.](use-powershell-cmdlets-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="90c5b-142">[Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md).</span></span>
- <span data-ttu-id="90c5b-143">[Utilisez PowerShell avec l'Antivirus Microsoft Defender.](/powershell/module/defender/)</span><span class="sxs-lookup"><span data-stu-id="90c5b-143">[Use PowerShell with Microsoft Defender Antivirus](/powershell/module/defender/).</span></span>

### <a name="use-windows-management-instruction-wmi-to-disable-the-auto-exclusions-list-on-windows-server-2016-and-windows-server-2019"></a><span data-ttu-id="90c5b-144">Utiliser Windows Management Instruction (WMI) pour désactiver la liste d'exclusions automatiques sur Windows Server 2016 et Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="90c5b-144">Use Windows Management Instruction (WMI) to disable the auto-exclusions list on Windows Server 2016 and Windows Server 2019</span></span>

<span data-ttu-id="90c5b-145">Utilisez la **méthode Set** de la [classe MSFT_MpPreference](/previous-versions/windows/desktop/defender/msft-mppreference) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="90c5b-145">Use the **Set** method of the [MSFT_MpPreference](/previous-versions/windows/desktop/defender/msft-mppreference) class for the following properties:</span></span>

```WMI
DisableAutoExclusions
```

<span data-ttu-id="90c5b-146">Pour plus d'informations et les paramètres autorisés, voir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="90c5b-146">See the following for more information and allowed parameters:</span></span>
- [<span data-ttu-id="90c5b-147">Windows Defender API WMIv2</span><span class="sxs-lookup"><span data-stu-id="90c5b-147">Windows Defender WMIv2 APIs</span></span>](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)

## <a name="list-of-automatic-exclusions"></a><span data-ttu-id="90c5b-148">Liste des exclusions automatiques</span><span class="sxs-lookup"><span data-stu-id="90c5b-148">List of automatic exclusions</span></span>

<span data-ttu-id="90c5b-149">Les sections suivantes contiennent les exclusions qui sont livrées avec des chemins d'accès et des types de fichiers d'exclusions automatiques.</span><span class="sxs-lookup"><span data-stu-id="90c5b-149">The following sections contain the exclusions that are delivered with automatic exclusions file paths and file types.</span></span>

### <a name="default-exclusions-for-all-roles"></a><span data-ttu-id="90c5b-150">Exclusions par défaut pour tous les rôles</span><span class="sxs-lookup"><span data-stu-id="90c5b-150">Default exclusions for all roles</span></span>

<span data-ttu-id="90c5b-151">Cette section répertorie les exclusions par défaut pour tous les rôles Windows Server 2016 et 2019.</span><span class="sxs-lookup"><span data-stu-id="90c5b-151">This section lists the default exclusions for all Windows Server 2016 and 2019 roles.</span></span>

> [!NOTE]
> <span data-ttu-id="90c5b-152">Les emplacements par défaut peuvent être différents de ceux répertoriés dans cet article.</span><span class="sxs-lookup"><span data-stu-id="90c5b-152">The default locations could be different than what's listed in this article.</span></span>

#### <a name="windows-tempedb-files"></a><span data-ttu-id="90c5b-153">Fichiers « temp.edb » Windows</span><span class="sxs-lookup"><span data-stu-id="90c5b-153">Windows "temp.edb" files</span></span>

- `%windir%\SoftwareDistribution\Datastore\*\tmp.edb`
- `%ProgramData%\Microsoft\Search\Data\Applications\Windows\*\*.log`

#### <a name="windows-update-files-or-automatic-update-files"></a><span data-ttu-id="90c5b-154">Fichiers Windows Update ou fichiers de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="90c5b-154">Windows Update files or Automatic Update files</span></span>

- `%windir%\SoftwareDistribution\Datastore\*\Datastore.edb`
- `%windir%\SoftwareDistribution\Datastore\*\edb.chk`
- `%windir%\SoftwareDistribution\Datastore\*\edb\*.log`
- `%windir%\SoftwareDistribution\Datastore\*\Edb\*.jrs`
- `%windir%\SoftwareDistribution\Datastore\*\Res\*.log`

#### <a name="windows-security-files"></a><span data-ttu-id="90c5b-155">Fichiers de sécurité Windows</span><span class="sxs-lookup"><span data-stu-id="90c5b-155">Windows Security files</span></span>

- `%windir%\Security\database\*.chk`
- `%windir%\Security\database\*.edb`
- `%windir%\Security\database\*.jrs`
- `%windir%\Security\database\*.log`
- `%windir%\Security\database\*.sdb`

#### <a name="group-policy-files"></a><span data-ttu-id="90c5b-156">Fichiers de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="90c5b-156">Group Policy files</span></span>

- `%allusersprofile%\NTUser.pol`
- `%SystemRoot%\System32\GroupPolicy\Machine\registry.pol`
- `%SystemRoot%\System32\GroupPolicy\User\registry.pol`

#### <a name="wins-files"></a><span data-ttu-id="90c5b-157">Fichiers WINS</span><span class="sxs-lookup"><span data-stu-id="90c5b-157">WINS files</span></span>

- `%systemroot%\System32\Wins\*\*.chk`
- `%systemroot%\System32\Wins\*\*.log`
- `%systemroot%\System32\Wins\*\*.mdb`
- `%systemroot%\System32\LogFiles\`
- `%systemroot%\SysWow64\LogFiles\`

#### <a name="file-replication-service-frs-exclusions"></a><span data-ttu-id="90c5b-158">Exclusions du service de réplication de fichiers (FRS)</span><span class="sxs-lookup"><span data-stu-id="90c5b-158">File Replication Service (FRS) exclusions</span></span>

- <span data-ttu-id="90c5b-159">Fichiers dans le dossier de travail du service de réplication de fichiers (FRS).</span><span class="sxs-lookup"><span data-stu-id="90c5b-159">Files in the File Replication Service (FRS) working folder.</span></span> <span data-ttu-id="90c5b-160">Le dossier de travail FRS est spécifié dans la clé de Registre `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\NtFrs\Parameters\Working Directory`</span><span class="sxs-lookup"><span data-stu-id="90c5b-160">The FRS working folder is specified in the registry key `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\NtFrs\Parameters\Working Directory`</span></span>

  - `%windir%\Ntfrs\jet\sys\*\edb.chk`
  - `%windir%\Ntfrs\jet\*\Ntfrs.jdb`
  - `%windir%\Ntfrs\jet\log\*\*.log`

- <span data-ttu-id="90c5b-161">Fichiers journaux de base de données FRS.</span><span class="sxs-lookup"><span data-stu-id="90c5b-161">FRS Database log files.</span></span> <span data-ttu-id="90c5b-162">Le dossier du fichier journal de la base de données FRS est spécifié dans la clé de Registre `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Ntfrs\Parameters\DB Log File Directory`</span><span class="sxs-lookup"><span data-stu-id="90c5b-162">The FRS Database log file folder is specified in the registry key `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Ntfrs\Parameters\DB Log File Directory`</span></span>

  - `%windir%\Ntfrs\*\Edb\*.log`

- <span data-ttu-id="90c5b-163">Dossier intermédiaire FRS.</span><span class="sxs-lookup"><span data-stu-id="90c5b-163">The FRS staging folder.</span></span> <span data-ttu-id="90c5b-164">Le dossier de transit est spécifié dans la clé de Registre `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\NtFrs\Parameters\Replica Sets\GUID\Replica Set Stage`</span><span class="sxs-lookup"><span data-stu-id="90c5b-164">The staging folder is specified in the registry key `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\NtFrs\Parameters\Replica Sets\GUID\Replica Set Stage`</span></span>

  - `%systemroot%\Sysvol\*\Ntfrs_cmp*\`

- <span data-ttu-id="90c5b-165">Dossier de préinstallation FRS.</span><span class="sxs-lookup"><span data-stu-id="90c5b-165">The FRS preinstall folder.</span></span> <span data-ttu-id="90c5b-166">Ce dossier est spécifié par le dossier `Replica_root\DO_NOT_REMOVE_NtFrs_PreInstall_Directory`</span><span class="sxs-lookup"><span data-stu-id="90c5b-166">This folder is specified by the folder `Replica_root\DO_NOT_REMOVE_NtFrs_PreInstall_Directory`</span></span>

  - `%systemroot%\SYSVOL\domain\DO_NOT_REMOVE_NtFrs_PreInstall_Directory\*\Ntfrs*\`

- <span data-ttu-id="90c5b-167">La base de données de réplication du système de fichiers distribués (DFSR) et les dossiers de travail.</span><span class="sxs-lookup"><span data-stu-id="90c5b-167">The Distributed File System Replication (DFSR) database and working folders.</span></span> <span data-ttu-id="90c5b-168">Ces dossiers sont spécifiés par la clé de Registre `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\DFSR\Parameters\Replication Groups\GUID\Replica Set Configuration File`</span><span class="sxs-lookup"><span data-stu-id="90c5b-168">These folders are specified by the registry key `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\DFSR\Parameters\Replication Groups\GUID\Replica Set Configuration File`</span></span>

  > [!NOTE]
  > <span data-ttu-id="90c5b-169">Pour les emplacements personnalisés, voir [Refuser les exclusions automatiques.](#opt-out-of-automatic-exclusions)</span><span class="sxs-lookup"><span data-stu-id="90c5b-169">For custom locations, see [Opt out of automatic exclusions](#opt-out-of-automatic-exclusions).</span></span>

  - `%systemdrive%\System Volume Information\DFSR\$db_normal$`
  - `%systemdrive%\System Volume Information\DFSR\FileIDTable_*`
  - `%systemdrive%\System Volume Information\DFSR\SimilarityTable_*`
  - `%systemdrive%\System Volume Information\DFSR\*.XML`
  - `%systemdrive%\System Volume Information\DFSR\$db_dirty$`
  - `%systemdrive%\System Volume Information\DFSR\$db_clean$`
  - `%systemdrive%\System Volume Information\DFSR\$db_lostl$`
  - `%systemdrive%\System Volume Information\DFSR\Dfsr.db`
  - `%systemdrive%\System Volume Information\DFSR\*.frx`
  - `%systemdrive%\System Volume Information\DFSR\*.log`
  - `%systemdrive%\System Volume Information\DFSR\Fsr*.jrs`
  - `%systemdrive%\System Volume Information\DFSR\Tmp.edb`

#### <a name="process-exclusions"></a><span data-ttu-id="90c5b-170">Exclusions de processus</span><span class="sxs-lookup"><span data-stu-id="90c5b-170">Process exclusions</span></span>

- `%systemroot%\System32\dfsr.exe`
- `%systemroot%\System32\dfsrs.exe`

#### <a name="hyper-v-exclusions"></a><span data-ttu-id="90c5b-171">Exclusions Hyper-V</span><span class="sxs-lookup"><span data-stu-id="90c5b-171">Hyper-V exclusions</span></span>

<span data-ttu-id="90c5b-172">Le tableau suivant répertorie les exclusions de types de fichiers, les exclusions de dossiers et les exclusions de processus qui sont automatiquement livrées lorsque vous installez le rôle Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="90c5b-172">The following table lists the file type exclusions, folder exclusions, and process exclusions that are delivered automatically when you install the Hyper-V role.</span></span>

|<span data-ttu-id="90c5b-173">Exclusions de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="90c5b-173">File type exclusions</span></span> |<span data-ttu-id="90c5b-174">Exclusions de dossiers</span><span class="sxs-lookup"><span data-stu-id="90c5b-174">Folder exclusions</span></span>  | <span data-ttu-id="90c5b-175">Process exclusions</span><span class="sxs-lookup"><span data-stu-id="90c5b-175">Process exclusions</span></span> |
|:--|:--|:--|
| `*.vhd` <br/> `*.vhdx` <br/> `*.avhd` <br/> `*.avhdx` <br/> `*.vsv` <br/> `*.iso` <br/> `*.rct` <br/> `*.vmcx` <br/> `*.vmrs` | `%ProgramData%\Microsoft\Windows\Hyper-V` <br/> `%ProgramFiles%\Hyper-V` <br/> `%SystemDrive%\ProgramData\Microsoft\Windows\Hyper-V\Snapshots` <br/> `%Public%\Documents\Hyper-V\Virtual Hard Disks` | `%systemroot%\System32\Vmms.exe` <br/> `%systemroot%\System32\Vmwp.exe` |

#### <a name="sysvol-files"></a><span data-ttu-id="90c5b-176">Fichiers SYSVOL</span><span class="sxs-lookup"><span data-stu-id="90c5b-176">SYSVOL files</span></span>

- `%systemroot%\Sysvol\Domain\*.adm`
- `%systemroot%\Sysvol\Domain\*.admx`
- `%systemroot%\Sysvol\Domain\*.adml`
- `%systemroot%\Sysvol\Domain\Registry.pol`
- `%systemroot%\Sysvol\Domain\*.aas`
- `%systemroot%\Sysvol\Domain\*.inf`
- `%systemroot%\Sysvol\Domain\*Scripts.ini`
- `%systemroot%\Sysvol\Domain\*.ins`
- `%systemroot%\Sysvol\Domain\Oscfilter.ini`


### <a name="active-directory-exclusions"></a><span data-ttu-id="90c5b-177">Exclusions Active Directory</span><span class="sxs-lookup"><span data-stu-id="90c5b-177">Active Directory exclusions</span></span>

<span data-ttu-id="90c5b-178">Cette section répertorie les exclusions qui sont automatiquement livrées lorsque vous installez les services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="90c5b-178">This section lists the exclusions that are delivered automatically when you install Active Directory Domain Services.</span></span>

#### <a name="ntds-database-files"></a><span data-ttu-id="90c5b-179">Fichiers de base de données NTDS</span><span class="sxs-lookup"><span data-stu-id="90c5b-179">NTDS database files</span></span>

<span data-ttu-id="90c5b-180">Les fichiers de base de données sont spécifiés dans la clé de Registre `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\NTDS\Parameters\DSA Database File`</span><span class="sxs-lookup"><span data-stu-id="90c5b-180">The database files are specified in the registry key `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\NTDS\Parameters\DSA Database File`</span></span>

- `%windir%\Ntds\ntds.dit`
- `%windir%\Ntds\ntds.pat`

#### <a name="the-ad-ds-transaction-log-files"></a><span data-ttu-id="90c5b-181">Fichiers journaux des transactions AD DS</span><span class="sxs-lookup"><span data-stu-id="90c5b-181">The AD DS transaction log files</span></span>

<span data-ttu-id="90c5b-182">Les fichiers journaux des transactions sont spécifiés dans la clé de Registre `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\NTDS\Parameters\Database Log Files Path`</span><span class="sxs-lookup"><span data-stu-id="90c5b-182">The transaction log files are specified in the registry key `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\NTDS\Parameters\Database Log Files Path`</span></span>

- `%windir%\Ntds\EDB*.log`
- `%windir%\Ntds\Res*.log`
- `%windir%\Ntds\Edb*.jrs`
- `%windir%\Ntds\Ntds*.pat`
- `%windir%\Ntds\TEMP.edb`

#### <a name="the-ntds-working-folder"></a><span data-ttu-id="90c5b-183">Dossier de travail NTDS</span><span class="sxs-lookup"><span data-stu-id="90c5b-183">The NTDS working folder</span></span>

<span data-ttu-id="90c5b-184">Ce dossier est spécifié dans la clé de Registre `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\NTDS\Parameters\DSA Working Directory`</span><span class="sxs-lookup"><span data-stu-id="90c5b-184">This folder is specified in the registry key `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\NTDS\Parameters\DSA Working Directory`</span></span>

- `%windir%\Ntds\Temp.edb`
- `%windir%\Ntds\Edb.chk`

#### <a name="process-exclusions-for-ad-ds-and-ad-ds-related-support-files"></a><span data-ttu-id="90c5b-185">Exclusions de processus pour les fichiers de support liés aux services AD DS et AD DS</span><span class="sxs-lookup"><span data-stu-id="90c5b-185">Process exclusions for AD DS and AD DS-related support files</span></span>

- `%systemroot%\System32\ntfrs.exe`
- `%systemroot%\System32\lsass.exe`

### <a name="dhcp-server-exclusions"></a><span data-ttu-id="90c5b-186">Exclusions de serveur DHCP</span><span class="sxs-lookup"><span data-stu-id="90c5b-186">DHCP Server exclusions</span></span>

<span data-ttu-id="90c5b-187">Cette section répertorie les exclusions qui sont automatiquement livrées lorsque vous installez le rôle serveur DHCP.</span><span class="sxs-lookup"><span data-stu-id="90c5b-187">This section lists the exclusions that are delivered automatically when you install the DHCP Server role.</span></span> <span data-ttu-id="90c5b-188">Les emplacements de fichiers DHCP Server sont spécifiés par les paramètres *DatabasePath,* *DhcpLogFilePath* et *BackupDatabasePath* dans la clé de Registre `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\DHCPServer\Parameters`</span><span class="sxs-lookup"><span data-stu-id="90c5b-188">The DHCP Server file locations are specified by the *DatabasePath*, *DhcpLogFilePath*, and *BackupDatabasePath* parameters in the registry key `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\DHCPServer\Parameters`</span></span>

- `%systemroot%\System32\DHCP\*\*.mdb`
- `%systemroot%\System32\DHCP\*\*.pat`
- `%systemroot%\System32\DHCP\*\*.log`
- `%systemroot%\System32\DHCP\*\*.chk`
- `%systemroot%\System32\DHCP\*\*.edb`

### <a name="dns-server-exclusions"></a><span data-ttu-id="90c5b-189">Exclusions de serveur DNS</span><span class="sxs-lookup"><span data-stu-id="90c5b-189">DNS Server exclusions</span></span>

<span data-ttu-id="90c5b-190">Cette section répertorie les exclusions de fichiers et de dossiers, ainsi que les exclusions de processus qui sont automatiquement livrées lorsque vous installez le rôle serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="90c5b-190">This section lists the file and folder exclusions and the process exclusions that are delivered automatically when you install the DNS Server role.</span></span>

#### <a name="file-and-folder-exclusions-for-the-dns-server-role"></a><span data-ttu-id="90c5b-191">Exclusions de fichiers et de dossiers pour le rôle serveur DNS</span><span class="sxs-lookup"><span data-stu-id="90c5b-191">File and folder exclusions for the DNS Server role</span></span>

- `%systemroot%\System32\Dns\*\*.log`
- `%systemroot%\System32\Dns\*\*.dns`
- `%systemroot%\System32\Dns\*\*.scc`
- `%systemroot%\System32\Dns\*\BOOT`

#### <a name="process-exclusions-for-the-dns-server-role"></a><span data-ttu-id="90c5b-192">Exclusions de processus pour le rôle serveur DNS</span><span class="sxs-lookup"><span data-stu-id="90c5b-192">Process exclusions for the DNS Server role</span></span>

- `%systemroot%\System32\dns.exe`

### <a name="file-and-storage-services-exclusions"></a><span data-ttu-id="90c5b-193">Exclusions des services de fichiers et de stockage</span><span class="sxs-lookup"><span data-stu-id="90c5b-193">File and Storage Services exclusions</span></span>

<span data-ttu-id="90c5b-194">Cette section répertorie les exclusions de fichiers et de dossiers qui sont automatiquement livrées lorsque vous installez le rôle Services de fichiers et de stockage.</span><span class="sxs-lookup"><span data-stu-id="90c5b-194">This section lists the file and folder exclusions that are delivered automatically when you install the File and Storage Services role.</span></span> <span data-ttu-id="90c5b-195">Les exclusions répertoriées ci-dessous n'incluent pas d'exclusions pour le rôle de clustering.</span><span class="sxs-lookup"><span data-stu-id="90c5b-195">The exclusions listed below do not include exclusions for the Clustering role.</span></span>

- `%SystemDrive%\ClusterStorage`
- `%clusterserviceaccount%\Local Settings\Temp`
- `%SystemDrive%\mscs`

### <a name="print-server-exclusions"></a><span data-ttu-id="90c5b-196">Exclusions du serveur d'impression</span><span class="sxs-lookup"><span data-stu-id="90c5b-196">Print Server exclusions</span></span>

<span data-ttu-id="90c5b-197">Cette section répertorie les exclusions de types de fichiers, les exclusions de dossiers et les exclusions de processus qui sont automatiquement livrées lorsque vous installez le rôle serveur d'impression.</span><span class="sxs-lookup"><span data-stu-id="90c5b-197">This section lists the file type exclusions, folder exclusions, and the process exclusions that are delivered automatically when you install the Print Server role.</span></span>

#### <a name="file-type-exclusions"></a><span data-ttu-id="90c5b-198">Exclusions de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="90c5b-198">File type exclusions</span></span>

- `*.shd`
- `*.spl`

#### <a name="folder-exclusions"></a><span data-ttu-id="90c5b-199">Exclusions de dossiers</span><span class="sxs-lookup"><span data-stu-id="90c5b-199">Folder exclusions</span></span>

<span data-ttu-id="90c5b-200">Ce dossier est spécifié dans la clé de Registre `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Print\Printers\DefaultSpoolDirectory`</span><span class="sxs-lookup"><span data-stu-id="90c5b-200">This folder is specified in the registry key `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Print\Printers\DefaultSpoolDirectory`</span></span>

- `%system32%\spool\printers\*`

#### <a name="process-exclusions"></a><span data-ttu-id="90c5b-201">Exclusions de processus</span><span class="sxs-lookup"><span data-stu-id="90c5b-201">Process exclusions</span></span>

- `spoolsv.exe`

### <a name="web-server-exclusions"></a><span data-ttu-id="90c5b-202">Exclusions de serveur web</span><span class="sxs-lookup"><span data-stu-id="90c5b-202">Web Server exclusions</span></span>

<span data-ttu-id="90c5b-203">Cette section répertorie les exclusions de dossiers et les exclusions de processus qui sont automatiquement livrées lorsque vous installez le rôle serveur Web.</span><span class="sxs-lookup"><span data-stu-id="90c5b-203">This section lists the folder exclusions and the process exclusions that are delivered automatically when you install the Web Server role.</span></span>

#### <a name="folder-exclusions"></a><span data-ttu-id="90c5b-204">Exclusions de dossiers</span><span class="sxs-lookup"><span data-stu-id="90c5b-204">Folder exclusions</span></span>

- `%SystemRoot%\IIS Temporary Compressed Files`
- `%SystemDrive%\inetpub\temp\IIS Temporary Compressed Files`
- `%SystemDrive%\inetpub\temp\ASP Compiled Templates`
- `%systemDrive%\inetpub\logs`
- `%systemDrive%\inetpub\wwwroot`

#### <a name="process-exclusions"></a><span data-ttu-id="90c5b-205">Process exclusions</span><span class="sxs-lookup"><span data-stu-id="90c5b-205">Process exclusions</span></span>

- `%SystemRoot%\system32\inetsrv\w3wp.exe`
- `%SystemRoot%\SysWOW64\inetsrv\w3wp.exe`
- `%SystemDrive%\PHP5433\php-cgi.exe`

#### <a name="turning-off-scanning-of-files-in-the-sysvolsysvol-folder-or-the-sysvol_dfsrsysvol-folder"></a><span data-ttu-id="90c5b-206">La non-analyse des fichiers dans le dossier Sysvol\Sysvol ou le dossier SYSVOL_DFSR\Sysvol</span><span class="sxs-lookup"><span data-stu-id="90c5b-206">Turning off scanning of files in the Sysvol\Sysvol folder or the SYSVOL_DFSR\Sysvol folder</span></span>

<span data-ttu-id="90c5b-207">L'emplacement actuel du ou des dossiers et tous les sous-dossiers est la cible d'examen du système de fichiers de la racine du jeu `Sysvol\Sysvol` `SYSVOL_DFSR\Sysvol` de réplicas.</span><span class="sxs-lookup"><span data-stu-id="90c5b-207">The current location of the `Sysvol\Sysvol` or `SYSVOL_DFSR\Sysvol` folder and all the subfolders is the file system reparse target of the replica set root.</span></span> <span data-ttu-id="90c5b-208">Les `Sysvol\Sysvol` `SYSVOL_DFSR\Sysvol` dossiers et les dossiers utilisent les emplacements suivants par défaut :</span><span class="sxs-lookup"><span data-stu-id="90c5b-208">The `Sysvol\Sysvol` and `SYSVOL_DFSR\Sysvol` folders use the following locations by default:</span></span>

- `%systemroot%\Sysvol\Domain`
- `%systemroot%\Sysvol_DFSR\Domain`

<span data-ttu-id="90c5b-209">Le chemin d'accès au chemin d'accès actif est référencé par le partage NETLOGON et peut être déterminé par le nom de la valeur SysVol dans la `SYSVOL` sous-clé suivante : `HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Services\Netlogon\Parameters`</span><span class="sxs-lookup"><span data-stu-id="90c5b-209">The path to the currently active `SYSVOL` is referenced by the NETLOGON share and can be determined by the SysVol value name in the following subkey: `HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Services\Netlogon\Parameters`</span></span>

<span data-ttu-id="90c5b-210">Excluez les fichiers suivants de ce dossier et de tous ses sous-dossiers :</span><span class="sxs-lookup"><span data-stu-id="90c5b-210">Exclude the following files from this folder and all its subfolders:</span></span>

- `*.adm`
- `*.admx`
- `*.adml`
- `Registry.pol`
- `Registry.tmp`
- `*.aas`
- `*.inf`
- `Scripts.ini`
- `*.ins`
- `Oscfilter.ini`

### <a name="windows-server-update-services-exclusions"></a><span data-ttu-id="90c5b-211">Exclusions de Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="90c5b-211">Windows Server Update Services exclusions</span></span>

<span data-ttu-id="90c5b-212">Cette section répertorie les exclusions de dossiers qui sont automatiquement livrées lorsque vous installez le rôle Windows Server Update Services (WSUS).</span><span class="sxs-lookup"><span data-stu-id="90c5b-212">This section lists the folder exclusions that are delivered automatically when you install the Windows Server Update Services (WSUS) role.</span></span> <span data-ttu-id="90c5b-213">Le dossier WSUS est spécifié dans la clé de Registre `HKEY_LOCAL_MACHINE\Software\Microsoft\Update Services\Server\Setup`</span><span class="sxs-lookup"><span data-stu-id="90c5b-213">The WSUS folder is specified in the registry key `HKEY_LOCAL_MACHINE\Software\Microsoft\Update Services\Server\Setup`</span></span>

- `%systemroot%\WSUS\WSUSContent`
- `%systemroot%\WSUS\UpdateServicesDBFiles`
- `%systemroot%\SoftwareDistribution\Datastore`
- `%systemroot%\SoftwareDistribution\Download`

## <a name="see-also"></a><span data-ttu-id="90c5b-214">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90c5b-214">See also</span></span>

- [<span data-ttu-id="90c5b-215">Configurer et valider des exclusions pour les analyses de l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="90c5b-215">Configure and validate exclusions for Microsoft Defender Antivirus scans</span></span>](configure-exclusions-microsoft-defender-antivirus.md)
- [<span data-ttu-id="90c5b-216">Configurer et valider des exclusions en fonction du nom de fichier, de l'extension et de l'emplacement du dossier</span><span class="sxs-lookup"><span data-stu-id="90c5b-216">Configure and validate exclusions based on file name, extension, and folder location</span></span>](configure-extension-file-exclusions-microsoft-defender-antivirus.md)
- [<span data-ttu-id="90c5b-217">Configurer et valider des exclusions pour les fichiers ouverts par des processus</span><span class="sxs-lookup"><span data-stu-id="90c5b-217">Configure and validate exclusions for files opened by processes</span></span>](configure-process-opened-file-exclusions-microsoft-defender-antivirus.md)
- [<span data-ttu-id="90c5b-218">Erreurs courantes à éviter lors de la définition d'exclusions</span><span class="sxs-lookup"><span data-stu-id="90c5b-218">Common mistakes to avoid when defining exclusions</span></span>](common-exclusion-mistakes-microsoft-defender-antivirus.md)
- [<span data-ttu-id="90c5b-219">Personnaliser, lancer et passer en revue les résultats des analyses et des corrections de l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="90c5b-219">Customize, initiate, and review the results of Microsoft Defender Antivirus scans and remediation</span></span>](customize-run-review-remediate-scans-microsoft-defender-antivirus.md)
- [<span data-ttu-id="90c5b-220">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="90c5b-220">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)