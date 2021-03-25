---
title: Déploiement basé sur Intune pour Microsoft Defender ATP pour Mac
description: Installez Microsoft Defender pour endpoint pour Mac, à l’aide de Microsoft Intune.
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
ms.openlocfilehash: 94cb92974b0e73a1254fd024c39d9a6ee620aad3
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51199536"
---
# <a name="intune-based-deployment-for-microsoft-defender-for-endpoint-for-mac"></a><span data-ttu-id="fcdc1-104">Déploiement basé sur Intune pour Microsoft Defender pour Endpoint pour Mac</span><span class="sxs-lookup"><span data-stu-id="fcdc1-104">Intune-based deployment for Microsoft Defender for Endpoint for Mac</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


> [!NOTE]
> <span data-ttu-id="fcdc1-105">Cette documentation explique la méthode héritée pour déployer et configurer Microsoft Defender pour endpoint sur les appareils macOS.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-105">This documentation explains the legacy method for deploying and configuring Microsoft Defender for Endpoint on macOS devices.</span></span> <span data-ttu-id="fcdc1-106">L’expérience native est désormais disponible dans la console MEM.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-106">The native experience is now available in the MEM console.</span></span> <span data-ttu-id="fcdc1-107">La version de l’interface utilisateur native dans la console MEM offre aux administrateurs un moyen beaucoup plus simple de configurer et de déployer l’application et de l’envoyer aux appareils macOS.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-107">The release of the native UI in the MEM console provide admins with a much simpler way to configure and deploy the application and send it down to macOS devices.</span></span> <br> <br>
><span data-ttu-id="fcdc1-108">Le billet de blog mem simplifie le déploiement [de Microsoft Defender pour endpoint pour macOS](https://techcommunity.microsoft.com/t5/microsoft-endpoint-manager-blog/microsoft-endpoint-manager-simplifies-deployment-of-microsoft/ba-p/1322995) explique les nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-108">The blog post [MEM simplifies deployment of Microsoft Defender for Endpoint for macOS](https://techcommunity.microsoft.com/t5/microsoft-endpoint-manager-blog/microsoft-endpoint-manager-simplifies-deployment-of-microsoft/ba-p/1322995) explains the new features.</span></span> <span data-ttu-id="fcdc1-109">Pour configurer l’application, go to [Settings for Microsoft Defender for Endpoint for Mac in Microsoft InTune](https://docs.microsoft.com/mem/intune/protect/antivirus-microsoft-defender-settings-macos).</span><span class="sxs-lookup"><span data-stu-id="fcdc1-109">To configure the app, go to [Settings for Microsoft Defender for Endpoint for Mac in Microsoft InTune](https://docs.microsoft.com/mem/intune/protect/antivirus-microsoft-defender-settings-macos).</span></span> <span data-ttu-id="fcdc1-110">Pour déployer l’application, go to [Add Microsoft Defender for Endpoint to macOS devices using Microsoft Intune](https://docs.microsoft.com/mem/intune/apps/apps-advanced-threat-protection-macos).</span><span class="sxs-lookup"><span data-stu-id="fcdc1-110">To deploy the app, go to [Add Microsoft Defender for Endpoint to macOS devices using Microsoft Intune](https://docs.microsoft.com/mem/intune/apps/apps-advanced-threat-protection-macos).</span></span>

<span data-ttu-id="fcdc1-111">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-111">**Applies to:**</span></span>

- [<span data-ttu-id="fcdc1-112">Microsoft Defender pour point de terminaison pour Mac</span><span class="sxs-lookup"><span data-stu-id="fcdc1-112">Microsoft Defender for Endpoint for Mac</span></span>](microsoft-defender-endpoint-mac.md)

<span data-ttu-id="fcdc1-113">Cette rubrique décrit comment déployer Microsoft Defender pour Endpoint pour Mac via Intune.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-113">This topic describes how to deploy Microsoft Defender for Endpoint for Mac through Intune.</span></span> <span data-ttu-id="fcdc1-114">Un déploiement réussi nécessite la réalisation de toutes les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="fcdc1-114">A successful deployment requires the completion of all of the following steps:</span></span>

1. [<span data-ttu-id="fcdc1-115">Télécharger les packages d’installation et d’intégration</span><span class="sxs-lookup"><span data-stu-id="fcdc1-115">Download installation and onboarding packages</span></span>](#download-installation-and-onboarding-packages)
1. [<span data-ttu-id="fcdc1-116">Configuration de l’appareil client</span><span class="sxs-lookup"><span data-stu-id="fcdc1-116">Client device setup</span></span>](#client-device-setup)
1. [<span data-ttu-id="fcdc1-117">Approuver les extensions système</span><span class="sxs-lookup"><span data-stu-id="fcdc1-117">Approve system extensions</span></span>](#approve-system-extensions)
1. [<span data-ttu-id="fcdc1-118">Créer des profils de configuration système</span><span class="sxs-lookup"><span data-stu-id="fcdc1-118">Create System Configuration profiles</span></span>](#create-system-configuration-profiles)
1. [<span data-ttu-id="fcdc1-119">Publier l'application</span><span class="sxs-lookup"><span data-stu-id="fcdc1-119">Publish application</span></span>](#publish-application)

## <a name="prerequisites-and-system-requirements"></a><span data-ttu-id="fcdc1-120">Conditions préalables et système requis</span><span class="sxs-lookup"><span data-stu-id="fcdc1-120">Prerequisites and system requirements</span></span>

<span data-ttu-id="fcdc1-121">Avant de commencer, consultez la page principale de [Microsoft Defender pour Endpoint pour Mac](microsoft-defender-endpoint-mac.md) pour obtenir une description des conditions préalables et de la requise pour la version logicielle actuelle.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-121">Before you get started, see [the main Microsoft Defender for Endpoint for Mac page](microsoft-defender-endpoint-mac.md) for a description of prerequisites and system requirements for the current software version.</span></span>

## <a name="overview"></a><span data-ttu-id="fcdc1-122">Présentation</span><span class="sxs-lookup"><span data-stu-id="fcdc1-122">Overview</span></span>

<span data-ttu-id="fcdc1-123">Le tableau suivant récapitule les étapes à suivre pour déployer et gérer Microsoft Defender pour Endpoint pour Mac, via Intune.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-123">The following table summarizes the steps you would need to take to deploy and manage Microsoft Defender for Endpoint for Macs, via Intune.</span></span> <span data-ttu-id="fcdc1-124">Des étapes plus détaillées sont disponibles ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-124">More detailed steps are available below.</span></span>

| <span data-ttu-id="fcdc1-125">Étape</span><span class="sxs-lookup"><span data-stu-id="fcdc1-125">Step</span></span> | <span data-ttu-id="fcdc1-126">Exemples de noms de fichiers</span><span class="sxs-lookup"><span data-stu-id="fcdc1-126">Sample file names</span></span> | <span data-ttu-id="fcdc1-127">BundleIdentifier</span><span class="sxs-lookup"><span data-stu-id="fcdc1-127">BundleIdentifier</span></span> |
|-|-|-|
| [<span data-ttu-id="fcdc1-128">Télécharger les packages d’installation et d’intégration</span><span class="sxs-lookup"><span data-stu-id="fcdc1-128">Download installation and onboarding packages</span></span>](#download-installation-and-onboarding-packages) | <span data-ttu-id="fcdc1-129">WindowsDefenderATPOnboarding__MDATP_wdav.atp.xml</span><span class="sxs-lookup"><span data-stu-id="fcdc1-129">WindowsDefenderATPOnboarding__MDATP_wdav.atp.xml</span></span> | <span data-ttu-id="fcdc1-130">com.microsoft.wdav.atp</span><span class="sxs-lookup"><span data-stu-id="fcdc1-130">com.microsoft.wdav.atp</span></span> |
| [<span data-ttu-id="fcdc1-131">Approuver l’extension système pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fcdc1-131">Approve System Extension for Microsoft Defender for Endpoint</span></span>](#approve-system-extensions) | <span data-ttu-id="fcdc1-132">MDATP_SysExt.xml</span><span class="sxs-lookup"><span data-stu-id="fcdc1-132">MDATP_SysExt.xml</span></span> | <span data-ttu-id="fcdc1-133">S/O</span><span class="sxs-lookup"><span data-stu-id="fcdc1-133">N/A</span></span> |
| [<span data-ttu-id="fcdc1-134">Approuver l’extension du noyau pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fcdc1-134">Approve Kernel Extension for Microsoft Defender for Endpoint</span></span>](#download-installation-and-onboarding-packages) | <span data-ttu-id="fcdc1-135">MDATP_KExt.xml</span><span class="sxs-lookup"><span data-stu-id="fcdc1-135">MDATP_KExt.xml</span></span> | <span data-ttu-id="fcdc1-136">S/O</span><span class="sxs-lookup"><span data-stu-id="fcdc1-136">N/A</span></span> |
| [<span data-ttu-id="fcdc1-137">Accorder un accès disque complet à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fcdc1-137">Grant full disk access to Microsoft Defender for Endpoint</span></span>](#create-system-configuration-profiles-step-8) | <span data-ttu-id="fcdc1-138">MDATP_tcc_Catalina_or_newer.xml</span><span class="sxs-lookup"><span data-stu-id="fcdc1-138">MDATP_tcc_Catalina_or_newer.xml</span></span> | <span data-ttu-id="fcdc1-139">com.microsoft.wdav.tcc</span><span class="sxs-lookup"><span data-stu-id="fcdc1-139">com.microsoft.wdav.tcc</span></span> |
| [<span data-ttu-id="fcdc1-140">Stratégie d’extension réseau</span><span class="sxs-lookup"><span data-stu-id="fcdc1-140">Network Extension policy</span></span>](#create-system-configuration-profiles-step-9) | <span data-ttu-id="fcdc1-141">MDATP_NetExt.xml</span><span class="sxs-lookup"><span data-stu-id="fcdc1-141">MDATP_NetExt.xml</span></span> | <span data-ttu-id="fcdc1-142">S/O</span><span class="sxs-lookup"><span data-stu-id="fcdc1-142">N/A</span></span> |
| [<span data-ttu-id="fcdc1-143">Configurer la mise à jour automatique Microsoft (AutoUpdate)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-143">Configure Microsoft AutoUpdate (MAU)</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/mac-updates#intune) | <span data-ttu-id="fcdc1-144">MDATP_Microsoft_AutoUpdate.xml</span><span class="sxs-lookup"><span data-stu-id="fcdc1-144">MDATP_Microsoft_AutoUpdate.xml</span></span> | <span data-ttu-id="fcdc1-145">com.microsoft.autoupdate2</span><span class="sxs-lookup"><span data-stu-id="fcdc1-145">com.microsoft.autoupdate2</span></span> |
| [<span data-ttu-id="fcdc1-146">Paramètres de configuration de Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="fcdc1-146">Microsoft Defender for Endpoint configuration settings</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/mac-preferences#intune-profile-1)<br/><br/> <span data-ttu-id="fcdc1-147">**Remarque :** Si vous envisagez d’exécuter un antivirus tiers pour macOS, définissez sur `passiveMode` `true` .</span><span class="sxs-lookup"><span data-stu-id="fcdc1-147">**Note:** If you are planning to run a third-party AV for macOS, set `passiveMode` to `true`.</span></span> | <span data-ttu-id="fcdc1-148">MDATP_WDAV_and_exclusion_settings_Preferences.xml</span><span class="sxs-lookup"><span data-stu-id="fcdc1-148">MDATP_WDAV_and_exclusion_settings_Preferences.xml</span></span> | <span data-ttu-id="fcdc1-149">com.microsoft.wdav</span><span class="sxs-lookup"><span data-stu-id="fcdc1-149">com.microsoft.wdav</span></span> |
| [<span data-ttu-id="fcdc1-150">Configurer Microsoft Defender pour les notifications de point de terminaison et de mise à jour automatique MS (MAU)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-150">Configure Microsoft Defender for Endpoint and MS AutoUpdate (MAU) notifications</span></span>](#create-system-configuration-profiles-step-10) | <span data-ttu-id="fcdc1-151">MDATP_MDAV_Tray_and_AutoUpdate2.mobileconfig</span><span class="sxs-lookup"><span data-stu-id="fcdc1-151">MDATP_MDAV_Tray_and_AutoUpdate2.mobileconfig</span></span> | <span data-ttu-id="fcdc1-152">com.microsoft.autoupdate2 ou com.microsoft.wdav.tray</span><span class="sxs-lookup"><span data-stu-id="fcdc1-152">com.microsoft.autoupdate2 or com.microsoft.wdav.tray</span></span> |

## <a name="download-installation-and-onboarding-packages"></a><span data-ttu-id="fcdc1-153">Télécharger les packages d’installation et d’intégration</span><span class="sxs-lookup"><span data-stu-id="fcdc1-153">Download installation and onboarding packages</span></span>

<span data-ttu-id="fcdc1-154">Téléchargez les packages d’installation et d’intégration à partir du Centre de sécurité Microsoft Defender :</span><span class="sxs-lookup"><span data-stu-id="fcdc1-154">Download the installation and onboarding packages from Microsoft Defender Security Center:</span></span>

1. <span data-ttu-id="fcdc1-155">Dans le Centre de sécurité Microsoft Defender, go to **Settings**  >  **Device Management**  >  **Onboarding**.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-155">In Microsoft Defender Security Center, go to **Settings** > **Device Management** > **Onboarding**.</span></span>

2. <span data-ttu-id="fcdc1-156">Définissez le système d’exploitation sur **macOS** et la méthode de déploiement sur Gestion des appareils **mobiles /Microsoft Intune**.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-156">Set the operating system to **macOS** and the deployment method to **Mobile Device Management / Microsoft Intune**.</span></span>

    ![Capture d’écran des paramètres d’intégration](images/atp-mac-install.png)

3. <span data-ttu-id="fcdc1-158">Sélectionnez **Télécharger le package d’installation.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-158">Select **Download installation package**.</span></span> <span data-ttu-id="fcdc1-159">Enregistrez-le _sous wdav.pkg_ dans un répertoire local.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-159">Save it as _wdav.pkg_ to a local directory.</span></span>

4. <span data-ttu-id="fcdc1-160">Sélectionnez **Télécharger le package d’intégration.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-160">Select **Download onboarding package**.</span></span> <span data-ttu-id="fcdc1-161">Enregistrez-le _WindowsDefenderATPOnboardingPackage.zip_ dans le même répertoire.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-161">Save it as _WindowsDefenderATPOnboardingPackage.zip_ to the same directory.</span></span>

5. <span data-ttu-id="fcdc1-162">Téléchargez **IntuneAppUtil à** partir [https://docs.microsoft.com/intune/lob-apps-macos](https://docs.microsoft.com/intune/lob-apps-macos) de .</span><span class="sxs-lookup"><span data-stu-id="fcdc1-162">Download **IntuneAppUtil** from [https://docs.microsoft.com/intune/lob-apps-macos](https://docs.microsoft.com/intune/lob-apps-macos).</span></span>

6. <span data-ttu-id="fcdc1-163">À partir d’une invite de commandes, vérifiez que vous avez les trois fichiers.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-163">From a command prompt, verify that you have the three files.</span></span>
  

    ```bash
    ls -l
    ```

    ```Output
    total 721688
    -rw-r--r--  1 test  staff     269280 Mar 15 11:25 IntuneAppUtil
    -rw-r--r--  1 test  staff      11821 Mar 15 09:23 WindowsDefenderATPOnboardingPackage.zip
    -rw-r--r--  1 test  staff  354531845 Mar 13 08:57 wdav.pkg
    ```
7. <span data-ttu-id="fcdc1-164">Extrayer le contenu des fichiers .zip :</span><span class="sxs-lookup"><span data-stu-id="fcdc1-164">Extract the contents of the .zip files:</span></span>

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

8. <span data-ttu-id="fcdc1-165">Faites d’IntuneAppUtil un exécutable :</span><span class="sxs-lookup"><span data-stu-id="fcdc1-165">Make IntuneAppUtil an executable:</span></span>

    ```bash
    chmod +x IntuneAppUtil
    ```

9. <span data-ttu-id="fcdc1-166">Créez le package wdav.pkg.intunemac à partir de wdav.pkg :</span><span class="sxs-lookup"><span data-stu-id="fcdc1-166">Create the wdav.pkg.intunemac package from wdav.pkg:</span></span>

    ```bash
    ./IntuneAppUtil -c wdav.pkg -o . -i "com.microsoft.wdav" -n "1.0.0"
    ```
    ```Output
    Microsoft Intune Application Utility for Mac OS X
    Version: 1.0.0.0
    Copyright 2018 Microsoft Corporation

    Creating intunemac file for /Users/test/Downloads/wdav.pkg
    Composing the intunemac file output
    Output written to ./wdav.pkg.intunemac.

    IntuneAppUtil successfully processed "wdav.pkg",
    to deploy refer to the product documentation.
    ```

## <a name="client-device-setup"></a><span data-ttu-id="fcdc1-167">Configuration de l’appareil client</span><span class="sxs-lookup"><span data-stu-id="fcdc1-167">Client device setup</span></span>

<span data-ttu-id="fcdc1-168">Vous n’avez pas besoin d’une mise en service spéciale pour un appareil Mac au-delà d’une installation standard [du portail d’entreprise.](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-macos-cp)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-168">You do not need any special provisioning for a Mac device beyond a standard [Company Portal installation](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-macos-cp).</span></span>

1. <span data-ttu-id="fcdc1-169">Confirmez la gestion des appareils.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-169">Confirm device management.</span></span>

    ![Confirmer la capture d’écran de la gestion des appareils](./images/mdatp-3-confirmdevicemgmt.png)

    <span data-ttu-id="fcdc1-171">Sélectionnez **Ouvrir les préférences système,** recherchez **Profil** de gestion dans la liste, puis sélectionnez **Approuver...**. Votre profil de gestion s’affiche comme **vérifié**:</span><span class="sxs-lookup"><span data-stu-id="fcdc1-171">Select **Open System Preferences**, locate **Management Profile** on the list, and select **Approve...**. Your Management Profile would be displayed as **Verified**:</span></span>

    ![Capture d’écran du profil de gestion](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-4-managementprofile)

2. <span data-ttu-id="fcdc1-173">Sélectionnez **Continuer** et terminez l’inscription.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-173">Select **Continue** and complete the enrollment.</span></span>

   <span data-ttu-id="fcdc1-174">Vous pouvez maintenant inscrire davantage d’appareils.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-174">You may now enroll more devices.</span></span> <span data-ttu-id="fcdc1-175">Vous pouvez également les inscrire ultérieurement, une fois que vous avez terminé l’approvisionnement de la configuration système et des packages d’application.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-175">You can also enroll them later, after you have finished provisioning system configuration and application packages.</span></span>

3. <span data-ttu-id="fcdc1-176">Dans Intune, ouvrez **Gérer**  >  **tous les**  >  **appareils.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-176">In Intune, open **Manage** > **Devices** > **All devices**.</span></span> <span data-ttu-id="fcdc1-177">Ici, vous pouvez voir votre appareil parmi ceux répertoriés :</span><span class="sxs-lookup"><span data-stu-id="fcdc1-177">Here you can see your device among those listed:</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="fcdc1-178">![Capture d’écran Ajouter des appareils](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-5-alldevices)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-178">![Add Devices screenshot](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-5-alldevices)</span></span>

## <a name="approve-system-extensions"></a><span data-ttu-id="fcdc1-179">Approuver les extensions système</span><span class="sxs-lookup"><span data-stu-id="fcdc1-179">Approve System Extensions</span></span>

<span data-ttu-id="fcdc1-180">Pour approuver les extensions système :</span><span class="sxs-lookup"><span data-stu-id="fcdc1-180">To approve the system extensions:</span></span>

1. <span data-ttu-id="fcdc1-181">Dans Intune, ouvrez **Gérer la** configuration  >  **de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-181">In Intune, open **Manage** > **Device configuration**.</span></span> <span data-ttu-id="fcdc1-182">Sélectionnez **Gérer**  >  **les profils**  >  **créer un profil.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-182">Select **Manage** > **Profiles** > **Create Profile**.</span></span>

2. <span data-ttu-id="fcdc1-183">Choisissez un nom pour le profil.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-183">Choose a name for the profile.</span></span> <span data-ttu-id="fcdc1-184">Change **Platform=macOS** to **Profile type=Extensions**.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-184">Change **Platform=macOS** to **Profile type=Extensions**.</span></span> <span data-ttu-id="fcdc1-185">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-185">Select **Create**.</span></span>

3. <span data-ttu-id="fcdc1-186">Dans **l’onglet Éléments de** base, nommez ce nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-186">In the **Basics** tab, give a name to this new profile.</span></span>

4. <span data-ttu-id="fcdc1-187">Dans **l’onglet Paramètres de configuration,** ajoutez les entrées suivantes dans la section **Extensions système autorisées** :</span><span class="sxs-lookup"><span data-stu-id="fcdc1-187">In the **Configuration settings** tab, add the following entries in the **Allowed system extensions** section:</span></span>

    <span data-ttu-id="fcdc1-188">Identificateur d’ensemble</span><span class="sxs-lookup"><span data-stu-id="fcdc1-188">Bundle identifier</span></span>         | <span data-ttu-id="fcdc1-189">Identificateur d’équipe</span><span class="sxs-lookup"><span data-stu-id="fcdc1-189">Team identifier</span></span>
    --------------------------|----------------
    <span data-ttu-id="fcdc1-190">com.microsoft.wdav.epsext</span><span class="sxs-lookup"><span data-stu-id="fcdc1-190">com.microsoft.wdav.epsext</span></span> | <span data-ttu-id="fcdc1-191">UBF8T346G9</span><span class="sxs-lookup"><span data-stu-id="fcdc1-191">UBF8T346G9</span></span>
    <span data-ttu-id="fcdc1-192">com.microsoft.wdav.netext</span><span class="sxs-lookup"><span data-stu-id="fcdc1-192">com.microsoft.wdav.netext</span></span> | <span data-ttu-id="fcdc1-193">UBF8T346G9</span><span class="sxs-lookup"><span data-stu-id="fcdc1-193">UBF8T346G9</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="fcdc1-194">![Capture d’écran des paramètres d’extension dans les paramètres de configuration sous l’onglet Éléments de base](images/mac-system-extension-intune2.png)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-194">![Screenshot of the extension settings in Configuration settings on the Basics tab](images/mac-system-extension-intune2.png)</span></span>

5. <span data-ttu-id="fcdc1-195">Dans **l’onglet Affectations,** affectez ce profil à tous les **utilisateurs & tous les appareils.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-195">In the **Assignments** tab, assign this profile to **All Users & All devices**.</span></span>

6. <span data-ttu-id="fcdc1-196">Examinez et créez ce profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-196">Review and create this configuration profile.</span></span>

## <a name="create-system-configuration-profiles"></a><span data-ttu-id="fcdc1-197">Créer des profils de configuration système</span><span class="sxs-lookup"><span data-stu-id="fcdc1-197">Create System Configuration profiles</span></span>

1. <span data-ttu-id="fcdc1-198">Dans Intune, ouvrez **Gérer la** configuration  >  **de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-198">In Intune, open **Manage** > **Device configuration**.</span></span> <span data-ttu-id="fcdc1-199">Sélectionnez **Gérer**  >  **les profils**  >  **créer un profil.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-199">Select **Manage** > **Profiles** > **Create Profile**.</span></span>

2. <span data-ttu-id="fcdc1-200">Choisissez un nom pour le profil.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-200">Choose a name for the profile.</span></span> <span data-ttu-id="fcdc1-201">Change **Platform=macOS** to **Profile type=Custom**.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-201">Change **Platform=macOS** to **Profile type=Custom**.</span></span> <span data-ttu-id="fcdc1-202">Sélectionnez **Configurer**.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-202">Select **Configure**.</span></span>

3. <span data-ttu-id="fcdc1-203">Ouvrez le profil de configuration et téléchargez intune/kext.xml.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-203">Open the configuration profile and upload intune/kext.xml.</span></span> <span data-ttu-id="fcdc1-204">Ce fichier a été créé dans l’une des sections précédentes.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-204">This file was created in one of the preceding sections.</span></span>

4. <span data-ttu-id="fcdc1-205">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-205">Select **OK**.</span></span>

    ![Importer une configuration à partir d’un fichier pour le profil de configuration personnalisé](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-6-systemconfigurationprofiles)

5. <span data-ttu-id="fcdc1-207">Sélectionnez   >  **Gérer les affectations.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-207">Select **Manage** > **Assignments**.</span></span> <span data-ttu-id="fcdc1-208">Dans **l’onglet** Inclure, sélectionnez Affecter à tous **les utilisateurs & tous les appareils.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-208">In the **Include** tab, select **Assign to All Users & All devices**.</span></span>

6. <span data-ttu-id="fcdc1-209">Répétez les étapes 1 à 5 pour plus de profils.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-209">Repeat steps 1 through 5 for more profiles.</span></span>

7. <span data-ttu-id="fcdc1-210">Créez un autre profil, donnez-lui un nom et téléchargez le fichier intune/WindowsDefenderATPOnboarding.xml.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-210">Create another profile, give it a name, and upload the intune/WindowsDefenderATPOnboarding.xml file.</span></span>

8. <span data-ttu-id="fcdc1-211">Téléchargez **fulldisk.mobileconfig à partir** de notre référentiel [GitHub](https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/mobileconfig/profiles/fulldisk.mobileconfig) et enregistrez-le sous **tcc.xml**.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-211">Download **fulldisk.mobileconfig** from [our GitHub repository](https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/mobileconfig/profiles/fulldisk.mobileconfig) and save it as **tcc.xml**.</span></span> <span data-ttu-id="fcdc1-212">Créez un autre profil, nommez-le et téléchargez-le dans celui-ci.<a name="create-system-configuration-profiles-step-8" id = "create-system-configuration-profiles-step-8"></a></span><span class="sxs-lookup"><span data-stu-id="fcdc1-212">Create another profile, give it any name and upload this file to it.<a name="create-system-configuration-profiles-step-8" id = "create-system-configuration-profiles-step-8"></a></span></span>

   > [!CAUTION]
   > <span data-ttu-id="fcdc1-213">macOS 10.15 (Contrôle) contient de nouvelles améliorations en matière de sécurité et de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-213">macOS 10.15 (Catalina) contains new security and privacy enhancements.</span></span> <span data-ttu-id="fcdc1-214">À partir de cette version, par défaut, les applications ne peuvent pas accéder à certains emplacements sur le disque (par exemple, Documents, Téléchargements, Bureau, etc.) sans consentement explicite.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-214">Beginning with this version, by default, applications are not able to access certain locations on disk (such as Documents, Downloads, Desktop, etc.) without explicit consent.</span></span> <span data-ttu-id="fcdc1-215">En l’absence de ce consentement, Microsoft Defender pour le point de terminaison n’est pas en mesure de protéger entièrement votre appareil.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-215">In the absence of this consent, Microsoft Defender for Endpoint is not able to fully protect your device.</span></span>
   >
   > <span data-ttu-id="fcdc1-216">Ce profil de configuration accorde un accès disque total à Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-216">This configuration profile grants Full Disk Access to Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="fcdc1-217">Si vous avez précédemment configuré Microsoft Defender pour endpoint via Intune, nous vous recommandons de mettre à jour le déploiement avec ce profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-217">If you previously configured Microsoft Defender for Endpoint through Intune, we recommend you update the deployment with this configuration profile.</span></span>

9. <span data-ttu-id="fcdc1-218">Dans le cadre des fonctionnalités de détection et de réponse des points de terminaison, Microsoft Defender pour Endpoint pour Mac inspecte le trafic de socket et signale ces informations au portail centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-218">As part of the Endpoint Detection and Response capabilities, Microsoft Defender for Endpoint for Mac inspects socket traffic and reports this information to the Microsoft Defender Security Center portal.</span></span> <span data-ttu-id="fcdc1-219">La stratégie suivante permet à l’extension réseau d’effectuer cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-219">The following policy allows the network extension to perform this functionality.</span></span> <span data-ttu-id="fcdc1-220">Téléchargez **netfilter.mobileconfig** à partir de notre référentiel [GitHub,](https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/mobileconfig/profiles/netfilter.mobileconfig)enregistrez-le sous netext.xml et déployez-le en utilisant les mêmes étapes que dans les sections précédentes.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-220">Download **netfilter.mobileconfig** from [our GitHub repository](https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/mobileconfig/profiles/netfilter.mobileconfig), save it as netext.xml and deploy it using the same steps as in the previous sections.</span></span> <a name = "create-system-configuration-profiles-step-9" id = "create-system-configuration-profiles-step-9"></a>

10. <span data-ttu-id="fcdc1-221">Pour permettre à Microsoft Defender pour point de terminaison pour Mac et Microsoft Auto Update d’afficher des notifications dans l’interface utilisateur sur macOS 10.15 (Île), téléchargez-le à partir de notre référentiel GitHub et importez-le en tant que charge utile `notif.mobileconfig` personnalisée. [](https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/mobileconfig/profiles/notif.mobileconfig)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-221">To allow Microsoft Defender for Endpoint for Mac and Microsoft Auto Update to display notifications in UI on macOS 10.15 (Catalina), download `notif.mobileconfig` from [our GitHub repository](https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/mobileconfig/profiles/notif.mobileconfig) and import it as a custom payload.</span></span> <a name = "create-system-configuration-profiles-step-10" id = "create-system-configuration-profiles-step-10"></a>

11. <span data-ttu-id="fcdc1-222">Sélectionnez **Gérer > affectations.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-222">Select **Manage > Assignments**.</span></span>  <span data-ttu-id="fcdc1-223">Dans **l’onglet** Inclure, sélectionnez Affecter à tous **les utilisateurs & tous les appareils.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-223">In the **Include** tab, select **Assign to All Users & All devices**.</span></span>

<span data-ttu-id="fcdc1-224">Une fois que les modifications Intune sont propagées aux appareils inscrits, vous pouvez les voir répertoriées sous État de  >  **l’appareil de surveillance**:</span><span class="sxs-lookup"><span data-stu-id="fcdc1-224">Once the Intune changes are propagated to the enrolled devices, you can see them listed under **Monitor** > **Device status**:</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="fcdc1-225">![Affichage de l’état de l’appareil dans le moniteur](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-7-devicestatusblade.png)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-225">![View of Device Status in Monitor](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-7-devicestatusblade.png)</span></span>

## <a name="publish-application"></a><span data-ttu-id="fcdc1-226">Publier l'application</span><span class="sxs-lookup"><span data-stu-id="fcdc1-226">Publish application</span></span>

1. <span data-ttu-id="fcdc1-227">Dans Intune, ouvrez le lame **Gérer > applications clientes.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-227">In Intune, open the **Manage > Client apps** blade.</span></span> <span data-ttu-id="fcdc1-228">Select **Apps > Add**.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-228">Select **Apps > Add**.</span></span>

2. <span data-ttu-id="fcdc1-229">Select **App type=Other/Line-of-business app**.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-229">Select **App type=Other/Line-of-business app**.</span></span>

3. <span data-ttu-id="fcdc1-230">Select **file=wdav.pkg.intunemac**.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-230">Select **file=wdav.pkg.intunemac**.</span></span> <span data-ttu-id="fcdc1-231">Sélectionnez **OK** pour télécharger.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-231">Select **OK** to upload.</span></span>

4. <span data-ttu-id="fcdc1-232">Sélectionnez **Configurer et** ajouter les informations requises.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-232">Select **Configure** and add the required information.</span></span>

5. <span data-ttu-id="fcdc1-233">Utilisez **macOS High Sierra 10.14 comme** système d’exploitation minimal.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-233">Use **macOS High Sierra 10.14** as the minimum OS.</span></span>

6. <span data-ttu-id="fcdc1-234">Définissez *Ignorer la version de l’application* sur **Oui.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-234">Set *Ignore app version* to **Yes**.</span></span> <span data-ttu-id="fcdc1-235">D’autres paramètres peuvent être n’importe quelle valeur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-235">Other settings can be any arbitrary value.</span></span>

    > [!CAUTION]
    > <span data-ttu-id="fcdc1-236">La définition *de la version Ignorer la version* de l’application sur Non a une incidence sur la capacité de l’application à recevoir des mises à jour via La mise à jour automatique Microsoft. </span><span class="sxs-lookup"><span data-stu-id="fcdc1-236">Setting *Ignore app version* to **No** impacts the ability of the application to receive updates through Microsoft AutoUpdate.</span></span> <span data-ttu-id="fcdc1-237">Pour [plus d’informations](mac-updates.md) sur la façon dont le produit est mis à jour, voir Déployer les mises à jour de Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-237">See [Deploy updates for Microsoft Defender for Endpoint for Mac](mac-updates.md) for additional information about how the product is updated.</span></span>
    >
    > <span data-ttu-id="fcdc1-238">Si la version téléchargée par Intune est inférieure à la version sur l’appareil, la version inférieure est installée, ce qui a pour effet de dégrader Microsoft Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-238">If the version uploaded by Intune is lower than the version on the device, then the lower version will be installed, effectively downgrading Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="fcdc1-239">Cela peut entraîner le non-fonctionnement d’une application.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-239">This could result in a non-functioning application.</span></span> <span data-ttu-id="fcdc1-240">Pour [plus d’informations](mac-updates.md) sur la façon dont le produit est mis à jour, voir Déployer les mises à jour de Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-240">See [Deploy updates for Microsoft Defender for Endpoint for Mac](mac-updates.md) for additional information about how the product is updated.</span></span> <span data-ttu-id="fcdc1-241">Si vous avez déployé Microsoft Defender pour le point de terminaison avec ignorer *la version de* l’application définie sur **Non,** changez-la en **Oui.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-241">If you deployed Microsoft Defender for Endpoint with *Ignore app version* set to **No**, please change it to **Yes**.</span></span> <span data-ttu-id="fcdc1-242">Si Microsoft Defender pour le point de terminaison ne peut toujours pas être installé sur un appareil client, désinstallez Microsoft Defender pour le point de terminaison et appuyez sur la stratégie mise à jour.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-242">If Microsoft Defender for Endpoint still cannot be installed on a client device, then uninstall Microsoft Defender for Endpoint and push the updated policy.</span></span>
     
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="fcdc1-243">![Affichage des informations d’application dans l’ajout d’application](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-8-intuneappinfo)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-243">![Display of App information in App add](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-8-intuneappinfo)</span></span>

7. <span data-ttu-id="fcdc1-244">Sélectionnez **OK** et **Ajoutez**.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-244">Select **OK** and **Add**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="fcdc1-245">![État de l’appareil affiché dans la fenêtre Notifications](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-9-intunepkginfo)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-245">![Device status shown in Notifications window](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-9-intunepkginfo)</span></span>

8. <span data-ttu-id="fcdc1-246">Le chargement du package peut prendre quelques instants.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-246">It may take a few moments to upload the package.</span></span> <span data-ttu-id="fcdc1-247">Une fois que vous avez terminé, sélectionnez le package dans la liste et allez à **Affectations** et **ajouter un groupe.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-247">After it's done, select the package from the list and go to **Assignments** and **Add group**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="fcdc1-248">![Capture d’écran des applications clientes](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-10-clientapps)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-248">![Client apps screenshot](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-10-clientapps)</span></span>

9. <span data-ttu-id="fcdc1-249">Change **Assignment type** to **Required**.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-249">Change **Assignment type** to **Required**.</span></span>

10. <span data-ttu-id="fcdc1-250">Sélectionnez **Groupes inclus.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-250">Select **Included Groups**.</span></span> <span data-ttu-id="fcdc1-251">Sélectionnez **Rendre cette application requise pour tous les appareils= Oui**.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-251">Select **Make this app required for all devices=Yes**.</span></span> <span data-ttu-id="fcdc1-252">Sélectionnez **Sélectionner un groupe à inclure et** ajoutez un groupe qui contient les utilisateurs que vous souhaitez cibler.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-252">Select **Select group to include** and add a group that contains the users you want to target.</span></span> <span data-ttu-id="fcdc1-253">Sélectionnez **OK** et **Enregistrez.**</span><span class="sxs-lookup"><span data-stu-id="fcdc1-253">Select **OK** and **Save**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="fcdc1-254">![Capture d’écran des informations sur les affectations Intune](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-11-assignments)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-254">![Intune assignments info screenshot](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-11-assignments)</span></span>

11. <span data-ttu-id="fcdc1-255">Après un certain temps, l’application sera publiée sur tous les appareils inscrits.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-255">After some time the application will be published to all enrolled devices.</span></span> <span data-ttu-id="fcdc1-256">Vous pouvez le voir dans surveiller l’appareil,  >  sous État **de l’installation de l’appareil**:</span><span class="sxs-lookup"><span data-stu-id="fcdc1-256">You can see it listed in **Monitor** > **Device**, under **Device install status**:</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="fcdc1-257">![Capture d’écran de l’état de l’appareil Intune](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-12-deviceinstall)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-257">![Intune device status screenshot](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-12-deviceinstall)</span></span>

## <a name="verify-client-device-state"></a><span data-ttu-id="fcdc1-258">Vérifier l’état de l’appareil client</span><span class="sxs-lookup"><span data-stu-id="fcdc1-258">Verify client device state</span></span>

1. <span data-ttu-id="fcdc1-259">Une fois les profils de configuration déployés sur vos appareils, ouvrez les **profils** de préférences  >  **système** sur votre appareil Mac.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-259">After the configuration profiles are deployed to your devices, open **System Preferences** > **Profiles** on your Mac device.</span></span>

    <span data-ttu-id="fcdc1-260">![Capture d’écran des préférences système](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-13-systempreferences)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-260">![System Preferences screenshot](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-13-systempreferences)</span></span><br/>
    <span data-ttu-id="fcdc1-261">![Capture d’écran des profils de préférences système](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-14-systempreferencesprofiles)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-261">![System Preferences Profiles screenshot](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-14-systempreferencesprofiles)</span></span>

2. <span data-ttu-id="fcdc1-262">Vérifiez que les profils de configuration suivants sont présents et installés.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-262">Verify that the following configuration profiles are present and installed.</span></span> <span data-ttu-id="fcdc1-263">Le **profil de** gestion doit être le profil système Intune.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-263">The **Management Profile** should be the Intune system profile.</span></span> <span data-ttu-id="fcdc1-264">_Wdav-config_ et _wdav-kext_ sont des profils de configuration système qui ont été ajoutés dans Intune : Capture d’écran ![ des profils](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-15-managementprofileconfig)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-264">_Wdav-config_ and _wdav-kext_ are system configuration profiles that were added in Intune: ![Profiles screenshot](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-15-managementprofileconfig)</span></span>

3. <span data-ttu-id="fcdc1-265">Vous devez également voir l’icône Microsoft Defender dans le coin supérieur droit :</span><span class="sxs-lookup"><span data-stu-id="fcdc1-265">You should also see the Microsoft Defender icon in the top-right corner:</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="fcdc1-266">![Icône Microsoft Defender dans la capture d’écran de la barre d’état](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-icon-bar)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-266">![Microsoft Defender icon in status bar screenshot](/windows/security/threat-protection/microsoft-defender-antivirus/images/mdatp-icon-bar)</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="fcdc1-267">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="fcdc1-267">Troubleshooting</span></span>

<span data-ttu-id="fcdc1-268">Problème : aucune licence trouvée</span><span class="sxs-lookup"><span data-stu-id="fcdc1-268">Issue: No license found</span></span>

<span data-ttu-id="fcdc1-269">Solution : suivez les étapes ci-dessus pour créer un profil d’appareil à l’aide WindowsDefenderATPOnboarding.xml</span><span class="sxs-lookup"><span data-stu-id="fcdc1-269">Solution: Follow the steps above to create a device profile using WindowsDefenderATPOnboarding.xml</span></span>

## <a name="logging-installation-issues"></a><span data-ttu-id="fcdc1-270">Journalisation des problèmes d’installation</span><span class="sxs-lookup"><span data-stu-id="fcdc1-270">Logging installation issues</span></span>

<span data-ttu-id="fcdc1-271">Pour plus d’informations sur la recherche du journal généré automatiquement par le programme d’installation en cas d’erreur, voir [Problèmes d’installation de journalisation.](mac-resources.md#logging-installation-issues)</span><span class="sxs-lookup"><span data-stu-id="fcdc1-271">For more information on how to find the automatically generated log that is created by the installer when an error occurs, see [Logging installation issues](mac-resources.md#logging-installation-issues).</span></span>

## <a name="uninstallation"></a><span data-ttu-id="fcdc1-272">Désinstallation</span><span class="sxs-lookup"><span data-stu-id="fcdc1-272">Uninstallation</span></span>

<span data-ttu-id="fcdc1-273">Voir [Désinstallation](mac-resources.md#uninstalling) pour plus d’informations sur la suppression de Microsoft Defender pour Endpoint pour Mac des appareils clients.</span><span class="sxs-lookup"><span data-stu-id="fcdc1-273">See [Uninstalling](mac-resources.md#uninstalling) for details on how to remove Microsoft Defender for Endpoint for Mac from client devices.</span></span>
