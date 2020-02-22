---
title: Actions correctives dans Office 365 automatisation de l’analyse et de la réponse
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
ms.collection: M365-security-compliance
description: Découvrez les actions de correction dans les fonctionnalités d’analyse et de réponse automatisées dans Office 365 Advanced Threat Protection Plan 2.
ms.openlocfilehash: e75ef1523247cbddcf6cb28d69a889db1de8e42f
ms.sourcegitcommit: 8876c216954b94adce9cdf493c49bd5a10190a3a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/21/2020
ms.locfileid: "42228530"
---
# <a name="remediation-actions-following-an-automated-investigation-in-office-365"></a><span data-ttu-id="95047-104">Actions de correction suite à une enquête automatisée dans Office 365</span><span class="sxs-lookup"><span data-stu-id="95047-104">Remediation actions following an automated investigation in Office 365</span></span>

## <a name="remediation-actions-overview"></a><span data-ttu-id="95047-105">Vue d’ensemble des actions de correction</span><span class="sxs-lookup"><span data-stu-id="95047-105">Remediation actions overview</span></span>

<span data-ttu-id="95047-106">[Les fonctionnalités d’analyse et de réponse automatisées](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air) dans Office 365 protection avancée contre les menaces incluent certaines actions de correction.</span><span class="sxs-lookup"><span data-stu-id="95047-106">[Automated investigation and response capabilities](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air) in Office 365 Advanced Threat Protection include certain remediation actions.</span></span> <span data-ttu-id="95047-107">Lorsqu’une enquête automatisée est en cours d’exécution ou qu’elle est terminée, vous verrez généralement une ou plusieurs actions correctives qui nécessitent l’approbation de votre équipe d’opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="95047-107">Whenever an automated investigation is running or has completed, you'll typically see one or more remediation actions that require approval by your security operations team to proceed.</span></span> <span data-ttu-id="95047-108">Le tableau suivant récapitule les actions de correction actuellement disponibles dans Office 365 Advanced Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="95047-108">The following table summarizes remediation actions currently available in Office 365 Advanced Threat Protection.</span></span> 

|<span data-ttu-id="95047-109">Opération</span><span class="sxs-lookup"><span data-stu-id="95047-109">Action</span></span> | <span data-ttu-id="95047-110">Description</span><span class="sxs-lookup"><span data-stu-id="95047-110">Description</span></span> |
|-----|-----|
|<span data-ttu-id="95047-111">Bloquer l’URL (heure du clic)</span><span class="sxs-lookup"><span data-stu-id="95047-111">Block URL (time-of-click)</span></span> |<span data-ttu-id="95047-112">Se protéger contre les e-mails et les documents contenant des URL malveillantes.</span><span class="sxs-lookup"><span data-stu-id="95047-112">Protect against emails and documents that contain malicious URLs.</span></span> <span data-ttu-id="95047-113">Cela permet de bloquer les liens malveillants et les pages Web associées via [des liens fiables](https://docs.microsoft.com/microsoft-365/security/office-365-security/atp-safe-links) lorsque l’utilisateur clique sur un lien dans un fichier Office existant ou dans un ancien message électronique.</span><span class="sxs-lookup"><span data-stu-id="95047-113">This enables the blocking of malicious links and any related webpages via [Safe Links](https://docs.microsoft.com/microsoft-365/security/office-365-security/atp-safe-links) when the user clicks a link in an existing Office file or in an older email message.</span></span> |
|<span data-ttu-id="95047-114">Courrier électronique de suppression douce</span><span class="sxs-lookup"><span data-stu-id="95047-114">Soft delete email</span></span>  |<span data-ttu-id="95047-115">Suppression logicielle de messages électroniques spécifiques de la boîte aux lettres d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="95047-115">Soft delete specific email messages from a user's mailbox</span></span>|
|<span data-ttu-id="95047-116">Clusters de suppression de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="95047-116">Soft delete email clusters</span></span>  |<span data-ttu-id="95047-117">Suppression logicielle de messages électroniques malveillants correspondant à une requête de toutes les boîtes aux lettres des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="95047-117">Soft delete malicious email messages matching a query from all users' mailboxes</span></span>|
|<span data-ttu-id="95047-118">Désactiver le transfert de courrier externe</span><span class="sxs-lookup"><span data-stu-id="95047-118">Turn off external mail forwarding</span></span> |<span data-ttu-id="95047-119">Supprime la règle de transfert d’une boîte aux lettres d’un utilisateur final spécifique.</span><span class="sxs-lookup"><span data-stu-id="95047-119">Removes forwarding rule from a specific end user's mailbox</span></span>|

## <a name="approve-or-reject-pending-actions"></a><span data-ttu-id="95047-120">Approuver (ou rejeter) les actions en attente</span><span class="sxs-lookup"><span data-stu-id="95047-120">Approve (or reject) pending actions</span></span>

![Page action de l’enquête par avion](../../media/air-investigationactionspage.png)

<span data-ttu-id="95047-122">Lors de l’affichage [des détails d’une enquête](air-view-investigation-results.md), vous pouvez approuver ou refuser les actions correctives en attente.</span><span class="sxs-lookup"><span data-stu-id="95047-122">While viewing the [details of an investigation](air-view-investigation-results.md), you can approve or reject any pending remediation actions.</span></span> <span data-ttu-id="95047-123">Nous vous recommandons de le faire dès que possible pour que vos investigations automatiques soient terminées.</span><span class="sxs-lookup"><span data-stu-id="95047-123">We recommend doing this as soon as possible so that your automated investigations complete.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95047-124">Les autorisations appropriées sont requises pour approuver ou rejeter les actions correctives.</span><span class="sxs-lookup"><span data-stu-id="95047-124">Appropriate permissions are required to approve or reject remediation actions.</span></span> <span data-ttu-id="95047-125">Consultez la rubrique [Required Permissions to use air Capabilities](office-365-air.md#required-permissions-to-use-air-capabilities).</span><span class="sxs-lookup"><span data-stu-id="95047-125">See [Required permissions to use AIR capabilities](office-365-air.md#required-permissions-to-use-air-capabilities).</span></span>

1. <span data-ttu-id="95047-126">Sélectionnez l’onglet **actions** .</span><span class="sxs-lookup"><span data-stu-id="95047-126">Select the **Actions** tab.</span></span>

2. <span data-ttu-id="95047-127">Sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="95047-127">Select an item in the list.</span></span> <span data-ttu-id="95047-128">(Cela active les boutons approuver et rejeter.)</span><span class="sxs-lookup"><span data-stu-id="95047-128">(This activates the Approve and Reject buttons.)</span></span>

3. <span data-ttu-id="95047-129">Examinez les informations disponibles pour les éléments que vous avez sélectionnés, puis approuvez ou rejetez la ou les actions.</span><span class="sxs-lookup"><span data-stu-id="95047-129">Review available information for the item(s) you selected, and then either approve or reject the action(s).</span></span> 
 - <span data-ttu-id="95047-130">**Approuver** : le début de la correction.</span><span class="sxs-lookup"><span data-stu-id="95047-130">**Approve** allows remediation to begin.</span></span>
 - <span data-ttu-id="95047-131">Le **rejet** n’effectue aucune action supplémentaire</span><span class="sxs-lookup"><span data-stu-id="95047-131">**Reject** takes no further action</span></span>

## <a name="related-articles"></a><span data-ttu-id="95047-132">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="95047-132">Related articles</span></span>

[<span data-ttu-id="95047-133">En savoir plus sur l’analyse et la réponse automatisées dans Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="95047-133">Learn about automated investigation and response in Microsoft Threat Protection</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-autoir)