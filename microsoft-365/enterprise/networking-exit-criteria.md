---
title: 'Phase 1 : Critères de sortie de l’infrastructure réseau'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/05/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Assurez-vous que votre configuration répond aux critères de Microsoft 365 Entreprise pour l’infrastructure réseau.
ms.openlocfilehash: 9ea601d66ef2df0d7a4efde188a70c51e3fb9f60
ms.sourcegitcommit: 3b2d3e2b38c4860db977e73dda119a465c669fa4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33400218"
---
# <a name="phase-1-networking-infrastructure-exit-criteria"></a><span data-ttu-id="241c4-103">Phase 1 : Critères de sortie de l’infrastructure réseau</span><span class="sxs-lookup"><span data-stu-id="241c4-103">Phase 1: Networking infrastructure exit criteria</span></span>

![](./media/deploy-foundation-infrastructure/networking_icon-small.png)

<span data-ttu-id="241c4-104">Vérifiez que votre infrastructure réseau répond aux critères requis suivants et que vous avez pris en considération les critères facultatifs.</span><span class="sxs-lookup"><span data-stu-id="241c4-104">Make sure your networking infrastructure meets the following required criteria and that you've considered those that are optional.</span></span>

<a name="crit-networking-step1"></a>
## <a name="required-your-network-is-ready-for-microsoft-365-enterprise"></a><span data-ttu-id="241c4-105">Obligatoire : votre réseau est prêt pour Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="241c4-105">Required: Your network is ready for Microsoft 365 Enterprise</span></span>

- <span data-ttu-id="241c4-106">Vos bureaux disposent d’une bande passante Internet adéquate pour le trafic Microsoft 365, y compris pour l’installation et les mises à jour d’Office 365, de Microsoft Intune et de Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="241c4-106">Your offices have adequate Internet bandwidth for Microsoft 365 traffic, including Office 365, Microsoft Intune, and Windows 10 Enterprise installation and updates</span></span>
- <span data-ttu-id="241c4-107">Votre réseau global est conforme à l’architecture de référence Office 365</span><span class="sxs-lookup"><span data-stu-id="241c4-107">Your overall network maps to an Office 365 reference architecture</span></span>
- <span data-ttu-id="241c4-108">Les modifications de votre réseau ont été testées et répondent aux exigences en matière de latence du trafic</span><span class="sxs-lookup"><span data-stu-id="241c4-108">Your network changes have been piloted and tested and meet with your traffic latency requirements</span></span> 

<span data-ttu-id="241c4-109">Si nécessaire, l’[Étape 1](networking-provide-bandwidth-cloud-services.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="241c4-109">If needed, [Step 1](networking-provide-bandwidth-cloud-services.md) can help you with this requirement.</span></span>

<a name="crit-networking-step2"></a>
## <a name="required-your-local-offices-have-local-internet-connections-and-name-resolution"></a><span data-ttu-id="241c4-110">Obligatoire : vos bureaux locaux ont une résolution de noms et des connexions Internet locales</span><span class="sxs-lookup"><span data-stu-id="241c4-110">Required: Your local offices have local Internet connections and name resolution</span></span>

<span data-ttu-id="241c4-p101">Vous avez configuré chaque bureau local avec un accès Internet via un fournisseur de services Internet local dont des serveurs DNS utilisent une adresse IP publique locale qui identifie leur emplacement sur Internet. Ainsi, les meilleures performances possibles pour les utilisateurs qui accèdent à Office 365 et Intune sont garanties.</span><span class="sxs-lookup"><span data-stu-id="241c4-p101">You configured each local office with Internet access with a local ISP whose DNS servers use a local public IP address that identifies their location on the Internet. This ensures the best possible performance for users who access Office 365 and Intune.</span></span>

<span data-ttu-id="241c4-113">Si vous n’utilisez pas de fournisseur de services Internet local pour chaque filiale, les performances peuvent en pâtir car le trafic réseau doit parcourir la structure fondamentale d’une organisation ou des requêtes de données sont prises en charge par des serveurs frontaux à distance.</span><span class="sxs-lookup"><span data-stu-id="241c4-113">If you don’t use a local ISP for each branch office, performance can suffer because network traffic must traverse an organization’s backbone or data requests are serviced by remote front-end servers.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="241c4-114">Comment effectuer les tests</span><span class="sxs-lookup"><span data-stu-id="241c4-114">How to test</span></span>
<span data-ttu-id="241c4-p102">Utilisez un outil ou site web sur un appareil dans ce bureau pour déterminer l’adresse IP publique utilisée par le serveur proxy. Par exemple, utilisez la page web [What Is My IP Address](https://www.whatismypublicip.com/). Cette adresse IP publique attribuée par votre fournisseur de services Internet doit être géographiquement locale. Elle ne doit pas être issue d’une plage d’adresses IP publiques pour un bureau local ou d’un fournisseur de sécurité réseau basé sur le cloud.</span><span class="sxs-lookup"><span data-stu-id="241c4-p102">Use a tool or web site from a device in that office to determine the public IP address that the proxy server is using. For example, use the [What Is My IP Address](https://www.whatismypublicip.com/) web page. This public IP address assigned by your ISP should be geographically local. It should not be from a public IP address range for a central office or from a cloud-based network security vendor.</span></span>

<span data-ttu-id="241c4-119">Si nécessaire, l’[Étape 2](networking-dns-resolution-same-location.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="241c4-119">If needed, [Step 2](networking-dns-resolution-same-location.md) can help you with this requirement.</span></span>

<a name="crit-networking-step3"></a>
## <a name="optional-unneeded-network-hairpins-are-removed"></a><span data-ttu-id="241c4-120">Facultatif : les épingles de réseau inutiles sont supprimées</span><span class="sxs-lookup"><span data-stu-id="241c4-120">Optional: Unneeded network hairpins are removed</span></span>

<span data-ttu-id="241c4-p103">Vous avez examiné vos épingles de réseau et avez identifié leur impact sur les performances pour tous vos bureaux. Vous avez supprimé les épingles de réseau lorsque cela était possible ou avez travaillé avec votre fournisseur de réseau ou de sécurité tiers pour implémenter une homologation Microsoft 365 optimale pour leur réseau.</span><span class="sxs-lookup"><span data-stu-id="241c4-p103">You examined your network hairpins and determined their impact on performance for all of your offices. You removed network hairpins where possible or worked with your third-party network or security provider to implement optimal Microsoft 365 peering for their network.</span></span>

<span data-ttu-id="241c4-123">Si nécessaire, l’[Étape 3](networking-avoid-network-hairpins.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="241c4-123">If needed, [Step 3](networking-avoid-network-hairpins.md) can help you with this option.</span></span>


<a name="crit-networking-step4"></a>
## <a name="optional-you-have-configured-traffic-bypass-on-your-internet-browsers-and-edge-devices"></a><span data-ttu-id="241c4-124">Facultatif : vous avez configuré le trafic de contournement sur vos navigateurs Internet et équipements de périmètre</span><span class="sxs-lookup"><span data-stu-id="241c4-124">Optional: You have configured traffic bypass on your Internet browsers and edge devices</span></span>

<span data-ttu-id="241c4-125">Vous avez déployé les derniers fichiers PAC sur vos navigateurs Internet locaux afin que le trafic vers des noms de domaine DNS Microsoft 365 contournent les serveurs proxy.</span><span class="sxs-lookup"><span data-stu-id="241c4-125">You deployed the latest PAC files to your on-premises Internet browsers so that traffic to Microsoft 365 DNS domain names bypass proxy servers.</span></span>

<span data-ttu-id="241c4-126">Vous avez configuré vos équipements de périmètre réseau (les pare-feu, SSL Break and Inspect et autres appareils d’inspection de paquets) de façon à ce qu’ils utilisent le trafic de contournement ou qu’ils traitent le trafic au minimum pour les catégories Optimiser et Autoriser des points de terminaison Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="241c4-126">You configured your network perimeter devices—such as firewalls, and SSL Break and Inspect, and packet inspection devices— to use traffic bypass or to minimally process traffic to the Optimize and Allow categories of Microsoft 365 endpoints.</span></span>


### <a name="how-to-test"></a><span data-ttu-id="241c4-127">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="241c4-127">How to test</span></span>

<span data-ttu-id="241c4-128">Utilisez les outils de journalisation sur vos appareils de périmètre réseau pour vous assurer que le trafic vers les destinations Microsoft 365 n’est pas en cours d’inspection, de déchiffrement ou altéré d’une autre façon.</span><span class="sxs-lookup"><span data-stu-id="241c4-128">Use the logging tools on your network perimeter devices to ensure that traffic to Microsoft 365 destinations isn’t being inspected, decrypted, or otherwise hindered.</span></span>

<span data-ttu-id="241c4-129">Si nécessaire, l’[Étape 4](networking-configure-proxies-firewalls.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="241c4-129">If needed, [Step 4](networking-configure-proxies-firewalls.md) can help you with this option.</span></span>


<a name="crit-networking-step5"></a>
## <a name="optional-your-clients-and-office-365-applications-are-configured-for-optimal-performance"></a><span data-ttu-id="241c4-130">Facultatif : vos applications Office 365 et clients sont configurés pour des performances optimales</span><span class="sxs-lookup"><span data-stu-id="241c4-130">Optional: Your clients and Office 365 applications are configured for optimal performance</span></span>

<span data-ttu-id="241c4-131">Vous avez optimisé les paramètres TCP sur vos appareils client et pour les services Exchange Online, Skype Entreprise Online, SharePoint Online et Project Online.</span><span class="sxs-lookup"><span data-stu-id="241c4-131">You have optimized the Transmssion Control Protocol (TCP) settings on your client devices and for Exchange Online, Skype for Business Online, SharePoint Online, and Project Online services.</span></span>

<span data-ttu-id="241c4-132">Si nécessaire, l’[Étape 5](networking-optimize-tcp-performance.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="241c4-132">If needed, [Step 5](networking-optimize-tcp-performance.md) can help you with this option.</span></span>

## <a name="results-and-next-steps"></a><span data-ttu-id="241c4-133">Résultats et étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="241c4-133">Results and next steps</span></span>

<span data-ttu-id="241c4-134">Les utilisateurs de votre intranet sont désormais prêts à utiliser les services de cloud computing de Microsoft 365 via un chemin de mise en réseau efficace vers et sur Internet.</span><span class="sxs-lookup"><span data-stu-id="241c4-134">Your intranet users are now ready to consume Microsoft 365 cloud services over an efficient networking path to and across the Internet.</span></span>

|||
|:-------|:-----|
|![](./media/deploy-foundation-infrastructure/identity_icon-small.png)| <span data-ttu-id="241c4-135">Si vous suivez les phases de déploiement de bout en bout de Microsoft 365 Entreprise, la prochaine phase est l’[identité](identity-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="241c4-135">If you're following the phases for the end-to-end deployment of Microsoft 365 Enterprise, your next phase is [identity](identity-infrastructure.md).</span></span> |
