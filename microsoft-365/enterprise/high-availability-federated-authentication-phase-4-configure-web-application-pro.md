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
# <a name="high-availability-federated-authentication-phase-4-configure-web-application-proxies"></a>Authentification fédérée haute disponibilité, phase 4 : Configurer les proxys d’application web

Dans cette phase de déploiement de la haute disponibilité pour l’authentification Microsoft 365 fédérée dans les services d’infrastructure Azure, vous créez un équilibreur de charge interne et deux serveurs AD FS.
  
Vous devez effectuer cette phase avant de passer à [la phase 5 : Configurer l’authentification fédérée pour Microsoft 365](high-availability-federated-authentication-phase-5-configure-federated-authentic.md). Voir [Déployer l’authentification fédérée haute](deploy-high-availability-federated-authentication-for-microsoft-365-in-azure.md) disponibilité Microsoft 365 dans Azure pour toutes les phases.
  
## <a name="create-the-internet-facing-load-balancer-in-azure"></a>Créer l’équilibreur de charge connecté à Internet dans Azure

Vous devez créer un équilibreur de charge connecté à Internet pour permettre à Azure de répartir équitablement le trafic d’authentification client entrant à partir d’Internet sur les deux serveurs proxy d’application web.
  
> [!NOTE]
> [!REMARQUE] Les ensembles de commandes suivants utilisent la dernière version d'Azure PowerShell. Voir [La mise en Azure PowerShell](/powershell/azure/get-started-azureps). 
  
Une fois que vous avez indiqué les valeurs d’emplacement et de groupe de ressources, exécutez le bloc obtenu à l’invite de commandes Azure PowerShell ou dans le PowerShell ISE.
  
> [!TIP]
> Pour générer des blocs de commandes PowerShell prêts à l’emploi en fonction de vos paramètres personnalisés, utilisez ce Microsoft Excel [de configuration.](https://github.com/MicrosoftDocs/OfficeDocs-Enterprise/raw/live/Enterprise/downloads/O365FedAuthInAzure_Config.xlsx) 

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

Pour afficher l’adresse IP publique affectée à votre équilibreur de charge connecté à Internet, exécutez ces commandes à l’invite de commande Azure PowerShell sur votre ordinateur local :
  
```powershell
Write-Host (Get-AzPublicIpaddress -Name "WebProxyPublicIP" -ResourceGroup $rgName).IPAddress
```

## <a name="determine-your-federation-service-fqdn-and-create-dns-records"></a>Déterminer le nom de domaine complet de votre service de fédération et créer des enregistrements DNS

Vous devez déterminer le nom DNS pour identifier le nom de votre service de fédération sur Internet. Azure AD Connecter configurera Microsoft 365 avec ce nom à la phase 5, qui fera partie de l’URL que Microsoft 365 envoie aux clients connectés pour obtenir un jeton de sécurité. Ce nom est, par exemple, fs.contoso.com (fs signifie federation service : service de fédération).
  
Une fois que le nom de domaine complet du service de fédération a été obtenu, créez un enregistrement DNS de domaine public A pour le nom de domaine complet pour le résoudre en adresse IP publique de l’équilibreur de charge Azure connecté à Internet.
  
|**Name**|**Type (Type)**|**TTL (Durée de vie)**|**Value (Valeur)**|
|:-----|:-----|:-----|:-----|
|Nom de domaine complet du service de fédération  <br/> |A  <br/> |3600  <br/> |adresse IP publique de l’équilibreur de charge Azure connecté à Internet (affiché par la commande **Write-Host** dans la section précédente) <br/> |
   
Voici un exemple :
  
|**Name**|**Type (Type)**|**TTL (Durée de vie)**|**Value (Valeur)**|
|:-----|:-----|:-----|:-----|
|fs.contoso.com  <br/> |A  <br/> |3600  <br/> |131.107.249.117  <br/> |
   
Ensuite, ajoutez un enregistrement d’adresse DNS à l’espace de noms DNS privé de votre organisation pour résoudre le nom de domaine complet de votre service de fédération en adresse IP privée affectée à l’équilibreur de charge interne pour les serveurs AD FS (tableau I, élément 4, colonne Valeur).
  
## <a name="create-the-web-application-proxy-server-virtual-machines-in-azure"></a>Créer les machines virtuelles des serveurs proxy d’application web dans Azure

Utilisez le bloc de commandes Azure PowerShell suivant pour créer les machines virtuelles pour les deux serveurs proxy d’application web.  
  
Notez que l’ensemble de commandes Azure PowerShell suivant utilise des valeurs provenant des tableaux suivants :
  
- Tableau M, pour vos machines virtuelles
    
- Tableau R, pour vos groupes de ressources
    
- Tableau V, pour vos paramètres de réseau virtuel
    
- Tableau S, pour vos sous-réseaux
    
- Tableau I, pour vos adresses IP statiques
    
- Tableau A, pour vos groupes à haute disponibilité
    
Rappelez-vous que vous avez défini le tableau M à la [phase 2](high-availability-federated-authentication-phase-2-configure-domain-controllers.md) : Configurer les contrôleurs de domaine et les tables R, V, S, I et A dans [la phase 1 :](high-availability-federated-authentication-phase-1-configure-azure.md)Configurer Azure .
  
Lorsque vous avez fourni toutes les valeurs correctes, exécutez le bloc obtenu à l’invite de commandes Azure PowerShell ou dans le PowerShell ISE.
  
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
> Étant donné que ces machines virtuelles sont pour une application intranet, aucune adresse IP publique ni étiquette de nom de domaine DNS ne leur est affectée et elles ne sont pas connectées à Internet. Toutefois, vous ne pouvez pas vous y connecter à partir du portail Azure. L’option **Se connecter** n’est pas disponible lorsque vous affichez les propriétés de la machine virtuelle. Utilisez l’accessoire de connexion Bureau à distance ou un autre outil de Bureau à distance pour vous connecter à la machine virtuelle à l’aide de son adresse IP privée ou de son nom DNS intranet, ainsi que les informations d’identification du compte Administrateur local.
  
Lorsque cette phase est terminée, voici la configuration résultante, avec les noms d’ordinateur de l’espace réservé.
  
**Phase 4 : L’équilibreur de charge connecté à Internet et les serveurs proxy d’application web de votre infrastructure d’authentification fédérée haute disponibilité dans Azure**

![Phase 4 de l’infrastructure d’authentification Microsoft 365 haute disponibilité dans Azure avec les serveurs proxy d’application web](../media/7e03183f-3b3b-4cbe-9028-89cc3f195a63.png)
  
## <a name="next-step"></a>Étape suivante

Utilisez [la phase 5 : Configurer l’authentification fédérée pour Microsoft 365](high-availability-federated-authentication-phase-5-configure-federated-authentic.md) pour continuer à configurer cette charge de travail.
  
## <a name="see-also"></a>Voir aussi

[Déployer une authentification fédérée haute disponibilité pour Microsoft 365 dans Azure](deploy-high-availability-federated-authentication-for-microsoft-365-in-azure.md)
  
[Identité fédérée pour votre environnement Microsoft 365 dev/test](federated-identity-for-your-microsoft-365-dev-test-environment.md)
  
[Centre de solutions et d'architecture Microsoft 365](../solutions/index.yml)