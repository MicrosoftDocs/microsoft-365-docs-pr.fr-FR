---
title: Prise en charge de la fonctionnalité CJC/double octet pour Advanced eDiscovery
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
description: Découvrez comment Advanced eDiscovery dans Microsoft 365 prend en charge les langues chinoise, japonaise et coréenne (CJK), qui utilisent un jeu de caractères codés sur deux octets.
ms.openlocfilehash: cef91001f48512545ce528d6f43de97c28c4c495
ms.sourcegitcommit: e17fd18b01d70e6428263c20cbce4b92e2a97765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48626934"
---
# <a name="cjk-language-support-for-advanced-ediscovery"></a><span data-ttu-id="9fd8f-103">Prise en charge de la langue CJC pour Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9fd8f-103">CJK language support for Advanced eDiscovery</span></span>

<span data-ttu-id="9fd8f-104">Advanced eDiscovery prend en charge les langues de jeu de caractères codés sur deux octets (notamment le chinois simplifié, le chinois traditionnel, le japonais et le coréen, qui sont appelés « langues *CJK* ») pour les scénarios avancés suivants dans un jeu de révision :</span><span class="sxs-lookup"><span data-stu-id="9fd8f-104">Advanced eDiscovery supports double-byte character set languages (these include Simplified Chinese, Traditional Chinese, Japanese, and Korean, which are collectively known as *CJK* languages) for the following advanced scenarios in a review set:</span></span>

- <span data-ttu-id="9fd8f-105">Lorsque vous [interrogez les données d’un ensemble de révision](review-set-search.md).</span><span class="sxs-lookup"><span data-stu-id="9fd8f-105">When you [query the data in a review set](review-set-search.md).</span></span>

- <span data-ttu-id="9fd8f-106">Lorsque vous [balisez des documents dans un ensemble de révision](tagging-documents.md).</span><span class="sxs-lookup"><span data-stu-id="9fd8f-106">When you [tag documents in a review set](tagging-documents.md).</span></span>

- <span data-ttu-id="9fd8f-107">Lorsque vous [analysez les données de cas dans un jeu de révision](analyzing-data-in-review-set.md) à l’aide de la détection à proximité, du Threading de messagerie électronique et de l’analyse des thèmes.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-107">When you [analyze case data in a review set](analyzing-data-in-review-set.md) by using near duplicate detection, email threading, and themes analytics.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="9fd8f-108">Questions fréquemment posées</span><span class="sxs-lookup"><span data-stu-id="9fd8f-108">Frequently asked questions</span></span>

<span data-ttu-id="9fd8f-109">**Comment puis-je créer une recherche pour collecter des éléments qui contiennent des caractères CJK ?**</span><span class="sxs-lookup"><span data-stu-id="9fd8f-109">**How do I create a search to collect items that contains CJK characters?**</span></span>

<span data-ttu-id="9fd8f-110">Vous pouvez utiliser les caractères CJK pour les [recherches par Mots clés](building-search-queries.md#keyword-searches), [les requêtes de mot clé et les conditions de recherche](keyword-queries-and-search-conditions.md) lors de la recherche de contenu dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-110">You can use CJK characters for [keyword searches](building-search-queries.md#keyword-searches), [keyword queries and search conditions](keyword-queries-and-search-conditions.md) when searching for content in Advanced eDiscovery.</span></span> <span data-ttu-id="9fd8f-111">La recherche de caractères CJK est également prise en charge lors de la recherche de contenu dans la recherche de contenu et eDiscovery de base.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-111">Searching for CJK characters is also supported when searching for content in Core eDiscovery and Content Search.</span></span>

<span data-ttu-id="9fd8f-112">Nous fournissons la prise en charge CJK pour tous les [opérateurs de recherche](keyword-queries-and-search-conditions.md#search-operators) et toutes les [conditions de recherche](keyword-queries-and-search-conditions.md#search-conditions), y compris les opérateurs booléens **and**, **or**, **not**et **near**.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-112">We provide CJK support for all [search operators](keyword-queries-and-search-conditions.md#search-operators) and [search conditions](keyword-queries-and-search-conditions.md#search-conditions), including the boolean operators **AND**, **OR**, **NOT**, and **NEAR**.</span></span>

<span data-ttu-id="9fd8f-113">Si vous êtes certain que les emplacements de contenu ou les éléments contiennent des caractères CJK, mais que les recherches ne renvoient pas de résultats, cliquez sur l’icône langue de la requête-pays/région.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-113">If you're certain that content locations or items contain CJK characters, but searches aren't returning any results, click the query language-country/region icon</span></span> ![Icône de langue de requête pays/région dans la recherche de contenu](../media/8d4b60c8-e1f1-40f9-88ae-ee2a7eca0886.png) <span data-ttu-id="9fd8f-115">et sélectionnez la valeur de code de culture du pays correspondant à la recherche.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-115">and select the corresponding language-country culture code value for the search.</span></span> <span data-ttu-id="9fd8f-116">La langue/région par défaut est neutre.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-116">The default language/region is neutral.</span></span>

<span data-ttu-id="9fd8f-117">**Puis-je Rechercher plusieurs langues en même temps ?**</span><span class="sxs-lookup"><span data-stu-id="9fd8f-117">**Can I search for multiple languages at once?**</span></span>

<span data-ttu-id="9fd8f-118">Cela dépend de votre scénario de recherche.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-118">It depends on your search scenario.</span></span>

- <span data-ttu-id="9fd8f-119">Lorsque vous [interrogez des données dans un jeu de réexamen](review-set-search.md) dans Advanced eDiscovery, vous pouvez rechercher plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-119">When you [query data in a review set](review-set-search.md) in Advanced eDiscovery, you can search for multiple languages.</span></span>

- <span data-ttu-id="9fd8f-120">Lorsque vous [créez une recherche pour collecter des données](create-search-to-collect-data.md), créez une recherche distincte pour chaque langue que vous ciblez.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-120">When you [create a search to collect data](create-search-to-collect-data.md), create a separate search for each language you're targeting.</span></span> <span data-ttu-id="9fd8f-121">Par exemple, si vous recherchez un document qui contient à la fois chinois et coréen, sélectionnez chinois pour votre première requête et sélectionnez coréen pour votre deuxième requête.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-121">For example, if you are searching for a document that contains both Chinese and Korean, select Chinese for your first query and select Korean for your second query.</span></span>

<span data-ttu-id="9fd8f-122">**Je ne vois pas l’icône de langue de requête pays/région pour sélectionner une langue pour les requêtes dans un jeu de révision. Comment puis-je spécifier un langage de requête dans une recherche de jeu de révision ?**</span><span class="sxs-lookup"><span data-stu-id="9fd8f-122">**I don't see the query language-country/region icon to select a language for queries in a review set. How can I specify a query language in a review set search?**</span></span>

<span data-ttu-id="9fd8f-123">Pour les requêtes de jeu de révision, il n’est pas nécessaire de spécifier une langue de document.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-123">For review set queries, you don't need to specify a document language.</span></span> <span data-ttu-id="9fd8f-124">Advanced eDiscovery détecte automatiquement les langues de document lorsque vous ajoutez du contenu à un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-124">Advanced eDiscovery automatically detects document languages when you add content to a review set.</span></span> <span data-ttu-id="9fd8f-125">Cela vous permet d’optimiser les résultats de votre requête dans un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-125">This helps you optimize your query results in a review set.</span></span>

<span data-ttu-id="9fd8f-126">**Puis-je voir les langues détectées dans les [métadonnées de fichier](view-documents-in-review-set.md#file-metadata)?**</span><span class="sxs-lookup"><span data-stu-id="9fd8f-126">**Can I see detected languages in [file metadata](view-documents-in-review-set.md#file-metadata)?**</span></span>

<span data-ttu-id="9fd8f-127">Non, vous ne pouvez pas voir les langues détectées dans les métadonnées de fichier.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-127">No, you can't see detected languages in file metadata.</span></span>

<span data-ttu-id="9fd8f-128">**Puis-je filtrer par langue de document dans un jeu de révision**?</span><span class="sxs-lookup"><span data-stu-id="9fd8f-128">**Can I filter by document languages in a review set**?</span></span>

<span data-ttu-id="9fd8f-129">Non, vous ne pouvez pas filtrer, trier ou Rechercher par langue de document dans un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-129">No, you can't filter, sort, or search by document languages in a review set.</span></span>

<span data-ttu-id="9fd8f-130">**Cette version CJC pour les scénarios d’ensembles de révision aura-t-elle une incidence sur l’ensemble des recherches existantes et sur les ensembles de révision ?**</span><span class="sxs-lookup"><span data-stu-id="9fd8f-130">**Will this CJK release for review set scenarios affect any of my existing searches and review sets?**</span></span>

<span data-ttu-id="9fd8f-131">Non, aucune de vos recherches existantes et de vos ensembles de révision ne change.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-131">No, none of your existing searches and review sets will change.</span></span> <span data-ttu-id="9fd8f-132">Vous n’avez pas besoin de réindexer les données existantes, et les résultats de recherche pour le texte anglais seront identiques.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-132">You don't need to reindex existing data, and search results for English text will be the same.</span></span>

<span data-ttu-id="9fd8f-133">**Comment puis-je modifier ma langue d’affichage pour le chinois, le japonais ou le coréen ?**</span><span class="sxs-lookup"><span data-stu-id="9fd8f-133">**How do I change my display language to Chinese, Japanese, or Korean?**</span></span>

<span data-ttu-id="9fd8f-134">Pour plus d’informations sur la façon de modifier la langue d’affichage et le fuseau horaire, consultez [la rubrique relative à la définition des paramètres de langue et de région pour Office 365](https://docs.microsoft.com/office365/troubleshoot/access-management/set-language-and-region).</span><span class="sxs-lookup"><span data-stu-id="9fd8f-134">For information about how to change display language and time zone, see [How to set language and region settings for Office 365](https://docs.microsoft.com/office365/troubleshoot/access-management/set-language-and-region).</span></span>

## <a name="known-issues"></a><span data-ttu-id="9fd8f-135">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="9fd8f-135">Known issues</span></span>

- <span data-ttu-id="9fd8f-136">La reconnaissance optique de caractères ne prend pas en charge les caractères CJK des fichiers image</span><span class="sxs-lookup"><span data-stu-id="9fd8f-136">OCR doesn't support CJK characters from image files</span></span>

- <span data-ttu-id="9fd8f-137">Les fichiers de messagerie (par exemple, \*. eml et \*. MSG) dans les [Annotations](view-documents-in-review-set.md#annotate-view) ne sont pas pris en charge pour les langues CJK.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-137">Email files (such as \*.eml and \*.msg) in [Annotate view](view-documents-in-review-set.md#annotate-view) aren't supported for CJK languages.</span></span>

- <span data-ttu-id="9fd8f-138">La mise en surbrillance des recherches dans l' [affichage de texte](view-documents-in-review-set.md#text-view) n’est pas prise en charge pour les langues CJK.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-138">Search hit highlighting in [Text view](view-documents-in-review-set.md#text-view) isn't supported for CJK languages.</span></span>

- <span data-ttu-id="9fd8f-139">Le [module de pertinence](using-relevance.md) utilisé pour analyser les données ne prend pas en charge les langues CJK.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-139">The [Relevance module](using-relevance.md) used to analyze data doesn't support CJK languages.</span></span>

- <span data-ttu-id="9fd8f-140">Les [conservations basées sur une requête](managing-holds.md#manage-non-custodial-holds) ne sont pas prises en charge pour les langues CJK.</span><span class="sxs-lookup"><span data-stu-id="9fd8f-140">[Query-based holds](managing-holds.md#manage-non-custodial-holds) aren't supported for CJK languages.</span></span> 
