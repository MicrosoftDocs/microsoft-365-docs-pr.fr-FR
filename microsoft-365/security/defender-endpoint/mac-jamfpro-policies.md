---
title: Configurer microsoft Defender ATP pour les stratégies macOS dans Jamf Pro
description: Découvrez comment configurer les stratégies Microsoft Defender ATP pour macOS dans Jamf Pro
keywords: policies, microsoft, defender, atp, mac, installation, deploy, uninstallation, intune, jamfpro, macos,pépé, mojave, high sierra
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
ms.openlocfilehash: 9b00d81d3d51c343565ec4eb743181baa2750b01
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51687732"
---
# <a name="set-up-the-microsoft-defender-for-endpoint-on-macos-policies-in-jamf-pro"></a><span data-ttu-id="551ee-104">Configurer microsoft Defender pour le point de terminaison sur les stratégies macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="551ee-104">Set up the Microsoft Defender for Endpoint on macOS policies in Jamf Pro</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="551ee-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="551ee-105">**Applies to:**</span></span>

- [<span data-ttu-id="551ee-106">Defender pour point de terminaison pour Mac</span><span class="sxs-lookup"><span data-stu-id="551ee-106">Defender for Endpoint for Mac</span></span>](microsoft-defender-endpoint-mac.md)

<span data-ttu-id="551ee-107">Cette page vous guide à travers les étapes à suivre pour configurer des stratégies macOS dans Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="551ee-107">This page will guide you through the steps you need to take to set up macOS policies in Jamf Pro.</span></span>

<span data-ttu-id="551ee-108">Vous devez suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="551ee-108">You'll need to take the following steps:</span></span>

1. [<span data-ttu-id="551ee-109">Obtenir le package d'intégration De Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="551ee-109">Get the Microsoft Defender for Endpoint onboarding package</span></span>](#step-1-get-the-microsoft-defender-for-endpoint-onboarding-package)

2. [<span data-ttu-id="551ee-110">Créer un profil de configuration dans Jamf Pro à l'aide du package d'intégration</span><span class="sxs-lookup"><span data-stu-id="551ee-110">Create a configuration profile in Jamf Pro using the onboarding package</span></span>](#step-2-create-a-configuration-profile-in-jamf-pro-using-the-onboarding-package)

3. [<span data-ttu-id="551ee-111">Configurer les paramètres de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="551ee-111">Configure Microsoft Defender for Endpoint settings</span></span>](#step-3-configure-microsoft-defender-for-endpoint-settings)

4. [<span data-ttu-id="551ee-112">Configurer les paramètres de notification microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="551ee-112">Configure Microsoft Defender for Endpoint notification settings</span></span>](#step-4-configure-notifications-settings)

5. [<span data-ttu-id="551ee-113">Configurer la mise à jour automatique Microsoft (AutoUpdate)</span><span class="sxs-lookup"><span data-stu-id="551ee-113">Configure Microsoft AutoUpdate (MAU)</span></span>](#step-5-configure-microsoft-autoupdate-mau)

6. [<span data-ttu-id="551ee-114">Accorder un accès disque complet à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="551ee-114">Grant full disk access to Microsoft Defender for Endpoint</span></span>](#step-6-grant-full-disk-access-to-microsoft-defender-for-endpoint)

7. [<span data-ttu-id="551ee-115">Approuver l'extension de noyau pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="551ee-115">Approve Kernel extension for Microsoft Defender for Endpoint</span></span>](#step-7-approve-kernel-extension-for-microsoft-defender-for-endpoint)

8. [<span data-ttu-id="551ee-116">Approuver les extensions système pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="551ee-116">Approve System extensions for Microsoft Defender for Endpoint</span></span>](#step-8-approve-system-extensions-for-microsoft-defender-for-endpoint)

9. [<span data-ttu-id="551ee-117">Configurer l'extension réseau</span><span class="sxs-lookup"><span data-stu-id="551ee-117">Configure Network Extension</span></span>](#step-9-configure-network-extension)

10. [<span data-ttu-id="551ee-118">Planifier des analyses avec Microsoft Defender pour endpoint sur macOS</span><span class="sxs-lookup"><span data-stu-id="551ee-118">Schedule scans with Microsoft Defender for Endpoint on macOS</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/mac-schedule-scan-atp)

11. [<span data-ttu-id="551ee-119">Déployer Microsoft Defender pour le point de terminaison sur macOS</span><span class="sxs-lookup"><span data-stu-id="551ee-119">Deploy Microsoft Defender for Endpoint on macOS</span></span>](#step-11-deploy-microsoft-defender-for-endpoint-on-macos)


## <a name="step-1-get-the-microsoft-defender-for-endpoint-onboarding-package"></a><span data-ttu-id="551ee-120">Étape 1 : Obtenir le package d'intégration De Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="551ee-120">Step 1: Get the Microsoft Defender for Endpoint onboarding package</span></span>

1. <span data-ttu-id="551ee-121">Dans [le Centre de sécurité Microsoft Defender,](https://securitycenter.microsoft.com )accédez à **Paramètres >'intégration.**</span><span class="sxs-lookup"><span data-stu-id="551ee-121">In [Microsoft Defender Security Center](https://securitycenter.microsoft.com ), navigate to **Settings > Onboarding**.</span></span> 

2. <span data-ttu-id="551ee-122">Sélectionnez macOS comme système d'exploitation et Gestion des périphériques mobiles /Microsoft Intune comme méthode de déploiement.</span><span class="sxs-lookup"><span data-stu-id="551ee-122">Select macOS as the operating system and Mobile Device Management / Microsoft Intune as the deployment method.</span></span>

    ![Image du Centre de sécurité Microsoft Defender](images/onboarding-macos.png)

3. <span data-ttu-id="551ee-124">Sélectionnez **Télécharger le package d'intégration** (WindowsDefenderATPOnboardingPackage.zip).</span><span class="sxs-lookup"><span data-stu-id="551ee-124">Select **Download onboarding package** (WindowsDefenderATPOnboardingPackage.zip).</span></span>

4. <span data-ttu-id="551ee-125">Extraire `WindowsDefenderATPOnboardingPackage.zip` .</span><span class="sxs-lookup"><span data-stu-id="551ee-125">Extract `WindowsDefenderATPOnboardingPackage.zip`.</span></span>

5. <span data-ttu-id="551ee-126">Copiez le fichier à votre emplacement préféré.</span><span class="sxs-lookup"><span data-stu-id="551ee-126">Copy the file to your preferred location.</span></span> <span data-ttu-id="551ee-127">Par exemple : `C:\Users\JaneDoe_or_JohnDoe.contoso\Downloads\WindowsDefenderATPOnboardingPackage_macOS_MDM_contoso\jamf\WindowsDefenderATPOnboarding.plist`.</span><span class="sxs-lookup"><span data-stu-id="551ee-127">For example,  `C:\Users\JaneDoe_or_JohnDoe.contoso\Downloads\WindowsDefenderATPOnboardingPackage_macOS_MDM_contoso\jamf\WindowsDefenderATPOnboarding.plist`.</span></span>


## <a name="step-2-create-a-configuration-profile-in-jamf-pro-using-the-onboarding-package"></a><span data-ttu-id="551ee-128">Étape 2 : Créer un profil de configuration dans Jamf Pro à l'aide du package d'intégration</span><span class="sxs-lookup"><span data-stu-id="551ee-128">Step 2: Create a configuration profile in Jamf Pro using the onboarding package</span></span>

1. <span data-ttu-id="551ee-129">Recherchez le `WindowsDefenderATPOnboarding.plist` fichier dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="551ee-129">Locate the file `WindowsDefenderATPOnboarding.plist` from the previous section.</span></span>

   ![Image du fichier WindowsDefenderATPOnboarding](images/plist-onboarding-file.png)

 
2. <span data-ttu-id="551ee-131">Dans le tableau de bord Jamf Pro, sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="551ee-131">In the Jamf Pro dashboard, select **New**.</span></span>

    ![Image de création d'un tableau de bord Jamf Pro](images/jamf-pro-configure-profile.png)

3. <span data-ttu-id="551ee-133">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="551ee-133">Enter the following details:</span></span>

   <span data-ttu-id="551ee-134">**Général**</span><span class="sxs-lookup"><span data-stu-id="551ee-134">**General**</span></span>
   - <span data-ttu-id="551ee-135">Nom : intégration MDATP pour macOS</span><span class="sxs-lookup"><span data-stu-id="551ee-135">Name: MDATP onboarding for macOS</span></span>
   - <span data-ttu-id="551ee-136">Description : intégration EDR MDATP pour macOS</span><span class="sxs-lookup"><span data-stu-id="551ee-136">Description: MDATP EDR onboarding for macOS</span></span>
   - <span data-ttu-id="551ee-137">Catégorie : Aucun</span><span class="sxs-lookup"><span data-stu-id="551ee-137">Category: None</span></span>
   - <span data-ttu-id="551ee-138">Méthode de distribution : installer automatiquement</span><span class="sxs-lookup"><span data-stu-id="551ee-138">Distribution Method: Install Automatically</span></span>
   - <span data-ttu-id="551ee-139">Niveau : niveau ordinateur</span><span class="sxs-lookup"><span data-stu-id="551ee-139">Level: Computer Level</span></span>

4. <span data-ttu-id="551ee-140">In **Application & Custom Settings** select **Configure**.</span><span class="sxs-lookup"><span data-stu-id="551ee-140">In **Application & Custom Settings** select **Configure**.</span></span>

    ![Image de configuration de l'application et des paramètres personnalisés](images/jamfpro-mac-profile.png)

5. <span data-ttu-id="551ee-142">Sélectionnez **Télécharger un fichier (fichier PLIST),** puis dans Domaine de **préférence,** entrez `com.microsoft.wdav.atp` :</span><span class="sxs-lookup"><span data-stu-id="551ee-142">Select **Upload File (PLIST file)** then in **Preference Domain** enter: `com.microsoft.wdav.atp`.</span></span> 

    ![Image du fichier de téléchargement plist jamfpro](images/jamfpro-plist-upload.png)

    ![Image du fichier de liste des propriétés de fichier de téléchargement](images/jamfpro-plist-file.png)

7. <span data-ttu-id="551ee-145">Sélectionnez **Ouvrir** et sélectionnez le fichier d'intégration.</span><span class="sxs-lookup"><span data-stu-id="551ee-145">Select **Open** and select the onboarding file.</span></span>

    ![Image du fichier d'intégration](images/jamfpro-plist-file-onboard.png)

8. <span data-ttu-id="551ee-147">Sélectionnez **Télécharger.**</span><span class="sxs-lookup"><span data-stu-id="551ee-147">Select **Upload**.</span></span> 

    ![Image du téléchargement d'un fichier plist](images/jamfpro-upload-plist.png)


9. <span data-ttu-id="551ee-149">Sélectionnez **l'onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="551ee-149">Select the **Scope** tab.</span></span>

    ![Image de l'onglet d'étendue](images/jamfpro-scope-tab.png)

10. <span data-ttu-id="551ee-151">Sélectionnez les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="551ee-151">Select the target computers.</span></span>

    ![Image des ordinateurs cibles](images/jamfpro-target-computer.png)

    ![Image des cibles](images/jamfpro-targets.png) 

11. <span data-ttu-id="551ee-154">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="551ee-154">Select **Save**.</span></span>

    ![Image des ordinateurs cibles de déploiement](images/jamfpro-deployment-target.png)

    ![Image des ordinateurs cibles sélectionnés](images/jamfpro-target-selected.png)

12. <span data-ttu-id="551ee-157">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="551ee-157">Select **Done**.</span></span>

    ![Image des ordinateurs de groupe cibles](images/jamfpro-target-group.png)

    ![Liste des profils de configuration](images/jamfpro-configuration-policies.png)

## <a name="step-3-configure-microsoft-defender-for-endpoint-settings"></a><span data-ttu-id="551ee-160">Étape 3 : Configurer Microsoft Defender pour les paramètres de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="551ee-160">Step 3: Configure Microsoft Defender for Endpoint settings</span></span>

1.  <span data-ttu-id="551ee-161">Utilisez les paramètres de configuration microsoft Defender pour les points de terminaison suivants :</span><span class="sxs-lookup"><span data-stu-id="551ee-161">Use the following Microsoft Defender for Endpoint configuration settings:</span></span>

    - <span data-ttu-id="551ee-162">enableRealTimeProtection</span><span class="sxs-lookup"><span data-stu-id="551ee-162">enableRealTimeProtection</span></span>
    - <span data-ttu-id="551ee-163">passiveMode</span><span class="sxs-lookup"><span data-stu-id="551ee-163">passiveMode</span></span>
    
    >[!NOTE]
    ><span data-ttu-id="551ee-164">Non désactivé par défaut, si vous envisagez d'exécuter un antivirus tiers pour macOS, définissez-le sur `true` .</span><span class="sxs-lookup"><span data-stu-id="551ee-164">Not turned on by default, if you are planning to run a third-party AV for macOS, set it to `true`.</span></span>

    - <span data-ttu-id="551ee-165">exclusions</span><span class="sxs-lookup"><span data-stu-id="551ee-165">exclusions</span></span>
    - <span data-ttu-id="551ee-166">excludedPath</span><span class="sxs-lookup"><span data-stu-id="551ee-166">excludedPath</span></span>
    - <span data-ttu-id="551ee-167">excludedFileExtension</span><span class="sxs-lookup"><span data-stu-id="551ee-167">excludedFileExtension</span></span>
    - <span data-ttu-id="551ee-168">excludedFileName</span><span class="sxs-lookup"><span data-stu-id="551ee-168">excludedFileName</span></span>
    - <span data-ttu-id="551ee-169">exclusionsMergePolicy</span><span class="sxs-lookup"><span data-stu-id="551ee-169">exclusionsMergePolicy</span></span>
    - <span data-ttu-id="551ee-170">allowedThreats</span><span class="sxs-lookup"><span data-stu-id="551ee-170">allowedThreats</span></span>
    
    >[!NOTE]
    ><span data-ttu-id="551ee-171">EICAR est sur l'exemple, si vous êtes en train de passer par une preuve de concept, supprimez-le en particulier si vous testez EICAR.</span><span class="sxs-lookup"><span data-stu-id="551ee-171">EICAR is on the sample, if you are going through a proof-of-concept, remove it especially if you are testing EICAR.</span></span>
        
    - <span data-ttu-id="551ee-172">disallowedThreatActions</span><span class="sxs-lookup"><span data-stu-id="551ee-172">disallowedThreatActions</span></span>
    - <span data-ttu-id="551ee-173">potentially_unwanted_application</span><span class="sxs-lookup"><span data-stu-id="551ee-173">potentially_unwanted_application</span></span>
    - <span data-ttu-id="551ee-174">archive_bomb</span><span class="sxs-lookup"><span data-stu-id="551ee-174">archive_bomb</span></span>
    - <span data-ttu-id="551ee-175">cloudService</span><span class="sxs-lookup"><span data-stu-id="551ee-175">cloudService</span></span>
    - <span data-ttu-id="551ee-176">automaticSampleSubmission</span><span class="sxs-lookup"><span data-stu-id="551ee-176">automaticSampleSubmission</span></span>
    - <span data-ttu-id="551ee-177">étiquettes</span><span class="sxs-lookup"><span data-stu-id="551ee-177">tags</span></span>
    - <span data-ttu-id="551ee-178">hideStatusMenuIcon</span><span class="sxs-lookup"><span data-stu-id="551ee-178">hideStatusMenuIcon</span></span>
    
     <span data-ttu-id="551ee-179">Pour plus d'informations, [voir Liste des propriétés pour le profil de configuration Jamf.](mac-preferences.md#property-list-for-jamf-configuration-profile)</span><span class="sxs-lookup"><span data-stu-id="551ee-179">For information, see [Property list for Jamf configuration profile](mac-preferences.md#property-list-for-jamf-configuration-profile).</span></span>

     ```XML
     <?xml version="1.0" encoding="UTF-8"?>
     <!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
     <plist version="1.0">
     <dict>
         <key>antivirusEngine</key>
         <dict>
             <key>enableRealTimeProtection</key>
             <true/>
             <key>passiveMode</key>
             <false/>
             <key>exclusions</key>
             <array>
                 <dict>
                     <key>$type</key>
                     <string>excludedPath</string>
                     <key>isDirectory</key>
                     <false/>
                     <key>path</key>
                     <string>/var/log/system.log</string>
                 </dict>
                 <dict>
                     <key>$type</key>
                     <string>excludedPath</string>
                     <key>isDirectory</key>
                     <true/>
                     <key>path</key>
                     <string>/home</string>
                 </dict>
                 <dict>
                     <key>$type</key>
                     <string>excludedFileExtension</string>
                     <key>extension</key>
                     <string>pdf</string>
                 </dict>
                 <dict>
                     <key>$type</key>
                     <string>excludedFileName</string>
                     <key>name</key>
                     <string>cat</string>
                 </dict>
             </array>
             <key>exclusionsMergePolicy</key>
             <string>merge</string>
             <key>allowedThreats</key>
             <array>
                 <string>EICAR-Test-File (not a virus)</string>
             </array>
             <key>disallowedThreatActions</key>
             <array>
                 <string>allow</string>
                 <string>restore</string>
             </array>
             <key>threatTypeSettings</key>
             <array>
                 <dict>
                     <key>key</key>
                     <string>potentially_unwanted_application</string>
                     <key>value</key>
                     <string>block</string>
                 </dict>
                 <dict>
                     <key>key</key>
                     <string>archive_bomb</string>
                     <key>value</key>
                     <string>audit</string>
                 </dict>
             </array>
             <key>threatTypeSettingsMergePolicy</key>
             <string>merge</string>
         </dict>
         <key>cloudService</key>
         <dict>
             <key>enabled</key>
             <true/>
             <key>diagnosticLevel</key>
             <string>optional</string>
             <key>automaticSampleSubmission</key>
             <true/>
         </dict>
         <key>edr</key>
         <dict>
             <key>tags</key>
             <array>
                 <dict>
                     <key>key</key>
                     <string>GROUP</string>
                     <key>value</key>
                     <string>ExampleTag</string>
                 </dict>
             </array>
         </dict>
         <key>userInterface</key>
         <dict>
             <key>hideStatusMenuIcon</key>
             <false/>
         </dict>
     </dict>
     </plist>
     ```

2. <span data-ttu-id="551ee-180">Enregistrez le fichier sous `MDATP_MDAV_configuration_settings.plist` .</span><span class="sxs-lookup"><span data-stu-id="551ee-180">Save the file as `MDATP_MDAV_configuration_settings.plist`.</span></span>


3.  <span data-ttu-id="551ee-181">Dans le tableau de bord Jamf Pro, sélectionnez **Général**.</span><span class="sxs-lookup"><span data-stu-id="551ee-181">In the Jamf Pro dashboard, select **General**.</span></span>

    ![Image du nouveau tableau de bord Jamf Pro](images/644e0f3af40c29e80ca1443535b2fe32.png)

4. <span data-ttu-id="551ee-183">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="551ee-183">Enter the following details:</span></span>

    <span data-ttu-id="551ee-184">**Général**</span><span class="sxs-lookup"><span data-stu-id="551ee-184">**General**</span></span>
    
    - <span data-ttu-id="551ee-185">Nom : paramètres de configuration MDAV MDATP</span><span class="sxs-lookup"><span data-stu-id="551ee-185">Name: MDATP MDAV configuration settings</span></span>
    - <span data-ttu-id="551ee-186">Description :\<blank\></span><span class="sxs-lookup"><span data-stu-id="551ee-186">Description:\<blank\></span></span>
    - <span data-ttu-id="551ee-187">Catégorie : Aucun (par défaut)</span><span class="sxs-lookup"><span data-stu-id="551ee-187">Category: None (default)</span></span>
    - <span data-ttu-id="551ee-188">Méthode de distribution : installer automatiquement (par défaut)</span><span class="sxs-lookup"><span data-stu-id="551ee-188">Distribution Method: Install Automatically(default)</span></span>
    - <span data-ttu-id="551ee-189">Niveau : Niveau ordinateur (par défaut)</span><span class="sxs-lookup"><span data-stu-id="551ee-189">Level: Computer Level(default)</span></span>

    ![Image des paramètres de configuration MDAV MDATP](images/3160906404bc5a2edf84d1d015894e3b.png)

5. <span data-ttu-id="551ee-191">In **Application & Custom Settings** select **Configure**.</span><span class="sxs-lookup"><span data-stu-id="551ee-191">In **Application & Custom Settings** select **Configure**.</span></span>

    ![Image de l'application et des paramètres personnalisés](images/e1cc1e48ec9d5d688087b4d771e668d2.png)

6. <span data-ttu-id="551ee-193">Sélectionnez **Télécharger un fichier (fichier PLIST).**</span><span class="sxs-lookup"><span data-stu-id="551ee-193">Select **Upload File (PLIST file)**.</span></span>

    ![Image du fichier plist des paramètres de configuration](images/6f85269276b2278eca4bce84f935f87b.png)

7. <span data-ttu-id="551ee-195">In **Preferences Domain**, enter `com.microsoft.wdav` , then select Upload  **PLIST File**.</span><span class="sxs-lookup"><span data-stu-id="551ee-195">In **Preferences Domain**, enter `com.microsoft.wdav`, then select  **Upload PLIST File**.</span></span>

    ![Image du domaine des préférences de paramètres de configuration](images/db15f147dd959e872a044184711d7d46.png)

8. <span data-ttu-id="551ee-197">Sélectionnez **Choisir un fichier.**</span><span class="sxs-lookup"><span data-stu-id="551ee-197">Select **Choose File**.</span></span>

    ![Image des paramètres de configuration choisir un fichier](images/526e978761fc571cca06907da7b01fd6.png)

9. <span data-ttu-id="551ee-199">Sélectionnez **le MDATP_MDAV_configuration_settings.plist,** puis sélectionnez **Ouvrir.**</span><span class="sxs-lookup"><span data-stu-id="551ee-199">Select the **MDATP_MDAV_configuration_settings.plist**, then select **Open**.</span></span>

    ![Image des paramètres de configuration mdatpmdav](images/98acea3750113b8dbab334296e833003.png)

10. <span data-ttu-id="551ee-201">Sélectionnez **Télécharger.**</span><span class="sxs-lookup"><span data-stu-id="551ee-201">Select **Upload**.</span></span>

    ![Image du téléchargement des paramètres de configuration](images/0adb21c13206861ba9b30a879ade93d3.png)

    ![Image de l'image de téléchargement des paramètres de configuration](images/f624de59b3cc86e3e2d32ae5de093e02.png)

    >[!NOTE]
    ><span data-ttu-id="551ee-204">Si vous téléchargez le fichier Intune, vous obtenez l'erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="551ee-204">If you happen to upload the Intune file, you'll get the following error:</span></span><br>
    ><span data-ttu-id="551ee-205">![Image du téléchargement de fichiers intune des paramètres de configuration](images/8e69f867664668796a3b2904896f0436.png)</span><span class="sxs-lookup"><span data-stu-id="551ee-205">![Image of configuration settings intune file upload](images/8e69f867664668796a3b2904896f0436.png)</span></span>


11. <span data-ttu-id="551ee-206">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="551ee-206">Select **Save**.</span></span> 

    ![Image de l'image Enregistrer l'image des paramètres de configuration](images/1b6b5a4edcb42d97f1e70a6a0fa48e3a.png)

12. <span data-ttu-id="551ee-208">Le fichier est téléchargé.</span><span class="sxs-lookup"><span data-stu-id="551ee-208">The file is uploaded.</span></span>

    ![Image de l'image téléchargée du fichier de paramètres de configuration](images/33e2b2a1611fdddf6b5b79e54496e3bb.png)

    ![Image du fichier de paramètres de configuration téléchargé](images/a422e57fe8d45689227e784443e51bd1.png)

13. <span data-ttu-id="551ee-211">Sélectionnez **l'onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="551ee-211">Select the **Scope** tab.</span></span>

    ![Image de l'étendue des paramètres de configuration](images/9fc17529e5577eefd773c658ec576a7d.png)

14. <span data-ttu-id="551ee-213">Sélectionnez **Le groupe d'ordinateurs de Contoso.**</span><span class="sxs-lookup"><span data-stu-id="551ee-213">Select **Contoso's Machine Group**.</span></span> 

15. <span data-ttu-id="551ee-214">Sélectionnez **Ajouter,** puis **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="551ee-214">Select **Add**, then select **Save**.</span></span>

    ![Image des paramètres de configuration addsav](images/cf30438b5512ac89af1d11cbf35219a6.png)

    ![Image de l'ajout d'enregistrer les paramètres de configuration](images/6f093e42856753a3955cab7ee14f12d9.png)

16. <span data-ttu-id="551ee-217">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="551ee-217">Select **Done**.</span></span> <span data-ttu-id="551ee-218">Vous verrez le nouveau profil **de configuration.**</span><span class="sxs-lookup"><span data-stu-id="551ee-218">You'll see the new **Configuration profile**.</span></span>

    ![Image de l'image de profil de configuration des paramètres de configuration](images/dd55405106da0dfc2f50f8d4525b01c8.png)


## <a name="step-4-configure-notifications-settings"></a><span data-ttu-id="551ee-220">Étape 4 : Configurer les paramètres de notifications</span><span class="sxs-lookup"><span data-stu-id="551ee-220">Step 4: Configure notifications settings</span></span>

<span data-ttu-id="551ee-221">Ces étapes s'appliquent à macOS 10.15 (Genreline) ou aux appareils plus nouveaux.</span><span class="sxs-lookup"><span data-stu-id="551ee-221">These steps are applicable of macOS 10.15 (Catalina) or newer.</span></span>

1. <span data-ttu-id="551ee-222">Dans le tableau de bord Jamf Pro, sélectionnez **Ordinateurs,** puis **Profils de configuration.**</span><span class="sxs-lookup"><span data-stu-id="551ee-222">In the Jamf Pro dashboard, select **Computers**, then **Configuration Profiles**.</span></span>

2. <span data-ttu-id="551ee-223">Cliquez **sur** Nouveau, puis entrez les détails suivants pour **options**:</span><span class="sxs-lookup"><span data-stu-id="551ee-223">Click **New**, and enter the following details for **Options**:</span></span>
    
    - <span data-ttu-id="551ee-224">Onglet **Général**:</span><span class="sxs-lookup"><span data-stu-id="551ee-224">Tab **General**:</span></span> 
        - <span data-ttu-id="551ee-225">**Name**: Paramètres de notification MDAV MDATP</span><span class="sxs-lookup"><span data-stu-id="551ee-225">**Name**: MDATP MDAV Notification settings</span></span>
        - <span data-ttu-id="551ee-226">**Description**: macOS 10.15 (Contrôle) ou une nouveauté</span><span class="sxs-lookup"><span data-stu-id="551ee-226">**Description**: macOS 10.15 (Catalina) or newer</span></span>
        - <span data-ttu-id="551ee-227">**Catégorie**: Aucun *(par défaut)*</span><span class="sxs-lookup"><span data-stu-id="551ee-227">**Category**: None *(default)*</span></span>
        - <span data-ttu-id="551ee-228">**Méthode de distribution**: installer automatiquement *(par défaut)*</span><span class="sxs-lookup"><span data-stu-id="551ee-228">**Distribution Method**: Install Automatically *(default)*</span></span>
        - <span data-ttu-id="551ee-229">**Niveau**: niveau ordinateur *(par défaut)*</span><span class="sxs-lookup"><span data-stu-id="551ee-229">**Level**: Computer Level *(default)*</span></span>

        ![Image des paramètres de profil de configuration mdatpmdav](images/c9820a5ff84aaf21635c04a23a97ca93.png)

    - <span data-ttu-id="551ee-231">Tab **Notifications,** click **Add**, and enter the following values:</span><span class="sxs-lookup"><span data-stu-id="551ee-231">Tab **Notifications**, click **Add**, and enter the following values:</span></span>
        - <span data-ttu-id="551ee-232">**ID d'offre groupée**: `com.microsoft.wdav.tray`</span><span class="sxs-lookup"><span data-stu-id="551ee-232">**Bundle ID**: `com.microsoft.wdav.tray`</span></span>
        - <span data-ttu-id="551ee-233">**Alertes critiques**: cliquez sur **Désactiver**</span><span class="sxs-lookup"><span data-stu-id="551ee-233">**Critical Alerts**: Click **Disable**</span></span>
        - <span data-ttu-id="551ee-234">**Notifications :** cliquez sur **Activer**</span><span class="sxs-lookup"><span data-stu-id="551ee-234">**Notifications**: Click **Enable**</span></span>
        - <span data-ttu-id="551ee-235">**Type d'alerte bannière**: sélectionner **Inclure** **et temporaire** *(par défaut)*</span><span class="sxs-lookup"><span data-stu-id="551ee-235">**Banner alert type**: Select **Include** and **Temporary** *(default)*</span></span>
        - <span data-ttu-id="551ee-236">**Notifications sur l'écran de verrouillage**: cliquez sur **Masquer**</span><span class="sxs-lookup"><span data-stu-id="551ee-236">**Notifications on lock screen**: Click **Hide**</span></span>
        - <span data-ttu-id="551ee-237">**Notifications dans le Centre de notifications**: cliquez sur **Afficher**</span><span class="sxs-lookup"><span data-stu-id="551ee-237">**Notifications in Notification Center**: Click **Display**</span></span>
        - <span data-ttu-id="551ee-238">**Icône d'application de badge**: cliquez sur **Afficher**</span><span class="sxs-lookup"><span data-stu-id="551ee-238">**Badge app icon**: Click **Display**</span></span>

        ![Image du bac de notifications mdatpmdav des paramètres de configuration](images/7f9138053dbcbf928e5182ee7b295ebe.png)

    - <span data-ttu-id="551ee-240">Tab **Notifications**, click **Add** one more time, scroll down to **New Notifications Settings**</span><span class="sxs-lookup"><span data-stu-id="551ee-240">Tab **Notifications**, click **Add** one more time, scroll down to **New Notifications Settings**</span></span>
        - <span data-ttu-id="551ee-241">**ID d'offre groupée**: `com.microsoft.autoupdate2`</span><span class="sxs-lookup"><span data-stu-id="551ee-241">**Bundle ID**: `com.microsoft.autoupdate2`</span></span>
        - <span data-ttu-id="551ee-242">Configurer le reste des paramètres sur les mêmes valeurs que ci-dessus</span><span class="sxs-lookup"><span data-stu-id="551ee-242">Configure the rest of the settings to the same values as above</span></span>

        ![Image des paramètres de configuration mdatpmdav notifications mau](images/4bac6ce277aedfb4a674f2d9fcb2599a.png)

        <span data-ttu-id="551ee-244">Notez que vous avez maintenant deux « tables » avec des configurations de notification, une pour l'ID d'offre groupée : **com.microsoft.wdav.tray** et une autre pour l'ID d'offre groupée : **com.microsoft.autoupdate2**.</span><span class="sxs-lookup"><span data-stu-id="551ee-244">Note that now you have two 'tables' with notification configurations, one for **Bundle ID: com.microsoft.wdav.tray**, and another for **Bundle ID: com.microsoft.autoupdate2**.</span></span> <span data-ttu-id="551ee-245">Bien que vous pouvez configurer les paramètres d'alerte en fonction de vos  besoins,  les ID d'offre groupée doivent être exactement les mêmes que ceux décrits précédemment, et le commutateur Inclure doit être en cours pour les **notifications.**</span><span class="sxs-lookup"><span data-stu-id="551ee-245">While you can configure alert settings per your requirements, Bundle IDs must be exactly the same as described before, and **Include** switch must be **On** for **Notifications**.</span></span>

3. <span data-ttu-id="551ee-246">Sélectionnez **l'onglet** Étendue, puis **sélectionnez Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="551ee-246">Select the **Scope** tab, then select **Add**.</span></span>

    ![Image de l'étendue ajouter des paramètres de configuration](images/441aa2ecd36abadcdd8aed03556080b5.png)

4. <span data-ttu-id="551ee-248">Sélectionnez **Le groupe d'ordinateurs de Contoso.**</span><span class="sxs-lookup"><span data-stu-id="551ee-248">Select **Contoso's Machine Group**.</span></span> 

5. <span data-ttu-id="551ee-249">Sélectionnez **Ajouter,** puis **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="551ee-249">Select **Add**, then select **Save**.</span></span>
    
    ![Image des paramètres de configuration contoso machine grp save](images/09a275e321268e5e3ac0c0865d3e2db5.png)
    
    ![Image des paramètres de configuration pour ajouter l'enregistrer](images/4d2d1d4ee13d3f840f425924c3df0d51.png)

6. <span data-ttu-id="551ee-252">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="551ee-252">Select **Done**.</span></span> <span data-ttu-id="551ee-253">Vous verrez le nouveau profil **de configuration.**</span><span class="sxs-lookup"><span data-stu-id="551ee-253">You'll see the new **Configuration profile**.</span></span>
    <span data-ttu-id="551ee-254">![Image du paramètre de configuration terminé img](images/633ad26b8bf24ec683c98b2feb884bdf.png)</span><span class="sxs-lookup"><span data-stu-id="551ee-254">![Image of configuration setting done img](images/633ad26b8bf24ec683c98b2feb884bdf.png)</span></span>

## <a name="step-5-configure-microsoft-autoupdate-mau"></a><span data-ttu-id="551ee-255">Étape 5 : Configurer la mise à jour automatique Microsoft (AutoUpdate)</span><span class="sxs-lookup"><span data-stu-id="551ee-255">Step 5: Configure Microsoft AutoUpdate (MAU)</span></span>

1. <span data-ttu-id="551ee-256">Utilisez les paramètres de configuration microsoft Defender pour les points de terminaison suivants :</span><span class="sxs-lookup"><span data-stu-id="551ee-256">Use the following Microsoft Defender for Endpoint configuration settings:</span></span>

      ```XML
   <?xml version="1.0" encoding="UTF-8"?>
   <!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
   <plist version="1.0">
   <dict>
    <key>ChannelName</key>
    <string>Current</string>
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

2. <span data-ttu-id="551ee-257">Enregistrez-le sous `MDATP_MDAV_MAU_settings.plist` .</span><span class="sxs-lookup"><span data-stu-id="551ee-257">Save it as `MDATP_MDAV_MAU_settings.plist`.</span></span>

3. <span data-ttu-id="551ee-258">Dans le tableau de bord Jamf Pro, sélectionnez **Général**.</span><span class="sxs-lookup"><span data-stu-id="551ee-258">In the Jamf Pro dashboard, select **General**.</span></span> 

    ![Image de l'image générale du paramètre de configuration](images/eaba2a23dd34f73bf59e826217ba6f15.png)

4. <span data-ttu-id="551ee-260">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="551ee-260">Enter the following details:</span></span>

    <span data-ttu-id="551ee-261">**Général**</span><span class="sxs-lookup"><span data-stu-id="551ee-261">**General**</span></span> 
    
    - <span data-ttu-id="551ee-262">Name: MDATP MDAV MAU settings</span><span class="sxs-lookup"><span data-stu-id="551ee-262">Name: MDATP MDAV MAU settings</span></span>
    - <span data-ttu-id="551ee-263">Description : Paramètres de mise à jour automatique Microsoft pour MDATP pour macOS</span><span class="sxs-lookup"><span data-stu-id="551ee-263">Description: Microsoft AutoUpdate settings for MDATP for macOS</span></span>
    - <span data-ttu-id="551ee-264">Catégorie : Aucun (par défaut)</span><span class="sxs-lookup"><span data-stu-id="551ee-264">Category: None (default)</span></span>
    - <span data-ttu-id="551ee-265">Méthode de distribution : installer automatiquement (par défaut)</span><span class="sxs-lookup"><span data-stu-id="551ee-265">Distribution Method: Install Automatically(default)</span></span>
    - <span data-ttu-id="551ee-266">Niveau : Niveau ordinateur (par défaut)</span><span class="sxs-lookup"><span data-stu-id="551ee-266">Level: Computer Level(default)</span></span>

5. <span data-ttu-id="551ee-267">Dans **Application & paramètres personnalisés, sélectionnez** **Configurer.**</span><span class="sxs-lookup"><span data-stu-id="551ee-267">In **Application & Custom Settings** select **Configure**.</span></span>

    ![Image de l'application de paramètre de configuration et des paramètres personnalisés](images/1f72e9c15eaafcabf1504397e99be311.png)

6. <span data-ttu-id="551ee-269">Sélectionnez **Télécharger un fichier (fichier PLIST).**</span><span class="sxs-lookup"><span data-stu-id="551ee-269">Select **Upload File (PLIST file)**.</span></span>

    ![Image de la liste des paramètres de configuration](images/1213872db5833aa8be535da57653219f.png)  

7. <span data-ttu-id="551ee-271">In **Preference Domain** enter: , then select Upload `com.microsoft.autoupdate2` **PLIST File**.</span><span class="sxs-lookup"><span data-stu-id="551ee-271">In **Preference Domain** enter: `com.microsoft.autoupdate2`, then select **Upload PLIST File**.</span></span>

    ![Image du domaine préf du paramètre de configuration](images/1213872db5833aa8be535da57653219f.png)

8. <span data-ttu-id="551ee-273">Sélectionnez **Choisir un fichier.**</span><span class="sxs-lookup"><span data-stu-id="551ee-273">Select **Choose File**.</span></span>

    ![Image du fichier choosefile du paramètre de configuration](images/335aff58950ce62d1dabc289ecdce9ed.png)

9. <span data-ttu-id="551ee-275">Sélectionnez **MDATP_MDAV_MAU_settings.plist.**</span><span class="sxs-lookup"><span data-stu-id="551ee-275">Select **MDATP_MDAV_MAU_settings.plist**.</span></span>

    ![Image des paramètres de configuration mdatpmdavmau](images/a26bd4967cd54bb113a2c8d32894c3de.png)

10. <span data-ttu-id="551ee-277">Sélectionnez **Télécharger.**</span><span class="sxs-lookup"><span data-stu-id="551ee-277">Select **Upload**.</span></span>
    <span data-ttu-id="551ee-278">![Image du délimitement de configuration de configuration](images/4239ca0528efb0734e4ca0b490bfb22d.png)</span><span class="sxs-lookup"><span data-stu-id="551ee-278">![Image of configuration setting uplimage](images/4239ca0528efb0734e4ca0b490bfb22d.png)</span></span>

    ![Image de la configuration de la configuration de la configuration](images/4ec20e72c8aed9a4c16912e01692436a.png)

11. <span data-ttu-id="551ee-280">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="551ee-280">Select **Save**.</span></span>

    ![Image du paramètre de configuration saveimg](images/253274b33e74f3f5b8d475cf8692ce4e.png)

12. <span data-ttu-id="551ee-282">Sélectionnez **l'onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="551ee-282">Select the **Scope** tab.</span></span>
   
     ![Image du paramètre de configuration scopetab](images/10ab98358b2d602f3f67618735fa82fb.png)

13. <span data-ttu-id="551ee-284">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="551ee-284">Select **Add**.</span></span>
    
    ![Image du paramètre de configuration addimg1](images/56e6f6259b9ce3c1706ed8d666ae4947.png)

    ![Image du paramètre de configuration addimg2](images/38c67ee1905c4747c3b26c8eba57726b.png)

    ![Image du paramètre de configuration addimg3](images/321ba245f14743c1d5d51c15e99deecc.png)

14. <span data-ttu-id="551ee-288">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="551ee-288">Select **Done**.</span></span>
    
    ![Image du paramètre de configuration doneimage](images/ba44cdb77e4781aa8b940fb83e3c21f7.png)

## <a name="step-6-grant-full-disk-access-to-microsoft-defender-for-endpoint"></a><span data-ttu-id="551ee-290">Étape 6 : Accorder un accès disque complet à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="551ee-290">Step 6: Grant full disk access to Microsoft Defender for Endpoint</span></span>

1. <span data-ttu-id="551ee-291">Dans le tableau de bord Jamf Pro, sélectionnez **Profils de configuration.**</span><span class="sxs-lookup"><span data-stu-id="551ee-291">In the Jamf Pro dashboard, select **Configuration Profiles**.</span></span>

    ![Image du profil de configuration des paramètres de configuration](images/264493cd01e62c7085659d6fdc26dc91.png)

2. <span data-ttu-id="551ee-293">Sélectionnez **+ Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="551ee-293">Select **+ New**.</span></span> 

3. <span data-ttu-id="551ee-294">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="551ee-294">Enter the following details:</span></span>

    <span data-ttu-id="551ee-295">**Général**</span><span class="sxs-lookup"><span data-stu-id="551ee-295">**General**</span></span> 
    - <span data-ttu-id="551ee-296">Nom : MDATP MDAV : accorder un accès disque total à l'EDR et à l'antivirus</span><span class="sxs-lookup"><span data-stu-id="551ee-296">Name: MDATP MDAV - grant Full Disk Access to EDR and AV</span></span>
    - <span data-ttu-id="551ee-297">Description : sur macOS Ou une nouveauté, le nouveau contrôle de stratégie des préférences de confidentialité</span><span class="sxs-lookup"><span data-stu-id="551ee-297">Description: On macOS Catalina or newer, the new Privacy Preferences Policy Control</span></span>
    - <span data-ttu-id="551ee-298">Catégorie : Aucun</span><span class="sxs-lookup"><span data-stu-id="551ee-298">Category: None</span></span>
    - <span data-ttu-id="551ee-299">Méthode de distribution : installer automatiquement</span><span class="sxs-lookup"><span data-stu-id="551ee-299">Distribution method: Install Automatically</span></span>
    - <span data-ttu-id="551ee-300">Niveau : niveau ordinateur</span><span class="sxs-lookup"><span data-stu-id="551ee-300">Level: Computer level</span></span>


    ![Image du paramètre de configuration général](images/ba3d40399e1a6d09214ecbb2b341923f.png)

4. <span data-ttu-id="551ee-302">In **Configure Privacy Preferences Policy Control** select **Configure**.</span><span class="sxs-lookup"><span data-stu-id="551ee-302">In **Configure Privacy Preferences Policy Control** select **Configure**.</span></span>

    ![Image du contrôle de stratégie de confidentialité de la configuration](images/715ae7ec8d6a262c489f94d14e1e51bb.png)

5. <span data-ttu-id="551ee-304">Dans **Le contrôle de stratégie des préférences de confidentialité,** entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="551ee-304">In **Privacy Preferences Policy Control**, enter the following details:</span></span>

    - <span data-ttu-id="551ee-305">Identificateur : `com.microsoft.wdav`</span><span class="sxs-lookup"><span data-stu-id="551ee-305">Identifier: `com.microsoft.wdav`</span></span>
    - <span data-ttu-id="551ee-306">Type d'identificateur : ID d'offre groupée</span><span class="sxs-lookup"><span data-stu-id="551ee-306">Identifier Type: Bundle ID</span></span>
    - <span data-ttu-id="551ee-307">Conditions requises pour le code : `identifier "com.microsoft.wdav" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span><span class="sxs-lookup"><span data-stu-id="551ee-307">Code Requirement: `identifier "com.microsoft.wdav" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span></span>


    ![Image des détails du contrôle de stratégie de confidentialité des paramètres de configuration](images/22cb439de958101c0a12f3038f905b27.png)

6. <span data-ttu-id="551ee-309">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="551ee-309">Select **+ Add**.</span></span>

    ![Image du paramètre de configuration ajouter la stratégie système à tous les fichiers](images/bd93e78b74c2660a0541af4690dd9485.png)

    - <span data-ttu-id="551ee-311">Sous Application ou service : définir sur **SystemPolicyAllFiles**</span><span class="sxs-lookup"><span data-stu-id="551ee-311">Under App or service: Set to **SystemPolicyAllFiles**</span></span>

    - <span data-ttu-id="551ee-312">Sous « accès » : définir sur **Autoriser**</span><span class="sxs-lookup"><span data-stu-id="551ee-312">Under "access": Set to **Allow**</span></span>

7. <span data-ttu-id="551ee-313">Sélectionnez **Enregistrer** (et non celui en bas à droite).</span><span class="sxs-lookup"><span data-stu-id="551ee-313">Select **Save** (not the one at the bottom right).</span></span>

    ![Image des images d'enregistrer les paramètres de configuration](images/6de50b4a897408ddc6ded56a09c09fe2.png)

8. <span data-ttu-id="551ee-315">Cliquez sur le `+` signe en de côté **d'App Access** pour ajouter une nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="551ee-315">Click the `+` sign next to **App Access** to add a new entry.</span></span>

    ![Image de l'accès aux applications de paramètre de configuration](images/tcc-add-entry.png)

9. <span data-ttu-id="551ee-317">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="551ee-317">Enter the following details:</span></span>

    - <span data-ttu-id="551ee-318">Identificateur : `com.microsoft.wdav.epsext`</span><span class="sxs-lookup"><span data-stu-id="551ee-318">Identifier: `com.microsoft.wdav.epsext`</span></span>
    - <span data-ttu-id="551ee-319">Type d'identificateur : ID d'offre groupée</span><span class="sxs-lookup"><span data-stu-id="551ee-319">Identifier Type: Bundle ID</span></span>
    - <span data-ttu-id="551ee-320">Conditions requises pour le code : `identifier "com.microsoft.wdav.epsext" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span><span class="sxs-lookup"><span data-stu-id="551ee-320">Code Requirement: `identifier "com.microsoft.wdav.epsext" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span></span>

10. <span data-ttu-id="551ee-321">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="551ee-321">Select **+ Add**.</span></span>

    ![Image de l'entrée tcc epsext du paramètre de configuration](images/tcc-epsext-entry.png)

    - <span data-ttu-id="551ee-323">Sous Application ou service : définir sur **SystemPolicyAllFiles**</span><span class="sxs-lookup"><span data-stu-id="551ee-323">Under App or service: Set to **SystemPolicyAllFiles**</span></span>

    - <span data-ttu-id="551ee-324">Sous « accès » : définir sur **Autoriser**</span><span class="sxs-lookup"><span data-stu-id="551ee-324">Under "access": Set to **Allow**</span></span>

11. <span data-ttu-id="551ee-325">Sélectionnez **Enregistrer** (et non celui en bas à droite).</span><span class="sxs-lookup"><span data-stu-id="551ee-325">Select **Save** (not the one at the bottom right).</span></span>

    ![Image du paramètre de configuration tcc epsext image2](images/tcc-epsext-entry2.png)

12. <span data-ttu-id="551ee-327">Sélectionnez **l'onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="551ee-327">Select the **Scope** tab.</span></span>

    ![Image de l'étendue du paramètre de configuration](images/2c49b16cd112729b3719724f581e6882.png)

13. <span data-ttu-id="551ee-329">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="551ee-329">Select **+ Add**.</span></span>

    ![Image de l'addimage du paramètre de configuration](images/57cef926d1b9260fb74a5f460cee887a.png)

14. <span data-ttu-id="551ee-331">Sélectionnez **Groupes d'ordinateurs** > **sous Nom** de groupe > sélectionnez Groupe MachineGroup de **Contoso.**</span><span class="sxs-lookup"><span data-stu-id="551ee-331">Select **Computer Groups** > under **Group Name** > select **Contoso's MachineGroup**.</span></span> 

    ![Image du paramètre de configuration contoso machinegrp](images/368d35b3d6179af92ffdbfd93b226b69.png)

15. <span data-ttu-id="551ee-333">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="551ee-333">Select **Add**.</span></span> 

16. <span data-ttu-id="551ee-334">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="551ee-334">Select **Save**.</span></span> 
    
17. <span data-ttu-id="551ee-335">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="551ee-335">Select **Done**.</span></span>
    
    ![Image de donimg de paramètre de configuration](images/809cef630281b64b8f07f20913b0039b.png)
    
    ![Image du paramètre de configuration donimg2](images/6c8b406ee224335a8c65d06953dc756e.png)

<span data-ttu-id="551ee-338">Vous pouvez également télécharger [fulldisk.mobileconfig](https://github.com/microsoft/mdatp-xplat/blob/master/macos/mobileconfig/profiles/fulldisk.mobileconfig) et le télécharger dans les profils de configuration JAMF comme décrit dans [Deploying Custom Configuration Profiles using Jamf Pro| Méthode 2 : Charger un profil de configuration sur Jamf Pro](https://www.jamf.com/jamf-nation/articles/648/deploying-custom-configuration-profiles-using-jamf-pro).</span><span class="sxs-lookup"><span data-stu-id="551ee-338">Alternatively, you can download [fulldisk.mobileconfig](https://github.com/microsoft/mdatp-xplat/blob/master/macos/mobileconfig/profiles/fulldisk.mobileconfig) and upload it to JAMF Configuration Profiles as described in [Deploying Custom Configuration Profiles using Jamf Pro|Method 2: Upload a Configuration Profile to Jamf Pro](https://www.jamf.com/jamf-nation/articles/648/deploying-custom-configuration-profiles-using-jamf-pro).</span></span>

## <a name="step-7-approve-kernel-extension-for-microsoft-defender-for-endpoint"></a><span data-ttu-id="551ee-339">Étape 7 : Approuver l'extension de noyau pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="551ee-339">Step 7: Approve Kernel extension for Microsoft Defender for Endpoint</span></span>

> [!CAUTION]
> <span data-ttu-id="551ee-340">Les appareils Apple Silicon (M1) ne supportent pas KEXT.</span><span class="sxs-lookup"><span data-stu-id="551ee-340">Apple Silicon (M1) devices do not support KEXT.</span></span> <span data-ttu-id="551ee-341">L'installation d'un profil de configuration constitué de stratégies KEXT échoue sur ces appareils.</span><span class="sxs-lookup"><span data-stu-id="551ee-341">Installation of a configuration profile consisting KEXT policies will fail on these devices.</span></span>

1. <span data-ttu-id="551ee-342">Dans les **profils de configuration,** **sélectionnez + Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="551ee-342">In the **Configuration Profiles**, select **+ New**.</span></span>

    ![Capture d'écran d'un billet de réseau social Description généré automatiquement](images/6c8b406ee224335a8c65d06953dc756e.png)

2. <span data-ttu-id="551ee-344">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="551ee-344">Enter the following details:</span></span>

    <span data-ttu-id="551ee-345">**Général**</span><span class="sxs-lookup"><span data-stu-id="551ee-345">**General**</span></span> 
    
    - <span data-ttu-id="551ee-346">Name: MDATP MDAV Kernel Extension</span><span class="sxs-lookup"><span data-stu-id="551ee-346">Name: MDATP MDAV Kernel Extension</span></span>
    - <span data-ttu-id="551ee-347">Description : extension de noyau MDATP (kext)</span><span class="sxs-lookup"><span data-stu-id="551ee-347">Description: MDATP kernel extension (kext)</span></span>
    - <span data-ttu-id="551ee-348">Catégorie : Aucun</span><span class="sxs-lookup"><span data-stu-id="551ee-348">Category: None</span></span>
    - <span data-ttu-id="551ee-349">Méthode de distribution : installer automatiquement</span><span class="sxs-lookup"><span data-stu-id="551ee-349">Distribution Method: Install Automatically</span></span>
    - <span data-ttu-id="551ee-350">Niveau : niveau ordinateur</span><span class="sxs-lookup"><span data-stu-id="551ee-350">Level: Computer Level</span></span>

    ![Image du noyau mdatpmdav des paramètres de configuration](images/24e290f5fc309932cf41f3a280d22c14.png)

3. <span data-ttu-id="551ee-352">In **Configure Approved Kernel Extensions** select **Configure**.</span><span class="sxs-lookup"><span data-stu-id="551ee-352">In **Configure Approved Kernel Extensions** select **Configure**.</span></span>

    ![Image de l'ext de noyau approuvé des paramètres de configuration](images/30be88b63abc5e8dde11b73f1b1ade6a.png)

   
4. <span data-ttu-id="551ee-354">Dans **Extensions de noyau approuvées,** entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="551ee-354">In **Approved Kernel Extensions** Enter the following details:</span></span>

    - <span data-ttu-id="551ee-355">Nom complet : Microsoft Corp.</span><span class="sxs-lookup"><span data-stu-id="551ee-355">Display Name: Microsoft Corp.</span></span>
    - <span data-ttu-id="551ee-356">ID d'équipe : UBF8T346G9</span><span class="sxs-lookup"><span data-stu-id="551ee-356">Team ID: UBF8T346G9</span></span>

    ![Image de l'extension de noyau appr des paramètres de configuration](images/39cf120d3ac3652292d8d1b6d057bd60.png)

5. <span data-ttu-id="551ee-358">Sélectionnez **l'onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="551ee-358">Select the **Scope** tab.</span></span>

    ![Image de l'onglet d'étendue des paramètres de configuration img](images/0df36fc308ba569db204ee32db3fb40a.png)

6. <span data-ttu-id="551ee-360">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="551ee-360">Select **+ Add**.</span></span>

7. <span data-ttu-id="551ee-361">Sélectionnez **Groupes d'ordinateurs** > **sous Nom** du > sélectionnez Groupe ordinateur de **Contoso.**</span><span class="sxs-lookup"><span data-stu-id="551ee-361">Select **Computer Groups** > under **Group Name** > select **Contoso's Machine Group**.</span></span>

8. <span data-ttu-id="551ee-362">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="551ee-362">Select **+ Add**.</span></span>

    ![Image des paramètres de configuration pour ajouter des images](images/0dde8a4c41110dbc398c485433a81359.png)

9. <span data-ttu-id="551ee-364">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="551ee-364">Select **Save**.</span></span>

    ![Image de l'économiserie des paramètres de configuration](images/0add8019b85a453b47fa5c402c72761b.png)

10. <span data-ttu-id="551ee-366">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="551ee-366">Select **Done**.</span></span>

    ![Image des paramètres de configuration doneimag](images/1c9bd3f68db20b80193dac18f33c22d0.png)

<span data-ttu-id="551ee-368">Vous pouvez également télécharger [kext.mobileconfig](https://github.com/microsoft/mdatp-xplat/blob/master/macos/mobileconfig/profiles/kext.mobileconfig) et le télécharger dans les profils de configuration JAMF comme décrit dans [Deploying Custom Configuration Profiles using Jamf Pro| Méthode 2 : Charger un profil de configuration sur Jamf Pro](https://www.jamf.com/jamf-nation/articles/648/deploying-custom-configuration-profiles-using-jamf-pro).</span><span class="sxs-lookup"><span data-stu-id="551ee-368">Alternatively, you can download [kext.mobileconfig](https://github.com/microsoft/mdatp-xplat/blob/master/macos/mobileconfig/profiles/kext.mobileconfig) and upload it to JAMF Configuration Profiles as described in [Deploying Custom Configuration Profiles using Jamf Pro|Method 2: Upload a Configuration Profile to Jamf Pro](https://www.jamf.com/jamf-nation/articles/648/deploying-custom-configuration-profiles-using-jamf-pro).</span></span>

## <a name="step-8-approve-system-extensions-for-microsoft-defender-for-endpoint"></a><span data-ttu-id="551ee-369">Étape 8 : Approuver les extensions système pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="551ee-369">Step 8: Approve System extensions for Microsoft Defender for Endpoint</span></span>

1. <span data-ttu-id="551ee-370">Dans les **profils de configuration,** **sélectionnez + Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="551ee-370">In the **Configuration Profiles**, select **+ New**.</span></span>

    ![Capture d'écran d'un billet de réseau social Description généré automatiquement](images/6c8b406ee224335a8c65d06953dc756e.png)

2. <span data-ttu-id="551ee-372">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="551ee-372">Enter the following details:</span></span>

    <span data-ttu-id="551ee-373">**Général**</span><span class="sxs-lookup"><span data-stu-id="551ee-373">**General**</span></span>
    
    - <span data-ttu-id="551ee-374">Name: MDATP MDAV System Extensions</span><span class="sxs-lookup"><span data-stu-id="551ee-374">Name: MDATP MDAV System Extensions</span></span>
    - <span data-ttu-id="551ee-375">Description : extensions système MDATP</span><span class="sxs-lookup"><span data-stu-id="551ee-375">Description: MDATP system extensions</span></span>
    - <span data-ttu-id="551ee-376">Catégorie : Aucun</span><span class="sxs-lookup"><span data-stu-id="551ee-376">Category: None</span></span>
    - <span data-ttu-id="551ee-377">Méthode de distribution : installer automatiquement</span><span class="sxs-lookup"><span data-stu-id="551ee-377">Distribution Method: Install Automatically</span></span>
    - <span data-ttu-id="551ee-378">Niveau : niveau ordinateur</span><span class="sxs-lookup"><span data-stu-id="551ee-378">Level: Computer Level</span></span>

    ![Image du nouveau prof des paramètres de configuration](images/sysext-new-profile.png)

3. <span data-ttu-id="551ee-380">Dans **les extensions système,** **sélectionnez Configurer.**</span><span class="sxs-lookup"><span data-stu-id="551ee-380">In **System Extensions** select **Configure**.</span></span>

   ![Image de configuration sysext des paramètres de configuration](images/sysext-configure.png)

4. <span data-ttu-id="551ee-382">Dans **les extensions système,** entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="551ee-382">In **System Extensions** enter the following details:</span></span>

   - <span data-ttu-id="551ee-383">Nom complet : Microsoft Corp. System Extensions</span><span class="sxs-lookup"><span data-stu-id="551ee-383">Display Name: Microsoft Corp. System Extensions</span></span>
   - <span data-ttu-id="551ee-384">Types d'extension système : extensions système autorisées</span><span class="sxs-lookup"><span data-stu-id="551ee-384">System Extension Types: Allowed System Extensions</span></span>
   - <span data-ttu-id="551ee-385">Identificateur d'équipe : UBF8T346G9</span><span class="sxs-lookup"><span data-stu-id="551ee-385">Team Identifier: UBF8T346G9</span></span>
   - <span data-ttu-id="551ee-386">Extensions système autorisées :</span><span class="sxs-lookup"><span data-stu-id="551ee-386">Allowed System Extensions:</span></span>
     - <span data-ttu-id="551ee-387">**com.microsoft.wdav.epsext**</span><span class="sxs-lookup"><span data-stu-id="551ee-387">**com.microsoft.wdav.epsext**</span></span>
     - <span data-ttu-id="551ee-388">**com.microsoft.wdav.netext**</span><span class="sxs-lookup"><span data-stu-id="551ee-388">**com.microsoft.wdav.netext**</span></span>

    ![Image des paramètres de configuration sysextconfig2](images/sysext-configure2.png)

5. <span data-ttu-id="551ee-390">Sélectionnez **l'onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="551ee-390">Select the **Scope** tab.</span></span>

    ![Image de l'étendue des paramètres de configuration](images/0df36fc308ba569db204ee32db3fb40a.png)

6. <span data-ttu-id="551ee-392">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="551ee-392">Select **+ Add**.</span></span>

7. <span data-ttu-id="551ee-393">Sélectionnez **Groupes d'ordinateurs** > **sous Nom du** > sélectionnez Groupe ordinateur de **Contoso.**</span><span class="sxs-lookup"><span data-stu-id="551ee-393">Select **Computer Groups** > under **Group Name** > select **Contoso's Machine Group**.</span></span>

8. <span data-ttu-id="551ee-394">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="551ee-394">Select **+ Add**.</span></span>

   ![Image de l'addima des paramètres de configuration](images/0dde8a4c41110dbc398c485433a81359.png)

9. <span data-ttu-id="551ee-396">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="551ee-396">Select **Save**.</span></span>

   ![Image de l'étendue sysext des paramètres de configuration](images/sysext-scope.png)

10. <span data-ttu-id="551ee-398">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="551ee-398">Select **Done**.</span></span>

    ![Image des paramètres de configuration sysext-final](images/sysext-final.png)

## <a name="step-9-configure-network-extension"></a><span data-ttu-id="551ee-400">Étape 9 : Configurer l'extension réseau</span><span class="sxs-lookup"><span data-stu-id="551ee-400">Step 9: Configure Network Extension</span></span>

<span data-ttu-id="551ee-401">Dans le cadre des fonctionnalités de détection et de réponse des points de terminaison, Microsoft Defender for Endpoint sur macOS inspecte le trafic de socket et signale ces informations au portail centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="551ee-401">As part of the Endpoint Detection and Response capabilities, Microsoft Defender for Endpoint on macOS inspects socket traffic and reports this information to the Microsoft Defender Security Center portal.</span></span> <span data-ttu-id="551ee-402">La stratégie suivante permet à l'extension réseau d'effectuer cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="551ee-402">The following policy allows the network extension to perform this functionality.</span></span>

<span data-ttu-id="551ee-403">Ces étapes s'appliquent à macOS 10.15 (Genre), ou une nouveauté.</span><span class="sxs-lookup"><span data-stu-id="551ee-403">These steps are applicable of macOS 10.15 (Catalina) or newer.</span></span>

1. <span data-ttu-id="551ee-404">Dans le tableau de bord Jamf Pro, sélectionnez **Ordinateurs,** puis **Profils de configuration.**</span><span class="sxs-lookup"><span data-stu-id="551ee-404">In the Jamf Pro dashboard, select **Computers**, then **Configuration Profiles**.</span></span>

2. <span data-ttu-id="551ee-405">Cliquez **sur** Nouveau, puis entrez les détails suivants pour **options**:</span><span class="sxs-lookup"><span data-stu-id="551ee-405">Click **New**, and enter the following details for **Options**:</span></span>

    - <span data-ttu-id="551ee-406">Onglet **Général**:</span><span class="sxs-lookup"><span data-stu-id="551ee-406">Tab **General**:</span></span> 
        - <span data-ttu-id="551ee-407">**Nom**: Extension réseau Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="551ee-407">**Name**: Microsoft Defender ATP Network Extension</span></span>
        - <span data-ttu-id="551ee-408">**Description**: macOS 10.15 (Contrôle) ou une nouveauté</span><span class="sxs-lookup"><span data-stu-id="551ee-408">**Description**: macOS 10.15 (Catalina) or newer</span></span>
        - <span data-ttu-id="551ee-409">**Catégorie**: Aucun *(par défaut)*</span><span class="sxs-lookup"><span data-stu-id="551ee-409">**Category**: None *(default)*</span></span>
        - <span data-ttu-id="551ee-410">**Méthode de distribution**: installer automatiquement *(par défaut)*</span><span class="sxs-lookup"><span data-stu-id="551ee-410">**Distribution Method**: Install Automatically *(default)*</span></span>
        - <span data-ttu-id="551ee-411">**Niveau**: niveau ordinateur *(par défaut)*</span><span class="sxs-lookup"><span data-stu-id="551ee-411">**Level**: Computer Level *(default)*</span></span>

    - <span data-ttu-id="551ee-412">Filtre **de contenu d'onglet**:</span><span class="sxs-lookup"><span data-stu-id="551ee-412">Tab **Content Filter**:</span></span>
        - <span data-ttu-id="551ee-413">**Nom du** filtre : filtre de contenu Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="551ee-413">**Filter Name**: Microsoft Defender ATP Content Filter</span></span>
        - <span data-ttu-id="551ee-414">**Identificateur**: `com.microsoft.wdav`</span><span class="sxs-lookup"><span data-stu-id="551ee-414">**Identifier**: `com.microsoft.wdav`</span></span>
        - <span data-ttu-id="551ee-415">Laisser **l'adresse du service,** **l'organisation,** **le nom d'utilisateur,** le mot de **passe,** **le certificat** vide (**Inclure** *n'est pas* sélectionné)</span><span class="sxs-lookup"><span data-stu-id="551ee-415">Leave **Service Address**, **Organization**, **User Name**, **Password**, **Certificate** blank (**Include** is *not* selected)</span></span>
        - <span data-ttu-id="551ee-416">**Filter Order**: Inspector</span><span class="sxs-lookup"><span data-stu-id="551ee-416">**Filter Order**: Inspector</span></span>
        - <span data-ttu-id="551ee-417">**Filtre de socket**: `com.microsoft.wdav.netext`</span><span class="sxs-lookup"><span data-stu-id="551ee-417">**Socket Filter**: `com.microsoft.wdav.netext`</span></span>
        - <span data-ttu-id="551ee-418">**Exigence désignée par le filtre de socket**: `identifier "com.microsoft.wdav.netext" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span><span class="sxs-lookup"><span data-stu-id="551ee-418">**Socket Filter Designated Requirement**: `identifier "com.microsoft.wdav.netext" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span></span>
        - <span data-ttu-id="551ee-419">Laisser **les champs Filtre réseau** vides **(Inclure** *n'est pas* sélectionné)</span><span class="sxs-lookup"><span data-stu-id="551ee-419">Leave **Network Filter** fields blank (**Include** is *not* selected)</span></span>

        <span data-ttu-id="551ee-420">Notez que **l'identificateur,** le filtre de **socket** et le **filtre de socket désignent** les valeurs exactes requises comme spécifié ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="551ee-420">Note that **Identifier**, **Socket Filter** and **Socket Filter Designated Requirement** exact values as specified above.</span></span>

        ![Image du paramètre de configuration mdatpmdav](images/netext-create-profile.png)

3. <span data-ttu-id="551ee-422">Sélectionnez **l'onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="551ee-422">Select the **Scope** tab.</span></span>

   ![Image de l'onglet système des paramètres de configuration](images/0df36fc308ba569db204ee32db3fb40a.png)

4. <span data-ttu-id="551ee-424">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="551ee-424">Select **+ Add**.</span></span>

5. <span data-ttu-id="551ee-425">Sélectionnez **Groupes d'ordinateurs** > **sous Nom** du > sélectionnez Groupe ordinateur de **Contoso.**</span><span class="sxs-lookup"><span data-stu-id="551ee-425">Select **Computer Groups** > under **Group Name** > select **Contoso's Machine Group**.</span></span>

6. <span data-ttu-id="551ee-426">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="551ee-426">Select **+ Add**.</span></span>

    ![Image des paramètres de configuration adim](images/0dde8a4c41110dbc398c485433a81359.png)

7. <span data-ttu-id="551ee-428">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="551ee-428">Select **Save**.</span></span>

    ![Image des paramètres de configuration savimg netextscop](images/netext-scope.png)

8. <span data-ttu-id="551ee-430">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="551ee-430">Select **Done**.</span></span>

    ![Image de paramètres de configuration netextfinal](images/netext-final.png)

<span data-ttu-id="551ee-432">Vous pouvez également télécharger [netfilter.mobileconfig](https://github.com/microsoft/mdatp-xplat/blob/master/macos/mobileconfig/profiles/netfilter.mobileconfig) et le télécharger dans les profils de configuration JAMF comme décrit dans [Deploying Custom Configuration Profiles using Jamf Pro| Méthode 2 : Charger un profil de configuration sur Jamf Pro](https://www.jamf.com/jamf-nation/articles/648/deploying-custom-configuration-profiles-using-jamf-pro).</span><span class="sxs-lookup"><span data-stu-id="551ee-432">Alternatively, you can download [netfilter.mobileconfig](https://github.com/microsoft/mdatp-xplat/blob/master/macos/mobileconfig/profiles/netfilter.mobileconfig) and upload it to JAMF Configuration Profiles as described in [Deploying Custom Configuration Profiles using Jamf Pro|Method 2: Upload a Configuration Profile to Jamf Pro](https://www.jamf.com/jamf-nation/articles/648/deploying-custom-configuration-profiles-using-jamf-pro).</span></span>

## <a name="step-10-schedule-scans-with-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="551ee-433">Étape 10 : Planifier des analyses avec Microsoft Defender pour Endpoint sur macOS</span><span class="sxs-lookup"><span data-stu-id="551ee-433">Step 10: Schedule scans with Microsoft Defender for Endpoint on macOS</span></span>
<span data-ttu-id="551ee-434">Suivez les instructions des [analyses de planification avec Microsoft Defender for Endpoint sur macOS.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/mac-schedule-scan-atp)</span><span class="sxs-lookup"><span data-stu-id="551ee-434">Follow the instructions on [Schedule scans with Microsoft Defender for Endpoint on macOS](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/mac-schedule-scan-atp).</span></span>

## <a name="step-11-deploy-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="551ee-435">Étape 11 : Déployer Microsoft Defender pour endpoint sur macOS</span><span class="sxs-lookup"><span data-stu-id="551ee-435">Step 11: Deploy Microsoft Defender for Endpoint on macOS</span></span>

1. <span data-ttu-id="551ee-436">Accédez à l'endroit où vous avez `wdav.pkg` enregistré.</span><span class="sxs-lookup"><span data-stu-id="551ee-436">Navigate to where you saved `wdav.pkg`.</span></span>

    ![Image de l'explorateur de fichiers wdav pkg](images/8dde76b5463047423f8637c86b05c29d.png)

2. <span data-ttu-id="551ee-438">Renommons-le `wdav_MDM_Contoso_200329.pkg` .</span><span class="sxs-lookup"><span data-stu-id="551ee-438">Rename it to `wdav_MDM_Contoso_200329.pkg`.</span></span>

    ![Image de l'explorateur de fichiers 1 wdavmdmpkg](images/fb2220fed3a530f4b3ef36f600da0c27.png)

3. <span data-ttu-id="551ee-440">Ouvrez le tableau de bord Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="551ee-440">Open the Jamf Pro dashboard.</span></span>

    ![Image des paramètres de configuration jamfpro](images/990742cd9a15ca9fdd37c9f695d1b9f4.png)

4. <span data-ttu-id="551ee-442">Sélectionnez votre ordinateur et cliquez sur l'icône d'engrenage en haut, puis **sélectionnez Gestion de l'ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="551ee-442">Select your computer and click the gear icon at the top, then select **Computer Management**.</span></span>

    ![Image des paramètres de configuration compmgmt](images/b6d671b2f18b89d96c1c8e2ea1991242.png)

5. <span data-ttu-id="551ee-444">Dans **les packages,** **sélectionnez + Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="551ee-444">In **Packages**, select **+ New**.</span></span> 
    <span data-ttu-id="551ee-445">![Une image contenant une description d'volatile a généré automatiquement un nouveau package](images/57aa4d21e2ccc65466bf284701d4e961.png)</span><span class="sxs-lookup"><span data-stu-id="551ee-445">![A picture containing bird Description automatically generated package new](images/57aa4d21e2ccc65466bf284701d4e961.png)</span></span>

6. <span data-ttu-id="551ee-446">Dans **le nouveau package,** entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="551ee-446">In **New Package** Enter the following details:</span></span>

    <span data-ttu-id="551ee-447">**Onglet Général**</span><span class="sxs-lookup"><span data-stu-id="551ee-447">**General tab**</span></span>
    - <span data-ttu-id="551ee-448">Nom complet : laissez-le vide pour le moment.</span><span class="sxs-lookup"><span data-stu-id="551ee-448">Display Name: Leave it blank for now.</span></span> <span data-ttu-id="551ee-449">Parce qu'il sera réinitialisé lorsque vous choisirez votre pkg.</span><span class="sxs-lookup"><span data-stu-id="551ee-449">Because it will be reset when you choose your pkg.</span></span>
    - <span data-ttu-id="551ee-450">Catégorie : Aucun (par défaut)</span><span class="sxs-lookup"><span data-stu-id="551ee-450">Category: None (default)</span></span>
    - <span data-ttu-id="551ee-451">Filename: Choose File</span><span class="sxs-lookup"><span data-stu-id="551ee-451">Filename: Choose File</span></span>

    ![Image de l'onglet Général des paramètres de configuration](images/21de3658bf58b1b767a17358a3f06341.png)

    <span data-ttu-id="551ee-453">Ouvrez le fichier et pointer vers `wdav.pkg` ou `wdav_MDM_Contoso_200329.pkg` .</span><span class="sxs-lookup"><span data-stu-id="551ee-453">Open the file and point it to `wdav.pkg` or `wdav_MDM_Contoso_200329.pkg`.</span></span>
    
    ![Capture d'écran d'une description d'ordinateur générée automatiquement](images/1aa5aaa0a387f4e16ce55b66facc77d1.png)

7. <span data-ttu-id="551ee-455">Sélectionnez **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="551ee-455">Select **Open**.</span></span> <span data-ttu-id="551ee-456">Définissez **le nom complet sur** Microsoft Defender - Protection avancée contre les **menaces et Antivirus Microsoft Defender.**</span><span class="sxs-lookup"><span data-stu-id="551ee-456">Set the **Display Name** to **Microsoft Defender Advanced Threat Protection and Microsoft Defender Antivirus**.</span></span>

    <span data-ttu-id="551ee-457">**Le fichier manifeste n'est** pas requis.</span><span class="sxs-lookup"><span data-stu-id="551ee-457">**Manifest File** is not required.</span></span> <span data-ttu-id="551ee-458">Microsoft Defender - Protection avancée contre les menaces fonctionne sans fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="551ee-458">Microsoft Defender Advanced Threat Protection works without Manifest File.</span></span>
    
    <span data-ttu-id="551ee-459">**Onglet Options**</span><span class="sxs-lookup"><span data-stu-id="551ee-459">**Options tab**</span></span><br> <span data-ttu-id="551ee-460">Conservez les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="551ee-460">Keep default values.</span></span>

    <span data-ttu-id="551ee-461">**Onglet Limitations**</span><span class="sxs-lookup"><span data-stu-id="551ee-461">**Limitations tab**</span></span><br> <span data-ttu-id="551ee-462">Conservez les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="551ee-462">Keep default values.</span></span>
    
     ![Image de l'onglet limitation des paramètres de configuration](images/56dac54634d13b2d3948ab50e8d3ef21.png)
   
8. <span data-ttu-id="551ee-464">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="551ee-464">Select **Save**.</span></span> <span data-ttu-id="551ee-465">Le package est téléchargé vers Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="551ee-465">The package is uploaded to Jamf Pro.</span></span> 

   ![Image des paramètres de configuration pack upl jamf pro](images/33f1ecdc7d4872555418bbc3efe4b7a3.png)

   <span data-ttu-id="551ee-467">Le déploiement du package peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="551ee-467">It can take a few minutes for the package to be available for deployment.</span></span>
   
   ![Image de l'upl du pack de paramètres de configuration](images/1626d138e6309c6e87bfaab64f5ccf7b.png)

9. <span data-ttu-id="551ee-469">Accédez à la page **Stratégies.**</span><span class="sxs-lookup"><span data-stu-id="551ee-469">Navigate to the **Policies** page.</span></span>

    ![Image des paramètres de configuration des locations](images/f878f8efa5ebc92d069f4b8f79f62c7f.png)

10. <span data-ttu-id="551ee-471">Sélectionnez **+ Nouveau** pour créer une stratégie.</span><span class="sxs-lookup"><span data-stu-id="551ee-471">Select **+ New** to create a new policy.</span></span>

    ![Image de la nouvelle stratégie des paramètres de configuration](images/847b70e54ed04787e415f5180414b310.png)


11. <span data-ttu-id="551ee-473">En **général,** entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="551ee-473">In **General** Enter the following details:</span></span>

    - <span data-ttu-id="551ee-474">Nom complet : Intégration MDATP Contoso 200329 v100.86.92 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="551ee-474">Display name: MDATP Onboarding Contoso 200329 v100.86.92 or later</span></span>

    ![<span data-ttu-id="551ee-475">Image de configuration settingsmdatponboard</span><span class="sxs-lookup"><span data-stu-id="551ee-475">Image of configuration settingsmdatponboard</span></span> ](images/625ba6d19e8597f05e4907298a454d28.png)

12. <span data-ttu-id="551ee-476">Sélectionnez **l'enregistrement périodique.**</span><span class="sxs-lookup"><span data-stu-id="551ee-476">Select **Recurring Check-in**.</span></span> 
    
    ![Image de vérification des paramètres de configuration](images/68bdbc5754dfc80aa1a024dde0fce7b0.png)

  
13. <span data-ttu-id="551ee-478">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="551ee-478">Select **Save**.</span></span> 
 
14. <span data-ttu-id="551ee-479">Sélectionnez **packages > configurer**.</span><span class="sxs-lookup"><span data-stu-id="551ee-479">Select **Packages > Configure**.</span></span>
 
    ![Image du pack de paramètres de configuration configuré](images/8fb4cc03721e1efb4a15867d5241ebfb.png)

15. <span data-ttu-id="551ee-481">Sélectionnez **le bouton** Ajouter en haut de Microsoft Defender - Protection avancée contre les **menaces et antivirus Microsoft Defender.**</span><span class="sxs-lookup"><span data-stu-id="551ee-481">Select the **Add** button next to **Microsoft Defender Advanced Threat Protection and Microsoft Defender Antivirus**.</span></span>

    ![Image des paramètres de configuration ajoutés par MDATP et MDA](images/526b83fbdbb31265b3d0c1e5fbbdc33a.png)

16. <span data-ttu-id="551ee-483">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="551ee-483">Select **Save**.</span></span>

    ![Image de configuration settingssavimg](images/9d6e5386e652e00715ff348af72671c6.png)

17. <span data-ttu-id="551ee-485">Sélectionnez **l'onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="551ee-485">Select the **Scope** tab.</span></span>  

    ![Image de scptab des paramètres de configuration](images/8d80fe378a31143db9be0bacf7ddc5a3.png)

18. <span data-ttu-id="551ee-487">Sélectionnez les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="551ee-487">Select the target computers.</span></span>

    ![Image des paramètres de configuration tgtcomp](images/6eda18a64a660fa149575454e54e7156.png)

    <span data-ttu-id="551ee-489">**Scope**</span><span class="sxs-lookup"><span data-stu-id="551ee-489">**Scope**</span></span>
    
    <span data-ttu-id="551ee-490">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="551ee-490">Select **Add**.</span></span>
    
    ![Image des paramètres de configuration ad1img](images/1c08d097829863778d562c10c5f92b67.png)

    ![Image des paramètres de configuration ad2img](images/216253cbfb6ae738b9f13496b9c799fd.png)

    <span data-ttu-id="551ee-493">**Libre-service**</span><span class="sxs-lookup"><span data-stu-id="551ee-493">**Self-Service**</span></span>
    
    ![Image du libre-service des paramètres de configuration](images/c9f85bba3e96d627fe00fc5a8363b83a.png)

19. <span data-ttu-id="551ee-495">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="551ee-495">Select **Done**.</span></span> 

    ![Image des paramètres de configuration do1img](images/99679a7835b0d27d0a222bc3fdaf7f3b.png)

    ![Image des paramètres de configuration do2img](images/632aaab79ae18d0d2b8e0c16b6ba39e2.png)




