---
title: Introduction à l’optimisation des performances pour SharePoint Online
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 6/22/2018
audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- SPO_Content
f1.keywords:
- CSH
ms.custom: Adm_O365
search.appverid: SPO160
ms.assetid: 81c4be5f-327e-435d-a568-526d68cffef0
description: Cet article explique les aspects spécifiques à prendre en compte lors de la conception de pages pour de meilleures performances dans SharePoint Online.
ms.openlocfilehash: d3a9dedbd5812774b81494af0f8defa5568f7dac
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690117"
---
# <a name="introduction-to-performance-tuning-for-sharepoint-online"></a><span data-ttu-id="1a8da-103">Introduction à l’optimisation des performances pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a8da-103">Introduction to performance tuning for SharePoint Online</span></span>

<span data-ttu-id="1a8da-104">Cet article explique les aspects spécifiques à prendre en compte lors de la conception de pages pour de meilleures performances dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="1a8da-104">This article explains what specific aspects you need to consider when designing pages for best performance in SharePoint Online.</span></span>
     
## <a name="sharepoint-online-metrics"></a><span data-ttu-id="1a8da-105">Mesures SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a8da-105">SharePoint Online metrics</span></span>

<span data-ttu-id="1a8da-106">Les mesures générales suivantes pour SharePoint Online fournissent des données réelles sur les performances :</span><span class="sxs-lookup"><span data-stu-id="1a8da-106">The following broad metrics for SharePoint Online provide real world data about performance:</span></span>
  
- <span data-ttu-id="1a8da-107">Chargement rapide des pages</span><span class="sxs-lookup"><span data-stu-id="1a8da-107">How fast pages load</span></span>
    
- <span data-ttu-id="1a8da-108">Nombre d’allers-retours requis par page</span><span class="sxs-lookup"><span data-stu-id="1a8da-108">How many round trips required per page</span></span>
    
- <span data-ttu-id="1a8da-109">Problèmes avec le service</span><span class="sxs-lookup"><span data-stu-id="1a8da-109">Issues with the service</span></span>
    
- <span data-ttu-id="1a8da-110">Autres éléments qui entraînent une dégradation des performances</span><span class="sxs-lookup"><span data-stu-id="1a8da-110">Other things that cause performance degradation</span></span>
    
### <a name="conclusions-reached-because-of-the-data"></a><span data-ttu-id="1a8da-111">Conclusions atteintes en raison des données</span><span class="sxs-lookup"><span data-stu-id="1a8da-111">Conclusions reached because of the data</span></span>

<span data-ttu-id="1a8da-112">Les données nous indiquent :</span><span class="sxs-lookup"><span data-stu-id="1a8da-112">The data tells us:</span></span>
  
- <span data-ttu-id="1a8da-113">La plupart des pages s’exécutent bien sur SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="1a8da-113">Most of the pages perform well on SharePoint Online.</span></span>
    
- <span data-ttu-id="1a8da-114">Les pages non personnalisées se chargent très rapidement.</span><span class="sxs-lookup"><span data-stu-id="1a8da-114">Non-customized pages load very quickly.</span></span>
    
- <span data-ttu-id="1a8da-115">OneDrive Entreprise, les sites d’équipe et les pages système, tels que _layouts, etc., sont tous rapidement chargés.</span><span class="sxs-lookup"><span data-stu-id="1a8da-115">OneDrive for Business, team sites and system pages, such as _layouts, etc., are all quick to load.</span></span>
    
- <span data-ttu-id="1a8da-116">Le chargement des 1 % de pages SharePoint Online les plus lentes prend plus de 5 000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="1a8da-116">The slowest 1% of SharePoint Online pages take more than 5,000 milliseconds to load.</span></span>
    
<span data-ttu-id="1a8da-117">Un test d’évaluation simple que vous pouvez utiliser serait de mesurer les performances en comparant le temps de chargement de votre propre portail au temps de chargement de la page d’accueil OneDrive Entreprise, car elle utilise peu de fonctionnalités personnalisées.</span><span class="sxs-lookup"><span data-stu-id="1a8da-117">One simple benchmark test you can use would be to measure performance by comparing the load time of your own portal against the load time of the OneDrive for Business home page as it uses few customized features.</span></span> <span data-ttu-id="1a8da-118">Il s’agit souvent de la première étape que le support vous demande d’effectuer lors de la résolution des problèmes de performances réseau.</span><span class="sxs-lookup"><span data-stu-id="1a8da-118">This will often be the first step Support will ask you to complete when troubleshooting network performance issues.</span></span>
  
## <a name="use-a-standard-user-account-when-checking-performance"></a><span data-ttu-id="1a8da-119">Utiliser un compte d’utilisateur standard lors de la vérification des performances</span><span class="sxs-lookup"><span data-stu-id="1a8da-119">Use a standard user account when checking performance</span></span>

<span data-ttu-id="1a8da-120">Un administrateur de collection de sites, un propriétaire de site, un éditeur ou un collaborateur appartiennent à des groupes de sécurité supplémentaires, ont des autorisations supplémentaires et, par conséquent, ont des éléments supplémentaires que SharePoint charge sur une page.</span><span class="sxs-lookup"><span data-stu-id="1a8da-120">A Site Collection Administrator, Site Owner, Editor, or Contributor belong to additional security groups, have additional permissions, and therefore have additional elements that SharePoint loads on a page.</span></span>
  
<span data-ttu-id="1a8da-121">Cela s’applique à SharePoint en local et à SharePoint Online, mais dans un scénario local, les différences ne seront pas aussi facilement perceptibles que dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="1a8da-121">This is applicable to SharePoint on-premises and SharePoint Online but in an on-premises scenario the differences will not be as easily noticed as in SharePoint Online.</span></span>
  
<span data-ttu-id="1a8da-122">Pour évaluer correctement le fonctionnement d’une page pour les utilisateurs, vous devez utiliser un compte d’utilisateur standard pour éviter de charger les contrôles de auteur et le trafic supplémentaire lié aux groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1a8da-122">In order to correctly evaluate how a page will perform for users, you should use a standard user account to avoid loading the authoring controls and additional traffic related to security groups.</span></span>
  
## <a name="connection-categories-for-performance-tuning"></a><span data-ttu-id="1a8da-123">Catégories de connexion pour l’optimisation des performances</span><span class="sxs-lookup"><span data-stu-id="1a8da-123">Connection categories for performance tuning</span></span>

<span data-ttu-id="1a8da-124">Vous pouvez classer les connexions entre le serveur et l’utilisateur en trois composants principaux.</span><span class="sxs-lookup"><span data-stu-id="1a8da-124">You can categorize the connections between the server and the user into three main components.</span></span> <span data-ttu-id="1a8da-125">Prenons ces éléments en considération lors de la conception de pages SharePoint Online pour obtenir des informations sur les temps de chargement.</span><span class="sxs-lookup"><span data-stu-id="1a8da-125">Consider these when designing SharePoint Online pages for insight into load times.</span></span>
  
- <span data-ttu-id="1a8da-126">**Serveur** Serveurs que Microsoft héberge dans les centres de données.</span><span class="sxs-lookup"><span data-stu-id="1a8da-126">**Server** The servers that Microsoft hosts in datacenters.</span></span>
    
- <span data-ttu-id="1a8da-127">**Réseau** Le réseau Microsoft, Internet et votre réseau local entre le centre de données et vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1a8da-127">**Network** The Microsoft network, the Internet, and your on-premises network between the datacenter and your users.</span></span>
    
- <span data-ttu-id="1a8da-128">**Navigateur** L’endroit où la page est chargée.</span><span class="sxs-lookup"><span data-stu-id="1a8da-128">**Browser** Where the page is loaded.</span></span>
    
<span data-ttu-id="1a8da-129">Au sein de ces trois connexions, il existe généralement cinq raisons qui provoquent 95 % de pages lentes.</span><span class="sxs-lookup"><span data-stu-id="1a8da-129">Within these three connections there are typically five reasons that cause 95% of slow pages.</span></span> <span data-ttu-id="1a8da-130">Chacune de ces raisons est abordée dans cet article :</span><span class="sxs-lookup"><span data-stu-id="1a8da-130">Each of these reasons is discussed in this article:</span></span>
  
- <span data-ttu-id="1a8da-131">Problèmes de navigation</span><span class="sxs-lookup"><span data-stu-id="1a8da-131">Navigation issues</span></span>
    
- <span data-ttu-id="1a8da-132">Roll up de contenu</span><span class="sxs-lookup"><span data-stu-id="1a8da-132">Content roll up</span></span>
    
- <span data-ttu-id="1a8da-133">Fichiers de grande taille</span><span class="sxs-lookup"><span data-stu-id="1a8da-133">Large files</span></span>
    
- <span data-ttu-id="1a8da-134">De nombreuses demandes au serveur</span><span class="sxs-lookup"><span data-stu-id="1a8da-134">Many requests to the server</span></span>
    
- <span data-ttu-id="1a8da-135">Traitement de la partie Web</span><span class="sxs-lookup"><span data-stu-id="1a8da-135">Web Part processing</span></span>
    
### <a name="server-connection"></a><span data-ttu-id="1a8da-136">Connexion au serveur</span><span class="sxs-lookup"><span data-stu-id="1a8da-136">Server connection</span></span>

<span data-ttu-id="1a8da-137">De nombreux problèmes qui affectent les performances avec SharePoint en local s’appliquent également à SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="1a8da-137">Many of the issues that affect performance with SharePoint on-premises also apply to SharePoint Online.</span></span>
  
<span data-ttu-id="1a8da-138">Comme vous vous y attendiez, vous avez beaucoup plus de contrôle sur la façon dont les serveurs fonctionnent avec SharePoint local.</span><span class="sxs-lookup"><span data-stu-id="1a8da-138">As you would expect, you have far more control over how servers perform with on-premises SharePoint.</span></span> <span data-ttu-id="1a8da-139">Avec SharePoint Online, les choses sont légèrement différentes.</span><span class="sxs-lookup"><span data-stu-id="1a8da-139">With SharePoint Online things are a little different.</span></span> <span data-ttu-id="1a8da-140">Plus vous faites de travail sur un serveur, plus le rendu d’une page est long.</span><span class="sxs-lookup"><span data-stu-id="1a8da-140">The more work you make a server do, the longer it takes to render a page.</span></span> <span data-ttu-id="1a8da-141">Avec SharePoint, le principal responsable à cet égard est les pages complexes avec plusieurs composants Web Parts.</span><span class="sxs-lookup"><span data-stu-id="1a8da-141">With SharePoint, the biggest culprit in this respect are complex pages with multiple web parts.</span></span>
  
<span data-ttu-id="1a8da-142">SharePoint Server local</span><span class="sxs-lookup"><span data-stu-id="1a8da-142">SharePoint Server on-premises</span></span>
  
![Capture d’écran du serveur local](../media/a8e9b646-cdff-4131-976a-b5f891da44ac.png)
  
<span data-ttu-id="1a8da-144">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a8da-144">SharePoint Online</span></span>
  
![Capture d’écran du serveur en ligne](../media/46b27ded-d8a4-4287-b3e0-2603a764b8f8.png)
  
<span data-ttu-id="1a8da-146">Avec SharePoint Online, certaines demandes de page peuvent en réalité finir par appeler plusieurs serveurs.</span><span class="sxs-lookup"><span data-stu-id="1a8da-146">With SharePoint Online, certain page requests may actually end up calling multiple servers.</span></span> <span data-ttu-id="1a8da-147">Vous pouvez obtenir une matrice de demandes entre les serveurs pour une demande individuelle.</span><span class="sxs-lookup"><span data-stu-id="1a8da-147">You could end up with a matrix of requests between servers for an individual request.</span></span> <span data-ttu-id="1a8da-148">Ces interactions sont coûteuses du point de vue du chargement des pages et ralentissent les choses.</span><span class="sxs-lookup"><span data-stu-id="1a8da-148">These interactions are expensive from a page load perspective and will make things slow.</span></span>
  
<span data-ttu-id="1a8da-149">Voici quelques exemples de ces interactions serveur à serveur :</span><span class="sxs-lookup"><span data-stu-id="1a8da-149">Examples of these server to server interactions are:</span></span>
  
- <span data-ttu-id="1a8da-150">Serveurs web SQL serveur</span><span class="sxs-lookup"><span data-stu-id="1a8da-150">Web to SQL Servers</span></span>
    
- <span data-ttu-id="1a8da-151">Serveurs web et d’applications</span><span class="sxs-lookup"><span data-stu-id="1a8da-151">Web to application servers</span></span>
    
<span data-ttu-id="1a8da-152">L’autre chose qui peut ralentir les interactions avec le serveur est les manques de cache.</span><span class="sxs-lookup"><span data-stu-id="1a8da-152">The other thing that can slow down server interactions is cache misses.</span></span> <span data-ttu-id="1a8da-153">Contrairement à SharePoint local, il est très probable que vous touchez le même serveur pour une page que vous avez visitée précédemment . Cela rend la mise en cache d’objets obsolète.</span><span class="sxs-lookup"><span data-stu-id="1a8da-153">Unlike on-premises SharePoint, there is a very slim chance that you will hit the same server for a page that you have visited previously; this makes object caching obsolete.</span></span>
  
### <a name="network-connection"></a><span data-ttu-id="1a8da-154">Connexion réseau </span><span class="sxs-lookup"><span data-stu-id="1a8da-154">Network connection</span></span>

<span data-ttu-id="1a8da-155">Avec SharePoint local qui n’utilise pas de wan, vous pouvez utiliser une connexion haut débit entre le centre de données et les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="1a8da-155">With on-premises SharePoint that doesn't make use of a WAN, you may use a high-speed connection between datacenter and end-users.</span></span> <span data-ttu-id="1a8da-156">En règle générale, les choses sont faciles à gérer du point de vue du réseau.</span><span class="sxs-lookup"><span data-stu-id="1a8da-156">Generally, things are easy to manage from a network perspective.</span></span>
  
<span data-ttu-id="1a8da-157">Avec SharePoint Online, plusieurs facteurs sont à prendre en compte . par exemple :</span><span class="sxs-lookup"><span data-stu-id="1a8da-157">With SharePoint Online, there are a few more factors to consider; for example:</span></span>
  
- <span data-ttu-id="1a8da-158">Le réseau Microsoft</span><span class="sxs-lookup"><span data-stu-id="1a8da-158">The Microsoft network</span></span>
    
- <span data-ttu-id="1a8da-159">The Internet</span><span class="sxs-lookup"><span data-stu-id="1a8da-159">The Internet</span></span>
    
- <span data-ttu-id="1a8da-160">Le isp</span><span class="sxs-lookup"><span data-stu-id="1a8da-160">The ISP</span></span>
    
<span data-ttu-id="1a8da-161">Quelle que soit la version de SharePoint (et le réseau) que vous utilisez, les éléments qui entraînent généralement la occupé(e) du réseau sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="1a8da-161">Regardless of which version of SharePoint (and which network) you are using, things that will typically cause the network to be busy include:</span></span>
  
- <span data-ttu-id="1a8da-162">Charge utile importante</span><span class="sxs-lookup"><span data-stu-id="1a8da-162">Large payload</span></span>
    
- <span data-ttu-id="1a8da-163">Nombreux fichiers</span><span class="sxs-lookup"><span data-stu-id="1a8da-163">Many files</span></span>
    
- <span data-ttu-id="1a8da-164">Distance physique importante avec le serveur</span><span class="sxs-lookup"><span data-stu-id="1a8da-164">Large physical distance to the server</span></span>
    
<span data-ttu-id="1a8da-165">L’une des fonctionnalités que vous pouvez utiliser dans SharePoint Online est le CDN Microsoft (réseau de distribution de contenu).</span><span class="sxs-lookup"><span data-stu-id="1a8da-165">One feature that you can leverage in SharePoint Online is the Microsoft CDN (Content Delivery Network).</span></span> <span data-ttu-id="1a8da-166">Un CDN est essentiellement une collection distribuée de serveurs déployés dans plusieurs centres de données.</span><span class="sxs-lookup"><span data-stu-id="1a8da-166">A CDN is basically a distributed collection of servers deployed across multiple datacenters.</span></span> <span data-ttu-id="1a8da-167">Avec un CDN, le contenu des pages peut être hébergé sur un serveur proche du client, même s’il est éloigné de SharePoint Server d’origine.</span><span class="sxs-lookup"><span data-stu-id="1a8da-167">With a CDN, content on pages can be hosted on a server close to the client even if the client is far away from the originating SharePoint Server.</span></span> <span data-ttu-id="1a8da-168">Microsoft l’utilisera davantage à l’avenir pour stocker des instances locales de pages qui ne peuvent pas être personnalisées, par exemple la page d’accueil de l’administrateur SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="1a8da-168">Microsoft will be using this more in the future to store local instances of pages which cannot be customized, for example the SharePoint Online admin home page.</span></span> <span data-ttu-id="1a8da-169">Pour plus d’informations sur les CDN, voir [Réseaux de distribution de contenu.](content-delivery-networks.md)</span><span class="sxs-lookup"><span data-stu-id="1a8da-169">For more information about CDNs, see [Content delivery networks](content-delivery-networks.md).</span></span>
  
<span data-ttu-id="1a8da-170">Vous devez connaître la vitesse de connexion de votre isp.</span><span class="sxs-lookup"><span data-stu-id="1a8da-170">Something that you need to be aware of but may not be able to do much about is the connection speed of your ISP.</span></span> <span data-ttu-id="1a8da-171">Un outil de test de vitesse simple vous indiquera la vitesse de connexion.</span><span class="sxs-lookup"><span data-stu-id="1a8da-171">A simple speed test tool will tell you the connection speed.</span></span>
  
### <a name="browser-connection"></a><span data-ttu-id="1a8da-172">Connexion du navigateur</span><span class="sxs-lookup"><span data-stu-id="1a8da-172">Browser connection</span></span>

<span data-ttu-id="1a8da-173">Il existe quelques facteurs à prendre en compte pour les navigateurs web du point de vue des performances.</span><span class="sxs-lookup"><span data-stu-id="1a8da-173">There are a few factors to consider with web browsers from a performance perspective.</span></span>
  
<span data-ttu-id="1a8da-174">La visite de pages complexes aura une incidence sur les performances.</span><span class="sxs-lookup"><span data-stu-id="1a8da-174">Visiting complex pages will affect performance.</span></span> <span data-ttu-id="1a8da-175">La plupart des navigateurs n’ont qu’un petit cache (environ 90 Mo), alors que la page web moyenne est généralement d’environ 1,6 Mo.</span><span class="sxs-lookup"><span data-stu-id="1a8da-175">Most browsers only have a small cache (around 90MB), while the average web page is typically around 1.6MB.</span></span> <span data-ttu-id="1a8da-176">L’utilisation n’est pas longue.</span><span class="sxs-lookup"><span data-stu-id="1a8da-176">This doesn't take long to get used up.</span></span>
  
<span data-ttu-id="1a8da-177">La bande passante peut également être un problème.</span><span class="sxs-lookup"><span data-stu-id="1a8da-177">Bandwidth may also be an issue.</span></span> <span data-ttu-id="1a8da-178">Par exemple, si un utilisateur regardera des vidéos dans une autre session, cela affectera les performances de votre page SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1a8da-178">For example, if a user is watching videos in another session, this will affect the performance of your SharePoint page.</span></span> <span data-ttu-id="1a8da-179">Bien que vous ne pouvez pas empêcher les utilisateurs de diffuser des contenus multimédias en continu, vous pouvez contrôler le chargement d’une page pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1a8da-179">While you can't prevent users from streaming media, you can control the way a page will load for users.</span></span>
  
<span data-ttu-id="1a8da-180">Consultez les articles suivants pour découvrir différentes techniques de personnalisation de page SharePoint Online et d’autres meilleures pratiques pour obtenir des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="1a8da-180">Check out the following articles for different SharePoint Online page customization techniques and other best practices to help you achieve optimal performance.</span></span>
  
- [<span data-ttu-id="1a8da-181">Options de navigation pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a8da-181">Navigation options for SharePoint Online</span></span>](navigation-options-for-sharepoint-online.md)
    
- [<span data-ttu-id="1a8da-182">Utiliser l’outil Diagnostic de page pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a8da-182">Use the Page Diagnostics tool for SharePoint Online</span></span>](page-diagnostics-for-spo.md)
    
- [<span data-ttu-id="1a8da-183">Optimisation des images pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a8da-183">Image optimization for SharePoint Online</span></span>](image-optimization-for-sharepoint-online.md)
    
- [<span data-ttu-id="1a8da-184">Différer le chargement des images et des éléments JavaScript dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a8da-184">Delay loading images and JavaScript in SharePoint Online</span></span>](delay-loading-images-and-javascript-in-sharepoint-online.md)
    
- [<span data-ttu-id="1a8da-185">Minimisation et regroupement dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a8da-185">Minification and bundling in SharePoint Online</span></span>](minification-and-bundling-in-sharepoint-online.md)
    
- [<span data-ttu-id="1a8da-186">Utilisation du réseau de distribution de contenu Office 365 avec SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a8da-186">Use the Office 365 Content Delivery Network (CDN) with SharePoint Online</span></span>](use-microsoft-365-cdn-with-spo.md)
    
- [<span data-ttu-id="1a8da-187">Utilisation du service Web De recherche de contenu au lieu du partie Web De requête de contenu pour améliorer les performances dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a8da-187">Using Content Search Web Part instead of Content Query Web Part to improve performance in SharePoint Online</span></span>](using-content-search-web-part-instead-of-content-query-web-part-to-improve-perfo.md)
    
- [<span data-ttu-id="1a8da-188">Planification de la capacité et test de charge SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a8da-188">Capacity planning and load testing SharePoint Online</span></span>](capacity-planning-and-load-testing-sharepoint-online.md)
    
- [<span data-ttu-id="1a8da-189">Diagnostic des problèmes de performances avec SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a8da-189">Diagnosing performance issues with SharePoint Online</span></span>](diagnosing-performance-issues-with-sharepoint-online.md)
    
- [<span data-ttu-id="1a8da-190">Utilisation du cache d’objets avec SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a8da-190">Using the object cache with SharePoint Online</span></span>](using-the-object-cache-with-sharepoint-online.md)
    
- [<span data-ttu-id="1a8da-191">Procédure : éviter les limitations ou les blocages dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a8da-191">How to: Avoid getting throttled or blocked in SharePoint Online</span></span>](https://msdn.microsoft.com/library/office/dn889829.aspx)
    

