---
title: Périphériques Windows 10 embarqués à l’aide d’un script local
f1.keywords: NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
description: Utilisez un script local pour déployer le package de configuration sur les appareils de sorte qu’ils soient intégrés au service.
ms.openlocfilehash: 74152f9488623d39e32ee4e47a452bd1daea28c7
ms.sourcegitcommit: 6647055154002c7d3b8f7ce25ad53c9636bc8066
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2020
ms.locfileid: "48769430"
---
# <a name="onboard-windows-10-devices-using-a-local-script"></a><span data-ttu-id="a1ad5-103">Périphériques Windows 10 embarqués à l’aide d’un script local</span><span class="sxs-lookup"><span data-stu-id="a1ad5-103">Onboard Windows 10 devices using a local script</span></span>

<span data-ttu-id="a1ad5-104">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a1ad5-104">**Applies to:**</span></span>

- [<span data-ttu-id="a1ad5-105">Microsoft 365 protection contre la perte de données (DLP)</span><span class="sxs-lookup"><span data-stu-id="a1ad5-105">Microsoft 365 Endpoint data loss prevention (DLP)</span></span>](/microsoft-365/compliance/endpoint-dlp-learn-about)

<span data-ttu-id="a1ad5-106">Vous pouvez également intégrer manuellement des appareils individuels à la protection contre la perte de données de point de terminaison de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-106">You can also manually onboard individual devices to Microsoft 365 Endpoint data loss prevention.</span></span> <span data-ttu-id="a1ad5-107">Vous pouvez effectuer cette opération en premier lieu lors du test du service avant de vous valider sur l’intégration de tous les périphériques de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-107">You might want to do this first when testing the service before you commit to onboarding all devices in your network.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1ad5-108">Ce script a été optimisé pour une utilisation sur un maximum de 10 appareils.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-108">This script has been optimized for use on up to 10 devices.</span></span>
>
> <span data-ttu-id="a1ad5-109">Pour déployer à l’envergure, utilisez d' [autres options de déploiement](dlp-configure-endpoints.md).</span><span class="sxs-lookup"><span data-stu-id="a1ad5-109">To deploy at scale, use [other deployment options](dlp-configure-endpoints.md).</span></span> <span data-ttu-id="a1ad5-110">Par exemple, vous pouvez déployer un script d’intégration sur plus de 10 appareils en production avec le script disponible dans les [appareils Windows 10 embarqués à l’aide](dlp-configure-endpoints-gp.md)de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-110">For example, you can deploy an onboarding script to more than 10 devices in production with the script available in [Onboard Windows 10 devices using Group Policy](dlp-configure-endpoints-gp.md).</span></span>

## <a name="onboard-devices"></a><span data-ttu-id="a1ad5-111">Périphériques intégrés</span><span class="sxs-lookup"><span data-stu-id="a1ad5-111">Onboard devices</span></span>
 
1.  <span data-ttu-id="a1ad5-112">Ouvrez le fichier Package. zip de la configuration GP ( *DeviceComplianceOnboardingPackage.zip* ) que vous avez téléchargé à partir de l’Assistant d’intégration de service.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-112">Open the GP configuration package .zip file ( *DeviceComplianceOnboardingPackage.zip* ) that you downloaded from the service onboarding wizard.</span></span> <span data-ttu-id="a1ad5-113">Vous pouvez également obtenir le package à partir du [Centre de conformité Microsoft](https://compliance.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="a1ad5-113">You can also get the package from [Microsoft Compliance center](https://compliance.microsoft.com)</span></span>

2. <span data-ttu-id="a1ad5-114">Dans le volet de navigation, sélectionnez **paramètres** d’intégration de l'  >  **appareil** .</span><span class="sxs-lookup"><span data-stu-id="a1ad5-114">In the navigation pane, select **Settings** > **Device onboarding** .</span></span>

3. <span data-ttu-id="a1ad5-115">Dans le champ **méthode de déploiement** , sélectionnez **script local** .</span><span class="sxs-lookup"><span data-stu-id="a1ad5-115">In the **Deployment method** field, select **Local Script** .</span></span>

4. <span data-ttu-id="a1ad5-116">Cliquez sur **Télécharger le package** et enregistrez le fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-116">Click **Download package** and save the .zip file.</span></span>
  
5. <span data-ttu-id="a1ad5-117">Extrayez le contenu du package de configuration vers un emplacement de l’appareil que vous souhaitez intégrer (par exemple, le bureau).</span><span class="sxs-lookup"><span data-stu-id="a1ad5-117">Extract the contents of the configuration package to a location on the device you want to onboard (for example, the Desktop).</span></span> <span data-ttu-id="a1ad5-118">Vous devez avoir un fichier nommé *DeviceOnboardingScript. cmd* .</span><span class="sxs-lookup"><span data-stu-id="a1ad5-118">You should have a file named *DeviceOnboardingScript.cmd* .</span></span>

6.  <span data-ttu-id="a1ad5-119">Ouvrez une invite de ligne de commande avec élévation de privilèges sur l’appareil et exécutez le script :</span><span class="sxs-lookup"><span data-stu-id="a1ad5-119">Open an elevated command-line prompt on the device and run the script:</span></span>

7.  <span data-ttu-id="a1ad5-120">Accédez à **Démarrer** , puis tapez **cmd** .</span><span class="sxs-lookup"><span data-stu-id="a1ad5-120">Go to **Start** and type **cmd** .</span></span>

8.  <span data-ttu-id="a1ad5-121">Cliquez avec le bouton droit sur **invite de commandes** et sélectionnez **exécuter en tant qu’administrateur** .</span><span class="sxs-lookup"><span data-stu-id="a1ad5-121">Right-click **Command prompt** and select **Run as administrator** .</span></span>

![Menu Démarrer de la fenêtre pointant sur Exécuter en tant qu’administrateur](../media/dlp-run-as-admin.png)

9.  <span data-ttu-id="a1ad5-123">Tapez l’emplacement du fichier de script.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-123">Type the location of the script file.</span></span> <span data-ttu-id="a1ad5-124">Si vous avez copié le fichier sur le bureau, tapez : *%UserProfile%\Desktop\WindowsDefenderATPOnboardingScript.cmd*</span><span class="sxs-lookup"><span data-stu-id="a1ad5-124">If you copied the file to the desktop, type: *%userprofile%\Desktop\WindowsDefenderATPOnboardingScript.cmd*</span></span>

10.  <span data-ttu-id="a1ad5-125">Appuyez sur la touche **entrée** ou cliquez sur **OK** .</span><span class="sxs-lookup"><span data-stu-id="a1ad5-125">Press the **Enter** key or click **OK** .</span></span>

<span data-ttu-id="a1ad5-126">Pour plus d’informations sur la façon dont vous pouvez valider manuellement le fait que l’appareil soit conforme et signale correctement les données de capteur, reportez-vous à la rubrique [Troubleshoot Microsoft Defender Advanced Threat Protection Onboard Problems](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding).</span><span class="sxs-lookup"><span data-stu-id="a1ad5-126">For information on how you can manually validate that the device is compliant and correctly reports sensor data see, [Troubleshoot Microsoft Defender Advanced Threat Protection onboarding issues](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding).</span></span>

## <a name="offboard-devices-using-a-local-script"></a><span data-ttu-id="a1ad5-127">Appareils débarquement à l’aide d’un script local</span><span class="sxs-lookup"><span data-stu-id="a1ad5-127">Offboard devices using a local script</span></span>
<span data-ttu-id="a1ad5-128">Pour des raisons de sécurité, le package utilisé pour les appareils débarquement expire 30 jours après la date de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-128">For security reasons, the package used to Offboard devices will expire 30 days after the date it was downloaded.</span></span> <span data-ttu-id="a1ad5-129">Les packages par débarquement expirés envoyés à un périphérique seront rejetés.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-129">Expired offboarding packages sent to an device will be rejected.</span></span> <span data-ttu-id="a1ad5-130">Lors du téléchargement d’un package par débarquement, vous êtes informé de la date d’expiration des packages et il est également inclus dans le nom du package.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-130">When downloading an offboarding package you will be notified of the packages expiry date and it will also be included in the package name.</span></span>

> [!NOTE]
> <span data-ttu-id="a1ad5-131">Les stratégies d’intégration et de par débarquement ne doivent pas être déployées sur le même appareil simultanément, sinon cette opération entraîne des collisions imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-131">Onboarding and offboarding policies must not be deployed on the same device at the same time, otherwise this will cause unpredictable collisions.</span></span>

1. <span data-ttu-id="a1ad5-132">Obtenir le package par débarquement à partir du [Centre de conformité Microsoft](https://compliance.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="a1ad5-132">Get the offboarding package from [Microsoft Compliance center](https://compliance.microsoft.com)</span></span>

2. <span data-ttu-id="a1ad5-133">Dans le volet de navigation, sélectionnez **paramètres** du  >  **périphérique par débarquement** .</span><span class="sxs-lookup"><span data-stu-id="a1ad5-133">In the navigation pane, select **Settings** > **Device offboarding** .</span></span>

3. <span data-ttu-id="a1ad5-134">Dans le champ **méthode de déploiement** , sélectionnez **script local** .</span><span class="sxs-lookup"><span data-stu-id="a1ad5-134">In the **Deployment method** field, select **Local Script** .</span></span>

4. <span data-ttu-id="a1ad5-135">Cliquez sur **Télécharger le package** et enregistrez le fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-135">Click **Download package** and save the .zip file.</span></span>

5. <span data-ttu-id="a1ad5-136">Extrayez le contenu du fichier. zip vers un emplacement partagé, en lecture seule, accessible aux appareils.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-136">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the devices.</span></span> <span data-ttu-id="a1ad5-137">Vous devez avoir un fichier nommé *DeviceComplianceOffboardingScript_valid_until_YYYY-mm-dd. cmd* .</span><span class="sxs-lookup"><span data-stu-id="a1ad5-137">You should have a file named *DeviceComplianceOffboardingScript_valid_until_YYYY-MM-DD.cmd* .</span></span>

6.  <span data-ttu-id="a1ad5-138">Ouvrez une invite de ligne de commande avec élévation de privilèges sur l’appareil et exécutez le script :</span><span class="sxs-lookup"><span data-stu-id="a1ad5-138">Open an elevated command-line prompt on the device and run the script:</span></span>

7.  <span data-ttu-id="a1ad5-139">Accédez à **Démarrer** , puis tapez **cmd** .</span><span class="sxs-lookup"><span data-stu-id="a1ad5-139">Go to **Start** and type **cmd** .</span></span>

8.  <span data-ttu-id="a1ad5-140">Cliquez avec le bouton droit sur **invite de commandes** et sélectionnez **exécuter en tant qu’administrateur** .</span><span class="sxs-lookup"><span data-stu-id="a1ad5-140">Right-click **Command prompt** and select **Run as administrator** .</span></span>

![Menu Démarrer de la fenêtre pointant sur Exécuter en tant qu’administrateur](../media/dlp-run-as-admin.png)

9.  <span data-ttu-id="a1ad5-142">Tapez l’emplacement du fichier de script.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-142">Type the location of the script file.</span></span> <span data-ttu-id="a1ad5-143">Si vous avez copié le fichier sur le bureau, tapez la commande suivante : *%userprofile%\desktop\ WindowsDefenderATPOffboardingScript_valid_until_YYYY-mm-dd. cmd*</span><span class="sxs-lookup"><span data-stu-id="a1ad5-143">If you copied the file to the desktop, type: *%userprofile%\Desktop\WindowsDefenderATPOffboardingScript_valid_until_YYYY-MM-DD.cmd*</span></span>

10.  <span data-ttu-id="a1ad5-144">Appuyez sur la touche **entrée** ou cliquez sur **OK** .</span><span class="sxs-lookup"><span data-stu-id="a1ad5-144">Press the **Enter** key or click **OK** .</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1ad5-145">Par débarquement entraîne l’arrêt de l’envoi des données de capteur au portail.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-145">Offboarding causes the device to stop sending sensor data to the portal.</span></span>


## <a name="monitor-device-configuration"></a><span data-ttu-id="a1ad5-146">Surveiller la configuration de l’appareil</span><span class="sxs-lookup"><span data-stu-id="a1ad5-146">Monitor device configuration</span></span>
<span data-ttu-id="a1ad5-147">Vous pouvez suivre les différentes étapes de vérification décrites dans la procédure [résolution des problèmes liés à l’intégration] (( https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding) pour vérifier que le script s’est exécuté correctement et que l’agent est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-147">You can follow the different verification steps in the [Troubleshoot onboarding issues]((https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding) to verify that the script completed successfully and the agent is running.</span></span>

<span data-ttu-id="a1ad5-148">La surveillance peut également être réalisée directement sur le portail ou à l’aide des différents outils de déploiement.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-148">Monitoring can also be done directly on the portal, or by using the different deployment tools.</span></span>

### <a name="monitor-devices-using-the-portal"></a><span data-ttu-id="a1ad5-149">Surveiller des périphériques à l’aide du portail</span><span class="sxs-lookup"><span data-stu-id="a1ad5-149">Monitor devices using the portal</span></span>
1. <span data-ttu-id="a1ad5-150">Accédez au [Centre de conformité Microsoft 365](https://compliance.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="a1ad5-150">Go to [Microsoft 365 Compliance center](https://compliance.microsoft.com).</span></span>

2. <span data-ttu-id="a1ad5-151">Choisissez **paramètres** d’intégration de l'  >  **appareil**  >  **Devices** .</span><span class="sxs-lookup"><span data-stu-id="a1ad5-151">Choose **Settings** > **Device onboarding** > **Devices** .</span></span>

3. <span data-ttu-id="a1ad5-152">Vérifiez que les appareils apparaissent.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-152">Verify that devices are appearing.</span></span>


## <a name="related-topics"></a><span data-ttu-id="a1ad5-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1ad5-153">Related topics</span></span>
- [<span data-ttu-id="a1ad5-154">Périphériques Windows 10 embarqués à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="a1ad5-154">Onboard Windows 10 devices using Group Policy</span></span>](dlp-configure-endpoints-gp.md)
- [<span data-ttu-id="a1ad5-155">Appareils intégrés Windows 10 à l’aide du gestionnaire de configuration de point de terminaison Microsoft</span><span class="sxs-lookup"><span data-stu-id="a1ad5-155">Onboard Windows 10 devices using Microsoft Endpoint Configuration Manager</span></span>](dlp-configure-endpoints-sccm.md)
- [<span data-ttu-id="a1ad5-156">Périphériques Windows 10 intégrés à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="a1ad5-156">Onboard Windows 10 devices using Mobile Device Management tools</span></span>](dlp-configure-endpoints-mdm.md)
- [<span data-ttu-id="a1ad5-157">Périphériques VDI (Virtual Desktop Infrastructure) non persistants</span><span class="sxs-lookup"><span data-stu-id="a1ad5-157">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>](dlp-configure-endpoints-vdi.md)
- [<span data-ttu-id="a1ad5-158">Exécution d’un test de détection sur un appareil Microsoft Defender nouvellement intégré</span><span class="sxs-lookup"><span data-stu-id="a1ad5-158">Run a detection test on a newly onboarded Microsoft Defender ATP device</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/run-detection-test)
- [<span data-ttu-id="a1ad5-159">Résoudre les problèmes d’intégration de la protection avancée contre les menaces Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="a1ad5-159">Troubleshoot Microsoft Defender Advanced Threat Protection onboarding issues</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding)
