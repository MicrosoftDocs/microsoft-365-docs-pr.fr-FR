---
title: Intégrer des appareils Windows 10 à sessions multiples dans Windows Virtual Desktop
description: En savoir plus dans cet article sur l’intégration Windows 10 appareils multisess session dans Windows Virtual Desktop
keywords: Windows Virtual Desktop, WVD, microsoft defender, point de terminaison, intégration
search.product: eADQiWindows 10XVcnh
ms.prod: w10
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
audience: ITPro
ms.topic: article
author: dansimp
ms.author: dansimp
ms.custom: nextgen
ms.reviewer: ''
manager: dansimp
ms.openlocfilehash: 9114a825ad011f0b2a17cea4929ab2a09bfa2172
ms.sourcegitcommit: 0d1b065c94125b495e9886200f7918de3bda40b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2021
ms.locfileid: "53339477"
---
# <a name="onboard-windows-10-multi-session-devices-in-windows-virtual-desktop"></a><span data-ttu-id="36385-104">Intégrer des appareils Windows 10 à sessions multiples dans Windows Virtual Desktop</span><span class="sxs-lookup"><span data-stu-id="36385-104">Onboard Windows 10 multi-session devices in Windows Virtual Desktop</span></span> 
<span data-ttu-id="36385-105">6 minutes de lecture</span><span class="sxs-lookup"><span data-stu-id="36385-105">6 minutes to read</span></span> 

<span data-ttu-id="36385-106">S’applique à :</span><span class="sxs-lookup"><span data-stu-id="36385-106">Applies to:</span></span> 
- <span data-ttu-id="36385-107">Windows 10 sessions multiples s’exécutant Windows Virtual Desktop (WVD)</span><span class="sxs-lookup"><span data-stu-id="36385-107">Windows 10 multi-session running on Windows Virtual Desktop (WVD)</span></span> 

<span data-ttu-id="36385-108">Microsoft Defender pour le point de terminaison prend en charge la surveillance des sessions VDI et Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="36385-108">Microsoft Defender for Endpoint supports monitoring both VDI and Windows Virtual Desktop sessions.</span></span> <span data-ttu-id="36385-109">En fonction des besoins de votre organisation, vous devrez peut-être implémenter des sessions VDI ou Windows Virtual Desktop pour aider vos employés à accéder aux données et applications d’entreprise à partir d’un appareil nonmanaté, d’un emplacement distant ou d’un scénario similaire.</span><span class="sxs-lookup"><span data-stu-id="36385-109">Depending on your organization's needs, you might need to implement VDI or Windows Virtual Desktop sessions to help your employees access corporate data and apps from an unmanaged device, remote location, or similar scenario.</span></span> <span data-ttu-id="36385-110">Avec Microsoft Defender pour le point de terminaison, vous pouvez surveiller ces machines virtuelles afin de vérifier les activités anormales.</span><span class="sxs-lookup"><span data-stu-id="36385-110">With Microsoft Defender for Endpoint, you can monitor these virtual machines for anomalous activity.</span></span>

 ## <a name="before-you-begin"></a><span data-ttu-id="36385-111">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="36385-111">Before you begin</span></span>
<span data-ttu-id="36385-112">Familiarisez-vous avec les considérations pour [les VDI non persistants.](/microsoft-365/security/defender-endpoint/configure-endpoints-vdi#onboard-non-persistent-virtual-desktop-infrastructure-vdi-devices-1)</span><span class="sxs-lookup"><span data-stu-id="36385-112">Familiarize yourself with the [considerations for non-persistent VDI](/microsoft-365/security/defender-endpoint/configure-endpoints-vdi#onboard-non-persistent-virtual-desktop-infrastructure-vdi-devices-1).</span></span> <span data-ttu-id="36385-113">Bien [que Windows Virtual Desktop](/azure/virtual-desktop/overview) ne fournisse pas d’options de non-persistance, il offre des moyens d’utiliser une image Windows de premier choix qui peut être utilisée pour mettre en service de nouveaux hôtes et redéployer des ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="36385-113">While [Windows Virtual Desktop](/azure/virtual-desktop/overview) doesn't provide non-persistence options, it does provide ways to use a golden Windows image that can be used to provision new hosts and redeploy machines.</span></span> <span data-ttu-id="36385-114">Cela augmente la sécurité dans l’environnement et a un impact sur les entrées créées et conservées dans le portail Microsoft Defender pour points de terminaison, ce qui réduit potentiellement la visibilité de vos analystes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="36385-114">This increases volatility in the environment and thus impacts what entries are created and maintained in the Microsoft Defender for Endpoint portal, potentially reducing visibility for your security analysts.</span></span>

> [!NOTE]
> <span data-ttu-id="36385-115">En fonction de votre choix de méthode d’intégration, les appareils peuvent apparaître dans le portail Microsoft Defender pour Endpoint comme :</span><span class="sxs-lookup"><span data-stu-id="36385-115">Depending on your choice of onboarding method, devices can appear in Microsoft Defender for Endpoint portal as either:</span></span> 
> - <span data-ttu-id="36385-116">Entrée unique pour chaque bureau virtuel</span><span class="sxs-lookup"><span data-stu-id="36385-116">Single entry for each virtual desktop</span></span> 
> - <span data-ttu-id="36385-117">Plusieurs entrées pour chaque bureau virtuel</span><span class="sxs-lookup"><span data-stu-id="36385-117">Multiple entries for each virtual desktop</span></span> 

<span data-ttu-id="36385-118">Microsoft recommande l’intégration Windows Virtual Desktop en tant qu’entrée unique par bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="36385-118">Microsoft recommends onboarding Windows Virtual Desktop as a single entry per virtual desktop.</span></span> <span data-ttu-id="36385-119">Cela garantit que l’expérience d’examen dans le portail Microsoft Defender Endpoint se trouve dans le contexte d’un appareil basé sur le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="36385-119">This ensures that the investigation experience in the Microsoft Defender Endpoint portal is in the context of one device based on the machine name.</span></span> <span data-ttu-id="36385-120">Les organisations qui suppriment et redéploient fréquemment des hôtes WVD doivent envisager fortement d’utiliser cette méthode, car elle empêche la création de plusieurs objets pour le même ordinateur dans le portail Microsoft Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="36385-120">Organizations that frequently delete and redeploy WVD hosts should strongly consider using this method as it prevents multiple objects for the same machine from being created in the Microsoft Defender for Endpoint portal.</span></span> <span data-ttu-id="36385-121">Cela peut semer la confusion lors de l’enquête sur les incidents.</span><span class="sxs-lookup"><span data-stu-id="36385-121">This can lead to confusion when investigating incidents.</span></span> <span data-ttu-id="36385-122">Pour les environnements de test ou non volatiles, vous pouvez choisir différemment.</span><span class="sxs-lookup"><span data-stu-id="36385-122">For test or non-volatile environments, you may opt to choose differently.</span></span> 

<span data-ttu-id="36385-123">Microsoft recommande d’ajouter le script d’intégration Microsoft Defender for Endpoint à l’image de qualité WVD.</span><span class="sxs-lookup"><span data-stu-id="36385-123">Microsoft recommends adding the Microsoft Defender for Endpoint onboarding script to the WVD golden image.</span></span> <span data-ttu-id="36385-124">De cette façon, vous pouvez vous assurer que ce script d’intégration s’exécute immédiatement au premier démarrage.</span><span class="sxs-lookup"><span data-stu-id="36385-124">This way, you can be sure that this onboarding script runs immediately at first boot.</span></span> <span data-ttu-id="36385-125">Il est exécuté en tant que script de démarrage au premier démarrage sur tous les ordinateurs WVD qui sont mis en service à partir de l’image WVD de premier niveau.</span><span class="sxs-lookup"><span data-stu-id="36385-125">It's executed as a startup script at first boot on all the WVD machines that are provisioned from the WVD golden image.</span></span> <span data-ttu-id="36385-126">Toutefois, si vous utilisez l’une des images de la galerie sans modification, placez le script dans un emplacement partagé et appelez-le à partir d’une stratégie de groupe locale ou de domaine.</span><span class="sxs-lookup"><span data-stu-id="36385-126">However, if you're using one of the gallery images without modification, place the script in a shared location and call it from either local or domain group policy.</span></span> 

> [!NOTE]
> <span data-ttu-id="36385-127">Le placement et la configuration du script de démarrage d’intégration VDI sur l’image de base WVD le configurent en tant que script de démarrage qui s’exécute au démarrage du WVD.</span><span class="sxs-lookup"><span data-stu-id="36385-127">The placement and configuration of the VDI onboarding startup script on the WVD golden image configures it as a startup script that runs when the WVD starts.</span></span> <span data-ttu-id="36385-128">Il n’est PAS recommandé d’intégrer l’image de qualité WVD réelle.</span><span class="sxs-lookup"><span data-stu-id="36385-128">It's NOT recommended to onboard the actual WVD golden image.</span></span> <span data-ttu-id="36385-129">Une autre considération est la méthode utilisée pour exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="36385-129">Another consideration is the method used to run the script.</span></span> <span data-ttu-id="36385-130">Il doit s’exécuter aussi tôt que possible dans le processus de démarrage/approvisionnement pour réduire le temps entre la mise à disposition de l’ordinateur pour la réception des sessions et l’intégration de l’appareil au service.</span><span class="sxs-lookup"><span data-stu-id="36385-130">It should run as early in the startup/provisioning process as possible to reduce the time between the machine being available to receive sessions and the device onboarding to the service.</span></span> <span data-ttu-id="36385-131">Les scénarios ci-dessous 1 & 2 prennent cela en compte.</span><span class="sxs-lookup"><span data-stu-id="36385-131">Below scenarios 1 & 2 take this into account.</span></span>

### <a name="scenarios"></a><span data-ttu-id="36385-132">Scénarios</span><span class="sxs-lookup"><span data-stu-id="36385-132">Scenarios</span></span>
<span data-ttu-id="36385-133">Il existe plusieurs façons d’intégrer un ordinateur hôte WVD :</span><span class="sxs-lookup"><span data-stu-id="36385-133">There are several ways to onboard a WVD host machine:</span></span>

- <span data-ttu-id="36385-134">Exécutez le script dans l’image de choix (ou à partir d’un emplacement partagé) au démarrage.</span><span class="sxs-lookup"><span data-stu-id="36385-134">Run the script in the golden image (or from a shared location) during startup.</span></span>
- <span data-ttu-id="36385-135">Utilisez un outil de gestion pour exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="36385-135">Use a management tool to run the script.</span></span>

#### <a name="scenario-1-using-local-group-policy"></a><span data-ttu-id="36385-136">*Scénario 1 : utilisation d’une stratégie de groupe locale*</span><span class="sxs-lookup"><span data-stu-id="36385-136">*Scenario 1: Using local group policy*</span></span>
<span data-ttu-id="36385-137">Ce scénario nécessite de placer le script dans une image de base et utilise la stratégie de groupe locale pour s’exécuter au début du processus de démarrage.</span><span class="sxs-lookup"><span data-stu-id="36385-137">This scenario requires placing the script in a golden image and uses local group policy to run early in the boot process.</span></span>

<span data-ttu-id="36385-138">Utilisez les instructions de l’outil Intégrer les périphériques [VDI (Virtual Desktop Infrastructure) non persistants.](configure-endpoints-vdi.md#onboard-the-non-persistent-virtual-desktop-infrastructure-vdi-devices)</span><span class="sxs-lookup"><span data-stu-id="36385-138">Use the instructions in [Onboard the non-persistent virtual desktop infrastructure (VDI) devices](configure-endpoints-vdi.md#onboard-the-non-persistent-virtual-desktop-infrastructure-vdi-devices).</span></span>

<span data-ttu-id="36385-139">Suivez les instructions pour une entrée unique pour chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="36385-139">Follow the instructions for a single entry for each device.</span></span>

#### <a name="scenario-2-using-domain-group-policy"></a><span data-ttu-id="36385-140">*Scénario 2 : utilisation de la stratégie de groupe de domaine*</span><span class="sxs-lookup"><span data-stu-id="36385-140">*Scenario 2: Using domain group policy*</span></span>
<span data-ttu-id="36385-141">Ce scénario utilise un script central et l’exécute à l’aide d’une stratégie de groupe basée sur un domaine.</span><span class="sxs-lookup"><span data-stu-id="36385-141">This scenario uses a centrally located script and runs it using a domain-based group policy.</span></span> <span data-ttu-id="36385-142">Vous pouvez également placer le script dans l’image d’or et l’exécuter de la même manière.</span><span class="sxs-lookup"><span data-stu-id="36385-142">You can also place the script in the golden image and run it in the same way.</span></span>

<span data-ttu-id="36385-143">**Télécharger le fichier WindowsDefenderATPOnboardingPackage.zip à partir du Centre de Windows Defender de sécurité**</span><span class="sxs-lookup"><span data-stu-id="36385-143">**Download the WindowsDefenderATPOnboardingPackage.zip file from the Windows Defender Security Center**</span></span>

1. <span data-ttu-id="36385-144">Ouvrir le fichier de configuration du package VDI .zip (WindowsDefenderATPOnboardingPackage.zip)</span><span class="sxs-lookup"><span data-stu-id="36385-144">Open the VDI configuration package .zip file (WindowsDefenderATPOnboardingPackage.zip)</span></span>  

    1. <span data-ttu-id="36385-145">Dans le Centre de sécurité Microsoft Defender de navigation, sélectionnez **Paramètres**  >  **intégration.**</span><span class="sxs-lookup"><span data-stu-id="36385-145">In the Microsoft Defender Security Center navigation pane, select **Settings** > **Onboarding**.</span></span> 
    1. <span data-ttu-id="36385-146">Sélectionnez Windows 10 comme système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="36385-146">Select Windows 10 as the operating system.</span></span> 
    1. <span data-ttu-id="36385-147">Dans le **champ Méthode de** déploiement, sélectionnez les scripts d’intégration VDI pour les points de terminaison non persistants.</span><span class="sxs-lookup"><span data-stu-id="36385-147">In the **Deployment method** field, select VDI onboarding scripts for non-persistent endpoints.</span></span> 
    1. <span data-ttu-id="36385-148">Cliquez **sur Télécharger le package** et enregistrez .zip fichier.</span><span class="sxs-lookup"><span data-stu-id="36385-148">Click **Download package** and save the .zip file.</span></span> 

2. <span data-ttu-id="36385-149">Extrayez le contenu du .zip vers un emplacement partagé en lecture seule accessible par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="36385-149">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the device.</span></span> <span data-ttu-id="36385-150">Vous devez avoir un dossier appelé **OptionalParamsPolicy** et les fichiers **WindowsDefenderATPOnboardingScript.cmd** **etOnboard-NonPersistentMachine.ps1**.</span><span class="sxs-lookup"><span data-stu-id="36385-150">You should have a folder called **OptionalParamsPolicy** and the files **WindowsDefenderATPOnboardingScript.cmd** and **Onboard-NonPersistentMachine.ps1**.</span></span>

<span data-ttu-id="36385-151">**Utiliser la console de gestion des stratégies de groupe pour exécuter le script au démarrage de la machine virtuelle**</span><span class="sxs-lookup"><span data-stu-id="36385-151">**Use Group Policy management console to run the script when the virtual machine starts**</span></span>

1. <span data-ttu-id="36385-152">Ouvrez la Console de gestion des stratégies de groupe (GPMC), cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="36385-152">Open the Group Policy Management Console (GPMC), right-click the Group Policy Object (GPO) you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="36385-153">Dans l’Éditeur de gestion des stratégies de groupe, go to **Computer configuration** \> **Preferences** \> **Control panel settings**.</span><span class="sxs-lookup"><span data-stu-id="36385-153">In the Group Policy Management Editor, go to **Computer configuration** \> **Preferences** \> **Control panel settings**.</span></span> 

3. <span data-ttu-id="36385-154">Cliquez avec le bouton droit **sur Tâches programmées,** **cliquez** sur Nouveau, puis sur **Tâche** immédiate (au moins Windows 7).</span><span class="sxs-lookup"><span data-stu-id="36385-154">Right-click **Scheduled tasks**, click **New**, and then click **Immediate Task** (At least Windows 7).</span></span> 

4. <span data-ttu-id="36385-155">Dans la fenêtre Tâche qui s’ouvre, allez dans **l’onglet** Général. Sous **Options de sécurité,** cliquez **sur Modifier l’utilisateur ou le groupe,** puis tapez SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="36385-155">In the Task window that opens, go to the **General** tab. Under **Security options** click **Change User or Group** and type SYSTEM.</span></span> <span data-ttu-id="36385-156">Cliquez **sur Vérifier les noms,** puis sur OK.</span><span class="sxs-lookup"><span data-stu-id="36385-156">Click **Check Names** and then click OK.</span></span> <span data-ttu-id="36385-157">NT AUTHORITY\SYSTEM apparaît en tant que compte d’utilisateur que la tâche exécutera.</span><span class="sxs-lookup"><span data-stu-id="36385-157">NT AUTHORITY\SYSTEM appears as the user account the task will run as.</span></span> 

5. <span data-ttu-id="36385-158">Sélectionnez **Exécuter, que l’utilisateur soit** connecté ou non et cochez la case Exécuter avec **les privilèges les plus élevés.**</span><span class="sxs-lookup"><span data-stu-id="36385-158">Select **Run whether user is logged on or not** and check the **Run with highest privileges** check box.</span></span> 

6. <span data-ttu-id="36385-159">Go to the **Actions** tab and click **New**.</span><span class="sxs-lookup"><span data-stu-id="36385-159">Go to the **Actions** tab and click **New**.</span></span> <span data-ttu-id="36385-160">**Assurez-vous que démarrer un programme** est sélectionné dans le champ Action.</span><span class="sxs-lookup"><span data-stu-id="36385-160">Ensure that **Start a program** is selected in the Action field.</span></span> <span data-ttu-id="36385-161">Entrez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="36385-161">Enter the following:</span></span> 

   `Action = "Start a program"`

   `Program/Script = C:\WINDOWS\system32\WindowsPowerShell\v1.0\powershell.exe`

   `Add Arguments (optional) = -ExecutionPolicy Bypass -command "& \\Path\To\Onboard-NonPersistentMachine.ps1"`

   <span data-ttu-id="36385-162">Ensuite, **sélectionnez OK** et fermez toutes les fenêtres GPMC ouvertes.</span><span class="sxs-lookup"><span data-stu-id="36385-162">Then select **OK** and close any open GPMC windows.</span></span>

#### <a name="scenario-3-onboarding-using-management-tools"></a><span data-ttu-id="36385-163">*Scénario 3 : intégration à l’aide des outils de gestion*</span><span class="sxs-lookup"><span data-stu-id="36385-163">*Scenario 3: Onboarding using management tools*</span></span>

<span data-ttu-id="36385-164">Si vous envisagez de gérer vos ordinateurs à l’aide d’un outil de gestion, vous pouvez intégrer des appareils Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="36385-164">If you plan to manage your machines using a management tool, you can onboard devices with Microsoft Endpoint Configuration Manager.</span></span>

<span data-ttu-id="36385-165">Pour plus d’informations, [voir Onboard Windows 10 à l’aide de Configuration Manager.](configure-endpoints-sccm.md)</span><span class="sxs-lookup"><span data-stu-id="36385-165">For more information, see [Onboard Windows 10 devices using Configuration Manager](configure-endpoints-sccm.md).</span></span>

> [!WARNING]
> <span data-ttu-id="36385-166">Si vous envisagez d’utiliser les règles de réduction de la [surface](attack-surface-reduction.md)d’attaque, notez que la règle « Bloquer les créations de processus provenant de commandes[PSExec](attack-surface-reduction.md#block-process-creations-originating-from-psexec-and-wmi-commands)et WMI » ne doit pas être utilisée, car cette règle est incompatible avec la gestion via Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="36385-166">If you plan to use [Attack Surface reduction Rules](attack-surface-reduction.md), note that the rule “[Block process creations originating from PSExec and WMI commands](attack-surface-reduction.md#block-process-creations-originating-from-psexec-and-wmi-commands)" should not be used, because that rule is incompatible with management through Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="36385-167">La règle bloque les commandes WMI que le client Configuration Manager utilise pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="36385-167">The rule blocks WMI commands that the Configuration Manager client uses to function correctly.</span></span> 

> [!TIP]
> <span data-ttu-id="36385-168">Après avoir intégré l’appareil, vous pouvez choisir d’exécuter un test de détection pour vérifier que l’appareil est correctement intégré au service.</span><span class="sxs-lookup"><span data-stu-id="36385-168">After onboarding the device, you can choose to run a detection test to verify that the device is properly onboarded to the service.</span></span> <span data-ttu-id="36385-169">Pour plus d’informations, voir Exécuter un test de détection sur un appareil [Microsoft Defender pour point de terminaison nouvellement intégré.](run-detection-test.md)</span><span class="sxs-lookup"><span data-stu-id="36385-169">For more information, see [Run a detection test on a newly onboarded Microsoft Defender for Endpoint device](run-detection-test.md).</span></span> 

#### <a name="tagging-your-machines-when-building-your-golden-image"></a><span data-ttu-id="36385-170">Marquage de vos ordinateurs lors de la création de votre image de qualité</span><span class="sxs-lookup"><span data-stu-id="36385-170">Tagging your machines when building your golden image</span></span> 

<span data-ttu-id="36385-171">Dans le cadre de votre intégration, vous pouvez envisager de définir une balise d’ordinateur pour différencier plus facilement les ordinateurs WVD dans le Centre de sécurité Microsoft.</span><span class="sxs-lookup"><span data-stu-id="36385-171">As part of your onboarding, you may want to consider setting a machine tag to can differentiate WVD machines more easily in the Microsoft Security Center.</span></span> <span data-ttu-id="36385-172">Pour plus d’informations, voir [Ajouter des balises de périphérique en définition d’une valeur de clé de Registre.](machine-tags.md#add-device-tags-by-setting-a-registry-key-value)</span><span class="sxs-lookup"><span data-stu-id="36385-172">For more information, see [Add device tags by setting a registry key value](machine-tags.md#add-device-tags-by-setting-a-registry-key-value).</span></span> 

#### <a name="other-recommended-configuration-settings"></a><span data-ttu-id="36385-173">Autres paramètres de configuration recommandés</span><span class="sxs-lookup"><span data-stu-id="36385-173">Other recommended configuration settings</span></span> 

<span data-ttu-id="36385-174">Lorsque vous construisez votre image de premier niveau, vous pouvez également configurer les paramètres de protection initiaux.</span><span class="sxs-lookup"><span data-stu-id="36385-174">When building your golden image, you may want to configure initial protection settings as well.</span></span> <span data-ttu-id="36385-175">Pour plus d’informations, [voir autres paramètres de configuration recommandés.](configure-endpoints-gp.md#other-recommended-configuration-settings)</span><span class="sxs-lookup"><span data-stu-id="36385-175">For more information, see [Other recommended configuration settings](configure-endpoints-gp.md#other-recommended-configuration-settings).</span></span> 

<span data-ttu-id="36385-176">En outre, si vous utilisez des profils utilisateur FSlogix, nous vous recommandons d’exclure les fichiers suivants de la protection toujours en cours :</span><span class="sxs-lookup"><span data-stu-id="36385-176">Also, if you're using FSlogix user profiles, we recommend you exclude the following files from always-on protection:</span></span> 

<span data-ttu-id="36385-177">**Exclure des fichiers :**</span><span class="sxs-lookup"><span data-stu-id="36385-177">**Exclude Files:**</span></span> 

`%ProgramFiles%\FSLogix\Apps\frxdrv.sys`

`%ProgramFiles%\FSLogix\Apps\frxdrvvt.sys`

`%ProgramFiles%\FSLogix\Apps\frxccd.sys`

`%TEMP%\*.VHD`

`%TEMP%\*.VHDX`

`%Windir%\TEMP\*.VHD`

`%Windir%\TEMP\*.VHDX`

`\\storageaccount.file.core.windows.net\share\*\*.VHD`

`\\storageaccount.file.core.windows.net\share\*\*.VHDX`

<span data-ttu-id="36385-178">**Exclure des processus :**</span><span class="sxs-lookup"><span data-stu-id="36385-178">**Exclude Processes:**</span></span>

`%ProgramFiles%\FSLogix\Apps\frxccd.exe`

`%ProgramFiles%\FSLogix\Apps\frxccds.exe`

`%ProgramFiles%\FSLogix\Apps\frxsvc.exe`

#### <a name="licensing-requirements"></a><span data-ttu-id="36385-179">Conditions d'octroi de licence</span><span class="sxs-lookup"><span data-stu-id="36385-179">Licensing requirements</span></span> 

<span data-ttu-id="36385-180">Remarque sur la gestion des licences : lors de l’utilisation de Windows 10 Entreprise multisesse session, en fonction de vos besoins, vous pouvez choisir d’avoir tous les utilisateurs sous licence via Microsoft Defender pour le point de terminaison (par utilisateur), Windows Enterprise E5, Microsoft 365 Security ou Microsoft 365 E5, ou avoir la VM sous licence via Azure Defender.</span><span class="sxs-lookup"><span data-stu-id="36385-180">Note on licensing: When using Windows 10 Enterprise multi-session, depending on your requirements, you can choose to either have all users licensed through Microsoft Defender for Endpoint (per user), Windows Enterprise E5, Microsoft 365 Security, or Microsoft 365 E5, or have the VM licensed through Azure Defender.</span></span>
<span data-ttu-id="36385-181">Les conditions de licence pour Microsoft Defender pour le point de terminaison se trouvent dans : [Exigences de licence.](minimum-requirements.md#licensing-requirements)</span><span class="sxs-lookup"><span data-stu-id="36385-181">Licensing requirements for Microsoft Defender for endpoint can be found at: [Licensing requirements](minimum-requirements.md#licensing-requirements).</span></span>

#### <a name="related-links"></a><span data-ttu-id="36385-182">Liens connexes</span><span class="sxs-lookup"><span data-stu-id="36385-182">Related Links</span></span>

[<span data-ttu-id="36385-183">Ajouter des exclusions pour Microsoft Defender à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="36385-183">Add exclusions for Microsoft Defender by using PowerShell</span></span>](/azure/architecture/example-scenario/wvd/windows-virtual-desktop-fslogix#add-exclusions-for-windows-defender-by-using-powershell)
