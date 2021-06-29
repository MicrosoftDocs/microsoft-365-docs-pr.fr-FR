---
title: Déploiement basé sur Intune pour Microsoft Defender pour Endpoint sur Mac
description: Installez Microsoft Defender pour point de terminaison sur Mac, à l’aide Microsoft Intune.
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
ms.openlocfilehash: 7243e8f6fad225e6c4570184736e8d6588466d0a
ms.sourcegitcommit: 6749455c52b0f98a92f6fffbc2bb86caf3538bd8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2021
ms.locfileid: "53194960"
---
# <a name="intune-based-deployment-for-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="f7961-104">Déploiement basé sur Intune pour Microsoft Defender pour Endpoint sur macOS</span><span class="sxs-lookup"><span data-stu-id="f7961-104">Intune-based deployment for Microsoft Defender for Endpoint on macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f7961-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f7961-105">**Applies to:**</span></span>

- [<span data-ttu-id="f7961-106">Microsoft Defender pour point de terminaison macOS</span><span class="sxs-lookup"><span data-stu-id="f7961-106">Microsoft Defender for Endpoint on macOS</span></span>](microsoft-defender-endpoint-mac.md)

<span data-ttu-id="f7961-107">Cette rubrique décrit comment déployer Microsoft Defender pour endpoint sur macOS via Intune.</span><span class="sxs-lookup"><span data-stu-id="f7961-107">This topic describes how to deploy Microsoft Defender for Endpoint on macOS through Intune.</span></span> <span data-ttu-id="f7961-108">Un déploiement réussi nécessite la réalisation de toutes les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f7961-108">A successful deployment requires the completion of all of the following steps:</span></span>

1. [<span data-ttu-id="f7961-109">Télécharger le package d’intégration</span><span class="sxs-lookup"><span data-stu-id="f7961-109">Download the onboarding package</span></span>](#download-the-onboarding-package)
1. [<span data-ttu-id="f7961-110">Configuration de l’appareil client</span><span class="sxs-lookup"><span data-stu-id="f7961-110">Client device setup</span></span>](#client-device-setup)
1. [<span data-ttu-id="f7961-111">Approuver les extensions système</span><span class="sxs-lookup"><span data-stu-id="f7961-111">Approve system extensions</span></span>](#approve-system-extensions)
1. [<span data-ttu-id="f7961-112">Créer des profils de configuration système</span><span class="sxs-lookup"><span data-stu-id="f7961-112">Create System Configuration profiles</span></span>](#create-system-configuration-profiles)
1. [<span data-ttu-id="f7961-113">Publier l'application</span><span class="sxs-lookup"><span data-stu-id="f7961-113">Publish application</span></span>](#publish-application)

## <a name="prerequisites-and-system-requirements"></a><span data-ttu-id="f7961-114">Conditions préalables et système requis</span><span class="sxs-lookup"><span data-stu-id="f7961-114">Prerequisites and system requirements</span></span>

<span data-ttu-id="f7961-115">Avant de commencer, consultez la page principale de Microsoft Defender pour point de terminaison sur [macOS](microsoft-defender-endpoint-mac.md) pour obtenir une description des conditions préalables et de la requise pour la version logicielle actuelle.</span><span class="sxs-lookup"><span data-stu-id="f7961-115">Before you get started, see [the main Microsoft Defender for Endpoint on macOS page](microsoft-defender-endpoint-mac.md) for a description of prerequisites and system requirements for the current software version.</span></span>

## <a name="overview"></a><span data-ttu-id="f7961-116">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="f7961-116">Overview</span></span>

<span data-ttu-id="f7961-117">Le tableau suivant récapitule les étapes à suivre pour déployer et gérer Microsoft Defender pour endpoint sur Mac, via Intune.</span><span class="sxs-lookup"><span data-stu-id="f7961-117">The following table summarizes the steps you would need to take to deploy and manage Microsoft Defender for Endpoint on Macs, via Intune.</span></span> <span data-ttu-id="f7961-118">Des étapes plus détaillées sont disponibles ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f7961-118">More detailed steps are available below.</span></span>

| <span data-ttu-id="f7961-119">Étape</span><span class="sxs-lookup"><span data-stu-id="f7961-119">Step</span></span> | <span data-ttu-id="f7961-120">Exemples de noms de fichiers</span><span class="sxs-lookup"><span data-stu-id="f7961-120">Sample file names</span></span> | <span data-ttu-id="f7961-121">BundleIdentifier</span><span class="sxs-lookup"><span data-stu-id="f7961-121">BundleIdentifier</span></span> |
|-|-|-|
| [<span data-ttu-id="f7961-122">Télécharger le package d’intégration</span><span class="sxs-lookup"><span data-stu-id="f7961-122">Download the onboarding package</span></span>](#download-the-onboarding-package) | <span data-ttu-id="f7961-123">WindowsDefenderATPOnboarding__MDATP_wdav.atp.xml</span><span class="sxs-lookup"><span data-stu-id="f7961-123">WindowsDefenderATPOnboarding__MDATP_wdav.atp.xml</span></span> | <span data-ttu-id="f7961-124">com.microsoft.wdav.atp</span><span class="sxs-lookup"><span data-stu-id="f7961-124">com.microsoft.wdav.atp</span></span> |
| [<span data-ttu-id="f7961-125">Approuver l’extension système pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f7961-125">Approve System Extension for Microsoft Defender for Endpoint</span></span>](#approve-system-extensions) | <span data-ttu-id="f7961-126">MDATP_SysExt.xml</span><span class="sxs-lookup"><span data-stu-id="f7961-126">MDATP_SysExt.xml</span></span> | <span data-ttu-id="f7961-127">S/O</span><span class="sxs-lookup"><span data-stu-id="f7961-127">N/A</span></span> |
| [<span data-ttu-id="f7961-128">Approuver l’extension du noyau pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f7961-128">Approve Kernel Extension for Microsoft Defender for Endpoint</span></span>](#download-the-onboarding-package) | <span data-ttu-id="f7961-129">MDATP_KExt.xml</span><span class="sxs-lookup"><span data-stu-id="f7961-129">MDATP_KExt.xml</span></span> | <span data-ttu-id="f7961-130">S/O</span><span class="sxs-lookup"><span data-stu-id="f7961-130">N/A</span></span> |
| [<span data-ttu-id="f7961-131">Accorder un accès disque complet à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f7961-131">Grant full disk access to Microsoft Defender for Endpoint</span></span>](#full-disk-access) | <span data-ttu-id="f7961-132">MDATP_tcc_Catalina_or_newer.xml</span><span class="sxs-lookup"><span data-stu-id="f7961-132">MDATP_tcc_Catalina_or_newer.xml</span></span> | <span data-ttu-id="f7961-133">com.microsoft.wdav.tcc</span><span class="sxs-lookup"><span data-stu-id="f7961-133">com.microsoft.wdav.tcc</span></span> |
| [<span data-ttu-id="f7961-134">Stratégie d’extension réseau</span><span class="sxs-lookup"><span data-stu-id="f7961-134">Network Extension policy</span></span>](#network-filter) | <span data-ttu-id="f7961-135">MDATP_NetExt.xml</span><span class="sxs-lookup"><span data-stu-id="f7961-135">MDATP_NetExt.xml</span></span> | <span data-ttu-id="f7961-136">S/O</span><span class="sxs-lookup"><span data-stu-id="f7961-136">N/A</span></span> |
| [<span data-ttu-id="f7961-137">Configurer la mise à jour automatique Microsoft (AutoUpdate)</span><span class="sxs-lookup"><span data-stu-id="f7961-137">Configure Microsoft AutoUpdate (MAU)</span></span>](mac-updates.md#intune) | <span data-ttu-id="f7961-138">MDATP_Microsoft_AutoUpdate.xml</span><span class="sxs-lookup"><span data-stu-id="f7961-138">MDATP_Microsoft_AutoUpdate.xml</span></span> | <span data-ttu-id="f7961-139">com.microsoft.autoupdate2</span><span class="sxs-lookup"><span data-stu-id="f7961-139">com.microsoft.autoupdate2</span></span> |
| [<span data-ttu-id="f7961-140">Paramètres de configuration de Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="f7961-140">Microsoft Defender for Endpoint configuration settings</span></span>](mac-preferences.md#intune-profile-1)<br/><br/> <span data-ttu-id="f7961-141">**Remarque :** Si vous envisagez d’exécuter un antivirus tiers pour macOS, définissez sur `passiveMode` `true` .</span><span class="sxs-lookup"><span data-stu-id="f7961-141">**Note:** If you're planning to run a third-party AV for macOS, set `passiveMode` to `true`.</span></span> | <span data-ttu-id="f7961-142">MDATP_WDAV_and_exclusion_settings_Preferences.xml</span><span class="sxs-lookup"><span data-stu-id="f7961-142">MDATP_WDAV_and_exclusion_settings_Preferences.xml</span></span> | <span data-ttu-id="f7961-143">com.microsoft.wdav</span><span class="sxs-lookup"><span data-stu-id="f7961-143">com.microsoft.wdav</span></span> |
| [<span data-ttu-id="f7961-144">Configurer Microsoft Defender pour les notifications de point de terminaison et de mise à jour automatique MS (MAU)</span><span class="sxs-lookup"><span data-stu-id="f7961-144">Configure Microsoft Defender for Endpoint and MS AutoUpdate (MAU) notifications</span></span>](mac-updates.md) | <span data-ttu-id="f7961-145">MDATP_MDAV_Tray_and_AutoUpdate2.mobileconfig</span><span class="sxs-lookup"><span data-stu-id="f7961-145">MDATP_MDAV_Tray_and_AutoUpdate2.mobileconfig</span></span> | <span data-ttu-id="f7961-146">com.microsoft.autoupdate2 ou com.microsoft.wdav.tray</span><span class="sxs-lookup"><span data-stu-id="f7961-146">com.microsoft.autoupdate2 or com.microsoft.wdav.tray</span></span> |


## <a name="download-the-onboarding-package"></a><span data-ttu-id="f7961-147">Télécharger le package d’intégration</span><span class="sxs-lookup"><span data-stu-id="f7961-147">Download the onboarding package</span></span>

<span data-ttu-id="f7961-148">Téléchargez les packages d’intégration à partir Centre de sécurité Microsoft Defender :</span><span class="sxs-lookup"><span data-stu-id="f7961-148">Download the onboarding packages from Microsoft Defender Security Center:</span></span>

1. <span data-ttu-id="f7961-149">In Centre de sécurité Microsoft Defender, go to **Paramètres**  >  **Device Management**  >  **Onboarding**.</span><span class="sxs-lookup"><span data-stu-id="f7961-149">In Microsoft Defender Security Center, go to **Settings** > **Device Management** > **Onboarding**.</span></span>

2. <span data-ttu-id="f7961-150">Définissez le système d’exploitation sur **macOS** et la méthode de déploiement sur Gestion des périphériques **mobiles/Microsoft Intune**.</span><span class="sxs-lookup"><span data-stu-id="f7961-150">Set the operating system to **macOS** and the deployment method to **Mobile Device Management / Microsoft Intune**.</span></span>

    ![Capture d’écran des paramètres d’intégration](images/atp-mac-install.png)

3. <span data-ttu-id="f7961-152">Sélectionnez **Télécharger le package d’intégration.**</span><span class="sxs-lookup"><span data-stu-id="f7961-152">Select **Download onboarding package**.</span></span> <span data-ttu-id="f7961-153">Enregistrez-le _WindowsDefenderATPOnboardingPackage.zip_ dans le même répertoire.</span><span class="sxs-lookup"><span data-stu-id="f7961-153">Save it as _WindowsDefenderATPOnboardingPackage.zip_ to the same directory.</span></span>

4. <span data-ttu-id="f7961-154">Extrayez le contenu du fichier .zip :</span><span class="sxs-lookup"><span data-stu-id="f7961-154">Extract the contents of the .zip file:</span></span>

    ```bash
    unzip WindowsDefenderATPOnboardingPackage.zip
    ```
    ```Output
    Archive:  WindowsDefenderATPOnboardingPackage.zip
    warning:  WindowsDefenderATPOnboardingPackage.zip appears to use backslashes as path separators
      inflating: intune/kext.xml
      inflating: intune/WindowsDefenderATPOnboarding.xml
      inflating: jamf/WindowsDefenderATPOnboarding.plist
    ```

## <a name="create-system-configuration-profiles"></a><span data-ttu-id="f7961-155">Créer des profils de configuration système</span><span class="sxs-lookup"><span data-stu-id="f7961-155">Create System Configuration profiles</span></span>

<span data-ttu-id="f7961-156">L’étape suivante consiste à créer des profils de configuration système dont Microsoft Defender pour le point de terminaison a besoin.</span><span class="sxs-lookup"><span data-stu-id="f7961-156">The next step is to create system configuration profiles that Microsoft Defender for Endpoint needs.</span></span>
<span data-ttu-id="f7961-157">Dans le centre [Microsoft Endpoint Manager' administration,](https://endpoint.microsoft.com/)ouvrez les **profils**  >  **de configuration des appareils.**</span><span class="sxs-lookup"><span data-stu-id="f7961-157">In the [Microsoft Endpoint Manager admin center](https://endpoint.microsoft.com/), open **Devices** > **Configuration profiles**.</span></span>

### <a name="onboarding-blob"></a><span data-ttu-id="f7961-158">Blob d’intégration</span><span class="sxs-lookup"><span data-stu-id="f7961-158">Onboarding blob</span></span>

<span data-ttu-id="f7961-159">Ce profil contient des informations de licence pour Microsoft Defender pour le point de terminaison, sans qu’il signale qu’il n’est pas titulaire d’une licence.</span><span class="sxs-lookup"><span data-stu-id="f7961-159">This profile contains a license information for Microsoft Defender for Endpoint, without it it will report that it is not licensed.</span></span>

1. <span data-ttu-id="f7961-160">Sélectionnez **Créer un profil** sous **Profils de configuration.**</span><span class="sxs-lookup"><span data-stu-id="f7961-160">Select **Create Profile** under **Configuration Profiles**.</span></span>
1. <span data-ttu-id="f7961-161">Select **Platform** = **macOS**, **Profile type** = **Templates**.</span><span class="sxs-lookup"><span data-stu-id="f7961-161">Select **Platform**=**macOS**, **Profile type**=**Templates**.</span></span> <span data-ttu-id="f7961-162">**Nom du modèle** = **Personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="f7961-162">**Template name**=**Custom**.</span></span> <span data-ttu-id="f7961-163">Cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="f7961-163">Click **Create**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f7961-164">![Création d’un profil de configuration personnalisé](images/mdatp-6-systemconfigurationprofiles-1.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-164">![Custom Configuration Profile creation](images/mdatp-6-systemconfigurationprofiles-1.png)</span></span>

1. <span data-ttu-id="f7961-165">Choisissez un nom pour le profil, par exemple, « Intégration de Defender ou de point de terminaison pour macOS ».</span><span class="sxs-lookup"><span data-stu-id="f7961-165">Choose a name for the profile, e.g., "Defender or Endpoint onboarding for macOS".</span></span> <span data-ttu-id="f7961-166">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f7961-166">Click **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f7961-167">![Profil de configuration personnalisé - nom](images/mdatp-6-systemconfigurationprofiles-2.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-167">![Custom Configuration Profile - name](images/mdatp-6-systemconfigurationprofiles-2.png)</span></span>

1. <span data-ttu-id="f7961-168">Choisissez un nom pour le nom du profil de configuration, par exemple« Defender pour l’intégration de point de terminaison pour macOS ».</span><span class="sxs-lookup"><span data-stu-id="f7961-168">Choose a name for the configuration profile name, e.g., "Defender for Endpoint onboarding for macOS".</span></span>
1. <span data-ttu-id="f7961-169">Sélectionnez intune/WindowsDefenderATPOnboarding.xml que vous avez extrait du package d’intégration ci-dessus en tant que fichier de profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="f7961-169">Select intune/WindowsDefenderATPOnboarding.xml that you extracted from the onboarding package above as configuration profile file.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f7961-170">![Importer une configuration à partir d’un fichier pour le profil de configuration personnalisé](images/mdatp-6-systemconfigurationprofiles.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-170">![Import a configuration from a file for Custom Configuration Profile](images/mdatp-6-systemconfigurationprofiles.png)</span></span>

1. <span data-ttu-id="f7961-171">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f7961-171">Click **Next**.</span></span>
1. <span data-ttu-id="f7961-172">Affectez des appareils sous **l’onglet** Affectation. Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f7961-172">Assign devices on the **Assignment** tab. Click **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f7961-173">![Profil de configuration personnalisé : affectation](images/mdatp-6-systemconfigurationprofiles-2.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-173">![Custom Configuration Profile - assignment](images/mdatp-6-systemconfigurationprofiles-2.png)</span></span>

1. <span data-ttu-id="f7961-174">Révision et **création.**</span><span class="sxs-lookup"><span data-stu-id="f7961-174">Review and **Create**.</span></span>
1. <span data-ttu-id="f7961-175">Ouvrez **les**  >  **profils de configuration des** appareils, vous pouvez y voir votre profil créé.</span><span class="sxs-lookup"><span data-stu-id="f7961-175">Open **Devices** > **Configuration profiles**, you can see your created profile there.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f7961-176">![Profil de configuration personnalisé - terminé](images/mdatp-6-systemconfigurationprofiles-3.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-176">![Custom Configuration Profile - done](images/mdatp-6-systemconfigurationprofiles-3.png)</span></span>

### <a name="approve-system-extensions"></a><span data-ttu-id="f7961-177">Approuver les extensions système</span><span class="sxs-lookup"><span data-stu-id="f7961-177">Approve System Extensions</span></span>

<span data-ttu-id="f7961-178">Ce profil est nécessaire pour macOS 10.15 (Îlelier) ou une nouvelle génération.</span><span class="sxs-lookup"><span data-stu-id="f7961-178">This profile is needed for macOS 10.15 (Catalina) or newer.</span></span> <span data-ttu-id="f7961-179">Il sera ignoré sur les anciens macOS.</span><span class="sxs-lookup"><span data-stu-id="f7961-179">It will be ignored on older macOS.</span></span>

1. <span data-ttu-id="f7961-180">Sélectionnez **Créer un profil** sous **Profils de configuration.**</span><span class="sxs-lookup"><span data-stu-id="f7961-180">Select **Create Profile** under **Configuration Profiles**.</span></span>
1. <span data-ttu-id="f7961-181">Select **Platform** = **macOS**, **Profile type** = **Templates**.</span><span class="sxs-lookup"><span data-stu-id="f7961-181">Select **Platform**=**macOS**, **Profile type**=**Templates**.</span></span> <span data-ttu-id="f7961-182">**Nom du modèle** = **Extensions**.</span><span class="sxs-lookup"><span data-stu-id="f7961-182">**Template name**=**Extensions**.</span></span> <span data-ttu-id="f7961-183">Cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="f7961-183">Click **Create**.</span></span>
1. <span data-ttu-id="f7961-184">Dans **l’onglet Basics,** nommez ce nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="f7961-184">In the **Basics** tab, give a name to this new profile.</span></span>
1. <span data-ttu-id="f7961-185">Dans **l’onglet Paramètres de configuration,** développez Extensions système et ajoutez les **entrées** suivantes dans la section **Extensions système autorisées** :</span><span class="sxs-lookup"><span data-stu-id="f7961-185">In the **Configuration settings** tab, expand **System Extensions** add the following entries in the **Allowed system extensions** section:</span></span>

    <span data-ttu-id="f7961-186">Identificateur d’ensemble</span><span class="sxs-lookup"><span data-stu-id="f7961-186">Bundle identifier</span></span>         | <span data-ttu-id="f7961-187">Identificateur d’équipe</span><span class="sxs-lookup"><span data-stu-id="f7961-187">Team identifier</span></span>
    --------------------------|----------------
    <span data-ttu-id="f7961-188">com.microsoft.wdav.epsext</span><span class="sxs-lookup"><span data-stu-id="f7961-188">com.microsoft.wdav.epsext</span></span> | <span data-ttu-id="f7961-189">UBF8T346G9</span><span class="sxs-lookup"><span data-stu-id="f7961-189">UBF8T346G9</span></span>
    <span data-ttu-id="f7961-190">com.microsoft.wdav.netext</span><span class="sxs-lookup"><span data-stu-id="f7961-190">com.microsoft.wdav.netext</span></span> | <span data-ttu-id="f7961-191">UBF8T346G9</span><span class="sxs-lookup"><span data-stu-id="f7961-191">UBF8T346G9</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f7961-192">![Paramètres d’extension système](images/mac-system-extension-intune2.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-192">![System extension settings](images/mac-system-extension-intune2.png)</span></span>

1. <span data-ttu-id="f7961-193">Dans **l’onglet Affectations,** affectez ce profil à tous les **utilisateurs & tous les appareils.**</span><span class="sxs-lookup"><span data-stu-id="f7961-193">In the **Assignments** tab, assign this profile to **All Users & All devices**.</span></span>
1. <span data-ttu-id="f7961-194">Examinez et créez ce profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="f7961-194">Review and create this configuration profile.</span></span>

### <a name="kernel-extensions"></a><span data-ttu-id="f7961-195">Extensions de noyau</span><span class="sxs-lookup"><span data-stu-id="f7961-195">Kernel Extensions</span></span>

<span data-ttu-id="f7961-196">Ce profil est nécessaire pour macOS 10.15 (Genre) ou une ancienne.</span><span class="sxs-lookup"><span data-stu-id="f7961-196">This profile is needed for macOS 10.15 (Catalina) or older.</span></span> <span data-ttu-id="f7961-197">Il sera ignoré sur les nouveaux macOS.</span><span class="sxs-lookup"><span data-stu-id="f7961-197">It will be ignored on newer macOS.</span></span>

> [!CAUTION]
> <span data-ttu-id="f7961-198">Les appareils Apple Silicon (M1) ne supportent pas KEXT.</span><span class="sxs-lookup"><span data-stu-id="f7961-198">Apple Silicon (M1) devices do not support KEXT.</span></span> <span data-ttu-id="f7961-199">L’installation d’un profil de configuration constitué de stratégies KEXT échoue sur ces appareils.</span><span class="sxs-lookup"><span data-stu-id="f7961-199">Installation of a configuration profile consisting KEXT policies will fail on these devices.</span></span>

1. <span data-ttu-id="f7961-200">Sélectionnez **Créer un profil** sous **Profils de configuration.**</span><span class="sxs-lookup"><span data-stu-id="f7961-200">Select **Create Profile** under **Configuration Profiles**.</span></span>
1. <span data-ttu-id="f7961-201">Select **Platform** = **macOS**, **Profile type** = **Templates**.</span><span class="sxs-lookup"><span data-stu-id="f7961-201">Select **Platform**=**macOS**, **Profile type**=**Templates**.</span></span> <span data-ttu-id="f7961-202">**Nom du modèle** = **Extensions**.</span><span class="sxs-lookup"><span data-stu-id="f7961-202">**Template name**=**Extensions**.</span></span> <span data-ttu-id="f7961-203">Cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="f7961-203">Click **Create**.</span></span>
1. <span data-ttu-id="f7961-204">Dans **l’onglet Basics,** nommez ce nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="f7961-204">In the **Basics** tab, give a name to this new profile.</span></span>
1. <span data-ttu-id="f7961-205">Dans **l’onglet Paramètres de configuration,** développez **Extensions de noyau.**</span><span class="sxs-lookup"><span data-stu-id="f7961-205">In the **Configuration settings** tab, expand **Kernel Extensions**.</span></span>
1. <span data-ttu-id="f7961-206">Définissez **l’identificateur** d’équipe **sur UBF8T346G9** et cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f7961-206">Set **Team identifier** to **UBF8T346G9** and click **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f7961-207">![Paramètres d’extension du noyau](images/mac-kernel-extension-intune2.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-207">![Kernel extension settings](images/mac-kernel-extension-intune2.png)</span></span>

1. <span data-ttu-id="f7961-208">Dans **l’onglet Affectations,** affectez ce profil à tous les **utilisateurs & tous les appareils.**</span><span class="sxs-lookup"><span data-stu-id="f7961-208">In the **Assignments** tab, assign this profile to **All Users & All devices**.</span></span>
1. <span data-ttu-id="f7961-209">Examinez et créez ce profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="f7961-209">Review and create this configuration profile.</span></span>

### <a name="full-disk-access"></a><span data-ttu-id="f7961-210">Accès disque total</span><span class="sxs-lookup"><span data-stu-id="f7961-210">Full Disk Access</span></span>

   > [!CAUTION]
   > <span data-ttu-id="f7961-211">macOS 10.15 (Contrôle) contient de nouvelles améliorations en matière de sécurité et de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="f7961-211">macOS 10.15 (Catalina) contains new security and privacy enhancements.</span></span> <span data-ttu-id="f7961-212">À partir de cette version, par défaut, les applications ne peuvent pas accéder à certains emplacements sur le disque (par exemple, Documents, Téléchargements, Bureau, etc.) sans consentement explicite.</span><span class="sxs-lookup"><span data-stu-id="f7961-212">Beginning with this version, by default, applications are not able to access certain locations on disk (such as Documents, Downloads, Desktop, etc.) without explicit consent.</span></span> <span data-ttu-id="f7961-213">En l’absence de ce consentement, Microsoft Defender pour le point de terminaison n’est pas en mesure de protéger entièrement votre appareil.</span><span class="sxs-lookup"><span data-stu-id="f7961-213">In the absence of this consent, Microsoft Defender for Endpoint is not able to fully protect your device.</span></span>
   >
   > <span data-ttu-id="f7961-214">Ce profil de configuration accorde un accès disque total à Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f7961-214">This configuration profile grants Full Disk Access to Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="f7961-215">Si vous avez précédemment configuré Microsoft Defender pour endpoint via Intune, nous vous recommandons de mettre à jour le déploiement avec ce profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="f7961-215">If you previously configured Microsoft Defender for Endpoint through Intune, we recommend you update the deployment with this configuration profile.</span></span>

<span data-ttu-id="f7961-216">Téléchargez [**fulldisk.mobileconfig à**](https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/mobileconfig/profiles/fulldisk.mobileconfig) partir de [notre GitHub.](https://github.com/microsoft/mdatp-xplat/tree/master/macos/mobileconfig/profiles)</span><span class="sxs-lookup"><span data-stu-id="f7961-216">Download [**fulldisk.mobileconfig**](https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/mobileconfig/profiles/fulldisk.mobileconfig) from [our GitHub repository](https://github.com/microsoft/mdatp-xplat/tree/master/macos/mobileconfig/profiles).</span></span>

<span data-ttu-id="f7961-217">Suivez les instructions d’intégration du [blob](#onboarding-blob) ci-dessus, en utilisant « Defender for Endpoint Full Disk Access » comme nom de profil et **téléchargé fulldisk.mobileconfig** comme nom de profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="f7961-217">Follow the instructions for [Onboarding blob](#onboarding-blob) from above, using "Defender for Endpoint Full Disk Access" as profile name, and downloaded **fulldisk.mobileconfig** as Configuration profile name.</span></span>

### <a name="network-filter"></a><span data-ttu-id="f7961-218">Filtre réseau</span><span class="sxs-lookup"><span data-stu-id="f7961-218">Network Filter</span></span>

<span data-ttu-id="f7961-219">Dans le cadre des fonctionnalités de détection et de réponse des points de terminaison, Microsoft Defender for Endpoint sur macOS inspecte le trafic de socket et signale ces informations au portail Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="f7961-219">As part of the Endpoint Detection and Response capabilities, Microsoft Defender for Endpoint on macOS inspects socket traffic and reports this information to the Microsoft Defender Security Center portal.</span></span> <span data-ttu-id="f7961-220">La stratégie suivante permet à l’extension réseau d’effectuer cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="f7961-220">The following policy allows the network extension to perform this functionality.</span></span>

<span data-ttu-id="f7961-221">Téléchargez [**netfilter.mobileconfig à**](https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/mobileconfig/profiles/netfilter.mobileconfig) partir de [notre GitHub.](https://github.com/microsoft/mdatp-xplat/tree/master/macos/mobileconfig/profiles)</span><span class="sxs-lookup"><span data-stu-id="f7961-221">Download [**netfilter.mobileconfig**](https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/mobileconfig/profiles/netfilter.mobileconfig) from [our GitHub repository](https://github.com/microsoft/mdatp-xplat/tree/master/macos/mobileconfig/profiles).</span></span>

<span data-ttu-id="f7961-222">Suivez les instructions d’intégration de [blob](#onboarding-blob) ci-dessus, en utilisant « Defender for Endpoint Network Filter » comme nom de profil et le fichier **netfilter.mobileconfig** téléchargé en tant que nom de profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="f7961-222">Follow the instructions for [Onboarding blob](#onboarding-blob) from above, using "Defender for Endpoint Network Filter" as profile name, and downloaded **netfilter.mobileconfig** as Configuration profile name.</span></span>

### <a name="notifications"></a><span data-ttu-id="f7961-223">Notifications</span><span class="sxs-lookup"><span data-stu-id="f7961-223">Notifications</span></span>

<span data-ttu-id="f7961-224">Ce profil permet à Microsoft Defender pour point de terminaison sur macOS et Microsoft Auto Update d’afficher des notifications dans l’interface utilisateur sur macOS 10.15 (Fonctionnalité) ou version plus nouvelle.</span><span class="sxs-lookup"><span data-stu-id="f7961-224">This profile is used to allow Microsoft Defender for Endpoint on macOS and Microsoft Auto Update to display notifications in UI on macOS 10.15 (Catalina) or newer.</span></span>

<span data-ttu-id="f7961-225">Téléchargez [**notif.mobileconfig à partir**](https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/mobileconfig/profiles/notif.mobileconfig) [de notre GitHub.](https://github.com/microsoft/mdatp-xplat/tree/master/macos/mobileconfig/profiles)</span><span class="sxs-lookup"><span data-stu-id="f7961-225">Download [**notif.mobileconfig**](https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/mobileconfig/profiles/notif.mobileconfig) from [our GitHub repository](https://github.com/microsoft/mdatp-xplat/tree/master/macos/mobileconfig/profiles).</span></span>

<span data-ttu-id="f7961-226">Suivez les instructions d’intégration de [blob](#onboarding-blob) ci-dessus, en utilisant « Defender pour les notifications de point de terminaison » comme nom de profil et téléchargé **notif.mobileconfig** comme nom de profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="f7961-226">Follow the instructions for [Onboarding blob](#onboarding-blob) from above, using "Defender for Endpoint Notifications" as profile name, and downloaded **notif.mobileconfig** as Configuration profile name.</span></span>

### <a name="view-status"></a><span data-ttu-id="f7961-227">Afficher l’état</span><span class="sxs-lookup"><span data-stu-id="f7961-227">View Status</span></span>

<span data-ttu-id="f7961-228">Une fois que les modifications Intune sont propagées aux appareils inscrits, vous pouvez les voir répertoriées sous État de  >  **l’appareil de surveillance**:</span><span class="sxs-lookup"><span data-stu-id="f7961-228">Once the Intune changes are propagated to the enrolled devices, you can see them listed under **Monitor** > **Device status**:</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="f7961-229">![Affichage de l’état de l’appareil dans le moniteur](images/mdatp-7-devicestatusblade.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-229">![View of Device Status in Monitor](images/mdatp-7-devicestatusblade.png)</span></span>

## <a name="publish-application"></a><span data-ttu-id="f7961-230">Publier l'application</span><span class="sxs-lookup"><span data-stu-id="f7961-230">Publish application</span></span>

<span data-ttu-id="f7961-231">Cette étape permet de déployer Microsoft Defender pour le point de terminaison sur les ordinateurs inscrits.</span><span class="sxs-lookup"><span data-stu-id="f7961-231">This step enables deploying Microsoft Defender for Endpoint to enrolled machines.</span></span>

1. <span data-ttu-id="f7961-232">Dans le centre [Microsoft Endpoint Manager' administration,](https://endpoint.microsoft.com/)ouvrez **Applications.**</span><span class="sxs-lookup"><span data-stu-id="f7961-232">In the [Microsoft Endpoint Manager admin center](https://endpoint.microsoft.com/), open **Apps**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f7961-233">![Prêt à créer une application](images/mdatp-8-app-before.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-233">![Ready to create application](images/mdatp-8-app-before.png)</span></span>

1. <span data-ttu-id="f7961-234">Sélectionnez Par plateforme > macOS > Ajouter.</span><span class="sxs-lookup"><span data-stu-id="f7961-234">Select By platform > macOS > Add.</span></span>
1. <span data-ttu-id="f7961-235">Choose **App type** = **macOS,** click **Select**.</span><span class="sxs-lookup"><span data-stu-id="f7961-235">Choose **App type**=**macOS**, click **Select**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f7961-236">![Spécifier le type d’application](images/mdatp-9-app-type.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-236">![Specify application type](images/mdatp-9-app-type.png)</span></span>

1. <span data-ttu-id="f7961-237">Conservez les valeurs par défaut, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f7961-237">Keep default values, click **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f7961-238">![Propriétés de l’application](images/mdatp-10-properties.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-238">![Application properties](images/mdatp-10-properties.png)</span></span>

1. <span data-ttu-id="f7961-239">Ajouter des affectations, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f7961-239">Add assignments, click **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f7961-240">![Capture d’écran des informations sur les affectations Intune](images/mdatp-11-assignments.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-240">![Intune assignments info screenshot](images/mdatp-11-assignments.png)</span></span>

1. <span data-ttu-id="f7961-241">Révision et **création.**</span><span class="sxs-lookup"><span data-stu-id="f7961-241">Review and **Create**.</span></span>
1. <span data-ttu-id="f7961-242">Vous pouvez visiter **Apps** By  >  **platform**  >  **macOS** pour le voir dans la liste de toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="f7961-242">You can visit **Apps** > **By platform** > **macOS** to see it on the list of all applications.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f7961-243">![Liste des applications](images/mdatp-12-applications.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-243">![Applications list](images/mdatp-12-applications.png)</span></span>

<span data-ttu-id="f7961-244">(Vous trouverez des informations détaillées sur la [page Intune](/mem/intune/apps/apps-advanced-threat-protection-macos)pour le déploiement de Defender.)</span><span class="sxs-lookup"><span data-stu-id="f7961-244">(You can find detailed information on the [Intune's page for Defender deployment](/mem/intune/apps/apps-advanced-threat-protection-macos).)</span></span>

   > [!CAUTION]
   > <span data-ttu-id="f7961-245">Vous devez créer tous les profils de configuration requis et les pousser vers tous les ordinateurs, comme expliqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="f7961-245">You have to create all required configuration profiles and push them to all machines, as explained above.</span></span>

## <a name="client-device-setup"></a><span data-ttu-id="f7961-246">Configuration de l’appareil client</span><span class="sxs-lookup"><span data-stu-id="f7961-246">Client device setup</span></span>

<span data-ttu-id="f7961-247">Vous n’avez pas besoin d’une mise en service spéciale pour un appareil Mac au-delà [d’une installation Portail d’entreprise standard.](/intune-user-help/enroll-your-device-in-intune-macos-cp)</span><span class="sxs-lookup"><span data-stu-id="f7961-247">You don't need any special provisioning for a Mac device beyond a standard [Company Portal installation](/intune-user-help/enroll-your-device-in-intune-macos-cp).</span></span>

1. <span data-ttu-id="f7961-248">Confirmez la gestion des appareils.</span><span class="sxs-lookup"><span data-stu-id="f7961-248">Confirm device management.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f7961-249">![Confirmer la capture d’écran de la gestion des appareils](images/mdatp-3-confirmdevicemgmt.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-249">![Confirm device management screenshot](images/mdatp-3-confirmdevicemgmt.png)</span></span>

    <span data-ttu-id="f7961-250">Sélectionnez **Ouvrir les préférences système,** recherchez **Profil** de gestion dans la liste, puis sélectionnez **Approuver...**. Votre profil de gestion s’affiche comme **vérifié**:</span><span class="sxs-lookup"><span data-stu-id="f7961-250">Select **Open System Preferences**, locate **Management Profile** on the list, and select **Approve...**. Your Management Profile would be displayed as **Verified**:</span></span>

    ![Capture d’écran du profil de gestion](images/mdatp-4-managementprofile.png)

2. <span data-ttu-id="f7961-252">Sélectionnez **Continuer** et terminez l’inscription.</span><span class="sxs-lookup"><span data-stu-id="f7961-252">Select **Continue** and complete the enrollment.</span></span>

   <span data-ttu-id="f7961-253">Vous pouvez maintenant inscrire davantage d’appareils.</span><span class="sxs-lookup"><span data-stu-id="f7961-253">You may now enroll more devices.</span></span> <span data-ttu-id="f7961-254">Vous pouvez également les inscrire ultérieurement, une fois que vous avez terminé l’approvisionnement de la configuration système et des packages d’application.</span><span class="sxs-lookup"><span data-stu-id="f7961-254">You can also enroll them later, after you have finished provisioning system configuration and application packages.</span></span>

3. <span data-ttu-id="f7961-255">Dans Intune, ouvrez **Gérer**  >  **tous les**  >  **appareils.**</span><span class="sxs-lookup"><span data-stu-id="f7961-255">In Intune, open **Manage** > **Devices** > **All devices**.</span></span> <span data-ttu-id="f7961-256">Ici, vous pouvez voir votre appareil parmi ceux répertoriés :</span><span class="sxs-lookup"><span data-stu-id="f7961-256">Here you can see your device among those listed:</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="f7961-257">![Capture d’écran Ajouter des appareils](images/mdatp-5-alldevices.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-257">![Add Devices screenshot](images/mdatp-5-alldevices.png)</span></span>

## <a name="verify-client-device-state"></a><span data-ttu-id="f7961-258">Vérifier l’état de l’appareil client</span><span class="sxs-lookup"><span data-stu-id="f7961-258">Verify client device state</span></span>

1. <span data-ttu-id="f7961-259">Une fois les profils de configuration déployés sur vos appareils, ouvrez les **profils** de préférences  >  **système** sur votre appareil Mac.</span><span class="sxs-lookup"><span data-stu-id="f7961-259">After the configuration profiles are deployed to your devices, open **System Preferences** > **Profiles** on your Mac device.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f7961-260">![Capture d’écran des préférences système](images/mdatp-13-systempreferences.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-260">![System Preferences screenshot](images/mdatp-13-systempreferences.png)</span></span>

    ![Capture d’écran des profils de préférences système](images/mdatp-14-systempreferencesprofiles.png)

2. <span data-ttu-id="f7961-262">Vérifiez que les profils de configuration suivants sont présents et installés.</span><span class="sxs-lookup"><span data-stu-id="f7961-262">Verify that the following configuration profiles are present and installed.</span></span> <span data-ttu-id="f7961-263">Le **profil de** gestion doit être le profil système Intune.</span><span class="sxs-lookup"><span data-stu-id="f7961-263">The **Management Profile** should be the Intune system profile.</span></span> <span data-ttu-id="f7961-264">_Wdav-config_ et _wdav-kext_ sont des profils de configuration système qui ont été ajoutés dans Intune :</span><span class="sxs-lookup"><span data-stu-id="f7961-264">_Wdav-config_ and _wdav-kext_ are system configuration profiles that were added in Intune:</span></span>

    ![Capture d’écran des profils](images/mdatp-15-managementprofileconfig.png)

3. <span data-ttu-id="f7961-266">Vous devez également voir l’icône Microsoft Defender pour point de terminaison dans le coin supérieur droit :</span><span class="sxs-lookup"><span data-stu-id="f7961-266">You should also see the Microsoft Defender for Endpoint icon in the top-right corner:</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f7961-267">![Icône Microsoft Defender pour point de terminaison dans la capture d’écran de la barre d’état](images/mdatp-icon-bar.png)</span><span class="sxs-lookup"><span data-stu-id="f7961-267">![Microsoft Defender for Endpoint icon in status bar screenshot](images/mdatp-icon-bar.png)</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="f7961-268">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="f7961-268">Troubleshooting</span></span>

<span data-ttu-id="f7961-269">Problème : aucune licence trouvée.</span><span class="sxs-lookup"><span data-stu-id="f7961-269">Issue: No license found.</span></span>

<span data-ttu-id="f7961-270">Solution : suivez les étapes ci-dessus pour créer un profil d’appareil à l’aide WindowsDefenderATPOnboarding.xml.</span><span class="sxs-lookup"><span data-stu-id="f7961-270">Solution: Follow the steps above to create a device profile using WindowsDefenderATPOnboarding.xml.</span></span>

## <a name="logging-installation-issues"></a><span data-ttu-id="f7961-271">Journalisation des problèmes d’installation</span><span class="sxs-lookup"><span data-stu-id="f7961-271">Logging installation issues</span></span>

<span data-ttu-id="f7961-272">Pour plus d’informations sur la recherche du journal généré automatiquement par le programme d’installation en cas d’erreur, voir [Problèmes d’installation de journalisation.](mac-resources.md#logging-installation-issues)</span><span class="sxs-lookup"><span data-stu-id="f7961-272">For more information on how to find the automatically generated log that is created by the installer when an error occurs, see [Logging installation issues](mac-resources.md#logging-installation-issues).</span></span>

## <a name="uninstallation"></a><span data-ttu-id="f7961-273">Désinstallation</span><span class="sxs-lookup"><span data-stu-id="f7961-273">Uninstallation</span></span>

<span data-ttu-id="f7961-274">Voir [Désinstallation](mac-resources.md#uninstalling) pour plus d’informations sur la suppression de Microsoft Defender pour Endpoint sur macOS des appareils clients.</span><span class="sxs-lookup"><span data-stu-id="f7961-274">See [Uninstalling](mac-resources.md#uninstalling) for details on how to remove Microsoft Defender for Endpoint on macOS from client devices.</span></span>
