---
title: Activer les règles de réduction de la surface d’attaque
description: Activez les règles de réduction de la surface d’attaque (ASR) pour protéger vos appareils contre les attaques qui utilisent des macros, des scripts et des techniques d’injection courantes.
keywords: Réduction de la surface d’attaque, système de prévention des intrusions hôtes, règles de protection, anti-attaque, attaque, prévention des infections, activer, activer
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
ms.openlocfilehash: 84947057abbd456dee5cbf5d0c6fea37f679d9ad
ms.sourcegitcommit: 6e5c00f84b5201422aed094f2697016407df8fc2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51570947"
---
# <a name="enable-attack-surface-reduction-rules"></a><span data-ttu-id="36089-104">Activer les règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="36089-104">Enable attack surface reduction rules</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="36089-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="36089-105">**Applies to:**</span></span>
- [<span data-ttu-id="36089-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="36089-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="36089-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="36089-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="36089-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="36089-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="36089-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="36089-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="36089-110">[Les règles de réduction de la surface d’attaque](attack-surface-reduction.md) (règles de réduction de la surface d’attaque) permettent d’éviter les actions que les programmes malveillants abusent souvent pour compromettre les appareils et les réseaux.</span><span class="sxs-lookup"><span data-stu-id="36089-110">[Attack surface reduction rules](attack-surface-reduction.md) (ASR rules) help prevent actions that malware often abuses to compromise devices and networks.</span></span> <span data-ttu-id="36089-111">Vous pouvez définir des règles de asr pour les appareils exécutant l’une des éditions et versions suivantes de Windows :</span><span class="sxs-lookup"><span data-stu-id="36089-111">You can set ASR rules for devices running any of the following editions and versions of Windows:</span></span>
- <span data-ttu-id="36089-112">Windows 10 Professionnel, [version 1709 ou](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1709) ultérieure</span><span class="sxs-lookup"><span data-stu-id="36089-112">Windows 10 Pro, [version 1709](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1709) or later</span></span>
- <span data-ttu-id="36089-113">Windows 10 Entreprise, [version 1709 ou](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1709) ultérieure</span><span class="sxs-lookup"><span data-stu-id="36089-113">Windows 10 Enterprise, [version 1709](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1709) or later</span></span>
- <span data-ttu-id="36089-114">Windows Server, [version 1803 (canal semi-annuel)](https://docs.microsoft.com/windows-server/get-started/whats-new-in-windows-server-1803) ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="36089-114">Windows Server, [version 1803 (Semi-Annual Channel)](https://docs.microsoft.com/windows-server/get-started/whats-new-in-windows-server-1803) or later</span></span>
- [<span data-ttu-id="36089-115">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="36089-115">Windows Server 2019</span></span>](https://docs.microsoft.com/windows-server/get-started-19/whats-new-19)

<span data-ttu-id="36089-116">Chaque règle asr contient l’un des trois paramètres ci-après :</span><span class="sxs-lookup"><span data-stu-id="36089-116">Each ASR rule contains one of three settings:</span></span>

- <span data-ttu-id="36089-117">Non configuré : désactiver la règle asr</span><span class="sxs-lookup"><span data-stu-id="36089-117">Not configured: Disable the ASR rule</span></span>
- <span data-ttu-id="36089-118">Bloquer : activer la règle asr</span><span class="sxs-lookup"><span data-stu-id="36089-118">Block: Enable the ASR rule</span></span>
- <span data-ttu-id="36089-119">Audit : évaluer l’impact de la règle asr sur votre organisation si elle est activée</span><span class="sxs-lookup"><span data-stu-id="36089-119">Audit: Evaluate how the ASR rule would impact your organization if enabled</span></span>

<span data-ttu-id="36089-120">Il est vivement recommandé d’utiliser des règles asr avec une licence Windows E5 (ou une référence de licence similaire) pour tirer parti des fonctionnalités avancées de surveillance et de rapport disponibles dans [Microsoft Defender pour Endpoint](https://docs.microsoft.com/windows/security/threat-protection) (Defender pour Endpoint).</span><span class="sxs-lookup"><span data-stu-id="36089-120">It's highly recommended you use ASR rules with a Windows E5 license (or similar licensing SKU) to take advantage of the advanced monitoring and reporting capabilities available in [Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection) (Defender for Endpoint).</span></span> <span data-ttu-id="36089-121">Toutefois, pour d’autres licences telles que Windows Professionnel ou E3 qui n’ont pas accès aux fonctionnalités avancées de surveillance et de rapport, vous pouvez développer vos propres outils de surveillance et de rapport en plus des événements générés à chaque point de terminaison lorsque des règles de la asr. sont déclenchées (par exemple, le forwarding d’événement).</span><span class="sxs-lookup"><span data-stu-id="36089-121">However, for other licenses like Windows Professional or E3 that don't have access to advanced monitoring and reporting capabilities, you can develop your own monitoring and reporting tools on top of the events that are generated at each endpoint when ASR rules are triggered (e.g., Event Forwarding).</span></span>

> [!TIP]
> <span data-ttu-id="36089-122">Pour en savoir plus sur les licences Windows, voir [Licences Windows 10](https://www.microsoft.com/licensing/product-licensing/windows10?activetab=windows10-pivot:primaryr5) et obtenir le guide des licences en [volume pour Windows 10.](https://download.microsoft.com/download/2/D/1/2D14FE17-66C2-4D4C-AF73-E122930B60F6/Windows-10-Volume-Licensing-Guide.pdf)</span><span class="sxs-lookup"><span data-stu-id="36089-122">To learn more about Windows licensing, see [Windows 10 Licensing](https://www.microsoft.com/licensing/product-licensing/windows10?activetab=windows10-pivot:primaryr5) and get the [Volume Licensing guide for Windows 10](https://download.microsoft.com/download/2/D/1/2D14FE17-66C2-4D4C-AF73-E122930B60F6/Windows-10-Volume-Licensing-Guide.pdf).</span></span>

<span data-ttu-id="36089-123">Vous pouvez activer les règles de réduction de la surface d’attaque à l’aide de l’une de ces méthodes :</span><span class="sxs-lookup"><span data-stu-id="36089-123">You can enable attack surface reduction rules by using any of these methods:</span></span>

- [<span data-ttu-id="36089-124">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="36089-124">Microsoft Intune</span></span>](#intune)
- [<span data-ttu-id="36089-125">Gestion des périphériques mobiles (MDM)</span><span class="sxs-lookup"><span data-stu-id="36089-125">Mobile Device Management (MDM)</span></span>](#mdm)
- [<span data-ttu-id="36089-126">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="36089-126">Microsoft Endpoint Configuration Manager</span></span>](#microsoft-endpoint-configuration-manager)
- [<span data-ttu-id="36089-127">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="36089-127">Group Policy</span></span>](#group-policy)
- [<span data-ttu-id="36089-128">PowerShell</span><span class="sxs-lookup"><span data-stu-id="36089-128">PowerShell</span></span>](#powershell)

<span data-ttu-id="36089-129">La gestion au niveau de l’entreprise telle qu’Intune ou Microsoft Endpoint Manager est recommandée.</span><span class="sxs-lookup"><span data-stu-id="36089-129">Enterprise-level management such as Intune or Microsoft Endpoint Manager is recommended.</span></span> <span data-ttu-id="36089-130">La gestion au niveau de l’entreprise permet d’éviter tout conflit de stratégie de groupe ou de paramètres PowerShell au démarrage.</span><span class="sxs-lookup"><span data-stu-id="36089-130">Enterprise-level management will overwrite any conflicting Group Policy or PowerShell settings on startup.</span></span>

## <a name="exclude-files-and-folders-from-asr-rules"></a><span data-ttu-id="36089-131">Exclure des fichiers et des dossiers des règles de la asr</span><span class="sxs-lookup"><span data-stu-id="36089-131">Exclude files and folders from ASR rules</span></span>

<span data-ttu-id="36089-132">Vous pouvez exclure les fichiers et dossiers de l’évaluation par la plupart des règles de réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="36089-132">You can exclude files and folders from being evaluated by most attack surface reduction rules.</span></span> <span data-ttu-id="36089-133">Cela signifie que même si une règle asr détermine que le fichier ou le dossier contient un comportement malveillant, il ne bloquera pas l’exécution du fichier.</span><span class="sxs-lookup"><span data-stu-id="36089-133">This means that even if an ASR rule determines the file or folder contains malicious behavior, it will not block the file from running.</span></span> <span data-ttu-id="36089-134">Cela peut potentiellement permettre à des fichiers non sécurisés de s’exécuter et d’infecter vos appareils.</span><span class="sxs-lookup"><span data-stu-id="36089-134">This could potentially allow unsafe files to run and infect your devices.</span></span>

<span data-ttu-id="36089-135">Vous pouvez également exclure les règles asr du déclenchement en fonction des hages de certificat et de fichier en permettant les indicateurs de certificat et de fichier Defender for Endpoint spécifiés.</span><span class="sxs-lookup"><span data-stu-id="36089-135">You can also exclude ASR rules from triggering based on certificate and file hashes by allowing specified Defender for Endpoint file and certificate indicators.</span></span> <span data-ttu-id="36089-136">(Voir [Gérer les indicateurs.)](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/manage-indicators)</span><span class="sxs-lookup"><span data-stu-id="36089-136">(See [Manage indicators](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/manage-indicators).)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36089-137">L’exclusion de fichiers ou de dossiers peut réduire considérablement la protection fournie par les règles de réduction de la réduction du nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="36089-137">Excluding files or folders can severely reduce the protection provided by ASR rules.</span></span> <span data-ttu-id="36089-138">Les fichiers exclus sont autorisés à s’exécuter et aucun rapport ou événement n’est enregistré.</span><span class="sxs-lookup"><span data-stu-id="36089-138">Excluded files will be allowed to run, and no report or event will be recorded.</span></span>
> <span data-ttu-id="36089-139">Si les règles de la récupération automatique des données détectent des fichiers qui, selon vous, ne devraient pas être détectés, vous devez d’abord utiliser le [mode audit pour tester la règle.](evaluate-attack-surface-reduction.md)</span><span class="sxs-lookup"><span data-stu-id="36089-139">If ASR rules are detecting files that you believe shouldn't be detected, you should [use audit mode first to test the rule](evaluate-attack-surface-reduction.md).</span></span>


<span data-ttu-id="36089-140">Vous pouvez spécifier des fichiers ou des dossiers individuels (à l’aide de chemins d’accès aux dossiers ou de noms de ressources complets), mais vous ne pouvez pas spécifier les règles à laquelle les exclusions s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="36089-140">You can specify individual files or folders (using folder paths or fully qualified resource names), but you can't specify which rules the exclusions apply to.</span></span> <span data-ttu-id="36089-141">Une exclusion est appliquée uniquement au démarrage de l’application ou du service exclu.</span><span class="sxs-lookup"><span data-stu-id="36089-141">An exclusion is applied only when the excluded application or service starts.</span></span> <span data-ttu-id="36089-142">Par exemple, si vous ajoutez une exclusion pour un service de mise à jour déjà en cours d’exécution, le service de mise à jour continue à déclencher des événements jusqu’à ce que le service soit arrêté et redémarré.</span><span class="sxs-lookup"><span data-stu-id="36089-142">For example, if you add an exclusion for an update service that is already running, the update service will continue to trigger events until the service is stopped and restarted.</span></span>

<span data-ttu-id="36089-143">Les règles de la asr prise en charge des variables d’environnement et des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="36089-143">ASR rules support environment variables and wildcards.</span></span> <span data-ttu-id="36089-144">Pour plus d’informations sur l’utilisation de caractères génériques, voir Utiliser des caractères génériques dans les listes d’exclusions de nom de fichier et de dossier ou [d’extension.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-extension-file-exclusions-microsoft-defender-antivirus#use-wildcards-in-the-file-name-and-folder-path-or-extension-exclusion-lists)</span><span class="sxs-lookup"><span data-stu-id="36089-144">For information about using wildcards, see [Use wildcards in the file name and folder path or extension exclusion lists](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-extension-file-exclusions-microsoft-defender-antivirus#use-wildcards-in-the-file-name-and-folder-path-or-extension-exclusion-lists).</span></span>

<span data-ttu-id="36089-145">Les procédures suivantes pour l’activation des règles de la asr. contiennent des instructions pour exclure des fichiers et des dossiers.</span><span class="sxs-lookup"><span data-stu-id="36089-145">The following procedures for enabling ASR rules include instructions for how to exclude files and folders.</span></span>

## <a name="intune"></a><span data-ttu-id="36089-146">Intune</span><span class="sxs-lookup"><span data-stu-id="36089-146">Intune</span></span>

1. <span data-ttu-id="36089-147">Sélectionnez **Profils de configuration**  >  **d’appareil.**</span><span class="sxs-lookup"><span data-stu-id="36089-147">Select **Device configuration** > **Profiles**.</span></span> <span data-ttu-id="36089-148">Choisissez un profil de protection de point de terminaison existant ou créez-en un.</span><span class="sxs-lookup"><span data-stu-id="36089-148">Choose an existing endpoint protection profile or create a new one.</span></span> <span data-ttu-id="36089-149">Pour en créer un, sélectionnez Créer un **profil** et entrez des informations pour ce profil.</span><span class="sxs-lookup"><span data-stu-id="36089-149">To create a new one, select **Create profile** and enter information for this profile.</span></span> <span data-ttu-id="36089-150">Pour **le type de profil,** **sélectionnez Endpoint Protection**.</span><span class="sxs-lookup"><span data-stu-id="36089-150">For **Profile type**, select **Endpoint protection**.</span></span> <span data-ttu-id="36089-151">Si vous avez choisi un profil existant, sélectionnez **Propriétés,** puis **Paramètres.**</span><span class="sxs-lookup"><span data-stu-id="36089-151">If you've chosen an existing profile, select **Properties** and then select **Settings**.</span></span>

2. <span data-ttu-id="36089-152">Dans le **volet de protection des points** de terminaison, **sélectionnez Windows Defender Exploit Guard,** puis sélectionnez **Réduction de la surface d’attaque.**</span><span class="sxs-lookup"><span data-stu-id="36089-152">In the **Endpoint protection** pane, select **Windows Defender Exploit Guard**, then select **Attack Surface Reduction**.</span></span> <span data-ttu-id="36089-153">Sélectionnez le paramètre souhaité pour chaque règle de asr.</span><span class="sxs-lookup"><span data-stu-id="36089-153">Select the desired setting for each ASR rule.</span></span>

3. <span data-ttu-id="36089-154">Sous **Exceptions de réduction de la surface d’attaque,** entrez des fichiers et dossiers individuels.</span><span class="sxs-lookup"><span data-stu-id="36089-154">Under **Attack Surface Reduction exceptions**, enter individual files and folders.</span></span> <span data-ttu-id="36089-155">Vous pouvez également sélectionner **Importer** pour importer un fichier CSV qui contient des fichiers et des dossiers à exclure des règles asr.</span><span class="sxs-lookup"><span data-stu-id="36089-155">You can also select **Import** to import a CSV file that contains files and folders to exclude from ASR rules.</span></span> <span data-ttu-id="36089-156">Chaque ligne du fichier CSV doit être mise en forme comme suit :</span><span class="sxs-lookup"><span data-stu-id="36089-156">Each line in the CSV file should be formatted as follows:</span></span>

   <span data-ttu-id="36089-157">`C:\folder`, `%ProgramFiles%\folder\file`, `C:\path`</span><span class="sxs-lookup"><span data-stu-id="36089-157">`C:\folder`, `%ProgramFiles%\folder\file`, `C:\path`</span></span>

4. <span data-ttu-id="36089-158">Sélectionnez **OK** dans les trois volets de configuration.</span><span class="sxs-lookup"><span data-stu-id="36089-158">Select **OK** on the three configuration panes.</span></span> <span data-ttu-id="36089-159">Sélectionnez **Ensuite Créer** si vous créez un fichier de protection de point de terminaison ou **Enregistrer** si vous modifiez un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="36089-159">Then select **Create** if you're creating a new endpoint protection file or **Save** if you're editing an existing one.</span></span>

## <a name="mdm"></a><span data-ttu-id="36089-160">MDM</span><span class="sxs-lookup"><span data-stu-id="36089-160">MDM</span></span>

<span data-ttu-id="36089-161">Utilisez le fournisseur de services de configuration [./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionRules](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules) (CSP) pour activer et définir individuellement le mode pour chaque règle.</span><span class="sxs-lookup"><span data-stu-id="36089-161">Use the [./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionRules](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules) configuration service provider (CSP) to individually enable and set the mode for each rule.</span></span>

<span data-ttu-id="36089-162">Voici un exemple de référence, à l’aide de [valeurs GUID pour les règles asr](attack-surface-reduction.md#attack-surface-reduction-rules).</span><span class="sxs-lookup"><span data-stu-id="36089-162">The following is a sample for reference, using [GUID values for ASR rules](attack-surface-reduction.md#attack-surface-reduction-rules).</span></span>

`OMA-URI path: ./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionRules`

`Value: 75668C1F-73B5-4CF0-BB93-3ECF5CB7CC84=2|3B576869-A4EC-4529-8536-B80A7769E899=1|D4F940AB-401B-4EfC-AADC-AD5F3C50688A=2|D3E037E1-3EB8-44C8-A917-57927947596D=1|5BEB7EFE-FD9A-4556-801D-275E5FFC04CC=0|BE9BA2D9-53EA-4CDC-84E5-9B1EEEE46550=1`

<span data-ttu-id="36089-163">Les valeurs à activer, désactiver ou activer en mode audit sont :</span><span class="sxs-lookup"><span data-stu-id="36089-163">The values to enable, disable, or enable in audit mode are:</span></span>

- <span data-ttu-id="36089-164">Disable = 0</span><span class="sxs-lookup"><span data-stu-id="36089-164">Disable = 0</span></span>
- <span data-ttu-id="36089-165">Bloc (activer la règle asr) = 1</span><span class="sxs-lookup"><span data-stu-id="36089-165">Block (enable ASR rule) = 1</span></span>
- <span data-ttu-id="36089-166">Audit = 2</span><span class="sxs-lookup"><span data-stu-id="36089-166">Audit = 2</span></span>

<span data-ttu-id="36089-167">Utilisez le fournisseur de services de configuration [./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionOnlyExclusions](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions) (CSP) pour ajouter des exclusions.</span><span class="sxs-lookup"><span data-stu-id="36089-167">Use the [./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionOnlyExclusions](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions) configuration service provider (CSP) to add exclusions.</span></span>

<span data-ttu-id="36089-168">Exemple :</span><span class="sxs-lookup"><span data-stu-id="36089-168">Example:</span></span>

`OMA-URI path: ./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionOnlyExclusions`

`Value: c:\path|e:\path|c:\Exclusions.exe`

> [!NOTE]
> <span data-ttu-id="36089-169">N’oubliez pas d’entrer des valeurs OMA-URI sans espaces.</span><span class="sxs-lookup"><span data-stu-id="36089-169">Be sure to enter OMA-URI values without spaces.</span></span>

## <a name="microsoft-endpoint-configuration-manager"></a><span data-ttu-id="36089-170">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="36089-170">Microsoft Endpoint Configuration Manager</span></span>

1. <span data-ttu-id="36089-171">Dans Microsoft Endpoint Configuration Manager, sélectionnez **Assets and Compliance**  >  **Endpoint Protection** Windows Defender Exploit  >  **Guard**.</span><span class="sxs-lookup"><span data-stu-id="36089-171">In Microsoft Endpoint Configuration Manager, go to **Assets and Compliance** > **Endpoint Protection** > **Windows Defender Exploit Guard**.</span></span>

2. <span data-ttu-id="36089-172">Sélectionnez **Home**  >  **Create Exploit Guard Policy**.</span><span class="sxs-lookup"><span data-stu-id="36089-172">Select **Home** > **Create Exploit Guard Policy**.</span></span>

3. <span data-ttu-id="36089-173">Entrez un nom et une description, sélectionnez **Réduction de la surface** d’attaque, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="36089-173">Enter a name and a description, select **Attack Surface Reduction**, and select **Next**.</span></span>

4. <span data-ttu-id="36089-174">Choisissez les règles qui bloqueront ou auditeront les actions et sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="36089-174">Choose which rules will block or audit actions and select **Next**.</span></span>

5. <span data-ttu-id="36089-175">Examinez les paramètres et sélectionnez **Suivant** pour créer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="36089-175">Review the settings and select **Next** to create the policy.</span></span>

6. <span data-ttu-id="36089-176">Une fois la stratégie créée, **fermez**.</span><span class="sxs-lookup"><span data-stu-id="36089-176">After the policy is created, **Close**.</span></span>

## <a name="group-policy"></a><span data-ttu-id="36089-177">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="36089-177">Group Policy</span></span>

> [!WARNING]
> <span data-ttu-id="36089-178">Si vous gérez vos ordinateurs et périphériques avec Intune, Configuration Manager ou toute autre plateforme de gestion au niveau de l’entreprise, le logiciel de gestion risque d’éviter les paramètres de stratégie de groupe en conflit au démarrage.</span><span class="sxs-lookup"><span data-stu-id="36089-178">If you manage your computers and devices with Intune, Configuration Manager, or other enterprise-level management platform, the management software will overwrite any conflicting Group Policy settings on startup.</span></span>

1. <span data-ttu-id="36089-179">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](https://technet.microsoft.com/library/cc731212.aspx)de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous souhaitez configurer et sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="36089-179">On your Group Policy management computer, open the [Group Policy Management Console](https://technet.microsoft.com/library/cc731212.aspx), right-click the Group Policy Object you want to configure and select **Edit**.</span></span>

2. <span data-ttu-id="36089-180">Dans **l’Éditeur de gestion des stratégies de** groupe, sélectionnez **Configuration** ordinateur et sélectionnez **Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="36089-180">In the **Group Policy Management Editor**, go to **Computer configuration** and select **Administrative templates**.</span></span>

3. <span data-ttu-id="36089-181">Développez l’arborescence **des composants Windows** de la réduction de la surface d’attaque de  >  **l’Antivirus**  >  **Microsoft Defender Exploit Guard.**  >  </span><span class="sxs-lookup"><span data-stu-id="36089-181">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Microsoft Defender Exploit Guard** > **Attack surface reduction**.</span></span>

4. <span data-ttu-id="36089-182">Sélectionnez **Configurer les règles de réduction de la surface d’attaque** et **sélectionnez Activé.**</span><span class="sxs-lookup"><span data-stu-id="36089-182">Select **Configure Attack surface reduction rules** and select **Enabled**.</span></span> <span data-ttu-id="36089-183">Vous pouvez ensuite définir l’état individuel de chaque règle dans la section Options.</span><span class="sxs-lookup"><span data-stu-id="36089-183">You can then set the individual state for each rule in the options section.</span></span>

   <span data-ttu-id="36089-184">Sélectionnez **Afficher...** et entrez l’ID de règle dans  la colonne Nom de la valeur et l’état choisi dans la colonne Valeur comme suit : </span><span class="sxs-lookup"><span data-stu-id="36089-184">Select **Show...** and enter the rule ID in the **Value name** column and your chosen state in the **Value** column as follows:</span></span>

   - <span data-ttu-id="36089-185">Disable = 0</span><span class="sxs-lookup"><span data-stu-id="36089-185">Disable = 0</span></span>
   - <span data-ttu-id="36089-186">Bloc (activer la règle asr) = 1</span><span class="sxs-lookup"><span data-stu-id="36089-186">Block (enable ASR rule) = 1</span></span>
   - <span data-ttu-id="36089-187">Audit = 2</span><span class="sxs-lookup"><span data-stu-id="36089-187">Audit = 2</span></span>

   ![Paramètre de stratégie de groupe affichant un ID de règle de réduction de la surface d’attaque vide et la valeur 1](/microsoft-365/security/defender-endpoint/images/asr-rules-gp)

5. <span data-ttu-id="36089-189">Pour exclure des fichiers et des dossiers des règles de réduction de la surface d’attaque, sélectionnez le paramètre Exclure les fichiers et les chemins d’accès des règles de réduction de la **surface** d’attaque et définissez l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="36089-189">To exclude files and folders from ASR rules, select the **Exclude files and paths from Attack surface reduction rules** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="36089-190">Sélectionnez **Afficher** et entrez chaque fichier ou dossier dans la **colonne Nom de la** valeur.</span><span class="sxs-lookup"><span data-stu-id="36089-190">Select **Show** and enter each file or folder in the **Value name** column.</span></span> <span data-ttu-id="36089-191">Entrez **0 dans** la colonne **Valeur** pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="36089-191">Enter **0** in the **Value** column for each item.</span></span>

> [!WARNING]
> <span data-ttu-id="36089-192">N’utilisez pas de guillemets, car ils ne sont pas pris en charge pour la colonne Nom de la valeur ou la **colonne** Valeur. </span><span class="sxs-lookup"><span data-stu-id="36089-192">Do not use quotes as they are not supported for either the **Value name** column or the **Value** column.</span></span>

## <a name="powershell"></a><span data-ttu-id="36089-193">PowerShell</span><span class="sxs-lookup"><span data-stu-id="36089-193">PowerShell</span></span>

> [!WARNING]
> <span data-ttu-id="36089-194">Si vous gérez vos ordinateurs et appareils avec Intune, Configuration Manager ou une autre plateforme de gestion au niveau de l’entreprise, le logiciel de gestion risque d’éviter les paramètres PowerShell en conflit au démarrage.</span><span class="sxs-lookup"><span data-stu-id="36089-194">If you manage your computers and devices with Intune, Configuration Manager, or another enterprise-level management platform, the management software will overwrite any conflicting PowerShell settings on startup.</span></span> <span data-ttu-id="36089-195">Pour permettre aux utilisateurs de définir la valeur à l’aide de PowerShell, utilisez l’option « Défini par l’utilisateur » pour la règle dans la plateforme de gestion.</span><span class="sxs-lookup"><span data-stu-id="36089-195">To allow users to define the value using PowerShell, use the "User Defined" option for the rule in the management platform.</span></span>

1. <span data-ttu-id="36089-196">Tapez **powershell** dans le menu Démarrer, cliquez avec **le bouton droit sur Windows PowerShell** puis **sélectionnez Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="36089-196">Type **powershell** in the Start menu, right-click **Windows PowerShell** and select **Run as administrator**.</span></span>

2. <span data-ttu-id="36089-197">Entrez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="36089-197">Enter the following cmdlet:</span></span>

    ```PowerShell
    Set-MpPreference -AttackSurfaceReductionRules_Ids <rule ID> -AttackSurfaceReductionRules_Actions Enabled
    ```

    <span data-ttu-id="36089-198">Pour activer les règles asr en mode audit, utilisez la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="36089-198">To enable ASR rules in audit mode, use the following cmdlet:</span></span>

    ```PowerShell
    Add-MpPreference -AttackSurfaceReductionRules_Ids <rule ID> -AttackSurfaceReductionRules_Actions AuditMode
    ```

    <span data-ttu-id="36089-199">Pour désactiver les règles de la asr, utilisez la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="36089-199">To turn off ASR rules, use the following cmdlet:</span></span>

    ```PowerShell
    Add-MpPreference -AttackSurfaceReductionRules_Ids <rule ID> -AttackSurfaceReductionRules_Actions Disabled
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="36089-200">Vous devez spécifier l’état individuellement pour chaque règle, mais vous pouvez combiner des règles et des états dans une liste séparée par des virgules.</span><span class="sxs-lookup"><span data-stu-id="36089-200">You must specify the state individually for each rule, but you can combine rules and states in a comma-separated list.</span></span>
    >
    > <span data-ttu-id="36089-201">Dans l’exemple suivant, les deux premières règles sont activées, la troisième est désactivée et la quatrième règle est activée en mode audit :</span><span class="sxs-lookup"><span data-stu-id="36089-201">In the following example, the first two rules will be enabled, the third rule will be disabled, and the fourth rule will be enabled in audit mode:</span></span>
    >
    > ```PowerShell
    > Set-MpPreference -AttackSurfaceReductionRules_Ids <rule ID 1>,<rule ID 2>,<rule ID 3>,<rule ID 4> -AttackSurfaceReductionRules_Actions Enabled, Enabled, Disabled, AuditMode
    > ```

    <span data-ttu-id="36089-202">Vous pouvez également utiliser le verbe `Add-MpPreference` PowerShell pour ajouter de nouvelles règles à la liste existante.</span><span class="sxs-lookup"><span data-stu-id="36089-202">You can also use the `Add-MpPreference` PowerShell verb to add new rules to the existing list.</span></span>

    > [!WARNING]
    > <span data-ttu-id="36089-203">`Set-MpPreference` est toujours en cours de réécriture de l’ensemble de règles existant.</span><span class="sxs-lookup"><span data-stu-id="36089-203">`Set-MpPreference` will always overwrite the existing set of rules.</span></span> <span data-ttu-id="36089-204">Si vous souhaitez l’ajouter à l’ensemble existant, vous devez `Add-MpPreference` l’utiliser à la place.</span><span class="sxs-lookup"><span data-stu-id="36089-204">If you want to add to the existing set, you should use `Add-MpPreference` instead.</span></span>
    > <span data-ttu-id="36089-205">Vous pouvez obtenir une liste de règles et leur état actuel à l’aide `Get-MpPreference` de .</span><span class="sxs-lookup"><span data-stu-id="36089-205">You can obtain a list of rules and their current state by using `Get-MpPreference`.</span></span>

3. <span data-ttu-id="36089-206">Pour exclure des fichiers et des dossiers des règles de la asr, utilisez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="36089-206">To exclude files and folders from ASR rules, use the following cmdlet:</span></span>

    ```PowerShell
    Add-MpPreference -AttackSurfaceReductionOnlyExclusions "<fully qualified path or resource>"
    ```

    <span data-ttu-id="36089-207">Continuez à `Add-MpPreference -AttackSurfaceReductionOnlyExclusions` l’utiliser pour ajouter d’autres fichiers et dossiers à la liste.</span><span class="sxs-lookup"><span data-stu-id="36089-207">Continue to use `Add-MpPreference -AttackSurfaceReductionOnlyExclusions` to add more files and folders to the list.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="36089-208">Permet `Add-MpPreference` d’ajouter ou d’ajouter des applications à la liste.</span><span class="sxs-lookup"><span data-stu-id="36089-208">Use `Add-MpPreference` to append or add apps to the list.</span></span> <span data-ttu-id="36089-209">`Set-MpPreference`L’utilisation de la cmdlet va supprimer la liste existante.</span><span class="sxs-lookup"><span data-stu-id="36089-209">Using the `Set-MpPreference` cmdlet will overwrite the existing list.</span></span>

## <a name="related-articles"></a><span data-ttu-id="36089-210">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="36089-210">Related articles</span></span>

- [<span data-ttu-id="36089-211">Réduire les surfaces d’attaque avec des règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="36089-211">Reduce attack surfaces with attack surface reduction rules</span></span>](attack-surface-reduction.md)

- [<span data-ttu-id="36089-212">Évaluer la réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="36089-212">Evaluate attack surface reduction</span></span>](evaluate-attack-surface-reduction.md)

- <span data-ttu-id="36089-213">[FAQ sur la réduction de la surface d’attaque](attack-surface-reduction.md).</span><span class="sxs-lookup"><span data-stu-id="36089-213">[Attack surface reduction FAQ](attack-surface-reduction.md)</span></span>
