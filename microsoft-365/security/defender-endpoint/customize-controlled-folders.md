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
ms.date: 03/24/2021
ms.technology: mde
ms.topic: how-to
ms.openlocfilehash: 0962913df63e6837664cdb8ff79710d66e66977c
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51199906"
---
# <a name="customize-controlled-folder-access"></a><span data-ttu-id="88aa7-104">Personnaliser l’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="88aa7-104">Customize controlled folder access</span></span>

<span data-ttu-id="88aa7-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="88aa7-105">**Applies to:**</span></span>
- [<span data-ttu-id="88aa7-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="88aa7-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="88aa7-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="88aa7-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="88aa7-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="88aa7-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="88aa7-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="88aa7-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)


<span data-ttu-id="88aa7-110">L’accès contrôlé aux dossiers vous permet de protéger les données précieuses contre les applications malveillantes et les menaces, telles que les ransomware.</span><span class="sxs-lookup"><span data-stu-id="88aa7-110">Controlled folder access helps you protect valuable data from malicious apps and threats, such as ransomware.</span></span> <span data-ttu-id="88aa7-111">L’accès contrôlé aux dossiers est pris en charge sur les clients Windows Server 2019 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="88aa7-111">Controlled folder access is supported on Windows Server 2019 and Windows 10 clients.</span></span>

<span data-ttu-id="88aa7-112">Cet article explique comment personnaliser les fonctionnalités d’accès contrôlé aux dossiers et comprend les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="88aa7-112">This article describes how to customize controlled folder access capabilities, and includes the following sections:</span></span>

- [<span data-ttu-id="88aa7-113">Protéger des dossiers supplémentaires</span><span class="sxs-lookup"><span data-stu-id="88aa7-113">Protect additional folders</span></span>](#protect-additional-folders)
- [<span data-ttu-id="88aa7-114">Ajouter des applications qui doivent être autorisées à accéder aux dossiers protégés</span><span class="sxs-lookup"><span data-stu-id="88aa7-114">Add apps that should be allowed to access protected folders</span></span>](#allow-specific-apps-to-make-changes-to-controlled-folders)
- [<span data-ttu-id="88aa7-115">Autoriser les fichiers exécutables signés à accéder aux dossiers protégés</span><span class="sxs-lookup"><span data-stu-id="88aa7-115">Allow signed executable files to access protected folders</span></span>](#allow-signed-executable-files-to-access-protected-folders)
- [<span data-ttu-id="88aa7-116">Personnaliser la notification</span><span class="sxs-lookup"><span data-stu-id="88aa7-116">Customize the notification</span></span>](#customize-the-notification)

> [!IMPORTANT]
> <span data-ttu-id="88aa7-117">L’accès contrôlé aux dossiers surveille les applications pour les activités détectées comme malveillantes.</span><span class="sxs-lookup"><span data-stu-id="88aa7-117">Controlled folder access monitors apps for activities that are detected as malicious.</span></span> <span data-ttu-id="88aa7-118">Parfois, les applications légitimes ne peuvent pas apporter de modifications à vos fichiers.</span><span class="sxs-lookup"><span data-stu-id="88aa7-118">Sometimes, legitimate apps are blocked from making changes to your files.</span></span> <span data-ttu-id="88aa7-119">Si l’accès contrôlé aux dossiers a un impact sur la productivité de votre organisation, vous pouvez envisager d’exécutez cette fonctionnalité en [mode audit](audit-windows-defender.md) pour en évaluer pleinement l’impact.</span><span class="sxs-lookup"><span data-stu-id="88aa7-119">If controlled folder access impacts your organization's productivity, you might consider running this feature in [audit mode](audit-windows-defender.md) to fully assess the impact.</span></span>

## <a name="protect-additional-folders"></a><span data-ttu-id="88aa7-120">Protéger des dossiers supplémentaires</span><span class="sxs-lookup"><span data-stu-id="88aa7-120">Protect additional folders</span></span>

<span data-ttu-id="88aa7-121">L’accès contrôlé aux dossiers s’applique à de nombreux dossiers système et emplacements par défaut, y compris les dossiers tels que **Documents,** **Images** et **Films.**</span><span class="sxs-lookup"><span data-stu-id="88aa7-121">Controlled folder access applies to many system folders and default locations, including folders such as **Documents**, **Pictures**, and **Movies**.</span></span> <span data-ttu-id="88aa7-122">Vous pouvez ajouter des dossiers supplémentaires à protéger, mais vous ne pouvez pas supprimer les dossiers par défaut dans la liste par défaut.</span><span class="sxs-lookup"><span data-stu-id="88aa7-122">You can add additional folders to be protected, but you cannot remove the default folders in the default list.</span></span>

<span data-ttu-id="88aa7-123">L’ajout d’autres dossiers à l’accès contrôlé aux dossiers peut être utile dans les cas où vous ne stockez pas de fichiers dans les bibliothèques Windows par défaut ou lorsque vous avez modifié l’emplacement par défaut de vos bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="88aa7-123">Adding other folders to controlled folder access can be helpful for cases when you don't store files in the default Windows libraries, or you've changed the default location of your libraries.</span></span>

<span data-ttu-id="88aa7-124">Vous pouvez également spécifier des partages réseau et des lecteurs mappés.</span><span class="sxs-lookup"><span data-stu-id="88aa7-124">You can also specify network shares and mapped drives.</span></span> <span data-ttu-id="88aa7-125">Les variables d’environnement et les caractères génériques sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="88aa7-125">Environment variables and wildcards are supported.</span></span> <span data-ttu-id="88aa7-126">Pour plus d’informations sur l’utilisation de caractères génériques, voir Utiliser des caractères génériques dans les listes d’exclusions de nom de fichier et de dossier ou [d’extension.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-extension-file-exclusions-microsoft-defender-antivirus#use-wildcards-in-the-file-name-and-folder-path-or-extension-exclusion-lists)</span><span class="sxs-lookup"><span data-stu-id="88aa7-126">For information about using wildcards, see [Use wildcards in the file name and folder path or extension exclusion lists](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-extension-file-exclusions-microsoft-defender-antivirus#use-wildcards-in-the-file-name-and-folder-path-or-extension-exclusion-lists).</span></span>

<span data-ttu-id="88aa7-127">Vous pouvez utiliser l’application de sécurité Windows, la stratégie de groupe, les cmdlets PowerShell ou les fournisseurs de services de configuration de gestion des appareils mobiles pour ajouter et supprimer des dossiers protégés supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="88aa7-127">You can use the Windows Security app, Group Policy, PowerShell cmdlets, or mobile device management configuration service providers to add and remove additional protected folders.</span></span>

### <a name="use-the-windows-security-app-to-protect-additional-folders"></a><span data-ttu-id="88aa7-128">Utiliser l’application Sécurité Windows pour protéger des dossiers supplémentaires</span><span class="sxs-lookup"><span data-stu-id="88aa7-128">Use the Windows Security app to protect additional folders</span></span>

1. <span data-ttu-id="88aa7-129">Ouvrez l’application Sécurité Windows en sélectionnant l’icône de bouclier dans la barre des tâches ou en recherchant sécurité dans le menu **Démarrer.**</span><span class="sxs-lookup"><span data-stu-id="88aa7-129">Open the Windows Security app by selecting the shield icon in the task bar or searching the start menu for **Security**.</span></span>

2. <span data-ttu-id="88aa7-130">Sélectionnez **Virus & protection contre les** menaces, puis faites défiler vers le bas jusqu’à la section Protection contre les **ransomware.**</span><span class="sxs-lookup"><span data-stu-id="88aa7-130">Select **Virus & threat protection**, and then scroll down to the **Ransomware protection** section.</span></span>

3. <span data-ttu-id="88aa7-131">Sélectionnez **Gérer la protection contre les ransomware** pour ouvrir le volet protection contre les **ransomware.**</span><span class="sxs-lookup"><span data-stu-id="88aa7-131">Select **Manage ransomware protection** to open the **Ransomware protection** pane.</span></span>

4. <span data-ttu-id="88aa7-132">Sous la section **Accès contrôlé aux dossiers,** sélectionnez **Dossiers protégés.**</span><span class="sxs-lookup"><span data-stu-id="88aa7-132">Under the **Controlled folder access** section, select **Protected folders**.</span></span>

5. <span data-ttu-id="88aa7-133">Sélectionnez **Oui** dans **l’invite contrôle d’accès** utilisateur.</span><span class="sxs-lookup"><span data-stu-id="88aa7-133">Choose **Yes** on the **User Access Control** prompt.</span></span> <span data-ttu-id="88aa7-134">Le **volet Dossiers protégés** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="88aa7-134">The **Protected folders** pane displays.</span></span>

4. <span data-ttu-id="88aa7-135">Sélectionnez **Ajouter un dossier protégé et** suivez les invites pour ajouter des dossiers.</span><span class="sxs-lookup"><span data-stu-id="88aa7-135">Select **Add a protected folder** and follow the prompts to add folders.</span></span>

### <a name="use-group-policy-to-protect-additional-folders"></a><span data-ttu-id="88aa7-136">Utiliser une stratégie de groupe pour protéger des dossiers supplémentaires</span><span class="sxs-lookup"><span data-stu-id="88aa7-136">Use Group Policy to protect additional folders</span></span>

1. <span data-ttu-id="88aa7-137">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)?preserve=true)de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="88aa7-137">On your Group Policy management computer, open the [Group Policy Management Console](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)?preserve=true), right-click the Group Policy Object you want to configure, and then and select **Edit**.</span></span>

2. <span data-ttu-id="88aa7-138">Dans **l’Éditeur de gestion des stratégies de** groupe, sélectionnez **Configuration** ordinateur et sélectionnez **Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="88aa7-138">In the **Group Policy Management Editor**, go to **Computer configuration** and select **Administrative templates**.</span></span>

3. <span data-ttu-id="88aa7-139">Développez l’arborescence **des composants Windows** de l’Antivirus  >  **Microsoft Defender**  >  **Windows Defender’accès contrôlé** aux  >  **dossiers** Exploit Guard.</span><span class="sxs-lookup"><span data-stu-id="88aa7-139">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Windows Defender Exploit Guard** > **Controlled folder access**.</span></span>

4. <span data-ttu-id="88aa7-140">Double-cliquez **sur Dossiers protégés configurés** et définissez l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="88aa7-140">Double-click **Configured protected folders** and set the option to **Enabled**.</span></span> <span data-ttu-id="88aa7-141">Sélectionnez **Afficher** et entrez chaque dossier.</span><span class="sxs-lookup"><span data-stu-id="88aa7-141">Select **Show** and enter each folder.</span></span>

### <a name="use-powershell-to-protect-additional-folders"></a><span data-ttu-id="88aa7-142">Utiliser PowerShell pour protéger des dossiers supplémentaires</span><span class="sxs-lookup"><span data-stu-id="88aa7-142">Use PowerShell to protect additional folders</span></span>

1. <span data-ttu-id="88aa7-143">Tapez **PowerShell dans** le menu Démarrer, cliquez avec le **bouton droit sur Windows PowerShell** puis **sélectionnez Exécuter en tant qu’administrateur**</span><span class="sxs-lookup"><span data-stu-id="88aa7-143">Type **PowerShell** in the Start menu, right-click **Windows PowerShell** and select **Run as administrator**</span></span>

2. <span data-ttu-id="88aa7-144">Entrez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="88aa7-144">Enter the following cmdlet:</span></span>

    ```PowerShell
    Add-MpPreference -ControlledFolderAccessProtectedFolders "<the folder to be protected>"
    ```
3. <span data-ttu-id="88aa7-145">Répétez l’étape 2 jusqu’à ce que vous ajoutiez tous les dossiers que vous souhaitez protéger.</span><span class="sxs-lookup"><span data-stu-id="88aa7-145">Repeat step 2 until you have added all the folders you want to protect.</span></span> <span data-ttu-id="88aa7-146">Les dossiers ajoutés sont visibles dans l’application Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="88aa7-146">Folders that are added are visible in the Windows Security app.</span></span>

   ![Capture d’écran d’une fenêtre PowerShell avec l’cmdlet ci-dessus entrée](/microsoft-365/security/defender-endpoint/images/cfa-allow-folder-ps)

> [!IMPORTANT]
> <span data-ttu-id="88aa7-148">Permet `Add-MpPreference` d’ajouter ou d’ajouter des applications à la liste.</span><span class="sxs-lookup"><span data-stu-id="88aa7-148">Use `Add-MpPreference` to append or add apps to the list.</span></span> <span data-ttu-id="88aa7-149">`Set-MpPreference`L’utilisation de la cmdlet va supprimer la liste existante.</span><span class="sxs-lookup"><span data-stu-id="88aa7-149">Using the `Set-MpPreference` cmdlet will overwrite the existing list.</span></span>

### <a name="use-mdm-csps-to-protect-additional-folders"></a><span data-ttu-id="88aa7-150">Utiliser des CSP mdm pour protéger des dossiers supplémentaires</span><span class="sxs-lookup"><span data-stu-id="88aa7-150">Use MDM CSPs to protect additional folders</span></span>

<span data-ttu-id="88aa7-151">Utilisez le fournisseur de services de configuration [./Vendor/MSFT/Policy/Config/Defender/GuardedFoldersList](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-defender#defender-guardedfolderslist) (CSP) pour permettre aux applications d’apporter des modifications aux dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="88aa7-151">Use the [./Vendor/MSFT/Policy/Config/Defender/GuardedFoldersList](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-defender#defender-guardedfolderslist) configuration service provider (CSP) to allow apps to make changes to protected folders.</span></span>

## <a name="allow-specific-apps-to-make-changes-to-controlled-folders"></a><span data-ttu-id="88aa7-152">Autoriser des applications spécifiques à apporter des modifications aux dossiers contrôlés</span><span class="sxs-lookup"><span data-stu-id="88aa7-152">Allow specific apps to make changes to controlled folders</span></span>

<span data-ttu-id="88aa7-153">Vous pouvez spécifier si certaines applications sont toujours considérées comme sécurisées et accorder un accès en écriture aux fichiers dans les dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="88aa7-153">You can specify if certain apps are always considered safe and give write access to files in protected folders.</span></span> <span data-ttu-id="88aa7-154">Autoriser les applications peut être utile si une application particulière que vous connaissez et que vous faites confiance est bloquée par la fonctionnalité d’accès contrôlé aux dossiers.</span><span class="sxs-lookup"><span data-stu-id="88aa7-154">Allowing apps can be useful if a particular app you know and trust is being blocked by the controlled folder access feature.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88aa7-155">Par défaut, Windows ajoute des applications qui sont considérées comme conviviales à la liste autorisée.</span><span class="sxs-lookup"><span data-stu-id="88aa7-155">By default, Windows adds apps that are considered friendly to the allowed list.</span></span> <span data-ttu-id="88aa7-156">Ces applications ajoutées automatiquement ne sont pas enregistrées dans la liste affichée dans l’application Sécurité Windows ou à l’aide des cmdlets PowerShell associées.</span><span class="sxs-lookup"><span data-stu-id="88aa7-156">Such apps that are added automatically are not recorded in the list shown in the Windows Security app or by using the associated PowerShell cmdlets.</span></span> <span data-ttu-id="88aa7-157">Il n’est pas nécessaire d’ajouter la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="88aa7-157">You shouldn't need to add most apps.</span></span> <span data-ttu-id="88aa7-158">Ajoutez uniquement des applications si elles sont bloquées et que vous pouvez vérifier leur fiabilité.</span><span class="sxs-lookup"><span data-stu-id="88aa7-158">Only add apps if they are being blocked and you can verify their trustworthiness.</span></span>

<span data-ttu-id="88aa7-159">Lorsque vous ajoutez une application, vous devez spécifier son emplacement.</span><span class="sxs-lookup"><span data-stu-id="88aa7-159">When you add an app, you have to specify the app's location.</span></span> <span data-ttu-id="88aa7-160">Seule l’application à cet emplacement sera autorisée à accéder aux dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="88aa7-160">Only the app in that location will be permitted access to the protected folders.</span></span> <span data-ttu-id="88aa7-161">Si l’application (du même nom) se trouve à un autre emplacement, elle n’est pas ajoutée à la liste d’applications et peut être bloquée par l’accès contrôlé aux dossiers.</span><span class="sxs-lookup"><span data-stu-id="88aa7-161">If the app (with the same name) is in a different location, it will not be added to the allow list and may be blocked by controlled folder access.</span></span>

<span data-ttu-id="88aa7-162">Une application ou un service autorisé dispose uniquement d’un accès en écriture à un dossier contrôlé après son démarrage.</span><span class="sxs-lookup"><span data-stu-id="88aa7-162">An allowed application or service only has write access to a controlled folder after it starts.</span></span> <span data-ttu-id="88aa7-163">Par exemple, un service de mise à jour continue de déclencher des événements une fois autorisé jusqu’à ce qu’il soit arrêté et redémarré.</span><span class="sxs-lookup"><span data-stu-id="88aa7-163">For example, an update service will continue to trigger events after it's allowed until it is stopped and restarted.</span></span>

### <a name="use-the-windows-defender-security-app-to-allow-specific-apps"></a><span data-ttu-id="88aa7-164">Utiliser l’application Windows Defender security pour autoriser des applications spécifiques</span><span class="sxs-lookup"><span data-stu-id="88aa7-164">Use the Windows Defender Security app to allow specific apps</span></span>

1. <span data-ttu-id="88aa7-165">Ouvrez l’application Sécurité Windows en recherchant sécurité dans le menu **Démarrer.**</span><span class="sxs-lookup"><span data-stu-id="88aa7-165">Open the Windows Security app by searching the start menu for **Security**.</span></span>

2. <span data-ttu-id="88aa7-166">Sélectionnez la **vignette & protection** contre les virus contre les menaces (ou l’icône de bouclier dans la barre de menus de gauche), puis sélectionnez Gérer la protection contre les **ransomware.**</span><span class="sxs-lookup"><span data-stu-id="88aa7-166">Select the **Virus & threat protection** tile (or the shield icon on the left menu bar) and then select **Manage ransomware protection**.</span></span>

3. <span data-ttu-id="88aa7-167">Sous la section **Accès contrôlé aux dossiers,** **sélectionnez Autoriser une application via Accès contrôlé aux dossiers**</span><span class="sxs-lookup"><span data-stu-id="88aa7-167">Under the **Controlled folder access** section, select **Allow an app through Controlled folder access**</span></span>

4. <span data-ttu-id="88aa7-168">Sélectionnez **Ajouter une application autorisée et** suivez les invites pour ajouter des applications.</span><span class="sxs-lookup"><span data-stu-id="88aa7-168">Select **Add an allowed app** and follow the prompts to add apps.</span></span>

   :::image type="content" source="images/cfa-allow-app.png" alt-text="Ajouter un bouton d’application autorisé":::

### <a name="use-group-policy-to-allow-specific-apps"></a><span data-ttu-id="88aa7-170">Utiliser une stratégie de groupe pour autoriser des applications spécifiques</span><span class="sxs-lookup"><span data-stu-id="88aa7-170">Use Group Policy to allow specific apps</span></span>

1. <span data-ttu-id="88aa7-171">Sur votre appareil de gestion des stratégies de groupe, ouvrez la [Console](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)?preserve=true)de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous souhaitez configurer et sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="88aa7-171">On your Group Policy management device, open the [Group Policy Management Console](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)?preserve=true), right-click the Group Policy Object you want to configure and select **Edit**.</span></span>

2. <span data-ttu-id="88aa7-172">Dans **l’Éditeur de gestion des stratégies de** groupe, sélectionnez **Configuration** ordinateur et sélectionnez **Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="88aa7-172">In the **Group Policy Management Editor**, go to **Computer configuration** and select **Administrative templates**.</span></span>

3. <span data-ttu-id="88aa7-173">Développez l’arborescence **des composants Windows** de l’Antivirus  >  **Microsoft Defender**  >  **Windows Defender’accès contrôlé** aux  >  **dossiers** Exploit Guard.</span><span class="sxs-lookup"><span data-stu-id="88aa7-173">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Windows Defender Exploit Guard** > **Controlled folder access**.</span></span>

4. <span data-ttu-id="88aa7-174">Double-cliquez sur le **paramètre Configurer les applications autorisées** et définissez l’option sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="88aa7-174">Double-click the **Configure allowed applications** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="88aa7-175">Sélectionnez **Afficher** et entrez chaque application.</span><span class="sxs-lookup"><span data-stu-id="88aa7-175">Select **Show** and enter each app.</span></span>

### <a name="use-powershell-to-allow-specific-apps"></a><span data-ttu-id="88aa7-176">Utiliser PowerShell pour autoriser des applications spécifiques</span><span class="sxs-lookup"><span data-stu-id="88aa7-176">Use PowerShell to allow specific apps</span></span>

1. <span data-ttu-id="88aa7-177">Tapez **PowerShell dans** le menu Démarrer, cliquez avec le **bouton droit sur Windows PowerShell** puis **sélectionnez Exécuter en tant qu’administrateur**</span><span class="sxs-lookup"><span data-stu-id="88aa7-177">Type **PowerShell** in the Start menu, right-click **Windows PowerShell** and select **Run as administrator**</span></span>
2. <span data-ttu-id="88aa7-178">Entrez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="88aa7-178">Enter the following cmdlet:</span></span>

    ```PowerShell
    Add-MpPreference -ControlledFolderAccessAllowedApplications "<the app that should be allowed, including the path>"
    ```

    <span data-ttu-id="88aa7-179">Par exemple, pour ajouter le fichier exécutable *test.exe* situé dans le dossier *C:\apps,* l’cmdlet serait la suivante :</span><span class="sxs-lookup"><span data-stu-id="88aa7-179">For example, to add the executable *test.exe* located in the folder *C:\apps*, the cmdlet would be as follows:</span></span>

    ```PowerShell
    Add-MpPreference -ControlledFolderAccessAllowedApplications "c:\apps\test.exe"
    ```

   <span data-ttu-id="88aa7-180">Continuez à utiliser `Add-MpPreference -ControlledFolderAccessAllowedApplications` pour ajouter d’autres applications à la liste.</span><span class="sxs-lookup"><span data-stu-id="88aa7-180">Continue to use `Add-MpPreference -ControlledFolderAccessAllowedApplications` to add more apps to the list.</span></span> <span data-ttu-id="88aa7-181">Les applications ajoutées à l’aide de cette cmdlet s’affichent dans l’application Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="88aa7-181">Apps added using this cmdlet will appear in the Windows Security app.</span></span>

   :::image type="content" source="images/cfa-allow-app-ps.png" alt-text="Cmdlet PowerShell pour autoriser une application":::

> [!IMPORTANT]
> <span data-ttu-id="88aa7-183">Permet `Add-MpPreference` d’ajouter ou d’ajouter des applications à la liste.</span><span class="sxs-lookup"><span data-stu-id="88aa7-183">Use `Add-MpPreference` to append or add apps to the list.</span></span> <span data-ttu-id="88aa7-184">`Set-MpPreference`L’utilisation de la cmdlet va supprimer la liste existante.</span><span class="sxs-lookup"><span data-stu-id="88aa7-184">Using the `Set-MpPreference` cmdlet will overwrite the existing list.</span></span>

### <a name="use-mdm-csps-to-allow-specific-apps"></a><span data-ttu-id="88aa7-185">Utiliser des CSP de gestion des applications mobiles pour autoriser des applications spécifiques</span><span class="sxs-lookup"><span data-stu-id="88aa7-185">Use MDM CSPs to allow specific apps</span></span>

<span data-ttu-id="88aa7-186">Utilisez le fournisseur de services de configuration [./Vendor/MSFT/Policy/Config/Defender/GuardedFoldersAllowedApplications](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-defender#defender-guardedfoldersallowedapplications) (CSP) pour permettre aux applications d’apporter des modifications aux dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="88aa7-186">Use the [./Vendor/MSFT/Policy/Config/Defender/GuardedFoldersAllowedApplications](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-defender#defender-guardedfoldersallowedapplications) configuration service provider (CSP) to allow apps to make changes to protected folders.</span></span>

## <a name="allow-signed-executable-files-to-access-protected-folders"></a><span data-ttu-id="88aa7-187">Autoriser les fichiers exécutables signés à accéder aux dossiers protégés</span><span class="sxs-lookup"><span data-stu-id="88aa7-187">Allow signed executable files to access protected folders</span></span>

<span data-ttu-id="88aa7-188">Les indicateurs de certificat et de fichier Microsoft Defender pour point de terminaison peuvent autoriser les fichiers exécutables signés à accéder aux dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="88aa7-188">Microsoft Defender for Endpoint certificate and file indicators can allow signed executable files to access protected folders.</span></span> <span data-ttu-id="88aa7-189">Pour plus d’informations sur l’implémentation, voir [Créer des indicateurs basés sur des certificats.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/indicator-certificates)</span><span class="sxs-lookup"><span data-stu-id="88aa7-189">For implementation details, see [Create indicators based on certificates](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/indicator-certificates).</span></span>

> [!Note]
> <span data-ttu-id="88aa7-190">Cela ne s’applique pas aux moteurs de script, y compris PowerShell</span><span class="sxs-lookup"><span data-stu-id="88aa7-190">This does no apply to scripting engines, including Powershell</span></span>

## <a name="customize-the-notification"></a><span data-ttu-id="88aa7-191">Personnaliser la notification</span><span class="sxs-lookup"><span data-stu-id="88aa7-191">Customize the notification</span></span>

<span data-ttu-id="88aa7-192">Pour plus d’informations sur la personnalisation de la notification lorsqu’une règle est déclenchée et bloque une application ou un fichier, voir Configurer les notifications d’alerte [dans Microsoft Defender pour le point de terminaison.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/configure-email-notifications)</span><span class="sxs-lookup"><span data-stu-id="88aa7-192">For more information about customizing the notification when a rule is triggered and blocks an app or file, see [Configure alert notifications in Microsoft Defender for Endpoint](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/configure-email-notifications).</span></span>

## <a name="see-also"></a><span data-ttu-id="88aa7-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88aa7-193">See also</span></span>

- [<span data-ttu-id="88aa7-194">Protéger les dossiers importants avec un accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="88aa7-194">Protect important folders with controlled folder access</span></span>](controlled-folders.md)
- [<span data-ttu-id="88aa7-195">Activer l’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="88aa7-195">Enable controlled folder access</span></span>](enable-controlled-folders.md)
- [<span data-ttu-id="88aa7-196">Évaluer les règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="88aa7-196">Evaluate attack surface reduction rules</span></span>](evaluate-attack-surface-reduction.md)
