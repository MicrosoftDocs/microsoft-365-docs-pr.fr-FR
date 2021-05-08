---
title: Afficher et gérer les actions dans le centre de gestion des actions
description: Utiliser le Centre de gestion des actions pour afficher et gérer les actions de correction
keywords: action, center, autoair, automated, investigation, response, remediation
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: how-to
ms.custom: autoir
ms.reviewer: evaldm, isco
ms.technology: m365d
ms.openlocfilehash: e3e842f812c5675334cc25fa35544165129db2b4
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52245887"
---
# <a name="view-and-manage-actions-in-the-action-center"></a><span data-ttu-id="4a9fa-104">Afficher et gérer les actions dans le centre de gestion des actions</span><span class="sxs-lookup"><span data-stu-id="4a9fa-104">View and manage actions in the Action center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="4a9fa-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="4a9fa-105">**Applies to:**</span></span>
- <span data-ttu-id="4a9fa-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4a9fa-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="4a9fa-107">Les fonctionnalités de protection contre les menaces Microsoft 365 Defender peuvent entraîner certaines actions de correction.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-107">Threat protection features in Microsoft 365 Defender can result in certain remediation actions.</span></span> <span data-ttu-id="4a9fa-108">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="4a9fa-108">Here are some examples:</span></span>
- <span data-ttu-id="4a9fa-109">[Les examens automatisés](m365d-autoir.md) peuvent entraîner des actions de correction prises automatiquement ou en attente d’approbation.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-109">[Automated investigations](m365d-autoir.md) can result in remediation actions that are taken automatically or await approval.</span></span>
- <span data-ttu-id="4a9fa-110">Un antivirus, un logiciel anti-programme malveillant et d’autres fonctionnalités de protection contre les menaces peuvent entraîner des actions de correction, telles que le blocage d’un fichier, d’une URL ou d’un processus, ou l’envoi d’un artefact en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-110">Antivirus, antimalware, and other threat protection features can result in remediation actions, such as blocking a file, URL, or process, or sending an artifact to quarantine.</span></span>
- <span data-ttu-id="4a9fa-111">Votre équipe en matière d’opérations de [](advanced-hunting-overview.md) sécurité peut prendre des mesures correctives manuellement, par exemple lors d’une recherche avancée ou lors de l’investigation d’alertes [ou d’incidents.](investigate-incidents.md) [](investigate-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="4a9fa-111">Your security operations team can take remediation actions manually, such as during [advanced hunting](advanced-hunting-overview.md) or while investigating [alerts](investigate-alerts.md) or [incidents](investigate-incidents.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4a9fa-112">Vous devez disposer des [autorisations appropriées](m365d-action-center.md#required-permissions-for-action-center-tasks) pour approuver ou rejeter les actions de correction.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-112">You must have [appropriate permissions](m365d-action-center.md#required-permissions-for-action-center-tasks) to approve or reject remediation actions.</span></span> <span data-ttu-id="4a9fa-113">Pour plus d’informations, [voir Les conditions préalables à l’examen et](m365d-configure-auto-investigation-response.md#prerequisites-for-automated-investigation-and-response-in-microsoft-365-defender)à la réponse automatisés dans Microsoft 365 Defender .</span><span class="sxs-lookup"><span data-stu-id="4a9fa-113">For more information, see [Prerequisites for automated investigation and response in Microsoft 365 Defender](m365d-configure-auto-investigation-response.md#prerequisites-for-automated-investigation-and-response-in-microsoft-365-defender).</span></span>

## <a name="review-pending-actions-in-the-action-center"></a><span data-ttu-id="4a9fa-114">Passer en revue les actions en attente dans le centre de actions</span><span class="sxs-lookup"><span data-stu-id="4a9fa-114">Review pending actions in the Action center</span></span>

<span data-ttu-id="4a9fa-115">Il est important d’approuver (ou de refuser) les actions en attente dès que possible de sorte que vos enquêtes automatisées puissent se poursuivre et se terminer dans un délai raisonnable.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-115">It's important to approve (or reject) pending actions as soon as possible so that your automated investigations can proceed and complete in a timely manner.</span></span> 

![Approuver ou rejeter une action](../../media/air-actioncenter-itemselected.png)

1. <span data-ttu-id="4a9fa-117">Accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-117">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in.</span></span> 

2. <span data-ttu-id="4a9fa-118">Dans le volet de navigation, choisissez **Centre de notifications**.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-118">In the navigation pane, choose **Action center**.</span></span> 

3. <span data-ttu-id="4a9fa-119">Dans le centre de notifications, dans l’onglet **En attente**, sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-119">In the Action Center, on the **Pending** tab, select an item in the list.</span></span> <span data-ttu-id="4a9fa-120">Son volet volant s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-120">Its flyout pane opens.</span></span>

4. <span data-ttu-id="4a9fa-121">Examinez les informations dans le volet volant, puis prenez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4a9fa-121">Review the information in the flyout pane, and then take one of the following steps:</span></span>
   - <span data-ttu-id="4a9fa-122">Sélectionnez **Ouvrir la page Examen** pour afficher plus de détails sur l’enquête.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-122">Select **Open investigation page** to view more details about the investigation.</span></span>
   - <span data-ttu-id="4a9fa-123">Sélectionnez **Approuver** pour lancer une action en attente.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-123">Select **Approve** to initiate a pending action.</span></span>
   - <span data-ttu-id="4a9fa-124">Sélectionnez **Rejeter** pour empêcher une action en attente d’être prise.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-124">Select **Reject** to prevent a pending action from being taken.</span></span>
   - <span data-ttu-id="4a9fa-125">Sélectionnez **Go hunt** (Aller à la recherche) pour aller [dans le recherche avancée](advanced-hunting-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4a9fa-125">Select **Go hunt** to go into [Advanced hunting](advanced-hunting-overview.md).</span></span> 

## <a name="undo-completed-actions"></a><span data-ttu-id="4a9fa-126">Annuler les actions terminées</span><span class="sxs-lookup"><span data-stu-id="4a9fa-126">Undo completed actions</span></span>

<span data-ttu-id="4a9fa-127">Si vous avez déterminé qu’un appareil ou un fichier n’est pas une menace, vous pouvez annuler les actions de correction qui ont été prises, que ces actions soient prises automatiquement ou manuellement.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-127">If you’ve determined that a device or a file is not a threat, you can undo remediation actions that were taken, whether those actions were taken automatically or manually.</span></span> <span data-ttu-id="4a9fa-128">Dans le centre de actions, sous **l’onglet** Historique, vous pouvez annuler l’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="4a9fa-128">In the Action center, on the **History** tab, you can undo any of the following actions:</span></span>  

| <span data-ttu-id="4a9fa-129">Source de l’action</span><span class="sxs-lookup"><span data-stu-id="4a9fa-129">Action source</span></span> | <span data-ttu-id="4a9fa-130">Actions prises en charge</span><span class="sxs-lookup"><span data-stu-id="4a9fa-130">Supported Actions</span></span> |
|:---|:---|
| <span data-ttu-id="4a9fa-131">- Examen automatisé</span><span class="sxs-lookup"><span data-stu-id="4a9fa-131">- Automated investigation</span></span> <br/><span data-ttu-id="4a9fa-132">- Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="4a9fa-132">- Microsoft Defender Antivirus</span></span> <br/><span data-ttu-id="4a9fa-133">- Actions de réponse manuelles</span><span class="sxs-lookup"><span data-stu-id="4a9fa-133">- Manual response actions</span></span> | <span data-ttu-id="4a9fa-134">- Isoler l’appareil</span><span class="sxs-lookup"><span data-stu-id="4a9fa-134">- Isolate device</span></span> <br/><span data-ttu-id="4a9fa-135">- Restreindre l’exécution du code</span><span class="sxs-lookup"><span data-stu-id="4a9fa-135">- Restrict code execution</span></span> <br/><span data-ttu-id="4a9fa-136">- Mettre en quarantaine un fichier</span><span class="sxs-lookup"><span data-stu-id="4a9fa-136">- Quarantine a file</span></span> <br/><span data-ttu-id="4a9fa-137">- Supprimer une clé de Registre</span><span class="sxs-lookup"><span data-stu-id="4a9fa-137">- Remove a registry key</span></span> <br/><span data-ttu-id="4a9fa-138">- Arrêter un service</span><span class="sxs-lookup"><span data-stu-id="4a9fa-138">- Stop a service</span></span> <br/><span data-ttu-id="4a9fa-139">- Désactiver un pilote</span><span class="sxs-lookup"><span data-stu-id="4a9fa-139">- Disable a driver</span></span> <br/><span data-ttu-id="4a9fa-140">- Supprimer une tâche programmée</span><span class="sxs-lookup"><span data-stu-id="4a9fa-140">- Remove a scheduled task</span></span> |

### <a name="undo-one-remediation-action"></a><span data-ttu-id="4a9fa-141">Annuler une action de correction</span><span class="sxs-lookup"><span data-stu-id="4a9fa-141">Undo one remediation action</span></span>

1. <span data-ttu-id="4a9fa-142">Go to the Action center ( [https://security.microsoft.com/action-center](https://security.microsoft.com/action-center) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-142">Go to the Action center ([https://security.microsoft.com/action-center](https://security.microsoft.com/action-center)) and sign in.</span></span>

2. <span data-ttu-id="4a9fa-143">Sous **l’onglet** Historique, sélectionnez une action à annuler.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-143">On the **History** tab, select an action that you want to undo.</span></span>

3. <span data-ttu-id="4a9fa-144">Dans le volet sur le côté droit de l’écran, sélectionnez **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-144">In the pane on the right side of the screen, select **Undo**.</span></span>

### <a name="undo-multiple-remediation-actions"></a><span data-ttu-id="4a9fa-145">Annuler plusieurs actions de correction</span><span class="sxs-lookup"><span data-stu-id="4a9fa-145">Undo multiple remediation actions</span></span>

1. <span data-ttu-id="4a9fa-146">Go to the Action center ( https://security.microsoft.com/action-center) and sign in.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-146">Go to the Action center (https://security.microsoft.com/action-center) and sign in.</span></span>

2. <span data-ttu-id="4a9fa-147">Sous **l’onglet** Historique, sélectionnez les actions à annuler.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-147">On the **History** tab, select the actions that you want to undo.</span></span> <span data-ttu-id="4a9fa-148">Veillez à sélectionner les éléments qui ont le même type d’action.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-148">Make sure to select items that have the same Action type.</span></span> <span data-ttu-id="4a9fa-149">Un volet volant s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-149">A flyout pane opens.</span></span>

3. <span data-ttu-id="4a9fa-150">Dans le volet volant, sélectionnez **Annuler.**</span><span class="sxs-lookup"><span data-stu-id="4a9fa-150">In the flyout pane, select **Undo**.</span></span>

### <a name="to-remove-a-file-from-quarantine-across-multiple-devices"></a><span data-ttu-id="4a9fa-151">Pour supprimer un fichier de la quarantaine sur plusieurs appareils</span><span class="sxs-lookup"><span data-stu-id="4a9fa-151">To remove a file from quarantine across multiple devices</span></span> 

1. <span data-ttu-id="4a9fa-152">Go to the Action center ( [https://security.microsoft.com/action-center](https://security.microsoft.com/action-center) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-152">Go to the Action center ([https://security.microsoft.com/action-center](https://security.microsoft.com/action-center)) and sign in.</span></span>

2. <span data-ttu-id="4a9fa-153">Sous **l’onglet** Historique, sélectionnez un fichier dont le fichier de mise en quarantaine du type d’action **est sélectionné.**</span><span class="sxs-lookup"><span data-stu-id="4a9fa-153">On the **History** tab, select a file that has the Action type **Quarantine file**.</span></span>

3. <span data-ttu-id="4a9fa-154">Dans le volet sur le côté droit de l’écran, sélectionnez Appliquer à **X plus d’instances** de ce fichier, puis **sélectionnez Annuler**.</span><span class="sxs-lookup"><span data-stu-id="4a9fa-154">In the pane on the right side of the screen, select **Apply to X more instances of this file**, and then select **Undo**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4a9fa-155">Prochaines étapes</span><span class="sxs-lookup"><span data-stu-id="4a9fa-155">Next steps</span></span>

- [<span data-ttu-id="4a9fa-156">Consulter les détails et les résultats d'un examen automatisé</span><span class="sxs-lookup"><span data-stu-id="4a9fa-156">View the details and results of an automated investigation</span></span>](m365d-autoir-results.md)
- [<span data-ttu-id="4a9fa-157">Découvrez comment gérer les faux positifs/négatifs (si vous en obtenez un)</span><span class="sxs-lookup"><span data-stu-id="4a9fa-157">Learn how to handle false positives/negatives (if you get one)</span></span>](m365d-autoir-report-false-positives-negatives.md)
