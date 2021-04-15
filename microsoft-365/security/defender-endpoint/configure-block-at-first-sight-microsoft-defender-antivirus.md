---
title: Activer bloquer à la première vue pour détecter les programmes malveillants en quelques secondes
description: Activer la fonctionnalité Bloquer à la première vue pour détecter et bloquer les programmes malveillants en quelques secondes.
keywords: analyse, BAFS, programmes malveillants, première vue, première vue, cloud, defender
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: priority
author: denisebmsft
ms.author: deniseb
ms.reviewer: ''
manager: dansimp
ms.custom: nextgen
ms.date: 10/22/2020
ms.technology: mde
ms.openlocfilehash: 1baa770da677ec755bd56db9b92c071680efae7b
ms.sourcegitcommit: 7a339c9f7039825d131b39481ddf54c57b021b11
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51765754"
---
# <a name="turn-on-block-at-first-sight"></a><span data-ttu-id="7bca4-104">Activer bloquer à la première vue</span><span class="sxs-lookup"><span data-stu-id="7bca4-104">Turn on block at first sight</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="7bca4-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="7bca4-105">**Applies to:**</span></span>

- [<span data-ttu-id="7bca4-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7bca4-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="7bca4-107">Bloquer à la première vue permet de détecter et de bloquer de nouveaux programmes malveillants en quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="7bca4-107">Block at first sight provides a way to detect and block new malware within seconds.</span></span> <span data-ttu-id="7bca4-108">Cette protection est activée par défaut lorsque certains paramètres prérequis sont activés.</span><span class="sxs-lookup"><span data-stu-id="7bca4-108">This protection is enabled by default when certain prerequisite settings are enabled.</span></span> <span data-ttu-id="7bca4-109">Ces paramètres incluent la protection de cloud, un délai d'envoi d'exemple spécifié (par exemple, 50 secondes) et un niveau de blocage de fichiers élevé.</span><span class="sxs-lookup"><span data-stu-id="7bca4-109">These settings include cloud-delivered protection, a specified sample submission timeout (such as 50 seconds), and a file-blocking level of high.</span></span> <span data-ttu-id="7bca4-110">Dans la plupart des organisations, ces paramètres sont activés par défaut avec les déploiements de l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="7bca4-110">In most enterprise organizations, these settings are enabled by default with Microsoft Defender Antivirus deployments.</span></span> 

<span data-ttu-id="7bca4-111">Vous pouvez [spécifier la durée d'exécution](configure-cloud-block-timeout-period-microsoft-defender-antivirus.md) d'un fichier pendant que le service de protection informatique analyse le fichier.</span><span class="sxs-lookup"><span data-stu-id="7bca4-111">You can [specify how long a file should be prevented from running](configure-cloud-block-timeout-period-microsoft-defender-antivirus.md) while the cloud-based protection service analyzes the file.</span></span> <span data-ttu-id="7bca4-112">De plus, vous pouvez personnaliser le message affiché sur le bureau des [utilisateurs](/windows/security/threat-protection//windows-defender-security-center/wdsc-customize-contact-information.md) lorsqu'un fichier est bloqué.</span><span class="sxs-lookup"><span data-stu-id="7bca4-112">And, you can [customize the message displayed on users' desktops](/windows/security/threat-protection//windows-defender-security-center/wdsc-customize-contact-information.md) when a file is blocked.</span></span> <span data-ttu-id="7bca4-113">Vous pouvez modifier le nom de la société, les informations de contact et l'URL du message.</span><span class="sxs-lookup"><span data-stu-id="7bca4-113">You can change the company name, contact information, and message URL.</span></span>

>[!TIP]
><span data-ttu-id="7bca4-114">Visitez le site web de démonstration Microsoft Defender for Endpoint [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) pour vérifier que les fonctionnalités fonctionnent et voir comment elles fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="7bca4-114">Visit the Microsoft Defender for Endpoint demo website at [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) to confirm the features are working and see how they work.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="7bca4-115">Mode de fonctionnement</span><span class="sxs-lookup"><span data-stu-id="7bca4-115">How it works</span></span>

<span data-ttu-id="7bca4-116">Lorsque l'Antivirus Microsoft Defender rencontre un fichier suspect mais non détecté, il interroge notre système de protection cloud.</span><span class="sxs-lookup"><span data-stu-id="7bca4-116">When Microsoft Defender Antivirus encounters a suspicious but undetected file, it queries our cloud protection backend.</span></span> <span data-ttu-id="7bca4-117">Le système back-end cloud applique l'heuristique, l'apprentissage automatique et l'analyse automatisée du fichier pour déterminer si les fichiers sont malveillants ou ne sont pas une menace.</span><span class="sxs-lookup"><span data-stu-id="7bca4-117">The cloud backend applies heuristics, machine learning, and automated analysis of the file to determine whether the files are malicious or not a threat.</span></span>

<span data-ttu-id="7bca4-118">L'Antivirus Microsoft Defender utilise plusieurs technologies de détection et de prévention pour fournir une protection précise, intelligente et en temps réel.</span><span class="sxs-lookup"><span data-stu-id="7bca4-118">Microsoft Defender Antivirus uses multiple detection and prevention technologies to deliver accurate, intelligent, and real-time protection.</span></span> <span data-ttu-id="7bca4-119">Pour en savoir plus, consultez ce blog : Découvrez les technologies avancées au cœur de Microsoft Defender pour la protection nouvelle génération de point [de terminaison.](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/)</span><span class="sxs-lookup"><span data-stu-id="7bca4-119">To learn more, see this blog: [Get to know the advanced technologies at the core of Microsoft Defender for Endpoint next-generation protection](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/).</span></span>
<span data-ttu-id="7bca4-120">![Liste des moteurs de Microsoft Defender AV](images/microsoft-defender-atp-next-generation-protection-engines.png)</span><span class="sxs-lookup"><span data-stu-id="7bca4-120">![List of Microsoft Defender AV engines](images/microsoft-defender-atp-next-generation-protection-engines.png)</span></span>  

<span data-ttu-id="7bca4-121">Dans Windows 10, version 1803 ou ultérieure, bloquer à la première vue peut bloquer les fichiers exécutables non portables (tels que JS, VBS ou macros) ainsi que les fichiers exécutables.</span><span class="sxs-lookup"><span data-stu-id="7bca4-121">In Windows 10, version 1803 or later, block at first sight can block non-portable executable files (such as JS, VBS, or macros) as well as executable files.</span></span>

<span data-ttu-id="7bca4-122">Bloquer à la première vue utilise uniquement le système de protection cloud pour les fichiers exécutables et les fichiers exécutables non portables qui sont téléchargés à partir d'Internet ou qui proviennent de la zone Internet.</span><span class="sxs-lookup"><span data-stu-id="7bca4-122">Block at first sight only uses the cloud protection backend for executable files and non-portable executable files that are downloaded from the Internet, or that originate from the Internet zone.</span></span> <span data-ttu-id="7bca4-123">Une valeur de hachage du fichier .exe est vérifiée via le système backend cloud pour déterminer si le fichier est un fichier précédemment non détecté.</span><span class="sxs-lookup"><span data-stu-id="7bca4-123">A hash value of the .exe file is checked via the cloud backend to determine if the file is a previously undetected file.</span></span>

<span data-ttu-id="7bca4-124">Si le système cloud backend ne parvient pas à effectuer une détermination, l'Antivirus Microsoft Defender verrouille le fichier et charge une copie dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="7bca4-124">If the cloud backend is unable to make a determination, Microsoft Defender Antivirus locks the file and uploads a copy to the cloud.</span></span> <span data-ttu-id="7bca4-125">Le cloud effectue une analyse supplémentaire pour parvenir à une détermination avant d'autoriser le fichier à s'exécuter ou de le bloquer dans toutes les futures rencontres, selon qu'il détermine si le fichier est malveillant ou sécurisé.</span><span class="sxs-lookup"><span data-stu-id="7bca4-125">The cloud performs additional analysis to reach a determination before it either allows the file to run or blocks it in all future encounters, depending on whether it determines the file to be malicious or safe.</span></span>

<span data-ttu-id="7bca4-126">Dans de nombreux cas, ce processus peut réduire le temps de réponse des nouveaux programmes malveillants de plusieurs heures à quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="7bca4-126">In many cases, this process can reduce the response time for new malware from hours to seconds.</span></span>

## <a name="turn-on-block-at-first-sight-with-microsoft-intune"></a><span data-ttu-id="7bca4-127">Activer bloquer à la première vue avec Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="7bca4-127">Turn on block at first sight with Microsoft Intune</span></span>

> [!TIP]
> <span data-ttu-id="7bca4-128">Microsoft Intune fait désormais partie de Microsoft Endpoint Manager.</span><span class="sxs-lookup"><span data-stu-id="7bca4-128">Microsoft Intune is now part of Microsoft Endpoint Manager.</span></span>

1. <span data-ttu-id="7bca4-129">Dans le Centre d'administration Microsoft Endpoint Manager ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ), accédez aux profils   >  **de configuration des appareils.**</span><span class="sxs-lookup"><span data-stu-id="7bca4-129">In the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)), navigate to **Devices** > **Configuration profiles**.</span></span>

2. <span data-ttu-id="7bca4-130">Sélectionnez ou créez un profil à l'aide du type de profil **Restrictions d'appareil.**</span><span class="sxs-lookup"><span data-stu-id="7bca4-130">Select or create a profile using the **Device restrictions** profile type.</span></span>

3. <span data-ttu-id="7bca4-131">Dans les **paramètres de configuration du** profil restrictions d'appareil, définissez ou confirmez les paramètres suivants sous **l'Antivirus Microsoft Defender**:</span><span class="sxs-lookup"><span data-stu-id="7bca4-131">In the **Configuration settings** for the Device restrictions profile, set or confirm the following settings under **Microsoft Defender Antivirus**:</span></span>

   - <span data-ttu-id="7bca4-132">**Protection cloud :** activée</span><span class="sxs-lookup"><span data-stu-id="7bca4-132">**Cloud-delivered protection**: Enabled</span></span>
   - <span data-ttu-id="7bca4-133">**Niveau de blocage de fichiers**: Élevé</span><span class="sxs-lookup"><span data-stu-id="7bca4-133">**File Blocking Level**: High</span></span>
   - <span data-ttu-id="7bca4-134">**Extension de temps pour l'analyse de fichiers par le cloud**: 50</span><span class="sxs-lookup"><span data-stu-id="7bca4-134">**Time extension for file scanning by the cloud**: 50</span></span>
   - <span data-ttu-id="7bca4-135">**Invite des utilisateurs avant l'envoi** de l'échantillon : envoyer toutes les données sans invite</span><span class="sxs-lookup"><span data-stu-id="7bca4-135">**Prompt users before sample submission**: Send all data without prompting</span></span>

   ![Config Intune](images/defender/intune-block-at-first-sight.png)

4. <span data-ttu-id="7bca4-137">Enregistrez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="7bca4-137">Save your settings.</span></span>

> [!TIP]
> - <span data-ttu-id="7bca4-138">La définition du niveau de blocage de fichiers **sur Élevé** applique un niveau élevé de détection.</span><span class="sxs-lookup"><span data-stu-id="7bca4-138">Setting the file blocking level to **High** applies a strong level of detection.</span></span> <span data-ttu-id="7bca4-139">Dans le cas peu probable où le blocage de fichiers entraîne une détection de faux positifs de fichiers légitimes, vous pouvez restaurer les [fichiers mis en quarantaine.](./restore-quarantined-files-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="7bca4-139">In the unlikely event that file blocking causes a false positive detection of legitimate files, you can [restore quarantined files](./restore-quarantined-files-microsoft-defender-antivirus.md).</span></span>
> - <span data-ttu-id="7bca4-140">Pour plus d'informations sur la configuration des restrictions d'appareil de l'Antivirus Microsoft Defender dans Intune, voir Configurer les paramètres de [restriction d'appareil dans Microsoft Intune.](/intune/device-restrictions-configure)</span><span class="sxs-lookup"><span data-stu-id="7bca4-140">For more information about configuring Microsoft Defender Antivirus device restrictions in Intune, see [Configure device restriction settings in Microsoft Intune](/intune/device-restrictions-configure).</span></span>
> - <span data-ttu-id="7bca4-141">Pour obtenir la liste des restrictions d'appareil de l'Antivirus Microsoft Defender dans Intune, voir Restriction d'appareil pour les [paramètres Windows 10 (et](/intune/device-restrictions-windows-10#microsoft-defender-antivirus)les plus nouveaux) dans Intune.</span><span class="sxs-lookup"><span data-stu-id="7bca4-141">For a list of Microsoft Defender Antivirus device restrictions in Intune, see [Device restriction for Windows 10 (and newer) settings in Intune](/intune/device-restrictions-windows-10#microsoft-defender-antivirus).</span></span>

## <a name="turn-on-block-at-first-sight-with-microsoft-endpoint-manager"></a><span data-ttu-id="7bca4-142">Activer bloquer à la première vue avec Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="7bca4-142">Turn on block at first sight with Microsoft Endpoint Manager</span></span>

> [!TIP]
> <span data-ttu-id="7bca4-143">Si vous recherchez Microsoft Endpoint Configuration Manager, il fait désormais partie de Microsoft Endpoint Manager.</span><span class="sxs-lookup"><span data-stu-id="7bca4-143">If you're looking for Microsoft Endpoint Configuration Manager, it's now part of Microsoft Endpoint Manager.</span></span>

1. <span data-ttu-id="7bca4-144">Dans Microsoft Endpoint Manager ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ), go to **Endpoint security**  >  **Antivirus**.</span><span class="sxs-lookup"><span data-stu-id="7bca4-144">In Microsoft Endpoint Manager ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)), go to **Endpoint security** > **Antivirus**.</span></span>

2. <span data-ttu-id="7bca4-145">Sélectionnez une stratégie existante ou créez une stratégie à l'aide du type de profil **Antivirus Microsoft Defender.**</span><span class="sxs-lookup"><span data-stu-id="7bca4-145">Select an existing policy, or create a new policy using the **Microsoft Defender Antivirus** profile type.</span></span>

3. <span data-ttu-id="7bca4-146">Définissez ou confirmez les paramètres de configuration suivants :</span><span class="sxs-lookup"><span data-stu-id="7bca4-146">Set or confirm the following configuration settings:</span></span>

   - <span data-ttu-id="7bca4-147">**Activer la protection cloud :** Oui</span><span class="sxs-lookup"><span data-stu-id="7bca4-147">**Turn on cloud-delivered protection**: Yes</span></span>
   - <span data-ttu-id="7bca4-148">**Niveau de protection cloud :** élevé</span><span class="sxs-lookup"><span data-stu-id="7bca4-148">**Cloud-delivered protection level**: High</span></span>
   - <span data-ttu-id="7bca4-149">**Délai d'out étendu de Defender Cloud en secondes**: 50</span><span class="sxs-lookup"><span data-stu-id="7bca4-149">**Defender Cloud Extended Timeout in Seconds**: 50</span></span>

   :::image type="content" source="images/endpointmgr-antivirus-cloudprotection.png" alt-text="Bloquer les paramètres à la première vue dans le Gestionnaire de point de terminaison":::

4. <span data-ttu-id="7bca4-151">Appliquez le profil antivirus Microsoft Defender à un groupe, tel que Tous les utilisateurs, Tous les **appareils** ou Tous **les utilisateurs et appareils.**</span><span class="sxs-lookup"><span data-stu-id="7bca4-151">Apply the Microsoft Defender Antivirus profile to a group, such as **All users**, **All devices**, or **All users and devices**.</span></span>

## <a name="turn-on-block-at-first-sight-with-group-policy"></a><span data-ttu-id="7bca4-152">Activer bloquer à la première vue avec la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7bca4-152">Turn on block at first sight with Group Policy</span></span>

> [!NOTE]
> <span data-ttu-id="7bca4-153">Nous vous recommandons d'utiliser Intune ou Microsoft Endpoint Manager pour activer bloquer à la première vue.</span><span class="sxs-lookup"><span data-stu-id="7bca4-153">We recommend using Intune or Microsoft Endpoint Manager to turn on block at first sight.</span></span> 

1. <span data-ttu-id="7bca4-154">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe que vous souhaitez configurer et sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="7bca4-154">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and select **Edit**.</span></span> 

2. <span data-ttu-id="7bca4-155">À **l'aide de l'Éditeur de gestion des stratégies** de groupe, go to **Computer configuration**  >  **Administrative**  >  **templates Windows Components**  >  **Microsoft Defender Antivirus**  >  **MAPS**.</span><span class="sxs-lookup"><span data-stu-id="7bca4-155">Using the **Group Policy Management Editor** go to **Computer configuration** > **Administrative templates** > **Windows Components** > **Microsoft Defender Antivirus** > **MAPS**.</span></span> 

3. <span data-ttu-id="7bca4-156">Dans la section MAPS, double-cliquez sur Configurer la fonctionnalité « Bloquer à la première vue » **et** définissez-la sur **Activé,** puis sélectionnez **OK.**</span><span class="sxs-lookup"><span data-stu-id="7bca4-156">In the MAPS section, double-click **Configure the 'Block at First Sight' feature**, and set it to **Enabled**, and then select **OK**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="7bca4-157">Le fait **de définir Always prompt (0)** réduit l'état de protection de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="7bca4-157">Setting to **Always prompt (0)** will lower the protection state of the device.</span></span> <span data-ttu-id="7bca4-158">Le paramètre **Ne jamais envoyer (2)** signifie que bloquer à la première vue ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="7bca4-158">Setting to **Never send (2)** means block at first sight will not function.</span></span>

4. <span data-ttu-id="7bca4-159">Dans la section MAPS, double-cliquez sur Envoyer des **exemples** de fichiers lorsque d'autres analyses sont requises et définissez-la **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="7bca4-159">In the MAPS section, double-click **Send file samples when further analysis is required**, and set it to **Enabled**.</span></span> <span data-ttu-id="7bca4-160">Sous **Envoyer des exemples de fichier lorsque d'autres analyses** sont **requises, sélectionnez Envoyer** tous les exemples, puis cliquez sur **OK.**</span><span class="sxs-lookup"><span data-stu-id="7bca4-160">Under **Send file samples when further analysis is required**, select **Send all samples**, and then click **OK**.</span></span>

5. <span data-ttu-id="7bca4-161">Si vous avez modifié des paramètres, redéployer l'objet de stratégie de groupe sur votre réseau pour vous assurer que tous les points de terminaison sont couverts.</span><span class="sxs-lookup"><span data-stu-id="7bca4-161">If you changed any settings, redeploy the Group Policy Object across your network to ensure all endpoints are covered.</span></span>

## <a name="confirm-block-at-first-sight-is-enabled-on-individual-clients"></a><span data-ttu-id="7bca4-162">Confirmer que bloquer à la première vue est activé sur des clients individuels</span><span class="sxs-lookup"><span data-stu-id="7bca4-162">Confirm block at first sight is enabled on individual clients</span></span>

<span data-ttu-id="7bca4-163">Vous pouvez vérifier que bloquer à la première vue est activé sur des clients individuels à l'aide des paramètres de sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="7bca4-163">You can confirm that block at first sight is enabled on individual clients using Windows security settings.</span></span>

<span data-ttu-id="7bca4-164">Bloquer à la première vue est automatiquement activé tant  que la protection cloud **et** l'envoi automatique d'échantillons sont tous deux activés.</span><span class="sxs-lookup"><span data-stu-id="7bca4-164">Block at first sight is automatically enabled as long as **Cloud-delivered protection** and **Automatic sample submission** are both turned on.</span></span>

1. <span data-ttu-id="7bca4-165">Ouvrez l'application Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="7bca4-165">Open the Windows Security app.</span></span>

2. <span data-ttu-id="7bca4-166">Sélectionnez **Protection & virus** contre les **menaces,** puis, sous Paramètres de protection contre & virus, sélectionnez Gérer **les paramètres.**</span><span class="sxs-lookup"><span data-stu-id="7bca4-166">Select **Virus & threat protection**, and then, under **Virus & threat protection settings**, select **Manage Settings**.</span></span>

   ![Capture d'écran de l'étiquette & protection contre les virus dans l'application Sécurité Windows](images/defender/wdav-protection-settings-wdsc.png)

3. <span data-ttu-id="7bca4-168">Confirmez **que la protection livrée par** le cloud et **l'envoi** automatique d'échantillons sont tous deux allumés.</span><span class="sxs-lookup"><span data-stu-id="7bca4-168">Confirm that **Cloud-delivered protection** and **Automatic sample submission** are both turned on.</span></span>

> [!NOTE]
> - <span data-ttu-id="7bca4-169">Si les paramètres prérequis sont configurés et déployés à l'aide de la stratégie de groupe, les paramètres décrits dans cette section sont grisés et ne peuvent pas être utilisés sur des points de terminaison individuels.</span><span class="sxs-lookup"><span data-stu-id="7bca4-169">If the prerequisite settings are configured and deployed using Group Policy, the settings described in this section will be greyed-out and unavailable for use on individual endpoints.</span></span> 
> - <span data-ttu-id="7bca4-170">Les modifications apportées via un objet de stratégie de groupe doivent d'abord être déployées sur des points de terminaison individuels avant que le paramètre ne soit mis à jour dans les paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="7bca4-170">Changes made through a Group Policy Object must first be deployed to individual endpoints before the setting will be updated in Windows Settings.</span></span>

## <a name="validate-block-at-first-sight-is-working"></a><span data-ttu-id="7bca4-171">Vérifier que bloquer à la première vue fonctionne</span><span class="sxs-lookup"><span data-stu-id="7bca4-171">Validate block at first sight is working</span></span>

<span data-ttu-id="7bca4-172">Pour vérifier que la fonctionnalité fonctionne, suivez les instructions de Validation des [connexions entre votre réseau et le cloud.](configure-network-connections-microsoft-defender-antivirus.md#validate-connections-between-your-network-and-the-cloud)</span><span class="sxs-lookup"><span data-stu-id="7bca4-172">To validate that the feature is working, follow the guidance in [Validate connections between your network and the cloud](configure-network-connections-microsoft-defender-antivirus.md#validate-connections-between-your-network-and-the-cloud).</span></span>

## <a name="turn-off-block-at-first-sight"></a><span data-ttu-id="7bca4-173">Désactiver bloquer à la première vue</span><span class="sxs-lookup"><span data-stu-id="7bca4-173">Turn off block at first sight</span></span>

> [!CAUTION]
> <span data-ttu-id="7bca4-174">La non-utilisation du blocage à la première vue réduit l'état de protection de vos appareils et de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="7bca4-174">Turning off block at first sight will lower the protection state of your device(s) and your network.</span></span>

<span data-ttu-id="7bca4-175">Vous pouvez choisir de désactiver bloquer à la première vue si vous souhaitez conserver les paramètres prérequis sans utiliser réellement la protection bloquer à la première vue.</span><span class="sxs-lookup"><span data-stu-id="7bca4-175">You might choose to disable block at first sight if you want to retain the prerequisite settings without actually using block at first sight protection.</span></span> <span data-ttu-id="7bca4-176">Vous pouvez désactiver temporairement bloquer à la première vue si vous rencontrez des problèmes de latence ou si vous souhaitez tester l'impact de la fonctionnalité sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="7bca4-176">You might do temporarily turn block at first sight off if you are experiencing latency issues or you want to test the feature's impact on your network.</span></span> <span data-ttu-id="7bca4-177">Toutefois, nous vous déconseillons de désactiver définitivement la protection bloquer à la première vue.</span><span class="sxs-lookup"><span data-stu-id="7bca4-177">However, we do not recommend disabling block at first sight protection permanently.</span></span>

### <a name="turn-off-block-at-first-sight-with-microsoft-endpoint-manager"></a><span data-ttu-id="7bca4-178">Désactiver bloquer à la première vue avec Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="7bca4-178">Turn off block at first sight with Microsoft Endpoint Manager</span></span>

1. <span data-ttu-id="7bca4-179">Go to Microsoft Endpoint Manager admin center ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="7bca4-179">Go to Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and sign in.</span></span>

2. <span data-ttu-id="7bca4-180">Go to **Endpoint security**  >  **Antivirus,** and then select your Microsoft Defender Antivirus policy.</span><span class="sxs-lookup"><span data-stu-id="7bca4-180">Go to **Endpoint security** > **Antivirus**, and then select your Microsoft Defender Antivirus policy.</span></span>

3. <span data-ttu-id="7bca4-181">Under **Manage**, choose **Properties**.</span><span class="sxs-lookup"><span data-stu-id="7bca4-181">Under **Manage**, choose **Properties**.</span></span>

4. <span data-ttu-id="7bca4-182">En de côté **des paramètres de configuration,** choisissez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="7bca4-182">Next to **Configuration settings**, choose **Edit**.</span></span>

5. <span data-ttu-id="7bca4-183">Modifiez un ou plusieurs des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7bca4-183">Change one or more of the following settings:</span></span>

   - <span data-ttu-id="7bca4-184">Définissez **Activer la protection cloud sur** **Non** ou **Non configuré.**</span><span class="sxs-lookup"><span data-stu-id="7bca4-184">Set **Turn on cloud-delivered protection** to **No** or **Not configured**.</span></span>
   - <span data-ttu-id="7bca4-185">Définissez **le niveau de protection livré par le cloud** sur Non **configuré.**</span><span class="sxs-lookup"><span data-stu-id="7bca4-185">Set **Cloud-delivered protection level** to **Not configured**.</span></span>
   - <span data-ttu-id="7bca4-186">Effacer la **zone Délai d'out étendu de Defender Cloud en secondes.**</span><span class="sxs-lookup"><span data-stu-id="7bca4-186">Clear the **Defender Cloud Extended Timeout In Seconds** box.</span></span>

6. <span data-ttu-id="7bca4-187">Examinez et enregistrez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="7bca4-187">Review and save your settings.</span></span>

### <a name="turn-off-block-at-first-sight-with-group-policy"></a><span data-ttu-id="7bca4-188">Désactiver bloquer à la première vue avec la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7bca4-188">Turn off block at first sight with Group Policy</span></span>

1. <span data-ttu-id="7bca4-189">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe à configurer, puis cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="7bca4-189">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure, and then click **Edit**.</span></span>

2. <span data-ttu-id="7bca4-190">À **l'aide de l'Éditeur de gestion des stratégies** de groupe, cliquez sur **Configuration** ordinateur et cliquez **sur Modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="7bca4-190">Using the **Group Policy Management Editor** go to **Computer configuration** and click **Administrative templates**.</span></span>

3. <span data-ttu-id="7bca4-191">Développez l'arborescence à **travers les composants Windows** Microsoft Defender  >  **Antivirus**  >  **MAPS**.</span><span class="sxs-lookup"><span data-stu-id="7bca4-191">Expand the tree through **Windows components** > **Microsoft Defender Antivirus** > **MAPS**.</span></span>

4. <span data-ttu-id="7bca4-192">Double-cliquez **sur Configurer la fonctionnalité «** Bloquer à la première vue » et définissez l'option sur **Désactivé.**</span><span class="sxs-lookup"><span data-stu-id="7bca4-192">Double-click **Configure the 'Block at First Sight' feature** and set the option to **Disabled**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7bca4-193">La désactivation de bloquer à la première vue ne désactive pas ou ne modifie pas les stratégies de groupe prérequises.</span><span class="sxs-lookup"><span data-stu-id="7bca4-193">Disabling block at first sight does not disable or alter the prerequisite group policies.</span></span>

## <a name="see-also"></a><span data-ttu-id="7bca4-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bca4-194">See also</span></span>

- [<span data-ttu-id="7bca4-195">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="7bca4-195">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)

- [<span data-ttu-id="7bca4-196">Activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="7bca4-196">Enable cloud-delivered protection</span></span>](enable-cloud-protection-microsoft-defender-antivirus.md)