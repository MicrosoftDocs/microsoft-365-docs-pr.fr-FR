---
title: Configurer microsoft Defender pour le point de terminaison sur les stratégies macOS dans Jamf Pro
description: Découvrez comment configurer les stratégies Microsoft Defender for Endpoint sur macOS dans Jamf Pro
keywords: policies, microsoft, defender, Microsoft Defender for Endpoint, mac, installation, deploy, uninstallation, intune, jamfpro, macos, defender, mojave, high sierra
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
ms.openlocfilehash: 577eea6e678b6a5d60e5bb8f2fbaaae25d239577
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53230066"
---
# <a name="set-up-the-microsoft-defender-for-endpoint-on-macos-policies-in-jamf-pro"></a><span data-ttu-id="b4f98-104">Configurer microsoft Defender pour le point de terminaison sur les stratégies macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="b4f98-104">Set up the Microsoft Defender for Endpoint on macOS policies in Jamf Pro</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="b4f98-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b4f98-105">**Applies to:**</span></span>

- [<span data-ttu-id="b4f98-106">Defender pour point de terminaison sur Mac</span><span class="sxs-lookup"><span data-stu-id="b4f98-106">Defender for Endpoint on Mac</span></span>](microsoft-defender-endpoint-mac.md)

<span data-ttu-id="b4f98-107">Cette page vous guide à travers les étapes à suivre pour configurer des stratégies macOS dans Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="b4f98-107">This page will guide you through the steps you need to take to set up macOS policies in Jamf Pro.</span></span>

<span data-ttu-id="b4f98-108">Vous devez suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b4f98-108">You'll need to take the following steps:</span></span>

1. [<span data-ttu-id="b4f98-109">Obtenir le package d’intégration Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="b4f98-109">Get the Microsoft Defender for Endpoint onboarding package</span></span>](#step-1-get-the-microsoft-defender-for-endpoint-onboarding-package)

2. [<span data-ttu-id="b4f98-110">Créer un profil de configuration dans Jamf Pro à l’aide du package d’intégration</span><span class="sxs-lookup"><span data-stu-id="b4f98-110">Create a configuration profile in Jamf Pro using the onboarding package</span></span>](#step-2-create-a-configuration-profile-in-jamf-pro-using-the-onboarding-package)

3. [<span data-ttu-id="b4f98-111">Configurer les paramètres de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="b4f98-111">Configure Microsoft Defender for Endpoint settings</span></span>](#step-3-configure-microsoft-defender-for-endpoint-settings)

4. [<span data-ttu-id="b4f98-112">Configurer microsoft Defender pour les paramètres de notification de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b4f98-112">Configure Microsoft Defender for Endpoint notification settings</span></span>](#step-4-configure-notifications-settings)

5. [<span data-ttu-id="b4f98-113">Configurer la mise à jour automatique Microsoft (AutoUpdate)</span><span class="sxs-lookup"><span data-stu-id="b4f98-113">Configure Microsoft AutoUpdate (MAU)</span></span>](#step-5-configure-microsoft-autoupdate-mau)

6. [<span data-ttu-id="b4f98-114">Accorder un accès disque complet à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b4f98-114">Grant full disk access to Microsoft Defender for Endpoint</span></span>](#step-6-grant-full-disk-access-to-microsoft-defender-for-endpoint)

7. [<span data-ttu-id="b4f98-115">Approuver l’extension de noyau pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b4f98-115">Approve Kernel extension for Microsoft Defender for Endpoint</span></span>](#step-7-approve-kernel-extension-for-microsoft-defender-for-endpoint)

8. [<span data-ttu-id="b4f98-116">Approuver les extensions système pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b4f98-116">Approve System extensions for Microsoft Defender for Endpoint</span></span>](#step-8-approve-system-extensions-for-microsoft-defender-for-endpoint)

9. [<span data-ttu-id="b4f98-117">Configurer l’extension réseau</span><span class="sxs-lookup"><span data-stu-id="b4f98-117">Configure Network Extension</span></span>](#step-9-configure-network-extension)

10. [<span data-ttu-id="b4f98-118">Planifier des analyses avec Microsoft Defender pour endpoint sur macOS</span><span class="sxs-lookup"><span data-stu-id="b4f98-118">Schedule scans with Microsoft Defender for Endpoint on macOS</span></span>](/windows/security/threat-protection/microsoft-defender-atp/mac-schedule-scan-atp)

11. [<span data-ttu-id="b4f98-119">Déployer Microsoft Defender pour le point de terminaison sur macOS</span><span class="sxs-lookup"><span data-stu-id="b4f98-119">Deploy Microsoft Defender for Endpoint on macOS</span></span>](#step-11-deploy-microsoft-defender-for-endpoint-on-macos)


## <a name="step-1-get-the-microsoft-defender-for-endpoint-onboarding-package"></a><span data-ttu-id="b4f98-120">Étape 1 : Obtenir le package d’intégration De Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b4f98-120">Step 1: Get the Microsoft Defender for Endpoint onboarding package</span></span>

1. <span data-ttu-id="b4f98-121">In [Centre de sécurité Microsoft Defender](https://securitycenter.microsoft.com), navigate to **Paramètres > Onboarding**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-121">In [Microsoft Defender Security Center](https://securitycenter.microsoft.com), navigate to **Settings > Onboarding**.</span></span>

2. <span data-ttu-id="b4f98-122">Sélectionnez macOS comme système d’exploitation et Gestion des périphériques mobiles/Microsoft Intune comme méthode de déploiement.</span><span class="sxs-lookup"><span data-stu-id="b4f98-122">Select macOS as the operating system and Mobile Device Management / Microsoft Intune as the deployment method.</span></span>

    ![Image de la Centre de sécurité Microsoft Defender](images/onboarding-macos.png)

3. <span data-ttu-id="b4f98-124">Sélectionnez **Télécharger le package d’intégration** (WindowsDefenderATPOnboardingPackage.zip).</span><span class="sxs-lookup"><span data-stu-id="b4f98-124">Select **Download onboarding package** (WindowsDefenderATPOnboardingPackage.zip).</span></span>

4. <span data-ttu-id="b4f98-125">Extraire `WindowsDefenderATPOnboardingPackage.zip` .</span><span class="sxs-lookup"><span data-stu-id="b4f98-125">Extract `WindowsDefenderATPOnboardingPackage.zip`.</span></span>

5. <span data-ttu-id="b4f98-126">Copiez le fichier à votre emplacement préféré.</span><span class="sxs-lookup"><span data-stu-id="b4f98-126">Copy the file to your preferred location.</span></span> <span data-ttu-id="b4f98-127">Par exemple : `C:\Users\JaneDoe_or_JohnDoe.contoso\Downloads\WindowsDefenderATPOnboardingPackage_macOS_MDM_contoso\jamf\WindowsDefenderATPOnboarding.plist`.</span><span class="sxs-lookup"><span data-stu-id="b4f98-127">For example,  `C:\Users\JaneDoe_or_JohnDoe.contoso\Downloads\WindowsDefenderATPOnboardingPackage_macOS_MDM_contoso\jamf\WindowsDefenderATPOnboarding.plist`.</span></span>


## <a name="step-2-create-a-configuration-profile-in-jamf-pro-using-the-onboarding-package"></a><span data-ttu-id="b4f98-128">Étape 2 : Créer un profil de configuration dans Jamf Pro à l’aide du package d’intégration</span><span class="sxs-lookup"><span data-stu-id="b4f98-128">Step 2: Create a configuration profile in Jamf Pro using the onboarding package</span></span>

1. <span data-ttu-id="b4f98-129">Recherchez le `WindowsDefenderATPOnboarding.plist` fichier dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="b4f98-129">Locate the file `WindowsDefenderATPOnboarding.plist` from the previous section.</span></span>

   ![Image du fichier WindowsDefenderATPOnboarding](images/plist-onboarding-file.png)


2. <span data-ttu-id="b4f98-131">Dans le tableau de bord Pro Jamf, sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-131">In the Jamf Pro dashboard, select **New**.</span></span>

    ![Image de création d’un tableau de bord jamf Pro tableau de bord](images/jamf-pro-configure-profile.png)

3. <span data-ttu-id="b4f98-133">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="b4f98-133">Enter the following details:</span></span>

   <span data-ttu-id="b4f98-134">**Général**</span><span class="sxs-lookup"><span data-stu-id="b4f98-134">**General**</span></span>
   - <span data-ttu-id="b4f98-135">Nom : intégration MDATP pour macOS</span><span class="sxs-lookup"><span data-stu-id="b4f98-135">Name: MDATP onboarding for macOS</span></span>
   - <span data-ttu-id="b4f98-136">Description : intégration PEPT MDATP pour macOS</span><span class="sxs-lookup"><span data-stu-id="b4f98-136">Description: MDATP EDR onboarding for macOS</span></span>
   - <span data-ttu-id="b4f98-137">Catégorie : Aucun</span><span class="sxs-lookup"><span data-stu-id="b4f98-137">Category: None</span></span>
   - <span data-ttu-id="b4f98-138">Méthode de distribution : installer automatiquement</span><span class="sxs-lookup"><span data-stu-id="b4f98-138">Distribution Method: Install Automatically</span></span>
   - <span data-ttu-id="b4f98-139">Niveau : niveau ordinateur</span><span class="sxs-lookup"><span data-stu-id="b4f98-139">Level: Computer Level</span></span>

4. <span data-ttu-id="b4f98-140">In **Application & Custom Paramètres** select **Configure**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-140">In **Application & Custom Settings** select **Configure**.</span></span>

    ![Image de configuration de l’application et des paramètres personnalisés](images/jamfpro-mac-profile.png)

5. <span data-ttu-id="b4f98-142">Sélectionnez **Télécharger fichier (fichier PLIST),** puis dans **Domaine** de préférence, entrez `com.microsoft.wdav.atp` :</span><span class="sxs-lookup"><span data-stu-id="b4f98-142">Select **Upload File (PLIST file)** then in **Preference Domain** enter: `com.microsoft.wdav.atp`.</span></span>

    ![Image du fichier de téléchargement plist jamfpro](images/jamfpro-plist-upload.png)

    ![Image du fichier de liste des propriétés de fichier de téléchargement](images/jamfpro-plist-file.png)

6. <span data-ttu-id="b4f98-145">Sélectionnez **Ouvrir** et sélectionnez le fichier d’intégration.</span><span class="sxs-lookup"><span data-stu-id="b4f98-145">Select **Open** and select the onboarding file.</span></span>

    ![Image du fichier d’intégration](images/jamfpro-plist-file-onboard.png)

7. <span data-ttu-id="b4f98-147">Sélectionnez **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-147">Select **Upload**.</span></span>

    ![Image du téléchargement d’un fichier plist](images/jamfpro-upload-plist.png)

8. <span data-ttu-id="b4f98-149">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="b4f98-149">Select the **Scope** tab.</span></span>

    ![Image de l’onglet d’étendue](images/jamfpro-scope-tab.png)

9. <span data-ttu-id="b4f98-151">Sélectionnez les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="b4f98-151">Select the target computers.</span></span>

    ![Image des ordinateurs cibles](images/jamfpro-target-computer.png)

    ![Image des cibles](images/jamfpro-targets.png)

10. <span data-ttu-id="b4f98-154">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-154">Select **Save**.</span></span>

    ![Image des ordinateurs cibles de déploiement](images/jamfpro-deployment-target.png)

    ![Image des ordinateurs cibles sélectionnés](images/jamfpro-target-selected.png)

11. <span data-ttu-id="b4f98-157">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-157">Select **Done**.</span></span>

    ![Image des ordinateurs de groupe cibles](images/jamfpro-target-group.png)

    ![Liste des profils de configuration](images/jamfpro-configuration-policies.png)

## <a name="step-3-configure-microsoft-defender-for-endpoint-settings"></a><span data-ttu-id="b4f98-160">Étape 3 : Configurer Microsoft Defender pour les paramètres de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b4f98-160">Step 3: Configure Microsoft Defender for Endpoint settings</span></span>

<span data-ttu-id="b4f98-161">Vous pouvez utiliser jamf Pro GUI pour modifier les paramètres individuels de la configuration Microsoft Defender ou utiliser la méthode héritée en créant un Plist de configuration dans un éditeur de texte et en le téléchargeant dans jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="b4f98-161">You can either use JAMF Pro GUI to edit individual settings of the Microsoft Defender configuration, or use the legacy method by creating a configuration Plist in a text editor, and uploading it to JAMF Pro.</span></span>

<span data-ttu-id="b4f98-162">Notez que vous devez utiliser exact comme domaine de préférence , Microsoft Defender utilise uniquement ce nom et pour `com.microsoft.wdav` charger ses  `com.microsoft.wdav.ext` paramètres gérés !</span><span class="sxs-lookup"><span data-stu-id="b4f98-162">Note that you must use exact `com.microsoft.wdav` as the **Preference Domain**, Microsoft Defender uses only this name and `com.microsoft.wdav.ext` to load its managed settings!</span></span>

<span data-ttu-id="b4f98-163">(La version peut être utilisée dans de rares cas lorsque vous préférez utiliser la méthode GUI, mais que vous devez également configurer un paramètre qui n’a pas encore été ajouté au `com.microsoft.wdav.ext` schéma.)</span><span class="sxs-lookup"><span data-stu-id="b4f98-163">(The `com.microsoft.wdav.ext` version may be used in rare cases when you prefer to use GUI method, but also need to configure a setting that has not been added to the schema yet.)</span></span>

### <a name="gui-method"></a><span data-ttu-id="b4f98-164">Méthode GUI</span><span class="sxs-lookup"><span data-stu-id="b4f98-164">GUI method</span></span>

1. <span data-ttu-id="b4f98-165">Téléchargez schema.jsfichier à partir du référentiel [GitHub Defender](https://github.com/microsoft/mdatp-xplat/tree/master/macos/schema) et enregistrez-le dans un fichier local :</span><span class="sxs-lookup"><span data-stu-id="b4f98-165">Download schema.json file from [Defender's GitHub repository](https://github.com/microsoft/mdatp-xplat/tree/master/macos/schema) and save it to a local file:</span></span>

    ```bash
    curl -o ~/Documents/schema.json https://raw.githubusercontent.com/microsoft/mdatp-xplat/master/macos/schema/schema.json
    ```

2. <span data-ttu-id="b4f98-166">Créez un profil de configuration sous Ordinateurs -> profils de configuration, entrez les détails suivants sous **l’onglet Général** :</span><span class="sxs-lookup"><span data-stu-id="b4f98-166">Create a new Configuration Profile under Computers -> Configuration Profiles, enter the following details on the **General** tab:</span></span>

    ![Nouveau profil](images/644e0f3af40c29e80ca1443535b2fe32.png)

    - <span data-ttu-id="b4f98-168">Nom : paramètres de configuration MDAV MDATP</span><span class="sxs-lookup"><span data-stu-id="b4f98-168">Name: MDATP MDAV configuration settings</span></span>
    - <span data-ttu-id="b4f98-169">Description :\<blank\></span><span class="sxs-lookup"><span data-stu-id="b4f98-169">Description:\<blank\></span></span>
    - <span data-ttu-id="b4f98-170">Catégorie : Aucun (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b4f98-170">Category: None (default)</span></span>
    - <span data-ttu-id="b4f98-171">Niveau : niveau ordinateur (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b4f98-171">Level: Computer Level (default)</span></span>
    - <span data-ttu-id="b4f98-172">Méthode de distribution : installer automatiquement (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b4f98-172">Distribution Method: Install Automatically (default)</span></span>

3. <span data-ttu-id="b4f98-173">Faites défiler vers le bas jusqu’à l’onglet Application &  Custom  **Paramètres,** sélectionnez **Applications** externes, cliquez sur Ajouter et utiliser le schéma personnalisé comme source à utiliser pour le domaine de préférence.</span><span class="sxs-lookup"><span data-stu-id="b4f98-173">Scroll down to the **Application & Custom Settings** tab, select **External Applications**, click **Add** and use **Custom Schema** as Source to use for the preference domain.</span></span>

    ![Ajouter un schéma personnalisé](images/4137189bc3204bb09eed3aabc41afd78.png)

4. <span data-ttu-id="b4f98-175">Entrez comme domaine de préférence, cliquez sur Ajouter un schéma et Télécharger le schema.jssur le fichier téléchargé à `com.microsoft.wdav` l’étape  1. </span><span class="sxs-lookup"><span data-stu-id="b4f98-175">Enter `com.microsoft.wdav` as the Preference Domain, click on **Add Schema** and **Upload** the schema.json file downloaded on Step 1.</span></span> <span data-ttu-id="b4f98-176">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-176">Click **Save**.</span></span>

    ![Télécharger schéma](images/a6f9f556037c42fabcfdcb1b697244cf.png)

5. <span data-ttu-id="b4f98-178">Vous pouvez voir tous les paramètres de configuration de Microsoft Defender pris en charge ci-dessous, sous **Propriétés de domaine de préférence.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-178">You can see all supported Microsoft Defender configuration settings below, under **Preference Domain Properties**.</span></span> <span data-ttu-id="b4f98-179">Cliquez **sur Ajouter/Supprimer des** propriétés pour sélectionner les paramètres à gérer, puis cliquez sur **OK** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="b4f98-179">Click **Add/Remove properties** to select the settings that you want to be managed, and click **Ok** to save your changes.</span></span> <span data-ttu-id="b4f98-180">(Paramètres non sélectionné ne sera pas inclus dans la configuration gérée, un utilisateur final pourra configurer ces paramètres sur ses ordinateurs.)</span><span class="sxs-lookup"><span data-stu-id="b4f98-180">(Settings left unselected will not be included into the managed configuration, an end user will be able to configure those settings on their machines.)</span></span>

    ![Sélectionner les paramètres gérés](images/817b3b760d11467abe9bdd519513f54f.png)

6. <span data-ttu-id="b4f98-182">Modifiez les valeurs des paramètres en valeurs souhaitées.</span><span class="sxs-lookup"><span data-stu-id="b4f98-182">Change values of the settings to desired values.</span></span> <span data-ttu-id="b4f98-183">Vous pouvez cliquer **sur Plus d’informations** pour obtenir la documentation d’un paramètre particulier.</span><span class="sxs-lookup"><span data-stu-id="b4f98-183">You can click **More information** to get documentation for a particular setting.</span></span> <span data-ttu-id="b4f98-184">(Vous pouvez cliquer sur **aperçu Plist** pour inspecter l’apparence de la liste de configuration.</span><span class="sxs-lookup"><span data-stu-id="b4f98-184">(You may click **Plist preview** to inspect what the configuration plist will look like.</span></span> <span data-ttu-id="b4f98-185">Cliquez **sur Éditeur de formulaire** pour revenir à l’éditeur visuel.)</span><span class="sxs-lookup"><span data-stu-id="b4f98-185">Click **Form editor** to return to the visual editor.)</span></span>

    ![Modifier les valeurs des paramètres](images/a14a79efd5c041bb8974cb5b12b3a9b6.png)

7. <span data-ttu-id="b4f98-187">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="b4f98-187">Select the **Scope** tab.</span></span>

    ![Étendue du profil de configuration](images/9fc17529e5577eefd773c658ec576a7d.png)

8. <span data-ttu-id="b4f98-189">Sélectionnez **Le groupe d’ordinateurs de Contoso.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-189">Select **Contoso's Machine Group**.</span></span>

9. <span data-ttu-id="b4f98-190">Sélectionnez **Ajouter,** puis **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-190">Select **Add**, then select **Save**.</span></span>

    ![Paramètres de configuration : ajouter](images/cf30438b5512ac89af1d11cbf35219a6.png)

    ![Paramètres de configuration : enregistrer](images/6f093e42856753a3955cab7ee14f12d9.png)

10. <span data-ttu-id="b4f98-193">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-193">Select **Done**.</span></span> <span data-ttu-id="b4f98-194">Vous verrez le nouveau profil **de configuration.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-194">You'll see the new **Configuration profile**.</span></span>

    ![Paramètres de configuration : terminé](images/dd55405106da0dfc2f50f8d4525b01c8.png)

<span data-ttu-id="b4f98-196">Microsoft Defender ajoute de nouveaux paramètres au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="b4f98-196">Microsoft Defender adds new settings over time.</span></span> <span data-ttu-id="b4f98-197">Ces nouveaux paramètres seront ajoutés au schéma et une nouvelle version sera publiée sur Github.</span><span class="sxs-lookup"><span data-stu-id="b4f98-197">These new settings will be added to the schema, and a new version will be published to Github.</span></span>
<span data-ttu-id="b4f98-198">Il vous suffit de télécharger un schéma mis à jour, de modifier  le profil de configuration existant et de modifier le schéma sous l’onglet Application **& Custom Paramètres.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-198">All you need to do to have updates is to download an updated schema, edit existing configuration profile, and **Edit schema** at the **Application & Custom Settings** tab.</span></span>

### <a name="legacy-method"></a><span data-ttu-id="b4f98-199">Méthode héritée</span><span class="sxs-lookup"><span data-stu-id="b4f98-199">Legacy method</span></span>

1. <span data-ttu-id="b4f98-200">Utilisez les paramètres de configuration de Microsoft Defender pour les points de terminaison suivants :</span><span class="sxs-lookup"><span data-stu-id="b4f98-200">Use the following Microsoft Defender for Endpoint configuration settings:</span></span>

    - <span data-ttu-id="b4f98-201">enableRealTimeProtection</span><span class="sxs-lookup"><span data-stu-id="b4f98-201">enableRealTimeProtection</span></span>
    - <span data-ttu-id="b4f98-202">passiveMode</span><span class="sxs-lookup"><span data-stu-id="b4f98-202">passiveMode</span></span>

    >[!NOTE]
    ><span data-ttu-id="b4f98-203">Non désactivé par défaut, si vous envisagez d’exécuter un antivirus tiers pour macOS, définissez-le sur `true` .</span><span class="sxs-lookup"><span data-stu-id="b4f98-203">Not turned on by default, if you are planning to run a third-party AV for macOS, set it to `true`.</span></span>

    - <span data-ttu-id="b4f98-204">exclusions</span><span class="sxs-lookup"><span data-stu-id="b4f98-204">exclusions</span></span>
    - <span data-ttu-id="b4f98-205">excludedPath</span><span class="sxs-lookup"><span data-stu-id="b4f98-205">excludedPath</span></span>
    - <span data-ttu-id="b4f98-206">excludedFileExtension</span><span class="sxs-lookup"><span data-stu-id="b4f98-206">excludedFileExtension</span></span>
    - <span data-ttu-id="b4f98-207">excludedFileName</span><span class="sxs-lookup"><span data-stu-id="b4f98-207">excludedFileName</span></span>
    - <span data-ttu-id="b4f98-208">exclusionsMergePolicy</span><span class="sxs-lookup"><span data-stu-id="b4f98-208">exclusionsMergePolicy</span></span>
    - <span data-ttu-id="b4f98-209">allowedThreats</span><span class="sxs-lookup"><span data-stu-id="b4f98-209">allowedThreats</span></span>

    >[!NOTE]
    ><span data-ttu-id="b4f98-210">EICAR est sur l’exemple, si vous êtes en train de passer par une preuve de concept, supprimez-le en particulier si vous testez EICAR.</span><span class="sxs-lookup"><span data-stu-id="b4f98-210">EICAR is on the sample, if you are going through a proof-of-concept, remove it especially if you are testing EICAR.</span></span>

    - <span data-ttu-id="b4f98-211">disallowedThreatActions</span><span class="sxs-lookup"><span data-stu-id="b4f98-211">disallowedThreatActions</span></span>
    - <span data-ttu-id="b4f98-212">potentially_unwanted_application</span><span class="sxs-lookup"><span data-stu-id="b4f98-212">potentially_unwanted_application</span></span>
    - <span data-ttu-id="b4f98-213">archive_bomb</span><span class="sxs-lookup"><span data-stu-id="b4f98-213">archive_bomb</span></span>
    - <span data-ttu-id="b4f98-214">cloudService</span><span class="sxs-lookup"><span data-stu-id="b4f98-214">cloudService</span></span>
    - <span data-ttu-id="b4f98-215">automaticSampleSubmission</span><span class="sxs-lookup"><span data-stu-id="b4f98-215">automaticSampleSubmission</span></span>
    - <span data-ttu-id="b4f98-216">balises</span><span class="sxs-lookup"><span data-stu-id="b4f98-216">tags</span></span>
    - <span data-ttu-id="b4f98-217">hideStatusMenuIcon</span><span class="sxs-lookup"><span data-stu-id="b4f98-217">hideStatusMenuIcon</span></span>

     <span data-ttu-id="b4f98-218">Pour plus d’informations, [voir Liste des propriétés pour le profil de configuration Jamf.](mac-preferences.md#property-list-for-jamf-configuration-profile)</span><span class="sxs-lookup"><span data-stu-id="b4f98-218">For information, see [Property list for Jamf configuration profile](mac-preferences.md#property-list-for-jamf-configuration-profile).</span></span>

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

2. <span data-ttu-id="b4f98-219">Enregistrez le fichier sous `MDATP_MDAV_configuration_settings.plist` .</span><span class="sxs-lookup"><span data-stu-id="b4f98-219">Save the file as `MDATP_MDAV_configuration_settings.plist`.</span></span>

3. <span data-ttu-id="b4f98-220">Dans le tableau de bord Jamf Pro, ouvrez **Ordinateurs,** et il y a des **profils de configuration.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-220">In the Jamf Pro dashboard, open **Computers**, and there **Configuration Profiles**.</span></span> <span data-ttu-id="b4f98-221">Cliquez sur \**Nouveau (* et basculez vers **l’onglet** Général.</span><span class="sxs-lookup"><span data-stu-id="b4f98-221">Click \**New(* and switch to the **General** tab.</span></span>

    ![Nouveau profil](images/644e0f3af40c29e80ca1443535b2fe32.png)

4. <span data-ttu-id="b4f98-223">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="b4f98-223">Enter the following details:</span></span>

    <span data-ttu-id="b4f98-224">**Général**</span><span class="sxs-lookup"><span data-stu-id="b4f98-224">**General**</span></span>

    - <span data-ttu-id="b4f98-225">Nom : paramètres de configuration MDAV MDATP</span><span class="sxs-lookup"><span data-stu-id="b4f98-225">Name: MDATP MDAV configuration settings</span></span>
    - <span data-ttu-id="b4f98-226">Description :\<blank\></span><span class="sxs-lookup"><span data-stu-id="b4f98-226">Description:\<blank\></span></span>
    - <span data-ttu-id="b4f98-227">Catégorie : Aucun (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b4f98-227">Category: None (default)</span></span>
    - <span data-ttu-id="b4f98-228">Méthode de distribution : installer automatiquement (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b4f98-228">Distribution Method: Install Automatically(default)</span></span>
    - <span data-ttu-id="b4f98-229">Niveau : Niveau ordinateur (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b4f98-229">Level: Computer Level(default)</span></span>

    ![Image des paramètres de configuration MDAV MDATP](images/3160906404bc5a2edf84d1d015894e3b.png)

5. <span data-ttu-id="b4f98-231">In **Application & Custom Paramètres** select **Configure**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-231">In **Application & Custom Settings** select **Configure**.</span></span>

    ![Image de l’application et des paramètres personnalisés](images/e1cc1e48ec9d5d688087b4d771e668d2.png)

6. <span data-ttu-id="b4f98-233">Sélectionnez **Télécharger fichier (fichier PLIST).**</span><span class="sxs-lookup"><span data-stu-id="b4f98-233">Select **Upload File (PLIST file)**.</span></span>

    ![Image du fichier plist des paramètres de configuration](images/6f85269276b2278eca4bce84f935f87b.png)

7. <span data-ttu-id="b4f98-235">In **Preferences Domain**, enter `com.microsoft.wdav` , then select Télécharger **PLIST File**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-235">In **Preferences Domain**, enter `com.microsoft.wdav`, then select  **Upload PLIST File**.</span></span>

    ![Image du domaine des préférences de paramètres de configuration](images/db15f147dd959e872a044184711d7d46.png)

8. <span data-ttu-id="b4f98-237">Sélectionnez **Choisir un fichier.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-237">Select **Choose File**.</span></span>

    ![Image des paramètres de configuration choisir un fichier](images/526e978761fc571cca06907da7b01fd6.png)

9. <span data-ttu-id="b4f98-239">Sélectionnez **le MDATP_MDAV_configuration_settings.plist,** puis sélectionnez **Ouvrir.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-239">Select the **MDATP_MDAV_configuration_settings.plist**, then select **Open**.</span></span>

    ![Image des paramètres de configuration mdatpmdav](images/98acea3750113b8dbab334296e833003.png)

10. <span data-ttu-id="b4f98-241">Sélectionnez **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-241">Select **Upload**.</span></span>

    ![Image du téléchargement des paramètres de configuration](images/0adb21c13206861ba9b30a879ade93d3.png)

    ![Image de l’image de téléchargement des paramètres de configuration](images/f624de59b3cc86e3e2d32ae5de093e02.png)

    >[!NOTE]
    ><span data-ttu-id="b4f98-244">Si vous téléchargez le fichier Intune, vous obtenez l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="b4f98-244">If you happen to upload the Intune file, you'll get the following error:</span></span><br>
    ><span data-ttu-id="b4f98-245">![Image du téléchargement de fichiers intune des paramètres de configuration](images/8e69f867664668796a3b2904896f0436.png)</span><span class="sxs-lookup"><span data-stu-id="b4f98-245">![Image of configuration settings intune file upload](images/8e69f867664668796a3b2904896f0436.png)</span></span>


11. <span data-ttu-id="b4f98-246">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-246">Select **Save**.</span></span>

    ![Image de l’image Enregistrer l’image des paramètres de configuration](images/1b6b5a4edcb42d97f1e70a6a0fa48e3a.png)

12. <span data-ttu-id="b4f98-248">Le fichier est téléchargé.</span><span class="sxs-lookup"><span data-stu-id="b4f98-248">The file is uploaded.</span></span>

    ![Image de l’image téléchargée du fichier de paramètres de configuration](images/33e2b2a1611fdddf6b5b79e54496e3bb.png)

    ![Image du fichier de paramètres de configuration téléchargé](images/a422e57fe8d45689227e784443e51bd1.png)

13. <span data-ttu-id="b4f98-251">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="b4f98-251">Select the **Scope** tab.</span></span>

    ![Image de l’étendue des paramètres de configuration](images/9fc17529e5577eefd773c658ec576a7d.png)

14. <span data-ttu-id="b4f98-253">Sélectionnez **Le groupe d’ordinateurs de Contoso.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-253">Select **Contoso's Machine Group**.</span></span>

15. <span data-ttu-id="b4f98-254">Sélectionnez **Ajouter,** puis **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-254">Select **Add**, then select **Save**.</span></span>

    ![Image des paramètres de configuration addsav](images/cf30438b5512ac89af1d11cbf35219a6.png)

    ![Image de l’ajout d’enregistrer les paramètres de configuration](images/6f093e42856753a3955cab7ee14f12d9.png)

16. <span data-ttu-id="b4f98-257">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-257">Select **Done**.</span></span> <span data-ttu-id="b4f98-258">Vous verrez le nouveau profil **de configuration.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-258">You'll see the new **Configuration profile**.</span></span>

    ![Image de l’image de profil de configuration des paramètres de configuration](images/dd55405106da0dfc2f50f8d4525b01c8.png)

## <a name="step-4-configure-notifications-settings"></a><span data-ttu-id="b4f98-260">Étape 4 : Configurer les paramètres de notification</span><span class="sxs-lookup"><span data-stu-id="b4f98-260">Step 4: Configure notifications settings</span></span>

<span data-ttu-id="b4f98-261">Ces étapes s’appliquent à macOS 10.15 (Genre), ou une nouveauté.</span><span class="sxs-lookup"><span data-stu-id="b4f98-261">These steps are applicable of macOS 10.15 (Catalina) or newer.</span></span>

1. <span data-ttu-id="b4f98-262">Dans le tableau de bord Jamf Pro, **sélectionnez Ordinateurs,** puis **Profils de configuration.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-262">In the Jamf Pro dashboard, select **Computers**, then **Configuration Profiles**.</span></span>

2. <span data-ttu-id="b4f98-263">Cliquez **sur** Nouveau, puis entrez les détails suivants pour **options**:</span><span class="sxs-lookup"><span data-stu-id="b4f98-263">Click **New**, and enter the following details for **Options**:</span></span>

    - <span data-ttu-id="b4f98-264">Onglet **Général**:</span><span class="sxs-lookup"><span data-stu-id="b4f98-264">Tab **General**:</span></span>
        - <span data-ttu-id="b4f98-265">**Name**: Paramètres de notification MDAV MDATP</span><span class="sxs-lookup"><span data-stu-id="b4f98-265">**Name**: MDATP MDAV Notification settings</span></span>
        - <span data-ttu-id="b4f98-266">**Description**: macOS 10.15 (Contrôle) ou une nouveauté</span><span class="sxs-lookup"><span data-stu-id="b4f98-266">**Description**: macOS 10.15 (Catalina) or newer</span></span>
        - <span data-ttu-id="b4f98-267">**Catégorie**: Aucun *(par défaut)*</span><span class="sxs-lookup"><span data-stu-id="b4f98-267">**Category**: None *(default)*</span></span>
        - <span data-ttu-id="b4f98-268">**Méthode de distribution**: installer automatiquement *(par défaut)*</span><span class="sxs-lookup"><span data-stu-id="b4f98-268">**Distribution Method**: Install Automatically *(default)*</span></span>
        - <span data-ttu-id="b4f98-269">**Niveau**: niveau ordinateur *(par défaut)*</span><span class="sxs-lookup"><span data-stu-id="b4f98-269">**Level**: Computer Level *(default)*</span></span>

        ![Image du nouvel écran de profil de configuration macOS](images/c9820a5ff84aaf21635c04a23a97ca93.png)

    - <span data-ttu-id="b4f98-271">Tab **Notifications,** click **Add**, and enter the following values:</span><span class="sxs-lookup"><span data-stu-id="b4f98-271">Tab **Notifications**, click **Add**, and enter the following values:</span></span>
        - <span data-ttu-id="b4f98-272">**ID d’offre groupée**: `com.microsoft.wdav.tray`</span><span class="sxs-lookup"><span data-stu-id="b4f98-272">**Bundle ID**: `com.microsoft.wdav.tray`</span></span>
        - <span data-ttu-id="b4f98-273">**Alertes critiques**: cliquez sur **Désactiver**</span><span class="sxs-lookup"><span data-stu-id="b4f98-273">**Critical Alerts**: Click **Disable**</span></span>
        - <span data-ttu-id="b4f98-274">**Notifications :** cliquez sur **Activer**</span><span class="sxs-lookup"><span data-stu-id="b4f98-274">**Notifications**: Click **Enable**</span></span>
        - <span data-ttu-id="b4f98-275">**Type d’alerte bannière**: sélectionner **Inclure** **et temporaire** *(par défaut)*</span><span class="sxs-lookup"><span data-stu-id="b4f98-275">**Banner alert type**: Select **Include** and **Temporary** *(default)*</span></span>
        - <span data-ttu-id="b4f98-276">**Notifications sur l’écran de verrouillage**: cliquez sur **Masquer**</span><span class="sxs-lookup"><span data-stu-id="b4f98-276">**Notifications on lock screen**: Click **Hide**</span></span>
        - <span data-ttu-id="b4f98-277">**Notifications dans le Centre de notifications**: cliquez sur **Afficher**</span><span class="sxs-lookup"><span data-stu-id="b4f98-277">**Notifications in Notification Center**: Click **Display**</span></span>
        - <span data-ttu-id="b4f98-278">**Icône d’application de badge**: cliquez sur **Afficher**</span><span class="sxs-lookup"><span data-stu-id="b4f98-278">**Badge app icon**: Click **Display**</span></span>

        ![Image du bac de notifications mdatpmdav des paramètres de configuration](images/7f9138053dbcbf928e5182ee7b295ebe.png)

    - <span data-ttu-id="b4f98-280">Tab **Notifications**, click **Add** one more time, scroll down to **New Notifications Paramètres**</span><span class="sxs-lookup"><span data-stu-id="b4f98-280">Tab **Notifications**, click **Add** one more time, scroll down to **New Notifications Settings**</span></span>
        - <span data-ttu-id="b4f98-281">**ID d’offre groupée**: `com.microsoft.autoupdate2`</span><span class="sxs-lookup"><span data-stu-id="b4f98-281">**Bundle ID**: `com.microsoft.autoupdate2`</span></span>
        - <span data-ttu-id="b4f98-282">Configurer le reste des paramètres sur les mêmes valeurs que ci-dessus</span><span class="sxs-lookup"><span data-stu-id="b4f98-282">Configure the rest of the settings to the same values as above</span></span>

        ![Image des paramètres de configuration mdatpmdav notifications mau](images/4bac6ce277aedfb4a674f2d9fcb2599a.png)

        <span data-ttu-id="b4f98-284">Notez que vous avez maintenant deux « tables » avec des configurations de notification, une pour l’ID d’offre groupée : **com.microsoft.wdav.tray** et une autre pour l’ID d’offre groupée : **com.microsoft.autoupdate2**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-284">Note that now you have two 'tables' with notification configurations, one for **Bundle ID: com.microsoft.wdav.tray**, and another for **Bundle ID: com.microsoft.autoupdate2**.</span></span> <span data-ttu-id="b4f98-285">Bien que vous pouvez configurer les paramètres d’alerte en fonction de vos  besoins,  les ID d’offre groupée doivent être exactement les mêmes que ceux décrits précédemment, et le commutateur Inclure doit être en cours pour les **notifications.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-285">While you can configure alert settings per your requirements, Bundle IDs must be exactly the same as described before, and **Include** switch must be **On** for **Notifications**.</span></span>

3. <span data-ttu-id="b4f98-286">Sélectionnez **l’onglet** Étendue, puis **sélectionnez Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-286">Select the **Scope** tab, then select **Add**.</span></span>

    ![Image de l’étendue ajouter des paramètres de configuration](images/441aa2ecd36abadcdd8aed03556080b5.png)

4. <span data-ttu-id="b4f98-288">Sélectionnez **Le groupe d’ordinateurs de Contoso.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-288">Select **Contoso's Machine Group**.</span></span>

5. <span data-ttu-id="b4f98-289">Sélectionnez **Ajouter,** puis **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-289">Select **Add**, then select **Save**.</span></span>

    ![Image des paramètres de configuration contoso machine grp save](images/09a275e321268e5e3ac0c0865d3e2db5.png)

    ![Image des paramètres de configuration pour ajouter l’enregistrer](images/4d2d1d4ee13d3f840f425924c3df0d51.png)

6. <span data-ttu-id="b4f98-292">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-292">Select **Done**.</span></span> <span data-ttu-id="b4f98-293">Vous verrez le nouveau profil **de configuration.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-293">You'll see the new **Configuration profile**.</span></span>
    <span data-ttu-id="b4f98-294">![Image du paramètre de configuration terminé img](images/633ad26b8bf24ec683c98b2feb884bdf.png)</span><span class="sxs-lookup"><span data-stu-id="b4f98-294">![Image of configuration setting done img](images/633ad26b8bf24ec683c98b2feb884bdf.png)</span></span>

## <a name="step-5-configure-microsoft-autoupdate-mau"></a><span data-ttu-id="b4f98-295">Étape 5 : Configurer la mise à jour automatique Microsoft (AutoUpdate)</span><span class="sxs-lookup"><span data-stu-id="b4f98-295">Step 5: Configure Microsoft AutoUpdate (MAU)</span></span>

1. <span data-ttu-id="b4f98-296">Utilisez les paramètres de configuration de Microsoft Defender pour les points de terminaison suivants :</span><span class="sxs-lookup"><span data-stu-id="b4f98-296">Use the following Microsoft Defender for Endpoint configuration settings:</span></span>

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

2. <span data-ttu-id="b4f98-297">Enregistrez-le sous `MDATP_MDAV_MAU_settings.plist` .</span><span class="sxs-lookup"><span data-stu-id="b4f98-297">Save it as `MDATP_MDAV_MAU_settings.plist`.</span></span>

3. <span data-ttu-id="b4f98-298">Dans le tableau de bord Pro Jamf, sélectionnez **Général**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-298">In the Jamf Pro dashboard, select **General**.</span></span>

    ![Image de l’image générale du paramètre de configuration](images/eaba2a23dd34f73bf59e826217ba6f15.png)

4. <span data-ttu-id="b4f98-300">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="b4f98-300">Enter the following details:</span></span>

    <span data-ttu-id="b4f98-301">**Général**</span><span class="sxs-lookup"><span data-stu-id="b4f98-301">**General**</span></span>

    - <span data-ttu-id="b4f98-302">Name: MDATP MDAV MAU settings</span><span class="sxs-lookup"><span data-stu-id="b4f98-302">Name: MDATP MDAV MAU settings</span></span>
    - <span data-ttu-id="b4f98-303">Description : Paramètres de mise à jour automatique Microsoft pour MDATP pour macOS</span><span class="sxs-lookup"><span data-stu-id="b4f98-303">Description: Microsoft AutoUpdate settings for MDATP for macOS</span></span>
    - <span data-ttu-id="b4f98-304">Catégorie : Aucun (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b4f98-304">Category: None (default)</span></span>
    - <span data-ttu-id="b4f98-305">Méthode de distribution : installer automatiquement (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b4f98-305">Distribution Method: Install Automatically(default)</span></span>
    - <span data-ttu-id="b4f98-306">Niveau : Niveau ordinateur (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b4f98-306">Level: Computer Level(default)</span></span>

5. <span data-ttu-id="b4f98-307">In **Application & Custom Paramètres** select **Configure**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-307">In **Application & Custom Settings** select **Configure**.</span></span>

    ![Image de l’application de paramètre de configuration et des paramètres personnalisés](images/1f72e9c15eaafcabf1504397e99be311.png)

6. <span data-ttu-id="b4f98-309">Sélectionnez **Télécharger fichier (fichier PLIST).**</span><span class="sxs-lookup"><span data-stu-id="b4f98-309">Select **Upload File (PLIST file)**.</span></span>

    ![Image de la liste des paramètres de configuration](images/1213872db5833aa8be535da57653219f.png)

7. <span data-ttu-id="b4f98-311">In **Preference Domain** enter: , then select Télécharger `com.microsoft.autoupdate2` **PLIST File**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-311">In **Preference Domain** enter: `com.microsoft.autoupdate2`, then select **Upload PLIST File**.</span></span>

    ![Image du domaine préf du paramètre de configuration](images/1213872db5833aa8be535da57653219f.png)

8. <span data-ttu-id="b4f98-313">Sélectionnez **Choisir un fichier.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-313">Select **Choose File**.</span></span>

    ![Image du fichier choosefile du paramètre de configuration](images/335aff58950ce62d1dabc289ecdce9ed.png)

9. <span data-ttu-id="b4f98-315">Sélectionnez **MDATP_MDAV_MAU_settings.plist.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-315">Select **MDATP_MDAV_MAU_settings.plist**.</span></span>

    ![Image des paramètres de configuration mdatpmdavmau](images/a26bd4967cd54bb113a2c8d32894c3de.png)

10. <span data-ttu-id="b4f98-317">Sélectionnez **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-317">Select **Upload**.</span></span>
    <span data-ttu-id="b4f98-318">![Image du délimitement de configuration de configuration](images/4239ca0528efb0734e4ca0b490bfb22d.png)</span><span class="sxs-lookup"><span data-stu-id="b4f98-318">![Image of configuration setting uplimage](images/4239ca0528efb0734e4ca0b490bfb22d.png)</span></span>

    ![Image de la configuration de la configuration de la configuration](images/4ec20e72c8aed9a4c16912e01692436a.png)

11. <span data-ttu-id="b4f98-320">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-320">Select **Save**.</span></span>

    ![Image du paramètre de configuration saveimg](images/253274b33e74f3f5b8d475cf8692ce4e.png)

12. <span data-ttu-id="b4f98-322">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="b4f98-322">Select the **Scope** tab.</span></span>

     ![Image du paramètre de configuration scopetab](images/10ab98358b2d602f3f67618735fa82fb.png)

13. <span data-ttu-id="b4f98-324">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-324">Select **Add**.</span></span>

    ![Image du paramètre de configuration addimg1](images/56e6f6259b9ce3c1706ed8d666ae4947.png)

    ![Image du paramètre de configuration addimg2](images/38c67ee1905c4747c3b26c8eba57726b.png)

    ![Image du paramètre de configuration addimg3](images/321ba245f14743c1d5d51c15e99deecc.png)

14. <span data-ttu-id="b4f98-328">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-328">Select **Done**.</span></span>

    ![Image du paramètre de configuration doneimage](images/ba44cdb77e4781aa8b940fb83e3c21f7.png)

## <a name="step-6-grant-full-disk-access-to-microsoft-defender-for-endpoint"></a><span data-ttu-id="b4f98-330">Étape 6 : Accorder un accès disque complet à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b4f98-330">Step 6: Grant full disk access to Microsoft Defender for Endpoint</span></span>

1. <span data-ttu-id="b4f98-331">Dans le tableau de bord Jamf Pro, sélectionnez **Profils de configuration.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-331">In the Jamf Pro dashboard, select **Configuration Profiles**.</span></span>

    ![Image du profil de configuration des paramètres de configuration](images/264493cd01e62c7085659d6fdc26dc91.png)

2. <span data-ttu-id="b4f98-333">Sélectionnez **+ Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-333">Select **+ New**.</span></span>

3. <span data-ttu-id="b4f98-334">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="b4f98-334">Enter the following details:</span></span>

    <span data-ttu-id="b4f98-335">**Général**</span><span class="sxs-lookup"><span data-stu-id="b4f98-335">**General**</span></span>
    - <span data-ttu-id="b4f98-336">Nom : MDATP MDAV - accorder un accès disque total à PEPT et antivirus</span><span class="sxs-lookup"><span data-stu-id="b4f98-336">Name: MDATP MDAV - grant Full Disk Access to EDR and AV</span></span>
    - <span data-ttu-id="b4f98-337">Description : sur macOS Ou une nouveauté, le nouveau contrôle de stratégie des préférences de confidentialité</span><span class="sxs-lookup"><span data-stu-id="b4f98-337">Description: On macOS Catalina or newer, the new Privacy Preferences Policy Control</span></span>
    - <span data-ttu-id="b4f98-338">Catégorie : Aucun</span><span class="sxs-lookup"><span data-stu-id="b4f98-338">Category: None</span></span>
    - <span data-ttu-id="b4f98-339">Méthode de distribution : installer automatiquement</span><span class="sxs-lookup"><span data-stu-id="b4f98-339">Distribution method: Install Automatically</span></span>
    - <span data-ttu-id="b4f98-340">Niveau : niveau ordinateur</span><span class="sxs-lookup"><span data-stu-id="b4f98-340">Level: Computer level</span></span>


    ![Image du paramètre de configuration général](images/ba3d40399e1a6d09214ecbb2b341923f.png)

4. <span data-ttu-id="b4f98-342">In **Configure Privacy Preferences Policy Control** select **Configure**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-342">In **Configure Privacy Preferences Policy Control** select **Configure**.</span></span>

    ![Image du contrôle de stratégie de confidentialité de la configuration](images/715ae7ec8d6a262c489f94d14e1e51bb.png)

5. <span data-ttu-id="b4f98-344">Dans **le contrôle de stratégie des préférences de confidentialité,** entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="b4f98-344">In **Privacy Preferences Policy Control**, enter the following details:</span></span>

    - <span data-ttu-id="b4f98-345">Identificateur : `com.microsoft.wdav`</span><span class="sxs-lookup"><span data-stu-id="b4f98-345">Identifier: `com.microsoft.wdav`</span></span>
    - <span data-ttu-id="b4f98-346">Type d’identificateur : ID d’offre groupée</span><span class="sxs-lookup"><span data-stu-id="b4f98-346">Identifier Type: Bundle ID</span></span>
    - <span data-ttu-id="b4f98-347">Conditions requises pour le code : `identifier "com.microsoft.wdav" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span><span class="sxs-lookup"><span data-stu-id="b4f98-347">Code Requirement: `identifier "com.microsoft.wdav" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span></span>


    ![Image des détails du contrôle de stratégie de confidentialité des paramètres de configuration](images/22cb439de958101c0a12f3038f905b27.png)

6. <span data-ttu-id="b4f98-349">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-349">Select **+ Add**.</span></span>

    ![Image du paramètre de configuration ajouter la stratégie système à tous les fichiers](images/bd93e78b74c2660a0541af4690dd9485.png)

    - <span data-ttu-id="b4f98-351">Sous Application ou service : définir sur **SystemPolicyAllFiles**</span><span class="sxs-lookup"><span data-stu-id="b4f98-351">Under App or service: Set to **SystemPolicyAllFiles**</span></span>

    - <span data-ttu-id="b4f98-352">Sous « accès » : définir sur **Autoriser**</span><span class="sxs-lookup"><span data-stu-id="b4f98-352">Under "access": Set to **Allow**</span></span>

7. <span data-ttu-id="b4f98-353">Sélectionnez **Enregistrer** (et non celui en bas à droite).</span><span class="sxs-lookup"><span data-stu-id="b4f98-353">Select **Save** (not the one at the bottom right).</span></span>

    ![Image des images d’enregistrer les paramètres de configuration](images/6de50b4a897408ddc6ded56a09c09fe2.png)

8. <span data-ttu-id="b4f98-355">Cliquez sur le `+` signe en de côté **d’App Access** pour ajouter une nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="b4f98-355">Click the `+` sign next to **App Access** to add a new entry.</span></span>

    ![Image de l’accès aux applications de paramètre de configuration](images/tcc-add-entry.png)

9. <span data-ttu-id="b4f98-357">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="b4f98-357">Enter the following details:</span></span>

    - <span data-ttu-id="b4f98-358">Identificateur : `com.microsoft.wdav.epsext`</span><span class="sxs-lookup"><span data-stu-id="b4f98-358">Identifier: `com.microsoft.wdav.epsext`</span></span>
    - <span data-ttu-id="b4f98-359">Type d’identificateur : ID d’offre groupée</span><span class="sxs-lookup"><span data-stu-id="b4f98-359">Identifier Type: Bundle ID</span></span>
    - <span data-ttu-id="b4f98-360">Conditions requises pour le code : `identifier "com.microsoft.wdav.epsext" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span><span class="sxs-lookup"><span data-stu-id="b4f98-360">Code Requirement: `identifier "com.microsoft.wdav.epsext" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span></span>

10. <span data-ttu-id="b4f98-361">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-361">Select **+ Add**.</span></span>

    ![Image de l’entrée tcc epsext du paramètre de configuration](images/tcc-epsext-entry.png)

    - <span data-ttu-id="b4f98-363">Sous Application ou service : définir sur **SystemPolicyAllFiles**</span><span class="sxs-lookup"><span data-stu-id="b4f98-363">Under App or service: Set to **SystemPolicyAllFiles**</span></span>

    - <span data-ttu-id="b4f98-364">Sous « accès » : définir sur **Autoriser**</span><span class="sxs-lookup"><span data-stu-id="b4f98-364">Under "access": Set to **Allow**</span></span>

11. <span data-ttu-id="b4f98-365">Sélectionnez **Enregistrer** (et non celui en bas à droite).</span><span class="sxs-lookup"><span data-stu-id="b4f98-365">Select **Save** (not the one at the bottom right).</span></span>

    ![Image du paramètre de configuration tcc epsext image2](images/tcc-epsext-entry2.png)

12. <span data-ttu-id="b4f98-367">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="b4f98-367">Select the **Scope** tab.</span></span>

    ![Image de l’étendue du paramètre de configuration](images/2c49b16cd112729b3719724f581e6882.png)

13. <span data-ttu-id="b4f98-369">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-369">Select **+ Add**.</span></span>

    ![Image de l’addimage du paramètre de configuration](images/57cef926d1b9260fb74a5f460cee887a.png)

14. <span data-ttu-id="b4f98-371">Sélectionnez **Groupes d’ordinateurs** > **sous Nom** de > sélectionnez Groupe machine de **Contoso.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-371">Select **Computer Groups** > under **Group Name** > select **Contoso's MachineGroup**.</span></span>

    ![Image du paramètre de configuration contoso machinegrp](images/368d35b3d6179af92ffdbfd93b226b69.png)

15. <span data-ttu-id="b4f98-373">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-373">Select **Add**.</span></span>

16. <span data-ttu-id="b4f98-374">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-374">Select **Save**.</span></span>

17. <span data-ttu-id="b4f98-375">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-375">Select **Done**.</span></span>

    ![Image de donimg de paramètre de configuration](images/809cef630281b64b8f07f20913b0039b.png)

    ![Image du paramètre de configuration donimg2](images/6c8b406ee224335a8c65d06953dc756e.png)

<span data-ttu-id="b4f98-378">Vous pouvez également télécharger [fulldisk.mobileconfig](https://github.com/microsoft/mdatp-xplat/blob/master/macos/mobileconfig/profiles/fulldisk.mobileconfig) et le télécharger dans les profils de configuration JAMF, comme décrit dans [Deploying Custom Configuration Profiles using Jamf Pro| Méthode 2 : Télécharger profil de configuration à Jamf Pro](https://www.jamf.com/jamf-nation/articles/648/deploying-custom-configuration-profiles-using-jamf-pro).</span><span class="sxs-lookup"><span data-stu-id="b4f98-378">Alternatively, you can download [fulldisk.mobileconfig](https://github.com/microsoft/mdatp-xplat/blob/master/macos/mobileconfig/profiles/fulldisk.mobileconfig) and upload it to JAMF Configuration Profiles as described in [Deploying Custom Configuration Profiles using Jamf Pro|Method 2: Upload a Configuration Profile to Jamf Pro](https://www.jamf.com/jamf-nation/articles/648/deploying-custom-configuration-profiles-using-jamf-pro).</span></span>

## <a name="step-7-approve-kernel-extension-for-microsoft-defender-for-endpoint"></a><span data-ttu-id="b4f98-379">Étape 7 : Approuver l’extension de noyau pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b4f98-379">Step 7: Approve Kernel extension for Microsoft Defender for Endpoint</span></span>

> [!CAUTION]
> <span data-ttu-id="b4f98-380">Les appareils Apple Silicon (M1) ne supportent pas KEXT.</span><span class="sxs-lookup"><span data-stu-id="b4f98-380">Apple Silicon (M1) devices do not support KEXT.</span></span> <span data-ttu-id="b4f98-381">L’installation d’un profil de configuration constitué de stratégies KEXT échoue sur ces appareils.</span><span class="sxs-lookup"><span data-stu-id="b4f98-381">Installation of a configuration profile consisting KEXT policies will fail on these devices.</span></span>

1. <span data-ttu-id="b4f98-382">Dans les **profils de configuration,** **sélectionnez + Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-382">In the **Configuration Profiles**, select **+ New**.</span></span>

    ![Capture d’écran d’un billet de réseau social Description généré automatiquement](images/6c8b406ee224335a8c65d06953dc756e.png)

2. <span data-ttu-id="b4f98-384">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="b4f98-384">Enter the following details:</span></span>

    <span data-ttu-id="b4f98-385">**Général**</span><span class="sxs-lookup"><span data-stu-id="b4f98-385">**General**</span></span>

    - <span data-ttu-id="b4f98-386">Name: MDATP MDAV Kernel Extension</span><span class="sxs-lookup"><span data-stu-id="b4f98-386">Name: MDATP MDAV Kernel Extension</span></span>
    - <span data-ttu-id="b4f98-387">Description : extension de noyau MDATP (kext)</span><span class="sxs-lookup"><span data-stu-id="b4f98-387">Description: MDATP kernel extension (kext)</span></span>
    - <span data-ttu-id="b4f98-388">Catégorie : Aucun</span><span class="sxs-lookup"><span data-stu-id="b4f98-388">Category: None</span></span>
    - <span data-ttu-id="b4f98-389">Méthode de distribution : installer automatiquement</span><span class="sxs-lookup"><span data-stu-id="b4f98-389">Distribution Method: Install Automatically</span></span>
    - <span data-ttu-id="b4f98-390">Niveau : niveau ordinateur</span><span class="sxs-lookup"><span data-stu-id="b4f98-390">Level: Computer Level</span></span>

    ![Image du noyau mdatpmdav des paramètres de configuration](images/24e290f5fc309932cf41f3a280d22c14.png)

3. <span data-ttu-id="b4f98-392">In **Configure Approved Kernel Extensions** select **Configure**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-392">In **Configure Approved Kernel Extensions** select **Configure**.</span></span>

    ![Image de l’ext de noyau approuvé des paramètres de configuration](images/30be88b63abc5e8dde11b73f1b1ade6a.png)


4. <span data-ttu-id="b4f98-394">Dans **Extensions de noyau approuvées,** entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="b4f98-394">In **Approved Kernel Extensions** Enter the following details:</span></span>

    - <span data-ttu-id="b4f98-395">Nom complet : Microsoft Corp.</span><span class="sxs-lookup"><span data-stu-id="b4f98-395">Display Name: Microsoft Corp.</span></span>
    - <span data-ttu-id="b4f98-396">ID d’équipe : UBF8T346G9</span><span class="sxs-lookup"><span data-stu-id="b4f98-396">Team ID: UBF8T346G9</span></span>

    ![Image de l’extension de noyau appr des paramètres de configuration](images/39cf120d3ac3652292d8d1b6d057bd60.png)

5. <span data-ttu-id="b4f98-398">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="b4f98-398">Select the **Scope** tab.</span></span>

    ![Image de l’onglet d’étendue des paramètres de configuration img](images/0df36fc308ba569db204ee32db3fb40a.png)

6. <span data-ttu-id="b4f98-400">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-400">Select **+ Add**.</span></span>

7. <span data-ttu-id="b4f98-401">Sélectionnez **Groupes d’ordinateurs** > **sous Nom du** > sélectionnez Groupe ordinateur de **Contoso.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-401">Select **Computer Groups** > under **Group Name** > select **Contoso's Machine Group**.</span></span>

8. <span data-ttu-id="b4f98-402">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-402">Select **+ Add**.</span></span>

    ![Image des paramètres de configuration pour ajouter des images](images/0dde8a4c41110dbc398c485433a81359.png)

9. <span data-ttu-id="b4f98-404">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-404">Select **Save**.</span></span>

    ![Image de l’économiserie des paramètres de configuration](images/0add8019b85a453b47fa5c402c72761b.png)

10. <span data-ttu-id="b4f98-406">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-406">Select **Done**.</span></span>

    ![Image des paramètres de configuration doneimag](images/1c9bd3f68db20b80193dac18f33c22d0.png)

<span data-ttu-id="b4f98-408">Vous pouvez également télécharger [kext.mobileconfig](https://github.com/microsoft/mdatp-xplat/blob/master/macos/mobileconfig/profiles/kext.mobileconfig) et le télécharger dans les profils de configuration JAMF, comme décrit dans [Deploying Custom Configuration Profiles using Jamf Pro| Méthode 2 : Télécharger profil de configuration à Jamf Pro](https://www.jamf.com/jamf-nation/articles/648/deploying-custom-configuration-profiles-using-jamf-pro).</span><span class="sxs-lookup"><span data-stu-id="b4f98-408">Alternatively, you can download [kext.mobileconfig](https://github.com/microsoft/mdatp-xplat/blob/master/macos/mobileconfig/profiles/kext.mobileconfig) and upload it to JAMF Configuration Profiles as described in [Deploying Custom Configuration Profiles using Jamf Pro|Method 2: Upload a Configuration Profile to Jamf Pro](https://www.jamf.com/jamf-nation/articles/648/deploying-custom-configuration-profiles-using-jamf-pro).</span></span>

## <a name="step-8-approve-system-extensions-for-microsoft-defender-for-endpoint"></a><span data-ttu-id="b4f98-409">Étape 8 : Approuver les extensions système pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b4f98-409">Step 8: Approve System extensions for Microsoft Defender for Endpoint</span></span>

1. <span data-ttu-id="b4f98-410">Dans les **profils de configuration,** **sélectionnez + Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-410">In the **Configuration Profiles**, select **+ New**.</span></span>

    ![Capture d’écran d’un billet de réseau social Description généré automatiquement](images/6c8b406ee224335a8c65d06953dc756e.png)

2. <span data-ttu-id="b4f98-412">Entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="b4f98-412">Enter the following details:</span></span>

    <span data-ttu-id="b4f98-413">**Général**</span><span class="sxs-lookup"><span data-stu-id="b4f98-413">**General**</span></span>

    - <span data-ttu-id="b4f98-414">Name: MDATP MDAV System Extensions</span><span class="sxs-lookup"><span data-stu-id="b4f98-414">Name: MDATP MDAV System Extensions</span></span>
    - <span data-ttu-id="b4f98-415">Description : extensions système MDATP</span><span class="sxs-lookup"><span data-stu-id="b4f98-415">Description: MDATP system extensions</span></span>
    - <span data-ttu-id="b4f98-416">Catégorie : Aucun</span><span class="sxs-lookup"><span data-stu-id="b4f98-416">Category: None</span></span>
    - <span data-ttu-id="b4f98-417">Méthode de distribution : installer automatiquement</span><span class="sxs-lookup"><span data-stu-id="b4f98-417">Distribution Method: Install Automatically</span></span>
    - <span data-ttu-id="b4f98-418">Niveau : niveau ordinateur</span><span class="sxs-lookup"><span data-stu-id="b4f98-418">Level: Computer Level</span></span>

    ![Image du nouveau prof des paramètres de configuration](images/sysext-new-profile.png)

3. <span data-ttu-id="b4f98-420">Dans **les extensions système,** **sélectionnez Configurer.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-420">In **System Extensions** select **Configure**.</span></span>

   ![Image de configuration sysext des paramètres de configuration](images/sysext-configure.png)

4. <span data-ttu-id="b4f98-422">Dans **les extensions système,** entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="b4f98-422">In **System Extensions** enter the following details:</span></span>

   - <span data-ttu-id="b4f98-423">Nom complet : Microsoft Corp. System Extensions</span><span class="sxs-lookup"><span data-stu-id="b4f98-423">Display Name: Microsoft Corp. System Extensions</span></span>
   - <span data-ttu-id="b4f98-424">Types d’extension système : extensions système autorisées</span><span class="sxs-lookup"><span data-stu-id="b4f98-424">System Extension Types: Allowed System Extensions</span></span>
   - <span data-ttu-id="b4f98-425">Identificateur d’équipe : UBF8T346G9</span><span class="sxs-lookup"><span data-stu-id="b4f98-425">Team Identifier: UBF8T346G9</span></span>
   - <span data-ttu-id="b4f98-426">Extensions système autorisées :</span><span class="sxs-lookup"><span data-stu-id="b4f98-426">Allowed System Extensions:</span></span>
     - <span data-ttu-id="b4f98-427">**com.microsoft.wdav.epsext**</span><span class="sxs-lookup"><span data-stu-id="b4f98-427">**com.microsoft.wdav.epsext**</span></span>
     - <span data-ttu-id="b4f98-428">**com.microsoft.wdav.netext**</span><span class="sxs-lookup"><span data-stu-id="b4f98-428">**com.microsoft.wdav.netext**</span></span>

    ![Image des paramètres de configuration sysextconfig2](images/sysext-configure2.png)

5. <span data-ttu-id="b4f98-430">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="b4f98-430">Select the **Scope** tab.</span></span>

    ![Image de l’étendue des paramètres de configuration](images/0df36fc308ba569db204ee32db3fb40a.png)

6. <span data-ttu-id="b4f98-432">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-432">Select **+ Add**.</span></span>

7. <span data-ttu-id="b4f98-433">Sélectionnez **Groupes d’ordinateurs** > **sous Nom du** > sélectionnez Groupe ordinateur de **Contoso.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-433">Select **Computer Groups** > under **Group Name** > select **Contoso's Machine Group**.</span></span>

8. <span data-ttu-id="b4f98-434">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-434">Select **+ Add**.</span></span>

   ![Image de l’addima des paramètres de configuration](images/0dde8a4c41110dbc398c485433a81359.png)

9. <span data-ttu-id="b4f98-436">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-436">Select **Save**.</span></span>

   ![Image de l’étendue sysext des paramètres de configuration](images/sysext-scope.png)

10. <span data-ttu-id="b4f98-438">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-438">Select **Done**.</span></span>

    ![Image des paramètres de configuration sysext-final](images/sysext-final.png)

## <a name="step-9-configure-network-extension"></a><span data-ttu-id="b4f98-440">Étape 9 : Configurer l’extension réseau</span><span class="sxs-lookup"><span data-stu-id="b4f98-440">Step 9: Configure Network Extension</span></span>

<span data-ttu-id="b4f98-441">Dans le cadre des fonctionnalités de détection et de réponse des points de terminaison, Microsoft Defender for Endpoint sur macOS inspecte le trafic de socket et signale ces informations au portail Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="b4f98-441">As part of the Endpoint Detection and Response capabilities, Microsoft Defender for Endpoint on macOS inspects socket traffic and reports this information to the Microsoft Defender Security Center portal.</span></span> <span data-ttu-id="b4f98-442">La stratégie suivante permet à l’extension réseau d’effectuer cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="b4f98-442">The following policy allows the network extension to perform this functionality.</span></span>

<span data-ttu-id="b4f98-443">Ces étapes s’appliquent à macOS 10.15 (Genre), ou une nouveauté.</span><span class="sxs-lookup"><span data-stu-id="b4f98-443">These steps are applicable of macOS 10.15 (Catalina) or newer.</span></span>

1. <span data-ttu-id="b4f98-444">Dans le tableau de bord Jamf Pro, **sélectionnez Ordinateurs,** puis **Profils de configuration.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-444">In the Jamf Pro dashboard, select **Computers**, then **Configuration Profiles**.</span></span>

2. <span data-ttu-id="b4f98-445">Cliquez **sur** Nouveau, puis entrez les détails suivants pour **options**:</span><span class="sxs-lookup"><span data-stu-id="b4f98-445">Click **New**, and enter the following details for **Options**:</span></span>

    - <span data-ttu-id="b4f98-446">Onglet **Général**:</span><span class="sxs-lookup"><span data-stu-id="b4f98-446">Tab **General**:</span></span>
        - <span data-ttu-id="b4f98-447">**Nom**: Extension réseau Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="b4f98-447">**Name**: Microsoft Defender ATP Network Extension</span></span>
        - <span data-ttu-id="b4f98-448">**Description**: macOS 10.15 (Contrôle) ou une nouveauté</span><span class="sxs-lookup"><span data-stu-id="b4f98-448">**Description**: macOS 10.15 (Catalina) or newer</span></span>
        - <span data-ttu-id="b4f98-449">**Catégorie**: Aucun *(par défaut)*</span><span class="sxs-lookup"><span data-stu-id="b4f98-449">**Category**: None *(default)*</span></span>
        - <span data-ttu-id="b4f98-450">**Méthode de distribution**: installer automatiquement *(par défaut)*</span><span class="sxs-lookup"><span data-stu-id="b4f98-450">**Distribution Method**: Install Automatically *(default)*</span></span>
        - <span data-ttu-id="b4f98-451">**Niveau**: niveau ordinateur *(par défaut)*</span><span class="sxs-lookup"><span data-stu-id="b4f98-451">**Level**: Computer Level *(default)*</span></span>

    - <span data-ttu-id="b4f98-452">Filtre **de contenu d’onglet**:</span><span class="sxs-lookup"><span data-stu-id="b4f98-452">Tab **Content Filter**:</span></span>
        - <span data-ttu-id="b4f98-453">**Nom du** filtre : filtre de contenu Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="b4f98-453">**Filter Name**: Microsoft Defender ATP Content Filter</span></span>
        - <span data-ttu-id="b4f98-454">**Identificateur**: `com.microsoft.wdav`</span><span class="sxs-lookup"><span data-stu-id="b4f98-454">**Identifier**: `com.microsoft.wdav`</span></span>
        - <span data-ttu-id="b4f98-455">Laisser **l’adresse du service,** **l’organisation,** **le nom d’utilisateur,** le mot de **passe,** **le certificat** vide (**Inclure** *n’est pas* sélectionné)</span><span class="sxs-lookup"><span data-stu-id="b4f98-455">Leave **Service Address**, **Organization**, **User Name**, **Password**, **Certificate** blank (**Include** is *not* selected)</span></span>
        - <span data-ttu-id="b4f98-456">**Filter Order**: Inspector</span><span class="sxs-lookup"><span data-stu-id="b4f98-456">**Filter Order**: Inspector</span></span>
        - <span data-ttu-id="b4f98-457">**Filtre de socket**: `com.microsoft.wdav.netext`</span><span class="sxs-lookup"><span data-stu-id="b4f98-457">**Socket Filter**: `com.microsoft.wdav.netext`</span></span>
        - <span data-ttu-id="b4f98-458">**Exigence désignée par le filtre de socket**: `identifier "com.microsoft.wdav.netext" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span><span class="sxs-lookup"><span data-stu-id="b4f98-458">**Socket Filter Designated Requirement**: `identifier "com.microsoft.wdav.netext" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span></span>
        - <span data-ttu-id="b4f98-459">Laisser **les champs Filtre réseau** vides **(Inclure** *n’est pas* sélectionné)</span><span class="sxs-lookup"><span data-stu-id="b4f98-459">Leave **Network Filter** fields blank (**Include** is *not* selected)</span></span>

        <span data-ttu-id="b4f98-460">Notez que **l’identificateur,** le filtre de **socket** et le **filtre de socket désignent** les valeurs exactes requises comme spécifié ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="b4f98-460">Note that **Identifier**, **Socket Filter** and **Socket Filter Designated Requirement** exact values as specified above.</span></span>

        ![Image du paramètre de configuration mdatpmdav](images/netext-create-profile.png)

3. <span data-ttu-id="b4f98-462">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="b4f98-462">Select the **Scope** tab.</span></span>

   ![Image de l’onglet système des paramètres de configuration](images/0df36fc308ba569db204ee32db3fb40a.png)

4. <span data-ttu-id="b4f98-464">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-464">Select **+ Add**.</span></span>

5. <span data-ttu-id="b4f98-465">Sélectionnez **Groupes d’ordinateurs** > **sous Nom du** > sélectionnez Groupe ordinateur de **Contoso.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-465">Select **Computer Groups** > under **Group Name** > select **Contoso's Machine Group**.</span></span>

6. <span data-ttu-id="b4f98-466">Sélectionnez **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-466">Select **+ Add**.</span></span>

    ![Image des paramètres de configuration adim](images/0dde8a4c41110dbc398c485433a81359.png)

7. <span data-ttu-id="b4f98-468">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-468">Select **Save**.</span></span>

    ![Image des paramètres de configuration savimg netextscop](images/netext-scope.png)

8. <span data-ttu-id="b4f98-470">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-470">Select **Done**.</span></span>

    ![Image de paramètres de configuration netextfinal](images/netext-final.png)

<span data-ttu-id="b4f98-472">Vous pouvez également télécharger [netfilter.mobileconfig](https://github.com/microsoft/mdatp-xplat/blob/master/macos/mobileconfig/profiles/netfilter.mobileconfig) et le télécharger dans les profils de configuration JAMF, comme décrit dans [Deploying Custom Configuration Profiles using Jamf Pro| Méthode 2 : Télécharger profil de configuration à Jamf Pro](https://www.jamf.com/jamf-nation/articles/648/deploying-custom-configuration-profiles-using-jamf-pro).</span><span class="sxs-lookup"><span data-stu-id="b4f98-472">Alternatively, you can download [netfilter.mobileconfig](https://github.com/microsoft/mdatp-xplat/blob/master/macos/mobileconfig/profiles/netfilter.mobileconfig) and upload it to JAMF Configuration Profiles as described in [Deploying Custom Configuration Profiles using Jamf Pro|Method 2: Upload a Configuration Profile to Jamf Pro](https://www.jamf.com/jamf-nation/articles/648/deploying-custom-configuration-profiles-using-jamf-pro).</span></span>


## <a name="step-10-schedule-scans-with-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="b4f98-473">Étape 10 : Planifier des analyses avec Microsoft Defender pour Endpoint sur macOS</span><span class="sxs-lookup"><span data-stu-id="b4f98-473">Step 10: Schedule scans with Microsoft Defender for Endpoint on macOS</span></span>
<span data-ttu-id="b4f98-474">Suivez les instructions des [analyses de planification avec Microsoft Defender for Endpoint sur macOS.](/windows/security/threat-protection/microsoft-defender-atp/mac-schedule-scan-atp)</span><span class="sxs-lookup"><span data-stu-id="b4f98-474">Follow the instructions on [Schedule scans with Microsoft Defender for Endpoint on macOS](/windows/security/threat-protection/microsoft-defender-atp/mac-schedule-scan-atp).</span></span>


## <a name="step-11-deploy-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="b4f98-475">Étape 11 : Déployer Microsoft Defender pour endpoint sur macOS</span><span class="sxs-lookup"><span data-stu-id="b4f98-475">Step 11: Deploy Microsoft Defender for Endpoint on macOS</span></span>

1. <span data-ttu-id="b4f98-476">Accédez à l’endroit où vous avez `wdav.pkg` enregistré.</span><span class="sxs-lookup"><span data-stu-id="b4f98-476">Navigate to where you saved `wdav.pkg`.</span></span>

    ![Image de l’explorateur de fichiers wdav pkg](images/8dde76b5463047423f8637c86b05c29d.png)

2. <span data-ttu-id="b4f98-478">Renommons-le `wdav_MDM_Contoso_200329.pkg` .</span><span class="sxs-lookup"><span data-stu-id="b4f98-478">Rename it to `wdav_MDM_Contoso_200329.pkg`.</span></span>

    ![Image de l’explorateur de fichiers 1 wdavmdmpkg](images/fb2220fed3a530f4b3ef36f600da0c27.png)

3. <span data-ttu-id="b4f98-480">Ouvrez le tableau de bord Pro Jamf.</span><span class="sxs-lookup"><span data-stu-id="b4f98-480">Open the Jamf Pro dashboard.</span></span>

    ![Image des paramètres de configuration jamfpro](images/990742cd9a15ca9fdd37c9f695d1b9f4.png)

4. <span data-ttu-id="b4f98-482">Sélectionnez votre ordinateur et cliquez sur l’icône d’engrenage en haut, puis sélectionnez **Gestion de l’ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-482">Select your computer and click the gear icon at the top, then select **Computer Management**.</span></span>

    ![Image des paramètres de configuration compmgmt](images/b6d671b2f18b89d96c1c8e2ea1991242.png)

5. <span data-ttu-id="b4f98-484">Dans **les packages,** **sélectionnez + Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-484">In **Packages**, select **+ New**.</span></span>
    <span data-ttu-id="b4f98-485">![Une image contenant une description d’volatile a généré automatiquement un nouveau package](images/57aa4d21e2ccc65466bf284701d4e961.png)</span><span class="sxs-lookup"><span data-stu-id="b4f98-485">![A picture containing bird Description automatically generated package new](images/57aa4d21e2ccc65466bf284701d4e961.png)</span></span>

6. <span data-ttu-id="b4f98-486">Dans **le nouveau package,** entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="b4f98-486">In **New Package** Enter the following details:</span></span>

    <span data-ttu-id="b4f98-487">**Onglet Général**</span><span class="sxs-lookup"><span data-stu-id="b4f98-487">**General tab**</span></span>
    - <span data-ttu-id="b4f98-488">Nom complet : laissez-le vide pour le moment.</span><span class="sxs-lookup"><span data-stu-id="b4f98-488">Display Name: Leave it blank for now.</span></span> <span data-ttu-id="b4f98-489">Parce qu’il sera réinitialisé lorsque vous choisirez votre pkg.</span><span class="sxs-lookup"><span data-stu-id="b4f98-489">Because it will be reset when you choose your pkg.</span></span>
    - <span data-ttu-id="b4f98-490">Catégorie : Aucun (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b4f98-490">Category: None (default)</span></span>
    - <span data-ttu-id="b4f98-491">Filename: Choose File</span><span class="sxs-lookup"><span data-stu-id="b4f98-491">Filename: Choose File</span></span>

    ![Image de l’onglet Général des paramètres de configuration](images/21de3658bf58b1b767a17358a3f06341.png)

    <span data-ttu-id="b4f98-493">Ouvrez le fichier et pointer vers `wdav.pkg` ou `wdav_MDM_Contoso_200329.pkg` .</span><span class="sxs-lookup"><span data-stu-id="b4f98-493">Open the file and point it to `wdav.pkg` or `wdav_MDM_Contoso_200329.pkg`.</span></span>

    ![Capture d’écran d’une description d’ordinateur générée automatiquement](images/1aa5aaa0a387f4e16ce55b66facc77d1.png)

7. <span data-ttu-id="b4f98-495">Sélectionnez **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-495">Select **Open**.</span></span> <span data-ttu-id="b4f98-496">Définissez **le nom complet sur** Microsoft Defender - Protection avancée contre les **menaces et Antivirus Microsoft Defender**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-496">Set the **Display Name** to **Microsoft Defender Advanced Threat Protection and Microsoft Defender Antivirus**.</span></span>

    <span data-ttu-id="b4f98-497">**Le fichier manifeste n’est** pas requis.</span><span class="sxs-lookup"><span data-stu-id="b4f98-497">**Manifest File** is not required.</span></span> <span data-ttu-id="b4f98-498">Microsoft Defender pour le point de terminaison fonctionne sans fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="b4f98-498">Microsoft Defender for Endpoint works without Manifest File.</span></span>

    <span data-ttu-id="b4f98-499">**Onglet Options**</span><span class="sxs-lookup"><span data-stu-id="b4f98-499">**Options tab**</span></span><br> <span data-ttu-id="b4f98-500">Conservez les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="b4f98-500">Keep default values.</span></span>

    <span data-ttu-id="b4f98-501">**Onglet Limitations**</span><span class="sxs-lookup"><span data-stu-id="b4f98-501">**Limitations tab**</span></span><br> <span data-ttu-id="b4f98-502">Conservez les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="b4f98-502">Keep default values.</span></span>

     ![Image de l’onglet Limitation des paramètres de configuration](images/56dac54634d13b2d3948ab50e8d3ef21.png)

8. <span data-ttu-id="b4f98-504">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-504">Select **Save**.</span></span> <span data-ttu-id="b4f98-505">Le package est téléchargé vers Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="b4f98-505">The package is uploaded to Jamf Pro.</span></span>

   ![Image des paramètres de configuration pack upl jamf pro](images/33f1ecdc7d4872555418bbc3efe4b7a3.png)

   <span data-ttu-id="b4f98-507">Le déploiement du package peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="b4f98-507">It can take a few minutes for the package to be available for deployment.</span></span>

   ![Image de l’upl du pack de paramètres de configuration](images/1626d138e6309c6e87bfaab64f5ccf7b.png)

9. <span data-ttu-id="b4f98-509">Accédez à la page **Stratégies.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-509">Navigate to the **Policies** page.</span></span>

    ![Image des paramètres de configuration des locations](images/f878f8efa5ebc92d069f4b8f79f62c7f.png)

10. <span data-ttu-id="b4f98-511">Sélectionnez **+ Nouveau** pour créer une stratégie.</span><span class="sxs-lookup"><span data-stu-id="b4f98-511">Select **+ New** to create a new policy.</span></span>

    ![Image de la nouvelle stratégie des paramètres de configuration](images/847b70e54ed04787e415f5180414b310.png)


11. <span data-ttu-id="b4f98-513">En **général,** entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="b4f98-513">In **General** Enter the following details:</span></span>

    - <span data-ttu-id="b4f98-514">Nom complet : Intégration MDATP Contoso 200329 v100.86.92 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="b4f98-514">Display name: MDATP Onboarding Contoso 200329 v100.86.92 or later</span></span>

    ![Image de configuration settingsmdatponboard](images/625ba6d19e8597f05e4907298a454d28.png)

12. <span data-ttu-id="b4f98-516">Sélectionnez **l’enregistrement périodique.**</span><span class="sxs-lookup"><span data-stu-id="b4f98-516">Select **Recurring Check-in**.</span></span>

    ![Image de vérification des paramètres de configuration](images/68bdbc5754dfc80aa1a024dde0fce7b0.png)


13. <span data-ttu-id="b4f98-518">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-518">Select **Save**.</span></span>

14. <span data-ttu-id="b4f98-519">Sélectionnez **packages > configurer**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-519">Select **Packages > Configure**.</span></span>

    ![Image du pack de paramètres de configuration configuré](images/8fb4cc03721e1efb4a15867d5241ebfb.png)

15. <span data-ttu-id="b4f98-521">Sélectionnez **le bouton** Ajouter en haut de Microsoft Defender - Protection avancée contre les **menaces et Antivirus Microsoft Defender**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-521">Select the **Add** button next to **Microsoft Defender Advanced Threat Protection and Microsoft Defender Antivirus**.</span></span>

    ![Image des paramètres de configuration ajoutés par MDATP et MDA](images/526b83fbdbb31265b3d0c1e5fbbdc33a.png)

16. <span data-ttu-id="b4f98-523">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-523">Select **Save**.</span></span>

    ![Image des paramètres de configurationssavimg](images/9d6e5386e652e00715ff348af72671c6.png)

17. <span data-ttu-id="b4f98-525">Sélectionnez **l’onglet** Étendue.</span><span class="sxs-lookup"><span data-stu-id="b4f98-525">Select the **Scope** tab.</span></span>

    ![Image de scptab des paramètres de configuration](images/8d80fe378a31143db9be0bacf7ddc5a3.png)

18. <span data-ttu-id="b4f98-527">Sélectionnez les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="b4f98-527">Select the target computers.</span></span>

    ![Image des paramètres de configuration tgtcomp](images/6eda18a64a660fa149575454e54e7156.png)

    <span data-ttu-id="b4f98-529">**Scope**</span><span class="sxs-lookup"><span data-stu-id="b4f98-529">**Scope**</span></span>

    <span data-ttu-id="b4f98-530">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-530">Select **Add**.</span></span>

    ![Image des paramètres de configuration ad1img](images/1c08d097829863778d562c10c5f92b67.png)

    ![Image des paramètres de configuration ad2img](images/216253cbfb6ae738b9f13496b9c799fd.png)

    <span data-ttu-id="b4f98-533">**Libre-service**</span><span class="sxs-lookup"><span data-stu-id="b4f98-533">**Self-Service**</span></span>

    ![Image du libre-service des paramètres de configuration](images/c9f85bba3e96d627fe00fc5a8363b83a.png)

19. <span data-ttu-id="b4f98-535">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="b4f98-535">Select **Done**.</span></span>

    ![Image des paramètres de configuration do1img](images/99679a7835b0d27d0a222bc3fdaf7f3b.png)

    ![Image des paramètres de configuration do2img](images/632aaab79ae18d0d2b8e0c16b6ba39e2.png)




