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
description: Cet article décrit les aspects spécifiques que vous devez prendre en compte lors de la conception de pages pour optimiser les performances dans SharePoint Online.
ms.openlocfilehash: d3a9dedbd5812774b81494af0f8defa5568f7dac
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690117"
---
# <a name="introduction-to-performance-tuning-for-sharepoint-online"></a><span data-ttu-id="3866c-103">Introduction à l’optimisation des performances pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3866c-103">Introduction to performance tuning for SharePoint Online</span></span>

<span data-ttu-id="3866c-104">Cet article décrit les aspects spécifiques que vous devez prendre en compte lors de la conception de pages pour optimiser les performances dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="3866c-104">This article explains what specific aspects you need to consider when designing pages for best performance in SharePoint Online.</span></span>
     
## <a name="sharepoint-online-metrics"></a><span data-ttu-id="3866c-105">Métriques SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3866c-105">SharePoint Online metrics</span></span>

<span data-ttu-id="3866c-106">Les grandes mesures suivantes de SharePoint Online fournissent des données réelles sur les performances :</span><span class="sxs-lookup"><span data-stu-id="3866c-106">The following broad metrics for SharePoint Online provide real world data about performance:</span></span>
  
- <span data-ttu-id="3866c-107">La vitesse de chargement des pages</span><span class="sxs-lookup"><span data-stu-id="3866c-107">How fast pages load</span></span>
    
- <span data-ttu-id="3866c-108">Nombre de boucles requises par page</span><span class="sxs-lookup"><span data-stu-id="3866c-108">How many round trips required per page</span></span>
    
- <span data-ttu-id="3866c-109">Problèmes liés au service</span><span class="sxs-lookup"><span data-stu-id="3866c-109">Issues with the service</span></span>
    
- <span data-ttu-id="3866c-110">Autres facteurs entraînant une dégradation des performances</span><span class="sxs-lookup"><span data-stu-id="3866c-110">Other things that cause performance degradation</span></span>
    
### <a name="conclusions-reached-because-of-the-data"></a><span data-ttu-id="3866c-111">Conclusions établies en raison des données</span><span class="sxs-lookup"><span data-stu-id="3866c-111">Conclusions reached because of the data</span></span>

<span data-ttu-id="3866c-112">Les données nous indiquent :</span><span class="sxs-lookup"><span data-stu-id="3866c-112">The data tells us:</span></span>
  
- <span data-ttu-id="3866c-113">La plupart des pages fonctionnent correctement sur SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="3866c-113">Most of the pages perform well on SharePoint Online.</span></span>
    
- <span data-ttu-id="3866c-114">Les pages non personnalisées sont chargées très rapidement.</span><span class="sxs-lookup"><span data-stu-id="3866c-114">Non-customized pages load very quickly.</span></span>
    
- <span data-ttu-id="3866c-115">OneDrive entreprise, les sites d’équipe et les pages système, telles que les _layouts, etc., sont tous rapides à charger.</span><span class="sxs-lookup"><span data-stu-id="3866c-115">OneDrive for Business, team sites and system pages, such as _layouts, etc., are all quick to load.</span></span>
    
- <span data-ttu-id="3866c-116">Le chargement des pages SharePoint Online les plus lentes est de plus de 5 000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="3866c-116">The slowest 1% of SharePoint Online pages take more than 5,000 milliseconds to load.</span></span>
    
<span data-ttu-id="3866c-117">Il est possible de mesurer les performances en comparant le temps de chargement de votre propre portail et le temps de chargement de la page d’accueil de OneDrive entreprise, car il utilise peu de fonctionnalités personnalisées.</span><span class="sxs-lookup"><span data-stu-id="3866c-117">One simple benchmark test you can use would be to measure performance by comparing the load time of your own portal against the load time of the OneDrive for Business home page as it uses few customized features.</span></span> <span data-ttu-id="3866c-118">Il s’agit souvent de la première étape que vous devez prendre en charge pour résoudre les problèmes de performances réseau.</span><span class="sxs-lookup"><span data-stu-id="3866c-118">This will often be the first step Support will ask you to complete when troubleshooting network performance issues.</span></span>
  
## <a name="use-a-standard-user-account-when-checking-performance"></a><span data-ttu-id="3866c-119">Utiliser un compte d’utilisateur standard lors de la vérification des performances</span><span class="sxs-lookup"><span data-stu-id="3866c-119">Use a standard user account when checking performance</span></span>

<span data-ttu-id="3866c-120">Un administrateur de collection de sites, un propriétaire de site, un éditeur ou un collaborateur appartient à des groupes de sécurité supplémentaires, disposent d’autorisations supplémentaires et, par conséquent, ont des éléments supplémentaires chargés par SharePoint sur une page.</span><span class="sxs-lookup"><span data-stu-id="3866c-120">A Site Collection Administrator, Site Owner, Editor, or Contributor belong to additional security groups, have additional permissions, and therefore have additional elements that SharePoint loads on a page.</span></span>
  
<span data-ttu-id="3866c-121">Ceci s’applique à SharePoint Online et SharePoint Online, mais dans un scénario local, les différences ne seront pas aussi facilement remarquées que dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="3866c-121">This is applicable to SharePoint on-premises and SharePoint Online but in an on-premises scenario the differences will not be as easily noticed as in SharePoint Online.</span></span>
  
<span data-ttu-id="3866c-122">Pour évaluer correctement l’exécution d’une page pour les utilisateurs, vous devez utiliser un compte d’utilisateur standard afin d’éviter de charger les contrôles de création et le trafic supplémentaire lié aux groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3866c-122">In order to correctly evaluate how a page will perform for users, you should use a standard user account to avoid loading the authoring controls and additional traffic related to security groups.</span></span>
  
## <a name="connection-categories-for-performance-tuning"></a><span data-ttu-id="3866c-123">Catégories de connexion pour le réglage des performances</span><span class="sxs-lookup"><span data-stu-id="3866c-123">Connection categories for performance tuning</span></span>

<span data-ttu-id="3866c-124">Vous pouvez catégoriser les connexions entre le serveur et l’utilisateur en trois composants principaux.</span><span class="sxs-lookup"><span data-stu-id="3866c-124">You can categorize the connections between the server and the user into three main components.</span></span> <span data-ttu-id="3866c-125">Tenez compte de ces éléments lors de la conception de pages SharePoint Online pour un aperçu des temps de chargement.</span><span class="sxs-lookup"><span data-stu-id="3866c-125">Consider these when designing SharePoint Online pages for insight into load times.</span></span>
  
- <span data-ttu-id="3866c-126">**Server (serveur** ) Les serveurs que Microsoft héberge dans les centres de contenu.</span><span class="sxs-lookup"><span data-stu-id="3866c-126">**Server** The servers that Microsoft hosts in datacenters.</span></span>
    
- <span data-ttu-id="3866c-127">**Réseau** Le réseau Microsoft, Internet et votre réseau local entre le centre de connaissances et vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="3866c-127">**Network** The Microsoft network, the Internet, and your on-premises network between the datacenter and your users.</span></span>
    
- <span data-ttu-id="3866c-128">**Explorateur** Emplacement de chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="3866c-128">**Browser** Where the page is loaded.</span></span>
    
<span data-ttu-id="3866c-129">Au sein de ces trois connexions, il existe généralement cinq raisons qui causent 95% de pages chargées.</span><span class="sxs-lookup"><span data-stu-id="3866c-129">Within these three connections there are typically five reasons that cause 95% of slow pages.</span></span> <span data-ttu-id="3866c-130">Chacune de ces raisons est abordée dans cet article :</span><span class="sxs-lookup"><span data-stu-id="3866c-130">Each of these reasons is discussed in this article:</span></span>
  
- <span data-ttu-id="3866c-131">Problèmes de navigation</span><span class="sxs-lookup"><span data-stu-id="3866c-131">Navigation issues</span></span>
    
- <span data-ttu-id="3866c-132">Cumul de contenu</span><span class="sxs-lookup"><span data-stu-id="3866c-132">Content roll up</span></span>
    
- <span data-ttu-id="3866c-133">Fichiers volumineux</span><span class="sxs-lookup"><span data-stu-id="3866c-133">Large files</span></span>
    
- <span data-ttu-id="3866c-134">Nombreuses requêtes adressées au serveur</span><span class="sxs-lookup"><span data-stu-id="3866c-134">Many requests to the server</span></span>
    
- <span data-ttu-id="3866c-135">Traitement des composants WebPart</span><span class="sxs-lookup"><span data-stu-id="3866c-135">Web Part processing</span></span>
    
### <a name="server-connection"></a><span data-ttu-id="3866c-136">Connexion au serveur</span><span class="sxs-lookup"><span data-stu-id="3866c-136">Server connection</span></span>

<span data-ttu-id="3866c-137">De nombreux problèmes qui affectent les performances avec SharePoint en local s’appliquent également à SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="3866c-137">Many of the issues that affect performance with SharePoint on-premises also apply to SharePoint Online.</span></span>
  
<span data-ttu-id="3866c-138">Comme vous pouvez vous y attendre, vous avez beaucoup plus de contrôle sur la façon dont les serveurs effectuent SharePoint sur site.</span><span class="sxs-lookup"><span data-stu-id="3866c-138">As you would expect, you have far more control over how servers perform with on-premises SharePoint.</span></span> <span data-ttu-id="3866c-139">Avec SharePoint Online, les choses sont un peu différentes.</span><span class="sxs-lookup"><span data-stu-id="3866c-139">With SharePoint Online things are a little different.</span></span> <span data-ttu-id="3866c-140">Plus le nombre de tâches que vous effectuez sur un serveur est long, plus le rendu d’une page est long.</span><span class="sxs-lookup"><span data-stu-id="3866c-140">The more work you make a server do, the longer it takes to render a page.</span></span> <span data-ttu-id="3866c-141">Avec SharePoint, le plus grand coupable de ce sujet sont des pages complexes avec plusieurs composants WebPart.</span><span class="sxs-lookup"><span data-stu-id="3866c-141">With SharePoint, the biggest culprit in this respect are complex pages with multiple web parts.</span></span>
  
<span data-ttu-id="3866c-142">SharePoint Server en local</span><span class="sxs-lookup"><span data-stu-id="3866c-142">SharePoint Server on-premises</span></span>
  
![Capture d’écran du serveur local](../media/a8e9b646-cdff-4131-976a-b5f891da44ac.png)
  
<span data-ttu-id="3866c-144">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3866c-144">SharePoint Online</span></span>
  
![Capture d’écran du serveur en ligne](../media/46b27ded-d8a4-4287-b3e0-2603a764b8f8.png)
  
<span data-ttu-id="3866c-146">Avec SharePoint Online, certaines demandes de page peuvent réellement appeler plusieurs serveurs.</span><span class="sxs-lookup"><span data-stu-id="3866c-146">With SharePoint Online, certain page requests may actually end up calling multiple servers.</span></span> <span data-ttu-id="3866c-147">Vous pouvez obtenir une matrice des demandes entre les serveurs pour une demande individuelle.</span><span class="sxs-lookup"><span data-stu-id="3866c-147">You could end up with a matrix of requests between servers for an individual request.</span></span> <span data-ttu-id="3866c-148">Ces interactions sont coûteuses du point de vue du chargement des pages et rendent les choses plus lentes.</span><span class="sxs-lookup"><span data-stu-id="3866c-148">These interactions are expensive from a page load perspective and will make things slow.</span></span>
  
<span data-ttu-id="3866c-149">Voici quelques exemples d’interactions serveur à serveur :</span><span class="sxs-lookup"><span data-stu-id="3866c-149">Examples of these server to server interactions are:</span></span>
  
- <span data-ttu-id="3866c-150">Web vers les serveurs SQL</span><span class="sxs-lookup"><span data-stu-id="3866c-150">Web to SQL Servers</span></span>
    
- <span data-ttu-id="3866c-151">Web vers les serveurs d’applications</span><span class="sxs-lookup"><span data-stu-id="3866c-151">Web to application servers</span></span>
    
<span data-ttu-id="3866c-152">Les échecs de cache sont les autres opérations qui ralentissent les interactions du serveur.</span><span class="sxs-lookup"><span data-stu-id="3866c-152">The other thing that can slow down server interactions is cache misses.</span></span> <span data-ttu-id="3866c-153">Contrairement à SharePoint sur site, il existe une très faible probabilité que vous atteigniez le même serveur pour une page que vous avez visitée précédemment ; Cela rend la mise en cache d’objets obsolète.</span><span class="sxs-lookup"><span data-stu-id="3866c-153">Unlike on-premises SharePoint, there is a very slim chance that you will hit the same server for a page that you have visited previously; this makes object caching obsolete.</span></span>
  
### <a name="network-connection"></a><span data-ttu-id="3866c-154">Connexion réseau </span><span class="sxs-lookup"><span data-stu-id="3866c-154">Network connection</span></span>

<span data-ttu-id="3866c-155">Avec SharePoint sur site qui n’utilise pas de réseau étendu (WAN), vous pouvez utiliser une connexion à haut débit entre le centre de données et les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="3866c-155">With on-premises SharePoint that doesn't make use of a WAN, you may use a high-speed connection between datacenter and end-users.</span></span> <span data-ttu-id="3866c-156">En règle générale, les choses sont faciles à gérer du point de vue du réseau.</span><span class="sxs-lookup"><span data-stu-id="3866c-156">Generally, things are easy to manage from a network perspective.</span></span>
  
<span data-ttu-id="3866c-157">Avec SharePoint Online, il existe quelques facteurs supplémentaires à prendre en compte ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="3866c-157">With SharePoint Online, there are a few more factors to consider; for example:</span></span>
  
- <span data-ttu-id="3866c-158">Le réseau Microsoft</span><span class="sxs-lookup"><span data-stu-id="3866c-158">The Microsoft network</span></span>
    
- <span data-ttu-id="3866c-159">Internet</span><span class="sxs-lookup"><span data-stu-id="3866c-159">The Internet</span></span>
    
- <span data-ttu-id="3866c-160">Le fournisseur de services Internet</span><span class="sxs-lookup"><span data-stu-id="3866c-160">The ISP</span></span>
    
<span data-ttu-id="3866c-161">Quelle que soit la version de SharePoint (et le réseau) que vous utilisez, les éléments qui entraînent généralement la disponibilité du réseau sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="3866c-161">Regardless of which version of SharePoint (and which network) you are using, things that will typically cause the network to be busy include:</span></span>
  
- <span data-ttu-id="3866c-162">Grande charge utile</span><span class="sxs-lookup"><span data-stu-id="3866c-162">Large payload</span></span>
    
- <span data-ttu-id="3866c-163">Nombreux fichiers</span><span class="sxs-lookup"><span data-stu-id="3866c-163">Many files</span></span>
    
- <span data-ttu-id="3866c-164">Grande distance physique vers le serveur</span><span class="sxs-lookup"><span data-stu-id="3866c-164">Large physical distance to the server</span></span>
    
<span data-ttu-id="3866c-165">L’une des fonctionnalités que vous pouvez utiliser dans SharePoint Online est le réseau de distribution de contenu (CDN) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3866c-165">One feature that you can leverage in SharePoint Online is the Microsoft CDN (Content Delivery Network).</span></span> <span data-ttu-id="3866c-166">Un CDN est fondamentalement une collection distribuée de serveurs déployés sur plusieurs centres de contenu.</span><span class="sxs-lookup"><span data-stu-id="3866c-166">A CDN is basically a distributed collection of servers deployed across multiple datacenters.</span></span> <span data-ttu-id="3866c-167">Avec un CDN, le contenu sur les pages peut être hébergé sur un serveur proche du client même si le client est éloigné du serveur SharePoint d’origine.</span><span class="sxs-lookup"><span data-stu-id="3866c-167">With a CDN, content on pages can be hosted on a server close to the client even if the client is far away from the originating SharePoint Server.</span></span> <span data-ttu-id="3866c-168">Microsoft utilisera cette version plus prochaine pour stocker les instances locales des pages qui ne peuvent pas être personnalisées, par exemple la page d’accueil de l’administration SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="3866c-168">Microsoft will be using this more in the future to store local instances of pages which cannot be customized, for example the SharePoint Online admin home page.</span></span> <span data-ttu-id="3866c-169">Pour plus d’informations sur CDN, consultez la rubrique [Content Delivery Networks](content-delivery-networks.md).</span><span class="sxs-lookup"><span data-stu-id="3866c-169">For more information about CDNs, see [Content delivery networks](content-delivery-networks.md).</span></span>
  
<span data-ttu-id="3866c-170">La vitesse de connexion de votre fournisseur de services Internet (ISP) ne vous indiquera peut-être pas que vous devez prendre en compte.</span><span class="sxs-lookup"><span data-stu-id="3866c-170">Something that you need to be aware of but may not be able to do much about is the connection speed of your ISP.</span></span> <span data-ttu-id="3866c-171">Un outil de test rapide vous indiquera la vitesse de connexion.</span><span class="sxs-lookup"><span data-stu-id="3866c-171">A simple speed test tool will tell you the connection speed.</span></span>
  
### <a name="browser-connection"></a><span data-ttu-id="3866c-172">Connexion de navigateur</span><span class="sxs-lookup"><span data-stu-id="3866c-172">Browser connection</span></span>

<span data-ttu-id="3866c-173">Il existe quelques facteurs à prendre en compte pour les navigateurs Web du point de vue des performances.</span><span class="sxs-lookup"><span data-stu-id="3866c-173">There are a few factors to consider with web browsers from a performance perspective.</span></span>
  
<span data-ttu-id="3866c-174">La consultation des pages complexes affectera les performances.</span><span class="sxs-lookup"><span data-stu-id="3866c-174">Visiting complex pages will affect performance.</span></span> <span data-ttu-id="3866c-175">La plupart des navigateurs ont seulement un petit cache (environ 90MB), tandis que la page Web moyenne est généralement d’environ 1,6 Mo.</span><span class="sxs-lookup"><span data-stu-id="3866c-175">Most browsers only have a small cache (around 90MB), while the average web page is typically around 1.6MB.</span></span> <span data-ttu-id="3866c-176">L’utilisation de cette valeur n’est pas assez longue.</span><span class="sxs-lookup"><span data-stu-id="3866c-176">This doesn't take long to get used up.</span></span>
  
<span data-ttu-id="3866c-177">La bande passante peut également être un problème.</span><span class="sxs-lookup"><span data-stu-id="3866c-177">Bandwidth may also be an issue.</span></span> <span data-ttu-id="3866c-178">Par exemple, si un utilisateur regarde des vidéos dans une autre session, cela aura une incidence sur les performances de votre page SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3866c-178">For example, if a user is watching videos in another session, this will affect the performance of your SharePoint page.</span></span> <span data-ttu-id="3866c-179">Bien que vous ne puissiez pas empêcher les utilisateurs de diffuser des médias en continu, vous pouvez contrôler le chargement d’une page pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="3866c-179">While you can't prevent users from streaming media, you can control the way a page will load for users.</span></span>
  
<span data-ttu-id="3866c-180">Consultez les articles suivants pour connaître les différentes techniques de personnalisation des pages SharePoint Online et d’autres meilleures pratiques pour obtenir des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="3866c-180">Check out the following articles for different SharePoint Online page customization techniques and other best practices to help you achieve optimal performance.</span></span>
  
- [<span data-ttu-id="3866c-181">Options de navigation pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3866c-181">Navigation options for SharePoint Online</span></span>](navigation-options-for-sharepoint-online.md)
    
- [<span data-ttu-id="3866c-182">Utiliser l’outil de diagnostics de page pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3866c-182">Use the Page Diagnostics tool for SharePoint Online</span></span>](page-diagnostics-for-spo.md)
    
- [<span data-ttu-id="3866c-183">Optimisation des images pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3866c-183">Image optimization for SharePoint Online</span></span>](image-optimization-for-sharepoint-online.md)
    
- [<span data-ttu-id="3866c-184">Différer le chargement des images et des éléments JavaScript dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3866c-184">Delay loading images and JavaScript in SharePoint Online</span></span>](delay-loading-images-and-javascript-in-sharepoint-online.md)
    
- [<span data-ttu-id="3866c-185">Minimisation et regroupement dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3866c-185">Minification and bundling in SharePoint Online</span></span>](minification-and-bundling-in-sharepoint-online.md)
    
- [<span data-ttu-id="3866c-186">Utilisation du réseau de distribution de contenu Office 365 avec SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3866c-186">Use the Office 365 Content Delivery Network (CDN) with SharePoint Online</span></span>](use-microsoft-365-cdn-with-spo.md)
    
- [<span data-ttu-id="3866c-187">Utilisation du composant WebPart de recherche de contenu au lieu du composant WebPart requête de contenu pour améliorer les performances dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3866c-187">Using Content Search Web Part instead of Content Query Web Part to improve performance in SharePoint Online</span></span>](using-content-search-web-part-instead-of-content-query-web-part-to-improve-perfo.md)
    
- [<span data-ttu-id="3866c-188">Planification de la capacité et test de charge SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3866c-188">Capacity planning and load testing SharePoint Online</span></span>](capacity-planning-and-load-testing-sharepoint-online.md)
    
- [<span data-ttu-id="3866c-189">Diagnostic des problèmes de performances avec SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3866c-189">Diagnosing performance issues with SharePoint Online</span></span>](diagnosing-performance-issues-with-sharepoint-online.md)
    
- [<span data-ttu-id="3866c-190">Utilisation du cache d’objets avec SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3866c-190">Using the object cache with SharePoint Online</span></span>](using-the-object-cache-with-sharepoint-online.md)
    
- [<span data-ttu-id="3866c-191">Procédure : éviter les limitations ou les blocages dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3866c-191">How to: Avoid getting throttled or blocked in SharePoint Online</span></span>](https://msdn.microsoft.com/library/office/dn889829.aspx)
    

