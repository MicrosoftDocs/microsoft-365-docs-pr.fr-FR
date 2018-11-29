---
title: 'Étape 2 : Configurer les connexions Internet locales pour chaque bureau'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 10/31/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et configurez votre résolution DNS pour de meilleures performances.
ms.openlocfilehash: 9ccd5c477b4aeda8e7dcf482cc09c8a357f19f40
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26866856"
---
# <a name="step-2-configure-local-internet-connections-for-each-office"></a><span data-ttu-id="c435a-103">Étape 2 : Configurer les connexions Internet locales pour chaque bureau</span><span class="sxs-lookup"><span data-stu-id="c435a-103">Step 2: Configure local Internet connections for each office</span></span>

<span data-ttu-id="c435a-104">*Cette étape est requise et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="c435a-104">*This step is required and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/networking_icon-small.png)

<span data-ttu-id="c435a-p101">À l’Étape 2, vous vérifiez que chacun de vos bureaux est équipé de connexions Internet locales et utilise des serveurs DNS locaux. Ces deux éléments sont requis pour réduire la latence de connexion et garantir que les ordinateurs clients locaux établissent des connexions avec le point d’entrée le plus proche aux services services cloud Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c435a-p101">In Step 2, you ensure that each of your offices have local Internet connections and use local DNS servers. Both of these elements are required to reduce connection latency and ensure that on-premises client computers make connections to the nearest point of entry to Microsoft 365 cloud-based services.</span></span>

<span data-ttu-id="c435a-p102">Dans les réseaux traditionnels des grandes entreprises, le trafic Internet traverse la structure fondamentale du réseau jusqu’à atteindre une connexion Internet centrale. Cela ne fonctionne pas correctement pour optimiser les performances sur une infrastructure SaaS distribuée globalement, qui inclut les produits Office 365 et Enterprise Mobility + Security (EMS) dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c435a-p102">In traditional networks for large organizations, Internet traffic travels across the network backbone to a central Internet connection. This does not work well for optimizing performance to a globally distributed Software-as-a-Service (SaaS) infrastructure, which includes the Office 365 and Enterprise Mobility + Security (EMS) products in Microsoft 365.</span></span>

<span data-ttu-id="c435a-p103">Le réseau global Microsoft inclut des serveurs frontaux sur l’ensemble des services cloud de Microsoft 365 dans le monde entier. Pour de meilleures performances, les clients locaux doivent accéder au serveur frontal le plus proche géographiquement, plutôt que d’envoyer le trafic sur une structure fondamentale du réseau et sur le serveur frontal qui est le plus proche de la connexion Internet centrale de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="c435a-p103">The Microsoft Global Network includes front end servers to the set of cloud services for Microsoft 365 all over the world. For the best performance, on-premises clients should access a front-end server that is geographically closest to them, rather than sending the traffic over a network backbone and to the front-end server that is closest to the organization’s central Internet connection.</span></span>

<span data-ttu-id="c435a-p104">Pour diriger la demande d’un client vers le serveur frontal le plus proche géographiquement, les serveurs DNS de Microsoft utilisent des requêtes DNS correspondant à la demande de connexion initiale du client. Par conséquent, pour la latence de réseau la plus faible :</span><span class="sxs-lookup"><span data-stu-id="c435a-p104">To direct a client request to the geographically nearest front-end server, Microsoft’s DNS servers use the DNS queries corresponding the client’s initial connection request. Therefore, for the lowest network latency:</span></span>

- <span data-ttu-id="c435a-113">Tous les bureaux de votre organisation doivent avoir des connexions Internet locales pour le trafic réseau de catégorie [Optimiser](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles#new-office-365-endpoint-categories).</span><span class="sxs-lookup"><span data-stu-id="c435a-113">All offices of your organization should have local Internet connections for [Optimize](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles#new-office-365-endpoint-categories) category network traffic.</span></span>
- <span data-ttu-id="c435a-114">Chaque connexion Internet locale doit utiliser un serveur DNS régional local pour le trafic Internet sortant de cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="c435a-114">Each local Internet connection should be using a regionally local DNS server for outbound Internet traffic from that location.</span></span>

<span data-ttu-id="c435a-115">Pour plus d’informations, reportez-vous à [Sortir les connexions réseau localement](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles#egress-network-connections-locally).</span><span class="sxs-lookup"><span data-stu-id="c435a-115">For more information, see [Egress network connections locally](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles#egress-network-connections-locally).</span></span> 

<span data-ttu-id="c435a-116">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](networking-exit-criteria.md#crit-networking-step2) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="c435a-116">As an interim checkpoint, you can see the [exit criteria](networking-exit-criteria.md#crit-networking-step2) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="c435a-117">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="c435a-117">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step3.png)|[<span data-ttu-id="c435a-118">Éviter les épingles de réseau</span><span class="sxs-lookup"><span data-stu-id="c435a-118">Avoid network hairpins</span></span>](networking-avoid-network-hairpins.md)|
