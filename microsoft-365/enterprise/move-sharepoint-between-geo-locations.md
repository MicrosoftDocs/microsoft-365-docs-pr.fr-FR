---
title: Déplacer un site SharePoint vers un autre emplacement géographique
ms.reviewer: adwood
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: o365-solutions
ms.collection:
- Strat_SP_gtc
- SPO_Content
localization_priority: Normal
f1.keywords:
- NOCSH
description: Découvrez comment déplacer un site SharePoint vers un autre emplacement géographique au sein de votre environnement multigéogé et communiquer les attentes des modifications à vos utilisateurs.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: eed323b2e2b8f68a4a603052657e17495bb17690
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50910929"
---
# <a name="move-a-sharepoint-site-to-a-different-geo-location"></a><span data-ttu-id="6e165-103">Déplacer un site SharePoint vers un autre emplacement géographique</span><span class="sxs-lookup"><span data-stu-id="6e165-103">Move a SharePoint site to a different geo location</span></span>

<span data-ttu-id="6e165-104">La fonctionnalité de déplacement géographique de site de SharePoint vous permet de déplacer des sites SharePoint sur d’autres emplacements géographiques au sein de votre environnement multigéographique.</span><span class="sxs-lookup"><span data-stu-id="6e165-104">With SharePoint site geo move, you can move SharePoint sites to other geo locations within your multi-geo environment.</span></span>

<span data-ttu-id="6e165-105">Les types de sites pouvant être déplacés entre emplacements géographiques sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="6e165-105">The following types of site can be moved between geo locations:</span></span>

- <span data-ttu-id="6e165-106">Sites connectés à un groupe Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="6e165-106">Microsoft 365 Group-connected sites</span></span>
- <span data-ttu-id="6e165-107">Sites modernes non associés à un groupe Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="6e165-107">Modern sites without a Microsoft 365 Group association</span></span>
- <span data-ttu-id="6e165-108">Sites SharePoint classiques</span><span class="sxs-lookup"><span data-stu-id="6e165-108">Classic SharePoint sites</span></span>
- <span data-ttu-id="6e165-109">Sites de communication</span><span class="sxs-lookup"><span data-stu-id="6e165-109">Communication sites</span></span>

<span data-ttu-id="6e165-110">Pour pouvoir déplacer un site, vous devez être un administrateur général ou un administrateur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6e165-110">You must be a Global Administrator or SharePoint Administrator to move a site between geo locations.</span></span>

<span data-ttu-id="6e165-111">Lors du déplacement géographique de site SharePoint, il existe une fenêtre en lecture seule d’environ 4 à 6 heures, selon le contenu du site.</span><span class="sxs-lookup"><span data-stu-id="6e165-111">There is a read-only window during the SharePoint site geo move of approximately 4-6 hours, depending on site contents.</span></span>

## <a name="best-practices"></a><span data-ttu-id="6e165-112">Meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="6e165-112">Best practices</span></span>

- <span data-ttu-id="6e165-113">Essayez d’effectuer un déplacement de site SharePoint sur un site de test pour vous familiariser avec la procédure.</span><span class="sxs-lookup"><span data-stu-id="6e165-113">Try a SharePoint site move on a test site to get familiar with the procedure.</span></span>
- <span data-ttu-id="6e165-114">Avant de planifier ou d’effectuer le déplacement, vérifiez si le site peut être déplacé.</span><span class="sxs-lookup"><span data-stu-id="6e165-114">Validate whether the site can be moved prior to scheduling or performing the move.</span></span>
- <span data-ttu-id="6e165-115">Autant que possible, planifiez les déplacements intersites en dehors des heures d’ouverture afin de réduire l’impact sur les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6e165-115">When possible schedule cross-geo sites moves for outside business hours to reduce user impact.</span></span>
- <span data-ttu-id="6e165-116">Avant de déplacer des sites, communiquez avec les utilisateurs concernés.</span><span class="sxs-lookup"><span data-stu-id="6e165-116">Communicate with impacted users prior to the sites move.</span></span>

## <a name="communicating-to-your-users"></a><span data-ttu-id="6e165-117">Communication avec vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6e165-117">Communicating to your users</span></span>

<span data-ttu-id="6e165-118">Lors du déplacement géographique de sites SharePoint, il est important d’indiquer aux utilisateurs des sites (généralement, toute personne ayant la possibilité de modifier le site) à quoi ils doivent s’attendre.</span><span class="sxs-lookup"><span data-stu-id="6e165-118">When moving SharePoint sites between geo locations, it's important to communicate to the sites' users (generally anyone with the ability to edit the site) what to expect.</span></span> <span data-ttu-id="6e165-119">Cela peut vous aider à atténuer la confusion des utilisateurs et les appels à votre support technique.</span><span class="sxs-lookup"><span data-stu-id="6e165-119">This can help reduce user confusion and calls to your help desk.</span></span> <span data-ttu-id="6e165-120">Avant de déplacer des sites, envoyez un courrier électronique à leurs utilisateurs pour leur communiquer les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6e165-120">Email your sites' users before the move and let them know the following information:</span></span>

- <span data-ttu-id="6e165-121">date de début et durée prévues du déplacement ;</span><span class="sxs-lookup"><span data-stu-id="6e165-121">When the move is expected to start and how long it is expected to take</span></span>
- <span data-ttu-id="6e165-122">emplacement géographique cible du déplacement et URL permettant d’accéder à ce nouvel emplacement ;</span><span class="sxs-lookup"><span data-stu-id="6e165-122">What geo location their site is moving to, and the URL to access the new location</span></span>
- <span data-ttu-id="6e165-123">nécessité de fermer les fichiers et de ne pas y apporter de modifications durant le déplacement ;</span><span class="sxs-lookup"><span data-stu-id="6e165-123">They should close their files and not make edits during the move.</span></span>
- <span data-ttu-id="6e165-124">absence de modification des autorisations et des partages de fichiers en raison du déplacement ;</span><span class="sxs-lookup"><span data-stu-id="6e165-124">File permissions and sharing will not change because of the move.</span></span>
- <span data-ttu-id="6e165-125">changement d’expérience utilisateur dans un environnement multigéographique.</span><span class="sxs-lookup"><span data-stu-id="6e165-125">What to expect from the user experience in a multi-geo environment</span></span>

<span data-ttu-id="6e165-126">Une fois le déplacement terminé, n’oubliez pas d’envoyer un courrier aux utilisateurs de vos sites pour les avertir qu’ils peuvent reprendre leur travail.</span><span class="sxs-lookup"><span data-stu-id="6e165-126">Be sure to send your sites' users an email when the move has successfully completed informing them that they can resume working on their sites.</span></span>

## <a name="scheduling-sharepoint-site-moves"></a><span data-ttu-id="6e165-127">Planification des déplacements de sites SharePoint</span><span class="sxs-lookup"><span data-stu-id="6e165-127">Scheduling SharePoint site moves</span></span>

<span data-ttu-id="6e165-128">Vous pouvez planifier les déplacements de sites SharePoint (voir plus loin dans cet article).</span><span class="sxs-lookup"><span data-stu-id="6e165-128">You can schedule SharePoint site moves in advance (described later in this article).</span></span> <span data-ttu-id="6e165-129">Vous pouvez planifier les déplacements comme suit :</span><span class="sxs-lookup"><span data-stu-id="6e165-129">You can schedule moves as follows:</span></span>

- <span data-ttu-id="6e165-130">Vous pouvez planifier jusqu’à 4 000 déplacements à la fois.</span><span class="sxs-lookup"><span data-stu-id="6e165-130">You can schedule up to 4,000 moves at a time.</span></span>
- <span data-ttu-id="6e165-131">Lorsque les déplacements commencent, vous pouvez planifier plus d’informations, avec un maximum de 4 000 déplacements dans la file d’attente et à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="6e165-131">As the moves begin, you can schedule more, with a maximum of 4,000 pending moves in the queue and any given time.</span></span>

<span data-ttu-id="6e165-132">Pour planifier un déplacement géographique de site SharePoint, lorsque vous commencez le déplacement, incluez parmi l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="6e165-132">To schedule a SharePoint site geo move for a later time, include one of the following parameters when you start the move:</span></span>

- <span data-ttu-id="6e165-133">`PreferredMoveBeginDate` – Le déplacement commencera probablement à l’heure indiquée.</span><span class="sxs-lookup"><span data-stu-id="6e165-133">`PreferredMoveBeginDate` – The move will likely begin at this specified time.</span></span>
- <span data-ttu-id="6e165-134">`PreferredMoveEndDate` – Le déplacement devrait être terminé à l’heure indiquée.</span><span class="sxs-lookup"><span data-stu-id="6e165-134">`PreferredMoveEndDate` – The move will likely be completed by this specified time, on a best effort basis.</span></span>

<span data-ttu-id="6e165-135">L’heure doit être exprimée en Temps universel coordonné (UTC) pour les deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="6e165-135">Time must be specified in Coordinated Universal Time (UTC) for both parameters.</span></span>

## <a name="moving-the-site"></a><span data-ttu-id="6e165-136">Déplacement du site</span><span class="sxs-lookup"><span data-stu-id="6e165-136">Moving the site</span></span>

<span data-ttu-id="6e165-137">Un déplacement géographique de site SharePoint nécessite que vous vous connectiez et opériez le déplacement de l’URL d’administration SharePoint vers l’emplacement géographique du site.</span><span class="sxs-lookup"><span data-stu-id="6e165-137">SharePoint site geo move requires that you connect and perform the move from the SharePoint Admin URL in the geo location where the site is.</span></span>

<span data-ttu-id="6e165-138">Par exemple, si l’URL du site est <https://contosohealthcare.sharepoint.com/sites/Turbines> , connectez-vous à l’URL d’administration SharePoint à <https://contosohealthcare-admin.sharepoint.com> l’adresse :</span><span class="sxs-lookup"><span data-stu-id="6e165-138">For example, if the site URL is <https://contosohealthcare.sharepoint.com/sites/Turbines>, connect to the SharePoint Admin URL at <https://contosohealthcare-admin.sharepoint.com>:</span></span>

```powershell
Connect-SPOService -Url https://contosohealthcare-admin.sharepoint.com
```

![Fenêtre SharePoint Online Management Shell affichant la commande Connect-SPOService commande](../media/move-onedrive-between-geo-locations-image1.png)

### <a name="validating-the-environment"></a><span data-ttu-id="6e165-140">Validation de l’environnement</span><span class="sxs-lookup"><span data-stu-id="6e165-140">Validating the environment</span></span>

<span data-ttu-id="6e165-141">Avant de planifier le déplacement d’un site, nous vous recommandons de vérifier que celui-ci peut être déplacé.</span><span class="sxs-lookup"><span data-stu-id="6e165-141">We recommend that before scheduling any site move, you perform a validation to ensure that the site can be moved.</span></span>

<span data-ttu-id="6e165-142">Il n’est pas possible de déplacer des sites avec :</span><span class="sxs-lookup"><span data-stu-id="6e165-142">We do not support moving sites with:</span></span>

- <span data-ttu-id="6e165-143">Business Connectivity Services</span><span class="sxs-lookup"><span data-stu-id="6e165-143">Business Connectivity Services</span></span>
- <span data-ttu-id="6e165-144">InfoPath Forms</span><span class="sxs-lookup"><span data-stu-id="6e165-144">InfoPath forms</span></span>
- <span data-ttu-id="6e165-145">Modèles d’IRM (Gestion des Droits relatifs à l’Information) appliqués</span><span class="sxs-lookup"><span data-stu-id="6e165-145">Information Rights Management (IRM) templates applied</span></span>

<span data-ttu-id="6e165-146">Pour vous assurer que tous les emplacements géographiques sont compatibles, exécutez la cmdlet `Get-SPOGeoMoveCrossCompatibilityStatus`.</span><span class="sxs-lookup"><span data-stu-id="6e165-146">To ensure all geo locations are compatible, run `Get-SPOGeoMoveCrossCompatibilityStatus`.</span></span> <span data-ttu-id="6e165-147">Cela a pour effet d’afficher les emplacements géographiques et d’indiquer si leur environnement est compatible avec l’emplacement géographique cible.</span><span class="sxs-lookup"><span data-stu-id="6e165-147">This will display all your geo locations and whether the environment is compatible with the destination geo location.</span></span>

<span data-ttu-id="6e165-148">Pour vérifier si votre site peut être déplacé, utilisez la cmdlet `Start-SPOSiteContentMove` avec le paramètre `-ValidationOnly`.</span><span class="sxs-lookup"><span data-stu-id="6e165-148">To perform a validation-only check on your site, use `Start-SPOSiteContentMove` with the `-ValidationOnly` parameter to validate if the site is able to be moved.</span></span> <span data-ttu-id="6e165-149">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6e165-149">For example:</span></span>

```PowerShell
Start-SPOSiteContentMove -SourceSiteUrl <SourceSiteUrl> -ValidationOnly -DestinationDataLocation <DestinationLocation>
```

<span data-ttu-id="6e165-150">Cette cmdlet retourne *Success* si le site peut être déplacé, ou *Fail* en cas de blocage du déplacement.</span><span class="sxs-lookup"><span data-stu-id="6e165-150">This will return *Success* if the site is ready to be moved or *Fail* if any of blocked conditions are present.</span></span>

### <a name="start-a-sharepoint-site-geo-move-for-a-site-with-no-associated-microsoft-365-group"></a><span data-ttu-id="6e165-151">Démarrer un déplacement géographique de site SharePoint sans groupe Microsoft 365 associé</span><span class="sxs-lookup"><span data-stu-id="6e165-151">Start a SharePoint site geo move for a site with no associated Microsoft 365 Group</span></span>

<span data-ttu-id="6e165-152">Par défaut, l’URL initiale du site est remplacée par l’URL de l’emplacement géographique cible.</span><span class="sxs-lookup"><span data-stu-id="6e165-152">By default, initial URL for the site will change to the URL of the destination geo location.</span></span> <span data-ttu-id="6e165-153">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6e165-153">For example:</span></span>

<span data-ttu-id="6e165-154"><https://Contoso.sharepoint.com/sites/projectx> devient <https://ContosoEUR.sharepoint.com/sites/projectx></span><span class="sxs-lookup"><span data-stu-id="6e165-154"><https://Contoso.sharepoint.com/sites/projectx> to <https://ContosoEUR.sharepoint.com/sites/projectx></span></span>

<span data-ttu-id="6e165-155">Quand un site est dépourvu d’association de groupe Microsoft 365, vous pouvez également le renommer à l’aide du paramètre `-DestinationUrl`.</span><span class="sxs-lookup"><span data-stu-id="6e165-155">For sites with no Microsoft 365 Group association, you can also rename the site by using the `-DestinationUrl` parameter.</span></span> <span data-ttu-id="6e165-156">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6e165-156">For example:</span></span>

<span data-ttu-id="6e165-157"><https://Contoso.sharepoint.com/sites/projectx> devient <https://ContosoEUR.sharepoint.com/sites/projecty></span><span class="sxs-lookup"><span data-stu-id="6e165-157"><https://Contoso.sharepoint.com/sites/projectx> to <https://ContosoEUR.sharepoint.com/sites/projecty></span></span>

<span data-ttu-id="6e165-158">Pour commencer à déplacer le site, exécutez la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="6e165-158">To start the site move, run:</span></span>

```powershell
Start-SPOSiteContentMove -SourceSiteUrl <siteURL> -DestinationDataLocation <DestinationDataLocation> -DestinationUrl <DestinationSiteURL>
```

![Capture d’écran de la fenêtre de PowerShell affichant la cmdlet Start-SPOSiteContentMove](../media/multi-geo-sharepoint-site-move-powershell.png)

### <a name="start-a-sharepoint-site-geo-move-for-a-microsoft-365-group-connected-site"></a><span data-ttu-id="6e165-160">Démarrer un déplacement géographique de site SharePoint connecté à un groupe Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="6e165-160">Start a SharePoint site geo move for a Microsoft 365 Group-connected site</span></span>

<span data-ttu-id="6e165-161">Pour déplacer un site connecté à un groupe Office 365, l’administrateur général ou l’administrateur SharePoint doivent commencer par modifier l’attribut d’emplacement de données favori (PDL) pour le groupe Office 365.</span><span class="sxs-lookup"><span data-stu-id="6e165-161">To move an Office 365 Group-connected site, the Global Administrator or SharePoint Administrator must first change the Preferred Data Location (PDL) attribute for the Office 365 Group.</span></span>

<span data-ttu-id="6e165-162">Pour définir l’emplacement par défaut des données pour un groupe Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="6e165-162">To set the PDL for a Microsoft 365 Group:</span></span>

```PowerShell
Set-SPOUnifiedGroup -PreferredDataLocation <PDL> -GroupAlias <GroupAlias>
Get-SPOUnifiedGroup -GroupAlias <GroupAlias>
```

<span data-ttu-id="6e165-163">Une fois l’emplacement par défaut des données mis à jour, vous pouvez commencer à déplacer le site :</span><span class="sxs-lookup"><span data-stu-id="6e165-163">Once you have updated the PDL, you can start the site move:</span></span>

```PowerShell
Start-SPOUnifiedGroupMove -GroupAlias <GroupAlias> -DestinationDataLocation <DestinationDataLocation>
```

## <a name="cancel-a-sharepoint-site-geo-move"></a><span data-ttu-id="6e165-164">Annuler un déplacement géographique de site SharePoint</span><span class="sxs-lookup"><span data-stu-id="6e165-164">Cancel a SharePoint site geo move</span></span>

<span data-ttu-id="6e165-165">Vous pouvez arrêter un déplacement géographique de site OneDrive, à la condition que ce déplacement ne soit pas en cours ou terminé, en utilisant la cmdlet `Stop-SPOSiteContentMove` :</span><span class="sxs-lookup"><span data-stu-id="6e165-165">You can stop a SharePoint site geo move, provided the move is not in progress or completed by using the `Stop-SPOSiteContentMove` cmdlet.</span></span>

## <a name="determining-the-status-of-a-sharepoint-site-geo-move"></a><span data-ttu-id="6e165-166">Détermination de l’état d’un déplacement géographique de site SharePoint</span><span class="sxs-lookup"><span data-stu-id="6e165-166">Determining the status of a SharePoint site geo move</span></span>

<span data-ttu-id="6e165-167">Vous pouvez déterminer l’état d’un déplacement de site hors de la zone géographique à laquelle vous êtes connecté à l’aide des cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="6e165-167">You can determine the status of a site move in our out of the geo that you are connected to by using the following cmdlets:</span></span>

- <span data-ttu-id="6e165-168">[Get-SPOSiteContentMoveState](/powershell/module/sharepoint-online/get-spositecontentmovestate) (sites non connectés à un groupe)</span><span class="sxs-lookup"><span data-stu-id="6e165-168">[Get-SPOSiteContentMoveState](/powershell/module/sharepoint-online/get-spositecontentmovestate) (non-Group-connected sites)</span></span>
- <span data-ttu-id="6e165-169">[Get-SPOUnifiedGroupMoveState](/powershell/module/sharepoint-online/get-spounifiedgroupmovestate) (sites connectés à un groupe)</span><span class="sxs-lookup"><span data-stu-id="6e165-169">[Get-SPOUnifiedGroupMoveState](/powershell/module/sharepoint-online/get-spounifiedgroupmovestate) (Group-connected sites)</span></span>

<span data-ttu-id="6e165-170">Pour spécifier le site dont vous voulez voir l’état de déplacement, utilisez le paramètre `-SourceSiteUrl`.</span><span class="sxs-lookup"><span data-stu-id="6e165-170">Use the `-SourceSiteUrl` parameter to specify the site for which you want to see move status.</span></span>

<span data-ttu-id="6e165-171">Les états de déplacement sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6e165-171">The move statuses are described in the following table.</span></span>

****

|<span data-ttu-id="6e165-172">Statut</span><span class="sxs-lookup"><span data-stu-id="6e165-172">Status</span></span>|<span data-ttu-id="6e165-173">Description</span><span class="sxs-lookup"><span data-stu-id="6e165-173">Description</span></span>|
|---|---|
|<span data-ttu-id="6e165-174">Ready to Trigger</span><span class="sxs-lookup"><span data-stu-id="6e165-174">Ready to Trigger</span></span>|<span data-ttu-id="6e165-175">Le déplacement n’a pas commencé.</span><span class="sxs-lookup"><span data-stu-id="6e165-175">The move has not started.</span></span>|
|<span data-ttu-id="6e165-176">Scheduled</span><span class="sxs-lookup"><span data-stu-id="6e165-176">Scheduled</span></span>|<span data-ttu-id="6e165-177">Le déplacement est en file d’attente mais n’a pas encore commencé.</span><span class="sxs-lookup"><span data-stu-id="6e165-177">The move is in queue but has not yet started.</span></span>|
|<span data-ttu-id="6e165-178">InProgress (n/4)</span><span class="sxs-lookup"><span data-stu-id="6e165-178">InProgress (n/4)</span></span>|<span data-ttu-id="6e165-179">Le déplacement est en cours dans l’un des états suivants : Validation (1/4), Sauvegarde (2/4), Restauration (3/4), Nettoyage (4/4).</span><span class="sxs-lookup"><span data-stu-id="6e165-179">The move is in progress in one of the following states: Validation (1/4), Backup (2/4), Restore (3/4), Cleanup (4/4).</span></span>|
|<span data-ttu-id="6e165-180">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="6e165-180">Success</span></span>|<span data-ttu-id="6e165-181">Le déplacement a réussi.</span><span class="sxs-lookup"><span data-stu-id="6e165-181">The move has completed successfully.</span></span>|
|<span data-ttu-id="6e165-182">Échec</span><span class="sxs-lookup"><span data-stu-id="6e165-182">Failed</span></span>|<span data-ttu-id="6e165-183">Le déplacement a échoué.</span><span class="sxs-lookup"><span data-stu-id="6e165-183">The move failed.</span></span>|
|

<span data-ttu-id="6e165-184">Vous pouvez également appliquer l’option `-Verbose` pour voir des informations supplémentaires sur le déplacement.</span><span class="sxs-lookup"><span data-stu-id="6e165-184">You can also apply the `-Verbose` option to see additional information about the move.</span></span>

## <a name="user-experience"></a><span data-ttu-id="6e165-185">Expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="6e165-185">User experience</span></span>

<span data-ttu-id="6e165-186">Les utilisateurs du site devraient constater une perturbation minimale lors du déplacement géographique du site.</span><span class="sxs-lookup"><span data-stu-id="6e165-186">Site users should notice minimal disruption when their site is moved to a different geo location.</span></span> <span data-ttu-id="6e165-187">À l’exception d’un bref état en lecture seule lors du déplacement, les liens et autorisations existants continuent de fonctionner comme prévu après le déplacement.</span><span class="sxs-lookup"><span data-stu-id="6e165-187">Aside from a brief read-only state during the move, existing links and permissions will continue to work as expected once the move is completed.</span></span>

### <a name="site"></a><span data-ttu-id="6e165-188">Site</span><span class="sxs-lookup"><span data-stu-id="6e165-188">Site</span></span>

<span data-ttu-id="6e165-189">Durant le déplacement, le site est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6e165-189">While the move is in progress the site is set to read-only.</span></span> <span data-ttu-id="6e165-190">Une fois le déplacement terminé, l’utilisateur est redirigé vers le nouveau site dans le nouvel emplacement géographique quand il clique sur des signets ou d’autres liens pointant sur le site.</span><span class="sxs-lookup"><span data-stu-id="6e165-190">Once the move is completed, the user is directed to the new site in the new geo location when they click on bookmarks or other links to the site.</span></span>

### <a name="permissions"></a><span data-ttu-id="6e165-191">Autorisations</span><span class="sxs-lookup"><span data-stu-id="6e165-191">Permissions</span></span>

<span data-ttu-id="6e165-192">Les utilisateurs disposant d’autorisations d’accès au site continuent de pouvoir y accéder durant et après le déplacement.</span><span class="sxs-lookup"><span data-stu-id="6e165-192">Users with permissions to site will continue to have access to the site during the move and after it's complete.</span></span>

### <a name="sync-client"></a><span data-ttu-id="6e165-193">Client de synchronisation</span><span class="sxs-lookup"><span data-stu-id="6e165-193">Sync Client</span></span>

<span data-ttu-id="6e165-194">Le client de synchronisation détecte et transfère automatiquement la synchronisation vers le nouvel emplacement du site une fois celui-ci déplacé.</span><span class="sxs-lookup"><span data-stu-id="6e165-194">The sync client will automatically detect and seamlessly transfer syncing to the new site location once the site move is complete.</span></span> <span data-ttu-id="6e165-195">L’utilisateur n’a pas besoin de se reconnecter ou d’effectuer un autre action</span><span class="sxs-lookup"><span data-stu-id="6e165-195">The user does not need to sign in again or take any other action.</span></span> <span data-ttu-id="6e165-196">(version 17.3.6943.0625 ou une version ultérieure du client de synchronisation requise).</span><span class="sxs-lookup"><span data-stu-id="6e165-196">(Version 17.3.6943.0625 or later of the sync client required.)</span></span>

<span data-ttu-id="6e165-197">Si un utilisateur met à jour un fichier pendant le déplacement, le client de synchronisation l’informe que les chargements de fichiers sont mis en attente pendant le déplacement.</span><span class="sxs-lookup"><span data-stu-id="6e165-197">If a user updates a file while the move is in progress, the sync client will notify them that file uploads are pending while the move is underway.</span></span>

### <a name="sharing-links"></a><span data-ttu-id="6e165-198">Partage des liens</span><span class="sxs-lookup"><span data-stu-id="6e165-198">Sharing links</span></span>

<span data-ttu-id="6e165-199">Une fois le déplacement géographique de site OneDrive terminé, les liens partagés existants vers les fichiers déplacés redirigent automatiquement vers le nouvel emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="6e165-199">When the SharePoint site geo move completes, the existing shared links for the files that were moved will automatically redirect to the new geo location.</span></span>

### <a name="most-recently-used-files-in-office-mru"></a><span data-ttu-id="6e165-200">Fichiers récents dans Office</span><span class="sxs-lookup"><span data-stu-id="6e165-200">Most Recently Used files in Office (MRU)</span></span>

<span data-ttu-id="6e165-201">Une fois le déplacement terminé, le service Fichiers récents est mis à jour avec l’URL du site et les URL de son contenu.</span><span class="sxs-lookup"><span data-stu-id="6e165-201">The MRU service is updated with the site url and its content URLs once the move completes.</span></span> <span data-ttu-id="6e165-202">Cela vaut pour Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="6e165-202">This applies to Word, Excel, and PowerPoint.</span></span>

### <a name="onenote-experience"></a><span data-ttu-id="6e165-203">Expérience OneNote</span><span class="sxs-lookup"><span data-stu-id="6e165-203">OneNote experience</span></span>

<span data-ttu-id="6e165-204">Le client OneNote Win32 et l’application UWP (plateforme Windows universelle) détectent et synchronisent automatiquement et sans difficulté les blocs-notes sur le nouvel emplacement du site une fois celui-ci déplacé.</span><span class="sxs-lookup"><span data-stu-id="6e165-204">OneNote win32 client and UWP (Universal) App will automatically detect and seamlessly sync notebooks to the new site location once site move is complete.</span></span> <span data-ttu-id="6e165-205">L’utilisateur n’a pas besoin de se reconnecter ou d’effectuer un autre action.</span><span class="sxs-lookup"><span data-stu-id="6e165-205">The user does not need to sign in again or take any other action.</span></span> <span data-ttu-id="6e165-206">Le seul indicateur pour l’utilisateur est un échec éventuel de synchronisation de bloc-notes durant le déplacement du site.</span><span class="sxs-lookup"><span data-stu-id="6e165-206">The only visible indicator to the user is notebook sync would fail when site move is in progress.</span></span> <span data-ttu-id="6e165-207">Cette expérience est disponible sur les versions suivantes du client OneNote :</span><span class="sxs-lookup"><span data-stu-id="6e165-207">This experience is available on the following OneNote client versions:</span></span>

- <span data-ttu-id="6e165-208">OneNote win32 – Version 16.0.8326.2096 (et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="6e165-208">OneNote win32 – Version 16.0.8326.2096 (and later)</span></span>
- <span data-ttu-id="6e165-209">OneNote UWP – Version 16.0.8431.1006 (et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="6e165-209">OneNote UWP – Version 16.0.8431.1006 (and later)</span></span>
- <span data-ttu-id="6e165-210">Application mobile OneNote : Version 16.0.8431.1011 (et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="6e165-210">OneNote Mobile App – Version 16.0.8431.1011 (and later)</span></span>

### <a name="teams-applicable-to-microsoft-365-group-connected-sites"></a><span data-ttu-id="6e165-211">Microsoft Teams (applicable aux sites connectés à un groupe Microsoft 365)</span><span class="sxs-lookup"><span data-stu-id="6e165-211">Teams (applicable to Microsoft 365 Group connected sites)</span></span>

<span data-ttu-id="6e165-212">Une fois le déplacement géographique de site SharePoint terminé, les utilisateurs ont accès aux fichiers du site de groupe Microsoft 365 sur leur application Teams.</span><span class="sxs-lookup"><span data-stu-id="6e165-212">When the SharePoint site geo move completes, users will have access to their Microsoft 365 Group site files on the Teams app.</span></span> <span data-ttu-id="6e165-213">Par ailleurs, les fichiers partagés via une conversation Teams à partir de leur site avant le déplacement géographique continuent également de fonctionner après le déplacement.</span><span class="sxs-lookup"><span data-stu-id="6e165-213">Additionally, files shared via Teams chat from their site prior to geo move will continue to work after move is complete.</span></span>

### <a name="sharepoint-mobile-app-iosandroid"></a><span data-ttu-id="6e165-214">Application SharePoint Mobile (iOS/Android)</span><span class="sxs-lookup"><span data-stu-id="6e165-214">SharePoint Mobile App (iOS/Android)</span></span>

<span data-ttu-id="6e165-215">L’application SharePoint Mobile étant inter-géographique, elle est capable de détecter le nouvel emplacement géographique du site.</span><span class="sxs-lookup"><span data-stu-id="6e165-215">The SharePoint Mobile App is cross geo compatible and able to detect the site's new geo location.</span></span>

### <a name="sharepoint-workflows"></a><span data-ttu-id="6e165-216">Flux de travail SharePoint</span><span class="sxs-lookup"><span data-stu-id="6e165-216">SharePoint workflows</span></span>

<span data-ttu-id="6e165-217">Les flux de travail SharePoint 2013 doivent être republiés une fois le site déplacé.</span><span class="sxs-lookup"><span data-stu-id="6e165-217">SharePoint 2013 workflows need to be republished after the site move.</span></span> <span data-ttu-id="6e165-218">Les flux de travail SharePoint 2010 devraient continuer de fonctionner normalement.</span><span class="sxs-lookup"><span data-stu-id="6e165-218">SharePoint 2010 workflows should continue to function normally.</span></span>

### <a name="apps"></a><span data-ttu-id="6e165-219">Applications</span><span class="sxs-lookup"><span data-stu-id="6e165-219">Apps</span></span>

<span data-ttu-id="6e165-220">Si vous migrez un site comportant des applications, vous devez ré-instancier celles-ci dans le nouvel emplacement géographique du site, car les applications et leurs liens pourraient ne pas être disponibles dans l’emplacement géographique cible.</span><span class="sxs-lookup"><span data-stu-id="6e165-220">If you are moving a site with apps, you must re-instantiate the app in the site's new geo location as the app and its connections may not be available in the destination geo location.</span></span>

### <a name="flow"></a><span data-ttu-id="6e165-221">Flux</span><span class="sxs-lookup"><span data-stu-id="6e165-221">Flow</span></span>

<span data-ttu-id="6e165-222">Dans la plupart des cas, les flux continueront de fonctionner après un déplacement géographique de site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6e165-222">In most cases Flows will continue to work after a SharePoint site geo move.</span></span> <span data-ttu-id="6e165-223">Nous vous conseillons de les tester une fois le déplacement terminé.</span><span class="sxs-lookup"><span data-stu-id="6e165-223">We recommend that you test them once the move has completed.</span></span>

### <a name="powerapps"></a><span data-ttu-id="6e165-224">PowerApps</span><span class="sxs-lookup"><span data-stu-id="6e165-224">PowerApps</span></span>

<span data-ttu-id="6e165-225">Les applications PowerApps doivent être recréées dans l’emplacement cible.</span><span class="sxs-lookup"><span data-stu-id="6e165-225">PowerApps need to be recreated in the destination location.</span></span>

### <a name="data-movement-between-geo-locations"></a><span data-ttu-id="6e165-226">Déplacement de données entre emplacements géographiques</span><span class="sxs-lookup"><span data-stu-id="6e165-226">Data movement between geo locations</span></span>

<span data-ttu-id="6e165-227">SharePoint utilise Stockage Blob Azure pour son contenu, tandis que les métadonnées associés à des sites et à ses fichiers sont stockées dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6e165-227">SharePoint uses Azure Blob storage for its content, while the metadata associated with sites and its files is stored within SharePoint.</span></span> <span data-ttu-id="6e165-228">Le déplacement du site de son emplacement géographique source vers son emplacement géographique cible implique également le déplacement de son Stockage Blob.</span><span class="sxs-lookup"><span data-stu-id="6e165-228">After the site is moved from its source geo location to its destination geo location, the service will also move its associated Blob Storage.</span></span> <span data-ttu-id="6e165-229">Le déplacement du Stockage Blob prend environ 40 jours.</span><span class="sxs-lookup"><span data-stu-id="6e165-229">Blob Storage moves complete in approximately 40 days.</span></span>