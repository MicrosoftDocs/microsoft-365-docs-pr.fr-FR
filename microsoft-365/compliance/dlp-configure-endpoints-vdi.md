---
title: Périphériques VDI (Virtual Desktop Infrastructure) non persistants
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
description: Déployez le package de configuration sur un périphérique VDI (Virtual Desktop Infrastructure) de sorte qu’il soit intégré au service de protection contre la perte de données de point de terminaison Microsoft 365.
ms.openlocfilehash: ce5ad0ba6af3e18a6f6c53e1860fc47a77c38770
ms.sourcegitcommit: 6647055154002c7d3b8f7ce25ad53c9636bc8066
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2020
ms.locfileid: "48769417"
---
# <a name="onboard-non-persistent-virtual-desktop-infrastructure-vdi-devices"></a><span data-ttu-id="a8bc2-103">Périphériques VDI (Virtual Desktop Infrastructure) non persistants</span><span class="sxs-lookup"><span data-stu-id="a8bc2-103">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>

<span data-ttu-id="a8bc2-104">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a8bc2-104">**Applies to:**</span></span>
- [<span data-ttu-id="a8bc2-105">Microsoft 365 protection contre la perte de données (DLP)</span><span class="sxs-lookup"><span data-stu-id="a8bc2-105">Microsoft 365 Endpoint data loss prevention (DLP)</span></span>](/microsoft-365/compliance/endpoint-dlp-learn-about)

- <span data-ttu-id="a8bc2-106">Périphériques VDI (Virtual Desktop Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="a8bc2-106">Virtual desktop infrastructure (VDI) devices</span></span>

>[!WARNING]
> <span data-ttu-id="a8bc2-107">Microsoft 365 la prise en charge de la protection contre la perte de données pour Windows Virtual Desktop prend en charge les scénarios à session unique.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-107">Microsoft 365 Endpoint data loss prevention support for Windows Virtual Desktop supports single session scenarios.</span></span> <span data-ttu-id="a8bc2-108">Les scénarios multisession sur le bureau virtuel Windows ne sont actuellement pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-108">Multi-session scenarios on Windows Virtual Desktop are currently not supported.</span></span>

## <a name="onboard-vdi-devices"></a><span data-ttu-id="a8bc2-109">Périphériques VDI intégrés</span><span class="sxs-lookup"><span data-stu-id="a8bc2-109">Onboard VDI devices</span></span>

<span data-ttu-id="a8bc2-110">La protection contre la perte de données de point de terminaison Microsoft 365 prend en charge l’intégration de session VDI non persistante.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-110">Microsoft 365 Endpoint data loss prevention supports non-persistent VDI session onboarding.</span></span> 

>[!Note]
><span data-ttu-id="a8bc2-111">Pour intégrer des sessions VDI non persistantes, les périphériques VDI doivent être sur Windows 10 1809 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-111">To onboard non-persistent VDI sessions, VDI devices must be on Windows 10 1809 or higher.</span></span>

<span data-ttu-id="a8bc2-112">Il peut être associé à des défis lors de l’intégration de VDIs.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-112">There might be associated challenges when onboarding VDIs.</span></span> <span data-ttu-id="a8bc2-113">Les problèmes suivants sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="a8bc2-113">The following are typical challenges for this scenario:</span></span>

- <span data-ttu-id="a8bc2-114">Intégration instantanée précoce d’une session courte, qui doit être intégrée à la protection contre la perte de données du point de terminaison de Microsoft 365 avant la mise en service réelle.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-114">Instant early onboarding of a short-lived sessions, which must be onboarded to  Microsoft 365 Endpoint data loss prevention prior to the actual provisioning.</span></span>
- <span data-ttu-id="a8bc2-115">Le nom de l’appareil est généralement réutilisé pour les nouvelles sessions.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-115">The device name is typically reused for new sessions.</span></span>

<span data-ttu-id="a8bc2-116">Les périphériques VDI peuvent apparaître dans le centre de conformité Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="a8bc2-116">VDI devices can appear in the Microsoft 365 Compliance center as either:</span></span>

- <span data-ttu-id="a8bc2-117">Entrée unique pour chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-117">Single entry for each device.</span></span>  
<span data-ttu-id="a8bc2-118">Notez que dans ce cas, le *même* nom de périphérique doit être configuré lors de la création de la session, par exemple à l’aide d’un fichier de réponses sans assistance.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-118">Note that in this case, the *same* device name must be configured when the session is created, for example using an unattended answer file.</span></span>
- <span data-ttu-id="a8bc2-119">Plusieurs entrées pour chaque appareil-un pour chaque session.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-119">Multiple entries for each device - one for each session.</span></span>

<span data-ttu-id="a8bc2-120">Les étapes suivantes vous guident à travers le processus d’intégration des périphériques VDI et mettent en évidence les étapes d’une ou plusieurs entrées.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-120">The following steps will guide you through onboarding VDI devices and will highlight steps for single and multiple entries.</span></span>

>[!WARNING]
> <span data-ttu-id="a8bc2-121">Pour les environnements pour lesquels il existe des configurations de ressources faibles, la procédure de démarrage VDI peut ralentir l’intégration de la protection contre la perte de données de point de terminaison de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-121">For environments where there are low resource configurations, the VDI boot procedure might slow the Microsoft 365 Endpoint data loss prevention onboarding.</span></span> 

1.  <span data-ttu-id="a8bc2-122">Ouvrez le fichier. zip du package de configuration VDI ( *DeviceCompliancePackage.zip* ) que vous avez téléchargé à partir de l’Assistant d’intégration de service.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-122">Open the VDI configuration package .zip file ( *DeviceCompliancePackage.zip* ) that you downloaded from the service onboarding wizard.</span></span>

2.  <span data-ttu-id="a8bc2-123">Dans le volet de navigation, sélectionnez **paramètres** d’intégration de l'  >  **appareil**  >  **Onboarding** .</span><span class="sxs-lookup"><span data-stu-id="a8bc2-123">In the navigation pane, select **Settings** > **Device onboarding** > **Onboarding** .</span></span>

3. <span data-ttu-id="a8bc2-124">Dans le champ **méthode de déploiement** , sélectionnez **scripts d’intégration VDI pour les points de terminaison non persistants** .</span><span class="sxs-lookup"><span data-stu-id="a8bc2-124">In the **Deployment method** field, select **VDI onboarding scripts for non-persistent endpoints** .</span></span>

5. <span data-ttu-id="a8bc2-125">Cliquez sur **Télécharger le package** et enregistrez le fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-125">Click **Download package** and save the .zip file.</span></span>

6. <span data-ttu-id="a8bc2-126">Copiez les fichiers à partir du dossier DeviceCompliancePackage extrait du fichier. zip dans l' `golden/master` image sous le chemin d’accès `C:\WINDOWS\System32\GroupPolicy\Machine\Scripts\Startup` .</span><span class="sxs-lookup"><span data-stu-id="a8bc2-126">Copy the files from the DeviceCompliancePackage folder extracted from the .zip file into the `golden/master` image under the path `C:\WINDOWS\System32\GroupPolicy\Machine\Scripts\Startup`.</span></span> 

7. <span data-ttu-id="a8bc2-127">Si vous n’implémentez pas une seule entrée pour chaque périphérique, copiez DeviceComplianceOnboardingScript. cmd.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-127">If you are not implementing a single entry for each device, copy DeviceComplianceOnboardingScript.cmd.</span></span>

8. <span data-ttu-id="a8bc2-128">Si vous implémentez une entrée unique pour chaque périphérique, copiez les Onboard-NonPersistentMachine.ps1 et DeviceComplianceOnboardingScript. cmd.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-128">If you are implementing a single entry for each device, copy both Onboard-NonPersistentMachine.ps1 and DeviceComplianceOnboardingScript.cmd.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="a8bc2-129">Si le dossier n’apparaît pas `C:\WINDOWS\System32\GroupPolicy\Machine\Scripts\Startup` , il est peut-être masqué.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-129">If you don't see the `C:\WINDOWS\System32\GroupPolicy\Machine\Scripts\Startup` folder, it might be hidden.</span></span> <span data-ttu-id="a8bc2-130">Vous devez choisir l’option **afficher les fichiers et les dossiers cachés** dans l’Explorateur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-130">You'll need to choose the **Show hidden files and folders** option from File Explorer.</span></span>

9. <span data-ttu-id="a8bc2-131">Ouvrez une fenêtre d’éditeur de stratégie de groupe locale et accédez à configuration de l' **ordinateur**  >  scripts de **Paramètres Windows** -  >  **Scripts**  >  **démarrage** .</span><span class="sxs-lookup"><span data-stu-id="a8bc2-131">Open a Local Group Policy Editor window and navigate to **Computer Configuration** > **Windows Settings** > **Scripts** > **Startup** .</span></span>

   > [!NOTE]
   > <span data-ttu-id="a8bc2-132">La stratégie de groupe de domaine peut également être utilisée pour l’intégration d’appareils VDI non persistants.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-132">Domain Group Policy may also be used for onboarding non-persistent VDI devices.</span></span>

4. <span data-ttu-id="a8bc2-133">En fonction de la méthode que vous souhaitez mettre en œuvre, suivez les étapes appropriées :</span><span class="sxs-lookup"><span data-stu-id="a8bc2-133">Depending on the method you'd like to implement, follow the appropriate steps:</span></span>

   <span data-ttu-id="a8bc2-134">**Pour une entrée unique pour chaque appareil**</span><span class="sxs-lookup"><span data-stu-id="a8bc2-134">**For single entry for each device**</span></span>
   
   <span data-ttu-id="a8bc2-135">Sélectionnez l’onglet **scripts PowerShell** , puis cliquez sur **Ajouter** (l’Explorateur Windows s’ouvre directement dans le chemin d’accès où vous avez copié le script d’intégration plus haut).</span><span class="sxs-lookup"><span data-stu-id="a8bc2-135">Select the **PowerShell Scripts** tab, then click **Add** (Windows Explorer will open directly in the path where you copied the onboarding script earlier).</span></span> <span data-ttu-id="a8bc2-136">Naviguez jusqu’à script PowerShell d’intégration `Onboard-NonPersistentMachine.ps1` .</span><span class="sxs-lookup"><span data-stu-id="a8bc2-136">Navigate to onboarding PowerShell script `Onboard-NonPersistentMachine.ps1`.</span></span>
   
   <span data-ttu-id="a8bc2-137">**Pour plusieurs entrées pour chaque périphérique** :</span><span class="sxs-lookup"><span data-stu-id="a8bc2-137">**For multiple entries for each device** :</span></span>
   
   <span data-ttu-id="a8bc2-138">Sélectionnez l’onglet **scripts** , puis cliquez sur **Ajouter** (l’Explorateur Windows s’ouvre directement dans le chemin d’accès où vous avez copié le script d’intégration plus haut).</span><span class="sxs-lookup"><span data-stu-id="a8bc2-138">Select the **Scripts** tab, then click **Add** (Windows Explorer will open directly in the path where you copied the onboarding script earlier).</span></span> <span data-ttu-id="a8bc2-139">Naviguez jusqu’au script d’intégration `DeviceComplianceOnboardingScript.cmd` .</span><span class="sxs-lookup"><span data-stu-id="a8bc2-139">Navigate to the onboarding bash script `DeviceComplianceOnboardingScript.cmd`.</span></span>

5. <span data-ttu-id="a8bc2-140">Testez votre solution :</span><span class="sxs-lookup"><span data-stu-id="a8bc2-140">Test your solution:</span></span>

   1. <span data-ttu-id="a8bc2-141">Créez un pool avec un seul appareil.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-141">Create a pool with one device.</span></span>
      
   1. <span data-ttu-id="a8bc2-142">Connectez-vous à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-142">Logon to device.</span></span>
      
   1. <span data-ttu-id="a8bc2-143">Déconnexion de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-143">Logoff from device.</span></span>

   1. <span data-ttu-id="a8bc2-144">Connectez-vous à l’appareil avec un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-144">Logon to device with another user.</span></span>
      
   1. <span data-ttu-id="a8bc2-145">**Pour une entrée unique pour chaque appareil** : Vérifiez une seule entrée dans le centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-145">**For single entry for each device** : Check only one entry in Microsoft Defender Security Center.</span></span><br>
      <span data-ttu-id="a8bc2-146">**Pour plusieurs entrées pour chaque périphérique** : Vérifiez plusieurs entrées dans le centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-146">**For multiple entries for each device** : Check multiple entries in Microsoft Defender Security Center.</span></span>

6. <span data-ttu-id="a8bc2-147">Cliquez sur **liste des périphériques** dans le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-147">Click **Devices list** on the Navigation pane.</span></span>

7. <span data-ttu-id="a8bc2-148">Utilisez la fonction de recherche en entrant le nom du périphérique et sélectionnez **appareil** comme type de recherche.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-148">Use the search function by entering the device name and select **Device** as search type.</span></span>

## <a name="updating-non-persistent-virtual-desktop-infrastructure-vdi-images"></a><span data-ttu-id="a8bc2-149">Mise à jour des images VDI (Virtual Desktop Infrastructure) non persistantes</span><span class="sxs-lookup"><span data-stu-id="a8bc2-149">Updating non-persistent virtual desktop infrastructure (VDI) images</span></span>
<span data-ttu-id="a8bc2-150">En guise de meilleure pratique, nous vous recommandons d’utiliser les outils de maintenance hors ligne pour corriger les images de référence/des images principales.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-150">As a best practice, we recommend using offline servicing tools to patch golden/master images.</span></span><br>
<span data-ttu-id="a8bc2-151">Par exemple, vous pouvez utiliser les commandes ci-dessous pour installer une mise à jour alors que l’image reste en mode hors connexion :</span><span class="sxs-lookup"><span data-stu-id="a8bc2-151">For example, you can use the below commands to install an update while the image remains offline:</span></span>

```console
DISM /Mount-image /ImageFile:"D:\Win10-1909.vhdx" /index:1 /MountDir:"C:\Temp\OfflineServicing" 
DISM /Image:"C:\Temp\OfflineServicing" /Add-Package /Packagepath:"C:\temp\patch\windows10.0-kb4541338-x64.msu"
DISM /Unmount-Image /MountDir:"C:\Temp\OfflineServicing" /commit
```

<span data-ttu-id="a8bc2-152">Pour plus d’informations sur les commandes DISM et la maintenance hors connexion, reportez-vous aux articles suivants :</span><span class="sxs-lookup"><span data-stu-id="a8bc2-152">For more information on DISM commands and offline servicing, please refer to the articles below:</span></span>
- [<span data-ttu-id="a8bc2-153">Modifier une image Windows à l’aide de DISM</span><span class="sxs-lookup"><span data-stu-id="a8bc2-153">Modify a Windows image using DISM</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/mount-and-modify-a-windows-image-using-dism)
- [<span data-ttu-id="a8bc2-154">Options de Command-Line de gestion des images DISM</span><span class="sxs-lookup"><span data-stu-id="a8bc2-154">DISM Image Management Command-Line Options</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/dism-image-management-command-line-options-s14)
- [<span data-ttu-id="a8bc2-155">Réduire la taille du magasin de composants dans une image Windows hors connexion</span><span class="sxs-lookup"><span data-stu-id="a8bc2-155">Reduce the Size of the Component Store in an Offline Windows Image</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/reduce-the-size-of-the-component-store-in-an-offline-windows-image)

<span data-ttu-id="a8bc2-156">Si la maintenance hors connexion n’est pas une option viable pour votre environnement VDI non persistant, les étapes suivantes doivent être prises pour garantir la cohérence et l’intégrité du capteur :</span><span class="sxs-lookup"><span data-stu-id="a8bc2-156">If offline servicing is not a viable option for your non-persistent VDI environment, the following steps should be taken to ensure consistency and sensor health:</span></span>

1. <span data-ttu-id="a8bc2-157">Après le démarrage de l’image principale pour la maintenance en ligne ou la mise à jour corrective, exécutez un script par débarquement pour désactiver le capteur de protection contre la perte de données de point de terminaison de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-157">After booting the master image for online servicing or patching, run an offboarding script to turn off the Microsoft 365 Endpoint data loss prevention sensor.</span></span> <span data-ttu-id="a8bc2-158">Pour plus d’informations, consultez [la rubrique débarquement Devices using a local script](dlp-configure-endpoints-script.md#offboard-devices-using-a-local-script).</span><span class="sxs-lookup"><span data-stu-id="a8bc2-158">For more information, see [Offboard devices using a local script](dlp-configure-endpoints-script.md#offboard-devices-using-a-local-script).</span></span>

2. <span data-ttu-id="a8bc2-159">Assurez-vous que le capteur est arrêté en exécutant la commande ci-dessous dans une fenêtre CMD :</span><span class="sxs-lookup"><span data-stu-id="a8bc2-159">Ensure the sensor is stopped by running the command below in a CMD window:</span></span>

   ```console
   sc query sense
   ```

3. <span data-ttu-id="a8bc2-160">Effectuer la maintenance de l’image selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-160">Service the image as needed.</span></span>

4. <span data-ttu-id="a8bc2-161">Exécutez les commandes ci-dessous en utilisant PsExec.exe (qui peut être téléchargé à partir du https://download.sysinternals.com/files/PSTools.zip) pour nettoyer le contenu du dossier Cyber que le capteur a pu accumuler depuis le démarrage) :</span><span class="sxs-lookup"><span data-stu-id="a8bc2-161">Run the below commands using PsExec.exe (which can be downloaded from https://download.sysinternals.com/files/PSTools.zip) to cleanup the cyber folder contents that the sensor may have accumulated since boot:</span></span>

    ```console
    PsExec.exe -s cmd.exe
    cd "C:\ProgramData\Microsoft\Windows Defender Advanced Threat Protection\Cyber"
    del *.* /f /s /q
    REG DELETE “HKLM\SOFTWARE\Microsoft\Windows Advanced Threat Protection" /v senseGuid /f
    exit
    ```

5. <span data-ttu-id="a8bc2-162">Ré-scellez l’image Golden/Master comme vous le feriez normalement.</span><span class="sxs-lookup"><span data-stu-id="a8bc2-162">Re-seal the golden/master image as you normally would.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8bc2-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8bc2-163">Related topics</span></span>
- [<span data-ttu-id="a8bc2-164">Périphériques Windows 10 embarqués à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="a8bc2-164">Onboard Windows 10 devices using Group Policy</span></span>](dlp-configure-endpoints-gp.md)
- [<span data-ttu-id="a8bc2-165">Appareils intégrés Windows 10 à l’aide du gestionnaire de configuration de point de terminaison Microsoft</span><span class="sxs-lookup"><span data-stu-id="a8bc2-165">Onboard Windows 10 devices using Microsoft Endpoint Configuration Manager</span></span>](dlp-configure-endpoints-sccm.md)
- [<span data-ttu-id="a8bc2-166">Périphériques Windows 10 intégrés à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="a8bc2-166">Onboard Windows 10 devices using Mobile Device Management tools</span></span>](dlp-configure-endpoints-mdm.md)
- [<span data-ttu-id="a8bc2-167">Périphériques Windows 10 embarqués à l’aide d’un script local</span><span class="sxs-lookup"><span data-stu-id="a8bc2-167">Onboard Windows 10 devices using a local script</span></span>](dlp-configure-endpoints-script.md)
- [<span data-ttu-id="a8bc2-168">Résoudre les problèmes d’intégration de la protection avancée contre les menaces Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="a8bc2-168">Troubleshoot Microsoft Defender Advanced Threat Protection onboarding issues</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding)
