---
title: Révision de l’administrateur pour les messages signalés
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
description: Découvrez comment passer en revue les messages signalés et comment envoyer des commentaires à vos utilisateurs.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 619cd35b6a60f0d50aa6c13e4cad2b8d7ae947a8
ms.sourcegitcommit: e8f5d88f0fe54620308d3bec05263568f9da2931
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52730963"
---
# <a name="admin-review-for-reported-messages"></a><span data-ttu-id="a083b-103">Révision de l’administrateur pour les messages signalés</span><span class="sxs-lookup"><span data-stu-id="a083b-103">Admin review for reported messages</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

> [!NOTE]
> <span data-ttu-id="a083b-104">Les informations de cet article concernent un produit d’aperçu qui peut être considérablement modifié avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="a083b-104">The information in this article relates to a preview product that may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a083b-105">Ce document est fourni uniquement à des fins d’évaluation et d’exploration.</span><span class="sxs-lookup"><span data-stu-id="a083b-105">This document is provided for evaluation and exploration purposes only.</span></span>

<span data-ttu-id="a083b-106">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="a083b-106">**Applies to**</span></span>
- [<span data-ttu-id="a083b-107">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="a083b-107">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="a083b-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a083b-108">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="a083b-109">Dans Microsoft 365 organisations avec des boîtes aux lettres Exchange Online et Microsoft Defender pour Office 365, les administrateurs peuvent désormais renvoyer des messages de modèle aux utilisateurs finaux après avoir passé en revue les messages signalés.</span><span class="sxs-lookup"><span data-stu-id="a083b-109">In Microsoft 365 organizations with Exchange Online mailboxes and Microsoft Defender for Office 365, admins can now send templated messages back to end users after they review reported messages.</span></span> <span data-ttu-id="a083b-110">Cela peut être personnalisé pour votre organisation et en fonction du verdict de votre administrateur.</span><span class="sxs-lookup"><span data-stu-id="a083b-110">This can be customized for your organization and based on your admin’s verdict as well.</span></span>

<span data-ttu-id="a083b-111">Cette fonctionnalité est conçue pour envoyer des commentaires à vos utilisateurs, mais ne modifie pas les verdicts des messages dans le système.</span><span class="sxs-lookup"><span data-stu-id="a083b-111">This feature is designed to give feedback to your users but does not change the verdicts of messages in the system.</span></span> <span data-ttu-id="a083b-112">Pour aider Microsoft à mettre à jour et à améliorer ses filtres, vous devez envoyer des messages pour analyse à l’aide de [la soumission d’administrateur.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="a083b-112">To help Microsoft update and improve its filters, you will need to submit messages for analysis using [Admin submission](admin-submission.md).</span></span>

<span data-ttu-id="a083b-113">Vous ne pourrez marquer et avertir les utilisateurs des résultats de la révision que si le message a été signalé comme faux positifs ou [faux négatifs.](report-false-positives-and-false-negatives.md)</span><span class="sxs-lookup"><span data-stu-id="a083b-113">You will only be able to mark and notify users of review results if the message was reported as a [false positives or false negatives](report-false-positives-and-false-negatives.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="a083b-114">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a083b-114">What do you need to know before you begin?</span></span>

- <span data-ttu-id="a083b-115">Pour modifier la configuration des soumissions d’utilisateurs, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="a083b-115">To modify the configuration for User submissions, you need to be a member of one of the following role groups:</span></span>
    - <span data-ttu-id="a083b-116">Gestion de l’organisation ou administrateur de la sécurité dans [le Centre de sécurité.](permissions-microsoft-365-compliance-security.md)</span><span class="sxs-lookup"><span data-stu-id="a083b-116">Organization Management or Security Administrator in the [Security center](permissions-microsoft-365-compliance-security.md).</span></span>
    - <span data-ttu-id="a083b-117">Gestion de [l’organisation Exchange Online](/Exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="a083b-117">Organization Management in [Exchange Online](/Exchange/permissions-exo/permissions-exo).</span></span>

- <span data-ttu-id="a083b-118">Vous aurez également besoin d’accéder à la Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a083b-118">You'll also need access to the Exchange Online PowerShell.</span></span> <span data-ttu-id="a083b-119">Si le compte que vous essayez d’utiliser n’a pas accès à Exchange Online PowerShell, vous recevrez une erreur qui indique spécifier une adresse de messagerie dans *votre domaine.*</span><span class="sxs-lookup"><span data-stu-id="a083b-119">If the account that you're trying to use doesn't have access to Exchange Online PowerShell, you'll receive an error that says *Specify an email address in your domain*.</span></span> <span data-ttu-id="a083b-120">Pour plus d’informations sur l’activation ou la désactivation de l’accès Exchange Online PowerShell, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="a083b-120">For more information about enabling or disabling access to Exchange Online PowerShell, see the following topics:</span></span>
    - [<span data-ttu-id="a083b-121">Activer ou désactiver l’accès à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="a083b-121">Enable or disable access to Exchange Online PowerShell</span></span>](/powershell/exchange/disable-access-to-exchange-online-powershell)
    - [<span data-ttu-id="a083b-122">Règles d’accès client dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="a083b-122">Client Access Rules in Exchange Online</span></span>](/exchange/clients-and-mobile-in-exchange-online/client-access-rules/client-access-rules)

## <a name="configure-the-messages-used-to-notify-users"></a><span data-ttu-id="a083b-123">Configurer les messages utilisés pour avertir les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a083b-123">Configure the messages used to notify users</span></span>

1. <span data-ttu-id="a083b-124">Dans le centre [Microsoft 365 de sécurité,](../defender/overview-security-center.md)allez à **Stratégies &** Stratégies de menace \>  \> **Stratégies De l’utilisateur a signalé les paramètres de message**.</span><span class="sxs-lookup"><span data-stu-id="a083b-124">In the [Microsoft 365 security center](../defender/overview-security-center.md), go to **Policies & rules** \> **Threat policies** \> **User reported message settings**.</span></span>

2. <span data-ttu-id="a083b-125">Si vous souhaitez spécifier le nom complet  de l’expéditeur, cochez la case Spécifier l’adresse de messagerie Office 365 à utiliser en tant qu’expéditeur dans la section **Notifications** par courrier électronique pour les résultats de l’avis de l’administrateur, puis entrez le nom que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="a083b-125">If you want to specify the sender display name, check the box for **Specify Office 365 email address to use as sender** under the **Email notifications for admin review results** section, and enter in the name you wish to use.</span></span> <span data-ttu-id="a083b-126">Il s’agit de l’adresse de messagerie qui sera visible dans Outlook et où les réponses seront envoyés.</span><span class="sxs-lookup"><span data-stu-id="a083b-126">This is the email address that will be visible in Outlook and where replies will go to.</span></span>

3. <span data-ttu-id="a083b-127">Si vous souhaitez personnaliser l’un des modèles, cliquez sur **Personnaliser la notification par courrier électronique.**</span><span class="sxs-lookup"><span data-stu-id="a083b-127">If you want to customize any of the templates, click **Customize email notification**.</span></span> <span data-ttu-id="a083b-128">Dans ce flyout, vous serez en mesure de personnaliser uniquement les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="a083b-128">In this flyout, you will be able to customize only the following:</span></span>
    - <span data-ttu-id="a083b-129">Hameçonnage</span><span class="sxs-lookup"><span data-stu-id="a083b-129">Phishing</span></span>
    - <span data-ttu-id="a083b-130">Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="a083b-130">Junk</span></span>
    - <span data-ttu-id="a083b-131">Aucune menace détectée</span><span class="sxs-lookup"><span data-stu-id="a083b-131">No threats found</span></span>
    - <span data-ttu-id="a083b-132">Formation de sensibilisation</span><span class="sxs-lookup"><span data-stu-id="a083b-132">Awareness training</span></span>
    - <span data-ttu-id="a083b-133">Pied de page</span><span class="sxs-lookup"><span data-stu-id="a083b-133">Footer</span></span>

4. <span data-ttu-id="a083b-134">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a083b-134">When you're finished, click **Save**.</span></span> <span data-ttu-id="a083b-135">Pour effacer ces valeurs, cliquez **sur Ignorer** dans la page Soumissions de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a083b-135">To clear these values, click **Discard** on the User submissions page.</span></span>
