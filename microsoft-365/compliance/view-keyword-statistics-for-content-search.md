---
title: Afficher des statistiques pour les résultats de recherche eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.search: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
description: Découvrez comment utiliser la fonctionnalité statistiques de recherche pour afficher des statistiques pour les recherches de contenu et les recherches associées à un cas eDiscovery principal dans le centre de conformité Microsoft 365 de recherche.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: a0e543c89b91560520a4e4bf31feb8471c91da4a
ms.sourcegitcommit: efb932db63ad3ab4af4b585428d567d069410e4e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2021
ms.locfileid: "52311095"
---
# <a name="view-statistics-for-ediscovery-search-results"></a><span data-ttu-id="7c6ba-103">Afficher des statistiques pour les résultats de recherche eDiscovery</span><span class="sxs-lookup"><span data-stu-id="7c6ba-103">View statistics for eDiscovery search results</span></span>

<span data-ttu-id="7c6ba-104">Après avoir créé et exécuté une recherche de contenu ou une recherche associée à un cas core eDiscovery, vous pouvez afficher des statistiques sur les résultats de recherche estimés.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-104">After you create and run a Content search or a search associated with a Core eDiscovery case, you can view statistics about the estimated search results.</span></span> <span data-ttu-id="7c6ba-105">Cela inclut un résumé des résultats de recherche (semblable au résumé des résultats de recherche estimés affichés sur la page volante de recherche), les statistiques de requête telles que le nombre d’emplacements de contenu avec des éléments qui correspondent à la requête de recherche et l’identité des emplacements de contenu qui ont le plus d’éléments correspondants.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-105">This includes a summary of the search results (similar to the summary of the estimated search results displayed on the search flyout page), the query statistics such as the number of content locations with items that match the search query, and the identity of content locations that have the most matching items.</span></span>
  
<span data-ttu-id="7c6ba-106">En outre, vous pouvez utiliser la liste de mots clés pour configurer une recherche afin de renvoyer des statistiques pour chaque mot clé dans une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-106">Additionally, you can use the keywords list to configure a search to return statistics for each keyword in a search query.</span></span> <span data-ttu-id="7c6ba-107">Cela vous permet de comparer le nombre de résultats renvoyés par chaque mot clé dans une requête.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-107">This lets you compare the number of results returned by each keyword in a query.</span></span>
  
<span data-ttu-id="7c6ba-108">Vous pouvez également télécharger des statistiques de recherche dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-108">You can also download search statistics to a CSV file.</span></span> <span data-ttu-id="7c6ba-109">Cela vous permet d’utiliser les fonctionnalités de filtrage et de tri dans Excel pour comparer les résultats et préparer des rapports pour vos résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-109">This lets you use the filtering and sorting features in Excel to compare results, and prepare reports for your search results.</span></span>
  
## <a name="get-statistics-for-searches"></a><span data-ttu-id="7c6ba-110">Obtenir des statistiques pour les recherches</span><span class="sxs-lookup"><span data-stu-id="7c6ba-110">Get statistics for searches</span></span>

<span data-ttu-id="7c6ba-111">Pour afficher des statistiques pour une recherche de contenu ou une recherche associée à un cas de découverte électronique principale :</span><span class="sxs-lookup"><span data-stu-id="7c6ba-111">To display statistics for a Content search or a search associated with a Core eDiscovery case.:</span></span>
  
1. <span data-ttu-id="7c6ba-112">Dans le centre Microsoft 365 conformité, cliquez sur **Afficher tout,** puis faites l’une des choses suivantes :</span><span class="sxs-lookup"><span data-stu-id="7c6ba-112">In the Microsoft 365 compliance center, click **Show all**, and then do one of the following:</span></span>

   - <span data-ttu-id="7c6ba-113">Cliquez **sur Recherche de** contenu, puis sélectionnez une recherche pour afficher la page volante.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-113">Click **Content search** and then select a search to display the flyout page.</span></span>

     <span data-ttu-id="7c6ba-114">OU</span><span class="sxs-lookup"><span data-stu-id="7c6ba-114">OR</span></span>

   - <span data-ttu-id="7c6ba-115">Cliquez **sur eDiscovery** Core, sélectionnez un cas, puis sélectionnez une recherche sous l’onglet Recherches pour afficher  >  la page volante. </span><span class="sxs-lookup"><span data-stu-id="7c6ba-115">Click **eDiscovery** > **Core**, select a case, and then select a search on the **Searches** tab to display the flyout page.</span></span>

2. <span data-ttu-id="7c6ba-116">Dans la page volante de la recherche sélectionnée, cliquez sur l’onglet **Statistiques de** recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-116">On the flyout page of the selected search, click the **Search statistics** tab.</span></span>
  
   ![Onglet Statistiques de recherche](../media/SearchStatistics1.png)

<span data-ttu-id="7c6ba-118">**L’onglet Statistiques** de recherche contient les sections suivantes qui contiennent différents types de statistiques sur la recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-118">The **Search statistics** tab contains for following sections that contain different types of statistics about the search.</span></span>

### <a name="search-content"></a><span data-ttu-id="7c6ba-119">Rechercher du contenu</span><span class="sxs-lookup"><span data-stu-id="7c6ba-119">Search content</span></span>

<span data-ttu-id="7c6ba-120">Cette section affiche un résumé graphique des éléments estimés renvoyés par la recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-120">This section displays a graphical summary of the estimated items returned by the search.</span></span> <span data-ttu-id="7c6ba-121">Cela indique le nombre d’éléments qui correspondent aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-121">This indicates the number of items that match the search criteria.</span></span> <span data-ttu-id="7c6ba-122">Ces informations vous donnent une idée du nombre estimé d’éléments renvoyés par la recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-122">This information gives you an idea about the estimated number of items returned by the search.</span></span>

![Estimations de recherche pour une recherche](../media/SearchContentReport.png)

- <span data-ttu-id="7c6ba-124">**Éléments estimés par emplacement**: nombre total d’éléments estimés renvoyés par la recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-124">**Estimated items by locations**: The total number of estimated items returned by the search.</span></span> <span data-ttu-id="7c6ba-125">Le nombre spécifique d’éléments situés dans des boîtes aux lettres et dans des sites est également affiché.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-125">The specific number of items located in mailboxes and located in sites is also displayed.</span></span>

- <span data-ttu-id="7c6ba-126">**Emplacements estimés avec occurrences**: nombre total d’emplacements de contenu qui contiennent des éléments renvoyés par la recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-126">**Estimated locations with hits**: The total number of content locations that contain items returned by the search.</span></span> <span data-ttu-id="7c6ba-127">Le nombre spécifique d’emplacements de boîtes aux lettres et de sites est également affiché.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-127">The specific number of mailbox and site locations is also displayed.</span></span>

- <span data-ttu-id="7c6ba-128">**Volume de données par emplacement (en Mo)**: taille totale de tous les éléments estimés renvoyés par la recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-128">**Data volume by location (in MB)**: The total size of all estimated items returned by the search.</span></span> <span data-ttu-id="7c6ba-129">La taille spécifique des éléments de boîte aux lettres et des éléments de site est également affichée.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-129">The specific size of mailbox items and site items is also displayed.</span></span>

### <a name="condition-report"></a><span data-ttu-id="7c6ba-130">Rapport de condition</span><span class="sxs-lookup"><span data-stu-id="7c6ba-130">Condition report</span></span>

<span data-ttu-id="7c6ba-131">Cette section affiche des statistiques sur la requête de recherche et le nombre d’éléments estimés qui correspondent à différentes parties de la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-131">This section displays statistics about the search query and the number of estimated items that matched different parts of the search query.</span></span> <span data-ttu-id="7c6ba-132">Vous pouvez utiliser ces statistiques pour analyser le nombre d’éléments qui correspondent à chaque composant de la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-132">You can use these statistics to analyze the number of items that match each component of search query.</span></span> <span data-ttu-id="7c6ba-133">Cela peut vous aider à affiner les critères de recherche et, si nécessaire, à affiner l’étendue de l’étendue.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-133">This can help you refine the search criteria and if necessary narrow the scope of the scope.</span></span> <span data-ttu-id="7c6ba-134">Vous pouvez également télécharger une copie de ce rapport au format CSV.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-134">You can also download a copy of this report in CSV format.</span></span>

![Rapport de condition](../media/SearchContentReportNoKeywordList.png)

- <span data-ttu-id="7c6ba-136">**Type d’emplacement**: type d’emplacement de contenu applicable aux statistiques de requête.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-136">**Location type**: The type of content location that the query statistics are applicable to.</span></span> <span data-ttu-id="7c6ba-137">La valeur **de** Exchange indique un emplacement de boîte aux lettres ; une valeur de **SharePoint** indique un emplacement de site.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-137">The value of **Exchange** indicates a mailbox location; a value of **SharePoint** indicates a site location.</span></span>

- <span data-ttu-id="7c6ba-138">**Partie**: partie de la requête de recherche à qui les statistiques s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-138">**Part**: The part of the search query the statistics are applicable to.</span></span> <span data-ttu-id="7c6ba-139">**Primary** indique l’intégralité de la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-139">**Primary** indicates the entire search query.</span></span> <span data-ttu-id="7c6ba-140">**Le** mot clé indique que les statistiques de la ligne sont pour un mot clé spécifique.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-140">**Keyword** indicates the statistics in the row are for a specific keyword.</span></span> <span data-ttu-id="7c6ba-141">Si vous utilisez une liste de mots clés pour la requête de recherche, les statistiques de chaque composant de la requête sont incluses dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-141">If you use a keyword list for search query, statistics for each component of the query are included in this table.</span></span> <span data-ttu-id="7c6ba-142">Pour plus d’informations, voir [Obtenir des statistiques sur les mots clés pour les recherches.](#get-keyword-statistics-for-searches)</span><span class="sxs-lookup"><span data-stu-id="7c6ba-142">For more information, see [Get keyword statistics for searches](#get-keyword-statistics-for-searches).</span></span>

- <span data-ttu-id="7c6ba-143">**Condition**: composant réel (mot clé ou condition) de la requête de recherche qui a renvoyé les statistiques affichées dans la ligne correspondante.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-143">**Condition**: The actual component (keyword or condition) of the search query that returned the statistics displayed in the corresponding row.</span></span>

- <span data-ttu-id="7c6ba-144">**Emplacements** avec accès : nombre d’emplacements de contenu (spécifiés par la colonne **Type** d’emplacement) qui contiennent des éléments qui correspondent à la requête principale ou de mot clé répertoriée dans la colonne **Condition.**</span><span class="sxs-lookup"><span data-stu-id="7c6ba-144">**Locations with hits**: The number of the content locations (specified by the **Location type** column) that contain items that match the primary or keyword query listed in the **Condition** column.</span></span>

- <span data-ttu-id="7c6ba-145">**Éléments**: nombre d’éléments (à partir de l’emplacement de contenu spécifié) qui correspondent à la requête répertoriée dans la **colonne Condition.**</span><span class="sxs-lookup"><span data-stu-id="7c6ba-145">**Items**: The number of items (from the specified content location) that match the query listed in the **Condition** column.</span></span> <span data-ttu-id="7c6ba-146">Comme indiqué précédemment, si un élément contient plusieurs instances d’un mot clé recherché, il n’est compté qu’une seule fois dans cette colonne.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-146">As previously explained, if an item contains multiple instances of a keyword that is being searched for, it's only counted once in this column.</span></span>

- <span data-ttu-id="7c6ba-147">**Taille (Mo)**: taille totale de tous les éléments trouvés (à l’emplacement de contenu spécifié) qui correspondent à la requête de recherche dans la colonne **Condition.**</span><span class="sxs-lookup"><span data-stu-id="7c6ba-147">**Size (MB)**: The total size of all items that were found (in the specified content location) that match the search query in the **Condition** column.</span></span>

### <a name="top-locations"></a><span data-ttu-id="7c6ba-148">Emplacements principaux</span><span class="sxs-lookup"><span data-stu-id="7c6ba-148">Top locations</span></span>

<span data-ttu-id="7c6ba-149">Cette section affiche des statistiques sur les emplacements de contenu spécifiques avec le plus d’éléments renvoyés par la recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-149">This section displays statistics about the specific content locations with the most items returned by the search.</span></span> <span data-ttu-id="7c6ba-150">Les 1 000 principaux emplacements sont affichés.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-150">The top 1,000 locations are displayed.</span></span> <span data-ttu-id="7c6ba-151">Vous pouvez également télécharger une copie de ce rapport au format CSV.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-151">You can also download a copy of this report in CSV format.</span></span>

- <span data-ttu-id="7c6ba-152">Nom du nom de l’emplacement (adresse de messagerie des boîtes aux lettres et URL des sites).</span><span class="sxs-lookup"><span data-stu-id="7c6ba-152">The name of the location name (the email address of mailboxes and the URL for sites).</span></span>

- <span data-ttu-id="7c6ba-153">Type d’emplacement (boîte aux lettres ou site).</span><span class="sxs-lookup"><span data-stu-id="7c6ba-153">Location type (a mailbox or site).</span></span>

- <span data-ttu-id="7c6ba-154">Nombre estimé d’éléments dans l’emplacement de contenu renvoyé par la recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-154">Estimated number of items in the content location returned by the search.</span></span>

- <span data-ttu-id="7c6ba-155">Taille totale des éléments estimés dans chaque emplacement de contenu.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-155">The total size of estimated items in each content location.</span></span>

## <a name="get-keyword-statistics-for-searches"></a><span data-ttu-id="7c6ba-156">Obtenir des statistiques sur les mots clés pour les recherches</span><span class="sxs-lookup"><span data-stu-id="7c6ba-156">Get keyword statistics for searches</span></span>

<span data-ttu-id="7c6ba-157">Comme expliqué précédemment, la section **Rapport de condition** affiche la requête de recherche et le nombre (et la taille) d’éléments qui correspondent à la requête.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-157">As previous explained, the **Condition report** section shows the search query and the number (and size) of items that match the query.</span></span> <span data-ttu-id="7c6ba-158">Si vous utilisez une liste de mots clés lorsque vous créez ou modifiez une requête de recherche, vous pouvez obtenir des statistiques améliorées qui indiquent le nombre d’éléments qui correspondent à chaque mot clé ou expression de mot clé.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-158">If you use a keyword list when you create or edit a search query, you can get enhanced statistics that show how many items match each keyword or keyword phrase.</span></span> <span data-ttu-id="7c6ba-159">Cela peut vous aider à identifier rapidement les parties de la requête qui sont les plus (et les moins) efficaces.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-159">This can help you quickly identify which parts of the query are the most (and least) effective.</span></span> <span data-ttu-id="7c6ba-160">Par exemple, si un mot clé renvoie un grand nombre d’éléments, vous pouvez choisir d’affiner la requête de mot clé pour affiner les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-160">For example, if a keyword returns a large number of items, you might choose to refine the keyword query to narrow the search results.</span></span>

<span data-ttu-id="7c6ba-161">Pour créer une liste de mots clés et afficher des statistiques de mots clés pour une recherche :</span><span class="sxs-lookup"><span data-stu-id="7c6ba-161">To create a keyword list and view keyword statistics for a search:</span></span>
  
1. <span data-ttu-id="7c6ba-162">Dans le centre Microsoft 365 conformité, créez une recherche de contenu ou une recherche associée à un cas eDiscovery principal.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-162">In the Microsoft 365 compliance center, create a new Content search or a search associated with a Core eDiscovery case.</span></span>

2. <span data-ttu-id="7c6ba-163">Dans la page **Conditions** de l’Assistant Recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-163">On the **Conditions** page of the search wizard.</span></span> <span data-ttu-id="7c6ba-164">cochez la **case Afficher la liste des** mots clés.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-164">select the **Show keyword list** checkbox.</span></span>

   ![Afficher la case à cocher liste des mots clés](../media/SearchKeywordsList1.png)

3. <span data-ttu-id="7c6ba-166">Tapez une phase de mot clé ou de mot clé dans une ligne du tableau des mots clés.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-166">Type a keyword or keyword phase in a row in the keywords table.</span></span> <span data-ttu-id="7c6ba-167">Par exemple, tapez **budget** sur la première ligne, **tapez** sécurité dans la deuxième ligne et tapez **FY2021** dans la troisième ligne.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-167">For example, type **budget** in the first row, type **security** in the second row, and type **FY2021** in the third row.</span></span>

   ![Tapez jusqu’à 20 mots clés ou expressions de mots clés dans la liste](../media/SearchKeywordsList2.png)

   > [!NOTE]
   > <span data-ttu-id="7c6ba-169">Pour réduire les problèmes causés par les grandes listes de mots clés, vous êtes limité à 20 lignes au maximum dans la liste de mots clés d’une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-169">To help reduce issues caused by large keyword lists, you're limited to a maximum of 20 rows in the keyword list of a search query.</span></span>

4. <span data-ttu-id="7c6ba-170">Après avoir ajouté les mots clés à la liste dont vous souhaitez rechercher et obtenir des statistiques, exécutez la recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-170">After adding the keywords to the list that you want to search and get statistics for, run the search.</span></span>

5. <span data-ttu-id="7c6ba-171">Lorsque la recherche est terminée, sélectionnez-la pour afficher la page volante.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-171">When the search is completed, select it to display the flyout page.</span></span>

6. <span data-ttu-id="7c6ba-172">Sous **l’onglet Statistiques de** recherche, cliquez sur le rapport **de condition** pour afficher les statistiques de mot clé pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-172">On the **Search statistics** tab, click the **Condition report** to display the keyword statistics for the search.</span></span>

    ![Les statistiques de chaque mot clé sont affichées](../media/SearchKeywordsList3.png)
  
    <span data-ttu-id="7c6ba-174">Comme indiqué dans la capture d’écran précédente, les statistiques de chaque mot clé sont affichées . Cela inclut :</span><span class="sxs-lookup"><span data-stu-id="7c6ba-174">As shown in the previous screenshot, the statistics for each keyword are displayed; this includes:</span></span>

    - <span data-ttu-id="7c6ba-175">Statistiques de mots clés pour chaque type d’emplacement de contenu inclus dans la recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-175">The keyword statistics for each type of content location included in the search.</span></span>

    - <span data-ttu-id="7c6ba-176">Nombre d’éléments de boîte aux lettres nonndex.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-176">The number of unindexed mailbox items.</span></span>

    - <span data-ttu-id="7c6ba-177">Requête et résultats de recherche réels  pour chaque mot clé (identifié comme mot clé dans la colonne **Part),** qui inclut toutes les conditions de la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-177">The actual search query and results for each keyword (identified as **Keyword** in the **Part** column), which includes any conditions from the search query.</span></span>

    - <span data-ttu-id="7c6ba-178">Requête de recherche complète  (identifiée comme principale dans la colonne **Partie)** et statistiques de la requête complète pour chaque type d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-178">The complete search query (identified as **Primary** in the **Part** column) and the statistics for the complete query for each location type.</span></span> <span data-ttu-id="7c6ba-179">Notez que ces statistiques sont les mêmes que celles affichées sous **l’onglet** Résumé.</span><span class="sxs-lookup"><span data-stu-id="7c6ba-179">Note these are the same statistics displayed on the **Summary** tab.</span></span>
