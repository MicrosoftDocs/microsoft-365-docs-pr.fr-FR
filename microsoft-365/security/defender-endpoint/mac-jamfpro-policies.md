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
ms.openlocfilehash: 1559d8dca6b6909f22473c5a8f4d25d4bac501d1
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51062254"
---
# <a name="set-up-the-microsoft-defender-for-endpoint-for-macos-policies-in-jamf-pro"></a><span data-ttu-id="97e35-104">Configurer microsoft Defender pour le point de terminaison pour les stratégies macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="97e35-104">Set up the Microsoft Defender for Endpoint for macOS policies in Jamf Pro</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="97e35-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="97e35-105">**Applies to:**</span></span>

- [<span data-ttu-id="97e35-106">Defender pour point de terminaison pour Mac</span><span class="sxs-lookup"><span data-stu-id="97e35-106">Defender for Endpoint for Mac</span></span>](microsoft-defender-endpoint-mac.md)

<span data-ttu-id="97e35-107">Cette page vous guide à travers les étapes à suivre pour configurer des stratégies macOS dans Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="97e35-107">This page will guide you through the steps you need to take to set up macOS policies in Jamf Pro.</span></span>

<span data-ttu-id="97e35-108">Vous devez suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="97e35-108">You'll need to take the following steps:</span></span>

1. [<span data-ttu-id="97e35-109">Obtenir le package d’intégration De Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="97e35-109">Get the Microsoft Defender for Endpoint onboarding package</span></span>](#step-1-get-the-microsoft-defender-for-endpoint-onboarding-package)

2. [<span data-ttu-id="97e35-110">Créer un profil de configuration dans Jamf Pro à l’aide du package d’intégration</span><span class="sxs-lookup"><span data-stu-id="97e35-110">Create a configuration profile in Jamf Pro using the onboarding package</span></span>](#step-2-create-a-configuration-profile-in-jamf-pro-using-the-onboarding-package)

3. [<span data-ttu-id="97e35-111">Configurer les paramètres de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="97e35-111">Configure Microsoft Defender for Endpoint settings</span></span>](#step-3-configure-microsoft-defender-for-endpoint-settings)

4. [<span data-ttu-id="97e35-112">Configurer les paramètres de notification microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="97e35-112">Configure Microsoft Defender for Endpoint notification settings</span></span>](#step-4-configure-notifications-settings)

5. [<span data-ttu-id="97e35-113">Configurer la mise à jour automatique Microsoft (AutoUpdate)</span><span class="sxs-lookup"><span data-stu-id="97e35-113">Configure Microsoft AutoUpdate (MAU)</span></span>](#step-5-configure-microsoft-autoupdate-mau)

6. [<span data-ttu-id="97e35-114">Accorder un accès disque complet à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="97e35-114">Grant full disk access to Microsoft Defender for Endpoint</span></span>](#step-6-grant-full-disk-access-to-microsoft-defender-for-endpoint)

7. [<span data-ttu-id="97e35-115">Approuver l’extension de noyau pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="97e35-115">Approve Kernel extension for Microsoft Defender for Endpoint</span></span>](#step-7-approve-kernel-extension-for-microsoft-defender-for-endpoint)

8. [<span data-ttu-id="97e35-116">Approuver les extensions système pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="97e35-116">Approve System extensions for Microsoft Defender for Endpoint</span></span>](#step-8-approve-system-extensions-for-microsoft-defender-for-endpoint)

9. [<span data-ttu-id="97e35-117">Configurer l’extension réseau</span><span class="sxs-lookup"><span data-stu-id="97e35-117">Configure Network Extension</span></span>](#step-9-configure-network-extension)

10. [<span data-ttu-id="97e35-118">Planifier des analyses avec Microsoft Defender pour Endpoint pour Mac</span><span class="sxs-lookup"><span data-stu-id="97e35-118">Schedule scans with Microsoft Defender for Endpoint for Mac</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/mac-schedule-scan-atp)

11. [<span data-ttu-id="97e35-119">Déployer Microsoft Defender pour le point de terminaison pour macOS</span><span class="sxs-lookup"><span data-stu-id="97e35-119">Deploy Microsoft Defender for Endpoint for macOS</span></span>](#step-11-deploy-microsoft-defender-for-endpoint-for-macos)


## <a name="step-1-get-the-microsoft-defender-for-endpoint-onboarding-package"></a><span data-ttu-id="97e35-120">Étape 1 : Obtenir le package d’intégration De Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="97e35-120">Step 1: Get the Microsoft Defender for Endpoint onboarding package</span></span>

1. <span data-ttu-id="97e35-121">Dans [le Centre de sécurité Microsoft Defender,](https://securitycenter.microsoft.com )accédez à **Paramètres >'intégration.**</span><span class="sxs-lookup"><span data-stu-id="97e35-121">In [Microsoft Defender Security Center](https://securitycenter.microsoft.com ), navigate to **Settings > Onboarding**.</span></span> 

2. <span data-ttu-id="97e35-122">Sélectionnez macOS comme système d’exploitation et Gestion des périphériques mobiles/Microsoft Intune comme méthode de déploiement.</span><span class="sxs-lookup"><span data-stu-id="97e35-122">Select macOS as the operating system and Mobile Device Management / Microsoft Intune as the deployment method.</span></span>

    ![Image du Centre de sécurité Microsoft Defender](images/onboarding-macos.png)

3. <span data-ttu-id="97e35-124">Sélectionnez **Télécharger le package d’intégration** (WindowsDefenderATPOnboardingPackage.zip).</span><span class="sxs-lookup"><span data-stu-id="97e35-124">Select **Download onboarding package** (WindowsDefenderATPOnboardingPackage.zip).</span></span>

4. <span data-ttu-id="97e35-125">Extraire `WindowsDefenderATPOnboardingPackage.zip` .</span><span class="sxs-lookup"><span data-stu-id="97e35-125">Extract `WindowsDefenderATPOnboardingPackage.zip`.</span></span>

5. <span data-ttu-id="97e35-126">Copiez le fichier à votre emplacement préféré.</span><span class="sxs-lookup"><span data-stu-id="97e35-126">Copy the file to your preferred location.</span></span> <span data-ttu-id="97e35-127">Par exemple : `C:\Users\JaneDoe_or_JohnDoe.contoso\Downloads\WindowsDefenderATPOnboardingPackage_macOS_MDM_contoso\jamf\WindowsDefenderATPOnboarding.plist`.</span><span class="sxs-lookup"><span data-stu-id="97e35-127">For example,  `C:\Users\JaneDoe_or_JohnDoe.contoso\Downloads\WindowsDefenderATPOnboardingPackage_macOS_MDM_contoso\jamf\WindowsDefenderATPOnboarding.plist`.</span></span>


## <a name="step-2-create-a-configuration-profile-in-jamf-pro-using-the-onboarding-package"></a><span data-ttu-id="97e35-128">Étape 2 : Créer un profil de configuration dans Jamf Pro à l’aide du package d’intégration</span><span class="sxs-lookup"><span data-stu-id="97e35-128">Step 2: Create a configuration profile in Jamf Pro using the onboarding package</span></span>

1. <span data-ttu-id="97e35-129">Recherchez le `WindowsDefenderATPOnboarding.plist` fichier dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="97e35-129">Locate the file `WindowsDefenderATPOnboarding.plist` from the previous section.</span></span>

   ![Image du fichier WindowsDefenderATPOnboarding](images/plist-onboarding-file.png)

 
2. <span data-ttu-id="97e35-131">Dans le tableau de bord Jamf Pro, sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="97e35-131">In the Jamf Pro dashboard, select **New**.</span></span>

    ![Image de création d’un tableau de bord Jamf Pro](images/jamf-pro-configure-profile.png)

3. <span data-ttu-id="97e35-133">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="97e35-133">Enter the following details:</span></span>

   <span data-ttu-id="97e35-134">**Général**</span><span class="sxs-lookup"><span data-stu-id="97e35-134">**General**</span></span>
   - <span data-ttu-id="97e35-135">Nom : intégration MDATP pour macOS</span><span class="sxs-lookup"><span data-stu-id="97e35-135">Name: MDATP onboarding for macOS</span></span>
   - <span data-ttu-id="97e35-136">Description : intégration EDR MDATP pour macOS</span><span class="sxs-lookup"><span data-stu-id="97e35-136">Description: MDATP EDR onboarding for macOS</span></span>
   - <span data-ttu-id="97e35-137">Catégorie : Aucun</span><span class="sxs-lookup"><span data-stu-id="97e35-137">Category: None</span></span>
   - <span data-ttu-id="97e35-138">Méthode de distribution : installer automatiquement</span><span class="sxs-lookup"><span data-stu-id="97e35-138">Distribution Method: Install Automatically</span></span>
   - <span data-ttu-id="97e35-139">Niveau : niveau ordinateur</span><span class="sxs-lookup"><span data-stu-id="97e35-139">Level: Computer Level</span></span>

4. <span data-ttu-id="97e35-140">In **Application & Custom Settings** select **Configure**.</span><span class="sxs-lookup"><span data-stu-id="97e35-140">In **Application & Custom Settings** select **Configure**.</span></span>

    ![Image de configuration de l’application et des paramètres personnalisés](images/jamfpro-mac-profile.png)

5. <span data-ttu-id="97e35-142">Sélectionnez **Télécharger un fichier (fichier PLIST),** puis dans Domaine de **préférence,** entrez `com.microsoft.wdav.atp` :</span><span class="sxs-lookup"><span data-stu-id="97e35-142">Select **Upload File (PLIST file)** then in **Preference Domain** enter: `com.microsoft.wdav.atp`.</span></span> 

    ![Image du fichier de téléchargement plist jamfpro](images/jamfpro-plist-upload.png)

    ![Image du fichier de liste des propriétés de fichier de téléchargement](images/jamfpro-plist-file.png)

7. <span data-ttu-id="97e35-145">Sélectionnez **Ouvrir** et sélectionnez le fichier d’intégration.</span><span class="sxs-lookup"><span data-stu-id="97e35-145">Select **Open** and select the onboarding file.</span></span>

    ![Image du fichier d’intégration](images/jamfpro-plist-file-onboard.png)

8. <span data-ttu-id="97e35-147">Sélectionnez **Télécharger.**</span><span class="sxs-lookup"><span data-stu-id="97e35-147">Select **Upload**.</span></span> 

    ![Image du téléchargement d’un fichier plist](images/jamfpro-upload-plist.png)


9. <span data-ttu-id="97e35-149">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="97e35-149">Select the **Scope** tab.</span></span>

    ![Image de l’onglet d’étendue](images/jamfpro-scope-tab.png)

10. <span data-ttu-id="97e35-151">Sélectionnez les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="97e35-151">Select the target computers.</span></span>

    ![Image des ordinateurs cibles](images/jamfpro-target-computer.png)

    ![Image des cibles](images/jamfpro-targets.png) 

11. <span data-ttu-id="97e35-154">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="97e35-154">Select **Save**.</span></span>

    ![Image des ordinateurs cibles de déploiement](images/jamfpro-deployment-target.png)

    ![Image des ordinateurs cibles sélectionnés](images/jamfpro-target-selected.png)

12. <span data-ttu-id="97e35-157">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="97e35-157">Select **Done**.</span></span>

    ![Image des ordinateurs de groupe cibles](images/jamfpro-target-group.png)

    ![Liste des profils de configuration](images/jamfpro-configuration-policies.png)

## <a name="step-3-configure-microsoft-defender-for-endpoint-settings"></a><span data-ttu-id="97e35-160">Étape 3 : Configurer Microsoft Defender pour les paramètres de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="97e35-160">Step 3: Configure Microsoft Defender for Endpoint settings</span></span>

1.  <span data-ttu-id="97e35-161">Utilisez les paramètres de configuration microsoft Defender pour les points de terminaison suivants :</span><span class="sxs-lookup"><span data-stu-id="97e35-161">Use the following Microsoft Defender for Endpoint configuration settings:</span></span>

    - <span data-ttu-id="97e35-162">enableRealTimeProtection</span><span class="sxs-lookup"><span data-stu-id="97e35-162">enableRealTimeProtection</span></span>
    - <span data-ttu-id="97e35-163">passiveMode</span><span class="sxs-lookup"><span data-stu-id="97e35-163">passiveMode</span></span>
    
    >[!NOTE]
    ><span data-ttu-id="97e35-164">Non désactivé par défaut, si vous envisagez d’exécuter un antivirus tiers pour macOS, définissez-le sur `true` .</span><span class="sxs-lookup"><span data-stu-id="97e35-164">Not turned on by default, if you are planning to run a third-party AV for macOS, set it to `true`.</span></span>

    - <span data-ttu-id="97e35-165">exclusions</span><span class="sxs-lookup"><span data-stu-id="97e35-165">exclusions</span></span>
    - <span data-ttu-id="97e35-166">excludedPath</span><span class="sxs-lookup"><span data-stu-id="97e35-166">excludedPath</span></span>
    - <span data-ttu-id="97e35-167">excludedFileExtension</span><span class="sxs-lookup"><span data-stu-id="97e35-167">excludedFileExtension</span></span>
    - <span data-ttu-id="97e35-168">excludedFileName</span><span class="sxs-lookup"><span data-stu-id="97e35-168">excludedFileName</span></span>
    - <span data-ttu-id="97e35-169">exclusionsMergePolicy</span><span class="sxs-lookup"><span data-stu-id="97e35-169">exclusionsMergePolicy</span></span>
    - <span data-ttu-id="97e35-170">allowedThreats</span><span class="sxs-lookup"><span data-stu-id="97e35-170">allowedThreats</span></span>
    
    >[!NOTE]
    ><span data-ttu-id="97e35-171">EICAR est sur l’exemple, si vous êtes en train de passer par une preuve de concept, supprimez-le en particulier si vous testez EICAR.</span><span class="sxs-lookup"><span data-stu-id="97e35-171">EICAR is on the sample, if you are going through a proof-of-concept, remove it especially if you are testing EICAR.</span></span>
        
    - <span data-ttu-id="97e35-172">disallowedThreatActions</span><span class="sxs-lookup"><span data-stu-id="97e35-172">disallowedThreatActions</span></span>
    - <span data-ttu-id="97e35-173">potentially_unwanted_application</span><span class="sxs-lookup"><span data-stu-id="97e35-173">potentially_unwanted_application</span></span>
    - <span data-ttu-id="97e35-174">archive_bomb</span><span class="sxs-lookup"><span data-stu-id="97e35-174">archive_bomb</span></span>
    - <span data-ttu-id="97e35-175">cloudService</span><span class="sxs-lookup"><span data-stu-id="97e35-175">cloudService</span></span>
    - <span data-ttu-id="97e35-176">automaticSampleSubmission</span><span class="sxs-lookup"><span data-stu-id="97e35-176">automaticSampleSubmission</span></span>
    - <span data-ttu-id="97e35-177">étiquettes</span><span class="sxs-lookup"><span data-stu-id="97e35-177">tags</span></span>
    - <span data-ttu-id="97e35-178">hideStatusMenuIcon</span><span class="sxs-lookup"><span data-stu-id="97e35-178">hideStatusMenuIcon</span></span>
    
     <span data-ttu-id="97e35-179">Pour plus d’informations, [voir Liste des propriétés pour le profil de configuration Jamf.](mac-preferences.md#property-list-for-jamf-configuration-profile)</span><span class="sxs-lookup"><span data-stu-id="97e35-179">For information, see [Property list for Jamf configuration profile](mac-preferences.md#property-list-for-jamf-configuration-profile).</span></span>

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

2. <span data-ttu-id="97e35-180">Enregistrez le fichier sous `MDATP_MDAV_configuration_settings.plist` .</span><span class="sxs-lookup"><span data-stu-id="97e35-180">Save the file as `MDATP_MDAV_configuration_settings.plist`.</span></span>


3.  <span data-ttu-id="97e35-181">Dans le tableau de bord Jamf Pro, sélectionnez **Général**.</span><span class="sxs-lookup"><span data-stu-id="97e35-181">In the Jamf Pro dashboard, select **General**.</span></span>

    ![Image du nouveau tableau de bord Jamf Pro](images/644e0f3af40c29e80ca1443535b2fe32.png)

4. <span data-ttu-id="97e35-183">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="97e35-183">Enter the following details:</span></span>

    <span data-ttu-id="97e35-184">**Général**</span><span class="sxs-lookup"><span data-stu-id="97e35-184">**General**</span></span>
    
    - <span data-ttu-id="97e35-185">Nom : paramètres de configuration MDAV MDATP</span><span class="sxs-lookup"><span data-stu-id="97e35-185">Name: MDATP MDAV configuration settings</span></span>
    - <span data-ttu-id="97e35-186">Description :\<blank\></span><span class="sxs-lookup"><span data-stu-id="97e35-186">Description:\<blank\></span></span>
    - <span data-ttu-id="97e35-187">Catégorie : Aucun (par défaut)</span><span class="sxs-lookup"><span data-stu-id="97e35-187">Category: None (default)</span></span>
    - <span data-ttu-id="97e35-188">Méthode de distribution : installer automatiquement (par défaut)</span><span class="sxs-lookup"><span data-stu-id="97e35-188">Distribution Method: Install Automatically(default)</span></span>
    - <span data-ttu-id="97e35-189">Niveau : Niveau ordinateur (par défaut)</span><span class="sxs-lookup"><span data-stu-id="97e35-189">Level: Computer Level(default)</span></span>

    ![Image des paramètres de configuration MDAV MDATP](images/3160906404bc5a2edf84d1d015894e3b.png)

5. <span data-ttu-id="97e35-191">In **Application & Custom Settings** select **Configure**.</span><span class="sxs-lookup"><span data-stu-id="97e35-191">In **Application & Custom Settings** select **Configure**.</span></span>

    ![Image de l’application et des paramètres personnalisés](images/e1cc1e48ec9d5d688087b4d771e668d2.png)

6. <span data-ttu-id="97e35-193">Sélectionnez **Télécharger un fichier (fichier PLIST).**</span><span class="sxs-lookup"><span data-stu-id="97e35-193">Select **Upload File (PLIST file)**.</span></span>

    ![Image du fichier plist des paramètres de configuration](images/6f85269276b2278eca4bce84f935f87b.png)

7. <span data-ttu-id="97e35-195">In **Preferences Domain**, enter `com.microsoft.wdav` , then select Upload  **PLIST File**.</span><span class="sxs-lookup"><span data-stu-id="97e35-195">In **Preferences Domain**, enter `com.microsoft.wdav`, then select  **Upload PLIST File**.</span></span>

    ![Image du domaine des préférences de paramètres de configuration](images/db15f147dd959e872a044184711d7d46.png)

8. <span data-ttu-id="97e35-197">Sélectionnez **Choisir un fichier.**</span><span class="sxs-lookup"><span data-stu-id="97e35-197">Select **Choose File**.</span></span>

    ![Image des paramètres de configuration choisir un fichier](images/526e978761fc571cca06907da7b01fd6.png)

9. <span data-ttu-id="97e35-199">Sélectionnez **le MDATP_MDAV_configuration_settings.plist,** puis sélectionnez **Ouvrir.**</span><span class="sxs-lookup"><span data-stu-id="97e35-199">Select the **MDATP_MDAV_configuration_settings.plist**, then select **Open**.</span></span>

    ![Image des paramètres de configuration mdatpmdav](images/98acea3750113b8dbab334296e833003.png)

10. <span data-ttu-id="97e35-201">Sélectionnez **Télécharger.**</span><span class="sxs-lookup"><span data-stu-id="97e35-201">Select **Upload**.</span></span>

    ![Image du téléchargement des paramètres de configuration](images/0adb21c13206861ba9b30a879ade93d3.png)

    ![Image de l’image de téléchargement des paramètres de configuration](images/f624de59b3cc86e3e2d32ae5de093e02.png)

    >[!NOTE]
    ><span data-ttu-id="97e35-204">Si vous téléchargez le fichier Intune, vous obtenez l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="97e35-204">If you happen to upload the Intune file, you'll get the following error:</span></span><br>
    ><span data-ttu-id="97e35-205">![Image du téléchargement de fichiers intune des paramètres de configuration](images/8e69f867664668796a3b2904896f0436.png)</span><span class="sxs-lookup"><span data-stu-id="97e35-205">![Image of configuration settings intune file upload](images/8e69f867664668796a3b2904896f0436.png)</span></span>


11. <span data-ttu-id="97e35-206">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="97e35-206">Select **Save**.</span></span> 

    ![Image de l’image Enregistrer les paramètres de configuration](images/1b6b5a4edcb42d97f1e70a6a0fa48e3a.png)

12. <span data-ttu-id="97e35-208">Le fichier est téléchargé.</span><span class="sxs-lookup"><span data-stu-id="97e35-208">The file is uploaded.</span></span>

    ![Image de l’image téléchargée du fichier de paramètres de configuration](images/33e2b2a1611fdddf6b5b79e54496e3bb.png)

    ![Image du fichier de paramètres de configuration téléchargé](images/a422e57fe8d45689227e784443e51bd1.png)

13. <span data-ttu-id="97e35-211">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="97e35-211">Select the **Scope** tab.</span></span>

    ![Image de l’étendue des paramètres de configuration](images/9fc17529e5577eefd773c658ec576a7d.png)

14. <span data-ttu-id="97e35-213">Sélectionnez **Le groupe d’ordinateurs de Contoso.**</span><span class="sxs-lookup"><span data-stu-id="97e35-213">Select **Contoso's Machine Group**.</span></span> 

15. <span data-ttu-id="97e35-214">Sélectionnez **Ajouter,** puis **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="97e35-214">Select **Add**, then select **Save**.</span></span>

    ![Image des paramètres de configuration addsav](images/cf30438b5512ac89af1d11cbf35219a6.png)

    ![Image de l’ajout d’enregistrer les paramètres de configuration](images/6f093e42856753a3955cab7ee14f12d9.png)

16. <span data-ttu-id="97e35-217">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="97e35-217">Select **Done**.</span></span> <span data-ttu-id="97e35-218">Vous verrez le nouveau profil **de configuration.**</span><span class="sxs-lookup"><span data-stu-id="97e35-218">You'll see the new **Configuration profile**.</span></span>

    ![Image de l’image de profil de configuration des paramètres de configuration](images/dd55405106da0dfc2f50f8d4525b01c8.png)


## <a name="step-4-configure-notifications-settings"></a><span data-ttu-id="97e35-220">Étape 4 : Configurer les paramètres de notifications</span><span class="sxs-lookup"><span data-stu-id="97e35-220">Step 4: Configure notifications settings</span></span>

<span data-ttu-id="97e35-221">Ces étapes s’appliquent à macOS 10.15 (Genreline) ou aux appareils plus nouveaux.</span><span class="sxs-lookup"><span data-stu-id="97e35-221">These steps are applicable of macOS 10.15 (Catalina) or newer.</span></span>

1. <span data-ttu-id="97e35-222">Téléchargement `notif.mobileconfig` à partir de notre référentiel [GitHub](https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/mobileconfig/profiles/notif.mobileconfig)</span><span class="sxs-lookup"><span data-stu-id="97e35-222">Download `notif.mobileconfig` from [our GitHub repository](https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/mobileconfig/profiles/notif.mobileconfig)</span></span>

2. <span data-ttu-id="97e35-223">Enregistrez-le sous `MDATP_MDAV_notification_settings.plist` .</span><span class="sxs-lookup"><span data-stu-id="97e35-223">Save it as `MDATP_MDAV_notification_settings.plist`.</span></span>

3. <span data-ttu-id="97e35-224">Dans le tableau de bord Jamf Pro, sélectionnez **Général**.</span><span class="sxs-lookup"><span data-stu-id="97e35-224">In the Jamf Pro dashboard, select **General**.</span></span> 
       
4. <span data-ttu-id="97e35-225">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="97e35-225">Enter the following details:</span></span>

    <span data-ttu-id="97e35-226">**Général**</span><span class="sxs-lookup"><span data-stu-id="97e35-226">**General**</span></span> 
    
    - <span data-ttu-id="97e35-227">Nom : paramètres de notification MDAV MDATP</span><span class="sxs-lookup"><span data-stu-id="97e35-227">Name: MDATP MDAV Notification settings</span></span>
    - <span data-ttu-id="97e35-228">Description : macOS 10.15 (Contrôle) ou une nouveauté</span><span class="sxs-lookup"><span data-stu-id="97e35-228">Description: macOS 10.15 (Catalina) or newer</span></span>
    - <span data-ttu-id="97e35-229">Catégorie : Aucun (par défaut)</span><span class="sxs-lookup"><span data-stu-id="97e35-229">Category: None (default)</span></span>
    - <span data-ttu-id="97e35-230">Méthode de distribution : installer automatiquement (par défaut)</span><span class="sxs-lookup"><span data-stu-id="97e35-230">Distribution Method: Install Automatically(default)</span></span>
    - <span data-ttu-id="97e35-231">Niveau : Niveau ordinateur (par défaut)</span><span class="sxs-lookup"><span data-stu-id="97e35-231">Level: Computer Level(default)</span></span>

    ![Image des paramètres de configuration mdatpmdav](images/c9820a5ff84aaf21635c04a23a97ca93.png)


5. <span data-ttu-id="97e35-233">Sélectionnez **Télécharger un fichier (fichier PLIST).**</span><span class="sxs-lookup"><span data-stu-id="97e35-233">Select **Upload File (PLIST file)**.</span></span>

    ![Image des paramètres de configuration téléchargez plistfile](images/7f9138053dbcbf928e5182ee7b295ebe.png)
 

6. <span data-ttu-id="97e35-235">Sélectionnez **Choisir**  >  **un fichier MDATP_MDAV_Notification_Settings.plist.**</span><span class="sxs-lookup"><span data-stu-id="97e35-235">Select **Choose File** > **MDATP_MDAV_Notification_Settings.plist**.</span></span>


    ![Image des paramètres de configuration mdatpmdav notsettings](images/4bac6ce277aedfb4a674f2d9fcb2599a.png)


    ![Image des paramètres de configuration mdatpmdav notifsettings](images/20e33b98eb54447881dc6c89e58b890f.png)

7. <span data-ttu-id="97e35-238">Sélectionnez **Ouvrir**  >  **le téléchargement.**</span><span class="sxs-lookup"><span data-stu-id="97e35-238">Select **Open** > **Upload**.</span></span>

    ![Image de l’upl img des paramètres de configuration](images/7697c33b9fd376ae5a8023d01f9d3857.png)


    ![Image de l’image upl des paramètres de configuration](images/2bda9244ec25d1526811da4ea91b1c86.png)

8. <span data-ttu-id="97e35-241">Sélectionnez **l’onglet** Étendue, puis **sélectionnez Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="97e35-241">Select the **Scope** tab, then select **Add**.</span></span>

    ![Image de l’étendue ajouter des paramètres de configuration](images/441aa2ecd36abadcdd8aed03556080b5.png)


9. <span data-ttu-id="97e35-243">Sélectionnez **Le groupe d’ordinateurs de Contoso.**</span><span class="sxs-lookup"><span data-stu-id="97e35-243">Select **Contoso's Machine Group**.</span></span> 

10. <span data-ttu-id="97e35-244">Sélectionnez **Ajouter,** puis **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="97e35-244">Select **Add**, then select **Save**.</span></span>
    
    ![Image des paramètres de configuration contoso machine grp save](images/09a275e321268e5e3ac0c0865d3e2db5.png)

    
    ![Image des paramètres de configuration pour ajouter l’enregistrer](images/4d2d1d4ee13d3f840f425924c3df0d51.png)

11. <span data-ttu-id="97e35-247">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="97e35-247">Select **Done**.</span></span> <span data-ttu-id="97e35-248">Vous verrez le nouveau profil **de configuration.**</span><span class="sxs-lookup"><span data-stu-id="97e35-248">You'll see the new **Configuration profile**.</span></span>
    <span data-ttu-id="97e35-249">![Image du paramètre de configuration terminé img](images/633ad26b8bf24ec683c98b2feb884bdf.png)</span><span class="sxs-lookup"><span data-stu-id="97e35-249">![Image of configuration setting done img](images/633ad26b8bf24ec683c98b2feb884bdf.png)</span></span>

## <a name="step-5-configure-microsoft-autoupdate-mau"></a><span data-ttu-id="97e35-250">Étape 5 : Configurer la mise à jour automatique Microsoft (AutoUpdate)</span><span class="sxs-lookup"><span data-stu-id="97e35-250">Step 5: Configure Microsoft AutoUpdate (MAU)</span></span>

1. <span data-ttu-id="97e35-251">Utilisez les paramètres de configuration microsoft Defender pour les points de terminaison suivants :</span><span class="sxs-lookup"><span data-stu-id="97e35-251">Use the following Microsoft Defender for Endpoint configuration settings:</span></span>

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

2. <span data-ttu-id="97e35-252">Enregistrez-le sous `MDATP_MDAV_MAU_settings.plist` .</span><span class="sxs-lookup"><span data-stu-id="97e35-252">Save it as `MDATP_MDAV_MAU_settings.plist`.</span></span>

3. <span data-ttu-id="97e35-253">Dans le tableau de bord Jamf Pro, sélectionnez **Général**.</span><span class="sxs-lookup"><span data-stu-id="97e35-253">In the Jamf Pro dashboard, select **General**.</span></span> 

    ![Image de l’image générale du paramètre de configuration](images/eaba2a23dd34f73bf59e826217ba6f15.png)

4. <span data-ttu-id="97e35-255">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="97e35-255">Enter the following details:</span></span>

    <span data-ttu-id="97e35-256">**Général**</span><span class="sxs-lookup"><span data-stu-id="97e35-256">**General**</span></span> 
    
    - <span data-ttu-id="97e35-257">Name: MDATP MDAV MAU settings</span><span class="sxs-lookup"><span data-stu-id="97e35-257">Name: MDATP MDAV MAU settings</span></span>
    - <span data-ttu-id="97e35-258">Description : Paramètres de mise à jour automatique Microsoft pour MDATP pour macOS</span><span class="sxs-lookup"><span data-stu-id="97e35-258">Description: Microsoft AutoUpdate settings for MDATP for macOS</span></span>
    - <span data-ttu-id="97e35-259">Catégorie : Aucun (par défaut)</span><span class="sxs-lookup"><span data-stu-id="97e35-259">Category: None (default)</span></span>
    - <span data-ttu-id="97e35-260">Méthode de distribution : installer automatiquement (par défaut)</span><span class="sxs-lookup"><span data-stu-id="97e35-260">Distribution Method: Install Automatically(default)</span></span>
    - <span data-ttu-id="97e35-261">Niveau : Niveau ordinateur (par défaut)</span><span class="sxs-lookup"><span data-stu-id="97e35-261">Level: Computer Level(default)</span></span>

5. <span data-ttu-id="97e35-262">In **Application & Custom Settings** select **Configure**.</span><span class="sxs-lookup"><span data-stu-id="97e35-262">In **Application & Custom Settings** select **Configure**.</span></span>

    ![Image de l’application de paramètre de configuration et des paramètres personnalisés](images/1f72e9c15eaafcabf1504397e99be311.png)

6. <span data-ttu-id="97e35-264">Sélectionnez **Télécharger un fichier (fichier PLIST).**</span><span class="sxs-lookup"><span data-stu-id="97e35-264">Select **Upload File (PLIST file)**.</span></span>

    ![Image de la liste plist des paramètres de configuration](images/1213872db5833aa8be535da57653219f.png)  

7. <span data-ttu-id="97e35-266">In **Preference Domain** enter: , then select Upload `com.microsoft.autoupdate2` **PLIST File**.</span><span class="sxs-lookup"><span data-stu-id="97e35-266">In **Preference Domain** enter: `com.microsoft.autoupdate2`, then select **Upload PLIST File**.</span></span>

    ![Image du domaine préf du paramètre de configuration](images/1213872db5833aa8be535da57653219f.png)

8. <span data-ttu-id="97e35-268">Sélectionnez **Choisir un fichier.**</span><span class="sxs-lookup"><span data-stu-id="97e35-268">Select **Choose File**.</span></span>

    ![Image du fichier choosefile du paramètre de configuration](images/335aff58950ce62d1dabc289ecdce9ed.png)

9. <span data-ttu-id="97e35-270">Sélectionnez **MDATP_MDAV_MAU_settings.plist.**</span><span class="sxs-lookup"><span data-stu-id="97e35-270">Select **MDATP_MDAV_MAU_settings.plist**.</span></span>

    ![Image des paramètres de configuration mdatpmdavmau](images/a26bd4967cd54bb113a2c8d32894c3de.png)

10. <span data-ttu-id="97e35-272">Sélectionnez **Télécharger.**</span><span class="sxs-lookup"><span data-stu-id="97e35-272">Select **Upload**.</span></span>
    <span data-ttu-id="97e35-273">![Image de la configuration de la configuration de délimitation](images/4239ca0528efb0734e4ca0b490bfb22d.png)</span><span class="sxs-lookup"><span data-stu-id="97e35-273">![Image of configuration setting uplimage](images/4239ca0528efb0734e4ca0b490bfb22d.png)</span></span>

    ![Image de la configuration de la configuration de la configuration](images/4ec20e72c8aed9a4c16912e01692436a.png)

11. <span data-ttu-id="97e35-275">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="97e35-275">Select **Save**.</span></span>

    ![Image du paramètre de configuration saveimg](images/253274b33e74f3f5b8d475cf8692ce4e.png)

12. <span data-ttu-id="97e35-277">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="97e35-277">Select the **Scope** tab.</span></span>
   
     ![Image du paramètre de configuration scopetab](images/10ab98358b2d602f3f67618735fa82fb.png)

13. <span data-ttu-id="97e35-279">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="97e35-279">Select **Add**.</span></span>
    
    ![Image du paramètre de configuration addimg1](images/56e6f6259b9ce3c1706ed8d666ae4947.png)

    ![Image du paramètre de configuration addimg2](images/38c67ee1905c4747c3b26c8eba57726b.png)

    ![Image du paramètre de configuration addimg3](images/321ba245f14743c1d5d51c15e99deecc.png)

14. <span data-ttu-id="97e35-283">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="97e35-283">Select **Done**.</span></span>
    
    ![Image du paramètre de configuration doneimage](images/ba44cdb77e4781aa8b940fb83e3c21f7.png)

## <a name="step-6-grant-full-disk-access-to-microsoft-defender-for-endpoint"></a><span data-ttu-id="97e35-285">Étape 6 : Accorder un accès disque total à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="97e35-285">Step 6: Grant full disk access to Microsoft Defender for Endpoint</span></span>

1. <span data-ttu-id="97e35-286">Dans le tableau de bord Jamf Pro, sélectionnez **Profils de configuration.**</span><span class="sxs-lookup"><span data-stu-id="97e35-286">In the Jamf Pro dashboard, select **Configuration Profiles**.</span></span>

    ![Image du profil de configuration des paramètres de configuration](images/264493cd01e62c7085659d6fdc26dc91.png)

2. <span data-ttu-id="97e35-288">Sélectionnez **+ Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="97e35-288">Select **+ New**.</span></span> 

3. <span data-ttu-id="97e35-289">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="97e35-289">Enter the following details:</span></span>

    <span data-ttu-id="97e35-290">**Général**</span><span class="sxs-lookup"><span data-stu-id="97e35-290">**General**</span></span> 
    - <span data-ttu-id="97e35-291">Nom : MDATP MDAV : accorder un accès disque total à l’EDR et à l’antivirus</span><span class="sxs-lookup"><span data-stu-id="97e35-291">Name: MDATP MDAV - grant Full Disk Access to EDR and AV</span></span>
    - <span data-ttu-id="97e35-292">Description : sur macOS Ou une nouveauté, le nouveau contrôle de stratégie des préférences de confidentialité</span><span class="sxs-lookup"><span data-stu-id="97e35-292">Description: On macOS Catalina or newer, the new Privacy Preferences Policy Control</span></span>
    - <span data-ttu-id="97e35-293">Catégorie : Aucun</span><span class="sxs-lookup"><span data-stu-id="97e35-293">Category: None</span></span>
    - <span data-ttu-id="97e35-294">Méthode de distribution : installer automatiquement</span><span class="sxs-lookup"><span data-stu-id="97e35-294">Distribution method: Install Automatically</span></span>
    - <span data-ttu-id="97e35-295">Niveau : niveau ordinateur</span><span class="sxs-lookup"><span data-stu-id="97e35-295">Level: Computer level</span></span>


    ![Image du paramètre de configuration général](images/ba3d40399e1a6d09214ecbb2b341923f.png)

4. <span data-ttu-id="97e35-297">In **Configure Privacy Preferences Policy Control** select **Configure**.</span><span class="sxs-lookup"><span data-stu-id="97e35-297">In **Configure Privacy Preferences Policy Control** select **Configure**.</span></span>

    ![Image du contrôle de stratégie de confidentialité de la configuration](images/715ae7ec8d6a262c489f94d14e1e51bb.png)

5. <span data-ttu-id="97e35-299">Dans **Le contrôle de stratégie des préférences de confidentialité,** entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="97e35-299">In **Privacy Preferences Policy Control**, enter the following details:</span></span>

    - <span data-ttu-id="97e35-300">Identificateur : `com.microsoft.wdav`</span><span class="sxs-lookup"><span data-stu-id="97e35-300">Identifier: `com.microsoft.wdav`</span></span>
    - <span data-ttu-id="97e35-301">Type d’identificateur : ID d’offre groupée</span><span class="sxs-lookup"><span data-stu-id="97e35-301">Identifier Type: Bundle ID</span></span>
    - <span data-ttu-id="97e35-302">Conditions requises pour le code : `identifier "com.microsoft.wdav" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span><span class="sxs-lookup"><span data-stu-id="97e35-302">Code Requirement: `identifier "com.microsoft.wdav" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span></span>


    ![Image des détails du contrôle de stratégie de confidentialité des paramètres de configuration](images/22cb439de958101c0a12f3038f905b27.png)

6. <span data-ttu-id="97e35-304">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="97e35-304">Select **+ Add**.</span></span>

    ![Image du paramètre de configuration ajouter la stratégie système à tous les fichiers](images/bd93e78b74c2660a0541af4690dd9485.png)

    - <span data-ttu-id="97e35-306">Sous Application ou service : définir sur **SystemPolicyAllFiles**</span><span class="sxs-lookup"><span data-stu-id="97e35-306">Under App or service: Set to **SystemPolicyAllFiles**</span></span>

    - <span data-ttu-id="97e35-307">Sous « accès » : définir sur **Autoriser**</span><span class="sxs-lookup"><span data-stu-id="97e35-307">Under "access": Set to **Allow**</span></span>

7. <span data-ttu-id="97e35-308">Sélectionnez **Enregistrer** (et non celui en bas à droite).</span><span class="sxs-lookup"><span data-stu-id="97e35-308">Select **Save** (not the one at the bottom right).</span></span>

    ![Image des images d’enregistrer les paramètres de configuration](images/6de50b4a897408ddc6ded56a09c09fe2.png)

8. <span data-ttu-id="97e35-310">Cliquez sur le `+` signe en de côté **d’App Access** pour ajouter une nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="97e35-310">Click the `+` sign next to **App Access** to add a new entry.</span></span>

    ![Image de l’accès aux applications de paramètre de configuration](images/tcc-add-entry.png)

9. <span data-ttu-id="97e35-312">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="97e35-312">Enter the following details:</span></span>

    - <span data-ttu-id="97e35-313">Identificateur : `com.microsoft.wdav.epsext`</span><span class="sxs-lookup"><span data-stu-id="97e35-313">Identifier: `com.microsoft.wdav.epsext`</span></span>
    - <span data-ttu-id="97e35-314">Type d’identificateur : ID d’offre groupée</span><span class="sxs-lookup"><span data-stu-id="97e35-314">Identifier Type: Bundle ID</span></span>
    - <span data-ttu-id="97e35-315">Conditions requises pour le code : `identifier "com.microsoft.wdav.epsext" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span><span class="sxs-lookup"><span data-stu-id="97e35-315">Code Requirement: `identifier "com.microsoft.wdav.epsext" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span></span>

10. <span data-ttu-id="97e35-316">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="97e35-316">Select **+ Add**.</span></span>

    ![Image de l’entrée tcc epsext du paramètre de configuration](images/tcc-epsext-entry.png)

    - <span data-ttu-id="97e35-318">Sous Application ou service : définir sur **SystemPolicyAllFiles**</span><span class="sxs-lookup"><span data-stu-id="97e35-318">Under App or service: Set to **SystemPolicyAllFiles**</span></span>

    - <span data-ttu-id="97e35-319">Sous « accès » : définir sur **Autoriser**</span><span class="sxs-lookup"><span data-stu-id="97e35-319">Under "access": Set to **Allow**</span></span>

11. <span data-ttu-id="97e35-320">Sélectionnez **Enregistrer** (et non celui en bas à droite).</span><span class="sxs-lookup"><span data-stu-id="97e35-320">Select **Save** (not the one at the bottom right).</span></span>

    ![Image du paramètre de configuration tcc epsext image2](images/tcc-epsext-entry2.png)

12. <span data-ttu-id="97e35-322">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="97e35-322">Select the **Scope** tab.</span></span>

    ![Image de l’étendue du paramètre de configuration](images/2c49b16cd112729b3719724f581e6882.png)

13. <span data-ttu-id="97e35-324">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="97e35-324">Select **+ Add**.</span></span>

    ![Image de l’addimage du paramètre de configuration](images/57cef926d1b9260fb74a5f460cee887a.png)

14. <span data-ttu-id="97e35-326">Sélectionnez **Groupes d’ordinateurs** > **sous Nom** de groupe > sélectionnez Groupe MachineGroup de **Contoso.**</span><span class="sxs-lookup"><span data-stu-id="97e35-326">Select **Computer Groups** > under **Group Name** > select **Contoso's MachineGroup**.</span></span> 

    ![Image du paramètre de configuration contoso machinegrp](images/368d35b3d6179af92ffdbfd93b226b69.png)

15. <span data-ttu-id="97e35-328">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="97e35-328">Select **Add**.</span></span> 

16. <span data-ttu-id="97e35-329">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="97e35-329">Select **Save**.</span></span> 
    
17. <span data-ttu-id="97e35-330">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="97e35-330">Select **Done**.</span></span>
    
    ![Image de donimg de paramètre de configuration](images/809cef630281b64b8f07f20913b0039b.png)
    
    ![Image du paramètre de configuration donimg2](images/6c8b406ee224335a8c65d06953dc756e.png)


## <a name="step-7-approve-kernel-extension-for-microsoft-defender-for-endpoint"></a><span data-ttu-id="97e35-333">Étape 7 : Approuver l’extension de noyau pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="97e35-333">Step 7: Approve Kernel extension for Microsoft Defender for Endpoint</span></span>

1. <span data-ttu-id="97e35-334">Dans les **profils de configuration,** **sélectionnez + Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="97e35-334">In the **Configuration Profiles**, select **+ New**.</span></span>

    ![Capture d’écran d’un billet de réseau social Description généré automatiquement](images/6c8b406ee224335a8c65d06953dc756e.png)

2. <span data-ttu-id="97e35-336">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="97e35-336">Enter the following details:</span></span>

    <span data-ttu-id="97e35-337">**Général**</span><span class="sxs-lookup"><span data-stu-id="97e35-337">**General**</span></span> 
    
    - <span data-ttu-id="97e35-338">Name: MDATP MDAV Kernel Extension</span><span class="sxs-lookup"><span data-stu-id="97e35-338">Name: MDATP MDAV Kernel Extension</span></span>
    - <span data-ttu-id="97e35-339">Description : extension de noyau MDATP (kext)</span><span class="sxs-lookup"><span data-stu-id="97e35-339">Description: MDATP kernel extension (kext)</span></span>
    - <span data-ttu-id="97e35-340">Catégorie : Aucun</span><span class="sxs-lookup"><span data-stu-id="97e35-340">Category: None</span></span>
    - <span data-ttu-id="97e35-341">Méthode de distribution : installer automatiquement</span><span class="sxs-lookup"><span data-stu-id="97e35-341">Distribution Method: Install Automatically</span></span>
    - <span data-ttu-id="97e35-342">Niveau : niveau ordinateur</span><span class="sxs-lookup"><span data-stu-id="97e35-342">Level: Computer Level</span></span>

    ![Image du noyau mdatpmdav des paramètres de configuration](images/24e290f5fc309932cf41f3a280d22c14.png)

3. <span data-ttu-id="97e35-344">In **Configure Approved Kernel Extensions** select **Configure**.</span><span class="sxs-lookup"><span data-stu-id="97e35-344">In **Configure Approved Kernel Extensions** select **Configure**.</span></span>

    ![Image de l’ext de noyau approuvé des paramètres de configuration](images/30be88b63abc5e8dde11b73f1b1ade6a.png)

   
4. <span data-ttu-id="97e35-346">Dans **Extensions de noyau approuvées,** entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="97e35-346">In **Approved Kernel Extensions** Enter the following details:</span></span>

    - <span data-ttu-id="97e35-347">Nom complet : Microsoft Corp.</span><span class="sxs-lookup"><span data-stu-id="97e35-347">Display Name: Microsoft Corp.</span></span>
    - <span data-ttu-id="97e35-348">ID d’équipe : UBF8T346G9</span><span class="sxs-lookup"><span data-stu-id="97e35-348">Team ID: UBF8T346G9</span></span>

    ![Image de l’extension de noyau appr des paramètres de configuration](images/39cf120d3ac3652292d8d1b6d057bd60.png)

5. <span data-ttu-id="97e35-350">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="97e35-350">Select the **Scope** tab.</span></span>

    ![Image de l’onglet d’étendue des paramètres de configuration img](images/0df36fc308ba569db204ee32db3fb40a.png)

6. <span data-ttu-id="97e35-352">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="97e35-352">Select **+ Add**.</span></span>

7. <span data-ttu-id="97e35-353">Sélectionnez **Groupes d’ordinateurs** > **sous Nom** du > sélectionnez Groupe ordinateur de **Contoso.**</span><span class="sxs-lookup"><span data-stu-id="97e35-353">Select **Computer Groups** > under **Group Name** > select **Contoso's Machine Group**.</span></span>

8. <span data-ttu-id="97e35-354">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="97e35-354">Select **+ Add**.</span></span>

    ![Image des paramètres de configuration pour ajouter des images](images/0dde8a4c41110dbc398c485433a81359.png)

9. <span data-ttu-id="97e35-356">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="97e35-356">Select **Save**.</span></span>

    ![Image de l’économiserie des paramètres de configuration](images/0add8019b85a453b47fa5c402c72761b.png)

10. <span data-ttu-id="97e35-358">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="97e35-358">Select **Done**.</span></span>

    ![Image des paramètres de configuration doneimag](images/1c9bd3f68db20b80193dac18f33c22d0.png)


## <a name="step-8-approve-system-extensions-for-microsoft-defender-for-endpoint"></a><span data-ttu-id="97e35-360">Étape 8 : Approuver les extensions système pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="97e35-360">Step 8: Approve System extensions for Microsoft Defender for Endpoint</span></span>

1. <span data-ttu-id="97e35-361">Dans les **profils de configuration,** **sélectionnez + Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="97e35-361">In the **Configuration Profiles**, select **+ New**.</span></span>

    ![Capture d’écran d’un billet de réseau social Description généré automatiquement](images/6c8b406ee224335a8c65d06953dc756e.png)

2. <span data-ttu-id="97e35-363">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="97e35-363">Enter the following details:</span></span>

    <span data-ttu-id="97e35-364">**Général**</span><span class="sxs-lookup"><span data-stu-id="97e35-364">**General**</span></span>
    
    - <span data-ttu-id="97e35-365">Name: MDATP MDAV System Extensions</span><span class="sxs-lookup"><span data-stu-id="97e35-365">Name: MDATP MDAV System Extensions</span></span>
    - <span data-ttu-id="97e35-366">Description : extensions système MDATP</span><span class="sxs-lookup"><span data-stu-id="97e35-366">Description: MDATP system extensions</span></span>
    - <span data-ttu-id="97e35-367">Catégorie : Aucun</span><span class="sxs-lookup"><span data-stu-id="97e35-367">Category: None</span></span>
    - <span data-ttu-id="97e35-368">Méthode de distribution : installer automatiquement</span><span class="sxs-lookup"><span data-stu-id="97e35-368">Distribution Method: Install Automatically</span></span>
    - <span data-ttu-id="97e35-369">Niveau : niveau ordinateur</span><span class="sxs-lookup"><span data-stu-id="97e35-369">Level: Computer Level</span></span>

    ![Image du nouveau prof des paramètres de configuration](images/sysext-new-profile.png)

3. <span data-ttu-id="97e35-371">Dans **les extensions système,** **sélectionnez Configurer.**</span><span class="sxs-lookup"><span data-stu-id="97e35-371">In **System Extensions** select **Configure**.</span></span>

   ![Image de configuration sysext des paramètres de configuration](images/sysext-configure.png)

4. <span data-ttu-id="97e35-373">Dans **les extensions système,** entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="97e35-373">In **System Extensions** enter the following details:</span></span>

   - <span data-ttu-id="97e35-374">Nom complet : Microsoft Corp. System Extensions</span><span class="sxs-lookup"><span data-stu-id="97e35-374">Display Name: Microsoft Corp. System Extensions</span></span>
   - <span data-ttu-id="97e35-375">Types d’extension système : extensions système autorisées</span><span class="sxs-lookup"><span data-stu-id="97e35-375">System Extension Types: Allowed System Extensions</span></span>
   - <span data-ttu-id="97e35-376">Identificateur d’équipe : UBF8T346G9</span><span class="sxs-lookup"><span data-stu-id="97e35-376">Team Identifier: UBF8T346G9</span></span>
   - <span data-ttu-id="97e35-377">Extensions système autorisées :</span><span class="sxs-lookup"><span data-stu-id="97e35-377">Allowed System Extensions:</span></span>
     - <span data-ttu-id="97e35-378">**com.microsoft.wdav.epsext**</span><span class="sxs-lookup"><span data-stu-id="97e35-378">**com.microsoft.wdav.epsext**</span></span>
     - <span data-ttu-id="97e35-379">**com.microsoft.wdav.netext**</span><span class="sxs-lookup"><span data-stu-id="97e35-379">**com.microsoft.wdav.netext**</span></span>

    ![Image des paramètres de configuration sysextconfig2](images/sysext-configure2.png)

5. <span data-ttu-id="97e35-381">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="97e35-381">Select the **Scope** tab.</span></span>

    ![Image de l’étendue des paramètres de configuration](images/0df36fc308ba569db204ee32db3fb40a.png)

6. <span data-ttu-id="97e35-383">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="97e35-383">Select **+ Add**.</span></span>

7. <span data-ttu-id="97e35-384">Sélectionnez **Groupes d’ordinateurs** > **sous Nom** du > sélectionnez Groupe ordinateur de **Contoso.**</span><span class="sxs-lookup"><span data-stu-id="97e35-384">Select **Computer Groups** > under **Group Name** > select **Contoso's Machine Group**.</span></span>

8. <span data-ttu-id="97e35-385">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="97e35-385">Select **+ Add**.</span></span>

   ![Image de l’addima des paramètres de configuration](images/0dde8a4c41110dbc398c485433a81359.png)

9. <span data-ttu-id="97e35-387">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="97e35-387">Select **Save**.</span></span>

   ![Image de l’étendue sysext des paramètres de configuration](images/sysext-scope.png)

10. <span data-ttu-id="97e35-389">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="97e35-389">Select **Done**.</span></span>

    ![Image des paramètres de configuration sysext-final](images/sysext-final.png)

## <a name="step-9-configure-network-extension"></a><span data-ttu-id="97e35-391">Étape 9 : Configurer l’extension réseau</span><span class="sxs-lookup"><span data-stu-id="97e35-391">Step 9: Configure Network Extension</span></span>

<span data-ttu-id="97e35-392">Dans le cadre des fonctionnalités de détection et de réponse des points de terminaison, Microsoft Defender pour Endpoint pour Mac inspecte le trafic de socket et signale ces informations au portail centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="97e35-392">As part of the Endpoint Detection and Response capabilities, Microsoft Defender for Endpoint for Mac inspects socket traffic and reports this information to the Microsoft Defender Security Center portal.</span></span> <span data-ttu-id="97e35-393">La stratégie suivante permet à l’extension réseau d’effectuer cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="97e35-393">The following policy allows the network extension to perform this functionality.</span></span>

>[!NOTE]
><span data-ttu-id="97e35-394">JAMF ne prend pas en charge les stratégies de filtrage de contenu, ce qui est une condition préalable à l’activation des extensions réseau installées par Microsoft Defender pour Endpoint pour Mac sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="97e35-394">JAMF doesn’t have built-in support for content filtering policies, which are a pre-requisite for enabling the network extensions that Microsoft Defender for Endpoint for Mac installs on the device.</span></span> <span data-ttu-id="97e35-395">De plus, JAMF modifie parfois le contenu des stratégies déployées.</span><span class="sxs-lookup"><span data-stu-id="97e35-395">Furthermore, JAMF sometimes changes the content of the policies being deployed.</span></span>
><span data-ttu-id="97e35-396">En tant que tel, les étapes suivantes fournissent une solution de contournement qui implique la signature du profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="97e35-396">As such, the following steps provide a workaround that involve signing the configuration profile.</span></span>

1. <span data-ttu-id="97e35-397">Télécharger `netfilter.mobileconfig` à partir de notre référentiel [GitHub](https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/mobileconfig/profiles/netfilter.mobileconfig) sur votre appareil et l’enregistrer sous `com.microsoft.network-extension.mobileconfig`</span><span class="sxs-lookup"><span data-stu-id="97e35-397">Download `netfilter.mobileconfig` from [our GitHub repository](https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/mobileconfig/profiles/netfilter.mobileconfig) to your device and save it as `com.microsoft.network-extension.mobileconfig`</span></span>

2. <span data-ttu-id="97e35-398">Suivez les instructions de cette [page](https://www.jamf.com/jamf-nation/articles/649/creating-a-signing-certificate-using-jamf-pro-s-built-in-certificate-authority) pour créer un certificat de signature à l’aide de l’autorité de certification intégrée de JAMF</span><span class="sxs-lookup"><span data-stu-id="97e35-398">Follow the instructions on [this page](https://www.jamf.com/jamf-nation/articles/649/creating-a-signing-certificate-using-jamf-pro-s-built-in-certificate-authority) to create a signing certificate using JAMF’s built-in certificate authority</span></span>

3. <span data-ttu-id="97e35-399">Une fois le certificat créé et installé sur votre appareil, exécutez la commande suivante à partir du Terminal à partir d’un appareil macOS :</span><span class="sxs-lookup"><span data-stu-id="97e35-399">After the certificate is created and installed to your device, run the following command from the Terminal from a macOS device:</span></span>

   ```bash
   $ security cms -S -N "<certificate name>" -i com.microsoft.network-extension.mobileconfig -o com.microsoft.network-extension.signed.mobileconfig
   ```

   ![Fenêtre Terminal avec commande pour créer une configuration signée](images/netext-create-profile.png)

4. <span data-ttu-id="97e35-401">À partir du portail JAMF, accédez aux **profils de configuration** et cliquez sur le **bouton** Télécharger.</span><span class="sxs-lookup"><span data-stu-id="97e35-401">From the JAMF portal, navigate to **Configuration Profiles** and click the **Upload** button.</span></span> 

   ![Image de la fenêtre de téléchargement](images/netext-upload-file.png)

5. <span data-ttu-id="97e35-403">Sélectionnez **Choisir un** fichier et `microsoft.network-extension.signed.mobileconfig` sélectionnez .</span><span class="sxs-lookup"><span data-stu-id="97e35-403">Select **Choose File** and select `microsoft.network-extension.signed.mobileconfig`.</span></span>

   ![Image du fichier de texte netexte de la fenêtre de téléchargement](images/netext-choose-file.png)

6. <span data-ttu-id="97e35-405">Sélectionnez **Télécharger.**</span><span class="sxs-lookup"><span data-stu-id="97e35-405">Select **Upload**.</span></span>

   ![Image du fichier de chargement de la fenêtre de téléchargement netexte2](images/netext-upload-file2.png)

7. <span data-ttu-id="97e35-407">Après avoir téléchargé le fichier, vous êtes redirigé vers une nouvelle page pour finaliser la création de ce profil.</span><span class="sxs-lookup"><span data-stu-id="97e35-407">After uploading the file, you are redirected to a new page to finalize the creation of this profile.</span></span>

   ![Image de la nouvelle page de profil de configuration netexte](images/netext-profile-page.png)

8. <span data-ttu-id="97e35-409">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="97e35-409">Select the **Scope** tab.</span></span>

   ![Image de l’onglet système des paramètres de configuration](images/0df36fc308ba569db204ee32db3fb40a.png)

9. <span data-ttu-id="97e35-411">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="97e35-411">Select **+ Add**.</span></span>

10. <span data-ttu-id="97e35-412">Sélectionnez **Groupes d’ordinateurs** > **sous Nom** du > sélectionnez Groupe ordinateur de **Contoso.**</span><span class="sxs-lookup"><span data-stu-id="97e35-412">Select **Computer Groups** > under **Group Name** > select **Contoso's Machine Group**.</span></span>

11. <span data-ttu-id="97e35-413">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="97e35-413">Select **+ Add**.</span></span>

    ![Image des paramètres de configuration adim](images/0dde8a4c41110dbc398c485433a81359.png)

12. <span data-ttu-id="97e35-415">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="97e35-415">Select **Save**.</span></span>

    ![Image des paramètres de configuration savimg netextscop](images/netext-scope.png)

13. <span data-ttu-id="97e35-417">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="97e35-417">Select **Done**.</span></span>

    ![Image de paramètres de configuration netextfinal](images/netext-final.png)

## <a name="step-10-schedule-scans-with-microsoft-defender-for-endpoint-for-mac"></a><span data-ttu-id="97e35-419">Étape 10 : Planifier des analyses avec Microsoft Defender pour Endpoint pour Mac</span><span class="sxs-lookup"><span data-stu-id="97e35-419">Step 10: Schedule scans with Microsoft Defender for Endpoint for Mac</span></span>
<span data-ttu-id="97e35-420">Suivez les instructions des [analyses de planification avec Microsoft Defender pour Endpoint pour Mac.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/mac-schedule-scan-atp)</span><span class="sxs-lookup"><span data-stu-id="97e35-420">Follow the instructions on [Schedule scans with Microsoft Defender for Endpoint for Mac](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/mac-schedule-scan-atp).</span></span>

## <a name="step-11-deploy-microsoft-defender-for-endpoint-for-macos"></a><span data-ttu-id="97e35-421">Étape 11 : Déployer Microsoft Defender pour le point de terminaison pour macOS</span><span class="sxs-lookup"><span data-stu-id="97e35-421">Step 11: Deploy Microsoft Defender for Endpoint for macOS</span></span>

1. <span data-ttu-id="97e35-422">Accédez à l’endroit où vous avez enregistré `wdav.pkg` .</span><span class="sxs-lookup"><span data-stu-id="97e35-422">Navigate to where you saved `wdav.pkg`.</span></span>

    ![Image de l’explorateur de fichiers wdav pkg](images/8dde76b5463047423f8637c86b05c29d.png)

2. <span data-ttu-id="97e35-424">Renommons-le `wdav_MDM_Contoso_200329.pkg` .</span><span class="sxs-lookup"><span data-stu-id="97e35-424">Rename it to `wdav_MDM_Contoso_200329.pkg`.</span></span>

    ![Image de l’explorateur de fichiers 1 wdavmdmpkg](images/fb2220fed3a530f4b3ef36f600da0c27.png)

3. <span data-ttu-id="97e35-426">Ouvrez le tableau de bord Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="97e35-426">Open the Jamf Pro dashboard.</span></span>

    ![Image des paramètres de configuration jamfpro](images/990742cd9a15ca9fdd37c9f695d1b9f4.png)

4. <span data-ttu-id="97e35-428">Sélectionnez votre ordinateur et cliquez sur l’icône d’engrenage en haut, puis **sélectionnez Gestion de l’ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="97e35-428">Select your computer and click the gear icon at the top, then select **Computer Management**.</span></span>

    ![Image des paramètres de configuration compmgmt](images/b6d671b2f18b89d96c1c8e2ea1991242.png)

5. <span data-ttu-id="97e35-430">Dans **les packages,** **sélectionnez + Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="97e35-430">In **Packages**, select **+ New**.</span></span> 
    <span data-ttu-id="97e35-431">![Une image contenant une description d’volatile a généré automatiquement un nouveau package](images/57aa4d21e2ccc65466bf284701d4e961.png)</span><span class="sxs-lookup"><span data-stu-id="97e35-431">![A picture containing bird Description automatically generated package new](images/57aa4d21e2ccc65466bf284701d4e961.png)</span></span>

6. <span data-ttu-id="97e35-432">Dans **le nouveau package,** entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="97e35-432">In **New Package** Enter the following details:</span></span>

    <span data-ttu-id="97e35-433">**Onglet Général**</span><span class="sxs-lookup"><span data-stu-id="97e35-433">**General tab**</span></span>
    - <span data-ttu-id="97e35-434">Nom complet : laissez-le vide pour le moment.</span><span class="sxs-lookup"><span data-stu-id="97e35-434">Display Name: Leave it blank for now.</span></span> <span data-ttu-id="97e35-435">Parce qu’il sera réinitialisé lorsque vous choisirez votre pkg.</span><span class="sxs-lookup"><span data-stu-id="97e35-435">Because it will be reset when you choose your pkg.</span></span>
    - <span data-ttu-id="97e35-436">Catégorie : Aucun (par défaut)</span><span class="sxs-lookup"><span data-stu-id="97e35-436">Category: None (default)</span></span>
    - <span data-ttu-id="97e35-437">Filename: Choose File</span><span class="sxs-lookup"><span data-stu-id="97e35-437">Filename: Choose File</span></span>

    ![Image de l’onglet Général des paramètres de configuration](images/21de3658bf58b1b767a17358a3f06341.png)

    <span data-ttu-id="97e35-439">Ouvrez le fichier et pointer vers `wdav.pkg` ou `wdav_MDM_Contoso_200329.pkg` .</span><span class="sxs-lookup"><span data-stu-id="97e35-439">Open the file and point it to `wdav.pkg` or `wdav_MDM_Contoso_200329.pkg`.</span></span>
    
    ![Capture d’écran d’une description d’ordinateur générée automatiquement](images/1aa5aaa0a387f4e16ce55b66facc77d1.png)

7. <span data-ttu-id="97e35-441">Sélectionnez **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="97e35-441">Select **Open**.</span></span> <span data-ttu-id="97e35-442">Définissez **le nom complet sur** Microsoft Defender - Protection avancée contre les **menaces et Antivirus Microsoft Defender.**</span><span class="sxs-lookup"><span data-stu-id="97e35-442">Set the **Display Name** to **Microsoft Defender Advanced Threat Protection and Microsoft Defender Antivirus**.</span></span>

    <span data-ttu-id="97e35-443">**Le fichier manifeste n’est** pas requis.</span><span class="sxs-lookup"><span data-stu-id="97e35-443">**Manifest File** is not required.</span></span> <span data-ttu-id="97e35-444">Microsoft Defender - Protection avancée contre les menaces fonctionne sans fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="97e35-444">Microsoft Defender Advanced Threat Protection works without Manifest File.</span></span>
    
    <span data-ttu-id="97e35-445">**Onglet Options**</span><span class="sxs-lookup"><span data-stu-id="97e35-445">**Options tab**</span></span><br> <span data-ttu-id="97e35-446">Conservez les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="97e35-446">Keep default values.</span></span>

    <span data-ttu-id="97e35-447">**Onglet Limitations**</span><span class="sxs-lookup"><span data-stu-id="97e35-447">**Limitations tab**</span></span><br> <span data-ttu-id="97e35-448">Conservez les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="97e35-448">Keep default values.</span></span>
    
     ![Image de l’onglet limitation des paramètres de configuration](images/56dac54634d13b2d3948ab50e8d3ef21.png)
   
8. <span data-ttu-id="97e35-450">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="97e35-450">Select **Save**.</span></span> <span data-ttu-id="97e35-451">Le package est téléchargé vers Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="97e35-451">The package is uploaded to Jamf Pro.</span></span> 

   ![Image des paramètres de configuration pack upl jamf pro](images/33f1ecdc7d4872555418bbc3efe4b7a3.png)

   <span data-ttu-id="97e35-453">Le déploiement du package peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="97e35-453">It can take a few minutes for the package to be available for deployment.</span></span>
   
   ![Image de l’upl du pack de paramètres de configuration](images/1626d138e6309c6e87bfaab64f5ccf7b.png)

9. <span data-ttu-id="97e35-455">Accédez à la page **Stratégies.**</span><span class="sxs-lookup"><span data-stu-id="97e35-455">Navigate to the **Policies** page.</span></span>

    ![Image des paramètres de configuration](images/f878f8efa5ebc92d069f4b8f79f62c7f.png)

10. <span data-ttu-id="97e35-457">Sélectionnez **+ Nouveau** pour créer une stratégie.</span><span class="sxs-lookup"><span data-stu-id="97e35-457">Select **+ New** to create a new policy.</span></span>

    ![Image de la nouvelle stratégie des paramètres de configuration](images/847b70e54ed04787e415f5180414b310.png)


11. <span data-ttu-id="97e35-459">En **général,** entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="97e35-459">In **General** Enter the following details:</span></span>

    - <span data-ttu-id="97e35-460">Nom complet : MDATP Onboarding Contoso 200329 v100.86.92 ou ultérieur</span><span class="sxs-lookup"><span data-stu-id="97e35-460">Display name: MDATP Onboarding Contoso 200329 v100.86.92 or later</span></span>

    ![<span data-ttu-id="97e35-461">Image de configuration settingsmdatponboard</span><span class="sxs-lookup"><span data-stu-id="97e35-461">Image of configuration settingsmdatponboard</span></span> ](images/625ba6d19e8597f05e4907298a454d28.png)

12. <span data-ttu-id="97e35-462">Sélectionnez **l’enregistrement périodique.**</span><span class="sxs-lookup"><span data-stu-id="97e35-462">Select **Recurring Check-in**.</span></span> 
    
    ![Image de vérification des paramètres de configuration](images/68bdbc5754dfc80aa1a024dde0fce7b0.png)

  
13. <span data-ttu-id="97e35-464">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="97e35-464">Select **Save**.</span></span> 
 
14. <span data-ttu-id="97e35-465">Sélectionnez **packages > configurer**.</span><span class="sxs-lookup"><span data-stu-id="97e35-465">Select **Packages > Configure**.</span></span>
 
    ![Image du pack de paramètres de configuration configuré](images/8fb4cc03721e1efb4a15867d5241ebfb.png)

15. <span data-ttu-id="97e35-467">Sélectionnez **le bouton** Ajouter en haut de Microsoft Defender - Protection avancée contre les **menaces et antivirus Microsoft Defender.**</span><span class="sxs-lookup"><span data-stu-id="97e35-467">Select the **Add** button next to **Microsoft Defender Advanced Threat Protection and Microsoft Defender Antivirus**.</span></span>

    ![Image des paramètres de configuration ajoutés par MDATP et MDA](images/526b83fbdbb31265b3d0c1e5fbbdc33a.png)

16. <span data-ttu-id="97e35-469">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="97e35-469">Select **Save**.</span></span>

    ![Image de configuration settingssavimg](images/9d6e5386e652e00715ff348af72671c6.png)

17. <span data-ttu-id="97e35-471">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="97e35-471">Select the **Scope** tab.</span></span>  

    ![Image de scptab des paramètres de configuration](images/8d80fe378a31143db9be0bacf7ddc5a3.png)

18. <span data-ttu-id="97e35-473">Sélectionnez les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="97e35-473">Select the target computers.</span></span>

    ![Image des paramètres de configuration tgtcomp](images/6eda18a64a660fa149575454e54e7156.png)

    <span data-ttu-id="97e35-475">**Scope**</span><span class="sxs-lookup"><span data-stu-id="97e35-475">**Scope**</span></span>
    
    <span data-ttu-id="97e35-476">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="97e35-476">Select **Add**.</span></span>
    
    ![Image des paramètres de configuration ad1img](images/1c08d097829863778d562c10c5f92b67.png)

    ![Image des paramètres de configuration ad2img](images/216253cbfb6ae738b9f13496b9c799fd.png)

    <span data-ttu-id="97e35-479">**Libre-service**</span><span class="sxs-lookup"><span data-stu-id="97e35-479">**Self-Service**</span></span>
    
    ![Image du libre-service des paramètres de configuration](images/c9f85bba3e96d627fe00fc5a8363b83a.png)

19. <span data-ttu-id="97e35-481">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="97e35-481">Select **Done**.</span></span> 

    ![Image des paramètres de configuration do1img](images/99679a7835b0d27d0a222bc3fdaf7f3b.png)

    ![Image des paramètres de configuration do2img](images/632aaab79ae18d0d2b8e0c16b6ba39e2.png)




