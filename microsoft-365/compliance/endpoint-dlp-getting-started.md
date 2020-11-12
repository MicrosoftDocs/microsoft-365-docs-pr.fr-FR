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
ms.openlocfilehash: 8f4b1b04aadbb639f6c7daeeb564c10abd7737b2
ms.sourcegitcommit: ca733da1ed919b286a93068b560608e82f8def05
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48990549"
---
# <a name="get-started-with-endpoint-data-loss-prevention"></a><span data-ttu-id="9aead-103">Prise en main de la protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9aead-103">Get started with Endpoint data loss prevention</span></span>

<span data-ttu-id="9aead-104">La protection contre la perte de données de point de terminaison (Endpoint DLP) Microsoft fait partie de la suite de fonctionnalités de protection contre la perte de données (DLP) Microsoft 365 que vous pouvez utiliser pour découvrir et protéger les éléments sensibles dans les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9aead-104">Microsoft Endpoint data loss prevention (Endpoint DLP) is part of the Microsoft 365 data loss prevention (DLP) suite of features you can use to discover and protect sensitive items across Microsoft 365 services.</span></span> <span data-ttu-id="9aead-105">Pour plus d’informations sur les offres DLP de Microsoft, voir [Vue d’ensemble de la protection contre la perte de données](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="9aead-105">For more information about all of Microsoft’s DLP offerings, see [Overview of data loss prevention](data-loss-prevention-policies.md).</span></span> <span data-ttu-id="9aead-106">Pour en savoir plus sur Endpoint DLP, voir [En savoir plus sur Points de terminaison Protection contre la perte de données (Preview)](endpoint-dlp-learn-about.md)</span><span class="sxs-lookup"><span data-stu-id="9aead-106">To learn more about Endpoint DLP, see [Learn about Endpoint data loss prevention (preview)](endpoint-dlp-learn-about.md)</span></span>

<span data-ttu-id="9aead-107">Microsoft Endpoint DLP vous permet de surveiller les appareils Windows 10 et de détecter les situations d’utilisation et de partage des éléments sensibles.</span><span class="sxs-lookup"><span data-stu-id="9aead-107">Microsoft Endpoint DLP allows you to monitor Windows 10 devices and detect when sensitive items are used and shared.</span></span> <span data-ttu-id="9aead-108">Ainsi, vous bénéficiez de la visibilité et du contrôle dont vous avez besoin pour vous assurer qu’ils sont utilisés et protégés correctement, et pour éviter tout comportement risqué susceptible de les compromettre.</span><span class="sxs-lookup"><span data-stu-id="9aead-108">This gives you the visibility and control you need to ensure that they are used and protected properly, and to help prevent risky behavior that might compromise them.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="9aead-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="9aead-109">Before you begin</span></span>

### <a name="skusubscriptions-licensing"></a><span data-ttu-id="9aead-110">Licences SKU/abonnements</span><span class="sxs-lookup"><span data-stu-id="9aead-110">SKU/subscriptions licensing</span></span>

<span data-ttu-id="9aead-111">Avant de commencer à utiliser point de terminaison DLP, vous devez confirmer votre [abonnement Microsoft 365](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) et tous les modules complémentaires.</span><span class="sxs-lookup"><span data-stu-id="9aead-111">Before you get started with Endpoint DLP, you should confirm your [Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) and any add-ons.</span></span> <span data-ttu-id="9aead-112">Pour accéder à la fonctionnalité de points de terminaison DLP et l’utiliser, vous devez disposer de l’un de ces abonnements ou modules complémentaires.</span><span class="sxs-lookup"><span data-stu-id="9aead-112">To access and use Endpoint DLP functionality, you must have one of these subscriptions or add-ons.</span></span>

- <span data-ttu-id="9aead-113">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="9aead-113">Microsoft 365 E5</span></span>
- <span data-ttu-id="9aead-114">Microsoft 365 A5 (EDU)</span><span class="sxs-lookup"><span data-stu-id="9aead-114">Microsoft 365 A5 (EDU)</span></span>
- <span data-ttu-id="9aead-115">Microsoft 365 E5 Conformité</span><span class="sxs-lookup"><span data-stu-id="9aead-115">Microsoft 365 E5 compliance</span></span>
- <span data-ttu-id="9aead-116">Microsoft 365 A5 Conformité</span><span class="sxs-lookup"><span data-stu-id="9aead-116">Microsoft 365 A5 compliance</span></span>
- <span data-ttu-id="9aead-117">Microsoft 365 E5, Protection des informations et gouvernance</span><span class="sxs-lookup"><span data-stu-id="9aead-117">Microsoft 365 E5 information protection and governance</span></span>
- <span data-ttu-id="9aead-118">Microsoft 365 A5, Protection des informations et gouvernance</span><span class="sxs-lookup"><span data-stu-id="9aead-118">Microsoft 365 A5 information protection and governance</span></span>


### <a name="permissions"></a><span data-ttu-id="9aead-119">Autorisations</span><span class="sxs-lookup"><span data-stu-id="9aead-119">Permissions</span></span>

<span data-ttu-id="9aead-120">Pour activer la gestion des appareils, le compte que vous utilisez doit être membre de l’un de ces rôles :</span><span class="sxs-lookup"><span data-stu-id="9aead-120">To enable device management, the account you use must be a member of any one of these roles:</span></span>

- <span data-ttu-id="9aead-121">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="9aead-121">Global admin</span></span>
- <span data-ttu-id="9aead-122">Administrateur de la sécurité</span><span class="sxs-lookup"><span data-stu-id="9aead-122">Security admin</span></span>
- <span data-ttu-id="9aead-123">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="9aead-123">Compliance admin</span></span>

<span data-ttu-id="9aead-124">Si vous voulez utiliser un compte personnalisé pour afficher les paramètres de gestion des appareils, celui-ci doit se trouver dans l’un de ces rôles :</span><span class="sxs-lookup"><span data-stu-id="9aead-124">If you want to use a custom account to view the device management settings, it must be in one of these roles:</span></span>

- <span data-ttu-id="9aead-125">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="9aead-125">Global admin</span></span>
- <span data-ttu-id="9aead-126">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="9aead-126">Compliance admin</span></span>
- <span data-ttu-id="9aead-127">Administrateur des données de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="9aead-127">Compliance data admin</span></span>
- <span data-ttu-id="9aead-128">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="9aead-128">Global reader</span></span>

<span data-ttu-id="9aead-129">Si vous voulez utiliser un compte personnalisé pour accéder à la page d’intégration/déclassement, celui-ci doit se trouver dans l’un de ces rôles :</span><span class="sxs-lookup"><span data-stu-id="9aead-129">If you want to use a custom account to access the onboarding/offboarding page, it must be in one of these roles:</span></span>

- <span data-ttu-id="9aead-130">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="9aead-130">Global admin</span></span>
- <span data-ttu-id="9aead-131">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="9aead-131">Compliance admin</span></span>

<span data-ttu-id="9aead-132">Si vous voulez utiliser un compte personnalisé pour activer/désactiver la surveillance de l’appareil, celui-ci doit se trouver dans l’un de ces rôles :</span><span class="sxs-lookup"><span data-stu-id="9aead-132">If you want to use a custom account to turn on/off device monitoring, it must be in one of these roles:</span></span>

- <span data-ttu-id="9aead-133">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="9aead-133">Global admin</span></span>
- <span data-ttu-id="9aead-134">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="9aead-134">Compliance admin</span></span>

<span data-ttu-id="9aead-135">Les données du point de terminaison DLP peuvent être affichées dans [l’Explorateur d’activités](data-classification-activity-explorer.md).</span><span class="sxs-lookup"><span data-stu-id="9aead-135">Data from Endpoint DLP can be viewed in [Activity explorer](data-classification-activity-explorer.md).</span></span> <span data-ttu-id="9aead-136">Il existe quatre rôles qui accordent l’autorisation à l’Explorateur d’activités, le compte que vous utilisez pour accéder aux données doit être membre de l’un d’eux.</span><span class="sxs-lookup"><span data-stu-id="9aead-136">There are four roles that grant permission to activity explorer, the account you use for accessing the data must be a member of any one of them.</span></span>

- <span data-ttu-id="9aead-137">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="9aead-137">Global admin</span></span>
- <span data-ttu-id="9aead-138">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="9aead-138">Compliance admin</span></span>
- <span data-ttu-id="9aead-139">Administrateur de la sécurité</span><span class="sxs-lookup"><span data-stu-id="9aead-139">Security admin</span></span>
- <span data-ttu-id="9aead-140">Administrateur des données de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="9aead-140">Compliance data admin</span></span>

### <a name="prepare-your-endpoints"></a><span data-ttu-id="9aead-141">Préparer vos points de terminaison</span><span class="sxs-lookup"><span data-stu-id="9aead-141">Prepare your endpoints</span></span>

<span data-ttu-id="9aead-142">Assurez-vous que les appareils Windows 10 pour lesquels vous envisagez de déployer le point de terminaison DLP répondent à ces exigences.</span><span class="sxs-lookup"><span data-stu-id="9aead-142">Make sure that the Windows 10 devices that you plan on deploying Endpoint DLP to meet these requirements.</span></span>

1. <span data-ttu-id="9aead-143">Vous devez exécuter Windows 10 x64 Build 1809 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9aead-143">Must be running Windows 10 x64 build 1809 or later.</span></span>

2. <span data-ttu-id="9aead-144">La version du client anti-programme malveillant est 4.18.2009.7 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9aead-144">Antimalware Client Version is 4.18.2009.7 or newer.</span></span> <span data-ttu-id="9aead-145">Vérifiez votre version actuelle à l’aide de l’application Sécurité Windows, sélectionnez l’icône Paramètres, puis À propos de.</span><span class="sxs-lookup"><span data-stu-id="9aead-145">Check your current version by opening Windows Security app, select the Settings icon, and then select About.</span></span> <span data-ttu-id="9aead-146">Le numéro de version est répertorié sous version du client anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="9aead-146">The version number is listed under Antimalware Client Version.</span></span> <span data-ttu-id="9aead-147">Effectuez une mise à jour vers la dernière version du client anti-programme malveillant en installant Windows Update KB4052623.</span><span class="sxs-lookup"><span data-stu-id="9aead-147">Update to the latest Antimalware Client Version by installing Windows Update KB4052623.</span></span> <span data-ttu-id="9aead-148">Remarque : aucune des composants de sécurité Windows ne doit être actif, vous pouvez exécuter la protection contre la perte de données de point de terminaison indépendamment de l’état de Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="9aead-148">Note: None of Windows Security components need to be active, you can run Endpoint DLP independent of Windows Security status.</span></span>

3. <span data-ttu-id="9aead-149">Les mises à jour Windows suivantes sont installées.</span><span class="sxs-lookup"><span data-stu-id="9aead-149">The following Windows Updates are installed.</span></span> <span data-ttu-id="9aead-150">Remarque : ces mises à jour ne sont pas des conditions préalables à l’intégration d’un appareil au DLP de point de terminaison , mais contiennent des correctifs pour les problèmes importants qui doivent donc être installés avant d’utiliser le produit.</span><span class="sxs-lookup"><span data-stu-id="9aead-150">Note: These updates are not a pre-requisite to onboard a device to Endpoint DLP, but contain fixes for important issues thus must be installed before using the product.</span></span>

    - <span data-ttu-id="9aead-151">Pour Windows 10 version 1809 : KB4559003, KB4577069, KB4580390</span><span class="sxs-lookup"><span data-stu-id="9aead-151">For Windows 10 1809 - KB4559003, KB4577069, KB4580390</span></span>
    - <span data-ttu-id="9aead-152">Pour Windows 10 version 1903 ou 1909 : KB4559004, KB4577062, KB4580386</span><span class="sxs-lookup"><span data-stu-id="9aead-152">For Windows 10 1903 or 1909 - KB4559004, KB4577062, KB4580386</span></span>
    - <span data-ttu-id="9aead-153">Pour Windows 10 version 2004 : KB4568831, KB4577063</span><span class="sxs-lookup"><span data-stu-id="9aead-153">For Windows 10 2004 - KB4568831, KB4577063</span></span>
    - <span data-ttu-id="9aead-154">Pour les appareils exécutant Office 2016 (et non aucune autre version d’Office) : KB4577063</span><span class="sxs-lookup"><span data-stu-id="9aead-154">For devices running Office 2016 (and not any other Office version) - KB4577063</span></span> 

4. <span data-ttu-id="9aead-155">Tous les appareils doivent être [joints à Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join) ou jointure hybride Azure AD.</span><span class="sxs-lookup"><span data-stu-id="9aead-155">All devices must be [Azure Active Directory (Azure AD) joined](https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join), or Hybrid Azure AD joined.</span></span>

5. <span data-ttu-id="9aead-156">Installez le navigateur Microsoft Chromium Edge sur l’appareil de point de terminaison afin d’appliquer des actions de stratégie pour l’activité de téléchargement vers le Cloud.</span><span class="sxs-lookup"><span data-stu-id="9aead-156">Install Microsoft Chromium Edge browser on the endpoint device to enforce policy actions for the upload to cloud activity.</span></span> <span data-ttu-id="9aead-157">Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Télécharger le nouveau Microsoft Edge basé sur Chromium](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium).</span><span class="sxs-lookup"><span data-stu-id="9aead-157">See, [Download the new Microsoft Edge based on Chromium](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium).</span></span>

6. <span data-ttu-id="9aead-158">Si vous utilisez le Canal Entreprise mensuel de Microsoft 365 Apps versions 2004-2008, un problème connu concerne la protection contre la perte de données de point de terminaison qui classe le contenu Office. Vous devez effectuer une mise à jour vers la version 2009 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9aead-158">If you are on Monthly Enterprise Channel of Microsoft 365 Apps versions 2004-2008, there is a known issue with Endpoint DLP classifying Office content and you need to update to version 2009 or later.</span></span> <span data-ttu-id="9aead-159">Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Historique des mises à jour de Microsoft 365 Apps (répertoriées par date)](https://docs.microsoft.com/officeupdates/update-history-microsoft365-apps-by-date).</span><span class="sxs-lookup"><span data-stu-id="9aead-159">See [Update history for Microsoft 365 Apps (listed by date)](https://docs.microsoft.com/officeupdates/update-history-microsoft365-apps-by-date) for current versions.</span></span> <span data-ttu-id="9aead-160">Si vous souhaitez en savoir plus sur ce problème, veuillez consultez la section Suite Office, dans les [Notes de publication pour les publications du Canal actuel dans 2020](https://docs.microsoft.com/officeupdates/current-channel#version-2010-october-27).</span><span class="sxs-lookup"><span data-stu-id="9aead-160">To learn more about this issue, see the Office Suite section of [Release notes for Current Channel releases in 2020](https://docs.microsoft.com/officeupdates/current-channel#version-2010-october-27).</span></span>

## <a name="onboarding-devices-into-device-management"></a><span data-ttu-id="9aead-161">Intégration d’appareils dans la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="9aead-161">Onboarding devices into device management</span></span>

<span data-ttu-id="9aead-162">Vous devez activer la surveillance des appareils et intégrer vos points de terminaison avant de pouvoir surveiller et protéger les éléments sensibles sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="9aead-162">You must enable device monitoring and onboard your endpoints before you can monitor and protect sensitive items on a device.</span></span> <span data-ttu-id="9aead-163">Ces deux actions sont effectuées dans le portail de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9aead-163">Both of these actions are done in the Microsoft 365 Compliance portal.</span></span>

<span data-ttu-id="9aead-164">Lorsque vous voulez intégrer des appareils qui n’ont pas encore été intégrés, vous devez télécharger et déployer les scripts appropriés sur ces appareils.</span><span class="sxs-lookup"><span data-stu-id="9aead-164">When you want to onboard devices that haven't been onboarded yet, you'll download the appropriate script and deploy it to those devices.</span></span> <span data-ttu-id="9aead-165">Suivez la procédure [d’intégration d’appareils](endpoint-dlp-getting-started.md#onboarding-devices).</span><span class="sxs-lookup"><span data-stu-id="9aead-165">Follow the [Onboarding devices procedure](endpoint-dlp-getting-started.md#onboarding-devices).</span></span>

<span data-ttu-id="9aead-166">Si vous disposez déjà d’appareils incorporés dans [Microsoft Defender pour point de terminaison](https://docs.microsoft.com/windows/security/threat-protection/), ceux-ci apparaissent déjà dans la liste des périphériques gérés.</span><span class="sxs-lookup"><span data-stu-id="9aead-166">If you already have devices onboarded into [Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection/), they will already appear in the managed devices list.</span></span> <span data-ttu-id="9aead-167">Suivez la procédure [Appareils intégrés à Microsoft Defender pour point de terminaison](endpoint-dlp-getting-started.md#with-devices-onboarded-into-microsoft-defender-for- endpoint).</span><span class="sxs-lookup"><span data-stu-id="9aead-167">Follow the [With devices onboarded into Microsoft Defender for Endpoint procedure](endpoint-dlp-getting-started.md#with-devices-onboarded-into-microsoft-defender-for- endpoint).</span></span>

### <a name="onboarding-devices"></a><span data-ttu-id="9aead-168">Intégration des appareils</span><span class="sxs-lookup"><span data-stu-id="9aead-168">Onboarding devices</span></span>

<span data-ttu-id="9aead-169">Dans ce scénario de déploiement, vous allez intégrer des appareils qui n’ont pas encore été intégrés, et vous voulez simplement contrôler et protéger les éléments sensibles contre le partage involontaire sur les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="9aead-169">In this deployment scenario, you'll onboard devices that have not been onboarded yet, and you just want to monitor and protect sensitive items from unintentional sharing on Windows 10 devices.</span></span>

1. <span data-ttu-id="9aead-170">Ouvrez le [Centre de conformité Microsoft](https://compliance.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="9aead-170">Open the [Microsoft compliance center](https://compliance.microsoft.com).</span></span>

2. <span data-ttu-id="9aead-171">Ouvrez la page Paramètres du centre de conformité et sélectionnez **Appareils intégrés**.</span><span class="sxs-lookup"><span data-stu-id="9aead-171">Open the Compliance Center settings page and choose **Onboard devices**.</span></span> 

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="9aead-172">![activer la gestion des appareils](../media/endpoint-dlp-learn-about-1-enable-device-management.png)</span><span class="sxs-lookup"><span data-stu-id="9aead-172">![enable device management](../media/endpoint-dlp-learn-about-1-enable-device-management.png)</span></span>

   > [!NOTE]
   > <span data-ttu-id="9aead-173">Bien que l’activation de l’intégration des appareils dure généralement environ 60 secondes, patientez jusqu’à 30 minutes avant de contacter le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9aead-173">While it usually takes about 60 seconds for device onboarding to be enabled, please allow up to 30 minutes before engaging with Microsoft support.</span></span>

3. <span data-ttu-id="9aead-174">Sélectionnez **Gestion des appareils** pour ouvrir la liste des **Appareils**.</span><span class="sxs-lookup"><span data-stu-id="9aead-174">Choose **Device management** to open the **Devices** list.</span></span> <span data-ttu-id="9aead-175">La liste est vide tant que vous n’avez pas intégré de périphériques.</span><span class="sxs-lookup"><span data-stu-id="9aead-175">The list will be empty until you onboard devices.</span></span>

4. <span data-ttu-id="9aead-176">Sélectionnez **Intégration** pour lancer le processus d’intégration.</span><span class="sxs-lookup"><span data-stu-id="9aead-176">Choose **Onboarding** to begin the onboarding process.</span></span>

5. <span data-ttu-id="9aead-177">Choisissez la manière dont vous voulez déployer ces autres appareils à partir de la liste **Méthode de déploiement** , puis **Télécharger le package**.</span><span class="sxs-lookup"><span data-stu-id="9aead-177">Choose the way you want to deploy to these additional devices from the **Deployment method** list and then **download package**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="9aead-178">![méthode de déploiement](../media/endpoint-dlp-getting-started-3-deployment-method.png)</span><span class="sxs-lookup"><span data-stu-id="9aead-178">![deployment method](../media/endpoint-dlp-getting-started-3-deployment-method.png)</span></span>
   
6. <span data-ttu-id="9aead-179">Suivez les procédures appropriées dans [Outils et méthodes d’intégration pour les ordinateurs Windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="9aead-179">Follow the appropriate procedures in [Onboarding tools and methods for Windows 10 machines](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span></span> <span data-ttu-id="9aead-180">Ce lien vous dirige vers une page d’accueil dans laquelle vous pouvez accéder aux procédures Microsoft Defender pour point de terminaison qui correspondent au package de déploiement que vous avez sélectionné à l’étape 5 :</span><span class="sxs-lookup"><span data-stu-id="9aead-180">This link take you to a landing page where you can access Microsoft Defender for Endpoint procedures that match the deployment package you selected in step 5:</span></span>

    - <span data-ttu-id="9aead-181">Intégrer les ordinateurs Windows 10 utilisant une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="9aead-181">Onboard Windows 10 machines using Group Policy</span></span>
    - <span data-ttu-id="9aead-182">Intégrer les ordinateurs Windows à l’aide du gestionnaire de configuration de point de terminaison Microsoft</span><span class="sxs-lookup"><span data-stu-id="9aead-182">Onboard Windows machines using Microsoft Endpoint Configuration Manager</span></span>
    - <span data-ttu-id="9aead-183">Intégrer les ordinateurs Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="9aead-183">Onboard Windows 10 machines using Mobile Device Management tools</span></span>
    - <span data-ttu-id="9aead-184">Intégrer les ordinateurs Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="9aead-184">Onboard Windows 10 machines using a local script</span></span>
    - <span data-ttu-id="9aead-185">Intégrer les ordinateurs virtuels d’infrastructure de bureau virtuel (VDI) non persistants.</span><span class="sxs-lookup"><span data-stu-id="9aead-185">Onboard non-persistent virtual desktop infrastructure (VDI) machines.</span></span>

<span data-ttu-id="9aead-186">Une fois l’opération effectuée et le point de terminaison intégré, celui-ci doit être visible dans la liste des appareils et commencer à créer des rapports d’activité d’audit dans l’Explorateur d’activités.</span><span class="sxs-lookup"><span data-stu-id="9aead-186">Once done and endpoint is onboarded, it should be visible in the devices list and also start reporting audit activity logs to Activity explorer.</span></span>

> [!NOTE]
> <span data-ttu-id="9aead-187">Cette expérience est sous l’application de la licence.</span><span class="sxs-lookup"><span data-stu-id="9aead-187">This experience is under license enforcement.</span></span> <span data-ttu-id="9aead-188">Sans la licence requise, les données ne sont pas visibles ni accessibles.</span><span class="sxs-lookup"><span data-stu-id="9aead-188">Without the required license, data will not be visible or accessible.</span></span>

### <a name="with-devices-onboarded-into-microsoft-defender-for-endpoint"></a><span data-ttu-id="9aead-189">Appareils intégrés à Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9aead-189">With devices onboarded into Microsoft Defender for Endpoint</span></span>

<span data-ttu-id="9aead-190">Dans ce scénario, Microsoft Defender pour point de terminaison est déjà déployé et des points de terminaison y sont signalés.</span><span class="sxs-lookup"><span data-stu-id="9aead-190">In this scenario, Microsoft Defender for Endpoint is already deployed and there are endpoints reporting in.</span></span> <span data-ttu-id="9aead-191">Tous ces points de terminaison s’affichent dans la liste des appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="9aead-191">All these endpoints will appear in the managed devices list.</span></span> <span data-ttu-id="9aead-192">Vous pouvez continuer à intégrer de nouveaux appareils dans le point de terminaison DLP pour étendre la couverture à l’aide de la [procédure d’intégration d’appareils](endpoint-dlp-getting-started.md#onboarding-devices).</span><span class="sxs-lookup"><span data-stu-id="9aead-192">You can continue to onboard new devices into Endpoint DLP to expand coverage by using the [Onboarding devices procedure](endpoint-dlp-getting-started.md#onboarding-devices).</span></span>

1. <span data-ttu-id="9aead-193">Ouvrez le [Centre de conformité Microsoft](https://compliance.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="9aead-193">Open the [Microsoft compliance center](https://compliance.microsoft.com).</span></span>

2. <span data-ttu-id="9aead-194">Ouvrez la page Paramètres du centre de conformité et sélectionnez **Activer la surveillance d’appareils**.</span><span class="sxs-lookup"><span data-stu-id="9aead-194">Open the Compliance Center settings page and choose **Enable device monitoring**.</span></span>

3. <span data-ttu-id="9aead-195">Sélectionnez **Gestion des appareils** pour ouvrir la liste des **Appareils**.</span><span class="sxs-lookup"><span data-stu-id="9aead-195">Choose **Device management** to open the **Devices** list.</span></span> <span data-ttu-id="9aead-196">Vous devriez voir apparaître la liste des appareils qui signalent déjà à Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="9aead-196">You should see the list of devices that are already reporting in to Microsoft Defender for Endpoint.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="9aead-197">![Gestion des appareils](../media/endpoint-dlp-getting-started-2-device-management.png)</span><span class="sxs-lookup"><span data-stu-id="9aead-197">![device management](../media/endpoint-dlp-getting-started-2-device-management.png)</span></span>
   
4. <span data-ttu-id="9aead-198">Sélectionnez **Intégration** si vous avez besoin d’intégrer d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="9aead-198">Choose **Onboarding** if you need to onboard additional devices.</span></span>

5. <span data-ttu-id="9aead-199">Choisissez la manière dont vous voulez déployer ces autres appareils à partir de la liste **Méthode de déploiement** , puis **Télécharger le package**.</span><span class="sxs-lookup"><span data-stu-id="9aead-199">Choose the way you want to deploy to these additional devices from the **Deployment method** list and then **Download package**.</span></span>

6. <span data-ttu-id="9aead-200">Suivez les procédures appropriées dans [Outils et méthodes d’intégration pour les ordinateurs Windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="9aead-200">Follow the appropriate procedures in [Onboarding tools and methods for Windows 10 machines](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span></span> <span data-ttu-id="9aead-201">Ce lien vous dirige vers une page d’accueil dans laquelle vous pouvez accéder aux procédures Microsoft Defender pour point de terminaison qui correspondent au package de déploiement que vous avez sélectionné à l’étape 5 :</span><span class="sxs-lookup"><span data-stu-id="9aead-201">This link take you to a landing page where you can access Microsoft Defender for Endpoint procedures that match the deployment package you selected in step 5:</span></span>

    - <span data-ttu-id="9aead-202">Intégrer les ordinateurs Windows 10 utilisant une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="9aead-202">Onboard Windows 10 machines using Group Policy</span></span>
    - <span data-ttu-id="9aead-203">Intégrer les ordinateurs Windows à l’aide du gestionnaire de configuration de point de terminaison Microsoft</span><span class="sxs-lookup"><span data-stu-id="9aead-203">Onboard Windows machines using Microsoft Endpoint Configuration Manager</span></span>
    - <span data-ttu-id="9aead-204">Intégrer les ordinateurs Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="9aead-204">Onboard Windows 10 machines using Mobile Device Management tools</span></span>
    - <span data-ttu-id="9aead-205">Intégrer les ordinateurs Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="9aead-205">Onboard Windows 10 machines using a local script</span></span>
    - <span data-ttu-id="9aead-206">Intégrer les ordinateurs virtuels d’infrastructure de bureau virtuel (VDI) non persistants.</span><span class="sxs-lookup"><span data-stu-id="9aead-206">Onboard non-persistent virtual desktop infrastructure (VDI) machines.</span></span>

<span data-ttu-id="9aead-207">Une fois l’opération effectuée et le point de terminaison intégré, celui-ci doit être visible dans le tableau des **Appareils** et commencer à créer des rapports d’activité d’audit dans l’ **Explorateur d’activités**.</span><span class="sxs-lookup"><span data-stu-id="9aead-207">Once done and endpoint is onboarded, it should be visible under the **Devices** table and also start reporting audit logs to the **Activity Explorer**.</span></span>

> [!NOTE]
><span data-ttu-id="9aead-208">Cette expérience est sous l’application de la licence.</span><span class="sxs-lookup"><span data-stu-id="9aead-208">This experience is under license enforcement.</span></span> <span data-ttu-id="9aead-209">Sans la licence requise, les données ne sont pas visibles ni accessibles.</span><span class="sxs-lookup"><span data-stu-id="9aead-209">Without the required license, data will not be visible or accessible.</span></span>

### <a name="viewing-endpoint-dlp-data-in-activity-explorer"></a><span data-ttu-id="9aead-210">Affichage de données DLP de point de terminaison dans l’Explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="9aead-210">Viewing Endpoint DLP data in activity explorer</span></span>

1. <span data-ttu-id="9aead-211">Ouvrez la [Page classification des données](https://compliance.microsoft.com/dataclassification?viewid=overview) pour votre domaine dans le centre de conformité Microsoft 365, puis sélectionnez Explorateur d’activités.</span><span class="sxs-lookup"><span data-stu-id="9aead-211">Open the [Data classification page](https://compliance.microsoft.com/dataclassification?viewid=overview) for your domain in the Microsoft 365 Compliance center and choose Activity explorer.</span></span>

2. <span data-ttu-id="9aead-212">Reportez-vous aux procédures décrites dans [Prise en main de l’Explorateur d’activités](data-classification-activity-explorer.md) pour accéder aux données de vos appareils de point de terminaison et les filtrer.</span><span class="sxs-lookup"><span data-stu-id="9aead-212">Refer to the procedures in [Get started with Activity explorer](data-classification-activity-explorer.md) to access and filter all the data for your Endpoint devices.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="9aead-213">![filtre de l’Explorateur d’activités pour les appareils de point de terminaison](../media/endpoint-dlp-4-getting-started-activity-explorer.png)</span><span class="sxs-lookup"><span data-stu-id="9aead-213">![activity explorer filter for endpoint devices](../media/endpoint-dlp-4-getting-started-activity-explorer.png)</span></span>

## <a name="next-steps"></a><span data-ttu-id="9aead-214">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9aead-214">Next steps</span></span>
<span data-ttu-id="9aead-215">Maintenant que vous disposez d’appareils intégrés et que vous pouvez afficher les données d’activité dans l’Explorateur d’activités, vous êtes prêt à passer à l’étape suivante dans laquelle vous créez des stratégies DLP qui protègent vos éléments sensibles.</span><span class="sxs-lookup"><span data-stu-id="9aead-215">Now that you have onboarded devices and can view the activity data in Activity explorer, you are ready to move on to your next step where you create DLP policies that protect your sensitive items.</span></span>

- [<span data-ttu-id="9aead-216">Utilisation des points de terminaison de protection contre la perte de données (aperçu)</span><span class="sxs-lookup"><span data-stu-id="9aead-216">Using Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-using.md)

## <a name="see-also"></a><span data-ttu-id="9aead-217">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9aead-217">See also</span></span>

- [<span data-ttu-id="9aead-218">En savoir plus sur les points de terminaison de protection contre la perte de données (Preview)</span><span class="sxs-lookup"><span data-stu-id="9aead-218">Learn about Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-learn-about.md)
- [<span data-ttu-id="9aead-219">Utilisation des points de terminaison de protection contre la perte de données (aperçu)</span><span class="sxs-lookup"><span data-stu-id="9aead-219">Using Endpoint data loss prevention (preview)</span></span>](endpoint-dlp-using.md)
- [<span data-ttu-id="9aead-220">Vue d’ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="9aead-220">Overview of data loss prevention</span></span>](data-loss-prevention-policies.md)
- [<span data-ttu-id="9aead-221">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="9aead-221">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="9aead-222">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="9aead-222">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="9aead-223">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9aead-223">Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection/)
- <span data-ttu-id="9aead-224">[Outils et méthodes d’intégration pour les appareils Windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="9aead-224">[Onboarding tools and methods for Windows 10 machines](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints)</span></span>
- [<span data-ttu-id="9aead-225">Abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9aead-225">Microsoft 365 subscription</span></span>](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1)
- [<span data-ttu-id="9aead-226">Azure AD appareils joints</span><span class="sxs-lookup"><span data-stu-id="9aead-226">Azure AD joined devices</span></span>](https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join)
- [<span data-ttu-id="9aead-227">Télécharger le nouveau Microsoft Edge sur la base de chrome</span><span class="sxs-lookup"><span data-stu-id="9aead-227">Download the new Microsoft Edge based on Chromium</span></span>](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium)
