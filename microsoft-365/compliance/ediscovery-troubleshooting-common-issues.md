---
title: Résolution des problèmes eDiscovery courants
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: troubleshooting
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Découvrez les étapes de résolution des problèmes de base que vous pouvez suivre pour résoudre les problèmes courants dans Office 365 eDiscovery.
siblings_only: true
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 28c092cefbdd8add46d3f36aa118e230d16a918a
ms.sourcegitcommit: 50908a93554290ff1157b58d0a868a33e012513c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52822237"
---
# <a name="investigate-troubleshoot-and-resolve-common-ediscovery-issues"></a><span data-ttu-id="56576-103">Examiner, résoudre et résoudre les problèmes eDiscovery courants</span><span class="sxs-lookup"><span data-stu-id="56576-103">Investigate, troubleshoot, and resolve common eDiscovery issues</span></span>

<span data-ttu-id="56576-104">Cette rubrique traite des étapes de résolution des problèmes de base que vous pouvez effectuer pour identifier et résoudre les problèmes que vous pouvez rencontrer lors d’une recherche de découverte électronique ou ailleurs dans le processus eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="56576-104">This topic covers basic troubleshooting steps you can take to identify and resolve issues you may encounter during an eDiscovery search or elsewhere in the eDiscovery process.</span></span> <span data-ttu-id="56576-105">La résolution de certains de ces scénarios nécessite l’aide du Support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="56576-105">Resolving some of these scenarios requires help from Microsoft Support.</span></span> <span data-ttu-id="56576-106">Les informations sur le moment où contacter le Support Microsoft sont incluses dans les étapes de résolution.</span><span class="sxs-lookup"><span data-stu-id="56576-106">Information on when to contact Microsoft Support is included in the resolution steps.</span></span>

## <a name="errorissue-ambiguous-location"></a><span data-ttu-id="56576-107">Erreur/problème : emplacement ambigu</span><span class="sxs-lookup"><span data-stu-id="56576-107">Error/issue: Ambiguous location</span></span>

<span data-ttu-id="56576-108">Si vous essayez d’ajouter l’emplacement de la boîte aux lettres de l’utilisateur à rechercher et qu’il existe des objets en double ou en conflit avec le même userID dans l’annuaire Exchange Online Protection (EOP), vous recevez cette erreur : `The compliance search contains the following invalid location(s):useralias@contoso.com. The location "useralias@contoso.com" is ambiguous` .</span><span class="sxs-lookup"><span data-stu-id="56576-108">If you try to add user's mailbox location to search and there are duplicate or conflicting objects with the same userID in the Exchange Online Protection (EOP) directory, you receive this error: `The compliance search contains the following invalid location(s):useralias@contoso.com. The location "useralias@contoso.com" is ambiguous`.</span></span>

### <a name="resolution"></a><span data-ttu-id="56576-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="56576-109">Resolution</span></span>

<span data-ttu-id="56576-110">Recherchez des utilisateurs en double ou une liste de distribution avec le même ID d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56576-110">Check for duplicate users or distribution list with the same user ID.</span></span>

1. <span data-ttu-id="56576-111">Connecter [au Centre de sécurité & conformité PowerShell.](/powershell/exchange/connect-to-scc-powershell)</span><span class="sxs-lookup"><span data-stu-id="56576-111">Connect to [Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell).</span></span>

2. <span data-ttu-id="56576-112">Exécutez la commande suivante pour récupérer toutes les instances du nom d’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="56576-112">Run the following command to retrieve all instances of the username:</span></span>

    ```powershell
    Get-Recipient <username>
    ```

   <span data-ttu-id="56576-113">La sortie de « useralias@contoso.com » serait similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="56576-113">The output for 'useralias@contoso.com' would be similar to the following:</span></span>

   > 
   > |<span data-ttu-id="56576-114">Nom</span><span class="sxs-lookup"><span data-stu-id="56576-114">Name</span></span>|<span data-ttu-id="56576-115">RecipientType</span><span class="sxs-lookup"><span data-stu-id="56576-115">RecipientType</span></span>|
   > |---|---|
   > |<span data-ttu-id="56576-116">Alias, Utilisateur</span><span class="sxs-lookup"><span data-stu-id="56576-116">Alias, User</span></span>|<span data-ttu-id="56576-117">MailUser</span><span class="sxs-lookup"><span data-stu-id="56576-117">MailUser</span></span>|
   > |<span data-ttu-id="56576-118">Alias, Utilisateur</span><span class="sxs-lookup"><span data-stu-id="56576-118">Alias, User</span></span>|<span data-ttu-id="56576-119">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="56576-119">User</span></span>|

3. <span data-ttu-id="56576-120">Si plusieurs utilisateurs sont renvoyés, recherchez et corrigez l’objet en conflit.</span><span class="sxs-lookup"><span data-stu-id="56576-120">If multiple users are returned, locate and fix the conflicting object.</span></span>

## <a name="errorissue-search-fails-on-specific-locations"></a><span data-ttu-id="56576-121">Erreur/problème : la recherche échoue à des emplacements spécifiques</span><span class="sxs-lookup"><span data-stu-id="56576-121">Error/issue: Search fails on specific locations</span></span>

<span data-ttu-id="56576-122">Une recherche eDiscovery ou de contenu peut produire l’erreur suivante : `This search completed with (#) errors.  Would you like to retry the search on the failed locations?`</span><span class="sxs-lookup"><span data-stu-id="56576-122">An eDiscovery or content search may yield the following error: `This search completed with (#) errors.  Would you like to retry the search on the failed locations?`</span></span>

![Capture d’écran d’erreur d’erreur d’un emplacement spécifique à la recherche](../media/edisc-tshoot-specific-location-search-fails.png)

### <a name="resolution"></a><span data-ttu-id="56576-124">Résolution</span><span class="sxs-lookup"><span data-stu-id="56576-124">Resolution</span></span>

<span data-ttu-id="56576-125">Si vous recevez cette erreur, nous vous recommandons de vérifier les emplacements qui ont échoué dans la recherche, puis de réexécuter la recherche uniquement sur les emplacements qui ont échoué.</span><span class="sxs-lookup"><span data-stu-id="56576-125">If you receive this error, we recommend that you verify the locations that failed in the search  then rerun the search only on the failed locations.</span></span>

1. <span data-ttu-id="56576-126">Connecter [au Centre de sécurité & conformité PowerShell,](/powershell/exchange/connect-to-scc-powershell) puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="56576-126">Connect to [Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell) and then run the following command:</span></span>

   ```powershell
   Get-ComplianceSearch <searchname> | FL
   ```

2. <span data-ttu-id="56576-127">À partir de la sortie PowerShell, affichez les emplacements qui ont échoué dans le champ erreurs ou à partir des détails d’état dans l’erreur à partir de la sortie de recherche.</span><span class="sxs-lookup"><span data-stu-id="56576-127">From the PowerShell output, view the failed locations in the errors field or from the status details in the error from the search output.</span></span>

3. <span data-ttu-id="56576-128">Réessayez la recherche eDiscovery sur les emplacements qui ont échoué uniquement.</span><span class="sxs-lookup"><span data-stu-id="56576-128">Retry the eDiscovery search on the failed locations only.</span></span>

4. <span data-ttu-id="56576-129">Si vous continuez à recevoir ces erreurs, consultez Réessayer les emplacements d’échec [pour](/Office365/SecurityCompliance/retry-failed-content-search) plus d’étapes de résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="56576-129">If you continue to receive these errors, see [Retry failed locations](/Office365/SecurityCompliance/retry-failed-content-search) for more troubleshooting steps.</span></span>

## <a name="errorissue-file-not-found"></a><span data-ttu-id="56576-130">Erreur/problème : fichier in trouvé</span><span class="sxs-lookup"><span data-stu-id="56576-130">Error/issue: File not found</span></span>

<span data-ttu-id="56576-131">Lors de l’exécution d’une recherche de découverte électronique qui inclut SharePoint Online et les emplacements One Drive for Business, vous pouvez recevoir l’erreur même si le fichier se trouve `File Not Found` sur le site.</span><span class="sxs-lookup"><span data-stu-id="56576-131">When running an eDiscovery search that includes SharePoint Online and One Drive For Business locations, you may receive the error `File Not Found` although the file is located on the site.</span></span> <span data-ttu-id="56576-132">Cette erreur sera dans les avertissements d’exportation et errors.csv ou ignorée items.csv.</span><span class="sxs-lookup"><span data-stu-id="56576-132">This error will be in the export warnings and errors.csv or skipped items.csv.</span></span> <span data-ttu-id="56576-133">Cela peut se produire si le fichier n’est pas trouvé sur le site ou si l’index n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="56576-133">This may occur if the file can't be found on the site or if the index is out of date.</span></span> <span data-ttu-id="56576-134">Voici le texte d’une erreur réelle (avec une accentuation ajoutée).</span><span class="sxs-lookup"><span data-stu-id="56576-134">Here's the text of an actual error (with emphasis added).</span></span>

> <span data-ttu-id="56576-135">28.06.2019 10:02:19_FailedToExportItem_Failed télécharger du contenu.</span><span class="sxs-lookup"><span data-stu-id="56576-135">28.06.2019 10:02:19_FailedToExportItem_Failed to download content.</span></span> <span data-ttu-id="56576-136">Informations de diagnostic supplémentaires : Microsoft. Office. Compliance.EDiscovery.ExportWorker.Exceptions.ContentDownloadTemporaryFailure: Failed to download from content 6ea52149-91cd-4965-b5bb-82ca6a3ec9be of type Document.</span><span class="sxs-lookup"><span data-stu-id="56576-136">Additional diagnostic info : Microsoft.Office.Compliance.EDiscovery.ExportWorker.Exceptions.ContentDownloadTemporaryFailure: Failed to download from content 6ea52149-91cd-4965-b5bb-82ca6a3ec9be of type Document.</span></span> <span data-ttu-id="56576-137">ID de corrélation : 3bd84722-937b-4c23-b61b-08d6fba9ec32.</span><span class="sxs-lookup"><span data-stu-id="56576-137">Correlation Id: 3bd84722-937b-4c23-b61b-08d6fba9ec32.</span></span> <span data-ttu-id="56576-138">ServerErrorCode: -2147024894 ---> Microsoft. SharePoint. Client.ServerException : ***fichier in trouvé.***</span><span class="sxs-lookup"><span data-stu-id="56576-138">ServerErrorCode: -2147024894 ---> Microsoft.SharePoint.Client.ServerException: ***File Not Found***.</span></span> <span data-ttu-id="56576-139">chez Microsoft. SharePoint. Client.ClientRequest.ProcessResponseStream(Stream responseStream) chez Microsoft. SharePoint. Client.ClientRequest.ProcessResponse() --- fin de la trace de pile des exceptions internes ---</span><span class="sxs-lookup"><span data-stu-id="56576-139">at Microsoft.SharePoint.Client.ClientRequest.ProcessResponseStream(Stream responseStream) at Microsoft.SharePoint.Client.ClientRequest.ProcessResponse() --- End of inner exception stack trace ---</span></span>

### <a name="resolution"></a><span data-ttu-id="56576-140">Résolution</span><span class="sxs-lookup"><span data-stu-id="56576-140">Resolution</span></span>

1. <span data-ttu-id="56576-141">Vérifiez l’emplacement identifié dans la recherche pour vous assurer que l’emplacement du fichier est correct et ajouté aux emplacements de recherche.</span><span class="sxs-lookup"><span data-stu-id="56576-141">Check location identified in the search to ensure that the location of the file is correct and added in the search locations.</span></span>

2. <span data-ttu-id="56576-142">Utilisez les procédures de demande manuelle d’analyse et [de réindexation](/sharepoint/crawl-site-content) d’un site, d’une bibliothèque ou d’une liste pour réindexer le site.</span><span class="sxs-lookup"><span data-stu-id="56576-142">Use the procedures at [Manually request crawling and re-indexing of a site, a library, or a list](/sharepoint/crawl-site-content) to reindex the site.</span></span>

## <a name="errorissue-this-file-wasnt-exported-because-it-doesnt-exist-anymore-the-file-was-included-in-the-count-of-estimated-search-results-because-its-still-listed-in-the-index-the-file-will-eventually-be-removed-from-the-index-and-wont-cause-an-error-in-the-future"></a><span data-ttu-id="56576-143">Erreur/problème : ce fichier n’a pas été exporté car il n’existe plus.</span><span class="sxs-lookup"><span data-stu-id="56576-143">Error/issue: This file wasn't exported because it doesn't exist anymore.</span></span> <span data-ttu-id="56576-144">Le fichier a été inclus dans le nombre de résultats de recherche estimés, car il est toujours répertorié dans l’index.</span><span class="sxs-lookup"><span data-stu-id="56576-144">The file was included in the count of estimated search results because it's still listed in the index.</span></span> <span data-ttu-id="56576-145">Le fichier sera finalement supprimé de l’index et ne provoquera pas d’erreur à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="56576-145">The file will eventually be removed from the index, and won't cause an error in the future.</span></span>

<span data-ttu-id="56576-146">Vous pouvez voir cette erreur lors de l’exécution d’une recherche de découverte électronique qui inclut SharePoint en ligne et One Drive for Business.</span><span class="sxs-lookup"><span data-stu-id="56576-146">You may see that error when running an eDiscovery search that includes SharePoint Online and One Drive For Business locations.</span></span> <span data-ttu-id="56576-147">eDiscovery s’appuie sur l’index SPO pour identifier les emplacements de fichiers.</span><span class="sxs-lookup"><span data-stu-id="56576-147">eDiscovery relies on teh SPO index to identify the file locations.</span></span> <span data-ttu-id="56576-148">Si le fichier a été supprimé mais que l’index SPO n’a pas encore été mis à jour, cette erreur peut se produire.</span><span class="sxs-lookup"><span data-stu-id="56576-148">If the file was deleted but the SPO index was not yet updated this error may occur.</span></span>

### <a name="resolution"></a><span data-ttu-id="56576-149">Résolution</span><span class="sxs-lookup"><span data-stu-id="56576-149">Resolution</span></span> 
<span data-ttu-id="56576-150">Ouvrez l’emplacement SPO et vérifiez que ce fichier n’y est pas.</span><span class="sxs-lookup"><span data-stu-id="56576-150">Open the SPO location and verify that this file indeed is not there.</span></span>
<span data-ttu-id="56576-151">La solution suggérée consiste à réindexer manuellement le site ou à attendre la réindexation du site par le processus en arrière-plan automatique.</span><span class="sxs-lookup"><span data-stu-id="56576-151">Suggested solution is to manually reindex the site, or wait till the site reindexes by the automatic background process.</span></span>


## <a name="errorissue-this-search-result-was-not-downloaded-as-it-is-a-folder-or-other-artefact-that-cant-be-downloaded-by-itself-any-items-inside-the-folder-or-library-will-be-downloaded"></a><span data-ttu-id="56576-152">Erreur/problème : ce résultat de recherche n’a pas été téléchargé car il s’agit d’un dossier ou d’un autre artefact qui ne peut pas être téléchargé seul, tous les éléments à l’intérieur du dossier ou de la bibliothèque seront téléchargés.</span><span class="sxs-lookup"><span data-stu-id="56576-152">Error/issue: This search result was not downloaded as it is a folder or other artefact that can't be downloaded by itself, any items inside the folder or library will be downloaded.</span></span>

<span data-ttu-id="56576-153">Vous pouvez voir cette erreur lors de l’exécution d’une recherche de découverte électronique qui inclut SharePoint en ligne et One Drive for Business.</span><span class="sxs-lookup"><span data-stu-id="56576-153">You may see that error when running an eDiscovery search that includes SharePoint Online and One Drive For Business locations.</span></span> <span data-ttu-id="56576-154">Cela signifie que nous allions essayer d’exporter l’élément signalé dans l’index, mais qu’il s’est traduit par un dossier afin de ne pas l’exporter.</span><span class="sxs-lookup"><span data-stu-id="56576-154">It means that we were going to try and export the item reported in the index, but it turned out to be a folder so we did not export it.</span></span> <span data-ttu-id="56576-155">Comme mentionné dans l’erreur, nous n’exportons pas les éléments de dossier, mais nous exportons leur contenu.</span><span class="sxs-lookup"><span data-stu-id="56576-155">As mentioned in the error, we don't export folder items but we do export their contents.</span></span>


## <a name="errorissue-search-fails-because-recipient-is-not-found"></a><span data-ttu-id="56576-156">Erreur/problème : la recherche échoue car le destinataire est in trouvé</span><span class="sxs-lookup"><span data-stu-id="56576-156">Error/issue: Search fails because recipient is not found</span></span>

<span data-ttu-id="56576-157">Une recherche eDiscovery échoue avec l’erreur . `recipient not found`</span><span class="sxs-lookup"><span data-stu-id="56576-157">An eDiscovery search fails with error the `recipient not found`.</span></span> <span data-ttu-id="56576-158">Cette erreur peut se produire si l’objet utilisateur est in Exchange Online Protection (EOP) car l’objet n’a pas été synchronisé.</span><span class="sxs-lookup"><span data-stu-id="56576-158">This error may occur if the user object cannot be found in Exchange Online Protection (EOP) because the object has not synced.</span></span>

### <a name="resolution"></a><span data-ttu-id="56576-159">Résolution</span><span class="sxs-lookup"><span data-stu-id="56576-159">Resolution</span></span>

1. <span data-ttu-id="56576-160">Connectez-vous à [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="56576-160">Connect to [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="56576-161">Exécutez la commande suivante pour vérifier si l’utilisateur est synchronisé avec Exchange Online Protection :</span><span class="sxs-lookup"><span data-stu-id="56576-161">Run the following command to check if the user is synced to Exchange Online Protection:</span></span>

   ```powershell
   Get-Recipient <userId> | FL
   ```

3. <span data-ttu-id="56576-162">Il doit y avoir un objet utilisateur de messagerie pour la question de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56576-162">There should be a mail user object for the user question.</span></span> <span data-ttu-id="56576-163">Si rien n’est renvoyé, examinez l’objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56576-163">If nothing is returned, investigate the user object.</span></span> <span data-ttu-id="56576-164">Contactez le Support Microsoft si l’objet ne peut pas être synchronisé.</span><span class="sxs-lookup"><span data-stu-id="56576-164">Contact Microsoft Support if the object can't be synced.</span></span>

## <a name="errorissue-exporting-search-results-is-slow"></a><span data-ttu-id="56576-165">Erreur/problème : l’exportation des résultats de recherche est lente</span><span class="sxs-lookup"><span data-stu-id="56576-165">Error/issue: Exporting search results is slow</span></span>

<span data-ttu-id="56576-166">Lors de l’exportation des résultats de recherche à partir d’eDiscovery ou de recherche de contenu dans le Centre de sécurité et conformité, le téléchargement prend plus de temps que prévu.</span><span class="sxs-lookup"><span data-stu-id="56576-166">When exporting search results from eDiscovery or Content Search in the Security and Compliance center, the download takes longer than expected.</span></span>  <span data-ttu-id="56576-167">Vous pouvez vérifier la quantité de données à télécharger et éventuellement augmenter la vitesse d’exportation.</span><span class="sxs-lookup"><span data-stu-id="56576-167">You can check to see the amount of data to be download and possibly increase the export speed.</span></span>

### <a name="resolution"></a><span data-ttu-id="56576-168">Résolution</span><span class="sxs-lookup"><span data-stu-id="56576-168">Resolution</span></span>

1. <span data-ttu-id="56576-169">Connecter [au Centre de sécurité & conformité PowerShell,](/powershell/exchange/connect-to-scc-powershell) puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="56576-169">Connect to [Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell) and then run the following command:</span></span>

   ```powershell
   Get-ComplianceSearch <searchname> | FL
   ```

2. <span data-ttu-id="56576-170">Recherchez la quantité de données à télécharger dans les paramètres SearchResults et SearchStatistics.</span><span class="sxs-lookup"><span data-stu-id="56576-170">Find the amount of data to be downloaded in the SearchResults and SearchStatistics parameters.</span></span>

3. <span data-ttu-id="56576-171">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="56576-171">Run the following command:</span></span>

   ```powershell
   Get-ComplianceSearchAction | FL
   ```

4. <span data-ttu-id="56576-172">Dans le champ résultats, recherchez les données qui ont été exportées et affichez les erreurs rencontrées.</span><span class="sxs-lookup"><span data-stu-id="56576-172">In the results field, find the data that has been exported and view any errors encountered.</span></span>

5. <span data-ttu-id="56576-173">Recherchez les erreurs éventuelles dans le fichier trace.log situé dans le répertoire vers qui vous avez exporté le contenu.</span><span class="sxs-lookup"><span data-stu-id="56576-173">Check the trace.log file located in the directory that you exported the content to for any errors.</span></span>

6. <span data-ttu-id="56576-174">Si vous avez encore des problèmes, envisagez de diviser les recherches qui retournent un grand ensemble de résultats en recherches plus petites.</span><span class="sxs-lookup"><span data-stu-id="56576-174">If you still have issues, consider dividing searches that return a large set of results into smaller searches.</span></span> <span data-ttu-id="56576-175">Par exemple, vous pouvez utiliser des plages de dates dans les requêtes de recherche pour renvoyer un ensemble de résultats plus petit qui peut être téléchargé plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="56576-175">For example, you can use date ranges in search queries to return a smaller set of results that can be downloaded faster.</span></span>

## <a name="errorissue-internal-server-error-500-occurred"></a><span data-ttu-id="56576-176">Erreur/problème : « Une erreur de serveur interne (500) s’est produite »</span><span class="sxs-lookup"><span data-stu-id="56576-176">Error/issue: "Internal server error (500) occurred"</span></span>

<span data-ttu-id="56576-177">Lors de l’exécution d’une recherche de découverte électronique, si la recherche échoue continuellement avec une erreur semblable à « Erreur interne du serveur (500) s’est produite », vous devrez peut-être réexécuter la recherche uniquement sur des emplacements de boîtes aux lettres spécifiques.</span><span class="sxs-lookup"><span data-stu-id="56576-177">When running an eDiscovery search, if the search continually fails with error similar to "Internal server error (500) occurred", you may need rerun the search only on specific mailbox locations.</span></span>

![Capture d’écran de l’erreur du serveur interne 500](../media/edisc-tshoot-error-500.png)

### <a name="resolution"></a><span data-ttu-id="56576-179">Résolution</span><span class="sxs-lookup"><span data-stu-id="56576-179">Resolution</span></span>

1. <span data-ttu-id="56576-180">Décomposez la recherche en recherches plus petites et exécutez à nouveau la recherche.</span><span class="sxs-lookup"><span data-stu-id="56576-180">Break the search into smaller searches and run the search again.</span></span>  <span data-ttu-id="56576-181">Essayez d’utiliser une plage de dates plus petite ou limitez le nombre d’emplacements recherchés.</span><span class="sxs-lookup"><span data-stu-id="56576-181">Try using a smaller date range or limit the number of locations being searched.</span></span>

2. <span data-ttu-id="56576-182">Connecter [au Centre de sécurité & conformité PowerShell,](/powershell/exchange/connect-to-scc-powershell) puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="56576-182">Connect to [Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell) and then run the following command:</span></span>

   ```powershell Set-CaseHoldPolicy <policyname> -RetryDistribution
   Get-ComplianceSearch <searchname> | FL
   ```

3. <span data-ttu-id="56576-183">Examinez la sortie pour les résultats et les erreurs.</span><span class="sxs-lookup"><span data-stu-id="56576-183">Examine the output for results and errors.</span></span>

4. <span data-ttu-id="56576-184">Examinez le fichier trace.log.</span><span class="sxs-lookup"><span data-stu-id="56576-184">Examine the trace.log file.</span></span> <span data-ttu-id="56576-185">Il se trouve dans le même dossier que celui vers qui vous avez exporté les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="56576-185">It's located  in the same folder that you exported the search results to.</span></span>

5. <span data-ttu-id="56576-186">Contactez le support technique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="56576-186">Contact Microsoft Support.</span></span>

## <a name="errorissue-holds-dont-sync"></a><span data-ttu-id="56576-187">Erreur/problème : les holds ne sont pas synchronisés</span><span class="sxs-lookup"><span data-stu-id="56576-187">Error/issue: Holds don't sync</span></span>

<span data-ttu-id="56576-188">Erreur de distribution de synchronisation de stratégie de la stratégie de prise en main eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="56576-188">eDiscovery Case Hold Policy Sync Distribution error.</span></span> <span data-ttu-id="56576-189">L’erreur se lit comme ci-après :</span><span class="sxs-lookup"><span data-stu-id="56576-189">The error reads:</span></span>

> <span data-ttu-id="56576-190">« Ressources : le déploiement de la stratégie prend plus de temps que prévu.</span><span class="sxs-lookup"><span data-stu-id="56576-190">"Resources: It's taking longer than expected to deploy the policy.</span></span> <span data-ttu-id="56576-191">La mise à jour de l’état de déploiement final peut prendre 2 heures supplémentaires, donc vérifiez-la dans quelques heures. »</span><span class="sxs-lookup"><span data-stu-id="56576-191">It might take an additional 2 hours to update the final deployment status, so check back in a couple hours."</span></span>

### <a name="resolution"></a><span data-ttu-id="56576-192">Résolution</span><span class="sxs-lookup"><span data-stu-id="56576-192">Resolution</span></span>

1. <span data-ttu-id="56576-193">Connecter au Centre de sécurité & conformité [PowerShell,](/powershell/exchange/connect-to-scc-powershell) puis exécutez la commande suivante pour une mise en attente de cas eDiscovery :</span><span class="sxs-lookup"><span data-stu-id="56576-193">Connect to [Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell) and then run the following command for an eDiscovery case hold:</span></span>

   ```powershell
   Get-CaseHoldPolicy <policyname> - DistributionDetail | FL
   ```

    <span data-ttu-id="56576-194">Pour une stratégie de rétention, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="56576-194">For a retention policy, run the following command:</span></span>

   ```powershell
   Get-RetentionCompliancePolicy <policyname> - DistributionDetail | FL
   ```

2. <span data-ttu-id="56576-195">Examinez la valeur dans le paramètre DistributionDetail pour les erreurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="56576-195">Examine the value in the DistributionDetail parameter for errors like the following:</span></span>

   > <span data-ttu-id="56576-196">Erreur : Ressources : le déploiement de la stratégie prend plus de temps que prévu.</span><span class="sxs-lookup"><span data-stu-id="56576-196">Error: Resources: It's taking longer than expected to deploy the policy.</span></span> <span data-ttu-id="56576-197">La mise à jour de l’état de déploiement final peut prendre 2 heures supplémentaires, donc vérifiez-la dans quelques heures. »</span><span class="sxs-lookup"><span data-stu-id="56576-197">It might take an additional 2 hours to update the final deployment status, so check back in a couple hours."</span></span>

3. <span data-ttu-id="56576-198">Essayez d’exécutez le paramètre RetryDistribution sur la stratégie en question :</span><span class="sxs-lookup"><span data-stu-id="56576-198">Try running the RetryDistribution parameter on the policy in question:</span></span>

   <span data-ttu-id="56576-199">Pour les cas eDiscovery :</span><span class="sxs-lookup"><span data-stu-id="56576-199">For eDiscovery case holds:</span></span>

   ```powershell
   Set-CaseHoldPolicy <policyname> -RetryDistribution
   ```

   <span data-ttu-id="56576-200">Pour les stratégies de rétention :</span><span class="sxs-lookup"><span data-stu-id="56576-200">For retention policies:</span></span>

   ```powershell
   Set-RetentionCompliancePolicy <policyname> -RetryDistribution
   ```

4. <span data-ttu-id="56576-201">Contactez le support technique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="56576-201">Contact Microsoft Support.</span></span>

## <a name="error-the-condition-specified-using-http-conditional-headers-is-not-met"></a><span data-ttu-id="56576-202">Erreur : « La condition spécifiée à l’aide d’en-têtes conditionnels HTTP n’est pas remplie »</span><span class="sxs-lookup"><span data-stu-id="56576-202">Error: "The condition specified using HTTP conditional header(s) is not met"</span></span>

<span data-ttu-id="56576-203">Lorsque vous téléchargez des résultats de recherche à l’aide de l’outil d’exportation eDiscovery, il est possible que vous receviez l’erreur suivante : Il s’agit d’une erreur passagère, qui se produit généralement à `System.Net.WebException: The remote server returned an error: (412) The condition specified using HTTP conditional header(s) is not met.` l’emplacement stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="56576-203">When downloading search results using the eDiscovery Export Tool, it's possible you might receive the following error: `System.Net.WebException: The remote server returned an error: (412) The condition specified using HTTP conditional header(s) is not met.` This is transient error, which typically occurs in the Azure Storage location.</span></span>

### <a name="resolution"></a><span data-ttu-id="56576-204">Résolution</span><span class="sxs-lookup"><span data-stu-id="56576-204">Resolution</span></span>

<span data-ttu-id="56576-205">Pour résoudre ce problème, réessayez de [télécharger](export-search-results.md#step-2-download-the-search-results)les résultats de la recherche, ce qui redémarrera l’outil d’exportation eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="56576-205">To resolve this issue, retry [downloading the search results](export-search-results.md#step-2-download-the-search-results), which will restart the eDiscovery Export Tool.</span></span>

## <a name="errorissue-downloaded-export-shows-no-results"></a><span data-ttu-id="56576-206">Erreur/problème : l’exportation téléchargée n’affiche aucun résultat</span><span class="sxs-lookup"><span data-stu-id="56576-206">Error/issue: Downloaded export shows no results</span></span>

<span data-ttu-id="56576-207">Une fois l’exportation réussie, le téléchargement terminé via l’outil d’exportation affiche zéro fichier dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="56576-207">After a successful export, the completed download via the export tool shows zero files in the results.</span></span>

### <a name="resolution"></a><span data-ttu-id="56576-208">Résolution</span><span class="sxs-lookup"><span data-stu-id="56576-208">Resolution</span></span>

<span data-ttu-id="56576-209">Il s’agit d’un problème côté client et, pour y remédier, essayez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="56576-209">This is a client-side issue and in order to remediate it, please attempt the following steps:</span></span>

1. <span data-ttu-id="56576-210">Essayez d’utiliser un autre client/ordinateur pour télécharger.</span><span class="sxs-lookup"><span data-stu-id="56576-210">Try using another client/machine to download.</span></span>

2. <span data-ttu-id="56576-211">Supprimez les anciennes recherches qui ne sont plus nécessaires à l’aide de la cmdlet [Remove-ComplianceSearch.](/powershell/module/exchange/remove-compliancesearch)</span><span class="sxs-lookup"><span data-stu-id="56576-211">Remove old searches that are no longer needed using [Remove-ComplianceSearch](/powershell/module/exchange/remove-compliancesearch) cmdlet.</span></span>

3. <span data-ttu-id="56576-212">Veillez à effectuer le téléchargement sur un lecteur local.</span><span class="sxs-lookup"><span data-stu-id="56576-212">Make sure to download to a local drive.</span></span>

4. <span data-ttu-id="56576-213">Assurez-vous que le scanneur antivirus n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="56576-213">Make sure the virus scanner is not running.</span></span>

5. <span data-ttu-id="56576-214">Assurez-vous qu’aucune autre exportation n’est téléchargée vers le même dossier ou n’importe quel dossier parent.</span><span class="sxs-lookup"><span data-stu-id="56576-214">Make sure that no other export is downloading to the same folder or any parent folder.</span></span>

6. <span data-ttu-id="56576-215">Si les étapes précédentes ne fonctionnent pas, désactivez la fermeture à la fermeture de la fermeture et la déplication.</span><span class="sxs-lookup"><span data-stu-id="56576-215">If the previous steps did not work, disable zipping and de-duplication.</span></span>

7. <span data-ttu-id="56576-216">Si cela fonctionne, le problème est dû à un scanneur antivirus local ou à un problème de disque.</span><span class="sxs-lookup"><span data-stu-id="56576-216">If this works then the issue is due to a local virus scanner or a disk issue.</span></span>
