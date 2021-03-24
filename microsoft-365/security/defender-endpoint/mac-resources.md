---
title: Ressources pour Microsoft Defender ATP pour Mac
description: Ressources pour Microsoft Defender ATP pour Mac, notamment comment le désinstaller, comment collecter des journaux de diagnostic, des commandes CLI et des problèmes connus avec le produit.
keywords: microsoft, defender, atp, mac, installation, déployer, désinstallation, intune, jamf, macos,pépé, mojave, high sierra
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
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 336f85b41884a441d0967c7f242b69c4d0e4941f
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51064113"
---
# <a name="resources-for-microsoft-defender-for-endpoint-for-mac"></a><span data-ttu-id="6eef5-104">Ressources pour Microsoft Defender pour point de terminaison pour Mac</span><span class="sxs-lookup"><span data-stu-id="6eef5-104">Resources for Microsoft Defender for Endpoint for Mac</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="6eef5-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6eef5-105">**Applies to:**</span></span>
- [<span data-ttu-id="6eef5-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6eef5-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="6eef5-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6eef5-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="6eef5-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="6eef5-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="6eef5-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6eef5-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

## <a name="collecting-diagnostic-information"></a><span data-ttu-id="6eef5-110">Collecte d’informations de diagnostic</span><span class="sxs-lookup"><span data-stu-id="6eef5-110">Collecting diagnostic information</span></span>

<span data-ttu-id="6eef5-111">Si vous pouvez reproduire un problème, augmentez le niveau de journalisation, exécutez le système pendant un certain temps et rétablissez le niveau de journalisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="6eef5-111">If you can reproduce a problem, increase the logging level, run the system for some time, and restore the logging level to the default.</span></span>

1. <span data-ttu-id="6eef5-112">Augmenter le niveau de journalisation :</span><span class="sxs-lookup"><span data-stu-id="6eef5-112">Increase logging level:</span></span>

   ```bash
   mdatp log level set --level verbose
   ```

   ```Output
   Log level configured successfully
   ```

2. <span data-ttu-id="6eef5-113">Reproduire le problème</span><span class="sxs-lookup"><span data-stu-id="6eef5-113">Reproduce the problem</span></span>

3. <span data-ttu-id="6eef5-114">Exécutez `sudo mdatp diagnostic create` cette session pour enregistrer les journaux microsoft Defender pour les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="6eef5-114">Run `sudo mdatp diagnostic create` to back up the Microsoft Defender for Endpoint logs.</span></span> <span data-ttu-id="6eef5-115">Les fichiers sont stockés dans une archive .zip.</span><span class="sxs-lookup"><span data-stu-id="6eef5-115">The files will be stored inside a .zip archive.</span></span> <span data-ttu-id="6eef5-116">Cette commande imprime également le chemin d’accès du fichier à la sauvegarde une fois l’opération réussie.</span><span class="sxs-lookup"><span data-stu-id="6eef5-116">This command will also print out the file path to the backup after the operation succeeds.</span></span>

   > [!TIP]
   > <span data-ttu-id="6eef5-117">Par défaut, les journaux de diagnostic sont enregistrés dans `/Library/Application Support/Microsoft/Defender/wdavdiag/` .</span><span class="sxs-lookup"><span data-stu-id="6eef5-117">By default, diagnostic logs are saved to `/Library/Application Support/Microsoft/Defender/wdavdiag/`.</span></span> <span data-ttu-id="6eef5-118">Pour modifier le répertoire dans lequel les journaux de diagnostic sont enregistrés, passez à la commande ci-dessous, en remplaçant par le `--path [directory]` `[directory]` répertoire souhaité.</span><span class="sxs-lookup"><span data-stu-id="6eef5-118">To change the directory where diagnostic logs are saved, pass `--path [directory]` to the below command, replacing `[directory]` with the desired directory.</span></span>

   ```bash
   sudo mdatp diagnostic create
   ```
   ```console
   Diagnostic file created: "/Library/Application Support/Microsoft/Defender/wdavdiag/932e68a8-8f2e-4ad0-a7f2-65eb97c0de01.zip"
   ```

4. <span data-ttu-id="6eef5-119">Restaurer le niveau de journalisation :</span><span class="sxs-lookup"><span data-stu-id="6eef5-119">Restore logging level:</span></span>

   ```bash
   mdatp log level set --level info
   ```
   ```console
   Log level configured successfully
   ```

## <a name="logging-installation-issues"></a><span data-ttu-id="6eef5-120">Journalisation des problèmes d’installation</span><span class="sxs-lookup"><span data-stu-id="6eef5-120">Logging installation issues</span></span>

<span data-ttu-id="6eef5-121">Si une erreur se produit lors de l’installation, le programme d’installation signale uniquement un échec général.</span><span class="sxs-lookup"><span data-stu-id="6eef5-121">If an error occurs during installation, the installer will only report a general failure.</span></span>

<span data-ttu-id="6eef5-122">Le journal détaillé sera enregistré dans `/Library/Logs/Microsoft/mdatp/install.log` .</span><span class="sxs-lookup"><span data-stu-id="6eef5-122">The detailed log will be saved to `/Library/Logs/Microsoft/mdatp/install.log`.</span></span> <span data-ttu-id="6eef5-123">Si vous avez des problèmes lors de l’installation, envoyez-nous ce fichier afin que nous aidions à diagnostiquer la cause.</span><span class="sxs-lookup"><span data-stu-id="6eef5-123">If you experience issues during installation, send us this file so we can help diagnose the cause.</span></span>

## <a name="uninstalling"></a><span data-ttu-id="6eef5-124">Désinstallation</span><span class="sxs-lookup"><span data-stu-id="6eef5-124">Uninstalling</span></span>

<span data-ttu-id="6eef5-125">Il existe plusieurs façons de désinstaller Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="6eef5-125">There are several ways to uninstall Microsoft Defender for Endpoint for Mac.</span></span> <span data-ttu-id="6eef5-126">Notez que bien que la désinstallation gérée de manière centralisée soit disponible sur JAMF, elle n’est pas encore disponible pour Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="6eef5-126">Note that while centrally managed uninstall is available on JAMF, it is not yet available for Microsoft Intune.</span></span>

### <a name="interactive-uninstallation"></a><span data-ttu-id="6eef5-127">Désinstallation interactive</span><span class="sxs-lookup"><span data-stu-id="6eef5-127">Interactive uninstallation</span></span>

- <span data-ttu-id="6eef5-128">Ouvrez **Finder > Applications.**</span><span class="sxs-lookup"><span data-stu-id="6eef5-128">Open **Finder > Applications**.</span></span> <span data-ttu-id="6eef5-129">Cliquez avec le bouton **droit sur Microsoft Defender ATP > déplacer vers la corbeille.**</span><span class="sxs-lookup"><span data-stu-id="6eef5-129">Right click on **Microsoft Defender ATP > Move to Trash**.</span></span>

### <a name="from-the-command-line"></a><span data-ttu-id="6eef5-130">À partir de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="6eef5-130">From the command line</span></span>

- ```sudo rm -rf '/Applications/Microsoft Defender ATP.app'```
- ```sudo rm -rf '/Library/Application Support/Microsoft/Defender/'```

## <a name="configuring-from-the-command-line"></a><span data-ttu-id="6eef5-131">Configuration à partir de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="6eef5-131">Configuring from the command line</span></span>

<span data-ttu-id="6eef5-132">Les tâches importantes, telles que le contrôle des paramètres du produit et le déclenchement d’analyses à la demande, peuvent être réalisées à partir de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="6eef5-132">Important tasks, such as controlling product settings and triggering on-demand scans, can be done from the command line:</span></span>

|<span data-ttu-id="6eef5-133">Group</span><span class="sxs-lookup"><span data-stu-id="6eef5-133">Group</span></span>        |<span data-ttu-id="6eef5-134">Scénario</span><span class="sxs-lookup"><span data-stu-id="6eef5-134">Scenario</span></span>                                   |<span data-ttu-id="6eef5-135">Commande</span><span class="sxs-lookup"><span data-stu-id="6eef5-135">Command</span></span>                                                                           |
|-------------|-------------------------------------------|----------------------------------------------------------------------------------|
|<span data-ttu-id="6eef5-136">Configuration</span><span class="sxs-lookup"><span data-stu-id="6eef5-136">Configuration</span></span>|<span data-ttu-id="6eef5-137">Activer/désactiver la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="6eef5-137">Turn on/off real-time protection</span></span>           |`mdatp config real-time-protection --value [enabled/disabled]`                    |
|<span data-ttu-id="6eef5-138">Configuration</span><span class="sxs-lookup"><span data-stu-id="6eef5-138">Configuration</span></span>|<span data-ttu-id="6eef5-139">Activer/désactiver la protection cloud</span><span class="sxs-lookup"><span data-stu-id="6eef5-139">Turn on/off cloud protection</span></span>               |`mdatp config cloud --value [enabled/disabled]`                                   |
|<span data-ttu-id="6eef5-140">Configuration</span><span class="sxs-lookup"><span data-stu-id="6eef5-140">Configuration</span></span>|<span data-ttu-id="6eef5-141">Activer/désactiver les diagnostics de produit</span><span class="sxs-lookup"><span data-stu-id="6eef5-141">Turn on/off product diagnostics</span></span>            |`mdatp config cloud-diagnostic --value [enabled/disabled]`                        |
|<span data-ttu-id="6eef5-142">Configuration</span><span class="sxs-lookup"><span data-stu-id="6eef5-142">Configuration</span></span>|<span data-ttu-id="6eef5-143">Activer/désactiver l’envoi automatique d’échantillons</span><span class="sxs-lookup"><span data-stu-id="6eef5-143">Turn on/off automatic sample submission</span></span>    |`mdatp config cloud-automatic-sample-submission --value [enabled/disabled]`       |
|<span data-ttu-id="6eef5-144">Configuration</span><span class="sxs-lookup"><span data-stu-id="6eef5-144">Configuration</span></span>|<span data-ttu-id="6eef5-145">Ajouter un nom de menace à la liste autorisée</span><span class="sxs-lookup"><span data-stu-id="6eef5-145">Add a threat name to the allowed list</span></span>      |`mdatp threat allowed add --name [threat-name]`                                   |
|<span data-ttu-id="6eef5-146">Configuration</span><span class="sxs-lookup"><span data-stu-id="6eef5-146">Configuration</span></span>|<span data-ttu-id="6eef5-147">Supprimer un nom de menace de la liste autorisée</span><span class="sxs-lookup"><span data-stu-id="6eef5-147">Remove a threat name from the allowed list</span></span> |`mdatp threat allowed remove --name [threat-name]`                                |
|<span data-ttu-id="6eef5-148">Configuration</span><span class="sxs-lookup"><span data-stu-id="6eef5-148">Configuration</span></span>|<span data-ttu-id="6eef5-149">Liste de tous les noms de menaces autorisés</span><span class="sxs-lookup"><span data-stu-id="6eef5-149">List all allowed threat names</span></span>              |`mdatp threat allowed list`                                                       |
|<span data-ttu-id="6eef5-150">Configuration</span><span class="sxs-lookup"><span data-stu-id="6eef5-150">Configuration</span></span>|<span data-ttu-id="6eef5-151">Activer la protection PUA</span><span class="sxs-lookup"><span data-stu-id="6eef5-151">Turn on PUA protection</span></span>                     |`mdatp threat policy set --type potentially_unwanted_application -- action block` |
|<span data-ttu-id="6eef5-152">Configuration</span><span class="sxs-lookup"><span data-stu-id="6eef5-152">Configuration</span></span>|<span data-ttu-id="6eef5-153">Désactiver la protection PUA</span><span class="sxs-lookup"><span data-stu-id="6eef5-153">Turn off PUA protection</span></span>                    |`mdatp threat policy set --type potentially_unwanted_application -- action off`   |
|<span data-ttu-id="6eef5-154">Configuration</span><span class="sxs-lookup"><span data-stu-id="6eef5-154">Configuration</span></span>|<span data-ttu-id="6eef5-155">Activer le mode audit pour la protection PUA</span><span class="sxs-lookup"><span data-stu-id="6eef5-155">Turn on audit mode for PUA protection</span></span>      |`mdatp threat policy set --type potentially_unwanted_application -- action audit` |
|<span data-ttu-id="6eef5-156">Configuration</span><span class="sxs-lookup"><span data-stu-id="6eef5-156">Configuration</span></span>|<span data-ttu-id="6eef5-157">Activer/désactiver passiveMode</span><span class="sxs-lookup"><span data-stu-id="6eef5-157">Turn on/off passiveMode</span></span>                    |`mdatp config passive-mode --value enabled [enabled/disabled]`                    |
|<span data-ttu-id="6eef5-158">Diagnostics</span><span class="sxs-lookup"><span data-stu-id="6eef5-158">Diagnostics</span></span>  |<span data-ttu-id="6eef5-159">Modifier le niveau de journal</span><span class="sxs-lookup"><span data-stu-id="6eef5-159">Change the log level</span></span>                       |`mdatp log level set --level [error/warning/info/verbose]`                        |
|<span data-ttu-id="6eef5-160">Diagnostics</span><span class="sxs-lookup"><span data-stu-id="6eef5-160">Diagnostics</span></span>  |<span data-ttu-id="6eef5-161">Générer des journaux de diagnostic</span><span class="sxs-lookup"><span data-stu-id="6eef5-161">Generate diagnostic logs</span></span>                   |`mdatp diagnostic create --path [directory]`                                      |
|<span data-ttu-id="6eef5-162">Intégrité</span><span class="sxs-lookup"><span data-stu-id="6eef5-162">Health</span></span>       |<span data-ttu-id="6eef5-163">Vérifier l’état du produit</span><span class="sxs-lookup"><span data-stu-id="6eef5-163">Check the product's health</span></span>                 |`mdatp health`                                                                    |
|<span data-ttu-id="6eef5-164">Intégrité</span><span class="sxs-lookup"><span data-stu-id="6eef5-164">Health</span></span>       |<span data-ttu-id="6eef5-165">Vérifier l’attribut d’un produit de harpon</span><span class="sxs-lookup"><span data-stu-id="6eef5-165">Check for a spefic product attribute</span></span>       |`mdatp health --field [attribute: healthy/licensed/engine_version...]`            |
|<span data-ttu-id="6eef5-166">Protection</span><span class="sxs-lookup"><span data-stu-id="6eef5-166">Protection</span></span>   |<span data-ttu-id="6eef5-167">Analyser un chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6eef5-167">Scan a path</span></span>                                |`mdatp scan custom --path [path] [--ignore-exclusions]`                           |
|<span data-ttu-id="6eef5-168">Protection</span><span class="sxs-lookup"><span data-stu-id="6eef5-168">Protection</span></span>   |<span data-ttu-id="6eef5-169">Faire une analyse rapide</span><span class="sxs-lookup"><span data-stu-id="6eef5-169">Do a quick scan</span></span>                            |`mdatp scan quick`                                                                |
|<span data-ttu-id="6eef5-170">Protection</span><span class="sxs-lookup"><span data-stu-id="6eef5-170">Protection</span></span>   |<span data-ttu-id="6eef5-171">Faire une analyse complète</span><span class="sxs-lookup"><span data-stu-id="6eef5-171">Do a full scan</span></span>                             |`mdatp scan full`                                                                 |
|<span data-ttu-id="6eef5-172">Protection</span><span class="sxs-lookup"><span data-stu-id="6eef5-172">Protection</span></span>   |<span data-ttu-id="6eef5-173">Annuler une analyse à la demande en cours</span><span class="sxs-lookup"><span data-stu-id="6eef5-173">Cancel an ongoing on-demand scan</span></span>           |`mdatp scan cancel`                                                               |
|<span data-ttu-id="6eef5-174">Protection</span><span class="sxs-lookup"><span data-stu-id="6eef5-174">Protection</span></span>   |<span data-ttu-id="6eef5-175">Demander une mise à jour des informations de sécurité</span><span class="sxs-lookup"><span data-stu-id="6eef5-175">Request a security intelligence update</span></span>     |`mdatp definitions update`                                                        |
|<span data-ttu-id="6eef5-176">EDR</span><span class="sxs-lookup"><span data-stu-id="6eef5-176">EDR</span></span>          |<span data-ttu-id="6eef5-177">Ajouter une balise de groupe à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6eef5-177">Add group tag to device.</span></span> <span data-ttu-id="6eef5-178">Les balises EDR sont utilisées pour gérer les groupes d’appareils.</span><span class="sxs-lookup"><span data-stu-id="6eef5-178">EDR tags are used for managing device groups.</span></span> <span data-ttu-id="6eef5-179">Pour plus d’informations, visitez https://docs.microsoft.com/microsoft-365/security/defender-endpoint/machine-groups</span><span class="sxs-lookup"><span data-stu-id="6eef5-179">For more information, please visit https://docs.microsoft.com/microsoft-365/security/defender-endpoint/machine-groups</span></span> |`mdatp edr tag set --name GROUP --value [name]` |
|<span data-ttu-id="6eef5-180">EDR</span><span class="sxs-lookup"><span data-stu-id="6eef5-180">EDR</span></span>          |<span data-ttu-id="6eef5-181">Supprimer une balise de groupe de l’appareil</span><span class="sxs-lookup"><span data-stu-id="6eef5-181">Remove group tag from device</span></span>               |`mdatp edr tag remove --tag-name [name]`                                          |
|<span data-ttu-id="6eef5-182">EDR</span><span class="sxs-lookup"><span data-stu-id="6eef5-182">EDR</span></span>          |<span data-ttu-id="6eef5-183">Ajouter un ID de groupe</span><span class="sxs-lookup"><span data-stu-id="6eef5-183">Add Group ID</span></span>                               |`mdatp edr group-ids --group-id [group]`                                          |

### <a name="how-to-enable-autocompletion"></a><span data-ttu-id="6eef5-184">Comment activer lacompletion automatique</span><span class="sxs-lookup"><span data-stu-id="6eef5-184">How to enable autocompletion</span></span>

<span data-ttu-id="6eef5-185">Pour activer lacompletion automatique dans Bash, exécutez la commande suivante et redémarrez la session Terminal :</span><span class="sxs-lookup"><span data-stu-id="6eef5-185">To enable autocompletion in bash, run the following command and restart the Terminal session:</span></span>

```bash
echo "source /Applications/Microsoft\ Defender\ ATP.app/Contents/Resources/Tools/mdatp_completion.bash" >> ~/.bash_profile
```

<span data-ttu-id="6eef5-186">Pour activer lacompletion automatique dans zsh :</span><span class="sxs-lookup"><span data-stu-id="6eef5-186">To enable autocompletion in zsh:</span></span>

- <span data-ttu-id="6eef5-187">Vérifiez si lacompletion automatique est activée sur votre appareil :</span><span class="sxs-lookup"><span data-stu-id="6eef5-187">Check whether autocompletion is enabled on your device:</span></span>

   ```zsh
   cat ~/.zshrc | grep autoload
   ```

- <span data-ttu-id="6eef5-188">Si la commande précédente ne produit aucune sortie, vous pouvez activer lacomplémentation automatique à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="6eef5-188">If the preceding command does not produce any output, you can enable autocompletion using the following command:</span></span>

   ```zsh
   echo "autoload -Uz compinit && compinit" >> ~/.zshrc
   ```

- <span data-ttu-id="6eef5-189">Exécutez les commandes suivantes pour activer lacompletion automatique pour Microsoft Defender pour Endpoint pour Mac et redémarrer la session Terminal :</span><span class="sxs-lookup"><span data-stu-id="6eef5-189">Run the following commands to enable autocompletion for Microsoft Defender for Endpoint for Mac and restart the Terminal session:</span></span>

   ```zsh
   sudo mkdir -p /usr/local/share/zsh/site-functions
   ```
   ```zsh
   sudo ln -svf "/Applications/Microsoft Defender ATP.app/Contents/Resources/Tools/mdatp_completion.zsh" /usr/local/share/zsh/site-functions/_mdatp
   ```

## <a name="client-microsoft-defender-for-endpoint-quarantine-directory"></a><span data-ttu-id="6eef5-190">Répertoire de mise en quarantaine du client Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="6eef5-190">Client Microsoft Defender for Endpoint quarantine directory</span></span>

<span data-ttu-id="6eef5-191">`/Library/Application Support/Microsoft/Defender/quarantine/` contient les fichiers mis en quarantaine par `mdatp` .</span><span class="sxs-lookup"><span data-stu-id="6eef5-191">`/Library/Application Support/Microsoft/Defender/quarantine/` contains the files quarantined by `mdatp`.</span></span> <span data-ttu-id="6eef5-192">Les fichiers sont nommés d’après l’threat trackingId.</span><span class="sxs-lookup"><span data-stu-id="6eef5-192">The files are named after the threat trackingId.</span></span> <span data-ttu-id="6eef5-193">Le trackingIds actuel est affiché avec `mdatp threat list` .</span><span class="sxs-lookup"><span data-stu-id="6eef5-193">The current trackingIds is shown with `mdatp threat list`.</span></span>

## <a name="microsoft-defender-for-endpoint-portal-information"></a><span data-ttu-id="6eef5-194">Informations du portail Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="6eef5-194">Microsoft Defender for Endpoint portal information</span></span>

<span data-ttu-id="6eef5-195">[Les fonctionnalités EDR](https://techcommunity.microsoft.com/t5/microsoft-defender-atp/edr-capabilities-for-macos-have-now-arrived/ba-p/1047801)pour macOS sont désormais arrivées, sur le blog Microsoft Defender for Endpoint, qui fournit des instructions détaillées sur ce à quoi vous devez vous attendre dans le Centre de sécurité Microsoft Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="6eef5-195">[EDR capabilities for macOS have now arrived](https://techcommunity.microsoft.com/t5/microsoft-defender-atp/edr-capabilities-for-macos-have-now-arrived/ba-p/1047801), on the Microsoft Defender for Endpoint blog, provides detailed guidance on what to expect in Microsoft Defender for Endpoint Security Center.</span></span>