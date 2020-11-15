---
title: Prise en main de la protection contre la perte de données de point de terminaison Microsoft 365
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 07/21/2020
audience: ITPro
ms.topic: conceptual
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- m365solution-mip
- m365initiative-compliance
search.appverid:
- MET150
description: Configurez la protection contre la perte de données de point de terminaison Microsoft 365 pour surveiller les activités des fichiers, puis implémenter des actions de protection de ces fichiers aux points de terminaison.
ms.openlocfilehash: 6ba3b83d634f946f818890a732a83166f346162d
ms.sourcegitcommit: fcc1b40732f28f075d95faffc1655473e262dd95
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2020
ms.locfileid: "49073093"
---
# <a name="get-started-with-endpoint-data-loss-prevention"></a><span data-ttu-id="58432-103">Prise en main de la protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="58432-103">Get started with Endpoint data loss prevention</span></span>

<span data-ttu-id="58432-p101">La protection contre la perte de données de point de terminaison Microsoft (DLP de point de terminaison) fait partie de la suite de fonctionnalités de protection contre la perte de données Microsoft 365 que vous pouvez utiliser pour découvrir et protéger les éléments sensibles dans les services Microsoft 365. Si vous souhaitez en savoir plus sur toutes les offres DLP de Microsoft, consultez l’article [Présentation de la protection contre la perte de données](data-loss-prevention-policies.md). Si vous souhaitez en savoir plus sur la DLP de point de terminaison, consultez l’article [Découvrir la protection contre la perte de données de point de terminaison](endpoint-dlp-learn-about.md)</span><span class="sxs-lookup"><span data-stu-id="58432-p101">Microsoft Endpoint data loss prevention (Endpoint DLP) is part of the Microsoft 365 data loss prevention (DLP) suite of features you can use to discover and protect sensitive items across Microsoft 365 services. For more information about all of Microsoft’s DLP offerings, see [Overview of data loss prevention](data-loss-prevention-policies.md). To learn more about Endpoint DLP, see [Learn about Endpoint data loss prevention](endpoint-dlp-learn-about.md)</span></span>

<span data-ttu-id="58432-p102">La DLP de point de terminaison Microsoft vous permet de surveiller les appareils Windows 10 et de détecter le partage et l’utilisation des éléments sensibles. Cela vous donne la visibilité et le contrôle dont vous avez besoin pour vous assurer qu’ils sont correctement utilisés et protégés, et pour éviter les comportements à risque qui pourraient les compromettre.</span><span class="sxs-lookup"><span data-stu-id="58432-p102">Microsoft Endpoint DLP allows you to monitor Windows 10 devices and detect when sensitive items are used and shared. This gives you the visibility and control you need to ensure that they are used and protected properly, and to help prevent risky behavior that might compromise them.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="58432-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="58432-109">Before you begin</span></span>

### <a name="skusubscriptions-licensing"></a><span data-ttu-id="58432-110">Licences SKU / abonnements</span><span class="sxs-lookup"><span data-stu-id="58432-110">SKU/subscriptions licensing</span></span>

<span data-ttu-id="58432-p103">Avant de commencer avec la DLP de point de terminaison, vous devez confirmer votre [abonnement Microsoft 365](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) et tous les modules complémentaires. Pour accéder et utiliser la fonctionnalité de DLP de point de terminaison, vous devez disposer de l’un de ces abonnements ou modules complémentaires.</span><span class="sxs-lookup"><span data-stu-id="58432-p103">Before you get started with Endpoint DLP, you should confirm your [Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) and any add-ons. To access and use Endpoint DLP functionality, you must have one of these subscriptions or add-ons.</span></span>

- <span data-ttu-id="58432-113">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="58432-113">Microsoft 365 E5</span></span>
- <span data-ttu-id="58432-114">Microsoft 365 A5 (EDU)</span><span class="sxs-lookup"><span data-stu-id="58432-114">Microsoft 365 A5 (EDU)</span></span>
- <span data-ttu-id="58432-115">Microsoft 365 E5 Conformité</span><span class="sxs-lookup"><span data-stu-id="58432-115">Microsoft 365 E5 compliance</span></span>
- <span data-ttu-id="58432-116">Microsoft 365 A5 Conformité</span><span class="sxs-lookup"><span data-stu-id="58432-116">Microsoft 365 A5 compliance</span></span>
- <span data-ttu-id="58432-117">Microsoft 365 E5, Protection des informations et gouvernance</span><span class="sxs-lookup"><span data-stu-id="58432-117">Microsoft 365 E5 information protection and governance</span></span>
- <span data-ttu-id="58432-118">Microsoft 365 A5, Protection des informations et gouvernance</span><span class="sxs-lookup"><span data-stu-id="58432-118">Microsoft 365 A5 information protection and governance</span></span>


### <a name="permissions"></a><span data-ttu-id="58432-119">Autorisations</span><span class="sxs-lookup"><span data-stu-id="58432-119">Permissions</span></span>

<span data-ttu-id="58432-120">Pour activer la gestion des appareils, le compte que vous utilisez doit être membre de l’un de ces rôles :</span><span class="sxs-lookup"><span data-stu-id="58432-120">To enable device management, the account you use must be a member of any one of these roles:</span></span>

- <span data-ttu-id="58432-121">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="58432-121">Global admin</span></span>
- <span data-ttu-id="58432-122">Administrateur de la sécurité</span><span class="sxs-lookup"><span data-stu-id="58432-122">Security admin</span></span>
- <span data-ttu-id="58432-123">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="58432-123">Compliance admin</span></span>

<span data-ttu-id="58432-124">Si vous voulez utiliser un compte personnalisé pour afficher les paramètres de gestion des appareils, celui-ci doit se trouver dans l’un de ces rôles :</span><span class="sxs-lookup"><span data-stu-id="58432-124">If you want to use a custom account to view the device management settings, it must be in one of these roles:</span></span>

- <span data-ttu-id="58432-125">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="58432-125">Global admin</span></span>
- <span data-ttu-id="58432-126">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="58432-126">Compliance admin</span></span>
- <span data-ttu-id="58432-127">Administrateur des données de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="58432-127">Compliance data admin</span></span>
- <span data-ttu-id="58432-128">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="58432-128">Global reader</span></span>

<span data-ttu-id="58432-129">Si vous voulez utiliser un compte personnalisé pour accéder à la page d’intégration/déclassement, celui-ci doit se trouver dans l’un de ces rôles :</span><span class="sxs-lookup"><span data-stu-id="58432-129">If you want to use a custom account to access the onboarding/offboarding page, it must be in one of these roles:</span></span>

- <span data-ttu-id="58432-130">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="58432-130">Global admin</span></span>
- <span data-ttu-id="58432-131">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="58432-131">Compliance admin</span></span>

<span data-ttu-id="58432-132">Si vous voulez utiliser un compte personnalisé pour activer/désactiver la surveillance de l’appareil, celui-ci doit se trouver dans l’un de ces rôles :</span><span class="sxs-lookup"><span data-stu-id="58432-132">If you want to use a custom account to turn on/off device monitoring, it must be in one of these roles:</span></span>

- <span data-ttu-id="58432-133">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="58432-133">Global admin</span></span>
- <span data-ttu-id="58432-134">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="58432-134">Compliance admin</span></span>

<span data-ttu-id="58432-p104">Les données de la DLP de point de terminaison peuvent être affichées dans l’[explorateur d’activités](data-classification-activity-explorer.md). Il y a quatre rôles qui accordent l’autorisation à l’explorateur d’activités. Le compte que vous utilisez pour accéder aux données doit être membre de l’un d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="58432-p104">Data from Endpoint DLP can be viewed in [Activity explorer](data-classification-activity-explorer.md). There are four roles that grant permission to activity explorer, the account you use for accessing the data must be a member of any one of them.</span></span>

- <span data-ttu-id="58432-137">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="58432-137">Global admin</span></span>
- <span data-ttu-id="58432-138">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="58432-138">Compliance admin</span></span>
- <span data-ttu-id="58432-139">Administrateur de la sécurité</span><span class="sxs-lookup"><span data-stu-id="58432-139">Security admin</span></span>
- <span data-ttu-id="58432-140">Administrateur des données de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="58432-140">Compliance data admin</span></span>

### <a name="prepare-your-endpoints"></a><span data-ttu-id="58432-141">Préparer vos points de terminaison</span><span class="sxs-lookup"><span data-stu-id="58432-141">Prepare your endpoints</span></span>

<span data-ttu-id="58432-142">Assurez-vous que les appareils Windows 10 pour lesquels vous envisagez de déployer le point de terminaison DLP répondent à ces exigences.</span><span class="sxs-lookup"><span data-stu-id="58432-142">Make sure that the Windows 10 devices that you plan on deploying Endpoint DLP to meet these requirements.</span></span>

1. <span data-ttu-id="58432-143">Vous devez disposer de la version 1809 de Windows 10 x64 ou d’une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="58432-143">Must be running Windows 10 x64 build 1809 or later.</span></span>

2. <span data-ttu-id="58432-p105">Vous devez disposer de la version 4.18.2009.7 du client anti-programme malveillant ou une version plus récente. Vérifiez votre version actuelle en ouvrant l’application de sécurité Windows, en sélectionnant l’icône Paramètres, puis À propos de. Le numéro de version est indiqué sous Version du client anti-programme malveillant. Effectuez une mise à jour vers la dernière version du client antimalware en installant Windows Update KB4052623. Remarque : aucun des composants de sécurité Windows ne doit être actif. Vous pouvez exécuter la DLP de point de terminaison indépendamment de l’état de la sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="58432-p105">Antimalware Client Version is 4.18.2009.7 or newer. Check your current version by opening Windows Security app, select the Settings icon, and then select About. The version number is listed under Antimalware Client Version. Update to the latest Antimalware Client Version by installing Windows Update KB4052623. Note: None of Windows Security components need to be active, you can run Endpoint DLP independent of Windows Security status.</span></span>

3. <span data-ttu-id="58432-p106">Les mises à jour Windows suivantes sont installées. Remarque : ces mises à jour ne sont pas une condition préalable à l’intégration d’un appareil à la DLP de point de terminaison, mais contiennent des correctifs pour des problèmes importants et doivent donc être installées avant d’utiliser le produit.</span><span class="sxs-lookup"><span data-stu-id="58432-p106">The following Windows Updates are installed. Note: These updates are not a pre-requisite to onboard a device to Endpoint DLP, but contain fixes for important issues thus must be installed before using the product.</span></span>

    - <span data-ttu-id="58432-151">Pour la version 1809 de Windows 10 : KB4559003, KB4577069, KB4580390</span><span class="sxs-lookup"><span data-stu-id="58432-151">For Windows 10 1809 - KB4559003, KB4577069, KB4580390</span></span>
    - <span data-ttu-id="58432-152">Pour Windows 10 version 1903 ou 1909 : KB4559004, KB4577062, KB4580386</span><span class="sxs-lookup"><span data-stu-id="58432-152">For Windows 10 1903 or 1909 - KB4559004, KB4577062, KB4580386</span></span>
    - <span data-ttu-id="58432-153">Pour Windows 10 version 2004 : KB4568831, KB4577063</span><span class="sxs-lookup"><span data-stu-id="58432-153">For Windows 10 2004 - KB4568831, KB4577063</span></span>
    - <span data-ttu-id="58432-154">Pour les appareils exécutant Office 2016 (et non aucune autre version d’Office) : KB4577063</span><span class="sxs-lookup"><span data-stu-id="58432-154">For devices running Office 2016 (and not any other Office version) - KB4577063</span></span> 

4. <span data-ttu-id="58432-155">Tous les appareils doivent être [joints à Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join) ou à Azure AD Hybride.</span><span class="sxs-lookup"><span data-stu-id="58432-155">All devices must be [Azure Active Directory (Azure AD) joined](https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join), or Hybrid Azure AD joined.</span></span>

5. <span data-ttu-id="58432-p107">Installez le navigateur Microsoft Chromium Edge sur l’appareil final afin d’appliquer des actions de stratégie pour l’activité de téléchargement vers le cloud. Consultez l’article [Télécharger le nouveau Microsoft Edge basé sur Chromium](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium).</span><span class="sxs-lookup"><span data-stu-id="58432-p107">Install Microsoft Chromium Edge browser on the endpoint device to enforce policy actions for the upload to cloud activity. See, [Download the new Microsoft Edge based on Chromium](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium).</span></span>

6. <span data-ttu-id="58432-p108">Si vous utilisez le Canal Entreprise mensuel des versions 2004 à 2008 de Microsoft 365 Apps, il existe un problème connu avec la DLP de point de terminaison classifiant le contenu Office. Vous devez effectuer une mise à jour vers la version 2009 ou une version ultérieure. Consultez l’article [Historique des mises à jour pour Microsoft 365 Apps (répertoriées par date)](https://docs.microsoft.com/officeupdates/update-history-microsoft365-apps-by-date) pour les versions actuelles. Si vous souhaitez en savoir plus sur ce problème, consultez la section Suite Office des [Notes de publication pour les versions du Canal actuel en 2020](https://docs.microsoft.com/officeupdates/current-channel#version-2010-october-27).</span><span class="sxs-lookup"><span data-stu-id="58432-p108">If you are on Monthly Enterprise Channel of Microsoft 365 Apps versions 2004-2008, there is a known issue with Endpoint DLP classifying Office content and you need to update to version 2009 or later. See [Update history for Microsoft 365 Apps (listed by date)](https://docs.microsoft.com/officeupdates/update-history-microsoft365-apps-by-date) for current versions. To learn more about this issue, see the Office Suite section of [Release notes for Current Channel releases in 2020](https://docs.microsoft.com/officeupdates/current-channel#version-2010-october-27).</span></span>

## <a name="onboarding-devices-into-device-management"></a><span data-ttu-id="58432-161">Intégrer les appareils dans la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="58432-161">Onboarding devices into device management</span></span>

<span data-ttu-id="58432-p109">Vous devez activer la surveillance des appareils et intégrer vos points de terminaison avant de pouvoir surveiller et protéger les éléments sensibles sur un appareil. Ces deux actions sont effectuées dans le portail de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="58432-p109">You must enable device monitoring and onboard your endpoints before you can monitor and protect sensitive items on a device. Both of these actions are done in the Microsoft 365 Compliance portal.</span></span>

<span data-ttu-id="58432-p110">Lorsque vous souhaitez intégrer des appareils qui n’ont pas encore été intégrés, vous téléchargez le script approprié et le déployez sur ces appareils. Suivez la procédure pour [Intégrer des appareils](endpoint-dlp-getting-started.md#onboarding-devices).</span><span class="sxs-lookup"><span data-stu-id="58432-p110">When you want to onboard devices that haven't been onboarded yet, you'll download the appropriate script and deploy it to those devices. Follow the [Onboarding devices procedure](endpoint-dlp-getting-started.md#onboarding-devices).</span></span>

<span data-ttu-id="58432-p111">Si vous avez déjà des appareils intégrés dans [Microsoft Defender pour point de terminaison](https://docs.microsoft.com/windows/security/threat-protection/), ils apparaîtront déjà dans la liste des appareils gérés. Suivez la procédure [Avec les appareils intégrés à Microsoft Defender pour point de terminaison](endpoint-dlp-getting-started.md#with-devices-onboarded-into-microsoft-defender-for- endpoint).</span><span class="sxs-lookup"><span data-stu-id="58432-p111">If you already have devices onboarded into [Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection/), they will already appear in the managed devices list. Follow the [With devices onboarded into Microsoft Defender for Endpoint procedure](endpoint-dlp-getting-started.md#with-devices-onboarded-into-microsoft-defender-for- endpoint).</span></span>

### <a name="onboarding-devices"></a><span data-ttu-id="58432-168">Intégrer les appareils</span><span class="sxs-lookup"><span data-stu-id="58432-168">Onboarding devices</span></span>

<span data-ttu-id="58432-169">Dans ce scénario de déploiement, vous allez intégrer des appareils qui n’ont pas encore été intégrés, et vous voulez simplement contrôler et protéger les éléments sensibles contre le partage involontaire sur les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="58432-169">In this deployment scenario, you'll onboard devices that have not been onboarded yet, and you just want to monitor and protect sensitive items from unintentional sharing on Windows 10 devices.</span></span>

1. <span data-ttu-id="58432-170">Ouvrez le [Centre de conformité Microsoft](https://compliance.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="58432-170">Open the [Microsoft compliance center](https://compliance.microsoft.com).</span></span>

2. <span data-ttu-id="58432-171">Ouvrez la page Paramètres du centre de conformité et sélectionnez **Appareils intégrés**.</span><span class="sxs-lookup"><span data-stu-id="58432-171">Open the Compliance Center settings page and choose **Onboard devices**.</span></span> 

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="58432-172">![activer la gestion des appareils](../media/endpoint-dlp-learn-about-1-enable-device-management.png)</span><span class="sxs-lookup"><span data-stu-id="58432-172">![enable device management](../media/endpoint-dlp-learn-about-1-enable-device-management.png)</span></span>

   > [!NOTE]
   > <span data-ttu-id="58432-173">L’activation de l’intégration des appareils prend généralement environ 60 secondes. Toutefois, patientez jusqu’à 30 minutes avant de contacter le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="58432-173">While it usually takes about 60 seconds for device onboarding to be enabled, please allow up to 30 minutes before engaging with Microsoft support.</span></span>

3. <span data-ttu-id="58432-p112">Sélectionnez **Gestion des appareils** pour ouvrir la liste des **Appareils**. La liste sera vide tant que vous n’aurez pas intégré d’appareils.</span><span class="sxs-lookup"><span data-stu-id="58432-p112">Choose **Device management** to open the **Devices** list. The list will be empty until you onboard devices.</span></span>

4. <span data-ttu-id="58432-176">Sélectionnez **Intégration** pour lancer le processus d’intégration.</span><span class="sxs-lookup"><span data-stu-id="58432-176">Choose **Onboarding** to begin the onboarding process.</span></span>

5. <span data-ttu-id="58432-177">Choisissez la manière dont vous voulez déployer ces autres appareils à partir de la liste **Méthode de déploiement** , puis **Télécharger le package**.</span><span class="sxs-lookup"><span data-stu-id="58432-177">Choose the way you want to deploy to these additional devices from the **Deployment method** list and then **download package**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="58432-178">![méthode de déploiement](../media/endpoint-dlp-getting-started-3-deployment-method.png)</span><span class="sxs-lookup"><span data-stu-id="58432-178">![deployment method](../media/endpoint-dlp-getting-started-3-deployment-method.png)</span></span>
   
6. <span data-ttu-id="58432-p113">Suivez les procédures appropriées décrites dans l’article [Outils et méthodes d’intégration pour les ordinateurs Windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints). Ce lien vous dirige vers une page de destination dans laquelle vous pouvez accéder aux procédures Microsoft Defender pour point de terminaison qui correspondent au package de déploiement que vous avez sélectionné à l’étape 5 :</span><span class="sxs-lookup"><span data-stu-id="58432-p113">Follow the appropriate procedures in [Onboarding tools and methods for Windows 10 machines](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints). This link take you to a landing page where you can access Microsoft Defender for Endpoint procedures that match the deployment package you selected in step 5:</span></span>

    - <span data-ttu-id="58432-181">Intégrer des ordinateurs Windows 10 avec une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="58432-181">Onboard Windows 10 machines using Group Policy</span></span>
    - <span data-ttu-id="58432-182">Intégrer les ordinateurs Windows à l’aide du gestionnaire de configuration de point de terminaison Microsoft</span><span class="sxs-lookup"><span data-stu-id="58432-182">Onboard Windows machines using Microsoft Endpoint Configuration Manager</span></span>
    - <span data-ttu-id="58432-183">Intégrer les ordinateurs Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="58432-183">Onboard Windows 10 machines using Mobile Device Management tools</span></span>
    - <span data-ttu-id="58432-184">Intégrer les ordinateurs Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="58432-184">Onboard Windows 10 machines using a local script</span></span>
    - <span data-ttu-id="58432-185">Intégrer les ordinateurs virtuels d’infrastructure de bureau virtuel (VDI) non persistants.</span><span class="sxs-lookup"><span data-stu-id="58432-185">Onboard non-persistent virtual desktop infrastructure (VDI) machines.</span></span>

<span data-ttu-id="58432-186">Une fois l’opération effectuée et le point de terminaison intégré, celui-ci doit être visible dans la liste des appareils et doit commencer à créer des rapports d’activité d’audit dans l’Explorateur d’activités.</span><span class="sxs-lookup"><span data-stu-id="58432-186">Once done and endpoint is onboarded, it should be visible in the devices list and also start reporting audit activity logs to Activity explorer.</span></span>

> [!NOTE]
> <span data-ttu-id="58432-p114">Cette expérience est soumise à l’application de la licence. Sans la licence requise, les données ne seront ni visibles ni accessibles.</span><span class="sxs-lookup"><span data-stu-id="58432-p114">This experience is under license enforcement. Without the required license, data will not be visible or accessible.</span></span>

### <a name="with-devices-onboarded-into-microsoft-defender-for-endpoint"></a><span data-ttu-id="58432-189">Avec des appareils intégrés dans Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="58432-189">With devices onboarded into Microsoft Defender for Endpoint</span></span>

<span data-ttu-id="58432-p115">Dans ce scénario, Microsoft Defender pour point de terminaison est déjà déployé et des points de terminaison effectuent des rapports. Tous ces points de terminaison apparaîtront dans la liste des appareils gérés. Vous pouvez continuer à intégrer de nouveaux appareils dans la DLP pour point de terminaison pour étendre la couverture à l’aide de la [Procédure d’intégration des appareils](endpoint-dlp-getting-started.md#onboarding-devices).</span><span class="sxs-lookup"><span data-stu-id="58432-p115">In this scenario, Microsoft Defender for Endpoint is already deployed and there are endpoints reporting in. All these endpoints will appear in the managed devices list. You can continue to onboard new devices into Endpoint DLP to expand coverage by using the [Onboarding devices procedure](endpoint-dlp-getting-started.md#onboarding-devices).</span></span>

1. <span data-ttu-id="58432-193">Ouvrez le [Centre de conformité Microsoft](https://compliance.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="58432-193">Open the [Microsoft compliance center](https://compliance.microsoft.com).</span></span>

2. <span data-ttu-id="58432-194">Ouvrez la page Paramètres du Centre de conformité et sélectionnez **Activer la surveillance des appareils**.</span><span class="sxs-lookup"><span data-stu-id="58432-194">Open the Compliance Center settings page and choose **Enable device monitoring**.</span></span>

3. <span data-ttu-id="58432-p116">Sélectionnez **Gestion des appareils** pour ouvrir la liste des **Appareils**. Vous devriez voir la liste des appareils qui effectuent déjà des rapports à Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="58432-p116">Choose **Device management** to open the **Devices** list. You should see the list of devices that are already reporting in to Microsoft Defender for Endpoint.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="58432-197">![gestion des appareils](../media/endpoint-dlp-getting-started-2-device-management.png)</span><span class="sxs-lookup"><span data-stu-id="58432-197">![device management](../media/endpoint-dlp-getting-started-2-device-management.png)</span></span>
   
4. <span data-ttu-id="58432-198">Sélectionnez **Intégration** si vous avez besoin d’intégrer d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="58432-198">Choose **Onboarding** if you need to onboard additional devices.</span></span>

5. <span data-ttu-id="58432-199">Choisissez la manière dont vous souhaitez déployer ces autres appareils dans la liste **Méthode de déploiement** , puis **Télécharger le package**.</span><span class="sxs-lookup"><span data-stu-id="58432-199">Choose the way you want to deploy to these additional devices from the **Deployment method** list and then **Download package**.</span></span>

6. <span data-ttu-id="58432-p117">Suivez les procédures appropriées décrites dans l’article [Outils et méthodes d’intégration pour les ordinateurs Windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints). Ce lien vous dirige vers une page de destination dans laquelle vous pouvez accéder aux procédures Microsoft Defender pour point de terminaison qui correspondent au package de déploiement que vous avez sélectionné à l’étape 5 :</span><span class="sxs-lookup"><span data-stu-id="58432-p117">Follow the appropriate procedures in [Onboarding tools and methods for Windows 10 machines](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints). This link take you to a landing page where you can access Microsoft Defender for Endpoint procedures that match the deployment package you selected in step 5:</span></span>

    - <span data-ttu-id="58432-202">Intégrer des ordinateurs Windows 10 avec une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="58432-202">Onboard Windows 10 machines using Group Policy</span></span>
    - <span data-ttu-id="58432-203">Intégrer les ordinateurs Windows à l’aide du gestionnaire de configuration de point de terminaison Microsoft</span><span class="sxs-lookup"><span data-stu-id="58432-203">Onboard Windows machines using Microsoft Endpoint Configuration Manager</span></span>
    - <span data-ttu-id="58432-204">Intégrer les ordinateurs Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="58432-204">Onboard Windows 10 machines using Mobile Device Management tools</span></span>
    - <span data-ttu-id="58432-205">Intégrer les ordinateurs Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="58432-205">Onboard Windows 10 machines using a local script</span></span>
    - <span data-ttu-id="58432-206">Intégrer les ordinateurs virtuels d’infrastructure de bureau virtuel (VDI) non persistants.</span><span class="sxs-lookup"><span data-stu-id="58432-206">Onboard non-persistent virtual desktop infrastructure (VDI) machines.</span></span>

<span data-ttu-id="58432-207">Une fois l’opération effectuée et le point de terminaison intégré, celui-ci doit être visible dans le tableau des **Appareils** et doit commencer à créer des rapports d’activité d’audit dans l’ **Explorateur d’activités**.</span><span class="sxs-lookup"><span data-stu-id="58432-207">Once done and endpoint is onboarded, it should be visible under the **Devices** table and also start reporting audit logs to the **Activity Explorer**.</span></span>

> [!NOTE]
><span data-ttu-id="58432-p118">Cette expérience est soumise à l’application de la licence. Sans la licence requise, les données ne seront ni visibles ni accessibles.</span><span class="sxs-lookup"><span data-stu-id="58432-p118">This experience is under license enforcement. Without the required license, data will not be visible or accessible.</span></span>

### <a name="viewing-endpoint-dlp-alerts-in-dlp-alerts-management-dashboard"></a><span data-ttu-id="58432-210">Afficher les alertes de la DLP de point de terminaison dans le tableau de bord de Gestion des alertes DLP</span><span class="sxs-lookup"><span data-stu-id="58432-210">Viewing Endpoint DLP alerts in DLP Alerts Management dashboard</span></span>

1. <span data-ttu-id="58432-211">Ouvrez la page de protection contre la perte de données dans le Centre de conformité Microsoft 365, puis sélectionnez Alertes.</span><span class="sxs-lookup"><span data-stu-id="58432-211">Open the Data loss prevention page in the Microsoft 365 Compliance center and choose Alerts.</span></span>

2. <span data-ttu-id="58432-212">Reportez-vous aux procédures décrites dans [Comment configurer et afficher les alertes pour les stratégies DLP](dlp-configure-view-alerts-policies.md) pour afficher les alertes relatives à vos stratégies DLP de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="58432-212">Refer to the procedures in [How to configure and view alerts for your DLP policies](dlp-configure-view-alerts-policies.md) to view alerts for your Endpoint DLP policies.</span></span>


### <a name="viewing-endpoint-dlp-data-in-activity-explorer"></a><span data-ttu-id="58432-213">Affichage de données DLP de point de terminaison dans l’Explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="58432-213">Viewing Endpoint DLP data in activity explorer</span></span>

1. <span data-ttu-id="58432-214">Ouvrez la [Page classification des données](https://compliance.microsoft.com/dataclassification?viewid=overview) pour votre domaine dans le centre de conformité Microsoft 365, puis sélectionnez Explorateur d’activités.</span><span class="sxs-lookup"><span data-stu-id="58432-214">Open the [Data classification page](https://compliance.microsoft.com/dataclassification?viewid=overview) for your domain in the Microsoft 365 Compliance center and choose Activity explorer.</span></span>

2. <span data-ttu-id="58432-215">Reportez-vous aux procédures décrites dans [Prise en main de l’Explorateur d’activités](data-classification-activity-explorer.md) pour accéder aux données de vos appareils de point de terminaison et les filtrer.</span><span class="sxs-lookup"><span data-stu-id="58432-215">Refer to the procedures in [Get started with Activity explorer](data-classification-activity-explorer.md) to access and filter all the data for your Endpoint devices.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="58432-216">![filtre de l’Explorateur d’activités pour les appareils de point de terminaison](../media/endpoint-dlp-4-getting-started-activity-explorer.png)</span><span class="sxs-lookup"><span data-stu-id="58432-216">![activity explorer filter for endpoint devices](../media/endpoint-dlp-4-getting-started-activity-explorer.png)</span></span>

## <a name="next-steps"></a><span data-ttu-id="58432-217">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="58432-217">Next steps</span></span>
<span data-ttu-id="58432-218">Maintenant que vous disposez d’appareils intégrés et que vous pouvez afficher les données d’activité dans l’Explorateur d’activités, vous êtes prêt à passer à l’étape suivante dans laquelle vous créez des stratégies DLP qui protègent vos éléments sensibles.</span><span class="sxs-lookup"><span data-stu-id="58432-218">Now that you have onboarded devices and can view the activity data in Activity explorer, you are ready to move on to your next step where you create DLP policies that protect your sensitive items.</span></span>

- [<span data-ttu-id="58432-219">Utilisation des points de terminaison de protection contre la perte de données (aperçu)</span><span class="sxs-lookup"><span data-stu-id="58432-219">Using Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-using.md)

## <a name="see-also"></a><span data-ttu-id="58432-220">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58432-220">See also</span></span>

- [<span data-ttu-id="58432-221">En savoir plus sur les points de terminaison de protection contre la perte de données (Preview)</span><span class="sxs-lookup"><span data-stu-id="58432-221">Learn about Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-learn-about.md)
- [<span data-ttu-id="58432-222">Utilisation des points de terminaison de protection contre la perte de données (aperçu)</span><span class="sxs-lookup"><span data-stu-id="58432-222">Using Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-using.md)
- [<span data-ttu-id="58432-223">Vue d’ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="58432-223">Overview of data loss prevention</span></span>](data-loss-prevention-policies.md)
- [<span data-ttu-id="58432-224">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="58432-224">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="58432-225">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="58432-225">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="58432-226">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="58432-226">Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection/)
- <span data-ttu-id="58432-227">[Outils et méthodes d’intégration pour les appareils Windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="58432-227">[Onboarding tools and methods for Windows 10 machines](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints)</span></span>
- [<span data-ttu-id="58432-228">Abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="58432-228">Microsoft 365 subscription</span></span>](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1)
- [<span data-ttu-id="58432-229">Azure AD appareils joints</span><span class="sxs-lookup"><span data-stu-id="58432-229">Azure AD joined devices</span></span>](https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join)
- [<span data-ttu-id="58432-230">Télécharger le nouveau Microsoft Edge sur la base de chrome</span><span class="sxs-lookup"><span data-stu-id="58432-230">Download the new Microsoft Edge based on Chromium</span></span>](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium)
