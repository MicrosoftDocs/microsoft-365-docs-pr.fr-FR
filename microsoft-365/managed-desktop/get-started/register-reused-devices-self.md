---
title: Inscrivez vous-même les appareils existant
description: Enregistrer les appareils réutilisés vous avez peut-être déjà des utilisateurs pour qu’ils puissent être gérés par le bureau géré Microsoft
ms.prod: w10
author: jaimeo
f1.keywords:
- NOCSH
ms.author: jaimeo
ms.localizationpriority: medium
ms.openlocfilehash: 51c241c46a4c8745bcae169a1c1d89e5c4393f2f
ms.sourcegitcommit: abf63669daf12993ad3353e4b578f41c8910b20f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2020
ms.locfileid: "47289138"
---
# <a name="register-existing-devices-yourself"></a><span data-ttu-id="85fd9-103">Inscrivez vous-même les appareils existant</span><span class="sxs-lookup"><span data-stu-id="85fd9-103">Register existing devices yourself</span></span>

>[!NOTE]
><span data-ttu-id="85fd9-104">Cette rubrique décrit la procédure à suivre pour réutiliser les appareils dont vous disposez déjà et les enregistrer dans le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="85fd9-104">This topic describes the steps for you to re-use devices you already have and register them in Microsoft Managed Desktop.</span></span> <span data-ttu-id="85fd9-105">Si vous travaillez avec des appareils de marque, suivez plutôt les étapes de la procédure [inscrire de nouveaux appareils dans Microsoft Managed Desktop](register-devices-self.md) .</span><span class="sxs-lookup"><span data-stu-id="85fd9-105">If you are working with brand-new devices, follow the steps in [Register new devices in Microsoft Managed Desktop yourself](register-devices-self.md) instead.</span></span>

<span data-ttu-id="85fd9-106">Le processus pour les partenaires est documenté dans la [procédure permettant aux partenaires d’inscrire des appareils](register-devices-partner.md).</span><span class="sxs-lookup"><span data-stu-id="85fd9-106">The process for Partners is documented in [Steps for Partners to register devices](register-devices-partner.md).</span></span>

<span data-ttu-id="85fd9-107">Microsoft Managed Desktop peut fonctionner avec les nouveaux appareils ou vous pouvez réutiliser des appareils que vous avez peut-être déjà (ce qui vous obligera à les réimager).</span><span class="sxs-lookup"><span data-stu-id="85fd9-107">Microsoft Managed Desktop can work with brand-new devices or you can re-use devices you might already have (which will require that you re-image them).</span></span> <span data-ttu-id="85fd9-108">Vous pouvez enregistrer des appareils à l’aide du portail d’administration de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="85fd9-108">You can register devices by using the Microsoft Managed Desktop Admin Portal.</span></span>

## <a name="prepare-to-register-existing-devices"></a><span data-ttu-id="85fd9-109">Préparation à l’enregistrement des appareils existants</span><span class="sxs-lookup"><span data-stu-id="85fd9-109">Prepare to register existing devices</span></span>


<span data-ttu-id="85fd9-110">Pour enregistrer des appareils existants, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="85fd9-110">To register existing devices, follow these steps:</span></span>

1. [<span data-ttu-id="85fd9-111">Obtenez le hachage matériel de chaque périphérique.</span><span class="sxs-lookup"><span data-stu-id="85fd9-111">Obtain the hardware hash for each device.</span></span>](#obtain-the-hardware-hash)
2. [<span data-ttu-id="85fd9-112">Fusionner les données de hachage</span><span class="sxs-lookup"><span data-stu-id="85fd9-112">Merge the hash data</span></span>](#merge-hash-data)
3. <span data-ttu-id="85fd9-113">[Inscrivez les appareils dans le bureau géré Microsoft](#register-devices-by-using-the-admin-portal).</span><span class="sxs-lookup"><span data-stu-id="85fd9-113">[Register the devices in Microsoft Managed Desktop](#register-devices-by-using-the-admin-portal).</span></span>
4. [<span data-ttu-id="85fd9-114">Vérifiez que l’image est correcte.</span><span class="sxs-lookup"><span data-stu-id="85fd9-114">Double-check that the image is correct.</span></span>](#check-the-image)
5. [<span data-ttu-id="85fd9-115">Remise de l’appareil</span><span class="sxs-lookup"><span data-stu-id="85fd9-115">Deliver the device</span></span>](#deliver-the-device)

### <a name="obtain-the-hardware-hash"></a><span data-ttu-id="85fd9-116">Obtenir le hachage matériel</span><span class="sxs-lookup"><span data-stu-id="85fd9-116">Obtain the hardware hash</span></span>

<span data-ttu-id="85fd9-117">Microsoft Managed Desktop identifie chaque appareil de manière unique en référençant son hachage matériel.</span><span class="sxs-lookup"><span data-stu-id="85fd9-117">Microsoft Managed Desktop identifies each device uniquely by referencing its hardware hash.</span></span> <span data-ttu-id="85fd9-118">Vous disposez de quatre options pour obtenir ces informations à partir d’appareils que vous utilisez déjà :</span><span class="sxs-lookup"><span data-stu-id="85fd9-118">You have four options for getting this information from devices you're already using:</span></span>

- <span data-ttu-id="85fd9-119">Demandez à votre fournisseur OEM le fichier d’enregistrement automatique du pilote automatique, qui inclut les hachages matériels.</span><span class="sxs-lookup"><span data-stu-id="85fd9-119">Ask your OEM supplier for the AutoPilot registration file, which will include the hardware hashes.</span></span>
- <span data-ttu-id="85fd9-120">Collectez des informations dans le [Gestionnaire de configuration de point de terminaison Microsoft](#microsoft-endpoint-configuration-manager).</span><span class="sxs-lookup"><span data-stu-id="85fd9-120">Collect information in [Microsoft Endpoint Configuration Manager](#microsoft-endpoint-configuration-manager).</span></span>
- <span data-ttu-id="85fd9-121">Exécutez un script Windows PowerShell, soit à l’aide d' [Active Directory](#active-directory-powershell-script-method) , soit [manuellement](#manual-powershell-script-method) sur chaque appareil, et recueillez les résultats dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="85fd9-121">Run a Windows PowerShell script--either by using [Active Directory](#active-directory-powershell-script-method) or [manually](#manual-powershell-script-method) on each device--and collect the results in a file.</span></span>
- <span data-ttu-id="85fd9-122">Démarrez chaque périphérique--mais ne terminez pas l’expérience d’installation Windows--et [collectez les hachages sur un lecteur flash amovible](#flash-drive-method).</span><span class="sxs-lookup"><span data-stu-id="85fd9-122">Start each device--but don't complete the Windows setup experience--and [collect the hashes on a removable flash drive](#flash-drive-method).</span></span>

#### <a name="microsoft-endpoint-configuration-manager"></a><span data-ttu-id="85fd9-123">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="85fd9-123">Microsoft Endpoint Configuration Manager</span></span>

<span data-ttu-id="85fd9-124">Vous pouvez utiliser le gestionnaire de configuration de point de terminaison Microsoft pour collecter les hachages matériels à partir des appareils existants que vous souhaitez enregistrer avec le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="85fd9-124">You can use Microsoft Endpoint Configuration Manager to collect the hardware hashes from existing devices that you want to register with Microsoft Managed Desktop.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85fd9-125">Tous les appareils pour lesquels vous souhaitez obtenir ces informations doivent exécuter Windows 10, version 1703 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85fd9-125">Any devices you want to get this information for must be running Windows 10, version 1703 or later.</span></span> 

<span data-ttu-id="85fd9-126">Si vous avez rempli toutes ces conditions préalables, vous êtes prêt à collecter les informations en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="85fd9-126">If you've met all these prerequisites, you're ready to collect the information by following these steps:</span></span>

1. <span data-ttu-id="85fd9-127">Dans la console Configuration Manager, sélectionnez **analyse**.</span><span class="sxs-lookup"><span data-stu-id="85fd9-127">In the Configuration Manager console, select **Monitoring**.</span></span> 
2. <span data-ttu-id="85fd9-128">Dans l’espace de travail analyse, développez le nœud **rapports** , développez **rapports**, puis sélectionnez le nœud **général matériel** .</span><span class="sxs-lookup"><span data-stu-id="85fd9-128">In the Monitoring workspace, expand the **Reporting** node, expand **Reports**, and select the **Hardware - General** node.</span></span> 
3. <span data-ttu-id="85fd9-129">Exécutez le rapport, les **informations du périphérique Windows AutoPilot**et affichez les résultats.</span><span class="sxs-lookup"><span data-stu-id="85fd9-129">Run the report, **Windows Autopilot Device Information**, and view the results.</span></span>
4. <span data-ttu-id="85fd9-130">Dans la visionneuse de rapports, sélectionnez l’icône **Exporter** , puis choisissez l’option **CSV (valeurs séparées par des virgules)** .</span><span class="sxs-lookup"><span data-stu-id="85fd9-130">In the report viewer, select the **Export** icon, and choose the **CSV (comma-delimited)** option.</span></span>
5. <span data-ttu-id="85fd9-131">Après avoir enregistré le fichier, vous devez filtrer les résultats sur les appareils que vous prévoyez de vous inscrire auprès du bureau géré Microsoft et charger les données dans le [portail d’administration](https://aka.ms/mmdportal)de bureau géré Microsoft, sélectionnez **appareils** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="85fd9-131">After saving the file, you will need to filter results to just those devices you plan to register with Microsoft Managed Desktop and upload the data to Microsoft Managed Desktop [Admin Portal](https://aka.ms/mmdportal), select **Devices** in the left navigation pane.</span></span> <span data-ttu-id="85fd9-132">Sélectionnez **+ inscrire les appareils**; le survol s’ouvre :</span><span class="sxs-lookup"><span data-stu-id="85fd9-132">Select **+ Register devices**; the fly-in opens:</span></span>


<span data-ttu-id="85fd9-133">Pour plus d’informations, reportez-vous à [la rubrique inscrire des appareils à l’aide du portail d’administration](#register-devices-by-using-the-admin-portal) .</span><span class="sxs-lookup"><span data-stu-id="85fd9-133">Refer to [Register devices by using the Admin Portal](#register-devices-by-using-the-admin-portal) for more information.</span></span>


#### <a name="active-directory-powershell-script-method"></a><span data-ttu-id="85fd9-134">Méthode de script PowerShell Active Directory</span><span class="sxs-lookup"><span data-stu-id="85fd9-134">Active Directory PowerShell script method</span></span>

<span data-ttu-id="85fd9-135">Dans un environnement Active Directory, vous pouvez utiliser l' `Get-WindowsAutoPilotInfo` applet de commande PowerShell pour collecter les informations à distance à partir de périphériques dans des groupes Active Directory à l’aide de WinRM.</span><span class="sxs-lookup"><span data-stu-id="85fd9-135">In an Active Directory environment, you can use the `Get-WindowsAutoPilotInfo` PowerShell cmdlet to remotely collect the information from devices in Active Directory Groups by using WinRM.</span></span> <span data-ttu-id="85fd9-136">Vous pouvez également utiliser l' `Get-AD Computer` applet de commande et obtenir des résultats filtrés pour les noms de modèle de matériel spécifiques inclus dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="85fd9-136">You can also use the `Get-AD Computer` cmdlet and get filtered results for a specific hardware model names included in the catalog.</span></span> <span data-ttu-id="85fd9-137">Pour ce faire, vérifiez d’abord ces conditions préalables, puis passez aux étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="85fd9-137">To do this, first confirm these prerequisites, and then proceed with the steps:</span></span>

- <span data-ttu-id="85fd9-138">WinRM est activé.</span><span class="sxs-lookup"><span data-stu-id="85fd9-138">WinRM is enabled.</span></span>
- <span data-ttu-id="85fd9-139">Les appareils que vous souhaitez enregistrer sont actifs sur le réseau (c’est-à-dire qu’ils ne sont pas déconnectés ou désactivés).</span><span class="sxs-lookup"><span data-stu-id="85fd9-139">The devices you want to register are active on the network (that is, they are not disconnected or turned off).</span></span>
- <span data-ttu-id="85fd9-140">Assurez-vous que vous disposez d’un paramètre d’informations d’identification de domaine qui a l’autorisation de s’exécuter à distance sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="85fd9-140">Make sure you have a domain credential parameter that has permission to execute remotely on the devices.</span></span>
- <span data-ttu-id="85fd9-141">Assurez-vous que le pare-feu Windows autorise l’accès à WMI.</span><span class="sxs-lookup"><span data-stu-id="85fd9-141">Make sure that Windows Firewall allows access to WMI.</span></span> <span data-ttu-id="85fd9-142">Pour ce faire, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="85fd9-142">To do that, follow these steps:</span></span>

    1. <span data-ttu-id="85fd9-143">Ouvrez le panneau de configuration du **pare-feu Windows Defender** et sélectionnez **autoriser une application ou une fonctionnalité via le pare-feu Windows Defender**.</span><span class="sxs-lookup"><span data-stu-id="85fd9-143">Open the **Windows Defender Firewall** control panel and select **Allow an app or feature through Windows Defender Firewall**.</span></span>
    
    2. <span data-ttu-id="85fd9-144">Recherchez **Windows Management Instrumentation (WMI)** dans la liste, activez à la fois **privé et public**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="85fd9-144">Find **Windows Management Instrumentation (WMI)** in the list, enable for both **Private and Public**, and then select **OK**.</span></span>

1.  <span data-ttu-id="85fd9-145">Ouvrez une invite PowerShell avec des droits d’administration.</span><span class="sxs-lookup"><span data-stu-id="85fd9-145">Open a PowerShell prompt with administrative rights.</span></span>

2.  <span data-ttu-id="85fd9-146">Exécutez l' *un* des scripts suivants :</span><span class="sxs-lookup"><span data-stu-id="85fd9-146">Run *either one* of these scripts:</span></span>

    ```powershell
    Install-script -name Get-WindowsAutoPilotInfo 
    #example one – leverage Get-ADComputer to enumerate devices 
    Get-ADComputer -filter * | powershell -ExecutionPolicy Unrestricted Get-WindowsAutoPilotInfo.ps1 -credential Domainname\<accountname>
    ```

    ```powershell 
    #example two – target specific devices: 
    Set-ExecutionPolicy powershell -ExecutionPolicy Unrestricted Get-WindowsAutoPilotInfo.ps1 -credential Domainname\<accountname> -Name Machine1,Machine2,Machine3
    ```

3. <span data-ttu-id="85fd9-147">Accéder à tous les répertoires où se trouvent des entrées pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="85fd9-147">Access any directories where there might be entries for the devices.</span></span> <span data-ttu-id="85fd9-148">Supprimez les entrées de chaque périphérique de *tous les* répertoires, y compris les services de domaine Active Directory Windows Server et Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="85fd9-148">Remove entries for each device from *all* directories, including Windows Server Active Directory Domain Services and Azure Active Directory.</span></span> <span data-ttu-id="85fd9-149">N’oubliez pas que cette suppression peut prendre quelques heures.</span><span class="sxs-lookup"><span data-stu-id="85fd9-149">Be aware that this removal could take a few hours to completely process.</span></span>

4. <span data-ttu-id="85fd9-150">Services de gestion d’accès où il peut y avoir des entrées pour les périphériques.</span><span class="sxs-lookup"><span data-stu-id="85fd9-150">Access management services where there might be entries for the devices.</span></span> <span data-ttu-id="85fd9-151">Supprimez les entrées de chaque périphérique de *tous les* services de gestion, y compris le gestionnaire de configuration de point de terminaison Microsoft, Microsoft Intune et Windows AutoPilot.</span><span class="sxs-lookup"><span data-stu-id="85fd9-151">Remove entries for each device from *all* management services, including Microsoft Endpoint Configuration Manager, Microsoft Intune, and Windows Autopilot.</span></span> <span data-ttu-id="85fd9-152">N’oubliez pas que cette suppression peut prendre quelques heures.</span><span class="sxs-lookup"><span data-stu-id="85fd9-152">Be aware that this removal could take a few hours to completely process.</span></span>

<span data-ttu-id="85fd9-153">À présent, vous pouvez procéder à l' [inscription des appareils](#register-devices-by-using-the-admin-portal).</span><span class="sxs-lookup"><span data-stu-id="85fd9-153">Now you can proceed to [register devices](#register-devices-by-using-the-admin-portal).</span></span>

#### <a name="manual-powershell-script-method"></a><span data-ttu-id="85fd9-154">Méthode de script PowerShell manuel</span><span class="sxs-lookup"><span data-stu-id="85fd9-154">Manual PowerShell script method</span></span>

1.  <span data-ttu-id="85fd9-155">Ouvrez une invite PowerShell avec des droits d’administration.</span><span class="sxs-lookup"><span data-stu-id="85fd9-155">Open a PowerShell prompt with administrative rights.</span></span>
2.  <span data-ttu-id="85fd9-156">Générer `Install-Script -Name Get-WindowsAutoPilotInfo`</span><span class="sxs-lookup"><span data-stu-id="85fd9-156">Run `Install-Script -Name Get-WindowsAutoPilotInfo`</span></span>
3.  <span data-ttu-id="85fd9-157">Générer `powershell -ExecutionPolicy Unrestricted Get-WindowsAutoPilotInfo -OutputFile <path>\hardwarehash.csv`</span><span class="sxs-lookup"><span data-stu-id="85fd9-157">Run `powershell -ExecutionPolicy Unrestricted Get-WindowsAutoPilotInfo -OutputFile <path>\hardwarehash.csv`</span></span>
4. [<span data-ttu-id="85fd9-158">Fusionnez les données de hachage.</span><span class="sxs-lookup"><span data-stu-id="85fd9-158">Merge the hash data.</span></span>](#merge-hash-data)

#### <a name="flash-drive-method"></a><span data-ttu-id="85fd9-159">Flash Drive, méthode</span><span class="sxs-lookup"><span data-stu-id="85fd9-159">Flash drive method</span></span>

1. <span data-ttu-id="85fd9-160">Sur un appareil autre que celui que vous enregistrez, insérez un lecteur USB.</span><span class="sxs-lookup"><span data-stu-id="85fd9-160">On a device other than the one you're registering, insert a USB drive.</span></span>
2. <span data-ttu-id="85fd9-161">Ouvrez une invite PowerShell avec des droits d’administration.</span><span class="sxs-lookup"><span data-stu-id="85fd9-161">Open a PowerShell prompt with administrative rights.</span></span>
3. <span data-ttu-id="85fd9-162">Générer `Save-Script -Name Get-WindowsAutoPilotInfo -Path <pathToUsb>`</span><span class="sxs-lookup"><span data-stu-id="85fd9-162">Run `Save-Script -Name Get-WindowsAutoPilotInfo -Path <pathToUsb>`</span></span>
4. <span data-ttu-id="85fd9-163">Activez l’appareil que vous enregistrez, mais *ne démarrez pas l’installation*.</span><span class="sxs-lookup"><span data-stu-id="85fd9-163">Turn on the device you are registering, but *do not start the setup experience*.</span></span> <span data-ttu-id="85fd9-164">Si vous démarrez accidentellement le programme d’installation, vous devrez réinitialiser ou recréer l’image de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="85fd9-164">If you accidentally start the setup experience, you'll have to reset or reimage the device.</span></span>
5. <span data-ttu-id="85fd9-165">Insérez le lecteur USB, puis appuyez sur MAJ + F10.</span><span class="sxs-lookup"><span data-stu-id="85fd9-165">Insert the USB drive, and then press SHIFT + F10.</span></span>
6. <span data-ttu-id="85fd9-166">Ouvrez une invite PowerShell avec des droits d’administration, puis exécutez `cd <pathToUsb>` .</span><span class="sxs-lookup"><span data-stu-id="85fd9-166">Open a PowerShell prompt with administrative rights, and then run `cd <pathToUsb>`.</span></span>
7. <span data-ttu-id="85fd9-167">Générer `Set-ExecutionPolicy -ExecutionPolicy Unrestricted`</span><span class="sxs-lookup"><span data-stu-id="85fd9-167">Run `Set-ExecutionPolicy -ExecutionPolicy Unrestricted`</span></span>
8. <span data-ttu-id="85fd9-168">Générer `.\Get-WindowsAutoPilotInfo -OutputFile <path>\hardwarehash.csv`</span><span class="sxs-lookup"><span data-stu-id="85fd9-168">Run `.\Get-WindowsAutoPilotInfo -OutputFile <path>\hardwarehash.csv`</span></span>
9. <span data-ttu-id="85fd9-169">Supprimez le lecteur USB, puis arrêtez l’appareil en exécutant `shutdown -s -t 0`</span><span class="sxs-lookup"><span data-stu-id="85fd9-169">Remove the USB drive, and then shut down the device by running `shutdown -s -t 0`</span></span>
10. [<span data-ttu-id="85fd9-170">Fusionnez les données de hachage.</span><span class="sxs-lookup"><span data-stu-id="85fd9-170">Merge the hash data.</span></span>](#merge-hash-data)

>[!IMPORTANT]
><span data-ttu-id="85fd9-171">Ne mettez pas sous tension le périphérique que vous enregistrez jusqu’à ce que vous ayez terminé son inscription.</span><span class="sxs-lookup"><span data-stu-id="85fd9-171">Do not power on the device you are registering again until you've completed registration for it.</span></span> 



### <a name="merge-hash-data"></a><span data-ttu-id="85fd9-172">Fusionner les données de hachage</span><span class="sxs-lookup"><span data-stu-id="85fd9-172">Merge hash data</span></span>

<span data-ttu-id="85fd9-173">Si vous avez collecté les données de hachage du matériel à l’aide de la méthode manuelle PowerShell ou Flash Drive, il vous faut maintenant que les données des fichiers CSV soient combinées en un seul fichier pour terminer l’inscription.</span><span class="sxs-lookup"><span data-stu-id="85fd9-173">If you collected the hardware hash data by the manual PowerShell or flash drive methods, you now need to have the data in the CSV files combined into a single file to complete registration.</span></span> <span data-ttu-id="85fd9-174">Voici un exemple de script PowerShell pour faciliter cette tâche :</span><span class="sxs-lookup"><span data-stu-id="85fd9-174">Here's a sample PowerShell script to make this easy:</span></span>

```powershell
Import-CSV -Path (Get-ChildItem -Filter *.csv) | ConvertTo-Csv -NoTypeInformation | % {$_.Replace('"', '')} | Out-File .\aggregatedDevices.csv
```

<span data-ttu-id="85fd9-175">Une fois les données hachées fusionnées dans un fichier CSV, vous pouvez maintenant [enregistrer les appareils](#register-devices-by-using-the-admin-portal).</span><span class="sxs-lookup"><span data-stu-id="85fd9-175">With the hash data merged into one CSV file, you can now proceed to [register the devices](#register-devices-by-using-the-admin-portal).</span></span>


#### <a name="register-devices-by-using-the-admin-portal"></a><span data-ttu-id="85fd9-176">Inscrire des appareils à l’aide du portail d’administration</span><span class="sxs-lookup"><span data-stu-id="85fd9-176">Register devices by using the Admin Portal</span></span>

<span data-ttu-id="85fd9-177">À partir du portail d' [administration](https://aka.ms/mmdportal)de bureau géré Microsoft, sélectionnez **périphériques** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="85fd9-177">From the Microsoft Managed Desktop [Admin Portal](https://aka.ms/mmdportal), select **Devices** in the left navigation pane.</span></span> <span data-ttu-id="85fd9-178">Sélectionnez **+ inscrire les appareils**; le survol s’ouvre :</span><span class="sxs-lookup"><span data-stu-id="85fd9-178">Select **+ Register devices**; the fly-in opens:</span></span>

<span data-ttu-id="85fd9-179">[![Entrée brusque après la sélection d’appareils de caisse, liste des appareils avec des colonnes pour les utilisateurs affectés, numéro de série, État, date de dernière vue et âge](../../media/new-registration-ui.png)](../../media/new-registration-ui.png)</span><span class="sxs-lookup"><span data-stu-id="85fd9-179">[![Fly-in after selecting Register devices, listing devices with columns for assigned users, serial number, status, last-seen date, and age](../../media/new-registration-ui.png)](../../media/new-registration-ui.png)</span></span>


<!--Registering any existing devices with Managed Desktop will completely re-image them; make sure you've backed up any important data prior to starting the registration process.-->


<span data-ttu-id="85fd9-180">Procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="85fd9-180">Follow these steps:</span></span>

1. <span data-ttu-id="85fd9-181">Dans **chargement du fichier**, indiquez le chemin d’accès au fichier CSV que vous avez créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="85fd9-181">In **File upload**, provide a path to the CSV file you created previously.</span></span>

1. <span data-ttu-id="85fd9-182">Sélectionnez **inscrire les appareils**.</span><span class="sxs-lookup"><span data-stu-id="85fd9-182">Select **Register devices**.</span></span> <span data-ttu-id="85fd9-183">Le système ajoute les périphériques à votre liste d’appareils sur le panneau des **appareils**, marqué comme **AutopilotRegistrationRequested**.</span><span class="sxs-lookup"><span data-stu-id="85fd9-183">The system will add the devices to your list of devices on the **Devices blade**, marked as **AutopilotRegistrationRequested**.</span></span> <span data-ttu-id="85fd9-184">L’inscription prend généralement moins de 10 minutes et, lorsque le périphérique s’affiche comme **prêt pour l’utilisateur** , ce qui signifie qu’il est prêt et qu’il attend qu’un utilisateur commence à utiliser.</span><span class="sxs-lookup"><span data-stu-id="85fd9-184">Registration typically takes less than 10 minutes, and when successful the device will show as **Ready for user** meaning it's ready and waiting for a user to start using.</span></span>


<span data-ttu-id="85fd9-185">Vous pouvez surveiller la progression de l’inscription de l’appareil sur la page principale **des périphériques de bureau gérés par Microsoft** .</span><span class="sxs-lookup"><span data-stu-id="85fd9-185">You can monitor the progress of device registration on the main **Microsoft Managed Desktop - Devices** page.</span></span> <span data-ttu-id="85fd9-186">Les États possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="85fd9-186">Possible states reported there include:</span></span>

| <span data-ttu-id="85fd9-187">État</span><span class="sxs-lookup"><span data-stu-id="85fd9-187">State</span></span> | <span data-ttu-id="85fd9-188">Description</span><span class="sxs-lookup"><span data-stu-id="85fd9-188">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="85fd9-189">AutopilotRegistrationRequested</span><span class="sxs-lookup"><span data-stu-id="85fd9-189">AutopilotRegistrationRequested</span></span> | <span data-ttu-id="85fd9-190">L’inscription n’est pas encore terminée.</span><span class="sxs-lookup"><span data-stu-id="85fd9-190">Registration is not done yet.</span></span> <span data-ttu-id="85fd9-191">Réactivez-vous plus tard.</span><span class="sxs-lookup"><span data-stu-id="85fd9-191">Check back later.</span></span> |
| <span data-ttu-id="85fd9-192">Échec de l’inscription</span><span class="sxs-lookup"><span data-stu-id="85fd9-192">Registration failed</span></span> | <span data-ttu-id="85fd9-193">L’inscription n’a pas pu aboutir.</span><span class="sxs-lookup"><span data-stu-id="85fd9-193">Registration could not be completed.</span></span> <span data-ttu-id="85fd9-194">Pour plus d’informations, consultez la rubrique [Troubleshooting Device Registration](#troubleshooting-device-registration) .</span><span class="sxs-lookup"><span data-stu-id="85fd9-194">Refer to [Troubleshooting device registration](#troubleshooting-device-registration) for more information.</span></span> |
| <span data-ttu-id="85fd9-195">Prêt pour l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="85fd9-195">Ready for user</span></span> | <span data-ttu-id="85fd9-196">L’inscription a réussi et l’appareil est maintenant prêt à être remis à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="85fd9-196">Registration succeeded and the device is now ready to be delivered to the user.</span></span> <span data-ttu-id="85fd9-197">Microsoft Managed Desktop les guide tout au long du paramétrage, il n’est donc pas nécessaire d’effectuer d’autres préparatifs.</span><span class="sxs-lookup"><span data-stu-id="85fd9-197">Microsoft Managed Desktop will guide them through first time set-up, so there’s no need for you to do any further preparations.</span></span> |
| <span data-ttu-id="85fd9-198">Actif</span><span class="sxs-lookup"><span data-stu-id="85fd9-198">Active</span></span> | <span data-ttu-id="85fd9-199">L’appareil a été remis à l’utilisateur et il a été enregistré auprès de votre client.</span><span class="sxs-lookup"><span data-stu-id="85fd9-199">The device has been delivered to the user and they have registered with your tenant.</span></span> <span data-ttu-id="85fd9-200">Cela indique également qu’ils utilisent régulièrement l’appareil.</span><span class="sxs-lookup"><span data-stu-id="85fd9-200">This also indicates that they are regularly using the device.</span></span> |
| <span data-ttu-id="85fd9-201">Inactive</span><span class="sxs-lookup"><span data-stu-id="85fd9-201">Inactive</span></span> | <span data-ttu-id="85fd9-202">L’appareil a été remis à l’utilisateur et il a été enregistré auprès de votre client.</span><span class="sxs-lookup"><span data-stu-id="85fd9-202">The device has been delivered to the user and they have registered with your tenant.</span></span> <span data-ttu-id="85fd9-203">Toutefois, ils n’ont pas utilisé le périphérique récemment (au cours des 7 derniers jours).</span><span class="sxs-lookup"><span data-stu-id="85fd9-203">However, they have not used the device recently (in the last 7 days).</span></span>  | 

#### <a name="troubleshooting-device-registration"></a><span data-ttu-id="85fd9-204">Dépannage de l’inscription de l’appareil</span><span class="sxs-lookup"><span data-stu-id="85fd9-204">Troubleshooting device registration</span></span>

| <span data-ttu-id="85fd9-205">Message d’erreur</span><span class="sxs-lookup"><span data-stu-id="85fd9-205">Error message</span></span> | <span data-ttu-id="85fd9-206">Détails</span><span class="sxs-lookup"><span data-stu-id="85fd9-206">Details</span></span> |
|---------------|-------------|
| <span data-ttu-id="85fd9-207">Appareil introuvable</span><span class="sxs-lookup"><span data-stu-id="85fd9-207">Device not found</span></span> | <span data-ttu-id="85fd9-208">Nous n’avons pas pu inscrire cet appareil, car nous n’avons pas pu trouver de correspondance pour le fabricant, le modèle ou le numéro de série fourni.</span><span class="sxs-lookup"><span data-stu-id="85fd9-208">We couldn’t register this device because we could not find a match for the provided manufacturer, model, or serial number.</span></span> <span data-ttu-id="85fd9-209">Vérifiez ces valeurs auprès de votre fournisseur d’appareils.</span><span class="sxs-lookup"><span data-stu-id="85fd9-209">Confirm these values with your device supplier.</span></span> |
| <span data-ttu-id="85fd9-210">Hachage matériel non valide</span><span class="sxs-lookup"><span data-stu-id="85fd9-210">Hardware hash not valid</span></span> | <span data-ttu-id="85fd9-211">Le hachage matériel que vous avez fourni pour cet appareil n’a pas été correctement mis en forme.</span><span class="sxs-lookup"><span data-stu-id="85fd9-211">The hardware hash you provided for this device was not formatted correctly.</span></span> <span data-ttu-id="85fd9-212">Vérifiez le hachage matériel, puis renvoyez-le.</span><span class="sxs-lookup"><span data-stu-id="85fd9-212">Double-check the hardware hash and then resubmit.</span></span> |
| <span data-ttu-id="85fd9-213">L’appareil est déjà enregistré</span><span class="sxs-lookup"><span data-stu-id="85fd9-213">Device already registered</span></span> | <span data-ttu-id="85fd9-214">Ce périphérique est déjà enregistré dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="85fd9-214">This device is already registered to your organization.</span></span> <span data-ttu-id="85fd9-215">Aucune autre action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="85fd9-215">No further action required.</span></span> |
| <span data-ttu-id="85fd9-216">Appareil revendiqué par une autre organisation</span><span class="sxs-lookup"><span data-stu-id="85fd9-216">Device claimed by another organization</span></span> | <span data-ttu-id="85fd9-217">Ce périphérique a déjà été revendiqué par une autre organisation.</span><span class="sxs-lookup"><span data-stu-id="85fd9-217">This device has already been claimed by another organization.</span></span> <span data-ttu-id="85fd9-218">Vérifiez auprès de votre fournisseur d’appareils.</span><span class="sxs-lookup"><span data-stu-id="85fd9-218">Check with your device supplier.</span></span> |
| <span data-ttu-id="85fd9-219">Erreur inattendue</span><span class="sxs-lookup"><span data-stu-id="85fd9-219">Unexpected error</span></span> | <span data-ttu-id="85fd9-220">Votre demande n’a pas pu être traitée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="85fd9-220">Your request could not be automatically processed.</span></span> <span data-ttu-id="85fd9-221">Contactez le support technique et indiquez l’ID de la demande : <requestId></span><span class="sxs-lookup"><span data-stu-id="85fd9-221">Contact Support and provide the Request ID: <requestId></span></span> |

### <a name="check-the-image"></a><span data-ttu-id="85fd9-222">Vérifier l’image</span><span class="sxs-lookup"><span data-stu-id="85fd9-222">Check the image</span></span>

<span data-ttu-id="85fd9-223">Si votre appareil vient d’un fournisseur de partenaires de bureau géré Microsoft, l’image doit être correcte.</span><span class="sxs-lookup"><span data-stu-id="85fd9-223">If your device has come from a Microsoft Managed Desktop partner supplier, the image should be correct.</span></span>

<span data-ttu-id="85fd9-224">Si vous le souhaitez, vous pouvez également appliquer l’image par vous-même.</span><span class="sxs-lookup"><span data-stu-id="85fd9-224">You’re also welcome to apply the image on your own if you prefer.</span></span> <span data-ttu-id="85fd9-225">Pour commencer, contactez le représentant Microsoft avec lequel vous travaillez et ils vous fourniront l’emplacement et les étapes à suivre pour appliquer l’image.</span><span class="sxs-lookup"><span data-stu-id="85fd9-225">To get started, contact the Microsoft representative you’re working with and they will provide you the location and steps for applying the image.</span></span>

### <a name="deliver-the-device"></a><span data-ttu-id="85fd9-226">Remise de l’appareil</span><span class="sxs-lookup"><span data-stu-id="85fd9-226">Deliver the device</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85fd9-227">Avant de remettre l’appareil à votre utilisateur, vérifiez que vous avez obtenu et appliqué les [licences appropriées](../get-ready/prerequisites.md) pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="85fd9-227">Before you hand off the device to your user, make sure you have obtained and applied the [appropriate licenses](../get-ready/prerequisites.md) for that user.</span></span>

<span data-ttu-id="85fd9-228">Si toutes les licences sont appliquées, vous pouvez [faire en sorte que vos utilisateurs soient prêts à utiliser les appareils](get-started-devices.md), puis votre utilisateur peut démarrer l’appareil et poursuivre l’installation de Windows.</span><span class="sxs-lookup"><span data-stu-id="85fd9-228">If all the licenses are applied, you can [get your users ready to use devices](get-started-devices.md), and then your user can start up the device and proceed through the Windows setup experience.</span></span>









