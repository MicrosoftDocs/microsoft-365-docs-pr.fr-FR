---
title: Collecter des données pour un cas dans Advanced eDiscovery
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
ms.assetid: ''
description: Découvrez comment identifier un ensemble de documents à consulter lors d’une enquête à l’aide de l’outil de recherche dans Advanced eDiscovery.
ms.custom: seo-marvel-2020
ms.openlocfilehash: b69127f1a372a9b843b9c7dac1b2909dd80b2988
ms.sourcegitcommit: 98b889e674ad1d5fa37d4b6c5fc3eda60a1d67f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2021
ms.locfileid: "49751265"
---
# <a name="collect-data-for-a-case-in-advanced-ediscovery"></a><span data-ttu-id="b641f-103">Collecter des données pour un cas dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="b641f-103">Collect data for a case in Advanced eDiscovery</span></span>

<span data-ttu-id="b641f-104">Une fois que vous avez identifié les dépositaires et les sources de données intéressantes pour votre cas, il est temps d’identifier l’ensemble des documents dans lesquels vous souhaitez approfondir votre attention.</span><span class="sxs-lookup"><span data-stu-id="b641f-104">Once you've identified custodians and data sources that are of interest for your case, it's time to identify the set of documents to delve into.</span></span> <span data-ttu-id="b641f-105">Vous pouvez utiliser l’outil de recherche dans Advanced eDiscovery pour identifier les documents pertinents d’une absence ou d’une absence privative de marchés dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b641f-105">You can use the Search tool in Advanced eDiscovery to identify relevant documents from custodial and non-custodial locations in Microsoft 365.</span></span>

<span data-ttu-id="b641f-106">Après avoir exécuté une recherche, vous pouvez afficher des statistiques sur les éléments récupérés, tels que les emplacements qui ont le plus d’éléments qui correspondent à la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="b641f-106">After you run a search, you can view statistics on the retrieved items, such as the locations that had the most items that matched the search query.</span></span> <span data-ttu-id="b641f-107">Vous pouvez également afficher un aperçu d’un sous-ensemble des résultats.</span><span class="sxs-lookup"><span data-stu-id="b641f-107">You can also preview a subset of the results.</span></span> <span data-ttu-id="b641f-108">Une fois que vous avez identifié l’ensemble de documents que vous souhaitez examiner, vous pouvez ajouter les résultats de la recherche à un jeu de vérification pour le collecter et le traiter.</span><span class="sxs-lookup"><span data-stu-id="b641f-108">When you've identified the set of documents you want to further examine, you can add the search results to a review set to collect and process.</span></span>

## <a name="create-a-search"></a><span data-ttu-id="b641f-109">Créer une recherche</span><span class="sxs-lookup"><span data-stu-id="b641f-109">Create a search</span></span>

<span data-ttu-id="b641f-110">La sélection de **nouvelle recherche** sous l’onglet **recherches** démarre un assistant qui vous guide tout au long de la procédure de création d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="b641f-110">Selecting **New search** on the **Searches** tab will start a wizard that guides you through creating a search.</span></span> <span data-ttu-id="b641f-111">Pour plus d’informations sur la création d’une recherche, voir [Create a Search to Collect Data](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="b641f-111">For detailed information on how to create a search, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="b641f-112">Après la création d’une recherche, une page de menu volant contenant des informations s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b641f-112">After a search is created, a flyout page with details is displayed.</span></span> <span data-ttu-id="b641f-113">Les **statistiques** et les boutons d' **Aperçu** sont initialement indisponibles car la recherche n’a pas encore été effectuée.</span><span class="sxs-lookup"><span data-stu-id="b641f-113">The **Statistics** and **Preview** buttons are initially unavailable because the search hasn't completed yet.</span></span> <span data-ttu-id="b641f-114">Vous pouvez suivre la progression de la recherche dans l’onglet **recherches** .</span><span class="sxs-lookup"><span data-stu-id="b641f-114">You can keep track of the progress of the search on the **Searches** tab.</span></span>

## <a name="view-search-results-and-statistics"></a><span data-ttu-id="b641f-115">Afficher les statistiques et les résultats de la recherche</span><span class="sxs-lookup"><span data-stu-id="b641f-115">View search results and statistics</span></span>

<span data-ttu-id="b641f-116">Il existe deux composants d’une recherche de contenu : statistiques (estimations) et aperçu.</span><span class="sxs-lookup"><span data-stu-id="b641f-116">There are two components of a content search: Statistics (Estimates) and Preview.</span></span> <span data-ttu-id="b641f-117">À mesure que chacun de ces composants est terminé, l’état affiché dans les colonnes correspondantes de l’onglet **recherches** passe de **soumis** à **en cours** à **terminé**.</span><span class="sxs-lookup"><span data-stu-id="b641f-117">As each of these components complete, you'll see the status displayed in the corresponding columns on the **Searches** tab change from **Submitted** to **In progress** to **Completed**.</span></span>

<span data-ttu-id="b641f-118">Une fois l’estimation de la recherche terminée, sélectionnez la recherche pour afficher la page de menu volant, qui affiche certaines statistiques de haut niveau sur les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="b641f-118">Once the search estimate is completed, select the search to display the flyout page, which will display some high-level statistics about the results of the search.</span></span> <span data-ttu-id="b641f-119">À ce stade, le bouton **statistiques** est actif.</span><span class="sxs-lookup"><span data-stu-id="b641f-119">At this point, the **Statistics** button will be active.</span></span> <span data-ttu-id="b641f-120">Vous pouvez le sélectionner pour afficher les statistiques de recherche, telles que :</span><span class="sxs-lookup"><span data-stu-id="b641f-120">You can select it to see search statistics, such as:</span></span>

- <span data-ttu-id="b641f-121">Résumé</span><span class="sxs-lookup"><span data-stu-id="b641f-121">Summary</span></span>
- <span data-ttu-id="b641f-122">Emplacements les plus fréquents</span><span class="sxs-lookup"><span data-stu-id="b641f-122">Top locations</span></span>
- <span data-ttu-id="b641f-123">Requêtes</span><span class="sxs-lookup"><span data-stu-id="b641f-123">Queries</span></span>

<span data-ttu-id="b641f-124">Pour plus d’informations sur les statistiques de recherche, voir statistiques de la [recherche](search-statistics-in-advanced-ediscovery.md).</span><span class="sxs-lookup"><span data-stu-id="b641f-124">For more information about search statistics, see [Search statistics](search-statistics-in-advanced-ediscovery.md).</span></span>

<span data-ttu-id="b641f-125">Une fois l’aperçu terminé, le bouton **Aperçu** est actif.</span><span class="sxs-lookup"><span data-stu-id="b641f-125">Once preview is completed, the **Preview** button will be active.</span></span> <span data-ttu-id="b641f-126">Sélectionnez-le pour afficher un aperçu d’un sous-ensemble de résultats.</span><span class="sxs-lookup"><span data-stu-id="b641f-126">Select it to preview a sampled subset of the results.</span></span>

## <a name="add-search-results-to-a-review-set"></a><span data-ttu-id="b641f-127">Ajouter des résultats de recherche à un jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="b641f-127">Add search results to a review set</span></span>

<span data-ttu-id="b641f-128">Lorsque vous êtes prêt à collecter et à traiter tous les résultats d’une recherche, vous pouvez le faire en l’ajoutant à un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="b641f-128">When you're ready to collect and process the entire results of a search, you can do so by adding it to a review set.</span></span> <span data-ttu-id="b641f-129">Pour plus d’informations, consultez [la rubrique ajouter des données à un jeu de vérification](add-data-to-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="b641f-129">For details, see [Add data to a review set](add-data-to-review-set.md).</span></span>

## <a name="add-non-microsoft-365-data-to-a-review-set"></a><span data-ttu-id="b641f-130">Ajouter des données non-Microsoft 365 à un jeu de révision</span><span class="sxs-lookup"><span data-stu-id="b641f-130">Add non-Microsoft 365 data to a review set</span></span>

<span data-ttu-id="b641f-131">Dans le cadre du processus de collecte pour un cas, vous pouvez également ajouter des données non Office 365 à un jeu de réexamens et les examiner et les analyser avec les données Office 365 que vous avez collectées à l’aide de l’outil de recherche.</span><span class="sxs-lookup"><span data-stu-id="b641f-131">As part of the collection process for a case, you can also add non-Office 365 data to a review set and review and analyze together with the Office 365 data that you collected by using the search tool.</span></span> <span data-ttu-id="b641f-132">Lorsque vous ajoutez un autre non-Office 365, vous devez l’associer à un dépositaire spécifique dans le cas.</span><span class="sxs-lookup"><span data-stu-id="b641f-132">When you add non-Office 365, you have to associate it with a specific custodian in the case.</span></span> <span data-ttu-id="b641f-133">Pour plus d’informations, voir [charger des données non-Microsoft 365 dans un jeu de révision](load-non-Office-365-data-into-a-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="b641f-133">For more information, see [Load non-Microsoft 365 data into a review set](load-non-Office-365-data-into-a-review-set.md).</span></span>
