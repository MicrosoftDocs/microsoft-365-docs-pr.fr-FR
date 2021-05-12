---
title: Personnaliser l’accès contrôlé aux dossiers
description: Ajoutez d’autres dossiers qui doivent être protégés par un accès contrôlé aux dossiers ou autorisez les applications qui bloquent de manière incorrecte les modifications apportées aux fichiers importants.
keywords: Accès contrôlé aux dossiers, windows 10, windows defender, ransomware, protéger, fichiers, dossiers, personnaliser, ajouter un dossier, ajouter une application, autoriser, ajouter un exécutable
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Normal
audience: ITPro
author: denisebmsft
ms.author: deniseb
ms.reviewer: jcedola, dbodorin, vladiso, nixanm, anvascon
manager: dansimp
ms.date: 05/10/2021
ms.technology: mde
ms.topic: how-to
ms.openlocfilehash: e12368b6241a2c79eead66ed77b30b7864af3955
ms.sourcegitcommit: 68383240ef7a673d5f28e2ecfab9f105bf1d8c8f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2021
ms.locfileid: "52326537"
---
# <a name="customize-controlled-folder-access"></a><span data-ttu-id="47b2f-104">Personnaliser l’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="47b2f-104">Customize controlled folder access</span></span>

<span data-ttu-id="47b2f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="47b2f-105">**Applies to:**</span></span>
- [<span data-ttu-id="47b2f-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="47b2f-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="47b2f-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="47b2f-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> [!TIP]
> <span data-ttu-id="47b2f-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="47b2f-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="47b2f-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="47b2f-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="47b2f-110">L’accès contrôlé aux dossiers vous permet de protéger les données précieuses contre les applications malveillantes et les menaces, telles que les ransomware.</span><span class="sxs-lookup"><span data-stu-id="47b2f-110">Controlled folder access helps you protect valuable data from malicious apps and threats, such as ransomware.</span></span> <span data-ttu-id="47b2f-111">L’accès contrôlé aux dossiers est pris en charge sur les clients Windows Server 2019 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="47b2f-111">Controlled folder access is supported on Windows Server 2019 and Windows 10 clients.</span></span> <span data-ttu-id="47b2f-112">Cet article explique comment personnaliser les fonctionnalités d’accès contrôlé aux dossiers et comprend les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="47b2f-112">This article describes how to customize controlled folder access capabilities, and includes the following sections:</span></span>

- [<span data-ttu-id="47b2f-113">Protéger des dossiers supplémentaires</span><span class="sxs-lookup"><span data-stu-id="47b2f-113">Protect additional folders</span></span>](#protect-additional-folders)
- [<span data-ttu-id="47b2f-114">Ajouter des applications qui doivent être autorisées à accéder aux dossiers protégés</span><span class="sxs-lookup"><span data-stu-id="47b2f-114">Add apps that should be allowed to access protected folders</span></span>](#allow-specific-apps-to-make-changes-to-controlled-folders)
- [<span data-ttu-id="47b2f-115">Autoriser les fichiers exécutables signés à accéder aux dossiers protégés</span><span class="sxs-lookup"><span data-stu-id="47b2f-115">Allow signed executable files to access protected folders</span></span>](#allow-signed-executable-files-to-access-protected-folders)
- [<span data-ttu-id="47b2f-116">Personnaliser la notification</span><span class="sxs-lookup"><span data-stu-id="47b2f-116">Customize the notification</span></span>](#customize-the-notification)

> [!IMPORTANT]
> <span data-ttu-id="47b2f-117">L’accès contrôlé aux dossiers surveille les applications pour les activités détectées comme malveillantes.</span><span class="sxs-lookup"><span data-stu-id="47b2f-117">Controlled folder access monitors apps for activities that are detected as malicious.</span></span> <span data-ttu-id="47b2f-118">Parfois, les applications légitimes ne peuvent pas apporter de modifications à vos fichiers.</span><span class="sxs-lookup"><span data-stu-id="47b2f-118">Sometimes, legitimate apps are blocked from making changes to your files.</span></span> <span data-ttu-id="47b2f-119">Si l’accès contrôlé aux dossiers a un impact sur la productivité de votre organisation, vous pouvez envisager d’exécutez cette fonctionnalité en [mode audit](audit-windows-defender.md) pour en évaluer pleinement l’impact.</span><span class="sxs-lookup"><span data-stu-id="47b2f-119">If controlled folder access impacts your organization's productivity, you might consider running this feature in [audit mode](audit-windows-defender.md) to fully assess the impact.</span></span>

## <a name="protect-additional-folders"></a><span data-ttu-id="47b2f-120">Protéger des dossiers supplémentaires</span><span class="sxs-lookup"><span data-stu-id="47b2f-120">Protect additional folders</span></span>

<span data-ttu-id="47b2f-121">L’accès contrôlé aux dossiers s’applique à de nombreux dossiers système et emplacements par défaut, y compris aux dossiers tels que **Documents,** **Images** et **Films.**</span><span class="sxs-lookup"><span data-stu-id="47b2f-121">Controlled folder access applies to many system folders and default locations, including folders such as **Documents**, **Pictures**, and **Movies**.</span></span> <span data-ttu-id="47b2f-122">Vous pouvez ajouter d’autres dossiers à protéger, mais vous ne pouvez pas supprimer les dossiers par défaut dans la liste par défaut.</span><span class="sxs-lookup"><span data-stu-id="47b2f-122">You can add other folders to be protected, but you cannot remove the default folders in the default list.</span></span>

<span data-ttu-id="47b2f-123">L’ajout d’autres dossiers à l’accès contrôlé aux dossiers peut être utile dans les cas où vous ne stockez pas de fichiers dans les bibliothèques Windows par défaut ou lorsque vous avez modifié l’emplacement par défaut de vos bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="47b2f-123">Adding other folders to controlled folder access can be helpful for cases when you don't store files in the default Windows libraries, or you've changed the default location of your libraries.</span></span>

<span data-ttu-id="47b2f-124">Vous pouvez également spécifier des partages réseau et des lecteurs mappés.</span><span class="sxs-lookup"><span data-stu-id="47b2f-124">You can also specify network shares and mapped drives.</span></span> <span data-ttu-id="47b2f-125">Les variables d’environnement et les caractères génériques sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="47b2f-125">Environment variables and wildcards are supported.</span></span> <span data-ttu-id="47b2f-126">Pour plus d’informations sur l’utilisation de caractères génériques, voir Utiliser des caractères génériques dans les listes d’exclusions de nom de fichier et de dossier ou [d’extension.](configure-extension-file-exclusions-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="47b2f-126">For information about using wildcards, see [Use wildcards in the file name and folder path or extension exclusion lists](configure-extension-file-exclusions-microsoft-defender-antivirus.md).</span></span>

<span data-ttu-id="47b2f-127">Vous pouvez utiliser l’application de sécurité Windows, la stratégie de groupe, les cmdlets PowerShell ou les fournisseurs de services de configuration de gestion des appareils mobiles pour ajouter et supprimer des dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="47b2f-127">You can use the Windows Security app, Group Policy, PowerShell cmdlets, or mobile device management configuration service providers to add and remove protected folders.</span></span>

### <a name="use-the-windows-security-app-to-protect-additional-folders"></a><span data-ttu-id="47b2f-128">Utiliser l’application Sécurité Windows pour protéger des dossiers supplémentaires</span><span class="sxs-lookup"><span data-stu-id="47b2f-128">Use the Windows Security app to protect additional folders</span></span>

1. <span data-ttu-id="47b2f-129">Ouvrez l’application Sécurité Windows en sélectionnant l’icône de bouclier dans la barre des tâches ou en recherchant la sécurité *dans* le menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="47b2f-129">Open the Windows Security app by selecting the shield icon in the task bar, or by searching for *security* in the Start menu.</span></span>

2. <span data-ttu-id="47b2f-130">Sélectionnez **Virus & protection contre les** menaces, puis faites défiler vers le bas jusqu’à la section Protection contre les **ransomware.**</span><span class="sxs-lookup"><span data-stu-id="47b2f-130">Select **Virus & threat protection**, and then scroll down to the **Ransomware protection** section.</span></span>

3. <span data-ttu-id="47b2f-131">Sélectionnez **Gérer la protection contre les ransomware** pour ouvrir le volet protection contre les **ransomware.**</span><span class="sxs-lookup"><span data-stu-id="47b2f-131">Select **Manage ransomware protection** to open the **Ransomware protection** pane.</span></span>

4. <span data-ttu-id="47b2f-132">Sous la section **Accès contrôlé aux dossiers,** sélectionnez **Dossiers protégés.**</span><span class="sxs-lookup"><span data-stu-id="47b2f-132">Under the **Controlled folder access** section, select **Protected folders**.</span></span>

5. <span data-ttu-id="47b2f-133">Sélectionnez **Oui** dans **l’invite contrôle d’accès** utilisateur.</span><span class="sxs-lookup"><span data-stu-id="47b2f-133">Choose **Yes** on the **User Access Control** prompt.</span></span> <span data-ttu-id="47b2f-134">Le **volet Dossiers protégés** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="47b2f-134">The **Protected folders** pane displays.</span></span>

6. <span data-ttu-id="47b2f-135">Sélectionnez **Ajouter un dossier protégé et** suivez les invites pour ajouter des dossiers.</span><span class="sxs-lookup"><span data-stu-id="47b2f-135">Select **Add a protected folder** and follow the prompts to add folders.</span></span>

### <a name="use-group-policy-to-protect-additional-folders"></a><span data-ttu-id="47b2f-136">Utiliser une stratégie de groupe pour protéger des dossiers supplémentaires</span><span class="sxs-lookup"><span data-stu-id="47b2f-136">Use Group Policy to protect additional folders</span></span>

1. <span data-ttu-id="47b2f-137">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la[Console de gestion des stratégies de groupe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)?preserve=true).</span><span class="sxs-lookup"><span data-stu-id="47b2f-137">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)?preserve=true).</span></span> 

2. <span data-ttu-id="47b2f-138">Cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous souhaitez configurer, puis sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="47b2f-138">Right-click the Group Policy Object you want to configure, and then select **Edit**.</span></span>

3. <span data-ttu-id="47b2f-139">Dans votre Éditeur **de gestion des stratégies de** groupe, allez aux modèles d’administration des stratégies de **configuration**  >    >  **ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="47b2f-139">In your **Group Policy Management Editor**, go to **Computer configuration** > **Policies** > **Administrative templates**.</span></span>

4. <span data-ttu-id="47b2f-140">Développez l’arborescence **des composants Windows** de l’Antivirus  >  **Microsoft Defender**  >  **Windows Defender’accès contrôlé** aux  >  **dossiers** Exploit Guard.</span><span class="sxs-lookup"><span data-stu-id="47b2f-140">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Windows Defender Exploit Guard** > **Controlled folder access**.</span></span> <br/><span data-ttu-id="47b2f-141">**REMARQUE**: sur les versions antérieures de Windows, vous pouvez voir **Windows Defender antivirus** au lieu de **l’Antivirus Microsoft Defender.**</span><span class="sxs-lookup"><span data-stu-id="47b2f-141">**NOTE**: On older versions of Windows, you might see **Windows Defender Antivirus** instead of **Microsoft Defender Antivirus**.</span></span>

5. <span data-ttu-id="47b2f-142">Double-cliquez **sur Dossiers protégés configurés,** puis définissez l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="47b2f-142">Double-click **Configured protected folders**, and then set the option to **Enabled**.</span></span> <span data-ttu-id="47b2f-143">Sélectionnez **Afficher** et spécifiez chaque dossier à protéger.</span><span class="sxs-lookup"><span data-stu-id="47b2f-143">Select **Show**, and specify each folder that you want to protect.</span></span>

6. <span data-ttu-id="47b2f-144">Déployez votre objet de stratégie de groupe comme vous le faites généralement.</span><span class="sxs-lookup"><span data-stu-id="47b2f-144">Deploy your Group Policy Object as you usually do.</span></span>

### <a name="use-powershell-to-protect-additional-folders"></a><span data-ttu-id="47b2f-145">Utiliser PowerShell pour protéger des dossiers supplémentaires</span><span class="sxs-lookup"><span data-stu-id="47b2f-145">Use PowerShell to protect additional folders</span></span>

1. <span data-ttu-id="47b2f-146">Tapez **PowerShell dans** le menu Démarrer, cliquez avec le **bouton droit sur Windows PowerShell** puis **sélectionnez Exécuter en tant qu’administrateur**</span><span class="sxs-lookup"><span data-stu-id="47b2f-146">Type **PowerShell** in the Start menu, right-click **Windows PowerShell** and select **Run as administrator**</span></span>

2. <span data-ttu-id="47b2f-147">Tapez l’cmdlet PowerShell suivante, en remplaçant par le chemin d’accès du dossier `<the folder to be protected>` (par exemple : `"c:\apps\"`</span><span class="sxs-lookup"><span data-stu-id="47b2f-147">Type the following PowerShell cmdlet, replacing `<the folder to be protected>` with the folder's path (such as `"c:\apps\"`):</span></span>

    ```PowerShell
    Add-MpPreference -ControlledFolderAccessProtectedFolders "<the folder to be protected>"
    ```
3. <span data-ttu-id="47b2f-148">Répétez l’étape 2 pour chaque dossier que vous souhaitez protéger.</span><span class="sxs-lookup"><span data-stu-id="47b2f-148">Repeat step 2 for each folder that you want to protect.</span></span> <span data-ttu-id="47b2f-149">Les dossiers protégés sont visibles dans l’application Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="47b2f-149">Folders that are protected are visible in the Windows Security app.</span></span>

   :::image type="content" source="images/cfa-allow-folder-ps.png" alt-text="Fenêtre PowerShell avec cmdlet affichée":::

> [!IMPORTANT]
> <span data-ttu-id="47b2f-151">Permet `Add-MpPreference` d’ajouter ou d’ajouter des applications à la liste et non `Set-MpPreference` .</span><span class="sxs-lookup"><span data-stu-id="47b2f-151">Use `Add-MpPreference` to append or add apps to the list and not `Set-MpPreference`.</span></span> <span data-ttu-id="47b2f-152">`Set-MpPreference`L’utilisation de la cmdlet va supprimer la liste existante.</span><span class="sxs-lookup"><span data-stu-id="47b2f-152">Using the `Set-MpPreference` cmdlet will overwrite the existing list.</span></span>

### <a name="use-mdm-csps-to-protect-additional-folders"></a><span data-ttu-id="47b2f-153">Utiliser des CSP mdm pour protéger des dossiers supplémentaires</span><span class="sxs-lookup"><span data-stu-id="47b2f-153">Use MDM CSPs to protect additional folders</span></span>

<span data-ttu-id="47b2f-154">Utilisez le fournisseur de services de configuration [./Vendor/MSFT/Policy/Config/Defender/GuardedFoldersList](/windows/client-management/mdm/policy-csp-defender#defender-guardedfolderslist) (CSP) pour permettre aux applications d’apporter des modifications aux dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="47b2f-154">Use the [./Vendor/MSFT/Policy/Config/Defender/GuardedFoldersList](/windows/client-management/mdm/policy-csp-defender#defender-guardedfolderslist) configuration service provider (CSP) to allow apps to make changes to protected folders.</span></span>

## <a name="allow-specific-apps-to-make-changes-to-controlled-folders"></a><span data-ttu-id="47b2f-155">Autoriser des applications spécifiques à apporter des modifications aux dossiers contrôlés</span><span class="sxs-lookup"><span data-stu-id="47b2f-155">Allow specific apps to make changes to controlled folders</span></span>

<span data-ttu-id="47b2f-156">Vous pouvez spécifier si certaines applications sont toujours considérées comme sécurisées et accorder un accès en écriture aux fichiers dans les dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="47b2f-156">You can specify if certain apps are always considered safe and give write access to files in protected folders.</span></span> <span data-ttu-id="47b2f-157">Autoriser les applications peut être utile si une application particulière que vous connaissez et que vous faites confiance est bloquée par la fonctionnalité d’accès contrôlé aux dossiers.</span><span class="sxs-lookup"><span data-stu-id="47b2f-157">Allowing apps can be useful if a particular app you know and trust is being blocked by the controlled folder access feature.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="47b2f-158">Par défaut, Windows ajoute des applications qui sont considérées comme conviviales à la liste autorisée.</span><span class="sxs-lookup"><span data-stu-id="47b2f-158">By default, Windows adds apps that are considered friendly to the allowed list.</span></span> <span data-ttu-id="47b2f-159">Ces applications ajoutées automatiquement ne sont pas enregistrées dans la liste affichée dans l’application Sécurité Windows ou à l’aide des cmdlets PowerShell associées.</span><span class="sxs-lookup"><span data-stu-id="47b2f-159">Such apps that are added automatically are not recorded in the list shown in the Windows Security app or by using the associated PowerShell cmdlets.</span></span> <span data-ttu-id="47b2f-160">Il n’est pas nécessaire d’ajouter la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="47b2f-160">You shouldn't need to add most apps.</span></span> <span data-ttu-id="47b2f-161">Ajoutez uniquement des applications si elles sont bloquées et que vous pouvez vérifier leur fiabilité.</span><span class="sxs-lookup"><span data-stu-id="47b2f-161">Only add apps if they are being blocked and you can verify their trustworthiness.</span></span>

<span data-ttu-id="47b2f-162">Lorsque vous ajoutez une application, vous devez spécifier son emplacement.</span><span class="sxs-lookup"><span data-stu-id="47b2f-162">When you add an app, you have to specify the app's location.</span></span> <span data-ttu-id="47b2f-163">Seule l’application à cet emplacement sera autorisée à accéder aux dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="47b2f-163">Only the app in that location will be permitted access to the protected folders.</span></span> <span data-ttu-id="47b2f-164">Si l’application (avec le même nom) se trouve à un autre emplacement, elle n’est pas ajoutée à la liste d’applications et peut être bloquée par l’accès contrôlé aux dossiers.</span><span class="sxs-lookup"><span data-stu-id="47b2f-164">If the app (with the same name) is in a different location, it will not be added to the allowlist and may be blocked by controlled folder access.</span></span>

<span data-ttu-id="47b2f-165">Une application ou un service autorisé dispose uniquement d’un accès en écriture à un dossier contrôlé après son démarrage.</span><span class="sxs-lookup"><span data-stu-id="47b2f-165">An allowed application or service only has write access to a controlled folder after it starts.</span></span> <span data-ttu-id="47b2f-166">Par exemple, un service de mise à jour continue de déclencher des événements une fois autorisé jusqu’à ce qu’il soit arrêté et redémarré.</span><span class="sxs-lookup"><span data-stu-id="47b2f-166">For example, an update service will continue to trigger events after it's allowed until it is stopped and restarted.</span></span>

### <a name="use-the-windows-defender-security-app-to-allow-specific-apps"></a><span data-ttu-id="47b2f-167">Utiliser l’application Windows Defender security pour autoriser des applications spécifiques</span><span class="sxs-lookup"><span data-stu-id="47b2f-167">Use the Windows Defender Security app to allow specific apps</span></span>

1. <span data-ttu-id="47b2f-168">Ouvrez l’application Sécurité Windows en recherchant sécurité dans le menu **Démarrer.**</span><span class="sxs-lookup"><span data-stu-id="47b2f-168">Open the Windows Security app by searching the start menu for **Security**.</span></span>

2. <span data-ttu-id="47b2f-169">Sélectionnez la **vignette & protection** contre les virus contre les menaces (ou l’icône de bouclier dans la barre de menus de gauche), puis sélectionnez Gérer la protection contre les **ransomware.**</span><span class="sxs-lookup"><span data-stu-id="47b2f-169">Select the **Virus & threat protection** tile (or the shield icon on the left menu bar) and then select **Manage ransomware protection**.</span></span>

3. <span data-ttu-id="47b2f-170">Sous la section **Accès contrôlé aux dossiers,** **sélectionnez Autoriser une application via Accès contrôlé aux dossiers**</span><span class="sxs-lookup"><span data-stu-id="47b2f-170">Under the **Controlled folder access** section, select **Allow an app through Controlled folder access**</span></span>

4. <span data-ttu-id="47b2f-171">Sélectionnez **Ajouter une application autorisée et** suivez les invites pour ajouter des applications.</span><span class="sxs-lookup"><span data-stu-id="47b2f-171">Select **Add an allowed app** and follow the prompts to add apps.</span></span>

   :::image type="content" source="images/cfa-allow-app.png" alt-text="Ajouter un bouton d’application autorisé":::

### <a name="use-group-policy-to-allow-specific-apps"></a><span data-ttu-id="47b2f-173">Utiliser une stratégie de groupe pour autoriser des applications spécifiques</span><span class="sxs-lookup"><span data-stu-id="47b2f-173">Use Group Policy to allow specific apps</span></span>

1. <span data-ttu-id="47b2f-174">Sur votre appareil de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)?preserve=true)de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous souhaitez configurer et sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="47b2f-174">On your Group Policy management device, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)?preserve=true), right-click the Group Policy Object you want to configure and select **Edit**.</span></span>

2. <span data-ttu-id="47b2f-175">Dans l’**Éditeur de gestion des stratégies de groupe**, accédez à **Configuration ordinateur**, puis sélectionnez **Modèles d’administration**.</span><span class="sxs-lookup"><span data-stu-id="47b2f-175">In the **Group Policy Management Editor**, go to **Computer configuration** and select **Administrative templates**.</span></span>

3. <span data-ttu-id="47b2f-176">Développez l’arborescence **des composants Windows** de l’Antivirus  >  **Microsoft Defender**  >  **Windows Defender’accès contrôlé** aux  >  **dossiers** Exploit Guard.</span><span class="sxs-lookup"><span data-stu-id="47b2f-176">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Windows Defender Exploit Guard** > **Controlled folder access**.</span></span>

4. <span data-ttu-id="47b2f-177">Double-cliquez sur le **paramètre Configurer les applications autorisées** et définissez l’option sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="47b2f-177">Double-click the **Configure allowed applications** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="47b2f-178">Sélectionnez **Afficher** et entrez chaque application.</span><span class="sxs-lookup"><span data-stu-id="47b2f-178">Select **Show** and enter each app.</span></span>

### <a name="use-powershell-to-allow-specific-apps"></a><span data-ttu-id="47b2f-179">Utiliser PowerShell pour autoriser des applications spécifiques</span><span class="sxs-lookup"><span data-stu-id="47b2f-179">Use PowerShell to allow specific apps</span></span>

1. <span data-ttu-id="47b2f-180">Tapez **PowerShell dans** le menu Démarrer, cliquez avec le **bouton droit sur Windows PowerShell** puis **sélectionnez Exécuter en tant qu’administrateur**</span><span class="sxs-lookup"><span data-stu-id="47b2f-180">Type **PowerShell** in the Start menu, right-click **Windows PowerShell** and select **Run as administrator**</span></span>
2. <span data-ttu-id="47b2f-181">Entrez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="47b2f-181">Enter the following cmdlet:</span></span>

    ```PowerShell
    Add-MpPreference -ControlledFolderAccessAllowedApplications "<the app that should be allowed, including the path>"
    ```

    <span data-ttu-id="47b2f-182">Par exemple, pour ajouter le fichier exécutable *test.exe* situé dans le dossier *C:\apps,* l’cmdlet serait la suivante :</span><span class="sxs-lookup"><span data-stu-id="47b2f-182">For example, to add the executable *test.exe* located in the folder *C:\apps*, the cmdlet would be as follows:</span></span>

    ```PowerShell
    Add-MpPreference -ControlledFolderAccessAllowedApplications "c:\apps\test.exe"
    ```

   <span data-ttu-id="47b2f-183">Continuez à utiliser `Add-MpPreference -ControlledFolderAccessAllowedApplications` pour ajouter d’autres applications à la liste.</span><span class="sxs-lookup"><span data-stu-id="47b2f-183">Continue to use `Add-MpPreference -ControlledFolderAccessAllowedApplications` to add more apps to the list.</span></span> <span data-ttu-id="47b2f-184">Les applications ajoutées à l’aide de cette cmdlet s’affichent dans l’application Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="47b2f-184">Apps added using this cmdlet will appear in the Windows Security app.</span></span>

   :::image type="content" source="images/cfa-allow-app-ps.png" alt-text="Cmdlet PowerShell pour autoriser une application":::

> [!IMPORTANT]
> <span data-ttu-id="47b2f-186">Permet `Add-MpPreference` d’ajouter ou d’ajouter des applications à la liste.</span><span class="sxs-lookup"><span data-stu-id="47b2f-186">Use `Add-MpPreference` to append or add apps to the list.</span></span> <span data-ttu-id="47b2f-187">`Set-MpPreference`L’utilisation de la cmdlet va supprimer la liste existante.</span><span class="sxs-lookup"><span data-stu-id="47b2f-187">Using the `Set-MpPreference` cmdlet will overwrite the existing list.</span></span>

### <a name="use-mdm-csps-to-allow-specific-apps"></a><span data-ttu-id="47b2f-188">Utiliser des CSP de gestion des applications mobiles pour autoriser des applications spécifiques</span><span class="sxs-lookup"><span data-stu-id="47b2f-188">Use MDM CSPs to allow specific apps</span></span>

<span data-ttu-id="47b2f-189">Utilisez le fournisseur de services de configuration [./Vendor/MSFT/Policy/Config/Defender/GuardedFoldersAllowedApplications](/windows/client-management/mdm/policy-csp-defender#defender-guardedfoldersallowedapplications) (CSP) pour permettre aux applications d’apporter des modifications aux dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="47b2f-189">Use the [./Vendor/MSFT/Policy/Config/Defender/GuardedFoldersAllowedApplications](/windows/client-management/mdm/policy-csp-defender#defender-guardedfoldersallowedapplications) configuration service provider (CSP) to allow apps to make changes to protected folders.</span></span>

## <a name="allow-signed-executable-files-to-access-protected-folders"></a><span data-ttu-id="47b2f-190">Autoriser les fichiers exécutables signés à accéder aux dossiers protégés</span><span class="sxs-lookup"><span data-stu-id="47b2f-190">Allow signed executable files to access protected folders</span></span>

<span data-ttu-id="47b2f-191">Les indicateurs de certificat et de fichier Microsoft Defender pour point de terminaison peuvent autoriser les fichiers exécutables signés à accéder aux dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="47b2f-191">Microsoft Defender for Endpoint certificate and file indicators can allow signed executable files to access protected folders.</span></span> <span data-ttu-id="47b2f-192">Pour plus d’informations sur l’implémentation, voir [Créer des indicateurs basés sur des certificats.](indicator-certificates.md)</span><span class="sxs-lookup"><span data-stu-id="47b2f-192">For implementation details, see [Create indicators based on certificates](indicator-certificates.md).</span></span>

> [!Note]
> <span data-ttu-id="47b2f-193">Cela ne s’applique pas aux moteurs de script, y compris PowerShell</span><span class="sxs-lookup"><span data-stu-id="47b2f-193">This does no apply to scripting engines, including Powershell</span></span>

## <a name="customize-the-notification"></a><span data-ttu-id="47b2f-194">Personnaliser la notification</span><span class="sxs-lookup"><span data-stu-id="47b2f-194">Customize the notification</span></span>

<span data-ttu-id="47b2f-195">Pour plus d’informations sur la personnalisation de la notification lorsqu’une règle est déclenchée et bloque une application ou un fichier, voir Configurer les notifications d’alerte [dans Microsoft Defender pour le point de terminaison.](configure-email-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="47b2f-195">For more information about customizing the notification when a rule is triggered and blocks an app or file, see [Configure alert notifications in Microsoft Defender for Endpoint](configure-email-notifications.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="47b2f-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47b2f-196">See also</span></span>

- [<span data-ttu-id="47b2f-197">Protéger les dossiers importants avec un accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="47b2f-197">Protect important folders with controlled folder access</span></span>](controlled-folders.md)
- [<span data-ttu-id="47b2f-198">Activer l’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="47b2f-198">Enable controlled folder access</span></span>](enable-controlled-folders.md)
- [<span data-ttu-id="47b2f-199">Évaluer les règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="47b2f-199">Evaluate attack surface reduction rules</span></span>](evaluate-attack-surface-reduction.md)
