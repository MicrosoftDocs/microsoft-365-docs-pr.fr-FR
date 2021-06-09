---
title: Activer l’accès contrôlé aux dossiers
keywords: Accès contrôlé aux dossiers, windows 10, windows defender, ransomware, protéger, fichiers, dossiers, activer, utiliser
description: Découvrez comment protéger vos fichiers importants en activant l’accès contrôlé aux dossiers
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
audience: ITPro
author: dansimp
ms.author: dansimp
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 1d09eaf04999478a0cd0b4907667a522a23fb39f
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52841977"
---
# <a name="enable-controlled-folder-access"></a><span data-ttu-id="6ac6b-104">Activer l’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="6ac6b-104">Enable controlled folder access</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="6ac6b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6ac6b-105">**Applies to:**</span></span>
- [<span data-ttu-id="6ac6b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6ac6b-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="6ac6b-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6ac6b-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="6ac6b-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="6ac6b-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="6ac6b-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="6ac6b-110">[L’accès contrôlé aux dossiers](controlled-folders.md) vous permet de protéger les données précieuses contre les applications malveillantes et les menaces, telles que les ransomware.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-110">[Controlled folder access](controlled-folders.md) helps you protect valuable data from malicious apps and threats, such as ransomware.</span></span> <span data-ttu-id="6ac6b-111">L’accès contrôlé aux dossiers est inclus Windows 10 et Windows Server 2019.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-111">Controlled folder access is included with Windows 10 and Windows Server 2019.</span></span>

<span data-ttu-id="6ac6b-112">Vous pouvez activer l’accès contrôlé aux dossiers à l’aide de l’une des méthodes ci-après :</span><span class="sxs-lookup"><span data-stu-id="6ac6b-112">You can enable controlled folder access by using any of these methods:</span></span>

* [<span data-ttu-id="6ac6b-113">Sécurité Windows application</span><span class="sxs-lookup"><span data-stu-id="6ac6b-113">Windows Security app</span></span>](#windows-security-app)
* [<span data-ttu-id="6ac6b-114">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="6ac6b-114">Microsoft Intune</span></span>](#intune)
* [<span data-ttu-id="6ac6b-115">Gestion des périphériques mobiles (MDM)</span><span class="sxs-lookup"><span data-stu-id="6ac6b-115">Mobile Device Management (MDM)</span></span>](#mobile-device-management-mdm)
* [<span data-ttu-id="6ac6b-116">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6ac6b-116">Microsoft Endpoint Configuration Manager</span></span>](#microsoft-endpoint-configuration-manager)
* [<span data-ttu-id="6ac6b-117">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="6ac6b-117">Group Policy</span></span>](#group-policy)
* [<span data-ttu-id="6ac6b-118">PowerShell</span><span class="sxs-lookup"><span data-stu-id="6ac6b-118">PowerShell</span></span>](#powershell)

<span data-ttu-id="6ac6b-119">[Le mode audit](evaluate-controlled-folder-access.md) vous permet de tester le fonctionnement de la fonctionnalité (et de passer en revue les événements) sans impact sur l’utilisation normale de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-119">[Audit mode](evaluate-controlled-folder-access.md) allows you to test how the feature would work (and review events) without impacting the normal use of the device.</span></span>

<span data-ttu-id="6ac6b-120">Les paramètres de stratégie de groupe qui désactivent la fusion de listes d’administrateurs locaux remplacent les paramètres d’accès contrôlé aux dossiers.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-120">Group Policy settings that disable local administrator list merging will override controlled folder access settings.</span></span> <span data-ttu-id="6ac6b-121">Ils remplacent également les dossiers protégés et les applications autorisées définies par l’administrateur local par le biais d’un accès contrôlé aux dossiers.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-121">They also override protected folders and allowed apps set by the local administrator through controlled folder access.</span></span> <span data-ttu-id="6ac6b-122">Ces stratégies sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6ac6b-122">These policies include:</span></span>

* <span data-ttu-id="6ac6b-123">Antivirus Microsoft Defender configurer **le comportement de fusion de l’administrateur local pour les listes**</span><span class="sxs-lookup"><span data-stu-id="6ac6b-123">Microsoft Defender Antivirus **Configure local administrator merge behavior for lists**</span></span>
* <span data-ttu-id="6ac6b-124">System Center Endpoint Protection autoriser **les utilisateurs à ajouter des exclusions et des remplacements**</span><span class="sxs-lookup"><span data-stu-id="6ac6b-124">System Center Endpoint Protection **Allow users to add exclusions and overrides**</span></span>

<span data-ttu-id="6ac6b-125">Pour plus d’informations sur la désactivation de la fusion de listes locales, voir Empêcher ou autoriser les utilisateurs à modifier localement les paramètres de stratégie de [Microsoft Defender AV.](/windows/security/threat-protection/microsoft-defender-antivirus/configure-local-policy-overrides-microsoft-defender-antivirus#configure-how-locally-and-globally-defined-threat-remediation-and-exclusions-lists-are-merged)</span><span class="sxs-lookup"><span data-stu-id="6ac6b-125">For more information about disabling local list merging, see [Prevent or allow users to locally modify Microsoft Defender AV policy settings](/windows/security/threat-protection/microsoft-defender-antivirus/configure-local-policy-overrides-microsoft-defender-antivirus#configure-how-locally-and-globally-defined-threat-remediation-and-exclusions-lists-are-merged).</span></span>

## <a name="windows-security-app"></a><span data-ttu-id="6ac6b-126">Sécurité Windows application</span><span class="sxs-lookup"><span data-stu-id="6ac6b-126">Windows Security app</span></span>

1. <span data-ttu-id="6ac6b-127">Ouvrez l Sécurité Windows en sélectionnant l’icône de bouclier dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-127">Open the Windows Security app by selecting the shield icon in the task bar.</span></span> <span data-ttu-id="6ac6b-128">Vous pouvez également rechercher Defender dans le menu **Démarrer.**</span><span class="sxs-lookup"><span data-stu-id="6ac6b-128">You can also search the start menu for **Defender**.</span></span>

2. <span data-ttu-id="6ac6b-129">Sélectionnez la **vignette & protection** contre les virus contre les menaces (ou l’icône de bouclier dans la barre de menus de gauche), puis sélectionnez Protection contre les **ransomware.**</span><span class="sxs-lookup"><span data-stu-id="6ac6b-129">Select the **Virus & threat protection** tile (or the shield icon on the left menu bar) and then select **Ransomware protection**.</span></span>

3. <span data-ttu-id="6ac6b-130">Définissez le commutateur pour **l’accès contrôlé aux** dossiers sur **On**.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-130">Set the switch for **Controlled folder access** to **On**.</span></span>

> [!NOTE]
> <span data-ttu-id="6ac6b-131">Si l’accès contrôlé aux dossiers est configuré avec la stratégie de groupe, PowerShell ou les CSP MDM, l’état change dans l’application Sécurité Windows après un redémarrage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-131">If controlled folder access is configured with Group Policy, PowerShell, or MDM CSPs, the state will change in the Windows Security app after a restart of the device.</span></span>
> <span data-ttu-id="6ac6b-132">Si la fonctionnalité est définie sur **le mode Audit** avec l’un de ces outils, l’application Sécurité Windows affiche l’état comme Étant **éteint.**</span><span class="sxs-lookup"><span data-stu-id="6ac6b-132">If the feature is set to **Audit mode** with any of those tools, the Windows Security app will show the state as **Off**.</span></span>
> <span data-ttu-id="6ac6b-133">Si vous protégez les données de profil utilisateur, nous vous recommandons de le faire sur le lecteur d’installation Windows par défaut.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-133">If you are protecting user profile data, we recommend that the user profile should be on the default Windows installation drive.</span></span>

## <a name="intune"></a><span data-ttu-id="6ac6b-134">Intune</span><span class="sxs-lookup"><span data-stu-id="6ac6b-134">Intune</span></span>

1. <span data-ttu-id="6ac6b-135">Connectez-vous au [portail Azure et](https://portal.azure.com) ouvrez Intune.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-135">Sign in to the [Azure portal](https://portal.azure.com) and open Intune.</span></span>

2. <span data-ttu-id="6ac6b-136">Go to **Device configuration**  >  **Profiles**  >  **Create profile**.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-136">Go to **Device configuration** > **Profiles** > **Create profile**.</span></span>

3. <span data-ttu-id="6ac6b-137">Nommez le profil, choisissez **Windows 10 et ultérieures** et **Endpoint Protection**.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-137">Name the profile, choose **Windows 10 and later** and **Endpoint protection**.</span></span> <br/> <span data-ttu-id="6ac6b-138">![Créer un profil de protection des points de terminaison](/microsoft-365/security/defender-endpoint/images/create-endpoint-protection-profile)</span><span class="sxs-lookup"><span data-stu-id="6ac6b-138">![Create endpoint protection profile](/microsoft-365/security/defender-endpoint/images/create-endpoint-protection-profile)</span></span> <br/>

4. <span data-ttu-id="6ac6b-139">Go to **Configure**  >  **Windows Defender Exploit Guard**  >  **Controlled folder access**  >  **Enable**.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-139">Go to **Configure** > **Windows Defender Exploit Guard** > **Controlled folder access** > **Enable**.</span></span>

5. <span data-ttu-id="6ac6b-140">Tapez le chemin d’accès à chaque application qui a accès aux dossiers protégés et le chemin d’accès à tout dossier supplémentaire qui nécessite une protection.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-140">Type the path to each application that has access to protected folders and the path to any additional folder that needs protection.</span></span> <span data-ttu-id="6ac6b-141">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-141">Select **Add**.</span></span><br/> <span data-ttu-id="6ac6b-142">![Activer l’accès contrôlé aux dossiers dans Intune](/microsoft-365/security/defender-endpoint/images/enable-cfa-intune)</span><span class="sxs-lookup"><span data-stu-id="6ac6b-142">![Enable controlled folder access in Intune](/microsoft-365/security/defender-endpoint/images/enable-cfa-intune)</span></span><br/>

   > [!NOTE]
   > <span data-ttu-id="6ac6b-143">Wilcard est pris en charge pour les applications, mais pas pour les dossiers.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-143">Wilcard is supported for applications, but not for folders.</span></span> <span data-ttu-id="6ac6b-144">Les sous-foldeurs ne sont pas protégés.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-144">Subfolders are not protected.</span></span> <span data-ttu-id="6ac6b-145">Les applications autorisées continueront à déclencher des événements jusqu’à leur redémarrage.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-145">Allowed apps will continue to trigger events until they are restarted.</span></span>

6. <span data-ttu-id="6ac6b-146">Sélectionnez **OK** pour enregistrer chaque lame ouvert et **créer.**</span><span class="sxs-lookup"><span data-stu-id="6ac6b-146">Select **OK** to save each open blade and **Create**.</span></span>

7. <span data-ttu-id="6ac6b-147">Sélectionnez les **affectations de profil,** affectez à tous les utilisateurs **& tous** les appareils et **enregistrez**.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-147">Select the profile **Assignments**, assign to **All Users & All Devices**, and **Save**.</span></span>

## <a name="mobile-device-management-mdm"></a><span data-ttu-id="6ac6b-148">Gestion des périphériques mobiles (MDM)</span><span class="sxs-lookup"><span data-stu-id="6ac6b-148">Mobile Device Management (MDM)</span></span>

<span data-ttu-id="6ac6b-149">Utilisez le fournisseur de services de configuration [./Vendor/MSFT/Policy/Config/ControlledFolderAccessProtectedFolders](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders) (CSP) pour permettre aux applications d’apporter des modifications aux dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-149">Use the [./Vendor/MSFT/Policy/Config/ControlledFolderAccessProtectedFolders](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders) configuration service provider (CSP) to allow apps to make changes to protected folders.</span></span>

## <a name="microsoft-endpoint-configuration-manager"></a><span data-ttu-id="6ac6b-150">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6ac6b-150">Microsoft Endpoint Configuration Manager</span></span>

1. <span data-ttu-id="6ac6b-151">In Microsoft Endpoint Configuration Manager, go to **Assets and Compliance**  >  **Endpoint Protection** Windows Defender  >  **Exploit Guard**.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-151">In Microsoft Endpoint Configuration Manager, go to **Assets and Compliance** > **Endpoint Protection** > **Windows Defender Exploit Guard**.</span></span>

2. <span data-ttu-id="6ac6b-152">Sélectionnez **Home**  >  **Create Exploit Guard Policy**.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-152">Select **Home** > **Create Exploit Guard Policy**.</span></span>

3. <span data-ttu-id="6ac6b-153">Entrez un nom et une description, sélectionnez **Accès contrôlé aux** dossiers, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-153">Enter a name and a description, select **Controlled folder access**, and select **Next**.</span></span>

4. <span data-ttu-id="6ac6b-154">Choisissez si bloquer ou auditer les modifications, autoriser d’autres applications ou ajouter d’autres dossiers, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-154">Choose whether block or audit changes, allow other apps, or add other folders, and select **Next**.</span></span>
   > [!NOTE]
   > <span data-ttu-id="6ac6b-155">Wilcard est pris en charge pour les applications, mais pas pour les dossiers.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-155">Wilcard is supported for applications, but not for folders.</span></span> <span data-ttu-id="6ac6b-156">Les sous-foldeurs ne sont pas protégés.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-156">Subfolders are not protected.</span></span> <span data-ttu-id="6ac6b-157">Les applications autorisées continueront à déclencher des événements jusqu’à leur redémarrage.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-157">Allowed apps will continue to trigger events until they are restarted.</span></span>

5. <span data-ttu-id="6ac6b-158">Examinez les paramètres et sélectionnez **Suivant** pour créer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-158">Review the settings and select **Next** to create the policy.</span></span>

6. <span data-ttu-id="6ac6b-159">Une fois la stratégie créée, **fermez**.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-159">After the policy is created, **Close**.</span></span>

## <a name="group-policy"></a><span data-ttu-id="6ac6b-160">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="6ac6b-160">Group Policy</span></span>

1. <span data-ttu-id="6ac6b-161">Sur votre appareil de gestion des stratégies de groupe, ouvrez la [Console](https://technet.microsoft.com/library/cc731212.aspx)de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous souhaitez configurer et sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="6ac6b-161">On your Group Policy management device, open the [Group Policy Management Console](https://technet.microsoft.com/library/cc731212.aspx), right-click the Group Policy Object you want to configure and select **Edit**.</span></span>

2. <span data-ttu-id="6ac6b-162">Dans l’**Éditeur de gestion des stratégies de groupe**, accédez à **Configuration ordinateur**, puis sélectionnez **Modèles d’administration**.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-162">In the **Group Policy Management Editor**, go to **Computer configuration** and select **Administrative templates**.</span></span>

3. <span data-ttu-id="6ac6b-163">Développez l’arborescence **Windows composants > Antivirus Microsoft Defender > Windows Defender Exploit Guard > accès contrôlé aux dossiers.**</span><span class="sxs-lookup"><span data-stu-id="6ac6b-163">Expand the tree to **Windows components > Microsoft Defender Antivirus > Windows Defender Exploit Guard > Controlled folder access**.</span></span>

4. <span data-ttu-id="6ac6b-164">Double-cliquez sur **le paramètre Configurer l’accès contrôlé aux** dossiers et définissez l’option sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="6ac6b-164">Double-click the **Configure Controlled folder access** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="6ac6b-165">Dans la section Options, vous devez spécifier l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="6ac6b-165">In the options section you must specify one of the following options:</span></span>
    * <span data-ttu-id="6ac6b-166">**Activer** : les applications malveillantes et suspectes ne seront pas autorisées à apporter des modifications aux fichiers des dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-166">**Enable** - Malicious and suspicious apps won't be allowed to make changes to files in protected folders.</span></span> <span data-ttu-id="6ac6b-167">Une notification sera fournie dans le journal Windows événements.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-167">A notification will be provided in the Windows event log.</span></span>
    * <span data-ttu-id="6ac6b-168">**Désactiver (par défaut)** : la fonctionnalité Accès contrôlé aux dossiers ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-168">**Disable (Default)** - The Controlled folder access feature won't work.</span></span> <span data-ttu-id="6ac6b-169">Toutes les applications peuvent apporter des modifications aux fichiers des dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-169">All apps can make changes to files in protected folders.</span></span>
    * <span data-ttu-id="6ac6b-170">**Mode audit** : les modifications sont autorisées si une application malveillante ou suspecte tente d’apporter une modification à un fichier dans un dossier protégé.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-170">**Audit Mode** - Changes will be allowed if a malicious or suspicious app attempts to make a change to a file in a protected folder.</span></span> <span data-ttu-id="6ac6b-171">Toutefois, il sera enregistré dans le journal Windows événements dans lequel vous pourrez évaluer l’impact sur votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-171">However, it will be recorded in the Windows event log where you can assess the impact on your organization.</span></span>
    * <span data-ttu-id="6ac6b-172">**Bloquer la modification du disque** uniquement : les tentatives d’écriture d’applications nontrues dans les secteurs de disque sont enregistrées dans Windows journal des événements.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-172">**Block disk modification only** - Attempts by untrusted apps to write to disk sectors will be logged in Windows Event log.</span></span> <span data-ttu-id="6ac6b-173">Ces journaux se trouvent dans **les journaux des applications** et des services > Microsoft > Windows > Windows Defender > Operational > ID 1123.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-173">These logs can be found in **Applications and Services Logs** > Microsoft > Windows > Windows Defender > Operational > ID 1123.</span></span>
    * <span data-ttu-id="6ac6b-174">**Auditer** la modification du disque uniquement : seules les tentatives d’écriture dans les secteurs de disque protégés seront **enregistrées** dans le journal des événements Windows (sous Journaux des applications et des services  >  **Microsoft**  >  **Windows**  >  **Windows Defender**  >  **Operational**  >  **ID 1124**).</span><span class="sxs-lookup"><span data-stu-id="6ac6b-174">**Audit disk modification only** - Only attempts to write to protected disk sectors will be recorded in the Windows event log (under **Applications and Services Logs** > **Microsoft** > **Windows** > **Windows Defender** > **Operational** > **ID 1124**).</span></span> <span data-ttu-id="6ac6b-175">Les tentatives de modification ou de suppression de fichiers dans des dossiers protégés ne sont pas enregistrées.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-175">Attempts to modify or delete files in protected folders won't be recorded.</span></span>

      ![Capture d’écran de l’option de stratégie de groupe Activée et mode Audit sélectionnée dans la baisse](/microsoft-365/security/defender-endpoint/images/cfa-gp-enable)

> [!IMPORTANT]
> <span data-ttu-id="6ac6b-177">Pour activer entièrement l’accès contrôlé aux dossiers, vous  devez définir l’option de stratégie de groupe sur Activé et sélectionner Bloquer dans le menu déroulant Options. </span><span class="sxs-lookup"><span data-stu-id="6ac6b-177">To fully enable controlled folder access, you must set the Group Policy option to **Enabled** and select **Block** in the options drop-down menu.</span></span>

## <a name="powershell"></a><span data-ttu-id="6ac6b-178">PowerShell</span><span class="sxs-lookup"><span data-stu-id="6ac6b-178">PowerShell</span></span>

1. <span data-ttu-id="6ac6b-179">Tapez **powershell** dans le menu Démarrer, cliquez avec **le bouton droit sur Windows PowerShell** puis **sélectionnez Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="6ac6b-179">Type **powershell** in the Start menu, right-click **Windows PowerShell** and select **Run as administrator**.</span></span>

2. <span data-ttu-id="6ac6b-180">Entrez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="6ac6b-180">Enter the following cmdlet:</span></span>

    ```PowerShell
    Set-MpPreference -EnableControlledFolderAccess Enabled
    ```

<span data-ttu-id="6ac6b-181">Vous pouvez activer la fonctionnalité en mode audit en spécifiant `AuditMode` au lieu de `Enabled` .</span><span class="sxs-lookup"><span data-stu-id="6ac6b-181">You can enable the feature in audit mode by specifying `AuditMode` instead of `Enabled`.</span></span>

<span data-ttu-id="6ac6b-182">Permet `Disabled` de désactiver la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="6ac6b-182">Use `Disabled` to turn off the feature.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ac6b-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ac6b-183">See also</span></span>

* [<span data-ttu-id="6ac6b-184">Protéger les dossiers importants avec un accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="6ac6b-184">Protect important folders with controlled folder access</span></span>](controlled-folders.md)
* [<span data-ttu-id="6ac6b-185">Personnaliser l’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="6ac6b-185">Customize controlled folder access</span></span>](customize-controlled-folders.md)
* [<span data-ttu-id="6ac6b-186">Évaluer Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6ac6b-186">Evaluate Microsoft Defender for Endpoint</span></span>](evaluate-mde.md)
