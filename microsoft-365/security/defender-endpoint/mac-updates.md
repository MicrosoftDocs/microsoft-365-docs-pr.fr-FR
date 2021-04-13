---
title: Déployer les mises à jour de Microsoft Defender ATP pour Mac
description: Contrôler les mises à jour de Microsoft Defender ATP pour Mac dans les environnements d'entreprise.
keywords: microsoft, defender, atp, mac, mises à jour, déployer
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
ms.openlocfilehash: 3321c1bd181b89c53e2618fc20fa7f733a20cfc1
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51689052"
---
# <a name="deploy-updates-for-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="402ae-104">Déployer les mises à jour de Microsoft Defender pour endpoint sur macOS</span><span class="sxs-lookup"><span data-stu-id="402ae-104">Deploy updates for Microsoft Defender for Endpoint on macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="402ae-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="402ae-105">**Applies to:**</span></span>

- [<span data-ttu-id="402ae-106">Microsoft Defender pour point de terminaison sur macOS</span><span class="sxs-lookup"><span data-stu-id="402ae-106">Microsoft Defender for Endpoint on macOS</span></span>](microsoft-defender-endpoint-mac.md)
- [<span data-ttu-id="402ae-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="402ae-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="402ae-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="402ae-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="402ae-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="402ae-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="402ae-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="402ae-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="402ae-111">Microsoft publie régulièrement des mises à jour logicielles pour améliorer les performances, la sécurité et fournir de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="402ae-111">Microsoft regularly publishes software updates to improve performance, security, and to deliver new features.</span></span>

<span data-ttu-id="402ae-112">Pour mettre à jour Microsoft Defender pour endpoint sur macOS, un programme nommé Microsoft AutoUpdate (MAU) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="402ae-112">To update Microsoft Defender for Endpoint on macOS, a program named Microsoft AutoUpdate (MAU) is used.</span></span> <span data-ttu-id="402ae-113">Par défaut, MAU recherche automatiquement les mises à jour quotidiennes, mais vous pouvez la modifier en une fois par semaine, par mois ou manuellement.</span><span class="sxs-lookup"><span data-stu-id="402ae-113">By default, MAU automatically checks for updates daily, but you can change that to weekly, monthly, or manually.</span></span>

![Capture d'écran MAU](images/MDATP-34-MAU.png)

<span data-ttu-id="402ae-115">Si vous décidez de déployer des mises à jour à l'aide de vos outils de distribution de logiciels, vous devez configurer MAU pour vérifier manuellement les mises à jour logicielles.</span><span class="sxs-lookup"><span data-stu-id="402ae-115">If you decide to deploy updates by using your software distribution tools, you should configure MAU to manually check for software updates.</span></span> <span data-ttu-id="402ae-116">Vous pouvez déployer des préférences pour configurer comment et quand MAU recherche les mises à jour pour les Mac de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="402ae-116">You can deploy preferences to configure how and when MAU checks for updates for the Macs in your organization.</span></span>

## <a name="use-msupdate"></a><span data-ttu-id="402ae-117">Utiliser msupdate</span><span class="sxs-lookup"><span data-stu-id="402ae-117">Use msupdate</span></span>

<span data-ttu-id="402ae-118">MAU inclut un outil en ligne de commande, appelé *msupdate,* conçu pour les administrateurs informatiques afin qu'ils contrôlent plus précisément le moment où les mises à jour sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="402ae-118">MAU includes a command-line tool, called *msupdate*, that is designed for IT administrators so that they have more precise control over when updates are applied.</span></span> <span data-ttu-id="402ae-119">Vous pouvez trouver des instructions sur l'utilisation de cet outil dans La mise à [jour d'Office pour Mac à l'aide de msupdate](https://docs.microsoft.com/deployoffice/mac/update-office-for-mac-using-msupdate).</span><span class="sxs-lookup"><span data-stu-id="402ae-119">Instructions for how to use this tool can be found in [Update Office for Mac by using msupdate](https://docs.microsoft.com/deployoffice/mac/update-office-for-mac-using-msupdate).</span></span>

<span data-ttu-id="402ae-120">Dans MAU, l'identificateur d'application pour Microsoft Defender pour le point de terminaison sur macOS est *WDAV00*.</span><span class="sxs-lookup"><span data-stu-id="402ae-120">In MAU, the application identifier for Microsoft Defender for Endpoint on macOS is *WDAV00*.</span></span> <span data-ttu-id="402ae-121">Pour télécharger et installer les dernières mises à jour de Microsoft Defender pour Endpoint sur macOS, exécutez la commande suivante à partir d'une fenêtre Terminal :</span><span class="sxs-lookup"><span data-stu-id="402ae-121">To download and install the latest updates for Microsoft Defender for Endpoint on macOS, execute the following command from a Terminal window:</span></span>

```
./msupdate --install --apps wdav00
```

## <a name="set-preferences-for-microsoft-autoupdate"></a><span data-ttu-id="402ae-122">Définir des préférences pour la mise à jour automatique Microsoft</span><span class="sxs-lookup"><span data-stu-id="402ae-122">Set preferences for Microsoft AutoUpdate</span></span>

<span data-ttu-id="402ae-123">Cette section décrit les préférences les plus courantes qui peuvent être utilisées pour configurer MAU.</span><span class="sxs-lookup"><span data-stu-id="402ae-123">This section describes the most common preferences that can be used to configure MAU.</span></span> <span data-ttu-id="402ae-124">Ces paramètres peuvent être déployés en tant que profil de configuration via la console de gestion que votre entreprise utilise.</span><span class="sxs-lookup"><span data-stu-id="402ae-124">These settings can be deployed as a configuration profile through the management console that your enterprise is using.</span></span> <span data-ttu-id="402ae-125">Un exemple de profil de configuration est illustré dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="402ae-125">An example of a configuration profile is shown in the following sections.</span></span>

### <a name="set-the-channel-name"></a><span data-ttu-id="402ae-126">Définir le nom du canal</span><span class="sxs-lookup"><span data-stu-id="402ae-126">Set the channel name</span></span>

<span data-ttu-id="402ae-127">Le canal détermine le type et la fréquence des mises à jour proposées via MAU.</span><span class="sxs-lookup"><span data-stu-id="402ae-127">The channel determines the type and frequency of updates that are offered through MAU.</span></span> <span data-ttu-id="402ae-128">Les appareils peuvent `Beta` tester de nouvelles fonctionnalités avant d'utiliser `Preview` et `Current` .</span><span class="sxs-lookup"><span data-stu-id="402ae-128">Devices in `Beta` can try out new features before devices in `Preview` and `Current`.</span></span> 

<span data-ttu-id="402ae-129">Le `Current` canal contient la version la plus stable du produit.</span><span class="sxs-lookup"><span data-stu-id="402ae-129">The `Current` channel contains the most stable version of the product.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="402ae-130">Avant la mise à jour automatique Microsoft version 4.29, les canaux avaient des noms différents :</span><span class="sxs-lookup"><span data-stu-id="402ae-130">Prior to Microsoft AutoUpdate version 4.29, channels had different names:</span></span> 
> 
> - <span data-ttu-id="402ae-131">`Beta` a été nommé `InsiderFast` (Insider Fast)</span><span class="sxs-lookup"><span data-stu-id="402ae-131">`Beta` was named `InsiderFast` (Insider Fast)</span></span>
> - <span data-ttu-id="402ae-132">`Preview` a été nommé `External` (Insider Slow)</span><span class="sxs-lookup"><span data-stu-id="402ae-132">`Preview` was named `External` (Insider Slow)</span></span>
> - <span data-ttu-id="402ae-133">`Current` a été nommé `Production`</span><span class="sxs-lookup"><span data-stu-id="402ae-133">`Current` was named `Production`</span></span>

>[!TIP]
><span data-ttu-id="402ae-134">Pour afficher un aperçu des nouvelles fonctionnalités et fournir des commentaires préliminaires, il est recommandé de configurer certains appareils dans votre entreprise sur `Beta` ou `Preview` .</span><span class="sxs-lookup"><span data-stu-id="402ae-134">In order to preview new features and provide early feedback, it is recommended that you configure some devices in your enterprise to `Beta` or `Preview`.</span></span>

|<span data-ttu-id="402ae-135">Section</span><span class="sxs-lookup"><span data-stu-id="402ae-135">Section</span></span>|<span data-ttu-id="402ae-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="402ae-136">Value</span></span>|
|:--|:--|
| <span data-ttu-id="402ae-137">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="402ae-137">**Domain**</span></span> | <span data-ttu-id="402ae-138">com.microsoft.autoupdate2</span><span class="sxs-lookup"><span data-stu-id="402ae-138">com.microsoft.autoupdate2</span></span> |
| <span data-ttu-id="402ae-139">**Key**</span><span class="sxs-lookup"><span data-stu-id="402ae-139">**Key**</span></span> | <span data-ttu-id="402ae-140">ChannelName</span><span class="sxs-lookup"><span data-stu-id="402ae-140">ChannelName</span></span> |
| <span data-ttu-id="402ae-141">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="402ae-141">**Data type**</span></span> | <span data-ttu-id="402ae-142">Chaîne</span><span class="sxs-lookup"><span data-stu-id="402ae-142">String</span></span> |
| <span data-ttu-id="402ae-143">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="402ae-143">**Possible values**</span></span> | <span data-ttu-id="402ae-144">Bêta</span><span class="sxs-lookup"><span data-stu-id="402ae-144">Beta</span></span> <br/> <span data-ttu-id="402ae-145">Aperçu</span><span class="sxs-lookup"><span data-stu-id="402ae-145">Preview</span></span> <br/> <span data-ttu-id="402ae-146">Current</span><span class="sxs-lookup"><span data-stu-id="402ae-146">Current</span></span> |
|||

>[!WARNING]
><span data-ttu-id="402ae-147">Ce paramètre modifie le canal pour toutes les applications qui sont mises à jour via La mise à jour automatique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="402ae-147">This setting changes the channel for all applications that are updated through Microsoft AutoUpdate.</span></span> <span data-ttu-id="402ae-148">Pour modifier le canal uniquement pour Microsoft Defender pour le point de terminaison sur macOS, exécutez la commande suivante après le remplacement par `[channel-name]` le canal souhaité :</span><span class="sxs-lookup"><span data-stu-id="402ae-148">To change the channel only for Microsoft Defender for Endpoint on macOS, execute the following command after replacing `[channel-name]` with the desired channel:</span></span>
> ```bash
> defaults write com.microsoft.autoupdate2 Applications -dict-add "/Applications/Microsoft Defender ATP.app" " { 'Application ID' = 'WDAV00' ; 'App Domain' = 'com.microsoft.wdav' ; LCID = 1033 ; ChannelName = '[channel-name]' ; }"
> ```

### <a name="set-update-check-frequency"></a><span data-ttu-id="402ae-149">Définir la fréquence de vérification des mises à jour</span><span class="sxs-lookup"><span data-stu-id="402ae-149">Set update check frequency</span></span>

<span data-ttu-id="402ae-150">Modifier la fréquence à la recherche de mises à jour par MAU.</span><span class="sxs-lookup"><span data-stu-id="402ae-150">Change how often MAU searches for updates.</span></span>

|<span data-ttu-id="402ae-151">Section</span><span class="sxs-lookup"><span data-stu-id="402ae-151">Section</span></span>|<span data-ttu-id="402ae-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="402ae-152">Value</span></span>|
|:--|:--|
| <span data-ttu-id="402ae-153">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="402ae-153">**Domain**</span></span> | <span data-ttu-id="402ae-154">com.microsoft.autoupdate2</span><span class="sxs-lookup"><span data-stu-id="402ae-154">com.microsoft.autoupdate2</span></span> |
| <span data-ttu-id="402ae-155">**Key**</span><span class="sxs-lookup"><span data-stu-id="402ae-155">**Key**</span></span> | <span data-ttu-id="402ae-156">UpdateCheckFrequency</span><span class="sxs-lookup"><span data-stu-id="402ae-156">UpdateCheckFrequency</span></span> |
| <span data-ttu-id="402ae-157">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="402ae-157">**Data type**</span></span> | <span data-ttu-id="402ae-158">Entier</span><span class="sxs-lookup"><span data-stu-id="402ae-158">Integer</span></span> |
| <span data-ttu-id="402ae-159">**Valeur par défaut**</span><span class="sxs-lookup"><span data-stu-id="402ae-159">**Default value**</span></span> | <span data-ttu-id="402ae-160">720 (minutes)</span><span class="sxs-lookup"><span data-stu-id="402ae-160">720 (minutes)</span></span> |
| <span data-ttu-id="402ae-161">**Comment**</span><span class="sxs-lookup"><span data-stu-id="402ae-161">**Comment**</span></span> | <span data-ttu-id="402ae-162">Cette valeur est définie en minutes.</span><span class="sxs-lookup"><span data-stu-id="402ae-162">This value is set in minutes.</span></span> |


### <a name="change-how-mau-interacts-with-updates"></a><span data-ttu-id="402ae-163">Modifier la façon dont MAU interagit avec les mises à jour</span><span class="sxs-lookup"><span data-stu-id="402ae-163">Change how MAU interacts with updates</span></span>

<span data-ttu-id="402ae-164">Modifier la façon dont MAU recherche les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="402ae-164">Change how MAU searches for updates.</span></span>

|<span data-ttu-id="402ae-165">Section</span><span class="sxs-lookup"><span data-stu-id="402ae-165">Section</span></span>|<span data-ttu-id="402ae-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="402ae-166">Value</span></span>|
|:--|:--|
| <span data-ttu-id="402ae-167">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="402ae-167">**Domain**</span></span> | <span data-ttu-id="402ae-168">com.microsoft.autoupdate2</span><span class="sxs-lookup"><span data-stu-id="402ae-168">com.microsoft.autoupdate2</span></span> |
| <span data-ttu-id="402ae-169">**Key**</span><span class="sxs-lookup"><span data-stu-id="402ae-169">**Key**</span></span> | <span data-ttu-id="402ae-170">HowToCheck</span><span class="sxs-lookup"><span data-stu-id="402ae-170">HowToCheck</span></span> |
| <span data-ttu-id="402ae-171">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="402ae-171">**Data type**</span></span> | <span data-ttu-id="402ae-172">Chaîne</span><span class="sxs-lookup"><span data-stu-id="402ae-172">String</span></span> |
| <span data-ttu-id="402ae-173">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="402ae-173">**Possible values**</span></span> | <span data-ttu-id="402ae-174">Manuel</span><span class="sxs-lookup"><span data-stu-id="402ae-174">Manual</span></span> <br/> <span data-ttu-id="402ae-175">AutomaticCheck</span><span class="sxs-lookup"><span data-stu-id="402ae-175">AutomaticCheck</span></span> <br/> <span data-ttu-id="402ae-176">AutomaticDownload</span><span class="sxs-lookup"><span data-stu-id="402ae-176">AutomaticDownload</span></span> |
| <span data-ttu-id="402ae-177">**Comment**</span><span class="sxs-lookup"><span data-stu-id="402ae-177">**Comment**</span></span> |  <span data-ttu-id="402ae-178">Notez que AutomaticDownload est téléchargé et installé en mode silencieux si possible.</span><span class="sxs-lookup"><span data-stu-id="402ae-178">Note that AutomaticDownload will do a download and install silently if possible.</span></span> |


### <a name="change-whether-the-check-for-updates-button-is-enabled"></a><span data-ttu-id="402ae-179">Indique si le bouton « Vérifier les mises à jour » est activé.</span><span class="sxs-lookup"><span data-stu-id="402ae-179">Change whether the "Check for Updates" button is enabled</span></span>

<span data-ttu-id="402ae-180">Indiquez si les utilisateurs locaux pourront cliquer sur l’option « Vérifier les mises à jour » dans l’interface utilisateur Microsoft AutoUpdate.</span><span class="sxs-lookup"><span data-stu-id="402ae-180">Change whether local users will be able to click the "Check for Updates" option in the Microsoft AutoUpdate user interface.</span></span>

|<span data-ttu-id="402ae-181">Section</span><span class="sxs-lookup"><span data-stu-id="402ae-181">Section</span></span>|<span data-ttu-id="402ae-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="402ae-182">Value</span></span>|
|:--|:--|
| <span data-ttu-id="402ae-183">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="402ae-183">**Domain**</span></span> | <span data-ttu-id="402ae-184">com.microsoft.autoupdate2</span><span class="sxs-lookup"><span data-stu-id="402ae-184">com.microsoft.autoupdate2</span></span> |
| <span data-ttu-id="402ae-185">**Key**</span><span class="sxs-lookup"><span data-stu-id="402ae-185">**Key**</span></span> | <span data-ttu-id="402ae-186">EnableCheckForUpdatesButton</span><span class="sxs-lookup"><span data-stu-id="402ae-186">EnableCheckForUpdatesButton</span></span> |
| <span data-ttu-id="402ae-187">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="402ae-187">**Data type**</span></span> | <span data-ttu-id="402ae-188">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="402ae-188">Boolean</span></span> |
| <span data-ttu-id="402ae-189">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="402ae-189">**Possible values**</span></span> | <span data-ttu-id="402ae-190">True (par défaut)</span><span class="sxs-lookup"><span data-stu-id="402ae-190">True (default)</span></span> <br/> <span data-ttu-id="402ae-191">Faux</span><span class="sxs-lookup"><span data-stu-id="402ae-191">False</span></span> |


### <a name="disable-insider-checkbox"></a><span data-ttu-id="402ae-192">Désactiver la case à cocher Insider</span><span class="sxs-lookup"><span data-stu-id="402ae-192">Disable Insider checkbox</span></span>

<span data-ttu-id="402ae-193">Définissez la valeur sur True pour que le programme « Rejoignez le programme Office Insider... » case à cocher non disponible/grisée pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="402ae-193">Set to true to make the "Join the Office Insider Program..." checkbox unavailable / greyed out to users.</span></span>

|<span data-ttu-id="402ae-194">Section</span><span class="sxs-lookup"><span data-stu-id="402ae-194">Section</span></span>|<span data-ttu-id="402ae-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="402ae-195">Value</span></span>|
|:--|:--|
| <span data-ttu-id="402ae-196">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="402ae-196">**Domain**</span></span> | <span data-ttu-id="402ae-197">com.microsoft.autoupdate2</span><span class="sxs-lookup"><span data-stu-id="402ae-197">com.microsoft.autoupdate2</span></span> |
| <span data-ttu-id="402ae-198">**Key**</span><span class="sxs-lookup"><span data-stu-id="402ae-198">**Key**</span></span> | <span data-ttu-id="402ae-199">DisableInsiderCheckbox</span><span class="sxs-lookup"><span data-stu-id="402ae-199">DisableInsiderCheckbox</span></span> |
| <span data-ttu-id="402ae-200">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="402ae-200">**Data type**</span></span> | <span data-ttu-id="402ae-201">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="402ae-201">Boolean</span></span> |
| <span data-ttu-id="402ae-202">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="402ae-202">**Possible values**</span></span> | <span data-ttu-id="402ae-203">False (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="402ae-203">False (default)</span></span> <br/> <span data-ttu-id="402ae-204">Vrai</span><span class="sxs-lookup"><span data-stu-id="402ae-204">True</span></span> |


### <a name="limit-the-telemetry-that-is-sent-from-mau"></a><span data-ttu-id="402ae-205">Limiter la télémétrie envoyée à partir de MAU</span><span class="sxs-lookup"><span data-stu-id="402ae-205">Limit the telemetry that is sent from MAU</span></span>

<span data-ttu-id="402ae-206">Définissez ce dernier sur False pour envoyer un minimum de données de pulsation, aucune utilisation de l’application et aucun détail sur l’environnement.</span><span class="sxs-lookup"><span data-stu-id="402ae-206">Set to false to send minimal heartbeat data, no application usage, and no environment details.</span></span>

|<span data-ttu-id="402ae-207">Section</span><span class="sxs-lookup"><span data-stu-id="402ae-207">Section</span></span>|<span data-ttu-id="402ae-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="402ae-208">Value</span></span>|
|:--|:--|
| <span data-ttu-id="402ae-209">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="402ae-209">**Domain**</span></span> | <span data-ttu-id="402ae-210">com.microsoft.autoupdate2</span><span class="sxs-lookup"><span data-stu-id="402ae-210">com.microsoft.autoupdate2</span></span> |
| <span data-ttu-id="402ae-211">**Key**</span><span class="sxs-lookup"><span data-stu-id="402ae-211">**Key**</span></span> | <span data-ttu-id="402ae-212">SendAllTelemetryEnabled</span><span class="sxs-lookup"><span data-stu-id="402ae-212">SendAllTelemetryEnabled</span></span> |
| <span data-ttu-id="402ae-213">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="402ae-213">**Data type**</span></span> | <span data-ttu-id="402ae-214">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="402ae-214">Boolean</span></span> |
| <span data-ttu-id="402ae-215">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="402ae-215">**Possible values**</span></span> | <span data-ttu-id="402ae-216">True (par défaut)</span><span class="sxs-lookup"><span data-stu-id="402ae-216">True (default)</span></span> <br/> <span data-ttu-id="402ae-217">Faux</span><span class="sxs-lookup"><span data-stu-id="402ae-217">False</span></span> |


## <a name="example-configuration-profile"></a><span data-ttu-id="402ae-218">Exemple de profil de configuration</span><span class="sxs-lookup"><span data-stu-id="402ae-218">Example configuration profile</span></span>

<span data-ttu-id="402ae-219">Le profil de configuration suivant est utilisé pour :</span><span class="sxs-lookup"><span data-stu-id="402ae-219">The following configuration profile is used to:</span></span>
- <span data-ttu-id="402ae-220">Placer l'appareil dans le canal bêta</span><span class="sxs-lookup"><span data-stu-id="402ae-220">Place the device in the Beta channel</span></span>
- <span data-ttu-id="402ae-221">Télécharger et installer automatiquement les mises à jour</span><span class="sxs-lookup"><span data-stu-id="402ae-221">Automatically download and install updates</span></span>
- <span data-ttu-id="402ae-222">Activer le bouton « Vérifier les mises à jour » dans l'interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="402ae-222">Enable the "Check for updates" button in the user interface</span></span>
- <span data-ttu-id="402ae-223">Autoriser les utilisateurs de l'appareil à s'inscrire aux canaux Insider</span><span class="sxs-lookup"><span data-stu-id="402ae-223">Allow users on the device to enroll into the Insider channels</span></span>

### <a name="jamf"></a><span data-ttu-id="402ae-224">JAMF</span><span class="sxs-lookup"><span data-stu-id="402ae-224">JAMF</span></span>

```XML
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>ChannelName</key>
    <string>Beta</string>
    <key>HowToCheck</key>
    <string>AutomaticDownload</string>
    <key>EnableCheckForUpdatesButton</key>
    <true/>
    <key>DisableInsiderCheckbox</key>
    <false/>
    <key>SendAllTelemetryEnabled</key>
    <true/>
</dict>
</plist>
```

### <a name="intune"></a><span data-ttu-id="402ae-225">Intune</span><span class="sxs-lookup"><span data-stu-id="402ae-225">Intune</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1">
    <dict>
        <key>PayloadUUID</key>
        <string>B762FF60-6ACB-4A72-9E72-459D00C936F3</string>
        <key>PayloadType</key>
        <string>Configuration</string>
        <key>PayloadOrganization</key>
        <string>Microsoft</string>
        <key>PayloadIdentifier</key>
        <string>com.microsoft.autoupdate2</string>
        <key>PayloadDisplayName</key>
        <string>Microsoft AutoUpdate settings</string>
        <key>PayloadDescription</key>
        <string>Microsoft AutoUpdate configuration settings</string>
        <key>PayloadVersion</key>
        <integer>1</integer>
        <key>PayloadEnabled</key>
        <true/>
        <key>PayloadRemovalDisallowed</key>
        <true/>
        <key>PayloadScope</key>
        <string>System</string>
        <key>PayloadContent</key>
        <array>
            <dict>
            <key>PayloadUUID</key>
            <string>5A6F350A-CC2C-440B-A074-68E3F34EBAE9</string>
            <key>PayloadType</key>
            <string>com.microsoft.autoupdate2</string>
            <key>PayloadOrganization</key>
            <string>Microsoft</string>
            <key>PayloadIdentifier</key>
            <string>com.microsoft.autoupdate2</string>
            <key>PayloadDisplayName</key>
            <string>Microsoft AutoUpdate configuration settings</string>
            <key>PayloadDescription</key>
            <string/>
            <key>PayloadVersion</key>
            <integer>1</integer>
            <key>PayloadEnabled</key>
            <true/>
            <key>ChannelName</key>
            <string>Beta</string>
            <key>HowToCheck</key>
            <string>AutomaticDownload</string>
            <key>EnableCheckForUpdatesButton</key>
            <true/>
            <key>DisableInsiderCheckbox</key>
            <false/>
            <key>SendAllTelemetryEnabled</key>
            <true/>
            </dict>
        </array>
    </dict>
</plist>
```

<span data-ttu-id="402ae-226">Pour configurer MAU, vous pouvez déployer ce profil de configuration à partir de l'outil de gestion que votre entreprise utilise :</span><span class="sxs-lookup"><span data-stu-id="402ae-226">To configure MAU, you can deploy this configuration profile from the management tool that your enterprise is using:</span></span>
- <span data-ttu-id="402ae-227">À partir de JAMF, téléchargez ce profil de configuration et définissez le domaine de préférence sur *com.microsoft.autoupdate2*.</span><span class="sxs-lookup"><span data-stu-id="402ae-227">From JAMF, upload this configuration profile and set the Preference Domain to *com.microsoft.autoupdate2*.</span></span>
- <span data-ttu-id="402ae-228">À partir d'Intune, téléchargez ce profil de configuration et définissez le nom du profil de configuration personnalisé sur *com.microsoft.autoupdate2*.</span><span class="sxs-lookup"><span data-stu-id="402ae-228">From Intune, upload this configuration profile and set the custom configuration profile name to *com.microsoft.autoupdate2*.</span></span>

## <a name="resources"></a><span data-ttu-id="402ae-229">Ressources</span><span class="sxs-lookup"><span data-stu-id="402ae-229">Resources</span></span>

- [<span data-ttu-id="402ae-230">Référence msupdate</span><span class="sxs-lookup"><span data-stu-id="402ae-230">msupdate reference</span></span>](https://docs.microsoft.com/deployoffice/mac/update-office-for-mac-using-msupdate)
