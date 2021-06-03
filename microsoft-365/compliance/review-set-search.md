---
title: Interroger le contenu d’un jeu à réviser
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
description: Découvrez comment créer et exécuter une requête dans un jeu à réviser pour organiser le contenu pour une révision plus efficace dans Advanced eDiscovery cas.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 64dbeb8ad68f4188e5768a0a7e0e80ca6c22760b
ms.sourcegitcommit: cc9e3cac6af23f20d7cc5ac6fc6f6e01bc3cc5c5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52736423"
---
# <a name="query-and-filter-content-in-a-review-set"></a><span data-ttu-id="9790f-103">Interroger et filtrer le contenu d’un jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="9790f-103">Query and filter content in a review set</span></span>

<span data-ttu-id="9790f-104">Dans la plupart des cas, il est utile d’approfondir le contenu d’un jeu à réviser et de l’organiser pour faciliter une révision plus efficace.</span><span class="sxs-lookup"><span data-stu-id="9790f-104">In most cases, it will be useful to dig deeper into the content in a review set and organize it to facilitate a more efficient review.</span></span> <span data-ttu-id="9790f-105">L’utilisation de filtres et de requêtes dans un ensemble de révision vous permet de vous concentrer sur un sous-ensemble de documents qui répondent aux critères de votre avis.</span><span class="sxs-lookup"><span data-stu-id="9790f-105">Using filters and queries in a review set helps you focus on a subset of documents that meet the criteria of your review.</span></span>

## <a name="default-filters"></a><span data-ttu-id="9790f-106">Filtres par défaut</span><span class="sxs-lookup"><span data-stu-id="9790f-106">Default filters</span></span>

<span data-ttu-id="9790f-107">Dans un jeu à réviser, il existe cinq filtres par défaut qui sont pré-chargés dans le jeu à réviser :</span><span class="sxs-lookup"><span data-stu-id="9790f-107">In a review set, there are five default filters that are pre-loaded in the review set:</span></span>

- <span data-ttu-id="9790f-108">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="9790f-108">Keywords</span></span>
- <span data-ttu-id="9790f-109">Date</span><span class="sxs-lookup"><span data-stu-id="9790f-109">Date</span></span>
- <span data-ttu-id="9790f-110">Sender/Author</span><span class="sxs-lookup"><span data-stu-id="9790f-110">Sender/Author</span></span>
- <span data-ttu-id="9790f-111">Objet/Titre</span><span class="sxs-lookup"><span data-stu-id="9790f-111">Subject/Title</span></span>
- <span data-ttu-id="9790f-112">Balises</span><span class="sxs-lookup"><span data-stu-id="9790f-112">Tags</span></span>

![Types de filtres par défaut](../media/DefaultFilterTypes.png)

<span data-ttu-id="9790f-114">Cliquez sur chaque filtre pour le développer et attribuer une valeur.</span><span class="sxs-lookup"><span data-stu-id="9790f-114">Click each filter to expand it and assign a value.</span></span> <span data-ttu-id="9790f-115">Cliquez en dehors du filtre pour appliquer automatiquement le filtre au jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="9790f-115">Click outside the filter to automatically apply the filter to the review set.</span></span> <span data-ttu-id="9790f-116">La capture d’écran suivante montre le filtre Date configuré pour afficher les documents dans une plage de dates.</span><span class="sxs-lookup"><span data-stu-id="9790f-116">The following screenshot shows the Date filter configured to show documents within a date range.</span></span>

![Filtre par défaut développé](../media/ExpandedFilter.png)

## <a name="add-or-remove-filters"></a><span data-ttu-id="9790f-118">Ajouter ou supprimer des filtres</span><span class="sxs-lookup"><span data-stu-id="9790f-118">Add or remove filters</span></span>

<span data-ttu-id="9790f-119">Pour ajouter ou supprimer des filtres qui sont affichés pour le jeu à réviser, sélectionnez **Filtres** pour ouvrir le panneau de filtrage, qui s’affiche sur une page volante.</span><span class="sxs-lookup"><span data-stu-id="9790f-119">To add or remove filters that are displayed for the review set, select **Filters** to open the filter panel, which is displayed on a flyout page.</span></span> 

![Panneau de filtrage](../media/FilterPanel.png)

<span data-ttu-id="9790f-121">Les filtres disponibles sont organisés en quatre sections :</span><span class="sxs-lookup"><span data-stu-id="9790f-121">The available filters are organized in four sections:</span></span>

- <span data-ttu-id="9790f-122">**Recherche**: filtres qui fournissent différentes fonctionnalités de recherche.</span><span class="sxs-lookup"><span data-stu-id="9790f-122">**Search**: Filters that provide different search capabilities.</span></span>

- <span data-ttu-id="9790f-123">**Codage analytique &** prédictif : filtre les propriétés générées et ajoutées aux documents lorsque vous exécutez le travail d’analyse de messagerie électronique **Document &** ou que vous utilisez des modèles de codage prédictifs.</span><span class="sxs-lookup"><span data-stu-id="9790f-123">**Analytics & predictive coding**: Filters for properties generated and added to documents when you run the **Document & email analytic** job or use predictive coding models.</span></span>

- <span data-ttu-id="9790f-124">**ID :** filtre toutes les propriétés d’ID des documents.</span><span class="sxs-lookup"><span data-stu-id="9790f-124">**IDs**: Filters for all ID properties of documents.</span></span>

- <span data-ttu-id="9790f-125">**Propriétés d’élément**: filtre les propriétés de document.</span><span class="sxs-lookup"><span data-stu-id="9790f-125">**Item properties**: Filters for document properties.</span></span> 

<span data-ttu-id="9790f-126">Développez chaque section et sélectionnez ou désélectionnez des filtres pour les ajouter ou les supprimer dans l’ensemble de filtres.</span><span class="sxs-lookup"><span data-stu-id="9790f-126">Expand each section and select or deselect filters to add or remove them in the filter set.</span></span> <span data-ttu-id="9790f-127">Lorsque vous ajoutez un filtre, il s’affiche dans le jeu de filtres.</span><span class="sxs-lookup"><span data-stu-id="9790f-127">When you add a filter, it's displayed in the filter set.</span></span> 

![Liste des sections et propriétés de filtre dans le panneau de filtrage](../media/FilterPanel2.png)

> [!NOTE]
> <span data-ttu-id="9790f-129">Lorsque vous développez une section dans le panneau de filtrage, vous remarquerez que les types de filtres par défaut sont sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="9790f-129">When you expand a section in the filter panel, you'll notice that the default filter types are selected.</span></span> <span data-ttu-id="9790f-130">Vous pouvez conserver ces éléments sélectionnés ou les désélectionner et les supprimer du jeu de filtres.</span><span class="sxs-lookup"><span data-stu-id="9790f-130">You can keep these selected or deselect them and removed them from the filter set.</span></span> 

## <a name="filter-types"></a><span data-ttu-id="9790f-131">Types de filtre</span><span class="sxs-lookup"><span data-stu-id="9790f-131">Filter types</span></span>

<span data-ttu-id="9790f-132">Chaque champ utilisable dans une recherche dans un jeu à réviser possède un filtre correspondant que vous pouvez utiliser pour filtrer des éléments en fonction d’un champ spécifique.</span><span class="sxs-lookup"><span data-stu-id="9790f-132">Every searchable field in a review set has a corresponding filter that you can use for filter items based on a specific field.</span></span>

<span data-ttu-id="9790f-133">Il existe plusieurs types de filtres :</span><span class="sxs-lookup"><span data-stu-id="9790f-133">There are multiple types of filters:</span></span>

- <span data-ttu-id="9790f-134">**Texte libre**: un filtre de texte libre est appliqué à des champs de texte tels que « Subject ».</span><span class="sxs-lookup"><span data-stu-id="9790f-134">**Freetext**: A freetext filter is applied to text fields such as "Subject".</span></span> <span data-ttu-id="9790f-135">Vous pouvez lister plusieurs termes de recherche en les séparant par une virgule.</span><span class="sxs-lookup"><span data-stu-id="9790f-135">You can list multiple search terms by separating them with a comma.</span></span>

- <span data-ttu-id="9790f-136">**Date**: un filtre de date est utilisé pour les champs de date tels que « Date de dernière modification ».</span><span class="sxs-lookup"><span data-stu-id="9790f-136">**Date**: A date filter is used for date fields such as "Last modified date".</span></span>

- <span data-ttu-id="9790f-137">**Options de** recherche : un filtre d’options de recherche fournit une liste des valeurs possibles (chaque valeur est affichée avec une case à cocher que vous pouvez sélectionner) pour des champs particuliers dans l’avis.</span><span class="sxs-lookup"><span data-stu-id="9790f-137">**Search options**: A search options filter provides a list of possible values (each value is displayed with a checkbox that you can select) for particular fields in the review.</span></span> <span data-ttu-id="9790f-138">Ce filtre est utilisé pour les champs, tels que « Expéditeur », où il existe un nombre fini de valeurs possibles dans le jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="9790f-138">This filter is used for fields, such as "Sender", where there is a finite number of possible values in the review set.</span></span>

- <span data-ttu-id="9790f-139">**Mot** clé : une condition de mot clé est une instance spécifique de condition de texte libre que vous pouvez utiliser pour rechercher des termes.</span><span class="sxs-lookup"><span data-stu-id="9790f-139">**Keyword**: A keyword condition is a specific instance of freetext condition that you can use to search for terms.</span></span> <span data-ttu-id="9790f-140">Vous pouvez également utiliser un langage de requête de type KQL dans ce type de filtre.</span><span class="sxs-lookup"><span data-stu-id="9790f-140">You can also use KQL-like query language in this type of filter.</span></span> <span data-ttu-id="9790f-141">Pour plus d’informations, voir les sections Langage de requête et Générateur de requêtes avancé dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="9790f-141">For more information, see the Query language and Advanced query builder sections in this topic.</span></span>

## <a name="include-and-exclude-filter-relationships"></a><span data-ttu-id="9790f-142">Inclure et exclure des relations de filtre</span><span class="sxs-lookup"><span data-stu-id="9790f-142">Include and exclude filter relationships</span></span>

<span data-ttu-id="9790f-143">Vous avez la possibilité de modifier la relation Inclure et exclure pour un filtre particulier.</span><span class="sxs-lookup"><span data-stu-id="9790f-143">You have the option to change the include and exclude relationship for a particular filter.</span></span> <span data-ttu-id="9790f-144">Par exemple, dans le filtre Balise, vous pouvez exclure les éléments **marqués** avec une balise particulière en sélectionnant Égal à aucun des éléments du filtre de ladown.</span><span class="sxs-lookup"><span data-stu-id="9790f-144">For example, in the Tag filter, you can exclude items that are tagged with a particular tag by selecting **Equals none of** in the dropdown filter.</span></span> 

![Exclure le filtre de balise](../media/TagFilterExclude.png)

## <a name="save-filters-as-queries"></a><span data-ttu-id="9790f-146">Enregistrer des filtres en tant que requêtes</span><span class="sxs-lookup"><span data-stu-id="9790f-146">Save filters as queries</span></span>

<span data-ttu-id="9790f-147">Une fois que vous êtes satisfait de vos filtres, vous pouvez enregistrer la combinaison de filtres en tant que requête de filtre.</span><span class="sxs-lookup"><span data-stu-id="9790f-147">After you are satisfied with your filters, you can save the filter combination as a filter query.</span></span> <span data-ttu-id="9790f-148">Cela vous permet d’appliquer le filtre dans les prochaines sessions de révision.</span><span class="sxs-lookup"><span data-stu-id="9790f-148">This lets you apply the filter in the future review sessions.</span></span>

<span data-ttu-id="9790f-149">Pour enregistrer un filtre, **sélectionnez Enregistrer la requête et** nommez-la.</span><span class="sxs-lookup"><span data-stu-id="9790f-149">To save a filter, select **Save the query** and name it.</span></span> <span data-ttu-id="9790f-150">Vous ou d’autres réviseurs pouvez exécuter  des requêtes de filtre précédemment enregistrées en sélectionnant la dropdown des requêtes de filtre enregistrées et en sélectionnant une requête de filtre à appliquer aux documents de l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="9790f-150">You or other reviewers can run previously saved filter queries by selecting the **Saved filter queries** dropdown and selecting a filter query to apply to review set documents.</span></span> 

![Enregistrer une requête de filtre](../media/SaveFilterQuery.png)

<span data-ttu-id="9790f-152">Pour supprimer une requête de filtre, ouvrez le panneau de filtrage et sélectionnez l’icône de corbeille en côté de la requête.</span><span class="sxs-lookup"><span data-stu-id="9790f-152">To delete a filter query, open the filter panel and select the trashcan icon next to the query.</span></span>

![Supprimer une requête de filtre](../media/DeleteFilterQuery.png)

## <a name="query-language"></a><span data-ttu-id="9790f-154">Langage de requête</span><span class="sxs-lookup"><span data-stu-id="9790f-154">Query language</span></span>

<span data-ttu-id="9790f-155">En plus d’utiliser des filtres, vous pouvez également utiliser un langage de requête KQL dans le filtre Mots clés pour créer votre requête de recherche de jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="9790f-155">In addition to using filters, you can also use a KQL-like query language in the Keywords filter to build your review set search query.</span></span> <span data-ttu-id="9790f-156">Le langage de requête pour les requêtes de jeu à réviser prend en charge les opérateurs booléens standard, tels que **AND**, **OR**, **NOT** et **NEAR**.</span><span class="sxs-lookup"><span data-stu-id="9790f-156">The query language for review set queries supports standard Boolean operators, such as **AND**, **OR**, **NOT**, and **NEAR**.</span></span> <span data-ttu-id="9790f-157">Il prend également en charge un caractère générique à caractère unique (?) et un caractère générique à plusieurs caractères (\*).</span><span class="sxs-lookup"><span data-stu-id="9790f-157">It also supports a single-character wildcard (?) and a multi-character wildcard (\*).</span></span>

## <a name="advanced-query-builder"></a><span data-ttu-id="9790f-158">Générateur de requêtes avancé</span><span class="sxs-lookup"><span data-stu-id="9790f-158">Advanced query builder</span></span>

<span data-ttu-id="9790f-159">Vous pouvez également créer des requêtes plus avancées pour rechercher des documents dans un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="9790f-159">You can also build more advanced queries to search for documents in a review set.</span></span>

1. <span data-ttu-id="9790f-160">Ouvrez le panneau de filtrage, **sélectionnez Filtres** et **développez** la section Recherche.</span><span class="sxs-lookup"><span data-stu-id="9790f-160">Open the filter panel, select **Filters**, and expand the **Search** section.</span></span>

  ![Ajouter un filtre KQL](../media/AddKQLFilter.png)

2. <span data-ttu-id="9790f-162">Sélectionnez **le filtre KQL,** puis cliquez **sur Ouvrir le générateur de requêtes.**</span><span class="sxs-lookup"><span data-stu-id="9790f-162">Select the **KQL** filter and click **Open query builder**.</span></span>

   <span data-ttu-id="9790f-163">Dans ce panneau, vous pouvez créer des requêtes KQL complexes à l’aide du générateur de requêtes.</span><span class="sxs-lookup"><span data-stu-id="9790f-163">In this panel, you can create complex KQL queries by using the query builder.</span></span> <span data-ttu-id="9790f-164">Vous pouvez ajouter des conditions ou des groupes de conditions composés de plusieurs conditions connectées logiquement par des **relations AND** ou **OR.**</span><span class="sxs-lookup"><span data-stu-id="9790f-164">You can add conditions or add condition groups that are made up of multiple conditions that are logically connected by **AND** or **OR** relationships.</span></span>

   ![Utiliser le générateur de requêtes pour configurer des requêtes de filtre complexes](../media/ComplexQuery.png)
