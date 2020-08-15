---
title: Utilisation du cache d’objets avec SharePoint Online
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 4/20/2015
audience: Admin
ms.topic: troubleshooting
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- SPO_Content
f1.keywords:
- CSH
ms.custom: Adm_O365
search.appverid:
- SPO160
- MET150
ms.assetid: 38bc9c14-3826-449c-beb6-b1003bcbeaaf
description: Cet article explique la différence entre l’utilisation du cache d’objets dans SharePoint Server 2013 sur site et SharePoint Online.
ms.openlocfilehash: 279d156a941aad6fbe7adbcf052c57f5b58c652f
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46695873"
---
# <a name="using-the-object-cache-with-sharepoint-online"></a><span data-ttu-id="07365-103">Utilisation du cache d’objets avec SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="07365-103">Using the object cache with SharePoint Online</span></span>

<span data-ttu-id="07365-104">Cet article explique la différence entre l’utilisation du cache d’objets dans SharePoint Server 2013 sur site et SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="07365-104">This article explains the difference between using the object cache in SharePoint Server 2013 on-premises and SharePoint Online.</span></span>
  
<span data-ttu-id="07365-105">Il y a un impact négatif significatif sur le recours au cache d’objets dans le déploiement de SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="07365-105">There is significant negative impact of relying on the object cache in SharePoint Online deployment.</span></span> <span data-ttu-id="07365-106">Toute dépendance vis-à-vis du cache d’objets dans SharePoint Online réduira la fiabilité de votre page.</span><span class="sxs-lookup"><span data-stu-id="07365-106">Any dependency on object cache in SharePoint Online will reduce the reliability of your page.</span></span> 
  
## <a name="how-the-sharepoint-online-and-sharepoint-server-2013-object-cache-works"></a><span data-ttu-id="07365-107">Fonctionnement du cache d’objets SharePoint Online et SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="07365-107">How the SharePoint Online and SharePoint Server 2013 object cache works</span></span>

<span data-ttu-id="07365-108">Lorsque SharePoint Server 2013 est hébergé en local, le client dispose de serveurs Web frontaux privés qui hébergent le cache d’objets.</span><span class="sxs-lookup"><span data-stu-id="07365-108">When SharePoint Server 2013 is hosted on-premises, the customer has private front-end web servers that host the object cache.</span></span> <span data-ttu-id="07365-109">Cela signifie que le cache est dédié à un client et qu’il est limité par la capacité de mémoire disponible et allouée au cache d’objets.</span><span class="sxs-lookup"><span data-stu-id="07365-109">This means the cache is dedicated to one customer and is only limited by how much memory is available and allocated to the object cache.</span></span> <span data-ttu-id="07365-110">Étant donné qu’un seul client est pris en charge dans le scénario local, les serveurs Web frontaux ont généralement des demandes de requêtes sur les mêmes sites.</span><span class="sxs-lookup"><span data-stu-id="07365-110">Because only one customer is served in the on-premises scenario the front-end web servers typically have users making requests to the same sites over and over.</span></span> <span data-ttu-id="07365-111">Cela signifie que le cache est saturé rapidement et qu’il reste complet des résultats de la requête de liste et des objets SharePoint demandés régulièrement par vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="07365-111">This means that the cache gets full quickly and remains full of the list query results and SharePoint objects that your users are requesting on a regular basis.</span></span>
  
![Affiche le trafic et la charge vers les serveurs web frontaux locaux](../media/a0d38b36-4909-4abb-8d4e-4930814bb3de.png)
  
<span data-ttu-id="07365-113">Par conséquent, la deuxième fois qu’un utilisateur visite une page, le temps de chargement de la page est amélioré.</span><span class="sxs-lookup"><span data-stu-id="07365-113">As a result, the second time a user visits a page, the page load time improves.</span></span> <span data-ttu-id="07365-114">Après un minimum de quatre chargements de la même page, la page est mise en cache sur tous les serveurs Web frontaux.</span><span class="sxs-lookup"><span data-stu-id="07365-114">After a minimum of four loads of the same page, the page is cached on all of the front-end web servers.</span></span>
  
<span data-ttu-id="07365-115">En revanche, dans SharePoint Online, il existe beaucoup plus de serveurs, mais également de nombreux autres sites.</span><span class="sxs-lookup"><span data-stu-id="07365-115">In contrast, in SharePoint Online there are many more servers but also many more sites.</span></span> <span data-ttu-id="07365-116">Chaque utilisateur peut se connecter à un autre serveur Web frontal qui n’a pas de cache rempli.</span><span class="sxs-lookup"><span data-stu-id="07365-116">Each user may connect to a different front-end web server that doesn't have the cache populated.</span></span> <span data-ttu-id="07365-117">Ou peut-être que le cache est rempli pour un serveur, mais que le prochain utilisateur de ce serveur Web frontal demande une page d’un autre site.</span><span class="sxs-lookup"><span data-stu-id="07365-117">Or, perhaps the cache does get populated for a server, but the next user to that front-end web server requests a page from a different site.</span></span> <span data-ttu-id="07365-118">Ou bien, même si l’utilisateur suivant demande la même page que lors de sa visite précédente, il bénéficie d’un équilibrage de charge sur un autre serveur Web frontal qui n’a pas cette page dans son cache.</span><span class="sxs-lookup"><span data-stu-id="07365-118">Or, even if the next user requests the same page as on their previous visit, they are load-balanced to a different front-end web server that doesn't have that page in its cache.</span></span> <span data-ttu-id="07365-119">Dans ce dernier cas, la mise en cache n’aide pas les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="07365-119">In this last case, caching doesn't help the users at all.</span></span>
  
<span data-ttu-id="07365-120">Dans la figure suivante, chaque point représente une page demandée par un utilisateur et là où il est mis en cache.</span><span class="sxs-lookup"><span data-stu-id="07365-120">In the following figure, each dot represents a page that a user is requesting and where it cached.</span></span> <span data-ttu-id="07365-121">Différentes couleurs représentent différents clients qui utilisent l’infrastructure SaaS partagée.</span><span class="sxs-lookup"><span data-stu-id="07365-121">Different colors represent different customers making shared use of the SaaS infrastructure.</span></span>
  
![Affiche les résultats de la mise en cache d’objets dans SharePoint Online](../media/25d04011-ef83-4cb7-9e04-a6ed490f63c3.png)
  
<span data-ttu-id="07365-123">Comme vous pouvez le voir dans le diagramme, les risques qu’un utilisateur donné accède à un serveur avec la version mise en cache de la page sont réduits.</span><span class="sxs-lookup"><span data-stu-id="07365-123">As you can see from the diagram, the chances of any given user hitting a server with the cached version of their page are slim.</span></span> <span data-ttu-id="07365-124">En outre, en raison du grand débit et du fait que les serveurs sont partagés entre de nombreux sites, le cache n’a pas été utilisé depuis longtemps car il n’y a qu’un espace suffisant pour la mise en cache.</span><span class="sxs-lookup"><span data-stu-id="07365-124">Also, due to the large throughput and fact that the servers are shared between many sites, the cache doesn't last long since there is only so much space for caching available.</span></span>
  
<span data-ttu-id="07365-125">Pour toutes ces raisons, il n’est pas possible de s’appuyer sur la récupération des objets mis en cache pour garantir une expérience utilisateur de qualité et des temps de chargement des pages dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="07365-125">For all of these reasons, relying on users getting cached objects is not an effective way to ensure a quality user experience and page load times in SharePoint Online.</span></span>
  
## <a name="if-we-cant-rely-on-the-object-cache-to-improve-performance-in-sharepoint-online-what-do-we-use-instead"></a><span data-ttu-id="07365-126">Si nous ne pouvons pas compter sur le cache d’objets pour améliorer les performances dans SharePoint Online, que pouvons-nous utiliser à la place ?</span><span class="sxs-lookup"><span data-stu-id="07365-126">If we can't rely on the object cache to improve performance in SharePoint Online, what do we use instead?</span></span>

<span data-ttu-id="07365-127">Étant donné que vous ne devez pas vous appuyer sur la mise en cache dans SharePoint Online, vous devez évaluer d’autres approches de conception pour les personnalisations SharePoint qui utilisent le cache d’objets.</span><span class="sxs-lookup"><span data-stu-id="07365-127">Since you shouldn't rely on caching in SharePoint Online, you should evaluate alternative design approaches for SharePoint customizations that use the object cache.</span></span> <span data-ttu-id="07365-128">Cela signifie que l’utilisation d’approches pour les problèmes de performances ne repose pas sur la mise en cache d’objets pour produire de bonnes résultats pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="07365-128">This means using approaches for performance issues which do not rely on the object caching in order to produce good results for users.</span></span> <span data-ttu-id="07365-129">Ceci est décrit dans certains autres Articles de cette série et inclut les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="07365-129">This is described in some of the other articles in this series and include:</span></span>
  
- [<span data-ttu-id="07365-130">Options de navigation pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="07365-130">Navigation options for SharePoint Online</span></span>](navigation-options-for-sharepoint-online.md)
    
- [<span data-ttu-id="07365-131">Minimisation et regroupement dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="07365-131">Minification and bundling in SharePoint Online</span></span>](minification-and-bundling-in-sharepoint-online.md)
    
- [<span data-ttu-id="07365-132">Utilisation du réseau de distribution de contenu Office 365 avec SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="07365-132">Use the Office 365 Content Delivery Network (CDN) with SharePoint Online</span></span>](use-microsoft-365-cdn-with-spo.md)
    
- [<span data-ttu-id="07365-133">Différer le chargement des images et des éléments JavaScript dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="07365-133">Delay loading images and JavaScript in SharePoint Online</span></span>](delay-loading-images-and-javascript-in-sharepoint-online.md)
    

