---
title: Inscrivez vous-même les appareils existant
description: Inscrire les appareils réutilisés que vous avez peut-être déjà vous-même afin qu’ils soient gérés par Bureau géré Microsoft
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
f1.keywords:
- NOCSH
ms.author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
manager: laurawi
ms.topic: article
audience: Admin
ms.openlocfilehash: 1703e4ed4ea0f3306edf6fdf07ab9c97a9266d4f
ms.sourcegitcommit: 39609c4d8c432c8e7d7a31cb35c8020e5207385b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/30/2021
ms.locfileid: "51445565"
---
# <a name="register-existing-devices-yourself"></a><span data-ttu-id="f17f4-104">Inscrivez vous-même les appareils existant</span><span class="sxs-lookup"><span data-stu-id="f17f4-104">Register existing devices yourself</span></span>

>[!NOTE]
><span data-ttu-id="f17f4-105">Cette rubrique décrit les étapes à suivre pour réutiliser les appareils que vous avez déjà et les inscrire dans Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f17f4-105">This topic describes the steps for you to reuse devices you already have and register them in Microsoft Managed Desktop.</span></span> <span data-ttu-id="f17f4-106">Si vous travaillez avec de nouveaux appareils, suivez plutôt les étapes de l’enregistrement des nouveaux appareils dans Bureau géré [Microsoft.](register-devices-self.md)</span><span class="sxs-lookup"><span data-stu-id="f17f4-106">If you are working with brand-new devices, follow the steps in [Register new devices in Microsoft Managed Desktop yourself](register-devices-self.md) instead.</span></span>

<span data-ttu-id="f17f4-107">Le processus pour les partenaires est documenté dans la procédure [d’inscription](register-devices-partner.md)des appareils par les partenaires.</span><span class="sxs-lookup"><span data-stu-id="f17f4-107">The process for Partners is documented in [Steps for Partners to register devices](register-devices-partner.md).</span></span>

<span data-ttu-id="f17f4-108">Bureau géré Microsoft peut fonctionner avec de nouveaux appareils ou vous pouvez réutiliser les appareils que vous avez peut-être déjà (ce qui nécessitera de les réimager).</span><span class="sxs-lookup"><span data-stu-id="f17f4-108">Microsoft Managed Desktop can work with brand-new devices or you can reuse devices you might already have (which will require that you reimage them).</span></span> <span data-ttu-id="f17f4-109">Vous pouvez inscrire des appareils avec Bureau géré Microsoft dans le portail Microsoft Endpoint Manager.</span><span class="sxs-lookup"><span data-stu-id="f17f4-109">You can register devices with Microsoft Managed Desktop in the Microsoft Endpoint Manager portal.</span></span>

## <a name="prepare-to-register-existing-devices"></a><span data-ttu-id="f17f4-110">Préparer l’inscription des appareils existants</span><span class="sxs-lookup"><span data-stu-id="f17f4-110">Prepare to register existing devices</span></span>


<span data-ttu-id="f17f4-111">Pour inscrire des appareils existants, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f17f4-111">To register existing devices, follow these steps:</span></span>

1. [<span data-ttu-id="f17f4-112">Obtenez le hachage matériel pour chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="f17f4-112">Obtain the hardware hash for each device.</span></span>](#obtain-the-hardware-hash)
2. [<span data-ttu-id="f17f4-113">Fusionner les données de hachage</span><span class="sxs-lookup"><span data-stu-id="f17f4-113">Merge the hash data</span></span>](#merge-hash-data)
3. <span data-ttu-id="f17f4-114">[Enregistrez les appareils dans Bureau géré Microsoft](#register-devices-by-using-the-admin-portal).</span><span class="sxs-lookup"><span data-stu-id="f17f4-114">[Register the devices in Microsoft Managed Desktop](#register-devices-by-using-the-admin-portal).</span></span>
4. [<span data-ttu-id="f17f4-115">Vérifiez que l’image est correcte.</span><span class="sxs-lookup"><span data-stu-id="f17f4-115">Double-check that the image is correct.</span></span>](#check-the-image)
5. [<span data-ttu-id="f17f4-116">Remettre l’appareil</span><span class="sxs-lookup"><span data-stu-id="f17f4-116">Deliver the device</span></span>](#deliver-the-device)

### <a name="obtain-the-hardware-hash"></a><span data-ttu-id="f17f4-117">Obtenir le hachage matériel</span><span class="sxs-lookup"><span data-stu-id="f17f4-117">Obtain the hardware hash</span></span>

<span data-ttu-id="f17f4-118">Bureau géré Microsoft identifie chaque appareil de manière unique en référant son hachage matériel.</span><span class="sxs-lookup"><span data-stu-id="f17f4-118">Microsoft Managed Desktop identifies each device uniquely by referencing its hardware hash.</span></span> <span data-ttu-id="f17f4-119">Vous avez quatre options pour obtenir ces informations à partir des appareils que vous utilisez déjà :</span><span class="sxs-lookup"><span data-stu-id="f17f4-119">You have four options for getting this information from devices you're already using:</span></span>

- <span data-ttu-id="f17f4-120">Demandez à votre fournisseur OEM le fichier d’inscription AutoPilot, qui inclut les h biens matériels.</span><span class="sxs-lookup"><span data-stu-id="f17f4-120">Ask your OEM supplier for the AutoPilot registration file, which will include the hardware hashes.</span></span>
- <span data-ttu-id="f17f4-121">Collectez des informations [dans Microsoft Endpoint Configuration Manager.](#microsoft-endpoint-configuration-manager)</span><span class="sxs-lookup"><span data-stu-id="f17f4-121">Collect information in [Microsoft Endpoint Configuration Manager](#microsoft-endpoint-configuration-manager).</span></span>
- <span data-ttu-id="f17f4-122">Exécutez un Windows PowerShell script (à l’aide [](#manual-powershell-script-method) [d’Active Directory](#active-directory-powershell-script-method) ou manuellement sur chaque appareil) et collectez les résultats dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="f17f4-122">Run a Windows PowerShell script--either by using [Active Directory](#active-directory-powershell-script-method) or [manually](#manual-powershell-script-method) on each device--and collect the results in a file.</span></span>
- <span data-ttu-id="f17f4-123">Démarrez chaque appareil(mais ne terminez pas l’expérience d’installation de Windows) et collectez les [hages](#flash-drive-method)sur un lecteur flash amovible.</span><span class="sxs-lookup"><span data-stu-id="f17f4-123">Start each device--but don't complete the Windows setup experience--and [collect the hashes on a removable flash drive](#flash-drive-method).</span></span>

#### <a name="microsoft-endpoint-configuration-manager"></a><span data-ttu-id="f17f4-124">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f17f4-124">Microsoft Endpoint Configuration Manager</span></span>

<span data-ttu-id="f17f4-125">Vous pouvez utiliser Microsoft Endpoint Configuration Manager pour collecter les hages matériels à partir d’appareils existants que vous souhaitez inscrire auprès de Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f17f4-125">You can use Microsoft Endpoint Configuration Manager to collect the hardware hashes from existing devices that you want to register with Microsoft Managed Desktop.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f17f4-126">Tous les appareils pour qui vous souhaitez obtenir ces informations doivent être exécutant Windows 10, version 1703 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f17f4-126">Any devices you want to get this information for must be running Windows 10, version 1703 or later.</span></span> 

<span data-ttu-id="f17f4-127">Si vous avez satisfait à toutes ces conditions préalables, vous êtes prêt à collecter les informations en suivant les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f17f4-127">If you've met all these prerequisites, you're ready to collect the information by following these steps:</span></span>

1. <span data-ttu-id="f17f4-128">Dans la console Configuration Manager, sélectionnez **Analyse.**</span><span class="sxs-lookup"><span data-stu-id="f17f4-128">In the Configuration Manager console, select **Monitoring**.</span></span> 
2. <span data-ttu-id="f17f4-129">Dans l’espace de  travail Surveillance, développez le nœud Rapports, développez **Rapports** et sélectionnez le nœud Matériel **-** Général.</span><span class="sxs-lookup"><span data-stu-id="f17f4-129">In the Monitoring workspace, expand the **Reporting** node, expand **Reports**, and select the **Hardware - General** node.</span></span> 
3. <span data-ttu-id="f17f4-130">Exécutez le rapport, **Windows Autopilot Device Information** et affichez les résultats.</span><span class="sxs-lookup"><span data-stu-id="f17f4-130">Run the report, **Windows Autopilot Device Information**, and view the results.</span></span>
4. <span data-ttu-id="f17f4-131">Dans la visionneuse  de rapports, sélectionnez l’icône Exporter, puis choisissez l’option **CSV (délimitée** par des virgules).</span><span class="sxs-lookup"><span data-stu-id="f17f4-131">In the report viewer, select the **Export** icon, and choose the **CSV (comma-delimited)** option.</span></span>
5. <span data-ttu-id="f17f4-132">Après avoir enregistré le fichier, vous devez filtrer les résultats uniquement sur les appareils que vous prévoyez d’inscrire auprès de Bureau géré Microsoft et de charger les données sur Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f17f4-132">After saving the file, you will need to filter results to just those devices you plan to register with Microsoft Managed Desktop and upload the data to Microsoft Managed Desktop.</span></span> <span data-ttu-id="f17f4-133">Ouvrez Microsoft Endpoint Manager et accédez au menu **Appareils,** puis recherchez la section Bureau géré Microsoft et sélectionnez **Appareils.**</span><span class="sxs-lookup"><span data-stu-id="f17f4-133">Open Microsoft Endpoint Manager and navigate to the **Devices** menu, then look for Microsoft Managed Desktop section and select **Devices**.</span></span> <span data-ttu-id="f17f4-134">Sélectionnez **+ Inscrivez les** appareils, ce qui ouvre un fly-in pour inscrire de nouveaux appareils.</span><span class="sxs-lookup"><span data-stu-id="f17f4-134">Select **+ Register devices**, which opens a fly-in to register new devices.</span></span>


<span data-ttu-id="f17f4-135">Pour plus [d’informations, voir Inscrire](#register-devices-by-using-the-admin-portal) des appareils à l’aide du portail d’administration.</span><span class="sxs-lookup"><span data-stu-id="f17f4-135">Refer to [Register devices by using the Admin Portal](#register-devices-by-using-the-admin-portal) for more information.</span></span>


#### <a name="active-directory-powershell-script-method"></a><span data-ttu-id="f17f4-136">Méthode de script PowerShell Active Directory</span><span class="sxs-lookup"><span data-stu-id="f17f4-136">Active Directory PowerShell script method</span></span>

<span data-ttu-id="f17f4-137">Dans un environnement Active Directory, vous pouvez utiliser l’applet de commande PowerShell pour collecter à distance les informations des appareils des groupes Active Directory à l’aide de `Get-WindowsAutoPilotInfo` WinRM.</span><span class="sxs-lookup"><span data-stu-id="f17f4-137">In an Active Directory environment, you can use the `Get-WindowsAutoPilotInfo` PowerShell cmdlet to remotely collect the information from devices in Active Directory Groups by using WinRM.</span></span> <span data-ttu-id="f17f4-138">Vous pouvez également utiliser la cmdlet et obtenir des résultats filtrés pour un nom de modèle matériel spécifique `Get-AD Computer` inclus dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="f17f4-138">You can also use the `Get-AD Computer` cmdlet and get filtered results for a specific hardware model name included in the catalog.</span></span> <span data-ttu-id="f17f4-139">Avant de poursuivre, confirmez d’abord ces conditions préalables, puis procédez comme vous le souhaitez :</span><span class="sxs-lookup"><span data-stu-id="f17f4-139">Before you proceed, first confirm these prerequisites, and then proceed with the steps:</span></span>

- <span data-ttu-id="f17f4-140">WinRM est activé.</span><span class="sxs-lookup"><span data-stu-id="f17f4-140">WinRM is enabled.</span></span>
- <span data-ttu-id="f17f4-141">Les appareils que vous souhaitez inscrire sont actifs sur le réseau (c’est-à-dire qu’ils ne sont pas déconnectés ou désactivés).</span><span class="sxs-lookup"><span data-stu-id="f17f4-141">The devices you want to register are active on the network (that is, they are not disconnected or turned off).</span></span>
- <span data-ttu-id="f17f4-142">Assurez-vous que vous disposez d’un paramètre d’informations d’identification de domaine autorisé à s’exécuter à distance sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="f17f4-142">Make sure you have a domain credential parameter that has permission to execute remotely on the devices.</span></span>
- <span data-ttu-id="f17f4-143">Assurez-vous que le Pare-feu Windows autorise l’accès à WMI.</span><span class="sxs-lookup"><span data-stu-id="f17f4-143">Make sure that Windows Firewall allows access to WMI.</span></span> <span data-ttu-id="f17f4-144">Pour ce faire, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f17f4-144">To do that, follow these steps:</span></span>

    1. <span data-ttu-id="f17f4-145">Ouvrez le **panneau de Windows Defender pare-feu** et sélectionnez Autoriser une application ou une fonctionnalité **via Windows Defender pare-feu.**</span><span class="sxs-lookup"><span data-stu-id="f17f4-145">Open the **Windows Defender Firewall** control panel and select **Allow an app or feature through Windows Defender Firewall**.</span></span>
    
    2. <span data-ttu-id="f17f4-146">Recherchez **Windows Management Instrumentation (WMI)** dans la liste, activez pour privé et **public,** puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="f17f4-146">Find **Windows Management Instrumentation (WMI)** in the list, enable for both **Private and Public**, and then select **OK**.</span></span>

1.  <span data-ttu-id="f17f4-147">Ouvrez une invite PowerShell avec des droits d’administration.</span><span class="sxs-lookup"><span data-stu-id="f17f4-147">Open a PowerShell prompt with administrative rights.</span></span>

2.  <span data-ttu-id="f17f4-148">Exécutez *l’un* de ces scripts :</span><span class="sxs-lookup"><span data-stu-id="f17f4-148">Run *either one* of these scripts:</span></span>

    ```powershell
    Install-script -name Get-WindowsAutoPilotInfo 
    #example one – leverage Get-ADComputer to enumerate devices 
    Get-ADComputer -filter * | powershell -ExecutionPolicy Unrestricted Get-WindowsAutoPilotInfo.ps1 -credential Domainname\<accountname>
    ```

    ```powershell 
    #example two – target specific devices: 
    Set-ExecutionPolicy powershell -ExecutionPolicy Unrestricted Get-WindowsAutoPilotInfo.ps1 -credential Domainname\<accountname> -Name Machine1,Machine2,Machine3
    ```

3. <span data-ttu-id="f17f4-149">Accéder aux répertoires où il peut y avoir des entrées pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="f17f4-149">Access any directories where there might be entries for the devices.</span></span> <span data-ttu-id="f17f4-150">Supprimez les entrées de chaque appareil de *tous* les répertoires, y compris windows Server Active Directory Domain Services et Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f17f4-150">Remove entries for each device from *all* directories, including Windows Server Active Directory Domain Services and Azure Active Directory.</span></span> <span data-ttu-id="f17f4-151">N’ignorez pas que le processus de suppression peut prendre quelques heures.</span><span class="sxs-lookup"><span data-stu-id="f17f4-151">Be aware that removal could take a few hours to completely process.</span></span>

4. <span data-ttu-id="f17f4-152">Accéder aux services de gestion où il peut y avoir des entrées pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="f17f4-152">Access management services where there might be entries for the devices.</span></span> <span data-ttu-id="f17f4-153">Supprimez les entrées de chaque appareil de tous les services de gestion, y compris Microsoft Endpoint Configuration Manager, Microsoft Intune et Windows Autopilot. </span><span class="sxs-lookup"><span data-stu-id="f17f4-153">Remove entries for each device from *all* management services, including Microsoft Endpoint Configuration Manager, Microsoft Intune, and Windows Autopilot.</span></span> <span data-ttu-id="f17f4-154">N’ignorez pas que le processus de suppression peut prendre quelques heures.</span><span class="sxs-lookup"><span data-stu-id="f17f4-154">Be aware that removal could take a few hours to completely process.</span></span>

<span data-ttu-id="f17f4-155">Vous pouvez désormais inscrire [des appareils.](#register-devices-by-using-the-admin-portal)</span><span class="sxs-lookup"><span data-stu-id="f17f4-155">Now you can proceed to [register devices](#register-devices-by-using-the-admin-portal).</span></span>

#### <a name="manual-powershell-script-method"></a><span data-ttu-id="f17f4-156">Méthode de script PowerShell manuelle</span><span class="sxs-lookup"><span data-stu-id="f17f4-156">Manual PowerShell script method</span></span>

1.  <span data-ttu-id="f17f4-157">Ouvrez une invite PowerShell avec des droits d’administration.</span><span class="sxs-lookup"><span data-stu-id="f17f4-157">Open a PowerShell prompt with administrative rights.</span></span>
2.  <span data-ttu-id="f17f4-158">Exécuter `Install-Script -Name Get-WindowsAutoPilotInfo`</span><span class="sxs-lookup"><span data-stu-id="f17f4-158">Run `Install-Script -Name Get-WindowsAutoPilotInfo`</span></span>
3.  <span data-ttu-id="f17f4-159">Exécuter `powershell -ExecutionPolicy Unrestricted Get-WindowsAutoPilotInfo -OutputFile <path>\hardwarehash.csv`</span><span class="sxs-lookup"><span data-stu-id="f17f4-159">Run `powershell -ExecutionPolicy Unrestricted Get-WindowsAutoPilotInfo -OutputFile <path>\hardwarehash.csv`</span></span>
4. [<span data-ttu-id="f17f4-160">Fusionnez les données de hachage.</span><span class="sxs-lookup"><span data-stu-id="f17f4-160">Merge the hash data.</span></span>](#merge-hash-data)

#### <a name="flash-drive-method"></a><span data-ttu-id="f17f4-161">Méthode de lecteur Flash</span><span class="sxs-lookup"><span data-stu-id="f17f4-161">Flash drive method</span></span>

1. <span data-ttu-id="f17f4-162">Sur un appareil autre que celui que vous inscrivez, insérez un lecteur USB.</span><span class="sxs-lookup"><span data-stu-id="f17f4-162">On a device other than the one you're registering, insert a USB drive.</span></span>
2. <span data-ttu-id="f17f4-163">Ouvrez une invite PowerShell avec des droits d’administration.</span><span class="sxs-lookup"><span data-stu-id="f17f4-163">Open a PowerShell prompt with administrative rights.</span></span>
3. <span data-ttu-id="f17f4-164">Exécuter `Save-Script -Name Get-WindowsAutoPilotInfo -Path <pathToUsb>`</span><span class="sxs-lookup"><span data-stu-id="f17f4-164">Run `Save-Script -Name Get-WindowsAutoPilotInfo -Path <pathToUsb>`</span></span>
4. <span data-ttu-id="f17f4-165">Activer l’appareil que vous inscrivez, mais *ne démarrez pas l’expérience de configuration.*</span><span class="sxs-lookup"><span data-stu-id="f17f4-165">Turn on the device you are registering, but *do not start the setup experience*.</span></span> <span data-ttu-id="f17f4-166">Si vous démarrez accidentellement l’installation, vous devez réinitialiser ou réinitialiser l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f17f4-166">If you accidentally start the setup experience, you'll have to reset or reimage the device.</span></span>
5. <span data-ttu-id="f17f4-167">Insérez le lecteur USB, puis appuyez sur Shift + F10.</span><span class="sxs-lookup"><span data-stu-id="f17f4-167">Insert the USB drive, and then press SHIFT + F10.</span></span>
6. <span data-ttu-id="f17f4-168">Ouvrez une invite PowerShell avec des droits d’administration, puis exécutez `cd <pathToUsb>` .</span><span class="sxs-lookup"><span data-stu-id="f17f4-168">Open a PowerShell prompt with administrative rights, and then run `cd <pathToUsb>`.</span></span>
7. <span data-ttu-id="f17f4-169">Exécuter `Set-ExecutionPolicy -ExecutionPolicy Unrestricted`</span><span class="sxs-lookup"><span data-stu-id="f17f4-169">Run `Set-ExecutionPolicy -ExecutionPolicy Unrestricted`</span></span>
8. <span data-ttu-id="f17f4-170">Exécuter `.\Get-WindowsAutoPilotInfo -OutputFile <path>\hardwarehash.csv`</span><span class="sxs-lookup"><span data-stu-id="f17f4-170">Run `.\Get-WindowsAutoPilotInfo -OutputFile <path>\hardwarehash.csv`</span></span>
9. <span data-ttu-id="f17f4-171">Supprimez le lecteur USB, puis fermez l’appareil en exécutant `shutdown -s -t 0`</span><span class="sxs-lookup"><span data-stu-id="f17f4-171">Remove the USB drive, and then shut down the device by running `shutdown -s -t 0`</span></span>
10. [<span data-ttu-id="f17f4-172">Fusionnez les données de hachage.</span><span class="sxs-lookup"><span data-stu-id="f17f4-172">Merge the hash data.</span></span>](#merge-hash-data)

>[!IMPORTANT]
><span data-ttu-id="f17f4-173">N’alimentation sur l’appareil que vous inscrivez à nouveau tant que vous n’avez pas terminé l’inscription pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="f17f4-173">Do not power on the device you are registering again until you've completed registration for it.</span></span> 



### <a name="merge-hash-data"></a><span data-ttu-id="f17f4-174">Fusionner les données de hachage</span><span class="sxs-lookup"><span data-stu-id="f17f4-174">Merge hash data</span></span>

<span data-ttu-id="f17f4-175">Si vous avez collecté les données de hachage matériel par le manuel PowerShell ou les méthodes de disque mémoire flash, vous devez maintenant combiner les données dans les fichiers CSV en un seul fichier pour terminer l’inscription.</span><span class="sxs-lookup"><span data-stu-id="f17f4-175">If you collected the hardware hash data by the manual PowerShell or flash drive methods, you now need to have the data in the CSV files combined into a single file to complete registration.</span></span> <span data-ttu-id="f17f4-176">Voici un exemple de script PowerShell pour faciliter l’accès :</span><span class="sxs-lookup"><span data-stu-id="f17f4-176">Here's a sample PowerShell script to make it easy:</span></span>

```powershell
Import-CSV -Path (Get-ChildItem -Filter *.csv) | ConvertTo-Csv -NoTypeInformation | % {$_.Replace('"', '')} | Out-File .\aggregatedDevices.csv
```

<span data-ttu-id="f17f4-177">Une fois les données de hachage fusionnées dans un fichier CSV, vous pouvez désormais enregistrer [les appareils.](#register-devices-by-using-the-admin-portal)</span><span class="sxs-lookup"><span data-stu-id="f17f4-177">With the hash data merged into one CSV file, you can now proceed to [register the devices](#register-devices-by-using-the-admin-portal).</span></span>


#### <a name="register-devices-by-using-the-admin-portal"></a><span data-ttu-id="f17f4-178">Inscrire des appareils à l’aide du portail d’administration</span><span class="sxs-lookup"><span data-stu-id="f17f4-178">Register devices by using the Admin Portal</span></span>

<span data-ttu-id="f17f4-179">Dans [Microsoft Endpoint Manager,](https://endpoint.microsoft.com/)sélectionnez **Appareils** dans le volet de navigation gauche.</span><span class="sxs-lookup"><span data-stu-id="f17f4-179">In [Microsoft Endpoint Manager](https://endpoint.microsoft.com/), select **Devices** in the left navigation pane.</span></span> <span data-ttu-id="f17f4-180">Recherchez la section Bureau géré Microsoft du menu et sélectionnez **Appareils.**</span><span class="sxs-lookup"><span data-stu-id="f17f4-180">Look for the Microsoft Managed Desktop section of the menu and select **Devices**.</span></span> <span data-ttu-id="f17f4-181">Dans l’espace de travail Appareils de bureau gérés Microsoft, sélectionnez **+** Inscrivez les appareils, qui ouvre un fly-in pour inscrire de nouveaux appareils.</span><span class="sxs-lookup"><span data-stu-id="f17f4-181">In the Microsoft Managed Desktop Devices workspace, Select **+ Register devices**, which opens a fly-in to register new devices.</span></span>

<!-- Update with new picture [![Fly-in after selecting Register devices, listing devices with columns for assigned users, serial number, status, last-seen date, and age](../../media/new-registration-ui.png)](../../media/new-registration-ui.png) -->


<!--Registering any existing devices with Managed Desktop will completely re-image them; make sure you've backed up any important data prior to starting the registration process.-->


<span data-ttu-id="f17f4-182">Procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f17f4-182">Follow these steps:</span></span>

1. <span data-ttu-id="f17f4-183">Dans **le chargement de** fichier, fournissez un chemin d’accès au fichier CSV que vous avez créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="f17f4-183">In **File upload**, provide a path to the CSV file you created previously.</span></span>

1. <span data-ttu-id="f17f4-184">Sélectionnez **Enregistrer les appareils.**</span><span class="sxs-lookup"><span data-stu-id="f17f4-184">Select **Register devices**.</span></span> <span data-ttu-id="f17f4-185">Le système ajoute les appareils à votre liste d’appareils sur le blade **Devices**, marqué comme **Étant en attente d’inscription.**</span><span class="sxs-lookup"><span data-stu-id="f17f4-185">The system will add the devices to your list of devices on the **Devices blade**, marked as **Registration Pending**.</span></span> <span data-ttu-id="f17f4-186">L’inscription prend généralement moins de 10 minutes et, en cas de réussite, l’appareil s’affiche comme prêt pour l’utilisateur, ce qui signifie qu’il est prêt et attend qu’un utilisateur commence à l’utiliser. </span><span class="sxs-lookup"><span data-stu-id="f17f4-186">Registration typically takes less than 10 minutes, and when successful the device will show as **Ready for user** meaning it's ready and waiting for a user to start using.</span></span>


<span data-ttu-id="f17f4-187">Vous pouvez surveiller la progression de l’inscription de l’appareil sur la page principale.</span><span class="sxs-lookup"><span data-stu-id="f17f4-187">You can monitor the progress of device registration on the main page.</span></span> <span data-ttu-id="f17f4-188">Les états possibles signalés sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="f17f4-188">Possible states reported there include:</span></span>

| <span data-ttu-id="f17f4-189">État</span><span class="sxs-lookup"><span data-stu-id="f17f4-189">State</span></span> | <span data-ttu-id="f17f4-190">Description</span><span class="sxs-lookup"><span data-stu-id="f17f4-190">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="f17f4-191">Inscription en attente</span><span class="sxs-lookup"><span data-stu-id="f17f4-191">Registration Pending</span></span> | <span data-ttu-id="f17f4-192">L’inscription n’est pas encore terminée.</span><span class="sxs-lookup"><span data-stu-id="f17f4-192">Registration is not done yet.</span></span> <span data-ttu-id="f17f4-193">Revenir plus tard.</span><span class="sxs-lookup"><span data-stu-id="f17f4-193">Check back later.</span></span> |
| <span data-ttu-id="f17f4-194">Échec de l’inscription</span><span class="sxs-lookup"><span data-stu-id="f17f4-194">Registration failed</span></span> | <span data-ttu-id="f17f4-195">L’inscription n’a pas pu être terminée.</span><span class="sxs-lookup"><span data-stu-id="f17f4-195">Registration could not be completed.</span></span> <span data-ttu-id="f17f4-196">Pour plus [d’informations, voir](#troubleshooting-device-registration) Résolution des problèmes d’inscription de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f17f4-196">Refer to [Troubleshooting device registration](#troubleshooting-device-registration) for more information.</span></span> |
| <span data-ttu-id="f17f4-197">Prêt pour l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="f17f4-197">Ready for user</span></span> | <span data-ttu-id="f17f4-198">L’inscription a réussi et l’appareil est maintenant prêt à être remis à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f17f4-198">Registration succeeded and the device is now ready to be delivered to the user.</span></span> <span data-ttu-id="f17f4-199">Le Bureau géré Microsoft les guide tout au long de la première phase de mise en place, il n’est donc pas nécessaire d’y faire d’autres préparations.</span><span class="sxs-lookup"><span data-stu-id="f17f4-199">Microsoft Managed Desktop will guide them through first-time set-up, so there’s no need for you to do any further preparations.</span></span> |
| <span data-ttu-id="f17f4-200">Actif</span><span class="sxs-lookup"><span data-stu-id="f17f4-200">Active</span></span> | <span data-ttu-id="f17f4-201">L’appareil a été remis à l’utilisateur et il s’est inscrit auprès de votre client.</span><span class="sxs-lookup"><span data-stu-id="f17f4-201">The device has been delivered to the user and they have registered with your tenant.</span></span> <span data-ttu-id="f17f4-202">Cela indique également qu’ils utilisent régulièrement l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f17f4-202">This also indicates that they are regularly using the device.</span></span> |
| <span data-ttu-id="f17f4-203">Inactif</span><span class="sxs-lookup"><span data-stu-id="f17f4-203">Inactive</span></span> | <span data-ttu-id="f17f4-204">L’appareil a été remis à l’utilisateur et il s’est inscrit auprès de votre client.</span><span class="sxs-lookup"><span data-stu-id="f17f4-204">The device has been delivered to the user and they have registered with your tenant.</span></span> <span data-ttu-id="f17f4-205">Toutefois, ils n’ont pas utilisé l’appareil récemment (au cours des 7 derniers jours).</span><span class="sxs-lookup"><span data-stu-id="f17f4-205">However, they have not used the device recently (in the last 7 days).</span></span>  | 

#### <a name="troubleshooting-device-registration"></a><span data-ttu-id="f17f4-206">Résolution des problèmes d’inscription de l’appareil</span><span class="sxs-lookup"><span data-stu-id="f17f4-206">Troubleshooting device registration</span></span>

| <span data-ttu-id="f17f4-207">Message d’erreur</span><span class="sxs-lookup"><span data-stu-id="f17f4-207">Error message</span></span> | <span data-ttu-id="f17f4-208">Détails</span><span class="sxs-lookup"><span data-stu-id="f17f4-208">Details</span></span> |
|---------------|-------------|
| <span data-ttu-id="f17f4-209">Appareil in trouvé</span><span class="sxs-lookup"><span data-stu-id="f17f4-209">Device not found</span></span> | <span data-ttu-id="f17f4-210">Nous n’avons pas pu enregistrer cet appareil car nous n’avons pas pu trouver de correspondance pour le fabricant, le modèle ou le numéro de série fourni.</span><span class="sxs-lookup"><span data-stu-id="f17f4-210">We couldn’t register this device because we could not find a match for the provided manufacturer, model, or serial number.</span></span> <span data-ttu-id="f17f4-211">Confirmez ces valeurs auprès de votre fournisseur d’appareils.</span><span class="sxs-lookup"><span data-stu-id="f17f4-211">Confirm these values with your device supplier.</span></span> |
| <span data-ttu-id="f17f4-212">Hachage matériel non valide</span><span class="sxs-lookup"><span data-stu-id="f17f4-212">Hardware hash not valid</span></span> | <span data-ttu-id="f17f4-213">Le hachage matériel que vous avez fourni pour cet appareil n’a pas été mis en forme correctement.</span><span class="sxs-lookup"><span data-stu-id="f17f4-213">The hardware hash you provided for this device was not formatted correctly.</span></span> <span data-ttu-id="f17f4-214">Vérifiez à nouveau le hachage matériel, puis resoumettre.</span><span class="sxs-lookup"><span data-stu-id="f17f4-214">Double-check the hardware hash and then resubmit.</span></span> |
| <span data-ttu-id="f17f4-215">Appareil déjà inscrit</span><span class="sxs-lookup"><span data-stu-id="f17f4-215">Device already registered</span></span> | <span data-ttu-id="f17f4-216">Cet appareil est déjà inscrit dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f17f4-216">This device is already registered to your organization.</span></span> <span data-ttu-id="f17f4-217">Aucune action supplémentaire n’est requise.</span><span class="sxs-lookup"><span data-stu-id="f17f4-217">No further action required.</span></span> |
| <span data-ttu-id="f17f4-218">Appareil revendiqué par une autre organisation</span><span class="sxs-lookup"><span data-stu-id="f17f4-218">Device claimed by another organization</span></span> | <span data-ttu-id="f17f4-219">Cet appareil a déjà été revendiqué par une autre organisation.</span><span class="sxs-lookup"><span data-stu-id="f17f4-219">This device has already been claimed by another organization.</span></span> <span data-ttu-id="f17f4-220">Vérifiez auprès de votre fournisseur d’appareils.</span><span class="sxs-lookup"><span data-stu-id="f17f4-220">Check with your device supplier.</span></span> |
| <span data-ttu-id="f17f4-221">Erreur inattendue</span><span class="sxs-lookup"><span data-stu-id="f17f4-221">Unexpected error</span></span> | <span data-ttu-id="f17f4-222">Votre demande n’a pas pu être traitée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="f17f4-222">Your request could not be automatically processed.</span></span> <span data-ttu-id="f17f4-223">Contactez le support technique et fournissez l’ID de demande : <requestId></span><span class="sxs-lookup"><span data-stu-id="f17f4-223">Contact Support and provide the Request ID: <requestId></span></span> |

### <a name="check-the-image"></a><span data-ttu-id="f17f4-224">Vérifier l’image</span><span class="sxs-lookup"><span data-stu-id="f17f4-224">Check the image</span></span>

<span data-ttu-id="f17f4-225">Si votre appareil est issu d’un fournisseur de partenaire Bureau géré Microsoft, l’image doit être correcte.</span><span class="sxs-lookup"><span data-stu-id="f17f4-225">If your device has come from a Microsoft Managed Desktop partner supplier, the image should be correct.</span></span>

<span data-ttu-id="f17f4-226">Vous pouvez également appliquer l’image vous-même si vous préférez.</span><span class="sxs-lookup"><span data-stu-id="f17f4-226">You’re also welcome to apply the image on your own if you prefer.</span></span> <span data-ttu-id="f17f4-227">To get started, contact the Microsoft representative you’re working with and they will provide you the location and steps for applying the image.</span><span class="sxs-lookup"><span data-stu-id="f17f4-227">To get started, contact the Microsoft representative you’re working with and they will provide you the location and steps for applying the image.</span></span>

### <a name="deliver-the-device"></a><span data-ttu-id="f17f4-228">Remettre l’appareil</span><span class="sxs-lookup"><span data-stu-id="f17f4-228">Deliver the device</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f17f4-229">Avant de remettre l’appareil à votre utilisateur, assurez-vous que vous avez obtenu et appliqué les [licences](../get-ready/prerequisites.md) appropriées pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f17f4-229">Before you hand off the device to your user, make sure you have obtained and applied the [appropriate licenses](../get-ready/prerequisites.md) for that user.</span></span>

<span data-ttu-id="f17f4-230">Si toutes les licences sont appliquées, vous pouvez préparer vos utilisateurs à utiliser des [appareils,](get-started-devices.md)puis démarrer l’appareil et passer à l’expérience d’installation de Windows.</span><span class="sxs-lookup"><span data-stu-id="f17f4-230">If all the licenses are applied, you can [get your users ready to use devices](get-started-devices.md), and then your user can start up the device and proceed through the Windows setup experience.</span></span>









