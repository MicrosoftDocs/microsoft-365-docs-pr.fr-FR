---
title: Microsoft Defender pour point de terminaison sur les ressources Linux
ms.reviewer: ''
description: Décrit les ressources de Microsoft Defender pour Endpoint sur Linux, notamment comment le désinstaller, comment collecter les journaux de diagnostic, les commandes CLI et les problèmes connus avec le produit.
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, linux, installation, déployer, désinstallation, préinstallation, ansible, linux, redhat, ubuntu, debian, sles, suse, centos
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: aaf9c0a8eef4e050ca034d1aee69d24c5adb909d
ms.sourcegitcommit: 3d30ec03628870a22c54b6ec5d865cbe94f34245
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52930366"
---
# <a name="resources"></a><span data-ttu-id="7667c-104">Ressources</span><span class="sxs-lookup"><span data-stu-id="7667c-104">Resources</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="7667c-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="7667c-105">**Applies to:**</span></span>

- [<span data-ttu-id="7667c-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7667c-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="7667c-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="7667c-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="7667c-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="7667c-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="7667c-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="7667c-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

## <a name="collect-diagnostic-information"></a><span data-ttu-id="7667c-110">Collecter des informations de diagnostic</span><span class="sxs-lookup"><span data-stu-id="7667c-110">Collect diagnostic information</span></span>

<span data-ttu-id="7667c-111">Si vous pouvez reproduire un problème, augmentez d’abord le niveau de journalisation, exécutez le système pendant un certain temps, puis rétablissez le niveau de journalisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="7667c-111">If you can reproduce a problem, first increase the logging level, run the system for some time, and then restore the logging level to the default.</span></span>

1. <span data-ttu-id="7667c-112">Augmenter le niveau de journalisation :</span><span class="sxs-lookup"><span data-stu-id="7667c-112">Increase logging level:</span></span>

   ```bash
   mdatp log level set --level debug
   ```

   ```Output
   Log level configured successfully
   ```

2. <span data-ttu-id="7667c-113">Reproduisez le problème.</span><span class="sxs-lookup"><span data-stu-id="7667c-113">Reproduce the problem.</span></span>

3. <span data-ttu-id="7667c-114">Exécutez la commande suivante pour back up Defender for Endpoint’s logs.</span><span class="sxs-lookup"><span data-stu-id="7667c-114">Run the following command to back up Defender for Endpoint's logs.</span></span> <span data-ttu-id="7667c-115">Les fichiers sont stockés dans une archive .zip de données.</span><span class="sxs-lookup"><span data-stu-id="7667c-115">The files will be stored inside of a .zip archive.</span></span>

   ```bash
   sudo mdatp diagnostic create
   ```

    <span data-ttu-id="7667c-116">Cette commande imprime également le chemin d’accès du fichier à la sauvegarde une fois l’opération réussie :</span><span class="sxs-lookup"><span data-stu-id="7667c-116">This command will also print out the file path to the backup after the operation succeeds:</span></span>

   ```Output
   Diagnostic file created: <path to file>
   ```

4. <span data-ttu-id="7667c-117">Restaurer le niveau de journalisation :</span><span class="sxs-lookup"><span data-stu-id="7667c-117">Restore logging level:</span></span>

   ```bash
   mdatp log level set --level info
   ```

   ```Output
   Log level configured successfully
   ```

## <a name="log-installation-issues"></a><span data-ttu-id="7667c-118">Journaux des problèmes d’installation</span><span class="sxs-lookup"><span data-stu-id="7667c-118">Log installation issues</span></span>

<span data-ttu-id="7667c-119">Si une erreur se produit pendant l’installation, le programme d’installation signale uniquement un échec général.</span><span class="sxs-lookup"><span data-stu-id="7667c-119">If an error occurs during installation, the installer will only report a general failure.</span></span>

<span data-ttu-id="7667c-120">Le journal détaillé sera enregistré dans `/var/log/microsoft/mdatp/install.log` .</span><span class="sxs-lookup"><span data-stu-id="7667c-120">The detailed log will be saved to `/var/log/microsoft/mdatp/install.log`.</span></span>
<span data-ttu-id="7667c-121">Si vous avez des problèmes lors de l’installation, envoyez-nous ce fichier afin que nous aidions à diagnostiquer la cause.</span><span class="sxs-lookup"><span data-stu-id="7667c-121">If you experience issues during installation, send us this file so we can help diagnose the cause.</span></span>

## <a name="uninstall"></a><span data-ttu-id="7667c-122">Désinstaller</span><span class="sxs-lookup"><span data-stu-id="7667c-122">Uninstall</span></span>

<span data-ttu-id="7667c-123">Il existe plusieurs façons de désinstaller Defender pour Endpoint sur Linux.</span><span class="sxs-lookup"><span data-stu-id="7667c-123">There are several ways to uninstall Defender for Endpoint on Linux.</span></span> <span data-ttu-id="7667c-124">Si vous utilisez un outil de configuration tel que l’Outil de configuration, suivez les instructions de désinstallation du package pour l’outil de configuration.</span><span class="sxs-lookup"><span data-stu-id="7667c-124">If you are using a configuration tool such as Puppet, follow the package uninstallation instructions for the configuration tool.</span></span>

### <a name="manual-uninstallation"></a><span data-ttu-id="7667c-125">Désinstallation manuelle</span><span class="sxs-lookup"><span data-stu-id="7667c-125">Manual uninstallation</span></span>

- <span data-ttu-id="7667c-126">`sudo yum remove mdatp` pour RHEL et les variantes (CentOS et Oracle Linux).</span><span class="sxs-lookup"><span data-stu-id="7667c-126">`sudo yum remove mdatp` for RHEL and variants(CentOS and Oracle Linux).</span></span>
- <span data-ttu-id="7667c-127">`sudo zypper remove mdatp` pour SLES et les variantes.</span><span class="sxs-lookup"><span data-stu-id="7667c-127">`sudo zypper remove mdatp` for SLES and variants.</span></span>
- <span data-ttu-id="7667c-128">`sudo apt-get purge mdatp` pour les systèmes Ubuntu et Debian.</span><span class="sxs-lookup"><span data-stu-id="7667c-128">`sudo apt-get purge mdatp` for Ubuntu and Debian systems.</span></span>

## <a name="configure-from-the-command-line"></a><span data-ttu-id="7667c-129">Configurer à partir de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="7667c-129">Configure from the command line</span></span>

<span data-ttu-id="7667c-130">Des tâches importantes, telles que le contrôle des paramètres du produit et le déclenchement d’analyses à la demande, peuvent être réalisées à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7667c-130">Important tasks, such as controlling product settings and triggering on-demand scans, can be done from the command line.</span></span>

### <a name="global-options"></a><span data-ttu-id="7667c-131">Options globales</span><span class="sxs-lookup"><span data-stu-id="7667c-131">Global options</span></span>

<span data-ttu-id="7667c-132">Par défaut, l’outil en ligne de commande produit le résultat dans un format lisible par l’homme.</span><span class="sxs-lookup"><span data-stu-id="7667c-132">By default, the command-line tool outputs the result in human-readable format.</span></span> <span data-ttu-id="7667c-133">En outre, l’outil prend également en charge la sortie du résultat en tant que JSON, ce qui est utile pour les scénarios d’automatisation.</span><span class="sxs-lookup"><span data-stu-id="7667c-133">In addition, the tool also supports outputting the result as JSON, which is useful for automation scenarios.</span></span> <span data-ttu-id="7667c-134">Pour modifier la sortie en JSON, passez `--output json` à l’une des commandes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7667c-134">To change the output to JSON, pass `--output json` to any of the below commands.</span></span>

### <a name="supported-commands"></a><span data-ttu-id="7667c-135">Commandes prises en charge</span><span class="sxs-lookup"><span data-stu-id="7667c-135">Supported commands</span></span>

<span data-ttu-id="7667c-136">Le tableau suivant répertorie les commandes pour certains des scénarios les plus courants.</span><span class="sxs-lookup"><span data-stu-id="7667c-136">The following table lists commands for some of the most common scenarios.</span></span> <span data-ttu-id="7667c-137">Exécutez `mdatp help` à partir du Terminal pour afficher la liste complète des commandes prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7667c-137">Run `mdatp help` from the Terminal to view the full list of supported commands.</span></span>

|<span data-ttu-id="7667c-138">Group</span><span class="sxs-lookup"><span data-stu-id="7667c-138">Group</span></span>                 |<span data-ttu-id="7667c-139">Scénario</span><span class="sxs-lookup"><span data-stu-id="7667c-139">Scenario</span></span>                                                |<span data-ttu-id="7667c-140">Commande</span><span class="sxs-lookup"><span data-stu-id="7667c-140">Command</span></span>                                                                |
|----------------------|--------------------------------------------------------|-----------------------------------------------------------------------|
|<span data-ttu-id="7667c-141">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-141">Configuration</span></span>         |<span data-ttu-id="7667c-142">Activer/désactiver la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="7667c-142">Turn on/off real-time protection</span></span>                        |`mdatp config real-time-protection --value [enabled\|disabled]`        |
|<span data-ttu-id="7667c-143">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-143">Configuration</span></span>         |<span data-ttu-id="7667c-144">Activer/désactiver la surveillance du comportement</span><span class="sxs-lookup"><span data-stu-id="7667c-144">Turn on/off behavior monitoring</span></span>                         |`mdatp config behavior-monitoring --value [enabled\|disabled]`
|<span data-ttu-id="7667c-145">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-145">Configuration</span></span>         |<span data-ttu-id="7667c-146">Activer/désactiver la protection cloud</span><span class="sxs-lookup"><span data-stu-id="7667c-146">Turn on/off cloud protection</span></span>                            |`mdatp config cloud --value [enabled\|disabled]`                       |
|<span data-ttu-id="7667c-147">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-147">Configuration</span></span>         |<span data-ttu-id="7667c-148">Activer/désactiver les diagnostics de produit</span><span class="sxs-lookup"><span data-stu-id="7667c-148">Turn on/off product diagnostics</span></span>                         |`mdatp config cloud-diagnostic --value [enabled\|disabled]`            |
|<span data-ttu-id="7667c-149">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-149">Configuration</span></span>         |<span data-ttu-id="7667c-150">Activer/désactiver l’envoi automatique d’échantillons</span><span class="sxs-lookup"><span data-stu-id="7667c-150">Turn on/off automatic sample submission</span></span>                 |`mdatp config cloud-automatic-sample-submission [enabled\|disabled]`   |
|<span data-ttu-id="7667c-151">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-151">Configuration</span></span>         |<span data-ttu-id="7667c-152">Activer/désactiver le mode passif antivirus</span><span class="sxs-lookup"><span data-stu-id="7667c-152">Turn on/off AV passive mode</span></span>                             |`mdatp config passive-mode --value [enabled\|disabled]`                |
|<span data-ttu-id="7667c-153">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-153">Configuration</span></span>         |<span data-ttu-id="7667c-154">Ajouter/supprimer une exclusion antivirus pour une extension de fichier</span><span class="sxs-lookup"><span data-stu-id="7667c-154">Add/remove an antivirus exclusion for a file extension</span></span>  |`mdatp exclusion extension [add\|remove] --name [extension]`           |
|<span data-ttu-id="7667c-155">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-155">Configuration</span></span>         |<span data-ttu-id="7667c-156">Ajouter/supprimer une exclusion antivirus pour un fichier</span><span class="sxs-lookup"><span data-stu-id="7667c-156">Add/remove an antivirus exclusion for a file</span></span>            |`mdatp exclusion file [add\|remove] --path [path-to-file]`             |
|<span data-ttu-id="7667c-157">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-157">Configuration</span></span>         |<span data-ttu-id="7667c-158">Ajouter/supprimer une exclusion antivirus pour un répertoire</span><span class="sxs-lookup"><span data-stu-id="7667c-158">Add/remove an antivirus exclusion for a directory</span></span>       |`mdatp exclusion folder [add\|remove] --path [path-to-directory]`      |
|<span data-ttu-id="7667c-159">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-159">Configuration</span></span>         |<span data-ttu-id="7667c-160">Ajouter/supprimer une exclusion antivirus pour un processus</span><span class="sxs-lookup"><span data-stu-id="7667c-160">Add/remove an antivirus exclusion for a process</span></span>         |`mdatp exclusion process [add\|remove] --path [path-to-process]`<br/>`mdatp exclusion process [add\|remove] --name [process-name]` |
|<span data-ttu-id="7667c-161">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-161">Configuration</span></span>         |<span data-ttu-id="7667c-162">Liste de toutes les exclusions antivirus</span><span class="sxs-lookup"><span data-stu-id="7667c-162">List all antivirus exclusions</span></span>                           |`mdatp exclusion list`                                                 |
|<span data-ttu-id="7667c-163">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-163">Configuration</span></span>         |<span data-ttu-id="7667c-164">Ajouter un nom de menace à la liste autorisée</span><span class="sxs-lookup"><span data-stu-id="7667c-164">Add a threat name to the allowed list</span></span>                   |`mdatp threat allowed add --name [threat-name]`                        |
|<span data-ttu-id="7667c-165">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-165">Configuration</span></span>         |<span data-ttu-id="7667c-166">Supprimer un nom de menace de la liste autorisée</span><span class="sxs-lookup"><span data-stu-id="7667c-166">Remove a threat name from the allowed list</span></span>              |`mdatp threat allowed remove --name [threat-name]`                     |
|<span data-ttu-id="7667c-167">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-167">Configuration</span></span>         |<span data-ttu-id="7667c-168">Liste de tous les noms de menaces autorisés</span><span class="sxs-lookup"><span data-stu-id="7667c-168">List all allowed threat names</span></span>                           |`mdatp threat allowed list`                                            |
|<span data-ttu-id="7667c-169">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-169">Configuration</span></span>         |<span data-ttu-id="7667c-170">Activer la protection PUA</span><span class="sxs-lookup"><span data-stu-id="7667c-170">Turn on PUA protection</span></span>                                  |`mdatp threat policy set --type potentially_unwanted_application --action block` |
|<span data-ttu-id="7667c-171">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-171">Configuration</span></span>         |<span data-ttu-id="7667c-172">Désactiver la protection PUA</span><span class="sxs-lookup"><span data-stu-id="7667c-172">Turn off PUA protection</span></span>                                 |`mdatp threat policy set --type potentially_unwanted_application --action off` |
|<span data-ttu-id="7667c-173">Configuration</span><span class="sxs-lookup"><span data-stu-id="7667c-173">Configuration</span></span>         |<span data-ttu-id="7667c-174">Activer le mode audit pour la protection PUA</span><span class="sxs-lookup"><span data-stu-id="7667c-174">Turn on audit mode for PUA protection</span></span>                   |`mdatp threat policy set --type potentially_unwanted_application --action audit` |
|<span data-ttu-id="7667c-175">Diagnostics</span><span class="sxs-lookup"><span data-stu-id="7667c-175">Diagnostics</span></span>           |<span data-ttu-id="7667c-176">Modifier le niveau de journal</span><span class="sxs-lookup"><span data-stu-id="7667c-176">Change the log level</span></span>                                    |`mdatp log level set --level verbose [error|warning|info|verbose]`     |
|<span data-ttu-id="7667c-177">Diagnostics</span><span class="sxs-lookup"><span data-stu-id="7667c-177">Diagnostics</span></span>           |<span data-ttu-id="7667c-178">Générer des journaux de diagnostic</span><span class="sxs-lookup"><span data-stu-id="7667c-178">Generate diagnostic logs</span></span>                                |`mdatp diagnostic create --path [directory]`                           |
|<span data-ttu-id="7667c-179">Intégrité</span><span class="sxs-lookup"><span data-stu-id="7667c-179">Health</span></span>                |<span data-ttu-id="7667c-180">Vérifier l’état du produit</span><span class="sxs-lookup"><span data-stu-id="7667c-180">Check the product's health</span></span>                              |`mdatp health`                                                         |
|<span data-ttu-id="7667c-181">Protection</span><span class="sxs-lookup"><span data-stu-id="7667c-181">Protection</span></span>            |<span data-ttu-id="7667c-182">Analyser un chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="7667c-182">Scan a path</span></span>                                             |`mdatp scan custom --path [path] [--ignore-exclusions]`                |
|<span data-ttu-id="7667c-183">Protection</span><span class="sxs-lookup"><span data-stu-id="7667c-183">Protection</span></span>            |<span data-ttu-id="7667c-184">Faire une analyse rapide</span><span class="sxs-lookup"><span data-stu-id="7667c-184">Do a quick scan</span></span>                                         |`mdatp scan quick`                                                     |
|<span data-ttu-id="7667c-185">Protection</span><span class="sxs-lookup"><span data-stu-id="7667c-185">Protection</span></span>            |<span data-ttu-id="7667c-186">Faire une analyse complète</span><span class="sxs-lookup"><span data-stu-id="7667c-186">Do a full scan</span></span>                                          |`mdatp scan full`                                                      |
|<span data-ttu-id="7667c-187">Protection</span><span class="sxs-lookup"><span data-stu-id="7667c-187">Protection</span></span>            |<span data-ttu-id="7667c-188">Annuler une analyse à la demande en cours</span><span class="sxs-lookup"><span data-stu-id="7667c-188">Cancel an ongoing on-demand scan</span></span>                        |`mdatp scan cancel`                                                    |
|<span data-ttu-id="7667c-189">Protection</span><span class="sxs-lookup"><span data-stu-id="7667c-189">Protection</span></span>            |<span data-ttu-id="7667c-190">Demander une mise à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="7667c-190">Request a security intelligence update</span></span>                  |`mdatp definitions update`                                             |
|<span data-ttu-id="7667c-191">Historique de la protection</span><span class="sxs-lookup"><span data-stu-id="7667c-191">Protection history</span></span>    |<span data-ttu-id="7667c-192">Imprimer l’historique complet de la protection</span><span class="sxs-lookup"><span data-stu-id="7667c-192">Print the full protection history</span></span>                       |`mdatp threat list`                                                    |
|<span data-ttu-id="7667c-193">Historique de la protection</span><span class="sxs-lookup"><span data-stu-id="7667c-193">Protection history</span></span>    |<span data-ttu-id="7667c-194">Obtenir les détails sur les menaces</span><span class="sxs-lookup"><span data-stu-id="7667c-194">Get threat details</span></span>                                      |`mdatp threat get --id [threat-id]`                                    |
|<span data-ttu-id="7667c-195">Gestion de la mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="7667c-195">Quarantine management</span></span> |<span data-ttu-id="7667c-196">Liste de tous les fichiers mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="7667c-196">List all quarantined files</span></span>                              |`mdatp threat quarantine list`                                         |
|<span data-ttu-id="7667c-197">Gestion de la mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="7667c-197">Quarantine management</span></span> |<span data-ttu-id="7667c-198">Supprimer tous les fichiers de la quarantaine</span><span class="sxs-lookup"><span data-stu-id="7667c-198">Remove all files from the quarantine</span></span>                    |`mdatp threat quarantine remove-all`                                   |
|<span data-ttu-id="7667c-199">Gestion de la mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="7667c-199">Quarantine management</span></span> |<span data-ttu-id="7667c-200">Ajouter un fichier détecté comme une menace en quarantaine</span><span class="sxs-lookup"><span data-stu-id="7667c-200">Add a file detected as a threat to the quarantine</span></span>       |`mdatp threat quarantine add --id [threat-id]`                         |
|<span data-ttu-id="7667c-201">Gestion de la mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="7667c-201">Quarantine management</span></span> |<span data-ttu-id="7667c-202">Supprimer de la quarantaine un fichier détecté comme une menace</span><span class="sxs-lookup"><span data-stu-id="7667c-202">Remove a file detected as a threat from the quarantine</span></span>  |`mdatp threat quarantine remove --id [threat-id]`                      |
|<span data-ttu-id="7667c-203">Gestion de la mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="7667c-203">Quarantine management</span></span> |<span data-ttu-id="7667c-204">Restaurer un fichier de la quarantaine</span><span class="sxs-lookup"><span data-stu-id="7667c-204">Restore a file from the quarantine</span></span>                      |`mdatp threat quarantine restore --id [threat-id]`                     |
|<span data-ttu-id="7667c-205">Détection et réponse des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="7667c-205">Endpoint Detection and Response</span></span> |<span data-ttu-id="7667c-206">Définir la prévisualisation (inutilisée)</span><span class="sxs-lookup"><span data-stu-id="7667c-206">Set early preview (unused)</span></span>                    |`mdatp edr early-preview [enable|disable]`                             |
|<span data-ttu-id="7667c-207">Détection et réponse des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="7667c-207">Endpoint Detection and Response</span></span> |<span data-ttu-id="7667c-208">Définir l’ID de groupe</span><span class="sxs-lookup"><span data-stu-id="7667c-208">Set group-id</span></span>                                  |`mdatp edr group-ids --group-id [group-id]`                            |
|<span data-ttu-id="7667c-209">Détection et réponse des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="7667c-209">Endpoint Detection and Response</span></span> |<span data-ttu-id="7667c-210">Balise Set/Remove uniquement `GROUP` prise en charge</span><span class="sxs-lookup"><span data-stu-id="7667c-210">Set/Remove tag, only `GROUP` supported</span></span>        |`mdatp edr tag set --name GROUP --value [tag]`                         |
|<span data-ttu-id="7667c-211">Détection et réponse des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="7667c-211">Endpoint Detection and Response</span></span> |<span data-ttu-id="7667c-212">exclusions de liste (racine)</span><span class="sxs-lookup"><span data-stu-id="7667c-212">list exclusions (root)</span></span>                        |`mdatp edr exclusion list [processes|paths|extensions|all]`            |

## <a name="microsoft-defender-for-endpoint-portal-information"></a><span data-ttu-id="7667c-213">Informations du portail Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="7667c-213">Microsoft Defender for Endpoint portal information</span></span>

<span data-ttu-id="7667c-214">Dans le portail Defender pour points de terminaison, deux catégories d’informations s’offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="7667c-214">In the Defender for Endpoint portal, you'll see two categories of information:</span></span>

- <span data-ttu-id="7667c-215">Alertes antivirus, notamment :</span><span class="sxs-lookup"><span data-stu-id="7667c-215">Antivirus alerts, including:</span></span>
  - <span data-ttu-id="7667c-216">Severity</span><span class="sxs-lookup"><span data-stu-id="7667c-216">Severity</span></span>
  - <span data-ttu-id="7667c-217">Type d’analyse</span><span class="sxs-lookup"><span data-stu-id="7667c-217">Scan type</span></span>
  - <span data-ttu-id="7667c-218">Informations sur l’appareil (nom d’hôte, identificateur d’appareil, identificateur client, version de l’application et type de système d’exploitation)</span><span class="sxs-lookup"><span data-stu-id="7667c-218">Device information (hostname, device identifier, tenant identifier, app version, and OS type)</span></span>
  - <span data-ttu-id="7667c-219">Informations sur le fichier (nom, chemin d’accès, taille et hachage)</span><span class="sxs-lookup"><span data-stu-id="7667c-219">File information (name, path, size, and hash)</span></span>
  - <span data-ttu-id="7667c-220">Informations sur les menaces (nom, type et état)</span><span class="sxs-lookup"><span data-stu-id="7667c-220">Threat information (name, type, and state)</span></span>
- <span data-ttu-id="7667c-221">Informations sur l’appareil, notamment :</span><span class="sxs-lookup"><span data-stu-id="7667c-221">Device information, including:</span></span>
  - <span data-ttu-id="7667c-222">Identificateur d’appareil</span><span class="sxs-lookup"><span data-stu-id="7667c-222">Device identifier</span></span>
  - <span data-ttu-id="7667c-223">Identificateur de client</span><span class="sxs-lookup"><span data-stu-id="7667c-223">Tenant identifier</span></span>
  - <span data-ttu-id="7667c-224">Version de l’application.</span><span class="sxs-lookup"><span data-stu-id="7667c-224">App version</span></span>
  - <span data-ttu-id="7667c-225">Nom d'hôte</span><span class="sxs-lookup"><span data-stu-id="7667c-225">Hostname</span></span>
  - <span data-ttu-id="7667c-226">Type de système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="7667c-226">OS type</span></span>
  - <span data-ttu-id="7667c-227">Version du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="7667c-227">OS version</span></span>
  - <span data-ttu-id="7667c-228">Modèle ordinateur</span><span class="sxs-lookup"><span data-stu-id="7667c-228">Computer model</span></span>
  - <span data-ttu-id="7667c-229">Architecture du processeur</span><span class="sxs-lookup"><span data-stu-id="7667c-229">Processor architecture</span></span>
  - <span data-ttu-id="7667c-230">Si l’appareil est une machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="7667c-230">Whether the device is a virtual machine</span></span>

### <a name="known-issues"></a><span data-ttu-id="7667c-231">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="7667c-231">Known issues</span></span>

- <span data-ttu-id="7667c-232">Vous pouvez voir « Aucune donnée de capteur, communications altérées » dans la page d’informations de l’ordinateur du portail Centre de sécurité Microsoft Defender, même si le produit fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="7667c-232">You might see "No sensor data, impaired communications" in the machine information page of the Microsoft Defender Security Center portal, even though the product is working as expected.</span></span> <span data-ttu-id="7667c-233">Nous travaillons à la résoudre.</span><span class="sxs-lookup"><span data-stu-id="7667c-233">We are working on addressing this issue.</span></span>
- <span data-ttu-id="7667c-234">Les utilisateurs connectés n’apparaissent pas sur le Centre de sécurité Microsoft Defender web.</span><span class="sxs-lookup"><span data-stu-id="7667c-234">Logged on users do not appear in the Microsoft Defender Security Center portal.</span></span>
- <span data-ttu-id="7667c-235">Dans les distributions SUSE, si l’installation de *libatomic1* échoue, vous devez vérifier que votre système d’exploitation est enregistré :</span><span class="sxs-lookup"><span data-stu-id="7667c-235">In SUSE distributions, if the installation of *libatomic1* fails, you should validate that your OS is registered:</span></span>

   ```bash
   sudo SUSEConnect --status-text
   ```
