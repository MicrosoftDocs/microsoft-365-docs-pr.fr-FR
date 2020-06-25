---
title: Configuration de base d’une entreprise simulée pour Microsoft 365
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/21/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom:
- Ent_TLGs
- seo-marvel-apr2020
ms.assetid: 6f916a77-301c-4be2-b407-6cec4d80df76
description: Utilisez ce Guide de Laboratoire Test afin de créer une simulation d’environnement de test dédiée à Microsoft 365 Entreprise.
ms.openlocfilehash: 486429bf9e1c0a88c9beb01a092f968256c1fa77
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44818494"
---
# <a name="the-simulated-enterprise-base-configuration"></a><span data-ttu-id="27c7e-103">Configuration de base d’une entreprise simulée</span><span class="sxs-lookup"><span data-stu-id="27c7e-103">The simulated enterprise base configuration</span></span>

<span data-ttu-id="27c7e-104">*Ce Guide de Laboratoire Test peut être utilisé pour les environnements de test Microsoft 365 Enterprise et Office 365 Enterprise.*</span><span class="sxs-lookup"><span data-stu-id="27c7e-104">*This Test Lab Guide can be used for both Microsoft 365 Enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="27c7e-105">Vous trouverez dans cet article des instructions détaillées pour créer un environnement simplifié pour Microsoft 365 Entreprise qui comprend :</span><span class="sxs-lookup"><span data-stu-id="27c7e-105">This article provides you with step-by-step instructions to create a simplified environment for Microsoft 365 Enterprise that includes:</span></span>

- <span data-ttu-id="27c7e-106">Un abonnement d’évaluation ou payant Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="27c7e-106">A Microsoft 365 E5 trial or paid subscription.</span></span>
- <span data-ttu-id="27c7e-107">Un intranet simplifié d’une organisation connecté à Internet, composé de trois machines virtuelles sur un réseau virtuel Azure (DC1, APP1 et CLIENT1).</span><span class="sxs-lookup"><span data-stu-id="27c7e-107">A simplified organization intranet connected to the Internet, consisting of three virtual machines on an Azure virtual network (DC1, APP1, and CLIENT1).</span></span>
 
![Configuration de base d’une entreprise simulée](../media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase4.png)

<span data-ttu-id="27c7e-109">Vous pouvez utiliser l’environnement obtenu pour tester les fonctions et le bon fonctionnement de[Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise), par vous-même ou en suivant les conseils des [guides de laboratoire de test](m365-enterprise-test-lab-guides.md).</span><span class="sxs-lookup"><span data-stu-id="27c7e-109">You can use the resulting environment to test the features and functionality of [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise) with additional [Test Lab Guides](m365-enterprise-test-lab-guides.md) or on your own.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="27c7e-111">Accédez au [Guide de laboratoire de laboratoire de test Microsoft 365 Entreprise](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) d’une carte visuelle à tous les Articles de la pile de guides de laboratoires de test Microsoft 365 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="27c7e-111">Go to [Microsoft 365 Enterprise Test Lab Guide Stack](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-create-a-simulated-intranet"></a><span data-ttu-id="27c7e-112">Phase 1: Créer un intranet simulé</span><span class="sxs-lookup"><span data-stu-id="27c7e-112">Phase 1: Create a simulated intranet</span></span>

<span data-ttu-id="27c7e-113">Dans cette phase, vous allez créer un intranet simulé dans les services d’infrastructure Azure comprenant un contrôleur de domaine Windows Server Active Directory, un serveur d’application et un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="27c7e-113">In this phase, you build a simulated intranet in Azure infrastructure services that includes an Active Directory Domain Services (AD DS) domain controller, an application server, and a client computer.</span></span> 

<span data-ttu-id="27c7e-114">Vous utiliserez ces ordinateurs dans des[Guides de laboratoire de Test Microsoft 365 Enterprise](m365-enterprise-test-lab-guides.md)supplémentaires afin de configurer et montrer l’identité hybride et les autres fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="27c7e-114">You'll use these computers in additional [Microsoft 365 Enterprise Test Lab Guides](m365-enterprise-test-lab-guides.md) to configure and demonstrate hybrid identity and other capabilities.</span></span>

### <a name="method-1-build-your-simulated-intranet-with-an-azure-resource-manager-template"></a><span data-ttu-id="27c7e-115">Méthode 1: Créer votre intranet simulé avec un Modèle de Gestion de Ressources Azure </span><span class="sxs-lookup"><span data-stu-id="27c7e-115">Method 1: Build your simulated intranet with an Azure Resource Manager template</span></span>

<span data-ttu-id="27c7e-116">In this method, you use an Azure Resource Manager (ARM) template to build out the simulated intranet.</span><span class="sxs-lookup"><span data-stu-id="27c7e-116">In this method, you use an Azure Resource Manager (ARM) template to build out the simulated intranet.</span></span> <span data-ttu-id="27c7e-117">ARM templates contain all of the instructions to create the Azure networking infrastructure, the virtual machines, and their configuration.</span><span class="sxs-lookup"><span data-stu-id="27c7e-117">ARM templates contain all of the instructions to create the Azure networking infrastructure, the virtual machines, and their configuration.</span></span>

<span data-ttu-id="27c7e-118">Avant de déployer le modèle, parcourez le[modèle de la page Lisez-moi](https://github.com/maxskunkworks/TLG/tree/master/tlg-base-config_3-vm.m365-ems) et obtenez les informations suivantes prêtes :</span><span class="sxs-lookup"><span data-stu-id="27c7e-118">Prior to deploying the template, read through the [template README page](https://github.com/maxskunkworks/TLG/tree/master/tlg-base-config_3-vm.m365-ems) and have the following information ready:</span></span>

- <span data-ttu-id="27c7e-119">The public DNS domain name of your test environment (testlab.\<your public domain>).</span><span class="sxs-lookup"><span data-stu-id="27c7e-119">The public DNS domain name of your test environment (testlab.\<your public domain>).</span></span> <span data-ttu-id="27c7e-120">You'll need to enter this name in the **Domain Name field** of the **Custom deployment** page.</span><span class="sxs-lookup"><span data-stu-id="27c7e-120">You'll need to enter this name in the **Domain Name field** of the **Custom deployment** page.</span></span>
- <span data-ttu-id="27c7e-121">A DNS label prefix for the URLs of the public IP addresses of your virtual machines.</span><span class="sxs-lookup"><span data-stu-id="27c7e-121">A DNS label prefix for the URLs of the public IP addresses of your virtual machines.</span></span> <span data-ttu-id="27c7e-122">You'll need to enter this label in the **Dns Label Prefix** field of the **Custom deployment** page.</span><span class="sxs-lookup"><span data-stu-id="27c7e-122">You'll need to enter this label in the **Dns Label Prefix** field of the **Custom deployment** page.</span></span>

<span data-ttu-id="27c7e-123">Après avoir lu via les instructions, cliquez sur **déployer vers Azure** sur la [page modèle LISEZMOI](https://github.com/maxskunkworks/TLG/tree/master/tlg-base-config_3-vm.m365-ems) pour commencer.</span><span class="sxs-lookup"><span data-stu-id="27c7e-123">After reading through the instructions, click **Deploy to Azure** on the [template README page](https://github.com/maxskunkworks/TLG/tree/master/tlg-base-config_3-vm.m365-ems) to get started.</span></span>

>[!Note]
><span data-ttu-id="27c7e-124">L’Intranet simulé créé par le modèle GRA nécessite un abonnement payant à Azure.</span><span class="sxs-lookup"><span data-stu-id="27c7e-124">The simulated intranet built by the ARM template requires a paid Azure subscription.</span></span>
>

<span data-ttu-id="27c7e-125">Voici votre configuration une fois le modèle terminé.</span><span class="sxs-lookup"><span data-stu-id="27c7e-125">Here is your configuration after the template is complete.</span></span>

![L’intranet simulé dans les services d’infrastructure Azure.](../media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase3.png)

### <a name="method-2-build-your-simulated-intranet-with-azure-powershell"></a><span data-ttu-id="27c7e-127">Méthode 2 : Créer votre intranet simulé avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="27c7e-127">Method 2: Build your simulated intranet with Azure PowerShell</span></span>

<span data-ttu-id="27c7e-128">En utilisant cette méthode, vous utilisez Windows PowerShell et le module Azure PowerShell afin de créer l’infrastructure de réseau, les machines virtuelles et leur configuration.</span><span class="sxs-lookup"><span data-stu-id="27c7e-128">In this method, you use Windows PowerShell and the Azure PowerShell module to build out the networking infrastructure, the virtual machines, and their configuration.</span></span>

<span data-ttu-id="27c7e-129">Use this method if you want to get experience creating elements of Azure infrastructure one step at a time with PowerShell.</span><span class="sxs-lookup"><span data-stu-id="27c7e-129">Use this method if you want to get experience creating elements of Azure infrastructure one step at a time with PowerShell.</span></span> <span data-ttu-id="27c7e-130">You can then customize the PowerShell command blocks for your own deployment of other virtual machines in Azure.</span><span class="sxs-lookup"><span data-stu-id="27c7e-130">You can then customize the PowerShell command blocks for your own deployment of other virtual machines in Azure.</span></span>

#### <a name="step-1-create-dc1"></a><span data-ttu-id="27c7e-131">Phase 1: création de DC1</span><span class="sxs-lookup"><span data-stu-id="27c7e-131">Step 1: Create DC1</span></span>

<span data-ttu-id="27c7e-132">Durant cette phase, nous allons créer un réseau virtuel Azure et ajouter la machine virtuelle DC1 qui est un contrôleur de domaine pour un domaine Windows Server Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="27c7e-132">In this step, we create an Azure virtual network and add DC1, a virtual machine that is a domain controller for an AD DS domain.</span></span>

<span data-ttu-id="27c7e-133">Tout d’abord, démarrez une invite de commandes Windows PowerShell sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="27c7e-133">First, start a Windows PowerShell command prompt on your local computer.</span></span>
  
> [!NOTE]
> <span data-ttu-id="27c7e-134">The following command sets use the latest version of Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="27c7e-134">The following command sets use the latest version of Azure PowerShell.</span></span> <span data-ttu-id="27c7e-135">See [Get started with Azure PowerShell cmdlets](https://docs.microsoft.com/powershell/azureps-cmdlets-docs/).</span><span class="sxs-lookup"><span data-stu-id="27c7e-135">See [Get started with Azure PowerShell cmdlets](https://docs.microsoft.com/powershell/azureps-cmdlets-docs/).</span></span> 
  
<span data-ttu-id="27c7e-136">Connectez-vous à votre compte Azure avec la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="27c7e-136">Sign in to your Azure account with the following command.</span></span>
  
```powershell
Connect-AzAccount
```

<span data-ttu-id="27c7e-137">Obtenez le nom de votre abonnement à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="27c7e-137">Get your subscription name using the following command.</span></span>
  
```powershell
Get-AzSubscription | Sort Name | Select Name
```

<span data-ttu-id="27c7e-138">Set your Azure subscription.</span><span class="sxs-lookup"><span data-stu-id="27c7e-138">Set your Azure subscription.</span></span> <span data-ttu-id="27c7e-139">Replace everything within the quotes, including the < and > characters, with the correct name.</span><span class="sxs-lookup"><span data-stu-id="27c7e-139">Replace everything within the quotes, including the < and > characters, with the correct name.</span></span>
  
```powershell
$subscr="<subscription name>"
Get-AzSubscription -SubscriptionName $subscr | Select-AzSubscription
```

<span data-ttu-id="27c7e-140">Next, create a new resource group for your simulated enterprise test lab.</span><span class="sxs-lookup"><span data-stu-id="27c7e-140">Next, create a new resource group for your simulated enterprise test lab.</span></span> <span data-ttu-id="27c7e-141">To determine a unique resource group name, use this command to list your existing resource groups.</span><span class="sxs-lookup"><span data-stu-id="27c7e-141">To determine a unique resource group name, use this command to list your existing resource groups.</span></span>
  
```powershell
Get-AzResourceGroup | Sort ResourceGroupName | Select ResourceGroupName
```

<span data-ttu-id="27c7e-142">Create your new resource group with these commands.</span><span class="sxs-lookup"><span data-stu-id="27c7e-142">Create your new resource group with these commands.</span></span> <span data-ttu-id="27c7e-143">Replace everything within the quotes, including the < and > characters, with the correct names.</span><span class="sxs-lookup"><span data-stu-id="27c7e-143">Replace everything within the quotes, including the < and > characters, with the correct names.</span></span>
  
```powershell
$rgName="<resource group name>"
$locName="<location name, such as West US>"
New-AzResourceGroup -Name $rgName -Location $locName
```

<span data-ttu-id="27c7e-144">Next, you create the TestLab virtual network that will host the Corpnet subnet of the simulated enterprise environment and protect it with a network security group.</span><span class="sxs-lookup"><span data-stu-id="27c7e-144">Next, you create the TestLab virtual network that will host the Corpnet subnet of the simulated enterprise environment and protect it with a network security group.</span></span> <span data-ttu-id="27c7e-145">Fill in the name of your resource group and run these commands at the PowerShell command prompt on your local computer.</span><span class="sxs-lookup"><span data-stu-id="27c7e-145">Fill in the name of your resource group and run these commands at the PowerShell command prompt on your local computer.</span></span>
  
```powershell
$rgName="<name of your new resource group>"
$locName=(Get-AzResourceGroup -Name $rgName).Location
$corpnetSubnet=New-AzVirtualNetworkSubnetConfig -Name Corpnet -AddressPrefix 10.0.0.0/24
New-AzVirtualNetwork -Name TestLab -ResourceGroupName $rgName -Location $locName -AddressPrefix 10.0.0.0/8 -Subnet $corpnetSubnet -DNSServer 10.0.0.4
$rule1=New-AzNetworkSecurityRuleConfig -Name "RDPTraffic" -Description "Allow RDP to all VMs on the subnet" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
New-AzNetworkSecurityGroup -Name Corpnet -ResourceGroupName $rgName -Location $locName -SecurityRules $rule1
$vnet=Get-AzVirtualNetwork -ResourceGroupName $rgName -Name TestLab
$nsg=Get-AzNetworkSecurityGroup -Name Corpnet -ResourceGroupName $rgName
Set-AzVirtualNetworkSubnetConfig -VirtualNetwork $vnet -Name Corpnet -AddressPrefix "10.0.0.0/24" -NetworkSecurityGroup $nsg
$vnet | Set-AzVirtualNetwork
```

<span data-ttu-id="27c7e-146">Ensuite, vous créez la machine virtuelle DC1 et le configurez comme contrôleur de domaine pour le **testlab.**\<your public domain></span><span class="sxs-lookup"><span data-stu-id="27c7e-146">Next, you create the DC1 virtual machine and configure it as a domain controller for the **testlab.**\<your public domain></span></span> <span data-ttu-id="27c7e-147">Domaine AD DS et serveur DNS pour les machines virtuelles du réseau virtuel TestLab.</span><span class="sxs-lookup"><span data-stu-id="27c7e-147">AD DS domain and a DNS server for the virtual machines of the TestLab virtual network.</span></span> <span data-ttu-id="27c7e-148">Par exemple, si votre nom de domaine public est \*\* <span>contoso</span>.com\*\*, la machine virtuelle DC1 sera un contrôleur de domaine pour le **<span>testlab</span>. contoso.com** domaine.</span><span class="sxs-lookup"><span data-stu-id="27c7e-148">For example, if your public domain name is **<span>contoso</span>.com**, the DC1 virtual machine will be a domain controller for the **<span>testlab</span>.contoso.com** domain.</span></span>
  
<span data-ttu-id="27c7e-149">Pour créer une machine virtuelle Azure pour DC1, indiquez d’abord le nom de votre groupe de ressources, puis exécutez ces commandes à l’invite de commandes PowerShell sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="27c7e-149">To create an Azure virtual machine for DC1, fill in the name of your resource group and run these commands at the PowerShell command prompt on your local computer.</span></span>
  
```powershell
$rgName="<resource group name>"
$locName=(Get-AzResourceGroup -Name $rgName).Location
$vnet=Get-AzVirtualNetwork -Name TestLab -ResourceGroupName $rgName
$pip=New-AzPublicIpAddress -Name DC1-PIP -ResourceGroupName $rgName -Location $locName -AllocationMethod Dynamic
$nic=New-AzNetworkInterface -Name DC1-NIC -ResourceGroupName $rgName -Location $locName -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $pip.Id -PrivateIpAddress 10.0.0.4
$vm=New-AzVMConfig -VMName DC1 -VMSize Standard_A2_V2
$cred=Get-Credential -Message "Type the name and password of the local administrator account for DC1."
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName DC1 -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name "DC1-OS" -DiskSizeInGB 128 -CreateOption FromImage
$diskConfig=New-AzDiskConfig -AccountType "Standard_LRS" -Location $locName -CreateOption Empty -DiskSizeGB 20
$dataDisk1=New-AzDisk -DiskName "DC1-DataDisk1" -Disk $diskConfig -ResourceGroupName $rgName
$vm=Add-AzVMDataDisk -VM $vm -Name "DC1-DataDisk1" -CreateOption Attach -ManagedDiskId $dataDisk1.Id -Lun 1
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm
```

<span data-ttu-id="27c7e-150">You will be prompted for a user name and password for the local administrator account on DC1.</span><span class="sxs-lookup"><span data-stu-id="27c7e-150">You will be prompted for a user name and password for the local administrator account on DC1.</span></span> <span data-ttu-id="27c7e-151">Use a strong password and record both the name and password in a secure location.</span><span class="sxs-lookup"><span data-stu-id="27c7e-151">Use a strong password and record both the name and password in a secure location.</span></span>
  
<span data-ttu-id="27c7e-152">Ensuite, connectez-vous à la machine virtuelle DC1.</span><span class="sxs-lookup"><span data-stu-id="27c7e-152">Next, connect to the DC1 virtual machine.</span></span>
  
1. <span data-ttu-id="27c7e-153">Dans le [Portail Azure](https://portal.azure.com), cliquez sur **Groupes de Ressources >** [nom de votre nouveau groupe de ressources] **> DC1 > Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-153">In the [Azure portal](https://portal.azure.com), click **Resource Groups >** [the name of your new resource group] **> DC1 > Connect**.</span></span>
    
2. <span data-ttu-id="27c7e-154">In the open pane, click **Download RDP file**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-154">In the open pane, click **Download RDP file**.</span></span> <span data-ttu-id="27c7e-155">Open the DC1.rdp file that is downloaded, and then click **Connect**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-155">Open the DC1.rdp file that is downloaded, and then click **Connect**.</span></span>
    
3. <span data-ttu-id="27c7e-156">Spécifiez le nom du compte Administrateur local DC1 :</span><span class="sxs-lookup"><span data-stu-id="27c7e-156">Specify the DC1 local administrator account name:</span></span>
    
   - <span data-ttu-id="27c7e-157">Pour Windows 7 :</span><span class="sxs-lookup"><span data-stu-id="27c7e-157">For Windows 7:</span></span>
    
     <span data-ttu-id="27c7e-158">In the **Windows Security** dialog box, click **Use another account**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-158">In the **Windows Security** dialog box, click **Use another account**.</span></span> <span data-ttu-id="27c7e-159">In **User name**, type **DC1\\**[Local administrator account name].</span><span class="sxs-lookup"><span data-stu-id="27c7e-159">In **User name**, type **DC1\\**[Local administrator account name].</span></span>
    
   - <span data-ttu-id="27c7e-160">Pour Windows 8 ou Windows 10 :</span><span class="sxs-lookup"><span data-stu-id="27c7e-160">For Windows 8 or Windows 10:</span></span>
    
     <span data-ttu-id="27c7e-161">In the **Windows Security** dialog box, click **More choices**, and then click **Use a different account**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-161">In the **Windows Security** dialog box, click **More choices**, and then click **Use a different account**.</span></span> <span data-ttu-id="27c7e-162">In **User name**, type **DC1\\**[Local administrator account name].</span><span class="sxs-lookup"><span data-stu-id="27c7e-162">In **User name**, type **DC1\\**[Local administrator account name].</span></span>
    
4. <span data-ttu-id="27c7e-163">Dans **Mot de passe**, tapez le mot de passe du compte Administrateur local, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-163">In **Password**, type the password of the local administrator account, and then click **OK**.</span></span>
    
5. <span data-ttu-id="27c7e-164">Quand vous y êtes invité, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-164">When prompted, click **Yes**.</span></span>
    
<span data-ttu-id="27c7e-165">Ensuite, ajoutez un disque de données supplémentaire en tant que nouveau volume avec la lettre de lecteur F:, à l’aide de la commande suivante, dans l’invite de commande Windows PowerShell au niveau administrateur sur DC1.</span><span class="sxs-lookup"><span data-stu-id="27c7e-165">Next, add an extra data disk as a new volume with the drive letter F: with this command at an administrator-level Windows PowerShell command prompt on DC1.</span></span>
  
```powershell
Get-Disk | Where PartitionStyle -eq "RAW" | Initialize-Disk -PartitionStyle MBR -PassThru | New-Partition -AssignDriveLetter -UseMaximumSize | Format-Volume -FileSystem NTFS -NewFileSystemLabel "WSAD Data"
```

<span data-ttu-id="27c7e-166">Ensuite, configurez DC1 comme un contrôleur de domaine et un serveur DNS pour le domaine **testlab.**\<your public domain></span><span class="sxs-lookup"><span data-stu-id="27c7e-166">Next, configure DC1 as a domain controller and DNS server for the **testlab.**\<your public domain></span></span> <span data-ttu-id="27c7e-167">.</span><span class="sxs-lookup"><span data-stu-id="27c7e-167">domain.</span></span> <span data-ttu-id="27c7e-168">Spécifiez votre nom de domaine public, supprimez les \< and > caractères, puis exécutez ces commandes dans une invite de commandes Windows PowerShell au niveau de l’administrateur sur DC1.</span><span class="sxs-lookup"><span data-stu-id="27c7e-168">Specify your public domain name, remove the \< and > characters, and then run these commands at an administrator-level Windows PowerShell command prompt on DC1.</span></span>
  
```powershell
$yourDomain="<your public domain>"
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
Install-ADDSForest -DomainName testlab.$yourDomain -DatabasePath "F:\NTDS" -SysvolPath "F:\SYSVOL" -LogPath "F:\Logs"
```
<span data-ttu-id="27c7e-169">You will need to specify a safe mode administrator password.</span><span class="sxs-lookup"><span data-stu-id="27c7e-169">You will need to specify a safe mode administrator password.</span></span> <span data-ttu-id="27c7e-170">Store this password in a secure location.</span><span class="sxs-lookup"><span data-stu-id="27c7e-170">Store this password in a secure location.</span></span>
  
<span data-ttu-id="27c7e-171">Notez que l’exécution de ces commandes peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="27c7e-171">Note that these commands can take a few minutes to complete.</span></span>
  
<span data-ttu-id="27c7e-172">Après le redémarrage de DC1, reconnectez-vous à la machine virtuelle DC1.</span><span class="sxs-lookup"><span data-stu-id="27c7e-172">After DC1 restarts, reconnect to the DC1 virtual machine.</span></span>
  
1. <span data-ttu-id="27c7e-173">Dans le [Portail Azure](https://portal.azure.com), cliquez sur **Groupes de Ressources >** [nom de votre groupe de ressources] **> DC1 > Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-173">In the [Azure portal](https://portal.azure.com), click **Resource Groups >** [your resource group name] **> DC1 > Connect**.</span></span>
    
2. <span data-ttu-id="27c7e-174">Exécutez le fichier DC1.rdp qui est téléchargé, puis cliquez sur **Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-174">Run the DC1.rdp file that is downloaded, and then click **Connect**.</span></span>
    
3. <span data-ttu-id="27c7e-175">In **Windows Security**, click **Use another account**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-175">In **Windows Security**, click **Use another account**.</span></span> <span data-ttu-id="27c7e-176">In **User name**, type **TESTLAB\\**[Local administrator account name].</span><span class="sxs-lookup"><span data-stu-id="27c7e-176">In **User name**, type **TESTLAB\\**[Local administrator account name].</span></span>
    
4. <span data-ttu-id="27c7e-177">Dans **Mot de passe**, tapez le mot de passe du compte Administrateur local, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-177">In **Password**, type the password of the local administrator account, and then click **OK**.</span></span>
    
5. <span data-ttu-id="27c7e-178">Quand vous y êtes invité, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-178">When prompted, click **Yes**.</span></span>
    
<span data-ttu-id="27c7e-179">Next, create a user account in Active Directory that will be used when logging in to TESTLAB domain member computers.</span><span class="sxs-lookup"><span data-stu-id="27c7e-179">Next, create a user account in Active Directory that will be used when logging in to TESTLAB domain member computers.</span></span> <span data-ttu-id="27c7e-180">Run this command at an administrator-level Windows PowerShell command prompt.</span><span class="sxs-lookup"><span data-stu-id="27c7e-180">Run this command at an administrator-level Windows PowerShell command prompt.</span></span>
  
```powershell
New-ADUser -SamAccountName User1 -AccountPassword (read-host "Set user password" -assecurestring) -name "User1" -enabled $true -PasswordNeverExpires $true -ChangePasswordAtLogon $false
```

<span data-ttu-id="27c7e-181">Note that this command prompts you to supply the User1 account password.</span><span class="sxs-lookup"><span data-stu-id="27c7e-181">Note that this command prompts you to supply the User1 account password.</span></span> <span data-ttu-id="27c7e-182">Because this account will be used for remote desktop connections for all TESTLAB domain member computers, choose a strong password.</span><span class="sxs-lookup"><span data-stu-id="27c7e-182">Because this account will be used for remote desktop connections for all TESTLAB domain member computers, choose a strong password.</span></span> <span data-ttu-id="27c7e-183">Record the User1 account password and store it in a secured location.</span><span class="sxs-lookup"><span data-stu-id="27c7e-183">Record the User1 account password and store it in a secured location.</span></span>
  
<span data-ttu-id="27c7e-184">Next, configure the new User1 account as a domain, enterprise, and schema administrator.</span><span class="sxs-lookup"><span data-stu-id="27c7e-184">Next, configure the new User1 account as a domain, enterprise, and schema administrator.</span></span> <span data-ttu-id="27c7e-185">Run this command at the administrator-level Windows PowerShell command prompt.</span><span class="sxs-lookup"><span data-stu-id="27c7e-185">Run this command at the administrator-level Windows PowerShell command prompt.</span></span>
  
```powershell
$yourDomain="<your public domain>"
$domainName = "testlab."+$yourDomain
$userName="user1@" + $domainName
$userSID=(New-Object System.Security.Principal.NTAccount($userName)).Translate([System.Security.Principal.SecurityIdentifier]).Value
$groupNames=@("Domain Admins","Enterprise Admins","Schema Admins")
ForEach ($name in $groupNames) {Add-ADPrincipalGroupMembership -Identity $userSID -MemberOf (Get-ADGroup -Identity $name).SID.Value}
```

<span data-ttu-id="27c7e-186">Fermez la session Bureau à distance avec DC1 et reconnectez-vous à l’aide du compte TESTLAB\\Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="27c7e-186">Close the Remote Desktop session with DC1 and then reconnect using the TESTLAB\\User1 account.</span></span>
  
<span data-ttu-id="27c7e-187">Ensuite, pour autoriser le trafic pour l’outil Ping, exécutez cette commande à l’invite de commandes Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="27c7e-187">Next, to allow traffic for the Ping tool, run this command at an administrator-level Windows PowerShell command prompt.</span></span>
  
```powershell
Set-NetFirewallRule -DisplayName "File and Printer Sharing (Echo Request - ICMPv4-In)" -enabled True
```

<span data-ttu-id="27c7e-188">Il s’agit de votre configuration actuelle.</span><span class="sxs-lookup"><span data-stu-id="27c7e-188">This is your current configuration.</span></span>
  
![Phase 1 de la configuration de base de l’entreprise simulée](../media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase1.png)
  
#### <a name="step-2-configure-app1"></a><span data-ttu-id="27c7e-190">Phase 2:Configurer APP1</span><span class="sxs-lookup"><span data-stu-id="27c7e-190">Step 2: Configure APP1</span></span>

<span data-ttu-id="27c7e-191">Durant cette phase, vous allez créer et configurer APP1, qui est un serveur d’applications qui fournit initial des services web et de partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="27c7e-191">In this step, you create and configure APP1, which is an application server that initially provides web and file sharing services.</span></span>

<span data-ttu-id="27c7e-192">Pour créer une machine virtuelle Azure pour APP1, renseignez d’abord le nom de votre groupe de ressources, puis exécutez ces commandes à l’invite de commandes sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="27c7e-192">To create an Azure Virtual Machine for APP1, fill in the name of your resource group and run these commands at the  command prompt on your local computer.</span></span>
  
```powershell
$rgName="<resource group name>"
$locName=(Get-AzResourceGroup -Name $rgName).Location
$vnet=Get-AzVirtualNetwork -Name TestLab -ResourceGroupName $rgName
$pip=New-AzPublicIpAddress -Name APP1-PIP -ResourceGroupName $rgName -Location $locName -AllocationMethod Dynamic
$nic=New-AzNetworkInterface -Name APP1-NIC -ResourceGroupName $rgName -Location $locName -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $pip.Id
$vm=New-AzVMConfig -VMName APP1 -VMSize Standard_A2_V2
$cred=Get-Credential -Message "Type the name and password of the local administrator account for APP1."
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName APP1 -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name "APP1-OS" -DiskSizeInGB 128 -CreateOption FromImage
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm
```

<span data-ttu-id="27c7e-193">Ensuite, connectez-vous à la machine virtuelle APP1 en utilisant le nom du compte Administrateur local APP1 et le mot de passe, et ouvrez une invite de commande Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="27c7e-193">Next, connect to the APP1 virtual machine using the APP1 local administrator account name and password, and then open a Windows PowerShell command prompt.</span></span>
  
<span data-ttu-id="27c7e-194">Pour vérifier la résolution de noms et les communications réseau entre APP1 et DC1, exécutez la commande **ping dc1.testlab.**\<your public domain name></span><span class="sxs-lookup"><span data-stu-id="27c7e-194">To check name resolution and network communication between APP1 and DC1, run the **ping dc1.testlab.**\<your public domain name></span></span> <span data-ttu-id="27c7e-195">et vérifiez qu’il y a quatre réponses.</span><span class="sxs-lookup"><span data-stu-id="27c7e-195">command and verify that there are four replies.</span></span>
  
<span data-ttu-id="27c7e-196">Maintenant, associez la machine virtuelle APP1 au domaine TESTLAB avec ces commandes à l’invite Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="27c7e-196">Next, join the APP1 virtual machine to the TESTLAB domain with these commands at the Windows PowerShell prompt.</span></span>
  
```powershell
$yourDomain="<your public domain name>"
Add-Computer -DomainName ("testlab." + $yourDomain)
Restart-Computer
```

<span data-ttu-id="27c7e-197">Les informations d’identification du compte de domaine TESTLAB\\Utilisateur1 doivent être fournies après l’exécution de la commande **Add-Computer**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-197">Note that you must supply the TESTLAB\\User1 domain account credentials after running the **Add-Computer** command.</span></span>
  
<span data-ttu-id="27c7e-198">Après le redémarrage d’APP1, connectez-vous en utilisant le compte TESTLAB\\Utilisateur1 et ouvrez une invite de commandes Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="27c7e-198">After APP1 restarts, connect to it using the TESTLAB\\User1 account, and then open an administrator-level Windows PowerShell command prompt.</span></span>
  
<span data-ttu-id="27c7e-199">Transformez APP1 en serveur web en exécutant cette commande à l’invite de commandes Windows PowerShell de niveau supérieur sur APP1.</span><span class="sxs-lookup"><span data-stu-id="27c7e-199">Next, make APP1 a web server with this command at an administrator-level Windows PowerShell command prompt on APP1.</span></span>
  
```powershell
Install-WindowsFeature Web-WebServer -IncludeManagementTools
```

<span data-ttu-id="27c7e-200">Ensuite, créez un dossier partagé et un fichier de texte dans le dossier sur APP1 avec ces commandes PowerShell.</span><span class="sxs-lookup"><span data-stu-id="27c7e-200">Next, create a shared folder and a text file within the folder on APP1 with these PowerShell commands.</span></span>
  
```powershell
New-Item -path c:\files -type directory
Write-Output "This is a shared file." | out-file c:\files\example.txt
New-SmbShare -name files -path c:\files -changeaccess TESTLAB\User1
```

<span data-ttu-id="27c7e-201">Il s’agit de votre configuration actuelle.</span><span class="sxs-lookup"><span data-stu-id="27c7e-201">This is your current configuration.</span></span>
  
![Phase 2 de la configuration de base de l’entreprise simulée](../media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase2.png)
  
#### <a name="step-3-configure-client1"></a><span data-ttu-id="27c7e-203">Phase 3:Configurer CLIENT1</span><span class="sxs-lookup"><span data-stu-id="27c7e-203">Step 3: Configure CLIENT1</span></span>

<span data-ttu-id="27c7e-204">Durant cette phase, vous allez créer et configurer CLIENT1, qui se comporte comme un ordinateur portable, une tablette ou un ordinateur de bureau classique sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="27c7e-204">In this step, you create and configure CLIENT1, which acts as a typical laptop, tablet, or desktop computer on the intranet.</span></span>

> [!NOTE]  
> <span data-ttu-id="27c7e-205">The following command set creates CLIENT1 running Windows Server 2016 Datacenter, which can be done for all types of Azure subscriptions.</span><span class="sxs-lookup"><span data-stu-id="27c7e-205">The following command set creates CLIENT1 running Windows Server 2016 Datacenter, which can be done for all types of Azure subscriptions.</span></span> <span data-ttu-id="27c7e-206">If you have a Visual Studio-based Azure subscription, you can create CLIENT1 running Windows 10 with the [Azure portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="27c7e-206">If you have a Visual Studio-based Azure subscription, you can create CLIENT1 running Windows 10 with the [Azure portal](https://portal.azure.com).</span></span> 
  
<span data-ttu-id="27c7e-207">Pour créer une machine virtuelle Azure pour CLIENT1, renseignez d’abord le nom de votre groupe de ressources, puis exécutez ces commandes à l’invite de commandes sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="27c7e-207">To create an Azure Virtual Machine for CLIENT1, fill in the name of your resource group and run these commands at the  command prompt on your local computer.</span></span>
  
```powershell
$rgName="<resource group name>"
$locName=(Get-AzResourceGroup -Name $rgName).Location
$vnet=Get-AzVirtualNetwork -Name TestLab -ResourceGroupName $rgName
$pip=New-AzPublicIpAddress -Name CLIENT1-PIP -ResourceGroupName $rgName -Location $locName -AllocationMethod Dynamic
$nic=New-AzNetworkInterface -Name CLIENT1-NIC -ResourceGroupName $rgName -Location $locName -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $pip.Id
$vm=New-AzVMConfig -VMName CLIENT1 -VMSize Standard_A2_V2
$cred=Get-Credential -Message "Type the name and password of the local administrator account for CLIENT1."
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName CLIENT1 -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name "CLIENT1-OS" -DiskSizeInGB 128 -CreateOption FromImage
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm
```

<span data-ttu-id="27c7e-208">Ensuite, connectez-vous à la machine virtuelle CLIENT1 en utilisant le nom du compte Administrateur local CLIENT1 et le mot de passe, et ouvrez une invite de commande Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="27c7e-208">Next, connect to the CLIENT1 virtual machine using the CLIENT1 local administrator account name and password, and then open an administrator-level Windows PowerShell command prompt.</span></span>
  
<span data-ttu-id="27c7e-209">Pour vérifier la résolution de noms et les communications réseau entre CLIENT1 et DC1, exécutez la commande **ping dc1.testlab.**\<your public domain name></span><span class="sxs-lookup"><span data-stu-id="27c7e-209">To check name resolution and network communication between CLIENT1 and DC1, run the **ping dc1.testlab.**\<your public domain name></span></span> <span data-ttu-id="27c7e-210">dans une invite de commandes Windows PowerShell et vérifiez qu’il y a quatre réponses.</span><span class="sxs-lookup"><span data-stu-id="27c7e-210">command at a Windows PowerShell command prompt and verify that there are four replies.</span></span>
  
<span data-ttu-id="27c7e-211">Maintenant, associez la machine virtuelle CLIENT1 au domaine TESTLAB avec ces commandes à l’invite Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="27c7e-211">Next, join the CLIENT1 virtual machine to the TESTLAB domain with these commands at the Windows PowerShell prompt.</span></span>
  
```powershell
$yourDomain="<your public domain name>"
Add-Computer -DomainName ("testlab." + $yourDomain)
Restart-Computer
```

<span data-ttu-id="27c7e-212">Les informations d’identification de votre compte de domaine TESTLAB\\Utilisateur1 doivent être fournies après l’exécution de la commande **Add-Computer**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-212">Note that you must supply your TESTLAB\\User1 domain account credentials after running the **Add-Computer** command.</span></span>
  
<span data-ttu-id="27c7e-213">Après le redémarrage de CLIENT1, connectez-vous en utilisant le mot de passe et le nom du compte TESTLAB\\Utilisateur1 et ouvrez une invite de commandes Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="27c7e-213">After CLIENT1 restarts, connect to it using the TESTLAB\\User1 account name and password, and then open an administrator-level Windows PowerShell command prompt.</span></span>
  
<span data-ttu-id="27c7e-214">Ensuite, vérifiez que vous pouvez accéder aux ressources web et de partage de fichiers sur APP1 de CLIENT1.</span><span class="sxs-lookup"><span data-stu-id="27c7e-214">Next, verify that you can access web and file share resources on APP1 from CLIENT1.</span></span>
  
1. <span data-ttu-id="27c7e-215">Dans le Gestionnaire de Serveur, dans le volet de l’arborescence, cliquez sur **Serveur Local**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-215">In Server Manager, in the tree pane, click **Local Server**.</span></span>
    
2. <span data-ttu-id="27c7e-216">Dans **Propriétés pour CLIENT1**, cliquez sur **Activer** à côté de **Configuration de sécurité renforcée d’Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-216">In **Properties for CLIENT1**, click **On** next to **IE Enhanced Security Configuration**.</span></span>
    
3. <span data-ttu-id="27c7e-217">Dans **Configuration de sécurité renforcée d’Internet Explorer**, cliquez sur **Désactiver** pour **Administrateurs** et **Utilisateurs**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-217">In **Internet Explorer Enhanced Security Configuration**, click **Off** for **Administrators** and **Users**, and then click **OK**.</span></span>
    
4. <span data-ttu-id="27c7e-218">Sur l’écran d’accueil, cliquez sur **Internet Explorer**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-218">From the Start screen, click **Internet Explorer**, and then click **OK**.</span></span>
    
5. <span data-ttu-id="27c7e-219">Dans la barre d’adresses, tapez **http<span>://</span>app1.testab.**\<your public domain name>**/**, puis appuyez sur ENTRER.</span><span class="sxs-lookup"><span data-stu-id="27c7e-219">In the Address bar, type **http<span>://</span>app1.testab.**\<your public domain name>**/**, and then press ENTER.</span></span> <span data-ttu-id="27c7e-220">La page web Internet Information Services par défaut pour APP1 s’affiche.</span><span class="sxs-lookup"><span data-stu-id="27c7e-220">You should see the default Internet Information Services web page for APP1.</span></span>
    
6. <span data-ttu-id="27c7e-221">Dans la barre des tâches du bureau, cliquez sur l’icône de l’Explorateur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="27c7e-221">From the desktop taskbar, click the File Explorer icon.</span></span>
    
7. <span data-ttu-id="27c7e-222">In the address bar, type **\\\\app1\\Files**, and then press ENTER.</span><span class="sxs-lookup"><span data-stu-id="27c7e-222">In the address bar, type **\\\\app1\\Files**, and then press ENTER.</span></span> <span data-ttu-id="27c7e-223">You should see a folder window with the contents of the Files shared folder.</span><span class="sxs-lookup"><span data-stu-id="27c7e-223">You should see a folder window with the contents of the Files shared folder.</span></span>
    
8. <span data-ttu-id="27c7e-224">In the **Files** shared folder window, double-click the **Example.txt** file.</span><span class="sxs-lookup"><span data-stu-id="27c7e-224">In the **Files** shared folder window, double-click the **Example.txt** file.</span></span> <span data-ttu-id="27c7e-225">You should see the contents of the Example.txt file.</span><span class="sxs-lookup"><span data-stu-id="27c7e-225">You should see the contents of the Example.txt file.</span></span>
    
9. <span data-ttu-id="27c7e-226">Fermez les fenêtres de dossiers partagés **Exemple.txt - Bloc-notes** et **Fichiers**.</span><span class="sxs-lookup"><span data-stu-id="27c7e-226">Close the **example.txt - Notepad** and the **Files** shared folder windows.</span></span>
    
<span data-ttu-id="27c7e-227">Il s’agit de votre configuration actuelle.</span><span class="sxs-lookup"><span data-stu-id="27c7e-227">This is your current configuration.</span></span>
  
![Phase 3 de la configuration de base de l’entreprise simulée](../media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase3.png)


## <a name="phase-2-create-your-microsoft-365-e5-subscription"></a><span data-ttu-id="27c7e-229">Phase 2 : Création de votre abonnement Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="27c7e-229">Phase 2: Create your Microsoft 365 E5 subscription</span></span>

<span data-ttu-id="27c7e-230">In this phase, you create a new Microsoft 365 E5 subscription that uses a new Azure AD tenant, one that is separate from your production subscription.</span><span class="sxs-lookup"><span data-stu-id="27c7e-230">In this phase, you create a new Microsoft 365 E5 subscription that uses a new Azure AD tenant, one that is separate from your production subscription.</span></span> <span data-ttu-id="27c7e-231">You can do this in two ways:</span><span class="sxs-lookup"><span data-stu-id="27c7e-231">You can do this in two ways:</span></span>

- <span data-ttu-id="27c7e-232">Utiliser un abonnement d’évaluation de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="27c7e-232">Use a trial subscription of Microsoft 365 E5.</span></span> 

  <span data-ttu-id="27c7e-233">The Microsoft 365 E5 trial subscription is 30 days, which can be easily extended to 60 days.</span><span class="sxs-lookup"><span data-stu-id="27c7e-233">The Microsoft 365 E5 trial subscription is 30 days, which can be easily extended to 60 days.</span></span> <span data-ttu-id="27c7e-234">When the trial subscription expires, you must either convert it to a paid subscription or create a new trial subscription.</span><span class="sxs-lookup"><span data-stu-id="27c7e-234">When the trial subscription expires, you must either convert it to a paid subscription or create a new trial subscription.</span></span> <span data-ttu-id="27c7e-235">Creating new trial subscriptions means you will leave your configuration, which could include complex scenarios, behind.</span><span class="sxs-lookup"><span data-stu-id="27c7e-235">Creating new trial subscriptions means you will leave your configuration, which could include complex scenarios, behind.</span></span>  

- <span data-ttu-id="27c7e-236">Utiliser un abonnement de production de Microsoft 365 E5 distinct avec un nombre réduit de licences.</span><span class="sxs-lookup"><span data-stu-id="27c7e-236">Use a separate production subscription of Microsoft 365 E5 with a small number of licenses.</span></span>

  <span data-ttu-id="27c7e-237">This is an additional cost, but ensures that you have a working test environment to try features, configurations, and scenarios that does not expire.</span><span class="sxs-lookup"><span data-stu-id="27c7e-237">This is an additional cost, but ensures that you have a working test environment to try features, configurations, and scenarios that does not expire.</span></span> <span data-ttu-id="27c7e-238">You can use the same test environment over the long term for proofs of concept, demonstration to peers and management, and application development and testing.</span><span class="sxs-lookup"><span data-stu-id="27c7e-238">You can use the same test environment over the long term for proofs of concept, demonstration to peers and management, and application development and testing.</span></span> <span data-ttu-id="27c7e-239">This is the recommended method.</span><span class="sxs-lookup"><span data-stu-id="27c7e-239">This is the recommended method.</span></span>

### <a name="sign-up-for-an-office-365-e5-trial-subscription"></a><span data-ttu-id="27c7e-240">Inscription à un abonnement d’évaluation Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="27c7e-240">Sign up for an Office 365 E5 trial subscription</span></span>

<span data-ttu-id="27c7e-241">Connectez-vous à CLIENT1 avec le compte CORP\User1 à partir du Portail Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="27c7e-241">Connect to CLIENT1 with the CORP\User1 account from the Azure portal.</span></span>

<span data-ttu-id="27c7e-242">Pour créer un abonnement d’évaluation Office 365 E5, suivez les instructions de [phase 1](lightweight-base-configuration-microsoft-365-enterprise.md#phase-1-create-your-office-365-e5-subscription) du Guide de laboratoire de test de la configuration de base légère.</span><span class="sxs-lookup"><span data-stu-id="27c7e-242">To create a new Office 365 E5 trial subscription, perform the instructions in [Phase 1](lightweight-base-configuration-microsoft-365-enterprise.md#phase-1-create-your-office-365-e5-subscription) of the lightweight base configuration Test Lab Guide.</span></span>

<span data-ttu-id="27c7e-243">Pour configurer un abonnement d’évaluation Office 365 E5, suivez les instructions de [phase 2](lightweight-base-configuration-microsoft-365-enterprise.md#phase-2-configure-your-office-365-trial-subscription) du Guide de laboratoire de test de la configuration de base légère.</span><span class="sxs-lookup"><span data-stu-id="27c7e-243">To configure your new Office 365 E5 trial subscription, perform the instructions in [Phase 2](lightweight-base-configuration-microsoft-365-enterprise.md#phase-2-configure-your-office-365-trial-subscription) of the lightweight base configuration Test Lab Guide.</span></span>

#### <a name="using-an-office-365-e5-test-environment"></a><span data-ttu-id="27c7e-244">Utilisation d’un environnement de test Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="27c7e-244">Using an Office 365 E5 test environment</span></span>

<span data-ttu-id="27c7e-245">Si vous avez simplement besoin d’un environnement de test Office 365, vous pouvez vous arrêter ici.</span><span class="sxs-lookup"><span data-stu-id="27c7e-245">If all you need is an Office 365 test environment, you can stop here.</span></span> 

<span data-ttu-id="27c7e-246">Pour plus d’informations sur les guides de labo de test, voir [les guides de laboratoire de test Microsoft 365 Entreprise](m365-enterprise-test-lab-guides.md) pour Office 365 et Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="27c7e-246">See [Microsoft 365 Enterprise Test Lab Guides](m365-enterprise-test-lab-guides.md) for additional Test Lab Guides that apply to both Office 365 and Microsoft 365.</span></span>

### <a name="add-a-microsoft-365-e5-trial-subscription"></a><span data-ttu-id="27c7e-247">Ajouter un abonnement d’évaluation de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="27c7e-247">Add a Microsoft 365 E5 trial subscription</span></span>

<span data-ttu-id="27c7e-248">Pour configurer un abonnement d’évaluation Microsoft 365 E5 et configurer des comptes d’utilisateur avec licences, suivez les instructions de [phase 3](lightweight-base-configuration-microsoft-365-enterprise.md#phase-3-add-a-microsoft-365-e5-trial-subscription) du Guide de laboratoire de test de la configuration de base légère.</span><span class="sxs-lookup"><span data-stu-id="27c7e-248">To a Microsoft 365 E5 trial subscription and configure your users accounts with licenses, perform the instructions in [Phase 3](lightweight-base-configuration-microsoft-365-enterprise.md#phase-3-add-a-microsoft-365-e5-trial-subscription) of the lightweight base configuration Test Lab Guide.</span></span>

  
## <a name="results"></a><span data-ttu-id="27c7e-249">Résultats</span><span class="sxs-lookup"><span data-stu-id="27c7e-249">Results</span></span>

<span data-ttu-id="27c7e-250">Votre environnement de test comporte maintenant :</span><span class="sxs-lookup"><span data-stu-id="27c7e-250">Your test environment now has:</span></span>
  
- <span data-ttu-id="27c7e-251">Abonnement d’évaluation de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="27c7e-251">Microsoft 365 E5 trial subscription.</span></span>
- <span data-ttu-id="27c7e-252">Tous vos comptes d’utilisateurs appropriés sont configurés pour utiliser Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="27c7e-252">All your appropriate user accounts are enabled to use Microsoft 365 E5.</span></span>
- <span data-ttu-id="27c7e-253">Un intranet simulé et simplifié.</span><span class="sxs-lookup"><span data-stu-id="27c7e-253">A simulated and simplified intranet.</span></span>
    
<span data-ttu-id="27c7e-254">Il s’agit de votre configuration finale.</span><span class="sxs-lookup"><span data-stu-id="27c7e-254">This is your final configuration.</span></span>
  
![Phase 2 de la configuration de base de l’entreprise simulée](../media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase4.png)
  
<span data-ttu-id="27c7e-256">Vous êtes désormais prêt à profiter des fonctionnalités supplémentaires de [Microsoft 365 Entreprise](https://www.microsoft.com/microsoft-365/enterprise).</span><span class="sxs-lookup"><span data-stu-id="27c7e-256">You are now ready to experiment with additional features of [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="27c7e-257">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="27c7e-257">Next steps</span></span>

<span data-ttu-id="27c7e-258">Découvrez les nouveaux ensembles de guides pour les tests de laboratoire :</span><span class="sxs-lookup"><span data-stu-id="27c7e-258">Explore these additional sets of Test Lab Guides:</span></span>
  
- [<span data-ttu-id="27c7e-259">Identité</span><span class="sxs-lookup"><span data-stu-id="27c7e-259">Identity</span></span>](m365-enterprise-test-lab-guides.md#identity)
- [<span data-ttu-id="27c7e-260">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="27c7e-260">Mobile device management</span></span>](m365-enterprise-test-lab-guides.md#mobile-device-management)
- [<span data-ttu-id="27c7e-261">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="27c7e-261">Information protection</span></span>](m365-enterprise-test-lab-guides.md#information-protection)

## <a name="see-also"></a><span data-ttu-id="27c7e-262">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27c7e-262">See also</span></span>

[<span data-ttu-id="27c7e-263">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="27c7e-263">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="27c7e-264">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="27c7e-264">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="27c7e-265">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="27c7e-265">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
