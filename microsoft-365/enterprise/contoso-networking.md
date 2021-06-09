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
description: Comprendre l’infrastructure réseau contoso et la façon dont l’entreprise utilise sa technologie SD-WAN pour optimiser les performances réseau pour Microsoft 365 services cloud d’entreprise.
ms.openlocfilehash: d5f3581b81d33bdc200321692b82d57a96d09298
ms.sourcegitcommit: 66b8fc1d8ba4f17487cd2004ac19cf2fff472f3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2020
ms.locfileid: "48754013"
---
# <a name="networking-for-the-contoso-corporation"></a><span data-ttu-id="600d4-103">Mise en réseau de Contoso Corporation</span><span class="sxs-lookup"><span data-stu-id="600d4-103">Networking for the Contoso Corporation</span></span>

<span data-ttu-id="600d4-104">Pour adopter une infrastructure cloud inclusive, Contoso a conçu un changement fondamental dans la façon dont le trafic réseau vers les services cloud se déplace.</span><span class="sxs-lookup"><span data-stu-id="600d4-104">To adopt a cloud-inclusive infrastructure, Contoso devised a fundamental shift in how network traffic to cloud services travels.</span></span> <span data-ttu-id="600d4-105">Au lieu d’un modèle interne de hub-and-spoke qui met l’accent sur la connectivité réseau et le trafic pour le niveau suivant de la hiérarchie office, ils mappent les emplacements utilisateur à la sortie Internet locale et aux connexions locales vers l’emplacement réseau Microsoft 365 le plus proche sur Internet.</span><span class="sxs-lookup"><span data-stu-id="600d4-105">Instead of an internal hub-and-spoke model that focuses network connectivity and traffic for the next level of the office hierarchy, they mapped user locations to local internet egress and local connections to the closest Microsoft 365 network location on the internet.</span></span>

## <a name="networking-infrastructure"></a><span data-ttu-id="600d4-106">Infrastructure réseau</span><span class="sxs-lookup"><span data-stu-id="600d4-106">Networking infrastructure</span></span>

<span data-ttu-id="600d4-107">Voici les éléments réseau qui relient les bureaux Contoso dans le monde entier :</span><span class="sxs-lookup"><span data-stu-id="600d4-107">These are the network elements that link Contoso offices across the globe:</span></span>

- <span data-ttu-id="600d4-108">Réseau étendu de commutation multiprotocole WAN (MPLS) </span><span class="sxs-lookup"><span data-stu-id="600d4-108">Multiprotocol Label Switching (MPLS) WAN network</span></span>

  <span data-ttu-id="600d4-109">Un réseau WAN MPLS connecte le siège social parisien aux bureaux régionaux et régionaux aux succursales dans une configuration de hub.</span><span class="sxs-lookup"><span data-stu-id="600d4-109">An MPLS WAN network connects the Paris headquarters to regional offices and regional offices to satellite offices in a spoke-and-hub configuration.</span></span> <span data-ttu-id="600d4-110">Le réseau permet aux utilisateurs d’accéder aux serveurs locaux qui sont des applications métier au siège social parisien.</span><span class="sxs-lookup"><span data-stu-id="600d4-110">The network enables users to access on-premises servers that make up line-of-business applications in the Paris headquarters.</span></span> <span data-ttu-id="600d4-111">Il a également pour effet d’router tout trafic Internet générique vers le bureau parisien, où les appareils de sécurité réseau excursent les demandes.</span><span class="sxs-lookup"><span data-stu-id="600d4-111">It also routes any generic internet traffic to the Paris office, where network security devices scrub the requests.</span></span> <span data-ttu-id="600d4-112">Dans chaque bureau, les routeurs livrent le trafic aux hôtes câblés ou aux points d’accès sans fil sur les sous-réseaux, qui utilisent l’espace d’adressa visite IP privé.</span><span class="sxs-lookup"><span data-stu-id="600d4-112">Within each office, routers deliver traffic to wired hosts or wireless access points on subnets, which use the private IP address space.</span></span>

- <span data-ttu-id="600d4-113">Accès Internet direct local pour le trafic Microsoft 365 réseau</span><span class="sxs-lookup"><span data-stu-id="600d4-113">Local direct internet access for Microsoft 365 traffic</span></span>

  <span data-ttu-id="600d4-114">Chaque bureau dispose d’un périphérique de réseau wan (SD-WAN) défini par logiciel qui dispose d’un ou de plusieurs circuits réseau isp Internet locaux avec sa propre connectivité Internet via un serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="600d4-114">Each office has a software-defined WAN (SD-WAN) device that has one or more local internet ISP network circuits with its own internet connectivity through a proxy server.</span></span> <span data-ttu-id="600d4-115">Cela est généralement implémenté sous la mesure d’une liaison wan vers un isp local qui fournit également des adresses IP publiques et un serveur DNS local.</span><span class="sxs-lookup"><span data-stu-id="600d4-115">This is typically implemented as a WAN link to a local ISP that also provides public IP addresses and a local DNS server.</span></span>

- <span data-ttu-id="600d4-116">Présence sur Internet</span><span class="sxs-lookup"><span data-stu-id="600d4-116">Internet presence</span></span>

  <span data-ttu-id="600d4-117">Contoso possède le nom de domaine public contoso \. com.</span><span class="sxs-lookup"><span data-stu-id="600d4-117">Contoso owns the contoso\.com public domain name.</span></span> <span data-ttu-id="600d4-118">Le site web public contoso pour la commande de produits est un ensemble de serveurs dans un centre de données connecté à Internet sur le campus parisien.</span><span class="sxs-lookup"><span data-stu-id="600d4-118">The Contoso public web site for ordering products is a set of servers in an internet-connected datacenter in the Paris campus.</span></span> <span data-ttu-id="600d4-119">Contoso utilise une plage d’adresses IP publiques /24 sur Internet.</span><span class="sxs-lookup"><span data-stu-id="600d4-119">Contoso uses a /24 public IP address range on the internet.</span></span>

<span data-ttu-id="600d4-120">La figure 1 illustre l’infrastructure réseau contoso et ses connexions à Internet.</span><span class="sxs-lookup"><span data-stu-id="600d4-120">Figure 1 shows the Contoso networking infrastructure and its connections to the internet.</span></span>

![Le réseau Contoso](../media/contoso-networking/contoso-networking-fig1.png)
 
<span data-ttu-id="600d4-122">**Figure 1 : Réseau Contoso**</span><span class="sxs-lookup"><span data-stu-id="600d4-122">**Figure 1: The Contoso network**</span></span>

## <a name="use-of-sd-wan-for-optimal-network-connectivity-to-microsoft"></a><span data-ttu-id="600d4-123">Utilisation de la technologie SD-WAN pour la connectivité réseau optimale à Microsoft</span><span class="sxs-lookup"><span data-stu-id="600d4-123">Use of SD-WAN for optimal network connectivity to Microsoft</span></span>

<span data-ttu-id="600d4-124">Contoso a suivi les [principes de connectivité réseau Microsoft 365](microsoft-365-network-connectivity-principles.md) pour :</span><span class="sxs-lookup"><span data-stu-id="600d4-124">Contoso followed [Microsoft 365 network connectivity principles](microsoft-365-network-connectivity-principles.md) to:</span></span>

- <span data-ttu-id="600d4-125">Identification et différenciation du trafic réseau Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="600d4-125">Identify and differentiate Microsoft 365 network traffic</span></span>
- <span data-ttu-id="600d4-126">Sortir les connexions réseau localement</span><span class="sxs-lookup"><span data-stu-id="600d4-126">Egress network connections locally</span></span>
- <span data-ttu-id="600d4-127">Éviter les épingles de réseau</span><span class="sxs-lookup"><span data-stu-id="600d4-127">Avoid network hairpins</span></span>
- <span data-ttu-id="600d4-128">Ignorer les périphériques de sécurité réseau en double</span><span class="sxs-lookup"><span data-stu-id="600d4-128">Bypass duplicate network security devices</span></span>

<span data-ttu-id="600d4-129">Il existe trois catégories de trafic réseau pour Microsoft 365 : *Optimiser,* Autoriser *et* *Par défaut.*</span><span class="sxs-lookup"><span data-stu-id="600d4-129">There are three categories of network traffic for Microsoft 365: *Optimize*, *Allow*, and *Default*.</span></span> <span data-ttu-id="600d4-130">Le trafic Optimiser et Autoriser est un trafic réseau approuvé chiffré et sécurisé aux points de terminaison et destiné au Microsoft 365 réseau.</span><span class="sxs-lookup"><span data-stu-id="600d4-130">Optimize and Allow traffic is trusted network traffic that's encrypted and secured at the endpoints and is destined for the Microsoft 365 network.</span></span>

<span data-ttu-id="600d4-131">Contoso a décidé d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="600d4-131">Contoso decided to:</span></span>

- <span data-ttu-id="600d4-132">Utilisez la sortie Internet directe pour optimiser et autoriser le trafic de catégorie et pour le trafic de catégorie Par défaut vers la connexion Internet centrale basée à Paris.</span><span class="sxs-lookup"><span data-stu-id="600d4-132">Use direct internet egress for Optimize and Allow category traffic and to forward all Default category traffic to the Paris-based central internet connection.</span></span>

- <span data-ttu-id="600d4-133">Déployez des périphériques SD-WAN à chaque bureau comme moyen simple de suivre ces principes et d’obtenir des performances réseau optimales pour Microsoft 365 services informatiques.</span><span class="sxs-lookup"><span data-stu-id="600d4-133">Deploy SD-WAN devices at each office as a simple way to follow these principles and achieve optimal network performance for Microsoft 365 cloud-based services.</span></span>

  <span data-ttu-id="600d4-134">Les appareils SD-WAN ont un port réseau local LAN pour le réseau local et plusieurs ports WAN.</span><span class="sxs-lookup"><span data-stu-id="600d4-134">The SD-WAN devices have a LAN port for the local office network and multiple WAN ports.</span></span> <span data-ttu-id="600d4-135">Un port WAN se connecte à son réseau MPLS.</span><span class="sxs-lookup"><span data-stu-id="600d4-135">One WAN port connects to their MPLS network.</span></span> <span data-ttu-id="600d4-136">Un autre se connecte à un circuit isp local.</span><span class="sxs-lookup"><span data-stu-id="600d4-136">Another connects to a local ISP circuit.</span></span> <span data-ttu-id="600d4-137">L’appareil SD-WAN achemine le trafic réseau de catégorie Optimiser et Autoriser sur le lien du fournisseur de services Internet.</span><span class="sxs-lookup"><span data-stu-id="600d4-137">The SD-WAN device routes Optimize and Allow category network traffic over the ISP link.</span></span>

## <a name="the-contoso-line-of-business-app-infrastructure"></a><span data-ttu-id="600d4-138">Infrastructure d’applications métier Contoso</span><span class="sxs-lookup"><span data-stu-id="600d4-138">The Contoso line-of-business app infrastructure</span></span>

<span data-ttu-id="600d4-139">Contoso a conçu son infrastructure intranet d’application métier et de serveur pour les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="600d4-139">Contoso architected its line-of-business application and server intranet infrastructure for the following:</span></span>

- <span data-ttu-id="600d4-140">Les succursales utilisent des serveurs de mise en cache locale pour stocker les documents et les sites web internes les plus sollicités.</span><span class="sxs-lookup"><span data-stu-id="600d4-140">Satellite offices use local caching servers to store frequently accessed documents and internal web sites.</span></span>
- <span data-ttu-id="600d4-p107">Les centres régionaux utilisent les serveurs d’applications régionaux pour les bureaux régionaux et les succursales. Ces serveurs se synchronisent avec les serveurs du siège social à Paris.</span><span class="sxs-lookup"><span data-stu-id="600d4-p107">Regional hubs use regional application servers for the regional and satellite offices. These servers synchronize with servers in the Paris headquarters.</span></span>
- <span data-ttu-id="600d4-143">Les centres de données du campus parisien contiennent des serveurs d’applications centralisés qui servent l’ensemble de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="600d4-143">The Paris campus datacenters contain centralized application servers that serve the entire organization.</span></span>

<span data-ttu-id="600d4-144">La figure 2 montre le pourcentage de capacité du trafic réseau utilisé lors de l’accès aux serveurs sur l’intranet Contoso.</span><span class="sxs-lookup"><span data-stu-id="600d4-144">Figure 2 shows the percentage of network traffic capacity used when accessing servers across the Contoso intranet.</span></span>

![Infrastructure Contoso pour les applications internes](../media/contoso-networking/contoso-networking-fig2.png)
 
<span data-ttu-id="600d4-146">**Figure 2 : Infrastructure Contoso pour les applications internes**</span><span class="sxs-lookup"><span data-stu-id="600d4-146">**Figure 2: The Contoso infrastructure for internal applications**</span></span>

<span data-ttu-id="600d4-147">Pour les centres régionaux ou satellites, 60 % des ressources requises par les employés peuvent être servies par des serveurs de succursales et de centres régionaux.</span><span class="sxs-lookup"><span data-stu-id="600d4-147">For the satellite or regional hub offices, 60 percent of the resources needed by employees can be served by satellite and regional hub office servers.</span></span> <span data-ttu-id="600d4-148">Les 40 % de demandes de ressources supplémentaires doivent passer par la liaison WAN vers le campus parisien.</span><span class="sxs-lookup"><span data-stu-id="600d4-148">The additional 40 percent of resource requests must go over the WAN link to the Paris campus.</span></span>

## <a name="network-analysis-and-preparation-for-microsoft-365-for-enterprise"></a><span data-ttu-id="600d4-149">Analyse et préparation du réseau pour Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="600d4-149">Network analysis and preparation for Microsoft 365 for enterprise</span></span>

<span data-ttu-id="600d4-150">L’adoption Microsoft 365 pour les services d’entreprise par les utilisateurs de Contoso dépend d’une connectivité hautement disponible et performante à Internet ou directement aux services cloud de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="600d4-150">Successful adoption of Microsoft 365 for enterprise services by Contoso users depends on highly available and performant connectivity to the internet or directly to Microsoft cloud services.</span></span> <span data-ttu-id="600d4-151">Contoso a pris les mesures suivantes pour planifier et implémenter une connectivité optimisée Microsoft 365 pour les services cloud d’entreprise :</span><span class="sxs-lookup"><span data-stu-id="600d4-151">Contoso took these steps to plan and implement optimized connectivity to Microsoft 365 for enterprise cloud services:</span></span>

1. <span data-ttu-id="600d4-152">Créer un diagramme de réseau WAN d’entreprise pour faciliter la planification</span><span class="sxs-lookup"><span data-stu-id="600d4-152">Create a company WAN network diagram to aid with planning</span></span>

   <span data-ttu-id="600d4-153">Pour commencer la planification du réseau, Contoso a créé un diagramme montrant les emplacements de bureau, la connectivité réseau existante, les périphériques de périmètre réseau existants et les classes de service gérées sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="600d4-153">To start their network planning, Contoso created a diagram showing their office locations, existing network connectivity, existing network perimeter devices, and classes of service that are managed on the network.</span></span> <span data-ttu-id="600d4-154">Ils ont utilisé ce diagramme pour chaque étape suivante de la planification et de l’implémentation de la connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="600d4-154">They used this diagram for each subsequent step in the planning and implementation of networking connectivity.</span></span>

2. <span data-ttu-id="600d4-155">Créer un plan de Microsoft 365 pour la connectivité réseau d’entreprise</span><span class="sxs-lookup"><span data-stu-id="600d4-155">Create a plan for Microsoft 365 for enterprise network connectivity</span></span>

   <span data-ttu-id="600d4-156">Contoso a utilisé les principes Microsoft 365 de connectivité réseau et des [exemples](microsoft-365-network-connectivity-principles.md) d’architectures réseau de référence pour identifier SD-WAN comme topologie préférée pour la Microsoft 365 réseau.</span><span class="sxs-lookup"><span data-stu-id="600d4-156">Contoso used the [Microsoft 365 network connectivity principles](microsoft-365-network-connectivity-principles.md) and sample reference network architectures to identify SD-WAN as their preferred topology for Microsoft 365 connectivity.</span></span>

3. <span data-ttu-id="600d4-157">Analyser l’utilisation de la connexion Internet et la bande passante MPLS-WAN à chaque bureau et augmenter la bande passante selon les besoins</span><span class="sxs-lookup"><span data-stu-id="600d4-157">Analyze internet-connection utilization and MPLS-WAN bandwidth at each office, and increase bandwidth as needed</span></span>

   <span data-ttu-id="600d4-158">L’utilisation actuelle de chaque bureau a été analysée et les circuits ont été augmentés afin que le trafic informatique Microsoft 365 prévu fonctionne avec une capacité inutilisée moyenne de 20 %.</span><span class="sxs-lookup"><span data-stu-id="600d4-158">Each office's current usage was analyzed, and circuits were increased so that predicted Microsoft 365 cloud-based traffic would operate with an average of 20-percent unused capacity.</span></span>

4. <span data-ttu-id="600d4-159">Optimiser les performances pour les services réseau Microsoft</span><span class="sxs-lookup"><span data-stu-id="600d4-159">Optimize performance to Microsoft network services</span></span>

   <span data-ttu-id="600d4-160">Contoso a déterminé l’ensemble des points de terminaison Office 365, Intune et Azure, ainsi que des pare-feux, des périphériques de sécurité et d’autres systèmes configurés dans le chemin d’accès Internet pour des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="600d4-160">Contoso determined the set of Office 365, Intune, and Azure endpoints and configured firewalls, security devices, and other systems in the internet path for optimal performance.</span></span> <span data-ttu-id="600d4-161">Les points de terminaison pour Office 365 trafic de catégorie Optimiser et Autoriser ont été configurés dans les périphériques SD-WAN pour le routage sur le circuit isp.</span><span class="sxs-lookup"><span data-stu-id="600d4-161">Endpoints for Office 365 Optimize and Allow category traffic were configured into the SD-WAN devices for routing over the ISP circuit.</span></span>

5. <span data-ttu-id="600d4-162">Configurer le DNS interne</span><span class="sxs-lookup"><span data-stu-id="600d4-162">Configure internal DNS</span></span>

   <span data-ttu-id="600d4-163">Le DNS doit être fonctionnel et le trafic Microsoft 365 doit y être vérifié.</span><span class="sxs-lookup"><span data-stu-id="600d4-163">DNS is required to be functional and to be looked up locally for Microsoft 365 traffic.</span></span>

6. <span data-ttu-id="600d4-164">Valider la connectivité des points de terminaison et des ports réseau</span><span class="sxs-lookup"><span data-stu-id="600d4-164">Validate network endpoint and port connectivity</span></span>

   <span data-ttu-id="600d4-165">Contoso a mis en place des outils de test de connectivité réseau Microsoft pour valider la connectivité Microsoft 365 pour les services cloud d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="600d4-165">Contoso ran Microsoft network connectivity test tools to validate connectivity for Microsoft 365 for enterprise cloud services.</span></span>

7. <span data-ttu-id="600d4-166">Optimiser les ordinateurs des employés pour la connectivité réseau</span><span class="sxs-lookup"><span data-stu-id="600d4-166">Optimize employee computers for network connectivity</span></span>

   <span data-ttu-id="600d4-167">Les ordinateurs individuels ont été vérifiés pour s’assurer que les dernières mises à jour du système d’exploitation ont été installées et que la surveillance de la sécurité des points de terminaison était active sur tous les clients.</span><span class="sxs-lookup"><span data-stu-id="600d4-167">Individual computers were checked to ensure that the latest operating system updates were installed and that endpoint security monitoring was active on all clients.</span></span>

## <a name="next-step"></a><span data-ttu-id="600d4-168">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="600d4-168">Next step</span></span>

<span data-ttu-id="600d4-169">Découvrez comment Contoso exploite ses services de domaine [Active Directory](contoso-identity.md) locaux dans le cloud pour les employés et fédère l’authentification pour les clients et les partenaires commerciaux.</span><span class="sxs-lookup"><span data-stu-id="600d4-169">Learn how Contoso is [leveraging its on-premises Active Directory Domain Services in the cloud](contoso-identity.md) for employees and federating authentication for customers and business partners.</span></span>

## <a name="see-also"></a><span data-ttu-id="600d4-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="600d4-170">See also</span></span>

[<span data-ttu-id="600d4-171">Feuille de route réseau pour les Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="600d4-171">Networking roadmap for Microsoft 365</span></span>](networking-roadmap-microsoft-365.md)

[<span data-ttu-id="600d4-172">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="600d4-172">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="600d4-173">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="600d4-173">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)
