---
title: Informations sur le flux de messagerie sortant et entrant dans le tableau de bord flux de messagerie
f1.keywords:
- NOCSH
ms.author: siosulli
author: siosulli
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
ms.assetid: f2738dec-41b0-43c4-b814-84c0a4e45c6d
description: Les administrateurs peuvent en savoir plus sur les informations sur le flux de messagerie sortant et entrant dans le tableau de bord flux de messagerie du Centre de sécurité & conformité.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 4a3117223e466a4a7aad7edf25ecdbcf0a3de719
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204136"
---
# <a name="outbound-and-inbound-mail-flow-insight-in-the-security--compliance-center"></a><span data-ttu-id="80263-103">Informations sur le flux de messagerie sortant et entrant dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="80263-103">Outbound and inbound mail flow insight in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="80263-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="80263-104">**Applies to**</span></span>
- [<span data-ttu-id="80263-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="80263-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="80263-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="80263-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="80263-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="80263-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="80263-108">L’aperçu du flux de messagerie [](mail-flow-insights-v2.md) sortant et entrant dans le tableau de bord flux [](view-mail-flow-reports.md#connector-report) de messagerie dans le Centre de sécurité [&](https://protection.office.com) conformité combine les informations du rapport connecteur et de l’ancien rapport de vue d’ensemble **TLS** à un seul endroit. </span><span class="sxs-lookup"><span data-stu-id="80263-108">The **Outbound and inbound mail flow** insight in the [Mail flow dashboard](mail-flow-insights-v2.md) in the [Security & Compliance Center](https://protection.office.com) combines the information from the [Connector report](view-mail-flow-reports.md#connector-report) and the former **TLS overview report** in one place.</span></span>

<span data-ttu-id="80263-109">Le widget affiche le chiffrement TLS utilisé pour la connexion lorsque des messages sont remis à et depuis votre organisation.</span><span class="sxs-lookup"><span data-stu-id="80263-109">The widget displays the TLS encryption that's used for the connection when messages are delivered to and from your organization.</span></span> <span data-ttu-id="80263-110">Les connexions établies avec d’autres services de messagerie sont chiffrées par TLS lorsque TLS est proposé par les deux côtés.</span><span class="sxs-lookup"><span data-stu-id="80263-110">The connections that are established with other email services are encrypted by TLS when TLS is offered by both sides.</span></span> <span data-ttu-id="80263-111">Le widget offre un instantané de la dernière semaine de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="80263-111">The widget offers a snapshot of the last week of mail flow.</span></span>

![Widget de flux de messagerie sortant et entrant dans le tableau de bord de flux de messagerie dans le Centre de sécurité & conformité](../../media/mfi-outbound-and-inbound-mail-flow-report-widget.png)

<span data-ttu-id="80263-113">Les informations du widget sont liées aux connecteurs et à la protection des messages TLS Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="80263-113">The information in the widget is related to connectors and TLS message protection in Microsoft 365.</span></span> <span data-ttu-id="80263-114">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="80263-114">For more information, see these topics:</span></span>

- [<span data-ttu-id="80263-115">Configurer le flux de messagerie à l’aide des connecteurs</span><span class="sxs-lookup"><span data-stu-id="80263-115">Configure mail flow using connectors</span></span>](/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow)
- [<span data-ttu-id="80263-116">Mode d’utilisation de TLS par Exchange Online pour sécuriser les connexions de messagerie</span><span class="sxs-lookup"><span data-stu-id="80263-116">How Exchange Online uses TLS to secure email connections</span></span>](../../compliance/exchange-online-uses-tls-to-secure-email-connections.md)
- [<span data-ttu-id="80263-117">Informations de référence technique sur le chiffrement dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="80263-117">Technical reference details about encryption in Microsoft 365</span></span>](../../compliance/technical-reference-details-about-encryption.md)

## <a name="message-protected-in-transit-by-tls"></a><span data-ttu-id="80263-118">Message protégé en transit (par TLS)</span><span class="sxs-lookup"><span data-stu-id="80263-118">Message protected in transit (by TLS)</span></span>

<span data-ttu-id="80263-119">Lorsque vous cliquez sur Afficher les **détails** sur le widget, le volant Message protégé en **transit (par TLS)** vous présente la protection TLS pour les messages entrants et sortants de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="80263-119">When you click **View Details** on the widget, the **Message protected in transit (by TLS)** flyout shows you the TLS protection for messages entering and leaving your organization.</span></span>

![Message protégé en transit (par TLS) qui s’affiche après que vous avez cliqué sur Afficher les détails sur le widget de messagerie sortant et entrant](../../media/mfi-outbound-and-inbound-mail-flow-report-details.png)

<span data-ttu-id="80263-121">Actuellement, TLS 1.2 est la version de TLS la plus sécurisée proposée par les Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="80263-121">Currently, TLS 1.2 is the most secure version of TLS that's offered by Microsoft 365.</span></span> <span data-ttu-id="80263-122">Souvent, vous devez connaître le chiffrement TLS utilisé pour les audits de conformité.</span><span class="sxs-lookup"><span data-stu-id="80263-122">Often, you'll need to know the TLS encryption that's being used for compliance audits.</span></span> <span data-ttu-id="80263-123">Vous n’avez probablement pas de relation directe avec la plupart des serveurs de messagerie source et de destination (vous ne les possédez pas, et Microsoft non plus), vous n’avez donc pas beaucoup d’options pour améliorer le chiffrement TLS utilisé par ces serveurs.</span><span class="sxs-lookup"><span data-stu-id="80263-123">You probably don't have a direct relationship with most of the source and destination email servers (you don't own them, and neither does Microsoft), so you don't have many options to improve the TLS encryption that's used by those servers.</span></span>

<span data-ttu-id="80263-124">Toutefois, vous pouvez utiliser des [connecteurs](/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) pour garantir la meilleure protection TLS disponible pour les messages envoyés entre vos serveurs de messagerie et Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="80263-124">But, you can use [connectors](/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) to ensure the best available TLS protection for messages that are sent between your email servers and Microsoft 365.</span></span> <span data-ttu-id="80263-125">Le flux de messagerie entre Microsoft 365 et vos propres serveurs de messagerie ou serveurs qui appartiennent à vos partenaires est souvent plus important et sensible que les messages ordinaires. Vous pouvez donc appliquer une sécurité et un niveau de sécurité supplémentaires à ces messages.</span><span class="sxs-lookup"><span data-stu-id="80263-125">Mail flow between Microsoft 365 and your own email servers or servers that belong to your partners is often more important and sensitive than regular messages, so you'll want to apply extra security and vigilance to those messages.</span></span>

<span data-ttu-id="80263-126">Vous pouvez mettre à niveau ou corriger vos propres serveurs de messagerie pour améliorer le chiffrement TLS utilisé, ou contactez vos partenaires pour en faire de même.</span><span class="sxs-lookup"><span data-stu-id="80263-126">You can upgrade or fix your own email servers to improve the TLS encryption that's being used, or reach out to your partners to do the same.</span></span> <span data-ttu-id="80263-127">Le **rapport connecteur affiche** à la fois le volume de flux de messagerie et le chiffrement TLS pour les messages qui utilisent Microsoft 365 connecteurs.</span><span class="sxs-lookup"><span data-stu-id="80263-127">The **Connector Report** displays both mail flow volume and TLS encryption for messages that use your Microsoft 365 connectors.</span></span>

<span data-ttu-id="80263-128">Vous pouvez cliquer sur **le lien du rapport connecteur** pour y [aller.](view-mail-flow-reports.md#connector-report)</span><span class="sxs-lookup"><span data-stu-id="80263-128">You can click the **Connector report** link to go to the [Connector report](view-mail-flow-reports.md#connector-report).</span></span> <span data-ttu-id="80263-129">Les informations suivantes peuvent être disponibles sur la page de rapport **connecteur** si la condition associée a été détectée :</span><span class="sxs-lookup"><span data-stu-id="80263-129">The following insights might be available on the **Connector report** page if the associated condition has been detected:</span></span>

- <span data-ttu-id="80263-130">**Connecteur partenaire entrant avec un flux de messagerie TLS1.0 important**</span><span class="sxs-lookup"><span data-stu-id="80263-130">**Inbound Partner connector seeing significant TLS1.0 mail flow**</span></span>
- <span data-ttu-id="80263-131">**Connecteur OnPremises entrant avec un flux de messagerie TLS1.0 important**</span><span class="sxs-lookup"><span data-stu-id="80263-131">**Inbound OnPremises connector seeing significant TLS1.0 mail flow**</span></span>

<span data-ttu-id="80263-132">Pour les connexions TLS 1.0, vous devez vraiment mettre à niveau ou corriger votre serveur de messagerie ou le serveur de votre partenaire afin d’éviter tout problème lorsque la prise en charge de TLS 1.0 est finalement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="80263-132">For TLS 1.0 connections, you really need to get your email server or your partner's server upgraded or fixed to avoid any issues when TLS 1.0 support is eventually deprecated in Microsoft 365.</span></span>

## <a name="see-also"></a><span data-ttu-id="80263-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80263-133">See also</span></span>

<span data-ttu-id="80263-134">Pour plus d’informations sur d’autres informations dans le tableau de bord de flux de messagerie, voir Informations sur le flux de messagerie dans le Centre de sécurité [& conformité.](mail-flow-insights-v2.md)</span><span class="sxs-lookup"><span data-stu-id="80263-134">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>