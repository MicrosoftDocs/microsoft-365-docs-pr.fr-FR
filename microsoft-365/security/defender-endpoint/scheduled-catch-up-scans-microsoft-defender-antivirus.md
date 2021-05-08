---
title: Planifier des analyses rapides et complètes régulières avec Antivirus Microsoft Defender
description: Configurer des analyses périodiques (programmées), notamment quand elles doivent s’exécuter et s’ils s’exécutent en tant qu’analyses complètes ou rapides
keywords: analyse rapide, analyse complète, rapide ou complète, analyse de planification, quotidienne, hebdomadaire, heure, programmée, périodique, régulière
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 05/05/2021
ms.reviewer: pauhijbr, ksarens
manager: dansimp
ms.technology: mde
ms.topic: how-to
ms.openlocfilehash: 1748a33be2c27123eb0437784dcdb2cb7905616a
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52274687"
---
# <a name="configure-scheduled-quick-or-full-microsoft-defender-antivirus-scans"></a><span data-ttu-id="495f0-104">Configurer des analyses antivirus Microsoft Defender rapides ou complètes</span><span class="sxs-lookup"><span data-stu-id="495f0-104">Configure scheduled quick or full Microsoft Defender Antivirus scans</span></span>

<span data-ttu-id="495f0-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="495f0-105">**Applies to:**</span></span>

- [<span data-ttu-id="495f0-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="495f0-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)


> [!NOTE]
> <span data-ttu-id="495f0-107">Par défaut, Antivirus Microsoft Defender recherche une mise à jour 15 minutes avant l’heure des analyses programmées.</span><span class="sxs-lookup"><span data-stu-id="495f0-107">By default, Microsoft Defender Antivirus checks for an update 15 minutes before the time of any scheduled scans.</span></span> <span data-ttu-id="495f0-108">Vous pouvez [gérer la planification du téléchargement](manage-protection-update-schedule-microsoft-defender-antivirus.md) et de l’application des mises à jour de la protection pour remplacer cette valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="495f0-108">You can [Manage the schedule for when protection updates should be downloaded and applied](manage-protection-update-schedule-microsoft-defender-antivirus.md) to override this default.</span></span> 

<span data-ttu-id="495f0-109">Outre la protection en temps réel [](run-scan-microsoft-defender-antivirus.md) toujours en cours et les analyses à la demande, vous pouvez configurer des analyses régulières et programmées.</span><span class="sxs-lookup"><span data-stu-id="495f0-109">In addition to always-on real-time protection and [on-demand](run-scan-microsoft-defender-antivirus.md) scans, you can set up regular, scheduled scans.</span></span> 

<span data-ttu-id="495f0-110">Vous pouvez configurer le type d’analyse, le moment où l’analyse doit se produire et si l’analyse doit se produire après une mise à jour de [la protection](manage-protection-updates-microsoft-defender-antivirus.md) ou si le point de terminaison est utilisé.</span><span class="sxs-lookup"><span data-stu-id="495f0-110">You can configure the type of scan, when the scan should occur, and if the scan should occur after a [protection update](manage-protection-updates-microsoft-defender-antivirus.md) or if the endpoint is being used.</span></span> <span data-ttu-id="495f0-111">Vous pouvez également spécifier à quel moment des analyses spéciales doivent être nécessaires pour terminer la correction.</span><span class="sxs-lookup"><span data-stu-id="495f0-111">You can also specify when special scans to complete remediation should occur.</span></span>

<span data-ttu-id="495f0-112">Cet article explique comment configurer des analyses programmées avec la stratégie de groupe, les cmdlets PowerShell et WMI.</span><span class="sxs-lookup"><span data-stu-id="495f0-112">This article describes how to configure scheduled scans with Group Policy, PowerShell cmdlets, and WMI.</span></span> <span data-ttu-id="495f0-113">Vous pouvez également configurer des analyses de planifications [avec Microsoft Endpoint Configuration Manager](/configmgr/protect/deploy-use/endpoint-antimalware-policies#scheduled-scans-settings) ou [Microsoft Intune](/mem/intune/configuration/device-restrictions-windows-10).</span><span class="sxs-lookup"><span data-stu-id="495f0-113">You can also configure schedules scans with [Microsoft Endpoint Configuration Manager](/configmgr/protect/deploy-use/endpoint-antimalware-policies#scheduled-scans-settings) or [Microsoft Intune](/mem/intune/configuration/device-restrictions-windows-10).</span></span>

## <a name="to-configure-the-group-policy-settings-described-in-this-article"></a><span data-ttu-id="495f0-114">Pour configurer les paramètres de stratégie de groupe décrits dans cet article</span><span class="sxs-lookup"><span data-stu-id="495f0-114">To configure the Group Policy settings described in this article</span></span>

1. <span data-ttu-id="495f0-115">Sur votre ordinateur de gestion des stratégies de groupe, dans l’Éditeur de stratégie de groupe, allez à Modèles d’administration de **configuration** ordinateur  >    >  **Windows composants**  >    >  **Antivirus Microsoft Defender’analyse.**</span><span class="sxs-lookup"><span data-stu-id="495f0-115">On your Group Policy management machine, in the Group Policy Editor, go to **Computer configuration** > **Administrative Templates** > **Windows Components** > **Microsoft Defender Antivirus** > **Scan**.</span></span>

2. <span data-ttu-id="495f0-116">Cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="495f0-116">Right-click the Group Policy Object you want to configure, and then select **Edit**.</span></span>

3. <span data-ttu-id="495f0-117">Spécifiez les paramètres de l’objet de stratégie de groupe, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="495f0-117">Specify settings for the Group Policy Object, and then select **OK**.</span></span> 

4. <span data-ttu-id="495f0-118">Répétez les étapes 1 à 4 pour chaque paramètre à configurer.</span><span class="sxs-lookup"><span data-stu-id="495f0-118">Repeat steps 1-4 for each setting you want to configure.</span></span>

5. <span data-ttu-id="495f0-119">Déployez votre objet de stratégie de groupe comme vous le faites normalement.</span><span class="sxs-lookup"><span data-stu-id="495f0-119">Deploy your Group Policy Object as you normally do.</span></span> <span data-ttu-id="495f0-120">Si vous avez besoin d’aide sur les objets de stratégie de groupe, voir [Créer un objet de stratégie de groupe.](/windows/security/threat-protection/windows-firewall/create-a-group-policy-object)</span><span class="sxs-lookup"><span data-stu-id="495f0-120">If you need help with Group Policy Objects, see [Create a Group Policy Object](/windows/security/threat-protection/windows-firewall/create-a-group-policy-object).</span></span>

<span data-ttu-id="495f0-121">Consultez également la rubrique Gérer quand les mises à jour de [la protection](manage-protection-update-schedule-microsoft-defender-antivirus.md) doivent être téléchargées et appliquées, et empêcher ou autoriser les utilisateurs à modifier localement les [paramètres de](configure-local-policy-overrides-microsoft-defender-antivirus.md) stratégie.</span><span class="sxs-lookup"><span data-stu-id="495f0-121">Also see the [Manage when protection updates should be downloaded and applied](manage-protection-update-schedule-microsoft-defender-antivirus.md) and [Prevent or allow users to locally modify policy settings](configure-local-policy-overrides-microsoft-defender-antivirus.md) topics.</span></span>

## <a name="quick-scan-versus-full-scan-and-custom-scan"></a><span data-ttu-id="495f0-122">Analyse rapide par rapport à l’analyse complète et à l’analyse personnalisée</span><span class="sxs-lookup"><span data-stu-id="495f0-122">Quick scan versus full scan and custom scan</span></span>

<span data-ttu-id="495f0-123">Lorsque vous définissez des analyses programmées, vous pouvez définir si l’analyse doit être une analyse complète ou rapide.</span><span class="sxs-lookup"><span data-stu-id="495f0-123">When you set up scheduled scans, you can set up whether the scan should be a full or quick scan.</span></span>


|<span data-ttu-id="495f0-124">Analyse rapide</span><span class="sxs-lookup"><span data-stu-id="495f0-124">Quick scan</span></span>  |<span data-ttu-id="495f0-125">Analyse complète</span><span class="sxs-lookup"><span data-stu-id="495f0-125">Full scan</span></span>  | <span data-ttu-id="495f0-126">Analyse personnalisée</span><span class="sxs-lookup"><span data-stu-id="495f0-126">Custom scan</span></span> |
|---------|---------|---------|
|<span data-ttu-id="495f0-127">Une analyse rapide examine tous les emplacements où des programmes malveillants peuvent être enregistrés pour démarrer avec le système, tels que les clés de Registre et les dossiers de démarrage Windows connus.</span><span class="sxs-lookup"><span data-stu-id="495f0-127">A quick scan looks at all the locations where there could be malware registered to start with the system, such as registry keys and known Windows startup folders.</span></span> <p><span data-ttu-id="495f0-128">Dans la plupart des cas, une analyse rapide est suffisante et est recommandée pour les analyses programmées.</span><span class="sxs-lookup"><span data-stu-id="495f0-128">In most cases, a quick scan is sufficient and is recommended for scheduled scans.</span></span> |<span data-ttu-id="495f0-129">Une analyse complète commence par l’exécution d’une analyse rapide, puis se poursuit avec une analyse séquentielle de tous les disques fixes montés et lecteurs amovibles/réseau (si l’analyse complète est configurée pour le faire).</span><span class="sxs-lookup"><span data-stu-id="495f0-129">A full scan starts by running a quick scan and then continues with a sequential file scan of all mounted fixed disks and removable/network drives (if the full scan is configured to do so).</span></span> <p><span data-ttu-id="495f0-130">L’analyse complète peut prendre quelques heures ou jours, en fonction de la quantité et du type de données à analyser.</span><span class="sxs-lookup"><span data-stu-id="495f0-130">A full scan can take a few hours or days to complete, depending on the amount and type of data that needs to be scanned.</span></span><p><span data-ttu-id="495f0-131">Une fois l’analyse complète terminée, de nouvelles informations de sécurité sont disponibles et une nouvelle analyse est nécessaire pour s’assurer qu’aucune autre menace n’est détectée avec la nouvelle intelligence de sécurité.</span><span class="sxs-lookup"><span data-stu-id="495f0-131">When the full scan is complete, new security intelligence is available, and a new scan is required to make sure that no other threats are detected with the new security intelligence.</span></span>   | <span data-ttu-id="495f0-132">Une analyse personnalisée est une analyse rapide qui s’exécute sur les fichiers et dossiers que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="495f0-132">A custom scan is a quick scan that runs on the files and folders you specify.</span></span> <span data-ttu-id="495f0-133">Par exemple, vous pouvez choisir d’analyser un lecteur USB ou un dossier spécifique sur le lecteur local de votre appareil.</span><span class="sxs-lookup"><span data-stu-id="495f0-133">For example, you can opt to scan a USB drive, or a specific folder on your device's local drive.</span></span> <p> | 

>[!NOTE]
><span data-ttu-id="495f0-134">Par défaut, les analyses rapides s’exécutent sur des appareils amovibles montés, tels que des lecteurs USB.</span><span class="sxs-lookup"><span data-stu-id="495f0-134">By default, quick scans run on mounted removable devices, such as USB drives.</span></span>

### <a name="how-do-i-know-which-scan-type-to-choose"></a><span data-ttu-id="495f0-135">Comment savoir quel type d’analyse choisir ?</span><span class="sxs-lookup"><span data-stu-id="495f0-135">How do I know which scan type to choose?</span></span>

<span data-ttu-id="495f0-136">Utilisez le tableau suivant pour choisir un type d’analyse.</span><span class="sxs-lookup"><span data-stu-id="495f0-136">Use the following table to choose a scan type.</span></span>


|<span data-ttu-id="495f0-137">Scénario</span><span class="sxs-lookup"><span data-stu-id="495f0-137">Scenario</span></span>  |<span data-ttu-id="495f0-138">Type d’analyse recommandé</span><span class="sxs-lookup"><span data-stu-id="495f0-138">Recommended scan type</span></span>  |
|---------|---------|
|<span data-ttu-id="495f0-139">Vous souhaitez configurer des analyses régulières et programmées</span><span class="sxs-lookup"><span data-stu-id="495f0-139">You want to set up regular, scheduled scans</span></span>     | <span data-ttu-id="495f0-140">Analyse rapide</span><span class="sxs-lookup"><span data-stu-id="495f0-140">Quick scan</span></span> <p><span data-ttu-id="495f0-141">Une analyse rapide vérifie les processus, la mémoire, les profils et certains emplacements de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="495f0-141">A quick scan checks the processes, memory, profiles, and certain locations on the device.</span></span> <span data-ttu-id="495f0-142">Combinée à [une protection en](configure-real-time-protection-microsoft-defender-antivirus.md)temps réel toujours en cours, une analyse rapide permet d’assurer une couverture forte à la fois pour les programmes malveillants qui commencent par le système et les programmes malveillants au niveau du noyau.</span><span class="sxs-lookup"><span data-stu-id="495f0-142">Combined with [always-on real-time protection](configure-real-time-protection-microsoft-defender-antivirus.md), a quick scan helps provide strong coverage both for malware that starts with the system and kernel-level malware.</span></span> <span data-ttu-id="495f0-143">La protection en temps réel examine les fichiers lorsqu’ils sont ouverts et fermés, et chaque fois qu’un utilisateur navigue vers un dossier.</span><span class="sxs-lookup"><span data-stu-id="495f0-143">Real-time protection reviews files when they are opened and closed, and whenever a user navigates to a folder.</span></span>         |
|<span data-ttu-id="495f0-144">Les menaces, telles que les programmes malveillants, sont détectées sur un appareil</span><span class="sxs-lookup"><span data-stu-id="495f0-144">Threats, such as malware, are detected on a device</span></span>     | <span data-ttu-id="495f0-145">Analyse complète</span><span class="sxs-lookup"><span data-stu-id="495f0-145">Full scan</span></span> <p><span data-ttu-id="495f0-146">Une analyse complète peut aider à identifier s’il existe des composants inactifs qui nécessitent un nettoyage plus approfondi.</span><span class="sxs-lookup"><span data-stu-id="495f0-146">A full scan can help identify whether there are any inactive components that require a more thorough clean-up.</span></span>         |
|<span data-ttu-id="495f0-147">Vous souhaitez exécuter une [analyse à la demande](run-scan-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="495f0-147">You want to run an [on-demand scan](run-scan-microsoft-defender-antivirus.md)</span></span>     | <span data-ttu-id="495f0-148">Analyse complète</span><span class="sxs-lookup"><span data-stu-id="495f0-148">Full scan</span></span>  <p><span data-ttu-id="495f0-149">Une analyse complète examine tous les fichiers sur le disque de l’appareil, y compris les fichiers obsolètes, archivés et qui ne sont pas accessibles quotidiennement.</span><span class="sxs-lookup"><span data-stu-id="495f0-149">A full scan looks at all files on the device disk, including files that are stale, archived, and not accessed on a daily basis.</span></span>      |
| <span data-ttu-id="495f0-150">Vous souhaitez vous assurer qu’un appareil portable, tel qu’un lecteur USB, ne contient pas de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="495f0-150">You want to make sure a portable device, such as a USB drive, does not contain malware</span></span> | <span data-ttu-id="495f0-151">Analyse personnalisée</span><span class="sxs-lookup"><span data-stu-id="495f0-151">Custom scan</span></span> <p><span data-ttu-id="495f0-152">Une analyse personnalisée vous permet de sélectionner des emplacements, dossiers ou fichiers spécifiques et exécute une analyse rapide.</span><span class="sxs-lookup"><span data-stu-id="495f0-152">A custom scan enables you to select specific locations, folders, or files and runs a quick scan.</span></span> |

### <a name="what-else-do-i-need-to-know-about-quick-and-full-scans"></a><span data-ttu-id="495f0-153">Que dois-je savoir d’autre sur les analyses rapides et complètes ?</span><span class="sxs-lookup"><span data-stu-id="495f0-153">What else do I need to know about quick and full scans?</span></span>

- <span data-ttu-id="495f0-154">Les fichiers malveillants peuvent être stockés dans des emplacements qui ne sont pas inclus dans une analyse rapide.</span><span class="sxs-lookup"><span data-stu-id="495f0-154">Malicious files can be stored in locations that are not included in a quick scan.</span></span> <span data-ttu-id="495f0-155">Toutefois, la protection en temps réel toujours en cours examine tous les fichiers ouverts et fermés, ainsi que tous les fichiers qui se contiennent dans des dossiers accessibles par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="495f0-155">However, always-on real-time protection reviews all files that are opened and closed, and any files that are in folders that are accessed by a user.</span></span> <span data-ttu-id="495f0-156">La combinaison d’une protection en temps réel et d’une analyse rapide permet de fournir une protection forte contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="495f0-156">The combination of real-time protection and a quick scan helps provide strong protection against malware.</span></span>

- <span data-ttu-id="495f0-157">La protection à l’accès avec une protection assurée par le [cloud](cloud-protection-microsoft-defender-antivirus.md) permet de s’assurer que tous les fichiers accessibles sur le système sont analysés avec les derniers modèles d’intelligence de sécurité et d’apprentissage automatique dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="495f0-157">On-access protection with [cloud-delivered protection](cloud-protection-microsoft-defender-antivirus.md) helps ensure that all the files accessed on the system are being scanned with the latest security intelligence and cloud machine learning models.</span></span>

- <span data-ttu-id="495f0-158">Lorsque la protection en temps réel détecte des programmes malveillants et que l’étendue des fichiers affectés n’est pas déterminée initialement, Antivirus Microsoft Defender lance une analyse complète dans le cadre du processus de correction.</span><span class="sxs-lookup"><span data-stu-id="495f0-158">When real-time protection detects malware and the extent of the affected files is not determined initially, Microsoft Defender Antivirus initiates a full scan as part of the remediation process.</span></span>

- <span data-ttu-id="495f0-159">Une analyse complète peut détecter des fichiers malveillants qui n’ont pas été détectés par d’autres analyses, telles qu’une analyse rapide.</span><span class="sxs-lookup"><span data-stu-id="495f0-159">A full scan can detect malicious files that were not detected by other scans, such as a quick scan.</span></span> <span data-ttu-id="495f0-160">Toutefois, une analyse complète peut prendre un certain temps et utiliser des ressources système précieuses pour se terminer.</span><span class="sxs-lookup"><span data-stu-id="495f0-160">However, a full scan can take a while and use valuable system resources to complete.</span></span>

- <span data-ttu-id="495f0-161">Si un appareil est hors connexion pendant une période prolongée, une analyse complète peut prendre plus de temps.</span><span class="sxs-lookup"><span data-stu-id="495f0-161">If a device is offline for an extended period of time, a full scan can take longer to complete.</span></span> 

## <a name="set-up-scheduled-scans"></a><span data-ttu-id="495f0-162">Configurer des analyses programmées</span><span class="sxs-lookup"><span data-stu-id="495f0-162">Set up scheduled scans</span></span>

<span data-ttu-id="495f0-163">Les analyses programmées s’exécutent le jour et l’heure que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="495f0-163">Scheduled scans run on the day and time that you specify.</span></span> <span data-ttu-id="495f0-164">Vous pouvez utiliser la stratégie de groupe, PowerShell et WMI pour configurer des analyses programmées.</span><span class="sxs-lookup"><span data-stu-id="495f0-164">You can use Group Policy, PowerShell, and WMI to configure scheduled scans.</span></span>

> [!NOTE]
> <span data-ttu-id="495f0-165">Si un appareil est débranché et s’exécute sur batterie pendant une analyse complète programmée, l’analyse programmée s’arrête avec l’événement 1002, qui indique que l’analyse s’est arrêtée avant la fin.</span><span class="sxs-lookup"><span data-stu-id="495f0-165">If a device is unplugged and running on battery during a scheduled full scan, the scheduled scan will stop with event 1002, which states that the scan stopped before completion.</span></span> <span data-ttu-id="495f0-166">Antivirus Microsoft Defender exécutera une analyse complète à l’heure prévue suivante.</span><span class="sxs-lookup"><span data-stu-id="495f0-166">Microsoft Defender Antivirus will run a full scan at the next scheduled time.</span></span>

### <a name="use-group-policy-to-schedule-scans"></a><span data-ttu-id="495f0-167">Utiliser une stratégie de groupe pour planifier des analyses</span><span class="sxs-lookup"><span data-stu-id="495f0-167">Use Group Policy to schedule scans</span></span>

|<span data-ttu-id="495f0-168">Lieu</span><span class="sxs-lookup"><span data-stu-id="495f0-168">Location</span></span> | <span data-ttu-id="495f0-169">Paramètre</span><span class="sxs-lookup"><span data-stu-id="495f0-169">Setting</span></span> | <span data-ttu-id="495f0-170">Description</span><span class="sxs-lookup"><span data-stu-id="495f0-170">Description</span></span> | <span data-ttu-id="495f0-171">Paramètre par défaut (s’il n’est pas configuré)</span><span class="sxs-lookup"><span data-stu-id="495f0-171">Default setting (if not configured)</span></span> |
|:---|:---|:---|:---|
|<span data-ttu-id="495f0-172">Analyser</span><span class="sxs-lookup"><span data-stu-id="495f0-172">Scan</span></span> | <span data-ttu-id="495f0-173">Spécifier le type d’analyse à utiliser pour une analyse programmée</span><span class="sxs-lookup"><span data-stu-id="495f0-173">Specify the scan type to use for a scheduled scan</span></span> | <span data-ttu-id="495f0-174">Analyse rapide</span><span class="sxs-lookup"><span data-stu-id="495f0-174">Quick scan</span></span> |
|<span data-ttu-id="495f0-175">Analyser</span><span class="sxs-lookup"><span data-stu-id="495f0-175">Scan</span></span> | <span data-ttu-id="495f0-176">Spécifier le jour de la semaine pour exécuter une analyse programmée</span><span class="sxs-lookup"><span data-stu-id="495f0-176">Specify the day of the week to run a scheduled scan</span></span> | <span data-ttu-id="495f0-177">Spécifiez le jour (ou jamais) d’exécuter une analyse.</span><span class="sxs-lookup"><span data-stu-id="495f0-177">Specify the day (or never) to run a scan.</span></span> | <span data-ttu-id="495f0-178">Jamais</span><span class="sxs-lookup"><span data-stu-id="495f0-178">Never</span></span> |
|<span data-ttu-id="495f0-179">Analyser</span><span class="sxs-lookup"><span data-stu-id="495f0-179">Scan</span></span> | <span data-ttu-id="495f0-180">Spécifier l’heure de la journée pour exécuter une analyse programmée</span><span class="sxs-lookup"><span data-stu-id="495f0-180">Specify the time of day to run a scheduled scan</span></span> | <span data-ttu-id="495f0-181">Spécifiez le nombre de minutes après minuit (par exemple, entrez **60** pour 1 heure du matin).</span><span class="sxs-lookup"><span data-stu-id="495f0-181">Specify the number of minutes after midnight (for example, enter **60** for 1 a.m.).</span></span> | <span data-ttu-id="495f0-182">2 h 00</span><span class="sxs-lookup"><span data-stu-id="495f0-182">2 a.m.</span></span> |
|<span data-ttu-id="495f0-183">Root</span><span class="sxs-lookup"><span data-stu-id="495f0-183">Root</span></span> | <span data-ttu-id="495f0-184">Randomize scheduled task times</span><span class="sxs-lookup"><span data-stu-id="495f0-184">Randomize scheduled task times</span></span> |<span data-ttu-id="495f0-185">In Antivirus Microsoft Defender, randomize the start time of the scan to any interval from 0 to 4 hours.</span><span class="sxs-lookup"><span data-stu-id="495f0-185">In Microsoft Defender Antivirus, randomize the start time of the scan to any interval from 0 to 4 hours.</span></span> <p><span data-ttu-id="495f0-186">Dans [SCEP](/mem/intune/protect/certificates-scep-configure), rendre aléatoires les analyses à n’importe quel intervalle plus ou moins 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="495f0-186">In [SCEP](/mem/intune/protect/certificates-scep-configure), randomize scans to any interval plus or minus 30 minutes.</span></span> <span data-ttu-id="495f0-187">Cela peut être utile dans les machines virtuelles ou les déploiements VDI.</span><span class="sxs-lookup"><span data-stu-id="495f0-187">This can be useful in virtual machines or VDI deployments.</span></span> | <span data-ttu-id="495f0-188">Activé</span><span class="sxs-lookup"><span data-stu-id="495f0-188">Enabled</span></span> |


### <a name="use-powershell-cmdlets-to-schedule-scans"></a><span data-ttu-id="495f0-189">Utiliser les cmdlets PowerShell pour planifier des analyses</span><span class="sxs-lookup"><span data-stu-id="495f0-189">Use PowerShell cmdlets to schedule scans</span></span>

<span data-ttu-id="495f0-190">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="495f0-190">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -ScanParameters
Set-MpPreference -ScanScheduleDay
Set-MpPreference -ScanScheduleTime
Set-MpPreference -RandomizeScheduleTaskTimes

```

<span data-ttu-id="495f0-191">Pour plus d’informations, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender/) Antivirus Microsoft Defender et Defender pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="495f0-191">For more information, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

### <a name="use-windows-management-instruction-wmi-to-schedule-scans"></a><span data-ttu-id="495f0-192">Utiliser Windows Management Instruction (WMI) pour planifier des analyses</span><span class="sxs-lookup"><span data-stu-id="495f0-192">Use Windows Management Instruction (WMI) to schedule scans</span></span>

<span data-ttu-id="495f0-193">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="495f0-193">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
ScanParameters
ScanScheduleDay
ScanScheduleTime
RandomizeScheduleTaskTimes
```

<span data-ttu-id="495f0-194">Pour plus d’informations et des paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="495f0-194">For more information and allowed parameters, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span></span>


## <a name="start-scheduled-scans-only-when-the-endpoint-is-not-in-use"></a><span data-ttu-id="495f0-195">Démarrer des analyses programmées uniquement lorsque le point de terminaison n’est pas en cours d’utilisation</span><span class="sxs-lookup"><span data-stu-id="495f0-195">Start scheduled scans only when the endpoint is not in use</span></span>

<span data-ttu-id="495f0-196">Vous pouvez définir l’analyse programmée de façon à ce qu’elle se produise uniquement lorsque le point de terminaison est allumé mais qu’il n’est pas utilisé avec la stratégie de groupe, PowerShell ou WMI.</span><span class="sxs-lookup"><span data-stu-id="495f0-196">You can set the scheduled scan to only occur when the endpoint is turned on but not in use with Group Policy, PowerShell, or WMI.</span></span>

> [!NOTE]
> <span data-ttu-id="495f0-197">Ces analyses ne respectent pas la configuration de limitation du processeur et tirez pleinement parti des ressources disponibles pour effectuer l’analyse aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="495f0-197">These scans will not honor the CPU throttling configuration and take full advantage of the resources available to complete the scan as fast as possible.</span></span>

### <a name="use-group-policy-to-schedule-scans"></a><span data-ttu-id="495f0-198">Utiliser une stratégie de groupe pour planifier des analyses</span><span class="sxs-lookup"><span data-stu-id="495f0-198">Use Group Policy to schedule scans</span></span>

|<span data-ttu-id="495f0-199">Lieu</span><span class="sxs-lookup"><span data-stu-id="495f0-199">Location</span></span> | <span data-ttu-id="495f0-200">Paramètre</span><span class="sxs-lookup"><span data-stu-id="495f0-200">Setting</span></span> | <span data-ttu-id="495f0-201">Description</span><span class="sxs-lookup"><span data-stu-id="495f0-201">Description</span></span> | <span data-ttu-id="495f0-202">Paramètre par défaut (s’il n’est pas configuré)</span><span class="sxs-lookup"><span data-stu-id="495f0-202">Default setting (if not configured)</span></span> |
|:---|:---|:---|:---|
|<span data-ttu-id="495f0-203">Analyser</span><span class="sxs-lookup"><span data-stu-id="495f0-203">Scan</span></span> | <span data-ttu-id="495f0-204">Démarrer l’analyse programmée uniquement lorsque l’ordinateur est en cours d’utilisation</span><span class="sxs-lookup"><span data-stu-id="495f0-204">Start the scheduled scan only when computer is on but not in use</span></span> | <span data-ttu-id="495f0-205">Les analyses programmées ne s’exécutent pas, sauf si l’ordinateur est en cours d’utilisation</span><span class="sxs-lookup"><span data-stu-id="495f0-205">Scheduled scans will not run, unless the computer is on but not in use</span></span> | <span data-ttu-id="495f0-206">Activé</span><span class="sxs-lookup"><span data-stu-id="495f0-206">Enabled</span></span> |

### <a name="use-powershell-cmdlets"></a><span data-ttu-id="495f0-207">Utiliser les cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="495f0-207">Use PowerShell cmdlets</span></span>

<span data-ttu-id="495f0-208">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="495f0-208">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -ScanOnlyIfIdleEnabled
```

<span data-ttu-id="495f0-209">Pour plus d’informations, [voir Utiliser les cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter les [cmdlets](/powershell/module/defender/)Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="495f0-209">For more information, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/).</span></span>

### <a name="use-windows-management-instruction-wmi"></a><span data-ttu-id="495f0-210">Utiliser Windows Management Instruction (WMI)</span><span class="sxs-lookup"><span data-stu-id="495f0-210">Use Windows Management Instruction (WMI)</span></span>

<span data-ttu-id="495f0-211">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="495f0-211">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
ScanOnlyIfIdleEnabled
```

<span data-ttu-id="495f0-212">Pour plus d’informations sur les API et les paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span><span class="sxs-lookup"><span data-stu-id="495f0-212">For more information about APIs and allowed parameters, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span></span>

<a id="remed"></a>
## <a name="configure-when-full-scans-should-be-run-to-complete-remediation"></a><span data-ttu-id="495f0-213">Configurer le moment où les analyses complètes doivent être exécutés pour terminer la correction</span><span class="sxs-lookup"><span data-stu-id="495f0-213">Configure when full scans should be run to complete remediation</span></span>

<span data-ttu-id="495f0-214">Certaines menaces peuvent nécessiter une analyse complète pour terminer leur suppression et leur correction.</span><span class="sxs-lookup"><span data-stu-id="495f0-214">Some threats might require a full scan to complete their removal and remediation.</span></span> <span data-ttu-id="495f0-215">Vous pouvez spécifier quand ces analyses doivent se produire avec la stratégie de groupe, PowerShell ou WMI.</span><span class="sxs-lookup"><span data-stu-id="495f0-215">You can specify when these scans should occur with Group Policy, PowerShell, or WMI.</span></span>

### <a name="use-group-policy-to-schedule-remediation-required-scans"></a><span data-ttu-id="495f0-216">Utiliser une stratégie de groupe pour planifier des analyses requises pour la correction</span><span class="sxs-lookup"><span data-stu-id="495f0-216">Use Group Policy to schedule remediation-required scans</span></span>

| <span data-ttu-id="495f0-217">Lieu</span><span class="sxs-lookup"><span data-stu-id="495f0-217">Location</span></span> | <span data-ttu-id="495f0-218">Paramètre</span><span class="sxs-lookup"><span data-stu-id="495f0-218">Setting</span></span> | <span data-ttu-id="495f0-219">Description</span><span class="sxs-lookup"><span data-stu-id="495f0-219">Description</span></span> | <span data-ttu-id="495f0-220">Paramètre par défaut (s’il n’est pas configuré)</span><span class="sxs-lookup"><span data-stu-id="495f0-220">Default setting (if not configured)</span></span> |
|---|---|---|---|
|<span data-ttu-id="495f0-221">Correction</span><span class="sxs-lookup"><span data-stu-id="495f0-221">Remediation</span></span> | <span data-ttu-id="495f0-222">Spécifier le jour de la semaine pour exécuter une analyse complète programmée afin de terminer la correction</span><span class="sxs-lookup"><span data-stu-id="495f0-222">Specify the day of the week to run a scheduled full scan to complete remediation</span></span> | <span data-ttu-id="495f0-223">Spécifiez le jour (ou jamais) d’exécuter une analyse.</span><span class="sxs-lookup"><span data-stu-id="495f0-223">Specify the day (or never) to run a scan.</span></span> | <span data-ttu-id="495f0-224">Jamais</span><span class="sxs-lookup"><span data-stu-id="495f0-224">Never</span></span> |
|<span data-ttu-id="495f0-225">Correction</span><span class="sxs-lookup"><span data-stu-id="495f0-225">Remediation</span></span> | <span data-ttu-id="495f0-226">Spécifier l’heure de la journée pour exécuter une analyse complète programmée afin de terminer la correction</span><span class="sxs-lookup"><span data-stu-id="495f0-226">Specify the time of day to run a scheduled full scan to complete remediation</span></span> | <span data-ttu-id="495f0-227">Spécifiez le nombre de minutes après minuit (par exemple, entrez **60** pour 1 h 00)</span><span class="sxs-lookup"><span data-stu-id="495f0-227">Specify the number of minutes after midnight (for example, enter **60** for 1 a.m.)</span></span> | <span data-ttu-id="495f0-228">2 h 00</span><span class="sxs-lookup"><span data-stu-id="495f0-228">2 a.m.</span></span> |

### <a name="use-powershell-cmdlets"></a><span data-ttu-id="495f0-229">Utiliser les cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="495f0-229">Use PowerShell cmdlets</span></span>

<span data-ttu-id="495f0-230">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="495f0-230">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -RemediationScheduleDay
Set-MpPreference -RemediationScheduleTime
```

<span data-ttu-id="495f0-231">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, voir utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender/) Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="495f0-231">See [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

### <a name="use-windows-management-instruction-wmi"></a><span data-ttu-id="495f0-232">Utiliser Windows Management Instruction (WMI)</span><span class="sxs-lookup"><span data-stu-id="495f0-232">Use Windows Management Instruction (WMI)</span></span>

<span data-ttu-id="495f0-233">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="495f0-233">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
RemediationScheduleDay
RemediationScheduleTime
```

<span data-ttu-id="495f0-234">Pour plus d’informations et les paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span><span class="sxs-lookup"><span data-stu-id="495f0-234">For more information and allowed parameters, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span></span>


## <a name="set-up-daily-quick-scans"></a><span data-ttu-id="495f0-235">Configurer des analyses rapides quotidiennes</span><span class="sxs-lookup"><span data-stu-id="495f0-235">Set up daily quick scans</span></span>

<span data-ttu-id="495f0-236">Vous pouvez activer une analyse rapide quotidienne qui peut être exécuté en plus de vos autres analyses programmées avec la stratégie de groupe, PowerShell ou WMI.</span><span class="sxs-lookup"><span data-stu-id="495f0-236">You can enable a daily quick scan that can be run in addition to your other scheduled scans with Group Policy, PowerShell, or WMI.</span></span>

### <a name="use-group-policy-to-schedule-daily-scans"></a><span data-ttu-id="495f0-237">Utiliser une stratégie de groupe pour planifier des analyses quotidiennes</span><span class="sxs-lookup"><span data-stu-id="495f0-237">Use Group Policy to schedule daily scans</span></span>

|<span data-ttu-id="495f0-238">Lieu</span><span class="sxs-lookup"><span data-stu-id="495f0-238">Location</span></span> | <span data-ttu-id="495f0-239">Paramètre</span><span class="sxs-lookup"><span data-stu-id="495f0-239">Setting</span></span> | <span data-ttu-id="495f0-240">Description</span><span class="sxs-lookup"><span data-stu-id="495f0-240">Description</span></span> | <span data-ttu-id="495f0-241">Paramètre par défaut (s’il n’est pas configuré)</span><span class="sxs-lookup"><span data-stu-id="495f0-241">Default setting (if not configured)</span></span> |
|:---|:---|:---|:---|
|<span data-ttu-id="495f0-242">Analyser</span><span class="sxs-lookup"><span data-stu-id="495f0-242">Scan</span></span> | <span data-ttu-id="495f0-243">Spécifier l’intervalle pour exécuter des analyses rapides par jour</span><span class="sxs-lookup"><span data-stu-id="495f0-243">Specify the interval to run quick scans per day</span></span> | <span data-ttu-id="495f0-244">Spécifiez le nombre d’heures devant s’écoulée avant la prochaine analyse rapide.</span><span class="sxs-lookup"><span data-stu-id="495f0-244">Specify how many hours should elapse before the next quick scan.</span></span> <span data-ttu-id="495f0-245">Par exemple, pour exécuter toutes les deux heures, entrez **2**, pour une fois par jour, **entrez 24**.</span><span class="sxs-lookup"><span data-stu-id="495f0-245">For example, to run every two hours, enter **2**, for once a day, enter **24**.</span></span> <span data-ttu-id="495f0-246">Entrez **0 pour** ne jamais exécuter une analyse rapide quotidienne.</span><span class="sxs-lookup"><span data-stu-id="495f0-246">Enter **0** to never run a daily quick scan.</span></span> | <span data-ttu-id="495f0-247">Jamais</span><span class="sxs-lookup"><span data-stu-id="495f0-247">Never</span></span> |
|<span data-ttu-id="495f0-248">Analyser</span><span class="sxs-lookup"><span data-stu-id="495f0-248">Scan</span></span> | <span data-ttu-id="495f0-249">Spécifier l’heure d’une analyse rapide quotidienne</span><span class="sxs-lookup"><span data-stu-id="495f0-249">Specify the time for a daily quick scan</span></span> | <span data-ttu-id="495f0-250">Spécifiez le nombre de minutes après minuit (par exemple, entrez **60** pour 1 h 00)</span><span class="sxs-lookup"><span data-stu-id="495f0-250">Specify the number of minutes after midnight (for example, enter **60** for 1 a.m.)</span></span> | <span data-ttu-id="495f0-251">2 h 00</span><span class="sxs-lookup"><span data-stu-id="495f0-251">2 a.m.</span></span> |

### <a name="use-powershell-cmdlets-to-schedule-daily-scans"></a><span data-ttu-id="495f0-252">Utiliser les cmdlets PowerShell pour planifier des analyses quotidiennes</span><span class="sxs-lookup"><span data-stu-id="495f0-252">Use PowerShell cmdlets to schedule daily scans</span></span>

<span data-ttu-id="495f0-253">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="495f0-253">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -ScanScheduleQuickScanTime
```

<span data-ttu-id="495f0-254">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender/)Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="495f0-254">For more information about how to use PowerShell with Microsoft Defender Antivirus, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/).</span></span>

### <a name="use-windows-management-instruction-wmi-to-schedule-daily-scans"></a><span data-ttu-id="495f0-255">Utiliser Windows Management Instruction (WMI) pour planifier des analyses quotidiennes</span><span class="sxs-lookup"><span data-stu-id="495f0-255">Use Windows Management Instruction (WMI) to schedule daily scans</span></span>

<span data-ttu-id="495f0-256">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="495f0-256">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
ScanScheduleQuickScanTime
```

<span data-ttu-id="495f0-257">Pour plus d’informations et les paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span><span class="sxs-lookup"><span data-stu-id="495f0-257">For more information and allowed parameters, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span></span>


## <a name="enable-scans-after-protection-updates"></a><span data-ttu-id="495f0-258">Activer les analyses après les mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="495f0-258">Enable scans after protection updates</span></span>

<span data-ttu-id="495f0-259">Vous pouvez forcer l’analyse après chaque mise à jour [de la protection](manage-protection-updates-microsoft-defender-antivirus.md) avec la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="495f0-259">You can force a scan to occur after every [protection update](manage-protection-updates-microsoft-defender-antivirus.md) with Group Policy.</span></span>

### <a name="use-group-policy-to-schedule-scans-after-protection-updates"></a><span data-ttu-id="495f0-260">Utiliser la stratégie de groupe pour planifier des analyses après les mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="495f0-260">Use Group Policy to schedule scans after protection updates</span></span>

|<span data-ttu-id="495f0-261">Lieu</span><span class="sxs-lookup"><span data-stu-id="495f0-261">Location</span></span> | <span data-ttu-id="495f0-262">Paramètre</span><span class="sxs-lookup"><span data-stu-id="495f0-262">Setting</span></span> | <span data-ttu-id="495f0-263">Description</span><span class="sxs-lookup"><span data-stu-id="495f0-263">Description</span></span> | <span data-ttu-id="495f0-264">Paramètre par défaut (s’il n’est pas configuré)</span><span class="sxs-lookup"><span data-stu-id="495f0-264">Default setting (if not configured)</span></span>|
|:---|:---|:---|:---|
|<span data-ttu-id="495f0-265">Mises à jour des signatures</span><span class="sxs-lookup"><span data-stu-id="495f0-265">Signature updates</span></span> | <span data-ttu-id="495f0-266">Activer l’analyse après la mise à jour des informations de sécurité</span><span class="sxs-lookup"><span data-stu-id="495f0-266">Turn on scan after Security intelligence update</span></span> | <span data-ttu-id="495f0-267">Une analyse se produit immédiatement après le téléchargement d’une nouvelle mise à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="495f0-267">A scan will occur immediately after a new protection update is downloaded</span></span> | <span data-ttu-id="495f0-268">Activé</span><span class="sxs-lookup"><span data-stu-id="495f0-268">Enabled</span></span> |

## <a name="see-also"></a><span data-ttu-id="495f0-269">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="495f0-269">See also</span></span>

- [<span data-ttu-id="495f0-270">Empêcher ou autoriser les utilisateurs à modifier localement les paramètres de stratégie</span><span class="sxs-lookup"><span data-stu-id="495f0-270">Prevent or allow users to locally modify policy settings</span></span>](configure-local-policy-overrides-microsoft-defender-antivirus.md)
- <span data-ttu-id="495f0-271">[Configurer et exécuter des analyses à la demande avec l’antivirus Microsoft Defender](run-scan-microsoft-defender-antivirus.md).</span><span class="sxs-lookup"><span data-stu-id="495f0-271">[Configure and run on-demand Microsoft Defender Antivirus scans](run-scan-microsoft-defender-antivirus.md)</span></span>
- [<span data-ttu-id="495f0-272">Configurer les options d’analyse de l’antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="495f0-272">Configure Microsoft Defender Antivirus scanning options</span></span>](configure-advanced-scan-types-microsoft-defender-antivirus.md)
- [<span data-ttu-id="495f0-273">Gérer les mises Antivirus Microsoft Defender jour et appliquer les lignes de base</span><span class="sxs-lookup"><span data-stu-id="495f0-273">Manage Microsoft Defender Antivirus updates and apply baselines</span></span>](manage-updates-baselines-microsoft-defender-antivirus.md)
- [<span data-ttu-id="495f0-274">Gérer le moment où les mises à jour de protection doivent être téléchargées et appliquées</span><span class="sxs-lookup"><span data-stu-id="495f0-274">Manage when protection updates should be downloaded and applied</span></span>](manage-protection-update-schedule-microsoft-defender-antivirus.md) 
- [<span data-ttu-id="495f0-275">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="495f0-275">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)