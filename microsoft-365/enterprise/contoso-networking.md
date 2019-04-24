---
title: Mise en réseau de Contoso Corporation
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 09/18/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Comprendre l’infrastructure réseau Contoso et la façon dont elle utilise la technologie SD-WAN pour assurer la performance optimale de la connectivité réseau avec les services informatiques Microsoft 365 Entreprise.
ms.openlocfilehash: 09da5f25a9c2cc49ade470fa8fa7fe98d9f7a20e
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283759"
---
# <a name="networking-for-the-contoso-corporation"></a><span data-ttu-id="318c7-103">Mise en réseau de Contoso Corporation</span><span class="sxs-lookup"><span data-stu-id="318c7-103">Networking for the Contoso Corporation</span></span>

<span data-ttu-id="318c7-104">**Résumé :** Comprendre l’infrastructure réseau Contoso et la façon dont elle utilise la technologie SD-WAN pour assurer la performance optimale de la connectivité réseau avec les services informatiques Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="318c7-104">**Summary:** Understand the Contoso networking infrastructure and how it uses its SD-WAN technology for optimal performance network connectivity to Microsoft 365 Enterprise cloud based services.</span></span>

<span data-ttu-id="318c7-p101">Pour adopter une infrastructure informatique incluse, les ingénieurs réseau de Contoso ont radicalement modifié la manière dont le trafic réseau circule vers les services informatiques. Au lieu d’utiliser un modèle « Hub and Spoke » qui concentre la connectivité réseau sur le siège social, ils ont cherché à mapper les emplacements utilisateur à la sortie Internet locale et les connexions locales aux emplacements réseau de Microsoft sur Internet.</span><span class="sxs-lookup"><span data-stu-id="318c7-p101">To adopt a cloud-inclusive infrastructure, Contoso's network engineers realized the fundamental shift in the way that network traffic to cloud-based services travels. Instead of a hub and spoke model that focusses network connectivity on the head office, they worked to map user locations to local Internet egress and local connections to Microsoft network locations on the Internet.</span></span>

## <a name="contosos-networking-infrastructure"></a><span data-ttu-id="318c7-107">Infrastructure réseau de Contoso</span><span class="sxs-lookup"><span data-stu-id="318c7-107">Contoso's networking infrastructure</span></span>

<span data-ttu-id="318c7-108">Voici les éléments du réseau de Contoso qui permettent de relier leurs bureaux entre eux dans le monde entier :</span><span class="sxs-lookup"><span data-stu-id="318c7-108">The elements of Contoso's network that links their offices across the globe are the following:</span></span>

- <span data-ttu-id="318c7-109">Réseau WAN MPLS</span><span class="sxs-lookup"><span data-stu-id="318c7-109">MPLS WAN network</span></span>

  <span data-ttu-id="318c7-p102">Un réseau WAN MPLS permet de connecter le siège social de Paris aux bureaux régionaux et les bureaux régionaux aux succursales dans une configuration « Hub and Spoke ». Il s’agit pour les utilisateurs d’accéder aux serveurs locaux qui composent les applications métier au bureau de Paris. Il achemine également tout le trafic Internet générique au bureau de Paris où les périphériques de sécurité réseau traitent les demandes. Dans chaque bureau, les routeurs acheminent le trafic vers les hôtes ou les points d’accès sans fil sur les sous-réseaux qui utilisent l’espace d’adressage IP privé.</span><span class="sxs-lookup"><span data-stu-id="318c7-p102">An MPLS WAN network connects the Paris headquarters to regional offices and regional offices to satellite offices in a spoke and hub configuration. This is for users to access on-premises servers that make up line of business applications in the Paris office. It also routes any generic Internet traffic to the Paris office where network security devices scrub the requests. Within each office, routers deliver traffic to hosts or wireless access points on subnets, which use the private IP address space.</span></span>

- <span data-ttu-id="318c7-114">Accès Internet local direct pour le trafic Office 365</span><span class="sxs-lookup"><span data-stu-id="318c7-114">Local direct Internet access for Office 365 traffic</span></span>

  <span data-ttu-id="318c7-p103">Chaque bureau dispose d’un périphérique SD-WAN avec l’un des circuits en réseau ISP Internet local doté de sa propre connectivité Internet via un serveur proxy. Il est généralement implémenté sous la forme d’une liaison WAN vers ISP local qui fournit également des adresses IP publiques et des adresses IP du serveur DNS local pour le serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="318c7-p103">Each office has an SD-WAN device with one of more local Internet ISP network circuits, with its own Internet connectivity through a proxy server. This is typically implemented as a WAN link to a local ISP that also provides public IP addresses and local DNS server IP addresses for the proxy server.</span></span>

- <span data-ttu-id="318c7-117">Présence sur Internet</span><span class="sxs-lookup"><span data-stu-id="318c7-117">Internet presence</span></span>

  <span data-ttu-id="318c7-p104">Contoso est propriétaire du nom de domaine public contoso.com. Le site web public de Contoso pour les commandes de produits se compose d’un ensemble de serveurs dans un centre de données connecté à Internet sur le site parisien. Contoso utilise une plage d’adresses IP publiques disponible 24 h/24 sur Internet.</span><span class="sxs-lookup"><span data-stu-id="318c7-p104">Contoso owns the contoso.com public domain name. The Contoso public web site for ordering products is a set of servers in an Internet-connected datacenter in the Paris campus. Contoso uses a /24 public IP address range on the Internet.</span></span>

<span data-ttu-id="318c7-121">La figure 1 indique l’infrastructure réseau de Contoso et ses connexions à Internet.</span><span class="sxs-lookup"><span data-stu-id="318c7-121">Figure 1 shows Contoso's networking infrastructure and its connections to the Internet.</span></span>

![](./media/contoso-networking/contoso-networking-fig1.png)
 
<span data-ttu-id="318c7-122">**Figure 1 : Réseau de Contoso**</span><span class="sxs-lookup"><span data-stu-id="318c7-122">**Figure 1: Contoso's network**</span></span>

## <a name="use-of-sd-wan-for-optimal-network-connectivity-to-microsoft"></a><span data-ttu-id="318c7-123">Utilisation de la technologie SD-WAN pour la connectivité réseau optimale à Microsoft</span><span class="sxs-lookup"><span data-stu-id="318c7-123">Use of SD-WAN for optimal network connectivity to Microsoft</span></span>

<span data-ttu-id="318c7-124">Contoso a suivi les [principes de connectivité réseau Office 365](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles) suivants :</span><span class="sxs-lookup"><span data-stu-id="318c7-124">Contoso followed [Office 365 network connectivity principles](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles):</span></span>

1. <span data-ttu-id="318c7-125">Identifier et différencier le trafic réseau Office 365</span><span class="sxs-lookup"><span data-stu-id="318c7-125">Identify and differentiate Office 365 network traffic</span></span>
2. <span data-ttu-id="318c7-126">Sortir les connexions réseau localement</span><span class="sxs-lookup"><span data-stu-id="318c7-126">Egress network connections locally</span></span>
3. <span data-ttu-id="318c7-127">Éviter les épingles de réseau</span><span class="sxs-lookup"><span data-stu-id="318c7-127">Avoid network hairpins</span></span>
4. <span data-ttu-id="318c7-128">Ignorer les périphériques de sécurité réseau en double</span><span class="sxs-lookup"><span data-stu-id="318c7-128">Bypass duplicate network security devices</span></span>

<span data-ttu-id="318c7-p105">Il existe trois catégories de trafic réseau pour Office 365 : Optimiser, Autoriser et Par défaut. Le trafic Optimiser et Autoriser correspond au trafic réseau de confiance qui est chiffré et sécurisé aux points de terminaison et destiné aux centres de données Microsoft.</span><span class="sxs-lookup"><span data-stu-id="318c7-p105">There are three categories of network traffic for Office 365: Optimize, Allow, and Default. Optimize and Allow traffic is trusted network traffic that is encrypted and secured at the endpoints and is destined for Microsoft datacenters.</span></span>

<span data-ttu-id="318c7-131">Contoso a décidé d’utiliser la sortie Internet directe pour le trafic de catégorie Optimiser et Autoriser et pour transférer le trafic de catégorie Par défaut vers la connexion Internet centrale basée à Paris.</span><span class="sxs-lookup"><span data-stu-id="318c7-131">Contoso decided to use direct Internet egress for Optimize and Allow category traffic and to forward all Default category traffic to the Paris-based central Internet connection.</span></span>

<span data-ttu-id="318c7-132">Ils ont décidé de déployer des périphériques SD-WAN à chacun de leur bureau afin de suivre simplement ces principes et assurer la performance optimale de la connectivité réseau avec les services informatiques Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="318c7-132">They decided to deploy SD-WAN devices at each of their office locations as a simple way to follow these principles and achieve optimal network performance for Microsoft 365 cloud-based services.</span></span>

<span data-ttu-id="318c7-p106">Les périphériques SD-WAN disposent d’un port LAN pour le réseau de bureaux local et plusieurs ports WAN. Un port WAN se connecte à leur réseau MPLS et les autres ports WAN se connectent aux circuits ISP locaux. Le périphérique SD-WAN achemine le trafic réseau de catégorie Optimiser et Autoriser vers les liaisons ISP.</span><span class="sxs-lookup"><span data-stu-id="318c7-p106">The SD-WAN devices have a LAN port for the local office network and multiple WAN ports. One WAN port connects to their MPLS network and other WAN ports connect to local ISP circuits. The SD-WAN device routes Optimize and Allow category network traffic to the ISP links.</span></span>

## <a name="contosos-line-of-business-app-infrastructure"></a><span data-ttu-id="318c7-136">Ligne d’infrastructure d’applications pour les entreprises de Contoso</span><span class="sxs-lookup"><span data-stu-id="318c7-136">Contoso's line of business app infrastructure</span></span>

<span data-ttu-id="318c7-137">Contoso a conçu son infrastructure d’applications et serveur pour les entreprises pour les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="318c7-137">Contoso has architected its line of business application and server infrastructure for the following:</span></span>

- <span data-ttu-id="318c7-138">Les succursales utilisent des serveurs de mise en cache locale pour stocker les documents et les sites web internes les plus sollicités.</span><span class="sxs-lookup"><span data-stu-id="318c7-138">Satellite offices use local caching servers to store frequently accessed documents and internal web sites.</span></span>
- <span data-ttu-id="318c7-p107">Les centres régionaux utilisent les serveurs d’applications régionaux pour les bureaux régionaux et les succursales. Ces serveurs se synchronisent avec les serveurs du siège social à Paris.</span><span class="sxs-lookup"><span data-stu-id="318c7-p107">Regional hubs use regional application servers for the regional and satellite offices. These servers synchronize with servers in the Paris headquarters.</span></span>
- <span data-ttu-id="318c7-141">Le site de Paris comporte les centres de données contenant les serveurs d’applications centralisés qui servent l’organisation entière.</span><span class="sxs-lookup"><span data-stu-id="318c7-141">The Paris campus has the datacenters that contain the centralized application servers that serve the entire organization.</span></span>

<span data-ttu-id="318c7-142">La figure 2 indique le pourcentage du trafic réseau lors de l’accès aux serveurs au sein de l’intranet de Contoso.</span><span class="sxs-lookup"><span data-stu-id="318c7-142">Figure 2 shows the percentage of network traffic when accessing servers across Contoso’s intranet.</span></span>

![](./media/contoso-networking/contoso-networking-fig2.png)
 
<span data-ttu-id="318c7-143">**Figure 2 : infrastructure des applications internes de Contoso**</span><span class="sxs-lookup"><span data-stu-id="318c7-143">**Figure 2: Contoso's infrastructure for internal applications**</span></span>

<span data-ttu-id="318c7-p108">Pour les utilisateurs des centres régionaux et des succursales, 60 % des ressources requises par les collaborateurs peuvent être prises en charge par les serveurs de ces sites. Les 40 % des demandes de ressources restantes doivent accéder au siège social parisien par le biais d’une connexion WAN.</span><span class="sxs-lookup"><span data-stu-id="318c7-p108">For users in satellite or regional hub offices, 60% of the resources needed by employees can be served by satellite and regional hub office servers. The additional 40% of resource requests must go over the WAN link to the Paris campus.</span></span>

## <a name="contosos-network-analysis-and-preparation-of-their-network-for-microsoft-365-enterprise"></a><span data-ttu-id="318c7-146">Analyse des réseaux de Contoso et préparation de son réseau pour Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="318c7-146">Contoso's network analysis and preparation of their network for Microsoft 365 Enterprise</span></span>

<span data-ttu-id="318c7-p109">L’adoption réussie des services Microsoft 365 Entreprise par les utilisateurs de Contoso dépend de la connectivité performante et à haut niveau de disponibilité à Internet ou directement aux services de cloud computing Microsoft. Afin de planifier et d’implémenter une connectivité optimisée aux services de cloud computing Microsoft 365 Entreprise, Contoso a pris les mesures suivantes :</span><span class="sxs-lookup"><span data-stu-id="318c7-p109">Successful adoption of Microsoft 365 Enterprise services by Contoso’s users depend on highly available and performant connectivity to the Internet, or directly to Microsoft cloud services. Contoso took these steps to plan for and implement optimized connectivity to Microsoft 365 Enterprise cloud services:</span></span>

1. <span data-ttu-id="318c7-149">Création d’un diagramme de réseau WAN d’entreprise pour simplifier la planification</span><span class="sxs-lookup"><span data-stu-id="318c7-149">Created a company WAN network diagram to aid with planning</span></span>

   <span data-ttu-id="318c7-p110">Contoso a commencé à planifier son réseau en créant un diagramme montrant ses sites, la connectivité réseau existante, les périphériques du périmètre du réseau existants et les classes de service gérés sur le réseau. Contoso a utilisé ce diagramme pour chaque étape suivante de la planification et de l’implémentation de la connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="318c7-p110">Contoso started their network planning by creating a diagram showing their locations, the existing network connectivity, their existing network perimeter devices and classes of service that are managed on the network. They used this diagram for each subsequent step in the planning and implementation of networking connectivity.</span></span>

2. <span data-ttu-id="318c7-152">Création d’un plan pour la connectivité réseau de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="318c7-152">Created a plan for Microsoft 365 Enterprise network connectivity</span></span>

   <span data-ttu-id="318c7-153">Contoso a utilisé les [principes de connectivité réseau Office 365](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles) et fourni les architectures réseau de référence pour déterminer SD-WAN comme sa topologie par défaut pour la connectivité Office 365.</span><span class="sxs-lookup"><span data-stu-id="318c7-153">Contoso used the [Office 365 network connectivity principles](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles) and provided reference network architectures to determine SD-WAN as their preferred topology for Office 365 connectivity.</span></span>

3. <span data-ttu-id="318c7-154">Analyse de l’utilisation de la connexion à Internet et de la bande passante WAN MPLS à chaque bureau, et de la bande passante accrue, le cas échéant</span><span class="sxs-lookup"><span data-stu-id="318c7-154">Analyzed Internet connection utilization and MPLS WAN bandwidth at each office and increased bandwidth as needed</span></span>

   <span data-ttu-id="318c7-155">L’utilisation actuelle de chaque bureau a été analysée et les circuits ont été augmentés afin que le trafic informatique Microsoft 365 prévu soit assuré avec une moyenne de 20 % de capacité inutilisée.</span><span class="sxs-lookup"><span data-stu-id="318c7-155">Each office was analyzed for the current usage and circuits were increased so that predicted Microsoft 365 cloud-based traffic would be operating with an average of 20% of unused capacity.</span></span>

4. <span data-ttu-id="318c7-156">Optimisation des performances vers les services réseau Microsoft</span><span class="sxs-lookup"><span data-stu-id="318c7-156">Optimized performance to Microsoft network services</span></span>

   <span data-ttu-id="318c7-p111">Contoso a choisi l’ensemble de points de terminaison Office 365, Intune et Azure, et a configuré les pare-feux, les périphériques de sécurité et les autres systèmes dans le chemin d’accès Internet afin d’assurer des performances optimales. Les points de terminaison du trafic de catégorie Optimiser et Autoriser pour Office 365 ont été configurés dans les périphériques SD-WAN ayant fourni l’accès direct à Internet.</span><span class="sxs-lookup"><span data-stu-id="318c7-p111">Contoso determined the set of Office 365, Intune, and Azure endpoints and configured firewalls, security devices, and other systems in the Internet path for optimal performance. Endpoints for Office 365 Optimize and Allow category traffic was configured into the SD-WAN devices that provided direct Internet access.</span></span>

5. <span data-ttu-id="318c7-159">Configuration du DNS interne</span><span class="sxs-lookup"><span data-stu-id="318c7-159">Configured internal DNS</span></span>

   <span data-ttu-id="318c7-160">Le DNS doit être fonctionnel et le trafic Office 365 doit y être vérifié.</span><span class="sxs-lookup"><span data-stu-id="318c7-160">DNS is required to be functional and to be looked up locally for Office 365 traffic.</span></span>

6. <span data-ttu-id="318c7-161">Validation de la connectivité des ports et des points de terminaison réseau</span><span class="sxs-lookup"><span data-stu-id="318c7-161">Validated network endpoint and port connectivity</span></span>

   <span data-ttu-id="318c7-162">Contoso a exécuté des outils de test de connectivité réseau fournis par Microsoft pour valider la connectivité pour les services cloud de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="318c7-162">Contoso ran network connectivity test tools provided by Microsoft to validate connectivity for Microsoft 365 Enterprise cloud services.</span></span>

7. <span data-ttu-id="318c7-163">Optimisation des ordinateurs des employés pour la connectivité réseau</span><span class="sxs-lookup"><span data-stu-id="318c7-163">Optimized employee computers for network connectivity</span></span>

   <span data-ttu-id="318c7-164">Les ordinateurs individuels ont été vérifiés pour s’assurer que les dernières mises à jour du système d’exploitation ont été installées et que la surveillance de la sécurité des points de terminaison est active sur tous les clients.</span><span class="sxs-lookup"><span data-stu-id="318c7-164">Individual computers were checked to ensure that the latest operating system updates were installed and that endpoint security monitoring is active on all clients.</span></span>

## <a name="next-step"></a><span data-ttu-id="318c7-165">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="318c7-165">Next step</span></span>

<span data-ttu-id="318c7-166">[En savoir plus](contoso-identity.md) sur la façon dont Contoso exploite son fournisseur d’identité local dans le cloud pour les employés, et fédère l’authentification pour les clients et les partenaires professionnels.</span><span class="sxs-lookup"><span data-stu-id="318c7-166">[Learn](contoso-identity.md) how Contoso is leveraging its on-premises identity provider in the cloud for employees and federating authentication for customers and business partners.</span></span>

## <a name="see-also"></a><span data-ttu-id="318c7-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="318c7-167">See also</span></span>

[<span data-ttu-id="318c7-168">Mise en réseau pour Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="318c7-168">Networking for Microsoft 365 Enterprise</span></span>](networking-infrastructure.md)

[<span data-ttu-id="318c7-169">Guide de déploiement</span><span class="sxs-lookup"><span data-stu-id="318c7-169">Deployment guide</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="318c7-170">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="318c7-170">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)
