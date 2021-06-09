---
title: Microsoft 365 Informations réseau
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 09/21/2020
audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
description: Microsoft 365 Informations réseau
ms.openlocfilehash: 10b1c66a8f9aae555c2841b2b290f341bec3c7ec
ms.sourcegitcommit: fb6c5e04ade1e82b26b2f911577b5ac721f1c544
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "52470555"
---
# <a name="microsoft-365-network-insights"></a><span data-ttu-id="32b81-103">Microsoft 365 Informations réseau</span><span class="sxs-lookup"><span data-stu-id="32b81-103">Microsoft 365 Network Insights</span></span>

<span data-ttu-id="32b81-104">**Les informations réseau sont** des mesures de performances collectées à partir de votre client Microsoft 365 et disponibles uniquement pour les utilisateurs administratifs de votre client.</span><span class="sxs-lookup"><span data-stu-id="32b81-104">**Network insights** are performance metrics collected from your Microsoft 365 tenant, and available to view only by administrative users in your tenant.</span></span> <span data-ttu-id="32b81-105">Insights are displayed in the Microsoft 365 Admin Center at <https://portal.microsoft.com/adminportal/home#/networkperformance> .</span><span class="sxs-lookup"><span data-stu-id="32b81-105">Insights are displayed in the Microsoft 365 Admin Center at <https://portal.microsoft.com/adminportal/home#/networkperformance>.</span></span>

<span data-ttu-id="32b81-106">Les informations sont conçues pour vous aider à concevoir des périmètres réseau pour vos bureaux.</span><span class="sxs-lookup"><span data-stu-id="32b81-106">Insights are intended to help in designing network perimeters for your office locations.</span></span> <span data-ttu-id="32b81-107">Chaque insight fournit des détails en direct sur les caractéristiques de performances d’un problème commun spécifique pour chaque emplacement géographique où les utilisateurs accèdent à votre client.</span><span class="sxs-lookup"><span data-stu-id="32b81-107">Each insight provides live details about the performance characteristics for a specific common issue for each geographic location where users are accessing your tenant.</span></span>

<span data-ttu-id="32b81-108">Il existe six informations réseau spécifiques qui peuvent être affichées pour chaque emplacement de bureau :</span><span class="sxs-lookup"><span data-stu-id="32b81-108">There are six specific network insights that may be shown for each office location:</span></span>

- [<span data-ttu-id="32b81-109">Sortie du réseau backhauled</span><span class="sxs-lookup"><span data-stu-id="32b81-109">Backhauled network egress</span></span>](#backhauled-network-egress)
- [<span data-ttu-id="32b81-110">Périphérique intermédiaire réseau</span><span class="sxs-lookup"><span data-stu-id="32b81-110">Network intermediary device</span></span>](#network-intermediary-device)
- [<span data-ttu-id="32b81-111">Meilleures performances détectées pour les clients proches de chez vous</span><span class="sxs-lookup"><span data-stu-id="32b81-111">Better performance detected for customers near you</span></span>](#better-performance-detected-for-customers-near-you)
- [<span data-ttu-id="32b81-112">Utilisation d’une porte d’Exchange Online service non optimale</span><span class="sxs-lookup"><span data-stu-id="32b81-112">Use of a non-optimal Exchange Online service front door</span></span>](#use-of-a-non-optimal-exchange-online-service-front-door)
- [<span data-ttu-id="32b81-113">Utilisation d’une porte d’entrée du service SharePoint Online non optimale</span><span class="sxs-lookup"><span data-stu-id="32b81-113">Use of a non-optimal SharePoint Online service front door</span></span>](#use-of-a-non-optimal-sharepoint-online-service-front-door)
- [<span data-ttu-id="32b81-114">Faible vitesse de téléchargement à partir SharePoint première ligne</span><span class="sxs-lookup"><span data-stu-id="32b81-114">Low download speed from SharePoint front door</span></span>](#low-download-speed-from-sharepoint-front-door)
- [<span data-ttu-id="32b81-115">Sortie réseau optimale de l’utilisateur chinois</span><span class="sxs-lookup"><span data-stu-id="32b81-115">China user optimal network egress</span></span>](#china-user-optimal-network-egress)

<span data-ttu-id="32b81-116">Il existe deux informations réseau au niveau du client qui peuvent être affichées pour le client.</span><span class="sxs-lookup"><span data-stu-id="32b81-116">There are two tenant level network insights that may be shown for the tenant.</span></span> <span data-ttu-id="32b81-117">Ceux-ci apparaissent également dans les pages de score de productivité :</span><span class="sxs-lookup"><span data-stu-id="32b81-117">These also appear in the productivity score pages:</span></span>

- [<span data-ttu-id="32b81-118">Exchange exemples de connexions touchés par des problèmes de connectivité</span><span class="sxs-lookup"><span data-stu-id="32b81-118">Exchange sampled connections impacted by connectivity issues</span></span>](#exchange-sampled-connections-impacted-by-connectivity-issues)
- [<span data-ttu-id="32b81-119">SharePoint exemples de connexions touchés par des problèmes de connectivité</span><span class="sxs-lookup"><span data-stu-id="32b81-119">SharePoint sampled connections impacted by connectivity issues</span></span>](#sharepoint-sampled-connections-impacted-by-connectivity-issues)

>[!IMPORTANT]
><span data-ttu-id="32b81-120">Les informations sur le réseau, les recommandations en matière de performances et les évaluations dans le Centre d’administration Microsoft 365 sont actuellement en état de prévisualisation et sont uniquement disponibles pour les locataires Microsoft 365 qui ont été inscrits au programme d’aperçu des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="32b81-120">Network insights, performance recommendations and assessments in the Microsoft 365 Admin Center is currently in preview status, and is only available for Microsoft 365 tenants that have been enrolled in the feature preview program.</span></span>

## <a name="backhauled-network-egress"></a><span data-ttu-id="32b81-121">Sortie du réseau backhauled</span><span class="sxs-lookup"><span data-stu-id="32b81-121">Backhauled network egress</span></span>

<span data-ttu-id="32b81-122">Cette information s’affiche si le service d’informations réseau détecte que la distance entre un emplacement d’utilisateur donné et la sortie réseau est supérieure à 500 km (800 kilomètres), ce qui indique que le trafic Microsoft 365 est rétrogradé vers un périphérique edge Internet ou un proxy commun.</span><span class="sxs-lookup"><span data-stu-id="32b81-122">This insight will be displayed if the network insights service detects that the distance from a given user location to the network egress is greater than 500 miles (800 kilometers), indicating that Microsoft 365 traffic is being backhauled to a common Internet edge device or proxy.</span></span>

<span data-ttu-id="32b81-123">Cette information est abrégée en « Egress » dans certains affichages récapitulatifs.</span><span class="sxs-lookup"><span data-stu-id="32b81-123">This insight is abbreviated as "Egress" in some summary views.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="32b81-124">![Sortie du réseau backhauled](../media/m365-mac-perf/m365-mac-perf-insights-detail-backhauled.png)</span><span class="sxs-lookup"><span data-stu-id="32b81-124">![Backhauled network egress](../media/m365-mac-perf/m365-mac-perf-insights-detail-backhauled.png)</span></span>

### <a name="what-does-this-mean"></a><span data-ttu-id="32b81-125">Qu’est-ce que cela signifie ?</span><span class="sxs-lookup"><span data-stu-id="32b81-125">What does this mean?</span></span>

<span data-ttu-id="32b81-126">Cela indique que la distance entre l’emplacement du bureau et la sortie réseau est de plus de 500 km (800 kilomètres).</span><span class="sxs-lookup"><span data-stu-id="32b81-126">This identifies that the distance between the office location and the network egress is more than 500 miles (800 kilometers).</span></span> <span data-ttu-id="32b81-127">L’emplacement du bureau est identifié par un emplacement d’ordinateur client obscurci et l’emplacement de sortie réseau est identifié à l’aide de l’adresse IP inversée pour les bases de données d’emplacements.</span><span class="sxs-lookup"><span data-stu-id="32b81-127">The office location is identified by an obfuscated client machine location and the network egress location is identified by using reverse IP Address to location databases.</span></span> <span data-ttu-id="32b81-128">L’emplacement du bureau peut être incorrect si Windows services de localisation sont désactivés sur les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="32b81-128">The office location may be inaccurate if Windows Location Services is disabled on machines.</span></span> <span data-ttu-id="32b81-129">L’emplacement de sortie réseau peut être incorrect si les informations de la base de données d’adresses IP inverses sont inexactes.</span><span class="sxs-lookup"><span data-stu-id="32b81-129">The network egress location may be inaccurate if the reverse IP Address database information is inaccurate.</span></span>

<span data-ttu-id="32b81-130">Ces informations incluent l’emplacement du bureau, le pourcentage estimé du nombre total d’utilisateurs locataires sur l’emplacement, l’emplacement de sortie du réseau actuel, la pertinence de l’emplacement de sortie, la distance entre l’emplacement et le point de sortie actuel, la date à laquelle la condition a été détectée pour la première fois et la date à laquelle la condition a été résolue.</span><span class="sxs-lookup"><span data-stu-id="32b81-130">Details for this insight include the office location, estimated percentage of total tenant user at the location, the current network egress location, relevance of the egress location, the distance between the location and the current egress point, the date the condition was first detected, and the date the condition was resolved.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="32b81-131">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="32b81-131">What should I do?</span></span>

<span data-ttu-id="32b81-132">Pour ce faire, nous vous recommandons d’utiliser une sortie réseau plus proche de l’emplacement du bureau afin que la connectivité puisse être acheminée de manière optimale vers le réseau global de Microsoft et vers la porte d’entrée du service Microsoft 365 la plus proche.</span><span class="sxs-lookup"><span data-stu-id="32b81-132">For this insight, we would recommend network egress closer to the office location so that connectivity can route optimally to Microsoft's global network and to the nearest Microsoft 365 service front door.</span></span> <span data-ttu-id="32b81-133">Une sortie étroite du réseau vers les emplacements de bureau des utilisateurs permet également d’améliorer les performances à l’avenir, car Microsoft étend les points de présence réseau et les portes avant du service Microsoft 365 à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="32b81-133">Having close network egress to users office locations also allows for improved performance in the future as Microsoft expands both network points of presence and Microsoft 365 service front doors in the future.</span></span>

<span data-ttu-id="32b81-134">Pour plus d’informations sur la résolution de ce problème, voir Egress [connexions](microsoft-365-network-connectivity-principles.md#egress-network-connections-locally) réseau localement dans Office 365 principes de [connectivité réseau.](microsoft-365-network-connectivity-principles.md)</span><span class="sxs-lookup"><span data-stu-id="32b81-134">For more information about how to resolve this issue, see [Egress network connections locally](microsoft-365-network-connectivity-principles.md#egress-network-connections-locally) in [Office 365 Network Connectivity Principles](microsoft-365-network-connectivity-principles.md).</span></span>

## <a name="network-intermediary-device"></a><span data-ttu-id="32b81-135">Périphérique intermédiaire réseau</span><span class="sxs-lookup"><span data-stu-id="32b81-135">Network intermediary device</span></span>

<span data-ttu-id="32b81-136">Cette information s’affiche si nous avons détecté des appareils entre vos utilisateurs et le réseau de Microsoft, ce qui peut avoir un impact sur Office 365 l’expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="32b81-136">This insight will be displayed if we detected devices between your users and Microsoft's network which may impact the Office 365 user experience.</span></span> <span data-ttu-id="32b81-137">Il est recommandé de les contourner pour des Microsoft 365 réseau spécifiques destinés aux centres de données Microsoft.</span><span class="sxs-lookup"><span data-stu-id="32b81-137">It is recommended that these be bypassed for specific Microsoft 365 network traffic that is destined for Microsoft datacenters.</span></span> <span data-ttu-id="32b81-138">Cette recommandation est également décrite dans Microsoft 365 [principes de connectivité réseau.](microsoft-365-network-connectivity-principles.md)</span><span class="sxs-lookup"><span data-stu-id="32b81-138">This recommendation is additionally described in [Microsoft 365 Network Connectivity Principles](microsoft-365-network-connectivity-principles.md).</span></span> 

<span data-ttu-id="32b81-139">L’une des informations intermédiaires du réseau que nous montrons est la coupure SSL et l’inspection lorsque les points de terminaison réseau Office 365 critiques pour les Exchange, SharePoint et Teams sont interceptés et déchiffrés par des périphériques intermédiaires réseau.</span><span class="sxs-lookup"><span data-stu-id="32b81-139">One network intermediary insight we show is SSL break and inspection when critical Office 365 network endpoints for Exchange, SharePoint and Teams are intercepted and decrypted by network intermediary devices.</span></span>

### <a name="what-does-this-mean"></a><span data-ttu-id="32b81-140">Qu’est-ce que cela signifie ?</span><span class="sxs-lookup"><span data-stu-id="32b81-140">What does this mean?</span></span>

<span data-ttu-id="32b81-141">Les périphériques intermédiaires réseau tels que les serveurs proxy, les VPN et les périphériques de protection contre la perte de données peuvent affecter les performances et la stabilité des clients Microsoft 365 où le trafic est intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="32b81-141">Network intermediary devices such as proxy servers, VPNs, and data loss prevention devices can affect performance and stability of Microsoft 365 clients where traffic is intermediated.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="32b81-142">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="32b81-142">What should I do?</span></span>

<span data-ttu-id="32b81-143">Configurez le périphérique intermédiaire réseau détecté pour contourner le traitement du trafic Microsoft 365 réseau.</span><span class="sxs-lookup"><span data-stu-id="32b81-143">Configure the network intermediary device that was detected to bypass processing for Microsoft 365 network traffic.</span></span>

## <a name="better-performance-detected-for-customers-near-you"></a><span data-ttu-id="32b81-144">Meilleures performances détectées pour les clients proches de chez vous</span><span class="sxs-lookup"><span data-stu-id="32b81-144">Better performance detected for customers near you</span></span>

<span data-ttu-id="32b81-145">Cette information s’affiche si le service d’informations réseau détecte qu’un nombre significatif de clients dans votre zone d’information offrent de meilleures performances que les utilisateurs de votre organisation à cet emplacement de bureau.</span><span class="sxs-lookup"><span data-stu-id="32b81-145">This insight will be displayed if the network insights service detects that a significant number of customers in your metro area have better performance than users in your organization at this office location.</span></span>

<span data-ttu-id="32b81-146">Cette information est abrégée en « Homologues » dans certains affichages récapitulatifs.</span><span class="sxs-lookup"><span data-stu-id="32b81-146">This insight is abbreviated as "Peers" in some summary views.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="32b81-147">![Performances relatives du réseau](../media/m365-mac-perf/m365-mac-perf-insights-detail-cust-near-you.png)</span><span class="sxs-lookup"><span data-stu-id="32b81-147">![Relative network performance](../media/m365-mac-perf/m365-mac-perf-insights-detail-cust-near-you.png)</span></span>

### <a name="what-does-this-mean"></a><span data-ttu-id="32b81-148">Qu’est-ce que cela signifie ?</span><span class="sxs-lookup"><span data-stu-id="32b81-148">What does this mean?</span></span>

<span data-ttu-id="32b81-149">Cette vue d’ensemble examine les performances globales Microsoft 365 clients dans la même ville que cet emplacement de bureau.</span><span class="sxs-lookup"><span data-stu-id="32b81-149">This insight examines the aggregate performance of Microsoft 365 customers in the same city as this office location.</span></span> <span data-ttu-id="32b81-150">Cette information s’affiche si la latence moyenne de vos utilisateurs est supérieure de 10 % à la latence moyenne des locataires voisins.</span><span class="sxs-lookup"><span data-stu-id="32b81-150">This insight is displayed if the average latency of your users is 10% greater than the average latency of neighboring tenants.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="32b81-151">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="32b81-151">What should I do?</span></span>

<span data-ttu-id="32b81-152">Il peut y avoir de nombreuses raisons à cette condition, notamment la latence dans votre réseau d’entreprise ou votre isp isp, les goulots d’étranglement ou les problèmes de conception de l’architecture.</span><span class="sxs-lookup"><span data-stu-id="32b81-152">There could be many reasons for this condition, including latency in your corporate network or ISP, bottlenecks, or architecture design issues.</span></span> <span data-ttu-id="32b81-153">Examinez la latence entre chaque saut de l’itinéraire entre votre réseau de bureau et la Microsoft 365 frontale actuelle.</span><span class="sxs-lookup"><span data-stu-id="32b81-153">Examine the latency between each hop in the route between your office network and the current Microsoft 365 front door.</span></span> <span data-ttu-id="32b81-154">Pour plus d’informations, [Microsoft 365 principes de connectivité réseau.](microsoft-365-network-connectivity-principles.md)</span><span class="sxs-lookup"><span data-stu-id="32b81-154">For more information, see [Microsoft 365 Network Connectivity Principles](microsoft-365-network-connectivity-principles.md).</span></span>

## <a name="use-of-a-non-optimal-exchange-online-service-front-door"></a><span data-ttu-id="32b81-155">Utilisation d’une porte d’Exchange Online service non optimale</span><span class="sxs-lookup"><span data-stu-id="32b81-155">Use of a non-optimal Exchange Online service front door</span></span>

<span data-ttu-id="32b81-156">Cette information s’affiche si le service d’informations réseau détecte que les utilisateurs d’un emplacement spécifique ne se connectent pas à une porte d’entrée Exchange Online service optimale.</span><span class="sxs-lookup"><span data-stu-id="32b81-156">This insight will be displayed if the network insights service detects that users in a specific location are not connecting to an optimal Exchange Online service front door.</span></span>

<span data-ttu-id="32b81-157">Cette information est abrégée en « Routage » dans certains affichages récapitulatifs.</span><span class="sxs-lookup"><span data-stu-id="32b81-157">This insight is abbreviated as "Routing" in some summary views.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="32b81-158">![Porte frontale EXO non optimale](../media/m365-mac-perf/m365-mac-perf-insights-detail-front-door-exo.png)</span><span class="sxs-lookup"><span data-stu-id="32b81-158">![Non-optimal EXO front door](../media/m365-mac-perf/m365-mac-perf-insights-detail-front-door-exo.png)</span></span>

### <a name="what-does-this-mean"></a><span data-ttu-id="32b81-159">Qu’est-ce que cela signifie ?</span><span class="sxs-lookup"><span data-stu-id="32b81-159">What does this mean?</span></span>

<span data-ttu-id="32b81-160">Nous listons Exchange Online porte d’entrée du service qui conviennent à une utilisation à partir de la ville de l’emplacement du bureau avec de bonnes performances.</span><span class="sxs-lookup"><span data-stu-id="32b81-160">We list Exchange Online service front doors which are suitable for use from the office location city with good performance.</span></span> <span data-ttu-id="32b81-161">Si le test actuel indique l’utilisation d’un Exchange Online service frontal qui ne figure pas dans cette liste, nous appelons cette recommandation.</span><span class="sxs-lookup"><span data-stu-id="32b81-161">If the current test shows use of an Exchange Online service front door not on this list, then we call out this recommendation.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="32b81-162">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="32b81-162">What should I do?</span></span>

<span data-ttu-id="32b81-163">L’utilisation d’une porte frontale de service Exchange Online non optimale peut être causée par une rétrograder du réseau avant la sortie du réseau d’entreprise, auquel cas nous recommandons une sortie locale et directe du réseau.</span><span class="sxs-lookup"><span data-stu-id="32b81-163">Use of a non-optimal Exchange Online service front door could be caused by network backhaul before the corporate network egress in which case we recommend local and direct network egress.</span></span> <span data-ttu-id="32b81-164">Cela peut également être dû à l’utilisation d’un serveur récursif DNS distant, auquel cas nous vous recommandons d’aligner le serveur de résolution récursive DNS avec la sortie réseau.</span><span class="sxs-lookup"><span data-stu-id="32b81-164">It could also be caused by use of a remote DNS Recursive Resolver server in which case we recommend aligning the DNS Recursive Resolver server with the network egress.</span></span>

## <a name="use-of-a-non-optimal-sharepoint-online-service-front-door"></a><span data-ttu-id="32b81-165">Utilisation d’une porte d’entrée du service SharePoint Online non optimale</span><span class="sxs-lookup"><span data-stu-id="32b81-165">Use of a non-optimal SharePoint Online service front door</span></span>

<span data-ttu-id="32b81-166">Cette information s’affiche si le service d’informations réseau détecte que les utilisateurs situés à un emplacement spécifique ne se connectent pas à la porte d’entrée du service SharePoint Online la plus proche.</span><span class="sxs-lookup"><span data-stu-id="32b81-166">This insight will be displayed if the network insights service detects that users in a specific location are not connecting to the closest SharePoint Online service front door.</span></span>

<span data-ttu-id="32b81-167">Cette information est abrégée en « Afd » dans certains affichages récapitulatifs.</span><span class="sxs-lookup"><span data-stu-id="32b81-167">This insight is abbreviated as "Afd" in some summary views.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="32b81-168">![Porte d’entrée SPO non optimale](../media/m365-mac-perf/m365-mac-perf-insights-detail-front-door-spo.png)</span><span class="sxs-lookup"><span data-stu-id="32b81-168">![Non-optimal SPO front door](../media/m365-mac-perf/m365-mac-perf-insights-detail-front-door-spo.png)</span></span>

### <a name="what-does-this-mean"></a><span data-ttu-id="32b81-169">Qu’est-ce que cela signifie ?</span><span class="sxs-lookup"><span data-stu-id="32b81-169">What does this mean?</span></span>

<span data-ttu-id="32b81-170">Nous identifions la SharePoint frontale du service en ligne à qui le client de test se connecte.</span><span class="sxs-lookup"><span data-stu-id="32b81-170">We identify the SharePoint Online service front door that the test client is connecting to.</span></span> <span data-ttu-id="32b81-171">Ensuite, pour la ville de l’emplacement du bureau, nous comparons cela à la porte d’SharePoint service en ligne prévue pour cette ville.</span><span class="sxs-lookup"><span data-stu-id="32b81-171">Then for the office location city we compare that to the expected SharePoint Online service front door for that city.</span></span> <span data-ttu-id="32b81-172">Si ce n’est pas le cas, nous vous en faisons la recommandation.</span><span class="sxs-lookup"><span data-stu-id="32b81-172">If it doesn't match, then we make this recommendation.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="32b81-173">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="32b81-173">What should I do?</span></span>

<span data-ttu-id="32b81-174">L’utilisation d’une porte d’entrée du service SharePoint Online non optimale peut être causée par une rétrograder du réseau avant la sortie du réseau d’entreprise, auquel cas nous recommandons la sortie locale et directe du réseau.</span><span class="sxs-lookup"><span data-stu-id="32b81-174">Use of a non-optimal SharePoint Online service front door could be caused by network backhaul before the corporate network egress in which case we recommend local and direct network egress.</span></span> <span data-ttu-id="32b81-175">Cela peut également être dû à l’utilisation d’un serveur récursif DNS distant, auquel cas nous vous recommandons d’aligner le serveur de résolution récursive DNS avec la sortie réseau.</span><span class="sxs-lookup"><span data-stu-id="32b81-175">It could also be caused by use of a remote DNS Recursive Resolver server in which case we recommend aligning the DNS Recursive Resolver server with the network egress.</span></span>

## <a name="low-download-speed-from-sharepoint-front-door"></a><span data-ttu-id="32b81-176">Faible vitesse de téléchargement à partir SharePoint première ligne</span><span class="sxs-lookup"><span data-stu-id="32b81-176">Low download speed from SharePoint front door</span></span>

<span data-ttu-id="32b81-177">Cette information s’affiche si le service d’informations réseau détecte que la bande passante entre l’emplacement de bureau spécifique et SharePoint Online est inférieure à 1 Mbits/s.</span><span class="sxs-lookup"><span data-stu-id="32b81-177">This insight will be displayed if the network insights service detects that bandwidth between the specific office location and SharePoint Online is less than 1 MBps.</span></span>

<span data-ttu-id="32b81-178">Cette information est abrégée « Débit » dans certains affichages récapitulatifs.</span><span class="sxs-lookup"><span data-stu-id="32b81-178">This insight is abbreviated as "Throughput" in some summary views.</span></span>

### <a name="what-does-this-mean"></a><span data-ttu-id="32b81-179">Qu’est-ce que cela signifie ?</span><span class="sxs-lookup"><span data-stu-id="32b81-179">What does this mean?</span></span>

<span data-ttu-id="32b81-180">La vitesse de téléchargement qu’un utilisateur peut obtenir à partir de SharePoint Online et des OneDrive Entreprise frontales du service est mesurée en mégaoctets par seconde (MBits/s).</span><span class="sxs-lookup"><span data-stu-id="32b81-180">The download speed that a user can get from SharePoint Online and OneDrive for Business service front doors is measured in megabytes per second (MBps).</span></span> <span data-ttu-id="32b81-181">Si cette valeur est inférieure à 1 Mbits/s, nous fournissons cette information.</span><span class="sxs-lookup"><span data-stu-id="32b81-181">If this value is less than 1 MBps then we provide this insight.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="32b81-182">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="32b81-182">What should I do?</span></span>

<span data-ttu-id="32b81-183">Pour améliorer les vitesses de téléchargement, vous devrez peut-être augmenter la bande passante.</span><span class="sxs-lookup"><span data-stu-id="32b81-183">To improve download speeds, bandwidth may need to be increased.</span></span> <span data-ttu-id="32b81-184">Sinon, il peut y avoir une congestion du réseau entre les ordinateurs des utilisateurs à l’emplacement du bureau et le SharePoint du service en ligne.</span><span class="sxs-lookup"><span data-stu-id="32b81-184">Alternatively, there may be network congestion between user machines at the office location and the SharePoint Online service front door.</span></span> <span data-ttu-id="32b81-185">Cette perte est parfois appelée perte congestive et limite la vitesse de téléchargement disponible pour les utilisateurs, même si une bande passante suffisante est disponible.</span><span class="sxs-lookup"><span data-stu-id="32b81-185">This is sometimes called congestive loss and it restricts the download speed available to users even if sufficient bandwidth is available.</span></span>

## <a name="china-user-optimal-network-egress"></a><span data-ttu-id="32b81-186">Sortie réseau optimale de l’utilisateur chinois</span><span class="sxs-lookup"><span data-stu-id="32b81-186">China user optimal network egress</span></span>

<span data-ttu-id="32b81-187">Cette information s’affiche si des utilisateurs de votre organisation en Chine se connectent à votre client Microsoft 365 dans d’autres emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="32b81-187">This insight will be displayed if your organization has users in China connecting to your Microsoft 365 tenant in other geographic locations.</span></span> 

### <a name="what-does-this-mean"></a><span data-ttu-id="32b81-188">Qu’est-ce que cela signifie ?</span><span class="sxs-lookup"><span data-stu-id="32b81-188">What does this mean?</span></span>

<span data-ttu-id="32b81-189">Si votre organisation dispose d’une connectivité WAN privée, nous vous recommandons de configurer un circuit réseau WAN à partir de vos bureaux en Chine qui dispose d’une sortie réseau vers Internet dans l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="32b81-189">If your organization has private WAN connectivity, we recommend configuring a network WAN circuit from your office locations in China that has network egress to the Internet in any of the following locations:</span></span>

- <span data-ttu-id="32b81-190">Hong Kong</span><span class="sxs-lookup"><span data-stu-id="32b81-190">Hong Kong</span></span>
- <span data-ttu-id="32b81-191">Japon</span><span class="sxs-lookup"><span data-stu-id="32b81-191">Japan</span></span>
- <span data-ttu-id="32b81-192">Taïwan</span><span class="sxs-lookup"><span data-stu-id="32b81-192">Taiwan</span></span>
- <span data-ttu-id="32b81-193">Corée du Sud</span><span class="sxs-lookup"><span data-stu-id="32b81-193">South Korea</span></span>
- <span data-ttu-id="32b81-194">Singapour</span><span class="sxs-lookup"><span data-stu-id="32b81-194">Singapore</span></span>
- <span data-ttu-id="32b81-195">Malaisie</span><span class="sxs-lookup"><span data-stu-id="32b81-195">Malaysia</span></span>

<span data-ttu-id="32b81-196">Une sortie d’Internet plus éloignée des utilisateurs que ces emplacements réduit les performances, et la sortie en Chine peut entraîner des problèmes de latence et de connectivité élevés en raison d’une congestion croisée.</span><span class="sxs-lookup"><span data-stu-id="32b81-196">Internet egress further away from users than these locations will reduce performance, and egress in China may cause high latency and connectivity issues due to cross-border congestion.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="32b81-197">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="32b81-197">What should I do?</span></span>

<span data-ttu-id="32b81-198">Pour plus d’informations sur la façon d’atténuer les problèmes de performances liés à cette information, voir Microsoft 365 optimisation globale des performances des clients pour les [utilisateurs chinois.](microsoft-365-networking-china.md)</span><span class="sxs-lookup"><span data-stu-id="32b81-198">For more information about how to mitigate performance issues related to this insight, see [Microsoft 365 global tenant performance optimization for China users](microsoft-365-networking-china.md).</span></span>

## <a name="exchange-sampled-connections-impacted-by-connectivity-issues"></a><span data-ttu-id="32b81-199">Exchange exemples de connexions touchés par des problèmes de connectivité</span><span class="sxs-lookup"><span data-stu-id="32b81-199">Exchange sampled connections impacted by connectivity issues</span></span>

<span data-ttu-id="32b81-200">Cette information indique quand 50 % ou plus des connexions échantillonées sont impactées.</span><span class="sxs-lookup"><span data-stu-id="32b81-200">This insight will show when 50% or more of the sampled connections are impacted.</span></span> <span data-ttu-id="32b81-201">L’impact est défini par l Exchange évaluation inférieure à 60 % pour chaque échantillon.</span><span class="sxs-lookup"><span data-stu-id="32b81-201">The impact is defined by the Exchange assessment being below 60% for each sample.</span></span>

### <a name="what-does-this-mean"></a><span data-ttu-id="32b81-202">Qu’est-ce que cela signifie ?</span><span class="sxs-lookup"><span data-stu-id="32b81-202">What does this mean?</span></span>

<span data-ttu-id="32b81-203">Il s’agit d’une indication que la majorité de vos utilisateurs sont susceptibles de rencontre des problèmes d’expérience utilisateur avec Outlook connexion à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="32b81-203">It is an indication that the majority of your users are likely to be experiencing user experience issues with Outlook connecting to Exchange Online.</span></span> <span data-ttu-id="32b81-204">Le pourcentage d’échantillons représente probablement le pourcentage d’utilisateurs qui indiquent moins de 60 points.</span><span class="sxs-lookup"><span data-stu-id="32b81-204">The percentage of samples likely represents the percentage of users who show below 60 points.</span></span>  

### <a name="what-should-i-do"></a><span data-ttu-id="32b81-205">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="32b81-205">What should I do?</span></span>

<span data-ttu-id="32b81-206">Activez la visibilité de la connectivité réseau de l’emplacement du bureau si vous ne l’avez pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="32b81-206">Enable office location network connectivity visibility if you have not already done so.</span></span> <span data-ttu-id="32b81-207">Vous souhaitez identifier les bureaux qui sont touchés par une connectivité réseau médiocre qui a un impact sur Exchange et trouver des moyens d’améliorer le périmètre réseau à chaque bureau qui connecte les utilisateurs au réseau de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="32b81-207">You want to identify which offices are impacted by poor network connectivity that is impacting Exchange and find ways to improve the network perimeter at each that connects the users to Microsoft's network.</span></span>

## <a name="sharepoint-sampled-connections-impacted-by-connectivity-issues"></a><span data-ttu-id="32b81-208">SharePoint exemples de connexions touchés par des problèmes de connectivité</span><span class="sxs-lookup"><span data-stu-id="32b81-208">SharePoint sampled connections impacted by connectivity issues</span></span>

<span data-ttu-id="32b81-209">Cette information indique quand 50 % ou plus des connexions échantillonées sont impactées.</span><span class="sxs-lookup"><span data-stu-id="32b81-209">This insight will show when 50% or more of the sampled connections are impacted.</span></span> <span data-ttu-id="32b81-210">L’impact est défini par l’évaluation SharePoint inférieure à 40 % pour chaque échantillon.</span><span class="sxs-lookup"><span data-stu-id="32b81-210">The impact is defined by the SharePoint assessment being below 40% for each sample.</span></span>

### <a name="what-does-this-mean"></a><span data-ttu-id="32b81-211">Qu’est-ce que cela signifie ?</span><span class="sxs-lookup"><span data-stu-id="32b81-211">What does this mean?</span></span>

<span data-ttu-id="32b81-212">Cela indique que la majorité de vos utilisateurs rencontreront probablement des problèmes d’expérience utilisateur avec SharePoint et OneDrive.</span><span class="sxs-lookup"><span data-stu-id="32b81-212">It is an indication that the majority of your users are likely to be experiencing user experience issues with SharePoint and OneDrive.</span></span> <span data-ttu-id="32b81-213">Le pourcentage d’échantillons représente probablement le pourcentage d’utilisateurs qui indiquent moins de 40 points.</span><span class="sxs-lookup"><span data-stu-id="32b81-213">The percentage of samples likely represents the percentage of users who show below 40 points.</span></span>  

### <a name="what-should-i-do"></a><span data-ttu-id="32b81-214">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="32b81-214">What should I do?</span></span>

<span data-ttu-id="32b81-215">Activez la visibilité de la connectivité réseau de l’emplacement du bureau si vous ne l’avez pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="32b81-215">Enable office location network connectivity visibility if you have not already done so.</span></span> <span data-ttu-id="32b81-216">Vous souhaitez identifier les bureaux qui sont touchés par une connectivité réseau médiocre qui a un impact sur SharePoint et trouver des moyens d’améliorer le périmètre réseau à chaque bureau qui connecte les utilisateurs au réseau de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="32b81-216">You want to identify which offices are impacted by poor network connectivity that is impacting SharePoint and find ways to improve the network perimeter at each that connects the users to Microsoft's network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32b81-217">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32b81-217">Related topics</span></span>

[<span data-ttu-id="32b81-218">Connectivité réseau dans le Centre d’administration Microsoft 365 (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="32b81-218">Network connectivity in the Microsoft 365 Admin Center (preview)</span></span>](office-365-network-mac-perf-overview.md)

[<span data-ttu-id="32b81-219">Microsoft 365'évaluation réseau (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="32b81-219">Microsoft 365 network assessment (preview)</span></span>](office-365-network-mac-perf-score.md)

[<span data-ttu-id="32b81-220">Microsoft 365 de test de connectivité réseau (aperçu)</span><span class="sxs-lookup"><span data-stu-id="32b81-220">Microsoft 365 network connectivity test tool (preview)</span></span>](office-365-network-mac-perf-onboarding-tool.md)

[<span data-ttu-id="32b81-221">Microsoft 365 Services de localisation de connectivité réseau (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="32b81-221">Microsoft 365 Network Connectivity Location Services (preview)</span></span>](office-365-network-mac-location-services.md)
