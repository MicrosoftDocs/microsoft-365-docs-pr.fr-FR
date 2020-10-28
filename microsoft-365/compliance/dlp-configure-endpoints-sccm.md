---
title: Périphériques Windows 10 embarqués à l’aide du gestionnaire de configuration
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
description: Utilisez le gestionnaire de configuration pour déployer le package de configuration sur les appareils afin qu’ils soient intégrés au service.
ms.openlocfilehash: ea1b0cba10dc3e7120192e0c0ee87e2e354f1cc2
ms.sourcegitcommit: 6647055154002c7d3b8f7ce25ad53c9636bc8066
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2020
ms.locfileid: "48769433"
---
# <a name="onboard-windows-10-devices-using-configuration-manager"></a><span data-ttu-id="afc33-103">Périphériques Windows 10 embarqués à l’aide du gestionnaire de configuration</span><span class="sxs-lookup"><span data-stu-id="afc33-103">Onboard Windows 10 devices using Configuration Manager</span></span>

<span data-ttu-id="afc33-104">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="afc33-104">**Applies to:**</span></span>

- [<span data-ttu-id="afc33-105">Microsoft 365 protection contre la perte de données (DLP)</span><span class="sxs-lookup"><span data-stu-id="afc33-105">Microsoft 365 Endpoint data loss prevention (DLP)</span></span>](/microsoft-365/compliance/endpoint-dlp-learn-about)
- <span data-ttu-id="afc33-106">Gestionnaire de configuration de System Center 2012 R2</span><span class="sxs-lookup"><span data-stu-id="afc33-106">System Center 2012 R2 Configuration Manager</span></span>

### <a name="onboard-devices-using-system-center-configuration-manager"></a><span data-ttu-id="afc33-107">Périphériques intégrés à l’aide de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="afc33-107">Onboard devices using System Center Configuration Manager</span></span>

1. <span data-ttu-id="afc33-108">Ouvrez le fichier. zip du package de configuration du gestionnaire de configuration ( *DeviceComplianceOnboardingPackage.zip* ) que vous avez téléchargé à partir de l’Assistant d’intégration de service.</span><span class="sxs-lookup"><span data-stu-id="afc33-108">Open the Configuration Manager configuration package .zip file ( *DeviceComplianceOnboardingPackage.zip* ) that you downloaded from the service onboarding wizard.</span></span> <span data-ttu-id="afc33-109">Vous pouvez également obtenir le package à partir du [Centre de conformité Microsoft](https://compliance.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="afc33-109">You can also get the package from [Microsoft Compliance center](https://compliance.microsoft.com/).</span></span>

2. <span data-ttu-id="afc33-110">Dans le volet de navigation, sélectionnez **paramètres** d’intégration de l'  >  **appareil**  >  **Onboarding** .</span><span class="sxs-lookup"><span data-stu-id="afc33-110">In the navigation pane, select **Settings** > **Device Onboarding** > **Onboarding** .</span></span>

3. <span data-ttu-id="afc33-111">Dans le champ **méthode de déploiement** , sélectionnez **Microsoft Endpoint Configuration Manager 2012/2012 R2/1511/1602** .</span><span class="sxs-lookup"><span data-stu-id="afc33-111">In the **Deployment method** field, select **Microsoft Endpoint Configuration Manager 2012/2012 R2/1511/1602** .</span></span>
 
4. <span data-ttu-id="afc33-112">Sélectionnez **Télécharger le package** , puis enregistrez le fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="afc33-112">Select **Download package** , and save the .zip file.</span></span>

5. <span data-ttu-id="afc33-113">Extrayez le contenu du fichier. zip vers un emplacement partagé en lecture seule accessible par les administrateurs réseau qui déploieront le package.</span><span class="sxs-lookup"><span data-stu-id="afc33-113">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the network administrators who will deploy the package.</span></span> <span data-ttu-id="afc33-114">Vous devez avoir un fichier nommé *DeviceComplianceOnboardingScript. cmd* .</span><span class="sxs-lookup"><span data-stu-id="afc33-114">You should have a file named *DeviceComplianceOnboardingScript.cmd* .</span></span>

6. <span data-ttu-id="afc33-115">Déployez le package en suivant les étapes décrites dans l’article [packages and Programs dans System Center 2012 R2 Configuration Manager](https://docs.microsoft.com/previous-versions/system-center/system-center-2012-R2/gg699369\(v=technet.10\)) .</span><span class="sxs-lookup"><span data-stu-id="afc33-115">Deploy the package by following the steps in the [Packages and Programs in System Center 2012 R2 Configuration Manager](https://docs.microsoft.com/previous-versions/system-center/system-center-2012-R2/gg699369\(v=technet.10\)) article.</span></span>

7. <span data-ttu-id="afc33-116">Choisissez une collection d’appareils prédéfinie dans laquelle déployer le package.</span><span class="sxs-lookup"><span data-stu-id="afc33-116">Choose a predefined device collection to deploy the package to.</span></span>

> [!NOTE]
> <span data-ttu-id="afc33-117">La protection contre la perte de données de point de terminaison Microsoft 365 ne prend pas en charge l’intégration pendant la phase [OOBE (out-of-Box Experience)](https://answers.microsoft.com/en-us/windows/wiki/windows_10/how-to-complete-the-windows-10-out-of-box/47e3f943-f000-45e3-8c5c-9d85a1a0cf87) .</span><span class="sxs-lookup"><span data-stu-id="afc33-117">Microsoft 365 Endpoint data loss prevention doesn't support onboarding during the [Out-Of-Box Experience (OOBE)](https://answers.microsoft.com/en-us/windows/wiki/windows_10/how-to-complete-the-windows-10-out-of-box/47e3f943-f000-45e3-8c5c-9d85a1a0cf87) phase.</span></span> <span data-ttu-id="afc33-118">Assurez-vous que les utilisateurs ont terminé OOBE après l’installation ou la mise à niveau de Windows.</span><span class="sxs-lookup"><span data-stu-id="afc33-118">Make sure users complete OOBE after running Windows installation or upgrading.</span></span>

>[!TIP]
> <span data-ttu-id="afc33-119">Après avoir intégré l’appareil, vous pouvez choisir d’exécuter un test de détection pour vérifier qu’un appareil est correctement intégré au service.</span><span class="sxs-lookup"><span data-stu-id="afc33-119">After onboarding the device, you can choose to run a detection test to verify that an device is properly onboarded to the service.</span></span> <span data-ttu-id="afc33-120">Pour plus d’informations, reportez-vous à [la rubrique Run a Detection test on a nouvellement Onboard Microsoft Defender ATP Device](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/run-detection-test).</span><span class="sxs-lookup"><span data-stu-id="afc33-120">For more information, see [Run a detection test on a newly onboarded Microsoft Defender ATP device](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/run-detection-test).</span></span>
>
> <span data-ttu-id="afc33-121">Notez qu’il est possible de créer une règle de détection sur une application du gestionnaire de configuration pour vérifier en permanence si un périphérique a été intégré.</span><span class="sxs-lookup"><span data-stu-id="afc33-121">Note that it is possible to create a detection rule on a Configuration Manager application to continuously check if a device has been onboarded.</span></span> <span data-ttu-id="afc33-122">Une application est un autre type d’objet qu’un package et un programme.</span><span class="sxs-lookup"><span data-stu-id="afc33-122">An application is a different type of object than a package and program.</span></span>
> <span data-ttu-id="afc33-123">Si un périphérique n’est pas encore intégré (en raison d’une exécution OOBE en attente ou toute autre raison), le gestionnaire de configuration tente de l’intégrer à l’appareil jusqu’à ce que la règle détecte le changement d’État.</span><span class="sxs-lookup"><span data-stu-id="afc33-123">If a device is not yet onboarded (due to pending OOBE completion or any other reason), Configuration Manager will retry to onboard the device until the rule detects the status change.</span></span>
> 
> <span data-ttu-id="afc33-124">Ce comportement peut être obtenu en créant une règle de détection vérifiant si la valeur de Registre « OnboardingState » (de type REG_DWORD) = 1.</span><span class="sxs-lookup"><span data-stu-id="afc33-124">This behavior can be accomplished by creating a detection rule checking if the "OnboardingState" registry value (of type REG_DWORD) = 1.</span></span>
> <span data-ttu-id="afc33-125">Cette valeur de Registre se trouve sous « HKLM\SOFTWARE\Microsoft\Windows Advanced Threat Protection\Status ».</span><span class="sxs-lookup"><span data-stu-id="afc33-125">This registry value is located under "HKLM\SOFTWARE\Microsoft\Windows Advanced Threat Protection\Status".</span></span>
<span data-ttu-id="afc33-126">Pour plus d’informations, consultez la rubrique [configure Detection Methods in System Center 2012 R2 Configuration Manager](https://docs.microsoft.com/previous-versions/system-center/system-center-2012-R2/gg682159\(v=technet.10\)#step-4-configure-detection-methods-to-indicate-the-presence-of-the-deployment-type).</span><span class="sxs-lookup"><span data-stu-id="afc33-126">For more information, see [Configure Detection Methods in System Center 2012 R2 Configuration Manager](https://docs.microsoft.com/previous-versions/system-center/system-center-2012-R2/gg682159\(v=technet.10\)#step-4-configure-detection-methods-to-indicate-the-presence-of-the-deployment-type).</span></span>

### <a name="configure-sample-collection-settings"></a><span data-ttu-id="afc33-127">Configurer des paramètres de collection d’exemples</span><span class="sxs-lookup"><span data-stu-id="afc33-127">Configure sample collection settings</span></span>

<span data-ttu-id="afc33-128">Pour chaque appareil, vous pouvez définir une valeur de configuration indiquant si les échantillons peuvent être collectés à partir de l’appareil lorsqu’une demande est effectuée via le centre de sécurité Microsoft Defender pour soumettre un fichier à une analyse approfondie.</span><span class="sxs-lookup"><span data-stu-id="afc33-128">For each device, you can set a configuration value to state whether samples can be collected from the device when a request is made through Microsoft Defender Security Center to submit a file for deep analysis.</span></span>

>[!NOTE]
><span data-ttu-id="afc33-129">Ces paramètres de configuration sont généralement effectués via le gestionnaire de configuration.</span><span class="sxs-lookup"><span data-stu-id="afc33-129">These configuration settings are typically done through Configuration Manager.</span></span> 

<span data-ttu-id="afc33-130">Vous pouvez définir une règle de conformité pour l’élément de configuration dans le gestionnaire de configuration afin de modifier le paramètre de partage de l’exemple sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="afc33-130">You can set a compliance rule for configuration item in Configuration Manager to change the sample share setting on a device.</span></span>

<span data-ttu-id="afc33-131">Cette règle doit être un élément de configuration de règle de conformité de *Correction* qui définit la valeur d’une clé de Registre sur les appareils cibles afin de s’assurer qu’ils sont des plaintes.</span><span class="sxs-lookup"><span data-stu-id="afc33-131">This rule should be a *remediating* compliance rule configuration item that sets the value of a registry key on targeted devices to make sure they’re complaint.</span></span>

<span data-ttu-id="afc33-132">La configuration est définie par le biais de l’entrée de clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="afc33-132">The configuration is set through the following registry key entry:</span></span>

```
Path: “HKLM\SOFTWARE\Policies\Microsoft\Windows Advanced Threat Protection”
Name: "AllowSampleCollection"
Value: 0 or 1
```
<span data-ttu-id="afc33-133">Où :</span><span class="sxs-lookup"><span data-stu-id="afc33-133">Where:</span></span><br>
<span data-ttu-id="afc33-134">Le type de clé est un D-WORD.</span><span class="sxs-lookup"><span data-stu-id="afc33-134">Key type is a D-WORD.</span></span> <br>
<span data-ttu-id="afc33-135">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="afc33-135">Possible values are:</span></span>
- <span data-ttu-id="afc33-136">0-n’autorise pas le partage d’exemples à partir de cet appareil</span><span class="sxs-lookup"><span data-stu-id="afc33-136">0 - doesn't allow sample sharing  from this device</span></span>
- <span data-ttu-id="afc33-137">1-autorise le partage de tous les types de fichiers à partir de cet appareil</span><span class="sxs-lookup"><span data-stu-id="afc33-137">1 - allows sharing of all file types from this device</span></span>

<span data-ttu-id="afc33-138">La valeur par défaut s’il n’existe pas de clé de Registre est 1.</span><span class="sxs-lookup"><span data-stu-id="afc33-138">The default value in case the registry key doesn’t exist is 1.</span></span>

<span data-ttu-id="afc33-139">Pour plus d’informations sur la conformité de System Center Configuration Manager, voir [Introduction to Compliance Settings in System center 2012 R2 Configuration Manager](https://docs.microsoft.com/previous-versions/system-center/system-center-2012-R2/gg682139\(v=technet.10\)).</span><span class="sxs-lookup"><span data-stu-id="afc33-139">For more information about System Center Configuration Manager Compliance, see [Introduction to compliance settings in System Center 2012 R2 Configuration Manager](https://docs.microsoft.com/previous-versions/system-center/system-center-2012-R2/gg682139\(v=technet.10\)).</span></span>


## <a name="other-recommended-configuration-settings"></a><span data-ttu-id="afc33-140">Autres paramètres de configuration recommandés</span><span class="sxs-lookup"><span data-stu-id="afc33-140">Other recommended configuration settings</span></span>
<span data-ttu-id="afc33-141">Une fois les périphériques d’intégration au service, il est important de tirer parti des fonctionnalités de protection contre les menaces incluses en les activant avec les paramètres de configuration recommandés suivants.</span><span class="sxs-lookup"><span data-stu-id="afc33-141">After onboarding devices to the service, it's important to take advantage of the included threat protection capabilities by enabling them with the following recommended configuration settings.</span></span>

### <a name="device-collection-configuration"></a><span data-ttu-id="afc33-142">Configuration de la collection d’appareils</span><span class="sxs-lookup"><span data-stu-id="afc33-142">Device collection configuration</span></span>
<span data-ttu-id="afc33-143">Si vous utilisez le gestionnaire de configuration de point de terminaison, la version 2002 ou une version ultérieure, vous pouvez choisir d’élargir le déploiement pour inclure des serveurs ou des clients de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="afc33-143">If you're using Endpoint Configuration Manager, version 2002 or later, you can choose to broaden the deployment to include servers or down-level clients.</span></span>


### <a name="next-generation-protection-configuration"></a><span data-ttu-id="afc33-144">Configuration de la protection nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="afc33-144">Next generation protection configuration</span></span>

<span data-ttu-id="afc33-145">Les paramètres de configuration suivants sont recommandés :</span><span class="sxs-lookup"><span data-stu-id="afc33-145">The following configuration settings are recommended:</span></span>

<span data-ttu-id="afc33-146">**Analyser**</span><span class="sxs-lookup"><span data-stu-id="afc33-146">**Scan**</span></span>

- <span data-ttu-id="afc33-147">Analyser les périphériques de stockage amovibles tels que les lecteurs USB : Oui</span><span class="sxs-lookup"><span data-stu-id="afc33-147">Scan removable storage devices such as USB drives: Yes</span></span>

<span data-ttu-id="afc33-148">**Protection en temps réel**</span><span class="sxs-lookup"><span data-stu-id="afc33-148">**Real-time Protection**</span></span>

- <span data-ttu-id="afc33-149">Activer la surveillance comportementale : Oui</span><span class="sxs-lookup"><span data-stu-id="afc33-149">Enable Behavioral Monitoring: Yes</span></span>
- <span data-ttu-id="afc33-150">Activer la protection contre les applications potentiellement indésirables lors du téléchargement et avant l’installation : Oui</span><span class="sxs-lookup"><span data-stu-id="afc33-150">Enable protection against Potentially Unwanted Applications at download and prior to installation: Yes</span></span>

<span data-ttu-id="afc33-151">**Service de protection du Cloud**</span><span class="sxs-lookup"><span data-stu-id="afc33-151">**Cloud Protection Service**</span></span>

- <span data-ttu-id="afc33-152">Type d’appartenance au service protection du Cloud : appartenance avancée</span><span class="sxs-lookup"><span data-stu-id="afc33-152">Cloud Protection Service membership type: Advanced membership</span></span>

<span data-ttu-id="afc33-153">**Réduction** de la surface d’attaque Configurez toutes les règles disponibles pour l’audit.</span><span class="sxs-lookup"><span data-stu-id="afc33-153">**Attack surface reduction** Configure all available rules to Audit.</span></span>

>[!NOTE]
> <span data-ttu-id="afc33-154">Le blocage de ces activités peut interrompre des processus de gestion légitimes.</span><span class="sxs-lookup"><span data-stu-id="afc33-154">Blocking these activities may interrupt legitimate business processes.</span></span> <span data-ttu-id="afc33-155">La meilleure approche consiste à définir tous les éléments sur audit, à identifier ceux qui peuvent être activés, puis à activer ces paramètres sur les points de terminaison qui n’ont pas de détections fausses.</span><span class="sxs-lookup"><span data-stu-id="afc33-155">The best approach is setting everything to audit, identifying which ones are safe to turn on, and then enabling those settings on endpoints which do not have false positive detections.</span></span>

<span data-ttu-id="afc33-156">**Protection réseau**</span><span class="sxs-lookup"><span data-stu-id="afc33-156">**Network protection**</span></span>

<span data-ttu-id="afc33-157">Avant d’activer la protection réseau en mode d’audit ou de blocage, vérifiez que vous avez installé la mise à jour du logiciel anti-programme malveillant, qui peut être obtenue à partir de la [page support](https://support.microsoft.com/en-us/help/4560203/windows-defender-anti-malware-platform-binaries-are-missing).</span><span class="sxs-lookup"><span data-stu-id="afc33-157">Prior to enabling network protection in audit or block mode, ensure that you've installed the antimalware platform update, which can be obtained from the [support page](https://support.microsoft.com/en-us/help/4560203/windows-defender-anti-malware-platform-binaries-are-missing).</span></span>


<span data-ttu-id="afc33-158">**Accès contrôlé aux dossiers**</span><span class="sxs-lookup"><span data-stu-id="afc33-158">**Controlled folder access**</span></span>

<span data-ttu-id="afc33-159">Activez la fonctionnalité en mode audit pendant au moins 30 jours.</span><span class="sxs-lookup"><span data-stu-id="afc33-159">Enable the feature in audit mode for at least 30 days.</span></span> <span data-ttu-id="afc33-160">Après cette période, passez en revue les détections et créez une liste des applications autorisées à écrire dans les répertoires protégés.</span><span class="sxs-lookup"><span data-stu-id="afc33-160">After this period, review detections and create a list of applications that are allowed to write to protected directories.</span></span>

<span data-ttu-id="afc33-161">Pour plus d’informations, consultez la rubrique [Evaluate controled Folder Access](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/evaluate-controlled-folder-access).</span><span class="sxs-lookup"><span data-stu-id="afc33-161">For more information, see [Evaluate controlled folder access](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/evaluate-controlled-folder-access).</span></span>


## <a name="offboard-devices-using-configuration-manager"></a><span data-ttu-id="afc33-162">Appareils débarquement à l’aide du gestionnaire de configuration</span><span class="sxs-lookup"><span data-stu-id="afc33-162">Offboard devices using Configuration Manager</span></span>

<span data-ttu-id="afc33-163">Pour des raisons de sécurité, le package utilisé pour les appareils débarquement expire 30 jours après la date de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="afc33-163">For security reasons, the package used to Offboard devices will expire 30 days after the date it was downloaded.</span></span> <span data-ttu-id="afc33-164">Les packages par débarquement expirés envoyés à un appareil seront rejetés.</span><span class="sxs-lookup"><span data-stu-id="afc33-164">Expired offboarding packages sent to a device will be rejected.</span></span> <span data-ttu-id="afc33-165">Lors du téléchargement d’un package par débarquement, vous êtes informé de la date d’expiration des packages et il est également inclus dans le nom du package.</span><span class="sxs-lookup"><span data-stu-id="afc33-165">When downloading an offboarding package, you will be notified of the packages expiry date and it will also be included in the package name.</span></span>

> [!NOTE]
> <span data-ttu-id="afc33-166">Les stratégies d’intégration et de par débarquement ne doivent pas être déployées sur le même appareil simultanément, sinon cette opération entraîne des collisions imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="afc33-166">Onboarding and offboarding policies must not be deployed on the same device at the same time, otherwise this will cause unpredictable collisions.</span></span>

### <a name="offboard-devices-using-microsoft-endpoint-configuration-manager-current-branch"></a><span data-ttu-id="afc33-167">Périphériques débarquement utilisant la branche actuelle du gestionnaire de configuration de point de terminaison Microsoft</span><span class="sxs-lookup"><span data-stu-id="afc33-167">Offboard devices using Microsoft Endpoint Configuration Manager current branch</span></span>

<span data-ttu-id="afc33-168">Si vous utilisez la branche actuelle du gestionnaire de configuration de point de terminaison Microsoft, consultez la rubrique [créer un fichier de configuration par débarquement](https://docs.microsoft.com/configmgr/protect/deploy-use/windows-defender-advanced-threat-protection#create-an-offboarding-configuration-file).</span><span class="sxs-lookup"><span data-stu-id="afc33-168">If you use Microsoft Endpoint Configuration Manager current branch, see [Create an offboarding configuration file](https://docs.microsoft.com/configmgr/protect/deploy-use/windows-defender-advanced-threat-protection#create-an-offboarding-configuration-file).</span></span>

### <a name="offboard-devices-using-system-center-2012-r2-configuration-manager"></a><span data-ttu-id="afc33-169">Appareils débarquement à l’aide du gestionnaire de configuration System Center 2012 R2</span><span class="sxs-lookup"><span data-stu-id="afc33-169">Offboard devices using System Center 2012 R2 Configuration Manager</span></span>

1. <span data-ttu-id="afc33-170">Obtenir le package par débarquement à partir du [Centre de conformité Microsoft](https://compliance.microsoft.com/):</span><span class="sxs-lookup"><span data-stu-id="afc33-170">Get the offboarding package from [Microsoft Compliance center](https://compliance.microsoft.com/):</span></span>

2. <span data-ttu-id="afc33-171">Dans le volet de navigation, sélectionnez **paramètres** d'  >   **intégration d’appareil** >  **par débarquement** .</span><span class="sxs-lookup"><span data-stu-id="afc33-171">In the navigation pane, select **Settings** >  **Device onboarding**> **Offboarding** .</span></span>

3. <span data-ttu-id="afc33-172">Sélectionnez Windows 10 comme système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="afc33-172">Select Windows 10 as the operating system.</span></span>

4. <span data-ttu-id="afc33-173">Dans le champ **méthode de déploiement** , sélectionnez **Microsoft Endpoint Configuration Manager 2012/2012 R2/1511/1602** .</span><span class="sxs-lookup"><span data-stu-id="afc33-173">In the **Deployment method** field, select **Microsoft Endpoint Configuration Manager 2012/2012 R2/1511/1602** .</span></span>
    
5. <span data-ttu-id="afc33-174">Sélectionnez **Télécharger le package** , puis enregistrez le fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="afc33-174">Select **Download package** , and save the .zip file.</span></span>

6. <span data-ttu-id="afc33-175">Extrayez le contenu du fichier. zip vers un emplacement partagé en lecture seule accessible par les administrateurs réseau qui déploieront le package.</span><span class="sxs-lookup"><span data-stu-id="afc33-175">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the network administrators who will deploy the package.</span></span> <span data-ttu-id="afc33-176">Vous devez avoir un fichier nommé *DeviceComplianceOffboardingScript_valid_until_YYYY-mm-dd. cmd* .</span><span class="sxs-lookup"><span data-stu-id="afc33-176">You should have a file named *DeviceComplianceOffboardingScript_valid_until_YYYY-MM-DD.cmd* .</span></span>

7. <span data-ttu-id="afc33-177">Déployez le package en suivant les étapes décrites dans l’article [packages and Programs dans System Center 2012 R2 Configuration Manager](https://docs.microsoft.com/previous-versions/system-center/system-center-2012-R2/gg699369\(v=technet.10\)) .</span><span class="sxs-lookup"><span data-stu-id="afc33-177">Deploy the package by following the steps in the [Packages and Programs in System Center 2012 R2 Configuration Manager](https://docs.microsoft.com/previous-versions/system-center/system-center-2012-R2/gg699369\(v=technet.10\)) article.</span></span>

8. <span data-ttu-id="afc33-178">Choisissez une collection d’appareils prédéfinie dans laquelle déployer le package.</span><span class="sxs-lookup"><span data-stu-id="afc33-178">Choose a predefined device collection to deploy the package to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="afc33-179">Par débarquement entraîne l’arrêt de l’envoi des données de capteur au portail, mais les données de l’appareil, y compris la référence à toutes les alertes qu’il a subi, seront conservées pendant 6 mois maximum.</span><span class="sxs-lookup"><span data-stu-id="afc33-179">Offboarding causes the device to stop sending sensor data to the portal but data from the device, including reference to any alerts it has had will be retained for up to 6 months.</span></span>


## <a name="monitor-device-configuration"></a><span data-ttu-id="afc33-180">Surveiller la configuration de l’appareil</span><span class="sxs-lookup"><span data-stu-id="afc33-180">Monitor device configuration</span></span>

<span data-ttu-id="afc33-181">Si vous utilisez la branche actuelle du gestionnaire de configuration de point de terminaison Microsoft, utilisez le tableau de bord Microsoft Defender ATP intégré dans la console du gestionnaire de configuration.</span><span class="sxs-lookup"><span data-stu-id="afc33-181">If you're using Microsoft Endpoint Configuration Manager current branch, use the built-in Microsoft Defender ATP dashboard in the Configuration Manager console.</span></span> <span data-ttu-id="afc33-182">Pour plus d’informations, consultez la rubrique [Microsoft Defender Advanced Threat Protection-Monitor](https://docs.microsoft.com/configmgr/protect/deploy-use/windows-defender-advanced-threat-protection#monitor).</span><span class="sxs-lookup"><span data-stu-id="afc33-182">For more information, see [Microsoft Defender Advanced Threat Protection - Monitor](https://docs.microsoft.com/configmgr/protect/deploy-use/windows-defender-advanced-threat-protection#monitor).</span></span>

<span data-ttu-id="afc33-183">Si vous utilisez System Center 2012 R2 Configuration Manager, la surveillance se compose de deux parties :</span><span class="sxs-lookup"><span data-stu-id="afc33-183">If you're using System Center 2012 R2 Configuration Manager, monitoring consists of two parts:</span></span>

1. <span data-ttu-id="afc33-184">La confirmation du package de configuration a été correctement déployée et est en cours d’exécution (ou s’est exécutée correctement) sur les périphériques de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="afc33-184">Confirming the configuration package has been correctly deployed and is running (or has successfully run) on the devices in your network.</span></span>

2. <span data-ttu-id="afc33-185">Vérifier que les appareils sont conformes au service de protection contre la perte de données de point de terminaison de Microsoft 365 (cela garantit que l’appareil peut effectuer le processus d’intégration et continuer à signaler les données au service).</span><span class="sxs-lookup"><span data-stu-id="afc33-185">Checking that the devices are compliant with the Microsoft 365 Endpoint data loss prevention service (this ensures the device can complete the onboarding process and can continue to report data to the service).</span></span>

### <a name="confirm-the-configuration-package-has-been-correctly-deployed"></a><span data-ttu-id="afc33-186">Vérifiez que le package de configuration a été correctement déployé</span><span class="sxs-lookup"><span data-stu-id="afc33-186">Confirm the configuration package has been correctly deployed</span></span>

1. <span data-ttu-id="afc33-187">Dans la console Configuration Manager, cliquez sur **analyse** en bas du volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="afc33-187">In the Configuration Manager console, click **Monitoring** at the bottom of the navigation pane.</span></span>

2. <span data-ttu-id="afc33-188">Sélectionnez **vue d’ensemble** , puis **déploiements** .</span><span class="sxs-lookup"><span data-stu-id="afc33-188">Select **Overview** and then **Deployments** .</span></span>

3. <span data-ttu-id="afc33-189">Sélectionnez sur le déploiement avec le nom du package.</span><span class="sxs-lookup"><span data-stu-id="afc33-189">Select on the deployment with the package name.</span></span>

4. <span data-ttu-id="afc33-190">Examinez les indicateurs d’État sous **statistiques de saisie semi-automatique** et **État du contenu** .</span><span class="sxs-lookup"><span data-stu-id="afc33-190">Review the status indicators under **Completion Statistics** and **Content Status** .</span></span>

    <span data-ttu-id="afc33-191">En cas d’échec de déploiement (appareils avec **erreur** , **conditions non satisfaites** ou **État d’échec** ), vous devrez peut-être dépanner les appareils.</span><span class="sxs-lookup"><span data-stu-id="afc33-191">If there are failed deployments (devices with **Error** , **Requirements Not Met** , or **Failed statuses** ), you may need to  troubleshoot the devices.</span></span> <span data-ttu-id="afc33-192">Pour plus d’informations, reportez-vous à la rubrique Dépannage des problèmes d’intégration de la [protection avancée contre les menaces Microsoft](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding).</span><span class="sxs-lookup"><span data-stu-id="afc33-192">For more information, see, [Troubleshoot Microsoft Defender Advanced Threat Protection onboarding issues](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding).</span></span>

    ![Gestionnaire de configuration affichant le déploiement réussi sans erreur](../media/sccm-deployment.png)

### <a name="check-that-the-devices-are-compliant-with-the-microsoft-365-endpoint-data-loss-prevention-service"></a><span data-ttu-id="afc33-194">Vérifier que les appareils sont compatibles avec le service de protection contre la perte de données du point de terminaison Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="afc33-194">Check that the devices are compliant with the Microsoft 365 Endpoint data loss prevention service</span></span>

<span data-ttu-id="afc33-195">Vous pouvez définir une règle de conformité pour l’élément de configuration dans System Center 2012 R2 Configuration Manager pour surveiller votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="afc33-195">You can set a compliance rule for configuration item in System Center 2012 R2 Configuration Manager to monitor your deployment.</span></span>

> [!NOTE]
> <span data-ttu-id="afc33-196">Cette procédure et l’entrée de registre s’appliquent au point de terminaison DLP ainsi qu’à la protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="afc33-196">This procedure and registry entry applies to Endpoint DLP as well as Advanced Threat Protection.</span></span>

<span data-ttu-id="afc33-197">Cette règle doit être un élément de configuration de règle de conformité *sans correction* qui analyse la valeur d’une clé de Registre sur des appareils ciblés.</span><span class="sxs-lookup"><span data-stu-id="afc33-197">This rule should be a *non-remediating* compliance rule configuration item that monitors the value of a registry key on targeted devices.</span></span>

<span data-ttu-id="afc33-198">Surveillez l’entrée de clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="afc33-198">Monitor the following registry key entry:</span></span>
```
Path: “HKLM\SOFTWARE\Microsoft\Windows Advanced Threat Protection\Status”
Name: “OnboardingState”
Value: “1”
```
<span data-ttu-id="afc33-199">Pour plus d’informations, reportez-vous [à Introduction to Compliance Settings dans System Center 2012 R2 Configuration Manager](https://docs.microsoft.com/previous-versions/system-center/system-center-2012-R2/gg682139\(v=technet.10\)).</span><span class="sxs-lookup"><span data-stu-id="afc33-199">For more information, see [Introduction to compliance settings in System Center 2012 R2 Configuration Manager](https://docs.microsoft.com/previous-versions/system-center/system-center-2012-R2/gg682139\(v=technet.10\)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="afc33-200">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afc33-200">Related topics</span></span>
- [<span data-ttu-id="afc33-201">Périphériques Windows 10 embarqués à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="afc33-201">Onboard Windows 10 devices using Group Policy</span></span>](dlp-configure-endpoints-gp.md)
- [<span data-ttu-id="afc33-202">Périphériques Windows 10 intégrés à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="afc33-202">Onboard Windows 10 devices using Mobile Device Management tools</span></span>](dlp-configure-endpoints-mdm.md)
- [<span data-ttu-id="afc33-203">Périphériques Windows 10 embarqués à l’aide d’un script local</span><span class="sxs-lookup"><span data-stu-id="afc33-203">Onboard Windows 10 devices using a local script</span></span>](dlp-configure-endpoints-script.md)
- [<span data-ttu-id="afc33-204">Périphériques VDI (Virtual Desktop Infrastructure) non persistants</span><span class="sxs-lookup"><span data-stu-id="afc33-204">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>](dlp-configure-endpoints-vdi.md)
- [<span data-ttu-id="afc33-205">Exécution d’un test de détection sur un appareil Microsoft Defender nouvellement intégré</span><span class="sxs-lookup"><span data-stu-id="afc33-205">Run a detection test on a newly onboarded Microsoft Defender ATP device</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/run-detection-test)
- [<span data-ttu-id="afc33-206">Résoudre les problèmes d’intégration de la protection avancée contre les menaces Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="afc33-206">Troubleshoot Microsoft Defender Advanced Threat Protection onboarding issues</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding)
