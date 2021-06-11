---
title: Résoudre les erreurs de mise en suspens de la découverte électronique
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.custom:
- seo-marvel-apr2020
description: Résoudre les erreurs liées aux conservations légales appliquées aux dépositaires et aux sources de données qui ne sont pas en conservation dans core eDiscovery.
ms.openlocfilehash: b101bf92c6a304262b3886a4ce0280f427a4a847
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52538470"
---
# <a name="troubleshoot-ediscovery-hold-errors"></a><span data-ttu-id="8b060-103">Résoudre les erreurs de mise en suspens de la découverte électronique</span><span class="sxs-lookup"><span data-stu-id="8b060-103">Troubleshoot eDiscovery hold errors</span></span>

<span data-ttu-id="8b060-104">Cet article traite des problèmes courants qui peuvent se produire avec les conserves eDiscovery et explique comment les résoudre.</span><span class="sxs-lookup"><span data-stu-id="8b060-104">This article discusses common issues that may occur with eDiscovery holds and how to resolve them.</span></span> <span data-ttu-id="8b060-105">L’article inclut également des pratiques recommandées pour vous aider à atténuer ou à éviter ces problèmes.</span><span class="sxs-lookup"><span data-stu-id="8b060-105">The article also includes recommended practices to help you mitigate or avoid these issues.</span></span>

## <a name="recommended-practices"></a><span data-ttu-id="8b060-106">Pratiques recommandées</span><span class="sxs-lookup"><span data-stu-id="8b060-106">Recommended practices</span></span>

<span data-ttu-id="8b060-107">Pour réduire le nombre d’erreurs liées aux conserves eDiscovery, nous vous recommandons les pratiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="8b060-107">To reduce the number of errors related to eDiscovery holds, we recommend the following practices:</span></span>

- <span data-ttu-id="8b060-108">Si une distribution de la mise en attente est toujours en attente, avec l’un ou l’autre état, patientez jusqu’à ce que la distribution de la mise en attente soit `On (Pending)` terminée avant d’effectuer d’autres mises à `Off (Pending)` jour.</span><span class="sxs-lookup"><span data-stu-id="8b060-108">If a hold distribution is still pending, with a status of either `On (Pending)` or `Off (Pending)`, wait until the hold distribution is complete before you make any further updates.</span></span>

- <span data-ttu-id="8b060-109">Vérifiez si une stratégie de mise en attente est en attente avant d’y apporter d’autres mises à jour.</span><span class="sxs-lookup"><span data-stu-id="8b060-109">Check whether a hold policy is pending before you make any further updates to it.</span></span> <span data-ttu-id="8b060-110">Exécutez les commandes suivantes ou enregistrez-les dans un script PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8b060-110">Run the following commands or save them to a PowerShell script.</span></span>

    ```powershell
    $status = Get-CaseHoldPolicy -Identity <policyname> 
    if($status.DistributionStatus -ne "Pending"){
        # policy no longer pending
        Set-CaseHoldPolicy -Identity <policyname> -AddExchangeLocation $user1
    }else{
        # policy still pending
        Write-Host "Hold policy still pending."
    }
   ```

- <span data-ttu-id="8b060-111">Fusionnez vos mises à jour vers une mise en attente eDiscovery dans une seule demande en bloc au lieu de mettre à jour la stratégie de mise à jour à plusieurs reprises pour chaque transaction.</span><span class="sxs-lookup"><span data-stu-id="8b060-111">Merge your updates to an eDiscovery hold in a single bulk request rather than updating the hold policy repeatedly for each transaction.</span></span> <span data-ttu-id="8b060-112">Par exemple, pour ajouter plusieurs boîtes aux lettres utilisateur à une stratégie de blocage existante à l’aide de la cmdlet [Set-CaseHoldPolicy,](/powershell/module/exchange/set-caseholdpolicy) exécutez la commande (ou ajoutez-la en tant que bloc de code à un script) afin qu’elle ne s’exécute qu’une seule fois pour ajouter plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8b060-112">For example, to add multiple user mailboxes to an existing hold policy using the [Set-CaseHoldPolicy](/powershell/module/exchange/set-caseholdpolicy) cmdlet, run the command (or add as a code block to a script) so that it runs only once to add multiple users.</span></span>

  <span data-ttu-id="8b060-113">**Correct**</span><span class="sxs-lookup"><span data-stu-id="8b060-113">**Correct**</span></span>

    ```powershell
    Set-CaseHoldPolicy -Identity <policyname> -AddExchangeLocation {$user1, $user2, $user3, $user4, $user5}
    ```

   <span data-ttu-id="8b060-114">**Incorrect**</span><span class="sxs-lookup"><span data-stu-id="8b060-114">**Incorrect**</span></span>

    ```powershell
    $users = {$user1, $user2, $user3, $user4, $user5}
    ForEach($user in $users)
    {
        Set-CaseHoldPolicy -Identity <policyname> -AddExchangeLocation $user
    }
    ```

   <span data-ttu-id="8b060-115">Dans l’exemple incorrect précédent, la cmdlet est exécuté cinq fois distinctement pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="8b060-115">In the previous incorrect example, the cmdlet is run five separate times to complete the task.</span></span> <span data-ttu-id="8b060-116">Pour plus d’informations sur les pratiques recommandées pour ajouter des utilisateurs à une stratégie de attente, consultez la section [Plus d’informations.](#more-information)</span><span class="sxs-lookup"><span data-stu-id="8b060-116">For more information about the recommended practices for adding users to a hold policy, see the [More information](#more-information) section.</span></span>

- <span data-ttu-id="8b060-117">Avant de contacter le Support Microsoft à propos des problèmes de la découverte électronique, suivez les étapes de la section [Erreur/problème](#errorissue-holds-dont-sync) : Les attentes ne sont pas synchronisées pour réessayer la distribution de la attente.</span><span class="sxs-lookup"><span data-stu-id="8b060-117">Before contacting Microsoft Support about eDiscovery hold issues, follow the steps in the [Error/issue: Holds don't sync](#errorissue-holds-dont-sync) section to retry the hold distribution.</span></span> <span data-ttu-id="8b060-118">Ce processus résout souvent des problèmes temporaires, notamment des erreurs de serveur interne.</span><span class="sxs-lookup"><span data-stu-id="8b060-118">This process often resolves temporary issues including, internal server errors.</span></span>

## <a name="errorissue-holds-dont-sync"></a><span data-ttu-id="8b060-119">Erreur/problème : les holds ne sont pas synchronisés</span><span class="sxs-lookup"><span data-stu-id="8b060-119">Error/issue: Holds don't sync</span></span>

<span data-ttu-id="8b060-120">Si vous voyez l’un des messages d’erreur suivants lors de la mise en attente des dépositaires et des sources de données, utilisez les étapes de résolution pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="8b060-120">If you see one the following error messages when putting custodians and data sources on hold, use the resolution steps to troubleshoot the issue.</span></span>

> <span data-ttu-id="8b060-121">Ressources : le déploiement de la stratégie prend plus de temps que prévu.</span><span class="sxs-lookup"><span data-stu-id="8b060-121">Resources: It's taking longer than expected to deploy the policy.</span></span> <span data-ttu-id="8b060-122">La mise à jour de l’état de déploiement final peut prendre 2 heures supplémentaires. Vérifiez-le dans quelques heures.</span><span class="sxs-lookup"><span data-stu-id="8b060-122">It might take an additional 2 hours to update the final deployment status, so check back in a couple hours.</span></span>

> <span data-ttu-id="8b060-123">La stratégie ne peut pas être déployée sur la source de contenu en raison d’un problème Office 365 de centre de données temporaire.</span><span class="sxs-lookup"><span data-stu-id="8b060-123">Policy cannot be deployed to the content source due to a temporary Office 365 datacenter issue.</span></span> <span data-ttu-id="8b060-124">La stratégie actuelle n’est appliquée à aucun contenu de la source, donc le déploiement bloqué n’a aucun impact.</span><span class="sxs-lookup"><span data-stu-id="8b060-124">The current policy is not applied to any content in the source, so there's no impact from the blocked deployment.</span></span> <span data-ttu-id="8b060-125">Pour résoudre ce problème, essayez de redéployer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="8b060-125">To fix this issue, please try redeploying the policy.</span></span>

> <span data-ttu-id="8b060-126">Désolé, nous n’avons pas pu effectuer les modifications demandées à la stratégie en raison d’une erreur temporaire du serveur interne.</span><span class="sxs-lookup"><span data-stu-id="8b060-126">Sorry, we could not perform the requested changes to policy due to a transient internal server error.</span></span> <span data-ttu-id="8b060-127">Veuillez essayer à nouveau dans 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="8b060-127">Please try again in 30 minutes.</span></span>

### <a name="resolution"></a><span data-ttu-id="8b060-128">Résolution</span><span class="sxs-lookup"><span data-stu-id="8b060-128">Resolution</span></span>

1. <span data-ttu-id="8b060-129">Connecter [au Centre de sécurité & conformité PowerShell](/powershell/exchange/connect-to-scc-powershell) et exécutez la commande suivante pour une mise en attente eDiscovery :</span><span class="sxs-lookup"><span data-stu-id="8b060-129">Connect to [Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell) and run the following command for an eDiscovery hold:</span></span>

   ```powershell
   Get-CaseHoldPolicy <policyname> -DistributionDetail | FL
   ```

2. <span data-ttu-id="8b060-130">Examinez la valeur dans le *paramètre DistributionDetail.*</span><span class="sxs-lookup"><span data-stu-id="8b060-130">Examine the value in the *DistributionDetail* parameter.</span></span> <span data-ttu-id="8b060-131">Recherchez les erreurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8b060-131">Look for errors like the following:</span></span>

   > <span data-ttu-id="8b060-132">Erreur : Ressources : le déploiement de la stratégie prend plus de temps que prévu.</span><span class="sxs-lookup"><span data-stu-id="8b060-132">Error: Resources: It's taking longer than expected to deploy the policy.</span></span> <span data-ttu-id="8b060-133">La mise à jour de l’état de déploiement final peut prendre 2 heures supplémentaires. Vérifiez-le dans quelques heures.</span><span class="sxs-lookup"><span data-stu-id="8b060-133">It might take an additional 2 hours to update the final deployment status, so check back in a couple hours.</span></span>

3. <span data-ttu-id="8b060-134">Essayez d’exécution de la commande **Set-CaseHoldPolicy -RetryDistribution** sur la stratégie de mise en attente en question ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="8b060-134">Try running the **Set-CaseHoldPolicy -RetryDistribution** command on the hold policy in question; for example:</span></span>

   ```powershell
   Set-CaseHoldPolicy <policyname> -RetryDistribution
   ```

## <a name="error-the-sharepoint-site-is-read-only-or-not-accessible"></a><span data-ttu-id="8b060-135">Erreur : le site SharePoint est en lecture seule ou inaccessible</span><span class="sxs-lookup"><span data-stu-id="8b060-135">Error: The SharePoint site is read-only or not accessible</span></span>

<span data-ttu-id="8b060-136">Si vous voyez le message d’erreur suivant lors de la mise en attente des dépositaires et des sources de données, cela signifie que l’administrateur global de votre organisation ou l’administrateur [SharePoint a](/sharepoint/sharepoint-admin-role) verrouillé le site.</span><span class="sxs-lookup"><span data-stu-id="8b060-136">If you see the following error message when putting custodians and data sources on hold, it means that your organization's [global admin or SharePoint admin](/sharepoint/sharepoint-admin-role) has locked the site.</span></span> <span data-ttu-id="8b060-137">Un site verrouillé empêche eDiscovery de placer le site en attente.</span><span class="sxs-lookup"><span data-stu-id="8b060-137">A locked site blocks eDiscovery from placing a hold on the site.</span></span>

> <span data-ttu-id="8b060-138">Le site SharePoint est accessible en lecture seule ou inaccessible.</span><span class="sxs-lookup"><span data-stu-id="8b060-138">The SharePoint site is read-only or not accessible.</span></span> <span data-ttu-id="8b060-139">Veuillez contacter l’administrateur du site pour rendre le site accessible en ligne, puis redéployer cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="8b060-139">Please contact the site administrator to make the site writable, and then redeploy this policy.</span></span>

### <a name="resolution"></a><span data-ttu-id="8b060-140">Résolution</span><span class="sxs-lookup"><span data-stu-id="8b060-140">Resolution</span></span>

<span data-ttu-id="8b060-141">Déverrouillez le site (ou demandez à un administrateur de le déverrouiller) pour résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="8b060-141">Unlock the site (or ask an admin to unlock it) to resolve this issue.</span></span> <span data-ttu-id="8b060-142">Pour en savoir plus sur la façon de modifier l’état de verrouillage d’un site, voir [Verrouiller et déverrouiller des sites.](/sharepoint/manage-lock-status)</span><span class="sxs-lookup"><span data-stu-id="8b060-142">To learn more about how to change the lock state for a site, see [Lock and unlock sites](/sharepoint/manage-lock-status).</span></span>

## <a name="error-the-mailbox-or-sharepoint-site-may-not-exist"></a><span data-ttu-id="8b060-143">Erreur : la boîte aux lettres ou SharePoint site n’existe peut-être pas</span><span class="sxs-lookup"><span data-stu-id="8b060-143">Error: The mailbox or SharePoint site may not exist</span></span>

<span data-ttu-id="8b060-144">Si vous voyez le message d’erreur suivant lors de la mise en attente des dépositaires et des sources de données, utilisez les étapes de résolution pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="8b060-144">If you see the following error message when putting custodians and data sources on hold, use the resolution steps to troubleshoot the issue.</span></span>

> <span data-ttu-id="8b060-145">La boîte aux lettres ou SharePoint site web n’existe peut-être pas.</span><span class="sxs-lookup"><span data-stu-id="8b060-145">The mailbox or SharePoint site may not exist.</span></span>  <span data-ttu-id="8b060-146">Si ce n’est pas le cas, contactez le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8b060-146">If this is incorrect, please contact Microsoft support.</span></span>  <span data-ttu-id="8b060-147">Dans le cas contraire, supprimez-la de cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="8b060-147">Otherwise, please remove it from this policy.</span></span>

### <a name="resolution"></a><span data-ttu-id="8b060-148">Résolution</span><span class="sxs-lookup"><span data-stu-id="8b060-148">Resolution</span></span>

- <span data-ttu-id="8b060-149">Exécutez [Get-Mailbox](/powershell/module/exchange/get-mailbox) dans Exchange Online PowerShell pour vérifier si la boîte aux lettres utilisateur existe dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8b060-149">Run the [Get-Mailbox](/powershell/module/exchange/get-mailbox) in Exchange Online PowerShell to check if the user mailbox exists in your organization.</span></span>

- <span data-ttu-id="8b060-150">Exécutez la cmdlet [Get-SPOSite](/powershell/module/sharepoint-online/get-sposite) dans SharePoint Online PowerShell pour vérifier si le site existe dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8b060-150">Run the [Get-SPOSite](/powershell/module/sharepoint-online/get-sposite) cmdlet in SharePoint Online PowerShell to check if the site exists in your organization.</span></span>

- <span data-ttu-id="8b060-151">Vérifiez si l’URL du site a changé.</span><span class="sxs-lookup"><span data-stu-id="8b060-151">Check to see if the site URL has changed.</span></span>

## <a name="more-information"></a><span data-ttu-id="8b060-152">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="8b060-152">More information</span></span>

<span data-ttu-id="8b060-153">Les instructions sur la mise à jour des stratégies de blocage pour plusieurs utilisateurs dans la section « Pratiques recommandées » résultent du fait que le système bloque les mises à jour simultanées d’une stratégie de blocage.</span><span class="sxs-lookup"><span data-stu-id="8b060-153">The guidance about updating hold policies for multiple users in the "Recommended practices" section results from the fact that the system blocks simultaneous updates to a hold policy.</span></span> <span data-ttu-id="8b060-154">Cela signifie que lorsqu’une stratégie de mise à jour de mise en attente est appliquée aux nouveaux emplacements de contenu et que la stratégie de mise en attente est dans un état en attente, des emplacements de contenu supplémentaires ne peuvent pas être ajoutés à la stratégie de mise en attente.</span><span class="sxs-lookup"><span data-stu-id="8b060-154">That means when an updated hold policy is applied to new content locations and the hold policy is in a pending state, additional content locations can't be added to the hold policy.</span></span> <span data-ttu-id="8b060-155">Voici quelques éléments à garder à l’esprit pour vous aider à atténuer ce problème :</span><span class="sxs-lookup"><span data-stu-id="8b060-155">Here are some things to keep in mind to help you mitigate this issue:</span></span>
  
- <span data-ttu-id="8b060-156">Chaque fois qu’une mise à jour de la mise à jour d’une mise en attente est mise à jour, elle passe immédiatement dans un état en attente.</span><span class="sxs-lookup"><span data-stu-id="8b060-156">Every time a hold updated is updated, it immediately goes into a pending state.</span></span> <span data-ttu-id="8b060-157">L’état d’état en attente signifie que la attente est appliquée aux emplacements de contenu.</span><span class="sxs-lookup"><span data-stu-id="8b060-157">The pending state status means the hold is being applied to content locations.</span></span>
  
- <span data-ttu-id="8b060-158">Si vous avez un script qui exécute une boucle et ajoute des emplacements à la stratégie un par un (semblable à l’exemple incorrect présenté dans la section « Pratiques recommandées », le premier emplacement de contenu (par exemple, une boîte aux lettres utilisateur) lance le processus de synchronisation qui déclenche l’état en attente.</span><span class="sxs-lookup"><span data-stu-id="8b060-158">If you have a script that runs a loop and adds locations to policy one by one (similar to the incorrect example shown in the "Recommended practices" section), the first content location (for example, a user mailbox) initiates the sync process that triggers the pending state.</span></span> <span data-ttu-id="8b060-159">Cela signifie que les autres utilisateurs ajoutés à la stratégie dans les boucles suivantes entraînent une erreur.</span><span class="sxs-lookup"><span data-stu-id="8b060-159">That means the other users that are added to the policy in subsequent loops result in an error.</span></span>
  
- <span data-ttu-id="8b060-160">Si votre organisation utilise un script qui exécute une boucle pour mettre à jour les emplacements de contenu pour une stratégie de mise en attente, vous devez mettre à jour le script afin qu’il met à jour les emplacements en une seule opération en bloc (comme illustré dans l’exemple correct dans la section « Pratiques recommandées »).</span><span class="sxs-lookup"><span data-stu-id="8b060-160">If your organization is using a script that runs a loop to update the content locations for a hold policy, you must update the script so that it updates locations in a single bulk operation (as shown in the correct example in the "Recommended practices" section).</span></span>
