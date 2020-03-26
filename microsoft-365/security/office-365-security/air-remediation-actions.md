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
ms.openlocfilehash: 1dff52fe1bdab364e03bc42afc84c9b54696ccf5
ms.sourcegitcommit: 58c1b4208a5e231463091573e40696d08fc39b8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2020
ms.locfileid: "42955532"
---
# <a name="remediation-actions-following-an-automated-investigation-in-office-365"></a><span data-ttu-id="8ab34-104">Actions de correction suite à une enquête automatisée dans Office 365</span><span class="sxs-lookup"><span data-stu-id="8ab34-104">Remediation actions following an automated investigation in Office 365</span></span>

## <a name="remediation-actions"></a><span data-ttu-id="8ab34-105">Actions de correction</span><span class="sxs-lookup"><span data-stu-id="8ab34-105">Remediation actions</span></span>

<span data-ttu-id="8ab34-106">[Les fonctionnalités d’analyse et de réponse automatisées](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air) (air) dans [Office 365 Advanced Threat Protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp) (Office 365 ATP) plan 2 incluent certaines actions de correction.</span><span class="sxs-lookup"><span data-stu-id="8ab34-106">[Automated investigation and response capabilities](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air) (AIR) in [Office 365 Advanced Threat Protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp) (Office 365 ATP) Plan 2 include certain remediation actions.</span></span> <span data-ttu-id="8ab34-107">Lorsqu’une enquête automatisée est en cours d’exécution ou qu’elle est terminée, vous verrez généralement une ou plusieurs actions correctives qui nécessitent l’approbation de votre équipe d’opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8ab34-107">Whenever an automated investigation is running or has completed, you'll typically see one or more remediation actions that require approval by your security operations team to proceed.</span></span> 

<span data-ttu-id="8ab34-108">Le tableau suivant récapitule les actions de correction actuellement disponibles dans Office 365 ATP.</span><span class="sxs-lookup"><span data-stu-id="8ab34-108">The following table summarizes the remediation actions that are currently available in Office 365 ATP.</span></span> 

|<span data-ttu-id="8ab34-109">Opération</span><span class="sxs-lookup"><span data-stu-id="8ab34-109">Action</span></span> | <span data-ttu-id="8ab34-110">Description</span><span class="sxs-lookup"><span data-stu-id="8ab34-110">Description</span></span> |
|-----|-----|
|<span data-ttu-id="8ab34-111">Bloquer l’URL (heure du clic)</span><span class="sxs-lookup"><span data-stu-id="8ab34-111">Block URL (time-of-click)</span></span> |<span data-ttu-id="8ab34-112">Protège contre les messages électroniques et les documents contenant des URL malveillantes.</span><span class="sxs-lookup"><span data-stu-id="8ab34-112">Protects against email messages and documents that contain malicious URLs.</span></span> <span data-ttu-id="8ab34-113">Cela permet de bloquer les liens malveillants et les pages Web associées via [des liens fiables](https://docs.microsoft.com/microsoft-365/security/office-365-security/atp-safe-links) lorsque l’utilisateur clique sur un lien dans un fichier Office existant ou dans un ancien message électronique.</span><span class="sxs-lookup"><span data-stu-id="8ab34-113">This enables the blocking of malicious links and any related webpages via [Safe Links](https://docs.microsoft.com/microsoft-365/security/office-365-security/atp-safe-links) when the user clicks a link in an existing Office file or in an older email message.</span></span> |
|<span data-ttu-id="8ab34-114">Courrier électronique de suppression douce</span><span class="sxs-lookup"><span data-stu-id="8ab34-114">Soft delete email</span></span>  |<span data-ttu-id="8ab34-115">Suppression logicielle de messages électroniques spécifiques de la boîte aux lettres d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8ab34-115">Soft delete specific email messages from a user's mailbox.</span></span> <br/><span data-ttu-id="8ab34-116">Un message supprimé (récupérable) est déplacé vers le dossier éléments récupérables d’un utilisateur et est conservé jusqu’à l’expiration de la période de rétention des éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="8ab34-116">A soft-deleted message is moved to a user's Recoverable Items folder and is retained until the deleted item retention period expires.</span></span> |
|<span data-ttu-id="8ab34-117">Clusters de suppression de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="8ab34-117">Soft delete email clusters</span></span>  |<span data-ttu-id="8ab34-118">Soft supprime les messages électroniques malveillants qui correspondent à une requête de toutes les boîtes aux lettres des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8ab34-118">Soft delete malicious email messages matching a query from all users' mailboxes.</span></span> <br/><span data-ttu-id="8ab34-119">Les messages supprimés de manière récupérable sont déplacés vers le dossier éléments récupérables des utilisateurs et sont conservés jusqu’à l’expiration de la période de rétention des éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="8ab34-119">Soft-deleted messages are moved to users' Recoverable Items folder and are retained until the deleted item retention period expires.</span></span> |
|<span data-ttu-id="8ab34-120">Désactiver le transfert de courrier externe</span><span class="sxs-lookup"><span data-stu-id="8ab34-120">Turn off external mail forwarding</span></span> |<span data-ttu-id="8ab34-121">Supprime une règle de transfert d’une boîte aux lettres d’un utilisateur final spécifique.</span><span class="sxs-lookup"><span data-stu-id="8ab34-121">Removes a forwarding rule from a specific end user's mailbox.</span></span>|

> [!NOTE]
> <span data-ttu-id="8ab34-122">Dans Office 365 ATP, aucune action de correction n’est effectuée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="8ab34-122">In Office 365 ATP, no remediation actions are taken automatically.</span></span> <span data-ttu-id="8ab34-123">Les actions de correction ne sont prises qu’après approbation de l’équipe de sécurité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8ab34-123">Remediation actions are taken only upon approval by your organization's security team.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="8ab34-124">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="8ab34-124">Next steps</span></span>

- [<span data-ttu-id="8ab34-125">Afficher les actions de correction en attente ou terminées à la suite d’une enquête automatisée dans Office 365</span><span class="sxs-lookup"><span data-stu-id="8ab34-125">View pending or completed remediation actions following an automated investigation in Office 365</span></span>](air-review-approve-pending-completed-actions.md)

- [<span data-ttu-id="8ab34-126">Détails et résultats d’une enquête automatisée dans Office 365</span><span class="sxs-lookup"><span data-stu-id="8ab34-126">Details and results of an automated investigation in Office 365</span></span>](air-view-investigation-results.md)

## <a name="related-articles"></a><span data-ttu-id="8ab34-127">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="8ab34-127">Related articles</span></span>

- [<span data-ttu-id="8ab34-128">Enquête automatisée dans Microsoft Defender protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="8ab34-128">Automated investigation in Microsoft Defender Advanced Threat Protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)

- [<span data-ttu-id="8ab34-129">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="8ab34-129">Microsoft Threat Protection</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/microsoft-threat-protection)