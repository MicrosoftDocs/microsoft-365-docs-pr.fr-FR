---
title: Examiner et gérer les actions de correction dans Microsoft Defender pour Office 365
keywords: AIR, autoIR, ATP, automatisé, examen, réponse, correction, menaces, avancé, menace, protection
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
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
description: Découvrez les actions de correction dans les fonctionnalités d’examen et de réponse automatisées dans Microsoft Defender pour Office 365 Plan 2.
ms.technology: mdo
ms.prod: m365-security
ms.date: 01/29/2021
ms.openlocfilehash: a11e9ee6a4c2426951fe2b4aa4f2dd08d1931f1c
ms.sourcegitcommit: 786f90a163d34c02b8451d09aa1efb1e1d5f543c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "50287112"
---
# <a name="review-and-manage-remediation-actions-in-office-365"></a><span data-ttu-id="b7089-104">Examiner et gérer les actions de correction dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b7089-104">Review and manage remediation actions in Office 365</span></span>

<span data-ttu-id="b7089-105">Comme des enquêtes automatisées sur & de collaboration  entraînent des verdicts, tels que malveillants ou suspects, certaines actions de correction sont créées.</span><span class="sxs-lookup"><span data-stu-id="b7089-105">As automated investigations on email & collaboration content result in verdicts, such as *Malicious* or *Suspicious*, certain remediation actions are created.</span></span> <span data-ttu-id="b7089-106">Dans Microsoft Defender pour Office 365, les actions de correction peuvent inclure :</span><span class="sxs-lookup"><span data-stu-id="b7089-106">In Microsoft Defender for Office 365, remediation actions can include:</span></span>
- <span data-ttu-id="b7089-107">Blocage d’une URL (heure du clic)</span><span class="sxs-lookup"><span data-stu-id="b7089-107">Blocking a URL (time-of-click)</span></span>
- <span data-ttu-id="b7089-108">Suppression de messages électroniques ou de clusters de suppression (soft)</span><span class="sxs-lookup"><span data-stu-id="b7089-108">Soft deleting email messages or clusters</span></span>
- <span data-ttu-id="b7089-109">Mise en quarantaine des pièces jointes ou des e-mails</span><span class="sxs-lookup"><span data-stu-id="b7089-109">Quarantining email or email attachments</span></span>
- <span data-ttu-id="b7089-110">Turning off external mail forwarding</span><span class="sxs-lookup"><span data-stu-id="b7089-110">Turning off external mail forwarding</span></span>

<span data-ttu-id="b7089-111">Ces mesures correctives ne sont prises que si votre équipe en charge des opérations de sécurité ne les approuve pas.</span><span class="sxs-lookup"><span data-stu-id="b7089-111">These remediation actions are not taken unless and until your security operations team approves them.</span></span> <span data-ttu-id="b7089-112">Nous vous recommandons d’examiner et d’approuver les actions en attente dès que possible afin que vos enquêtes automatisées se terminent en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="b7089-112">We recommend reviewing and approving any pending actions as soon as possible so that your automated investigations complete in a timely manner.</span></span> <span data-ttu-id="b7089-113">Dans certains cas, vous pouvez annuler une action de correction.</span><span class="sxs-lookup"><span data-stu-id="b7089-113">In some cases, you can undo a remediation action.</span></span>

<span data-ttu-id="b7089-114">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="b7089-114">**Applies to**</span></span>
- [<span data-ttu-id="b7089-115">Microsoft Defender pour Office 365 Plan 2</span><span class="sxs-lookup"><span data-stu-id="b7089-115">Microsoft Defender for Office 365 plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="b7089-116">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b7089-116">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

## <a name="approve-or-reject-pending-actions"></a><span data-ttu-id="b7089-117">Approuver (ou rejeter) les actions en attente</span><span class="sxs-lookup"><span data-stu-id="b7089-117">Approve (or reject) pending actions</span></span>

1. <span data-ttu-id="b7089-118">Go to the Microsoft 365 security center [https://security.microsoft.com](https://security.microsoft.com) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="b7089-118">Go to the Microsoft 365 security center [https://security.microsoft.com](https://security.microsoft.com)) and sign in.</span></span>
2. <span data-ttu-id="b7089-119">Dans le volet de navigation, sélectionnez **Centre de l’action.**</span><span class="sxs-lookup"><span data-stu-id="b7089-119">In the navigation pane, select **Action center**.</span></span>
3. <span data-ttu-id="b7089-120">Sous **l’onglet En** attente, examinez la liste des actions en attente d’approbation.</span><span class="sxs-lookup"><span data-stu-id="b7089-120">On the **Pending** tab, review the list of actions that are awaiting approval.</span></span>
4. <span data-ttu-id="b7089-121">Sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="b7089-121">Select an item in the list.</span></span> <span data-ttu-id="b7089-122">Son volet volant s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="b7089-122">Its flyout pane opens.</span></span> 
5. <span data-ttu-id="b7089-123">Examinez les informations dans le volet volant, puis prenez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7089-123">Review the information in the flyout pane, and then take one of the following steps:</span></span>
   - <span data-ttu-id="b7089-124">Sélectionnez **Ouvrir la page Examen** pour afficher plus de détails sur l’enquête.</span><span class="sxs-lookup"><span data-stu-id="b7089-124">Select **Open investigation page** to view more details about the investigation.</span></span>
   - <span data-ttu-id="b7089-125">Sélectionnez **Approuver** pour lancer une action en attente.</span><span class="sxs-lookup"><span data-stu-id="b7089-125">Select **Approve** to initiate a pending action.</span></span>
   - <span data-ttu-id="b7089-126">Sélectionnez **Rejeter** pour empêcher une action en attente d’être prise.</span><span class="sxs-lookup"><span data-stu-id="b7089-126">Select **Reject** to prevent a pending action from being taken.</span></span>

## <a name="undo-one-remediation-action"></a><span data-ttu-id="b7089-127">Annuler une action de correction</span><span class="sxs-lookup"><span data-stu-id="b7089-127">Undo one remediation action</span></span>

1. <span data-ttu-id="b7089-128">Go to the Action center ( [https://security.microsoft.com/action-center](https://security.microsoft.com/action-center) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="b7089-128">Go to the Action center ([https://security.microsoft.com/action-center](https://security.microsoft.com/action-center)) and sign in.</span></span>
2. <span data-ttu-id="b7089-129">Sous **l’onglet** Historique, sélectionnez une action à annuler.</span><span class="sxs-lookup"><span data-stu-id="b7089-129">On the **History** tab, select an action that you want to undo.</span></span>
3. <span data-ttu-id="b7089-130">Dans le volet sur le côté droit de l’écran, sélectionnez **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="b7089-130">In the pane on the right side of the screen, select **Undo**.</span></span>

## <a name="undo-multiple-remediation-actions"></a><span data-ttu-id="b7089-131">Annuler plusieurs actions de correction</span><span class="sxs-lookup"><span data-stu-id="b7089-131">Undo multiple remediation actions</span></span>

1. <span data-ttu-id="b7089-132">Go to the Action center ( [https://security.microsoft.com/action-center](https://security.microsoft.com/action-center) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="b7089-132">Go to the Action center ([https://security.microsoft.com/action-center](https://security.microsoft.com/action-center)) and sign in.</span></span>
2. <span data-ttu-id="b7089-133">Sous **l’onglet** Historique, sélectionnez les actions à annuler.</span><span class="sxs-lookup"><span data-stu-id="b7089-133">On the **History** tab, select the actions that you want to undo.</span></span> <span data-ttu-id="b7089-134">Veillez à sélectionner les éléments qui ont le même type d’action.</span><span class="sxs-lookup"><span data-stu-id="b7089-134">Make sure to select items that have the same Action type.</span></span> <span data-ttu-id="b7089-135">Un volet volant s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="b7089-135">A flyout pane opens.</span></span>
3. <span data-ttu-id="b7089-136">Dans le volet volant, sélectionnez Annuler.</span><span class="sxs-lookup"><span data-stu-id="b7089-136">In the flyout pane, select Undo.</span></span>

## <a name="to-remove-a-file-from-quarantine-across-multiple-devices"></a><span data-ttu-id="b7089-137">Pour supprimer un fichier de la quarantaine sur plusieurs appareils</span><span class="sxs-lookup"><span data-stu-id="b7089-137">To remove a file from quarantine across multiple devices</span></span>

1. <span data-ttu-id="b7089-138">Go to the Action center ( [https://security.microsoft.com/action-center](https://security.microsoft.com/action-center) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="b7089-138">Go to the Action center ([https://security.microsoft.com/action-center](https://security.microsoft.com/action-center)) and sign in.</span></span>
2. <span data-ttu-id="b7089-139">Sous **l’onglet** Historique, sélectionnez un fichier dont le fichier de mise en quarantaine du type d’action **est sélectionné.**</span><span class="sxs-lookup"><span data-stu-id="b7089-139">On the **History** tab, select a file that has the Action type **Quarantine file**.</span></span>
3. <span data-ttu-id="b7089-140">Dans le volet sur le côté droit de l’écran, sélectionnez Appliquer à **X plus d’instances** de ce fichier, puis **sélectionnez Annuler**.</span><span class="sxs-lookup"><span data-stu-id="b7089-140">In the pane on the right side of the screen, select **Apply to X more instances of this file**, and then select **Undo**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b7089-141">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="b7089-141">Next steps</span></span>

- [<span data-ttu-id="b7089-142">Utiliser l’Explorateur de menaces</span><span class="sxs-lookup"><span data-stu-id="b7089-142">Use Threat Explorer</span></span>](threat-explorer.md)
- [<span data-ttu-id="b7089-143">Comment signaler les faux positifs/négatifs dans les fonctionnalités automatisées d’examen et de réponse</span><span class="sxs-lookup"><span data-stu-id="b7089-143">How to report false positives/negatives in automated investigation and response capabilities</span></span>](air-report-false-positives-negatives.md)

## <a name="see-also"></a><span data-ttu-id="b7089-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7089-144">See also</span></span>

- [<span data-ttu-id="b7089-145">Afficher les détails et les résultats d’une enquête automatisée dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b7089-145">View details and results of an automated investigation in Office 365</span></span>](air-view-investigation-results.md)
