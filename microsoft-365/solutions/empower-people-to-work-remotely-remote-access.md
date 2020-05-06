---
title: Étape 2. Fournir l’accès à distance aux applications et services locaux
f1.keywords:
- NOCSH
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 05/01/2020
audience: ITPro
ms.topic: article
ms.prod: microsoft-365-enterprise
localization_priority: Priority
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
- remotework
ms.custom:
- M365solutions
description: Assurez-vous que vos employés à distance peuvent accéder aux ressources locales tout en optimisant l’accès aux services cloud de Microsoft 365.
ms.openlocfilehash: fb91451b52c55f2cad1e0efefe19a044ce1cc37b
ms.sourcegitcommit: 101084f9c81616342d78493232d8f13f5ffa4ddf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2020
ms.locfileid: "44002647"
---
# <a name="step-2-provide-remote-access-to-on-premises-apps-and-services"></a><span data-ttu-id="9cc82-104">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="9cc82-104">Step 2.</span></span> <span data-ttu-id="9cc82-105">Fournir l’accès à distance aux applications et services locaux</span><span class="sxs-lookup"><span data-stu-id="9cc82-105">Provide remote access to on-premises apps and services</span></span>

<span data-ttu-id="9cc82-106">Si votre organisation utilise une solution VPN d’accès à distance, généralement avec les serveurs VPN sur la périphérie de votre réseau et les clients VPN installés sur les appareils de vos utilisateurs, vos utilisateurs peuvent utiliser les connexions VPN d’accès à distance pour accéder aux applications et serveurs locaux.</span><span class="sxs-lookup"><span data-stu-id="9cc82-106">If your organization uses a remote access VPN solution, typically with VPN servers on the edge of your network and VPN clients installed on your users' devices, your users can use remote access VPN connections to access on-premises apps and servers.</span></span> <span data-ttu-id="9cc82-107">Mais vous devrez peut-être optimiser le trafic vers les services cloud de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9cc82-107">But you may need to optimize traffic to Microsoft 365 cloud-based services.</span></span>

<span data-ttu-id="9cc82-108">Si vos utilisateurs n’utilisent pas de solution VPN, vous pouvez utiliser le proxy d’application Azure Active Directory (Azure AD) et le VPN Azure Point-to-Site (P2S) pour fournir un accès, si toutes vos applications sont basées sur le web.</span><span class="sxs-lookup"><span data-stu-id="9cc82-108">If your users do not use a VPN solution, you can use Azure Active Directory (Azure AD) Application Proxy and Azure Point-to-Site (P2S) VPN to provide access, depending on whether all your apps are web-based.</span></span>

<span data-ttu-id="9cc82-109">Il existe trois configurations principales :</span><span class="sxs-lookup"><span data-stu-id="9cc82-109">There are three primary configurations:</span></span>

1. <span data-ttu-id="9cc82-110">Vous utilisez déjà une solution VPN d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="9cc82-110">You are already using a remote access VPN solution.</span></span>
2. <span data-ttu-id="9cc82-111">Vous n’utilisez pas une solution VPN d’accès à distance, vous avez une identité hybride, et vous avez besoin d’un accès à distance uniquement pour les applications web locales.</span><span class="sxs-lookup"><span data-stu-id="9cc82-111">You are not using a remote access VPN solution, you have hybrid identity, and you need remote access only to on-premises web-based apps.</span></span>
3. <span data-ttu-id="9cc82-112">Vous n’utilisez pas de solution VPN d’accès à distance et vous avez besoin d’accéder à des applications locales, dont certaines ne sont pas basées sur le web.</span><span class="sxs-lookup"><span data-stu-id="9cc82-112">You are not using a remote access VPN solution and you need access to on-premises apps, some of which are not web-based.</span></span>

<span data-ttu-id="9cc82-113">Avec les connexions d’accès à distance, vous pouvez également utiliser le [Bureau à distance](https://support.microsoft.com/help/4028379/windows-10-how-to-use-remote-desktop) pour connecter vos utilisateurs à un PC local.</span><span class="sxs-lookup"><span data-stu-id="9cc82-113">With remote access connections, you can also use [Remote Desktop](https://support.microsoft.com/help/4028379/windows-10-how-to-use-remote-desktop) to connect your users to an on-premises PC.</span></span> <span data-ttu-id="9cc82-114">Par exemple, un employé distant peut utiliser le Bureau à distance pour se connecter au PC de son bureau à partir de son appareil Windows, iOS ou Android.</span><span class="sxs-lookup"><span data-stu-id="9cc82-114">For example, a remote worker can use Remote Desktop to connect to the PC in their office from their Windows, iOS or Android device.</span></span> <span data-ttu-id="9cc82-115">Lorsqu’il est connecté à distance, il peut l’utiliser comme s’il était assis face à son PC.</span><span class="sxs-lookup"><span data-stu-id="9cc82-115">Once they are remotely connected, they can use it as if they were sitting in front of it.</span></span>

## <a name="optimize-performance-for-remote-access-vpn-clients-to-microsoft-365-cloud-services"></a><span data-ttu-id="9cc82-116">Optimiser les performances des clients VPN d’accès à distance aux services cloud de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9cc82-116">Optimize performance for remote access VPN clients to Microsoft 365 cloud services</span></span>

<span data-ttu-id="9cc82-117">Si vos employés à distance utilisent un client VPN traditionnel pour obtenir l’accès à distance au réseau de votre organisation, vérifiez que le client VPN a une prise en charge de la segmentation de tunnel.</span><span class="sxs-lookup"><span data-stu-id="9cc82-117">If your remote workers are using a traditional VPN client to obtain remote access to your organization network, verify that the VPN client has split tunneling support.</span></span>

<span data-ttu-id="9cc82-118">Sans cette segmentation, l’ensemble de votre trafic de travail à distance est envoyé sur la connexion VPN, où il doit être transféré vers les appareils Microsoft Edge de votre organisation, être traité, puis envoyé sur Internet.</span><span class="sxs-lookup"><span data-stu-id="9cc82-118">Without split tunneling, all of your remote work traffic gets sent across the VPN connection, where it must be forwarded to your organization’s edge devices, get processed, and then sent on the Internet.</span></span>

![Trafic réseau provenant de clients VPN sans segmentation de tunnel](../media/empower-people-to-work-remotely-remote-access/empower-people-to-work-remotely-remote-access-before-tunneling.png)

<span data-ttu-id="9cc82-120">Le trafic Microsoft 365 doit emprunter une route indirecte au sein de votre organisation, qui peut être transférée vers un point d’entrée réseau Microsoft éloigné loin de l’emplacement physique du client VPN.</span><span class="sxs-lookup"><span data-stu-id="9cc82-120">Microsoft 365 traffic must take an indirect route through your organization, which could be the forwarded to a Microsoft network entry point far away from the VPN client’s physical location.</span></span> <span data-ttu-id="9cc82-121">Ce chemin d’accès indirect ajoute de la latence au trafic réseau et réduit les performances globales.</span><span class="sxs-lookup"><span data-stu-id="9cc82-121">This indirect path adds latency to the network traffic and decreases overall performance.</span></span> 

<span data-ttu-id="9cc82-122">La segmentation de tunnel vous permet de configurer votre client VPN pour empêcher l’envoi de certains types de trafic sur la connexion VPN vers le réseau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="9cc82-122">With split tunneling, you can configure your VPN client to exclude specific types of traffic from being sent over the VPN connection to the organization network.</span></span>

<span data-ttu-id="9cc82-123">Pour optimiser l’accès aux ressources cloud de Microsoft 365, configurez vos clients VPN avec la segmentation de tunnel afin d’exclure le trafic vers la catégorie **Optimiser** des points de terminaison Microsoft 365 sur la connexion VPN.</span><span class="sxs-lookup"><span data-stu-id="9cc82-123">To optimize access to Microsoft 365 cloud resources, configure your split tunneling VPN clients to exclude traffic to the **Optimize** category Microsoft 365 endpoints over the VPN connection.</span></span> <span data-ttu-id="9cc82-124">Pour plus d’informations, consultez [Catégories de points de terminaison Office 365](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles#new-office-365-endpoint-categories).</span><span class="sxs-lookup"><span data-stu-id="9cc82-124">For more information, see [Office 365 endpoint categories](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles#new-office-365-endpoint-categories).</span></span> <span data-ttu-id="9cc82-125">Consultez la liste des points de terminaison de catégorie Optimiser [ici](https://docs.microsoft.com/office365/enterprise/urls-and-ip-address-ranges).</span><span class="sxs-lookup"><span data-stu-id="9cc82-125">See the list of Optimize category endpoints [here](https://docs.microsoft.com/office365/enterprise/urls-and-ip-address-ranges).</span></span>

![Trafic réseau provenant de clients VPN avec segmentation de tunnel](../media/empower-people-to-work-remotely-remote-access/empower-people-to-work-remotely-remote-access-after-tunneling.png)

<span data-ttu-id="9cc82-127">Cela permet au client VPN d’envoyer et de recevoir du trafic de service cloud Microsoft 365 crucial directement via Internet et vers le point d’entrée le plus proche dans le réseau Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9cc82-127">This allows the VPN client to send and receive crucial Microsoft 365 cloud service traffic directly over the Internet and to the nearest entry point into the Microsoft network.</span></span>

<span data-ttu-id="9cc82-128">Pour plus d’informations et de conseils, voir [Optimiser la connectivité d’Office 365 pour les utilisateurs à distance à l’aide de la segmentation de tunnel de VPN](https://docs.microsoft.com/office365/enterprise/office-365-vpn-split-tunnel).</span><span class="sxs-lookup"><span data-stu-id="9cc82-128">For more information and guidance, see [Optimize Office 365 connectivity for remote users using VPN split tunneling](https://docs.microsoft.com/office365/enterprise/office-365-vpn-split-tunnel).</span></span>

## <a name="deploy-remote-access-when-all-your-apps-are-web-apps-and-you-have-hybrid-identity"></a><span data-ttu-id="9cc82-129">Déployer l’accès à distance lorsque toutes vos applications sont des applications web et que vous avez une identité hybride</span><span class="sxs-lookup"><span data-stu-id="9cc82-129">Deploy remote access when all your apps are web apps and you have hybrid identity</span></span>

<span data-ttu-id="9cc82-130">Si vos employés distants n’utilisent pas de client VPN classique et que vos comptes d’utilisateurs et groupes locaux sont synchronisés avec Azure AD, vous pouvez utiliser le proxy d’application Azure AD pour fournir un accès à distance sécurisé pour les applications web hébergées sur les serveurs intranet.</span><span class="sxs-lookup"><span data-stu-id="9cc82-130">If your remote workers are not using a traditional VPN client and your on-premises user accounts and groups are synchronized with Azure AD, you can use Azure AD Application Proxy to provide secure remote access for web-based applications hosted on intranet servers.</span></span> <span data-ttu-id="9cc82-131">Les applications web incluent les sites SharePoint, les serveurs Outlook Web Access ou toute autre application métier basée sur le web.</span><span class="sxs-lookup"><span data-stu-id="9cc82-131">Web-based applications include SharePoint sites, Outlook Web Access servers, or any other web-based line of business applications.</span></span> 

<span data-ttu-id="9cc82-132">Voici les composants du proxy d’application Azure AD.</span><span class="sxs-lookup"><span data-stu-id="9cc82-132">Here are the components of Azure AD Application Proxy.</span></span>

![Composants du proxy d’application Azure AD](../media/empower-people-to-work-remotely-remote-access/empower-people-to-work-remotely-remote-access-application-proxy.png)

<span data-ttu-id="9cc82-134">Si vous souhaitez en savoir plus, consultez la page [Présentation du proxy d’application Azure AD](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy).</span><span class="sxs-lookup"><span data-stu-id="9cc82-134">For more information, see this [overview of Azure AD Application Proxy](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy).</span></span>

## <a name="deploy-remote-access-when-not-all-your-apps-are-web-apps"></a><span data-ttu-id="9cc82-135">Déployer l’accès à distance lorsque l’ensemble de vos applications ne sont pas des applications web</span><span class="sxs-lookup"><span data-stu-id="9cc82-135">Deploy remote access when not all your apps are web apps</span></span>

<span data-ttu-id="9cc82-136">Si vos employés distants n’utilisent pas de client VPN classique et que l’une de vos applications n’est pas basée sur le web, vous pouvez utiliser un réseau privé virtuel (P2S) Azure.</span><span class="sxs-lookup"><span data-stu-id="9cc82-136">If your remote workers are not using a traditional VPN client and any of your apps are not web-based, you can use an Azure Point-to-Site (P2S) VPN.</span></span>

<span data-ttu-id="9cc82-137">Une connexion VPN P2S crée une connexion sécurisée entre un appareil de travail distant et le réseau de votre organisation via un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="9cc82-137">A P2S VPN connection creates a secure connection from a remote worker’s device to your organization network through an Azure virtual network.</span></span> 

![Composants d’Azure P2S VPN](../media/empower-people-to-work-remotely-remote-access/empower-people-to-work-remotely-remote-access-p2s-vpn.png)

<span data-ttu-id="9cc82-139">Si vous souhaitez en savoir plus, consultez la page [Présentation de P2S VPN](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-about).</span><span class="sxs-lookup"><span data-stu-id="9cc82-139">For more information, see this [overview of P2S VPN](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-about).</span></span>

## <a name="deploy-windows-virtual-desktop-to-provide-remote-access-for-remote-workers-using-personal-devices"></a><span data-ttu-id="9cc82-140">Déployer l’application de Windows Virtual Desktop pour fournir l’accès distant aux travailleurs à distance en utilisant des appareils personnels</span><span class="sxs-lookup"><span data-stu-id="9cc82-140">Deploy Windows Virtual Desktop to provide remote access for remote workers using personal devices</span></span> 

<span data-ttu-id="9cc82-141">Pour prendre en charge les travailleurs distants qui peuvent uniquement utiliser leurs appareils personnels et non gérés, utilisez l’application de Windows Virtual Desktop dans Azure pour créer et attribuer des bureaux virtuels à vos utilisateurs pour qu’ils les utilisent à partir de leur domicile.</span><span class="sxs-lookup"><span data-stu-id="9cc82-141">To support remote workers who can only use their personal and unmanaged devices, use Windows Virtual Desktop in Azure to create and allocate virtual desktops for your users to use from home.</span></span>

<span data-ttu-id="9cc82-142">Les PC virtualisés peuvent agir comme des PC connectés au réseau de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9cc82-142">Virtualized PCs can act just like PCs connected to your organization network.</span></span>

<span data-ttu-id="9cc82-143">Si vous souhaitez en savoir plus, consultez la page [Présentation de Windows Virtual Desktop](https://docs.microsoft.com/azure/virtual-desktop/overview).</span><span class="sxs-lookup"><span data-stu-id="9cc82-143">For more information, see [this overview of Windows Virtual Desktop](https://docs.microsoft.com/azure/virtual-desktop/overview).</span></span>

## <a name="admin-technical-resources-for-remote-access"></a><span data-ttu-id="9cc82-144">Ressources techniques dédiées aux administrateurs pour l’accès à distance</span><span class="sxs-lookup"><span data-stu-id="9cc82-144">Admin technical resources for remote access</span></span>

- [<span data-ttu-id="9cc82-145">Comment optimiser rapidement le trafic Office 365 pour les membres du personnel à distance et réduire la charge sur votre infrastructure</span><span class="sxs-lookup"><span data-stu-id="9cc82-145">How to quickly optimize Office 365 traffic for remote staff & reduce the load on your infrastructure</span></span>](https://techcommunity.microsoft.com/t5/office-365-blog/how-to-quickly-optimize-office-365-traffic-for-remote-staff-amp/ba-p/1214571)
- [<span data-ttu-id="9cc82-146">Optimiser la connectivité d’Office 365 pour les utilisateurs à distance à l’aide de la segmentation de tunnel VPN</span><span class="sxs-lookup"><span data-stu-id="9cc82-146">Optimize Office 365 connectivity for remote users using VPN split tunneling</span></span>](https://docs.microsoft.com/office365/enterprise/office-365-vpn-split-tunnel)

## <a name="results-of-step-2"></a><span data-ttu-id="9cc82-147">Résultats de l’étape 2</span><span class="sxs-lookup"><span data-stu-id="9cc82-147">Results of Step 2</span></span>

<span data-ttu-id="9cc82-148">Après le déploiement d’une solution d’accès à distance pour vos employés à distance :</span><span class="sxs-lookup"><span data-stu-id="9cc82-148">After deployment of a remote access solution for your remote workers:</span></span>

| <span data-ttu-id="9cc82-149">Configuration de l’accès à distance</span><span class="sxs-lookup"><span data-stu-id="9cc82-149">Remote access configuration</span></span> | <span data-ttu-id="9cc82-150">Résultats</span><span class="sxs-lookup"><span data-stu-id="9cc82-150">Results</span></span> |
|:-------|:-----|
| <span data-ttu-id="9cc82-151">Une solution VPN d’accès à distance est en place</span><span class="sxs-lookup"><span data-stu-id="9cc82-151">A remote access VPN solution is in place</span></span> | <span data-ttu-id="9cc82-152">Vous avez configuré votre client VPN d’accès distant pour la segmentation de tunnel et pour la catégorie Optimiser des points de terminaison Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9cc82-152">You have configured your remote access VPN client for split tunneling and for the Optimize category of Microsoft 365 endpoints.</span></span> |
| <span data-ttu-id="9cc82-153">Aucune solution VPN d’accès à distance et vous avez besoin d’un accès à distance uniquement pour les applications web locales</span><span class="sxs-lookup"><span data-stu-id="9cc82-153">No remote access VPN solution and you need remote access only to on-premises web-based apps</span></span> | <span data-ttu-id="9cc82-154">Vous avez configuré l’application proxy Azure.</span><span class="sxs-lookup"><span data-stu-id="9cc82-154">You have configured Azure Application Proxy.</span></span> |
| <span data-ttu-id="9cc82-155">Aucune solution VPN d’accès à distance et vous avez besoin d’accéder à des applications locales, dont certaines ne sont pas basées sur le web</span><span class="sxs-lookup"><span data-stu-id="9cc82-155">No remote access VPN solution and you need access to on-premises apps, some of which are not web-based</span></span> | <span data-ttu-id="9cc82-156">Vous avez configuré Azure P2S VPN.</span><span class="sxs-lookup"><span data-stu-id="9cc82-156">You have configured Azure P2S VPN.</span></span> |
| <span data-ttu-id="9cc82-157">Les employés à distance utilisent leurs appareils personnels chez eux</span><span class="sxs-lookup"><span data-stu-id="9cc82-157">Remote workers are using their personal devices from home</span></span> | <span data-ttu-id="9cc82-158">Vous avez configuré Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="9cc82-158">You have configured Windows Virtual Desktop.</span></span> |
|||

## <a name="next-step"></a><span data-ttu-id="9cc82-159">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="9cc82-159">Next step</span></span>

<span data-ttu-id="9cc82-160">Poursuivez avec l’[Étape 3](empower-people-to-work-remotely-manage-endpoints.md) pour gérer vos appareils, PC et autres points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="9cc82-160">Continue with [Step 3](empower-people-to-work-remotely-manage-endpoints.md) to manage your devices, PCs, and other endpoints.</span></span>
