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
description: Découvrez comment créer et exécuter une requête dans un jeu de réexamen afin d’organiser les données pour une révision plus efficace dans un cas avancé de découverte électronique.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 1ead897d412af2356d8b57ab8494539a5ed9a019
ms.sourcegitcommit: 3c39866865c8c61bce2169818d8551da65033cfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2020
ms.locfileid: "48816567"
---
# <a name="query-the-data-in-a-review-set"></a><span data-ttu-id="2b47d-103">Interroger les données d’un jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="2b47d-103">Query the data in a review set</span></span>

<span data-ttu-id="2b47d-104">Dans la plupart des cas, il est utile de pouvoir approfondir les données dans un jeu de révision et d’organiser ces données pour faciliter une révision plus efficace.</span><span class="sxs-lookup"><span data-stu-id="2b47d-104">In most cases, it will be useful to be able to dig deeper into the data in a review set and organize that data to facilitate a more efficient review.</span></span> <span data-ttu-id="2b47d-105">L’utilisation de requêtes dans un jeu de vérification vous permet de vous concentrer sur un sous-ensemble de documents qui répondent aux critères de votre révision.</span><span class="sxs-lookup"><span data-stu-id="2b47d-105">Using Queries in a review set helps you focus on a subset of documents that meet the criteria of your review.</span></span>

## <a name="creating-and-running-a-query-in-a-review-set"></a><span data-ttu-id="2b47d-106">Création et exécution d’une requête dans un jeu de révision</span><span class="sxs-lookup"><span data-stu-id="2b47d-106">Creating and running a query in a review set</span></span>

<span data-ttu-id="2b47d-107">Pour créer et exécuter une requête sur les documents d’un jeu de révision, sélectionnez **nouvelle requête** dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="2b47d-107">To create and run a query on the documents in a review set, select **New query** in the review set.</span></span> <span data-ttu-id="2b47d-108">Une fois que vous avez nommé votre requête et défini les conditions, sélectionnez **Enregistrer** pour enregistrer et exécuter la requête.</span><span class="sxs-lookup"><span data-stu-id="2b47d-108">After you name your query and define the conditions, select **Save** to save and run the query.</span></span> <span data-ttu-id="2b47d-109">Pour exécuter une requête qui a été précédemment enregistrée, sélectionnez une requête enregistrée.</span><span class="sxs-lookup"><span data-stu-id="2b47d-109">To run a query that has been previously saved, select a saved query.</span></span>

![Examiner les requêtes Set](../media/AeDReviewSetQueries.png)

## <a name="building-a-review-set-query"></a><span data-ttu-id="2b47d-111">Création d’une requête d’ensemble de révision</span><span class="sxs-lookup"><span data-stu-id="2b47d-111">Building a review set query</span></span>

<span data-ttu-id="2b47d-112">Vous pouvez créer une requête à l’aide d’une combinaison de mots clés, de propriétés et de conditions dans la condition de mots clés.</span><span class="sxs-lookup"><span data-stu-id="2b47d-112">You can build a query by using a combination of keywords, properties, and conditions in the Keywords condition.</span></span> <span data-ttu-id="2b47d-113">Vous pouvez également regrouper les conditions sous forme de bloc (appelé *groupe de conditions* ) pour créer une requête plus complexe.</span><span class="sxs-lookup"><span data-stu-id="2b47d-113">You can also group conditions as a block (called a *condition group* ) to build a more complex query.</span></span> <span data-ttu-id="2b47d-114">Pour consulter la liste et la description des propriétés de métadonnées que vous pouvez rechercher, consultez [Champs de métadonnées des documents dans Advanced eDiscovery](document-metadata-fields-in-Advanced-eDiscovery.md).</span><span class="sxs-lookup"><span data-stu-id="2b47d-114">For a list and description of metadata properties that you can search, see [Document metadata fields in Advanced eDiscovery](document-metadata-fields-in-Advanced-eDiscovery.md).</span></span>

### <a name="conditions"></a><span data-ttu-id="2b47d-115">Conditions</span><span class="sxs-lookup"><span data-stu-id="2b47d-115">Conditions</span></span>

<span data-ttu-id="2b47d-116">Chaque champ pouvant faire l’objet d’une recherche dans un ensemble de réexamen a une condition correspondante que vous pouvez utiliser pour créer votre requête.</span><span class="sxs-lookup"><span data-stu-id="2b47d-116">Every searchable field in a review set has a corresponding condition that you can use to build your query.</span></span>

<span data-ttu-id="2b47d-117">Il existe plusieurs types de conditions :</span><span class="sxs-lookup"><span data-stu-id="2b47d-117">There are multiple types of conditions:</span></span>

- <span data-ttu-id="2b47d-118">FREETEXT : une condition FREETEXT est utilisée pour les champs de texte tels que subject.</span><span class="sxs-lookup"><span data-stu-id="2b47d-118">Freetext: A freetext condition is used for text fields such as subject.</span></span> <span data-ttu-id="2b47d-119">Vous pouvez répertorier plusieurs termes de recherche en les séparant par une virgule.</span><span class="sxs-lookup"><span data-stu-id="2b47d-119">You can list multiple search terms by separating them out with a comma.</span></span>

- <span data-ttu-id="2b47d-120">Date : une condition de date est utilisée pour les champs de date tels que date de dernière modification.</span><span class="sxs-lookup"><span data-stu-id="2b47d-120">Date: A date condition is used for date fields such as last modified date.</span></span>

- <span data-ttu-id="2b47d-121">Options de recherche : une condition options de recherche fournit une liste de valeurs possibles pour le champ particulier dans votre jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="2b47d-121">Search options: A search options condition will provide a list of possible values for the particular field in your review set.</span></span> <span data-ttu-id="2b47d-122">Cette valeur est utilisée pour les champs, tels que sender, où il existe un nombre fini de valeurs possibles dans votre ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="2b47d-122">This is used for fields, such as sender, where there is a finite number of possible values in your review set.</span></span>

- <span data-ttu-id="2b47d-123">Mot clé : une condition de mot clé est une instance spécifique de la condition FREETEXT que vous pouvez utiliser pour rechercher des termes ou utiliser le langage de requête KQL dans.</span><span class="sxs-lookup"><span data-stu-id="2b47d-123">Keyword: A keyword condition is a specific instance of freetext condition that you can use to search for terms, or use KQL-like query language in.</span></span> <span data-ttu-id="2b47d-124">Voir ci-dessous pour plus de détails.</span><span class="sxs-lookup"><span data-stu-id="2b47d-124">See below for more detail.</span></span>

### <a name="query-language"></a><span data-ttu-id="2b47d-125">Langage de requête</span><span class="sxs-lookup"><span data-stu-id="2b47d-125">Query language</span></span>

<span data-ttu-id="2b47d-126">En plus des conditions, vous pouvez utiliser un langage de requête de type KQL dans la condition Keywords pour créer votre requête.</span><span class="sxs-lookup"><span data-stu-id="2b47d-126">In addition to conditions, you can use a KQL-like query language in the Keywords condition to build your query.</span></span> <span data-ttu-id="2b47d-127">Le langage de requête pour les requêtes de jeu de révision prend en charge les opérateurs booléens standard, tels que **and** , **or** , **not** et **near** .</span><span class="sxs-lookup"><span data-stu-id="2b47d-127">The query language for review set queries supports standard Boolean operators, such as **AND** , **OR** , **NOT** , and **NEAR** .</span></span> <span data-ttu-id="2b47d-128">Il prend également en charge un caractère générique ( ?) à un seul caractère et un caractère générique à caractères multiples (\*).</span><span class="sxs-lookup"><span data-stu-id="2b47d-128">It also supports a single-character wildcard (?) and a multi-character wildcard (\*).</span></span>

## <a name="filters"></a><span data-ttu-id="2b47d-129">Filtres</span><span class="sxs-lookup"><span data-stu-id="2b47d-129">Filters</span></span>

<span data-ttu-id="2b47d-130">Outre les requêtes que vous pouvez enregistrer, vous pouvez utiliser les filtres Set Set pour appliquer rapidement des conditions supplémentaires à une requête Set Review.</span><span class="sxs-lookup"><span data-stu-id="2b47d-130">In addition to queries that you can save, you can use review set filters to quickly apply additional conditions to a review set query.</span></span> <span data-ttu-id="2b47d-131">L’utilisation de filtres vous permet d’affiner les résultats affichés par une requête d’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="2b47d-131">Using filters help you further refine the results displayed by a review set query.</span></span>

![Vérifier les filtres Set](../media/AeDReviewSetFilters.png)

<span data-ttu-id="2b47d-133">Les filtres diffèrent des requêtes de deux façons importantes :</span><span class="sxs-lookup"><span data-stu-id="2b47d-133">Filters differ from queries in two significant ways:</span></span>

- <span data-ttu-id="2b47d-134">Les filtres sont transitoires.</span><span class="sxs-lookup"><span data-stu-id="2b47d-134">Filters are transient.</span></span> <span data-ttu-id="2b47d-135">Elles ne sont pas conservées au-delà de la session existante.</span><span class="sxs-lookup"><span data-stu-id="2b47d-135">They don't persist beyond the existing session.</span></span> <span data-ttu-id="2b47d-136">En d’autres termes, vous ne pouvez pas enregistrer un filtre.</span><span class="sxs-lookup"><span data-stu-id="2b47d-136">In other words, you can't save a filter.</span></span> <span data-ttu-id="2b47d-137">Les requêtes sont enregistrées dans l’ensemble de révision et y accèdent chaque fois que vous ouvrez l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="2b47d-137">Queries are saved to the review set, and access them whenever open the review set.</span></span>

- <span data-ttu-id="2b47d-138">Les filtres sont toujours additionnés.</span><span class="sxs-lookup"><span data-stu-id="2b47d-138">Filters are always additive.</span></span> <span data-ttu-id="2b47d-139">Les filtres sont appliqués en plus de la requête de jeu à réviser actuelle.</span><span class="sxs-lookup"><span data-stu-id="2b47d-139">Filters are applied in addition to the current review set query.</span></span> <span data-ttu-id="2b47d-140">L’application d’une autre requête a pour effet de remplacer les résultats renvoyés par la requête actuelle.</span><span class="sxs-lookup"><span data-stu-id="2b47d-140">Applying a different query will replace the results returned by the current query.</span></span>
