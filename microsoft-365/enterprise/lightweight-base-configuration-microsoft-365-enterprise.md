---
title: Configuration de base légère
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/15/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom:
- Ent_TLGs
ms.assetid: 6f916a77-301c-4be2-b407-6cec4d80df76
description: Utilisez ce guide de laboratoire de test pour créer un environnement de test léger destiné aux tests Microsoft 365 Entreprise.
ms.openlocfilehash: 26109f6237ad2eaeb2ac323c190a885031c03a04
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289276"
---
# <a name="the-lightweight-base-configuration"></a><span data-ttu-id="c9ace-103">Configuration de base légère</span><span class="sxs-lookup"><span data-stu-id="c9ace-103">The lightweight base configuration</span></span>

<span data-ttu-id="c9ace-104">Cet article vous fournit des instructions étape par étape pour créer un environnement simplifié qui comprend Office 365 E5, Enterprise Mobility + Security (EMS) E5 et un ordinateur exécutant Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="c9ace-104">This article provides you with step-by-step instructions to create a simplified environment that includes Office 365 E5, Enterprise Mobility + Security (EMS) E5, and a computer running Windows 10 Enterprise.</span></span> 

![Environnement de test Microsoft 3656 Entreprise léger](media/lightweight-base-configuration-microsoft-365-enterprise/Phase4.png)

<span data-ttu-id="c9ace-106">Utilisez l’environnement que vous aurez créé pour tester les fonctionnalités et le bon fonctionnement de [Microsoft 365 Entreprise](https://www.microsoft.com/microsoft-365/enterprise).</span><span class="sxs-lookup"><span data-stu-id="c9ace-106">Use the resulting environment to test the features and functionality of [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise).</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)
  
> [!TIP]
> <span data-ttu-id="c9ace-108">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="c9ace-108">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-create-your-office-365-e5-subscription"></a><span data-ttu-id="c9ace-109">Phase 1 : Création de votre abonnement Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="c9ace-109">Phase 1: Create your Office 365 E5 subscription</span></span>

<span data-ttu-id="c9ace-110">Suivez les étapes des phases 2 et 3 de l’article sur l’[environnement de développement/test Office 365](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment) pour créer un environnement de développement/test Office 365 léger, comme illustré à la Figure 1.</span><span class="sxs-lookup"><span data-stu-id="c9ace-110">Follow the steps in Phase 2 and Phase 3 of the [Office 365 dev/test environment](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment) to create a lightweight Office 365 dev/test environment, as shown in Figure 1.</span></span>
  
<span data-ttu-id="c9ace-111">**Figure 1 : Votre abonnement Office 365 E5 avec son client et ses comptes d’utilisateur Azure Active Directory (AD)**</span><span class="sxs-lookup"><span data-stu-id="c9ace-111">**Figure 1: Your Office 365 E5 subscription with its Azure Active Directory (AD) tenant and user accounts**</span></span>

![Phase 1 de l’environnement de test Microsoft 365 Entreprise](media/lightweight-base-configuration-microsoft-365-enterprise/Phase1.png)

> [!NOTE]
> <span data-ttu-id="c9ace-p101">L’abonnement à la version d’évaluation d’Office 365 E5 est valide pendant 30 jours. Vous pouvez facilement l’étendre jusqu’à 60 jours. Pour un environnement de test permanent, créez un abonnement payant avec un nombre réduit de licences.</span><span class="sxs-lookup"><span data-stu-id="c9ace-p101">The Office 365 E5 trial subscription is 30 days, which can be easily extended to 60 days. For a permanent test environment, create a new paid subscription with a small number of licenses.</span></span> 
  
## <a name="phase-2-add-ems"></a><span data-ttu-id="c9ace-115">Phase 2 : Ajout d’EMS</span><span class="sxs-lookup"><span data-stu-id="c9ace-115">Phase 2: Add EMS</span></span>

<span data-ttu-id="c9ace-116">Dans cette phase, vous vous inscrivez pour l’abonnement à la version d’évaluation d’EMS E5 et l’ajoutez à la même organisation que votre abonnement à la version d’évaluation d’Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="c9ace-116">In this phase, you sign up for the EMS E5 trial subscription and add it to the same organization as your Office 365 E5 trial subscription.</span></span>
  
<span data-ttu-id="c9ace-117">Tout d’abord, ajoutez l’abonnement d’évaluation EMS E5 et attribuez une licence EMS à votre compte Administrateur général.</span><span class="sxs-lookup"><span data-stu-id="c9ace-117">First, add the EMS E5 trial subscription and assign an EMS license to your global administrator account.</span></span>
  
1. <span data-ttu-id="c9ace-118">Utilisez une instance privée d’un navigateur Internet pour vous connecter au portail Office à l’aide de vos informations d’identification de compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="c9ace-118">With a private instance of an Internet browser, sign in to the Office 365 portal with your global administrator account credentials.</span></span> <span data-ttu-id="c9ace-119">Pour obtenir de l’aide, consultez [Où se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="c9ace-119">For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="c9ace-120">Cliquez sur la vignette **Administration**.</span><span class="sxs-lookup"><span data-stu-id="c9ace-120">Click the **Admin** tile.</span></span>
    
3. <span data-ttu-id="c9ace-121">Sous l’onglet **Centre d’administration Microsoft 365** de votre navigateur, dans le volet de navigation gauche, cliquez sur **Facturation > Acheter des services**.</span><span class="sxs-lookup"><span data-stu-id="c9ace-121">On the **Microsoft 365 admin center** tab, in the left navigation, click **Billing > Purchase services**.</span></span>
    
4. <span data-ttu-id="c9ace-p103">Dans la page **Acheter des services**, recherchez l’élément **Enterprise Mobility + Security E5**. Pointez votre souris dessus et cliquez sur **Démarrer l’essai gratuit**.</span><span class="sxs-lookup"><span data-stu-id="c9ace-p103">On the **Purchase services** page, find the **Enterprise Mobility + Security E5** item. Hover your mouse pointer over it and click **Start free trial**.</span></span>
    
5. <span data-ttu-id="c9ace-124">Dans la page **Confirmer votre commande**, cliquez sur **Essayer maintenant**.</span><span class="sxs-lookup"><span data-stu-id="c9ace-124">On the **Confirm your order** page, click **Try now**.</span></span>
    
6. <span data-ttu-id="c9ace-125">Dans la page **Réception de la commande**, cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="c9ace-125">On the **Order receipt** page, click **Continue**.</span></span>
    
7. <span data-ttu-id="c9ace-126">Sous l’onglet **Centre d’administration Office 365** de votre navigateur, dans le volet de navigation gauche, cliquez sur **Utilisateurs > Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="c9ace-126">On the **Office 365 Admin center** tab in your browser, in the left navigation, click **Users > Active users**.</span></span>
    
8. <span data-ttu-id="c9ace-127">Cliquez sur votre compte Administrateur général, puis cliquez sur **Modifier** pour les **licences de produit**.</span><span class="sxs-lookup"><span data-stu-id="c9ace-127">Click your global administrator account, and then click **Edit** for **Product licenses**.</span></span>
    
9. <span data-ttu-id="c9ace-128">Dans le volet **Licences de produit**, activez la licence de produit pour **Enterprise Mobility + Security E5** en sélectionnant **Activer**, cliquez sur **Enregistrer**, cliquez deux fois sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="c9ace-128">On the **Product licenses** pane, turn the product license for **Enterprise Mobility + Security E5** to **On**, click **Save,** and then click **Close** twice.</span></span>
    
> [!NOTE]
> <span data-ttu-id="c9ace-p104">L’abonnement à la version d’évaluation d’Enterprise Mobility + Security E5 est de 90 jours. Pour un environnement de test permanent, créez un nouvel abonnement payant avec un nombre réduit de licences.</span><span class="sxs-lookup"><span data-stu-id="c9ace-p104">The Enterprise Mobility + Security E5 trial subscription is 90 days. For a permanent test environment, create a new paid subscription with a small number of licenses.</span></span> 
  
 <span data-ttu-id="c9ace-131">***Si vous avez terminé la Phase 3 de l’*** [environnement de développement/test Office 365](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment), répétez les étapes 8 et 9 de la procédure précédente pour tous vos autres comptes (Utilisateur 2, Utilisateur 3, Utilisateur 4 et Utilisateur 5).</span><span class="sxs-lookup"><span data-stu-id="c9ace-131">***If you completed Phase 3 of the*** [Office 365 dev/test environment](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment), repeat steps 8 and 9 of the previous procedure for all of your other accounts (User 2, User 3, User 4, and User 5).</span></span>
  
<span data-ttu-id="c9ace-132">Votre environnement de test comporte maintenant :</span><span class="sxs-lookup"><span data-stu-id="c9ace-132">Your test environment now has:</span></span>
  
- <span data-ttu-id="c9ace-133">Des abonnements d’évaluation Office 365 E5 Entreprise et EMS E5 qui partagent le même client Azure AD avec votre liste des comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c9ace-133">Office 365 E5 Enterprise and EMS E5 trial subscriptions sharing the same Azure AD tenant with your list of user accounts.</span></span>
- <span data-ttu-id="c9ace-134">Tous vos comptes d’utilisateur appropriés (l’administrateur général ou tous les cinq comptes d’utilisateur) sont activés pour utiliser Office 365 E5 et EMS E5.</span><span class="sxs-lookup"><span data-stu-id="c9ace-134">All your appropriate user accounts (either just the global administrator or all five user accounts) are enabled to use Office 365 E5 and EMS E5.</span></span>
    
<span data-ttu-id="c9ace-135">La figure 2 montre la configuration obtenue, qui ajoute EMS.</span><span class="sxs-lookup"><span data-stu-id="c9ace-135">Figure 2 shows your resulting configuration, which adds EMS.</span></span>
  
<span data-ttu-id="c9ace-136">**Figure 2 : Ajout de l’abonnement à la version d’évaluation d’EMS**</span><span class="sxs-lookup"><span data-stu-id="c9ace-136">**Figure 2: Adding the EMS trial subscription**</span></span>

![Phase 2 de l’environnement de test Microsoft 365 Entreprise](media/lightweight-base-configuration-microsoft-365-enterprise/Phase2.png)
  
## <a name="phase-3-create-a-windows-10-enterprise-computer"></a><span data-ttu-id="c9ace-138">Phase 3 : Création d’un ordinateur Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="c9ace-138">Phase 3: Create a Windows 10 Enterprise computer</span></span>

<span data-ttu-id="c9ace-139">Au cours de cette phase, vous allez créer un ordinateur autonome exécutant Windows 10 Entreprise sous forme d’un ordinateur physique, d’une machine virtuelle ou d’une machine virtuelle Azure.</span><span class="sxs-lookup"><span data-stu-id="c9ace-139">In this phase, you create a standalone computer running Windows 10 Enterprise as either a physical computer, a virtual machine, or an Azure virtual machine.</span></span>
  
### <a name="physical-computer"></a><span data-ttu-id="c9ace-140">Ordinateur physique</span><span class="sxs-lookup"><span data-stu-id="c9ace-140">Physical computer</span></span>

<span data-ttu-id="c9ace-p105">Munissez-vous d’un ordinateur personnel et installez Windows 10 Entreprise dessus. Vous pouvez télécharger la version d’évaluation de Windows 10 Entreprise [ici](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span><span class="sxs-lookup"><span data-stu-id="c9ace-p105">Obtain a personal computer and install Windows 10 Enterprise on it. You can download the Windows 10 Enterprise trial [here](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span></span>
  
### <a name="virtual-machine"></a><span data-ttu-id="c9ace-143">Machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="c9ace-143">Virtual machine</span></span>

<span data-ttu-id="c9ace-p106">Créez une machine virtuelle à l’aide de l’hyperviseur de votre choix et installez Windows 10 Entreprise dessus. Vous pouvez télécharger la version d’évaluation de Windows 10 Entreprise [ici](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span><span class="sxs-lookup"><span data-stu-id="c9ace-p106">Create a virtual machine using the hypervisor of your choice and install Windows 10 Enterprise on it. You can download the Windows 10 Enterprise trial [here](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span></span>
  
### <a name="virtual-machine-in-azure"></a><span data-ttu-id="c9ace-146">Machine virtuelle dans Azure</span><span class="sxs-lookup"><span data-stu-id="c9ace-146">Virtual machine in Azure</span></span>

<span data-ttu-id="c9ace-p107">Pour créer une machine virtuelle exécutant Windows 10 dans Microsoft Azure, ***vous devez disposer d’un abonnement Visual Studio*** qui vous permet d’accéder à l’image pour Windows 10 Entreprise. D’autres types d’abonnements Azure, tels que les abonnements d’évaluation et payants, ne permettent pas d’accéder à cette image. Pour obtenir les informations les plus récentes, reportez-vous à l’article [Utilisation d’un client Windows dans Azure pour les scénarios de développement et/ou test](https://docs.microsoft.com/azure/virtual-machines/windows/client-images).</span><span class="sxs-lookup"><span data-stu-id="c9ace-p107">To create a Windows 10 virtual machine in Microsoft Azure, ***you must have a Visual Studio-based subscription***, which has access to the image for Windows 10 Enterprise. Other types of Azure subscriptions, such as trial and paid subscriptions, do not have access to this image. For the latest information, see [Use Windows client in Azure for dev/test scenarios](https://docs.microsoft.com/azure/virtual-machines/windows/client-images).</span></span>
  
> [!NOTE]
> <span data-ttu-id="c9ace-p108">Les ensembles de commandes suivants utilisent la dernière version d’Azure PowerShell. Reportez-vous à l’article relatif à la [prise en main des cmdlets Azure PowerShell](https://docs.microsoft.com/powershell/azureps-cmdlets-docs/). Ces ensembles de commandes créent une machine virtuelle Windows 10 Entreprise nommée WIN10 ainsi que l’intégralité de son infrastructure requise, y compris un groupe de ressources, un compte de stockage et un réseau virtuel. Si vous connaissez déjà les services d’infrastructure Azure, adaptez ces instructions à votre infrastructure actuellement déployée.</span><span class="sxs-lookup"><span data-stu-id="c9ace-p108">The following command sets use the latest version of Azure PowerShell. See [Get started with Azure PowerShell cmdlets](https://docs.microsoft.com/powershell/azureps-cmdlets-docs/). These command sets build a Windows 10 Enterprise virtual machine named WIN10 and all of its required infrastructure, including a resource group, a storage account, and a virtual network. If you are already familiar with Azure infrastructure services, please adapt these instructions to suit your currently deployed infrastructure.</span></span> 
  
<span data-ttu-id="c9ace-154">Tout d’abord, lancez une invite Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9ace-154">First, start a Microsoft PowerShell prompt.</span></span>
  
<span data-ttu-id="c9ace-155">Connectez-vous à votre compte Azure avec la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="c9ace-155">Sign in to your Azure account with the following command.</span></span>
  
```
Connect-AzAccount
```

<span data-ttu-id="c9ace-156">Obtenez le nom de votre abonnement à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="c9ace-156">Get your subscription name using the following command.</span></span>
  
```
Get-AzSubscription | Sort Name | Select Name
```

<span data-ttu-id="c9ace-p109">Définissez votre abonnement Azure. Remplacez tout le texte entre guillemets, y compris les caractères \< et >, avec le nom correct.</span><span class="sxs-lookup"><span data-stu-id="c9ace-p109">Set your Azure subscription. Replace everything within the quotes, including the \< and > characters, with the correct name.</span></span>
  
```
$subscr="<subscription name>"
Get-AzSubscription -SubscriptionName $subscr | Select-AzSubscription
```

<span data-ttu-id="c9ace-p110">Ensuite, créez un nouveau groupe de ressources. Pour déterminer un nom de groupe de ressources unique, utilisez cette commande pour répertorier vos groupes de ressources existants.</span><span class="sxs-lookup"><span data-stu-id="c9ace-p110">Next, create a new resource group. To determine a unique resource group name, use this command to list your existing resource groups.</span></span>
  
```
Get-AzResourceGroup | Sort ResourceGroupName | Select ResourceGroupName
```

<span data-ttu-id="c9ace-p111">Créez votre groupe de ressources avec ces commandes. Remplacez tout le texte entre guillemets, y compris les caractères \< et >, par les noms corrects.</span><span class="sxs-lookup"><span data-stu-id="c9ace-p111">Create your new resource group with these commands. Replace everything within the quotes, including the \< and > characters, with the correct names.</span></span>
  
```
$rgName="<resource group name>"
$locName="<location name, such as West US>"
New-AzResourceGroup -Name $rgName -Location $locName
```

<span data-ttu-id="c9ace-p112">Ensuite, créez une ressource virtuelle et la machine virtuelle WIN10 avec ces commandes. Lorsque vous y êtes invité, indiquez le nom et le mot de passe du compte d’administrateur local pour WIN10, et enregistrez ces informations dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="c9ace-p112">Next, you create a new virtual network and the WIN10 virtual machine with these commands. When prompted, provide the name and password of the local administrator account for WIN10 and store these in a secure location.</span></span>
  
```
$corpnetSubnet=New-AzVirtualNetworkSubnetConfig -Name Corpnet -AddressPrefix 10.0.0.0/24
New-AzVirtualNetwork -Name "M365Ent-TestLab" -ResourceGroupName $rgName -Location $locName -AddressPrefix 10.0.0.0/8 -Subnet $corpnetSubnet
$rule1=New-AzNetworkSecurityRuleConfig -Name "RDPTraffic" -Description "Allow RDP to all VMs on the subnet" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
New-AzNetworkSecurityGroup -Name Corpnet -ResourceGroupName $rgName -Location $locName -SecurityRules $rule1
$vnet=Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "M365Ent-TestLab"
$nsg=Get-AzNetworkSecurityGroup -Name Corpnet -ResourceGroupName $rgName
Set-AzVirtualNetworkSubnetConfig -VirtualNetwork $vnet -Name Corpnet -AddressPrefix "10.0.0.0/24" -NetworkSecurityGroup $nsg
$pip=New-AzPublicIpAddress -Name WIN10-PIP -ResourceGroupName $rgName -Location $locName -AllocationMethod Dynamic
$nic=New-AzNetworkInterface -Name WIN10-NIC -ResourceGroupName $rgName -Location $locName -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $pip.Id
$vm=New-AzVMConfig -VMName WIN10 -VMSize Standard_D1_V2
$cred=Get-Credential -Message "Type the name and password of the local administrator account for WIN10."
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName WIN10 -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsDesktop -Offer Windows-10 -Skus RS3-Pro -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name WIN10-TestLab-OSDisk -DiskSizeInGB 128 -CreateOption FromImage
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm
```

## <a name="phase-4-join-your-windows-10-computer-to-azure-ad"></a><span data-ttu-id="c9ace-165">Phase 4 : Association de votre ordinateur Windows 10 à Azure AD</span><span class="sxs-lookup"><span data-stu-id="c9ace-165">Phase 4: Join your Windows 10 computer to Azure AD</span></span>

<span data-ttu-id="c9ace-166">Lorsque l’ordinateur physique ou la machine virtuelle avec Windows 10 Entreprise est créée, connectez-vous avec un compte d’administrateur local.</span><span class="sxs-lookup"><span data-stu-id="c9ace-166">After the physical or virtual machine with Windows 10 Enterprise is created, sign in with a local administrator account.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c9ace-167">Suivez [ces instructions](https://docs.microsoft.com/azure/virtual-machines/windows/connect-logon) pour vous connecter à une machine virtuelle dans Azure.</span><span class="sxs-lookup"><span data-stu-id="c9ace-167">For a virtual machine in Azure, connect to it using [these instructions](https://docs.microsoft.com/azure/virtual-machines/windows/connect-logon).</span></span>
  
<span data-ttu-id="c9ace-168">Ensuite, associez l’ordinateur WIN10 au client Azure AD de vos abonnements Office 365 et EMS.</span><span class="sxs-lookup"><span data-stu-id="c9ace-168">Next, join the WIN10 computer to the Azure AD tenant of your Office 365 and EMS subscriptions.</span></span>
  
1. <span data-ttu-id="c9ace-169">Sur le bureau de l’ordinateur WIN10, cliquez sur **Démarrer > Paramètres > Comptes > Accès Professionnel ou Scolaire > Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="c9ace-169">At the desktop of the WIN10 computer, click **Start > Settings > Accounts > Access work or school > Connect**.</span></span>
    
2. <span data-ttu-id="c9ace-170">Dans la boîte de dialogue **Configurer un compte professionnel ou scolaire**, cliquez sur **Joindre cet appareil à Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="c9ace-170">In the **Set up a work or school account** dialog box, click **Join this device to Azure Active Directory**.</span></span>
    
3. <span data-ttu-id="c9ace-171">Dans **Compte professionnel ou scolaire**, saisissez le nom de compte Administrateur général de votre abonnement Office 365, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="c9ace-171">In **Work or school account**, type the global administrator account name of your Office 365 subscription, and then click **Next**.</span></span>
    
4. <span data-ttu-id="c9ace-172">Dans **Saisie du mot de passe**, saisissez le mot de passe de votre compte Administrateur général, puis cliquez sur **Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="c9ace-172">In **Enter password**, type the password for your global administrator account, and then click **Sign in**.</span></span>
    
5. <span data-ttu-id="c9ace-173">Lorsque vous devez confirmer qu’il s’agit bien de votre organisation, cliquez sur **Joindre**, puis sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="c9ace-173">When prompted to make sure this is your organization, click **Join**, and then click **Done**.</span></span>
    
6. <span data-ttu-id="c9ace-174">Fermez la fenêtre Paramètres.</span><span class="sxs-lookup"><span data-stu-id="c9ace-174">Close the settings window.</span></span>
    
<span data-ttu-id="c9ace-175">Ensuite, installez Office 365 ProPlus sur l’ordinateur WIN10.</span><span class="sxs-lookup"><span data-stu-id="c9ace-175">Next, install Office 365 ProPlus on the WIN10 computer.</span></span>
  
1. <span data-ttu-id="c9ace-176">Ouvrez le navigateur Microsoft Edge et connectez-vous au portail Office à l’aide de vos informations d’identification de compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="c9ace-176">Open the Microsoft Edge browser and sign in to the Office 365 portal with your global administrator account credentials.</span></span> <span data-ttu-id="c9ace-177">Pour obtenir de l’aide, consultez [Où se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="c9ace-177">For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="c9ace-178">Dans l’onglet **Accueil Microsoft Office**, cliquez sur **Installer Office 2016**.</span><span class="sxs-lookup"><span data-stu-id="c9ace-178">On the **Microsoft Office Home** tab, click **Install Office 2016**.</span></span>
    
3. <span data-ttu-id="c9ace-179">Lorsque vous êtes invité à décider de l’action à effectuer, cliquez sur **Exécuter**, puis sur **Oui** pour **Contrôle de compte d’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="c9ace-179">When prompted with what to do, click **Run**, and then click **Yes** for **User Account Control**.</span></span>
    
4. <span data-ttu-id="c9ace-p114">Attendez qu’Office termine l’installation. Lorsque le message **Vous voilà prêt !** s’affiche, cliquez deux fois sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="c9ace-p114">Wait for Office to complete its installation. When you see **You're all set!**, click **Close** twice.</span></span>
    
<span data-ttu-id="c9ace-182">La figure 3 indique l’environnement obtenu, incluant l’ordinateur WIN10 qui a :</span><span class="sxs-lookup"><span data-stu-id="c9ace-182">Figure 3 shows your resulting environment, which includes the WIN10 computer that has:</span></span>

- <span data-ttu-id="c9ace-183">rejoint le client Azure AD de vos abonnements Office 365 et EMS ;</span><span class="sxs-lookup"><span data-stu-id="c9ace-183">Joined the Azure AD tenant of your Office 365 and EMS subscriptions.</span></span>
- <span data-ttu-id="c9ace-184">été inscrit en tant que périphérique Azure AD dans Intune (EMS) ;</span><span class="sxs-lookup"><span data-stu-id="c9ace-184">Enrolled as an Azure AD device in Intune (EMS).</span></span>
- <span data-ttu-id="c9ace-185">installé Office 365 ProPlus.</span><span class="sxs-lookup"><span data-stu-id="c9ace-185">Has Office 365 ProPlus installed.</span></span>
  
<span data-ttu-id="c9ace-186">**Figure 3 : Configuration finale de l’environnement de test Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="c9ace-186">**Figure 3: The final configuration of the Microsoft 365 test environment**</span></span>


![Phase 4 de l’environnement de test Microsoft 365 Entreprise](media/lightweight-base-configuration-microsoft-365-enterprise/Phase4.png)
  
<span data-ttu-id="c9ace-188">Vous êtes désormais prêt à profiter des fonctionnalités supplémentaires de [Microsoft 365 Entreprise](https://www.microsoft.com/microsoft-365/enterprise).</span><span class="sxs-lookup"><span data-stu-id="c9ace-188">You are now ready to experiment with additional features of [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="c9ace-189">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="c9ace-189">Next steps</span></span>

<span data-ttu-id="c9ace-190">Découvrez les nouveaux ensembles de guides pour les tests de laboratoire :</span><span class="sxs-lookup"><span data-stu-id="c9ace-190">Explore these additional sets of Test Lab Guides:</span></span>
  
- [<span data-ttu-id="c9ace-191">Identité</span><span class="sxs-lookup"><span data-stu-id="c9ace-191">Identity</span></span>](m365-enterprise-test-lab-guides.md#identity)
- [<span data-ttu-id="c9ace-192">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="c9ace-192">Mobile device management</span></span>](m365-enterprise-test-lab-guides.md#mobile-device-management)
- [<span data-ttu-id="c9ace-193">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="c9ace-193">Information protection</span></span>](m365-enterprise-test-lab-guides.md#information-protection)
   

## <a name="see-also"></a><span data-ttu-id="c9ace-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9ace-194">See also</span></span>

[<span data-ttu-id="c9ace-195">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="c9ace-195">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="c9ace-196">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="c9ace-196">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="c9ace-197">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="c9ace-197">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
