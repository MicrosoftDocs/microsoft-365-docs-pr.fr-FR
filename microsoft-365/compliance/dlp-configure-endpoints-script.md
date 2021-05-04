---
title: Intégrer les appareils Windows 10 utilisant un script local
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
description: Utilisez un script local pour déployer le package de configuration sur les appareils afin qu'ils soient intégrés au service.
ms.openlocfilehash: e9efa76af72f9169bdec1acf35d72066ac0a776e
ms.sourcegitcommit: 55791ddab9ae484f76b30f0470eec8a4cf7b46d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51893305"
---
# <a name="onboard-windows-10-devices-using-a-local-script"></a><span data-ttu-id="e52a7-103">Intégrer les appareils Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="e52a7-103">Onboard Windows 10 devices using a local script</span></span>

<span data-ttu-id="e52a7-104">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e52a7-104">**Applies to:**</span></span>

- [<span data-ttu-id="e52a7-105">Microsoft 365 Protection contre la perte de données (DLP) de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e52a7-105">Microsoft 365 Endpoint data loss prevention (DLP)</span></span>](./endpoint-dlp-learn-about.md)

<span data-ttu-id="e52a7-106">Vous pouvez également intégrer manuellement des appareils individuels pour Microsoft 365 protection contre la perte de données de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="e52a7-106">You can also manually onboard individual devices to Microsoft 365 Endpoint data loss prevention.</span></span> <span data-ttu-id="e52a7-107">Vous pouvez d'abord le faire lors du test du service avant de vous engager à intégrer tous les appareils de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="e52a7-107">You might want to do this first when testing the service before you commit to onboarding all devices in your network.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e52a7-108">Ce script a été optimisé pour une utilisation sur jusqu'à 10 appareils.</span><span class="sxs-lookup"><span data-stu-id="e52a7-108">This script has been optimized for use on up to 10 devices.</span></span>
>
> <span data-ttu-id="e52a7-109">Pour déployer à grande échelle, utilisez [d'autres options de déploiement.](dlp-configure-endpoints.md)</span><span class="sxs-lookup"><span data-stu-id="e52a7-109">To deploy at scale, use [other deployment options](dlp-configure-endpoints.md).</span></span> <span data-ttu-id="e52a7-110">Par exemple, vous pouvez déployer un script d'intégration sur plus de 10 appareils en production avec le script disponible dans les appareils Windows 10 intégrés à l'aide de la stratégie [de groupe.](dlp-configure-endpoints-gp.md)</span><span class="sxs-lookup"><span data-stu-id="e52a7-110">For example, you can deploy an onboarding script to more than 10 devices in production with the script available in [Onboard Windows 10 devices using Group Policy](dlp-configure-endpoints-gp.md).</span></span>

## <a name="onboard-devices"></a><span data-ttu-id="e52a7-111">Intégration des appareils</span><span class="sxs-lookup"><span data-stu-id="e52a7-111">Onboard devices</span></span>
 
1.  <span data-ttu-id="e52a7-112">Ouvrez le fichier de package de configuration de .zip de groupe (*DeviceComplianceOnboardingPackage.zip*) que vous avez téléchargé à partir de l'Assistant d'intégration de service.</span><span class="sxs-lookup"><span data-stu-id="e52a7-112">Open the GP configuration package .zip file (*DeviceComplianceOnboardingPackage.zip*) that you downloaded from the service onboarding wizard.</span></span> <span data-ttu-id="e52a7-113">Vous pouvez également obtenir le package à partir du [Centre de conformité Microsoft](https://compliance.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="e52a7-113">You can also get the package from [Microsoft Compliance center](https://compliance.microsoft.com)</span></span>

2. <span data-ttu-id="e52a7-114">Dans le volet de navigation, sélectionnez  >  **Paramètres'intégration de l'appareil.**</span><span class="sxs-lookup"><span data-stu-id="e52a7-114">In the navigation pane, select **Settings** > **Device onboarding**.</span></span>

3. <span data-ttu-id="e52a7-115">Dans le **champ Méthode de** déploiement, sélectionnez Script **local.**</span><span class="sxs-lookup"><span data-stu-id="e52a7-115">In the **Deployment method** field, select **Local Script**.</span></span>

4. <span data-ttu-id="e52a7-116">Cliquez **sur Télécharger le package** et enregistrez .zip fichier.</span><span class="sxs-lookup"><span data-stu-id="e52a7-116">Click **Download package** and save the .zip file.</span></span>
  
5. <span data-ttu-id="e52a7-117">Extrayez le contenu du package de configuration vers un emplacement sur l'appareil que vous souhaitez intégrer (par exemple, le Bureau).</span><span class="sxs-lookup"><span data-stu-id="e52a7-117">Extract the contents of the configuration package to a location on the device you want to onboard (for example, the Desktop).</span></span> <span data-ttu-id="e52a7-118">Vous devez avoir un fichier nommé *DeviceOnboardingScript.cmd*.</span><span class="sxs-lookup"><span data-stu-id="e52a7-118">You should have a file named *DeviceOnboardingScript.cmd*.</span></span>

6.  <span data-ttu-id="e52a7-119">Ouvrez une invite de ligne de commande avec élévation de niveaux sur l'appareil et exécutez le script :</span><span class="sxs-lookup"><span data-stu-id="e52a7-119">Open an elevated command-line prompt on the device and run the script:</span></span>

7.  <span data-ttu-id="e52a7-120">Accéder à **Démarrer** et taper **cmd**.</span><span class="sxs-lookup"><span data-stu-id="e52a7-120">Go to **Start** and type **cmd**.</span></span>

8.  <span data-ttu-id="e52a7-121">Cliquez avec le bouton droit sur **Invite de commandes** et sélectionnez **Exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="e52a7-121">Right-click **Command prompt** and select **Run as administrator**.</span></span>

    ![Menu Démarrer de la fenêtre pointant sur Exécuter en tant qu'administrateur](../media/dlp-run-as-admin.png)

9.  <span data-ttu-id="e52a7-123">Tapez l'emplacement du fichier de script.</span><span class="sxs-lookup"><span data-stu-id="e52a7-123">Type the location of the script file.</span></span> <span data-ttu-id="e52a7-124">Si vous avez copié le fichier sur le Bureau, tapez : *%userprofile%\Desktop\WindowsDefenderATPOnboardingScript.cmd*</span><span class="sxs-lookup"><span data-stu-id="e52a7-124">If you copied the file to the desktop, type: *%userprofile%\Desktop\WindowsDefenderATPOnboardingScript.cmd*</span></span>

10.  <span data-ttu-id="e52a7-125">Appuyez sur **entrée** ou cliquez sur **OK.**</span><span class="sxs-lookup"><span data-stu-id="e52a7-125">Press the **Enter** key or click **OK**.</span></span>

<span data-ttu-id="e52a7-126">Pour plus d'informations sur la façon dont vous pouvez vérifier manuellement que l'appareil est conforme et signale correctement les données du capteur, consultez la Microsoft Defender Advanced Threat Protection problèmes [d'intégration.](/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding)</span><span class="sxs-lookup"><span data-stu-id="e52a7-126">For information on how you can manually validate that the device is compliant and correctly reports sensor data see, [Troubleshoot Microsoft Defender Advanced Threat Protection onboarding issues](/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding).</span></span>

## <a name="offboard-devices-using-a-local-script"></a><span data-ttu-id="e52a7-127">Hors-carte des appareils à l'aide d'un script local</span><span class="sxs-lookup"><span data-stu-id="e52a7-127">Offboard devices using a local script</span></span>
<span data-ttu-id="e52a7-128">Pour des raisons de sécurité, le package utilisé pour la sortie des appareils expirera 30 jours après la date de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="e52a7-128">For security reasons, the package used to Offboard devices will expire 30 days after the date it was downloaded.</span></span> <span data-ttu-id="e52a7-129">Les packages de offboarding expirés envoyés à un appareil seront rejetés.</span><span class="sxs-lookup"><span data-stu-id="e52a7-129">Expired offboarding packages sent to an device will be rejected.</span></span> <span data-ttu-id="e52a7-130">Lorsque vous téléchargez un package de déclassage, vous êtes informé de la date d'expiration des packages et il est également inclus dans le nom du package.</span><span class="sxs-lookup"><span data-stu-id="e52a7-130">When downloading an offboarding package you will be notified of the packages expiry date and it will also be included in the package name.</span></span>

> [!NOTE]
> <span data-ttu-id="e52a7-131">Les stratégies d'intégration et deboarding ne doivent pas être déployées sur le même appareil en même temps, sinon cela provoquera des collisions imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="e52a7-131">Onboarding and offboarding policies must not be deployed on the same device at the same time, otherwise this will cause unpredictable collisions.</span></span>

1. <span data-ttu-id="e52a7-132">Obtenir le package deboarding à partir du [Centre de conformité Microsoft](https://compliance.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="e52a7-132">Get the offboarding package from [Microsoft Compliance center](https://compliance.microsoft.com)</span></span>

2. <span data-ttu-id="e52a7-133">Dans le volet de navigation, sélectionnez **Paramètres**  >  **de l'appareil.**</span><span class="sxs-lookup"><span data-stu-id="e52a7-133">In the navigation pane, select **Settings** > **Device offboarding**.</span></span>

3. <span data-ttu-id="e52a7-134">Dans le **champ Méthode de** déploiement, sélectionnez Script **local.**</span><span class="sxs-lookup"><span data-stu-id="e52a7-134">In the **Deployment method** field, select **Local Script**.</span></span>

4. <span data-ttu-id="e52a7-135">Cliquez **sur Télécharger le package** et enregistrez .zip fichier.</span><span class="sxs-lookup"><span data-stu-id="e52a7-135">Click **Download package** and save the .zip file.</span></span>

5. <span data-ttu-id="e52a7-136">Extrayez le contenu du .zip vers un emplacement partagé en lecture seule accessible par les appareils.</span><span class="sxs-lookup"><span data-stu-id="e52a7-136">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the devices.</span></span> <span data-ttu-id="e52a7-137">Vous devez avoir un fichier nommé *DeviceComplianceOffboardingScript_valid_until_YYYY-MM-DD.cmd*.</span><span class="sxs-lookup"><span data-stu-id="e52a7-137">You should have a file named *DeviceComplianceOffboardingScript_valid_until_YYYY-MM-DD.cmd*.</span></span>

6.  <span data-ttu-id="e52a7-138">Ouvrez une invite de ligne de commande avec élévation de niveaux sur l'appareil et exécutez le script :</span><span class="sxs-lookup"><span data-stu-id="e52a7-138">Open an elevated command-line prompt on the device and run the script:</span></span>

7.  <span data-ttu-id="e52a7-139">Accéder à **Démarrer** et taper **cmd**.</span><span class="sxs-lookup"><span data-stu-id="e52a7-139">Go to **Start** and type **cmd**.</span></span>

8.  <span data-ttu-id="e52a7-140">Cliquez avec le bouton droit sur **Invite de commandes** et sélectionnez **Exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="e52a7-140">Right-click **Command prompt** and select **Run as administrator**.</span></span>

    ![Menu Démarrer de la fenêtre pointant sur Exécuter en tant qu'administrateur](../media/dlp-run-as-admin.png)

9.  <span data-ttu-id="e52a7-142">Tapez l'emplacement du fichier de script.</span><span class="sxs-lookup"><span data-stu-id="e52a7-142">Type the location of the script file.</span></span> <span data-ttu-id="e52a7-143">Si vous avez copié le fichier sur le Bureau, tapez : *%userprofile%\Desktop\WindowsDefenderATPOffboardingScript_valid_until_YYYY-MM-DD.cmd*</span><span class="sxs-lookup"><span data-stu-id="e52a7-143">If you copied the file to the desktop, type: *%userprofile%\Desktop\WindowsDefenderATPOffboardingScript_valid_until_YYYY-MM-DD.cmd*</span></span>

10.  <span data-ttu-id="e52a7-144">Appuyez sur **entrée** ou cliquez sur **OK.**</span><span class="sxs-lookup"><span data-stu-id="e52a7-144">Press the **Enter** key or click **OK**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e52a7-145">Le fait d'arrêter l'envoi de données de capteur au portail par le fait que l'appareil n'est plus à l'origine de laboardage.</span><span class="sxs-lookup"><span data-stu-id="e52a7-145">Offboarding causes the device to stop sending sensor data to the portal.</span></span>


## <a name="monitor-device-configuration"></a><span data-ttu-id="e52a7-146">Surveiller la configuration de l'appareil</span><span class="sxs-lookup"><span data-stu-id="e52a7-146">Monitor device configuration</span></span>
<span data-ttu-id="e52a7-147">Vous pouvez suivre les différentes étapes de vérification dans [Résoudre les problèmes d'intégration](( pour vérifier que le script s'est correctement terminé et que https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding) l'agent est en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="e52a7-147">You can follow the different verification steps in the [Troubleshoot onboarding issues]((https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding) to verify that the script completed successfully and the agent is running.</span></span>

<span data-ttu-id="e52a7-148">La surveillance peut également être effectuée directement sur le portail ou à l'aide des différents outils de déploiement.</span><span class="sxs-lookup"><span data-stu-id="e52a7-148">Monitoring can also be done directly on the portal, or by using the different deployment tools.</span></span>

### <a name="monitor-devices-using-the-portal"></a><span data-ttu-id="e52a7-149">Surveiller les appareils à l'aide du portail</span><span class="sxs-lookup"><span data-stu-id="e52a7-149">Monitor devices using the portal</span></span>
1. <span data-ttu-id="e52a7-150">Go to [Microsoft 365 Compliance center](https://compliance.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="e52a7-150">Go to [Microsoft 365 Compliance center](https://compliance.microsoft.com).</span></span>

2. <span data-ttu-id="e52a7-151">Choose **Paramètres**  >  **Device onboarding**  >  **Devices**.</span><span class="sxs-lookup"><span data-stu-id="e52a7-151">Choose **Settings** > **Device onboarding** > **Devices**.</span></span>

3. <span data-ttu-id="e52a7-152">Vérifiez que les appareils apparaissent.</span><span class="sxs-lookup"><span data-stu-id="e52a7-152">Verify that devices are appearing.</span></span>


## <a name="related-topics"></a><span data-ttu-id="e52a7-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e52a7-153">Related topics</span></span>
- [<span data-ttu-id="e52a7-154">Intégrer des Windows 10 à l'aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e52a7-154">Onboard Windows 10 devices using Group Policy</span></span>](dlp-configure-endpoints-gp.md)
- [<span data-ttu-id="e52a7-155">Intégrer Windows 10 appareils à l'aide Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="e52a7-155">Onboard Windows 10 devices using Microsoft Endpoint Configuration Manager</span></span>](dlp-configure-endpoints-sccm.md)
- [<span data-ttu-id="e52a7-156">Intégrer les appareils Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="e52a7-156">Onboard Windows 10 devices using Mobile Device Management tools</span></span>](dlp-configure-endpoints-mdm.md)
- [<span data-ttu-id="e52a7-157">Intégrer les ordinateurs virtuels d’infrastructure de bureau (VDI) non persistants</span><span class="sxs-lookup"><span data-stu-id="e52a7-157">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>](dlp-configure-endpoints-vdi.md)
- [<span data-ttu-id="e52a7-158">Exécuter un test de détection sur un appareil Microsoft Defender pour point de terminaison nouvellement intégré</span><span class="sxs-lookup"><span data-stu-id="e52a7-158">Run a detection test on a newly onboarded Microsoft Defender for Endpoint device</span></span>](/windows/security/threat-protection/microsoft-defender-atp/run-detection-test)
- [<span data-ttu-id="e52a7-159">Résoudre les problèmes Microsoft Defender Advanced Threat Protection'intégration</span><span class="sxs-lookup"><span data-stu-id="e52a7-159">Troubleshoot Microsoft Defender Advanced Threat Protection onboarding issues</span></span>](/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding)