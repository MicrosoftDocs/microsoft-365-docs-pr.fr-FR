---
title: Déploiement manuel de Microsoft Defender pour point de terminaison pour macOS
description: Installez Microsoft Defender pour point de terminaison pour macOS manuellement, à partir de la ligne de commande.
keywords: microsoft, defender, atp, mac, installation, déployer, désinstallation, intune, jamf, macos, magasin, mojave, high sierra
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
ms.openlocfilehash: a9e75441a8c4a336e8c657d27330c118fcac4788
ms.sourcegitcommit: 7b8104015a76e02bc215e1cf08069979c70650ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/31/2021
ms.locfileid: "51476304"
---
# <a name="manual-deployment-for-microsoft-defender-for-endpoint-for-macos"></a><span data-ttu-id="6a0cd-104">Déploiement manuel de Microsoft Defender pour point de terminaison pour macOS</span><span class="sxs-lookup"><span data-stu-id="6a0cd-104">Manual deployment for Microsoft Defender for Endpoint for macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="6a0cd-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6a0cd-105">**Applies to:**</span></span>
- [<span data-ttu-id="6a0cd-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6a0cd-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="6a0cd-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6a0cd-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="6a0cd-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="6a0cd-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="6a0cd-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="6a0cd-110">Cette rubrique décrit comment déployer Microsoft Defender pour endpoint pour macOS manuellement.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-110">This topic describes how to deploy Microsoft Defender for Endpoint for macOS manually.</span></span> <span data-ttu-id="6a0cd-111">Un déploiement réussi nécessite la réalisation de toutes les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="6a0cd-111">A successful deployment requires the completion of all of the following steps:</span></span>
- [<span data-ttu-id="6a0cd-112">Télécharger les packages d’installation et d’intégration</span><span class="sxs-lookup"><span data-stu-id="6a0cd-112">Download installation and onboarding packages</span></span>](#download-installation-and-onboarding-packages)
- [<span data-ttu-id="6a0cd-113">Installation d’applications (macOS 10.15 et versions antérieures)</span><span class="sxs-lookup"><span data-stu-id="6a0cd-113">Application installation (macOS 10.15 and older versions)</span></span>](#application-installation-macos-1015-and-older-versions)
- [<span data-ttu-id="6a0cd-114">Installation d’applications (macOS 11 et versions plus récentes)</span><span class="sxs-lookup"><span data-stu-id="6a0cd-114">Application installation (macOS 11 and newer versions)</span></span>](#application-installation-macos-11-and-newer-versions)
- [<span data-ttu-id="6a0cd-115">Configuration du client</span><span class="sxs-lookup"><span data-stu-id="6a0cd-115">Client configuration</span></span>](#client-configuration)

## <a name="prerequisites-and-system-requirements"></a><span data-ttu-id="6a0cd-116">Conditions préalables et système requis</span><span class="sxs-lookup"><span data-stu-id="6a0cd-116">Prerequisites and system requirements</span></span>

<span data-ttu-id="6a0cd-117">Avant de commencer, consultez la page principale de Microsoft Defender pour point de terminaison [pour macOS](microsoft-defender-endpoint-mac.md) pour obtenir une description des conditions préalables et de la requise pour la version logicielle actuelle.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-117">Before you get started, see [the main Microsoft Defender for Endpoint for macOS page](microsoft-defender-endpoint-mac.md) for a description of prerequisites and system requirements for the current software version.</span></span>

## <a name="download-installation-and-onboarding-packages"></a><span data-ttu-id="6a0cd-118">Télécharger les packages d’installation et d’intégration</span><span class="sxs-lookup"><span data-stu-id="6a0cd-118">Download installation and onboarding packages</span></span>

<span data-ttu-id="6a0cd-119">Téléchargez les packages d’installation et d’intégration à partir du Centre de sécurité Microsoft Defender :</span><span class="sxs-lookup"><span data-stu-id="6a0cd-119">Download the installation and onboarding packages from Microsoft Defender Security Center:</span></span>

1. <span data-ttu-id="6a0cd-120">Dans le Centre de sécurité Microsoft Defender, go to **Settings > Device Management > Onboarding**.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-120">In Microsoft Defender Security Center, go to **Settings > Device Management > Onboarding**.</span></span>
2. <span data-ttu-id="6a0cd-121">Dans la section 1 de la page, définissez le système d’exploitation sur **macOS** et la méthode de déploiement sur **le script local.**</span><span class="sxs-lookup"><span data-stu-id="6a0cd-121">In Section 1 of the page, set operating system to **macOS** and Deployment method to **Local script**.</span></span>
3. <span data-ttu-id="6a0cd-122">Dans la section 2 de la page, sélectionnez **Télécharger le package d’installation.**</span><span class="sxs-lookup"><span data-stu-id="6a0cd-122">In Section 2 of the page, select **Download installation package**.</span></span> <span data-ttu-id="6a0cd-123">Enregistrez-le sous wdav.pkg dans un répertoire local.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-123">Save it as wdav.pkg to a local directory.</span></span>
4. <span data-ttu-id="6a0cd-124">Dans la section 2 de la page, **sélectionnez Télécharger le package d’intégration.**</span><span class="sxs-lookup"><span data-stu-id="6a0cd-124">In Section 2 of the page, select **Download onboarding package**.</span></span> <span data-ttu-id="6a0cd-125">Enregistrez-le WindowsDefenderATPOnboardingPackage.zip dans le même répertoire.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-125">Save it as WindowsDefenderATPOnboardingPackage.zip to the same directory.</span></span>

    ![Capture d’écran du Centre de sécurité Microsoft Defender](images/atp-portal-onboarding-page.png)

5. <span data-ttu-id="6a0cd-127">À partir d’une invite de commandes, vérifiez que vous avez les deux fichiers.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-127">From a command prompt, verify that you have the two files.</span></span>
    
## <a name="application-installation-macos-1015-and-older-versions"></a><span data-ttu-id="6a0cd-128">Installation d’applications (macOS 10.15 et versions antérieures)</span><span class="sxs-lookup"><span data-stu-id="6a0cd-128">Application installation (macOS 10.15 and older versions)</span></span>

<span data-ttu-id="6a0cd-129">Pour effectuer ce processus, vous devez avoir des privilèges d’administrateur sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-129">To complete this process, you must have admin privileges on the device.</span></span>

1. <span data-ttu-id="6a0cd-130">Accédez au wdav.pkg téléchargé dans Finder et ouvrez-le.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-130">Navigate to the downloaded wdav.pkg in Finder and open it.</span></span>

    ![Capture d’écran de l’installation de l’application1](images/mdatp-28-appinstall.png)

2. <span data-ttu-id="6a0cd-132">Sélectionnez **Continuer,** acceptez les termes du contrat de licence, puis entrez le mot de passe lorsque vous y invitez.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-132">Select **Continue**, agree with the License terms, and enter the password when prompted.</span></span>

    ![Installation de l’application capture d’écran2](images/mdatp-29-appinstalllogin.png)

   > [!IMPORTANT]
   > <span data-ttu-id="6a0cd-134">Vous serez invité à autoriser l’installation d’un pilote microsoft (« Extension système bloquée » ou « L’installation est en attente » ou les deux.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-134">You will be prompted to allow a driver from Microsoft to be installed (either "System Extension Blocked" or "Installation is on hold" or both.</span></span> <span data-ttu-id="6a0cd-135">Le pilote doit être autorisé à être installé.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-135">The driver must be allowed to be installed.</span></span>

   ![Installation de l’application screenshot3](images/mdatp-30-systemextension.png)

3. <span data-ttu-id="6a0cd-137">Sélectionnez **Ouvrir les préférences de sécurité** ou Ouvrir les préférences système > sécurité & **confidentialité.**</span><span class="sxs-lookup"><span data-stu-id="6a0cd-137">Select **Open Security Preferences** or **Open System Preferences > Security & Privacy**.</span></span> <span data-ttu-id="6a0cd-138">Sélectionnez **Autoriser**:</span><span class="sxs-lookup"><span data-stu-id="6a0cd-138">Select **Allow**:</span></span>

    ![Capture d’écran de la fenêtre Sécurité et confidentialité](images/mdatp-31-securityprivacysettings.png)

   <span data-ttu-id="6a0cd-140">L’installation se poursuit.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-140">The installation proceeds.</span></span>

   > [!CAUTION]
   > <span data-ttu-id="6a0cd-141">Si vous ne sélectionnez pas **Autoriser,** l’installation se poursuit au bout de 5 minutes.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-141">If you don't select **Allow**, the installation will proceed after 5 minutes.</span></span> <span data-ttu-id="6a0cd-142">Microsoft Defender pour le point de terminaison sera chargé, mais certaines fonctionnalités, telles que la protection en temps réel, seront désactivées.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-142">Microsoft Defender for Endpoint will be loaded, but some features, such as real-time protection, will be disabled.</span></span> <span data-ttu-id="6a0cd-143">Pour [plus d’informations](mac-support-kext.md) sur la résolution de ce problème, voir Résoudre les problèmes d’extension du noyau.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-143">See [Troubleshoot kernel extension issues](mac-support-kext.md) for information on how to resolve this.</span></span>

> [!NOTE]
> <span data-ttu-id="6a0cd-144">MacOS peut demander à redémarrer l’appareil lors de la première installation de Microsoft Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-144">macOS may request to reboot the device upon the first installation of Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="6a0cd-145">La protection en temps réel n’est pas disponible tant que l’appareil n’est pas redémarrage.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-145">Real-time protection will not be available until the device is rebooted.</span></span>

## <a name="application-installation-macos-11-and-newer-versions"></a><span data-ttu-id="6a0cd-146">Installation d’applications (macOS 11 et versions plus récentes)</span><span class="sxs-lookup"><span data-stu-id="6a0cd-146">Application installation (macOS 11 and newer versions)</span></span>

<span data-ttu-id="6a0cd-147">Pour effectuer ce processus, vous devez avoir des privilèges d’administrateur sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-147">To complete this process, you must have admin privileges on the device.</span></span>

1. <span data-ttu-id="6a0cd-148">Accédez au wdav.pkg téléchargé dans Finder et ouvrez-le.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-148">Navigate to the downloaded wdav.pkg in Finder and open it.</span></span>

    ![Installation de l’application screenshot4](images/big-sur-install-1.png)

2. <span data-ttu-id="6a0cd-150">Sélectionnez **Continuer,** acceptez les termes du contrat de licence, puis entrez le mot de passe lorsque vous y invitez.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-150">Select **Continue**, agree with the License terms, and enter the password when prompted.</span></span>

3. <span data-ttu-id="6a0cd-151">À la fin du processus d’installation, vous serez promu pour approuver les extensions système utilisées par le produit.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-151">At the end of the installation process, you'll be promoted to approve the system extensions used by the product.</span></span> <span data-ttu-id="6a0cd-152">Sélectionnez **Ouvrir les préférences de sécurité.**</span><span class="sxs-lookup"><span data-stu-id="6a0cd-152">Select **Open Security Preferences**.</span></span>

    ![Approbation des extensions système](images/big-sur-install-2.png)

4. <span data-ttu-id="6a0cd-154">Dans la **fenêtre Sécurité & confidentialité,** sélectionnez **Autoriser.**</span><span class="sxs-lookup"><span data-stu-id="6a0cd-154">From the **Security & Privacy** window, select **Allow**.</span></span>

    ![Préférences de sécurité des extensions système1](images/big-sur-install-3.png)

5. <span data-ttu-id="6a0cd-156">Répétez les étapes 3 & 4 pour toutes les extensions système distribuées avec Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-156">Repeat steps 3 & 4 for all system extensions distributed with Microsoft Defender for Endpoint for Mac.</span></span>

6. <span data-ttu-id="6a0cd-157">Dans le cadre des fonctionnalités de détection et de réponse des points de terminaison, Microsoft Defender pour Endpoint pour Mac inspecte le trafic de socket et signale ces informations au portail centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-157">As part of the Endpoint Detection and Response capabilities, Microsoft Defender for Endpoint for Mac inspects socket traffic and reports this information to the Microsoft Defender Security Center portal.</span></span> <span data-ttu-id="6a0cd-158">Lorsque vous avez été invité à accorder à Microsoft Defender pour les autorisations de point de terminaison pour filtrer le trafic réseau, sélectionnez **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-158">When prompted to grant Microsoft Defender for Endpoint permissions to filter network traffic, select **Allow**.</span></span>

    ![Préférences de sécurité des extensions système2](images/big-sur-install-4.png)

7. <span data-ttu-id="6a0cd-160">Ouvrez La sécurité **des** préférences système & confidentialité et accédez à l’onglet Confidentialité. Accordez l’autorisation d’accès disque total à Microsoft Defender  >   **ATP** et Microsoft **Defender ATP Endpoint Security Extension**.  </span><span class="sxs-lookup"><span data-stu-id="6a0cd-160">Open **System Preferences** > **Security & Privacy** and navigate to the **Privacy** tab. Grant **Full Disk Access** permission to **Microsoft Defender ATP** and **Microsoft Defender ATP Endpoint Security Extension**.</span></span>

    ![Accès disque total](images/big-sur-install-5.png)

## <a name="client-configuration"></a><span data-ttu-id="6a0cd-162">Configuration du client</span><span class="sxs-lookup"><span data-stu-id="6a0cd-162">Client configuration</span></span>

1. <span data-ttu-id="6a0cd-163">Copiez wdav.pkg et MicrosoftDefenderATPOnboardingMacOs.py sur l’appareil où vous déployez Microsoft Defender pour endpoint pour macOS.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-163">Copy wdav.pkg and MicrosoftDefenderATPOnboardingMacOs.py to the device where you deploy Microsoft Defender for Endpoint for macOS.</span></span>

    <span data-ttu-id="6a0cd-164">L’appareil client n’est pas associé à org_id.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-164">The client device isn't associated with org_id.</span></span> <span data-ttu-id="6a0cd-165">Notez que *l’org_id* est vide.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-165">Note that the *org_id* attribute is blank.</span></span>

    ```bash
    mdatp health --field org_id
    ```

2. <span data-ttu-id="6a0cd-166">Exécutez le script Python pour installer le fichier de configuration :</span><span class="sxs-lookup"><span data-stu-id="6a0cd-166">Run the Python script to install the configuration file:</span></span>

    ```bash
    /usr/bin/python MicrosoftDefenderATPOnboardingMacOs.py
    ```

3. <span data-ttu-id="6a0cd-167">Vérifiez que l’appareil est désormais associé à votre organisation et signale un ID d’organisation valide :</span><span class="sxs-lookup"><span data-stu-id="6a0cd-167">Verify that the device is now associated with your organization and reports a valid org ID:</span></span>

    ```bash
    mdatp health --field org_id
    ```

    <span data-ttu-id="6a0cd-168">Après l’installation, vous verrez l’icône Microsoft Defender dans la barre d’état macOS dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-168">After installation, you'll see the Microsoft Defender icon in the macOS status bar in the top-right corner.</span></span>
    
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a0cd-169">![Icône Microsoft Defender dans la capture d’écran de la barre d’état](images/mdatp-icon-bar.png)</span><span class="sxs-lookup"><span data-stu-id="6a0cd-169">![Microsoft Defender icon in status bar screenshot](images/mdatp-icon-bar.png)</span></span>


## <a name="how-to-allow-full-disk-access"></a><span data-ttu-id="6a0cd-170">Comment autoriser l’accès disque total</span><span class="sxs-lookup"><span data-stu-id="6a0cd-170">How to Allow Full Disk Access</span></span>

> [!CAUTION]
> <span data-ttu-id="6a0cd-171">macOS 10.15 (Contrôle) contient de nouvelles améliorations en matière de sécurité et de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-171">macOS 10.15 (Catalina) contains new security and privacy enhancements.</span></span> <span data-ttu-id="6a0cd-172">À partir de cette version, par défaut, les applications ne peuvent pas accéder à certains emplacements sur le disque (par exemple, Documents, Téléchargements, Bureau, etc.) sans consentement explicite.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-172">Beginning with this version, by default, applications are not able to access certain locations on disk (such as Documents, Downloads, Desktop, etc.) without explicit consent.</span></span> <span data-ttu-id="6a0cd-173">En l’absence de ce consentement, Microsoft Defender pour le point de terminaison n’est pas en mesure de protéger entièrement votre appareil.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-173">In the absence of this consent, Microsoft Defender for Endpoint is not able to fully protect your device.</span></span>

1. <span data-ttu-id="6a0cd-174">Pour accorder le consentement, **ouvrez La** sécurité des préférences système  >  **&**  >  **confidentialité** confidentialité accès disque  >  **total**.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-174">To grant consent, open **System Preferences** > **Security & Privacy** > **Privacy** > **Full Disk Access**.</span></span> <span data-ttu-id="6a0cd-175">Cliquez sur l’icône de verrouillage pour apporter des modifications (en bas de la boîte de dialogue).</span><span class="sxs-lookup"><span data-stu-id="6a0cd-175">Click the lock icon to make changes (bottom of the dialog box).</span></span> <span data-ttu-id="6a0cd-176">Sélectionnez Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-176">Select Microsoft Defender for Endpoint.</span></span>

2. <span data-ttu-id="6a0cd-177">Exécutez un test de détection antivirus pour vérifier que l’appareil est correctement intégré et signaler au service.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-177">Run an AV detection test to verify that the device is properly onboarded and reporting to the service.</span></span> <span data-ttu-id="6a0cd-178">Effectuez les étapes suivantes sur l’appareil nouvellement intégré :</span><span class="sxs-lookup"><span data-stu-id="6a0cd-178">Perform the following steps on the newly onboarded device:</span></span>

    1. <span data-ttu-id="6a0cd-179">Assurez-vous que la protection en temps réel est activée (notée par un résultat de 1 à partir de l’exécution de la commande suivante) :</span><span class="sxs-lookup"><span data-stu-id="6a0cd-179">Ensure that real-time protection is enabled (denoted by a result of 1 from running the following command):</span></span>

        ```bash
        mdatp health --field real_time_protection_enabled
        ```

    1. <span data-ttu-id="6a0cd-180">Ouvrez une fenêtre Terminal.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-180">Open a Terminal window.</span></span> <span data-ttu-id="6a0cd-181">Copiez et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="6a0cd-181">Copy and execute the following command:</span></span>

        ```bash
        curl -o ~/Downloads/eicar.com.txt https://www.eicar.org/download/eicar.com.txt
        ```

    1. <span data-ttu-id="6a0cd-182">Le fichier doit avoir été mis en quarantaine par Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-182">The file should have been quarantined by Defender for Endpoint for Mac.</span></span> <span data-ttu-id="6a0cd-183">Utilisez la commande suivante pour lister toutes les menaces détectées :</span><span class="sxs-lookup"><span data-stu-id="6a0cd-183">Use the following command to list all the detected threats:</span></span>

        ```bash
        mdatp threat list
        ```

3. <span data-ttu-id="6a0cd-184">Exécutez un test de détection EDR pour vérifier que l’appareil est correctement intégré et signaler au service.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-184">Run an EDR detection test to verify that the device is properly onboarded and reporting to the service.</span></span> <span data-ttu-id="6a0cd-185">Effectuez les étapes suivantes sur l’appareil nouvellement intégré :</span><span class="sxs-lookup"><span data-stu-id="6a0cd-185">Perform the following steps on the newly onboarded device:</span></span>

   1. <span data-ttu-id="6a0cd-186">Dans votre navigateur, tel que Microsoft Edge pour Mac ou Safari.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-186">In your browser such as Microsoft Edge for Mac or Safari.</span></span>

   1. <span data-ttu-id="6a0cd-187">Téléchargez les fichiers MacOS MDATP DIY.zip https://aka.ms/mdatpmacosdiy et extrayez.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-187">Download MDATP MacOS DIY.zip from https://aka.ms/mdatpmacosdiy and extract.</span></span>

      <span data-ttu-id="6a0cd-188">Vous pouvez être invité à :</span><span class="sxs-lookup"><span data-stu-id="6a0cd-188">You may be prompted:</span></span>

      > <span data-ttu-id="6a0cd-189">Voulez-vous autoriser les téléchargements sur « mdatpclientanalyzer.blob.core.windows.net » ?</span><span class="sxs-lookup"><span data-stu-id="6a0cd-189">Do you want to allow downloads on "mdatpclientanalyzer.blob.core.windows.net"?</span></span><br/>
      > <span data-ttu-id="6a0cd-190">Vous pouvez modifier les sites web qui peuvent télécharger des fichiers dans Préférences de sites Web.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-190">You can change which websites can download files in Websites Preferences.</span></span>

4. <span data-ttu-id="6a0cd-191">Cliquez sur **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-191">Click **Allow**.</span></span>

5. <span data-ttu-id="6a0cd-192">Open **Downloads**.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-192">Open **Downloads**.</span></span>

6. <span data-ttu-id="6a0cd-193">Vous devriez voir **MDATP MacOS 2013.**</span><span class="sxs-lookup"><span data-stu-id="6a0cd-193">You should see **MDATP MacOS DIY**.</span></span>

   > [!TIP]
   > <span data-ttu-id="6a0cd-194">Si vous double-cliquez, vous recevez le message suivant :</span><span class="sxs-lookup"><span data-stu-id="6a0cd-194">If you double-click, you will get the following message:</span></span>
   > 
   > > <span data-ttu-id="6a0cd-195">**« MDATP MacOS VERIFIE » ne peut pas être ouvert, car le développeur ne peut pas être vérifié.**</span><span class="sxs-lookup"><span data-stu-id="6a0cd-195">**"MDATP MacOS DIY" cannot be opened because the developer cannot be verifier.**</span></span><br/>
   > > <span data-ttu-id="6a0cd-196">MacOS ne peut pas vérifier que cette application est exempt de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-196">macOS cannot verify that this app is free from malware.</span></span><br/>
   > > <span data-ttu-id="6a0cd-197">**\[ Déplacer vers \] annuler la corbeille** **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="6a0cd-197">**\[Move to Trash\]** **\[Cancel\]**</span></span> 
  
7. <span data-ttu-id="6a0cd-198">Cliquez sur **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-198">Click **Cancel**.</span></span>

8. <span data-ttu-id="6a0cd-199">Cliquez avec le bouton **droit de la souris sur MDATP MacOS(2013),** puis cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-199">Right-click **MDATP MacOS DIY**, and then click **Open**.</span></span> 

    <span data-ttu-id="6a0cd-200">Le système doit afficher le message suivant :</span><span class="sxs-lookup"><span data-stu-id="6a0cd-200">The system should display the following message:</span></span>

    > <span data-ttu-id="6a0cd-201">**macOS ne peut pas vérifier le développeur de **MDATP MacOSMUT .** Voulez-vous vraiment l’ouvrir ?**</span><span class="sxs-lookup"><span data-stu-id="6a0cd-201">**macOS cannot verify the developer of **MDATP MacOS DIY**. Are you sure you want to open it?**</span></span><br/>
    > <span data-ttu-id="6a0cd-202">En ouvrant cette application, vous allez remplacement de la sécurité système qui peut exposer votre ordinateur et vos informations personnelles à des programmes malveillants qui peuvent endommager votre Mac ou compromettre votre confidentialité.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-202">By opening this app, you will be overriding system security which can expose your computer and personal information to malware that may harm your Mac or compromise your privacy.</span></span>

10. <span data-ttu-id="6a0cd-203">Cliquez sur **Ouvrir**. </span><span class="sxs-lookup"><span data-stu-id="6a0cd-203">Click **Open**.</span></span>

    <span data-ttu-id="6a0cd-204">Le système doit afficher le message suivant :</span><span class="sxs-lookup"><span data-stu-id="6a0cd-204">The system should display the following message:</span></span>

    > <span data-ttu-id="6a0cd-205">Microsoft Defender ATP - fichier test MACOS EDR PDF</span><span class="sxs-lookup"><span data-stu-id="6a0cd-205">Microsoft Defender ATP - macOS EDR DIY test file</span></span><br/>
    > <span data-ttu-id="6a0cd-206">L’alerte correspondante sera disponible dans le portail MDATP.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-206">Corresponding alert will be available in the MDATP portal.</span></span>

11. <span data-ttu-id="6a0cd-207">Cliquez sur **Ouvrir**. </span><span class="sxs-lookup"><span data-stu-id="6a0cd-207">Click **Open**.</span></span>

    <span data-ttu-id="6a0cd-208">Dans quelques minutes, une alerte nommée « alerte de test macOS EDR » doit être appelée.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-208">In a few minutes an alert named "macOS EDR Test Alert" should be raised.</span></span>

12. <span data-ttu-id="6a0cd-209">Go to Microsoft Defender Security Center ( https://SecurityCenter.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="6a0cd-209">Go to Microsoft Defender Security Center (https://SecurityCenter.microsoft.com).</span></span>

13. <span data-ttu-id="6a0cd-210">Go to the Alert Queue.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-210">Go to the Alert Queue.</span></span>

    :::image type="content" source="images/b8db76c2-c368-49ad-970f-dcb87534d9be.png" alt-text="Exemple d’alerte de test macOS EDR qui affiche la gravité, la catégorie, la source de détection et un menu d’actions réduire.":::
    
    <span data-ttu-id="6a0cd-212">Regardez les détails de l’alerte et la chronologie de l’appareil, puis effectuez les étapes d’examen normales.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-212">Look at the alert details and the device timeline, and perform the regular investigation steps.</span></span>

## <a name="logging-installation-issues"></a><span data-ttu-id="6a0cd-213">Journalisation des problèmes d’installation</span><span class="sxs-lookup"><span data-stu-id="6a0cd-213">Logging installation issues</span></span>

<span data-ttu-id="6a0cd-214">Pour [plus d’informations](mac-resources.md#logging-installation-issues) sur la recherche du journal généré automatiquement par le programme d’installation en cas d’erreur, voir problèmes d’installation de journalisation.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-214">See [Logging installation issues](mac-resources.md#logging-installation-issues) for more information on how to find the automatically generated log that is created by the installer when an error occurs.</span></span>

## <a name="uninstallation"></a><span data-ttu-id="6a0cd-215">Désinstallation</span><span class="sxs-lookup"><span data-stu-id="6a0cd-215">Uninstallation</span></span>

<span data-ttu-id="6a0cd-216">Voir [Désinstallation](mac-resources.md#uninstalling) pour plus d’informations sur la suppression de Microsoft Defender pour endpoint pour macOS des appareils clients.</span><span class="sxs-lookup"><span data-stu-id="6a0cd-216">See [Uninstalling](mac-resources.md#uninstalling) for details on how to remove Microsoft Defender for Endpoint for macOS from client devices.</span></span>
