---
title: Prise en main de l’extension de la conformité Microsoft
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
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
description: Préparez, puis déployez l’extension de la conformité Microsoft.
ms.openlocfilehash: a76a4b1ab5b92a1e237663f65002b99d792b13bb
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53288370"
---
# <a name="get-started-with-microsoft-compliance-extension"></a><span data-ttu-id="73a33-103">Prise en main de l’extension de la conformité Microsoft</span><span class="sxs-lookup"><span data-stu-id="73a33-103">Get started with Microsoft Compliance Extension</span></span>

<span data-ttu-id="73a33-104">Utilisez les procédures ci-après pour déployer l’extension de la conformité Microsoft.</span><span class="sxs-lookup"><span data-stu-id="73a33-104">Use these procedures to roll out the Microsoft Compliance Extension.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="73a33-105">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="73a33-105">Before you begin</span></span>

<span data-ttu-id="73a33-106">Pour utiliser l’extension de la conformité Microsoft, l’appareil doit être intégré à la protection contre la perte de données du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="73a33-106">To use Microsoft Compliance Extension, the device must be onboarded into endpoint DLP.</span></span> <span data-ttu-id="73a33-107">Consultez ces articles si vous êtes novice en matière de DLP ou de DLP des points d'extrémité.</span><span class="sxs-lookup"><span data-stu-id="73a33-107">Review these articles if you are new to DLP or endpoint DLP</span></span>

- [<span data-ttu-id="73a33-108">En savoir plus sur l’extension de la conformité Microsoft</span><span class="sxs-lookup"><span data-stu-id="73a33-108">Learn about Microsoft Compliance Extension</span></span>](dlp-chrome-learn-about.md)
- [<span data-ttu-id="73a33-109">En savoir plus sur la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="73a33-109">Learn about data loss prevention</span></span>](dlp-learn-about-dlp.md)
- [<span data-ttu-id="73a33-110">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="73a33-110">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="73a33-111">Création d’une stratégie DLP à partir d’un modèle</span><span class="sxs-lookup"><span data-stu-id="73a33-111">Create a DLP policy from a template</span></span>](create-a-dlp-policy-from-a-template.md)
- [<span data-ttu-id="73a33-112">Découvrir la protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="73a33-112">Learn about endpoint data loss prevention</span></span>](endpoint-dlp-learn-about.md)
- [<span data-ttu-id="73a33-113">Prise en main de la protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="73a33-113">Get started with Endpoint data loss prevention</span></span>](endpoint-dlp-getting-started.md)
- [<span data-ttu-id="73a33-114">Outils et méthodes d’intégration pour les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="73a33-114">Onboarding tools and methods for Windows 10 devices</span></span>](dlp-configure-endpoints.md)
- [<span data-ttu-id="73a33-115">Configurer le proxy du dispositif et les paramètres de connexion à Internet pour le DLP du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="73a33-115">Configure device proxy and internet connection settings for Endpoint DLP</span></span>](endpoint-dlp-configure-proxy.md)
- [<span data-ttu-id="73a33-116">Utilisation des points de terminaison protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="73a33-116">Using Endpoint data loss prevention</span></span>](endpoint-dlp-using.md)

### <a name="skusubscriptions-licensing"></a><span data-ttu-id="73a33-117">Licences SKU / abonnements</span><span class="sxs-lookup"><span data-stu-id="73a33-117">SKU/subscriptions licensing</span></span>

<span data-ttu-id="73a33-118">Avant de commencer, vous devez confirmer votre [abonnement Microsoft 365](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) et tous les modules complémentaires.</span><span class="sxs-lookup"><span data-stu-id="73a33-118">Before you get started, you should confirm your [Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) and any add-ons.</span></span> <span data-ttu-id="73a33-119">Pour accéder à la fonctionnalité de points de terminaison DLP et l’utiliser, vous devez disposer de l’un de ces abonnements ou modules complémentaires.</span><span class="sxs-lookup"><span data-stu-id="73a33-119">To access and use Endpoint DLP functionality, you must have one of these subscriptions or add-ons.</span></span>

- <span data-ttu-id="73a33-120">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="73a33-120">Microsoft 365 E5</span></span>
- <span data-ttu-id="73a33-121">Microsoft 365 A5 (EDU)</span><span class="sxs-lookup"><span data-stu-id="73a33-121">Microsoft 365 A5 (EDU)</span></span>
- <span data-ttu-id="73a33-122">Microsoft 365 E5 Conformité</span><span class="sxs-lookup"><span data-stu-id="73a33-122">Microsoft 365 E5 compliance</span></span>
- <span data-ttu-id="73a33-123">Microsoft 365 A5 Conformité</span><span class="sxs-lookup"><span data-stu-id="73a33-123">Microsoft 365 A5 compliance</span></span>
- <span data-ttu-id="73a33-124">Microsoft 365 E5, Protection des informations et gouvernance</span><span class="sxs-lookup"><span data-stu-id="73a33-124">Microsoft 365 E5 information protection and governance</span></span>
- <span data-ttu-id="73a33-125">Microsoft 365 A5, Protection des informations et gouvernance</span><span class="sxs-lookup"><span data-stu-id="73a33-125">Microsoft 365 A5 information protection and governance</span></span>

<span data-ttu-id="73a33-126">Pour obtenir des instructions détaillées sur les licences, consultez [instructions relatives aux licences Microsoft 365 pour la sécurité et la conformité](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#information-protection).</span><span class="sxs-lookup"><span data-stu-id="73a33-126">For detailed licensing guidance, see [Microsoft 365 licensing guidance for security & compliance](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#information-protection).</span></span>

- <span data-ttu-id="73a33-127">Votre organisation doit avoir une licence pour la DLP de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="73a33-127">Your org must be licensed for Endpoint DLP</span></span>
- <span data-ttu-id="73a33-128">Vos appareils doivent exécuter Windows 10 x64 build 1809 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="73a33-128">Your devices must be running Windows 10 x64 build 1809 or later.</span></span>
- <span data-ttu-id="73a33-129">La version client Antimalware doit être 4.18.2101.9 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="73a33-129">The device must have Antimalware Client Version is 4.18.2101.9 or later.</span></span> <span data-ttu-id="73a33-130">Vérifiez votre version actuelle à l’aide de l’application **Sécurité Windows**, sélectionnez l’icône **Paramètres**, puis **À propos de**.</span><span class="sxs-lookup"><span data-stu-id="73a33-130">Check your current version by opening **Windows Security** app, select the **Settings** icon, and then select **About**.</span></span>


### <a name="permissions"></a><span data-ttu-id="73a33-131">Autorisations</span><span class="sxs-lookup"><span data-stu-id="73a33-131">Permissions</span></span>

<span data-ttu-id="73a33-132">Les données du point de terminaison DLP peuvent être affichées dans [l’Explorateur d’activités](data-classification-activity-explorer.md).</span><span class="sxs-lookup"><span data-stu-id="73a33-132">Data from Endpoint DLP can be viewed in [Activity explorer](data-classification-activity-explorer.md).</span></span> <span data-ttu-id="73a33-133">Il existe sept rôles qui accordent l’autorisation à l’Explorateur d’activités, le compte que vous utilisez pour accéder aux données doit être membre de l’un d’eux.</span><span class="sxs-lookup"><span data-stu-id="73a33-133">There are seven roles that grant permission to activity explorer, the account you use for accessing the data must be a member of any one of them.</span></span>

- <span data-ttu-id="73a33-134">Administrateur global</span><span class="sxs-lookup"><span data-stu-id="73a33-134">Global admin</span></span>
- <span data-ttu-id="73a33-135">Administrateur de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="73a33-135">Compliance admin</span></span>
- <span data-ttu-id="73a33-136">Administrateur de la sécurité</span><span class="sxs-lookup"><span data-stu-id="73a33-136">Security admin</span></span>
- <span data-ttu-id="73a33-137">Administrateur des données de mise en conformité</span><span class="sxs-lookup"><span data-stu-id="73a33-137">Compliance data admin</span></span>
- <span data-ttu-id="73a33-138">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="73a33-138">Global reader</span></span>
- <span data-ttu-id="73a33-139">Lecteur Sécurité</span><span class="sxs-lookup"><span data-stu-id="73a33-139">Security reader</span></span>
- <span data-ttu-id="73a33-140">Lecteur de rapports</span><span class="sxs-lookup"><span data-stu-id="73a33-140">Reports reader</span></span>

### <a name="overall-installation-workflow"></a><span data-ttu-id="73a33-141">Flux de travail d’installation global</span><span class="sxs-lookup"><span data-stu-id="73a33-141">Overall installation workflow</span></span>

<span data-ttu-id="73a33-p105">Le déploiement de l’extension de la conformité Microsoft est un processus en plusieurs phases. Vous pouvez choisir de l'installer sur un ordinateur à la fois, ou d'utiliser Microsoft Endpoint Manager ou stratégie de groupe pour les déploiements à l'échelle de l'organisation.</span><span class="sxs-lookup"><span data-stu-id="73a33-p105">Deploying Microsoft Compliance Extension is a multi-phase process. You can choose to install on one machine at a time, or use Microsoft Endpoint Manager or Group Policy for organization-wide deployments.</span></span>

1. <span data-ttu-id="73a33-144">[Préparez vos appareils](#prepare-your-devices).</span><span class="sxs-lookup"><span data-stu-id="73a33-144">[Prepare your devices](#prepare-your-devices).</span></span>
2. [<span data-ttu-id="73a33-145">Configuration de base ordinateur simple Selfhost</span><span class="sxs-lookup"><span data-stu-id="73a33-145">Basic Setup Single Machine Selfhost</span></span>](#basic-setup-single-machine-selfhost)
3. [<span data-ttu-id="73a33-146">Déployer à l'aide de Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="73a33-146">Deploy using Microsoft Endpoint Manager</span></span>](#deploy-using-microsoft-endpoint-manager)
4. [<span data-ttu-id="73a33-147">Déployer à l’aide d’une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="73a33-147">Deploy using Group Policy</span></span>](#deploy-using-group-policy)
5. [<span data-ttu-id="73a33-148">Tester l’extension</span><span class="sxs-lookup"><span data-stu-id="73a33-148">Test the Extension</span></span>](#test-the-extension)
6. [<span data-ttu-id="73a33-149">Utiliser le tableau de bord de gestion des alertes pour afficher les alertes DLP dans Chrome</span><span class="sxs-lookup"><span data-stu-id="73a33-149">Use the Alerts Management Dashboard to viewing Chrome DLP alerts</span></span>](#use-the-alerts-management-dashboard-to-viewing-chrome-dlp-alerts)
7. [<span data-ttu-id="73a33-150">Affichage de données DLP dans l’Explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="73a33-150">Viewing Chrome DLP data in activity explorer</span></span>](#viewing-chrome-dlp-data-in-activity-explorer)

### <a name="prepare-infrastructure"></a><span data-ttu-id="73a33-151">Préparation de l'infrastructure</span><span class="sxs-lookup"><span data-stu-id="73a33-151">Prepare infrastructure</span></span>

<span data-ttu-id="73a33-152">Si vous déployez l'extension de conformité Microsoft sur tous vos appareils Windows 10 contrôlés, vous devez supprimer Google Chrome des listes des applications et des navigateurs non autorisés.</span><span class="sxs-lookup"><span data-stu-id="73a33-152">If you are rolling out the Microsoft Compliance Extension to all your monitored Windows 10 devices, you should remove Google Chrome from the unallowed app and unallowed browser lists.</span></span> <span data-ttu-id="73a33-153">Pour plus d'informations, voir [Navigateurs non autorisés ](endpoint-dlp-using.md#unallowed-browsers).</span><span class="sxs-lookup"><span data-stu-id="73a33-153">For more information, see [Unallowed browsers](endpoint-dlp-using.md#unallowed-browsers).</span></span> <span data-ttu-id="73a33-154">Si vous ne le déployez que sur quelques appareils, vous pouvez laisser Chrome sur la liste des navigateurs non autorisés ou des applications non autorisées.</span><span class="sxs-lookup"><span data-stu-id="73a33-154">If you are only rolling it out to a few devices, you can leave Chrome on the unallowed browser or unallowed app lists.</span></span> <span data-ttu-id="73a33-155">L'extension de conformité Microsoft contournera les restrictions des deux listes pour les ordinateurs sur lesquels elle est installée.</span><span class="sxs-lookup"><span data-stu-id="73a33-155">The Microsoft Compliance Extension will bypass the restrictions of both lists for those computers where it is installed.</span></span>

### <a name="prepare-your-devices"></a><span data-ttu-id="73a33-156">Préparer vos appareils</span><span class="sxs-lookup"><span data-stu-id="73a33-156">Prepare your devices</span></span>

1. <span data-ttu-id="73a33-157">Utilisez les procédures de ces rubriques pour intégrer vos appareils :</span><span class="sxs-lookup"><span data-stu-id="73a33-157">Use the procedures in these topics to onboard your devices:</span></span>
    1. [<span data-ttu-id="73a33-158">Prise en main de la protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="73a33-158">Get started with Endpoint data loss prevention</span></span>](endpoint-dlp-getting-started.md)
    1. [<span data-ttu-id="73a33-159">Outils et méthodes d’intégration pour les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="73a33-159">Onboarding tools and methods for Windows 10 devices</span></span>](dlp-configure-endpoints.md)
    1. [<span data-ttu-id="73a33-160">Configurer le proxy du dispositif et les paramètres de connexion à Internet pour le DLP du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="73a33-160">Configure device proxy and internet connection settings for Endpoint DLP</span></span>](endpoint-dlp-configure-proxy.md)

### <a name="basic-setup-single-machine-selfhost"></a><span data-ttu-id="73a33-161">Configuration de base ordinateur simple Selfhost</span><span class="sxs-lookup"><span data-stu-id="73a33-161">Basic Setup Single Machine Selfhost</span></span>

<span data-ttu-id="73a33-162">Il s'agit de la méthode recommandée.</span><span class="sxs-lookup"><span data-stu-id="73a33-162">This is the recommended method.</span></span>

1. <span data-ttu-id="73a33-163">Connectez-vous à l'ordinateur Windows 10 sur lequel vous souhaitez installer l'extension de conformité Microsoft, puis exécutez ce script PowerShell en tant qu'administrateur.</span><span class="sxs-lookup"><span data-stu-id="73a33-163">Sign in to the Windows 10 computer on which you want to install the Microsoft Compliance Extension on, and run this PowerShell script as an administrator.</span></span>

   ```powershell
   Get-Item -path "HKLM:\SOFTWARE\Microsoft\Windows Defender\Miscellaneous Configuration" | New-ItemProperty -Name DlpDisableBrowserCache -Value 0 -Force
   ```

2. <span data-ttu-id="73a33-164">Accédez à [Extension de la conformité Microsoft : Chrome Web Store (google.com)](https://chrome.google.com/webstore/detail/microsoft-compliance-exte/echcggldkblhodogklpincgchnpgcdco).</span><span class="sxs-lookup"><span data-stu-id="73a33-164">Navigate to [Microsoft Compliance Extension - Chrome Web Store (google.com)](https://chrome.google.com/webstore/detail/microsoft-compliance-exte/echcggldkblhodogklpincgchnpgcdco).</span></span>

3. <span data-ttu-id="73a33-165">Installez l’extension à l’aide des instructions de la page Chrome Web Store.</span><span class="sxs-lookup"><span data-stu-id="73a33-165">Install the extension using the instructions on the Chrome Web Store page.</span></span>

### <a name="deploy-using-microsoft-endpoint-manager"></a><span data-ttu-id="73a33-166">Déployez à l'aide de Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="73a33-166">Deploy using Microsoft Endpoint Manager</span></span>

<span data-ttu-id="73a33-167">Utilisez cette méthode de configuration pour les déploiements à l'échelle de l'entreprise.</span><span class="sxs-lookup"><span data-stu-id="73a33-167">Use this setup method for organization-wide deployments.</span></span>

##### <a name="enabling-required-registry-key-via-microsoft-endpoint-manager"></a><span data-ttu-id="73a33-168">Activation de la clé de Registre requise via Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="73a33-168">Enabling Required Registry Key via Microsoft Endpoint Manager</span></span>

1. <span data-ttu-id="73a33-169">Créez un script PowerShell avec le contenu suivant :</span><span class="sxs-lookup"><span data-stu-id="73a33-169">Create a PowerShell script with the following contents:</span></span>

    ```powershell
    Get-Item -path "HKLM:\SOFTWARE\Microsoft\Windows Defender\Miscellaneous Configuration" | New-ItemProperty -Name DlpDisableBrowserCache -Value 0 -Force
    ```

2. <span data-ttu-id="73a33-170">Connectez-vous au [Centre d’administration Microsoft Endpoint Manager](https://endpoint.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="73a33-170">Sign in to the [Microsoft Endpoint Manager Admin Center](https://endpoint.microsoft.com).</span></span>

3. <span data-ttu-id="73a33-171">Accédez à **Appareils** > **Scripts** puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="73a33-171">Navigate to **Devices** > **Scripts** and select **Add**.</span></span>

4. <span data-ttu-id="73a33-172">Accédez à l’emplacement du script créé lorsque vous y avez été invité.</span><span class="sxs-lookup"><span data-stu-id="73a33-172">Browse to the location of the script created when prompted.</span></span>

5. <span data-ttu-id="73a33-173">Sélectionnez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="73a33-173">Select the following settings:</span></span>
    1. <span data-ttu-id="73a33-174">Exécuter ce script à l’aide des informations d’identification connectées : OUI</span><span class="sxs-lookup"><span data-stu-id="73a33-174">Run this script using the logged-on credentials: YES</span></span>
    1. <span data-ttu-id="73a33-175">Appliquer la vérification de la signature de script : NON</span><span class="sxs-lookup"><span data-stu-id="73a33-175">Enforce script signature check: NO</span></span>
    1. <span data-ttu-id="73a33-176">Exécuter un script dans l’hôte PowerShell 64 bits : OUI</span><span class="sxs-lookup"><span data-stu-id="73a33-176">Run script in 64-bit PowerShell Host: YES</span></span>

6. <span data-ttu-id="73a33-177">Sélectionnez les groupes d’appareils appropriés et appliquez la stratégie.</span><span class="sxs-lookup"><span data-stu-id="73a33-177">Select the proper device groups and apply the policy.</span></span>

#### <a name="microsoft-endpoint-manager-force-install-steps"></a><span data-ttu-id="73a33-178">Étapes de l'installation forcée de Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="73a33-178">Microsoft Endpoint Manager Force Install Steps</span></span>

<span data-ttu-id="73a33-179">Avant d'ajouter l'extension de la conformité Microsoft à la liste des extensions installées de force, il est important d'ingérer l'ADMX de Chrome.</span><span class="sxs-lookup"><span data-stu-id="73a33-179">Before adding the Microsoft Compliance Extension to the list of force-installed extensions, it is important to ingest the Chrome ADMX.</span></span> <span data-ttu-id="73a33-180">Les étapes de ce processus dans Microsoft Endpoint Manager sont documentées par Google : [Gérer le navigateur Chrome avec Microsoft Intune - Aide de Google Chrome Enterprise](https://support.google.com/chrome/a/answer/9102677?hl=en#zippy=%2Cstep-ingest-the-chrome-admx-file-into-intune).</span><span class="sxs-lookup"><span data-stu-id="73a33-180">Steps for this process in Microsoft Endpoint Manager are documented by Google: [Manage Chrome Browser with Microsoft Intune - Google Chrome Enterprise Help](https://support.google.com/chrome/a/answer/9102677?hl=en#zippy=%2Cstep-ingest-the-chrome-admx-file-into-intune).</span></span>

 <span data-ttu-id="73a33-181">Après avoir ingéré l’ADMX, vous pouvez suivre les étapes ci-dessous pour créer un profil de configuration pour cette extension.</span><span class="sxs-lookup"><span data-stu-id="73a33-181">After ingesting the ADMX, the steps below can be followed to create a configuration profile for this extension.</span></span>

1. <span data-ttu-id="73a33-182">Connectez-vous au centre d'administration de la gestion des points de terminaison Microsoft ( https://endpoint.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="73a33-182">Sign in to the Microsoft Endpoint Manager Admin Center (https://endpoint.microsoft.com).</span></span>

2. <span data-ttu-id="73a33-183">Accédez aux profils de configuration.</span><span class="sxs-lookup"><span data-stu-id="73a33-183">Navigate to Configuration Profiles.</span></span>

3. <span data-ttu-id="73a33-184">Sélectionnez **Créer le profil**.</span><span class="sxs-lookup"><span data-stu-id="73a33-184">Select **Create Profile**.</span></span>

4. <span data-ttu-id="73a33-185">Sélectionnez **Windows 10** en tant que plateforme.</span><span class="sxs-lookup"><span data-stu-id="73a33-185">Select **Windows 10** as the platform.</span></span>

5. <span data-ttu-id="73a33-186">Sélectionnez **Personnaliser** en tant que type de profil.</span><span class="sxs-lookup"><span data-stu-id="73a33-186">Select **Custom** as profile type.</span></span>

6. <span data-ttu-id="73a33-187">Sélectionnez l’onglet **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="73a33-187">Select the **Settings** tab.</span></span>

7. <span data-ttu-id="73a33-188">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="73a33-188">Select **Add**.</span></span>

8. <span data-ttu-id="73a33-189">Entrez les informations de stratégie suivantes.</span><span class="sxs-lookup"><span data-stu-id="73a33-189">Enter the following policy information.</span></span>

    <span data-ttu-id="73a33-190">OMA-URI : `./Device/Vendor/MSFT/Policy/Config/Chrome~Policy~googlechrome~Extensions/ExtensionInstallForcelist`</span><span class="sxs-lookup"><span data-stu-id="73a33-190">OMA-URI: `./Device/Vendor/MSFT/Policy/Config/Chrome~Policy~googlechrome~Extensions/ExtensionInstallForcelist`</span></span><br/>
    <span data-ttu-id="73a33-191">Type de données`String`</span><span class="sxs-lookup"><span data-stu-id="73a33-191">Data type: `String`</span></span><br/>
    <span data-ttu-id="73a33-192">Valeur : `<enabled/><data id="ExtensionInstallForcelistDesc" value="1&#xF000; echcggldkblhodogklpincgchnpgcdco;https://clients2.google.com/service/update2/crx"/>`</span><span class="sxs-lookup"><span data-stu-id="73a33-192">Value: `<enabled/><data id="ExtensionInstallForcelistDesc" value="1&#xF000; echcggldkblhodogklpincgchnpgcdco;https://clients2.google.com/service/update2/crx"/>`</span></span>

9. <span data-ttu-id="73a33-193">Cliquez sur Créer.</span><span class="sxs-lookup"><span data-stu-id="73a33-193">Click create.</span></span>

### <a name="deploy-using-group-policy"></a><span data-ttu-id="73a33-194">Déployer à l’aide d’une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="73a33-194">Deploy using Group Policy</span></span>

<span data-ttu-id="73a33-195">Si vous ne voulez pas utiliser Microsoft Endpoint Manager, vous pouvez utiliser des stratégies de groupe pour déployer l’extension de la conformité Microsoft au sein de votre organisation</span><span class="sxs-lookup"><span data-stu-id="73a33-195">If you don't want to use Microsoft Endpoint Manager, you can use group policies to deploy the Microsoft Compliance Extension across your organization</span></span>

1. <span data-ttu-id="73a33-196">Vos appareils doivent être gérables via une stratégie de groupe, et vous devez importer tous les ADMX Chrome dans le Store central de stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="73a33-196">Your devices must be manageable via Group Policy, and you need to import all Chrome ADMXs into the Group Policy Central Store.</span></span> <span data-ttu-id="73a33-197">Pour plus d’informations, reportez-vous à l’article [Comment créer et gérer le magasin central des modèles d’administration de stratégie de groupe dans Windows](/troubleshoot/windows-client/group-policy/create-and-manage-central-store).</span><span class="sxs-lookup"><span data-stu-id="73a33-197">For more information, see [How to create and manage the Central Store for Group Policy Administrative Templates in Windows](/troubleshoot/windows-client/group-policy/create-and-manage-central-store).</span></span>

2. <span data-ttu-id="73a33-198">Créez un script PowerShell en utilisant cette commande PowerShell :</span><span class="sxs-lookup"><span data-stu-id="73a33-198">Create a PowerShell script using this PowerShell command:</span></span>

    ```powershell
    Get-Item -path "HKLM:\SOFTWARE\Microsoft\Windows Defender\Miscellaneous Configuration" | New-ItemProperty -Name DlpDisableBrowserCache -Value 0 -Force
    ```

3. <span data-ttu-id="73a33-199">Ouvrez la **Console de gestion des stratégies de groupe** et accédez à votre unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="73a33-199">Open the **Group Policy Management Console** and navigate to your organizational unit (OU).</span></span>

4. <span data-ttu-id="73a33-200">Cliquez avec le bouton droit et sélectionnez **Créer un GPO dans ce domaine et lier ici**.</span><span class="sxs-lookup"><span data-stu-id="73a33-200">Right-click and select **Create a GPO in this domain and Link it here**.</span></span> <span data-ttu-id="73a33-201">Lorsque vous y êtes invité, attribuez un nom descriptif à cet objet de stratégie de groupe (GPO) et terminez sa création.</span><span class="sxs-lookup"><span data-stu-id="73a33-201">When prompted, assign a descriptive name to this group policy object (GPO) and finish creating it.</span></span>

5. <span data-ttu-id="73a33-202">Cliquez avec le bouton droit sur le GPO, puis sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="73a33-202">Right-click the GPO and select **Edit**.</span></span>

6. <span data-ttu-id="73a33-203">Accédez à **Configuration de l'ordinateur** > **Préférences** > **Panneau de configuration Paramètres** > **Tâches planifiées**.</span><span class="sxs-lookup"><span data-stu-id="73a33-203">Go to **Computer Configuration** > **Preferences** > **Control Panel Settings** > **Scheduled Tasks**.</span></span>

7. <span data-ttu-id="73a33-204">Créez une tâche immédiate en faisant un clic droit et en sélectionnant **Nouveau** > **Tâche immédiate (au moins Windows 7)**.</span><span class="sxs-lookup"><span data-stu-id="73a33-204">Create a new immediate task by selecting right-clicking and selecting **New** > **Immediate Task (At least Windows 7)**.</span></span>

8. <span data-ttu-id="73a33-205">Donnez un nom et une description à la tâche.</span><span class="sxs-lookup"><span data-stu-id="73a33-205">Give the task a name & description.</span></span>

9. <span data-ttu-id="73a33-206">Sélectionnez le compte correspondant pour exécuter la tâche immédiate (par exemple, NT Authority).</span><span class="sxs-lookup"><span data-stu-id="73a33-206">Choose the corresponding account to run the immediate task, for example NT Authority</span></span>

10. <span data-ttu-id="73a33-207">Sélectionnez **Exécuter avec les autorisations maximales**.</span><span class="sxs-lookup"><span data-stu-id="73a33-207">Select **Run with highest privileges**.</span></span>

11. <span data-ttu-id="73a33-208">Configurez la stratégie pour Windows 10.</span><span class="sxs-lookup"><span data-stu-id="73a33-208">Configure the policy for Windows 10.</span></span>

12. <span data-ttu-id="73a33-209">Dans l’onglet **Actions** , sélectionnez l’action **Démarrer un programme**.</span><span class="sxs-lookup"><span data-stu-id="73a33-209">In the **Actions** tab, select the action **Start a program**.</span></span>

13. <span data-ttu-id="73a33-210">Entrez le chemin d’accès au programme/script créé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="73a33-210">Enter the path to the Program/Script created in Step 1.</span></span>

14. <span data-ttu-id="73a33-211">Sélectionnez **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="73a33-211">Select **Apply**.</span></span>

#### <a name="adding-the-chrome-extension-to-the-forceinstall-list"></a><span data-ttu-id="73a33-212">Ajout de l'extension Chrome à la liste de ForceInstall</span><span class="sxs-lookup"><span data-stu-id="73a33-212">Adding the Chrome Extension to the ForceInstall List</span></span>

1. <span data-ttu-id="73a33-213">Dans l’Éditeur de gestion des stratégies de groupe, accédez à votre OU.</span><span class="sxs-lookup"><span data-stu-id="73a33-213">In the Group Policy Management Editor, navigate to your OU.</span></span>

2. <span data-ttu-id="73a33-214">Développez le chemin d’accès suivant **Configuration ordinateur/utilisateur** > **Stratégies d’administration** > **Modèles d’administration** > **Modèles d’administration classiques** > **Google** > **Google Chrome** > **Extensions**.</span><span class="sxs-lookup"><span data-stu-id="73a33-214">Expand the following path **Computer/User configuration** > **Policies** > **Administrative templates** > **Classic administrative templates** > **Google** > **Google Chrome** > **Extensions**.</span></span> <span data-ttu-id="73a33-215">Ce chemin d’accès peut varier en fonction de votre configuration.</span><span class="sxs-lookup"><span data-stu-id="73a33-215">This path may vary depending on your configuration.</span></span>

3. <span data-ttu-id="73a33-216">Sélectionnez **Configurer la liste des extensions installées avec force**.</span><span class="sxs-lookup"><span data-stu-id="73a33-216">Select **Configure the list of force-installed extensions**.</span></span>

4. <span data-ttu-id="73a33-217">Cliquez avec le bouton droit et sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="73a33-217">Right click and select **Edit**.</span></span>

5. <span data-ttu-id="73a33-218">Sélectionnez **Activé**.</span><span class="sxs-lookup"><span data-stu-id="73a33-218">Select **Enabled**.</span></span>

6. <span data-ttu-id="73a33-219">Sélectionnez **Afficher**.</span><span class="sxs-lookup"><span data-stu-id="73a33-219">Select **Show**.</span></span>

7. <span data-ttu-id="73a33-220">Sous **Valeur**, ajoutez l’entrée suivante : `echcggldkblhodogklpincgchnpgcdco;https://clients2.google.com/service/update2/crx`</span><span class="sxs-lookup"><span data-stu-id="73a33-220">Under **Value**, add the following entry: `echcggldkblhodogklpincgchnpgcdco;https://clients2.google.com/service/update2/crx`</span></span>

8. <span data-ttu-id="73a33-221">Sélectionnez **OK**, puis **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="73a33-221">Select **OK** and then **Apply**.</span></span>

### <a name="test-the-extension"></a><span data-ttu-id="73a33-222">Tester l’extension</span><span class="sxs-lookup"><span data-stu-id="73a33-222">Test the Extension</span></span>

#### <a name="upload-to-cloud-service-or-access-by-unallowed-browsers-cloud-egress"></a><span data-ttu-id="73a33-223">Chargement vers un service en ligne, ou accès par des navigateurs non autorisés sortie du cloud</span><span class="sxs-lookup"><span data-stu-id="73a33-223">Upload to cloud service, or access by unallowed browsers Cloud Egress</span></span>

1. <span data-ttu-id="73a33-224">Créez ou obtenez un élément sensible, puis essayez de télécharger un fichier vers l’un des domaines de service restreints de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="73a33-224">Create or get a sensitive item and, try to upload a file to one of your organization’s restricted service domains.</span></span> <span data-ttu-id="73a33-225">Les données sensibles doivent correspondre à l'un de nos [Types d'informations sensibles intégrés](sensitive-information-type-entity-definitions.md), ou à l'un des types d'informations sensibles de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="73a33-225">The sensitive data must match one of our built-in [Sensitive Info Types](sensitive-information-type-entity-definitions.md), or one of your organization’s sensitive information types.</span></span> <span data-ttu-id="73a33-226">Vous devriez recevoir une notification de toast DLP sur l'appareil à partir duquel vous effectuez le test, indiquant que cette action n'est pas autorisée lorsque le fichier est ouvert.</span><span class="sxs-lookup"><span data-stu-id="73a33-226">You should get a DLP toast notification on the device you are testing from that shows that this action is not allowed when the file is open.</span></span>

#### <a name="testing-other-dlp-scenarios-in-chrome"></a><span data-ttu-id="73a33-227">Tests d’autres scénarios DLP dans Chrome</span><span class="sxs-lookup"><span data-stu-id="73a33-227">Testing other DLP scenarios in Chrome</span></span>

<span data-ttu-id="73a33-228">Maintenant que vous avez supprimé Chrome de la liste des navigateurs/applications interdits, vous pouvez tester les scénarios ci-dessous pour vérifier que le comportement répond aux exigences de votre organisation :</span><span class="sxs-lookup"><span data-stu-id="73a33-228">Now that you’ve removed Chrome from the disallowed browsers/apps list, you can test the scenarios below to confirm the behavior meets your organization’s requirements:</span></span>

- <span data-ttu-id="73a33-229">Copier des données d’un élément sensible vers un autre document à l’aide du Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="73a33-229">Copy data from a sensitive item to another document using the Clipboard</span></span>
  - <span data-ttu-id="73a33-230">Pour tester, ouvrez un fichier protégé contre les actions de copie vers le presse-papiers dans le navigateur Chrome et essayez de copier les données du fichier.</span><span class="sxs-lookup"><span data-stu-id="73a33-230">To test, open a file that is protected against copy to clipboard actions in the Chrome browser and attempt to copy data from the file.</span></span>
  - <span data-ttu-id="73a33-231">Résultat attendu : notification toast DLP indiquant que cette action n’est pas autorisée lorsque le fichier est ouvert.</span><span class="sxs-lookup"><span data-stu-id="73a33-231">Expected Result: A DLP toast notification showing that this action is not allowed when the file is open.</span></span>
- <span data-ttu-id="73a33-232">Imprimer un document</span><span class="sxs-lookup"><span data-stu-id="73a33-232">Print a document</span></span>
  - <span data-ttu-id="73a33-233">Pour tester, ouvrez un fichier protégé contre les actions d’impression dans le navigateur Chrome et essayez d’imprimer le fichier.</span><span class="sxs-lookup"><span data-stu-id="73a33-233">To test, open a file that is protected against print actions in the Chrome browser and attempt to print the file.</span></span>
  - <span data-ttu-id="73a33-234">Résultat attendu : notification toast DLP indiquant que cette action n’est pas autorisée lorsque le fichier est ouvert.</span><span class="sxs-lookup"><span data-stu-id="73a33-234">Expected Result: A DLP toast notification showing that this action is not allowed when the file is open.</span></span>
- <span data-ttu-id="73a33-235">Copier sur un support amovible USB</span><span class="sxs-lookup"><span data-stu-id="73a33-235">Copy to USB Removeable Media</span></span>
  - <span data-ttu-id="73a33-236">Pour le tester, essayez d'enregistrer le fichier sur un support de stockage amovible.</span><span class="sxs-lookup"><span data-stu-id="73a33-236">To test, try to save the file to a removeable media storage.</span></span>
  - <span data-ttu-id="73a33-237">Résultat attendu : notification toast DLP indiquant que cette action n’est pas autorisée lorsque le fichier est ouvert.</span><span class="sxs-lookup"><span data-stu-id="73a33-237">Expected Result: A DLP toast notification showing that this action is not allowed when the file is open.</span></span>
- <span data-ttu-id="73a33-238">Copier vers le partage réseau</span><span class="sxs-lookup"><span data-stu-id="73a33-238">Copy to Network Share</span></span>
  - <span data-ttu-id="73a33-239">Pour tester, essayez d’enregistrer le fichier sur un partage réseau.</span><span class="sxs-lookup"><span data-stu-id="73a33-239">To test, try to save the file to a network share.</span></span>
  - <span data-ttu-id="73a33-240">Résultat attendu : notification toast DLP indiquant que cette action n’est pas autorisée lorsque le fichier est ouvert.</span><span class="sxs-lookup"><span data-stu-id="73a33-240">Expected Result: A DLP toast notification showing that this action is not allowed when the file is open.</span></span>

### <a name="use-the-alerts-management-dashboard-to-viewing-chrome-dlp-alerts"></a><span data-ttu-id="73a33-241">Utiliser le tableau de bord de gestion des alertes pour afficher les alertes DLP dans Chrome</span><span class="sxs-lookup"><span data-stu-id="73a33-241">Use the Alerts Management Dashboard to viewing Chrome DLP alerts</span></span>

1. <span data-ttu-id="73a33-242">Ouvrez la page **Protection contre la perte de données** dans le [Centre de conformité Microsoft 365](https://compliance.microsoft.com), puis sélectionnez **Alertes**.</span><span class="sxs-lookup"><span data-stu-id="73a33-242">Open the **Data loss prevention** page in the [Microsoft 365 Compliance center](https://compliance.microsoft.com) and select **Alerts**.</span></span>

2. <span data-ttu-id="73a33-243">Reportez-vous aux procédures décrites dans [Comment configurer et afficher les alertes pour les stratégies DLP](dlp-configure-view-alerts-policies.md) pour afficher les alertes relatives à vos stratégies DLP de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="73a33-243">Refer to the procedures in [How to configure and view alerts for your DLP policies](dlp-configure-view-alerts-policies.md) to view alerts for your Endpoint DLP policies.</span></span>

### <a name="viewing-chrome-dlp-data-in-activity-explorer"></a><span data-ttu-id="73a33-244">Affichage de données DLP dans l’Explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="73a33-244">Viewing Chrome DLP data in activity explorer</span></span>

1. <span data-ttu-id="73a33-245">Ouvrez la [Page classification des données](https://compliance.microsoft.com/dataclassification?viewid=overview) pour votre domaine dans le centre de conformité Microsoft 365, puis sélectionnez **Explorateur d’activités**.</span><span class="sxs-lookup"><span data-stu-id="73a33-245">Open the [Data classification page](https://compliance.microsoft.com/dataclassification?viewid=overview) for your domain in the Microsoft 365 Compliance center and choose **Activity explorer**.</span></span>

2. <span data-ttu-id="73a33-246">Reportez-vous aux procédures décrites dans [Prise en main de l’Explorateur d’activités](data-classification-activity-explorer.md) pour accéder aux données de vos appareils de point de terminaison et les filtrer.</span><span class="sxs-lookup"><span data-stu-id="73a33-246">Refer to the procedures in [Get started with Activity explorer](data-classification-activity-explorer.md) to access and filter all the data for your Endpoint devices.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="73a33-247">![filtre de l’Explorateur d’activités pour les appareils de point de terminaison](../media/endpoint-dlp-4-getting-started-activity-explorer.png)</span><span class="sxs-lookup"><span data-stu-id="73a33-247">![activity explorer filter for endpoint devices](../media/endpoint-dlp-4-getting-started-activity-explorer.png)</span></span>

### <a name="known-issues-and-limitations"></a><span data-ttu-id="73a33-248">Problèmes et limites connus</span><span class="sxs-lookup"><span data-stu-id="73a33-248">Known Issues and Limitations</span></span>

1. <span data-ttu-id="73a33-249">L'application du Block Override pour la sortie du nuage n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="73a33-249">Block Override enforcement for cloud egress is not supported.</span></span>
2. <span data-ttu-id="73a33-250">Le mode Incognito n'est pas pris en charge et doit être désactivé.</span><span class="sxs-lookup"><span data-stu-id="73a33-250">Incognito mode is not supported and must be disabled.</span></span>

## <a name="next-steps"></a><span data-ttu-id="73a33-251">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="73a33-251">Next steps</span></span>

<span data-ttu-id="73a33-252">Maintenant que vous disposez d’appareils intégrés et que vous pouvez afficher les données d’activité dans l’Explorateur d’activités, vous êtes prêt à passer à l’étape suivante dans laquelle vous créez des stratégies DLP qui protègent vos éléments sensibles.</span><span class="sxs-lookup"><span data-stu-id="73a33-252">Now that you have onboarded devices and can view the activity data in Activity explorer, you are ready to move on to your next step where you create DLP policies that protect your sensitive items.</span></span>

- [<span data-ttu-id="73a33-253">Utilisation des points de terminaison protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="73a33-253">Using Endpoint data loss prevention</span></span>](endpoint-dlp-using.md)

## <a name="see-also"></a><span data-ttu-id="73a33-254">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73a33-254">See also</span></span>

- [<span data-ttu-id="73a33-255">Découvrir la protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="73a33-255">Learn about Endpoint data loss prevention</span></span>](endpoint-dlp-learn-about.md)
- [<span data-ttu-id="73a33-256">Utilisation de la prévention des pertes de données sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="73a33-256">Using Endpoint data loss prevention</span></span>](endpoint-dlp-using.md)
- [<span data-ttu-id="73a33-257">En savoir plus sur la prévention des pertes de données</span><span class="sxs-lookup"><span data-stu-id="73a33-257">Learn about data loss prevention</span></span>](dlp-learn-about-dlp.md)
- [<span data-ttu-id="73a33-258">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="73a33-258">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="73a33-259">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="73a33-259">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="73a33-260">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="73a33-260">Microsoft Defender for Endpoint</span></span>](/windows/security/threat-protection/)
- <span data-ttu-id="73a33-261">[Outils et méthodes d’intégration pour les appareils Windows 10](/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="73a33-261">[Onboarding tools and methods for Windows 10 machines](/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints)</span></span>
- [<span data-ttu-id="73a33-262">Abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="73a33-262">Microsoft 365 subscription</span></span>](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1)
- [<span data-ttu-id="73a33-263">Azure AD appareils joints</span><span class="sxs-lookup"><span data-stu-id="73a33-263">Azure AD joined devices</span></span>](/azure/active-directory/devices/concept-azure-ad-join)
- [<span data-ttu-id="73a33-264">Télécharger le nouveau Microsoft Edge sur la base de chrome</span><span class="sxs-lookup"><span data-stu-id="73a33-264">Download the new Microsoft Edge based on Chromium</span></span>](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium)
