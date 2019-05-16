---
title: 'Étape 3 : Éviter les épingles de réseau'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 10/31/2018
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Découvrez le fonctionnement des épingles de réseau et supprimez-les pour obtenir de meilleures performances.
ms.openlocfilehash: eb233c02d1d4c0198c11d520acca1d680df78a82
ms.sourcegitcommit: 66bb5af851947078872a4d31d3246e69f7dd42bb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34073284"
---
# <a name="step-3-avoid-network-hairpins"></a><span data-ttu-id="36a39-103">Étape 3 : Éviter les épingles de réseau</span><span class="sxs-lookup"><span data-stu-id="36a39-103">Step 3: Avoid network hairpins</span></span>

<span data-ttu-id="36a39-104">*Cette étape est requise et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="36a39-104">*This step is required and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/networking_icon-small.png)

<span data-ttu-id="36a39-p101">Une [épingle de réseau](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles#BKMK_P3) se produit lorsque le trafic vers une destination est d’abord dirigé vers un autre emplacement intermédiaire, comme une pile de sécurité locale, un courtier d’accès au cloud ou une passerelle web basée sur le cloud. Une épingle de réseau peut également se produire à cause d’un routage médiocre sur Internet dû à des fournisseurs de services réseau. Une épingle ajoute une latence et peut potentiellement rediriger le trafic vers un emplacement distant géographiquement.</span><span class="sxs-lookup"><span data-stu-id="36a39-p101">A [network hairpin](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles#BKMK_P3) happens when traffic bound for a destination is first directed to another intermediate location, such as an on-premises security stack, cloud access broker, or cloud-based web gateway. A network hairpin could also be caused by poor routing on the Internet due to network service providers. A hairpin adds latency and can potentially redirect traffic to a geographically distant location.</span></span>

<span data-ttu-id="36a39-p102">Pour optimiser les performances pour le trafic vers les services basés sur le cloud de Microsoft 365, vérifiez si l’ISP qui fournit la connexion Internet locale a une relation d’homologation directe avec le réseau global de Microsoft à proximité immédiate de cet emplacement. Ces connexions n’ont pas d’épingles.</span><span class="sxs-lookup"><span data-stu-id="36a39-p102">To optimize performance for traffic to Microsoft 365 cloud-based services, check whether the ISP providing the local Internet connection has a direct peering relationship with the Microsoft Global Network in close proximity to that location. These connections do not have hairpins.</span></span>

<span data-ttu-id="36a39-p103">Si vous utilisez les services de sécurité ou de réseau basés sur le cloud pour votre trafic Microsoft 365, assurez-vous que l’effet des épingles est évalué et que leur impact sur les performances est compris. Examinez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="36a39-p103">If you use cloud-based network or security services for your Microsoft 365 traffic, ensure that the hairpinning effect is evaluated and its impact on performance is understood. Examine the following:</span></span>

- <span data-ttu-id="36a39-112">le nombre et les emplacements des fournisseurs de services par lesquels le trafic est transféré par rapport à vos succursales et points d’homologation du réseau global de Microsoft ;</span><span class="sxs-lookup"><span data-stu-id="36a39-112">The number and locations of your service providers through which the traffic is forwarded in relationship to your branch offices and Microsoft Global Network peering points</span></span> 
- <span data-ttu-id="36a39-113">la qualité de la relation d’homologation du réseau du fournisseur de services avec votre ISP et Microsoft ;</span><span class="sxs-lookup"><span data-stu-id="36a39-113">The quality of the network peering relationship of the service provider with your ISP and Microsoft</span></span> 
- <span data-ttu-id="36a39-114">l’impact sur les performances de la transmission dans l’infrastructure du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="36a39-114">The performance impact of backhauling in the service provider infrastructure</span></span>

<span data-ttu-id="36a39-115">Dès que possible, configurez vos routeurs périphériques pour envoyer le trafic Microsoft 365 approuvé directement, au lieu d’utiliser la transmission par proxy ou le tunneling via un cloud tiers ou un fournisseur de sécurité réseau basé sur le cloud qui traite votre trafic Internet.</span><span class="sxs-lookup"><span data-stu-id="36a39-115">Whenever possible, configure your edge routers to send trusted Microsoft 365 traffic directly, instead of proxying or tunneling through a third-party cloud or cloud-based network security vendor that processes your Internet traffic.</span></span> 

<span data-ttu-id="36a39-116">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](networking-exit-criteria.md#crit-networking-step3) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="36a39-116">As an interim checkpoint, you can see the [exit criteria](networking-exit-criteria.md#crit-networking-step3) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="36a39-117">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="36a39-117">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step4.png)|[<span data-ttu-id="36a39-118">Configurer le trafic de contournement</span><span class="sxs-lookup"><span data-stu-id="36a39-118">Configure traffic bypass</span></span>](networking-configure-proxies-firewalls.md)|
