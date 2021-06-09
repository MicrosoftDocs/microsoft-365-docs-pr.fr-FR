---
title: Prise en charge de LASK/Double Byte pour Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment Advanced eDiscovery en Microsoft 365 prend en charge les langues chinoise, japonaise et coréenne (JCK), qui utilisent un jeu de caractères sur deux sur deux caractères.
ms.openlocfilehash: ee47c5cd7f1a378ccfff05b8f7712e91092907cb
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50926600"
---
# <a name="cjk-language-support-for-advanced-ediscovery"></a><span data-ttu-id="4be7c-103">Prise en charge linguistique DE LASK pour Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="4be7c-103">CJK language support for Advanced eDiscovery</span></span>

<span data-ttu-id="4be7c-104">Advanced eDiscovery prend en charge les langues de jeu de caractères sur deux sur deux caractères (notamment le chinois simplifié, le chinois traditionnel, le japonais et le coréen, qui sont collectivement appelés langues *DUK),* pour les scénarios avancés suivants dans un jeu à réviser :</span><span class="sxs-lookup"><span data-stu-id="4be7c-104">Advanced eDiscovery supports double-byte character set languages (these include Simplified Chinese, Traditional Chinese, Japanese, and Korean, which are collectively known as *CJK* languages) for the following advanced scenarios in a review set:</span></span>

- <span data-ttu-id="4be7c-105">Lorsque vous [interrogez les données dans un jeu à réviser](review-set-search.md).</span><span class="sxs-lookup"><span data-stu-id="4be7c-105">When you [query the data in a review set](review-set-search.md).</span></span>

- <span data-ttu-id="4be7c-106">Lorsque vous [balisez des documents dans un jeu à réviser.](tagging-documents.md)</span><span class="sxs-lookup"><span data-stu-id="4be7c-106">When you [tag documents in a review set](tagging-documents.md).</span></span>

- <span data-ttu-id="4be7c-107">Lorsque vous [analysez des données de cas dans un jeu à réviser](analyzing-data-in-review-set.md) à l’aide de la détection des quasi-doublons, du thread de messagerie électronique et de l’analyse des thèmes.</span><span class="sxs-lookup"><span data-stu-id="4be7c-107">When you [analyze case data in a review set](analyzing-data-in-review-set.md) by using near duplicate detection, email threading, and themes analytics.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="4be7c-108">Foire aux questions</span><span class="sxs-lookup"><span data-stu-id="4be7c-108">Frequently asked questions</span></span>

<span data-ttu-id="4be7c-109">**Comment créer une recherche pour collecter des éléments qui contiennent des caractères DUKS ?**</span><span class="sxs-lookup"><span data-stu-id="4be7c-109">**How do I create a search to collect items that contains CJK characters?**</span></span>

<span data-ttu-id="4be7c-110">Vous pouvez utiliser des caractèresJCK pour les [recherches](building-search-queries.md#keyword-searches)par mot clé, les requêtes par mot clé et les [conditions](keyword-queries-and-search-conditions.md) de recherche lors de la recherche de contenu dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="4be7c-110">You can use CJK characters for [keyword searches](building-search-queries.md#keyword-searches), [keyword queries and search conditions](keyword-queries-and-search-conditions.md) when searching for content in Advanced eDiscovery.</span></span> <span data-ttu-id="4be7c-111">La recherche de caractères DUKS est également prise en charge lors de la recherche de contenu dans core eDiscovery et la recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="4be7c-111">Searching for CJK characters is also supported when searching for content in Core eDiscovery and Content Search.</span></span>

<span data-ttu-id="4be7c-112">Nous fournissons la [](keyword-queries-and-search-conditions.md#search-operators) prise en charge DE LASK pour tous les opérateurs de recherche et [conditions](keyword-queries-and-search-conditions.md#search-conditions)de recherche, y compris les opérateurs booléens **ET**, **OU**, **NOT** et **NEAR**.</span><span class="sxs-lookup"><span data-stu-id="4be7c-112">We provide CJK support for all [search operators](keyword-queries-and-search-conditions.md#search-operators) and [search conditions](keyword-queries-and-search-conditions.md#search-conditions), including the boolean operators **AND**, **OR**, **NOT**, and **NEAR**.</span></span>

<span data-ttu-id="4be7c-113">Si vous êtes certain que les emplacements de contenu ou les éléments contiennent des caractèresJC, mais que les recherches ne retournent aucun résultat, cliquez sur l’icône langue-pays/région de la requête</span><span class="sxs-lookup"><span data-stu-id="4be7c-113">If you're certain that content locations or items contain CJK characters, but searches aren't returning any results, click the query language-country/region icon</span></span> ![Icône Langue-pays/région de requête dans la recherche de contenu](../media/8d4b60c8-e1f1-40f9-88ae-ee2a7eca0886.png) <span data-ttu-id="4be7c-115">et sélectionnez la valeur de code de culture correspondant au pays/la langue pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="4be7c-115">and select the corresponding language-country culture code value for the search.</span></span> <span data-ttu-id="4be7c-116">La langue/région par défaut est neutre.</span><span class="sxs-lookup"><span data-stu-id="4be7c-116">The default language/region is neutral.</span></span>

<span data-ttu-id="4be7c-117">**Puis-je rechercher plusieurs langues à la fois ?**</span><span class="sxs-lookup"><span data-stu-id="4be7c-117">**Can I search for multiple languages at once?**</span></span>

<span data-ttu-id="4be7c-118">Cela dépend de votre scénario de recherche.</span><span class="sxs-lookup"><span data-stu-id="4be7c-118">It depends on your search scenario.</span></span>

- <span data-ttu-id="4be7c-119">Lorsque vous [interrogez des données dans un jeu à réviser Advanced eDiscovery,](review-set-search.md) vous pouvez rechercher plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="4be7c-119">When you [query data in a review set](review-set-search.md) in Advanced eDiscovery, you can search for multiple languages.</span></span>

- <span data-ttu-id="4be7c-120">Lorsque vous [créez une recherche pour collecter des données,](create-search-to-collect-data.md)créez une recherche distincte pour chaque langue que vous ciblez.</span><span class="sxs-lookup"><span data-stu-id="4be7c-120">When you [create a search to collect data](create-search-to-collect-data.md), create a separate search for each language you're targeting.</span></span> <span data-ttu-id="4be7c-121">Par exemple, si vous recherchez un document qui contient du chinois et du coréen, sélectionnez Chinois pour votre première requête et coréen pour votre deuxième requête.</span><span class="sxs-lookup"><span data-stu-id="4be7c-121">For example, if you are searching for a document that contains both Chinese and Korean, select Chinese for your first query and select Korean for your second query.</span></span>

<span data-ttu-id="4be7c-122">**Je ne vois pas l’icône langue-pays/région de la requête pour sélectionner une langue pour les requêtes dans un jeu à réviser. Comment puis-je spécifier une langue de requête dans une recherche de jeu à réviser ?**</span><span class="sxs-lookup"><span data-stu-id="4be7c-122">**I don't see the query language-country/region icon to select a language for queries in a review set. How can I specify a query language in a review set search?**</span></span>

<span data-ttu-id="4be7c-123">Pour les requêtes de jeu à réviser, il n’est pas nécessaire de spécifier une langue de document.</span><span class="sxs-lookup"><span data-stu-id="4be7c-123">For review set queries, you don't need to specify a document language.</span></span> <span data-ttu-id="4be7c-124">Advanced eDiscovery détecte automatiquement les langues de document lorsque vous ajoutez du contenu à un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="4be7c-124">Advanced eDiscovery automatically detects document languages when you add content to a review set.</span></span> <span data-ttu-id="4be7c-125">Cela vous permet d’optimiser les résultats de votre requête dans un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="4be7c-125">This helps you optimize your query results in a review set.</span></span>

<span data-ttu-id="4be7c-126">**Puis-je voir les langues détectées dans les [métadonnées de fichier](view-documents-in-review-set.md#file-metadata)?**</span><span class="sxs-lookup"><span data-stu-id="4be7c-126">**Can I see detected languages in [file metadata](view-documents-in-review-set.md#file-metadata)?**</span></span>

<span data-ttu-id="4be7c-127">Non, vous ne pouvez pas voir les langues détectées dans les métadonnées de fichier.</span><span class="sxs-lookup"><span data-stu-id="4be7c-127">No, you can't see detected languages in file metadata.</span></span>

<span data-ttu-id="4be7c-128">**Puis-je filtrer par langues de document dans un jeu à réviser**?</span><span class="sxs-lookup"><span data-stu-id="4be7c-128">**Can I filter by document languages in a review set**?</span></span>

<span data-ttu-id="4be7c-129">Non, vous ne pouvez pas filtrer, trier ou rechercher par langues de document dans un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="4be7c-129">No, you can't filter, sort, or search by document languages in a review set.</span></span>

<span data-ttu-id="4be7c-130">**Cette version DEMCS pour les scénarios d’ensemble de révision affectera-t-elle l’une de mes recherches et jeux de révision existants ?**</span><span class="sxs-lookup"><span data-stu-id="4be7c-130">**Will this CJK release for review set scenarios affect any of my existing searches and review sets?**</span></span>

<span data-ttu-id="4be7c-131">Non, aucune de vos recherches et jeux de révision existants ne change.</span><span class="sxs-lookup"><span data-stu-id="4be7c-131">No, none of your existing searches and review sets will change.</span></span> <span data-ttu-id="4be7c-132">Vous n’avez pas besoin de réindexer des données existantes et les résultats de recherche pour le texte en anglais seront les mêmes.</span><span class="sxs-lookup"><span data-stu-id="4be7c-132">You don't need to reindex existing data, and search results for English text will be the same.</span></span>

<span data-ttu-id="4be7c-133">**Comment modifier ma langue d’affichage en chinois, japonais ou coréen ?**</span><span class="sxs-lookup"><span data-stu-id="4be7c-133">**How do I change my display language to Chinese, Japanese, or Korean?**</span></span>

<span data-ttu-id="4be7c-134">Pour plus d’informations sur la modification de la langue d’affichage et du fuseau horaire, voir Comment définir les [paramètres](/office365/troubleshoot/access-management/set-language-and-region)de langue et de région pour Office 365 .</span><span class="sxs-lookup"><span data-stu-id="4be7c-134">For information about how to change display language and time zone, see [How to set language and region settings for Office 365](/office365/troubleshoot/access-management/set-language-and-region).</span></span>

## <a name="known-issues"></a><span data-ttu-id="4be7c-135">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="4be7c-135">Known issues</span></span>

- <span data-ttu-id="4be7c-136">OcR ne prend pas en charge les caractères DE LASK à partir de fichiers image</span><span class="sxs-lookup"><span data-stu-id="4be7c-136">OCR doesn't support CJK characters from image files</span></span>

- <span data-ttu-id="4be7c-137">Les fichiers e-mail (tels que \*.eml et \*.msg) en affichage [Annotate](view-documents-in-review-set.md#annotate-view) ne sont pas pris en charge pour les langues DE LATA.</span><span class="sxs-lookup"><span data-stu-id="4be7c-137">Email files (such as \*.eml and \*.msg) in [Annotate view](view-documents-in-review-set.md#annotate-view) aren't supported for CJK languages.</span></span>

- <span data-ttu-id="4be7c-138">La mise en surbrillance des résultats de recherche [en affichage Texte](view-documents-in-review-set.md#text-view) n’est pas prise en charge pour les langues DUKS.</span><span class="sxs-lookup"><span data-stu-id="4be7c-138">Search hit highlighting in [Text view](view-documents-in-review-set.md#text-view) isn't supported for CJK languages.</span></span>

- <span data-ttu-id="4be7c-139">Le [module de pertinence utilisé](using-relevance.md) pour analyser les données ne prend pas en charge les langues DUKCO.</span><span class="sxs-lookup"><span data-stu-id="4be7c-139">The [Relevance module](using-relevance.md) used to analyze data doesn't support CJK languages.</span></span>

- <span data-ttu-id="4be7c-140">[Les prises en charge basées sur](managing-holds.md#manage-non-custodial-holds) des requêtes ne sont pas prises en charge pour les langues DUKS.</span><span class="sxs-lookup"><span data-stu-id="4be7c-140">[Query-based holds](managing-holds.md#manage-non-custodial-holds) aren't supported for CJK languages.</span></span>