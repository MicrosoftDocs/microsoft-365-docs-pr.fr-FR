---
title: Configuration et contrôle du transfert de messages externes, du transfert automatique, de l’accès 5.7.520 refusé, de la désactivation du transfert externe, votre administrateur a désactivé le transfert externe, stratégie anti-courrier indésirable sortant
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 07/01/2020
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
ms.custom:
- seo-marvel-apr2020
description: .
ms.openlocfilehash: c0a3849d330b508630eb60c7ee24cd8b498a32b8
ms.sourcegitcommit: 260c69fa31a898428d51cfdbd762c5f0213c403c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/10/2020
ms.locfileid: "48417234"
---
# <a name="configuring-external-email-forwarding-in-office-365"></a><span data-ttu-id="43630-103">Configuration du transfert de messages électroniques externes dans Office 365</span><span class="sxs-lookup"><span data-stu-id="43630-103">Configuring external email forwarding in Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="43630-104">Le transfert externe est contrôlé par la *stratégie anti-courrier indésirable sortant* et l’étendue aux utilisateurs en fonction du paramètre configuré.</span><span class="sxs-lookup"><span data-stu-id="43630-104">External forwarding is controlled by the *outbound anti-spam policy* and scoped to users based on the configured setting.</span></span> <span data-ttu-id="43630-105">Actuellement, 3 les paramètres sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="43630-105">Currently 3 settings are supported:</span></span>

- <span data-ttu-id="43630-106">**Automatique** – cela est contrôlé par le système : il permet le filtrage du courrier indésirable sortant pour contrôler le transfert automatique du courrier électronique externe.</span><span class="sxs-lookup"><span data-stu-id="43630-106">**Automatic** – This is system-controlled: It allows outbound spam filtering to control automatic external email forwarding.</span></span> <span data-ttu-id="43630-107">Il s’agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="43630-107">This is the default setting.</span></span>

- <span data-ttu-id="43630-108">**Activé – le** transfert externe automatique est autorisé et non restreint.</span><span class="sxs-lookup"><span data-stu-id="43630-108">**On** – Automatic external forwarding is allowed and not restricted.</span></span>

- <span data-ttu-id="43630-109">**Off** : le transfert externe automatique est désactivé et entraîne une notification d’échec de remise à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="43630-109">**Off** – Automatic external forwarding is disabled and will result in a Non-delivery report (NDR) to the end user.</span></span>

<span data-ttu-id="43630-110">Pour plus d’informations sur la configuration de ces paramètres, voir [configurer le filtrage du courrier indésirable sortant dans EOP](https://docs.microsoft.com/microsoft-365/security/office-365-security/configure-the-outbound-spam-policy?view=o365-worldwide&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="43630-110">See [Configure outbound spam filtering in EOP](https://docs.microsoft.com/microsoft-365/security/office-365-security/configure-the-outbound-spam-policy?view=o365-worldwide&preserve-view=true) for more information on how to configure these settings.</span></span>

> [!NOTE]
> <span data-ttu-id="43630-111">La désactivation du transfert automatique désactive également les règles de boîte de réception qui redirigent les messages vers des adresses externes.</span><span class="sxs-lookup"><span data-stu-id="43630-111">Disabling automatic forwarding will also disable Inbox rules that redirect messages to external addresses.</span></span>

## <a name="controlling-external-email-forwarding"></a><span data-ttu-id="43630-112">Contrôle du transfert du courrier électronique externe</span><span class="sxs-lookup"><span data-stu-id="43630-112">Controlling external email forwarding</span></span>

<span data-ttu-id="43630-113">En tant qu’administrateur d’une organisation, vous pouvez avoir des exigences en matière d’entreprise pour limiter ou contrôler qui est en mesure de transférer automatiquement des courriers électroniques à l’aide de règles de boîte de réception ou de l’envoi SMTP, en dehors de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="43630-113">As an admin of an organization you may have company requirements to restrict or control who is able to automatically forward emails using inbox rules, or SMTP forwarding, outside of the organization.</span></span> <span data-ttu-id="43630-114">Le transfert du courrier peut être une fonctionnalité utile, mais peut également présenter un risque grâce à une divulgation potentielle d’informations, même en fournissant des informations aux attaquants qui peuvent être exploités pour attaquer l’organisation ou ses partenaires.</span><span class="sxs-lookup"><span data-stu-id="43630-114">Email forwarding can be a useful feature, but can also pose a risk through the potential disclosure of information, even by providing information to attackers that can be leveraged to attack the organization or its partners.</span></span>

<span data-ttu-id="43630-115">Office 365 n’autorise pas le transfert externe automatique par les règles de boîte de réception ou la configuration des boîtes aux lettres, qui fournit une stratégie par défaut sécurisée.</span><span class="sxs-lookup"><span data-stu-id="43630-115">Office 365 doesn't allow automatic external forwarding by either Inbox rules or mail box configuration, which provides a secure default policy.</span></span> <span data-ttu-id="43630-116">Toutefois, l’administrateur peut modifier ces paramètres pour tous les utilisateurs de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="43630-116">However, the admin can modify these settings for all, or some, users in the organization.</span></span> <span data-ttu-id="43630-117">Le transfert de messages entre les utilisateurs internes n’est pas affecté par une telle modification.</span><span class="sxs-lookup"><span data-stu-id="43630-117">Forwarding messages between internal users isn't affected by such a modification.</span></span>

> [!NOTE]
> <span data-ttu-id="43630-118">La désactivation du transfert automatique vers des adresses externes dans Office 365 est effectuée en phases avec des détails communiqués via des publications du [Centre de messages](https://admin.microsoft.com/Adminportal/Home?source=applauncher&ref=/MessageCenter) .</span><span class="sxs-lookup"><span data-stu-id="43630-118">Disabling automatic forwarding to external addresses in Office 365 is being rolled out in phases with details communicated via [Message Center](https://admin.microsoft.com/Adminportal/Home?source=applauncher&ref=/MessageCenter) posts.</span></span> <span data-ttu-id="43630-119">Pour aider les administrateurs à se préparer à ces modifications, demandez-leur de modifier les stratégies à l’avance afin de s’assurer que les utilisateurs ne sont pas perturbés.</span><span class="sxs-lookup"><span data-stu-id="43630-119">To help administrators prepare for these changes have them modify policies ahead of time to ensure there is no disruption to their users.</span></span>

<span data-ttu-id="43630-120">Vous trouverez plus d’informations sur les utilisateurs qui utilisent le transfert automatique (règles de boîte de réception ou le transfert SMTP) dans votre organisation dans le [rapport de messages transférés automatiquement](https://docs.microsoft.com/microsoft-365/security/office-365-security/mfi-auto-forwarded-messages-report?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="43630-120">More information about users that are using automatic forwarding (inbox rules or SMTP forwarding) in your organization can be found in the [auto-forwarded messages report](https://docs.microsoft.com/microsoft-365/security/office-365-security/mfi-auto-forwarded-messages-report?view=o365-worldwide&preserve-view=true).</span></span>

## <a name="how-does-this-policy-work-with-other-automatic-forwarding-controls"></a><span data-ttu-id="43630-121">Comment cette stratégie fonctionne-t-elle avec d’autres contrôles de transfert automatique ?</span><span class="sxs-lookup"><span data-stu-id="43630-121">How does this policy work with other automatic forwarding controls</span></span>

<span data-ttu-id="43630-122">En tant qu’administrateur, vous avez peut-être déjà d’autres types de contrôles en place, ce qui bloque le transfert automatique dans les [domaines distants](https://docs.microsoft.com/exchange/mail-flow-best-practices/remote-domains/remote-domains) et l’utilisation d’une règle de transport Exchange (ETR).</span><span class="sxs-lookup"><span data-stu-id="43630-122">As an admin, you may already have other types of controls in place, such blocking automatic forwarding in [remote domains](https://docs.microsoft.com/exchange/mail-flow-best-practices/remote-domains/remote-domains) and the use of an Exchange Transport Rule (ETR).</span></span> <span data-ttu-id="43630-123">Ces deux contrôles sont indépendants de cette fonctionnalité particulière, par exemple si vous autorisez le transfert automatique pour un domaine distant, mais bloquer le transfert automatique via la stratégie de courrier indésirable sortant, le message est alors bloqué.</span><span class="sxs-lookup"><span data-stu-id="43630-123">Both of these controls are independent of this particular feature, for example if you allow automatic forwarding for a remote domain, but block automatic forwarding via the outbound spam policy the result will be that the automatically forwarded message is blocked.</span></span> <span data-ttu-id="43630-124">De même, si vous autorisez le transfert automatique dans la stratégie anti-courrier indésirable sortant, tout en le bloquant dans un ETR ou un domaine distant, le message sera bloqué par l’un de ces contrôles.</span><span class="sxs-lookup"><span data-stu-id="43630-124">Similarly if you allow automatic forwarding in the outbound spam policy but block it in an ETR or remote domain then the message will be blocked by either of these controls.</span></span> <span data-ttu-id="43630-125">Cela vous permet, par exemple, d’autoriser le transfert automatique dans la stratégie de courrier indésirable sortant et d’utiliser des domaines distants pour contrôler les domaines vers lesquels les utilisateurs peuvent transférer automatiquement des messages.</span><span class="sxs-lookup"><span data-stu-id="43630-125">This allows you to, for example, allow automatic forwarding in the outbound spam policy and utilize remote domains to control the domains that users can automatic forward messages to.</span></span>


## <a name="the-blocked-email-forwarding-message"></a><span data-ttu-id="43630-126">Message de transfert de courrier électronique bloqué</span><span class="sxs-lookup"><span data-stu-id="43630-126">The blocked email forwarding message</span></span>

<span data-ttu-id="43630-127">Lorsqu’un message est détecté comme étant automatiquement transféré et que la stratégie d’organisation *bloque* cette activité, une notification d’échec de **remise (NDR)** est renvoyée à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="43630-127">When a message is detected as automatically forwarded and the organizational policy *blocks* that activity a **Non-delivery report (NDR)** will be generated back to the end user.</span></span> <span data-ttu-id="43630-128">Le rapport indiquera que le message n’a pas été remis.</span><span class="sxs-lookup"><span data-stu-id="43630-128">The report will indicate the message was not delivered.</span></span> <span data-ttu-id="43630-129">Le rapport de non-remise aura le format suivant :</span><span class="sxs-lookup"><span data-stu-id="43630-129">The NDR will have the following format:</span></span> 

`5.7.520 Access Denied – Your administrator has disabled external forwarding – AS(XXXX)`
