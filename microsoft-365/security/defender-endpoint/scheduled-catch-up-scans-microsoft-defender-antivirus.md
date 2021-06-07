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
ms.date: 06/04/2021
ms.reviewer: pauhijbr, ksarens
manager: dansimp
ms.technology: mde
ms.topic: how-to
ms.openlocfilehash: f1344026878b7fbd6242d82b1afb0e6671c32073
ms.sourcegitcommit: b09aee96a1e2266b33ba81dfe497f24c5300bb56
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2021
ms.locfileid: "52789267"
---
# <a name="configure-scheduled-quick-or-full-microsoft-defender-antivirus-scans"></a><span data-ttu-id="84741-104">Configurer des analyses antivirus Microsoft Defender rapides ou complètes</span><span class="sxs-lookup"><span data-stu-id="84741-104">Configure scheduled quick or full Microsoft Defender Antivirus scans</span></span>

<span data-ttu-id="84741-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="84741-105">**Applies to:**</span></span>

- [<span data-ttu-id="84741-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="84741-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)


> [!NOTE]
> <span data-ttu-id="84741-107">Par défaut, Antivirus Microsoft Defender recherche une mise à jour 15 minutes avant l’heure des analyses programmées.</span><span class="sxs-lookup"><span data-stu-id="84741-107">By default, Microsoft Defender Antivirus checks for an update 15 minutes before the time of any scheduled scans.</span></span> <span data-ttu-id="84741-108">Vous pouvez [gérer la planification du téléchargement](manage-protection-update-schedule-microsoft-defender-antivirus.md) et de l’application des mises à jour de la protection pour remplacer cette valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="84741-108">You can [Manage the schedule for when protection updates should be downloaded and applied](manage-protection-update-schedule-microsoft-defender-antivirus.md) to override this default.</span></span> 

<span data-ttu-id="84741-109">Outre la protection en temps réel toujours en cours et les [analyses](run-scan-microsoft-defender-antivirus.md) à la demande, vous pouvez configurer des analyses régulières et programmées.</span><span class="sxs-lookup"><span data-stu-id="84741-109">In addition to always-on real-time protection and [on-demand](run-scan-microsoft-defender-antivirus.md) scans, you can set up regular, scheduled scans.</span></span> 

<span data-ttu-id="84741-110">Vous pouvez configurer le type d’analyse, le moment où l’analyse doit se produire et si l’analyse doit se produire après une mise à jour de [la protection](manage-protection-updates-microsoft-defender-antivirus.md) ou si le point de terminaison est utilisé.</span><span class="sxs-lookup"><span data-stu-id="84741-110">You can configure the type of scan, when the scan should occur, and if the scan should occur after a [protection update](manage-protection-updates-microsoft-defender-antivirus.md) or if the endpoint is being used.</span></span> <span data-ttu-id="84741-111">Vous pouvez également spécifier le moment où des analyses spéciales doivent être nécessaires pour terminer la correction.</span><span class="sxs-lookup"><span data-stu-id="84741-111">You can also specify when special scans to complete remediation should occur.</span></span>

<span data-ttu-id="84741-112">Cet article explique comment configurer des analyses programmées avec la stratégie de groupe, les cmdlets PowerShell et WMI.</span><span class="sxs-lookup"><span data-stu-id="84741-112">This article describes how to configure scheduled scans with Group Policy, PowerShell cmdlets, and WMI.</span></span> <span data-ttu-id="84741-113">Vous pouvez également configurer des analyses de planifications [avec Microsoft Endpoint Configuration Manager](/configmgr/protect/deploy-use/endpoint-antimalware-policies#scheduled-scans-settings) ou [Microsoft Intune](/mem/intune/configuration/device-restrictions-windows-10).</span><span class="sxs-lookup"><span data-stu-id="84741-113">You can also configure schedules scans with [Microsoft Endpoint Configuration Manager](/configmgr/protect/deploy-use/endpoint-antimalware-policies#scheduled-scans-settings) or [Microsoft Intune](/mem/intune/configuration/device-restrictions-windows-10).</span></span>

## <a name="to-configure-the-group-policy-settings-described-in-this-article"></a><span data-ttu-id="84741-114">Pour configurer les paramètres de stratégie de groupe décrits dans cet article</span><span class="sxs-lookup"><span data-stu-id="84741-114">To configure the Group Policy settings described in this article</span></span>

1. <span data-ttu-id="84741-115">Sur votre ordinateur de gestion des stratégies de groupe, dans l’Éditeur de stratégie de groupe, allez à Modèles d’administration de **configuration** ordinateur  >    >  **Windows composants**  >    >  **Antivirus Microsoft Defender’analyse.**</span><span class="sxs-lookup"><span data-stu-id="84741-115">On your Group Policy management machine, in the Group Policy Editor, go to **Computer configuration** > **Administrative Templates** > **Windows Components** > **Microsoft Defender Antivirus** > **Scan**.</span></span>

2. <span data-ttu-id="84741-116">Cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous souhaitez configurer, puis sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="84741-116">Right-click the Group Policy Object you want to configure, and then select **Edit**.</span></span>

3. <span data-ttu-id="84741-117">Spécifiez les paramètres de l’objet de stratégie de groupe, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="84741-117">Specify settings for the Group Policy Object, and then select **OK**.</span></span> 

4. <span data-ttu-id="84741-118">Répétez les étapes 1 à 4 pour chaque paramètre à configurer.</span><span class="sxs-lookup"><span data-stu-id="84741-118">Repeat steps 1-4 for each setting you want to configure.</span></span>

5. <span data-ttu-id="84741-119">Déployez votre objet de stratégie de groupe comme vous le faites normalement.</span><span class="sxs-lookup"><span data-stu-id="84741-119">Deploy your Group Policy Object as you normally do.</span></span> <span data-ttu-id="84741-120">Si vous avez besoin d’aide sur les objets de stratégie de groupe, voir [Créer un objet de stratégie de groupe.](/windows/security/threat-protection/windows-firewall/create-a-group-policy-object)</span><span class="sxs-lookup"><span data-stu-id="84741-120">If you need help with Group Policy Objects, see [Create a Group Policy Object](/windows/security/threat-protection/windows-firewall/create-a-group-policy-object).</span></span>

<span data-ttu-id="84741-121">Consultez également la rubrique Gérer quand les mises à jour de [la protection](manage-protection-update-schedule-microsoft-defender-antivirus.md) doivent être téléchargées et appliquées, et empêcher ou autoriser les utilisateurs à modifier localement les [paramètres de](configure-local-policy-overrides-microsoft-defender-antivirus.md) stratégie.</span><span class="sxs-lookup"><span data-stu-id="84741-121">Also see the [Manage when protection updates should be downloaded and applied](manage-protection-update-schedule-microsoft-defender-antivirus.md) and [Prevent or allow users to locally modify policy settings](configure-local-policy-overrides-microsoft-defender-antivirus.md) topics.</span></span>

## <a name="quick-scan-versus-full-scan-and-custom-scan"></a><span data-ttu-id="84741-122">Analyse rapide par rapport à l’analyse complète et à l’analyse personnalisée</span><span class="sxs-lookup"><span data-stu-id="84741-122">Quick scan versus full scan and custom scan</span></span>

<span data-ttu-id="84741-123">Lorsque vous définissez des analyses programmées, vous pouvez définir si l’analyse doit être une analyse complète ou rapide.</span><span class="sxs-lookup"><span data-stu-id="84741-123">When you set up scheduled scans, you can set up whether the scan should be a full or quick scan.</span></span>


|<span data-ttu-id="84741-124">Analyse rapide</span><span class="sxs-lookup"><span data-stu-id="84741-124">Quick scan</span></span>  |<span data-ttu-id="84741-125">Analyse complète</span><span class="sxs-lookup"><span data-stu-id="84741-125">Full scan</span></span>  | <span data-ttu-id="84741-126">Analyse personnalisée</span><span class="sxs-lookup"><span data-stu-id="84741-126">Custom scan</span></span> |
|---------|---------|---------|
|<span data-ttu-id="84741-127">Une analyse rapide examine tous les emplacements où des programmes malveillants peuvent être enregistrés pour démarrer avec le système, tels que les clés de Registre et les dossiers de démarrage Windows connus.</span><span class="sxs-lookup"><span data-stu-id="84741-127">A quick scan looks at all the locations where there could be malware registered to start with the system, such as registry keys and known Windows startup folders.</span></span> <p><span data-ttu-id="84741-128">Dans la plupart des cas, une analyse rapide est suffisante et est recommandée pour les analyses programmées.</span><span class="sxs-lookup"><span data-stu-id="84741-128">In most cases, a quick scan is sufficient and is recommended for scheduled scans.</span></span> |<span data-ttu-id="84741-129">Une analyse complète commence par l’exécution d’une analyse rapide, puis se poursuit avec une analyse séquentielle de tous les disques fixes montés et lecteurs amovibles/réseau (si l’analyse complète est configurée pour le faire).</span><span class="sxs-lookup"><span data-stu-id="84741-129">A full scan starts by running a quick scan and then continues with a sequential file scan of all mounted fixed disks and removable/network drives (if the full scan is configured to do so).</span></span> <p><span data-ttu-id="84741-130">L’analyse complète peut prendre quelques heures ou jours, en fonction de la quantité et du type de données à analyser.</span><span class="sxs-lookup"><span data-stu-id="84741-130">A full scan can take a few hours or days to complete, depending on the amount and type of data that needs to be scanned.</span></span><p><span data-ttu-id="84741-131">Une fois l’analyse complète terminée, de nouvelles informations de sécurité sont disponibles et une nouvelle analyse est nécessaire pour s’assurer qu’aucune autre menace n’est détectée avec la nouvelle intelligence de sécurité.</span><span class="sxs-lookup"><span data-stu-id="84741-131">When the full scan is complete, new security intelligence is available, and a new scan is required to make sure that no other threats are detected with the new security intelligence.</span></span>   | <span data-ttu-id="84741-132">Une analyse personnalisée est une analyse rapide qui s’exécute sur les fichiers et dossiers que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="84741-132">A custom scan is a quick scan that runs on the files and folders you specify.</span></span> <span data-ttu-id="84741-133">Par exemple, vous pouvez choisir d’analyser un lecteur USB ou un dossier spécifique sur le lecteur local de votre appareil.</span><span class="sxs-lookup"><span data-stu-id="84741-133">For example, you can opt to scan a USB drive, or a specific folder on your device's local drive.</span></span> <p> | 

>[!NOTE]
><span data-ttu-id="84741-134">Par défaut, les analyses rapides s’exécutent sur des appareils amovibles montés, tels que des lecteurs USB.</span><span class="sxs-lookup"><span data-stu-id="84741-134">By default, quick scans run on mounted removable devices, such as USB drives.</span></span>

### <a name="how-do-i-know-which-scan-type-to-choose"></a><span data-ttu-id="84741-135">Comment savoir quel type d’analyse choisir ?</span><span class="sxs-lookup"><span data-stu-id="84741-135">How do I know which scan type to choose?</span></span>

<span data-ttu-id="84741-136">Utilisez le tableau suivant pour choisir un type d’analyse.</span><span class="sxs-lookup"><span data-stu-id="84741-136">Use the following table to choose a scan type.</span></span>


|<span data-ttu-id="84741-137">Scénario</span><span class="sxs-lookup"><span data-stu-id="84741-137">Scenario</span></span>  |<span data-ttu-id="84741-138">Type d’analyse recommandé</span><span class="sxs-lookup"><span data-stu-id="84741-138">Recommended scan type</span></span>  |
|---------|---------|
|<span data-ttu-id="84741-139">Vous souhaitez configurer des analyses régulières et programmées</span><span class="sxs-lookup"><span data-stu-id="84741-139">You want to set up regular, scheduled scans</span></span>     | <span data-ttu-id="84741-140">Analyse rapide</span><span class="sxs-lookup"><span data-stu-id="84741-140">Quick scan</span></span> <p><span data-ttu-id="84741-141">Une analyse rapide vérifie les processus, la mémoire, les profils et certains emplacements de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="84741-141">A quick scan checks the processes, memory, profiles, and certain locations on the device.</span></span> <span data-ttu-id="84741-142">Combinée à [une protection en](configure-real-time-protection-microsoft-defender-antivirus.md)temps réel toujours en cours, une analyse rapide permet d’assurer une couverture forte à la fois pour les programmes malveillants qui commencent par le système et les programmes malveillants au niveau du noyau.</span><span class="sxs-lookup"><span data-stu-id="84741-142">Combined with [always-on real-time protection](configure-real-time-protection-microsoft-defender-antivirus.md), a quick scan helps provide strong coverage both for malware that starts with the system and kernel-level malware.</span></span> <span data-ttu-id="84741-143">La protection en temps réel examine les fichiers lorsqu’ils sont ouverts et fermés, et chaque fois qu’un utilisateur navigue vers un dossier.</span><span class="sxs-lookup"><span data-stu-id="84741-143">Real-time protection reviews files when they are opened and closed, and whenever a user navigates to a folder.</span></span>         |
|<span data-ttu-id="84741-144">Les menaces, telles que les programmes malveillants, sont détectées sur un appareil individuel</span><span class="sxs-lookup"><span data-stu-id="84741-144">Threats, such as malware, are detected on an individual device</span></span>     | <span data-ttu-id="84741-145">Analyse rapide</span><span class="sxs-lookup"><span data-stu-id="84741-145">Quick scan</span></span> <p><span data-ttu-id="84741-146">Dans la plupart des cas, une analyse rapide permet de détecter et de nettoyer les programmes malveillants détectés.</span><span class="sxs-lookup"><span data-stu-id="84741-146">In most cases, a quick scan will catch and clean up detected malware.</span></span>   |
|<span data-ttu-id="84741-147">Vous souhaitez exécuter une [analyse à la demande](run-scan-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="84741-147">You want to run an [on-demand scan](run-scan-microsoft-defender-antivirus.md)</span></span>     | <span data-ttu-id="84741-148">Analyse rapide</span><span class="sxs-lookup"><span data-stu-id="84741-148">Quick scan</span></span>       |
| <span data-ttu-id="84741-149">Vous souhaitez vous assurer qu’un appareil portable, tel qu’un lecteur USB, ne contient pas de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="84741-149">You want to make sure a portable device, such as a USB drive, does not contain malware</span></span> | <span data-ttu-id="84741-150">Analyse personnalisée</span><span class="sxs-lookup"><span data-stu-id="84741-150">Custom scan</span></span> <p><span data-ttu-id="84741-151">Une analyse personnalisée vous permet de sélectionner des emplacements, dossiers ou fichiers spécifiques et exécute une analyse rapide.</span><span class="sxs-lookup"><span data-stu-id="84741-151">A custom scan enables you to select specific locations, folders, or files and runs a quick scan.</span></span> |

### <a name="what-else-do-i-need-to-know-about-quick-and-full-scans"></a><span data-ttu-id="84741-152">Que dois-je savoir d’autre sur les analyses rapides et complètes ?</span><span class="sxs-lookup"><span data-stu-id="84741-152">What else do I need to know about quick and full scans?</span></span>

- <span data-ttu-id="84741-153">Les fichiers malveillants peuvent être stockés dans des emplacements qui ne sont pas inclus dans une analyse rapide.</span><span class="sxs-lookup"><span data-stu-id="84741-153">Malicious files can be stored in locations that are not included in a quick scan.</span></span> <span data-ttu-id="84741-154">Toutefois, la protection en temps réel toujours en cours examine tous les fichiers ouverts et fermés, ainsi que tous les fichiers qui se contiennent dans des dossiers accessibles par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="84741-154">However, always-on real-time protection reviews all files that are opened and closed, and any files that are in folders that are accessed by a user.</span></span> <span data-ttu-id="84741-155">La combinaison d’une protection en temps réel et d’une analyse rapide permet de fournir une protection forte contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="84741-155">The combination of real-time protection and a quick scan helps provide strong protection against malware.</span></span>

- <span data-ttu-id="84741-156">La protection à l’accès avec une protection assurée par le [cloud](cloud-protection-microsoft-defender-antivirus.md) permet de s’assurer que tous les fichiers accessibles sur le système sont analysés avec les dernières informations de sécurité et les derniers modèles d’apprentissage automatique dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="84741-156">On-access protection with [cloud-delivered protection](cloud-protection-microsoft-defender-antivirus.md) helps ensure that all the files accessed on the system are being scanned with the latest security intelligence and cloud machine learning models.</span></span>

- <span data-ttu-id="84741-157">Lorsque la protection en temps réel détecte des programmes malveillants et que l’étendue des fichiers affectés n’est pas déterminée initialement, Antivirus Microsoft Defender lance une analyse complète dans le cadre du processus de correction.</span><span class="sxs-lookup"><span data-stu-id="84741-157">When real-time protection detects malware and the extent of the affected files is not determined initially, Microsoft Defender Antivirus initiates a full scan as part of the remediation process.</span></span>

- <span data-ttu-id="84741-158">Une analyse complète peut détecter des fichiers malveillants qui n’ont pas été détectés par d’autres analyses, telles qu’une analyse rapide.</span><span class="sxs-lookup"><span data-stu-id="84741-158">A full scan can detect malicious files that were not detected by other scans, such as a quick scan.</span></span> <span data-ttu-id="84741-159">Toutefois, une analyse complète peut prendre un certain temps et utiliser des ressources système précieuses pour se terminer.</span><span class="sxs-lookup"><span data-stu-id="84741-159">However, a full scan can take a while and use valuable system resources to complete.</span></span>

- <span data-ttu-id="84741-160">Si un appareil est hors connexion pendant une période prolongée, une analyse complète peut prendre plus de temps.</span><span class="sxs-lookup"><span data-stu-id="84741-160">If a device is offline for an extended period of time, a full scan can take longer to complete.</span></span> 

## <a name="set-up-scheduled-scans"></a><span data-ttu-id="84741-161">Configurer des analyses programmées</span><span class="sxs-lookup"><span data-stu-id="84741-161">Set up scheduled scans</span></span>

<span data-ttu-id="84741-162">Les analyses programmées s’exécutent le jour et l’heure que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="84741-162">Scheduled scans run on the day and time that you specify.</span></span> <span data-ttu-id="84741-163">Vous pouvez utiliser la stratégie de groupe, PowerShell et WMI pour configurer des analyses programmées.</span><span class="sxs-lookup"><span data-stu-id="84741-163">You can use Group Policy, PowerShell, and WMI to configure scheduled scans.</span></span>

> [!NOTE]
> <span data-ttu-id="84741-164">Si un appareil est débranché et s’exécute sur batterie pendant une analyse complète programmée, l’analyse programmée s’arrête avec l’événement 1002, qui indique que l’analyse s’est arrêtée avant la fin.</span><span class="sxs-lookup"><span data-stu-id="84741-164">If a device is unplugged and running on battery during a scheduled full scan, the scheduled scan will stop with event 1002, which states that the scan stopped before completion.</span></span> <span data-ttu-id="84741-165">Antivirus Microsoft Defender exécutera une analyse complète à l’heure prévue suivante.</span><span class="sxs-lookup"><span data-stu-id="84741-165">Microsoft Defender Antivirus will run a full scan at the next scheduled time.</span></span>

### <a name="use-group-policy-to-schedule-scans"></a><span data-ttu-id="84741-166">Utiliser une stratégie de groupe pour planifier des analyses</span><span class="sxs-lookup"><span data-stu-id="84741-166">Use Group Policy to schedule scans</span></span>

|<span data-ttu-id="84741-167">Emplacement</span><span class="sxs-lookup"><span data-stu-id="84741-167">Location</span></span> | <span data-ttu-id="84741-168">Paramètre</span><span class="sxs-lookup"><span data-stu-id="84741-168">Setting</span></span> | <span data-ttu-id="84741-169">Description</span><span class="sxs-lookup"><span data-stu-id="84741-169">Description</span></span> | <span data-ttu-id="84741-170">Paramètre par défaut (s’il n’est pas configuré)</span><span class="sxs-lookup"><span data-stu-id="84741-170">Default setting (if not configured)</span></span> |
|:---|:---|:---|:---|
|<span data-ttu-id="84741-171">Analyser</span><span class="sxs-lookup"><span data-stu-id="84741-171">Scan</span></span> | <span data-ttu-id="84741-172">Spécifier le type d’analyse à utiliser pour une analyse programmée</span><span class="sxs-lookup"><span data-stu-id="84741-172">Specify the scan type to use for a scheduled scan</span></span> | <span data-ttu-id="84741-173">Analyse rapide</span><span class="sxs-lookup"><span data-stu-id="84741-173">Quick scan</span></span> |
|<span data-ttu-id="84741-174">Analyser</span><span class="sxs-lookup"><span data-stu-id="84741-174">Scan</span></span> | <span data-ttu-id="84741-175">Spécifier le jour de la semaine pour exécuter une analyse programmée</span><span class="sxs-lookup"><span data-stu-id="84741-175">Specify the day of the week to run a scheduled scan</span></span> | <span data-ttu-id="84741-176">Spécifiez le jour (ou jamais) d’exécuter une analyse.</span><span class="sxs-lookup"><span data-stu-id="84741-176">Specify the day (or never) to run a scan.</span></span> | <span data-ttu-id="84741-177">Jamais</span><span class="sxs-lookup"><span data-stu-id="84741-177">Never</span></span> |
|<span data-ttu-id="84741-178">Analyser</span><span class="sxs-lookup"><span data-stu-id="84741-178">Scan</span></span> | <span data-ttu-id="84741-179">Spécifier l’heure de la journée pour exécuter une analyse programmée</span><span class="sxs-lookup"><span data-stu-id="84741-179">Specify the time of day to run a scheduled scan</span></span> | <span data-ttu-id="84741-180">Spécifiez le nombre de minutes après minuit (par exemple, entrez **60** pour 1 h).</span><span class="sxs-lookup"><span data-stu-id="84741-180">Specify the number of minutes after midnight (for example, enter **60** for 1 a.m.).</span></span> | <span data-ttu-id="84741-181">2 h 00</span><span class="sxs-lookup"><span data-stu-id="84741-181">2 a.m.</span></span> |
|<span data-ttu-id="84741-182">Root</span><span class="sxs-lookup"><span data-stu-id="84741-182">Root</span></span> | <span data-ttu-id="84741-183">Randomize scheduled task times</span><span class="sxs-lookup"><span data-stu-id="84741-183">Randomize scheduled task times</span></span> |<span data-ttu-id="84741-184">In Antivirus Microsoft Defender, randomize the start time of the scan to any interval from 0 to 4 hours.</span><span class="sxs-lookup"><span data-stu-id="84741-184">In Microsoft Defender Antivirus, randomize the start time of the scan to any interval from 0 to 4 hours.</span></span> <p><span data-ttu-id="84741-185">Dans [SCEP](/mem/intune/protect/certificates-scep-configure), rendre aléatoires les analyses à n’importe quel intervalle plus ou moins 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="84741-185">In [SCEP](/mem/intune/protect/certificates-scep-configure), randomize scans to any interval plus or minus 30 minutes.</span></span> <span data-ttu-id="84741-186">Cela peut être utile dans les machines virtuelles ou les déploiements VDI.</span><span class="sxs-lookup"><span data-stu-id="84741-186">This can be useful in virtual machines or VDI deployments.</span></span> | <span data-ttu-id="84741-187">Activé</span><span class="sxs-lookup"><span data-stu-id="84741-187">Enabled</span></span> |


### <a name="use-powershell-cmdlets-to-schedule-scans"></a><span data-ttu-id="84741-188">Utiliser les cmdlets PowerShell pour planifier des analyses</span><span class="sxs-lookup"><span data-stu-id="84741-188">Use PowerShell cmdlets to schedule scans</span></span>

<span data-ttu-id="84741-189">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="84741-189">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -ScanParameters
Set-MpPreference -ScanScheduleDay
Set-MpPreference -ScanScheduleTime
Set-MpPreference -RandomizeScheduleTaskTimes

```

<span data-ttu-id="84741-190">Pour plus d’informations, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender/) Antivirus Microsoft Defender et Defender pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="84741-190">For more information, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

### <a name="use-windows-management-instruction-wmi-to-schedule-scans"></a><span data-ttu-id="84741-191">Utiliser Windows Management Instruction (WMI) pour planifier des analyses</span><span class="sxs-lookup"><span data-stu-id="84741-191">Use Windows Management Instruction (WMI) to schedule scans</span></span>

<span data-ttu-id="84741-192">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="84741-192">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
ScanParameters
ScanScheduleDay
ScanScheduleTime
RandomizeScheduleTaskTimes
```

<span data-ttu-id="84741-193">Pour plus d’informations et les paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="84741-193">For more information and allowed parameters, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span></span>


## <a name="start-scheduled-scans-only-when-the-endpoint-is-not-in-use"></a><span data-ttu-id="84741-194">Démarrer des analyses programmées uniquement lorsque le point de terminaison n’est pas en cours d’utilisation</span><span class="sxs-lookup"><span data-stu-id="84741-194">Start scheduled scans only when the endpoint is not in use</span></span>

<span data-ttu-id="84741-195">Vous pouvez définir l’analyse programmée de façon à ce qu’elle se produise uniquement lorsque le point de terminaison est allumé mais qu’il n’est pas utilisé avec la stratégie de groupe, PowerShell ou WMI.</span><span class="sxs-lookup"><span data-stu-id="84741-195">You can set the scheduled scan to only occur when the endpoint is turned on but not in use with Group Policy, PowerShell, or WMI.</span></span>

> [!NOTE]
> <span data-ttu-id="84741-196">Ces analyses ne respectent pas la configuration de limitation du processeur et tirez pleinement parti des ressources disponibles pour effectuer l’analyse aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="84741-196">These scans will not honor the CPU throttling configuration and take full advantage of the resources available to complete the scan as fast as possible.</span></span>

### <a name="use-group-policy-to-schedule-scans"></a><span data-ttu-id="84741-197">Utiliser une stratégie de groupe pour planifier des analyses</span><span class="sxs-lookup"><span data-stu-id="84741-197">Use Group Policy to schedule scans</span></span>

|<span data-ttu-id="84741-198">Emplacement</span><span class="sxs-lookup"><span data-stu-id="84741-198">Location</span></span> | <span data-ttu-id="84741-199">Paramètre</span><span class="sxs-lookup"><span data-stu-id="84741-199">Setting</span></span> | <span data-ttu-id="84741-200">Description</span><span class="sxs-lookup"><span data-stu-id="84741-200">Description</span></span> | <span data-ttu-id="84741-201">Paramètre par défaut (s’il n’est pas configuré)</span><span class="sxs-lookup"><span data-stu-id="84741-201">Default setting (if not configured)</span></span> |
|:---|:---|:---|:---|
|<span data-ttu-id="84741-202">Analyser</span><span class="sxs-lookup"><span data-stu-id="84741-202">Scan</span></span> | <span data-ttu-id="84741-203">Démarrer l’analyse programmée uniquement lorsque l’ordinateur est en cours d’utilisation</span><span class="sxs-lookup"><span data-stu-id="84741-203">Start the scheduled scan only when computer is on but not in use</span></span> | <span data-ttu-id="84741-204">Les analyses programmées ne s’exécutent pas, sauf si l’ordinateur est en cours d’utilisation</span><span class="sxs-lookup"><span data-stu-id="84741-204">Scheduled scans will not run, unless the computer is on but not in use</span></span> | <span data-ttu-id="84741-205">Activé</span><span class="sxs-lookup"><span data-stu-id="84741-205">Enabled</span></span> |

### <a name="use-powershell-cmdlets"></a><span data-ttu-id="84741-206">Utiliser les cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="84741-206">Use PowerShell cmdlets</span></span>

<span data-ttu-id="84741-207">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="84741-207">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -ScanOnlyIfIdleEnabled
```

<span data-ttu-id="84741-208">Pour plus d’informations, voir [Utiliser les cmdlets PowerShell pour configurer et gérer l'Antivirus Microsoft Defender](use-powershell-cmdlets-microsoft-defender-antivirus.md) et [Cmdlets Defender](/powershell/module/defender/).</span><span class="sxs-lookup"><span data-stu-id="84741-208">For more information, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/).</span></span>

### <a name="use-windows-management-instruction-wmi"></a><span data-ttu-id="84741-209">Utiliser Windows Management Instruction (WMI)</span><span class="sxs-lookup"><span data-stu-id="84741-209">Use Windows Management Instruction (WMI)</span></span>

<span data-ttu-id="84741-210">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="84741-210">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
ScanOnlyIfIdleEnabled
```

<span data-ttu-id="84741-211">Pour plus d’informations sur les API et les paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span><span class="sxs-lookup"><span data-stu-id="84741-211">For more information about APIs and allowed parameters, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span></span>

<a id="remed"></a>
## <a name="configure-when-full-scans-should-be-run-to-complete-remediation"></a><span data-ttu-id="84741-212">Configurer le moment où les analyses complètes doivent être exécutés pour terminer la correction</span><span class="sxs-lookup"><span data-stu-id="84741-212">Configure when full scans should be run to complete remediation</span></span>

<span data-ttu-id="84741-213">Certaines menaces peuvent nécessiter une analyse complète pour terminer leur suppression et leur correction.</span><span class="sxs-lookup"><span data-stu-id="84741-213">Some threats might require a full scan to complete their removal and remediation.</span></span> <span data-ttu-id="84741-214">Vous pouvez spécifier quand ces analyses doivent se produire avec la stratégie de groupe, PowerShell ou WMI.</span><span class="sxs-lookup"><span data-stu-id="84741-214">You can specify when these scans should occur with Group Policy, PowerShell, or WMI.</span></span>

### <a name="use-group-policy-to-schedule-remediation-required-scans"></a><span data-ttu-id="84741-215">Utiliser la stratégie de groupe pour planifier des analyses nécessaires à la correction</span><span class="sxs-lookup"><span data-stu-id="84741-215">Use Group Policy to schedule remediation-required scans</span></span>

| <span data-ttu-id="84741-216">Emplacement</span><span class="sxs-lookup"><span data-stu-id="84741-216">Location</span></span> | <span data-ttu-id="84741-217">Paramètre</span><span class="sxs-lookup"><span data-stu-id="84741-217">Setting</span></span> | <span data-ttu-id="84741-218">Description</span><span class="sxs-lookup"><span data-stu-id="84741-218">Description</span></span> | <span data-ttu-id="84741-219">Paramètre par défaut (s’il n’est pas configuré)</span><span class="sxs-lookup"><span data-stu-id="84741-219">Default setting (if not configured)</span></span> |
|---|---|---|---|
|<span data-ttu-id="84741-220">Correction</span><span class="sxs-lookup"><span data-stu-id="84741-220">Remediation</span></span> | <span data-ttu-id="84741-221">Spécifier le jour de la semaine pour exécuter une analyse complète programmée afin de terminer la correction</span><span class="sxs-lookup"><span data-stu-id="84741-221">Specify the day of the week to run a scheduled full scan to complete remediation</span></span> | <span data-ttu-id="84741-222">Spécifiez le jour (ou jamais) d’exécuter une analyse.</span><span class="sxs-lookup"><span data-stu-id="84741-222">Specify the day (or never) to run a scan.</span></span> | <span data-ttu-id="84741-223">Jamais</span><span class="sxs-lookup"><span data-stu-id="84741-223">Never</span></span> |
|<span data-ttu-id="84741-224">Correction</span><span class="sxs-lookup"><span data-stu-id="84741-224">Remediation</span></span> | <span data-ttu-id="84741-225">Spécifier l’heure de la journée pour exécuter une analyse complète programmée afin de terminer la correction</span><span class="sxs-lookup"><span data-stu-id="84741-225">Specify the time of day to run a scheduled full scan to complete remediation</span></span> | <span data-ttu-id="84741-226">Spécifiez le nombre de minutes après minuit (par exemple, entrez **60** pour 1 h 00)</span><span class="sxs-lookup"><span data-stu-id="84741-226">Specify the number of minutes after midnight (for example, enter **60** for 1 a.m.)</span></span> | <span data-ttu-id="84741-227">2 h 00</span><span class="sxs-lookup"><span data-stu-id="84741-227">2 a.m.</span></span> |

### <a name="use-powershell-cmdlets"></a><span data-ttu-id="84741-228">Utiliser les cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="84741-228">Use PowerShell cmdlets</span></span>

<span data-ttu-id="84741-229">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="84741-229">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -RemediationScheduleDay
Set-MpPreference -RemediationScheduleTime
```

<span data-ttu-id="84741-230">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender/) Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="84741-230">See [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

### <a name="use-windows-management-instruction-wmi"></a><span data-ttu-id="84741-231">Utiliser Windows Management Instruction (WMI)</span><span class="sxs-lookup"><span data-stu-id="84741-231">Use Windows Management Instruction (WMI)</span></span>

<span data-ttu-id="84741-232">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="84741-232">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
RemediationScheduleDay
RemediationScheduleTime
```

<span data-ttu-id="84741-233">Pour plus d’informations et les paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span><span class="sxs-lookup"><span data-stu-id="84741-233">For more information and allowed parameters, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span></span>


## <a name="set-up-daily-quick-scans"></a><span data-ttu-id="84741-234">Configurer des analyses rapides quotidiennes</span><span class="sxs-lookup"><span data-stu-id="84741-234">Set up daily quick scans</span></span>

<span data-ttu-id="84741-235">Vous pouvez activer une analyse rapide quotidienne qui peut être exécuté en plus de vos autres analyses programmées avec la stratégie de groupe, PowerShell ou WMI.</span><span class="sxs-lookup"><span data-stu-id="84741-235">You can enable a daily quick scan that can be run in addition to your other scheduled scans with Group Policy, PowerShell, or WMI.</span></span>

### <a name="use-group-policy-to-schedule-daily-scans"></a><span data-ttu-id="84741-236">Utiliser une stratégie de groupe pour planifier des analyses quotidiennes</span><span class="sxs-lookup"><span data-stu-id="84741-236">Use Group Policy to schedule daily scans</span></span>

|<span data-ttu-id="84741-237">Emplacement</span><span class="sxs-lookup"><span data-stu-id="84741-237">Location</span></span> | <span data-ttu-id="84741-238">Paramètre</span><span class="sxs-lookup"><span data-stu-id="84741-238">Setting</span></span> | <span data-ttu-id="84741-239">Description</span><span class="sxs-lookup"><span data-stu-id="84741-239">Description</span></span> | <span data-ttu-id="84741-240">Paramètre par défaut (s’il n’est pas configuré)</span><span class="sxs-lookup"><span data-stu-id="84741-240">Default setting (if not configured)</span></span> |
|:---|:---|:---|:---|
|<span data-ttu-id="84741-241">Analyser</span><span class="sxs-lookup"><span data-stu-id="84741-241">Scan</span></span> | <span data-ttu-id="84741-242">Spécifier l’intervalle pour exécuter des analyses rapides par jour</span><span class="sxs-lookup"><span data-stu-id="84741-242">Specify the interval to run quick scans per day</span></span> | <span data-ttu-id="84741-243">Spécifiez le nombre d’heures devant s’écoulée avant la prochaine analyse rapide.</span><span class="sxs-lookup"><span data-stu-id="84741-243">Specify how many hours should elapse before the next quick scan.</span></span> <span data-ttu-id="84741-244">Par exemple, pour exécuter toutes les deux heures, entrez **2**, pour une fois par jour, **entrez 24**.</span><span class="sxs-lookup"><span data-stu-id="84741-244">For example, to run every two hours, enter **2**, for once a day, enter **24**.</span></span> <span data-ttu-id="84741-245">Entrez **0 pour** ne jamais exécuter une analyse rapide quotidienne.</span><span class="sxs-lookup"><span data-stu-id="84741-245">Enter **0** to never run a daily quick scan.</span></span> | <span data-ttu-id="84741-246">Jamais</span><span class="sxs-lookup"><span data-stu-id="84741-246">Never</span></span> |
|<span data-ttu-id="84741-247">Analyser</span><span class="sxs-lookup"><span data-stu-id="84741-247">Scan</span></span> | <span data-ttu-id="84741-248">Spécifier l’heure d’une analyse rapide quotidienne</span><span class="sxs-lookup"><span data-stu-id="84741-248">Specify the time for a daily quick scan</span></span> | <span data-ttu-id="84741-249">Spécifiez le nombre de minutes après minuit (par exemple, entrez **60** pour 1 h 00)</span><span class="sxs-lookup"><span data-stu-id="84741-249">Specify the number of minutes after midnight (for example, enter **60** for 1 a.m.)</span></span> | <span data-ttu-id="84741-250">2 h 00</span><span class="sxs-lookup"><span data-stu-id="84741-250">2 a.m.</span></span> |

### <a name="use-powershell-cmdlets-to-schedule-daily-scans"></a><span data-ttu-id="84741-251">Utiliser les cmdlets PowerShell pour planifier des analyses quotidiennes</span><span class="sxs-lookup"><span data-stu-id="84741-251">Use PowerShell cmdlets to schedule daily scans</span></span>

<span data-ttu-id="84741-252">Utilisez les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="84741-252">Use the following cmdlets:</span></span>

```PowerShell
Set-MpPreference -ScanScheduleQuickScanTime
```

<span data-ttu-id="84741-253">Pour plus d’informations sur l’utilisation de PowerShell avec Antivirus Microsoft Defender, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter des [cmdlets](/powershell/module/defender/)Antivirus Microsoft Defender et Defender.</span><span class="sxs-lookup"><span data-stu-id="84741-253">For more information about how to use PowerShell with Microsoft Defender Antivirus, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/).</span></span>

### <a name="use-windows-management-instruction-wmi-to-schedule-daily-scans"></a><span data-ttu-id="84741-254">Utiliser Windows Management Instruction (WMI) pour planifier des analyses quotidiennes</span><span class="sxs-lookup"><span data-stu-id="84741-254">Use Windows Management Instruction (WMI) to schedule daily scans</span></span>

<span data-ttu-id="84741-255">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="84741-255">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
ScanScheduleQuickScanTime
```

<span data-ttu-id="84741-256">Pour plus d’informations et les paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span><span class="sxs-lookup"><span data-stu-id="84741-256">For more information and allowed parameters, see [Windows Defender WMIv2 APIs](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal).</span></span>


## <a name="enable-scans-after-protection-updates"></a><span data-ttu-id="84741-257">Activer les analyses après les mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="84741-257">Enable scans after protection updates</span></span>

<span data-ttu-id="84741-258">Vous pouvez forcer une analyse à se produire après chaque mise à jour [de protection](manage-protection-updates-microsoft-defender-antivirus.md) avec la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="84741-258">You can force a scan to occur after every [protection update](manage-protection-updates-microsoft-defender-antivirus.md) with Group Policy.</span></span>

### <a name="use-group-policy-to-schedule-scans-after-protection-updates"></a><span data-ttu-id="84741-259">Utiliser la stratégie de groupe pour planifier des analyses après les mises à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="84741-259">Use Group Policy to schedule scans after protection updates</span></span>

|<span data-ttu-id="84741-260">Emplacement</span><span class="sxs-lookup"><span data-stu-id="84741-260">Location</span></span> | <span data-ttu-id="84741-261">Paramètre</span><span class="sxs-lookup"><span data-stu-id="84741-261">Setting</span></span> | <span data-ttu-id="84741-262">Description</span><span class="sxs-lookup"><span data-stu-id="84741-262">Description</span></span> | <span data-ttu-id="84741-263">Paramètre par défaut (s’il n’est pas configuré)</span><span class="sxs-lookup"><span data-stu-id="84741-263">Default setting (if not configured)</span></span>|
|:---|:---|:---|:---|
|<span data-ttu-id="84741-264">Mises à jour des signatures</span><span class="sxs-lookup"><span data-stu-id="84741-264">Signature updates</span></span> | <span data-ttu-id="84741-265">Activer l’analyse après la mise à jour des informations de sécurité</span><span class="sxs-lookup"><span data-stu-id="84741-265">Turn on scan after Security intelligence update</span></span> | <span data-ttu-id="84741-266">Une analyse se produit immédiatement après le téléchargement d’une nouvelle mise à jour de la protection</span><span class="sxs-lookup"><span data-stu-id="84741-266">A scan will occur immediately after a new protection update is downloaded</span></span> | <span data-ttu-id="84741-267">Activé</span><span class="sxs-lookup"><span data-stu-id="84741-267">Enabled</span></span> |

## <a name="see-also"></a><span data-ttu-id="84741-268">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84741-268">See also</span></span>

- [<span data-ttu-id="84741-269">Empêcher ou autoriser les utilisateurs à modifier localement les paramètres de stratégie</span><span class="sxs-lookup"><span data-stu-id="84741-269">Prevent or allow users to locally modify policy settings</span></span>](configure-local-policy-overrides-microsoft-defender-antivirus.md)
- <span data-ttu-id="84741-270">[Configurer et exécuter des analyses à la demande avec l’antivirus Microsoft Defender](run-scan-microsoft-defender-antivirus.md).</span><span class="sxs-lookup"><span data-stu-id="84741-270">[Configure and run on-demand Microsoft Defender Antivirus scans](run-scan-microsoft-defender-antivirus.md)</span></span>
- [<span data-ttu-id="84741-271">Configurer les options d’analyse de l’antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="84741-271">Configure Microsoft Defender Antivirus scanning options</span></span>](configure-advanced-scan-types-microsoft-defender-antivirus.md)
- [<span data-ttu-id="84741-272">Gérer les mises Antivirus Microsoft Defender jour et appliquer les lignes de base</span><span class="sxs-lookup"><span data-stu-id="84741-272">Manage Microsoft Defender Antivirus updates and apply baselines</span></span>](manage-updates-baselines-microsoft-defender-antivirus.md)
- [<span data-ttu-id="84741-273">Gérer le moment où les mises à jour de protection doivent être téléchargées et appliquées</span><span class="sxs-lookup"><span data-stu-id="84741-273">Manage when protection updates should be downloaded and applied</span></span>](manage-protection-update-schedule-microsoft-defender-antivirus.md) 
- [<span data-ttu-id="84741-274">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="84741-274">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)