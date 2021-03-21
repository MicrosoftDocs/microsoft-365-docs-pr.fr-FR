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
description: Découvrez les étapes de résolution des problèmes de base que vous pouvez suivre pour résoudre les problèmes courants dans la découverte électronique Office 365.
siblings_only: true
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: a867ed2e55c73fe4bbd890273d78cf57f4bfbd2c
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50926544"
---
# <a name="investigate-troubleshoot-and-resolve-common-ediscovery-issues"></a><span data-ttu-id="44476-103">Examiner, résoudre et résoudre les problèmes eDiscovery courants</span><span class="sxs-lookup"><span data-stu-id="44476-103">Investigate, troubleshoot, and resolve common eDiscovery issues</span></span>

<span data-ttu-id="44476-104">Cette rubrique traite des étapes de dépannage de base que vous pouvez effectuer pour identifier et résoudre les problèmes que vous pouvez rencontrer lors d’une recherche de découverte électronique ou ailleurs dans le processus eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="44476-104">This topic covers basic troubleshooting steps you can take to identify and resolve issues you may encounter during an eDiscovery search or elsewhere in the eDiscovery process.</span></span> <span data-ttu-id="44476-105">La résolution de certains de ces scénarios nécessite l’aide du Support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="44476-105">Resolving some of these scenarios requires help from Microsoft Support.</span></span> <span data-ttu-id="44476-106">Les informations sur le moment où contacter le Support Microsoft sont incluses dans les étapes de résolution.</span><span class="sxs-lookup"><span data-stu-id="44476-106">Information on when to contact Microsoft Support is included in the resolution steps.</span></span>

## <a name="errorissue-ambiguous-location"></a><span data-ttu-id="44476-107">Erreur/problème : emplacement ambigu</span><span class="sxs-lookup"><span data-stu-id="44476-107">Error/issue: Ambiguous location</span></span>

<span data-ttu-id="44476-108">Si vous essayez d’ajouter l’emplacement de boîte aux lettres de l’utilisateur à rechercher et qu’il existe des objets en double ou en conflit avec le même userID dans l’annuaire Exchange Online Protection (EOP), vous recevez cette erreur : `The compliance search contains the following invalid location(s):useralias@contoso.com. The location "useralias@contoso.com" is ambiguous`</span><span class="sxs-lookup"><span data-stu-id="44476-108">If you try to add user's mailbox location to search and there are duplicate or conflicting objects with the same userID in the Exchange Online Protection (EOP) directory, you receive this error: `The compliance search contains the following invalid location(s):useralias@contoso.com. The location "useralias@contoso.com" is ambiguous`.</span></span>

### <a name="resolution"></a><span data-ttu-id="44476-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="44476-109">Resolution</span></span>

<span data-ttu-id="44476-110">Recherchez des utilisateurs en double ou une liste de distribution avec le même ID d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="44476-110">Check for duplicate users or distribution list with the same user ID.</span></span>

1. <span data-ttu-id="44476-111">Connectez-vous [au Centre de sécurité & conformité PowerShell.](/powershell/exchange/connect-to-scc-powershell)</span><span class="sxs-lookup"><span data-stu-id="44476-111">Connect to [Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell).</span></span>

2. <span data-ttu-id="44476-112">Exécutez la commande suivante pour récupérer toutes les instances du nom d’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="44476-112">Run the following command to retrieve all instances of the username:</span></span>

    ```powershell
    Get-Recipient <username>
    ```

   <span data-ttu-id="44476-113">La sortie de « useralias@contoso.com » serait similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="44476-113">The output for 'useralias@contoso.com' would be similar to the following:</span></span>

   > 
   > |<span data-ttu-id="44476-114">Nom</span><span class="sxs-lookup"><span data-stu-id="44476-114">Name</span></span>|<span data-ttu-id="44476-115">RecipientType</span><span class="sxs-lookup"><span data-stu-id="44476-115">RecipientType</span></span>|
   > |---|---|
   > |<span data-ttu-id="44476-116">Alias, Utilisateur</span><span class="sxs-lookup"><span data-stu-id="44476-116">Alias, User</span></span>|<span data-ttu-id="44476-117">MailUser</span><span class="sxs-lookup"><span data-stu-id="44476-117">MailUser</span></span>|
   > |<span data-ttu-id="44476-118">Alias, Utilisateur</span><span class="sxs-lookup"><span data-stu-id="44476-118">Alias, User</span></span>|<span data-ttu-id="44476-119">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="44476-119">User</span></span>|

3. <span data-ttu-id="44476-120">Si plusieurs utilisateurs sont renvoyés, recherchez et corrigez l’objet en conflit.</span><span class="sxs-lookup"><span data-stu-id="44476-120">If multiple users are returned, locate and fix the conflicting object.</span></span>

## <a name="errorissue-search-fails-on-specific-locations"></a><span data-ttu-id="44476-121">Erreur/problème : la recherche échoue à des emplacements spécifiques</span><span class="sxs-lookup"><span data-stu-id="44476-121">Error/issue: Search fails on specific locations</span></span>

<span data-ttu-id="44476-122">Une recherche eDiscovery ou de contenu peut produire l’erreur suivante : `This search completed with (#) errors.  Would you like to retry the search on the failed locations?`</span><span class="sxs-lookup"><span data-stu-id="44476-122">An eDiscovery or content search may yield the following error: `This search completed with (#) errors.  Would you like to retry the search on the failed locations?`</span></span>

![Capture d’écran d’erreur d’erreur d’un emplacement spécifique à la recherche](../media/edisc-tshoot-specific-location-search-fails.png)

### <a name="resolution"></a><span data-ttu-id="44476-124">Résolution</span><span class="sxs-lookup"><span data-stu-id="44476-124">Resolution</span></span>

<span data-ttu-id="44476-125">Si vous recevez cette erreur, nous vous recommandons de vérifier les emplacements qui ont échoué dans la recherche, puis de réexécuter la recherche uniquement sur les emplacements qui ont échoué.</span><span class="sxs-lookup"><span data-stu-id="44476-125">If you receive this error, we recommend that you verify the locations that failed in the search  then rerun the search only on the failed locations.</span></span>

1. <span data-ttu-id="44476-126">Connectez-vous au Centre de & de sécurité [PowerShell,](/powershell/exchange/connect-to-scc-powershell) puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="44476-126">Connect to [Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell) and then run the following command:</span></span>

   ```powershell
   Get-ComplianceSearch <searchname> | FL
   ```

2. <span data-ttu-id="44476-127">À partir de la sortie PowerShell, affichez les emplacements qui ont échoué dans le champ erreurs ou à partir des détails d’état dans l’erreur à partir de la sortie de recherche.</span><span class="sxs-lookup"><span data-stu-id="44476-127">From the PowerShell output, view the failed locations in the errors field or from the status details in the error from the search output.</span></span>

3. <span data-ttu-id="44476-128">Réessayez la recherche eDiscovery sur les emplacements qui ont échoué uniquement.</span><span class="sxs-lookup"><span data-stu-id="44476-128">Retry the eDiscovery search on the failed locations only.</span></span>

4. <span data-ttu-id="44476-129">Si vous continuez à recevoir ces erreurs, consultez Réessayer les emplacements d’échec [pour](/Office365/SecurityCompliance/retry-failed-content-search) plus d’étapes de résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="44476-129">If you continue to receive these errors, see [Retry failed locations](/Office365/SecurityCompliance/retry-failed-content-search) for more troubleshooting steps.</span></span>

## <a name="errorissue-file-not-found"></a><span data-ttu-id="44476-130">Erreur/problème : fichier in trouvé</span><span class="sxs-lookup"><span data-stu-id="44476-130">Error/issue: File not found</span></span>

<span data-ttu-id="44476-131">Lors de l’exécution d’une recherche de découverte électronique qui inclut des emplacements SharePoint Online et One Drive For Business, vous pouvez recevoir l’erreur même si le fichier se trouve `File Not Found` sur le site.</span><span class="sxs-lookup"><span data-stu-id="44476-131">When running an eDiscovery search that includes SharePoint Online and One Drive For Business locations, you may receive the error `File Not Found` although the file is located on the site.</span></span> <span data-ttu-id="44476-132">Cette erreur sera dans les avertissements d’exportation et errors.csv ou ignorée items.csv.</span><span class="sxs-lookup"><span data-stu-id="44476-132">This error will be in the export warnings and errors.csv or skipped items.csv.</span></span> <span data-ttu-id="44476-133">Cela peut se produire si le fichier n’est pas trouvé sur le site ou si l’index n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="44476-133">This may occur if the file can't be found on the site or if the index is out of date.</span></span> <span data-ttu-id="44476-134">Voici le texte d’une erreur réelle (avec une accentuation ajoutée).</span><span class="sxs-lookup"><span data-stu-id="44476-134">Here's the text of an actual error (with emphasis added).</span></span>

> <span data-ttu-id="44476-135">28.06.2019 10:02:19_FailedToExportItem_Failed télécharger du contenu.</span><span class="sxs-lookup"><span data-stu-id="44476-135">28.06.2019 10:02:19_FailedToExportItem_Failed to download content.</span></span> <span data-ttu-id="44476-136">Informations de diagnostic supplémentaires : Microsoft.Office.Compliance.EDiscovery.ExportWorker.Exceptions.ContentDownloadTemporaryFailure: Failed to download from content 6ea52149-91cd-4965-b5bb-82ca6a3ec9be of type Document.</span><span class="sxs-lookup"><span data-stu-id="44476-136">Additional diagnostic info : Microsoft.Office.Compliance.EDiscovery.ExportWorker.Exceptions.ContentDownloadTemporaryFailure: Failed to download from content 6ea52149-91cd-4965-b5bb-82ca6a3ec9be of type Document.</span></span> <span data-ttu-id="44476-137">ID de corrélation : 3bd84722-937b-4c23-b61b-08d6fba9ec32.</span><span class="sxs-lookup"><span data-stu-id="44476-137">Correlation Id: 3bd84722-937b-4c23-b61b-08d6fba9ec32.</span></span> <span data-ttu-id="44476-138">ServerErrorCode: -2147024894 ---> Microsoft.SharePoint.Client.ServerException: ***File Not Found***.</span><span class="sxs-lookup"><span data-stu-id="44476-138">ServerErrorCode: -2147024894 ---> Microsoft.SharePoint.Client.ServerException: ***File Not Found***.</span></span> <span data-ttu-id="44476-139">at Microsoft.SharePoint.Client.ClientRequest.ProcessResponseStream(Stream responseStream) at Microsoft.SharePoint.Client.ClientRequest.ProcessResponse() --- End of inner exception stack trace ---</span><span class="sxs-lookup"><span data-stu-id="44476-139">at Microsoft.SharePoint.Client.ClientRequest.ProcessResponseStream(Stream responseStream) at Microsoft.SharePoint.Client.ClientRequest.ProcessResponse() --- End of inner exception stack trace ---</span></span>

### <a name="resolution"></a><span data-ttu-id="44476-140">Résolution</span><span class="sxs-lookup"><span data-stu-id="44476-140">Resolution</span></span>

1. <span data-ttu-id="44476-141">Vérifiez l’emplacement identifié dans la recherche pour vous assurer que l’emplacement du fichier est correct et ajouté aux emplacements de recherche.</span><span class="sxs-lookup"><span data-stu-id="44476-141">Check location identified in the search to ensure the that the location of the file is correct and added in the search locations.</span></span>

2. <span data-ttu-id="44476-142">Utilisez les procédures de demande manuelle d’analyse et [de réindexation](/sharepoint/crawl-site-content) d’un site, d’une bibliothèque ou d’une liste pour réindexer le site.</span><span class="sxs-lookup"><span data-stu-id="44476-142">Use the procedures at [Manually request crawling and re-indexing of a site, a library, or a list](/sharepoint/crawl-site-content) to reindex the site.</span></span>

## <a name="errorissue-search-fails-because-recipient-is-not-found"></a><span data-ttu-id="44476-143">Erreur/problème : la recherche échoue car le destinataire est in trouvé</span><span class="sxs-lookup"><span data-stu-id="44476-143">Error/issue: Search fails because recipient is not found</span></span>

<span data-ttu-id="44476-144">Une recherche eDiscovery échoue avec l’erreur « `recipient not found` .</span><span class="sxs-lookup"><span data-stu-id="44476-144">An eDiscovery search fails with error the `recipient not found`.</span></span> <span data-ttu-id="44476-145">Cette erreur peut se produire si l’objet utilisateur est in trouver dans Exchange Online Protection (EOP) car l’objet n’a pas été synchronisé.</span><span class="sxs-lookup"><span data-stu-id="44476-145">This error may occur if the user object cannot be found in Exchange Online Protection (EOP) because the object has not synced.</span></span>

### <a name="resolution"></a><span data-ttu-id="44476-146">Résolution</span><span class="sxs-lookup"><span data-stu-id="44476-146">Resolution</span></span>

1. <span data-ttu-id="44476-147">Connectez-vous à [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="44476-147">Connect to [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="44476-148">Exécutez la commande suivante pour vérifier si l’utilisateur est synchronisé avec Exchange Online Protection :</span><span class="sxs-lookup"><span data-stu-id="44476-148">Run the following command to check if the user is synced to Exchange Online Protection:</span></span>

   ```powershell
   Get-Recipient <userId> | FL
   ```

3. <span data-ttu-id="44476-149">Il doit y avoir un objet utilisateur de messagerie pour la question de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="44476-149">There should be a mail user object for the user question.</span></span> <span data-ttu-id="44476-150">Si rien n’est renvoyé, examinez l’objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="44476-150">If nothing is returned, investigate the user object.</span></span> <span data-ttu-id="44476-151">Contactez le Support Microsoft si l’objet ne peut pas être synchronisé.</span><span class="sxs-lookup"><span data-stu-id="44476-151">Contact Microsoft Support if the object can't be synced.</span></span>

## <a name="errorissue-exporting-search-results-is-slow"></a><span data-ttu-id="44476-152">Erreur/problème : l’exportation des résultats de recherche est lente</span><span class="sxs-lookup"><span data-stu-id="44476-152">Error/issue: Exporting search results is slow</span></span>

<span data-ttu-id="44476-153">Lors de l’exportation des résultats de recherche à partir d’eDiscovery ou de recherche de contenu dans le Centre de sécurité et conformité, le téléchargement prend plus de temps que prévu.</span><span class="sxs-lookup"><span data-stu-id="44476-153">When exporting search results from eDiscovery or Content Search in the Security and Compliance center, the download takes longer than expected.</span></span>  <span data-ttu-id="44476-154">Vous pouvez vérifier la quantité de données à télécharger et éventuellement augmenter la vitesse d’exportation.</span><span class="sxs-lookup"><span data-stu-id="44476-154">You can check to see the amount of data to be download and possibly increase the export speed.</span></span>

### <a name="resolution"></a><span data-ttu-id="44476-155">Résolution</span><span class="sxs-lookup"><span data-stu-id="44476-155">Resolution</span></span>

1. <span data-ttu-id="44476-156">Connectez-vous au Centre de & de sécurité [PowerShell,](/powershell/exchange/connect-to-scc-powershell) puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="44476-156">Connect to [Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell) and then run the following command:</span></span>

   ```powershell
   Get-ComplianceSearch <searchname> | FL
   ```

2. <span data-ttu-id="44476-157">Recherchez la quantité de données à télécharger dans les paramètres SearchResults et SearchStatistics.</span><span class="sxs-lookup"><span data-stu-id="44476-157">Find the amount of data to be downloaded in the SearchResults and SearchStatistics parameters.</span></span>

3. <span data-ttu-id="44476-158">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="44476-158">Run the following command:</span></span>

   ```powershell
   Get-ComplianceSearchAction | FL
   ```

4. <span data-ttu-id="44476-159">Dans le champ résultats, recherchez les données qui ont été exportées et affichez les erreurs rencontrées.</span><span class="sxs-lookup"><span data-stu-id="44476-159">In the results field, find the data that has been exported and view any errors encountered.</span></span>

5. <span data-ttu-id="44476-160">Recherchez les erreurs éventuelles dans le fichier trace.log situé dans le répertoire vers qui vous avez exporté le contenu.</span><span class="sxs-lookup"><span data-stu-id="44476-160">Check the trace.log file located in the directory that you exported the content to for any errors.</span></span>

6. <span data-ttu-id="44476-161">Si vous avez encore des problèmes, envisagez de diviser les recherches qui retournent un grand ensemble de résultats en recherches plus petites.</span><span class="sxs-lookup"><span data-stu-id="44476-161">If you still have issues, consider dividing searches that return a large set of results into smaller searches.</span></span> <span data-ttu-id="44476-162">Par exemple, vous pouvez utiliser des plages de dates dans les requêtes de recherche pour renvoyer un ensemble de résultats plus petit qui peut être téléchargé plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="44476-162">For example, you can use date ranges in search queries to return a smaller set of results that can be downloaded faster.</span></span>

## <a name="errorissue-internal-server-error-500-occurred"></a><span data-ttu-id="44476-163">Erreur/problème : « Une erreur de serveur interne (500) s’est produite »</span><span class="sxs-lookup"><span data-stu-id="44476-163">Error/issue: "Internal server error (500) occurred"</span></span>

<span data-ttu-id="44476-164">Lors de l’exécution d’une recherche de découverte électronique, si la recherche échoue continuellement avec une erreur semblable à « Erreur interne du serveur (500) s’est produite », vous devrez peut-être réexécuter la recherche uniquement sur des emplacements de boîtes aux lettres spécifiques.</span><span class="sxs-lookup"><span data-stu-id="44476-164">When running an eDiscovery search, if the search continually fails with error similar to "Internal server error (500) occurred", you may need rerun the search only on specific mailbox locations.</span></span>

![Capture d’écran de l’erreur du serveur interne 500](../media/edisc-tshoot-error-500.png)

### <a name="resolution"></a><span data-ttu-id="44476-166">Résolution</span><span class="sxs-lookup"><span data-stu-id="44476-166">Resolution</span></span>

1. <span data-ttu-id="44476-167">Décomposez la recherche en recherches plus petites et exécutez à nouveau la recherche.</span><span class="sxs-lookup"><span data-stu-id="44476-167">Break the search into smaller searches and run the search again.</span></span>  <span data-ttu-id="44476-168">Essayez d’utiliser une plage de dates plus petite ou limitez le nombre d’emplacements recherchés.</span><span class="sxs-lookup"><span data-stu-id="44476-168">Try using a smaller date range or limit the number of locations being searched.</span></span>

2. <span data-ttu-id="44476-169">Connectez-vous au Centre de & de sécurité [PowerShell,](/powershell/exchange/connect-to-scc-powershell) puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="44476-169">Connect to [Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell) and then run the following command:</span></span>

   ```powershell Set-CaseHoldPolicy <policyname> -RetryDistribution
   Get-ComplianceSearch <searchname> | FL
   ```

3. <span data-ttu-id="44476-170">Examinez la sortie pour les résultats et les erreurs.</span><span class="sxs-lookup"><span data-stu-id="44476-170">Examine the output for results and errors.</span></span>

4. <span data-ttu-id="44476-171">Examinez le fichier trace.log.</span><span class="sxs-lookup"><span data-stu-id="44476-171">Examine the trace.log file.</span></span> <span data-ttu-id="44476-172">Il se trouve dans le même dossier que celui dans quoi vous avez exporté les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="44476-172">It's located  in the same folder that you exported the search results to.</span></span>

5. <span data-ttu-id="44476-173">Contactez le support technique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="44476-173">Contact Microsoft Support.</span></span>

## <a name="errorissue-holds-dont-sync"></a><span data-ttu-id="44476-174">Erreur/problème : les holds ne sont pas synchronisés</span><span class="sxs-lookup"><span data-stu-id="44476-174">Error/issue: Holds don't sync</span></span>

<span data-ttu-id="44476-175">Erreur de distribution de synchronisation de stratégie de prise en main de cas eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="44476-175">eDiscovery Case Hold Policy Sync Distribution error.</span></span> <span data-ttu-id="44476-176">L’erreur se lit comme ci-après :</span><span class="sxs-lookup"><span data-stu-id="44476-176">The error reads:</span></span>

> <span data-ttu-id="44476-177">« Ressources : le déploiement de la stratégie prend plus de temps que prévu.</span><span class="sxs-lookup"><span data-stu-id="44476-177">"Resources: It's taking longer than expected to deploy the policy.</span></span> <span data-ttu-id="44476-178">La mise à jour de l’état de déploiement final peut prendre 2 heures supplémentaires, donc vérifiez-la dans quelques heures. »</span><span class="sxs-lookup"><span data-stu-id="44476-178">It might take an additional 2 hours to update the final deployment status, so check back in a couple hours."</span></span>

### <a name="resolution"></a><span data-ttu-id="44476-179">Résolution</span><span class="sxs-lookup"><span data-stu-id="44476-179">Resolution</span></span>

1. <span data-ttu-id="44476-180">[Connectez-vous au Centre de sécurité & conformité PowerShell,](/powershell/exchange/connect-to-scc-powershell) puis exécutez la commande suivante pour une mise en attente de cas eDiscovery :</span><span class="sxs-lookup"><span data-stu-id="44476-180">Connect to [Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell) and then run the following command for an eDiscovery case hold:</span></span>

   ```powershell
   Get-CaseHoldPolicy <policyname> - DistributionDetail | FL
   ```

    <span data-ttu-id="44476-181">Pour une stratégie de rétention, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="44476-181">For a retention policy, run the following command:</span></span>

   ```powershell
   Get-RetentionCompliancePolicy <policyname> - DistributionDetail | FL
   ```

2. <span data-ttu-id="44476-182">Examinez la valeur dans le paramètre DistributionDetail pour les erreurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="44476-182">Examine the value in the DistributionDetail parameter for errors like the following:</span></span>

   > <span data-ttu-id="44476-183">Erreur : Ressources : le déploiement de la stratégie prend plus de temps que prévu.</span><span class="sxs-lookup"><span data-stu-id="44476-183">Error: Resources: It's taking longer than expected to deploy the policy.</span></span> <span data-ttu-id="44476-184">La mise à jour de l’état de déploiement final peut prendre 2 heures supplémentaires, donc vérifiez-la dans quelques heures. »</span><span class="sxs-lookup"><span data-stu-id="44476-184">It might take an additional 2 hours to update the final deployment status, so check back in a couple hours."</span></span>

3. <span data-ttu-id="44476-185">Essayez d’exécutez le paramètre RetryDistribution sur la stratégie en question :</span><span class="sxs-lookup"><span data-stu-id="44476-185">Try running the RetryDistribution parameter on the policy in question:</span></span>

   <span data-ttu-id="44476-186">Pour les cas eDiscovery :</span><span class="sxs-lookup"><span data-stu-id="44476-186">For eDiscovery case holds:</span></span>

   ```powershell
   Set-CaseHoldPolicy <policyname> -RetryDistribution
   ```

   <span data-ttu-id="44476-187">Pour les stratégies de rétention :</span><span class="sxs-lookup"><span data-stu-id="44476-187">For retention policies:</span></span>

   ```powershell
   Set-RetentionCompliancePolicy <policyname> -RetryDistribution
   ```

4. <span data-ttu-id="44476-188">Contactez le support technique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="44476-188">Contact Microsoft Support.</span></span>

## <a name="error-the-condition-specified-using-http-conditional-headers-is-not-met"></a><span data-ttu-id="44476-189">Erreur : « La condition spécifiée à l’aide d’en-têtes conditionnels HTTP n’est pas remplie »</span><span class="sxs-lookup"><span data-stu-id="44476-189">Error: "The condition specified using HTTP conditional header(s) is not met"</span></span>

<span data-ttu-id="44476-190">Lorsque vous téléchargez des résultats de recherche à l’aide de l’outil d’exportation eDiscovery, il est possible que vous receviez l’erreur suivante : Il s’agit d’une erreur temporaire, qui se produit généralement dans l’emplacement de stockage `System.Net.WebException: The remote server returned an error: (412) The condition specified using HTTP conditional header(s) is not met.` Azure.</span><span class="sxs-lookup"><span data-stu-id="44476-190">When downloading search results using the eDiscovery Export Tool, it's possible you might receive the following error: `System.Net.WebException: The remote server returned an error: (412) The condition specified using HTTP conditional header(s) is not met.` This is transient error, which typically occurs in the Azure Storage location.</span></span>

### <a name="resolution"></a><span data-ttu-id="44476-191">Résolution</span><span class="sxs-lookup"><span data-stu-id="44476-191">Resolution</span></span>

<span data-ttu-id="44476-192">Pour résoudre ce problème, réessayez de [télécharger](export-search-results.md#step-2-download-the-search-results)les résultats de la recherche, ce qui redémarrera l’outil d’exportation eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="44476-192">To resolve this issue, retry [downloading the search results](export-search-results.md#step-2-download-the-search-results), which will restart the eDiscovery Export Tool.</span></span>

## <a name="errorissue-downloaded-export-shows-no-results"></a><span data-ttu-id="44476-193">Erreur/problème : l’exportation téléchargée n’affiche aucun résultat</span><span class="sxs-lookup"><span data-stu-id="44476-193">Error/issue: Downloaded export shows no results</span></span>

<span data-ttu-id="44476-194">Une fois l’exportation réussie, le téléchargement terminé via l’outil d’exportation affiche zéro fichier dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="44476-194">After a successful export, the completed download via the export tool shows zero files in the results.</span></span>

### <a name="resolution"></a><span data-ttu-id="44476-195">Résolution</span><span class="sxs-lookup"><span data-stu-id="44476-195">Resolution</span></span>

<span data-ttu-id="44476-196">Il s’agit d’un problème côté client et, pour y remédier, essayez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="44476-196">This is a client-side issue and in order to remediate it, please attempt the following steps:</span></span>

1. <span data-ttu-id="44476-197">Essayez d’utiliser un autre client/ordinateur pour télécharger.</span><span class="sxs-lookup"><span data-stu-id="44476-197">Try using another client/machine to download.</span></span>

2. <span data-ttu-id="44476-198">Veillez à effectuer le téléchargement sur un lecteur local.</span><span class="sxs-lookup"><span data-stu-id="44476-198">Make sure to download to a local drive.</span></span>

3. <span data-ttu-id="44476-199">Assurez-vous que le scanneur antivirus n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="44476-199">Make sure the virus scanner is not running.</span></span>

4. <span data-ttu-id="44476-200">Assurez-vous qu’aucune autre exportation n’est téléchargée vers le même dossier ou n’importe quel dossier parent.</span><span class="sxs-lookup"><span data-stu-id="44476-200">Make sure that no other export is downloading to the same folder or any parent folder.</span></span>

5. <span data-ttu-id="44476-201">Si les étapes précédentes ne fonctionnent pas, désactivez la fermeture à la fermeture de la fermeture et la déplication.</span><span class="sxs-lookup"><span data-stu-id="44476-201">If the previous steps did not work, disable zipping and de-duplication.</span></span>

6. <span data-ttu-id="44476-202">Si cela fonctionne, le problème est dû à un scanneur antivirus local ou à un problème de disque.</span><span class="sxs-lookup"><span data-stu-id="44476-202">If this works then the issue is due to a local virus scanner or a disk issue.</span></span>