---
title: Appareils Windows 10 intégrés utilisant Configuration Manager
description: Utilisez Configuration Manager pour déployer le package de configuration sur les appareils afin qu’ils soient intégrés au service.
keywords: intégrer des appareils à l’aide de sccm, gestion des appareils, configurer Microsoft Defender pour les appareils endpoint
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
ms.date: 02/07/2020
ms.technology: mde
ms.openlocfilehash: d827fb89a082286b1b7b77ea0a14e588ce171161
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52842193"
---
# <a name="onboard-windows-10-devices-using-configuration-manager"></a><span data-ttu-id="a722d-104">Appareils Windows 10 intégrés utilisant Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a722d-104">Onboard Windows 10 devices using Configuration Manager</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="a722d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a722d-105">**Applies to:**</span></span>

- [<span data-ttu-id="a722d-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a722d-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="a722d-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a722d-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)
- <span data-ttu-id="a722d-108">Microsoft Endpoint Configuration Manager branche actuelle</span><span class="sxs-lookup"><span data-stu-id="a722d-108">Microsoft Endpoint Configuration Manager current branch</span></span>
- <span data-ttu-id="a722d-109">Gestionnaire de configuration de System Center 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a722d-109">System Center 2012 R2 Configuration Manager</span></span>

><span data-ttu-id="a722d-110">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="a722d-110">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="a722d-111">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="a722d-111">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-configureendpointssccm-abovefoldlink)

## <a name="supported-client-operating-systems"></a><span data-ttu-id="a722d-112">Systèmes d’exploitation clients pris en charge</span><span class="sxs-lookup"><span data-stu-id="a722d-112">Supported client operating systems</span></span>

<span data-ttu-id="a722d-113">En fonction de la version de Configuration Manager que vous exécutez, les systèmes d’exploitation clients suivants peuvent être intégrés :</span><span class="sxs-lookup"><span data-stu-id="a722d-113">Based on the version of Configuration Manager you're running, the following client operating systems can be onboarded:</span></span>

#### <a name="configuration-manager-version-1910-and-prior"></a><span data-ttu-id="a722d-114">Configuration Manager version 1910 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="a722d-114">Configuration Manager version 1910 and prior</span></span>

- <span data-ttu-id="a722d-115">Ordinateurs clients exécutant Windows 10</span><span class="sxs-lookup"><span data-stu-id="a722d-115">Clients computers running Windows 10</span></span> 

#### <a name="configuration-manager-version-2002-and-later"></a><span data-ttu-id="a722d-116">Configuration Manager version 2002 et ultérieures</span><span class="sxs-lookup"><span data-stu-id="a722d-116">Configuration Manager version 2002 and later</span></span>

<span data-ttu-id="a722d-117">À partir de Configuration Manager version 2002, vous pouvez intégrer les systèmes d’exploitation suivants :</span><span class="sxs-lookup"><span data-stu-id="a722d-117">Starting in Configuration Manager version 2002, you can onboard the following operating systems:</span></span>

- <span data-ttu-id="a722d-118">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a722d-118">Windows 8.1</span></span>
- <span data-ttu-id="a722d-119">Windows 10</span><span class="sxs-lookup"><span data-stu-id="a722d-119">Windows 10</span></span>
- <span data-ttu-id="a722d-120">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a722d-120">Windows Server 2012 R2</span></span>
- <span data-ttu-id="a722d-121">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a722d-121">Windows Server 2016</span></span>
- <span data-ttu-id="a722d-122">Windows Server 2016, version 1803 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="a722d-122">Windows Server 2016, version 1803 or later</span></span>
- <span data-ttu-id="a722d-123">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="a722d-123">Windows Server 2019</span></span>

>[!NOTE]
><span data-ttu-id="a722d-124">Pour plus d’informations sur la façon d’intégrer Windows Server 2012 R2, Windows Server 2016 et Windows Server 2019, consultez la Windows [serveurs intégrés.](configure-server-endpoints.md)</span><span class="sxs-lookup"><span data-stu-id="a722d-124">For more information on how to onboard Windows Server 2012 R2, Windows Server 2016, and Windows Server 2019, see, [Onboard Windows servers](configure-server-endpoints.md).</span></span>



### <a name="onboard-devices-using-system-center-configuration-manager"></a><span data-ttu-id="a722d-125">Intégrer des appareils à l’aide System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a722d-125">Onboard devices using System Center Configuration Manager</span></span>


<span data-ttu-id="a722d-126">[![Image du PDF montrant les différents chemins de déploiement](images/onboard-config-mgr.png)](images/onboard-config-mgr.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="a722d-126">[![Image of the PDF showing the various deployment paths](images/onboard-config-mgr.png)](images/onboard-config-mgr.png#lightbox)</span></span>


<span data-ttu-id="a722d-127">Consultez le [fichier PDF](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf) [ou Visio](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.vsdx) pour voir les différents chemins d’accès dans le déploiement de Microsoft Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="a722d-127">Check out the [PDF](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.pdf)  or  [Visio](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/security/defender-endpoint/downloads/mdatp-deployment-strategy.vsdx) to see the various paths in deploying Microsoft Defender for Endpoint.</span></span> 



1. <span data-ttu-id="a722d-128">Ouvrez le fichier de package de configuration Configuration Manager .zip (*WindowsDefenderATPOnboardingPackage.zip*) que vous avez téléchargé à partir de l’Assistant d’intégration de service.</span><span class="sxs-lookup"><span data-stu-id="a722d-128">Open the Configuration Manager configuration package .zip file (*WindowsDefenderATPOnboardingPackage.zip*) that you downloaded from the service onboarding wizard.</span></span> <span data-ttu-id="a722d-129">Vous pouvez également obtenir le package à partir [de Centre de sécurité Microsoft Defender](https://securitycenter.windows.com/):</span><span class="sxs-lookup"><span data-stu-id="a722d-129">You can also get the package from [Microsoft Defender Security Center](https://securitycenter.windows.com/):</span></span>

    1. <span data-ttu-id="a722d-130">Dans le volet de navigation, sélectionnez  >  **Paramètres’intégration.**</span><span class="sxs-lookup"><span data-stu-id="a722d-130">In the navigation pane, select **Settings** > **Onboarding**.</span></span>
    
    1. <span data-ttu-id="a722d-131">Sélectionnez Windows 10 comme système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a722d-131">Select Windows 10 as the operating system.</span></span>

    1. <span data-ttu-id="a722d-132">Dans le champ Méthode **de** déploiement, **sélectionnez System Center Configuration Manager 2012/2012 R2/1511/1602**.</span><span class="sxs-lookup"><span data-stu-id="a722d-132">In the **Deployment method** field, select **System Center Configuration Manager 2012/2012 R2/1511/1602**.</span></span>
    
    1. <span data-ttu-id="a722d-133">Sélectionnez **le package** de téléchargement et enregistrez .zip fichier.</span><span class="sxs-lookup"><span data-stu-id="a722d-133">Select **Download package**, and save the .zip file.</span></span>

2. <span data-ttu-id="a722d-134">Extrayez le contenu du fichier .zip vers un emplacement partagé en lecture seule accessible par les administrateurs réseau qui déploieront le package.</span><span class="sxs-lookup"><span data-stu-id="a722d-134">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the network administrators who will deploy the package.</span></span> <span data-ttu-id="a722d-135">Vous devez avoir un fichier nommé *WindowsDefenderATPOnboardingScript.cmd*.</span><span class="sxs-lookup"><span data-stu-id="a722d-135">You should have a file named *WindowsDefenderATPOnboardingScript.cmd*.</span></span>

3. <span data-ttu-id="a722d-136">Déployez le package en suivant les étapes de l’article Packages et programmes [System Center 2012 R2 Configuration Manager.](/previous-versions/system-center/system-center-2012-R2/gg699369\(v=technet.10\))</span><span class="sxs-lookup"><span data-stu-id="a722d-136">Deploy the package by following the steps in the [Packages and Programs in System Center 2012 R2 Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg699369\(v=technet.10\)) article.</span></span>

    <span data-ttu-id="a722d-137">a.</span><span class="sxs-lookup"><span data-stu-id="a722d-137">a.</span></span> <span data-ttu-id="a722d-138">Choisissez une collection d’appareils prédéfiny pour déployer le package.</span><span class="sxs-lookup"><span data-stu-id="a722d-138">Choose a predefined device collection to deploy the package to.</span></span>

> [!NOTE]
> <span data-ttu-id="a722d-139">Defender pour le point de terminaison ne prend pas en charge l’intégration pendant la phase [OOBE (Out-Of-Box Experience).](https://answers.microsoft.com/en-us/windows/wiki/windows_10/how-to-complete-the-windows-10-out-of-box/47e3f943-f000-45e3-8c5c-9d85a1a0cf87)</span><span class="sxs-lookup"><span data-stu-id="a722d-139">Defender for Endpoint doesn't support onboarding during the [Out-Of-Box Experience (OOBE)](https://answers.microsoft.com/en-us/windows/wiki/windows_10/how-to-complete-the-windows-10-out-of-box/47e3f943-f000-45e3-8c5c-9d85a1a0cf87) phase.</span></span> <span data-ttu-id="a722d-140">Assurez-vous que les utilisateurs ont terminé la OOBE après Windows’installation ou de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="a722d-140">Make sure users complete OOBE after running Windows installation or upgrading.</span></span>

>[!TIP]
> <span data-ttu-id="a722d-141">Après avoir intégré l’appareil, vous pouvez choisir d’exécuter un test de détection pour vérifier qu’un appareil est correctement intégré au service.</span><span class="sxs-lookup"><span data-stu-id="a722d-141">After onboarding the device, you can choose to run a detection test to verify that an device is properly onboarded to the service.</span></span> <span data-ttu-id="a722d-142">Pour plus d’informations, voir Exécuter un test de détection sur un appareil [Defender for Endpoint nouvellement intégré.](run-detection-test.md)</span><span class="sxs-lookup"><span data-stu-id="a722d-142">For more information, see [Run a detection test on a newly onboarded Defender for Endpoint device](run-detection-test.md).</span></span>
>
> <span data-ttu-id="a722d-143">Notez qu’il est possible de créer une règle de détection sur une application Configuration Manager pour vérifier en permanence si un appareil a été intégré.</span><span class="sxs-lookup"><span data-stu-id="a722d-143">Note that it is possible to create a detection rule on a Configuration Manager application to continuously check if a device has been onboarded.</span></span> <span data-ttu-id="a722d-144">Une application est un type d’objet différent d’un package et d’un programme.</span><span class="sxs-lookup"><span data-stu-id="a722d-144">An application is a different type of object than a package and program.</span></span>
> <span data-ttu-id="a722d-145">Si un appareil n’est pas encore intégré (en raison de l’exécution de la OOBE en attente ou d’une autre raison), Configuration Manager réessaye d’intégrer l’appareil jusqu’à ce que la règle détecte le changement d’état.</span><span class="sxs-lookup"><span data-stu-id="a722d-145">If a device is not yet onboarded (due to pending OOBE completion or any other reason), Configuration Manager will retry to onboard the device until the rule detects the status change.</span></span>
> 
> <span data-ttu-id="a722d-146">Ce comportement peut être réalisé en créant une règle de détection vérifiant si la valeur de Registre « OnboardingState » (de type REG_DWORD) = 1.</span><span class="sxs-lookup"><span data-stu-id="a722d-146">This behavior can be accomplished by creating a detection rule checking if the "OnboardingState" registry value (of type REG_DWORD) = 1.</span></span>
> <span data-ttu-id="a722d-147">Cette valeur de Registre se trouve sous « HKLM\SOFTWARE\Microsoft\Windows Advanced Threat Protection\Status ».</span><span class="sxs-lookup"><span data-stu-id="a722d-147">This registry value is located under "HKLM\SOFTWARE\Microsoft\Windows Advanced Threat Protection\Status".</span></span>
<span data-ttu-id="a722d-148">Pour plus d’informations, [voir Configure Detection Methods in System Center 2012 R2 Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682159\(v=technet.10\)#step-4-configure-detection-methods-to-indicate-the-presence-of-the-deployment-type).</span><span class="sxs-lookup"><span data-stu-id="a722d-148">For more information, see [Configure Detection Methods in System Center 2012 R2 Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682159\(v=technet.10\)#step-4-configure-detection-methods-to-indicate-the-presence-of-the-deployment-type).</span></span>

### <a name="configure-sample-collection-settings"></a><span data-ttu-id="a722d-149">Configurer des paramètres de collection d’exemples</span><span class="sxs-lookup"><span data-stu-id="a722d-149">Configure sample collection settings</span></span>

<span data-ttu-id="a722d-150">Pour chaque appareil, vous pouvez définir une valeur de configuration pour déterminer si des échantillons peuvent être collectés à partir de l’appareil lorsqu’une demande est faite via Centre de sécurité Microsoft Defender pour soumettre un fichier pour analyse approfondie.</span><span class="sxs-lookup"><span data-stu-id="a722d-150">For each device, you can set a configuration value to state whether samples can be collected from the device when a request is made through Microsoft Defender Security Center to submit a file for deep analysis.</span></span>

>[!NOTE]
><span data-ttu-id="a722d-151">Ces paramètres de configuration sont généralement effectués via Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a722d-151">These configuration settings are typically done through Configuration Manager.</span></span> 

<span data-ttu-id="a722d-152">Vous pouvez définir une règle de conformité pour l’élément de configuration dans Configuration Manager afin de modifier le paramètre de partage d’exemples sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="a722d-152">You can set a compliance rule for configuration item in Configuration Manager to change the sample share setting on a device.</span></span>

<span data-ttu-id="a722d-153">Cette règle doit  être un élément de configuration de règle de conformité de correction qui définit la valeur d’une clé de Registre sur les appareils ciblés pour s’assurer qu’ils sont conformes.</span><span class="sxs-lookup"><span data-stu-id="a722d-153">This rule should be a *remediating* compliance rule configuration item that sets the value of a registry key on targeted devices to make sure they’re complaint.</span></span>

<span data-ttu-id="a722d-154">La configuration est définie par le biais de l’entrée de clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="a722d-154">The configuration is set through the following registry key entry:</span></span>

```console
Path: "HKLM\SOFTWARE\Policies\Microsoft\Windows Advanced Threat Protection"
Name: "AllowSampleCollection"
Value: 0 or 1
```

<span data-ttu-id="a722d-155">Où :</span><span class="sxs-lookup"><span data-stu-id="a722d-155">Where:</span></span><br>
<span data-ttu-id="a722d-156">Le type de clé est un D-WORD.</span><span class="sxs-lookup"><span data-stu-id="a722d-156">Key type is a D-WORD.</span></span> <br>
<span data-ttu-id="a722d-157">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a722d-157">Possible values are:</span></span>
- <span data-ttu-id="a722d-158">0 : n’autorise pas le partage d’exemples à partir de cet appareil</span><span class="sxs-lookup"><span data-stu-id="a722d-158">0 - doesn't allow sample sharing  from this device</span></span>
- <span data-ttu-id="a722d-159">1 : autorise le partage de tous les types de fichiers à partir de cet appareil</span><span class="sxs-lookup"><span data-stu-id="a722d-159">1 - allows sharing of all file types from this device</span></span>

<span data-ttu-id="a722d-160">La valeur par défaut au cas où la clé de Registre n’existe pas est 1.</span><span class="sxs-lookup"><span data-stu-id="a722d-160">The default value in case the registry key doesn’t exist is 1.</span></span>

<span data-ttu-id="a722d-161">Pour plus d’informations sur System Center Configuration Manager conformité, voir Introduction aux paramètres de conformité dans [System Center 2012 R2 Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682139\(v=technet.10\)).</span><span class="sxs-lookup"><span data-stu-id="a722d-161">For more information about System Center Configuration Manager Compliance, see [Introduction to compliance settings in System Center 2012 R2 Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682139\(v=technet.10\)).</span></span>


## <a name="other-recommended-configuration-settings"></a><span data-ttu-id="a722d-162">Autres paramètres de configuration recommandés</span><span class="sxs-lookup"><span data-stu-id="a722d-162">Other recommended configuration settings</span></span>
<span data-ttu-id="a722d-163">Une fois les appareils intégrés au service, il est important de tirer parti des fonctionnalités de protection contre les menaces incluses en les activant avec les paramètres de configuration recommandés suivants.</span><span class="sxs-lookup"><span data-stu-id="a722d-163">After onboarding devices to the service, it's important to take advantage of the included threat protection capabilities by enabling them with the following recommended configuration settings.</span></span>

### <a name="device-collection-configuration"></a><span data-ttu-id="a722d-164">Configuration de la collection d’appareils</span><span class="sxs-lookup"><span data-stu-id="a722d-164">Device collection configuration</span></span>
<span data-ttu-id="a722d-165">Si vous utilisez Endpoint Configuration Manager, version 2002 ou ultérieure, vous pouvez choisir d’élargir le déploiement pour inclure des serveurs ou des clients de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="a722d-165">If you're using Endpoint Configuration Manager, version 2002 or later, you can choose to broaden the deployment to include servers or down-level clients.</span></span>


### <a name="next-generation-protection-configuration"></a><span data-ttu-id="a722d-166">Configuration de la protection nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="a722d-166">Next generation protection configuration</span></span>
<span data-ttu-id="a722d-167">Les paramètres de configuration suivants sont recommandés :</span><span class="sxs-lookup"><span data-stu-id="a722d-167">The following configuration settings are recommended:</span></span>

<span data-ttu-id="a722d-168">**Analyser**</span><span class="sxs-lookup"><span data-stu-id="a722d-168">**Scan**</span></span> <br>
- <span data-ttu-id="a722d-169">Analyser les périphériques de stockage amovibles tels que les lecteurs USB : Oui</span><span class="sxs-lookup"><span data-stu-id="a722d-169">Scan removable storage devices such as USB drives: Yes</span></span>

<span data-ttu-id="a722d-170">**Protection en temps réel**</span><span class="sxs-lookup"><span data-stu-id="a722d-170">**Real-time Protection**</span></span> <br>
- <span data-ttu-id="a722d-171">Activer la surveillance comportementale : Oui</span><span class="sxs-lookup"><span data-stu-id="a722d-171">Enable Behavioral Monitoring: Yes</span></span>
- <span data-ttu-id="a722d-172">Activer la protection contre les applications potentiellement indésirables au téléchargement et avant l’installation : Oui</span><span class="sxs-lookup"><span data-stu-id="a722d-172">Enable protection against Potentially Unwanted Applications at download and prior to installation: Yes</span></span>

<span data-ttu-id="a722d-173">**Cloud Protection Service**</span><span class="sxs-lookup"><span data-stu-id="a722d-173">**Cloud Protection Service**</span></span>
- <span data-ttu-id="a722d-174">Type d’appartenance au service Cloud Protection : appartenance avancée</span><span class="sxs-lookup"><span data-stu-id="a722d-174">Cloud Protection Service membership type: Advanced membership</span></span>

<span data-ttu-id="a722d-175">**Réduction de la surface d’attaque** Configurez toutes les règles disponibles pour auditer.</span><span class="sxs-lookup"><span data-stu-id="a722d-175">**Attack surface reduction** Configure all available rules to Audit.</span></span>

>[!NOTE]
> <span data-ttu-id="a722d-176">Le blocage de ces activités peut interrompre les processus d’entreprise légitimes.</span><span class="sxs-lookup"><span data-stu-id="a722d-176">Blocking these activities may interrupt legitimate business processes.</span></span> <span data-ttu-id="a722d-177">La meilleure approche consiste à définir tous les paramètres à auditer, à identifier ceux qui sont sûrs à activer, puis à activer ces paramètres sur les points de terminaison qui n’ont pas de détections de faux positifs.</span><span class="sxs-lookup"><span data-stu-id="a722d-177">The best approach is setting everything to audit, identifying which ones are safe to turn on, and then enabling those settings on endpoints which do not have false positive detections.</span></span>


<span data-ttu-id="a722d-178">**Protection du réseau**</span><span class="sxs-lookup"><span data-stu-id="a722d-178">**Network protection**</span></span> <br>
<span data-ttu-id="a722d-179">Avant d’activer la protection réseau en mode audit ou blocage, assurez-vous que vous avez installé la mise à jour de la plateforme anti-programme malveillant, qui peut être obtenue à partir de la [page de support.](https://support.microsoft.com/en-us/help/4560203/windows-defender-anti-malware-platform-binaries-are-missing)</span><span class="sxs-lookup"><span data-stu-id="a722d-179">Prior to enabling network protection in audit or block mode, ensure that you've installed the antimalware platform update, which can be obtained from the [support page](https://support.microsoft.com/en-us/help/4560203/windows-defender-anti-malware-platform-binaries-are-missing).</span></span>


<span data-ttu-id="a722d-180">**Accès contrôlé aux dossiers**</span><span class="sxs-lookup"><span data-stu-id="a722d-180">**Controlled folder access**</span></span><br>
<span data-ttu-id="a722d-181">Activez la fonctionnalité en mode audit pendant au moins 30 jours.</span><span class="sxs-lookup"><span data-stu-id="a722d-181">Enable the feature in audit mode for at least 30 days.</span></span> <span data-ttu-id="a722d-182">Après cette période, examinez les détections et créez une liste d’applications autorisées à écrire dans des répertoires protégés.</span><span class="sxs-lookup"><span data-stu-id="a722d-182">After this period, review detections and create a list of applications that are allowed to write to protected directories.</span></span>

<span data-ttu-id="a722d-183">Pour plus d’informations, voir [Évaluer l’accès contrôlé aux dossiers.](evaluate-controlled-folder-access.md)</span><span class="sxs-lookup"><span data-stu-id="a722d-183">For more information, see [Evaluate controlled folder access](evaluate-controlled-folder-access.md).</span></span>


## <a name="offboard-devices-using-configuration-manager"></a><span data-ttu-id="a722d-184">Hors-carte des appareils à l’aide de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a722d-184">Offboard devices using Configuration Manager</span></span>

<span data-ttu-id="a722d-185">Pour des raisons de sécurité, le package utilisé pour la sortie des appareils expirera 30 jours après la date de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="a722d-185">For security reasons, the package used to Offboard devices will expire 30 days after the date it was downloaded.</span></span> <span data-ttu-id="a722d-186">Les packages deboarding expirés envoyés à un appareil seront rejetés.</span><span class="sxs-lookup"><span data-stu-id="a722d-186">Expired offboarding packages sent to a device will be rejected.</span></span> <span data-ttu-id="a722d-187">Lorsque vous téléchargez un package de déclassage, vous êtes informé de la date d’expiration des packages et il est également inclus dans le nom du package.</span><span class="sxs-lookup"><span data-stu-id="a722d-187">When downloading an offboarding package, you will be notified of the packages expiry date and it will also be included in the package name.</span></span>

> [!NOTE]
> <span data-ttu-id="a722d-188">Les stratégies d’intégration et deboarding ne doivent pas être déployées sur le même appareil en même temps, sinon cela provoquera des collisions imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="a722d-188">Onboarding and offboarding policies must not be deployed on the same device at the same time, otherwise this will cause unpredictable collisions.</span></span>

### <a name="offboard-devices-using-microsoft-endpoint-manager-current-branch"></a><span data-ttu-id="a722d-189">Appareils de tableau de bord à l’Microsoft Endpoint Manager branche actuelle</span><span class="sxs-lookup"><span data-stu-id="a722d-189">Offboard devices using Microsoft Endpoint Manager current branch</span></span>

<span data-ttu-id="a722d-190">Si vous utilisez Microsoft Endpoint Manager branche actuelle, voir Créer un fichier [de configuration deboarding.](/configmgr/protect/deploy-use/windows-defender-advanced-threat-protection#create-an-offboarding-configuration-file)</span><span class="sxs-lookup"><span data-stu-id="a722d-190">If you use Microsoft Endpoint Manager current branch, see [Create an offboarding configuration file](/configmgr/protect/deploy-use/windows-defender-advanced-threat-protection#create-an-offboarding-configuration-file).</span></span>

### <a name="offboard-devices-using-system-center-2012-r2-configuration-manager"></a><span data-ttu-id="a722d-191">Appareils de déboardage System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a722d-191">Offboard devices using System Center 2012 R2 Configuration Manager</span></span>

1. <span data-ttu-id="a722d-192">Obtenez le package deboarding à partir [Centre de sécurité Microsoft Defender](https://securitycenter.windows.com/):</span><span class="sxs-lookup"><span data-stu-id="a722d-192">Get the offboarding package from [Microsoft Defender Security Center](https://securitycenter.windows.com/):</span></span>

    1. <span data-ttu-id="a722d-193">Dans le volet de navigation, sélectionnez **Paramètres**  >   **de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="a722d-193">In the navigation pane, select **Settings** >  **Offboarding**.</span></span>

    1. <span data-ttu-id="a722d-194">Sélectionnez Windows 10 comme système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a722d-194">Select Windows 10 as the operating system.</span></span>

    1. <span data-ttu-id="a722d-195">Dans le champ Méthode **de** déploiement, **sélectionnez System Center Configuration Manager 2012/2012 R2/1511/1602**.</span><span class="sxs-lookup"><span data-stu-id="a722d-195">In the **Deployment method** field, select **System Center Configuration Manager 2012/2012 R2/1511/1602**.</span></span>
    
    1. <span data-ttu-id="a722d-196">Sélectionnez **le package** de téléchargement et enregistrez .zip fichier.</span><span class="sxs-lookup"><span data-stu-id="a722d-196">Select **Download package**, and save the .zip file.</span></span>

2. <span data-ttu-id="a722d-197">Extrayez le contenu du fichier .zip vers un emplacement partagé en lecture seule accessible par les administrateurs réseau qui déploieront le package.</span><span class="sxs-lookup"><span data-stu-id="a722d-197">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the network administrators who will deploy the package.</span></span> <span data-ttu-id="a722d-198">Vous devez avoir un fichier nommé *WindowsDefenderATPOffboardingScript_valid_until_YYYY-MM-DD.cmd*.</span><span class="sxs-lookup"><span data-stu-id="a722d-198">You should have a file named *WindowsDefenderATPOffboardingScript_valid_until_YYYY-MM-DD.cmd*.</span></span>

3. <span data-ttu-id="a722d-199">Déployez le package en suivant les étapes de l’article Packages et programmes [System Center 2012 R2 Configuration Manager.](/previous-versions/system-center/system-center-2012-R2/gg699369\(v=technet.10\))</span><span class="sxs-lookup"><span data-stu-id="a722d-199">Deploy the package by following the steps in the [Packages and Programs in System Center 2012 R2 Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg699369\(v=technet.10\)) article.</span></span>

    <span data-ttu-id="a722d-200">a.</span><span class="sxs-lookup"><span data-stu-id="a722d-200">a.</span></span> <span data-ttu-id="a722d-201">Choisissez une collection d’appareils prédéfiny pour déployer le package.</span><span class="sxs-lookup"><span data-stu-id="a722d-201">Choose a predefined device collection to deploy the package to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a722d-202">Laboarding empêche l’appareil d’envoyer des données de capteur au portail, mais les données de l’appareil, y compris la référence aux alertes qu’il a eues, seront conservées pendant 6 mois.</span><span class="sxs-lookup"><span data-stu-id="a722d-202">Offboarding causes the device to stop sending sensor data to the portal but data from the device, including reference to any alerts it has had will be retained for up to 6 months.</span></span>


## <a name="monitor-device-configuration"></a><span data-ttu-id="a722d-203">Surveiller la configuration de l’appareil</span><span class="sxs-lookup"><span data-stu-id="a722d-203">Monitor device configuration</span></span>

<span data-ttu-id="a722d-204">Si vous utilisez la Microsoft Endpoint Manager actuelle, utilisez le tableau de bord Defender for Endpoint intégré dans la console Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a722d-204">If you're using Microsoft Endpoint Manager current branch, use the built-in Defender for Endpoint dashboard in the Configuration Manager console.</span></span> <span data-ttu-id="a722d-205">Pour plus d’informations, [voir Defender for Endpoint - Monitor](/configmgr/protect/deploy-use/windows-defender-advanced-threat-protection#monitor).</span><span class="sxs-lookup"><span data-stu-id="a722d-205">For more information, see [Defender for Endpoint - Monitor](/configmgr/protect/deploy-use/windows-defender-advanced-threat-protection#monitor).</span></span>

<span data-ttu-id="a722d-206">Si vous utilisez System Center 2012 R2 Configuration Manager, la surveillance se compose de deux parties :</span><span class="sxs-lookup"><span data-stu-id="a722d-206">If you're using System Center 2012 R2 Configuration Manager, monitoring consists of two parts:</span></span>

1. <span data-ttu-id="a722d-207">Confirmation que le package de configuration a été correctement déployé et qu’il est en cours d’exécution (ou qu’il s’est correctement exécuté) sur les appareils de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="a722d-207">Confirming the configuration package has been correctly deployed and is running (or has successfully run) on the devices in your network.</span></span>

2. <span data-ttu-id="a722d-208">Vérification de la conformité des appareils avec le service Defender for Endpoint (cela garantit que l’appareil peut terminer le processus d’intégration et continuer à signaler des données au service).</span><span class="sxs-lookup"><span data-stu-id="a722d-208">Checking that the devices are compliant with the Defender for Endpoint service (this ensures the device can complete the onboarding process and can continue to report data to the service).</span></span>

### <a name="confirm-the-configuration-package-has-been-correctly-deployed"></a><span data-ttu-id="a722d-209">Vérifier que le package de configuration a été correctement déployé</span><span class="sxs-lookup"><span data-stu-id="a722d-209">Confirm the configuration package has been correctly deployed</span></span>

1. <span data-ttu-id="a722d-210">Dans la console Configuration Manager, cliquez **sur Analyse** en bas du volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="a722d-210">In the Configuration Manager console, click **Monitoring** at the bottom of the navigation pane.</span></span>

2. <span data-ttu-id="a722d-211">Sélectionnez **Vue d’ensemble,** puis **Déploiements.**</span><span class="sxs-lookup"><span data-stu-id="a722d-211">Select **Overview** and then **Deployments**.</span></span>

3. <span data-ttu-id="a722d-212">Sélectionnez le déploiement avec le nom du package.</span><span class="sxs-lookup"><span data-stu-id="a722d-212">Select on the deployment with the package name.</span></span>

4. <span data-ttu-id="a722d-213">Examinez les indicateurs d’état sous **Statistiques d’achèvement** et **État du contenu.**</span><span class="sxs-lookup"><span data-stu-id="a722d-213">Review the status indicators under **Completion Statistics** and **Content Status**.</span></span>

    <span data-ttu-id="a722d-214">En cas d’échec des déploiements (appareils avec **erreur,** conditions requises non remplies ou états d’échec), vous devrez peut-être résoudre les problèmes des appareils.</span><span class="sxs-lookup"><span data-stu-id="a722d-214">If there are failed deployments (devices with **Error**, **Requirements Not Met**, or **Failed statuses**), you may need to  troubleshoot the devices.</span></span> <span data-ttu-id="a722d-215">Pour plus d’informations, voir résoudre les problèmes d’intégration de Microsoft Defender pour les [points de terminaison.](troubleshoot-onboarding.md)</span><span class="sxs-lookup"><span data-stu-id="a722d-215">For more information, see, [Troubleshoot Microsoft Defender for Endpoint onboarding issues](troubleshoot-onboarding.md).</span></span>

    ![Configuration Manager affichant un déploiement réussi sans erreur](images/sccm-deployment.png)

### <a name="check-that-the-devices-are-compliant-with-the-microsoft-defender-for-endpoint-service"></a><span data-ttu-id="a722d-217">Vérifier que les appareils sont conformes au service Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="a722d-217">Check that the devices are compliant with the Microsoft Defender for Endpoint service</span></span>

<span data-ttu-id="a722d-218">Vous pouvez définir une règle de conformité pour l’élément de configuration dans System Center 2012 R2 Configuration Manager pour surveiller votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="a722d-218">You can set a compliance rule for configuration item in System Center 2012 R2 Configuration Manager to monitor your deployment.</span></span>

<span data-ttu-id="a722d-219">Cette règle doit être un élément de configuration de règle de conformité *sans* correction qui surveille la valeur d’une clé de Registre sur des appareils ciblés.</span><span class="sxs-lookup"><span data-stu-id="a722d-219">This rule should be a *non-remediating* compliance rule configuration item that monitors the value of a registry key on targeted devices.</span></span>

<span data-ttu-id="a722d-220">Surveillez l’entrée de clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="a722d-220">Monitor the following registry key entry:</span></span>

```console
Path: "HKLM\SOFTWARE\Microsoft\Windows Advanced Threat Protection\Status"
Name: "OnboardingState"
Value: "1"
```

<span data-ttu-id="a722d-221">Pour plus d’informations, voir Introduction aux paramètres de conformité [dans System Center 2012 R2 Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682139\(v=technet.10\)).</span><span class="sxs-lookup"><span data-stu-id="a722d-221">For more information, see [Introduction to compliance settings in System Center 2012 R2 Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682139\(v=technet.10\)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a722d-222">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a722d-222">Related topics</span></span>
- [<span data-ttu-id="a722d-223">Intégrer des Windows 10 à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="a722d-223">Onboard Windows 10 devices using Group Policy</span></span>](configure-endpoints-gp.md)
- [<span data-ttu-id="a722d-224">Intégrer les appareils Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="a722d-224">Onboard Windows 10 devices using Mobile Device Management tools</span></span>](configure-endpoints-mdm.md)
- [<span data-ttu-id="a722d-225">Intégrer les appareils Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="a722d-225">Onboard Windows 10 devices using a local script</span></span>](configure-endpoints-script.md)
- [<span data-ttu-id="a722d-226">Intégrer les ordinateurs virtuels d’infrastructure de bureau (VDI) non persistants</span><span class="sxs-lookup"><span data-stu-id="a722d-226">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>](configure-endpoints-vdi.md)
- [<span data-ttu-id="a722d-227">Exécuter un test de détection sur un appareil Microsoft Defender pour point de terminaison nouvellement intégré</span><span class="sxs-lookup"><span data-stu-id="a722d-227">Run a detection test on a newly onboarded Microsoft Defender for Endpoint device</span></span>](run-detection-test.md)
- [<span data-ttu-id="a722d-228">Résoudre les problèmes d’intégration de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="a722d-228">Troubleshoot Microsoft Defender for Endpoint onboarding issues</span></span>](troubleshoot-onboarding.md)
