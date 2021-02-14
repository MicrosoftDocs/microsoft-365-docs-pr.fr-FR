---
title: Connecter un réseau local à Microsoft Azure Virtual Network
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/21/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
f1.keywords:
- CSH
ms.custom:
- Ent_Solutions
- seo-marvel-apr2020
ms.assetid: 81190961-5454-4a5c-8b0e-6ae75b9fb035
description: 'Résumé : Découvrez comment configurer un réseau virtuel Azure intersites pour les charges de travail de serveur Office avec une connexion VPN de site à site.'
ms.openlocfilehash: cddb9cfcff02f91ef76f989b87e9dda049cc1b08
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46695820"
---
# <a name="connect-an-on-premises-network-to-a-microsoft-azure-virtual-network"></a><span data-ttu-id="2547f-103">Connecter un réseau local à Microsoft Azure Virtual Network</span><span class="sxs-lookup"><span data-stu-id="2547f-103">Connect an on-premises network to a Microsoft Azure virtual network</span></span>

<span data-ttu-id="2547f-104">Un réseau virtuel Azure entre différents locaux est connecté à votre réseau local, étendant ainsi votre réseau pour inclure des sous-réseaux et machines virtuelles hébergés dans les services d’infrastructure Azure.</span><span class="sxs-lookup"><span data-stu-id="2547f-104">A cross-premises Azure virtual network is connected to your on-premises network, extending your network to include subnets and virtual machines hosted in Azure infrastructure services.</span></span> <span data-ttu-id="2547f-105">Cette connexion permet aux ordinateurs de votre réseau local d’accéder directement aux machines virtuelles dans Azure et inversement.</span><span class="sxs-lookup"><span data-stu-id="2547f-105">This connection lets computers on your on-premises network to directly access virtual machines in Azure and vice versa.</span></span> 

<span data-ttu-id="2547f-p102">Par exemple, un serveur de synchronisation d’annuaires s’exécutant sur une machine virtuelle Azure doit interroger vos contrôleurs de domaine locaux pour obtenir des modifications apportées aux comptes et synchroniser ces modifications avec votre abonnement Microsoft 365. Cet article vous montre comment configurer un réseau virtuel Azure entre sites à l’aide d’une connexion vpn (virtual private network) de site à site prête à héberger des machines virtuelles Azure.</span><span class="sxs-lookup"><span data-stu-id="2547f-p102">For example, a directory synchronization server running on an Azure virtual machine needs to query your on-premises domain controllers for changes to accounts and synchronize those changes with your Microsoft 365 subscription. This article shows you how to set up a cross-premises Azure virtual network using a site-to-site virtual private network (VPN) connection that is ready to host Azure virtual machines.</span></span>

## <a name="configure-a-cross-premises-azure-virtual-network"></a><span data-ttu-id="2547f-108">Configurer un réseau virtuel Azure entre plusieurs locaux</span><span class="sxs-lookup"><span data-stu-id="2547f-108">Configure a cross-premises Azure virtual network</span></span>

<span data-ttu-id="2547f-p103">Vos machines virtuelles dans Azure n'ont pas besoin d'être isolées de votre environnement local. Pour connecter des machines virtuelles Azure à des ressources réseau locales, vous devez configurer un réseau virtuel Azure local. Le diagramme suivant montre les composants requis pour déployer un réseau virtuel Azure entre différents locaux avec une machine virtuelle dans Azure.</span><span class="sxs-lookup"><span data-stu-id="2547f-p103">Your virtual machines in Azure don't have to be isolated from your on-premises environment. To connect Azure virtual machines to your on-premises network resources, you must configure a cross-premises Azure virtual network. The following diagram shows the required components to deploy a cross-premises Azure virtual network with a virtual machine in Azure.</span></span>
  
![Réseau local connecté à Microsoft Azure via une connexion VPN de site à site](../media/86ab63a6-bfae-4f75-8470-bd40dff123ac.png)
 
<span data-ttu-id="2547f-p104">Dans le diagramme, il existe deux réseaux connectés par une connexion VPN de site à site : le réseau local et le réseau virtuel Azure. La connexion VPN de site à site est :</span><span class="sxs-lookup"><span data-stu-id="2547f-p104">In the diagram, there are two networks connected by a site-to-site VPN connection: the on-premises network and the Azure virtual network. The site-to-site VPN connection is:</span></span>

- <span data-ttu-id="2547f-115">entre deux points de terminaison qui sont adressables et se trouvent sur l’Internet public ;</span><span class="sxs-lookup"><span data-stu-id="2547f-115">Between two endpoints that are addressable and located on the public Internet.</span></span>
- <span data-ttu-id="2547f-116">terminée par un appareil VPN sur le réseau local et une passerelle VPN Azure sur le réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="2547f-116">Terminated by a VPN device on the on-premises network and an Azure VPN gateway on the Azure virtual network.</span></span>

<span data-ttu-id="2547f-p105">Le réseau virtuel Azure héberge des machines virtuelles. Le trafic réseau provenant des machines virtuelles sur le réseau virtuel Azure est transféré vers la passerelle VPN, qui transfère ensuite le trafic via la connexion VPN de site à site à l’appareil VPN sur le réseau local. L’infrastructure de routage sur le réseau local transfère par la suite le trafic à sa destination.</span><span class="sxs-lookup"><span data-stu-id="2547f-p105">The Azure virtual network hosts virtual machines. Network traffic originating from virtual machines on the Azure virtual network gets forwarded to the VPN gateway, which then forwards the traffic across the site-to-site VPN connection to the VPN device on the on-premises network. The routing infrastructure of the on-premises network then forwards the traffic to its destination.</span></span>

>[!Note]
><span data-ttu-id="2547f-p106">Vous pouvez aussi utiliser [ExpressRoute](https://azure.microsoft.com/services/expressroute/), une connexion directe entre votre organisation et le réseau de Microsoft. Le trafic sur ExpressRoute ne passe pas sur l’Internet public. Cet article ne décrit pas l’utilisation d’ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2547f-p106">You can also use [ExpressRoute](https://azure.microsoft.com/services/expressroute/), which is a direct connection between your organization and Microsoft's network. Traffic over ExpressRoute does not travel over the public Internet. This article does not describe the use of ExpressRoute.</span></span>
>
  
<span data-ttu-id="2547f-123">Pour configurer la connexion VPN entre votre réseau Azure Virtual Network et votre réseau local, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="2547f-123">To set up the VPN connection between your Azure virtual network and your on-premises network, follow these steps:</span></span> 
  
1. <span data-ttu-id="2547f-124">**Local :** Définissez et créez un itinéraire réseau local pour l'espace d'adressage du réseau virtuel Azure qui pointe vers votre périphérique VPN local.</span><span class="sxs-lookup"><span data-stu-id="2547f-124">**On-premises:** Define and create an on-premises network route for the address space of the Azure virtual network that points to your on-premises VPN device.</span></span>
    
2. <span data-ttu-id="2547f-125">**Microsoft Azure** : Créez un réseau virtuel Azure avec une connexion VPN de site à site.</span><span class="sxs-lookup"><span data-stu-id="2547f-125">**Microsoft Azure:** Create an Azure virtual network with a site-to-site VPN connection.</span></span> 
    
3. <span data-ttu-id="2547f-126">**Local :** Configurez votre périphérique VPN matériel ou logiciel local pour marquer la fin de la connexion VPN en utilisant la sécurité du protocole Internet (IPsec).</span><span class="sxs-lookup"><span data-stu-id="2547f-126">**On premises:** Configure your on-premises hardware or software VPN device to terminate the VPN connection, which uses Internet Protocol security (IPsec).</span></span>
    
<span data-ttu-id="2547f-127">Après avoir établi la connexion VPN de site à site, vous ajoutez des machines virtuelles Azure aux sous-réseaux du réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="2547f-127">After you establish the site-to-site VPN connection, you add Azure virtual machines to the subnets of the virtual network.</span></span>
  
## <a name="plan-your-azure-virtual-network"></a><span data-ttu-id="2547f-128">Planification de votre réseau Azure Virtual Network</span><span class="sxs-lookup"><span data-stu-id="2547f-128">Plan your Azure virtual network</span></span>
<a name="PlanningVirtual"></a>

### <a name="prerequisites"></a><span data-ttu-id="2547f-129">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="2547f-129">Prerequisites</span></span>
<a name="Prerequisites"></a>

- <span data-ttu-id="2547f-p107">Un abonnement Azure. Pour plus d’informations sur les abonnements Azure, accédez à la [page décrivant comment acheter Azure](https://azure.microsoft.com/pricing/purchase-options/).</span><span class="sxs-lookup"><span data-stu-id="2547f-p107">An Azure subscription. For information about Azure subscriptions, go to the [How To Buy Azure page](https://azure.microsoft.com/pricing/purchase-options/).</span></span>
    
- <span data-ttu-id="2547f-132">Un espace d’adressage IPv4 privé disponible à affecter au réseau virtuel et à ses sous-réseaux, avec suffisamment d’espace pour leur croissance afin d’accueillir le nombre de machines virtuelles nécessaires maintenant et à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="2547f-132">An available private IPv4 address space to assign to the virtual network and its subnets, with sufficient room for growth to accommodate the number of virtual machines needed now and in the future.</span></span>
    
- <span data-ttu-id="2547f-p108">Un périphérique VPN disponible dans votre réseau local pour marquer la fin de la connexion VPN de site à site qui prend en charge la configuration requise IPsec. Pour plus d'informations, voir [À propos des périphériques VPN pour les connexions de réseau virtuel de site à site](https://go.microsoft.com/fwlink/p/?LinkId=393093).</span><span class="sxs-lookup"><span data-stu-id="2547f-p108">An available VPN device in your on-premises network to terminate the site-to-site VPN connection that supports the requirements for IPsec. For more information, see [About VPN devices for site-to-site virtual network connections](https://go.microsoft.com/fwlink/p/?LinkId=393093).</span></span>
    
- <span data-ttu-id="2547f-135">La modification de votre infrastructure de routage pour que le trafic routé vers l'espace d'adressage du réseau virtuel Azure soit acheminé vers le périphérique VPN qui héberge la connexion VPN de site à site.</span><span class="sxs-lookup"><span data-stu-id="2547f-135">Changes to your routing infrastructure so that traffic routed to the address space of the Azure virtual network gets forwarded to the VPN device that hosts the site-to-site VPN connection.</span></span>
    
- <span data-ttu-id="2547f-136">Un proxy web fournissant un accès à Internet aux ordinateurs connectés au réseau local et au réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="2547f-136">A web proxy that gives computers that are connected to the on-premises network and the Azure virtual network access to the Internet.</span></span>
    
### <a name="solution-architecture-design-assumptions"></a><span data-ttu-id="2547f-137">Hypothèses en matière de conception de l’architecture de la solution</span><span class="sxs-lookup"><span data-stu-id="2547f-137">Solution architecture design assumptions</span></span>

<span data-ttu-id="2547f-138">La liste suivante répertorie les choix de conception qui ont été faits pour l’architecture de cette solution.</span><span class="sxs-lookup"><span data-stu-id="2547f-138">The following list represents the design choices that have been made for this solution architecture.</span></span> 
  
- <span data-ttu-id="2547f-p109">Cette solution utilise un seul réseau virtuel Azure avec une connexion VPN de site à site. Le réseau virtuel Azure héberge un sous-réseau unique qui contient plusieurs machines virtuelles.</span><span class="sxs-lookup"><span data-stu-id="2547f-p109">This solution uses a single Azure virtual network with a site-to-site VPN connection. The Azure virtual network hosts a single subnet that can contain multiple virtual machines.</span></span> 
    
- <span data-ttu-id="2547f-p110">Vous pouvez utiliser le service Routage et accès distant (RRAS) dans Windows Server 2016 ou Windows Server 2012 pour établir une connexion VPN de site à site IPsec entre le réseau local et le réseau virtuel Azure. Vous pouvez également utiliser d'autres options, telles que des périphériques VPN Cisco ou Juniper Networks.</span><span class="sxs-lookup"><span data-stu-id="2547f-p110">You can use the Routing and Remote Access Service (RRAS) in Windows Server 2016 or Windows Server 2012 to establish an IPsec site-to-site VPN connection between the on-premises network and the Azure virtual network. You can also use other options, such as Cisco or Juniper Networks VPN devices.</span></span>
    
- <span data-ttu-id="2547f-p111">Le réseau local peut tout de même disposer de services réseau, tels qu’un AD DS (Active Directory Domain Services), un système DNS (Domain Name System) et des serveurs proxy. Selon vos besoins, il peut être utile de placer certaines de ces ressources réseau dans le réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="2547f-p111">The on-premises network might still have network services like Active Directory Domain Services (AD DS), Domain Name System (DNS), and proxy servers. Depending on your requirements, it might be beneficial to place some of these network resources in the Azure virtual network.</span></span>
    
<span data-ttu-id="2547f-p112">Pour un réseau virtuel Azure existant comportant un ou plusieurs sous-réseaux, déterminez s'il reste assez d'espace d'adressage pour qu'un sous-réseau supplémentaire puisse héberger les machines virtuelles dont vous avez besoin. Si vous n'avez pas assez d'espace d'adressage restant pour un sous-réseau supplémentaire, créez un réseau virtuel supplémentaire qui dispose de sa propre connexion VPN de site à site.</span><span class="sxs-lookup"><span data-stu-id="2547f-p112">For an existing Azure virtual network with one or more subnets, determine whether there is remaining address space for an additional subnet to host your needed virtual machines, based on your requirements. If you don't have remaining address space for an additional subnet, create an additional virtual network that has its own site-to-site VPN connection.</span></span>
  
### <a name="plan-the-routing-infrastructure-changes-for-the-azure-virtual-network"></a><span data-ttu-id="2547f-147">Planification des modifications d’infrastructure de routage pour le réseau virtuel Azure</span><span class="sxs-lookup"><span data-stu-id="2547f-147">Plan the routing infrastructure changes for the Azure virtual network</span></span>

<span data-ttu-id="2547f-148">Vous devez configurer votre infrastructure de routage locale pour acheminer le trafic destiné à l'espace d'adressage du réseau virtuel Azure au périphérique VPN local qui héberge la connexion VPN de site à site.</span><span class="sxs-lookup"><span data-stu-id="2547f-148">You must configure your on-premises routing infrastructure to forward traffic destined for the address space of the Azure virtual network to the on-premises VPN device that is hosting the site-to-site VPN connection.</span></span>
  
<span data-ttu-id="2547f-149">La méthode de mise à jour exacte de votre infrastructure de routage dépend de votre gestion des informations de routage, c’est-à-dire :</span><span class="sxs-lookup"><span data-stu-id="2547f-149">The exact method of updating your routing infrastructure depends on how you manage routing information, which can be:</span></span>
  
- <span data-ttu-id="2547f-150">Des mises à jour de la table de routage en fonction de la configuration manuelle.</span><span class="sxs-lookup"><span data-stu-id="2547f-150">Routing table updates based on manual configuration.</span></span>
    
- <span data-ttu-id="2547f-151">Des mises à jour de la table de routage en fonction des protocoles de routage, tels que le protocole RIP (Routing Information Protocol) ou le protocole OSPF (Open Shortest Path First).</span><span class="sxs-lookup"><span data-stu-id="2547f-151">Routing table updates based on routing protocols, such as Routing Information Protocol (RIP) or Open Shortest Path First (OSPF).</span></span>
    
<span data-ttu-id="2547f-152">Consultez votre spécialiste du routage pour vous assurer que le trafic destiné au réseau virtuel Azure est transféré au périphérique VPN local.</span><span class="sxs-lookup"><span data-stu-id="2547f-152">Consult with your routing specialist to make sure that traffic destined for the Azure virtual network is forwarded to the on-premises VPN device.</span></span>
  
### <a name="plan-for-firewall-rules-for-traffic-to-and-from-the-on-premises-vpn-device"></a><span data-ttu-id="2547f-153">Planification des règles de pare-feu pour le trafic vers et depuis le périphérique VPN local</span><span class="sxs-lookup"><span data-stu-id="2547f-153">Plan for firewall rules for traffic to and from the on-premises VPN device</span></span>

<span data-ttu-id="2547f-154">Si votre périphérique VPN se trouve sur un réseau de périmètre qui dispose d’un pare-feu entre le réseau de périmètre et Internet, vous devrez peut-être configurer le pare-feu pour que les règles suivantes autorisent la connexion VPN de site à site.</span><span class="sxs-lookup"><span data-stu-id="2547f-154">If your VPN device is on a perimeter network that has a firewall between the perimeter network and the Internet, you might have to configure the firewall for the following rules to allow the site-to-site VPN connection.</span></span>
  
- <span data-ttu-id="2547f-155">Trafic vers le périphérique VPN (entrant, à partir d’Internet) :</span><span class="sxs-lookup"><span data-stu-id="2547f-155">Traffic to the VPN device (incoming from the Internet):</span></span>
    
  - <span data-ttu-id="2547f-156">Adresse IP de destination du périphérique VPN et protocole IP 50</span><span class="sxs-lookup"><span data-stu-id="2547f-156">Destination IP address of the VPN device and IP protocol 50</span></span>
    
  - <span data-ttu-id="2547f-157">Adresse IP de destination du périphérique VPN et port 500 de destination UDP</span><span class="sxs-lookup"><span data-stu-id="2547f-157">Destination IP address of the VPN device and UDP destination port 500</span></span>
    
  - <span data-ttu-id="2547f-158">Adresse IP de destination du périphérique VPN et port 4500 de destination UDP</span><span class="sxs-lookup"><span data-stu-id="2547f-158">Destination IP address of the VPN device and UDP destination port 4500</span></span>
    
- <span data-ttu-id="2547f-159">Trafic provenant du périphérique VPN (sortant, en direction d’Internet) :</span><span class="sxs-lookup"><span data-stu-id="2547f-159">Traffic from the VPN device (outgoing to the Internet):</span></span>
    
  - <span data-ttu-id="2547f-160">Adresse IP source du périphérique VPN et protocole IP 50</span><span class="sxs-lookup"><span data-stu-id="2547f-160">Source IP address of the VPN device and IP protocol 50</span></span>
    
  - <span data-ttu-id="2547f-161">Adresse IP source du périphérique VPN et port 500 source UDP</span><span class="sxs-lookup"><span data-stu-id="2547f-161">Source IP address of the VPN device and UDP source port 500</span></span>
    
  - <span data-ttu-id="2547f-162">Adresse IP source du périphérique VPN et port 4500 source UDP</span><span class="sxs-lookup"><span data-stu-id="2547f-162">Source IP address of the VPN device and UDP source port 4500</span></span>
    
### <a name="plan-for-the-private-ip-address-space-of-the-azure-virtual-network"></a><span data-ttu-id="2547f-163">Planification de l’espace d’adressage IP privé du réseau virtuel Azure</span><span class="sxs-lookup"><span data-stu-id="2547f-163">Plan for the private IP address space of the Azure virtual network</span></span>

<span data-ttu-id="2547f-164">L'espace d'adressage IP privé du réseau virtuel Azure doit pouvoir prendre en charge les adresses utilisées par Azure pour héberger le réseau virtuel et au moins un sous-réseau disposant de suffisamment d'adresses pour vos machines virtuelles Azure.</span><span class="sxs-lookup"><span data-stu-id="2547f-164">The private IP address space of the Azure virtual network must be able to accommodate addresses used by Azure to host the virtual network and with at least one subnet that has enough addresses for your Azure virtual machines.</span></span>
  
<span data-ttu-id="2547f-165">Pour déterminer le nombre d’adresses nécessaires pour le sous-réseau, comptez le nombre de machines virtuelles dont vous avez besoin maintenant, estimez la croissance future, puis utilisez le tableau suivant pour déterminer la taille du sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="2547f-165">To determine the number of addresses needed for the subnet, count the number of virtual machines that you need now, estimate for future growth, and then use the following table to determine the size of the subnet.</span></span>
  
|<span data-ttu-id="2547f-166">**Nombre de machines virtuelles nécessaires**</span><span class="sxs-lookup"><span data-stu-id="2547f-166">**Number of virtual machines needed**</span></span>|<span data-ttu-id="2547f-167">**Nombre de bits d'hôte requis**</span><span class="sxs-lookup"><span data-stu-id="2547f-167">**Number of host bits needed**</span></span>|<span data-ttu-id="2547f-168">**Taille du sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="2547f-168">**Size of the subnet**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2547f-169">1-3</span><span class="sxs-lookup"><span data-stu-id="2547f-169">1-3</span></span>  <br/> |<span data-ttu-id="2547f-170">3</span><span class="sxs-lookup"><span data-stu-id="2547f-170">3</span></span>  <br/> |<span data-ttu-id="2547f-171">/29</span><span class="sxs-lookup"><span data-stu-id="2547f-171">/29</span></span>  <br/> |
|<span data-ttu-id="2547f-172">4-11</span><span class="sxs-lookup"><span data-stu-id="2547f-172">4-11</span></span>  <br/> |<span data-ttu-id="2547f-173">4</span><span class="sxs-lookup"><span data-stu-id="2547f-173">4</span></span>  <br/> |<span data-ttu-id="2547f-174">/28</span><span class="sxs-lookup"><span data-stu-id="2547f-174">/28</span></span>  <br/> |
|<span data-ttu-id="2547f-175">12-27</span><span class="sxs-lookup"><span data-stu-id="2547f-175">12-27</span></span>  <br/> |<span data-ttu-id="2547f-176">5</span><span class="sxs-lookup"><span data-stu-id="2547f-176">5</span></span>  <br/> |<span data-ttu-id="2547f-177">/27</span><span class="sxs-lookup"><span data-stu-id="2547f-177">/27</span></span>  <br/> |
|<span data-ttu-id="2547f-178">28-59</span><span class="sxs-lookup"><span data-stu-id="2547f-178">28-59</span></span>  <br/> |<span data-ttu-id="2547f-179">6</span><span class="sxs-lookup"><span data-stu-id="2547f-179">6</span></span>  <br/> |<span data-ttu-id="2547f-180">/26</span><span class="sxs-lookup"><span data-stu-id="2547f-180">/26</span></span>  <br/> |
|<span data-ttu-id="2547f-181">60-123</span><span class="sxs-lookup"><span data-stu-id="2547f-181">60-123</span></span>  <br/> |<span data-ttu-id="2547f-182">7</span><span class="sxs-lookup"><span data-stu-id="2547f-182">7</span></span>  <br/> |<span data-ttu-id="2547f-183">/25</span><span class="sxs-lookup"><span data-stu-id="2547f-183">/25</span></span>  <br/> |
   
### <a name="planning-worksheet-for-configuring-your-azure-virtual-network"></a><span data-ttu-id="2547f-184">Planification de la feuille de travail pour la configuration de votre réseau virtuel Azure</span><span class="sxs-lookup"><span data-stu-id="2547f-184">Planning worksheet for configuring your Azure virtual network</span></span>
<span data-ttu-id="2547f-185"><a name="worksheet"> </a></span><span class="sxs-lookup"><span data-stu-id="2547f-185"><a name="worksheet"> </a></span></span>

<span data-ttu-id="2547f-186">Avant de créer un réseau virtuel Azure pour héberger des machines virtuelles, vous devez déterminer les paramètres nécessaires dans les tableaux suivants.</span><span class="sxs-lookup"><span data-stu-id="2547f-186">Before you create an Azure virtual network to host virtual machines, you must determine the settings needed in the following tables.</span></span>
  
<span data-ttu-id="2547f-187">Pour les paramètres du réseau virtuel, remplissez le tableau V.</span><span class="sxs-lookup"><span data-stu-id="2547f-187">For the settings of the virtual network, fill in Table V.</span></span>
  
 <span data-ttu-id="2547f-188">**Tableau V : configuration de réseau virtuel entre différents locaux**</span><span class="sxs-lookup"><span data-stu-id="2547f-188">**Table V: Cross-premises virtual network configuration**</span></span>
  
|<span data-ttu-id="2547f-189">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2547f-189">**Item**</span></span>|<span data-ttu-id="2547f-190">**Élément Configuration**</span><span class="sxs-lookup"><span data-stu-id="2547f-190">**Configuration element**</span></span>|<span data-ttu-id="2547f-191">**Description**</span><span class="sxs-lookup"><span data-stu-id="2547f-191">**Description**</span></span>|<span data-ttu-id="2547f-192">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="2547f-192">**Value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2547f-193">1.</span><span class="sxs-lookup"><span data-stu-id="2547f-193">1.</span></span>  <br/> |<span data-ttu-id="2547f-194">Nom du réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="2547f-194">Virtual network name</span></span>  <br/> |<span data-ttu-id="2547f-195">Nom à affecter au réseau virtuel Azure (par exemple, DirSyncNet).</span><span class="sxs-lookup"><span data-stu-id="2547f-195">A name to assign to the Azure virtual network (example DirSyncNet).</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png) |
|<span data-ttu-id="2547f-197">2.</span><span class="sxs-lookup"><span data-stu-id="2547f-197">2.</span></span>  <br/> |<span data-ttu-id="2547f-198">Emplacement du réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="2547f-198">Virtual network location</span></span>  <br/> |<span data-ttu-id="2547f-199">Centre de données Azure qui contiendra le réseau virtuel (par exemple, Ouest des États-Unis).</span><span class="sxs-lookup"><span data-stu-id="2547f-199">The Azure datacenter that will contain the virtual network (such as West US).</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png)  <br/> |
|<span data-ttu-id="2547f-201">3.</span><span class="sxs-lookup"><span data-stu-id="2547f-201">3.</span></span>  <br/> |<span data-ttu-id="2547f-202">Adresse IP du périphérique VPN</span><span class="sxs-lookup"><span data-stu-id="2547f-202">VPN device IP address</span></span>  <br/> |<span data-ttu-id="2547f-p113">Adresse IPv4 publique de l’interface de votre périphérique VPN sur Internet. Renseignez-vous auprès de votre service informatique pour déterminer cette adresse.</span><span class="sxs-lookup"><span data-stu-id="2547f-p113">The public IPv4 address of your VPN device's interface on the Internet. Work with your IT department to determine this address.</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png)  <br/> |
|<span data-ttu-id="2547f-206">4.</span><span class="sxs-lookup"><span data-stu-id="2547f-206">4.</span></span>  <br/> |<span data-ttu-id="2547f-207">Espace d’adressage du réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="2547f-207">Virtual network address space</span></span>  <br/> |<span data-ttu-id="2547f-p114">Espace d’adressage (défini dans un préfixe d’adresse privée unique) pour le réseau virtuel. Renseignez-vous auprès de votre service informatique pour déterminer cet espace d’adressage. L’espace d’adressage doit être au format de routage CIDR (Classless Interdomain Routing), également appelé format de préfixe de réseau. Par exemple, 10.24.64.0/20.</span><span class="sxs-lookup"><span data-stu-id="2547f-p114">The address space (defined in a single private address prefix) for the virtual network. Work with your IT department to determine this address space. The address space should be in Classless Interdomain Routing (CIDR) format, also known as network prefix format. An example is 10.24.64.0/20.</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png) <br/> |
|<span data-ttu-id="2547f-213">5.</span><span class="sxs-lookup"><span data-stu-id="2547f-213">5.</span></span>  <br/> |<span data-ttu-id="2547f-214">Clé partagée IPsec</span><span class="sxs-lookup"><span data-stu-id="2547f-214">IPsec shared key</span></span>  <br/> |<span data-ttu-id="2547f-p115">Chaîne alphanumérique aléatoire de 32 caractères, qui sera utilisée pour authentifier les deux côtés de la connexion VPN de site à site. Renseignez-vous auprès de votre service informatique ou de sécurité pour déterminer la valeur de cette clé, puis stockez-la dans un emplacement sécurisé. Vous pouvez également consulter la page relative à la [création d'une chaîne aléatoire pour une clé prépartagée IPsec](https://social.technet.microsoft.com/wiki/contents/articles/32330.create-a-random-string-for-an-ipsec-preshared-key.aspx).</span><span class="sxs-lookup"><span data-stu-id="2547f-p115">A 32-character random, alphanumeric string that will be used to authenticate both sides of the site-to-site VPN connection. Work with your IT or security department to determine this key value and then store it in a secure location. Alternately, see [Create a random string for an IPsec preshared key](https://social.technet.microsoft.com/wiki/contents/articles/32330.create-a-random-string-for-an-ipsec-preshared-key.aspx).  </span></span><br/> |![ligne](../media/Common-Images/TableLine.png) <br/> |
   
<span data-ttu-id="2547f-219">Remplissez le tableau S pour les sous-réseaux de cette solution.</span><span class="sxs-lookup"><span data-stu-id="2547f-219">Fill in Table S for the subnets of this solution.</span></span>
  
- <span data-ttu-id="2547f-p116">Pour le premier sous-réseau, déterminez un espace d'adressage 28 bits (avec une longueur de préfixe de /28) pour le sous-réseau de passerelle Azure. Voir la rubrique sur le [calcul de l'espace d'adressage de sous-réseau de passerelle pour les réseaux virtuels Azure](https://blogs.technet.microsoft.com/solutions_advisory_board/2016/12/01/calculating-the-gateway-subnet-address-space-for-azure-virtual-networks/) pour savoir comment déterminer cet espace d'adressage.</span><span class="sxs-lookup"><span data-stu-id="2547f-p116">For the first subnet, determine a 28-bit address space (with a /28 prefix length) for the Azure gateway subnet. See [Calculating the gateway subnet address space for Azure virtual networks](https://blogs.technet.microsoft.com/solutions_advisory_board/2016/12/01/calculating-the-gateway-subnet-address-space-for-azure-virtual-networks/) for information about how to determine this address space.</span></span>
    
- <span data-ttu-id="2547f-222">Pour le deuxième sous-réseau, indiquez un nom convivial, un espace d’adressage IP unique fondé sur l’espace d’adressage de réseau virtuel et une description de l’objectif.</span><span class="sxs-lookup"><span data-stu-id="2547f-222">For the second subnet, specify a friendly name, a single IP address space based on the virtual network address space, and a descriptive purpose.</span></span>
    
<span data-ttu-id="2547f-p117">Renseignez-vous auprès de votre service informatique pour déterminer ces espaces d’adressage à partir de l’espace d’adressage de réseau virtuel. Les deux espaces d’adressage doivent être au format CIDR.</span><span class="sxs-lookup"><span data-stu-id="2547f-p117">Work with your IT department to determine these address spaces from the virtual network address space. Both address spaces should be in CIDR format.</span></span>
  
 <span data-ttu-id="2547f-225">**Tableau S : sous-réseaux dans le réseau virtuel**</span><span class="sxs-lookup"><span data-stu-id="2547f-225">**Table S: Subnets in the virtual network**</span></span>
  
|<span data-ttu-id="2547f-226">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2547f-226">**Item**</span></span>|<span data-ttu-id="2547f-227">**Nom du sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="2547f-227">**Subnet name**</span></span>|<span data-ttu-id="2547f-228">**Espace d'adressage de sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="2547f-228">**Subnet address space**</span></span>|<span data-ttu-id="2547f-229">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="2547f-229">**Purpose**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2547f-230">1.</span><span class="sxs-lookup"><span data-stu-id="2547f-230">1.</span></span>  <br/> |<span data-ttu-id="2547f-231">GatewaySubnet</span><span class="sxs-lookup"><span data-stu-id="2547f-231">GatewaySubnet</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png)  <br/> |<span data-ttu-id="2547f-233">Sous-réseau utilisé par la passerelle Azure.</span><span class="sxs-lookup"><span data-stu-id="2547f-233">The subnet used by the Azure gateway.</span></span>  <br/> |
|<span data-ttu-id="2547f-234">2.</span><span class="sxs-lookup"><span data-stu-id="2547f-234">2.</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png)  <br/> |![ligne](../media/Common-Images/TableLine.png)  <br/> |![ligne](../media/Common-Images/TableLine.png)  <br/> |
   
<span data-ttu-id="2547f-p118">Concernant les serveurs DNS locaux qui doivent être utilisés par les machines virtuelles du réseau virtuel, remplissez le tableau D. Donnez un nom convivial et une adresse IP unique à chaque serveur DNS. Ce nom convivial n’a pas besoin de correspondre au nom d’hôte ou au nom de l’ordinateur du serveur DNS. Notez que le tableau comporte deux entrées vides, mais vous pouvez en ajouter d’autres. Renseignez-vous auprès de votre service informatique pour déterminer cette liste.</span><span class="sxs-lookup"><span data-stu-id="2547f-p118">For the on-premises DNS servers that you want the virtual machines in the virtual network to use, fill in Table D. Give each DNS server a friendly name and a single IP address. This friendly name does not need to match the host name or computer name of the DNS server. Note that two blank entries are listed, but you can add more. Work with your IT department to determine this list.</span></span>
  
 <span data-ttu-id="2547f-242">**Tableau D : serveurs DNS locaux**</span><span class="sxs-lookup"><span data-stu-id="2547f-242">**Table D: On-premises DNS servers**</span></span>
  
|<span data-ttu-id="2547f-243">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2547f-243">**Item**</span></span>|<span data-ttu-id="2547f-244">**Nom convivial du serveur DNS**</span><span class="sxs-lookup"><span data-stu-id="2547f-244">**DNS server friendly name**</span></span>|<span data-ttu-id="2547f-245">**Adresse IP du serveur DNS**</span><span class="sxs-lookup"><span data-stu-id="2547f-245">**DNS server IP address**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2547f-246">1.</span><span class="sxs-lookup"><span data-stu-id="2547f-246">1.</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png)  <br/> |![ligne](../media/Common-Images/TableLine.png)  <br/> |
|<span data-ttu-id="2547f-249">2.</span><span class="sxs-lookup"><span data-stu-id="2547f-249">2.</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png)  <br/> |![ligne](../media/Common-Images/TableLine.png)  <br/> |
   
<span data-ttu-id="2547f-252">Pour acheminer les paquets du réseau virtuel Azure vers le réseau de votre organisation par le biais de la connexion VPN de site à site, vous devez configurer le réseau virtuel avec un réseau local.</span><span class="sxs-lookup"><span data-stu-id="2547f-252">To route packets from the Azure virtual network to your organization network across the site-to-site VPN connection, you must configure the virtual network with a local network.</span></span> <span data-ttu-id="2547f-253">Ce réseau local possède la liste des espaces d’adressage (au format CIDR) pour l’ensemble des emplacements sur le réseau local de votre organisation que les machines virtuelles du réseau virtuel doivent atteindre.</span><span class="sxs-lookup"><span data-stu-id="2547f-253">This local network has a list of the address spaces (in CIDR format) for all of the locations on your organization's on-premises network that the virtual machines in the virtual network must reach.</span></span> <span data-ttu-id="2547f-254">Il peut s’agir de l’ensemble des emplacements sur le réseau local ou un sous-ensemble.</span><span class="sxs-lookup"><span data-stu-id="2547f-254">This can be all of the locations on the on-premises network or a subset.</span></span> <span data-ttu-id="2547f-255">La liste des espaces d’adressage qui définissent votre réseau local doit être unique et ne doit pas se chevaucher avec les espaces d’adressage utilisés pour ce réseau virtuel ou les autres réseaux virtuels intersites.</span><span class="sxs-lookup"><span data-stu-id="2547f-255">The list of address spaces that define your local network must be unique and must not overlap with the address spaces used for this virtual network or your other cross-premises virtual networks.</span></span>
  
<span data-ttu-id="2547f-p120">Pour l’ensemble des espaces d’adressage du réseau local, remplissez le tableau L. Notez que le tableau comporte trois entrées vides, mais vous aurez généralement besoin d’en ajouter. Renseignez-vous auprès de votre service informatique pour déterminer cette liste.</span><span class="sxs-lookup"><span data-stu-id="2547f-p120">For the set of local network address spaces, fill in Table L. Note that three blank entries are listed but you will typically need more. Work with your IT department to determine this list.</span></span>
  
 <span data-ttu-id="2547f-258">**Tableau L : préfixes d'adresse pour le réseau local**</span><span class="sxs-lookup"><span data-stu-id="2547f-258">**Table L: Address prefixes for the local network**</span></span>
  
|<span data-ttu-id="2547f-259">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2547f-259">**Item**</span></span>|<span data-ttu-id="2547f-260">**Espace d'adressage du réseau local**</span><span class="sxs-lookup"><span data-stu-id="2547f-260">**Local network address space**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2547f-261">1.</span><span class="sxs-lookup"><span data-stu-id="2547f-261">1.</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png)  <br/> |
|<span data-ttu-id="2547f-263">2.</span><span class="sxs-lookup"><span data-stu-id="2547f-263">2.</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png)  <br/> |
|<span data-ttu-id="2547f-265">3.</span><span class="sxs-lookup"><span data-stu-id="2547f-265">3.</span></span>  <br/> |![ligne](../media/Common-Images/TableLine.png)  <br/> |
   
## <a name="deployment-roadmap"></a><span data-ttu-id="2547f-267">Feuille de route de déploiement</span><span class="sxs-lookup"><span data-stu-id="2547f-267">Deployment roadmap</span></span>
<span data-ttu-id="2547f-268"><a name="DeploymentRoadmap"> </a></span><span class="sxs-lookup"><span data-stu-id="2547f-268"><a name="DeploymentRoadmap"> </a></span></span>

<span data-ttu-id="2547f-269">La création du réseau virtuel entre différents locaux et l'ajout de machines virtuelles dans Azure se composent de trois phases :</span><span class="sxs-lookup"><span data-stu-id="2547f-269">Creating the cross-premises virtual network and adding virtual machines in Azure consists of three phases:</span></span>
  
- <span data-ttu-id="2547f-270">Phase 1 : préparer votre réseau local.</span><span class="sxs-lookup"><span data-stu-id="2547f-270">Phase 1: Prepare your on-premises network.</span></span>
    
- <span data-ttu-id="2547f-271">Phase 2 : créer le réseau virtuel entre différents locaux dans Azure.</span><span class="sxs-lookup"><span data-stu-id="2547f-271">Phase 2: Create the cross-premises virtual network in Azure.</span></span>
    
- <span data-ttu-id="2547f-272">Phase 3 (facultative) : ajouter des machines virtuelles.</span><span class="sxs-lookup"><span data-stu-id="2547f-272">Phase 3 (Optional): Add virtual machines.</span></span>
    
### <a name="phase-1-prepare-your-on-premises-network"></a><span data-ttu-id="2547f-273">Phase 1 : préparer votre réseau local</span><span class="sxs-lookup"><span data-stu-id="2547f-273">Phase 1: Prepare your on-premises network</span></span>
<a name="Phase1"></a>

<span data-ttu-id="2547f-p121">Vous devez configurer votre réseau local avec un itinéraire qui pointe vers l’espace d’adressage du réseau virtuel et remet finalement le trafic qui y est destiné au routeur sur le périmètre du réseau local. Contactez votre administrateur réseau pour savoir comment ajouter l’itinéraire à l’infrastructure de routage de votre réseau local.</span><span class="sxs-lookup"><span data-stu-id="2547f-p121">You must configure your on-premises network with a route that points to and ultimately delivers traffic destined for the address space of the virtual network to the router on the edge of the on-premises network. Consult with your network administrator to determine how to add the route to the routing infrastructure of your on-premises network.</span></span>
  
<span data-ttu-id="2547f-276">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="2547f-276">Here is your resulting configuration.</span></span>
  
![Le réseau local doit disposer d’un itinéraire pour l’espace d’adressage du réseau virtuel qui pointe vers l’appareil VPN.](../media/90bab36b-cb60-4ea5-81d5-4737b696d41c.png)
  
### <a name="phase-2-create-the-cross-premises-virtual-network-in-azure"></a><span data-ttu-id="2547f-278">Phase 2 : créer le réseau virtuel entre différents locaux dans Azure</span><span class="sxs-lookup"><span data-stu-id="2547f-278">Phase 2: Create the cross-premises virtual network in Azure</span></span>
<a name="Phase2"></a>

<span data-ttu-id="2547f-p122">Tout d’abord, ouvrez une invite PowerShell Azure. Si vous n’avez pas installé Azure PowerShell, reportez-vous à l’article [Prise en main d’Azure PowerShell](https://docs.microsoft.com/powershell/azure/get-started-azureps).</span><span class="sxs-lookup"><span data-stu-id="2547f-p122">First, open an Azure PowerShell prompt. If you have not installed Azure PowerShell, see [Get started with Azure PowerShell](https://docs.microsoft.com/powershell/azure/get-started-azureps).</span></span>

 
<span data-ttu-id="2547f-281">Ensuite, connectez-vous à votre compte Azure avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="2547f-281">Next, login to your Azure account with this command.</span></span>
  
```powershell
Connect-AzAccount
```

<span data-ttu-id="2547f-282">Obtenez le nom de votre abonnement à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="2547f-282">Get your subscription name using the following command.</span></span>
  
```powershell
Get-AzSubscription | Sort SubscriptionName | Select SubscriptionName
```

<span data-ttu-id="2547f-p123">Définissez votre abonnement Azure avec les commandes suivantes. Remplacez tout le texte entre guillemets, y compris les caractères < et >, par le nom d’abonnement correct.</span><span class="sxs-lookup"><span data-stu-id="2547f-p123">Set your Azure subscription with these commands. Replace everything within the quotes, including the < and > characters, with the correct subscription name.</span></span>
  
```powershell
$subscrName="<subscription name>"
Select-AzSubscription -SubscriptionName $subscrName
```

<span data-ttu-id="2547f-p124">Ensuite, créez un nouveau groupe de ressources pour votre réseau virtuel. Pour déterminer un nom de groupe de ressources unique, utilisez cette commande pour répertorier vos groupes de ressources existants.</span><span class="sxs-lookup"><span data-stu-id="2547f-p124">Next, create a new resource group for your virtual network. To determine a unique resource group name, use this command to list your existing resource groups.</span></span>
  
```powershell
Get-AzResourceGroup | Sort ResourceGroupName | Select ResourceGroupName
```

<span data-ttu-id="2547f-287">Créez votre nouveau groupe de ressources avec ces commandes.</span><span class="sxs-lookup"><span data-stu-id="2547f-287">Create your new resource group with these commands.</span></span>
  
```powershell
$rgName="<resource group name>"
$locName="<Table V - Item 2 - Value column>"
New-AzResourceGroup -Name $rgName -Location $locName
```

<span data-ttu-id="2547f-288">Ensuite, créez le réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="2547f-288">Next, you create the Azure virtual network.</span></span>
  
```powershell
# Fill in the variables from previous values and from Tables V, S, and D
$rgName="<name of your new resource group>"
$locName="<Azure location of your new resource group>"
$vnetName="<Table V - Item 1 - Value column>"
$vnetAddrPrefix="<Table V - Item 4 - Value column>"
$gwSubnetPrefix="<Table S - Item 1 - Subnet address space column>"
$SubnetName="<Table S - Item 2 - Subnet name column>"
$SubnetPrefix="<Table S - Item 2 - Subnet address space column>"
$dnsServers=@( "<Table D - Item 1 - DNS server IP address column>", "<Table D - Item 2 - DNS server IP address column>" )
$locShortName=(Get-AzResourceGroup -Name $rgName).Location

# Create the Azure virtual network and a network security group that allows incoming remote desktop connections to the subnet that is hosting virtual machines
$gatewaySubnet=New-AzVirtualNetworkSubnetConfig -Name "GatewaySubnet" -AddressPrefix $gwSubnetPrefix
$vmSubnet=New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetPrefix
New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgName -Location $locName -AddressPrefix $vnetAddrPrefix -Subnet $gatewaySubnet,$vmSubnet -DNSServer $dnsServers
$rule1=New-AzNetworkSecurityRuleConfig -Name "RDPTraffic" -Description "Allow RDP to all VMs on the subnet" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
New-AzNetworkSecurityGroup -Name $SubnetName -ResourceGroupName $rgName -Location $locShortName -SecurityRules $rule1
$vnet=Get-AzVirtualNetwork -ResourceGroupName $rgName -Name $vnetName
$nsg=Get-AzNetworkSecurityGroup -Name $SubnetName -ResourceGroupName $rgName
Set-AzVirtualNetworkSubnetConfig -VirtualNetwork $vnet -Name $SubnetName -AddressPrefix $SubnetPrefix -NetworkSecurityGroup $nsg
$vnet | Set-AzVirtualNetwork
```

<span data-ttu-id="2547f-289">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="2547f-289">Here is your resulting configuration.</span></span>
  
![Le réseau virtuel n’est pas encore connecté au réseau local.](../media/54a37782-a6cc-4d48-b38d-73e128b44a82.png)
  
<span data-ttu-id="2547f-291">Utilisez ces commandes pour créer les passerelles pour la connexion VPN de site à site.</span><span class="sxs-lookup"><span data-stu-id="2547f-291">Next, use these commands to create the gateways for the site-to-site VPN connection.</span></span>
  
```powershell
# Fill in the variables from previous values and from Tables V and L
$vnetName="<Table V - Item 1 - Value column>"
$localGatewayIP="<Table V - Item 3 - Value column>"
$localNetworkPrefix=@( <comma-separated, double-quote enclosed list of the local network address prefixes from Table L, example: "10.1.0.0/24", "10.2.0.0/24"> )
$vnetConnectionKey="<Table V - Item 5 - Value column>"
$vnet=Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgName
# Attach a virtual network gateway to a public IP address and the gateway subnet
$publicGatewayVipName="PublicIPAddress"
$vnetGatewayIpConfigName="PublicIPConfig"
New-AzPublicIpAddress -Name $vnetGatewayIpConfigName -ResourceGroupName $rgName -Location $locName -AllocationMethod Dynamic
$publicGatewayVip=Get-AzPublicIpAddress -Name $vnetGatewayIpConfigName -ResourceGroupName $rgName
$vnetGatewayIpConfig=New-AzVirtualNetworkGatewayIpConfig -Name $vnetGatewayIpConfigName -PublicIpAddressId $publicGatewayVip.Id -SubnetId $vnet.Subnets[0].Id
# Create the Azure gateway
$vnetGatewayName="AzureGateway"
$vnetGateway=New-AzVirtualNetworkGateway -Name $vnetGatewayName -ResourceGroupName $rgName -Location $locName -GatewayType Vpn -VpnType RouteBased -IpConfigurations $vnetGatewayIpConfig
# Create the gateway for the local network
$localGatewayName="LocalNetGateway"
$localGateway=New-AzLocalNetworkGateway -Name $localGatewayName -ResourceGroupName $rgName -Location $locName -GatewayIpAddress $localGatewayIP -AddressPrefix $localNetworkPrefix
# Create the Azure virtual network VPN connection
$vnetConnectionName="S2SConnection"
$vnetConnection=New-AzVirtualNetworkGatewayConnection -Name $vnetConnectionName -ResourceGroupName $rgName -Location $locName -ConnectionType IPsec -SharedKey $vnetConnectionKey -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localGateway
```

<span data-ttu-id="2547f-292">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="2547f-292">Here is your resulting configuration.</span></span>
  
![Le réseau virtuel dispose maintenant d’une passerelle.](../media/82dd66b2-a4b7-48f6-a89b-cfdd94630980.png)
  
<span data-ttu-id="2547f-p125">Ensuite, configurez votre périphérique VPN local de sorte qu'il se connecte à la passerelle VPN Azure. Pour plus d'informations, voir [À propos des périphériques VPN pour les connexions du réseau virtuel Azure de site à site](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices).</span><span class="sxs-lookup"><span data-stu-id="2547f-p125">Next, configure your on-premises VPN device to connect to the Azure VPN gateway. For more information, see [About VPN Devices for site-to-site Azure Virtual Network connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices).</span></span>
  
<span data-ttu-id="2547f-296">Pour configurer votre périphérique VPN, vous avez besoin des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="2547f-296">To configure your VPN device, you will need the following:</span></span>
  
- <span data-ttu-id="2547f-297">L’adresse IPv4 publique de la passerelle VPN Azure pour votre réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="2547f-297">The public IPv4 address of the Azure VPN gateway for your virtual network.</span></span> <span data-ttu-id="2547f-298">Utilisez la commande **Get-AzPublicIpAddress -Name $vnetGatewayIpConfigName -ResourceGroupName $rgName** pour afficher cette adresse.</span><span class="sxs-lookup"><span data-stu-id="2547f-298">Use the **Get-AzPublicIpAddress -Name $vnetGatewayIpConfigName -ResourceGroupName $rgName** command to display this address.</span></span>
    
- <span data-ttu-id="2547f-299">La clé prépartagée IPsec pour la connexion VPN de site à site (Tableau V - Élément 5 - colonne Valeur).</span><span class="sxs-lookup"><span data-stu-id="2547f-299">The IPsec pre-shared key for the site-to-site VPN connection (Table V- Item 5 - Value column).</span></span>
    
<span data-ttu-id="2547f-300">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="2547f-300">Here is your resulting configuration.</span></span>
  
![Le réseau virtuel est désormais connecté au réseau local.](../media/6379c423-4f22-4453-941b-7ff32484a0a5.png)
  
### <a name="phase-3-optional-add-virtual-machines"></a><span data-ttu-id="2547f-302">Phase 3 (facultative) : ajouter des machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="2547f-302">Phase 3 (Optional): Add virtual machines</span></span>

<span data-ttu-id="2547f-p127">Créez les machines virtuelles dont vous avez besoin dans Azure. Pour plus d’informations, reportez-vous à [Créer une machine virtuelle Windows avec le portail Azure](https://go.microsoft.com/fwlink/p/?LinkId=393098).</span><span class="sxs-lookup"><span data-stu-id="2547f-p127">Create the virtual machines you need in Azure. For more information, see [Create a Windows virtual machine with the Azure portal](https://go.microsoft.com/fwlink/p/?LinkId=393098).</span></span>
  
<span data-ttu-id="2547f-305">Utilisez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="2547f-305">Use the following settings:</span></span>
  
- <span data-ttu-id="2547f-306">Dans l’onglet **De base**, sélectionnez le même abonnement et le même groupe de ressources que votre réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="2547f-306">On the **Basics** tab, select the same subscription and resource group as your virtual network.</span></span> <span data-ttu-id="2547f-307">Vous en aurez besoin ultérieurement pour vous connecter à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="2547f-307">You will need these later to sign in to the virtual machine.</span></span> <span data-ttu-id="2547f-308">Dans la section **Détails de l’instance**, sélectionnez la taille de machine virtuelle appropriée.</span><span class="sxs-lookup"><span data-stu-id="2547f-308">In the **Instance details** section, choose the appropriate virtual machine size.</span></span> <span data-ttu-id="2547f-309">Enregistrez le nom d’utilisateur du compte administrateur et le mot de passe dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="2547f-309">Record the administrator account user name and password in a secure location.</span></span> 
    
- <span data-ttu-id="2547f-310">Dans l’onglet **Mise en réseau**, sélectionnez le nom de votre réseau virtuel et le sous-réseau pour l’hébergement de machines virtuelles (pas GatewaySubnet).</span><span class="sxs-lookup"><span data-stu-id="2547f-310">On the **Networking** tab, select the name of your virtual network and the subnet for hosting virtual machines (not the GatewaySubnet).</span></span> <span data-ttu-id="2547f-311">Tous les autres paramètres conservent leurs valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="2547f-311">Leave all other settings at their default values.</span></span>
    
<span data-ttu-id="2547f-p130">Vérifiez que votre machine virtuelle utilise le DNS correctement en vérifiant votre DNS interne pour vous assurer que les enregistrements d’adresse (A) ont été ajoutés pour votre nouvelle machine virtuelle. Pour accéder à Internet, vos machines virtuelles Azure doivent être configurées pour utiliser le serveur proxy de votre réseau local. Contactez votre administrateur réseau pour les étapes de configuration supplémentaires à effectuer sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="2547f-p130">Verify that your virtual machine is using DNS correctly by checking your internal DNS to ensure that Address (A) records were added for you new virtual machine. To access the Internet, your Azure virtual machines must be configured to use your on-premises network's proxy server. Contact your network administrator for additional configuration steps to perform on the server.</span></span>
  
<span data-ttu-id="2547f-315">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="2547f-315">Here is your resulting configuration.</span></span>
  
![Le réseau virtuel héberge maintenant des machines virtuelles qui sont accessibles à partir du réseau local.](../media/86ab63a6-bfae-4f75-8470-bd40dff123ac.png)
  
## <a name="next-step"></a><span data-ttu-id="2547f-317">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="2547f-317">Next step</span></span>
  
[<span data-ttu-id="2547f-318">Déployer la synchronisation d’annuaires Microsoft 365 dans Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="2547f-318">Deploy Microsoft 365 Directory Synchronization in Microsoft Azure</span></span>](deploy-microsoft-365-directory-synchronization-dirsync-in-microsoft-azure.md)
