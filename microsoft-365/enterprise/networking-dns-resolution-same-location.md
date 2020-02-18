---
title: 'Étape 2 : Configurer les connexions Internet locales pour chaque bureau'
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/23/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et configurez votre résolution DNS pour de meilleures performances.
ms.openlocfilehash: 8b4302c06e75c59a1b99eb60399c9df897ad17ea
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42066657"
---
# <a name="step-2-configure-local-internet-connections-for-each-office"></a><span data-ttu-id="75054-103">Étape 2 : Configurer les connexions Internet locales pour chaque bureau</span><span class="sxs-lookup"><span data-stu-id="75054-103">Step 2: Configure local Internet connections for each office</span></span>

<span data-ttu-id="75054-104">*Cette étape est requise et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="75054-104">*This step is required and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![Phase 1 : Réseau](../media/deploy-foundation-infrastructure/networking_icon-small.png)

<span data-ttu-id="75054-p101">À l’Étape 2, vous vérifiez que chacun de vos bureaux est équipé de connexions Internet locales et utilise des serveurs DNS locaux. Ces deux éléments sont requis pour réduire la latence de connexion et garantir que les ordinateurs clients locaux établissent des connexions avec le point d’entrée le plus proche aux services services cloud Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="75054-p101">In Step 2, you ensure that each of your offices have local Internet connections and use local DNS servers. Both of these elements are required to reduce connection latency and ensure that on-premises client computers make connections to the nearest point of entry to Microsoft 365 cloud-based services.</span></span>

<span data-ttu-id="75054-108">Dans les réseaux classiques pour les grandes organisations, le trafic Internet circule sur la structure fondamentale du réseau jusqu'à une connexion Internet centrale.</span><span class="sxs-lookup"><span data-stu-id="75054-108">In traditional networks for large organizations, Internet traffic travels across the network backbone to a central Internet connection.</span></span> <span data-ttu-id="75054-109">Cela ne fonctionne pas bien pour optimiser les performances d’une infrastructure de logiciel en tant que service (SaaS) distribuée dans le monde entier, qui inclut les produits Office 365 et Intune dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="75054-109">This does not work well for optimizing performance to a globally distributed Software-as-a-Service (SaaS) infrastructure, which includes the Office 365 and Intune products in Microsoft 365.</span></span>

<span data-ttu-id="75054-110">Le réseau mondial Microsoft inclut une infrastructure *de porte service distribuée*, une périphérie de réseau hautement disponible et évolutive avec des emplacements géographiquement répartis.</span><span class="sxs-lookup"><span data-stu-id="75054-110">The Microsoft Global Network includes a *Distributed Service Front Door* infrastructure, a highly available and scalable network edge with geographically distributed locations.</span></span> <span data-ttu-id="75054-111">Il met fin aux connexions des utilisateurs finaux sur un serveur frontal et achemine efficacement le trafic des utilisateurs finaux au sein du réseau mondial Microsoft.</span><span class="sxs-lookup"><span data-stu-id="75054-111">It terminates end user connections at a front door server and efficiently routes end user traffic within the Microsoft Global Network.</span></span>

![Le réseau mondial Microsoft](../media/networking-dns-resolution-same-location/microsoft-global-network.png)

<span data-ttu-id="75054-113">Pour de meilleures performances, les clients locaux doivent accéder à la porte principale la plus proche géographiquement, plutôt que d’envoyer le trafic sur une structure fondamentale du réseau et sur l’emplacement principal qui est le plus proche de la connexion Internet centrale de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="75054-113">For the best performance, on-premises clients should access a front door location that is geographically closest to them, rather than sending the traffic over a network backbone and to the front door that is closest to the organization’s central Internet connection.</span></span>

<span data-ttu-id="75054-114">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="75054-114">Here’s an example.</span></span>

![Exemple d’utilisation du réseau mondial Microsoft](../media/networking-dns-resolution-same-location/microsoft-global-network-example.png)

<span data-ttu-id="75054-116">Lorsqu’un utilisateur de la succursale de Paris souhaite accéder à un site SharePoint Online :</span><span class="sxs-lookup"><span data-stu-id="75054-116">When a user in the Paris branch office wants to access a SharePoint Online site:</span></span>

1. <span data-ttu-id="75054-117">Il envoie une requête DNS pour résoudre un nom, tel que contoso.sharepoint.com.</span><span class="sxs-lookup"><span data-stu-id="75054-117">It sends a DNS query to resolve a name, such as contoso.sharepoint.com.</span></span> 
2. <span data-ttu-id="75054-118">Le serveur DNS fourni par le fournisseur de services Internet transfère cette requête à un serveur DNS Microsoft.</span><span class="sxs-lookup"><span data-stu-id="75054-118">The DNS server provided by the ISP forwards that query to a Microsoft DNS server.</span></span>
3. <span data-ttu-id="75054-119">Les serveurs DNS de Microsoft font correspondre l'adresse IP source de la requête DNS transférée à la région du monde à laquelle cette adresse est attribuée.</span><span class="sxs-lookup"><span data-stu-id="75054-119">Microsoft’s DNS servers match the source IP address of the forwarded DNS query to the region of the world assigned that address.</span></span> <span data-ttu-id="75054-120">Le serveur DNS Microsoft répond à l’aide de l’adresse IP de la porte principale du réseau Microsoft la plus proche en Europe.</span><span class="sxs-lookup"><span data-stu-id="75054-120">The Microsoft DNS server responds with the IP address of the nearest Microsoft Network front door in Europe.</span></span>
4. <span data-ttu-id="75054-121">Le serveur DNS du fournisseur de services Internet envoie cette adresse IP à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="75054-121">The ISP DNS server sends that IP address to the user.</span></span>
5. <span data-ttu-id="75054-122">L’utilisateur établit une connexion au serveur SharePoint via la porte principale de l’Europe.</span><span class="sxs-lookup"><span data-stu-id="75054-122">The user initiates a connection to the SharePoint server through the Europe front door.</span></span>

<span data-ttu-id="75054-123">Pour diriger la demande d’un client vers la porte principale la plus proche géographiquement, les serveurs DNS de Microsoft utilisent des requêtes DNS correspondant à la demande de connexion initiale du client.</span><span class="sxs-lookup"><span data-stu-id="75054-123">To direct a client request to the geographically nearest front door, Microsoft’s DNS servers use the DNS queries corresponding the client’s initial connection request.</span></span> <span data-ttu-id="75054-124">Par conséquent, pour la latence de réseau la plus faible :</span><span class="sxs-lookup"><span data-stu-id="75054-124">Therefore, for the lowest network latency:</span></span>

- <span data-ttu-id="75054-125">Tous les bureaux de votre organisation doivent avoir des connexions Internet locales pour le trafic réseau de catégorie [Optimiser](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles#new-office-365-endpoint-categories).</span><span class="sxs-lookup"><span data-stu-id="75054-125">All offices of your organization should have local Internet connections for [Optimize](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles#new-office-365-endpoint-categories) category network traffic.</span></span>
- <span data-ttu-id="75054-126">Chaque connexion Internet locale doit utiliser un serveur DNS régional local pour le trafic Internet sortant de cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="75054-126">Each local Internet connection should be using a regionally local DNS server for outbound Internet traffic from that location.</span></span>

<span data-ttu-id="75054-127">Pour plus d’informations, reportez-vous à [Sortir les connexions réseau localement](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles#egress-network-connections-locally).</span><span class="sxs-lookup"><span data-stu-id="75054-127">For more information, see [Egress network connections locally](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles#egress-network-connections-locally).</span></span> 

<span data-ttu-id="75054-128">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](networking-exit-criteria.md#crit-networking-step2) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="75054-128">As an interim checkpoint, you can see the [exit criteria](networking-exit-criteria.md#crit-networking-step2) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="75054-129">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="75054-129">Next step</span></span>

|||
|:-------|:-----|
|![Étape 3](../media/stepnumbers/Step3.png)|[<span data-ttu-id="75054-131">Éviter les épingles de réseau</span><span class="sxs-lookup"><span data-stu-id="75054-131">Avoid network hairpins</span></span>](networking-avoid-network-hairpins.md)|
