---
title: Authentification fédérée haute disponibilité Phase 2 Configurer les contrôleurs de domaine
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/25/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
f1.keywords:
- CSH
ms.custom: Ent_Solutions
ms.assetid: 6b0eff4c-2c5e-4581-8393-a36f7b36a72f
description: 'Résumé : Configurez les contrôleurs de domaine et le serveur de synchronisation d’annuaires pour votre authentification fédérée haute disponibilité pour Microsoft 365 dans Microsoft Azure.'
ms.openlocfilehash: 1c3fd686ee553a57d66dcfd51a6045167a12de8a
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690005"
---
# <a name="high-availability-federated-authentication-phase-2-configure-domain-controllers"></a><span data-ttu-id="2596e-103">Authentification fédérée haute disponibilité, phase 2 : Configurer les contrôleurs de domaine</span><span class="sxs-lookup"><span data-stu-id="2596e-103">High availability federated authentication Phase 2: Configure domain controllers</span></span>

<span data-ttu-id="2596e-104">Dans cette phase de déploiement de la haute disponibilité pour l’authentification fédérée Microsoft 365 dans les services d’infrastructure Azure, vous configurez deux contrôleurs de domaine et le serveur de synchronisation d’annuaires dans le réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="2596e-104">In this phase of deploying high availability for Microsoft 365 federated authentication in Azure infrastructure services, you configure two domain controllers and the directory synchronization server in the Azure virtual network.</span></span> <span data-ttu-id="2596e-105">Les requêtes web client d’authentification peuvent ensuite être authentifiées dans le réseau virtuel Azure, plutôt que d’envoyer ce trafic d’authentification sur le VPN de site à site à votre réseau local.</span><span class="sxs-lookup"><span data-stu-id="2596e-105">Client web requests for authentication can then be authenticated in the Azure virtual network, rather than sending that authentication traffic across the site-to-site VPN connection to your on-premises network.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2596e-106">Les services AD FS (Active Directory Federation Services) ne peuvent pas utiliser Azure Active Directory (Azure AD) en remplacement des contrôleurs de domaine des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="2596e-106">Active Directory Federation Services (AD FS) cannot use Azure Active Directory (Azure AD) as a substitute for Active Directory Domain Services (AD DS) domain controllers.</span></span> 
  
<span data-ttu-id="2596e-107">Vous devez effectuer cette phase avant de passer à la phase 3 : Configurer les serveurs [AD FS](high-availability-federated-authentication-phase-3-configure-ad-fs-servers.md).</span><span class="sxs-lookup"><span data-stu-id="2596e-107">You must complete this phase before moving on to [Phase 3: Configure AD FS servers](high-availability-federated-authentication-phase-3-configure-ad-fs-servers.md).</span></span> <span data-ttu-id="2596e-108">Pour toutes les phases, voir Déployer l’authentification fédérée haute disponibilité pour [Microsoft 365 dans Azure.](deploy-high-availability-federated-authentication-for-microsoft-365-in-azure.md)</span><span class="sxs-lookup"><span data-stu-id="2596e-108">See [Deploy high availability federated authentication for Microsoft 365 in Azure](deploy-high-availability-federated-authentication-for-microsoft-365-in-azure.md) for all of the phases.</span></span>
  
## <a name="create-the-domain-controller-virtual-machines-in-azure"></a><span data-ttu-id="2596e-109">Créer les machines virtuelles du contrôleur de domaine dans Azure</span><span class="sxs-lookup"><span data-stu-id="2596e-109">Create the domain controller virtual machines in Azure</span></span>

<span data-ttu-id="2596e-110">Tout d'abord, vous devez remplir la colonne du **nom de la machine virtuelle** du tableau M et modifier les tailles de machine virtuelle selon vos besoins dans la colonne **Taille minimale**.</span><span class="sxs-lookup"><span data-stu-id="2596e-110">First, you need to fill out the **Virtual machine name** column of Table M and modify virtual machine sizes as needed in the **Minimum size** column.</span></span>
  
|<span data-ttu-id="2596e-111">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2596e-111">**Item**</span></span>|<span data-ttu-id="2596e-112">**Nom de la machine virtuelle**</span><span class="sxs-lookup"><span data-stu-id="2596e-112">**Virtual machine name**</span></span>|<span data-ttu-id="2596e-113">**Image de la galerie**</span><span class="sxs-lookup"><span data-stu-id="2596e-113">**Gallery image**</span></span>|<span data-ttu-id="2596e-114">**Type de stockage**</span><span class="sxs-lookup"><span data-stu-id="2596e-114">**Storage type**</span></span>|<span data-ttu-id="2596e-115">**Taille minimale**</span><span class="sxs-lookup"><span data-stu-id="2596e-115">**Minimum size**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2596e-116">1.</span><span class="sxs-lookup"><span data-stu-id="2596e-116">1.</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png) <span data-ttu-id="2596e-118"> (premier contrôleur de domaine, par exemple DC1)</span><span class="sxs-lookup"><span data-stu-id="2596e-118">(first domain controller, example DC1)</span></span>  <br/> |<span data-ttu-id="2596e-119">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="2596e-119">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="2596e-120">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="2596e-120">Standard_LRS</span></span>  <br/> |<span data-ttu-id="2596e-121">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="2596e-121">Standard_D2</span></span>  <br/> |
|<span data-ttu-id="2596e-122">2.</span><span class="sxs-lookup"><span data-stu-id="2596e-122">2.</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png) <span data-ttu-id="2596e-124"> (deuxième contrôleur de domaine, par exemple DC2)</span><span class="sxs-lookup"><span data-stu-id="2596e-124">(second domain controller, example DC2)</span></span>  <br/> |<span data-ttu-id="2596e-125">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="2596e-125">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="2596e-126">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="2596e-126">Standard_LRS</span></span>  <br/> |<span data-ttu-id="2596e-127">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="2596e-127">Standard_D2</span></span>  <br/> |
|<span data-ttu-id="2596e-128">3.</span><span class="sxs-lookup"><span data-stu-id="2596e-128">3.</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png) <span data-ttu-id="2596e-130">(serveur de synchronisation d’annuaires, exemple DS1)</span><span class="sxs-lookup"><span data-stu-id="2596e-130">(directory synchronization server, example DS1)</span></span>  <br/> |<span data-ttu-id="2596e-131">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="2596e-131">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="2596e-132">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="2596e-132">Standard_LRS</span></span>  <br/> |<span data-ttu-id="2596e-133">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="2596e-133">Standard_D2</span></span>  <br/> |
|<span data-ttu-id="2596e-134">4.</span><span class="sxs-lookup"><span data-stu-id="2596e-134">4.</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png) <span data-ttu-id="2596e-136">(premier serveur AD FS, par exemple ADFS1)</span><span class="sxs-lookup"><span data-stu-id="2596e-136">(first AD FS server, example ADFS1)</span></span>  <br/> |<span data-ttu-id="2596e-137">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="2596e-137">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="2596e-138">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="2596e-138">Standard_LRS</span></span>  <br/> |<span data-ttu-id="2596e-139">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="2596e-139">Standard_D2</span></span>  <br/> |
|<span data-ttu-id="2596e-140">5.</span><span class="sxs-lookup"><span data-stu-id="2596e-140">5.</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png) <span data-ttu-id="2596e-142">(second serveur AD FS, par exemple ADFS2)</span><span class="sxs-lookup"><span data-stu-id="2596e-142">(second AD FS server, example ADFS2)</span></span>  <br/> |<span data-ttu-id="2596e-143">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="2596e-143">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="2596e-144">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="2596e-144">Standard_LRS</span></span>  <br/> |<span data-ttu-id="2596e-145">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="2596e-145">Standard_D2</span></span>  <br/> |
|<span data-ttu-id="2596e-146">6.</span><span class="sxs-lookup"><span data-stu-id="2596e-146">6.</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png) <span data-ttu-id="2596e-148">(premier serveur proxy d’application web, exemple WEB1)</span><span class="sxs-lookup"><span data-stu-id="2596e-148">(first web application proxy server, example WEB1)</span></span>  <br/> |<span data-ttu-id="2596e-149">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="2596e-149">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="2596e-150">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="2596e-150">Standard_LRS</span></span>  <br/> |<span data-ttu-id="2596e-151">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="2596e-151">Standard_D2</span></span>  <br/> |
|<span data-ttu-id="2596e-152">7.</span><span class="sxs-lookup"><span data-stu-id="2596e-152">7.</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png) <span data-ttu-id="2596e-154">(second serveur proxy d’application web, exemple WEB2)</span><span class="sxs-lookup"><span data-stu-id="2596e-154">(second web application proxy server, example WEB2)</span></span>  <br/> |<span data-ttu-id="2596e-155">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="2596e-155">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="2596e-156">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="2596e-156">Standard_LRS</span></span>  <br/> |<span data-ttu-id="2596e-157">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="2596e-157">Standard_D2</span></span>  <br/> |
   
 <span data-ttu-id="2596e-158">**Tableau M - Machines virtuelles pour l’authentification fédérée haute disponibilité pour Microsoft 365 dans Azure**</span><span class="sxs-lookup"><span data-stu-id="2596e-158">**Table M - Virtual machines for the high availability federated authentication for Microsoft 365 in Azure**</span></span>
  
<span data-ttu-id="2596e-159">Pour obtenir la liste complète des tailles de machine virtuelle, reportez-vous à la rubrique [Tailles des machines virtuelles Windows dans Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-sizes).</span><span class="sxs-lookup"><span data-stu-id="2596e-159">For the complete list of virtual machine sizes, see [Sizes for virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-sizes).</span></span>
  
<span data-ttu-id="2596e-160">Le bloc de commandes Azure PowerShell suivant permet de créer les machines virtuelles pour les deux contrôleurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="2596e-160">The following Azure PowerShell command block creates the virtual machines for the two domain controllers.</span></span> <span data-ttu-id="2596e-161">Spécifiez les valeurs des variables, en supprimant les \< and > caractères.</span><span class="sxs-lookup"><span data-stu-id="2596e-161">Specify the values for the variables, removing the \< and > characters.</span></span> <span data-ttu-id="2596e-162">Notez que ce bloc de commandes Azure PowerShell utilise des valeurs provenant des tableaux suivants :</span><span class="sxs-lookup"><span data-stu-id="2596e-162">Note that this Azure PowerShell command block uses values from the following tables:</span></span>
  
- <span data-ttu-id="2596e-163">Tableau M, pour vos machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="2596e-163">Table M, for your virtual machines</span></span>
    
- <span data-ttu-id="2596e-164">Tableau R, pour vos groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="2596e-164">Table R, for your resource groups</span></span>
    
- <span data-ttu-id="2596e-165">Tableau V, pour vos paramètres de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="2596e-165">Table V, for your virtual network settings</span></span>
    
- <span data-ttu-id="2596e-166">Tableau S, pour vos sous-réseaux</span><span class="sxs-lookup"><span data-stu-id="2596e-166">Table S, for your subnets</span></span>
    
- <span data-ttu-id="2596e-167">Tableau I, pour vos adresses IP statiques</span><span class="sxs-lookup"><span data-stu-id="2596e-167">Table I, for your static IP addresses</span></span>
    
- <span data-ttu-id="2596e-168">Tableau A, pour vos groupes à haute disponibilité</span><span class="sxs-lookup"><span data-stu-id="2596e-168">Table A, for your availability sets</span></span>
    
<span data-ttu-id="2596e-169">Rappelez-vous que vous avez défini les tableaux R, V, S, I et A dans [la phase 1 : Configurer Azure](high-availability-federated-authentication-phase-1-configure-azure.md).</span><span class="sxs-lookup"><span data-stu-id="2596e-169">Recall that you defined Tables R, V, S, I, and A in [Phase 1: Configure Azure](high-availability-federated-authentication-phase-1-configure-azure.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="2596e-170">[!REMARQUE] Les ensembles de commandes suivants utilisent la dernière version d'Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2596e-170">The following command sets use the latest version of Azure PowerShell.</span></span> <span data-ttu-id="2596e-171">Voir [La mise en place d’Azure PowerShell.](https://docs.microsoft.com/powershell/azure/get-started-azureps)</span><span class="sxs-lookup"><span data-stu-id="2596e-171">See [Get started with Azure PowerShell](https://docs.microsoft.com/powershell/azure/get-started-azureps).</span></span> 
  
<span data-ttu-id="2596e-172">Lorsque vous avez indiqué toutes les valeurs correctes, exécutez le bloc résultant à l’invite de commandes Azure PowerShell ou dans l’environnement d'écriture de scripts intégré de Windows PowerShell (ISE) sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2596e-172">When you have supplied all the correct values, run the resulting block at the Azure PowerShell prompt or in the PowerShell Integrated Script Environment (ISE) on your local computer.</span></span>
  
> [!TIP]
> <span data-ttu-id="2596e-173">Pour générer des blocs de commandes PowerShell prêts à l’emploi en fonction de vos paramètres personnalisés, utilisez ce manuel de [configuration Microsoft Excel.](https://github.com/MicrosoftDocs/OfficeDocs-Enterprise/raw/live/Enterprise/downloads/O365FedAuthInAzure_Config.xlsx)</span><span class="sxs-lookup"><span data-stu-id="2596e-173">To generate ready-to-run PowerShell command blocks based on your custom settings, use this [Microsoft Excel configuration workbook](https://github.com/MicrosoftDocs/OfficeDocs-Enterprise/raw/live/Enterprise/downloads/O365FedAuthInAzure_Config.xlsx).</span></span> 

```powershell
# Set up variables common to both virtual machines
$locName="<your Azure location>"
$vnetName="<Table V - Item 1 - Value column>"
$subnetName="<Table S - Item 1 - Value column>"
$avName="<Table A - Item 1 - Availability set name column>"
$rgNameTier="<Table R - Item 1 - Resource group name column>"
$rgNameInfra="<Table R - Item 4 - Resource group name column>"

$rgName=$rgNameInfra
$vnet=Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgName
$subnet=Get-AzVirtualNetworkSubnetConfig -VirtualNetwork $vnet -Name $subnetName

$rgName=$rgNameTier
$avSet=Get-AzAvailabilitySet -Name $avName -ResourceGroupName $rgName 

# Create the first domain controller
$vmName="<Table M - Item 1 - Virtual machine name column>"
$vmSize="<Table M - Item 1 - Minimum size column>"
$staticIP="<Table I - Item 1 - Value column>"
$diskStorageType="<Table M - Item 1 - Storage type column>"
$diskSize=<size of the extra disk for Active Directory Domain Services (AD DS) data in GB>

$nic=New-AzNetworkInterface -Name ($vmName +"-NIC") -ResourceGroupName $rgName -Location $locName -Subnet $subnet -PrivateIpAddress $staticIP
$vm=New-AzVMConfig -VMName $vmName -VMSize $vmSize -AvailabilitySetId $avset.Id
$vm=Set-AzVMOSDisk -VM $vm -Name ($vmName +"-OS") -DiskSizeInGB 128 -CreateOption FromImage -StorageAccountType $diskStorageType
$diskConfig=New-AzDiskConfig -AccountType $diskStorageType -Location $locName -CreateOption Empty -DiskSizeGB $diskSize
$dataDisk1=New-AzDisk -DiskName ($vmName + "-DataDisk1") -Disk $diskConfig -ResourceGroupName $rgName
$vm=Add-AzVMDataDisk -VM $vm -Name ($vmName + "-DataDisk1") -CreateOption Attach -ManagedDiskId $dataDisk1.Id -Lun 1
$cred=Get-Credential -Message "Type the name and password of the local administrator account for the first domain controller." 
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName $vmName -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm

# Create the second domain controller
$vmName="<Table M - Item 2 - Virtual machine name column>"
$vmSize="<Table M - Item 2 - Minimum size column>"
$staticIP="<Table I - Item 2 - Value column>"
$diskStorageType="<Table M - Item 2 - Storage type column>"
$diskSize=<size of the extra disk for AD DS data in GB>

$nic=New-AzNetworkInterface -Name ($vmName +"-NIC") -ResourceGroupName $rgName -Location $locName -Subnet $subnet -PrivateIpAddress $staticIP
$vm=New-AzVMConfig -VMName $vmName -VMSize $vmSize -AvailabilitySetId $avset.Id
$vm=Set-AzVMOSDisk -VM $vm -Name ($vmName +"-OS") -DiskSizeInGB 128 -CreateOption FromImage -StorageAccountType $diskStorageType
$diskConfig=New-AzDiskConfig -AccountType $diskStorageType -Location $locName -CreateOption Empty -DiskSizeGB $diskSize
$dataDisk1=New-AzDisk -DiskName ($vmName + "-DataDisk1") -Disk $diskConfig -ResourceGroupName $rgName
$vm=Add-AzVMDataDisk -VM $vm -Name ($vmName + "-DataDisk1") -CreateOption Attach -ManagedDiskId $dataDisk1.Id -Lun 1
$cred=Get-Credential -Message "Type the name and password of the local administrator account for the second domain controller." 
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName $vmName -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm

# Create the directory synchronization server
$vmName="<Table M - Item 3 - Virtual machine name column>"
$vmSize="<Table M - Item 3 - Minimum size column>"
$staticIP="<Table I - Item 3 - Value column>"
$diskStorageType="<Table M - Item 3 - Storage type column>"

$nic=New-AzNetworkInterface -Name ($vmName +"-NIC") -ResourceGroupName $rgName -Location $locName -Subnet $subnet -PrivateIpAddress $staticIP
$vm=New-AzVMConfig -VMName $vmName -VMSize $vmSize

$cred=Get-Credential -Message "Type the name and password of the local administrator account for the directory synchronization server." 
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName $vmName -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name ($vmName +"-OS") -DiskSizeInGB 128 -CreateOption FromImage -StorageAccountType $diskStorageType
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm
```

> [!NOTE]
> <span data-ttu-id="2596e-p105">Étant donné que ces machines virtuelles sont destinées à une application intranet, aucune adresse IP publique ni étiquette de nom de domaine DNS ne leur est affectée et elles ne sont pas connectées à Internet. Toutefois, cela signifie également que vous ne pouvez pas vous y connecter à partir du portail Azure. L’option de **connexion** n’est pas disponible lorsque vous affichez les propriétés de la machine virtuelle. Utilisez l’accessoire de connexion Bureau à distance ou un autre outil de Bureau à distance pour vous connecter à la machine virtuelle à l’aide de son adresse IP privée ou de son nom DNS intranet.</span><span class="sxs-lookup"><span data-stu-id="2596e-p105">Because these virtual machines are for an intranet application, they are not assigned a public IP address or a DNS domain name label and exposed to the Internet. However, this also means that you cannot connect to them from the Azure portal. The **Connect** option is unavailable when you view the properties of the virtual machine. Use the Remote Desktop Connection accessory or another Remote Desktop tool to connect to the virtual machine using its private IP address or intranet DNS name.</span></span>
  
## <a name="configure-the-first-domain-controller"></a><span data-ttu-id="2596e-178">Configurer le premier contrôleur de domaine</span><span class="sxs-lookup"><span data-stu-id="2596e-178">Configure the first domain controller</span></span>

<span data-ttu-id="2596e-p106">Utilisez le client Bureau à distance de votre choix et créez une connexion de Bureau à distance pour la machine virtuelle du premier contrôleur de domaine. Utilisez son nom d’ordinateur ou son nom DNS intranet et les informations d’identification du compte Administrateur local.</span><span class="sxs-lookup"><span data-stu-id="2596e-p106">Use the remote desktop client of your choice and create a remote desktop connection to the first domain controller virtual machine. Use its intranet DNS or computer name and the credentials of the local administrator account.</span></span>
  
<span data-ttu-id="2596e-181">Ensuite, ajoutez le disque de données supplémentaire au premier contrôleur de domaine avec cette commande à partir d’une invite de commandes Windows PowerShell sur la machine virtuelle du premier contrôleur **de domaine**:</span><span class="sxs-lookup"><span data-stu-id="2596e-181">Next, add the extra data disk to the first domain controller with this command from a Windows PowerShell command prompt **on the first domain controller virtual machine**:</span></span>
  
```powershell
Get-Disk | Where PartitionStyle -eq "RAW" | Initialize-Disk -PartitionStyle MBR -PassThru | New-Partition -AssignDriveLetter -UseMaximumSize | Format-Volume -FileSystem NTFS -NewFileSystemLabel "WSAD Data"
```

<span data-ttu-id="2596e-182">Ensuite, testez la connectivité du premier contrôleur de domaine vers des emplacements du réseau de votre organisation à l'aide de la commande **ping** pour effectuer un test ping des noms et des adresses IP des ressources du réseau de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2596e-182">Next, test the first domain controller's connectivity to locations on your organization network by using the **ping** command to ping names and IP addresses of resources on your organization network.</span></span>
  
<span data-ttu-id="2596e-p107">Cette procédure permet de vérifier que la résolution de noms DNS fonctionne correctement (que la machine virtuelle est configurée correctement avec les serveurs DNS locaux) et que des paquets peuvent être envoyés vers et depuis le réseau virtuel intersites. Si ce test de base échoue, contactez votre service informatique pour résoudre les problèmes de résolution de noms DNS et de livraison de paquets.</span><span class="sxs-lookup"><span data-stu-id="2596e-p107">This procedure ensures that DNS name resolution is working correctly (that the virtual machine is correctly configured with on-premises DNS servers) and that packets can be sent to and from the cross-premises virtual network. If this basic test fails, contact your IT department to troubleshoot the DNS name resolution and packet delivery issues.</span></span>
  
<span data-ttu-id="2596e-185">Ensuite, à partir de l’invite de commandes Windows PowerShell sur le premier contrôleur de domaine, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2596e-185">Next, from the Windows PowerShell command prompt on the first domain controller, run the following commands:</span></span>
  
```powershell
$domname="<DNS domain name of the domain for which this computer will be a domain controller, such as corp.contoso.com>"
$cred = Get-Credential -Message "Enter credentials of an account with permission to join a new domain controller to the domain"
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
Install-ADDSDomainController -InstallDns -DomainName $domname  -DatabasePath "F:\NTDS" -SysvolPath "F:\SYSVOL" -LogPath "F:\Logs" -Credential $cred
```

<span data-ttu-id="2596e-p108">Vous êtes invité à fournir les informations d’identification d’un compte Administrateur de domaine. L’ordinateur redémarre.</span><span class="sxs-lookup"><span data-stu-id="2596e-p108">You will be prompted to supply the credentials of a domain administrator account. The computer will restart.</span></span>
  
## <a name="configure-the-second-domain-controller"></a><span data-ttu-id="2596e-188">Configurer le deuxième contrôleur de domaine</span><span class="sxs-lookup"><span data-stu-id="2596e-188">Configure the second domain controller</span></span>

<span data-ttu-id="2596e-p109">Utilisez le client Bureau à distance de votre choix et créez une connexion de Bureau à distance pour la machine virtuelle du deuxième contrôleur de domaine. Utilisez son nom d’ordinateur ou son nom DNS intranet et les informations d’identification du compte Administrateur local.</span><span class="sxs-lookup"><span data-stu-id="2596e-p109">Use the remote desktop client of your choice and create a remote desktop connection to the second domain controller virtual machine. Use its intranet DNS or computer name and the credentials of the local administrator account.</span></span>
  
<span data-ttu-id="2596e-191">Ensuite, vous devez ajouter le disque de données supplémentaire au deuxième contrôleur de domaine avec cette commande à partir d’une invite de commandes Windows PowerShell sur la machine virtuelle du deuxième contrôleur **de** domaine :</span><span class="sxs-lookup"><span data-stu-id="2596e-191">Next, you need to add the extra data disk to the second domain controller with this command from a Windows PowerShell command prompt **on the second domain controller virtual machine**:</span></span>
  
```powershell
Get-Disk | Where PartitionStyle -eq "RAW" | Initialize-Disk -PartitionStyle MBR -PassThru | New-Partition -AssignDriveLetter -UseMaximumSize | Format-Volume -FileSystem NTFS -NewFileSystemLabel "WSAD Data"
```

<span data-ttu-id="2596e-192">Ensuite, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2596e-192">Next, run the following commands:</span></span>
  
```powershell
$domname="<DNS domain name of the domain for which this computer will be a domain controller, such as corp.contoso.com>"
$cred = Get-Credential -Message "Enter credentials of an account with permission to join a new domain controller to the domain"
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
Install-ADDSDomainController -InstallDns -DomainName $domname  -DatabasePath "F:\NTDS" -SysvolPath "F:\SYSVOL" -LogPath "F:\Logs" -Credential $cred

```

<span data-ttu-id="2596e-p110">Vous êtes invité à fournir les informations d’identification d’un compte Administrateur de domaine. L’ordinateur redémarre.</span><span class="sxs-lookup"><span data-stu-id="2596e-p110">You will be prompted to supply the credentials of a domain administrator account. The computer will restart.</span></span>
  
<span data-ttu-id="2596e-195">Ensuite, vous devez mettre à jour les serveurs DNS pour votre réseau virtuel afin que Azure affecte aux machines virtuelles les adresses IP des deux nouveaux contrôleurs de domaine à utiliser comme serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="2596e-195">Next, you need to update the DNS servers for your virtual network so that Azure assigns virtual machines the IP addresses of the two new domain controllers to use as their DNS servers.</span></span> <span data-ttu-id="2596e-196">Remplissez les variables, puis exécutez ces commandes à partir d’Windows PowerShell invite de commandes sur votre ordinateur local :</span><span class="sxs-lookup"><span data-stu-id="2596e-196">Fill in the variables and then run these commands from a Windows PowerShell command prompt on your local computer:</span></span>
  
```powershell
$rgName="<Table R - Item 4 - Resource group name column>"
$adrgName="<Table R - Item 1 - Resource group name column>"
$locName="<your Azure location>"
$vnetName="<Table V - Item 1 - Value column>"
$onpremDNSIP1="<Table D - Item 1 - DNS server IP address column>"
$onpremDNSIP2="<Table D - Item 2 - DNS server IP address column>"
$staticIP1="<Table I - Item 1 - Value column>"
$staticIP2="<Table I - Item 2 - Value column>"
$firstDCName="<Table M - Item 1 - Virtual machine name column>"
$secondDCName="<Table M - Item 2 - Virtual machine name column>"

$vnet=Get-AzVirtualNetwork -ResourceGroupName $rgName -Name $vnetName
$vnet.DhcpOptions.DnsServers.Add($staticIP1)
$vnet.DhcpOptions.DnsServers.Add($staticIP2) 
$vnet.DhcpOptions.DnsServers.Remove($onpremDNSIP1)
$vnet.DhcpOptions.DnsServers.Remove($onpremDNSIP2) 
Set-AzVirtualNetwork -VirtualNetwork $vnet
Restart-AzVM -ResourceGroupName $adrgName -Name $firstDCName
Restart-AzVM -ResourceGroupName $adrgName -Name $secondDCName
```

<span data-ttu-id="2596e-p112">Notez que nous redémarrons les deux contrôleurs de domaine afin qu’ils ne soient pas configurés avec les serveurs DNS locaux comme serveurs DNS. Comme ils sont tous les deux des serveurs DNS, ils ont été automatiquement configurés avec les serveurs DNS locaux comme redirecteurs DNS lorsqu’ils ont été promus comme contrôleurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="2596e-p112">Note that we restart the two domain controllers so that they are not configured with the on-premises DNS servers as DNS servers. Because they are both DNS servers themselves, they were automatically configured with the on-premises DNS servers as DNS forwarders when they were promoted to domain controllers.</span></span>
  
<span data-ttu-id="2596e-p113">Ensuite, nous devons créer un site de réplication Active Directory pour vérifier que les serveurs du réseau virtuel Azure utilisent les contrôleurs de domaine locaux. Connectez-vous à l’un des contrôleurs de domaine avec un compte Administrateur de domaine et exécutez les commandes suivantes à partir d’une invite de commandes Windows PowerShell au niveau de l’administrateur :</span><span class="sxs-lookup"><span data-stu-id="2596e-p113">Next, we need to create an Active Directory replication site to ensure that servers in the Azure virtual network use the local domain controllers. Connect to either domain controller with a domain administrator account and run the following commands from an administrator-level Windows PowerShell prompt:</span></span>
  
```powershell
$vnet="<Table V - Item 1 - Value column>"
$vnetSpace="<Table V - Item 4 - Value column>"
New-ADReplicationSite -Name $vnet 
New-ADReplicationSubnet -Name $vnetSpace -Site $vnet
```

## <a name="configure-the-directory-synchronization-server"></a><span data-ttu-id="2596e-201">Configurer le serveur de synchronisation d’annuaires</span><span class="sxs-lookup"><span data-stu-id="2596e-201">Configure the directory synchronization server</span></span>

<span data-ttu-id="2596e-202">Utilisez le client Bureau à distance de votre choix et créez une connexion bureau à distance à la machine virtuelle du serveur de synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="2596e-202">Use the remote desktop client of your choice and create a remote desktop connection to the directory synchronization server virtual machine.</span></span> <span data-ttu-id="2596e-203">Utilisez son nom d'ordinateur ou son nom DNS intranet et les informations d'identification du compte Administrateur local.</span><span class="sxs-lookup"><span data-stu-id="2596e-203">Use its intranet DNS or computer name and the credentials of the local administrator account.</span></span>
  
<span data-ttu-id="2596e-204">Ensuite, joignez-le au domaine AD DS approprié avec ces commandes à l’invite Windows PowerShell suivante.</span><span class="sxs-lookup"><span data-stu-id="2596e-204">Next, join it to the appropriate AD DS domain with these commands at the Windows PowerShell prompt.</span></span>
  
```powershell
$domName="<AD DS domain name to join, such as corp.contoso.com>"
$cred=Get-Credential -Message "Type the name and password of a domain acccount."
Add-Computer -DomainName $domName -Credential $cred
Restart-Computer
```

<span data-ttu-id="2596e-205">Lorsque cette phase est terminée, voici la configuration résultante, avec les noms d’ordinateur de l’espace réservé.</span><span class="sxs-lookup"><span data-stu-id="2596e-205">Here is the configuration resulting from the successful completion of this phase, with placeholder computer names.</span></span>
  
<span data-ttu-id="2596e-206">**Phase 2 : Contrôleurs de domaine et serveur de synchronisation d’annuaires pour votre infrastructure d’authentification fédérée haute disponibilité dans Azure**</span><span class="sxs-lookup"><span data-stu-id="2596e-206">**Phase 2: The domain controllers and directory synchronization server for your high availability federated authentication infrastructure in Azure**</span></span>

![Phase 2 de l’infrastructure d’authentification fédérée Microsoft 365 haute disponibilité dans Azure avec les contrôleurs de domaine](../media/b0c1013b-3fb4-499e-93c1-bf310d8f4c32.png)
  
## <a name="next-step"></a><span data-ttu-id="2596e-208">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="2596e-208">Next step</span></span>

<span data-ttu-id="2596e-209">Utilisez [la phase 3 : Configurez les serveurs AD FS](high-availability-federated-authentication-phase-3-configure-ad-fs-servers.md) pour continuer à configurer cette charge de travail.</span><span class="sxs-lookup"><span data-stu-id="2596e-209">Use [Phase 3: Configure AD FS servers](high-availability-federated-authentication-phase-3-configure-ad-fs-servers.md) to continue configuring this workload.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2596e-210">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2596e-210">See Also</span></span>

[<span data-ttu-id="2596e-211">Déployer une authentification fédérée haute disponibilité pour Microsoft 365 dans Azure</span><span class="sxs-lookup"><span data-stu-id="2596e-211">Deploy high availability federated authentication for Microsoft 365 in Azure</span></span>](deploy-high-availability-federated-authentication-for-microsoft-365-in-azure.md)
  
[<span data-ttu-id="2596e-212">Identité fédérée pour votre environnement de test/dev Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2596e-212">Federated identity for your Microsoft 365 dev/test environment</span></span>](federated-identity-for-your-microsoft-365-dev-test-environment.md)
  
[<span data-ttu-id="2596e-213">Centre de solutions et d'architecture Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2596e-213">Microsoft 365 solution and architecture center</span></span>](../solutions/solution-architecture-center.md)


