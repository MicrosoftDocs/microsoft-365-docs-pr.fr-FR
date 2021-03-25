---
title: S’assurer que vos appareils sont correctement configurés
description: Configurez correctement les appareils pour renforcer la résilience globale contre les menaces et améliorer votre capacité à détecter les attaques et à y répondre.
keywords: intégré, gestion Intune, MDATP, WDATP, Microsoft Defender, Windows Defender, protection avancée contre les menaces, réduction de la surface d’attaque, RÉDUCTION, ligne de base de sécurité
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
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: e7b00ceafc2761f42c316f434a27acf7c551e7cf
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51163362"
---
# <a name="ensure-your-devices-are-configured-properly"></a><span data-ttu-id="d6ea2-104">S’assurer que vos appareils sont correctement configurés</span><span class="sxs-lookup"><span data-stu-id="d6ea2-104">Ensure your devices are configured properly</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="d6ea2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d6ea2-105">**Applies to:**</span></span>
- [<span data-ttu-id="d6ea2-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d6ea2-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="d6ea2-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d6ea2-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="d6ea2-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="d6ea2-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="d6ea2-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-onboardconfigure-abovefoldlink)

<span data-ttu-id="d6ea2-110">Avec des appareils correctement configurés, vous pouvez renforcer la résilience globale contre les menaces et améliorer votre capacité à détecter les attaques et à y répondre.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-110">With properly configured devices, you can boost overall resilience against threats and enhance your capability to detect and respond to attacks.</span></span> <span data-ttu-id="d6ea2-111">La gestion de la configuration de la sécurité permet de s’assurer que vos appareils :</span><span class="sxs-lookup"><span data-stu-id="d6ea2-111">Security configuration management helps ensure that your devices:</span></span>

- <span data-ttu-id="d6ea2-112">Intégration à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d6ea2-112">Onboard to Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="d6ea2-113">Meet or exceed the Defender for Endpoint security baseline configuration</span><span class="sxs-lookup"><span data-stu-id="d6ea2-113">Meet or exceed the Defender for Endpoint security baseline configuration</span></span>
- <span data-ttu-id="d6ea2-114">Mettre en place des atténuations de la surface d’attaque stratégique</span><span class="sxs-lookup"><span data-stu-id="d6ea2-114">Have strategic attack surface mitigations in place</span></span>

<span data-ttu-id="d6ea2-115">Cliquez **sur Gestion de la** configuration dans le menu de navigation pour ouvrir la page Gestion de la configuration des appareils.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-115">Click **Configuration management** from the navigation menu to open the Device configuration management page.</span></span>

<span data-ttu-id="d6ea2-116">![Page Gestion de la configuration de la sécurité](images/secconmgmt_main.png)</span><span class="sxs-lookup"><span data-stu-id="d6ea2-116">![Security configuration management page](images/secconmgmt_main.png)</span></span><br>
<span data-ttu-id="d6ea2-117">*Page Gestion de la configuration des appareils*</span><span class="sxs-lookup"><span data-stu-id="d6ea2-117">*Device configuration management page*</span></span>

<span data-ttu-id="d6ea2-118">Vous pouvez suivre l’état de configuration au niveau de l’organisation et prendre rapidement des mesures en réponse à une couverture d’intégration médiocre, à des problèmes de conformité et à des atténuations de la surface d’attaque mal optimisées via des liens directs et profonds vers des pages de gestion des appareils sur Microsoft Intune et le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-118">You can track configuration status at an organizational level and quickly take action in response to poor onboarding coverage, compliance issues, and poorly optimized attack surface mitigations through direct, deep links to device management pages on Microsoft Intune and Microsoft 365 security center.</span></span>

<span data-ttu-id="d6ea2-119">Pour ce faire, vous bénéficiez des avantages de :</span><span class="sxs-lookup"><span data-stu-id="d6ea2-119">In doing so, you benefit from:</span></span>
- <span data-ttu-id="d6ea2-120">Visibilité complète des événements sur vos appareils</span><span class="sxs-lookup"><span data-stu-id="d6ea2-120">Comprehensive visibility of the events on your devices</span></span>
- <span data-ttu-id="d6ea2-121">Veille fiable sur les menaces et technologies puissantes d’apprentissage des appareils pour traiter les événements bruts et identifier l’activité de violation et les indicateurs de menace</span><span class="sxs-lookup"><span data-stu-id="d6ea2-121">Robust threat intelligence and powerful device learning technologies for processing raw events and identifying the breach activity and threat indicators</span></span>
- <span data-ttu-id="d6ea2-122">Pile complète de fonctionnalités de sécurité configurées pour arrêter efficacement l’installation de programmes malveillants, le piratage de fichiers et de processus système, l’exfiltration de données et d’autres activités contre les menaces</span><span class="sxs-lookup"><span data-stu-id="d6ea2-122">A full stack of security features configured to efficiently stop the installation of malicious implants, hijacking of system files and process, data exfiltration, and other threat activities</span></span>
- <span data-ttu-id="d6ea2-123">Optimisation des atténuations de la surface d’attaque, optimisation des défenses stratégiques contre l’activité des menaces tout en réduisant l’impact sur la productivité</span><span class="sxs-lookup"><span data-stu-id="d6ea2-123">Optimized attack surface mitigations, maximizing strategic defenses against threat activity while minimizing impact to productivity</span></span>

## <a name="enroll-devices-to-intune-management"></a><span data-ttu-id="d6ea2-124">Inscrire des appareils à la gestion Intune</span><span class="sxs-lookup"><span data-stu-id="d6ea2-124">Enroll devices to Intune management</span></span>

<span data-ttu-id="d6ea2-125">La gestion de la configuration des appareils fonctionne en étroite collaboration avec la gestion des appareils Intune pour établir l’inventaire des appareils de votre organisation et la configuration de sécurité de référence.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-125">Device configuration management works closely with Intune device management to establish the inventory of the devices in your organization and the baseline security configuration.</span></span> <span data-ttu-id="d6ea2-126">Vous pourrez suivre et gérer les problèmes de configuration sur les appareils Windows 10 gérés par Intune.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-126">You will be able to track and manage configuration issues on Intune-managed Windows 10 devices.</span></span>

<span data-ttu-id="d6ea2-127">Avant de pouvoir vous assurer que vos appareils sont correctement configurés, inscrivez-les à la gestion Intune.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-127">Before you can ensure your devices are configured properly, enroll them to Intune management.</span></span> <span data-ttu-id="d6ea2-128">L’inscription Intune est robuste et offre plusieurs options d’inscription pour les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-128">Intune enrollment is robust and has several enrollment options for Windows 10 devices.</span></span> <span data-ttu-id="d6ea2-129">Pour plus d’informations sur les options d’inscription Intune, voir la configuration de [l’inscription pour les appareils Windows.](https://docs.microsoft.com/intune/windows-enroll)</span><span class="sxs-lookup"><span data-stu-id="d6ea2-129">For more information about Intune enrollment options, read about [setting up enrollment for Windows devices](https://docs.microsoft.com/intune/windows-enroll).</span></span>

>[!NOTE]
><span data-ttu-id="d6ea2-130">Pour inscrire des appareils Windows à Intune, les administrateurs doivent avoir déjà reçu des licences.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-130">To enroll Windows devices to Intune, administrators must have already been assigned licenses.</span></span> <span data-ttu-id="d6ea2-131">[En savoir plus sur l’attribution de licences pour l’inscription des appareils.](https://docs.microsoft.com/intune/licenses-assign)</span><span class="sxs-lookup"><span data-stu-id="d6ea2-131">[Read about assigning licenses for device enrollment](https://docs.microsoft.com/intune/licenses-assign).</span></span>

>[!TIP] 
><span data-ttu-id="d6ea2-132">Pour optimiser la gestion des appareils via Intune, [connectez Intune à Defender pour endpoint.](https://docs.microsoft.com/intune/advanced-threat-protection#enable-windows-defender-atp-in-intune)</span><span class="sxs-lookup"><span data-stu-id="d6ea2-132">To optimize device management through Intune, [connect Intune to Defender for Endpoint](https://docs.microsoft.com/intune/advanced-threat-protection#enable-windows-defender-atp-in-intune).</span></span>

## <a name="obtain-required-permissions"></a><span data-ttu-id="d6ea2-133">Obtenir les autorisations requises</span><span class="sxs-lookup"><span data-stu-id="d6ea2-133">Obtain required permissions</span></span>
<span data-ttu-id="d6ea2-134">Par défaut, seuls les utilisateurs qui ont reçu le rôle Administrateur général ou Administrateur du service Intune sur Azure AD peuvent gérer et affecter les profils de configuration d’appareil nécessaires à l’intégration des appareils et au déploiement de la ligne de base de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-134">By default, only users who have been assigned the Global Administrator or the Intune Service Administrator role on Azure AD can manage and assign the device configuration profiles needed for onboarding devices and deploying the security baseline.</span></span>

<span data-ttu-id="d6ea2-135">Si d’autres rôles vous ont été attribués, assurez-vous que vous avez les autorisations nécessaires :</span><span class="sxs-lookup"><span data-stu-id="d6ea2-135">If you have been assigned other roles, ensure you have the necessary permissions:</span></span>

- <span data-ttu-id="d6ea2-136">Autorisations complètes sur les configurations d’appareil</span><span class="sxs-lookup"><span data-stu-id="d6ea2-136">Full permissions to device configurations</span></span>
- <span data-ttu-id="d6ea2-137">Autorisations complètes sur les lignes de base de sécurité</span><span class="sxs-lookup"><span data-stu-id="d6ea2-137">Full permissions to security baselines</span></span>
- <span data-ttu-id="d6ea2-138">Autorisations de lecture des stratégies de conformité des appareils</span><span class="sxs-lookup"><span data-stu-id="d6ea2-138">Read permissions to device compliance policies</span></span>
- <span data-ttu-id="d6ea2-139">Autorisations de lecture pour l’organisation</span><span class="sxs-lookup"><span data-stu-id="d6ea2-139">Read permissions to the organization</span></span>

<span data-ttu-id="d6ea2-140">![Autorisations requises sur intune](images/secconmgmt_intune_permissions.png)</span><span class="sxs-lookup"><span data-stu-id="d6ea2-140">![Required permissions on intune](images/secconmgmt_intune_permissions.png)</span></span><br>
<span data-ttu-id="d6ea2-141">*Autorisations de configuration d’appareil sur Intune*</span><span class="sxs-lookup"><span data-stu-id="d6ea2-141">*Device configuration permissions on Intune*</span></span>

>[!TIP] 
><span data-ttu-id="d6ea2-142">Pour en savoir plus sur l’attribution d’autorisations sur Intune, découvrez [comment créer des rôles personnalisés.](https://docs.microsoft.com/intune/create-custom-role#to-create-a-custom-role)</span><span class="sxs-lookup"><span data-stu-id="d6ea2-142">To learn more about assigning permissions on Intune, [read about creating custom roles](https://docs.microsoft.com/intune/create-custom-role#to-create-a-custom-role).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d6ea2-143">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d6ea2-143">In this section</span></span>
<span data-ttu-id="d6ea2-144">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d6ea2-144">Topic</span></span> | <span data-ttu-id="d6ea2-145">Description</span><span class="sxs-lookup"><span data-stu-id="d6ea2-145">Description</span></span>
:---|:---
[<span data-ttu-id="d6ea2-146">Obtenir des appareils intégrés à Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d6ea2-146">Get devices onboarded to Defender for Endpoint</span></span>](configure-machines-onboarding.md)| <span data-ttu-id="d6ea2-147">Suivre l’état d’intégration des appareils gérés par Intune et intégrer d’autres appareils via Intune.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-147">Track onboarding status of Intune-managed devices and onboard more devices through Intune.</span></span> 
[<span data-ttu-id="d6ea2-148">Renforcer la conformité à la ligne de base de sécurité de Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="d6ea2-148">Increase compliance to the Defender for Endpoint security baseline</span></span>](configure-machines-security-baseline.md) | <span data-ttu-id="d6ea2-149">Suivre la conformité et la non-conformité des lignes de base.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-149">Track baseline compliance and noncompliance.</span></span> <span data-ttu-id="d6ea2-150">Déployez la ligne de base de sécurité sur d’autres appareils gérés par Intune.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-150">Deploy the security baseline to more Intune-managed devices.</span></span>
[<span data-ttu-id="d6ea2-151">Optimiser le déploiement et les détections de règles asr</span><span class="sxs-lookup"><span data-stu-id="d6ea2-151">Optimize ASR rule deployment and detections</span></span>](configure-machines-asr.md) | <span data-ttu-id="d6ea2-152">Examinez le déploiement des règles et ajustez les détections à l’aide des outils d’analyse d’impact dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-152">Review rule deployment and tweak detections using impact analysis tools in Microsoft 365 security center.</span></span>

><span data-ttu-id="d6ea2-153">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="d6ea2-153">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="d6ea2-154">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-154">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-onboardconfigure-belowfoldlink)
