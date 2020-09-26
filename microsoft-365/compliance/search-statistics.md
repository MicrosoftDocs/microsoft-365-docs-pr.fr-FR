---
title: Statistiques de recherche
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Les statistiques de recherche sont un moyen efficace de valider les résultats de la recherche et s’affichent sous état sur la page de menu volant détails de la recherche.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 24de99cf0a7ae21b5966811b988c93d64abd5148
ms.sourcegitcommit: 2160e7cf373f992dd4d11793a59cb8c44f8d587e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48286090"
---
# <a name="search-statistics-in-data-investigations-preview"></a><span data-ttu-id="67324-103">Statistiques de recherche dans les enquêtes de données (aperçu)</span><span class="sxs-lookup"><span data-stu-id="67324-103">Search statistics in Data Investigations (preview)</span></span>

<span data-ttu-id="67324-104">Un moyen efficace de valider les résultats de la recherche lors de l’examen d’un incident de données consiste à consulter les statistiques de vos résultats de recherche pour vous assurer qu’ils s’alignent sur vos attentes.</span><span class="sxs-lookup"><span data-stu-id="67324-104">An effective way to validate your search results when investigation a data incident is to view the statistics about your search results to make sure they align with your expectations.</span></span> <span data-ttu-id="67324-105">Une fois la recherche terminée, les statistiques de haut niveau suivantes s’affichent sous **État** sur la page de menu volant des détails de recherche :</span><span class="sxs-lookup"><span data-stu-id="67324-105">When a search as finished running, the following high-level statistics are displayed under **Status** on the search details flyout page:</span></span>

![Page de menu volant de recherche statisics sur les détails de la recherche](../media/SearchDetailsFlyout.png)

- <span data-ttu-id="67324-107">Nombre et taille estimés des éléments correspondant aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="67324-107">The estimated number and size of items that matched the search criteria.</span></span>

- <span data-ttu-id="67324-108">Nombre et taille des éléments partiellement indexés (également appelés *éléments non indexés*) qui ne peuvent pas faire l’objet d’une recherche, mais qui ont été trouvés dans les emplacements de contenu qui ont été inclus dans la recherche.</span><span class="sxs-lookup"><span data-stu-id="67324-108">The number and size of partially indexed items (also called *unindexed items*) that aren't searchable but that were found in the content locations that were included in the search.</span></span>

- <span data-ttu-id="67324-109">Nombre de boîtes aux lettres et de sites ayant fait l’objet d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="67324-109">The number of mailboxes and sites that were searched.</span></span>

<span data-ttu-id="67324-110">Pour afficher des statistiques plus détaillées, cliquez sur **statistiques** sur la page de menu volant détails de la recherche.</span><span class="sxs-lookup"><span data-stu-id="67324-110">To view more detailed statistics, click **Statistics** on the search details flyout page.</span></span> <span data-ttu-id="67324-111">Sur la page **statistiques de recherche** , vous pouvez afficher le résumé de la recherche, l’emplacement du niveau supérieur contenant les éléments qui correspondent aux résultats de la recherche, ainsi que des statistiques détaillées sur la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="67324-111">On the **Search statistics** page, you can view the search summary, the top location that contained items that matched the search results, and detailed statistics about the search query.</span></span>

![Liste déroulante des statistiques de recherche](../media/SearchStatisticsDropDownList.png)

## <a name="summary"></a><span data-ttu-id="67324-113">Résumé</span><span class="sxs-lookup"><span data-stu-id="67324-113">Summary</span></span>

<span data-ttu-id="67324-114">Dans l’affichage de **synthèse** , vous pouvez voir les résultats de la recherche décomposés par type d’emplacement (par exemple, des emplacements de boîtes aux lettres Exchange et des sites SharePoint).</span><span class="sxs-lookup"><span data-stu-id="67324-114">In the **Summary** view, you can see the search results broken down by location type (for example, locations include Exchange mailboxes and SharePoint sites).</span></span> <span data-ttu-id="67324-115">Les informations suivantes s’affichent pour chaque type d’emplacement :</span><span class="sxs-lookup"><span data-stu-id="67324-115">The following information is displayed for each location type:</span></span>

- <span data-ttu-id="67324-116">Nombre d’emplacements qui ont des éléments correspondant aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="67324-116">The number of locations that had items that matched the search criteria.</span></span>

- <span data-ttu-id="67324-117">Nombre total d’éléments de chaque type d’emplacement correspondant aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="67324-117">The total number of items from each location type that matched the search criteria.</span></span>

- <span data-ttu-id="67324-118">Taille totale des éléments de chaque type d’emplacement correspondant aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="67324-118">The total size of items from each location type that matched the search criteria.</span></span>

## <a name="top-locations"></a><span data-ttu-id="67324-119">Emplacements les plus fréquents</span><span class="sxs-lookup"><span data-stu-id="67324-119">Top locations</span></span>

<span data-ttu-id="67324-120">Dans l’affichage des **emplacements de niveau supérieur** , vous pouvez voir les emplacements de contenu individuels avec le plus grand nombre d’éléments correspondant aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="67324-120">In the **Top locations** view, you see the individual content locations with the most items that matched the search criteria.</span></span> <span data-ttu-id="67324-121">Pour chaque emplacement de contenu, les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="67324-121">For each content location, the following information is displayed:</span></span>

- <span data-ttu-id="67324-122">Nom de l’emplacement ; l’adresse de messagerie des boîtes aux lettres et l’URL des sites SharePoint</span><span class="sxs-lookup"><span data-stu-id="67324-122">The name of the location; the email address for mailboxes and the URL for SharePoint sites</span></span>

- <span data-ttu-id="67324-123">Type d’emplacement</span><span class="sxs-lookup"><span data-stu-id="67324-123">The location type</span></span>

- <span data-ttu-id="67324-124">Nombre d’éléments correspondant aux critères de recherche</span><span class="sxs-lookup"><span data-stu-id="67324-124">Number of items that matched the search criteria</span></span>

- <span data-ttu-id="67324-125">Taille totale de tous les éléments correspondant aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="67324-125">The total size of all items that matched the search criteria.</span></span>

## <a name="queries"></a><span data-ttu-id="67324-126">Requêtes</span><span class="sxs-lookup"><span data-stu-id="67324-126">Queries</span></span>

<span data-ttu-id="67324-127">Dans l’affichage **requêtes** , vous pouvez afficher des statistiques détaillées pour chaque composant de la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="67324-127">In the **Queries** view, you can see detailed statistics for each component of the search query.</span></span> <span data-ttu-id="67324-128">Si vous avez utilisé la liste de mots clés dans la requête de recherche, vous pouvez afficher les statistiques améliorées dans l’affichage **requêtes** qui indiquent le nombre d’éléments qui correspondent à chaque mot clé ou expression de mot clé.</span><span class="sxs-lookup"><span data-stu-id="67324-128">If you used the keyword list in the search query, you can view enhanced statistics in the **Queries** view  that show how many items match each keyword or keyword phrase.</span></span> <span data-ttu-id="67324-129">Cela peut vous aider à identifier rapidement les parties de la requête qui sont les plus efficaces (et les moins).</span><span class="sxs-lookup"><span data-stu-id="67324-129">This can help you quickly identify which parts of the query are the most (and least) effective.</span></span> 

<span data-ttu-id="67324-130">Les informations suivantes sont affichées dans l’affichage **requêtes** :</span><span class="sxs-lookup"><span data-stu-id="67324-130">The following information is displayed in the **Queries** view:</span></span>

 - <span data-ttu-id="67324-131">**Type d’emplacement** : type d’emplacement de contenu pour les statistiques affichées dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="67324-131">**Location type** - The type of content location for the statistics displayed in the row.</span></span>

- <span data-ttu-id="67324-132">**Partie** : cette colonne affiche l’une des valeurs suivantes : **Primary** ou **Keyword**.</span><span class="sxs-lookup"><span data-stu-id="67324-132">**Part** - This column will display one of the following values: **Primary** or **Keyword**.</span></span> <span data-ttu-id="67324-133">**Principal** signifie que la ligne présente des statistiques sur l’ensemble de la requête ; **Mot clé** signifie que les statistiques de la ligne sont pour l’un des composants de requête.</span><span class="sxs-lookup"><span data-stu-id="67324-133">**Primary** means the row presents statistics on the entire query; **Keyword** means the statistics in the row are for one of the query components.</span></span>

- <span data-ttu-id="67324-134">**Condition** : composant de requête réel de la requête de recherche à laquelle la ligne fait référence.</span><span class="sxs-lookup"><span data-stu-id="67324-134">**Condition** - The actual query component of the search query the row refers to.</span></span> <span data-ttu-id="67324-135">Si la valeur dans la colonne **composant** est **principale**, les statistiques de l’ensemble de la requête de recherche sont affichées ; Si la valeur est **mot clé**, les statistiques du composant de la requête affichée dans la colonne **requête** sont affichées.</span><span class="sxs-lookup"><span data-stu-id="67324-135">If the value in the **Part** column is **Primary**, then the statistics for the entire search query are displayed; if the value is **Keyword**, then the statistics for the component of the query shown in the **Query** column are displayed.</span></span> <span data-ttu-id="67324-136">Par exemple, si la liste de mots-clés a été utilisée, les statistiques l’un des mots-clés sont affichés.</span><span class="sxs-lookup"><span data-stu-id="67324-136">For example, if the keyword list was used, then the statistics one of the keywords are displayed.</span></span>

  <span data-ttu-id="67324-137">Voici quelques autres éléments à connaître concernant les statistiques affichées dans la colonne **requêtes** :</span><span class="sxs-lookup"><span data-stu-id="67324-137">Here are some other things to know about the statistics displayed in the **Queries** column:</span></span>
  
  - <span data-ttu-id="67324-138">Lorsque vous recherchez tout le contenu dans des boîtes aux lettres (en ne spécifiant aucun mot-clé), la requête réelle est **(taille >= 0)** de sorte que tous les éléments soient renvoyés.</span><span class="sxs-lookup"><span data-stu-id="67324-138">When you search for all content in mailboxes (by not specifying any keywords), the actual query is **(size >= 0)** so that all items are returned</span></span>
  
  - <span data-ttu-id="67324-139">Lorsque vous effectuez des recherches dans des sites SharePoint et OneDrive, les deux composants suivants sont ajoutés à la requête de recherche :</span><span class="sxs-lookup"><span data-stu-id="67324-139">When you search SharePoint and OneDrive sites, the two following components are added to the search query:</span></span>
    
    <span data-ttu-id="67324-140">**Non IsExternalContent : 1** -cela exclut le contenu d’une organisation SharePoint locale</span><span class="sxs-lookup"><span data-stu-id="67324-140">**NOT IsExternalContent:1** - This excludes any content from an on-premises SharePoint organization</span></span>
    
    <span data-ttu-id="67324-141">**Non isOneNotePage : 1** -cela exclut tous les fichiers OneNote, car il s’agit de doublons de tous les documents qui correspondent à la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="67324-141">**NOT isOneNotePage:1** - This excludes all OneNote files because these would be duplicates of any document that matches the search query.</span></span>

- <span data-ttu-id="67324-142">**Emplacements dans la recherche** Nombre d’emplacements de contenu contenant des éléments qui correspondent à la requête de recherche pour la partie ou la condition affichée dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="67324-142">**Locations in search** The number of content locations that had items that matched the search query for the part/condition displayed in the row.</span></span> <span data-ttu-id="67324-143">Notez que les boîtes aux lettres d’archivage sont comptabilisées comme un emplacement distinct si elles contiennent des éléments qui correspondent aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="67324-143">Note that archive mailboxes are counted as a separate location if they contain items that match the search criteria.</span></span>

- <span data-ttu-id="67324-144">**Items** : nombre total d’éléments correspondant aux critères de recherche pour le composant ou la condition affiché dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="67324-144">**Items** - The total number of items that matched the search criteria for the part/condition displayed in the row.</span></span>

- <span data-ttu-id="67324-145">**Size** : nombre total d’éléments correspondant aux critères de recherche pour le composant ou la condition affiché dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="67324-145">**Size** - The total number of items that matched the search criteria for the part/condition displayed in the row.</span></span>

