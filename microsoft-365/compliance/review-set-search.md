---
title: Interroger les données d’un jeu à réviser
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Découvrez comment créer et exécuter une requête dans un jeu à réviser pour organiser les données pour une révision plus efficace dans Advanced eDiscovery cas.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 5a03b0c863f9cc2050b18ce83ed11b8a71d1db4d
ms.sourcegitcommit: 94e64afaf12f3d8813099d8ffa46baba65772763
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "52345799"
---
# <a name="query-the-data-in-a-review-set"></a><span data-ttu-id="1cf93-103">Interroger les données d’un jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="1cf93-103">Query the data in a review set</span></span>

<span data-ttu-id="1cf93-104">Dans la plupart des cas, il est utile de pouvoir approfondir les données d’un jeu à réviser et d’organiser ces données pour faciliter une révision plus efficace.</span><span class="sxs-lookup"><span data-stu-id="1cf93-104">In most cases, it will be useful to be able to dig deeper into the data in a review set and organize that data to facilitate a more efficient review.</span></span> <span data-ttu-id="1cf93-105">L’utilisation de requêtes dans un jeu à réviser vous permet de vous concentrer sur un sous-ensemble de documents qui répondent aux critères de votre avis.</span><span class="sxs-lookup"><span data-stu-id="1cf93-105">Using Queries in a review set helps you focus on a subset of documents that meet the criteria of your review.</span></span>

## <a name="creating-and-running-a-query-in-a-review-set"></a><span data-ttu-id="1cf93-106">Création et exécution d’une requête dans un jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="1cf93-106">Creating and running a query in a review set</span></span>

<span data-ttu-id="1cf93-107">Pour créer et exécuter une requête sur les documents d’un jeu à réviser, sélectionnez **Nouvelle requête** dans le jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="1cf93-107">To create and run a query on the documents in a review set, select **New query** in the review set.</span></span> <span data-ttu-id="1cf93-108">Après avoir nommé votre requête et défini les conditions, sélectionnez **Enregistrer** pour enregistrer et exécuter la requête.</span><span class="sxs-lookup"><span data-stu-id="1cf93-108">After you name your query and define the conditions, select **Save** to save and run the query.</span></span> <span data-ttu-id="1cf93-109">Pour exécuter une requête qui a été précédemment enregistrée, sélectionnez une requête enregistrée.</span><span class="sxs-lookup"><span data-stu-id="1cf93-109">To run a query that has been previously saved, select a saved query.</span></span>

![Examiner les requêtes définies](../media/AeDReviewSetQueries.png)

## <a name="building-a-review-set-query"></a><span data-ttu-id="1cf93-111">Création d’une requête de jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="1cf93-111">Building a review set query</span></span>

<span data-ttu-id="1cf93-112">Vous pouvez créer une requête à l’aide d’une combinaison de mots clés, propriétés et conditions dans la condition Mots clés.</span><span class="sxs-lookup"><span data-stu-id="1cf93-112">You can build a query by using a combination of keywords, properties, and conditions in the Keywords condition.</span></span> <span data-ttu-id="1cf93-113">Vous pouvez également grouper des conditions en tant que bloc (appelé groupe *de conditions)* pour créer une requête plus complexe.</span><span class="sxs-lookup"><span data-stu-id="1cf93-113">You can also group conditions as a block (called a *condition group*) to build a more complex query.</span></span> <span data-ttu-id="1cf93-114">Pour consulter la liste et la description des propriétés de métadonnées que vous pouvez rechercher, consultez [Champs de métadonnées des documents dans Advanced eDiscovery](document-metadata-fields-in-Advanced-eDiscovery.md).</span><span class="sxs-lookup"><span data-stu-id="1cf93-114">For a list and description of metadata properties that you can search, see [Document metadata fields in Advanced eDiscovery](document-metadata-fields-in-Advanced-eDiscovery.md).</span></span>

### <a name="conditions"></a><span data-ttu-id="1cf93-115">Conditions</span><span class="sxs-lookup"><span data-stu-id="1cf93-115">Conditions</span></span>

<span data-ttu-id="1cf93-116">Chaque champ utilisable dans une recherche dans un jeu à réviser a une condition correspondante que vous pouvez utiliser pour créer votre requête.</span><span class="sxs-lookup"><span data-stu-id="1cf93-116">Every searchable field in a review set has a corresponding condition that you can use to build your query.</span></span>

<span data-ttu-id="1cf93-117">Il existe plusieurs types de conditions :</span><span class="sxs-lookup"><span data-stu-id="1cf93-117">There are multiple types of conditions:</span></span>

- <span data-ttu-id="1cf93-118">Texte libre : une condition de texte libre est utilisée pour les champs de texte tels que l’objet.</span><span class="sxs-lookup"><span data-stu-id="1cf93-118">Freetext: A freetext condition is used for text fields such as subject.</span></span> <span data-ttu-id="1cf93-119">Vous pouvez lister plusieurs termes de recherche en les séparant par une virgule.</span><span class="sxs-lookup"><span data-stu-id="1cf93-119">You can list multiple search terms by separating them out with a comma.</span></span>

- <span data-ttu-id="1cf93-120">Date : une condition de date est utilisée pour les champs de date tels que la date de dernière modification.</span><span class="sxs-lookup"><span data-stu-id="1cf93-120">Date: A date condition is used for date fields such as last modified date.</span></span>

- <span data-ttu-id="1cf93-121">Options de recherche : une condition d’options de recherche fournit une liste des valeurs possibles pour le champ particulier dans votre jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="1cf93-121">Search options: A search options condition will provide a list of possible values for the particular field in your review set.</span></span> <span data-ttu-id="1cf93-122">Il est utilisé pour les champs, tels que l’expéditeur, où il existe un nombre fini de valeurs possibles dans votre jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="1cf93-122">This is used for fields, such as sender, where there is a finite number of possible values in your review set.</span></span>

- <span data-ttu-id="1cf93-123">Mot clé : une condition de mot clé est une instance spécifique de condition de texte libre que vous pouvez utiliser pour rechercher des termes ou utiliser un langage de requête KQL.</span><span class="sxs-lookup"><span data-stu-id="1cf93-123">Keyword: A keyword condition is a specific instance of freetext condition that you can use to search for terms, or use KQL-like query language in.</span></span> <span data-ttu-id="1cf93-124">Pour plus d’informations, voir ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="1cf93-124">See below for more detail.</span></span>

### <a name="query-language"></a><span data-ttu-id="1cf93-125">Langage de requête</span><span class="sxs-lookup"><span data-stu-id="1cf93-125">Query language</span></span>

<span data-ttu-id="1cf93-126">Outre les conditions, vous pouvez utiliser un langage de requête KQL dans la condition Keywords pour créer votre requête.</span><span class="sxs-lookup"><span data-stu-id="1cf93-126">In addition to conditions, you can use a KQL-like query language in the Keywords condition to build your query.</span></span> <span data-ttu-id="1cf93-127">Le langage de requête pour les requêtes de jeu à réviser prend en charge les opérateurs booléens standard, tels que **AND**, **OR**, **NOT** et **NEAR**.</span><span class="sxs-lookup"><span data-stu-id="1cf93-127">The query language for review set queries supports standard Boolean operators, such as **AND**, **OR**, **NOT**, and **NEAR**.</span></span> <span data-ttu-id="1cf93-128">Il prend également en charge un caractère générique à caractère unique (?) et un caractère générique à plusieurs caractères (\*).</span><span class="sxs-lookup"><span data-stu-id="1cf93-128">It also supports a single-character wildcard (?) and a multi-character wildcard (\*).</span></span>

## <a name="filters"></a><span data-ttu-id="1cf93-129">Filtres</span><span class="sxs-lookup"><span data-stu-id="1cf93-129">Filters</span></span>

<span data-ttu-id="1cf93-130">Outre les requêtes que vous pouvez enregistrer, vous pouvez utiliser des filtres de jeu à réviser pour appliquer rapidement des conditions supplémentaires à une requête de jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="1cf93-130">In addition to queries that you can save, you can use review set filters to quickly apply additional conditions to a review set query.</span></span> <span data-ttu-id="1cf93-131">L’utilisation de filtres vous permet d’affiner davantage les résultats affichés par une requête de jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="1cf93-131">Using filters help you further refine the results displayed by a review set query.</span></span>

![Passer en revue les filtres](../media/AeDReviewSetFilters.png)

<span data-ttu-id="1cf93-133">Les filtres diffèrent des requêtes de deux manières significatives :</span><span class="sxs-lookup"><span data-stu-id="1cf93-133">Filters differ from queries in two significant ways:</span></span>

- <span data-ttu-id="1cf93-134">Les filtres sont temporaires.</span><span class="sxs-lookup"><span data-stu-id="1cf93-134">Filters are transient.</span></span> <span data-ttu-id="1cf93-135">Elles ne persistent pas au-delà de la session existante.</span><span class="sxs-lookup"><span data-stu-id="1cf93-135">They don't persist beyond the existing session.</span></span> <span data-ttu-id="1cf93-136">En d’autres termes, vous ne pouvez pas enregistrer un filtre.</span><span class="sxs-lookup"><span data-stu-id="1cf93-136">In other words, you can't save a filter.</span></span> <span data-ttu-id="1cf93-137">Les requêtes sont enregistrées dans le jeu à réviser et y accèdent chaque fois que vous ouvrez le jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="1cf93-137">Queries are saved to the review set, and access them whenever you open the review set.</span></span>

- <span data-ttu-id="1cf93-138">Les filtres sont toujours additives.</span><span class="sxs-lookup"><span data-stu-id="1cf93-138">Filters are always additive.</span></span> <span data-ttu-id="1cf93-139">Les filtres sont appliqués en plus de la requête de jeu à réviser actuelle.</span><span class="sxs-lookup"><span data-stu-id="1cf93-139">Filters are applied in addition to the current review set query.</span></span> <span data-ttu-id="1cf93-140">L’application d’une autre requête a pour effet de remplacer les résultats renvoyés par la requête actuelle.</span><span class="sxs-lookup"><span data-stu-id="1cf93-140">Applying a different query will replace the results returned by the current query.</span></span>
