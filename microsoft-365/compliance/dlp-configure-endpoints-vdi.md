---
title: Intégrer les ordinateurs virtuels d’infrastructure de bureau virtuel (VDI) non persistants.
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
description: Déployez le package de configuration sur un appareil VDI (Virtual Desktop Infrastructure) afin qu’il soit intégré au service de protection contre la perte de données de point de terminaison Microsoft 365.
ms.openlocfilehash: 2a62de6c238c1f681bde8a9bf25ecd596a10d390
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50917950"
---
# <a name="onboard-non-persistent-virtual-desktop-infrastructure-vdi-devices"></a><span data-ttu-id="8091f-103">Intégrer les ordinateurs virtuels d’infrastructure de bureau virtuel (VDI) non persistants.</span><span class="sxs-lookup"><span data-stu-id="8091f-103">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>

<span data-ttu-id="8091f-104">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8091f-104">**Applies to:**</span></span>
- [<span data-ttu-id="8091f-105">Protection contre la perte de données de point de terminaison Microsoft 365 (DLP)</span><span class="sxs-lookup"><span data-stu-id="8091f-105">Microsoft 365 Endpoint data loss prevention (DLP)</span></span>](./endpoint-dlp-learn-about.md)

- <span data-ttu-id="8091f-106">Périphériques VDI (Virtual Desktop Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="8091f-106">Virtual desktop infrastructure (VDI) devices</span></span>

>[!WARNING]
> <span data-ttu-id="8091f-107">La prise en charge de la protection contre la perte de données de point de terminaison Microsoft 365 pour Windows Virtual Desktop prend en charge les scénarios de session unique.</span><span class="sxs-lookup"><span data-stu-id="8091f-107">Microsoft 365 Endpoint data loss prevention support for Windows Virtual Desktop supports single session scenarios.</span></span> <span data-ttu-id="8091f-108">Les scénarios à sessions multiples sur Windows Virtual Desktop ne sont actuellement pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8091f-108">Multi-session scenarios on Windows Virtual Desktop are currently not supported.</span></span>

## <a name="onboard-vdi-devices"></a><span data-ttu-id="8091f-109">Appareils VDI intégrés</span><span class="sxs-lookup"><span data-stu-id="8091f-109">Onboard VDI devices</span></span>

<span data-ttu-id="8091f-110">La protection contre la perte de données de point de terminaison Microsoft 365 prend en charge l’intégration de session VDI non persistante.</span><span class="sxs-lookup"><span data-stu-id="8091f-110">Microsoft 365 Endpoint data loss prevention supports non-persistent VDI session onboarding.</span></span> 

>[!Note]
><span data-ttu-id="8091f-111">Pour intégrer des sessions VDI non persistantes, les appareils VDI doivent être sur Windows 10 1809 ou une autre.</span><span class="sxs-lookup"><span data-stu-id="8091f-111">To onboard non-persistent VDI sessions, VDI devices must be on Windows 10 1809 or higher.</span></span>

<span data-ttu-id="8091f-112">Il peut y avoir des difficultés associées lors de l’intégration des VDIs.</span><span class="sxs-lookup"><span data-stu-id="8091f-112">There might be associated challenges when onboarding VDIs.</span></span> <span data-ttu-id="8091f-113">Voici quelques défis classiques pour ce scénario :</span><span class="sxs-lookup"><span data-stu-id="8091f-113">The following are typical challenges for this scenario:</span></span>

- <span data-ttu-id="8091f-114">Intégration anticipée instantanée d’une session de courte durée, qui doit être intégré à la protection contre la perte de données du point de terminaison Microsoft 365 avant la mise en service réelle.</span><span class="sxs-lookup"><span data-stu-id="8091f-114">Instant early onboarding of a short-lived sessions, which must be onboarded to  Microsoft 365 Endpoint data loss prevention prior to the actual provisioning.</span></span>
- <span data-ttu-id="8091f-115">Le nom de l’appareil est généralement réutilisé pour les nouvelles sessions.</span><span class="sxs-lookup"><span data-stu-id="8091f-115">The device name is typically reused for new sessions.</span></span>

<span data-ttu-id="8091f-116">Les appareils VDI peuvent apparaître dans le Centre de conformité Microsoft 365 sous la forme :</span><span class="sxs-lookup"><span data-stu-id="8091f-116">VDI devices can appear in the Microsoft 365 Compliance center as either:</span></span>

- <span data-ttu-id="8091f-117">Entrée unique pour chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="8091f-117">Single entry for each device.</span></span>  
<span data-ttu-id="8091f-118">Notez que dans  ce cas, le même nom d’appareil doit être configuré lors de la création de la session, par exemple à l’aide d’un fichier de réponses sans surveillance.</span><span class="sxs-lookup"><span data-stu-id="8091f-118">Note that in this case, the *same* device name must be configured when the session is created, for example using an unattended answer file.</span></span>
- <span data-ttu-id="8091f-119">Plusieurs entrées pour chaque appareil - une pour chaque session.</span><span class="sxs-lookup"><span data-stu-id="8091f-119">Multiple entries for each device - one for each session.</span></span>

<span data-ttu-id="8091f-120">Les étapes suivantes vous guident tout au long de l’intégration des appareils VDI et mettent en évidence les étapes pour les entrées simples et multiples.</span><span class="sxs-lookup"><span data-stu-id="8091f-120">The following steps will guide you through onboarding VDI devices and will highlight steps for single and multiple entries.</span></span>

>[!WARNING]
> <span data-ttu-id="8091f-121">Pour les environnements où les configurations de ressources sont faibles, la procédure de démarrage VDI peut ralentir l’intégration de protection contre la perte de données de point de terminaison Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8091f-121">For environments where there are low resource configurations, the VDI boot procedure might slow the Microsoft 365 Endpoint data loss prevention onboarding.</span></span> 

1.  <span data-ttu-id="8091f-122">Ouvrez le fichier .zip du package de configuration VDI (*DeviceCompliancePackage.zip*) que vous avez téléchargé à partir de l’Assistant d’intégration de service.</span><span class="sxs-lookup"><span data-stu-id="8091f-122">Open the VDI configuration package .zip file (*DeviceCompliancePackage.zip*) that you downloaded from the service onboarding wizard.</span></span>

2.  <span data-ttu-id="8091f-123">Dans le volet de navigation, sélectionnez **Paramètres**  >  **Intégration de l’appareil.**  >  </span><span class="sxs-lookup"><span data-stu-id="8091f-123">In the navigation pane, select **Settings** > **Device onboarding** > **Onboarding**.</span></span>

3. <span data-ttu-id="8091f-124">Dans le **champ Méthode de** déploiement, sélectionnez les **scripts d’intégration VDI pour les** points de terminaison non persistants.</span><span class="sxs-lookup"><span data-stu-id="8091f-124">In the **Deployment method** field, select **VDI onboarding scripts for non-persistent endpoints**.</span></span>

5. <span data-ttu-id="8091f-125">Cliquez **sur Télécharger le package** et enregistrez le fichier .zip.</span><span class="sxs-lookup"><span data-stu-id="8091f-125">Click **Download package** and save the .zip file.</span></span>

6. <span data-ttu-id="8091f-126">Copiez les fichiers du dossier DeviceCompliancePackage extrait du fichier .zip dans l’image sous `golden/master` le chemin d’accès. `C:\WINDOWS\System32\GroupPolicy\Machine\Scripts\Startup`</span><span class="sxs-lookup"><span data-stu-id="8091f-126">Copy the files from the DeviceCompliancePackage folder extracted from the .zip file into the `golden/master` image under the path `C:\WINDOWS\System32\GroupPolicy\Machine\Scripts\Startup`.</span></span> 

7. <span data-ttu-id="8091f-127">Si vous n’implémentez pas une seule entrée pour chaque appareil, copiez DeviceComplianceOnboardingScript.cmd.</span><span class="sxs-lookup"><span data-stu-id="8091f-127">If you are not implementing a single entry for each device, copy DeviceComplianceOnboardingScript.cmd.</span></span>

8. <span data-ttu-id="8091f-128">Si vous implémentez une entrée unique pour chaque appareil, copiez à la fois Onboard-NonPersistentMachine.ps1 et DeviceComplianceOnboardingScript.cmd.</span><span class="sxs-lookup"><span data-stu-id="8091f-128">If you are implementing a single entry for each device, copy both Onboard-NonPersistentMachine.ps1 and DeviceComplianceOnboardingScript.cmd.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8091f-129">Si vous ne voyez pas le `C:\WINDOWS\System32\GroupPolicy\Machine\Scripts\Startup` dossier, il peut être masqué.</span><span class="sxs-lookup"><span data-stu-id="8091f-129">If you don't see the `C:\WINDOWS\System32\GroupPolicy\Machine\Scripts\Startup` folder, it might be hidden.</span></span> <span data-ttu-id="8091f-130">Vous devez choisir l’option Afficher les fichiers **et dossiers masqués** dans l’Explorateur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="8091f-130">You'll need to choose the **Show hidden files and folders** option from File Explorer.</span></span>

9. <span data-ttu-id="8091f-131">Ouvrez une fenêtre Éditeur de stratégie de groupe locale et accédez au démarrage des scripts de  >  **paramètres Windows** de configuration  >    >  **ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="8091f-131">Open a Local Group Policy Editor window and navigate to **Computer Configuration** > **Windows Settings** > **Scripts** > **Startup**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="8091f-132">La stratégie de groupe de domaine peut également être utilisée pour l’intégration d’appareils VDI non persistants.</span><span class="sxs-lookup"><span data-stu-id="8091f-132">Domain Group Policy may also be used for onboarding non-persistent VDI devices.</span></span>

4. <span data-ttu-id="8091f-133">Selon la méthode que vous souhaitez implémenter, suivez les étapes appropriées :</span><span class="sxs-lookup"><span data-stu-id="8091f-133">Depending on the method you'd like to implement, follow the appropriate steps:</span></span>

   <span data-ttu-id="8091f-134">**Pour une entrée unique pour chaque appareil**</span><span class="sxs-lookup"><span data-stu-id="8091f-134">**For single entry for each device**</span></span>
   
   <span data-ttu-id="8091f-135">Sélectionnez **l’onglet Scripts PowerShell,** puis cliquez sur Ajouter (l’Explorateur Windows s’ouvre directement dans le chemin d’accès où vous avez copié le script d’intégration précédemment). </span><span class="sxs-lookup"><span data-stu-id="8091f-135">Select the **PowerShell Scripts** tab, then click **Add** (Windows Explorer will open directly in the path where you copied the onboarding script earlier).</span></span> <span data-ttu-id="8091f-136">Accédez au script PowerShell `Onboard-NonPersistentMachine.ps1` d’intégration.</span><span class="sxs-lookup"><span data-stu-id="8091f-136">Navigate to onboarding PowerShell script `Onboard-NonPersistentMachine.ps1`.</span></span>
   
   <span data-ttu-id="8091f-137">**Pour plusieurs entrées pour chaque appareil**:</span><span class="sxs-lookup"><span data-stu-id="8091f-137">**For multiple entries for each device**:</span></span>
   
   <span data-ttu-id="8091f-138">Sélectionnez **l’onglet Scripts,** puis cliquez sur Ajouter (l’Explorateur Windows s’ouvre directement dans le chemin d’accès où vous avez copié le script d’intégration précédemment). </span><span class="sxs-lookup"><span data-stu-id="8091f-138">Select the **Scripts** tab, then click **Add** (Windows Explorer will open directly in the path where you copied the onboarding script earlier).</span></span> <span data-ttu-id="8091f-139">Accédez au script Bash `DeviceComplianceOnboardingScript.cmd` d’intégration.</span><span class="sxs-lookup"><span data-stu-id="8091f-139">Navigate to the onboarding bash script `DeviceComplianceOnboardingScript.cmd`.</span></span>

5. <span data-ttu-id="8091f-140">Testez votre solution :</span><span class="sxs-lookup"><span data-stu-id="8091f-140">Test your solution:</span></span>

   1. <span data-ttu-id="8091f-141">Créez un pool avec un seul appareil.</span><span class="sxs-lookup"><span data-stu-id="8091f-141">Create a pool with one device.</span></span>
      
   1. <span data-ttu-id="8091f-142">Se logo à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8091f-142">Logon to device.</span></span>
      
   1. <span data-ttu-id="8091f-143">Ffage de la logo à partir de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8091f-143">Logoff from device.</span></span>

   1. <span data-ttu-id="8091f-144">Se rendre sur l’appareil avec un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8091f-144">Logon to device with another user.</span></span>
      
   1. <span data-ttu-id="8091f-145">**Pour une entrée unique pour chaque appareil :** vérifiez une seule entrée dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="8091f-145">**For single entry for each device**: Check only one entry in Microsoft Defender Security Center.</span></span><br>
      <span data-ttu-id="8091f-146">**Pour plusieurs entrées pour chaque appareil :** vérifiez plusieurs entrées dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="8091f-146">**For multiple entries for each device**: Check multiple entries in Microsoft Defender Security Center.</span></span>

6. <span data-ttu-id="8091f-147">Cliquez **sur La liste Appareils** dans le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="8091f-147">Click **Devices list** on the Navigation pane.</span></span>

7. <span data-ttu-id="8091f-148">Utilisez la fonction de recherche en entrant le nom de l’appareil et **sélectionnez Appareil** comme type de recherche.</span><span class="sxs-lookup"><span data-stu-id="8091f-148">Use the search function by entering the device name and select **Device** as search type.</span></span>

## <a name="updating-non-persistent-virtual-desktop-infrastructure-vdi-images"></a><span data-ttu-id="8091f-149">Mise à jour d’images VDI (Virtual Desktop Infrastructure) non persistantes</span><span class="sxs-lookup"><span data-stu-id="8091f-149">Updating non-persistent virtual desktop infrastructure (VDI) images</span></span>
<span data-ttu-id="8091f-150">En tant que meilleure pratique, nous vous recommandons d’utiliser des outils de maintenance hors connexion pour mettre à jour les images de base/de base.</span><span class="sxs-lookup"><span data-stu-id="8091f-150">As a best practice, we recommend using offline servicing tools to patch golden/master images.</span></span><br>
<span data-ttu-id="8091f-151">Par exemple, vous pouvez utiliser les commandes ci-dessous pour installer une mise à jour pendant que l’image reste hors connexion :</span><span class="sxs-lookup"><span data-stu-id="8091f-151">For example, you can use the below commands to install an update while the image remains offline:</span></span>

```console
DISM /Mount-image /ImageFile:"D:\Win10-1909.vhdx" /index:1 /MountDir:"C:\Temp\OfflineServicing" 
DISM /Image:"C:\Temp\OfflineServicing" /Add-Package /Packagepath:"C:\temp\patch\windows10.0-kb4541338-x64.msu"
DISM /Unmount-Image /MountDir:"C:\Temp\OfflineServicing" /commit
```

<span data-ttu-id="8091f-152">Pour plus d’informations sur les commandes DISM et la maintenance hors connexion, consultez les articles ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="8091f-152">For more information on DISM commands and offline servicing, please refer to the articles below:</span></span>
- [<span data-ttu-id="8091f-153">Modifier une image Windows à l’aide de DISM</span><span class="sxs-lookup"><span data-stu-id="8091f-153">Modify a Windows image using DISM</span></span>](/windows-hardware/manufacture/desktop/mount-and-modify-a-windows-image-using-dism)
- [<span data-ttu-id="8091f-154">Options de gestion des images DISM Command-Line d’images</span><span class="sxs-lookup"><span data-stu-id="8091f-154">DISM Image Management Command-Line Options</span></span>](/windows-hardware/manufacture/desktop/dism-image-management-command-line-options-s14)
- [<span data-ttu-id="8091f-155">Réduire la taille du magasin de composants dans une image Windows hors connexion</span><span class="sxs-lookup"><span data-stu-id="8091f-155">Reduce the Size of the Component Store in an Offline Windows Image</span></span>](/windows-hardware/manufacture/desktop/reduce-the-size-of-the-component-store-in-an-offline-windows-image)

<span data-ttu-id="8091f-156">Si la maintenance hors connexion n’est pas une option viable pour votre environnement VDI non persistant, les étapes suivantes doivent être prises pour garantir la cohérence et l’état du capteur :</span><span class="sxs-lookup"><span data-stu-id="8091f-156">If offline servicing is not a viable option for your non-persistent VDI environment, the following steps should be taken to ensure consistency and sensor health:</span></span>

1. <span data-ttu-id="8091f-157">Après avoir démarré l’image maître pour la maintenance en ligne ou la correction, exécutez un script de mise hors service pour désactiver le capteur de protection contre la perte de données du point de terminaison Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8091f-157">After booting the master image for online servicing or patching, run an offboarding script to turn off the Microsoft 365 Endpoint data loss prevention sensor.</span></span> <span data-ttu-id="8091f-158">Pour plus d’informations, voir [Les appareils hors-carte à l’aide d’un script local.](dlp-configure-endpoints-script.md#offboard-devices-using-a-local-script)</span><span class="sxs-lookup"><span data-stu-id="8091f-158">For more information, see [Offboard devices using a local script](dlp-configure-endpoints-script.md#offboard-devices-using-a-local-script).</span></span>

2. <span data-ttu-id="8091f-159">Assurez-vous que le capteur est arrêté en exécutant la commande ci-dessous dans une fenêtre CMD :</span><span class="sxs-lookup"><span data-stu-id="8091f-159">Ensure the sensor is stopped by running the command below in a CMD window:</span></span>

   ```console
   sc query sense
   ```

3. <span data-ttu-id="8091f-160">Service de l’image selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="8091f-160">Service the image as needed.</span></span>

4. <span data-ttu-id="8091f-161">Exécutez les commandes ci-dessous à l’aide PsExec.exe (qui peut être téléchargé à partir de pour nettoyer le contenu du dossier cyber que le capteur a peut-être cumulé https://download.sysinternals.com/files/PSTools.zip) depuis le démarrage :</span><span class="sxs-lookup"><span data-stu-id="8091f-161">Run the below commands using PsExec.exe (which can be downloaded from https://download.sysinternals.com/files/PSTools.zip) to cleanup the cyber folder contents that the sensor may have accumulated since boot:</span></span>

    ```console
    PsExec.exe -s cmd.exe
    cd "C:\ProgramData\Microsoft\Windows Defender Advanced Threat Protection\Cyber"
    del *.* /f /s /q
    REG DELETE “HKLM\SOFTWARE\Microsoft\Windows Advanced Threat Protection" /v senseGuid /f
    exit
    ```

5. <span data-ttu-id="8091f-162">Rescellez l’image de premier plan comme vous le feriez normalement.</span><span class="sxs-lookup"><span data-stu-id="8091f-162">Re-seal the golden/master image as you normally would.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8091f-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8091f-163">Related topics</span></span>
- [<span data-ttu-id="8091f-164">Intégrer des appareils Windows 10 à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8091f-164">Onboard Windows 10 devices using Group Policy</span></span>](dlp-configure-endpoints-gp.md)
- [<span data-ttu-id="8091f-165">Intégrer des appareils Windows 10 à l’aide de Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8091f-165">Onboard Windows 10 devices using Microsoft Endpoint Configuration Manager</span></span>](dlp-configure-endpoints-sccm.md)
- [<span data-ttu-id="8091f-166">Intégrer les appareils Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="8091f-166">Onboard Windows 10 devices using Mobile Device Management tools</span></span>](dlp-configure-endpoints-mdm.md)
- [<span data-ttu-id="8091f-167">Intégrer les appareils Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="8091f-167">Onboard Windows 10 devices using a local script</span></span>](dlp-configure-endpoints-script.md)
- [<span data-ttu-id="8091f-168">Résoudre les problèmes d’intégration de la Protection avancée contre les menaces Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="8091f-168">Troubleshoot Microsoft Defender Advanced Threat Protection onboarding issues</span></span>](/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding)