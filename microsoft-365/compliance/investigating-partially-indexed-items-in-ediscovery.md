---
title: Étude des éléments partiellement indexés dans eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/26/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 4e8ff113-6361-41e2-915a-6338a7e2a1ed
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment gérer des éléments partiellement indexés (ou non indexés) à partir d’Exchange, SharePoint et OneDrive entreprise au sein de votre organisation.
ms.openlocfilehash: bbf234e2051cd103d1b99ab75b8e5c15365762a9
ms.sourcegitcommit: d7975c391e03eeb96e29c1d02e77d2a1433ea67c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/05/2020
ms.locfileid: "48919996"
---
# <a name="investigating-partially-indexed-items-in-ediscovery"></a><span data-ttu-id="431d0-103">Étude des éléments partiellement indexés dans eDiscovery</span><span class="sxs-lookup"><span data-stu-id="431d0-103">Investigating partially indexed items in eDiscovery</span></span>

<span data-ttu-id="431d0-104">Une recherche de découverte électronique exécutée à partir du centre de conformité Microsoft 365 inclut automatiquement les éléments partiellement indexés dans les résultats de recherche estimés lors de l’exécution d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="431d0-104">An eDiscovery search that you run from the Microsoft 365 compliance center automatically includes partially indexed items in the estimated search results when you run a search.</span></span> <span data-ttu-id="431d0-105">Les éléments partiellement indexés sont des éléments de boîte aux lettres Exchange et des documents sur SharePoint et des sites OneDrive entreprise qui n’ont pas été complètement indexés pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="431d0-105">Partially indexed items are Exchange mailbox items and documents on SharePoint and OneDrive for Business sites that for some reason weren't completely indexed for search.</span></span> <span data-ttu-id="431d0-106">La plupart des messages électroniques et des documents de site sont indexés, car ils sont inclus dans les [limites d’indexation pour les messages électroniques](limits-for-content-search.md#indexing-limits-for-email-messages).</span><span class="sxs-lookup"><span data-stu-id="431d0-106">Most email messages and site documents are successfully indexed because they fall within the [Indexing limits for email messages](limits-for-content-search.md#indexing-limits-for-email-messages).</span></span> <span data-ttu-id="431d0-107">Toutefois, certains éléments peuvent dépasser ces limites d’indexation et seront partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="431d0-107">However, some items may exceed these indexing limits, and will be partially indexed.</span></span> <span data-ttu-id="431d0-108">Voici d’autres raisons pour lesquelles les éléments ne peuvent pas être indexés pour la recherche et sont renvoyés en tant qu’éléments partiellement indexés lors de l’exécution d’une recherche de découverte électronique :</span><span class="sxs-lookup"><span data-stu-id="431d0-108">Here are other reasons why items can't be indexed for search and are returned as partially indexed items when you run an eDiscovery search:</span></span>
  
- <span data-ttu-id="431d0-109">Les messages électroniques comportent un fichier joint sans gestionnaire valide, tel que des fichiers image ; Il s’agit de la cause la plus fréquente d’éléments de courrier électronique partiellement indexés</span><span class="sxs-lookup"><span data-stu-id="431d0-109">Email messages have an attached file without a valid handler, such as image files; this is the most common cause of partially indexed email items</span></span>

- <span data-ttu-id="431d0-110">Trop de fichiers joints à un message électronique</span><span class="sxs-lookup"><span data-stu-id="431d0-110">Too many files attached to an email message</span></span>

- <span data-ttu-id="431d0-111">Un fichier joint à un message électronique est trop volumineux</span><span class="sxs-lookup"><span data-stu-id="431d0-111">A file attached to an email message is too large</span></span>

- <span data-ttu-id="431d0-112">Le type de fichier est pris en charge pour l’indexation, mais une erreur d’indexation s’est produite pour un fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="431d0-112">The file type is supported for indexing but an indexing error occurred for a specific file</span></span>

<span data-ttu-id="431d0-113">Bien que cela varie, les clients de la plupart des organisations disposent de moins de 1% de contenu par volume et de moins de 12% de contenu par taille partiellement indexée.</span><span class="sxs-lookup"><span data-stu-id="431d0-113">Although it varies, most organizations customers have less than 1% of content by volume and less than 12% of content by size that is partially indexed.</span></span> <span data-ttu-id="431d0-114">La raison de la différence entre le volume et la taille est que les fichiers volumineux ont une probabilité plus élevée de contenir du contenu qui ne peut pas être complètement indexé.</span><span class="sxs-lookup"><span data-stu-id="431d0-114">The reason for the difference between the volume versus size is that larger files have a higher probability of containing content that can't be completely indexed.</span></span>
  
## <a name="why-does-the-partially-indexed-item-count-change-for-a-search"></a><span data-ttu-id="431d0-115">Pourquoi le nombre d’éléments partiellement indexés change pour une recherche ?</span><span class="sxs-lookup"><span data-stu-id="431d0-115">Why does the partially indexed item count change for a search?</span></span>

<span data-ttu-id="431d0-116">Une fois que vous avez exécuté une recherche de découverte électronique, le nombre total et la taille des éléments partiellement indexés des emplacements qui ont été recherchés sont répertoriés dans les statistiques de résultats de recherche qui s’affichent dans les statistiques détaillées de la recherche.</span><span class="sxs-lookup"><span data-stu-id="431d0-116">After you run an eDiscovery search, the total number and size of partially indexed items in the locations that were searched are listed in the search result statistics that are displayed in the detailed statistics for the search.</span></span> <span data-ttu-id="431d0-117">Remarque ces éléments sont appelés  *éléments non indexés*  dans les statistiques de la recherche.</span><span class="sxs-lookup"><span data-stu-id="431d0-117">Note these are called  *unindexed items*  in the search statistics.</span></span> <span data-ttu-id="431d0-118">Voici quelques éléments qui affecteront le nombre d’éléments partiellement indexés renvoyés dans les résultats de la recherche :</span><span class="sxs-lookup"><span data-stu-id="431d0-118">Here are a few things that will affect the number of partially indexed items that are returned in the search results:</span></span>
  
- <span data-ttu-id="431d0-119">Si un élément est partiellement indexé et correspond à la requête de recherche, il est inclus dans le nombre (et la taille) des éléments de résultat de recherche et des éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="431d0-119">If an item is partially indexed and matches the search query, it's included in both the count (and size) of search result items and partially indexed items.</span></span> <span data-ttu-id="431d0-120">Toutefois, lorsque les résultats de cette même recherche sont exportés, l’élément est inclus uniquement avec le jeu de résultats de recherche ; elle n’est pas incluse en tant qu’élément partiellement indexé.</span><span class="sxs-lookup"><span data-stu-id="431d0-120">However, when the results of that same search are exported, the item is included only with set of search results; it's not included as a partially indexed item.</span></span>

- <span data-ttu-id="431d0-121">Si vous spécifiez une plage de dates pour une requête de recherche (en l’incluant dans la requête de mot clé ou à l’aide d’une condition), tout élément partiellement indexé ne correspondant pas à la plage de dates n’est pas inclus dans le nombre d’éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="431d0-121">If you specify a date range for a search query (by including it in the keyword query or by using a condition), any partially indexed item that doesn't match the date range isn't included in the count of partially indexed items.</span></span> <span data-ttu-id="431d0-122">Seuls les éléments partiellement indexés qui appartiennent à la plage de dates sont inclus dans le nombre d’éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="431d0-122">Only the partially indexed items that fall within date range are included in the count of partially indexed items.</span></span>

> [!NOTE]
> <span data-ttu-id="431d0-123">Les éléments partiellement indexés situés dans les sites SharePoint et OneDrive ne *sont pas* inclus dans l’estimation des éléments partiellement indexés affichés dans les statistiques détaillées de la recherche.</span><span class="sxs-lookup"><span data-stu-id="431d0-123">Partially indexed items located in SharePoint and OneDrive sites *are not* included in the estimate of partially indexed items that's displayed in the detailed statistics for the search.</span></span> <span data-ttu-id="431d0-124">Toutefois, les éléments partiellement indexés peuvent être exportés lorsque vous exportez les résultats d’une recherche de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="431d0-124">However, partially indexed items can be exported when you export the results of an eDiscovery search.</span></span> <span data-ttu-id="431d0-125">Par exemple, si vous recherchez uniquement les sites de recherche, le nombre estimé des éléments partiellement indexés est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="431d0-125">For example, if you only search sites, the estimated number partially indexed items will be zero.</span></span>
  
## <a name="calculating-the-ratio-of-partially-indexed-items-in-your-organization"></a><span data-ttu-id="431d0-126">Calcul du ratio d’éléments partiellement indexés dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="431d0-126">Calculating the ratio of partially indexed items in your organization</span></span>

<span data-ttu-id="431d0-127">Pour comprendre l’exposition de votre organisation à des éléments partiellement indexés, vous pouvez effectuer une recherche sur tout le contenu de toutes les boîtes aux lettres (à l’aide d’une requête de mot-clé vide).</span><span class="sxs-lookup"><span data-stu-id="431d0-127">To understand your organization's exposure to partially indexed items, you can run a search for all content in all mailboxes (by using a blank keyword query).</span></span> <span data-ttu-id="431d0-128">Dans l’exemple ci-dessous, il y a 56 208 (4 830 Mo) d’éléments entièrement indexés et 470 (316 Mo) partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="431d0-128">In the following example below, there are 56,208 (4,830 MB) fully indexed items and 470 (316 MB) partially indexed items.</span></span>
  
![Exemple de statistiques de recherche affichant des éléments partiellement indexés](../media/0f6a5cf7-4c98-44a0-a0dd-5aed67124641.png)
  
<span data-ttu-id="431d0-130">Vous pouvez déterminer le pourcentage d’éléments partiellement indexés à l’aide des calculs suivants.</span><span class="sxs-lookup"><span data-stu-id="431d0-130">You can determine the percentage of partially indexed items by using the following calculations.</span></span>
  
 <span data-ttu-id="431d0-131">**Pour calculer le ratio d’éléments partiellement indexés dans votre organisation, procédez comme suit :**</span><span class="sxs-lookup"><span data-stu-id="431d0-131">**To calculate the ratio of partially indexed items in your organization:**</span></span>

`(Total number of partially indexed items/Total number of items) x 100`

`(470/56,208) x 100 = 0.84%`

<span data-ttu-id="431d0-132">À l’aide des résultats de recherche de l’exemple précédent,. 84% de tous les éléments de boîte aux lettres sont partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="431d0-132">By using the search results from the previous example, .84% of all mailboxes items are partially indexed.</span></span>
  
 <span data-ttu-id="431d0-133">**Pour calculer le pourcentage de la taille des éléments partiellement indexés de votre organisation :**</span><span class="sxs-lookup"><span data-stu-id="431d0-133">**To calculate the percentage of the size of partially indexed items in your organization:**</span></span>

`(Size of all partially indexed items/Size of all items) x 100`

`(316 MB/4830 MB) x 100 = 6.54%`

<span data-ttu-id="431d0-134">Par conséquent, dans l’exemple précédent, 6,54% de la taille totale des éléments de boîte aux lettres proviennent d’éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="431d0-134">So in the previous example, 6.54% of the total size of mailbox items are from partially indexed items.</span></span> <span data-ttu-id="431d0-135">Comme indiqué précédemment, la plupart des entreprises clientes disposent de moins de 1% du contenu par volume et de moins de 12% de contenu par taille partiellement indexée.</span><span class="sxs-lookup"><span data-stu-id="431d0-135">As previously stated, most organizations customers have less than 1% of content by volume and less than 12% of content by size that is partially indexed.</span></span>

## <a name="working-with-partially-indexed-items"></a><span data-ttu-id="431d0-136">Utilisation d’éléments partiellement indexés</span><span class="sxs-lookup"><span data-stu-id="431d0-136">Working with partially indexed items</span></span>

<span data-ttu-id="431d0-137">Dans les cas où vous devez examiner partiellement des éléments pour vérifier qu’ils ne contiennent pas d’informations pertinentes, vous pouvez [exporter un rapport de recherche de contenu](export-a-content-search-report.md) qui contient des informations sur les éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="431d0-137">In cases when you need to examine partially items to validate that they don't contain relevant information, you can [export a content search report](export-a-content-search-report.md) that contains information about partially indexed items.</span></span> <span data-ttu-id="431d0-138">Lorsque vous exportez un rapport de recherche de contenu, veillez à choisir l’une des options d’exportation qui incluent des éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="431d0-138">When you export a content search report, be sure to choose one of the export options that includes partially indexed items.</span></span>
  
![Choisir la deuxième ou troisième option pour exporter des éléments partiellement indexés](../media/624a62b4-78f7-4329-ab5d-e62e3b369885.png)
  
<span data-ttu-id="431d0-140">Lorsque vous exportez des résultats de recherche de découverte électronique ou un rapport de recherche à l’aide de l’une de ces options, l’exportation inclut un rapport nommé Items.csv non indexée.</span><span class="sxs-lookup"><span data-stu-id="431d0-140">When you export eDiscovery search results or a search report using one of these options, the export includes a report named Unindexed Items.csv.</span></span> <span data-ttu-id="431d0-141">Ce rapport inclut la plupart des mêmes informations que le fichier ResultsLog.csv ; Toutefois, le fichier Items.csv non indexé inclut également deux champs liés à des éléments partiellement indexés : les **balises d’erreur** et les propriétés de l' **erreur**.</span><span class="sxs-lookup"><span data-stu-id="431d0-141">This report includes most of the same information as the ResultsLog.csv file; however, the Unindexed Items.csv file also includes two fields related to partially indexed items: **Error Tags** and **Error Properties**.</span></span> <span data-ttu-id="431d0-142">Ces champs contiennent des informations sur l’erreur d’indexation pour chaque élément partiellement indexé.</span><span class="sxs-lookup"><span data-stu-id="431d0-142">These fields contain information about the indexing error for each partially indexed item.</span></span> <span data-ttu-id="431d0-143">L’utilisation des informations de ces deux champs peut vous aider à déterminer si l’erreur d’indexation pour un impact particulier a une incidence sur votre enquête.</span><span class="sxs-lookup"><span data-stu-id="431d0-143">Using the information in these two fields can help you determine whether or not the indexing error for a particular impacts your investigation.</span></span> <span data-ttu-id="431d0-144">Si c’est le cas, vous pouvez effectuer une recherche ciblée et récupérer et exporter des messages électroniques spécifiques et des documents SharePoint ou OneDrive pour les examiner afin de déterminer s’ils sont pertinents pour votre enquête.</span><span class="sxs-lookup"><span data-stu-id="431d0-144">If it does, you can perform a targeted search and retrieve and export specific email messages and SharePoint or OneDrive documents so that you can examine them to determine if they're relevant to your investigation.</span></span> <span data-ttu-id="431d0-145">Pour obtenir des instructions pas à pas, consultez la rubrique [préparer un fichier CSV pour une recherche ciblée dans Office 365](csv-file-for-an-id-list-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="431d0-145">For step-by-step instructions, see [Prepare a CSV file for a targeted search in Office 365](csv-file-for-an-id-list-content-search.md).</span></span>

> [!NOTE]
> <span data-ttu-id="431d0-146">Le fichier Items.csv unindex contient également des champs nommés **Error type** et **Error message**.</span><span class="sxs-lookup"><span data-stu-id="431d0-146">The Unindexed Items.csv file also contains fields named **Error Type** and **Error Message**.</span></span> <span data-ttu-id="431d0-147">Il s’agit de champs hérités qui contiennent des informations similaires aux informations des champs **balises d’erreur** et **propriétés d’erreur** , mais avec des informations moins détaillées.</span><span class="sxs-lookup"><span data-stu-id="431d0-147">These are legacy fields that contain information that is similar to the information in the **Error Tags** and **Error Properties** fields, but with less detailed information.</span></span> <span data-ttu-id="431d0-148">Vous pouvez ignorer ces champs hérités en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="431d0-148">You can safely ignore these legacy fields.</span></span>
  
## <a name="errors-related-to-partially-indexed-items"></a><span data-ttu-id="431d0-149">Erreurs liées à des éléments partiellement indexés</span><span class="sxs-lookup"><span data-stu-id="431d0-149">Errors related to partially indexed items</span></span>

<span data-ttu-id="431d0-150">Les balises d’erreur sont constituées de deux informations, l’erreur et le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="431d0-150">Error tags are made up of two pieces of information, the error and the file type.</span></span> <span data-ttu-id="431d0-151">Par exemple, dans cette paire erreur/type de message :</span><span class="sxs-lookup"><span data-stu-id="431d0-151">For example, in this error/filetype pair:</span></span>

```text
 parseroutputsize_xls
```

 <span data-ttu-id="431d0-152">`parseroutputsize` est l’erreur et `xls` est le type de fichier du fichier dans lequel l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="431d0-152">`parseroutputsize` is the error and `xls` is the file type of the file the error occurred on.</span></span> <span data-ttu-id="431d0-153">Dans les cas où le type de fichier n’a pas été reconnu ou que le type de fichier n’a pas pu s’appliquer à l’erreur, vous verrez la valeur `noformat` à la place du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="431d0-153">In cases were the file type wasn't recognized or the file type didn't apply to the error, you will see the value `noformat` in place of the file type.</span></span>
  
<span data-ttu-id="431d0-154">Voici une liste des erreurs d’indexation et une description de la cause possible de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="431d0-154">The following is a list of indexing errors and a description of the possible cause of the error.</span></span>
  
|<span data-ttu-id="431d0-155">**Balise Error**</span><span class="sxs-lookup"><span data-stu-id="431d0-155">**Error tag**</span></span>|<span data-ttu-id="431d0-156">**Description**</span><span class="sxs-lookup"><span data-stu-id="431d0-156">**Description**</span></span>|
|:-----|:-----|
| `attachmentcount` <br/> |<span data-ttu-id="431d0-157">Un message électronique contient trop de pièces jointes et certaines de ces pièces jointes n’ont pas été traitées.</span><span class="sxs-lookup"><span data-stu-id="431d0-157">An email message had too many attachments, and some of these attachments weren't processed.</span></span>  <br/> |
| `attachmentdepth` <br/> |<span data-ttu-id="431d0-158">Le plan de recherche de contenu et l’analyseur de documents ont trouvé trop de niveaux de pièces jointes imbriqués dans d’autres pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="431d0-158">The content retriever and document parser found too many levels of attachments nested inside other attachments.</span></span> <span data-ttu-id="431d0-159">Certaines de ces pièces jointes n’ont pas été traitées.</span><span class="sxs-lookup"><span data-stu-id="431d0-159">Some of these attachments were not processed.</span></span>  <br/> |
| `attachmentrms` <br/> |<span data-ttu-id="431d0-160">Le décodage d’une pièce jointe a échoué car elle était protégée par RMS.</span><span class="sxs-lookup"><span data-stu-id="431d0-160">An attachment failed decoding because it was RMS-protected.</span></span>  <br/> |
| `attachmentsize` <br/> |<span data-ttu-id="431d0-161">Un fichier joint à un message électronique est trop volumineux et n’a pas pu être traité.</span><span class="sxs-lookup"><span data-stu-id="431d0-161">A file attached to an email message was too large and couldn't be processed.</span></span>  <br/> |
| `indexingtruncated` <br/> |<span data-ttu-id="431d0-162">Lors de l’écriture du message électronique traité dans l’index, l’une des propriétés indexable était trop volumineuse et a été tronquée.</span><span class="sxs-lookup"><span data-stu-id="431d0-162">When writing the processed email message to the index, one of the indexable properties was too large and was truncated.</span></span> <span data-ttu-id="431d0-163">Les propriétés tronquées sont répertoriées dans le champ propriétés de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="431d0-163">The truncated properties are listed in Error Properties field.</span></span>  <br/> |
| `invalidunicode` <br/> |<span data-ttu-id="431d0-164">Un message électronique contient du texte qui n’a pas pu être traité en tant que format Unicode valide.</span><span class="sxs-lookup"><span data-stu-id="431d0-164">An email message contained text that couldn't be processed as valid Unicode.</span></span> <span data-ttu-id="431d0-165">L’indexation de cet élément est peut-être incomplète.</span><span class="sxs-lookup"><span data-stu-id="431d0-165">Indexing for this item may be incomplete.</span></span>  <br/> |
| `parserencrypted` <br/> |<span data-ttu-id="431d0-166">Le contenu de la pièce jointe ou du message électronique est chiffré et Microsoft 365 n’a pas pu décoder le contenu.</span><span class="sxs-lookup"><span data-stu-id="431d0-166">The content of attachment or email message is encrypted, and Microsoft 365 couldn't decode the content.</span></span>  <br/> |
| `parsererror` <br/> |<span data-ttu-id="431d0-167">Une erreur inconnue s’est produite lors de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="431d0-167">An unknown error occurred during parsing.</span></span> <span data-ttu-id="431d0-168">Cela résulte généralement d’un problème logiciel ou d’un blocage de service.</span><span class="sxs-lookup"><span data-stu-id="431d0-168">This typically results from a software bug or a service crash.</span></span>  <br/> |
| `parserinputsize` <br/> |<span data-ttu-id="431d0-169">Une pièce jointe était trop volumineuse pour être gérée par l’analyseur, et l’analyse de cette pièce jointe n’a pas été effectuée ou n’a pas été terminée.</span><span class="sxs-lookup"><span data-stu-id="431d0-169">An attachment was too large for the parser to handle, and the parsing of that attachment didn't happen or wasn't completed.</span></span>  <br/> |
| `parsermalformed` <br/> |<span data-ttu-id="431d0-170">Une pièce jointe est mal formée et n’a pas pu être gérée par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="431d0-170">An attachment was malformed and couldn't be handled by the parser.</span></span> <span data-ttu-id="431d0-171">Ce résultat peut provenir d’anciens formats de fichiers, de fichiers créés par des logiciels incompatibles ou de virus prétendant être autres que réclamés.</span><span class="sxs-lookup"><span data-stu-id="431d0-171">This result from can old file formats, files created by incompatible software, or viruses pretending to be something other than claimed.</span></span>  <br/> |
| `parseroutputsize` <br/> |<span data-ttu-id="431d0-172">La sortie de l’analyse d’une pièce jointe était trop volumineuse et devait être tronquée.</span><span class="sxs-lookup"><span data-stu-id="431d0-172">The output from the parsing of an attachment was too large and had to be truncated.</span></span>  <br/> |
| `parserunknowntype` <br/> |<span data-ttu-id="431d0-173">Une pièce jointe a un type de fichier que Microsoft 365 n’a pas pu détecter.</span><span class="sxs-lookup"><span data-stu-id="431d0-173">An attachment had a file type that Microsoft 365 couldn't detect.</span></span>  <br/> |
| `parserunsupportedtype` <br/> |<span data-ttu-id="431d0-174">Une pièce jointe a un type de fichier qu’Office 365 a pu détecter, mais l’analyse de ce type de fichier n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="431d0-174">An attachment had a file type that Office 365 could detect, but parsing that file type isn't supported.</span></span>  <br/> |
| `propertytoobig` <br/> |<span data-ttu-id="431d0-175">La valeur d’une propriété de messagerie dans la Banque d’Exchange est trop grande pour être récupérée et le message n’a pas pu être traité.</span><span class="sxs-lookup"><span data-stu-id="431d0-175">The value of an email property in Exchange Store was too large to be retrieved and the message couldn't be processed.</span></span> <span data-ttu-id="431d0-176">Cela ne se produit généralement que pour la propriété Body d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="431d0-176">This typically only happens to the body property of an email message.</span></span>  <br/> |
| `retrieverrms` <br/> |<span data-ttu-id="431d0-177">Le extracteur de contenu n’a pas pu décoder un message protégé par RMS.</span><span class="sxs-lookup"><span data-stu-id="431d0-177">The content retriever failed to decode an RMS-protected message.</span></span>  <br/> |
| `wordbreakertruncated` <br/> |<span data-ttu-id="431d0-178">Trop de mots ont été identifiés dans le document lors de l’indexation.</span><span class="sxs-lookup"><span data-stu-id="431d0-178">Too many words were identified in the document during indexing.</span></span> <span data-ttu-id="431d0-179">Le traitement de la propriété s’est arrêté lorsque la limite est atteinte, et la propriété est tronquée.</span><span class="sxs-lookup"><span data-stu-id="431d0-179">Processing of the property stopped when reaching the limit, and the property is truncated.</span></span>  <br/> |

<span data-ttu-id="431d0-180">Les champs d’erreur décrivent les champs qui sont affectés par l’erreur de traitement répertoriée dans le champ balises d’erreur.</span><span class="sxs-lookup"><span data-stu-id="431d0-180">Error fields describe which fields are affected by the processing error listed in the Error Tags field.</span></span> <span data-ttu-id="431d0-181">Si vous recherchez une propriété telle que  `subject` ou  `participants` , les erreurs contenues dans le corps du message n’ont pas d’impact sur les résultats de votre recherche.</span><span class="sxs-lookup"><span data-stu-id="431d0-181">If you're searching a property such as  `subject` or  `participants`, errors in the body of the message won't impact the results of your search.</span></span> <span data-ttu-id="431d0-182">Cela peut être utile lorsque vous déterminez exactement quels éléments partiellement indexés vous pouvez être amené à approfondir votre enquête.</span><span class="sxs-lookup"><span data-stu-id="431d0-182">This can be useful when determining exactly which partially indexed items you might need to further investigate.</span></span>
  
## <a name="using-a-powershell-script-to-determine-your-organizations-exposure-to-partially-indexed-email-items"></a><span data-ttu-id="431d0-183">Utilisation d’un script PowerShell pour déterminer l’exposition de votre organisation à des éléments de courrier électronique partiellement indexés</span><span class="sxs-lookup"><span data-stu-id="431d0-183">Using a PowerShell script to determine your organization's exposure to partially indexed email items</span></span>

<span data-ttu-id="431d0-184">Les étapes suivantes montrent comment exécuter un script PowerShell qui recherche tous les éléments dans toutes les boîtes aux lettres Exchange, puis génère un rapport sur le ratio d’éléments de messagerie partiellement indexés de votre organisation (par nombre et taille) et affiche le nombre d’éléments (et leur type de fichier) pour chaque erreur d’indexation qui se produit.</span><span class="sxs-lookup"><span data-stu-id="431d0-184">The following steps show you how to run a PowerShell script that searches for all items in all Exchange mailboxes, and then generates a report about your organization's ratio of partially indexed email items (by count and by size) and displays the number of items (and their file type) for each indexing error that occurs.</span></span> <span data-ttu-id="431d0-185">Utilisez les descriptions de balise Error de la section précédente pour identifier l’erreur d’indexation.</span><span class="sxs-lookup"><span data-stu-id="431d0-185">Use the error tag descriptions in the previous section to identify the indexing error.</span></span>
  
1. <span data-ttu-id="431d0-186">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier. ps1 ; par exemple, `PartiallyIndexedItems.ps1` .</span><span class="sxs-lookup"><span data-stu-id="431d0-186">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `PartiallyIndexedItems.ps1`.</span></span>

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

2. <span data-ttu-id="431d0-187">[Connectez-vous au Centre de conformité et sécurité PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627084).</span><span class="sxs-lookup"><span data-stu-id="431d0-187">[Connect to Security & Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627084).</span></span>

3. <span data-ttu-id="431d0-188">Dans la sécurité & Centre de conformité PowerShell, accédez au dossier dans lequel vous avez enregistré le script à l’étape 1, puis exécutez le script. par exemple :</span><span class="sxs-lookup"><span data-stu-id="431d0-188">In Security & Compliance Center PowerShell, go to the folder where you saved the script in step 1, and then run the script; for example:</span></span>

    ```powershell
    .\PartiallyIndexedItems.ps1
    ```

<span data-ttu-id="431d0-189">Voici un exemple de la sortie renvoyée par le script.</span><span class="sxs-lookup"><span data-stu-id="431d0-189">Here's an example fo the output returned by the script.</span></span>
  
![Exemple de sortie d’un script qui génère un rapport sur l’exposition de votre organisation à des éléments de courrier électronique partiellement indexés](../media/aeab5943-c15d-431a-bdb2-82f135abc2f3.png)
  
<span data-ttu-id="431d0-191">Veuillez prendre en compte les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="431d0-191">Note the following:</span></span>
  
1. <span data-ttu-id="431d0-192">Le nombre total et la taille des éléments de courrier électronique, et le ratio de votre organisation pour les éléments de courrier électronique partiellement indexés (par nombre et par taille)</span><span class="sxs-lookup"><span data-stu-id="431d0-192">The total number and size of email items, and your organization's ratio of partially indexed email items (by count and by size)</span></span>

2. <span data-ttu-id="431d0-193">Balises d’erreur de liste et types de fichiers correspondants pour lesquels l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="431d0-193">A list error tags and the corresponding file types for which the error occurred.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="431d0-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="431d0-194">See also</span></span>

[<span data-ttu-id="431d0-195">Éléments partiellement indexés dans eDiscovery</span><span class="sxs-lookup"><span data-stu-id="431d0-195">Partially indexed items in eDiscovery</span></span>](partially-indexed-items-in-content-search.md)
