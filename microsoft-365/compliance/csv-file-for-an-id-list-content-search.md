---
title: Préparer un fichier CSV pour une recherche de contenu de liste d’ID
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
ms.assetid: 82c97bb4-2b64-4edc-804d-cedbda525d22
ms.custom:
- seo-marvel-apr2020
description: Utilisez un fichier CSV d’une recherche de contenu existante pour créer une recherche de liste d’ID qui renvoie des éléments de courrier spécifiques.
ms.openlocfilehash: 37a398d0896fcfd7b7282bda1f6a549ed9f53601
ms.sourcegitcommit: efb932db63ad3ab4af4b585428d567d069410e4e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2021
ms.locfileid: "52311537"
---
# <a name="prepare-a-csv-file-for-an-id-list-content-search"></a><span data-ttu-id="b549e-103">Préparer un fichier CSV pour une recherche de contenu de liste d’ID</span><span class="sxs-lookup"><span data-stu-id="b549e-103">Prepare a CSV file for an ID list Content search</span></span>

<span data-ttu-id="b549e-104">Vous pouvez rechercher des messages électroniques de boîte aux lettres spécifiques et d’autres éléments de boîte aux lettres à l’aide d’Exchange ID de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="b549e-104">You can search for specific mailbox email messages and other mailbox items using a list of Exchange IDs.</span></span> <span data-ttu-id="b549e-105">Pour créer une recherche de liste d'identification, vous soumettez un fichier CSV (valeur séparée par des virgules) qui identifie les éléments spécifiques de la boîte aux lettres à rechercher.</span><span class="sxs-lookup"><span data-stu-id="b549e-105">To create an ID list search, you submit a comma-separated value (CSV) file that identifies the specific mailbox items to search for.</span></span> <span data-ttu-id="b549e-106">Pour ce fichier CSV, vous utilisez le fichier **Results.csv** ou le fichier Items.csv **nonndexé** inclus lorsque vous exportez les résultats de recherche de contenu ou exportez un rapport de recherche de contenu à partir d’une recherche de contenu existante.</span><span class="sxs-lookup"><span data-stu-id="b549e-106">For this CSV file, you use the **Results.csv** file or the **Unindexed Items.csv** file that are included when you export the Content search results or export a Content search report from an existing Content search.</span></span> <span data-ttu-id="b549e-107">Ensuite, vous modifiez l’un de ces fichiers pour indiquer les éléments spécifiques à rechercher, créez une recherche de liste d’ID et soumettez le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="b549e-107">Then you edit one of these files to indicate the specific items to search for, create a new ID list search, and submit the CSV file.</span></span>

<span data-ttu-id="b549e-108">**Pourquoi créer une recherche de liste d’ID ?**</span><span class="sxs-lookup"><span data-stu-id="b549e-108">**Why create an ID list search?**</span></span> <span data-ttu-id="b549e-109">Si vous ne parvenez pas à déterminer si un élément répond à une demande eDiscovery en fonction des métadonnées dans les fichiers **Results.csv** ou **non** Items.csv, vous pouvez utiliser une recherche de liste d’ID pour rechercher, afficher un aperçu, puis exporter cet élément pour déterminer s’il répond au cas que vous examinez.</span><span class="sxs-lookup"><span data-stu-id="b549e-109">If you're unable to determine if an item is responsive to an eDiscovery request based on the metadata in the **Results.csv** or **Unindexed Items.csv** files, you can use an ID list search to find, preview, and then export that item to determine if it's responsive to the case you're investigating.</span></span> <span data-ttu-id="b549e-110">Les recherches de liste d’ID sont généralement utilisées pour rechercher et renvoyer un ensemble spécifique d’éléments nonndex.</span><span class="sxs-lookup"><span data-stu-id="b549e-110">ID list searches are typically used to search for and return a specific set of unindexed items.</span></span>

<span data-ttu-id="b549e-111">Voici une vue d’ensemble rapide du processus de création d’une recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="b549e-111">Here's a quick overview of the process for creating an ID list search.</span></span>

1. <span data-ttu-id="b549e-112">Créez et exécutez une recherche dans le centre Microsoft 365 conformité.</span><span class="sxs-lookup"><span data-stu-id="b549e-112">Create and run a new search in the Microsoft 365 compliance center.</span></span>

2. <span data-ttu-id="b549e-113">Exporter les résultats de recherche de contenu ou le rapport de recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="b549e-113">Export the content search results or the content search report.</span></span> <span data-ttu-id="b549e-114">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="b549e-114">For more information, see:</span></span>

    - [<span data-ttu-id="b549e-115">Exporter les résultats de la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="b549e-115">Export Content search results</span></span>](export-search-results.md)

    - [<span data-ttu-id="b549e-116">Exporter un rapport de recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="b549e-116">Export a Content search report</span></span>](export-a-content-search-report.md)

3. <span data-ttu-id="b549e-117">Modifiez **leResults.csv** fichier  ou le fichier Items.csvnon non Items.csvet identifiez les éléments de boîte aux lettres spécifiques à inclure dans la recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="b549e-117">Edit the **Results.csv** file or **Unindexed Items.csv** file and identify the specific mailbox items to include in the ID list search.</span></span> <span data-ttu-id="b549e-118">Consultez [les instructions de](#prepare-the-csv-file-for-an-id-list-search) préparation d’un fichier CSV pour une recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="b549e-118">See the [instructions](#prepare-the-csv-file-for-an-id-list-search) for preparing a CSV file for an ID list search.</span></span>

4. <span data-ttu-id="b549e-119">Créez une recherche de liste d’ID (voir [les instructions)](#create-an-id-list-search)et soumettez le fichier CSV que vous avez préparé.</span><span class="sxs-lookup"><span data-stu-id="b549e-119">Create a new ID list search (see the [instructions](#create-an-id-list-search)) and submit the CSV file that you prepared.</span></span> <span data-ttu-id="b549e-120">La requête de recherche créée recherche uniquement les éléments sélectionnés dans le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="b549e-120">The search query that's created will only search for the items selected in the CSV file.</span></span>

> [!NOTE]
> <span data-ttu-id="b549e-121">Les recherches de liste d’ID sont uniquement pris en charge pour les éléments de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="b549e-121">ID list searches are only supported for mailbox items.</span></span> <span data-ttu-id="b549e-122">Vous ne pouvez pas rechercher d’SharePoint et OneDrive documents dans une recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="b549e-122">You can't search for SharePoint and OneDrive documents in an ID list search.</span></span>

## <a name="prepare-the-csv-file-for-an-id-list-search"></a><span data-ttu-id="b549e-123">Préparer le fichier CSV pour une recherche de liste d’ID</span><span class="sxs-lookup"><span data-stu-id="b549e-123">Prepare the CSV file for an ID list search</span></span>

<span data-ttu-id="b549e-124">Après avoir exporté les résultats de recherche ou le rapport pour une recherche, effectuez les étapes suivantes pour préparer le fichier CSV pour une recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="b549e-124">After you export the search results or report for a search, perform the following steps to prepare the CSV file for an ID list search.</span></span> <span data-ttu-id="b549e-125">Ce fichier CSV identifie chaque élément de la recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="b549e-125">This CSV file identifies every item in the ID list search.</span></span>

<span data-ttu-id="b549e-126">Vous pouvez utiliser un fichier CSV à partir d’une recherche qui incluait des sites SharePoint et des comptes OneDrive, mais vous pouvez uniquement sélectionner des éléments de boîte aux lettres pour une recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="b549e-126">You can use a CSV file from a search that included SharePoint sites and OneDrive accounts, but you can only select mailbox items for an ID list search.</span></span> <span data-ttu-id="b549e-127">Si vous sélectionnez un document dans SharePoint ou OneDrive, la validation du fichier CSV échoue lorsque vous créez une recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="b549e-127">If you select a document in SharePoint or OneDrive, the CSV file will fail validation when you create an ID list search.</span></span>

1. <span data-ttu-id="b549e-128">Ouvrez **leResults.csv** **fichier** Items.csvnon Excel.</span><span class="sxs-lookup"><span data-stu-id="b549e-128">Open the **Results.csv** or **Unindexed Items.csv** file in Excel.</span></span>

2. <span data-ttu-id="b549e-129">Dans la **colonne Sélectionnée,** tapez **Oui** dans la cellule qui correspond à l’élément que vous souhaitez rechercher.</span><span class="sxs-lookup"><span data-stu-id="b549e-129">In the **Selected** column, type **Yes** in the cell that corresponds to the item that you want to search for.</span></span> <span data-ttu-id="b549e-130">Répétez cette étape pour chaque élément que vous souhaitez rechercher.</span><span class="sxs-lookup"><span data-stu-id="b549e-130">Repeat this step for every item that you want to search for.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b549e-131">Lorsque vous ouvrez le fichier CSV dans Excel, le format de données de la colonne **ID** de document a peut-être été modifié en **Général**.</span><span class="sxs-lookup"><span data-stu-id="b549e-131">When you open the CSV file in Excel, the data format for the **Document ID** column may have been changed to **General**.</span></span> <span data-ttu-id="b549e-132">Cela entraîne l’affichage de l’ID de document pour un élément en notation scientifique.</span><span class="sxs-lookup"><span data-stu-id="b549e-132">This results in displaying the document ID for an item in scientific notation.</span></span> <span data-ttu-id="b549e-133">Par exemple, l’ID de document « 481037338205 » est affiché sous la référence « 4.81037E+11 ».</span><span class="sxs-lookup"><span data-stu-id="b549e-133">For example, the document ID of "481037338205" is displayed as "4.81037E+11".</span></span> <span data-ttu-id="b549e-134">Si cela se produit, vous devez effectuer les étapes suivantes  pour modifier le format de données de la colonne **ID** de document en numéro afin de restaurer le format correct pour l’ID de document.</span><span class="sxs-lookup"><span data-stu-id="b549e-134">If this happens, you have to perform the next steps to change the data format of the **Document ID** column to **Number** to restore the correct format for the document ID.</span></span> <span data-ttu-id="b549e-135">Si vous ne le faites pas, la recherche de liste d’ID qui utilise le fichier CSV échoue.</span><span class="sxs-lookup"><span data-stu-id="b549e-135">If you don't do this, the ID list search that uses the CSV file will fail.</span></span>

3. <span data-ttu-id="b549e-136">Cliquez avec le bouton droit sur **l’intégralité de** la colonne ID de document et **sélectionnez Format de cellule.**</span><span class="sxs-lookup"><span data-stu-id="b549e-136">Right-click the entire **Document ID** column and select **Format Cells**.</span></span>

4. <span data-ttu-id="b549e-137">Dans la **zone Catégorie,** cliquez sur **Numéro**.</span><span class="sxs-lookup"><span data-stu-id="b549e-137">In the **Category** box, click **Number**.</span></span>

5. <span data-ttu-id="b549e-138">Modifiez le nombre de décimales sur **0,** puis cliquez sur **OK** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="b549e-138">Change the number of decimal places to **0**, and then click **OK** to save your changes.</span></span> <span data-ttu-id="b549e-139">Notez que les valeurs de la colonne ID de document sont modifiées en nombres.</span><span class="sxs-lookup"><span data-stu-id="b549e-139">Notice that the values in the Document ID column are changed to numbers.</span></span>

    <span data-ttu-id="b549e-140">Voici un exemple de fichier CSV prêt à être envoyé pour une recherche de contenu de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="b549e-140">Here's an example of a CSV file that's ready to be submitted for an ID list content search.</span></span>

    ![Exemple de fichier CSV pour une recherche de contenu ciblée](../media/SearchIDListCSVFile.png)

6. <span data-ttu-id="b549e-142">Enregistrez le fichier CSV ou utilisez **Enregistrer sous** pour enregistrer le fichier avec un nom de fichier différent.</span><span class="sxs-lookup"><span data-stu-id="b549e-142">Save the CSV file or use **Save As** to the save the file with different file name.</span></span> <span data-ttu-id="b549e-143">Dans les deux cas, n’oubliez pas d’enregistrer le fichier au format CSV.</span><span class="sxs-lookup"><span data-stu-id="b549e-143">In both cases, be sure to save the file with the CSV format.</span></span>

## <a name="create-an-id-list-search"></a><span data-ttu-id="b549e-144">Créer une recherche de liste d’ID</span><span class="sxs-lookup"><span data-stu-id="b549e-144">Create an ID list search</span></span>

<span data-ttu-id="b549e-145">L’étape suivante consiste à créer une recherche de liste d’ID et à soumettre le fichier CSV que vous avez préparé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="b549e-145">The next step is to create a new ID list search and submit the CSV file that you prepared in the previous step.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b549e-146">Vous devez créer une recherche de liste d’ID au plus 2 jours après l’exportation des résultats ou du rapport de recherche.</span><span class="sxs-lookup"><span data-stu-id="b549e-146">You should create an ID list search no more than 2 days after exporting the search results or report.</span></span> <span data-ttu-id="b549e-147">Si les résultats ou le rapport de recherche exportés il y a plus de 2 jours, vous devez ré-exporter les résultats ou le rapport de recherche pour générer des fichiers CSV mis à jour.</span><span class="sxs-lookup"><span data-stu-id="b549e-147">If the search results or report where exported more than 2 days ago, you should re-export the search results or report to generate updated CSV files.</span></span> <span data-ttu-id="b549e-148">Vous pouvez ensuite préparer l’un des fichiers CSV mis à jour et l’utiliser pour créer une recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="b549e-148">Then you can prepare one of the updated CSV files and use it to create an ID list search.</span></span>

1. <span data-ttu-id="b549e-149">Accédez à <https://compliance.microsoft.com> et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="b549e-149">Go to <https://compliance.microsoft.com> and sign in.</span></span>

2. <span data-ttu-id="b549e-150">Dans le volet de navigation gauche du centre de conformité Microsoft 365, cliquez sur **Afficher tout** , puis sur **Recherche de contenu**.</span><span class="sxs-lookup"><span data-stu-id="b549e-150">In the left navigation pane of the Microsoft 365 compliance center, click **Show all**, and then click **Content search**.</span></span>

3. <span data-ttu-id="b549e-151">Dans la page **de recherche de** contenu, cliquez sur Rechercher par liste **d’ID.**</span><span class="sxs-lookup"><span data-stu-id="b549e-151">On the **Content search** page, click **Search by ID List**.</span></span>

4. <span data-ttu-id="b549e-152">Dans le programme volant Rechercher par **liste d’ID,** nommez  la recherche (et éventuellement décrivez-la), puis cliquez sur Parcourir et sélectionnez le fichier CSV que vous avez préparé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="b549e-152">On the **Search by ID List** flyout, name the search (and optionally describe it) and then click **Browse** and select the CSV file that you prepared in the previous step.</span></span>

    <span data-ttu-id="b549e-153">Microsoft 365 tente de valider le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="b549e-153">Microsoft 365 attempts to validate the CSV file.</span></span> <span data-ttu-id="b549e-154">Si la validation échoue, un message d’erreur s’affiche pour vous aider à résoudre les erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="b549e-154">If the validation is unsuccessful, an error message is displayed that might help you troubleshoot the validation errors.</span></span> <span data-ttu-id="b549e-155">Le fichier CSV doit être validé avec succès pour créer une recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="b549e-155">The CSV file has to be successfully validated to create an ID list search.</span></span>

5. <span data-ttu-id="b549e-156">Une fois le fichier CSV validé, cliquez sur **Rechercher** pour créer la recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="b549e-156">After the CSV file is successfully validated, click **Search** to create the ID list search.</span></span>

    <span data-ttu-id="b549e-157">Voici un exemple de page volante d’une recherche de liste d’ID qui affiche la requête générée et le nombre estimé de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="b549e-157">Here's an example of the flyout page from an ID list search that shows the query that's generated and the estimated number of search results.</span></span>

    ![Requête de recherche pour la recherche de liste d’ID](../media/SearchIDListFlyout.png)

    <span data-ttu-id="b549e-159">Le nombre d’éléments estimés affichés dans les statistiques pour la recherche d’ID doit correspondre au nombre d’éléments que vous avez sélectionnés dans le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="b549e-159">The number of estimated items displayed in statistics for the ID search should match the number of items that you selected in the CSV file.</span></span>

6. <span data-ttu-id="b549e-160">Afficher un aperçu ou exporter les éléments renvoyés par la recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="b549e-160">Preview or export the items returned by the ID list search.</span></span>

## <a name="more-information"></a><span data-ttu-id="b549e-161">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b549e-161">More information</span></span>

<span data-ttu-id="b549e-162">Si vous déplacez une boîte aux lettres après avoir créé une recherche de liste d’ID, la requête de recherche ne retourne pas les éléments spécifiés.</span><span class="sxs-lookup"><span data-stu-id="b549e-162">If you move a mailbox after creating an ID list search, the query for the search won't return the specified items.</span></span> <span data-ttu-id="b549e-163">Cela est dû au fait que la **propriété DocumentId** des éléments de boîte aux lettres est modifiée lorsqu’une boîte aux lettres est déplacée.</span><span class="sxs-lookup"><span data-stu-id="b549e-163">That's because the **DocumentId** property for mailbox items is changed when a mailbox is moved.</span></span> <span data-ttu-id="b549e-164">Dans les rares cas où une boîte aux lettres est déplacée après avoir créé une recherche de liste d’ID, vous devez créer une recherche de contenu (ou mettre à jour les résultats de recherche pour une recherche existante), puis exporter les résultats ou le rapport de recherche pour générer des fichiers CSV mis à jour qui peuvent être utilisés pour créer une recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="b549e-164">In the rare instance when a mailbox is moved after you create an ID list search, you should create a new Content search (or update the search results for an existing search) and then export the search results or report to generate updated CSV files that can be used to create a new ID list search.</span></span>
