---
title: Feuille de route de mise en réseau pour Microsoft 365
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 08/10/2020
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Feuille de route pour l’implémentation de la mise en réseau Microsoft 365.
ms.openlocfilehash: 93d0f253e098815139b431a826f7e5e7a0410b37
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689910"
---
# <a name="networking-roadmap-for-microsoft-365"></a><span data-ttu-id="ec2ed-103">Feuille de route de mise en réseau pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ec2ed-103">Networking roadmap for Microsoft 365</span></span>

<span data-ttu-id="ec2ed-104">Microsoft 365 for Enterprise inclut des services Cloud de collaboration et de productivité, Microsoft Intune, ainsi que de nombreux services d’identité et de sécurité de Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-104">Microsoft 365 for enterprise includes collaboration and productivity cloud services, Microsoft Intune, and many identity and security services of Microsoft Azure.</span></span> <span data-ttu-id="ec2ed-105">Tous ces services cloud s’appuient sur la sécurité, les performances et la fiabilité des connexions à partir d’appareils clients via Internet ou des circuits dédiés.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-105">All of these cloud-based services rely on the security, performance, and reliability of connections from client devices over the Internet or dedicated circuits.</span></span> <span data-ttu-id="ec2ed-106">Pour héberger ces services et les rendre accessibles aux clients dans le monde entier, Microsoft a conçu une infrastructure réseau qui met en évidence les performances et l’intégration.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-106">To host these services and make them available to customers all over the world, Microsoft has designed a networking infrastructure that emphasizes performance and integration.</span></span> 

<span data-ttu-id="ec2ed-107">Une partie essentielle de votre intégration Microsoft 365 est de vous assurer que vos connexions réseau et Internet sont configurées pour un accès optimisé.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-107">A crucial part of your Microsoft 365 onboarding is to ensure that your network and Internet connections are set up for optimized access.</span></span> <span data-ttu-id="ec2ed-108">La configuration de votre réseau local pour accéder à un nuage Software-as-a-service distribué globalement est différente d’un réseau traditionnel qui est optimisé pour le trafic vers des centres de contenu locaux et une connexion Internet centrale.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-108">Configuring your on-premises network to access a globally distributed Software-as-a-Service (SaaS) cloud is different from a traditional network that is optimized for traffic to on-premises datacenters and a central Internet connection.</span></span> 

<span data-ttu-id="ec2ed-109">Utilisez ces articles pour comprendre les différences clés et modifier vos équipements de périmètre, ordinateurs clients et réseau local pour obtenir les meilleures performances de la part de vos utilisateurs locaux.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-109">Use these articles to understand the key differences and to modify your edge devices, client computers, and on-premises network to get the best performance for your on-premises users.</span></span>

## <a name="plan"></a><span data-ttu-id="ec2ed-110">Offre</span><span class="sxs-lookup"><span data-stu-id="ec2ed-110">Plan</span></span>

<span data-ttu-id="ec2ed-111">Lors de la phase de planification de votre implémentation réseau :</span><span class="sxs-lookup"><span data-stu-id="ec2ed-111">In the planning phase of your networking implementation:</span></span>

- [<span data-ttu-id="ec2ed-112">Comprendre le fonctionnement de la mise en réseau Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ec2ed-112">Understand how Microsoft 365 networking works</span></span>](microsoft-365-networking-overview.md)
- [<span data-ttu-id="ec2ed-113">Évaluer votre connectivité réseau actuelle</span><span class="sxs-lookup"><span data-stu-id="ec2ed-113">Assess your current network connectivity</span></span>](assessing-network-connectivity.md)
- [<span data-ttu-id="ec2ed-114">Déterminer si ExpressRoute est approprié pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="ec2ed-114">Determine if ExpressRoute is right for your organization</span></span>](network-planning-with-expressroute.md)
- [<span data-ttu-id="ec2ed-115">Planifier les périphériques réseau</span><span class="sxs-lookup"><span data-stu-id="ec2ed-115">Plan for your network devices</span></span>](plan-for-network-devices.md)
- [<span data-ttu-id="ec2ed-116">Configurer votre réseau pour la migration</span><span class="sxs-lookup"><span data-stu-id="ec2ed-116">Get your network set up for migration</span></span>](network-and-migration-planning.md)

## <a name="deploy"></a><span data-ttu-id="ec2ed-117">Déployer</span><span class="sxs-lookup"><span data-stu-id="ec2ed-117">Deploy</span></span>

<span data-ttu-id="ec2ed-118">Dans la phase de déploiement de votre implémentation réseau :</span><span class="sxs-lookup"><span data-stu-id="ec2ed-118">In the deployment phase of your networking implementation:</span></span>

- [<span data-ttu-id="ec2ed-119">Vérifier que votre réseau d’entreprise est optimisé pour la connectivité de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ec2ed-119">Ensure your enterprise network is optimized for Microsoft 365 connectivity</span></span>](set-up-network-for-microsoft-365.md)
- [<span data-ttu-id="ec2ed-120">Ajouter les domaines DNS pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="ec2ed-120">Add the DNS domains for your organization</span></span>](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain)
- [<span data-ttu-id="ec2ed-121">Optimiser votre connectivité aux points de terminaison Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ec2ed-121">Optimize your connectivity to Microsoft 365 endpoints</span></span>](microsoft-365-ip-web-service.md)
- [<span data-ttu-id="ec2ed-122">Optimiser la connectivité pour les travailleurs distants</span><span class="sxs-lookup"><span data-stu-id="ec2ed-122">Optimize connectivity for remote workers</span></span>](microsoft-365-vpn-split-tunnel.md)
- <span data-ttu-id="ec2ed-123">Si nécessaire, [configurez ExpressRoute](azure-expressroute.md)</span><span class="sxs-lookup"><span data-stu-id="ec2ed-123">If needed, [configure ExpressRoute](azure-expressroute.md)</span></span>

## <a name="manage"></a><span data-ttu-id="ec2ed-124">Gestion</span><span class="sxs-lookup"><span data-stu-id="ec2ed-124">Manage</span></span>

<span data-ttu-id="ec2ed-125">Dans la phase de gestion de votre implémentation réseau :</span><span class="sxs-lookup"><span data-stu-id="ec2ed-125">In the management phase of your networking implementation:</span></span>

- [<span data-ttu-id="ec2ed-126">Vérifier que les périphériques réseau utilisent les derniers points de terminaison Office 365</span><span class="sxs-lookup"><span data-stu-id="ec2ed-126">Ensure that your network devices are using the latest Office 365 endpoints</span></span>](microsoft-365-endpoints.md)
- [<span data-ttu-id="ec2ed-127">Surveiller et régler les performances de votre réseau</span><span class="sxs-lookup"><span data-stu-id="ec2ed-127">Monitor and tune your networking performance</span></span>](network-planning-and-performance.md)
- [<span data-ttu-id="ec2ed-128">Surveiller vos connexions ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ec2ed-128">Monitor your ExpressRoute connections</span></span>](managing-expressroute-for-connectivity.md)

## <a name="network-equipment-vendors"></a><span data-ttu-id="ec2ed-129">Fournisseurs d’équipement réseau</span><span class="sxs-lookup"><span data-stu-id="ec2ed-129">Network equipment vendors</span></span>

<span data-ttu-id="ec2ed-130">Si vous êtes un fournisseur d’équipement réseau, participez au [programme de partenariat réseau Microsoft 365](microsoft-365-networking-partner-program.md).</span><span class="sxs-lookup"><span data-stu-id="ec2ed-130">If you are a network equipment vendor, join the [Microsoft 365 Networking Partner Program](microsoft-365-networking-partner-program.md).</span></span> <span data-ttu-id="ec2ed-131">Inscrivez-vous au programme pour créer des principes de connectivité réseau Microsoft 365 dans vos produits et solutions.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-131">Enroll in the program to build Microsoft 365 network connectivity principles into your products and solutions.</span></span> 

## <a name="how-contoso-did-networking-for-microsoft-365"></a><span data-ttu-id="ec2ed-132">Mise en réseau de contoso pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ec2ed-132">How Contoso did networking for Microsoft 365</span></span>

<span data-ttu-id="ec2ed-133">Découvrez comment Contoso Corporation, une entreprise multinationale fictive mais représentative, [a optimisé ses appareils réseau et ses connexions Internet](contoso-networking.md) pour les services cloud Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-133">See how the Contoso Corporation, a fictional but representative multi-national business, [optimized their network devices and Internet connections](contoso-networking.md) for Microsoft 365 cloud services.</span></span>

![Société Contoso](../media/contoso-overview/contoso-icon.png)

## <a name="next-step"></a><span data-ttu-id="ec2ed-135">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="ec2ed-135">Next step</span></span>

<span data-ttu-id="ec2ed-136">Commencez votre planification de mise en réseau à l’aide de la [vue d’ensemble de la connectivité réseau Microsoft 365](microsoft-365-networking-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ec2ed-136">Start your networking planning with the [Microsoft 365 networking connectivity overview](microsoft-365-networking-overview.md).</span></span>
