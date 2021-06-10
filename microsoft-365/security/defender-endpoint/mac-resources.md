---
title: Ressources pour Microsoft Defender pour point de terminaison sur Mac
description: Ressources pour Microsoft Defender pour le point de terminaison sur Mac, notamment comment le désinstaller, comment collecter des journaux de diagnostic, des commandes CLI et des problèmes connus avec le produit.
keywords: microsoft, defender, Microsoft Defender pour point de terminaison, mac, installation, déployer, désinstallation, intune, jamf, macos,pératin, mojave, high sierra
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
ms.openlocfilehash: fa5d5b4470644e1ff50af46a8dd3f035cd9b3184
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52842865"
---
# <a name="resources-for-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="29b1f-104">Ressources pour Microsoft Defender pour point de terminaison sur macOS</span><span class="sxs-lookup"><span data-stu-id="29b1f-104">Resources for Microsoft Defender for Endpoint on macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="29b1f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="29b1f-105">**Applies to:**</span></span>

- [<span data-ttu-id="29b1f-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="29b1f-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="29b1f-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="29b1f-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="29b1f-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="29b1f-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="29b1f-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="29b1f-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

## <a name="collecting-diagnostic-information"></a><span data-ttu-id="29b1f-110">Collecte d’informations de diagnostic</span><span class="sxs-lookup"><span data-stu-id="29b1f-110">Collecting diagnostic information</span></span>

<span data-ttu-id="29b1f-111">Si vous pouvez reproduire un problème, augmentez le niveau de journalisation, exécutez le système pendant un certain temps et rétablissez le niveau de journalisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="29b1f-111">If you can reproduce a problem, increase the logging level, run the system for some time, and restore the logging level to the default.</span></span>

1. <span data-ttu-id="29b1f-112">Augmenter le niveau de journalisation :</span><span class="sxs-lookup"><span data-stu-id="29b1f-112">Increase logging level:</span></span>

   ```bash
   mdatp log level set --level verbose
   ```

   ```Output
   Log level configured successfully
   ```

2. <span data-ttu-id="29b1f-113">Reproduire le problème</span><span class="sxs-lookup"><span data-stu-id="29b1f-113">Reproduce the problem</span></span>

3. <span data-ttu-id="29b1f-114">Exécutez `sudo mdatp diagnostic create` cette session pour enregistrer les journaux microsoft Defender pour les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="29b1f-114">Run `sudo mdatp diagnostic create` to back up the Microsoft Defender for Endpoint logs.</span></span> <span data-ttu-id="29b1f-115">Les fichiers sont stockés dans une archive .zip de données.</span><span class="sxs-lookup"><span data-stu-id="29b1f-115">The files will be stored inside a .zip archive.</span></span> <span data-ttu-id="29b1f-116">Cette commande imprime également le chemin d’accès du fichier à la sauvegarde une fois l’opération réussie.</span><span class="sxs-lookup"><span data-stu-id="29b1f-116">This command will also print out the file path to the backup after the operation succeeds.</span></span>

   > [!TIP]
   > <span data-ttu-id="29b1f-117">Par défaut, les journaux de diagnostic sont enregistrés dans `/Library/Application Support/Microsoft/Defender/wdavdiag/` .</span><span class="sxs-lookup"><span data-stu-id="29b1f-117">By default, diagnostic logs are saved to `/Library/Application Support/Microsoft/Defender/wdavdiag/`.</span></span> <span data-ttu-id="29b1f-118">Pour modifier le répertoire dans lequel les journaux de diagnostic sont enregistrés, passez à la commande ci-dessous, en remplaçant par le `--path [directory]` `[directory]` répertoire souhaité.</span><span class="sxs-lookup"><span data-stu-id="29b1f-118">To change the directory where diagnostic logs are saved, pass `--path [directory]` to the below command, replacing `[directory]` with the desired directory.</span></span>

   ```bash
   sudo mdatp diagnostic create
   ```

   ```console
   Diagnostic file created: "/Library/Application Support/Microsoft/Defender/wdavdiag/932e68a8-8f2e-4ad0-a7f2-65eb97c0de01.zip"
   ```

4. <span data-ttu-id="29b1f-119">Restaurer le niveau de journalisation :</span><span class="sxs-lookup"><span data-stu-id="29b1f-119">Restore logging level:</span></span>

   ```bash
   mdatp log level set --level info
   ```

   ```console
   Log level configured successfully
   ```

## <a name="logging-installation-issues"></a><span data-ttu-id="29b1f-120">Journalisation des problèmes d’installation</span><span class="sxs-lookup"><span data-stu-id="29b1f-120">Logging installation issues</span></span>

<span data-ttu-id="29b1f-121">Si une erreur se produit pendant l’installation, le programme d’installation signale uniquement un échec général.</span><span class="sxs-lookup"><span data-stu-id="29b1f-121">If an error occurs during installation, the installer will only report a general failure.</span></span>

<span data-ttu-id="29b1f-122">Le journal détaillé sera enregistré dans `/Library/Logs/Microsoft/mdatp/install.log` .</span><span class="sxs-lookup"><span data-stu-id="29b1f-122">The detailed log will be saved to `/Library/Logs/Microsoft/mdatp/install.log`.</span></span> <span data-ttu-id="29b1f-123">Si vous avez des problèmes lors de l’installation, envoyez-nous ce fichier afin que nous aidions à diagnostiquer la cause.</span><span class="sxs-lookup"><span data-stu-id="29b1f-123">If you experience issues during installation, send us this file so we can help diagnose the cause.</span></span>

## <a name="uninstalling"></a><span data-ttu-id="29b1f-124">Désinstallation</span><span class="sxs-lookup"><span data-stu-id="29b1f-124">Uninstalling</span></span>

<span data-ttu-id="29b1f-125">Il existe plusieurs façons de désinstaller Microsoft Defender pour Endpoint sur macOS.</span><span class="sxs-lookup"><span data-stu-id="29b1f-125">There are several ways to uninstall Microsoft Defender for Endpoint on macOS.</span></span> <span data-ttu-id="29b1f-126">Notez que bien que la désinstallation gérée de manière centralisée soit disponible sur JAMF, elle n’est pas encore disponible pour les Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="29b1f-126">Note that while centrally managed uninstall is available on JAMF, it is not yet available for Microsoft Intune.</span></span>

### <a name="interactive-uninstallation"></a><span data-ttu-id="29b1f-127">Désinstallation interactive</span><span class="sxs-lookup"><span data-stu-id="29b1f-127">Interactive uninstallation</span></span>

- <span data-ttu-id="29b1f-128">Ouvrez **Finder > Applications.**</span><span class="sxs-lookup"><span data-stu-id="29b1f-128">Open **Finder > Applications**.</span></span> <span data-ttu-id="29b1f-129">Cliquez avec le bouton **droit sur Microsoft Defender pour le point de terminaison > déplacer vers la corbeille.**</span><span class="sxs-lookup"><span data-stu-id="29b1f-129">Right click on **Microsoft Defender for Endpoint > Move to Trash**.</span></span>

### <a name="from-the-command-line"></a><span data-ttu-id="29b1f-130">À partir de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="29b1f-130">From the command line</span></span>

- ```sudo '/Library/Application Support/Microsoft/Defender/uninstall/uninstall'```

## <a name="configuring-from-the-command-line"></a><span data-ttu-id="29b1f-131">Configuration à partir de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="29b1f-131">Configuring from the command line</span></span>

<span data-ttu-id="29b1f-132">Les tâches importantes, telles que le contrôle des paramètres du produit et le déclenchement d’analyses à la demande, peuvent être réalisées à partir de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="29b1f-132">Important tasks, such as controlling product settings and triggering on-demand scans, can be done from the command line:</span></span>

|<span data-ttu-id="29b1f-133">Group</span><span class="sxs-lookup"><span data-stu-id="29b1f-133">Group</span></span>        |<span data-ttu-id="29b1f-134">Scénario</span><span class="sxs-lookup"><span data-stu-id="29b1f-134">Scenario</span></span>                                   |<span data-ttu-id="29b1f-135">Commande</span><span class="sxs-lookup"><span data-stu-id="29b1f-135">Command</span></span>                                                                           |
|-------------|-------------------------------------------|----------------------------------------------------------------------------------|
|<span data-ttu-id="29b1f-136">Configuration</span><span class="sxs-lookup"><span data-stu-id="29b1f-136">Configuration</span></span>|<span data-ttu-id="29b1f-137">Activer/désactiver la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="29b1f-137">Turn on/off real-time protection</span></span>           |`mdatp config real-time-protection --value [enabled/disabled]`                    |
|<span data-ttu-id="29b1f-138">Configuration</span><span class="sxs-lookup"><span data-stu-id="29b1f-138">Configuration</span></span>|<span data-ttu-id="29b1f-139">Activer/désactiver la protection cloud</span><span class="sxs-lookup"><span data-stu-id="29b1f-139">Turn on/off cloud protection</span></span>               |`mdatp config cloud --value [enabled/disabled]`                                   |
|<span data-ttu-id="29b1f-140">Configuration</span><span class="sxs-lookup"><span data-stu-id="29b1f-140">Configuration</span></span>|<span data-ttu-id="29b1f-141">Activer/désactiver les diagnostics de produit</span><span class="sxs-lookup"><span data-stu-id="29b1f-141">Turn on/off product diagnostics</span></span>            |`mdatp config cloud-diagnostic --value [enabled/disabled]`                        |
|<span data-ttu-id="29b1f-142">Configuration</span><span class="sxs-lookup"><span data-stu-id="29b1f-142">Configuration</span></span>|<span data-ttu-id="29b1f-143">Activer/désactiver l’envoi automatique d’échantillons</span><span class="sxs-lookup"><span data-stu-id="29b1f-143">Turn on/off automatic sample submission</span></span>    |`mdatp config cloud-automatic-sample-submission --value [enabled/disabled]`       |
|<span data-ttu-id="29b1f-144">Configuration</span><span class="sxs-lookup"><span data-stu-id="29b1f-144">Configuration</span></span>|<span data-ttu-id="29b1f-145">Ajouter un nom de menace à la liste autorisée</span><span class="sxs-lookup"><span data-stu-id="29b1f-145">Add a threat name to the allowed list</span></span>      |`mdatp threat allowed add --name [threat-name]`                                   |
|<span data-ttu-id="29b1f-146">Configuration</span><span class="sxs-lookup"><span data-stu-id="29b1f-146">Configuration</span></span>|<span data-ttu-id="29b1f-147">Supprimer un nom de menace de la liste autorisée</span><span class="sxs-lookup"><span data-stu-id="29b1f-147">Remove a threat name from the allowed list</span></span> |`mdatp threat allowed remove --name [threat-name]`                                |
|<span data-ttu-id="29b1f-148">Configuration</span><span class="sxs-lookup"><span data-stu-id="29b1f-148">Configuration</span></span>|<span data-ttu-id="29b1f-149">Liste de tous les noms de menaces autorisés</span><span class="sxs-lookup"><span data-stu-id="29b1f-149">List all allowed threat names</span></span>              |`mdatp threat allowed list`                                                       |
|<span data-ttu-id="29b1f-150">Configuration</span><span class="sxs-lookup"><span data-stu-id="29b1f-150">Configuration</span></span>|<span data-ttu-id="29b1f-151">Activer la protection PUA</span><span class="sxs-lookup"><span data-stu-id="29b1f-151">Turn on PUA protection</span></span>                     |`mdatp threat policy set --type potentially_unwanted_application -- action block` |
|<span data-ttu-id="29b1f-152">Configuration</span><span class="sxs-lookup"><span data-stu-id="29b1f-152">Configuration</span></span>|<span data-ttu-id="29b1f-153">Désactiver la protection PUA</span><span class="sxs-lookup"><span data-stu-id="29b1f-153">Turn off PUA protection</span></span>                    |`mdatp threat policy set --type potentially_unwanted_application -- action off`   |
|<span data-ttu-id="29b1f-154">Configuration</span><span class="sxs-lookup"><span data-stu-id="29b1f-154">Configuration</span></span>|<span data-ttu-id="29b1f-155">Activer le mode audit pour la protection PUA</span><span class="sxs-lookup"><span data-stu-id="29b1f-155">Turn on audit mode for PUA protection</span></span>      |`mdatp threat policy set --type potentially_unwanted_application -- action audit` |
|<span data-ttu-id="29b1f-156">Configuration</span><span class="sxs-lookup"><span data-stu-id="29b1f-156">Configuration</span></span>|<span data-ttu-id="29b1f-157">Activer/désactiver passiveMode</span><span class="sxs-lookup"><span data-stu-id="29b1f-157">Turn on/off passiveMode</span></span>                    |`mdatp config passive-mode --value enabled [enabled/disabled]`                    |
|<span data-ttu-id="29b1f-158">Diagnostics</span><span class="sxs-lookup"><span data-stu-id="29b1f-158">Diagnostics</span></span>  |<span data-ttu-id="29b1f-159">Modifier le niveau de journal</span><span class="sxs-lookup"><span data-stu-id="29b1f-159">Change the log level</span></span>                       |`mdatp log level set --level [error/warning/info/verbose]`                        |
|<span data-ttu-id="29b1f-160">Diagnostics</span><span class="sxs-lookup"><span data-stu-id="29b1f-160">Diagnostics</span></span>  |<span data-ttu-id="29b1f-161">Générer des journaux de diagnostic</span><span class="sxs-lookup"><span data-stu-id="29b1f-161">Generate diagnostic logs</span></span>                   |`mdatp diagnostic create --path [directory]`                                      |
|<span data-ttu-id="29b1f-162">Intégrité</span><span class="sxs-lookup"><span data-stu-id="29b1f-162">Health</span></span>       |<span data-ttu-id="29b1f-163">Vérifier l’état du produit</span><span class="sxs-lookup"><span data-stu-id="29b1f-163">Check the product's health</span></span>                 |`mdatp health`                                                                    |
|<span data-ttu-id="29b1f-164">Intégrité</span><span class="sxs-lookup"><span data-stu-id="29b1f-164">Health</span></span>       |<span data-ttu-id="29b1f-165">Vérifier l’attribut d’un produit de harpon</span><span class="sxs-lookup"><span data-stu-id="29b1f-165">Check for a spefic product attribute</span></span>       |`mdatp health --field [attribute: healthy/licensed/engine_version...]`            |
|<span data-ttu-id="29b1f-166">Protection</span><span class="sxs-lookup"><span data-stu-id="29b1f-166">Protection</span></span>   |<span data-ttu-id="29b1f-167">Analyser un chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="29b1f-167">Scan a path</span></span>                                |`mdatp scan custom --path [path] [--ignore-exclusions]`                           |
|<span data-ttu-id="29b1f-168">Protection</span><span class="sxs-lookup"><span data-stu-id="29b1f-168">Protection</span></span>   |<span data-ttu-id="29b1f-169">Faire une analyse rapide</span><span class="sxs-lookup"><span data-stu-id="29b1f-169">Do a quick scan</span></span>                            |`mdatp scan quick`                                                                |
|<span data-ttu-id="29b1f-170">Protection</span><span class="sxs-lookup"><span data-stu-id="29b1f-170">Protection</span></span>   |<span data-ttu-id="29b1f-171">Faire une analyse complète</span><span class="sxs-lookup"><span data-stu-id="29b1f-171">Do a full scan</span></span>                             |`mdatp scan full`                                                                 |
|<span data-ttu-id="29b1f-172">Protection</span><span class="sxs-lookup"><span data-stu-id="29b1f-172">Protection</span></span>   |<span data-ttu-id="29b1f-173">Annuler une analyse à la demande en cours</span><span class="sxs-lookup"><span data-stu-id="29b1f-173">Cancel an ongoing on-demand scan</span></span>           |`mdatp scan cancel`                                                               |
|<span data-ttu-id="29b1f-174">Protection</span><span class="sxs-lookup"><span data-stu-id="29b1f-174">Protection</span></span>   |<span data-ttu-id="29b1f-175">Demander une mise à jour des informations de sécurité</span><span class="sxs-lookup"><span data-stu-id="29b1f-175">Request a security intelligence update</span></span>     |`mdatp definitions update`                                                        |
|<span data-ttu-id="29b1f-176">PEPT</span><span class="sxs-lookup"><span data-stu-id="29b1f-176">EDR</span></span>          |<span data-ttu-id="29b1f-177">Ajouter une balise de groupe à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="29b1f-177">Add group tag to device.</span></span> <span data-ttu-id="29b1f-178">PEPT balises sont utilisées pour gérer les groupes d’appareils.</span><span class="sxs-lookup"><span data-stu-id="29b1f-178">EDR tags are used for managing device groups.</span></span> <span data-ttu-id="29b1f-179">Pour plus d’informations, visitez /microsoft-365/security/defender-endpoint/machine-groups</span><span class="sxs-lookup"><span data-stu-id="29b1f-179">For more information, please visit /microsoft-365/security/defender-endpoint/machine-groups</span></span> |`mdatp edr tag set --name GROUP --value [name]` |
|<span data-ttu-id="29b1f-180">PEPT</span><span class="sxs-lookup"><span data-stu-id="29b1f-180">EDR</span></span>          |<span data-ttu-id="29b1f-181">Supprimer une balise de groupe de l’appareil</span><span class="sxs-lookup"><span data-stu-id="29b1f-181">Remove group tag from device</span></span>               |`mdatp edr tag remove --tag-name [name]`                                          |
|<span data-ttu-id="29b1f-182">PEPT</span><span class="sxs-lookup"><span data-stu-id="29b1f-182">EDR</span></span>          |<span data-ttu-id="29b1f-183">Ajouter un ID de groupe</span><span class="sxs-lookup"><span data-stu-id="29b1f-183">Add Group ID</span></span>                               |`mdatp edr group-ids --group-id [group]`                                          |

### <a name="how-to-enable-autocompletion"></a><span data-ttu-id="29b1f-184">Comment activer lacompletion automatique</span><span class="sxs-lookup"><span data-stu-id="29b1f-184">How to enable autocompletion</span></span>

<span data-ttu-id="29b1f-185">Pour activer lacompletion automatique dans Bash, exécutez la commande suivante et redémarrez la session Terminal :</span><span class="sxs-lookup"><span data-stu-id="29b1f-185">To enable autocompletion in bash, run the following command and restart the Terminal session:</span></span>

```bash
echo "source /Applications/Microsoft\ Defender\ ATP.app/Contents/Resources/Tools/mdatp_completion.bash" >> ~/.bash_profile
```

<span data-ttu-id="29b1f-186">Pour activer lacompletion automatique dans zsh :</span><span class="sxs-lookup"><span data-stu-id="29b1f-186">To enable autocompletion in zsh:</span></span>

- <span data-ttu-id="29b1f-187">Vérifiez si lacompletion automatique est activée sur votre appareil :</span><span class="sxs-lookup"><span data-stu-id="29b1f-187">Check whether autocompletion is enabled on your device:</span></span>

   ```zsh
   cat ~/.zshrc | grep autoload
   ```

- <span data-ttu-id="29b1f-188">Si la commande précédente ne produit aucune sortie, vous pouvez activer lacomplémentation automatique à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="29b1f-188">If the preceding command does not produce any output, you can enable autocompletion using the following command:</span></span>

   ```zsh
   echo "autoload -Uz compinit && compinit" >> ~/.zshrc
   ```

- <span data-ttu-id="29b1f-189">Exécutez les commandes suivantes pour activer lacompletion automatique pour Microsoft Defender pour Endpoint sur macOS et redémarrez la session Terminal :</span><span class="sxs-lookup"><span data-stu-id="29b1f-189">Run the following commands to enable autocompletion for Microsoft Defender for Endpoint on macOS and restart the Terminal session:</span></span>

   ```zsh
   sudo mkdir -p /usr/local/share/zsh/site-functions
   ```
   ```zsh
   sudo ln -svf "/Applications/Microsoft Defender ATP.app/Contents/Resources/Tools/mdatp_completion.zsh" /usr/local/share/zsh/site-functions/_mdatp
   ```

## <a name="client-microsoft-defender-for-endpoint-quarantine-directory"></a><span data-ttu-id="29b1f-190">Répertoire de mise en quarantaine du client Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="29b1f-190">Client Microsoft Defender for Endpoint quarantine directory</span></span>

<span data-ttu-id="29b1f-191">`/Library/Application Support/Microsoft/Defender/quarantine/` contient les fichiers mis en quarantaine par `mdatp` .</span><span class="sxs-lookup"><span data-stu-id="29b1f-191">`/Library/Application Support/Microsoft/Defender/quarantine/` contains the files quarantined by `mdatp`.</span></span> <span data-ttu-id="29b1f-192">Les fichiers sont nommés d’après l’threat trackingId.</span><span class="sxs-lookup"><span data-stu-id="29b1f-192">The files are named after the threat trackingId.</span></span> <span data-ttu-id="29b1f-193">Le trackingIds actuel est affiché avec `mdatp threat list` .</span><span class="sxs-lookup"><span data-stu-id="29b1f-193">The current trackingIds is shown with `mdatp threat list`.</span></span>

## <a name="microsoft-defender-for-endpoint-portal-information"></a><span data-ttu-id="29b1f-194">Informations du portail Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="29b1f-194">Microsoft Defender for Endpoint portal information</span></span>

<span data-ttu-id="29b1f-195">PEPT fonctionnalités pour [macOS](https://techcommunity.microsoft.com/t5/microsoft-defender-atp/edr-capabilities-for-macos-have-now-arrived/ba-p/1047801)sont désormais arrivées, sur le blog Microsoft Defender pour point de terminaison, fournit des instructions détaillées sur ce à quoi vous devez vous attendre dans Microsoft Defender pour le Centre de sécurité des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="29b1f-195">[EDR capabilities for macOS have now arrived](https://techcommunity.microsoft.com/t5/microsoft-defender-atp/edr-capabilities-for-macos-have-now-arrived/ba-p/1047801), on the Microsoft Defender for Endpoint blog, provides detailed guidance on what to expect in Microsoft Defender for Endpoint Security Center.</span></span>
