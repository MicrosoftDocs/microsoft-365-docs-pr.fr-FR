---
title: Obtenir des appareils intégrés à Microsoft Defender pour le point de terminaison
description: Suivez l'intégration des appareils gérés par Intune à Microsoft Defender pour endpoint et augmentez le taux d'intégration.
keywords: intégration, gestion Intune, Microsoft Defender pour le point de terminaison, Microsoft Defender, Windows Defender, gestion de la configuration
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
ms.openlocfilehash: e0d5a13b0c33516209bd2d18361a1de6ab9245c2
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51932940"
---
# <a name="get-devices-onboarded-to-microsoft-defender-for-endpoint"></a><span data-ttu-id="27e6e-104">Obtenir des appareils intégrés à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="27e6e-104">Get devices onboarded to Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="27e6e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="27e6e-105">**Applies to:**</span></span>
- [<span data-ttu-id="27e6e-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="27e6e-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="27e6e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="27e6e-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="27e6e-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="27e6e-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="27e6e-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="27e6e-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-onboardconfigure-abovefoldlink)

<span data-ttu-id="27e6e-110">Chaque appareil intégré ajoute un capteur de détection et de réponse de point de terminaison (EDR) supplémentaire et augmente la visibilité sur l'activité de violation dans votre réseau.</span><span class="sxs-lookup"><span data-stu-id="27e6e-110">Each onboarded device adds an additional endpoint detection and response (EDR) sensor and increases visibility over breach activity in your network.</span></span> <span data-ttu-id="27e6e-111">L'intégration garantit également qu'un appareil peut être vérifié pour les composants vulnérables ainsi que les problèmes de configuration de sécurité et peut recevoir des actions de correction critiques pendant les attaques.</span><span class="sxs-lookup"><span data-stu-id="27e6e-111">Onboarding also ensures that a device can be checked for vulnerable components as well security configuration issues and can receive critical remediation actions during attacks.</span></span>

<span data-ttu-id="27e6e-112">Avant de pouvoir suivre et gérer l'intégration d'appareils :</span><span class="sxs-lookup"><span data-stu-id="27e6e-112">Before you can track and manage onboarding of devices:</span></span>
- [<span data-ttu-id="27e6e-113">Inscrire vos appareils à la gestion Intune</span><span class="sxs-lookup"><span data-stu-id="27e6e-113">Enroll your devices to Intune management</span></span>](configure-machines.md#enroll-devices-to-intune-management)
- [<span data-ttu-id="27e6e-114">Vérifier que vous avez les autorisations nécessaires</span><span class="sxs-lookup"><span data-stu-id="27e6e-114">Ensure you have the necessary permissions</span></span>](configure-machines.md#obtain-required-permissions)

## <a name="discover-and-track-unprotected-devices"></a><span data-ttu-id="27e6e-115">Découvrir et suivre les appareils non protégés</span><span class="sxs-lookup"><span data-stu-id="27e6e-115">Discover and track unprotected devices</span></span>

<span data-ttu-id="27e6e-116">La  carte d'intégration fournit une vue d'ensemble de votre taux d'intégration en comparant le nombre d'appareils Windows 10 réellement intégrés à Defender for Endpoint et le nombre total d'appareils Windows 10 gérés par Intune.</span><span class="sxs-lookup"><span data-stu-id="27e6e-116">The **Onboarding** card provides a high-level overview of your onboarding rate by comparing the number of Windows 10 devices that have actually onboarded to Defender for Endpoint against the total number of Intune-managed Windows 10 devices.</span></span>

<span data-ttu-id="27e6e-117">![Carte d'intégration de gestion de la configuration des appareils](images/secconmgmt_onboarding_card.png)</span><span class="sxs-lookup"><span data-stu-id="27e6e-117">![Device configuration management Onboarding card](images/secconmgmt_onboarding_card.png)</span></span><br>
<span data-ttu-id="27e6e-118">*Carte montrant les appareils intégrés par rapport au nombre total d'appareils Windows 10 gérés par Intune*</span><span class="sxs-lookup"><span data-stu-id="27e6e-118">*Card showing onboarded devices compared to the total number of Intune-managed Windows 10 device*</span></span>

>[!NOTE]
><span data-ttu-id="27e6e-119">Si vous avez utilisé Le Gestionnaire de configuration du Centre de sécurité, le script d'intégration ou d'autres méthodes d'intégration qui n'utilisent pas les profils Intune, vous pouvez rencontrer des incohérences de données.</span><span class="sxs-lookup"><span data-stu-id="27e6e-119">If you used Security Center Configuration Manager, the onboarding script, or other onboarding methods that don’t use Intune profiles, you might encounter data discrepancies.</span></span> <span data-ttu-id="27e6e-120">Pour résoudre ces incohérences, créez un profil de configuration Intune correspondant pour l'intégration de Defender for Endpoint et affectez ce profil à vos appareils.</span><span class="sxs-lookup"><span data-stu-id="27e6e-120">To resolve these discrepancies, create a corresponding Intune configuration profile for Defender for Endpoint onboarding and assign that profile to your devices.</span></span>

## <a name="onboard-more-devices-with-intune-profiles"></a><span data-ttu-id="27e6e-121">Intégrer d'autres appareils avec des profils Intune</span><span class="sxs-lookup"><span data-stu-id="27e6e-121">Onboard more devices with Intune profiles</span></span>

<span data-ttu-id="27e6e-122">Defender for Endpoint fournit plusieurs options pratiques pour [l'intégration d'appareils Windows 10.](onboard-configure.md)</span><span class="sxs-lookup"><span data-stu-id="27e6e-122">Defender for Endpoint provides several convenient options for [onboarding Windows 10 devices](onboard-configure.md).</span></span> <span data-ttu-id="27e6e-123">Toutefois, pour les appareils gérés par Intune, vous pouvez tirer parti des profils Intune pour déployer facilement le capteur Defender for Endpoint afin de sélectionner des appareils, ce qui permet d'intégrer efficacement ces appareils au service.</span><span class="sxs-lookup"><span data-stu-id="27e6e-123">For Intune-managed devices, however, you can leverage Intune profiles to conveniently deploy the Defender for Endpoint sensor to select devices, effectively onboarding these devices to the service.</span></span>

<span data-ttu-id="27e6e-124">À partir de **la carte d'intégration,** sélectionnez **Intégrer d'autres appareils** pour créer et affecter un profil sur Intune.</span><span class="sxs-lookup"><span data-stu-id="27e6e-124">From the **Onboarding** card, select **Onboard more devices** to create and assign a profile on Intune.</span></span> <span data-ttu-id="27e6e-125">Le lien vous permet d'utiliser la page de conformité des appareils sur Intune, qui fournit une vue d'ensemble similaire de votre état d'intégration.</span><span class="sxs-lookup"><span data-stu-id="27e6e-125">The link takes you to the device compliance page on Intune, which provides a similar overview of your onboarding state.</span></span>

<span data-ttu-id="27e6e-126">![Page de conformité des appareils Microsoft Defender for Endpoint sur la gestion des appareils Intune](images/secconmgmt_onboarding_1deviceconfprofile.png)</span><span class="sxs-lookup"><span data-stu-id="27e6e-126">![Microsoft Defender for Endpoint device compliance page on Intune device management](images/secconmgmt_onboarding_1deviceconfprofile.png)</span></span><br>
   <span data-ttu-id="27e6e-127">*Page de conformité des appareils Microsoft Defender for Endpoint sur la gestion des appareils Intune*</span><span class="sxs-lookup"><span data-stu-id="27e6e-127">*Microsoft Defender for Endpoint device compliance page on Intune device management*</span></span>

>[!TIP]
><span data-ttu-id="27e6e-128">Vous pouvez également accéder à la page de conformité d'intégration Defender for Endpoint dans le portail [Microsoft Azure](https://portal.azure.com/) à partir de Tous les services **> Intune > Conformité** des appareils > Microsoft Defender ATP .</span><span class="sxs-lookup"><span data-stu-id="27e6e-128">Alternatively, you can navigate to the Defender for Endpoint onboarding compliance page in the [Microsoft Azure portal](https://portal.azure.com/) from **All services > Intune > Device compliance > Microsoft Defender ATP**.</span></span>

>[!NOTE]
> <span data-ttu-id="27e6e-129">Si vous souhaitez afficher les données d'appareil les plus récentes, cliquez sur Liste des appareils sans **capteur ATP.**</span><span class="sxs-lookup"><span data-stu-id="27e6e-129">If you want to view the most up-to-date device data, click on **List of devices without ATP sensor**.</span></span>

<span data-ttu-id="27e6e-130">À partir de la page de conformité des appareils, créez un profil de configuration spécifique pour le déploiement du capteur Defender for Endpoint et affectez ce profil aux appareils que vous souhaitez intégrer.</span><span class="sxs-lookup"><span data-stu-id="27e6e-130">From the device compliance page, create a configuration profile specifically for the deployment of the Defender for Endpoint sensor and assign that profile to the devices you want to onboard.</span></span> <span data-ttu-id="27e6e-131">Pour ce faire, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="27e6e-131">To do this, you can either:</span></span>

- <span data-ttu-id="27e6e-132">Sélectionnez Créer un profil de configuration d'appareil pour configurer le capteur **ATP** afin qu'il commence par un profil de configuration d'appareil prédéféré.</span><span class="sxs-lookup"><span data-stu-id="27e6e-132">Select **Create a device configuration profile to configure ATP sensor** to start with a predefined device configuration profile.</span></span>
- <span data-ttu-id="27e6e-133">Créez le profil de configuration de l'appareil de A à Z.</span><span class="sxs-lookup"><span data-stu-id="27e6e-133">Create the device configuration profile from scratch.</span></span>

<span data-ttu-id="27e6e-134">Pour plus d'informations, découvrez l'utilisation des profils de configuration d'appareil Intune pour intégrer des [appareils à Defender for Endpoint.](https://docs.microsoft.com/intune/advanced-threat-protection#onboard-devices-by-using-a-configuration-profile)</span><span class="sxs-lookup"><span data-stu-id="27e6e-134">For more information, [read about using Intune device configuration profiles to onboard devices to Defender for Endpoint](https://docs.microsoft.com/intune/advanced-threat-protection#onboard-devices-by-using-a-configuration-profile).</span></span>

><span data-ttu-id="27e6e-135">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="27e6e-135">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="27e6e-136">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="27e6e-136">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-onboardconfigure-belowfoldlink)

## <a name="related-topics"></a><span data-ttu-id="27e6e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27e6e-137">Related topics</span></span>
- [<span data-ttu-id="27e6e-138">Vérifier que vos appareils sont correctement configurés</span><span class="sxs-lookup"><span data-stu-id="27e6e-138">Ensure your devices are configured properly</span></span>](configure-machines.md)
- [<span data-ttu-id="27e6e-139">Renforcer la conformité à la ligne de base de sécurité de Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="27e6e-139">Increase compliance to the Defender for Endpoint security baseline</span></span>](configure-machines-security-baseline.md)
- [<span data-ttu-id="27e6e-140">Optimiser le déploiement et les détections de règles asr</span><span class="sxs-lookup"><span data-stu-id="27e6e-140">Optimize ASR rule deployment and detections</span></span>](configure-machines-asr.md)
