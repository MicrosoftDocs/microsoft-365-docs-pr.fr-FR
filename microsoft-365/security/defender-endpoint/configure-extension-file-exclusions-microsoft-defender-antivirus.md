---
title: Configurer et valider des exclusions en fonction de l'extension, du nom ou de l'emplacement
description: Exclure des fichiers des analyses de l'Antivirus Microsoft Defender en fonction de leur extension de fichier, de leur nom de fichier ou de leur emplacement.
keywords: exclusions, fichiers, extension, type de fichier, nom de dossier, nom de fichier, analyses
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.localizationpriority: medium
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 74732c033ee1a8d45fe6f9a44bf641a3a9adbc13
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51690292"
---
# <a name="configure-and-validate-exclusions-based-on-file-extension-and-folder-location"></a><span data-ttu-id="bae70-104">Configurer et valider des exclusions en fonction de l'extension de fichier et de l'emplacement du dossier</span><span class="sxs-lookup"><span data-stu-id="bae70-104">Configure and validate exclusions based on file extension and folder location</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="bae70-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="bae70-105">**Applies to:**</span></span>

- [<span data-ttu-id="bae70-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="bae70-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

> [!IMPORTANT]
> <span data-ttu-id="bae70-107">Les exclusions de l'Antivirus Microsoft Defender ne s'appliquent pas aux autres fonctionnalités de Microsoft Defender pour les [](/microsoft-365/security/defender-endpoint/controlled-folders)points de terminaison, notamment la détection et la réponse des points de terminaison [(EDR),](/microsoft-365/security/defender-endpoint/overview-endpoint-detection-response)les règles de réduction de la surface d'attaque [(ASR)](/microsoft-365/security/defender-endpoint/attack-surface-reduction)et l'accès contrôlé aux dossiers.</span><span class="sxs-lookup"><span data-stu-id="bae70-107">Microsoft Defender Antivirus exclusions don't apply to other Microsoft Defender for Endpoint capabilities, including [endpoint detection and response (EDR)](/microsoft-365/security/defender-endpoint/overview-endpoint-detection-response), [attack surface reduction (ASR) rules](/microsoft-365/security/defender-endpoint/attack-surface-reduction), and [controlled folder access](/microsoft-365/security/defender-endpoint/controlled-folders).</span></span> <span data-ttu-id="bae70-108">Les fichiers que vous excluez à l'aide des méthodes décrites dans cet article peuvent toujours déclencher des alertes EDR et d'autres détections.</span><span class="sxs-lookup"><span data-stu-id="bae70-108">Files that you exclude using the methods described in this article can still trigger EDR alerts and other detections.</span></span> <span data-ttu-id="bae70-109">Pour exclure les fichiers à grande étendue, ajoutez-les aux indicateurs [personnalisés](/microsoft-365/security/defender-endpoint/manage-indicators)Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="bae70-109">To exclude files broadly, add them to the Microsoft Defender for Endpoint [custom indicators](/microsoft-365/security/defender-endpoint/manage-indicators).</span></span>

## <a name="exclusion-lists"></a><span data-ttu-id="bae70-110">Listes d'exclusions</span><span class="sxs-lookup"><span data-stu-id="bae70-110">Exclusion lists</span></span>

<span data-ttu-id="bae70-111">Vous pouvez exclure certains fichiers des analyses de l'Antivirus Microsoft Defender en modifiant des listes d'exclusions.</span><span class="sxs-lookup"><span data-stu-id="bae70-111">You can exclude certain files from Microsoft Defender Antivirus scans by modifying exclusion lists.</span></span> <span data-ttu-id="bae70-112">**En règle générale, il n'est pas nécessaire d'appliquer des exclusions.**</span><span class="sxs-lookup"><span data-stu-id="bae70-112">**Generally, you shouldn't need to apply exclusions**.</span></span> <span data-ttu-id="bae70-113">L'Antivirus Microsoft Defender inclut de nombreuses exclusions automatiques basées sur les comportements connus du système d'exploitation et les fichiers de gestion classiques, tels que ceux utilisés dans la gestion d'entreprise, la gestion de bases de données et d'autres scénarios et situations d'entreprise.</span><span class="sxs-lookup"><span data-stu-id="bae70-113">Microsoft Defender Antivirus includes many automatic exclusions based on known operating system behaviors and typical management files, such as those used in enterprise management, database management, and other enterprise scenarios and situations.</span></span>

> [!NOTE]
> <span data-ttu-id="bae70-114">Les exclusions s'appliquent également aux détections d'applications potentiellement indésirables (PUA).</span><span class="sxs-lookup"><span data-stu-id="bae70-114">Exclusions apply to Potentially Unwanted Apps (PUA) detections as well.</span></span>

> [!NOTE]
> <span data-ttu-id="bae70-115">Les exclusions automatiques s'appliquent uniquement à Windows Server 2016 et aux niveaux supérieurs.</span><span class="sxs-lookup"><span data-stu-id="bae70-115">Automatic exclusions apply only to Windows Server 2016 and above.</span></span> <span data-ttu-id="bae70-116">Ces exclusions ne sont pas visibles dans l'application Sécurité Windows et dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bae70-116">These exclusions are not visible in the Windows Security app and in PowerShell.</span></span>

<span data-ttu-id="bae70-117">Cet article explique comment configurer des listes d'exclusions pour les fichiers et dossiers.</span><span class="sxs-lookup"><span data-stu-id="bae70-117">This article  describes how to configure exclusion lists for the files and folders.</span></span> <span data-ttu-id="bae70-118">Voir [Recommandations pour définir des exclusions avant](configure-exclusions-microsoft-defender-antivirus.md#recommendations-for-defining-exclusions) de définir vos listes d'exclusions.</span><span class="sxs-lookup"><span data-stu-id="bae70-118">See [Recommendations for defining exclusions](configure-exclusions-microsoft-defender-antivirus.md#recommendations-for-defining-exclusions) before defining your exclusion lists.</span></span>

| <span data-ttu-id="bae70-119">Exclusion</span><span class="sxs-lookup"><span data-stu-id="bae70-119">Exclusion</span></span> | <span data-ttu-id="bae70-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="bae70-120">Examples</span></span> | <span data-ttu-id="bae70-121">Liste d'exclusions</span><span class="sxs-lookup"><span data-stu-id="bae70-121">Exclusion list</span></span> |
|:---|:---|:---|
|<span data-ttu-id="bae70-122">Tout fichier avec une extension spécifique</span><span class="sxs-lookup"><span data-stu-id="bae70-122">Any file with a specific extension</span></span> | <span data-ttu-id="bae70-123">Tous les fichiers avec l'extension spécifiée, n'importe où sur l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bae70-123">All files with the specified extension, anywhere on the machine.</span></span> <p> <span data-ttu-id="bae70-124">Syntaxe valide : `.test` et `test`</span><span class="sxs-lookup"><span data-stu-id="bae70-124">Valid syntax: `.test` and `test`</span></span>  | <span data-ttu-id="bae70-125">Exclusions d'extensions</span><span class="sxs-lookup"><span data-stu-id="bae70-125">Extension exclusions</span></span> |
|<span data-ttu-id="bae70-126">N'importe quel fichier sous un dossier spécifique</span><span class="sxs-lookup"><span data-stu-id="bae70-126">Any file under a specific folder</span></span> | <span data-ttu-id="bae70-127">Tous les fichiers sous le `c:\test\sample` dossier</span><span class="sxs-lookup"><span data-stu-id="bae70-127">All files under the `c:\test\sample` folder</span></span> | <span data-ttu-id="bae70-128">Exclusions de fichiers et de dossiers</span><span class="sxs-lookup"><span data-stu-id="bae70-128">File and folder exclusions</span></span> |
| <span data-ttu-id="bae70-129">Un fichier spécifique dans un dossier spécifique</span><span class="sxs-lookup"><span data-stu-id="bae70-129">A specific file in a specific folder</span></span> | <span data-ttu-id="bae70-130">Fichier `c:\sample\sample.test` uniquement</span><span class="sxs-lookup"><span data-stu-id="bae70-130">The file `c:\sample\sample.test` only</span></span> | <span data-ttu-id="bae70-131">Exclusions de fichiers et de dossiers</span><span class="sxs-lookup"><span data-stu-id="bae70-131">File and folder exclusions</span></span> |
| <span data-ttu-id="bae70-132">Un processus spécifique</span><span class="sxs-lookup"><span data-stu-id="bae70-132">A specific process</span></span> | <span data-ttu-id="bae70-133">Fichier exécutable `c:\test\process.exe`</span><span class="sxs-lookup"><span data-stu-id="bae70-133">The executable file `c:\test\process.exe`</span></span> | <span data-ttu-id="bae70-134">Exclusions de fichiers et de dossiers</span><span class="sxs-lookup"><span data-stu-id="bae70-134">File and folder exclusions</span></span> |

<span data-ttu-id="bae70-135">Les listes d'exclusions ont les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="bae70-135">Exclusion lists have the following characteristics:</span></span>

- <span data-ttu-id="bae70-136">Les exclusions de dossiers s'appliquent à tous les fichiers et dossiers de ce dossier, sauf si le sous-dossier est un point d'parage.</span><span class="sxs-lookup"><span data-stu-id="bae70-136">Folder exclusions apply to all files and folders under that folder, unless the subfolder is a reparse point.</span></span> <span data-ttu-id="bae70-137">Les sous-ensembles de points d'parse doivent être exclus séparément.</span><span class="sxs-lookup"><span data-stu-id="bae70-137">Reparse point subfolders must be excluded separately.</span></span>
- <span data-ttu-id="bae70-138">Les extensions de fichier s'appliquent à n'importe quel nom de fichier avec l'extension définie si aucun chemin d'accès ou dossier n'est défini.</span><span class="sxs-lookup"><span data-stu-id="bae70-138">File extensions apply to any file name with the defined extension if a path or folder is not defined.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="bae70-139">L'utilisation de caractères génériques tels que l'astérisque ( ) modifie l'interprétation des règles \* d'exclusion.</span><span class="sxs-lookup"><span data-stu-id="bae70-139">Using wildcards such as the asterisk (\*) will alter how the exclusion rules are interpreted.</span></span> <span data-ttu-id="bae70-140">Pour plus d'informations sur le fonctionnement des [caractères génériques,](#use-wildcards-in-the-file-name-and-folder-path-or-extension-exclusion-lists) voir la section Utiliser des caractères génériques dans la section des listes d'exclusions de nom de fichier et de dossier ou d'extension.</span><span class="sxs-lookup"><span data-stu-id="bae70-140">See the [Use wildcards in the file name and folder path or extension exclusion lists](#use-wildcards-in-the-file-name-and-folder-path-or-extension-exclusion-lists) section for important information about how wildcards work.</span></span>
> - <span data-ttu-id="bae70-141">Vous ne pouvez pas exclure les lecteurs réseau mappés.</span><span class="sxs-lookup"><span data-stu-id="bae70-141">You cannot exclude mapped network drives.</span></span> <span data-ttu-id="bae70-142">Vous devez spécifier le chemin d'accès réseau réel.</span><span class="sxs-lookup"><span data-stu-id="bae70-142">You must specify the actual network path.</span></span>
> - <span data-ttu-id="bae70-143">Les dossiers qui sont des points d'analyse créés après le démarrage du service Antivirus Microsoft Defender et qui ont été ajoutés à la liste d'exclusions ne seront pas inclus.</span><span class="sxs-lookup"><span data-stu-id="bae70-143">Folders that are reparse points that are created after the Microsoft Defender Antivirus service starts and that have been added to the exclusion list will not be included.</span></span> <span data-ttu-id="bae70-144">Vous devez redémarrer le service (en redémarré Windows) pour que les nouveaux points d'parage soient reconnus comme cibles d'exclusion valides.</span><span class="sxs-lookup"><span data-stu-id="bae70-144">You must restart the service (by restarting Windows) for new reparse points to be recognized as a valid exclusion target.</span></span>

<span data-ttu-id="bae70-145">Pour exclure les fichiers ouverts par un processus spécifique, voir Configurer et valider les exclusions pour les fichiers [ouverts par des processus.](configure-process-opened-file-exclusions-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="bae70-145">To exclude files opened by a specific process, see [Configure and validate exclusions for files opened by processes](configure-process-opened-file-exclusions-microsoft-defender-antivirus.md).</span></span>

<span data-ttu-id="bae70-146">Les exclusions s'appliquent [aux analyses programmées,](scheduled-catch-up-scans-microsoft-defender-antivirus.md)aux analyses à la demande [et](run-scan-microsoft-defender-antivirus.md)à la protection en [temps réel.](configure-real-time-protection-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="bae70-146">The exclusions apply to [scheduled scans](scheduled-catch-up-scans-microsoft-defender-antivirus.md), [on-demand scans](run-scan-microsoft-defender-antivirus.md), and [real-time protection](configure-real-time-protection-microsoft-defender-antivirus.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bae70-147">Les modifications apportées aux listes d'exclusions avec la stratégie de **groupe** s'afficheront dans les listes de l'application [Sécurité Windows.](microsoft-defender-security-center-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="bae70-147">Exclusion list changes made with Group Policy **will show** in the lists in the [Windows Security app](microsoft-defender-security-center-antivirus.md).</span></span>
> <span data-ttu-id="bae70-148">Les modifications apportées dans l'application Sécurité Windows **ne s'afficheront pas** dans les listes de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="bae70-148">Changes made in the Windows Security app **will not show** in the Group Policy lists.</span></span>

<span data-ttu-id="bae70-149">Par défaut, les modifications locales apportées aux listes (par les utilisateurs ayant des privilèges d'administrateur, y compris les modifications apportées avec PowerShell et WMI) seront fusionnées avec les listes telles que définies (et déployées) par la stratégie de groupe, Configuration Manager ou Intune.</span><span class="sxs-lookup"><span data-stu-id="bae70-149">By default, local changes made to the lists (by users with administrator privileges, including changes made with PowerShell and WMI) will be merged with the lists as defined (and deployed) by Group Policy, Configuration Manager, or Intune.</span></span> <span data-ttu-id="bae70-150">Les listes de stratégie de groupe prévalent en cas de conflit.</span><span class="sxs-lookup"><span data-stu-id="bae70-150">The Group Policy lists take precedence when there are conflicts.</span></span>

<span data-ttu-id="bae70-151">Vous pouvez [configurer la façon dont les listes d'exclusions définies](configure-local-policy-overrides-microsoft-defender-antivirus.md#merge-lists) localement et globalement sont fusionnées pour permettre aux modifications locales de remplacer les paramètres de déploiement géré.</span><span class="sxs-lookup"><span data-stu-id="bae70-151">You can [configure how locally and globally defined exclusions lists are merged](configure-local-policy-overrides-microsoft-defender-antivirus.md#merge-lists) to allow local changes to override managed deployment settings.</span></span>

## <a name="configure-the-list-of-exclusions-based-on-folder-name-or-file-extension"></a><span data-ttu-id="bae70-152">Configurer la liste des exclusions en fonction du nom du dossier ou de l'extension de fichier</span><span class="sxs-lookup"><span data-stu-id="bae70-152">Configure the list of exclusions based on folder name or file extension</span></span>

### <a name="use-intune-to-configure-file-name-folder-or-file-extension-exclusions"></a><span data-ttu-id="bae70-153">Utiliser Intune pour configurer des exclusions de nom de fichier, de dossier ou d'extension de fichier</span><span class="sxs-lookup"><span data-stu-id="bae70-153">Use Intune to configure file name, folder, or file extension exclusions</span></span>

<span data-ttu-id="bae70-154">Consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="bae70-154">See the following articles:</span></span>
- [<span data-ttu-id="bae70-155">Configurer les paramètres de restriction d'appareil dans Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="bae70-155">Configure device restriction settings in Microsoft Intune</span></span>](/intune/device-restrictions-configure)
- [<span data-ttu-id="bae70-156">Paramètres de restriction de l'appareil de l'Antivirus Microsoft Defender pour Windows 10 dans Intune</span><span class="sxs-lookup"><span data-stu-id="bae70-156">Microsoft Defender Antivirus device restriction settings for Windows 10 in Intune</span></span>](/intune/device-restrictions-windows-10#microsoft-defender-antivirus)

### <a name="use-configuration-manager-to-configure-file-name-folder-or-file-extension-exclusions"></a><span data-ttu-id="bae70-157">Utiliser Configuration Manager pour configurer des exclusions de nom de fichier, de dossier ou d'extension de fichier</span><span class="sxs-lookup"><span data-stu-id="bae70-157">Use Configuration Manager to configure file name, folder, or file extension exclusions</span></span>

<span data-ttu-id="bae70-158">Découvrez [comment créer et déployer des stratégies anti-programme](/configmgr/protect/deploy-use/endpoint-antimalware-policies#exclusion-settings) malveillant : paramètres d'exclusion pour plus d'informations sur la configuration de Microsoft Endpoint Manager (branche actuelle).</span><span class="sxs-lookup"><span data-stu-id="bae70-158">See [How to create and deploy antimalware policies: Exclusion settings](/configmgr/protect/deploy-use/endpoint-antimalware-policies#exclusion-settings) for details on configuring Microsoft Endpoint Manager (current branch).</span></span>

### <a name="use-group-policy-to-configure-folder-or-file-extension-exclusions"></a><span data-ttu-id="bae70-159">Utiliser une stratégie de groupe pour configurer des exclusions de dossiers ou d'extensions de fichiers</span><span class="sxs-lookup"><span data-stu-id="bae70-159">Use Group Policy to configure folder or file extension exclusions</span></span>

>[!NOTE]
><span data-ttu-id="bae70-160">Si vous spécifiez un chemin d'accès complet à un fichier, seul ce fichier est exclu.</span><span class="sxs-lookup"><span data-stu-id="bae70-160">If you specify a fully qualified path to a file, then only that file is excluded.</span></span> <span data-ttu-id="bae70-161">Si un dossier est défini dans l'exclusion, tous les fichiers et sous-répertoires de ce dossier sont exclus.</span><span class="sxs-lookup"><span data-stu-id="bae70-161">If a folder is defined in the exclusion, then all files and subdirectories under that folder are excluded.</span></span>

1. <span data-ttu-id="bae70-162">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="bae70-162">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="bae70-163">Dans **l'Éditeur de gestion des stratégies de** groupe, sélectionnez **Configuration** ordinateur et **sélectionnez Modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="bae70-163">In the **Group Policy Management Editor** go to **Computer configuration** and select **Administrative templates**.</span></span>

3. <span data-ttu-id="bae70-164">Développez l'arborescence **des composants Windows**  >  **Exclusions de l'Antivirus Microsoft Defender.**  >  </span><span class="sxs-lookup"><span data-stu-id="bae70-164">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Exclusions**.</span></span>

4. <span data-ttu-id="bae70-165">Ouvrez le **paramètre Exclusions de** chemin d'accès pour modification et ajoutez vos exclusions.</span><span class="sxs-lookup"><span data-stu-id="bae70-165">Open the **Path Exclusions** setting for editing, and add your exclusions.</span></span>

    1. <span data-ttu-id="bae70-166">Définissez l'option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="bae70-166">Set the option to **Enabled**.</span></span>
    1. <span data-ttu-id="bae70-167">Sous la section **Options,** cliquez sur **Afficher.**</span><span class="sxs-lookup"><span data-stu-id="bae70-167">Under the **Options** section, click **Show**.</span></span>
    1. <span data-ttu-id="bae70-168">Spécifiez chaque dossier sur sa propre ligne sous la **colonne Nom de** la valeur.</span><span class="sxs-lookup"><span data-stu-id="bae70-168">Specify each folder on its own line under the **Value name** column.</span></span>
    1. <span data-ttu-id="bae70-169">Si vous spécifiez un fichier, veillez à entrer un chemin d'accès complet au fichier, y compris la lettre de lecteur, le chemin d'accès au dossier, le nom de fichier et l'extension.</span><span class="sxs-lookup"><span data-stu-id="bae70-169">If you are specifying a file, ensure that you enter a fully qualified path to the file, including the drive letter, folder path, file name, and extension.</span></span> <span data-ttu-id="bae70-170">Entrez **0 dans** la **colonne** Valeur.</span><span class="sxs-lookup"><span data-stu-id="bae70-170">Enter **0** in the **Value** column.</span></span>

5. <span data-ttu-id="bae70-171">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="bae70-171">Choose **OK**.</span></span>

6. <span data-ttu-id="bae70-172">Ouvrez **le paramètre Exclusions des extensions** pour la modification et ajoutez vos exclusions.</span><span class="sxs-lookup"><span data-stu-id="bae70-172">Open the **Extension Exclusions** setting for editing and add your exclusions.</span></span>

    1. <span data-ttu-id="bae70-173">Définissez l'option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="bae70-173">Set the option to **Enabled**.</span></span>
    1. <span data-ttu-id="bae70-174">Sous la section **Options,** sélectionnez **Afficher.**</span><span class="sxs-lookup"><span data-stu-id="bae70-174">Under the **Options** section, select **Show**.</span></span>
    1. <span data-ttu-id="bae70-175">Entrez chaque extension de fichier sur sa propre ligne sous la **colonne Nom de** la valeur.</span><span class="sxs-lookup"><span data-stu-id="bae70-175">Enter each file extension on its own line under the **Value name** column.</span></span>  <span data-ttu-id="bae70-176">Entrez **0 dans** la **colonne** Valeur.</span><span class="sxs-lookup"><span data-stu-id="bae70-176">Enter **0** in the **Value** column.</span></span>

7. <span data-ttu-id="bae70-177">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="bae70-177">Choose **OK**.</span></span>

<a id="ps"></a>

### <a name="use-powershell-cmdlets-to-configure-file-name-folder-or-file-extension-exclusions"></a><span data-ttu-id="bae70-178">Utiliser les cmdlets PowerShell pour configurer des exclusions de nom de fichier, de dossier ou d'extension de fichier</span><span class="sxs-lookup"><span data-stu-id="bae70-178">Use PowerShell cmdlets to configure file name, folder, or file extension exclusions</span></span>

<span data-ttu-id="bae70-179">L'utilisation de PowerShell pour ajouter ou supprimer des exclusions pour des fichiers basés sur l'extension, l'emplacement ou le nom de fichier nécessite l'utilisation d'une combinaison de trois cmdlets et du paramètre de liste d'exclusions approprié.</span><span class="sxs-lookup"><span data-stu-id="bae70-179">Using PowerShell to add or remove exclusions for files based on the extension, location, or file name requires using a combination of three cmdlets and the appropriate exclusion list parameter.</span></span> <span data-ttu-id="bae70-180">Les cmdlets sont toutes dans le [module Defender.](/powershell/module/defender/)</span><span class="sxs-lookup"><span data-stu-id="bae70-180">The cmdlets are all in the [Defender module](/powershell/module/defender/).</span></span>

<span data-ttu-id="bae70-181">Le format des cmdlets est le suivant :</span><span class="sxs-lookup"><span data-stu-id="bae70-181">The format for the cmdlets is as follows:</span></span>

```PowerShell
<cmdlet> -<exclusion list> "<item>"
```

<span data-ttu-id="bae70-182">Les listes suivantes sont autorisées en tant que `<cmdlet>` :</span><span class="sxs-lookup"><span data-stu-id="bae70-182">The following are allowed as the `<cmdlet>`:</span></span>

| <span data-ttu-id="bae70-183">Action de configuration</span><span class="sxs-lookup"><span data-stu-id="bae70-183">Configuration action</span></span> | <span data-ttu-id="bae70-184">Cmdlet PowerShell</span><span class="sxs-lookup"><span data-stu-id="bae70-184">PowerShell cmdlet</span></span> |
|:---|:---|
|<span data-ttu-id="bae70-185">Créer ou overwrite la liste</span><span class="sxs-lookup"><span data-stu-id="bae70-185">Create or overwrite the list</span></span> | `Set-MpPreference` |
|<span data-ttu-id="bae70-186">Ajouter à la liste</span><span class="sxs-lookup"><span data-stu-id="bae70-186">Add to the list</span></span> | `Add-MpPreference` |
|<span data-ttu-id="bae70-187">Supprimer l'élément de la liste</span><span class="sxs-lookup"><span data-stu-id="bae70-187">Remove item from the list</span></span> | `Remove-MpPreference` |

<span data-ttu-id="bae70-188">Les listes suivantes sont autorisées en tant que `<exclusion list>` :</span><span class="sxs-lookup"><span data-stu-id="bae70-188">The following are allowed as the `<exclusion list>`:</span></span>

| <span data-ttu-id="bae70-189">Type d'exclusion</span><span class="sxs-lookup"><span data-stu-id="bae70-189">Exclusion type</span></span> | <span data-ttu-id="bae70-190">Paramètre PowerShell</span><span class="sxs-lookup"><span data-stu-id="bae70-190">PowerShell parameter</span></span> |
|:---|:---|
| <span data-ttu-id="bae70-191">Tous les fichiers avec une extension de fichier spécifiée</span><span class="sxs-lookup"><span data-stu-id="bae70-191">All files with a specified file extension</span></span> | `-ExclusionExtension` |
| <span data-ttu-id="bae70-192">Tous les fichiers sous un dossier (y compris les fichiers dans les sous-répertoires) ou un fichier spécifique</span><span class="sxs-lookup"><span data-stu-id="bae70-192">All files under a folder (including files in subdirectories), or a specific file</span></span> | `-ExclusionPath` |

> [!IMPORTANT]
> <span data-ttu-id="bae70-193">Si vous avez créé une liste, avec ou , en utilisant à nouveau la `Set-MpPreference` `Add-MpPreference` `Set-MpPreference` cmdlet, la liste existante est réécrite.</span><span class="sxs-lookup"><span data-stu-id="bae70-193">If you have created a list, either with `Set-MpPreference` or `Add-MpPreference`, using the `Set-MpPreference` cmdlet again will overwrite the existing list.</span></span>

<span data-ttu-id="bae70-194">Par exemple, l'extrait de code suivant permet aux analyses de l'Antivirus Microsoft Defender d'exclure tout fichier avec `.test` l'extension de fichier :</span><span class="sxs-lookup"><span data-stu-id="bae70-194">For example, the following code snippet would cause Microsoft Defender Antivirus scans to exclude any file with the `.test` file extension:</span></span>

```PowerShell
Add-MpPreference -ExclusionExtension ".test"
```

<span data-ttu-id="bae70-195">Pour plus d'informations, voir [Utiliser les cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter l'Antivirus Microsoft Defender et [les cmdlets Defender.](/powershell/module/defender/)</span><span class="sxs-lookup"><span data-stu-id="bae70-195">For more information, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/).</span></span>

### <a name="use-windows-management-instruction-wmi-to-configure-file-name-folder-or-file-extension-exclusions"></a><span data-ttu-id="bae70-196">Utiliser Windows Management Instruction (WMI) pour configurer les exclusions de nom de fichier, de dossier ou d'extension de fichier</span><span class="sxs-lookup"><span data-stu-id="bae70-196">Use Windows Management Instruction (WMI) to configure file name, folder, or file extension exclusions</span></span>

<span data-ttu-id="bae70-197">Utilisez les [ **méthodes Set,** **Add** et **Remove** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="bae70-197">Use the [**Set**, **Add**, and **Remove** methods of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
ExclusionExtension
ExclusionPath
```

<span data-ttu-id="bae70-198">L'utilisation **de Set**, **Add** et **Remove** est analogue à leurs équivalents dans PowerShell : , `Set-MpPreference` et `Add-MpPreference` `Remove-MpPreference` .</span><span class="sxs-lookup"><span data-stu-id="bae70-198">The use of **Set**, **Add**, and **Remove** is analogous to their counterparts in PowerShell: `Set-MpPreference`, `Add-MpPreference`, and `Remove-MpPreference`.</span></span>

<span data-ttu-id="bae70-199">Pour plus d'informations, [voir Windows Defender API WMIv2.](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="bae70-199">For more information, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span></span>

<a id="man-tools"></a>

### <a name="use-the-windows-security-app-to-configure-file-name-folder-or-file-extension-exclusions"></a><span data-ttu-id="bae70-200">Utiliser l'application Sécurité Windows pour configurer les exclusions de nom de fichier, de dossier ou d'extension de fichier</span><span class="sxs-lookup"><span data-stu-id="bae70-200">Use the Windows Security app to configure file name, folder, or file extension exclusions</span></span>

<span data-ttu-id="bae70-201">Voir [Ajouter des exclusions dans l'application Sécurité Windows](microsoft-defender-security-center-antivirus.md) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="bae70-201">See [Add exclusions in the Windows Security app](microsoft-defender-security-center-antivirus.md) for instructions.</span></span>

<a id="wildcards"></a>

## <a name="use-wildcards-in-the-file-name-and-folder-path-or-extension-exclusion-lists"></a><span data-ttu-id="bae70-202">Utiliser des caractères génériques dans les listes d'exclusion de nom de fichier et de dossier ou d'extension</span><span class="sxs-lookup"><span data-stu-id="bae70-202">Use wildcards in the file name and folder path or extension exclusion lists</span></span>

<span data-ttu-id="bae70-203">Vous pouvez utiliser l'astérisque, le point d'interrogation ou les variables d'environnement `*` `?` (par exemple) comme caractères génériques lors de la définition d'éléments dans la liste d'exclusion du nom de fichier ou du chemin d'accès du `%ALLUSERSPROFILE%` dossier.</span><span class="sxs-lookup"><span data-stu-id="bae70-203">You can use the asterisk `*`, question mark `?`, or environment variables (such as `%ALLUSERSPROFILE%`) as wildcards when defining items in the file name or folder path exclusion list.</span></span> <span data-ttu-id="bae70-204">La façon dont ces caractères génériques sont interprétés diffère de leur utilisation habituelle dans d'autres applications et langues.</span><span class="sxs-lookup"><span data-stu-id="bae70-204">The way in which these wildcards are interpreted differs from their usual usage in other apps and languages.</span></span> <span data-ttu-id="bae70-205">Veillez à lire cette section pour comprendre leurs limitations spécifiques.</span><span class="sxs-lookup"><span data-stu-id="bae70-205">Make sure to read this section to understand their specific limitations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bae70-206">Il existe des limitations clés et des scénarios d'utilisation pour ces caractères génériques :</span><span class="sxs-lookup"><span data-stu-id="bae70-206">There are key limitations and usage scenarios for these wildcards:</span></span>
> - <span data-ttu-id="bae70-207">L'utilisation des variables d'environnement est limitée aux variables de l'ordinateur et à celles applicables aux processus en cours d'exécution en tant que compte NT AUTHORITY\SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="bae70-207">Environment variable usage is limited to machine variables and those applicable to processes running as an NT AUTHORITY\SYSTEM account.</span></span>
> - <span data-ttu-id="bae70-208">Vous ne pouvez pas utiliser de caractère générique à la place d'une lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="bae70-208">You cannot use a wildcard in place of a drive letter.</span></span>
> - <span data-ttu-id="bae70-209">Un astérisque dans `*` une exclusion de dossier est en place pour un dossier unique.</span><span class="sxs-lookup"><span data-stu-id="bae70-209">An asterisk `*` in a folder exclusion stands in place for a single folder.</span></span> <span data-ttu-id="bae70-210">Utilisez plusieurs instances pour `\*\` indiquer plusieurs dossiers imbrifiés avec des noms non spécifiés.</span><span class="sxs-lookup"><span data-stu-id="bae70-210">Use multiple instances of `\*\` to indicate multiple nested folders with unspecified names.</span></span>

<span data-ttu-id="bae70-211">Le tableau suivant décrit comment les caractères génériques peuvent être utilisés et fournit quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="bae70-211">The following table describes how the wildcards can be used and provides some examples.</span></span>


|<span data-ttu-id="bae70-212">Caractère générique</span><span class="sxs-lookup"><span data-stu-id="bae70-212">Wildcard</span></span>  |<span data-ttu-id="bae70-213">Exemples</span><span class="sxs-lookup"><span data-stu-id="bae70-213">Examples</span></span>  |
|:---------|:---------|
|<span data-ttu-id="bae70-214">`*` (astérisque)</span><span class="sxs-lookup"><span data-stu-id="bae70-214">`*` (asterisk)</span></span> <p> <span data-ttu-id="bae70-215">Dans **les inclusions** de nom de fichier et d'extension de fichier, l'astérisque remplace un nombre quelconque de caractères et s'applique uniquement aux fichiers du dernier dossier défini dans l'argument.</span><span class="sxs-lookup"><span data-stu-id="bae70-215">In **file name and file extension inclusions**, the asterisk replaces any number of characters, and only applies to files in the last folder defined in the argument.</span></span> <p> <span data-ttu-id="bae70-216">Dans **les exclusions de dossiers,** l'astérisque remplace un dossier unique.</span><span class="sxs-lookup"><span data-stu-id="bae70-216">In **folder exclusions**, the asterisk replaces a single folder.</span></span> <span data-ttu-id="bae70-217">Utilisez plusieurs `*` dossiers avec barres obliques `\` pour indiquer plusieurs dossiers imbrmbrés.</span><span class="sxs-lookup"><span data-stu-id="bae70-217">Use multiple `*` with folder slashes `\` to indicate multiple nested folders.</span></span> <span data-ttu-id="bae70-218">Après la correspondance du nombre de dossiers avec caractères wild carded et nommés, tous les sous-dossiers sont également inclus.</span><span class="sxs-lookup"><span data-stu-id="bae70-218">After matching the number of wild carded and named folders, all subfolders are also included.</span></span>   | <span data-ttu-id="bae70-219">`C:\MyData\*.txt` includes `C:\MyData\notes.txt`</span><span class="sxs-lookup"><span data-stu-id="bae70-219">`C:\MyData\*.txt` includes `C:\MyData\notes.txt`</span></span> <p> <span data-ttu-id="bae70-220">`C:\somepath\*\Data` inclut n'importe quel fichier et ses `C:\somepath\Archives\Data` sous-dossiers, `C:\somepath\Authorized\Data` ainsi que ses sous-dossiers</span><span class="sxs-lookup"><span data-stu-id="bae70-220">`C:\somepath\*\Data` includes any file in `C:\somepath\Archives\Data` and its subfolders, and `C:\somepath\Authorized\Data` and its subfolders</span></span> <p> <span data-ttu-id="bae70-221">`C:\Serv\*\*\Backup` inclut n'importe quel fichier et ses `C:\Serv\Primary\Denied\Backup` sous-dossiers `C:\Serv\Secondary\Allowed\Backup` et ses sous-dossiers</span><span class="sxs-lookup"><span data-stu-id="bae70-221">`C:\Serv\*\*\Backup` includes any file in `C:\Serv\Primary\Denied\Backup` and its subfolders and `C:\Serv\Secondary\Allowed\Backup` and its subfolders</span></span>     |
|<span data-ttu-id="bae70-222">`?` (point d'interrogation)</span><span class="sxs-lookup"><span data-stu-id="bae70-222">`?` (question mark)</span></span>  <p> <span data-ttu-id="bae70-223">Dans **les inclusions de** nom de fichier et d'extension de fichier, le point d'interrogation remplace un seul caractère et s'applique uniquement aux fichiers du dernier dossier défini dans l'argument.</span><span class="sxs-lookup"><span data-stu-id="bae70-223">In **file name and file extension inclusions**, the question mark replaces a single character, and only applies to files in the last folder defined in the argument.</span></span> <p> <span data-ttu-id="bae70-224">Dans **les exclusions de dossiers,** le point d'interrogation remplace un seul caractère dans un nom de dossier.</span><span class="sxs-lookup"><span data-stu-id="bae70-224">In **folder exclusions**, the question mark replaces a single character in a folder name.</span></span> <span data-ttu-id="bae70-225">Après la correspondance du nombre de dossiers avec caractères wild carded et nommés, tous les sous-dossiers sont également inclus.</span><span class="sxs-lookup"><span data-stu-id="bae70-225">After matching the number of wild carded and named folders, all subfolders are also included.</span></span>   |<span data-ttu-id="bae70-226">`C:\MyData\my?.zip` includes `C:\MyData\my1.zip`</span><span class="sxs-lookup"><span data-stu-id="bae70-226">`C:\MyData\my?.zip` includes `C:\MyData\my1.zip`</span></span> <p> <span data-ttu-id="bae70-227">`C:\somepath\?\Data` inclut `C:\somepath\P\Data` n'importe quel fichier dans et ses sous-dossiers</span><span class="sxs-lookup"><span data-stu-id="bae70-227">`C:\somepath\?\Data` includes any file in `C:\somepath\P\Data` and its subfolders</span></span>  <p> <span data-ttu-id="bae70-228">`C:\somepath\test0?\Data` inclut n'importe `C:\somepath\test01\Data` quel fichier et ses sous-dossiers</span><span class="sxs-lookup"><span data-stu-id="bae70-228">`C:\somepath\test0?\Data` would include any file in `C:\somepath\test01\Data` and its subfolders</span></span>          |
|<span data-ttu-id="bae70-229">Variables d'environnement</span><span class="sxs-lookup"><span data-stu-id="bae70-229">Environment variables</span></span> <p> <span data-ttu-id="bae70-230">La variable définie est remplie en tant que chemin d'accès lorsque l'exclusion est évaluée.</span><span class="sxs-lookup"><span data-stu-id="bae70-230">The defined variable is populated as a path when the exclusion is evaluated.</span></span>          |<span data-ttu-id="bae70-231">`%ALLUSERSPROFILE%\CustomLogFiles` inclut `C:\ProgramData\CustomLogFiles\Folder1\file1.txt`</span><span class="sxs-lookup"><span data-stu-id="bae70-231">`%ALLUSERSPROFILE%\CustomLogFiles` would include `C:\ProgramData\CustomLogFiles\Folder1\file1.txt`</span></span>         |
        

> [!IMPORTANT]
> <span data-ttu-id="bae70-232">Si vous mélangez un argument d'exclusion de fichier avec un argument d'exclusion de dossier, les règles s'arrêtent à la correspondance de l'argument de fichier dans le dossier de correspondance et ne recherchent aucune correspondance de fichier dans les sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="bae70-232">If you mix a file exclusion argument with a folder exclusion argument, the rules will stop at the file argument match in the matched folder, and will not look for file matches in any subfolders.</span></span>
> <span data-ttu-id="bae70-233">Par exemple, vous pouvez exclure tous les fichiers qui commencent par « date » dans les dossiers et à l'aide de `c:\data\final\marked` `c:\data\review\marked` l'argument de règle `c:\data\*\marked\date*` .</span><span class="sxs-lookup"><span data-stu-id="bae70-233">For example, you can exclude all files that start with "date" in the folders `c:\data\final\marked` and `c:\data\review\marked` by using the rule argument `c:\data\*\marked\date*`.</span></span>
> <span data-ttu-id="bae70-234">Toutefois, cet argument ne correspond à aucun fichier des sous-dossiers sous `c:\data\final\marked` ou `c:\data\review\marked` .</span><span class="sxs-lookup"><span data-stu-id="bae70-234">This argument, however, will not match any files in subfolders under `c:\data\final\marked` or `c:\data\review\marked`.</span></span>

<a id="review"></a>

### <a name="system-environment-variables"></a><span data-ttu-id="bae70-235">Variables d'environnement système</span><span class="sxs-lookup"><span data-stu-id="bae70-235">System environment variables</span></span>

<span data-ttu-id="bae70-236">Le tableau suivant répertorie et décrit les variables d'environnement de compte système.</span><span class="sxs-lookup"><span data-stu-id="bae70-236">The following table lists and describes the system account environment variables.</span></span> 

| <span data-ttu-id="bae70-237">Cette variable d'environnement système...</span><span class="sxs-lookup"><span data-stu-id="bae70-237">This system environment variable...</span></span> | <span data-ttu-id="bae70-238">Redirige vers cette</span><span class="sxs-lookup"><span data-stu-id="bae70-238">Redirects to this</span></span> |
|:--|:--|
| `%APPDATA%`| `C:\Users\UserName.DomainName\AppData\Roaming` |
| `%APPDATA%\Microsoft\Internet Explorer\Quick Launch` | `C:\Windows\System32\config\systemprofile\AppData\Roaming\Microsoft\Internet Explorer\Quick Launch` |
| `%APPDATA%\Microsoft\Windows\Start Menu` | `C:\Windows\System32\config\systemprofile\AppData\Roaming\Microsoft\Windows\Start Menu` |
| `%APPDATA%\Microsoft\Windows\Start Menu\Programs` | `C:\Windows\System32\config\systemprofile\AppData\Roaming\Microsoft\Windows\Start Menu\Programs` |
| `%LOCALAPPDATA%` | `C:\Windows\System32\config\systemprofile\AppData\Local` |
| `%ProgramData%` | `C:\ProgramData` |
| `%ProgramFiles%` | `C:\Program Files` |
| `%ProgramFiles%\Common Files` | `C:\Program Files\Common Files` |
| `%ProgramFiles%\Windows Sidebar\Gadgets` | `C:\Program Files\Windows Sidebar\Gadgets` |
| `%ProgramFiles%\Common Files` | `C:\Program Files\Common Files` |
| `%ProgramFiles(x86)%` | `C:\Program Files (x86)` |
| `%ProgramFiles(x86)%\Common Files` | `C:\Program Files (x86)\Common Files` |
| `%SystemDrive%` | `C:` |
| `%SystemDrive%\Program Files` | `C:\Program Files` |
| `%SystemDrive%\Program Files (x86)` | `C:\Program Files (x86)` |
| `%SystemDrive%\Users` | `C:\Users` |
| `%SystemDrive%\Users\Public` | `C:\Users\Public` |
| `%SystemRoot%` | `C:\Windows` |
| `%windir%` | `C:\Windows` |
| `%windir%\Fonts` | `C:\Windows\Fonts` |
| `%windir%\Resources` | `C:\Windows\Resources` |
| `%windir%\resources\0409` | `C:\Windows\resources\0409` |
| `%windir%\system32` | `C:\Windows\System32` |
| `%ALLUSERSPROFILE%` | `C:\ProgramData` |
| `%ALLUSERSPROFILE%\Application Data` | `C:\ProgramData\Application Data` |
| `%ALLUSERSPROFILE%\Documents` | `C:\ProgramData\Documents` |
| `%ALLUSERSPROFILE%\Documents\My Music\Sample Music` | `C:\ProgramData\Documents\My Music\Sample Music` |
| `%ALLUSERSPROFILE%\Documents\My Music` | `C:\ProgramData\Documents\My Music` |
| `%ALLUSERSPROFILE%\Documents\My Pictures` | `C:\ProgramData\Documents\My Pictures` |
| `%ALLUSERSPROFILE%\Documents\My Pictures\Sample Pictures` | `C:\ProgramData\Documents\My Pictures\Sample Pictures` |
| `%ALLUSERSPROFILE%\Documents\My Videos` | `C:\ProgramData\Documents\My Videos` |
| `%ALLUSERSPROFILE%\Microsoft\Windows\DeviceMetadataStore` | `C:\ProgramData\Microsoft\Windows\DeviceMetadataStore` |
| `%ALLUSERSPROFILE%\Microsoft\Windows\GameExplorer` | `C:\ProgramData\Microsoft\Windows\GameExplorer` |
| `%ALLUSERSPROFILE%\Microsoft\Windows\Ringtones` | `C:\ProgramData\Microsoft\Windows\Ringtones` |
| `%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu` | `C:\ProgramData\Microsoft\Windows\Start Menu` |
| `%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs` | `C:\ProgramData\Microsoft\Windows\Start Menu\Programs` |
| `%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\Administrative Tools` | `C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Administrative Tools` |
| `%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\StartUp` | `C:\ProgramData\Microsoft\Windows\Start Menu\Programs\StartUp` |
| `%ALLUSERSPROFILE%\Microsoft\Windows\Templates` | `C:\ProgramData\Microsoft\Windows\Templates` |
| `%ALLUSERSPROFILE%\Start Menu` | `C:\ProgramData\Start Menu` |
| `%ALLUSERSPROFILE%\Start Menu\Programs` | <span data-ttu-id="bae70-239">C:\ProgramData\Start Menu\Programs</span><span class="sxs-lookup"><span data-stu-id="bae70-239">C:\ProgramData\Start Menu\Programs</span></span> |
| `%ALLUSERSPROFILE%\Start Menu\Programs\Administrative Tools` | `C:\ProgramData\Start Menu\Programs\Administrative Tools` | 
| `%ALLUSERSPROFILE%\Templates` | `C:\ProgramData\Templates` |
| `%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\Templates` | `C:\Windows\System32\config\systemprofile\AppData\Local\Microsoft\Windows\ConnectedSearch\Templates` |
| `%LOCALAPPDATA%\Microsoft\Windows\History` | `C:\Windows\System32\config\systemprofile\AppData\Local\Microsoft\Windows\History` |
| `%PUBLIC%` | `C:\Users\Public` |
| `%PUBLIC%\AccountPictures` | `C:\Users\Public\AccountPictures` |
| `%PUBLIC%\Desktop` | `C:\Users\Public\Desktop` |
| `%PUBLIC%\Documents` | `C:\Users\Public\Documents` |
| `%PUBLIC%\Downloads` | `C:\Users\Public\Downloads` |
| `%PUBLIC%\Music\Sample Music` | `C:\Users\Public\Music\Sample Music` |
| `%PUBLIC%\Music\Sample Playlists` | `C:\Users\Public\Music\Sample Playlists` |
| `%PUBLIC%\Pictures\Sample Pictures` | `C:\Users\Public\Pictures\Sample Pictures` |
| `%PUBLIC%\RecordedTV.library-ms` | `C:\Users\Public\RecordedTV.library-ms` |
| `%PUBLIC%\Videos` | `C:\Users\Public\Videos` |
| `%PUBLIC%\Videos\Sample Videos` | `C:\Users\Public\Videos\Sample Videos` | 
| `%USERPROFILE%` | `C:\Windows\System32\config\systemprofile` |
| `%USERPROFILE%\AppData\Local` | `C:\Windows\System32\config\systemprofile\AppData\Local` |
| `%USERPROFILE%\AppData\LocalLow` | `C:\Windows\System32\config\systemprofile\AppData\LocalLow` |
| `%USERPROFILE%\AppData\Roaming` | `C:\Windows\System32\config\systemprofile\AppData\Roaming` |


## <a name="review-the-list-of-exclusions"></a><span data-ttu-id="bae70-240">Passer en revue la liste des exclusions</span><span class="sxs-lookup"><span data-stu-id="bae70-240">Review the list of exclusions</span></span>

<span data-ttu-id="bae70-241">Vous pouvez récupérer les éléments de la liste d'exclusions à l'aide de l'une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="bae70-241">You can retrieve the items in the exclusion list using one of the following methods:</span></span>
- [<span data-ttu-id="bae70-242">Intune</span><span class="sxs-lookup"><span data-stu-id="bae70-242">Intune</span></span>](/intune/deploy-use/help-secure-windows-pcs-with-endpoint-protection-for-microsoft-intune)
- [<span data-ttu-id="bae70-243">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bae70-243">Microsoft Endpoint Configuration Manager</span></span>](/configmgr/protect/deploy-use/endpoint-antimalware-policies)
- <span data-ttu-id="bae70-244">MpCmdRun</span><span class="sxs-lookup"><span data-stu-id="bae70-244">MpCmdRun</span></span>
- <span data-ttu-id="bae70-245">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bae70-245">PowerShell</span></span>
- [<span data-ttu-id="bae70-246">Application sécurité Windows</span><span class="sxs-lookup"><span data-stu-id="bae70-246">Windows Security app</span></span>](microsoft-defender-security-center-antivirus.md)

>[!IMPORTANT]
><span data-ttu-id="bae70-247">Les modifications apportées aux listes d'exclusions avec la stratégie de **groupe** s'afficheront dans les listes de l'application [Sécurité Windows.](microsoft-defender-security-center-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="bae70-247">Exclusion list changes made with Group Policy **will show** in the lists in the [Windows Security app](microsoft-defender-security-center-antivirus.md).</span></span>
>
><span data-ttu-id="bae70-248">Les modifications apportées dans l'application Sécurité Windows **ne s'afficheront pas** dans les listes de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="bae70-248">Changes made in the Windows Security app **will not show** in the Group Policy lists.</span></span>

<span data-ttu-id="bae70-249">Si vous utilisez PowerShell, vous pouvez récupérer la liste de deux manières :</span><span class="sxs-lookup"><span data-stu-id="bae70-249">If you use PowerShell, you can retrieve the list in two ways:</span></span>

- <span data-ttu-id="bae70-250">Récupérez l'état de toutes les préférences de l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="bae70-250">Retrieve the status of all Microsoft Defender Antivirus preferences.</span></span> <span data-ttu-id="bae70-251">Chaque liste est affichée sur des lignes distinctes, mais les éléments de chaque liste sont combinés dans la même ligne.</span><span class="sxs-lookup"><span data-stu-id="bae70-251">Each list is displayed on separate lines, but the items within each list are combined into the same line.</span></span>
- <span data-ttu-id="bae70-252">Écrivez l'état de toutes les préférences dans une variable et utilisez cette variable pour appeler uniquement la liste spécifique qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="bae70-252">Write the status of all preferences to a variable, and use that variable to only call the specific list you are interested in.</span></span> <span data-ttu-id="bae70-253">Chaque utilisation `Add-MpPreference` est écrite sur une nouvelle ligne.</span><span class="sxs-lookup"><span data-stu-id="bae70-253">Each use of `Add-MpPreference` is written to a new line.</span></span>

### <a name="validate-the-exclusion-list-by-using-mpcmdrun"></a><span data-ttu-id="bae70-254">Valider la liste d'exclusions à l'aide de MpCmdRun</span><span class="sxs-lookup"><span data-stu-id="bae70-254">Validate the exclusion list by using MpCmdRun</span></span>

<span data-ttu-id="bae70-255">Pour vérifier les exclusions avec l'outil de ligne de commande [dédié mpcmdrun.exe, ](./command-line-arguments-microsoft-defender-antivirus.md?branch=v-anbic-wdav-new-mpcmdrun-options)utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="bae70-255">To check exclusions with the dedicated [command-line tool mpcmdrun.exe](./command-line-arguments-microsoft-defender-antivirus.md?branch=v-anbic-wdav-new-mpcmdrun-options), use the following command:</span></span>

```DOS
Start, CMD (Run as admin)
cd "%programdata%\microsoft\windows defender\platform"
cd 4.18.1812.3 (Where 4.18.1812.3 is this month's MDAV "Platform Update".)
MpCmdRun.exe -CheckExclusion -path <path>
```

>[!NOTE]
><span data-ttu-id="bae70-256">La vérification des exclusions avec MpCmdRun nécessite l'antivirus Microsoft Defender CAMP version 4.18.1812.3 (publiée en décembre 2018) ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bae70-256">Checking exclusions with MpCmdRun requires Microsoft Defender Antivirus CAMP version 4.18.1812.3 (released in December 2018) or later.</span></span>

### <a name="review-the-list-of-exclusions-alongside-all-other-microsoft-defender-antivirus-preferences-by-using-powershell"></a><span data-ttu-id="bae70-257">Passer en revue la liste des exclusions avec toutes les autres préférences de l'Antivirus Microsoft Defender à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="bae70-257">Review the list of exclusions alongside all other Microsoft Defender Antivirus preferences by using PowerShell</span></span>

<span data-ttu-id="bae70-258">Utilisez la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="bae70-258">Use the following cmdlet:</span></span>

```PowerShell
Get-MpPreference
```

<span data-ttu-id="bae70-259">Dans l'exemple suivant, les éléments contenus dans la `ExclusionExtension` liste sont mis en surbrillant :</span><span class="sxs-lookup"><span data-stu-id="bae70-259">In the following example, the items contained in the `ExclusionExtension` list are highlighted:</span></span>

![Sortie PowerShell pour Get-MpPreference la liste d'exclusions avec d'autres préférences](images/defender/wdav-powershell-get-exclusions-all.png)

<span data-ttu-id="bae70-261">Pour plus d'informations, voir [Utiliser les cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter l'Antivirus Microsoft Defender et [les cmdlets Defender.](/powershell/module/defender/)</span><span class="sxs-lookup"><span data-stu-id="bae70-261">For more information, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/).</span></span>

### <a name="retrieve-a-specific-exclusions-list-by-using-powershell"></a><span data-ttu-id="bae70-262">Récupérer une liste d'exclusions spécifique à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="bae70-262">Retrieve a specific exclusions list by using PowerShell</span></span>

<span data-ttu-id="bae70-263">Utilisez l'extrait de code suivant (entrez chaque ligne en tant que commande distincte) ; remplacez **WDAVprefs** par l'étiquette que vous souhaitez nommer la variable :</span><span class="sxs-lookup"><span data-stu-id="bae70-263">Use the following code snippet (enter each line as a separate command); replace **WDAVprefs** with whatever label you want to name the variable:</span></span>

```PowerShell
$WDAVprefs = Get-MpPreference
$WDAVprefs.ExclusionExtension
$WDAVprefs.ExclusionPath
```

<span data-ttu-id="bae70-264">Dans l'exemple suivant, la liste est divisée en nouvelles lignes pour chaque utilisation de `Add-MpPreference` l'cmdlet :</span><span class="sxs-lookup"><span data-stu-id="bae70-264">In the following example, the list is split into new lines for each use of the `Add-MpPreference` cmdlet:</span></span>

![Sortie PowerShell affichant uniquement les entrées de la liste d'exclusions](images/defender/wdav-powershell-get-exclusions-variable.png)

<span data-ttu-id="bae70-266">Pour plus d'informations, voir [Utiliser les cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter l'Antivirus Microsoft Defender et [les cmdlets Defender.](/powershell/module/defender/)</span><span class="sxs-lookup"><span data-stu-id="bae70-266">For more information, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/).</span></span>

<a id="validate"></a>

## <a name="validate-exclusions-lists-with-the-eicar-test-file"></a><span data-ttu-id="bae70-267">Valider les listes d'exclusions avec le fichier de test EICAR</span><span class="sxs-lookup"><span data-stu-id="bae70-267">Validate exclusions lists with the EICAR test file</span></span>

<span data-ttu-id="bae70-268">Vous pouvez vérifier que vos listes d'exclusions fonctionnent à l'aide de PowerShell avec la cmdlet ou la classe WebClient .NET pour télécharger `Invoke-WebRequest` un fichier de test.</span><span class="sxs-lookup"><span data-stu-id="bae70-268">You can validate that your exclusion lists are working by using PowerShell with either the `Invoke-WebRequest` cmdlet or the .NET WebClient class to download a test file.</span></span>

<span data-ttu-id="bae70-269">Dans l'extrait de code PowerShell suivant, remplacez *test.txt* par un fichier conforme à vos règles d'exclusion.</span><span class="sxs-lookup"><span data-stu-id="bae70-269">In the following PowerShell snippet, replace *test.txt* with a file that conforms to your exclusion rules.</span></span> <span data-ttu-id="bae70-270">Par exemple, si vous avez exclu `.testing` l'extension, `test.txt` remplacez par `test.testing` .</span><span class="sxs-lookup"><span data-stu-id="bae70-270">For example, if you have excluded the `.testing` extension, replace `test.txt` with `test.testing`.</span></span> <span data-ttu-id="bae70-271">Si vous testez un chemin d'accès, veillez à exécuter la cmdlet dans ce chemin d'accès.</span><span class="sxs-lookup"><span data-stu-id="bae70-271">If you are testing a path, ensure you run the cmdlet within that path.</span></span>

```PowerShell
Invoke-WebRequest "http://www.eicar.org/download/eicar.com.txt" -OutFile "test.txt"
```

<span data-ttu-id="bae70-272">Si l'Antivirus Microsoft Defender signale un programme malveillant, la règle ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="bae70-272">If Microsoft Defender Antivirus reports malware, then the rule is not working.</span></span> <span data-ttu-id="bae70-273">Si aucun programme malveillant n'est détecté et que le fichier téléchargé existe, l'exclusion fonctionne.</span><span class="sxs-lookup"><span data-stu-id="bae70-273">If there is no report of malware and the downloaded file exists, then the exclusion is working.</span></span> <span data-ttu-id="bae70-274">Vous pouvez ouvrir le fichier pour confirmer que le contenu est identique à ce qui est décrit sur le site web du fichier [de test EICAR.](http://www.eicar.org/86-0-Intended-use.html)</span><span class="sxs-lookup"><span data-stu-id="bae70-274">You can open the file to confirm the contents are the same as what is described on the [EICAR test file website](http://www.eicar.org/86-0-Intended-use.html).</span></span>

<span data-ttu-id="bae70-275">Vous pouvez également utiliser le code PowerShell suivant, qui appelle la classe WebClient .NET pour télécharger le fichier de test , comme avec l'cmdlet ; remplacezc:\test.txtpar un fichier conforme à la règle que vous validez `Invoke-WebRequest` : </span><span class="sxs-lookup"><span data-stu-id="bae70-275">You can also use the following PowerShell code, which calls the .NET WebClient class to download the test file - as with the `Invoke-WebRequest` cmdlet; replace *c:\test.txt* with a file that conforms to the rule you are validating:</span></span>

```PowerShell
$client = new-object System.Net.WebClient
$client.DownloadFile("http://www.eicar.org/download/eicar.com.txt","c:\test.txt")
```

<span data-ttu-id="bae70-276">Si vous n'avez pas accès à Internet, vous pouvez créer votre propre fichier de test EICAR en écrivant la chaîne EICAR dans un nouveau fichier texte avec la commande PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="bae70-276">If you do not have Internet access, you can create your own EICAR test file by writing the EICAR string to a new text file with the following PowerShell command:</span></span>

```PowerShell
[io.file]::WriteAllText("test.txt",'X5O!P%@AP[4\PZX54(P^)7CC)7}$EICAR-STANDARD-ANTIVIRUS-TEST-FILE!$H+H*')
```

<span data-ttu-id="bae70-277">Vous pouvez également copier la chaîne dans un fichier texte vierge et essayer de l'enregistrer avec le nom de fichier ou dans le dossier que vous tentez d'exclure.</span><span class="sxs-lookup"><span data-stu-id="bae70-277">You can also copy the string into a blank text file and attempt to save it with the file name or in the folder you are attempting to exclude.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bae70-278">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bae70-278">Related topics</span></span>

- [<span data-ttu-id="bae70-279">Configurer et valider des exclusions dans les analyses de l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="bae70-279">Configure and validate exclusions in Microsoft Defender Antivirus scans</span></span>](configure-exclusions-microsoft-defender-antivirus.md)
- [<span data-ttu-id="bae70-280">Configurer et valider des exclusions pour les fichiers ouverts par des processus</span><span class="sxs-lookup"><span data-stu-id="bae70-280">Configure and validate exclusions for files opened by processes</span></span>](configure-process-opened-file-exclusions-microsoft-defender-antivirus.md)
- [<span data-ttu-id="bae70-281">Configurer les exclusions de l'Antivirus Microsoft Defender sur Windows Server</span><span class="sxs-lookup"><span data-stu-id="bae70-281">Configure Microsoft Defender Antivirus exclusions on Windows Server</span></span>](configure-server-exclusions-microsoft-defender-antivirus.md)
- [<span data-ttu-id="bae70-282">Erreurs courantes à éviter lors de la définition d'exclusions</span><span class="sxs-lookup"><span data-stu-id="bae70-282">Common mistakes to avoid when defining exclusions</span></span>](common-exclusion-mistakes-microsoft-defender-antivirus.md)
