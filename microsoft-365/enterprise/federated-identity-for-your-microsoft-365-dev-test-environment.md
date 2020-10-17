---
title: Identité fédérée pour votre environnement de test Microsoft 365
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 05/26/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- TLG
- Ent_TLGs
ms.assetid: 65a6d687-a16a-4415-9fd5-011ba9c5fd80
description: 'Résumé : Configurez l’authentification fédérée pour votre environnement de test Microsoft 365.'
ms.openlocfilehash: 0fb8c55f5b7291cdc6bcec636981a9d31015e723
ms.sourcegitcommit: 53ff1fe6d6143b0bf011031eea9b85dc01ae4f74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "48487683"
---
# <a name="federated-identity-for-your-microsoft-365-test-environment"></a><span data-ttu-id="bd4bf-103">Identité fédérée pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bd4bf-103">Federated identity for your Microsoft 365 test environment</span></span>

<span data-ttu-id="bd4bf-104">*Ce guide de laboratoire de test peut être utilisé pour les environnements de test Microsoft 365 pour les environnements de test d’entreprise et Office 365.*</span><span class="sxs-lookup"><span data-stu-id="bd4bf-104">*This Test Lab Guide can be used for both Microsoft 365 for enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="bd4bf-p101">Microsoft 365 prend en charge l’identité fédérée. Cela signifie qu’au lieu d’effectuer la validation des informations d’identification, Microsoft 365 renvoie l’utilisateur qui se connecte à un serveur d’authentification fédérée approuvé par Microsoft 365. Si les informations d’identification de l’utilisateur sont correctes, le serveur d’authentification fédérée émet un jeton de sécurité que le client envoie ensuite à Microsoft 365 comme preuve d’authentification. L’identité fédérée autorise le déchargement et la montée en charge de l’authentification pour un abonnement Microsoft 365, ainsi que l’authentification avancée et les scénarios de sécurité.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-p101">Microsoft 365 supports federated identity. This means that instead of performing the validation of credentials itself, Microsoft 365 refers the connecting user to a federated authentication server that Microsoft 365 trusts. If the user's credentials are correct, the federated authentication server issues a security token that the client then sends to Microsoft 365 as proof of authentication. Federated identity allows for the offloading and scaling up of authentication for a Microsoft 365 subscription and advanced authentication and security scenarios.</span></span>
  
<span data-ttu-id="bd4bf-109">Cet article explique comment configurer l’authentification fédérée pour votre environnement de test Microsoft 365, en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-109">This article describes how to configure federated authentication for your Microsoft 365 test environment, resulting in the following:</span></span>

![L’authentification fédérée pour l’environnement de test Microsoft 365](../media/federated-identity-for-your-microsoft-365-dev-test-environment/federated-tlg-phase3.png)
  
<span data-ttu-id="bd4bf-111">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="bd4bf-111">This configuration consists of:</span></span>
  
- <span data-ttu-id="bd4bf-112">Un abonnement à la version d’évaluation ou de production de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-112">A Microsoft 365 E5 trial or production subscription.</span></span>
    
- <span data-ttu-id="bd4bf-113">Un intranet d’organisation simplifié connecté à Internet, composé de cinq machines virtuelles sur un sous-réseau d’un réseau virtuel Azure (DC1, APP1, CLIENT1, ADFS1 et PROXY1).</span><span class="sxs-lookup"><span data-stu-id="bd4bf-113">A simplified organization intranet connected to the internet, consisting of five virtual machines on a subnet of an Azure virtual network (DC1, APP1, CLIENT1, ADFS1, and PROXY1).</span></span> <span data-ttu-id="bd4bf-114">Azure AD Connect s’exécute sur APP1 pour synchroniser la liste des comptes dans le domaine des services de domaine Active Directory avec Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-114">Azure AD Connect runs on APP1 to synchronize the list of accounts in the Active Directory Domain Services domain to Microsoft 365.</span></span> <span data-ttu-id="bd4bf-115">PROXY1 reçoit les demandes d’authentification entrantes.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-115">PROXY1 receives the incoming authentication requests.</span></span> <span data-ttu-id="bd4bf-116">ADFS1 valide les informations d’identification avec DC1 et émet des jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-116">ADFS1 validates credentials with DC1 and issues security tokens.</span></span>
    
<span data-ttu-id="bd4bf-117">La configuration de cet environnement de test implique cinq phases :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-117">Setting up this test environment involves five phases:</span></span>
- [<span data-ttu-id="bd4bf-118">Étape 1 : Configuration de la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bd4bf-118">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>](#phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment)
- [<span data-ttu-id="bd4bf-119">Phase 2 : Création du serveur AD FS</span><span class="sxs-lookup"><span data-stu-id="bd4bf-119">Phase 2: Create the AD FS server</span></span>](#phase-2-create-the-ad-fs-server)
- [<span data-ttu-id="bd4bf-120">Phase 3 : création du serveur proxy web (PROXY1)</span><span class="sxs-lookup"><span data-stu-id="bd4bf-120">Phase 3: Create the web proxy server</span></span>](#phase-3-create-the-web-proxy-server)
- [<span data-ttu-id="bd4bf-121">Phase 4 : création d’un certificat auto-signé et configuration d’ADFS1 et de PROXY1</span><span class="sxs-lookup"><span data-stu-id="bd4bf-121">Phase 4: Create a self-signed certificate and configure ADFS1 and PROXY1</span></span>](#phase-4-create-a-self-signed-certificate-and-configure-adfs1-and-proxy1)
- [<span data-ttu-id="bd4bf-122">Phase 5: configuration de Microsoft 365 pour l’identité fédérée</span><span class="sxs-lookup"><span data-stu-id="bd4bf-122">Phase 5: Configure Microsoft 365 for federated identity</span></span>](#phase-5-configure-microsoft-365-for-federated-identity)
    
> [!NOTE]
> <span data-ttu-id="bd4bf-123">Vous ne pouvez pas configurer cet environnement de test avec un abonnement d’évaluation Azure.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-123">You can't configure this test environment with an Azure Trial subscription.</span></span>
  
## <a name="phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment"></a><span data-ttu-id="bd4bf-124">Étape 1 : Configuration de la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bd4bf-124">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="bd4bf-125">Suivez les instructions de la [synchronisation de hachage de mot de passe pour Microsoft 365](password-hash-sync-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="bd4bf-125">Follow the instructions in [password hash synchronization for Microsoft 365](password-hash-sync-m365-ent-test-environment.md).</span></span> <span data-ttu-id="bd4bf-126">La configuration obtenue se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-126">Your resulting configuration looks like this:</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](../media/federated-identity-for-your-microsoft-365-dev-test-environment/federated-tlg-phase1.png)
  
<span data-ttu-id="bd4bf-128">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="bd4bf-128">This configuration consists of:</span></span>
  
- <span data-ttu-id="bd4bf-129">Un abonnement d’évaluation ou payant Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-129">A Microsoft 365 E5 trial or paid subscriptions.</span></span>
- <span data-ttu-id="bd4bf-130">Un intranet d’organisation simplifié connecté à Internet, constitué des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-130">A simplified organization intranet connected to the internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> <span data-ttu-id="bd4bf-131">Azure AD Connect s’exécute sur APP1 pour synchroniser régulièrement le domaine des services de domaine Active Directory (AD DS) TESTLAB vers le client Azure AD de vos abonnements Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-131">Azure AD Connect runs on APP1 to synchronize the TESTLAB Active Directory Domain Services (AD DS) domain to the Azure AD tenant of your Microsoft 365 subscriptions periodically.</span></span>

## <a name="phase-2-create-the-ad-fs-server"></a><span data-ttu-id="bd4bf-132">Phase 2 : Création du serveur AD FS</span><span class="sxs-lookup"><span data-stu-id="bd4bf-132">Phase 2: Create the AD FS server</span></span>

<span data-ttu-id="bd4bf-133">Un serveur AD FS fournit une authentification fédérée entre Microsoft 365 et les comptes dans le domaine corp.contoso.com hébergé sur DC1.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-133">An AD FS server provides federated authentication between Microsoft 365 and the accounts in the corp.contoso.com domain hosted on DC1.</span></span>
  
<span data-ttu-id="bd4bf-134">Pour créer une machine virtuelle Azure pour ADFS1, indiquez le nom de votre abonnement et de votre groupe de ressources, ainsi que l’emplacement Azure de votre configuration de base, puis exécutez ces commandes à l’invite de commandes Azure PowerShell sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-134">To create an Azure virtual machine for ADFS1, fill in the name of your subscription and the resource group and Azure location for your Base Configuration, and then run these commands at the Azure PowerShell command prompt on your local computer.</span></span>
  
```powershell
$subscrName="<your Azure subscription name>"
$rgName="<the resource group name of your Base Configuration>"
$vnetName="TlgBaseConfig-01-VNET"
# NOTE: If you built your simulated intranet with Azure PowerShell, comment the previous line with a "#" and remove the "#" from the next line.
#$vnetName="TestLab"
Connect-AzAccount
Select-AzSubscription -SubscriptionName $subscrName
$staticIP="10.0.0.100"
$locName=(Get-AzResourceGroup -Name $rgName).Location
$vnet=Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgName
$pip = New-AzPublicIpAddress -Name ADFS1-PIP -ResourceGroupName $rgName -Location $locName -AllocationMethod Dynamic
$nic = New-AzNetworkInterface -Name ADFS1-NIC -ResourceGroupName $rgName -Location $locName -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $pip.Id -PrivateIpAddress $staticIP
$vm=New-AzVMConfig -VMName ADFS1 -VMSize Standard_D2_v2
$cred=Get-Credential -Message "Type the name and password of the local administrator account for ADFS1."
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName ADFS1 -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name "ADFS-OS" -DiskSizeInGB 128 -CreateOption FromImage -StorageAccountType "Standard_LRS"
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm
```

<span data-ttu-id="bd4bf-135">Ensuite, utilisez le [portail Azure](https://portal.azure.com) pour vous connecter à la machine virtuelle ADFS1 à l’aide du nom de compte d’administrateur local ADFS1 et de votre mot de passe, puis ouvrez une invite de commande Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-135">Next, use the [Azure portal](https://portal.azure.com) to connect to the ADFS1 virtual machine using the ADFS1 local administrator account name and password, and then open a Windows PowerShell command prompt.</span></span>
  
<span data-ttu-id="bd4bf-136">Pour vérifier la résolution du nom et la communication réseau entre ADFS1 et DC1, exécutez la commande **ping dc1.corp.contoso.com** et vérifiez qu’il y a quatre réponses.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-136">To check name resolution and network communication between ADFS1 and DC1, run the **ping dc1.corp.contoso.com** command and check that there are four replies.</span></span>
  
<span data-ttu-id="bd4bf-137">Ensuite, associez la machine virtuelle ADFS1 au domaine CORP avec ces commandes à l’invite Windows PowerShell sur ADFS1.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-137">Next, join the ADFS1 virtual machine to the CORP domain with these commands at the Windows PowerShell prompt on ADFS1.</span></span>
  
```powershell
$cred=Get-Credential -UserName "CORP\User1" -Message "Type the User1 account password."
Add-Computer -DomainName corp.contoso.com -Credential $cred
Restart-Computer
```

<span data-ttu-id="bd4bf-138">La configuration obtenue se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-138">Your resulting configuration looks like this:</span></span>
  
![Le serveur AD FS ajouté à la synchronisation d’annuaire pour l’environnement de test Microsoft 365](../media/federated-identity-for-your-microsoft-365-dev-test-environment/federated-tlg-phase2.png)
  
## <a name="phase-3-create-the-web-proxy-server"></a><span data-ttu-id="bd4bf-140">Phase 3 : création du serveur proxy web (PROXY1)</span><span class="sxs-lookup"><span data-stu-id="bd4bf-140">Phase 3: Create the web proxy server</span></span>

<span data-ttu-id="bd4bf-141">PROXY1 permet le traitement proxy des messages d’authentification entre les utilisateurs tentant de s’authentifier et ADFS1.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-141">PROXY1 provides proxying of authentication messages between users trying to authenticate and ADFS1.</span></span>
  
<span data-ttu-id="bd4bf-142">Pour créer une machine virtuelle Azure pour PROXY1, indiquez le nom de votre groupe de ressources et l’emplacement Azure, puis exécutez ces commandes à l’invite de commande Azure PowerShell sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-142">To create an Azure virtual machine for PROXY1, fill in the name of your resource group and Azure location, and then run these commands at the Azure PowerShell command prompt on your local computer.</span></span>
  
```powershell
$rgName="<the resource group name of your Base Configuration>"
$vnetName="TlgBaseConfig-01-VNET"
# NOTE: If you built your simulated intranet with Azure PowerShell, comment the previous line with a "#" and remove the "#" from the next line.
#$vnetName="TestLab"
$staticIP="10.0.0.101"
$locName=(Get-AzResourceGroup -Name $rgName).Location
$vnet=Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgName
$pip = New-AzPublicIpAddress -Name PROXY1-PIP -ResourceGroupName $rgName -Location $locName -AllocationMethod Static
$nic = New-AzNetworkInterface -Name PROXY1-NIC -ResourceGroupName $rgName -Location $locName -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $pip.Id -PrivateIpAddress $staticIP
$vm=New-AzVMConfig -VMName PROXY1 -VMSize Standard_D2_v2
$cred=Get-Credential -Message "Type the name and password of the local administrator account for PROXY1."
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName PROXY1 -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name "PROXY1-OS" -DiskSizeInGB 128 -CreateOption FromImage -StorageAccountType "Standard_LRS"
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm
```

> [!NOTE]
> <span data-ttu-id="bd4bf-143">Une adresse IP publique statique est affectée à PROXY1, car vous créez un enregistrement DNS public qui pointe vers celle-ci et elle ne doit pas être modifiée lorsque vous redémarrez la machine virtuelle PROXY1.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-143">PROXY1 is assigned a static public IP address because you will create a public DNS record that points to it and it must not change when you restart the PROXY1 virtual machine.</span></span>
  
<span data-ttu-id="bd4bf-144">Ensuite, ajoutez une règle au groupe de sécurité réseau pour le sous-réseau CorpNet afin d’autoriser le trafic entrant non sollicité provenant d’Internet vers l’adresse IP privée PROXY1's et le port TCP 443.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-144">Next, add a rule to the network security group for the CorpNet subnet to allow unsolicited inbound traffic from the internet to PROXY1's private IP address and TCP port 443.</span></span> <span data-ttu-id="bd4bf-145">Exécutez ces commandes dans l’invite de commande Azure PowerShell sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-145">Run these commands at the Azure PowerShell command prompt on your local computer.</span></span>
  
```powershell
$rgName="<the resource group name of your Base Configuration>"
Get-AzNetworkSecurityGroup -Name CorpNet -ResourceGroupName $rgName | Add-AzNetworkSecurityRuleConfig -Name "HTTPS-to-PROXY1" -Description "Allow TCP 443 to PROXY1" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 101 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "10.0.0.101" -DestinationPortRange "443" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="bd4bf-146">Ensuite, utilisez le [portail Azure](https://portal.azure.com) pour vous connecter à la machine virtuelle PROXY1 à l’aide du nom de compte d’administrateur local PROXY1 et de votre mot de passe, puis ouvrez une invite de commande Windows PowerShell sur PROXY1.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-146">Next, use the [Azure portal](https://portal.azure.com) to connect to the PROXY1 virtual machine using the PROXY1 local administrator account name and password, and then open a Windows PowerShell command prompt on PROXY1.</span></span>
  
<span data-ttu-id="bd4bf-147">Pour vérifier la résolution du nom et la communication réseau entre PROXY1 et DC1, exécutez la commande **ping dc1.corp.contoso.com** et vérifiez qu’il y a quatre réponses.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-147">To check name resolution and network communication between PROXY1 and DC1, run the **ping dc1.corp.contoso.com** command and check that there are four replies.</span></span>
  
<span data-ttu-id="bd4bf-148">Ensuite, associez la machine virtuelle PROXY1 au domaine CORP avec ces commandes à l’invite Windows PowerShell sur PROXY1.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-148">Next, join the PROXY1 virtual machine to the CORP domain with these commands at the Windows PowerShell prompt on PROXY1.</span></span>
  
```powershell
$cred=Get-Credential -UserName "CORP\User1" -Message "Type the User1 account password."
Add-Computer -DomainName corp.contoso.com -Credential $cred
Restart-Computer
```

<span data-ttu-id="bd4bf-149">Affichez l’adresse IP publique de PROXY1 avec ces commandes Azure PowerShell sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-149">Display the public IP address of PROXY1 with these Azure PowerShell commands on your local computer.</span></span>
  
```powershell
Write-Host (Get-AzPublicIpaddress -Name "PROXY1-PIP" -ResourceGroup $rgName).IPAddress
```

<span data-ttu-id="bd4bf-p106">Ensuite, utilisez votre fournisseur DNS public et créez un enregistrement A DNS public pour **fs.testlab.**\<*your DNS domain name*> qui renvoie l’adresse IP affichée par la commande **Write-Host**. **fs.testlab.**\<*your DNS domain name*> est désigné ci-après en tant que *nom de domaine complet du service FS (Federation Service)*.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-p106">Next, work with your public DNS provider and create a new public DNS A record for **fs.testlab.**\<*your DNS domain name*> that resolves to the IP address displayed by the **Write-Host** command. The **fs.testlab.**\<*your DNS domain name*> is hereafter referred to as the  *federation service FQDN*.</span></span>
  
<span data-ttu-id="bd4bf-154">Ensuite, utilisez le [portail Azure](https://portal.azure.com) pour vous connecter à la machine virtuelle DC1 à l’aide des informations d’identification de CORP\\User1, puis exécutez les commandes suivantes à une invite de commande Windows PowerShell de niveau administrateur :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-154">Next, use the [Azure portal](https://portal.azure.com) to connect to the DC1 virtual machine using the CORP\\User1 credentials, and then run the following commands at an administrator-level Windows PowerShell command prompt:</span></span>
  
```powershell
Add-DnsServerPrimaryZone -Name corp.contoso.com -ZoneFile corp.contoso.com.dns
Add-DnsServerResourceRecordA -Name "fs" -ZoneName corp.contoso.com -AllowUpdateAny -IPv4Address "10.0.0.100" -TimeToLive 01:00:00
```
<span data-ttu-id="bd4bf-155">Ces commandes créent un enregistrement DNS A interne de sorte que les machines virtuelles sur le réseau virtuel Azure puissent résoudre le nom de domaine complet du service de Fédération interne en adresse IP privée ADFS1's.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-155">These commands create an internal DNS A record so that virtual machines on the Azure virtual network can resolve the internal federation service FQDN to ADFS1's private IP address.</span></span>
  
<span data-ttu-id="bd4bf-156">La configuration obtenue se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-156">Your resulting configuration looks like this:</span></span>
  
![Le serveur proxy d’application web ajouté à la synchronisation d’annuaire pour l’environnement de test Microsoft 365](../media/federated-identity-for-your-microsoft-365-dev-test-environment/federated-tlg-phase3.png)
  
## <a name="phase-4-create-a-self-signed-certificate-and-configure-adfs1-and-proxy1"></a><span data-ttu-id="bd4bf-158">Phase 4 : création d’un certificat auto-signé et configuration d’ADFS1 et de PROXY1</span><span class="sxs-lookup"><span data-stu-id="bd4bf-158">Phase 4: Create a self-signed certificate and configure ADFS1 and PROXY1</span></span>

<span data-ttu-id="bd4bf-159">Au cours de cette phase, vous créez un certificat numérique auto-signé pour votre nom de domaine complet du service FS (Federation Service) et vous configurez ADFS1 et PROXY1 en tant que batterie de serveurs AD FS.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-159">In this phase, you create a self-signed digital certificate for your federation service FQDN and configure ADFS1 and PROXY1 as an AD FS farm.</span></span>
  
<span data-ttu-id="bd4bf-160">Tout d’abord, utilisez le [portail Azure](https://portal.azure.com) pour vous connecter à la machine virtuelle DC1 à l’aide des informations d’identification de CORP\\User1, puis ouvrez une invite de commande Windows PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-160">First, use the [Azure portal](https://portal.azure.com) to connect to the DC1 virtual machine using the CORP\\User1 credentials, and then open an administrator-level Windows PowerShell command prompt.</span></span>
  
<span data-ttu-id="bd4bf-161">Ensuite, créez un compte de service AD FS avec cette commande à l’invite de commandes Windows PowerShell sur DC1 :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-161">Next, create an AD FS service account with this command at the Windows PowerShell command prompt on DC1:</span></span>
  
```powershell
New-ADUser -SamAccountName ADFS-Service -AccountPassword (read-host "Set user password" -assecurestring) -name "ADFS-Service" -enabled $true -PasswordNeverExpires $true -ChangePasswordAtLogon $false
```
<span data-ttu-id="bd4bf-162">Notez que cette commande vous invite à indiquer le mot de passe du compte.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-162">Note that this command prompts you to supply the account password.</span></span> <span data-ttu-id="bd4bf-163">Choisissez un mot de passe fort et enregistrez-le dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-163">Choose a strong password and record it in a secured location.</span></span> <span data-ttu-id="bd4bf-164">Vous en aurez besoin pour cette phase et pour la phase 5.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-164">You will need it for this phase and for Phase 5.</span></span>
  
<span data-ttu-id="bd4bf-p108">Utilisez le [portail Azure](https://portal.azure.com) pour vous connecter à la machine virtuelle ADFS1 à l’aide des informations d’identification de CORP\\User1. Ouvrez une invite de commande Windows PowerShell de niveau administrateur sur ADFS1, indiquez votre nom de domaine complet du service FS (Federation Service), puis exécutez ces commandes pour créer un certificat auto-signé :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-p108">Use the [Azure portal](https://portal.azure.com) to connect to the ADFS1 virtual machine using the CORP\\User1 credentials. Open an administrator-level Windows PowerShell command prompt on ADFS1, fill in your federation service FQDN, and then run these commands to create a self-signed certificate:</span></span>
  
```powershell
$fedServiceFQDN="<federation service FQDN>"
New-SelfSignedCertificate -DnsName $fedServiceFQDN -CertStoreLocation "cert:\LocalMachine\My"
New-Item -path c:\Certs -type directory
New-SmbShare -name Certs -path c:\Certs -changeaccess CORP\User1
```

<span data-ttu-id="bd4bf-167">Ensuite, utilisez ces étapes pour enregistrer le nouveau certificat auto-signé en tant que fichier.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-167">Next, use these steps to save the new self-signed certificate as a file.</span></span>
  
1. <span data-ttu-id="bd4bf-168">Sélectionnez **Démarrer**, entrez **mmc.exe**, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-168">Select **Start**, enter **mmc.exe**, and then press **Enter**.</span></span>
    
2. <span data-ttu-id="bd4bf-169">Sélectionnez **fichier**  >  **Ajouter/supprimer un composant logiciel enfichable**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-169">Select **File** > **Add/Remove Snap-in**.</span></span>
    
3. <span data-ttu-id="bd4bf-170">Dans **Ajouter ou supprimer des composants logiciels enfichables**, double-cliquez sur **certificats** dans la liste des composants logiciels enfichables disponibles, sélectionnez **compte d’ordinateur**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-170">In **Add or Remove Snap-ins**, double-click **Certificates** in the list of available snap-ins, select **Computer account**, and then select **Next**.</span></span>
    
4. <span data-ttu-id="bd4bf-171">Dans **Sélectionner un ordinateur**, sélectionnez **Terminer**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-171">In **Select Computer**, select **Finish**, and then select **OK**.</span></span>
    
5. <span data-ttu-id="bd4bf-172">Dans le volet d’arborescence, ouvrez **Certificats (ordinateur local) > Personnel > Certificats**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-172">In the tree pane, open **Certificates (Local Computer) > Personal > Certificates**.</span></span>
    
6. <span data-ttu-id="bd4bf-173">Sélectionnez et maintenez (ou cliquez avec le bouton droit) le certificat avec votre nom de domaine complet du service de Fédération, sélectionnez **toutes les tâches**, puis **Exporter**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-173">Select and hold (or right-click) the certificate with your federation service FQDN, select **All tasks**, and then select **Export**.</span></span>
    
7. <span data-ttu-id="bd4bf-174">Sur la page d' **Accueil** , sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-174">On the **Welcome** page, select **Next**.</span></span>
    
8. <span data-ttu-id="bd4bf-175">Sur la page **Exporter la clé privée** , sélectionnez **Oui**, puis **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-175">On the **Export Private Key** page, select **Yes**, and then select **Next**.</span></span>
    
9. <span data-ttu-id="bd4bf-176">Sur la page **format de fichier d’exportation** , sélectionnez **exporter toutes les propriétés étendues**, puis **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-176">On the **Export File Format** page, select **Export all extended properties**, and then select **Next**.</span></span>
    
10. <span data-ttu-id="bd4bf-177">Sur la page **sécurité** , sélectionnez **mot** de passe et saisissez un mot de passe dans **mot** de passe et confirmer le **mot de passe.**</span><span class="sxs-lookup"><span data-stu-id="bd4bf-177">On the **Security** page, select **Password** and enter a password in **Password** and **Confirm password.**</span></span>
    
11. <span data-ttu-id="bd4bf-178">Sur la page **fichier à exporter** , sélectionnez **Parcourir**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-178">On the **File to Export** page, select **Browse**.</span></span>
    
12. <span data-ttu-id="bd4bf-179">Accédez au dossier **C : \\ certs** , entrez **SSL** dans **nom de fichier**, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="bd4bf-179">Browse to the **C:\\Certs** folder, enter **SSL** in **File name**, and then select **Save.**</span></span>
    
13. <span data-ttu-id="bd4bf-180">Sur la page **fichier à exporter** , sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-180">On the **File to Export** page, select **Next**.</span></span>
    
14. <span data-ttu-id="bd4bf-181">Sur la page **fin de l’Assistant Exportation du certificat** , sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-181">On the **Completing the Certificate Export Wizard** page, select **Finish**.</span></span> <span data-ttu-id="bd4bf-182">Lorsque vous y êtes invité, sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-182">When prompted, select **OK**.</span></span>
    
<span data-ttu-id="bd4bf-183">Ensuite, installez le service AD FS avec cette commande à l’invite de commande Windows PowerShell sur ADFS1 :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-183">Next, install the AD FS service with this command at the Windows PowerShell command prompt on ADFS1:</span></span>
  
```powershell
Install-WindowsFeature ADFS-Federation -IncludeManagementTools
```

<span data-ttu-id="bd4bf-184">Attendez la fin de l’installation.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-184">Wait for the installation to complete.</span></span>
  
<span data-ttu-id="bd4bf-185">Ensuite, configurez le service AD FS en suivant ces étapes :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-185">Next, configure the AD FS service with these steps:</span></span>
  
1. <span data-ttu-id="bd4bf-186">Sélectionnez **Démarrer**, puis sélectionnez l’icône **Gestionnaire de serveur** .</span><span class="sxs-lookup"><span data-stu-id="bd4bf-186">Select **Start**, and then select the **Server Manager** icon.</span></span>
    
2. <span data-ttu-id="bd4bf-187">Dans le volet d’arborescence du gestionnaire de serveur, sélectionnez **AD FS**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-187">In the tree pane of Server Manager, select **AD FS**.</span></span>
    
3. <span data-ttu-id="bd4bf-188">Dans la barre d’outils située en haut de la page, sélectionnez le symbole d’avertissement orange, puis sélectionnez **configurer le service de Fédération sur ce serveur**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-188">In the tool bar at the top, select the orange caution symbol, and then select **Configure the federation service on this server**.</span></span>
    
4. <span data-ttu-id="bd4bf-189">Sur la page d' **Accueil** de l’Assistant Configuration des services de fédération Active Directory (AD FS), sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-189">On the **Welcome** page of the Active Directory Federation Services Configuration Wizard, select **Next**.</span></span>
    
5. <span data-ttu-id="bd4bf-190">Sur la page **connexion à AD DS** , sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-190">On the **Connect to AD DS** page, select **Next**.</span></span>
    
6. <span data-ttu-id="bd4bf-191">Sur la page **Spécifier les propriétés de service** :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-191">On the **Specify Service Properties** page:</span></span>
    
  - <span data-ttu-id="bd4bf-192">Pour **certificat SSL**, sélectionnez la flèche vers le bas, puis sélectionnez le certificat portant le nom de votre nom de domaine complet du service de Fédération.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-192">For **SSL Certificate**, select the down arrow, and then select the certificate with the name of your federation service FQDN.</span></span>
    
  - <span data-ttu-id="bd4bf-193">Dans **nom complet du service de Fédération**, entrez le nom de votre organisation fictive.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-193">In **Federation Service Display Name**, enter the name of your fictional organization.</span></span>
    
  - <span data-ttu-id="bd4bf-194">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-194">Select **Next**.</span></span>
    
7. <span data-ttu-id="bd4bf-195">Sur la page **spécifier le compte de service** , sélectionnez **Sélectionner** pour le nom du **compte**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-195">On the **Specify Service Account** page, select **Select** for **Account name**.</span></span>
    
8. <span data-ttu-id="bd4bf-196">Dans **Sélectionner l’utilisateur ou le compte de service**, entrez **ADFS-service**, sélectionnez **vérifier les noms**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-196">In **Select User or Service Account**, enter **ADFS-Service**, select **Check Names**, and then select **OK**.</span></span>
    
9. <span data-ttu-id="bd4bf-197">Dans **mot de passe du compte**, entrez le mot de passe du compte ADFS-Service, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-197">In **Account Password**, enter the password for the ADFS-Service account, and then select **Next**.</span></span>
    
10. <span data-ttu-id="bd4bf-198">Sur la page **spécifier la base de données de configuration** , sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-198">On the **Specify Configuration Database** page, select **Next**.</span></span>
    
11. <span data-ttu-id="bd4bf-199">Sur la page **examiner les options** , sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-199">On the **Review Options** page, select **Next**.</span></span>
    
12. <span data-ttu-id="bd4bf-200">Sur la page **vérifications des conditions préalables** , sélectionnez **configurer**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-200">On the **Pre-requisite Checks** page, select **Configure**.</span></span>

13. <span data-ttu-id="bd4bf-201">Sur la page **résultats** , sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-201">On the **Results** page, select **Close**.</span></span>
    
14. <span data-ttu-id="bd4bf-202">Sélectionnez **Démarrer**, sélectionnez l’icône alimentation, sélectionnez **redémarrer**, puis **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-202">Select **Start**, select the power icon, select **Restart**, and then select **Continue**.</span></span>
    
<span data-ttu-id="bd4bf-203">À partir du [portail Azure](https://portal.azure.com), connectez-vous à PROXY1 avec les informations d’identification du compte CORP\\User1.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-203">From the [Azure portal](https://portal.azure.com), connect to PROXY1 with the CORP\\User1 account credentials.</span></span>
  
<span data-ttu-id="bd4bf-204">Ensuite, suivez ces étapes pour installer le certificat auto-signé sur **PROXY1 et APP1**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-204">Next, use these steps to install the self-signed certificate on **both PROXY1 and APP1**.</span></span>
  
1. <span data-ttu-id="bd4bf-205">Sélectionnez **Démarrer**, entrez **mmc.exe**, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-205">Select **Start**, enter **mmc.exe**, and then press **Enter**.</span></span>
    
2. <span data-ttu-id="bd4bf-206">Sélectionnez **fichier > ajouter/supprimer un composant logiciel enfichable**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-206">Select **File > Add/Remove Snap-in**.</span></span>
    
3. <span data-ttu-id="bd4bf-207">Dans **Ajouter ou supprimer des composants logiciels enfichables**, double-cliquez sur **certificats** dans la liste des composants logiciels enfichables disponibles, sélectionnez **compte d’ordinateur**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-207">In **Add or Remove Snap-ins**, double-click **Certificates** in the list of available snap-ins, select **Computer account**, and then select **Next**.</span></span>
    
4. <span data-ttu-id="bd4bf-208">Dans **Sélectionner un ordinateur**, sélectionnez **Terminer**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-208">In **Select Computer**, select **Finish**, and then select **OK**.</span></span>
    
5. <span data-ttu-id="bd4bf-209">Dans le volet de l’arborescence, ouvrez certificats personnels **(ordinateur local)**  >  **Personal**  >  **Certificates**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-209">In the tree pane, open **Certificates (Local Computer)** > **Personal** > **Certificates**.</span></span>
    
6. <span data-ttu-id="bd4bf-210">Sélectionnez (ou cliquez avec le bouton droit) **personnel**, sélectionnez **toutes les tâches**, puis **Importer**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-210">Select and hold (or right-click) **Personal**, select **All tasks**, and then select **Import**.</span></span>
    
7. <span data-ttu-id="bd4bf-211">Sur la page d' **Accueil** , sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-211">On the **Welcome** page, select **Next**.</span></span>
    
8. <span data-ttu-id="bd4bf-212">Sur la page **fichier à importer** , entrez \*\* \\ \\ adfs1 \\ certs \\ SSL. pfx\*\*, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-212">On the **File to Import** page, enter **\\\\adfs1\\certs\\ssl.pfx**, and then select **Next**.</span></span>
    
9. <span data-ttu-id="bd4bf-213">Sur la page **protection de clé privée** , saisissez le mot de passe du certificat dans **mot de passe**, puis cliquez sur **suivant.**</span><span class="sxs-lookup"><span data-stu-id="bd4bf-213">On the **Private key protection** page, enter the certificate password in **Password**, and then select **Next.**</span></span>
    
10. <span data-ttu-id="bd4bf-214">Sur la page **magasin de certificats** , sélectionnez **suivant.**</span><span class="sxs-lookup"><span data-stu-id="bd4bf-214">On the **Certificate store** page, select **Next.**</span></span>
    
11. <span data-ttu-id="bd4bf-215">Sur la page **terminé** , sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-215">On the **Completing** page, select **Finish**.</span></span>
    
12. <span data-ttu-id="bd4bf-216">Sur la page **magasin de certificats** , sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-216">On the **Certificate Store** page, select **Next**.</span></span>
    
13. <span data-ttu-id="bd4bf-217">Lorsque vous y êtes invité, sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-217">When prompted, select **OK**.</span></span>
    
14. <span data-ttu-id="bd4bf-218">Dans le volet de l’arborescence, sélectionnez **certificats**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-218">In the tree pane, select **Certificates**.</span></span>
    
15. <span data-ttu-id="bd4bf-219">Sélectionnez (ou cliquez avec le bouton droit) le certificat, puis sélectionnez **copier**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-219">Select and hold (or right-click) the certificate, and then select **Copy**.</span></span>
    
16. <span data-ttu-id="bd4bf-220">Dans le volet d’arborescence, ouvrez certificats d' **autorités de certification racines de confiance**  >  **Certificates**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-220">In the tree pane, open **Trusted Root Certification Authorities** > **Certificates**.</span></span>
    
17. <span data-ttu-id="bd4bf-221">Déplacez le pointeur de la souris en dessous de la liste des certificats installés, sélectionnez et maintenez (ou cliquez avec le bouton droit), puis sélectionnez **coller**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-221">Move your mouse pointer below the list of installed certificates, select and hold (or right-click), and then select **Paste**.</span></span>
    
<span data-ttu-id="bd4bf-222">Ouvrez une invite de commande PowerShell de niveau administrateur et exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-222">Open an administrator-level PowerShell command prompt and run the following command:</span></span>
  
```powershell
Install-WindowsFeature Web-Application-Proxy -IncludeManagementTools
```

<span data-ttu-id="bd4bf-223">Attendez la fin de l’installation.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-223">Wait for the installation to complete.</span></span>
  
<span data-ttu-id="bd4bf-224">Suivez ces étapes pour configurer le service de proxy d’application web de manière à ce qu’il utilise ADFS1 comme serveur de fédération :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-224">Use these steps to configure the web application proxy service to use ADFS1 as its federation server:</span></span>
  
1. <span data-ttu-id="bd4bf-225">Sélectionnez **Démarrer**, puis gestionnaire de **serveur**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-225">Select **Start**, and then select **Server Manager**.</span></span>
    
2. <span data-ttu-id="bd4bf-226">Dans le volet de l’arborescence, sélectionnez **accès à distance**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-226">In the tree pane, select **Remote Access**.</span></span>
    
3. <span data-ttu-id="bd4bf-227">Dans la barre d’outils située en haut de la page, sélectionnez le symbole d’avertissement orange, puis sélectionnez **ouvrir l’Assistant proxy d’application Web**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-227">In the tool bar at the top, select the orange caution symbol, and then select **Open the Web Application Proxy Wizard**.</span></span>
    
4. <span data-ttu-id="bd4bf-228">Sur la page d' **Accueil** de l’Assistant Configuration du proxy d’application Web, sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-228">On the **Welcome** page of the Web Application Proxy Configuration Wizard, select **Next**.</span></span>
    
5. <span data-ttu-id="bd4bf-229">Sur la page **Serveur de fédération** :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-229">On the **Federation Server** page:</span></span>
    
  - <span data-ttu-id="bd4bf-230">Dans la zone **nom du service de Fédération** , entrez le nom de domaine complet de votre service de Fédération.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-230">In the **Federation service name** box, enter your federation service FQDN.</span></span>
    
  - <span data-ttu-id="bd4bf-231">Dans la zone **nom d’utilisateur** , entrez **Corp \\ utilisateur1**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-231">In the **User name** box, enter **CORP\\User1**.</span></span>
    
  - <span data-ttu-id="bd4bf-232">Dans la zone **mot de passe** , entrez le mot de passe du compte utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-232">In the **Password** box, enter the password for the User1 account.</span></span>
    
  - <span data-ttu-id="bd4bf-233">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-233">Select **Next**.</span></span>
    
6. <span data-ttu-id="bd4bf-234">Sur la page **certificat de proxy AD FS** , sélectionnez la flèche vers le bas, sélectionnez le certificat avec votre nom de domaine complet du service de Fédération, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-234">On the **AD FS Proxy Certificate** page, select the down arrow, select the certificate with your federation service FQDN, and then select **Next**.</span></span>
    
7. <span data-ttu-id="bd4bf-235">Sur la page **confirmation** , sélectionnez **configurer**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-235">On the **Confirmation** page, select **Configure**.</span></span>
    
8. <span data-ttu-id="bd4bf-236">Sur la page **résultats** , sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-236">On the **Results** page, select **Close**.</span></span>
    
## <a name="phase-5-configure-microsoft-365-for-federated-identity"></a><span data-ttu-id="bd4bf-237">Phase 5: configuration de Microsoft 365 pour l’identité fédérée</span><span class="sxs-lookup"><span data-stu-id="bd4bf-237">Phase 5: Configure Microsoft 365 for federated identity</span></span>

<span data-ttu-id="bd4bf-238">Utilisez le [portail Azure](https://portal.azure.com) pour vous connecter à la machine virtuelle APP1 avec les informations d’identification du compte CORP\\User1.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-238">Use the [Azure portal](https://portal.azure.com) to connect to the APP1 virtual machine with the CORP\\User1 account credentials.</span></span>
  
<span data-ttu-id="bd4bf-239">Suivez ces étapes pour configurer Azure AD Connect et votre abonnement Microsoft 365 pour l’authentification fédérée :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-239">Use these steps to configure Azure AD Connect and your Microsoft 365 subscription for federated authentication:</span></span>
  
1. <span data-ttu-id="bd4bf-240">Sur le bureau, double-cliquez sur **Azure AD Connect**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-240">From the desktop, double-click **Azure AD Connect**.</span></span>
    
2. <span data-ttu-id="bd4bf-241">Sur la page **Bienvenue dans Azure ad Connect** , sélectionnez **configurer**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-241">On the **Welcome to Azure AD Connect** page, select **Configure**.</span></span>
    
3. <span data-ttu-id="bd4bf-242">Sur la page **tâches supplémentaires** , sélectionnez **modifier la connexion de l’utilisateur**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-242">On the **Additional tasks** page, select **Change user sign-in**, and then select **Next**.</span></span>
    
4. <span data-ttu-id="bd4bf-243">Sur la page **connexion à Azure ad** , entrez le nom et le mot de passe de votre compte d’administrateur général, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-243">On the **Connect to Azure AD** page, enter your global administrator account name and password, and then select **Next**.</span></span>
    
5. <span data-ttu-id="bd4bf-244">Sur la page de connexion de l' **utilisateur** , sélectionnez **Fédération avec AD FS**, puis **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-244">On the **User sign-in** page, select **Federation with AD FS**, and then select **Next**.</span></span>
    
6. <span data-ttu-id="bd4bf-245">Sur la **page batterie de serveurs AD FS** , sélectionnez **utiliser une batterie de serveurs AD FS existante**, entrez **ADFS1** dans la zone **nom du serveur** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-245">On the **AD FS farm** page, select **Use an existing AD FS farm**, enter **ADFS1** in the **Server Name** box, and then select **Next**.</span></span>
    
7. <span data-ttu-id="bd4bf-246">Lorsque vous êtes invité à fournir les informations d’identification du serveur, entrez les informations d’identification du compte d’entreprise \\ utilisateur1, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-246">When prompted for server credentials, enter the credentials of the CORP\\User1 account, and then select **OK**.</span></span>
    
8. <span data-ttu-id="bd4bf-247">Sur la page informations d’identification d' **administrateur de domaine** , entrez **Corp \\ utilisateur1** dans la zone **nom d’utilisateur** , entrez le mot de passe du compte dans la zone **mot de passe** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-247">On the **Domain Administrator** credentials page, enter **CORP\\User1** in the **Username** box, enter the account password in the **Password** box, and then select **Next**.</span></span>
    
9. <span data-ttu-id="bd4bf-248">Sur la page **compte de service AD FS** , entrez **Corp \\ ADFS-service** dans la zone **nom d'** utilisateur du domaine, entrez le mot de passe du compte dans la zone **mot de passe** de l’utilisateur de domaine, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-248">On the **AD FS service account** page, enter **CORP\\ADFS-Service** in the **Domain Username** box, enter the account password in the **Domain User Password** box, and then select **Next**.</span></span>
    
10. <span data-ttu-id="bd4bf-249">Sur la page **domaine Azure ad** , dans **domaine**, sélectionnez le nom du domaine que vous avez précédemment créé et ajouté à votre abonnement à la phase 1, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-249">On the **Azure AD Domain** page, in **Domain**, select the name of the domain that you previously created and added to your subscription in Phase 1, and then select **Next**.</span></span>
    
11. <span data-ttu-id="bd4bf-250">Sur la page **prêt à configurer** , sélectionnez **configurer**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-250">On the **Ready to configure** page, select **Configure**.</span></span>
    
12. <span data-ttu-id="bd4bf-251">Sur la page **installation terminée** , sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-251">On the **Installation complete** page, select **Verify**.</span></span>
    
    <span data-ttu-id="bd4bf-252">Des messages indiquant que la configuration intranet et Internet ont été vérifiés doivent s’afficher.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-252">You should see messages indicating that both the intranet and internet configuration was verified.</span></span>
    
13. <span data-ttu-id="bd4bf-253">Sur la page **installation terminée** , sélectionnez **quitter**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-253">On the **Installation complete** page, select **Exit**.</span></span>
    
<span data-ttu-id="bd4bf-254">Pour vérifier que l’authentification fédérée fonctionne, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-254">To demonstrate that federated authentication is working:</span></span>
  
1. <span data-ttu-id="bd4bf-255">Ouvrez une nouvelle instance privée de votre navigateur sur votre ordinateur local et accédez à [https://admin.microsoft.com](https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="bd4bf-255">Open a new private instance of your browser on your local computer and go to [https://admin.microsoft.com](https://admin.microsoft.com).</span></span>
    
2. <span data-ttu-id="bd4bf-256">Pour les informations d’identification de connexion, entrez **User1@** \<*the domain created in Phase 1*> .</span><span class="sxs-lookup"><span data-stu-id="bd4bf-256">For the sign-in credentials, enter **user1@**\<*the domain created in Phase 1*>.</span></span>
    
    <span data-ttu-id="bd4bf-257">Par exemple, si votre domaine de test est **testlab.contoso.com**, vous devez entrer « User1@testlab.contoso.com ».</span><span class="sxs-lookup"><span data-stu-id="bd4bf-257">For example, if your test domain is **testlab.contoso.com**, you would enter "user1@testlab.contoso.com".</span></span> <span data-ttu-id="bd4bf-258">Appuyez sur la touche de **tabulation** ou autorisez Microsoft 365 à vous rediriger automatiquement.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-258">Press the **Tab** key or allow Microsoft 365 to automatically redirect you.</span></span>
    
    <span data-ttu-id="bd4bf-259">Une page **Votre connexion n’est pas privée** devrait s’afficher.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-259">You should now see a **Your connection is not private** page.</span></span> <span data-ttu-id="bd4bf-260">Vous constatez que vous avez installé un certificat auto-signé sur ADFS1 que votre ordinateur de bureau ne peut pas valider.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-260">You are seeing this because you installed a self-signed certificate on ADFS1 that your desktop computer can't validate.</span></span> <span data-ttu-id="bd4bf-261">Dans un déploiement de production d’authentification fédérée, vous utiliseriez un certificat provenant d’une autorité de certification approuvée et vos utilisateurs ne verraient pas cette page.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-261">In a production deployment of federated authentication, you would use a certificate from a trusted certification authority and your users would not see this page.</span></span>
    
3. <span data-ttu-id="bd4bf-262">Sur la page **votre connexion n’est pas privée** , sélectionnez **avancé**, puis sélectionnez \*\*passer à \<*your federation service FQDN*> \*\*.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-262">On the **Your connection is not private** page, select **Advanced**, and then select **Proceed to \<*your federation service FQDN*>**.</span></span> 
    
4. <span data-ttu-id="bd4bf-263">Sur la page contenant le nom de votre organisation fictive, connectez-vous avec les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-263">On the page with the name of your fictional organization, sign in with the following:</span></span>
    
  - <span data-ttu-id="bd4bf-264">**CORP\\User1** pour le nom ;</span><span class="sxs-lookup"><span data-stu-id="bd4bf-264">**CORP\\User1** for the name</span></span>
    
  - <span data-ttu-id="bd4bf-265">le mot de passe du compte User1.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-265">The password for the User1 account</span></span>
    
    <span data-ttu-id="bd4bf-266">Vous devez voir la **page d’accueil Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-266">You should see the **Microsoft Office Home** page.</span></span>
    
<span data-ttu-id="bd4bf-p112">Cette procédure montre que votre abonnement d’évaluation est fédéré avec le domaine corp.contoso.com AD DS hébergé sur DC1. Voici les principes de base du processus d’authentification :</span><span class="sxs-lookup"><span data-stu-id="bd4bf-p112">This procedure demonstrates that your trial subscription is federated with the AD DS corp.contoso.com domain hosted on DC1. Here are the basics of the authentication process:</span></span>
  
1. <span data-ttu-id="bd4bf-269">Lorsque vous utilisez le domaine fédéré que vous avez créé à la phase 1 dans le nom de compte de connexion, Microsoft 365 redirige votre navigateur vers le nom de domaine complet de votre service FS (Federation Service) et PROXY1.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-269">When you use the federated domain that you created in Phase 1 within the sign-in account name, Microsoft 365 redirects your browser to your federation service FQDN and PROXY1.</span></span>
    
2. <span data-ttu-id="bd4bf-270">PROXY1 envoie la page de connexion de l’entreprise fictive à votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-270">PROXY1 sends your local computer the fictional company sign-in page.</span></span>
    
3. <span data-ttu-id="bd4bf-271">Lorsque vous envoyez CORP\\User1 et le mot de passe à PROXY1, il les transfère à ADFS1.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-271">When you send CORP\\User1 and the password to PROXY1, it forwards them to ADFS1.</span></span>
    
4. <span data-ttu-id="bd4bf-272">ADFS1 valide CORP\\User1 et le mot de passe avec DC1 et envoie un jeton de sécurité à votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-272">ADFS1 validates CORP\\User1 and the password with DC1 and sends your local computer a security token.</span></span>
    
5. <span data-ttu-id="bd4bf-273">Votre ordinateur local envoie le jeton de sécurité à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-273">Your local computer sends the security token to Microsoft 365.</span></span>
    
6. <span data-ttu-id="bd4bf-274">Microsoft 365 confirme que le jeton de sécurité a été créé par ADFS1 et autorise l’accès.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-274">Microsoft 365 validates that the security token was created by ADFS1 and allows access.</span></span>
    
<span data-ttu-id="bd4bf-p113">Votre abonnement d’évaluation est désormais configuré avec l’authentification fédérée. Vous pouvez utiliser cet environnement de développement/test pour les scénarios d’authentification avancés.</span><span class="sxs-lookup"><span data-stu-id="bd4bf-p113">Your trial subscription is now configured with federated authentication. You can use this dev/test environment for advanced authentication scenarios.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="bd4bf-277">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="bd4bf-277">Next step</span></span>

<span data-ttu-id="bd4bf-278">Lorsque vous êtes prêt à déployer l’authentification fédérée prête pour la production et la haute disponibilité pour Microsoft 365 dans Azure, consultez la rubrique [Deploy High Availability Federated Authentication for microsoft 365 in Azure](deploy-high-availability-federated-authentication-for-microsoft-365-in-azure.md).</span><span class="sxs-lookup"><span data-stu-id="bd4bf-278">When you are ready to deploy production-ready, high availability federated authentication for Microsoft 365 in Azure, see [Deploy high availability federated authentication for Microsoft 365 in Azure](deploy-high-availability-federated-authentication-for-microsoft-365-in-azure.md).</span></span>
  
