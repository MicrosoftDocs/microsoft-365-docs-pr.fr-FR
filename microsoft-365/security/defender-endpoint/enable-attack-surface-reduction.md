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
author: denisebmsft
ms.author: deniseb
ms.reviewer: oogunrinde
manager: dansimp
ms.technology: mde
ms.topic: how-to
ms.date: 06/02/2021
ms.openlocfilehash: 65215d15e79ab03611bbf28c153d6882fd1c355d
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53229142"
---
# <a name="enable-attack-surface-reduction-rules"></a><span data-ttu-id="e808a-104">Activer les règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="e808a-104">Enable attack surface reduction rules</span></span>

<span data-ttu-id="e808a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e808a-105">**Applies to:**</span></span>

- [<span data-ttu-id="e808a-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e808a-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="e808a-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e808a-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> [!TIP]
> <span data-ttu-id="e808a-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="e808a-108">Want to experience Defender for Endpoint?</span></span> <span data-ttu-id="e808a-109">[Inscrivez-vous à une version d’essai gratuite.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)</span><span class="sxs-lookup"><span data-stu-id="e808a-109">[Sign up for a free trial](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink).</span></span>

<span data-ttu-id="e808a-110">[Les règles de réduction de la surface d’attaque](attack-surface-reduction.md) (règles de réduction de la surface d’attaque) permettent d’éviter les actions que les programmes malveillants abusent souvent pour compromettre les appareils et les réseaux.</span><span class="sxs-lookup"><span data-stu-id="e808a-110">[Attack surface reduction rules](attack-surface-reduction.md) (ASR rules) help prevent actions that malware often abuses to compromise devices and networks.</span></span>

## <a name="requirements"></a><span data-ttu-id="e808a-111">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="e808a-111">Requirements</span></span>

<span data-ttu-id="e808a-112">Fonctionnalités de réduction de la surface d’attaque Windows versions</span><span class="sxs-lookup"><span data-stu-id="e808a-112">Attack surface reduction features across Windows versions</span></span>

<span data-ttu-id="e808a-113">Vous pouvez définir des règles de réduction de la surface d’attaque pour les appareils qui exécutent l’une des éditions et versions suivantes de Windows :</span><span class="sxs-lookup"><span data-stu-id="e808a-113">You can set attack surface reduction rules for devices that are running any of the following editions and versions of Windows:</span></span>

- <span data-ttu-id="e808a-114">Windows 10 Professionnel, [version 1709 ou](/windows/whats-new/whats-new-windows-10-version-1709) ultérieure</span><span class="sxs-lookup"><span data-stu-id="e808a-114">Windows 10 Pro, [version 1709](/windows/whats-new/whats-new-windows-10-version-1709) or later</span></span>
- <span data-ttu-id="e808a-115">Windows 10 Entreprise, [version 1709 ou](/windows/whats-new/whats-new-windows-10-version-1709) ultérieure</span><span class="sxs-lookup"><span data-stu-id="e808a-115">Windows 10 Enterprise, [version 1709](/windows/whats-new/whats-new-windows-10-version-1709) or later</span></span>
- <span data-ttu-id="e808a-116">Windows Serveur, [version 1803 (canal semi-annuel)](/windows-server/get-started/whats-new-in-windows-server-1803) ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="e808a-116">Windows Server, [version 1803 (Semi-Annual Channel)](/windows-server/get-started/whats-new-in-windows-server-1803) or later</span></span>
- [<span data-ttu-id="e808a-117">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="e808a-117">Windows Server 2019</span></span>](/windows-server/get-started-19/whats-new-19)

<span data-ttu-id="e808a-118">Pour utiliser l’ensemble des fonctionnalités des règles de réduction de la surface d’attaque, vous devez :</span><span class="sxs-lookup"><span data-stu-id="e808a-118">To use the entire feature-set of attack surface reduction rules, you need:</span></span>

- <span data-ttu-id="e808a-119">Antivirus Windows Defender comme antivirus principal (protection en temps réel)</span><span class="sxs-lookup"><span data-stu-id="e808a-119">Windows Defender Antivirus as primary AV (real-time protection on)</span></span>
- <span data-ttu-id="e808a-120">[Protection de la distribution cloud](/windows/security/threat-protection/microsoft-defender-antivirus/enable-cloud-protection-microsoft-defender-antivirus) sur (certaines règles l’exigent)</span><span class="sxs-lookup"><span data-stu-id="e808a-120">[Cloud-Delivery Protection](/windows/security/threat-protection/microsoft-defender-antivirus/enable-cloud-protection-microsoft-defender-antivirus) on (some rules require that)</span></span>
- <span data-ttu-id="e808a-121">Windows 10 Entreprise Licence E5 ou E3 ou licence Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="e808a-121">Windows 10 Enterprise E5 or E3 License or Microsoft 365 Business License</span></span>

<span data-ttu-id="e808a-122">Bien que les règles de réduction de la surface d’attaque ne nécessitent pas de licence [Windows E5,](/windows/deployment/deploy-enterprise-licenses)avec une licence Windows E5, vous disposez de fonctionnalités de gestion avancées, y compris la surveillance, l’analyse et les flux de travail disponibles dans Defender pour Endpoint, ainsi que des fonctionnalités de rapports et de configuration dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e808a-122">Although attack surface reduction rules don't require a [Windows E5 license](/windows/deployment/deploy-enterprise-licenses), with a Windows E5 license, you get advanced management capabilities including monitoring, analytics, and workflows available in Defender for Endpoint, as well as reporting and configuration capabilities in the Microsoft 365 security center.</span></span> <span data-ttu-id="e808a-123">Ces fonctionnalités avancées ne sont pas disponibles avec une licence E3, mais vous pouvez toujours utiliser l’Observateur d’événements pour passer en revue les événements de règle de réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="e808a-123">These advanced capabilities aren't available with an E3 license, but you can still use Event Viewer to review attack surface reduction rule events.</span></span>

<span data-ttu-id="e808a-124">Chaque règle asr contient l’un des quatre paramètres ci-après :</span><span class="sxs-lookup"><span data-stu-id="e808a-124">Each ASR rule contains one of four settings:</span></span>

- <span data-ttu-id="e808a-125">**Non configuré :** désactiver la règle asr</span><span class="sxs-lookup"><span data-stu-id="e808a-125">**Not configured**: Disable the ASR rule</span></span>
- <span data-ttu-id="e808a-126">**Bloquer**: activer la règle asr</span><span class="sxs-lookup"><span data-stu-id="e808a-126">**Block**: Enable the ASR rule</span></span>
- <span data-ttu-id="e808a-127">**Audit**: évaluer l’impact de la règle asr sur votre organisation si elle est activée</span><span class="sxs-lookup"><span data-stu-id="e808a-127">**Audit**: Evaluate how the ASR rule would impact your organization if enabled</span></span>
- <span data-ttu-id="e808a-128">**Avertir :** activer la règle asr, mais autoriser l’utilisateur final à contourner le blocage</span><span class="sxs-lookup"><span data-stu-id="e808a-128">**Warn**: Enable the ASR rule but allow the end user to bypass the block</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e808a-129">Actuellement, le mode avertissement n’est pas pris en charge pour trois règles de récupération automatique lorsque vous configurez des règles asr dans Microsoft Endpoint Manager (MEM).</span><span class="sxs-lookup"><span data-stu-id="e808a-129">Currently, warn mode is not supported for three ASR rules when you configure ASR rules in Microsoft Endpoint Manager (MEM).</span></span> <span data-ttu-id="e808a-130">Pour en savoir plus, consultez [les cas où le mode d’avertissement n’est pas pris en charge.](attack-surface-reduction.md#cases-where-warn-mode-is-not-supported)</span><span class="sxs-lookup"><span data-stu-id="e808a-130">To learn more, see [Cases where warn mode is not supported](attack-surface-reduction.md#cases-where-warn-mode-is-not-supported).</span></span>

<span data-ttu-id="e808a-131">Il est vivement recommandé d’utiliser des règles asr avec une licence Windows E5 (ou une référence de licence similaire) pour tirer parti des fonctionnalités avancées de surveillance et de rapport disponibles dans [Microsoft Defender pour endpoint](microsoft-defender-endpoint.md) (Defender pour endpoint).</span><span class="sxs-lookup"><span data-stu-id="e808a-131">It's highly recommended to use ASR rules with a Windows E5 license (or similar licensing SKU) to take advantage of the advanced monitoring and reporting capabilities available in [Microsoft Defender for Endpoint](microsoft-defender-endpoint.md) (Defender for Endpoint).</span></span> <span data-ttu-id="e808a-132">Toutefois, si vous avez une autre licence, telle que Windows Professional ou Windows E3, qui n’inclut pas de fonctionnalités avancées de surveillance et de rapport, vous pouvez développer vos propres outils de surveillance et de rapport en plus des événements générés à chaque point de terminaison lorsque des règles de la asr sont déclenchées (par exemple, le forwarding d’événement).</span><span class="sxs-lookup"><span data-stu-id="e808a-132">However, if you have another license, such as Windows Professional or Windows E3 that don't include advanced monitoring and reporting capabilities, you can develop your own monitoring and reporting tools on top of the events that are generated at each endpoint when ASR rules are triggered (for example, Event Forwarding).</span></span>

> [!TIP]
> <span data-ttu-id="e808a-133">Pour en savoir plus sur Windows gestion des licences, voir Windows 10 [Licences](https://www.microsoft.com/licensing/product-licensing/windows10?activetab=windows10-pivot:primaryr5) en volume et obtenir le guide des licences en [volume pour Windows 10](https://download.microsoft.com/download/2/D/1/2D14FE17-66C2-4D4C-AF73-E122930B60F6/Windows-10-Volume-Licensing-Guide.pdf).</span><span class="sxs-lookup"><span data-stu-id="e808a-133">To learn more about Windows licensing, see [Windows 10 Licensing](https://www.microsoft.com/licensing/product-licensing/windows10?activetab=windows10-pivot:primaryr5) and get the [Volume Licensing guide for Windows 10](https://download.microsoft.com/download/2/D/1/2D14FE17-66C2-4D4C-AF73-E122930B60F6/Windows-10-Volume-Licensing-Guide.pdf).</span></span>

<span data-ttu-id="e808a-134">Vous pouvez activer les règles de réduction de la surface d’attaque à l’aide de l’une de ces méthodes :</span><span class="sxs-lookup"><span data-stu-id="e808a-134">You can enable attack surface reduction rules by using any of these methods:</span></span>

- [<span data-ttu-id="e808a-135">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="e808a-135">Microsoft Intune</span></span>](#intune)
- [<span data-ttu-id="e808a-136">Gestion des périphériques mobiles (MDM)</span><span class="sxs-lookup"><span data-stu-id="e808a-136">Mobile Device Management (MDM)</span></span>](#mdm)
- [<span data-ttu-id="e808a-137">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="e808a-137">Microsoft Endpoint Configuration Manager</span></span>](#microsoft-endpoint-configuration-manager)
- [<span data-ttu-id="e808a-138">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e808a-138">Group Policy</span></span>](#group-policy)
- [<span data-ttu-id="e808a-139">PowerShell</span><span class="sxs-lookup"><span data-stu-id="e808a-139">PowerShell</span></span>](#powershell)

<span data-ttu-id="e808a-140">Enterprise de niveau supérieur tel qu’Intune ou Microsoft Endpoint Manager est recommandée.</span><span class="sxs-lookup"><span data-stu-id="e808a-140">Enterprise-level management such as Intune or Microsoft Endpoint Manager is recommended.</span></span> <span data-ttu-id="e808a-141">Enterprise au niveau de l’entreprise est en train de réécrire les paramètres de stratégie de groupe ou PowerShell en conflit au démarrage.</span><span class="sxs-lookup"><span data-stu-id="e808a-141">Enterprise-level management will overwrite any conflicting Group Policy or PowerShell settings on startup.</span></span>

## <a name="exclude-files-and-folders-from-asr-rules"></a><span data-ttu-id="e808a-142">Exclure des fichiers et des dossiers des règles de la asr</span><span class="sxs-lookup"><span data-stu-id="e808a-142">Exclude files and folders from ASR rules</span></span>

<span data-ttu-id="e808a-143">Vous pouvez exclure les fichiers et dossiers de l’évaluation par la plupart des règles de réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="e808a-143">You can exclude files and folders from being evaluated by most attack surface reduction rules.</span></span> <span data-ttu-id="e808a-144">Cela signifie que même si une règle asr détermine que le fichier ou le dossier contient un comportement malveillant, il ne bloquera pas l’exécution du fichier.</span><span class="sxs-lookup"><span data-stu-id="e808a-144">This means that even if an ASR rule determines the file or folder contains malicious behavior, it will not block the file from running.</span></span> <span data-ttu-id="e808a-145">Cela peut potentiellement permettre à des fichiers non sécurisés de s’exécuter et d’infecter vos appareils.</span><span class="sxs-lookup"><span data-stu-id="e808a-145">This could potentially allow unsafe files to run and infect your devices.</span></span>

<span data-ttu-id="e808a-146">Vous pouvez également exclure les règles asr du déclenchement en fonction des hages de certificat et de fichier en permettant les indicateurs de certificat et de fichier Defender for Endpoint spécifiés.</span><span class="sxs-lookup"><span data-stu-id="e808a-146">You can also exclude ASR rules from triggering based on certificate and file hashes by allowing specified Defender for Endpoint file and certificate indicators.</span></span> <span data-ttu-id="e808a-147">(Voir [Gérer les indicateurs.)](manage-indicators.md)</span><span class="sxs-lookup"><span data-stu-id="e808a-147">(See [Manage indicators](manage-indicators.md).)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e808a-148">L’exclusion de fichiers ou de dossiers peut réduire considérablement la protection fournie par les règles de réduction de la réduction du nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="e808a-148">Excluding files or folders can severely reduce the protection provided by ASR rules.</span></span> <span data-ttu-id="e808a-149">Les fichiers exclus sont autorisés à s’exécuter et aucun rapport ou événement n’est enregistré.</span><span class="sxs-lookup"><span data-stu-id="e808a-149">Excluded files will be allowed to run, and no report or event will be recorded.</span></span>
> <span data-ttu-id="e808a-150">Si les règles de la récupération automatique des données détectent des fichiers qui, selon vous, ne devraient pas être détectés, vous devez d’abord utiliser le [mode audit pour tester la règle.](evaluate-attack-surface-reduction.md)</span><span class="sxs-lookup"><span data-stu-id="e808a-150">If ASR rules are detecting files that you believe shouldn't be detected, you should [use audit mode first to test the rule](evaluate-attack-surface-reduction.md).</span></span>

<span data-ttu-id="e808a-151">Vous pouvez spécifier des fichiers ou des dossiers individuels (à l’aide de chemins d’accès aux dossiers ou de noms de ressources complets), mais vous ne pouvez pas spécifier les règles à laquelle les exclusions s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="e808a-151">You can specify individual files or folders (using folder paths or fully qualified resource names), but you can't specify which rules the exclusions apply to.</span></span> <span data-ttu-id="e808a-152">Une exclusion est appliquée uniquement au démarrage de l’application ou du service exclu.</span><span class="sxs-lookup"><span data-stu-id="e808a-152">An exclusion is applied only when the excluded application or service starts.</span></span> <span data-ttu-id="e808a-153">Par exemple, si vous ajoutez une exclusion pour un service de mise à jour déjà en cours d’exécution, le service de mise à jour continue à déclencher des événements jusqu’à ce que le service soit arrêté et redémarré.</span><span class="sxs-lookup"><span data-stu-id="e808a-153">For example, if you add an exclusion for an update service that is already running, the update service will continue to trigger events until the service is stopped and restarted.</span></span>

<span data-ttu-id="e808a-154">Les règles de la asr prise en charge des variables d’environnement et des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="e808a-154">ASR rules support environment variables and wildcards.</span></span> <span data-ttu-id="e808a-155">Pour plus d’informations sur l’utilisation de caractères génériques, voir Utiliser des caractères génériques dans les listes d’exclusions de nom de fichier et de dossier ou [d’extension.](configure-extension-file-exclusions-microsoft-defender-antivirus.md#use-wildcards-in-the-file-name-and-folder-path-or-extension-exclusion-lists)</span><span class="sxs-lookup"><span data-stu-id="e808a-155">For information about using wildcards, see [Use wildcards in the file name and folder path or extension exclusion lists](configure-extension-file-exclusions-microsoft-defender-antivirus.md#use-wildcards-in-the-file-name-and-folder-path-or-extension-exclusion-lists).</span></span>

<span data-ttu-id="e808a-156">Les procédures suivantes pour l’activation des règles de la asr. contiennent des instructions pour exclure des fichiers et des dossiers.</span><span class="sxs-lookup"><span data-stu-id="e808a-156">The following procedures for enabling ASR rules include instructions for how to exclude files and folders.</span></span>

## <a name="intune"></a><span data-ttu-id="e808a-157">Intune</span><span class="sxs-lookup"><span data-stu-id="e808a-157">Intune</span></span>

1. <span data-ttu-id="e808a-158">Sélectionnez **Profils de configuration**  >  **d’appareil.**</span><span class="sxs-lookup"><span data-stu-id="e808a-158">Select **Device configuration** > **Profiles**.</span></span> <span data-ttu-id="e808a-159">Choisissez un profil de protection de point de terminaison existant ou créez-en un.</span><span class="sxs-lookup"><span data-stu-id="e808a-159">Choose an existing endpoint protection profile or create a new one.</span></span> <span data-ttu-id="e808a-160">Pour en créer un, sélectionnez Créer un **profil** et entrez des informations pour ce profil.</span><span class="sxs-lookup"><span data-stu-id="e808a-160">To create a new one, select **Create profile** and enter information for this profile.</span></span> <span data-ttu-id="e808a-161">Pour **le type de profil,** **sélectionnez Endpoint Protection**.</span><span class="sxs-lookup"><span data-stu-id="e808a-161">For **Profile type**, select **Endpoint protection**.</span></span> <span data-ttu-id="e808a-162">Si vous avez choisi un profil existant, sélectionnez **Propriétés,** puis **sélectionnez Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="e808a-162">If you've chosen an existing profile, select **Properties** and then select **Settings**.</span></span>

2. <span data-ttu-id="e808a-163">Dans le **volet de protection des points** de terminaison, **sélectionnez Windows Defender Exploit Guard,** puis sélectionnez **Réduction de la surface d’attaque.**</span><span class="sxs-lookup"><span data-stu-id="e808a-163">In the **Endpoint protection** pane, select **Windows Defender Exploit Guard**, then select **Attack Surface Reduction**.</span></span> <span data-ttu-id="e808a-164">Sélectionnez le paramètre souhaité pour chaque règle de asr.</span><span class="sxs-lookup"><span data-stu-id="e808a-164">Select the desired setting for each ASR rule.</span></span>

3. <span data-ttu-id="e808a-165">Sous **Exceptions de réduction de la surface d’attaque,** entrez des fichiers et dossiers individuels.</span><span class="sxs-lookup"><span data-stu-id="e808a-165">Under **Attack Surface Reduction exceptions**, enter individual files and folders.</span></span> <span data-ttu-id="e808a-166">Vous pouvez également sélectionner **Importer** pour importer un fichier CSV qui contient des fichiers et des dossiers à exclure des règles asr.</span><span class="sxs-lookup"><span data-stu-id="e808a-166">You can also select **Import** to import a CSV file that contains files and folders to exclude from ASR rules.</span></span> <span data-ttu-id="e808a-167">Chaque ligne du fichier CSV doit être mise en forme comme suit :</span><span class="sxs-lookup"><span data-stu-id="e808a-167">Each line in the CSV file should be formatted as follows:</span></span>

   <span data-ttu-id="e808a-168">`C:\folder`, `%ProgramFiles%\folder\file`, `C:\path`</span><span class="sxs-lookup"><span data-stu-id="e808a-168">`C:\folder`, `%ProgramFiles%\folder\file`, `C:\path`</span></span>

4. <span data-ttu-id="e808a-169">Sélectionnez **OK** dans les trois volets de configuration.</span><span class="sxs-lookup"><span data-stu-id="e808a-169">Select **OK** on the three configuration panes.</span></span> <span data-ttu-id="e808a-170">Sélectionnez **Ensuite Créer** si vous créez un fichier de protection de point de terminaison ou **Enregistrer** si vous modifiez un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="e808a-170">Then select **Create** if you're creating a new endpoint protection file or **Save** if you're editing an existing one.</span></span>

## <a name="mem"></a><span data-ttu-id="e808a-171">MEM</span><span class="sxs-lookup"><span data-stu-id="e808a-171">MEM</span></span>

<span data-ttu-id="e808a-172">Vous pouvez utiliser Microsoft Endpoint Manager OMA-URI (MEM) pour configurer des règles ASR personnalisées.</span><span class="sxs-lookup"><span data-stu-id="e808a-172">You can use Microsoft Endpoint Manager (MEM) OMA-URI to configure custom ASR rules.</span></span> <span data-ttu-id="e808a-173">La procédure suivante utilise la règle Bloquer l’abus des pilotes [signés vulnérables exploités](attack-surface-reduction.md#block-abuse-of-exploited-vulnerable-signed-drivers) pour l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e808a-173">The following procedure uses the rule [Block abuse of exploited vulnerable signed drivers](attack-surface-reduction.md#block-abuse-of-exploited-vulnerable-signed-drivers) for the example.</span></span>

1. <span data-ttu-id="e808a-174">Ouvrez le Microsoft Endpoint Manager d’administration de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e808a-174">Open the Microsoft Endpoint Manager (MEM) admin center.</span></span> <span data-ttu-id="e808a-175">Dans le menu **Accueil,** cliquez **sur Appareils,** sélectionnez **Profil de configuration,** puis cliquez **sur Créer un profil.**</span><span class="sxs-lookup"><span data-stu-id="e808a-175">In the **Home** menu, click  **Devices**, select **Configuration profile**, and then click **Create profile**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="e808a-176">![MEM Create Profile](images/mem01-create-profile.png)</span><span class="sxs-lookup"><span data-stu-id="e808a-176">![MEM Create Profile](images/mem01-create-profile.png)</span></span>

2. <span data-ttu-id="e808a-177">Dans **Créer un profil,** dans les deux listes de listes suivantes, sélectionnez les listes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e808a-177">In **Create a profile**, in the following two drop-down lists, select the following:</span></span>

   - <span data-ttu-id="e808a-178">Dans **Plateforme,** sélectionnez **Windows 10 et ultérieures**</span><span class="sxs-lookup"><span data-stu-id="e808a-178">In **Platform**, select **Windows 10 and later**</span></span>
   - <span data-ttu-id="e808a-179">Dans **le type de profil,** **sélectionnez Modèles**</span><span class="sxs-lookup"><span data-stu-id="e808a-179">In **Profile type**, select **Templates**</span></span>

   <span data-ttu-id="e808a-180">Sélectionnez **Personnalisé,** puis cliquez sur **Créer.**</span><span class="sxs-lookup"><span data-stu-id="e808a-180">Select **Custom**, and then click **Create**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="e808a-181">![Attributs de profil de règle MEM](images/mem02-profile-attributes.png)</span><span class="sxs-lookup"><span data-stu-id="e808a-181">![MEM rule profile attributes](images/mem02-profile-attributes.png)</span></span>

3. <span data-ttu-id="e808a-182">L’outil modèle personnalisé s’ouvre à **l’étape 1 Éléments de base.**</span><span class="sxs-lookup"><span data-stu-id="e808a-182">The Custom template tool opens to step **1 Basics**.</span></span> <span data-ttu-id="e808a-183">Dans **1 Informations de** base, dans **Nom,** tapez un nom pour votre modèle, et dans **Description,** vous pouvez taper une description (facultative).</span><span class="sxs-lookup"><span data-stu-id="e808a-183">In **1 Basics**, in **Name**, type a name for your template, and in **Description** you can type a description (optional).</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="e808a-184">![Attributs de base MEM](images/mem03-1-basics.png)</span><span class="sxs-lookup"><span data-stu-id="e808a-184">![MEM basic attributes](images/mem03-1-basics.png)</span></span>

4. <span data-ttu-id="e808a-185">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e808a-185">Click **Next**.</span></span> <span data-ttu-id="e808a-186">Les **paramètres de configuration de l’étape 2** s’ouvrent.</span><span class="sxs-lookup"><span data-stu-id="e808a-186">Step **2 Configuration settings** opens.</span></span> <span data-ttu-id="e808a-187">Pour les Paramètres OMA-URI, cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="e808a-187">For OMA-URI Settings, click **Add**.</span></span> <span data-ttu-id="e808a-188">Deux options s’affichent maintenant : **Ajouter** et **exporter.**</span><span class="sxs-lookup"><span data-stu-id="e808a-188">Two options now appear: **Add** and **Export**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="e808a-189">![Paramètres de configuration MEM](images/mem04-2-configuration-settings.png)</span><span class="sxs-lookup"><span data-stu-id="e808a-189">![MEM Configuration settings](images/mem04-2-configuration-settings.png)</span></span>

5. <span data-ttu-id="e808a-190">Cliquez **à nouveau sur** Ajouter.</span><span class="sxs-lookup"><span data-stu-id="e808a-190">Click **Add** again.</span></span> <span data-ttu-id="e808a-191">La **ligne Ajouter un OMA-URI Paramètres** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="e808a-191">The **Add Row OMA-URI Settings** opens.</span></span> <span data-ttu-id="e808a-192">Dans **Ajouter une ligne,** faites les choses suivantes :</span><span class="sxs-lookup"><span data-stu-id="e808a-192">In **Add Row**, do the following:</span></span>

   - <span data-ttu-id="e808a-193">Dans **Nom,** tapez un nom pour la règle.</span><span class="sxs-lookup"><span data-stu-id="e808a-193">In **Name**, type a name for the rule.</span></span>
   - <span data-ttu-id="e808a-194">Dans **Description,** tapez une brève description.</span><span class="sxs-lookup"><span data-stu-id="e808a-194">In **Description**, type a brief description.</span></span>
   - <span data-ttu-id="e808a-195">Dans **OMA-URI,** tapez ou collez le lien OMA-URI spécifique pour la règle que vous ajoutez.</span><span class="sxs-lookup"><span data-stu-id="e808a-195">In **OMA-URI**, type or paste the specific OMA-URI link for the rule that you are adding.</span></span>
   - <span data-ttu-id="e808a-196">Dans **type de données,** sélectionnez **Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="e808a-196">In **Data type**, select **String**.</span></span>
   - <span data-ttu-id="e808a-197">Dans **Value,** tapez ou collez la valeur GUID, le signe et la valeur State sans espace \= (_GUID=StateValue_).</span><span class="sxs-lookup"><span data-stu-id="e808a-197">In **Value**, type or paste the GUID value, the \= sign and the State value with no spaces (_GUID=StateValue_).</span></span> <span data-ttu-id="e808a-198">Where: {0 : Disable (Disable the ASR rule)}, {1 : Block (Enable the ASR rule)}, {2 : Audit (Evaluate how the ASR rule would impact your organization if enabled)}, {6 : Warn (Enable the ASR rule but allow the end-user to bypass the block)}</span><span class="sxs-lookup"><span data-stu-id="e808a-198">Where: {0 : Disable (Disable the ASR rule)}, {1 : Block (Enable the ASR rule)}, {2 : Audit (Evaluate how the ASR rule would impact your organization if enabled)}, {6 : Warn (Enable the ASR rule but allow the end-user to bypass the block)}</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="e808a-199">![Configuration OMA URI MEM](images/mem05-add-row-oma-uri.png)</span><span class="sxs-lookup"><span data-stu-id="e808a-199">![MEM OMA URI configuration](images/mem05-add-row-oma-uri.png)</span></span>

6. <span data-ttu-id="e808a-200">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e808a-200">Click **Save**.</span></span> <span data-ttu-id="e808a-201">**Ajouter des fermetures** de ligne.</span><span class="sxs-lookup"><span data-stu-id="e808a-201">**Add Row** closes.</span></span> <span data-ttu-id="e808a-202">Dans **Personnalisé,** cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e808a-202">In **Custom**, click **Next**.</span></span> <span data-ttu-id="e808a-203">À **l’étape 3, les balises d’étendue** sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="e808a-203">In step **3 Scope tags**, scope tags are optional.</span></span> <span data-ttu-id="e808a-204">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e808a-204">Do one of the following:</span></span>

   - <span data-ttu-id="e808a-205">Cliquez **sur Sélectionner des balises d’étendue,** sélectionnez la balise d’étendue (facultative), puis cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="e808a-205">Click **Select Scope tags**, select the scope tag (optional) and then click **Next**.</span></span>
   - <span data-ttu-id="e808a-206">Ou cliquez sur **Suivant**</span><span class="sxs-lookup"><span data-stu-id="e808a-206">Or click **Next**</span></span>

7. <span data-ttu-id="e808a-207">À **l’étape 4 Affectations,** dans **Groupes** inclus - pour les groupes que vous souhaitez que cette règle applique - sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="e808a-207">In step **4 Assignments**, in **Included Groups** - for the groups that you want this rule to apply - select from the following options:</span></span>

   - <span data-ttu-id="e808a-208">**Ajouter des groupes**</span><span class="sxs-lookup"><span data-stu-id="e808a-208">**Add groups**</span></span>
   - <span data-ttu-id="e808a-209">**Ajouter tous les utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="e808a-209">**Add all users**</span></span>
   - <span data-ttu-id="e808a-210">**Ajouter tous les appareils**</span><span class="sxs-lookup"><span data-stu-id="e808a-210">**Add all devices**</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="e808a-211">![Affectations MEM](images/mem06-4-assignments.png)</span><span class="sxs-lookup"><span data-stu-id="e808a-211">![MEM assignments](images/mem06-4-assignments.png)</span></span>

8. <span data-ttu-id="e808a-212">Dans **les groupes exclus,** sélectionnez les groupes que vous souhaitez exclure de cette règle, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e808a-212">In **Excluded groups**, select any groups that you want to exclude from this rule, and then click **Next**.</span></span>

9. <span data-ttu-id="e808a-213">À **l’étape 5, règles d’applicabilité** pour les paramètres suivants, appliquez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e808a-213">In step **5 Applicability Rules** for the following settings, do the following:</span></span>

   - <span data-ttu-id="e808a-214">Dans **la règle,** **sélectionnez Attribuer un profil si** ou **n’affectez pas de profil si**</span><span class="sxs-lookup"><span data-stu-id="e808a-214">In **Rule**, select either **Assign profile if**, or **Don’t assign profile if**</span></span>
   - <span data-ttu-id="e808a-215">In **Property**, select the property to which you want this rule to apply</span><span class="sxs-lookup"><span data-stu-id="e808a-215">In **Property**, select the property to which you want this rule to apply</span></span>
   - <span data-ttu-id="e808a-216">Dans **Valeur,** entrez la valeur applicable ou la plage de valeurs</span><span class="sxs-lookup"><span data-stu-id="e808a-216">In **Value**, enter the applicable value or value range</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="e808a-217">![Règles d’applicabilité MEM](images/mem07-5-applicability-rules.png)</span><span class="sxs-lookup"><span data-stu-id="e808a-217">![MEM Applicability rules](images/mem07-5-applicability-rules.png)</span></span>

10. <span data-ttu-id="e808a-218">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e808a-218">Click **Next**.</span></span> <span data-ttu-id="e808a-219">À **l’étape 6 Révision + création,** examinez les paramètres et les informations que vous avez sélectionnés et entrés, puis cliquez sur **Créer.**</span><span class="sxs-lookup"><span data-stu-id="e808a-219">In step **6 Review + create**, review the settings and information you have selected and entered, and then click **Create**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="e808a-220">![Révision et création de MEM](images/mem08-6-review-create.png)</span><span class="sxs-lookup"><span data-stu-id="e808a-220">![MEM Review and create](images/mem08-6-review-create.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="e808a-221">Les règles sont actives et actives en quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="e808a-221">Rules are active and live within minutes.</span></span>

>[!NOTE]
> <span data-ttu-id="e808a-222">Gestion des conflits :</span><span class="sxs-lookup"><span data-stu-id="e808a-222">Conflict handling:</span></span>
>
> <span data-ttu-id="e808a-223">Si vous affectez à un appareil deux stratégies DER différentes, la façon dont les conflits sont gérés est des règles qui sont affectées à différents états, il n’y a aucune gestion des conflits en place et le résultat est une erreur.</span><span class="sxs-lookup"><span data-stu-id="e808a-223">If you assign a device two different ASR policies, the way conflict is handled is rules that are assigned different states, there is no conflict management in place, and the result is an error.</span></span>
>
> <span data-ttu-id="e808a-224">Les règles non conflictuelles n’entraînent pas d’erreur et la règle est appliquée correctement.</span><span class="sxs-lookup"><span data-stu-id="e808a-224">Non-conflicting rules will not result in an error, and the rule will be applied correctly.</span></span> <span data-ttu-id="e808a-225">Résultat : la première règle est appliquée et les règles non conflictuelles suivantes sont fusionnées dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="e808a-225">The result is that the first rule is applied, and subsequent non-conflicting rules are merged into the policy.</span></span>

## <a name="mdm"></a><span data-ttu-id="e808a-226">MDM</span><span class="sxs-lookup"><span data-stu-id="e808a-226">MDM</span></span>

<span data-ttu-id="e808a-227">Utilisez le fournisseur de services de configuration [./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionRules](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules) (CSP) pour activer et définir individuellement le mode pour chaque règle.</span><span class="sxs-lookup"><span data-stu-id="e808a-227">Use the [./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionRules](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules) configuration service provider (CSP) to individually enable and set the mode for each rule.</span></span>

<span data-ttu-id="e808a-228">Voici un exemple de référence, à l’aide de [valeurs GUID pour les règles asr](attack-surface-reduction.md#attack-surface-reduction-rules).</span><span class="sxs-lookup"><span data-stu-id="e808a-228">The following is a sample for reference, using [GUID values for ASR rules](attack-surface-reduction.md#attack-surface-reduction-rules).</span></span>

`OMA-URI path: ./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionRules`

`Value: 75668C1F-73B5-4CF0-BB93-3ECF5CB7CC84=2|3B576869-A4EC-4529-8536-B80A7769E899=1|D4F940AB-401B-4EfC-AADC-AD5F3C50688A=2|D3E037E1-3EB8-44C8-A917-57927947596D=1|5BEB7EFE-FD9A-4556-801D-275E5FFC04CC=0|BE9BA2D9-53EA-4CDC-84E5-9B1EEEE46550=1`

<span data-ttu-id="e808a-229">Les valeurs à activer (bloquer), désactiver, avertir ou activer en mode audit sont :</span><span class="sxs-lookup"><span data-stu-id="e808a-229">The values to enable (Block), disable, warn, or enable in audit mode are:</span></span>

- <span data-ttu-id="e808a-230">0 : Désactiver (désactiver la règle asr)</span><span class="sxs-lookup"><span data-stu-id="e808a-230">0 : Disable (Disable the ASR rule)</span></span>
- <span data-ttu-id="e808a-231">1 : Bloquer (activer la règle asr)</span><span class="sxs-lookup"><span data-stu-id="e808a-231">1 : Block (Enable the ASR rule)</span></span>
- <span data-ttu-id="e808a-232">2 : Audit (évaluer l’impact de la règle asr sur votre organisation si elle est activée)</span><span class="sxs-lookup"><span data-stu-id="e808a-232">2 : Audit (Evaluate how the ASR rule would impact your organization if enabled)</span></span>
- <span data-ttu-id="e808a-233">6 : Avertir (activer la règle asr mais autoriser l’utilisateur final à contourner le bloc).</span><span class="sxs-lookup"><span data-stu-id="e808a-233">6 : Warn  (Enable the ASR rule but allow the end-user to bypass the block).</span></span> <span data-ttu-id="e808a-234">Le mode Avertissement est désormais disponible pour la plupart des règles de la asr.</span><span class="sxs-lookup"><span data-stu-id="e808a-234">Warn mode is now available for most of the ASR rules.</span></span>

<span data-ttu-id="e808a-235">Utilisez le fournisseur de services de configuration [./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionOnlyExclusions](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions) (CSP) pour ajouter des exclusions.</span><span class="sxs-lookup"><span data-stu-id="e808a-235">Use the [./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionOnlyExclusions](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions) configuration service provider (CSP) to add exclusions.</span></span>

<span data-ttu-id="e808a-236">Exemple :</span><span class="sxs-lookup"><span data-stu-id="e808a-236">Example:</span></span>

`OMA-URI path: ./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionOnlyExclusions`

`Value: c:\path|e:\path|c:\Exclusions.exe`

> [!NOTE]
> <span data-ttu-id="e808a-237">N’oubliez pas d’entrer des valeurs OMA-URI sans espaces.</span><span class="sxs-lookup"><span data-stu-id="e808a-237">Be sure to enter OMA-URI values without spaces.</span></span>

## <a name="microsoft-endpoint-configuration-manager"></a><span data-ttu-id="e808a-238">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="e808a-238">Microsoft Endpoint Configuration Manager</span></span>

1. <span data-ttu-id="e808a-239">In Microsoft Endpoint Configuration Manager, go to **Assets and Compliance**  >  **Endpoint Protection** Windows Defender  >  **Exploit Guard**.</span><span class="sxs-lookup"><span data-stu-id="e808a-239">In Microsoft Endpoint Configuration Manager, go to **Assets and Compliance** > **Endpoint Protection** > **Windows Defender Exploit Guard**.</span></span>

2. <span data-ttu-id="e808a-240">Sélectionnez **Home**  >  **Create Exploit Guard Policy**.</span><span class="sxs-lookup"><span data-stu-id="e808a-240">Select **Home** > **Create Exploit Guard Policy**.</span></span>

3. <span data-ttu-id="e808a-241">Entrez un nom et une description, sélectionnez **Réduction de la surface** d’attaque, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e808a-241">Enter a name and a description, select **Attack Surface Reduction**, and select **Next**.</span></span>

4. <span data-ttu-id="e808a-242">Choisissez les règles qui bloqueront ou auditeront les actions et sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="e808a-242">Choose which rules will block or audit actions and select **Next**.</span></span>

5. <span data-ttu-id="e808a-243">Examinez les paramètres et **sélectionnez Suivant** pour créer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="e808a-243">Review the settings and select **Next** to create the policy.</span></span>

6. <span data-ttu-id="e808a-244">Une fois la stratégie créée, **fermez**.</span><span class="sxs-lookup"><span data-stu-id="e808a-244">After the policy is created, **Close**.</span></span>

## <a name="group-policy"></a><span data-ttu-id="e808a-245">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e808a-245">Group Policy</span></span>

> [!WARNING]
> <span data-ttu-id="e808a-246">Si vous gérez vos ordinateurs et périphériques avec Intune, Configuration Manager ou toute autre plateforme de gestion au niveau de l’entreprise, le logiciel de gestion risque d’éviter les paramètres de stratégie de groupe en conflit au démarrage.</span><span class="sxs-lookup"><span data-stu-id="e808a-246">If you manage your computers and devices with Intune, Configuration Manager, or other enterprise-level management platform, the management software will overwrite any conflicting Group Policy settings on startup.</span></span>

1. <span data-ttu-id="e808a-247">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console de gestion des stratégies de groupe](https://technet.microsoft.com/library/cc731212.aspx), faites un clic droit sur l’objet de stratégie de groupe à configurer, puis sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="e808a-247">On your Group Policy management computer, open the [Group Policy Management Console](https://technet.microsoft.com/library/cc731212.aspx), right-click the Group Policy Object you want to configure and select **Edit**.</span></span>

2. <span data-ttu-id="e808a-248">Dans l’**Éditeur de gestion des stratégies de groupe**, accédez à **Configuration ordinateur**, puis sélectionnez **Modèles d’administration**.</span><span class="sxs-lookup"><span data-stu-id="e808a-248">In the **Group Policy Management Editor**, go to **Computer configuration** and select **Administrative templates**.</span></span>

3. <span data-ttu-id="e808a-249">Développez l’arborescence **Windows composants Antivirus Microsoft Defender**  >    >  Protection contre les attaques Microsoft Defender réduction de la surface  >  **d’attaque.**</span><span class="sxs-lookup"><span data-stu-id="e808a-249">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Microsoft Defender Exploit Guard** > **Attack surface reduction**.</span></span>

4. <span data-ttu-id="e808a-250">Sélectionnez **Configurer les règles de réduction de la surface d’attaque** et **sélectionnez Activé.**</span><span class="sxs-lookup"><span data-stu-id="e808a-250">Select **Configure Attack surface reduction rules** and select **Enabled**.</span></span> <span data-ttu-id="e808a-251">Vous pouvez ensuite définir l’état individuel de chaque règle dans la section Options.</span><span class="sxs-lookup"><span data-stu-id="e808a-251">You can then set the individual state for each rule in the options section.</span></span>

   <span data-ttu-id="e808a-252">Sélectionnez **Afficher...** et entrez l’ID de règle dans  la colonne Nom de la valeur et l’état choisi dans la colonne Valeur comme suit : </span><span class="sxs-lookup"><span data-stu-id="e808a-252">Select **Show...** and enter the rule ID in the **Value name** column and your chosen state in the **Value** column as follows:</span></span>

   - <span data-ttu-id="e808a-253">0 : Désactiver (désactiver la règle asr)</span><span class="sxs-lookup"><span data-stu-id="e808a-253">0 : Disable (Disable the ASR rule)</span></span>
   - <span data-ttu-id="e808a-254">1 : Bloquer (activer la règle asr)</span><span class="sxs-lookup"><span data-stu-id="e808a-254">1 : Block (Enable the ASR rule)</span></span>
   - <span data-ttu-id="e808a-255">2 : Audit (évaluer l’impact de la règle asr sur votre organisation si elle est activée)</span><span class="sxs-lookup"><span data-stu-id="e808a-255">2 : Audit (Evaluate how the ASR rule would impact your organization if enabled)</span></span>
   - <span data-ttu-id="e808a-256">6 : Avertir (activer la règle asr mais autoriser l’utilisateur final à contourner le blocage)</span><span class="sxs-lookup"><span data-stu-id="e808a-256">6 : Warn  (Enable the ASR rule but allow the end-user to bypass the block)</span></span>

   :::image type="content" source="images/asr-rules-gp.png" alt-text="Règles asr dans la stratégie de groupe":::

5. <span data-ttu-id="e808a-258">Pour exclure des fichiers et des dossiers des règles de réduction de la surface d’attaque, sélectionnez le paramètre Exclure les fichiers et les chemins d’accès des règles de réduction de la **surface** d’attaque et définissez l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="e808a-258">To exclude files and folders from ASR rules, select the **Exclude files and paths from Attack surface reduction rules** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="e808a-259">Sélectionnez **Afficher** et entrez chaque fichier ou dossier dans la **colonne Nom de la** valeur.</span><span class="sxs-lookup"><span data-stu-id="e808a-259">Select **Show** and enter each file or folder in the **Value name** column.</span></span> <span data-ttu-id="e808a-260">Entrez **0 dans** la colonne **Valeur** pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="e808a-260">Enter **0** in the **Value** column for each item.</span></span>

   > [!WARNING]
   > <span data-ttu-id="e808a-261">N’utilisez pas de guillemets, car ils ne sont pas pris en charge pour la colonne Nom de la valeur ou la **colonne** Valeur. </span><span class="sxs-lookup"><span data-stu-id="e808a-261">Do not use quotes as they are not supported for either the **Value name** column or the **Value** column.</span></span>

## <a name="powershell"></a><span data-ttu-id="e808a-262">PowerShell</span><span class="sxs-lookup"><span data-stu-id="e808a-262">PowerShell</span></span>

> [!WARNING]
> <span data-ttu-id="e808a-263">Si vous gérez vos ordinateurs et appareils avec Intune, Configuration Manager ou une autre plateforme de gestion au niveau de l’entreprise, le logiciel de gestion risque d’éviter les paramètres PowerShell en conflit au démarrage.</span><span class="sxs-lookup"><span data-stu-id="e808a-263">If you manage your computers and devices with Intune, Configuration Manager, or another enterprise-level management platform, the management software will overwrite any conflicting PowerShell settings on startup.</span></span> <span data-ttu-id="e808a-264">Pour permettre aux utilisateurs de définir la valeur à l’aide de PowerShell, utilisez l’option « Défini par l’utilisateur » pour la règle dans la plateforme de gestion.</span><span class="sxs-lookup"><span data-stu-id="e808a-264">To allow users to define the value using PowerShell, use the "User Defined" option for the rule in the management platform.</span></span>

1. <span data-ttu-id="e808a-265">Tapez **powershell** dans le menu Démarrer, cliquez avec le **bouton droit** sur Windows PowerShell puis **sélectionnez Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="e808a-265">Type **powershell** in the Start menu, right-click **Windows PowerShell** and select **Run as administrator**.</span></span>

2. <span data-ttu-id="e808a-266">Tapez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="e808a-266">Type the following cmdlet:</span></span>

    ```PowerShell
    Set-MpPreference -AttackSurfaceReductionRules_Ids <rule ID> -AttackSurfaceReductionRules_Actions Enabled
    ```

    <span data-ttu-id="e808a-267">Pour activer les règles asr en mode audit, utilisez la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="e808a-267">To enable ASR rules in audit mode, use the following cmdlet:</span></span>

    ```PowerShell
    Add-MpPreference -AttackSurfaceReductionRules_Ids <rule ID> -AttackSurfaceReductionRules_Actions AuditMode
    ```

    <span data-ttu-id="e808a-268">Pour activer les règles de la asr en mode d’avertissement, utilisez l';</span><span class="sxs-lookup"><span data-stu-id="e808a-268">To enable ASR rules in warn mode, use the following cmdlet:</span></span>

    ```PowerShell
    Add-MpPreference -AttackSurfaceReductionRules_Ids <rule ID> -AttackSurfaceReductionRules_Actions Warn
    ```

    <span data-ttu-id="e808a-269">Pour activer l’utilisation abusive des pilotes signés vulnérables exploités, utilisez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="e808a-269">To enable ASR Block abuse of exploited vulnerable signed drivers, use the following cmdlet:</span></span>

   ```PowerShell
   Add-MpPreference -AttackSurfaceReductionRules_Ids 56a863a9-875e-4185-98a7-b882c64b5ce5 -AttackSurfaceReductionRules_Actions Enabled
   ```

    <span data-ttu-id="e808a-270">Pour désactiver les règles de la asr, utilisez la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="e808a-270">To turn off ASR rules, use the following cmdlet:</span></span>

    ```PowerShell
    Add-MpPreference -AttackSurfaceReductionRules_Ids <rule ID> -AttackSurfaceReductionRules_Actions Disabled
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="e808a-271">Vous devez spécifier l’état individuellement pour chaque règle, mais vous pouvez combiner des règles et des états dans une liste séparée par des virgules.</span><span class="sxs-lookup"><span data-stu-id="e808a-271">You must specify the state individually for each rule, but you can combine rules and states in a comma-separated list.</span></span>
    >
    > <span data-ttu-id="e808a-272">Dans l’exemple suivant, les deux premières règles sont activées, la troisième est désactivée et la quatrième règle est activée en mode audit :</span><span class="sxs-lookup"><span data-stu-id="e808a-272">In the following example, the first two rules will be enabled, the third rule will be disabled, and the fourth rule will be enabled in audit mode:</span></span>
    >
    > ```PowerShell
    > Set-MpPreference -AttackSurfaceReductionRules_Ids <rule ID 1>,<rule ID 2>,<rule ID 3>,<rule ID 4> -AttackSurfaceReductionRules_Actions Enabled, Enabled, Disabled, AuditMode
    > ```

    <span data-ttu-id="e808a-273">Vous pouvez également utiliser le verbe `Add-MpPreference` PowerShell pour ajouter de nouvelles règles à la liste existante.</span><span class="sxs-lookup"><span data-stu-id="e808a-273">You can also use the `Add-MpPreference` PowerShell verb to add new rules to the existing list.</span></span>

    > [!WARNING]
    > <span data-ttu-id="e808a-274">`Set-MpPreference` est toujours en cours de réécriture de l’ensemble de règles existant.</span><span class="sxs-lookup"><span data-stu-id="e808a-274">`Set-MpPreference` will always overwrite the existing set of rules.</span></span> <span data-ttu-id="e808a-275">Si vous souhaitez l’ajouter à l’ensemble existant, `Add-MpPreference` utilisez-le à la place.</span><span class="sxs-lookup"><span data-stu-id="e808a-275">If you want to add to the existing set, use `Add-MpPreference` instead.</span></span>
    > <span data-ttu-id="e808a-276">Vous pouvez obtenir une liste de règles et leur état actuel à l’aide `Get-MpPreference` de .</span><span class="sxs-lookup"><span data-stu-id="e808a-276">You can obtain a list of rules and their current state by using `Get-MpPreference`.</span></span>

3. <span data-ttu-id="e808a-277">Pour exclure des fichiers et des dossiers des règles de la asr, utilisez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="e808a-277">To exclude files and folders from ASR rules, use the following cmdlet:</span></span>

    ```PowerShell
    Add-MpPreference -AttackSurfaceReductionOnlyExclusions "<fully qualified path or resource>"
    ```

    <span data-ttu-id="e808a-278">Continuez à `Add-MpPreference -AttackSurfaceReductionOnlyExclusions` l’utiliser pour ajouter d’autres fichiers et dossiers à la liste.</span><span class="sxs-lookup"><span data-stu-id="e808a-278">Continue to use `Add-MpPreference -AttackSurfaceReductionOnlyExclusions` to add more files and folders to the list.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="e808a-279">Permet `Add-MpPreference` d’ajouter ou d’ajouter des applications à la liste.</span><span class="sxs-lookup"><span data-stu-id="e808a-279">Use `Add-MpPreference` to append or add apps to the list.</span></span> <span data-ttu-id="e808a-280">`Set-MpPreference`L’utilisation de la cmdlet va supprimer la liste existante.</span><span class="sxs-lookup"><span data-stu-id="e808a-280">Using the `Set-MpPreference` cmdlet will overwrite the existing list.</span></span>

## <a name="related-articles"></a><span data-ttu-id="e808a-281">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="e808a-281">Related articles</span></span>

- [<span data-ttu-id="e808a-282">Réduire les surfaces d’attaque avec des règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="e808a-282">Reduce attack surfaces with attack surface reduction rules</span></span>](attack-surface-reduction.md)

- [<span data-ttu-id="e808a-283">Évaluer la réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="e808a-283">Evaluate attack surface reduction</span></span>](evaluate-attack-surface-reduction.md)

- [<span data-ttu-id="e808a-284">FAQ sur la réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="e808a-284">Attack surface reduction FAQ</span></span>](attack-surface-reduction.md)
