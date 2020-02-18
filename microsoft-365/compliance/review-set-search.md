---
title: Interroger les données d’un jeu à réviser
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
description: ''
ms.openlocfilehash: 97c1acdb515e278c40ca25d47e2d9fd24c23d51f
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42070057"
---
# <a name="query-the-data-in-a-review-set"></a><span data-ttu-id="10fb7-102">Interroger les données d’un jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="10fb7-102">Query the data in a review set</span></span>

<span data-ttu-id="10fb7-103">Dans la plupart des cas, il est utile de pouvoir approfondir les données dans un jeu de révision et d’organiser ces données pour faciliter une révision plus efficace.</span><span class="sxs-lookup"><span data-stu-id="10fb7-103">In most cases, it will be useful to be able to dig deeper into the data in a review set and organize that data to facilitate a more efficient review.</span></span> <span data-ttu-id="10fb7-104">L’utilisation de requêtes dans un jeu de vérification vous permet de vous concentrer sur un sous-ensemble de documents qui répondent aux critères de votre révision.</span><span class="sxs-lookup"><span data-stu-id="10fb7-104">Using Queries in a review set helps you focus on a subset of documents that meet the criteria of your review.</span></span>

## <a name="creating-and-running-a-query-in-a-review-set"></a><span data-ttu-id="10fb7-105">Création et exécution d’une requête dans un jeu de révision</span><span class="sxs-lookup"><span data-stu-id="10fb7-105">Creating and running a query in a review set</span></span>

<span data-ttu-id="10fb7-106">Pour créer et exécuter une requête sur les documents d’un jeu de révision, cliquez sur **nouvelle requête** dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="10fb7-106">To create and run a query on the documents in a review set, click **New query** in the review set.</span></span> <span data-ttu-id="10fb7-107">Une fois que vous avez nommé votre requête et défini les conditions, cliquez sur **Enregistrer** pour enregistrer et exécuter la requête.</span><span class="sxs-lookup"><span data-stu-id="10fb7-107">After you name your query and define the conditions, click **Save** to save and run the query.</span></span> <span data-ttu-id="10fb7-108">Pour exécuter une requête qui a été précédemment enregistrée, cliquez sur une requête enregistrée.</span><span class="sxs-lookup"><span data-stu-id="10fb7-108">To run a query that has been previously saved, click a saved query.</span></span>

![Examiner les requêtes Set](../media/AeDReviewSetQueries.png)

## <a name="building-a-review-set-query"></a><span data-ttu-id="10fb7-110">Création d’une requête d’ensemble de révision</span><span class="sxs-lookup"><span data-stu-id="10fb7-110">Building a review set query</span></span>

<span data-ttu-id="10fb7-111">Vous pouvez créer une requête à l’aide d’une combinaison de cartes de condition et de langage de requête dans la carte de condition de mots-clés.</span><span class="sxs-lookup"><span data-stu-id="10fb7-111">You can build a query by using a combination of condition cards and query language in the Keywords condition card.</span></span> <span data-ttu-id="10fb7-112">Vous pouvez également regrouper les cartes de condition en tant que bloc (appelé *groupe de conditions*) pour créer une requête plus complexe.</span><span class="sxs-lookup"><span data-stu-id="10fb7-112">You can also group condition cards together as a block (called a *condition group*) to build a more complex query.</span></span> <span data-ttu-id="10fb7-113">Pour obtenir la liste et la description des propriétés de métadonnées que vous pouvez rechercher, voir [document Metadata Fields in Advanced eDiscovery](document-metadata-fields-in-Advanced-eDiscovery.md).</span><span class="sxs-lookup"><span data-stu-id="10fb7-113">For a list and description of metadata properties that you can search, see [Document metadata fields in Advanced eDiscovery](document-metadata-fields-in-Advanced-eDiscovery.md).</span></span>

### <a name="condition-cards"></a><span data-ttu-id="10fb7-114">Cartes de condition</span><span class="sxs-lookup"><span data-stu-id="10fb7-114">Condition cards</span></span>

<span data-ttu-id="10fb7-115">Chaque champ pouvant faire l’objet d’une recherche dans un jeu de révision dispose d’une carte de condition correspondante que vous pouvez utiliser pour créer votre requête.</span><span class="sxs-lookup"><span data-stu-id="10fb7-115">Every searchable field in a review set has a corresponding condition card that you can use to build your query.</span></span>

<span data-ttu-id="10fb7-116">Il existe plusieurs types de cartes de condition :</span><span class="sxs-lookup"><span data-stu-id="10fb7-116">There are multiple types of condition cards:</span></span>

- <span data-ttu-id="10fb7-117">FREETEXT : une carte de condition FREETEXT est utilisée pour les champs de texte tels que subject.</span><span class="sxs-lookup"><span data-stu-id="10fb7-117">Freetext: A freetext condition card is used for text fields such as subject.</span></span> <span data-ttu-id="10fb7-118">Vous pouvez répertorier plusieurs termes de recherche en les séparant par une virgule.</span><span class="sxs-lookup"><span data-stu-id="10fb7-118">You can list multiple search terms by separating them out with a comma.</span></span>

- <span data-ttu-id="10fb7-119">Date : une carte de condition de date est utilisée pour les champs de date tels que date de dernière modification.</span><span class="sxs-lookup"><span data-stu-id="10fb7-119">Date: A date condition card is used for date fields such as last modified date.</span></span>

- <span data-ttu-id="10fb7-120">Options de recherche : une carte de condition options de recherche fournit une liste des valeurs possibles pour le champ particulier dans votre jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="10fb7-120">Search options: A search options condition card will provide a list of possible values for the particular field in your review set.</span></span> <span data-ttu-id="10fb7-121">Cette valeur est utilisée pour les champs, tels que sender, où il existe un nombre fini de valeurs possibles dans votre ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="10fb7-121">This is used for fields, such as sender, where there is a finite number of possible values in your review set.</span></span>

- <span data-ttu-id="10fb7-122">Mot-clé : une carte de condition de mot-clé est une instance spécifique de la carte de condition FREETEXT que vous pouvez utiliser pour rechercher des termes ou utiliser le langage de requête KQL dans.</span><span class="sxs-lookup"><span data-stu-id="10fb7-122">Keyword: A keyword condition card is a specific instance of freetext condition card that you can use to search for terms, or use KQL-like query language in.</span></span> <span data-ttu-id="10fb7-123">Voir ci-dessous pour plus de détails.</span><span class="sxs-lookup"><span data-stu-id="10fb7-123">See below for more detail.</span></span>

### <a name="query-language"></a><span data-ttu-id="10fb7-124">Langage de requête</span><span class="sxs-lookup"><span data-stu-id="10fb7-124">Query language</span></span>

<span data-ttu-id="10fb7-125">En plus des cartes de condition, vous pouvez utiliser un langage de requête de type KQL dans la carte de mots-clés pour créer votre requête.</span><span class="sxs-lookup"><span data-stu-id="10fb7-125">In addition to condition cards, you can use a KQL-like query language in the Keywords card to build your query.</span></span> <span data-ttu-id="10fb7-126">Le langage de requête pour les requêtes de jeu de révision prend en charge les opérateurs booléens standard, tels que **and**, **or**, **not**et **near**.</span><span class="sxs-lookup"><span data-stu-id="10fb7-126">The query language for review set queries supports standard Boolean operators, such as **AND**, **OR**, **NOT**, and **NEAR**.</span></span> <span data-ttu-id="10fb7-127">Il prend également en charge un caractère générique ( ?) à un seul caractère et un caractère générique à caractères multiples (\*).</span><span class="sxs-lookup"><span data-stu-id="10fb7-127">It also supports a single-character wildcard (?) and a multi-character wildcard (\*).</span></span>

## <a name="using-filters"></a><span data-ttu-id="10fb7-128">Utilisation de filtres</span><span class="sxs-lookup"><span data-stu-id="10fb7-128">Using filters</span></span>

<span data-ttu-id="10fb7-129">Outre les requêtes que vous pouvez enregistrer, vous pouvez utiliser les filtres Set Set pour appliquer rapidement des conditions supplémentaires à une requête Set Review.</span><span class="sxs-lookup"><span data-stu-id="10fb7-129">In addition to queries that you can save, you can use review set filters to quickly apply additional conditions to a review set query.</span></span> <span data-ttu-id="10fb7-130">Cela vous permet d’affiner les résultats affichés par une requête d’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="10fb7-130">This helps you further refine the results displayed by a review set query.</span></span>

![Vérifier les filtres Set](../media/AeDReviewSetFilters.png)

<span data-ttu-id="10fb7-132">Les filtres diffèrent des requêtes de deux façons importantes :</span><span class="sxs-lookup"><span data-stu-id="10fb7-132">Filters differ from queries in two significant ways:</span></span>

- <span data-ttu-id="10fb7-133">Les filtres sont transitoires.</span><span class="sxs-lookup"><span data-stu-id="10fb7-133">Filters are transient.</span></span> <span data-ttu-id="10fb7-134">Elles ne sont pas conservées au-delà de la session existante.</span><span class="sxs-lookup"><span data-stu-id="10fb7-134">They don't persist beyond the existing session.</span></span> <span data-ttu-id="10fb7-135">En d’autres termes, vous ne pouvez pas enregistrer un filtre.</span><span class="sxs-lookup"><span data-stu-id="10fb7-135">In other words, you can't save a filter.</span></span> <span data-ttu-id="10fb7-136">Les requêtes sont enregistrées dans l’ensemble de révision et y accèdent chaque fois que vous ouvrez l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="10fb7-136">Queries are saved to the review set, and access them whenever open the review set.</span></span>

- <span data-ttu-id="10fb7-137">Les filtres sont toujours additionnés.</span><span class="sxs-lookup"><span data-stu-id="10fb7-137">Filters are always additive.</span></span> <span data-ttu-id="10fb7-138">Les filtres sont appliqués en plus de la requête d’ensemble de révision actuelle.</span><span class="sxs-lookup"><span data-stu-id="10fb7-138">Filters are applied in addition to the current review set query.</span></span> <span data-ttu-id="10fb7-139">L’application d’une requête différente remplace les résultats renvoyés par la requête actuelle.</span><span class="sxs-lookup"><span data-stu-id="10fb7-139">Applying a different query will replace the results returned by the current query.</span></span>
