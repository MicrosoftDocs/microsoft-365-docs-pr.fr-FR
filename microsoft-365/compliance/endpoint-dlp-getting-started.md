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
- SPO_Content
search.appverid:
- MET150
description: Configurez les points de terminaison contre la protection contre la perte de données Microsoft 365 pour surveiller les activités des fichiers et implémenter des actions de protection pour ces fichiers aux points de terminaison.
ms.openlocfilehash: 43ab2a30570f153f16819ede2eeed1f0e091da74
ms.sourcegitcommit: dffb9b72acd2e0bd286ff7e79c251e7ec6e8ecae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "47949844"
---
# <a name="get-started-with-endpoint-data-loss-prevention-preview"></a><span data-ttu-id="dc976-103">Prise en main des points de terminaison de protection contre la perte de données (aperçu)</span><span class="sxs-lookup"><span data-stu-id="dc976-103">Get started with Endpoint data loss prevention (preview)</span></span>

<span data-ttu-id="dc976-104">Microsoft Points de terminaison Protection contre la perte de données (Endpoint DLP) fait partie de la suite de fonctionnalités Microsoft 365 de protection contre la perte de données (DLP) que vous pouvez utiliser pour découvrir et protéger les éléments sensibles dans les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="dc976-104">Microsoft Endpoint data loss prevention (Endpoint DLP) is part of the Microsoft 365 data loss prevention (DLP) suite of features you can use to discover and protect sensitive items across Microsoft 365 services.</span></span> <span data-ttu-id="dc976-105">Pour plus d’informations sur les offres DLP de Microsoft, voir [Vue d’ensemble de la protection contre la perte de données](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="dc976-105">For more information about all of Microsoft’s DLP offerings, see [Overview of data loss prevention](data-loss-prevention-policies.md).</span></span> <span data-ttu-id="dc976-106">Pour en savoir plus sur Endpoint DLP, voir [En savoir plus sur Points de terminaison Protection contre la perte de données (Preview)](endpoint-dlp-learn-about.md)</span><span class="sxs-lookup"><span data-stu-id="dc976-106">To learn more about Endpoint DLP, see [Learn about Endpoint data loss prevention (preview)](endpoint-dlp-learn-about.md)</span></span>

<span data-ttu-id="dc976-107">Microsoft Endpoint DLP vous permet de surveiller les appareils Windows 10 et de détecter les situations d’utilisation et de partage des éléments sensibles.</span><span class="sxs-lookup"><span data-stu-id="dc976-107">Microsoft Endpoint DLP allows you to monitor Windows 10 devices and detect when sensitive items are used and shared.</span></span> <span data-ttu-id="dc976-108">Ainsi, vous bénéficiez de la visibilité et du contrôle dont vous avez besoin pour vous assurer qu’ils sont utilisés et protégés correctement, et pour éviter tout comportement risqué susceptible de les compromettre.</span><span class="sxs-lookup"><span data-stu-id="dc976-108">This gives you the visibility and control you need to ensure that they are used and protected properly, and to help prevent risky behavior that might compromise them.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="dc976-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="dc976-109">Before you begin</span></span>

### <a name="skusubscriptions-licensing"></a><span data-ttu-id="dc976-110">Licences SKU/abonnements</span><span class="sxs-lookup"><span data-stu-id="dc976-110">SKU/subscriptions licensing</span></span>

<span data-ttu-id="dc976-111">Avant de commencer à utiliser point de terminaison DLP, vous devez confirmer votre [abonnement Microsoft 365](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) et tous les modules complémentaires.</span><span class="sxs-lookup"><span data-stu-id="dc976-111">Before you get started with Endpoint DLP, you should confirm your [Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) and any add-ons.</span></span> <span data-ttu-id="dc976-112">Pour accéder à la fonctionnalité de points de terminaison DLP et l’utiliser, vous devez disposer de l’un de ces abonnements ou modules complémentaires.</span><span class="sxs-lookup"><span data-stu-id="dc976-112">To access and use Endpoint DLP functionality, you must have one of these subscriptions or add-ons.</span></span>

- <span data-ttu-id="dc976-113">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="dc976-113">Microsoft 365 E5</span></span>
- <span data-ttu-id="dc976-114">Microsoft 365 A5 (EDU)</span><span class="sxs-lookup"><span data-stu-id="dc976-114">Microsoft 365 A5 (EDU)</span></span>
- <span data-ttu-id="dc976-115">Microsoft 365 E5 Conformité</span><span class="sxs-lookup"><span data-stu-id="dc976-115">Microsoft 365 E5 compliance</span></span>
- <span data-ttu-id="dc976-116">Microsoft 365 A5 Conformité</span><span class="sxs-lookup"><span data-stu-id="dc976-116">Microsoft 365 A5 compliance</span></span>
- <span data-ttu-id="dc976-117">Microsoft 365 E5, Protection des informations et gouvernance</span><span class="sxs-lookup"><span data-stu-id="dc976-117">Microsoft 365 E5 information protection and governance</span></span>
- <span data-ttu-id="dc976-118">Microsoft 365 A5, Protection des informations et gouvernance</span><span class="sxs-lookup"><span data-stu-id="dc976-118">Microsoft 365 A5 information protection and governance</span></span>

### <a name="permissions"></a><span data-ttu-id="dc976-119">Autorisations</span><span class="sxs-lookup"><span data-stu-id="dc976-119">Permissions</span></span>

<span data-ttu-id="dc976-120">Pour activer la gestion des appareils, le compte que vous utilisez doit être membre de l’un de ces rôles :</span><span class="sxs-lookup"><span data-stu-id="dc976-120">To enable device management, the account you use must be a member of any one of these roles:</span></span>

- <span data-ttu-id="dc976-121">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="dc976-121">Global admin</span></span>
- <span data-ttu-id="dc976-122">Administrateur de la sécurité</span><span class="sxs-lookup"><span data-stu-id="dc976-122">Security admin</span></span>
- <span data-ttu-id="dc976-123">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="dc976-123">Compliance admin</span></span>

<span data-ttu-id="dc976-124">Si vous voulez utiliser un compte personnalisé pour afficher les paramètres de gestion des appareils, celui-ci doit se trouver dans l’un de ces rôles :</span><span class="sxs-lookup"><span data-stu-id="dc976-124">If you want to use a custom account to view the device management settings, it must be in one of these roles:</span></span>

- <span data-ttu-id="dc976-125">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="dc976-125">Global admin</span></span>
- <span data-ttu-id="dc976-126">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="dc976-126">Compliance admin</span></span>
- <span data-ttu-id="dc976-127">Administrateur des données de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="dc976-127">Compliance data admin</span></span>
- <span data-ttu-id="dc976-128">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="dc976-128">Global reader</span></span>

<span data-ttu-id="dc976-129">Si vous voulez utiliser un compte personnalisé pour accéder à la page d’intégration/déclassement, celui-ci doit se trouver dans l’un de ces rôles :</span><span class="sxs-lookup"><span data-stu-id="dc976-129">If you want to use a custom account to access the onboarding/offboarding page, it must be in one of these roles:</span></span>

- <span data-ttu-id="dc976-130">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="dc976-130">Global admin</span></span>
- <span data-ttu-id="dc976-131">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="dc976-131">Compliance admin</span></span>

<span data-ttu-id="dc976-132">Si vous voulez utiliser un compte personnalisé pour activer/désactiver la surveillance de l’appareil, celui-ci doit se trouver dans l’un de ces rôles :</span><span class="sxs-lookup"><span data-stu-id="dc976-132">If you want to use a custom account to turn on/off device monitoring, it must be in one of these roles:</span></span>

- <span data-ttu-id="dc976-133">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="dc976-133">Global admin</span></span>
- <span data-ttu-id="dc976-134">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="dc976-134">Compliance admin</span></span>

<span data-ttu-id="dc976-135">Les données du point de terminaison DLP peuvent être affichées dans [l’Explorateur d’activités](data-classification-activity-explorer.md).</span><span class="sxs-lookup"><span data-stu-id="dc976-135">Data from Endpoint DLP can be viewed in [Activity explorer](data-classification-activity-explorer.md).</span></span> <span data-ttu-id="dc976-136">Il existe quatre rôles qui accordent l’autorisation à l’Explorateur d’activités, le compte que vous utilisez pour accéder aux données doit être membre de l’un d’eux.</span><span class="sxs-lookup"><span data-stu-id="dc976-136">There are four roles that grant permission to activity explorer, the account you use for accessing the data must be a member of any one of them.</span></span>

- <span data-ttu-id="dc976-137">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="dc976-137">Global admin</span></span>
- <span data-ttu-id="dc976-138">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="dc976-138">Compliance admin</span></span>
- <span data-ttu-id="dc976-139">Administrateur de la sécurité</span><span class="sxs-lookup"><span data-stu-id="dc976-139">Security admin</span></span>
- <span data-ttu-id="dc976-140">Administrateur des données de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="dc976-140">Compliance data admin</span></span>

### <a name="prepare-your-endpoints"></a><span data-ttu-id="dc976-141">Préparer vos points de terminaison</span><span class="sxs-lookup"><span data-stu-id="dc976-141">Prepare your endpoints</span></span>

<span data-ttu-id="dc976-142">Assurez-vous que les appareils Windows 10 pour lesquels vous envisagez de déployer le point de terminaison DLP répondent à ces exigences.</span><span class="sxs-lookup"><span data-stu-id="dc976-142">Make sure that the Windows 10 devices that you plan on deploying Endpoint DLP to meet these requirements.</span></span>

1. <span data-ttu-id="dc976-143">Vous devez exécuter Windows 10 Build 1809 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="dc976-143">Must be running Windows 10 build 1809 or up.</span></span>
2. <span data-ttu-id="dc976-144">Tous les appareils doivent être [joints à Azure Active Directory (AAD)](https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join) ou joints à Azure AD Hybride.</span><span class="sxs-lookup"><span data-stu-id="dc976-144">All devices must be [Azure Active Directory (AAD) joined](https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join), or Hybrid Azure AD joined.</span></span>
3. <span data-ttu-id="dc976-145">Installez le navigateur Microsoft Chromium Edge sur l’appareil de point de terminaison afin d’appliquer des actions de stratégie pour l’activité de téléchargement vers le Cloud.</span><span class="sxs-lookup"><span data-stu-id="dc976-145">Install Microsoft Chromium Edge browser on the endpoint device to enforce policy actions for the upload to cloud activity.</span></span> <span data-ttu-id="dc976-146">[Télécharger le nouveau Microsoft Edge sur la base de chrome](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium).</span><span class="sxs-lookup"><span data-stu-id="dc976-146">See, [Download the new Microsoft Edge based on Chromium](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium).</span></span>

## <a name="onboarding-devices-into-device-management"></a><span data-ttu-id="dc976-147">Dispositifs d’intégration dans la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="dc976-147">Onboarding devices into device management</span></span>

 <span data-ttu-id="dc976-148">Vous devez activer la surveillance des appareils et intégrer vos points de terminaison avant de pouvoir surveiller et protéger les éléments sensibles sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="dc976-148">You must enable device monitoring and onboard your endpoints before you can monitor and protect sensitive items on a device.</span></span> <span data-ttu-id="dc976-149">Ces deux actions sont effectuées dans le portail de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="dc976-149">Both of these actions are done in the Microsoft 365 Compliance portal.</span></span>

<span data-ttu-id="dc976-150">Lorsque vous voulez intégrer des appareils qui n’ont pas encore été intégrés, vous devez télécharger et déployer les scripts appropriés sur ces appareils.</span><span class="sxs-lookup"><span data-stu-id="dc976-150">When you want to onboard devices that haven't been onboarded yet, you'll download the appropriate script and deploy it to those devices.</span></span> <span data-ttu-id="dc976-151">Suivez la procédure [d’intégration d’appareils](endpoint-dlp-getting-started.md#onboarding-devices).</span><span class="sxs-lookup"><span data-stu-id="dc976-151">Follow the [Onboarding devices procedure](endpoint-dlp-getting-started.md#onboarding-devices).</span></span>

<span data-ttu-id="dc976-152">Si vous disposez déjà d’appareils incorporés dans [Microsoft Defender Advanced Threat Protection (MDATP](https://docs.microsoft.com/windows/security/threat-protection/)), ceux-ci apparaissent déjà dans la liste des périphériques gérés.</span><span class="sxs-lookup"><span data-stu-id="dc976-152">If you already have devices onboarded into [Microsoft Defender Advanced Threat Protection (MDATP)](https://docs.microsoft.com/windows/security/threat-protection/), they will already appear in the managed devices list.</span></span> <span data-ttu-id="dc976-153">Suivez [Avec les appareils intégrés à la procédure MDATP](endpoint-dlp-getting-started.md#with-devices-onboarded-into-mdatp).</span><span class="sxs-lookup"><span data-stu-id="dc976-153">Follow the [With devices onboarded into MDATP procedure](endpoint-dlp-getting-started.md#with-devices-onboarded-into-mdatp).</span></span>

### <a name="onboarding-devices"></a><span data-ttu-id="dc976-154">Intégration des appareils</span><span class="sxs-lookup"><span data-stu-id="dc976-154">Onboarding devices</span></span>

<span data-ttu-id="dc976-155">Dans ce scénario de déploiement, vous allez intégrer des appareils qui n’ont pas encore été intégrés, et vous voulez simplement contrôler et protéger les éléments sensibles contre le partage involontaire sur les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="dc976-155">In this deployment scenario, you'll onboard devices that have not been onboarded yet, and you just want to monitor and protect sensitive items from unintentional sharing on Windows 10 devices.</span></span>

1. <span data-ttu-id="dc976-156">Ouvrez le [Centre de conformité Microsoft](https://compliance.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="dc976-156">Open the [Microsoft compliance center](https://compliance.microsoft.com).</span></span>
2. <span data-ttu-id="dc976-157">Ouvrez la page Paramètres du centre de conformité et sélectionnez **Appareils intégrés**.</span><span class="sxs-lookup"><span data-stu-id="dc976-157">Open the Compliance Center settings page and choose **Onboard devices**.</span></span> 

   ![activer la gestion des appareils](../media/endpoint-dlp-learn-about-1-enable-device-management.png)

   > [!NOTE]
   > <span data-ttu-id="dc976-159">Bien que l’activation de l’intégration des appareils dure généralement environ 60 secondes, patientez jusqu’à 30 minutes avant de contacter le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dc976-159">While it usually takes about 60 seconds for device onboarding to be enabled, please allow up to 30 minutes before engaging with Microsoft support.</span></span>

3. <span data-ttu-id="dc976-160">Sélectionnez **Gestion des appareils** pour ouvrir la liste des **Appareils**.</span><span class="sxs-lookup"><span data-stu-id="dc976-160">Choose **Device management** to open the **Devices** list.</span></span> <span data-ttu-id="dc976-161">La liste est vide tant que vous n’avez pas intégré de périphériques.</span><span class="sxs-lookup"><span data-stu-id="dc976-161">The list will be empty until you onboard devices.</span></span>
4. <span data-ttu-id="dc976-162">Sélectionnez **Intégration** pour lancer le processus d’intégration.</span><span class="sxs-lookup"><span data-stu-id="dc976-162">Choose **Onboarding** to begin the onboarding process.</span></span>
5. <span data-ttu-id="dc976-163">Choisissez la manière dont vous voulez déployer ces autres appareils à partir de la liste**Méthode de déploiement**, puis **Télécharger le package**.</span><span class="sxs-lookup"><span data-stu-id="dc976-163">Choose the way you want to deploy to these additional devices from the **Deployment method** list and then **download package**.</span></span>

   ![Méthode de déploiement](../media/endpoint-dlp-getting-started-3-deployment-method.png)
6. <span data-ttu-id="dc976-165">Suivez les procédures appropriées dans [Outils et méthodes d’intégration pour les ordinateurs Windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="dc976-165">Follow the appropriate procedures in [Onboarding tools and methods for Windows 10 machines](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span></span> <span data-ttu-id="dc976-166">Ce lien vous permet d’accéder à une page d’accueil dans laquelle vous pouvez accéder aux procédures MDATP qui correspondent au package de déploiement que vous avez sélectionné à l’étape 5 :</span><span class="sxs-lookup"><span data-stu-id="dc976-166">This link take you to a landing page where you can access MDATP procedures that match the deployment package you selected in step 5:</span></span>
    - <span data-ttu-id="dc976-167">Intégrer les ordinateurs Windows 10 utilisant une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="dc976-167">Onboard Windows 10 machines using Group Policy</span></span>
    - <span data-ttu-id="dc976-168">Intégrer les ordinateurs Windows à l’aide du gestionnaire de configuration de point de terminaison Microsoft</span><span class="sxs-lookup"><span data-stu-id="dc976-168">Onboard Windows machines using Microsoft Endpoint Configuration Manager</span></span>
    - <span data-ttu-id="dc976-169">Intégrer les ordinateurs Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="dc976-169">Onboard Windows 10 machines using Mobile Device Management tools</span></span>
    - <span data-ttu-id="dc976-170">Intégrer les ordinateurs Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="dc976-170">Onboard Windows 10 machines using a local script</span></span>
    - <span data-ttu-id="dc976-171">Intégrer les ordinateurs virtuels d’infrastructure de bureau virtuel (VDI) non persistants.</span><span class="sxs-lookup"><span data-stu-id="dc976-171">Onboard non-persistent virtual desktop infrastructure (VDI) machines.</span></span>

<span data-ttu-id="dc976-172">Une fois l’opération effectuée et le point de terminaison intégré, celui-ci doit être visible dans la liste des appareils et commencer à créer des rapports d’activité d’audit dans l’Explorateur d’activités.</span><span class="sxs-lookup"><span data-stu-id="dc976-172">Once done and endpoint is onboarded, it should be visible in the devices list and also start reporting audit activity logs to Activity explorer.</span></span>

> [!NOTE]
> <span data-ttu-id="dc976-173">Cette expérience est sous l’application de la licence.</span><span class="sxs-lookup"><span data-stu-id="dc976-173">This experience is under license enforcement.</span></span> <span data-ttu-id="dc976-174">Sans la licence requise, les données ne sont pas visibles ni accessibles.</span><span class="sxs-lookup"><span data-stu-id="dc976-174">Without the required license, data will not be visible or accessible.</span></span>

### <a name="with-devices-onboarded-into-mdatp"></a><span data-ttu-id="dc976-175">Avec les appareils intégrés à MDATP</span><span class="sxs-lookup"><span data-stu-id="dc976-175">With devices onboarded into MDATP</span></span>

<span data-ttu-id="dc976-176">Dans ce scénario, MDATP est déjà déployé et des points de terminaison y sont reportés.</span><span class="sxs-lookup"><span data-stu-id="dc976-176">In this scenario, MDATP is already deployed and there are endpoints reporting in.</span></span> <span data-ttu-id="dc976-177">Tous ces points de terminaison s’affichent dans la liste des appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="dc976-177">All these endpoints will appear in the managed devices list.</span></span> <span data-ttu-id="dc976-178">Vous pouvez continuer à intégrer de nouveaux appareils dans le point de terminaison DLP pour étendre la couverture à l’aide de la [procédure d’intégration d’appareils](endpoint-dlp-getting-started.md#onboarding-devices).</span><span class="sxs-lookup"><span data-stu-id="dc976-178">You can continue to onboard new devices into Endpoint DLP to expand coverage by using the [Onboarding devices procedure](endpoint-dlp-getting-started.md#onboarding-devices).</span></span>

1. <span data-ttu-id="dc976-179">Ouvrez le [Centre de conformité Microsoft](https://compliance.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="dc976-179">Open the [Microsoft compliance center](https://compliance.microsoft.com).</span></span>
2. <span data-ttu-id="dc976-180">Ouvrez la page Paramètres du centre de conformité et sélectionnez **Activer la surveillance d’appareils**.</span><span class="sxs-lookup"><span data-stu-id="dc976-180">Open the Compliance Center settings page and choose **Enable device monitoring**.</span></span>
3. <span data-ttu-id="dc976-181">Sélectionnez **Gestion des appareils** pour ouvrir la liste des **Appareils**.</span><span class="sxs-lookup"><span data-stu-id="dc976-181">Choose **Device management** to open the **Devices** list.</span></span> <span data-ttu-id="dc976-182">Vous devriez voir la liste des appareils qui signalent déjà les MDATP.</span><span class="sxs-lookup"><span data-stu-id="dc976-182">You should see the list of devices that are already reporting in to MDATP.</span></span> <span data-ttu-id="dc976-183">![Gestion des appareils](../media/endpoint-dlp-getting-started-2-device-management.png)</span><span class="sxs-lookup"><span data-stu-id="dc976-183">![device management](../media/endpoint-dlp-getting-started-2-device-management.png)</span></span>
4. <span data-ttu-id="dc976-184">Sélectionnez **Intégration** si vous avez besoin d’intégrer d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="dc976-184">Choose **Onboarding** if you need to onboard additional devices.</span></span>
5. <span data-ttu-id="dc976-185">Choisissez la manière dont vous voulez déployer ces autres appareils à partir de la liste**Méthode de déploiement**, puis **Télécharger le package**.</span><span class="sxs-lookup"><span data-stu-id="dc976-185">Choose the way you want to deploy to these additional devices from the **Deployment method** list and then **Download package**.</span></span>
6. <span data-ttu-id="dc976-186">Suivez les procédures appropriées dans [Outils et méthodes d’intégration pour les ordinateurs Windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="dc976-186">Follow the appropriate procedures in [Onboarding tools and methods for Windows 10 machines](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span></span> <span data-ttu-id="dc976-187">Ce lien vous permet d’accéder à une page d’accueil dans laquelle vous pouvez accéder aux procédures MDATP qui correspondent au package de déploiement que vous avez sélectionné à l’étape 5 :</span><span class="sxs-lookup"><span data-stu-id="dc976-187">This link take you to a landing page where you can access MDATP procedures that match the deployment package you selected in step 5:</span></span>
    - <span data-ttu-id="dc976-188">Intégrer les ordinateurs Windows 10 utilisant une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="dc976-188">Onboard Windows 10 machines using Group Policy</span></span>
    - <span data-ttu-id="dc976-189">Intégrer les ordinateurs Windows à l’aide du gestionnaire de configuration de point de terminaison Microsoft</span><span class="sxs-lookup"><span data-stu-id="dc976-189">Onboard Windows machines using Microsoft Endpoint Configuration Manager</span></span>
    - <span data-ttu-id="dc976-190">Intégrer les ordinateurs Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="dc976-190">Onboard Windows 10 machines using Mobile Device Management tools</span></span>
    - <span data-ttu-id="dc976-191">Intégrer les ordinateurs Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="dc976-191">Onboard Windows 10 machines using a local script</span></span>
    - <span data-ttu-id="dc976-192">Intégrer les ordinateurs virtuels d’infrastructure de bureau virtuel (VDI) non persistants.</span><span class="sxs-lookup"><span data-stu-id="dc976-192">Onboard non-persistent virtual desktop infrastructure (VDI) machines.</span></span>

<span data-ttu-id="dc976-193">Une fois l’opération effectuée et le point de terminaison intégré, celui-ci doit être visible dans le tableau des **Appareils** et commencer à créer des rapports d’activité d’audit dans l’**Explorateur d’activités**.</span><span class="sxs-lookup"><span data-stu-id="dc976-193">Once done and endpoint is onboarded, it should be visible under the **Devices** table and also start reporting audit logs to the **Activity Explorer**.</span></span>

> [!NOTE]
><span data-ttu-id="dc976-194">Cette expérience est sous l’application de la licence.</span><span class="sxs-lookup"><span data-stu-id="dc976-194">This experience is under license enforcement.</span></span> <span data-ttu-id="dc976-195">Sans la licence requise, les données ne sont pas visibles ni accessibles.</span><span class="sxs-lookup"><span data-stu-id="dc976-195">Without the required license, data will not be visible or accessible.</span></span>

### <a name="viewing-endpoint-dlp-data-in-activity-explorer"></a><span data-ttu-id="dc976-196">Affichage de données DLP de point de terminaison dans l’Explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="dc976-196">Viewing Endpoint DLP data in activity explorer</span></span>

1. <span data-ttu-id="dc976-197">Ouvrez la [Page classification des données](https://compliance.microsoft.com/dataclassification?viewid=overview) pour votre domaine dans le centre de conformité Microsoft 365, puis sélectionnez Explorateur d’activités.</span><span class="sxs-lookup"><span data-stu-id="dc976-197">Open the [Data classification page](https://compliance.microsoft.com/dataclassification?viewid=overview) for your domain in the Microsoft 365 Compliance center and choose Activity explorer.</span></span>
2. <span data-ttu-id="dc976-198">Reportez-vous aux procédures décrites dans [Prise en main de l’Explorateur d’activités](data-classification-activity-explorer.md) pour accéder aux données de vos appareils de point de terminaison et les filtrer.</span><span class="sxs-lookup"><span data-stu-id="dc976-198">Refer to the procedures in [Get started with Activity explorer](data-classification-activity-explorer.md) to access and filter all the data for your Endpoint devices.</span></span>

![filtre de l’Explorateur d’activités pour les appareils de point de terminaison](../media/endpoint-dlp-4-getting-started-activity-explorer.png)

## <a name="next-steps"></a><span data-ttu-id="dc976-200">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="dc976-200">Next steps</span></span>
<span data-ttu-id="dc976-201">Maintenant que vous disposez d’appareils intégrés et que vous pouvez afficher les données d’activité dans l’Explorateur d’activités, vous êtes prêt à passer à l’étape suivante dans laquelle vous créez des stratégies DLP qui protègent vos éléments sensibles.</span><span class="sxs-lookup"><span data-stu-id="dc976-201">Now that you have onboarded devices and can view the activity data in Activity explorer, you are ready to move on to your next step where you create DLP policies that protect your sensitive items.</span></span>

- [<span data-ttu-id="dc976-202">Utilisation des points de terminaison de protection contre la perte de données (aperçu)</span><span class="sxs-lookup"><span data-stu-id="dc976-202">Using Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-using.md)

## <a name="see-also"></a><span data-ttu-id="dc976-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc976-203">See also</span></span>

- [<span data-ttu-id="dc976-204">En savoir plus sur les points de terminaison de protection contre la perte de données (Preview)</span><span class="sxs-lookup"><span data-stu-id="dc976-204">Learn about Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-learn-about.md)
- [<span data-ttu-id="dc976-205">Utilisation des points de terminaison de protection contre la perte de données (aperçu)</span><span class="sxs-lookup"><span data-stu-id="dc976-205">Using Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-using.md)
- [<span data-ttu-id="dc976-206">Vue d’ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="dc976-206">Overview of data loss prevention</span></span>](data-loss-prevention-policies.md)
- [<span data-ttu-id="dc976-207">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="dc976-207">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="dc976-208">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="dc976-208">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="dc976-209">Microsoft Defender – Protection avancée contre les menaces (Microsoft Defender ATP)</span><span class="sxs-lookup"><span data-stu-id="dc976-209">Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP)</span></span>](https://docs.microsoft.com/windows/security/threat-protection/)
- <span data-ttu-id="dc976-210">[Outils et méthodes d’intégration pour les appareils Windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="dc976-210">[Onboarding tools and methods for Windows 10 machines](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints)</span></span>
- [<span data-ttu-id="dc976-211">Abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="dc976-211">Microsoft 365 subscription</span></span>](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1)
- [<span data-ttu-id="dc976-212">Azure Active Directory (ADD) adhésion</span><span class="sxs-lookup"><span data-stu-id="dc976-212">Azure Active Directory (AAD) joined</span></span>](https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join)
- [<span data-ttu-id="dc976-213">Télécharger le nouveau Microsoft Edge sur la base de chrome</span><span class="sxs-lookup"><span data-stu-id="dc976-213">Download the new Microsoft Edge based on Chromium</span></span>](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium)
