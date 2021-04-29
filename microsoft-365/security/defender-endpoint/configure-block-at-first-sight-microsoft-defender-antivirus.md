---
title: Activer bloquer à la première vue pour détecter les programmes malveillants en quelques secondes
description: Activer la fonctionnalité Bloquer à la première vue pour détecter et bloquer les programmes malveillants en quelques secondes.
keywords: analyser, bloquer à la première vue, programmes malveillants, première vue, cloud, defender, antivirus
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: priority
author: denisebmsft
ms.author: deniseb
ms.reviewer: marcmcc
manager: dansimp
ms.custom: nextgen
ms.date: 04/28/2021
ms.technology: mde
ms.openlocfilehash: d4db3549d04e5883f02ba263c06371371d385022
ms.sourcegitcommit: 8c89bc1d106b4716b07a1977d57e4d9ef98aecb3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2021
ms.locfileid: "52079202"
---
# <a name="turn-on-block-at-first-sight"></a><span data-ttu-id="8e050-104"> Activer le bloquage à première vue</span><span class="sxs-lookup"><span data-stu-id="8e050-104">Turn on block at first sight</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="8e050-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8e050-105">**Applies to:**</span></span>

- [<span data-ttu-id="8e050-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8e050-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="8e050-107">Cet article décrit une fonctionnalité antivirus/anti-programme malveillant appelée « bloquer à la première vue » et explique comment activer la fonctionnalité Bloquer à la première vue pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8e050-107">This article describes an antivirus/antimalware feature known as "block at first sight", and describes how to enable block at first sight for your organization.</span></span> 

> [!TIP]
> <span data-ttu-id="8e050-108">Cet article est destiné aux administrateurs d'entreprise et aux professionnels de l'informatique qui gèrent les paramètres de sécurité pour les organisations.</span><span class="sxs-lookup"><span data-stu-id="8e050-108">This article is intended for enterprise admins and IT Pros who manage security settings for organizations.</span></span> <span data-ttu-id="8e050-109">Si vous n'êtes pas un administrateur d'entreprise ou un professionnel de l'informatique, mais que vous avez des questions sur bloquer à la première vue, voir Pas un administrateur d'entreprise ou un [professionnel de l'informatique ?](#not-an-enterprise-admin-or-it-pro).</span><span class="sxs-lookup"><span data-stu-id="8e050-109">If you are not an enteprise admin or IT Pro but you have questions about block at first sight, see [Not an enterprise admin or IT Pro?](#not-an-enterprise-admin-or-it-pro).</span></span>

## <a name="what-is-block-at-first-sight"></a><span data-ttu-id="8e050-110">Qu'est-ce que « bloquer à la première vue » ?</span><span class="sxs-lookup"><span data-stu-id="8e050-110">What is "block at first sight"?</span></span>

<span data-ttu-id="8e050-111">Bloquer à la première vue est une fonctionnalité de protection contre les menaces de la nouvelle génération qui détecte les nouveaux programmes malveillants et les bloque en quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="8e050-111">Block at first sight is a threat protection feature of next-generation protection that detects new malware and blocks it within seconds.</span></span> <span data-ttu-id="8e050-112">Bloquer à la première vue est activé lorsque certains paramètres de sécurité sont activés.</span><span class="sxs-lookup"><span data-stu-id="8e050-112">Block at first sight is enabled when certain security settings are enabled.</span></span> <span data-ttu-id="8e050-113">Ces paramètres sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="8e050-113">These settings include:</span></span>

- <span data-ttu-id="8e050-114">Protection cloud</span><span class="sxs-lookup"><span data-stu-id="8e050-114">Cloud-delivered protection;</span></span> 
- <span data-ttu-id="8e050-115">Un délai d'envoi d'exemple spécifié (par exemple, 50 secondes) ; et</span><span class="sxs-lookup"><span data-stu-id="8e050-115">A specified sample submission timeout (such as 50 seconds); and</span></span> 
- <span data-ttu-id="8e050-116">Niveau de blocage de fichiers élevé.</span><span class="sxs-lookup"><span data-stu-id="8e050-116">A file-blocking level of high.</span></span> 

<span data-ttu-id="8e050-117">Dans la plupart des organisations, les paramètres nécessaires pour activer bloquer à la première vue sont configurés avec les déploiements de l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="8e050-117">In most enterprise organizations, the settings needed to enable block at first sight are configured with Microsoft Defender Antivirus deployments.</span></span> 

## <a name="how-it-works"></a><span data-ttu-id="8e050-118">Fonctionnement</span><span class="sxs-lookup"><span data-stu-id="8e050-118">How it works</span></span>

<span data-ttu-id="8e050-119">Lorsque l'Antivirus Microsoft Defender rencontre un fichier suspect mais non détecté, il interroge notre système de protection cloud.</span><span class="sxs-lookup"><span data-stu-id="8e050-119">When Microsoft Defender Antivirus encounters a suspicious but undetected file, it queries our cloud protection backend.</span></span> <span data-ttu-id="8e050-120">Le système back-end cloud applique l'heuristique, l'apprentissage automatique et l'analyse automatisée du fichier pour déterminer si les fichiers sont malveillants ou ne sont pas une menace.</span><span class="sxs-lookup"><span data-stu-id="8e050-120">The cloud backend applies heuristics, machine learning, and automated analysis of the file to determine whether the files are malicious or not a threat.</span></span>

<span data-ttu-id="8e050-121">L'Antivirus Microsoft Defender utilise plusieurs technologies de détection et de prévention pour fournir une protection précise, intelligente et en temps réel.</span><span class="sxs-lookup"><span data-stu-id="8e050-121">Microsoft Defender Antivirus uses multiple detection and prevention technologies to deliver accurate, intelligent, and real-time protection.</span></span> 

![Liste des moteurs de Microsoft Defender AV](images/microsoft-defender-atp-next-generation-protection-engines.png)  

> [!TIP]
> <span data-ttu-id="8e050-123">Pour en savoir plus, consultez ce blog : Découvrez les technologies avancées au cœur de Microsoft Defender pour la protection nouvelle génération de point [de terminaison.](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/)</span><span class="sxs-lookup"><span data-stu-id="8e050-123">To learn more, see this blog: [Get to know the advanced technologies at the core of Microsoft Defender for Endpoint next-generation protection](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/).</span></span>

## <a name="a-few-things-to-know-about-block-at-first-sight"></a><span data-ttu-id="8e050-124">Quelques informations à connaître sur bloquer à la première vue</span><span class="sxs-lookup"><span data-stu-id="8e050-124">A few things to know about block at first sight</span></span>

- <span data-ttu-id="8e050-125">Dans Windows 10, version 1803 ou ultérieure, bloquer à la première vue peut bloquer les fichiers exécutables non portables (tels que JS, VBS ou macros) et les fichiers exécutables.</span><span class="sxs-lookup"><span data-stu-id="8e050-125">In Windows 10, version 1803 or later, block at first sight can block non-portable executable files (such as JS, VBS, or macros) and executable files.</span></span>

- <span data-ttu-id="8e050-126">Bloquer à la première vue utilise uniquement le système de protection cloud pour les fichiers exécutables et les fichiers exécutables non portables qui sont téléchargés à partir d'Internet ou qui proviennent de la zone Internet.</span><span class="sxs-lookup"><span data-stu-id="8e050-126">Block at first sight only uses the cloud protection backend for executable files and non-portable executable files that are downloaded from the Internet, or that originate from the Internet zone.</span></span> <span data-ttu-id="8e050-127">Une valeur de hachage du fichier .exe est vérifiée via le système backend cloud pour déterminer si le fichier est un fichier précédemment non détecté.</span><span class="sxs-lookup"><span data-stu-id="8e050-127">A hash value of the .exe file is checked via the cloud backend to determine if the file is a previously undetected file.</span></span>

- <span data-ttu-id="8e050-128">Si le système cloud backend ne parvient pas à effectuer une détermination, l'Antivirus Microsoft Defender verrouille le fichier et charge une copie dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="8e050-128">If the cloud backend is unable to make a determination, Microsoft Defender Antivirus locks the file and uploads a copy to the cloud.</span></span> <span data-ttu-id="8e050-129">Le cloud effectue davantage d'analyses pour parvenir à une détermination avant d'autoriser l'exécution du fichier ou de le bloquer dans toutes les futures rencontres, selon qu'il détermine si le fichier est malveillant ou non une menace.</span><span class="sxs-lookup"><span data-stu-id="8e050-129">The cloud performs more analysis to reach a determination before it either allows the file to run or blocks it in all future encounters, depending on whether it determines the file to be malicious or not a threat.</span></span>

- <span data-ttu-id="8e050-130">Dans de nombreux cas, ce processus peut réduire le temps de réponse des nouveaux programmes malveillants de plusieurs heures à quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="8e050-130">In many cases, this process can reduce the response time for new malware from hours to seconds.</span></span>

- <span data-ttu-id="8e050-131">Vous pouvez [spécifier la durée d'exécution](configure-cloud-block-timeout-period-microsoft-defender-antivirus.md) d'un fichier pendant que le service de protection informatique analyse le fichier.</span><span class="sxs-lookup"><span data-stu-id="8e050-131">You can [specify how long a file should be prevented from running](configure-cloud-block-timeout-period-microsoft-defender-antivirus.md) while the cloud-based protection service analyzes the file.</span></span> <span data-ttu-id="8e050-132">De plus, vous pouvez personnaliser le message affiché sur le bureau des [utilisateurs](/windows/security/threat-protection//windows-defender-security-center/wdsc-customize-contact-information.md) lorsqu'un fichier est bloqué.</span><span class="sxs-lookup"><span data-stu-id="8e050-132">And, you can [customize the message displayed on users' desktops](/windows/security/threat-protection//windows-defender-security-center/wdsc-customize-contact-information.md) when a file is blocked.</span></span> <span data-ttu-id="8e050-133">Vous pouvez modifier le nom de la société, les informations de contact et l'URL du message.</span><span class="sxs-lookup"><span data-stu-id="8e050-133">You can change the company name, contact information, and message URL.</span></span>

## <a name="turn-on-block-at-first-sight-with-microsoft-intune"></a><span data-ttu-id="8e050-134">Activer bloquer à la première vue avec Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="8e050-134">Turn on block at first sight with Microsoft Intune</span></span>

> [!TIP]
> <span data-ttu-id="8e050-135">Microsoft Intune fait désormais partie de Microsoft Endpoint Manager.</span><span class="sxs-lookup"><span data-stu-id="8e050-135">Microsoft Intune is now part of Microsoft Endpoint Manager.</span></span>

1. <span data-ttu-id="8e050-136">Dans le Centre d'administration Microsoft Endpoint Manager ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ), accédez aux **profils**  >  **de configuration des appareils.**</span><span class="sxs-lookup"><span data-stu-id="8e050-136">In the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)), navigate to **Devices** > **Configuration profiles**.</span></span>

2. <span data-ttu-id="8e050-137">Sélectionnez ou créez un profil à l'aide du type de profil **Restrictions d'appareil.**</span><span class="sxs-lookup"><span data-stu-id="8e050-137">Select or create a profile using the **Device restrictions** profile type.</span></span>

3. <span data-ttu-id="8e050-138">Dans les **paramètres de configuration du** profil restrictions d'appareil, définissez ou confirmez les paramètres suivants sous **l'Antivirus Microsoft Defender**:</span><span class="sxs-lookup"><span data-stu-id="8e050-138">In the **Configuration settings** for the Device restrictions profile, set or confirm the following settings under **Microsoft Defender Antivirus**:</span></span>

   - <span data-ttu-id="8e050-139">**Protection cloud :** activée</span><span class="sxs-lookup"><span data-stu-id="8e050-139">**Cloud-delivered protection**: Enabled</span></span>
   - <span data-ttu-id="8e050-140">**Niveau de blocage de fichiers**: Élevé</span><span class="sxs-lookup"><span data-stu-id="8e050-140">**File Blocking Level**: High</span></span>
   - <span data-ttu-id="8e050-141">**Extension de temps pour l'analyse de fichiers par le cloud**: 50</span><span class="sxs-lookup"><span data-stu-id="8e050-141">**Time extension for file scanning by the cloud**: 50</span></span>
   - <span data-ttu-id="8e050-142">**Invite des utilisateurs avant l'envoi** de l'échantillon : envoyer toutes les données sans invite</span><span class="sxs-lookup"><span data-stu-id="8e050-142">**Prompt users before sample submission**: Send all data without prompting</span></span>

   ![Config Intune](images/defender/intune-block-at-first-sight.png)

4. <span data-ttu-id="8e050-144">Enregistrez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="8e050-144">Save your settings.</span></span>

> [!TIP]
> - <span data-ttu-id="8e050-145">La définition du niveau de blocage de fichiers **sur Élevé** applique un niveau élevé de détection.</span><span class="sxs-lookup"><span data-stu-id="8e050-145">Setting the file blocking level to **High** applies a strong level of detection.</span></span> <span data-ttu-id="8e050-146">Dans le cas peu probable que le blocage de fichiers entraîne une détection de faux positifs de fichiers légitimes, votre équipe des opérations de sécurité peut restaurer les [fichiers mis en quarantaine.](./restore-quarantined-files-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="8e050-146">In the unlikely event that file blocking causes a false positive detection of legitimate files, your security operations team can [restore quarantined files](./restore-quarantined-files-microsoft-defender-antivirus.md).</span></span>
> - <span data-ttu-id="8e050-147">Pour plus d'informations sur la configuration des restrictions d'appareil de l'Antivirus Microsoft Defender dans Intune, voir Configurer les paramètres de [restriction d'appareil dans Microsoft Intune.](/intune/device-restrictions-configure)</span><span class="sxs-lookup"><span data-stu-id="8e050-147">For more information about configuring Microsoft Defender Antivirus device restrictions in Intune, see [Configure device restriction settings in Microsoft Intune](/intune/device-restrictions-configure).</span></span>
> - <span data-ttu-id="8e050-148">Pour obtenir la liste des restrictions d'appareil de l'Antivirus Microsoft Defender dans Intune, voir Restriction d'appareil pour les [paramètres Windows 10 (et](/intune/device-restrictions-windows-10#microsoft-defender-antivirus)les plus nouveaux) dans Intune.</span><span class="sxs-lookup"><span data-stu-id="8e050-148">For a list of Microsoft Defender Antivirus device restrictions in Intune, see [Device restriction for Windows 10 (and newer) settings in Intune](/intune/device-restrictions-windows-10#microsoft-defender-antivirus).</span></span>

## <a name="turn-on-block-at-first-sight-with-microsoft-endpoint-manager"></a><span data-ttu-id="8e050-149">Activer bloquer à la première vue avec Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="8e050-149">Turn on block at first sight with Microsoft Endpoint Manager</span></span>

> [!TIP]
> <span data-ttu-id="8e050-150">Si vous recherchez Microsoft Endpoint Configuration Manager, il fait désormais partie de Microsoft Endpoint Manager.</span><span class="sxs-lookup"><span data-stu-id="8e050-150">If you're looking for Microsoft Endpoint Configuration Manager, it's now part of Microsoft Endpoint Manager.</span></span>

1. <span data-ttu-id="8e050-151">Dans Microsoft Endpoint Manager ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ), go to **Endpoint security**  >  **Antivirus**.</span><span class="sxs-lookup"><span data-stu-id="8e050-151">In Microsoft Endpoint Manager ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)), go to **Endpoint security** > **Antivirus**.</span></span>

2. <span data-ttu-id="8e050-152">Sélectionnez une stratégie existante ou créez une stratégie à l'aide du type de profil **Antivirus Microsoft Defender.**</span><span class="sxs-lookup"><span data-stu-id="8e050-152">Select an existing policy, or create a new policy using the **Microsoft Defender Antivirus** profile type.</span></span>

3. <span data-ttu-id="8e050-153">Définissez ou confirmez les paramètres de configuration suivants :</span><span class="sxs-lookup"><span data-stu-id="8e050-153">Set or confirm the following configuration settings:</span></span>

   - <span data-ttu-id="8e050-154">**Activer la protection cloud :** Oui</span><span class="sxs-lookup"><span data-stu-id="8e050-154">**Turn on cloud-delivered protection**: Yes</span></span>
   - <span data-ttu-id="8e050-155">**Niveau de protection cloud :** élevé</span><span class="sxs-lookup"><span data-stu-id="8e050-155">**Cloud-delivered protection level**: High</span></span>
   - <span data-ttu-id="8e050-156">**Délai d'out étendu de Defender Cloud en secondes**: 50</span><span class="sxs-lookup"><span data-stu-id="8e050-156">**Defender Cloud Extended Timeout in Seconds**: 50</span></span>

   :::image type="content" source="images/endpointmgr-antivirus-cloudprotection.png" alt-text="Bloquer les paramètres à la première vue dans le Gestionnaire de point de terminaison":::

4. <span data-ttu-id="8e050-158">Appliquez le profil antivirus Microsoft Defender à un groupe, tel que Tous les utilisateurs, Tous les **appareils** ou Tous **les utilisateurs et appareils.**</span><span class="sxs-lookup"><span data-stu-id="8e050-158">Apply the Microsoft Defender Antivirus profile to a group, such as **All users**, **All devices**, or **All users and devices**.</span></span>

## <a name="turn-on-block-at-first-sight-with-group-policy"></a><span data-ttu-id="8e050-159">Activer bloquer à la première vue avec la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8e050-159">Turn on block at first sight with Group Policy</span></span>

> [!NOTE]
> <span data-ttu-id="8e050-160">Nous vous recommandons d'utiliser Intune ou Microsoft Endpoint Manager pour activer bloquer à la première vue.</span><span class="sxs-lookup"><span data-stu-id="8e050-160">We recommend using Intune or Microsoft Endpoint Manager to turn on block at first sight.</span></span> 

1. <span data-ttu-id="8e050-161">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe que vous souhaitez configurer et sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="8e050-161">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and select **Edit**.</span></span> 

2. <span data-ttu-id="8e050-162">À **l'aide de l'Éditeur de gestion des stratégies** de groupe, go to **Computer configuration**  >  **Administrative**  >  **templates Windows Components**  >  **Microsoft Defender Antivirus**  >  **MAPS**.</span><span class="sxs-lookup"><span data-stu-id="8e050-162">Using the **Group Policy Management Editor** go to **Computer configuration** > **Administrative templates** > **Windows Components** > **Microsoft Defender Antivirus** > **MAPS**.</span></span> 

3. <span data-ttu-id="8e050-163">Dans la section MAPS, double-cliquez sur **Configurer** la fonctionnalité « Bloquer à la première vue » et définissez-la sur **Activé,** puis sélectionnez **OK.**</span><span class="sxs-lookup"><span data-stu-id="8e050-163">In the MAPS section, double-click **Configure the 'Block at First Sight' feature**, and set it to **Enabled**, and then select **OK**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="8e050-164">Le fait **de définir Always prompt (0)** réduit l'état de protection de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="8e050-164">Setting to **Always prompt (0)** will lower the protection state of the device.</span></span> <span data-ttu-id="8e050-165">Le paramètre **Ne jamais envoyer (2)** signifie que bloquer à la première vue ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="8e050-165">Setting to **Never send (2)** means block at first sight will not function.</span></span>

4. <span data-ttu-id="8e050-166">Dans la section MAPS, double-cliquez sur Envoyer des **exemples** de fichiers lorsque d'autres analyses sont requises et définissez-la **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="8e050-166">In the MAPS section, double-click **Send file samples when further analysis is required**, and set it to **Enabled**.</span></span> <span data-ttu-id="8e050-167">Sous **Envoyer des exemples de fichier lorsque d'autres analyses sont** **requises, sélectionnez Envoyer** tous les exemples, puis **sélectionnez OK.**</span><span class="sxs-lookup"><span data-stu-id="8e050-167">Under **Send file samples when further analysis is required**, select **Send all samples**, and then select **OK**.</span></span>

5. <span data-ttu-id="8e050-168">Redéployer votre objet de stratégie de groupe sur votre réseau comme vous le faites généralement.</span><span class="sxs-lookup"><span data-stu-id="8e050-168">Redeploy your Group Policy Object across your network as you usually do.</span></span>

## <a name="confirm-block-at-first-sight-is-enabled-on-individual-client-devices"></a><span data-ttu-id="8e050-169">Vérifier que bloquer à la première vue est activé sur des appareils clients individuels</span><span class="sxs-lookup"><span data-stu-id="8e050-169">Confirm block at first sight is enabled on individual client devices</span></span>

<span data-ttu-id="8e050-170">Vous pouvez vérifier que bloquer à la première vue est activé sur des appareils clients individuels à l'aide de l'application Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="8e050-170">You can confirm that block at first sight is enabled on individual client devices using the Windows Security app.</span></span> <span data-ttu-id="8e050-171">Bloquer à la première vue est automatiquement activé tant  que la protection cloud **et** l'envoi automatique d'échantillons sont tous deux activés.</span><span class="sxs-lookup"><span data-stu-id="8e050-171">Block at first sight is automatically enabled as long as **Cloud-delivered protection** and **Automatic sample submission** are both turned on.</span></span>

1. <span data-ttu-id="8e050-172">Ouvrez l'application Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="8e050-172">Open the Windows Security app.</span></span>

2. <span data-ttu-id="8e050-173">Sélectionnez **Protection & virus** contre les **menaces,** puis, sous Paramètres de protection contre & virus, sélectionnez Gérer **les paramètres.**</span><span class="sxs-lookup"><span data-stu-id="8e050-173">Select **Virus & threat protection**, and then, under **Virus & threat protection settings**, select **Manage Settings**.</span></span>

   ![Capture d'écran de l'étiquette & protection contre les virus dans l'application Sécurité Windows](images/defender/wdav-protection-settings-wdsc.png)

3. <span data-ttu-id="8e050-175">Confirmez **que la protection du cloud et** l'envoi automatique **d'échantillons** sont tous deux allumés.</span><span class="sxs-lookup"><span data-stu-id="8e050-175">Confirm that **Cloud-delivered protection** and **Automatic sample submission** are both turned on.</span></span>

> [!NOTE]
> - <span data-ttu-id="8e050-176">Si les paramètres prérequis sont configurés et déployés à l'aide de la stratégie de groupe, les paramètres décrits dans cette section sont grisés et ne peuvent pas être utilisés sur des points de terminaison individuels.</span><span class="sxs-lookup"><span data-stu-id="8e050-176">If the prerequisite settings are configured and deployed using Group Policy, the settings described in this section will be greyed-out and unavailable for use on individual endpoints.</span></span> 
> - <span data-ttu-id="8e050-177">Les modifications apportées via un objet de stratégie de groupe doivent d'abord être déployées sur des points de terminaison individuels avant que le paramètre ne soit mis à jour dans les paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="8e050-177">Changes made through a Group Policy Object must first be deployed to individual endpoints before the setting will be updated in Windows Settings.</span></span>

## <a name="validate-block-at-first-sight-is-working"></a><span data-ttu-id="8e050-178">Vérifier que bloquer à la première vue fonctionne</span><span class="sxs-lookup"><span data-stu-id="8e050-178">Validate block at first sight is working</span></span>

<span data-ttu-id="8e050-179">Pour vérifier que la fonctionnalité fonctionne, suivez les instructions de Validation des [connexions entre votre réseau et le cloud.](configure-network-connections-microsoft-defender-antivirus.md#validate-connections-between-your-network-and-the-cloud)</span><span class="sxs-lookup"><span data-stu-id="8e050-179">To validate that the feature is working, follow the guidance in [Validate connections between your network and the cloud](configure-network-connections-microsoft-defender-antivirus.md#validate-connections-between-your-network-and-the-cloud).</span></span>

## <a name="turn-off-block-at-first-sight"></a><span data-ttu-id="8e050-180">Désactiver bloquer à la première vue</span><span class="sxs-lookup"><span data-stu-id="8e050-180">Turn off block at first sight</span></span>

> [!CAUTION]
> <span data-ttu-id="8e050-181">La non-utilisation du blocage à la première vue réduit l'état de protection de vos appareils et de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="8e050-181">Turning off block at first sight will lower the protection state of your device(s) and your network.</span></span>

<span data-ttu-id="8e050-182">Vous pouvez choisir de désactiver bloquer à la première vue si vous souhaitez conserver les paramètres prérequis sans utiliser réellement la protection bloquer à la première vue.</span><span class="sxs-lookup"><span data-stu-id="8e050-182">You might choose to disable block at first sight if you want to retain the prerequisite settings without actually using block at first sight protection.</span></span> <span data-ttu-id="8e050-183">Vous pouvez désactiver temporairement bloquer à la première vue pour voir l'impact de cette fonctionnalité sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="8e050-183">You might temporarily turn block at first sight off to see how this feature affects your network.</span></span> <span data-ttu-id="8e050-184">Toutefois, nous vous déconseillons de désactiver définitivement la protection bloquer à la première vue.</span><span class="sxs-lookup"><span data-stu-id="8e050-184">However, we do not recommend disabling block at first sight protection permanently.</span></span>

### <a name="turn-off-block-at-first-sight-with-microsoft-endpoint-manager"></a><span data-ttu-id="8e050-185">Désactiver bloquer à la première vue avec Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="8e050-185">Turn off block at first sight with Microsoft Endpoint Manager</span></span>

1. <span data-ttu-id="8e050-186">Go to Microsoft Endpoint Manager admin center ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="8e050-186">Go to Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and sign in.</span></span>

2. <span data-ttu-id="8e050-187">Go to **Endpoint security**  >  **Antivirus,** and then select your Microsoft Defender Antivirus policy.</span><span class="sxs-lookup"><span data-stu-id="8e050-187">Go to **Endpoint security** > **Antivirus**, and then select your Microsoft Defender Antivirus policy.</span></span>

3. <span data-ttu-id="8e050-188">Under **Manage**, choose **Properties**.</span><span class="sxs-lookup"><span data-stu-id="8e050-188">Under **Manage**, choose **Properties**.</span></span>

4. <span data-ttu-id="8e050-189">En de côté **des paramètres de configuration,** choisissez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="8e050-189">Next to **Configuration settings**, choose **Edit**.</span></span>

5. <span data-ttu-id="8e050-190">Modifiez un ou plusieurs des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e050-190">Change one or more of the following settings:</span></span>

   - <span data-ttu-id="8e050-191">Définissez **Activer la protection cloud sur** **Non** ou **Non configuré.**</span><span class="sxs-lookup"><span data-stu-id="8e050-191">Set **Turn on cloud-delivered protection** to **No** or **Not configured**.</span></span>
   - <span data-ttu-id="8e050-192">Définissez **le niveau de protection livré par le cloud** sur Non **configuré.**</span><span class="sxs-lookup"><span data-stu-id="8e050-192">Set **Cloud-delivered protection level** to **Not configured**.</span></span>
   - <span data-ttu-id="8e050-193">Clear the check box for **Defender Cloud Extended Timeout In Seconds**.</span><span class="sxs-lookup"><span data-stu-id="8e050-193">Clear the check box for **Defender Cloud Extended Timeout In Seconds**.</span></span>

6. <span data-ttu-id="8e050-194">Examinez et enregistrez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="8e050-194">Review and save your settings.</span></span>

### <a name="turn-off-block-at-first-sight-with-group-policy"></a><span data-ttu-id="8e050-195">Désactiver bloquer à la première vue avec la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8e050-195">Turn off block at first sight with Group Policy</span></span>

1. <span data-ttu-id="8e050-196">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe à configurer, puis sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="8e050-196">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure, and then select **Edit**.</span></span>

2. <span data-ttu-id="8e050-197">À **l'aide de l'Éditeur de gestion des stratégies** de groupe, sélectionnez **Configuration** ordinateur et **sélectionnez Modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="8e050-197">Using the **Group Policy Management Editor** go to **Computer configuration** and select **Administrative templates**.</span></span>

3. <span data-ttu-id="8e050-198">Développez l'arborescence à **travers les composants Windows** Microsoft Defender  >  **Antivirus**  >  **MAPS**.</span><span class="sxs-lookup"><span data-stu-id="8e050-198">Expand the tree through **Windows components** > **Microsoft Defender Antivirus** > **MAPS**.</span></span>

4. <span data-ttu-id="8e050-199">Double-cliquez **sur Configurer la fonctionnalité «** Bloquer à la première vue » et définissez l'option sur **Désactivé.**</span><span class="sxs-lookup"><span data-stu-id="8e050-199">Double-click **Configure the 'Block at First Sight' feature** and set the option to **Disabled**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e050-200">La désactivation de bloquer à la première vue ne désactive pas ou ne modifie pas les stratégies de groupe prérequises.</span><span class="sxs-lookup"><span data-stu-id="8e050-200">Disabling block at first sight does not disable or alter the prerequisite group policies.</span></span>

## <a name="not-an-enterprise-admin-or-it-pro"></a><span data-ttu-id="8e050-201">Vous n'êtes pas un administrateur d'entreprise ou un professionnel de l'informatique ?</span><span class="sxs-lookup"><span data-stu-id="8e050-201">Not an enterprise admin or IT Pro?</span></span>

<span data-ttu-id="8e050-202">Si vous n'êtes pas un administrateur d'entreprise ou un professionnel de l'informatique, mais que vous avez des questions sur bloquer à la première vue, cette section est pour vous.</span><span class="sxs-lookup"><span data-stu-id="8e050-202">If you are not an enterprise admin or IT Pro, but you have questions about block at first sight, this section is for you.</span></span> <span data-ttu-id="8e050-203">Bloquer à la première vue est une fonctionnalité de protection contre les menaces qui détecte et bloque les programmes malveillants en quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="8e050-203">Block at first sight is a threat protection feature that detects and blocks malware within seconds.</span></span> <span data-ttu-id="8e050-204">Bien qu'il n'existe pas de paramètre spécifique appelé « Bloquer à la première vue », la fonctionnalité est activée lorsque certains paramètres sont configurés sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="8e050-204">Although there isn't a specific setting called "Block at first sight," the feature is enabled when certain settings are configured on your device.</span></span>

### <a name="how-to-manage-block-at-first-sight-on-or-off-on-your-own-device"></a><span data-ttu-id="8e050-205">Comment gérer bloquer à la première vue sur ou hors de votre propre appareil</span><span class="sxs-lookup"><span data-stu-id="8e050-205">How to manage block at first sight on or off on your own device</span></span>

<span data-ttu-id="8e050-206">Si vous avez un appareil personnel qui n'est pas géré par une organisation, vous vous demandez peut-être comment activer ou désactiver bloquer à la première vue.</span><span class="sxs-lookup"><span data-stu-id="8e050-206">If you have a personal device that is not managed by an organization, you might be wondering how to turn block at first sight on or off.</span></span> <span data-ttu-id="8e050-207">Vous pouvez utiliser l'application Sécurité Windows pour gérer bloquer à la première vue.</span><span class="sxs-lookup"><span data-stu-id="8e050-207">You can use the Windows Security app to manage block at first sight.</span></span>

1. <span data-ttu-id="8e050-208">Sur votre ordinateur Windows 10, ouvrez l'application Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="8e050-208">On your Windows 10 computer, open the Windows Security app.</span></span>

2. <span data-ttu-id="8e050-209">Sélectionnez **Protection contre & virus**.</span><span class="sxs-lookup"><span data-stu-id="8e050-209">Select **Virus & threat protection**.</span></span>

3. <span data-ttu-id="8e050-210">Sous Paramètres & protection contre les virus contre les **menaces,** **sélectionnez Gérer les paramètres.**</span><span class="sxs-lookup"><span data-stu-id="8e050-210">Under **Virus & threat protection settings**, select **Manage settings**.</span></span>

4. <span data-ttu-id="8e050-211">Effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e050-211">Take one of the following steps:</span></span>

   - <span data-ttu-id="8e050-212">Pour activer bloquer à la première vue, **assurez-vous** que la protection cloud et l'envoi automatique d'échantillons sont tous deux activés. </span><span class="sxs-lookup"><span data-stu-id="8e050-212">To enable block at first sight, make sure that both **Cloud-delivered protection** and **Automatic sample submission** are both turned on.</span></span>

   - <span data-ttu-id="8e050-213">Pour désactiver bloquer à la première vue, désactivez la protection cloud **ou** l'envoi **automatique d'échantillons.**</span><span class="sxs-lookup"><span data-stu-id="8e050-213">To disable block at first sight, turn off **Cloud-delivered protection** or **Automatic sample submission**.</span></span> <br/>
    
     > [!CAUTION]
     > <span data-ttu-id="8e050-214">La non-utilisation du blocage à la première vue réduit le niveau de protection de votre appareil.</span><span class="sxs-lookup"><span data-stu-id="8e050-214">Turning off block at first sight lowers the level of protection for your device.</span></span> <span data-ttu-id="8e050-215">Nous vous déconseillons de désactiver définitivement bloquer à la première vue.</span><span class="sxs-lookup"><span data-stu-id="8e050-215">We do not recommend permanently disabling block at first sight.</span></span> 


## <a name="see-also"></a><span data-ttu-id="8e050-216">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e050-216">See also</span></span>

- [<span data-ttu-id="8e050-217">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="8e050-217">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="8e050-218">Activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="8e050-218">Enable cloud-delivered protection</span></span>](enable-cloud-protection-microsoft-defender-antivirus.md)
- [<span data-ttu-id="8e050-219">Restez protégé avec la sécurité Windows</span><span class="sxs-lookup"><span data-stu-id="8e050-219">Stay protected with Windows Security</span></span>](https://support.microsoft.com/windows/stay-protected-with-windows-security-2ae0363d-0ada-c064-8b56-6a39afb6a963)