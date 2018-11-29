---
title: 'Phase 1 : Critères de sortie de l’infrastructure réseau'
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
description: Assurez-vous que votre configuration répond aux critères de Microsoft 365 Entreprise pour l’infrastructure réseau.
ms.openlocfilehash: 8161fa2b92ffb4c7c4713e9356c0bc1bfec39d07
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26866828"
---
# <a name="phase-1-networking-infrastructure-exit-criteria"></a><span data-ttu-id="1a0ad-103">Phase 1 : Critères de sortie de l’infrastructure réseau</span><span class="sxs-lookup"><span data-stu-id="1a0ad-103">Phase 1: Networking infrastructure exit criteria</span></span>

![](./media/deploy-foundation-infrastructure/networking_icon-small.png)

<span data-ttu-id="1a0ad-104">Si votre infrastructure réseau respecte les conditions suivantes, vous pouvez passer à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="1a0ad-104">If your networking infrastructure meets the following conditions, you’re ready to move to Phase 2.</span></span>

<a name="crit-networking-step1"></a>
## <a name="required-your-network-is-ready-for-microsoft-365-enterprise"></a><span data-ttu-id="1a0ad-105">Obligatoire : votre réseau est prêt pour Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="1a0ad-105">Required: Your network is ready for Microsoft 365 Enterprise</span></span>

- <span data-ttu-id="1a0ad-106">Vos bureaux ont une bande passante Internet adéquate pour le trafic Microsoft 365, y compris les mises à jour et l’installation d’Office 365, Microsoft Intune, Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="1a0ad-106">Your offices have adequate Internet bandwidth for Microsoft 365 traffic, including Office 365, Microsoft Intune, Windows 10 Enterprise installation and updates</span></span>
- <span data-ttu-id="1a0ad-107">Bureaux centraux pour tout le trafic Internet général</span><span class="sxs-lookup"><span data-stu-id="1a0ad-107">Central offices for all general Internet traffic</span></span>
- <span data-ttu-id="1a0ad-108">Succursales pour le trafic de point de terminaison de catégorie Optimiser</span><span class="sxs-lookup"><span data-stu-id="1a0ad-108">Branch offices for Optimize category endpoint traffic</span></span>
- <span data-ttu-id="1a0ad-109">Votre réseau général est aligné avec une architecture de référence Office 365</span><span class="sxs-lookup"><span data-stu-id="1a0ad-109">Your overall network maps to an Office 365 reference architecture</span></span>

<span data-ttu-id="1a0ad-110">Si nécessaire, l’[Étape 1](networking-provide-bandwidth-cloud-services.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="1a0ad-110">If needed, [Step 1](networking-provide-bandwidth-cloud-services.md) can help you with this requirement.</span></span>

<a name="crit-networking-step2"></a>
## <a name="required-your-local-offices-have-local-internet-connections-and-name-resolution"></a><span data-ttu-id="1a0ad-111">Obligatoire : vos bureaux locaux ont une résolution de noms et des connexions Internet locales</span><span class="sxs-lookup"><span data-stu-id="1a0ad-111">Required: Your local offices have local Internet connections and name resolution</span></span>

<span data-ttu-id="1a0ad-p101">Vous avez configuré chaque bureau local avec un accès Internet via un fournisseur de services Internet local dont des serveurs DNS utilisent une adresse IP publique locale qui identifie leur emplacement sur Internet. Ainsi, les meilleures performances possibles pour les utilisateurs qui accèdent à Office 365 et Intune sont garanties.</span><span class="sxs-lookup"><span data-stu-id="1a0ad-p101">You configured each local office with Internet access with a local ISP whose DNS servers use a local public IP address that identifies their location on the Internet. This ensures the best possible performance for users who access Office 365 and Intune.</span></span>

<span data-ttu-id="1a0ad-114">Si vous n’utilisez pas de fournisseur de services Internet local pour chaque filiale, les performances peuvent en pâtir car le trafic réseau doit parcourir la structure fondamentale d’une organisation ou des requêtes de données sont prises en charge par des serveurs frontaux à distance.</span><span class="sxs-lookup"><span data-stu-id="1a0ad-114">If you don’t use a local ISP for each branch office, performance can suffer because network traffic must traverse an organization’s backbone or data requests are serviced by remote front-end servers.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="1a0ad-115">Comment effectuer les tests</span><span class="sxs-lookup"><span data-stu-id="1a0ad-115">How to test</span></span>
<span data-ttu-id="1a0ad-p102">Utilisez un outil ou site web sur un appareil dans ce bureau pour déterminer l’adresse IP publique utilisée par le serveur proxy. Par exemple, utilisez la page web [What Is My IP Address](https://www.whatismypublicip.com/). Cette adresse IP publique attribuée par votre fournisseur de services Internet doit être géographiquement locale. Elle ne doit pas être issue d’une plage d’adresses IP publiques pour un bureau local ou d’un fournisseur de sécurité réseau basé sur le cloud.</span><span class="sxs-lookup"><span data-stu-id="1a0ad-p102">Use a tool or web site from a device in that office to determine the public IP address that the proxy server is using. For example, use the [What Is My IP Address](https://www.whatismypublicip.com/) web page. This public IP address assigned by your ISP should be geographically local. It should not be from a public IP address range for a central office or from a cloud-based network security vendor.</span></span>

<span data-ttu-id="1a0ad-120">Si nécessaire, l’[Étape 2](networking-dns-resolution-same-location.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="1a0ad-120">If needed, [Step 2](networking-dns-resolution-same-location.md) can help you with this requirement.</span></span>

<a name="crit-networking-step3"></a>
## <a name="optional-unneeded-network-hairpins-are-removed"></a><span data-ttu-id="1a0ad-121">Facultatif : les épingles de réseau inutiles sont supprimées</span><span class="sxs-lookup"><span data-stu-id="1a0ad-121">Optional: Unneeded network hairpins are removed</span></span>

<span data-ttu-id="1a0ad-p103">Vous avez examiné vos épingles de réseau et avez identifié leur impact sur les performances pour tous vos bureaux. Vous avez supprimé les épingles de réseau lorsque cela était possible ou avez travaillé avec votre fournisseur de réseau ou de sécurité tiers pour implémenter une homologation Microsoft 365 optimale pour leur réseau.</span><span class="sxs-lookup"><span data-stu-id="1a0ad-p103">You examined your network hairpins and determined their impact on performance for all of your offices. You removed network hairpins where possible or worked with your third-party network or security provider to implement optimal Microsoft 365 peering for their network.</span></span>

<span data-ttu-id="1a0ad-124">Si nécessaire, l’[Étape 3](networking-avoid-network-hairpins.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="1a0ad-124">If needed, [Step 3](networking-avoid-network-hairpins.md) can help you with this option.</span></span>


<a name="crit-networking-step4"></a>
## <a name="optional-you-have-configured-traffic-bypass-on-your-internet-browsers-and-edge-devices"></a><span data-ttu-id="1a0ad-125">Facultatif : vous avez configuré le trafic de contournement sur vos navigateurs Internet et équipements de périmètre</span><span class="sxs-lookup"><span data-stu-id="1a0ad-125">Optional: You have configured traffic bypass on your Internet browsers and edge devices</span></span>

<span data-ttu-id="1a0ad-126">Vous avez déployé les derniers fichiers PAC sur vos navigateurs Internet locaux afin que le trafic vers des noms de domaine DNS Microsoft 365 contournent les serveurs proxy.</span><span class="sxs-lookup"><span data-stu-id="1a0ad-126">You deployed the latest PAC files to your on-premises Internet browsers so that traffic to Microsoft 365 DNS domain names bypass proxy servers.</span></span>

<span data-ttu-id="1a0ad-127">Vous avez configuré vos équipements de périmètre réseau (les pare-feu, SSL Break and Inspect et autres appareils d’inspection de paquets) de façon à ce qu’ils utilisent le trafic de contournement ou qu’ils traitent le trafic au minimum pour les catégories Optimiser et Autoriser des points de terminaison Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1a0ad-127">You configured your network perimeter devices—such as firewalls, and SSL Break and Inspect, and packet inspection devices— to use traffic bypass or to minimally process traffic to the Optimize and Allow categories of Microsoft 365 endpoints.</span></span>


### <a name="how-to-test"></a><span data-ttu-id="1a0ad-128">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="1a0ad-128">How to test</span></span>

<span data-ttu-id="1a0ad-129">Utilisez les outils de journalisation sur vos appareils de périmètre réseau pour vous assurer que le trafic vers les destinations Microsoft 365 n’est pas en cours d’inspection, de déchiffrement ou altéré d’une autre façon.</span><span class="sxs-lookup"><span data-stu-id="1a0ad-129">Use the logging tools on your network perimeter devices to ensure that traffic to Microsoft 365 destinations isn’t being inspected, decrypted, or otherwise hindered.</span></span>

<span data-ttu-id="1a0ad-130">Si nécessaire, l’[Étape 4](networking-configure-proxies-firewalls.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="1a0ad-130">If needed, [Step 4](networking-configure-proxies-firewalls.md) can help you with this option.</span></span>


<a name="crit-networking-step5"></a>
## <a name="optional-your-clients-and-office-365-applications-are-configured-for-optimal-performance"></a><span data-ttu-id="1a0ad-131">Facultatif : vos applications Office 365 et clients sont configurés pour des performances optimales</span><span class="sxs-lookup"><span data-stu-id="1a0ad-131">Optional: Your clients and Office 365 applications are configured for optimal performance</span></span>

<span data-ttu-id="1a0ad-132">Vous avez optimisé les paramètres TCP sur vos appareils client et pour les services Exchange Online, Skype Entreprise Online, SharePoint Online et Project Online.</span><span class="sxs-lookup"><span data-stu-id="1a0ad-132">You have optimized the Transmssion Control Protocol (TCP) settings on your client devices and for Exchange Online, Skype for Business Online, SharePoint Online, and Project Online services.</span></span>

<span data-ttu-id="1a0ad-133">Si nécessaire, l’[Étape 5](networking-optimize-tcp-performance.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="1a0ad-133">If needed, [Step 5](networking-optimize-tcp-performance.md) can help you with this option.</span></span>

## <a name="next-phase"></a><span data-ttu-id="1a0ad-134">Phase suivante</span><span class="sxs-lookup"><span data-stu-id="1a0ad-134">Next phase</span></span>

|||
|:-------|:-----|
|![](./media/deploy-foundation-infrastructure/identity_icon-small.png)| <span data-ttu-id="1a0ad-135">Votre phase suivante dans le processus de déploiement de bout en bout pour Microsoft 365 Entreprise est [identité](identity-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="1a0ad-135">Your next phase in the end-to-end deployment process for Microsoft 365 Enterprise is [identity](identity-infrastructure.md).</span></span> |
