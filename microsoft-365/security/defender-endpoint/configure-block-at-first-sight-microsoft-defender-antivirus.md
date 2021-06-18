---
title: Activer Bloquer à la première consultation pour la détection d’un programme malveillant en quelques secondes
description: Activer la fonctionnalité Bloquer à la première consultation pour la détection et le blocage d’un programme malveillant en quelques secondes.
keywords: analyser, bloquer à la première consultation, programme malveillant, à la première consultation, cloud, defender, antivirus
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Priority
author: denisebmsft
ms.author: deniseb
ms.reviewer: marcmcc
manager: dansimp
ms.custom: nextgen
ms.date: 06/15/2021
ms.technology: mde
ms.topic: article
ms.openlocfilehash: 3a5f766e21afcb29d3503345a49637061b5f0e38
ms.sourcegitcommit: 1c11035dd4432e34603022740baef0c8f7ff4425
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/16/2021
ms.locfileid: "52964698"
---
# <a name="turn-on-block-at-first-sight"></a><span data-ttu-id="3760b-104">Activer Bloquer à la première consultation</span><span class="sxs-lookup"><span data-stu-id="3760b-104">Turn on block at first sight</span></span>

<span data-ttu-id="3760b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3760b-105">**Applies to:**</span></span>

- [<span data-ttu-id="3760b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3760b-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="3760b-107">Cet article présente la fonctionnalité antivirus/logiciel anti-programme malveillant appelée « Bloquer à la première consultation » et décrit la façon d’activer Bloquer à la première consultation pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3760b-107">This article describes an antivirus/antimalware feature known as "block at first sight", and describes how to enable block at first sight for your organization.</span></span> 

> [!TIP]
> <span data-ttu-id="3760b-108">Cet article est destiné aux administrateurs d’entreprise et aux professionnels de l’informatique qui gère les paramètres de sécurité pour des organisations.</span><span class="sxs-lookup"><span data-stu-id="3760b-108">This article is intended for enterprise admins and IT Pros who manage security settings for organizations.</span></span> <span data-ttu-id="3760b-109">Si vous n’êtes pas un administrateur d’entreprise ou un professionnel de l’informatique, mais que vous avez des questions à propos de Bloquer à la première consultation, consultez la section [Vous n’êtes pas un administrateur d’entreprise ou un professionnel de l’informatique ?](#not-an-enterprise-admin-or-it-pro).</span><span class="sxs-lookup"><span data-stu-id="3760b-109">If you are not an enteprise admin or IT Pro but you have questions about block at first sight, see the [Not an enterprise admin or IT Pro?](#not-an-enterprise-admin-or-it-pro) section.</span></span>

## <a name="what-is-block-at-first-sight"></a><span data-ttu-id="3760b-110">Qu’est-ce que « Bloquer à la première consultation » ?</span><span class="sxs-lookup"><span data-stu-id="3760b-110">What is "block at first sight"?</span></span>

<span data-ttu-id="3760b-111">Bloquer à la première consultation est une fonctionnalité de protection de nouvelle génération de protection contre les menaces qui détecte un nouveau programme malveillant et le bloque en quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="3760b-111">Block at first sight is a threat protection feature of next-generation protection that detects new malware and blocks it within seconds.</span></span> <span data-ttu-id="3760b-112">La fonctionnalité Bloquer à la première consultation est activée lorsque certains paramètres de sécurité sont activés.</span><span class="sxs-lookup"><span data-stu-id="3760b-112">Block at first sight is enabled when certain security settings are enabled.</span></span> <span data-ttu-id="3760b-113">Ces paramètres sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="3760b-113">These settings include:</span></span>

- <span data-ttu-id="3760b-114">Protection fournie par le cloud ;</span><span class="sxs-lookup"><span data-stu-id="3760b-114">Cloud-delivered protection;</span></span> 
- <span data-ttu-id="3760b-115">Un échantillon spécifique d’expiration de l'envoi (tel que 50 secondes) et</span><span class="sxs-lookup"><span data-stu-id="3760b-115">A specified sample submission timeout (such as 50 seconds); and</span></span> 
- <span data-ttu-id="3760b-116">Un blocage des fichiers de niveau élevé.</span><span class="sxs-lookup"><span data-stu-id="3760b-116">A file-blocking level of high.</span></span> 

<span data-ttu-id="3760b-117">Dans la plupart des entreprises, les paramètres nécessaires pour activer Bloquer à la première consultation sont configurés avec les déploiements de l’Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="3760b-117">In most enterprise organizations, the settings needed to enable block at first sight are configured with Microsoft Defender Antivirus deployments.</span></span> 

## <a name="how-it-works"></a><span data-ttu-id="3760b-118">Mode de fonctionnement</span><span class="sxs-lookup"><span data-stu-id="3760b-118">How it works</span></span>

<span data-ttu-id="3760b-119">Lorsque l’Antivirus Microsoft Defender rencontre un fichier suspect, mais non détecté, il interroge notre serveur principal de protection cloud.</span><span class="sxs-lookup"><span data-stu-id="3760b-119">When Microsoft Defender Antivirus encounters a suspicious but undetected file, it queries our cloud protection backend.</span></span> <span data-ttu-id="3760b-120">Le serveur principal de protection cloud applique la méthode heuristique, l’apprentissage automatique et l’analyse automatisée de fichier pour déterminer si les fichiers sont suspects ou s’ils ne sont pas une menace.</span><span class="sxs-lookup"><span data-stu-id="3760b-120">The cloud backend applies heuristics, machine learning, and automated analysis of the file to determine whether the files are malicious or not a threat.</span></span>

<span data-ttu-id="3760b-121">L’Antivirus Microsoft Defender utilise plusieurs technologies de prévention et de détection pour fournir une protection exacte, intelligente et en temps réel.</span><span class="sxs-lookup"><span data-stu-id="3760b-121">Microsoft Defender Antivirus uses multiple detection and prevention technologies to deliver accurate, intelligent, and real-time protection.</span></span> 

![Liste des moteurs AV de Microsoft Defender](images/microsoft-defender-atp-next-generation-protection-engines.png)  

> [!TIP]
> <span data-ttu-id="3760b-123">Pour en savoir plus, consultez [(Blog) Découvrir les technologies avancées au cœur de la protection de nouvelle génération de Microsoft Defender pour point de terminaison](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/).</span><span class="sxs-lookup"><span data-stu-id="3760b-123">To learn more, see [(Blog) Get to know the advanced technologies at the core of Microsoft Defender for Endpoint next-generation protection](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/).</span></span>

## <a name="a-few-things-to-know-about-block-at-first-sight"></a><span data-ttu-id="3760b-124">Quelques éléments à connaître à propos de la fonctionnalité Bloquer à la première consultation</span><span class="sxs-lookup"><span data-stu-id="3760b-124">A few things to know about block at first sight</span></span>

- <span data-ttu-id="3760b-125">Dans Windows 10, version 1803 ou ultérieure, Bloquer à la première consultation peut bloquer des fichiers exécutables non portables (tels que JS, VBS ou les macros) et des fichiers exécutables.</span><span class="sxs-lookup"><span data-stu-id="3760b-125">In Windows 10, version 1803 or later, block at first sight can block non-portable executable files (such as JS, VBS, or macros) and executable files.</span></span>

- <span data-ttu-id="3760b-126">Bloquer à la première consultation utilise uniquement le serveur principal de protection cloud pour les fichiers exécutables et les fichiers exécutables non portables qui sont téléchargés à partir d’Internet ou qui sont issus de la zone Internet.</span><span class="sxs-lookup"><span data-stu-id="3760b-126">Block at first sight only uses the cloud protection backend for executable files and non-portable executable files that are downloaded from the Internet, or that originate from the Internet zone.</span></span> <span data-ttu-id="3760b-127">Une valeur de hachage du fichier .exe est vérifiée via le serveur principal de protection cloud pour déterminer s’il s’agit d’un fichier précédemment non détecté.</span><span class="sxs-lookup"><span data-stu-id="3760b-127">A hash value of the .exe file is checked via the cloud backend to determine if the file is a previously undetected file.</span></span>

- <span data-ttu-id="3760b-128">Si le serveur principal cloud ne peut pas se prononcer, l’Antivirus Microsoft Defender bloque le fichier et télécharge une copie dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="3760b-128">If the cloud backend is unable to make a determination, Microsoft Defender Antivirus locks the file and uploads a copy to the cloud.</span></span> <span data-ttu-id="3760b-129">Le cloud effectue d’autres analyses pour se prononcer avant d’autoriser le fichier à s’exécuter ou de le bloquer dans toutes les autres occurrences, selon qu’il détermine que le fichier est suspect ou qu’il n’est pas une menace.</span><span class="sxs-lookup"><span data-stu-id="3760b-129">The cloud performs more analysis to reach a determination before it either allows the file to run or blocks it in all future encounters, depending on whether it determines the file to be malicious or not a threat.</span></span>

- <span data-ttu-id="3760b-130">Dans de nombreux cas, ce processus peut diminuer le temps de réponse de plusieurs heures à quelques secondes pour un nouveau programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="3760b-130">In many cases, this process can reduce the response time for new malware from hours to seconds.</span></span>

- <span data-ttu-id="3760b-131">Vous pouvez [spécifier la durée d’interdiction d’exécution d’un fichier](configure-cloud-block-timeout-period-microsoft-defender-antivirus.md) pendant que le service de protection dans le cloud analyse le fichier.</span><span class="sxs-lookup"><span data-stu-id="3760b-131">You can [specify how long a file should be prevented from running](configure-cloud-block-timeout-period-microsoft-defender-antivirus.md) while the cloud-based protection service analyzes the file.</span></span> <span data-ttu-id="3760b-132">Vous pouvez également [personnaliser le message affiché sur les bureaux des utilisateurs](/windows/security/threat-protection//windows-defender-security-center/wdsc-customize-contact-information.md) lorsqu’un fichier est bloqué.</span><span class="sxs-lookup"><span data-stu-id="3760b-132">And, you can [customize the message displayed on users' desktops](/windows/security/threat-protection//windows-defender-security-center/wdsc-customize-contact-information.md) when a file is blocked.</span></span> <span data-ttu-id="3760b-133">Vous pouvez modifier le nom de l’entreprise, les informations de contact et l’URL du message.</span><span class="sxs-lookup"><span data-stu-id="3760b-133">You can change the company name, contact information, and message URL.</span></span>

## <a name="turn-on-block-at-first-sight-with-microsoft-intune"></a><span data-ttu-id="3760b-134">Activer la fonctionnalité Bloquer à la première consultation avec Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="3760b-134">Turn on block at first sight with Microsoft Intune</span></span>

> [!TIP]
> <span data-ttu-id="3760b-135">Microsoft Intune fait désormais partie de Microsoft Endpoint Manager.</span><span class="sxs-lookup"><span data-stu-id="3760b-135">Microsoft Intune is now part of Microsoft Endpoint Manager.</span></span>

1. <span data-ttu-id="3760b-136">Dans le Centre d’administration Microsoft Endpoint Manager ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)), naviguez vers **Appareils** > **Profils de configuration**.</span><span class="sxs-lookup"><span data-stu-id="3760b-136">In the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)), navigate to **Devices** > **Configuration profiles**.</span></span>

2. <span data-ttu-id="3760b-137">Sélectionnez ou créez un profil à l’aide du type de profil **Restrictions d’appareil**.</span><span class="sxs-lookup"><span data-stu-id="3760b-137">Select or create a profile using the **Device restrictions** profile type.</span></span>

3. <span data-ttu-id="3760b-138">Dans **Paramètres de configuration** pour le profil des Restrictions d’appareil, configurez ou confirmez les paramètres suivants sous **Antivirus Microsoft Defender** :</span><span class="sxs-lookup"><span data-stu-id="3760b-138">In the **Configuration settings** for the Device restrictions profile, set or confirm the following settings under **Microsoft Defender Antivirus**:</span></span>

   - <span data-ttu-id="3760b-139">**Protection fournie par le cloud** : Activée</span><span class="sxs-lookup"><span data-stu-id="3760b-139">**Cloud-delivered protection**: Enabled</span></span>
   - <span data-ttu-id="3760b-140">**Niveau de blocage des fichiers** : Élevé</span><span class="sxs-lookup"><span data-stu-id="3760b-140">**File Blocking Level**: High</span></span>
   - <span data-ttu-id="3760b-141">**Extension de temps pour l’analyse des fichiers dans le cloud** : 50</span><span class="sxs-lookup"><span data-stu-id="3760b-141">**Time extension for file scanning by the cloud**: 50</span></span>
   - <span data-ttu-id="3760b-142">**Demander aux utilisateurs avant la soumission d’échantillons** : Envoyer tous les données sans demande</span><span class="sxs-lookup"><span data-stu-id="3760b-142">**Prompt users before sample submission**: Send all data without prompting</span></span>

   ![Configuration Intune](images/defender/intune-block-at-first-sight.png)

4. <span data-ttu-id="3760b-144">Enregistrez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="3760b-144">Save your settings.</span></span>

> [!TIP]
> - <span data-ttu-id="3760b-145">Le paramétrage du niveau de blocage des fichiers sur **Élevé** applique un niveau fort de détection.</span><span class="sxs-lookup"><span data-stu-id="3760b-145">Setting the file blocking level to **High** applies a strong level of detection.</span></span> <span data-ttu-id="3760b-146">Dans le cas peu probable où le blocage du fichier entraîne la détection de faux positif de fichiers légitimes, votre équipe des opérations de sécurité peut [restaurer les fichiers mis en quarantaine](./restore-quarantined-files-microsoft-defender-antivirus.md).</span><span class="sxs-lookup"><span data-stu-id="3760b-146">In the unlikely event that file blocking causes a false positive detection of legitimate files, your security operations team can [restore quarantined files](./restore-quarantined-files-microsoft-defender-antivirus.md).</span></span>
> - <span data-ttu-id="3760b-147">Pour plus d’informations sur la configuration de restriction d’appareils de l’Antivirus Microsoft Defender dans Microsoft Intune, voir [Configurer les paramètres de restriction d’appareil de dans Microsoft Intune](/intune/device-restrictions-configure).</span><span class="sxs-lookup"><span data-stu-id="3760b-147">For more information about configuring Microsoft Defender Antivirus device restrictions in Intune, see [Configure device restriction settings in Microsoft Intune](/intune/device-restrictions-configure).</span></span>
> - <span data-ttu-id="3760b-148">Pour une liste des restrictions d’appareils de l’Antivirus Microsoft Defender dans Intune, voir [Paramètres de restriction d’appareil pour Windows 10 (et versions ultérieures) dans Intune](/intune/device-restrictions-windows-10#microsoft-defender-antivirus).</span><span class="sxs-lookup"><span data-stu-id="3760b-148">For a list of Microsoft Defender Antivirus device restrictions in Intune, see [Device restriction for Windows 10 (and newer) settings in Intune](/intune/device-restrictions-windows-10#microsoft-defender-antivirus).</span></span>

## <a name="turn-on-block-at-first-sight-with-microsoft-endpoint-manager"></a><span data-ttu-id="3760b-149">Activer la fonctionnalité Bloquer à la première consultation avec Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="3760b-149">Turn on block at first sight with Microsoft Endpoint Manager</span></span>

> [!TIP]
> <span data-ttu-id="3760b-150">Si vous recherchez Microsoft Endpoint Configuration Manager, il fait désormais partie de Microsoft Endpoint Manager.</span><span class="sxs-lookup"><span data-stu-id="3760b-150">If you're looking for Microsoft Endpoint Configuration Manager, it's now part of Microsoft Endpoint Manager.</span></span>

1. <span data-ttu-id="3760b-151">Dans Microsoft Endpoint Manager ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)), accédez à **Sécurité des points de terminaison** > **Antivirus**.</span><span class="sxs-lookup"><span data-stu-id="3760b-151">In Microsoft Endpoint Manager ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)), go to **Endpoint security** > **Antivirus**.</span></span>

2. <span data-ttu-id="3760b-152">Sélectionnez une stratégie existante ou créez-en une nouvelle à l’aide du type de profil **Antivirus Microsoft Defender**.</span><span class="sxs-lookup"><span data-stu-id="3760b-152">Select an existing policy, or create a new policy using the **Microsoft Defender Antivirus** profile type.</span></span>

3. <span data-ttu-id="3760b-153">Configurez ou confirmez les paramètres de configuration suivants :</span><span class="sxs-lookup"><span data-stu-id="3760b-153">Set or confirm the following configuration settings:</span></span>

   - <span data-ttu-id="3760b-154">**Activer la protection par le cloud** : Oui</span><span class="sxs-lookup"><span data-stu-id="3760b-154">**Turn on cloud-delivered protection**: Yes</span></span>
   - <span data-ttu-id="3760b-155">**Niveau de protection par le cloud** : Élevé</span><span class="sxs-lookup"><span data-stu-id="3760b-155">**Cloud-delivered protection level**: High</span></span>
   - <span data-ttu-id="3760b-156">**Délai d’attente étendu du cloud Defender en secondes** : 50</span><span class="sxs-lookup"><span data-stu-id="3760b-156">**Defender Cloud Extended Timeout in Seconds**: 50</span></span>

   :::image type="content" source="images/endpointmgr-antivirus-cloudprotection.png" alt-text="Paramètres Bloquer à la première consultation dans Endpoint Manager":::

4. <span data-ttu-id="3760b-158">Appliquer un profil Antivirus Microsoft Defender à un groupe, tel que **Tous les utilisateurs**, **Tous les appareils** ou **Tous les utilisateurs et tous les appareils**.</span><span class="sxs-lookup"><span data-stu-id="3760b-158">Apply the Microsoft Defender Antivirus profile to a group, such as **All users**, **All devices**, or **All users and devices**.</span></span>

## <a name="turn-on-block-at-first-sight-with-group-policy"></a><span data-ttu-id="3760b-159">Activer la fonctionnalité Bloquer à la première consultation avec une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="3760b-159">Turn on block at first sight with Group Policy</span></span>

> [!NOTE]
> <span data-ttu-id="3760b-160">Nous vous recommandons d’utiliser Intune ou Microsoft Endpoint Manager pour activer Bloquer à la première consultation.</span><span class="sxs-lookup"><span data-stu-id="3760b-160">We recommend using Intune or Microsoft Endpoint Manager to turn on block at first sight.</span></span> 

1. <span data-ttu-id="3760b-161">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console de gestion des stratégies de groupe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), faites un clic droit sur l’objet de stratégie de groupe à configurer, puis sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="3760b-161">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and select **Edit**.</span></span> 

2. <span data-ttu-id="3760b-162">En utilisant **l’Éditeur de gestion des stratégies de groupe**, accédez à **Configuration de l’ordinateur** > **Modèles d’administration** > **Composants Windows** > **Antivirus Microsoft Defender** > **CARTES**.</span><span class="sxs-lookup"><span data-stu-id="3760b-162">Using the **Group Policy Management Editor** go to **Computer configuration** > **Administrative templates** > **Windows Components** > **Microsoft Defender Antivirus** > **MAPS**.</span></span> 

3. <span data-ttu-id="3760b-163">Dans la section CARTES, cliquez deux fois sur **Configurer la fonctionnalité « Bloquer à la première consultation »**, puis configurez-la sur **Activé**, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="3760b-163">In the MAPS section, double-click **Configure the 'Block at First Sight' feature**, and set it to **Enabled**, and then select **OK**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="3760b-164">La configuration sur **Toujours demander (0)** diminuera l’état de protection de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3760b-164">Setting to **Always prompt (0)** will lower the protection state of the device.</span></span> <span data-ttu-id="3760b-165">La configuration sur **Ne jamais envoyer (2)** signifie que Bloquer à la première consultation ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="3760b-165">Setting to **Never send (2)** means block at first sight will not function.</span></span>

4. <span data-ttu-id="3760b-166">Dans la section CARTES, cliquez deux fois sur **Envoyer des échantillons de fichier lorsqu'une analyse supplémentaire est nécessaire**, puis configurez l’option sur **Activé**.</span><span class="sxs-lookup"><span data-stu-id="3760b-166">In the MAPS section, double-click **Send file samples when further analysis is required**, and set it to **Enabled**.</span></span> <span data-ttu-id="3760b-167">Sous **Envoyer des exemples de fichier lorsqu'une analyse supplémentaire est nécessaire**, sélectionnez **Envoyer tous les échantillons**, puis **OK**.</span><span class="sxs-lookup"><span data-stu-id="3760b-167">Under **Send file samples when further analysis is required**, select **Send all samples**, and then select **OK**.</span></span>

5. <span data-ttu-id="3760b-168">Redéployez votre objet de stratégie de groupe sur votre réseau comme vous le faites habituellement.</span><span class="sxs-lookup"><span data-stu-id="3760b-168">Redeploy your Group Policy Object across your network as you usually do.</span></span>

## <a name="confirm-block-at-first-sight-is-enabled-on-individual-client-devices"></a><span data-ttu-id="3760b-169">Confirmer que la fonctionnalité Bloquer à la première consultation est activée sur les appareils client individuels</span><span class="sxs-lookup"><span data-stu-id="3760b-169">Confirm block at first sight is enabled on individual client devices</span></span>

<span data-ttu-id="3760b-170">Vous pouvez confirmer que Bloquer à la première consultation est activé sur des appareils client individuels en utilisant l’application Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="3760b-170">You can confirm that block at first sight is enabled on individual client devices using the Windows Security app.</span></span> <span data-ttu-id="3760b-171">La fonctionnalité Bloquer à la première consultation est automatiquement activée tant que les options **Protection assurée par le cloud** et **Envoi automatique d’un échantillon** sont activées.</span><span class="sxs-lookup"><span data-stu-id="3760b-171">Block at first sight is automatically enabled as long as **Cloud-delivered protection** and **Automatic sample submission** are both turned on.</span></span>

1. <span data-ttu-id="3760b-172">Ouvrez l’application Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="3760b-172">Open the Windows Security app.</span></span>

2. <span data-ttu-id="3760b-173">Sélectionnez **Protection contre les virus et les menaces**, puis sous **Paramètres de protection contre les virus et les menaces**, sélectionnez **Gérer les paramètres**.</span><span class="sxs-lookup"><span data-stu-id="3760b-173">Select **Virus & threat protection**, and then, under **Virus & threat protection settings**, select **Manage Settings**.</span></span>

   ![Capture d’écran de l’étiquette des paramètres de protection contre les virus et les menaces dans l’application Sécurité Windows](images/defender/wdav-protection-settings-wdsc.png)

3. <span data-ttu-id="3760b-175">Confirmez que les options **Protection assurée par le cloud** et **Envoi automatique d’un échantillon** sont activées.</span><span class="sxs-lookup"><span data-stu-id="3760b-175">Confirm that **Cloud-delivered protection** and **Automatic sample submission** are both turned on.</span></span>

> [!NOTE]
> - <span data-ttu-id="3760b-176">Si les paramètres de condition préalable sont configurés et déployés à l’aide d’une stratégie de groupe, les paramètres décrits dans cette section seront grisés et non disponibles pour une utilisation sur des points de terminaison individuels.</span><span class="sxs-lookup"><span data-stu-id="3760b-176">If the prerequisite settings are configured and deployed using Group Policy, the settings described in this section will be greyed-out and unavailable for use on individual endpoints.</span></span> 
> - <span data-ttu-id="3760b-177">Les modifications apportées via un objet de stratégie de groupe doivent d’abord être déployées vers les points de terminaison individuels avant que le paramètre soit mis à jour dans les Paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="3760b-177">Changes made through a Group Policy Object must first be deployed to individual endpoints before the setting will be updated in Windows Settings.</span></span>

## <a name="validate-block-at-first-sight-is-working"></a><span data-ttu-id="3760b-178">Confirmer que le fonctionnement de Bloquer à la première consultation</span><span class="sxs-lookup"><span data-stu-id="3760b-178">Validate block at first sight is working</span></span>

<span data-ttu-id="3760b-179">Pour valider le fonctionnement de la fonctionnalité, téléchargez le [Fichier d’exemple de Bloquer à la première consultation](https://demo.wd.microsoft.com/Page/BAFS).</span><span class="sxs-lookup"><span data-stu-id="3760b-179">To validate that the feature is working, download the [Block at first sight sample file](https://demo.wd.microsoft.com/Page/BAFS).</span></span> <span data-ttu-id="3760b-180">Pour télécharger le fichier, vous avez besoin d’un compte dans Azure AD auquel le rôle Administrateur de sécurité ou le rôle Administrateur général est attribué.</span><span class="sxs-lookup"><span data-stu-id="3760b-180">To download the file, you will need an account in Azure AD that has either the Security Administrator or Global Administrator role assigned.</span></span>

<span data-ttu-id="3760b-181">Pour valider le fonctionnement de la protection activée pour le cloud, suivez les instructions dans [Valider les connexions entre votre réseau et le cloud](configure-network-connections-microsoft-defender-antivirus.md#validate-connections-between-your-network-and-the-cloud).</span><span class="sxs-lookup"><span data-stu-id="3760b-181">To validate that cloud-enabled protection is working, follow the guidance in [Validate connections between your network and the cloud](configure-network-connections-microsoft-defender-antivirus.md#validate-connections-between-your-network-and-the-cloud).</span></span> 

## <a name="turn-off-block-at-first-sight"></a><span data-ttu-id="3760b-182">Désactiver la fonctionnalité Bloquer à la première consultation</span><span class="sxs-lookup"><span data-stu-id="3760b-182">Turn off block at first sight</span></span>

> [!CAUTION]
> <span data-ttu-id="3760b-183">La désactivation de Bloquer à la première consultation diminue le niveau de protection de votre ou vos appareils et de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="3760b-183">Turning off block at first sight will lower the protection state of your device(s) and your network.</span></span>

<span data-ttu-id="3760b-184">Vous pouvez peut-être décider de désactiver Bloquer à la première consultation si vous souhaitez retenir les paramètres de condition préalable sans utiliser réellement la protection Bloquer à la première consultation.</span><span class="sxs-lookup"><span data-stu-id="3760b-184">You might choose to disable block at first sight if you want to retain the prerequisite settings without actually using block at first sight protection.</span></span> <span data-ttu-id="3760b-185">Vous pouvez peut-être désactiver temporairement Bloquer à la première consultation pour voir comment cette fonctionnalité affecte votre réseau.</span><span class="sxs-lookup"><span data-stu-id="3760b-185">You might temporarily turn block at first sight off to see how this feature affects your network.</span></span> <span data-ttu-id="3760b-186">Cependant, nous vous déconseillons de désactiver la protection Bloquer à la première consultation de manière permanente.</span><span class="sxs-lookup"><span data-stu-id="3760b-186">However, we do not recommend disabling block at first sight protection permanently.</span></span>

### <a name="turn-off-block-at-first-sight-with-microsoft-endpoint-manager"></a><span data-ttu-id="3760b-187">Désactiver la fonctionnalité Bloquer à la première consultation avec Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="3760b-187">Turn off block at first sight with Microsoft Endpoint Manager</span></span>

1. <span data-ttu-id="3760b-188">Accédez au Centre d’administration Microsoft Endpoint Manager ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)), puis connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="3760b-188">Go to Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and sign in.</span></span>

2. <span data-ttu-id="3760b-189">Accédez à **Sécurité des points de terminaison** > **Antivirus**, puis sélectionnez votre stratégie Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="3760b-189">Go to **Endpoint security** > **Antivirus**, and then select your Microsoft Defender Antivirus policy.</span></span>

3. <span data-ttu-id="3760b-190">Sous **Gérer**, choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="3760b-190">Under **Manage**, choose **Properties**.</span></span>

4. <span data-ttu-id="3760b-191">Près de **Paramètres de configuration**, choisissez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="3760b-191">Next to **Configuration settings**, choose **Edit**.</span></span>

5. <span data-ttu-id="3760b-192">Modifiez un ou plusieurs des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="3760b-192">Change one or more of the following settings:</span></span>

   - <span data-ttu-id="3760b-193">Définissez **Activer la protection assurée par le cloud** sur **Non** ou sur **Non configuré**.</span><span class="sxs-lookup"><span data-stu-id="3760b-193">Set **Turn on cloud-delivered protection** to **No** or **Not configured**.</span></span>
   - <span data-ttu-id="3760b-194">Définissez **Niveau de protection assuré par le cloud** sur **Non configuré**.</span><span class="sxs-lookup"><span data-stu-id="3760b-194">Set **Cloud-delivered protection level** to **Not configured**.</span></span>
   - <span data-ttu-id="3760b-195">Désactivez la case à cocher pour **Délai d’attente étendu du cloud Defender en secondes**.</span><span class="sxs-lookup"><span data-stu-id="3760b-195">Clear the check box for **Defender Cloud Extended Timeout In Seconds**.</span></span>

6. <span data-ttu-id="3760b-196">Évaluez et enregistrez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="3760b-196">Review and save your settings.</span></span>

### <a name="turn-off-block-at-first-sight-with-group-policy"></a><span data-ttu-id="3760b-197">Désactiver Bloquer à la première consultation à l’aide d’une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="3760b-197">Turn off block at first sight with Group Policy</span></span>

1. <span data-ttu-id="3760b-198">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console de gestion des stratégies de groupe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), faites un clic droit sur l’objet de stratégie de groupe à configurer, puis sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="3760b-198">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure, and then select **Edit**.</span></span>

2. <span data-ttu-id="3760b-199">En utilisant l’**Éditeur de gestion des stratégies de groupe**, accédez à **Configuration ordinateur**, puis sélectionnez **Modèles d’administration**.</span><span class="sxs-lookup"><span data-stu-id="3760b-199">Using the **Group Policy Management Editor** go to **Computer configuration** and select **Administrative templates**.</span></span>

3. <span data-ttu-id="3760b-200">Développez l’arborescence via les **Composants Windows** > **Antivirus Microsoft Defender** > **CARTES**.</span><span class="sxs-lookup"><span data-stu-id="3760b-200">Expand the tree through **Windows components** > **Microsoft Defender Antivirus** > **MAPS**.</span></span>

4. <span data-ttu-id="3760b-201">Cliquez deux fois sur **Configurer la fonctionnalité « Bloquer à la première consultation »**, puis définissez l’option sur **Désactivé**.</span><span class="sxs-lookup"><span data-stu-id="3760b-201">Double-click **Configure the 'Block at First Sight' feature** and set the option to **Disabled**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3760b-202">La désactivation de la fonctionnalité Bloquer à la première consultation ne désactive pas ou n’altère pas les stratégies de groupe de condition préalable.</span><span class="sxs-lookup"><span data-stu-id="3760b-202">Disabling block at first sight does not disable or alter the prerequisite group policies.</span></span>

## <a name="not-an-enterprise-admin-or-it-pro"></a><span data-ttu-id="3760b-203">Vous n’êtes pas un administrateur d’entreprise ou un professionnel de l’informatique ?</span><span class="sxs-lookup"><span data-stu-id="3760b-203">Not an enterprise admin or IT Pro?</span></span>

<span data-ttu-id="3760b-204">Si vous n’êtes pas un administrateur d’entreprise ou un professionnel de l’informatique, mais que vous avez des questions à propos de Bloquer à la première consultation, cette section s’adresse à vous.</span><span class="sxs-lookup"><span data-stu-id="3760b-204">If you are not an enterprise admin or IT Pro, but you have questions about block at first sight, this section is for you.</span></span> <span data-ttu-id="3760b-205">Bloquer à la première consultation est une fonctionnalité de protection de contre les menaces qui détecte et bloque un programme malveillant en quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="3760b-205">Block at first sight is a threat protection feature that detects and blocks malware within seconds.</span></span> <span data-ttu-id="3760b-206">Bien qu’il n’existe aucun paramètre spécifique appelé « Bloquer à la première consultation », la fonctionnalité est activée lorsque certains paramètres sont configurés sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="3760b-206">Although there isn't a specific setting called "Block at first sight," the feature is enabled when certain settings are configured on your device.</span></span>

### <a name="how-to-manage-block-at-first-sight-on-or-off-on-your-own-device"></a><span data-ttu-id="3760b-207">Comment gérer l’activation ou la désactivation de Bloquer à la première consultation sur votre appareil</span><span class="sxs-lookup"><span data-stu-id="3760b-207">How to manage block at first sight on or off on your own device</span></span>

<span data-ttu-id="3760b-208">Si vous disposez d’un appareil personnel qui n’est pas géré par une organisation, vous n’aurez peut-être pas à vous demander comment activer ou désactiver la fonctionnalité Bloquer à la première consultation.</span><span class="sxs-lookup"><span data-stu-id="3760b-208">If you have a personal device that is not managed by an organization, you might be wondering how to turn block at first sight on or off.</span></span> <span data-ttu-id="3760b-209">Vous pouvez utiliser l’application Sécurité Windows pour gérer la fonctionnalité Bloquer à la première consultation.</span><span class="sxs-lookup"><span data-stu-id="3760b-209">You can use the Windows Security app to manage block at first sight.</span></span>

1. <span data-ttu-id="3760b-210">Sur votre ordinateur Windows 10, ouvrez l’application Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="3760b-210">On your Windows 10 computer, open the Windows Security app.</span></span>

2. <span data-ttu-id="3760b-211">Sélectionnez **Protection contre les virus et les menaces**.</span><span class="sxs-lookup"><span data-stu-id="3760b-211">Select **Virus & threat protection**.</span></span>

3. <span data-ttu-id="3760b-212">Sous **Paramètres de protection contre les virus et les menaces**, sélectionnez **Gérer les paramètres**.</span><span class="sxs-lookup"><span data-stu-id="3760b-212">Under **Virus & threat protection settings**, select **Manage settings**.</span></span>

4. <span data-ttu-id="3760b-213">Effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="3760b-213">Take one of the following steps:</span></span>

   - <span data-ttu-id="3760b-214">Pour activer la fonctionnalité Bloquer à la première consultation, vérifiez que les options **Protection assurée par le cloud** et **Envoi automatique d’un échantillon** sont activées.</span><span class="sxs-lookup"><span data-stu-id="3760b-214">To enable block at first sight, make sure that both **Cloud-delivered protection** and **Automatic sample submission** are both turned on.</span></span>

   - <span data-ttu-id="3760b-215">Pour désactiver la fonctionnalité Bloquer à la première consultation, désactivez **Protection assurée par le cloud** ou **Envoi automatique d’un échantillon**.</span><span class="sxs-lookup"><span data-stu-id="3760b-215">To disable block at first sight, turn off **Cloud-delivered protection** or **Automatic sample submission**.</span></span> <br/>
    
     > [!CAUTION]
     > <span data-ttu-id="3760b-216">La désactivation de la fonctionnalité Bloquer à la première consultation diminue le niveau de protection de votre appareil.</span><span class="sxs-lookup"><span data-stu-id="3760b-216">Turning off block at first sight lowers the level of protection for your device.</span></span> <span data-ttu-id="3760b-217">Nous vous déconseillons de désactiver définitivement la fonctionnalité Bloquer à la première consultation.</span><span class="sxs-lookup"><span data-stu-id="3760b-217">We do not recommend permanently disabling block at first sight.</span></span> 


## <a name="see-also"></a><span data-ttu-id="3760b-218">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3760b-218">See also</span></span>

- [<span data-ttu-id="3760b-219">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="3760b-219">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="3760b-220">Protection fournie par le cloud</span><span class="sxs-lookup"><span data-stu-id="3760b-220">Enable cloud-delivered protection</span></span>](enable-cloud-protection-microsoft-defender-antivirus.md)
- [<span data-ttu-id="3760b-221">Restez protégé grâce à la sécurité Windows</span><span class="sxs-lookup"><span data-stu-id="3760b-221">Stay protected with Windows Security</span></span>](https://support.microsoft.com/windows/stay-protected-with-windows-security-2ae0363d-0ada-c064-8b56-6a39afb6a963)
