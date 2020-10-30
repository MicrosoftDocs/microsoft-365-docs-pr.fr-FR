---
title: Prise en main des points de terminaison de protection contre la perte de données Microsoft 365 (Preview)
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
description: Configurez les points de terminaison contre la protection contre la perte de données Microsoft 365 pour surveiller les activités des fichiers et implémenter des actions de protection pour ces fichiers aux points de terminaison.
ms.openlocfilehash: 82ba434d1874ce57abcf0bcc4b60858e0e2ccbf8
ms.sourcegitcommit: c51de5e1a4cb9c4a7a9854a4226b32453d9e73e0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "48779212"
---
# <a name="get-started-with-endpoint-data-loss-prevention-preview"></a><span data-ttu-id="78775-103">Prise en main des points de terminaison de protection contre la perte de données (aperçu)</span><span class="sxs-lookup"><span data-stu-id="78775-103">Get started with Endpoint data loss prevention (preview)</span></span>

<span data-ttu-id="78775-104">Microsoft Points de terminaison Protection contre la perte de données (Endpoint DLP) fait partie de la suite de fonctionnalités Microsoft 365 de protection contre la perte de données (DLP) que vous pouvez utiliser pour découvrir et protéger les éléments sensibles dans les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="78775-104">Microsoft Endpoint data loss prevention (Endpoint DLP) is part of the Microsoft 365 data loss prevention (DLP) suite of features you can use to discover and protect sensitive items across Microsoft 365 services.</span></span> <span data-ttu-id="78775-105">Pour plus d’informations sur les offres DLP de Microsoft, voir [Vue d’ensemble de la protection contre la perte de données](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="78775-105">For more information about all of Microsoft’s DLP offerings, see [Overview of data loss prevention](data-loss-prevention-policies.md).</span></span> <span data-ttu-id="78775-106">Pour en savoir plus sur Endpoint DLP, voir [En savoir plus sur Points de terminaison Protection contre la perte de données (Preview)](endpoint-dlp-learn-about.md)</span><span class="sxs-lookup"><span data-stu-id="78775-106">To learn more about Endpoint DLP, see [Learn about Endpoint data loss prevention (preview)](endpoint-dlp-learn-about.md)</span></span>

<span data-ttu-id="78775-107">Microsoft Endpoint DLP vous permet de surveiller les appareils Windows 10 et de détecter les situations d’utilisation et de partage des éléments sensibles.</span><span class="sxs-lookup"><span data-stu-id="78775-107">Microsoft Endpoint DLP allows you to monitor Windows 10 devices and detect when sensitive items are used and shared.</span></span> <span data-ttu-id="78775-108">Ainsi, vous bénéficiez de la visibilité et du contrôle dont vous avez besoin pour vous assurer qu’ils sont utilisés et protégés correctement, et pour éviter tout comportement risqué susceptible de les compromettre.</span><span class="sxs-lookup"><span data-stu-id="78775-108">This gives you the visibility and control you need to ensure that they are used and protected properly, and to help prevent risky behavior that might compromise them.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="78775-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="78775-109">Before you begin</span></span>

### <a name="skusubscriptions-licensing"></a><span data-ttu-id="78775-110">Licences SKU/abonnements</span><span class="sxs-lookup"><span data-stu-id="78775-110">SKU/subscriptions licensing</span></span>

<span data-ttu-id="78775-111">Avant de commencer à utiliser point de terminaison DLP, vous devez confirmer votre [abonnement Microsoft 365](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) et tous les modules complémentaires.</span><span class="sxs-lookup"><span data-stu-id="78775-111">Before you get started with Endpoint DLP, you should confirm your [Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) and any add-ons.</span></span> <span data-ttu-id="78775-112">Pour accéder à la fonctionnalité de points de terminaison DLP et l’utiliser, vous devez disposer de l’un de ces abonnements ou modules complémentaires.</span><span class="sxs-lookup"><span data-stu-id="78775-112">To access and use Endpoint DLP functionality, you must have one of these subscriptions or add-ons.</span></span>

- <span data-ttu-id="78775-113">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="78775-113">Microsoft 365 E5</span></span>
- <span data-ttu-id="78775-114">Microsoft 365 A5 (EDU)</span><span class="sxs-lookup"><span data-stu-id="78775-114">Microsoft 365 A5 (EDU)</span></span>
- <span data-ttu-id="78775-115">Microsoft 365 E5 Conformité</span><span class="sxs-lookup"><span data-stu-id="78775-115">Microsoft 365 E5 compliance</span></span>
- <span data-ttu-id="78775-116">Microsoft 365 A5 Conformité</span><span class="sxs-lookup"><span data-stu-id="78775-116">Microsoft 365 A5 compliance</span></span>
- <span data-ttu-id="78775-117">Microsoft 365 E5, Protection des informations et gouvernance</span><span class="sxs-lookup"><span data-stu-id="78775-117">Microsoft 365 E5 information protection and governance</span></span>
- <span data-ttu-id="78775-118">Microsoft 365 A5, Protection des informations et gouvernance</span><span class="sxs-lookup"><span data-stu-id="78775-118">Microsoft 365 A5 information protection and governance</span></span>

### <a name="permissions"></a><span data-ttu-id="78775-119">Autorisations</span><span class="sxs-lookup"><span data-stu-id="78775-119">Permissions</span></span>

<span data-ttu-id="78775-120">Pour activer la gestion des appareils, le compte que vous utilisez doit être membre de l’un de ces rôles :</span><span class="sxs-lookup"><span data-stu-id="78775-120">To enable device management, the account you use must be a member of any one of these roles:</span></span>

- <span data-ttu-id="78775-121">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="78775-121">Global admin</span></span>
- <span data-ttu-id="78775-122">Administrateur de la sécurité</span><span class="sxs-lookup"><span data-stu-id="78775-122">Security admin</span></span>
- <span data-ttu-id="78775-123">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="78775-123">Compliance admin</span></span>

<span data-ttu-id="78775-124">Si vous voulez utiliser un compte personnalisé pour afficher les paramètres de gestion des appareils, celui-ci doit se trouver dans l’un de ces rôles :</span><span class="sxs-lookup"><span data-stu-id="78775-124">If you want to use a custom account to view the device management settings, it must be in one of these roles:</span></span>

- <span data-ttu-id="78775-125">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="78775-125">Global admin</span></span>
- <span data-ttu-id="78775-126">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="78775-126">Compliance admin</span></span>
- <span data-ttu-id="78775-127">Administrateur des données de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="78775-127">Compliance data admin</span></span>
- <span data-ttu-id="78775-128">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="78775-128">Global reader</span></span>

<span data-ttu-id="78775-129">Si vous voulez utiliser un compte personnalisé pour accéder à la page d’intégration/déclassement, celui-ci doit se trouver dans l’un de ces rôles :</span><span class="sxs-lookup"><span data-stu-id="78775-129">If you want to use a custom account to access the onboarding/offboarding page, it must be in one of these roles:</span></span>

- <span data-ttu-id="78775-130">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="78775-130">Global admin</span></span>
- <span data-ttu-id="78775-131">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="78775-131">Compliance admin</span></span>

<span data-ttu-id="78775-132">Si vous voulez utiliser un compte personnalisé pour activer/désactiver la surveillance de l’appareil, celui-ci doit se trouver dans l’un de ces rôles :</span><span class="sxs-lookup"><span data-stu-id="78775-132">If you want to use a custom account to turn on/off device monitoring, it must be in one of these roles:</span></span>

- <span data-ttu-id="78775-133">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="78775-133">Global admin</span></span>
- <span data-ttu-id="78775-134">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="78775-134">Compliance admin</span></span>

<span data-ttu-id="78775-135">Les données du point de terminaison DLP peuvent être affichées dans [l’Explorateur d’activités](data-classification-activity-explorer.md).</span><span class="sxs-lookup"><span data-stu-id="78775-135">Data from Endpoint DLP can be viewed in [Activity explorer](data-classification-activity-explorer.md).</span></span> <span data-ttu-id="78775-136">Il existe quatre rôles qui accordent l’autorisation à l’Explorateur d’activités, le compte que vous utilisez pour accéder aux données doit être membre de l’un d’eux.</span><span class="sxs-lookup"><span data-stu-id="78775-136">There are four roles that grant permission to activity explorer, the account you use for accessing the data must be a member of any one of them.</span></span>

- <span data-ttu-id="78775-137">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="78775-137">Global admin</span></span>
- <span data-ttu-id="78775-138">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="78775-138">Compliance admin</span></span>
- <span data-ttu-id="78775-139">Administrateur de la sécurité</span><span class="sxs-lookup"><span data-stu-id="78775-139">Security admin</span></span>
- <span data-ttu-id="78775-140">Administrateur des données de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="78775-140">Compliance data admin</span></span>

### <a name="prepare-your-endpoints"></a><span data-ttu-id="78775-141">Préparer vos points de terminaison</span><span class="sxs-lookup"><span data-stu-id="78775-141">Prepare your endpoints</span></span>

<span data-ttu-id="78775-142">Assurez-vous que les appareils Windows 10 pour lesquels vous envisagez de déployer le point de terminaison DLP répondent à ces exigences.</span><span class="sxs-lookup"><span data-stu-id="78775-142">Make sure that the Windows 10 devices that you plan on deploying Endpoint DLP to meet these requirements.</span></span>

1. <span data-ttu-id="78775-143">Vous devez exécuter Windows 10 x64 Build 1809 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="78775-143">Must be running Windows 10 x64 build 1809 or later.</span></span>

2. <span data-ttu-id="78775-144">La version du client anti-programme malveillant est 4.18.2009.7 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="78775-144">Antimalware Client Version is 4.18.2009.7 or newer.</span></span> <span data-ttu-id="78775-145">Vérifiez votre version actuelle à l’aide de l’application Sécurité Windows, sélectionnez l’icône Paramètres, puis À propos de.</span><span class="sxs-lookup"><span data-stu-id="78775-145">Check your current version by opening Windows Security app, select the Settings icon, and then select About.</span></span> <span data-ttu-id="78775-146">Le numéro de version est répertorié sous version du client anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="78775-146">The version number is listed under Antimalware Client Version.</span></span> <span data-ttu-id="78775-147">Effectuez une mise à jour vers la dernière version du client anti-programme malveillant en installant Windows Update KB4052623.</span><span class="sxs-lookup"><span data-stu-id="78775-147">Update to the latest Antimalware Client Version by installing Windows Update KB4052623.</span></span> <span data-ttu-id="78775-148">Remarque : aucune des composants de sécurité Windows ne doit être actif, vous pouvez exécuter la protection contre la perte de données de point de terminaison indépendamment de l’état de Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="78775-148">Note: None of Windows Security components need to be active, you can run Endpoint DLP independent of Windows Security status.</span></span>

3. <span data-ttu-id="78775-149">Les mises à jour Windows suivantes sont installées.</span><span class="sxs-lookup"><span data-stu-id="78775-149">The following Windows Updates are installed.</span></span> <span data-ttu-id="78775-150">Remarque : ces mises à jour ne sont pas des conditions préalables à l’intégration d’un appareil au DLP de point de terminaison , mais contiennent des correctifs pour les problèmes importants qui doivent donc être installés avant d’utiliser le produit.</span><span class="sxs-lookup"><span data-stu-id="78775-150">Note: These updates are not a pre-requisite to onboard a device to Endpoint DLP, but contain fixes for important issues thus must be installed before using the product.</span></span>

    - <span data-ttu-id="78775-151">Pour Windows 10 version 1809 : KB4559003, KB4577069, KB4580390</span><span class="sxs-lookup"><span data-stu-id="78775-151">For Windows 10 1809 - KB4559003, KB4577069, KB4580390</span></span>
    - <span data-ttu-id="78775-152">Pour Windows 10 version 1903 ou 1909 : KB4559004, KB4577062, KB4580386</span><span class="sxs-lookup"><span data-stu-id="78775-152">For Windows 10 1903 or 1909 - KB4559004, KB4577062, KB4580386</span></span>
    - <span data-ttu-id="78775-153">Pour Windows 10 version 2004 : KB4568831, KB4577063</span><span class="sxs-lookup"><span data-stu-id="78775-153">For Windows 10 2004 - KB4568831, KB4577063</span></span>
    - <span data-ttu-id="78775-154">Pour les appareils exécutant Office 2016 (et non aucune autre version d’Office) : KB4577063</span><span class="sxs-lookup"><span data-stu-id="78775-154">For devices running Office 2016 (and not any other Office version) - KB4577063</span></span> 

4. <span data-ttu-id="78775-155">Tous les appareils doivent être [joints à Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join) ou jointure hybride Azure AD.</span><span class="sxs-lookup"><span data-stu-id="78775-155">All devices must be [Azure Active Directory (Azure AD) joined](https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join), or Hybrid Azure AD joined.</span></span>

5. <span data-ttu-id="78775-156">Installez le navigateur Microsoft Chromium Edge sur l’appareil de point de terminaison afin d’appliquer des actions de stratégie pour l’activité de téléchargement vers le Cloud.</span><span class="sxs-lookup"><span data-stu-id="78775-156">Install Microsoft Chromium Edge browser on the endpoint device to enforce policy actions for the upload to cloud activity.</span></span> <span data-ttu-id="78775-157">[Télécharger le nouveau Microsoft Edge sur la base de chrome](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium).</span><span class="sxs-lookup"><span data-stu-id="78775-157">See, [Download the new Microsoft Edge based on Chromium](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium).</span></span>

## <a name="onboarding-devices-into-device-management"></a><span data-ttu-id="78775-158">Dispositifs d’intégration dans la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="78775-158">Onboarding devices into device management</span></span>

<span data-ttu-id="78775-159">Vous devez activer la surveillance des appareils et intégrer vos points de terminaison avant de pouvoir surveiller et protéger les éléments sensibles sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="78775-159">You must enable device monitoring and onboard your endpoints before you can monitor and protect sensitive items on a device.</span></span> <span data-ttu-id="78775-160">Ces deux actions sont effectuées dans le portail de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="78775-160">Both of these actions are done in the Microsoft 365 Compliance portal.</span></span>

<span data-ttu-id="78775-161">Lorsque vous voulez intégrer des appareils qui n’ont pas encore été intégrés, vous devez télécharger et déployer les scripts appropriés sur ces appareils.</span><span class="sxs-lookup"><span data-stu-id="78775-161">When you want to onboard devices that haven't been onboarded yet, you'll download the appropriate script and deploy it to those devices.</span></span> <span data-ttu-id="78775-162">Suivez la procédure [d’intégration d’appareils](endpoint-dlp-getting-started.md#onboarding-devices).</span><span class="sxs-lookup"><span data-stu-id="78775-162">Follow the [Onboarding devices procedure](endpoint-dlp-getting-started.md#onboarding-devices).</span></span>

<span data-ttu-id="78775-163">Si vous disposez déjà d’appareils incorporés dans [Microsoft Defender pour point de terminaison](https://docs.microsoft.com/windows/security/threat-protection/), ceux-ci apparaissent déjà dans la liste des périphériques gérés.</span><span class="sxs-lookup"><span data-stu-id="78775-163">If you already have devices onboarded into [Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection/), they will already appear in the managed devices list.</span></span> <span data-ttu-id="78775-164">Suivez la procédure [Appareils intégrés à Microsoft Defender pour point de terminaison](endpoint-dlp-getting-started.md#with-devices-onboarded-into-microsoft-defender-for- endpoint).</span><span class="sxs-lookup"><span data-stu-id="78775-164">Follow the [With devices onboarded into Microsoft Defender for Endpoint procedure](endpoint-dlp-getting-started.md#with-devices-onboarded-into-microsoft-defender-for- endpoint).</span></span>

### <a name="onboarding-devices"></a><span data-ttu-id="78775-165">Intégration des appareils</span><span class="sxs-lookup"><span data-stu-id="78775-165">Onboarding devices</span></span>

<span data-ttu-id="78775-166">Dans ce scénario de déploiement, vous allez intégrer des appareils qui n’ont pas encore été intégrés, et vous voulez simplement contrôler et protéger les éléments sensibles contre le partage involontaire sur les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="78775-166">In this deployment scenario, you'll onboard devices that have not been onboarded yet, and you just want to monitor and protect sensitive items from unintentional sharing on Windows 10 devices.</span></span>

1. <span data-ttu-id="78775-167">Ouvrez le [Centre de conformité Microsoft](https://compliance.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="78775-167">Open the [Microsoft compliance center](https://compliance.microsoft.com).</span></span>

2. <span data-ttu-id="78775-168">Ouvrez la page Paramètres du centre de conformité et sélectionnez **Appareils intégrés** .</span><span class="sxs-lookup"><span data-stu-id="78775-168">Open the Compliance Center settings page and choose **Onboard devices** .</span></span> 

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="78775-169">![activer la gestion des appareils](../media/endpoint-dlp-learn-about-1-enable-device-management.png)</span><span class="sxs-lookup"><span data-stu-id="78775-169">![enable device management](../media/endpoint-dlp-learn-about-1-enable-device-management.png)</span></span>

   > [!NOTE]
   > <span data-ttu-id="78775-170">Bien que l’activation de l’intégration des appareils dure généralement environ 60 secondes, patientez jusqu’à 30 minutes avant de contacter le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="78775-170">While it usually takes about 60 seconds for device onboarding to be enabled, please allow up to 30 minutes before engaging with Microsoft support.</span></span>

3. <span data-ttu-id="78775-171">Sélectionnez **Gestion des appareils** pour ouvrir la liste des **Appareils** .</span><span class="sxs-lookup"><span data-stu-id="78775-171">Choose **Device management** to open the **Devices** list.</span></span> <span data-ttu-id="78775-172">La liste est vide tant que vous n’avez pas intégré de périphériques.</span><span class="sxs-lookup"><span data-stu-id="78775-172">The list will be empty until you onboard devices.</span></span>

4. <span data-ttu-id="78775-173">Sélectionnez **Intégration** pour lancer le processus d’intégration.</span><span class="sxs-lookup"><span data-stu-id="78775-173">Choose **Onboarding** to begin the onboarding process.</span></span>

5. <span data-ttu-id="78775-174">Choisissez la manière dont vous voulez déployer ces autres appareils à partir de la liste **Méthode de déploiement** , puis **Télécharger le package** .</span><span class="sxs-lookup"><span data-stu-id="78775-174">Choose the way you want to deploy to these additional devices from the **Deployment method** list and then **download package** .</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="78775-175">![méthode de déploiement](../media/endpoint-dlp-getting-started-3-deployment-method.png)</span><span class="sxs-lookup"><span data-stu-id="78775-175">![deployment method](../media/endpoint-dlp-getting-started-3-deployment-method.png)</span></span>
   
6. <span data-ttu-id="78775-176">Suivez les procédures appropriées dans [Outils et méthodes d’intégration pour les ordinateurs Windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="78775-176">Follow the appropriate procedures in [Onboarding tools and methods for Windows 10 machines](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span></span> <span data-ttu-id="78775-177">Ce lien vous dirige vers une page d’accueil dans laquelle vous pouvez accéder aux procédures Microsoft Defender pour point de terminaison qui correspondent au package de déploiement que vous avez sélectionné à l’étape 5 :</span><span class="sxs-lookup"><span data-stu-id="78775-177">This link take you to a landing page where you can access Microsoft Defender for Endpoint procedures that match the deployment package you selected in step 5:</span></span>

    - <span data-ttu-id="78775-178">Intégrer les ordinateurs Windows 10 utilisant une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="78775-178">Onboard Windows 10 machines using Group Policy</span></span>
    - <span data-ttu-id="78775-179">Intégrer les ordinateurs Windows à l’aide du gestionnaire de configuration de point de terminaison Microsoft</span><span class="sxs-lookup"><span data-stu-id="78775-179">Onboard Windows machines using Microsoft Endpoint Configuration Manager</span></span>
    - <span data-ttu-id="78775-180">Intégrer les ordinateurs Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="78775-180">Onboard Windows 10 machines using Mobile Device Management tools</span></span>
    - <span data-ttu-id="78775-181">Intégrer les ordinateurs Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="78775-181">Onboard Windows 10 machines using a local script</span></span>
    - <span data-ttu-id="78775-182">Intégrer les ordinateurs virtuels d’infrastructure de bureau virtuel (VDI) non persistants.</span><span class="sxs-lookup"><span data-stu-id="78775-182">Onboard non-persistent virtual desktop infrastructure (VDI) machines.</span></span>

<span data-ttu-id="78775-183">Une fois l’opération effectuée et le point de terminaison intégré, celui-ci doit être visible dans la liste des appareils et commencer à créer des rapports d’activité d’audit dans l’Explorateur d’activités.</span><span class="sxs-lookup"><span data-stu-id="78775-183">Once done and endpoint is onboarded, it should be visible in the devices list and also start reporting audit activity logs to Activity explorer.</span></span>

> [!NOTE]
> <span data-ttu-id="78775-184">Cette expérience est sous l’application de la licence.</span><span class="sxs-lookup"><span data-stu-id="78775-184">This experience is under license enforcement.</span></span> <span data-ttu-id="78775-185">Sans la licence requise, les données ne sont pas visibles ni accessibles.</span><span class="sxs-lookup"><span data-stu-id="78775-185">Without the required license, data will not be visible or accessible.</span></span>

### <a name="with-devices-onboarded-into-microsoft-defender-for-endpoint"></a><span data-ttu-id="78775-186">Appareils intégrés à Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="78775-186">With devices onboarded into Microsoft Defender for Endpoint</span></span>

<span data-ttu-id="78775-187">Dans ce scénario, Microsoft Defender pour point de terminaison est déjà déployé et des points de terminaison y sont signalés.</span><span class="sxs-lookup"><span data-stu-id="78775-187">In this scenario, Microsoft Defender for Endpoint is already deployed and there are endpoints reporting in.</span></span> <span data-ttu-id="78775-188">Tous ces points de terminaison s’affichent dans la liste des appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="78775-188">All these endpoints will appear in the managed devices list.</span></span> <span data-ttu-id="78775-189">Vous pouvez continuer à intégrer de nouveaux appareils dans le point de terminaison DLP pour étendre la couverture à l’aide de la [procédure d’intégration d’appareils](endpoint-dlp-getting-started.md#onboarding-devices).</span><span class="sxs-lookup"><span data-stu-id="78775-189">You can continue to onboard new devices into Endpoint DLP to expand coverage by using the [Onboarding devices procedure](endpoint-dlp-getting-started.md#onboarding-devices).</span></span>

1. <span data-ttu-id="78775-190">Ouvrez le [Centre de conformité Microsoft](https://compliance.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="78775-190">Open the [Microsoft compliance center](https://compliance.microsoft.com).</span></span>

2. <span data-ttu-id="78775-191">Ouvrez la page Paramètres du centre de conformité et sélectionnez **Activer la surveillance d’appareils** .</span><span class="sxs-lookup"><span data-stu-id="78775-191">Open the Compliance Center settings page and choose **Enable device monitoring** .</span></span>

3. <span data-ttu-id="78775-192">Sélectionnez **Gestion des appareils** pour ouvrir la liste des **Appareils** .</span><span class="sxs-lookup"><span data-stu-id="78775-192">Choose **Device management** to open the **Devices** list.</span></span> <span data-ttu-id="78775-193">Vous devriez voir apparaître la liste des appareils qui signalent déjà à Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="78775-193">You should see the list of devices that are already reporting in to Microsoft Defender for Endpoint.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="78775-194">![Gestion des appareils](../media/endpoint-dlp-getting-started-2-device-management.png)</span><span class="sxs-lookup"><span data-stu-id="78775-194">![device management](../media/endpoint-dlp-getting-started-2-device-management.png)</span></span>
   
4. <span data-ttu-id="78775-195">Sélectionnez **Intégration** si vous avez besoin d’intégrer d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="78775-195">Choose **Onboarding** if you need to onboard additional devices.</span></span>

5. <span data-ttu-id="78775-196">Choisissez la manière dont vous voulez déployer ces autres appareils à partir de la liste **Méthode de déploiement** , puis **Télécharger le package** .</span><span class="sxs-lookup"><span data-stu-id="78775-196">Choose the way you want to deploy to these additional devices from the **Deployment method** list and then **Download package** .</span></span>

6. <span data-ttu-id="78775-197">Suivez les procédures appropriées dans [Outils et méthodes d’intégration pour les ordinateurs Windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="78775-197">Follow the appropriate procedures in [Onboarding tools and methods for Windows 10 machines](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span></span> <span data-ttu-id="78775-198">Ce lien vous dirige vers une page d’accueil dans laquelle vous pouvez accéder aux procédures Microsoft Defender pour point de terminaison qui correspondent au package de déploiement que vous avez sélectionné à l’étape 5 :</span><span class="sxs-lookup"><span data-stu-id="78775-198">This link take you to a landing page where you can access Microsoft Defender for Endpoint procedures that match the deployment package you selected in step 5:</span></span>

    - <span data-ttu-id="78775-199">Intégrer les ordinateurs Windows 10 utilisant une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="78775-199">Onboard Windows 10 machines using Group Policy</span></span>
    - <span data-ttu-id="78775-200">Intégrer les ordinateurs Windows à l’aide du gestionnaire de configuration de point de terminaison Microsoft</span><span class="sxs-lookup"><span data-stu-id="78775-200">Onboard Windows machines using Microsoft Endpoint Configuration Manager</span></span>
    - <span data-ttu-id="78775-201">Intégrer les ordinateurs Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="78775-201">Onboard Windows 10 machines using Mobile Device Management tools</span></span>
    - <span data-ttu-id="78775-202">Intégrer les ordinateurs Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="78775-202">Onboard Windows 10 machines using a local script</span></span>
    - <span data-ttu-id="78775-203">Intégrer les ordinateurs virtuels d’infrastructure de bureau virtuel (VDI) non persistants.</span><span class="sxs-lookup"><span data-stu-id="78775-203">Onboard non-persistent virtual desktop infrastructure (VDI) machines.</span></span>

<span data-ttu-id="78775-204">Une fois l’opération effectuée et le point de terminaison intégré, celui-ci doit être visible dans le tableau des **Appareils** et commencer à créer des rapports d’activité d’audit dans l’ **Explorateur d’activités** .</span><span class="sxs-lookup"><span data-stu-id="78775-204">Once done and endpoint is onboarded, it should be visible under the **Devices** table and also start reporting audit logs to the **Activity Explorer** .</span></span>

> [!NOTE]
><span data-ttu-id="78775-205">Cette expérience est sous l’application de la licence.</span><span class="sxs-lookup"><span data-stu-id="78775-205">This experience is under license enforcement.</span></span> <span data-ttu-id="78775-206">Sans la licence requise, les données ne sont pas visibles ni accessibles.</span><span class="sxs-lookup"><span data-stu-id="78775-206">Without the required license, data will not be visible or accessible.</span></span>

### <a name="viewing-endpoint-dlp-data-in-activity-explorer"></a><span data-ttu-id="78775-207">Affichage de données DLP de point de terminaison dans l’Explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="78775-207">Viewing Endpoint DLP data in activity explorer</span></span>

1. <span data-ttu-id="78775-208">Ouvrez la [Page classification des données](https://compliance.microsoft.com/dataclassification?viewid=overview) pour votre domaine dans le centre de conformité Microsoft 365, puis sélectionnez Explorateur d’activités.</span><span class="sxs-lookup"><span data-stu-id="78775-208">Open the [Data classification page](https://compliance.microsoft.com/dataclassification?viewid=overview) for your domain in the Microsoft 365 Compliance center and choose Activity explorer.</span></span>

2. <span data-ttu-id="78775-209">Reportez-vous aux procédures décrites dans [Prise en main de l’Explorateur d’activités](data-classification-activity-explorer.md) pour accéder aux données de vos appareils de point de terminaison et les filtrer.</span><span class="sxs-lookup"><span data-stu-id="78775-209">Refer to the procedures in [Get started with Activity explorer](data-classification-activity-explorer.md) to access and filter all the data for your Endpoint devices.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="78775-210">![filtre de l’Explorateur d’activités pour les appareils de point de terminaison](../media/endpoint-dlp-4-getting-started-activity-explorer.png)</span><span class="sxs-lookup"><span data-stu-id="78775-210">![activity explorer filter for endpoint devices](../media/endpoint-dlp-4-getting-started-activity-explorer.png)</span></span>

## <a name="next-steps"></a><span data-ttu-id="78775-211">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="78775-211">Next steps</span></span>
<span data-ttu-id="78775-212">Maintenant que vous disposez d’appareils intégrés et que vous pouvez afficher les données d’activité dans l’Explorateur d’activités, vous êtes prêt à passer à l’étape suivante dans laquelle vous créez des stratégies DLP qui protègent vos éléments sensibles.</span><span class="sxs-lookup"><span data-stu-id="78775-212">Now that you have onboarded devices and can view the activity data in Activity explorer, you are ready to move on to your next step where you create DLP policies that protect your sensitive items.</span></span>

- [<span data-ttu-id="78775-213">Utilisation des points de terminaison de protection contre la perte de données (aperçu)</span><span class="sxs-lookup"><span data-stu-id="78775-213">Using Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-using.md)

## <a name="see-also"></a><span data-ttu-id="78775-214">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78775-214">See also</span></span>

- [<span data-ttu-id="78775-215">En savoir plus sur les points de terminaison de protection contre la perte de données (Preview)</span><span class="sxs-lookup"><span data-stu-id="78775-215">Learn about Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-learn-about.md)
- [<span data-ttu-id="78775-216">Utilisation des points de terminaison de protection contre la perte de données (aperçu)</span><span class="sxs-lookup"><span data-stu-id="78775-216">Using Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-using.md)
- [<span data-ttu-id="78775-217">Vue d’ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="78775-217">Overview of data loss prevention</span></span>](data-loss-prevention-policies.md)
- [<span data-ttu-id="78775-218">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="78775-218">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="78775-219">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="78775-219">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="78775-220">Microsoft Defender – Protection avancée contre les menaces (Microsoft Defender ATP)</span><span class="sxs-lookup"><span data-stu-id="78775-220">Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP)</span></span>](https://docs.microsoft.com/windows/security/threat-protection/)
- <span data-ttu-id="78775-221">[Outils et méthodes d’intégration pour les appareils Windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="78775-221">[Onboarding tools and methods for Windows 10 machines](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints)</span></span>
- [<span data-ttu-id="78775-222">Abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="78775-222">Microsoft 365 subscription</span></span>](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1)
- [<span data-ttu-id="78775-223">Azure AD appareils joints</span><span class="sxs-lookup"><span data-stu-id="78775-223">Azure AD joined devices</span></span>](https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join)
- [<span data-ttu-id="78775-224">Télécharger le nouveau Microsoft Edge sur la base de chrome</span><span class="sxs-lookup"><span data-stu-id="78775-224">Download the new Microsoft Edge based on Chromium</span></span>](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium)
