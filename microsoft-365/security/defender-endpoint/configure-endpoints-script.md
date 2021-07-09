---
title: Intégrer les appareils Windows 10 utilisant un script local
description: Utilisez un script local pour déployer le package de configuration sur les appareils afin d’activer l’intégration des appareils au service.
keywords: configurer des appareils à l’aide d’un script local, la gestion des appareils, configurer Microsoft Defender pour les appareils endpoint
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
ms.openlocfilehash: e15a02753c7a1b346021a4351af24b8fd28315da
ms.sourcegitcommit: 0d1b065c94125b495e9886200f7918de3bda40b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2021
ms.locfileid: "53339645"
---
# <a name="onboard-the-windows-10-devices-using-a-local-script"></a><span data-ttu-id="013f0-104">Intégrer les appareils Windows 10 à l’aide d’un script local</span><span class="sxs-lookup"><span data-stu-id="013f0-104">Onboard the Windows 10 devices using a local script</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

- [<span data-ttu-id="013f0-105">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="013f0-105">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


><span data-ttu-id="013f0-106">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="013f0-106">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="013f0-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="013f0-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-configureendpointsscript-abovefoldlink)

<span data-ttu-id="013f0-108">Vous pouvez également intégrer manuellement des appareils individuels à Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="013f0-108">You can also manually onboard individual devices to Defender for Endpoint.</span></span> <span data-ttu-id="013f0-109">Vous pouvez d’abord le faire lors du test du service avant de vous engager à intégrer tous les appareils de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="013f0-109">You might want to do this first when testing the service before you commit to onboarding all devices in your network.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="013f0-110">Ce script a été optimisé pour une utilisation sur jusqu’à 10 appareils.</span><span class="sxs-lookup"><span data-stu-id="013f0-110">This script has been optimized for use on up to 10 devices.</span></span>
>
> <span data-ttu-id="013f0-111">Pour déployer à grande échelle, utilisez [d’autres options de déploiement.](configure-endpoints.md)</span><span class="sxs-lookup"><span data-stu-id="013f0-111">To deploy at scale, use [other deployment options](configure-endpoints.md).</span></span> <span data-ttu-id="013f0-112">Par exemple, vous pouvez déployer un script d’intégration sur plus de 10 appareils en production avec le script disponible dans les appareils Windows 10 intégrés à l’aide de la stratégie [de groupe.](configure-endpoints-gp.md)</span><span class="sxs-lookup"><span data-stu-id="013f0-112">For example, you can deploy an onboarding script to more than 10 devices in production with the script available in [Onboard Windows 10 devices using Group Policy](configure-endpoints-gp.md).</span></span>

## <a name="onboard-devices"></a><span data-ttu-id="013f0-113">Intégration des appareils</span><span class="sxs-lookup"><span data-stu-id="013f0-113">Onboard devices</span></span> 

<span data-ttu-id="013f0-114">[![Image du PDF montrant les différents chemins de déploiement](images/onboard-script.png)](images/onboard-script.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="013f0-114">[![Image of the PDF showing the various deployment paths](images/onboard-script.png)](images/onboard-script.png#lightbox)</span></span>


<span data-ttu-id="013f0-115">Consultez le [fichier PDF](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf) [ou Visio](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.vsdx) pour voir les différents chemins d’accès dans le déploiement de Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="013f0-115">Check out the [PDF](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf)  or  [Visio](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.vsdx) to see the various paths in deploying Defender for Endpoint.</span></span> 


1.  <span data-ttu-id="013f0-116">Ouvrez le fichier de package de configuration de .zip de groupe (*WindowsDefenderATPOnboardingPackage.zip*) que vous avez téléchargé à partir de l’Assistant d’intégration de service.</span><span class="sxs-lookup"><span data-stu-id="013f0-116">Open the GP configuration package .zip file (*WindowsDefenderATPOnboardingPackage.zip*) that you downloaded from the service onboarding wizard.</span></span> <span data-ttu-id="013f0-117">Vous pouvez également obtenir le package à partir [du portail Microsoft 365 Defender](https://security.microsoft.com/):</span><span class="sxs-lookup"><span data-stu-id="013f0-117">You can also get the package from [Microsoft 365  Defender portal](https://security.microsoft.com/):</span></span>

    1. <span data-ttu-id="013f0-118">Dans le volet de navigation, sélectionnez **Paramètres**  >  **Endpoints**  >  **Device Management**  >  **Onboarding**.</span><span class="sxs-lookup"><span data-stu-id="013f0-118">In the navigation pane, select **Settings** > **Endpoints** > **Device management** > **Onboarding**.</span></span>

    1. <span data-ttu-id="013f0-119">Sélectionnez Windows 10 comme système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="013f0-119">Select Windows 10 as the operating system.</span></span>

    1. <span data-ttu-id="013f0-120">Dans le **champ Méthode de** déploiement, sélectionnez Script **local.**</span><span class="sxs-lookup"><span data-stu-id="013f0-120">In the **Deployment method** field, select **Local Script**.</span></span>

    1. <span data-ttu-id="013f0-121">Cliquez **sur Télécharger le package** et enregistrez .zip fichier.</span><span class="sxs-lookup"><span data-stu-id="013f0-121">Click **Download package** and save the .zip file.</span></span>

  
2.  <span data-ttu-id="013f0-122">Extrayez le contenu du package de configuration vers un emplacement sur l’appareil que vous souhaitez intégrer (par exemple, le Bureau).</span><span class="sxs-lookup"><span data-stu-id="013f0-122">Extract the contents of the configuration package to a location on the device you want to onboard (for example, the Desktop).</span></span> <span data-ttu-id="013f0-123">Vous devez avoir un fichier nommé *WindowsDefenderATPLocalOnboardingScript.cmd*.</span><span class="sxs-lookup"><span data-stu-id="013f0-123">You should have a file named *WindowsDefenderATPLocalOnboardingScript.cmd*.</span></span>

3.  <span data-ttu-id="013f0-124">Ouvrez une invite de ligne de commande avec élévation de niveaux sur l’appareil et exécutez le script :</span><span class="sxs-lookup"><span data-stu-id="013f0-124">Open an elevated command-line prompt on the device and run the script:</span></span>

    1.  <span data-ttu-id="013f0-125">Accéder à **Démarrer** et taper **cmd**.</span><span class="sxs-lookup"><span data-stu-id="013f0-125">Go to **Start** and type **cmd**.</span></span>

    1.  <span data-ttu-id="013f0-126">Cliquez avec le bouton droit sur **Invite de commandes** et sélectionnez **Exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="013f0-126">Right-click **Command prompt** and select **Run as administrator**.</span></span>

        ![Fenêtre menu Démarrer pointant sur Exécuter en tant qu’administrateur](images/run-as-admin.png)

4.  <span data-ttu-id="013f0-128">Tapez l’emplacement du fichier de script.</span><span class="sxs-lookup"><span data-stu-id="013f0-128">Type the location of the script file.</span></span> <span data-ttu-id="013f0-129">Si vous avez copié le fichier sur le Bureau, tapez : *%userprofile%\Desktop\WindowsDefenderATPLocalOnboardingScript.cmd*</span><span class="sxs-lookup"><span data-stu-id="013f0-129">If you copied the file to the desktop, type: *%userprofile%\Desktop\WindowsDefenderATPLocalOnboardingScript.cmd*</span></span>

5.  <span data-ttu-id="013f0-130">Appuyez sur **entrée** ou cliquez sur **OK.**</span><span class="sxs-lookup"><span data-stu-id="013f0-130">Press the **Enter** key or click **OK**.</span></span>

<span data-ttu-id="013f0-131">Pour plus d’informations sur la façon dont vous pouvez vérifier manuellement que l’appareil est conforme et signale correctement les données du capteur, consultez La procédure de résolution des problèmes d’intégration de Microsoft Defender pour les points [de terminaison.](troubleshoot-onboarding.md)</span><span class="sxs-lookup"><span data-stu-id="013f0-131">For information on how you can manually validate that the device is compliant and correctly reports sensor data see, [Troubleshoot Microsoft Defender for Endpoint onboarding issues](troubleshoot-onboarding.md).</span></span>


>[!TIP]
> <span data-ttu-id="013f0-132">Après avoir intégré l’appareil, vous pouvez choisir d’exécuter un test de détection pour vérifier qu’un appareil est correctement intégré au service.</span><span class="sxs-lookup"><span data-stu-id="013f0-132">After onboarding the device, you can choose to run a detection test to verify that an device is properly onboarded to the service.</span></span> <span data-ttu-id="013f0-133">Pour plus d’informations, voir Exécuter un test de détection sur un point de terminaison [Microsoft Defender pour point de terminaison nouvellement intégré.](run-detection-test.md)</span><span class="sxs-lookup"><span data-stu-id="013f0-133">For more information, see [Run a detection test on a newly onboarded Microsoft Defender for Endpoint endpoint](run-detection-test.md).</span></span>

## <a name="configure-sample-collection-settings"></a><span data-ttu-id="013f0-134">Configurer des paramètres de collection d’exemples</span><span class="sxs-lookup"><span data-stu-id="013f0-134">Configure sample collection settings</span></span>
<span data-ttu-id="013f0-135">Pour chaque appareil, vous pouvez définir une valeur de configuration pour déterminer si des échantillons peuvent être collectés à partir de l’appareil lorsqu’une demande est faite via Microsoft 365 Defender pour soumettre un fichier pour analyse approfondie.</span><span class="sxs-lookup"><span data-stu-id="013f0-135">For each device, you can set a configuration value to state whether samples can be collected from the device when a request is made through Microsoft 365 Defender to submit a file for deep analysis.</span></span>

<span data-ttu-id="013f0-136">Vous pouvez configurer manuellement le paramètre de partage d’exemples sur l’appareil à l’aide de *regedit* ou en créant et en exécutant *un fichier .reg.*</span><span class="sxs-lookup"><span data-stu-id="013f0-136">You can manually configure the sample sharing setting on the device by using *regedit* or creating and running a *.reg* file.</span></span>  

<span data-ttu-id="013f0-137">La configuration est définie par le biais de l’entrée de clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="013f0-137">The configuration is set through the following registry key entry:</span></span>

```console
Path: “HKLM\SOFTWARE\Policies\Microsoft\Windows Advanced Threat Protection”
Name: "AllowSampleCollection"
Value: 0 or 1
```
<span data-ttu-id="013f0-138">Où :</span><span class="sxs-lookup"><span data-stu-id="013f0-138">Where:</span></span><br>
<span data-ttu-id="013f0-139">Le type de nom est D-WORD.</span><span class="sxs-lookup"><span data-stu-id="013f0-139">Name type is a D-WORD.</span></span> <br>
<span data-ttu-id="013f0-140">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="013f0-140">Possible values are:</span></span>
- <span data-ttu-id="013f0-141">0 : n’autorise pas le partage d’exemples à partir de cet appareil</span><span class="sxs-lookup"><span data-stu-id="013f0-141">0 - doesn't allow sample sharing  from this device</span></span>
- <span data-ttu-id="013f0-142">1 : autorise le partage de tous les types de fichiers à partir de cet appareil</span><span class="sxs-lookup"><span data-stu-id="013f0-142">1 - allows sharing of all file types from this device</span></span>

<span data-ttu-id="013f0-143">La valeur par défaut au cas où la clé de Registre n’existe pas est 1.</span><span class="sxs-lookup"><span data-stu-id="013f0-143">The default value in case the registry key doesn’t exist is 1.</span></span>


## <a name="offboard-devices-using-a-local-script"></a><span data-ttu-id="013f0-144">Hors-carte des appareils à l’aide d’un script local</span><span class="sxs-lookup"><span data-stu-id="013f0-144">Offboard devices using a local script</span></span>
<span data-ttu-id="013f0-145">Pour des raisons de sécurité, le package utilisé pour la sortie des appareils expirera 30 jours après la date de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="013f0-145">For security reasons, the package used to Offboard devices will expire 30 days after the date it was downloaded.</span></span> <span data-ttu-id="013f0-146">Les packages de offboarding expirés envoyés à un appareil seront rejetés.</span><span class="sxs-lookup"><span data-stu-id="013f0-146">Expired offboarding packages sent to an device will be rejected.</span></span> <span data-ttu-id="013f0-147">Lorsque vous téléchargez un package de déclassage, vous êtes informé de la date d’expiration des packages et il est également inclus dans le nom du package.</span><span class="sxs-lookup"><span data-stu-id="013f0-147">When downloading an offboarding package you will be notified of the packages expiry date and it will also be included in the package name.</span></span>

> [!NOTE]
> <span data-ttu-id="013f0-148">Les stratégies d’intégration et deboarding ne doivent pas être déployées sur le même appareil en même temps, sinon cela provoquera des collisions imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="013f0-148">Onboarding and offboarding policies must not be deployed on the same device at the same time, otherwise this will cause unpredictable collisions.</span></span>

1. <span data-ttu-id="013f0-149">Obtenez le package deboarding à partir [Microsoft 365 Defender portail :](https://security.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="013f0-149">Get the offboarding package from [Microsoft 365 Defender portal](https://security.microsoft.com/):</span></span>

    1. <span data-ttu-id="013f0-150">Dans le volet de navigation, sélectionnez **le Paramètres** de gestion des appareils  >  **endpoints.**  >    > </span><span class="sxs-lookup"><span data-stu-id="013f0-150">In the navigation pane, select **Settings** > **Endpoints** > **Device management** >**Offboarding**.</span></span>

    1. <span data-ttu-id="013f0-151">Sélectionnez Windows 10 comme système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="013f0-151">Select Windows 10 as the operating system.</span></span>

    1. <span data-ttu-id="013f0-152">Dans le **champ Méthode de** déploiement, sélectionnez Script **local.**</span><span class="sxs-lookup"><span data-stu-id="013f0-152">In the **Deployment method** field, select **Local Script**.</span></span>

    1. <span data-ttu-id="013f0-153">Cliquez **sur Télécharger le package** et enregistrez .zip fichier.</span><span class="sxs-lookup"><span data-stu-id="013f0-153">Click **Download package** and save the .zip file.</span></span>

2. <span data-ttu-id="013f0-154">Extrayez le contenu du .zip vers un emplacement partagé en lecture seule accessible par les appareils.</span><span class="sxs-lookup"><span data-stu-id="013f0-154">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the devices.</span></span> <span data-ttu-id="013f0-155">Vous devez avoir un fichier nommé *WindowsDefenderATPOffboardingScript_valid_until_YYYY-MM-DD.cmd*.</span><span class="sxs-lookup"><span data-stu-id="013f0-155">You should have a file named *WindowsDefenderATPOffboardingScript_valid_until_YYYY-MM-DD.cmd*.</span></span>

3.  <span data-ttu-id="013f0-156">Ouvrez une invite de ligne de commande avec élévation de niveaux sur l’appareil et exécutez le script :</span><span class="sxs-lookup"><span data-stu-id="013f0-156">Open an elevated command-line prompt on the device and run the script:</span></span>

    1.  <span data-ttu-id="013f0-157">Accéder à **Démarrer** et taper **cmd**.</span><span class="sxs-lookup"><span data-stu-id="013f0-157">Go to **Start** and type **cmd**.</span></span>

    1.  <span data-ttu-id="013f0-158">Cliquez avec le bouton droit sur **Invite de commandes** et sélectionnez **Exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="013f0-158">Right-click **Command prompt** and select **Run as administrator**.</span></span>

        ![Fenêtre menu Démarrer pointant sur Exécuter en tant qu’administrateur](images/run-as-admin.png)

4.  <span data-ttu-id="013f0-160">Tapez l’emplacement du fichier de script.</span><span class="sxs-lookup"><span data-stu-id="013f0-160">Type the location of the script file.</span></span> <span data-ttu-id="013f0-161">Si vous avez copié le fichier sur le Bureau, tapez : *%userprofile%\Desktop\WindowsDefenderATPOffboardingScript_valid_until_YYYY-MM-DD.cmd*</span><span class="sxs-lookup"><span data-stu-id="013f0-161">If you copied the file to the desktop, type: *%userprofile%\Desktop\WindowsDefenderATPOffboardingScript_valid_until_YYYY-MM-DD.cmd*</span></span>

5.  <span data-ttu-id="013f0-162">Appuyez sur **entrée** ou cliquez sur **OK.**</span><span class="sxs-lookup"><span data-stu-id="013f0-162">Press the **Enter** key or click **OK**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="013f0-163">Laboarding empêche l’appareil d’envoyer des données de capteur au portail, mais les données de l’appareil, y compris la référence aux alertes qu’il a eues, seront conservées pendant 6 mois.</span><span class="sxs-lookup"><span data-stu-id="013f0-163">Offboarding causes the device to stop sending sensor data to the portal but data from the device, including reference to any alerts it has had will be retained for up to 6 months.</span></span>


## <a name="monitor-device-configuration"></a><span data-ttu-id="013f0-164">Surveiller la configuration de l’appareil</span><span class="sxs-lookup"><span data-stu-id="013f0-164">Monitor device configuration</span></span>
<span data-ttu-id="013f0-165">Vous pouvez suivre les différentes [](troubleshoot-onboarding.md) étapes de vérification dans la résolution des problèmes d’intégration pour vérifier que le script s’est correctement terminé et que l’agent est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="013f0-165">You can follow the different verification steps in the [Troubleshoot onboarding issues](troubleshoot-onboarding.md) to verify that the script completed successfully and the agent is running.</span></span>

<span data-ttu-id="013f0-166">La surveillance peut également être effectuée directement sur le portail ou à l’aide des différents outils de déploiement.</span><span class="sxs-lookup"><span data-stu-id="013f0-166">Monitoring can also be done directly on the portal, or by using the different deployment tools.</span></span>

### <a name="monitor-devices-using-the-portal"></a><span data-ttu-id="013f0-167">Surveiller les appareils à l’aide du portail</span><span class="sxs-lookup"><span data-stu-id="013f0-167">Monitor devices using the portal</span></span>
1. <span data-ttu-id="013f0-168">Go to Microsoft 365 Defender portal.</span><span class="sxs-lookup"><span data-stu-id="013f0-168">Go to Microsoft 365 Defender portal.</span></span>

2. <span data-ttu-id="013f0-169">Cliquez sur **Inventaire des appareils.**</span><span class="sxs-lookup"><span data-stu-id="013f0-169">Click **Devices inventory**.</span></span>

3. <span data-ttu-id="013f0-170">Vérifiez que les appareils apparaissent.</span><span class="sxs-lookup"><span data-stu-id="013f0-170">Verify that devices are appearing.</span></span>


## <a name="related-topics"></a><span data-ttu-id="013f0-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="013f0-171">Related topics</span></span>
- [<span data-ttu-id="013f0-172">Intégrer des Windows 10 à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="013f0-172">Onboard Windows 10 devices using Group Policy</span></span>](configure-endpoints-gp.md)
- [<span data-ttu-id="013f0-173">Intégrer Windows 10 appareils à l’aide Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="013f0-173">Onboard Windows 10 devices using Microsoft Endpoint Configuration Manager</span></span>](configure-endpoints-sccm.md)
- [<span data-ttu-id="013f0-174">Intégrer les appareils Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="013f0-174">Onboard Windows 10 devices using Mobile Device Management tools</span></span>](configure-endpoints-mdm.md)
- [<span data-ttu-id="013f0-175">Intégrer les ordinateurs virtuels d’infrastructure de bureau (VDI) non persistants</span><span class="sxs-lookup"><span data-stu-id="013f0-175">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>](configure-endpoints-vdi.md)
- [<span data-ttu-id="013f0-176">Exécuter un test de détection sur un appareil Microsoft Defender pour point de terminaison nouvellement intégré</span><span class="sxs-lookup"><span data-stu-id="013f0-176">Run a detection test on a newly onboarded Microsoft Defender for Endpoint device</span></span>](run-detection-test.md)
- [<span data-ttu-id="013f0-177">Résoudre les problèmes d’intégration de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="013f0-177">Troubleshoot Microsoft Defender for Endpoint onboarding issues</span></span>](troubleshoot-onboarding.md)
