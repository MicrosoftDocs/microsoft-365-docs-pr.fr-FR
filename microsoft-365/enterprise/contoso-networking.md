---
title: Mise en réseau de Contoso Corporation
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
ms.author: josephd
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Comprendre l’infrastructure réseau contoso et la façon dont elle utilise la technologie SD-WAN pour optimiser les performances de mise en réseau à Microsoft 365 pour les services Cloud d’entreprise.
ms.openlocfilehash: d5f3581b81d33bdc200321692b82d57a96d09298
ms.sourcegitcommit: 66b8fc1d8ba4f17487cd2004ac19cf2fff472f3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2020
ms.locfileid: "48754013"
---
# <a name="networking-for-the-contoso-corporation"></a><span data-ttu-id="7a926-103">Mise en réseau de Contoso Corporation</span><span class="sxs-lookup"><span data-stu-id="7a926-103">Networking for the Contoso Corporation</span></span>

<span data-ttu-id="7a926-p101">Pour adopter une infrastructure de Cloud inclusive, Contoso a élaboré un changement fondamental dans la façon dont le trafic réseau vers les services Cloud transite. Au lieu d’un modèle interne Hub-and-spoke qui se concentre sur la connectivité réseau et le trafic pour le niveau suivant de la hiérarchie des bureaux, il a mappé des emplacements d’utilisateur à des connexions Internet locales et de sortie vers l’emplacement réseau Microsoft 365 le plus proche sur Internet.</span><span class="sxs-lookup"><span data-stu-id="7a926-p101">To adopt a cloud-inclusive infrastructure, Contoso devised a fundamental shift in how network traffic to cloud services travels. Instead of an internal hub-and-spoke model that focuses network connectivity and traffic for the next level of the office hierarchy, they mapped user locations to local internet egress and local connections to the closest Microsoft 365 network location on the internet.</span></span>

## <a name="networking-infrastructure"></a><span data-ttu-id="7a926-106">Infrastructure réseau</span><span class="sxs-lookup"><span data-stu-id="7a926-106">Networking infrastructure</span></span>

<span data-ttu-id="7a926-107">Voici les éléments réseau qui lient les bureaux Contoso dans le monde entier :</span><span class="sxs-lookup"><span data-stu-id="7a926-107">These are the network elements that link Contoso offices across the globe:</span></span>

- <span data-ttu-id="7a926-108">Réseau étendu de commutation multiprotocole WAN (MPLS) </span><span class="sxs-lookup"><span data-stu-id="7a926-108">Multiprotocol Label Switching (MPLS) WAN network</span></span>

  <span data-ttu-id="7a926-p102">Un réseau MPLS WAN connecte le siège social de Paris aux bureaux régionaux et aux bureaux régionaux de satellites dans une configuration spoke-and-Hub. Le réseau permet aux utilisateurs d’accéder à des serveurs sur site qui composent des applications métiers dans le siège social de Paris. Il achemine également tout trafic Internet générique vers le Bureau de Paris, dans lequel les périphériques de sécurité du réseau dépassent les demandes. Dans chaque bureau, les routeurs acheminent le trafic vers des hôtes filaires ou des points d’accès sans fil sur des sous-réseaux, qui utilisent l’espace d’adressage IP privé.</span><span class="sxs-lookup"><span data-stu-id="7a926-p102">An MPLS WAN network connects the Paris headquarters to regional offices and regional offices to satellite offices in a spoke-and-hub configuration. The network enables users to access on-premises servers that make up line-of-business applications in the Paris headquarters. It also routes any generic internet traffic to the Paris office, where network security devices scrub the requests. Within each office, routers deliver traffic to wired hosts or wireless access points on subnets, which use the private IP address space.</span></span>

- <span data-ttu-id="7a926-113">Accès Internet direct local pour le trafic Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7a926-113">Local direct internet access for Microsoft 365 traffic</span></span>

  <span data-ttu-id="7a926-p103">Chaque Office possède un périphérique WAN (SD-WAN) défini par le logiciel, qui dispose d’un ou de plusieurs circuits de réseau ISP locaux avec sa propre connectivité Internet via un serveur proxy. Elle est généralement implémentée en tant que liaison de réseau étendu à un fournisseur de services Internet local qui fournit également des adresses IP publiques et un serveur DNS local.</span><span class="sxs-lookup"><span data-stu-id="7a926-p103">Each office has a software-defined WAN (SD-WAN) device that has one or more local internet ISP network circuits with its own internet connectivity through a proxy server. This is typically implemented as a WAN link to a local ISP that also provides public IP addresses and a local DNS server.</span></span>

- <span data-ttu-id="7a926-116">Présence sur Internet</span><span class="sxs-lookup"><span data-stu-id="7a926-116">Internet presence</span></span>

  <span data-ttu-id="7a926-p104">Contoso possède le \. nom de domaine public contoso com. Le site Web public contoso pour commander des produits est un ensemble de serveurs dans un centre de contenu connecté à Internet dans le campus de Paris. Contoso utilise une/24 plage d’adresses IP publiques sur Internet.</span><span class="sxs-lookup"><span data-stu-id="7a926-p104">Contoso owns the contoso\.com public domain name. The Contoso public web site for ordering products is a set of servers in an internet-connected datacenter in the Paris campus. Contoso uses a /24 public IP address range on the internet.</span></span>

<span data-ttu-id="7a926-120">La figure 1 illustre l’infrastructure de réseau contoso et ses connexions à Internet.</span><span class="sxs-lookup"><span data-stu-id="7a926-120">Figure 1 shows the Contoso networking infrastructure and its connections to the internet.</span></span>

![Réseau contoso](../media/contoso-networking/contoso-networking-fig1.png)
 
<span data-ttu-id="7a926-122">**Figure 1 : réseau contoso**</span><span class="sxs-lookup"><span data-stu-id="7a926-122">**Figure 1: The Contoso network**</span></span>

## <a name="use-of-sd-wan-for-optimal-network-connectivity-to-microsoft"></a><span data-ttu-id="7a926-123">Utilisation de la technologie SD-WAN pour la connectivité réseau optimale à Microsoft</span><span class="sxs-lookup"><span data-stu-id="7a926-123">Use of SD-WAN for optimal network connectivity to Microsoft</span></span>

<span data-ttu-id="7a926-124">Contoso a suivi les [principes de connectivité réseau Microsoft 365](microsoft-365-network-connectivity-principles.md) pour :</span><span class="sxs-lookup"><span data-stu-id="7a926-124">Contoso followed [Microsoft 365 network connectivity principles](microsoft-365-network-connectivity-principles.md) to:</span></span>

- <span data-ttu-id="7a926-125">Identification et différenciation du trafic réseau Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7a926-125">Identify and differentiate Microsoft 365 network traffic</span></span>
- <span data-ttu-id="7a926-126">Sortir les connexions réseau localement</span><span class="sxs-lookup"><span data-stu-id="7a926-126">Egress network connections locally</span></span>
- <span data-ttu-id="7a926-127">Éviter les épingles de réseau</span><span class="sxs-lookup"><span data-stu-id="7a926-127">Avoid network hairpins</span></span>
- <span data-ttu-id="7a926-128">Ignorer les périphériques de sécurité réseau en double</span><span class="sxs-lookup"><span data-stu-id="7a926-128">Bypass duplicate network security devices</span></span>

<span data-ttu-id="7a926-129">Il existe trois catégories de trafic réseau pour Microsoft 365 : *optimize*, *allow*et *default*.</span><span class="sxs-lookup"><span data-stu-id="7a926-129">There are three categories of network traffic for Microsoft 365: *Optimize*, *Allow*, and *Default*.</span></span> <span data-ttu-id="7a926-130">Optimiser et autoriser le trafic est le trafic réseau approuvé qui est chiffré et sécurisé aux points de terminaison et qui est destiné au réseau Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7a926-130">Optimize and Allow traffic is trusted network traffic that's encrypted and secured at the endpoints and is destined for the Microsoft 365 network.</span></span>

<span data-ttu-id="7a926-131">Contoso a décidé d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a926-131">Contoso decided to:</span></span>

- <span data-ttu-id="7a926-132">Utilisez la sortie Internet directe pour optimiser et autoriser le trafic de catégorie et transférer tout le trafic de catégorie par défaut vers la connexion Internet centrale de Paris.</span><span class="sxs-lookup"><span data-stu-id="7a926-132">Use direct internet egress for Optimize and Allow category traffic and to forward all Default category traffic to the Paris-based central internet connection.</span></span>

- <span data-ttu-id="7a926-133">Déployer des périphériques SD-WAN au niveau de chaque bureau pour suivre facilement ces principes et obtenir des performances réseau optimales pour les services Cloud de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7a926-133">Deploy SD-WAN devices at each office as a simple way to follow these principles and achieve optimal network performance for Microsoft 365 cloud-based services.</span></span>

  <span data-ttu-id="7a926-134">Les appareils SD-WAN ont un port réseau local LAN pour le réseau local et plusieurs ports WAN.</span><span class="sxs-lookup"><span data-stu-id="7a926-134">The SD-WAN devices have a LAN port for the local office network and multiple WAN ports.</span></span> <span data-ttu-id="7a926-135">Un port WAN se connecte à son réseau MPLS.</span><span class="sxs-lookup"><span data-stu-id="7a926-135">One WAN port connects to their MPLS network.</span></span> <span data-ttu-id="7a926-136">Un autre se connecte à un circuit du fournisseur de services Internet local.</span><span class="sxs-lookup"><span data-stu-id="7a926-136">Another connects to a local ISP circuit.</span></span> <span data-ttu-id="7a926-137">L’appareil SD-WAN achemine le trafic réseau de catégorie Optimiser et Autoriser sur le lien du fournisseur de services Internet.</span><span class="sxs-lookup"><span data-stu-id="7a926-137">The SD-WAN device routes Optimize and Allow category network traffic over the ISP link.</span></span>

## <a name="the-contoso-line-of-business-app-infrastructure"></a><span data-ttu-id="7a926-138">Infrastructure d’application métier contoso</span><span class="sxs-lookup"><span data-stu-id="7a926-138">The Contoso line-of-business app infrastructure</span></span>

<span data-ttu-id="7a926-139">Contoso a conçu son infrastructure d’application métier et d’intranet de serveur pour les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7a926-139">Contoso architected its line-of-business application and server intranet infrastructure for the following:</span></span>

- <span data-ttu-id="7a926-140">Les succursales utilisent des serveurs de mise en cache locale pour stocker les documents et les sites web internes les plus sollicités.</span><span class="sxs-lookup"><span data-stu-id="7a926-140">Satellite offices use local caching servers to store frequently accessed documents and internal web sites.</span></span>
- <span data-ttu-id="7a926-p107">Les centres régionaux utilisent les serveurs d’applications régionaux pour les bureaux régionaux et les succursales. Ces serveurs se synchronisent avec les serveurs du siège social à Paris.</span><span class="sxs-lookup"><span data-stu-id="7a926-p107">Regional hubs use regional application servers for the regional and satellite offices. These servers synchronize with servers in the Paris headquarters.</span></span>
- <span data-ttu-id="7a926-143">Les centres de l’Université de Paris contiennent des serveurs d’applications centralisées qui servent l’ensemble de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="7a926-143">The Paris campus datacenters contain centralized application servers that serve the entire organization.</span></span>

<span data-ttu-id="7a926-144">La figure 2 montre le pourcentage de capacité de trafic réseau utilisé lors de l’accès aux serveurs sur l’intranet contoso.</span><span class="sxs-lookup"><span data-stu-id="7a926-144">Figure 2 shows the percentage of network traffic capacity used when accessing servers across the Contoso intranet.</span></span>

![L’infrastructure contoso pour les applications internes](../media/contoso-networking/contoso-networking-fig2.png)
 
<span data-ttu-id="7a926-146">**Figure 2 : infrastructure contoso pour les applications internes**</span><span class="sxs-lookup"><span data-stu-id="7a926-146">**Figure 2: The Contoso infrastructure for internal applications**</span></span>

<span data-ttu-id="7a926-147">Pour les bureaux satellites ou régionaux satellites, 60% des ressources nécessaires aux employés peuvent être pris en charge par les serveurs Office Hub et régionaux satellites.</span><span class="sxs-lookup"><span data-stu-id="7a926-147">For the satellite or regional hub offices, 60 percent of the resources needed by employees can be served by satellite and regional hub office servers.</span></span> <span data-ttu-id="7a926-148">Les demandes de ressources supplémentaires 40% doivent passer par la liaison WAN vers le campus de Paris.</span><span class="sxs-lookup"><span data-stu-id="7a926-148">The additional 40 percent of resource requests must go over the WAN link to the Paris campus.</span></span>

## <a name="network-analysis-and-preparation-for-microsoft-365-for-enterprise"></a><span data-ttu-id="7a926-149">Analyse et préparation réseau pour Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="7a926-149">Network analysis and preparation for Microsoft 365 for enterprise</span></span>

<span data-ttu-id="7a926-150">L’adoption réussie de Microsoft 365 pour Enterprise Services par les utilisateurs de contoso dépend de la connectivité hautement disponible et performante à Internet ou directement aux services Cloud de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7a926-150">Successful adoption of Microsoft 365 for enterprise services by Contoso users depends on highly available and performant connectivity to the internet or directly to Microsoft cloud services.</span></span> <span data-ttu-id="7a926-151">Contoso a effectué les étapes suivantes pour planifier et implémenter une connectivité optimisée à Microsoft 365 pour les services Cloud d’entreprise :</span><span class="sxs-lookup"><span data-stu-id="7a926-151">Contoso took these steps to plan and implement optimized connectivity to Microsoft 365 for enterprise cloud services:</span></span>

1. <span data-ttu-id="7a926-152">Création d’un diagramme réseau WAN d’entreprise pour faciliter la planification</span><span class="sxs-lookup"><span data-stu-id="7a926-152">Create a company WAN network diagram to aid with planning</span></span>

   <span data-ttu-id="7a926-153">Pour démarrer sa planification réseau, Contoso a créé un diagramme indiquant son emplacement de bureau, la connectivité réseau existante, les périphériques de périmètre réseau existants et les classes de service qui sont gérées sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="7a926-153">To start their network planning, Contoso created a diagram showing their office locations, existing network connectivity, existing network perimeter devices, and classes of service that are managed on the network.</span></span> <span data-ttu-id="7a926-154">Ils ont utilisé ce diagramme pour chaque étape suivante de la planification et de l’implémentation de la connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="7a926-154">They used this diagram for each subsequent step in the planning and implementation of networking connectivity.</span></span>

2. <span data-ttu-id="7a926-155">Création d’un plan pour Microsoft 365 pour la connectivité réseau d’entreprise</span><span class="sxs-lookup"><span data-stu-id="7a926-155">Create a plan for Microsoft 365 for enterprise network connectivity</span></span>

   <span data-ttu-id="7a926-156">Contoso a utilisé les [principes de connectivité réseau de microsoft 365](microsoft-365-network-connectivity-principles.md) et des exemples d’architectures réseau de référence pour identifier SD-WAN comme la topologie préférée de la connectivité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7a926-156">Contoso used the [Microsoft 365 network connectivity principles](microsoft-365-network-connectivity-principles.md) and sample reference network architectures to identify SD-WAN as their preferred topology for Microsoft 365 connectivity.</span></span>

3. <span data-ttu-id="7a926-157">Analyse de l’utilisation de la connexion Internet et de la bande passante MPLS-WAN au niveau de chaque bureau, et augmentation de la bande passante selon les besoins</span><span class="sxs-lookup"><span data-stu-id="7a926-157">Analyze internet-connection utilization and MPLS-WAN bandwidth at each office, and increase bandwidth as needed</span></span>

   <span data-ttu-id="7a926-158">L’utilisation actuelle de chaque Office a été analysée, et les circuits ont été augmentés de manière à ce que le trafic Cloud Microsoft 365 prévu fonctionne avec une moyenne de 20% de capacité inutilisée.</span><span class="sxs-lookup"><span data-stu-id="7a926-158">Each office's current usage was analyzed, and circuits were increased so that predicted Microsoft 365 cloud-based traffic would operate with an average of 20-percent unused capacity.</span></span>

4. <span data-ttu-id="7a926-159">Optimiser les performances vers les services réseau Microsoft</span><span class="sxs-lookup"><span data-stu-id="7a926-159">Optimize performance to Microsoft network services</span></span>

   <span data-ttu-id="7a926-160">Contoso a déterminé l’ensemble des points de terminaison Office 365, Intune et Azure et configuré des pare-feu, des périphériques de sécurité et d’autres systèmes sur Internet pour des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="7a926-160">Contoso determined the set of Office 365, Intune, and Azure endpoints and configured firewalls, security devices, and other systems in the internet path for optimal performance.</span></span> <span data-ttu-id="7a926-161">Les points de terminaison pour Office 365 optimiser et autoriser le trafic de catégorie ont été configurés sur les périphériques SD-WAN pour le routage via le circuit du fournisseur de services Internet.</span><span class="sxs-lookup"><span data-stu-id="7a926-161">Endpoints for Office 365 Optimize and Allow category traffic were configured into the SD-WAN devices for routing over the ISP circuit.</span></span>

5. <span data-ttu-id="7a926-162">Configurer le DNS interne</span><span class="sxs-lookup"><span data-stu-id="7a926-162">Configure internal DNS</span></span>

   <span data-ttu-id="7a926-163">Le DNS doit être fonctionnel et le trafic Microsoft 365 doit y être vérifié.</span><span class="sxs-lookup"><span data-stu-id="7a926-163">DNS is required to be functional and to be looked up locally for Microsoft 365 traffic.</span></span>

6. <span data-ttu-id="7a926-164">Valider le point de terminaison réseau et la connectivité de ports</span><span class="sxs-lookup"><span data-stu-id="7a926-164">Validate network endpoint and port connectivity</span></span>

   <span data-ttu-id="7a926-165">Contoso a exécuté les outils de test de connectivité réseau Microsoft pour valider la connectivité pour Microsoft 365 pour les services Cloud d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="7a926-165">Contoso ran Microsoft network connectivity test tools to validate connectivity for Microsoft 365 for enterprise cloud services.</span></span>

7. <span data-ttu-id="7a926-166">Optimiser les ordinateurs des employés pour la connectivité réseau</span><span class="sxs-lookup"><span data-stu-id="7a926-166">Optimize employee computers for network connectivity</span></span>

   <span data-ttu-id="7a926-167">Des ordinateurs individuels ont été vérifiés pour s’assurer que les dernières mises à jour du système d’exploitation ont été installées et que la surveillance de la sécurité du point de terminaison était active sur tous les clients.</span><span class="sxs-lookup"><span data-stu-id="7a926-167">Individual computers were checked to ensure that the latest operating system updates were installed and that endpoint security monitoring was active on all clients.</span></span>

## <a name="next-step"></a><span data-ttu-id="7a926-168">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="7a926-168">Next step</span></span>

<span data-ttu-id="7a926-169">Découvrez comment Contoso [exploite ses services de domaine Active Directory locaux dans le Cloud](contoso-identity.md) pour les employés et la Fédération de l’authentification pour les clients et les partenaires commerciaux.</span><span class="sxs-lookup"><span data-stu-id="7a926-169">Learn how Contoso is [leveraging its on-premises Active Directory Domain Services in the cloud](contoso-identity.md) for employees and federating authentication for customers and business partners.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a926-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a926-170">See also</span></span>

[<span data-ttu-id="7a926-171">Feuille de route de mise en réseau pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7a926-171">Networking roadmap for Microsoft 365</span></span>](networking-roadmap-microsoft-365.md)

[<span data-ttu-id="7a926-172">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="7a926-172">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="7a926-173">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="7a926-173">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)
