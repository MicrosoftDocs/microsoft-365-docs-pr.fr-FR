---
title: Planifier régulièrement des analyses rapides et complètes avec l'Antivirus Microsoft Defender
description: Configurer des analyses périodiques (programmées), notamment quand elles doivent s'exécuter et s'ils s'exécutent en tant qu'analyses complètes ou rapides
keywords: analyse rapide, analyse complète, rapide ou complète, analyse de planification, quotidienne, hebdomadaire, heure, programmée, périodique, régulière
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 11/02/2020
ms.reviewer: pauhijbr
manager: dansimp
ms.technology: mde
ms.openlocfilehash: bfa616423fc0c097b9909df8abf5b9c414490383
ms.sourcegitcommit: 7a339c9f7039825d131b39481ddf54c57b021b11
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51764086"
---
# <a name="configure-scheduled-quick-or-full-microsoft-defender-antivirus-scans"></a><span data-ttu-id="b2488-104">Configurer des analyses rapides ou complètes de l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="b2488-104">Configure scheduled quick or full Microsoft Defender Antivirus scans</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="b2488-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b2488-105">**Applies to:**</span></span>

- [<span data-ttu-id="b2488-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b2488-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)


> [!NOTE]
> <span data-ttu-id="b2488-107">Par défaut, l'Antivirus Microsoft Defender recherche une mise à jour 15 minutes avant l'heure des analyses programmées.</span><span class="sxs-lookup"><span data-stu-id="b2488-107">By default, Microsoft Defender Antivirus checks for an update 15 minutes before the time of any scheduled scans.</span></span> <span data-ttu-id="b2488-108">Vous pouvez [gérer la planification du téléchargement](manage-protection-update-schedule-microsoft-defender-antivirus.md) et de l'application des mises à jour de la protection pour remplacer cette valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="b2488-108">You can [Manage the schedule for when protection updates should be downloaded and applied](manage-protection-update-schedule-microsoft-defender-antivirus.md) to override this default.</span></span> 

<span data-ttu-id="b2488-109">Outre la protection en temps réel toujours en cours et les [analyses](run-scan-microsoft-defender-antivirus.md) à la demande, vous pouvez configurer des analyses régulières et programmées.</span><span class="sxs-lookup"><span data-stu-id="b2488-109">In addition to always-on real-time protection and [on-demand](run-scan-microsoft-defender-antivirus.md) scans, you can set up regular, scheduled scans.</span></span> 

<span data-ttu-id="b2488-110">Vous pouvez configurer le type d'analyse, le moment où l'analyse doit se produire et si l'analyse doit se produire après une mise à jour de [la protection](manage-protection-updates-microsoft-defender-antivirus.md) ou si le point de terminaison est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b2488-110">You can configure the type of scan, when the scan should occur, and if the scan should occur after a [protection update](manage-protection-updates-microsoft-defender-antivirus.md) or if the endpoint is being used.</span></span> <span data-ttu-id="b2488-111">Vous pouvez également spécifier le moment où des analyses spéciales doivent être nécessaires pour terminer la correction.</span><span class="sxs-lookup"><span data-stu-id="b2488-111">You can also specify when special scans to complete remediation should occur.</span></span>

<span data-ttu-id="b2488-112">Cet article explique comment configurer des analyses programmées avec la stratégie de groupe, les cmdlets PowerShell et WMI.</span><span class="sxs-lookup"><span data-stu-id="b2488-112">This article describes how to configure scheduled scans with Group Policy, PowerShell cmdlets, and WMI.</span></span> <span data-ttu-id="b2488-113">Vous pouvez également configurer des analyses de planifications avec [Microsoft Endpoint Configuration Manager](/configmgr/protect/deploy-use/endpoint-antimalware-policies#scheduled-scans-settings) ou Microsoft [Intune.](/mem/intune/configuration/device-restrictions-windows-10)</span><span class="sxs-lookup"><span data-stu-id="b2488-113">You can also configure schedules scans with [Microsoft Endpoint Configuration Manager](/configmgr/protect/deploy-use/endpoint-antimalware-policies#scheduled-scans-settings) or [Microsoft Intune](/mem/intune/configuration/device-restrictions-windows-10).</span></span>

## <a name="to-configure-the-group-policy-settings-described-in-this-article"></a><span data-ttu-id="b2488-114">Pour configurer les paramètres de stratégie de groupe décrits dans cet article</span><span class="sxs-lookup"><span data-stu-id="b2488-114">To configure the Group Policy settings described in this article</span></span>

1.  <span data-ttu-id="b2488-115">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="b2488-115">On your Group Policy management machine, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

3.  <span data-ttu-id="b2488-116">Dans **l'Éditeur de gestion des stratégies de** groupe, allez à **Configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="b2488-116">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

4.  <span data-ttu-id="b2488-117">Cliquez **sur Modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="b2488-117">Click **Administrative templates**.</span></span>

5.  <span data-ttu-id="b2488-118">Développez l'arborescence **des composants Windows > Antivirus Microsoft Defender,** puis l'emplacement spécifié dans le tableau ci-dessous. </span><span class="sxs-lookup"><span data-stu-id="b2488-118">Expand the tree to **Windows components > Microsoft Defender Antivirus** and then the **Location** specified in the table below.</span></span>

6. <span data-ttu-id="b2488-119">Double-cliquez sur le paramètre **de** stratégie comme indiqué dans le tableau ci-dessous et définissez l'option sur la configuration souhaitée.</span><span class="sxs-lookup"><span data-stu-id="b2488-119">Double-click the policy **Setting** as specified in the table below, and set the option to your desired configuration.</span></span> 

7. <span data-ttu-id="b2488-120">Cliquez **sur OK,** puis répétez l'une des autres configurations.</span><span class="sxs-lookup"><span data-stu-id="b2488-120">Click **OK**, and repeat for any other settings.</span></span>

<span data-ttu-id="b2488-121">Consultez également la rubrique Gérer quand les mises à jour de [la protection](manage-protection-update-schedule-microsoft-defender-antivirus.md) doivent être téléchargées et appliquées et Empêcher ou autoriser les utilisateurs à modifier localement les [paramètres de](configure-local-policy-overrides-microsoft-defender-antivirus.md) stratégie.</span><span class="sxs-lookup"><span data-stu-id="b2488-121">Also see the [Manage when protection updates should be downloaded and applied](manage-protection-update-schedule-microsoft-defender-antivirus.md) and [Prevent or allow users to locally modify policy settings](configure-local-policy-overrides-microsoft-defender-antivirus.md) topics.</span></span>

## <a name="quick-scan-versus-full-scan-and-custom-scan"></a><span data-ttu-id="b2488-122">Analyse rapide par rapport à l'analyse complète et à l'analyse personnalisée</span><span class="sxs-lookup"><span data-stu-id="b2488-122">Quick scan versus full scan and custom scan</span></span>

<span data-ttu-id="b2488-123">Lorsque vous définissez des analyses programmées, vous pouvez définir si l'analyse doit être une analyse complète ou rapide.</span><span class="sxs-lookup"><span data-stu-id="b2488-123">When you set up scheduled scans, you can set up whether the scan should be a full or quick scan.</span></span>

<span data-ttu-id="b2488-124">Les analyses rapides recherchent tous les emplacements où des programmes malveillants peuvent être enregistrés pour démarrer avec le système, tels que les clés de Registre et les dossiers de démarrage Windows connus.</span><span class="sxs-lookup"><span data-stu-id="b2488-124">Quick scans look at all the locations where there could be malware registered to start with the system, such as registry keys and known Windows startup folders.</span></span> 

<span data-ttu-id="b2488-125">Combinée avec la fonctionnalité de [protection](configure-real-time-protection-microsoft-defender-antivirus.md) en temps réel toujours en cours (qui examine les fichiers lorsqu'ils sont ouverts et fermés, et chaque fois qu'un utilisateur navigue vers un dossier), une analyse rapide permet d'assurer une couverture solide à la fois pour les programmes malveillants qui commencent par le système et les programmes malveillants au niveau du noyau.</span><span class="sxs-lookup"><span data-stu-id="b2488-125">Combined with [always-on real-time protection capability](configure-real-time-protection-microsoft-defender-antivirus.md) - which reviews files when they are opened and closed, and whenever a user navigates to a folder - a quick scan helps provide strong coverage both for malware that starts with the system and kernel-level malware.</span></span>  

<span data-ttu-id="b2488-126">Dans la plupart des cas, cela signifie qu'une analyse rapide est adéquate pour rechercher des programmes malveillants qui n'ont pas été détectés par la protection en temps réel.</span><span class="sxs-lookup"><span data-stu-id="b2488-126">In most instances, this means a quick scan is adequate to find malware that wasn't picked up by real-time protection.</span></span>

<span data-ttu-id="b2488-127">Une analyse complète peut être utile sur les points de terminaison qui ont rencontré une menace de programmes malveillants pour identifier s'il existe des composants inactifs nécessitant un nettoyage plus approfondi.</span><span class="sxs-lookup"><span data-stu-id="b2488-127">A full scan can be useful on endpoints that have encountered a malware threat to identify if there are any inactive components that require a more thorough clean-up.</span></span> <span data-ttu-id="b2488-128">Dans ce cas, vous pouvez utiliser une analyse complète lors de l'exécution [d'une analyse à la demande.](run-scan-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="b2488-128">In this instance, you may want to use a full scan when running an [on-demand scan](run-scan-microsoft-defender-antivirus.md).</span></span>

<span data-ttu-id="b2488-129">Une analyse personnalisée vous permet de spécifier les fichiers et dossiers à analyser, tels qu'un lecteur USB.</span><span class="sxs-lookup"><span data-stu-id="b2488-129">A custom scan allows you to specify the files and folders to scan, such as a USB drive.</span></span> 

>[!NOTE]
><span data-ttu-id="b2488-130">Par défaut, les analyses rapides s'exécutent sur des appareils amovibles montés, tels que des lecteurs USB.</span><span class="sxs-lookup"><span data-stu-id="b2488-130">By default, quick scans run on mounted removable devices, such as USB drives.</span></span>

## <a name="set-up-scheduled-scans"></a><span data-ttu-id="b2488-131">Configurer des analyses programmées</span><span class="sxs-lookup"><span data-stu-id="b2488-131">Set up scheduled scans</span></span>

<span data-ttu-id="b2488-132">Les analyses programmées s'exécuteront au jour et à l'heure que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="b2488-132">Scheduled scans will run at the day and time you specify.</span></span> <span data-ttu-id="b2488-133">Vous pouvez utiliser la stratégie de groupe, PowerShell et WMI pour configurer des analyses programmées.</span><span class="sxs-lookup"><span data-stu-id="b2488-133">You can use Group Policy, PowerShell, and WMI to configure scheduled scans.</span></span>

>[!NOTE]
><span data-ttu-id="b2488-134">Si un ordinateur est débranché et s'exécute sur batterie pendant une analyse complète programmée, l'analyse programmée s'arrête avec l'événement 1002, qui indique que l'analyse s'est arrêtée avant la fin.</span><span class="sxs-lookup"><span data-stu-id="b2488-134">If a computer is unplugged and running on battery during a scheduled full scan, the scheduled scan will stop with event 1002, which states that the scan stopped before completion.</span></span> <span data-ttu-id="b2488-135">L'Antivirus Microsoft Defender exécutera une analyse complète à l'heure prévue suivante.</span><span class="sxs-lookup"><span data-stu-id="b2488-135">Microsoft Defender Antivirus will run a full scan at the next scheduled time.</span></span>

### <a name="use-group-policy-to-schedule-scans"></a><span data-ttu-id="b2488-136">Utiliser une stratégie de groupe pour planifier des analyses</span><span class="sxs-lookup"><span data-stu-id="b2488-136">Use Group Policy to schedule scans</span></span>

|<span data-ttu-id="b2488-137">Emplacement</span><span class="sxs-lookup"><span data-stu-id="b2488-137">Location</span></span> | <span data-ttu-id="b2488-138">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b2488-138">Setting</span></span> | <span data-ttu-id="b2488-139">Description</span><span class="sxs-lookup"><span data-stu-id="b2488-139">Description</span></span> | <span data-ttu-id="b2488-140">Paramètre par défaut (s'il n'est pas configuré)</span><span class="sxs-lookup"><span data-stu-id="b2488-140">Default setting (if not configured)</span></span> |
|:---|:---|:---|:---|
|<span data-ttu-id="b2488-141">Analyser</span><span class="sxs-lookup"><span data-stu-id="b2488-141">Scan</span></span> | <span data-ttu-id="b2488-142">Spécifier le type d'analyse à utiliser pour une analyse programmée</span><span class="sxs-lookup"><span data-stu-id="b2488-142">Specify the scan type to use for a scheduled scan</span></span> | <span data-ttu-id="b2488-143">Analyse rapide</span><span class="sxs-lookup"><span data-stu-id="b2488-143">Quick scan</span></span> |
|<span data-ttu-id="b2488-144">Analyser</span><span class="sxs-lookup"><span data-stu-id="b2488-144">Scan</span></span> | <span data-ttu-id="b2488-145">Spécifier le jour de la semaine pour exécuter une analyse programmée</span><span class="sxs-lookup"><span data-stu-id="b2488-145">Specify the day of the week to run a scheduled scan</span></span> | <span data-ttu-id="b2488-146">Spécifiez le jour (ou jamais) d'exécuter une analyse.</span><span class="sxs-lookup"><span data-stu-id="b2488-146">Specify the day (or never) to run a scan.</span></span> | <span data-ttu-id="b2488-147">Jamais</span><span class="sxs-lookup"><span data-stu-id="b2488-147">Never</span></span> |
|<span data-ttu-id="b2488-148">Analyser</span><span class="sxs-lookup"><span data-stu-id="b2488-148">Scan</span></span> | <span data-ttu-id="b2488-149">Spécifier l'heure de la journée pour exécuter une analyse programmée</span><span class="sxs-lookup"><span data-stu-id="b2488-149">Specify the time of day to run a scheduled scan</span></span> | <span data-ttu-id="b2488-150">Spécifiez le nombre de minutes après minuit (par exemple, entrez **60** pour 1 h).</span><span class="sxs-lookup"><span data-stu-id="b2488-150">Specify the number of minutes after midnight (for example, enter **60** for 1 a.m.).</span></span> | <span data-ttu-id="b2488-151">2 h 00</span><span class="sxs-lookup"><span data-stu-id="b2488-151">2 a.m.</span></span> |
|<span data-ttu-id="b2488-152">Root</span><span class="sxs-lookup"><span data-stu-id="b2488-152">Root</span></span> | <span data-ttu-id="b2488-153">Randomize scheduled task times</span><span class="sxs-lookup"><span data-stu-id="b2488-153">Randomize scheduled task times</span></span> |<span data-ttu-id="b2488-154">Dans l'Antivirus Microsoft Defender : rendre aléatoire l'heure de début de l'analyse à n'importe quel intervalle de 0 à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="b2488-154">In Microsoft Defender Antivirus: Randomize the start time of the scan to any interval from 0 to 4 hours.</span></span> <br><span data-ttu-id="b2488-155">En FEP/SCEP : rendre aléatoire à n'importe quel intervalle plus ou moins 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="b2488-155">In FEP/SCEP: randomize to any interval plus or minus 30 minutes.</span></span> <span data-ttu-id="b2488-156">Cela peut être utile dans les déploiements VM ou VDI.</span><span class="sxs-lookup"><span data-stu-id="b2488-156">This can be useful in VM or VDI deployments.</span></span> | <span data-ttu-id="b2488-157">Activé</span><span class="sxs-lookup"><span data-stu-id="b2488-157">Enabled</span></span> |


### <a name="use-powershell-cmdlets-to-schedule-scans"></a><span data-ttu-id="b2488-158">Utiliser les cmdlets PowerShell pour planifier des analyses</span><span class="sxs-lookup"><span data-stu-id="b2488-158">Use PowerShell cmdlets to schedule scans</span></span>

<span data-ttu-id="b2488-159">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2488-159">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -ScanParameters
Set-MpPreference -ScanScheduleDay
Set-MpPreference -ScanScheduleTime
Set-MpPreference -RandomizeScheduleTaskTimes

```

<span data-ttu-id="b2488-160">Pour [plus d'informations](use-powershell-cmdlets-microsoft-defender-antivirus.md) sur l'utilisation de PowerShell avec l'Antivirus Microsoft Defender, voir les [cmdlets](/powershell/module/defender/) Utiliser PowerShell pour configurer et exécuter l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="b2488-160">See [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

### <a name="use-windows-management-instruction-wmi-to-schedule-scans"></a><span data-ttu-id="b2488-161">Utiliser Windows Management Instruction (WMI) pour planifier des analyses</span><span class="sxs-lookup"><span data-stu-id="b2488-161">Use Windows Management Instruction (WMI) to schedule scans</span></span>

<span data-ttu-id="b2488-162">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2488-162">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
ScanParameters
ScanScheduleDay
ScanScheduleTime
RandomizeScheduleTaskTimes
```

<span data-ttu-id="b2488-163">Pour plus d'informations et les paramètres autorisés, voir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2488-163">See the following for more information and allowed parameters:</span></span>
- [<span data-ttu-id="b2488-164">Windows Defender API WMIv2</span><span class="sxs-lookup"><span data-stu-id="b2488-164">Windows Defender WMIv2 APIs</span></span>](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)




## <a name="start-scheduled-scans-only-when-the-endpoint-is-not-in-use"></a><span data-ttu-id="b2488-165">Démarrer des analyses programmées uniquement lorsque le point de terminaison n'est pas en cours d'utilisation</span><span class="sxs-lookup"><span data-stu-id="b2488-165">Start scheduled scans only when the endpoint is not in use</span></span>

<span data-ttu-id="b2488-166">Vous pouvez définir l'analyse programmée de façon à ce qu'elle se produise uniquement lorsque le point de terminaison est allumé mais qu'il n'est pas utilisé avec la stratégie de groupe, PowerShell ou WMI.</span><span class="sxs-lookup"><span data-stu-id="b2488-166">You can set the scheduled scan to only occur when the endpoint is turned on but not in use with Group Policy, PowerShell, or WMI.</span></span>

> [!NOTE]
> <span data-ttu-id="b2488-167">Ces analyses ne respectent pas la configuration de limitation du processeur et tirez pleinement parti des ressources disponibles pour effectuer l'analyse aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="b2488-167">These scans will not honor the CPU throttling configuration and take full advantage of the resources available to complete the scan as fast as possible.</span></span>

### <a name="use-group-policy-to-schedule-scans"></a><span data-ttu-id="b2488-168">Utiliser une stratégie de groupe pour planifier des analyses</span><span class="sxs-lookup"><span data-stu-id="b2488-168">Use Group Policy to schedule scans</span></span>

|<span data-ttu-id="b2488-169">Emplacement</span><span class="sxs-lookup"><span data-stu-id="b2488-169">Location</span></span> | <span data-ttu-id="b2488-170">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b2488-170">Setting</span></span> | <span data-ttu-id="b2488-171">Description</span><span class="sxs-lookup"><span data-stu-id="b2488-171">Description</span></span> | <span data-ttu-id="b2488-172">Paramètre par défaut (s'il n'est pas configuré)</span><span class="sxs-lookup"><span data-stu-id="b2488-172">Default setting (if not configured)</span></span> |
|:---|:---|:---|:---|
|<span data-ttu-id="b2488-173">Analyser</span><span class="sxs-lookup"><span data-stu-id="b2488-173">Scan</span></span> | <span data-ttu-id="b2488-174">Démarrer l'analyse programmée uniquement lorsque l'ordinateur est en cours d'utilisation</span><span class="sxs-lookup"><span data-stu-id="b2488-174">Start the scheduled scan only when computer is on but not in use</span></span> | <span data-ttu-id="b2488-175">Les analyses programmées ne s'exécuteront pas, sauf si l'ordinateur est en cours d'utilisation</span><span class="sxs-lookup"><span data-stu-id="b2488-175">Scheduled scans will not run, unless the computer is on but not in use</span></span> | <span data-ttu-id="b2488-176">Activé</span><span class="sxs-lookup"><span data-stu-id="b2488-176">Enabled</span></span> |

### <a name="use-powershell-cmdlets"></a><span data-ttu-id="b2488-177">Utiliser les cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="b2488-177">Use PowerShell cmdlets</span></span>

<span data-ttu-id="b2488-178">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2488-178">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -ScanOnlyIfIdleEnabled
```

<span data-ttu-id="b2488-179">Pour [plus d'informations](use-powershell-cmdlets-microsoft-defender-antivirus.md) sur l'utilisation de PowerShell avec l'Antivirus Microsoft Defender, voir les [cmdlets](/powershell/module/defender/) Utiliser PowerShell pour configurer et exécuter l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="b2488-179">See [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

### <a name="use-windows-management-instruction-wmi"></a><span data-ttu-id="b2488-180">Utiliser Windows Management Instruction (WMI)</span><span class="sxs-lookup"><span data-stu-id="b2488-180">Use Windows Management Instruction (WMI)</span></span>

<span data-ttu-id="b2488-181">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2488-181">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
ScanOnlyIfIdleEnabled
```

<span data-ttu-id="b2488-182">Pour plus d'informations et les paramètres autorisés, voir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2488-182">See the following for more information and allowed parameters:</span></span>
- [<span data-ttu-id="b2488-183">Windows Defender API WMIv2</span><span class="sxs-lookup"><span data-stu-id="b2488-183">Windows Defender WMIv2 APIs</span></span>](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)

<a id="remed"></a>
## <a name="configure-when-full-scans-should-be-run-to-complete-remediation"></a><span data-ttu-id="b2488-184">Configurer le moment où les analyses complètes doivent être exécutés pour terminer la correction</span><span class="sxs-lookup"><span data-stu-id="b2488-184">Configure when full scans should be run to complete remediation</span></span>

<span data-ttu-id="b2488-185">Certaines menaces peuvent nécessiter une analyse complète pour terminer leur suppression et leur correction.</span><span class="sxs-lookup"><span data-stu-id="b2488-185">Some threats may require a full scan to complete their removal and remediation.</span></span> <span data-ttu-id="b2488-186">Vous pouvez planifier à quel moment ces analyses doivent se produire avec la stratégie de groupe, PowerShell ou WMI.</span><span class="sxs-lookup"><span data-stu-id="b2488-186">You can schedule when these scans should occur with Group Policy, PowerShell, or WMI.</span></span>

### <a name="use-group-policy-to-schedule-remediation-required-scans"></a><span data-ttu-id="b2488-187">Utiliser la stratégie de groupe pour planifier des analyses nécessaires à la correction</span><span class="sxs-lookup"><span data-stu-id="b2488-187">Use Group Policy to schedule remediation-required scans</span></span>

| <span data-ttu-id="b2488-188">Emplacement</span><span class="sxs-lookup"><span data-stu-id="b2488-188">Location</span></span> | <span data-ttu-id="b2488-189">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b2488-189">Setting</span></span> | <span data-ttu-id="b2488-190">Description</span><span class="sxs-lookup"><span data-stu-id="b2488-190">Description</span></span> | <span data-ttu-id="b2488-191">Paramètre par défaut (s'il n'est pas configuré)</span><span class="sxs-lookup"><span data-stu-id="b2488-191">Default setting (if not configured)</span></span> |
|---|---|---|---|
|<span data-ttu-id="b2488-192">Correction</span><span class="sxs-lookup"><span data-stu-id="b2488-192">Remediation</span></span> | <span data-ttu-id="b2488-193">Spécifier le jour de la semaine pour exécuter une analyse complète programmée afin de terminer la correction</span><span class="sxs-lookup"><span data-stu-id="b2488-193">Specify the day of the week to run a scheduled full scan to complete remediation</span></span> | <span data-ttu-id="b2488-194">Spécifiez le jour (ou jamais) d'exécuter une analyse.</span><span class="sxs-lookup"><span data-stu-id="b2488-194">Specify the day (or never) to run a scan.</span></span> | <span data-ttu-id="b2488-195">Jamais</span><span class="sxs-lookup"><span data-stu-id="b2488-195">Never</span></span> |
|<span data-ttu-id="b2488-196">Correction</span><span class="sxs-lookup"><span data-stu-id="b2488-196">Remediation</span></span> | <span data-ttu-id="b2488-197">Spécifier l'heure de la journée pour exécuter une analyse complète programmée afin de terminer la correction</span><span class="sxs-lookup"><span data-stu-id="b2488-197">Specify the time of day to run a scheduled full scan to complete remediation</span></span> | <span data-ttu-id="b2488-198">Spécifiez le nombre de minutes après minuit (par exemple, entrez **60** pour 1 h 00)</span><span class="sxs-lookup"><span data-stu-id="b2488-198">Specify the number of minutes after midnight (for example, enter **60** for 1 a.m.)</span></span> | <span data-ttu-id="b2488-199">2 h 00</span><span class="sxs-lookup"><span data-stu-id="b2488-199">2 a.m.</span></span> |

### <a name="use-powershell-cmdlets"></a><span data-ttu-id="b2488-200">Utiliser les cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="b2488-200">Use PowerShell cmdlets</span></span>

<span data-ttu-id="b2488-201">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2488-201">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -RemediationScheduleDay
Set-MpPreference -RemediationScheduleTime
```

<span data-ttu-id="b2488-202">Pour [plus d'informations](use-powershell-cmdlets-microsoft-defender-antivirus.md) sur l'utilisation de PowerShell avec l'Antivirus Microsoft Defender, voir les [cmdlets](/powershell/module/defender/) Utiliser PowerShell pour configurer et exécuter l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="b2488-202">See [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

### <a name="use-windows-management-instruction-wmi"></a><span data-ttu-id="b2488-203">Utiliser Windows Management Instruction (WMI)</span><span class="sxs-lookup"><span data-stu-id="b2488-203">Use Windows Management Instruction (WMI)</span></span>

<span data-ttu-id="b2488-204">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2488-204">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
RemediationScheduleDay
RemediationScheduleTime
```

<span data-ttu-id="b2488-205">Pour plus d'informations et les paramètres autorisés, voir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2488-205">See the following for more information and allowed parameters:</span></span>
- [<span data-ttu-id="b2488-206">Windows Defender API WMIv2</span><span class="sxs-lookup"><span data-stu-id="b2488-206">Windows Defender WMIv2 APIs</span></span>](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)




## <a name="set-up-daily-quick-scans"></a><span data-ttu-id="b2488-207">Configurer des analyses rapides quotidiennes</span><span class="sxs-lookup"><span data-stu-id="b2488-207">Set up daily quick scans</span></span>

<span data-ttu-id="b2488-208">Vous pouvez activer une analyse rapide quotidienne qui peut être exécuté en plus de vos autres analyses programmées avec la stratégie de groupe, PowerShell ou WMI.</span><span class="sxs-lookup"><span data-stu-id="b2488-208">You can enable a daily quick scan that can be run in addition to your other scheduled scans with Group Policy, PowerShell, or WMI.</span></span>


### <a name="use-group-policy-to-schedule-daily-scans"></a><span data-ttu-id="b2488-209">Utiliser la stratégie de groupe pour planifier des analyses quotidiennes</span><span class="sxs-lookup"><span data-stu-id="b2488-209">Use Group Policy to schedule daily scans</span></span>


|<span data-ttu-id="b2488-210">Emplacement</span><span class="sxs-lookup"><span data-stu-id="b2488-210">Location</span></span> | <span data-ttu-id="b2488-211">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b2488-211">Setting</span></span> | <span data-ttu-id="b2488-212">Description</span><span class="sxs-lookup"><span data-stu-id="b2488-212">Description</span></span> | <span data-ttu-id="b2488-213">Paramètre par défaut (s'il n'est pas configuré)</span><span class="sxs-lookup"><span data-stu-id="b2488-213">Default setting (if not configured)</span></span> |
|:---|:---|:---|:---|
|<span data-ttu-id="b2488-214">Analyser</span><span class="sxs-lookup"><span data-stu-id="b2488-214">Scan</span></span> | <span data-ttu-id="b2488-215">Spécifier l'intervalle pour exécuter des analyses rapides par jour</span><span class="sxs-lookup"><span data-stu-id="b2488-215">Specify the interval to run quick scans per day</span></span> | <span data-ttu-id="b2488-216">Spécifiez le nombre d'heures devant s'écoulée avant la prochaine analyse rapide.</span><span class="sxs-lookup"><span data-stu-id="b2488-216">Specify how many hours should elapse before the next quick scan.</span></span> <span data-ttu-id="b2488-217">Par exemple, pour exécuter toutes les deux heures, entrez **2**, pour une fois par jour, **entrez 24**.</span><span class="sxs-lookup"><span data-stu-id="b2488-217">For example, to run every two hours, enter **2**, for once a day, enter **24**.</span></span> <span data-ttu-id="b2488-218">Entrez **0 pour** ne jamais exécuter une analyse rapide quotidienne.</span><span class="sxs-lookup"><span data-stu-id="b2488-218">Enter **0** to never run a daily quick scan.</span></span> | <span data-ttu-id="b2488-219">Jamais</span><span class="sxs-lookup"><span data-stu-id="b2488-219">Never</span></span> |
|<span data-ttu-id="b2488-220">Analyser</span><span class="sxs-lookup"><span data-stu-id="b2488-220">Scan</span></span> | <span data-ttu-id="b2488-221">Spécifier l'heure d'une analyse rapide quotidienne</span><span class="sxs-lookup"><span data-stu-id="b2488-221">Specify the time for a daily quick scan</span></span> | <span data-ttu-id="b2488-222">Spécifiez le nombre de minutes après minuit (par exemple, entrez **60** pour 1 h 00)</span><span class="sxs-lookup"><span data-stu-id="b2488-222">Specify the number of minutes after midnight (for example, enter **60** for 1 a.m.)</span></span> | <span data-ttu-id="b2488-223">2 h 00</span><span class="sxs-lookup"><span data-stu-id="b2488-223">2 a.m.</span></span> |

### <a name="use-powershell-cmdlets-to-schedule-daily-scans"></a><span data-ttu-id="b2488-224">Utiliser les cmdlets PowerShell pour planifier des analyses quotidiennes</span><span class="sxs-lookup"><span data-stu-id="b2488-224">Use PowerShell cmdlets to schedule daily scans</span></span>

<span data-ttu-id="b2488-225">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2488-225">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -ScanScheduleQuickScanTime
```

<span data-ttu-id="b2488-226">Pour [plus d'informations](use-powershell-cmdlets-microsoft-defender-antivirus.md) sur l'utilisation de PowerShell avec l'Antivirus Microsoft Defender, voir les [cmdlets](/powershell/module/defender/) Utiliser PowerShell pour configurer et exécuter l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="b2488-226">See [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

### <a name="use-windows-management-instruction-wmi-to-schedule-daily-scans"></a><span data-ttu-id="b2488-227">Utiliser Windows Management Instruction (WMI) pour planifier des analyses quotidiennes</span><span class="sxs-lookup"><span data-stu-id="b2488-227">Use Windows Management Instruction (WMI) to schedule daily scans</span></span>

<span data-ttu-id="b2488-228">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2488-228">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
ScanScheduleQuickScanTime
```

<span data-ttu-id="b2488-229">Pour plus d'informations et les paramètres autorisés, voir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2488-229">See the following for more information and allowed parameters:</span></span>
- [<span data-ttu-id="b2488-230">Windows Defender API WMIv2</span><span class="sxs-lookup"><span data-stu-id="b2488-230">Windows Defender WMIv2 APIs</span></span>](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)


## <a name="enable-scans-after-protection-updates"></a><span data-ttu-id="b2488-231">Activer les analyses après les mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="b2488-231">Enable scans after protection updates</span></span>

<span data-ttu-id="b2488-232">Vous pouvez forcer une analyse à se produire après chaque mise à jour [de protection](manage-protection-updates-microsoft-defender-antivirus.md) avec la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b2488-232">You can force a scan to occur after every [protection update](manage-protection-updates-microsoft-defender-antivirus.md) with Group Policy.</span></span>

### <a name="use-group-policy-to-schedule-scans-after-protection-updates"></a><span data-ttu-id="b2488-233">Utiliser la stratégie de groupe pour planifier des analyses après les mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="b2488-233">Use Group Policy to schedule scans after protection updates</span></span>

|<span data-ttu-id="b2488-234">Emplacement</span><span class="sxs-lookup"><span data-stu-id="b2488-234">Location</span></span> | <span data-ttu-id="b2488-235">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b2488-235">Setting</span></span> | <span data-ttu-id="b2488-236">Description</span><span class="sxs-lookup"><span data-stu-id="b2488-236">Description</span></span> | <span data-ttu-id="b2488-237">Paramètre par défaut (s'il n'est pas configuré)</span><span class="sxs-lookup"><span data-stu-id="b2488-237">Default setting (if not configured)</span></span>|
|:---|:---|:---|:---|
|<span data-ttu-id="b2488-238">Mises à jour des signatures</span><span class="sxs-lookup"><span data-stu-id="b2488-238">Signature updates</span></span> | <span data-ttu-id="b2488-239">Activer l'analyse après la mise à jour des informations de sécurité</span><span class="sxs-lookup"><span data-stu-id="b2488-239">Turn on scan after Security intelligence update</span></span> | <span data-ttu-id="b2488-240">Une analyse se produit immédiatement après le téléchargement d'une nouvelle mise à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="b2488-240">A scan will occur immediately after a new protection update is downloaded</span></span> | <span data-ttu-id="b2488-241">Activé</span><span class="sxs-lookup"><span data-stu-id="b2488-241">Enabled</span></span> |

## <a name="see-also"></a><span data-ttu-id="b2488-242">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2488-242">See also</span></span>
- [<span data-ttu-id="b2488-243">Empêcher ou autoriser les utilisateurs à modifier localement les paramètres de stratégie</span><span class="sxs-lookup"><span data-stu-id="b2488-243">Prevent or allow users to locally modify policy settings</span></span>](configure-local-policy-overrides-microsoft-defender-antivirus.md)
- [<span data-ttu-id="b2488-244">Configurer et exécuter des analyses de l'Antivirus Microsoft Defender à la demande</span><span class="sxs-lookup"><span data-stu-id="b2488-244">Configure and run on-demand Microsoft Defender Antivirus scans</span></span>](run-scan-microsoft-defender-antivirus.md)
- [<span data-ttu-id="b2488-245">Configurer les options d'analyse de l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="b2488-245">Configure Microsoft Defender Antivirus scanning options</span></span>](configure-advanced-scan-types-microsoft-defender-antivirus.md)
- [<span data-ttu-id="b2488-246">Gérer les mises à jour de l'Antivirus Microsoft Defender et appliquer les lignes de base</span><span class="sxs-lookup"><span data-stu-id="b2488-246">Manage Microsoft Defender Antivirus updates and apply baselines</span></span>](manage-updates-baselines-microsoft-defender-antivirus.md)
- [<span data-ttu-id="b2488-247">Gérer le moment où les mises à jour de protection doivent être téléchargées et appliquées</span><span class="sxs-lookup"><span data-stu-id="b2488-247">Manage when protection updates should be downloaded and applied</span></span>](manage-protection-update-schedule-microsoft-defender-antivirus.md) 
- [<span data-ttu-id="b2488-248">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="b2488-248">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)