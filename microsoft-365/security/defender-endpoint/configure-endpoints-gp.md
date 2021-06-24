---
title: Intégrer Windows 10 appareils à Microsoft Defender pour le point de terminaison via la stratégie de groupe
description: Utilisez la stratégie de groupe pour déployer le package de configuration sur Windows 10 afin qu’ils soient intégrés au service.
keywords: configurer des appareils à l’aide de la stratégie de groupe, de la gestion des appareils, configurer Microsoft Defender pour les appareils endpoint, intégrer Microsoft Defender pour les appareils endpoint, stratégie de groupe
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.date: 04/24/2018
ms.technology: mde
ms.openlocfilehash: 80794a9d5e4da0d2da74fc714ffd1e0ceab34c8f
ms.sourcegitcommit: ccbdf2638fc6646bfb89450169953f4c3ce4b9b0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2021
ms.locfileid: "53105685"
---
# <a name="onboard-windows-10-devices-using-group-policy"></a><span data-ttu-id="01acc-104">Intégrer des Windows 10 à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="01acc-104">Onboard Windows 10 devices using Group Policy</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="01acc-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="01acc-105">**Applies to:**</span></span>

- <span data-ttu-id="01acc-106">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="01acc-106">Group Policy</span></span>
- [<span data-ttu-id="01acc-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="01acc-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="01acc-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="01acc-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="01acc-109">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="01acc-109">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="01acc-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="01acc-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-configureendpointsgp-abovefoldlink)


> [!NOTE]
> <span data-ttu-id="01acc-111">Pour utiliser les mises à jour de stratégie de groupe (GP) pour déployer le package, vous devez être sur Windows Server 2008 R2 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="01acc-111">To use Group Policy (GP) updates to deploy the package, you must be on Windows Server 2008 R2 or later.</span></span>
> 
> <span data-ttu-id="01acc-112">Pour Windows Server 2019, vous devrez peut-être remplacer NT AUTHORITY\Well-Known-System-Account par NT AUTHORITY\SYSTEM du fichier XML créé par la préférence de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="01acc-112">For Windows Server 2019, you may need to replace NT AUTHORITY\Well-Known-System-Account with NT AUTHORITY\SYSTEM of the XML file that the Group Policy preference creates.</span></span>

## <a name="onboard-devices-using-group-policy"></a><span data-ttu-id="01acc-113">Intégrer des appareils à l’aide d’une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="01acc-113">Onboard devices using Group Policy</span></span>

<span data-ttu-id="01acc-114">[![Image du PDF montrant les différents chemins de déploiement](images/onboard-gp.png)](images/onboard-gp.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="01acc-114">[![Image of the PDF showing the various deployment paths](images/onboard-gp.png)](images/onboard-gp.png#lightbox)</span></span>

<span data-ttu-id="01acc-115">Consultez le [fichier PDF](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf) [ou Visio](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.vsdx) pour voir les différents chemins d’accès dans le déploiement de Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="01acc-115">Check out the [PDF](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf)  or  [Visio](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.vsdx) to see the various paths in deploying Defender for Endpoint.</span></span> 



1. <span data-ttu-id="01acc-116">Ouvrez le fichier de package de configuration de .zip de groupe (*WindowsDefenderATPOnboardingPackage.zip*) que vous avez téléchargé à partir de l’Assistant d’intégration de service.</span><span class="sxs-lookup"><span data-stu-id="01acc-116">Open the GP configuration package .zip file (*WindowsDefenderATPOnboardingPackage.zip*) that you downloaded from the service onboarding wizard.</span></span> <span data-ttu-id="01acc-117">Vous pouvez également obtenir le package à partir [de Centre de sécurité Microsoft Defender](https://securitycenter.windows.com/):</span><span class="sxs-lookup"><span data-stu-id="01acc-117">You can also get the package from [Microsoft Defender Security Center](https://securitycenter.windows.com/):</span></span>
 
    1. <span data-ttu-id="01acc-118">Dans le volet de navigation, sélectionnez **Paramètres**  >  **intégration.**</span><span class="sxs-lookup"><span data-stu-id="01acc-118">In the navigation pane, select **Settings** > **Onboarding**.</span></span>

    1. <span data-ttu-id="01acc-119">Sélectionnez Windows 10 comme système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="01acc-119">Select Windows 10 as the operating system.</span></span>
    
    1. <span data-ttu-id="01acc-120">Dans le **champ Méthode de déploiement,** sélectionnez **Stratégie de groupe.**</span><span class="sxs-lookup"><span data-stu-id="01acc-120">In the **Deployment method** field, select **Group policy**.</span></span>
    
    1. <span data-ttu-id="01acc-121">Cliquez **sur Télécharger le package** et enregistrez .zip fichier.</span><span class="sxs-lookup"><span data-stu-id="01acc-121">Click **Download package** and save the .zip file.</span></span>

2. <span data-ttu-id="01acc-122">Extrayez le contenu du .zip vers un emplacement partagé en lecture seule accessible par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="01acc-122">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the device.</span></span> <span data-ttu-id="01acc-123">Vous devez avoir un dossier appelé *OptionalParamsPolicy* et le fichier *WindowsDefenderATPOnboardingScript.cmd*.</span><span class="sxs-lookup"><span data-stu-id="01acc-123">You should have a folder called *OptionalParamsPolicy* and the file *WindowsDefenderATPOnboardingScript.cmd*.</span></span>

3. <span data-ttu-id="01acc-124">Ouvrez [la Console](/internet-explorer/ie11-deploy-guide/group-policy-and-group-policy-mgmt-console-ie11) de gestion des stratégies de groupe (GPMC), cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="01acc-124">Open the [Group Policy Management Console](/internet-explorer/ie11-deploy-guide/group-policy-and-group-policy-mgmt-console-ie11) (GPMC), right-click the Group Policy Object (GPO) you want to configure and click **Edit**.</span></span>

4. <span data-ttu-id="01acc-125">Dans **l’Éditeur de gestion des stratégies** de groupe, allez à **Configuration** ordinateur, puis **Préférences,** puis **paramètres du panneau de configuration.**</span><span class="sxs-lookup"><span data-stu-id="01acc-125">In the **Group Policy Management Editor**, go to **Computer configuration**, then **Preferences**, and then **Control panel settings**.</span></span>

5. <span data-ttu-id="01acc-126">Cliquez avec le bouton droit **sur Tâches programmées,** pointez sur **Nouveau,** puis cliquez sur Tâche immédiate (au moins **Windows 7).**</span><span class="sxs-lookup"><span data-stu-id="01acc-126">Right-click **Scheduled tasks**, point to **New**, and then click **Immediate Task (At least Windows 7)**.</span></span>

6. <span data-ttu-id="01acc-127">Dans la **fenêtre** Tâche qui s’ouvre, allez dans **l’onglet** Général. Sous **Options de sécurité,** cliquez **sur Modifier l’utilisateur ou** le groupe, puis tapez SYSTEM, puis cliquez sur Vérifier les **noms,** **puis OK.**</span><span class="sxs-lookup"><span data-stu-id="01acc-127">In the **Task** window that opens, go to the **General** tab. Under **Security options** click **Change User or Group** and type SYSTEM and then click **Check Names** then **OK**.</span></span> <span data-ttu-id="01acc-128">NT AUTHORITY\SYSTEM apparaît en tant que compte d’utilisateur que la tâche exécutera.</span><span class="sxs-lookup"><span data-stu-id="01acc-128">NT AUTHORITY\SYSTEM appears as the user account the task will run as.</span></span>

7. <span data-ttu-id="01acc-129">Sélectionnez **Exécuter, que l’utilisateur soit** connecté ou non, puis cochez la case Exécuter avec les **privilèges les plus élevés.**</span><span class="sxs-lookup"><span data-stu-id="01acc-129">Select **Run whether user is logged on or not** and check the **Run with highest privileges** check box.</span></span>

8. <span data-ttu-id="01acc-130">Go to the **Actions** tab and click **New...** **Assurez-vous que démarrer un programme** est sélectionné dans le champ **Action.**</span><span class="sxs-lookup"><span data-stu-id="01acc-130">Go to the **Actions** tab and click **New...** Ensure that **Start a program** is selected in the **Action** field.</span></span> <span data-ttu-id="01acc-131">Entrez le nom de fichier et l’emplacement du fichier *WindowsDefenderATPOnboardingScript.cmd* partagé.</span><span class="sxs-lookup"><span data-stu-id="01acc-131">Enter the file name and location of the shared *WindowsDefenderATPOnboardingScript.cmd* file.</span></span>

9. <span data-ttu-id="01acc-132">Cliquez **sur OK** et fermez toutes les fenêtres GPMC ouvertes.</span><span class="sxs-lookup"><span data-stu-id="01acc-132">Click **OK** and close any open GPMC windows.</span></span>

>[!TIP]
> <span data-ttu-id="01acc-133">Après avoir intégré l’appareil, vous pouvez choisir d’exécuter un test de détection pour vérifier que l’appareil est correctement intégré au service.</span><span class="sxs-lookup"><span data-stu-id="01acc-133">After onboarding the device, you can choose to run a detection test to verify that the device is properly onboarded to the service.</span></span> <span data-ttu-id="01acc-134">Pour plus d’informations, voir Exécuter un test de détection sur un appareil [Defender for Endpoint nouvellement intégré.](run-detection-test.md)</span><span class="sxs-lookup"><span data-stu-id="01acc-134">For more information, see [Run a detection test on a newly onboarded Defender for Endpoint device](run-detection-test.md).</span></span>

## <a name="additional-defender-for-endpoint-configuration-settings"></a><span data-ttu-id="01acc-135">Paramètres de configuration defender supplémentaires pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="01acc-135">Additional Defender for Endpoint configuration settings</span></span>
<span data-ttu-id="01acc-136">Pour chaque appareil, vous pouvez déterminer si des échantillons peuvent être collectés à partir de l’appareil lorsqu’une demande est faite via Centre de sécurité Microsoft Defender pour soumettre un fichier pour analyse approfondie.</span><span class="sxs-lookup"><span data-stu-id="01acc-136">For each device, you can state whether samples can be collected from the device when a request is made through Microsoft Defender Security Center to submit a file for deep analysis.</span></span>

<span data-ttu-id="01acc-137">Vous pouvez utiliser la stratégie de groupe (GP) pour configurer des paramètres, tels que les paramètres de l’exemple de partage utilisé dans la fonctionnalité d’analyse approfondie.</span><span class="sxs-lookup"><span data-stu-id="01acc-137">You can use Group Policy (GP) to configure settings, such as settings for the sample sharing used in the deep analysis feature.</span></span>

### <a name="configure-sample-collection-settings"></a><span data-ttu-id="01acc-138">Configurer des paramètres de collection d’exemples</span><span class="sxs-lookup"><span data-stu-id="01acc-138">Configure sample collection settings</span></span>
1.  <span data-ttu-id="01acc-139">Sur votre appareil de gestion de la gp, copiez les fichiers suivants à partir du package de configuration :</span><span class="sxs-lookup"><span data-stu-id="01acc-139">On your GP management device, copy the following files from the configuration package:</span></span>

    - <span data-ttu-id="01acc-140">Copier _AtpConfiguration.admx_ dans _C : Windows \\ \\ PolicyDefinitions_</span><span class="sxs-lookup"><span data-stu-id="01acc-140">Copy _AtpConfiguration.admx_ into _C:\\Windows\\PolicyDefinitions_</span></span>

    - <span data-ttu-id="01acc-141">Copier _AtpConfiguration.adml_ dans _C : Windows \\ \\ PolicyDefinitions \\ en-US_</span><span class="sxs-lookup"><span data-stu-id="01acc-141">Copy _AtpConfiguration.adml_ into _C:\\Windows\\PolicyDefinitions\\en-US_</span></span>

    <span data-ttu-id="01acc-142">Si vous utilisez un magasin central pour les [modèles](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra)d’administration de stratégie de groupe, copiez les fichiers suivants à partir du package de configuration :</span><span class="sxs-lookup"><span data-stu-id="01acc-142">If you are using a [Central Store for Group Policy Administrative Templates](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra), copy the following files from the configuration package:</span></span>
    
    - <span data-ttu-id="01acc-143">Copier _AtpConfiguration.admx_ dans _\\ \\ \<forest.root\> \\ SysVol \\ \<forest.root\> \\ Policies \\ PolicyDefinitions_</span><span class="sxs-lookup"><span data-stu-id="01acc-143">Copy _AtpConfiguration.admx_ into _\\\\\<forest.root\>\\SysVol\\\<forest.root\>\\Policies\\PolicyDefinitions_</span></span>

    - <span data-ttu-id="01acc-144">Copier _AtpConfiguration.adml_ dans _\\ \\ \<forest.root\> \\ SysVol \\ \<forest.root\> \\ Policies \\ PolicyDefinitions \\ en-US_</span><span class="sxs-lookup"><span data-stu-id="01acc-144">Copy _AtpConfiguration.adml_ into _\\\\\<forest.root\>\\SysVol\\\<forest.root\>\\Policies\\PolicyDefinitions\\en-US_</span></span>

2.  <span data-ttu-id="01acc-145">Ouvrez la [Console de gestion des stratégies](/internet-explorer/ie11-deploy-guide/group-policy-and-group-policy-mgmt-console-ie11)de groupe, cliquez avec le bouton droit sur l’GPO que vous souhaitez configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="01acc-145">Open the [Group Policy Management Console](/internet-explorer/ie11-deploy-guide/group-policy-and-group-policy-mgmt-console-ie11), right-click the GPO you want to configure and click **Edit**.</span></span>

3.  <span data-ttu-id="01acc-146">Dans **l’Éditeur de gestion des stratégies de** groupe, allez à **Configuration de l’ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="01acc-146">In the **Group Policy Management Editor**, go to **Computer configuration**.</span></span>

4.  <span data-ttu-id="01acc-147">Cliquez **sur Stratégies,** **puis Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="01acc-147">Click **Policies**, then **Administrative templates**.</span></span>

5.  <span data-ttu-id="01acc-148">Cliquez **Windows composants,** **puis Windows Defender SmartScreen.**</span><span class="sxs-lookup"><span data-stu-id="01acc-148">Click **Windows components** and then **Windows Defender SmartScreen**.</span></span>

6.  <span data-ttu-id="01acc-149">Choisissez d’activer ou de désactiver le partage d’exemples à partir de vos appareils.</span><span class="sxs-lookup"><span data-stu-id="01acc-149">Choose to enable or disable sample sharing from your devices.</span></span>

>[!NOTE]
> <span data-ttu-id="01acc-150">Si vous ne définissez pas de valeur, la valeur par défaut consiste à activer la collection d’exemples.</span><span class="sxs-lookup"><span data-stu-id="01acc-150">If you don't set a value, the default value is to enable sample collection.</span></span>


## <a name="other-recommended-configuration-settings"></a><span data-ttu-id="01acc-151">Autres paramètres de configuration recommandés</span><span class="sxs-lookup"><span data-stu-id="01acc-151">Other recommended configuration settings</span></span>

### <a name="update-endpoint-protection-configuration"></a><span data-ttu-id="01acc-152">Mettre à jour la configuration de la protection des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="01acc-152">Update endpoint protection configuration</span></span>

<span data-ttu-id="01acc-153">Après avoir configuré le script d’intégration, continuez à modifier la même stratégie de groupe pour ajouter des configurations de protection des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="01acc-153">After configuring the onboarding script, continue editing the same group policy to add endpoint protection configurations.</span></span> <span data-ttu-id="01acc-154">Effectuez des modifications de stratégie de groupe à partir d’un système exécutant Windows 10 ou Server 2019 pour vous assurer que vous avez toutes les fonctionnalités Antivirus Microsoft Defender requises.</span><span class="sxs-lookup"><span data-stu-id="01acc-154">Perform group policy edits from a system running Windows 10 or Server 2019 to ensure you have all of the required Microsoft Defender Antivirus capabilities.</span></span> <span data-ttu-id="01acc-155">Vous devrez peut-être fermer et rouvrir l’objet de stratégie de groupe pour inscrire les paramètres de configuration de Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="01acc-155">You may need to close and reopen the group policy object to register the Defender ATP configuration settings.</span></span>

<span data-ttu-id="01acc-156">Toutes les stratégies se trouvent sous `Computer Configuration\Policies\Administrative Templates` .</span><span class="sxs-lookup"><span data-stu-id="01acc-156">All policies are located under `Computer Configuration\Policies\Administrative Templates`.</span></span>

<span data-ttu-id="01acc-157">**Emplacement de la stratégie** : \Windows\Windows Defender ATP</span><span class="sxs-lookup"><span data-stu-id="01acc-157">**Policy location:** \Windows Components\Windows Defender ATP</span></span>

<span data-ttu-id="01acc-158">Stratégie</span><span class="sxs-lookup"><span data-stu-id="01acc-158">Policy</span></span> | <span data-ttu-id="01acc-159">Paramètre</span><span class="sxs-lookup"><span data-stu-id="01acc-159">Setting</span></span> 
:---|:---
<span data-ttu-id="01acc-160">Enable\Disable Sample collection</span><span class="sxs-lookup"><span data-stu-id="01acc-160">Enable\Disable Sample collection</span></span>|   <span data-ttu-id="01acc-161">Activé : vérification « Activer la collecte d’exemples sur les ordinateurs »</span><span class="sxs-lookup"><span data-stu-id="01acc-161">Enabled - "Enable sample collection on machines" checked</span></span>

<br/>

<span data-ttu-id="01acc-162">**Emplacement de la stratégie** : \Windows\Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="01acc-162">**Policy location:**  \Windows Components\Microsoft Defender Antivirus</span></span>

<span data-ttu-id="01acc-163">Stratégie</span><span class="sxs-lookup"><span data-stu-id="01acc-163">Policy</span></span> | <span data-ttu-id="01acc-164">Paramètre</span><span class="sxs-lookup"><span data-stu-id="01acc-164">Setting</span></span> 
:---|:---
<span data-ttu-id="01acc-165">Configurer la détection pour les applications potentiellement indésirables</span><span class="sxs-lookup"><span data-stu-id="01acc-165">Configure detection for potentially unwanted applications</span></span> | <span data-ttu-id="01acc-166">Activé, Bloquer</span><span class="sxs-lookup"><span data-stu-id="01acc-166">Enabled, Block</span></span>

<br/>

<span data-ttu-id="01acc-167">**Emplacement de la stratégie** : \Windows\Antivirus Microsoft Defender\MAPS</span><span class="sxs-lookup"><span data-stu-id="01acc-167">**Policy location:** \Windows Components\Microsoft Defender Antivirus\MAPS</span></span>

<span data-ttu-id="01acc-168">Stratégie</span><span class="sxs-lookup"><span data-stu-id="01acc-168">Policy</span></span> | <span data-ttu-id="01acc-169">Paramètre</span><span class="sxs-lookup"><span data-stu-id="01acc-169">Setting</span></span> 
:---|:---
<span data-ttu-id="01acc-170">Rejoindre Microsoft MAPS</span><span class="sxs-lookup"><span data-stu-id="01acc-170">Join Microsoft MAPS</span></span> | <span data-ttu-id="01acc-171">Enabled, Advanced MAPS</span><span class="sxs-lookup"><span data-stu-id="01acc-171">Enabled, Advanced MAPS</span></span>
<span data-ttu-id="01acc-172">Envoyer des exemples de fichiers lorsque des analyses plus approfondies sont requises</span><span class="sxs-lookup"><span data-stu-id="01acc-172">Send file samples when further analysis is required</span></span> | <span data-ttu-id="01acc-173">Activé, Envoyer des exemples sûrs</span><span class="sxs-lookup"><span data-stu-id="01acc-173">Enabled, Send safe samples</span></span>

<br/>

<span data-ttu-id="01acc-174">**Emplacement de la stratégie** : \Windows\Antivirus Microsoft Defender\Protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="01acc-174">**Policy location:** \Windows Components\Microsoft Defender Antivirus\Real-time Protection</span></span>

<span data-ttu-id="01acc-175">Stratégie</span><span class="sxs-lookup"><span data-stu-id="01acc-175">Policy</span></span> | <span data-ttu-id="01acc-176">Paramètre</span><span class="sxs-lookup"><span data-stu-id="01acc-176">Setting</span></span> 
:---|:---
<span data-ttu-id="01acc-177">Désactiver la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="01acc-177">Turn off real-time protection</span></span>|<span data-ttu-id="01acc-178">Désactivé</span><span class="sxs-lookup"><span data-stu-id="01acc-178">Disabled</span></span>
<span data-ttu-id="01acc-179">Activer l’analyse du comportement</span><span class="sxs-lookup"><span data-stu-id="01acc-179">Turn on behavior monitoring</span></span>|<span data-ttu-id="01acc-180">Activé</span><span class="sxs-lookup"><span data-stu-id="01acc-180">Enabled</span></span>
<span data-ttu-id="01acc-181">Analyser tous les fichiers et pièces jointes téléchargés</span><span class="sxs-lookup"><span data-stu-id="01acc-181">Scan all downloaded files and attachments</span></span>|<span data-ttu-id="01acc-182">Activé</span><span class="sxs-lookup"><span data-stu-id="01acc-182">Enabled</span></span>
<span data-ttu-id="01acc-183">Surveiller l’activité des fichiers et des programmes sur votre ordinateur</span><span class="sxs-lookup"><span data-stu-id="01acc-183">Monitor file and program activity on your computer</span></span>|<span data-ttu-id="01acc-184">Activé</span><span class="sxs-lookup"><span data-stu-id="01acc-184">Enabled</span></span>

<br/>

<span data-ttu-id="01acc-185">**Emplacement de la stratégie** : \Windows\Antivirus Microsoft Defender\Scan</span><span class="sxs-lookup"><span data-stu-id="01acc-185">**Policy location:**  \Windows Components\Microsoft Defender Antivirus\Scan</span></span>

<span data-ttu-id="01acc-186">Ces paramètres configurent des analyses périodiques du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="01acc-186">These settings configure periodic scans of the endpoint.</span></span> <span data-ttu-id="01acc-187">Nous vous recommandons d’effectuer une analyse rapide hebdomadaire, autorisant les performances.</span><span class="sxs-lookup"><span data-stu-id="01acc-187">We recommend performing a weekly quick scan, performance permitting.</span></span>

<span data-ttu-id="01acc-188">Stratégie</span><span class="sxs-lookup"><span data-stu-id="01acc-188">Policy</span></span> | <span data-ttu-id="01acc-189">Paramètre</span><span class="sxs-lookup"><span data-stu-id="01acc-189">Setting</span></span> 
:---|:---
<span data-ttu-id="01acc-190">Recherchez les dernières informations sur la sécurité des virus et logiciels espions avant d’exécution d’une analyse programmée</span><span class="sxs-lookup"><span data-stu-id="01acc-190">Check for the latest virus and spyware security intelligence before running a scheduled scan</span></span> |<span data-ttu-id="01acc-191">Activé</span><span class="sxs-lookup"><span data-stu-id="01acc-191">Enabled</span></span>


<br/>

<span data-ttu-id="01acc-192">**Emplacement de la stratégie** : \Windows\Antivirus Microsoft Defender\Protection contre les attaques Microsoft Defender\Réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="01acc-192">**Policy location:** \Windows Components\Microsoft Defender Antivirus\Microsoft Defender Exploit Guard\Attack Surface Reduction</span></span>

<span data-ttu-id="01acc-193">Obtenir la liste actuelle des GUID de réduction de la surface d’attaque à partir des règles de personnalisation de la [réduction de la surface d’attaque](customize-attack-surface-reduction.md)</span><span class="sxs-lookup"><span data-stu-id="01acc-193">Get the current list of attack surface reduction GUIDs from [Customize attack surface reduction rules](customize-attack-surface-reduction.md)</span></span>

1. <span data-ttu-id="01acc-194">Ouvrez la **stratégie Configurer la Réduction de la surface d’attaque.**</span><span class="sxs-lookup"><span data-stu-id="01acc-194">Open the **Configure Attack Surface Reduction** policy.</span></span>

1. <span data-ttu-id="01acc-195">Sélectionnez **Activé**.</span><span class="sxs-lookup"><span data-stu-id="01acc-195">Select **Enabled**.</span></span>

1. <span data-ttu-id="01acc-196">Sélectionnez le **bouton** Afficher.</span><span class="sxs-lookup"><span data-stu-id="01acc-196">Select the **Show** button.</span></span>

1. <span data-ttu-id="01acc-197">Ajoutez chaque GUID dans le **champ Nom de** la valeur avec la valeur 2.</span><span class="sxs-lookup"><span data-stu-id="01acc-197">Add each GUID in the **Value Name** field with a Value of 2.</span></span>

   <span data-ttu-id="01acc-198">Chacun d’eux est alors uniquement mis en place pour l’audit.</span><span class="sxs-lookup"><span data-stu-id="01acc-198">This will set each up for audit only.</span></span>

   ![Image de la configuration de réduction de la surface d’attaque](images/asr-guid.png)



<span data-ttu-id="01acc-200">Stratégie</span><span class="sxs-lookup"><span data-stu-id="01acc-200">Policy</span></span> | <span data-ttu-id="01acc-201">Paramètre</span><span class="sxs-lookup"><span data-stu-id="01acc-201">Setting</span></span> 
:---|:---
<span data-ttu-id="01acc-202">Configurer l’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="01acc-202">Configure Controlled folder access</span></span>| <span data-ttu-id="01acc-203">Activé, mode Audit</span><span class="sxs-lookup"><span data-stu-id="01acc-203">Enabled, Audit Mode</span></span>



## <a name="offboard-devices-using-group-policy"></a><span data-ttu-id="01acc-204">Appareils de tableau de bord à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="01acc-204">Offboard devices using Group Policy</span></span>
<span data-ttu-id="01acc-205">Pour des raisons de sécurité, le package utilisé pour la sortie des appareils expirera 30 jours après la date de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="01acc-205">For security reasons, the package used to Offboard devices will expire 30 days after the date it was downloaded.</span></span> <span data-ttu-id="01acc-206">Les packages deboarding expirés envoyés à un appareil seront rejetés.</span><span class="sxs-lookup"><span data-stu-id="01acc-206">Expired offboarding packages sent to a device will be rejected.</span></span> <span data-ttu-id="01acc-207">Lorsque vous téléchargez un package de déclassage, vous êtes informé de la date d’expiration des packages et il est également inclus dans le nom du package.</span><span class="sxs-lookup"><span data-stu-id="01acc-207">When downloading an offboarding package you will be notified of the packages expiry date and it will also be included in the package name.</span></span>

> [!NOTE]
> <span data-ttu-id="01acc-208">Les stratégies d’intégration et deboarding ne doivent pas être déployées sur le même appareil en même temps, sinon cela provoquera des collisions imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="01acc-208">Onboarding and offboarding policies must not be deployed on the same device at the same time, otherwise this will cause unpredictable collisions.</span></span>

1. <span data-ttu-id="01acc-209">Obtenez le package deboarding à partir [de Centre de sécurité Microsoft Defender](https://securitycenter.windows.com/):</span><span class="sxs-lookup"><span data-stu-id="01acc-209">Get the offboarding package from [Microsoft Defender Security Center](https://securitycenter.windows.com/):</span></span>

    1. <span data-ttu-id="01acc-210">Dans le volet de navigation, sélectionnez **Paramètres**  >  **de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="01acc-210">In the navigation pane, select **Settings** > **Offboarding**.</span></span>

    1. <span data-ttu-id="01acc-211">Sélectionnez Windows 10 comme système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="01acc-211">Select Windows 10 as the operating system.</span></span>
    
    1. <span data-ttu-id="01acc-212">Dans le **champ Méthode de déploiement,** sélectionnez **Stratégie de groupe.**</span><span class="sxs-lookup"><span data-stu-id="01acc-212">In the **Deployment method** field, select **Group policy**.</span></span>

    1. <span data-ttu-id="01acc-213">Cliquez **sur Télécharger le package** et enregistrez .zip fichier.</span><span class="sxs-lookup"><span data-stu-id="01acc-213">Click **Download package** and save the .zip file.</span></span>

2. <span data-ttu-id="01acc-214">Extrayez le contenu du .zip vers un emplacement partagé en lecture seule accessible par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="01acc-214">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the device.</span></span> <span data-ttu-id="01acc-215">Vous devez avoir un fichier nommé *WindowsDefenderATPOffboardingScript_valid_until_YYYY-MM-DD.cmd*.</span><span class="sxs-lookup"><span data-stu-id="01acc-215">You should have a file named *WindowsDefenderATPOffboardingScript_valid_until_YYYY-MM-DD.cmd*.</span></span>

3. <span data-ttu-id="01acc-216">Ouvrez [la Console](/internet-explorer/ie11-deploy-guide/group-policy-and-group-policy-mgmt-console-ie11) de gestion des stratégies de groupe (GPMC), cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="01acc-216">Open the [Group Policy Management Console](/internet-explorer/ie11-deploy-guide/group-policy-and-group-policy-mgmt-console-ie11) (GPMC), right-click the Group Policy Object (GPO) you want to configure and click **Edit**.</span></span>

4. <span data-ttu-id="01acc-217">Dans **l’Éditeur de gestion des stratégies** de groupe, allez à **Configuration ordinateur,** puis **Préférences,** puis **paramètres du panneau de configuration.**</span><span class="sxs-lookup"><span data-stu-id="01acc-217">In the **Group Policy Management Editor**, go to **Computer configuration,** then **Preferences**, and then **Control panel settings**.</span></span>

5. <span data-ttu-id="01acc-218">Cliquez avec le bouton droit **sur Tâches programmées,** pointez sur **Nouveau,** puis cliquez sur **Tâche immédiate.**</span><span class="sxs-lookup"><span data-stu-id="01acc-218">Right-click **Scheduled tasks**, point to **New**, and then click **Immediate task**.</span></span>

6. <span data-ttu-id="01acc-219">Dans la **fenêtre** Tâche qui s’ouvre, allez dans **l’onglet** Général. Choisissez le compte d’utilisateur SYSTÈME local (BUILTIN\SYSTEM) sous **Options de sécurité.**</span><span class="sxs-lookup"><span data-stu-id="01acc-219">In the **Task** window that opens, go to the **General** tab. Choose the local SYSTEM user account (BUILTIN\SYSTEM) under **Security options**.</span></span>

7. <span data-ttu-id="01acc-220">Sélectionnez **Exécuter, que l’utilisateur soit** connecté ou non et cochez la case Exécuter avec les privilèges les plus **élevés.**</span><span class="sxs-lookup"><span data-stu-id="01acc-220">Select **Run whether user is logged on or not** and check the **Run with highest privileges** check-box.</span></span>

8. <span data-ttu-id="01acc-221">Go to the **Actions** tab and click **New...**. **Assurez-vous que démarrer un programme** est sélectionné dans le champ **Action.**</span><span class="sxs-lookup"><span data-stu-id="01acc-221">Go to the **Actions** tab and click **New...**. Ensure that **Start a program** is selected in the **Action** field.</span></span> <span data-ttu-id="01acc-222">Entrez le nom de fichier et l’emplacement du fichier *WindowsDefenderATPOffboardingScript_valid_until_YYYY-MM-DD.cmd.*</span><span class="sxs-lookup"><span data-stu-id="01acc-222">Enter the file name and location of the shared  *WindowsDefenderATPOffboardingScript_valid_until_YYYY-MM-DD.cmd* file.</span></span>

9. <span data-ttu-id="01acc-223">Cliquez **sur OK** et fermez toutes les fenêtres GPMC ouvertes.</span><span class="sxs-lookup"><span data-stu-id="01acc-223">Click **OK** and close any open GPMC windows.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01acc-224">Laboarding empêche l’appareil d’envoyer des données de capteur au portail, mais les données de l’appareil, y compris la référence aux alertes qu’il a eues, seront conservées pendant 6 mois.</span><span class="sxs-lookup"><span data-stu-id="01acc-224">Offboarding causes the device to stop sending sensor data to the portal but data from the device, including reference to any alerts it has had will be retained for up to 6 months.</span></span>


## <a name="monitor-device-configuration"></a><span data-ttu-id="01acc-225">Surveiller la configuration de l’appareil</span><span class="sxs-lookup"><span data-stu-id="01acc-225">Monitor device configuration</span></span>
<span data-ttu-id="01acc-226">Avec la stratégie de groupe, il n’est pas possible de surveiller le déploiement des stratégies sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="01acc-226">With Group Policy there isn’t an option to monitor deployment of policies on the devices.</span></span> <span data-ttu-id="01acc-227">La surveillance peut être effectuée directement sur le portail ou à l’aide des différents outils de déploiement.</span><span class="sxs-lookup"><span data-stu-id="01acc-227">Monitoring can be done directly on the portal, or by using the different deployment tools.</span></span>

## <a name="monitor-devices-using-the-portal"></a><span data-ttu-id="01acc-228">Surveiller les appareils à l’aide du portail</span><span class="sxs-lookup"><span data-stu-id="01acc-228">Monitor devices using the portal</span></span>
1. <span data-ttu-id="01acc-229">Go to [Centre de sécurité Microsoft Defender](https://securitycenter.windows.com/).</span><span class="sxs-lookup"><span data-stu-id="01acc-229">Go to [Microsoft Defender Security Center](https://securitycenter.windows.com/).</span></span>
2. <span data-ttu-id="01acc-230">Cliquez **sur Liste des appareils.**</span><span class="sxs-lookup"><span data-stu-id="01acc-230">Click **Devices list**.</span></span>
3. <span data-ttu-id="01acc-231">Vérifiez que les appareils apparaissent.</span><span class="sxs-lookup"><span data-stu-id="01acc-231">Verify that devices are appearing.</span></span>

> [!NOTE]
> <span data-ttu-id="01acc-232">L’affichage des appareils dans la liste Appareils peut prendre plusieurs **jours.**</span><span class="sxs-lookup"><span data-stu-id="01acc-232">It can take several days for devices to start showing on the **Devices list**.</span></span> <span data-ttu-id="01acc-233">Cela inclut le temps qu’il faut pour que les stratégies soient distribuées à l’appareil, le temps qu’il faut avant que l’utilisateur se connecte et le temps qu’il faut au point de terminaison pour commencer à créer des rapports.</span><span class="sxs-lookup"><span data-stu-id="01acc-233">This includes the time it takes for the policies to be distributed to the device, the time it takes before the user logs on, and the time it takes for the endpoint to start reporting.</span></span>


## <a name="related-topics"></a><span data-ttu-id="01acc-234">Sujets connexes</span><span class="sxs-lookup"><span data-stu-id="01acc-234">Related topics</span></span>
- [<span data-ttu-id="01acc-235">Intégrer Windows 10 appareils à l’aide Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="01acc-235">Onboard Windows 10 devices using Microsoft Endpoint Configuration Manager</span></span>](configure-endpoints-sccm.md)
- [<span data-ttu-id="01acc-236">Intégrer les appareils Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="01acc-236">Onboard Windows 10 devices using Mobile Device Management tools</span></span>](configure-endpoints-mdm.md)
- [<span data-ttu-id="01acc-237">Intégrer les appareils Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="01acc-237">Onboard Windows 10 devices using a local script</span></span>](configure-endpoints-script.md)
- [<span data-ttu-id="01acc-238">Intégrer les ordinateurs virtuels d’infrastructure de bureau (VDI) non persistants</span><span class="sxs-lookup"><span data-stu-id="01acc-238">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>](configure-endpoints-vdi.md)
- [<span data-ttu-id="01acc-239">Exécuter un test de détection sur un microsoft Defender pour les appareils de point de terminaison nouvellement intégré</span><span class="sxs-lookup"><span data-stu-id="01acc-239">Run a detection test on a newly onboarded Microsoft Defender for Endpoint devices</span></span>](run-detection-test.md)
- [<span data-ttu-id="01acc-240">Résoudre les problèmes d’intégration de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="01acc-240">Troubleshoot Microsoft Defender for Endpoint onboarding issues</span></span>](troubleshoot-onboarding.md)
