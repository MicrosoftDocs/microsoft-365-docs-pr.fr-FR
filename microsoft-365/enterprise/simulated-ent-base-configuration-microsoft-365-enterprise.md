---
title: Configuration de base d’une entreprise simulée pour Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 05/01/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom:
- Ent_TLGs
ms.assetid: 6f916a77-301c-4be2-b407-6cec4d80df76
description: Utilisez ce Guide de Laboratoire Test afin de créer une simulation d’environnement de test dédiée à Microsoft 365 Entreprise.
ms.openlocfilehash: 7a23f0eabcd9b4b0b94f6f932570fed12de32cbe
ms.sourcegitcommit: 2aeafb631aaabc53eea0a8029711eb891e48d249
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2019
ms.locfileid: "37746500"
---
# <a name="the-simulated-enterprise-base-configuration"></a><span data-ttu-id="8d173-103">Configuration de base d’une entreprise simulée</span><span class="sxs-lookup"><span data-stu-id="8d173-103">The simulated enterprise base configuration</span></span>

<span data-ttu-id="8d173-104">Vous trouverez dans cet article des instructions détaillées pour créer un environnement simplifié pour Microsoft 365 Entreprise qui comprend :</span><span class="sxs-lookup"><span data-stu-id="8d173-104">This article provides you with step-by-step instructions to create a simplified environment for Microsoft 365 Enterprise that includes:</span></span>

- <span data-ttu-id="8d173-105">Un abonnement d’évaluation ou payant Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="8d173-105">A Microsoft 365 E5 trial or paid subscription.</span></span>
- <span data-ttu-id="8d173-106">Un intranet simplifié d’une organisation connecté à Internet, composé de trois machines virtuelles sur un réseau virtuel Azure (DC1, APP1 et CLIENT1).</span><span class="sxs-lookup"><span data-stu-id="8d173-106">A simplified organization intranet connected to the Internet, consisting of three virtual machines on an Azure virtual network (DC1, APP1, and CLIENT1).</span></span>
 
![Configuration de base d’une entreprise simulée](media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase4.png)

<span data-ttu-id="8d173-108">Vous pouvez utiliser l’environnement obtenu pour tester les fonctions et le bon fonctionnement de[Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise), par vous-même ou en suivant les conseils des [guides de laboratoire de test](m365-enterprise-test-lab-guides.md).</span><span class="sxs-lookup"><span data-stu-id="8d173-108">You can use the resulting environment to test the features and functionality of [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise) with additional [Test Lab Guides](m365-enterprise-test-lab-guides.md) or on your own.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="8d173-110">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="8d173-110">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-create-a-simulated-intranet"></a><span data-ttu-id="8d173-111">Phase 1: Créer un intranet simulé</span><span class="sxs-lookup"><span data-stu-id="8d173-111">Phase 1: Create a simulated intranet</span></span>

<span data-ttu-id="8d173-112">Dans cette phase, vous allez créer un intranet simulé dans les services d’infrastructure Azure comprenant un contrôleur de domaine Windows Server Active Directory, un serveur d’application et un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="8d173-112">In this phase, you build a simulated intranet in Azure infrastructure services that includes an Active Directory Domain Services (AD DS) domain controller, an application server, and a client computer.</span></span> 

<span data-ttu-id="8d173-113">Vous utiliserez ces ordinateurs dans des[Guides de laboratoire de Test Microsoft 365 Enterprise](m365-enterprise-test-lab-guides.md)supplémentaires afin de configurer et montrer l’identité hybride et les autres fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="8d173-113">You'll use these computers in additional [Microsoft 365 Enterprise Test Lab Guides](m365-enterprise-test-lab-guides.md) to configure and demonstrate hybrid identity and other capabilities.</span></span>

### <a name="method-1-build-your-simulated-intranet-with-an-azure-resource-manager-template"></a><span data-ttu-id="8d173-114">Méthode 1: Créer votre intranet simulé avec un Modèle de Gestion de Ressources Azure </span><span class="sxs-lookup"><span data-stu-id="8d173-114">Method 1: Build your simulated intranet with an Azure Resource Manager template</span></span>

<span data-ttu-id="8d173-p101">En utilisant cette méthode, vous utilisez un modèle de Gestion des Ressources Azure(GRA) pour assembler intranet simulé. PROCESSEUR modèles contiennent toutes les instructions pour créer l’infrastructure réseau Azure, machines virtuelles et leur configuration.</span><span class="sxs-lookup"><span data-stu-id="8d173-p101">In this method, you use an Azure Resource Manager (ARM) template to build out the simulated intranet. ARM templates contain all of the instructions to create the Azure networking infrastructure, the virtual machines, and their configuration.</span></span>

<span data-ttu-id="8d173-117">Avant de déployer le modèle, parcourez le[modèle de la page Lisez-moi](https://github.com/maxskunkworks/TLG/tree/master/tlg-base-config_3-vm.m365-ems) et obtenez les informations suivantes prêtes :</span><span class="sxs-lookup"><span data-stu-id="8d173-117">Prior to deploying the template, read through the [template README page](https://github.com/maxskunkworks/TLG/tree/master/tlg-base-config_3-vm.m365-ems) and have the following information ready:</span></span>

- <span data-ttu-id="8d173-p102">Le nom de domaine DNS public de votre environnement de test (testlab.\< votre domaine public >). Vous devez entrer ce nom dans le**champ Nom de Domaine** de la page**déploiement Personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="8d173-p102">The public DNS domain name of your test environment (testlab.\<your public domain>). You’ll need to enter this name in the **Domain Name field** of the **Custom deployment** page.</span></span>
- <span data-ttu-id="8d173-p103">Un préfixe d’étiquette DNS pour les URL d’adresses IP publiques de vos machines virtuelles. Vous devez entrer cette étiquette dans le**préfixe d’étiquette Dns** champ de la page**déploiement Personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="8d173-p103">A DNS label prefix for the URLs of the public IP addresses of your virtual machines. You’ll need to enter this label in the **Dns Label Prefix** field of the **Custom deployment** page.</span></span>

<span data-ttu-id="8d173-122">Après avoir lu via les instructions, cliquez sur **déployer vers Azure** sur la [page modèle LISEZMOI](https://github.com/maxskunkworks/TLG/tree/master/tlg-base-config_3-vm.m365-ems) pour commencer.</span><span class="sxs-lookup"><span data-stu-id="8d173-122">After reading through the instructions, click **Deploy to Azure** on the [template README page](https://github.com/maxskunkworks/TLG/tree/master/tlg-base-config_3-vm.m365-ems) to get started.</span></span>

>[!Note]
><span data-ttu-id="8d173-123">L’Intranet simulé créé par le modèle GRA nécessite un abonnement payant à Azure.</span><span class="sxs-lookup"><span data-stu-id="8d173-123">The simulated intranet built by the ARM template requires a paid Azure subscription.</span></span>
>

<span data-ttu-id="8d173-124">Voici votre configuration une fois le modèle terminé.</span><span class="sxs-lookup"><span data-stu-id="8d173-124">Here is your configuration after the template is complete.</span></span>

![L’intranet simulé dans les services d’infrastructure Azure.](media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase3.png)

### <a name="method-2-build-your-simulated-intranet-with-azure-powershell"></a><span data-ttu-id="8d173-126">Méthode 2 : Créer votre intranet simulé avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8d173-126">Method 2: Build your simulated intranet with Azure PowerShell</span></span>

<span data-ttu-id="8d173-127">En utilisant cette méthode, vous utilisez Windows PowerShell et le module Azure PowerShell afin de créer l’infrastructure de réseau, les machines virtuelles et leur configuration.</span><span class="sxs-lookup"><span data-stu-id="8d173-127">In this method, you use Windows PowerShell and the Azure PowerShell module to build out the networking infrastructure, the virtual machines, and their configuration.</span></span>

<span data-ttu-id="8d173-p104">Utilisez cette méthode si vous souhaitez acquérir de l’expérience en créant des éléments d’infrastructure Azure, une étape après l’autre, avec PowerShell. Vous pouvez alors personnaliser les blocs de commande PowerShell pour votre propre déploiement d’autres machines virtuelles dans Azure.</span><span class="sxs-lookup"><span data-stu-id="8d173-p104">Use this method if you want to get experience creating elements of Azure infrastructure one step at a time with PowerShell. You can then customize the PowerShell command blocks for your own deployment of other virtual machines in Azure.</span></span>

#### <a name="step-1-create-dc1"></a><span data-ttu-id="8d173-130">Phase 1: création de DC1</span><span class="sxs-lookup"><span data-stu-id="8d173-130">Step 1: Create DC1</span></span>

<span data-ttu-id="8d173-131">Durant cette phase, nous allons créer un réseau virtuel Azure et ajouter la machine virtuelle DC1 qui est un contrôleur de domaine pour un domaine Windows Server Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="8d173-131">In this step, we create an Azure virtual network and add DC1, a virtual machine that is a domain controller for an AD DS domain.</span></span>

<span data-ttu-id="8d173-132">Tout d’abord, démarrez une invite de commandes Windows PowerShell sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8d173-132">First, start a Windows PowerShell command prompt on your local computer.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8d173-p105">Les ensembles de commandes suivants utilisent la dernière version d’Azure PowerShell. Reportez-vous à la rubrique relative à la [prise en main des cmdlets Azure PowerShell](https://docs.microsoft.com/powershell/azureps-cmdlets-docs/).</span><span class="sxs-lookup"><span data-stu-id="8d173-p105">The following command sets use the latest version of Azure PowerShell. See [Get started with Azure PowerShell cmdlets](https://docs.microsoft.com/powershell/azureps-cmdlets-docs/).</span></span> 
  
<span data-ttu-id="8d173-135">Connectez-vous à votre compte Azure avec la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="8d173-135">Sign in to your Azure account with the following command.</span></span>
  
```
Connect-AzAccount
```

<span data-ttu-id="8d173-136">Obtenez le nom de votre abonnement à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="8d173-136">Get your subscription name using the following command.</span></span>
  
```
Get-AzSubscription | Sort Name | Select Name
```

<span data-ttu-id="8d173-p106">Définissez votre abonnement Azure. Remplacez tout le texte entre guillemets, y compris les caractères < et >, avec le nom correct.</span><span class="sxs-lookup"><span data-stu-id="8d173-p106">Set your Azure subscription. Replace everything within the quotes, including the < and > characters, with the correct name.</span></span>
  
```
$subscr="<subscription name>"
Get-AzSubscription -SubscriptionName $subscr | Select-AzSubscription
```

<span data-ttu-id="8d173-p107">Ensuite, créez un nouveau groupe de ressources pour le laboratoire de test de votre entreprise simulée. Pour choisir un nom de groupe de ressources unique, utilisez cette commande pour répertorier les groupes de ressources existants.</span><span class="sxs-lookup"><span data-stu-id="8d173-p107">Next, create a new resource group for your simulated enterprise test lab. To determine a unique resource group name, use this command to list your existing resource groups.</span></span>
  
```
Get-AzResourceGroup | Sort ResourceGroupName | Select ResourceGroupName
```

<span data-ttu-id="8d173-p108">Créez votre nouveau groupe de ressources avec ces commandes. Remplacez tout le texte entre guillemets, y compris les caractères < et >, par les noms corrects.</span><span class="sxs-lookup"><span data-stu-id="8d173-p108">Create your new resource group with these commands. Replace everything within the quotes, including the < and > characters, with the correct names.</span></span>
  
```
$rgName="<resource group name>"
$locName="<location name, such as West US>"
New-AzResourceGroup -Name $rgName -Location $locName
```

<span data-ttu-id="8d173-p109">Ensuite, créez le réseau virtuel TestLab qui hébergera le sous-réseau du réseau de l’environnement de l’entreprise simulée et protégez-le avec un groupe de sécurité de réseau. Indiquez le nom de votre groupe de ressources et exécutez les commandes suivantes à l’invite de commandes PowerShell sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8d173-p109">Next, you create the TestLab virtual network that will host the Corpnet subnet of the simulated enterprise environment and protect it with a network security group. Fill in the name of your resource group and run these commands at the PowerShell command prompt on your local computer.</span></span>
  
```
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

<span data-ttu-id="8d173-145">Dans cette étape, nous créons la machine virtuelle DC1 et la configurons en tant que contrôleur de domaine pour votre domaine public**testlab.**\< AD DS (Active Directory Domain Services) et un serveur DNS pour les machines virtuelles du réseau virtuel TestLab.</span><span class="sxs-lookup"><span data-stu-id="8d173-145">Next, you create the DC1 virtual machine and configure it as a domain controller for the **testlab.**\<your public domain> AD DS domain and a DNS server for the virtual machines of the TestLab virtual network.</span></span> <span data-ttu-id="8d173-146">Par exemple, si votre nom de domaine public est \*\* <span>contoso</span>.com\*\*, la machine virtuelle DC1 sera un contrôleur de domaine pour le **<span>testlab</span>. contoso.com** domaine.</span><span class="sxs-lookup"><span data-stu-id="8d173-146">For example, if your public domain name is **<span>contoso</span>.com**, the DC1 virtual machine will be a domain controller for the **<span>testlab</span>.contoso.com** domain.</span></span>
  
<span data-ttu-id="8d173-147">Pour créer une machine virtuelle Azure pour DC1, indiquez d’abord le nom de votre groupe de ressources, puis exécutez ces commandes à l’invite de commandes PowerShell sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8d173-147">To create an Azure virtual machine for DC1, fill in the name of your resource group and run these commands at the PowerShell command prompt on your local computer.</span></span>
  
```
$rgName="<resource group name>"
$locName=(Get-AzResourceGroup -Name $rgName).Location
$vnet=Get-AzVirtualNetwork -Name TestLab -ResourceGroupName $rgName
$pip=New-AzPublicIpAddress -Name DC1-PIP -ResourceGroupName $rgName -Location $locName -AllocationMethod Dynamic
$nic=New-AzNetworkInterface -Name DC1-NIC -ResourceGroupName $rgName -Location $locName -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $pip.Id -PrivateIpAddress 10.0.0.4
$vm=New-AzVMConfig -VMName DC1 -VMSize Standard_A1
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

<span data-ttu-id="8d173-p111">Vous serez invité à indiquer un nom d’utilisateur et un mot de passe pour le compte d’administrateur local sur DC1. Utilisez un mot de passe et enregistrez le nom et le mot de passe dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="8d173-p111">You will be prompted for a user name and password for the local administrator account on DC1. Use a strong password and record both the name and password in a secure location.</span></span>
  
<span data-ttu-id="8d173-150">Ensuite, connectez-vous à la machine virtuelle DC1.</span><span class="sxs-lookup"><span data-stu-id="8d173-150">Next, connect to the DC1 virtual machine.</span></span>
  
1. <span data-ttu-id="8d173-151">Dans le [Portail Azure](https://portal.azure.com), cliquez sur **Groupes de Ressources >** [nom de votre nouveau groupe de ressources] **> DC1 > Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="8d173-151">In the [Azure portal](https://portal.azure.com), click **Resource Groups >** [the name of your new resource group] **> DC1 > Connect**.</span></span>
    
2. <span data-ttu-id="8d173-p112">Dans le volet ouvert, cliquez sur **Télécharger le fichier RDP**. Ouvrez le fichier DC1.rdp qui est téléchargé, puis cliquez sur **Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="8d173-p112">In the open pane, click **Download RDP file**. Open the DC1.rdp file that is downloaded, and then click **Connect**.</span></span>
    
3. <span data-ttu-id="8d173-154">Spécifiez le nom du compte Administrateur local DC1 :</span><span class="sxs-lookup"><span data-stu-id="8d173-154">Specify the DC1 local administrator account name:</span></span>
    
   - <span data-ttu-id="8d173-155">Pour Windows 7 :</span><span class="sxs-lookup"><span data-stu-id="8d173-155">For Windows 7:</span></span>
    
     <span data-ttu-id="8d173-p113">Dans la boîte de dialogue **Sécurité Windows**, cliquez sur **Utiliser un autre compte**. Dans **Nom d’utilisateur**, tapez **DC1\\**[nom du compte Administrateur local].</span><span class="sxs-lookup"><span data-stu-id="8d173-p113">In the **Windows Security** dialog box, click **Use another account**. In **User name**, type **DC1\\**[Local administrator account name].</span></span>
    
   - <span data-ttu-id="8d173-158">Pour Windows 8 ou Windows 10 :</span><span class="sxs-lookup"><span data-stu-id="8d173-158">For Windows 8 or Windows 10:</span></span>
    
     <span data-ttu-id="8d173-p114">Dans la boîte de dialogue **Sécurité Windows**, cliquez sur **Autres choix**, puis cliquez sur **Utiliser un autre compte**. Dans **Nom d’utilisateur**, tapez **DC1\\**[nom de compte Administrateur local].</span><span class="sxs-lookup"><span data-stu-id="8d173-p114">In the **Windows Security** dialog box, click **More choices**, and then click **Use a different account**. In **User name**, type **DC1\\**[Local administrator account name].</span></span>
    
4. <span data-ttu-id="8d173-161">Dans **Mot de passe**, tapez le mot de passe du compte Administrateur local, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d173-161">In **Password**, type the password of the local administrator account, and then click **OK**.</span></span>
    
5. <span data-ttu-id="8d173-162">Quand vous y êtes invité, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="8d173-162">When prompted, click **Yes**.</span></span>
    
<span data-ttu-id="8d173-163">Ensuite, ajoutez un disque de données supplémentaire en tant que nouveau volume avec la lettre de lecteur F:, à l’aide de la commande suivante, dans l’invite de commande Windows PowerShell au niveau administrateur sur DC1.</span><span class="sxs-lookup"><span data-stu-id="8d173-163">Next, add an extra data disk as a new volume with the drive letter F: with this command at an administrator-level Windows PowerShell command prompt on DC1.</span></span>
  
```
Get-Disk | Where PartitionStyle -eq "RAW" | Initialize-Disk -PartitionStyle MBR -PassThru | New-Partition -AssignDriveLetter -UseMaximumSize | Format-Volume -FileSystem NTFS -NewFileSystemLabel "WSAD Data"
```

<span data-ttu-id="8d173-p115">Maintenant, configurez DC1 comme un contrôleur de domaine et un serveur DNS pour le domaine **testlab.**\<votre domaine public>. Indiquez le nom de votre domaine public, supprimez les caractères \< et >, puis exécutez ces commandes à l’invite de commandes Windows PowerShell de niveau administrateur sur DC1.</span><span class="sxs-lookup"><span data-stu-id="8d173-p115">Next, configure DC1 as a domain controller and DNS server for the **testlab.**\<your public domain> domain. Specify your public domain name, remove the \< and > characters, and then run these commands at an administrator-level Windows PowerShell command prompt on DC1.</span></span>
  
```
$yourDomain="<your public domain>"
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
Install-ADDSForest -DomainName testlab.$yourDomain -DatabasePath "F:\NTDS" -SysvolPath "F:\SYSVOL" -LogPath "F:\Logs"
```
<span data-ttu-id="8d173-p116">Vous devez spécifier un mot de passe administrateur en mode sans échec. Conservez ce mot de passe dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="8d173-p116">You will need to specify a safe mode administrator password. Store this password in a secure location.</span></span>
  
<span data-ttu-id="8d173-168">Notez que l’exécution de ces commandes peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="8d173-168">Note that these commands can take a few minutes to complete.</span></span>
  
<span data-ttu-id="8d173-169">Après le redémarrage de DC1, reconnectez-vous à la machine virtuelle DC1.</span><span class="sxs-lookup"><span data-stu-id="8d173-169">After DC1 restarts, reconnect to the DC1 virtual machine.</span></span>
  
1. <span data-ttu-id="8d173-170">Dans le [Portail Azure](https://portal.azure.com), cliquez sur **Groupes de Ressources >** [nom de votre groupe de ressources] **> DC1 > Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="8d173-170">In the [Azure portal](https://portal.azure.com), click **Resource Groups >** [your resource group name] **> DC1 > Connect**.</span></span>
    
2. <span data-ttu-id="8d173-171">Exécutez le fichier DC1.rdp qui est téléchargé, puis cliquez sur **Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="8d173-171">Run the DC1.rdp file that is downloaded, and then click **Connect**.</span></span>
    
3. <span data-ttu-id="8d173-p117">Dans **Sécurité Windows**, cliquez sur **Utiliser un autre compte**. Dans **Nom d’utilisateur**, tapez **TESTLAB\\**[nom du compte Administrateur local].</span><span class="sxs-lookup"><span data-stu-id="8d173-p117">In **Windows Security**, click **Use another account**. In **User name**, type **TESTLAB\\**[Local administrator account name].</span></span>
    
4. <span data-ttu-id="8d173-174">Dans **Mot de passe**, tapez le mot de passe du compte Administrateur local, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d173-174">In **Password**, type the password of the local administrator account, and then click **OK**.</span></span>
    
5. <span data-ttu-id="8d173-175">Quand vous y êtes invité, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="8d173-175">When prompted, click **Yes**.</span></span>
    
<span data-ttu-id="8d173-p118">Ensuite, dans Active Directory, créez un compte d’utilisateur qui sera utilisé pour la connexion aux ordinateurs membres du domaine TESTLAB. Exécutez cette commande à l’invite de commandes Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="8d173-p118">Next, create a user account in Active Directory that will be used when logging in to TESTLAB domain member computers. Run this command at an administrator-level Windows PowerShell command prompt.</span></span>
  
```
New-ADUser -SamAccountName User1 -AccountPassword (read-host "Set user password" -assecurestring) -name "User1" -enabled $true -PasswordNeverExpires $true -ChangePasswordAtLogon $false
```

<span data-ttu-id="8d173-p119">Notez que cette commande vous invite à renseigner le mot de passe du compte Utilisateur1 (User1). Étant donné que ce compte est utilisé pour les connexions de bureau à distance pour tous les ordinateurs membres du domaine TESTLAB, choisissez un mot de passe fort. Enregistrez le mot de passe du compte Utilisateur1 et stockez-le dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="8d173-p119">Note that this command prompts you to supply the User1 account password. Because this account will be used for remote desktop connections for all TESTLAB domain member computers, choose a strong password. Record the User1 account password and store it in a secured location.</span></span>
  
<span data-ttu-id="8d173-p120">Maintenant, configurez le nouveau compte Utilisateur1 comme un administrateur de schéma, d’entreprise et de domaine. Exécutez cette commande à l’invite de commandes Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="8d173-p120">Next, configure the new User1 account as a domain, enterprise, and schema administrator. Run this command at the administrator-level Windows PowerShell command prompt.</span></span>
  
```
$yourDomain="<your public domain>"
$domainName = "testlab"+$yourDomain
$userName="user1@" + $domainName
$userSID=(New-Object System.Security.Principal.NTAccount($userName)).Translate([System.Security.Principal.SecurityIdentifier]).Value
$groupNames=@("Domain Admins","Enterprise Admins","Schema Admins")
ForEach ($name in $groupNames) {Add-ADPrincipalGroupMembership -Identity $userSID -MemberOf (Get-ADGroup -Identity $name).SID.Value}
```

<span data-ttu-id="8d173-183">Fermez la session Bureau à distance avec DC1 et reconnectez-vous à l’aide du compte TESTLAB\\Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="8d173-183">Close the Remote Desktop session with DC1 and then reconnect using the TESTLAB\\User1 account.</span></span>
  
<span data-ttu-id="8d173-184">Ensuite, pour autoriser le trafic pour l’outil Ping, exécutez cette commande à l’invite de commandes Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="8d173-184">Next, to allow traffic for the Ping tool, run this command at an administrator-level Windows PowerShell command prompt.</span></span>
  
```
Set-NetFirewallRule -DisplayName "File and Printer Sharing (Echo Request - ICMPv4-In)" -enabled True
```

<span data-ttu-id="8d173-185">Il s’agit de votre configuration actuelle.</span><span class="sxs-lookup"><span data-stu-id="8d173-185">This is your current configuration.</span></span>
  
![Phase 1 de la configuration de base de l’entreprise simulée](media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase1.png)
  
#### <a name="step-2-configure-app1"></a><span data-ttu-id="8d173-187">Phase 2:Configurer APP1</span><span class="sxs-lookup"><span data-stu-id="8d173-187">Step 2: Configure APP1</span></span>

<span data-ttu-id="8d173-188">Durant cette phase, vous allez créer et configurer APP1, qui est un serveur d’applications qui fournit initial des services web et de partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="8d173-188">In this step, you create and configure APP1, which is an application server that initially provides web and file sharing services.</span></span>

<span data-ttu-id="8d173-189">Pour créer une machine virtuelle Azure pour APP1, renseignez d’abord le nom de votre groupe de ressources, puis exécutez ces commandes à l’invite de commandes sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8d173-189">To create an Azure Virtual Machine for APP1, fill in the name of your resource group and run these commands at the  command prompt on your local computer.</span></span>
  
```
$rgName="<resource group name>"
$locName=(Get-AzResourceGroup -Name $rgName).Location
$vnet=Get-AzVirtualNetwork -Name TestLab -ResourceGroupName $rgName
$pip=New-AzPublicIpAddress -Name APP1-PIP -ResourceGroupName $rgName -Location $locName -AllocationMethod Dynamic
$nic=New-AzNetworkInterface -Name APP1-NIC -ResourceGroupName $rgName -Location $locName -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $pip.Id
$vm=New-AzVMConfig -VMName APP1 -VMSize Standard_A1
$cred=Get-Credential -Message "Type the name and password of the local administrator account for APP1."
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName APP1 -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name "APP1-OS" -DiskSizeInGB 128 -CreateOption FromImage
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm
```

<span data-ttu-id="8d173-190">Ensuite, connectez-vous à la machine virtuelle APP1 en utilisant le nom du compte Administrateur local APP1 et le mot de passe, et ouvrez une invite de commande Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8d173-190">Next, connect to the APP1 virtual machine using the APP1 local administrator account name and password, and then open a Windows PowerShell command prompt.</span></span>
  
<span data-ttu-id="8d173-191">Pour vérifier la résolution du nom et la communication réseau entre APP1 et DC1, exécutez la commande **ping dc1.testlab.**\<votre nom de domaine public> et vérifiez que quatre réponses apparaissent.</span><span class="sxs-lookup"><span data-stu-id="8d173-191">To check name resolution and network communication between APP1 and DC1, run the **ping dc1.testlab.**\<your public domain name> command and verify that there are four replies.</span></span>
  
<span data-ttu-id="8d173-192">Maintenant, associez la machine virtuelle APP1 au domaine TESTLAB avec ces commandes à l’invite Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8d173-192">Next, join the APP1 virtual machine to the TESTLAB domain with these commands at the Windows PowerShell prompt.</span></span>
  
```
$yourDomain="<your public domain name>"
Add-Computer -DomainName ("testlab" + $yourDomain)
Restart-Computer
```

<span data-ttu-id="8d173-193">Les informations d’identification du compte de domaine TESTLAB\\Utilisateur1 doivent être fournies après l’exécution de la commande **Add-Computer**.</span><span class="sxs-lookup"><span data-stu-id="8d173-193">Note that you must supply the TESTLAB\\User1 domain account credentials after running the **Add-Computer** command.</span></span>
  
<span data-ttu-id="8d173-194">Après le redémarrage d’APP1, connectez-vous en utilisant le compte TESTLAB\\Utilisateur1 et ouvrez une invite de commandes Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="8d173-194">After APP1 restarts, connect to it using the TESTLAB\\User1 account, and then open an administrator-level Windows PowerShell command prompt.</span></span>
  
<span data-ttu-id="8d173-195">Transformez APP1 en serveur web en exécutant cette commande à l’invite de commandes Windows PowerShell de niveau supérieur sur APP1.</span><span class="sxs-lookup"><span data-stu-id="8d173-195">Next, make APP1 a web server with this command at an administrator-level Windows PowerShell command prompt on APP1.</span></span>
  
```
Install-WindowsFeature Web-WebServer -IncludeManagementTools
```

<span data-ttu-id="8d173-196">Ensuite, créez un dossier partagé et un fichier de texte dans le dossier sur APP1 avec ces commandes PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8d173-196">Next, create a shared folder and a text file within the folder on APP1 with these PowerShell commands.</span></span>
  
```
New-Item -path c:\files -type directory
Write-Output "This is a shared file." | out-file c:\files\example.txt
New-SmbShare -name files -path c:\files -changeaccess TESTLAB\User1
```

<span data-ttu-id="8d173-197">Il s’agit de votre configuration actuelle.</span><span class="sxs-lookup"><span data-stu-id="8d173-197">This is your current configuration.</span></span>
  
![Phase 2 de la configuration de base de l’entreprise simulée](media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase2.png)
  
#### <a name="step-3-configure-client1"></a><span data-ttu-id="8d173-199">Phase 3:Configurer CLIENT1</span><span class="sxs-lookup"><span data-stu-id="8d173-199">Step 3: Configure CLIENT1</span></span>

<span data-ttu-id="8d173-200">Durant cette phase, vous allez créer et configurer CLIENT1, qui se comporte comme un ordinateur portable, une tablette ou un ordinateur de bureau classique sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="8d173-200">In this step, you create and configure CLIENT1, which acts as a typical laptop, tablet, or desktop computer on the intranet.</span></span>

> [!NOTE]  
> <span data-ttu-id="8d173-p121">Le jeu de commandes suivant crée CLIENT1 en exécutant Windows Server 2016 Datacenter, pour tous les types d’abonnements Azure. Si vous avez un abonnement Azure basé sur Visual Studio, vous pouvez créer CLIENT1 en exécutant Windows 10, avec le [portail Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="8d173-p121">The following command set creates CLIENT1 running Windows Server 2016 Datacenter, which can be done for all types of Azure subscriptions. If you have an Visual Studio-based Azure subscription, you can create CLIENT1 running Windows 10 with the [Azure portal](https://portal.azure.com).</span></span> 
  
<span data-ttu-id="8d173-203">Pour créer une machine virtuelle Azure pour CLIENT1, renseignez d’abord le nom de votre groupe de ressources, puis exécutez ces commandes à l’invite de commandes sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8d173-203">To create an Azure Virtual Machine for CLIENT1, fill in the name of your resource group and run these commands at the  command prompt on your local computer.</span></span>
  
```
$rgName="<resource group name>"
$locName=(Get-AzResourceGroup -Name $rgName).Location
$vnet=Get-AzVirtualNetwork -Name TestLab -ResourceGroupName $rgName
$pip=New-AzPublicIpAddress -Name CLIENT1-PIP -ResourceGroupName $rgName -Location $locName -AllocationMethod Dynamic
$nic=New-AzNetworkInterface -Name CLIENT1-NIC -ResourceGroupName $rgName -Location $locName -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $pip.Id
$vm=New-AzVMConfig -VMName CLIENT1 -VMSize Standard_A1
$cred=Get-Credential -Message "Type the name and password of the local administrator account for CLIENT1."
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName CLIENT1 -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name "CLIENT1-OS" -DiskSizeInGB 128 -CreateOption FromImage
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm
```

<span data-ttu-id="8d173-204">Ensuite, connectez-vous à la machine virtuelle CLIENT1 en utilisant le nom du compte Administrateur local CLIENT1 et le mot de passe, et ouvrez une invite de commande Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="8d173-204">Next, connect to the CLIENT1 virtual machine using the CLIENT1 local administrator account name and password, and then open an administrator-level Windows PowerShell command prompt.</span></span>
  
<span data-ttu-id="8d173-205">Pour vérifier la résolution du nom et la communication réseau entre CLIENT1 et DC1, exécutez la commande **ping dc1.testlab.**\<votre nom de domaine public> à l’invite de commandes Windows PowerShell et vérifiez que quatre réponses apparaissent.</span><span class="sxs-lookup"><span data-stu-id="8d173-205">To check name resolution and network communication between CLIENT1 and DC1, run the **ping dc1.testlab.**\<your public domain name> command at a Windows PowerShell command prompt and verify that there are four replies.</span></span>
  
<span data-ttu-id="8d173-206">Maintenant, associez la machine virtuelle CLIENT1 au domaine TESTLAB avec ces commandes à l’invite Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8d173-206">Next, join the CLIENT1 virtual machine to the TESTLAB domain with these commands at the Windows PowerShell prompt.</span></span>
  
```
$yourDomain="<your public domain name>"
Add-Computer -DomainName ("testlab" + $yourDomain)
Restart-Computer
```

<span data-ttu-id="8d173-207">Les informations d’identification de votre compte de domaine TESTLAB\\Utilisateur1 doivent être fournies après l’exécution de la commande **Add-Computer**.</span><span class="sxs-lookup"><span data-stu-id="8d173-207">Note that you must supply your TESTLAB\\User1 domain account credentials after running the **Add-Computer** command.</span></span>
  
<span data-ttu-id="8d173-208">Après le redémarrage de CLIENT1, connectez-vous en utilisant le mot de passe et le nom du compte TESTLAB\\Utilisateur1 et ouvrez une invite de commandes Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="8d173-208">After CLIENT1 restarts, connect to it using the TESTLAB\\User1 account name and password, and then open an administrator-level Windows PowerShell command prompt.</span></span>
  
<span data-ttu-id="8d173-209">Ensuite, vérifiez que vous pouvez accéder aux ressources web et de partage de fichiers sur APP1 de CLIENT1.</span><span class="sxs-lookup"><span data-stu-id="8d173-209">Next, verify that you can access web and file share resources on APP1 from CLIENT1.</span></span>
  
1. <span data-ttu-id="8d173-210">Dans le Gestionnaire de Serveur, dans le volet de l’arborescence, cliquez sur **Serveur Local**.</span><span class="sxs-lookup"><span data-stu-id="8d173-210">In Server Manager, in the tree pane, click **Local Server**.</span></span>
    
2. <span data-ttu-id="8d173-211">Dans **Propriétés pour CLIENT1**, cliquez sur **Activer** à côté de **Configuration de sécurité renforcée d’Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="8d173-211">In **Properties for CLIENT1**, click **On** next to **IE Enhanced Security Configuration**.</span></span>
    
3. <span data-ttu-id="8d173-212">Dans **Configuration de sécurité renforcée d’Internet Explorer**, cliquez sur **Désactiver** pour **Administrateurs** et **Utilisateurs**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d173-212">In **Internet Explorer Enhanced Security Configuration**, click **Off** for **Administrators** and **Users**, and then click **OK**.</span></span>
    
4. <span data-ttu-id="8d173-213">Sur l’écran d’accueil, cliquez sur **Internet Explorer**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d173-213">From the Start screen, click **Internet Explorer**, and then click **OK**.</span></span>
    
5. <span data-ttu-id="8d173-p122">Dans la barre d’adresses, tapez **http<span>://</span>app1.testab.**\<votre nom de domaine public>**/**, puis appuyez sur ENTRÉE. La page web Internet Information Services par défaut pour APP1 s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8d173-p122">In the Address bar, type **http<span>://</span>app1.testab.**\<your public domain name>**/**, and then press ENTER. You should see the default Internet Information Services web page for APP1.</span></span>
    
6. <span data-ttu-id="8d173-216">Dans la barre des tâches du bureau, cliquez sur l’icône de l’Explorateur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="8d173-216">From the desktop taskbar, click the File Explorer icon.</span></span>
    
7. <span data-ttu-id="8d173-p123">Dans la barre d’adresses, tapez **\\\\app1\\Files**, puis appuyez sur ENTRÉE. Une fenêtre de dossiers avec le contenu du dossier partagé Fichiers apparaît.</span><span class="sxs-lookup"><span data-stu-id="8d173-p123">In the address bar, type **\\\\app1\\Files**, and then press ENTER. You should see a folder window with the contents of the Files shared folder.</span></span>
    
8. <span data-ttu-id="8d173-p124">Dans la fenêtre du dossier partagé **Fichiers**, double-cliquez sur le fichier **Exemple.txt**. Le contenu du fichier Exemple.txt s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8d173-p124">In the **Files** shared folder window, double-click the **Example.txt** file. You should see the contents of the Example.txt file.</span></span>
    
9. <span data-ttu-id="8d173-221">Fermez les fenêtres de dossiers partagés **Exemple.txt - Bloc-notes** et **Fichiers**.</span><span class="sxs-lookup"><span data-stu-id="8d173-221">Close the **example.txt - Notepad** and the **Files** shared folder windows.</span></span>
    
<span data-ttu-id="8d173-222">Il s’agit de votre configuration actuelle.</span><span class="sxs-lookup"><span data-stu-id="8d173-222">This is your current configuration.</span></span>
  
![Phase 3 de la configuration de base de l’entreprise simulée](media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase3.png)


## <a name="phase-2-create-your-microsoft-365-e5-subscriptions"></a><span data-ttu-id="8d173-224">Phase 2 : Création de vos abonnements Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="8d173-224">Phase 2: Create your Microsoft 365 E5 subscriptions</span></span>

<span data-ttu-id="8d173-p125">Durant cette phase, vous allez créer un nouvel abonnement Microsoft 365 E5 qui utilise un nouveau client Azure AD commun, différent de votre abonnement de production. Vous pouvez procéder de deux façons :</span><span class="sxs-lookup"><span data-stu-id="8d173-p125">In this phase, you create a new Microsoft 365 E5 subscription that use a new Azure AD tenant, one that is separate from your production subscription. You can do this in two ways:</span></span>

- <span data-ttu-id="8d173-227">Utiliser un abonnement d’évaluation de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="8d173-227">Use a trial subscription of Microsoft 365 E5.</span></span> 

  <span data-ttu-id="8d173-p126">L’abonnement à la version d’évaluation Microsoft 365 E5 est valable 30 jours et peut être porté facilement à 60 jours. Quand l’abonnement à la version d’évaluation expire, soit vous le convertissez en abonnement payant, soit vous créez un nouvel abonnement à la version d’évaluation. Si vous choisissez cette dernière option, vous ne pourrez pas conserver votre configuration et les scénarios complexes qu’elle peut contenir.</span><span class="sxs-lookup"><span data-stu-id="8d173-p126">The Microsoft 365 E5 trial subscription is 30 days, which can be easily extended to 60 days. When the trial subscription expires, you must either convert it to a paid subscriptions or create a new trial subscription. Creating new trial subscriptions means you will leave your configuration, which could include complex scenarios, behind.</span></span>  
- <span data-ttu-id="8d173-231">Utiliser un abonnement de production de Microsoft 365 E5 distinct avec un nombre réduit de licences.</span><span class="sxs-lookup"><span data-stu-id="8d173-231">Use a separate production subscription of Microsoft 365 E5 with a small number of licenses.</span></span>

  <span data-ttu-id="8d173-p127">Cette solution a un coût supplémentaire, mais elle vous permet de bénéficier d’un environnement de test opérationnel pour essayer des fonctionnalités, des configurations et des scénarios sans contrainte de temps. Vous pouvez utiliser le même environnement de test sur le long terme pour valider la faisabilité des concepts, réaliser des démonstrations auprès de vos pairs et de votre direction, et développer et tester des applications. Nous vous recommandons d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="8d173-p127">This is an additional cost, but ensures that you have a working test environment to try features, configurations, and scenarios that does not expire. You can use the same test environment over the long term for proofs of concept, demonstration to peers and management, and application development and testing. This is the recommended method.</span></span>

### <a name="use-trial-subscriptions"></a><span data-ttu-id="8d173-235">Utilisation des abonnements à la version d’évaluation</span><span class="sxs-lookup"><span data-stu-id="8d173-235">Use trial subscriptions</span></span>

<span data-ttu-id="8d173-236">Suivez les étapes des phases 2 et 3 de l’article sur l’[environnement de développement/test Office 365](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment) pour créer un environnement de développement/test Office 365 léger.</span><span class="sxs-lookup"><span data-stu-id="8d173-236">First, follow the steps in Phase 2 and Phase 3 of the [Office 365 dev/test environment](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment) to create a lightweight Office 365 dev/test environment.</span></span>

>[!Note]
><span data-ttu-id="8d173-237">Vous avez créé un abonnement d’évaluation d’Office 365 pour que votre environnement de développement/test ait un client Azure AD distinct de tout abonnement payant que vous utilisez actuellement.</span><span class="sxs-lookup"><span data-stu-id="8d173-237">We have you create a trial subscription of Office 365 so that your dev/test environment has a separate Azure AD tenant from any paid subscriptions you currently have.</span></span> <span data-ttu-id="8d173-238">Cette séparation signifie que vous pouvez ajouter et supprimer des utilisateurs et groupes dans le client test sans incidence sur vos abonnements de production.</span><span class="sxs-lookup"><span data-stu-id="8d173-238">This separation means you can add and remove users and groups in the test tenant without effecting your production subscriptions.</span></span>
>

<span data-ttu-id="8d173-239">Ensuite, ajoutez l’abonnement d’évaluation Microsoft 365 E5 et attribuez une licence Microsoft 365 à votre compte Administrateur général.</span><span class="sxs-lookup"><span data-stu-id="8d173-239">Next, add the Microsoft 365 E5 trial subscription and assign a Microsoft 365 license to your global administrator account.</span></span>

1. <span data-ttu-id="8d173-240">Utilisez une instance privée d’un navigateur Internet pour vous connecter au centre d’administration Microsoft 365 sur [https://admin.microsoft.com](https://admin.microsoft.com)à l’aide de vos informations d’identification de compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="8d173-240">With a private instance of an Internet browser, sign in to the Microsoft 365 admin center at [https://admin.microsoft.com](https://admin.microsoft.com) with your global administrator account credentials.</span></span>
    
2. <span data-ttu-id="8d173-241">Sur la page **Centre d’administration Microsoft 365**, dans le volet de navigation de gauche, cliquez sur **Facturation > Acheter des services**.</span><span class="sxs-lookup"><span data-stu-id="8d173-241">On the **Microsoft 365 admin center** page, in the left navigation, click **Billing > Purchase services**.</span></span>
    
3. <span data-ttu-id="8d173-242">Sur la page**acheter des services**, recherchez l’élément **Microsoft 365 E5**.</span><span class="sxs-lookup"><span data-stu-id="8d173-242">On the **Purchase services** page, find the **Microsoft 365 E5** item.</span></span> <span data-ttu-id="8d173-243">Pointez votre souris dessus et cliquez sur **Démarrer l’essai gratuit**.</span><span class="sxs-lookup"><span data-stu-id="8d173-243">Hover your mouse pointer over it and click **Start free trial**.</span></span>

4. <span data-ttu-id="8d173-244">Sur la page **version d’évaluation de Microsoft 365 E5**, choisissez de recevoir un SMS ou un appel, entrez votre numéro de téléphone, puis cliquez sur **envoyer un SMS** ou **m’appeler**.</span><span class="sxs-lookup"><span data-stu-id="8d173-244">On the **Microsoft 365 E5 Trial** page, choose to receive a text or a call, enter your phone number, then click **Text me** or **Call me**.</span></span>

5. <span data-ttu-id="8d173-245">Dans la page **Confirmer votre commande**, cliquez sur **Essayer maintenant**.</span><span class="sxs-lookup"><span data-stu-id="8d173-245">On the **Confirm your order** page, click **Try now**.</span></span>

6. <span data-ttu-id="8d173-246">Dans la page **Réception de la commande**, cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="8d173-246">On the **Order receipt** page, click **Continue**.</span></span>

7. <span data-ttu-id="8d173-247">Dans le centre d’administration Microsoft 365, cliquez sur **utilisateurs actifs**et votre compte d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="8d173-247">In the Microsoft 365 admin center, click **Active users**, and then your administrator account.</span></span>

8. <span data-ttu-id="8d173-248">Cliquez sur **modifier** pour **licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="8d173-248">Click **Edit** for **Product licenses**.</span></span>

9. <span data-ttu-id="8d173-249">Désactivez la licence pour Office 365 Entreprise E5 et activer la licence pour Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="8d173-249">Turn off the license for Office 365 Enterprise E5 and turn on the license for Microsoft 365 E5.</span></span>

10. <span data-ttu-id="8d173-250">Cliquez sur **Enregistrer > Fermer > Fermer**.</span><span class="sxs-lookup"><span data-stu-id="8d173-250">Click **Save > Close > Close**.</span></span>

 <span data-ttu-id="8d173-251">***Si vous avez terminé la Phase 3 de l’*** [environnement de développement/test Office 365](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment), répétez les étapes 8 et 11 de la procédure précédente pour tous vos autres comptes (Utilisateur 2, Utilisateur 3, Utilisateur 4 et Utilisateur 5).</span><span class="sxs-lookup"><span data-stu-id="8d173-251">Next, ***if you completed Phase 3 of the*** [Office 365 dev/test environment](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment), repeat steps 8 through 11 of the previous procedure for all of your other accounts (User 2, User 3, User 4, and User 5).</span></span>
  
> [!NOTE]
> <span data-ttu-id="8d173-252">L’abonnement d’évaluation de Microsoft 365 E5 est de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="8d173-252">The Microsoft 365 E5 trial subscription is 30 days.</span></span> <span data-ttu-id="8d173-253">Pour un environnement de test permanent, convertissez cet abonnement en abonnement payant avec un nombre réduit de licences.</span><span class="sxs-lookup"><span data-stu-id="8d173-253">For a permanent test environment, convert this trial subscription to a paid subscription with a small number of licenses.</span></span>
  
<span data-ttu-id="8d173-254">Votre environnement de test comporte maintenant :</span><span class="sxs-lookup"><span data-stu-id="8d173-254">Your test environment now has:</span></span>
  
- <span data-ttu-id="8d173-255">Un abonnement d’évaluation de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="8d173-255">A Microsoft 365 E5 trial subscription.</span></span>
- <span data-ttu-id="8d173-256">Tous vos comptes d’utilisateur appropriés (l’administrateur général ou tous les cinq comptes d’utilisateur) sont activés pour utiliser Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="8d173-256">All your appropriate user accounts (either just the global administrator or all five user accounts) are enabled to use Microsoft 365 E5.</span></span>
    
### <a name="results"></a><span data-ttu-id="8d173-257">Résultats</span><span class="sxs-lookup"><span data-stu-id="8d173-257">Results</span></span>

<span data-ttu-id="8d173-258">Votre environnement de test comporte maintenant :</span><span class="sxs-lookup"><span data-stu-id="8d173-258">Your test environment now has:</span></span>
  
- <span data-ttu-id="8d173-259">Abonnement d’évaluation de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="8d173-259">Microsoft 365 E5 trial subscription.</span></span>
- <span data-ttu-id="8d173-260">Tous vos comptes d’utilisateur appropriés (l’administrateur général ou tous les cinq comptes d’utilisateur) sont activés pour utiliser Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="8d173-260">All your appropriate user accounts (either just the global administrator or all five user accounts) are enabled to use Microsoft 365 E5.</span></span>
    
<span data-ttu-id="8d173-261">Il s’agit de votre configuration finale.</span><span class="sxs-lookup"><span data-stu-id="8d173-261">This is your final configuration.</span></span>
  
![Phase 4 de la configuration de base de l’entreprise simulée](media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase4.png)
  
<span data-ttu-id="8d173-263">Vous êtes désormais prêt à profiter des fonctionnalités supplémentaires de [Microsoft 365 Entreprise](https://www.microsoft.com/microsoft-365/enterprise).</span><span class="sxs-lookup"><span data-stu-id="8d173-263">You are now ready to experiment with additional features of [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="8d173-264">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="8d173-264">Next steps</span></span>

<span data-ttu-id="8d173-265">Découvrez les nouveaux ensembles de guides pour les tests de laboratoire :</span><span class="sxs-lookup"><span data-stu-id="8d173-265">Explore these additional sets of Test Lab Guides:</span></span>
  
- [<span data-ttu-id="8d173-266">Identité</span><span class="sxs-lookup"><span data-stu-id="8d173-266">Identity</span></span>](m365-enterprise-test-lab-guides.md#identity)
- [<span data-ttu-id="8d173-267">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="8d173-267">Mobile device management</span></span>](m365-enterprise-test-lab-guides.md#mobile-device-management)
- [<span data-ttu-id="8d173-268">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="8d173-268">Information protection</span></span>](m365-enterprise-test-lab-guides.md#information-protection)

## <a name="see-also"></a><span data-ttu-id="8d173-269">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d173-269">See also</span></span>

[<span data-ttu-id="8d173-270">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="8d173-270">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="8d173-271">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="8d173-271">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="8d173-272">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="8d173-272">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
