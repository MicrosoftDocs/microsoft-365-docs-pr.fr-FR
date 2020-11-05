---
title: Aperçu des messages transférés automatiquement
f1.keywords:
- NOCSH
ms.author: siosulli
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: b5543faa-44fa-44c5-8180-fb835e7e452d
description: Les administrateurs peuvent en savoir plus sur le rapport de messages transférés automatiquement dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité.
ms.openlocfilehash: 28cb593d56d0b0054c8c8cbe4596d4f7df6442ab
ms.sourcegitcommit: d7975c391e03eeb96e29c1d02e77d2a1433ea67c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/05/2020
ms.locfileid: "48920595"
---
# <a name="auto-forwarded-messages-insight-in-the-security--compliance-center"></a><span data-ttu-id="d7d8e-103">Aperçu des messages transmis automatiquement dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="d7d8e-103">Auto-forwarded messages insight in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="d7d8e-104">La vue **messages transmis automatiquement** dans le [tableau de bord de flux de messagerie](mail-flow-insights-v2.md) dans le centre de [sécurité & conformité](https://protection.office.com) affiche des informations sur les messages qui sont automatiquement transférés de votre organisation à des destinataires dans des domaines externes.</span><span class="sxs-lookup"><span data-stu-id="d7d8e-104">The **Auto-forwarded messages** insight in the [Mail flow dashboard](mail-flow-insights-v2.md) in the [Security & Compliance Center](https://protection.office.com) displays information about messages that are automatically forwarded from your organization to recipients in external domains.</span></span>

![Widget messages transférés automatiquement dans le centre de sécurité & conformité](../../media/mfi-auto-forwarded-messages.png)

## <a name="auto-forwarded-messages-details"></a><span data-ttu-id="d7d8e-106">Détails des messages transférés automatiquement</span><span class="sxs-lookup"><span data-stu-id="d7d8e-106">Auto-forwarded messages details</span></span>

<span data-ttu-id="d7d8e-107">Lorsque vous cliquez sur le nombre de messages dans le widget, un volet flyout apparaît et affiche des informations supplémentaires sur les messages transférés automatiquement :</span><span class="sxs-lookup"><span data-stu-id="d7d8e-107">When you click the number of messages in the widget, a flyout pane appears that shows more information about the auto-forwarded messages:</span></span>

- <span data-ttu-id="d7d8e-108">**Messages transférés automatiquement par les méthodes de transfert** :</span><span class="sxs-lookup"><span data-stu-id="d7d8e-108">**Auto-forwarded messages by forwarding methods** :</span></span>

  - <span data-ttu-id="d7d8e-109">**Par les règles de flux de messagerie**</span><span class="sxs-lookup"><span data-stu-id="d7d8e-109">**By mail flow rules**</span></span>
  - <span data-ttu-id="d7d8e-110">**Par les règles de boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="d7d8e-110">**By Inbox rules**</span></span>
  - <span data-ttu-id="d7d8e-111">**Par transfert SMTP** : cette méthode indique le transfert automatique que les administrateurs peuvent configurer sur une boîte aux lettres, comme décrit dans [configurer le transfert du courrier pour une boîte aux lettres](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding).</span><span class="sxs-lookup"><span data-stu-id="d7d8e-111">**By SMTP forwarding** : This method indicates automatic forwarding that admins can configure on a mailbox as described in [Configure email forwarding for a mailbox](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding).</span></span>
  - <span data-ttu-id="d7d8e-112">Un lien vers le [rapport de transfert](view-mail-flow-reports.md#forwarding-report) pour plus de détails.</span><span class="sxs-lookup"><span data-stu-id="d7d8e-112">A link to the [Forwarding report](view-mail-flow-reports.md#forwarding-report) for more details.</span></span>

- <span data-ttu-id="d7d8e-113">**Messages transférés automatiquement par les domaines et les utilisateurs** :</span><span class="sxs-lookup"><span data-stu-id="d7d8e-113">**Auto-forwarded messages by domains and users** :</span></span>

  - <span data-ttu-id="d7d8e-114">**5 principaux domaines transférés vers**</span><span class="sxs-lookup"><span data-stu-id="d7d8e-114">**Top 5 domains forwarded to**</span></span>
  - <span data-ttu-id="d7d8e-115">**Nouveaux domaines (semaine dernière)**</span><span class="sxs-lookup"><span data-stu-id="d7d8e-115">**New domains (last week)**</span></span>
  - <span data-ttu-id="d7d8e-116">**Les 5 principaux utilisateurs de transfert**</span><span class="sxs-lookup"><span data-stu-id="d7d8e-116">**Top 5 forwarding users**</span></span>
  - <span data-ttu-id="d7d8e-117">**Nouveaux utilisateurs (semaine dernière)**</span><span class="sxs-lookup"><span data-stu-id="d7d8e-117">**New users (last week)**</span></span>
  - <span data-ttu-id="d7d8e-118">Un lien vers le [rapport des modifications de transfert](mfi-new-users-forwarding-email.md#forwarding-modifications-report) pour plus de détails.</span><span class="sxs-lookup"><span data-stu-id="d7d8e-118">A link to the [Forwarding modifications report](mfi-new-users-forwarding-email.md#forwarding-modifications-report) for more details.</span></span>

![Fenêtre mobile des détails pour le rapport de messages transférés automatiquement dans le centre de sécurité & conformité](../../media/mfi-auto-forwarded-messages-details.png)

## <a name="insights"></a><span data-ttu-id="d7d8e-120">Informations</span><span class="sxs-lookup"><span data-stu-id="d7d8e-120">Insights</span></span>

<span data-ttu-id="d7d8e-121">Deux analyses sont générées en fonction des données de rapport :</span><span class="sxs-lookup"><span data-stu-id="d7d8e-121">Two insights are generated based on the report data:</span></span>

- [<span data-ttu-id="d7d8e-122">Nouveaux utilisateurs transférant le courrier électronique</span><span class="sxs-lookup"><span data-stu-id="d7d8e-122">New users forwarding email</span></span>](mfi-new-users-forwarding-email.md)
- [<span data-ttu-id="d7d8e-123">Nouveaux domaines en cours de transmission de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="d7d8e-123">New domains being forwarded email</span></span>](mfi-new-domains-being-forwarded-email.md)

## <a name="see-also"></a><span data-ttu-id="d7d8e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7d8e-124">See also</span></span>

<span data-ttu-id="d7d8e-125">Pour plus d’informations sur les autres informations du tableau de bord de flux de messagerie, consultez [la rubrique mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="d7d8e-125">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
