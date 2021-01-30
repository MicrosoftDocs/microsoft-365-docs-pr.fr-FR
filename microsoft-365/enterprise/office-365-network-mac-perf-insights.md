---
title: Microsoft 365 Network Insights (prévisualisation)
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
description: Microsoft 365 Network Insights (prévisualisation)
ms.openlocfilehash: d6786ce6cd58ce6f350804fbbacd272b8c077dc0
ms.sourcegitcommit: 1ac884d8470b2f2a58b6f79e324fd91e4d11dceb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2021
ms.locfileid: "50055472"
---
# <a name="microsoft-365-network-insights-preview"></a><span data-ttu-id="674d2-103">Microsoft 365 Network Insights (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="674d2-103">Microsoft 365 Network Insights (preview)</span></span>

<span data-ttu-id="674d2-104">**Les informations réseau sont** des mesures de performances collectées à partir de votre client Microsoft 365 et disponibles uniquement pour les utilisateurs administratifs de votre client.</span><span class="sxs-lookup"><span data-stu-id="674d2-104">**Network insights** are performance metrics collected from your Microsoft 365 tenant, and available to view only by administrative users in your tenant.</span></span> <span data-ttu-id="674d2-105">Les informations sont affichées dans le Centre d’administration Microsoft 365 à l’adresse <https://portal.microsoft.com/adminportal/home#/networkperformance> .</span><span class="sxs-lookup"><span data-stu-id="674d2-105">Insights are displayed in the Microsoft 365 Admin Center at <https://portal.microsoft.com/adminportal/home#/networkperformance>.</span></span>

<span data-ttu-id="674d2-106">Les informations sont conçues pour vous aider à concevoir des périmètres réseau pour vos bureaux.</span><span class="sxs-lookup"><span data-stu-id="674d2-106">Insights are intended to help in designing network perimeters for your office locations.</span></span> <span data-ttu-id="674d2-107">Chaque insight fournit des détails en direct sur les caractéristiques de performances d’un problème commun spécifique pour chaque emplacement géographique où les utilisateurs accèdent à votre client.</span><span class="sxs-lookup"><span data-stu-id="674d2-107">Each insight provides live details about the performance characteristics for a specific common issue for each geographic location where users are accessing your tenant.</span></span>

<span data-ttu-id="674d2-108">Il existe six informations réseau spécifiques qui peuvent être affichées pour chaque emplacement de bureau :</span><span class="sxs-lookup"><span data-stu-id="674d2-108">There are six specific network insights that may be shown for each office location:</span></span>

- [<span data-ttu-id="674d2-109">Sortie du réseau backhauled</span><span class="sxs-lookup"><span data-stu-id="674d2-109">Backhauled network egress</span></span>](#backhauled-network-egress)
- [<span data-ttu-id="674d2-110">Périphérique intermédiaire réseau</span><span class="sxs-lookup"><span data-stu-id="674d2-110">Network intermediary device</span></span>](#network-intermediary-device)
- [<span data-ttu-id="674d2-111">Meilleures performances détectées pour les clients proches de chez vous</span><span class="sxs-lookup"><span data-stu-id="674d2-111">Better performance detected for customers near you</span></span>](#better-performance-detected-for-customers-near-you)
- [<span data-ttu-id="674d2-112">Utilisation d’une porte d’entrée de service Exchange Online non optimale</span><span class="sxs-lookup"><span data-stu-id="674d2-112">Use of a non-optimal Exchange Online service front door</span></span>](#use-of-a-non-optimal-exchange-online-service-front-door)
- [<span data-ttu-id="674d2-113">Utilisation d’une porte d’entrée de service SharePoint Online non optimale</span><span class="sxs-lookup"><span data-stu-id="674d2-113">Use of a non-optimal SharePoint Online service front door</span></span>](#use-of-a-non-optimal-sharepoint-online-service-front-door)
- [<span data-ttu-id="674d2-114">Vitesse de téléchargement faible à partir de la porte d’entrée SharePoint</span><span class="sxs-lookup"><span data-stu-id="674d2-114">Low download speed from SharePoint front door</span></span>](#low-download-speed-from-sharepoint-front-door)
- [<span data-ttu-id="674d2-115">Sortie réseau optimale de l’utilisateur chinois</span><span class="sxs-lookup"><span data-stu-id="674d2-115">China user optimal network egress</span></span>](#china-user-optimal-network-egress)

<span data-ttu-id="674d2-116">Il existe deux informations réseau au niveau du client qui peuvent être affichées pour le client.</span><span class="sxs-lookup"><span data-stu-id="674d2-116">There are two tenant level network insights that may be shown for the tenant.</span></span> <span data-ttu-id="674d2-117">Ceux-ci apparaissent également dans les pages de score de producvitivy :</span><span class="sxs-lookup"><span data-stu-id="674d2-117">These also appear in the producvitivy score pages:</span></span>

- [<span data-ttu-id="674d2-118">Exemples de connexions Exchange touchés par des problèmes de connectivité</span><span class="sxs-lookup"><span data-stu-id="674d2-118">Exchange sampled connections impacted by connectivity issues</span></span>](#exchange-sampled-connections-impacted-by-connectivity-issues)
- [<span data-ttu-id="674d2-119">Exemples de connexions SharePoint touchés par des problèmes de connectivité</span><span class="sxs-lookup"><span data-stu-id="674d2-119">SharePoint sampled connections impacted by connectivity issues</span></span>](#sharepoint-sampled-connections-impacted-by-connectivity-issues)

>[!IMPORTANT]
><span data-ttu-id="674d2-120">Les informations sur le réseau, les recommandations en matière de performances et les évaluations dans le Centre d’administration Microsoft 365 sont actuellement en état de prévisualisation et sont uniquement disponibles pour les clients Microsoft 365 qui ont été inscrits au programme d’aperçu des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="674d2-120">Network insights, performance recommendations and assessments in the Microsoft 365 Admin Center is currently in preview status, and is only available for Microsoft 365 tenants that have been enrolled in the feature preview program.</span></span>

## <a name="backhauled-network-egress"></a><span data-ttu-id="674d2-121">Sortie du réseau backhauled</span><span class="sxs-lookup"><span data-stu-id="674d2-121">Backhauled network egress</span></span>

<span data-ttu-id="674d2-122">Cette information s’affiche si le service d’informations réseau détecte que la distance entre un emplacement utilisateur donné et la sortie réseau est supérieure à 500 miles (800 kilomètres), ce qui indique que le trafic Microsoft 365 est rétrogradé vers un périphérique edge Internet ou un proxy commun.</span><span class="sxs-lookup"><span data-stu-id="674d2-122">This insight will be displayed if the network insights service detects that the distance from a given user location to the network egress is greater than 500 miles (800 kilometers), indicating that Microsoft 365 traffic is being backhauled to a common Internet edge device or proxy.</span></span>

<span data-ttu-id="674d2-123">Cette information est abrégée en « Sortie » dans certains affichages récapitulatifs.</span><span class="sxs-lookup"><span data-stu-id="674d2-123">This insight is abbreviated as "Egress" in some summary views.</span></span>

![Sortie du réseau backhauled](../media/m365-mac-perf/m365-mac-perf-insights-detail-backhauled.png)

### <a name="what-does-this-mean"></a><span data-ttu-id="674d2-125">Scénario</span><span class="sxs-lookup"><span data-stu-id="674d2-125">What does this mean?</span></span>

<span data-ttu-id="674d2-126">Cela indique que la distance entre l’emplacement du bureau et la sortie réseau est de plus de 500 km (800 kilomètres).</span><span class="sxs-lookup"><span data-stu-id="674d2-126">This identifies that the distance between the office location and the network egress is more than 500 miles (800 kilometers).</span></span> <span data-ttu-id="674d2-127">L’emplacement du bureau est identifié par un emplacement d’ordinateur client obscurci et l’emplacement de sortie réseau est identifié à l’aide de l’adresse IP inversée pour les bases de données d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="674d2-127">The office location is identified by an obfuscated client machine location and the network egress location is identified by using reverse IP Address to location databases.</span></span> <span data-ttu-id="674d2-128">L’emplacement du bureau peut être incorrect si les services de localisation Windows sont désactivés sur les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="674d2-128">The office location may be inaccurate if Windows Location Services is disabled on machines.</span></span> <span data-ttu-id="674d2-129">L’emplacement de sortie réseau peut être incorrect si les informations de la base de données d’adresses IP inverses sont inexactes.</span><span class="sxs-lookup"><span data-stu-id="674d2-129">The network egress location may be inaccurate if the reverse IP Address database information is inaccurate.</span></span>

<span data-ttu-id="674d2-130">Ces informations incluent l’emplacement du bureau, le pourcentage estimé du nombre total d’utilisateurs locataires sur l’emplacement, l’emplacement de sortie du réseau actuel, la pertinence de l’emplacement de sortie, la distance entre l’emplacement et le point de sortie actuel, la date à laquelle la condition a été détectée pour la première fois et la date à laquelle la condition a été résolue.</span><span class="sxs-lookup"><span data-stu-id="674d2-130">Details for this insight include the office location, estimated percentage of total tenant user at the location, the current network egress location, relevance of the egress location, the distance between the location and the current egress point, the date the condition was first detected, and the date the condition was resolved.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="674d2-131">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="674d2-131">What should I do?</span></span>

<span data-ttu-id="674d2-132">Pour ce faire, nous vous recommandons d’utiliser une sortie réseau plus proche de l’emplacement du bureau afin que la connectivité puisse être acheminée de manière optimale vers le réseau global de Microsoft et vers la porte d’entrée du service Microsoft 365 la plus proche.</span><span class="sxs-lookup"><span data-stu-id="674d2-132">For this insight, we would recommend network egress closer to the office location so that connectivity can route optimally to Microsoft's global network and to the nearest Microsoft 365 service front door.</span></span> <span data-ttu-id="674d2-133">Une sortie étroite du réseau vers les emplacements de bureau des utilisateurs permet également d’améliorer les performances à l’avenir, car Microsoft étend à la fois les points de présence réseau et les portes avant du service Microsoft 365 à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="674d2-133">Having close network egress to users office locations also allows for improved performance in the future as Microsoft expands both network points of presence and Microsoft 365 service front doors in the future.</span></span>

<span data-ttu-id="674d2-134">Pour plus d’informations sur la résolution de ce problème, voir La sortie des connexions réseau [localement](microsoft-365-network-connectivity-principles.md#egress-network-connections-locally) dans les principes de connectivité réseau [d’Office 365.](microsoft-365-network-connectivity-principles.md)</span><span class="sxs-lookup"><span data-stu-id="674d2-134">For more information about how to resolve this issue, see [Egress network connections locally](microsoft-365-network-connectivity-principles.md#egress-network-connections-locally) in [Office 365 Network Connectivity Principles](microsoft-365-network-connectivity-principles.md).</span></span>

## <a name="network-intermediary-device"></a><span data-ttu-id="674d2-135">Périphérique intermédiaire réseau</span><span class="sxs-lookup"><span data-stu-id="674d2-135">Network intermediary device</span></span>

<span data-ttu-id="674d2-136">Cette information s’affiche si nous avons détecté des appareils entre vos utilisateurs et le réseau de Microsoft qui peuvent avoir un impact sur l’expérience utilisateur d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="674d2-136">This insight will be displayed if we detected devices between your users and Microsoft's network which may impact the Office 365 user experience.</span></span> <span data-ttu-id="674d2-137">Il est recommandé de les contourner pour le trafic réseau Microsoft 365 spécifique destiné aux centres de données Microsoft.</span><span class="sxs-lookup"><span data-stu-id="674d2-137">It is recommended that these be bypassed for specific Microsoft 365 network traffic that is destined for Microsoft datacenters.</span></span> <span data-ttu-id="674d2-138">Cette recommandation est également décrite dans les principes de connectivité réseau [de Microsoft 365](microsoft-365-network-connectivity-principles.md)</span><span class="sxs-lookup"><span data-stu-id="674d2-138">This recommendation is additionally described in [Microsoft 365 Network Connectivity Principles](microsoft-365-network-connectivity-principles.md)</span></span>

### <a name="what-does-this-mean"></a><span data-ttu-id="674d2-139">Scénario</span><span class="sxs-lookup"><span data-stu-id="674d2-139">What does this mean?</span></span>

<span data-ttu-id="674d2-140">Les périphériques intermédiaires réseau tels que les serveurs proxy, les VPN et les périphériques de protection contre la perte de données peuvent affecter les performances et la stabilité des clients Microsoft 365 où le trafic est intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="674d2-140">Network intermediary devices such as proxy servers, VPNs, and data loss prevention devices can affect performance and stability of Microsoft 365 clients where traffic is intermediated.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="674d2-141">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="674d2-141">What should I do?</span></span>

<span data-ttu-id="674d2-142">Configurez le périphérique intermédiaire réseau détecté pour contourner le traitement du trafic réseau Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="674d2-142">Configure the network intermediary device that was detected to bypass processing for Microsoft 365 network traffic.</span></span>

## <a name="better-performance-detected-for-customers-near-you"></a><span data-ttu-id="674d2-143">Meilleures performances détectées pour les clients proches de chez vous</span><span class="sxs-lookup"><span data-stu-id="674d2-143">Better performance detected for customers near you</span></span>

<span data-ttu-id="674d2-144">Cette information s’affiche si le service d’informations réseau détecte qu’un nombre significatif de clients dans votre zone d’information offrent de meilleures performances que les utilisateurs de votre organisation à cet emplacement de bureau.</span><span class="sxs-lookup"><span data-stu-id="674d2-144">This insight will be displayed if the network insights service detects that a significant number of customers in your metro area have better performance than users in your organization at this office location.</span></span>

<span data-ttu-id="674d2-145">Cette information est abrégée en « Homologues » dans certains affichages récapitulatifs.</span><span class="sxs-lookup"><span data-stu-id="674d2-145">This insight is abbreviated as "Peers" in some summary views.</span></span>

![Performances relatives du réseau](../media/m365-mac-perf/m365-mac-perf-insights-detail-cust-near-you.png)

### <a name="what-does-this-mean"></a><span data-ttu-id="674d2-147">Scénario</span><span class="sxs-lookup"><span data-stu-id="674d2-147">What does this mean?</span></span>

<span data-ttu-id="674d2-148">Cette vue d’ensemble examine les performances agrégées des clients Microsoft 365 dans la même ville que cet emplacement de bureau.</span><span class="sxs-lookup"><span data-stu-id="674d2-148">This insight examines the aggregate performance of Microsoft 365 customers in the same city as this office location.</span></span> <span data-ttu-id="674d2-149">Cette information s’affiche si la latence moyenne de vos utilisateurs est supérieure de 10 % à la latence moyenne des locataires voisins.</span><span class="sxs-lookup"><span data-stu-id="674d2-149">This insight is displayed if the average latency of your users is 10% greater than the average latency of neighboring tenants.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="674d2-150">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="674d2-150">What should I do?</span></span>

<span data-ttu-id="674d2-151">Il peut y avoir de nombreuses raisons à cette condition, notamment la latence dans votre réseau d’entreprise ou votre isp isp, les goulots d’étranglement ou les problèmes de conception de l’architecture.</span><span class="sxs-lookup"><span data-stu-id="674d2-151">There could be many reasons for this condition, including latency in your corporate network or ISP, bottlenecks, or architecture design issues.</span></span> <span data-ttu-id="674d2-152">Examinez la latence entre chaque saut dans l’itinéraire entre votre réseau de bureau et la porte d’entrée Microsoft 365 actuelle.</span><span class="sxs-lookup"><span data-stu-id="674d2-152">Examine the latency between each hop in the route between your office network and the current Microsoft 365 front door.</span></span> <span data-ttu-id="674d2-153">Pour plus d’informations, voir Principes de connectivité réseau [Microsoft 365.](microsoft-365-network-connectivity-principles.md)</span><span class="sxs-lookup"><span data-stu-id="674d2-153">For more information, see [Microsoft 365 Network Connectivity Principles](microsoft-365-network-connectivity-principles.md).</span></span>

## <a name="use-of-a-non-optimal-exchange-online-service-front-door"></a><span data-ttu-id="674d2-154">Utilisation d’une porte d’entrée de service Exchange Online non optimale</span><span class="sxs-lookup"><span data-stu-id="674d2-154">Use of a non-optimal Exchange Online service front door</span></span>

<span data-ttu-id="674d2-155">Cette information s’affiche si le service d’informations réseau détecte que les utilisateurs situés à un emplacement spécifique ne se connectent pas à une porte d’entrée de service Exchange Online optimale.</span><span class="sxs-lookup"><span data-stu-id="674d2-155">This insight will be displayed if the network insights service detects that users in a specific location are not connecting to an optimal Exchange Online service front door.</span></span>

<span data-ttu-id="674d2-156">Cette information est abrégée en « Routage » dans certains affichages récapitulatifs.</span><span class="sxs-lookup"><span data-stu-id="674d2-156">This insight is abbreviated as "Routing" in some summary views.</span></span>

![Porte frontale EXO non optimale](../media/m365-mac-perf/m365-mac-perf-insights-detail-front-door-exo.png)

### <a name="what-does-this-mean"></a><span data-ttu-id="674d2-158">Scénario</span><span class="sxs-lookup"><span data-stu-id="674d2-158">What does this mean?</span></span>

<span data-ttu-id="674d2-159">Nous listons les portes d’entrée du service Exchange Online qui conviennent à une utilisation à partir de la ville de l’emplacement du bureau avec de bonnes performances.</span><span class="sxs-lookup"><span data-stu-id="674d2-159">We list Exchange Online service front doors which are suitable for use from the office location city with good performance.</span></span> <span data-ttu-id="674d2-160">Si le test actuel indique l’utilisation d’une porte d’entrée du service Exchange Online qui ne figure pas dans cette liste, nous appelons cette recommandation.</span><span class="sxs-lookup"><span data-stu-id="674d2-160">If the current test shows use of an Exchange Online service front door not on this list, then we call out this recommendation.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="674d2-161">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="674d2-161">What should I do?</span></span>

<span data-ttu-id="674d2-162">L’utilisation d’une porte frontale du service Exchange Online non optimale peut être causée par une rétrograder du réseau avant la sortie du réseau d’entreprise, auquel cas nous vous recommandons une sortie de réseau local et directe.</span><span class="sxs-lookup"><span data-stu-id="674d2-162">Use of a non-optimal Exchange Online service front door could be caused by network backhaul before the corporate network egress in which case we recommend local and direct network egress.</span></span> <span data-ttu-id="674d2-163">Cela peut également être dû à l’utilisation d’un serveur de résolution récursive DNS distant, auquel cas nous vous recommandons d’aligner le serveur de résolution récursive DNS avec la sortie réseau.</span><span class="sxs-lookup"><span data-stu-id="674d2-163">It could also be caused by use of a remote DNS Recursive Resolver server in which case we recommend aligning the DNS Recursive Resolver server with the network egress.</span></span>

## <a name="use-of-a-non-optimal-sharepoint-online-service-front-door"></a><span data-ttu-id="674d2-164">Utilisation d’une porte d’entrée de service SharePoint Online non optimale</span><span class="sxs-lookup"><span data-stu-id="674d2-164">Use of a non-optimal SharePoint Online service front door</span></span>

<span data-ttu-id="674d2-165">Cette information s’affiche si le service d’informations réseau détecte que les utilisateurs d’un emplacement spécifique ne se connectent pas à la porte d’entrée du service SharePoint Online la plus proche.</span><span class="sxs-lookup"><span data-stu-id="674d2-165">This insight will be displayed if the network insights service detects that users in a specific location are not connecting to the closest SharePoint Online service front door.</span></span>

<span data-ttu-id="674d2-166">Cette information est abrégée en « Afd » dans certains affichages récapitulatifs.</span><span class="sxs-lookup"><span data-stu-id="674d2-166">This insight is abbreviated as "Afd" in some summary views.</span></span>

![Porte d’entrée SPO non optimale](../media/m365-mac-perf/m365-mac-perf-insights-detail-front-door-spo.png)

### <a name="what-does-this-mean"></a><span data-ttu-id="674d2-168">Scénario</span><span class="sxs-lookup"><span data-stu-id="674d2-168">What does this mean?</span></span>

<span data-ttu-id="674d2-169">Nous identifions la porte d’entrée du service SharePoint Online à qui le client de test se connecte.</span><span class="sxs-lookup"><span data-stu-id="674d2-169">We identify the SharePoint Online service front door that the test client is connecting to.</span></span> <span data-ttu-id="674d2-170">Ensuite, pour la ville de l’emplacement du bureau, nous comparons cela à la porte d’entrée du service SharePoint Online attendue pour cette ville.</span><span class="sxs-lookup"><span data-stu-id="674d2-170">Then for the office location city we compare that to the expected SharePoint Online service front door for that city.</span></span> <span data-ttu-id="674d2-171">Si ce n’est pas le cas, nous vous en faire la recommandation.</span><span class="sxs-lookup"><span data-stu-id="674d2-171">If it doesn't match, then we make this recommendation.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="674d2-172">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="674d2-172">What should I do?</span></span>

<span data-ttu-id="674d2-173">L’utilisation d’une porte frontale de service SharePoint Online non optimale peut être causée par une rétrograder du réseau avant la sortie du réseau d’entreprise, auquel cas nous recommandons la sortie du réseau local et direct.</span><span class="sxs-lookup"><span data-stu-id="674d2-173">Use of a non-optimal SharePoint Online service front door could be caused by network backhaul before the corporate network egress in which case we recommend local and direct network egress.</span></span> <span data-ttu-id="674d2-174">Cela peut également être dû à l’utilisation d’un serveur de résolution récursive DNS distant, auquel cas nous vous recommandons d’aligner le serveur de résolution récursive DNS avec la sortie réseau.</span><span class="sxs-lookup"><span data-stu-id="674d2-174">It could also be caused by use of a remote DNS Recursive Resolver server in which case we recommend aligning the DNS Recursive Resolver server with the network egress.</span></span>

## <a name="low-download-speed-from-sharepoint-front-door"></a><span data-ttu-id="674d2-175">Vitesse de téléchargement faible à partir de la porte d’entrée SharePoint</span><span class="sxs-lookup"><span data-stu-id="674d2-175">Low download speed from SharePoint front door</span></span>

<span data-ttu-id="674d2-176">Cette information s’affiche si le service d’informations réseau détecte que la bande passante entre l’emplacement du bureau spécifique et SharePoint Online est inférieure à 1 Mbits/s.</span><span class="sxs-lookup"><span data-stu-id="674d2-176">This insight will be displayed if the network insights service detects that bandwidth between the specific office location and SharePoint Online is less than 1 MBps.</span></span>

<span data-ttu-id="674d2-177">Cette information est abrégée « Débit » dans certains affichages récapitulatifs.</span><span class="sxs-lookup"><span data-stu-id="674d2-177">This insight is abbreviated as "Throughput" in some summary views.</span></span>

### <a name="what-does-this-mean"></a><span data-ttu-id="674d2-178">Scénario</span><span class="sxs-lookup"><span data-stu-id="674d2-178">What does this mean?</span></span>

<span data-ttu-id="674d2-179">La vitesse de téléchargement qu’un utilisateur peut obtenir à partir des portes frontales du service SharePoint Online et OneDrive Entreprise est mesurée en mégaoctets par seconde (MBits/s).</span><span class="sxs-lookup"><span data-stu-id="674d2-179">The download speed that a user can get from SharePoint Online and OneDrive for Business service front doors is measured in megabytes per second (MBps).</span></span> <span data-ttu-id="674d2-180">Si cette valeur est inférieure à 1 Mbits/s, nous fournissons cette information.</span><span class="sxs-lookup"><span data-stu-id="674d2-180">If this value is less than 1 MBps then we provide this insight.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="674d2-181">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="674d2-181">What should I do?</span></span>

<span data-ttu-id="674d2-182">Pour améliorer les vitesses de téléchargement, vous devrez peut-être augmenter la bande passante.</span><span class="sxs-lookup"><span data-stu-id="674d2-182">To improve download speeds, bandwidth may need to be increased.</span></span> <span data-ttu-id="674d2-183">Sinon, il peut y avoir une congestion du réseau entre les ordinateurs des utilisateurs au niveau de l’emplacement du bureau et du service SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="674d2-183">Alternatively, there may be network congestion between user machines at the office location and the SharePoint Online service front door.</span></span> <span data-ttu-id="674d2-184">Cette perte est parfois appelée perte congestive et limite la vitesse de téléchargement disponible pour les utilisateurs, même si une bande passante suffisante est disponible.</span><span class="sxs-lookup"><span data-stu-id="674d2-184">This is sometimes called congestive loss and it restricts the download speed available to users even if sufficient bandwidth is available.</span></span>

## <a name="china-user-optimal-network-egress"></a><span data-ttu-id="674d2-185">Sortie réseau optimale de l’utilisateur chinois</span><span class="sxs-lookup"><span data-stu-id="674d2-185">China user optimal network egress</span></span>

<span data-ttu-id="674d2-186">Cette information s’affiche si des utilisateurs de votre organisation en Chine se connectent à votre client Microsoft 365 dans d’autres emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="674d2-186">This insight will be displayed if your organization has users in China connecting to your Microsoft 365 tenant in other geographic locations.</span></span> 

### <a name="what-does-this-mean"></a><span data-ttu-id="674d2-187">Scénario</span><span class="sxs-lookup"><span data-stu-id="674d2-187">What does this mean?</span></span>

<span data-ttu-id="674d2-188">Si votre organisation dispose d’une connectivité WAN privée, nous vous recommandons de configurer un circuit réseau WAN à partir de vos bureaux en Chine qui dispose d’une sortie réseau vers Internet à l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="674d2-188">If your organization has private WAN connectivity, we recommend configuring a network WAN circuit from your office locations in China that has network egress to the Internet in any of the following locations:</span></span>

- <span data-ttu-id="674d2-189">Hong Kong</span><span class="sxs-lookup"><span data-stu-id="674d2-189">Hong Kong</span></span>
- <span data-ttu-id="674d2-190">Japon</span><span class="sxs-lookup"><span data-stu-id="674d2-190">Japan</span></span>
- <span data-ttu-id="674d2-191">Taïwan</span><span class="sxs-lookup"><span data-stu-id="674d2-191">Taiwan</span></span>
- <span data-ttu-id="674d2-192">Corée du Sud</span><span class="sxs-lookup"><span data-stu-id="674d2-192">South Korea</span></span>
- <span data-ttu-id="674d2-193">Singapour</span><span class="sxs-lookup"><span data-stu-id="674d2-193">Singapore</span></span>
- <span data-ttu-id="674d2-194">Malaisie</span><span class="sxs-lookup"><span data-stu-id="674d2-194">Malaysia</span></span>

<span data-ttu-id="674d2-195">Une sortie d’Internet plus éloignée des utilisateurs que ces emplacements réduit les performances, et la sortie en Chine peut entraîner des problèmes de latence et de connectivité élevés en raison d’une congestion croisée.</span><span class="sxs-lookup"><span data-stu-id="674d2-195">Internet egress further away from users than these locations will reduce performance, and egress in China may cause high latency and connectivity issues due to cross-border congestion.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="674d2-196">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="674d2-196">What should I do?</span></span>

<span data-ttu-id="674d2-197">Pour plus d’informations sur la façon d’atténuer les problèmes de performances liés à cette information, consultez l’optimisation des performances globales du client [Microsoft 365](microsoft-365-networking-china.md)pour les utilisateurs chinois.</span><span class="sxs-lookup"><span data-stu-id="674d2-197">For more information about how to mitigate performance issues related to this insight, see [Microsoft 365 global tenant performance optimization for China users](microsoft-365-networking-china.md).</span></span>

## <a name="exchange-sampled-connections-impacted-by-connectivity-issues"></a><span data-ttu-id="674d2-198">Exemples de connexions Exchange touchés par des problèmes de connectivité</span><span class="sxs-lookup"><span data-stu-id="674d2-198">Exchange sampled connections impacted by connectivity issues</span></span>

<span data-ttu-id="674d2-199">Cette information indique quand 50 % ou plus des connexions échantillonées sont impactées.</span><span class="sxs-lookup"><span data-stu-id="674d2-199">This insight will show when 50% or more of the sampled connections are impacted.</span></span> <span data-ttu-id="674d2-200">L’impact est défini par l’évaluation Exchange inférieure à 60 % pour chaque échantillon.</span><span class="sxs-lookup"><span data-stu-id="674d2-200">The impact is defined by the Exchange assessment being below 60% for each sample.</span></span>

### <a name="what-does-this-mean"></a><span data-ttu-id="674d2-201">Scénario</span><span class="sxs-lookup"><span data-stu-id="674d2-201">What does this mean?</span></span>

<span data-ttu-id="674d2-202">Il s’agit d’une indication que la majorité de vos utilisateurs rencontreront probablement des problèmes d’expérience utilisateur avec Outlook qui se connecte à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="674d2-202">It is an indication that the majority of your users are likely to be experiencing user experience issues with Outlook connecting to Exchange Online.</span></span> <span data-ttu-id="674d2-203">Le pourcentage d’échantillons représente probablement le pourcentage d’utilisateurs qui indiquent moins de 60 points.</span><span class="sxs-lookup"><span data-stu-id="674d2-203">The percentage of samples likely represents the percentage of users who show below 60 points.</span></span>  

### <a name="what-should-i-do"></a><span data-ttu-id="674d2-204">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="674d2-204">What should I do?</span></span>

<span data-ttu-id="674d2-205">Activez la visibilité de la connectivité réseau de l’emplacement du bureau si vous ne l’avez pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="674d2-205">Enable office location network connectivity visibility if you have not already done so.</span></span> <span data-ttu-id="674d2-206">Vous souhaitez identifier les bureaux qui sont touchés par une connectivité réseau médiocre qui a un impact sur Exchange et trouver des moyens d’améliorer le périmètre réseau à chaque bureau qui connecte les utilisateurs au réseau de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="674d2-206">You want to identify which offices are impacted by poor network connectivity that is impacting Exchange and find ways to improve the network perimeter at each that connects the users to Microsoft's network.</span></span>

## <a name="sharepoint-sampled-connections-impacted-by-connectivity-issues"></a><span data-ttu-id="674d2-207">Exemples de connexions SharePoint touchés par des problèmes de connectivité</span><span class="sxs-lookup"><span data-stu-id="674d2-207">SharePoint sampled connections impacted by connectivity issues</span></span>

<span data-ttu-id="674d2-208">Cette information indique quand 50 % ou plus des connexions échantillonées sont impactées.</span><span class="sxs-lookup"><span data-stu-id="674d2-208">This insight will show when 50% or more of the sampled connections are impacted.</span></span> <span data-ttu-id="674d2-209">L’impact est défini par l’évaluation SharePoint inférieure à 40 % pour chaque échantillon.</span><span class="sxs-lookup"><span data-stu-id="674d2-209">The impact is defined by the SharePoint assessment being below 40% for each sample.</span></span>

### <a name="what-does-this-mean"></a><span data-ttu-id="674d2-210">Scénario</span><span class="sxs-lookup"><span data-stu-id="674d2-210">What does this mean?</span></span>

<span data-ttu-id="674d2-211">Il s’agit d’une indication que la majorité de vos utilisateurs rencontreront probablement des problèmes d’expérience utilisateur avec SharePoint et OneDrive.</span><span class="sxs-lookup"><span data-stu-id="674d2-211">It is an indication that the majority of your users are likely to be experiencing user experience issues with SharePoint and OneDrive.</span></span> <span data-ttu-id="674d2-212">Le pourcentage d’échantillons représente probablement le pourcentage d’utilisateurs qui indiquent moins de 40 points.</span><span class="sxs-lookup"><span data-stu-id="674d2-212">The percentage of samples likely represents the percentage of users who show below 40 points.</span></span>  

### <a name="what-should-i-do"></a><span data-ttu-id="674d2-213">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="674d2-213">What should I do?</span></span>

<span data-ttu-id="674d2-214">Activez la visibilité de la connectivité réseau de l’emplacement du bureau si vous ne l’avez pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="674d2-214">Enable office location network connectivity visibility if you have not already done so.</span></span> <span data-ttu-id="674d2-215">Vous souhaitez identifier les bureaux qui sont touchés par une connectivité réseau médiocre qui a un impact sur SharePoint et trouver des moyens d’améliorer le périmètre réseau à chaque bureau qui connecte les utilisateurs au réseau de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="674d2-215">You want to identify which offices are impacted by poor network connectivity that is impacting SharePoint and find ways to improve the network perimeter at each that connects the users to Microsoft's network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="674d2-216">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="674d2-216">Related topics</span></span>

[<span data-ttu-id="674d2-217">Connectivité réseau dans le Centre d’administration Microsoft 365 (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="674d2-217">Network connectivity in the Microsoft 365 Admin Center (preview)</span></span>](office-365-network-mac-perf-overview.md)

[<span data-ttu-id="674d2-218">Évaluation du réseau Microsoft 365 (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="674d2-218">Microsoft 365 network assessment (preview)</span></span>](office-365-network-mac-perf-score.md)

[<span data-ttu-id="674d2-219">Outil de test de connectivité réseau Microsoft 365 (aperçu)</span><span class="sxs-lookup"><span data-stu-id="674d2-219">Microsoft 365 network connectivity test tool (preview)</span></span>](office-365-network-mac-perf-onboarding-tool.md)

[<span data-ttu-id="674d2-220">Services d’emplacement de connectivité réseau Microsoft 365 (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="674d2-220">Microsoft 365 Network Connectivity Location Services (preview)</span></span>](office-365-network-mac-location-services.md)
