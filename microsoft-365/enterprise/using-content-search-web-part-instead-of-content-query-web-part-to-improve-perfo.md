---
title: Utilisation du composant WebPart de recherche de contenu au lieu du composant WebPart requête de contenu pour améliorer les performances dans SharePoint Online
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 4/20/2015
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- SPO_Content
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-apr2020
search.appverid:
- MET150
- SPO160
ms.assetid: e8ce6b72-745b-464a-85c7-cbf6eb53391b
description: Découvrez comment augmenter les performances en remplaçant le composant WebPart de requête de contenu par le composant WebPart de recherche de contenu dans SharePoint Server 2013 et SharePoint Online.
ms.openlocfilehash: e5f57e59a421d79302f447e229091fdfc96f1237
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690217"
---
# <a name="using-content-search-web-part-instead-of-content-query-web-part-to-improve-performance-in-sharepoint-online"></a><span data-ttu-id="fb7e9-103">Utilisation du composant WebPart de recherche de contenu au lieu du composant WebPart requête de contenu pour améliorer les performances dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="fb7e9-103">Using Content Search Web Part instead of Content Query Web Part to improve performance in SharePoint Online</span></span>

<span data-ttu-id="fb7e9-104">Cet article explique comment augmenter les performances en remplaçant le composant WebPart de requête de contenu par le composant WebPart de recherche de contenu dans SharePoint Server 2013 et SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-104">This article describes how to increase performance by replacing the Content Query Web Part with the Content Search Web Part in SharePoint Server 2013 and SharePoint Online.</span></span>
  
<span data-ttu-id="fb7e9-105">L’une des nouvelles fonctionnalités les plus puissantes de SharePoint Server 2013 et SharePoint Online est le composant WebPart de recherche de contenu (composant WebPart recherche).</span><span class="sxs-lookup"><span data-stu-id="fb7e9-105">One of the most powerful new features of SharePoint Server 2013 and SharePoint Online is the Content Search Web Part (CSWP).</span></span> <span data-ttu-id="fb7e9-106">Ce composant WebPart utilise l’index de recherche pour récupérer rapidement les résultats présentés à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-106">This Web Part uses the search index to quickly retrieve results which are shown to the user.</span></span> <span data-ttu-id="fb7e9-107">Utilisez le composant WebPart recherche de contenu au lieu du composant WebPart de requête de contenu (CQWP) dans vos pages pour améliorer les performances de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-107">Use the Content Search Web Part instead of the Content Query Web Part (CQWP) in your pages to improve performance for your users.</span></span>
  
<span data-ttu-id="fb7e9-108">L’utilisation d’un composant WebPart de recherche de contenu sur un composant WebPart de requête de contenu entraîne presque toujours une amélioration considérable des performances de chargement de pages sur SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-108">Using a Content Search Web Part over a Content Query Web Part will almost always result in significantly better page load performance on SharePoint Online.</span></span> <span data-ttu-id="fb7e9-109">Il existe une configuration supplémentaire pour obtenir la bonne requête, mais les récompenses sont des performances accrues et des utilisateurs plus heureux.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-109">There is a little additional configuration to get the right query, but the rewards are improved performance and happier users.</span></span>
  
## <a name="comparing-the-performance-gain-you-get-from-using-content-search-web-part-instead-of-content-query-web-part"></a><span data-ttu-id="fb7e9-110">Comparaison des gains de performances que vous obtenez en utilisant le composant WebPart de recherche de contenu au lieu du composant WebPart requête de contenu</span><span class="sxs-lookup"><span data-stu-id="fb7e9-110">Comparing the performance gain you get from using Content Search Web Part instead of Content Query Web Part</span></span>

<span data-ttu-id="fb7e9-111">Les exemples suivants montrent les gains de performances relatifs que vous pouvez recevoir lorsque vous utilisez un composant WebPart de recherche de contenu au lieu d’un composant WebPart de requête de contenu.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-111">The following examples show the relative performance gains you may receive when you use a Content Search Web Part instead of a Content Query Web Part.</span></span> <span data-ttu-id="fb7e9-112">Les effets sont plus évidents avec une structure de site complexe et des requêtes de contenu très étendues.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-112">The effects are more obvious with a complex site structure and very broad content queries.</span></span>
  
<span data-ttu-id="fb7e9-113">Cet exemple de site présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb7e9-113">This example site has the following characteristics:</span></span>
  
- <span data-ttu-id="fb7e9-114">8 niveaux de sous-sites.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-114">8 levels of subsites.</span></span>
    
- <span data-ttu-id="fb7e9-115">Répertorie les données à l’aide d’un type de contenu « fruit » personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-115">Lists using a custom "fruit" content type.</span></span>
    
- <span data-ttu-id="fb7e9-116">Dans le composant WebPart, la requête de contenu est large et renvoie tous les éléments dont le type de contenu est « fruit ».</span><span class="sxs-lookup"><span data-stu-id="fb7e9-116">In the Web Part, the content query is broad, returning all items with the content type of "fruit".</span></span>
    
- <span data-ttu-id="fb7e9-117">L’exemple utilise uniquement 50 éléments sur les 8 sites.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-117">The example only uses 50 items across the 8 sites.</span></span> <span data-ttu-id="fb7e9-118">Les effets seront encore plus prononcés pour les sites avec davantage de contenu.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-118">The effects will be even more pronounced for sites with more content.</span></span>
    
<span data-ttu-id="fb7e9-119">Voici une capture d’écran des résultats du composant WebPart de requête de contenu.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-119">Here is a screen shot of the results of the Content Query Web Part.</span></span>
  
![Figure illustrant la requête de contenu pour le composant WebPart](../media/b3d41f20-dfe5-46ed-9c0a-31057e82de33.png)
  
<span data-ttu-id="fb7e9-121">Dans Internet Explorer, utilisez l’onglet **réseau** des outils de développement F12 pour consulter les détails de l’en-tête de la réponse.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-121">In Internet Explorer, use the **Network** tab of the F12 developer tools to look at the details for the response header.</span></span> <span data-ttu-id="fb7e9-122">Dans la capture d’écran suivante, la valeur de la **SPRequestDuration** pour ce chargement de page est de 924 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-122">In the following screen shot, the value for the **SPRequestDuration** for this page load is 924 milliseconds.</span></span> 
  
![Capture d’écran montrant la durée de demande de 924](../media/343571f2-a249-4de2-bc11-2cee93498aea.png)
  
 <span data-ttu-id="fb7e9-124">**SPRequestDuration** indique le volume de travail réalisé sur le serveur pour préparer la page.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-124">**SPRequestDuration** indicates the amount of work that is done on the server to prepare the page.</span></span> <span data-ttu-id="fb7e9-125">Le changement de contenu par composants WebPart de requête avec le contenu par composants WebPart de recherche réduit considérablement le temps nécessaire au rendu de la page.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-125">Switching Content by Query Web Parts with Content by Search Web Parts dramatically reduces the time it takes to render the page.</span></span> <span data-ttu-id="fb7e9-126">En revanche, une page avec un composant WebPart de recherche de contenu équivalent, renvoyant le même nombre de résultats a une valeur **SPRequestDuration** de 106 millisecondes, comme illustré dans cette capture d’écran :</span><span class="sxs-lookup"><span data-stu-id="fb7e9-126">By contrast, a page with an equivalent Content Search Web Part, returning the same number of results has an **SPRequestDuration** value of 106 milliseconds as shown in this screen shot:</span></span> 
  
![Capture d’écran montrant la durée de demande de 106](../media/b46387ac-660d-4e5e-a11c-cc430e912962.png)
  
## <a name="adding-a-content-search-web-part-in-sharepoint-online"></a><span data-ttu-id="fb7e9-128">Ajout d’un composant WebPart de recherche de contenu dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="fb7e9-128">Adding a Content Search Web Part in SharePoint Online</span></span>

<span data-ttu-id="fb7e9-129">L’ajout d’un composant WebPart de recherche de contenu est très similaire à un composant WebPart de requête de contenu normal.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-129">Adding a Content Search Web Part is very similar to a regular Content Query Web Part.</span></span> <span data-ttu-id="fb7e9-130">Voir la section  *« Ajouter un composant WebPart de recherche de contenu »*  dans [Configure a Content Search Web part in SharePoint](https://support.office.com/article/Configure-a-Content-Search-Web-Part-in-SharePoint-0dc16de1-dbe4-462b-babb-bf8338c36c9a).</span><span class="sxs-lookup"><span data-stu-id="fb7e9-130">See the section  *"Add a Content Search Web Part"*  in [Configure a Content Search Web Part in SharePoint](https://support.office.com/article/Configure-a-Content-Search-Web-Part-in-SharePoint-0dc16de1-dbe4-462b-babb-bf8338c36c9a).</span></span>
  
## <a name="creating-the-right-search-query-for-your-content-search-web-part"></a><span data-ttu-id="fb7e9-131">Création de la requête de recherche appropriée pour votre composant WebPart de recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="fb7e9-131">Creating the right search query for your Content Search Web Part</span></span>

<span data-ttu-id="fb7e9-132">Une fois que vous avez ajouté un composant WebPart de recherche de contenu, vous pouvez affiner la recherche et renvoyer les éléments de votre choix.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-132">Once you have added a Content Search Web Part, you can refine the search and return the items you want.</span></span> <span data-ttu-id="fb7e9-133">Pour obtenir des instructions détaillées sur la procédure à suivre, voir la section  *« afficher du contenu en configurant une requête avancée dans un composant WebPart recherche de contenu »*  dans [Configure a Content Search Web part in SharePoint](https://support.office.com/article/Configure-a-Content-Search-Web-Part-in-SharePoint-0dc16de1-dbe4-462b-babb-bf8338c36c9a).</span><span class="sxs-lookup"><span data-stu-id="fb7e9-133">For detailed instructions on how to do this, see the section,  *"Display content by configuring an advanced query in a Content Search Web Part"*  in [Configure a Content Search Web Part in SharePoint](https://support.office.com/article/Configure-a-Content-Search-Web-Part-in-SharePoint-0dc16de1-dbe4-462b-babb-bf8338c36c9a).</span></span>
  
## <a name="query-building-and-testing-tool"></a><span data-ttu-id="fb7e9-134">Outil de création et de test de requêtes</span><span class="sxs-lookup"><span data-stu-id="fb7e9-134">Query building and testing tool</span></span>

<span data-ttu-id="fb7e9-135">Pour obtenir un outil permettant de créer et de tester des requêtes complexes, consultez l' [outil de requête de recherche](https://sp2013searchtool.codeplex.com/) sur CodePlex.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-135">For a tool to build and test complex queries, see the [Search Query Tool](https://sp2013searchtool.codeplex.com/) on Codeplex.</span></span> 
  

