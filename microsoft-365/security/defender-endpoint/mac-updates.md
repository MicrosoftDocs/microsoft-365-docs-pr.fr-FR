---
title: Déployer des mises à jour pour Microsoft Defender pour endpoint sur Mac
description: Contrôler les mises à jour de Microsoft Defender pour Endpoint sur Mac dans les environnements d’entreprise.
keywords: microsoft, defender, Microsoft Defender pour point de terminaison, mac, mises à jour, déployer
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
ms.openlocfilehash: e08781455888595d57bd8a9e6f792796ea1853cd
ms.sourcegitcommit: a6fb731fdf726d7d9fe4232cf69510013f2b54ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "52684206"
---
# <a name="deploy-updates-for-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="34766-104">Déployer les mises à jour de Microsoft Defender pour endpoint sur macOS</span><span class="sxs-lookup"><span data-stu-id="34766-104">Deploy updates for Microsoft Defender for Endpoint on macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="34766-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="34766-105">**Applies to:**</span></span>

- [<span data-ttu-id="34766-106">Microsoft Defender pour point de terminaison macOS</span><span class="sxs-lookup"><span data-stu-id="34766-106">Microsoft Defender for Endpoint on macOS</span></span>](microsoft-defender-endpoint-mac.md)
- [<span data-ttu-id="34766-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="34766-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="34766-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="34766-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="34766-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="34766-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="34766-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="34766-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="34766-111">Microsoft publie régulièrement des mises à jour logicielles pour améliorer les performances, la sécurité et fournir de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="34766-111">Microsoft regularly publishes software updates to improve performance, security, and to deliver new features.</span></span>

<span data-ttu-id="34766-112">Pour mettre à jour Microsoft Defender pour endpoint sur macOS, un programme nommé Microsoft AutoUpdate (MAU) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="34766-112">To update Microsoft Defender for Endpoint on macOS, a program named Microsoft AutoUpdate (MAU) is used.</span></span> <span data-ttu-id="34766-113">Par défaut, MAU recherche automatiquement les mises à jour quotidiennes, mais vous pouvez la modifier en une fois par semaine, par mois ou manuellement.</span><span class="sxs-lookup"><span data-stu-id="34766-113">By default, MAU automatically checks for updates daily, but you can change that to weekly, monthly, or manually.</span></span>

![Capture d’écran MAU](images/MDATP-34-MAU.png)

<span data-ttu-id="34766-115">Si vous décidez de déployer des mises à jour à l’aide de vos outils de distribution de logiciels, vous devez configurer MAU pour vérifier manuellement les mises à jour logicielles.</span><span class="sxs-lookup"><span data-stu-id="34766-115">If you decide to deploy updates by using your software distribution tools, you should configure MAU to manually check for software updates.</span></span> <span data-ttu-id="34766-116">Vous pouvez déployer des préférences pour configurer comment et quand MAU recherche les mises à jour pour les Mac dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="34766-116">You can deploy preferences to configure how and when MAU checks for updates for the Macs in your organization.</span></span>

## <a name="use-msupdate"></a><span data-ttu-id="34766-117">Utiliser msupdate</span><span class="sxs-lookup"><span data-stu-id="34766-117">Use msupdate</span></span>

<span data-ttu-id="34766-118">MAU inclut un outil en ligne de commande, appelé *msupdate,* conçu pour les administrateurs informatiques afin qu’ils contrôlent plus précisément le moment où les mises à jour sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="34766-118">MAU includes a command-line tool, called *msupdate*, that is designed for IT administrators so that they have more precise control over when updates are applied.</span></span> <span data-ttu-id="34766-119">Vous pouvez trouver des instructions sur l’utilisation de cet outil dans [Update Office pour Mac à l’aide de msupdate](https://docs.microsoft.com/deployoffice/mac/update-office-for-mac-using-msupdate).</span><span class="sxs-lookup"><span data-stu-id="34766-119">Instructions for how to use this tool can be found in [Update Office for Mac by using msupdate](https://docs.microsoft.com/deployoffice/mac/update-office-for-mac-using-msupdate).</span></span>

<span data-ttu-id="34766-120">Dans MAU, l’identificateur d’application pour Microsoft Defender pour le point de terminaison sur macOS est *WDAV00*.</span><span class="sxs-lookup"><span data-stu-id="34766-120">In MAU, the application identifier for Microsoft Defender for Endpoint on macOS is *WDAV00*.</span></span> <span data-ttu-id="34766-121">Pour télécharger et installer les dernières mises à jour de Microsoft Defender pour Endpoint sur macOS, exécutez la commande suivante à partir d’une fenêtre Terminal :</span><span class="sxs-lookup"><span data-stu-id="34766-121">To download and install the latest updates for Microsoft Defender for Endpoint on macOS, execute the following command from a Terminal window:</span></span>

```
./msupdate --install --apps wdav00
```

## <a name="set-preferences-for-microsoft-autoupdate"></a><span data-ttu-id="34766-122">Définir des préférences pour la mise à jour automatique Microsoft</span><span class="sxs-lookup"><span data-stu-id="34766-122">Set preferences for Microsoft AutoUpdate</span></span>

<span data-ttu-id="34766-123">Cette section décrit les préférences les plus courantes qui peuvent être utilisées pour configurer MAU.</span><span class="sxs-lookup"><span data-stu-id="34766-123">This section describes the most common preferences that can be used to configure MAU.</span></span> <span data-ttu-id="34766-124">Ces paramètres peuvent être déployés en tant que profil de configuration via la console de gestion que votre entreprise utilise.</span><span class="sxs-lookup"><span data-stu-id="34766-124">These settings can be deployed as a configuration profile through the management console that your enterprise is using.</span></span> <span data-ttu-id="34766-125">Un exemple de profil de configuration est illustré dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="34766-125">An example of a configuration profile is shown in the following sections.</span></span>

### <a name="set-the-channel-name"></a><span data-ttu-id="34766-126">Définir le nom du canal</span><span class="sxs-lookup"><span data-stu-id="34766-126">Set the channel name</span></span>

<span data-ttu-id="34766-127">Le canal détermine le type et la fréquence des mises à jour proposées via MAU.</span><span class="sxs-lookup"><span data-stu-id="34766-127">The channel determines the type and frequency of updates that are offered through MAU.</span></span> <span data-ttu-id="34766-128">Les appareils peuvent `Beta` tester de nouvelles fonctionnalités avant d’utiliser `Preview` et `Current` .</span><span class="sxs-lookup"><span data-stu-id="34766-128">Devices in `Beta` can try out new features before devices in `Preview` and `Current`.</span></span> 

<span data-ttu-id="34766-129">Le `Current` canal contient la version la plus stable du produit.</span><span class="sxs-lookup"><span data-stu-id="34766-129">The `Current` channel contains the most stable version of the product.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="34766-130">Avant la mise à jour automatique Microsoft version 4.29, les canaux avaient des noms différents :</span><span class="sxs-lookup"><span data-stu-id="34766-130">Prior to Microsoft AutoUpdate version 4.29, channels had different names:</span></span> 
> 
> - <span data-ttu-id="34766-131">`Beta` a été nommé `InsiderFast` (Insider Fast)</span><span class="sxs-lookup"><span data-stu-id="34766-131">`Beta` was named `InsiderFast` (Insider Fast)</span></span>
> - <span data-ttu-id="34766-132">`Preview` a été nommé `External` (Insider Slow)</span><span class="sxs-lookup"><span data-stu-id="34766-132">`Preview` was named `External` (Insider Slow)</span></span>
> - <span data-ttu-id="34766-133">`Current` a été nommé `Production`</span><span class="sxs-lookup"><span data-stu-id="34766-133">`Current` was named `Production`</span></span>

>[!TIP]
><span data-ttu-id="34766-134">Pour prévisualiser les nouvelles fonctionnalités et fournir des commentaires préliminaires, il est recommandé de configurer certains appareils dans votre entreprise sur `Beta` ou `Preview` .</span><span class="sxs-lookup"><span data-stu-id="34766-134">In order to preview new features and provide early feedback, it is recommended that you configure some devices in your enterprise to `Beta` or `Preview`.</span></span>

|<span data-ttu-id="34766-135">Section</span><span class="sxs-lookup"><span data-stu-id="34766-135">Section</span></span>|<span data-ttu-id="34766-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="34766-136">Value</span></span>|
|:--|:--|
| <span data-ttu-id="34766-137">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="34766-137">**Domain**</span></span> | `com.microsoft.autoupdate2` |
| <span data-ttu-id="34766-138">**Clé**</span><span class="sxs-lookup"><span data-stu-id="34766-138">**Key**</span></span> | <span data-ttu-id="34766-139">ChannelName</span><span class="sxs-lookup"><span data-stu-id="34766-139">ChannelName</span></span> |
| <span data-ttu-id="34766-140">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="34766-140">**Data type**</span></span> | <span data-ttu-id="34766-141">Chaîne</span><span class="sxs-lookup"><span data-stu-id="34766-141">String</span></span> |
| <span data-ttu-id="34766-142">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="34766-142">**Possible values**</span></span> | <span data-ttu-id="34766-143">Bêta</span><span class="sxs-lookup"><span data-stu-id="34766-143">Beta</span></span> <br/> <span data-ttu-id="34766-144">Aperçu</span><span class="sxs-lookup"><span data-stu-id="34766-144">Preview</span></span> <br/> <span data-ttu-id="34766-145">Current</span><span class="sxs-lookup"><span data-stu-id="34766-145">Current</span></span> |
|||

>[!WARNING]
><span data-ttu-id="34766-146">Ce paramètre modifie le canal pour toutes les applications qui sont mises à jour via la mise à jour automatique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="34766-146">This setting changes the channel for all applications that are updated through Microsoft AutoUpdate.</span></span> <span data-ttu-id="34766-147">Pour modifier le canal uniquement pour Microsoft Defender pour le point de terminaison sur macOS, exécutez la commande suivante après le remplacement par `[channel-name]` le canal souhaité :</span><span class="sxs-lookup"><span data-stu-id="34766-147">To change the channel only for Microsoft Defender for Endpoint on macOS, execute the following command after replacing `[channel-name]` with the desired channel:</span></span>
> ```bash
> defaults write com.microsoft.autoupdate2 Applications -dict-add "/Applications/Microsoft Defender ATP.app" " { 'Application ID' = 'WDAV00' ; 'App Domain' = 'com.microsoft.wdav' ; LCID = 1033 ; ChannelName = '[channel-name]' ; }"
> ```

### <a name="set-update-check-frequency"></a><span data-ttu-id="34766-148">Définir la fréquence de vérification des mises à jour</span><span class="sxs-lookup"><span data-stu-id="34766-148">Set update check frequency</span></span>

<span data-ttu-id="34766-149">Modifier la fréquence à la recherche de mises à jour par MAU.</span><span class="sxs-lookup"><span data-stu-id="34766-149">Change how often MAU searches for updates.</span></span>

|<span data-ttu-id="34766-150">Section</span><span class="sxs-lookup"><span data-stu-id="34766-150">Section</span></span>|<span data-ttu-id="34766-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="34766-151">Value</span></span>|
|:--|:--|
| <span data-ttu-id="34766-152">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="34766-152">**Domain**</span></span> | `com.microsoft.autoupdate2` |
| <span data-ttu-id="34766-153">**Clé**</span><span class="sxs-lookup"><span data-stu-id="34766-153">**Key**</span></span> | <span data-ttu-id="34766-154">UpdateCheckFrequency</span><span class="sxs-lookup"><span data-stu-id="34766-154">UpdateCheckFrequency</span></span> |
| <span data-ttu-id="34766-155">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="34766-155">**Data type**</span></span> | <span data-ttu-id="34766-156">Entier</span><span class="sxs-lookup"><span data-stu-id="34766-156">Integer</span></span> |
| <span data-ttu-id="34766-157">**Valeur par défaut**</span><span class="sxs-lookup"><span data-stu-id="34766-157">**Default value**</span></span> | <span data-ttu-id="34766-158">720 (minutes)</span><span class="sxs-lookup"><span data-stu-id="34766-158">720 (minutes)</span></span> |
| <span data-ttu-id="34766-159">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="34766-159">**Comment**</span></span> | <span data-ttu-id="34766-160">Cette valeur est définie en minutes.</span><span class="sxs-lookup"><span data-stu-id="34766-160">This value is set in minutes.</span></span> |


### <a name="change-how-mau-interacts-with-updates"></a><span data-ttu-id="34766-161">Modifier la façon dont MAU interagit avec les mises à jour</span><span class="sxs-lookup"><span data-stu-id="34766-161">Change how MAU interacts with updates</span></span>

<span data-ttu-id="34766-162">Modifier la façon dont MAU recherche les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="34766-162">Change how MAU searches for updates.</span></span>

|<span data-ttu-id="34766-163">Section</span><span class="sxs-lookup"><span data-stu-id="34766-163">Section</span></span>|<span data-ttu-id="34766-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="34766-164">Value</span></span>|
|:--|:--|
| <span data-ttu-id="34766-165">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="34766-165">**Domain**</span></span> | `com.microsoft.autoupdate2` |
| <span data-ttu-id="34766-166">**Clé**</span><span class="sxs-lookup"><span data-stu-id="34766-166">**Key**</span></span> | <span data-ttu-id="34766-167">HowToCheck</span><span class="sxs-lookup"><span data-stu-id="34766-167">HowToCheck</span></span> |
| <span data-ttu-id="34766-168">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="34766-168">**Data type**</span></span> | <span data-ttu-id="34766-169">Chaîne</span><span class="sxs-lookup"><span data-stu-id="34766-169">String</span></span> |
| <span data-ttu-id="34766-170">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="34766-170">**Possible values**</span></span> | <span data-ttu-id="34766-171">Manuel</span><span class="sxs-lookup"><span data-stu-id="34766-171">Manual</span></span> <br/> <span data-ttu-id="34766-172">AutomaticCheck</span><span class="sxs-lookup"><span data-stu-id="34766-172">AutomaticCheck</span></span> <br/> <span data-ttu-id="34766-173">AutomaticDownload</span><span class="sxs-lookup"><span data-stu-id="34766-173">AutomaticDownload</span></span> |
| <span data-ttu-id="34766-174">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="34766-174">**Comment**</span></span> |  <span data-ttu-id="34766-175">Notez que AutomaticDownload est téléchargé et installé en mode silencieux si possible.</span><span class="sxs-lookup"><span data-stu-id="34766-175">Note that AutomaticDownload will do a download and install silently if possible.</span></span> |


### <a name="change-whether-the-check-for-updates-button-is-enabled"></a><span data-ttu-id="34766-176">Indique si le bouton « Vérifier les mises à jour » est activé.</span><span class="sxs-lookup"><span data-stu-id="34766-176">Change whether the "Check for Updates" button is enabled</span></span>

<span data-ttu-id="34766-177">Indiquez si les utilisateurs locaux pourront cliquer sur l’option « Vérifier les mises à jour » dans l’interface utilisateur Microsoft AutoUpdate.</span><span class="sxs-lookup"><span data-stu-id="34766-177">Change whether local users will be able to click the "Check for Updates" option in the Microsoft AutoUpdate user interface.</span></span>

|<span data-ttu-id="34766-178">Section</span><span class="sxs-lookup"><span data-stu-id="34766-178">Section</span></span>|<span data-ttu-id="34766-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="34766-179">Value</span></span>|
|:--|:--|
| <span data-ttu-id="34766-180">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="34766-180">**Domain**</span></span> | `com.microsoft.autoupdate2` |
| <span data-ttu-id="34766-181">**Clé**</span><span class="sxs-lookup"><span data-stu-id="34766-181">**Key**</span></span> | <span data-ttu-id="34766-182">EnableCheckForUpdatesButton</span><span class="sxs-lookup"><span data-stu-id="34766-182">EnableCheckForUpdatesButton</span></span> |
| <span data-ttu-id="34766-183">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="34766-183">**Data type**</span></span> | <span data-ttu-id="34766-184">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="34766-184">Boolean</span></span> |
| <span data-ttu-id="34766-185">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="34766-185">**Possible values**</span></span> | <span data-ttu-id="34766-186">True (par défaut)</span><span class="sxs-lookup"><span data-stu-id="34766-186">True (default)</span></span> <br/> <span data-ttu-id="34766-187">False</span><span class="sxs-lookup"><span data-stu-id="34766-187">False</span></span> |


### <a name="disable-insider-checkbox"></a><span data-ttu-id="34766-188">Désactiver la case à cocher Insider</span><span class="sxs-lookup"><span data-stu-id="34766-188">Disable Insider checkbox</span></span>

<span data-ttu-id="34766-189">Définissez la valeur sur True pour que le programme « Rejoindre Office Programme Insider... » case à cocher non disponible/grisée pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="34766-189">Set to true to make the "Join the Office Insider Program..." checkbox unavailable / greyed out to users.</span></span>

|<span data-ttu-id="34766-190">Section</span><span class="sxs-lookup"><span data-stu-id="34766-190">Section</span></span>|<span data-ttu-id="34766-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="34766-191">Value</span></span>|
|:--|:--|
| <span data-ttu-id="34766-192">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="34766-192">**Domain**</span></span> | `com.microsoft.autoupdate2` |
| <span data-ttu-id="34766-193">**Clé**</span><span class="sxs-lookup"><span data-stu-id="34766-193">**Key**</span></span> | <span data-ttu-id="34766-194">DisableInsiderCheckbox</span><span class="sxs-lookup"><span data-stu-id="34766-194">DisableInsiderCheckbox</span></span> |
| <span data-ttu-id="34766-195">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="34766-195">**Data type**</span></span> | <span data-ttu-id="34766-196">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="34766-196">Boolean</span></span> |
| <span data-ttu-id="34766-197">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="34766-197">**Possible values**</span></span> | <span data-ttu-id="34766-198">False (par défaut)</span><span class="sxs-lookup"><span data-stu-id="34766-198">False (default)</span></span> <br/> <span data-ttu-id="34766-199">Vrai</span><span class="sxs-lookup"><span data-stu-id="34766-199">True</span></span> |


### <a name="limit-the-telemetry-that-is-sent-from-mau"></a><span data-ttu-id="34766-200">Limiter la télémétrie envoyée à partir de MAU</span><span class="sxs-lookup"><span data-stu-id="34766-200">Limit the telemetry that is sent from MAU</span></span>

<span data-ttu-id="34766-201">Définissez ce dernier sur False pour envoyer des données d’pulsation minimales, aucune utilisation de l’application et aucun détail sur l’environnement.</span><span class="sxs-lookup"><span data-stu-id="34766-201">Set to false to send minimal heartbeat data, no application usage, and no environment details.</span></span>

|<span data-ttu-id="34766-202">Section</span><span class="sxs-lookup"><span data-stu-id="34766-202">Section</span></span>|<span data-ttu-id="34766-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="34766-203">Value</span></span>|
|:--|:--|
| <span data-ttu-id="34766-204">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="34766-204">**Domain**</span></span> | `com.microsoft.autoupdate2` |
| <span data-ttu-id="34766-205">**Clé**</span><span class="sxs-lookup"><span data-stu-id="34766-205">**Key**</span></span> | <span data-ttu-id="34766-206">SendAllTelemetryEnabled</span><span class="sxs-lookup"><span data-stu-id="34766-206">SendAllTelemetryEnabled</span></span> |
| <span data-ttu-id="34766-207">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="34766-207">**Data type**</span></span> | <span data-ttu-id="34766-208">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="34766-208">Boolean</span></span> |
| <span data-ttu-id="34766-209">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="34766-209">**Possible values**</span></span> | <span data-ttu-id="34766-210">True (par défaut)</span><span class="sxs-lookup"><span data-stu-id="34766-210">True (default)</span></span> <br/> <span data-ttu-id="34766-211">False</span><span class="sxs-lookup"><span data-stu-id="34766-211">False</span></span> |


## <a name="example-configuration-profile"></a><span data-ttu-id="34766-212">Exemple de profil de configuration</span><span class="sxs-lookup"><span data-stu-id="34766-212">Example configuration profile</span></span>

<span data-ttu-id="34766-213">Le profil de configuration suivant est utilisé pour :</span><span class="sxs-lookup"><span data-stu-id="34766-213">The following configuration profile is used to:</span></span>
- <span data-ttu-id="34766-214">Placer l’appareil dans le canal de production</span><span class="sxs-lookup"><span data-stu-id="34766-214">Place the device in the Production channel</span></span>
- <span data-ttu-id="34766-215">Télécharger et installer automatiquement les mises à jour</span><span class="sxs-lookup"><span data-stu-id="34766-215">Automatically download and install updates</span></span>
- <span data-ttu-id="34766-216">Activer le bouton « Vérifier les mises à jour » dans l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="34766-216">Enable the "Check for updates" button in the user interface</span></span>
- <span data-ttu-id="34766-217">Autoriser les utilisateurs de l’appareil à s’inscrire aux canaux Insider</span><span class="sxs-lookup"><span data-stu-id="34766-217">Allow users on the device to enroll into the Insider channels</span></span>


>[!WARNING]
><span data-ttu-id="34766-218">La configuration ci-dessous est un exemple de configuration et ne doit pas être utilisée en production sans une révision appropriée des paramètres et une adaptation des configurations.</span><span class="sxs-lookup"><span data-stu-id="34766-218">The below configuration is an example configuration and should not be used in production without proper review of settings and tailor of configurations.</span></span>

>[!TIP]
><span data-ttu-id="34766-219">Pour afficher un aperçu des nouvelles fonctionnalités et fournir des commentaires préliminaires, il est recommandé de configurer certains appareils dans votre entreprise sur `Beta` ou `Preview` .</span><span class="sxs-lookup"><span data-stu-id="34766-219">In order to preview new features and provide early feedback, it is recommended that you configure some devices in your enterprise to `Beta` or `Preview`.</span></span>

### <a name="jamf"></a><span data-ttu-id="34766-220">JAMF</span><span class="sxs-lookup"><span data-stu-id="34766-220">JAMF</span></span>

```XML
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>ChannelName</key>
    <string>Production</string>
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

### <a name="intune"></a><span data-ttu-id="34766-221">Intune</span><span class="sxs-lookup"><span data-stu-id="34766-221">Intune</span></span>

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
            <string>Production</string>
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

<span data-ttu-id="34766-222">Pour configurer MAU, vous pouvez déployer ce profil de configuration à partir de l’outil de gestion que votre entreprise utilise :</span><span class="sxs-lookup"><span data-stu-id="34766-222">To configure MAU, you can deploy this configuration profile from the management tool that your enterprise is using:</span></span>
- <span data-ttu-id="34766-223">À partir de JAMF, téléchargez ce profil de configuration et définissez le domaine de préférence sur *com.microsoft.autoupdate2*.</span><span class="sxs-lookup"><span data-stu-id="34766-223">From JAMF, upload this configuration profile and set the Preference Domain to *com.microsoft.autoupdate2*.</span></span>
- <span data-ttu-id="34766-224">À partir d’Intune, téléchargez ce profil de configuration et définissez le nom du profil de configuration personnalisé sur *com.microsoft.autoupdate2*.</span><span class="sxs-lookup"><span data-stu-id="34766-224">From Intune, upload this configuration profile and set the custom configuration profile name to *com.microsoft.autoupdate2*.</span></span>

## <a name="resources"></a><span data-ttu-id="34766-225">Ressources</span><span class="sxs-lookup"><span data-stu-id="34766-225">Resources</span></span>

- [<span data-ttu-id="34766-226">Référence msupdate</span><span class="sxs-lookup"><span data-stu-id="34766-226">msupdate reference</span></span>](https://docs.microsoft.com/deployoffice/mac/update-office-for-mac-using-msupdate)
