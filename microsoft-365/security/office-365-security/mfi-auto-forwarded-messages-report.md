---
title: Aperçu des messages transférés automatiquement
f1.keywords:
- NOCSH
ms.author: siosulli
author: siosulli
manager: dansimp
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
ms.assetid: b5543faa-44fa-44c5-8180-fb835e7e452d
description: Les administrateurs peuvent en savoir plus sur le rapport des messages transmis automatiquement dans le tableau de bord de flux de messagerie du Centre de sécurité & conformité.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 75cf060d9a597bb991fc8af2c4c70f9ecc592ad7
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50929359"
---
# <a name="auto-forwarded-messages-insight-in-the-security--compliance-center"></a><span data-ttu-id="a07ac-103">Informations sur les messages transmis automatiquement dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="a07ac-103">Auto-forwarded messages insight in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="a07ac-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="a07ac-104">**Applies to**</span></span>
- [<span data-ttu-id="a07ac-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="a07ac-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="a07ac-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="a07ac-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="a07ac-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a07ac-107">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

<span data-ttu-id="a07ac-108">Les informations sur les **messages** transmis automatiquement dans le tableau de bord de flux de messagerie dans le Centre de sécurité & conformité affichent des informations sur les messages qui sont automatiquement transmis à partir de votre organisation à des destinataires dans des [domaines](https://protection.office.com) externes. [](mail-flow-insights-v2.md)</span><span class="sxs-lookup"><span data-stu-id="a07ac-108">The **Auto-forwarded messages** insight in the [Mail flow dashboard](mail-flow-insights-v2.md) in the [Security & Compliance Center](https://protection.office.com) displays information about messages that are automatically forwarded from your organization to recipients in external domains.</span></span>

![Widget de messages transmis automatiquement dans le Centre de sécurité & conformité](../../media/mfi-auto-forwarded-messages.png)

## <a name="auto-forwarded-messages-details"></a><span data-ttu-id="a07ac-110">Détails des messages transmis automatiquement</span><span class="sxs-lookup"><span data-stu-id="a07ac-110">Auto-forwarded messages details</span></span>

<span data-ttu-id="a07ac-111">Lorsque vous cliquez sur le nombre de messages dans le widget, un volet volant s’affiche, qui affiche plus d’informations sur les messages transmis automatiquement :</span><span class="sxs-lookup"><span data-stu-id="a07ac-111">When you click the number of messages in the widget, a flyout pane appears that shows more information about the auto-forwarded messages:</span></span>

- <span data-ttu-id="a07ac-112">**Les messages transmis automatiquement par les méthodes de forwarding**:</span><span class="sxs-lookup"><span data-stu-id="a07ac-112">**Auto-forwarded messages by forwarding methods**:</span></span>

  - <span data-ttu-id="a07ac-113">**Par règles de flux de messagerie**</span><span class="sxs-lookup"><span data-stu-id="a07ac-113">**By mail flow rules**</span></span>
  - <span data-ttu-id="a07ac-114">**Par règles de boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="a07ac-114">**By Inbox rules**</span></span>
  - <span data-ttu-id="a07ac-115">**Par le forwarding SMTP**: cette méthode indique le forwarding automatique que les administrateurs peuvent configurer sur une boîte aux lettres comme décrit dans Configurer le forwarding de courrier pour [une boîte aux lettres.](/Exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)</span><span class="sxs-lookup"><span data-stu-id="a07ac-115">**By SMTP forwarding**: This method indicates automatic forwarding that admins can configure on a mailbox as described in [Configure email forwarding for a mailbox](/Exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding).</span></span>
  - <span data-ttu-id="a07ac-116">Lien vers le rapport [de report pour](view-mail-flow-reports.md#forwarding-report) plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a07ac-116">A link to the [Forwarding report](view-mail-flow-reports.md#forwarding-report) for more details.</span></span>

- <span data-ttu-id="a07ac-117">**Messages transmis automatiquement par les domaines et les utilisateurs**:</span><span class="sxs-lookup"><span data-stu-id="a07ac-117">**Auto-forwarded messages by domains and users**:</span></span>

  - <span data-ttu-id="a07ac-118">**5 principaux domaines vers**</span><span class="sxs-lookup"><span data-stu-id="a07ac-118">**Top 5 domains forwarded to**</span></span>
  - <span data-ttu-id="a07ac-119">**Nouveaux domaines (dernière semaine)**</span><span class="sxs-lookup"><span data-stu-id="a07ac-119">**New domains (last week)**</span></span>
  - <span data-ttu-id="a07ac-120">**5 principaux utilisateurs de forwarding**</span><span class="sxs-lookup"><span data-stu-id="a07ac-120">**Top 5 forwarding users**</span></span>
  - <span data-ttu-id="a07ac-121">**Nouveaux utilisateurs (semaine dernière)**</span><span class="sxs-lookup"><span data-stu-id="a07ac-121">**New users (last week)**</span></span>
  - <span data-ttu-id="a07ac-122">Lien vers le rapport [de modifications de report pour](mfi-new-users-forwarding-email.md#forwarding-modifications-report) plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a07ac-122">A link to the [Forwarding modifications report](mfi-new-users-forwarding-email.md#forwarding-modifications-report) for more details.</span></span>

![Volant de détails pour le rapport des messages transmis automatiquement dans le Centre de sécurité & conformité](../../media/mfi-auto-forwarded-messages-details.png)

## <a name="insights"></a><span data-ttu-id="a07ac-124">Connaissances</span><span class="sxs-lookup"><span data-stu-id="a07ac-124">Insights</span></span>

<span data-ttu-id="a07ac-125">Deux informations sont générées en fonction des données du rapport :</span><span class="sxs-lookup"><span data-stu-id="a07ac-125">Two insights are generated based on the report data:</span></span>

- [<span data-ttu-id="a07ac-126">Nouveaux utilisateurs qui envoient du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="a07ac-126">New users forwarding email</span></span>](mfi-new-users-forwarding-email.md)
- [<span data-ttu-id="a07ac-127">Nouveaux domaines en cours de envoi de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="a07ac-127">New domains being forwarded email</span></span>](mfi-new-domains-being-forwarded-email.md)

## <a name="see-also"></a><span data-ttu-id="a07ac-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a07ac-128">See also</span></span>

<span data-ttu-id="a07ac-129">Pour plus d’informations sur d’autres informations dans le tableau de bord de flux de messagerie, voir Informations sur le flux de messagerie dans le Centre de sécurité [& conformité.](mail-flow-insights-v2.md)</span><span class="sxs-lookup"><span data-stu-id="a07ac-129">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>