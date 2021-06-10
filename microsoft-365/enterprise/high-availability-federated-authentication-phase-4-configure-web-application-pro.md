---
title: Authentification fédérée haute disponibilité, phase 4 Configurer les proxies d’application web
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
ms.assetid: 1c903173-67cd-47da-86d9-d333972dda80
description: 'Résumé : Configurez les serveurs proxy d’application web pour votre authentification fédérée haute disponibilité Microsoft 365 dans Microsoft Azure.'
ms.openlocfilehash: 95d73d05f2eef087e606df14db180b24c69d5932
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50929071"
---
# <a name="high-availability-federated-authentication-phase-4-configure-web-application-proxies"></a><span data-ttu-id="2b792-103">Authentification fédérée haute disponibilité, phase 4 : Configurer les proxys d’application web</span><span class="sxs-lookup"><span data-stu-id="2b792-103">High availability federated authentication Phase 4: Configure web application proxies</span></span>

<span data-ttu-id="2b792-104">Dans cette phase de déploiement de la haute disponibilité pour l’authentification Microsoft 365 fédérée dans les services d’infrastructure Azure, vous créez un équilibreur de charge interne et deux serveurs AD FS.</span><span class="sxs-lookup"><span data-stu-id="2b792-104">In this phase of deploying high availability for Microsoft 365 federated authentication in Azure infrastructure services, you create an internal load balancer and two AD FS servers.</span></span>
  
<span data-ttu-id="2b792-105">Vous devez effectuer cette phase avant de passer à [la phase 5 : Configurer l’authentification fédérée pour Microsoft 365](high-availability-federated-authentication-phase-5-configure-federated-authentic.md).</span><span class="sxs-lookup"><span data-stu-id="2b792-105">You must complete this phase before moving on to [Phase 5: Configure federated authentication for Microsoft 365](high-availability-federated-authentication-phase-5-configure-federated-authentic.md).</span></span> <span data-ttu-id="2b792-106">Voir [Déployer l’authentification fédérée haute](deploy-high-availability-federated-authentication-for-microsoft-365-in-azure.md) disponibilité Microsoft 365 dans Azure pour toutes les phases.</span><span class="sxs-lookup"><span data-stu-id="2b792-106">See [Deploy high availability federated authentication for Microsoft 365 in Azure](deploy-high-availability-federated-authentication-for-microsoft-365-in-azure.md) for all of the phases.</span></span>
  
## <a name="create-the-internet-facing-load-balancer-in-azure"></a><span data-ttu-id="2b792-107">Créer l’équilibreur de charge connecté à Internet dans Azure</span><span class="sxs-lookup"><span data-stu-id="2b792-107">Create the Internet-facing load balancer in Azure</span></span>

<span data-ttu-id="2b792-108">Vous devez créer un équilibreur de charge connecté à Internet pour permettre à Azure de répartir équitablement le trafic d’authentification client entrant à partir d’Internet sur les deux serveurs proxy d’application web.</span><span class="sxs-lookup"><span data-stu-id="2b792-108">You must create an Internet-facing load balancer so that Azure distributes the incoming client authentication traffic from the Internet evenly among the two web application proxy servers.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2b792-109">[!REMARQUE] Les ensembles de commandes suivants utilisent la dernière version d'Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2b792-109">The following command sets use the latest version of Azure PowerShell.</span></span> <span data-ttu-id="2b792-110">Voir [La mise en Azure PowerShell](/powershell/azure/get-started-azureps).</span><span class="sxs-lookup"><span data-stu-id="2b792-110">See [Get started with Azure PowerShell](/powershell/azure/get-started-azureps).</span></span> 
  
<span data-ttu-id="2b792-111">Une fois que vous avez indiqué les valeurs d’emplacement et de groupe de ressources, exécutez le bloc obtenu à l’invite de commandes Azure PowerShell ou dans le PowerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="2b792-111">When you have supplied location and resource group values, run the resulting block at the Azure PowerShell command prompt or in the PowerShell ISE.</span></span>
  
> [!TIP]
> <span data-ttu-id="2b792-112">Pour générer des blocs de commandes PowerShell prêts à l’emploi en fonction de vos paramètres personnalisés, utilisez ce Microsoft Excel [de configuration.](https://github.com/MicrosoftDocs/OfficeDocs-Enterprise/raw/live/Enterprise/downloads/O365FedAuthInAzure_Config.xlsx)</span><span class="sxs-lookup"><span data-stu-id="2b792-112">To generate ready-to-run PowerShell command blocks based on your custom settings, use this [Microsoft Excel configuration workbook](https://github.com/MicrosoftDocs/OfficeDocs-Enterprise/raw/live/Enterprise/downloads/O365FedAuthInAzure_Config.xlsx).</span></span> 

```powershell
# Set up key variables
$locName="<your Azure location>"
$rgName="<Table R - Item 4 - Resource group name column>"

$publicIP=New-AzPublicIpAddress -ResourceGroupName $rgName -Name "WebProxyPublicIP" -Location $LocName -AllocationMethod "Static"
$frontendIP=New-AzLoadBalancerFrontendIpConfig -Name "WebAppProxyServers-LBFE" -PublicIpAddress $publicIP
$beAddressPool=New-AzLoadBalancerBackendAddressPoolConfig -Name "WebAppProxyServers-LBBE"
$healthProbe=New-AzLoadBalancerProbeConfig -Name "WebServersProbe" -Protocol "TCP" -Port 443 -IntervalInSeconds 15 -ProbeCount 2
$lbrule=New-AzLoadBalancerRuleConfig -Name "WebTraffic" -FrontendIpConfiguration $frontendIP -BackendAddressPool $beAddressPool -Probe $healthProbe -Protocol "TCP" -FrontendPort 443 -BackendPort 443
New-AzLoadBalancer -ResourceGroupName $rgName -Name "WebAppProxyServers" -Location $locName -LoadBalancingRule $lbrule -BackendAddressPool $beAddressPool -Probe $healthProbe -FrontendIpConfiguration $frontendIP
```

<span data-ttu-id="2b792-113">Pour afficher l’adresse IP publique affectée à votre équilibreur de charge connecté à Internet, exécutez ces commandes à l’invite de commande Azure PowerShell sur votre ordinateur local :</span><span class="sxs-lookup"><span data-stu-id="2b792-113">To display the public IP address assigned to your Internet-facing load balancer, run these commands at the Azure PowerShell command prompt on your local computer:</span></span>
  
```powershell
Write-Host (Get-AzPublicIpaddress -Name "WebProxyPublicIP" -ResourceGroup $rgName).IPAddress
```

## <a name="determine-your-federation-service-fqdn-and-create-dns-records"></a><span data-ttu-id="2b792-114">Déterminer le nom de domaine complet de votre service de fédération et créer des enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="2b792-114">Determine your federation service FQDN and create DNS records</span></span>

<span data-ttu-id="2b792-115">Vous devez déterminer le nom DNS pour identifier le nom de votre service de fédération sur Internet.</span><span class="sxs-lookup"><span data-stu-id="2b792-115">You need to determine the DNS name to identify your federation service name on the Internet.</span></span> <span data-ttu-id="2b792-116">Azure AD Connecter configurera Microsoft 365 avec ce nom à la phase 5, qui fera partie de l’URL que Microsoft 365 envoie aux clients connectés pour obtenir un jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2b792-116">Azure AD Connect will configure Microsoft 365 with this name in Phase 5, which will become part of the URL that Microsoft 365 sends to connecting clients to get a security token.</span></span> <span data-ttu-id="2b792-117">Ce nom est, par exemple, fs.contoso.com (fs signifie federation service : service de fédération).</span><span class="sxs-lookup"><span data-stu-id="2b792-117">An example is fs.contoso.com (fs stands for federation service).</span></span>
  
<span data-ttu-id="2b792-118">Une fois que le nom de domaine complet du service de fédération a été obtenu, créez un enregistrement DNS de domaine public A pour le nom de domaine complet pour le résoudre en adresse IP publique de l’équilibreur de charge Azure connecté à Internet.</span><span class="sxs-lookup"><span data-stu-id="2b792-118">Once you have your federation service FDQN, create a public DNS domain A record for the federation service FDQN that resolves to the public IP address of the Azure Internet-facing load balancer.</span></span>
  
|<span data-ttu-id="2b792-119">**Name**</span><span class="sxs-lookup"><span data-stu-id="2b792-119">**Name**</span></span>|<span data-ttu-id="2b792-120">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="2b792-120">**Type**</span></span>|<span data-ttu-id="2b792-121">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="2b792-121">**TTL**</span></span>|<span data-ttu-id="2b792-122">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="2b792-122">**Value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2b792-123">Nom de domaine complet du service de fédération</span><span class="sxs-lookup"><span data-stu-id="2b792-123">federation service FDQN</span></span>  <br/> |<span data-ttu-id="2b792-124">A</span><span class="sxs-lookup"><span data-stu-id="2b792-124">A</span></span>  <br/> |<span data-ttu-id="2b792-125">3600</span><span class="sxs-lookup"><span data-stu-id="2b792-125">3600</span></span>  <br/> |<span data-ttu-id="2b792-126">adresse IP publique de l’équilibreur de charge Azure connecté à Internet (affiché par la commande **Write-Host** dans la section précédente)</span><span class="sxs-lookup"><span data-stu-id="2b792-126">public IP address of the Azure Internet-facing load balancer (displayed by the **Write-Host** command in the previous section)</span></span> <br/> |
   
<span data-ttu-id="2b792-127">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="2b792-127">Here is an example:</span></span>
  
|<span data-ttu-id="2b792-128">**Name**</span><span class="sxs-lookup"><span data-stu-id="2b792-128">**Name**</span></span>|<span data-ttu-id="2b792-129">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="2b792-129">**Type**</span></span>|<span data-ttu-id="2b792-130">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="2b792-130">**TTL**</span></span>|<span data-ttu-id="2b792-131">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="2b792-131">**Value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2b792-132">fs.contoso.com</span><span class="sxs-lookup"><span data-stu-id="2b792-132">fs.contoso.com</span></span>  <br/> |<span data-ttu-id="2b792-133">A</span><span class="sxs-lookup"><span data-stu-id="2b792-133">A</span></span>  <br/> |<span data-ttu-id="2b792-134">3600</span><span class="sxs-lookup"><span data-stu-id="2b792-134">3600</span></span>  <br/> |<span data-ttu-id="2b792-135">131.107.249.117</span><span class="sxs-lookup"><span data-stu-id="2b792-135">131.107.249.117</span></span>  <br/> |
   
<span data-ttu-id="2b792-136">Ensuite, ajoutez un enregistrement d’adresse DNS à l’espace de noms DNS privé de votre organisation pour résoudre le nom de domaine complet de votre service de fédération en adresse IP privée affectée à l’équilibreur de charge interne pour les serveurs AD FS (tableau I, élément 4, colonne Valeur).</span><span class="sxs-lookup"><span data-stu-id="2b792-136">Next, add a DNS address record to your organization's private DNS namespace that resolves your federation service FQDN to the private IP address assigned to the internal load balancer for the AD FS servers (Table I, item 4, Value column).</span></span>
  
## <a name="create-the-web-application-proxy-server-virtual-machines-in-azure"></a><span data-ttu-id="2b792-137">Créer les machines virtuelles des serveurs proxy d’application web dans Azure</span><span class="sxs-lookup"><span data-stu-id="2b792-137">Create the web application proxy server virtual machines in Azure</span></span>

<span data-ttu-id="2b792-138">Utilisez le bloc de commandes Azure PowerShell suivant pour créer les machines virtuelles pour les deux serveurs proxy d’application web. </span><span class="sxs-lookup"><span data-stu-id="2b792-138">Use the following block of Azure PowerShell commands to create the virtual machines for the two web application proxy servers.</span></span> 
  
<span data-ttu-id="2b792-139">Notez que l’ensemble de commandes Azure PowerShell suivant utilise des valeurs provenant des tableaux suivants :</span><span class="sxs-lookup"><span data-stu-id="2b792-139">Note that the following Azure PowerShell command sets use values from the following tables:</span></span>
  
- <span data-ttu-id="2b792-140">Tableau M, pour vos machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="2b792-140">Table M, for your virtual machines</span></span>
    
- <span data-ttu-id="2b792-141">Tableau R, pour vos groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="2b792-141">Table R, for your resource groups</span></span>
    
- <span data-ttu-id="2b792-142">Tableau V, pour vos paramètres de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="2b792-142">Table V, for your virtual network settings</span></span>
    
- <span data-ttu-id="2b792-143">Tableau S, pour vos sous-réseaux</span><span class="sxs-lookup"><span data-stu-id="2b792-143">Table S, for your subnets</span></span>
    
- <span data-ttu-id="2b792-144">Tableau I, pour vos adresses IP statiques</span><span class="sxs-lookup"><span data-stu-id="2b792-144">Table I, for your static IP addresses</span></span>
    
- <span data-ttu-id="2b792-145">Tableau A, pour vos groupes à haute disponibilité</span><span class="sxs-lookup"><span data-stu-id="2b792-145">Table A, for your availability sets</span></span>
    
<span data-ttu-id="2b792-146">Rappelez-vous que vous avez défini le tableau M à la [phase 2](high-availability-federated-authentication-phase-2-configure-domain-controllers.md) : Configurer les contrôleurs de domaine et les tables R, V, S, I et A dans [la phase 1 :](high-availability-federated-authentication-phase-1-configure-azure.md)Configurer Azure .</span><span class="sxs-lookup"><span data-stu-id="2b792-146">Recall that you defined Table M in [Phase 2: Configure domain controllers](high-availability-federated-authentication-phase-2-configure-domain-controllers.md) and Tables R, V, S, I, and A in [Phase 1: Configure Azure](high-availability-federated-authentication-phase-1-configure-azure.md).</span></span>
  
<span data-ttu-id="2b792-147">Lorsque vous avez fourni toutes les valeurs correctes, exécutez le bloc obtenu à l’invite de commandes Azure PowerShell ou dans le PowerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="2b792-147">When you have supplied all the proper values, run the resulting block at the Azure PowerShell command prompt or in the PowerShell ISE.</span></span>
  
```powershell
# Set up variables common to both virtual machines
$locName="<your Azure location>"
$vnetName="<Table V - Item 1 - Value column>"
$subnetName="<Table R - Item 3 - Subnet name column>"
$avName="<Table A - Item 3 - Availability set name column>"
$rgNameTier="<Table R - Item 3 - Resource group name column>"
$rgNameInfra="<Table R - Item 4 - Resource group name column>"

$rgName=$rgNameInfra
$vnet=Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgName
$subnet=Get-AzVirtualNetworkSubnetConfig -VirtualNetwork $vnet -Name $subnetName
$backendSubnet=Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet
$webLB=Get-AzLoadBalancer -ResourceGroupName $rgName -Name "WebAppProxyServers"

$rgName=$rgNameTier
$avSet=Get-AzAvailabilitySet -Name $avName -ResourceGroupName $rgName

# Create the first web application proxy server virtual machine
$vmName="<Table M - Item 6 - Virtual machine name column>"
$vmSize="<Table M - Item 6 - Minimum size column>"
$staticIP="<Table I - Item 7 - Value column>"
$diskStorageType="<Table M - Item 6 - Storage type column>"

$nic=New-AzNetworkInterface -Name ($vmName +"-NIC") -ResourceGroupName $rgName -Location $locName -Subnet $backendSubnet -LoadBalancerBackendAddressPool $webLB.BackendAddressPools[0] -PrivateIpAddress $staticIP
$vm=New-AzVMConfig -VMName $vmName -VMSize $vmSize -AvailabilitySetId $avset.Id

$cred=Get-Credential -Message "Type the name and password of the local administrator account for the first web application proxy server." 
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName $vmName -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name ($vmName +"-OS") -DiskSizeInGB 128 -CreateOption FromImage -StorageAccountType $diskStorageType
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm

# Create the second web application proxy virtual machine
$vmName="<Table M - Item 7 - Virtual machine name column>"
$vmSize="<Table M - Item 7 - Minimum size column>"
$staticIP="<Table I - Item 8 - Value column>"
$diskStorageType="<Table M - Item 7 - Storage type column>"

$nic=New-AzNetworkInterface -Name ($vmName +"-NIC") -ResourceGroupName $rgName -Location $locName  -Subnet $backendSubnet -LoadBalancerBackendAddressPool $webLB.BackendAddressPools[0] -PrivateIpAddress $staticIP
$vm=New-AzVMConfig -VMName $vmName -VMSize $vmSize -AvailabilitySetId $avset.Id

$cred=Get-Credential -Message "Type the name and password of the local administrator account for the second web application proxy server." 
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName $vmName -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name ($vmName +"-OS") -DiskSizeInGB 128 -CreateOption FromImage -StorageAccountType $diskStorageType
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm
```

> [!NOTE]
> <span data-ttu-id="2b792-p104">Étant donné que ces machines virtuelles sont pour une application intranet, aucune adresse IP publique ni étiquette de nom de domaine DNS ne leur est affectée et elles ne sont pas connectées à Internet. Toutefois, vous ne pouvez pas vous y connecter à partir du portail Azure. L’option **Se connecter** n’est pas disponible lorsque vous affichez les propriétés de la machine virtuelle. Utilisez l’accessoire de connexion Bureau à distance ou un autre outil de Bureau à distance pour vous connecter à la machine virtuelle à l’aide de son adresse IP privée ou de son nom DNS intranet, ainsi que les informations d’identification du compte Administrateur local.</span><span class="sxs-lookup"><span data-stu-id="2b792-p104">Because these virtual machines are for an intranet application, they are not assigned a public IP address or a DNS domain name label and exposed to the Internet. However, this also means that you cannot connect to them from the Azure portal. The **Connect** option is unavailable when you view the properties of the virtual machine. Use the Remote Desktop Connection accessory or another Remote Desktop tool to connect to the virtual machine using its private IP address or intranet DNS name and the credentials of the local administrator account.</span></span>
  
<span data-ttu-id="2b792-152">Lorsque cette phase est terminée, voici la configuration résultante, avec les noms d’ordinateur de l’espace réservé.</span><span class="sxs-lookup"><span data-stu-id="2b792-152">Here is the configuration resulting from the successful completion of this phase, with placeholder computer names.</span></span>
  
<span data-ttu-id="2b792-153">**Phase 4 : L’équilibreur de charge connecté à Internet et les serveurs proxy d’application web de votre infrastructure d’authentification fédérée haute disponibilité dans Azure**</span><span class="sxs-lookup"><span data-stu-id="2b792-153">**Phase 4: The Internet-facing load balancer and web application proxy servers for your high availability federated authentication infrastructure in Azure**</span></span>

![Phase 4 de l’infrastructure d’authentification Microsoft 365 haute disponibilité dans Azure avec les serveurs proxy d’application web](../media/7e03183f-3b3b-4cbe-9028-89cc3f195a63.png)
  
## <a name="next-step"></a><span data-ttu-id="2b792-155">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="2b792-155">Next step</span></span>

<span data-ttu-id="2b792-156">Utilisez [la phase 5 : Configurer l’authentification fédérée pour Microsoft 365](high-availability-federated-authentication-phase-5-configure-federated-authentic.md) pour continuer à configurer cette charge de travail.</span><span class="sxs-lookup"><span data-stu-id="2b792-156">Use [Phase 5: Configure federated authentication for Microsoft 365](high-availability-federated-authentication-phase-5-configure-federated-authentic.md) to continue configuring this workload.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2b792-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b792-157">See Also</span></span>

[<span data-ttu-id="2b792-158">Déployer une authentification fédérée haute disponibilité pour Microsoft 365 dans Azure</span><span class="sxs-lookup"><span data-stu-id="2b792-158">Deploy high availability federated authentication for Microsoft 365 in Azure</span></span>](deploy-high-availability-federated-authentication-for-microsoft-365-in-azure.md)
  
[<span data-ttu-id="2b792-159">Identité fédérée pour votre environnement Microsoft 365 dev/test</span><span class="sxs-lookup"><span data-stu-id="2b792-159">Federated identity for your Microsoft 365 dev/test environment</span></span>](federated-identity-for-your-microsoft-365-dev-test-environment.md)
  
[<span data-ttu-id="2b792-160">Centre de solutions et d'architecture Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2b792-160">Microsoft 365 solution and architecture center</span></span>](../solutions/index.yml)