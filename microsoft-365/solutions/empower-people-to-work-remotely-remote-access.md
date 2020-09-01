---
title: Étape 2. Fournir l’accès à distance aux applications et services locaux
f1.keywords:
- NOCSH
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 05/27/2020
audience: ITPro
ms.topic: article
ms.prod: microsoft-365-enterprise
localization_priority: Priority
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
- remotework
- m365solution-remotework
ms.custom: ''
description: Assurez-vous que vos employés à distance peuvent accéder aux ressources locales tout en optimisant l’accès aux services cloud de Microsoft 365.
ms.openlocfilehash: 7c928718a4d0f0d47fb601e6ab6e51f25c88a04a
ms.sourcegitcommit: 555d756c69ac9031d1fb928f2e1f9750beede066
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2020
ms.locfileid: "47308390"
---
# <a name="step-2-provide-remote-access-to-on-premises-apps-and-services"></a><span data-ttu-id="bc575-104">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="bc575-104">Step 2.</span></span> <span data-ttu-id="bc575-105">Fournir l’accès à distance aux applications et services locaux</span><span class="sxs-lookup"><span data-stu-id="bc575-105">Provide remote access to on-premises apps and services</span></span>

<span data-ttu-id="bc575-106">Si votre organisation utilise une solution VPN d’accès à distance, généralement avec les serveurs VPN sur la périphérie de votre réseau et les clients VPN installés sur les appareils de vos utilisateurs, vos utilisateurs peuvent utiliser les connexions VPN d’accès à distance pour accéder aux applications et serveurs locaux.</span><span class="sxs-lookup"><span data-stu-id="bc575-106">If your organization uses a remote access VPN solution, typically with VPN servers on the edge of your network and VPN clients installed on your users' devices, your users can use remote access VPN connections to access on-premises apps and servers.</span></span> <span data-ttu-id="bc575-107">Mais vous devrez peut-être optimiser le trafic vers les services cloud de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bc575-107">But you may need to optimize traffic to Microsoft 365 cloud-based services.</span></span>

<span data-ttu-id="bc575-108">Si vos utilisateurs n’utilisent pas de solution VPN, vous pouvez utiliser le proxy d’application Azure Active Directory (Azure AD) et le VPN Azure Point-to-Site (P2S) pour fournir un accès, si toutes vos applications sont basées sur le web.</span><span class="sxs-lookup"><span data-stu-id="bc575-108">If your users do not use a VPN solution, you can use Azure Active Directory (Azure AD) Application Proxy and Azure Point-to-Site (P2S) VPN to provide access, depending on whether all your apps are web-based.</span></span>

<span data-ttu-id="bc575-109">Il existe trois configurations principales :</span><span class="sxs-lookup"><span data-stu-id="bc575-109">There are three primary configurations:</span></span>

1. <span data-ttu-id="bc575-110">Vous utilisez déjà une solution VPN d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="bc575-110">You are already using a remote access VPN solution.</span></span>
2. <span data-ttu-id="bc575-111">Vous n’utilisez pas une solution VPN d’accès à distance, vous avez une identité hybride, et vous avez besoin d’un accès à distance uniquement pour les applications web locales.</span><span class="sxs-lookup"><span data-stu-id="bc575-111">You are not using a remote access VPN solution, you have hybrid identity, and you need remote access only to on-premises web-based apps.</span></span>
3. <span data-ttu-id="bc575-112">Vous n’utilisez pas de solution VPN d’accès à distance et vous avez besoin d’accéder à des applications locales, dont certaines ne sont pas basées sur le web.</span><span class="sxs-lookup"><span data-stu-id="bc575-112">You are not using a remote access VPN solution and you need access to on-premises apps, some of which are not web-based.</span></span>

<span data-ttu-id="bc575-113">Consultez cet organigramme pour accéder aux options de configuration de l’accès à distance décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="bc575-113">See this flowchart for the remote access configuration options discussed in this article.</span></span>

![Organigramme de configuration de l’accès à distance](../media/empower-people-to-work-remotely-remote-access/empower-people-to-work-remotely-remote-access-flowchart.png)

<span data-ttu-id="bc575-115">Avec les connexions d’accès à distance, vous pouvez également utiliser le [Bureau à distance](https://support.microsoft.com/help/4028379/windows-10-how-to-use-remote-desktop) pour connecter vos utilisateurs à un PC local.</span><span class="sxs-lookup"><span data-stu-id="bc575-115">With remote access connections, you can also use [Remote Desktop](https://support.microsoft.com/help/4028379/windows-10-how-to-use-remote-desktop) to connect your users to an on-premises PC.</span></span> <span data-ttu-id="bc575-116">Par exemple, un employé distant peut utiliser le Bureau à distance pour se connecter au PC de son bureau à partir de son appareil Windows, iOS ou Android.</span><span class="sxs-lookup"><span data-stu-id="bc575-116">For example, a remote worker can use Remote Desktop to connect to the PC in their office from their Windows, iOS or Android device.</span></span> <span data-ttu-id="bc575-117">Lorsqu’il est connecté à distance, il peut l’utiliser comme s’il était assis face à son PC.</span><span class="sxs-lookup"><span data-stu-id="bc575-117">Once they are remotely connected, they can use it as if they were sitting in front of it.</span></span>

## <a name="optimize-performance-for-remote-access-vpn-clients-to-microsoft-365-cloud-services"></a><span data-ttu-id="bc575-118">Optimiser les performances des clients VPN d’accès à distance aux services cloud de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bc575-118">Optimize performance for remote access VPN clients to Microsoft 365 cloud services</span></span>

<span data-ttu-id="bc575-119">Si vos employés à distance utilisent un client VPN traditionnel pour obtenir l’accès à distance au réseau de votre organisation, vérifiez que le client VPN a une prise en charge de la segmentation de tunnel.</span><span class="sxs-lookup"><span data-stu-id="bc575-119">If your remote workers are using a traditional VPN client to obtain remote access to your organization network, verify that the VPN client has split tunneling support.</span></span>

<span data-ttu-id="bc575-120">Sans cette segmentation, l’ensemble de votre trafic de travail à distance est envoyé sur la connexion VPN, où il doit être transféré vers les appareils Microsoft Edge de votre organisation, être traité, puis envoyé sur Internet.</span><span class="sxs-lookup"><span data-stu-id="bc575-120">Without split tunneling, all of your remote work traffic gets sent across the VPN connection, where it must be forwarded to your organization’s edge devices, get processed, and then sent on the Internet.</span></span>

![Trafic réseau provenant de clients VPN sans segmentation de tunnel](../media/empower-people-to-work-remotely-remote-access/empower-people-to-work-remotely-remote-access-before-tunneling.png)

<span data-ttu-id="bc575-122">Le trafic Microsoft 365 doit emprunter une route indirecte au sein de votre organisation, qui peut être transférée vers un point d’entrée réseau Microsoft éloigné loin de l’emplacement physique du client VPN.</span><span class="sxs-lookup"><span data-stu-id="bc575-122">Microsoft 365 traffic must take an indirect route through your organization, which could be the forwarded to a Microsoft network entry point far away from the VPN client’s physical location.</span></span> <span data-ttu-id="bc575-123">Ce chemin d’accès indirect ajoute de la latence au trafic réseau et réduit les performances globales.</span><span class="sxs-lookup"><span data-stu-id="bc575-123">This indirect path adds latency to the network traffic and decreases overall performance.</span></span> 

<span data-ttu-id="bc575-124">La segmentation de tunnel vous permet de configurer votre client VPN pour empêcher l’envoi de certains types de trafic sur la connexion VPN vers le réseau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="bc575-124">With split tunneling, you can configure your VPN client to exclude specific types of traffic from being sent over the VPN connection to the organization network.</span></span>

<span data-ttu-id="bc575-125">Pour optimiser l’accès aux ressources cloud de Microsoft 365, configurez vos clients VPN avec la segmentation de tunnel afin d’exclure le trafic vers la catégorie **Optimiser** des points de terminaison Microsoft 365 sur la connexion VPN.</span><span class="sxs-lookup"><span data-stu-id="bc575-125">To optimize access to Microsoft 365 cloud resources, configure your split tunneling VPN clients to exclude traffic to the **Optimize** category Microsoft 365 endpoints over the VPN connection.</span></span> <span data-ttu-id="bc575-126">Pour plus d’informations, consultez [Catégories de points de terminaison Office 365](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-network-connectivity-principles#new-office-365-endpoint-categories).</span><span class="sxs-lookup"><span data-stu-id="bc575-126">For more information, see [Office 365 endpoint categories](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-network-connectivity-principles#new-office-365-endpoint-categories).</span></span> <span data-ttu-id="bc575-127">Consultez la liste des points de terminaison de catégorie Optimiser [ici](https://docs.microsoft.com/microsoft-365/enterprise/urls-and-ip-address-ranges).</span><span class="sxs-lookup"><span data-stu-id="bc575-127">See the list of Optimize category endpoints [here](https://docs.microsoft.com/microsoft-365/enterprise/urls-and-ip-address-ranges).</span></span>

![Trafic réseau provenant de clients VPN avec segmentation de tunnel](../media/empower-people-to-work-remotely-remote-access/empower-people-to-work-remotely-remote-access-after-tunneling.png)

<span data-ttu-id="bc575-129">Cela permet au client VPN d’envoyer et de recevoir du trafic de service cloud Microsoft 365 crucial directement via Internet et vers le point d’entrée le plus proche dans le réseau Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bc575-129">This allows the VPN client to send and receive crucial Microsoft 365 cloud service traffic directly over the Internet and to the nearest entry point into the Microsoft network.</span></span>

<span data-ttu-id="bc575-130">Pour plus d’informations et de conseils, voir [Optimiser la connectivité d’Office 365 pour les utilisateurs à distance à l’aide de la segmentation de tunnel de VPN](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-vpn-split-tunnel??).</span><span class="sxs-lookup"><span data-stu-id="bc575-130">For more information and guidance, see [Optimize Office 365 connectivity for remote users using VPN split tunneling](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-vpn-split-tunnel??).</span></span>

## <a name="deploy-remote-access-when-all-your-apps-are-web-apps-and-you-have-hybrid-identity"></a><span data-ttu-id="bc575-131">Déployer l’accès à distance lorsque toutes vos applications sont des applications web et que vous avez une identité hybride</span><span class="sxs-lookup"><span data-stu-id="bc575-131">Deploy remote access when all your apps are web apps and you have hybrid identity</span></span>

<span data-ttu-id="bc575-132">Si vos employés distants n’utilisent pas de client VPN classique et que vos comptes d’utilisateurs et groupes locaux sont synchronisés avec Azure AD, vous pouvez utiliser le proxy d’application Azure AD pour fournir un accès à distance sécurisé pour les applications web hébergées sur les serveurs intranet.</span><span class="sxs-lookup"><span data-stu-id="bc575-132">If your remote workers are not using a traditional VPN client and your on-premises user accounts and groups are synchronized with Azure AD, you can use Azure AD Application Proxy to provide secure remote access for web-based applications hosted on intranet servers.</span></span> <span data-ttu-id="bc575-133">Les applications web incluent les sites SharePoint, les serveurs Outlook Web Access ou toute autre application métier basée sur le web.</span><span class="sxs-lookup"><span data-stu-id="bc575-133">Web-based applications include SharePoint sites, Outlook Web Access servers, or any other web-based line of business applications.</span></span> 

<span data-ttu-id="bc575-134">Voici les composants du proxy d’application Azure AD.</span><span class="sxs-lookup"><span data-stu-id="bc575-134">Here are the components of Azure AD Application Proxy.</span></span>

![Composants du proxy d’application Azure AD](../media/empower-people-to-work-remotely-remote-access/empower-people-to-work-remotely-remote-access-application-proxy.png)

<span data-ttu-id="bc575-136">Si vous souhaitez obtenir plus d’informations, consultez cette [vue d’ensemble des proxy d’application Azure AD](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy) et la [Partie 3 de la vidéo sur l’utilisation des proxy d’Azure AD](https://resources.techcommunity.microsoft.com/enabling-remote-work/#security).</span><span class="sxs-lookup"><span data-stu-id="bc575-136">For more information, see this [overview of Azure AD Application Proxy](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy) and the [Part 3 video on using Azure AD Application Proxy](https://resources.techcommunity.microsoft.com/enabling-remote-work/#security).</span></span>

>[!Note]
><span data-ttu-id="bc575-137">Le proxy d’application Azure AD ne fait pas partie de l’abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bc575-137">Azure AD Application Proxy is not included with a Microsoft 365 subscription.</span></span> <span data-ttu-id="bc575-138">Vous devez payer pour son utilisation avec un abonnement Azure distinct.</span><span class="sxs-lookup"><span data-stu-id="bc575-138">You must pay for usage with a separate Azure subscription.</span></span>
>

## <a name="deploy-remote-access-when-not-all-your-apps-are-web-apps"></a><span data-ttu-id="bc575-139">Déployer l’accès à distance lorsque l’ensemble de vos applications ne sont pas des applications web</span><span class="sxs-lookup"><span data-stu-id="bc575-139">Deploy remote access when not all your apps are web apps</span></span>

<span data-ttu-id="bc575-140">Si vos employés distants n’utilisent pas de client VPN classique et que l’une de vos applications n’est pas basée sur le web, vous pouvez utiliser un réseau privé virtuel (P2S) Azure.</span><span class="sxs-lookup"><span data-stu-id="bc575-140">If your remote workers are not using a traditional VPN client and any of your apps are not web-based, you can use an Azure Point-to-Site (P2S) VPN.</span></span>

<span data-ttu-id="bc575-141">Une connexion VPN P2S crée une connexion sécurisée entre un appareil de travail distant et le réseau de votre organisation via un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="bc575-141">A P2S VPN connection creates a secure connection from a remote worker’s device to your organization network through an Azure virtual network.</span></span> 

![Composants d’Azure P2S VPN](../media/empower-people-to-work-remotely-remote-access/empower-people-to-work-remotely-remote-access-p2s-vpn.png)

<span data-ttu-id="bc575-143">Si vous souhaitez en savoir plus, consultez la page [Présentation de P2S VPN](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-about).</span><span class="sxs-lookup"><span data-stu-id="bc575-143">For more information, see this [overview of P2S VPN](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-about).</span></span>

>[!Note]
><span data-ttu-id="bc575-144">Azure P2S VPN n’est pas inclus dans l’abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bc575-144">Azure P2S VPN is not included with a Microsoft 365 subscription.</span></span> <span data-ttu-id="bc575-145">Vous devez payer pour son utilisation avec un abonnement Azure distinct.</span><span class="sxs-lookup"><span data-stu-id="bc575-145">You must pay for usage with a separate Azure subscription.</span></span>
>

## <a name="deploy-windows-virtual-desktop-to-provide-remote-access-for-remote-workers-using-personal-devices"></a><span data-ttu-id="bc575-146">Déployer l’application de Windows Virtual Desktop pour fournir l’accès distant aux travailleurs à distance en utilisant des appareils personnels</span><span class="sxs-lookup"><span data-stu-id="bc575-146">Deploy Windows Virtual Desktop to provide remote access for remote workers using personal devices</span></span> 

<span data-ttu-id="bc575-147">Pour prendre en charge les travailleurs distants qui peuvent uniquement utiliser leurs appareils personnels et non gérés, utilisez l’application de Windows Virtual Desktop dans Azure pour créer et attribuer des bureaux virtuels à vos utilisateurs pour qu’ils les utilisent à partir de leur domicile.</span><span class="sxs-lookup"><span data-stu-id="bc575-147">To support remote workers who can only use their personal and unmanaged devices, use Windows Virtual Desktop in Azure to create and allocate virtual desktops for your users to use from home.</span></span> <span data-ttu-id="bc575-148">Les PC virtualisés peuvent agir comme des PC connectés au réseau de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bc575-148">Virtualized PCs can act just like PCs connected to your organization network.</span></span>

![Composants d’Azure Windows Virtual Desktop](../media/empower-people-to-work-remotely-remote-access/empower-people-to-work-remotely-remote-access-windows-virtual-desktop.png)

<span data-ttu-id="bc575-150">Si vous souhaitez plus d’informations, reportez-vous aux rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc575-150">For more information, see:</span></span> 

- <span data-ttu-id="bc575-151">[Cette vue d’ensemble de Windows Virtual Desktop](https://docs.microsoft.com/azure/virtual-desktop/overview).</span><span class="sxs-lookup"><span data-stu-id="bc575-151">[This overview of Windows Virtual Desktop](https://docs.microsoft.com/azure/virtual-desktop/overview).</span></span>
- <span data-ttu-id="bc575-152">[La partie 2 de la vidéo sur l’utilisation de l’application de Windows Virtual Desktop pour les travailleurs à distance](https://resources.techcommunity.microsoft.com/enabling-remote-work/#productivity).</span><span class="sxs-lookup"><span data-stu-id="bc575-152">[The Part 2 video on using Windows Virtual Desktop for remote workers](https://resources.techcommunity.microsoft.com/enabling-remote-work/#productivity).</span></span>

>[!Note]
><span data-ttu-id="bc575-153">Windows Virtual Desktop n’est pas inclus dans l’abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bc575-153">Windows Virtual Desktop is not included with a Microsoft 365 subscription.</span></span> <span data-ttu-id="bc575-154">Vous devez payer pour son utilisation avec un abonnement Azure distinct.</span><span class="sxs-lookup"><span data-stu-id="bc575-154">You must pay for usage with a separate Azure subscription.</span></span>
>

## <a name="protect-your-remote-desktop-services-connections-with-the-remote-desktop-services-gateway"></a><span data-ttu-id="bc575-155">Protéger vos connexions aux Services Bureau à distance avec la Passerelle des services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="bc575-155">Protect your Remote Desktop Services connections with the Remote Desktop Services Gateway</span></span>

<span data-ttu-id="bc575-156">Si vous utilisez les Services Bureau à distance (RDS) pour permettre aux employés de se connecter à des ordinateurs Windows sur votre réseau local, vous devez utiliser une Passerelle des services Bureau à distance Microsoft dans votre réseau de périmètre.</span><span class="sxs-lookup"><span data-stu-id="bc575-156">If you are using Remote Desktop Services (RDS) to allow employees to connect into Windows-based computers on your on-premises network, you should use a Microsoft Remote Desktop Services gateway in your edge network.</span></span> <span data-ttu-id="bc575-157">La passerelle utilise le protocole SSL (Secure Sockets Layer) pour chiffrer les communications et empêche le système hébergeant les services Bureau à distance d’être directement exposé à Internet.</span><span class="sxs-lookup"><span data-stu-id="bc575-157">The gateway uses Secure Sockets Layer (SSL) to encrypt communications and prevents the system hosting RDS from being directly exposed to the Internet.</span></span>

![Les Services Bureau à distance avec la Passerelle des services Bureau à distance](../media/empower-people-to-work-remotely-remote-access/empower-people-to-work-remotely-remote-access-remote-desktop.png)

<span data-ttu-id="bc575-159">Si vous souhaitez plus d’informations, consultez [cet article](https://www.microsoft.com/security/blog/2020/04/16/security-guidance-remote-desktop-adoption/).</span><span class="sxs-lookup"><span data-stu-id="bc575-159">See [this article](https://www.microsoft.com/security/blog/2020/04/16/security-guidance-remote-desktop-adoption/) for more information.</span></span>

## <a name="admin-technical-resources-for-remote-access"></a><span data-ttu-id="bc575-160">Ressources techniques dédiées aux administrateurs pour l’accès à distance</span><span class="sxs-lookup"><span data-stu-id="bc575-160">Admin technical resources for remote access</span></span>

- [<span data-ttu-id="bc575-161">Comment optimiser rapidement le trafic Office 365 pour les membres du personnel à distance et réduire la charge sur votre infrastructure</span><span class="sxs-lookup"><span data-stu-id="bc575-161">How to quickly optimize Office 365 traffic for remote staff & reduce the load on your infrastructure</span></span>](https://techcommunity.microsoft.com/t5/office-365-blog/how-to-quickly-optimize-office-365-traffic-for-remote-staff-amp/ba-p/1214571)
- [<span data-ttu-id="bc575-162">Optimiser la connectivité d’Office 365 pour les utilisateurs à distance à l’aide de la segmentation de tunnel VPN</span><span class="sxs-lookup"><span data-stu-id="bc575-162">Optimize Office 365 connectivity for remote users using VPN split tunneling</span></span>](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-vpn-split-tunnel?)

## <a name="results-of-step-2"></a><span data-ttu-id="bc575-163">Résultats de l’étape 2</span><span class="sxs-lookup"><span data-stu-id="bc575-163">Results of Step 2</span></span>

<span data-ttu-id="bc575-164">Après le déploiement d’une solution d’accès à distance pour vos employés à distance :</span><span class="sxs-lookup"><span data-stu-id="bc575-164">After deployment of a remote access solution for your remote workers:</span></span>

| <span data-ttu-id="bc575-165">Configuration de l’accès à distance</span><span class="sxs-lookup"><span data-stu-id="bc575-165">Remote access configuration</span></span> | <span data-ttu-id="bc575-166">Résultats</span><span class="sxs-lookup"><span data-stu-id="bc575-166">Results</span></span> |
|:-------|:-----|
| <span data-ttu-id="bc575-167">Une solution VPN d’accès à distance est en place</span><span class="sxs-lookup"><span data-stu-id="bc575-167">A remote access VPN solution is in place</span></span> | <span data-ttu-id="bc575-168">Vous avez configuré votre client VPN d’accès distant pour la segmentation de tunnel et pour la catégorie Optimiser des points de terminaison Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bc575-168">You have configured your remote access VPN client for split tunneling and for the Optimize category of Microsoft 365 endpoints.</span></span> |
| <span data-ttu-id="bc575-169">Aucune solution VPN d’accès à distance et vous avez besoin d’un accès à distance uniquement pour les applications web locales</span><span class="sxs-lookup"><span data-stu-id="bc575-169">No remote access VPN solution and you need remote access only to on-premises web-based apps</span></span> | <span data-ttu-id="bc575-170">Vous avez configuré l’application proxy Azure.</span><span class="sxs-lookup"><span data-stu-id="bc575-170">You have configured Azure Application Proxy.</span></span> |
| <span data-ttu-id="bc575-171">Aucune solution VPN d’accès à distance et vous avez besoin d’accéder à des applications locales, dont certaines ne sont pas basées sur le web</span><span class="sxs-lookup"><span data-stu-id="bc575-171">No remote access VPN solution and you need access to on-premises apps, some of which are not web-based</span></span> | <span data-ttu-id="bc575-172">Vous avez configuré Azure P2S VPN.</span><span class="sxs-lookup"><span data-stu-id="bc575-172">You have configured Azure P2S VPN.</span></span> |
| <span data-ttu-id="bc575-173">Les employés à distance utilisent leurs appareils personnels chez eux</span><span class="sxs-lookup"><span data-stu-id="bc575-173">Remote workers are using their personal devices from home</span></span> | <span data-ttu-id="bc575-174">Vous avez configuré Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="bc575-174">You have configured Windows Virtual Desktop.</span></span> |
| <span data-ttu-id="bc575-175">Les employés distants utilisent les connexions aux services Bureau à distance vers des systèmes locaux</span><span class="sxs-lookup"><span data-stu-id="bc575-175">Remote workers are using RDS connections to on-premises systems</span></span> | <span data-ttu-id="bc575-176">Vous avez déployé une passerelle des services Bureau à distance sur votre réseau de périmètre.</span><span class="sxs-lookup"><span data-stu-id="bc575-176">You have deployed a Remote Desktop Services gateway in your edge network.</span></span> |
|||

## <a name="next-step"></a><span data-ttu-id="bc575-177">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="bc575-177">Next step</span></span>

<span data-ttu-id="bc575-178">Continuez avec l’[Étape 3](empower-people-to-work-remotely-security-compliance.md) pour déployer les services de sécurité et de conformité Microsoft 365 pour protéger vos applications, données et appareils.</span><span class="sxs-lookup"><span data-stu-id="bc575-178">Continue with [Step 3](empower-people-to-work-remotely-security-compliance.md) to deploy Microsoft 365 security and compliance services to protect your apps, data, and devices.</span></span>
