---
title: Dépannage des problèmes eDiscovery courants
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Examinez, dépannez et résolvez les problèmes courants dans eDiscovery.
siblings_only: true
ms.openlocfilehash: 5bcbe498cb650268dc8ff6f2b41a6201e75a8192
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43631769"
---
# <a name="investigate-troubleshoot-and-resolve-common-ediscovery-issues"></a><span data-ttu-id="aa17c-103">Examiner, dépanner et résoudre les problèmes eDiscovery courants</span><span class="sxs-lookup"><span data-stu-id="aa17c-103">Investigate, troubleshoot, and resolve common eDiscovery issues</span></span>

<span data-ttu-id="aa17c-104">Cette rubrique décrit les étapes de résolution des problèmes que vous pouvez effectuer pour identifier et résoudre les problèmes que vous pouvez rencontrer lors d’une recherche de découverte électronique ou ailleurs dans le processus de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="aa17c-104">This topic covers basic troubleshooting steps you can take to identify and resolve issues you may encounter during an eDiscovery search or elsewhere in the eDiscovery process.</span></span> <span data-ttu-id="aa17c-105">La résolution de certains de ces scénarios nécessite de l’aide du support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aa17c-105">Resolving some of these scenarios requires help from Microsoft Support.</span></span> <span data-ttu-id="aa17c-106">Vous trouverez des informations sur le moment auquel contacter le support Microsoft dans la procédure de résolution.</span><span class="sxs-lookup"><span data-stu-id="aa17c-106">Information on when to contact Microsoft Support is included in the resolution steps.</span></span>

## <a name="errorissue-ambiguous-location"></a><span data-ttu-id="aa17c-107">Erreur/problème : emplacement ambigu</span><span class="sxs-lookup"><span data-stu-id="aa17c-107">Error/issue: Ambiguous location</span></span>

<span data-ttu-id="aa17c-108">Si vous essayez d’ajouter l’emplacement de la boîte aux lettres d’un utilisateur à la recherche et qu’il existe des objets en double ou en conflit avec le même ID utilisateur dans le répertoire Exchange `The compliance search contains the following invalid location(s):useralias@contoso.com. The location "useralias@contoso.com" is ambiguous`Online Protection (EoP), vous recevez le message d’erreur suivant :.</span><span class="sxs-lookup"><span data-stu-id="aa17c-108">If you try to add user's mailbox location to search and there are duplicate or conflicting objects with the same userID in the Exchange Online Protection (EOP) directory, you receive this error: `The compliance search contains the following invalid location(s):useralias@contoso.com. The location "useralias@contoso.com" is ambiguous`.</span></span> 

### <a name="resolution"></a><span data-ttu-id="aa17c-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="aa17c-109">Resolution</span></span>

<span data-ttu-id="aa17c-110">Recherchez les utilisateurs en double ou la liste de distribution avec le même ID d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aa17c-110">Check for duplicate users or distribution list with the same user ID.</span></span>

1. <span data-ttu-id="aa17c-111">Connectez-vous à [la sécurité & Centre de conformité PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="aa17c-111">Connect to [Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>

2. <span data-ttu-id="aa17c-112">Exécutez la commande suivante pour récupérer toutes les instances du nom d’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="aa17c-112">Run the following command to retrieve all instances of the username:</span></span>

    ```powershell
    Get-Recipient <username>
    ```

   <span data-ttu-id="aa17c-113">La sortie de « useralias@contoso.com » est semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="aa17c-113">The output for 'useralias@contoso.com' would be similar to the following:</span></span>

   > 
   > |<span data-ttu-id="aa17c-114">Nom</span><span class="sxs-lookup"><span data-stu-id="aa17c-114">Name</span></span>  |<span data-ttu-id="aa17c-115">RecipientType</span><span class="sxs-lookup"><span data-stu-id="aa17c-115">RecipientType</span></span>  |
   > |---------|---------|
   > |<span data-ttu-id="aa17c-116">Alias, User</span><span class="sxs-lookup"><span data-stu-id="aa17c-116">Alias, User</span></span>     |<span data-ttu-id="aa17c-117">MailUser</span><span class="sxs-lookup"><span data-stu-id="aa17c-117">MailUser</span></span>         |
   > |<span data-ttu-id="aa17c-118">Alias, User</span><span class="sxs-lookup"><span data-stu-id="aa17c-118">Alias, User</span></span>     |<span data-ttu-id="aa17c-119">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="aa17c-119">User</span></span>         |

3. <span data-ttu-id="aa17c-120">Si plusieurs utilisateurs sont renvoyés, recherchez et corrigez l’objet en conflit.</span><span class="sxs-lookup"><span data-stu-id="aa17c-120">If multiple users are returned, locate and fix the conflicting object.</span></span>

## <a name="errorissue-search-fails-on-specific-locations"></a><span data-ttu-id="aa17c-121">Erreur/problème : la recherche échoue sur des emplacements spécifiques</span><span class="sxs-lookup"><span data-stu-id="aa17c-121">Error/issue: Search fails on specific locations</span></span>

<span data-ttu-id="aa17c-122">Une recherche de contenu ou eDiscovery peut produire l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="aa17c-122">An eDiscovery or content search may yield the following error:</span></span>
><span data-ttu-id="aa17c-123">Cette recherche s’est terminée avec les erreurs (#).</span><span class="sxs-lookup"><span data-stu-id="aa17c-123">This search completed with (#) errors.</span></span>  <span data-ttu-id="aa17c-124">Voulez-vous relancer la recherche sur les emplacements ayant échoué ?</span><span class="sxs-lookup"><span data-stu-id="aa17c-124">Would you like to retry the search on the failed locations?</span></span>

![Capture d’écran des erreurs d’emplacement spécifique à la recherche](../media/edisc-tshoot-specific-location-search-fails.png)

### <a name="resolution"></a><span data-ttu-id="aa17c-126">Résolution</span><span class="sxs-lookup"><span data-stu-id="aa17c-126">Resolution</span></span>

<span data-ttu-id="aa17c-127">Si vous recevez cette erreur, nous vous recommandons de vérifier les emplacements qui ont échoué dans la recherche, puis de réexécuter la recherche uniquement sur les emplacements ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="aa17c-127">If you receive this error, we recommend that you verify the locations that failed in the search  then rerun the search only on the failed locations.</span></span>

1. <span data-ttu-id="aa17c-128">Connectez-vous au [Centre de sécurité & de conformité PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell) , puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="aa17c-128">Connect to [Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell) and then run the following command:</span></span>

    ```powershell
    Get-ComplianceSearch <searchname> | FL 
    ```

2. <span data-ttu-id="aa17c-129">À partir de la sortie PowerShell, affichez les emplacements en échec dans le champ erreurs ou à partir des informations d’État dans l’erreur du résultat de la recherche.</span><span class="sxs-lookup"><span data-stu-id="aa17c-129">From the PowerShell output, view the failed locations in the errors field or from the status details in the error from the search output.</span></span>

3. <span data-ttu-id="aa17c-130">Renouvelez la recherche de découverte électronique aux emplacements ayant échoué uniquement.</span><span class="sxs-lookup"><span data-stu-id="aa17c-130">Retry the eDiscovery search on the failed locations only.</span></span>

4. <span data-ttu-id="aa17c-131">Si vous continuez à recevoir ces erreurs, reportez-vous à la rubrique [Retry failed locations](https://docs.microsoft.com/Office365/SecurityCompliance/retry-failed-content-search) pour obtenir d’autres étapes de dépannage.</span><span class="sxs-lookup"><span data-stu-id="aa17c-131">If you continue to receive these errors, see [Retry failed locations](https://docs.microsoft.com/Office365/SecurityCompliance/retry-failed-content-search) for more troubleshooting steps.</span></span>

## <a name="errorissue-file-not-found"></a><span data-ttu-id="aa17c-132">Erreur/problème : fichier introuvable</span><span class="sxs-lookup"><span data-stu-id="aa17c-132">Error/issue: File not found</span></span>

<span data-ttu-id="aa17c-133">Lors de l’exécution d’une recherche de découverte électronique incluant SharePoint Online et un lecteur pour les emplacements d’entreprise `File Not Found` , vous pouvez recevoir le message d’erreur même si le fichier se trouve sur le site.</span><span class="sxs-lookup"><span data-stu-id="aa17c-133">When running an eDiscovery search that includes SharePoint Online and One Drive For Business locations, you may receive the error `File Not Found` although the file is located on the site.</span></span> <span data-ttu-id="aa17c-134">Cette erreur se produira dans les avertissements et les erreurs d’exportation. csv ou éléments ignorés. csv.</span><span class="sxs-lookup"><span data-stu-id="aa17c-134">This error will be in the export warnings and errors.csv or skipped items.csv.</span></span> <span data-ttu-id="aa17c-135">Cela peut se produire si le fichier est introuvable sur le site ou si l’index est obsolète.</span><span class="sxs-lookup"><span data-stu-id="aa17c-135">This may occur if the file can't be found on the site or if the index is out of date.</span></span> <span data-ttu-id="aa17c-136">Voici le texte d’une erreur réelle (avec mise en relief ajoutée).</span><span class="sxs-lookup"><span data-stu-id="aa17c-136">Here's the text of an actual error (with emphasis added).</span></span>
  
> <span data-ttu-id="aa17c-137">28.06.2019 10:02:19_FailedToExportItem_Failed pour télécharger du contenu.</span><span class="sxs-lookup"><span data-stu-id="aa17c-137">28.06.2019 10:02:19_FailedToExportItem_Failed to download content.</span></span> <span data-ttu-id="aa17c-138">Informations de diagnostic supplémentaires : Microsoft. Office. Compliance. EDiscovery. ExportWorker. exceptions. ContentDownloadTemporaryFailure : échec de téléchargement à partir du contenu 6ea52149-91cd-4965-b5bb-82ca6a3ec9be de type document.</span><span class="sxs-lookup"><span data-stu-id="aa17c-138">Additional diagnostic info : Microsoft.Office.Compliance.EDiscovery.ExportWorker.Exceptions.ContentDownloadTemporaryFailure: Failed to download from content 6ea52149-91cd-4965-b5bb-82ca6a3ec9be of type Document.</span></span> <span data-ttu-id="aa17c-139">ID de corrélation : 3bd84722-937b-4c23-B61B-08d6fba9ec32.</span><span class="sxs-lookup"><span data-stu-id="aa17c-139">Correlation Id: 3bd84722-937b-4c23-b61b-08d6fba9ec32.</span></span> <span data-ttu-id="aa17c-140">ServerErrorCode :-2147024894---> Microsoft. SharePoint. client. ServerException : ***fichier introuvable***.</span><span class="sxs-lookup"><span data-stu-id="aa17c-140">ServerErrorCode: -2147024894 ---> Microsoft.SharePoint.Client.ServerException: ***File Not Found***.</span></span> <span data-ttu-id="aa17c-141">at Microsoft. SharePoint. client. ClientRequest. ProcessResponseStream (Stream responseStream) à Microsoft. SharePoint. client. ClientRequest. ProcessResponse ()---fin de la trace de la pile d’exception interne---</span><span class="sxs-lookup"><span data-stu-id="aa17c-141">at Microsoft.SharePoint.Client.ClientRequest.ProcessResponseStream(Stream responseStream) at Microsoft.SharePoint.Client.ClientRequest.ProcessResponse() --- End of inner exception stack trace ---</span></span>

### <a name="resolution"></a><span data-ttu-id="aa17c-142">Résolution</span><span class="sxs-lookup"><span data-stu-id="aa17c-142">Resolution</span></span>

1. <span data-ttu-id="aa17c-143">Vérifiez l’emplacement identifié dans la recherche pour vous assurer que l’emplacement du fichier est correct et ajouté aux emplacements de recherche.</span><span class="sxs-lookup"><span data-stu-id="aa17c-143">Check location identified in the search to ensure the that the location of the file is correct and added in the search locations.</span></span>

2. <span data-ttu-id="aa17c-144">Utilisez les procédures pour [demander manuellement l’analyse et la réindexation d’un site, d’une bibliothèque ou d’une liste](https://docs.microsoft.com/sharepoint/crawl-site-content) pour réindexer le site.</span><span class="sxs-lookup"><span data-stu-id="aa17c-144">Use the procedures at [Manually request crawling and re-indexing of a site, a library, or a list](https://docs.microsoft.com/sharepoint/crawl-site-content) to reindex the site.</span></span>

## <a name="errorissue-search-fails-because-recipient-is-not-found"></a><span data-ttu-id="aa17c-145">Erreur/problème : la recherche échoue, car le destinataire est introuvable</span><span class="sxs-lookup"><span data-stu-id="aa17c-145">Error/issue: Search fails because recipient is not found</span></span>

<span data-ttu-id="aa17c-146">Une recherche de découverte électronique échoue avec `recipient not found`l’erreur.</span><span class="sxs-lookup"><span data-stu-id="aa17c-146">An eDiscovery search fails with error the `recipient not found`.</span></span> <span data-ttu-id="aa17c-147">Cette erreur peut se produire si l’objet utilisateur est introuvable dans Exchange Online Protection (EOP) car l’objet n’a pas été synchronisé.</span><span class="sxs-lookup"><span data-stu-id="aa17c-147">This error may occur if the user object cannot be found in Exchange Online Protection (EOP) because the object has not synced.</span></span>

### <a name="resolution"></a><span data-ttu-id="aa17c-148">Résolution</span><span class="sxs-lookup"><span data-stu-id="aa17c-148">Resolution</span></span>

1. <span data-ttu-id="aa17c-149">Connectez-vous à [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="aa17c-149">Connect to [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="aa17c-150">Exécutez la commande suivante pour vérifier si l’utilisateur est synchronisé avec Exchange Online Protection :</span><span class="sxs-lookup"><span data-stu-id="aa17c-150">Run the following command to check if the user is synced to Exchange Online Protection:</span></span>

    ```powershell
    Get-Recipient <userId> | FL
    ```

3. <span data-ttu-id="aa17c-151">Il doit y avoir un objet utilisateur de messagerie pour la question de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aa17c-151">There should be a mail user object for the user question.</span></span> <span data-ttu-id="aa17c-152">Si aucune valeur n’est renvoyée, examinez l’objet User.</span><span class="sxs-lookup"><span data-stu-id="aa17c-152">If nothing is returned, investigate the user object.</span></span> <span data-ttu-id="aa17c-153">Contactez le support Microsoft si l’objet ne peut pas être synchronisé.</span><span class="sxs-lookup"><span data-stu-id="aa17c-153">Contact Microsoft Support if the object can't be synced.</span></span>

## <a name="errorissue-exporting-search-results-is-slow"></a><span data-ttu-id="aa17c-154">Erreur/problème : l’exportation des résultats de la recherche est lente</span><span class="sxs-lookup"><span data-stu-id="aa17c-154">Error/issue: Exporting search results is slow</span></span>

<span data-ttu-id="aa17c-155">Lors de l’exportation des résultats de recherche à partir de eDiscovery ou de la recherche de contenu dans le centre de sécurité et conformité, le téléchargement prend plus de temps que prévu.</span><span class="sxs-lookup"><span data-stu-id="aa17c-155">When exporting search results from eDiscovery or Content Search in the Security and Compliance center, the download takes longer than expected.</span></span>  <span data-ttu-id="aa17c-156">Vous pouvez vérifier la quantité de données à télécharger et augmenter éventuellement la vitesse d’exportation.</span><span class="sxs-lookup"><span data-stu-id="aa17c-156">You can check to see the amount of data to be download and possibly increase the export speed.</span></span>

### <a name="resolution"></a><span data-ttu-id="aa17c-157">Résolution</span><span class="sxs-lookup"><span data-stu-id="aa17c-157">Resolution</span></span>

1.    <span data-ttu-id="aa17c-158">Essayez d’utiliser les étapes indiquées dans l’article [augmenter les vitesses de téléchargement](https://docs.microsoft.com/office365/securitycompliance/increase-download-speeds-when-exporting-ediscovery-results).</span><span class="sxs-lookup"><span data-stu-id="aa17c-158">Try using the steps identified in the article [Increase Download Speeds](https://docs.microsoft.com/office365/securitycompliance/increase-download-speeds-when-exporting-ediscovery-results).</span></span>

2.    <span data-ttu-id="aa17c-159">Si vous rencontrez toujours des problèmes, connectez-vous à la [sécurité & Centre de conformité PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell) , puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="aa17c-159">If you still have issues, connect to [Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell) and then run the following command:</span></span>

    ```powershell
    Get-ComplianceSearch <searchname> | FL
    ```

4. <span data-ttu-id="aa17c-160">Recherchez la quantité de données à télécharger dans les paramètres SearchResults et SearchStatistics.</span><span class="sxs-lookup"><span data-stu-id="aa17c-160">Find the amount of data to be downloaded in the SearchResults and SearchStatistics parameters.</span></span>

5. <span data-ttu-id="aa17c-161">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="aa17c-161">Run the following command:</span></span>

   ```powershell
   Get-ComplianceSearchAction | FL
   ```

6. <span data-ttu-id="aa17c-162">Dans le champ résultats, recherchez les données qui ont été exportées et affichez les erreurs rencontrées.</span><span class="sxs-lookup"><span data-stu-id="aa17c-162">In the results field, find the data that has been exported and view any errors encountered.</span></span>

7. <span data-ttu-id="aa17c-163">Vérifiez le fichier trace. log situé dans le répertoire dans lequel vous avez exporté le contenu pour détecter d’éventuelles erreurs.</span><span class="sxs-lookup"><span data-stu-id="aa17c-163">Check the trace.log file located in the directory that you exported the content to for any errors.</span></span>

## <a name="errorissue-internal-server-error-500-occurred"></a><span data-ttu-id="aa17c-164">Erreur/problème : « erreur interne du serveur (500) » s’est produite»</span><span class="sxs-lookup"><span data-stu-id="aa17c-164">Error/issue: "Internal server error (500) occurred"</span></span>

<span data-ttu-id="aa17c-165">Lors de l’exécution d’une recherche de découverte électronique, si la recherche continue de se produire avec une erreur semblable à « erreur interne du serveur (500) », vous pouvez être amené à relancer la recherche uniquement sur des emplacements de boîte aux lettres spécifiques.</span><span class="sxs-lookup"><span data-stu-id="aa17c-165">When running an eDiscovery search, if the search continually fails with error similar to "Internal server error (500) occurred", you may need rerun the search only on specific mailbox locations.</span></span>

![Capture d’écran de l’erreur de serveur interne 500](../media/edisc-tshoot-error-500.png)

### <a name="resolution"></a><span data-ttu-id="aa17c-167">Résolution</span><span class="sxs-lookup"><span data-stu-id="aa17c-167">Resolution</span></span>

1. <span data-ttu-id="aa17c-168">Fractionnez la recherche en petites recherches et réexécutez la recherche.</span><span class="sxs-lookup"><span data-stu-id="aa17c-168">Break the search into smaller searches and run the search again.</span></span>  <span data-ttu-id="aa17c-169">Essayez d’utiliser une plage de dates plus petite ou limitez le nombre d’emplacements recherchés.</span><span class="sxs-lookup"><span data-stu-id="aa17c-169">Try using a smaller date range or limit the number of locations being searched.</span></span>

2. <span data-ttu-id="aa17c-170">Connectez-vous au [Centre de sécurité & de conformité PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell) , puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="aa17c-170">Connect to [Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell) and then run the following command:</span></span>

    ```powershell Set-CaseHoldPolicy <policyname> -RetryDistribution
    Get-ComplianceSearch <searchname> | FL
    ```

3. <span data-ttu-id="aa17c-171">Examinez la sortie pour les résultats et les erreurs.</span><span class="sxs-lookup"><span data-stu-id="aa17c-171">Examine the output for results and errors.</span></span>

4. <span data-ttu-id="aa17c-172">Examinez le fichier trace. log.</span><span class="sxs-lookup"><span data-stu-id="aa17c-172">Examine the trace.log file.</span></span> <span data-ttu-id="aa17c-173">Il se trouve dans le dossier dans lequel vous avez exporté les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="aa17c-173">It's located  in the same folder that you exported the search results to.</span></span>

5. <span data-ttu-id="aa17c-174">Contactez le support technique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aa17c-174">Contact Microsoft Support.</span></span>

## <a name="errorissue-holds-dont-sync"></a><span data-ttu-id="aa17c-175">Erreur/problème : conservation ne pas synchroniser</span><span class="sxs-lookup"><span data-stu-id="aa17c-175">Error/issue: Holds don't sync</span></span>

<span data-ttu-id="aa17c-176">erreur de distribution de la stratégie de conservation de cas eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="aa17c-176">eDiscovery Case Hold Policy Sync Distribution error.</span></span> <span data-ttu-id="aa17c-177">L’erreur indique :</span><span class="sxs-lookup"><span data-stu-id="aa17c-177">The error reads:</span></span>

> <span data-ttu-id="aa17c-178">«Ressources : le déploiement de la stratégie prend plus de temps que prévu.</span><span class="sxs-lookup"><span data-stu-id="aa17c-178">"Resources: It's taking longer than expected to deploy the policy.</span></span> <span data-ttu-id="aa17c-179">La mise à jour de l’état final du déploiement peut prendre 2 heures supplémentaires, donc revenez en quelques heures.</span><span class="sxs-lookup"><span data-stu-id="aa17c-179">It might take an additional 2 hours to update the final deployment status, so check back in a couple hours."</span></span>

### <a name="resolution"></a><span data-ttu-id="aa17c-180">Résolution</span><span class="sxs-lookup"><span data-stu-id="aa17c-180">Resolution</span></span>

1.    <span data-ttu-id="aa17c-181">Connectez-vous à la [sécurité & Centre de conformité PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell) , puis exécutez la commande suivante pour une conservation de cas eDiscovery :</span><span class="sxs-lookup"><span data-stu-id="aa17c-181">Connect to [Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell) and then run the following command for an eDiscovery case hold:</span></span>

    ```powershell
    Get-CaseHoldPolicy <policyname> - DistributionDetail | FL
    ```

    <span data-ttu-id="aa17c-182">Pour une stratégie de rétention, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="aa17c-182">For a retention policy, run the following command:</span></span>

    ```powershell
    Get-RetentionCompliancePolicy <policyname> - DistributionDetail | FL
    ```

2. <span data-ttu-id="aa17c-183">Examinez la valeur du paramètre DistributionDetail pour rechercher les erreurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="aa17c-183">Examine the value in the DistributionDetail parameter for errors like the following:</span></span>
 
   > <span data-ttu-id="aa17c-184">Erreur : ressources : le déploiement de la stratégie prend plus de temps que prévu.</span><span class="sxs-lookup"><span data-stu-id="aa17c-184">Error: Resources: It's taking longer than expected to deploy the policy.</span></span> <span data-ttu-id="aa17c-185">La mise à jour de l’état final du déploiement peut prendre 2 heures supplémentaires, donc revenez en quelques heures.</span><span class="sxs-lookup"><span data-stu-id="aa17c-185">It might take an additional 2 hours to update the final deployment status, so check back in a couple hours."</span></span> 
   
3. <span data-ttu-id="aa17c-186">Essayez d’exécuter le paramètre RetryDistribution sur la stratégie en question :</span><span class="sxs-lookup"><span data-stu-id="aa17c-186">Try running the RetryDistribution parameter on the policy in question:</span></span>
   
    
    <span data-ttu-id="aa17c-187">Pour les conservations de cas eDiscovery :</span><span class="sxs-lookup"><span data-stu-id="aa17c-187">For eDiscovery case holds:</span></span>

    ```powershell
    Set-CaseHoldPolicy <policyname> -RetryDistribution
    ```

    <span data-ttu-id="aa17c-188">Pour les stratégies de rétention :</span><span class="sxs-lookup"><span data-stu-id="aa17c-188">For retention policies:</span></span>

    ```powershell
    Set-RetentionCompliancePolicy <policyname> -RetryDistribution
    ``` 

4. <span data-ttu-id="aa17c-189">Contactez le support technique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aa17c-189">Contact Microsoft Support.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa17c-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa17c-190">See Also</span></span>

- [<span data-ttu-id="aa17c-191">Conseils pour éviter les erreurs d’emplacement de contenu</span><span class="sxs-lookup"><span data-stu-id="aa17c-191">Tips to avoid content location errors</span></span>](retry-failed-content-search.md#tips-to-avoid-content-location-errors)
