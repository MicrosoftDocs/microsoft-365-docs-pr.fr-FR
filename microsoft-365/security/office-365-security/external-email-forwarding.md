---
title: Configuration et contrôle du transfert de messages externes, du transfert automatique, de l’accès 5.7.520 refusé, de la désactivation du transfert externe, votre administrateur a désactivé le transfert externe, stratégie anti-courrier indésirable sortant
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
ms.custom:
- seo-marvel-apr2020
description: .
ms.openlocfilehash: bbe341899599d5092db0b0961add5a9825eca3b4
ms.sourcegitcommit: ee39faf3507d0edc9497117b3b2854955c959c6c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "49616595"
---
# <a name="control-automatic-external-email-forwarding-in-microsoft-365"></a><span data-ttu-id="6e7ee-103">Contrôler le transfert automatique du courrier électronique externe dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="6e7ee-103">Control automatic external email forwarding in Microsoft 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="6e7ee-104">En tant qu’administrateur, vous pouvez être amené à limiter ou contrôler automatiquement les messages transférés à des destinataires externes (destinataires extérieurs à votre organisation).</span><span class="sxs-lookup"><span data-stu-id="6e7ee-104">As an admin, you might have company requirements to restrict or control automatically forwarded messages to external recipients (recipients outside of your organization).</span></span> <span data-ttu-id="6e7ee-105">Le transfert du courrier peut être utile, mais peut également poser un risque de sécurité en raison de la divulgation potentielle des informations.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-105">Email forwarding can be a useful, but can also pose a security risk due to the potential disclosure of information.</span></span> <span data-ttu-id="6e7ee-106">Les agresseurs peuvent utiliser ces informations pour attaquer votre organisation ou vos partenaires.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-106">Attackers might use this information to attack your organization or partners.</span></span>

<span data-ttu-id="6e7ee-107">Les types de transferts automatiques suivants sont disponibles dans Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="6e7ee-107">The following types of automatic forwarding are available in Microsoft 365:</span></span>

- <span data-ttu-id="6e7ee-108">Les utilisateurs peuvent configurer des [règles de boîte de réception](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59) pour transférer automatiquement des messages vers des expéditeurs externes (délibérément ou en raison d’un compte compromis).</span><span class="sxs-lookup"><span data-stu-id="6e7ee-108">Users can configure [Inbox rules](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59) to automatically forward messages to external senders (deliberately or as a result of a compromised account).</span></span>

- <span data-ttu-id="6e7ee-109">Les administrateurs peuvent configurer le transfert des [boîtes aux lettres](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding) (également appelé _transfert SMTP_) pour transférer automatiquement les messages vers des destinataires externes.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-109">Admins can configure [mailbox forwarding](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding) (also known as _SMTP forwarding_) to automatically forward messages to external recipients.</span></span>

<span data-ttu-id="6e7ee-110">Vous pouvez utiliser des stratégies de filtrage du courrier indésirable sortant pour contrôler le transfert automatique vers des destinataires externes.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-110">You can use outbound spam filter policies to control automatic forwarding to external recipients.</span></span> <span data-ttu-id="6e7ee-111">Trois paramètres sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="6e7ee-111">Three settings are available:</span></span>

- <span data-ttu-id="6e7ee-112">**Automatique**: le transfert externe automatique est bloqué.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-112">**Automatic**: Automatic external forwarding is blocked.</span></span> <span data-ttu-id="6e7ee-113">Le transfert automatique interne des messages continuera à fonctionner.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-113">Internal automatic forwarding of messages will continue to work.</span></span> <span data-ttu-id="6e7ee-114">Il s’agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-114">This is the default setting.</span></span>

- <span data-ttu-id="6e7ee-115">**Activé : le** transfert externe automatique est autorisé et non restreint.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-115">**On**: Automatic external forwarding is allowed and not restricted.</span></span>

- <span data-ttu-id="6e7ee-116">**Off**: le transfert externe automatique est désactivé et entraîne une notification d’échec de remise (également appelée notification de non-remise) à l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-116">**Off**: Automatic external forwarding is disabled and will result in a non-delivery report (also known as an NDR or bounce message) to the sender.</span></span>

<span data-ttu-id="6e7ee-117">Pour obtenir des instructions sur la configuration de ces paramètres, consultez la rubrique [configuration du filtrage du courrier indésirable sortant dans EOP](configure-the-outbound-spam-policy.md).</span><span class="sxs-lookup"><span data-stu-id="6e7ee-117">For instructions on how to configure these settings, see [Configure outbound spam filtering in EOP](configure-the-outbound-spam-policy.md).</span></span>

> [!NOTE]
>
> - <span data-ttu-id="6e7ee-118">La désactivation du transfert automatique désactive les règles de boîte de réception (utilisateurs) ou le transfert des boîtes aux lettres (administrateurs) qui redirigent les messages vers des adresses externes.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-118">Disabling automatic forwarding disables any Inbox rules (users) or mailbox forwarding (admins) that redirect messages to external addresses.</span></span>
>
> - <span data-ttu-id="6e7ee-119">Le transfert automatique des messages entre les utilisateurs internes n’est pas affecté par les paramètres des stratégies de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-119">Automatic forwarding of messages between internal users isn't affected by the settings in outbound spam filter policies.</span></span>
>
> - <span data-ttu-id="6e7ee-120">Vous pouvez afficher des informations sur les utilisateurs qui transfèrent automatiquement des messages à des destinataires externes dans le [rapport de messages transférés](mfi-auto-forwarded-messages-report.md)automatiquement.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-120">You can see information about users that are automatically forwarding messages to external recipients in the [Auto-forwarded messages report](mfi-auto-forwarded-messages-report.md).</span></span>

## <a name="how-the-outbound-spam-filter-policy-settings-work-with-other-automatic-email-forwarding-controls"></a><span data-ttu-id="6e7ee-121">Fonctionnement des paramètres de stratégie de filtrage du courrier indésirable sortant avec d’autres contrôles de transfert automatique du courrier</span><span class="sxs-lookup"><span data-stu-id="6e7ee-121">How the outbound spam filter policy settings work with other automatic email forwarding controls</span></span>

<span data-ttu-id="6e7ee-122">En tant qu’administrateur, vous avez peut-être déjà configuré d’autres contrôles pour autoriser ou bloquer le transfert automatique du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-122">As an admin, you might have already configured other controls to allow or block automatic email forwarding.</span></span> <span data-ttu-id="6e7ee-123">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6e7ee-123">For example:</span></span>

- <span data-ttu-id="6e7ee-124">[Domaines distants](https://docs.microsoft.com/exchange/mail-flow-best-practices/remote-domains/remote-domains) pour autoriser ou bloquer le transfert du courrier automatique vers certains ou tous les domaines externes.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-124">[Remote domains](https://docs.microsoft.com/exchange/mail-flow-best-practices/remote-domains/remote-domains) to allow or block automatic email forwarding to some or all external domains.</span></span>

- <span data-ttu-id="6e7ee-125">Conditions et actions dans les [règles de flux de messagerie](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) Exchange (également appelées règles de transport) pour détecter et bloquer les messages transférés automatiquement vers des destinataires externes.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-125">Conditions and actions in Exchange [mail flow rules](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) (also known as transport rules) to detect and block automatically forwarded messages to external recipients.</span></span>

<span data-ttu-id="6e7ee-126">Les paramètres des domaines distants et les règles de flux de messagerie sont indépendants des paramètres des stratégies de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-126">Remote domain settings and mail flow rules are independent of the settings in outbound spam filter policies.</span></span> <span data-ttu-id="6e7ee-127">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6e7ee-127">For example:</span></span>

- <span data-ttu-id="6e7ee-128">Vous autorisez le transfert automatique pour un domaine distant, mais vous bloquez le transfert automatique dans les stratégies de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-128">You allow automatic forwarding for a remote domain, but you block automatic forwarding in outbound spam filter policies.</span></span> <span data-ttu-id="6e7ee-129">Dans cet exemple, les messages transférés automatiquement sont bloqués.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-129">In this example, automatically forwarded messages are blocked.</span></span>

- <span data-ttu-id="6e7ee-130">Vous autorisez le transfert automatique dans les stratégies de filtrage du courrier indésirable sortant, mais vous utilisez des règles de flux de messagerie ou des paramètres de domaine distant pour bloquer le transfert automatique du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-130">You allow automatic forwarding in outbound spam filter policies, but you use mail flow rules or remote domain settings to block automatically forwarded email.</span></span> <span data-ttu-id="6e7ee-131">Dans cet exemple, les règles de flux de messagerie ou les paramètres de domaine distant bloquent les messages transférés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-131">In this example, the mail flow rules or remote domain settings will block automatically forwarded messages.</span></span>

<span data-ttu-id="6e7ee-132">Cette indépendance de fonctionnalité vous permet (par exemple) d’autoriser le transfert automatique dans les stratégies de filtrage du courrier indésirable sortant, mais d’utiliser des domaines distants pour contrôler les domaines externes vers lesquels les utilisateurs peuvent transférer des messages.</span><span class="sxs-lookup"><span data-stu-id="6e7ee-132">This feature independence allows you to (for example) allow automatic forwarding in outbound spam filter policies, but use remote domains to control the external domains that users can forward messages to.</span></span>

## <a name="the-blocked-email-forwarding-message"></a><span data-ttu-id="6e7ee-133">Message de transfert de courrier électronique bloqué</span><span class="sxs-lookup"><span data-stu-id="6e7ee-133">The blocked email forwarding message</span></span>

<span data-ttu-id="6e7ee-134">Lorsqu’un message est détecté comme étant automatiquement transféré et que la stratégie d’organisation *bloque* cette activité, le message est renvoyé à l’expéditeur dans une notification d’inactivité contenant les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6e7ee-134">When a message is detected as automatically forwarded, and the organizational policy *blocks* that activity, the message is returned to the sender in an NDR that contains the following information:</span></span>

`5.7.520 Access denied, Your organization does not allow external forwarding. Please contact your administrator for further assistance. AS(7555)`
