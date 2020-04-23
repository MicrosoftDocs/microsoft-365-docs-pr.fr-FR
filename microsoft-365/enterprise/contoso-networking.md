---
title: Mise en réseau de Contoso Corporation
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
ms.author: josephd
manager: laurawi
ms.date: 10/01/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Comprendre l’infrastructure réseau Contoso et la façon dont elle utilise la technologie SD-WAN pour assurer la performance optimale de la connectivité réseau avec les services cloud Microsoft 365 Entreprise.
ms.openlocfilehash: 4e649796b30b96db3b36de2dabec1f276728d3ea
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43625277"
---
# <a name="networking-for-the-contoso-corporation"></a><span data-ttu-id="d734e-103">Mise en réseau de Contoso Corporation</span><span class="sxs-lookup"><span data-stu-id="d734e-103">Networking for the Contoso Corporation</span></span>

<span data-ttu-id="d734e-p101">Pour adopter une infrastructure informatique incluse, les ingénieurs réseau de Contoso ont radicalement modifié la manière dont le trafic réseau circule vers les services cloud. Au lieu d’utiliser un modèle interne « Hub and Spoke » qui concentre la connectivité réseau et le trafic pour le niveau hiérarchique suivant chez Contoso, ils ont cherché à mapper les emplacements utilisateur à la sortie Internet locale et les connexions locales aux emplacements réseau de Microsoft 365 les plus proches sur Internet.</span><span class="sxs-lookup"><span data-stu-id="d734e-p101">To adopt a cloud-inclusive infrastructure, Contoso's network engineers realized the fundamental shift in the way that network traffic to cloud services travels. Instead of an internal hub and spoke model that focusses network connectivity and traffic for the next level of the Contoso office hierarchy, they worked to map user locations to local Internet egress and local connections to the closest Microsoft 365 network location on the Internet.</span></span>

## <a name="contosos-networking-infrastructure"></a><span data-ttu-id="d734e-106">Infrastructure réseau de Contoso</span><span class="sxs-lookup"><span data-stu-id="d734e-106">Contoso's networking infrastructure</span></span>

<span data-ttu-id="d734e-107">Voici les éléments du réseau de Contoso qui permettent de relier leurs bureaux entre eux dans le monde entier :</span><span class="sxs-lookup"><span data-stu-id="d734e-107">The elements of Contoso's network that links their offices across the globe are the following:</span></span>

- <span data-ttu-id="d734e-108">Réseau étendu de commutation multiprotocole WAN (MPLS) </span><span class="sxs-lookup"><span data-stu-id="d734e-108">Multiprotocol Label Switching (MPLS) WAN network</span></span>

  <span data-ttu-id="d734e-p102">Un réseau WAN MPLS permet de connecter le siège social de Paris aux bureaux régionaux et les bureaux régionaux aux succursales dans une configuration « Hub and Spoke ». Il s’agit pour les utilisateurs d’accéder aux serveurs locaux qui composent les applications métier au bureau de Paris. Il achemine également tout le trafic Internet générique au bureau de Paris où les périphériques de sécurité réseau traitent les demandes. Dans chaque bureau, les routeurs acheminent le trafic vers les hôtes câblés ou les points d’accès sans fil sur les sous-réseaux qui utilisent l’espace d’adressage IP privé.</span><span class="sxs-lookup"><span data-stu-id="d734e-p102">An MPLS WAN network connects the Paris headquarters to regional offices and regional offices to satellite offices in a spoke and hub configuration. This is for users to access on-premises servers that make up line of business applications in the Paris office. It also routes any generic Internet traffic to the Paris office where network security devices scrub the requests. Within each office, routers deliver traffic to wired hosts or wireless access points on subnets, which use the private IP address space.</span></span>

- <span data-ttu-id="d734e-113">Accès Internet local direct pour le trafic Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d734e-113">Local direct Internet access for Microsoft 365 traffic</span></span>

  <span data-ttu-id="d734e-p103">Chaque bureau dispose d’un périphérique SD-WAN avec l’un des circuits en réseau ISP Internet local doté de sa propre connectivité Internet via un serveur proxy. Il est généralement implémenté sous la forme d’une liaison WAN vers ISP local qui fournit également des adresses IP publiques et un serveur DNS local.</span><span class="sxs-lookup"><span data-stu-id="d734e-p103">Each office has a Software-Defined WAN (SD-WAN) device with one of more local Internet ISP network circuits, with its own Internet connectivity through a proxy server. This is typically implemented as a WAN link to a local ISP that also provides public IP addresses and a local DNS server.</span></span>

- <span data-ttu-id="d734e-116">Présence sur Internet</span><span class="sxs-lookup"><span data-stu-id="d734e-116">Internet presence</span></span>

  <span data-ttu-id="d734e-p104">Contoso est propriétaire du nom de domaine public contoso.com. Le site web public de Contoso pour les commandes de produits se compose d’un ensemble de serveurs dans un centre de données connecté à Internet sur le site parisien. Contoso utilise une plage d’adresses IP publiques disponible 24 h/24 sur Internet.</span><span class="sxs-lookup"><span data-stu-id="d734e-p104">Contoso owns the contoso.com public domain name. The Contoso public web site for ordering products is a set of servers in an Internet-connected datacenter in the Paris campus. Contoso uses a /24 public IP address range on the Internet.</span></span>

<span data-ttu-id="d734e-120">La figure 1 indique l’infrastructure réseau de Contoso et ses connexions à Internet.</span><span class="sxs-lookup"><span data-stu-id="d734e-120">Figure 1 shows Contoso's networking infrastructure and its connections to the Internet.</span></span>

![Réseau de Contoso](../media/contoso-networking/contoso-networking-fig1.png)
 
<span data-ttu-id="d734e-122">**Figure 1 : Réseau de Contoso**</span><span class="sxs-lookup"><span data-stu-id="d734e-122">**Figure 1: Contoso's network**</span></span>

## <a name="use-of-sd-wan-for-optimal-network-connectivity-to-microsoft"></a><span data-ttu-id="d734e-123">Utilisation de la technologie SD-WAN pour la connectivité réseau optimale à Microsoft</span><span class="sxs-lookup"><span data-stu-id="d734e-123">Use of SD-WAN for optimal network connectivity to Microsoft</span></span>

<span data-ttu-id="d734e-124">Contoso a suivi les [principes de connectivité réseau Microsoft 365](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles) pour :</span><span class="sxs-lookup"><span data-stu-id="d734e-124">Contoso followed [Microsoft 365 network connectivity principles](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles) to:</span></span>

1. <span data-ttu-id="d734e-125">Identification et différenciation du trafic réseau Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d734e-125">Identify and differentiate Microsoft 365 network traffic</span></span>
2. <span data-ttu-id="d734e-126">Sortir les connexions réseau localement</span><span class="sxs-lookup"><span data-stu-id="d734e-126">Egress network connections locally</span></span>
3. <span data-ttu-id="d734e-127">Éviter les épingles de réseau</span><span class="sxs-lookup"><span data-stu-id="d734e-127">Avoid network hairpins</span></span>
4. <span data-ttu-id="d734e-128">Ignorer les périphériques de sécurité réseau en double</span><span class="sxs-lookup"><span data-stu-id="d734e-128">Bypass duplicate network security devices</span></span>

<span data-ttu-id="d734e-129">Il existe trois catégories de trafic réseau pour Microsoft 365 : Optimiser, Autoriser et Par défaut.</span><span class="sxs-lookup"><span data-stu-id="d734e-129">There are three categories of network traffic for Microsoft 365: Optimize, Allow, and Default.</span></span> <span data-ttu-id="d734e-130">Optimiser et Autoriser le trafic est le trafic réseau approuvé qui est chiffré et sécurisé aux points de terminaison et est destiné au réseau Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d734e-130">Optimize and Allow traffic is trusted network traffic that is encrypted and secured at the endpoints and is destined for the Microsoft 365 network.</span></span>

<span data-ttu-id="d734e-131">Contoso a décidé d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d734e-131">Contoso decided to:</span></span>

- <span data-ttu-id="d734e-132">Utiliser la sortie Internet directe pour le trafic de catégorie Optimiser et Autoriser et pour transférer le trafic de catégorie Par défaut vers la connexion Internet centrale basée à Paris.</span><span class="sxs-lookup"><span data-stu-id="d734e-132">Use direct Internet egress for Optimize and Allow category traffic and to forward all Default category traffic to the Paris-based central Internet connection.</span></span>

- <span data-ttu-id="d734e-133">Déployer des périphériques SD-WAN à chacun de leur bureau afin de suivre simplement ces principes et assurer la performance optimale de la connectivité réseau avec les services informatiques cloud Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="d734e-133">Deploy SD-WAN devices at each of their office locations as a simple way to follow these principles and achieve optimal network performance for Microsoft 365 cloud-based services.</span></span>

  <span data-ttu-id="d734e-134">Les appareils SD-WAN ont un port réseau local LAN pour le réseau local et plusieurs ports WAN.</span><span class="sxs-lookup"><span data-stu-id="d734e-134">The SD-WAN devices have a LAN port for the local office network and multiple WAN ports.</span></span> <span data-ttu-id="d734e-135">Un port WAN se connecte à leur réseau MPLS et un autre port WAN se connecte à un circuit fournisseur de services Internet local.</span><span class="sxs-lookup"><span data-stu-id="d734e-135">One WAN port connects to their MPLS network and another WAN port connects to a local ISP circuit.</span></span> <span data-ttu-id="d734e-136">L’appareil SD-WAN achemine le trafic réseau de catégorie Optimiser et Autoriser sur le lien du fournisseur de services Internet.</span><span class="sxs-lookup"><span data-stu-id="d734e-136">The SD-WAN device routes Optimize and Allow category network traffic over the ISP link.</span></span>

## <a name="contosos-line-of-business-app-infrastructure"></a><span data-ttu-id="d734e-137">Ligne d’infrastructure d’applications pour les entreprises de Contoso</span><span class="sxs-lookup"><span data-stu-id="d734e-137">Contoso's line of business app infrastructure</span></span>

<span data-ttu-id="d734e-138">Contoso a conçu son infrastructure d’applications et serveur pour les entreprises pour les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d734e-138">Contoso has architected its line of business application and server intranet infrastructure for the following:</span></span>

- <span data-ttu-id="d734e-139">Les succursales utilisent des serveurs de mise en cache locale pour stocker les documents et les sites web internes les plus sollicités.</span><span class="sxs-lookup"><span data-stu-id="d734e-139">Satellite offices use local caching servers to store frequently accessed documents and internal web sites.</span></span>
- <span data-ttu-id="d734e-p107">Les centres régionaux utilisent les serveurs d’applications régionaux pour les bureaux régionaux et les succursales. Ces serveurs se synchronisent avec les serveurs du siège social à Paris.</span><span class="sxs-lookup"><span data-stu-id="d734e-p107">Regional hubs use regional application servers for the regional and satellite offices. These servers synchronize with servers in the Paris headquarters.</span></span>
- <span data-ttu-id="d734e-142">Le site de Paris comporte les centres de données contenant les serveurs d’applications centralisés qui servent l’organisation entière.</span><span class="sxs-lookup"><span data-stu-id="d734e-142">The Paris campus has the datacenters that contain the centralized application servers that serve the entire organization.</span></span>

<span data-ttu-id="d734e-143">La figure 2 indique le pourcentage du trafic réseau lors de l’accès aux serveurs au sein de l’intranet de Contoso.</span><span class="sxs-lookup"><span data-stu-id="d734e-143">Figure 2 shows the percentage of network traffic when accessing servers across Contoso’s intranet.</span></span>

![Infrastructure des applications internes de Contoso](../media/contoso-networking/contoso-networking-fig2.png)
 
<span data-ttu-id="d734e-145">**Figure 2 : infrastructure des applications internes de Contoso**</span><span class="sxs-lookup"><span data-stu-id="d734e-145">**Figure 2: Contoso's infrastructure for internal applications**</span></span>

<span data-ttu-id="d734e-p108">Pour les utilisateurs des centres régionaux et des succursales, 60 % des ressources requises par les collaborateurs peuvent être prises en charge par les serveurs de ces sites. Les 40 % des demandes de ressources restantes doivent accéder au siège social parisien par le biais d’une connexion WAN.</span><span class="sxs-lookup"><span data-stu-id="d734e-p108">For users in satellite or regional hub offices, 60% of the resources needed by employees can be served by satellite and regional hub office servers. The additional 40% of resource requests must go over the WAN link to the Paris campus.</span></span>

## <a name="contosos-network-analysis-and-preparation-of-their-network-for-microsoft-365-enterprise"></a><span data-ttu-id="d734e-148">Analyse des réseaux de Contoso et préparation de son réseau pour Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="d734e-148">Contoso's network analysis and preparation of their network for Microsoft 365 Enterprise</span></span>

<span data-ttu-id="d734e-p109">L’adoption réussie des services Microsoft 365 Entreprise par les utilisateurs de Contoso dépend de la connectivité performante et à haut niveau de disponibilité à Internet ou directement aux services de cloud computing Microsoft. Afin de planifier et d’implémenter une connectivité optimisée aux services de cloud computing Microsoft 365 Entreprise, Contoso a pris les mesures suivantes :</span><span class="sxs-lookup"><span data-stu-id="d734e-p109">Successful adoption of Microsoft 365 Enterprise services by Contoso’s users depend on highly available and performant connectivity to the Internet, or directly to Microsoft cloud services. Contoso took these steps to plan for and implement optimized connectivity to Microsoft 365 Enterprise cloud services:</span></span>

1. <span data-ttu-id="d734e-151">Création d’un diagramme de réseau WAN d’entreprise pour simplifier la planification</span><span class="sxs-lookup"><span data-stu-id="d734e-151">Created a company WAN network diagram to aid with planning</span></span>

   <span data-ttu-id="d734e-p110">Contoso a commencé à planifier son réseau en créant un diagramme montrant ses sites, la connectivité réseau existante, les périphériques du périmètre du réseau existants et les classes de service gérés sur le réseau. Contoso a utilisé ce diagramme pour chaque étape suivante de la planification et de l’implémentation de la connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="d734e-p110">Contoso started their network planning by creating a diagram showing their locations, the existing network connectivity, their existing network perimeter devices and classes of service that are managed on the network. They used this diagram for each subsequent step in the planning and implementation of networking connectivity.</span></span>

2. <span data-ttu-id="d734e-154">Création d’un plan pour la connectivité réseau de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="d734e-154">Created a plan for Microsoft 365 Enterprise network connectivity</span></span>

   <span data-ttu-id="d734e-155">Contoso a utilisé les [principes de connectivité réseau Microsoft 365](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles) et fourni les architectures réseau de référence pour déterminer SD-WAN comme sa topologie par défaut pour la connectivité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d734e-155">Contoso used the [Microsoft 365 network connectivity principles](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles) and provided reference network architectures to determine SD-WAN as their preferred topology for Microsoft 365 connectivity.</span></span>

3. <span data-ttu-id="d734e-156">Analyse de l’utilisation de la connexion à Internet et de la bande passante WAN MPLS à chaque bureau, et de la bande passante accrue, le cas échéant</span><span class="sxs-lookup"><span data-stu-id="d734e-156">Analyzed Internet connection utilization and MPLS WAN bandwidth at each office and increased bandwidth as needed</span></span>

   <span data-ttu-id="d734e-157">L’utilisation actuelle de chaque bureau a été analysée et les circuits ont été augmentés afin que le trafic informatique Microsoft 365 prévu soit assuré avec une moyenne de 20 % de capacité inutilisée.</span><span class="sxs-lookup"><span data-stu-id="d734e-157">Each office was analyzed for the current usage and circuits were increased so that predicted Microsoft 365 cloud-based traffic would be operating with an average of 20% of unused capacity.</span></span>

4. <span data-ttu-id="d734e-158">Optimisation des performances vers les services réseau Microsoft</span><span class="sxs-lookup"><span data-stu-id="d734e-158">Optimized performance to Microsoft network services</span></span>

   <span data-ttu-id="d734e-159">Contoso a déterminé la série d’autres points de terminaison Office 365, Intune et Azure, et configuré des pare-feux, des périphériques de sécurité et d’autres systèmes sur Internet pour des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="d734e-159">Contoso determined the set of Office 365, Intune, and Azure endpoints and configured firewalls, security devices, and other systems in the Internet path for optimal performance.</span></span> <span data-ttu-id="d734e-160">Les points de terminaison pour Office 365 le trafic de catégorie Optimiser et Autoriser ont été configurés sur les périphériques SD-WAN pour le routage via le circuit fournisseur de services Internet.</span><span class="sxs-lookup"><span data-stu-id="d734e-160">Endpoints for Office 365 Optimize and Allow category traffic was configured into the SD-WAN devices for routing over the ISP circuit.</span></span>

5. <span data-ttu-id="d734e-161">Configuration du DNS interne</span><span class="sxs-lookup"><span data-stu-id="d734e-161">Configured internal DNS</span></span>

   <span data-ttu-id="d734e-162">Le DNS doit être fonctionnel et le trafic Microsoft 365 doit y être vérifié.</span><span class="sxs-lookup"><span data-stu-id="d734e-162">DNS is required to be functional and to be looked up locally for Microsoft 365 traffic.</span></span>

6. <span data-ttu-id="d734e-163">Validation de la connectivité des ports et des points de terminaison réseau</span><span class="sxs-lookup"><span data-stu-id="d734e-163">Validated network endpoint and port connectivity</span></span>

   <span data-ttu-id="d734e-164">Contoso a exécuté des outils de test de connectivité réseau fournis par Microsoft pour valider la connectivité pour les services cloud de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="d734e-164">Contoso ran network connectivity test tools provided by Microsoft to validate connectivity for Microsoft 365 Enterprise cloud services.</span></span>

7. <span data-ttu-id="d734e-165">Optimisation des ordinateurs des employés pour la connectivité réseau</span><span class="sxs-lookup"><span data-stu-id="d734e-165">Optimized employee computers for network connectivity</span></span>

   <span data-ttu-id="d734e-166">Les ordinateurs individuels ont été vérifiés pour s’assurer que les dernières mises à jour du système d’exploitation ont été installées et que la surveillance de la sécurité des points de terminaison est active sur tous les clients.</span><span class="sxs-lookup"><span data-stu-id="d734e-166">Individual computers were checked to ensure that the latest operating system updates were installed and that endpoint security monitoring is active on all clients.</span></span>

## <a name="next-step"></a><span data-ttu-id="d734e-167">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="d734e-167">Next step</span></span>

<span data-ttu-id="d734e-168">[En savoir plus](contoso-identity.md) sur la façon dont Contoso exploite ses services de domaine Active Directory (AD DS) locaux dans le cloud pour les employés, et fédère l’authentification pour les clients et les partenaires professionnels.</span><span class="sxs-lookup"><span data-stu-id="d734e-168">[Learn](contoso-identity.md) how Contoso is leveraging its on-premises Active Directory Domain Services (AD DS) in the cloud for employees and federating authentication for customers and business partners.</span></span>

## <a name="see-also"></a><span data-ttu-id="d734e-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d734e-169">See also</span></span>

[<span data-ttu-id="d734e-170">Mise en réseau pour Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="d734e-170">Networking for Microsoft 365 Enterprise</span></span>](networking-infrastructure.md)

[<span data-ttu-id="d734e-171">Guide de déploiement</span><span class="sxs-lookup"><span data-stu-id="d734e-171">Deployment guide</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="d734e-172">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="d734e-172">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)
