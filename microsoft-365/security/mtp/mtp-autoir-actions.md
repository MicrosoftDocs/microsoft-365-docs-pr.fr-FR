---
title: Approuver ou rejeter les actions en attente à la suite d’un examen automatisé
description: Utiliser le centre d’actions pour gérer les actions liées à une enquête et une réponse automatisées
keywords: action, center, autoair, automated, investigation, response, remediation
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: conceptual
ms.custom: autoir
ms.reviewer: evaldm, isco
ms.date: 12/09/2020
ms.technology: m365d
ms.openlocfilehash: 3776dea4a5a24f4695a5c617325af14f1f03494f
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49930377"
---
# <a name="approve-or-reject-pending-actions-following-an-automated-investigation"></a><span data-ttu-id="f350f-104">Approuver ou rejeter les actions en attente à la suite d’un examen automatisé</span><span class="sxs-lookup"><span data-stu-id="f350f-104">Approve or reject pending actions following an automated investigation</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="f350f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f350f-105">**Applies to:**</span></span>
- <span data-ttu-id="f350f-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f350f-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="f350f-107">Lorsqu’une enquête automatisée s’exécute, elle peut engendrer une ou plusieurs [actions de correction](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-remediation-actions) nécessitant une approbation pour continuer.</span><span class="sxs-lookup"><span data-stu-id="f350f-107">When an automated investigation runs, it can result in one or more [remediation actions](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-remediation-actions) that require approval to proceed.</span></span> <span data-ttu-id="f350f-108">Par exemple, il peut être nécessaire de supprimer un cluster d’e-mails ou un fichier mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="f350f-108">For example, a cluster of email messages might need to be deleted, or a quarantined file might need to be removed.</span></span> <span data-ttu-id="f350f-109">Il est important d’approuver (ou de refuser) les actions en attente dès que possible de sorte que vos enquêtes automatisées puissent se poursuivre et se terminer dans un délai raisonnable.</span><span class="sxs-lookup"><span data-stu-id="f350f-109">It's important to approve (or reject) pending actions as soon as possible so that your automated investigations can proceed and complete in a timely manner.</span></span> 

> [!TIP]
> <span data-ttu-id="f350f-110">Si vous pensez que quelque chose a été manqué ou détecté à tort par les fonctionnalités d’investigation et de réponse automatisées dans Microsoft 365 Defender, faites-le nous savoir !</span><span class="sxs-lookup"><span data-stu-id="f350f-110">If you think something was missed or wrongly detected by automated investigation and response features in Microsoft 365 Defender, let us know!</span></span> <span data-ttu-id="f350f-111">Découvrez comment signaler les faux positifs/négatifs dans les fonctionnalités d’investigation et de réponse [automatisées (AIR) dans Microsoft 365 Defender.](mtp-autoir-report-false-positives-negatives.md)</span><span class="sxs-lookup"><span data-stu-id="f350f-111">See [How to report false positives/negatives in automated investigation and response (AIR) capabilities in Microsoft 365 Defender](mtp-autoir-report-false-positives-negatives.md).</span></span>

<span data-ttu-id="f350f-112">Les actions en attente peuvent être examinées et approuvées à l’aide du centre [de](#review-a-pending-action-in-the-action-center) actions ou de l’affichage [détails de l’enquête.](#review-a-pending-action-in-the-investigation-details-view)</span><span class="sxs-lookup"><span data-stu-id="f350f-112">Pending actions can be reviewed and approved by using the [Action center](#review-a-pending-action-in-the-action-center) or the [investigation details view](#review-a-pending-action-in-the-investigation-details-view).</span></span>

> [!NOTE]
> <span data-ttu-id="f350f-113">Vous devez disposer des [autorisations appropriées](mtp-action-center.md#required-permissions-for-action-center-tasks) pour approuver ou rejeter les actions de correction.</span><span class="sxs-lookup"><span data-stu-id="f350f-113">You must have [appropriate permissions](mtp-action-center.md#required-permissions-for-action-center-tasks) to approve or reject remediation actions.</span></span> <span data-ttu-id="f350f-114">Pour plus d’informations, voir [Conditions préalables à l’examen et à la réponse automatisés dans Microsoft 365 Defender.](mtp-configure-auto-investigation-response.md#prerequisites-for-automated-investigation-and-response-in-microsoft-365-defender)</span><span class="sxs-lookup"><span data-stu-id="f350f-114">For more information, see [Prerequisites for automated investigation and response in Microsoft 365 Defender](mtp-configure-auto-investigation-response.md#prerequisites-for-automated-investigation-and-response-in-microsoft-365-defender).</span></span>

## <a name="review-a-pending-action-in-the-action-center"></a><span data-ttu-id="f350f-115">Examiner une action en attente dans le centre de notifications</span><span class="sxs-lookup"><span data-stu-id="f350f-115">Review a pending action in the Action center</span></span>

1. <span data-ttu-id="f350f-116">Accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="f350f-116">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in.</span></span> 

2. <span data-ttu-id="f350f-117">Dans le volet de navigation, choisissez **Centre de notifications**.</span><span class="sxs-lookup"><span data-stu-id="f350f-117">In the navigation pane, choose **Action center**.</span></span> 

3. <span data-ttu-id="f350f-118">Dans le centre de notifications, dans l’onglet **En attente**, sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="f350f-118">In the Action Center, on the **Pending** tab, select an item in the list.</span></span> 

    - <span data-ttu-id="f350f-119">Si vous sélectionnez un élément dans la colonne **Numéro de l’enquête**, la page Détails de l’enquête s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f350f-119">If you select an item in the **Investigation number** column, the investigation details page opens.</span></span> <span data-ttu-id="f350f-120">Là, vous pouvez afficher les résultats de l’enquête, puis approuver ou rejeter l’action recommandée.</span><span class="sxs-lookup"><span data-stu-id="f350f-120">There, you can view the results of the investigation, and then either approve or reject the recommended action.</span></span>
 
    - <span data-ttu-id="f350f-121">Si vous sélectionnez une ligne dans la liste, un menu volant affiche des informations relatives à cet élément.</span><span class="sxs-lookup"><span data-stu-id="f350f-121">If you select a row in the list, a flyout opens, where you can view information about that item.</span></span> <br/>![Approuver ou rejeter une action](../../media/air-actioncenter-itemselected.png)<br/><span data-ttu-id="f350f-123">Utilisez les liens pour afficher une alerte ou une enquête associée, puis approuvez ou refusez l’action.</span><span class="sxs-lookup"><span data-stu-id="f350f-123">Use the links to view an associated alert or an investigation, and approve or reject the action.</span></span>

## <a name="review-a-pending-action-in-the-investigation-details-view"></a><span data-ttu-id="f350f-124">Examiner une action en attente dans la vue de détails de l’enquête</span><span class="sxs-lookup"><span data-stu-id="f350f-124">Review a pending action in the investigation details view</span></span>

![Détails de l’enquête](../../media/mtp-air-investdetails.png)

1. <span data-ttu-id="f350f-126">Sur une page de [détails de l’enquête](mtp-autoir-results.md), sélectionnez l’onglet **Actions en attente** (ou **Actions**). Les éléments en attente d’approbation sont répertoriés ici.</span><span class="sxs-lookup"><span data-stu-id="f350f-126">On an [investigation details](mtp-autoir-results.md) page, select the **Pending actions** (or **Actions**) tab. Items that are pending approval are listed here.</span></span>

2. <span data-ttu-id="f350f-127">Sélectionnez un élément dans la liste, puis choisissez **Approuver** ou **Rejeter**.</span><span class="sxs-lookup"><span data-stu-id="f350f-127">Select an item in the list, and then choose **Approve** or **Reject**.</span></span>

## <a name="undo-completed-actions"></a><span data-ttu-id="f350f-128">Annuler les actions terminées</span><span class="sxs-lookup"><span data-stu-id="f350f-128">Undo completed actions</span></span>

<span data-ttu-id="f350f-129">Si vous avez déterminé qu’un appareil ou un fichier n’est pas une menace, vous pouvez annuler les actions de correction qui ont été prises, que ces actions soient prises automatiquement ou manuellement.</span><span class="sxs-lookup"><span data-stu-id="f350f-129">If you’ve determined that a device or a file is not a threat, you can undo remediation actions that were taken, whether those actions were taken automatically or manually.</span></span> <span data-ttu-id="f350f-130">Dans le centre de actions, sous **l’onglet** Historique, vous pouvez annuler l’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="f350f-130">In the Action center, on the **History** tab, you can undo any of the following actions:</span></span>  

| <span data-ttu-id="f350f-131">Source d’action</span><span class="sxs-lookup"><span data-stu-id="f350f-131">Action source</span></span> | <span data-ttu-id="f350f-132">Actions prises en charge</span><span class="sxs-lookup"><span data-stu-id="f350f-132">Supported Actions</span></span> |
|:---|:---|
| <span data-ttu-id="f350f-133">- Examen automatisé</span><span class="sxs-lookup"><span data-stu-id="f350f-133">- Automated investigation</span></span> <br/><span data-ttu-id="f350f-134">- Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="f350f-134">- Microsoft Defender Antivirus</span></span> <br/><span data-ttu-id="f350f-135">- Actions de réponse manuelles</span><span class="sxs-lookup"><span data-stu-id="f350f-135">- Manual response actions</span></span> | <span data-ttu-id="f350f-136">- Isoler l’appareil</span><span class="sxs-lookup"><span data-stu-id="f350f-136">- Isolate device</span></span> <br/><span data-ttu-id="f350f-137">- Restreindre l’exécution du code</span><span class="sxs-lookup"><span data-stu-id="f350f-137">- Restrict code execution</span></span> <br/><span data-ttu-id="f350f-138">- Mettre en quarantaine un fichier</span><span class="sxs-lookup"><span data-stu-id="f350f-138">- Quarantine a file</span></span> <br/><span data-ttu-id="f350f-139">- Supprimer une clé de Registre</span><span class="sxs-lookup"><span data-stu-id="f350f-139">- Remove a registry key</span></span> <br/><span data-ttu-id="f350f-140">- Arrêter un service</span><span class="sxs-lookup"><span data-stu-id="f350f-140">- Stop a service</span></span> <br/><span data-ttu-id="f350f-141">- Désactiver un pilote</span><span class="sxs-lookup"><span data-stu-id="f350f-141">- Disable a driver</span></span> <br/><span data-ttu-id="f350f-142">- Supprimer une tâche programmée</span><span class="sxs-lookup"><span data-stu-id="f350f-142">- Remove a scheduled task</span></span> |

### <a name="to-undo-a-remediation-action"></a><span data-ttu-id="f350f-143">Pour annuler une action de correction</span><span class="sxs-lookup"><span data-stu-id="f350f-143">To undo a remediation action</span></span>

1. <span data-ttu-id="f350f-144">Go to the Action center ( [https://security.microsoft.com/action-center](https://security.microsoft.com/action-center) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="f350f-144">Go to the Action center ([https://security.microsoft.com/action-center](https://security.microsoft.com/action-center)) and sign in.</span></span>

2. <span data-ttu-id="f350f-145">Sous **l’onglet** Historique, sélectionnez une action à annuler.</span><span class="sxs-lookup"><span data-stu-id="f350f-145">On the **History** tab, select an action that you want to undo.</span></span>

3. <span data-ttu-id="f350f-146">Dans le volet sur le côté droit de l’écran, sélectionnez **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="f350f-146">In the pane on the right side of the screen, select **Undo**.</span></span>

### <a name="to-remove-a-file-from-quarantine-across-multiple-devices"></a><span data-ttu-id="f350f-147">Pour supprimer un fichier de la quarantaine sur plusieurs appareils</span><span class="sxs-lookup"><span data-stu-id="f350f-147">To remove a file from quarantine across multiple devices</span></span> 

1. <span data-ttu-id="f350f-148">Go to the Action center ( [https://security.microsoft.com/action-center](https://security.microsoft.com/action-center) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="f350f-148">Go to the Action center ([https://security.microsoft.com/action-center](https://security.microsoft.com/action-center)) and sign in.</span></span>

2. <span data-ttu-id="f350f-149">Sous **l’onglet** Historique, sélectionnez un fichier dont le fichier de mise en quarantaine du type d’action **est sélectionné.**</span><span class="sxs-lookup"><span data-stu-id="f350f-149">On the **History** tab, select a file that has the Action type **Quarantine file**.</span></span>

3. <span data-ttu-id="f350f-150">Dans le volet sur le côté droit de l’écran, sélectionnez Appliquer à **X plus d’instances** de ce fichier, puis **sélectionnez Annuler**.</span><span class="sxs-lookup"><span data-stu-id="f350f-150">In the pane on the right side of the screen, select **Apply to X more instances of this file**, and then select **Undo**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f350f-151">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="f350f-151">Next steps</span></span>

- [<span data-ttu-id="f350f-152">Consulter les détails et les résultats d'un examen automatisé</span><span class="sxs-lookup"><span data-stu-id="f350f-152">View the details and results of an automated investigation</span></span>](mtp-autoir-results.md)
- [<span data-ttu-id="f350f-153">Gérer les faux positifs/négatifs dans les fonctionnalités automatisées d’examen et de réponse</span><span class="sxs-lookup"><span data-stu-id="f350f-153">Handle false positives/negatives in automated investigation and response capabilities</span></span>](mtp-autoir-report-false-positives-negatives.md)
