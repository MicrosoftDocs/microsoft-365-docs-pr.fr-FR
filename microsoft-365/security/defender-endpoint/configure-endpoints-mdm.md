---
title: Intégrer les appareils Windows 10 à l’aide des outils de gestion des appareils mobiles
description: Utilisez les outils de gestion des appareils mobiles pour déployer le package de configuration sur les appareils afin qu'ils soient intégrés au service.
keywords: intégrer des appareils à l'aide de mdm, gestion des appareils, intégration de Microsoft Defender pour les appareils Endpoint, mdm
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 951b0f33356ab99485f09ccc4147691e13ed3c6e
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51935004"
---
# <a name="onboard-windows-10-devices-using-mobile-device-management-tools"></a><span data-ttu-id="87df0-104">Intégrer les appareils Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="87df0-104">Onboard Windows 10 devices using Mobile Device Management tools</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="87df0-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="87df0-105">**Applies to:**</span></span>
- [<span data-ttu-id="87df0-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="87df0-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="87df0-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="87df0-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="87df0-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="87df0-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="87df0-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="87df0-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-configureendpointsmdm-abovefoldlink)

<span data-ttu-id="87df0-110">Vous pouvez utiliser des solutions de gestion des périphériques mobiles (MDM) pour configurer des appareils.</span><span class="sxs-lookup"><span data-stu-id="87df0-110">You can use mobile device management (MDM) solutions to configure devices.</span></span> <span data-ttu-id="87df0-111">Defender for Endpoint prend en charge les appareils mobiles en fournissant des OMA-URIs pour créer des stratégies pour gérer les appareils.</span><span class="sxs-lookup"><span data-stu-id="87df0-111">Defender for Endpoint supports MDMs by providing OMA-URIs to create policies to manage devices.</span></span>

<span data-ttu-id="87df0-112">Pour plus d'informations sur l'utilisation du programme CSP Defender for Endpoint, voir le fichier DDF [WindowsAdvancedThreatProtection](https://msdn.microsoft.com/library/windows/hardware/mt723296(v=vs.85).aspx) et [WindowsAdvancedThreatProtection.](https://msdn.microsoft.com/library/windows/hardware/mt723297(v=vs.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="87df0-112">For more information on using Defender for Endpoint CSP see, [WindowsAdvancedThreatProtection CSP](https://msdn.microsoft.com/library/windows/hardware/mt723296(v=vs.85).aspx) and [WindowsAdvancedThreatProtection DDF file](https://msdn.microsoft.com/library/windows/hardware/mt723297(v=vs.85).aspx).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="87df0-113">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="87df0-113">Before you begin</span></span>
<span data-ttu-id="87df0-114">Si vous utilisez Microsoft Intune, l'appareil doit être inscrit à la gestion des appareils.</span><span class="sxs-lookup"><span data-stu-id="87df0-114">If you're using Microsoft Intune, you must have the device MDM Enrolled.</span></span> <span data-ttu-id="87df0-115">Dans le cas contraire, les paramètres ne seront pas appliqués correctement.</span><span class="sxs-lookup"><span data-stu-id="87df0-115">Otherwise, settings will not be applied successfully.</span></span> 

<span data-ttu-id="87df0-116">Pour plus d'informations sur l'activation de la gestion des périphériques multi-appareils avec Microsoft Intune, voir Inscription des appareils [(Microsoft Intune).](https://docs.microsoft.com/mem/intune/enrollment/device-enrollment)</span><span class="sxs-lookup"><span data-stu-id="87df0-116">For more information on enabling MDM with Microsoft Intune, see [Device enrollment (Microsoft Intune)](https://docs.microsoft.com/mem/intune/enrollment/device-enrollment).</span></span>

## <a name="onboard-devices-using-microsoft-intune"></a><span data-ttu-id="87df0-117">Intégrer des appareils à l'aide de Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="87df0-117">Onboard devices using Microsoft Intune</span></span>

<span data-ttu-id="87df0-118">[![Image du PDF montrant l'intégration d'appareils à Defender for Endpoint à l'aide de Microsoft Intune ](images/onboard-intune.png)](images/onboard-intune-big.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="87df0-118">[![Image of the PDF showing onboarding devices to Defender for Endpoint using Microsoft Intune](images/onboard-intune.png) ](images/onboard-intune-big.png#lightbox)</span></span>

<span data-ttu-id="87df0-119">Consultez le [fichier PDF](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf)  ou  [Visio](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.vsdx) pour voir les différents chemins d'accès dans le déploiement de Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="87df0-119">Check out the [PDF](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf)  or  [Visio](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.vsdx) to see the various paths in deploying Defender for Endpoint.</span></span> 

<span data-ttu-id="87df0-120">Suivez les instructions [d'Intune.](https://docs.microsoft.com/intune/advanced-threat-protection)</span><span class="sxs-lookup"><span data-stu-id="87df0-120">Follow the instructions from [Intune](https://docs.microsoft.com/intune/advanced-threat-protection).</span></span>

<span data-ttu-id="87df0-121">Pour plus d'informations sur l'utilisation du programme CSP Defender for Endpoint, voir le fichier DDF [WindowsAdvancedThreatProtection](https://msdn.microsoft.com/library/windows/hardware/mt723296(v=vs.85).aspx) et [WindowsAdvancedThreatProtection.](https://msdn.microsoft.com/library/windows/hardware/mt723297(v=vs.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="87df0-121">For more information on using Defender for Endpoint CSP see, [WindowsAdvancedThreatProtection CSP](https://msdn.microsoft.com/library/windows/hardware/mt723296(v=vs.85).aspx) and [WindowsAdvancedThreatProtection DDF file](https://msdn.microsoft.com/library/windows/hardware/mt723297(v=vs.85).aspx).</span></span>


> [!NOTE]
> - <span data-ttu-id="87df0-122">La **stratégie État d'état d'état des appareils** intégrés utilise des propriétés en lecture seule et ne peut pas être corrigé.</span><span class="sxs-lookup"><span data-stu-id="87df0-122">The **Health Status for onboarded devices** policy uses read-only properties and can't be remediated.</span></span>
> - <span data-ttu-id="87df0-123">La configuration de la fréquence de rapports de données de diagnostic est disponible uniquement pour les appareils sur Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="87df0-123">Configuration of diagnostic data reporting frequency is only available for devices on Windows 10, version 1703.</span></span>


>[!TIP]
> <span data-ttu-id="87df0-124">Après avoir intégré l'appareil, vous pouvez choisir d'exécuter un test de détection pour vérifier qu'un appareil est correctement intégré au service.</span><span class="sxs-lookup"><span data-stu-id="87df0-124">After onboarding the device, you can choose to run a detection test to verify that a device is properly onboarded to the service.</span></span> <span data-ttu-id="87df0-125">Pour plus d'informations, voir Exécuter un test de détection sur un appareil [Microsoft Defender pour point de terminaison nouvellement intégré.](run-detection-test.md)</span><span class="sxs-lookup"><span data-stu-id="87df0-125">For more information, see [Run a detection test on a newly onboarded Microsoft Defender for Endpoint device](run-detection-test.md).</span></span>


<span data-ttu-id="87df0-126">Consultez le [pdf ou](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf)  [Visio](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.vsdx) pour voir les différents chemins d'accès dans le déploiement de Microsoft Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="87df0-126">Check out the [PDF](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf)  or  [Visio](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.vsdx) to see the various paths in deploying Microsoft Defender for Endpoint.</span></span>

## <a name="offboard-and-monitor-devices-using-mobile-device-management-tools"></a><span data-ttu-id="87df0-127">Utiliser les outils de gestion des périphériques mobiles pour les appareils mobiles pour les hors-bord et les surveiller</span><span class="sxs-lookup"><span data-stu-id="87df0-127">Offboard and monitor devices using Mobile Device Management tools</span></span>
<span data-ttu-id="87df0-128">Pour des raisons de sécurité, le package utilisé pour la sortie des appareils expirera 30 jours après la date de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="87df0-128">For security reasons, the package used to Offboard devices will expire 30 days after the date it was downloaded.</span></span> <span data-ttu-id="87df0-129">Les packages deboarding expirés envoyés à un appareil seront rejetés.</span><span class="sxs-lookup"><span data-stu-id="87df0-129">Expired offboarding packages sent to a device will be rejected.</span></span> <span data-ttu-id="87df0-130">Lorsque vous téléchargez un package de déclassage, vous êtes informé de la date d'expiration des packages et il est également inclus dans le nom du package.</span><span class="sxs-lookup"><span data-stu-id="87df0-130">When downloading an offboarding package you will be notified of the packages expiry date and it will also be included in the package name.</span></span>

> [!NOTE]
> <span data-ttu-id="87df0-131">Les stratégies d'intégration et deboarding ne doivent pas être déployées sur le même appareil en même temps, sinon cela provoquera des collisions imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="87df0-131">Onboarding and offboarding policies must not be deployed on the same device at the same time, otherwise this will cause unpredictable collisions.</span></span>

1. <span data-ttu-id="87df0-132">Obtenez le package deboarding à partir du [Centre de sécurité Microsoft Defender](https://securitycenter.windows.com/):</span><span class="sxs-lookup"><span data-stu-id="87df0-132">Get the offboarding package from [Microsoft Defender Security Center](https://securitycenter.windows.com/):</span></span>

   1. <span data-ttu-id="87df0-133">Dans le volet de navigation, sélectionnez **Paramètres**  >  **Deboarding**.</span><span class="sxs-lookup"><span data-stu-id="87df0-133">In the navigation pane, select **Settings** > **Offboarding**.</span></span>

   1. <span data-ttu-id="87df0-134">Sélectionnez Windows 10 comme système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="87df0-134">Select Windows 10 as the operating system.</span></span>

   1. <span data-ttu-id="87df0-135">Dans le **champ Méthode de déploiement,** sélectionnez **Gestion des périphériques mobiles / Microsoft Intune**.</span><span class="sxs-lookup"><span data-stu-id="87df0-135">In the **Deployment method** field, select **Mobile Device Management / Microsoft Intune**.</span></span>
    
   1. <span data-ttu-id="87df0-136">Cliquez **sur Télécharger le package,** puis enregistrez le fichier .zip.</span><span class="sxs-lookup"><span data-stu-id="87df0-136">Click **Download package**, and save the .zip file.</span></span>

2. <span data-ttu-id="87df0-137">Extrayez le contenu du fichier .zip vers un emplacement partagé en lecture seule accessible par les administrateurs réseau qui déploieront le package.</span><span class="sxs-lookup"><span data-stu-id="87df0-137">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the network administrators who will deploy the package.</span></span> <span data-ttu-id="87df0-138">Vous devez avoir un fichier nommé *WindowsDefenderATP_valid_until_YYYY-MM-DD.offboarding*.</span><span class="sxs-lookup"><span data-stu-id="87df0-138">You should have a file named *WindowsDefenderATP_valid_until_YYYY-MM-DD.offboarding*.</span></span>

3. <span data-ttu-id="87df0-139">Utilisez la stratégie de configuration personnalisée Microsoft Intune pour déployer les paramètres OMA-URI pris en charge suivants.</span><span class="sxs-lookup"><span data-stu-id="87df0-139">Use the Microsoft Intune custom configuration policy to deploy the following supported OMA-URI settings.</span></span>

      <span data-ttu-id="87df0-140">OMA-URI : ./Device/Vendor/MSFT/WindowsAdvancedThreatProtection/Offboarding</span><span class="sxs-lookup"><span data-stu-id="87df0-140">OMA-URI: ./Device/Vendor/MSFT/WindowsAdvancedThreatProtection/Offboarding</span></span><br/>
      <span data-ttu-id="87df0-141">Type de date : Chaîne</span><span class="sxs-lookup"><span data-stu-id="87df0-141">Date type: String</span></span><br/>
      <span data-ttu-id="87df0-142">Valeur : [Copier et coller la valeur à partir du contenu du fichier WindowsDefenderATP_valid_until_YYYY-MM-DD.offboarding]</span><span class="sxs-lookup"><span data-stu-id="87df0-142">Value: [Copy and paste the value from the content of the WindowsDefenderATP_valid_until_YYYY-MM-DD.offboarding file]</span></span>

<span data-ttu-id="87df0-143">Pour plus d'informations sur les paramètres de stratégie Microsoft Intune, voir les paramètres de stratégie [Windows 10 dans Microsoft Intune.](https://docs.microsoft.com/intune/deploy-use/windows-10-policy-settings-in-microsoft-intune)</span><span class="sxs-lookup"><span data-stu-id="87df0-143">For more information on Microsoft Intune policy settings see, [Windows 10 policy settings in Microsoft Intune](https://docs.microsoft.com/intune/deploy-use/windows-10-policy-settings-in-microsoft-intune).</span></span>


> [!NOTE]
> <span data-ttu-id="87df0-144">La **stratégie État d'état d'état des appareils** déboardés utilise des propriétés en lecture seule et ne peut pas être corrigé.</span><span class="sxs-lookup"><span data-stu-id="87df0-144">The **Health Status for offboarded devices** policy uses read-only properties and can't be remediated.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="87df0-145">Laboarding empêche l'appareil d'envoyer des données de capteur au portail, mais les données de l'appareil, y compris la référence aux alertes qu'il a eues, seront conservées pendant 6 mois.</span><span class="sxs-lookup"><span data-stu-id="87df0-145">Offboarding causes the device to stop sending sensor data to the portal but data from the device, including reference to any alerts it has had will be retained for up to 6 months.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87df0-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87df0-146">Related topics</span></span>
- [<span data-ttu-id="87df0-147">Intégrer des appareils Windows 10 à l'aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="87df0-147">Onboard Windows 10 devices using Group Policy</span></span>](configure-endpoints-gp.md)
- [<span data-ttu-id="87df0-148">Intégrer des appareils Windows 10 à l'aide de Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="87df0-148">Onboard Windows 10 devices using Microsoft Endpoint Configuration Manager</span></span>](configure-endpoints-sccm.md)
- [<span data-ttu-id="87df0-149">Intégrer les appareils Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="87df0-149">Onboard Windows 10 devices using a local script</span></span>](configure-endpoints-script.md)
- [<span data-ttu-id="87df0-150">Intégrer les ordinateurs virtuels d’infrastructure de bureau (VDI) non persistants</span><span class="sxs-lookup"><span data-stu-id="87df0-150">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>](configure-endpoints-vdi.md)
- [<span data-ttu-id="87df0-151">Exécuter un test de détection sur un appareil Microsoft Defender pour point de terminaison nouvellement intégré</span><span class="sxs-lookup"><span data-stu-id="87df0-151">Run a detection test on a newly onboarded Microsoft Defender for Endpoint device</span></span>](run-detection-test.md)
- [<span data-ttu-id="87df0-152">Résoudre les problèmes d'intégration de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="87df0-152">Troubleshoot Microsoft Defender for Endpoint onboarding issues</span></span>](troubleshoot-onboarding.md)
