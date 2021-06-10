---
title: Activer l’accès contrôlé aux dossiers
keywords: Accès contrôlé aux dossiers, windows 10, windows defender, ransomware, protéger, fichiers, dossiers, activer, utiliser
description: Découvrez comment protéger vos fichiers importants en activant l’accès contrôlé aux dossiers
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.topic: article
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
ms.openlocfilehash: 5a90a12457597fa38c648fd44bf194d2322a26af
ms.sourcegitcommit: 3e971b31435d17ceeaa9871c01e88e25ead560fb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "52861220"
---
# <a name="enable-controlled-folder-access"></a><span data-ttu-id="1f746-104">Activer l’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="1f746-104">Enable controlled folder access</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="1f746-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1f746-105">**Applies to:**</span></span>
- [<span data-ttu-id="1f746-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1f746-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="1f746-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1f746-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="1f746-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="1f746-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="1f746-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="1f746-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="1f746-110">[L’accès contrôlé aux dossiers](controlled-folders.md) vous permet de protéger les données précieuses contre les applications malveillantes et les menaces, telles que les ransomware.</span><span class="sxs-lookup"><span data-stu-id="1f746-110">[Controlled folder access](controlled-folders.md) helps you protect valuable data from malicious apps and threats, such as ransomware.</span></span> <span data-ttu-id="1f746-111">L’accès contrôlé aux dossiers est inclus Windows 10 et Windows Server 2019.</span><span class="sxs-lookup"><span data-stu-id="1f746-111">Controlled folder access is included with Windows 10 and Windows Server 2019.</span></span>

<span data-ttu-id="1f746-112">Vous pouvez activer l’accès contrôlé aux dossiers à l’aide de l’une des méthodes ci-après :</span><span class="sxs-lookup"><span data-stu-id="1f746-112">You can enable controlled folder access by using any of these methods:</span></span>

* [<span data-ttu-id="1f746-113">Sécurité Windows application</span><span class="sxs-lookup"><span data-stu-id="1f746-113">Windows Security app</span></span>](#windows-security-app)
* [<span data-ttu-id="1f746-114">Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="1f746-114">Microsoft Endpoint Manager</span></span>](#endpoint-manager)
* [<span data-ttu-id="1f746-115">Gestion des périphériques mobiles (MDM)</span><span class="sxs-lookup"><span data-stu-id="1f746-115">Mobile Device Management (MDM)</span></span>](#mobile-device-management-mdm)
* [<span data-ttu-id="1f746-116">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="1f746-116">Microsoft Endpoint Configuration Manager</span></span>](#microsoft-endpoint-configuration-manager)
* [<span data-ttu-id="1f746-117">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="1f746-117">Group Policy</span></span>](#group-policy)
* [<span data-ttu-id="1f746-118">PowerShell</span><span class="sxs-lookup"><span data-stu-id="1f746-118">PowerShell</span></span>](#powershell)

<span data-ttu-id="1f746-119">[Le mode audit](evaluate-controlled-folder-access.md) vous permet de tester le fonctionnement de la fonctionnalité (et de passer en revue les événements) sans impact sur l’utilisation normale de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1f746-119">[Audit mode](evaluate-controlled-folder-access.md) allows you to test how the feature would work (and review events) without impacting the normal use of the device.</span></span>

<span data-ttu-id="1f746-120">Les paramètres de stratégie de groupe qui désactivent la fusion de listes d’administrateurs locaux remplacent les paramètres d’accès contrôlé aux dossiers.</span><span class="sxs-lookup"><span data-stu-id="1f746-120">Group Policy settings that disable local administrator list merging will override controlled folder access settings.</span></span> <span data-ttu-id="1f746-121">Ils remplacent également les dossiers protégés et les applications autorisées définies par l’administrateur local par le biais d’un accès contrôlé aux dossiers.</span><span class="sxs-lookup"><span data-stu-id="1f746-121">They also override protected folders and allowed apps set by the local administrator through controlled folder access.</span></span> <span data-ttu-id="1f746-122">Ces stratégies sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f746-122">These policies include:</span></span>

* <span data-ttu-id="1f746-123">Antivirus Microsoft Defender configurer **le comportement de fusion de l’administrateur local pour les listes**</span><span class="sxs-lookup"><span data-stu-id="1f746-123">Microsoft Defender Antivirus **Configure local administrator merge behavior for lists**</span></span>
* <span data-ttu-id="1f746-124">System Center Endpoint Protection autoriser **les utilisateurs à ajouter des exclusions et des remplacements**</span><span class="sxs-lookup"><span data-stu-id="1f746-124">System Center Endpoint Protection **Allow users to add exclusions and overrides**</span></span>

<span data-ttu-id="1f746-125">Pour plus d’informations sur la désactivation de la fusion de listes locales, voir Empêcher ou autoriser les utilisateurs à modifier localement les paramètres de stratégie de [Microsoft Defender AV.](/windows/security/threat-protection/microsoft-defender-antivirus/configure-local-policy-overrides-microsoft-defender-antivirus#configure-how-locally-and-globally-defined-threat-remediation-and-exclusions-lists-are-merged)</span><span class="sxs-lookup"><span data-stu-id="1f746-125">For more information about disabling local list merging, see [Prevent or allow users to locally modify Microsoft Defender AV policy settings](/windows/security/threat-protection/microsoft-defender-antivirus/configure-local-policy-overrides-microsoft-defender-antivirus#configure-how-locally-and-globally-defined-threat-remediation-and-exclusions-lists-are-merged).</span></span>

## <a name="windows-security-app"></a><span data-ttu-id="1f746-126">Sécurité Windows application</span><span class="sxs-lookup"><span data-stu-id="1f746-126">Windows Security app</span></span>

1. <span data-ttu-id="1f746-127">Ouvrez l Sécurité Windows en sélectionnant l’icône de bouclier dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="1f746-127">Open the Windows Security app by selecting the shield icon in the task bar.</span></span> <span data-ttu-id="1f746-128">Vous pouvez également rechercher Defender dans le menu **Démarrer.**</span><span class="sxs-lookup"><span data-stu-id="1f746-128">You can also search the start menu for **Defender**.</span></span>

2. <span data-ttu-id="1f746-129">Sélectionnez la **vignette & protection** contre les virus contre les menaces (ou l’icône de bouclier dans la barre de menus de gauche), puis sélectionnez Protection contre les **ransomware.**</span><span class="sxs-lookup"><span data-stu-id="1f746-129">Select the **Virus & threat protection** tile (or the shield icon on the left menu bar) and then select **Ransomware protection**.</span></span>

3. <span data-ttu-id="1f746-130">Définissez le commutateur pour **l’accès contrôlé aux** dossiers sur **On**.</span><span class="sxs-lookup"><span data-stu-id="1f746-130">Set the switch for **Controlled folder access** to **On**.</span></span>

> [!NOTE]
> <span data-ttu-id="1f746-131">Si l’accès contrôlé aux dossiers est configuré avec la stratégie de groupe, PowerShell ou les CSP MDM, l’état change dans l’application Sécurité Windows après un redémarrage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1f746-131">If controlled folder access is configured with Group Policy, PowerShell, or MDM CSPs, the state will change in the Windows Security app after a restart of the device.</span></span>
> <span data-ttu-id="1f746-132">Si la fonctionnalité est définie sur **le mode Audit** avec l’un de ces outils, l’application Sécurité Windows affiche l’état comme Étant **éteint.**</span><span class="sxs-lookup"><span data-stu-id="1f746-132">If the feature is set to **Audit mode** with any of those tools, the Windows Security app will show the state as **Off**.</span></span>
> <span data-ttu-id="1f746-133">Si vous protégez les données de profil utilisateur, nous vous recommandons de le faire sur le lecteur d’installation Windows par défaut.</span><span class="sxs-lookup"><span data-stu-id="1f746-133">If you are protecting user profile data, we recommend that the user profile should be on the default Windows installation drive.</span></span>

## <a name="endpoint-manager"></a><span data-ttu-id="1f746-134">Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="1f746-134">Endpoint Manager</span></span>

1. <span data-ttu-id="1f746-135">Connectez-vous au [Endpoint Manager](https://endpoint.microsoft.com) et ouvrez **Endpoint Security**.</span><span class="sxs-lookup"><span data-stu-id="1f746-135">Sign in to the [Endpoint Manager](https://endpoint.microsoft.com) and open **Endpoint Security**.</span></span>

2. <span data-ttu-id="1f746-136">Go to **Attack Surface Reduction**  >  **Policy**.</span><span class="sxs-lookup"><span data-stu-id="1f746-136">Go to **Attack Surface Reduction** > **Policy**.</span></span>

3. <span data-ttu-id="1f746-137">Sélectionnez **Plateforme,** **sélectionnez Windows 10 et** ultérieures, puis sélectionnez les règles de réduction de **la surface d’attaque de profil**  >  **Créer.**</span><span class="sxs-lookup"><span data-stu-id="1f746-137">Select **Platform**, choose **Windows 10 and later**, and select the profile **Attack Surface Reduction rules** > **Create**.</span></span>

4.  <span data-ttu-id="1f746-138">Nommez la stratégie et ajoutez une description.</span><span class="sxs-lookup"><span data-stu-id="1f746-138">Name the policy and add a description.</span></span> <span data-ttu-id="1f746-139">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="1f746-139">Select **Next**.</span></span>

5.  <span data-ttu-id="1f746-140">Faites défiler la page vers le bas, sélectionnez la page de la page de **la protection** des dossiers activée, puis choisissez **Activer.**</span><span class="sxs-lookup"><span data-stu-id="1f746-140">Scroll down to the bottom, select the **Enable Folder Protection** drop-down, and choose **Enable**.</span></span>

6.  <span data-ttu-id="1f746-141">Sélectionnez **la liste des dossiers supplémentaires** qui doivent être protégés et ajoutez les dossiers qui doivent être protégés.</span><span class="sxs-lookup"><span data-stu-id="1f746-141">Select **List of additional folders that need to be protected** and add the folders that need to be protected.</span></span>

7.  <span data-ttu-id="1f746-142">Sélectionnez **la liste des applications qui ont accès aux dossiers** protégés et ajoutez les applications qui ont accès aux dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="1f746-142">Select **List of apps that have access to protected folders** and add the apps that have access to protected folders.</span></span>

8.  <span data-ttu-id="1f746-143">Sélectionnez **Exclure les fichiers et les** chemins d’accès des règles de réduction de la surface d’attaque et ajoutez les fichiers et les chemins d’accès qui doivent être exclus des règles de réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="1f746-143">Select **Exclude files and paths from attack surface reduction rules** and add the files and paths that need to be excluded from attack surface reduction rules.</span></span>

9.  <span data-ttu-id="1f746-144">Sélectionnez les **affectations de profil,** affectez à tous les utilisateurs **& tous** les appareils, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1f746-144">Select the profile **Assignments**, assign to **All Users & All Devices**, and select **Save**.</span></span>

10.  <span data-ttu-id="1f746-145">Sélectionnez **Suivant** pour enregistrer chaque lame ouvert, puis **Créer.**</span><span class="sxs-lookup"><span data-stu-id="1f746-145">Select **Next** to save each open blade and then **Create**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="1f746-146">Les caractères génériques sont pris en charge pour les applications, mais pas pour les dossiers.</span><span class="sxs-lookup"><span data-stu-id="1f746-146">Wildcards are supported for applications, but not for folders.</span></span> <span data-ttu-id="1f746-147">Les sous-foldeurs ne sont pas protégés.</span><span class="sxs-lookup"><span data-stu-id="1f746-147">Subfolders are not protected.</span></span> <span data-ttu-id="1f746-148">Les applications autorisées continueront à déclencher des événements jusqu’à leur redémarrage.</span><span class="sxs-lookup"><span data-stu-id="1f746-148">Allowed apps will continue to trigger events until they are restarted.</span></span>

## <a name="mobile-device-management-mdm"></a><span data-ttu-id="1f746-149">Gestion des périphériques mobiles (MDM)</span><span class="sxs-lookup"><span data-stu-id="1f746-149">Mobile Device Management (MDM)</span></span>

<span data-ttu-id="1f746-150">Utilisez le fournisseur de services de configuration [./Vendor/MSFT/Policy/Config/ControlledFolderAccessProtectedFolders](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders) (CSP) pour permettre aux applications d’apporter des modifications aux dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="1f746-150">Use the [./Vendor/MSFT/Policy/Config/ControlledFolderAccessProtectedFolders](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders) configuration service provider (CSP) to allow apps to make changes to protected folders.</span></span>

## <a name="microsoft-endpoint-configuration-manager"></a><span data-ttu-id="1f746-151">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="1f746-151">Microsoft Endpoint Configuration Manager</span></span>

1. <span data-ttu-id="1f746-152">In Microsoft Endpoint Configuration Manager, go to **Assets and Compliance**  >  **Endpoint Protection** Windows Defender  >  **Exploit Guard**.</span><span class="sxs-lookup"><span data-stu-id="1f746-152">In Microsoft Endpoint Configuration Manager, go to **Assets and Compliance** > **Endpoint Protection** > **Windows Defender Exploit Guard**.</span></span>

2. <span data-ttu-id="1f746-153">Sélectionnez **Home**  >  **Create Exploit Guard Policy**.</span><span class="sxs-lookup"><span data-stu-id="1f746-153">Select **Home** > **Create Exploit Guard Policy**.</span></span>

3. <span data-ttu-id="1f746-154">Entrez un nom et une description, sélectionnez **Accès contrôlé aux** dossiers, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="1f746-154">Enter a name and a description, select **Controlled folder access**, and select **Next**.</span></span>

4. <span data-ttu-id="1f746-155">Choisissez si bloquer ou auditer les modifications, autoriser d’autres applications ou ajouter d’autres dossiers, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="1f746-155">Choose whether block or audit changes, allow other apps, or add other folders, and select **Next**.</span></span>
   > [!NOTE]
   > <span data-ttu-id="1f746-156">Wilcard est pris en charge pour les applications, mais pas pour les dossiers.</span><span class="sxs-lookup"><span data-stu-id="1f746-156">Wilcard is supported for applications, but not for folders.</span></span> <span data-ttu-id="1f746-157">Les sous-foldeurs ne sont pas protégés.</span><span class="sxs-lookup"><span data-stu-id="1f746-157">Subfolders are not protected.</span></span> <span data-ttu-id="1f746-158">Les applications autorisées continueront à déclencher des événements jusqu’à leur redémarrage.</span><span class="sxs-lookup"><span data-stu-id="1f746-158">Allowed apps will continue to trigger events until they are restarted.</span></span>

5. <span data-ttu-id="1f746-159">Examinez les paramètres et sélectionnez **Suivant** pour créer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="1f746-159">Review the settings and select **Next** to create the policy.</span></span>

6. <span data-ttu-id="1f746-160">Une fois la stratégie créée, **fermez**.</span><span class="sxs-lookup"><span data-stu-id="1f746-160">After the policy is created, **Close**.</span></span>

## <a name="group-policy"></a><span data-ttu-id="1f746-161">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="1f746-161">Group Policy</span></span>

1. <span data-ttu-id="1f746-162">Sur votre appareil de gestion des stratégies de groupe, ouvrez la [Console](https://technet.microsoft.com/library/cc731212.aspx)de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous souhaitez configurer et sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="1f746-162">On your Group Policy management device, open the [Group Policy Management Console](https://technet.microsoft.com/library/cc731212.aspx), right-click the Group Policy Object you want to configure and select **Edit**.</span></span>

2. <span data-ttu-id="1f746-163">Dans l’**Éditeur de gestion des stratégies de groupe**, accédez à **Configuration ordinateur**, puis sélectionnez **Modèles d’administration**.</span><span class="sxs-lookup"><span data-stu-id="1f746-163">In the **Group Policy Management Editor**, go to **Computer configuration** and select **Administrative templates**.</span></span>

3. <span data-ttu-id="1f746-164">Développez l’arborescence **Windows composants > Antivirus Microsoft Defender > Windows Defender Exploit Guard > accès contrôlé aux dossiers.**</span><span class="sxs-lookup"><span data-stu-id="1f746-164">Expand the tree to **Windows components > Microsoft Defender Antivirus > Windows Defender Exploit Guard > Controlled folder access**.</span></span>

4. <span data-ttu-id="1f746-165">Double-cliquez sur **le paramètre Configurer l’accès contrôlé aux** dossiers et définissez l’option sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="1f746-165">Double-click the **Configure Controlled folder access** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="1f746-166">Dans la section Options, vous devez spécifier l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f746-166">In the options section you must specify one of the following options:</span></span>
    * <span data-ttu-id="1f746-167">**Activer** : les applications malveillantes et suspectes ne seront pas autorisées à apporter des modifications aux fichiers des dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="1f746-167">**Enable** - Malicious and suspicious apps won't be allowed to make changes to files in protected folders.</span></span> <span data-ttu-id="1f746-168">Une notification sera fournie dans le journal Windows événements.</span><span class="sxs-lookup"><span data-stu-id="1f746-168">A notification will be provided in the Windows event log.</span></span>
    * <span data-ttu-id="1f746-169">**Désactiver (par défaut)** : la fonctionnalité Accès contrôlé aux dossiers ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="1f746-169">**Disable (Default)** - The Controlled folder access feature won't work.</span></span> <span data-ttu-id="1f746-170">Toutes les applications peuvent apporter des modifications aux fichiers des dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="1f746-170">All apps can make changes to files in protected folders.</span></span>
    * <span data-ttu-id="1f746-171">**Mode audit** : les modifications sont autorisées si une application malveillante ou suspecte tente d’apporter une modification à un fichier dans un dossier protégé.</span><span class="sxs-lookup"><span data-stu-id="1f746-171">**Audit Mode** - Changes will be allowed if a malicious or suspicious app attempts to make a change to a file in a protected folder.</span></span> <span data-ttu-id="1f746-172">Toutefois, il sera enregistré dans le journal Windows événements dans lequel vous pourrez évaluer l’impact sur votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1f746-172">However, it will be recorded in the Windows event log where you can assess the impact on your organization.</span></span>
    * <span data-ttu-id="1f746-173">**Bloquer la modification du disque** uniquement : les tentatives d’écriture dans les secteurs de disque par des applications nontrues sont enregistrées dans Windows journal des événements.</span><span class="sxs-lookup"><span data-stu-id="1f746-173">**Block disk modification only** - Attempts by untrusted apps to write to disk sectors will be logged in Windows Event log.</span></span> <span data-ttu-id="1f746-174">Ces journaux se trouvent dans **les journaux des applications** et des services > Microsoft > Windows > Windows Defender > Operational > ID 1123.</span><span class="sxs-lookup"><span data-stu-id="1f746-174">These logs can be found in **Applications and Services Logs** > Microsoft > Windows > Windows Defender > Operational > ID 1123.</span></span>
    * <span data-ttu-id="1f746-175">**Auditer** la modification du disque uniquement : seules les tentatives d’écriture dans les secteurs de disque protégés seront **enregistrées** dans le journal des événements Windows (sous Journaux des applications et des services  >  **Microsoft**  >  **Windows**  >  **Windows Defender**  >  **Operational**  >  **ID 1124**).</span><span class="sxs-lookup"><span data-stu-id="1f746-175">**Audit disk modification only** - Only attempts to write to protected disk sectors will be recorded in the Windows event log (under **Applications and Services Logs** > **Microsoft** > **Windows** > **Windows Defender** > **Operational** > **ID 1124**).</span></span> <span data-ttu-id="1f746-176">Les tentatives de modification ou de suppression de fichiers dans des dossiers protégés ne sont pas enregistrées.</span><span class="sxs-lookup"><span data-stu-id="1f746-176">Attempts to modify or delete files in protected folders won't be recorded.</span></span>

      ![Capture d’écran de l’option de stratégie de groupe Activée et mode Audit sélectionnée dans la baisse](/microsoft-365/security/defender-endpoint/images/cfa-gp-enable)

> [!IMPORTANT]
> <span data-ttu-id="1f746-178">Pour activer entièrement l’accès contrôlé aux dossiers, vous  devez définir l’option de stratégie de groupe sur Activé et sélectionner Bloquer dans le menu déroulant Options. </span><span class="sxs-lookup"><span data-stu-id="1f746-178">To fully enable controlled folder access, you must set the Group Policy option to **Enabled** and select **Block** in the options drop-down menu.</span></span>

## <a name="powershell"></a><span data-ttu-id="1f746-179">PowerShell</span><span class="sxs-lookup"><span data-stu-id="1f746-179">PowerShell</span></span>

1. <span data-ttu-id="1f746-180">Tapez **powershell** dans le menu Démarrer, cliquez avec le **bouton droit sur Windows PowerShell** puis **sélectionnez Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="1f746-180">Type **powershell** in the Start menu, right-click **Windows PowerShell** and select **Run as administrator**.</span></span>

2. <span data-ttu-id="1f746-181">Entrez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="1f746-181">Enter the following cmdlet:</span></span>

    ```PowerShell
    Set-MpPreference -EnableControlledFolderAccess Enabled
    ```

<span data-ttu-id="1f746-182">Vous pouvez activer la fonctionnalité en mode audit en spécifiant `AuditMode` au lieu de `Enabled` .</span><span class="sxs-lookup"><span data-stu-id="1f746-182">You can enable the feature in audit mode by specifying `AuditMode` instead of `Enabled`.</span></span>

<span data-ttu-id="1f746-183">Permet `Disabled` de désactiver la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1f746-183">Use `Disabled` to turn off the feature.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f746-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f746-184">See also</span></span>

* [<span data-ttu-id="1f746-185">Protéger les dossiers importants avec un accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="1f746-185">Protect important folders with controlled folder access</span></span>](controlled-folders.md)
* [<span data-ttu-id="1f746-186">Personnaliser l’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="1f746-186">Customize controlled folder access</span></span>](customize-controlled-folders.md)
* [<span data-ttu-id="1f746-187">Évaluer Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1f746-187">Evaluate Microsoft Defender for Endpoint</span></span>](evaluate-mde.md)
