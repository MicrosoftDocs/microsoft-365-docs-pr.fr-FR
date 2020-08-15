---
title: Configurer votre réseau pour Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/19/2019
audience: ITPro
ms.topic: hub-page
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
f1.keywords:
- CSH
ms.custom:
- Ent_TLGs
- seo-marvel-apr2020
ms.assetid: ''
description: Accédez à des liens vers des articles contenant des informations pour vous aider à configurer votre réseau pour Microsoft 365, notamment une vue d’ensemble de la connectivité réseau et une liste de points de terminaison.
ms.openlocfilehash: f0e0499c70745d31399240372c190758285408aa
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689674"
---
# <a name="set-up-your-network-for-microsoft-365"></a><span data-ttu-id="cff75-103">Configurer votre réseau pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cff75-103">Set up your network for Microsoft 365</span></span>

<span data-ttu-id="cff75-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="cff75-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="cff75-105">Une partie importante de votre intégration Microsoft 365 est de vous assurer que vos connexions réseau et Internet sont configurées pour un accès optimisé.</span><span class="sxs-lookup"><span data-stu-id="cff75-105">An important part of your Microsoft 365 onboarding is to ensure that your network and Internet connections are set up for optimized access.</span></span> <span data-ttu-id="cff75-106">La configuration de votre réseau local pour accéder à un nuage Software-as-a-service distribué globalement est différente d’un réseau traditionnel qui est optimisé pour le trafic vers des centres de contenu locaux et une connexion Internet centrale.</span><span class="sxs-lookup"><span data-stu-id="cff75-106">Configuring your on-premises network to access a globally distributed Software-as-a-Service (SaaS) cloud is different from a traditional network that is optimized for traffic to on-premises datacenters and a central Internet connection.</span></span> 

<span data-ttu-id="cff75-107">Utilisez ces articles pour comprendre les différences clés et modifier vos équipements de périmètre, ordinateurs clients et réseau local pour obtenir les meilleures performances de la part de vos utilisateurs locaux.</span><span class="sxs-lookup"><span data-stu-id="cff75-107">Use these articles to understand the key differences and to modify your edge devices, client computers, and on-premises network to get the best performance for your on-premises users.</span></span>

## <a name="how-microsoft-365-networking-works"></a><span data-ttu-id="cff75-108">Fonctionnement de la mise en réseau Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cff75-108">How Microsoft 365 networking works</span></span>

<span data-ttu-id="cff75-109">Consultez les articles suivants pour obtenir une vue d’ensemble de la connectivité pour Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="cff75-109">See these articles for an overview of connectivity for Microsoft 365:</span></span>

- [<span data-ttu-id="cff75-110">Vue d’ensemble de la connectivité réseau Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cff75-110">Microsoft 365 networking connectivity overview</span></span>](microsoft-365-networking-overview.md)
- [<span data-ttu-id="cff75-111">Principes de connectivité réseau de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cff75-111">Microsoft 365 network connectivity principles</span></span>](microsoft-365-network-connectivity-principles.md)
- [<span data-ttu-id="cff75-112">Évaluation de la connectivité réseau Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cff75-112">Assessing Microsoft 365 network connectivity</span></span>](assessing-network-connectivity.md)

<span data-ttu-id="cff75-113">Pour obtenir des conseils sur l’amélioration des performances, voir [planification réseau et optimisation des performances pour Microsoft 365](network-planning-and-performance.md).</span><span class="sxs-lookup"><span data-stu-id="cff75-113">For advice on enhancing performance, see [Network planning and performance tuning for Microsoft 365](network-planning-and-performance.md).</span></span>

## <a name="support-microsoft-365-networking-as-a-network-equipment-vendor"></a><span data-ttu-id="cff75-114">Prise en charge de la mise en réseau Microsoft 365 en tant que fournisseur d’équipement réseau</span><span class="sxs-lookup"><span data-stu-id="cff75-114">Support Microsoft 365 networking as a network equipment vendor</span></span>

<span data-ttu-id="cff75-p102">Si vous êtes un fournisseur d’équipement réseau, rejoignez le[programme de partenariat mise en réseau d’Office 365](microsoft-365-networking-partner-program.md). Inscrivez-vous au programme pour développer les principes de connectivité réseau Office 365 dans vos produits et solutions.</span><span class="sxs-lookup"><span data-stu-id="cff75-p102">If you are a network equipment vendor, join the [Office 365 Networking Partner Program](microsoft-365-networking-partner-program.md). Enroll in the program to build Office 365 network connectivity principles into your products and solutions.</span></span> 

## <a name="office-365-endpoints"></a><span data-ttu-id="cff75-117">Points de terminaison Office 365</span><span class="sxs-lookup"><span data-stu-id="cff75-117">Office 365 endpoints</span></span>

<span data-ttu-id="cff75-118">Les points de terminaison sont l’ensemble des adresses IP de destination, noms de domaine DNS et URL pour le trafic sur Internet Office 365.</span><span class="sxs-lookup"><span data-stu-id="cff75-118">Endpoints are the set of destination IP addresses, DNS domain names, and URLs for Office 365 traffic on the Internet.</span></span> 

<span data-ttu-id="cff75-p103">Pour optimiser les performances aux services Office 365 basés sur le cloud, certains points de terminaison nécessitent une gestion spéciale par les autres navigateurs client et les appareils dans votre réseau de périmètre. Ces appareils incluent pare-feux, SSL Break and Inspect et des appareils d’inspection des paquets, et systèmes de protection contre la perte de données.</span><span class="sxs-lookup"><span data-stu-id="cff75-p103">To optimize performance to Office 365 cloud-based services, some endpoints need special handling by your client browsers and the devices in your edge network. These devices include firewalls, SSL Break and Inspect and packet inspection devices, and data loss prevention systems.</span></span>

<span data-ttu-id="cff75-121">Voir [Gestion des points de terminaison d’Office 365 ](managing-office-365-endpoints.md) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="cff75-121">See [Managing Office 365 endpoints](managing-office-365-endpoints.md) for the details.</span></span>

<span data-ttu-id="cff75-p104">Il existe actuellement cinq différents clouds Office 365. Ce tableau vous permet d’accéder à la liste des points de terminaison pour chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="cff75-p104">There are currently five different Office 365 clouds. This table takes you to the list of endpoints for each one.</span></span>

| <span data-ttu-id="cff75-124">Points de terminaison</span><span class="sxs-lookup"><span data-stu-id="cff75-124">Endpoints</span></span> | <span data-ttu-id="cff75-125">Description</span><span class="sxs-lookup"><span data-stu-id="cff75-125">Description</span></span> |
|:-------|:-----|
| [<span data-ttu-id="cff75-126">Points de terminaison internationaux</span><span class="sxs-lookup"><span data-stu-id="cff75-126">Worldwide endpoints</span></span>](urls-and-ip-address-ranges.md) | <span data-ttu-id="cff75-127">Les points de terminaison pour les abonnements Office 365 dans le monde, dont le États-Unis Government Community Cloud (GCC).</span><span class="sxs-lookup"><span data-stu-id="cff75-127">The endpoints for worldwide Office 365 subscriptions, which include the United States Government Community Cloud (GCC).</span></span> |
| [<span data-ttu-id="cff75-128">Points de terminaison DoD du gouvernement américain</span><span class="sxs-lookup"><span data-stu-id="cff75-128">U.S. Government DoD endpoints</span></span>](microsoft-365-u-s-government-dod-endpoints.md) | <span data-ttu-id="cff75-129">Les points de terminaison pour les abonnements aux États-Unis Department of Defense (DoD).</span><span class="sxs-lookup"><span data-stu-id="cff75-129">The endpoints for United States Department of Defense (DoD) subscriptions.</span></span> |
| [<span data-ttu-id="cff75-130">Points de terminaison GCC High du gouvernement américain</span><span class="sxs-lookup"><span data-stu-id="cff75-130">U.S. Government GCC High endpoints</span></span>](microsoft-365-u-s-government-gcc-high-endpoints.md) | <span data-ttu-id="cff75-131">Les points de terminaison pour les abonnements aux États-Unis pour le secteur public Communauté Cloud élevé (GCC élevé).</span><span class="sxs-lookup"><span data-stu-id="cff75-131">The endpoints for United States Government Community Cloud High (GCC High) subscriptions.</span></span> |
| [<span data-ttu-id="cff75-132">Office 365 géré par les points de terminaison 21Vianet</span><span class="sxs-lookup"><span data-stu-id="cff75-132">Office 365 operated by 21Vianet endpoints</span></span>](urls-and-ip-address-ranges-21vianet.md) | <span data-ttu-id="cff75-133">Les points de terminaison pour Office 365 géré par 21Vianet, qui est conçu pour répondre aux besoins d’Office 365 en Chine.</span><span class="sxs-lookup"><span data-stu-id="cff75-133">The endpoints for Office 365 operated by 21Vianet, which is designed to meet the needs for Office 365 in China.</span></span> |
| [<span data-ttu-id="cff75-134">Points de terminaison Office 365 Germany</span><span class="sxs-lookup"><span data-stu-id="cff75-134">Office 365 Germany endpoints</span></span>](microsoft-365-germany-endpoints.md) | <span data-ttu-id="cff75-135">Les points de terminaison pour un cloud en Europe distinct, pour les clients plus régulés en Allemagne, Union européenne (UE) et l’Association européenne de libre-échange (AELE).</span><span class="sxs-lookup"><span data-stu-id="cff75-135">The endpoints for a separate cloud in Europe for the most regulated customers in Germany, the European Union (EU), and the European Free Trade Association (EFTA).</span></span> |
|||

<span data-ttu-id="cff75-136">Pour automatiser l’obtention de la dernière liste des points de terminaison pour votre cloud Office 365, voir [Service web d’URL et d’adresses IP Office 365](microsoft-365-ip-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="cff75-136">To automate getting the latest list of endpoints for your Office 365 cloud, see the [Office 365 IP Address and URL Web service](microsoft-365-ip-web-service.md).</span></span>

<span data-ttu-id="cff75-137">Pour plus de points de terminaison, voir les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="cff75-137">For additional endpoints, see these articles:</span></span>

- [<span data-ttu-id="cff75-138">Autres points de terminaison supplémentaires non inclus dans les services web</span><span class="sxs-lookup"><span data-stu-id="cff75-138">Additional endpoints not included in the Web service</span></span>](additional-office365-ip-addresses-and-urls.md)
- [<span data-ttu-id="cff75-139">Requêtes réseau dans Office 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="cff75-139">Network requests in Office 2016 for Mac</span></span>](network-requests-in-office-2016-for-mac.md)


## <a name="additional-topics-for-microsoft-365-networking"></a><span data-ttu-id="cff75-140">Rubriques supplémentaires pour Microsoft 365 Networking</span><span class="sxs-lookup"><span data-stu-id="cff75-140">Additional topics for Microsoft 365 networking</span></span>

<span data-ttu-id="cff75-141">Consultez les articles suivants pour obtenir des rubriques spécialisées sur la mise en réseau Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="cff75-141">See these articles for specialized topics in Microsoft 365 networking:</span></span>

- [<span data-ttu-id="cff75-142">Réseaux de distribution de contenu</span><span class="sxs-lookup"><span data-stu-id="cff75-142">Content delivery networks</span></span>](content-delivery-networks.md)
- [<span data-ttu-id="cff75-143">Prise en charge du protocole IPv6 dans les services Office 365</span><span class="sxs-lookup"><span data-stu-id="cff75-143">IPv6 support in Office 365 services</span></span>](ipv6-support.md)
- [<span data-ttu-id="cff75-144">Prise en charge de la traduction d’adresses réseau (NAT) avec Office 365</span><span class="sxs-lookup"><span data-stu-id="cff75-144">NAT support with Office 365</span></span>](nat-support-with-microsoft-365.md)

## <a name="expressroute-for-microsoft-365"></a><span data-ttu-id="cff75-145">ExpressRoute pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cff75-145">ExpressRoute for Microsoft 365</span></span>

<span data-ttu-id="cff75-146">Consultez les articles suivants pour plus d’informations sur l’utilisation d’ExpressRoute pour le trafic Office 365 :</span><span class="sxs-lookup"><span data-stu-id="cff75-146">See these articles for information on the use of ExpressRoute for Office 365 traffic:</span></span>

- [<span data-ttu-id="cff75-147">Azure ExpressRoute pour Office 365</span><span class="sxs-lookup"><span data-stu-id="cff75-147">Azure ExpressRoute for Office 365</span></span>](azure-expressroute.md)
- [<span data-ttu-id="cff75-148">Implémentation d’ExpressRoute pour Office 365</span><span class="sxs-lookup"><span data-stu-id="cff75-148">Implementing ExpressRoute for Office 365</span></span>](implementing-expressroute.md)
- [<span data-ttu-id="cff75-149">Planification de réseau avec ExpressRoute pour Office 365</span><span class="sxs-lookup"><span data-stu-id="cff75-149">Network planning with ExpressRoute for Office 365</span></span>](network-planning-with-expressroute.md)
- [<span data-ttu-id="cff75-150">Routage avec ExpressRoute pour Office 365</span><span class="sxs-lookup"><span data-stu-id="cff75-150">Routing with ExpressRoute for Office 365</span></span>](routing-with-expressroute.md)
