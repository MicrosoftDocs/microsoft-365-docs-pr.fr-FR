---
title: Collecter des données pour un cas dans Advanced eDiscovery
ms.author: esclee
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
ms.assetid: ''
description: ''
ms.openlocfilehash: 4e0bc71071ecfe20a2141e72b1146e9688618faf
ms.sourcegitcommit: e386037c9cc335c86896dc153344850735afbccd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2019
ms.locfileid: "39633603"
---
# <a name="collect-data-for-a-case-in-advanced-ediscovery"></a><span data-ttu-id="eafe7-102">Collecter des données pour un cas dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="eafe7-102">Collect data for a case in Advanced eDiscovery</span></span>

<span data-ttu-id="eafe7-103">Une fois que vous avez identifié les dépositaires et les sources de données intéressantes pour votre cas, il est temps d’identifier l’ensemble des documents dans lesquels vous souhaitez approfondir votre attention.</span><span class="sxs-lookup"><span data-stu-id="eafe7-103">Once you've identified custodians and data sources that are of interest for your case, it's time to identify the set of documents to delve into.</span></span> <span data-ttu-id="eafe7-104">Vous pouvez utiliser l’outil de recherche dans Advanced eDiscovery pour les identifier à des endroits privatives et non privatives dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="eafe7-104">You can use the Search tool in Advanced eDiscovery to identify these from custodial and non-custodial locations in Office 365.</span></span>

<span data-ttu-id="eafe7-105">Après avoir exécuté une recherche, vous pouvez afficher des statistiques sur les éléments récupérés, tels que les emplacements qui ont le plus d’éléments qui correspondent à la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="eafe7-105">After you run a search, you can view statistics on the retrieved items, such as the locations that had the most items that matched the search query.</span></span> <span data-ttu-id="eafe7-106">Vous pouvez également afficher un aperçu d’un sous-ensemble des résultats.</span><span class="sxs-lookup"><span data-stu-id="eafe7-106">You can also preview a subset of the results.</span></span> <span data-ttu-id="eafe7-107">Une fois que vous avez identifié l’ensemble de documents que vous souhaitez examiner, vous pouvez ajouter les résultats de la recherche à un jeu de vérification pour le collecter et le traiter.</span><span class="sxs-lookup"><span data-stu-id="eafe7-107">When you've identified the set of documents you want to further examine, you can add the search results to a review set to collect and process.</span></span>

## <a name="create-a-search"></a><span data-ttu-id="eafe7-108">Créer une recherche</span><span class="sxs-lookup"><span data-stu-id="eafe7-108">Create a search</span></span>

<span data-ttu-id="eafe7-109">La sélection de **nouvelle recherche** sous l’onglet **recherches** démarre un assistant qui vous guide tout au long de la procédure de création d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="eafe7-109">Selecting **New search** on the **Searches** tab will start a wizard that guides you through creating a search.</span></span> <span data-ttu-id="eafe7-110">Pour plus d’informations sur la création d’une recherche, voir [Create a Search to Collect Data](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="eafe7-110">For detailed information on how to create a search, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="eafe7-111">Après la création d’une recherche, une page de menu volant contenant des informations s’affiche.</span><span class="sxs-lookup"><span data-stu-id="eafe7-111">After a search is created, a flyout page with details is displayed.</span></span> <span data-ttu-id="eafe7-112">Les **statistiques** et les boutons d' **Aperçu** sont initialement indisponibles car la recherche n’a pas encore été effectuée.</span><span class="sxs-lookup"><span data-stu-id="eafe7-112">The **Statistics** and **Preview** buttons are initially unavailable because the search hasn't completed yet.</span></span> <span data-ttu-id="eafe7-113">Vous pouvez suivre la progression de la recherche dans l’onglet **recherches** .</span><span class="sxs-lookup"><span data-stu-id="eafe7-113">You can keep track of the progress of the search on the **Searches** tab.</span></span>

## <a name="view-search-results-and-statistics"></a><span data-ttu-id="eafe7-114">Afficher les statistiques et les résultats de la recherche</span><span class="sxs-lookup"><span data-stu-id="eafe7-114">View search results and statistics</span></span>

<span data-ttu-id="eafe7-115">Il existe deux composants d’une recherche de contenu : statistiques (estimations) et aperçu.</span><span class="sxs-lookup"><span data-stu-id="eafe7-115">There are two components of a content search: Statistics (Estimates) and Preview.</span></span> <span data-ttu-id="eafe7-116">À mesure que chacun de ces composants est terminé, l’état affiché dans les colonnes correspondantes de l’onglet **recherches** passe de **soumis** à **en cours** à **terminé**.</span><span class="sxs-lookup"><span data-stu-id="eafe7-116">As each of these components complete, you'll see the status displayed in the corresponding columns on the **Searches** tab change from **Submitted** to **In progress** to **Completed**.</span></span>

<span data-ttu-id="eafe7-117">Une fois l’estimation de la recherche terminée, sélectionnez la recherche pour afficher la page de menu volant, qui affiche certaines statistiques de haut niveau sur les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="eafe7-117">Once the search estimate is completed, select the search to display the flyout page, which will display some high-level statistics about the results of the search.</span></span> <span data-ttu-id="eafe7-118">À ce stade, le bouton **statistiques** est actif.</span><span class="sxs-lookup"><span data-stu-id="eafe7-118">At this point, the **Statistics** button will be active.</span></span> <span data-ttu-id="eafe7-119">Vous pouvez le sélectionner pour afficher les statistiques de recherche, telles que :</span><span class="sxs-lookup"><span data-stu-id="eafe7-119">You can select it to see search statistics, such as:</span></span>

- <span data-ttu-id="eafe7-120">Résumé</span><span class="sxs-lookup"><span data-stu-id="eafe7-120">Summary</span></span>
- <span data-ttu-id="eafe7-121">Emplacements les plus fréquents</span><span class="sxs-lookup"><span data-stu-id="eafe7-121">Top locations</span></span>
- <span data-ttu-id="eafe7-122">Requêtes</span><span class="sxs-lookup"><span data-stu-id="eafe7-122">Queries</span></span>

<span data-ttu-id="eafe7-123">Pour plus d’informations sur les statistiques de recherche, voir statistiques de la [recherche](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="eafe7-123">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

<span data-ttu-id="eafe7-124">Une fois l’aperçu terminé, le bouton **Aperçu** est actif.</span><span class="sxs-lookup"><span data-stu-id="eafe7-124">Once preview is completed, the **Preview** button will be active.</span></span> <span data-ttu-id="eafe7-125">Sélectionnez-le pour afficher un aperçu d’un sous-ensemble de résultats.</span><span class="sxs-lookup"><span data-stu-id="eafe7-125">Select it to preview a sampled subset of the results.</span></span>

## <a name="adding-search-results-to-a-review-set"></a><span data-ttu-id="eafe7-126">Ajout de résultats de recherche à un jeu de révision</span><span class="sxs-lookup"><span data-stu-id="eafe7-126">Adding search results to a review set</span></span>

<span data-ttu-id="eafe7-127">Lorsque vous êtes prêt à collecter et à traiter tous les résultats d’une recherche, vous pouvez le faire en l’ajoutant à un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="eafe7-127">When you're ready to collect and process the entire results of a search, you can do so by adding it to a review set.</span></span> <span data-ttu-id="eafe7-128">Pour plus d’informations, consultez [la rubrique ajouter des données à un jeu de vérification](add-data-to-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="eafe7-128">For details, see [Add data to a review set](add-data-to-review-set.md).</span></span>
