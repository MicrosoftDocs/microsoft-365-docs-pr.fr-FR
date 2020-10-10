---
title: Passer en revue et approuver les actions de correction en attente dans l’instruction et la réponse automatisées
keywords: AIR, autoIR, ATP, automatisation, analyse, réponse, correction, menaces, avancé, menace, protection
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
- m365-initiative-defender-office365
description: Découvrez les actions de correction dans les fonctionnalités d’analyse et de réponse automatisées dans Office 365 Advanced Threat Protection Plan 2.
ms.openlocfilehash: 29a3c2f59ba85c2c5d9965c0c7f262dcba1ecda7
ms.sourcegitcommit: 5e1b8c959a081022826fb09358730096248507ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48411985"
---
# <a name="view-pending-or-completed-remediation-actions-following-an-automated-investigation-in-office-365"></a><span data-ttu-id="b8f84-104">Afficher les actions de correction en attente ou terminées à la suite d’une enquête automatisée dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b8f84-104">View pending or completed remediation actions following an automated investigation in Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]



![Page action de l’enquête par avion](../../media/air-investigationactionspage.png)

## <a name="approve-or-reject-pending-actions"></a><span data-ttu-id="b8f84-106">Approuver (ou rejeter) les actions en attente</span><span class="sxs-lookup"><span data-stu-id="b8f84-106">Approve (or reject) pending actions</span></span>

<span data-ttu-id="b8f84-107">Lors de l’affichage [des détails d’une enquête](air-view-investigation-results.md), vous pouvez approuver ou refuser les actions correctives en attente.</span><span class="sxs-lookup"><span data-stu-id="b8f84-107">While viewing the [details of an investigation](air-view-investigation-results.md), you can approve or reject any pending remediation actions.</span></span> <span data-ttu-id="b8f84-108">Nous vous recommandons de le faire dès que possible pour que vos investigations automatiques soient terminées.</span><span class="sxs-lookup"><span data-stu-id="b8f84-108">We recommend doing this as soon as possible so that your automated investigations complete.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8f84-109">Les autorisations appropriées sont requises pour approuver ou rejeter les actions correctives.</span><span class="sxs-lookup"><span data-stu-id="b8f84-109">Appropriate permissions are required to approve or reject remediation actions.</span></span> <span data-ttu-id="b8f84-110">Consultez la rubrique [Required Permissions to use air Capabilities](office-365-air.md#required-permissions-to-use-air-capabilities).</span><span class="sxs-lookup"><span data-stu-id="b8f84-110">See [Required permissions to use AIR capabilities](office-365-air.md#required-permissions-to-use-air-capabilities).</span></span>

1. <span data-ttu-id="b8f84-111">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="b8f84-111">Go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="b8f84-112">Cette opération vous permet d’accéder au centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="b8f84-112">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="b8f84-113">Accédez aux enquêtes de **gestion des menaces**  >  **Investigations**.</span><span class="sxs-lookup"><span data-stu-id="b8f84-113">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="b8f84-114">Dans la liste des enquêtes, sélectionnez un élément dans la colonne **ID** .</span><span class="sxs-lookup"><span data-stu-id="b8f84-114">In the list of investigations, select an item in the **ID** column.</span></span> 

4. <span data-ttu-id="b8f84-115">Sélectionnez l’onglet **actions** .</span><span class="sxs-lookup"><span data-stu-id="b8f84-115">Select the **Actions** tab.</span></span>

5. <span data-ttu-id="b8f84-116">Sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="b8f84-116">Select an item in the list.</span></span> <span data-ttu-id="b8f84-117">(Cela active les boutons approuver et rejeter.)</span><span class="sxs-lookup"><span data-stu-id="b8f84-117">(This activates the Approve and Reject buttons.)</span></span>

6. <span data-ttu-id="b8f84-118">Examinez les informations disponibles pour les éléments que vous avez sélectionnés, puis approuvez ou rejetez la ou les actions.</span><span class="sxs-lookup"><span data-stu-id="b8f84-118">Review available information for the item(s) you selected, and then either approve or reject the action(s).</span></span> 
   - <span data-ttu-id="b8f84-119">**Approuver** : le début de la correction.</span><span class="sxs-lookup"><span data-stu-id="b8f84-119">**Approve** allows remediation to begin.</span></span>
   - <span data-ttu-id="b8f84-120">Le **rejet** n’effectue aucune action supplémentaire</span><span class="sxs-lookup"><span data-stu-id="b8f84-120">**Reject** takes no further action</span></span>

## <a name="next-steps"></a><span data-ttu-id="b8f84-121">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="b8f84-121">Next steps</span></span>

- [<span data-ttu-id="b8f84-122">Détails et résultats d’une enquête automatisée dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b8f84-122">Details and results of an automated investigation in Office 365</span></span>](air-view-investigation-results.md)

- [<span data-ttu-id="b8f84-123">Utiliser l’Explorateur de menaces</span><span class="sxs-lookup"><span data-stu-id="b8f84-123">Use Threat Explorer</span></span>](threat-explorer.md)
