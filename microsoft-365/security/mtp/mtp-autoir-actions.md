---
title: Approuver ou rejeter des actions en attente suite à une enquête automatisée
description: Utiliser le centre d’actions pour gérer les actions liées à une enquête et une réponse automatisées
keywords: action, center, autoair, automated, investigation, response, remediation
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: deniseb
author: denisebmsft
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: conceptual
ms.custom: autoir
ms.openlocfilehash: edc952a0361ee8cfa6ed3df2eaf80f0fc4bf7fd5
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40808459"
---
# <a name="approve-or-reject-pending-actions-from-automated-investigations"></a><span data-ttu-id="9c5e9-104">Approuver ou rejeter des actions en attente provenant d’une enquête automatisée</span><span class="sxs-lookup"><span data-stu-id="9c5e9-104">Approve or reject pending actions from automated investigations</span></span>

<span data-ttu-id="9c5e9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9c5e9-105">**Applies to:**</span></span>
- <span data-ttu-id="9c5e9-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="9c5e9-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="9c5e9-107">Lorsqu’une enquête automatisée s’exécute, elle peut engendrer une ou plusieurs [actions de correction](mtp-action-center.md#remediation-actions) nécessitant une approbation pour continuer.</span><span class="sxs-lookup"><span data-stu-id="9c5e9-107">When an automated investigation runs, it can result in one or more [remediation actions](mtp-action-center.md#remediation-actions) that require approval to proceed.</span></span> <span data-ttu-id="9c5e9-108">Par exemple, il peut être nécessaire de supprimer un cluster d’e-mails ou un fichier mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="9c5e9-108">For example, a cluster of email messages might need to be deleted, or a quarantined file might need to be removed.</span></span> <span data-ttu-id="9c5e9-109">Il est important d’approuver (ou de refuser) les actions en attente dès que possible de sorte que vos enquêtes automatisées puissent se poursuivre et se terminer dans un délai raisonnable.</span><span class="sxs-lookup"><span data-stu-id="9c5e9-109">It's important to approve (or reject) pending actions as soon as possible so that your automated investigations can proceed and complete in a timely manner.</span></span> 

<span data-ttu-id="9c5e9-110">Les actions en attente peuvent être examinées et approuvées à l’aide de l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9c5e9-110">Pending actions can be reviewed and approved by using one of several methods:</span></span>
- [<span data-ttu-id="9c5e9-111">Utiliser le Centre de notifications</span><span class="sxs-lookup"><span data-stu-id="9c5e9-111">Use the Action center</span></span>](#review-a-pending-action-in-the-action-center)
- [<span data-ttu-id="9c5e9-112">Utiliser la vue Détails de l’enquête</span><span class="sxs-lookup"><span data-stu-id="9c5e9-112">Use the investigation details view</span></span>](#review-a-pending-action-in-the-investigation-details-view)

> [!NOTE]
> <span data-ttu-id="9c5e9-113">Vous devez disposer des [autorisations appropriées](mtp-action-center.md#required-permissions-for-action-center-tasks) pour approuver ou rejeter les actions de correction.</span><span class="sxs-lookup"><span data-stu-id="9c5e9-113">You must have [appropriate permissions](mtp-action-center.md#required-permissions-for-action-center-tasks) to approve or reject remediation actions.</span></span>

## <a name="review-a-pending-action-in-the-action-center"></a><span data-ttu-id="9c5e9-114">Examiner une action en attente dans le centre de notifications</span><span class="sxs-lookup"><span data-stu-id="9c5e9-114">Review a pending action in the Action center</span></span>

1. <span data-ttu-id="9c5e9-115">Accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="9c5e9-115">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in.</span></span> 

2. <span data-ttu-id="9c5e9-116">Dans le volet de navigation, choisissez **Centre de notifications**.</span><span class="sxs-lookup"><span data-stu-id="9c5e9-116">In the navigation pane, choose **Action center**.</span></span> 

3. <span data-ttu-id="9c5e9-117">Dans le centre de notifications, dans l’onglet **En attente**, sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="9c5e9-117">In the Action Center, on the **Pending** tab, select an item in the list.</span></span> 

    - <span data-ttu-id="9c5e9-118">Si vous sélectionnez un élément dans la colonne **Numéro de l’enquête**, la page Détails de l’enquête s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="9c5e9-118">If you select an item in the **Investigation number** column, the investigation details page opens.</span></span> <span data-ttu-id="9c5e9-119">Là, vous pouvez afficher les résultats de l’enquête, puis approuver ou rejeter l’action recommandée.</span><span class="sxs-lookup"><span data-stu-id="9c5e9-119">There, you can view the results of the investigation, and then either approve or reject the recommended action.</span></span>
 
    - <span data-ttu-id="9c5e9-120">Si vous sélectionnez une ligne dans la liste, un menu volant affiche des informations relatives à cet élément.</span><span class="sxs-lookup"><span data-stu-id="9c5e9-120">If you select a row in the list, a flyout opens, where you can view information about that item.</span></span> <br/>![Approuver ou rejeter une action](../images/air-actioncenter-itemselected.png)<br/><span data-ttu-id="9c5e9-122">Utilisez les liens pour afficher une alerte ou une enquête associée, puis approuvez ou refusez l’action.</span><span class="sxs-lookup"><span data-stu-id="9c5e9-122">Use the links to view an associated alert or an investigation, and approve or reject the action.</span></span>

## <a name="review-a-pending-action-in-the-investigation-details-view"></a><span data-ttu-id="9c5e9-123">Examiner une action en attente dans la vue de détails de l’enquête</span><span class="sxs-lookup"><span data-stu-id="9c5e9-123">Review a pending action in the investigation details view</span></span>

![Détails de l’enquête](../images/mtp-air-investdetails.png)

1. <span data-ttu-id="9c5e9-125">Sur une page de [détails de l’enquête](mtp-autoir-results.md), sélectionnez l’onglet **Actions en attente** (ou **Actions**). Les éléments en attente d’approbation sont répertoriés ici.</span><span class="sxs-lookup"><span data-stu-id="9c5e9-125">On an [investigation details](mtp-autoir-results.md) page, select the **Pending actions** (or **Actions**) tab. Items that are pending approval are listed here.</span></span>

2. <span data-ttu-id="9c5e9-126">Sélectionnez un élément dans la liste, puis choisissez **Approuver** ou **Rejeter**.</span><span class="sxs-lookup"><span data-stu-id="9c5e9-126">Select an item in the list, and then choose **Approve** or **Reject**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9c5e9-127">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9c5e9-127">Next steps</span></span>

- <span data-ttu-id="9c5e9-128">[En savoir plus sur le centre de notifications](mtp-action-center.md).</span><span class="sxs-lookup"><span data-stu-id="9c5e9-128">[Learn more about the Action center](mtp-action-center.md)</span></span>
- [<span data-ttu-id="9c5e9-129">En savoir plus sur les incidents</span><span class="sxs-lookup"><span data-stu-id="9c5e9-129">Learn more about incidents</span></span>](incidents-overview.md)
- [<span data-ttu-id="9c5e9-130">En savoir plus sur le repérage</span><span class="sxs-lookup"><span data-stu-id="9c5e9-130">Learn about hunting</span></span>](advanced-hunting-overview.md)
