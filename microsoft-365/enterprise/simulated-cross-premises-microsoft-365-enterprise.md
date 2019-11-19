---
title: Réseau virtuel entre différents locaux simulé dans un environnement de test Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/14/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
description: 'Résumé : créer un réseau virtuel entre différents locaux simulé dans Microsoft Azure en tant qu’environnement de test Microsoft 365.'
ms.openlocfilehash: be753251670f882b277305f808354791efc38547
ms.sourcegitcommit: 9ee873c6a2f738a0c99921e036894b646742e706
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/15/2019
ms.locfileid: "38673310"
---
# <a name="simulated-cross-premises-virtual-network-in-a-microsoft-365-test-environment"></a><span data-ttu-id="0ba42-103">Réseau virtuel entre différents locaux simulé dans un environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0ba42-103">Simulated cross-premises virtual network in a Microsoft 365 test environment</span></span>

<span data-ttu-id="0ba42-104">*Ce Guide de Laboratoire Test peut être utilisé pour les environnements de test Microsoft 365 Entreprise et Office 365 Entreprise*.</span><span class="sxs-lookup"><span data-stu-id="0ba42-104">*This Test Lab Guide can be used for both Microsoft 365 Enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="0ba42-p101">Cet article vous guide tout au long de la création d’un environnement de cloud hybride simulé avec Microsoft Azure, à l’aide de deux réseaux virtuels Azure. Voici la configuration obtenue.</span><span class="sxs-lookup"><span data-stu-id="0ba42-p101">This article steps you through creating a simulated hybrid cloud environment with Microsoft Azure using two Azure virtual networks. Here is the resulting configuration.</span></span> 
  
![Phase 3 de l’environnement de test/développement de réseau virtuel intersites simulé, avec la machine virtuelle DC2 dans XPrem VNet](media/simulated-cross-premises-microsoft-365-enterprise/df458c56-022b-4688-ab18-056c3fd776b4.png)
  
<span data-ttu-id="0ba42-108">Cette configuration simule un environnement de production cloud hybride Azure IaaS et comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="0ba42-108">This simulates an Azure IaaS hybrid cloud production environment and consists of:</span></span>
  
- <span data-ttu-id="0ba42-109">Un réseau local simulé et simplifié hébergé dans un réseau virtuel Azure (réseau virtuel TestLab).</span><span class="sxs-lookup"><span data-stu-id="0ba42-109">A simulated and simplified on-premises network hosted in an Azure virtual network (the TestLab virtual network).</span></span>
    
- <span data-ttu-id="0ba42-110">Un réseau virtuel intersites simulé hébergé dans Azure (XPrem).</span><span class="sxs-lookup"><span data-stu-id="0ba42-110">A simulated cross-premises virtual network hosted in Azure (XPrem).</span></span>
    
- <span data-ttu-id="0ba42-111">Une relation d’homologation VNet entre les deux réseaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="0ba42-111">A VNet peering relationship between the two virtual networks.</span></span>
    
- <span data-ttu-id="0ba42-112">Un contrôleur de domaine secondaire dans le réseau virtuel XPrem.</span><span class="sxs-lookup"><span data-stu-id="0ba42-112">A secondary domain controller in the XPrem virtual network.</span></span>
    
<span data-ttu-id="0ba42-113">Ces éléments offrent une base commune à partir de laquelle vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="0ba42-113">This provides a basis and common starting point from which you can:</span></span> 
  
- <span data-ttu-id="0ba42-114">Développer et tester des applications dans un environnement cloud hybride Azure IaaS simulé.</span><span class="sxs-lookup"><span data-stu-id="0ba42-114">Develop and test applications in a simulated Azure IaaS hybrid cloud environment.</span></span>
    
- <span data-ttu-id="0ba42-115">Créer des configurations de test d’ordinateurs, certains au sein du réseau virtuel TestLab et d’autres au sein du réseau virtuel XPrem, afin de simuler les charges de travail informatiques dans un environnement cloud hybride.</span><span class="sxs-lookup"><span data-stu-id="0ba42-115">Create test configurations of computers, some within the TestLab virtual network and some within the XPrem virtual network, to simulate hybrid cloud-based IT workloads.</span></span>
    
<span data-ttu-id="0ba42-116">Les trois phases principales pour configurer cet environnement de développement/test sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0ba42-116">There are three major phases to setting up this dev/test environment:</span></span>
  
1. <span data-ttu-id="0ba42-117">Configurer le réseau virtuel TestLab.</span><span class="sxs-lookup"><span data-stu-id="0ba42-117">Configure the TestLab virtual network.</span></span>
    
2. <span data-ttu-id="0ba42-118">Créer le réseau virtuel intersites.</span><span class="sxs-lookup"><span data-stu-id="0ba42-118">Create the cross-premises virtual network.</span></span>
    
3. <span data-ttu-id="0ba42-119">Configurer DC2</span><span class="sxs-lookup"><span data-stu-id="0ba42-119">Configure DC2.</span></span>
    
> [!NOTE]
> <span data-ttu-id="0ba42-120">Cette configuration nécessite un abonnement payant à Azure.</span><span class="sxs-lookup"><span data-stu-id="0ba42-120">This configuration requires a paid Azure subscription.</span></span> 

<span data-ttu-id="0ba42-121">Vous pouvez utiliser l’environnement obtenu pour tester les fonctions et le bon fonctionnement de[Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise), par vous-même ou en suivant les conseils des [guides de laboratoire de test](m365-enterprise-test-lab-guides.md).</span><span class="sxs-lookup"><span data-stu-id="0ba42-121">You can use the resulting environment to test the features and functionality of [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise) with additional [Test Lab Guides](m365-enterprise-test-lab-guides.md) or on your own.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="0ba42-123">Cliquez [ici](media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="0ba42-123">Click [here](media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-configure-the-testlab-virtual-network"></a><span data-ttu-id="0ba42-124">Phase 1 : configurer le réseau virtuel TestLab</span><span class="sxs-lookup"><span data-stu-id="0ba42-124">Phase 1: Configure the TestLab virtual network</span></span>

<span data-ttu-id="0ba42-125">Suivez les instructions de la **phase 1**de la [configuration entreprise de base simulée](simulated-ent-base-configuration-microsoft-365-enterprise.md) pour configurer les ordinateurs DC1, APP1 et CLIENT1 du réseau virtuel Azure appelé TestLab.</span><span class="sxs-lookup"><span data-stu-id="0ba42-125">Use the instructions in **Phase 1** of the [simulated enterprise base configuration](simulated-ent-base-configuration-microsoft-365-enterprise.md) to configure the DC1, APP1, and CLIENT1 computers in the Azure virtual network named TestLab.</span></span>
  
<span data-ttu-id="0ba42-126">Il s’agit de votre configuration actuelle.</span><span class="sxs-lookup"><span data-stu-id="0ba42-126">This is your current configuration.</span></span> 
  
![Configuration de base d’une entreprise simulée dans Azure](media/simulated-cross-premises-microsoft-365-enterprise/25a010a6-c870-4690-b8f3-84421f8bc5c7.png)
  
## <a name="phase-2-create-the-xprem-virtual-network"></a><span data-ttu-id="0ba42-128">Phase 2 : Créer le réseau virtuel XPrem</span><span class="sxs-lookup"><span data-stu-id="0ba42-128">Phase 2: Create the XPrem virtual network</span></span>

<span data-ttu-id="0ba42-129">Dans cette phase, vous devez créer et configurer le nouveau réseau virtuel XPrem et le connecter au réseau virtuel TestLab avec l’homologation VNet.</span><span class="sxs-lookup"><span data-stu-id="0ba42-129">In this phase, you create and configure the new XPrem virtual network and then connect it to the TestLab virtual network with VNet peering.</span></span>
  
<span data-ttu-id="0ba42-130">Tout d’abord, démarrez une invite PowerShell Azure sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="0ba42-130">First, start an Azure PowerShell prompt on your local computer.</span></span>
  
> [!NOTE]
> <span data-ttu-id="0ba42-p102">Les ensembles de commandes suivants utilisent la dernière version d'Azure PowerShell. Reportez-vous à la rubrique relative à la [prise en main des cmdlets Azure PowerShell](https://docs.microsoft.com/powershell/azureps-cmdlets-docs/).</span><span class="sxs-lookup"><span data-stu-id="0ba42-p102">The following command sets use the latest version of Azure PowerShell. See [Get started with Azure PowerShell cmdlets](https://docs.microsoft.com/powershell/azureps-cmdlets-docs/).</span></span> 
  
<span data-ttu-id="0ba42-133">Connectez-vous à votre compte Azure avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="0ba42-133">Sign in to your Azure account with this command.</span></span>
  
```powershell
Connect-AzAccount
```

<span data-ttu-id="0ba42-134">Obtenez le nom de votre abonnement à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="0ba42-134">Get your subscription name using this command.</span></span>
  
```powershell
Get-AzSubscription | Sort Name | Select Name
```

<span data-ttu-id="0ba42-p103">Définissez votre abonnement Azure. Remplacez tout le texte entre guillemets, y compris les caractères \< et >, avec les noms corrects.</span><span class="sxs-lookup"><span data-stu-id="0ba42-p103">Set your Azure subscription. Replace everything within the quotes, including the \< and > characters, with the correct names.</span></span>
  
```powershell
$subscrName="<subscription name>"
Select-AzSubscription -SubscriptionName $subscrName
```

<span data-ttu-id="0ba42-137">Créez ensuite le réseau virtuel XPrem et protégez-le avec un groupe de sécurité réseau, à l’aide des commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="0ba42-137">Next, create the XPrem virtual network and protect it with a network security group with these commands.</span></span>
  
```powershell
$rgName="<name of the resource group that you used for your TestLab virtual network>"
$locName=(Get-AzResourceGroup -Name $rgName).Location
$Testnet=New-AzVirtualNetworkSubnetConfig -Name "Testnet" -AddressPrefix 192.168.0.0/24
New-AzVirtualNetwork -Name "XPrem" -ResourceGroupName $rgName -Location $locName -AddressPrefix 192.168.0.0/16 -Subnet $Testnet -DNSServer 10.0.0.4
$rule1=New-AzNetworkSecurityRuleConfig -Name "RDPTraffic" -Description "Allow RDP to all VMs on the subnet" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
New-AzNetworkSecurityGroup -Name "Testnet" -ResourceGroupName $rgName -Location $locName -SecurityRules $rule1
$vnet=Get-AzVirtualNetwork -ResourceGroupName $rgName -Name XPrem
$nsg=Get-AzNetworkSecurityGroup -Name "Testnet" -ResourceGroupName $rgName
Set-AzVirtualNetworkSubnetConfig -VirtualNetwork $vnet -Name "Testnet" -AddressPrefix 192.168.0.0/24 -NetworkSecurityGroup $nsg
$vnet | Set-AzVirtualNetwork
```

<span data-ttu-id="0ba42-138">Vous devez ensuite créer la relation d’homologation VNet entre les réseaux virtuels TestLab et XPrem, à l’aide des commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="0ba42-138">Next, you create the VNet peering relationship between the TestLab and XPrem VNets with these commands.</span></span>
  
```powershell
$rgName="<name of the resource group that you used for your TestLab virtual network>"
$vnet1=Get-AzVirtualNetwork -ResourceGroupName $rgName -Name TestLab
$vnet2=Get-AzVirtualNetwork -ResourceGroupName $rgName -Name XPrem
Add-AzVirtualNetworkPeering -Name TestLab2XPrem -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id
Add-AzVirtualNetworkPeering -Name XPrem2TestLab -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="0ba42-139">Il s’agit de votre configuration actuelle.</span><span class="sxs-lookup"><span data-stu-id="0ba42-139">This is your current configuration.</span></span> 
  
![Phase 2 de l’environnement de test/développement de réseau virtuel intersites simulé, avec XPrem VNet et la relation d’homologation VNet](media/simulated-cross-premises-microsoft-365-enterprise/cac5e999-69c7-4f4c-bfce-a7f4006115ef.png)
  
## <a name="phase-3-configure-dc2"></a><span data-ttu-id="0ba42-141">Phase 3 : Configurer DC2</span><span class="sxs-lookup"><span data-stu-id="0ba42-141">Phase 3: Configure DC2</span></span>

<span data-ttu-id="0ba42-142">Dans cette phase, vous devez créer la machine virtuelle DC2 dans le réseau virtuel XPrem, puis la configurer comme un contrôleur de domaine répliqué.</span><span class="sxs-lookup"><span data-stu-id="0ba42-142">In this phase, you create the DC2 virtual machine in the XPrem virtual network and then configure it as a replica domain controller.</span></span>
  
<span data-ttu-id="0ba42-p104">Tout d’abord, créez une machine virtuelle pour DC2. Exécutez ces commandes dans l’invite de commande Azure PowerShell sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="0ba42-p104">First, create a virtual machine for DC2. Run these commands at the Azure PowerShell command prompt on your local computer.</span></span>
  
```powershell
$rgName="<your resource group name>"
$locName=(Get-AzResourceGroup -Name $rgName).Location
$vnet=Get-AzVirtualNetwork -Name XPrem -ResourceGroupName $rgName
$pip=New-AzPublicIpAddress -Name DC2-PIP -ResourceGroupName $rgName -Location $locName -AllocationMethod Dynamic
$nic=New-AzNetworkInterface -Name DC2-NIC -ResourceGroupName $rgName -Location $locName -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $pip.Id -PrivateIpAddress 192.168.0.4
$vm=New-AzVMConfig -VMName DC2 -VMSize Standard_A1
$cred=Get-Credential -Message "Type the name and password of the local administrator account for DC2."
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName DC2 -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name "DC2-OS" -DiskSizeInGB 128 -CreateOption FromImage -StorageAccountType "Standard_LRS"
$diskConfig=New-AzDiskConfig -AccountType "Standard_LRS" -Location $locName -CreateOption Empty -DiskSizeGB 20
$dataDisk1=New-AzDisk -DiskName "DC2-DataDisk1" -Disk $diskConfig -ResourceGroupName $rgName
$vm=Add-AzVMDataDisk -VM $vm -Name "DC2-DataDisk1" -CreateOption Attach -ManagedDiskId $dataDisk1.Id -Lun 1
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm
```

<span data-ttu-id="0ba42-145">Ensuite, connectez-vous à la nouvelle machine virtuelle DC2 à partir du [portail Azure](https://portal.azure.com) à l’aide du nom de compte et du mot de passe de l’administrateur local.</span><span class="sxs-lookup"><span data-stu-id="0ba42-145">Next, connect to the new DC2 virtual machine from the [Azure portal](https://portal.azure.com) using its local administrator account name and password.</span></span>
  
<span data-ttu-id="0ba42-p105">Ensuite, configurez une règle de pare-feu Windows pour autoriser le trafic afin d’effectuer des tests de connectivité de base. Exécutez ces commandes à l’invite de commande Windows PowerShell de niveau administrateur sur DC2.</span><span class="sxs-lookup"><span data-stu-id="0ba42-p105">Next, configure a Windows Firewall rule to allow traffic for basic connectivity testing. From an administrator-level Windows PowerShell command prompt on DC2, run these commands.</span></span> 
  
```powershell
Set-NetFirewallRule -DisplayName "File and Printer Sharing (Echo Request - ICMPv4-In)" -enabled True
ping dc1.corp.contoso.com
```

<span data-ttu-id="0ba42-p106">La commande ping doit aboutir à quatre réponses réussies à partir de l’adresse IP 10.0.0.4. Il s’agit d’un test du trafic sur la relation d’homologation VNet.</span><span class="sxs-lookup"><span data-stu-id="0ba42-p106">The ping command should result in four successful replies from IP address 10.0.0.4. This is a test of traffic across the VNet peering relationship.</span></span> 
  
<span data-ttu-id="0ba42-150">Ensuite, ajoutez le disque de données supplémentaire en tant que nouveau volume avec la lettre de lecteur F: avec cette commande de l’invite de commande Windows PowerShell sur DC2.</span><span class="sxs-lookup"><span data-stu-id="0ba42-150">Next, add the extra data disk as a new volume with the drive letter F: with this command from the Windows PowerShell command prompt on DC2.</span></span>
  
```powershell
Get-Disk | Where PartitionStyle -eq "RAW" | Initialize-Disk -PartitionStyle MBR -PassThru | New-Partition -AssignDriveLetter -UseMaximumSize | Format-Volume -FileSystem NTFS -NewFileSystemLabel "WSAD Data"
```

<span data-ttu-id="0ba42-p107">Configurez ensuite DC2 en tant que contrôleur de domaine répliqué pour le domaine corp.contoso.com. Exécutez les commandes suivantes à partir de l’invite de commande Windows PowerShell sur DC2.</span><span class="sxs-lookup"><span data-stu-id="0ba42-p107">Next, configure DC2 as a replica domain controller for the corp.contoso.com domain. Run these commands from the Windows PowerShell command prompt on DC2.</span></span>
  
```powershell
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
Install-ADDSDomainController -Credential (Get-Credential CORP\User1) -DomainName "corp.contoso.com" -InstallDns:$true -DatabasePath "F:\NTDS" -LogPath "F:\Logs" -SysvolPath "F:\SYSVOL"
```

<span data-ttu-id="0ba42-153">Notez que vous devez fournir à la fois le mot de passe CORP\\User1 et le mot de passe du mode restauration des services d’annuaire, puis redémarrer DC2.</span><span class="sxs-lookup"><span data-stu-id="0ba42-153">Note that you are prompted to supply both the CORP\\User1 password and a Directory Services Restore Mode (DSRM) password, and to restart DC2.</span></span> 
  
<span data-ttu-id="0ba42-p108">Maintenant que le réseau virtuel XPrem possède son propre serveur DNS (DC2), vous devez configurer le réseau virtuel XPrem pour utiliser ce serveur DNS. Exécutez ces commandes à partir de l’invite de commande Azure PowerShell sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="0ba42-p108">Now that the XPrem virtual network has its own DNS server (DC2), you must configure the XPrem virtual network to use this DNS server. Run these commands from the Azure PowerShell command prompt on your local computer.</span></span>
  
```powershell
$vnet=Get-AzVirtualNetwork -ResourceGroupName $rgName -name "XPrem"
$vnet.DhcpOptions.DnsServers="192.168.0.4" 
Set-AzVirtualNetwork -VirtualNetwork $vnet
Restart-AzVM -ResourceGroupName $rgName -Name "DC2"
```

<span data-ttu-id="0ba42-p109">À partir du portail Azure sur votre ordinateur local, connectez-vous à DC1 avec les informations d’identification CORP\\User1. Pour configurer le domaine CORP afin que les ordinateurs et les utilisateurs utilisent leur contrôleur de domaine local pour l’authentification, exécutez les commandes suivantes à partir d’une invite de commande Windows PowerShell de niveau administrateur sur DC1.</span><span class="sxs-lookup"><span data-stu-id="0ba42-p109">From the Azure portal on your local computer, connect to DC1 with the CORP\\User1 credentials. To configure the CORP domain so that computers and users use their local domain controller for authentication, run these commands from an administrator-level Windows PowerShell command prompt on DC1.</span></span>
  
```powershell
New-ADReplicationSite -Name "TestLab" 
New-ADReplicationSite -Name "XPrem"
New-ADReplicationSubnet -Name "10.0.0.0/8" -Site "TestLab"
New-ADReplicationSubnet -Name "192.168.0.0/16" -Site "XPrem"
```

<span data-ttu-id="0ba42-158">Il s’agit de votre configuration actuelle.</span><span class="sxs-lookup"><span data-stu-id="0ba42-158">This is your current configuration.</span></span> 
  
![Phase 3 de l’environnement de test/développement de réseau virtuel intersites simulé, avec la machine virtuelle DC2 dans XPrem VNet](media/simulated-cross-premises-microsoft-365-enterprise/df458c56-022b-4688-ab18-056c3fd776b4.png)
  
<span data-ttu-id="0ba42-160">Votre environnement cloud hybride Azure simulé est prêt pour le test.</span><span class="sxs-lookup"><span data-stu-id="0ba42-160">Your simulated Azure hybrid cloud environment is now ready for testing.</span></span>
  
<span data-ttu-id="0ba42-161">Vous êtes désormais prêt à profiter des fonctionnalités supplémentaires de [Microsoft 365 Entreprise](https://www.microsoft.com/microsoft-365/enterprise).</span><span class="sxs-lookup"><span data-stu-id="0ba42-161">You are now ready to experiment with additional features of [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="0ba42-162">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="0ba42-162">Next steps</span></span>

<span data-ttu-id="0ba42-163">Découvrez les nouveaux ensembles de guides pour les tests de laboratoire :</span><span class="sxs-lookup"><span data-stu-id="0ba42-163">Explore these additional sets of Test Lab Guides:</span></span>
  
- [<span data-ttu-id="0ba42-164">Identité</span><span class="sxs-lookup"><span data-stu-id="0ba42-164">Identity</span></span>](m365-enterprise-test-lab-guides.md#identity)
- [<span data-ttu-id="0ba42-165">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="0ba42-165">Mobile device management</span></span>](m365-enterprise-test-lab-guides.md#mobile-device-management)
- [<span data-ttu-id="0ba42-166">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="0ba42-166">Information protection</span></span>](m365-enterprise-test-lab-guides.md#information-protection)

## <a name="see-also"></a><span data-ttu-id="0ba42-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ba42-167">See also</span></span>

[<span data-ttu-id="0ba42-168">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="0ba42-168">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="0ba42-169">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="0ba42-169">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="0ba42-170">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="0ba42-170">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
