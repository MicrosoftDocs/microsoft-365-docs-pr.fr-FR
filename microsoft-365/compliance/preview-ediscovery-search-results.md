---
title: Afficher un aperçu des résultats d’une recherche de découverte électronique
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MED150
- MET150
ms.custom:
- seo-marvel-apr2020
description: Afficher l’aperçu d’un exemple de résultats renvoyés par une recherche de contenu ou une recherche de découverte électronique principale dans le Centre de conformité Microsoft 365.
ms.openlocfilehash: a89c8c9ed2500b4e2a859c75be3da177203d1406
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52538587"
---
# <a name="preview-ediscovery-search-results"></a><span data-ttu-id="04634-103">Afficher un aperçu des résultats de la recherche de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="04634-103">Preview eDiscovery search results</span></span>

<span data-ttu-id="04634-104">Après avoir exécuté une recherche de contenu ou une recherche associée à un cas eDiscovery principal, vous pouvez afficher un aperçu d’un exemple des résultats renvoyés par la recherche.</span><span class="sxs-lookup"><span data-stu-id="04634-104">After you run a Content search or a search associated with a Core eDiscovery case, you can preview a sample of the results returned by the search.</span></span> <span data-ttu-id="04634-105">L’aperçu des éléments renvoyés par la requête de recherche peut vous aider à déterminer si la recherche retourne les résultats que vous espériez, ou si vous devez modifier la requête de recherche et réexécuter la recherche.</span><span class="sxs-lookup"><span data-stu-id="04634-105">Previewing items returned by the search query can help you determine if the search is returning the results you hope for or if you need to change the search query and rerun the search.</span></span>

<span data-ttu-id="04634-106">Pour afficher l’aperçu d’un exemple de résultats renvoyés par une recherche :</span><span class="sxs-lookup"><span data-stu-id="04634-106">To preview a sample of results returned by a search:</span></span>

1. <span data-ttu-id="04634-107">Dans le Centre de conformité Microsoft 365, allez sur la page de recherche de contenu ou sur un cas de découverte électronique principal.</span><span class="sxs-lookup"><span data-stu-id="04634-107">In the Microsoft 365 compliance center, go to the Content search page or a Core eDiscovery case.</span></span>

2. <span data-ttu-id="04634-108">Sélectionnez Rechercher pour afficher la page volante.</span><span class="sxs-lookup"><span data-stu-id="04634-108">Select search to display the flyout page.</span></span>

3. <span data-ttu-id="04634-109">En bas de la page volante, cliquez sur **Échantillon d’évaluation**.</span><span class="sxs-lookup"><span data-stu-id="04634-109">On the bottom of the flyout page, click **Review sample**.</span></span>

   ![Cliquez sur Exemple de révision dans la page volante pour afficher un aperçu des résultats](../media/PreviewSearchResults1.png)

   <span data-ttu-id="04634-111">Une page s’affiche et contient un échantillon des résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="04634-111">A page is displayed containing a sample of the search results.</span></span>

4. <span data-ttu-id="04634-112">Sélectionnez un élément pour afficher son contenu dans le volet de lecture.</span><span class="sxs-lookup"><span data-stu-id="04634-112">Select an item to view its contents in the reading pane.</span></span>

   ![Afficher un aperçu des éléments dans le volet de lecture](../media/PreviewSearchResults2.png)

   <span data-ttu-id="04634-114">Dans la capture d’écran précédente, notez que les mots clés de la requête de recherche sont mis en évidence lors de l’aperçu des éléments.</span><span class="sxs-lookup"><span data-stu-id="04634-114">In the previous screenshot, notice that keywords from the search query are highlighted when you preview items.</span></span>

## <a name="how-the-search-result-samples-are-selected"></a><span data-ttu-id="04634-115">Comment les échantillons de résultats de recherche sont sélectionnés</span><span class="sxs-lookup"><span data-stu-id="04634-115">How the search result samples are selected</span></span>

<span data-ttu-id="04634-116">Un maximum de 1 000 éléments sélectionnés de façon aléatoire sont disponibles pour aperçu.</span><span class="sxs-lookup"><span data-stu-id="04634-116">A maximum of 1,000 randomly selected items are available to preview.</span></span> <span data-ttu-id="04634-117">Outre une sélection aléatoire, les éléments disponibles pour aperçu doivent également répondre aux critères suivants :</span><span class="sxs-lookup"><span data-stu-id="04634-117">In addition to being randomly selected, items available for preview must also meet the following criteria:</span></span>

- <span data-ttu-id="04634-118">Un maximum de 100 éléments à partir d’un emplacement de contenu unique (une boîte aux lettres ou un site) peuvent être prévisualiser.</span><span class="sxs-lookup"><span data-stu-id="04634-118">A maximum of 100 items from a single content location (a mailbox or a site) can be previewed.</span></span> <span data-ttu-id="04634-119">Cela signifie qu’il est possible que moins de 1 000 éléments soient disponibles pour l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="04634-119">This means that it's possible that less than 1,000 items might be available for preview.</span></span> <span data-ttu-id="04634-120">Par exemple, si vous recherchez quatre boîtes aux lettres et que la recherche renvoie 1 500 éléments estimés, seuls 400 seront disponibles pour la prévisualisation, car seuls 100 éléments de chaque boîte aux lettres peuvent être prévisualisés.</span><span class="sxs-lookup"><span data-stu-id="04634-120">For example, if you search four mailboxes and the search returns 1,500 estimated items, only 400 will be available for preview because only 100 items from each mailbox can be previewed.</span></span>

- <span data-ttu-id="04634-121">Pour les éléments de boîte aux lettres, seuls les courriers électroniques peuvent être aperçus.</span><span class="sxs-lookup"><span data-stu-id="04634-121">For mailbox items, only email messages are available to preview.</span></span> <span data-ttu-id="04634-122">Les éléments tels que les tâches, les éléments de calendrier et les contacts ne peuvent pas être aperçus.</span><span class="sxs-lookup"><span data-stu-id="04634-122">Items like tasks, calendar items, and contacts can't be previewed.</span></span>

- <span data-ttu-id="04634-123">Pour les éléments de site, seuls les documents peuvent être aperçus.</span><span class="sxs-lookup"><span data-stu-id="04634-123">For site items, only documents are available to preview.</span></span> <span data-ttu-id="04634-124">Les éléments tels que les dossiers, listes ou pièces jointes de liste ne peuvent pas être prévisualisés.</span><span class="sxs-lookup"><span data-stu-id="04634-124">Items like folders, lists, or list attachments can't be previewed.</span></span>

## <a name="file-types-supported-when-previewing-search-results"></a><span data-ttu-id="04634-125">Types de fichiers pris en charge lors de l’aperçu des résultats de la recherche</span><span class="sxs-lookup"><span data-stu-id="04634-125">File types supported when previewing search results</span></span>

<span data-ttu-id="04634-126">Vous pouvez afficher un aperçu des types de fichiers pris en charge dans le volet de visualisation.</span><span class="sxs-lookup"><span data-stu-id="04634-126">You can preview supported file types in the preview pane.</span></span> <span data-ttu-id="04634-127">Si un type de fichier n’est pas pris en charge, vous devez télécharger une copie du fichier sur votre ordinateur local (en cliquant sur **Télécharger l’élément d’origine**).</span><span class="sxs-lookup"><span data-stu-id="04634-127">If a file type isn't supported, you have to download a copy of the file to your local computer (by clicking **Download original item**).</span></span> <span data-ttu-id="04634-128">Pour les pages web .aspx, l’URL de la page est incluse, même si vous n’êtes peut-être pas autorisé à accéder à la page.</span><span class="sxs-lookup"><span data-stu-id="04634-128">For .aspx Web pages, the URL for the page is included though you may not have permissions to access the page.</span></span> <span data-ttu-id="04634-129">Les éléments non indexés ne peuvent pas être affichés en aperçu.</span><span class="sxs-lookup"><span data-stu-id="04634-129">Unindexed items aren't available for previewing.</span></span>

<span data-ttu-id="04634-130">Les types de fichiers suivants sont pris en charge et peuvent être prévisualisés dans le volet résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="04634-130">The following file types are supported and can be previewed in the search results pane.</span></span>
  
- <span data-ttu-id="04634-131">.txt, .html, .mhtml</span><span class="sxs-lookup"><span data-stu-id="04634-131">.txt, .html, .mhtml</span></span>

- <span data-ttu-id="04634-132">.eml</span><span class="sxs-lookup"><span data-stu-id="04634-132">.eml</span></span>

- <span data-ttu-id="04634-133">.doc, .docx, .docm</span><span class="sxs-lookup"><span data-stu-id="04634-133">.doc, .docx, .docm</span></span>

- <span data-ttu-id="04634-134">.pptm, .pptx</span><span class="sxs-lookup"><span data-stu-id="04634-134">.pptm, .pptx</span></span>

- <span data-ttu-id="04634-135">.pdf</span><span class="sxs-lookup"><span data-stu-id="04634-135">.pdf</span></span>

<span data-ttu-id="04634-136">De plus, les types de conteneur de fichier suivants sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="04634-136">Also, the following file container types are supported.</span></span> <span data-ttu-id="04634-137">Vous pouvez afficher la liste des fichiers dans le conteneur dans le volet de visualisation.</span><span class="sxs-lookup"><span data-stu-id="04634-137">You can view the list of files in the container in the preview pane.</span></span>
  
- <span data-ttu-id="04634-138">.zip</span><span class="sxs-lookup"><span data-stu-id="04634-138">.zip</span></span>

- <span data-ttu-id="04634-139">.gzip</span><span class="sxs-lookup"><span data-stu-id="04634-139">.gzip</span></span>