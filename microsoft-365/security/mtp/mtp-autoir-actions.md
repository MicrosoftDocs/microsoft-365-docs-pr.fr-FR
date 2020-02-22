---
title: Approuver ou rejeter des actions en attente suite à une enquête automatisée
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
ms.topic: conceptual
ms.custom: autoir
ms.openlocfilehash: 5118f7fddaee0fa768675597dee862eb75e4ed96
ms.sourcegitcommit: 48b69caf6550e68cb14472ea8cfc76b53e7ae9c6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/21/2020
ms.locfileid: "42225492"
---
# <a name="approve-or-reject-pending-actions-from-automated-investigations"></a><span data-ttu-id="0c0c8-104">Approuver ou rejeter des actions en attente provenant d’une enquête automatisée</span><span class="sxs-lookup"><span data-stu-id="0c0c8-104">Approve or reject pending actions from automated investigations</span></span>

<span data-ttu-id="0c0c8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0c0c8-105">**Applies to:**</span></span>
- <span data-ttu-id="0c0c8-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="0c0c8-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="0c0c8-107">Lorsqu’une enquête automatisée s’exécute, elle peut engendrer une ou plusieurs [actions de correction](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-remediation-actions) nécessitant une approbation pour continuer.</span><span class="sxs-lookup"><span data-stu-id="0c0c8-107">When an automated investigation runs, it can result in one or more [remediation actions](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-remediation-actions) that require approval to proceed.</span></span> <span data-ttu-id="0c0c8-108">Par exemple, il peut être nécessaire de supprimer un cluster d’e-mails ou un fichier mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="0c0c8-108">For example, a cluster of email messages might need to be deleted, or a quarantined file might need to be removed.</span></span> <span data-ttu-id="0c0c8-109">Il est important d’approuver (ou de refuser) les actions en attente dès que possible de sorte que vos enquêtes automatisées puissent se poursuivre et se terminer dans un délai raisonnable.</span><span class="sxs-lookup"><span data-stu-id="0c0c8-109">It's important to approve (or reject) pending actions as soon as possible so that your automated investigations can proceed and complete in a timely manner.</span></span> 

> [!TIP]
> <span data-ttu-id="0c0c8-110">Si vous pensez qu’un message a été manqué ou incorrectement détecté par les fonctionnalités d’analyse et de réponse automatiques dans Microsoft Threat Protection, faites-le nous savoir.</span><span class="sxs-lookup"><span data-stu-id="0c0c8-110">If you think something was missed or wrongly detected by automated investigation and response features in Microsoft Threat Protection, let us know!</span></span> <span data-ttu-id="0c0c8-111">Découvrez [Comment signaler des faux positifs/négatifs dans les capacités d’inspection et de réponse automatiques de Microsoft Threat Protection](mtp-autoir-report-false-positives-negatives.md).</span><span class="sxs-lookup"><span data-stu-id="0c0c8-111">See [How to report false positives/negatives in automated investigation and response (AIR) capabilities in Microsoft Threat Protection](mtp-autoir-report-false-positives-negatives.md).</span></span>

<span data-ttu-id="0c0c8-112">Les actions en attente peuvent être examinées et approuvées à l’aide de l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0c0c8-112">Pending actions can be reviewed and approved by using one of several methods:</span></span>
- [<span data-ttu-id="0c0c8-113">Utiliser le Centre de notifications</span><span class="sxs-lookup"><span data-stu-id="0c0c8-113">Use the Action center</span></span>](#review-a-pending-action-in-the-action-center)
- [<span data-ttu-id="0c0c8-114">Utiliser la vue Détails de l’enquête</span><span class="sxs-lookup"><span data-stu-id="0c0c8-114">Use the investigation details view</span></span>](#review-a-pending-action-in-the-investigation-details-view)

> [!NOTE]
> <span data-ttu-id="0c0c8-115">Vous devez disposer des [autorisations appropriées](mtp-action-center.md#required-permissions-for-action-center-tasks) pour approuver ou rejeter les actions de correction.</span><span class="sxs-lookup"><span data-stu-id="0c0c8-115">You must have [appropriate permissions](mtp-action-center.md#required-permissions-for-action-center-tasks) to approve or reject remediation actions.</span></span>

## <a name="review-a-pending-action-in-the-action-center"></a><span data-ttu-id="0c0c8-116">Examiner une action en attente dans le centre de notifications</span><span class="sxs-lookup"><span data-stu-id="0c0c8-116">Review a pending action in the Action center</span></span>

1. <span data-ttu-id="0c0c8-117">Accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="0c0c8-117">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in.</span></span> 

2. <span data-ttu-id="0c0c8-118">Dans le volet de navigation, choisissez **Centre de notifications**.</span><span class="sxs-lookup"><span data-stu-id="0c0c8-118">In the navigation pane, choose **Action center**.</span></span> 

3. <span data-ttu-id="0c0c8-119">Dans le centre de notifications, dans l’onglet **En attente**, sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="0c0c8-119">In the Action Center, on the **Pending** tab, select an item in the list.</span></span> 

    - <span data-ttu-id="0c0c8-120">Si vous sélectionnez un élément dans la colonne **Numéro de l’enquête**, la page Détails de l’enquête s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="0c0c8-120">If you select an item in the **Investigation number** column, the investigation details page opens.</span></span> <span data-ttu-id="0c0c8-121">Là, vous pouvez afficher les résultats de l’enquête, puis approuver ou rejeter l’action recommandée.</span><span class="sxs-lookup"><span data-stu-id="0c0c8-121">There, you can view the results of the investigation, and then either approve or reject the recommended action.</span></span>
 
    - <span data-ttu-id="0c0c8-122">Si vous sélectionnez une ligne dans la liste, un menu volant affiche des informations relatives à cet élément.</span><span class="sxs-lookup"><span data-stu-id="0c0c8-122">If you select a row in the list, a flyout opens, where you can view information about that item.</span></span> <br/>![Approuver ou rejeter une action](../../media/air-actioncenter-itemselected.png)<br/><span data-ttu-id="0c0c8-124">Utilisez les liens pour afficher une alerte ou une enquête associée, puis approuvez ou refusez l’action.</span><span class="sxs-lookup"><span data-stu-id="0c0c8-124">Use the links to view an associated alert or an investigation, and approve or reject the action.</span></span>

## <a name="review-a-pending-action-in-the-investigation-details-view"></a><span data-ttu-id="0c0c8-125">Examiner une action en attente dans la vue de détails de l’enquête</span><span class="sxs-lookup"><span data-stu-id="0c0c8-125">Review a pending action in the investigation details view</span></span>

![Détails de l’enquête](../../media/mtp-air-investdetails.png)

1. <span data-ttu-id="0c0c8-127">Sur une page de [détails de l’enquête](mtp-autoir-results.md), sélectionnez l’onglet **Actions en attente** (ou **Actions**). Les éléments en attente d’approbation sont répertoriés ici.</span><span class="sxs-lookup"><span data-stu-id="0c0c8-127">On an [investigation details](mtp-autoir-results.md) page, select the **Pending actions** (or **Actions**) tab. Items that are pending approval are listed here.</span></span>

2. <span data-ttu-id="0c0c8-128">Sélectionnez un élément dans la liste, puis choisissez **Approuver** ou **Rejeter**.</span><span class="sxs-lookup"><span data-stu-id="0c0c8-128">Select an item in the list, and then choose **Approve** or **Reject**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0c0c8-129">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="0c0c8-129">Next steps</span></span>

- <span data-ttu-id="0c0c8-130">[En savoir plus sur le centre de notifications](mtp-action-center.md).</span><span class="sxs-lookup"><span data-stu-id="0c0c8-130">[Learn more about the Action center](mtp-action-center.md)</span></span>
- [<span data-ttu-id="0c0c8-131">En savoir plus sur les incidents</span><span class="sxs-lookup"><span data-stu-id="0c0c8-131">Learn more about incidents</span></span>](incidents-overview.md)
- [<span data-ttu-id="0c0c8-132">En savoir plus sur le repérage</span><span class="sxs-lookup"><span data-stu-id="0c0c8-132">Learn about hunting</span></span>](advanced-hunting-overview.md)
