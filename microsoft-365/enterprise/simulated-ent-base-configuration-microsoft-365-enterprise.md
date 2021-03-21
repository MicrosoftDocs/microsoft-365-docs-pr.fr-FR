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
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom:
- Ent_TLGs
- seo-marvel-apr2020
ms.assetid: 6f916a77-301c-4be2-b407-6cec4d80df76
description: Utilisez ce guide de laboratoire de test pour créer un environnement de test d’entreprise simulé pour Microsoft 365 pour entreprise.
ms.openlocfilehash: 8df63e1a580b57aa263c11dccaed947f46f2cbb9
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50926043"
---
# <a name="the-simulated-enterprise-base-configuration"></a><span data-ttu-id="1ddd9-103">Configuration de base d’une entreprise simulée</span><span class="sxs-lookup"><span data-stu-id="1ddd9-103">The simulated enterprise base configuration</span></span>

<span data-ttu-id="1ddd9-104">*Ce guide de laboratoire de test peut être utilisé pour les environnements de test Microsoft 365 entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="1ddd9-104">*This Test Lab Guide can be used for both Microsoft 365 for enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="1ddd9-105">Cet article explique comment créer un environnement simplifié pour Microsoft 365 pour entreprise qui inclut :</span><span class="sxs-lookup"><span data-stu-id="1ddd9-105">This article describes how to create a simplified environment for Microsoft 365 for enterprise that includes:</span></span>

- <span data-ttu-id="1ddd9-106">Un abonnement d’évaluation ou payant Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-106">A Microsoft 365 E5 trial or paid subscription.</span></span>
- <span data-ttu-id="1ddd9-107">Un intranet d’organisation simplifié connecté à Internet, constitué de trois machines virtuelles sur un réseau virtuel Azure (DC1, APP1 et CLIENT1).</span><span class="sxs-lookup"><span data-stu-id="1ddd9-107">A simplified organization intranet connected to the internet, consisting of three virtual machines on an Azure virtual network (DC1, APP1, and CLIENT1).</span></span>
 
![Configuration de base d’une entreprise simulée](../media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase4.png)

<span data-ttu-id="1ddd9-109">La création d’un environnement de test simplifié implique deux phases :</span><span class="sxs-lookup"><span data-stu-id="1ddd9-109">Creating a simplified test environment involves two phases:</span></span>
- [<span data-ttu-id="1ddd9-110">Phase 1: Créer un intranet simulé</span><span class="sxs-lookup"><span data-stu-id="1ddd9-110">Phase 1: Create a simulated intranet</span></span>](#phase-1-create-a-simulated-intranet)
- [<span data-ttu-id="1ddd9-111">Phase 2 : Création de votre abonnement Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="1ddd9-111">Phase 2: Create your Microsoft 365 E5 subscription</span></span>](#phase-2-create-your-microsoft-365-e5-subscription)

<span data-ttu-id="1ddd9-112">Vous pouvez utiliser l’environnement résultant pour tester les fonctionnalités de [Microsoft 365](https://www.microsoft.com/microsoft-365/enterprise) pour entreprise à l’aide de guides de laboratoire de [test](m365-enterprise-test-lab-guides.md) supplémentaires ou par vous-même.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-112">You can use the resulting environment to test the features and functionality of [Microsoft 365 for enterprise](https://www.microsoft.com/microsoft-365/enterprise) with additional [Test Lab Guides](m365-enterprise-test-lab-guides.md) or on your own.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="1ddd9-114">Pour obtenir une carte visuelle de tous les articles de la pile du Guide de laboratoire de test Microsoft 365 pour entreprise, allez à [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="1ddd9-114">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>

## <a name="phase-1-create-a-simulated-intranet"></a><span data-ttu-id="1ddd9-115">Phase 1: Créer un intranet simulé</span><span class="sxs-lookup"><span data-stu-id="1ddd9-115">Phase 1: Create a simulated intranet</span></span>

<span data-ttu-id="1ddd9-116">Dans cette phase, créez un intranet simulé dans les services d’infrastructure Azure qui inclut un contrôleur de domaine AD DS (Active Directory Domain Services), un serveur d’applications et un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-116">In this phase, build a simulated intranet in Azure infrastructure services that includes an Active Directory Domain Services (AD DS) domain controller, an application server, and a client computer.</span></span>

<span data-ttu-id="1ddd9-117">Vous utiliserez ces ordinateurs dans d’autres guides de laboratoire de [test Microsoft 365](m365-enterprise-test-lab-guides.md) pour entreprise pour configurer et montrer l’identité hybride et d’autres fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-117">You'll use these computers in additional [Microsoft 365 for enterprise Test Lab Guides](m365-enterprise-test-lab-guides.md) to configure and demonstrate hybrid identity and other capabilities.</span></span>

### <a name="method-1-build-your-simulated-intranet-with-an-azure-resource-manager-template"></a><span data-ttu-id="1ddd9-118">Méthode 1: Créer votre intranet simulé avec un Modèle de Gestion de Ressources Azure </span><span class="sxs-lookup"><span data-stu-id="1ddd9-118">Method 1: Build your simulated intranet with an Azure Resource Manager template</span></span>

<span data-ttu-id="1ddd9-119">Dans cette méthode, vous utilisez un modèle Azure Resource Manager pour créer l’intranet simulé.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-119">In this method, you use an Azure Resource Manager template to build out the simulated intranet.</span></span> <span data-ttu-id="1ddd9-120">Les modèles Azure Resource Manager contiennent toutes les instructions pour créer l’infrastructure réseau Azure, les machines virtuelles et leur configuration.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-120">Azure Resource Manager templates contain all of the instructions to create the Azure networking infrastructure, the virtual machines, and their configuration.</span></span>

<span data-ttu-id="1ddd9-121">Avant de déployer le modèle, lisez la [page README du](https://github.com/maxskunkworks/TLG/tree/master/tlg-base-config_3-vm.m365-ems) modèle et préparez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1ddd9-121">Before deploying the template, read through the [template README page](https://github.com/maxskunkworks/TLG/tree/master/tlg-base-config_3-vm.m365-ems) and have the following information ready:</span></span>

- <span data-ttu-id="1ddd9-122">Nom de domaine DNS public de votre environnement de test (testlab). \<*your public domain*></span><span class="sxs-lookup"><span data-stu-id="1ddd9-122">The public DNS domain name of your test environment (testlab.\<*your public domain*>).</span></span> <span data-ttu-id="1ddd9-123">Vous devez entrer ce nom dans le champ Nom de **domaine** de la page **Déploiement** personnalisé.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-123">You'll enter this name in the **Domain Name** field of the **Custom deployment** page.</span></span>
- <span data-ttu-id="1ddd9-p103">Un préfixe d’étiquette DNS pour les URL d’adresses IP publiques de vos machines virtuelles. Vous devez entrer cette étiquette dans le **préfixe d’étiquette Dns** champ de la page **déploiement Personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-p103">A DNS label prefix for the URLs of the public IP addresses of your virtual machines. You'll need to enter this label in the **Dns Label Prefix** field of the **Custom deployment** page.</span></span>

<span data-ttu-id="1ddd9-126">Après avoir lu les instructions, sélectionnez **Déployer sur Azure** sur la page MODÈLE [README](https://github.com/maxskunkworks/TLG/tree/master/tlg-base-config_3-vm.m365-ems) pour commencer.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-126">After you read through the instructions, select **Deploy to Azure** on the [template README page](https://github.com/maxskunkworks/TLG/tree/master/tlg-base-config_3-vm.m365-ems) to get started.</span></span>

>[!Note]
><span data-ttu-id="1ddd9-127">L’intranet simulé créé par le modèle Azure Resource Manager nécessite un abonnement Azure payant.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-127">The simulated intranet built by the Azure Resource Manager template requires a paid Azure subscription.</span></span>

<span data-ttu-id="1ddd9-128">Une fois le modèle terminé, votre configuration ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="1ddd9-128">After the template is complete, your configuration looks like this:</span></span>

![L’intranet simulé dans les services d’infrastructure Azure.](../media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase3.png)

### <a name="method-2-build-your-simulated-intranet-with-azure-powershell"></a><span data-ttu-id="1ddd9-130">Méthode 2 : Créer votre intranet simulé avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1ddd9-130">Method 2: Build your simulated intranet with Azure PowerShell</span></span>

<span data-ttu-id="1ddd9-131">En utilisant cette méthode, vous utilisez Windows PowerShell et le module Azure PowerShell afin de créer l’infrastructure de réseau, les machines virtuelles et leur configuration.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-131">In this method, you use Windows PowerShell and the Azure PowerShell module to build out the networking infrastructure, the virtual machines, and their configuration.</span></span>

<span data-ttu-id="1ddd9-p104">Utilisez cette méthode si vous souhaitez acquérir de l’expérience en créant des éléments d’infrastructure Azure, une étape après l’autre, avec PowerShell. Vous pouvez alors personnaliser les blocs de commande PowerShell pour votre propre déploiement d’autres machines virtuelles dans Azure.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-p104">Use this method if you want to get experience creating elements of Azure infrastructure one step at a time with PowerShell. You can then customize the PowerShell command blocks for your own deployment of other virtual machines in Azure.</span></span>

#### <a name="step-1-create-dc1"></a><span data-ttu-id="1ddd9-134">Phase 1: création de DC1</span><span class="sxs-lookup"><span data-stu-id="1ddd9-134">Step 1: Create DC1</span></span>

<span data-ttu-id="1ddd9-135">Dans cette étape, vous allez créer un réseau virtuel Azure et ajouter DC1, une machine virtuelle qui est un contrôleur de domaine pour un domaine AD DS.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-135">In this step, you create an Azure virtual network and add DC1, a virtual machine that is a domain controller for an AD DS domain.</span></span>

<span data-ttu-id="1ddd9-136">Tout d’abord, démarrez une invite de commandes Windows PowerShell sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-136">First, start a Windows PowerShell command prompt on your local computer.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1ddd9-p105">Les ensembles de commandes suivants utilisent la dernière version d’Azure PowerShell. Reportez-vous à la rubrique relative à la [prise en main des cmdlets Azure PowerShell](/powershell/azureps-cmdlets-docs/).</span><span class="sxs-lookup"><span data-stu-id="1ddd9-p105">The following command sets use the latest version of Azure PowerShell. See [Get started with Azure PowerShell cmdlets](/powershell/azureps-cmdlets-docs/).</span></span> 
  
<span data-ttu-id="1ddd9-139">Connectez-vous à votre compte Azure avec la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-139">Sign in to your Azure account with the following command.</span></span>
  
```powershell
Connect-AzAccount
```

<span data-ttu-id="1ddd9-140">Obtenez le nom de votre abonnement à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-140">Get your subscription name using the following command.</span></span>
  
```powershell
Get-AzSubscription | Sort Name | Select Name
```

<span data-ttu-id="1ddd9-141">Définissez votre abonnement Azure.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-141">Set your Azure subscription.</span></span> <span data-ttu-id="1ddd9-142">Remplacez tout le texte entre guillemets, y compris les crochets (« < » et « > ») par le nom correct.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-142">Replace everything within the quotation marks, including the angle brackets ("<" and ">"), with the correct name.</span></span>
  
```powershell
$subscr="<subscription name>"
Get-AzSubscription -SubscriptionName $subscr | Select-AzSubscription
```

<span data-ttu-id="1ddd9-p107">Ensuite, créez un nouveau groupe de ressources pour le laboratoire de test de votre entreprise simulée. Pour choisir un nom de groupe de ressources unique, utilisez cette commande pour répertorier les groupes de ressources existants.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-p107">Next, create a new resource group for your simulated enterprise test lab. To determine a unique resource group name, use this command to list your existing resource groups.</span></span>
  
```powershell
Get-AzResourceGroup | Sort ResourceGroupName | Select ResourceGroupName
```

<span data-ttu-id="1ddd9-145">Créez votre nouveau groupe de ressources avec ces commandes.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-145">Create your new resource group with these commands.</span></span> <span data-ttu-id="1ddd9-146">Remplacez tout le texte entre guillemets, y compris les crochets, par les noms corrects.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-146">Replace everything within the quotation marks, including the angle brackets, with the correct names.</span></span>
  
```powershell
$rgName="<resource group name>"
$locName="<location name, such as West US>"
New-AzResourceGroup -Name $rgName -Location $locName
```

<span data-ttu-id="1ddd9-147">Ensuite, créez le réseau virtuel TestLab qui hébergera le sous-réseau du réseau d’entreprise de l’environnement d’entreprise simulé et protégez-le avec un groupe de sécurité réseau.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-147">Next, create the TestLab virtual network that will host the corporate network subnet of the simulated enterprise environment and protect it with a network security group.</span></span> <span data-ttu-id="1ddd9-148">Remplissez le nom de votre groupe de ressources et exécutez ces commandes à l’invite de commandes PowerShell sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-148">Fill in the name of your resource group and run these commands at the PowerShell command prompt on your local computer.</span></span>
  
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

<span data-ttu-id="1ddd9-149">Ensuite, vous créez la machine virtuelle DC1 et le configurez comme contrôleur de domaine pour le **testlab.**\<your public domain></span><span class="sxs-lookup"><span data-stu-id="1ddd9-149">Next, you create the DC1 virtual machine and configure it as a domain controller for the **testlab.**\<your public domain></span></span> <span data-ttu-id="1ddd9-150">Domaine AD DS et serveur DNS pour les machines virtuelles du réseau virtuel TestLab.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-150">AD DS domain and a DNS server for the virtual machines of the TestLab virtual network.</span></span> <span data-ttu-id="1ddd9-151">Par exemple, si votre nom de domaine public est **<span>contoso</span>.com**, la machine virtuelle DC1 sera un contrôleur de domaine pour le **<span>testlab</span>. contoso.com** domaine.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-151">For example, if your public domain name is **<span>contoso</span>.com**, the DC1 virtual machine will be a domain controller for the **<span>testlab</span>.contoso.com** domain.</span></span>
  
<span data-ttu-id="1ddd9-152">Pour créer une machine virtuelle Azure pour DC1, indiquez d’abord le nom de votre groupe de ressources, puis exécutez ces commandes à l’invite de commandes PowerShell sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-152">To create an Azure virtual machine for DC1, fill in the name of your resource group and run these commands at the PowerShell command prompt on your local computer.</span></span>
  
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

<span data-ttu-id="1ddd9-p111">Vous serez invité à indiquer un nom d’utilisateur et un mot de passe pour le compte d’administrateur local sur DC1. Utilisez un mot de passe et enregistrez le nom et le mot de passe dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-p111">You will be prompted for a user name and password for the local administrator account on DC1. Use a strong password and record both the name and password in a secure location.</span></span>
  
<span data-ttu-id="1ddd9-155">Ensuite, connectez-vous à la machine virtuelle DC1 :</span><span class="sxs-lookup"><span data-stu-id="1ddd9-155">Next, connect to the DC1 virtual machine:</span></span>
  
1. <span data-ttu-id="1ddd9-156">Dans le [portail Azure,](https://portal.azure.com)sélectionnez Groupes de **ressources** > <le nom de votre nouveau groupe de ressources _ ***> > _* DC1**  >  **Connect**.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-156">In the [Azure portal](https://portal.azure.com), select **Resource Groups** > <**_the name of your new resource group_*_> > _\* DC1*\* > **Connect**.</span></span>
    
2. <span data-ttu-id="1ddd9-157">Dans le volet ouvert, sélectionnez **Télécharger le fichier RDP.**</span><span class="sxs-lookup"><span data-stu-id="1ddd9-157">In the open pane, select **Download RDP file**.</span></span> <span data-ttu-id="1ddd9-158">Ouvrez le fichier DC1.rdp qui est téléchargé, puis sélectionnez **Se connecter.**</span><span class="sxs-lookup"><span data-stu-id="1ddd9-158">Open the DC1.rdp file that is downloaded, and then select **Connect**.</span></span>
    
3. <span data-ttu-id="1ddd9-159">Spécifiez le nom du compte Administrateur local DC1 :</span><span class="sxs-lookup"><span data-stu-id="1ddd9-159">Specify the DC1 local administrator account name:</span></span>
    
   - <span data-ttu-id="1ddd9-160">Pour Windows 7 :</span><span class="sxs-lookup"><span data-stu-id="1ddd9-160">For Windows 7:</span></span>
    
     <span data-ttu-id="1ddd9-161">Dans la boîte **de dialogue Sécurité Windows,** **sélectionnez Utiliser un autre compte.**</span><span class="sxs-lookup"><span data-stu-id="1ddd9-161">In the **Windows Security** dialog box, select **Use another account**.</span></span> <span data-ttu-id="1ddd9-162">Dans **le nom d’utilisateur,** entrez le nom du compte administrateur local **DC1 \\** < >.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-162">In **User name**, enter **DC1\\**<*local administrator account name*>.</span></span>
    
   - <span data-ttu-id="1ddd9-163">Pour Windows 8 ou Windows 10 :</span><span class="sxs-lookup"><span data-stu-id="1ddd9-163">For Windows 8 or Windows 10:</span></span>
    
     <span data-ttu-id="1ddd9-164">Dans la **boîte de dialogue Sécurité Windows,** sélectionnez Plus de **choix,** puis **sélectionnez Utiliser un autre compte.**</span><span class="sxs-lookup"><span data-stu-id="1ddd9-164">In the **Windows Security** dialog box, select **More choices**, and then select **Use a different account**.</span></span> <span data-ttu-id="1ddd9-165">Dans **le nom d’utilisateur,** entrez le nom du compte administrateur local **DC1 \\** < >.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-165">In **User name**, enter **DC1\\**<*local administrator account name*>.</span></span>
    
4. <span data-ttu-id="1ddd9-166">Dans **Mot de** passe, entrez le mot de passe du compte d’administrateur local, puis sélectionnez **OK.**</span><span class="sxs-lookup"><span data-stu-id="1ddd9-166">In **Password**, enter the password of the local administrator account, and then select **OK**.</span></span>
    
5. <span data-ttu-id="1ddd9-167">Lorsque vous y invitez, sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-167">When prompted, select **Yes**.</span></span>
    
<span data-ttu-id="1ddd9-168">Ensuite, ajoutez un disque de données supplémentaire en tant que nouveau volume avec la lettre de lecteur F:, à l’aide de la commande suivante, dans l’invite de commande Windows PowerShell au niveau administrateur sur DC1.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-168">Next, add an extra data disk as a new volume with the drive letter F: with this command at an administrator-level Windows PowerShell command prompt on DC1.</span></span>
  
```powershell
Get-Disk | Where PartitionStyle -eq "RAW" | Initialize-Disk -PartitionStyle MBR -PassThru | New-Partition -AssignDriveLetter -UseMaximumSize | Format-Volume -FileSystem NTFS -NewFileSystemLabel "WSAD Data"
```

<span data-ttu-id="1ddd9-169">Ensuite, configurez DC1 comme un contrôleur de domaine et un serveur DNS pour le domaine **testlab.**\<*your public domain*></span><span class="sxs-lookup"><span data-stu-id="1ddd9-169">Next, configure DC1 as a domain controller and DNS server for the **testlab.**\<*your public domain*></span></span> <span data-ttu-id="1ddd9-170">.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-170">domain.</span></span> <span data-ttu-id="1ddd9-171">Spécifiez votre nom de domaine public, supprimez les crochets, puis exécutez ces commandes à une invite de commandes de niveau administrateur Windows PowerShell sur DC1.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-171">Specify your public domain name, remove the angle brackets, and then run these commands at an administrator-level Windows PowerShell command prompt on DC1.</span></span>
  
```powershell
$yourDomain="<your public domain>"
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
Install-ADDSForest -DomainName testlab.$yourDomain -DatabasePath "F:\NTDS" -SysvolPath "F:\SYSVOL" -LogPath "F:\Logs"
```
<span data-ttu-id="1ddd9-p116">Vous devez spécifier un mot de passe administrateur en mode sans échec. Conservez ce mot de passe dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-p116">You will need to specify a safe mode administrator password. Store this password in a secure location.</span></span>
  
<span data-ttu-id="1ddd9-174">Notez que l’exécution de ces commandes peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-174">Note that these commands can take a few minutes to complete.</span></span>
  
<span data-ttu-id="1ddd9-175">Après le redémarrage de DC1, reconnectez-vous à la machine virtuelle DC1.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-175">After DC1 restarts, reconnect to the DC1 virtual machine.</span></span>
  
1. <span data-ttu-id="1ddd9-176">Dans le [portail Azure, sélectionnez](https://portal.azure.com) **Groupes** de ressources > <*nom* de votre groupe de ressources> > **DC1**  >  **Connect**.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-176">In the [Azure portal](https://portal.azure.com), select **Resource Groups** > <*your resource group name*> > **DC1** > **Connect**.</span></span>
    
2. <span data-ttu-id="1ddd9-177">Exécutez le fichier DC1.rdp téléchargé, puis sélectionnez **Se connecter.**</span><span class="sxs-lookup"><span data-stu-id="1ddd9-177">Run the DC1.rdp file that is downloaded, and then select **Connect**.</span></span>
    
3. <span data-ttu-id="1ddd9-178">Dans **Sécurité Windows,** **sélectionnez Utiliser un autre compte.**</span><span class="sxs-lookup"><span data-stu-id="1ddd9-178">In **Windows Security**, select **Use another account**.</span></span> <span data-ttu-id="1ddd9-179">Dans **le nom d’utilisateur,** entrez le nom du compte **\\** < *d’administrateur local* TESTLAB>.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-179">In **User name**, enter **TESTLAB\\**<*local administrator account name*>.</span></span>
    
4. <span data-ttu-id="1ddd9-180">Dans la **zone Mot** de passe, entrez le mot de passe du compte d’administrateur local, puis sélectionnez **OK.**</span><span class="sxs-lookup"><span data-stu-id="1ddd9-180">In the **Password** box, enter the password of the local administrator account, and then select **OK**.</span></span>
    
5. <span data-ttu-id="1ddd9-181">Lorsque vous y invitez, sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-181">When prompted, select **Yes**.</span></span>
    
<span data-ttu-id="1ddd9-182">Ensuite, créez un compte d’utilisateur dans Active Directory qui sera utilisé lors de la signature sur les ordinateurs membres du domaine TESTLAB.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-182">Next, create a user account in Active Directory that will be used when signing in to TESTLAB domain member computers.</span></span> <span data-ttu-id="1ddd9-183">Exécutez cette commande à l’invite de commande Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-183">Run this command at an administrator-level Windows PowerShell command prompt.</span></span>
  
```powershell
New-ADUser -SamAccountName User1 -AccountPassword (read-host "Set user password" -assecurestring) -name "User1" -enabled $true -PasswordNeverExpires $true -ChangePasswordAtLogon $false
```

<span data-ttu-id="1ddd9-184">Notez que cette commande vous invite à indiquer le mot de passe du compte Utilisateur 1.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-184">Note that this command prompts you to supply the User1 account password.</span></span> <span data-ttu-id="1ddd9-185">Ce compte sera utilisé pour les connexions bureau à distance pour tous les ordinateurs membres du domaine TESTLAB. Choisissez donc un mot de passe fort.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-185">This account will be used for remote desktop connections for all TESTLAB domain member computers, so choose a strong password.</span></span> <span data-ttu-id="1ddd9-186">Enregistrez le mot de passe du compte Utilisateur 1 et stockez-le dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-186">Record the User1 account password and store it in a secured location.</span></span>
  
<span data-ttu-id="1ddd9-p120">Maintenant, configurez le nouveau compte Utilisateur1 comme un administrateur de schéma, d’entreprise et de domaine. Exécutez cette commande à l’invite de commandes Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-p120">Next, configure the new User1 account as a domain, enterprise, and schema administrator. Run this command at the administrator-level Windows PowerShell command prompt.</span></span>
  
```powershell
$yourDomain="<your public domain>"
$domainName = "testlab."+$yourDomain
$userName="user1@" + $domainName
$userSID=(New-Object System.Security.Principal.NTAccount($userName)).Translate([System.Security.Principal.SecurityIdentifier]).Value
$groupNames=@("Domain Admins","Enterprise Admins","Schema Admins")
ForEach ($name in $groupNames) {Add-ADPrincipalGroupMembership -Identity $userSID -MemberOf (Get-ADGroup -Identity $name).SID.Value}
```

<span data-ttu-id="1ddd9-189">Fermez la session Bureau à distance avec DC1 et reconnectez-vous à l’aide du compte TESTLAB\\Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-189">Close the Remote Desktop session with DC1 and then reconnect using the TESTLAB\\User1 account.</span></span>
  
<span data-ttu-id="1ddd9-190">Ensuite, pour autoriser le trafic pour l’outil Ping, exécutez cette commande à l’invite de commandes Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-190">Next, to allow traffic for the Ping tool, run this command at an administrator-level Windows PowerShell command prompt.</span></span>
  
```powershell
Set-NetFirewallRule -DisplayName "File and Printer Sharing (Echo Request - ICMPv4-In)" -enabled True
```

<span data-ttu-id="1ddd9-191">Votre configuration actuelle se présente comme ceci :</span><span class="sxs-lookup"><span data-stu-id="1ddd9-191">Your current configuration looks like this:</span></span>
  
![Phase 1 de la configuration de base de l’entreprise simulée](../media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase1.png)
  
#### <a name="step-2-configure-app1"></a><span data-ttu-id="1ddd9-193">Phase 2:Configurer APP1</span><span class="sxs-lookup"><span data-stu-id="1ddd9-193">Step 2: Configure APP1</span></span>

<span data-ttu-id="1ddd9-194">Durant cette phase, vous allez créer et configurer APP1, qui est un serveur d’applications qui fournit initial des services web et de partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-194">In this step, you create and configure APP1, which is an application server that initially provides web and file sharing services.</span></span>

<span data-ttu-id="1ddd9-195">Pour créer une machine virtuelle Azure pour APP1, renseignez d’abord le nom de votre groupe de ressources, puis exécutez ces commandes à l’invite de commandes sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-195">To create an Azure Virtual Machine for APP1, fill in the name of your resource group and run these commands at the  command prompt on your local computer.</span></span>
  
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

<span data-ttu-id="1ddd9-196">Ensuite, connectez-vous à la machine virtuelle APP1 en utilisant le nom du compte Administrateur local APP1 et le mot de passe, et ouvrez une invite de commande Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-196">Next, connect to the APP1 virtual machine using the APP1 local administrator account name and password, and then open a Windows PowerShell command prompt.</span></span>
  
<span data-ttu-id="1ddd9-197">Pour vérifier la résolution de noms et les communications réseau entre APP1 et DC1, exécutez la commande **ping dc1.testlab.**\<*your public domain name*></span><span class="sxs-lookup"><span data-stu-id="1ddd9-197">To check name resolution and network communication between APP1 and DC1, run the **ping dc1.testlab.**\<*your public domain name*></span></span> <span data-ttu-id="1ddd9-198">et vérifiez qu’il y a quatre réponses.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-198">command and verify that there are four replies.</span></span>
  
<span data-ttu-id="1ddd9-199">Maintenant, associez la machine virtuelle APP1 au domaine TESTLAB avec ces commandes à l’invite Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-199">Next, join the APP1 virtual machine to the TESTLAB domain with these commands at the Windows PowerShell prompt.</span></span>
  
```powershell
$yourDomain="<your public domain name>"
Add-Computer -DomainName ("testlab." + $yourDomain)
Restart-Computer
```

<span data-ttu-id="1ddd9-200">Notez qu’après avoir exécuté la commande **Add-Computer,** vous devez fournir les informations d’identification du compte de domaine TESTLAB \\ User1.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-200">Note that you after you run the **Add-Computer** command, you must supply the TESTLAB\\User1 domain account credentials.</span></span>
  
<span data-ttu-id="1ddd9-201">Après le redémarrage d’APP1, connectez-vous en utilisant le compte TESTLAB\\Utilisateur1 et ouvrez une invite de commandes Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-201">After APP1 restarts, connect to it using the TESTLAB\\User1 account, and then open an administrator-level Windows PowerShell command prompt.</span></span>
  
<span data-ttu-id="1ddd9-202">Transformez APP1 en serveur web en exécutant cette commande à l’invite de commandes Windows PowerShell de niveau supérieur sur APP1.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-202">Next, make APP1 a web server with this command at an administrator-level Windows PowerShell command prompt on APP1.</span></span>
  
```powershell
Install-WindowsFeature Web-WebServer -IncludeManagementTools
```

<span data-ttu-id="1ddd9-203">Ensuite, créez un dossier partagé et un fichier de texte dans le dossier sur APP1 avec ces commandes PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-203">Next, create a shared folder and a text file within the folder on APP1 with these PowerShell commands.</span></span>
  
```powershell
New-Item -path c:\files -type directory
Write-Output "This is a shared file." | out-file c:\files\example.txt
New-SmbShare -name files -path c:\files -changeaccess TESTLAB\User1
```

<span data-ttu-id="1ddd9-204">Votre configuration actuelle se présente comme ceci :</span><span class="sxs-lookup"><span data-stu-id="1ddd9-204">Your current configuration looks like this:</span></span>
  
![Phase 2 de la configuration de base de l’entreprise simulée](../media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase2.png)
  
#### <a name="step-3-configure-client1"></a><span data-ttu-id="1ddd9-206">Phase 3:Configurer CLIENT1</span><span class="sxs-lookup"><span data-stu-id="1ddd9-206">Step 3: Configure CLIENT1</span></span>

<span data-ttu-id="1ddd9-207">Durant cette phase, vous allez créer et configurer CLIENT1, qui se comporte comme un ordinateur portable, une tablette ou un ordinateur de bureau classique sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-207">In this step, you create and configure CLIENT1, which acts as a typical laptop, tablet, or desktop computer on the intranet.</span></span>

> [!NOTE]  
> <span data-ttu-id="1ddd9-p122">Le jeu de commandes suivant crée CLIENT1 en exécutant Windows Server 2016 Datacenter, pour tous les types d’abonnements Azure. Si vous avez un abonnement Azure basé sur Visual Studio, vous pouvez créer CLIENT1 en exécutant Windows 10, avec le [portail Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="1ddd9-p122">The following command set creates CLIENT1 running Windows Server 2016 Datacenter, which can be done for all types of Azure subscriptions. If you have a Visual Studio-based Azure subscription, you can create CLIENT1 running Windows 10 with the [Azure portal](https://portal.azure.com).</span></span>
  
<span data-ttu-id="1ddd9-210">Pour créer une machine virtuelle Azure pour CLIENT1, remplissez le nom de votre groupe de ressources et exécutez ces commandes à l’invite de commandes sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-210">To create an Azure Virtual Machine for CLIENT1, fill in the name of your resource group and run these commands at the command prompt on your local computer.</span></span>
  
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

<span data-ttu-id="1ddd9-211">Ensuite, connectez-vous à la machine virtuelle CLIENT1 en utilisant le nom du compte Administrateur local CLIENT1 et le mot de passe, et ouvrez une invite de commande Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-211">Next, connect to the CLIENT1 virtual machine using the CLIENT1 local administrator account name and password, and then open an administrator-level Windows PowerShell command prompt.</span></span>
  
<span data-ttu-id="1ddd9-212">Pour vérifier la résolution de noms et les communications réseau entre CLIENT1 et DC1, exécutez la commande **ping dc1.testlab.**\<*your public domain name*></span><span class="sxs-lookup"><span data-stu-id="1ddd9-212">To check name resolution and network communication between CLIENT1 and DC1, run the **ping dc1.testlab.**\<*your public domain name*></span></span> <span data-ttu-id="1ddd9-213">dans une invite de commandes Windows PowerShell et vérifiez qu’il y a quatre réponses.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-213">command at a Windows PowerShell command prompt and verify that there are four replies.</span></span>
  
<span data-ttu-id="1ddd9-214">Maintenant, associez la machine virtuelle CLIENT1 au domaine TESTLAB avec ces commandes à l’invite Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-214">Next, join the CLIENT1 virtual machine to the TESTLAB domain with these commands at the Windows PowerShell prompt.</span></span>
  
```powershell
$yourDomain="<your public domain name>"
Add-Computer -DomainName ("testlab." + $yourDomain)
Restart-Computer
```

<span data-ttu-id="1ddd9-215">Les informations d’identification de votre compte de domaine TESTLAB\\Utilisateur1 doivent être fournies après l’exécution de la commande **Add-Computer**.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-215">Note that you must supply your TESTLAB\\User1 domain account credentials after running the **Add-Computer** command.</span></span>
  
<span data-ttu-id="1ddd9-216">Après le redémarrage de CLIENT1, connectez-vous en utilisant le mot de passe et le nom du compte TESTLAB\\Utilisateur1 et ouvrez une invite de commandes Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-216">After CLIENT1 restarts, connect to it using the TESTLAB\\User1 account name and password, and then open an administrator-level Windows PowerShell command prompt.</span></span>
  
<span data-ttu-id="1ddd9-217">Ensuite, vérifiez que vous pouvez accéder aux ressources web et de partage de fichiers sur APP1 de CLIENT1.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-217">Next, verify that you can access web and file share resources on APP1 from CLIENT1.</span></span>
  
1. <span data-ttu-id="1ddd9-218">Dans le Gestionnaire de serveur, dans le volet d’arborescence, sélectionnez **Serveur local.**</span><span class="sxs-lookup"><span data-stu-id="1ddd9-218">In Server Manager, in the tree pane, select **Local Server**.</span></span>
    
2. <span data-ttu-id="1ddd9-219">Dans **les propriétés de CLIENT1,** **sélectionnez Sur** en plus de la configuration de sécurité renforcée **d’IE.**</span><span class="sxs-lookup"><span data-stu-id="1ddd9-219">In **Properties for CLIENT1**, select **On** next to **IE Enhanced Security Configuration**.</span></span>
    
3. <span data-ttu-id="1ddd9-220">Dans **la configuration de sécurité renforcée d’Internet Explorer,** sélectionnez **Off** pour les administrateurs et les **utilisateurs,** puis **sélectionnez OK**. </span><span class="sxs-lookup"><span data-stu-id="1ddd9-220">In **Internet Explorer Enhanced Security Configuration**, select **Off** for **Administrators** and **Users**, and then select **OK**.</span></span>
    
4. <span data-ttu-id="1ddd9-221">Dans l’écran d’accueil, **sélectionnez Internet Explorer,** puis **sélectionnez OK.**</span><span class="sxs-lookup"><span data-stu-id="1ddd9-221">From the Start screen, select **Internet Explorer**, and then select **OK**.</span></span>
    
5. <span data-ttu-id="1ddd9-222">Dans la barre d’adresses, **entrez http <span>://</span>app1.testab.** \<*your public domain name*> **/** , puis appuyez sur **Entrée**.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-222">In the address bar, enter **http <span>://</span>app1.testab.**\<*your public domain name*>**/**, and then press **Enter**.</span></span> <span data-ttu-id="1ddd9-223">La page web Internet Information Services par défaut pour APP1 s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-223">You should see the default Internet Information Services web page for APP1.</span></span>
    
6. <span data-ttu-id="1ddd9-224">Dans la barre des tâches du bureau, sélectionnez l’icône Explorateur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-224">On the desktop taskbar, select the File Explorer icon.</span></span>
    
7. <span data-ttu-id="1ddd9-225">Dans la barre d’adresses, entrez **\\ \\ fichiers app1, \\** puis appuyez sur **Entrée**.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-225">In the address bar, enter **\\\\app1\\Files**, and then press **Enter**.</span></span> <span data-ttu-id="1ddd9-226">Une fenêtre de dossiers avec le contenu du dossier partagé Fichiers apparaît.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-226">You should see a folder window with the contents of the Files shared folder.</span></span>
    
8. <span data-ttu-id="1ddd9-p126">Dans la fenêtre du dossier partagé **Fichiers**, double-cliquez sur le fichier **Exemple.txt**. Le contenu du fichier Exemple.txt s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-p126">In the **Files** shared folder window, double-click the **Example.txt** file. You should see the contents of the Example.txt file.</span></span>
    
9. <span data-ttu-id="1ddd9-229">Fermez les fenêtres de dossiers partagés **Exemple.txt - Bloc-notes** et **Fichiers**.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-229">Close the **example.txt - Notepad** and the **Files** shared folder windows.</span></span>
    
<span data-ttu-id="1ddd9-230">Votre configuration actuelle se présente comme ceci :</span><span class="sxs-lookup"><span data-stu-id="1ddd9-230">Your current configuration looks like this:</span></span>
  
![Phase 3 de la configuration de base de l’entreprise simulée](../media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase3.png)

## <a name="phase-2-create-your-microsoft-365-e5-subscription"></a><span data-ttu-id="1ddd9-232">Phase 2 : Création de votre abonnement Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="1ddd9-232">Phase 2: Create your Microsoft 365 E5 subscription</span></span>

<span data-ttu-id="1ddd9-p127">Durant cette phase, vous allez créer un nouvel abonnement Microsoft 365 E5 qui utilise un nouveau client Azure AD commun, différent de votre abonnement de production. Vous pouvez procéder de deux façons :</span><span class="sxs-lookup"><span data-stu-id="1ddd9-p127">In this phase, you create a new Microsoft 365 E5 subscription that uses a new Azure AD tenant, one that is separate from your production subscription. You can do this in two ways:</span></span>

- <span data-ttu-id="1ddd9-235">Utiliser un abonnement d’évaluation de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-235">Use a trial subscription of Microsoft 365 E5.</span></span>

  <span data-ttu-id="1ddd9-p128">L’abonnement à la version d’évaluation Microsoft 365 E5 est valable 30 jours et peut être porté facilement à 60 jours. Quand l’abonnement à la version d’évaluation expire, soit vous le convertissez en abonnement payant, soit vous créez un nouvel abonnement à la version d’évaluation. Si vous choisissez cette dernière option, vous ne pourrez pas conserver votre configuration et les scénarios complexes qu’elle peut contenir.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-p128">The Microsoft 365 E5 trial subscription is 30 days, which can be easily extended to 60 days. When the trial subscription expires, you must either convert it to a paid subscription or create a new trial subscription. Creating new trial subscriptions means you will leave your configuration, which could include complex scenarios, behind.</span></span>  

- <span data-ttu-id="1ddd9-239">Utiliser un abonnement de production de Microsoft 365 E5 distinct avec un nombre réduit de licences.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-239">Use a separate production subscription of Microsoft 365 E5 with a small number of licenses.</span></span>

  <span data-ttu-id="1ddd9-240">Il s’agit d’un coût supplémentaire, mais garantit que vous avez un environnement de test de travail qui n’expire pas ; vous pouvez essayer des fonctionnalités, des configurations et des scénarios.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-240">This is an additional cost, but ensures that you have a working test environment that doesn't expire; in it, you can try features, configurations, and scenarios.</span></span> <span data-ttu-id="1ddd9-241">Vous pouvez utiliser le même environnement de test à long terme pour les preuves de concept, la démonstration aux pairs et à la gestion, ainsi que pour le développement et les tests d’applications.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-241">You can use the same test environment over the long term for proofs of concept, demonstration to peers and management, and application development and testing.</span></span> <span data-ttu-id="1ddd9-242">Il s'agit de la méthode recommandée.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-242">This is the recommended method.</span></span>

### <a name="sign-up-for-an-office-365-e5-trial-subscription"></a><span data-ttu-id="1ddd9-243">Inscription à un abonnement d’évaluation Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="1ddd9-243">Sign up for an Office 365 E5 trial subscription</span></span>

<span data-ttu-id="1ddd9-244">À partir du portail Azure, connectez-vous à CLIENT1 avec le compte CORP\User1.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-244">From the Azure portal, connect to CLIENT1 with the CORP\User1 account.</span></span>

<span data-ttu-id="1ddd9-245">Pour créer un abonnement d’évaluation Office 365 E5, suivez les instructions de [phase 1](lightweight-base-configuration-microsoft-365-enterprise.md#phase-1-create-your-microsoft-365-e5-subscription) du Guide de laboratoire de test de la configuration de base légère.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-245">To create a new Office 365 E5 trial subscription, perform the instructions in [Phase 1](lightweight-base-configuration-microsoft-365-enterprise.md#phase-1-create-your-microsoft-365-e5-subscription) of the lightweight base configuration Test Lab Guide.</span></span>

<span data-ttu-id="1ddd9-246">Pour configurer un abonnement d’évaluation Office 365 E5, suivez les instructions de [phase 2](lightweight-base-configuration-microsoft-365-enterprise.md#phase-2-configure-your-office-365-trial-subscription) du Guide de laboratoire de test de la configuration de base légère.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-246">To configure your new Office 365 E5 trial subscription, perform the instructions in [Phase 2](lightweight-base-configuration-microsoft-365-enterprise.md#phase-2-configure-your-office-365-trial-subscription) of the lightweight base configuration Test Lab Guide.</span></span>

#### <a name="using-an-office-365-e5-test-environment"></a><span data-ttu-id="1ddd9-247">Utilisation d’un environnement de test Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="1ddd9-247">Using an Office 365 E5 test environment</span></span>

<span data-ttu-id="1ddd9-248">Si vous n’avez besoin que d’un environnement de test Office 365, vous n’avez pas besoin de lire le reste de cet article.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-248">If you need only an Office 365 test environment, you do not need to read the rest of this article.</span></span>

<span data-ttu-id="1ddd9-249">Pour obtenir des guides de laboratoire de test supplémentaires qui s’appliquent à Microsoft 365 et Office 365, consultez les guides de laboratoire de [test Microsoft 365 pour](m365-enterprise-test-lab-guides.md)entreprise.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-249">For additional Test Lab Guides that apply to both Microsoft 365 and Office 365, see [Microsoft 365 for enterprise Test Lab Guides](m365-enterprise-test-lab-guides.md).</span></span>

### <a name="add-a-microsoft-365-e5-trial-subscription"></a><span data-ttu-id="1ddd9-250">Ajouter un abonnement d’évaluation de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-250">Add a Microsoft 365 E5 trial subscription</span></span>

<span data-ttu-id="1ddd9-251">Pour ajouter un abonnement d’essai Microsoft 365 E5 et configurer vos comptes d’utilisateurs avec des licences, exécutez les instructions de la [phase 3](lightweight-base-configuration-microsoft-365-enterprise.md#phase-3-add-a-microsoft-365-e5-trial-subscription) du Guide de laboratoire de test de configuration de base légère.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-251">To add a Microsoft 365 E5 trial subscription and configure your users accounts with licenses, perform the instructions in [Phase 3](lightweight-base-configuration-microsoft-365-enterprise.md#phase-3-add-a-microsoft-365-e5-trial-subscription) of the lightweight base configuration Test Lab Guide.</span></span>

  
## <a name="results"></a><span data-ttu-id="1ddd9-252">Résultats</span><span class="sxs-lookup"><span data-stu-id="1ddd9-252">Results</span></span>

<span data-ttu-id="1ddd9-253">Votre environnement de test comporte maintenant :</span><span class="sxs-lookup"><span data-stu-id="1ddd9-253">Your test environment now has:</span></span>
  
- <span data-ttu-id="1ddd9-254">Abonnement d’évaluation de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-254">Microsoft 365 E5 trial subscription.</span></span>
- <span data-ttu-id="1ddd9-255">Tous vos comptes d’utilisateurs appropriés sont configurés pour utiliser Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-255">All your appropriate user accounts are enabled to use Microsoft 365 E5.</span></span>
- <span data-ttu-id="1ddd9-256">Un intranet simulé et simplifié.</span><span class="sxs-lookup"><span data-stu-id="1ddd9-256">A simulated and simplified intranet.</span></span>
    
<span data-ttu-id="1ddd9-257">Votre configuration finale ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="1ddd9-257">Your final configuration looks like this:</span></span>
  
![Phase 2 de la configuration de base de l’entreprise simulée](../media/simulated-ent-base-configuration-microsoft-365-enterprise/Phase4.png)
  
<span data-ttu-id="1ddd9-259">Vous êtes maintenant prêt à expérimenter des fonctionnalités supplémentaires de [Microsoft 365 pour entreprise.](https://www.microsoft.com/microsoft-365/enterprise)</span><span class="sxs-lookup"><span data-stu-id="1ddd9-259">You are now ready to experiment with additional features of [Microsoft 365 for enterprise](https://www.microsoft.com/microsoft-365/enterprise).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="1ddd9-260">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="1ddd9-260">Next steps</span></span>

<span data-ttu-id="1ddd9-261">Découvrez les nouveaux ensembles de guides pour les tests de laboratoire :</span><span class="sxs-lookup"><span data-stu-id="1ddd9-261">Explore these additional sets of Test Lab Guides:</span></span>
  
- [<span data-ttu-id="1ddd9-262">Identité</span><span class="sxs-lookup"><span data-stu-id="1ddd9-262">Identity</span></span>](m365-enterprise-test-lab-guides.md#identity)
- [<span data-ttu-id="1ddd9-263">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="1ddd9-263">Mobile device management</span></span>](m365-enterprise-test-lab-guides.md#mobile-device-management)
- [<span data-ttu-id="1ddd9-264">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="1ddd9-264">Information protection</span></span>](m365-enterprise-test-lab-guides.md#information-protection)

## <a name="see-also"></a><span data-ttu-id="1ddd9-265">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ddd9-265">See also</span></span>

[<span data-ttu-id="1ddd9-266">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="1ddd9-266">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="1ddd9-267">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="1ddd9-267">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="1ddd9-268">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="1ddd9-268">Microsoft 365 for enterprise documentation</span></span>](/microsoft-365-enterprise/)