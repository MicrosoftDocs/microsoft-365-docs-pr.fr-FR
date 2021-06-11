---
title: Recherche d’éléments partiellement indexés dans eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
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
description: Découvrez comment gérer des éléments partiellement indexés (également appelés éléments non indexés) à partir de Exchange, SharePoint et OneDrive Entreprise au sein de votre organisation.
ms.openlocfilehash: 539fd2687735a5ee14be543750becca8c6c3154c
ms.sourcegitcommit: efb932db63ad3ab4af4b585428d567d069410e4e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2021
ms.locfileid: "52311453"
---
# <a name="investigating-partially-indexed-items-in-ediscovery"></a><span data-ttu-id="359b5-103">Recherche d’éléments partiellement indexés dans eDiscovery</span><span class="sxs-lookup"><span data-stu-id="359b5-103">Investigating partially indexed items in eDiscovery</span></span>

<span data-ttu-id="359b5-104">Une recherche de découverte électronique que vous exécutez à partir du centre de conformité Microsoft 365 inclut automatiquement des éléments partiellement indexés dans les résultats de recherche estimés lorsque vous exécutez une recherche.</span><span class="sxs-lookup"><span data-stu-id="359b5-104">An eDiscovery search that you run from the Microsoft 365 compliance center automatically includes partially indexed items in the estimated search results when you run a search.</span></span> <span data-ttu-id="359b5-105">Les éléments partiellement indexés sont des Exchange de boîtes aux lettres et des documents sur des sites SharePoint et OneDrive Entreprise qui, pour une raison quelconque, n’ont pas été complètement indexés pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="359b5-105">Partially indexed items are Exchange mailbox items and documents on SharePoint and OneDrive for Business sites that for some reason weren't completely indexed for search.</span></span> <span data-ttu-id="359b5-106">La plupart des messages électroniques et des documents de site sont indexés avec succès, car ils se limitent aux [limites d’indexation des messages électroniques.](limits-for-content-search.md#indexing-limits-for-email-messages)</span><span class="sxs-lookup"><span data-stu-id="359b5-106">Most email messages and site documents are successfully indexed because they fall within the [Indexing limits for email messages](limits-for-content-search.md#indexing-limits-for-email-messages).</span></span> <span data-ttu-id="359b5-107">Toutefois, certains éléments peuvent dépasser ces limites d’indexation et seront partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="359b5-107">However, some items may exceed these indexing limits, and will be partially indexed.</span></span> <span data-ttu-id="359b5-108">Voici d’autres raisons pour lesquelles les éléments ne peuvent pas être indexés pour la recherche et sont renvoyés en tant qu’éléments partiellement indexés lorsque vous exécutez une recherche de découverte électronique :</span><span class="sxs-lookup"><span data-stu-id="359b5-108">Here are other reasons why items can't be indexed for search and are returned as partially indexed items when you run an eDiscovery search:</span></span>
  
- <span data-ttu-id="359b5-109">Les messages électroniques ont un fichier joint sans un handler valide, tel que des fichiers image ; Il s’agit de la cause la plus courante des éléments de courrier partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="359b5-109">Email messages have an attached file without a valid handler, such as image files; this is the most common cause of partially indexed email items.</span></span>

- <span data-ttu-id="359b5-110">Le nombre de fichiers joints à un message électronique est trop important.</span><span class="sxs-lookup"><span data-stu-id="359b5-110">Too many files attached to an email message.</span></span>

- <span data-ttu-id="359b5-111">Un fichier joint à un message électronique est trop volumineux.</span><span class="sxs-lookup"><span data-stu-id="359b5-111">A file attached to an email message is too large.</span></span>

- <span data-ttu-id="359b5-112">Le type de fichier est pris en charge pour l'indexation, mais une erreur d'indexation s'est produite pour un fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="359b5-112">The file type is supported for indexing but an indexing error occurred for a specific file.</span></span>

<span data-ttu-id="359b5-113">Bien que cela varie, la plupart des clients d’organisations ont moins de 1 % de contenu par volume et moins de 12 % de contenu par taille partiellement indexée.</span><span class="sxs-lookup"><span data-stu-id="359b5-113">Although it varies, most organizations customers have less than 1% of content by volume and less than 12% of content by size that is partially indexed.</span></span> <span data-ttu-id="359b5-114">La différence entre le volume et la taille est dû au fait que les fichiers plus volumineux ont une probabilité plus élevée de contenir du contenu qui ne peut pas être complètement indexé.</span><span class="sxs-lookup"><span data-stu-id="359b5-114">The reason for the difference between the volume versus size is that larger files have a higher probability of containing content that can't be completely indexed.</span></span>
  
## <a name="why-does-the-partially-indexed-item-count-change-for-a-search"></a><span data-ttu-id="359b5-115">Pourquoi le nombre d’éléments partiellement indexés change-t-il pour une recherche ?</span><span class="sxs-lookup"><span data-stu-id="359b5-115">Why does the partially indexed item count change for a search?</span></span>

<span data-ttu-id="359b5-116">Après avoir exécuté une recherche de découverte électronique, le nombre total et la taille des éléments partiellement indexés dans les emplacements qui ont fait l’objet de la recherche sont répertoriés dans les statistiques des résultats de la recherche qui sont affichées dans les statistiques détaillées de la recherche.</span><span class="sxs-lookup"><span data-stu-id="359b5-116">After you run an eDiscovery search, the total number and size of partially indexed items in the locations that were searched are listed in the search result statistics that are displayed in the detailed statistics for the search.</span></span> <span data-ttu-id="359b5-117">Notez qu’ils sont appelés éléments  *nonndex dans*  les statistiques de recherche.</span><span class="sxs-lookup"><span data-stu-id="359b5-117">Note these are called  *unindexed items*  in the search statistics.</span></span> <span data-ttu-id="359b5-118">Voici quelques éléments qui affectent le nombre d’éléments partiellement indexés renvoyés dans les résultats de la recherche :</span><span class="sxs-lookup"><span data-stu-id="359b5-118">Here are a few things that will affect the number of partially indexed items that are returned in the search results:</span></span>
  
- <span data-ttu-id="359b5-119">Si un élément est partiellement indexé et correspond à la requête de recherche, il est inclus dans le nombre (et la taille) d’éléments de résultat de recherche et dans les éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="359b5-119">If an item is partially indexed and matches the search query, it's included in both the count (and size) of search result items and partially indexed items.</span></span> <span data-ttu-id="359b5-120">Toutefois, lorsque les résultats de cette même recherche sont exportés, l’élément est inclus uniquement avec l’ensemble des résultats de recherche ; il n’est pas inclus en tant qu’élément partiellement indexé.</span><span class="sxs-lookup"><span data-stu-id="359b5-120">However, when the results of that same search are exported, the item is included only with set of search results; it's not included as a partially indexed item.</span></span>

- <span data-ttu-id="359b5-121">Les éléments partiellement indexés situés dans les *sites* SharePoint et OneDrive ne sont pas inclus dans l’estimation des éléments partiellement indexés affichés dans les statistiques détaillées de la recherche.</span><span class="sxs-lookup"><span data-stu-id="359b5-121">Partially indexed items located in SharePoint and OneDrive sites *are not* included in the estimate of partially indexed items that's displayed in the detailed statistics for the search.</span></span> <span data-ttu-id="359b5-122">Toutefois, les éléments partiellement indexés peuvent être exportés lorsque vous exportez les résultats d’une recherche de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="359b5-122">However, partially indexed items can be exported when you export the results of an eDiscovery search.</span></span> <span data-ttu-id="359b5-123">Par exemple, si vous recherchez uniquement des sites, le nombre estimé d’éléments partiellement indexés sera zéro.</span><span class="sxs-lookup"><span data-stu-id="359b5-123">For example, if you only search sites, the estimated number partially indexed items will be zero.</span></span>
  
## <a name="calculating-the-ratio-of-partially-indexed-items-in-your-organization"></a><span data-ttu-id="359b5-124">Calcul du taux d’éléments partiellement indexés dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="359b5-124">Calculating the ratio of partially indexed items in your organization</span></span>

<span data-ttu-id="359b5-125">Pour comprendre l’exposition de votre organisation aux éléments partiellement indexés, vous pouvez exécuter une recherche de tout le contenu dans toutes les boîtes aux lettres (à l’aide d’une requête de mot clé vide).</span><span class="sxs-lookup"><span data-stu-id="359b5-125">To understand your organization's exposure to partially indexed items, you can run a search for all content in all mailboxes (by using a blank keyword query).</span></span> <span data-ttu-id="359b5-126">Dans l’exemple suivant, il y a 1 629 904 (146,46 Go) d’éléments entièrement indexés et 10 025 (10,27 Go) d’éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="359b5-126">In the following example, there are 1,629,904 (146.46 GB) fully indexed items and 10,025 (10.27 GB) partially indexed items.</span></span>
  
![Exemple de statistiques de recherche affichant des éléments partiellement indexés](../media/PartiallyIndexedItemsTest.png)
  
<span data-ttu-id="359b5-128">Vous pouvez déterminer le pourcentage d’éléments partiellement indexés à l’aide des calculs suivants.</span><span class="sxs-lookup"><span data-stu-id="359b5-128">You can determine the percentage of partially indexed items by using the following calculations.</span></span>
  
 <span data-ttu-id="359b5-129">**Pour calculer le taux d’éléments partiellement indexés dans votre organisation :**</span><span class="sxs-lookup"><span data-stu-id="359b5-129">**To calculate the ratio of partially indexed items in your organization:**</span></span>

`(Total number of partially indexed items/Total number of items) x 100`

`(10025/1629904) x 100 = 0.62%`

<span data-ttu-id="359b5-130">À l’aide des résultats de recherche de l’exemple précédent, 0,62 % de tous les éléments de boîtes aux lettres sont partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="359b5-130">By using the search results from the previous example, 0.62% of all mailboxes items are partially indexed.</span></span>
  
 <span data-ttu-id="359b5-131">**Pour calculer le pourcentage de la taille des éléments partiellement indexés dans votre organisation :**</span><span class="sxs-lookup"><span data-stu-id="359b5-131">**To calculate the percentage of the size of partially indexed items in your organization:**</span></span>

`(Size of all partially indexed items/Size of all items) x 100`

`(10.27 GB/146.46 MB) x 100 = 7.0%`

<span data-ttu-id="359b5-132">Ainsi, dans l’exemple précédent, 7 % de la taille totale des éléments de boîte aux lettres sont des éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="359b5-132">So in the previous example, 7% of the total size of mailbox items are from partially indexed items.</span></span> <span data-ttu-id="359b5-133">Comme indiqué précédemment, la plupart des clients d’organisations ont moins de 1 % du contenu par volume et moins de 12 % du contenu par taille partiellement indexée.</span><span class="sxs-lookup"><span data-stu-id="359b5-133">As previously stated, most organizations customers have less than 1% of content by volume and less than 12% of content by size that is partially indexed.</span></span>

## <a name="working-with-partially-indexed-items"></a><span data-ttu-id="359b5-134">Travailler avec des éléments partiellement indexés</span><span class="sxs-lookup"><span data-stu-id="359b5-134">Working with partially indexed items</span></span>

<span data-ttu-id="359b5-135">Dans les cas où vous devez examiner partiellement les éléments pour vérifier [](export-a-content-search-report.md) qu’ils ne contiennent pas d’informations pertinentes, vous pouvez exporter un rapport de recherche de contenu qui contient des informations sur les éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="359b5-135">In cases when you need to examine partially items to validate that they don't contain relevant information, you can [export a content search report](export-a-content-search-report.md) that contains information about partially indexed items.</span></span> <span data-ttu-id="359b5-136">Lorsque vous exportez un rapport de recherche de contenu, n’oubliez pas de choisir l’une des options d’exportation qui inclut les éléments partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="359b5-136">When you export a content search report, be sure to choose one of the export options that includes partially indexed items.</span></span>
  
![Choisir la deuxième ou la troisième option pour exporter des éléments partiellement indexés](../media/PartiallyIndexedItemsExportOptions.png)
  
<span data-ttu-id="359b5-138">Lorsque vous exportez des résultats de recherche eDiscovery ou un rapport de recherche à l’aide de l’une de ces options, l’exportation inclut un rapport nommé Items.csv.</span><span class="sxs-lookup"><span data-stu-id="359b5-138">When you export eDiscovery search results or a search report using one of these options, the export includes a report named Unindexed Items.csv.</span></span> <span data-ttu-id="359b5-139">Ce rapport inclut la plupart des mêmes informations que le ResultsLog.csv de données . toutefois, le fichier Items.csv non indexé inclut également deux champs liés aux éléments partiellement indexés **:** les balises d’erreur et les propriétés **d’erreur.**</span><span class="sxs-lookup"><span data-stu-id="359b5-139">This report includes most of the same information as the ResultsLog.csv file; however, the Unindexed Items.csv file also includes two fields related to partially indexed items: **Error Tags** and **Error Properties**.</span></span> <span data-ttu-id="359b5-140">Ces champs contiennent des informations sur l’erreur d’indexation pour chaque élément partiellement indexé.</span><span class="sxs-lookup"><span data-stu-id="359b5-140">These fields contain information about the indexing error for each partially indexed item.</span></span> <span data-ttu-id="359b5-141">L’utilisation des informations de ces deux champs peut vous aider à déterminer si l’erreur d’indexation d’un événement particulier a un impact sur votre enquête.</span><span class="sxs-lookup"><span data-stu-id="359b5-141">Using the information in these two fields can help you determine whether or not the indexing error for a particular impacts your investigation.</span></span> <span data-ttu-id="359b5-142">Si c’est le cas, vous pouvez effectuer une recherche ciblée, récupérer et exporter des messages électroniques et des documents SharePoint ou OneDrive spécifiques afin de pouvoir les examiner afin de déterminer s’ils sont pertinents pour votre enquête.</span><span class="sxs-lookup"><span data-stu-id="359b5-142">If it does, you can perform a targeted search and retrieve and export specific email messages and SharePoint or OneDrive documents so that you can examine them to determine if they're relevant to your investigation.</span></span> <span data-ttu-id="359b5-143">Pour obtenir des instructions détaillées, voir Préparer un fichier [CSV](csv-file-for-an-id-list-content-search.md)pour une recherche ciblée dans Office 365 .</span><span class="sxs-lookup"><span data-stu-id="359b5-143">For step-by-step instructions, see [Prepare a CSV file for a targeted search in Office 365](csv-file-for-an-id-list-content-search.md).</span></span>

> [!NOTE]
> <span data-ttu-id="359b5-144">Le fichier Items.csv non Items.csv contient également des champs **nommés Type d’erreur** et **Message d’erreur.**</span><span class="sxs-lookup"><span data-stu-id="359b5-144">The Unindexed Items.csv file also contains fields named **Error Type** and **Error Message**.</span></span> <span data-ttu-id="359b5-145">Il s’agit de champs hérités qui  contiennent  des informations similaires aux informations des champs Balises d’erreur et Propriétés d’erreur, mais avec des informations moins détaillées.</span><span class="sxs-lookup"><span data-stu-id="359b5-145">These are legacy fields that contain information that is similar to the information in the **Error Tags** and **Error Properties** fields, but with less detailed information.</span></span> <span data-ttu-id="359b5-146">Vous pouvez ignorer ces champs hérités en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="359b5-146">You can safely ignore these legacy fields.</span></span>
  
## <a name="errors-related-to-partially-indexed-items"></a><span data-ttu-id="359b5-147">Erreurs liées aux éléments partiellement indexés</span><span class="sxs-lookup"><span data-stu-id="359b5-147">Errors related to partially indexed items</span></span>

<span data-ttu-id="359b5-148">Les balises d’erreur sont composés de deux éléments d’information, l’erreur et le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="359b5-148">Error tags are made up of two pieces of information, the error and the file type.</span></span> <span data-ttu-id="359b5-149">Par exemple, dans cette paire erreur/type de fichier :</span><span class="sxs-lookup"><span data-stu-id="359b5-149">For example, in this error/file-type pair:</span></span>

```text
 parseroutputsize_xls
```

 <span data-ttu-id="359b5-150">`parseroutputsize` est l’erreur `xls` et est le type de fichier du fichier sur qui l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="359b5-150">`parseroutputsize` is the error and `xls` is the file type of the file the error occurred on.</span></span> <span data-ttu-id="359b5-151">Dans les cas où le type de fichier n’a pas été reconnu ou s’il ne s’est pas appliqué à l’erreur, vous verrez la valeur à la `noformat` place du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="359b5-151">In cases where the file type wasn't recognized or the file type didn't apply to the error, you will see the value `noformat` in place of the file type.</span></span>
  
<span data-ttu-id="359b5-152">Voici une liste des erreurs d’indexation et une description de la cause possible de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="359b5-152">The following is a list of indexing errors and a description of the possible cause of the error.</span></span>
  
| <span data-ttu-id="359b5-153">Balise d’erreur</span><span class="sxs-lookup"><span data-stu-id="359b5-153">Error tag</span></span> | <span data-ttu-id="359b5-154">Description</span><span class="sxs-lookup"><span data-stu-id="359b5-154">Description</span></span> |
|:-----|:-----|
| `attachmentcount` <br/> |<span data-ttu-id="359b5-155">Un message électronique avait trop de pièces jointes et certaines de ces pièces jointes n’ont pas été traitées.</span><span class="sxs-lookup"><span data-stu-id="359b5-155">An email message had too many attachments, and some of these attachments weren't processed.</span></span>  <br/> |
| `attachmentdepth` <br/> |<span data-ttu-id="359b5-156">L’outil de récupération de contenu et l’outil d’étude de documents ont trouvé un trop grand nombre de niveaux de pièces jointes imbrmbrées dans d’autres pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="359b5-156">The content retriever and document parser found too many levels of attachments nested inside other attachments.</span></span> <span data-ttu-id="359b5-157">Certaines de ces pièces jointes n’ont pas été traitées.</span><span class="sxs-lookup"><span data-stu-id="359b5-157">Some of these attachments were not processed.</span></span>  <br/> |
| `attachmentrms` <br/> |<span data-ttu-id="359b5-158">Échec du décodage d’une pièce jointe car elle était protégée par RMS.</span><span class="sxs-lookup"><span data-stu-id="359b5-158">An attachment failed decoding because it was RMS-protected.</span></span>  <br/> |
| `attachmentsize` <br/> |<span data-ttu-id="359b5-159">Un fichier joint à un message électronique était trop grand et n’a pas pu être traitée.</span><span class="sxs-lookup"><span data-stu-id="359b5-159">A file attached to an email message was too large and couldn't be processed.</span></span>  <br/> |
| `indexingtruncated` <br/> |<span data-ttu-id="359b5-160">Lors de l’écriture du message électronique traitée dans l’index, l’une des propriétés indexables était trop grande et a été tronquée.</span><span class="sxs-lookup"><span data-stu-id="359b5-160">When writing the processed email message to the index, one of the indexable properties was too large and was truncated.</span></span> <span data-ttu-id="359b5-161">Les propriétés tronquées sont répertoriées dans le champ Propriétés d’erreur.</span><span class="sxs-lookup"><span data-stu-id="359b5-161">The truncated properties are listed in Error Properties field.</span></span>  <br/> |
| `invalidunicode` <br/> |<span data-ttu-id="359b5-162">Un message électronique contenait du texte qui n’a pas pu être traitée en tant qu’Unicode valide.</span><span class="sxs-lookup"><span data-stu-id="359b5-162">An email message contained text that couldn't be processed as valid Unicode.</span></span> <span data-ttu-id="359b5-163">L’indexation de cet élément peut être incomplète.</span><span class="sxs-lookup"><span data-stu-id="359b5-163">Indexing for this item may be incomplete.</span></span>  <br/> |
| `parserencrypted` <br/> |<span data-ttu-id="359b5-164">Le contenu de la pièce jointe ou du message électronique est chiffré et Microsoft 365 n’a pas pu décoder le contenu.</span><span class="sxs-lookup"><span data-stu-id="359b5-164">The content of attachment or email message is encrypted, and Microsoft 365 couldn't decode the content.</span></span>  <br/> |
| `parsererror` <br/> |<span data-ttu-id="359b5-165">Une erreur inconnue s’est produite lors de l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="359b5-165">An unknown error occurred during parsing.</span></span> <span data-ttu-id="359b5-166">Cela résulte généralement d’un bogue logiciel ou d’un incident de service.</span><span class="sxs-lookup"><span data-stu-id="359b5-166">This typically results from a software bug or a service crash.</span></span>  <br/> |
| `parserinputsize` <br/> |<span data-ttu-id="359b5-167">Une pièce jointe était trop volumineuse pour que l’outil d’outil de l’outil de recherche gère cette pièce jointe, et l’utilisation de cette pièce jointe n’a pas eu lieu ou n’a pas été achevée.</span><span class="sxs-lookup"><span data-stu-id="359b5-167">An attachment was too large for the parser to handle, and the parsing of that attachment didn't happen or wasn't completed.</span></span>  <br/> |
| `parsermalformed` <br/> |<span data-ttu-id="359b5-168">Une pièce jointe a été malformée et n’a pas pu être gérée par l’outil d’outils d’enquête.</span><span class="sxs-lookup"><span data-stu-id="359b5-168">An attachment was malformed and couldn't be handled by the parser.</span></span> <span data-ttu-id="359b5-169">Ce résultat peut être dû à d’anciens formats de fichiers, à des fichiers créés par des logiciels incompatibles ou à des virus qui prétendent être autre chose que revendiqués.</span><span class="sxs-lookup"><span data-stu-id="359b5-169">This result can be due to old file formats, files created by incompatible software, or viruses pretending to be something other than claimed.</span></span>  <br/> |
| `parseroutputsize` <br/> |<span data-ttu-id="359b5-170">La sortie de l’utilisation d’une pièce jointe était trop volumineuse et devait être tronquée.</span><span class="sxs-lookup"><span data-stu-id="359b5-170">The output from the parsing of an attachment was too large and had to be truncated.</span></span>  <br/> |
| `parserunknowntype` <br/> |<span data-ttu-id="359b5-171">Une pièce jointe avait un type de fichier Microsoft 365 impossible à détecter.</span><span class="sxs-lookup"><span data-stu-id="359b5-171">An attachment had a file type that Microsoft 365 couldn't detect.</span></span>  <br/> |
| `parserunsupportedtype` <br/> |<span data-ttu-id="359b5-172">Une pièce jointe avait un type de fichier que Office 365 pouvait détecter, mais l’examen de ce type de fichier n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="359b5-172">An attachment had a file type that Office 365 could detect, but parsing that file type isn't supported.</span></span>  <br/> |
| `propertytoobig` <br/> |<span data-ttu-id="359b5-173">La valeur d’une propriété de messagerie dans Exchange Store était trop grande pour être récupérée et le message n’a pas pu être traitée.</span><span class="sxs-lookup"><span data-stu-id="359b5-173">The value of an email property in Exchange Store was too large to be retrieved and the message couldn't be processed.</span></span> <span data-ttu-id="359b5-174">Cela se produit généralement uniquement pour la propriété body d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="359b5-174">This typically only happens to the body property of an email message.</span></span>  <br/> |
| `retrieverrms` <br/> |<span data-ttu-id="359b5-175">Le récupérateur de contenu n’a pas pu décoder un message protégé par RMS.</span><span class="sxs-lookup"><span data-stu-id="359b5-175">The content retriever failed to decode an RMS-protected message.</span></span>  <br/> |
| `wordbreakertruncated` <br/> |<span data-ttu-id="359b5-176">Trop de mots ont été identifiés dans le document lors de l’indexation.</span><span class="sxs-lookup"><span data-stu-id="359b5-176">Too many words were identified in the document during indexing.</span></span> <span data-ttu-id="359b5-177">Le traitement de la propriété s’est arrêté lorsque la limite est atteinte et la propriété est tronquée.</span><span class="sxs-lookup"><span data-stu-id="359b5-177">Processing of the property stopped when reaching the limit, and the property is truncated.</span></span>  <br/> |

<span data-ttu-id="359b5-178">Les champs d’erreur décrivent les champs affectés par l’erreur de traitement répertoriée dans le champ Balises d’erreur.</span><span class="sxs-lookup"><span data-stu-id="359b5-178">Error fields describe which fields are affected by the processing error listed in the Error Tags field.</span></span> <span data-ttu-id="359b5-179">Si vous recherchez une propriété telle que ou , les erreurs dans le corps du message n’auront pas  `subject`  `participants` d’impact sur les résultats de votre recherche.</span><span class="sxs-lookup"><span data-stu-id="359b5-179">If you're searching a property such as  `subject` or  `participants`, errors in the body of the message won't impact the results of your search.</span></span> <span data-ttu-id="359b5-180">Cela peut être utile lors de la détermination des éléments partiellement indexés que vous devrez peut-être examiner plus en détail.</span><span class="sxs-lookup"><span data-stu-id="359b5-180">This can be useful when determining exactly which partially indexed items you might need to further investigate.</span></span>
  
## <a name="using-a-powershell-script-to-determine-your-organizations-exposure-to-partially-indexed-email-items"></a><span data-ttu-id="359b5-181">Utilisation d’un script PowerShell pour déterminer l’exposition de votre organisation aux éléments de courrier partiellement indexés</span><span class="sxs-lookup"><span data-stu-id="359b5-181">Using a PowerShell script to determine your organization's exposure to partially indexed email items</span></span>

<span data-ttu-id="359b5-182">Les étapes suivantes vous montrent comment exécuter un script PowerShell qui recherche tous les éléments dans toutes les boîtes aux lettres Exchange, puis génère un rapport sur le rapport entre les éléments de courrier partiellement indexés de votre organisation (par nombre et par taille) et affiche le nombre d’éléments (et leur type de fichier) pour chaque erreur d’indexation qui se produit.</span><span class="sxs-lookup"><span data-stu-id="359b5-182">The following steps show you how to run a PowerShell script that searches for all items in all Exchange mailboxes, and then generates a report about your organization's ratio of partially indexed email items (by count and by size) and displays the number of items (and their file type) for each indexing error that occurs.</span></span> <span data-ttu-id="359b5-183">Utilisez les descriptions de balise d’erreur de la section précédente pour identifier l’erreur d’indexation.</span><span class="sxs-lookup"><span data-stu-id="359b5-183">Use the error tag descriptions in the previous section to identify the indexing error.</span></span>
  
1. <span data-ttu-id="359b5-184">Enregistrez le texte suivant dans un fichier Windows PowerShell script à l’aide d’un suffixe de nom de fichier .ps1 ; par exemple, `PartiallyIndexedItems.ps1` .</span><span class="sxs-lookup"><span data-stu-id="359b5-184">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `PartiallyIndexedItems.ps1`.</span></span>

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

2. <span data-ttu-id="359b5-185">[Se connecter à l’interface PowerShell du Centre de sécurité et conformité](/powershell/exchange/exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="359b5-185">[Connect to Security & Compliance Center PowerShell](/powershell/exchange/exchange-online-powershell).</span></span>

3. <span data-ttu-id="359b5-186">Dans le Centre de sécurité & conformité PowerShell, allez dans le dossier où vous avez enregistré le script à l’étape 1, puis exécutez le script . par exemple :</span><span class="sxs-lookup"><span data-stu-id="359b5-186">In Security & Compliance Center PowerShell, go to the folder where you saved the script in step 1, and then run the script; for example:</span></span>

   ```powershell
   .\PartiallyIndexedItems.ps1
   ```

<span data-ttu-id="359b5-187">Voici un exemple de sortie renvoyée par le script.</span><span class="sxs-lookup"><span data-stu-id="359b5-187">Here's an example fo the output returned by the script.</span></span>
  
![Exemple de sortie à partir d’un script qui génère un rapport sur l’exposition de votre organisation aux éléments de courrier partiellement indexés](../media/aeab5943-c15d-431a-bdb2-82f135abc2f3.png)

> [!NOTE]
> <span data-ttu-id="359b5-189">Veuillez prendre en compte les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="359b5-189">Note the following:</span></span>
>  
> - <span data-ttu-id="359b5-190">Le nombre total et la taille des éléments de courrier, ainsi que le rapport de votre organisation des éléments de courrier partiellement indexés (par nombre et par taille).</span><span class="sxs-lookup"><span data-stu-id="359b5-190">The total number and size of email items, and your organization's ratio of partially indexed email items (by count and by size).</span></span>
> 
> - <span data-ttu-id="359b5-191">Balises d’erreur de liste et types de fichiers correspondants pour lesquels l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="359b5-191">A list error tags and the corresponding file types for which the error occurred.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="359b5-192">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="359b5-192">See also</span></span>

[<span data-ttu-id="359b5-193">Éléments partiellement indexés dans eDiscovery</span><span class="sxs-lookup"><span data-stu-id="359b5-193">Partially indexed items in eDiscovery</span></span>](partially-indexed-items-in-content-search.md)