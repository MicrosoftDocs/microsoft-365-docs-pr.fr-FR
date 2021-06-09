---
title: Déplacer un site OneDrive vers un autre emplacement géographique
ms.reviewer: adwood
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: o365-solutions
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
ms.collection:
- Strat_SP_gtc
- SPO_Content
localization_priority: Normal
description: Trouvez des informations sur le déplacement d’un site OneDrive vers un autre emplacement géographique, notamment sur la planification des déplacements de sites et la communication des attentes aux utilisateurs.
ms.openlocfilehash: 59b3fb47fd195967e7af056c7a71fb4e736471d1
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689593"
---
# <a name="move-a-onedrive-site-to-a-different-geo-location"></a><span data-ttu-id="6a0f7-103">Déplacer un site OneDrive vers un autre emplacement géographique</span><span class="sxs-lookup"><span data-stu-id="6a0f7-103">Move a OneDrive site to a different geo location</span></span> 

<span data-ttu-id="6a0f7-104">Avec OneDrive géolocalisation, vous pouvez déplacer les données d’un OneDrive vers un autre emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-104">With OneDrive geo move, you can move a user's OneDrive to a different geo location.</span></span> <span data-ttu-id="6a0f7-105">OneDrive le déplacement géographique est effectué par l’administrateur SharePoint Online ou l’administrateur Microsoft 365 général.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-105">OneDrive geo move is performed by the SharePoint Online administrator or the Microsoft 365 global administrator.</span></span> <span data-ttu-id="6a0f7-106">Avant de commencer un déplacement géographique OneDrive, n’oubliez pas d’avertir l’utilisateur dont le OneDrive est déplacé et de lui recommander de fermer tous les fichiers pendant toute la durée du déplacement.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-106">Before you start a OneDrive geo move, be sure to notify the user whose OneDrive is being moved and recommend they close all files for the duration of the move.</span></span> <span data-ttu-id="6a0f7-107">(Si un document est ouvert par l’utilisateur à l’aide du client Office pendant le déplacement, le document doit être enregistré au nouvel emplacement une fois le déplacement terminé.) Le déplacement peut être programmé ultérieurement, si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-107">(If the user has a document open using the Office client during the move, then upon move completion the document will need to be saved to the new location.) The move can be scheduled for a future time, if desired.</span></span>

<span data-ttu-id="6a0f7-108">Le service OneDrive utilise Azure Blob Stockage pour stocker du contenu.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-108">The OneDrive service uses Azure Blob Storage to store content.</span></span> <span data-ttu-id="6a0f7-109">Le Stockage blob associé au OneDrive de l’utilisateur sera déplacé de la source vers l’emplacement géographique de destination dans les 40 jours suivant la OneDrive de destination disponible pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-109">The Storage blob associated with the user's OneDrive will be moved from the source to destination geo location within 40 days of destination OneDrive being available to the user.</span></span> <span data-ttu-id="6a0f7-110">L’accès à la OneDrive de l’utilisateur est restauré dès que la OneDrive de destination est disponible.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-110">The access to the user's OneDrive will be restored as soon as the destination OneDrive is available.</span></span>

<span data-ttu-id="6a0f7-p103">Pendant la durée du déplacement géographique du site OneDrive (environ 2 à 6 heures), le site OneDrive de l’utilisateur est défini en lecture seule. L’utilisateur peut toujours accéder à ses fichiers via le client de synchronisation OneDrive ou son site OneDrive dans SharePoint Online. Une fois le déplacement géographique du site OneDrive terminé, l’utilisateur est connecté automatiquement à son site OneDrive à l’emplacement géographique de destination lorsqu’il navigue vers OneDrive dans le lanceur d’applications Microsoft 365. Le client de synchronisation commence automatiquement la synchronisation à partir du nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-p103">During OneDrive geo move window (about 2-6 hours) the user's OneDrive is set to read-only. The user can still access their files via the OneDrive sync client or their OneDrive site in SharePoint Online. After OneDrive geo move is complete, the user will be automatically connected to their OneDrive at the destination geo location when they navigate to OneDrive in the Microsoft 365 app launcher. The sync client will automatically begin syncing from the new location.</span></span>

<span data-ttu-id="6a0f7-115">Les procédures décrites dans cet article nécessitent le [module Microsoft SharePoint Online PowerShell](https://www.microsoft.com/download/details.aspx?id=35588).</span><span class="sxs-lookup"><span data-stu-id="6a0f7-115">The procedures in this article require the [Microsoft SharePoint Online PowerShell Module](https://www.microsoft.com/download/details.aspx?id=35588).</span></span>

## <a name="communicating-to-your-users"></a><span data-ttu-id="6a0f7-116">Communication avec vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6a0f7-116">Communicating to your users</span></span>

<span data-ttu-id="6a0f7-p104">Lors du déplacement de sites OneDrive entre différents emplacements géographiques, il est important de communiquer à vos utilisateurs ce à quoi ils doivent s’attendre. Cela peut vous aider à réduire la confusion des utilisateurs et diminuer le nombre d’appels à votre support technique. Prévenez vos utilisateurs par courriel avant le déplacement et faites-leur part des informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6a0f7-p104">When moving OneDrive sites between geo locations, it's important to communicate to your users what to expect. This can help reduce user confusion and calls to your help desk. Email your users before the move and let them know the following information:</span></span>

- <span data-ttu-id="6a0f7-120">La date de début prévue du déplacement et la durée attendue de l’opération.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-120">When the move is expected to start and how long it is expected to take</span></span>
- <span data-ttu-id="6a0f7-121">L’emplacement géographique vers lequel est déplacé leur espace OneDrive et l’URL permettant d’accéder au nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-121">What geo location their OneDrive is moving to, and the URL to access the new location</span></span>
- <span data-ttu-id="6a0f7-122">Conseillez-leur de fermer leurs fichiers et de ne pas y apporter de modifications lors du déplacement.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-122">They should close their files and not make edits during the move.</span></span>
- <span data-ttu-id="6a0f7-123">Le partage et les autorisations de fichiers ne sont modifiés par la migration.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-123">File permissions and sharing will not change as a result of the move.</span></span>
- <span data-ttu-id="6a0f7-124">Présentez-leur l’[expérience utilisateur dans un environnement multigéographique](multi-geo-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="6a0f7-124">What to expect from the [user experience in a multi-geo environment](multi-geo-user-experience.md)</span></span>

<span data-ttu-id="6a0f7-125">N’oubliez pas d’envoyer un courrier électronique à vos utilisateurs une fois le déplacement terminé pour les avertir qu’ils peuvent reprendre leur travail dans OneDrive.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-125">Be sure to send your users an email when the move has successfully completed informing them that they can resume working in OneDrive.</span></span>

## <a name="scheduling-onedrive-site-moves"></a><span data-ttu-id="6a0f7-126">Planification de déplacements de site OneDrive</span><span class="sxs-lookup"><span data-stu-id="6a0f7-126">Scheduling OneDrive site moves</span></span>

<span data-ttu-id="6a0f7-p105">Vous pouvez planifier les déplacements de site OneDrive à l’avance (décrit plus loin dans cet article). Nous vous recommandons de commencer avec un petit nombre d’utilisateurs pour valider vos stratégies de communication et de flux de travail. Une fois que vous êtes habitué au processus, vous pouvez planifier des déplacements comme suit :</span><span class="sxs-lookup"><span data-stu-id="6a0f7-p105">You can schedule OneDrive site moves in advance (described later in this article). We recommend that you start with a small number of users to validate your workflows and communication strategies. Once you are comfortable with the process, you can schedule moves as follows:</span></span>

- <span data-ttu-id="6a0f7-130">Vous pouvez planifier jusqu’à 4 000 déplacements à la fois.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-130">You can schedule up to 4,000 moves at a time.</span></span>
- <span data-ttu-id="6a0f7-131">Lorsque les déplacements commencent, vous pouvez planifier plus d’informations, avec un maximum de 4 000 déplacements dans la file d’attente et à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-131">As the moves begin, you can schedule more, with a maximum of 4,000 pending moves in the queue and any given time.</span></span>
- <span data-ttu-id="6a0f7-132">La taille maximale d’un élément pouvant être déplacé par OneDrive est de 1 téraoctet (1 to).</span><span class="sxs-lookup"><span data-stu-id="6a0f7-132">The maximum size of a OneDrive that can be moved is 1 terabyte (1 TB).</span></span>

## <a name="moving-a-onedrive-site"></a><span data-ttu-id="6a0f7-133">Déplacement d’un site OneDrive</span><span class="sxs-lookup"><span data-stu-id="6a0f7-133">Moving a OneDrive site</span></span>

<span data-ttu-id="6a0f7-134">Pour effectuer un OneDrive géographique, l’administrateur client doit d’abord définir l’emplacement par choix par utilisateur (PDL) sur l’emplacement géographique approprié.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-134">To perform a OneDrive geo move, the tenant administrator must first set the user's Preferred Data Location (PDL) to the appropriate geo location.</span></span> <span data-ttu-id="6a0f7-135">Une fois la PDL définie, attendez au moins 24 heures que la mise à jour PDL soit synchronisée entre les emplacements géographiques avant de commencer le OneDrive géo.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-135">Once the PDL is set, wait for at least 24 hours for the PDL update to sync across the geo locations before starting the OneDrive geo move.</span></span>

<span data-ttu-id="6a0f7-136">Lorsque vous utilisez les cmdlets de déplacement géographique, connectez-vous au service SPO à l’emplacement OneDrive l’emplacement géographique actuel de l’utilisateur, à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6a0f7-136">When using the geo move cmdlets, connect to SPO Service at the user's current OneDrive geo location, using the following syntax:</span></span>

`Connect-SPOService -url https://<tenantName>-admin.sharepoint.com`

<span data-ttu-id="6a0f7-137">Par exemple : pour déplacer OneDrive de l’utilisateur « Matt@contosoenergy.onmicrosoft.com » , connectez-vous au Centre d’administration EUR SharePoint car le OneDrive de l’utilisateur se trouve dans l’emplacement géographique EUR :</span><span class="sxs-lookup"><span data-stu-id="6a0f7-137">For example: To move OneDrive of user 'Matt@contosoenergy.onmicrosoft.com', connect to EUR SharePoint Admin center as the user's OneDrive is in EUR geo location:</span></span>

`Connect-SPOSservice -url https://contosoenergyeur-admin.sharepoint.com`

![Capture d’écran d’une fenêtre PowerShell affichant la cmdlet connect-sposervice](../media/move-onedrive-between-geo-locations-image1.png)

## <a name="validating-the-environment"></a><span data-ttu-id="6a0f7-139">Validation de l’environnement</span><span class="sxs-lookup"><span data-stu-id="6a0f7-139">Validating the environment</span></span>

<span data-ttu-id="6a0f7-140">Avant de commencer un déplacement géographique OneDrive, nous vous recommandons de valider l’environnement.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-140">Before you start a OneDrive geo move, we recommend that you validate the environment.</span></span>

<span data-ttu-id="6a0f7-141">Pour vous assurer que tous les emplacements géographiques sont compatibles, exécutez :</span><span class="sxs-lookup"><span data-stu-id="6a0f7-141">To ensure that all geo locations are compatible, run:</span></span>

`Get-SPOGeoMoveCrossCompatibilityStatus`

<span data-ttu-id="6a0f7-142">Une liste de vos emplacements géographiques s’affichera et le contenu que vous pourrez déplacer entre ces emplacements sera marqué « Compatible ».</span><span class="sxs-lookup"><span data-stu-id="6a0f7-142">You will see a list of your geo locations and whether content can be moved between will be denoted as "Compatible".</span></span> <span data-ttu-id="6a0f7-143">Si la commande renvoie « Incompatible », réessayez de valider l’état plus tard.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-143">If the command returns "Incompatible" please retry validating the status at a later date.</span></span>

<span data-ttu-id="6a0f7-144">Si un OneDrive contient, par exemple, un sous-site, il ne peut pas être déplacé.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-144">If a OneDrive contains a subsite, for example, it cannot be moved.</span></span> <span data-ttu-id="6a0f7-145">Vous pouvez utiliser la cmdlet Start-SPOUserAndContentMove avec le paramètre -ValidationOnly pour contrôler si le site OneDrive peut être déplacé :</span><span class="sxs-lookup"><span data-stu-id="6a0f7-145">You can use the Start-SPOUserAndContentMove cmdlet with the -ValidationOnly parameter to validate if the OneDrive is able to be moved:</span></span>

`Start-SPOUserAndContentMove -UserPrincipalName <UPN> -DestinationDataLocation <DestinationDataLocation> -ValidationOnly`

<span data-ttu-id="6a0f7-p109">Ceci renvoie Opération réussie si le site OneDrive est prêt à être déplacé ou Échec s’il existe une conservation légale ou un sous-site qui empêche le déplacement. Une fois que vous avez contrôlé que le site OneDrive est prêt à être déplacé, vous pouvez commencer le déplacement.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-p109">This will return Success if the OneDrive is ready to be moved or Fail if there is a legal hold or subsite that would prevent the move. Once you have validated that the OneDrive is ready to move, you can start the move.</span></span>

## <a name="start-a-onedrive-geo-move"></a><span data-ttu-id="6a0f7-148">Démarrer un déplacement géographique OneDrive</span><span class="sxs-lookup"><span data-stu-id="6a0f7-148">Start a OneDrive geo move</span></span>

<span data-ttu-id="6a0f7-149">Pour démarrer le déplacement, exécutez :</span><span class="sxs-lookup"><span data-stu-id="6a0f7-149">To start the move, run:</span></span>  

`Start-SPOUserAndContentMove -UserPrincipalName <UserPrincipalName> -DestinationDataLocation <DestinationDataLocation>`

<span data-ttu-id="6a0f7-150">À l’aide de ces paramètres :</span><span class="sxs-lookup"><span data-stu-id="6a0f7-150">Using these parameters:</span></span>

-   <span data-ttu-id="6a0f7-151">_UserPrincipalName_ : UPN de l’utilisateur dont le site OneDrive est déplacé.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-151">_UserPrincipalName_ – UPN of the user whose OneDrive is being moved.</span></span>

-   <span data-ttu-id="6a0f7-152">_DestinationDataLocation_ : Geo-Location où le OneDrive doit être déplacé.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-152">_DestinationDataLocation_ – Geo-Location where the OneDrive needs to be moved.</span></span> <span data-ttu-id="6a0f7-153">Il doit être identique à l’emplacement de données préféré de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-153">This should be same as the user's preferred data location.</span></span>

<span data-ttu-id="6a0f7-154">Par exemple, pour déplacer le site OneDrive de matt@contosoenergy.onmicrosoft.com de l’emplacement EUR à AUS, exécutez :</span><span class="sxs-lookup"><span data-stu-id="6a0f7-154">For example, to move the OneDrive of matt@contosoenergy.onmicrosoft.com from EUR to AUS, run:</span></span>

`Start-SPOUserAndContentMove -UserPrincipalName matt@contosoenergy.onmicrosoft.com -DestinationDataLocation AUS`

![Capture d’écran de la fenêtre PowerShell affichant la cmdlet Start-SPOUserAndContentMove](../media/move-onedrive-between-geo-locations-image2.png)

<span data-ttu-id="6a0f7-156">Pour planifier un déplacement géographique à un autre moment, utilisez l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="6a0f7-156">To schedule a geo move for a later time, use one of the following parameters:</span></span>

-   <span data-ttu-id="6a0f7-p111">_PreferredMoveBeginDate_ : le déplacement commencera probablement à l’heure spécifiée. L’heure doit être spécifiée en Temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="6a0f7-p111">_PreferredMoveBeginDate_ – The move will likely begin at this specified time. Time must be specified in Coordinated Universal Time (UTC).</span></span>

-   <span data-ttu-id="6a0f7-p112">_PreferredMoveEndDate_ : le déplacement se terminera probablement d’ici l’heure spécifiée, dans la mesure du possible. L’heure doit être spécifiée en Temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="6a0f7-p112">_PreferredMoveEndDate_ – The move will likely be completed by this specified time, on a best effort basis. Time must be specified in Coordinated Universal Time (UTC).</span></span> 

## <a name="cancel-a-onedrive-geo-move"></a><span data-ttu-id="6a0f7-161">Annuler un déplacement géographique OneDrive</span><span class="sxs-lookup"><span data-stu-id="6a0f7-161">Cancel a OneDrive geo move</span></span> 

<span data-ttu-id="6a0f7-162">Vous pouvez arrêter le déplacement géographique du OneDrive d’un utilisateur, à condition que le déplacement ne soit pas en cours ou terminé à l’aide de la cmdlet :</span><span class="sxs-lookup"><span data-stu-id="6a0f7-162">You can stop the geo move of a user's OneDrive, provided the move is not in progress or completed by using the cmdlet:</span></span>

`Stop-SPOUserAndContentMove – UserPrincipalName <UserPrincipalName>`

<span data-ttu-id="6a0f7-163">où _UserPrincipalName_ est l’UPN de l’utilisateur dont vous souhaitez arrêter le déplacement du site OneDrive.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-163">Where _UserPrincipalName_ is the UPN of the user whose OneDrive move you want to stop.</span></span>

## <a name="determining-current-status"></a><span data-ttu-id="6a0f7-164">Déterminer l’état actuel</span><span class="sxs-lookup"><span data-stu-id="6a0f7-164">Determining current status</span></span>

<span data-ttu-id="6a0f7-165">Vous pouvez vérifier l’état d’une OneDrive géographique à l’entrée ou à la sortie de la géo à qui vous êtes connecté à l’aide de l'Get-SPOUserAndContentMoveState de données.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-165">You can check the status of a OneDrive geo move in or out of the geo that you're connected to by using the Get-SPOUserAndContentMoveState cmdlet.</span></span>

<span data-ttu-id="6a0f7-166">Ces états de déplacement sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-166">The move statuses are described in the following table.</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a0f7-167"><strong>État</strong></span><span class="sxs-lookup"><span data-stu-id="6a0f7-167"><strong>Status</strong></span></span></th>
<th align="left"><span data-ttu-id="6a0f7-168"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="6a0f7-168"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="6a0f7-169">NotStarted</span><span class="sxs-lookup"><span data-stu-id="6a0f7-169">NotStarted</span></span></td>
<td align="left"><span data-ttu-id="6a0f7-170">Le déplacement n’a pas commencé.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-170">The move has not started.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="6a0f7-171">InProgress (<em>n</em>/4)</span><span class="sxs-lookup"><span data-stu-id="6a0f7-171">InProgress (<em>n</em>/4)</span></span></td>
<td align="left"><span data-ttu-id="6a0f7-172">Le déplacement est en cours dans l’un des états suivants : Validation (1/4), Sauvegarde (2/4), Restauration (3/4), Nettoyage (4/4).</span><span class="sxs-lookup"><span data-stu-id="6a0f7-172">The move is in progress in one of the following states: Validation (1/4), Backup (2/4), Restore (3/4), Cleanup (4/4).</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="6a0f7-173">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="6a0f7-173">Success</span></span></td>
<td align="left"><span data-ttu-id="6a0f7-174">Le déplacement a réussi.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-174">The move has completed successfully.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="6a0f7-175">Échec</span><span class="sxs-lookup"><span data-stu-id="6a0f7-175">Failed</span></span></td>
<td align="left"><span data-ttu-id="6a0f7-176">Le déplacement a échoué.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-176">The move failed.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6a0f7-177">Pour rechercher l’état du déplacement d’un utilisateur spécifique, utilisez le paramètre UserPrincipalName :</span><span class="sxs-lookup"><span data-stu-id="6a0f7-177">To find the status of a specific user's move, use the UserPrincipalName parameter:</span></span>

`Get-SPOUserAndContentMoveState -UserPrincipalName <UPN>`

<span data-ttu-id="6a0f7-178">Pour rechercher l’état de tous les déplacements à l’intérieur ou à l’écart de l’emplacement géographique à qui vous êtes connecté, utilisez le paramètre MoveState avec l’une des valeurs suivantes : NotStarted, InProgress, Success, Failed, All.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-178">To find the status of all of the moves in or out of the geo location that you're connected to, use the MoveState parameter with one of the following values: NotStarted, InProgress, Success, Failed, All.</span></span>

`Get-SPOUserAndContentMoveState -MoveState <value>`

<span data-ttu-id="6a0f7-179">Vous pouvez également ajouter le paramètre `-Verbose` pour des descriptions plus détaillées de l’état de déplacement.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-179">You can also add the `-Verbose` parameter for more verbose descriptions of the move state.</span></span>

## <a name="user-experience"></a><span data-ttu-id="6a0f7-180">Expérience de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="6a0f7-180">User Experience</span></span>

<span data-ttu-id="6a0f7-p113">Les utilisateurs de OneDrive devraient observer des perturbations minimales si leur site OneDrive est déplacé vers un autre emplacement géographique. Excepté un état de lecture seule bref lors du déplacement, les autorisations et liens existants continueront à fonctionner comme prévu une fois le déplacement terminé.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-p113">Users of OneDrive should notice minimal disruption if their OneDrive is moved to a different geo location. Aside from a brief read-only state during the move, existing links and permissions will continue to work as expected once the move is completed.</span></span>

### <a name="onedrive-for-business"></a><span data-ttu-id="6a0f7-183">OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="6a0f7-183">OneDrive for Business</span></span>

<span data-ttu-id="6a0f7-184">Lorsque le déplacement est en cours, la OneDrive de l’utilisateur est définie en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-184">While the move is in progress the user's OneDrive is set to read-only.</span></span> <span data-ttu-id="6a0f7-185">Une fois le déplacement terminé, l’utilisateur est dirigé vers son OneDrive dans le nouvel emplacement géographique lorsqu’il navigue vers OneDrive le lanceur d’applications Microsoft 365 ou un navigateur web.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-185">Once the move is completed, the user is directed to their OneDrive in the new geo location when they navigate to OneDrive the Microsoft 365 app launcher or a web browser.</span></span>

### <a name="permissions-on-onedrive-content"></a><span data-ttu-id="6a0f7-186">Autorisations sur le contenu OneDrive</span><span class="sxs-lookup"><span data-stu-id="6a0f7-186">Permissions on OneDrive content</span></span>

<span data-ttu-id="6a0f7-187">Les utilisateurs autorisé à OneDrive contenu continueront d’avoir accès au contenu pendant le déplacement et une fois qu’il est terminé.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-187">Users with permissions to OneDrive content will continue to have access to the content during the move and after it's complete.</span></span>

### <a name="onedrive-sync-client"></a><span data-ttu-id="6a0f7-188">Client de synchronisation OneDrive</span><span class="sxs-lookup"><span data-stu-id="6a0f7-188">OneDrive Sync Client</span></span> 

<span data-ttu-id="6a0f7-p115">Le client de synchronisation OneDrive détecte automatiquement la synchronisation avec le nouvel emplacement OneDrive et la transfère en toute transparence une fois le déplacement géographique de OneDrive terminé. L’utilisateur n’a pas besoin de se connecter à nouveau, ni d’effectuer une autre action. (Version 17.3.6943.0625 ou ultérieure du client de synchronisation requise.)</span><span class="sxs-lookup"><span data-stu-id="6a0f7-p115">The OneDrive sync client will automatically detect and seamlessly transfer syncing to the new OneDrive location once the OneDrive geo move is complete. The user does not need to sign-in again or take any other action.  (Version 17.3.6943.0625 or later of the sync client required.)</span></span>

<span data-ttu-id="6a0f7-192">Si un utilisateur met à jour un fichier pendant le déplacement géographique de OneDrive, le client de synchronisation l’informe que des téléchargements de fichiers sont en attente pendant le déplacement.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-192">If a user updates a file while the OneDrive geo move is in progress, the sync client will notify them that file uploads are pending while the move is underway.</span></span>

### <a name="sharing-links"></a><span data-ttu-id="6a0f7-193">Liens de partage</span><span class="sxs-lookup"><span data-stu-id="6a0f7-193">Sharing links</span></span> 

<span data-ttu-id="6a0f7-194">Lorsque le déplacement géographique de OneDrive est terminé, les liens partagés existants pour les fichiers qui ont été déplacés redirigent automatiquement vers le nouvel emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-194">Upon OneDrive geo move completion, the existing shared links for the files that were moved will automatically redirect to the new geo location.</span></span>

### <a name="onenote-experience"></a><span data-ttu-id="6a0f7-195">Expérience OneNote</span><span class="sxs-lookup"><span data-stu-id="6a0f7-195">OneNote Experience</span></span> 

<span data-ttu-id="6a0f7-p116">Le client OneNote win32 client et l’application UWP (universelle) détecteront automatiquement et synchroniseront en toute transparence les blocs-notes avec le nouvel emplacement OneDrive à la fin du déplacement géographique de OneDrive. L’utilisateur n’a pas besoin de se connecter à nouveau ou d’effectuer une autre action. Le seul indicateur visible pour l’utilisateur est l’échec de la synchronisation des blocs-notes lorsque le déplacement géographique de OneDrive est en cours. Cette expérience est disponible sur les versions de client OneNote suivantes :</span><span class="sxs-lookup"><span data-stu-id="6a0f7-p116">OneNote win32 client and UWP (Universal) App will automatically detect and seamlessly sync notebooks to the new OneDrive location once OneDrive geo move is complete. The user does not need to sign-in again or take any other action. The only visible indicator to the user is notebook sync would fail when OneDrive geo move is in progress. This experience is available on the following OneNote client versions:</span></span>

-   <span data-ttu-id="6a0f7-200">OneNote win32 – Version 16.0.8326.2096 (et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="6a0f7-200">OneNote win32 – Version 16.0.8326.2096 (and later)</span></span>

-   <span data-ttu-id="6a0f7-201">OneNote UWP – Version 16.0.8431.1006 (et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="6a0f7-201">OneNote UWP – Version 16.0.8431.1006 (and later)</span></span>

-   <span data-ttu-id="6a0f7-202">Application mobile OneNote : Version 16.0.8431.1011 (et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="6a0f7-202">OneNote Mobile App – Version 16.0.8431.1011 (and later)</span></span>

### <a name="teams-app"></a><span data-ttu-id="6a0f7-203">Application Teams</span><span class="sxs-lookup"><span data-stu-id="6a0f7-203">Teams app</span></span>

<span data-ttu-id="6a0f7-p117">Lorsque le déplacement géographique de OneDrive est terminé, les utilisateurs ont accès à leurs fichiers OneDrive sur l’application Teams. En outre, les fichiers partagés via la conversation Teams de leur site OneDrive avant le déplacement géographique continuent à fonctionner après le déplacement.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-p117">Upon OneDrive geo move completion, users will have access to their OneDrive files on the Teams app. Additionally, files shared via Teams chat from their OneDrive prior to geo move will continue to work after move is complete.</span></span>

### <a name="onedrive-for-business-mobile-app-ios"></a><span data-ttu-id="6a0f7-206">Application mobile OneDrive Entreprise (iOS)</span><span class="sxs-lookup"><span data-stu-id="6a0f7-206">OneDrive for Business Mobile App (iOS)</span></span> 

<span data-ttu-id="6a0f7-207">Lorsque le déplacement géographique de OneDrive est terminé, l’utilisateur doit se déconnecter et se reconnecter sur l’application mobile iOS pour réaliser la synchronisation avec le nouvel emplacement OneDrive.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-207">Upon OneDrive geo move completion, the user would need to sign out and sign in again on the iOS Mobile App to sync to the new OneDrive location.</span></span>

### <a name="existing-followed-groups-and-sites"></a><span data-ttu-id="6a0f7-208">Sites et groupes suivis existants</span><span class="sxs-lookup"><span data-stu-id="6a0f7-208">Existing followed groups and sites</span></span>

<span data-ttu-id="6a0f7-209">Les sites suivis et les groupes s’afficheront dans les OneDrive de l’utilisateur, quel que soit leur emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-209">Followed sites and groups will show up in the user's OneDrive regardless of their geo location.</span></span> <span data-ttu-id="6a0f7-210">Les sites et les groupes hébergés dans un autre emplacement géographique s’ouvrent dans un onglet distinct.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-210">Sites and groups hosted in another geo location will open in a separate tab.</span></span>

### <a name="delve-geo-url-updates"></a><span data-ttu-id="6a0f7-211">Delve Mises à jour de l’URL géographique</span><span class="sxs-lookup"><span data-stu-id="6a0f7-211">Delve Geo URL updates</span></span>

<span data-ttu-id="6a0f7-212">Les utilisateurs sont envoyés vers la Delve géographique correspondant à leur PDL uniquement après que leur OneDrive a été déplacée vers la nouvelle géographique.</span><span class="sxs-lookup"><span data-stu-id="6a0f7-212">Users will be sent to the Delve geo corresponding to their PDL only after their OneDrive has been moved to the new geo.</span></span>
