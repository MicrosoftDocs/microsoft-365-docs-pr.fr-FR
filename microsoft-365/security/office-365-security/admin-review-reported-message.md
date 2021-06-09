---
title: Révision par l’administrateur des messages signalés
f1.keywords:
- NOCSH
ms.author: dansimp
author: dansimp
manager: dansimp
audience: Admin
ms.topic: how-to
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: Découvrez comment passer en revue les messages signalés et envoyer des commentaires à vos utilisateurs.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 7386f5b283e2bfabb76eee91d33dfda0e42ec7b1
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52769124"
---
# <a name="admin-review-for-reported-messages"></a><span data-ttu-id="8854c-103">Révision par l’administrateur des messages signalés</span><span class="sxs-lookup"><span data-stu-id="8854c-103">Admin review for reported messages</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

> [!NOTE]
> <span data-ttu-id="8854c-104">Les informations de cet article concernent un produit d’aperçu qui peut être considérablement modifié avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="8854c-104">The information in this article relates to a preview product that may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8854c-105">Ce document est fourni uniquement à des fins d’évaluation et d’exploration.</span><span class="sxs-lookup"><span data-stu-id="8854c-105">This document is provided for evaluation and exploration purposes only.</span></span>

<span data-ttu-id="8854c-106">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="8854c-106">**Applies to**</span></span>
- [<span data-ttu-id="8854c-107">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="8854c-107">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="8854c-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8854c-108">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="8854c-109">Dans Microsoft 365 organisations avec des boîtes aux lettres Exchange Online et Microsoft Defender pour Office 365, les administrateurs peuvent désormais renvoyer des messages de modèle aux utilisateurs finaux après avoir passé en revue les messages signalés.</span><span class="sxs-lookup"><span data-stu-id="8854c-109">In Microsoft 365 organizations with Exchange Online mailboxes and Microsoft Defender for Office 365, admins can now send templated messages back to end users after they review reported messages.</span></span> <span data-ttu-id="8854c-110">Cela peut être personnalisé pour votre organisation et en fonction du verdict de votre administrateur.</span><span class="sxs-lookup"><span data-stu-id="8854c-110">This can be customized for your organization and based on your admin’s verdict as well.</span></span>

<span data-ttu-id="8854c-111">Cette fonctionnalité est conçue pour envoyer des commentaires à vos utilisateurs, mais ne modifie pas les verdicts des messages dans le système.</span><span class="sxs-lookup"><span data-stu-id="8854c-111">This feature is designed to give feedback to your users but does not change the verdicts of messages in the system.</span></span> <span data-ttu-id="8854c-112">Pour aider Microsoft à mettre à jour et à améliorer ses filtres, vous devez envoyer des messages pour analyse à l’aide de [la soumission d’administrateur.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="8854c-112">To help Microsoft update and improve its filters, you will need to submit messages for analysis using [Admin submission](admin-submission.md).</span></span>

<span data-ttu-id="8854c-113">Vous ne pourrez marquer et avertir les utilisateurs des résultats de la révision que si le message a été signalé comme faux positifs ou [faux négatifs.](report-false-positives-and-false-negatives.md)</span><span class="sxs-lookup"><span data-stu-id="8854c-113">You will only be able to mark and notify users of review results if the message was reported as a [false positives or false negatives](report-false-positives-and-false-negatives.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="8854c-114">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="8854c-114">What do you need to know before you begin?</span></span>

- <span data-ttu-id="8854c-115">Pour modifier la configuration des soumissions d’utilisateurs, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="8854c-115">To modify the configuration for User submissions, you need to be a member of one of the following role groups:</span></span>
  - <span data-ttu-id="8854c-116">Administrateur de la gestion de l’organisation ou de la sécurité [dans Microsoft 365 de sécurité.](permissions-microsoft-365-security-center.md)</span><span class="sxs-lookup"><span data-stu-id="8854c-116">Organization Management or Security Administrator in the [Microsoft 365 security center](permissions-microsoft-365-security-center.md).</span></span>
  - <span data-ttu-id="8854c-117">Gestion de [l’organisation Exchange Online](/Exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="8854c-117">Organization Management in [Exchange Online](/Exchange/permissions-exo/permissions-exo).</span></span>

- <span data-ttu-id="8854c-118">Vous aurez également besoin d’accéder à la Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8854c-118">You'll also need access to the Exchange Online PowerShell.</span></span> <span data-ttu-id="8854c-119">Si le compte que vous essayez d’utiliser n’a pas accès à Exchange Online PowerShell, vous recevrez une erreur qui indique spécifier une adresse de messagerie dans *votre domaine.*</span><span class="sxs-lookup"><span data-stu-id="8854c-119">If the account that you're trying to use doesn't have access to Exchange Online PowerShell, you'll receive an error that says *Specify an email address in your domain*.</span></span> <span data-ttu-id="8854c-120">Pour plus d’informations sur l’activation ou la désactivation de l’accès Exchange Online PowerShell, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="8854c-120">For more information about enabling or disabling access to Exchange Online PowerShell, see the following topics:</span></span>
  - [<span data-ttu-id="8854c-121">Activer ou désactiver l’accès à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="8854c-121">Enable or disable access to Exchange Online PowerShell</span></span>](/powershell/exchange/disable-access-to-exchange-online-powershell)
  - [<span data-ttu-id="8854c-122">Règles d’accès client Exchange Online</span><span class="sxs-lookup"><span data-stu-id="8854c-122">Client Access Rules in Exchange Online</span></span>](/exchange/clients-and-mobile-in-exchange-online/client-access-rules/client-access-rules)

## <a name="configure-the-messages-used-to-notify-users"></a><span data-ttu-id="8854c-123">Configurer les messages utilisés pour avertir les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="8854c-123">Configure the messages used to notify users</span></span>

1. <span data-ttu-id="8854c-124">Dans le centre [Microsoft 365 de sécurité,](../defender/overview-security-center.md)allez à **Stratégies &** Stratégies de menace \>  \> **Stratégies De l’utilisateur a signalé les paramètres de message**.</span><span class="sxs-lookup"><span data-stu-id="8854c-124">In the [Microsoft 365 security center](../defender/overview-security-center.md), go to **Policies & rules** \> **Threat policies** \> **User reported message settings**.</span></span>

2. <span data-ttu-id="8854c-125">Si vous souhaitez spécifier le nom complet  de l’expéditeur, cochez la case Spécifier l’adresse de messagerie Office 365 à utiliser en tant qu’expéditeur dans la section **Notifications** par courrier électronique pour les résultats de l’avis de l’administrateur, puis entrez le nom que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="8854c-125">If you want to specify the sender display name, check the box for **Specify Office 365 email address to use as sender** under the **Email notifications for admin review results** section, and enter in the name you wish to use.</span></span> <span data-ttu-id="8854c-126">Il s’agit de l’adresse de messagerie qui sera visible dans Outlook et où les réponses seront envoyés.</span><span class="sxs-lookup"><span data-stu-id="8854c-126">This is the email address that will be visible in Outlook and where replies will go to.</span></span>

3. <span data-ttu-id="8854c-127">Si vous souhaitez personnaliser l’un des modèles, cliquez sur **Personnaliser la notification par courrier électronique.**</span><span class="sxs-lookup"><span data-stu-id="8854c-127">If you want to customize any of the templates, click **Customize email notification**.</span></span> <span data-ttu-id="8854c-128">Dans ce flyout, vous serez en mesure de personnaliser uniquement les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8854c-128">In this flyout, you will be able to customize only the following:</span></span>
    - <span data-ttu-id="8854c-129">Hameçonnage</span><span class="sxs-lookup"><span data-stu-id="8854c-129">Phishing</span></span>
    - <span data-ttu-id="8854c-130">Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="8854c-130">Junk</span></span>
    - <span data-ttu-id="8854c-131">Aucune menace détectée</span><span class="sxs-lookup"><span data-stu-id="8854c-131">No threats found</span></span>
    - <span data-ttu-id="8854c-132">Formation de sensibilisation</span><span class="sxs-lookup"><span data-stu-id="8854c-132">Awareness training</span></span>
    - <span data-ttu-id="8854c-133">Pied de page</span><span class="sxs-lookup"><span data-stu-id="8854c-133">Footer</span></span>

4. <span data-ttu-id="8854c-134">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8854c-134">When you're finished, click **Save**.</span></span> <span data-ttu-id="8854c-135">Pour effacer ces valeurs, cliquez **sur Ignorer** dans la page Soumissions de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8854c-135">To clear these values, click **Discard** on the User submissions page.</span></span>
