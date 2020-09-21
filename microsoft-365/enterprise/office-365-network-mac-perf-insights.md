---
title: Informations sur le réseau Microsoft 365 (aperçu)
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 09/17/2020
audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
description: Informations sur le réseau Microsoft 365 (aperçu)
ms.openlocfilehash: 682c888fefb9bec9725e470d62019c857fc2de07
ms.sourcegitcommit: cd11588b47904c7d2ae899a9f5280f93d3850171
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2020
ms.locfileid: "48171337"
---
# <a name="microsoft-365-network-insights-preview"></a><span data-ttu-id="179d0-103">Informations sur le réseau Microsoft 365 (aperçu)</span><span class="sxs-lookup"><span data-stu-id="179d0-103">Microsoft 365 Network Insights (preview)</span></span>

<span data-ttu-id="179d0-104">**Network Insights** est une mesure des performances collectées auprès de votre client Microsoft 365 et disponible uniquement par les utilisateurs administratifs de votre client.</span><span class="sxs-lookup"><span data-stu-id="179d0-104">**Network insights** are performance metrics collected from your Microsoft 365 tenant, and available to view only by administrative users in your tenant.</span></span> <span data-ttu-id="179d0-105">Les informations s’affichent dans le centre d’administration Microsoft 365 à l’adresse <https://portal.microsoft.com/adminportal/home#/networkperformance> .</span><span class="sxs-lookup"><span data-stu-id="179d0-105">Insights are displayed in the Microsoft 365 Admin Center at <https://portal.microsoft.com/adminportal/home#/networkperformance>.</span></span>

<span data-ttu-id="179d0-106">Les informations sont destinées à vous aider à concevoir des périmètres réseau pour vos emplacements de bureau.</span><span class="sxs-lookup"><span data-stu-id="179d0-106">Insights are intended to help in designing network perimeters for your office locations.</span></span> <span data-ttu-id="179d0-107">Chaque vue fournit des informations détaillées sur les caractéristiques de performances d’un problème commun spécifique pour chaque emplacement géographique où les utilisateurs accèdent à votre client.</span><span class="sxs-lookup"><span data-stu-id="179d0-107">Each insight provides live details about the performance characteristics for a specific common issue for each geographic location where users are accessing your tenant.</span></span>

<span data-ttu-id="179d0-108">Six informations spécifiques sur le réseau peuvent être affichées pour chaque emplacement de bureau :</span><span class="sxs-lookup"><span data-stu-id="179d0-108">There are six specific network insights that may be shown for each office location:</span></span>

- [<span data-ttu-id="179d0-109">Sortie réseau retractée</span><span class="sxs-lookup"><span data-stu-id="179d0-109">Backhauled network egress</span></span>](#backhauled-network-egress)
- [<span data-ttu-id="179d0-110">Meilleures performances détectées pour les clients proches de vous</span><span class="sxs-lookup"><span data-stu-id="179d0-110">Better performance detected for customers near you</span></span>](#better-performance-detected-for-customers-near-you)
- [<span data-ttu-id="179d0-111">Utilisation d’un service frontal Exchange Online non optimal</span><span class="sxs-lookup"><span data-stu-id="179d0-111">Use of a non-optimal Exchange Online service front door</span></span>](#use-of-a-non-optimal-exchange-online-service-front-door)
- [<span data-ttu-id="179d0-112">Utilisation d’un service SharePoint Online non optimal</span><span class="sxs-lookup"><span data-stu-id="179d0-112">Use of a non-optimal SharePoint Online service front door</span></span>](#use-of-a-non-optimal-sharepoint-online-service-front-door)
- [<span data-ttu-id="179d0-113">Vitesse de téléchargement faible à partir de la porte d’entrée SharePoint</span><span class="sxs-lookup"><span data-stu-id="179d0-113">Low download speed from SharePoint front door</span></span>](#low-download-speed-from-sharepoint-front-door)
- [<span data-ttu-id="179d0-114">Sortie du réseau chinois utilisateur optimal</span><span class="sxs-lookup"><span data-stu-id="179d0-114">China user optimal network egress</span></span>](#china-user-optimal-network-egress)

<span data-ttu-id="179d0-115">Il existe deux idées de réseau au niveau du client qui peuvent être affichées pour le client.</span><span class="sxs-lookup"><span data-stu-id="179d0-115">There are two tenant level network insights that may be shown for the tenant.</span></span> <span data-ttu-id="179d0-116">Elles apparaissent également dans les pages de score producvitivy :</span><span class="sxs-lookup"><span data-stu-id="179d0-116">These also appear in the producvitivy score pages:</span></span>

- [<span data-ttu-id="179d0-117">Connexions Exchange échantillonnées affectées par les problèmes de connectivité</span><span class="sxs-lookup"><span data-stu-id="179d0-117">Exchange sampled connections impacted by connectivity issues</span></span>](#exchange-sampled-connections-impacted-by-connectivity-issues)
- [<span data-ttu-id="179d0-118">Connexions SharePoint échantillonnées affectées par les problèmes de connectivité</span><span class="sxs-lookup"><span data-stu-id="179d0-118">SharePoint sampled connections impacted by connectivity issues</span></span>](#sharepoint-sampled-connections-impacted-by-connectivity-issues)

>[!IMPORTANT]
><span data-ttu-id="179d0-119">Les informations sur le réseau, les recommandations en matière de performances et les évaluations dans le centre d’administration 365 de Microsoft sont actuellement en état d’aperçu et sont uniquement disponibles pour les locataires Microsoft 365 qui ont été apportées dans le programme d’aperçu des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="179d0-119">Network insights, performance recommendations and assessments in the Microsoft 365 Admin Center is currently in preview status, and is only available for Microsoft 365 tenants that have been enrolled in the feature preview program.</span></span>

## <a name="backhauled-network-egress"></a><span data-ttu-id="179d0-120">Sortie réseau retractée</span><span class="sxs-lookup"><span data-stu-id="179d0-120">Backhauled network egress</span></span>

<span data-ttu-id="179d0-121">Cette vue s’affiche si le service réseau Insights détecte que la distance entre un emplacement utilisateur donné et la sortie réseau est supérieure à 500 kilomètres (800 kilomètres), ce qui indique que le trafic Microsoft 365 est replacé vers un périphérique ou un proxy Internet Edge commun.</span><span class="sxs-lookup"><span data-stu-id="179d0-121">This insight will be displayed if the network insights service detects that the distance from a given user location to the network egress is greater than 500 miles (800 kilometers), indicating that Microsoft 365 traffic is being backhauled to a common Internet edge device or proxy.</span></span>

<span data-ttu-id="179d0-122">Cette vue est abrégée en « sortie » dans certains affichages de résumés.</span><span class="sxs-lookup"><span data-stu-id="179d0-122">This insight is abbreviated as "Egress" in some summary views.</span></span>

![Sortie réseau retractée](../media/m365-mac-perf/m365-mac-perf-insights-detail-backhauled.png)

### <a name="what-does-this-mean"></a><span data-ttu-id="179d0-124">Scénario</span><span class="sxs-lookup"><span data-stu-id="179d0-124">What does this mean?</span></span>

<span data-ttu-id="179d0-125">Cela indique que la distance entre l’emplacement du bureau et la sortie du réseau est supérieure à 500 kilomètres (800 kilomètres).</span><span class="sxs-lookup"><span data-stu-id="179d0-125">This identifies that the distance between the office location and the network egress is more than 500 miles (800 kilometers).</span></span> <span data-ttu-id="179d0-126">L’emplacement du Bureau est identifié par un emplacement de l’ordinateur client masqué et l’emplacement de sortie du réseau est identifié à l’aide de l’adresse IP inverse pour les bases de données d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="179d0-126">The office location is identified by an obfuscated client machine location and the network egress location is identified by using reverse IP Address to location databases.</span></span> <span data-ttu-id="179d0-127">L’emplacement du Bureau peut être inexact si les services d’emplacement Windows sont désactivés sur les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="179d0-127">The office location may be inaccurate if Windows Location Services is disabled on machines.</span></span> <span data-ttu-id="179d0-128">L’emplacement de sortie réseau peut être inexact si les informations de la base de données d’adresses IP inversées sont inexactes.</span><span class="sxs-lookup"><span data-stu-id="179d0-128">The network egress location may be inaccurate if the reverse IP Address database information is inaccurate.</span></span>

<span data-ttu-id="179d0-129">Les détails de cette analyse incluent l’emplacement du bureau, le pourcentage estimé du nombre total d’utilisateurs clients à l’emplacement, l’emplacement de sortie du réseau actuel, la pertinence de l’emplacement de sortie, la distance entre l’emplacement et le point de sortie actuel, la date du premier détection de la condition et la date à laquelle la condition a été résolue.</span><span class="sxs-lookup"><span data-stu-id="179d0-129">Details for this insight include the office location, estimated percentage of total tenant user at the location, the current network egress location, relevance of the egress location, the distance between the location and the current egress point, the date the condition was first detected, and the date the condition was resolved.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="179d0-130">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="179d0-130">What should I do?</span></span>

<span data-ttu-id="179d0-131">Pour cette vue d’ensemble, nous recommandons un accès réseau plus proche de l’emplacement du Bureau de sorte que la connectivité puisse acheminer les performances de façon optimale vers le réseau mondial de Microsoft et vers le service frontal Microsoft 365 service le plus proche.</span><span class="sxs-lookup"><span data-stu-id="179d0-131">For this insight, we would recommend network egress closer to the office location so that connectivity can route optimally to Microsoft's global network and to the nearest Microsoft 365 service front door.</span></span> <span data-ttu-id="179d0-132">Une sortie étroite du réseau vers les bureaux des utilisateurs permet également d’améliorer les performances à l’avenir à mesure que Microsoft étend à la fois les points de présence réseau et les portes frontales du service Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="179d0-132">Having close network egress to users office locations also allows for improved performance in the future as Microsoft expands both network points of presence and Microsoft 365 service front doors in the future.</span></span>

<span data-ttu-id="179d0-133">Pour plus d’informations sur la façon de résoudre ce problème, reportez-vous à la rubrique [sortie locale des connexions réseau](microsoft-365-network-connectivity-principles.md#egress-network-connections-locally) dans [Office 365 principes de connectivité réseau](microsoft-365-network-connectivity-principles.md).</span><span class="sxs-lookup"><span data-stu-id="179d0-133">For more information about how to resolve this issue, see [Egress network connections locally](microsoft-365-network-connectivity-principles.md#egress-network-connections-locally) in [Office 365 Network Connectivity Principles](microsoft-365-network-connectivity-principles.md).</span></span>

## <a name="better-performance-detected-for-customers-near-you"></a><span data-ttu-id="179d0-134">Meilleures performances détectées pour les clients proches de vous</span><span class="sxs-lookup"><span data-stu-id="179d0-134">Better performance detected for customers near you</span></span>

<span data-ttu-id="179d0-135">Cette vue s’affiche si le service réseau Insights détecte qu’un nombre important de clients dans votre zone de métro offre de meilleures performances que les utilisateurs de votre organisation à cet emplacement de bureau.</span><span class="sxs-lookup"><span data-stu-id="179d0-135">This insight will be displayed if the network insights service detects that a significant number of customers in your metro area have better performance than users in your organization at this office location.</span></span>

<span data-ttu-id="179d0-136">Cette vue est abrégée en « pairs » dans certains affichages de résumés.</span><span class="sxs-lookup"><span data-stu-id="179d0-136">This insight is abbreviated as "Peers" in some summary views.</span></span>

![Performances réseau relatives](../media/m365-mac-perf/m365-mac-perf-insights-detail-cust-near-you.png)

### <a name="what-does-this-mean"></a><span data-ttu-id="179d0-138">Scénario</span><span class="sxs-lookup"><span data-stu-id="179d0-138">What does this mean?</span></span>

<span data-ttu-id="179d0-139">Cette vue d’ensemble examine les performances totales des clients Microsoft 365 dans la même ville que cet emplacement de bureau.</span><span class="sxs-lookup"><span data-stu-id="179d0-139">This insight examines the aggregate performance of Microsoft 365 customers in the same city as this office location.</span></span> <span data-ttu-id="179d0-140">Cette vue s’affiche si la latence moyenne de vos utilisateurs est supérieure de 10% à la latence moyenne des clients voisins.</span><span class="sxs-lookup"><span data-stu-id="179d0-140">This insight is displayed if the average latency of your users is 10% greater than the average latency of neighboring tenants.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="179d0-141">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="179d0-141">What should I do?</span></span>

<span data-ttu-id="179d0-142">Il peut y avoir plusieurs raisons à cette condition, notamment la latence de votre réseau d’entreprise ou de votre fournisseur de services Internet, des goulots d’étranglement ou des problèmes de conception de l’architecture.</span><span class="sxs-lookup"><span data-stu-id="179d0-142">There could be many reasons for this condition, including latency in your corporate network or ISP, bottlenecks, or architecture design issues.</span></span> <span data-ttu-id="179d0-143">Examinez la latence entre chaque tronçon de l’itinéraire entre votre réseau Office et le porte-avant Microsoft 365 actuel.</span><span class="sxs-lookup"><span data-stu-id="179d0-143">Examine the latency between each hop in the route between your office network and the current Microsoft 365 front door.</span></span> <span data-ttu-id="179d0-144">Pour plus d’informations, consultez la rubrique [Office 365 Network Connectivity principes](microsoft-365-network-connectivity-principles.md).</span><span class="sxs-lookup"><span data-stu-id="179d0-144">For more information, see [Office 365 Network Connectivity Principles](microsoft-365-network-connectivity-principles.md).</span></span>

## <a name="use-of-a-non-optimal-exchange-online-service-front-door"></a><span data-ttu-id="179d0-145">Utilisation d’un service frontal Exchange Online non optimal</span><span class="sxs-lookup"><span data-stu-id="179d0-145">Use of a non-optimal Exchange Online service front door</span></span>

<span data-ttu-id="179d0-146">Cette vue s’affiche si le service réseau Insights détecte que les utilisateurs situés à un emplacement spécifique ne se connectent pas à un service frontal Exchange Online optimal.</span><span class="sxs-lookup"><span data-stu-id="179d0-146">This insight will be displayed if the network insights service detects that users in a specific location are not connecting to an optimal Exchange Online service front door.</span></span>

<span data-ttu-id="179d0-147">Cette vue est abrégée en « routage » dans certains affichages de résumés.</span><span class="sxs-lookup"><span data-stu-id="179d0-147">This insight is abbreviated as "Routing" in some summary views.</span></span>

![Portes frontales EXO non optimales](../media/m365-mac-perf/m365-mac-perf-insights-detail-front-door-exo.png)

### <a name="what-does-this-mean"></a><span data-ttu-id="179d0-149">Scénario</span><span class="sxs-lookup"><span data-stu-id="179d0-149">What does this mean?</span></span>

<span data-ttu-id="179d0-150">Nous répertorions les portes frontales du service Exchange Online qui peuvent être utilisées à partir de la ville de l’emplacement du bureau avec de bonnes performances.</span><span class="sxs-lookup"><span data-stu-id="179d0-150">We list Exchange Online service front doors which are suitable for use from the office location city with good performance.</span></span> <span data-ttu-id="179d0-151">Si le test actuel indique l’utilisation d’un service frontal Exchange Online qui ne figurent pas sur cette liste, nous appelons cette recommandation.</span><span class="sxs-lookup"><span data-stu-id="179d0-151">If the current test shows use of an Exchange Online service front door not on this list, then we call out this recommendation.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="179d0-152">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="179d0-152">What should I do?</span></span>

<span data-ttu-id="179d0-153">L’utilisation d’une trappe frontal non optimale d’un service Exchange Online pourrait être causée par le système de test réseau avant la sortie du réseau d’entreprise, auquel cas nous vous recommandons de sortir du réseau local et direct.</span><span class="sxs-lookup"><span data-stu-id="179d0-153">Use of a non-optimal Exchange Online service front door could be caused by network backhaul before the corporate network egress in which case we recommend local and direct network egress.</span></span> <span data-ttu-id="179d0-154">Il peut également être dû à l’utilisation d’un serveur de résolution récursive DNS à distance dans ce cas, nous vous recommandons d’aligner le serveur de résolution récursive DNS avec la sortie réseau.</span><span class="sxs-lookup"><span data-stu-id="179d0-154">It could also be caused by use of a remote DNS Recursive Resolver server in which case we recommend aligning the DNS Recursive Resolver server with the network egress.</span></span>

## <a name="use-of-a-non-optimal-sharepoint-online-service-front-door"></a><span data-ttu-id="179d0-155">Utilisation d’un service SharePoint Online non optimal</span><span class="sxs-lookup"><span data-stu-id="179d0-155">Use of a non-optimal SharePoint Online service front door</span></span>

<span data-ttu-id="179d0-156">Cette vue s’affiche si le service réseau Insights détecte que les utilisateurs situés à un emplacement spécifique ne se connectent pas au porte-tout du service SharePoint Online le plus proche.</span><span class="sxs-lookup"><span data-stu-id="179d0-156">This insight will be displayed if the network insights service detects that users in a specific location are not connecting to the closest SharePoint Online service front door.</span></span>

<span data-ttu-id="179d0-157">Cette vue est abrégée sous la forme « AFD » dans certains affichages de résumés.</span><span class="sxs-lookup"><span data-stu-id="179d0-157">This insight is abbreviated as "Afd" in some summary views.</span></span>

![Portes frontales SPO non optimales](../media/m365-mac-perf/m365-mac-perf-insights-detail-front-door-spo.png)

### <a name="what-does-this-mean"></a><span data-ttu-id="179d0-159">Scénario</span><span class="sxs-lookup"><span data-stu-id="179d0-159">What does this mean?</span></span>

<span data-ttu-id="179d0-160">Nous allons identifier la porte d’écran du service SharePoint Online à laquelle le client de test se connecte.</span><span class="sxs-lookup"><span data-stu-id="179d0-160">We identify the SharePoint Online service front door that the test client is connecting to.</span></span> <span data-ttu-id="179d0-161">Ensuite, pour la ville de l’emplacement du bureau, nous comparons cette ville avec le service SharePoint Online attendu pour cette ville.</span><span class="sxs-lookup"><span data-stu-id="179d0-161">Then for the office location city we compare that to the expected SharePoint Online service front door for that city.</span></span> <span data-ttu-id="179d0-162">S’il ne correspond pas, nous en faisons la recommandation.</span><span class="sxs-lookup"><span data-stu-id="179d0-162">If it doesn't match, then we make this recommendation.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="179d0-163">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="179d0-163">What should I do?</span></span>

<span data-ttu-id="179d0-164">L’utilisation d’une trappe frontal non optimale de service SharePoint Online pourrait être causée par le système de test réseau avant la sortie du réseau d’entreprise, auquel cas nous vous recommandons de sortir du réseau local et direct.</span><span class="sxs-lookup"><span data-stu-id="179d0-164">Use of a non-optimal SharePoint Online service front door could be caused by network backhaul before the corporate network egress in which case we recommend local and direct network egress.</span></span> <span data-ttu-id="179d0-165">Il peut également être dû à l’utilisation d’un serveur de résolution récursive DNS à distance dans ce cas, nous vous recommandons d’aligner le serveur de résolution récursive DNS avec la sortie réseau.</span><span class="sxs-lookup"><span data-stu-id="179d0-165">It could also be caused by use of a remote DNS Recursive Resolver server in which case we recommend aligning the DNS Recursive Resolver server with the network egress.</span></span>

## <a name="low-download-speed-from-sharepoint-front-door"></a><span data-ttu-id="179d0-166">Vitesse de téléchargement faible à partir de la porte d’entrée SharePoint</span><span class="sxs-lookup"><span data-stu-id="179d0-166">Low download speed from SharePoint front door</span></span>

<span data-ttu-id="179d0-167">Cette vue s’affiche si le service réseau Insights détecte que la bande passante entre l’emplacement de bureau spécifique et SharePoint Online est inférieure à 1 MBps.</span><span class="sxs-lookup"><span data-stu-id="179d0-167">This insight will be displayed if the network insights service detects that bandwidth between the specific office location and SharePoint Online is less than 1 MBps.</span></span>

<span data-ttu-id="179d0-168">Cette vue est abrégée en « débit » dans certains affichages de résumés.</span><span class="sxs-lookup"><span data-stu-id="179d0-168">This insight is abbreviated as "Throughput" in some summary views.</span></span>

### <a name="what-does-this-mean"></a><span data-ttu-id="179d0-169">Scénario</span><span class="sxs-lookup"><span data-stu-id="179d0-169">What does this mean?</span></span>

<span data-ttu-id="179d0-170">La vitesse de téléchargement qu’un utilisateur peut obtenir à partir de SharePoint Online et des portes frontales du service OneDrive entreprise est exprimée en mégaoctets par seconde (Mbits/s).</span><span class="sxs-lookup"><span data-stu-id="179d0-170">The download speed that a user can get from SharePoint Online and OneDrive for Business service front doors is measured in megabytes per second (MBps).</span></span> <span data-ttu-id="179d0-171">Si cette valeur est inférieure à 1 MBps, nous fournissons cette vue.</span><span class="sxs-lookup"><span data-stu-id="179d0-171">If this value is less than 1 MBps then we provide this insight.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="179d0-172">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="179d0-172">What should I do?</span></span>

<span data-ttu-id="179d0-173">Pour améliorer la vitesse de téléchargement, vous devrez peut-être augmenter la bande passante.</span><span class="sxs-lookup"><span data-stu-id="179d0-173">To improve download speeds, bandwidth may need to be increased.</span></span> <span data-ttu-id="179d0-174">Par ailleurs, il peut y avoir une congestion réseau entre les ordinateurs des utilisateurs à l’emplacement du bureau et le capot frontal du service SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="179d0-174">Alternatively, there may be network congestion between user machines at the office location and the SharePoint Online service front door.</span></span> <span data-ttu-id="179d0-175">Cette opération est parfois appelée perte de congestion et limite la vitesse de téléchargement disponible aux utilisateurs, même si la bande passante disponible est suffisante.</span><span class="sxs-lookup"><span data-stu-id="179d0-175">This is sometimes called congestive loss and it restricts the download speed available to users even if sufficient bandwidth is available.</span></span>

## <a name="china-user-optimal-network-egress"></a><span data-ttu-id="179d0-176">Sortie du réseau chinois utilisateur optimal</span><span class="sxs-lookup"><span data-stu-id="179d0-176">China user optimal network egress</span></span>

<span data-ttu-id="179d0-177">Cette vue s’affiche si votre organisation a des utilisateurs en Chine se connectent à votre client Microsoft 365 dans d’autres emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="179d0-177">This insight will be displayed if your organization has users in China connecting to your Microsoft 365 tenant in other geographic locations.</span></span> 

### <a name="what-does-this-mean"></a><span data-ttu-id="179d0-178">Scénario</span><span class="sxs-lookup"><span data-stu-id="179d0-178">What does this mean?</span></span>

<span data-ttu-id="179d0-179">Si votre organisation possède une connectivité WAN privée, nous vous recommandons de configurer un circuit WAN réseau à partir de vos emplacements de bureau en Chine qui dispose de la sortie réseau vers Internet dans l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="179d0-179">If your organization has private WAN connectivity, we recommend configuring a network WAN circuit from your office locations in China that has network egress to the Internet in any of the following locations:</span></span>

- <span data-ttu-id="179d0-180">Hong Kong (R.A.S.)</span><span class="sxs-lookup"><span data-stu-id="179d0-180">Hong Kong</span></span>
- <span data-ttu-id="179d0-181">Japon</span><span class="sxs-lookup"><span data-stu-id="179d0-181">Japan</span></span>
- <span data-ttu-id="179d0-182">Taïwan</span><span class="sxs-lookup"><span data-stu-id="179d0-182">Taiwan</span></span>
- <span data-ttu-id="179d0-183">Corée du Sud</span><span class="sxs-lookup"><span data-stu-id="179d0-183">South Korea</span></span>
- <span data-ttu-id="179d0-184">Singapour</span><span class="sxs-lookup"><span data-stu-id="179d0-184">Singapore</span></span>
- <span data-ttu-id="179d0-185">Malaisie</span><span class="sxs-lookup"><span data-stu-id="179d0-185">Malaysia</span></span>

<span data-ttu-id="179d0-186">Une sortie Internet plus éloignée des utilisateurs que ces emplacements réduira les performances, et la sortie en Chine peut entraîner des problèmes de latence et de connectivité élevés en raison d’une congestion transfrontalière.</span><span class="sxs-lookup"><span data-stu-id="179d0-186">Internet egress further away from users than these locations will reduce performance, and egress in China may cause high latency and connectivity issues due to cross-border congestion.</span></span>

### <a name="what-should-i-do"></a><span data-ttu-id="179d0-187">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="179d0-187">What should I do?</span></span>

<span data-ttu-id="179d0-188">Pour plus d’informations sur la façon d’atténuer les problèmes de performances liés à cette vue, consultez la rubrique [Office 365 global client Optimization for China Users](microsoft-365-networking-china.md).</span><span class="sxs-lookup"><span data-stu-id="179d0-188">For more information about how to mitigate performance issues related to this insight, see [Office 365 global tenant performance optimization for China users](microsoft-365-networking-china.md).</span></span>

## <a name="exchange-sampled-connections-impacted-by-connectivity-issues"></a><span data-ttu-id="179d0-189">Connexions Exchange échantillonnées affectées par les problèmes de connectivité</span><span class="sxs-lookup"><span data-stu-id="179d0-189">Exchange sampled connections impacted by connectivity issues</span></span>

<span data-ttu-id="179d0-190">Cette vue indique quand 50% ou plus des connexions échantillonnées sont concernés.</span><span class="sxs-lookup"><span data-stu-id="179d0-190">This insight will show when 50% or more of the sampled connections are impacted.</span></span> <span data-ttu-id="179d0-191">L’impact est défini par l’évaluation Exchange en dessous de 60% pour chaque échantillon.</span><span class="sxs-lookup"><span data-stu-id="179d0-191">The impact is defined by the Exchange assessment being below 60% for each sample.</span></span>

### <a name="what-does-this-mean"></a><span data-ttu-id="179d0-192">Scénario</span><span class="sxs-lookup"><span data-stu-id="179d0-192">What does this mean?</span></span>

<span data-ttu-id="179d0-193">Cela indique que la majorité de vos utilisateurs sont susceptibles de rencontrer des problèmes d’expérience utilisateur avec Outlook en se connectant à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="179d0-193">It is an indication that the majority of your users are likely to be experiencing user experience issues with Outlook connecting to Exchange Online.</span></span> <span data-ttu-id="179d0-194">Le pourcentage d’échantillons représente probablement le pourcentage d’utilisateurs qui affichent au-dessous de 60 points.</span><span class="sxs-lookup"><span data-stu-id="179d0-194">The percentage of samples likely represents the percentage of users who show below 60 points.</span></span>  

### <a name="what-should-i-do"></a><span data-ttu-id="179d0-195">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="179d0-195">What should I do?</span></span>

<span data-ttu-id="179d0-196">Activer la visibilité de la connectivité réseau de l’emplacement Office si vous ne l’avez pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="179d0-196">Enable office location network connectivity visibility if you have not already done so.</span></span> <span data-ttu-id="179d0-197">Vous voulez identifier les bureaux concernés par une faible connectivité réseau qui a un impact sur Exchange et trouver des moyens d’améliorer le périmètre réseau pour chacun d’eux qui connecte les utilisateurs au réseau de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="179d0-197">You want to identify which offices are impacted by poor network connectivity that is impacting Exchange and find ways to improve the network perimeter at each that connects the users to Microsoft's network.</span></span>

## <a name="sharepoint-sampled-connections-impacted-by-connectivity-issues"></a><span data-ttu-id="179d0-198">Connexions SharePoint échantillonnées affectées par les problèmes de connectivité</span><span class="sxs-lookup"><span data-stu-id="179d0-198">SharePoint sampled connections impacted by connectivity issues</span></span>

<span data-ttu-id="179d0-199">Cette vue indique quand 50% ou plus des connexions échantillonnées sont concernés.</span><span class="sxs-lookup"><span data-stu-id="179d0-199">This insight will show when 50% or more of the sampled connections are impacted.</span></span> <span data-ttu-id="179d0-200">L’évaluation de SharePoint est définie par l’évaluation de SharePoint en dessous de 40% pour chaque échantillon.</span><span class="sxs-lookup"><span data-stu-id="179d0-200">The impact is defined by the SharePoint assessment being below 40% for each sample.</span></span>

### <a name="what-does-this-mean"></a><span data-ttu-id="179d0-201">Scénario</span><span class="sxs-lookup"><span data-stu-id="179d0-201">What does this mean?</span></span>

<span data-ttu-id="179d0-202">Cela indique que la majorité de vos utilisateurs sont susceptibles de rencontrer des problèmes d’expérience utilisateur avec SharePoint et OneDrive.</span><span class="sxs-lookup"><span data-stu-id="179d0-202">It is an indication that the majority of your users are likely to be experiencing user experience issues with SharePoint and OneDrive.</span></span> <span data-ttu-id="179d0-203">Le pourcentage d’échantillons représente probablement le pourcentage d’utilisateurs qui affichent au-dessous de 40 points.</span><span class="sxs-lookup"><span data-stu-id="179d0-203">The percentage of samples likely represents the percentage of users who show below 40 points.</span></span>  

### <a name="what-should-i-do"></a><span data-ttu-id="179d0-204">Que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="179d0-204">What should I do?</span></span>

<span data-ttu-id="179d0-205">Activer la visibilité de la connectivité réseau de l’emplacement Office si vous ne l’avez pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="179d0-205">Enable office location network connectivity visibility if you have not already done so.</span></span> <span data-ttu-id="179d0-206">Vous voulez identifier les bureaux concernés par une faible connectivité réseau qui a un impact sur SharePoint et trouver des moyens d’améliorer le périmètre réseau pour chacun d’eux qui connecte les utilisateurs au réseau de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="179d0-206">You want to identify which offices are impacted by poor network connectivity that is impacting SharePoint and find ways to improve the network perimeter at each that connects the users to Microsoft's network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="179d0-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="179d0-207">Related topics</span></span>

[<span data-ttu-id="179d0-208">Connectivité réseau dans le centre d’administration Microsoft 365 (version d’évaluation)</span><span class="sxs-lookup"><span data-stu-id="179d0-208">Network connectivity in the Microsoft 365 Admin Center (preview)</span></span>](office-365-network-mac-perf-overview.md)

[<span data-ttu-id="179d0-209">Microsoft 365 Network Assessment (aperçu)</span><span class="sxs-lookup"><span data-stu-id="179d0-209">Microsoft 365 network assessment (preview)</span></span>](office-365-network-mac-perf-score.md)

[<span data-ttu-id="179d0-210">Outil de test de connectivité réseau Microsoft 365 (aperçu)</span><span class="sxs-lookup"><span data-stu-id="179d0-210">Microsoft 365 network connectivity test tool (preview)</span></span>](office-365-network-mac-perf-onboarding-tool.md)

[<span data-ttu-id="179d0-211">Services d’emplacement de connectivité réseau Microsoft 365 (aperçu)</span><span class="sxs-lookup"><span data-stu-id="179d0-211">Microsoft 365 Network Connectivity Location Services (preview)</span></span>](office-365-network-mac-location-services.md)
