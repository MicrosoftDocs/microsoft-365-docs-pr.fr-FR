---
title: Configurer des exclusions pour les fichiers ouverts par des processus spécifiques
description: Vous pouvez exclure des fichiers des analyses si elles ont été ouvertes par un processus spécifique.
keywords: Antivirus Microsoft Defender, processus, exclusion, fichiers, analyses
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
ms.openlocfilehash: 2fdc646cf616ff6a6fa36a83be3d2b1dd0432fbe
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52274611"
---
# <a name="configure-exclusions-for-files-opened-by-processes"></a><span data-ttu-id="16897-104">Configurer des exclusions pour les fichiers ouverts par des processus</span><span class="sxs-lookup"><span data-stu-id="16897-104">Configure exclusions for files opened by processes</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="16897-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="16897-105">**Applies to:**</span></span>

- [<span data-ttu-id="16897-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="16897-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="16897-107">Vous pouvez exclure des analyses des fichiers qui ont été ouverts par des processus spécifiques Antivirus Microsoft Defender analyses.</span><span class="sxs-lookup"><span data-stu-id="16897-107">You can exclude files that have been opened by specific processes from Microsoft Defender Antivirus scans.</span></span> <span data-ttu-id="16897-108">Voir [Recommandations pour définir des exclusions](configure-exclusions-microsoft-defender-antivirus.md#recommendations-for-defining-exclusions) avant de définir vos listes d’exclusions.</span><span class="sxs-lookup"><span data-stu-id="16897-108">See [Recommendations for defining exclusions](configure-exclusions-microsoft-defender-antivirus.md#recommendations-for-defining-exclusions) before defining your exclusion lists.</span></span>

<span data-ttu-id="16897-109">Cet article explique comment configurer des listes d’exclusions.</span><span class="sxs-lookup"><span data-stu-id="16897-109">This article describes how to configure exclusion lists.</span></span> 

## <a name="examples-of-exclusions"></a><span data-ttu-id="16897-110">Exemples d’exclusions</span><span class="sxs-lookup"><span data-stu-id="16897-110">Examples of exclusions</span></span>

|<span data-ttu-id="16897-111">Exclusion</span><span class="sxs-lookup"><span data-stu-id="16897-111">Exclusion</span></span> | <span data-ttu-id="16897-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="16897-112">Example</span></span> |
|---|---|
|<span data-ttu-id="16897-113">Tout fichier sur l’ordinateur ouvert par n’importe quel processus avec un nom de fichier spécifique</span><span class="sxs-lookup"><span data-stu-id="16897-113">Any file on the machine that is opened by any process with a specific file name</span></span> | <span data-ttu-id="16897-114">La spécification `test.exe` exclurait les fichiers ouverts par :</span><span class="sxs-lookup"><span data-stu-id="16897-114">Specifying `test.exe` would exclude files opened by:</span></span> <br/>`c:\sample\test.exe`<br/>`d:\internal\files\test.exe` |  
|<span data-ttu-id="16897-115">Tout fichier sur l’ordinateur ouvert par un processus sous un dossier spécifique</span><span class="sxs-lookup"><span data-stu-id="16897-115">Any file on the machine that is opened by any process under a specific folder</span></span> | <span data-ttu-id="16897-116">La spécification `c:\test\sample\*` exclurait les fichiers ouverts par :</span><span class="sxs-lookup"><span data-stu-id="16897-116">Specifying `c:\test\sample\*` would exclude files opened by:</span></span><br/>`c:\test\sample\test.exe`<br/>`c:\test\sample\test2.exe`<br/>`c:\test\sample\utility.exe` | 
|<span data-ttu-id="16897-117">Tout fichier sur l’ordinateur ouvert par un processus spécifique dans un dossier spécifique</span><span class="sxs-lookup"><span data-stu-id="16897-117">Any file on the machine that is opened by a specific process in a specific folder</span></span> | <span data-ttu-id="16897-118">La spécification `c:\test\process.exe` exclurait les fichiers ouverts uniquement par `c:\test\process.exe`</span><span class="sxs-lookup"><span data-stu-id="16897-118">Specifying `c:\test\process.exe` would exclude files only opened by `c:\test\process.exe`</span></span> |


<span data-ttu-id="16897-119">Lorsque vous ajoutez un processus à la liste d’exclusions de processus, Antivirus Microsoft Defender pas analyser les fichiers ouverts par ce processus, quel que soit l’emplacement des fichiers.</span><span class="sxs-lookup"><span data-stu-id="16897-119">When you add a process to the process exclusion list, Microsoft Defender Antivirus won't scan files opened by that process, no matter where the files are located.</span></span> <span data-ttu-id="16897-120">Toutefois, le processus proprement dit sera analysé, sauf s’il a également été ajouté à la liste [d’exclusions de fichiers.](configure-extension-file-exclusions-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="16897-120">The process itself, however, will be scanned unless it has also been added to the [file exclusion list](configure-extension-file-exclusions-microsoft-defender-antivirus.md).</span></span>

<span data-ttu-id="16897-121">Les exclusions s’appliquent uniquement à la protection et à la surveillance en temps [réel toujours en temps réel.](configure-real-time-protection-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="16897-121">The exclusions only apply to [always-on real-time protection and monitoring](configure-real-time-protection-microsoft-defender-antivirus.md).</span></span> <span data-ttu-id="16897-122">Elles ne s’appliquent pas aux analyses programmées ou à la demande.</span><span class="sxs-lookup"><span data-stu-id="16897-122">They don't apply to scheduled or on-demand scans.</span></span>

<span data-ttu-id="16897-123">Les modifications apportées avec  la stratégie de groupe aux listes d’exclusions s’afficheront dans les listes de [l Sécurité Windows app.](microsoft-defender-security-center-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="16897-123">Changes made with Group Policy to the exclusion lists **will show** in the lists in the [Windows Security app](microsoft-defender-security-center-antivirus.md).</span></span> <span data-ttu-id="16897-124">Toutefois, les modifications apportées à l Sécurité Windows’application **ne s’afficheront pas** dans les listes de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="16897-124">However, changes made in the Windows Security app **will not show** in the Group Policy lists.</span></span>

<span data-ttu-id="16897-125">Vous pouvez ajouter, supprimer et examiner les listes pour les exclusions dans la stratégie de groupe, Microsoft Endpoint Configuration Manager, Microsoft Intune et avec l’application Sécurité Windows, et vous pouvez utiliser des caractères génériques pour personnaliser davantage les listes.</span><span class="sxs-lookup"><span data-stu-id="16897-125">You can add, remove, and review the lists for exclusions in Group Policy, Microsoft Endpoint Configuration Manager, Microsoft Intune, and with the Windows Security app, and you can use wildcards to further customize the lists.</span></span>

<span data-ttu-id="16897-126">Vous pouvez également utiliser les cmdlets PowerShell et WMI pour configurer les listes d’exclusions, y compris la révision de vos listes.</span><span class="sxs-lookup"><span data-stu-id="16897-126">You can also use PowerShell cmdlets and WMI to configure the exclusion lists, including reviewing your lists.</span></span>

<span data-ttu-id="16897-127">Par défaut, les modifications locales apportées aux listes (par les utilisateurs ayant des privilèges d’administrateur, les modifications apportées avec PowerShell et WMI) sont fusionnées avec les listes telles que définies (et déployées) par la stratégie de groupe, Configuration Manager ou Intune.</span><span class="sxs-lookup"><span data-stu-id="16897-127">By default, local changes made to the lists (by users with administrator privileges; changes made with PowerShell and WMI) will be merged with the lists as defined (and deployed) by Group Policy, Configuration Manager, or Intune.</span></span> <span data-ttu-id="16897-128">Les listes de stratégies de groupe sont prioritaire en cas de conflit.</span><span class="sxs-lookup"><span data-stu-id="16897-128">The Group Policy lists will take precedence in the case of conflicts.</span></span>

<span data-ttu-id="16897-129">Vous pouvez [configurer la façon dont les listes d’exclusions définies](configure-local-policy-overrides-microsoft-defender-antivirus.md#merge-lists) localement et globalement sont fusionnées pour permettre aux modifications locales de remplacer les paramètres de déploiement géré.</span><span class="sxs-lookup"><span data-stu-id="16897-129">You can [configure how locally and globally defined exclusions lists are merged](configure-local-policy-overrides-microsoft-defender-antivirus.md#merge-lists) to allow local changes to override managed deployment settings.</span></span>

## <a name="configure-the-list-of-exclusions-for-files-opened-by-specified-processes"></a><span data-ttu-id="16897-130">Configurer la liste des exclusions pour les fichiers ouverts par des processus spécifiés</span><span class="sxs-lookup"><span data-stu-id="16897-130">Configure the list of exclusions for files opened by specified processes</span></span>

### <a name="use-microsoft-intune-to-exclude-files-that-have-been-opened-by-specified-processes-from-scans"></a><span data-ttu-id="16897-131">Utiliser Microsoft Intune pour exclure des analyses les fichiers qui ont été ouverts par des processus spécifiés</span><span class="sxs-lookup"><span data-stu-id="16897-131">Use Microsoft Intune to exclude files that have been opened by specified processes from scans</span></span>

<span data-ttu-id="16897-132">Pour plus d’informations, voir Configurer les [paramètres](/intune/device-restrictions-configure) de restriction d’appareil Microsoft Intune et Antivirus Microsoft Defender paramètres de restriction d’appareil pour Windows 10 [dans Intune.](/intune/device-restrictions-windows-10#microsoft-defender-antivirus)</span><span class="sxs-lookup"><span data-stu-id="16897-132">See [Configure device restriction settings in Microsoft Intune](/intune/device-restrictions-configure) and [Microsoft Defender Antivirus device restriction settings for Windows 10 in Intune](/intune/device-restrictions-windows-10#microsoft-defender-antivirus) for more details.</span></span>

### <a name="use-microsoft-endpoint-manager-to-exclude-files-that-have-been-opened-by-specified-processes-from-scans"></a><span data-ttu-id="16897-133">Utiliser Microsoft Endpoint Manager pour exclure des analyses les fichiers qui ont été ouverts par des processus spécifiés</span><span class="sxs-lookup"><span data-stu-id="16897-133">Use Microsoft Endpoint Manager to exclude files that have been opened by specified processes from scans</span></span>

<span data-ttu-id="16897-134">Découvrez comment créer et déployer des stratégies de logiciel [anti-programme](/configmgr/protect/deploy-use/endpoint-antimalware-policies#exclusion-settings) malveillant : paramètres d’exclusion pour plus d’informations sur la configuration Microsoft Endpoint Manager (branche actuelle).</span><span class="sxs-lookup"><span data-stu-id="16897-134">See [How to create and deploy antimalware policies: Exclusion settings](/configmgr/protect/deploy-use/endpoint-antimalware-policies#exclusion-settings) for details on configuring Microsoft Endpoint Manager (current branch).</span></span>

### <a name="use-group-policy-to-exclude-files-that-have-been-opened-by-specified-processes-from-scans"></a><span data-ttu-id="16897-135">Utiliser la stratégie de groupe pour exclure des analyses les fichiers qui ont été ouverts par des processus spécifiés</span><span class="sxs-lookup"><span data-stu-id="16897-135">Use Group Policy to exclude files that have been opened by specified processes from scans</span></span>

1. <span data-ttu-id="16897-136">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="16897-136">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="16897-137">Dans **l’Éditeur de gestion des stratégies de** groupe, cliquez sur **Configuration** ordinateur et cliquez **sur Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="16897-137">In the **Group Policy Management Editor** go to **Computer configuration** and click **Administrative templates**.</span></span>

3. <span data-ttu-id="16897-138">Développez l’arborescence **Windows composants > Antivirus Microsoft Defender > exclusions.**</span><span class="sxs-lookup"><span data-stu-id="16897-138">Expand the tree to **Windows components > Microsoft Defender Antivirus > Exclusions**.</span></span>

4. <span data-ttu-id="16897-139">Double-cliquez sur **Exclusions de processus** et ajoutez les exclusions :</span><span class="sxs-lookup"><span data-stu-id="16897-139">Double-click **Process Exclusions** and add the exclusions:</span></span>

    1. <span data-ttu-id="16897-140">Définissez l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="16897-140">Set the option to **Enabled**.</span></span>
    2. <span data-ttu-id="16897-141">Sous la section **Options,** cliquez sur **Afficher...**.</span><span class="sxs-lookup"><span data-stu-id="16897-141">Under the **Options** section, click **Show...**.</span></span>
    3. <span data-ttu-id="16897-142">Entrez chaque processus sur sa propre ligne sous la **colonne Nom de** la valeur.</span><span class="sxs-lookup"><span data-stu-id="16897-142">Enter each process on its own line under the **Value name** column.</span></span> <span data-ttu-id="16897-143">Consultez l’exemple de tableau pour les différents types d’exclusions de processus.</span><span class="sxs-lookup"><span data-stu-id="16897-143">See the example table for the different types of process exclusions.</span></span>  <span data-ttu-id="16897-144">Entrez **0 dans** la colonne **Valeur** pour tous les processus.</span><span class="sxs-lookup"><span data-stu-id="16897-144">Enter **0** in the **Value** column for all processes.</span></span>

5. <span data-ttu-id="16897-145">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="16897-145">Click **OK**.</span></span>

### <a name="use-powershell-cmdlets-to-exclude-files-that-have-been-opened-by-specified-processes-from-scans"></a><span data-ttu-id="16897-146">Utiliser les cmdlets PowerShell pour exclure des analyses les fichiers qui ont été ouverts par des processus spécifiés</span><span class="sxs-lookup"><span data-stu-id="16897-146">Use PowerShell cmdlets to exclude files that have been opened by specified processes from scans</span></span>

<span data-ttu-id="16897-147">L’utilisation de PowerShell pour ajouter ou supprimer des exclusions pour les fichiers qui ont été ouverts par des processus nécessite l’utilisation d’une combinaison de trois cmdlets avec le `-ExclusionProcess` paramètre.</span><span class="sxs-lookup"><span data-stu-id="16897-147">Using PowerShell to add or remove exclusions for files that have been opened by processes requires using a combination of three cmdlets with the `-ExclusionProcess` parameter.</span></span> <span data-ttu-id="16897-148">Les cmdlets sont toutes dans le [module Defender.](/powershell/module/defender/)</span><span class="sxs-lookup"><span data-stu-id="16897-148">The cmdlets are all in the [Defender module](/powershell/module/defender/).</span></span>

<span data-ttu-id="16897-149">Le format des cmdlets est :</span><span class="sxs-lookup"><span data-stu-id="16897-149">The format for the cmdlets is:</span></span>

```PowerShell
<cmdlet> -ExclusionProcess "<item>"
```

<span data-ttu-id="16897-150">Les listes suivantes sont autorisées en tant que \<cmdlet> :</span><span class="sxs-lookup"><span data-stu-id="16897-150">The following are allowed as the \<cmdlet>:</span></span>

|<span data-ttu-id="16897-151">Action de configuration</span><span class="sxs-lookup"><span data-stu-id="16897-151">Configuration action</span></span> | <span data-ttu-id="16897-152">Cmdlet PowerShell</span><span class="sxs-lookup"><span data-stu-id="16897-152">PowerShell cmdlet</span></span> |
|---|---|
|<span data-ttu-id="16897-153">Créer ou overwrite la liste</span><span class="sxs-lookup"><span data-stu-id="16897-153">Create or overwrite the list</span></span> | `Set-MpPreference` |
|<span data-ttu-id="16897-154">Ajouter à la liste</span><span class="sxs-lookup"><span data-stu-id="16897-154">Add to the list</span></span> | `Add-MpPreference` |
|<span data-ttu-id="16897-155">Supprimer des éléments de la liste</span><span class="sxs-lookup"><span data-stu-id="16897-155">Remove items from the list</span></span> | `Remove-MpPreference` |

>[!IMPORTANT]
><span data-ttu-id="16897-156">Si vous avez créé une liste, avec ou , en utilisant à nouveau la `Set-MpPreference` `Add-MpPreference` `Set-MpPreference` cmdlet, la liste existante est réécrite.</span><span class="sxs-lookup"><span data-stu-id="16897-156">If you have created a list, either with `Set-MpPreference` or `Add-MpPreference`, using the `Set-MpPreference` cmdlet again will overwrite the existing list.</span></span>

<span data-ttu-id="16897-157">Par exemple, l’extrait de code suivant entraîne l’exclusion par les analyses de l’Antivirus Microsoft Defender de tout fichier ouvert par le processus spécifié :</span><span class="sxs-lookup"><span data-stu-id="16897-157">For example, the following code snippet would cause Microsoft Defender AV scans to exclude any file that is opened by the specified process:</span></span>

```PowerShell
Add-MpPreference -ExclusionProcess "c:\internal\test.exe"
```

<span data-ttu-id="16897-158">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, voir Gérer l’antivirus avec les cmdlets PowerShell et [Antivirus Microsoft Defender cmdlets.](/powershell/module/defender)</span><span class="sxs-lookup"><span data-stu-id="16897-158">For more information on how to use PowerShell with Microsoft Defender Antivirus, see Manage antivirus with PowerShell cmdlets and [Microsoft Defender Antivirus cmdlets](/powershell/module/defender).</span></span>

### <a name="use-windows-management-instruction-wmi-to-exclude-files-that-have-been-opened-by-specified-processes-from-scans"></a><span data-ttu-id="16897-159">Utiliser Windows Management Instruction (WMI) pour exclure des analyses les fichiers qui ont été ouverts par des processus spécifiés</span><span class="sxs-lookup"><span data-stu-id="16897-159">Use Windows Management Instruction (WMI) to exclude files that have been opened by specified processes from scans</span></span>

<span data-ttu-id="16897-160">Utilisez les [ **méthodes Set,** **Add** et **Remove** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="16897-160">Use the [**Set**, **Add**, and **Remove** methods of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
ExclusionProcess
```

<span data-ttu-id="16897-161">L’utilisation **de Set**, **Add** et **Remove** est analogue à leurs équivalents dans PowerShell : , `Set-MpPreference` et `Add-MpPreference` `Remove-MpPreference` .</span><span class="sxs-lookup"><span data-stu-id="16897-161">The use of **Set**, **Add**, and **Remove** is analogous to their counterparts in PowerShell: `Set-MpPreference`, `Add-MpPreference`, and `Remove-MpPreference`.</span></span>

<span data-ttu-id="16897-162">Pour plus d’informations et les paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span><span class="sxs-lookup"><span data-stu-id="16897-162">For more information and allowed parameters, see  [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span></span>

### <a name="use-the-windows-security-app-to-exclude-files-that-have-been-opened-by-specified-processes-from-scans"></a><span data-ttu-id="16897-163">Utiliser l’Sécurité Windows pour exclure des analyses les fichiers qui ont été ouverts par des processus spécifiés</span><span class="sxs-lookup"><span data-stu-id="16897-163">Use the Windows Security app to exclude files that have been opened by specified processes from scans</span></span>

<span data-ttu-id="16897-164">Pour [plus d’instructions, voir Ajouter des exclusions Sécurité Windows’application.](microsoft-defender-security-center-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="16897-164">See [Add exclusions in the Windows Security app](microsoft-defender-security-center-antivirus.md) for instructions.</span></span>

## <a name="use-wildcards-in-the-process-exclusion-list"></a><span data-ttu-id="16897-165">Utiliser des caractères génériques dans la liste d’exclusions de processus</span><span class="sxs-lookup"><span data-stu-id="16897-165">Use wildcards in the process exclusion list</span></span>

<span data-ttu-id="16897-166">L’utilisation de caractères génériques dans la liste d’exclusions de processus est différente de leur utilisation dans d’autres listes d’exclusions.</span><span class="sxs-lookup"><span data-stu-id="16897-166">The use of wildcards in the process exclusion list is different from their use in other exclusion lists.</span></span>

<span data-ttu-id="16897-167">En particulier, vous ne pouvez pas utiliser le caractère générique de point d’interrogation ( ) et le caractère générique astérisque ( ) ne peut être utilisé qu’à la fin d’un `?` `*` chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="16897-167">In particular, you cannot use the question mark (`?`) wildcard, and the asterisk (`*`) wildcard can only be used at the end of a complete path.</span></span> <span data-ttu-id="16897-168">Vous pouvez toujours utiliser des variables d’environnement (par exemple) comme caractères génériques lors de la définition d’éléments dans la liste `%ALLUSERSPROFILE%` d’exclusions de processus.</span><span class="sxs-lookup"><span data-stu-id="16897-168">You can still use environment variables (such as `%ALLUSERSPROFILE%`) as wildcards when defining items in the process exclusion list.</span></span>

<span data-ttu-id="16897-169">Le tableau suivant décrit comment les caractères génériques peuvent être utilisés dans la liste d’exclusions de processus :</span><span class="sxs-lookup"><span data-stu-id="16897-169">The following table describes how the wildcards can be used in the process exclusion list:</span></span>

|<span data-ttu-id="16897-170">Caractère générique</span><span class="sxs-lookup"><span data-stu-id="16897-170">Wildcard</span></span> | <span data-ttu-id="16897-171">Exemple d’utilisation</span><span class="sxs-lookup"><span data-stu-id="16897-171">Example use</span></span> | <span data-ttu-id="16897-172">Exemples de correspondances</span><span class="sxs-lookup"><span data-stu-id="16897-172">Example matches</span></span> |
|:---|:---|:---|
|<span data-ttu-id="16897-173">`*` (astérisque)</span><span class="sxs-lookup"><span data-stu-id="16897-173">`*` (asterisk)</span></span> <br/><br/> <span data-ttu-id="16897-174">Remplace un nombre quelconque de caractères</span><span class="sxs-lookup"><span data-stu-id="16897-174">Replaces any number of characters</span></span> | `C:\MyData\*` | <span data-ttu-id="16897-175">Tout fichier ouvert par `C:\MyData\file.exe`</span><span class="sxs-lookup"><span data-stu-id="16897-175">Any file opened by `C:\MyData\file.exe`</span></span> |
|<span data-ttu-id="16897-176">Variables d’environnement</span><span class="sxs-lookup"><span data-stu-id="16897-176">Environment variables</span></span> <br/><br/> <span data-ttu-id="16897-177">La variable définie est remplie en tant que chemin d’accès lorsque l’exclusion est évaluée</span><span class="sxs-lookup"><span data-stu-id="16897-177">The defined variable is populated as a path when the exclusion is evaluated</span></span> | `%ALLUSERSPROFILE%\CustomLogFiles\file.exe` | <span data-ttu-id="16897-178">Tout fichier ouvert par `C:\ProgramData\CustomLogFiles\file.exe`</span><span class="sxs-lookup"><span data-stu-id="16897-178">Any file opened by `C:\ProgramData\CustomLogFiles\file.exe`</span></span> |

## <a name="review-the-list-of-exclusions"></a><span data-ttu-id="16897-179">Passer en revue la liste des exclusions</span><span class="sxs-lookup"><span data-stu-id="16897-179">Review the list of exclusions</span></span>

<span data-ttu-id="16897-180">Vous pouvez récupérer les éléments de la liste d’exclusions avec MpCmdRun, PowerShell, [Microsoft Endpoint Configuration Manager,](/configmgr/protect/deploy-use/endpoint-antimalware-policies#exclusion-settings) [Intune](/intune/device-restrictions-configure)ou [l’application Sécurité Windows.](microsoft-defender-security-center-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="16897-180">You can retrieve the items in the exclusion list with MpCmdRun, PowerShell, [Microsoft Endpoint Configuration Manager](/configmgr/protect/deploy-use/endpoint-antimalware-policies#exclusion-settings), [Intune](/intune/device-restrictions-configure), or the [Windows Security app](microsoft-defender-security-center-antivirus.md).</span></span>

<span data-ttu-id="16897-181">Si vous utilisez PowerShell, vous pouvez récupérer la liste de deux manières :</span><span class="sxs-lookup"><span data-stu-id="16897-181">If you use PowerShell, you can retrieve the list in two ways:</span></span>

- <span data-ttu-id="16897-182">Récupérez l’état de toutes Antivirus Microsoft Defender préférences.</span><span class="sxs-lookup"><span data-stu-id="16897-182">Retrieve the status of all Microsoft Defender Antivirus preferences.</span></span> <span data-ttu-id="16897-183">Chacune des listes s’affichera sur des lignes distinctes, mais les éléments de chaque liste seront combinés dans la même ligne.</span><span class="sxs-lookup"><span data-stu-id="16897-183">Each of the lists will be displayed on separate lines, but the items within each list will be combined into the same line.</span></span>
- <span data-ttu-id="16897-184">Écrivez l’état de toutes les préférences dans une variable et utilisez cette variable pour appeler uniquement la liste spécifique qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="16897-184">Write the status of all preferences to a variable, and use that variable to only call the specific list you are interested in.</span></span> <span data-ttu-id="16897-185">Chaque utilisation `Add-MpPreference` est écrite sur une nouvelle ligne.</span><span class="sxs-lookup"><span data-stu-id="16897-185">Each use of `Add-MpPreference` is written to a new line.</span></span>

### <a name="validate-the-exclusion-list-by-using-mpcmdrun"></a><span data-ttu-id="16897-186">Valider la liste d’exclusions à l’aide de MpCmdRun</span><span class="sxs-lookup"><span data-stu-id="16897-186">Validate the exclusion list by using MpCmdRun</span></span>

<span data-ttu-id="16897-187">Pour vérifier les exclusions avec l’outil en ligne de commande [mpcmdrun.exe, ](./command-line-arguments-microsoft-defender-antivirus.md?branch=v-anbic-wdav-new-mpcmdrun-options)utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="16897-187">To check exclusions with the dedicated [command-line tool mpcmdrun.exe](./command-line-arguments-microsoft-defender-antivirus.md?branch=v-anbic-wdav-new-mpcmdrun-options), use the following command:</span></span>

```DOS
MpCmdRun.exe -CheckExclusion -path <path>
```

> [!NOTE]
> <span data-ttu-id="16897-188">La vérification des exclusions avec MpCmdRun nécessite Antivirus Microsoft Defender CAMP version 4.18.1812.3 (publiée en décembre 2018) ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="16897-188">Checking exclusions with MpCmdRun requires Microsoft Defender Antivirus CAMP version 4.18.1812.3 (released in December 2018) or later.</span></span>


### <a name="review-the-list-of-exclusions-alongside-all-other-microsoft-defender-antivirus-preferences-by-using-powershell"></a><span data-ttu-id="16897-189">Passer en revue la liste des exclusions avec toutes les autres préférences Antivirus Microsoft Defender à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="16897-189">Review the list of exclusions alongside all other Microsoft Defender Antivirus preferences by using PowerShell</span></span>

<span data-ttu-id="16897-190">Utilisez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="16897-190">Use the following cmdlet:</span></span>

```PowerShell
Get-MpPreference
```

<span data-ttu-id="16897-191">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender) Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="16897-191">See [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

### <a name="retrieve-a-specific-exclusions-list-by-using-powershell"></a><span data-ttu-id="16897-192">Récupérer une liste d’exclusions spécifique à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="16897-192">Retrieve a specific exclusions list by using PowerShell</span></span>

<span data-ttu-id="16897-193">Utilisez l’extrait de code suivant (entrez chaque ligne en tant que commande distincte) ; remplacez **WDAVprefs** par l’étiquette que vous souhaitez nommer la variable :</span><span class="sxs-lookup"><span data-stu-id="16897-193">Use the following code snippet (enter each line as a separate command); replace **WDAVprefs** with whatever label you want to name the variable:</span></span>

```PowerShell
$WDAVprefs = Get-MpPreference
$WDAVprefs.ExclusionProcess
```

<span data-ttu-id="16897-194">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender) Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="16897-194">See [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

## <a name="related-articles"></a><span data-ttu-id="16897-195">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="16897-195">Related articles</span></span>

- [<span data-ttu-id="16897-196">Configurer et valider des exclusions dans Antivirus Microsoft Defender analyses</span><span class="sxs-lookup"><span data-stu-id="16897-196">Configure and validate exclusions in Microsoft Defender Antivirus scans</span></span>](configure-exclusions-microsoft-defender-antivirus.md)
- [<span data-ttu-id="16897-197">Configurer et valider des exclusions en fonction du nom de fichier, de l’extension et de l’emplacement du dossier</span><span class="sxs-lookup"><span data-stu-id="16897-197">Configure and validate exclusions based on file name, extension, and folder location</span></span>](configure-extension-file-exclusions-microsoft-defender-antivirus.md)
- [<span data-ttu-id="16897-198">Configurer des exclusions Antivirus Microsoft Defender sur Windows Server</span><span class="sxs-lookup"><span data-stu-id="16897-198">Configure Microsoft Defender Antivirus exclusions on Windows Server</span></span>](configure-server-exclusions-microsoft-defender-antivirus.md)
- [<span data-ttu-id="16897-199">Erreurs courantes à éviter lors de la définition d’exclusions</span><span class="sxs-lookup"><span data-stu-id="16897-199">Common mistakes to avoid when defining exclusions</span></span>](common-exclusion-mistakes-microsoft-defender-antivirus.md)
- [<span data-ttu-id="16897-200">Personnaliser, lancer et passer en revue les résultats des analyses et Antivirus Microsoft Defender correction</span><span class="sxs-lookup"><span data-stu-id="16897-200">Customize, initiate, and review the results of Microsoft Defender Antivirus scans and remediation</span></span>](customize-run-review-remediate-scans-microsoft-defender-antivirus.md)
- [<span data-ttu-id="16897-201">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="16897-201">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)