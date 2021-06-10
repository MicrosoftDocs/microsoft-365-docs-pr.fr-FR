---
title: Intégrer les ordinateurs virtuels d’infrastructure de bureau virtuel (VDI) non persistants.
description: Déployez le package de configuration sur un appareil VDI (Virtual Desktop Infrastructure) afin qu’il soit intégré au service Microsoft Defender for Endpoint.
keywords: configurer l’infrastructure VDI (Virtual Desktop Infrastructure), vdi, gestion des appareils, configurer Microsoft Defender pour les points de terminaison, points de terminaison
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
ms.date: 04/16/2020
ms.technology: mde
ms.openlocfilehash: d09967a18848365702f52f65a7f0624d2b2ae3d6
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52843209"
---
# <a name="onboard-non-persistent-virtual-desktop-infrastructure-vdi-devices"></a><span data-ttu-id="a8df5-104">Intégrer les ordinateurs virtuels d’infrastructure de bureau virtuel (VDI) non persistants.</span><span class="sxs-lookup"><span data-stu-id="a8df5-104">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="a8df5-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a8df5-105">**Applies to:**</span></span>
- [<span data-ttu-id="a8df5-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a8df5-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="a8df5-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a8df5-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)
- <span data-ttu-id="a8df5-108">Périphériques VDI (Virtual Desktop Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="a8df5-108">Virtual desktop infrastructure (VDI) devices</span></span>
- <span data-ttu-id="a8df5-109">Windows 10, Windows Server 2019, Windows Server 2008R2/2012R2/2016</span><span class="sxs-lookup"><span data-stu-id="a8df5-109">Windows 10, Windows Server 2019, Windows Server 2008R2/2012R2/2016</span></span>

><span data-ttu-id="a8df5-110">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="a8df5-110">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="a8df5-111">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="a8df5-111">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-configvdi-abovefoldlink)

## <a name="onboard-non-persistent-virtual-desktop-infrastructure-vdi-devices"></a><span data-ttu-id="a8df5-112">Intégrer les ordinateurs virtuels d’infrastructure de bureau virtuel (VDI) non persistants.</span><span class="sxs-lookup"><span data-stu-id="a8df5-112">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>

<span data-ttu-id="a8df5-113">Defender pour le point de terminaison prend en charge l’intégration de session VDI non persistante.</span><span class="sxs-lookup"><span data-stu-id="a8df5-113">Defender for Endpoint supports non-persistent VDI session onboarding.</span></span> 


<span data-ttu-id="a8df5-114">Il peut y avoir des difficultés associées lors de l’intégration des VDIs.</span><span class="sxs-lookup"><span data-stu-id="a8df5-114">There might be associated challenges when onboarding VDIs.</span></span> <span data-ttu-id="a8df5-115">Les défis classiques de ce scénario sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="a8df5-115">The following are typical challenges for this scenario:</span></span>

- <span data-ttu-id="a8df5-116">Intégration anticipée instantanée d’une session à durée de vie courte, qui doit être intégré à Defender for Endpoint avant la mise en service réelle.</span><span class="sxs-lookup"><span data-stu-id="a8df5-116">Instant early onboarding of a short-lived sessions, which must be onboarded to Defender for Endpoint prior to the actual provisioning.</span></span>
- <span data-ttu-id="a8df5-117">Le nom de l’appareil est généralement réutilisé pour les nouvelles sessions.</span><span class="sxs-lookup"><span data-stu-id="a8df5-117">The device name is typically reused for new sessions.</span></span>

<span data-ttu-id="a8df5-118">Les appareils VDI peuvent apparaître dans le portail Defender for Endpoint sous la forme :</span><span class="sxs-lookup"><span data-stu-id="a8df5-118">VDI devices can appear in Defender for Endpoint portal as either:</span></span>

- <span data-ttu-id="a8df5-119">Entrée unique pour chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="a8df5-119">Single entry for each device.</span></span>

  > [!NOTE]
  > <span data-ttu-id="a8df5-120">Dans ce cas, le *même* nom d’appareil doit être configuré lors de la création de la session, par exemple à l’aide d’un fichier de réponses sans surveillance.</span><span class="sxs-lookup"><span data-stu-id="a8df5-120">In this case, the *same* device name must be configured when the session is created, for example using an unattended answer file.</span></span>

- <span data-ttu-id="a8df5-121">Plusieurs entrées pour chaque appareil - une pour chaque session.</span><span class="sxs-lookup"><span data-stu-id="a8df5-121">Multiple entries for each device - one for each session.</span></span>

<span data-ttu-id="a8df5-122">Les étapes suivantes vous guident tout au long de l’intégration des appareils VDI et mettent en évidence les étapes pour les entrées simples et multiples.</span><span class="sxs-lookup"><span data-stu-id="a8df5-122">The following steps will guide you through onboarding VDI devices and will highlight steps for single and multiple entries.</span></span>

>[!WARNING]
> <span data-ttu-id="a8df5-123">Pour les environnements dans lequel il existe des configurations de ressources faibles, la procédure de démarrage VDI peut ralentir l’intégration du capteur Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="a8df5-123">For environments where there are low resource configurations, the VDI boot procedure might slow the Defender for Endpoint sensor onboarding.</span></span> 


### <a name="for-windows-10-or-windows-server-2019"></a><span data-ttu-id="a8df5-124">Pour Windows 10 ou Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="a8df5-124">For Windows 10 or Windows Server 2019</span></span>

1.  <span data-ttu-id="a8df5-125">Ouvrez le fichier de package de configuration VDI .zip (*WindowsDefenderATPOnboardingPackage.zip*) que vous avez téléchargé à partir de l’Assistant d’intégration de service.</span><span class="sxs-lookup"><span data-stu-id="a8df5-125">Open the VDI configuration package .zip file (*WindowsDefenderATPOnboardingPackage.zip*) that you downloaded from the service onboarding wizard.</span></span> <span data-ttu-id="a8df5-126">Vous pouvez également obtenir le package à partir [de Centre de sécurité Microsoft Defender](https://securitycenter.windows.com/):</span><span class="sxs-lookup"><span data-stu-id="a8df5-126">You can also get the package from [Microsoft Defender Security Center](https://securitycenter.windows.com/):</span></span>

    1.  <span data-ttu-id="a8df5-127">Dans le volet de navigation, sélectionnez  >  **Paramètres’intégration.**</span><span class="sxs-lookup"><span data-stu-id="a8df5-127">In the navigation pane, select **Settings** > **Onboarding**.</span></span>

    1. <span data-ttu-id="a8df5-128">Sélectionnez Windows 10 comme système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a8df5-128">Select Windows 10 as the operating system.</span></span>

    1.  <span data-ttu-id="a8df5-129">Dans le **champ Méthode de** déploiement, sélectionnez les **scripts d’intégration VDI pour les** points de terminaison non persistants.</span><span class="sxs-lookup"><span data-stu-id="a8df5-129">In the **Deployment method** field, select **VDI onboarding scripts for non-persistent endpoints**.</span></span>

    1. <span data-ttu-id="a8df5-130">Cliquez **sur Télécharger le package** et enregistrez .zip fichier.</span><span class="sxs-lookup"><span data-stu-id="a8df5-130">Click **Download package** and save the .zip file.</span></span>

2. <span data-ttu-id="a8df5-131">Copiez les fichiers du dossier WindowsDefenderATPOnboardingPackage extraits du fichier .zip dans l’image sous `golden/master` le chemin d’accès. `C:\WINDOWS\System32\GroupPolicy\Machine\Scripts\Startup`</span><span class="sxs-lookup"><span data-stu-id="a8df5-131">Copy the files from the WindowsDefenderATPOnboardingPackage folder extracted from the .zip file into the `golden/master` image under the path `C:\WINDOWS\System32\GroupPolicy\Machine\Scripts\Startup`.</span></span> 

    1. <span data-ttu-id="a8df5-132">Si vous n’implémentez pas une seule entrée pour chaque appareil, copiez WindowsDefenderATPOnboardingScript.cmd.</span><span class="sxs-lookup"><span data-stu-id="a8df5-132">If you are not implementing a single entry for each device, copy WindowsDefenderATPOnboardingScript.cmd.</span></span>

    1. <span data-ttu-id="a8df5-133">Si vous implémentez une entrée unique pour chaque appareil, copiez à la fois Onboard-NonPersistentMachine.ps1 et WindowsDefenderATPOnboardingScript.cmd.</span><span class="sxs-lookup"><span data-stu-id="a8df5-133">If you are implementing a single entry for each device, copy both Onboard-NonPersistentMachine.ps1 and WindowsDefenderATPOnboardingScript.cmd.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="a8df5-134">Si vous ne voyez pas le `C:\WINDOWS\System32\GroupPolicy\Machine\Scripts\Startup` dossier, il peut être masqué.</span><span class="sxs-lookup"><span data-stu-id="a8df5-134">If you don't see the `C:\WINDOWS\System32\GroupPolicy\Machine\Scripts\Startup` folder, it might be hidden.</span></span> <span data-ttu-id="a8df5-135">Vous devez choisir l’option Afficher les fichiers **et dossiers masqués** dans l’Explorateur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="a8df5-135">You'll need to choose the **Show hidden files and folders** option from File Explorer.</span></span>

3. <span data-ttu-id="a8df5-136">Ouvrez une fenêtre Éditeur de stratégie de groupe locale et accédez à **Configuration** ordinateur  >  **Windows Paramètres**  >  **scripts de**  >  **démarrage.**</span><span class="sxs-lookup"><span data-stu-id="a8df5-136">Open a Local Group Policy Editor window and navigate to **Computer Configuration** > **Windows Settings** > **Scripts** > **Startup**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="a8df5-137">La stratégie de groupe de domaine peut également être utilisée pour l’intégration d’appareils VDI non persistants.</span><span class="sxs-lookup"><span data-stu-id="a8df5-137">Domain Group Policy may also be used for onboarding non-persistent VDI devices.</span></span>

4. <span data-ttu-id="a8df5-138">Selon la méthode que vous souhaitez implémenter, suivez les étapes appropriées :</span><span class="sxs-lookup"><span data-stu-id="a8df5-138">Depending on the method you'd like to implement, follow the appropriate steps:</span></span>

   - <span data-ttu-id="a8df5-139">Pour une entrée unique pour chaque appareil :</span><span class="sxs-lookup"><span data-stu-id="a8df5-139">For single entry for each device:</span></span>
   
     <span data-ttu-id="a8df5-140">Sélectionnez **l’onglet Scripts PowerShell,** puis cliquez sur Ajouter **(Windows** Explorer s’ouvre directement dans le chemin d’accès où vous avez copié le script d’intégration précédemment).</span><span class="sxs-lookup"><span data-stu-id="a8df5-140">Select the **PowerShell Scripts** tab, then click **Add** (Windows Explorer will open directly in the path where you copied the onboarding script earlier).</span></span> <span data-ttu-id="a8df5-141">Accédez au script PowerShell `Onboard-NonPersistentMachine.ps1` d’intégration.</span><span class="sxs-lookup"><span data-stu-id="a8df5-141">Navigate to onboarding PowerShell script `Onboard-NonPersistentMachine.ps1`.</span></span> <span data-ttu-id="a8df5-142">Il n’est pas nécessaire de spécifier l’autre fichier, car il sera déclenché automatiquement.</span><span class="sxs-lookup"><span data-stu-id="a8df5-142">There is no need to specify the other file, as it will be triggered automatically.</span></span>
   
   - <span data-ttu-id="a8df5-143">Pour plusieurs entrées pour chaque appareil :</span><span class="sxs-lookup"><span data-stu-id="a8df5-143">For multiple entries for each device:</span></span>
   
     <span data-ttu-id="a8df5-144">Sélectionnez **l’onglet Scripts,** puis cliquez sur Ajouter **(Windows** Explorer s’ouvre directement dans le chemin d’accès où vous avez copié le script d’intégration précédemment).</span><span class="sxs-lookup"><span data-stu-id="a8df5-144">Select the **Scripts** tab, then click **Add** (Windows Explorer will open directly in the path where you copied the onboarding script earlier).</span></span> <span data-ttu-id="a8df5-145">Accédez au script Bash `WindowsDefenderATPOnboardingScript.cmd` d’intégration.</span><span class="sxs-lookup"><span data-stu-id="a8df5-145">Navigate to the onboarding bash script `WindowsDefenderATPOnboardingScript.cmd`.</span></span>

5. <span data-ttu-id="a8df5-146">Testez votre solution :</span><span class="sxs-lookup"><span data-stu-id="a8df5-146">Test your solution:</span></span>

   1. <span data-ttu-id="a8df5-147">Créez un pool avec un seul appareil.</span><span class="sxs-lookup"><span data-stu-id="a8df5-147">Create a pool with one device.</span></span>
      
   1. <span data-ttu-id="a8df5-148">Logon à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a8df5-148">Logon to device.</span></span>
      
   1. <span data-ttu-id="a8df5-149">Ffage de la logo à partir de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a8df5-149">Logoff from device.</span></span>

   1. <span data-ttu-id="a8df5-150">Se rendre sur l’appareil avec un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a8df5-150">Logon to device with another user.</span></span>
      
   1. <span data-ttu-id="a8df5-151">Selon la méthode que vous souhaitez implémenter, suivez les étapes appropriées :</span><span class="sxs-lookup"><span data-stu-id="a8df5-151">Depending on the method you'd like to implement, follow the appropriate steps:</span></span>
   
      - <span data-ttu-id="a8df5-152">Pour une entrée unique pour chaque appareil :</span><span class="sxs-lookup"><span data-stu-id="a8df5-152">For single entry for each device:</span></span> 
    
        <span data-ttu-id="a8df5-153">Vérifiez une seule entrée dans Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="a8df5-153">Check only one entry in Microsoft Defender Security Center.</span></span>

      - <span data-ttu-id="a8df5-154">Pour plusieurs entrées pour chaque appareil :</span><span class="sxs-lookup"><span data-stu-id="a8df5-154">For multiple entries for each device:</span></span> 
       
        <span data-ttu-id="a8df5-155">Vérifiez plusieurs entrées dans Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="a8df5-155">Check multiple entries in Microsoft Defender Security Center.</span></span>

6. <span data-ttu-id="a8df5-156">Cliquez **sur La liste Appareils** dans le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="a8df5-156">Click **Devices list** on the Navigation pane.</span></span>

7. <span data-ttu-id="a8df5-157">Utilisez la fonction de recherche en entrant le nom de l’appareil et **sélectionnez Appareil** comme type de recherche.</span><span class="sxs-lookup"><span data-stu-id="a8df5-157">Use the search function by entering the device name and select **Device** as search type.</span></span>


## <a name="for-downlevel-skus"></a><span data-ttu-id="a8df5-158">Pour les SSO de niveau bas</span><span class="sxs-lookup"><span data-stu-id="a8df5-158">For downlevel SKUs</span></span>

> [!NOTE]
> <span data-ttu-id="a8df5-159">Le Registre suivant n’est pertinent que lorsque l’objectif est d’obtenir une entrée unique pour chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="a8df5-159">The following registry is relevant only when the aim is to achieve a 'Single entry for each device'.</span></span>

1. <span data-ttu-id="a8df5-160">Définissez la valeur de Registre sur :</span><span class="sxs-lookup"><span data-stu-id="a8df5-160">Set registry value to:</span></span>

    ```console
   [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Advanced Threat Protection\DeviceTagging]
    "VDI"="NonPersistent"
    ```

    <span data-ttu-id="a8df5-161">ou à l’aide de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="a8df5-161">or using command line:</span></span>

    ```console
    reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Advanced Threat Protection\DeviceTagging" /v VDI /t REG_SZ /d "NonPersistent" /f
    ```

2. <span data-ttu-id="a8df5-162">Suivez le [processus d’intégration du serveur.](configure-server-endpoints.md#windows-server-2008-r2-sp1-windows-server-2012-r2-and-windows-server-2016)</span><span class="sxs-lookup"><span data-stu-id="a8df5-162">Follow the [server onboarding process](configure-server-endpoints.md#windows-server-2008-r2-sp1-windows-server-2012-r2-and-windows-server-2016).</span></span> 



## <a name="updating-non-persistent-virtual-desktop-infrastructure-vdi-images"></a><span data-ttu-id="a8df5-163">Mise à jour d’images VDI (Virtual Desktop Infrastructure) non persistantes</span><span class="sxs-lookup"><span data-stu-id="a8df5-163">Updating non-persistent virtual desktop infrastructure (VDI) images</span></span>
<span data-ttu-id="a8df5-164">En tant que meilleure pratique, nous vous recommandons d’utiliser des outils de maintenance hors connexion pour mettre à jour les images de base/de base.</span><span class="sxs-lookup"><span data-stu-id="a8df5-164">As a best practice, we recommend using offline servicing tools to patch golden/master images.</span></span><br>
<span data-ttu-id="a8df5-165">Par exemple, vous pouvez utiliser les commandes ci-dessous pour installer une mise à jour pendant que l’image reste hors connexion :</span><span class="sxs-lookup"><span data-stu-id="a8df5-165">For example, you can use the below commands to install an update while the image remains offline:</span></span>

```console
DISM /Mount-image /ImageFile:"D:\Win10-1909.vhdx" /index:1 /MountDir:"C:\Temp\OfflineServicing" 
DISM /Image:"C:\Temp\OfflineServicing" /Add-Package /Packagepath:"C:\temp\patch\windows10.0-kb4541338-x64.msu"
DISM /Unmount-Image /MountDir:"C:\Temp\OfflineServicing" /commit
```

<span data-ttu-id="a8df5-166">Pour plus d’informations sur les commandes DISM et la maintenance hors connexion, consultez les articles ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="a8df5-166">For more information on DISM commands and offline servicing, please refer to the articles below:</span></span>
- [<span data-ttu-id="a8df5-167">Modifier une image Windows à l’aide de DISM</span><span class="sxs-lookup"><span data-stu-id="a8df5-167">Modify a Windows image using DISM</span></span>](/windows-hardware/manufacture/desktop/mount-and-modify-a-windows-image-using-dism)
- [<span data-ttu-id="a8df5-168">Options de gestion des images DISM Command-Line d’images</span><span class="sxs-lookup"><span data-stu-id="a8df5-168">DISM Image Management Command-Line Options</span></span>](/windows-hardware/manufacture/desktop/dism-image-management-command-line-options-s14)
- [<span data-ttu-id="a8df5-169">Réduire la taille du magasin de composants dans une image de Windows hors connexion</span><span class="sxs-lookup"><span data-stu-id="a8df5-169">Reduce the Size of the Component Store in an Offline Windows Image</span></span>](/windows-hardware/manufacture/desktop/reduce-the-size-of-the-component-store-in-an-offline-windows-image)

<span data-ttu-id="a8df5-170">Si la maintenance hors connexion n’est pas une option viable pour votre environnement VDI non persistant, les étapes suivantes doivent être prises pour garantir la cohérence et l’état du capteur :</span><span class="sxs-lookup"><span data-stu-id="a8df5-170">If offline servicing is not a viable option for your non-persistent VDI environment, the following steps should be taken to ensure consistency and sensor health:</span></span>

1. <span data-ttu-id="a8df5-171">Après avoir démarré l’image maître pour la maintenance en ligne ou la correction, exécutez un script de mise hors service pour désactiver le capteur Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="a8df5-171">After booting the master image for online servicing or patching, run an offboarding script to turn off the Defender for Endpoint sensor.</span></span> <span data-ttu-id="a8df5-172">Pour plus d’informations, voir [Les appareils hors-carte à l’aide d’un script local.](configure-endpoints-script.md#offboard-devices-using-a-local-script)</span><span class="sxs-lookup"><span data-stu-id="a8df5-172">For more information, see [Offboard devices using a local script](configure-endpoints-script.md#offboard-devices-using-a-local-script).</span></span>

2. <span data-ttu-id="a8df5-173">Assurez-vous que le capteur est arrêté en exécutant la commande ci-dessous dans une fenêtre CMD :</span><span class="sxs-lookup"><span data-stu-id="a8df5-173">Ensure the sensor is stopped by running the command below in a CMD window:</span></span>

   ```console
   sc query sense
   ```

3. <span data-ttu-id="a8df5-174">Service de l’image selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="a8df5-174">Service the image as needed.</span></span>

4. <span data-ttu-id="a8df5-175">Exécutez les commandes ci-dessous à l’aide PsExec.exe (qui peut être téléchargé à partir de pour nettoyer le contenu du dossier cyber que le capteur a peut-être cumulé https://download.sysinternals.com/files/PSTools.zip) depuis le démarrage :</span><span class="sxs-lookup"><span data-stu-id="a8df5-175">Run the below commands using PsExec.exe (which can be downloaded from https://download.sysinternals.com/files/PSTools.zip) to cleanup the cyber folder contents that the sensor may have accumulated since boot:</span></span>

    ```console
    PsExec.exe -s cmd.exe
    cd "C:\ProgramData\Microsoft\Windows Defender Advanced Threat Protection\Cyber"
    del *.* /f /s /q
    REG DELETE “HKLM\SOFTWARE\Microsoft\Windows Advanced Threat Protection" /v senseGuid /f
    exit
    ```

5. <span data-ttu-id="a8df5-176">Rescellez l’image de premier plan comme vous le feriez normalement.</span><span class="sxs-lookup"><span data-stu-id="a8df5-176">Re-seal the golden/master image as you normally would.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8df5-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8df5-177">Related topics</span></span>
- [<span data-ttu-id="a8df5-178">Intégrer des Windows 10 à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="a8df5-178">Onboard Windows 10 devices using Group Policy</span></span>](configure-endpoints-gp.md)
- [<span data-ttu-id="a8df5-179">Intégrer Windows 10 appareils à l’aide Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a8df5-179">Onboard Windows 10 devices using Microsoft Endpoint Configuration Manager</span></span>](configure-endpoints-sccm.md)
- [<span data-ttu-id="a8df5-180">Intégrer les appareils Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="a8df5-180">Onboard Windows 10 devices using Mobile Device Management tools</span></span>](configure-endpoints-mdm.md)
- [<span data-ttu-id="a8df5-181">Intégrer les appareils Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="a8df5-181">Onboard Windows 10 devices using a local script</span></span>](configure-endpoints-script.md)
- [<span data-ttu-id="a8df5-182">Résoudre les problèmes d’intégration de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="a8df5-182">Troubleshoot Microsoft Defender for Endpoint onboarding issues</span></span>](troubleshoot-onboarding.md)
