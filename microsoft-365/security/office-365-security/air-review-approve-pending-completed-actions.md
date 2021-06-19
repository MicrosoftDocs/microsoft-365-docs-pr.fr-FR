---
title: Examiner et gérer les actions de correction dans Microsoft Defender pour Office 365
keywords: AIR, autoIR, Microsoft Defender pour point de terminaison, automatisé, examen, réponse, correction, menaces, avancé, menace, protection
f1.keywords:
- NOCSH
author: JoeDavies-MSFT
ms.author: josephd
manager: dansimp
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
description: Découvrez les actions de correction dans les fonctionnalités d’investigation et de réponse automatisées dans Microsoft Defender pour Office 365 Plan 2.
ms.technology: mdo
ms.prod: m365-security
ms.date: 06/10/2021
ms.openlocfilehash: 8fc01ab0dd5178032ea7b101f5361c25bb10bbea
ms.sourcegitcommit: d904f04958a13a514ce10219ed822b9e4f74ca2d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "53028930"
---
# <a name="review-and-manage-remediation-actions-in-office-365"></a><span data-ttu-id="fe721-104">Examiner et gérer les actions de correction dans Office 365</span><span class="sxs-lookup"><span data-stu-id="fe721-104">Review and manage remediation actions in Office 365</span></span>

<span data-ttu-id="fe721-105">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="fe721-105">**Applies to**</span></span>
- [<span data-ttu-id="fe721-106">Microsoft Defender pour Office 365 Plan 2</span><span class="sxs-lookup"><span data-stu-id="fe721-106">Microsoft Defender for Office 365 plan 2</span></span>](defender-for-office-365.md)

<span data-ttu-id="fe721-107">Comme des enquêtes automatisées sur & de collaboration  entraînent des verdicts, tels que malveillants ou suspects, certaines actions de correction sont créées.</span><span class="sxs-lookup"><span data-stu-id="fe721-107">As automated investigations on email & collaboration content result in verdicts, such as *Malicious* or *Suspicious*, certain remediation actions are created.</span></span> <span data-ttu-id="fe721-108">Dans Microsoft Defender pour Office 365, les actions de correction peuvent inclure :</span><span class="sxs-lookup"><span data-stu-id="fe721-108">In Microsoft Defender for Office 365, remediation actions can include:</span></span>

- <span data-ttu-id="fe721-109">Suppression de messages électroniques ou de clusters de suppression (soft)</span><span class="sxs-lookup"><span data-stu-id="fe721-109">Soft deleting email messages or clusters</span></span>
- <span data-ttu-id="fe721-110">Turning off external mail forwarding</span><span class="sxs-lookup"><span data-stu-id="fe721-110">Turning off external mail forwarding</span></span>

<span data-ttu-id="fe721-111">Ces mesures correctives ne sont prises que si votre équipe en charge des opérations de sécurité ne les approuve pas.</span><span class="sxs-lookup"><span data-stu-id="fe721-111">These remediation actions are not taken unless and until your security operations team approves them.</span></span> <span data-ttu-id="fe721-112">Nous vous recommandons d’examiner et d’approuver les actions en attente dès que possible afin que vos enquêtes automatisées se terminent en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="fe721-112">We recommend reviewing and approving any pending actions as soon as possible so that your automated investigations complete in a timely manner.</span></span> <span data-ttu-id="fe721-113">Dans certains cas, vous pouvez reconsidérer les actions envoyées.</span><span class="sxs-lookup"><span data-stu-id="fe721-113">In some cases, you can reconsider submitted actions.</span></span>  <span data-ttu-id="fe721-114">Vous devez faire partie du rôle De recherche & purge avant d’effectuer des actions.</span><span class="sxs-lookup"><span data-stu-id="fe721-114">You need to be part of Search & purge role before taking any actions.</span></span>


## <a name="approve-or-reject-pending-actions"></a><span data-ttu-id="fe721-115">Approuver (ou rejeter) les actions en attente</span><span class="sxs-lookup"><span data-stu-id="fe721-115">Approve (or reject) pending actions</span></span>
<span data-ttu-id="fe721-116">Il existe quatre façons de rechercher et d’agir sur des enquêtes automatiques :</span><span class="sxs-lookup"><span data-stu-id="fe721-116">There are four different ways to find and take auto investigation actions:</span></span>

- [<span data-ttu-id="fe721-117">File d’attente des incidents</span><span class="sxs-lookup"><span data-stu-id="fe721-117">Incident queue</span></span>](https://security.microsoft.com/incidents)
- [<span data-ttu-id="fe721-118">Centre de notifications</span><span class="sxs-lookup"><span data-stu-id="fe721-118">Action center</span></span>](https://security.microsoft.com/action-center/pending)
- <span data-ttu-id="fe721-119">Examen proprement dit (accessible via incident ou à partir d’une alerte)</span><span class="sxs-lookup"><span data-stu-id="fe721-119">Investigation itself (accessed via Incident or from an alert)</span></span>
- [<span data-ttu-id="fe721-120">File d’attente des examens d’investigation et de correction</span><span class="sxs-lookup"><span data-stu-id="fe721-120">Investigation and remediation investigations queue</span></span>](https://security.microsoft.com/airinvestigation)

## <a name="incident-queue"></a><span data-ttu-id="fe721-121">File d’attente des incidents</span><span class="sxs-lookup"><span data-stu-id="fe721-121">Incident queue</span></span>
1. <span data-ttu-id="fe721-122">Go to the [Microsoft 365 security center](https://security.microsoft.com) and sign in.</span><span class="sxs-lookup"><span data-stu-id="fe721-122">Go to the [Microsoft 365 security center](https://security.microsoft.com) and sign in.</span></span>
2. <span data-ttu-id="fe721-123">Dans le volet de navigation, sélectionnez **Incidents & alertes > Incidents**.</span><span class="sxs-lookup"><span data-stu-id="fe721-123">In the navigation pane, select **Incidents & alerts > Incidents**.</span></span>
3. <span data-ttu-id="fe721-124">Sélectionnez un nom d’incident pour ouvrir sa page récapitulatif.</span><span class="sxs-lookup"><span data-stu-id="fe721-124">Select an incident name to open its summary page.</span></span>
4. <span data-ttu-id="fe721-125">Sélectionnez **l’onglet Preuve et** réponse.</span><span class="sxs-lookup"><span data-stu-id="fe721-125">Select the **Evidence and Response** tab.</span></span>
5. <span data-ttu-id="fe721-126">Sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="fe721-126">Select an item in the list.</span></span> <span data-ttu-id="fe721-127">Son volet latéral s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="fe721-127">Its side pane opens.</span></span>
6. <span data-ttu-id="fe721-128">Dans le volet latéral, prenez des mesures d’approbation ou de rejet.</span><span class="sxs-lookup"><span data-stu-id="fe721-128">In the side pane, take approve or reject actions.</span></span>

## <a name="investigation-queue"></a><span data-ttu-id="fe721-129">File d’attente d’examen</span><span class="sxs-lookup"><span data-stu-id="fe721-129">Investigation queue</span></span> 
1. <span data-ttu-id="fe721-130">Go to the [Microsoft 365 security center](https://security.microsoft.com) and sign in.</span><span class="sxs-lookup"><span data-stu-id="fe721-130">Go to the [Microsoft 365 security center](https://security.microsoft.com) and sign in.</span></span>
2. <span data-ttu-id="fe721-131">Naviguez à partir de la page alertes/incident.</span><span class="sxs-lookup"><span data-stu-id="fe721-131">Navigate from the alerts/incident page.</span></span> 
3. <span data-ttu-id="fe721-132">Dans la page Examen, allez dans **l’onglet Actions en** attente.</span><span class="sxs-lookup"><span data-stu-id="fe721-132">On the Investigation page, go to the **pending actions** tab.</span></span> 
4. <span data-ttu-id="fe721-133">Sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="fe721-133">Select an item in the list.</span></span> <span data-ttu-id="fe721-134">Son volet latéral s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="fe721-134">Its side pane opens.</span></span>  
5. <span data-ttu-id="fe721-135">Dans le volet latéral, prenez des mesures d’approbation ou de rejet.</span><span class="sxs-lookup"><span data-stu-id="fe721-135">In the side pane, take approve or reject actions.</span></span>

## <a name="action-center"></a><span data-ttu-id="fe721-136">Centre de notifications</span><span class="sxs-lookup"><span data-stu-id="fe721-136">Action center</span></span>
1. <span data-ttu-id="fe721-137">Go to the [Microsoft 365 security center](https://security.microsoft.com) and sign in.</span><span class="sxs-lookup"><span data-stu-id="fe721-137">Go to the [Microsoft 365 security center](https://security.microsoft.com) and sign in.</span></span>
2. <span data-ttu-id="fe721-138">Dans le volet de navigation, sélectionnez **Centre de l’action.**</span><span class="sxs-lookup"><span data-stu-id="fe721-138">In the navigation pane, select **Action center**.</span></span>
3. <span data-ttu-id="fe721-139">Sous **l’onglet En** attente, examinez la liste des actions en attente d’approbation.</span><span class="sxs-lookup"><span data-stu-id="fe721-139">On the **Pending** tab, review the list of actions that are awaiting approval.</span></span>
   - <span data-ttu-id="fe721-140">Sélectionnez **Ouvrir la page Examen** pour afficher plus de détails sur l’enquête.</span><span class="sxs-lookup"><span data-stu-id="fe721-140">Select **Open investigation page** to view more details about the investigation.</span></span>
   - <span data-ttu-id="fe721-141">Sélectionnez **Approuver** pour lancer une action en attente.</span><span class="sxs-lookup"><span data-stu-id="fe721-141">Select **Approve** to initiate a pending action.</span></span>
   - <span data-ttu-id="fe721-142">Sélectionnez **Rejeter** pour empêcher une action en attente d’être prise.</span><span class="sxs-lookup"><span data-stu-id="fe721-142">Select **Reject** to prevent a pending action from being taken.</span></span>

## <a name="investigation-and-remediation-investigations-queue"></a><span data-ttu-id="fe721-143">File d’attente des examens d’investigation et de correction</span><span class="sxs-lookup"><span data-stu-id="fe721-143">Investigation and remediation investigations queue</span></span>
1. <span data-ttu-id="fe721-144">Go to the [Microsoft 365 security center](https://security.microsoft.com) and sign in.</span><span class="sxs-lookup"><span data-stu-id="fe721-144">Go to the [Microsoft 365 security center](https://security.microsoft.com) and sign in.</span></span>
2. <span data-ttu-id="fe721-145">Ouvrir les enquêtes en attente.</span><span class="sxs-lookup"><span data-stu-id="fe721-145">Open pending investigations.</span></span> 
3. <span data-ttu-id="fe721-146">Dans la page Examen, allez dans **l’onglet Actions en** attente.</span><span class="sxs-lookup"><span data-stu-id="fe721-146">On the Investigation page, go to the **pending actions** tab.</span></span>
4. <span data-ttu-id="fe721-147">Sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="fe721-147">Select an item in the list.</span></span> <span data-ttu-id="fe721-148">Son volet latéral s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="fe721-148">Its side pane opens.</span></span>  
5. <span data-ttu-id="fe721-149">Dans le volet latéral, prenez des mesures d’approbation ou de rejet.</span><span class="sxs-lookup"><span data-stu-id="fe721-149">In the side pane, take approve or reject actions.</span></span>

## <a name="change-or-undo-one-remediation-action"></a><span data-ttu-id="fe721-150">Modifier ou annuler une action de correction</span><span class="sxs-lookup"><span data-stu-id="fe721-150">Change or undo one remediation action</span></span>

<span data-ttu-id="fe721-151">Il existe deux façons de reconsidérer les actions envoyées :</span><span class="sxs-lookup"><span data-stu-id="fe721-151">There are two different ways to reconsider submitted actions:</span></span>
   - <span data-ttu-id="fe721-152">Via le centre [de l’action unifiée.](https://security.microsoft.com/action-center)</span><span class="sxs-lookup"><span data-stu-id="fe721-152">Through the [unified action center](https://security.microsoft.com/action-center).</span></span>
   - <span data-ttu-id="fe721-153">Bien que le [centre Office actions .](https://security.microsoft.com/threatincidents)</span><span class="sxs-lookup"><span data-stu-id="fe721-153">Though the [Office action center](https://security.microsoft.com/threatincidents).</span></span>
   
## <a name="change-or-undo-through-the-unified-action-center"></a><span data-ttu-id="fe721-154">Modifier ou annuler via le centre de l’action unifiée</span><span class="sxs-lookup"><span data-stu-id="fe721-154">Change or undo through the unified action center</span></span>
1. <span data-ttu-id="fe721-155">Go to the [unified action center](https://security.microsoft.com/action-center) and sign in.</span><span class="sxs-lookup"><span data-stu-id="fe721-155">Go to the [unified action center](https://security.microsoft.com/action-center) and sign in.</span></span>
2. <span data-ttu-id="fe721-156">Sous **l’onglet** Historique, sélectionnez une action que vous souhaitez modifier ou annuler.</span><span class="sxs-lookup"><span data-stu-id="fe721-156">On the **History** tab, select an action that you want to change or undo.</span></span>
3. <span data-ttu-id="fe721-157">Dans le volet sur le côté droit de l’écran, sélectionnez l’action appropriée **(** déplacer vers la boîte de **réception,** déplacer vers le courrier **indésirable,** déplacer vers les éléments supprimés , \*\*suppression (suppression souple) ou suppression (supprimer **définitivement).**</span><span class="sxs-lookup"><span data-stu-id="fe721-157">In the pane on the right side of the screen, select the appropriate action (**move to inbox**, **move to junk**, **move to deleted items**, \*\*soft delete", or **hard delete**).</span></span>

 ## <a name="change-or-undo-through-the-office-action-center"></a><span data-ttu-id="fe721-158">Modifier ou annuler via le centre de Office actions</span><span class="sxs-lookup"><span data-stu-id="fe721-158">Change or undo through the Office action center</span></span> 
1. <span data-ttu-id="fe721-159">Go to the [Office action center](https://security.microsoft.com/threatincidents) and sign in.</span><span class="sxs-lookup"><span data-stu-id="fe721-159">Go to the [Office action center](https://security.microsoft.com/threatincidents) and sign in.</span></span>
2. <span data-ttu-id="fe721-160">Sélectionnez la correction appropriée.</span><span class="sxs-lookup"><span data-stu-id="fe721-160">Select the appropriate remediation.</span></span>
3. <span data-ttu-id="fe721-161">Dans le volet latéral, cliquez sur l’entrée des envois de courrier et attendez le chargement de la liste.</span><span class="sxs-lookup"><span data-stu-id="fe721-161">In the side pane, click on the mail submissions entry and wait for the list to load.</span></span> 
4. <span data-ttu-id="fe721-162">Attendez que le bouton Action en haut s’active et sélectionnez le bouton Action pour modifier le type d’action.</span><span class="sxs-lookup"><span data-stu-id="fe721-162">Wait for the Action button at the top to enable and select the Action button to change the action type.</span></span> 
5. <span data-ttu-id="fe721-163">Cela crée les actions appropriées.</span><span class="sxs-lookup"><span data-stu-id="fe721-163">This will create the appropriate actions.</span></span>

## <a name="next-steps"></a><span data-ttu-id="fe721-164">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="fe721-164">Next steps</span></span>

- [<span data-ttu-id="fe721-165">Utiliser l’Explorateur de menaces</span><span class="sxs-lookup"><span data-stu-id="fe721-165">Use Threat Explorer</span></span>](threat-explorer.md) 
- [<span data-ttu-id="fe721-166">Actions d’administration /manuelles</span><span class="sxs-lookup"><span data-stu-id="fe721-166">Admin /Manual Actions</span></span>](remediate-malicious-email-delivered-office-365.md)
- [<span data-ttu-id="fe721-167">Comment signaler les faux positifs/négatifs dans les fonctionnalités automatisées d’examen et de réponse</span><span class="sxs-lookup"><span data-stu-id="fe721-167">How to report false positives/negatives in automated investigation and response capabilities</span></span>](air-report-false-positives-negatives.md)

## <a name="see-also"></a><span data-ttu-id="fe721-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe721-168">See also</span></span>

- [<span data-ttu-id="fe721-169">Afficher les détails et les résultats d’un examen automatisé dans Office 365</span><span class="sxs-lookup"><span data-stu-id="fe721-169">View details and results of an automated investigation in Office 365</span></span>](air-view-investigation-results.md)
