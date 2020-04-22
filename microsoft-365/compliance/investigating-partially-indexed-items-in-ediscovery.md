---
title: Étude des éléments partiellement indexés dans eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/26/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid: MOE150
ms.assetid: 4e8ff113-6361-41e2-915a-6338a7e2a1ed
description: Les éléments partiellement indexés (également appelés éléments non indexés) sont des éléments de boîte aux lettres Exchange et des documents sur les sites SharePoint et OneDrive qui n’ont pas été complètement indexés pour la recherche de contenu. Dans cet article, vous pouvez découvrir pourquoi les éléments ne peuvent pas être indexés pour la recherche et sont renvoyés en tant qu’éléments partiellement indexés, identifier les erreurs de recherche pour les éléments partiellement indexés et utiliser un script PowerShell pour déterminer l’exposition de votre organisation à des éléments de courrier électronique partiellement indexés.
ms.openlocfilehash: 64b052e5c04019d5937c3763094529ae5c4c9e42
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43637462"
---
# <a name="investigating-partially-indexed-items-in-ediscovery"></a><span data-ttu-id="b5c1e-104">Étude des éléments partiellement indexés dans eDiscovery</span><span class="sxs-lookup"><span data-stu-id="b5c1e-104">Investigating partially indexed items in eDiscovery</span></span>

<span data-ttu-id="b5c1e-105">Une recherche de contenu exécutée à partir du centre de sécurité & conformité inclut automatiquement les éléments partiellement indexés dans les résultats de recherche estimés lors de l’exécution d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-105">A Content Search that you run from the Security & Compliance Center automatically includes partially indexed items in the estimated search results when you run a search.</span></span> <span data-ttu-id="b5c1e-106">Les éléments partiellement indexés sont des éléments de boîte aux lettres Exchange et des documents sur SharePoint et des sites OneDrive entreprise qui n’ont pas été complètement indexés pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-106">Partially indexed items are Exchange mailbox items and documents on SharePoint and OneDrive for Business sites that for some reason weren't completely indexed for search.</span></span> <span data-ttu-id="b5c1e-107">La plupart des messages électroniques et des documents de site sont indexés, car ils sont inclus dans les [limites d’indexation pour les messages électroniques](limits-for-content-search.md#indexing-limits-for-email-messages).</span><span class="sxs-lookup"><span data-stu-id="b5c1e-107">Most email messages and site documents are successfully indexed because they fall within the [Indexing limits for email messages](limits-for-content-search.md#indexing-limits-for-email-messages).</span></span> <span data-ttu-id="b5c1e-108">Toutefois, certains éléments peuvent dépasser ces limites d’indexation et seront partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-108">However, some items may exceed these indexing limits, and will be partially indexed.</span></span> <span data-ttu-id="b5c1e-109">Voici d’autres raisons pour lesquelles les éléments ne peuvent pas être indexés pour la recherche et sont renvoyés en tant qu’éléments partiellement indexés lors de l’exécution d’une recherche de contenu :</span><span class="sxs-lookup"><span data-stu-id="b5c1e-109">Here are other reasons why items can't be indexed for search and are returned as partially indexed items when you run a Content Search:</span></span>
  
- <span data-ttu-id="b5c1e-110">Les messages électroniques contiennent un fichier joint d’un type de fichier qui ne peut pas être indexé ; dans la plupart des cas, le type de fichier n’est [pas reconnu ou n’est pas pris en charge pour l’indexation](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search) .</span><span class="sxs-lookup"><span data-stu-id="b5c1e-110">Email messages have an attached file of a file type that can't be indexed; in most cases, the file type is [unrecognized or unsupported for indexing](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search)</span></span>
    
- <span data-ttu-id="b5c1e-111">Les messages électroniques comportent un fichier joint sans gestionnaire valide, tel que des fichiers image ; Il s’agit de la cause la plus fréquente d’éléments de courrier électronique partiellement indexés</span><span class="sxs-lookup"><span data-stu-id="b5c1e-111">Email messages have an attached file without a valid handler, such as image files; this is the most common cause of partially indexed email items</span></span>
    
- <span data-ttu-id="b5c1e-112">Trop de fichiers joints à un message électronique</span><span class="sxs-lookup"><span data-stu-id="b5c1e-112">Too many files attached to an email message</span></span>
    
- <span data-ttu-id="b5c1e-113">Un fichier joint à un message électronique est trop volumineux</span><span class="sxs-lookup"><span data-stu-id="b5c1e-113">A file attached to an email message is too large</span></span>
    
- <span data-ttu-id="b5c1e-114">Le type de fichier est pris en charge pour l’indexation, mais une erreur d’indexation s’est produite pour un fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-114">The file type is supported for indexing but an indexing error occurred for a specific file</span></span>
    
<span data-ttu-id="b5c1e-115">Bien que cela varie, les clients de la plupart des organisations disposent de moins de 1% de contenu par volume et de moins de 12% de contenu par taille partiellement indexée.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-115">Although it varies, most organizations customers have less than 1% of content by volume and less than 12% of content by size that is partially indexed.</span></span> <span data-ttu-id="b5c1e-116">La raison de la différence entre le volume et la taille est que les fichiers volumineux ont une probabilité plus élevée de contenir du contenu qui ne peut pas être complètement indexé.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-116">The reason for the difference between the volume versus size is that larger files have a higher probability of containing content that can't be completely indexed.</span></span>
  
## <a name="why-does-the-partially-indexed-item-count-change-for-a-search"></a><span data-ttu-id="b5c1e-117">Pourquoi le nombre d’éléments partiellement indexés change pour une recherche ?</span><span class="sxs-lookup"><span data-stu-id="b5c1e-117">Why does the partially indexed item count change for a search?</span></span>

<span data-ttu-id="b5c1e-118">Une fois que vous avez exécuté une recherche de contenu dans le centre de sécurité & conformité, le nombre total et la taille des éléments partiellement indexés des emplacements de recherche sont répertoriés dans les statistiques des résultats de la recherche qui s’affichent dans les statistiques détaillées de la recherche.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-118">After you run a Content Search in the Security & Compliance Center, the total number and size of partially indexed items in the locations that were searched are listed in the search result statistics that are displayed in the detailed statistics for the search.</span></span> <span data-ttu-id="b5c1e-119">Remarque ces éléments sont appelés *éléments non indexés* dans les statistiques de la recherche.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-119">Note these are called  *unindexed items*  in the search statistics.</span></span> <span data-ttu-id="b5c1e-120">Voici quelques éléments qui affecteront le nombre d’éléments partiellement indexés renvoyés dans les résultats de la recherche :</span><span class="sxs-lookup"><span data-stu-id="b5c1e-120">Here are a few things that will affect the number of partially indexed items that are returned in the search results:</span></span> 
  
- <span data-ttu-id="b5c1e-121">Si un élément est partiellement indexé et correspond à la requête de recherche, il est inclus dans le nombre (et la taille) des éléments de résultat de recherche et des éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-121">If an item is partially indexed and matches the search query, it's included in both the count (and size) of search result items and partially indexed items.</span></span> <span data-ttu-id="b5c1e-122">Toutefois, lorsque les résultats de cette même recherche sont exportés, l’élément est inclus uniquement avec le jeu de résultats de recherche ; elle n’est pas incluse en tant qu’élément partiellement indexé.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-122">However, when the results of that same search are exported, the item is included only with set of search results; it's not included as a partially indexed item.</span></span>
    
- <span data-ttu-id="b5c1e-123">Si vous spécifiez une plage de dates pour une requête de recherche (en l’incluant dans la requête de mot clé ou à l’aide d’une condition), tout élément partiellement indexé ne correspondant pas à la plage de dates n’est pas inclus dans le nombre d’éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-123">If you specify a date range for a search query (by including it in the keyword query or by using a condition), any partially indexed item that doesn't match the date range isn't included in the count of partially indexed items.</span></span> <span data-ttu-id="b5c1e-124">Seuls les éléments partiellement indexés qui appartiennent à la plage de dates sont inclus dans le nombre d’éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-124">Only the partially indexed items that fall within date range are included in the count of partially indexed items.</span></span>
    
 <span data-ttu-id="b5c1e-125">**Remarque :** Les éléments partiellement indexés situés dans les sites SharePoint et OneDrive ne *sont pas* inclus dans l’estimation des éléments partiellement indexés affichés dans les statistiques détaillées de la recherche.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-125">**Note:** Partially indexed items located in SharePoint and OneDrive sites  *are not*  included in the estimate of partially indexed items that's displayed in the detailed statistics for the search.</span></span> <span data-ttu-id="b5c1e-126">Toutefois, les éléments partiellement indexés peuvent être exportés lorsque vous exportez les résultats d’une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-126">However, partially indexed items can be exported when you export the results of a Content Search.</span></span> <span data-ttu-id="b5c1e-127">Par exemple, si vous recherchez uniquement des sites dans une recherche de contenu, le nombre estimé des éléments partiellement indexés est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-127">For example, if you only search sites in a Content Search, the estimated number partially indexed items will be zero.</span></span> 
  
## <a name="calculating-the-ratio-of-partially-indexed-items-in-your-organization"></a><span data-ttu-id="b5c1e-128">Calcul du ratio d’éléments partiellement indexés dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="b5c1e-128">Calculating the ratio of partially indexed items in your organization</span></span>

<span data-ttu-id="b5c1e-129">Pour comprendre l’exposition de votre organisation à des éléments partiellement indexés, vous pouvez effectuer une recherche sur tout le contenu de toutes les boîtes aux lettres (à l’aide d’une requête de mot-clé vide).</span><span class="sxs-lookup"><span data-stu-id="b5c1e-129">To understand your organization's exposure to partially indexed items, you can run a search for all content in all mailboxes (by using a blank keyword query).</span></span> <span data-ttu-id="b5c1e-130">Dans l’exemple ci-dessous, il y a 56 208 (4 830 Mo) d’éléments entièrement indexés et 470 (316 Mo) partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-130">In the following example below, there are 56,208 (4,830 MB) fully indexed items and 470 (316 MB) partially indexed items.</span></span>
  
![Exemple de statistiques de recherche affichant des éléments partiellement indexés](../media/0f6a5cf7-4c98-44a0-a0dd-5aed67124641.png)
  
<span data-ttu-id="b5c1e-132">Vous pouvez déterminer le pourcentage d’éléments partiellement indexés à l’aide des calculs suivants.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-132">You can determine the percentage of partially indexed items by using the following calculations.</span></span>
  
 <span data-ttu-id="b5c1e-133">**Pour calculer le ratio d’éléments partiellement indexés dans votre organisation, procédez comme suit :**</span><span class="sxs-lookup"><span data-stu-id="b5c1e-133">**To calculate the ratio of partially indexed items in your organization:**</span></span>

`(Total number of partially indexed items/Total number of items) x 100`


`(470/56,208) x 100 = 0.84%`
 
<span data-ttu-id="b5c1e-134">À l’aide des résultats de recherche de l’exemple précédent,. 84% de tous les éléments de boîte aux lettres sont partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-134">By using the search results from the previous example, .84% of all mailboxes items are partially indexed.</span></span>
  
 <span data-ttu-id="b5c1e-135">**Pour calculer le pourcentage de la taille des éléments partiellement indexés de votre organisation :**</span><span class="sxs-lookup"><span data-stu-id="b5c1e-135">**To calculate the percentage of the size of partially indexed items in your organization:**</span></span>

`(Size of all partially indexed items/Size of all items) x 100`

`(316 MB/4830 MB) x 100 = 6.54%`

<span data-ttu-id="b5c1e-136">Par conséquent, dans l’exemple précédent, 6,54% de la taille totale des éléments de boîte aux lettres proviennent d’éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-136">So in the previous example, 6.54% of the total size of mailbox items are from partially indexed items.</span></span> <span data-ttu-id="b5c1e-137">Comme indiqué précédemment, la plupart des entreprises clientes disposent de moins de 1% du contenu par volume et de moins de 12% de contenu par taille partiellement indexée.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-137">As previously stated, most organizations customers have less than 1% of content by volume and less than 12% of content by size that is partially indexed.</span></span>

## <a name="working-with-partially-indexed-items"></a><span data-ttu-id="b5c1e-138">Utilisation d’éléments partiellement indexés</span><span class="sxs-lookup"><span data-stu-id="b5c1e-138">Working with partially indexed items</span></span>

<span data-ttu-id="b5c1e-139">Dans les cas où vous devez examiner partiellement des éléments pour vérifier qu’ils ne contiennent pas d’informations pertinentes, vous pouvez [exporter un rapport de recherche de contenu](export-a-content-search-report.md) qui contient des informations sur les éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-139">In cases when you need to examine partially items to validate that they don't contain relevant information, you can [export a content search report](export-a-content-search-report.md) that contains information about partially indexed items.</span></span> <span data-ttu-id="b5c1e-140">Lorsque vous exportez un rapport de recherche de contenu, veillez à choisir l’une des options d’exportation qui incluent des éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-140">When you export a content search report, be sure to choose one of the export options that includes partially indexed items.</span></span> 
  
![Choisir la deuxième ou troisième option pour exporter des éléments partiellement indexés](../media/624a62b4-78f7-4329-ab5d-e62e3b369885.png)
  
<span data-ttu-id="b5c1e-142">Lorsque vous exportez des résultats de recherche de contenu ou un rapport de recherche de contenu à l’aide de l’une de ces options, l’exportation inclut un rapport nommé éléments non indexés. csv.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-142">When you export content search results or a content search report using one of these options, the export includes a report named Unindexed Items.csv.</span></span> <span data-ttu-id="b5c1e-143">Ce rapport inclut la plupart des mêmes informations que le fichier ResultsLog. csv ; Toutefois, le fichier éléments non indexés. csv inclut également deux champs liés à des éléments partiellement indexés : les **balises d’erreur** et les **propriétés d’erreur**.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-143">This report includes most of the same information as the ResultsLog.csv file; however, the Unindexed Items.csv file also includes two fields related to partially indexed items: **Error Tags** and **Error Properties**.</span></span> <span data-ttu-id="b5c1e-144">Ces champs contiennent des informations sur l’erreur d’indexation pour chaque élément partiellement indexé.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-144">These fields contain information about the indexing error for each partially indexed item.</span></span> <span data-ttu-id="b5c1e-145">L’utilisation des informations de ces deux champs peut vous aider à déterminer si l’erreur d’indexation pour un impact particulier a une incidence sur votre enquête.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-145">Using the information in these two fields can help you determine whether or not the indexing error for a particular impacts your investigation.</span></span> <span data-ttu-id="b5c1e-146">Si c’est le cas, vous pouvez effectuer une recherche de contenu ciblé et extraire et exporter des messages électroniques spécifiques et des documents SharePoint ou OneDrive pour les examiner afin de déterminer s’ils sont pertinents pour votre enquête.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-146">If it does, you can perform a targeted content search and retrieve and export specific email messages and SharePoint or OneDrive documents so that you can examine them to determine if they're relevant to your investigation.</span></span> <span data-ttu-id="b5c1e-147">Pour obtenir des instructions pas à pas, voir [Prepare a CSV file for a targeted content Search in Office 365](csv-file-for-an-id-list-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="b5c1e-147">For step-by-step instructions, see [Prepare a CSV file for a targeted Content Search in Office 365](csv-file-for-an-id-list-content-search.md).</span></span>
  
 <span data-ttu-id="b5c1e-148">**Remarque :** Le fichier éléments non indexés. csv contient également des champs nommés **type d’erreur** et message d' **erreur**.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-148">**Note:** The Unindexed Items.csv file also contains fields named **Error Type** and **Error Message**.</span></span> <span data-ttu-id="b5c1e-149">Il s’agit de champs hérités qui contiennent des informations similaires aux informations des champs **balises d’erreur** et **propriétés d’erreur** , mais avec des informations moins détaillées.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-149">These are legacy fields that contain information that is similar to the information in the **Error Tags** and **Error Properties** fields, but with less detailed information.</span></span> <span data-ttu-id="b5c1e-150">Vous pouvez ignorer ces champs hérités en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-150">You can safely ignore these legacy fields.</span></span> 
  
## <a name="errors-related-to-partially-indexed-items"></a><span data-ttu-id="b5c1e-151">Erreurs liées à des éléments partiellement indexés</span><span class="sxs-lookup"><span data-stu-id="b5c1e-151">Errors related to partially indexed items</span></span>

<span data-ttu-id="b5c1e-152">Les balises d’erreur sont constituées de deux informations, l’erreur et le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-152">Error tags are made up of two pieces of information, the error and the file type.</span></span> <span data-ttu-id="b5c1e-153">Par exemple, dans cette paire erreur/type de message :</span><span class="sxs-lookup"><span data-stu-id="b5c1e-153">For example, in this error/filetype pair:</span></span>

```text
 parseroutputsize_xls
```

   
 <span data-ttu-id="b5c1e-154">`parseroutputsize`est l’erreur et `xls` est le type de fichier du fichier dans lequel l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-154">`parseroutputsize` is the error and  `xls` is the file type of the file the error occurred on.</span></span> <span data-ttu-id="b5c1e-155">Dans les cas où le type de fichier n’a pas été reconnu ou que le type de fichier n’est pas applicable à `noformat` l’erreur, vous verrez la valeur à la place du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-155">In cases were the file type wasn't recognized or the file type was doesn't apply to the error, you will see the value  `noformat` in place of the file type.</span></span> 
  
<span data-ttu-id="b5c1e-156">Voici une liste des erreurs d’indexation et une description de la cause possible de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-156">The following is a list of indexing errors and a description of the possible cause of the error.</span></span>
  
|<span data-ttu-id="b5c1e-157">**Balise Error**</span><span class="sxs-lookup"><span data-stu-id="b5c1e-157">**Error tag**</span></span>|<span data-ttu-id="b5c1e-158">**Description**</span><span class="sxs-lookup"><span data-stu-id="b5c1e-158">**Description**</span></span>|
|:-----|:-----|
| `attachmentcount` <br/> |<span data-ttu-id="b5c1e-159">Un message électronique contient trop de pièces jointes et certaines de ces pièces jointes n’ont pas été traitées.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-159">An email message had too many attachments, and some of these attachments weren't processed.</span></span>  <br/> |
| `attachmentdepth` <br/> |<span data-ttu-id="b5c1e-160">Le plan de recherche de contenu et l’analyseur de documents ont trouvé trop de niveaux de pièces jointes imbriqués dans d’autres pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-160">The content retriever and document parser found too many levels of attachments nested inside other attachments.</span></span> <span data-ttu-id="b5c1e-161">Certaines de ces pièces jointes n’ont pas été traitées.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-161">Some of these attachments were not processed.</span></span>  <br/> |
| `attachmentrms` <br/> |<span data-ttu-id="b5c1e-162">Le décodage d’une pièce jointe a échoué car elle était protégée par RMS.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-162">An attachment failed decoding because it was RMS-protected.</span></span>  <br/> |
| `attachmentsize` <br/> |<span data-ttu-id="b5c1e-163">Un fichier joint à un message électronique est trop volumineux et n’a pas pu être traité.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-163">A file attached to an email message was too large and couldn't be processed.</span></span>  <br/> |
| `indexingtruncated` <br/> |<span data-ttu-id="b5c1e-164">Lors de l’écriture du message électronique traité dans l’index, l’une des propriétés indexable était trop volumineuse et a été tronquée.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-164">When writing the processed email message to the index, one of the indexable properties was too large and was truncated.</span></span> <span data-ttu-id="b5c1e-165">Les propriétés tronquées sont répertoriées dans le champ propriétés de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-165">The truncated properties are listed in Error Properties field.</span></span>  <br/> |
| `invalidunicode` <br/> |<span data-ttu-id="b5c1e-166">Un message électronique contient du texte qui n’a pas pu être traité en tant que format Unicode valide.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-166">An email message contained text that couldn't be processed as valid Unicode.</span></span> <span data-ttu-id="b5c1e-167">L’indexation de cet élément est peut-être incomplète.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-167">Indexing for this item may be incomplete.</span></span>  <br/> |
| `parserencrypted` <br/> |<span data-ttu-id="b5c1e-168">Le contenu de la pièce jointe ou du message électronique est chiffré et Microsoft 365 n’a pas pu décoder le contenu.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-168">The content of attachment or email message is encrypted, and Microsoft 365 couldn't decode the content.</span></span>  <br/> |
| `parsererror` <br/> |<span data-ttu-id="b5c1e-169">Une erreur inconnue s’est produite lors de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-169">An unknown error occurred during parsing.</span></span> <span data-ttu-id="b5c1e-170">Cela résulte généralement d’un problème logiciel ou d’un blocage de service.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-170">This typically results from a software bug or a service crash.</span></span>  <br/> |
| `parserinputsize` <br/> |<span data-ttu-id="b5c1e-171">Une pièce jointe était trop volumineuse pour être gérée par l’analyseur, et l’analyse de cette pièce jointe n’a pas été effectuée ou n’a pas été terminée.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-171">An attachment was too large for the parser to handle, and the parsing of that attachment didn't happen or wasn't completed.</span></span>  <br/> |
| `parsermalformed` <br/> |<span data-ttu-id="b5c1e-172">Une pièce jointe est mal formée et n’a pas pu être gérée par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-172">An attachment was malformed and couldn't be handled by the parser.</span></span> <span data-ttu-id="b5c1e-173">Ce résultat peut provenir d’anciens formats de fichiers, de fichiers créés par des logiciels incompatibles ou de virus prétendant être autres que réclamés.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-173">This result from can old file formats, files created by incompatible software, or viruses pretending to be something other than claimed.</span></span>  <br/> |
| `parseroutputsize` <br/> |<span data-ttu-id="b5c1e-174">La sortie de l’analyse d’une pièce jointe était trop volumineuse et devait être tronquée.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-174">The output from the parsing of an attachment was too large and had to be truncated.</span></span>  <br/> |
| `parserunknowntype` <br/> |<span data-ttu-id="b5c1e-175">Une pièce jointe a un type de fichier que Microsoft 365 n’a pas pu détecter.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-175">An attachment had a file type that Microsoft 365 couldn't detect.</span></span>  <br/> |
| `parserunsupportedtype` <br/> |<span data-ttu-id="b5c1e-176">Une pièce jointe a un type de fichier détecté par Office 365could, mais l’analyse de ce type de fichier n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-176">An attachment had a file type that Office 365could detect, but parsing that file type isn't supported.</span></span>  <br/> |
| `propertytoobig` <br/> |<span data-ttu-id="b5c1e-177">La valeur d’une propriété de messagerie dans la Banque d’Exchange est trop grande pour être récupérée et le message n’a pas pu être traité.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-177">The value of an email property in Exchange Store was too large to be retrieved and the message couldn't be processed.</span></span> <span data-ttu-id="b5c1e-178">Cela ne se produit généralement que pour la propriété Body d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-178">This typically only happens to the body property of an email message.</span></span>  <br/> |
| `retrieverrms` <br/> |<span data-ttu-id="b5c1e-179">Le extracteur de contenu n’a pas pu décoder un message protégé par RMS.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-179">The content retriever failed to decode an RMS-protected message.</span></span>  <br/> |
| `wordbreakertruncated` <br/> |<span data-ttu-id="b5c1e-180">Trop de mots ont été identifiés dans le document lors de l’indexation.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-180">Too many words were identified in the document during indexing.</span></span> <span data-ttu-id="b5c1e-181">Le traitement de la propriété s’est arrêté lorsque la limite est atteinte, et la propriété est tronquée.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-181">Processing of the property stopped when reaching the limit, and the property is truncated.</span></span>  <br/> |
   
<span data-ttu-id="b5c1e-182">Les champs d’erreur décrivent les champs qui sont affectés par l’erreur de traitement répertoriée dans le champ balises d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-182">Error fields describe which fields are affected by the processing error listed in the Error Tags field.</span></span> <span data-ttu-id="b5c1e-183">Si vous recherchez une propriété telle que `subject` ou `participants`, les erreurs contenues dans le corps du message n’ont pas d’impact sur les résultats de votre recherche.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-183">If you're searching a property such as  `subject` or  `participants`, errors in the body of the message won't impact the results of your search.</span></span> <span data-ttu-id="b5c1e-184">Cela peut être utile lorsque vous déterminez exactement quels éléments partiellement indexés vous pouvez être amené à approfondir votre enquête.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-184">This can be useful when determining exactly which partially indexed items you might need to further investigate.</span></span>
  
## <a name="using-a-powershell-script-to-determine-your-organizations-exposure-to-partially-indexed-email-items"></a><span data-ttu-id="b5c1e-185">Utilisation d’un script PowerShell pour déterminer l’exposition de votre organisation à des éléments de courrier électronique partiellement indexés</span><span class="sxs-lookup"><span data-stu-id="b5c1e-185">Using a PowerShell script to determine your organization's exposure to partially indexed email items</span></span>

<span data-ttu-id="b5c1e-186">Les étapes suivantes montrent comment exécuter un script PowerShell qui recherche tous les éléments dans toutes les boîtes aux lettres Exchange, puis génère un rapport sur le ratio d’éléments de messagerie partiellement indexés de votre organisation (par nombre et taille) et affiche le nombre d’éléments (et leur type de fichier) pour chaque erreur d’indexation qui se produit.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-186">The following steps show you how to run a PowerShell script that searches for all items in all Exchange mailboxes, and then generates a report about your organization's ratio of partially indexed email items (by count and by size) and displays the number of items (and their file type) for each indexing error that occurs.</span></span> <span data-ttu-id="b5c1e-187">Utilisez les descriptions de balise Error de la section précédente pour identifier l’erreur d’indexation.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-187">Use the error tag descriptions in the previous section to identify the indexing error.</span></span>
  
1. <span data-ttu-id="b5c1e-188">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier. ps1 ; par exemple, `PartiallyIndexedItems.ps1`.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-188">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `PartiallyIndexedItems.ps1`.</span></span>

```powershell
  write-host "**************************************************"
  write-host "     Security & Compliance Center      " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "   eDiscovery Partially Indexed Item Statistics   " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "**************************************************"
  " " 
  # Create a search with Error Tags Refinders enabled
  Remove-ComplianceSearch "RefinerTest" -Confirm:$false -ErrorAction 'SilentlyContinue'
  New-ComplianceSearch -Name "RefinerTest" -ContentMatchQuery "size>0" -RefinerNames ErrorTags -ExchangeLocation ALL
  Start-ComplianceSearch "RefinerTest"
  # Loop while search is in progress
  do{
      Write-host "Waiting for search to complete..."
      Start-Sleep -s 5
      $complianceSearch = Get-ComplianceSearch "RefinerTest"
  }while ($complianceSearch.Status -ne 'Completed')
  $refiners = $complianceSearch.Refiners | ConvertFrom-Json
  $errorTagProperties = $refiners.Entries | Get-Member -MemberType NoteProperty
  $partiallyIndexedRatio = $complianceSearch.UnindexedItems / $complianceSearch.Items
  $partiallyIndexedSizeRatio = $complianceSearch.UnindexedSize / $complianceSearch.Size
  " "
  "===== Partially indexed items ====="
  "         Total          Ratio"
  "Count    {0:N0}{1:P2}" -f $complianceSearch.Items.ToString("N0").PadRight(15, " "), $partiallyIndexedRatio
  "Size(GB) {0:N2}{1:P2}" -f ($complianceSearch.Size / 1GB).ToString("N2").PadRight(15, " "), $partiallyIndexedSizeRatio
  " "
  Write-Host ===== Reasons for partially indexed items =====
  foreach($errorTagProperty in $errorTagProperties)
  {
      $name = $refiners.Entries.($errorTagProperty.Name).Name
      $count = $refiners.Entries.($errorTagProperty.Name).TotalCount
      $frag = $name.Split("{_}")
      $errorTag = $frag[0]
      $fileType = $frag[1]
      if ($errorTag -ne $lastErrorTag)
      {
          $errorTag
      }
      "    " + $fileType + " => " + $count
      $lastErrorTag = $errorTag
  }
  
```

2. <span data-ttu-id="b5c1e-189">[Se connecter à l’interface PowerShell du Centre de sécurité et conformité](https://go.microsoft.com/fwlink/p/?linkid=627084).</span><span class="sxs-lookup"><span data-stu-id="b5c1e-189">[Connect to Security & Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627084).</span></span>
    
3. <span data-ttu-id="b5c1e-190">Dans la sécurité & Centre de conformité PowerShell, accédez au dossier dans lequel vous avez enregistré le script à l’étape 1, puis exécutez le script. par exemple :</span><span class="sxs-lookup"><span data-stu-id="b5c1e-190">In Security & Compliance Center PowerShell, go to the folder where you saved the script in step 1, and then run the script; for example:</span></span>

    ```powershell
    .\PartiallyIndexedItems.ps1
    ```

<span data-ttu-id="b5c1e-191">Voici un exemple de la sortie renvoyée par le script.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-191">Here's an example fo the output returned by the script.</span></span>
  
![Exemple de sortie d’un script qui génère un rapport sur l’exposition de votre organisation à des éléments de courrier électronique partiellement indexés](../media/aeab5943-c15d-431a-bdb2-82f135abc2f3.png)
  
<span data-ttu-id="b5c1e-193">Notez également les points suivants :</span><span class="sxs-lookup"><span data-stu-id="b5c1e-193">Note the following:</span></span>
  
1. <span data-ttu-id="b5c1e-194">Le nombre total et la taille des éléments de courrier électronique, et le ratio de votre organisation pour les éléments de courrier électronique partiellement indexés (par nombre et par taille)</span><span class="sxs-lookup"><span data-stu-id="b5c1e-194">The total number and size of email items, and your organization's ratio of partially indexed email items (by count and by size)</span></span>
    
2. <span data-ttu-id="b5c1e-195">Balises d’erreur de liste et types de fichiers correspondants pour lesquels l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-195">A list error tags and the corresponding file types for which the error occurred.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b5c1e-196">Voir également</span><span class="sxs-lookup"><span data-stu-id="b5c1e-196">See also</span></span>

[<span data-ttu-id="b5c1e-197">Éléments partiellement indexés dans la recherche de contenu dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b5c1e-197">Partially indexed items in Content Search in Office 365</span></span>](partially-indexed-items-in-content-search.md)
