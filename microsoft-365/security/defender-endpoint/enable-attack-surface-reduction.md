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
ms.reviewer: oogunrinde
manager: dansimp
ms.technology: mde
ms.topic: how-to
ms.openlocfilehash: b3460e2c9b6073c518bea46147be69d4b89cd96a
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52538638"
---
# <a name="enable-attack-surface-reduction-rules"></a><span data-ttu-id="17da1-104">Activer les règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="17da1-104">Enable attack surface reduction rules</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="17da1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="17da1-105">**Applies to:**</span></span>

- [<span data-ttu-id="17da1-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="17da1-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="17da1-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="17da1-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> [!TIP]
> <span data-ttu-id="17da1-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="17da1-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="17da1-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="17da1-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="17da1-110">[Les règles de réduction de la surface d’attaque](attack-surface-reduction.md) (règles de réduction de la surface d’attaque) permettent d’éviter les actions que les programmes malveillants abusent souvent pour compromettre les appareils et les réseaux.</span><span class="sxs-lookup"><span data-stu-id="17da1-110">[Attack surface reduction rules](attack-surface-reduction.md) (ASR rules) help prevent actions that malware often abuses to compromise devices and networks.</span></span>

<span data-ttu-id="17da1-111">**Conditions requises** Vous pouvez définir des règles de réduction de la surface d’attaque pour les appareils qui exécutent l’une des éditions et versions suivantes de Windows :</span><span class="sxs-lookup"><span data-stu-id="17da1-111">**Requirements** You can set attack surface reduction rules for devices that are running any of the following editions and versions of Windows:</span></span>

- <span data-ttu-id="17da1-112">Windows 10 Professionnel, [version 1709 ou](/windows/whats-new/whats-new-windows-10-version-1709) ultérieure</span><span class="sxs-lookup"><span data-stu-id="17da1-112">Windows 10 Pro, [version 1709](/windows/whats-new/whats-new-windows-10-version-1709) or later</span></span>
- <span data-ttu-id="17da1-113">Windows 10 Entreprise, [version 1709 ou](/windows/whats-new/whats-new-windows-10-version-1709) ultérieure</span><span class="sxs-lookup"><span data-stu-id="17da1-113">Windows 10 Enterprise, [version 1709](/windows/whats-new/whats-new-windows-10-version-1709) or later</span></span>
- <span data-ttu-id="17da1-114">Windows Serveur, [version 1803 (canal semi-annuel)](/windows-server/get-started/whats-new-in-windows-server-1803) ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="17da1-114">Windows Server, [version 1803 (Semi-Annual Channel)](/windows-server/get-started/whats-new-in-windows-server-1803) or later</span></span>
- [<span data-ttu-id="17da1-115">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="17da1-115">Windows Server 2019</span></span>](/windows-server/get-started-19/whats-new-19)

<span data-ttu-id="17da1-116">Bien que les règles de réduction de la surface d’attaque ne nécessitent pas [Windows licence E5,](/windows/deployment/deploy-enterprise-licenses)si vous avez Windows E5, vous obtenez des fonctionnalités de gestion avancées.</span><span class="sxs-lookup"><span data-stu-id="17da1-116">Although attack surface reduction rules don't require a [Windows E5 license](/windows/deployment/deploy-enterprise-licenses), if you have Windows E5, you get advanced management capabilities.</span></span> <span data-ttu-id="17da1-117">Ces fonctionnalités disponibles uniquement dans Windows E5 incluent la surveillance, l’analyse et les flux de travail disponibles dans [Defender](/microsoft-365/security/defender-endpoint/microsoft-defender-endpoint?view=o365-worldwide&preserve-view=true)pour le point de terminaison, ainsi que les fonctionnalités de rapport et de configuration dans le centre de sécurité [Microsoft 365](/microsoft-365/security/defender/overview-security-center?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="17da1-117">These capabilities available only in Windows E5 include monitoring, analytics, and workflows available in [Defender for Endpoint](/microsoft-365/security/defender-endpoint/microsoft-defender-endpoint?view=o365-worldwide&preserve-view=true), as well as reporting and configuration capabilities in the [Microsoft 365 security center](/microsoft-365/security/defender/overview-security-center?view=o365-worldwide&preserve-view=true).</span></span> <span data-ttu-id="17da1-118">Ces fonctionnalités avancées ne sont pas disponibles avec une licence Windows Professional ou Windows E3 ; toutefois, si vous avez ces licences, vous pouvez utiliser l’Observateur d’événements et les journaux Antivirus Microsoft Defender pour passer en revue vos événements de règle de réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="17da1-118">These advanced capabilities aren't available with a Windows Professional or Windows E3 license; however, if you do have those licenses, you can use Event Viewer and Microsoft Defender Antivirus logs to review your attack surface reduction rule events.</span></span>

<span data-ttu-id="17da1-119">Chaque règle asr contient l’un des quatre paramètres ci-après :</span><span class="sxs-lookup"><span data-stu-id="17da1-119">Each ASR rule contains one of four settings:</span></span>

- <span data-ttu-id="17da1-120">**Non configuré :** désactiver la règle asr</span><span class="sxs-lookup"><span data-stu-id="17da1-120">**Not configured**: Disable the ASR rule</span></span>
- <span data-ttu-id="17da1-121">**Bloquer**: activer la règle asr</span><span class="sxs-lookup"><span data-stu-id="17da1-121">**Block**: Enable the ASR rule</span></span>
- <span data-ttu-id="17da1-122">**Audit**: évaluer l’impact de la règle asr sur votre organisation si elle est activée</span><span class="sxs-lookup"><span data-stu-id="17da1-122">**Audit**: Evaluate how the ASR rule would impact your organization if enabled</span></span>
- <span data-ttu-id="17da1-123">**Avertir :** activer la règle asr, mais autoriser l’utilisateur final à contourner le blocage</span><span class="sxs-lookup"><span data-stu-id="17da1-123">**Warn**: Enable the ASR rule but allow the end user to bypass the block</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17da1-124">Actuellement, le mode avertissement n’est pas pris en charge pour trois règles de récupération automatique lorsque vous configurez des règles asr dans Microsoft Endpoint Manager (MEM).</span><span class="sxs-lookup"><span data-stu-id="17da1-124">Currently, warn mode is not supported for three ASR rules when you configure ASR rules in Microsoft Endpoint Manager (MEM).</span></span> <span data-ttu-id="17da1-125">Pour en savoir plus, consultez [les cas où le mode d’avertissement n’est pas pris en charge.](attack-surface-reduction.md#cases-where-warn-mode-is-not-supported)</span><span class="sxs-lookup"><span data-stu-id="17da1-125">To learn more, see [Cases where warn mode is not supported](attack-surface-reduction.md#cases-where-warn-mode-is-not-supported).</span></span>

<span data-ttu-id="17da1-126">Il est vivement recommandé d’utiliser des règles asr avec une licence Windows E5 (ou une référence de licence similaire) pour tirer parti des fonctionnalités avancées de surveillance et de rapport disponibles dans [Microsoft Defender pour endpoint](https://docs.microsoft.com/windows/security/threat-protection) (Defender pour endpoint).</span><span class="sxs-lookup"><span data-stu-id="17da1-126">It's highly recommended you use ASR rules with a Windows E5 license (or similar licensing SKU) to take advantage of the advanced monitoring and reporting capabilities available in [Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection) (Defender for Endpoint).</span></span> <span data-ttu-id="17da1-127">Toutefois, pour d’autres licences telles que Windows Professional ou E3 qui n’ont pas accès aux fonctionnalités avancées de surveillance et de rapport, vous pouvez développer vos propres outils de surveillance et de rapport en plus des événements générés à chaque point de terminaison lorsque des règles de la assurance sont déclenchées (par exemple, le forwarding d’événement).</span><span class="sxs-lookup"><span data-stu-id="17da1-127">However, for other licenses like Windows Professional or E3 that don't have access to advanced monitoring and reporting capabilities, you can develop your own monitoring and reporting tools on top of the events that are generated at each endpoint when ASR rules are triggered (e.g., Event Forwarding).</span></span>

> [!TIP]
> <span data-ttu-id="17da1-128">Pour en savoir plus sur Windows gestion des licences, voir Windows 10 [Licences](https://www.microsoft.com/licensing/product-licensing/windows10?activetab=windows10-pivot:primaryr5) en volume et obtenir le guide des licences en [volume pour Windows 10](https://download.microsoft.com/download/2/D/1/2D14FE17-66C2-4D4C-AF73-E122930B60F6/Windows-10-Volume-Licensing-Guide.pdf).</span><span class="sxs-lookup"><span data-stu-id="17da1-128">To learn more about Windows licensing, see [Windows 10 Licensing](https://www.microsoft.com/licensing/product-licensing/windows10?activetab=windows10-pivot:primaryr5) and get the [Volume Licensing guide for Windows 10](https://download.microsoft.com/download/2/D/1/2D14FE17-66C2-4D4C-AF73-E122930B60F6/Windows-10-Volume-Licensing-Guide.pdf).</span></span>

<span data-ttu-id="17da1-129">Vous pouvez activer les règles de réduction de la surface d’attaque à l’aide de l’une de ces méthodes :</span><span class="sxs-lookup"><span data-stu-id="17da1-129">You can enable attack surface reduction rules by using any of these methods:</span></span>

- [<span data-ttu-id="17da1-130">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="17da1-130">Microsoft Intune</span></span>](#intune)
- [<span data-ttu-id="17da1-131">Gestion des périphériques mobiles (MDM)</span><span class="sxs-lookup"><span data-stu-id="17da1-131">Mobile Device Management (MDM)</span></span>](#mdm)
- [<span data-ttu-id="17da1-132">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="17da1-132">Microsoft Endpoint Configuration Manager</span></span>](#microsoft-endpoint-configuration-manager)
- [<span data-ttu-id="17da1-133">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="17da1-133">Group Policy</span></span>](#group-policy)
- [<span data-ttu-id="17da1-134">PowerShell</span><span class="sxs-lookup"><span data-stu-id="17da1-134">PowerShell</span></span>](#powershell)

<span data-ttu-id="17da1-135">Enterprise de niveau supérieur tel qu’Intune ou Microsoft Endpoint Manager est recommandée.</span><span class="sxs-lookup"><span data-stu-id="17da1-135">Enterprise-level management such as Intune or Microsoft Endpoint Manager is recommended.</span></span> <span data-ttu-id="17da1-136">Enterprise au niveau de l’entreprise est en train de réécrire les paramètres de stratégie de groupe ou PowerShell en conflit au démarrage.</span><span class="sxs-lookup"><span data-stu-id="17da1-136">Enterprise-level management will overwrite any conflicting Group Policy or PowerShell settings on startup.</span></span>

## <a name="exclude-files-and-folders-from-asr-rules"></a><span data-ttu-id="17da1-137">Exclure des fichiers et des dossiers des règles de la asr</span><span class="sxs-lookup"><span data-stu-id="17da1-137">Exclude files and folders from ASR rules</span></span>

<span data-ttu-id="17da1-138">Vous pouvez exclure les fichiers et dossiers de l’évaluation par la plupart des règles de réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="17da1-138">You can exclude files and folders from being evaluated by most attack surface reduction rules.</span></span> <span data-ttu-id="17da1-139">Cela signifie que même si une règle asr détermine que le fichier ou le dossier contient un comportement malveillant, il ne bloquera pas l’exécution du fichier.</span><span class="sxs-lookup"><span data-stu-id="17da1-139">This means that even if an ASR rule determines the file or folder contains malicious behavior, it will not block the file from running.</span></span> <span data-ttu-id="17da1-140">Cela peut potentiellement permettre à des fichiers non sécurisés de s’exécuter et d’infecter vos appareils.</span><span class="sxs-lookup"><span data-stu-id="17da1-140">This could potentially allow unsafe files to run and infect your devices.</span></span>

<span data-ttu-id="17da1-141">Vous pouvez également exclure les règles asr du déclenchement en fonction des hages de certificat et de fichier en permettant les indicateurs de certificat et de fichier Defender for Endpoint spécifiés.</span><span class="sxs-lookup"><span data-stu-id="17da1-141">You can also exclude ASR rules from triggering based on certificate and file hashes by allowing specified Defender for Endpoint file and certificate indicators.</span></span> <span data-ttu-id="17da1-142">(Voir [Gérer les indicateurs.)](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/manage-indicators)</span><span class="sxs-lookup"><span data-stu-id="17da1-142">(See [Manage indicators](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/manage-indicators).)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17da1-143">L’exclusion de fichiers ou de dossiers peut réduire considérablement la protection fournie par les règles de réduction de la réduction du nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="17da1-143">Excluding files or folders can severely reduce the protection provided by ASR rules.</span></span> <span data-ttu-id="17da1-144">Les fichiers exclus sont autorisés à s’exécuter et aucun rapport ou événement n’est enregistré.</span><span class="sxs-lookup"><span data-stu-id="17da1-144">Excluded files will be allowed to run, and no report or event will be recorded.</span></span>
> <span data-ttu-id="17da1-145">Si les règles de la récupération automatique des données détectent des fichiers qui, selon vous, ne devraient pas être détectés, vous devez d’abord utiliser le [mode audit pour tester la règle.](evaluate-attack-surface-reduction.md)</span><span class="sxs-lookup"><span data-stu-id="17da1-145">If ASR rules are detecting files that you believe shouldn't be detected, you should [use audit mode first to test the rule](evaluate-attack-surface-reduction.md).</span></span>

<span data-ttu-id="17da1-146">Vous pouvez spécifier des fichiers ou des dossiers individuels (à l’aide de chemins d’accès aux dossiers ou de noms de ressources complets), mais vous ne pouvez pas spécifier les règles à laquelle les exclusions s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="17da1-146">You can specify individual files or folders (using folder paths or fully qualified resource names), but you can't specify which rules the exclusions apply to.</span></span> <span data-ttu-id="17da1-147">Une exclusion est appliquée uniquement au démarrage de l’application ou du service exclu.</span><span class="sxs-lookup"><span data-stu-id="17da1-147">An exclusion is applied only when the excluded application or service starts.</span></span> <span data-ttu-id="17da1-148">Par exemple, si vous ajoutez une exclusion pour un service de mise à jour déjà en cours d’exécution, le service de mise à jour continue à déclencher des événements jusqu’à ce que le service soit arrêté et redémarré.</span><span class="sxs-lookup"><span data-stu-id="17da1-148">For example, if you add an exclusion for an update service that is already running, the update service will continue to trigger events until the service is stopped and restarted.</span></span>

<span data-ttu-id="17da1-149">Les règles de la asr prise en charge des variables d’environnement et des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="17da1-149">ASR rules support environment variables and wildcards.</span></span> <span data-ttu-id="17da1-150">Pour plus d’informations sur l’utilisation de caractères génériques, voir Utiliser des caractères génériques dans les listes d’exclusions de nom de fichier et de dossier ou [d’extension.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-extension-file-exclusions-microsoft-defender-antivirus#use-wildcards-in-the-file-name-and-folder-path-or-extension-exclusion-lists)</span><span class="sxs-lookup"><span data-stu-id="17da1-150">For information about using wildcards, see [Use wildcards in the file name and folder path or extension exclusion lists](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-extension-file-exclusions-microsoft-defender-antivirus#use-wildcards-in-the-file-name-and-folder-path-or-extension-exclusion-lists).</span></span>

<span data-ttu-id="17da1-151">Les procédures suivantes pour l’activation des règles de la asr. contiennent des instructions pour exclure des fichiers et des dossiers.</span><span class="sxs-lookup"><span data-stu-id="17da1-151">The following procedures for enabling ASR rules include instructions for how to exclude files and folders.</span></span>

## <a name="intune"></a><span data-ttu-id="17da1-152">Intune</span><span class="sxs-lookup"><span data-stu-id="17da1-152">Intune</span></span>

1. <span data-ttu-id="17da1-153">Sélectionnez **Profils de configuration**  >  **d’appareil.**</span><span class="sxs-lookup"><span data-stu-id="17da1-153">Select **Device configuration** > **Profiles**.</span></span> <span data-ttu-id="17da1-154">Choisissez un profil de protection de point de terminaison existant ou créez-en un.</span><span class="sxs-lookup"><span data-stu-id="17da1-154">Choose an existing endpoint protection profile or create a new one.</span></span> <span data-ttu-id="17da1-155">Pour en créer un, sélectionnez Créer un **profil** et entrez des informations pour ce profil.</span><span class="sxs-lookup"><span data-stu-id="17da1-155">To create a new one, select **Create profile** and enter information for this profile.</span></span> <span data-ttu-id="17da1-156">Pour **le type de profil,** **sélectionnez Endpoint Protection**.</span><span class="sxs-lookup"><span data-stu-id="17da1-156">For **Profile type**, select **Endpoint protection**.</span></span> <span data-ttu-id="17da1-157">Si vous avez choisi un profil existant, sélectionnez **Propriétés,** puis **sélectionnez Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="17da1-157">If you've chosen an existing profile, select **Properties** and then select **Settings**.</span></span>

2. <span data-ttu-id="17da1-158">Dans le **volet de protection des points** de terminaison, **sélectionnez Windows Defender Exploit Guard,** puis sélectionnez Réduction **de la surface d’attaque.**</span><span class="sxs-lookup"><span data-stu-id="17da1-158">In the **Endpoint protection** pane, select **Windows Defender Exploit Guard**, then select **Attack Surface Reduction**.</span></span> <span data-ttu-id="17da1-159">Sélectionnez le paramètre souhaité pour chaque règle de asr.</span><span class="sxs-lookup"><span data-stu-id="17da1-159">Select the desired setting for each ASR rule.</span></span>

3. <span data-ttu-id="17da1-160">Sous **Exceptions de réduction de la surface d’attaque,** entrez des fichiers et dossiers individuels.</span><span class="sxs-lookup"><span data-stu-id="17da1-160">Under **Attack Surface Reduction exceptions**, enter individual files and folders.</span></span> <span data-ttu-id="17da1-161">Vous pouvez également sélectionner **Importer** pour importer un fichier CSV qui contient des fichiers et des dossiers à exclure des règles asr.</span><span class="sxs-lookup"><span data-stu-id="17da1-161">You can also select **Import** to import a CSV file that contains files and folders to exclude from ASR rules.</span></span> <span data-ttu-id="17da1-162">Chaque ligne du fichier CSV doit être mise en forme comme suit :</span><span class="sxs-lookup"><span data-stu-id="17da1-162">Each line in the CSV file should be formatted as follows:</span></span>

   <span data-ttu-id="17da1-163">`C:\folder`, `%ProgramFiles%\folder\file`, `C:\path`</span><span class="sxs-lookup"><span data-stu-id="17da1-163">`C:\folder`, `%ProgramFiles%\folder\file`, `C:\path`</span></span>

4. <span data-ttu-id="17da1-164">Sélectionnez **OK** dans les trois volets de configuration.</span><span class="sxs-lookup"><span data-stu-id="17da1-164">Select **OK** on the three configuration panes.</span></span> <span data-ttu-id="17da1-165">Sélectionnez **Ensuite Créer** si vous créez un fichier de protection de point de terminaison ou **Enregistrer** si vous modifiez un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="17da1-165">Then select **Create** if you're creating a new endpoint protection file or **Save** if you're editing an existing one.</span></span>

## <a name="mem"></a><span data-ttu-id="17da1-166">MEM</span><span class="sxs-lookup"><span data-stu-id="17da1-166">MEM</span></span>

<span data-ttu-id="17da1-167">Vous pouvez utiliser Microsoft Endpoint Manager OMA-URI (MEM) pour configurer des règles ASR personnalisées.</span><span class="sxs-lookup"><span data-stu-id="17da1-167">You can use Microsoft Endpoint Manager (MEM) OMA-URI to configure custom ASR rules.</span></span> <span data-ttu-id="17da1-168">La procédure suivante utilise la règle Bloquer l’abus des pilotes [signés vulnérables exploités](attack-surface-reduction.md#block-abuse-of-exploited-vulnerable-signed-drivers) pour l’exemple.</span><span class="sxs-lookup"><span data-stu-id="17da1-168">The following procedure uses the rule [Block abuse of exploited vulnerable signed drivers](attack-surface-reduction.md#block-abuse-of-exploited-vulnerable-signed-drivers) for the example.</span></span>

1. <span data-ttu-id="17da1-169">Ouvrez le Microsoft Endpoint Manager d’administration de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="17da1-169">Open the Microsoft Endpoint Manager (MEM) admin center.</span></span> <span data-ttu-id="17da1-170">Dans le menu **Accueil,** cliquez **sur Appareils,** sélectionnez **Profil de configuration,** puis cliquez **sur Créer un profil.**</span><span class="sxs-lookup"><span data-stu-id="17da1-170">In the **Home** menu, click  **Devices**, select **Configuration profile**, and then click **Create profile**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="17da1-171">![MEM Create Profile](images/mem01-create-profile.png)</span><span class="sxs-lookup"><span data-stu-id="17da1-171">![MEM Create Profile](images/mem01-create-profile.png)</span></span>

2. <span data-ttu-id="17da1-172">Dans **Créer un profil,** dans les deux listes de listes suivantes, sélectionnez les listes suivantes :</span><span class="sxs-lookup"><span data-stu-id="17da1-172">In **Create a profile**, in the following two drop-down lists, select the following:</span></span>

   - <span data-ttu-id="17da1-173">Dans **Plateforme,** sélectionnez **Windows 10 et ultérieures**</span><span class="sxs-lookup"><span data-stu-id="17da1-173">In **Platform**, select **Windows 10 and later**</span></span>
   - <span data-ttu-id="17da1-174">Dans **le type de profil,** **sélectionnez Modèles**</span><span class="sxs-lookup"><span data-stu-id="17da1-174">In **Profile type**, select **Templates**</span></span>

   <span data-ttu-id="17da1-175">Sélectionnez **Personnalisé,** puis cliquez sur **Créer.**</span><span class="sxs-lookup"><span data-stu-id="17da1-175">Select **Custom**, and then click **Create**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="17da1-176">![Attributs de profil de règle MEM](images/mem02-profile-attributes.png)</span><span class="sxs-lookup"><span data-stu-id="17da1-176">![MEM rule profile attributes](images/mem02-profile-attributes.png)</span></span>

3. <span data-ttu-id="17da1-177">L’outil modèle personnalisé s’ouvre à **l’étape 1 Éléments de base.**</span><span class="sxs-lookup"><span data-stu-id="17da1-177">The Custom template tool opens to step **1 Basics**.</span></span> <span data-ttu-id="17da1-178">Dans **1 Informations de** base, dans **Nom,** tapez un nom pour votre modèle, et dans **Description,** vous pouvez taper une description (facultative).</span><span class="sxs-lookup"><span data-stu-id="17da1-178">In **1 Basics**, in **Name**, type a name for your template, and in **Description** you can type a description (optional).</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="17da1-179">![Attributs de base MEM](images/mem03-1-basics.png)</span><span class="sxs-lookup"><span data-stu-id="17da1-179">![MEM basic attributes](images/mem03-1-basics.png)</span></span>

4. <span data-ttu-id="17da1-180">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="17da1-180">Click **Next**.</span></span> <span data-ttu-id="17da1-181">Les **paramètres de configuration de l’étape 2** s’ouvrent.</span><span class="sxs-lookup"><span data-stu-id="17da1-181">Step **2 Configuration settings** opens.</span></span> <span data-ttu-id="17da1-182">Pour les Paramètres OMA-URI, cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="17da1-182">For OMA-URI Settings, click **Add**.</span></span> <span data-ttu-id="17da1-183">Deux options s’affichent maintenant : **Ajouter** et **exporter.**</span><span class="sxs-lookup"><span data-stu-id="17da1-183">Two options now appear: **Add** and **Export**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="17da1-184">![Paramètres de configuration MEM](images/mem04-2-configuration-settings.png)</span><span class="sxs-lookup"><span data-stu-id="17da1-184">![MEM Configuration settings](images/mem04-2-configuration-settings.png)</span></span>

5. <span data-ttu-id="17da1-185">Cliquez **à nouveau sur** Ajouter.</span><span class="sxs-lookup"><span data-stu-id="17da1-185">Click **Add** again.</span></span> <span data-ttu-id="17da1-186">La **ligne Ajouter un OMA-URI Paramètres** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="17da1-186">The **Add Row OMA-URI Settings** opens.</span></span> <span data-ttu-id="17da1-187">Dans **Ajouter une ligne,** faites les choses suivantes :</span><span class="sxs-lookup"><span data-stu-id="17da1-187">In **Add Row**, do the following:</span></span>

   - <span data-ttu-id="17da1-188">Dans **Nom,** tapez un nom pour la règle.</span><span class="sxs-lookup"><span data-stu-id="17da1-188">In **Name**, type a name for the rule.</span></span>
   - <span data-ttu-id="17da1-189">Dans **Description,** tapez une brève description.</span><span class="sxs-lookup"><span data-stu-id="17da1-189">In **Description**, type a brief description.</span></span>
   - <span data-ttu-id="17da1-190">Dans **OMA-URI,** tapez ou collez le lien OMA-URI spécifique pour la règle que vous ajoutez.</span><span class="sxs-lookup"><span data-stu-id="17da1-190">In **OMA-URI**, type or paste the specific OMA-URI link for the rule that you are adding.</span></span>
   - <span data-ttu-id="17da1-191">Dans **type de données,** sélectionnez **Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="17da1-191">In **Data type**, select **String**.</span></span>
   - <span data-ttu-id="17da1-192">Dans **Value,** tapez ou collez la valeur GUID, le signe et la valeur State sans espace \= (_GUID=StateValue_).</span><span class="sxs-lookup"><span data-stu-id="17da1-192">In **Value**, type or paste the GUID value, the \= sign and the State value with no spaces (_GUID=StateValue_).</span></span> <span data-ttu-id="17da1-193">Where: {0 : Disable (Disable the ASR rule)}, {1 : Block (Enable the ASR rule)}, {2 : Audit (Evaluate how the ASR rule would impact your organization if enabled)}, {6 : Warn (Enable the ASR rule but allow the end-user to bypass the block)}</span><span class="sxs-lookup"><span data-stu-id="17da1-193">Where: {0 : Disable (Disable the ASR rule)}, {1 : Block (Enable the ASR rule)}, {2 : Audit (Evaluate how the ASR rule would impact your organization if enabled)}, {6 : Warn (Enable the ASR rule but allow the end-user to bypass the block)}</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="17da1-194">![Configuration OMA URI MEM](images/mem05-add-row-oma-uri.png)</span><span class="sxs-lookup"><span data-stu-id="17da1-194">![MEM OMA URI configuration](images/mem05-add-row-oma-uri.png)</span></span>

6. <span data-ttu-id="17da1-195">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="17da1-195">Click **Save**.</span></span> <span data-ttu-id="17da1-196">**Ajouter des fermetures** de ligne.</span><span class="sxs-lookup"><span data-stu-id="17da1-196">**Add Row** closes.</span></span> <span data-ttu-id="17da1-197">Dans **Personnalisé,** cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="17da1-197">In **Custom**, click **Next**.</span></span> <span data-ttu-id="17da1-198">À **l’étape 3, les balises d’étendue** sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="17da1-198">In step **3 Scope tags**, scope tags are optional.</span></span> <span data-ttu-id="17da1-199">Effectuez l'une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="17da1-199">Do one of the following:</span></span>

   - <span data-ttu-id="17da1-200">Cliquez **sur Sélectionner des balises d’étendue,** sélectionnez la balise d’étendue (facultative), puis cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="17da1-200">Click **Select Scope tags**, select the scope tag (optional) and then click **Next**.</span></span>
   - <span data-ttu-id="17da1-201">Ou cliquez sur **Suivant**</span><span class="sxs-lookup"><span data-stu-id="17da1-201">Or click **Next**</span></span>

7. <span data-ttu-id="17da1-202">À **l’étape 4 Affectations,** dans **Groupes** inclus - pour les groupes que vous souhaitez que cette règle applique - sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="17da1-202">In step **4 Assignments**, in **Included Groups** - for the groups that you want this rule to apply - select from the following options:</span></span>

   - <span data-ttu-id="17da1-203">**Ajouter des groupes**</span><span class="sxs-lookup"><span data-stu-id="17da1-203">**Add groups**</span></span>
   - <span data-ttu-id="17da1-204">**Ajouter tous les utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="17da1-204">**Add all users**</span></span>
   - <span data-ttu-id="17da1-205">**Ajouter tous les appareils**</span><span class="sxs-lookup"><span data-stu-id="17da1-205">**Add all devices**</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="17da1-206">![Affectations MEM](images/mem06-4-assignments.png)</span><span class="sxs-lookup"><span data-stu-id="17da1-206">![MEM assignments](images/mem06-4-assignments.png)</span></span>

8. <span data-ttu-id="17da1-207">Dans **les groupes exclus,** sélectionnez les groupes que vous souhaitez exclure de cette règle, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="17da1-207">In **Excluded groups**, select any groups that you want to exclude from this rule, and then click **Next**.</span></span>

9. <span data-ttu-id="17da1-208">À **l’étape 5, règles d’applicabilité** pour les paramètres suivants, appliquez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="17da1-208">In step **5 Applicability Rules** for the following settings, do the following:</span></span>

   - <span data-ttu-id="17da1-209">Dans **la règle,** **sélectionnez Attribuer un profil si** ou **n’affectez pas de profil si**</span><span class="sxs-lookup"><span data-stu-id="17da1-209">In **Rule**, select either **Assign profile if**, or **Don’t assign profile if**</span></span>
   - <span data-ttu-id="17da1-210">In **Property**, select the property to which you want this rule to apply</span><span class="sxs-lookup"><span data-stu-id="17da1-210">In **Property**, select the property to which you want this rule to apply</span></span>
   - <span data-ttu-id="17da1-211">Dans **Valeur,** entrez la valeur applicable ou la plage de valeurs</span><span class="sxs-lookup"><span data-stu-id="17da1-211">In **Value**, enter the applicable value or value range</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="17da1-212">![Règles d’applicabilité MEM](images/mem07-5-applicability-rules.png)</span><span class="sxs-lookup"><span data-stu-id="17da1-212">![MEM Applicability rules](images/mem07-5-applicability-rules.png)</span></span>

10. <span data-ttu-id="17da1-213">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="17da1-213">Click **Next**.</span></span> <span data-ttu-id="17da1-214">À **l’étape 6 Révision + création,** examinez les paramètres et les informations que vous avez sélectionnés et entrés, puis cliquez sur **Créer.**</span><span class="sxs-lookup"><span data-stu-id="17da1-214">In step **6 Review + create**, review the settings and information you have selected and entered, and then click **Create**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="17da1-215">![Révision et création de MEM](images/mem08-6-review-create.png)</span><span class="sxs-lookup"><span data-stu-id="17da1-215">![MEM Review and create](images/mem08-6-review-create.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="17da1-216">Les règles sont actives et actives en quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="17da1-216">Rules are active and live within minutes.</span></span>

>[!NOTE]
> <span data-ttu-id="17da1-217">Gestion des conflits :</span><span class="sxs-lookup"><span data-stu-id="17da1-217">Conflict handling:</span></span>
> 
> <span data-ttu-id="17da1-218">Si vous affectez à un appareil deux stratégies DER différentes, la façon dont les conflits sont gérés est des règles qui sont affectées à différents états, il n’y a aucune gestion des conflits en place et le résultat est une erreur.</span><span class="sxs-lookup"><span data-stu-id="17da1-218">If you assign a device two different ASR policies, the way conflict is handled is rules that are assigned different states, there is no conflict management in place, and the result is an error.</span></span>
> 
> <span data-ttu-id="17da1-219">Les règles non conflictuelles n’entraînent pas d’erreur et la règle est appliquée correctement.</span><span class="sxs-lookup"><span data-stu-id="17da1-219">Non-conflicting rules will not result in an error, and the rule will be applied correctly.</span></span> <span data-ttu-id="17da1-220">Résultat : la première règle est appliquée et les règles non conflictuelles suivantes sont fusionnées dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="17da1-220">The result is that the first rule is applied, and subsequent non-conflicting rules are merged into the policy.</span></span>

## <a name="mdm"></a><span data-ttu-id="17da1-221">MDM</span><span class="sxs-lookup"><span data-stu-id="17da1-221">MDM</span></span>

<span data-ttu-id="17da1-222">Utilisez le fournisseur de services de configuration [./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionRules](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules) (CSP) pour activer et définir individuellement le mode pour chaque règle.</span><span class="sxs-lookup"><span data-stu-id="17da1-222">Use the [./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionRules](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules) configuration service provider (CSP) to individually enable and set the mode for each rule.</span></span>

<span data-ttu-id="17da1-223">Voici un exemple de référence, à l’aide de [valeurs GUID pour les règles asr](attack-surface-reduction.md#attack-surface-reduction-rules).</span><span class="sxs-lookup"><span data-stu-id="17da1-223">The following is a sample for reference, using [GUID values for ASR rules](attack-surface-reduction.md#attack-surface-reduction-rules).</span></span>

`OMA-URI path: ./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionRules`

`Value: 75668C1F-73B5-4CF0-BB93-3ECF5CB7CC84=2|3B576869-A4EC-4529-8536-B80A7769E899=1|D4F940AB-401B-4EfC-AADC-AD5F3C50688A=2|D3E037E1-3EB8-44C8-A917-57927947596D=1|5BEB7EFE-FD9A-4556-801D-275E5FFC04CC=0|BE9BA2D9-53EA-4CDC-84E5-9B1EEEE46550=1`

<span data-ttu-id="17da1-224">Les valeurs à activer (bloquer), désactiver, avertir ou activer en mode audit sont :</span><span class="sxs-lookup"><span data-stu-id="17da1-224">The values to enable (Block), disable, warn, or enable in audit mode are:</span></span>

- <span data-ttu-id="17da1-225">0 : Désactiver (désactiver la règle asr)</span><span class="sxs-lookup"><span data-stu-id="17da1-225">0 : Disable (Disable the ASR rule)</span></span>
- <span data-ttu-id="17da1-226">1 : Bloquer (activer la règle asr)</span><span class="sxs-lookup"><span data-stu-id="17da1-226">1 : Block (Enable the ASR rule)</span></span>
- <span data-ttu-id="17da1-227">2 : Audit (évaluer l’impact de la règle asr sur votre organisation si elle est activée)</span><span class="sxs-lookup"><span data-stu-id="17da1-227">2 : Audit (Evaluate how the ASR rule would impact your organization if enabled)</span></span>
- <span data-ttu-id="17da1-228">6 : Avertir (activer la règle asr mais autoriser l’utilisateur final à contourner le bloc).</span><span class="sxs-lookup"><span data-stu-id="17da1-228">6 : Warn  (Enable the ASR rule but allow the end-user to bypass the block).</span></span> <span data-ttu-id="17da1-229">Le mode Avertissement est désormais disponible pour la plupart des règles de la asr.</span><span class="sxs-lookup"><span data-stu-id="17da1-229">Warn mode is now available for most of the ASR rules.</span></span>

<span data-ttu-id="17da1-230">Utilisez le fournisseur de services de configuration [./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionOnlyExclusions](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions) (CSP) pour ajouter des exclusions.</span><span class="sxs-lookup"><span data-stu-id="17da1-230">Use the [./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionOnlyExclusions](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions) configuration service provider (CSP) to add exclusions.</span></span>

<span data-ttu-id="17da1-231">Exemple :</span><span class="sxs-lookup"><span data-stu-id="17da1-231">Example:</span></span>

`OMA-URI path: ./Vendor/MSFT/Policy/Config/Defender/AttackSurfaceReductionOnlyExclusions`

`Value: c:\path|e:\path|c:\Exclusions.exe`

> [!NOTE]
> <span data-ttu-id="17da1-232">N’oubliez pas d’entrer des valeurs OMA-URI sans espaces.</span><span class="sxs-lookup"><span data-stu-id="17da1-232">Be sure to enter OMA-URI values without spaces.</span></span>

## <a name="microsoft-endpoint-configuration-manager"></a><span data-ttu-id="17da1-233">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="17da1-233">Microsoft Endpoint Configuration Manager</span></span>

1. <span data-ttu-id="17da1-234">In Microsoft Endpoint Configuration Manager, go to **Assets and Compliance**  >  **Endpoint Protection** Windows Defender  >  **Exploit Guard**.</span><span class="sxs-lookup"><span data-stu-id="17da1-234">In Microsoft Endpoint Configuration Manager, go to **Assets and Compliance** > **Endpoint Protection** > **Windows Defender Exploit Guard**.</span></span>

2. <span data-ttu-id="17da1-235">Sélectionnez **Home**  >  **Create Exploit Guard Policy**.</span><span class="sxs-lookup"><span data-stu-id="17da1-235">Select **Home** > **Create Exploit Guard Policy**.</span></span>

3. <span data-ttu-id="17da1-236">Entrez un nom et une description, sélectionnez **Réduction de la surface** d’attaque, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="17da1-236">Enter a name and a description, select **Attack Surface Reduction**, and select **Next**.</span></span>

4. <span data-ttu-id="17da1-237">Choisissez les règles qui bloqueront ou auditeront les actions et sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="17da1-237">Choose which rules will block or audit actions and select **Next**.</span></span>

5. <span data-ttu-id="17da1-238">Examinez les paramètres et sélectionnez **Suivant** pour créer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="17da1-238">Review the settings and select **Next** to create the policy.</span></span>

6. <span data-ttu-id="17da1-239">Une fois la stratégie créée, **fermez**.</span><span class="sxs-lookup"><span data-stu-id="17da1-239">After the policy is created, **Close**.</span></span>

## <a name="group-policy"></a><span data-ttu-id="17da1-240">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="17da1-240">Group Policy</span></span>

> [!WARNING]
> <span data-ttu-id="17da1-241">Si vous gérez vos ordinateurs et périphériques avec Intune, Configuration Manager ou toute autre plateforme de gestion au niveau de l’entreprise, le logiciel de gestion risque d’éviter les paramètres de stratégie de groupe en conflit au démarrage.</span><span class="sxs-lookup"><span data-stu-id="17da1-241">If you manage your computers and devices with Intune, Configuration Manager, or other enterprise-level management platform, the management software will overwrite any conflicting Group Policy settings on startup.</span></span>

1. <span data-ttu-id="17da1-242">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console de gestion des stratégies de groupe](https://technet.microsoft.com/library/cc731212.aspx), faites un clic droit sur l’objet de stratégie de groupe à configurer, puis sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="17da1-242">On your Group Policy management computer, open the [Group Policy Management Console](https://technet.microsoft.com/library/cc731212.aspx), right-click the Group Policy Object you want to configure and select **Edit**.</span></span>

2. <span data-ttu-id="17da1-243">Dans l’**Éditeur de gestion des stratégies de groupe**, accédez à **Configuration ordinateur**, puis sélectionnez **Modèles d’administration**.</span><span class="sxs-lookup"><span data-stu-id="17da1-243">In the **Group Policy Management Editor**, go to **Computer configuration** and select **Administrative templates**.</span></span>

3. <span data-ttu-id="17da1-244">Développez l’arborescence **Windows composants Antivirus Microsoft Defender**  >    >  Protection contre les attaques Microsoft Defender réduction de la surface  >  **d’attaque.**</span><span class="sxs-lookup"><span data-stu-id="17da1-244">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Microsoft Defender Exploit Guard** > **Attack surface reduction**.</span></span>

4. <span data-ttu-id="17da1-245">Sélectionnez **Configurer les règles de réduction de la surface d’attaque** et **sélectionnez Activé.**</span><span class="sxs-lookup"><span data-stu-id="17da1-245">Select **Configure Attack surface reduction rules** and select **Enabled**.</span></span> <span data-ttu-id="17da1-246">Vous pouvez ensuite définir l’état individuel de chaque règle dans la section Options.</span><span class="sxs-lookup"><span data-stu-id="17da1-246">You can then set the individual state for each rule in the options section.</span></span>

   <span data-ttu-id="17da1-247">Sélectionnez **Afficher...** et entrez l’ID de règle dans  la colonne Nom de la valeur et l’état choisi dans la colonne Valeur comme suit : </span><span class="sxs-lookup"><span data-stu-id="17da1-247">Select **Show...** and enter the rule ID in the **Value name** column and your chosen state in the **Value** column as follows:</span></span>

   - <span data-ttu-id="17da1-248">0 : Désactiver (désactiver la règle asr)</span><span class="sxs-lookup"><span data-stu-id="17da1-248">0 : Disable (Disable the ASR rule)</span></span>
   - <span data-ttu-id="17da1-249">1 : Bloquer (activer la règle asr)</span><span class="sxs-lookup"><span data-stu-id="17da1-249">1 : Block (Enable the ASR rule)</span></span>
   - <span data-ttu-id="17da1-250">2 : Audit (évaluer l’impact de la règle asr sur votre organisation si elle est activée)</span><span class="sxs-lookup"><span data-stu-id="17da1-250">2 : Audit (Evaluate how the ASR rule would impact your organization if enabled)</span></span>
   - <span data-ttu-id="17da1-251">6 : Avertir (activer la règle asr mais autoriser l’utilisateur final à contourner le blocage)</span><span class="sxs-lookup"><span data-stu-id="17da1-251">6 : Warn  (Enable the ASR rule but allow the end-user to bypass the block)</span></span>

   :::image type="content" source="images/asr-rules-gp.png" alt-text="Règles asr dans la stratégie de groupe":::

5. <span data-ttu-id="17da1-253">Pour exclure des fichiers et des dossiers des règles de réduction de la surface d’attaque, sélectionnez le paramètre Exclure les fichiers et les chemins d’accès des règles de réduction de la **surface** d’attaque et définissez l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="17da1-253">To exclude files and folders from ASR rules, select the **Exclude files and paths from Attack surface reduction rules** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="17da1-254">Sélectionnez **Afficher** et entrez chaque fichier ou dossier dans la **colonne Nom de la** valeur.</span><span class="sxs-lookup"><span data-stu-id="17da1-254">Select **Show** and enter each file or folder in the **Value name** column.</span></span> <span data-ttu-id="17da1-255">Entrez **0 dans** la colonne **Valeur** pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="17da1-255">Enter **0** in the **Value** column for each item.</span></span>

   > [!WARNING]
   > <span data-ttu-id="17da1-256">N’utilisez pas de guillemets, car ils ne sont pas pris en charge pour la colonne Nom de la valeur ou la **colonne** Valeur. </span><span class="sxs-lookup"><span data-stu-id="17da1-256">Do not use quotes as they are not supported for either the **Value name** column or the **Value** column.</span></span>

## <a name="powershell"></a><span data-ttu-id="17da1-257">PowerShell</span><span class="sxs-lookup"><span data-stu-id="17da1-257">PowerShell</span></span>

> [!WARNING]
> <span data-ttu-id="17da1-258">Si vous gérez vos ordinateurs et appareils avec Intune, Configuration Manager ou une autre plateforme de gestion au niveau de l’entreprise, le logiciel de gestion risque d’éviter les paramètres PowerShell en conflit au démarrage.</span><span class="sxs-lookup"><span data-stu-id="17da1-258">If you manage your computers and devices with Intune, Configuration Manager, or another enterprise-level management platform, the management software will overwrite any conflicting PowerShell settings on startup.</span></span> <span data-ttu-id="17da1-259">Pour permettre aux utilisateurs de définir la valeur à l’aide de PowerShell, utilisez l’option « Défini par l’utilisateur » pour la règle dans la plateforme de gestion.</span><span class="sxs-lookup"><span data-stu-id="17da1-259">To allow users to define the value using PowerShell, use the "User Defined" option for the rule in the management platform.</span></span>

1. <span data-ttu-id="17da1-260">Tapez **powershell** dans le menu Démarrer, cliquez avec le **bouton droit sur Windows PowerShell** puis **sélectionnez Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="17da1-260">Type **powershell** in the Start menu, right-click **Windows PowerShell** and select **Run as administrator**.</span></span>

2. <span data-ttu-id="17da1-261">Tapez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="17da1-261">Type the following cmdlet:</span></span>

    ```PowerShell
    Set-MpPreference -AttackSurfaceReductionRules_Ids <rule ID> -AttackSurfaceReductionRules_Actions Enabled
    ```

    <span data-ttu-id="17da1-262">Pour activer les règles asr en mode audit, utilisez la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="17da1-262">To enable ASR rules in audit mode, use the following cmdlet:</span></span>

    ```PowerShell
    Add-MpPreference -AttackSurfaceReductionRules_Ids <rule ID> -AttackSurfaceReductionRules_Actions AuditMode
    ```

    <span data-ttu-id="17da1-263">Pour activer les règles de la asr en mode d’avertissement, utilisez l';</span><span class="sxs-lookup"><span data-stu-id="17da1-263">To enable ASR rules in warn mode, use the following cmdlet:</span></span>

    ```PowerShell
    Add-MpPreference -AttackSurfaceReductionRules_Ids <rule ID> -AttackSurfaceReductionRules_Actions Warn
    ```

    <span data-ttu-id="17da1-264">Pour activer l’utilisation abusive des pilotes signés vulnérables exploités, utilisez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="17da1-264">To enable ASR Block abuse of exploited vulnerable signed drivers, use the following cmdlet:</span></span>

   ```PowerShell
   "& {&'Add-MpPreference' -AttackSurfaceReductionRules_Ids 56a863a9-875e-4185-98a7-b882c64b5ce5 -AttackSurfaceReductionRules_Actions Enabled"}
   ```

    <span data-ttu-id="17da1-265">Pour désactiver les règles de la asr, utilisez la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="17da1-265">To turn off ASR rules, use the following cmdlet:</span></span>

    ```PowerShell
    Add-MpPreference -AttackSurfaceReductionRules_Ids <rule ID> -AttackSurfaceReductionRules_Actions Disabled
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="17da1-266">Vous devez spécifier l’état individuellement pour chaque règle, mais vous pouvez combiner des règles et des états dans une liste séparée par des virgules.</span><span class="sxs-lookup"><span data-stu-id="17da1-266">You must specify the state individually for each rule, but you can combine rules and states in a comma-separated list.</span></span>
    >
    > <span data-ttu-id="17da1-267">Dans l’exemple suivant, les deux premières règles sont activées, la troisième est désactivée et la quatrième règle est activée en mode audit :</span><span class="sxs-lookup"><span data-stu-id="17da1-267">In the following example, the first two rules will be enabled, the third rule will be disabled, and the fourth rule will be enabled in audit mode:</span></span>
    >
    > ```PowerShell
    > Set-MpPreference -AttackSurfaceReductionRules_Ids <rule ID 1>,<rule ID 2>,<rule ID 3>,<rule ID 4> -AttackSurfaceReductionRules_Actions Enabled, Enabled, Disabled, AuditMode
    > ```

    <span data-ttu-id="17da1-268">Vous pouvez également utiliser le verbe `Add-MpPreference` PowerShell pour ajouter de nouvelles règles à la liste existante.</span><span class="sxs-lookup"><span data-stu-id="17da1-268">You can also use the `Add-MpPreference` PowerShell verb to add new rules to the existing list.</span></span>

    > [!WARNING]
    > <span data-ttu-id="17da1-269">`Set-MpPreference` est toujours en cours de réécriture de l’ensemble de règles existant.</span><span class="sxs-lookup"><span data-stu-id="17da1-269">`Set-MpPreference` will always overwrite the existing set of rules.</span></span> <span data-ttu-id="17da1-270">Si vous souhaitez l’ajouter à l’ensemble existant, `Add-MpPreference` utilisez-le à la place.</span><span class="sxs-lookup"><span data-stu-id="17da1-270">If you want to add to the existing set, use `Add-MpPreference` instead.</span></span>
    > <span data-ttu-id="17da1-271">Vous pouvez obtenir une liste de règles et leur état actuel à l’aide `Get-MpPreference` de .</span><span class="sxs-lookup"><span data-stu-id="17da1-271">You can obtain a list of rules and their current state by using `Get-MpPreference`.</span></span>

3. <span data-ttu-id="17da1-272">Pour exclure des fichiers et des dossiers des règles de la asr, utilisez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="17da1-272">To exclude files and folders from ASR rules, use the following cmdlet:</span></span>

    ```PowerShell
    Add-MpPreference -AttackSurfaceReductionOnlyExclusions "<fully qualified path or resource>"
    ```

    <span data-ttu-id="17da1-273">Continuez à `Add-MpPreference -AttackSurfaceReductionOnlyExclusions` l’utiliser pour ajouter d’autres fichiers et dossiers à la liste.</span><span class="sxs-lookup"><span data-stu-id="17da1-273">Continue to use `Add-MpPreference -AttackSurfaceReductionOnlyExclusions` to add more files and folders to the list.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="17da1-274">Permet `Add-MpPreference` d’ajouter ou d’ajouter des applications à la liste.</span><span class="sxs-lookup"><span data-stu-id="17da1-274">Use `Add-MpPreference` to append or add apps to the list.</span></span> <span data-ttu-id="17da1-275">`Set-MpPreference`L’utilisation de la cmdlet va supprimer la liste existante.</span><span class="sxs-lookup"><span data-stu-id="17da1-275">Using the `Set-MpPreference` cmdlet will overwrite the existing list.</span></span>

## <a name="related-articles"></a><span data-ttu-id="17da1-276">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="17da1-276">Related articles</span></span>

- [<span data-ttu-id="17da1-277">Réduire les surfaces d’attaque avec des règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="17da1-277">Reduce attack surfaces with attack surface reduction rules</span></span>](attack-surface-reduction.md)

- [<span data-ttu-id="17da1-278">Évaluer la réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="17da1-278">Evaluate attack surface reduction</span></span>](evaluate-attack-surface-reduction.md)

- <span data-ttu-id="17da1-279">[FAQ sur la réduction de la surface d’attaque](attack-surface-reduction.md).</span><span class="sxs-lookup"><span data-stu-id="17da1-279">[Attack surface reduction FAQ](attack-surface-reduction.md)</span></span>
