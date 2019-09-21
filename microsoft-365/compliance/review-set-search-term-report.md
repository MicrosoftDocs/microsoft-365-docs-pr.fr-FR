---
title: Générer un rapport de termes de recherche pour un jeu de révision
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 877c0017359ab9193c4cae81cbef4240909053a8
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37080349"
---
# <a name="generate-search-term-report-for-a-review-set"></a><span data-ttu-id="8ae6c-102">Générer un rapport de termes de recherche pour un jeu de révision</span><span class="sxs-lookup"><span data-stu-id="8ae6c-102">Generate search term report for a review set</span></span>

<span data-ttu-id="8ae6c-103">Dans eDiscovery, l’une des conditions les plus fréquemment utilisées pour demander des documents consiste à utiliser des termes de recherche par mot clé.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-103">In eDiscovery, one of the most frequently used conditions for querying documents is by using keyword search terms.</span></span> <span data-ttu-id="8ae6c-104">En identifiant les documents qui contiennent les mots clés spécifiques (également appelés *termes*) qui sont importants pour un cas, les réviseurs peuvent commencer à comprendre ce qu’ils font face.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-104">By identifying documents that contain the specific keywords (also referred to as *terms*) that are important to a case, reviewers can begin to get a high-level understanding of what they are facing.</span></span> <span data-ttu-id="8ae6c-105">Dans Advanced eDiscovery dans Microsoft 365, vous pouvez le faire précisément en générant des rapports de termes de recherche sur les requêtes sauvegardées au sein d’un ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-105">In Advanced eDiscovery in Microsoft 365, you can do precisely this by generating search term reports on saved queries within a review set.</span></span>

## <a name="step-1-create-a-saved-query-in-the-review-set"></a><span data-ttu-id="8ae6c-106">Étape 1 : créer une requête enregistrée dans l’ensemble de révision</span><span class="sxs-lookup"><span data-stu-id="8ae6c-106">Step 1: Create a saved query in the review set</span></span>

<span data-ttu-id="8ae6c-107">Pour générer un rapport de termes de recherche pertinent, créez une requête enregistrée qui définit l’ensemble des documents dans l’ensemble de révision pour lequel vous souhaitez générer un rapport de termes de recherche.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-107">To generate a meaningful search term report, create a saved query that defines the set of documents in the review set that you want to generate a search term report for.</span></span> <span data-ttu-id="8ae6c-108">Par exemple, vous pouvez utiliser une plage de dates ou le jeu de termes de recherche réel (à l’aide de la carte de condition de mots-clés) pour créer la requête.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-108">For example, you can use a date range or the actual set of search terms (by using the Keywords condition card) to create the query.</span></span> <span data-ttu-id="8ae6c-109">Pour en savoir plus sur les requêtes Set de révision, consultez [la rubrique Query the Data in a Review Set](review-set-search.md).</span><span class="sxs-lookup"><span data-stu-id="8ae6c-109">To learn more about review set queries, see [Query the data in a review set](review-set-search.md).</span></span>

## <a name="step-2-generate-a-search-term-report"></a><span data-ttu-id="8ae6c-110">Étape 2 : générer un rapport de termes de recherche</span><span class="sxs-lookup"><span data-stu-id="8ae6c-110">Step 2: Generate a search term report</span></span>

<span data-ttu-id="8ae6c-111">Il existe deux façons de générer un rapport de termes de recherche : via le menu contextuel de la requête enregistrée que vous avez créée à l’étape 1, ou via la console de gestion des rapports sur les termes de la recherche.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-111">There are two different ways to generate a search term report: through the context menu of the saved query you created in Step 1, or through the search term report management console.</span></span>

- <span data-ttu-id="8ae6c-112">Pour utiliser le menu contextuel, ouvrez le menu contextuel de la requête enregistrée que vous avez créée à l’étape 1, puis cliquez sur **générer un rapport de termes de recherche**.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-112">To use the context menu, open the context menu of the saved query you created in Step 1, and click **Generate search term report**.</span></span>

- <span data-ttu-id="8ae6c-113">Pour utiliser la console de gestion, accédez à **Manage Review set > view search term Reports**, cliquez sur **New**, puis sélectionnez la requête enregistrée que vous avez créée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-113">To use the management console, go to **Manage review set > View search term reports**, click **New**, and then select the saved query you created in Step 1.</span></span>

<span data-ttu-id="8ae6c-114">Ensuite, entrez les termes sur lesquels vous souhaitez créer un rapport, séparés par des sauts de ligne ; Si la requête enregistrée que vous avez créée à l’étape 1 condition de mot-clé utilisée, la page de menu volant est pré-renseignée avec les termes de la première carte de condition de mot clé utilisée dans la requête enregistrée.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-114">Then, enter the terms you would like to report on, separated by newline; if the saved query that you created in Step 1 used keyword condition card, the flyout page will be pre-populated with the terms from the first keyword condition card used in the saved query.</span></span>

<span data-ttu-id="8ae6c-115">Ensuite, sélectionnez jusqu’à trois tableaux croisés dynamiques à afficher, puis cliquez sur **générer**pour démarrer le travail de génération de l’état de la recherche.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-115">Then, select up to three pivots to report on, and click on **Generate**, which will start the search term report generation job.</span></span>

### <a name="what-is-a-pivot"></a><span data-ttu-id="8ae6c-116">Qu’est-ce qu’un tableau croisé dynamique ?</span><span class="sxs-lookup"><span data-stu-id="8ae6c-116">What is a pivot?</span></span>

<span data-ttu-id="8ae6c-117">Les tableaux croisés dynamiques indiquent comment le rapport sera organisé.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-117">Pivots are how the report will be organized.</span></span> <span data-ttu-id="8ae6c-118">Prenons l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-118">Consider the following example.</span></span>

- <span data-ttu-id="8ae6c-119">La requête enregistrée extrait 10 documents : Doc1 à Doc10.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-119">The saved query retrieves 10 documents: doc1 thru doc10.</span></span>

- <span data-ttu-id="8ae6c-120">Doc1, Doc2, Doc3, doc4, Doc5, Doc6 et Doc7 contiennent le terme « eDiscovery ».</span><span class="sxs-lookup"><span data-stu-id="8ae6c-120">doc1, doc2, doc3, doc4, doc5, doc6, and doc7 contain the term "eDiscovery".</span></span>

- <span data-ttu-id="8ae6c-121">Doc6, Doc7, Doc8, Doc9 et Doc10 contiennent le terme « enquête ».</span><span class="sxs-lookup"><span data-stu-id="8ae6c-121">doc6, doc7, doc8, doc9, and doc10 contain the term "Investigation".</span></span>

- <span data-ttu-id="8ae6c-122">Doc1, Doc3, Doc5, Doc7, Doc9 proviennent du dépositaire A.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-122">doc1, doc3, doc5, doc7, doc9 are from custodian A.</span></span>

- <span data-ttu-id="8ae6c-123">Doc2, doc4, Doc6, Doc8, Doc10 proviennent du dépositaire B.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-123">doc2, doc4, doc6, doc8, doc10 are from custodian B.</span></span>

<span data-ttu-id="8ae6c-124">Dans ce cas, si vous générez un rapport de terme de recherche sur les termes « eDiscovery » et « investigation » et pivot sur les dépositaires, l’état de terme de recherche serait organisé comme suit :</span><span class="sxs-lookup"><span data-stu-id="8ae6c-124">In this case, if you were to generate a search term report on the terms "eDiscovery" and "Investigation" and pivot on custodians, the search term report would be organized as follows:</span></span>

- <span data-ttu-id="8ae6c-125">« eDiscovery »-dépositaire A : 4 documents</span><span class="sxs-lookup"><span data-stu-id="8ae6c-125">"eDiscovery" - custodian A: 4 documents</span></span>

- <span data-ttu-id="8ae6c-126">« eDiscovery »-dépositaire B : 3 documents</span><span class="sxs-lookup"><span data-stu-id="8ae6c-126">"eDiscovery" - custodian B: 3 documents</span></span>

- <span data-ttu-id="8ae6c-127">"Enquête"-dépositaire A : 2 documents</span><span class="sxs-lookup"><span data-stu-id="8ae6c-127">"Investigation" - custodian A: 2 documents</span></span>

- <span data-ttu-id="8ae6c-128">"Enquête" : dépositaire B : 3 documents</span><span class="sxs-lookup"><span data-stu-id="8ae6c-128">"Investigation" - custodian B: 3 documents</span></span>

## <a name="step-3-download-report"></a><span data-ttu-id="8ae6c-129">Étape 3 : Télécharger le rapport</span><span class="sxs-lookup"><span data-stu-id="8ae6c-129">Step 3: Download report</span></span>

<span data-ttu-id="8ae6c-130">Dans la console de gestion des termes de recherche, vous pouvez suivre l’état d’une tâche de rapport de termes de recherche précédemment créée.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-130">In the search term management console, you can track the status of a previously-created search term report job.</span></span> <span data-ttu-id="8ae6c-131">Une fois le travail terminé, vous pouvez cliquer sur la ligne de l’état de terme de recherche et cliquer sur « Télécharger » pour télécharger l’état de terme de recherche dans un format CSV.</span><span class="sxs-lookup"><span data-stu-id="8ae6c-131">Once the job completes, you can click on the row for the search term report and click "Download", which will download the search term report in a CSV format.</span></span> <span data-ttu-id="8ae6c-132">Il y aura une ligne par (terme de recherche, tableaux croisés dynamiques) tuple, et chaque ligne contiendra les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ae6c-132">There will be one row per (search term, pivots) tuple, and each row will contain the following information:</span></span>

- <span data-ttu-id="8ae6c-133">Combien de documents ont été extraits ?</span><span class="sxs-lookup"><span data-stu-id="8ae6c-133">How many documents were retrieved?</span></span>

- <span data-ttu-id="8ae6c-134">Combien de fois le terme de recherche a-t-il été trouvé dans les documents ?</span><span class="sxs-lookup"><span data-stu-id="8ae6c-134">How many times was the search term found across the documents?</span></span>

- <span data-ttu-id="8ae6c-135">Quel est le volume total des documents extraits ?</span><span class="sxs-lookup"><span data-stu-id="8ae6c-135">What is the total volume of retrieved documents?</span></span>

- <span data-ttu-id="8ae6c-136">Combien de familles ont été récupérées ?</span><span class="sxs-lookup"><span data-stu-id="8ae6c-136">How many families were retrieved?</span></span>

- <span data-ttu-id="8ae6c-137">Quel est le nombre total de documents de ces familles, y compris les documents qui n’ont pas le terme de recherche ?</span><span class="sxs-lookup"><span data-stu-id="8ae6c-137">What is the total document count of those families, including the documents that did not have the search term?</span></span>

- <span data-ttu-id="8ae6c-138">Quel est le volume total de ce qui précède ?</span><span class="sxs-lookup"><span data-stu-id="8ae6c-138">What is the total volume of the above?</span></span>