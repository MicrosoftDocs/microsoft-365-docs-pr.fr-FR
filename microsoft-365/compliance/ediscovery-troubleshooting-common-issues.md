---
title: Problèmes courants de découverte électronique Troublshooting
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
description: Examinez, dépannez et résolvez les problèmes courants dans Office 365 eDiscovery.
siblings_only: true
ms.openlocfilehash: db355067aa4e3fc41541e6414b59c92aaac1b5b3
ms.sourcegitcommit: 75c8f89049081f08852699c8d51c3a07b12165da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37207290"
---
# <a name="investigate-troubleshoot-and-resolve-common-ediscovery-issues"></a><span data-ttu-id="5d306-103">Examiner, dépanner et résoudre les problèmes eDiscovery courants</span><span class="sxs-lookup"><span data-stu-id="5d306-103">Investigate, troubleshoot and resolve common eDiscovery issues</span></span>

<span data-ttu-id="5d306-104">Cette rubrique décrit les étapes de résolution des problèmes que vous pouvez effectuer pour identifier et résoudre les problèmes que vous pouvez rencontrer lors d’une recherche de découverte électronique ou ailleurs dans le processus de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="5d306-104">This topic covers basic troubleshooting steps you can take to identify and resolve issues you may encounter during an eDiscovery search or elsewhere in the eDiscovery process.</span></span> <span data-ttu-id="5d306-105">La résolution de certains de ces scénarios nécessite l’aide des services de support technique (CSS).</span><span class="sxs-lookup"><span data-stu-id="5d306-105">Resolving some of these scenarios requires help from Customer Support Services (CSS).</span></span> <span data-ttu-id="5d306-106">Les informations sur le moment de contacter CSS sont incluses dans la procédure de résolution.</span><span class="sxs-lookup"><span data-stu-id="5d306-106">Information on when to contact CSS is included in the resolution steps.</span></span>

## <a name="errorissue-ambiguous-location"></a><span data-ttu-id="5d306-107">Erreur/problème emplacement ambigu</span><span class="sxs-lookup"><span data-stu-id="5d306-107">Error/issue ambiguous location</span></span>

<span data-ttu-id="5d306-108">Vous recevez cette erreur «la recherche de conformité contient l’emplacement `(s):useralias@contoso.com. The location "useralias@contoso.com" is ambiguous"` non valide suivant si vous avez essayé d’ajouter l’emplacement de boîte aux lettres de l’utilisateur pour la recherche et qu’il existe des objets en double ou en conflit avec le même ID d’utilisateur dans Exchange Online Protection (EoP) Active.</span><span class="sxs-lookup"><span data-stu-id="5d306-108">You'll receive this error "The compliance search contains the following invalid location `(s):useralias@contoso.com. The location "useralias@contoso.com" is ambiguous"` if you tried to add user’s mailbox location to search and there are duplicate or conflicting objects with the same user id in the Exchange Online Protection (EOP) directory.</span></span>

### <a name="resolution"></a><span data-ttu-id="5d306-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="5d306-109">Resolution</span></span>

<span data-ttu-id="5d306-110">Recherchez les utilisateurs en double ou la liste de distribution avec le même ID d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5d306-110">Check for duplicate users or distribution list with the same user ID.</span></span>

1. <span data-ttu-id="5d306-111">Connectez-vous à [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="5d306-111">Connect to [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>
2. <span data-ttu-id="5d306-112">Récupérez toutes les instances du nom d’utilisateur, tapez :</span><span class="sxs-lookup"><span data-stu-id="5d306-112">Retrieve all instances of the username, type:</span></span>

```powershell
Get-Recipient <username>
```

<span data-ttu-id="5d306-113">La sortie de’useralias@contoso.com’peut être</span><span class="sxs-lookup"><span data-stu-id="5d306-113">The output for 'useralias@contoso.com' might be</span></span>

> 
> |<span data-ttu-id="5d306-114">Nom</span><span class="sxs-lookup"><span data-stu-id="5d306-114">Name</span></span>  |<span data-ttu-id="5d306-115">RecipientType</span><span class="sxs-lookup"><span data-stu-id="5d306-115">RecipientType</span></span>  |
> |---------|---------|
> |<span data-ttu-id="5d306-116">Alias, User</span><span class="sxs-lookup"><span data-stu-id="5d306-116">Alias, User</span></span>     |<span data-ttu-id="5d306-117">MailUser</span><span class="sxs-lookup"><span data-stu-id="5d306-117">MailUser</span></span>         |
> |<span data-ttu-id="5d306-118">Alias, User</span><span class="sxs-lookup"><span data-stu-id="5d306-118">Alias, User</span></span>     |<span data-ttu-id="5d306-119">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="5d306-119">User</span></span>         |

3. <span data-ttu-id="5d306-120">Si plusieurs utilisateurs sont renvoyés, recherchez et corrigez l’objet en conflit.</span><span class="sxs-lookup"><span data-stu-id="5d306-120">If multiple users are returned, locate and fix the conflicting object.</span></span>

## <a name="errorissue-search-fails-on-specific-locations"></a><span data-ttu-id="5d306-121">Échec de la recherche d’erreur/problème sur des emplacements spécifiques</span><span class="sxs-lookup"><span data-stu-id="5d306-121">Error/issue search fails on specific locations</span></span>

<span data-ttu-id="5d306-122">Une recherche de contenu ou eDiscovery peut produire l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="5d306-122">An eDiscovery or content search may yield the following error:</span></span>
><span data-ttu-id="5d306-123">Cette recherche s’est terminée avec les erreurs (#).</span><span class="sxs-lookup"><span data-stu-id="5d306-123">This search completed with (#) errors.</span></span>  <span data-ttu-id="5d306-124">Voulez-vous relancer la recherche sur les emplacements ayant échoué ?</span><span class="sxs-lookup"><span data-stu-id="5d306-124">Would you like to retry the search on the failed locations?</span></span>

![capture d’écran des erreurs d’emplacement spécifique à la recherche]( media/edisc-tshoot-specific-location-search-fails.png)

### <a name="resolution"></a><span data-ttu-id="5d306-126">Résolution</span><span class="sxs-lookup"><span data-stu-id="5d306-126">Resolution</span></span>

<span data-ttu-id="5d306-127">Si vous recevez cette erreur, nous vous recommandons de vérifier les emplacements ayant échoué dans la recherche, puis de ré-exécuter la recherche uniquement sur les emplacements ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="5d306-127">If you receive this error, we recommend that you verify the locations that failed in the search  then re-run the search only on the failed locations.</span></span>

1. <span data-ttu-id="5d306-128">Connectez-vous à [Exchange Online Protection PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="5d306-128">Connect to [Exchange Online Protection Powershell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps).</span></span>
1. <span data-ttu-id="5d306-129">Type :</span><span class="sxs-lookup"><span data-stu-id="5d306-129">Type:</span></span>

```powershell
Get-Compliancesearch searchname|fl 
```

3. <span data-ttu-id="5d306-130">À partir de la sortie PowerShell, affichez les emplacements en échec dans le champ erreurs ou à partir des informations d’État dans l’erreur du résultat de la recherche.</span><span class="sxs-lookup"><span data-stu-id="5d306-130">From the PowerShell output, view the failed locations in the errors field or from the status details in the error from the search output.</span></span>
1. <span data-ttu-id="5d306-131">Renouvelez la recherche de découverte électronique aux emplacements ayant échoué uniquement.</span><span class="sxs-lookup"><span data-stu-id="5d306-131">Retry the eDiscovery search on the failed locations only.</span></span>
1. <span data-ttu-id="5d306-132">Si vous continuez à recevoir ces erreurs, reportez-vous à la rubrique [Retry failed locations](https://docs.microsoft.com/en-us/Office365/SecurityCompliance/retry-failed-content-search) pour connaître les étapes de dépannage supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="5d306-132">If you continue to receive these error, see [Retry failed locations](https://docs.microsoft.com/en-us/Office365/SecurityCompliance/retry-failed-content-search) for additional troubleshooting steps.</span></span>

## <a name="errorissue-file-not-found"></a><span data-ttu-id="5d306-133">Erreur/fichier de problème introuvable</span><span class="sxs-lookup"><span data-stu-id="5d306-133">Error/issue file not found</span></span>

<span data-ttu-id="5d306-134">Lors de l’exécution d’une recherche de découverte électronique incluant SharePoint Online et un lecteur pour les emplacements d’entreprise `File Not Found` , vous pouvez recevoir le message d’erreur même si le fichier se trouve sur le site.</span><span class="sxs-lookup"><span data-stu-id="5d306-134">When running an eDiscovery search that includes SharePoint Online and One Drive For Business locations, you may receive the error `File Not Found` although the file is located on the site.</span></span> <span data-ttu-id="5d306-135">Cette erreur se produit dans les avertissements et les erreurs d’exportation. csv ou éléments ignorés. csv cela peut se produire si le fichier est introuvable sur le site ou si l’index est obsolète.</span><span class="sxs-lookup"><span data-stu-id="5d306-135">This error will be in the export warnings and errors.csv or skipped items.csv  This may occur if the file cannot be located on the site or the index is out of date.</span></span> <span data-ttu-id="5d306-136">Voici le texte d’une erreur réelle, avec l’accentuation ajoutée.</span><span class="sxs-lookup"><span data-stu-id="5d306-136">Here's the text of an actual error, with emphasis added.</span></span>
  
> <span data-ttu-id="5d306-137">28.06.2019 10:02:19_FailedToExportItem_Failed pour télécharger du contenu.</span><span class="sxs-lookup"><span data-stu-id="5d306-137">28.06.2019 10:02:19_FailedToExportItem_Failed to download content.</span></span> <span data-ttu-id="5d306-138">Informations de diagnostic supplémentaires : Microsoft. Office. Compliance. EDiscovery. ExportWorker. exceptions. ContentDownloadTemporaryFailure : échec de téléchargement à partir du contenu 6ea52149-91cd-4965-b5bb-82ca6a3ec9be de type document.</span><span class="sxs-lookup"><span data-stu-id="5d306-138">Additional diagnostic info : Microsoft.Office.Compliance.EDiscovery.ExportWorker.Exceptions.ContentDownloadTemporaryFailure: Failed to download from content 6ea52149-91cd-4965-b5bb-82ca6a3ec9be of type Document.</span></span> <span data-ttu-id="5d306-139">ID de corrélation : 3bd84722-937b-4c23-B61B-08d6fba9ec32.</span><span class="sxs-lookup"><span data-stu-id="5d306-139">Correlation Id: 3bd84722-937b-4c23-b61b-08d6fba9ec32.</span></span> <span data-ttu-id="5d306-140">ServerErrorCode :-2147024894---> Microsoft. SharePoint. client. ServerException : ***fichier introuvable***.</span><span class="sxs-lookup"><span data-stu-id="5d306-140">ServerErrorCode: -2147024894 ---> Microsoft.SharePoint.Client.ServerException: ***File Not Found***.</span></span> <span data-ttu-id="5d306-141">at Microsoft. SharePoint. client. ClientRequest. ProcessResponseStream (Stream responseStream) à Microsoft. SharePoint. client. ClientRequest. ProcessResponse ()---fin de la trace de la pile d’exception interne---</span><span class="sxs-lookup"><span data-stu-id="5d306-141">at Microsoft.SharePoint.Client.ClientRequest.ProcessResponseStream(Stream responseStream) at Microsoft.SharePoint.Client.ClientRequest.ProcessResponse() --- End of inner exception stack trace ---</span></span>

### <a name="resolution"></a><span data-ttu-id="5d306-142">Résolution</span><span class="sxs-lookup"><span data-stu-id="5d306-142">Resolution</span></span>

1. <span data-ttu-id="5d306-143">Vérifiez l’emplacement identifié dans la recherche pour vous assurer que l’emplacement du fichier est correct et ajouté aux emplacements de recherche.</span><span class="sxs-lookup"><span data-stu-id="5d306-143">Check location identified in the search to ensure the that the location of the file is correct and added in the search locations.</span></span>
2. <span data-ttu-id="5d306-144">Utilisez les procédures pour [demander manuellement l’analyse et la réindexation d’un site, d’une bibliothèque ou d’une liste](https://docs.microsoft.com/en-us/sharepoint/crawl-site-content) pour réindexer le site.</span><span class="sxs-lookup"><span data-stu-id="5d306-144">Use the procedures at [Manually request crawling and re-indexing of a site, a library or a list](https://docs.microsoft.com/en-us/sharepoint/crawl-site-content) to re-index the site.</span></span>

## <a name="errorissue-search-fails-recipient-not-found"></a><span data-ttu-id="5d306-145">Échec de la recherche d’erreur/problème le destinataire est introuvable</span><span class="sxs-lookup"><span data-stu-id="5d306-145">Error/issue search fails recipient not found</span></span>

<span data-ttu-id="5d306-146">la recherche de découverte électronique `recipient not found`échoue avec une erreur.</span><span class="sxs-lookup"><span data-stu-id="5d306-146">eDiscovery search fails with error `recipient not found`.</span></span> <span data-ttu-id="5d306-147">Cette erreur peut se produire si l’objet utilisateur est introuvable dans Exchange Online Protection (EOP) car l’objet n’a pas été synchronisé.</span><span class="sxs-lookup"><span data-stu-id="5d306-147">This error may occur if the user object cannot be found in Exchange Online Protection (EOP) because the object has not synced.</span></span>

### <a name="resolution"></a><span data-ttu-id="5d306-148">Résolution</span><span class="sxs-lookup"><span data-stu-id="5d306-148">Resolution</span></span>

1. <span data-ttu-id="5d306-149">Connectez-vous à [Exchange Online Protection PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="5d306-149">Connect to [Exchange Online Protection PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps).</span></span>
1. <span data-ttu-id="5d306-150">Vérifiez si l’objet utilisateur est synchronisé avec le type de protection Exchange Online :</span><span class="sxs-lookup"><span data-stu-id="5d306-150">Check to see if the user object is synced to Exchange Online Protection type:</span></span>

```powershell
Get-Recipient userId|fl
```

3. <span data-ttu-id="5d306-151">Il doit y avoir un objet MailUser pour la question de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5d306-151">There should be a mailuser object for the user question.</span></span> <span data-ttu-id="5d306-152">Si aucune valeur n’est renvoyée, examinez l’objet User.</span><span class="sxs-lookup"><span data-stu-id="5d306-152">If nothing is returned, investigate the user object.</span></span> <span data-ttu-id="5d306-153">Contacter CSS si l’objet ne peut pas être synchronisé.</span><span class="sxs-lookup"><span data-stu-id="5d306-153">Contact CSS if the object can't be synced.</span></span>

## <a name="errorissue-exporting-search-results-is-slow"></a><span data-ttu-id="5d306-154">Erreur/problème l’exportation des résultats de la recherche est lente</span><span class="sxs-lookup"><span data-stu-id="5d306-154">Error/issue exporting search results is slow</span></span>

<span data-ttu-id="5d306-155">Lors de l’exportation des résultats de recherche à partir de eDiscovery ou de la recherche de contenu dans le centre de sécurité et conformité, le téléchargement prend plus de temps que prévu.</span><span class="sxs-lookup"><span data-stu-id="5d306-155">When exporting search results from eDiscovery or Content Search in the Security and Compliance center, the download takes longer than expected.</span></span>  <span data-ttu-id="5d306-156">Vous pouvez vérifier la quantité de données à télécharger et augmenter éventuellement la vitesse d’exportation.</span><span class="sxs-lookup"><span data-stu-id="5d306-156">You can check to see the amount of data to be download and possibly increase the export speed.</span></span>

### <a name="resolution"></a><span data-ttu-id="5d306-157">Résolution</span><span class="sxs-lookup"><span data-stu-id="5d306-157">Resolution</span></span>

1.  <span data-ttu-id="5d306-158">Essayez d’utiliser les étapes indiquées dans l’article [augmenter les vitesses de téléchargement](https://docs.microsoft.com/en-us/office365/securitycompliance/increase-download-speeds-when-exporting-ediscovery-results).</span><span class="sxs-lookup"><span data-stu-id="5d306-158">Try using the steps identified in the article [Increase Download Speeds](https://docs.microsoft.com/en-us/office365/securitycompliance/increase-download-speeds-when-exporting-ediscovery-results).</span></span>
2.  <span data-ttu-id="5d306-159">Si vous rencontrez toujours des problèmes, connectez-vous à [Exchange Online Protection PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps) et tapez :</span><span class="sxs-lookup"><span data-stu-id="5d306-159">If you still have issues, connect to [Exchange Online Protection PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps) and type:</span></span>

```powershell
Get-ComplianceSearch searchname\fl
```

4. <span data-ttu-id="5d306-160">Recherchez la quantité de données à télécharger dans les paramètres SearchResults et SearchStatistics.</span><span class="sxs-lookup"><span data-stu-id="5d306-160">Find the amount of data to be downloaded in the SearchResults and SearchStatistics parameters.</span></span>
5. <span data-ttu-id="5d306-161">Type :</span><span class="sxs-lookup"><span data-stu-id="5d306-161">Type:</span></span>

```powershell
Get-ComplianceSearchAction |fl
```

6. <span data-ttu-id="5d306-162">Dans le champ résultats, recherchez les données qui ont été exportées et affichez les erreurs rencontrées.</span><span class="sxs-lookup"><span data-stu-id="5d306-162">In the results field find the data that has been exported and view any errors encountered.</span></span>
7. <span data-ttu-id="5d306-163">Vérifiez le fichier trace. log situé dans le répertoire dans lequel vous avez exporté le contenu pour détecter d’éventuelles erreurs.</span><span class="sxs-lookup"><span data-stu-id="5d306-163">Check the trace.log file located in the directory that you exported the content to for any errors.</span></span>

## <a name="errorissue-internal-server-error-500-occurred"></a><span data-ttu-id="5d306-164">Erreur/problème "une erreur de serveur interne (500) s’est produite"</span><span class="sxs-lookup"><span data-stu-id="5d306-164">Error/issue "Internal server error (500) occurred"</span></span>

<span data-ttu-id="5d306-165">Lors de l’exécution d’une recherche de découverte électronique, si la recherche continue de se produire avec une erreur semblable à « erreur interne du serveur (500) », vous pouvez être amené à relancer la recherche uniquement sur des emplacements de boîte aux lettres spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5d306-165">When running an eDiscovery search, if the search continually fails with error similar to "Internal server error (500) occurred", you may need re-run the search only on specific mailbox locations.</span></span>

![capture d’écran de l’erreur de serveur interne 500](media/edisc-tshoot-error-500.png)

### <a name="resolution"></a><span data-ttu-id="5d306-167">Résolution</span><span class="sxs-lookup"><span data-stu-id="5d306-167">Resolution</span></span>

1. <span data-ttu-id="5d306-168">Fractionnez la recherche en petites recherches et réexécutez la recherche.</span><span class="sxs-lookup"><span data-stu-id="5d306-168">Break the search into smaller searches and run the search again.</span></span>  <span data-ttu-id="5d306-169">Essayez d’utiliser une plage de dates plus petite ou limitez le nombre d’emplacements recherchés.</span><span class="sxs-lookup"><span data-stu-id="5d306-169">Try using a smaller date range or limit the number of locations being searched.</span></span>
2. <span data-ttu-id="5d306-170">Connectez-vous à [Exchange Online Protection PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps) et tapez :</span><span class="sxs-lookup"><span data-stu-id="5d306-170">Connect to [Exchange Online Protection PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps) and type:</span></span>

```powershell
Get-ComplianceSearch searchname |fl
```

3. <span data-ttu-id="5d306-171">Examinez la sortie pour les résultats et les erreurs.</span><span class="sxs-lookup"><span data-stu-id="5d306-171">Examine the output for results and errors.</span></span>
3. <span data-ttu-id="5d306-172">Examinez le fichier trace. log.</span><span class="sxs-lookup"><span data-stu-id="5d306-172">Examine the trace.log file.</span></span> <span data-ttu-id="5d306-173">Il se trouve dans le dossier vers lequel vous avez envoyé l’exportation.</span><span class="sxs-lookup"><span data-stu-id="5d306-173">It will be in the same folder that you sent the export to.</span></span>
4. <span data-ttu-id="5d306-174">Contactez le support technique CSS.</span><span class="sxs-lookup"><span data-stu-id="5d306-174">Contact Support CSS.</span></span>

## <a name="errorissue-holds-dont-sync"></a><span data-ttu-id="5d306-175">Erreurs/problèmes suspendus ne pas synchroniser</span><span class="sxs-lookup"><span data-stu-id="5d306-175">Error/issue holds don't sync</span></span>

<span data-ttu-id="5d306-176">erreur de distribution de la stratégie de conservation de cas eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="5d306-176">eDiscovery Case Hold Policy Sync Distribution error.</span></span> <span data-ttu-id="5d306-177">L’erreur indique :</span><span class="sxs-lookup"><span data-stu-id="5d306-177">The error reads:</span></span>

> <span data-ttu-id="5d306-178">«Ressources : le déploiement de la stratégie prend plus de temps que prévu.</span><span class="sxs-lookup"><span data-stu-id="5d306-178">"Resources: It's taking longer than expected to deploy the policy.</span></span> <span data-ttu-id="5d306-179">La mise à jour de l’état final du déploiement peut prendre deux heures supplémentaires, vous pouvez donc vérifier en quelques heures.</span><span class="sxs-lookup"><span data-stu-id="5d306-179">It might take an additional two hours to update the final deployment status, so check back in a couple hours.”</span></span>

### <a name="resolution"></a><span data-ttu-id="5d306-180">Résolution</span><span class="sxs-lookup"><span data-stu-id="5d306-180">Resolution</span></span>

1.  <span data-ttu-id="5d306-181">Connectez-vous à [Exchange Online Protection PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps) et tapez :</span><span class="sxs-lookup"><span data-stu-id="5d306-181">Connect to [Exchange Online Protection PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps) and type:</span></span>

```powershell
Get-RetentionCompliancePolicy  policyname - Distributiondetail|fl
```

2. <span data-ttu-id="5d306-182">Examinez la valeur du paramètre Distributiondetail pour rechercher les erreurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="5d306-182">Examine the value in the Distributiondetail parameter for errors like the following:</span></span>

> <span data-ttu-id="5d306-183">Si une erreur existe, créez une escalade à PG pour forcer une resynchronisation manuelle sur la stratégie.</span><span class="sxs-lookup"><span data-stu-id="5d306-183">If error exists, create escalation to PG to force a manual re-sync on the Policy.</span></span>

3. <span data-ttu-id="5d306-184">Code CSS des contacts.</span><span class="sxs-lookup"><span data-stu-id="5d306-184">Contact CSS.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d306-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d306-185">See Also</span></span>
- [<span data-ttu-id="5d306-186">Conseils pour éviter les erreurs d’emplacement de contenu</span><span class="sxs-lookup"><span data-stu-id="5d306-186">Tips to avoid content location errors</span></span>](https://docs.microsoft.com/en-us/microsoft-365/compliance/retry-failed-content-search%23tips-to-avoid-content-location-errors)