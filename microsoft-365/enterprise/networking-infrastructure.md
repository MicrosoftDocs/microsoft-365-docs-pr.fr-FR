---
title: 'Phase 1 : Infrastructure réseau pour Microsoft 365 Entreprise'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 10/31/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Les étapes de déploiement de l’infrastructure réseau pour Microsoft 365 Entreprise.
ms.openlocfilehash: 9b8c23d543eca97147801d70e42de7105266c52d
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291181"
---
# <a name="phase-1-networking-infrastructure-for-microsoft-365-enterprise"></a><span data-ttu-id="45565-103">Phase 1 : Infrastructure réseau pour Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="45565-103">Phase 1: Networking infrastructure for Microsoft 365 Enterprise</span></span>

![](./media/deploy-foundation-infrastructure/networking_icon.png)

<span data-ttu-id="45565-104">Microsoft 365 Entreprise inclut Office 365 et Microsoft Intune dans le cadre de la gestion d’entreprise + Security (EMS).</span><span class="sxs-lookup"><span data-stu-id="45565-104">Microsoft 365 Enterprise includes Office 365 and Microsoft Intune as part of Enterprise Management + Security (EMS).</span></span> <span data-ttu-id="45565-105">Ces deux services cloud s’appuient sur la sécurité, les performances et la fiabilité des connexions à partir d’appareils clients via Internet ou des circuits dédiés.</span><span class="sxs-lookup"><span data-stu-id="45565-105">Both of these cloud-based services rely on the security, performance, and reliability of connections from client devices over the Internet or dedicated circuits.</span></span> <span data-ttu-id="45565-106">Pour héberger ces services et les rendre accessibles aux clients dans le monde entier, Microsoft a conçu une infrastructure réseau qui met en évidence les performances et l’intégration.</span><span class="sxs-lookup"><span data-stu-id="45565-106">To host these services and make them available to customers all over the world, Microsoft has designed a networking infrastructure that emphasizes performance and integration.</span></span> 

<span data-ttu-id="45565-p102">Dans cette phase, vous découvrez les considérations clés pour la création d’une connexion performante aux services cloud de Microsoft 365 Entreprise. Pour une vue d’ensemble, consultez la rubrique relative aux [principes de la mise en réseau d’Office 365](https://techcommunity.microsoft.com/t5/Office-365-Blog/Getting-the-best-connectivity-and-performance-in-Office-365/ba-p/124694).</span><span class="sxs-lookup"><span data-stu-id="45565-p102">In this phase, you step through the key considerations for creating a performant connection to the cloud services of Microsoft 365 Enterprise. For an overview, see [Office 365 networking principles](https://techcommunity.microsoft.com/t5/Office-365-Blog/Getting-the-best-connectivity-and-performance-in-Office-365/ba-p/124694).</span></span>

>[!Note]
><span data-ttu-id="45565-109">Si vous avez déjà déployé une infrastructure réseau, consultez les [critères de sortie](networking-exit-criteria.md) de cette phase pour vous assurer que vous répondez aux conditions requises et facultatives pour Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="45565-109">If you already have a networking infrastructure deployed, please see the [exit criteria](networking-exit-criteria.md) for this phase to make sure that it meets the required and optional conditions for Microsoft 365 Enterprise.</span></span>

## <a name="plan-and-deploy-your-microsoft-365-enterprise-networking-infrastructure"></a><span data-ttu-id="45565-110">Planifier et déployer votre infrastructure réseau de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="45565-110">Plan and deploy your Microsoft 365 Enterprise networking infrastructure</span></span> 

<span data-ttu-id="45565-111">Procédez comme suit pour déployer votre infrastructure réseau pour la configuration requise et les fonctionnalités de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="45565-111">Use the following steps to build out your networking infrastructure for the requirements and capabilities of Microsoft 365 Enterprise.</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step1.png)|[<span data-ttu-id="45565-112">Préparer le réseau de votre organisation pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="45565-112">Prepare your network for Microsoft 365</span></span>](networking-provide-bandwidth-cloud-services.md)|
|![](./media/stepnumbers/Step2.png)|[<span data-ttu-id="45565-113">Configurer les connexions Internet locales pour chaque bureau</span><span class="sxs-lookup"><span data-stu-id="45565-113">Configure local Internet connections for each office</span></span>](networking-dns-resolution-same-location.md)|
|![](./media/stepnumbers/Step3.png)|[<span data-ttu-id="45565-114">Éviter les épingles de réseau</span><span class="sxs-lookup"><span data-stu-id="45565-114">Avoid network hairpins</span></span>](networking-avoid-network-hairpins.md)|
|![](./media/stepnumbers/Step4.png)|[<span data-ttu-id="45565-115">Configurer le trafic de contournement</span><span class="sxs-lookup"><span data-stu-id="45565-115">Configure traffic bypass</span></span>](networking-configure-proxies-firewalls.md)|
|![](./media/stepnumbers/Step5.png)|[<span data-ttu-id="45565-116">Optimisez les performances du service Office 365 et du client</span><span class="sxs-lookup"><span data-stu-id="45565-116">Optimize client and Office 365 service performance</span></span>](networking-optimize-tcp-performance.md)|


<span data-ttu-id="45565-117">Lorsque vous avez terminé ces étapes, accédez aux [critères de sortie](networking-exit-criteria.md) de cette phase pour vous assurer que vous répondez aux conditions requises et facultatives pour Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="45565-117">When you've completed these steps, go to the [exit criteria](networking-exit-criteria.md) for this phase to ensure that you meet the required and optional conditions for Microsoft 365 Enterprise.</span></span>

## <a name="how-microsoft-does-microsoft-365-enterprise"></a><span data-ttu-id="45565-118">Comment Microsoft gère-t-il Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="45565-118">How Microsoft does Microsoft 365 Enterprise</span></span>

<span data-ttu-id="45565-119">Jetez un œil aux coulisses de Microsoft et découvrez comment l’entreprise a mis en place et a amélioré le réseau Microsoft pour les services cloud Office 365 en lisant l’article relatif à l’[optimisation des performances réseau pour Microsoft Office 365](https://www.microsoft.com/itshowcase/Article/Content/631/Optimizing-network-performance-for-Microsoft-Office-365).</span><span class="sxs-lookup"><span data-stu-id="45565-119">Peek inside Microsoft and learn how the company prepared for and optimized the Microsoft network for the Office 365 cloud services with [Optimizing network performance for Microsoft Office 365](https://www.microsoft.com/itshowcase/Article/Content/631/Optimizing-network-performance-for-Microsoft-Office-365).</span></span>

## <a name="how-contoso-did-microsoft-365-enterprise"></a><span data-ttu-id="45565-120">Comment Contoso est-elle passée à Microsoft 365 Entreprise ?</span><span class="sxs-lookup"><span data-stu-id="45565-120">How Contoso did Microsoft 365 Enterprise</span></span>

<span data-ttu-id="45565-121">Découvrez comment Contoso Corporation, une entreprise multinationale fictive mais représentative, [a optimisé son réseau](contoso-networking.md) pour les services cloud Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="45565-121">See how the Contoso Corporation, a fictional but representative multi-national business, [optimized their network](contoso-networking.md) for Microsoft 365 cloud services.</span></span>

![](./media/contoso-overview/contoso-icon.png)

## <a name="next-step"></a><span data-ttu-id="45565-122">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="45565-122">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step1.png)|[<span data-ttu-id="45565-123">Préparer le réseau de votre organisation pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="45565-123">Prepare your network for Microsoft 365</span></span>](networking-provide-bandwidth-cloud-services.md)|

