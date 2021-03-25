---
title: Renforcer la conformité à la ligne de base de sécurité de Microsoft Defender ATP
description: La ligne de base de sécurité Microsoft Defender ATP définit les contrôles de sécurité Microsoft Defender ATP pour fournir une protection optimale.
keywords: Gestion Intune, MDATP, WDATP, Microsoft Defender, asr de protection avancée contre les menaces, ligne de base de sécurité
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: lomayor
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 74073441ad7be89e0af278ff1e371133251b5ea7
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51163398"
---
# <a name="increase-compliance-to-the-microsoft-defender-for-endpoint-security-baseline"></a><span data-ttu-id="67d13-104">Renforcer la conformité à la ligne de base de sécurité microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="67d13-104">Increase compliance to the Microsoft Defender for Endpoint security baseline</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="67d13-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="67d13-105">**Applies to:**</span></span>
- [<span data-ttu-id="67d13-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="67d13-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="67d13-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="67d13-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="67d13-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="67d13-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="67d13-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="67d13-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-onboardconfigure-abovefoldlink)

<span data-ttu-id="67d13-110">Les lignes de base de sécurité garantissent que les fonctionnalités de sécurité sont configurées conformément aux conseils des experts en sécurité et des administrateurs système Windows experts.</span><span class="sxs-lookup"><span data-stu-id="67d13-110">Security baselines ensure that security features are configured according to guidance from both security experts and expert Windows system administrators.</span></span> <span data-ttu-id="67d13-111">Lorsqu’elle est déployée, la ligne de base de sécurité defender pour point de terminaison définit les contrôles de sécurité Defender pour les points de terminaison afin de fournir une protection optimale.</span><span class="sxs-lookup"><span data-stu-id="67d13-111">When deployed, the Defender for Endpoint security baseline sets Defender for Endpoint security controls to provide optimal protection.</span></span>

<span data-ttu-id="67d13-112">Pour comprendre les lignes de base de sécurité et la façon dont elles sont affectées sur Intune à l’aide de profils de configuration, [lisez ce FAQ.](https://docs.microsoft.com/intune/security-baselines#q--a)</span><span class="sxs-lookup"><span data-stu-id="67d13-112">To understand security baselines and how they are assigned on Intune using configuration profiles, [read this FAQ](https://docs.microsoft.com/intune/security-baselines#q--a).</span></span>

<span data-ttu-id="67d13-113">Avant de pouvoir déployer et suivre la conformité aux lignes de base de sécurité :</span><span class="sxs-lookup"><span data-stu-id="67d13-113">Before you can deploy and track compliance to security baselines:</span></span>
- [<span data-ttu-id="67d13-114">Inscrire vos appareils à la gestion Intune</span><span class="sxs-lookup"><span data-stu-id="67d13-114">Enroll your devices to Intune management</span></span>](configure-machines.md#enroll-devices-to-intune-management)
- [<span data-ttu-id="67d13-115">Vérifier que vous avez les autorisations nécessaires</span><span class="sxs-lookup"><span data-stu-id="67d13-115">Ensure you have the necessary permissions</span></span>](configure-machines.md#obtain-required-permissions)

## <a name="compare-the-microsoft-defender-atp-and-the-windows-intune-security-baselines"></a><span data-ttu-id="67d13-116">Comparer les lignes de base de sécurité Microsoft Defender ATP et Windows Intune</span><span class="sxs-lookup"><span data-stu-id="67d13-116">Compare the Microsoft Defender ATP and the Windows Intune security baselines</span></span>
<span data-ttu-id="67d13-117">La ligne de base de sécurité Windows Intune fournit un ensemble complet de paramètres recommandés nécessaires pour configurer en toute sécurité les appareils exécutant Windows, y compris les paramètres de navigateur, les paramètres PowerShell, ainsi que les paramètres de certaines fonctionnalités de sécurité telles que l’Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="67d13-117">The Windows Intune security baseline provides a comprehensive set of recommended settings needed to securely configure devices running Windows, including browser settings, PowerShell settings, as well as settings for some security features like Microsoft Defender Antivirus.</span></span> <span data-ttu-id="67d13-118">En revanche, la ligne de base de Defender pour point de terminaison fournit des paramètres qui optimisent tous les contrôles de sécurité dans la pile Defender pour les points de terminaison, y compris les paramètres de détection et de réponse des points de terminaison (EDR), ainsi que les paramètres également trouvés dans la ligne de base de sécurité Windows Intune.</span><span class="sxs-lookup"><span data-stu-id="67d13-118">In contrast, the Defender for Endpoint baseline provides settings that optimize all the security controls in the Defender for Endpoint stack, including settings for endpoint detection and response (EDR) as well as settings also found in the Windows Intune security baseline.</span></span> <span data-ttu-id="67d13-119">Pour plus d’informations sur chaque ligne de base, voir :</span><span class="sxs-lookup"><span data-stu-id="67d13-119">For more information about each baseline, see:</span></span>

- [<span data-ttu-id="67d13-120">Paramètres de base de sécurité Windows pour Intune</span><span class="sxs-lookup"><span data-stu-id="67d13-120">Windows security baseline settings for Intune</span></span>](https://docs.microsoft.com/intune/security-baseline-settings-windows)
- [<span data-ttu-id="67d13-121">Paramètres de référence de Microsoft Defender ATP pour Intune</span><span class="sxs-lookup"><span data-stu-id="67d13-121">Microsoft Defender ATP baseline settings for Intune</span></span>](https://docs.microsoft.com/intune/security-baseline-settings-defender-atp)

<span data-ttu-id="67d13-122">Dans l’idéal, les appareils intégrés à Defender pour point de terminaison sont déployés à la fois sur les deux lignes de base : la ligne de base de sécurité Windows Intune pour sécuriser initialement Windows, puis la ligne de base de sécurité De Defender pour point de terminaison superposée au-dessus pour configurer de manière optimale les contrôles de sécurité Defender pour les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="67d13-122">Ideally, devices onboarded to Defender for Endpoint are deployed both baselines: the Windows Intune security baseline to initially secure Windows and then the Defender for Endpoint security baseline layered on top to optimally configure the Defender for Endpoint security controls.</span></span> <span data-ttu-id="67d13-123">Pour tirer parti des données les plus récentes sur les risques et les menaces et réduire les conflits à mesure que les lignes de base évoluent, appliquez toujours les dernières versions des lignes de base sur tous les produits dès leur publication.</span><span class="sxs-lookup"><span data-stu-id="67d13-123">To benefit from the latest data on risks and threats and to minimize conflicts as baselines evolve, always apply the latest versions of the baselines across all products as soon as they are released.</span></span>

>[!NOTE]
><span data-ttu-id="67d13-124">La ligne de base de sécurité defender pour point de terminaison a été optimisée pour les appareils physiques et n’est actuellement pas recommandée pour une utilisation sur des ordinateurs virtuels (VM) ou des points de terminaison VDI.</span><span class="sxs-lookup"><span data-stu-id="67d13-124">The Defender for Endpoint security baseline has been optimized for physical devices and is currently not recommended for use on virtual machine (VMs) or VDI endpoints.</span></span> <span data-ttu-id="67d13-125">Certains paramètres de référence peuvent avoir un impact sur les sessions interactives à distance sur les environnements virtualisés.</span><span class="sxs-lookup"><span data-stu-id="67d13-125">Certain baseline settings can impact remote interactive sessions on virtualized environments.</span></span>

## <a name="monitor-compliance-to-the-defender-for-endpoint-security-baseline"></a><span data-ttu-id="67d13-126">Surveiller la conformité à la ligne de base de sécurité de Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="67d13-126">Monitor compliance to the Defender for Endpoint security baseline</span></span>

<span data-ttu-id="67d13-127">La **carte de référence** sécurité sur la gestion de la [configuration](configure-machines.md) des appareils fournit une vue d’ensemble de la conformité sur les appareils Windows 10 qui ont reçu la ligne de base de sécurité Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="67d13-127">The **Security baseline** card on [device configuration management](configure-machines.md) provides an overview of compliance across Windows 10 devices that have been assigned the Defender for Endpoint security baseline.</span></span>

<span data-ttu-id="67d13-128">![Carte de référence de sécurité](images/secconmgmt_baseline_card.png)</span><span class="sxs-lookup"><span data-stu-id="67d13-128">![Security baseline card](images/secconmgmt_baseline_card.png)</span></span><br>
<span data-ttu-id="67d13-129">*Carte montrant la conformité à la ligne de base de sécurité defender pour point de terminaison*</span><span class="sxs-lookup"><span data-stu-id="67d13-129">*Card showing compliance to the Defender for Endpoint security baseline*</span></span>

<span data-ttu-id="67d13-130">L’un des types d’état suivants est attribué à chaque appareil :</span><span class="sxs-lookup"><span data-stu-id="67d13-130">Each device is given one of the following status types:</span></span>

- <span data-ttu-id="67d13-131">**Correspond à la ligne de** base : les paramètres de l’appareil correspondent à tous les paramètres de la ligne de base</span><span class="sxs-lookup"><span data-stu-id="67d13-131">**Matches baseline**—device settings match all the settings in the baseline</span></span>
- <span data-ttu-id="67d13-132">**Ne correspond pas à la ligne de** base : au moins un paramètre d’appareil ne correspond pas à la ligne de base</span><span class="sxs-lookup"><span data-stu-id="67d13-132">**Does not match baseline**—at least one device setting doesn't match the baseline</span></span>
- <span data-ttu-id="67d13-133">**Mal configuré :** au moins un paramètre de référence n’est pas correctement configuré sur l’appareil et est en conflit, en erreur ou en attente</span><span class="sxs-lookup"><span data-stu-id="67d13-133">**Misconfigured**—at least one baseline setting isn't properly configured on the device and is in a conflict, error, or pending state</span></span>
- <span data-ttu-id="67d13-134">**Non applicable :** au moins un paramètre de référence n’est pas applicable sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="67d13-134">**Not applicable**—At least one baseline setting isn't applicable on the device</span></span>

<span data-ttu-id="67d13-135">Pour passer en revue des appareils spécifiques, **sélectionnez Configurer la ligne de base de sécurité** sur la carte.</span><span class="sxs-lookup"><span data-stu-id="67d13-135">To review specific devices, select **Configure security baseline** on the card.</span></span> <span data-ttu-id="67d13-136">Cela vous permet d’utiliser la gestion des appareils Intune.</span><span class="sxs-lookup"><span data-stu-id="67d13-136">This takes you to Intune device management.</span></span> <span data-ttu-id="67d13-137">À partir de là, **sélectionnez État de l’appareil** pour les noms et les états des appareils.</span><span class="sxs-lookup"><span data-stu-id="67d13-137">From there, select **Device status** for the names and statuses of the devices.</span></span>

>[!NOTE]
><span data-ttu-id="67d13-138">Vous pouvez faire face à des incohérences dans les données agrégées affichées sur la page de gestion de la configuration des appareils et celles affichées sur les écrans de vue d’ensemble dans Intune.</span><span class="sxs-lookup"><span data-stu-id="67d13-138">You might experience discrepancies in aggregated data displayed on the device configuration management page and those displayed on overview screens in Intune.</span></span>

## <a name="review-and-assign-the-microsoft-defender-for-endpoint-security-baseline"></a><span data-ttu-id="67d13-139">Examiner et affecter la ligne de base de sécurité microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="67d13-139">Review and assign the Microsoft Defender for Endpoint security baseline</span></span>

<span data-ttu-id="67d13-140">La gestion de la configuration des appareils surveille la conformité de référence uniquement des appareils Windows 10 qui ont été spécifiquement affectés à la ligne de base de sécurité Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="67d13-140">Device configuration management monitors baseline compliance only of Windows 10 devices that have been specifically assigned the Microsoft Defender for Endpoint security baseline.</span></span> <span data-ttu-id="67d13-141">Vous pouvez facilement consulter la ligne de base et l’affecter aux appareils sur la gestion des appareils Intune.</span><span class="sxs-lookup"><span data-stu-id="67d13-141">You can conveniently review the baseline and assign it to devices on Intune device management.</span></span>

1. <span data-ttu-id="67d13-142">Sélectionnez **Configurer la ligne de base de sécurité** sur la carte de **référence** sécurité pour passer à la gestion des appareils Intune.</span><span class="sxs-lookup"><span data-stu-id="67d13-142">Select **Configure security baseline** on the **Security baseline** card to go to Intune device management.</span></span> <span data-ttu-id="67d13-143">Une vue d’ensemble similaire de la conformité de référence s’affiche.</span><span class="sxs-lookup"><span data-stu-id="67d13-143">A similar overview of baseline compliance is displayed.</span></span>

   >[!TIP]
   > <span data-ttu-id="67d13-144">Vous pouvez également accéder à la ligne de base de sécurité Defender for Endpoint dans le portail Microsoft Azure à partir de Tous les **services > Intune >** Sécurité des appareils > Sécurité > base de référence Microsoft Defender ATP .</span><span class="sxs-lookup"><span data-stu-id="67d13-144">Alternatively, you can navigate to the Defender for Endpoint security baseline in the Microsoft Azure portal from **All services > Intune > Device security > Security baselines > Microsoft Defender ATP baseline**.</span></span>


2. <span data-ttu-id="67d13-145">Créez un profil.</span><span class="sxs-lookup"><span data-stu-id="67d13-145">Create a new profile.</span></span>

   <span data-ttu-id="67d13-146">![Vue d’ensemble de la ligne de base de sécurité microsoft Defender pour point de terminaison sur Intune](images/secconmgmt_baseline_intuneprofile1.png)</span><span class="sxs-lookup"><span data-stu-id="67d13-146">![Microsoft Defender for Endpoint security baseline overview on Intune](images/secconmgmt_baseline_intuneprofile1.png)</span></span><br>
   <span data-ttu-id="67d13-147">*Vue d’ensemble de la ligne de base de sécurité microsoft Defender pour point de terminaison sur Intune*</span><span class="sxs-lookup"><span data-stu-id="67d13-147">*Microsoft Defender for Endpoint security baseline overview on Intune*</span></span>

3. <span data-ttu-id="67d13-148">Lors de la création du profil, vous pouvez examiner et ajuster des paramètres spécifiques sur la ligne de base.</span><span class="sxs-lookup"><span data-stu-id="67d13-148">During profile creation, you can review and adjust specific settings on the baseline.</span></span>

   <span data-ttu-id="67d13-149">![Options de base de sécurité lors de la création du profil sur Intune](images/secconmgmt_baseline_intuneprofile2.png)</span><span class="sxs-lookup"><span data-stu-id="67d13-149">![Security baseline options during profile creation on Intune](images/secconmgmt_baseline_intuneprofile2.png)</span></span><br>
   <span data-ttu-id="67d13-150">*Options de base de sécurité lors de la création du profil sur Intune*</span><span class="sxs-lookup"><span data-stu-id="67d13-150">*Security baseline options during profile creation on Intune*</span></span>

4. <span data-ttu-id="67d13-151">Affectez le profil au groupe d’appareils approprié.</span><span class="sxs-lookup"><span data-stu-id="67d13-151">Assign the profile to the appropriate device group.</span></span>

   <span data-ttu-id="67d13-152">![Profils de base de sécurité sur Intune](images/secconmgmt_baseline_intuneprofile3.png)</span><span class="sxs-lookup"><span data-stu-id="67d13-152">![Security baseline profiles on Intune](images/secconmgmt_baseline_intuneprofile3.png)</span></span><br>
   <span data-ttu-id="67d13-153">*Affectation du profil de base de sécurité sur Intune*</span><span class="sxs-lookup"><span data-stu-id="67d13-153">*Assigning the security baseline profile on Intune*</span></span>

5. <span data-ttu-id="67d13-154">Créez le profil pour l’enregistrer et déployez-le sur le groupe d’appareils affecté.</span><span class="sxs-lookup"><span data-stu-id="67d13-154">Create the profile to save it and deploy it to the assigned device group.</span></span>

   <span data-ttu-id="67d13-155">![Affectation de la ligne de base de sécurité sur Intune](images/secconmgmt_baseline_intuneprofile4.png)</span><span class="sxs-lookup"><span data-stu-id="67d13-155">![Assigning the security baseline on Intune](images/secconmgmt_baseline_intuneprofile4.png)</span></span><br>
   <span data-ttu-id="67d13-156">*Création du profil de base de sécurité sur Intune*</span><span class="sxs-lookup"><span data-stu-id="67d13-156">*Creating the security baseline profile on Intune*</span></span>

>[!TIP]
><span data-ttu-id="67d13-157">Les lignes de base de sécurité sur Intune offrent un moyen pratique de sécuriser et de protéger de manière exhaustive vos appareils.</span><span class="sxs-lookup"><span data-stu-id="67d13-157">Security baselines on Intune provide a convenient way to comprehensively secure and protect your devices.</span></span> <span data-ttu-id="67d13-158">[En savoir plus sur les bases de référence de sécurité sur Intune.](https://docs.microsoft.com/intune/security-baselines)</span><span class="sxs-lookup"><span data-stu-id="67d13-158">[Learn more about security baselines on Intune](https://docs.microsoft.com/intune/security-baselines).</span></span>

><span data-ttu-id="67d13-159">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="67d13-159">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="67d13-160">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="67d13-160">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-onboardconfigure-belowfoldlink)

## <a name="related-topics"></a><span data-ttu-id="67d13-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67d13-161">Related topics</span></span>
- [<span data-ttu-id="67d13-162">S’assurer que vos appareils sont correctement configurés</span><span class="sxs-lookup"><span data-stu-id="67d13-162">Ensure your devices are configured properly</span></span>](configure-machines.md)
- [<span data-ttu-id="67d13-163">Obtenir des appareils intégrés à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="67d13-163">Get devices onboarded to Microsoft Defender for Endpoint</span></span>](configure-machines-onboarding.md)
- [<span data-ttu-id="67d13-164">Optimiser le déploiement et les détections de règles asr</span><span class="sxs-lookup"><span data-stu-id="67d13-164">Optimize ASR rule deployment and detections</span></span>](configure-machines-asr.md)
