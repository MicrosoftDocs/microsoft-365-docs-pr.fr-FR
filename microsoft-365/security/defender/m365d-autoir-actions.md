---
title: Afficher et gérer les actions dans le centre de gestion de l’action
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
ms.openlocfilehash: f3dba2116e0f13f265937ef65fd3b69bcb1e725b
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52274651"
---
# <a name="view-and-manage-actions-in-the-action-center"></a><span data-ttu-id="6b04e-104">Afficher et gérer les actions dans le centre de gestion de l’action</span><span class="sxs-lookup"><span data-stu-id="6b04e-104">View and manage actions in the Action center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="6b04e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6b04e-105">**Applies to:**</span></span>
- <span data-ttu-id="6b04e-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6b04e-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="6b04e-107">Les fonctionnalités de protection contre les menaces de Microsoft 365 Defender peuvent entraîner certaines actions de correction.</span><span class="sxs-lookup"><span data-stu-id="6b04e-107">Threat protection features in Microsoft 365 Defender can result in certain remediation actions.</span></span> <span data-ttu-id="6b04e-108">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="6b04e-108">Here are some examples:</span></span>

- <span data-ttu-id="6b04e-109">[Les examens](m365d-autoir.md) automatisés peuvent entraîner des actions de correction qui sont prises automatiquement ou qui attendent votre approbation.</span><span class="sxs-lookup"><span data-stu-id="6b04e-109">[Automated investigations](m365d-autoir.md) can result in remediation actions that are taken automatically or await your approval.</span></span>
- <span data-ttu-id="6b04e-110">Un antivirus, un logiciel anti-programme malveillant et d’autres fonctionnalités de protection contre les menaces peuvent entraîner des actions de correction, telles que le blocage d’un fichier, d’une URL ou d’un processus, ou l’envoi d’un artefact en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="6b04e-110">Antivirus, antimalware, and other threat protection features can result in remediation actions, such as blocking a file, URL, or process, or sending an artifact to quarantine.</span></span>
- <span data-ttu-id="6b04e-111">Votre équipe en matière d’opérations de [](advanced-hunting-overview.md) sécurité peut prendre des mesures correctives manuellement, par exemple lors d’une recherche avancée ou lors de l’investigation d’alertes [ou d’incidents.](investigate-incidents.md) [](investigate-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="6b04e-111">Your security operations team can take remediation actions manually, such as during [advanced hunting](advanced-hunting-overview.md) or while investigating [alerts](investigate-alerts.md) or [incidents](investigate-incidents.md).</span></span>

> [!NOTE]
> <span data-ttu-id="6b04e-112">Vous devez disposer des [autorisations appropriées](m365d-action-center.md#required-permissions-for-action-center-tasks) pour approuver ou rejeter les actions de correction.</span><span class="sxs-lookup"><span data-stu-id="6b04e-112">You must have [appropriate permissions](m365d-action-center.md#required-permissions-for-action-center-tasks) to approve or reject remediation actions.</span></span> <span data-ttu-id="6b04e-113">Pour plus d’informations, consultez [les conditions préalables.](m365d-configure-auto-investigation-response.md#prerequisites-for-automated-investigation-and-response-in-microsoft-365-defender)</span><span class="sxs-lookup"><span data-stu-id="6b04e-113">For more information, see the [prerequisites](m365d-configure-auto-investigation-response.md#prerequisites-for-automated-investigation-and-response-in-microsoft-365-defender).</span></span>

## <a name="review-pending-actions-in-the-action-center"></a><span data-ttu-id="6b04e-114">Passer en revue les actions en attente dans le centre de actions</span><span class="sxs-lookup"><span data-stu-id="6b04e-114">Review pending actions in the Action center</span></span>

<span data-ttu-id="6b04e-115">Il est important d’approuver (ou de refuser) les actions en attente dès que possible de sorte que vos enquêtes automatisées puissent se poursuivre et se terminer dans un délai raisonnable.</span><span class="sxs-lookup"><span data-stu-id="6b04e-115">It's important to approve (or reject) pending actions as soon as possible so that your automated investigations can proceed and complete in a timely manner.</span></span> 

1. <span data-ttu-id="6b04e-116">Accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="6b04e-116">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in.</span></span> 

2. <span data-ttu-id="6b04e-117">Dans le volet de navigation, choisissez **Centre de notifications**.</span><span class="sxs-lookup"><span data-stu-id="6b04e-117">In the navigation pane, choose **Action center**.</span></span> 

3. <span data-ttu-id="6b04e-118">Dans le centre de notifications, dans l’onglet **En attente**, sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="6b04e-118">In the Action Center, on the **Pending** tab, select an item in the list.</span></span> <span data-ttu-id="6b04e-119">Son volet volant s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="6b04e-119">Its flyout pane opens.</span></span> <span data-ttu-id="6b04e-120">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="6b04e-120">Here's an example.</span></span>

   ![Approuver ou rejeter une action](../../media/air-actioncenter-itemselected.png)

4. <span data-ttu-id="6b04e-122">Examinez les informations dans le volet volant, puis prenez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="6b04e-122">Review the information in the flyout pane, and then take one of the following steps:</span></span>
   - <span data-ttu-id="6b04e-123">Sélectionnez **Ouvrir la page Examen** pour afficher plus de détails sur l’enquête.</span><span class="sxs-lookup"><span data-stu-id="6b04e-123">Select **Open investigation page** to view more details about the investigation.</span></span>
   - <span data-ttu-id="6b04e-124">Sélectionnez **Approuver** pour lancer une action en attente.</span><span class="sxs-lookup"><span data-stu-id="6b04e-124">Select **Approve** to initiate a pending action.</span></span>
   - <span data-ttu-id="6b04e-125">Sélectionnez **Rejeter** pour empêcher une action en attente d’être prise.</span><span class="sxs-lookup"><span data-stu-id="6b04e-125">Select **Reject** to prevent a pending action from being taken.</span></span>
   - <span data-ttu-id="6b04e-126">Sélectionnez **Go hunt** (Aller à la recherche) pour passer [à la recherche avancée](advanced-hunting-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6b04e-126">Select **Go hunt** to go into [Advanced hunting](advanced-hunting-overview.md).</span></span> 

## <a name="undo-completed-actions"></a><span data-ttu-id="6b04e-127">Annuler les actions terminées</span><span class="sxs-lookup"><span data-stu-id="6b04e-127">Undo completed actions</span></span>

<span data-ttu-id="6b04e-128">Si vous avez déterminé qu’un appareil ou un fichier n’est pas une menace, vous pouvez annuler les actions de correction qui ont été prises, que ces actions soient prises automatiquement ou manuellement.</span><span class="sxs-lookup"><span data-stu-id="6b04e-128">If you’ve determined that a device or a file is not a threat, you can undo remediation actions that were taken, whether those actions were taken automatically or manually.</span></span> <span data-ttu-id="6b04e-129">Dans le centre de actions, sous **l’onglet** Historique, vous pouvez annuler l’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="6b04e-129">In the Action center, on the **History** tab, you can undo any of the following actions:</span></span>  

| <span data-ttu-id="6b04e-130">Source d’action</span><span class="sxs-lookup"><span data-stu-id="6b04e-130">Action source</span></span> | <span data-ttu-id="6b04e-131">Actions prises en charge</span><span class="sxs-lookup"><span data-stu-id="6b04e-131">Supported Actions</span></span> |
|:---|:---|
| <span data-ttu-id="6b04e-132">- Examen automatisé</span><span class="sxs-lookup"><span data-stu-id="6b04e-132">- Automated investigation</span></span> <br/><span data-ttu-id="6b04e-133">- Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="6b04e-133">- Microsoft Defender Antivirus</span></span> <br/><span data-ttu-id="6b04e-134">- Actions de réponse manuelles</span><span class="sxs-lookup"><span data-stu-id="6b04e-134">- Manual response actions</span></span> | <span data-ttu-id="6b04e-135">- Isoler l’appareil</span><span class="sxs-lookup"><span data-stu-id="6b04e-135">- Isolate device</span></span> <br/><span data-ttu-id="6b04e-136">- Restreindre l’exécution du code</span><span class="sxs-lookup"><span data-stu-id="6b04e-136">- Restrict code execution</span></span> <br/><span data-ttu-id="6b04e-137">- Mettre en quarantaine un fichier</span><span class="sxs-lookup"><span data-stu-id="6b04e-137">- Quarantine a file</span></span> <br/><span data-ttu-id="6b04e-138">- Supprimer une clé de Registre</span><span class="sxs-lookup"><span data-stu-id="6b04e-138">- Remove a registry key</span></span> <br/><span data-ttu-id="6b04e-139">- Arrêter un service</span><span class="sxs-lookup"><span data-stu-id="6b04e-139">- Stop a service</span></span> <br/><span data-ttu-id="6b04e-140">- Désactiver un pilote</span><span class="sxs-lookup"><span data-stu-id="6b04e-140">- Disable a driver</span></span> <br/><span data-ttu-id="6b04e-141">- Supprimer une tâche programmée</span><span class="sxs-lookup"><span data-stu-id="6b04e-141">- Remove a scheduled task</span></span> |

### <a name="undo-one-remediation-action"></a><span data-ttu-id="6b04e-142">Annuler une action de correction</span><span class="sxs-lookup"><span data-stu-id="6b04e-142">Undo one remediation action</span></span>

1. <span data-ttu-id="6b04e-143">Go to the Action center ( [https://security.microsoft.com/action-center](https://security.microsoft.com/action-center) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="6b04e-143">Go to the Action center ([https://security.microsoft.com/action-center](https://security.microsoft.com/action-center)) and sign in.</span></span>

2. <span data-ttu-id="6b04e-144">Sous **l’onglet** Historique, sélectionnez une action à annuler.</span><span class="sxs-lookup"><span data-stu-id="6b04e-144">On the **History** tab, select an action that you want to undo.</span></span>

3. <span data-ttu-id="6b04e-145">Dans le volet sur le côté droit de l’écran, sélectionnez **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="6b04e-145">In the pane on the right side of the screen, select **Undo**.</span></span>

### <a name="undo-multiple-remediation-actions"></a><span data-ttu-id="6b04e-146">Annuler plusieurs actions de correction</span><span class="sxs-lookup"><span data-stu-id="6b04e-146">Undo multiple remediation actions</span></span>

1. <span data-ttu-id="6b04e-147">Go to the Action center ( https://security.microsoft.com/action-center) and sign in.</span><span class="sxs-lookup"><span data-stu-id="6b04e-147">Go to the Action center (https://security.microsoft.com/action-center) and sign in.</span></span>

2. <span data-ttu-id="6b04e-148">Sous **l’onglet** Historique, sélectionnez les actions à annuler.</span><span class="sxs-lookup"><span data-stu-id="6b04e-148">On the **History** tab, select the actions that you want to undo.</span></span> <span data-ttu-id="6b04e-149">Veillez à sélectionner les éléments qui ont le même type d’action.</span><span class="sxs-lookup"><span data-stu-id="6b04e-149">Make sure to select items that have the same Action type.</span></span> <span data-ttu-id="6b04e-150">Un volet volant s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="6b04e-150">A flyout pane opens.</span></span>

3. <span data-ttu-id="6b04e-151">Dans le volet volant, sélectionnez **Annuler.**</span><span class="sxs-lookup"><span data-stu-id="6b04e-151">In the flyout pane, select **Undo**.</span></span>

### <a name="to-remove-a-file-from-quarantine-across-multiple-devices"></a><span data-ttu-id="6b04e-152">Pour supprimer un fichier de la quarantaine sur plusieurs appareils</span><span class="sxs-lookup"><span data-stu-id="6b04e-152">To remove a file from quarantine across multiple devices</span></span> 

1. <span data-ttu-id="6b04e-153">Go to the Action center ( [https://security.microsoft.com/action-center](https://security.microsoft.com/action-center) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="6b04e-153">Go to the Action center ([https://security.microsoft.com/action-center](https://security.microsoft.com/action-center)) and sign in.</span></span>

2. <span data-ttu-id="6b04e-154">Sous **l’onglet** Historique, sélectionnez un fichier dont le type de fichier de mise en **quarantaine** est action.</span><span class="sxs-lookup"><span data-stu-id="6b04e-154">On the **History** tab, select a file that has a **Quarantine file** Action type.</span></span>

3. <span data-ttu-id="6b04e-155">Dans le volet sur le côté droit de l’écran, sélectionnez Appliquer à **X plus d’instances** de ce fichier, puis **sélectionnez Annuler**.</span><span class="sxs-lookup"><span data-stu-id="6b04e-155">In the pane on the right side of the screen, select **Apply to X more instances of this file**, and then select **Undo**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6b04e-156">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="6b04e-156">Next steps</span></span>

- [<span data-ttu-id="6b04e-157">Consulter les détails et les résultats d'un examen automatisé</span><span class="sxs-lookup"><span data-stu-id="6b04e-157">View the details and results of an automated investigation</span></span>](m365d-autoir-results.md)
- [<span data-ttu-id="6b04e-158">Corriger les faux positifs ou les faux négatifs)</span><span class="sxs-lookup"><span data-stu-id="6b04e-158">Address false positives or false negatives)</span></span>](m365d-autoir-report-false-positives-negatives.md)
