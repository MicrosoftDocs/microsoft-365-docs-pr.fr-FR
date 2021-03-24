---
title: Configuration et contrôle du forwarding de courrier externe, transmission automatique, 5.7.520 Accès refusé, désactivation du forwarding externe, Votre administrateur a désactivé le forwarding externe, stratégie anti-courrier indésirable sortant
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: overview
localization_priority: Normal
ms.assetid: ''
ms.custom:
- seo-marvel-apr2020
description: .
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 0f42da077ca84341824fad01fcb23eae976336a1
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51063406"
---
# <a name="control-automatic-external-email-forwarding-in-microsoft-365"></a><span data-ttu-id="670b0-103">Contrôler le forwarding automatique du courrier externe dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="670b0-103">Control automatic external email forwarding in Microsoft 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="670b0-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="670b0-104">**Applies to**</span></span>
- [<span data-ttu-id="670b0-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="670b0-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="670b0-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="670b0-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="670b0-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="670b0-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="670b0-108">En tant qu’administrateur, vous pouvez avoir des exigences d’entreprise pour restreindre ou contrôler les messages automatiquement transmis à des destinataires externes (destinataires extérieurs à votre organisation).</span><span class="sxs-lookup"><span data-stu-id="670b0-108">As an admin, you might have company requirements to restrict or control automatically forwarded messages to external recipients (recipients outside of your organization).</span></span> <span data-ttu-id="670b0-109">Le forwarding de courrier électronique peut être utile, mais peut également poser un risque de sécurité en raison de la divulgation potentielle d’informations.</span><span class="sxs-lookup"><span data-stu-id="670b0-109">Email forwarding can be a useful, but can also pose a security risk due to the potential disclosure of information.</span></span> <span data-ttu-id="670b0-110">Les attaquants peuvent utiliser ces informations pour attaquer votre organisation ou vos partenaires.</span><span class="sxs-lookup"><span data-stu-id="670b0-110">Attackers might use this information to attack your organization or partners.</span></span>


<span data-ttu-id="670b0-111">Les types de transmission automatique suivants sont disponibles dans Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="670b0-111">The following types of automatic forwarding are available in Microsoft 365:</span></span>

- <span data-ttu-id="670b0-112">Les utilisateurs peuvent configurer [des règles](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59) de boîte de réception pour transmettre automatiquement des messages à des expéditeurs externes (délibérément ou à la suite d’un compte compromis).</span><span class="sxs-lookup"><span data-stu-id="670b0-112">Users can configure [Inbox rules](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59) to automatically forward messages to external senders (deliberately or as a result of a compromised account).</span></span>

- <span data-ttu-id="670b0-113">Les administrateurs peuvent configurer le [forwarding](/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding) de boîte aux lettres (également appelé « _smTP forwarding_) pour qu’il puisse automatiquement envoyer des messages à des destinataires externes.</span><span class="sxs-lookup"><span data-stu-id="670b0-113">Admins can configure [mailbox forwarding](/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding) (also known as _SMTP forwarding_) to automatically forward messages to external recipients.</span></span> <span data-ttu-id="670b0-114">L’administrateur peut choisir de simplement envoyer des messages ou de conserver des copies de messages transmis dans la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="670b0-114">The admin can choose whether to simply forward messages, or keep copies of forwarded messages in the mailbox.</span></span>

<span data-ttu-id="670b0-115">Vous pouvez utiliser des stratégies de filtrage du courrier indésirable sortant pour contrôler le forwarding automatique vers des destinataires externes.</span><span class="sxs-lookup"><span data-stu-id="670b0-115">You can use outbound spam filter policies to control automatic forwarding to external recipients.</span></span> <span data-ttu-id="670b0-116">Trois paramètres sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="670b0-116">Three settings are available:</span></span>

- <span data-ttu-id="670b0-117">**Automatique**: le forwarding externe automatique est bloqué.</span><span class="sxs-lookup"><span data-stu-id="670b0-117">**Automatic**: Automatic external forwarding is blocked.</span></span> <span data-ttu-id="670b0-118">Le forwarding automatique interne des messages continuera de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="670b0-118">Internal automatic forwarding of messages will continue to work.</span></span> <span data-ttu-id="670b0-119">Il s’agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="670b0-119">This is the default setting.</span></span>
- <span data-ttu-id="670b0-120">**On**: le forwarding externe automatique est autorisé et non restreint.</span><span class="sxs-lookup"><span data-stu-id="670b0-120">**On**: Automatic external forwarding is allowed and not restricted.</span></span>
- <span data-ttu-id="670b0-121">**Désactivé**: le forwarding externe automatique est désactivé et entraîne une non-remise (également appelée une NDR ou une non-remise) à l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="670b0-121">**Off**: Automatic external forwarding is disabled and will result in a non-delivery report (also known as an NDR or bounce message) to the sender.</span></span>

<span data-ttu-id="670b0-122">Pour obtenir des instructions sur la configuration de ces paramètres, voir Configurer le filtrage du courrier indésirable sortant [dans EOP.](configure-the-outbound-spam-policy.md)</span><span class="sxs-lookup"><span data-stu-id="670b0-122">For instructions on how to configure these settings, see [Configure outbound spam filtering in EOP](configure-the-outbound-spam-policy.md).</span></span>

> [!NOTE]
>
> - <span data-ttu-id="670b0-123">La désactivation du redirection automatique désactive les règles de boîte de réception (utilisateurs) ou de boîtes aux lettres (administrateurs) qui redirigent les messages vers des adresses externes.</span><span class="sxs-lookup"><span data-stu-id="670b0-123">Disabling automatic forwarding disables any Inbox rules (users) or mailbox forwarding (admins) that redirect messages to external addresses.</span></span>
>
> - <span data-ttu-id="670b0-124">Le filtrage automatique des messages entre utilisateurs internes n’est pas affecté par les paramètres des stratégies de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="670b0-124">Automatic forwarding of messages between internal users isn't affected by the settings in outbound spam filter policies.</span></span>
>
> - <span data-ttu-id="670b0-125">Vous pouvez voir les informations sur les utilisateurs qui sont automatiquement en cours de forwardage des messages à des destinataires externes dans le rapport de [messages transmis automatiquement.](mfi-auto-forwarded-messages-report.md)</span><span class="sxs-lookup"><span data-stu-id="670b0-125">You can see information about users that are automatically forwarding messages to external recipients in the [Auto-forwarded messages report](mfi-auto-forwarded-messages-report.md).</span></span>

## <a name="how-the-outbound-spam-filter-policy-settings-work-with-other-automatic-email-forwarding-controls"></a><span data-ttu-id="670b0-126">Fonctionnement des paramètres de stratégie de filtrage du courrier indésirable sortant avec d’autres contrôles de transmission automatique du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="670b0-126">How the outbound spam filter policy settings work with other automatic email forwarding controls</span></span>

<span data-ttu-id="670b0-127">En tant qu’administrateur, vous avez peut-être déjà configuré d’autres contrôles pour autoriser ou bloquer le forwarding automatique du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="670b0-127">As an admin, you might have already configured other controls to allow or block automatic email forwarding.</span></span> <span data-ttu-id="670b0-128">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="670b0-128">For example:</span></span>

- <span data-ttu-id="670b0-129">[Domaines distants permettant](/exchange/mail-flow-best-practices/remote-domains/remote-domains) d’autoriser ou de bloquer le forwarding automatique du courrier électronique vers tout ou partie des domaines externes.</span><span class="sxs-lookup"><span data-stu-id="670b0-129">[Remote domains](/exchange/mail-flow-best-practices/remote-domains/remote-domains) to allow or block automatic email forwarding to some or all external domains.</span></span>

- <span data-ttu-id="670b0-130">Conditions et actions dans les règles de flux de messagerie [Exchange](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) (également appelées règles de transport) pour détecter et bloquer les messages automatiquement transmis à des destinataires externes.</span><span class="sxs-lookup"><span data-stu-id="670b0-130">Conditions and actions in Exchange [mail flow rules](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) (also known as transport rules) to detect and block automatically forwarded messages to external recipients.</span></span>

<span data-ttu-id="670b0-131">Les paramètres de domaine distant et les règles de flux de messagerie sont indépendants des paramètres des stratégies de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="670b0-131">Remote domain settings and mail flow rules are independent of the settings in outbound spam filter policies.</span></span> <span data-ttu-id="670b0-132">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="670b0-132">For example:</span></span>

- <span data-ttu-id="670b0-133">Vous autorisez le forwarding automatique pour un domaine distant, mais vous bloquez le forwarding automatique dans les stratégies de filtrage du courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="670b0-133">You allow automatic forwarding for a remote domain, but you block automatic forwarding in outbound spam filter policies.</span></span> <span data-ttu-id="670b0-134">Dans cet exemple, les messages automatiquement transmis sont bloqués.</span><span class="sxs-lookup"><span data-stu-id="670b0-134">In this example, automatically forwarded messages are blocked.</span></span>

- <span data-ttu-id="670b0-135">Vous autorisez le forwarding automatique dans les stratégies de filtrage du courrier indésirable sortant, mais vous utilisez des règles de flux de messagerie ou des paramètres de domaine distant pour bloquer le courrier électronique automatiquement transmis.</span><span class="sxs-lookup"><span data-stu-id="670b0-135">You allow automatic forwarding in outbound spam filter policies, but you use mail flow rules or remote domain settings to block automatically forwarded email.</span></span> <span data-ttu-id="670b0-136">Dans cet exemple, les règles de flux de messagerie ou les paramètres de domaine distant bloquent les messages automatiquement transmis.</span><span class="sxs-lookup"><span data-stu-id="670b0-136">In this example, the mail flow rules or remote domain settings will block automatically forwarded messages.</span></span>

<span data-ttu-id="670b0-137">Cette indépendance de fonctionnalité vous permet (par exemple) d’autoriser le forwarding automatique dans les stratégies de filtrage du courrier indésirable sortant, mais d’utiliser des domaines distants pour contrôler les domaines externes vers qui les utilisateurs peuvent envoyer des messages.</span><span class="sxs-lookup"><span data-stu-id="670b0-137">This feature independence allows you to (for example) allow automatic forwarding in outbound spam filter policies, but use remote domains to control the external domains that users can forward messages to.</span></span>

## <a name="blocked-email-forwarding-messages"></a><span data-ttu-id="670b0-138">Messages de courrier bloqués</span><span class="sxs-lookup"><span data-stu-id="670b0-138">Blocked email forwarding messages</span></span>

<span data-ttu-id="670b0-139">Lorsqu’un message est détecté comme étant [](configure-the-outbound-spam-policy.md) automatiquement transmis et  que la stratégie de filtrage du courrier indésirable sortant bloque cette activité, le message est renvoyé à l’expéditeur dans une NDR contenant les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="670b0-139">When a message is detected as automatically forwarded, and the [outbound spam filter](configure-the-outbound-spam-policy.md) policy *blocks* that activity, the message is returned to the sender in an NDR that contains the following information:</span></span>

`5.7.520 Access denied, Your organization does not allow external forwarding. Please contact your administrator for further assistance. AS(7555)`