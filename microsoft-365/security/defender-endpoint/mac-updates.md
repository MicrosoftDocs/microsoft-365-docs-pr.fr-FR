---
title: Déployer les mises à jour de Microsoft Defender ATP pour Mac
description: Contrôler les mises à jour de Microsoft Defender ATP pour Mac dans les environnements d’entreprise.
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
ms.openlocfilehash: 99f507ad381ee21ba91753716439180fafe37c24
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51066305"
---
# <a name="deploy-updates-for-microsoft-defender-for-endpoint-for-mac"></a><span data-ttu-id="bb556-104">Déployer les mises à jour de Microsoft Defender pour Endpoint pour Mac</span><span class="sxs-lookup"><span data-stu-id="bb556-104">Deploy updates for Microsoft Defender for Endpoint for Mac</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="bb556-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="bb556-105">**Applies to:**</span></span>

- [<span data-ttu-id="bb556-106">Microsoft Defender pour point de terminaison pour Mac</span><span class="sxs-lookup"><span data-stu-id="bb556-106">Microsoft Defender for Endpoint for Mac</span></span>](microsoft-defender-endpoint-mac.md)
- [<span data-ttu-id="bb556-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="bb556-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="bb556-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bb556-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="bb556-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="bb556-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="bb556-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="bb556-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="bb556-111">Microsoft publie régulièrement des mises à jour logicielles pour améliorer les performances, la sécurité et fournir de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="bb556-111">Microsoft regularly publishes software updates to improve performance, security, and to deliver new features.</span></span>

<span data-ttu-id="bb556-112">Pour mettre à jour Microsoft Defender pour endpoint pour Mac, un programme nommé Microsoft AutoUpdate (MAU) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="bb556-112">To update Microsoft Defender for Endpoint for Mac, a program named Microsoft AutoUpdate (MAU) is used.</span></span> <span data-ttu-id="bb556-113">Par défaut, MAU recherche automatiquement les mises à jour quotidiennes, mais vous pouvez la modifier de manière hebdomadaire, mensuelle ou manuelle.</span><span class="sxs-lookup"><span data-stu-id="bb556-113">By default, MAU automatically checks for updates daily, but you can change that to weekly, monthly, or manually.</span></span>

![Capture d’écran MAU](images/MDATP-34-MAU.png)

<span data-ttu-id="bb556-115">Si vous décidez de déployer des mises à jour à l’aide de vos outils de distribution de logiciels, vous devez configurer MAU pour vérifier manuellement les mises à jour logicielles.</span><span class="sxs-lookup"><span data-stu-id="bb556-115">If you decide to deploy updates by using your software distribution tools, you should configure MAU to manually check for software updates.</span></span> <span data-ttu-id="bb556-116">Vous pouvez déployer des préférences pour configurer comment et quand MAU recherche les mises à jour pour les Mac dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bb556-116">You can deploy preferences to configure how and when MAU checks for updates for the Macs in your organization.</span></span>

## <a name="use-msupdate"></a><span data-ttu-id="bb556-117">Utiliser msupdate</span><span class="sxs-lookup"><span data-stu-id="bb556-117">Use msupdate</span></span>

<span data-ttu-id="bb556-118">MAU inclut un outil en ligne de commande, appelé *msupdate,* conçu pour les administrateurs informatiques afin qu’ils contrôlent plus précisément le moment où les mises à jour sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="bb556-118">MAU includes a command-line tool, called *msupdate*, that is designed for IT administrators so that they have more precise control over when updates are applied.</span></span> <span data-ttu-id="bb556-119">Vous pouvez trouver des instructions sur l’utilisation de cet outil dans La mise à [jour d’Office pour Mac à l’aide de msupdate](https://docs.microsoft.com/deployoffice/mac/update-office-for-mac-using-msupdate).</span><span class="sxs-lookup"><span data-stu-id="bb556-119">Instructions for how to use this tool can be found in [Update Office for Mac by using msupdate](https://docs.microsoft.com/deployoffice/mac/update-office-for-mac-using-msupdate).</span></span>

<span data-ttu-id="bb556-120">Dans MAU, l’identificateur d’application de Microsoft Defender pour Endpoint pour Mac *est WDAV00*.</span><span class="sxs-lookup"><span data-stu-id="bb556-120">In MAU, the application identifier for Microsoft Defender for Endpoint for Mac is *WDAV00*.</span></span> <span data-ttu-id="bb556-121">Pour télécharger et installer les dernières mises à jour de Microsoft Defender pour Endpoint pour Mac, exécutez la commande suivante à partir d’une fenêtre Terminal :</span><span class="sxs-lookup"><span data-stu-id="bb556-121">To download and install the latest updates for Microsoft Defender for Endpoint for Mac, execute the following command from a Terminal window:</span></span>

```
./msupdate --install --apps wdav00
```

## <a name="set-preferences-for-microsoft-autoupdate"></a><span data-ttu-id="bb556-122">Définir des préférences pour la mise à jour automatique Microsoft</span><span class="sxs-lookup"><span data-stu-id="bb556-122">Set preferences for Microsoft AutoUpdate</span></span>

<span data-ttu-id="bb556-123">Cette section décrit les préférences les plus courantes qui peuvent être utilisées pour configurer MAU.</span><span class="sxs-lookup"><span data-stu-id="bb556-123">This section describes the most common preferences that can be used to configure MAU.</span></span> <span data-ttu-id="bb556-124">Ces paramètres peuvent être déployés en tant que profil de configuration via la console de gestion que votre entreprise utilise.</span><span class="sxs-lookup"><span data-stu-id="bb556-124">These settings can be deployed as a configuration profile through the management console that your enterprise is using.</span></span> <span data-ttu-id="bb556-125">Un exemple de profil de configuration est illustré dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="bb556-125">An example of a configuration profile is shown in the following sections.</span></span>

### <a name="set-the-channel-name"></a><span data-ttu-id="bb556-126">Définir le nom du canal</span><span class="sxs-lookup"><span data-stu-id="bb556-126">Set the channel name</span></span>

<span data-ttu-id="bb556-127">Le canal détermine le type et la fréquence des mises à jour proposées via MAU.</span><span class="sxs-lookup"><span data-stu-id="bb556-127">The channel determines the type and frequency of updates that are offered through MAU.</span></span> <span data-ttu-id="bb556-128">Les appareils peuvent `Beta` tester de nouvelles fonctionnalités avant d’utiliser `Preview` et `Current` .</span><span class="sxs-lookup"><span data-stu-id="bb556-128">Devices in `Beta` can try out new features before devices in `Preview` and `Current`.</span></span> 

<span data-ttu-id="bb556-129">Le `Current` canal contient la version la plus stable du produit.</span><span class="sxs-lookup"><span data-stu-id="bb556-129">The `Current` channel contains the most stable version of the product.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="bb556-130">Avant la mise à jour automatique Microsoft version 4.29, les canaux avaient des noms différents :</span><span class="sxs-lookup"><span data-stu-id="bb556-130">Prior to Microsoft AutoUpdate version 4.29, channels had different names:</span></span> 
> 
> - <span data-ttu-id="bb556-131">`Beta` a été nommé `InsiderFast` (Insider Fast)</span><span class="sxs-lookup"><span data-stu-id="bb556-131">`Beta` was named `InsiderFast` (Insider Fast)</span></span>
> - <span data-ttu-id="bb556-132">`Preview` a été nommé `External` (Insider Slow)</span><span class="sxs-lookup"><span data-stu-id="bb556-132">`Preview` was named `External` (Insider Slow)</span></span>
> - <span data-ttu-id="bb556-133">`Current` a été nommé `Production`</span><span class="sxs-lookup"><span data-stu-id="bb556-133">`Current` was named `Production`</span></span>

>[!TIP]
><span data-ttu-id="bb556-134">Pour afficher un aperçu des nouvelles fonctionnalités et fournir des commentaires préliminaires, il est recommandé de configurer certains appareils dans votre entreprise sur `Beta` ou `Preview` .</span><span class="sxs-lookup"><span data-stu-id="bb556-134">In order to preview new features and provide early feedback, it is recommended that you configure some devices in your enterprise to `Beta` or `Preview`.</span></span>

|||
|:--|:--|
| <span data-ttu-id="bb556-135">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="bb556-135">**Domain**</span></span> | <span data-ttu-id="bb556-136">com.microsoft.autoupdate2</span><span class="sxs-lookup"><span data-stu-id="bb556-136">com.microsoft.autoupdate2</span></span> |
| <span data-ttu-id="bb556-137">**Clé**</span><span class="sxs-lookup"><span data-stu-id="bb556-137">**Key**</span></span> | <span data-ttu-id="bb556-138">ChannelName</span><span class="sxs-lookup"><span data-stu-id="bb556-138">ChannelName</span></span> |
| <span data-ttu-id="bb556-139">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="bb556-139">**Data type**</span></span> | <span data-ttu-id="bb556-140">Chaîne</span><span class="sxs-lookup"><span data-stu-id="bb556-140">String</span></span> |
| <span data-ttu-id="bb556-141">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="bb556-141">**Possible values**</span></span> | <span data-ttu-id="bb556-142">Bêta</span><span class="sxs-lookup"><span data-stu-id="bb556-142">Beta</span></span> <br/> <span data-ttu-id="bb556-143">Aperçu</span><span class="sxs-lookup"><span data-stu-id="bb556-143">Preview</span></span> <br/> <span data-ttu-id="bb556-144">Current</span><span class="sxs-lookup"><span data-stu-id="bb556-144">Current</span></span> |
|||

>[!WARNING]
><span data-ttu-id="bb556-145">Ce paramètre modifie le canal pour toutes les applications qui sont mises à jour via La mise à jour automatique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bb556-145">This setting changes the channel for all applications that are updated through Microsoft AutoUpdate.</span></span> <span data-ttu-id="bb556-146">Pour modifier le canal uniquement pour Microsoft Defender pour point de terminaison pour Mac, exécutez la commande suivante après le remplacement par `[channel-name]` le canal souhaité :</span><span class="sxs-lookup"><span data-stu-id="bb556-146">To change the channel only for Microsoft Defender for Endpoint for Mac, execute the following command after replacing `[channel-name]` with the desired channel:</span></span>
> ```bash
> defaults write com.microsoft.autoupdate2 Applications -dict-add "/Applications/Microsoft Defender ATP.app" " { 'Application ID' = 'WDAV00' ; 'App Domain' = 'com.microsoft.wdav' ; LCID = 1033 ; ChannelName = '[channel-name]' ; }"
> ```

### <a name="set-update-check-frequency"></a><span data-ttu-id="bb556-147">Définir la fréquence de vérification des mises à jour</span><span class="sxs-lookup"><span data-stu-id="bb556-147">Set update check frequency</span></span>

<span data-ttu-id="bb556-148">Modifier la fréquence à la recherche de mises à jour par MAU.</span><span class="sxs-lookup"><span data-stu-id="bb556-148">Change how often MAU searches for updates.</span></span>

|||
|:--|:--|
| <span data-ttu-id="bb556-149">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="bb556-149">**Domain**</span></span> | <span data-ttu-id="bb556-150">com.microsoft.autoupdate2</span><span class="sxs-lookup"><span data-stu-id="bb556-150">com.microsoft.autoupdate2</span></span> |
| <span data-ttu-id="bb556-151">**Clé**</span><span class="sxs-lookup"><span data-stu-id="bb556-151">**Key**</span></span> | <span data-ttu-id="bb556-152">UpdateCheckFrequency</span><span class="sxs-lookup"><span data-stu-id="bb556-152">UpdateCheckFrequency</span></span> |
| <span data-ttu-id="bb556-153">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="bb556-153">**Data type**</span></span> | <span data-ttu-id="bb556-154">Entier</span><span class="sxs-lookup"><span data-stu-id="bb556-154">Integer</span></span> |
| <span data-ttu-id="bb556-155">**Valeur par défaut**</span><span class="sxs-lookup"><span data-stu-id="bb556-155">**Default value**</span></span> | <span data-ttu-id="bb556-156">720 (minutes)</span><span class="sxs-lookup"><span data-stu-id="bb556-156">720 (minutes)</span></span> |
| <span data-ttu-id="bb556-157">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="bb556-157">**Comment**</span></span> | <span data-ttu-id="bb556-158">Cette valeur est définie en minutes.</span><span class="sxs-lookup"><span data-stu-id="bb556-158">This value is set in minutes.</span></span> |
|||

### <a name="change-how-mau-interacts-with-updates"></a><span data-ttu-id="bb556-159">Modifier la façon dont MAU interagit avec les mises à jour</span><span class="sxs-lookup"><span data-stu-id="bb556-159">Change how MAU interacts with updates</span></span>

<span data-ttu-id="bb556-160">Modifier la façon dont MAU recherche les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="bb556-160">Change how MAU searches for updates.</span></span>

|||
|:--|:--|
| <span data-ttu-id="bb556-161">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="bb556-161">**Domain**</span></span> | <span data-ttu-id="bb556-162">com.microsoft.autoupdate2</span><span class="sxs-lookup"><span data-stu-id="bb556-162">com.microsoft.autoupdate2</span></span> |
| <span data-ttu-id="bb556-163">**Clé**</span><span class="sxs-lookup"><span data-stu-id="bb556-163">**Key**</span></span> | <span data-ttu-id="bb556-164">HowToCheck</span><span class="sxs-lookup"><span data-stu-id="bb556-164">HowToCheck</span></span> |
| <span data-ttu-id="bb556-165">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="bb556-165">**Data type**</span></span> | <span data-ttu-id="bb556-166">Chaîne</span><span class="sxs-lookup"><span data-stu-id="bb556-166">String</span></span> |
| <span data-ttu-id="bb556-167">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="bb556-167">**Possible values**</span></span> | <span data-ttu-id="bb556-168">Manuel</span><span class="sxs-lookup"><span data-stu-id="bb556-168">Manual</span></span> <br/> <span data-ttu-id="bb556-169">AutomaticCheck</span><span class="sxs-lookup"><span data-stu-id="bb556-169">AutomaticCheck</span></span> <br/> <span data-ttu-id="bb556-170">AutomaticDownload</span><span class="sxs-lookup"><span data-stu-id="bb556-170">AutomaticDownload</span></span> |
| <span data-ttu-id="bb556-171">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="bb556-171">**Comment**</span></span> |  <span data-ttu-id="bb556-172">Notez que AutomaticDownload est téléchargé et installé en mode silencieux si possible.</span><span class="sxs-lookup"><span data-stu-id="bb556-172">Note that AutomaticDownload will do a download and install silently if possible.</span></span> |
|||

### <a name="change-whether-the-check-for-updates-button-is-enabled"></a><span data-ttu-id="bb556-173">Indique si le bouton « Vérifier les mises à jour » est activé.</span><span class="sxs-lookup"><span data-stu-id="bb556-173">Change whether the "Check for Updates" button is enabled</span></span>

<span data-ttu-id="bb556-174">Indiquez si les utilisateurs locaux pourront cliquer sur l’option « Vérifier les mises à jour » dans l’interface utilisateur Microsoft AutoUpdate.</span><span class="sxs-lookup"><span data-stu-id="bb556-174">Change whether local users will be able to click the "Check for Updates" option in the Microsoft AutoUpdate user interface.</span></span>

|||
|:--|:--|
| <span data-ttu-id="bb556-175">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="bb556-175">**Domain**</span></span> | <span data-ttu-id="bb556-176">com.microsoft.autoupdate2</span><span class="sxs-lookup"><span data-stu-id="bb556-176">com.microsoft.autoupdate2</span></span> |
| <span data-ttu-id="bb556-177">**Clé**</span><span class="sxs-lookup"><span data-stu-id="bb556-177">**Key**</span></span> | <span data-ttu-id="bb556-178">EnableCheckForUpdatesButton</span><span class="sxs-lookup"><span data-stu-id="bb556-178">EnableCheckForUpdatesButton</span></span> |
| <span data-ttu-id="bb556-179">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="bb556-179">**Data type**</span></span> | <span data-ttu-id="bb556-180">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="bb556-180">Boolean</span></span> |
| <span data-ttu-id="bb556-181">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="bb556-181">**Possible values**</span></span> | <span data-ttu-id="bb556-182">True (par défaut)</span><span class="sxs-lookup"><span data-stu-id="bb556-182">True (default)</span></span> <br/> <span data-ttu-id="bb556-183">False</span><span class="sxs-lookup"><span data-stu-id="bb556-183">False</span></span> |
|||

### <a name="disable-insider-checkbox"></a><span data-ttu-id="bb556-184">Désactiver la case à cocher Insider</span><span class="sxs-lookup"><span data-stu-id="bb556-184">Disable Insider checkbox</span></span>

<span data-ttu-id="bb556-185">Définissez la valeur sur true pour que le programme « Rejoignez le programme Office Insider... » case à cocher non disponible/grisée pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bb556-185">Set to true to make the "Join the Office Insider Program..." checkbox unavailable / greyed out to users.</span></span>

|||
|:--|:--|
| <span data-ttu-id="bb556-186">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="bb556-186">**Domain**</span></span> | <span data-ttu-id="bb556-187">com.microsoft.autoupdate2</span><span class="sxs-lookup"><span data-stu-id="bb556-187">com.microsoft.autoupdate2</span></span> |
| <span data-ttu-id="bb556-188">**Clé**</span><span class="sxs-lookup"><span data-stu-id="bb556-188">**Key**</span></span> | <span data-ttu-id="bb556-189">DisableInsiderCheckbox</span><span class="sxs-lookup"><span data-stu-id="bb556-189">DisableInsiderCheckbox</span></span> |
| <span data-ttu-id="bb556-190">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="bb556-190">**Data type**</span></span> | <span data-ttu-id="bb556-191">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="bb556-191">Boolean</span></span> |
| <span data-ttu-id="bb556-192">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="bb556-192">**Possible values**</span></span> | <span data-ttu-id="bb556-193">False (par défaut)</span><span class="sxs-lookup"><span data-stu-id="bb556-193">False (default)</span></span> <br/> <span data-ttu-id="bb556-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="bb556-194">True</span></span> |
|||

### <a name="limit-the-telemetry-that-is-sent-from-mau"></a><span data-ttu-id="bb556-195">Limiter la télémétrie envoyée à partir de MAU</span><span class="sxs-lookup"><span data-stu-id="bb556-195">Limit the telemetry that is sent from MAU</span></span>

<span data-ttu-id="bb556-196">Définissez ce dernier sur False pour envoyer un minimum de données de pulsation, aucune utilisation de l’application et aucun détail sur l’environnement.</span><span class="sxs-lookup"><span data-stu-id="bb556-196">Set to false to send minimal heartbeat data, no application usage, and no environment details.</span></span>

|||
|:--|:--|
| <span data-ttu-id="bb556-197">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="bb556-197">**Domain**</span></span> | <span data-ttu-id="bb556-198">com.microsoft.autoupdate2</span><span class="sxs-lookup"><span data-stu-id="bb556-198">com.microsoft.autoupdate2</span></span> |
| <span data-ttu-id="bb556-199">**Clé**</span><span class="sxs-lookup"><span data-stu-id="bb556-199">**Key**</span></span> | <span data-ttu-id="bb556-200">SendAllTelemetryEnabled</span><span class="sxs-lookup"><span data-stu-id="bb556-200">SendAllTelemetryEnabled</span></span> |
| <span data-ttu-id="bb556-201">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="bb556-201">**Data type**</span></span> | <span data-ttu-id="bb556-202">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="bb556-202">Boolean</span></span> |
| <span data-ttu-id="bb556-203">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="bb556-203">**Possible values**</span></span> | <span data-ttu-id="bb556-204">True (par défaut)</span><span class="sxs-lookup"><span data-stu-id="bb556-204">True (default)</span></span> <br/> <span data-ttu-id="bb556-205">False</span><span class="sxs-lookup"><span data-stu-id="bb556-205">False</span></span> |
|||

## <a name="example-configuration-profile"></a><span data-ttu-id="bb556-206">Exemple de profil de configuration</span><span class="sxs-lookup"><span data-stu-id="bb556-206">Example configuration profile</span></span>

<span data-ttu-id="bb556-207">Le profil de configuration suivant est utilisé pour :</span><span class="sxs-lookup"><span data-stu-id="bb556-207">The following configuration profile is used to:</span></span>
- <span data-ttu-id="bb556-208">Placer l’appareil dans le canal bêta</span><span class="sxs-lookup"><span data-stu-id="bb556-208">Place the device in the Beta channel</span></span>
- <span data-ttu-id="bb556-209">Télécharger et installer automatiquement les mises à jour</span><span class="sxs-lookup"><span data-stu-id="bb556-209">Automatically download and install updates</span></span>
- <span data-ttu-id="bb556-210">Activer le bouton « Vérifier les mises à jour » dans l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="bb556-210">Enable the "Check for updates" button in the user interface</span></span>
- <span data-ttu-id="bb556-211">Autoriser les utilisateurs de l’appareil à s’inscrire aux canaux Insider</span><span class="sxs-lookup"><span data-stu-id="bb556-211">Allow users on the device to enroll into the Insider channels</span></span>

### <a name="jamf"></a><span data-ttu-id="bb556-212">JAMF</span><span class="sxs-lookup"><span data-stu-id="bb556-212">JAMF</span></span>

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

### <a name="intune"></a><span data-ttu-id="bb556-213">Intune</span><span class="sxs-lookup"><span data-stu-id="bb556-213">Intune</span></span>

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

<span data-ttu-id="bb556-214">Pour configurer MAU, vous pouvez déployer ce profil de configuration à partir de l’outil de gestion que votre entreprise utilise :</span><span class="sxs-lookup"><span data-stu-id="bb556-214">To configure MAU, you can deploy this configuration profile from the management tool that your enterprise is using:</span></span>
- <span data-ttu-id="bb556-215">À partir de JAMF, téléchargez ce profil de configuration et définissez le domaine de préférence sur *com.microsoft.autoupdate2*.</span><span class="sxs-lookup"><span data-stu-id="bb556-215">From JAMF, upload this configuration profile and set the Preference Domain to *com.microsoft.autoupdate2*.</span></span>
- <span data-ttu-id="bb556-216">À partir d’Intune, téléchargez ce profil de configuration et définissez le nom du profil de configuration personnalisé sur *com.microsoft.autoupdate2*.</span><span class="sxs-lookup"><span data-stu-id="bb556-216">From Intune, upload this configuration profile and set the custom configuration profile name to *com.microsoft.autoupdate2*.</span></span>

## <a name="resources"></a><span data-ttu-id="bb556-217">Ressources</span><span class="sxs-lookup"><span data-stu-id="bb556-217">Resources</span></span>

- [<span data-ttu-id="bb556-218">Référence msupdate</span><span class="sxs-lookup"><span data-stu-id="bb556-218">msupdate reference</span></span>](https://docs.microsoft.com/deployoffice/mac/update-office-for-mac-using-msupdate)
