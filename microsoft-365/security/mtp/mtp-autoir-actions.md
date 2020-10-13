---
title: Approuver ou rejeter les actions en attente à la suite d’une enquête automatisée
description: Utiliser le centre d’actions pour gérer les actions liées à une enquête et une réponse automatisées
keywords: action, center, autoair, automated, investigation, response, remediation
search.appverid: met150
ms.prod: microsoft-365-enterprise
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
ms.date: 09/16/2020
ms.openlocfilehash: 22a40e3c0c804800f2de02e705d1dfec6e296db0
ms.sourcegitcommit: de600339b08951d6dd3933288a8da2327a4b6ef3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/13/2020
ms.locfileid: "48429610"
---
# <a name="approve-or-reject-pending-actions-following-an-automated-investigation"></a><span data-ttu-id="eee37-104">Approuver ou rejeter les actions en attente à la suite d’une enquête automatisée</span><span class="sxs-lookup"><span data-stu-id="eee37-104">Approve or reject pending actions following an automated investigation</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="eee37-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="eee37-105">**Applies to:**</span></span>
- <span data-ttu-id="eee37-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="eee37-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="eee37-107">Lorsqu’une enquête automatisée s’exécute, elle peut engendrer une ou plusieurs [actions de correction](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-remediation-actions) nécessitant une approbation pour continuer.</span><span class="sxs-lookup"><span data-stu-id="eee37-107">When an automated investigation runs, it can result in one or more [remediation actions](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-remediation-actions) that require approval to proceed.</span></span> <span data-ttu-id="eee37-108">Par exemple, il peut être nécessaire de supprimer un cluster d’e-mails ou un fichier mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="eee37-108">For example, a cluster of email messages might need to be deleted, or a quarantined file might need to be removed.</span></span> <span data-ttu-id="eee37-109">Il est important d’approuver (ou de refuser) les actions en attente dès que possible de sorte que vos enquêtes automatisées puissent se poursuivre et se terminer dans un délai raisonnable.</span><span class="sxs-lookup"><span data-stu-id="eee37-109">It's important to approve (or reject) pending actions as soon as possible so that your automated investigations can proceed and complete in a timely manner.</span></span> 

> [!TIP]
> <span data-ttu-id="eee37-110">Si vous pensez qu’un message a été manqué ou incorrectement détecté par les fonctionnalités d’analyse et de réponse automatiques dans Microsoft Threat Protection, faites-le nous savoir.</span><span class="sxs-lookup"><span data-stu-id="eee37-110">If you think something was missed or wrongly detected by automated investigation and response features in Microsoft Threat Protection, let us know!</span></span> <span data-ttu-id="eee37-111">Découvrez [Comment signaler des faux positifs/négatifs dans les capacités d’inspection et de réponse automatiques de Microsoft Threat Protection](mtp-autoir-report-false-positives-negatives.md).</span><span class="sxs-lookup"><span data-stu-id="eee37-111">See [How to report false positives/negatives in automated investigation and response (AIR) capabilities in Microsoft Threat Protection](mtp-autoir-report-false-positives-negatives.md).</span></span>

<span data-ttu-id="eee37-112">Les actions en attente peuvent être révisées et approuvées à l’aide du [Centre de maintenance](#review-a-pending-action-in-the-action-center) ou de l' [Affichage détails](#review-a-pending-action-in-the-investigation-details-view)de l’enquête.</span><span class="sxs-lookup"><span data-stu-id="eee37-112">Pending actions can be reviewed and approved by using the [Action center](#review-a-pending-action-in-the-action-center) or the [investigation details view](#review-a-pending-action-in-the-investigation-details-view).</span></span>

> [!NOTE]
> <span data-ttu-id="eee37-113">Vous devez disposer des [autorisations appropriées](mtp-action-center.md#required-permissions-for-action-center-tasks) pour approuver ou rejeter les actions de correction.</span><span class="sxs-lookup"><span data-stu-id="eee37-113">You must have [appropriate permissions](mtp-action-center.md#required-permissions-for-action-center-tasks) to approve or reject remediation actions.</span></span>

## <a name="review-a-pending-action-in-the-action-center"></a><span data-ttu-id="eee37-114">Examiner une action en attente dans le centre de notifications</span><span class="sxs-lookup"><span data-stu-id="eee37-114">Review a pending action in the Action center</span></span>

1. <span data-ttu-id="eee37-115">Accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="eee37-115">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in.</span></span> 

2. <span data-ttu-id="eee37-116">Dans le volet de navigation, choisissez **Centre de notifications**.</span><span class="sxs-lookup"><span data-stu-id="eee37-116">In the navigation pane, choose **Action center**.</span></span> 

3. <span data-ttu-id="eee37-117">Dans le centre de notifications, dans l’onglet **En attente**, sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="eee37-117">In the Action Center, on the **Pending** tab, select an item in the list.</span></span> 

    - <span data-ttu-id="eee37-118">Si vous sélectionnez un élément dans la colonne **Numéro de l’enquête**, la page Détails de l’enquête s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="eee37-118">If you select an item in the **Investigation number** column, the investigation details page opens.</span></span> <span data-ttu-id="eee37-119">Là, vous pouvez afficher les résultats de l’enquête, puis approuver ou rejeter l’action recommandée.</span><span class="sxs-lookup"><span data-stu-id="eee37-119">There, you can view the results of the investigation, and then either approve or reject the recommended action.</span></span>
 
    - <span data-ttu-id="eee37-120">Si vous sélectionnez une ligne dans la liste, un menu volant affiche des informations relatives à cet élément.</span><span class="sxs-lookup"><span data-stu-id="eee37-120">If you select a row in the list, a flyout opens, where you can view information about that item.</span></span> <br/>![Approuver ou rejeter une action](../../media/air-actioncenter-itemselected.png)<br/><span data-ttu-id="eee37-122">Utilisez les liens pour afficher une alerte ou une enquête associée, puis approuvez ou refusez l’action.</span><span class="sxs-lookup"><span data-stu-id="eee37-122">Use the links to view an associated alert or an investigation, and approve or reject the action.</span></span>

## <a name="review-a-pending-action-in-the-investigation-details-view"></a><span data-ttu-id="eee37-123">Examiner une action en attente dans la vue de détails de l’enquête</span><span class="sxs-lookup"><span data-stu-id="eee37-123">Review a pending action in the investigation details view</span></span>

![Détails de l’enquête](../../media/mtp-air-investdetails.png)

1. <span data-ttu-id="eee37-125">Sur une page de [détails de l’enquête](mtp-autoir-results.md), sélectionnez l’onglet **Actions en attente** (ou **Actions**). Les éléments en attente d’approbation sont répertoriés ici.</span><span class="sxs-lookup"><span data-stu-id="eee37-125">On an [investigation details](mtp-autoir-results.md) page, select the **Pending actions** (or **Actions**) tab. Items that are pending approval are listed here.</span></span>

2. <span data-ttu-id="eee37-126">Sélectionnez un élément dans la liste, puis choisissez **Approuver** ou **Rejeter**.</span><span class="sxs-lookup"><span data-stu-id="eee37-126">Select an item in the list, and then choose **Approve** or **Reject**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="eee37-127">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="eee37-127">Next steps</span></span>

- [<span data-ttu-id="eee37-128">Consulter les détails et les résultats d'un examen automatisé</span><span class="sxs-lookup"><span data-stu-id="eee37-128">View the details and results of an automated investigation</span></span>](mtp-autoir-results.md)
- [<span data-ttu-id="eee37-129">Gérer les faux positifs/négatifs dans les fonctionnalités d’analyse et de réponse automatisées</span><span class="sxs-lookup"><span data-stu-id="eee37-129">Handle false positives/negatives in automated investigation and response capabilities</span></span>](mtp-autoir-report-false-positives-negatives.md)
