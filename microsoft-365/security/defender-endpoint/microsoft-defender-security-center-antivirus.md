---
title: Antivirus Microsoft Defender dans l’application Sécurité Windows de messagerie
description: Avec Antivirus Microsoft Defender désormais inclus dans l’application Sécurité Windows, vous pouvez examiner, comparer et effectuer des tâches courantes.
keywords: wdav, antivirus, pare-feu, sécurité, fenêtres
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: normal
ms.topic: article
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 48ab72e9700e45cd4eab520a43d6f3d9ef18e227
ms.sourcegitcommit: be929f79751c0c52dfa6bd98a854432a0c63faf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52926534"
---
# <a name="microsoft-defender-antivirus-in-the-windows-security-app"></a><span data-ttu-id="8a8cf-104">Antivirus Microsoft Defender dans l’application Sécurité Windows de messagerie</span><span class="sxs-lookup"><span data-stu-id="8a8cf-104">Microsoft Defender Antivirus in the Windows Security app</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="8a8cf-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-105">**Applies to:**</span></span>

- [<span data-ttu-id="8a8cf-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8a8cf-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="8a8cf-107">Dans Windows 10 version 1703 et ultérieures, l’application Windows Defender fait partie du Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-107">In Windows 10, version 1703 and later, the Windows Defender app is part of the Windows Security.</span></span>

<span data-ttu-id="8a8cf-108">Paramètres qui faisaient auparavant partie du client Windows Defender et du Windows Paramètres principal ont été combinés et déplacés vers la nouvelle application, qui est installée par défaut dans le cadre de Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-108">Settings that were previously part of the Windows Defender client and main Windows Settings have been combined and moved to the new app, which is installed by default as part of Windows 10, version 1703.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a8cf-109">La désactivation du service Sécurité Windows ne désactive pas Antivirus Microsoft Defender ou [Pare-feu Windows Defender](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security).</span><span class="sxs-lookup"><span data-stu-id="8a8cf-109">Disabling the Windows Security Center service does not disable Microsoft Defender Antivirus or [Windows Defender Firewall](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security).</span></span> <span data-ttu-id="8a8cf-110">Ceux-ci sont désactivés automatiquement lorsqu’un antivirus tiers ou un produit de pare-feu est installé et maintenu à jour.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-110">These are disabled automatically when a third-party antivirus or firewall product is installed and kept up to date.</span></span>
>
> <span data-ttu-id="8a8cf-111">Si vous désactivez le service centre Sécurité Windows ou configurez ses paramètres de stratégie de groupe associés pour empêcher son démarrage ou son exécution, l’application Sécurité Windows peut afficher des informations obsolètes ou inexactes sur les produits antivirus ou pare-feu que vous avez installés sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-111">If you do disable the Windows Security Center service, or configure its associated Group Policy settings to prevent it from starting or running, the Windows Security app might display stale or inaccurate information about any antivirus or firewall products you have installed on the device.</span></span>
> <span data-ttu-id="8a8cf-112">Cela peut également empêcher les Antivirus Microsoft Defender de s’activer si vous avez un antivirus tiers ancien ou obsolète, ou si vous désinstallez des produits antivirus tiers que vous avez peut-être précédemment installés.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-112">It might also prevent Microsoft Defender Antivirus from enabling itself if you have an old or outdated third-party antivirus, or if you uninstall any third-party antivirus products you might have previously installed.</span></span>
> <span data-ttu-id="8a8cf-113">Cela réduit considérablement la protection de votre appareil et peut entraîner une infection par des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-113">This will significantly lower the protection of your device and could lead to malware infection.</span></span>

<span data-ttu-id="8a8cf-114">Consultez [l’article Sécurité Windows pour](/windows/threat-protection/windows-defender-security-center/windows-defender-security-center) plus d’informations sur les autres fonctionnalités Windows sécurité qui peuvent être surveillées dans l’application.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-114">See the [Windows Security article](/windows/threat-protection/windows-defender-security-center/windows-defender-security-center) for more information on other Windows security features that can be monitored in the app.</span></span>

<span data-ttu-id="8a8cf-115">L Sécurité Windows’application est une interface client Windows 10 version 1703 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-115">The Windows Security app is a client interface on Windows 10, version 1703 and later.</span></span> <span data-ttu-id="8a8cf-116">Il ne s’agit pas du Centre de sécurité Microsoft Defender web utilisé pour examiner et gérer [Microsoft Defender for Endpoint.](/microsoft-365/security/defender-endpoint/microsoft-defender-endpoint)</span><span class="sxs-lookup"><span data-stu-id="8a8cf-116">It is not the Microsoft Defender Security Center web portal that is used to review and manage [Microsoft Defender for Endpoint](/microsoft-365/security/defender-endpoint/microsoft-defender-endpoint).</span></span>

## <a name="review-virus-and-threat-protection-settings-in-the-windows-security-app"></a><span data-ttu-id="8a8cf-117">Passer en revue les paramètres de protection contre les virus et les menaces dans l Sécurité Windows appl</span><span class="sxs-lookup"><span data-stu-id="8a8cf-117">Review virus and threat protection settings in the Windows Security app</span></span>

![Capture d’écran de l’étiquette des paramètres de protection contre les virus et les menaces dans l’application Sécurité Windows](images/defender/wdav-protection-settings-wdsc.png)

1. <span data-ttu-id="8a8cf-119">Ouvrez l Sécurité Windows application en cliquant sur l’icône de bouclier dans la barre des tâches ou en recherchant Defender dans le menu **Démarrer.**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-119">Open the Windows Security app by clicking the shield icon in the task bar or searching the start menu for **Defender**.</span></span>

2. <span data-ttu-id="8a8cf-120">Sélectionnez la **vignette & protection contre** les virus contre les menaces (ou l’icône de bouclier dans la barre de menus de gauche).</span><span class="sxs-lookup"><span data-stu-id="8a8cf-120">Select the **Virus & threat protection** tile (or the shield icon on the left menu bar).</span></span>
   
<span data-ttu-id="8a8cf-121">Les sections suivantes décrivent comment effectuer certaines des tâches les plus courantes lors de l’examen ou de l’interaction avec la protection contre les menaces fournie par Antivirus Microsoft Defender dans l’application Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-121">The following sections describe how to perform some of the most common tasks when reviewing or interacting with the threat protection provided by Microsoft Defender Antivirus in the Windows Security app.</span></span>

> [!NOTE]
> <span data-ttu-id="8a8cf-122">Si ces paramètres sont configurés et déployés à l’aide de la stratégie de groupe, les paramètres décrits dans cette section sont grisés et ne peuvent pas être utilisés sur des points de terminaison individuels.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-122">If these settings are configured and deployed using Group Policy, the settings described in this section will be greyed-out and unavailable for use on individual endpoints.</span></span> <span data-ttu-id="8a8cf-123">Les modifications apportées via un objet de stratégie de groupe doivent d’abord être déployées vers les points de terminaison individuels avant que le paramètre soit mis à jour dans les Paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-123">Changes made through a Group Policy Object must first be deployed to individual endpoints before the setting will be updated in Windows Settings.</span></span> <span data-ttu-id="8a8cf-124">La [rubrique Configure end-user interaction with Antivirus Microsoft Defender](configure-end-user-interaction-microsoft-defender-antivirus.md) describes how local policy override settings can be configured.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-124">The [Configure end-user interaction with Microsoft Defender Antivirus](configure-end-user-interaction-microsoft-defender-antivirus.md) topic describes how local policy override settings can be configured.</span></span>

## <a name="run-a-scan-with-the-windows-security-app"></a><span data-ttu-id="8a8cf-125">Exécuter une analyse avec l’Sécurité Windows de recherche</span><span class="sxs-lookup"><span data-stu-id="8a8cf-125">Run a scan with the Windows Security app</span></span>

1. <span data-ttu-id="8a8cf-126">Ouvrez l’Sécurité Windows en recherchant sécurité dans le menu **Démarrer,** puis en **sélectionnant Sécurité Windows**.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-126">Open the Windows Security app by searching the start menu for **Security**, and then selecting **Windows Security**.</span></span>

2. <span data-ttu-id="8a8cf-127">Sélectionnez la **vignette & protection contre** les virus contre les menaces (ou l’icône de bouclier dans la barre de menus de gauche).</span><span class="sxs-lookup"><span data-stu-id="8a8cf-127">Select the **Virus & threat protection** tile (or the shield icon on the left menu bar).</span></span>

3. <span data-ttu-id="8a8cf-128">Sélectionnez **Analyse rapide.**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-128">Select **Quick scan**.</span></span> <span data-ttu-id="8a8cf-129">Ou, pour exécuter une analyse complète, sélectionnez **Options** d’analyse, puis sélectionnez une option, telle que **l’analyse complète**.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-129">Or, to run a full scan, select **Scan options**, and then select an option, such as **Full scan**.</span></span>

## <a name="review-the-security-intelligence-update-version-and-download-the-latest-updates-in-the-windows-security-app"></a><span data-ttu-id="8a8cf-130">Passer en revue la version de mise à jour des informations de sécurité et télécharger les dernières mises à jour dans l’Sécurité Windows de sécurité</span><span class="sxs-lookup"><span data-stu-id="8a8cf-130">Review the security intelligence update version and download the latest updates in the Windows Security app</span></span>

![Informations sur le numéro de version de l’intelligence de la sécurité](images/defender/wdav-wdsc-defs.png)

1. <span data-ttu-id="8a8cf-132">Ouvrez l’Sécurité Windows en recherchant sécurité dans le menu *Démarrer,* puis en **sélectionnant Sécurité Windows**.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-132">Open the Windows Security app by searching the start menu for *Security*, and then selecting **Windows Security**.</span></span>

2. <span data-ttu-id="8a8cf-133">Sélectionnez la **vignette & protection contre** les virus contre les menaces (ou l’icône de bouclier dans la barre de menus de gauche).</span><span class="sxs-lookup"><span data-stu-id="8a8cf-133">Select the **Virus & threat protection** tile (or the shield icon on the left menu bar).</span></span>

3. <span data-ttu-id="8a8cf-134">Sélectionnez **les mises à jour & protection contre les virus contre les menaces.**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-134">Select **Virus & threat protection updates**.</span></span> <span data-ttu-id="8a8cf-135">La version actuellement installée s’affiche avec des informations sur le moment où elle a été téléchargée.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-135">The currently installed version is displayed along with some information about when it was downloaded.</span></span> <span data-ttu-id="8a8cf-136">Vous pouvez vérifier votre version actuelle par rapport à la dernière version disponible pour le téléchargement manuel ou consulter le journal des changements pour cette version.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-136">You can check your current against the latest version available for manual download, or review the change log for that version.</span></span> <span data-ttu-id="8a8cf-137">Consultez les mises à jour de l’intelligence [de sécurité pour Antivirus Microsoft Defender logiciel anti-programme malveillant Microsoft.](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span><span class="sxs-lookup"><span data-stu-id="8a8cf-137">See [Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/en-us/wdsi/defenderupdates).</span></span>

4. <span data-ttu-id="8a8cf-138">Sélectionnez **Vérifier les mises à jour pour** télécharger les nouvelles mises à jour de la protection (le cas caser).</span><span class="sxs-lookup"><span data-stu-id="8a8cf-138">Select **Check for updates** to download new protection updates (if there are any).</span></span>

## <a name="ensure-microsoft-defender-antivirus-is-enabled-in-the-windows-security-app"></a><span data-ttu-id="8a8cf-139">Vérifier Antivirus Microsoft Defender est activé dans l’application Sécurité Windows de messagerie</span><span class="sxs-lookup"><span data-stu-id="8a8cf-139">Ensure Microsoft Defender Antivirus is enabled in the Windows Security app</span></span>

1. <span data-ttu-id="8a8cf-140">Ouvrez l’Sécurité Windows en recherchant sécurité dans le menu *Démarrer,* puis en **sélectionnant Sécurité Windows**.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-140">Open the Windows Security app by searching the start menu for *Security*, and then selecting **Windows Security**.</span></span>

2. <span data-ttu-id="8a8cf-141">Sélectionnez la **vignette & protection contre** les virus contre les menaces (ou l’icône de bouclier dans la barre de menus de gauche).</span><span class="sxs-lookup"><span data-stu-id="8a8cf-141">Select the **Virus & threat protection** tile (or the shield icon on the left menu bar).</span></span>

3. <span data-ttu-id="8a8cf-142">Sélectionnez **les paramètres & protection contre les virus contre les menaces.**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-142">Select **Virus & threat protection settings**.</span></span>

4. <span data-ttu-id="8a8cf-143">Basculez le **commutateur de protection en temps** réel sur **Sur**.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-143">Toggle the **Real-time protection** switch to **On**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8a8cf-144">Si vous **éteyez la protection en** temps réel, elle est automatiquement réaxion après un court délai.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-144">If you switch **Real-time protection** off, it will automatically turn back on after a short delay.</span></span> <span data-ttu-id="8a8cf-145">Cela permet de vous assurer que vous êtes protégé contre les programmes malveillants et les menaces.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-145">This is to ensure you are protected from malware and threats.</span></span>
    > <span data-ttu-id="8a8cf-146">Si vous installez un autre produit antivirus, Antivirus Microsoft Defender se désactive automatiquement et est indiqué en tant que tel dans l’Sécurité Windows app.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-146">If you install another antivirus product, Microsoft Defender Antivirus automatically disables itself and is indicated as such in the Windows Security app.</span></span> <span data-ttu-id="8a8cf-147">Un paramètre s’affiche pour vous permettre d’activer [l’analyse périodique limitée.](limited-periodic-scanning-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="8a8cf-147">A setting will appear that will allow you to enable [limited periodic scanning](limited-periodic-scanning-microsoft-defender-antivirus.md).</span></span>

## <a name="add-exclusions-for-microsoft-defender-antivirus-in-the-windows-security-app"></a><span data-ttu-id="8a8cf-148">Ajouter des exclusions pour Antivirus Microsoft Defender dans l’application Sécurité Windows’application</span><span class="sxs-lookup"><span data-stu-id="8a8cf-148">Add exclusions for Microsoft Defender Antivirus in the Windows Security app</span></span>

1. <span data-ttu-id="8a8cf-149">Ouvrez l’Sécurité Windows en recherchant sécurité dans le menu *Démarrer,* puis en **sélectionnant Sécurité Windows**.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-149">Open the Windows Security app by searching the start menu for *Security*, and then selecting **Windows Security**.</span></span>

2. <span data-ttu-id="8a8cf-150">Sélectionnez la **vignette & protection contre** les virus contre les menaces (ou l’icône de bouclier dans la barre de menus de gauche).</span><span class="sxs-lookup"><span data-stu-id="8a8cf-150">Select the **Virus & threat protection** tile (or the shield icon on the left menu bar).</span></span>

3. <span data-ttu-id="8a8cf-151">Sous les **paramètres Gérer,** sélectionnez **Paramètres de protection contre & virus.**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-151">Under the **Manage settings**, select **Virus & threat protection settings**.</span></span>

4. <span data-ttu-id="8a8cf-152">Sous le **paramètre Exclusions,** **sélectionnez Ajouter ou supprimer des exclusions.**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-152">Under the **Exclusions** setting, select **Add or remove exclusions**.</span></span> 

5. <span data-ttu-id="8a8cf-153">Sélectionnez l’icône plus ( **+** ) pour choisir le type et définir les options pour chaque exclusion.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-153">Select the plus icon (**+**) to choose the type and set the options for each exclusion.</span></span> 

<span data-ttu-id="8a8cf-154">Le tableau suivant récapitule les types d’exclusion et ce qui se produit :</span><span class="sxs-lookup"><span data-stu-id="8a8cf-154">The following table summarizes exclusion types and what happens:</span></span>

|<span data-ttu-id="8a8cf-155">Type d’exclusion</span><span class="sxs-lookup"><span data-stu-id="8a8cf-155">Exclusion type</span></span>  |<span data-ttu-id="8a8cf-156">Défini par</span><span class="sxs-lookup"><span data-stu-id="8a8cf-156">Defined by</span></span>  |<span data-ttu-id="8a8cf-157">Action exécutée</span><span class="sxs-lookup"><span data-stu-id="8a8cf-157">What happens</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="8a8cf-158">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-158">**File**</span></span> |<span data-ttu-id="8a8cf-159">Emplacement</span><span class="sxs-lookup"><span data-stu-id="8a8cf-159">Location</span></span> <br/><span data-ttu-id="8a8cf-160">Exemple : `c:\sample\sample.test`</span><span class="sxs-lookup"><span data-stu-id="8a8cf-160">Example: `c:\sample\sample.test`</span></span> |<span data-ttu-id="8a8cf-161">Le fichier spécifique est ignoré par Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-161">The specific file is skipped by Microsoft Defender Antivirus.</span></span> |
|<span data-ttu-id="8a8cf-162">**Folder**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-162">**Folder**</span></span>    |<span data-ttu-id="8a8cf-163">Emplacement</span><span class="sxs-lookup"><span data-stu-id="8a8cf-163">Location</span></span> <br/><span data-ttu-id="8a8cf-164">Exemple : `c:\test\sample`</span><span class="sxs-lookup"><span data-stu-id="8a8cf-164">Example: `c:\test\sample`</span></span>       |<span data-ttu-id="8a8cf-165">Tous les éléments du dossier spécifié sont ignorés par Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-165">All items in the specified folder are skipped by Microsoft Defender Antivirus.</span></span>         |
|<span data-ttu-id="8a8cf-166">**Type de fichier**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-166">**File type**</span></span>   |<span data-ttu-id="8a8cf-167">Extension de fichier</span><span class="sxs-lookup"><span data-stu-id="8a8cf-167">File extension</span></span> <br/><span data-ttu-id="8a8cf-168">Exemple : `.test`</span><span class="sxs-lookup"><span data-stu-id="8a8cf-168">Example: `.test`</span></span> |<span data-ttu-id="8a8cf-169">Tous les fichiers avec `.test` l’extension n’importe où sur votre appareil sont ignorés par Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-169">All files with the `.test` extension anywhere on your device are skipped by Microsoft Defender Antivirus.</span></span>         |
|<span data-ttu-id="8a8cf-170">**Processus**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-170">**Process**</span></span>     |<span data-ttu-id="8a8cf-171">Chemin d’accès au fichier exécutable</span><span class="sxs-lookup"><span data-stu-id="8a8cf-171">Executable file path</span></span> <br><span data-ttu-id="8a8cf-172">Exemple : `c:\test\process.exe`</span><span class="sxs-lookup"><span data-stu-id="8a8cf-172">Example: `c:\test\process.exe`</span></span>         |<span data-ttu-id="8a8cf-173">Le processus spécifique et tous les fichiers ouverts par ce processus sont ignorés par Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-173">The specific process and any files that are opened by that process are skipped by Microsoft Defender Antivirus.</span></span>         |

<span data-ttu-id="8a8cf-174">Pour en savoir plus, consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a8cf-174">To learn more, see the following resources:</span></span>
- [<span data-ttu-id="8a8cf-175">Configurer et valider des exclusions en fonction de l’extension de fichier et de l’emplacement du dossier</span><span class="sxs-lookup"><span data-stu-id="8a8cf-175">Configure and validate exclusions based on file extension and folder location</span></span>](./configure-extension-file-exclusions-microsoft-defender-antivirus.md) 
- [<span data-ttu-id="8a8cf-176">Configurer des exclusions pour les fichiers ouverts par des processus</span><span class="sxs-lookup"><span data-stu-id="8a8cf-176">Configure exclusions for files opened by processes</span></span>](./configure-process-opened-file-exclusions-microsoft-defender-antivirus.md)

## <a name="review-threat-detection-history-in-the-windows-defender-security-center-app"></a><span data-ttu-id="8a8cf-177">Passer en revue l’historique de détection des menaces dans Windows Defender’application Centre de sécurité</span><span class="sxs-lookup"><span data-stu-id="8a8cf-177">Review threat detection history in the Windows Defender Security Center app</span></span>

1. <span data-ttu-id="8a8cf-178">Ouvrez l’Sécurité Windows en recherchant sécurité dans le menu *Démarrer,* puis en **sélectionnant Sécurité Windows**.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-178">Open the Windows Security app by searching the start menu for *Security*, and then selecting **Windows Security**.</span></span>

2. <span data-ttu-id="8a8cf-179">Sélectionnez la **vignette & protection contre** les virus contre les menaces (ou l’icône de bouclier dans la barre de menus de gauche).</span><span class="sxs-lookup"><span data-stu-id="8a8cf-179">Select the **Virus & threat protection** tile (or the shield icon on the left menu bar).</span></span>

3. <span data-ttu-id="8a8cf-180">Sélectionnez **l’historique de la protection.**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-180">Select **Protection history**.</span></span> <span data-ttu-id="8a8cf-181">Tous les éléments récents sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-181">Any recent items are listed.</span></span>

## <a name="set-ransomware-protection-and-recovery-options"></a><span data-ttu-id="8a8cf-182">Définir les options de protection et de récupération des ransomware</span><span class="sxs-lookup"><span data-stu-id="8a8cf-182">Set ransomware protection and recovery options</span></span>

1. <span data-ttu-id="8a8cf-183">Ouvrez l’Sécurité Windows en recherchant sécurité dans le menu *Démarrer,* puis en **sélectionnant Sécurité Windows**.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-183">Open the Windows Security app by searching the start menu for *Security*, and then selecting **Windows Security**.</span></span>

2. <span data-ttu-id="8a8cf-184">Sélectionnez la **vignette & protection contre** les virus contre les menaces (ou l’icône de bouclier dans la barre de menus de gauche).</span><span class="sxs-lookup"><span data-stu-id="8a8cf-184">Select the **Virus & threat protection** tile (or the shield icon on the left menu bar).</span></span>

3. <span data-ttu-id="8a8cf-185">Sous Protection **contre les ransomware,** **sélectionnez Gérer la protection contre les ransomware.**</span><span class="sxs-lookup"><span data-stu-id="8a8cf-185">Under **Ransomware protection**, select **Manage ransomware protection**.</span></span>

4. <span data-ttu-id="8a8cf-186">Pour modifier **les paramètres d’accès contrôlé aux** dossiers, voir Protéger les dossiers importants avec accès contrôlé aux [dossiers.](/microsoft-365/security/defender-endpoint/controlled-folders)</span><span class="sxs-lookup"><span data-stu-id="8a8cf-186">To change **Controlled folder access** settings, see [Protect important folders with Controlled folder access](/microsoft-365/security/defender-endpoint/controlled-folders).</span></span>

5. <span data-ttu-id="8a8cf-187">Pour configurer les options  de récupération  de ransomware, sélectionnez Configurer sous Récupération des données de ransomware et suivez les instructions pour lier ou configurer votre compte OneDrive afin de pouvoir facilement récupérer d’une attaque par ransomware.</span><span class="sxs-lookup"><span data-stu-id="8a8cf-187">To set up ransomware recovery options, select **Set up** under **Ransomware data recovery** and follow the instructions for linking or setting up your OneDrive account so you can easily recover from a ransomware attack.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a8cf-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a8cf-188">See also</span></span>
- [<span data-ttu-id="8a8cf-189">Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="8a8cf-189">Microsoft Defender Antivirus</span></span>](microsoft-defender-antivirus-in-windows-10.md)